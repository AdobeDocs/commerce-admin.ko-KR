---
title: Storefront 주문 관리
description: 고객이 Commerce 상점 첫 화면에서 주문 내역을 보고 관리하는 방법을 알아봅니다.
exl-id: 85d953e6-f5a1-4a5e-a6ef-36b9cf6988bb
feature: Orders, Storefront
source-git-commit: c13a4b730ed70ed4829cc20b13c2723137dcbb3a
workflow-type: tm+mt
source-wordcount: '753'
ht-degree: 0%

---

# Storefront 주문 관리

고객은 계정에서 모든 주문에 액세스할 수 있습니다. 주문을 새 주문으로 보고, 필터링하고, 추적하고, 다시 제출할 수 있습니다. 주문 상태에 따라 고객은 주문, 송장, 선적 및 환불 레코드를 인쇄할 수 있습니다.

## 주문 필터링

{{b2b-feature}}

초기 _[!UICONTROL My Orders]_&#x200B;결과에는 상거래 인스턴스 내 모든 웹 사이트에서 보낸 하위 사용자의 일치하는 주문도 포함되어 있습니다. 회사 계정과 연결된 고객은 주문 목록을 필터링하여 결과 내에서 레코드를 빠르게 찾을 수 있습니다. 필터 옵션을 표시하기 위해 고객이&#x200B;**[!UICONTROL Filter]**&#x200B;을(를) 클릭하고&#x200B;**[!UICONTROL Close]**&#x200B;을(를) 클릭하여 필터를 숨깁니다.

![내 주문](./assets/account-dashboard-my-orders-b2b.png){width="700" zoomable="yes"}

| 필터 | 설명 |
| ------ | ----------- |
| [!UICONTROL SKU or Product Name] | SKU 또는 제품 이름을 입력합니다. |
| [!UICONTROL Order Number] | 전체 또는 부분 주문 번호일 수 있습니다. |
| [!UICONTROL Order Status] | 드롭다운에서 상태별로 필터링할 값을 선택합니다. |
| [!UICONTROL Invoice Number] | 전체 또는 부분 송장 번호를 입력합니다. |
| [!UICONTROL Order Date] | 하나 또는 두 날짜 필드를 주문 날짜별로 필터링하도록 설정합니다. |
| [!UICONTROL Created by] | 주문 생성자가 회사 주문을 필터링합니다. |
| [!UICONTROL Order Total] | 최소, 최대 또는 두 값을 모두 설정하여 주문 합계로 필터링합니다. |

## 주문 보기

고객이 목록에서 주문을 찾아 **[!UICONTROL View Order]**&#x200B;을(를) 클릭합니다. 오픈 주문에서 다음 중 하나를 수행할 수 있습니다.

![순서 보기](./assets/customer-account-order-items-ordered.png){width="700" zoomable="yes"}

### 최근에 주문한 제품 보기

주문 후 로그인한 고객의 사이드바와 **[!UICONTROL My Account]** 페이지에 **[!UICONTROL Recent Orders]** 블록이 표시됩니다. 지난번 구매한 제품 5개를 표시합니다.

고객이 제품을 선택하고 **[!UICONTROL Add to Cart]**&#x200B;을(를) 클릭하여 장바구니에 제품을 읽을 수 있습니다. **[!UICONTROL View all]**&#x200B;을(를) 클릭하여 _[!UICONTROL My Account]_&#x200B;페이지 및&#x200B;**[!UICONTROL Recent Orders]**&#x200B;블록으로 리디렉션하는 마지막 순서를 볼 수도 있습니다.

### 인쇄 순서

1. 고객이 **[!UICONTROL Print Order]**&#x200B;을(를) 클릭합니다.

1. 인쇄 대화 상자의 지침에 따라 인쇄를 완료합니다.

### 인보이스 인쇄

1. **[!UICONTROL Invoices]** 탭에서 고객이 다음 중 하나를 클릭합니다.

   - **[!UICONTROL Print All Invoices]**

   - **[!UICONTROL Print Invoice]**

   ![인보이스](./assets/customer-account-order-invoices.png){width="700" zoomable="yes"}

1. [인쇄] 대화 상자를 사용하여 인쇄를 완료합니다.

### 배송 인쇄

1. **[!UICONTROL Order Shipments]** 탭에서 고객이 다음 중 하나를 클릭합니다.

   - **[!UICONTROL Print All Shipments]**

   - **[!UICONTROL Print Shipment]**

   ![모든 배송 인쇄](./assets/customer-account-order-shipments.png){width="700" zoomable="yes"}

1. [인쇄] 대화 상자를 사용하여 인쇄를 완료합니다.

### 배송 추적

1. **[!UICONTROL Order Shipments]** 탭에서 **[!UICONTROL Track this Shipment]**&#x200B;을(를) 클릭합니다.

   사용할 수 있는 모든 추적 정보는 팝업 창에 나타납니다.

1. 준비가 되면 고객이 **[!UICONTROL Close Window]**&#x200B;을(를) 클릭합니다.

### 환불 인쇄

1. **환불** 탭에서 고객이 다음 중 하나를 클릭합니다.

   - **모든 환불 인쇄**

   - **환불 인쇄**

   ![환불](./assets/customer-account-order-refunds.png){width="700" zoomable="yes"}

1. [인쇄] 대화 상자를 사용하여 인쇄를 완료합니다.

[_순서 변경 허용_](reorders-allow.md) 구성 옵션이 활성화된 경우 고객이 순서 변경을 사용할 수 있습니다.

고객은 다음 두 페이지에서 특정 주문에 대한 순서 조정 기능을 시작할 수 있습니다.

- 내 주문 페이지
- 주문 보기 페이지

## 재주문

_[!UICONTROL Reorder]_&#x200B;링크는&#x200B;_[!UICONTROL View]_ 링크 근처에 있는 주문과 함께 목록에 표시됩니다.

![내 주문 페이지에서 링크 순서 바꾸기](./assets/account-dashboard-reorder.png){width="700" zoomable="yes"}

**사례 1.** 주문의 모든 제품을 재정렬할 수 있습니다.

고객이 장바구니로 리디렉션되고 모든 제품이 장바구니에 추가됩니다.

**사례 2.** 주문의 일부/모든 제품을 재정렬할 수 없습니다.

>[!NOTE]
>
>`Not Visible Individually` 제품의 순서를 변경할 수 있습니다.

_[!UICONTROL Reorder]_&#x200B;링크가&#x200B;_[!UICONTROL My Orders]_ 및 _[!UICONTROL View Order]_&#x200B;페이지에 표시되지 않습니다.

![내 주문 페이지](./assets/account-dashboard-reorder-grid.png){width="700" zoomable="yes"}

>[!TIP]
>
>장바구니가 비어 있지 않고 고객이 [!UICONTROL My Orders] 또는 [!UICONTROL Order View] 페이지에서 **[!UICONTROL Reorder]**&#x200B;을(를) 클릭하는 경우 기존 제품이 추가된 순서 변경 제품과 함께 장바구니에 남아 있습니다.

## 주문 취소

[_취소 허용_](cancel-allow.md) 구성 옵션이 활성화된 경우 고객이 취소를 사용할 수 있습니다.

고객은 다음 세 페이지에서 특정 주문에 대한 취소 기능을 시작할 수 있습니다.

- 내 주문 페이지
- 주문 보기 페이지
- 내 계정 페이지

_[!UICONTROL Cancel Order]_&#x200B;링크가&#x200B;_[!UICONTROL Reorder]_ 링크 근처에 표시됩니다. 주문을 취소할 수 없는 경우 링크가 표시되지 않습니다.

![내 주문 페이지에서 링크 취소](./assets/account-dashboard-cancel.png){width="700" zoomable="yes"}

취소를 수행하려면 고객이 다음을 수행합니다.

1. **[!UICONTROL Cancel Order]** 클릭 수

1. 취소 이유 제공

   ![주문 이유 취소](./assets/cancel-order-reasons.png){width="700" zoomable="yes"}

   [_취소 허용_](cancel-allow.md) 페이지에서 취소 이유를 사용자 지정할 수 있습니다.

1. **[!UICONTROL Confirm]** 클릭 수

   ![내 주문 페이지에서 취소](./assets/cancel-order.png){width="700" zoomable="yes"}

   취소 후 _[!UICONTROL Pending]_&#x200B;상태의 주문이&#x200B;_[!UICONTROL Canceled]_ 상태로 변경되고, _[!UICONTROL Processing]_&#x200B;상태의 주문이&#x200B;_[!UICONTROL Closed]_ 상태로 변경되고, 환불이 처리됩니다.

   취소가 완료되면 고객에게 이메일이 전송됩니다.

   ![주문 전자 메일 취소](./assets/cancel-order-email.png){width="700" zoomable="yes"}

   고객의 주문 내역에 취소 정보가 추가됩니다. 주문 메모 및 설명 기록 탭에 나타납니다.

   ![주문 메모 취소](./assets/cancel-order-notes.png){width="700" zoomable="yes"}

   ![댓글 기록 취소](./assets/cancel-order-comments.png){width="700" zoomable="yes"}

   어떤 이유로 주문이 취소할 수 없는 상태로 변경되고 고객이 페이지를 새로 고치지 않은 경우 주문을 취소할 수 있는 링크가 여전히 나타납니다. 그러나 취소하려고 하면 오류 메시지가 표시됩니다.

   ![주문 취소 오류 메시지](./assets/cancel-order-error-message.png){width="700" zoomable="yes"}

   페이지를 새로 고치면 주문이 이미 완료된 것을 알 수 있으므로 취소가 작동하지 않았습니다.

   ![새로 고침 후 주문 취소](./assets/cancel-order-after-refresh.png){width="700" zoomable="yes"}
