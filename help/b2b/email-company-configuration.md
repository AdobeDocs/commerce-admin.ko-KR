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

회사에 대한 기본 연락처로 할당된 [영업 담당자](account-company-manage.md)은(는) 회사에 보낸 많은 자동 전자 메일 메시지를 보낸 사람으로 기본적으로 구성됩니다.

1. _관리자_ 사이드바에서 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**(으)로 이동합니다.

1. 왼쪽 패널에서 **[!UICONTROL Customers]**&#x200B;을(를) 확장하고 **[!UICONTROL Company Configuration]**&#x200B;을(를) 선택합니다.

1. 필요한 경우 **[!UICONTROL Store View]**&#x200B;을(를) 저장소 보기로 설정하여 구성의 [범위](../getting-started/websites-stores-views.md#scope-settings)을(를) 정의합니다.

1. **[!UICONTROL Company Registration]** 섹션을 완료합니다.

   >[!NOTE]
   >
   >필드를 편집할 수 있도록 하려면 **[!UICONTROL Use system value]** 확인란의 선택을 취소하십시오.

   - 새 회사 등록 요청을 받으면 알림을 받을 [스토어 연락처](../getting-started/store-details.md#store-email-addresses)로 **[!UICONTROL Company Registration Email Recipient]**&#x200B;을(를) 설정합니다.

   - **[!UICONTROL Send Company Registration Email Copy To]** 필드에 등록 알림 복사본을 받을 각 사용자의 전자 메일 주소를 입력합니다. 여러 이메일 주소는 쉼표로 구분합니다.

   - 알림 복사본을 보내는 방법을 결정하려면 **[!UICONTROL Send Email Copy Method]**&#x200B;을(를) 다음 중 하나로 설정하십시오.

      - `Bcc` - 고객에게 보내는 것과 동일한 전자 메일의 헤더에 받는 사람을 포함하여 _무료 사본_&#x200B;을 보냅니다. BCC 수신자는 고객에게 표시되지 않습니다.
      - `Separate Email` - 복사본을 별도의 전자 메일로 보냅니다.

   - 기본값 대신 사용할 전자 메일 템플릿을 준비한 경우 **[!UICONTROL Default Company Registration Email]**&#x200B;을(를) 템플릿 이름으로 설정합니다. 기본적으로 `Company Registration Request` 템플릿이 사용됩니다.

     ![고객 구성 - 회사 등록](./assets/company-email-options-company-registration.png){width="600" zoomable="yes"}

1. **[!UICONTROL Customer-Related Emails]** 섹션을 완료합니다.

   기본값 대신 사용할 대체 전자 메일 템플릿을 준비한 경우 다음 각 항목에 사용할 템플릿을 선택합니다.

   - **[!UICONTROL Default 'Sales Rep Assigned' Email]**
   - **[!UICONTROL Default 'Assign Company to Customer' Email]**
   - **[!UICONTROL Default 'Assign Company Admin' Email]**
   - **[!UICONTROL Default 'Company Admin Inactive' Email]**
   - **[!UICONTROL Default 'Company Admin Changed to Member' Email]**
   - **[!UICONTROL Default 'Customer Status Active' Email]**
   - **[!UICONTROL Default 'Customer Status Inactive' Email]**

   ![고객 구성 - 고객 관련 이메일](./assets/company-email-options-customer-related-emails.png){width="600" zoomable="yes"}

1. **[!UICONTROL Company Status Change]** 섹션을 완료합니다.

   - 회사 상태가 변경되면 알림을 받을 [스토어 연락처](../getting-started/store-details.md#store-email-addresses)(으)로 **[!UICONTROL Company Status Change for Email Recipient]**&#x200B;을(를) 설정합니다.

   - **[!UICONTROL Send Company Status Change Email Copy To]** 필드에 상태 변경 알림의 복사본을 받을 각 사용자의 전자 메일 주소를 입력합니다. 여러 이메일 주소는 쉼표로 구분합니다.

   - 알림 복사본을 보내는 방법을 결정하려면 **[!UICONTROL Send Email Copy Method]**&#x200B;을(를) 다음 중 하나로 설정하십시오.

      - `Bcc` - 고객에게 보내는 것과 동일한 전자 메일의 헤더에 받는 사람을 포함하여 _무료 사본_&#x200B;을 보냅니다. BCC 수신자는 고객에게 표시되지 않습니다.
      - `Separate Email` - 복사본을 별도의 전자 메일로 보냅니다.

   - 회사 상태가 `Pending Approval`에서 `Active`(으)로 변경될 때 기본값 대신 사용할 전자 메일 템플릿이 준비된 경우 **[!UICONTROL Default 'Company Status Change to Active 1' Email]**&#x200B;을(를) 해당 템플릿으로 설정하십시오. 기본적으로 `Company Status Active 1` 템플릿이 사용됩니다.

   - 회사 상태가 `Rejected` 또는 `Blocked`에서 `Active`(으)로 변경될 때 기본값 대신 사용할 전자 메일 템플릿이 준비된 경우 **[!UICONTROL Default 'Company Status Change to Active 2' Email]**&#x200B;을(를) 해당 템플릿으로 설정하십시오. 기본적으로 `Company Status Active 2` 템플릿이 사용됩니다.

   - 회사 상태가 `Rejected`(으)로 변경될 때 기본값 대신 사용할 전자 메일 템플릿이 준비되어 있는 경우 **[!UICONTROL Default 'Company Status Change to Rejected' Email]**&#x200B;을(를) 해당 템플릿으로 설정하십시오. 기본적으로 `Company Status Rejected` 템플릿이 사용됩니다.

   - 회사 상태가 `Blocked`(으)로 변경될 때 기본값 대신 사용할 전자 메일 템플릿이 준비되어 있는 경우 **[!UICONTROL Default 'Company Status Change to Blocked' Email]**&#x200B;을(를) 해당 템플릿으로 설정하십시오. 기본적으로 `Company Status Blocked` 템플릿이 사용됩니다.

   - 회사 상태가 `Pending Approval`(으)로 변경될 때 기본값 대신 사용할 전자 메일 템플릿이 준비되어 있는 경우 **[!UICONTROL Default 'Company Status Change to Pending Approval' Email]**&#x200B;을(를) 해당 템플릿으로 설정하십시오. 기본적으로 `Company Status Pending Approval` 템플릿이 사용됩니다.

     ![고객 구성 - 회사 상태 변경](./assets/company-email-options-company-status-change.png){width="600" zoomable="yes"}

1. **[!UICONTROL Company Credit Emails]** 섹션을 완료합니다.

   - 회사에 할당된 크레딧 한도가 변경되면 알림을 받을 [스토어 연락처](../getting-started/store-details.md#store-email-addresses)로 **[!UICONTROL Company Credit Change Email Sender]**&#x200B;을(를) 설정합니다. 기본적으로 알림은 _영업 담당자_&#x200B;에게 전송됩니다.

   - **[!UICONTROL Send Company Credit Change Email Copy To]** 필드에 신용 변경 알림의 복사본을 받을 각 사용자의 전자 메일 주소를 입력합니다. 여러 이메일 주소는 쉼표로 구분합니다.

   - 알림 복사본을 보내는 방법을 결정하려면 **[!UICONTROL Send Email Copy Method]**&#x200B;을(를) 다음 중 하나로 설정하십시오.

      - `Bcc` - 고객에게 보내는 것과 동일한 전자 메일의 헤더에 받는 사람을 포함하여 _무료 사본_&#x200B;을 보냅니다. BCC 수신자는 고객에게 표시되지 않습니다.
      - `Separate Email` - 복사본을 별도의 전자 메일로 보냅니다.

   - 기본값 대신 사용할 이메일 템플릿을 준비한 경우 회사 관리자에게 전송되는 다음 각 알림에 대한 템플릿을 선택합니다.

      - **[!UICONTROL Allocated Email Template]**
      - **[!UICONTROL Updated Email Template]**
      - **[!UICONTROL Reimbursed Email Template]**
      - **[!UICONTROL Refunded Email Template]**
      - **[!UICONTROL Reverted Email Template]**

   ![고객 구성 - 회사 크레딧 전자 메일](./assets/company-email-options-company-credit.png){width="600" zoomable="yes"}

1. 완료되면 **[!UICONTROL Save Config]**&#x200B;을(를) 클릭합니다.
