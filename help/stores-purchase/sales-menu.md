---
title: '[!UICONTROL Sales] 메뉴'
description: Commerce 관리자에는 [!UICONTROL Sales] 메뉴 - 워크플로우에서 위치에 따라 주문 작업을 위한 도구에 액세스할 수 있습니다.
exl-id: 105106a4-85f7-4143-8411-69ff67ff9331
source-git-commit: 61df9a4bcfaf09491ae2d353478ceb281082fa74
workflow-type: tm+mt
source-wordcount: '435'
ht-degree: 0%

---

# [!UICONTROL Sales] 메뉴

판매 메뉴에는 주문 워크플로우의 위치에 따라 트랜잭션이 나열됩니다. 각 옵션은 주문 수명 동안 다른 단계로 간주할 수 있습니다.

![판매 메뉴](./assets/admin-menu-sales.png){width="450" zoomable="yes"}

## 표시 [!UICONTROL Sales] 메뉴

다음에서 _관리자_ 사이드바, 클릭 **[!UICONTROL Sales]**.

## 메뉴 옵션

### [!UICONTROL Quotes]

![Adobe Commerce](../assets/b2b.svg) (Adobe Commerce B2B와 함께 사용 가능)

승인된 구매자는 [가격 협상](../b2b/quotes.md) 을(를) 전송하여 판매자와 함께 [요청](../b2b/quote-request.md) 장바구니에서.

### [!UICONTROL Orders]

다음의 경우 [주문](orders.md) 가 배치되면 판매 주문이 트랜잭션의 임시 레코드로 생성됩니다. 결제가 처리되지 않았으며, 주문을 취소할 수 있습니다.

### [!UICONTROL Invoices]

An [인보이스](invoices.md) 은 주문에 대한 결제 영수증 레코드입니다. 단일 주문에 대해 여러 송장을 생성할 수 있습니다. 각 주문에는 지정한 구매 제품이 많거나 적습니다. 지급 조치에 따라 송장이 생성될 때 지급이 자동으로 수집될 수 있습니다.

### [!UICONTROL Shipments]

A [배송](shipments.md) 는 배송된 주문에 대한 제품 레코드입니다. 송장과 마찬가지로 주문의 모든 제품이 출하될 때까지 단일 주문과 여러 납품을 연결할 수 있습니다.

### [!UICONTROL Credit Memos]

A [대변 메모](credit-memos.md) 는 전체 또는 부분 환불을 위해 고객이 지불해야 하는 금액을 보여 주는 문서입니다. 해당 금액은 구매에 적용되거나 고객에게 환불될 수 있습니다.

### [!UICONTROL Returns]

![Adobe Commerce](../assets/adobe-logo.svg) (Adobe Commerce 전용)

A [반송된 상품 승인](returns.md) (RMA)는 교환 또는 환불을 위해 품목을 반품하도록 요청하는 고객에게 부여될 수 있습니다. RMA는 단순, 그룹화, 구성 및 번들 제품 유형에 대해 발급할 수 있습니다. 그러나 가상 및 다운로드 가능한 제품이나 기프트 카드에는 RMA를 사용할 수 없습니다.

### [!UICONTROL Billing Agreements]

A [청구 계약](paypal-billing-agreements.md) 은 단일 구매로 제한되지 않는다는 점을 제외하고 구매 발주와 유사합니다. 체크아웃 중에 고객은 결제 방법으로 청구 계약을 선택합니다. 고객이 각 구매에 대한 결제 정보를 입력할 필요가 없기 때문에 청구 계약을 통해 체크아웃 프로세스를 간소화할 수 있습니다.

### [!UICONTROL Transactions]

다음 [트랜잭션](transactions.md) 페이지는 스토어와 모든 결제 시스템 간에 발생한 모든 결제 활동을 나열하고 보다 자세한 정보에 대한 액세스를 제공합니다.

### [!UICONTROL Braintree Virtual Terminal]

가상 터미널 Braintree 페이지에서 관리자는 선택한 금액에 대한 결제를 수락할 수 있습니다. 터미널 기능을 사용할 수 있도록 하려면 판매자가 기본 을 구성해야 합니다 [Braintree 설정](braintree.md). Braintree은 사기 행위 감지 및 PayPal 통합을 통해 완전히 사용자 지정 가능한 체크아웃 경험을 제공합니다.

### [!UICONTROL Archive]

![Adobe Commerce](../assets/adobe-logo.svg) (Adobe Commerce 전용)

(보관 옵션을 활성화해야 함) [주문 보관](order-archive.md) 및 기타 영업 문서는 정기적으로 성능을 향상시키고 작업 공간에 불필요한 정보가 없도록 합니다.
