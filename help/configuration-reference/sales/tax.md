---
title: '[!UICONTROL Sales] &gt; [!UICONTROL Tax]'
description: 에서 구성 설정을 검토합니다. [!UICONTROL Sales] &gt; [!UICONTROL Tax] 상거래 관리자의 페이지입니다.
exl-id: eb929a6c-adb2-45ac-b6ec-6239938355bf
feature: Configuration, Taxes
source-git-commit: f95e6d22f83b518c64b254f0d98147e3c6ebaf42
workflow-type: tm+mt
source-wordcount: '1305'
ht-degree: 0%

---

# [!UICONTROL Sales] > [!UICONTROL Tax]

>[!NOTE]
>
>Adobe Commerce 및 Magento Open Source 릴리스 2.4.0 - 2.4.3에는 와 통합하는 데 사용되는 Vertex 공급업체가 개발한 확장이 포함되어 있습니다. [!UICONTROL Vertex Cloud]. 2.4.4 릴리스부터 이 확장은 더 이상 핵심 릴리스와 번들로 제공되지 않으며 Commerce Marketplace에서 설치하고 업데이트해야 합니다. Marketplace에서는 확장 개발자가 제공하는 현재 설명서에 대한 액세스도 제공합니다.
><br><br>
>번들 확장을 활성화하고 구성한 경우 2.4.4 업그레이드 프로세스의 일부로 composer.json 파일을 업데이트하고 앞으로 확장 업데이트를 관리해야 합니다. 다음을 참조하십시오 [모듈 및 확장 업그레이드](https://experienceleague.adobe.com/docs/commerce-operations/upgrade-guide/modules/upgrade.html) 다음에서 _업그레이드 안내서_ 추가 정보.

{{config}}

## [!UICONTROL Tax Classes]

![세금 분류](./assets/tax-tax-classes.png)<!-- zoom -->

이러한 설정 변경에 대한 자세한 내용은 [세금 등급](../../stores-purchase/tax-class.md) 다음에서 _경험 저장 및 구매 안내서_.

| 필드 | [범위](../../getting-started/websites-stores-views.md#scope-settings) | 설명 |
|--- |--- |--- |
| [!UICONTROL Tax Class for Shipping] | 웹 사이트 | 배송에 사용되는 세금 분류를 식별합니다. 옵션에는 사용 가능한 모든 제품 세금 분류가 포함됩니다. `None` / `Taxable Goods` / `Shipping` / `Tax Exempt` |
| [!UICONTROL Tax Class for Gift Options] | 웹 사이트 | ![Adobe Commerce](../../assets/adobe-logo.svg) (Adobe Commerce만 해당) 선물 옵션에 사용되는 기본 세금 분류를 식별합니다. |
| [!UICONTROL Default Tax Class for Product] | 글로벌 | 제품에 사용되는 기본 세금 분류를 식별합니다. |
| [!UICONTROL Default Tax Class for Customer] | 글로벌 | 고객에 사용되는 기본 세금 분류를 식별합니다. |

{style="table-layout:auto"}

## [!UICONTROL Calculation Settings]

![계산 설정](./assets/tax-calculation-settings.png)<!-- zoom -->

| 필드 | [범위](../../getting-started/websites-stores-views.md#scope-settings) | 설명 |
|--- |--- |--- |
| [!UICONTROL Tax Calculation Method Based On] | 웹 사이트 | 주문에 대한 세금을 계산하는 데 사용되는 방법을 결정합니다. 옵션:<br/>**`Unit Price`**- 세금 계산은 각 제품의 단가를 기준으로 합니다.<br/>**`Row Total`** - 세금 계산은 라인 항목 합계를 기반으로 합니다. <br/>**`Total`**- 세금 계산은 주문 합계를 기반으로 합니다.<br/><br/>_**&#x200B;참고:**_다음과 같이 세금 계산 확장이 마켓플레이스에서 설치된 경우 _꼭짓점 클라우드_확장 서비스가 옵션으로 나열됩니다. |
| [!UICONTROL Tax Calculation Based On] | 웹 사이트 | 세금 계산이 배송 주소, 청구 주소 또는 배송 출처를 기준으로 하는지 여부를 결정합니다. 옵션: `Shipping Address` / `Billing Address` / `Shipping Origin` |
| [!UICONTROL Catalog Prices] | 웹 사이트 | 카탈로그 가격에 세금이 포함되는지 또는 제외되는지를 결정합니다. 옵션: `Excluding Tax` / `Including Tax` |
| [!UICONTROL Shipping Prices] | 웹 사이트 | 배송비에 세금을 포함하거나 제외하는 방법을 결정합니다. 옵션: `Excluding Tax` / `Including Tax` |
| [!UICONTROL Apply Customer Tax] | 웹 사이트 | 할인 이전 또는 이후에 세금이 적용되는지 여부를 결정합니다. 옵션: `Before Discount` / `After Discount` |
| [!UICONTROL Apply Discount on Prices] | 웹 사이트 | 할인 가격에 세금이 포함되는지 또는 제외되는지를 결정합니다. 옵션: `Excluding Tax` / `Including Tax` |
| [!UICONTROL Apply Tax On] | 웹 사이트 | 세금이 원래 가격에 적용되는지 또는 가능한 경우 사용자 지정 가격에 적용되는지 여부를 결정합니다. 옵션: `Custom price if available` / `Original price only` |
| [!UICONTROL Enable Cross Border Trade] | 웹 사이트 | 활성화하면 세율이 다른 지역의 경계 간에 일관된 가격을 적용합니다. 옵션: `Yes` / `No` <br/><br/>**_참고:_**국경 간 무역을 사용하면 세율별 이익률이 조정된다. |

{style="table-layout:auto"}

## [!UICONTROL Default Tax Destination Calculation]

![기본 세금 대상 계산](./assets/tax-default-tax-destination-calculation.png)<!-- zoom -->

| 필드 | [범위](../../getting-started/websites-stores-views.md#scope-settings) | 설명 |
|--- |--- |--- |
| [!UICONTROL Default Country] | 스토어 뷰 | 세금 계산의 기준이 되는 국가를 결정합니다. |
| [!UICONTROL Default State] | 스토어 뷰 | 세금 계산의 기준이 되는 상태를 결정합니다. 별표(*)는 선택한 국가 내의 모든 상태를 나타내는 와일드카드로 기능할 수 있습니다. |
| [!UICONTROL Default Post Code] | 스토어 뷰 | 세금 계산의 기준이 되는 우편 번호 또는 우편번호를 식별합니다. 별표(*)는 와일드카드로 작동하여 선택한 상태 내의 모든 우편 번호를 나타낼 수 있습니다. |

{style="table-layout:auto"}

## [!UICONTROL Price Display Settings]

![가격 표시 설정](./assets/tax-price-display-settings.png)<!-- zoom -->

이러한 설정 변경에 대한 자세한 내용은 [가격 표시 설정 구성](../../stores-purchase/display-settings.md#configure-price-display-settings) 다음에서 _경험 저장 및 구매 안내서_.

| 필드 | [범위](../../getting-started/websites-stores-views.md#scope-settings) | 설명 |
|--- |--- |--- |
| [!UICONTROL Display Product Prices in Catalog] | 스토어 뷰 | 카탈로그에 게시된 제품 가격에 세금이 포함되는지 또는 제외되는지 여부를 결정하거나 두 가지 버전의 가격을 표시합니다(하나는 세금이 포함됨). 옵션: `Excluding Tax` / `Including Tax` / `Including and Excluding Tax` <br/><br/>**_참고:_**제품 가격 표시 필드를 다음으로 설정한 경우 `Including Tax`즉, 세금 출처와 일치하는 세금 규칙이 있거나 세금 규칙과 일치하는 고객 주소가 있는 경우에만 세금이 표시됩니다. 일치를 트리거할 수 있는 이벤트에는 고객 계정 생성, 로그인 또는 장바구니에서 세금 및 배송 예상 도구의 사용이 포함됩니다. |
| [!UICONTROL Display Shipping Prices] | 스토어 뷰 | 배송비에 세금이 포함되는지 또는 제외되는지 또는 배송비의 두 가지 버전을 표시할지 여부를 결정합니다. 하나는 세금이 있고 다른 하나는 세금이 없습니다. 옵션: `Excluding Tax` / `Including Tax` / `Including and Excluding Tax` |

{style="table-layout:auto"}

## [!UICONTROL Shopping Cart Display Settings]

![장바구니 표시 설정](./assets/tax-shopping-cart-display-settings.png)<!-- zoom -->

이러한 설정 변경에 대한 자세한 내용은 [장바구니 표시 설정 구성](../../stores-purchase/display-settings.md#step-2-configure-shopping-cart-display-settings) 다음에서 _경험 저장 및 구매 안내서_.

| 필드 | [범위](../../getting-started/websites-stores-views.md#scope-settings) | 설명 |
|--- |--- |--- |
| [!UICONTROL Display Prices] | 스토어 뷰 | 장바구니 가격에 세금이 포함되는지 또는 제외되는지, 또는 두 가지 버전의 가격을 표시할지 여부를 결정합니다. 하나는 세금이 있고 다른 하나는 세금이 없습니다. 옵션: `Excluding Tax` / `Including Tax` / `Including and Excluding Tax` |
| [!UICONTROL Display Subtotal|Store View] | 장바구니 소계에 세금이 포함되는지 또는 제외되는지, 또는 소계의 두 가지 버전(하나가 세금과 함께 표시됨)을 표시하는지, 아니면 세금이 없이 표시하는지 결정합니다. 옵션: `Excluding Tax` / `Including Tax` / `Including and Excluding Tax` |
| [!UICONTROL Display Shipping Amount] | 스토어 뷰 | 장바구니 배송 금액에 세금이 포함되는지 또는 제외되는지, 아니면 두 가지 버전의 배송 금액을 표시할지 여부를 결정합니다. 하나는 세금이 있고 다른 하나는 세금이 없습니다. 옵션: `Excluding Tax` / `Including Tax` / `Including and Excluding Tax` |
| [!UICONTROL Additionally Show Order Total Without Tax] | 스토어 뷰 | 세금 없이 총 금액이 포함된 추가 줄이 장바구니에 표시되는지 여부를 결정합니다. 옵션: `Yes` / `No` |
| [!UICONTROL Display Full Tax Summary] | 스토어 뷰 | 장바구니에 전체 세금 요약이 포함되어 있는지 여부를 결정합니다. 옵션: `Yes` / `No` |
| [!UICONTROL Display Zero Tax Subtotal] | 스토어 뷰 | 세금이 0일 때 장바구니에 세금 소계가 포함되는지 여부를 결정합니다. 옵션: `Yes` / `No` |

{style="table-layout:auto"}

## [!UICONTROL Orders, Invoices, Credit Memos Display Settings]

![주문, 송장, 대변 메모 표시 설정](./assets/tax-orders-invoices-credit-memos-display-settings.png)<!-- zoom -->

이러한 설정 변경에 대한 자세한 내용은 [주문, 송장 및 대변 메모 표시 설정 구성](../../stores-purchase/display-settings.md#step-3-configure-order-invoice-and-credit-memo-display-settings) 다음에서 _경험 저장 및 구매 안내서_.

| 필드 | [범위](../../getting-started/websites-stores-views.md#scope-settings) | 설명 |
|--- |--- |--- |
| [!UICONTROL Display Prices] | 스토어 뷰 | 판매 문서의 가격에 세금이 포함되어 있는지 또는 각 문서에 두 가지 버전의 가격이 표시되는지 여부를 결정합니다. 하나는 세금이 있고 다른 하나는 세금이 없습니다. 옵션: `Excluding Tax` / `Including Tax` / `Including and Excluding Tax` |
| [!UICONTROL Display Subtotal] | 스토어 뷰 | 판매 문서의 소계에 세금이 포함되는지 또는 제외되는지 여부를 결정하거나 각 문서에 두 버전의 소계가 표시되는지 여부를 결정합니다. 하나는 세금이 있고 다른 하나는 세금이 없습니다. 옵션: `Excluding Tax` / `Including Tax` / `Including and Excluding Tax` |
| [!UICONTROL Display Shipping Amount] | 스토어 뷰 | 판매 문서의 배송 금액에 세금이 포함되는지 아니면 제외되는지, 또는 각 문서에 두 가지 버전의 소계가 표시되는지 여부를 결정합니다. 하나는 세금이 있고 다른 하나는 세금이 없습니다. 옵션: `Excluding Tax` / `Including Tax` / `Including and Excluding Tax` |
| [!UICONTROL Additionally Show Order Total Without Tax] | 스토어 뷰 | 세금 없이 총 금액이 포함된 추가 줄이 판매 문서에 표시되는지 여부를 결정합니다. 옵션: `Yes` / `No` |
| [!UICONTROL Display Full Tax Summary] | 스토어 뷰 | 전체 세금 요약이 판매 문서에 표시되는지 여부를 결정합니다. 옵션: `Yes` / `No` |
| [!UICONTROL Display Zero Tax Subtotal] | 스토어 뷰 | 세금이 부과되지 않을 때 판매 문서의 소계 섹션이 표시되는지 결정합니다. 옵션: `Yes` / `No` |
| [!UICONTROL Display Gift Wrapping Prices] | 스토어 뷰 | ![Adobe Commerce](../../assets/adobe-logo.svg) (Adobe Commerce만 해당) 소계에 선물 포장 가격이 포함되어 있는지 여부를 결정합니다. 옵션: `Excluding Tax` / `Including Tax` / `Including and Excluding Tax` |
| [!UICONTROL Display Printed Card Prices] | 스토어 뷰 | ![Adobe Commerce](../../assets/adobe-logo.svg) (Adobe Commerce만 해당) 인쇄된 카드 가격이 소계에 포함되는지 여부를 결정합니다. 옵션: `Excluding Tax` / `Including Tax` / `Including and Excluding Tax` |

{style="table-layout:auto"}

## [!UICONTROL Fixed Product Taxes]

![고정 제품세](./assets/tax-fixed-product-taxes.png)<!-- zoom -->

이러한 설정 변경에 대한 자세한 내용은 [고정 제품 세금(FPT)](../../stores-purchase/fixed-product-tax.md) 다음에서 _경험 저장 및 구매 안내서_.

| 필드 | [범위](../../getting-started/websites-stores-views.md#scope-settings) | 설명 |
|--- |--- |--- |
| [!UICONTROL Enable FPT] | 웹 사이트 | FPT를 사용할 수 있는지 여부를 결정합니다. 옵션: `Yes` / `No` |
| [!UICONTROL Display Prices in Product Lists] | 웹 사이트 | 제품 목록에서 FPT의 표시를 제어합니다. 옵션:<br/> **`Including FPT Only`** - 표시된 가격에는 고정 제품 세금이 포함됩니다. FPT 금액은 별도로 표시되지 않습니다.<br/>**`Including FPT and FPT description`**- 표시된 가격에는 고정 제품 세금이 포함됩니다. FPT 금액이 별도로 표시됩니다.<br/>**`Excluding FPT. Including FPT description and final price`** - 표시된 가격에는 고정 제품 세금이 포함되지 않습니다. FPT 금액이 별도로 표시됩니다.<br/>**`Excluding FPT`**- 표시된 가격에는 고정 제품 세금이 포함되지 않습니다. FPT 금액은 별도로 표시되지 않습니다. |
| [!UICONTROL Display Prices On Product View Page] | 웹 사이트 | 제품 페이지에서 FPT의 표시를 제어합니다. 옵션:<br/> **`Including FPT Only`** - 표시된 가격에는 고정 제품 세금이 포함됩니다. FPT 금액은 별도로 표시되지 않습니다.<br/>**`Including FPT and FPT description`**- 표시된 가격에는 고정 제품 세금이 포함됩니다. FPT 금액이 별도로 표시됩니다.<br/>**`Excluding FPT. Including FPT description and final price`** - 표시된 가격에는 고정 제품 세금이 포함되지 않습니다. FPT 금액이 별도로 표시됩니다.<br/>**`Excluding FPT`**- 표시된 가격에는 고정 제품 세금이 포함되지 않습니다. FPT 금액은 별도로 표시되지 않습니다. |
| [!UICONTROL Display Prices in Sales Modules] | 웹 사이트 | 장바구니 및 체크아웃 중에 FPT의 표시를 제어합니다. 옵션:<br/> **`Including FPT Only`** - 표시된 가격에는 고정 제품 세금이 포함됩니다. FPT 금액은 별도로 표시되지 않습니다.<br/>**`Including FPT and FPT description`**- 표시된 가격에는 고정 제품 세금이 포함됩니다. FPT 금액이 별도로 표시됩니다.<br/>**`Excluding FPT. Including FPT description and final price`** - 표시된 가격에는 고정 제품 세금이 포함되지 않습니다. FPT 금액이 별도로 표시됩니다.<br/>**`Excluding FPT`**- 표시된 가격에는 고정 제품 세금이 포함되지 않습니다. FPT 금액은 별도로 표시되지 않습니다. |
| [!UICONTROL Display Prices in Emails] | 웹 사이트 | 이메일에 FPT가 표시되도록 제어합니다. 옵션:<br/> **`Including FPT Only`** - 표시된 가격에는 고정 제품 세금이 포함됩니다. FPT 금액은 별도로 표시되지 않습니다.<br/>**`Including FPT and FPT description`**- 표시된 가격에는 고정 제품 세금이 포함됩니다. FPT 금액이 별도로 표시됩니다.<br/>** FPT 제외 FPT 설명 및 최종 가격 포함&#x200B;**- 표시된 가격에는 고정 제품 세금이 포함되지 않습니다. FPT 금액이 별도로 표시됩니다.<br/>**`Excluding FPT`** - 표시된 가격에는 고정 제품 세금이 포함되지 않습니다. FPT 금액은 별도로 표시되지 않습니다. |
| [!UICONTROL Apply Tax to FPT] | 웹 사이트 | FPT 금액에 세금이 적용되는지 여부를 결정합니다. 옵션: `Yes` / `No` |
| [!UICONTROL Include FPT in Subtotal] | 웹 사이트 | FPT가 장바구니 소계에 포함되는지 여부를 결정합니다. 옵션: <br/>**`Yes`**- 장바구니 소계에 FPT를 포함합니다.<br/>**`No`** - FPT는 소계에 포함되지 않으며 장바구니에서 소계 뒤에 배치됩니다. |

{style="table-layout:auto"}
