---
title: '[!UICONTROL Sales] &gt; [!UICONTROL Sales]'
description: Commerce 관리자의 [!UICONTROL Sales] &gt; [!UICONTROL Sales] 페이지에서 구성 설정을 검토하십시오.
exl-id: 29091aab-e608-4e68-a6fe-f2808c78581c
feature: Configuration, Orders
source-git-commit: 8d73a3a635c20e636c4b8bde41a4f807d3fd9f2e
workflow-type: tm+mt
source-wordcount: '1226'
ht-degree: 1%

---

# [!UICONTROL Sales] > [!UICONTROL Sales]

{{config}}

## [!UICONTROL General]

![일반](./assets/sales-general.png)<!-- zoom -->

<!-- [General](https://experienceleague.adobe.com/en/docs/commerce-admin/stores-sales/site-store/sales-documents) -->

| 필드 | [범위](../../getting-started/websites-stores-views.md#scope-settings) | 설명 |
|--- |--- |--- |
| [!UICONTROL Hide Customer IP] | 스토어 뷰 | 주문, 송장, 선적 및 대변 메모에 고객 IP 주소를 표시할지 여부를 결정합니다. 옵션: `Yes` / `No` |

{style="table-layout:auto"}

## [!UICONTROL Checkout Totals Sort Order]

![체크아웃 합계 정렬 순서](./assets/sales-checkout-totals-sort-order.png)<!-- zoom -->

<!-- [Checkout Totals Sort Order](https://experienceleague.adobe.com/en/docs/commerce-admin/stores-sales/point-of-purchase/checkout/checkout-totals-sort-order) -->

| 필드 | [범위](../../getting-started/websites-stores-views.md#scope-settings) | 설명 |
|--- |--- |--- |
| [!UICONTROL Subtotal] | 웹 사이트 | 다른 체크아웃 합계와 관련하여 소계를 계산하는 시기를 결정하는 숫자입니다. 기본값: `10` |
| [!UICONTROL Discount] | 웹 사이트 | 다른 체크아웃 합계와 관련하여 할인이 계산되는 시기를 결정하는 숫자입니다. 기본값: `20` |
| [!UICONTROL Shipping] | 웹 사이트 | 기타 체크아웃 합계와 관련하여 배송이 계산되는 시기를 결정하는 숫자입니다. 기본값: `30` |
| [!UICONTROL Tax] | 웹 사이트 | 기타 체크아웃 합계와 관련하여 세금이 계산되는 시기를 결정하는 숫자입니다. 기본값: `40` |
| [!UICONTROL Fixed Product Tax] | 웹 사이트 | 기타 체크아웃 합계와 관련하여 고정 제품 세금이 계산되는 시기를 결정하는 숫자입니다. 기본값: `50` |
| [!UICONTROL Grand Total] | 웹 사이트 | 기타 체크아웃 합계와 관련하여 총계를 계산하는 시기를 결정하는 숫자입니다. 기본값: `100` |

{style="table-layout:auto"}

## [!UICONTROL Reorder]

![순서 바꾸기](./assets/sales-reorder.png)<!-- zoom -->

<!-- [Reorder](https://experienceleague.adobe.com/en/docs/commerce-admin/stores-sales/shopper-tools/reorders-allow) -->

| 필드 | [범위](../../getting-started/websites-stores-views.md#scope-settings) | 설명 |
|--- |--- |--- |
| [!UICONTROL Allow Reorder] | 스토어 뷰 | 고객이 계정에서 순서를 변경할 수 있는지 여부를 결정합니다. 옵션: `Yes` / `No` |

{style="table-layout:auto"}

## [!UICONTROL Allow Zero Grand Total]

| 필드 | [범위](../../getting-started/websites-stores-views.md#scope-settings) | 설명 |
|--- |--- |--- |
| [!UICONTROL Allow Zero Grand Total for Credit Memo] | 스토어 뷰 | 총계가 0인 대변 메모를 생성할 가능성을 결정합니다. 옵션: `Yes` / `No` |

{style="table-layout:auto"}

## [!UICONTROL Invoice and Packing Slip Design]

![인보이스 및 포장 명세서 디자인](./assets/sales-invoice-packing-slip-design.png)<!-- zoom -->

<!-- [Invoice and Packing Slip Design](https://experienceleague.adobe.com/en/docs/commerce-admin/stores-sales/site-store/sales-documents) -->

| 필드 | [범위](../../getting-started/websites-stores-views.md#scope-settings) | 설명 |
|--- |--- |--- |
| [!UICONTROL Logo for PDF Print-outs] | 스토어 뷰 | PDF 송장 및 포장 명세서 헤더에 나타나는 로고 파일을 식별합니다. 허용되는 파일 형식: <br/>JPG/JPEG <br/>TIF/TIFF <br/>PNG |
| [!UICONTROL Logo for HTML Print View] | 스토어 뷰 | 송장 및 포장 명세서 HTML 인쇄 보기의 헤더에 표시되는 로고 파일을 식별합니다. 허용되는 파일 형식: <br/>JPG /JPEG <br/>GIF <br/>PNG |
| [!UICONTROL Address] | 스토어 뷰 | 송장 및 포장 명세서에 표시하려는 상점 주소. |

{style="table-layout:auto"}

## [!UICONTROL Minimum Order Amount]

![최소 주문 금액](./assets/sales-minimum-order-amount.png)<!-- zoom -->

<!-- [Minimum Order Amount](https://experienceleague.adobe.com/en/docs/commerce-admin/stores-sales/point-of-purchase/cart/cart-configuration#minimum-order-amount) -->

| 필드 | [범위](../../getting-started/websites-stores-views.md#scope-settings) | 설명 |
|--- |--- |--- |
| [!UICONTROL Enable] | 웹 사이트 | 사이트에 대해 최소 주문 금액이 설정되었는지 여부를 결정합니다. 옵션: `Yes` / `No` |
| [!UICONTROL Minimum Amount] | 웹 사이트 | 할인이 적용된 후 주문하는 최소 소계를 지정합니다. |
| [!UICONTROL Include Discount Amount] | 웹 사이트 | 최소 주문 금액에 적용된 할인이 포함되는지 여부를 결정합니다. 옵션: `Yes` / `No` |
| [!UICONTROL Include Tax to Amount] | 웹 사이트 | 최소 주문 금액에 세금이 포함되는지 여부를 결정합니다. 옵션: `Yes` / `No` |
| [!UICONTROL Description Message] | 스토어 뷰 | 장바구니 합계가 최소 주문 수량보다 작을 때 장바구니의 맨 위에 표시되는 메시지를 결정합니다. 비워 두면 다음과 같은 기본 메시지가 나타납니다. `Minimum order amount is $[minimum_amount]` |
| [!UICONTROL Error to Show in Shopping Cart] | 스토어 뷰 | 주문 금액이 필요한 최소 주문 금액보다 적을 경우 미니 장바구니 또는 체크아웃 링크에서 표시되는 메시지를 결정합니다. 비워 두면 기본 메시지가 나타납니다. |
| [!UICONTROL Validate Each Address Separately in Multi-address Checkout] | 웹 사이트 | 복수 품목 주문의 경우, 주소를 분리할 주문 품목이 최소 주문 금액을 충족하는지 여부를 결정합니다. 옵션: `Yes` / `No` |
| [!UICONTROL Multi-address Description Message] | 스토어 뷰 | 다중 주소 주문의 경우, 주소로 보낸 항목이 최소 주문 수량보다 적은 경우 장바구니에 표시되는 메시지를 결정합니다. |
| [!UICONTROL Multi-address Error to Show in Shopping Cart] | 스토어 뷰 | 다중 주소 주문의 경우, 주문 금액이 필요한 최소 주문 금액보다 적을 때 미니 장바구니 또는 체크아웃 링크에서 표시되는 메시지를 결정합니다. 비워 두면 기본 메시지가 나타납니다. |

{style="table-layout:auto"}

## [!UICONTROL Dashboard]

![대시보드](./assets/sales-dashboard.png)<!-- zoom -->

<!-- [Dashboard](https://experienceleague.adobe.com/en/docs/commerce-admin/start/admin/tools/admin-dashboard) -->

| 필드 | [범위](../../getting-started/websites-stores-views.md#scope-settings) | 설명 |
|--- |--- |--- |
| [!UICONTROL Use Aggregated Data] | 글로벌 | 실시간으로 집계된 판매 데이터를 사용하여 대시보드 스냅샷 보고서를 생성하는지 여부를 결정합니다. 처리할 데이터가 많은 경우 실시간 데이터 표시를 해제하여 성능을 향상시킬 수 있습니다. 옵션: `Yes` / `No` |

{style="table-layout:auto"}

## [!UICONTROL Orders Cron Settings]

![주문 크론 설정](./assets/sales-orders-cron-settings.png)<!-- zoom -->

<!-- [Orders Cron Settings](https://experienceleague.adobe.com/en/docs/commerce-admin/systems/tools/cron) -->

| 필드 | [범위](../../getting-started/websites-stores-views.md#scope-settings) | 설명 |
|--- |--- |--- |
| [!UICONTROL Pending Payment Order Lifetime] | 웹 사이트 | 보류 중인 주문의 수명(분)을 결정합니다. 기본 설정: `480`분(8시간) |

{style="table-layout:auto"}

## [!UICONTROL Promotions]

[!BADGE SaaS만]{type=Positive url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="Adobe Commerce as a Cloud Service 프로젝트에만 적용됩니다(Adobe 관리 SaaS 인프라)."}

![프로모션 설정](./assets/sales-promotions-settings.png)<!-- zoom -->

| 필드 | [범위](../../getting-started/websites-stores-views.md#scope-settings) | 설명 |
|--- |--- |--- |
| [!UICONTROL Apply Catalog Price Rule on Grouped Price] | 글로벌 | 계층 가격 수량이 [(으)로 설정된 경우 카탈로그 가격 규칙에 대해 &#x200B;](../../catalog/product-price-tier.md)계층 가격 설정`1`을 사용합니다.  옵션: `Yes` / `No` |

## [!UICONTROL Gift Options]

![선물 옵션](./assets/sales-gift-options.png)<!-- zoom -->

<!-- [Gift Options](https://experienceleague.adobe.com/en/docs/commerce-admin/stores-sales/point-of-purchase/cart/cart-configuration#gift-options) -->

| 필드 | [범위](../../getting-started/websites-stores-views.md#scope-settings) | 설명 |
|--- |--- |--- |
| [!UICONTROL Allow Gift Messages on Order Level] | 웹 사이트 | 전체 주문에 대해 선물 메시지를 추가할 수 있는지 여부를 지정합니다. |
| [!UICONTROL Allow Gift Messages on Order Items] | 웹 사이트 | 개별 주문 항목에 대한 선물 메시지를 추가할 수 있는지 여부를 지정합니다. |
| [!UICONTROL Allow Gift Wrapping on Order Level] | 웹 사이트 | ![Adobe Commerce](../../assets/adobe-logo.svg)(Adobe Commerce만 해당) 전체 주문에 대해 선물 포장을 추가할 수 있는지 여부를 지정합니다. |
| [!UICONTROL Allow Gift Wrapping for Order Items] | 웹 사이트 | ![Adobe Commerce](../../assets/adobe-logo.svg)(Adobe Commerce만 해당) 개별 주문 항목에 선물 포장을 추가할 수 있는지 여부를 지정합니다. |
| [!UICONTROL Allow Gift Receipt] | 웹 사이트 | ![Adobe Commerce](../../assets/adobe-logo.svg)(Adobe Commerce만 해당) 주문에 대한 선물 영수증을 추가할 수 있는지 여부를 지정합니다. |
| [!UICONTROL Allow Printed Card] | 웹 사이트 | ![Adobe Commerce](../../assets/adobe-logo.svg)(Adobe Commerce만 해당) 주문에 대해 인쇄된 카드를 추가할 수 있는지 여부를 지정합니다. |
| [!UICONTROL Default Price for Printed Card] | 웹 사이트 | ![Adobe Commerce](../../assets/adobe-logo.svg)(Adobe Commerce만 해당) 인쇄된 카드의 기본 가격을 지정합니다. |

{style="table-layout:auto"}

## [!UICONTROL Minimum Advertised Price]

![최소 광고 가격](./assets/sales-minimum-advertised-price.png)<!-- zoom -->

<!-- [Minimum Advertised Price](https://experienceleague.adobe.com/en/docs/commerce-admin/catalog/products/pricing/product-price-minimum-advertised) -->

| 필드 | [범위](../../getting-started/websites-stores-views.md#scope-settings) | 설명 |
|--- |--- |--- |
| [!UICONTROL Enable MAP] | 웹 사이트 | 스토어에 대한 최소 광고 가격을 활성화합니다. 옵션: `Yes` / `No` |
| [!UICONTROL Display Actual Price] | 웹 사이트 | 제품의 실제 가격이 고객에게 표시되는 위치를 결정합니다. 옵션: <br/>**`In Cart`**- 장바구니에 실제 제품 가격을 표시합니다.<br/>**`Before Order Confirmation`** - 주문 확인 직전 체크아웃 프로세스가 끝날 때 실제 제품 가격을 표시합니다. <br/>**`On Gesture`**- 고객이 &quot;가격 클릭&quot; 또는 &quot;이유가 무엇입니까?&quot;를 클릭하면 실제 제품 가격이 팝업으로 표시됩니다. 링크를 클릭합니다. |
| [!UICONTROL Default Popup Text Message] | 스토어 뷰 | 고객이 범주 목록 또는 제품 보기 페이지에서 &quot;가격 클릭&quot; 링크를 선택할 때 표시되는 텍스트 메시지입니다. |
| [!UICONTROL Default "What's This" Text Message] | 스토어 뷰 | 고객이 &quot;이게 뭐야?&quot;를 클릭할 때 표시되는 텍스트 메시지 제품 보기 페이지의 링크입니다. |
| [!UICONTROL Manufacturer's Suggested Retail Price] | 글로벌 | 제조업체(MSRP)가 제안한 소매 가격. |

{style="table-layout:auto"}

## [!UICONTROL Multicoupon Settings]

{{ee-feature}}

![다중 채널 설정](./assets/sales-multicoupon-settings.png)<!-- zoom -->

| 필드 | [범위](../../getting-started/websites-stores-views.md#scope-settings) | 설명 |
|--- |--- |--- |
| [!UICONTROL Maximum number of coupons per order] | 웹 사이트 | 주문당 허용되는 최대 쿠폰 수를 결정합니다. 이 기능은 관리, GraphQL 및 REST API에서만 사용할 수 있습니다. Storefront에서 **_사용할 수 없음_**&#x200B;입니다. |

{style="table-layout:auto"}

## [!UICONTROL Order by SKU Settings]

{{ee-feature}}

![SKU 설정별 주문](./assets/sales-order-by-sku-settings.png)<!-- zoom -->

<!-- [Order by SKU Settings](https://experienceleague.adobe.com/en/docs/commerce-admin/stores-sales/point-of-purchase/cart/order-by-sku) -->

![고객 그룹에 대한 SKU별 주문 설정](./assets/sales-order-by-sku-settings.png)<!-- zoom -->

| 필드 | [범위](../../getting-started/websites-stores-views.md#scope-settings) | 설명 |
|--- |--- |--- |
| [!UICONTROL Enable Order by SKU on My Account in Storefront] | 웹 사이트 | 고객 계정 대시보드에서 SKU별 주문을 사용할 수 있는지 여부를 결정합니다. 옵션: <br/>**`Yes, for Everyone`**- SKU별 주문 탭이 모든 고객의 계정 대시보드에 표시됩니다.<br/>**`Yes, for Specified Customer Groups`** - SKU별 주문 탭이 지정된 그룹의 구성원 또는 공유 카탈로그의 계정 대시보드에 나타납니다. <br/>**`No`**- 고객 계정에서 SKU별 주문 탭을 사용할 수 없습니다. |
| [!UICONTROL Customer Groups] | 웹 사이트 | 고객 그룹을 결정합니다. 옵션: `General` / `Retailer` / `Wholesale` |

{style="table-layout:auto"}

## [!UICONTROL Instant Purchase]

![즉시 구매](./assets/sales-instant-purchase.png)<!-- zoom -->

<!-- [Instant Purchase](https://experienceleague.adobe.com/en/docs/commerce-admin/stores-sales/point-of-purchase/checkout-instant-purchase) -->

| 필드 | [범위](../../getting-started/websites-stores-views.md#scope-settings) | 설명 |
|--- |--- |--- |
| [!UICONTROL Enabled] | 스토어 뷰 | Braintree과 같은 결제 방법에 자격 증명 모음이 활성화된 경우 스토어 보기에 대해 즉시 구매를 활성화합니다. 옵션: `Yes` / `No` |
| [!UICONTROL Button Text] | 스토어 뷰 | 즉시 구매 단추에 나타나는 텍스트를 지정합니다. 기본 텍스트는 `Instant Purchase`입니다. |

{style="table-layout:auto"}

## [!UICONTROL Rate Limiting]

![속도 제한](assets/sales-rate-limiting.png)<!-- zoom -->

| 필드 | [범위](../../getting-started/websites-stores-views.md#scope-settings) | 설명 |
|--------------------------------------------------------|--- |------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Enable rate limiting for placing orders] | 스토어 뷰 | 스토어 보기에서 주문을 하는 데 속도 제한이 사용되는지 여부를 결정합니다(기본값은 `No`). 옵션: `Yes` / `No`. |
| [!UICONTROL Requests limit per authenticated customer] | 스토어 뷰 | 인증된 고객이 해당 기간 동안 수행할 수 있는 구매 요청 수입니다. 기본 제한은 `10`입니다. |
| [!UICONTROL Requests limit per guest] | 스토어 뷰 | 인증되지 않은 고객이 지정된 기간 동안 수행할 수 있는 구매 요청 수입니다. 기본값은 `50`입니다. |
| [!UICONTROL Counter resets in a ...] | 스토어 뷰 | 인증된/인증되지 않은 고객이 특정 수의 구매 요청을 할 수 있는 기간(기본값: `Minute`). 옵션: `Minute` / `Hour` /`Day` |

{style="table-layout:auto"}

## [!UICONTROL Orders, Invoices, Shipments, Credit Memos Archiving]

{{ee-feature}}

![주문, 송장, 배송, 대변 메모 보관](./assets/sales-orders-invoices-shipments-credit-memos-archiving.png)<!-- zoom -->

이러한 설정 변경에 대한 자세한 내용은 [저장 및 구매 경험 안내서](../../stores-purchase/order-archive.md#configure-the-order-archive)에서 _주문 보관 구성_&#x200B;을 참조하십시오.

| 필드 | [범위](../../getting-started/websites-stores-views.md#scope-settings) | 설명 |
|--- |--- |--- |
| [!UICONTROL Enable Archiving] | 글로벌 | 보관을 사용할지 여부를 결정합니다. 옵션: `Yes` / `No` |
| [!UICONTROL Archive Orders Purchased] | 글로벌 | 완료된 주문이 보관되기까지 경과되는 일 수를 결정합니다. 기본값: `30` |
| [!UICONTROL Order  Statuses to be Archived] | 글로벌 | 보관할 주문의 [상태](../../stores-purchase/order-status.md)를 결정합니다. 기본적으로 완료 또는 마감됨 상태의 주문은 보관됩니다. 옵션: `Pending` / `Processing` / `Suspected Fraud` / `Complete` / `Closed` / `Canceled` / `On Hold` |

{style="table-layout:auto"}

## [!UICONTROL RMA Settings]

{{ee-feature}}

![RMA 설정](./assets/sales-rma-settings.png)<!-- zoom -->

이러한 설정 변경에 대한 자세한 내용은 [저장 및 구매 경험 안내서](../../stores-purchase/rma-configure.md)에서 _반환 구성_&#x200B;을 참조하십시오.

| 필드 | [범위](../../getting-started/websites-stores-views.md#scope-settings) | 설명 |
|--- |--- |--- |
| [!UICONTROL Enable RMA on Storefront] | 웹 사이트 | 고객이 상점 첫 화면에서 RMA 요청을 만들고 볼 수 있는지 여부를 결정합니다. RMA는 신규 및 기존 주문 모두에 적용할 수 있습니다. 기본적으로 RMA는 상점 앞에 대해 활성화되지 않습니다. 옵션: `Yes` / `No` |
| [!UICONTROL Enable RMA on Product Level] | 웹 사이트 | 제품 정보에서 RMA 활성화 필드에 대한 기본값을 결정합니다. |
| [!UICONTROL Use Store Address] | 웹 사이트 | 반송된 상품의 배송에 사용되는 연락처명과 주소를 결정합니다. 옵션: <br/>**`Yes`**- 배송 설정의 [원본 지점](../../stores-purchase/shipping-settings.md#point-of-origin) 주소를 사용합니다.<br/>**`No`** - 다른 주소를 입력할 수 있도록 주소 양식을 엽니다. |

{style="table-layout:auto"}
