---
title: ' [!DNL Commerce] 계정 공유'
description: 다른 [!DNL Commerce] 계정 소유자의  [!DNL Commerce] 계정에 제한된 액세스 권한을 부여하는 방법을 알아보세요.
exl-id: adc4fed4-89f4-4b0c-811c-fcf6f94dbc22
feature: User Account
source-git-commit: e7d76a7fa9ba8d8b8ee1ce122f7ca61e2aa317c6
workflow-type: tm+mt
source-wordcount: '836'
ht-degree: 0%

---

# [!DNL Commerce] 계정 공유

[!DNL Commerce] 계정에는 신뢰할 수 있는 직원과 사이트 관리에 도움이 되는 서비스 공급자가 사용할 수 있는 정보가 포함되어 있습니다. 기본 계정 소유자는 다른 [!DNL Commerce] 계정 소유자에게 제한된 액세스 권한을 부여할 수 있습니다. 공유 액세스는 취소할 수 있지만 한 사용자에서 다른 사용자로 전송할 수 없습니다.

[!DNL Commerce] 지원 팀이 계정에 액세스할 수 없으므로 공유 액세스를 설정할 수 없습니다. 적절한 권한이 있는 기본 계정 소유자만 공유 액세스를 설정할 수 있습니다. 계정 액세스를 공유할 때 청구 기록 또는 신용카드 정보와 같은 모든 중요한 정보는 보호되며 다른 사용자에게는 제공되지 않습니다.

>[!NOTE]
>
>공유 액세스 권한이 있는 사용자가 수행한 모든 작업은 기본 계정 소유자의 단독 책임입니다. Adobe은 계정에 대한 액세스 권한을 공유한 사용자가 수행한 모든 작업에 대해 책임을 지지 않습니다.

![공유 액세스 설정](./assets/shared-access.png){width="600" zoomable="yes"}

## 공유 계정 설정

1. 시작하기 전에 **새 공유 액세스 피부여자**&#x200B;의 [!DNL Commerce] 계정에서 다음 정보를 가져옵니다.

   - 사용자는 account.adobe.com에서 계정에 이미 등록하고 account.magento.com을 통해 로그인해야 합니다. 자세한 내용은 [Commerce 계정 만들기](https://experienceleague.adobe.com/en/docs/commerce-admin/start/commerce-account/commerce-account-create#create-a-commerce-account)를 참조하십시오.
   - `MAGE ID/Account ID (MAG00XXXXXXX)`은(는) _[!UICONTROL Magento]_탭의 왼쪽 위,**로그아웃**링크 바로 위에 표시됩니다.
   - 계정과 연결된 `Email` 주소입니다.

1. [[!DNL Commerce] 계정](commerce-account-create.md)에 로그인합니다.

1. 왼쪽 탐색 패널에서 **[!UICONTROL Shared Access]**&#x200B;을(를) 클릭합니다.

1. **[!UICONTROL Add New User]**&#x200B;을(를) 클릭합니다.

   ![새 사용자 추가](./assets/shared-access-add.png){width="600" zoomable="yes"}

1. [!UICONTROL _New User Information]_ 아래에서 다음을 수행합니다.

   - 새 사용자의 [!DNL Commerce] 계정에서 **[!UICONTROL Account ID]**&#x200B;을(를) 입력하십시오.
   - 새 사용자의 [!DNL Commerce] 계정과 연결된 **[!UICONTROL Email]** 주소를 입력하십시오.

   ![새 사용자 정보](./assets/shared-new-user.png){width="600"}

1. _[!UICONTROL Shared Information]_에서 다음을 수행합니다.

   - 공유 계정을 식별하려면 **[!UICONTROL Share Name]**&#x200B;을(를) 입력하십시오. 이 이름은 내부 참조용이며 귀하와 귀하의 계정을 공유하는 사람에게만 표시됩니다.

     가장 좋은 방법은 조직 이름을 [!UICONTROL Share Name]&#x200B;(으)로 사용하는 것입니다. `CLOUD SHARED ACCESS FROM MAG XYX`(으)로 시작하는 이름을 사용하지 마십시오.
   - 새 사용자와 개인 연락처 정보를 공유하려면 **[!UICONTROL Your Email]** 및 **[!UICONTROL Your Phone]**&#x200B;을(를) 입력하십시오.

1. _[!UICONTROL Grant Account Permissions]_에서 공유할 각 [!DNL Commerce] 제품 및 서비스의 확인란을 선택합니다.

   ![계정 권한 부여](./assets/shared-permissions.png){width="600"}

1. **[!UICONTROL Create Shared Access]**&#x200B;을(를) 클릭합니다.

   새 사용자 정보가 공유 액세스 페이지의 _[!UICONTROL Manage Permissions]_섹션에 나타나고 공유 계정에 액세스하는 지침이 포함된 전자 메일 초대장이 새 사용자에게 전송됩니다.

   ![공유 액세스에 대한 권한 관리](./assets/shared-manage-permissions.png){width="600" zoomable="yes"}

>[!NOTE]
>
>_[!UICONTROL Security Tool]_에 대한 액세스 권한을 공유할 필요가 없습니다. MAGE ID를 가진 모든 사용자는 자신의 계정으로 보안 검색 도구를 설정할 수 있습니다. [필요한 메서드](https://experienceleague.adobe.com/en/docs/commerce-admin/systems/security/security-scan) 중 하나를 사용하여 사이트를 변경하고 도메인의 소유권을 확인하는 데 필요한 권한만 있으면 됩니다.

## 공유 계정 액세스

다음은 공유 계정에 대한 초대를 받는 공유 사용자의 관점에서 작성됩니다.

1. 공유 계정에 대한 초대를 받으면 전자 메일의 지침에 따라 자신의 [!DNL Commerce] 계정에 로그인하십시오.

   계정의 왼쪽 탐색 패널에 새 _[!UICONTROL Shared with me]_탭이 있습니다. 오른쪽 상단의_[!UICONTROL Switch Accounts]_ 컨트롤에는 `My Account`에 대한 옵션과 공유 계정 이름이 있습니다.

   ![나와 공유](./assets/shared-with-me.png){width="600" zoomable="yes"}

   >[!NOTE]
   >
   >   _[!UICONTROL Switch Accounts]_컨트롤이 표시되지 않으면 기본 계정 소유자에게 연락하여 올바른 [계정 정보](#set-up-a-shared-account)를 입력했는지 확인하십시오.


1. 공유 계정에 액세스하려면 **[!UICONTROL Switch Accounts]**&#x200B;을(를) 공유 계정의 이름으로 설정하십시오.

   ![공유 계정으로 전환](./assets/shared-switch.png){width="600" zoomable="yes"}

   공유 계정에 환영 메시지와 연락처 정보가 표시됩니다. 왼쪽 탐색 패널에는 사용할 권한이 있는 항목만 포함됩니다.

1. 공유 계정을 도움말 센터에 연결하려면 공유 계정의 왼쪽 탐색 패널에서 **[!UICONTROL Support]**&#x200B;을(를) 클릭합니다.

   ![지원](./assets/shared-support.png){width="600" zoomable="yes"}

   공유 계정의 [Adobe Commerce 도움말 센터](https://experienceleague.adobe.com/en/docs/commerce-knowledge-base/kb/overview)를 사용하여 문서 및 문제 해결 정보를 검색하고 알려진 문제에 대한 패치를 찾고 지원 티켓을 만들 수 있습니다.

   >[!NOTE]
   >
   >공유 액세스 권한을 받은 후 사용자는 [[!DNL Commerce] 계정](https://account.magento.com/customer/account/login)에 로그인하고 _공유 액세스_(으)로 이동한 후 **[!UICONTROL Support]** 탭을 클릭해야 합니다. 이 작업은 `SSO` 호출을 통해 [Adobe Commerce 지원 기술 자료](https://experienceleague.adobe.com/en/docs/commerce-knowledge-base/kb/overview)가 제대로 구성되었는지 확인하기 위해서만 필요합니다.

1. 자신의 계정으로 돌아가려면 브라우저 컨트롤에서 **뒤로**&#x200B;를 클릭하고 **[!UICONTROL Switch Accounts]**&#x200B;을(를) `My Account`(으)로 설정합니다.

## 공유 액세스 취소

1. Commerce 계정에 로그인합니다.

1. 왼쪽 탐색 패널에서 **[!UICONTROL Shared Access]**&#x200B;을(를) 클릭합니다.

1. _[!UICONTROL Managing Users & Permissions]_에서 해지할 계정을 찾은 다음&#x200B;**[!UICONTROL Delete]**을(를) 클릭합니다.

   >[!NOTE]
   >
   > **[!UICONTROL Delete]**&#x200B;이(가) 표시되지 않으면 **[!UICONTROL Share Name]**&#x200B;이(가) `Cloud Shared Access from MAG XYZ`(으)로 시작하는지 확인하십시오. 해당 [이름 지정 패턴](https://experienceleague.adobe.com/en/docs/commerce-knowledge-base/kb/help-center-guide/magento-help-center-user-guide#remove-cloud-shared-access-users)의 계정은 삭제할 수 없습니다.
   > 
   > 이 경우 계정 소유자에게 공유 액세스 계정을 수정하여 계정 권한을 지우도록 요청하십시오. 해당 업데이트 후에는 사용자가 계정 리소스에 액세스할 수 없습니다.
   >
   > 또한 사용자가 프로젝트에서 제거되어 더 이상 이메일 알림을 받지 않도록 하십시오. [이전 팀원이 Adobe Commerce 클라우드 알림 이메일을 받습니다](https://experienceleague.adobe.com/en/docs/commerce-knowledge-base/kb/troubleshooting/miscellaneous/former-teammembers-receive-cloud-notification-emails)


1. 확인 메시지가 표시되면 **[!UICONTROL Delete User]**&#x200B;을(를) 클릭합니다.

>[!NOTE]
>
>이 인터페이스에서 공유 이름이 _MAG에서 클라우드 공유 액세스[XYZ]_&#x200B;인 사용자를 삭제할 수 없습니다. [Cloud 프로젝트를 통해 공유 액세스 권한을 부여받은 사용자를 삭제하는 방법](https://experienceleague.adobe.com/en/docs/commerce-knowledge-base/kb/troubleshooting/miscellaneous/shared-access-troubleshooting)을 참조하세요.
