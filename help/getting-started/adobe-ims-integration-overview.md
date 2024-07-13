---
title: Adobe Identity Management 서비스(IMS) 통합 개요
description: Adobe Commerce Admin 로그인과 Adobe IMS의 선택적 통합을 소개합니다.
exl-id: 106d731c-a541-4a19-a38c-221e80740508
feature: Identity Management
source-git-commit: 3ff5807fd0a3ebf2e9d4f9c085852dd7777a1103
workflow-type: tm+mt
source-wordcount: '767'
ht-degree: 0%

---

# Adobe Identity Management 서비스(IMS) 통합 개요

{{ee-feature}}

이제 Adobe 계정이 있는 Adobe Commerce 관리자 사용자는 Adobe ID을 사용하여 Adobe Commerce에 로그인할 수 있습니다. IMS(Adobe Identity Management 서비스)는 인증을 지원하는 Adobe의 OAuth 2.0 기반 ID 관리 기능입니다. Commerce 관리 인증을 Adobe 비즈니스 제품의 IMS 인증 워크플로에 통합하면 다른 Adobe 제품과 함께 작업하는 사용자의 인증 프로세스를 간소화할 수 있습니다. 이 통합은 선택 사항이며 인스턴스별로 활성화되어 있습니다. 이 통합이 활성화되면 관리자 사용자 워크플로우만 영향을 받습니다. 

Commerce Admin IMS 통합에 필요한 모듈은 Adobe Commerce 핵심 릴리스와 번들로 제공되는 `adobe-ims-metapackage`에 패키지되어 있습니다.

이 통합을 구현하려면 [IMS와 Commerce Admin 통합 구성](./adobe-ims-config.md)을 참조하세요.

## IMS와 통합 후 관리 워크플로우 및 인터페이스 변경 사항

이 통합이 활성화되면 Commerce 관리자 사용자는 관리자에서 관리자 사용자를 만드는 것과 같이 재인증이 필요한 일상적인 작업을 수행할 때 기본 Commerce 관리자 로그인 및 인증 워크플로가 변경됩니다. 모듈을 사용하려면 Adobe 조직 수준에서 2단계 인증(2FA)을 적용해야 합니다. 기본 관리자 로그인 및 2FA가 비활성화되고 _[!UICONTROL Sign In with Adobe ID]_단추가 기본 관리자 로그인 양식을 대체합니다. 권한은 여전히 관리자로부터 관리됩니다.

## IMS와 Admin 통합이 Commerce 암호에 미치는 영향

Adobe IMS와 통합된 Commerce 배포에서는 IMS 활성화 프로세스 동안 Commerce 애플리케이션에 대해 구성된 Adobe IMS 조직에 액세스할 수 있는 Adobe ID 계정이 필요합니다.  IMS 통합이 활성화되면 관리자는 Adobe 자격 증명을 사용하여 Adobe 로그인 페이지를 통해 인증합니다. Adobe IMS 통합이 활성화되어 있는 한 관리자의 Commerce 암호 및 사용자 이름은 인증에 더 이상 사용되지 않습니다.

IMS 통합이 비활성화되면 관리자는 Adobe Commerce 사용자 이름과 암호를 사용하여 Commerce을 통해 다시 인증해야 합니다. 관리자 사용자는 이 통합을 활성화하기 전에 Commerce 관리자 자격 증명(사용자 이름 및 암호)과 2FA 자격 증명을 저장해야 합니다.

사용자 인증과 관련된 특정 백엔드 구성 요소에는 여전히 null이 아닌 암호가 필요합니다. 이 요구 사항을 충족하기 위해 Commerce은 `admin_user` 표에 새로 만든 관리자의 암호를 임의로 만듭니다.

Commerce 애플리케이션에 대한 사용자 계정 및 역할 권한은 여전히 Commerce 관리에서 관리됩니다.


## IMS 자격 증명을 사용하여 웹 API 토큰 생성

Commerce Admin API는 Adobe IMS를 사용한 관리자 인증이 Commerce 인스턴스에서 활성화되면 영향을 받습니다. 관리자 사용자는 더 이상 Commerce 인스턴스에서 발급한 자격 증명을 사용할 수 없습니다. 이들은 관리자에 로그인하고 서비스에서 관리 REST 및 SOAP API에 요청을 하는 데 사용할 수 있는 액세스 토큰을 가져오는 데 필요한 자격 증명입니다.

Adobe IMS 통합이 활성화되면 관리자는 인증이 필요한 Adobe Commerce API 엔드포인트에 대해 [Adobe IMS OAuth 토큰](https://developer.adobe.com/developer-console/docs/guides/authentication/OAuthIntegration/)을 사용해야 합니다. 클라이언트 솔루션은 웹 API 사용을 위해 토큰을 동적으로 가져옵니다. 이 인증 메커니즘은 이 통합 구성의 일부로 REST 및 SOAP 웹 API 영역에 대해 활성화됩니다.

IMS 액세스 토큰을 포함하여 웹 API에서 Commerce 액세스 토큰을 사용하는 방법에 대한 개요는 [토큰 기반 인증](https://developer.adobe.com/commerce/webapi/get-started/authentication/gs-authentication-token/)을 참조하십시오.

## Commerce 세션 관리 및 Adobe IMS 액세스 토큰

액세스 토큰에는 사용자 자격 증명과 로그인 세션 정보가 모두 포함됩니다. 사용자가 인증되고 세션이 시작되면 다음 두 변수가 사용자의 세션에 추가됩니다.

`token_last_check_time`. 현재 시간을 식별하며 `\Magento\AdminAdobeIms\Plugin\BackendAuthSessionPlugin` 플러그 인에서 사용됩니다.

`adobe_access_token` — 인증 중에 받은 `ACCESS_TOKEN` 값을 식별합니다.

`\Magento\AdminAdobeIms\Plugin\BackendAuthSessionPlugin` 플러그인은 `token_last_check_time`이(가) 10분 전에 업데이트되었는지 확인합니다. 10분 전에 `token_last_check_time`을(를) 검사한 경우 인증 워크플로우는 IMS에 API를 호출하여 액세스 토큰의 유효성을 검사하고 세션이 계속됩니다. 액세스 토큰이 올바른 경우 `token_last_check_time` 값이 현재 시간으로 업데이트됩니다. 토큰이 유효하지 않으면 세션이 종료됩니다.

## 중요 파일

`adminAdobeIms` - `AdobeImsApi` 모듈을 기반으로 관리자 로그인 구현을 제공합니다.

`admin_adobe_ims_webapi` - 유효성이 확인된 모든 액세스 토큰의 레코드를 유지 관리합니다. 토큰이 유효화되거나 무효화되면 토큰의 상태에 대한 레코드가 이 테이블에 보존됩니다.

`adobeIms` - Adobe IMS와의 통합과 관련된 모든 비즈니스 논리를 구현합니다(이전 버전과 호환되지 않도록 유지됨).

`adobeImsApi` - Adobe IMS와의 통합을 지원하는 인터페이스를 선언합니다.

`adminadobe-ims.log` - 오류 로그 파일입니다.

## 통합 활성화

Adobe IMS 메타패키지는 Adobe Commerce 2.4.5 이상 버전과 함께 설치되지만 사용할 수 있도록 구성해야 합니다. 인증 논리(`AdminAdobeIms`)를 사용하도록 설정하는 모듈을 지원하도록 `AdobeIms` 모듈을 확장합니다.

통합 활성화에 대한 자세한 내용은 [Adobe IMS와 Commerce Admin 통합 구성](./adobe-ims-config.md)을 참조하십시오.
