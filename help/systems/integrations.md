---
title: 통합
description: 서드파티 통합을 위해 OAuth 자격 증명 및 리디렉션 URL을 구성하는 방법에 대해 알아봅니다.
exl-id: b7632994-b07b-4cdb-b62c-79bc7a3a01c8
role: Admin, Developer
feature: System, Integration, Configuration
source-git-commit: 64ccc2d5016e915a554c2253773bb50f4d33d6f4
workflow-type: tm+mt
source-wordcount: '521'
ht-degree: 0%

---

# 통합

Commerce 관리에서 통합을 정의하면 서드파티 통합을 위한 OAuth 자격 증명 및 리디렉션 URL의 위치가 설정되고 통합에 필요한 사용 가능한 API 리소스가 식별됩니다. 통합 등록 프로세스에 대한 자세한 내용은 [OAuth 기반 인증](https://developer.adobe.com/commerce/webapi/get-started/authentication/gs-authentication-oauth/) Commerce 개발자 설명서에서 참조하십시오.

![통합](./assets/integrations.png){width="700" zoomable="yes"}

## 온보딩 워크플로우

1. **통합 승인** - 다음으로 이동 **[!UICONTROL System]** > _[!UICONTROL Extensions]_>**[!UICONTROL Integrations]**페이지를 열고 관련 통합을 찾은 다음 권한을 부여합니다.
1. **로그인 확인 및 설정** - 메시지가 표시되면 요청된 액세스 권한을 수락합니다. 서드파티로 리디렉션되면 시스템에 로그인하거나 계정을 만듭니다. 로그인에 성공하면 통합 페이지로 돌아갑니다.
1. **인증된 통합 확인 받기** - 통합이 승인되었다는 알림이 전송됩니다. 통합을 설정하고 자격 증명을 받은 후 더 이상 액세스 또는 요청 토큰에 대한 호출을 수행할 필요가 없습니다.

## 통합 추가

1. 다음에서 _관리자_ 사이드바, 이동 **[!UICONTROL System]** > _[!UICONTROL Extensions]_>**[!UICONTROL Integrations]**.

   ![새로운 통합](./assets/integration-new.png){width="600" zoomable="yes"}

1. 다음 통합 정보를 입력합니다.

   - 다음을 입력합니다. **[!UICONTROL Name]** 통합 및 연락처 **[!UICONTROL Email]** 주소.

   - 다음을 입력합니다. **[!UICONTROL Callback URL]** 토큰 교환에 OAuth를 사용할 때 OAuth 자격 증명을 보낼 수 있는 경우. 사용 `https://` 이 권장됩니다.

   - 다음을 입력합니다. **[!UICONTROL Identity Link URL]** 이러한 Adobe Commerce 또는 Magento Open Source 통합 자격 증명을 사용하여 사용자를 서드파티 계정으로 리디렉션합니다.

   >[!NOTE]
   >
   > 다음 `Integration not secure` 경고 레이블은 의 각 통합 이름 근처에 표시됩니다 [!UICONTROL Integrations] HTTPS URL이 저장될 때까지 그리드 미리 알림 [!UICONTROL Callback URL] 및 [!UICONTROL Identity Link URL] 필드.

   - 메시지가 표시되면 암호를 입력하여 ID를 확인합니다.

1. 왼쪽 패널에서 을 선택합니다 **[!UICONTROL API]** 다음을 수행합니다.

   - 설정 **[!UICONTROL Resource Access]** 다음 중 하나를 수행합니다.

      - `All`
      - `Custom`

   - 사용자 지정 액세스의 경우 필요한 각 리소스의 확인란을 선택합니다.

     ![통합 - 사용 가능한 API](./assets/integrations-available-api.png){width="600" zoomable="yes"}

1. 완료되면 다음을 클릭하십시오. **[!UICONTROL Save]**.

## 통합 활성화

기본적으로 저장된 통합은 `Inactive` 상태. 활성화하려면 다음 단계를 완료하십시오.

1. 다음에서 _관리자_ 사이드바, 이동 **[!UICONTROL System]** > _[!UICONTROL Extensions]_>**[!UICONTROL Integrations]**.

1. 새로 생성된 통합을 찾고 **[!UICONTROL Activate]** 링크를 클릭합니다.

1. 오른쪽 위 모서리에서 을(를) 클릭합니다. **[!UICONTROL Allow]**.

   이 작업은 확장을 위한 통합 토큰을 표시합니다. 이 정보를 통합에 사용할 안전하고 암호화된 위치에 복사합니다.

   ![확장을 위한 통합 토큰](./assets/integration-tokens-for-extensions.png){width="600" zoomable="yes"}

1. 오른쪽 위 모서리에서 을(를) 클릭합니다. **[!UICONTROL Done]**.

## 통합 재인증

새 통합 액세스 토큰 및 액세스 토큰 암호를 생성하려면 관리자로부터 통합을 다시 승인하십시오.

1. 다음에서 _관리자_ 사이드바, 이동 **[!UICONTROL System]** > _[!UICONTROL Extensions]_>**[!UICONTROL Integrations]**.

1. 과의 통합 찾기 **[!UICONTROL Active]** 상태.

1. 위치 _[!UICONTROL Activate]_열을 클릭하고&#x200B;**[!UICONTROL Reauthorize]**.

1. 클릭 **[!UICONTROL Reauthorize]** API 리소스에 대한 액세스를 승인합니다.

1. 확장에 대한 새 통합 토큰을 저장하고 **[!UICONTROL Done]**.

## API 게스트 액세스 보안 설정 변경

기본적으로 시스템에서는 CMS, 카탈로그 및 기타 저장소 리소스에 대한 익명 게스트 액세스를 허용하지 않습니다. 설정을 변경해야 하는 경우 다음을 수행합니다.

1. 다음에서 _관리자_ 사이드바, 이동 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. 왼쪽 패널에서 를 확장합니다. **[!UICONTROL Services]** 및 선택 **[!UICONTROL Magento Web API]**.

1. 확장 ![확장 선택기](../assets/icon-display-expand.png) 다음 **[!UICONTROL Web API Security Setting]** 섹션.

   ![서비스 구성 - 웹 API 보안 설정](../configuration-reference/services/assets/web-api-security.png){width="600" zoomable="yes"}

1. 설정 **[!UICONTROL Allow Anonymous Guest Access]** 끝 `Yes`.

1. 완료되면 다음을 클릭하십시오. **[!UICONTROL Save Config]**.

자세한 내용은 [익명 웹 API에 대한 액세스 제한](https://developer.adobe.com/commerce/webapi/rest/use-rest/anonymous-api-security/) Commerce 개발자 설명서에서 참조하십시오.

## 통합 삭제

1. 다음에서 _관리자_ 사이드바, 이동 **[!UICONTROL System]** > _[!UICONTROL Extensions]_>**[!UICONTROL Integrations]**.

1. 기존 통합을 찾고 아이콘( ![휴지통 아이콘](../assets/icon-delete-trashcan-solid.png) )에 있는 **[!UICONTROL Delete]** 열.

1. 작업을 확인하려면 **[!UICONTROL OK]**.
