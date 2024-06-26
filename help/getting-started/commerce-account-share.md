---
title: 공유 [!DNL Commerce] account
description: 에 제한된 액세스 권한을 부여하는 방법 알아보기 [!DNL Commerce] 기타 계정 [!DNL Commerce] 계정 보유자입니다.
exl-id: adc4fed4-89f4-4b0c-811c-fcf6f94dbc22
feature: User Account
source-git-commit: ec634ebedd43b8bbc6b4a3e5079035b055740f2d
workflow-type: tm+mt
source-wordcount: '805'
ht-degree: 0%

---

# 공유 [!DNL Commerce] account

사용자 [!DNL Commerce] 계정에는 사이트 관리에 도움이 되는 신뢰할 수 있는 직원과 서비스 공급자가 사용할 수 있는 정보가 포함되어 있습니다. 주 계정 소유자로서 귀하는 다른 사용자에게 제한된 액세스 권한을 부여할 수 있습니다 [!DNL Commerce] 계정 보유자입니다. 공유 액세스는 취소할 수 있지만 한 사용자에서 다른 사용자로 전송할 수 없습니다.

다음 [!DNL Commerce] 지원 팀은 계정에 대한 액세스 권한이 없어 공유 액세스를 설정할 수 없습니다. 적절한 권한이 있는 기본 계정 소유자만 공유 액세스를 설정할 수 있습니다. 계정 액세스를 공유할 때 청구 기록 또는 신용카드 정보와 같은 모든 중요한 정보는 보호되며 다른 사용자에게는 제공되지 않습니다.

>[!NOTE]
>
>공유 액세스 권한이 있는 사용자가 수행한 모든 작업은 기본 계정 소유자의 단독 책임입니다. Adobe은 귀하의 계정에 대한 액세스 권한을 공유한 사용자가 수행한 모든 작업에 대해 책임을 지지 않습니다.

![공유 액세스 설정](./assets/shared-access.png){width="600" zoomable="yes"}

## 공유 계정 설정

1. 시작하기 전에 [!DNL Commerce] 계정 **새 공유 액세스 피부여자**:

   - 사용자는 account.adobe.com에서 계정에 이미 등록하고 account.magento.com을 통해 로그인해야 합니다.
   - 다음 `MAGE ID/Account ID (MAG00XXXXXXX)` 의 왼쪽 위 모서리에 표시됩니다. _[!UICONTROL Magento]_탭, 바로 위&#x200B;**로그아웃**링크를 클릭합니다.
   - 다음 `Email` 계정과 연결된 주소.

1. 에 로그인 [[!DNL Commerce] account](commerce-account-create.md).

1. 왼쪽 탐색 패널에서 을 클릭합니다. **[!UICONTROL Shared Access]**.

1. 클릭 **[!UICONTROL Add New User]**.

   ![새 사용자 추가](./assets/shared-access-add.png){width="600" zoomable="yes"}

1. 아래 [!UICONTROL _New User Information]_, 다음 작업을 수행하십시오.

   - 다음을 입력합니다. **[!UICONTROL Account ID]** 새 사용자의 [!DNL Commerce] 계정입니다.
   - 다음을 입력합니다. **[!UICONTROL Email]** 새 사용자의 주소와 연결된 주소 [!DNL Commerce] 계정입니다.

   ![새 사용자 정보](./assets/shared-new-user.png){width="600"}

1. 아래 _[!UICONTROL Shared Information]_를 사용하여 다음을 수행합니다.

   - 공유 계정을 식별하려면 **[!UICONTROL Share Name]**. 이 이름은 내부 참조용이며 귀하와 귀하의 계정을 공유하는 사람에게만 표시됩니다.

     가장 좋은 방법은 조직 이름을 로 사용하는 것입니다. [!UICONTROL Share Name]. 다음으로 시작하는 이름 사용 안 함 `CLOUD SHARED ACCESS FROM MAG XYX`.
   - 개인 연락처 정보를 새 사용자와 공유하려면 다음을 입력하십시오. **[!UICONTROL Your Email]** 및 **[!UICONTROL Your Phone]**.

1. 아래 _[!UICONTROL Grant Account Permissions]_, 각 의 확인란을 선택합니다. [!DNL Commerce] 공유할 제품 및 서비스입니다.

   ![계정 권한 부여](./assets/shared-permissions.png){width="600"}

1. 클릭 **[!UICONTROL Create Shared Access]**.

   새 사용자 정보가 _[!UICONTROL Manage Permissions]_공유 계정 액세스에 대한 지침이 포함된 전자 메일 초대장이 새 사용자에게 전송됩니다.

   ![공유 액세스에 대한 권한 관리](./assets/shared-manage-permissions.png){width="600" zoomable="yes"}

>[!NOTE]
>
>에 대한 액세스 권한을 공유할 필요는 없습니다. _[!UICONTROL Security Tool]_- MAGE ID를 가진 모든 사용자는 자신의 계정으로 보안 검색 도구를 설정할 수 있습니다. 이 고객은 사이트 변경 및 도메인 소유권 확인 중 하나를 사용하는 데 필요한 권한만 있으면 됩니다 [필수 메서드](https://experienceleague.adobe.com/en/docs/commerce-admin/systems/security/security-scan)).

## 공유 계정 액세스

다음은 공유 계정에 대한 초대를 받는 공유 사용자의 관점에서 작성됩니다.

1. 공유 계정에 대한 초대를 받으면 이메일의 지침에 따라 자신의 계정에 로그인합니다 [!DNL Commerce] 계정입니다.

   계정의 왼쪽 탐색 패널에 새 항목이 있습니다. _[!UICONTROL Shared with me]_탭. 다음_[!UICONTROL Switch Accounts]_ 오른쪽 위 모서리의 컨트롤에는 다음 옵션이 있습니다. `My Account` 공유 계정 이름.

   ![나와 공유됨](./assets/shared-with-me.png){width="600" zoomable="yes"}

1. 공유 계정에 대한 액세스 권한을 얻으려면 다음을 설정하십시오. **[!UICONTROL Switch Accounts]** 공유 계정 이름.

   ![공유 계정으로 전환](./assets/shared-switch.png){width="600" zoomable="yes"}

   공유 계정에 환영 메시지와 연락처 정보가 표시됩니다. 왼쪽 탐색 패널에는 사용할 권한이 있는 항목만 포함됩니다.

1. 공유 계정을 도움말 센터에 연결하려면 **[!UICONTROL Support]** 공유 계정의 왼쪽 탐색 패널에서 을 수행합니다.

   ![지원](./assets/shared-support.png){width="600" zoomable="yes"}

   다음을 사용할 수 있습니다. [Adobe Commerce 도움말 센터](https://experienceleague.adobe.com/en/docs/commerce-knowledge-base/kb/overview.html) 공유 계정에서 문서 및 문제 해결 정보를 검색하고, 알려진 문제에 대한 패치를 찾고, 지원 티켓을 만듭니다.

   >[!NOTE]
   >
   >공유 액세스 권한을 받은 후 사용자는 [[!DNL Commerce] account](https://account.magento.com/customer/account/login), 다음으로 이동 _공유 액세스_&#x200B;을(를) 클릭하고 **[!UICONTROL Support]** 탭. 이 작업은 다음을 확인하기 위해 처음으로 필요합니다. [Adobe Commerce 지원 기술 자료](https://experienceleague.adobe.com/en/docs/commerce-knowledge-base/kb/overview.html) 을(를) 통해 제대로 구성되었습니다. `SSO` 호출합니다.

1. 자신의 계정으로 돌아가려면 **뒤로** 브라우저 컨트롤 및 설정에서 **[!UICONTROL Switch Accounts]** 끝 `My Account`.

## 공유 액세스 취소

1. Commerce 계정에 로그인합니다.

1. 왼쪽 탐색 패널에서 을 클릭합니다. **[!UICONTROL Shared Access]**.

1. 다음에서 해지할 계정 찾기 _[!UICONTROL Managing Users & Permissions]_및 클릭&#x200B;**[!UICONTROL Delete]**.

   >[!NOTE]
   >
   > If  **[!UICONTROL Delete]** 이(가) 표시되지 않으면 **[!UICONTROL Share Name]** 시작 문자 `Cloud Shared Access from MAG XYZ`. 해당 계정이 있는 계정은 삭제할 수 없습니다. [명명 패턴](https://experienceleague.adobe.com/en/docs/commerce-knowledge-base/kb/help-center-guide/magento-help-center-user-guide#remove-cloud-shared-access-users).
   > 
   > 이 경우 계정 소유자에게 공유 액세스 계정을 수정하여 계정 권한을 지우도록 요청하십시오. 해당 업데이트 후에는 사용자가 계정 리소스에 액세스할 수 없습니다.
   >
   > 또한 사용자가 프로젝트에서 제거되어 더 이상 이메일 알림을 받지 않도록 하십시오. [이전 팀원이 Adobe Commerce 클라우드 알림 이메일을 받습니다.](https://experienceleague.adobe.com/en/docs/commerce-knowledge-base/kb/troubleshooting/miscellaneous/former-teammembers-receive-cloud-notification-emails.html)


1. 확인을 묻는 메시지가 나타나면 **[!UICONTROL Delete User]**.

>[!NOTE]
>
>의 공유 이름을 가진 사용자는 삭제할 수 없습니다. _MAG의 클라우드 공유 액세스[XYZ]_ 이 인터페이스에서 다음을 수행합니다. 다음을 참조하십시오 [Cloud 프로젝트를 통해 공유 액세스 권한이 부여된 사용자를 삭제하는 방법](https://experienceleague.adobe.com/en/docs/commerce-knowledge-base/kb/help-center-guide/magento-help-center-user-guide.html?lang=en#remove-cloud-shared-access-users).
