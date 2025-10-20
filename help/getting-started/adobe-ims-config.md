---
title: ID를 사용하여 Commerce 관리 통합 구성
description: Adobe Commerce Admin 사용자 계정 로그인을 Adobe ID과 통합하려면 이 선택적 절차를 따르십시오.
exl-id: 518b7c21-e6b3-47d7-81a5-c34fbe0f197c
feature: Identity Management
badgePaas: label="PaaS만" type="Informative" url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="Adobe Commerce 온 클라우드 프로젝트(Adobe 관리 PaaS 인프라) 및 온프레미스 프로젝트에만 적용됩니다."
source-git-commit: a71f3ba94229c402421ee476c37cfcbfd88a26c7
workflow-type: tm+mt
source-wordcount: '817'
ht-degree: 0%

---

# Adobe ID과 Commerce Admin Integration 구성

{{ee-feature}}

이 통합은 Commerce을 보유하고 있고 Adobe Commerce 및 Adobe Business 제품에 대한 로그인을 간소화하려는 관리자 권한이 있는 Adobe ID 판매자를 지원합니다. 선택 사항이며 인스턴스별로 활성화되어 있습니다. 활성화된 경우 관리자 사용자 워크플로우만 영향을 받습니다. 

>[!IMPORTANT]
>
>관리자 사용자는 이 통합을 활성화하기 전에 Commerce 관리자 자격 증명(사용자 이름 및 암호)과 2FA 자격 증명을 저장해야 합니다. IMS 통합이 비활성화된 경우 이러한 자격 증명이 필요합니다.

## 사전 요구 사항

* Adobe Commerce 2.4.5 이상
* [Adobe Admin Console](https://adminconsole.adobe.com/)에 액세스할 수 있는 Adobe.com 계정입니다.

이 통합을 구성하는 관리자는 모듈을 사용하는 동안 다음 자격 증명이 필요합니다.

* 조직 ID([Adobe Admin Console](https://adminconsole.adobe.com/)에서 가져옴)이며, 길이는 24자 이상이어야 합니다. 인증된 사용자는 이 IMS 조직에 속해야 합니다. 조직 ID 찾기에 대한 자세한 내용은 [Experience Cloud의 조직](https://experienceleague.adobe.com/docs/core-services/interface/administration/organizations.html)을 참조하세요.
* 2FA는 모듈을 활성화하기 위해 Adobe Admin Console의 조직 수준에서 적용되어야 합니다. [인증 설정](https://helpx.adobe.com/enterprise/using/authentication-settings.html#two-step-verification)을 확인하세요.
* 클라이언트 ID
* 클라이언트 암호
* [Adobe Developer Console](https://developer.adobe.com/developer-console/docs/guides/credentials/)에서 API 키를 검색한 후 클라이언트 ID 및 클라이언트 암호를 사용할 수 있습니다.

Commerce Admin 사용자는 로그인하려면 Adobe ID으로 계정을 만들어야 합니다.

## 일반 단계

* [Adobe](https://adminconsole.adobe.com/)에서 Adobe Admin Console 조직 ID 가져오기
* [Adobe Developer Console](https://developer.adobe.com/)에서 새 프로젝트, IMS API 키 및 암호를 생성합니다.
* Adobe Admin Console에서 Adobe Commerce 사용자 구성
* `AdminAdobeIms` 모듈을 사용하도록 설정합니다.

통합이 성공하려면 모든 Adobe Commerce 사용자에게 동일한 이름과 기본 이메일 주소를 사용하는 관리자 사용자 계정이 있어야 합니다. 일치하는 관리자 사용자 계정이 없는 경우 필수 권한이 있는 사용자(일반적으로 관리자 역할이 할당됨)는 동일한 이름 및 전자 메일을 사용하여 수동으로 [관리자 사용자 계정을 만듭니다](../systems/permissions-users-all.md#create-a-user).

## 통합 구성

시스템 액세스 권한이 있는 관리자 또는 개발자가 다음 단계를 완료하면 모든 관리자의 Commerce 관리자 로그인 페이지에 _[!UICONTROL Sign into Adobe Commerce with Adobe IMS]_&#x200B;단추가 표시됩니다.

### 1단계: Adobe 조직 ID 가져오기

이 기능을 사용하려면 하나 이상의 IMS 조직 멤버십이 필요합니다. Adobe ID이 있는 경우 기본적으로 하나 이상의 Adobe 조직에 속합니다. 조직 ID를 검색하려면 [Adobe Admin Console](https://adminconsole.adobe.com/)에 로그인하십시오.

### 2단계: 새 프로젝트, IMS API 키 및 암호 생성

조직에 대한 프로젝트를 생성하려면 조직의 Adobe 관리자 계정에 시스템 관리자 또는 개발자 역할이 있어야 합니다. [Developer Console 안내서](https://developer.adobe.com/developer-console/docs/guides/projects/)를 참조하세요.

1. [Adobe Developer Console](https://developer.adobe.com/)에 로그인합니다.
1. **[!UICONTROL Projects]** 탭(adobe.io/projects)으로 이동하여 **[!UICONTROL Create a new project]**&#x200B;을(를) 클릭합니다.
1. 새로 만든 프로젝트 페이지에서 **[!UICONTROL Add API]**&#x200B;을(를) 클릭합니다.
1. **[!UICONTROL Adobe Services]** > **[!UICONTROL Adobe Commerce with Adobe ID]**&#x200B;을(를) 선택합니다.
1. **[!UICONTROL Oauth 2.0 Web]**&#x200B;을(를) 선택합니다.
1. **[!UICONTROL Redirect URI]** 지정: `https://<commerce_base_url>/`
1. **[!UICONTROL Redirect URI pattern]** 지정: `https://<commerce_base_url>/.*`

   `\\`(으)로 점 앞에 추가하여 호스트 이름에서 점을 이스케이프 처리합니다. URL 끝에 와일드카드를 추가하면 Adobe Commerce 관리자 비밀 키가 지원됩니다.

1. **[!UICONTROL Save configured API]**&#x200B;을(를) 클릭합니다.
1. 생성된 프로젝트에서 [!UICONTROL Client ID] 및 [!UICONTROL Client Secret] 키를 복사합니다.

### 3단계: Adobe Admin Console에서 Adobe Commerce 사용자 구성

통합을 활성화하기 전에 각 Adobe Commerce 관리자 계정에 해당 Adobe IMS 계정이 있는지 확인하십시오. Adobe ID을 사용하여 로그인하려면 Adobe Commerce 사용자가 특정 Adobe 조직에 속해 있어야 합니다.

>[!TIP]
>
>CSV 파일에서 사용자 정보를 업로드하여 여러 사용자 계정을 만들 수 있습니다. [여러 사용자 관리](https://helpx.adobe.com/enterprise/using/bulk-upload-users.html)를 참조하십시오.

1. [Adobe Admin Console](https://helpx.adobe.com/enterprise/using/admin-console.html)에서 **[!UICONTROL Users]** > **[!UICONTROL Users]**(으)로 이동합니다.

1. **[!UICONTROL Add User]**&#x200B;을(를) 클릭합니다.

1. 사용자의 이메일 주소를 입력합니다.

   해당하는 경우 권장 ID 유형이 자동으로 채워집니다. 이 설정을 조직의 구매 계획을 기반으로 하는 목록의 제품 ID 중 하나로 변경할 수 있습니다.

   한 번에 최대 10명의 사용자를 추가할 수 있습니다. 더 추가하려면 변경 내용을 저장한 후 이전 단계를 반복합니다.

1. **[!UICONTROL Save]**&#x200B;을(를) 클릭합니다.

사용자가 추가되어 [!UICONTROL Users] 목록에 표시됩니다.

### 4단계: AdminAdobeIms 모듈 활성화

`AdminAdobeIms` 모듈은 Adobe Commerce/Adobe IMS 통합을 담당합니다. 새 프로젝트를 설정하고 조직 ID, 클라이언트 ID 및 클라이언트 암호를 복사한 후 `AdminAdobeIms` 모듈을 사용하도록 설정할 수 있습니다.

`bin/magento admin:adobe-ims:enable` 입력. 다음 매개변수를 입력하라는 메시지가 표시됩니다. 프로젝트를 만드는 동안 생성된 값을 사용합니다.

* 조직 ID
* 클라이언트 ID
* 클라이언트 암호
* 2FA 사용

Adobe Commerce에 활성화 성공 또는 실패 여부를 나타내는 메시지가 표시됩니다.

이 기능을 활성화하면 다른 Adobe Commerce 사용자 계정을 Adobe IMS 계정으로 전환할 수 있습니다. Adobe ID을 사용하여 로그인하려면 Adobe Commerce 사용자가 구성된 Adobe 조직에 속해 있어야 합니다.

## ID 및 SSO(Single Sign-On)

Adobe ID, Enterprise ID 및 Federated ID을 포함한 ID 구성 옵션과 Adobe 앱에 대한 보안 액세스를 위해 SSO(Single Sign-On)를 구성하는 방법에 대한 자세한 내용은 [Enterprise Admin Console](https://helpx.adobe.com/enterprise/using/set-up-identity.html) 설명서의 *ID 및 SSO 설정*&#x200B;을 참조하십시오.
