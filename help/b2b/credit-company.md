---
title: 회사 크레딧 관리
description: 회사 크레딧 라인, 매개 변수 설정 및 계정에서 결제 처리에 대해 알아봅니다.
exl-id: 62ff2a36-053d-4ba0-9969-0f05701afbff
feature: B2B, Companies, Payments
role: Admin
source-git-commit: 7288a4f47940e07c4d083826532308228d271c5e
workflow-type: tm+mt
source-wordcount: '802'
ht-degree: 0%

---

# 회사 크레딧 관리

구성에서 [계정 결제](../getting-started/../b2b/enable-basic-features.md#configure-payment-on-account)를 사용하도록 설정한 경우 회사는 회사에 부여된 크레딧 한도까지 자신의 계정에서 구매할 수 있습니다. 활성화되면 고객은 계정 대시보드에서 회사 크레딧 상태를 확인할 수 있습니다.

![회사 크레딧](./assets/company-create-credit-admin.png){width="700" zoomable="yes"}

각 회사 프로파일에 대해 다음과 같은 신용 관련 매개변수를 설정할 수 있습니다.

- 신용 통화
- 크레딧 제한
- 크레딧 제한 초과 허용
- 변경 사유

회사에 미결 잔액이 있는 경우 관리자로부터 볼 때 판매 주문 상단에 스토어 관리자에 대한 알림이 표시됩니다. 자세한 내용은 [회사 계정 만들기](account-company-create.md)를 참조하세요.

## 회사 신용 활동

회사 프로필의 [!UICONTROL Company Credit] 섹션에는 고객 신용 활동의 요약과 회사 신용 기록 그리드가 표시됩니다.

![회사 크레딧 활동](./assets/company-credit-reimbursements-grid.png){width="700" zoomable="yes"}

| 열 | 설명 |
|--- |--- |
| [!UICONTROL Date] | 트랜잭션 날짜. 날짜 및 시간을 표시하려면 날짜 위로 마우스를 가져갑니다. |
| [!UICONTROL Operation] | 거래와 연계된 활동 유형. 값: <br/>**[!UICONTROL Allocated]**- 회사에 할당된 크레딧.<br/>**[!UICONTROL Updated]** - 다음 필드 중 하나에 변경 내용이 적용되었습니다. [!UICONTROL Credit limit] / [!UICONTROL Credit currency] / [!UICONTROL Allow to exceed credit limit] <br/>**[!UICONTROL Purchased]**- 주문이 완료되었습니다.<br/>**[!UICONTROL Reimbursed]** - 미상환 잔액이 환급되었습니다. <br/>**[!UICONTROL Refunded]**- 대변 메모 금액이 환불되었습니다.<br/>**[!UICONTROL Reverted]** - 주문이 취소되었으며 금액이 크레딧 잔액으로 반환되었습니다. |
| [!UICONTROL Amount] | 다음 거래 유형과 연결된 거래 금액: `Purchased` / `Reimbursed` / `Refunded` / `Reverted` <br/>구매 금액의 경우 금액은 저장소의 표시 통화와 신용 통화 설정의 형식으로 표시되며 현재 전환율(해당되는 경우)이 표시됩니다. 예: <br/>EUR 20,000.00($22,400.00) <br/>USD/EUR 0.8928 |
| [!UICONTROL Outstanding Balance] | 상환된 금액에서 계정입금 방법을 사용하여 수행한 모든 주문의 총 납기를 뺀 금액입니다. 양은 양수 또는 음수 값으로 나타날 수 있습니다. <br/>**[!UICONTROL Positive value]**- 선금이 양수 값으로 표시됩니다.<br/>**[!UICONTROL Negative value]** - 기한이 음수 값으로 표시됩니다. |
| [!UICONTROL Available Credit] | _[!UICONTROL Credit Limit]_&#x200B;및_[!UICONTROL Outstanding Balance]_&#x200B;의 합계입니다. 기업이 신용 한도를 초과한 경우 금액은 음의 값으로 나타난다. |
| [!UICONTROL Credit Limit] | 회사에 대한 크레딧 금액. |
| [!UICONTROL Updated By] | 작업을 시작한 사람의 이름입니다. |
| [!UICONTROL Custom Reference Number] | 트랜잭션과 연결된 사용자 지정 참조 번호입니다. |
| [!UICONTROL Comment] | 작업 유형에 따라 `Reason for Change` 필드의 값을 컴파일했습니다. <br/>**[!UICONTROL Purchased]**- 구매의 댓글, 주문 번호 및 주문 링크를 포함합니다.<br/>**[!UICONTROL Reimbursed]** - 환급 트랜잭션의 설명을 포함합니다. |
| [!UICONTROL Action] | `Reimbursed` 작업에만 해당됩니다. **[!UICONTROL Edit]** - 환급 금액을 업데이트할 수 있습니다. |

{style="table-layout:auto"}

## 신용 정보 업데이트

고객이 상인에게 미결 신용에 대한 지급을 이행하면 매장 관리자는 관리에서 고객 신용 정보를 갱신해야 합니다.

1. _관리자_ 사이드바에서 **고객 > 회사**(으)로 이동합니다.

1. 그리드에서 회사를 찾아 _편집_ 모드로 엽니다.

1. **회사 크레딧** 섹션을 확장합니다.

1. **크레딧 제한**&#x200B;에 대해 새 값을 입력하십시오.

1. 필요에 따라 다른 값을 변경합니다.

1. 업데이트가 완료되면 **[!UICONTROL Save]**&#x200B;을(를) 클릭합니다.

## 결제 수신

상환된 잔액은 회사가 자신의 계좌 잔액에 대해 지급하는 오프라인 결제입니다. 스토어 관리자가 _환급 잔액_ 버튼을 사용하여 회사 프로필에 금액을 수동으로 입력합니다. 금액이 실행되면 미결 잔액과 사용 가능한 회사 신용이 재계산되고 회사 신용 내역에 해당 조치를 기록합니다. 상환된 금액은 구성에 지정된 대로 대변 통화로 입력됩니다.

### 회사 계정에 결제 적용

1. _관리자_ 사이드바에서 **[!UICONTROL Customers]** > **[!UICONTROL Companies]**(으)로 이동합니다.

1. 목록에서 회사 레코드를 찾아 **[!UICONTROL Edit]** 모드로 엽니다.

1. 페이지 맨 위에서 **환급 잔액**&#x200B;을 클릭합니다.

1. 대화 상자에서 결제 정보를 추가합니다.

   ![변제 잔액](./assets/company-reimburse-balance.png){width="500"}

   - **금액**&#x200B;을(를) 입력하십시오.

     금액은 양수 또는 음수 값으로 입력할 수 있습니다.

   - 해당하는 경우 **사용자 지정 참조 번호**&#x200B;를 입력하여 참조하십시오.

     환급당 하나의 사용자 정의 참조 번호만 입력할 수 있습니다. 여러 PO에 지급을 적용하려면 각각에 대해 별도의 상환을 생성하십시오.

   - 필요에 따라 환급에 대해 설명하는 **설명**&#x200B;을 입력하십시오.

1. **변제**&#x200B;를 클릭합니다.

   회사의 미결 잔액 및 사용 가능한 크레딧이 다시 계산되며, 상환을 반영하도록 회사 크레딧 내역이 갱신됩니다.

### 환급 편집

1. 회사 프로필을 **[!UICONTROL Edit]** 모드로 엽니다.

1. **회사 크레딧** 섹션에서 ![확장 선택기](../assets/icon-display-expand.png)를 확장합니다.

1. 그리드에서 환급 트랜잭션을 찾아 **[!UICONTROL Edit]**&#x200B;을(를) 클릭합니다.

1. **사용자 지정 참조 번호** 및 **댓글**&#x200B;에 필요한 변경 작업을 수행합니다.

   상환 금액은 변경할 수 없습니다.

1. **[!UICONTROL Save]**&#x200B;을(를) 클릭합니다.

## Storefront 신용 정보

회사 관리자의 경우 계정 대시보드에 _회사 크레딧_ 섹션이 표시됩니다. 현재 미결 잔액, 사용 가능한 크레딧 및 미결 송장 목록에 따라 회사 계정에 할당된 크레딧 한도를 제공합니다.

판매자가 회사 크레딧에 청구된 주문을 취소하면 주문 금액이 회사 잔고에 반환되고 _크레딧 할당 내역_&#x200B;에 작업 기록이 포함됩니다.

![회사 크레딧](./assets/company-credit.png){width="700" zoomable="yes"}

## 회사 신용 데모

이 데모 비디오를 통해 회사 크레딧 관리에 대해 알아보십시오.

>[!VIDEO](https://video.tv.adobe.com/v/3410762?quality=12&learn=on&captions=kor)
