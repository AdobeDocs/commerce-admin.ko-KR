---
title: "[!UICONTROL My Purchase Orders]"
description: 구매 주문과 이를 사용하여 기업이 구매를 관리하는 방법에 대해 알아봅니다.
exl-id: b7348bc8-b874-4642-a372-530883d9d94c
feature: B2B, Companies, Purchase Orders
source-git-commit: c94d4e8d13c32c1c1b1d37440fdb953c8527b76c
workflow-type: tm+mt
source-wordcount: '475'
ht-degree: 0%

---

# [!UICONTROL My Purchase Orders]

회사에 대해 구매 주문이 [사용](purchase-order-flow.md)되면 회사 사용자 계정에 로그인한 고객에 대한 모든 주문은 자동으로 구매 주문(PO)으로 만들어집니다. 필요한 권한이 있는 회사 사용자는 하위 사용자가 만든 PO와 함께 만든 PO를 만들고 편집하고 삭제할 수 있습니다.

![내 구매 주문](./assets/account-dashboard-my-purchase-orders.png){width="700" zoomable="yes"}

>[!NOTE]
>
>구매 주문은 주문이 생성된 시점의 품목 가격, 할인 및 배송료의 _스냅숏_&#x200B;을 만듭니다. PO가 생성된 후 품목 가격이 변경되면 최초 가격이 사용됩니다.

## 구매 주문 관리

_구매 주문 보기_ 페이지에서 고객은 [역할 권한](account-company-roles-permissions.md)에 따라 PO를 관리할 수 있습니다.

- PO를 보려면 **[!UICONTROL View]**&#x200B;을(를) 클릭하십시오.
- PO에 대한 댓글을 보려면 **[!UICONTROL Comments]** 탭을 클릭하십시오.
- 전체 주문 내역을 보려면 **[!UICONTROL History Log]** 탭을 클릭하십시오.

>[!IMPORTANT]
>
>구매 발주의 품목이 품절되거나 가용 수량이 부족한 경우, 구매 발주가 실제 주문으로 변환될 때 오류가 발생합니다. 미납주문이 사용으로 설정된 경우 주문이 정상적으로 처리됩니다.

## 기존 구매 발주의 새 구매 발주

고객이 기존 구매 발주를 가지고 있고 신규 품목을 추가하려는 경우 신규 PO에 신규 제품이 추가된 중복 구매 발주를 생성할 수 있습니다. 고객은 다음 단계를 완료합니다.

1. _내 구매 주문_ 페이지에서 고객이 구매 주문을 찾아 **[!UICONTROL View]** 링크를 클릭합니다.

1. 고객이 **[!UICONTROL Add Items to Shopping Cart]**&#x200B;을(를) 클릭합니다.

   모든 항목이 나열된 장바구니 페이지가 열립니다.

1. 추가 또는 변경을 수행합니다.

1. (선택 사항) **[!UICONTROL Custom Reference Number]**&#x200B;을(를) 사용하여 내부 송장/PO 번호를 주문에 추가합니다.

1. 일반 체크 아웃 워크플로를 따르고 **[!UICONTROL Place Purchase Order]**&#x200B;을(를) 클릭합니다.

_[!UICONTROL Add Items to Shopping Cart]_을(를) 클릭할 때 장바구니에 항목이 있으면 대화 상자가 표시됩니다. 이 대화 상자를 통해 장바구니 항목을 새 항목과 병합하거나 장바구니의 항목을 PO의 항목으로 바꿀 수 있습니다.

더 이상 필요하지 않은 경우 원래 구매 발주를 마감할 수 있습니다.

## 구매 주문 승인

회사 구조 또는 할당된 회사 역할에 따라 승인자로 지정된 고객의 경우 _[!UICONTROL My Purchase Orders]_대시보드 페이지에&#x200B;**[!UICONTROL Requires My Approval]**탭이 표시됩니다. 고객은 이 탭을 클릭하여 승인을 기다리는 PO를 검토합니다. 카운터는 승인 대기 중인 주문 수를 보여 줍니다.

구매 주문의 **[!UICONTROL View]**&#x200B;을(를) 클릭하고 세부 정보를 검토한 후 승인자는 **[!UICONTROL Approve]** 또는 **[!UICONTROL Reject]**&#x200B;을(를) 클릭할 수 있습니다.

### 일괄 승인/거부

Adobe Commerce 2.4.1부터 승인자는 한 번에 여러 구매 발주를 승인하거나 거부할 수 있습니다.

1. _[!UICONTROL My Purchase Order]_페이지에서&#x200B;**[!UICONTROL Requires My Approval]**탭을 클릭합니다.

1. 승인 또는 거부할 각 구매 발주에 대한 확인란을 선택합니다.

1. **[!UICONTROL Approve Selected]** 또는 **[!UICONTROL Reject Selected]**&#x200B;을(를) 클릭합니다.

고객은 조치를 허용하는 상태의 구매 발주만 선택할 수 있습니다. 회사 관리자는 회사의 모든 활성 구매 발주에 대해 일괄 승인 또는 거부를 수행할 수 있습니다.
