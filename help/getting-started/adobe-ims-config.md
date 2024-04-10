---
title: ID를 사용하여 Commerce 관리자 통합 구성
description: Adobe Commerce Admin 사용자 계정 로그인을 Adobe ID과 통합하려면 이 선택적 절차를 따르십시오.
exl-id: 518b7c21-e6b3-47d7-81a5-c34fbe0f197c
feature: Identity Management
source-git-commit: 9a9106cde5184823755fb1f44fe7eae300442abc
workflow-type: tm+mt
source-wordcount: '755'
ht-degree: 0%

---

# Adobe ID과 Commerce Admin Integration 구성

{{ee-feature}}

이 통합은 Adobe ID이 있고 Adobe Commerce 및 Adobe 비즈니스 제품에 대한 로그인을 간소화하려는 관리자 권한이 있는 상거래 상인을 지원합니다. 선택 사항이며 인스턴스별로 활성화되어 있습니다. 활성화된 경우 관리자 사용자 워크플로우만 영향을 받습니다. 

>[!IMPORTANT]
>
>관리자 사용자는 이 통합을 활성화하기 전에 상거래 관리자 자격 증명(사용자 이름 및 암호)과 2FA 자격 증명을 저장해야 합니다. IMS 통합이 비활성화된 경우 이러한 자격 증명이 필요합니다.

## 전제 조건

* Adobe Commerce 2.4.5 이상
* 다음에 대한 액세스 권한이 있는 Adobe.com 계정 [Adobe Admin Console](https://adminconsole.adobe.com/).

이 통합을 구성하는 관리자는 모듈을 사용하는 동안 다음 자격 증명이 필요합니다.

* 조직 ID(다음에서 가져옴) [Adobe Admin Console](https://adminconsole.adobe.com/)), 최소 24자 이상이어야 합니다. 인증된 사용자는 이 IMS 조직에 속해야 합니다. 조직 ID 찾기에 대한 자세한 내용은 [Experience Cloud의 조직](https://experienceleague.adobe.com/docs/core-services/interface/administration/organizations.html).
* 2FA는 모듈을 활성화하기 위해 Adobe Admin Console의 조직 수준에서 적용되어야 합니다. 확인 [인증 설정](https://helpx.adobe.com/enterprise/using/authentication-settings.html#two-step-verification).
* 클라이언트 ID
* 클라이언트 암호
* 클라이언트 ID 및 클라이언트 암호는 [Adobe Developer 콘솔](https://developer.adobe.com/developer-console/docs/guides/credentials/).

Commerce 관리자 사용자는 로그인하려면 Adobe ID으로 계정을 만들어야 합니다.

## 일반 단계

* 에서 Adobe 조직 ID 가져오기 [Adobe Admin Console](https://adminconsole.adobe.com/)
* 에서 새 프로젝트, IMS API 키 및 암호를 생성합니다. [Adobe Developer 콘솔](https://developer.adobe.com/)
* Adobe Admin Console에서 Adobe Commerce 사용자 구성
* 활성화 `AdminAdobeIms` 모듈.

통합이 성공하려면 모든 Adobe Commerce 사용자에게 동일한 이름과 기본 이메일 주소를 사용하는 관리자 사용자 계정이 있어야 합니다. 일치하는 관리자 사용자 계정이 없는 경우 필요한 권한(일반적으로 관리자 역할이 할당됨)이 있는 사용자는 수동으로 이동해야 합니다 [관리자 계정 만들기](../systems/permissions-users-all.md#create-a-user) (이름 및 이메일이 동일한 경우)

## 통합 구성

관리자 또는 시스템 액세스 권한이 있는 개발자가 다음 단계를 완료하면 _[!UICONTROL Sign into Adobe Commerce with Adobe IMS]_모든 관리자의 Commerce 관리자 로그인 페이지에 단추가 표시됩니다.

### 1단계: Adobe 조직 ID 가져오기

이 기능을 사용하려면 하나 이상의 IMS 조직 멤버십이 필요합니다. Adobe ID이 있는 경우 기본적으로 하나 이상의 Adobe 조직에 속합니다. 에 로그인합니다 [Adobe Admin Console](https://adminconsole.adobe.com/) 조직 ID를 검색합니다.

### 2단계: 새 프로젝트, IMS API 키 및 암호 생성

조직에 대한 프로젝트를 생성하려면 조직의 Adobe 관리자 계정에 시스템 관리자 또는 개발자 역할이 있어야 합니다. 다음을 참조하십시오. [Developer Console 안내서](https://developer.adobe.com/developer-console/docs/guides/projects/).

1. 에 로그인 [Adobe Developer 콘솔](https://developer.adobe.com/).
1. 로 이동 **[!UICONTROL Projects]** tab(adobe.io/projects) 및 클릭 **[!UICONTROL Create a new project]**.
1. 클릭 **[!UICONTROL Add API]** 을 참조하십시오.
1. 선택 **[!UICONTROL Adobe Services]** > **[!UICONTROL Adobe Commerce with Adobe ID]**.
1. 선택 **[!UICONTROL Oauth 2.0 Web]**.
1. 다음을 지정합니다. **[!UICONTROL Redirect URI]**: `https://<hostname>/`
1. 다음을 지정합니다. **[!UICONTROL Redirect URI pattern]**: `https://<hostname>/.*`

   점 앞에 을 추가하여 호스트 이름에서 점을 이스케이프 처리합니다. `\\`. URL 끝에 와일드카드를 추가하면 Adobe Commerce 관리자 비밀 키가 지원됩니다.

1. 클릭 **[!UICONTROL Save configured API]**.
1. 다음을 복사합니다. [!UICONTROL Client ID] 및 [!UICONTROL Client Secret] 생성된 프로젝트의 키입니다.

### 3단계: Adobe Admin Console에서 Adobe Commerce 사용자 구성

통합을 활성화하기 전에 각 Adobe Commerce 관리자 계정에 해당 Adobe IMS 계정이 있는지 확인하십시오. Adobe ID을 사용하여 로그인하려면 Adobe Commerce 사용자가 특정 Adobe 조직에 속해 있어야 합니다.

>[!TIP]
>
>CSV 파일에서 사용자 정보를 업로드하여 여러 사용자 계정을 만들 수 있습니다. 다음을 참조하십시오 [여러 사용자 관리](https://helpx.adobe.com/enterprise/using/bulk-upload-users.html).

1. 다음에서 [Adobe Admin Console](https://helpx.adobe.com/enterprise/using/admin-console.html), 다음으로 이동 **[!UICONTROL Users]**  > **[!UICONTROL Users]**.

1. 클릭 **[!UICONTROL Add User]**.

1. 사용자의 이메일 주소를 입력합니다.

   해당하는 경우 권장 ID 유형이 자동으로 채워집니다. 이 설정을 조직의 구매 계획을 기반으로 하는 목록의 제품 ID 중 하나로 변경할 수 있습니다.

   한 번에 최대 10명의 사용자를 추가할 수 있습니다. 더 추가하려면 변경 내용을 저장한 후 이전 단계를 반복합니다.

1. 클릭 **[!UICONTROL Save]**.

사용자가 추가되고에 표시됩니다. [!UICONTROL Users] 목록을 표시합니다.

### 4단계: AdminAdobeIms 모듈 활성화

다음 `AdminAdobeIms` 모듈은 Adobe Commerce/Adobe IMS 통합을 담당합니다. 새 프로젝트를 설정하고 조직 ID, 클라이언트 ID 및 클라이언트 암호를 복사한 후 `AdminAdobeIms` 모듈.

입력 `bin/magento admin:adobe-ims:enable`. 다음 매개변수를 입력하라는 메시지가 표시됩니다. 프로젝트를 만드는 동안 생성된 값을 사용합니다.

* 조직 ID
* 클라이언트 ID
* 클라이언트 암호
* 2FA 사용

Adobe Commerce에 활성화 성공 또는 실패 여부를 나타내는 메시지가 표시됩니다.

이 기능을 활성화하면 다른 Adobe Commerce 사용자 계정을 Adobe IMS 계정으로 전환할 수 있습니다. Adobe ID을 사용하여 로그인하려면 Adobe Commerce 사용자가 구성된 Adobe 조직에 속해 있어야 합니다.
