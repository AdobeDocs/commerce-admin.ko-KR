---
title: 회사 이메일 구성
description: 회사 계정에 대한 커뮤니케이션을 보내는 데 사용되는 이메일 옵션 및 템플릿에 대해 알아봅니다.
exl-id: fd61c0c6-0887-4ff2-8002-906ff615bad9
feature: B2B, Companies, Configuration
role: Admin
source-git-commit: 03d1892799ca5021aad5c19fc9f2bb4f5da87c76
workflow-type: tm+mt
source-wordcount: '676'
ht-degree: 0%

---

# 회사 이메일 옵션 구성

다음 [영업 담당자](account-company-manage.md) 회사에 대한 기본 연락처로 할당된 은 회사에 전송된 많은 자동화된 이메일 메시지를 보낸 사람으로 기본적으로 구성됩니다.

1. 다음에서 _관리자_ 사이드바, 이동 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. 왼쪽 패널에서 를 확장합니다. **[!UICONTROL Customers]** 및 선택 **[!UICONTROL Company Configuration]**.

1. 필요한 경우 다음을 설정합니다. **[!UICONTROL Store View]** 을(를) 저장소 보기에 추가하여 [범위](../getting-started/websites-stores-views.md#scope-settings) 을 참조하십시오.

1. 다음을 완료합니다. **[!UICONTROL Company Registration]** 섹션:

   >[!NOTE]
   >
   >지우기 **[!UICONTROL Use system value]** 필드를 편집할 수 있도록 하는 확인란입니다.

   - 설정 **[!UICONTROL Company Registration Email Recipient]** (으)로 [저장소 연락처](../getting-started/store-details.md#store-email-addresses) 새 회사 등록 요청이 접수되면 알림을 받을 사람.

   - 다음에서 **[!UICONTROL Send Company Registration Email Copy To]** 필드에 등록 통지 사본을 받을 각 개인의 이메일 주소를 입력합니다. 여러 이메일 주소는 쉼표로 구분합니다.

   - 알림 사본이 전송되는 방법을 결정하려면 을(를) 설정합니다 **[!UICONTROL Send Email Copy Method]** 다음 중 하나를 수행합니다.

      - `Bcc` - 을(를) 보냅니다. _무차별적 복사_ 고객에게 전송된 동일한 이메일의 헤더에 수신자를 포함하여. BCC 수신자는 고객에게 표시되지 않습니다.
      - `Separate Email` - 사본을 별도의 이메일로 전송합니다.

   - 기본값 대신 사용할 이메일 템플릿을 준비한 경우 을(를) 설정합니다 **[!UICONTROL Default Company Registration Email]** 를 사용하여 템플릿 이름을 변경할 수 있습니다. 기본적으로 `Company Registration Request` 템플릿이 사용됩니다.

     ![고객 구성 - 회사 등록](./assets/company-email-options-company-registration.png){width="600" zoomable="yes"}

1. 다음을 완료합니다. **[!UICONTROL Customer-Related Emails]** 섹션:

   기본값 대신 사용할 대체 전자 메일 템플릿을 준비한 경우 다음 각 항목에 사용할 템플릿을 선택합니다.

   - **[!UICONTROL Default 'Sales Rep Assigned' Email]**
   - **[!UICONTROL Default 'Assign Company to Customer' Email]**
   - **[!UICONTROL Default 'Assign Company Admin' Email]**
   - **[!UICONTROL Default 'Company Admin Inactive' Email]**
   - **[!UICONTROL Default 'Company Admin Changed to Member' Email]**
   - **[!UICONTROL Default 'Customer Status Active' Email]**
   - **[!UICONTROL Default 'Customer Status Inactive' Email]**

   ![고객 구성 - 고객 관련 이메일](./assets/company-email-options-customer-related-emails.png){width="600" zoomable="yes"}

1. 다음을 완료합니다. **[!UICONTROL Company Status Change]** 섹션:

   - 설정 **[!UICONTROL Company Status Change for Email Recipient]** (으)로 [저장소 연락처](../getting-started/store-details.md#store-email-addresses) 회사 상태가 변경될 때 알림을 받을 사람입니다.

   - 다음에서 **[!UICONTROL Send Company Status Change Email Copy To]** 필드에 상태 변경 통지의 사본을 받을 각 개인의 이메일 주소를 입력합니다. 여러 이메일 주소는 쉼표로 구분합니다.

   - 알림 사본이 전송되는 방법을 결정하려면 을(를) 설정합니다 **[!UICONTROL Send Email Copy Method]** 다음 중 하나를 수행합니다.

      - `Bcc` - 을(를) 보냅니다. _무차별적 복사_ 고객에게 전송된 동일한 이메일의 헤더에 수신자를 포함하여. BCC 수신자는 고객에게 표시되지 않습니다.
      - `Separate Email` - 사본을 별도의 이메일로 전송합니다.

   - 회사 상태가에서 변경될 때 기본값 대신 사용할 이메일 템플릿이 준비된 경우 `Pending Approval` 끝 `Active`, 설정됨 **[!UICONTROL Default 'Company Status Change to Active 1' Email]** 템플릿에 추가합니다. 기본적으로 `Company Status Active 1` 템플릿이 사용됩니다.

   - 회사 상태가에서 변경될 때 기본값 대신 사용할 이메일 템플릿이 준비된 경우 `Rejected` 또는 `Blocked` 끝 `Active`, 설정됨 **[!UICONTROL Default 'Company Status Change to Active 2' Email]** 템플릿에 추가합니다. 기본적으로 `Company Status Active 2` 템플릿이 사용됩니다.

   - 회사 상태가 (으)로 변경될 때 기본값 대신 사용할 이메일 템플릿을 준비했습니다. `Rejected`, 설정됨 **[!UICONTROL Default 'Company Status Change to Rejected' Email]** 템플릿에 추가합니다. 기본적으로 `Company Status Rejected` 템플릿이 사용됩니다.

   - 회사 상태가 (으)로 변경될 때 기본값 대신 사용할 이메일 템플릿을 준비했습니다. `Blocked`, 설정됨 **[!UICONTROL Default 'Company Status Change to Blocked' Email]** 템플릿에 추가합니다. 기본적으로 `Company Status Blocked` 템플릿이 사용됩니다.

   - 회사 상태가 (으)로 변경될 때 기본값 대신 사용할 이메일 템플릿을 준비했습니다. `Pending Approval`, 설정됨 **[!UICONTROL Default 'Company Status Change to Pending Approval' Email]** 템플릿에 추가합니다. 기본적으로 `Company Status Pending Approval` 템플릿이 사용됩니다.

     ![고객 구성 - 회사 상태 변경](./assets/company-email-options-company-status-change.png){width="600" zoomable="yes"}

1. 다음을 완료합니다. **[!UICONTROL Company Credit Emails]** 섹션:

   - 설정 **[!UICONTROL Company Credit Change Email Sender]** (으)로 [저장소 연락처](../getting-started/store-details.md#store-email-addresses) 회사에 할당된 크레딧 한도가 변경되면 알림을 받을 사용자. 기본적으로 알림이 (으)로 전송됩니다. _영업 담당자_.

   - 다음에서 **[!UICONTROL Send Company Credit Change Email Copy To]** 필드에 신용 변경 통지의 사본을 받을 각 개인의 이메일 주소를 입력합니다. 여러 이메일 주소는 쉼표로 구분합니다.

   - 알림 사본이 전송되는 방법을 결정하려면 을(를) 설정합니다 **[!UICONTROL Send Email Copy Method]** 다음 중 하나를 수행합니다.

      - `Bcc` - 을(를) 보냅니다. _무차별적 복사_ 고객에게 전송된 동일한 이메일의 헤더에 수신자를 포함하여. BCC 수신자는 고객에게 표시되지 않습니다.
      - `Separate Email` - 사본을 별도의 이메일로 전송합니다.

   - 기본값 대신 사용할 이메일 템플릿을 준비한 경우 회사 관리자에게 전송되는 다음 각 알림에 대한 템플릿을 선택합니다.

      - **[!UICONTROL Allocated Email Template]**
      - **[!UICONTROL Updated Email Template]**
      - **[!UICONTROL Reimbursed Email Template]**
      - **[!UICONTROL Refunded Email Template]**
      - **[!UICONTROL Reverted Email Template]**

   ![고객 구성 - 회사 크레딧 이메일](./assets/company-email-options-company-credit.png){width="600" zoomable="yes"}

1. 완료되면 다음을 클릭하십시오. **[!UICONTROL Save Config]**.
