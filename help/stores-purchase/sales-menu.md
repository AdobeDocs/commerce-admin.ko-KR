---
title: '[!UICONTROL Sales] 메뉴'
description: Commerce 관리자에는 [!UICONTROL Sales] 메뉴가 포함되어 있으며, 이 메뉴를 통해 워크플로우의 위치에 따라 주문 작업을 위한 도구에 액세스할 수 있습니다.
exl-id: 105106a4-85f7-4143-8411-69ff67ff9331
source-git-commit: 621b4729e23952ddd720b4dcc49b5341baae64cc
workflow-type: tm+mt
source-wordcount: '540'
ht-degree: 0%

---

# [!UICONTROL Sales] 메뉴

판매 메뉴에는 주문 워크플로우의 위치에 따라 트랜잭션이 나열됩니다. 각 옵션은 주문 수명 동안 다른 단계로 간주할 수 있습니다.

>[!BEGINTABS]

>[!TAB Adobe Commerce]

[!BADGE PaaS만]{type=Informative url="https://experienceleague.adobe.com/ko/docs/commerce/user-guides/product-solutions" tooltip="Adobe Commerce 온 클라우드 프로젝트(Adobe 관리 PaaS 인프라) 및 온프레미스 프로젝트에만 적용됩니다."}

![판매 메뉴](./assets/admin-menu-sales.png){width="450" zoomable="yes"}

>[!TAB Adobe Commerce as a Cloud Service]

[!BADGE SaaS만]{type=Positive url="https://experienceleague.adobe.com/ko/docs/commerce/user-guides/product-solutions" tooltip="Adobe Commerce as a Cloud Service 및 Adobe Commerce Optimizer 프로젝트에만 적용됩니다(Adobe 관리 SaaS 인프라)."}

![판매 메뉴](./assets/admin-menu-sales-accs.png){width="450" zoomable="yes"}

>[!ENDTABS]

## [!UICONTROL Sales] 메뉴 표시

_관리자_ 사이드바에서 **[!UICONTROL Sales]**&#x200B;을(를) 클릭합니다.

## 메뉴 옵션

### [!UICONTROL Quotes]

![Adobe Commerce B2B](../assets/b2b.svg)(Adobe Commerce B2B에서 사용 가능)

승인된 구매자는 장바구니에서 [요청](../b2b/quote-request.md)을 보내 판매자와 [가격을 협상](../b2b/quotes.md)할 수 있습니다.

### [!UICONTROL Quote Templates]

![Adobe Commerce B2B](../assets/b2b.svg)(Adobe Commerce B2B에서 사용 가능)

구매자와 판매자가 재사용 가능하고 사용자 지정 가능한 [견적 템플릿](../b2b/quote-templates-overview.md)을 만들어 견적 프로세스를 간소화할 수 있습니다.

### [!UICONTROL Orders]

[주문](orders.md)을 넣으면 판매 주문이 임시 트랜잭션 레코드로 만들어집니다. 결제가 처리되지 않았으며, 주문을 취소할 수 있습니다.

### [!UICONTROL Invoices]

[invoice](invoices.md)은(는) 주문에 대한 결제 영수증에 대한 기록입니다. 단일 주문에 대해 여러 송장을 생성할 수 있습니다. 각 주문에는 지정한 구매 제품이 많거나 적습니다. 지급 조치에 따라 송장이 생성될 때 지급이 자동으로 수집될 수 있습니다.

### [!UICONTROL Shipments]

[배송](shipments.md)은(는) 배송된 주문의 제품 레코드입니다. 송장과 마찬가지로 주문의 모든 제품이 출하될 때까지 단일 주문과 여러 납품을 연결할 수 있습니다.

### [!UICONTROL Credit Memos]

[대변 메모](credit-memos.md)은(는) 고객이 전액 또는 일부 환불을 받아야 하는 금액을 표시하는 문서입니다. 해당 금액은 구매에 적용되거나 고객에게 환불될 수 있습니다.

### [!UICONTROL Returns]

![Adobe Commerce](../assets/adobe-logo.svg)(Adobe Commerce 전용)

[반품된 상품 승인](returns.md)(RMA)은 교환 또는 환불을 위해 품목을 반품하도록 요청하는 고객에게 부여될 수 있습니다. RMA는 단순, 그룹화, 구성 및 번들 제품 유형에 대해 발급할 수 있습니다. 그러나 가상 및 다운로드 가능한 제품이나 기프트 카드에는 RMA를 사용할 수 없습니다.

### [!UICONTROL Billing Agreements]

[!BADGE PaaS만]{type=Informative url="https://experienceleague.adobe.com/ko/docs/commerce/user-guides/product-solutions" tooltip="Adobe Commerce 온 클라우드 프로젝트(Adobe 관리 PaaS 인프라) 및 온프레미스 프로젝트에만 적용됩니다."}

[청구 계약](paypal-billing-agreements.md)은(는) 단일 구매로 제한되지 않는다는 점을 제외하면 구매 주문과 유사합니다. 체크아웃 중에 고객은 결제 방법으로 청구 계약을 선택합니다. 고객이 각 구매에 대한 결제 정보를 입력할 필요가 없기 때문에 청구 계약을 통해 체크아웃 프로세스를 간소화할 수 있습니다.

### [!UICONTROL Transactions]

[거래](transactions.md) 페이지에는 스토어와 모든 결제 시스템 간에 발생한 모든 결제 활동이 나열되며 보다 자세한 정보에 대한 액세스를 제공합니다.

### [!UICONTROL Braintree Virtual Terminal]

[!BADGE PaaS만]{type=Informative url="https://experienceleague.adobe.com/ko/docs/commerce/user-guides/product-solutions" tooltip="Adobe Commerce 온 클라우드 프로젝트(Adobe 관리 PaaS 인프라) 및 온프레미스 프로젝트에만 적용됩니다."}

Braintree 가상 터미널 페이지에서 관리자는 선택한 금액에 대한 결제를 수락할 수 있습니다. 터미널 기능을 사용하려면 판매자가 기본 [Braintree 설정](braintree.md)을 구성해야 합니다. Braintree은 사기 행위 감지 및 PayPal 통합을 통해 사용자 지정 가능한 체크아웃 경험을 제공합니다.

### [!UICONTROL Archive]

![Adobe Commerce](../assets/adobe-logo.svg)(Adobe Commerce 전용)

(보관 옵션을 활성화해야 함) [주문 및 기타 판매 문서를 정기적으로 보관하면 성능이 향상되고 작업 영역에 불필요한 정보가 없게 됩니다.](order-archive.md)
