---
title: '[!UICONTROL Sales] &gt; [!UICONTROL Delivery Methods]'
description: Commerce 관리자의 [!UICONTROL Sales] &gt; [!UICONTROL Delivery Methods] 페이지에서 구성 설정을 검토하십시오.
exl-id: 159b76a8-3676-4692-9cd6-18947bda4666
feature: Configuration, Shipping/Delivery
source-git-commit: 06673ccb7eb471d3ddea97218ad525dd2cdcf380
workflow-type: tm+mt
source-wordcount: '3773'
ht-degree: 0%

---

# [!UICONTROL Sales] > [!UICONTROL Delivery Methods]

{{config}}

## [!UICONTROL Basic Delivery Methods]

### [!UICONTROL Flat Rate]

![고정 속도](./assets/delivery-methods-flat-rate.png)<!-- zoom -->

<!-- [Flat Rate](https://docs.magento.com/user-guide/shipping/shipping-flat-rate.html) -->

| 필드 | [범위](../../getting-started/websites-stores-views.md#scope-settings) | 설명 |
|--- |--- |--- |
| [!UICONTROL Enabled] | 웹 사이트 | 활성화되면 정액 요금이 장바구니의 _배송비 및 세금 예상_ 섹션과 체크아웃 중 _배송비_ 섹션에 옵션으로 나타납니다. 옵션: `Yes` / `No` |
| [!UICONTROL Title] | 스토어 뷰 | 체크아웃 중에 이 배송 방법에 사용되는 이름입니다. |
| [!UICONTROL Method Name] | 스토어 뷰 | 출하 견적을 생성하는 데 사용되는 계산 방법을 설명하는 이름. 장바구니에서 계산된 예상 비율 옆에 메서드 이름이 표시됩니다. 기본값은 `Fixed`입니다. |
| [!UICONTROL Type] | 웹 사이트 | 고정 비율을 결정하는 데 사용되는 계산 유형을 설명합니다. 옵션: <br/>**`None`**- 사용된 계산이 없습니다. 정액 비율을 0으로 설정합니다. 이는 무료 배송에 해당합니다.<br/>**`Per Order`** - 전체 주문에 대해 단일 정액 요금을 부과합니다. <br/>**`Per Item`**- 장바구니에 있는 각 항목에 대해 별도의 정액 요금을 부과합니다. 총 수량에 서로 다른 품목의 조합이 포함된 경우에도 요금에 장바구니의 품목 수를 곱합니다. |
| [!UICONTROL Price] | 웹 사이트 | 정액 배송에 대해 고객에게 청구하는 가격. |
| [!UICONTROL Calculate Handling Fee] | 웹 사이트 | 포함된 경우 처리 수수료 계산 방법을 결정합니다. 옵션: `Fixed` / `Percent` |
| [!UICONTROL Handling Fee] | 웹 사이트 | 금액을 계산하기 위해 선택한 방법에 따라 처리 수수료에 대해 부과할 금액을 입력합니다. 예를 들어, 요금이 고정 요금을 기준으로 하는 경우 4.90과 같이 그 금액을 소수점으로 입력합니다. 단, 취급 수수료가 주문의 백분율을 기준으로 하는 경우 백분율로 금액을 입력합니다. 예를 들어 주문의 6%를 부과하려면 값을 `.06`(으)로 입력하십시오. |
| [!UICONTROL Displayed Error Message] | 스토어 뷰 | 고객이 고정 요금을 선택하지만 어떤 이유로든 이 방법을 사용할 수 없는 경우 나타나는 메시지입니다. |
| [!UICONTROL Ship to Applicable Countries] | 웹 사이트 | 정액 운임 선적을 제공하는 국가를 식별합니다. 옵션: <br/>**`All Allowed Countries`**- 스토어 구성에 지정된 모든 국가의 고객은 정액 배송을 사용할 수 있습니다.<br/>**`Specific Countries`** - 특정 국가의 고객만 정액 배송을 사용할 수 있습니다. |
| [!UICONTROL Ship to Specific Countries] | 웹 사이트 | 고객이 정액 배송을 사용할 수 있는 각 국가를 식별합니다. |
| [!UICONTROL Show Method if Not Applicable] | 웹 사이트 | 결제 방법이 구매에 적용되지 않는 경우 결제 중에 정액 요금이 옵션으로 표시되는지 여부를 결정합니다. 옵션: `Yes` / `No` |
| [!UICONTROL Sort Order] | 웹 사이트 | 체크아웃 중에 다른 게재 방법과 함께 나열할 때 정액 요금이 표시되는 순서를 결정하는 숫자입니다. |

{style="table-layout:auto"}

### [!UICONTROL Free Shipping]

![무료 배송](./assets/delivery-methods-free-shipping.png)<!-- zoom -->

<!-- [Free Shipping](https://docs.magento.com/user-guide/shipping/shipping-free.html) -->

| 필드 | [범위](../../getting-started/websites-stores-views.md#scope-settings) | 설명 |
|--- |--- |--- |
| [!UICONTROL Enabled] | 웹 사이트 | 활성화하면 체크아웃 중에 배송 섹션에 무료 배송이 옵션으로 나타납니다. 옵션: `Yes` / `No` |
| [!UICONTROL Title] | 스토어 뷰 | 체크아웃 중에 이 배송 방법에 사용되는 이름입니다. |
| 메서드 이름 | 스토어 뷰 | 출하 견적을 생성하는 데 사용되는 계산 방법을 설명하는 이름. 장바구니에서 계산된 예상 비율 옆에 메서드 이름이 표시됩니다. 기본값은 `Free`입니다. |
| 최소 주문 금액 | 웹 사이트 | 주문에 무료 배송을 적용하는 데 필요한 최소 구매. |
| 금액에 세금 포함 | 웹 사이트 | 세금이 최소 주문 금액 계산에 포함되는지 여부를 결정합니다. 옵션: <br/>**예** - 최소 주문 금액(소계 + 세금 - 할인)을 계산할 때 세금이 포함됩니다.<br/>**아니요** - 최소 주문 금액(소계 - 할인)을 계산할 때 세금이 포함되지 않습니다. |
| 표시된 오류 메시지 | 스토어 뷰 | 고객이 무료 배송을 선택하는 경우 표시되지만 어떤 이유로든 이 방법을 사용할 수 없습니다. |
| 해당 국가로 배송 | 웹 사이트 | 무료 배송을 제공하는 국가를 식별합니다. 옵션: <br/>**허용된 모든 국가** - 스토어 구성에 지정된 모든 국가의 고객은 무료 배송을 사용할 수 있습니다. <br/>**특정 국가** - 특정 국가의 고객만 무료 배송을 사용할 수 있습니다. |
| 특정 국가로 배송 | 웹 사이트 | 고객이 무료 배송을 사용할 수 있는 각 국가를 식별합니다. |
| 해당되지 않는 경우 메서드 표시 | 웹 사이트 | 결제 방법이 구매에 적용되지 않는 경우 무료 배송이 체크아웃 중에 옵션으로 표시되는지 여부를 결정합니다. 옵션: `Yes` / `No` |
| [!UICONTROL Sort Order] | 웹 사이트 | 체크아웃 중에 다른 배송 방법과 함께 나열할 때 무료 배송이 표시되는 주문을 결정하는 숫자입니다. |

{style="table-layout:auto"}

### [!UICONTROL Table Rates]

![테이블 속도](./assets/delivery-methods-table-rates.png)<!-- zoom -->

<!-- [Table Rates](https://docs.magento.com/user-guide/shipping/shipping-table-rate.html) -->

| 필드 | [범위](../../getting-started/websites-stores-views.md#scope-settings) | 설명 |
|--- |--- |--- |
| [!UICONTROL Enabled] | 웹 사이트 | 활성화되면 체크아웃 시 장바구니의 배송 및 세금 예상 섹션과 배송 섹션에 테이블 세율이 옵션으로 나타납니다. 옵션: `Yes` / `No` |
| [!UICONTROL Title] | 스토어 뷰 | 체크아웃 중에 이 배송 방법에 사용되는 이름입니다. |
| 메서드 이름 | 스토어 뷰 | 출하 견적을 생성하는 데 사용되는 계산 방법을 설명하는 이름. 장바구니에서 계산된 예상 비율 옆에 메서드 이름이 표시됩니다. 기본값은 `Table Rate`입니다. |
| [!UICONTROL Condition] | 웹 사이트 | 계산의 기준이 되는 조건을 결정합니다. 업로드되는 CSV 파일의 형식은 각 조건에 따라 다릅니다. 옵션: `Weight vs. Destination` / `Price vs. Destination` / `# of Items vs. Destination` |
| [!UICONTROL Include Virtual Products in Price Calculation] | 웹 사이트 | 배송이 필요하지 않은 가상 제품이 테이블 요금 가격 계산에 포함되는지 여부를 결정합니다. |
| [!UICONTROL Calculate Handling Fee] | 웹 사이트 | 포함된 경우 처리 수수료 계산 방법을 결정합니다. 옵션: `Fixed` / `Percent` |
| [!UICONTROL Handling Fee] | 웹 사이트 | 배송 처리에 드는 비용을 충당하기 위해 배송 요금에 추가되는 요금. 값을 소수점으로 입력합니다. 예를 들어 수수료가 백분율을 기준으로 하는 경우 6%가 아닌 0.06을 입력합니다. 고정 금액을 보려면 `6.00`을(를) 입력하십시오. |
| [!UICONTROL Displayed Error Message] | 스토어 뷰 | 고객이 테이블 환율을 선택하지만 어떤 이유로든 이 방법을 사용할 수 없는 경우 나타나는 메시지. |
| [!UICONTROL Ship to Applicable Countries] | 웹 사이트 | 테이블 요금 배송을 제공하는 국가를 식별합니다. 옵션: <br/>**`All Allowed Countries`**- 스토어 구성에 지정된 모든 국가의 고객은 테이블 요금 배송을 사용할 수 있습니다.<br/>**`Specific Countries`** - 특정 국가의 고객만 테이블 요금 배송을 사용할 수 있습니다. |
| [!UICONTROL Ship to Specific Countries] | 웹 사이트 | 고객이 테이블 요금 배송을 사용할 수 있는 각 국가를 식별합니다. |
| [!UICONTROL Show Method if Not Applicable] | 웹 사이트 | 결제 방법이 구매에 적용되지 않는 경우 체크아웃 중에 테이블 비율 이 옵션으로 표시되는지 여부를 결정합니다. 옵션: `Yes` / `No` |
| [!UICONTROL Sort Order] | 웹 사이트 | 체크아웃 중에 다른 게재 방법과 함께 나열할 때 테이블 환율이 표시되는 순서를 결정하는 숫자입니다. |

{style="table-layout:auto"}

### [!UICONTROL In-Store Delivery]

![매장 내 배달](./assets/delivery-methods-in-store-delivery.png)<!-- zoom -->

<!-- [In-Store Delivery](https://docs.magento.com/user-guide/shipping/shipping-in-store-delivery.html) -->

| 필드 | [범위](../../getting-started/websites-stores-views.md#scope-settings) | 설명 |
|--- |--- |--- |
| [!UICONTROL Enabled] | 웹 사이트 | 활성화되면 체크아웃 중에 장바구니의 _배송비 및 세금 예상_ 섹션과 _배송_ 섹션에 매장 배송이 옵션으로 나타날 수 있습니다. 옵션: `Yes` / `No` |
| [!UICONTROL Method Name] | 스토어 뷰 | 매장 픽업 기능을 배송 방법으로 식별하는 이름입니다. 이 값은 Shipping checkout 페이지 상단의 탭 레이블과 같은 페이지 하단의 사용 가능한 배송 방법 테이블에 표시됩니다. 기본값은 `In-store Delivery`입니다. |
| [!UICONTROL Title] | 스토어 뷰 | 체크아웃 중에 이 배송 방법에 사용되는 이름입니다. |
| [!UICONTROL Price] | 웹 사이트 | 매장 내 픽업에 대해 고객에게 청구하는 가격입니다. |
| [!UICONTROL Search Radius] | 웹 사이트 | 픽업 위치를 검색할 때 사용할 반경(km). |
| [!UICONTROL Displayed Error Message] | 스토어 뷰 | 고객이 매장 내 픽업을 선택하지만 배송 방법을 사용할 수 없을 때 표시되는 메시지입니다. |

{style="table-layout:auto"}

## [!UICONTROL Carriers]

### [!UICONTROL UPS]

{{ups-api}}

![UPS REST 계정 설정](./assets/delivery-methods-ups1.png)<!-- zoom -->

![UPS XML 계정 설정](./assets/delivery-methods-ups1.png)<!-- zoom -->

<!-- [UPS REST Account Settings](https://docs.magento.com/user-guide/shipping/ups.html) -->

| 필드 | [범위](../../getting-started/websites-stores-views.md#scope-settings) | 설명 |
|--- |--- |--- |
| [!UICONTROL Enabled for Checkout] | 웹 사이트 | 체크아웃 중에 배송 방법으로 고객이 UPS를 사용할 수 있는지 여부를 결정합니다. 옵션: `Yes` / `No` |
| [!UICONTROL Enabled for RMA] | 웹 사이트 | 고객이 RMA의 배송 방법으로 UPS를 사용할 수 있는지 여부를 결정합니다. 옵션: `Yes` / `No` |
| _[!UICONTROL UPS Account Settings]_ |  |  |
| [!UICONTROL Live Account] | 스토어 뷰 | United Parcel Service 계정이 라이브임을 지정합니다. 옵션: `Yes` / `No` |
| [!UICONTROL Title] | 스토어 뷰 | 체크아웃 중에 이 배송 방법에 사용되는 이름입니다. |
| _[!UICONTROL UPS REST Account Settings]_ |  |  |
| [!UICONTROL Gateway URL] | 웹 사이트 | UPS REST 서비스의 경우 에는 JSON 데이터를 전송하는 데 필요한 게이트웨이 URL, 추적 URL, 배송 URL의 URL이 표시됩니다 |
| [!UICONTROL Mode] | 웹 사이트 | UPS 시스템으로 전송되는 데이터에 사용되는 전송 모드를 결정합니다. 옵션: <br/>**`Development`**- UPS는 Commerce 서버에서 받은 데이터가 SSL을 통해 전송되는지 확인하지 않습니다.<br/>**`Live`** - UPS는 Commerce 서버에서 받은 데이터가 SSL(Secure Socket Layer)을 통해 전송되는지 확인합니다. |
| 사용자 ID | 웹 사이트 | UPS 발송자 계정 클라이언트 ID. |
| [!UICONTROL Origin of the Shipment] | 웹 사이트 | (UPS REST만 해당) 제품 선적이 시작된 국가 또는 지역. |
| [!UICONTROL Password] | 스토어 뷰 | UPS 발송자 계정 클라이언트 암호. |

{style="table-layout:auto"}

![UPS 패키지 정보](./assets/delivery-methods-ups-packaging-settings.png)<!-- zoom -->

<!-- [UPS Package Information](https://docs.magento.com/user-guide/shipping/ups.html) -->

| 필드 | [범위](../../getting-started/websites-stores-views.md#scope-settings) | 설명 |
|--- |--- |--- |
| _[!UICONTROL UPS Negotiated Rate Settings]_ |  |  |
| [!UICONTROL Enable Negotiated Rates] | 웹 사이트 | (UPS REST만 해당) UPS와의 계약에 따라 특별 요금을 활성화/비활성화합니다. 옵션: `Yes` / `No` |
| [!UICONTROL Packages Request Type] | 웹 사이트 | 여러 패키지가 있는 배송에 대한 중량을 계산하는 방법을 결정합니다. 옵션: `Divide to equal weight (one request)` / `Use origin weight (multiple requests)` |
| [!UICONTROL Shipper Number] | 웹 사이트 | (UPS REST만 해당) 협상된 비율을 사용하려면 6자의 UPS 배송자 번호가 필요합니다. |
| [!UICONTROL Container] | 웹 사이트 | 납품을 포장하는 데 사용되는 컨테이너 유형을 설정합니다. 옵션: `Customer Packaging` / `UPS Letter Envelope` / `Customer Packaging` / `UPS Letter Envelope` / `UPS Tube` / `UPS Express Box` / `UPS Worldwide 25 kilo` / `UPS Worldwide 10 kilo` |
| [!UICONTROL Weight Unit] | 웹 사이트 | 스토어의 제품 중량에 대한 기본 측정 단위를 설정합니다. 자세한 내용은 [차원 가중치](../../stores-purchase/carriers.md#dimensional-weight)를 참조하십시오. |
| [!UICONTROL Tracking URL] | 웹 사이트 | (UPS REST만 해당) 패키지를 추적하는 데 사용되는 UPS URL입니다. |
| [!UICONTROL Destination Type] | 웹 사이트 | 기본 발송 대상 유형을 설정합니다. 옵션: `Business` / `Residential` |
| [!UICONTROL Maximum Package Weight] | 웹 사이트 | UPS에서 지정한 대로 패키지를 지정할 수 있는 최대 가중치를 설정합니다. 주문한 제품이 최대 패키지 중량을 초과하면 이 배송 옵션을 이용할 수 없습니다. [UPS.com](https://www.ups.com/us/en/global.page)에 따르면, 패키지는 70kg(150파운드)을 초과할 수 없습니다. 최대 중량을 확인하려면 운송업체에 문의하십시오. |
| [!UICONTROL Pickup Method] | 웹 사이트 | UPS 픽업 방법을 설정합니다. 옵션: `Regular Daily Pickup` / `On Call Air` / `One Time Pickup` / `Letter Center` / `Customer Counter` |
| [!UICONTROL Minimum Package Weight] | 웹 사이트 | UPS에서 지정한 대로 패키지를 지정할 수 있는 최소 가중치를 설정합니다. 주문한 제품의 무게가 최소 포장 무게보다 작은 경우 이 배송 옵션을 사용할 수 없습니다. 최소 중량을 확인하려면 운송 업체에 문의하십시오. |
| [!UICONTROL Calculate Handling Fee] | 웹 사이트 | 테이블 요금 배송에 대한 처리 수수료 계산 방법을 설정합니다. 옵션: <br>**`Fixed`**- 수수료는 정률입니다.<br>**`Percent`** - 취급 수수료는 주문 금액의 백분율로 적용됩니다. |
| [!UICONTROL Handling Applied] | 웹 사이트 | 각 주문에 처리 비용이 적용되는지 또는 주문 내의 각 패키지에 적용되는지를 지정합니다. |
| [!UICONTROL Handling Fee] | 웹 사이트 | 배송비 가격에 포함된 처리를 설정합니다. 취급 수수료는 고정 금액 또는 백분율로 설정할 수 있습니다. <br/><br/>**_참고:_**백분율을 입력할 경우 25%의 경우 십진수 형식 `0.25`을(를) 사용하십시오. |

{style="table-layout:auto"}

![UPS 허용 메서드](./assets/delivery-methods-ups-allowed-methods.png)<!-- zoom -->

<!-- [UPS Allowed Methods](https://docs.magento.com/user-guide/shipping/ups.html) -->

| 필드 | [범위](../../getting-started/websites-stores-views.md#scope-settings) | 설명 |
|--- |--- |--- |
| _[!UICONTROL UPS allowed methods]_ |  |  |
| [!UICONTROL Allowed Methods] | 웹 사이트 | 고객에게 제공되는 UPS 배송 방법을 지정합니다. 배송 요금은 선택한 배송 방법을 기준으로 계산됩니다. |
| [!UICONTROL Free Method] | 웹 사이트 | UPS를 통해 무료 배송 방법에 사용되는 방법을 식별합니다. 무료 배송을 비활성화하려면 &quot;없음&quot;을 선택하십시오. <br/><br/>**_참고:_**이 메서드는 기본 [무료 배송](../../stores-purchase/shipping-free.md)과 비슷하지만 체크아웃 중에 UPS 배송 옵션으로 나타납니다. |
| [!UICONTROL Free Shipping Amount Threshold] | 웹 사이트 | 주문 금액이 무료 배송 임계값을 충족하면 무료 배송이 적용되는지 여부를 결정합니다. 옵션: `Enable` / `Disable` |
| [!UICONTROL Free Shipping Amount Threshold] | 웹 사이트 | 무료 배송에 대한 자격이 부여되기 위해 주문이 도달해야 하는 최소 총 금액을 설정합니다. |
| [!UICONTROL Displayed Error Message] | 스토어 뷰 | 어떤 이유로든 이 배송 방법을 사용할 수 없을 때 표시되는 오류 메시지. |

{style="table-layout:auto"}

![UPS 적용 국가 및 기타 설정](./assets/delivery-methods-ups-ship-to.png)<!-- zoom -->

<!-- [UPS Applicable Countries and Other Settings](https://docs.magento.com/user-guide/shipping/ups.html) -->

| 필드 | [범위](../../getting-started/websites-stores-views.md#scope-settings) | 설명 |
|--- |--- |--- |
| _[!UICONTROL UPS Applicable countries and other Settings]_ |  |  |
| [!UICONTROL Ship to Applicable Countries] | 웹 사이트 | 고객이 이 배송 방법을 사용할 수 있는 국가를 지정합니다. 옵션: <br/>**`All Allowed Countries`**- 스토어 구성에 지정된 모든 [국가](../../getting-started/store-details.md#country-options)의 고객이 이 배송 방법을 사용할 수 있습니다.<br/>**`Specific Countries`** - 이 옵션을 선택하면 [!UICONTROL Ship to Specific Countries] 목록이 나타납니다. 목록에서 이 배송 방법을 사용할 수 있는 각 국가를 선택하십시오. |
| [!UICONTROL Show Method if Not Applicable] | 웹 사이트 | 체크아웃하는 동안 UPS가 항상 배송 옵션으로 표시되는지 여부를 결정합니다. 옵션: <br/>**`Yes`**- 주문에 적용할 수 없는 경우에도 체크아웃 중에 UPS가 배송 옵션으로 항상 나타납니다.<br/>**`No`** - 주문에 해당하는 경우에만 UPS가 체크아웃 중에 배송 옵션으로 나타납니다. (예를 들어 주문 가중치가 최대 중량을 초과하는 경우) |
| [!UICONTROL Debug] | 웹 사이트 | 디버깅을 위해 스토어와 UPS 간의 데이터 전송이 시스템에 기록되는지 여부를 지정합니다. 추적하여 기록해야 하는 문제가 없는 경우 이 옵션을 `No`(으)로 설정해야 합니다. |
| [!UICONTROL Sort Order] | 웹 사이트 | 체크아웃 중에 다른 게재 방법과 함께 나열할 때 UPS가 표시되는 순서를 결정하는 숫자입니다. 목록의 맨 위에 `0`을(를) 입력하십시오. |

{style="table-layout:auto"}

### [!UICONTROL USPS]

| 필드 | [범위](../../getting-started/websites-stores-views.md#scope-settings) | 설명 |
|--- |--- |--- |
| 체크아웃이 활성화됨 | 웹 사이트 | 체크아웃 중에 고객이 USPS를 배송 방법으로 사용할 수 있는지 여부를 결정합니다. 옵션: `Yes` / `No` |
| _[!UICONTROL USPS Account Settings]_ |  |  |
| [!UICONTROL Gateway URL] | 웹 사이트 | 배송 속도를 동적으로 검색하기 위해 USPS 시스템에 연결하는 데 사용되는 URL입니다. |
| [!UICONTROL Secure Gateway URL] | 웹 사이트 | SSL(Secure Socket Layer)을 통해 USPS 시스템에 연결하여 배송 속도를 동적으로 검색하는 데 사용되는 보안 URL입니다. |
| [!UICONTROL Title] | 스토어 뷰 | 이 배송 옵션의 제목은 장바구니 체크아웃에 표시되는 것과 같습니다. |
| [!UICONTROL User ID] | 웹 사이트 | USPS 발송자 계정 사용자 ID입니다. |
| [!UICONTROL Password] | 웹 사이트 | USPS 발송자 계정 암호입니다. |
| [!UICONTROL Mode] | 웹 사이트 | USPS 시스템으로 전송되는 데이터에 사용되는 전송 모드를 결정합니다. 옵션은 다음과 같습니다. <br/>**`Development`**- USPS가 Commerce 서버에서 받은 데이터가 SSL을 통해 전송되는지 확인하지 않습니다.<br/>**`Live`** - USPS는 Commerce 서버에서 받은 데이터가 SSL(Secure Socket Layer)을 통해 전송되는지 확인합니다. |

{style="table-layout:auto"}

![USPS 패키징 설정](./assets/delivery-methods-usps-packaging.png)<!-- zoom -->

<!-- [USPS Packaging Settings](https://docs.magento.com/user-guide/shipping/usps.html) -->

| 필드 | [범위](../../getting-started/websites-stores-views.md#scope-settings) | 설명 |
|--- |--- |--- |
| _[!UICONTROL USPS packaging Settings]_ |  |  |
| [!UICONTROL Packages Request Type] | 웹 사이트 | 여러 패키지가 있는 배송에 대한 중량을 계산하는 방법을 결정합니다. 옵션: `Divide to equal weight (one request)` / `Use origin weight (multiple requests)` |
| [!UICONTROL Container] | 웹 사이트 | 납품을 포장하는 데 사용되는 컨테이너 유형을 설정합니다. 옵션: `Variable` / `Flat Rate Box` / `Flat Rate Envelope` / `Rectangular` / 사각형이 아님 |
| [!UICONTROL Size] | 웹 사이트 | 크기 옵션을 일반 배송 패키지 크기로 설정합니다. 이 옵션은 배송비 계산에 영향을 줍니다. 옵션: `Regular` / `Large` / `Oversize` |
| [!UICONTROL Machinable] | 웹 사이트 | 패키지를 컴퓨터에서 처리할 수 있는지 여부를 지정합니다. 이 옵션은 배송비 계산에 영향을 줍니다. |
| [!UICONTROL Maximum Package Weight] | 웹 사이트 | USPS에서 지정하는 대로 패키지를 지정할 수 있는 최대 가중치를 설정합니다. 주문한 제품이 최대 패키지 중량을 초과하면 이 배송 옵션을 이용할 수 없습니다. |

{style="table-layout:auto"}

![USPS 처리 비용 설정](./assets/delivery-methods-usps-handling-fee.png)<!-- zoom -->

<!-- [USPS Handling Fee Settings](https://docs.magento.com/user-guide/shipping/usps.html) -->

| 필드 | [범위](../../getting-started/websites-stores-views.md#scope-settings) | 설명 |
|--- |--- |--- |
| _[!UICONTROL USPS Handling Fee settings]_ |  |  |
| [!UICONTROL Calculate Handling Fee] | 웹 사이트 | 테이블 요금 배송에 대한 처리 수수료 계산 방법을 설정합니다. 옵션: <br/>**`Fixed`**- 수수료는 정률입니다.<br/>**`Percent`** - 취급 수수료는 주문 금액의 백분율로 적용됩니다. |
| [!UICONTROL Handling Applied] | 웹 사이트 | 각 주문에 처리 비용이 적용되는지 또는 주문 내의 각 패키지에 적용되는지를 지정합니다. |
| [!UICONTROL Handling Fee] | 웹 사이트 | 배송비 가격에 포함된 처리를 설정합니다. 취급 수수료는 고정 금액 또는 백분율로 설정할 수 있습니다. <br/><br/>**_참고:_**백분율을 입력할 때 25%의 경우 십진수 형식 `0.25`을(를) 사용하십시오. |

{style="table-layout:auto"}

![USPS 허용 메서드](./assets/delivery-methods-usps-allowed-methods.png)<!-- zoom -->

<!-- [USPS Allowed Methods](https://docs.magento.com/user-guide/shipping/usps.html) -->

| 필드 | [범위](../../getting-started/websites-stores-views.md#scope-settings) | 설명 |
|--- |--- |--- |
| _[!UICONTROL USPS Allowed Methods]_ |  |  |
| [!UICONTROL Allowed Methods] | 웹 사이트 | 고객에게 제공되는 허용된 USPS 배송 방법을 지정합니다. 배송 요금은 선택한 배송 방법을 기준으로 계산됩니다. |
| [!UICONTROL Free Method] | 웹 사이트 | USPS를 통해 무료 배송 방법을 설정하거나 `None`을(를) 선택하여 비활성화할 수 있습니다. <br/><br/>**_참고:_**이 배송 방법은 스토어의 무료 배송 방법과 유사하지만 USPS 배송 옵션으로 나열되고 USPS 배송으로 식별됩니다. |
| [!UICONTROL Minimum Order Amount for Free Shipping] | 웹 사이트 | 무료 배송을 위해 충족해야 하는 최소 주문 금액을 설정합니다. |
| [!UICONTROL Displayed Error Message] | 스토어 뷰 | 어떤 이유로든 USPS를 사용할 수 없을 때 표시되는 오류 메시지입니다. |

{style="table-layout:auto"}

![USPS 적용 국가](./assets/delivery-methods-usps-countries.png)<!-- zoom -->

<!-- [USPS Applicable Countries](https://docs.magento.com/user-guide/shipping/usps.html) -->

| 필드 | [범위](../../getting-started/websites-stores-views.md#scope-settings) | 설명 |
|--- |--- |--- |
| _[!UICONTROL USPS Applicable Countries]_ |  |  |
| [!UICONTROL Ship to Applicable Countries] | 웹 사이트 | 주문을 배송할 수 있는 국가를 지정합니다. 옵션: <br/>**`All Allowed Countries`**- 스토어 구성에 지정된 모든 [국가](../../getting-started/store-details.md#country-options)의 고객이 이 배송 방법을 사용할 수 있습니다.<br/>**`Specific Countries`** - 이 옵션을 선택하면 [!UICONTROL Ship to Specific Countries] 목록이 나타납니다. 목록에서 이 배송 방법을 사용할 수 있는 각 국가를 선택하십시오. |
| [!UICONTROL Show Method if Not Applicable] | 웹 사이트 | 체크아웃 중 USPS 배송의 표시를 제어합니다. 옵션: <br/>**`Yes`**- USPS는 주문에 적용할 수 없는 경우에도 체크아웃 중에 배송 옵션으로 항상 표시됩니다.<br/>**`No`** - USPS는 주문에 적용할 수 있는 경우(즉, 주문 무게가 최대 중량을 초과하는 경우) 체크아웃 중에 배송 옵션으로 나타납니다. |
| [!UICONTROL Debug] | 웹 사이트 | 시스템이 디버깅을 위해 스토어와 USPS 간의 데이터 전송 로그를 유지하는지 확인합니다. 추적하여 기록해야 하는 문제가 없는 경우 이 옵션을 `No`(으)로 설정해야 합니다. |
| [!UICONTROL Sort Order] | 웹 사이트 | 체크아웃 중에 다른 게재 방법과 함께 나열할 때 USPS가 표시되는 순서를 결정하는 숫자입니다. 목록의 맨 위에 `0`을(를) 입력하십시오. |

{style="table-layout:auto"}

### [!UICONTROL FedEx]

<!-- [FedEx Account Settings](https://docs.magento.com/user-guide/shipping/fedex.html) -->

#### FedEx 계정 설정

![FedEx 계정 설정](./assets/delivery-methods-fedex-account-settings.png){width="600" zoomable="yes"}

| 필드 | [범위](../../getting-started/websites-stores-views.md#scope-settings) | 설명 |
|-------|------ |-----------------------------------------------------------------------------|
| [!UICONTROL Enabled for Checkout] | 웹 사이트 | 고객이 체크아웃 중에 FedEx를 배송 방법으로 사용할 수 있는지 여부를 결정합니다. 옵션: `Yes` / `No` |
| [!UICONTROL Title] | 스토어 뷰 | 이 배송 옵션의 제목은 장바구니 체크아웃에 표시되는 것과 같습니다. |
| [!UICONTROL Account ID] | 웹 사이트 | FedEx 계정 ID입니다. |
| [!UICONTROL Api Key] | 웹 사이트 | FedEx 계정 API 키. |
| [!UICONTROL Secret Key] | 웹 사이트 | FedEx 계정 API 비밀 키. |
| [!UICONTROL Sandbox Mode] | 웹 사이트 | 테스트 환경에서 FedEx 트랜잭션을 실행하려면 샌드박스 모드를 `Yes`(으)로 설정합니다. 옵션: `Yes` / `No`. |
| [!UICONTROL Web-Services URL] | 웹 사이트 | 필요한 URL은 샌드박스 모드 설정에 따라 다릅니다. 옵션: <br/>**`Production`**- 스토어가 라이브 상태일 때 FedEx 웹 서비스에 액세스하기 위한 URL입니다.<br/>**`Sandbox`** - FedEx 웹 서비스의 테스트 환경에 액세스할 수 있는 URL. |

{style="table-layout:auto"}

#### FedEx 패키징 설정

![FedEx 패키징](./assets/delivery-methods-fedex-packaging.png){width="600" zoomable="yes"}

| 필드 | [범위](../../getting-started/websites-stores-views.md#scope-settings) | 설명 |
|--- |--- |--- |
| [!UICONTROL Pickup Type] | 웹 사이트 | 목록에서 픽업 방법을 선택합니다. <br/>**`DropOff at Fedex Location`**- (기본값) 로컬 FedEx 스테이션에서 발송을 중단함을 나타냅니다.<br/>**`Contact Fedex to Schedule`** - FedEx에 연락하여 픽업을 요청함을 나타냅니다. <br/>**`Use Scheduled Pickup`**- 예약된 정기 픽업의 일부로 배송이 픽업되었음을 나타냅니다.<br/>**`On Call`** - FedEx를 호출하여 픽업이 예약되었음을 나타냅니다. <br/>**`Package Return Program`**- FedEx Ground Package Returns Program에서 선적을 선택함을 나타냅니다.<br/>**`Regular Stop`** - 정기 픽업 일정에 따라 선적이 픽업됨을 나타냅니다. <br/>**`Tag`**- 배송 픽업이 Express 태그 또는 Ground Call 태그 픽업 요청에만 해당됨을 나타냅니다. 이는 반송 레이블에만 적용됩니다. |
| [!UICONTROL Packages Request Type] | 웹 사이트 | 여러 패키지가 있는 배송에 대한 중량을 계산하는 방법을 결정합니다. 옵션: `Divide to equal weight (one request)` / `Use origin weight (multiple requests)` |
| [!UICONTROL Packaging] | 웹 사이트 | 목록에서 스토어에서 주문한 제품을 패키지하는 데 일반적으로 사용하는 컨테이너 유형을 선택합니다. |
| [!UICONTROL Weight Unit] | 웹 사이트 | 패키지 가중치에 사용되는 단위입니다. 옵션: `Pounds`(기본값) / `Kilograms` |
| [!UICONTROL Maximum Package Weight] | 웹 사이트 | FedEx의 기본값은 150파운드입니다. 지원되는 최대 무게에 대해서는 운송 회사에 문의하십시오. FedEx에 특별한 약정이 없는 한 기본값을 사용하는 것이 좋습니다. |

{style="table-layout:auto"}

#### FedEx 취급 수수료 설정

![FedEx 취급 수수료](./assets/delivery-methods-fedex-handling-fee.png){width="600" zoomable="yes"}

| 필드 | [범위](../../getting-started/websites-stores-views.md#scope-settings) | 설명 |
|--- |--- |--- |
| [!UICONTROL Calculate Handling Fee] | 웹 사이트 | 취급 수수료를 계산하는 데 사용되는 방법을 결정합니다. 옵션: `Fixed Fee` / `Percentage` <br/><br/>**_참고:_**처리 요금은 선택 사항이며 FedEx 배송 비용에 추가되는 추가 요금으로 표시됩니다. |
| [!UICONTROL Handling Applied] | 웹 사이트 | 취급 수수료를 적용하는 방법을 결정합니다. 옵션: `Per Order` / `Per Package` |
| [!UICONTROL Handling Fee] | 웹 사이트 | 금액을 계산하는 데 사용되는 방법에 따라 처리 수수료로 청구되는 금액을 지정합니다. 요금이 고정 요금을 기준으로 하는 경우 `4.90`과(와) 같이 금액을 소수로 입력하십시오. 처리 수수료가 주문의 백분율을 기준으로 하는 경우 백분율로 금액을 입력합니다. 예를 들어 주문의 6%를 부과하려면 값을 `.06`(으)로 입력합니다. |

{style="table-layout:auto"}

#### FedEx 게재 방법

![FedEx 배달 메서드](./assets/delivery-methods-fedex-delivery-methods.png){width="600" zoomable="yes"}

| 필드 | [범위](../../getting-started/websites-stores-views.md#scope-settings) | 설명 |
|--- |--- |--- |
| [!UICONTROL Residential Delivery] | 웹 사이트 | B2C(Business-to-Consumer) 또는 B2B(Business-to-Business)를 판매하는지 여부에 따라 다음 중 하나로 설정합니다. <br/>**`Yes`**- B2C 게재용<br/>**`No`** - B2B 게재용 |
| [!UICONTROL Allowed Methods] | 웹 사이트 | 목록에서 지원하는 운송 방법을 선택합니다. 방법은 FedEx 계정, 배송 빈도 및 크기, 해외 배송 허용 여부에 따라 다릅니다. 상인으로서, 당신은 지상 운송만 제공하기로 결정할 수 있습니다. |
| [!UICONTROL Hub ID] | 웹 사이트 | [!DNL Smart Post] 메서드와 함께 사용되는 FedEx에서 제공한 ID입니다. |
| [!UICONTROL Free Method] | 웹 사이트 | 목록에서 무료 배송 오퍼에 사용할 배송 방법을 선택합니다. <br/><br/>**_참고:_**이 배송 방법은 일반 무료 배송 방법과 유사하지만 FedEx 배송 옵션에 나열되어 있으며 FedEx 배송으로 식별됩니다. |
| [!UICONTROL Free Shipping Amount Threshold] | 웹 사이트 | 무료 배송에 최소 주문 금액이 필요한지 여부를 결정합니다. 옵션: <br/>**`Enable`**- 최소 금액을 충족하는 주문에 대해 무료 FedEx 배송을 활성화합니다.<br/>**`Disable`** - 최소 주문으로 무료 FedEx 배송을 사용하지 않도록 설정합니다. |
| [!UICONTROL Free Shipping Amount Threshold] | 웹 사이트 | 무료 배송에 필요한 최소 주문 금액을 지정합니다. |
| [!UICONTROL Displayed Error Message] | 스토어 뷰 | FedEx가 어떤 이유로든 사용할 수 없을 때 나타나는 메시지입니다. 기본 메시지를 사용하거나 다른 메시지를 입력할 수 있습니다. |

{style="table-layout:auto"}

#### FedEx 적용 국가 설정

![FedEx 적용 국가](./assets/delivery-methods-fedex-applicable-countries.png){width="600" zoomable="yes"}

| 필드 | [범위](../../getting-started/websites-stores-views.md#scope-settings) | 설명 |
|--- |--- |--- |
| [!UICONTROL Ship to Applicable Countries] | 웹 사이트 | 고객이 FedEx로 배송할 수 있는 국가를 나타냅니다. 옵션: <br/>**`All Allowed Countries`**- 스토어 구성에 지정된 모든 [국가](../../getting-started/store-details.md#country-options)의 고객이 이 배송 방법을 사용할 수 있습니다.<br/>**`Specific Countries`** - 이 옵션을 선택하면 [!UICONTROL Ship to Specific Countries] 목록이 나타납니다. 목록에서 이 배송 방법을 사용할 수 있는 각 국가를 선택하십시오. |
| [!UICONTROL Ship to Specific Countries] | 웹 사이트 | 고객이 FedEx로 배송할 수 있는 특정 국가를 나타냅니다. |
| [!UICONTROL Debug] | 웹 사이트 | 시스템이 디버깅을 위해 스토어와 FedEx 간의 데이터 전송 로그를 유지하는지 확인합니다. 추적하여 기록해야 하는 문제가 없는 경우 이 옵션을 `No`(으)로 설정해야 합니다. |
| [!UICONTROL Show Method if Not Applicable] | 웹 사이트 | 체크아웃 중 배송 방법으로 FedEx가 표시되는 시점을 결정합니다. 옵션: <br/>**`Yes`**- 주문에 FedEx 배송 옵션이 사용되는지 여부에 관계없이 배달 방법 목록에 표시됩니다.<br/>**`No`** - FedEx 배송 옵션이 주문에 적용할 수 없는 경우(예: 주문 중량이 최대 중량을 초과하는 경우) 배달 방법 목록에 표시되지 않습니다. |
| [!UICONTROL Sort Order] | 웹 사이트 | 체크아웃하는 동안 다른 배달 방법과 함께 나열할 때 FedEx가 표시되는 순서를 결정하는 숫자입니다. 목록의 맨 위에 `0`을(를) 입력하십시오. |

{style="table-layout:auto"}

### [!UICONTROL DHL]

![DHL 계정 설정](./assets/delivery-methods-dhl-account-settings.png)<!-- zoom -->

<!-- [DHL Account Settings](https://docs.magento.com/user-guide/shipping/dhl.html) -->

| 필드 | [범위](../../getting-started/websites-stores-views.md#scope-settings) | 설명 |
|--- |--- |--- |
| _[!UICONTROL DHL Account Settings]_ |  |  |
| [!UICONTROL Enabled for Checkout] | 웹 사이트 | 고객이 체크아웃 중에 DHL을 배송 방법으로 사용할 수 있는지 여부를 결정합니다. 옵션: `Yes` / `No` |
| [!UICONTROL Title] | 스토어 뷰 | 체크아웃 중에 표시되는 이 배송 방법의 제목입니다. |
| [!UICONTROL Gateway URL] | 웹 사이트 | 일반적으로 기본 게이트웨이 URL을 사용할 수 있습니다. 그러나 DHL에서 대체 URL을 제공한 경우 이 필드에 값을 입력합니다. |
| [!UICONTROL Access ID] | 웹 사이트 | DHL 배송자 계정 액세스 ID입니다. |
| [!UICONTROL Password] | 웹 사이트 | DHL 배송자 계정 암호입니다. |
| [!UICONTROL Account Number] | 웹 사이트 | 당신의 DHL 쉬퍼 계정 번호입니다. |

{style="table-layout:auto"}

![DHL 패키지 설정](./assets/delivery-methods-dhl-package-settings.png)<!-- zoom -->

<!-- [DHL Package Settings](https://docs.magento.com/user-guide/shipping/dhl.html) -->

| 필드 | [범위](../../getting-started/websites-stores-views.md#scope-settings) | 설명 |
|--- |--- |--- |
| _[!UICONTROL DHL Package Settings]_ |  |  |
| [!UICONTROL Calculate Handling Fee] | 웹 사이트 | 처리 요금은 선택 사항이며 DHL 배송 비용에 추가되는 추가 비용으로 표시됩니다. 목록에서 처리 수수료를 계산하는 데 사용할 방법을 선택합니다. 옵션: 고정 수수료 / 백분율. |
| [!UICONTROL Handling Applied] | 웹 사이트 | 목록에서 처리 수수료를 적용할 방법을 선택합니다. 옵션: `Per Order` / `Per Package` |
| 취급 수수료 | 웹 사이트 | 금액을 계산하기 위해 선택한 방법에 따라 처리 수수료에 대해 부과할 금액을 입력합니다. 예를 들어, 요금이 고정 요금을 기준으로 하는 경우 `4.90`과(와) 같이 그 금액을 소수점으로 입력하십시오. 단, 취급 수수료가 주문의 백분율을 기준으로 하는 경우 백분율로 금액을 입력합니다. 예를 들어 주문의 6%를 부과하려면 값을 `.06`(으)로 입력하십시오. |
| [!UICONTROL Divide Order Weight] | 스토어 뷰 | 주문 무게가 70kg을 초과하는 경우 정확한 배송비를 보장하기 위해 더 작은 단위로 나눌 수 있는지 여부를 결정합니다. 옵션: `Yes` / `No` |
| [!UICONTROL Weight Unit] | 스토어 뷰 | 운송 계산에 사용되는 가중치의 측정 단위를 결정합니다. 옵션: `Pounds` / `Kilograms` |
| [!UICONTROL Size] | 스토어 뷰 | 패키지의 크기를 결정합니다. 옵션: <br/>**`Regular`**- 배송된 패키지가 DHL 표준 패키징 방법을 준수합니다. [!UICONTROL Allowed Methods] 목록에서 매장에서 제품을 배송하는 데 사용되는 각 포장 방법을 선택합니다.<br/>**`Specific`** - 배송된 패키지에 사용자 지정 차원이 있는 경우 다음을 완료하십시오. [!UICONTROL Height (cm)] / [!UICONTROL Depth (cm)] / [!UICONTROL Width (cm)] |

{style="table-layout:auto"}

![DHL 허용 메서드](./assets/delivery-methods-dhl-allowed-methods.png)<!-- zoom -->

<!-- DHL Allowed Methods](https://docs.magento.com/user-guide/shipping/dhl.html) -->

| 필드 | [범위](../../getting-started/websites-stores-views.md#scope-settings) | 설명 |
|--- |--- |--- |
| _[!UICONTROL DHL allowed methods]_ |  |  |
| [!UICONTROL Allowed Methods] | 웹 사이트 | 목록에서 지원하는 각 운송 방법을 선택합니다. |
| [!UICONTROL Ready Time] | 웹 사이트 | 주문이 제출된 후 패키지를 가져올 수 있는 시간(시간)을 지정합니다. |
| [!UICONTROL Displayed Error Message] | 스토어 뷰 | 이 메시지는 어떤 이유로든 DHL을 사용할 수 없게 되면 나타납니다. 기본 메시지를 사용하거나 직접 메시지를 입력할 수 있습니다. |
| [!UICONTROL Free Method] |  | 이 배송 방법은 일반 무료 배송 방법과 유사하지만, DHL 배송 옵션 내에 기재되어 있으며 DHL 배송으로 식별됩니다. 목록에서 무료 배송 오퍼에 사용할 배송 방법을 선택합니다. |
| [!UICONTROL Free Shipping with Minimum Order Amount] | 웹 사이트 | 다음 중 하나로 설정합니다. <br/>**`Enable`**- 최소 금액을 충족하는 주문에 대해 무료 DHL 배송을 허용합니다.<br/>**`Disable`** - 최소 주문과 함께 무료 DHL 배송을 제공하지 않습니다. |
| [!UICONTROL Minimum Order Amount for Free Shipping] | 웹 사이트 | [!UICONTROL Free Shipping with Minimum Order]을(를) 사용하도록 설정하는 경우 필드에 최소 주문 금액 값을 입력하십시오. |

{style="table-layout:auto"}

![DHL 적용 국가](./assets/delivery-methods-dhl-applicable-countries.png)<!-- zoom -->

<!-- [DHL Applicable Countries](https://docs.magento.com/user-guide/shipping/dhl.html) -->

| 필드 | [범위](../../getting-started/websites-stores-views.md#scope-settings) | 설명 |
|--- |--- |--- |
| _[!UICONTROL DHL applicable countries]_ |  |  |
| [!UICONTROL Ship to Applicable Countries] | 웹 사이트 | 고객이 이 배송 방법을 사용할 수 있는 국가를 지정합니다. 옵션: <br/>**모든 허용된 국가** - 모든 허용된 국가가 무료 배송 방법을 사용할 수 있습니다. [!UICONTROL General] 구성 페이지에 허용된 국가가 지정되었습니다. <br/>**특정 국가** - 이 배송 옵션을 특정 국가로 배송 목록에 지정된 국가로 제한합니다. |
| [!UICONTROL Ship to Specific Countries] | 웹 사이트 | DHL 선적을 보낼 수 있는 국가를 지정합니다. [!UICONTROL Ship to Applicable Countries] 옵션에서 `Specific Countries`을(를) 선택한 경우 이 선택된 국가 목록이 사용됩니다. |
| [!UICONTROL Show Method if Not Applicable] | 웹 사이트 | 체크아웃 중에 DHL이 배송 방법으로 나타나는 시점을 결정합니다. 옵션: <br/>**`Yes`**- DHL은 주문에 적용되지 않더라도 체크아웃 중에 항상 배송 옵션으로 나타납니다.<br/>**`No`** - DHL은 주문에 적용할 수 있는 경우(즉, 주문 중량이 최대 중량을 초과하는 경우) 체크아웃 중에 배송 옵션으로 나타납니다. |
| [!UICONTROL Debug] | 웹 사이트 | 오류 정보가 있는 로그 파일을 만듭니다. |
| [!UICONTROL Sort Order] | 웹 사이트 | 체크아웃 중에 다른 게재 방법과 함께 나열할 때 DHL이 표시되는 순서를 결정하는 숫자입니다. 목록의 맨 위에 배치하려면 `0`을(를) 입력하십시오. |

{style="table-layout:auto"}
