---
title: 이중 인증 관리
description: 이중 인증을 관리하고 관리자 사용자에 대한 인증자를 재설정하는 방법에 대해 알아봅니다.
exl-id: 68256214-2d50-4c42-846f-306ffc305f25
role: Admin
feature: Configuration, Security, User Account
badgePaas: label="PaaS만" type="Informative" url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="Adobe Commerce 온 클라우드 프로젝트(Adobe 관리 PaaS 인프라) 및 온프레미스 프로젝트에만 적용됩니다."
TQID: https://experienceleague.adobe.com/aE-36667-f0E4GSXDjZZmFUkS3wa-xTLUMbVtjwS6qk
product_v2: id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2: id: ba9e5be9-7de1-4f71-a5d2-baead0e425eeid: bd989d82-1e15-4534-88db-f1f51dd77ffaid: dac87252-6066-4d6e-a9d2-f6d84c323de7
subfeature_v2: id: b01a71b7-d17a-42b2-a9ac-af4b8d9d2ef5
role_v2: id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
level_v2: id: b5a62a22-46f7-4f0d-b151-3fc640bef588id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2: id: c1579802-ddd4-4214-8a91-97b2066abe11id: d095671a-1355-40aa-8b5f-06c33c68080bid: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 336
ht-degree: 0%

---

# 이중 인증 관리

2단계 인증(2FA)을 사용하여 _관리자_&#x200B;에 로그인할 수 없는 사용자는 문제를 동기화하거나 해결할 수 있습니다. 계정과 연결된 인증자를 재설정할 수도 있습니다. 재설정하면 사용자가 다시 로그인하고 필요한 인증자를 다시 구성해야 합니다.

2FA로 로그인하는 데 문제가 있는 경우 다음 사항을 고려하십시오.

- 일부 모바일 앱에는 동기화 옵션이 포함되어 있습니다. 이 옵션은 앱과 서버를 다시 연결하고 장치와 서버의 시간 설정을 동기화합니다.
- 장치를 취소하거나 인증자를 재설정하면 사용자가 연결할 수 있습니다.
- Adobe Commerce 또는 Magento Open Source 설치에 대한 웹 캐시 및 쿠키를 지우는 것도 도움이 될 수 있습니다. Google과 같은 인증자는 생성된 쿠키를 사용하여 액세스 및 기간을 저장합니다. 특정 브라우저 및 스토어 도메인에 대한 쿠키를 지웁니다.
- 쿠키를 차단하면 [!DNL Google Authenticator]과(와) 같은 일부 인증자가 확인 프로세스를 완료할 수 없습니다. 브라우저에 Adobe Commerce 설치에 대한 쿠키를 허용하는 규칙을 추가합니다.

명령줄에서 인증자를 재설정하고 고급 문제 해결 정보를 보려면 개발자 설명서에서 [2단계 인증](https://developer.adobe.com/commerce/testing/functional-testing-framework/two-factor-authentication/)을 참조하십시오.

**_사용자 계정에 대한 인증자를 재설정하려면:_**

>[!NOTE]
>
>다른 사용자에 대해 2FA 공급자를 재설정하려면 `All` 권한이 있는 _관리자_&#x200B;이거나 [!UICONTROL System] > [!UICONTROL Permissions] > [!UICONTROL Two Factor Auth] 및 [!UICONTROL System] > [!UICONTROL Permissions] > [!UICONTROL All Users]을(를) 선택한 역할에 대해 `Custom` 권한이 있어야 합니다. 자세한 내용은 [사용자 역할](permissions-user-roles.md)을 참조하세요.

1. _관리자_ 사이드바에서 **[!UICONTROL System]** > _[!UICONTROL Permissions]_>**[!UICONTROL All Users]**(으)로 이동합니다.

1. 사용자를 선택하고 편집 모드에서 계정을 엽니다.

1. _[!UICONTROL Current User Identity Verification]_섹션까지 아래로 스크롤하고 암호를 입력합니다.

1. 왼쪽 패널에서 **[!UICONTROL 2FA]**&#x200B;을(를) 클릭합니다.

1. _[!UICONTROL Configuration reset]_섹션에서&#x200B;**[!UICONTROL Reset]**및&#x200B;**[!UICONTROL OK]**을(를) 클릭하여 확인합니다.

   ![사용자 계정 - 2FA 사용](./assets/admin-2fa-config-reset-providers.png){width="600" zoomable="yes"}

   사용자가 필요한 2FA 메서드를 계정에 복원하려면 _로그온_ 페이지에서 각 메서드를 다시 구성해야 합니다.

1. 완료되면 **[!UICONTROL Save User]**&#x200B;을(를) 클릭합니다.
