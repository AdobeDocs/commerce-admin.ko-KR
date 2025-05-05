---
title: SKU별 주문
description: SKU를 통한 고객 맞춤 오더를 지원하도록 스토어를 구성하는 방법에 대해 알아봅니다.
exl-id: cb39554f-ab76-46d5-8217-e43bc8f9f88d
feature: Orders, Storefront, Configuration
source-git-commit: 61df9a4bcfaf09491ae2d353478ceb281082fa74
workflow-type: tm+mt
source-wordcount: '586'
ht-degree: 0%

---

# SKU별 주문

{{ee-feature}}

&#39;SKU&#39;는 &#39;Stock Keeping Unit&#39;입니다. SKU는 일반적으로 온라인 판매자가 크기, 색상, 가격 및 재료와 같은 가장 중요한 제품 특성을 식별하는 데 도움이 됩니다. 제품 ID가 SKU와 다릅니다.

- `Product ID`은(는) 제품을 식별하기 위해 내부적으로 사용되며 고객이 사용할 수 없는 일련의 순차적인 숫자입니다.
- `SKU`은(는) 일반적으로 마케팅 또는 내부 추적을 위한 제품 이름과 특성을 기반으로 판매자가 생성합니다. 예: 파란색, 면 T-셔츠, 크기: T-COT-MED-BL. 필요한 경우 판매자가 SKU를 변경할 수 있습니다.

일반적으로, SKU는 제품의 구별되는 특성을 나타내는 약어 세트를 포함한다. 최대 SKU 길이는 64자입니다. SKU는 인벤토리를 효과적으로 추적 및 관리하는 데 중요하므로 전자 상거래에 올바르게 설정하는 것이 중요합니다.

_Order by SKU_&#x200B;은(는) 모든 쇼핑객에게 편리하도록 스토어에 표시하거나 특정 고객 그룹의 쇼핑객만 사용할 수 있는 [위젯](../content-design/widgets.md)입니다. 구매자는 SKU별 주문 블록에 SKU 및 수량 정보를 직접 입력하거나 고객 계정에서 csv 파일을 업로드할 수 있습니다. 구성에 관계없이 저장소 관리자는 항상 SKU로 주문할 수 있습니다.

![Storefront에서 SKU로 주문](./assets/storefront-order-by-sku.png){width="700" zoomable="yes"}

## SKU별 주문 구성

1. _관리자_ 사이드바에서 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**(으)로 이동합니다.

1. 왼쪽 패널에서 **[!UICONTROL Sales]** 섹션을 확장하고 아래의 **[!UICONTROL Sales]**&#x200B;을(를) 선택합니다.

1. **[!UICONTROL Order by SKU Settings]** 섹션에서 ![확장 선택기](../assets/icon-display-expand.png)를 확장합니다.

1. **[!UICONTROL Enable Order by SKU on my Account in Storefront]**&#x200B;을(를) 다음 중 하나로 설정합니다.

   - `Yes, for Everyone` - SKU별 주문 블록은 모든 쇼핑객의 매장에서 사용할 수 있습니다.
   - `Yes, for Specified Customer Groups` - SKU별 주문은 `Wholesale`과(와) 같은 특정 고객 그룹의 멤버만 사용할 수 있습니다.
   - `No` - SKU별 주문 블록이 상점 앞에 표시되지 않으며 고객 계정에서 SKU별 주문 페이지를 사용할 수 없습니다.

   ![SKU 설정별 주문](../configuration-reference/sales/assets/sales-order-by-sku-settings.png){width="600" zoomable="yes"}

1. **[!UICONTROL Save Config]**&#x200B;을(를) 클릭합니다.

![Adobe Commerce B2B](../assets/b2b.svg)(Adobe Commerce B2B만 해당) _&#x200B;**SKU별 주문 기능을 사용하려면 빠른 주문 기능을 사용하지 않도록 설정하십시오.**&#x200B;_

1. **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**(으)로 이동합니다.

1. _[!UICONTROL General]_&#x200B;아래의 왼쪽 패널에서&#x200B;**[!UICONTROL B2B Features]**&#x200B;을(를) 선택합니다.

1. **[!UICONTROL B2B Features]** 섹션에서 ![확장 선택기](../assets/icon-display-expand.png)를 확장합니다.

1. **[!UICONTROL Enable Quick Order]**&#x200B;을(를) `No`(으)로 설정합니다.

   [빠른 주문 기능](../b2b/quick-order.md)을 통해 고객과 게스트는 SKU 또는 제품 이름을 기반으로 빠르게 주문할 수 있습니다.

## Storefront 경험

스토어에 대해 기능이 구성되면 고객은 _SKU별 주문_ 위젯이 포함된 모든 페이지 또는 계정 대시보드에서 SKU별로 주문할 수 있습니다.

### 페이지 블록에서 SKU로 주문

1. _SKU별 주문_ 블록에서 고객이 주문할 항목의 **[!UICONTROL SKU]** 및 **[!UICONTROL Qty]**&#x200B;을(를) 입력합니다.

1. 다른 항목을 추가하려면 **[!UICONTROL Add Row]**&#x200B;을(를) 클릭하고 프로세스를 반복합니다.

1. **[!UICONTROL Add to Cart]**&#x200B;을(를) 클릭합니다.

### 고객 계정에서 SKU로 주문

1. 상점에서 고객은 계정에 로그인합니다.

1. 왼쪽 패널에서 **[!UICONTROL Order by SKU]**&#x200B;을(를) 선택합니다.

1. 환경 설정에 따라 개별 항목을 추가합니다.

   _&#x200B;**SKU별로 각 항목 추가:**&#x200B;_

   - 주문할 항목의 **[!UICONTROL SKU]** 및 **[!UICONTROL Qty]**&#x200B;을(를) 입력합니다.

   - 필요에 따라 항목을 추가하려면 _행 추가_ ![더하기 기호 단추](../assets/button-add-item.png)를 클릭하고 필요한 수만큼 반복합니다.

   - **[!UICONTROL Add to Cart]**&#x200B;을(를) 클릭합니다.

   _&#x200B;**여러 항목의 CSV 파일을 업로드합니다.**&#x200B;_

   - `SKU` 및 `Qty`에 대한 열이 포함된 [데이터 가져오기 CSV](../systems/data-csv.md)(쉼표로 구분된 값) 파일을 준비합니다.

   가져올 ![SKU](./assets/account-dashboard-order-by-sku-import.png){width="500" zoomable="yes"}

   - CSV 파일을 업로드하려면 **[!UICONTROL Choose File]**&#x200B;을(를) 클릭하고 업로드할 파일을 선택하십시오.

   - **[!UICONTROL Add to Cart]**&#x200B;을(를) 클릭합니다.

   추가 옵션이 있는 제품이 있는 경우, 장바구니에서 제품에 주의가 필요하다는 메시지가 고객에게 표시됩니다.

   ![제품에 주의가 필요합니다](./assets/account-dashboard-order-by-sku-cart-product-requires-attention.png){width="600" zoomable="yes"}

   >[!NOTE]
   >
   >중복 SKU가 있는 경우 수량은 장바구니에서 하나의 라인 항목으로 결합됩니다. 고객은 항목의 수량을 변경하고 **[!UICONTROL Update Shopping Cart]**&#x200B;을(를) 클릭하여 합계를 다시 계산할 수 있습니다.

