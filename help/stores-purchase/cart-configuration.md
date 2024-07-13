---
title: 장바구니 구성
description: 스토어에서 구매 경험을 지원하기 위해 구성할 수 있는 장바구니 기능에 대해 알아봅니다.
exl-id: b98ec7ce-9354-4f03-b67e-dd1587f0c866
feature: Shopping Cart, Configuration
source-git-commit: 61df9a4bcfaf09491ae2d353478ceb281082fa74
workflow-type: tm+mt
source-wordcount: '2449'
ht-degree: 0%

---

# 장바구니 구성

장바구니 구성은 고객이 장바구니 페이지로 리디렉션되는 시기와 제품 썸네일에 사용되는 이미지를 포함하여 스토어 고객에게 장바구니가 작동하는 방식을 결정합니다. 또한 체크아웃 프로세스가 시작되기 전에 최소 금액에 도달하도록 주문하고, 견적 가격이 유효한 일수를 지정하고, _주문 총계_ 섹션에서 항목 순서를 지정할 수 있습니다.

[**미니 장바구니**](#mini-cart) - 장바구니 링크/아이콘에 장바구니에 있는 다른 제품(또는 SKU)의 수 또는 모든 항목의 총 수량이 표시되는지 결정하려면 이 옵션을 구성합니다.

[**미니 장바구니 링크**](#configure-the-cart-link) - 고객이 스토어 페이지 상단에 있는 장바구니 아이콘의 항목 수를 클릭할 때 미니 장바구니가 표시되는지 확인하려면 이 옵션을 구성하십시오.

[**장바구니로 리디렉션**](#redirect-to-cart)- 장바구니에 항목이 추가될 때마다 장바구니 페이지가 표시되는지 또는 고객이 페이지로 이동하기로 선택한 경우에만 표시되는지 결정하려면 이 옵션을 구성합니다.

[**견적 수명**](#quote-lifetime) - 가격이 유효한 기간을 지정하려면 이 옵션을 구성합니다.

[**최소 주문 금액**](#minimum-order-amount) - 이러한 옵션을 구성하여 할인이 적용된 후 주문 소계를 충족해야 하는 최소 금액과 장바구니에 표시되는 메시지를 지정합니다.

[**최소 주문 수량**](#minimum-order-quantity) - 이러한 옵션을 구성하여 주문하는 데 필요한 최소 항목 수를 지정합니다.

[**장바구니 썸네일**](#cart-thumbnails) - 장바구니 썸네일 옵션을 구성하여 그룹화되거나 구성 가능한 제품의 장바구니에 표시된 썸네일을 결정합니다.

[**선물 옵션**](#gift-options) - 선물 옵션을 구성하여 고객이 선물 메시지나 인사말 카드를 추가할 수 있는지, 선물 포장 옵션을 사용할 수 있는지 확인합니다.

>[!NOTE]
>
>체크아웃 프로세스 구성에 대한 자세한 내용은 [체크아웃 옵션](checkout-process.md)을 참조하십시오.

## 미니 카트

_미니 장바구니_에 장바구니에 있는 항목의 요약이 표시됩니다. 기본적으로 활성화되어 있으며 페이지 상단의 장바구니 링크를 클릭하면 표시됩니다.
장바구니에 있는 다른 제품(또는 SKU)의 수 또는 모든 항목의 총 수량을 표시하도록 링크를 구성할 수 있습니다.

![쇼핑객이 제품 페이지의 장바구니 사이드바를 표시합니다](./assets/storefront-mini-cart-watch.png){width="700" zoomable="yes"}

>[!NOTE]
>
>_등록됨_ 고객의 경우 여러 장치 및 브라우저에서 미니 장바구니가 자동으로 동기화되지 않는 경우가 있습니다. 이러한 경우 고객은 해당 디바이스 또는 브라우저에서 [장바구니](cart.md) 페이지를 열면 미니 장바구니를 동기화할 수 있습니다.

### 미니 장바구니 구성

1. _관리자_ 사이드바에서 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**(으)로 이동합니다.

1. 왼쪽 패널에서 **[!UICONTROL Sales]**&#x200B;을(를) 확장하고 **[!UICONTROL Checkout]**&#x200B;을(를) 선택합니다.

1. _[!UICONTROL Mini Cart]_섹션에서 ![확장 선택기](../assets/icon-display-expand.png)를 확장합니다.

   ![미니 장바구니 구성](../configuration-reference/sales/assets/checkout-mini-cart.png){width="600" zoomable="yes"}

1. 특정 스토어 보기에 대한 설정인 경우 구성이 적용되는 [스토어 보기를 선택](../configuration-reference/scope-change.md#set-the-scope)합니다.

   메시지가 표시되면 **[!UICONTROL OK]**&#x200B;을(를) 클릭하여 계속합니다.

1. **[!UICONTROL Display Mini Cart]**&#x200B;을(를) 다음 중 하나로 설정합니다.

   - `Yes` - 스토어 페이지에 미니 장바구니를 표시합니다. 사이드바의 모양은 테마에 따라 다릅니다.
   - `No` - 스토어 페이지에서 미니 장바구니를 표시하지 않도록 설정합니다.

1. 표시가 활성화된 경우 다른 옵션을 업데이트하여 표시를 구성합니다.

   - **[!UICONTROL Number of Items to Display Scrollbar]**&#x200B;의 경우 스크롤 막대가 트리거되기 전에 사이드바에 표시할 수 있는 항목 수를 입력합니다.
   - **[!UICONTROL Maximum Display Recently Added Item(s)]**&#x200B;의 경우 미니 장바구니에 표시할 최근에 추가한 항목의 최대 수를 입력합니다.

1. **[!UICONTROL Save Config]**&#x200B;을(를) 클릭합니다.

### 장바구니 링크 구성

1. _관리자_ 사이드바에서 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**에 연결되었습니다.

1. 왼쪽 패널에서 **[!UICONTROL Sales]**&#x200B;을(를) 확장하고 **[!UICONTROL Checkout]**&#x200B;을(를) 선택합니다.

1. **[!UICONTROL My Cart Link]** 섹션에서 ![확장 선택기](../assets/icon-display-expand.png)를 확장합니다.

1. **[!UICONTROL Display Cart Summary]**&#x200B;을(를) 다음 설정 중 하나로 설정합니다.

   - `Display item quantities` - 이 설정은 각 제품에 대한 수량을 추가하여 장바구니에 있는 총 제품 수를 표시합니다.
   - `Display number of items in cart` - 이 설정은 수량에 관계없이 장바구니에 있는 제품 항목 수를 표시합니다.

   ![내 장바구니 링크에 대한 구성 옵션](../configuration-reference/sales/assets/checkout-my-cart-link.png){width="600" zoomable="yes"}

1. **[!UICONTROL Save Config]**&#x200B;을(를) 클릭합니다.

## 장바구니로 리디렉션

장바구니 페이지는 항목이 장바구니에 추가될 때마다 또는 고객이 페이지로 이동하기로 선택한 경우에만 나타나도록 구성할 수 있습니다. 현재 장바구니에 있는 항목에 대한 기본 정보는 항상 [미니 장바구니](#mini-cart)에서 사용할 수 있습니다. 이러한 결정은 고객이 체크아웃을 계속 진행할 수 있도록 유도하는 이점과 고객이 쇼핑을 계속할 수 있도록 하는 이점의 균형을 맞추는 문제입니다. 그것은 개인적인 선호의 단순한 문제일 수도 있다. 그러나 숫자로 백업하려는 경우 A/B 테스트를 실행하여 전환율이 더 높은 접근 방식을 확인할 수 있습니다.

**_장바구니 표시 시기를 구성하려면:_**

1. _관리자_ 사이드바에서 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**(으)로 이동합니다.

1. 왼쪽 패널에서 **[!UICONTROL Sales]**&#x200B;을(를) 확장하고 **[!UICONTROL Checkout]**&#x200B;을(를) 선택합니다.

1. **[!UICONTROL Shopping Cart]** 섹션에서 ![확장 선택기](../assets/icon-display-expand.png)를 확장합니다.

   ![페이지에서 장바구니 구성 설정을 확장했습니다](../configuration-reference/sales/assets/checkout-shopping-cart.png){width="600" zoomable="yes"}

1. 특정 스토어 보기에 대한 설정인 경우 구성이 적용되는 [스토어 보기를 선택](../configuration-reference/scope-change.md#set-the-scope)합니다.

   메시지가 표시되면 **[!UICONTROL OK]**&#x200B;을(를) 클릭하여 계속합니다.

1. **[!UICONTROL After Adding a Product Redirect to Shopping Cart]**&#x200B;을(를) 다음 중 하나로 설정합니다.

   - `Yes` - 제품이 장바구니에 추가되면 바로 장바구니 페이지를 표시합니다.
   - `No` - 장바구니에 제품을 추가한 후 장바구니로 리디렉션을 사용하지 않습니다.

1. **[!UICONTROL Save Config]**&#x200B;을(를) 클릭합니다.

## 견적 라이프타임

Adobe Commerce B2B를 설치하고 활성화하면 _견적_ 기능에 대한 지원을 추가할 수 있습니다. 이 기능을 사용하면 승인된 구매자가 장바구니에서 요청을 제출하여 가격 협상 프로세스를 시작할 수 있습니다. _견적_ 그리드는 받은 각 견적을 나열하며 구매자와 판매자 간의 통신 내역을 유지합니다. B2B 기능에 대한 자세한 내용은 _Adobe Commerce B2B 사용 안내서_&#x200B;의 [협상된 따옴표](../b2b/quotes.md)를 참조하십시오.

구성에서 장바구니 견적 라이프타임을 설정하여 가격이 유효한 기간을 결정할 수 있습니다. 예를 들어, 쇼핑객이 며칠 후 장바구니를 무인 상태로 두는 경우, 일부 품목의 견적 가격이 더 이상 동일하지 않을 수 있습니다. 기본적으로 견적 수명은 30일로 설정됩니다.

**_견적 라이프타임을 구성하려면:_**

1. _관리자_ 사이드바에서 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**(으)로 이동합니다.

1. 왼쪽 패널에서 **[!UICONTROL Sales]**&#x200B;을(를) 확장하고 **[!UICONTROL Checkout]**&#x200B;을(를) 선택합니다.

1. **[!UICONTROL Shopping Cart]** 섹션에서 ![확장 선택기](../assets/icon-display-expand.png)를 확장합니다.

   ![페이지에서 장바구니 구성 설정을 확장했습니다](../configuration-reference/sales/assets/checkout-shopping-cart.png){width="600" zoomable="yes"}

1. 특정 스토어 보기에 대한 설정인 경우 구성이 적용되는 [스토어 보기를 선택](../configuration-reference/scope-change.md#set-the-scope)합니다.

   메시지가 표시되면 **[!UICONTROL OK]**&#x200B;을(를) 클릭하여 계속합니다.

1. **[!UICONTROL Quote Lifetime (days)]**&#x200B;에 대해 견적 가격이 유효한 일 수를 입력하십시오.

1. **[!UICONTROL Save Config]**&#x200B;을(를) 클릭합니다.

## 최소 주문 금액

이 구성을 통해 할인이 적용된 후 주문 소계를 충족해야 하는 최소 금액을 지정할 수 있습니다. 여러 주소로 배송된 주문은 주소당 최소 주문 금액을 충족해야 할 수 있습니다. 체크아웃 버튼은 최소 주문 금액에 도달한 후에만 사용할 수 있습니다.

![장바구니에 최소 주문 메시지가 표시됩니다](./assets/storefront-cart-minimum-order-amount.png){width="700" zoomable="yes"}

**_최소 주문량을 구성하려면:_**

1. _관리자_ 사이드바에서 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**(으)로 이동합니다.

1. 왼쪽 패널에서 **[!UICONTROL Sales]**&#x200B;을(를) 확장하고 아래의 **[!UICONTROL Sales]**&#x200B;을(를) 선택합니다.

1. **[!UICONTROL Minimum Order Amount]** 섹션에서 ![확장 선택기](../assets/icon-display-expand.png)를 확장합니다.

   ![페이지에서 확장된 최소 순서 구성 옵션](../configuration-reference/sales/assets/sales-minimum-order-amount.png){width="600" zoomable="yes"}

1. 최소 주문량을 요구하려면 **[!UICONTROL Enable]**&#x200B;을(를) `Yes`(으)로 설정하십시오.

1. 최소 주문이 활성화된 경우 다음 옵션을 설정하여 요구 사항을 구성합니다.

   - 할인이 적용된 후 소계에 필요한 **[!UICONTROL Minimum Amount]**&#x200B;을(를) 입력하십시오.

   - **[!UICONTROL Include Discount Amount]**&#x200B;을(를) 다음 중 하나로 설정합니다.

      - `Yes` - 소계가 할인 포함 최소 금액을 충족해야 합니다. 최소 $50의 예를 사용하여 장바구니에 25% 할인이 적용된 $60 상단이 포함된 경우 결과 소계는 $45이고 장바구니가 최소값을 충족하지 않습니다.
      - `No` - 소계가 할인 없이 최소 금액을 충족해야 합니다.

   - **[!UICONTROL Include Tax to Amount]**&#x200B;을(를) 다음 중 하나로 설정합니다.

      - `Yes` - 세금이 포함된 최소 금액을 충족하려면 소계가 필요합니다.
      - `No` - 소계가 세금 없이 최소 금액을 충족하도록 요구합니다.

1. 필요한 경우 최소 주문 금액 메시지 설정을 사용자 정의합니다.

   - **[!UICONTROL Description Message]**&#x200B;의 경우 소계가 최소 금액을 충족하지 않을 때 장바구니 상단에 표시되는 메시지를 사용자 지정하는 데 사용할 텍스트를 입력하십시오.

   - **[!UICONTROL Error to Show in Shopping Cart]**&#x200B;에 장바구니 오류 메시지를 사용자 지정하는 데 사용할 텍스트를 입력하십시오.

   기본 메시지를 사용하려면 메시지 설명 필드를 비워 둡니다.

1. 필요한 경우 다중 주소 주문에 대한 최소 주문 금액 설정을 구성합니다.

   - 다중 주소 순서의 각 주소가 최소 주문 수량을 충족하도록 하려면 **[!UICONTROL Validate Each Address Separately in Multi-address Checkout]**&#x200B;을(를) `Yes`(으)로 설정하십시오.

   - 필요한 경우 최소 주문 금액 메시지 설정을 사용자 정의합니다.

      - **[!UICONTROL Multi-address Description Message]** - 장바구니 상단에 표시되는 메시지를 사용자 지정하는 데 사용할 텍스트를 입력합니다. 이 텍스트는 최소값에 맞지 않습니다.

      - **[!UICONTROL Multi-address Error to Show in Shopping Cart]** - 최소값을 충족하지 않는 다중 주소 주문에 대한 장바구니 오류 메시지를 사용자 지정하는 데 사용할 텍스트를 입력하고 상자에 텍스트를 입력합니다.

     기본 메시지를 사용하려면 메시지 설명 필드를 비워 둡니다.

1. **[!UICONTROL Save Config]**&#x200B;을(를) 클릭합니다.

## 최소 주문 수량

주문에 허용된 최소 수량을 설정할 수 있습니다. 각 고객 그룹에 따라 최소 수량을 구성할 수도 있습니다.

1. **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**(으)로 이동합니다.

1. 왼쪽 패널에서 **[!UICONTROL Catalog]**&#x200B;을(를) 확장하고 **[!UICONTROL Inventory]**&#x200B;을(를) 선택합니다.

1. **[!UICONTROL Product Stock Options]** 섹션에서 ![확장 선택기](../assets/icon-display-expand.png)를 확장합니다.

   ![제품 재고 옵션](../configuration-reference/catalog/assets/catalog-inventory-product-stock-options.png){width="600" zoomable="yes"}

1. **[!UICONTROL Minimum Qty Allowed in Shopping Cart]**&#x200B;의 경우 주문에 대한 제품의 최소 수량을 설정하십시오.

   필요한 경우 **[!UICONTROL Use system value]** 확인란의 선택을 취소하여 이러한 설정을 수정합니다.

   - **[!UICONTROL Customer Group]** 설정을 특정 그룹으로 변경하고 해당 그룹의 **[!UICONTROL Minimum Qty]**&#x200B;을(를) 입력하십시오. 다른 그룹 및 수량 제한을 추가하려면 **[!UICONTROL Add Minimum Qty]**&#x200B;을(를) 클릭하십시오.

   - 모든 고객에 대해 동일한 최소 수량 제한을 설정하려면 `ALL GROUPS` 선택을 유지하고 **[!UICONTROL Minimum Qty]**&#x200B;을(를) 입력하십시오.

1. **[!UICONTROL Save Config]**&#x200B;을(를) 클릭합니다.

   ![장바구니의 최소 수량 요구 사항](./assets/minimum-qty-allowed-in-shopping-cart.png){width="700" zoomable="yes"}

## 장바구니 썸네일

![Adobe Commerce](../assets/adobe-logo.svg)(Adobe Commerce 전용)

장바구니에 표시되는 썸네일 이미지는 고객이 구매하려는 항목에 대한 빠른 개요를 제공합니다. 그러나 옵션이 여러 개인 제품의 경우 이미지가 장바구니에 있는 제품의 변형과 일치하지 않을 수 있습니다. 고객이 특정 색상의 품목을 구매하는 경우 장바구니에 있는 썸네일이 일치하는 것이 이상적입니다.

그룹화되고 구성 가능한 제품 모두에 대한 썸네일 이미지를 설정하여 &quot;상위&quot; 제품 또는 제품 변형의 이미지를 표시할 수 있습니다.

![장바구니에서 각 제품에 대한 썸네일 이미지를 표시합니다](./assets/storefront-cart.png){width="700" zoomable="yes"}

**_장바구니 축소판을 구성하려면:_**

1. _관리자_ 사이드바에서 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**(으)로 이동합니다.

1. 왼쪽 패널에서 **[!UICONTROL Sales]**&#x200B;을(를) 확장하고 **[!UICONTROL Checkout]**&#x200B;을(를) 선택합니다.

1. **[!UICONTROL Shopping Cart]** 섹션에서 ![확장 선택기](../assets/icon-display-expand.png)를 확장합니다.

   ![페이지에서 장바구니 구성 설정을 확장했습니다](../configuration-reference/sales/assets/checkout-shopping-cart.png){width="600" zoomable="yes"}

1. **[!UICONTROL Grouped Product Image]**&#x200B;을(를) 설정하여 [그룹화된 제품](../catalog/product-create-grouped.md)에 대해 장바구니에 사용되는 썸네일 확인:

   - `Product Thumbnail Itself` - 장바구니에 추가된 제품 변형에 할당된 썸네일 사용
   - `Parent Product Thumbnail` - 상위 제품에 지정된 썸네일을 사용합니다.

1. **[!UICONTROL Configurable Product Image]**&#x200B;을(를) 설정하여 [구성 가능한 제품](../catalog/product-create-configurable.md)에 대해 장바구니에 사용되는 썸네일 확인:

   - `Product Thumbnail Itself` - 장바구니에 추가된 제품 변형에 할당된 썸네일 사용
   - `Parent Product Thumbnail` - 상위 제품에 지정된 썸네일을 사용합니다.

1. **[!UICONTROL Save Config]**&#x200B;을(를) 클릭합니다.

## 선물 옵션

사용 가능한 선물 옵션 선택은 체크아웃 프로세스가 시작되기 전에 장바구니에 표시됩니다. 선물 옵션 구성은 고객이 선물 메시지나 인사말 카드를 추가할 수 있는지 여부와 선물 포장 옵션을 사용할 수 있는지 여부를 결정합니다. 각각의 상품은 별도의 메시지와 선물 포장을 할 수 있습니다. 전체 주문에 적용하면 고객이 선물 영수증과 인사카드도 추가할 수 있다.

![상점 첫 화면 예 - 장바구니의 선물 옵션](./assets/storefront-cart-gift-options-for-products-or-order.png){width="700" zoomable="yes"}

선물 옵션 구성은 전체 웹 사이트에 적용되지만 제품 수준에서 재정의할 수 있습니다.

### 선물 옵션 활성화

1. _관리자_ 사이드바에서 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**(으)로 이동합니다.

1. 왼쪽 패널에서 **[!UICONTROL Sales]**&#x200B;을(를) 확장하고 아래의 **[!UICONTROL Sales]**&#x200B;을(를) 선택합니다.

1. 페이지에서 ![확장 선택기](../assets/icon-display-expand.png) **[!UICONTROL Gift Options]**&#x200B;을(를) 확장합니다.

   ![판매 구성 - 선물 옵션 설정](../configuration-reference/sales/assets/sales-gift-options.png){width="600" zoomable="yes"}

1. 기프트 메시지 옵션을 원하는 대로 설정합니다.

   - **[!UICONTROL Allow Gift Messages on Order Level]**&#x200B;에 대해 전체 주문에 대해 하나의 선물 메시지를 활성화하려면 `Yes`을(를) 선택하십시오.
   - **[!UICONTROL Allow Gift Messages for Order Items]**&#x200B;의 경우 `Yes`을(를) 선택하여 고객 장바구니에 개별 항목에 대한 별도의 선물 메시지를 추가할 수 있도록 설정합니다.

1. ![Adobe Commerce](../assets/adobe-logo.svg)(Adobe Commerce만 해당) 환경 설정에 따라 선물 포장 옵션을 설정합니다.

   - **[!UICONTROL Allow Gift Wrapping on Order Level]**&#x200B;에 대해 전체 주문에 대해 하나의 선물 포장을 사용하려면 `Yes`을(를) 선택하십시오.
   - **[!UICONTROL Allow Gift Wrapping for Order Items]**&#x200B;의 경우 `Yes`을(를) 선택하여 고객 장바구니의 각 항목에 개별적으로 선물 포장을 추가할 수 있도록 설정하십시오.

   고객이 포장을 선택할 수 있도록 [선물 포장 디자인](#gift-wrap)을 다르게 정의할 수도 있습니다.

1. ![Adobe Commerce](../assets/adobe-logo.svg)(Adobe Commerce만 해당) 고객에게 선물 영수증을 포함하는 옵션을 제공하려면 **[!UICONTROL Allow Gift Receipt]**&#x200B;을(를) `Yes`(으)로 설정하십시오.

1. ![Adobe Commerce](../assets/adobe-logo.svg)(Adobe Commerce만 해당) 고객에게 인쇄된 카드를 포함할 수 있는 옵션을 제공하려면 **[!UICONTROL Allow Printed Card]**&#x200B;을(를) `Yes`(으)로 설정하십시오.

1. ![Adobe Commerce](../assets/adobe-logo.svg)(Adobe Commerce만 해당) **[!UICONTROL Default Price for Printed Card]**&#x200B;을(를) 입력합니다.

1. **[!UICONTROL Save Config]**&#x200B;을(를) 클릭합니다.

### 선물 포장

![Adobe Commerce](../assets/adobe-logo.svg)(Adobe Commerce 전용)

선물 포장은 배송이 가능한 제품이면 누구나 가능하며, 개별 상품 또는 전체 주문 시 제공이 가능하다. 각 선물 포장 디자인에 대해 별도의 가격을 부과하고, 장바구니에서 제품에 대한 옵션으로 표시되는 각 디자인에 대한 썸네일 이미지를 업로드할 수 있습니다. 고객이 선물 포장 썸네일을 클릭하면 전체 크기 이미지가 표시됩니다. 체크아웃 검토 중에 선물 포장 비용이 _주문 요약_ 섹션에 다른 [체크아웃 합계](checkout-totals-sort-order.md)와 함께 표시됩니다.

선물 포장 이미지는 반복 패턴을 표시하는 견본이어야 하며, 사용할 리본 샘플을 포함할 수도 있습니다. 종이를 스캔하거나 포장된 패키지를 촬영할 수 있습니다. 업로드된 이미지는 GIF, JPG 또는 PNG 이미지일 수 있으며 정사각형이어야 합니다. 다음 예에서 업로드된 선물 포장 이미지는 230 x 230픽셀입니다.

![장바구니의 선물 옵션](./assets/storefront-cart-gift-options-gift-wrap.png){width="700" zoomable="yes"}

#### 선물 포장 디자인 추가

1. _관리자_ 사이드바에서 **[!UICONTROL Stores]** > _[!UICONTROL Other Settings]_>**[!UICONTROL Gift Wrapping]**(으)로 이동합니다.

   ![선물 포장 표](./assets/gift-wrapping.png){width="700" zoomable="yes"}

1. 오른쪽 상단에서 **[!UICONTROL Add Gift Wrapping]**&#x200B;을(를) 클릭합니다.

1. 체크 아웃 중에 표시할 **[!UICONTROL Gift Wrapping Design]**&#x200B;의 이름을 입력하십시오.

   필요한 경우 **[!UICONTROL Scope]**&#x200B;을(를) 변경하고 각 스토어 보기에 대해 다른 이름을 구성할 수 있습니다.

1. 선물 포장 디자인을 사용할 수 있는 **[!UICONTROL Websites]**&#x200B;을(를) 선택하십시오.

1. **[!UICONTROL Status]**&#x200B;을(를) `Enabled`(으)로 설정합니다.

   계절 래핑 옵션이 있는 경우 옵션을 사용하지 않으려면 `Disabled`(으)로 설정할 수 있습니다.

1. 선물 포장 디자인의 **[!UICONTROL Price]**&#x200B;을(를) 입력하십시오.

   이 설정은 제품 수준에서 설정된 선물 포장 가격으로 대체할 수 있습니다.

   ![새 선물 포장](./assets/gift-wrapping-new.png){width="600" zoomable="yes"}

1. 선물 포장의 썸네일 **[!UICONTROL Image]**&#x200B;을(를) 업로드하려면 **[!UICONTROL Choose File]**&#x200B;을(를) 클릭하고 디렉터리에서 업로드할 파일을 선택하십시오.

   레코드가 저장된 후 _[!UICONTROL Gift Wrapping Information]_에 이미지의 축소판이 나타납니다.

1. **[!UICONTROL Save]**&#x200B;을(를) 클릭합니다.

#### 선물 포장 디자인 편집

1. _관리자_ 사이드바에서 **[!UICONTROL Stores]** > _[!UICONTROL Other Settings]_>**[!UICONTROL Gift Wrapping]**(으)로 이동합니다.

1. 목록에서 선물 포장 기록을 찾습니다.

1. _Action_ 열에서 **[!UICONTROL Edit]**&#x200B;을(를) 클릭합니다.

   ![선물 포장 정보 편집](./assets/gift-wrapping-edit.png){width="600" zoomable="yes"}

1. 필요한 사항을 변경합니다.

1. **[!UICONTROL Save]**&#x200B;을(를) 클릭합니다.

#### 선물 포장 디자인 삭제

_선물 포장_ 그리드를 연 상태에서 이러한 방법 중 하나를 사용하여 포장 디자인을 삭제합니다.

**_방법 1: 선물 포장 디자인 하나 삭제_**

1. 편집 모드에서 선물 포장 디자인을 엽니다.

1. 작업 영역의 맨 위에서 **[!UICONTROL Delete]**&#x200B;을(를) 클릭합니다.

1. 메시지가 표시되면 **[!UICONTROL OK]**&#x200B;을(를) 클릭하여 확인합니다.

**_방법 2: 여러 선물 포장 디자인 삭제_**

1. _선물 포장_ 그리드에서 삭제할 각 선물 포장 디자인의 확인란을 선택합니다.

1. **[!UICONTROL Actions]** 컨트롤을 `Delete`(으)로 설정합니다.

1. **[!UICONTROL Submit]**&#x200B;을(를) 클릭합니다.

### 선물 옵션 세금

![Adobe Commerce](../assets/adobe-logo.svg)(Adobe Commerce 전용)

선물 포장과 인쇄된 기프트 카드 가격은 세금을 포함하거나 제외하거나 두 옵션을 모두 표시하도록 구성할 수 있습니다. 전역 또는 웹 사이트 레벨에서 이러한 항목에 대한 세금 분류를 지정할 수도 있습니다.

**_선물 옵션 세금을 구성하려면:_**

1. _관리자_ 사이드바에서 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**(으)로 이동합니다.

1. 왼쪽 패널에서 **[!UICONTROL Sales]**&#x200B;을(를) 확장하고 **[!UICONTROL Tax]**&#x200B;을(를) 선택합니다.

1. **[!UICONTROL Tax Classes]** 섹션에서 ![확장 선택기](../assets/icon-display-expand.png)를 확장합니다.

   ![세금 클래스 구성](../configuration-reference/sales/assets/tax-tax-classes.png){width="600" zoomable="yes"}

1. **[!UICONTROL Tax Class for Gift Options]**&#x200B;을(를) 해당 세금 분류로 설정합니다.

1. **[!UICONTROL Orders, Invoices, Credit Memos Display Settings]** 섹션에서 ![확장 선택기](../assets/icon-display-expand.png)를 확장합니다.

   ![주문, 송장, 대변 메모 표시 설정](../configuration-reference/sales/assets/tax-orders-invoices-credit-memos-display-settings.png){width="600" zoomable="yes"}

1. **[!UICONTROL Display Gift Wrapping Prices]**&#x200B;을(를) 다음 중 하나로 설정합니다.

   - `Excluding Tax`
   - `Including Tax`
   - `Including and Excluding Tax`

1. **[!UICONTROL Display Printed Card Prices]**&#x200B;을(를) 다음 중 하나로 설정합니다.

   - `Excluding Tax`
   - `Including Tax`
   - `Including and Excluding Tax`

1. **[!UICONTROL Save Config]**&#x200B;을(를) 클릭합니다.
