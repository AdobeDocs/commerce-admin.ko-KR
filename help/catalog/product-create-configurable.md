---
title: 구성 가능한 제품
description: 쇼핑객에게 다양한 선택 항목을 제공하는 구성 가능한 제품을 만드는 방법을 알아봅니다.
exl-id: 2066fd20-5227-41e9-b213-31825a58ebd9
feature: Catalog Management, Products
source-git-commit: 6fcbcd3b7cace10f0841a46b3cd27343862b3f3b
workflow-type: tm+mt
source-wordcount: '1981'
ht-degree: 0%

---

# 구성 가능한 제품

구성 가능한 제품은 변형(예: 색상 또는 크기)에 대한 드롭다운 옵션과 함께 단일 제품으로 표시됩니다. 각 변형은 자체 SKU를 사용하는 별도의 간단한 제품으로, 사용자 지정 옵션이 있는 간단한 제품과 달리 개별 인벤토리 추적을 가능하게 합니다.

**각 변형에 대한 인벤토리를 추적해야 하는 여러 옵션(색상, 크기, 재질 등)이 있는 제품에 가장 적합합니다.** 초기 설정이 더 오래 걸리지만 더 나은 확장성을 제공합니다.

![구성 가능한 제품](./assets/product-configurable.png){width="700" zoomable="yes"}

## 시작하기 전에

### 사전 요구 사항 체크리스트

구성 가능한 제품을 만들기 전에 다음을 확인하십시오.

1. **특성 집합** - 변형 특성(예: 색상 및 크기)이 포함된 특성 집합입니다.
1. **변형 특성 생성됨** - 아래 설정으로 구성된 특성
1. **제품 이미지** - (선택 사항이지만 권장됨) 상위 제품 및 각 변형에 대한 이미지

### 속성 요구 사항

제품 변형에 사용되는 각 속성에는 다음 설정이 있어야 합니다.

| 속성 | 필수 설정 |
|--- |--- |
| [!UICONTROL Scope] | `Global` |
| [!UICONTROL Catalog Input Type for Store Owner] | `Dropdown`, `Visual Swatch` 또는 `Text Swatch` |
| [!UICONTROL Values Required] | `Yes` |

{style="table-layout:auto"}

특성 만들기에 대한 지침은 [제품 특성](product-attributes.md)을 참조하세요.

## 1단계: 제품 기반 만들기

### 1단계: 제품 유형 선택

1. _관리자_ 사이드바에서 **[!UICONTROL Catalog]** > **[!UICONTROL Products]**(으)로 이동합니다.

1. 오른쪽 상단의 _[!UICONTROL Add Product]_( ![메뉴 화살표](../assets/icon-menu-down-arrow-red.png){width="25"}) 메뉴에서&#x200B;**[!UICONTROL Configurable Product]**&#x200B;을(를) 선택합니다.

   ![구성 가능한 제품 추가](./assets/product-add-configurable.png){width="700" zoomable="yes"}

### 2단계: 속성 세트 선택

[특성 집합](attribute-sets.md)은(는) 제품 양식에 표시되는 필드와 변형에 사용할 수 있는 특성을 결정합니다.

1. 페이지 상단에 있는 속성 세트 필드를 클릭하고 다음 중 하나를 수행합니다.

   - **[!UICONTROL Search]**&#x200B;의 경우 특성 집합의 이름을 입력하십시오.
   - 목록에서 사용할 속성 세트를 선택합니다.

   선택한 속성 세트를 반영하도록 양식이 업데이트됩니다.

1. 특성 집합에 다른 특성을 추가하려면 **[!UICONTROL Add Attribute]**&#x200B;을(를) 클릭하고 [특성 추가](product-attributes-add.md)의 지침을 따릅니다.

   ![템플릿 선택](./assets/product-create-choose-attribute-set.png){width="600" zoomable="yes"}

### 3단계: 기본 정보 입력

1. 제품 **[!UICONTROL Product Name]**&#x200B;을(를) 입력하십시오.

1. 제품 이름을 기준으로 기본 **[!UICONTROL SKU]**&#x200B;을(를) 적용하거나 다른 값을 입력하십시오.

1. 제품 **[!UICONTROL Price]**&#x200B;을(를) 입력하십시오.

   >[!NOTE]
   >
   >이 가격은 하위 제품 가격으로 대체됩니다. 고객에게 표시되는 실제 가격은 [!UICONTROL In Stock] 하위 제품에서 가져옵니다.

1. 제품을 아직 게시할 준비가 되지 않았으므로 **[!UICONTROL Enable Product]**&#x200B;을(를) `No`(으)로 설정하십시오.

1. **[!UICONTROL Save]**&#x200B;을(를) 클릭하고 계속합니다.

   제품을 저장하면 왼쪽 위 모서리에 [스토어 보기](introduction.md#product-scope) 선택기가 나타납니다.

1. 제품을 사용할 수 있는 **[!UICONTROL Store View]**&#x200B;을(를) 선택하십시오.

   ![스토어 보기 선택](./assets/product-create-store-view-choose.png){width="600" zoomable="yes"}

### 4단계: 기본 설정 완료

1. **[!UICONTROL Tax Class]**&#x200B;을(를) 다음 중 하나로 설정합니다.

   - `None`
   - `Taxable Goods`

1. **[!UICONTROL Quantity]**&#x200B;을(를) 비워 둡니다. 수량은 제품 변형에 의해 결정됩니다.

1. **[!UICONTROL Stock Status]**&#x200B;을(를) 설정된 대로 둡니다.

   구성 가능한 제품의 재고 상태는 관련 변형에 의해 결정됩니다. 제품이 수량 없이 저장되었으므로 **[!UICONTROL Stock Status]**&#x200B;이(가) `Out of Stock`(으)로 설정됩니다.

   >[!NOTE]
   >
   >구성 가능한 제품의 **재고 상태**&#x200B;는 하위 제품의 재고 상태를 부분적으로 기반으로 하여 **_반수동으로_** 제어된 설정입니다. **_다중 기준_** 재고 상태 계산의 일부입니다. 자세한 내용은 [재고 상태 구성](#configure-stock-status)을 참조하십시오.

1. 제품 **[!UICONTROL Weight]**&#x200B;을(를) 입력하십시오.

   >[!NOTE]
   >
   >구성 가능한 제품에는 항상 무게가 있어야 합니다. 드롭다운에서 **[!UICONTROL This item has no weight]**&#x200B;을(를) 선택하면 제품을 저장할 때 자동으로 **[!UICONTROL This item has weight]**(으)로 변경됩니다.

1. **[!UICONTROL Visibility]**&#x200B;의 기본 `Catalog, Search` 설정을 사용합니다.

1. [새 제품](../content-design/widget-new-products-list.md) 목록에 제품을 포함하려면 **[!UICONTROL Set Product as New]** 확인란을 선택하십시오.

1. 제품에 범주를 할당하려면 **[!UICONTROL Select…]** 상자를 클릭하고 다음 중 하나를 수행합니다.

   **기존 범주 선택:**

   - 일치하는 항목을 찾으려면 상자에 입력을 시작하십시오.

   - 할당할 각 범주의 확인란을 선택합니다.

   ![번들 제품에 대해 하나 이상의 범주를 선택하십시오](./assets/product-create-categories.png){width="600" zoomable="yes"}

   **새 범주 만들기:**

   - **[!UICONTROL New Category]**&#x200B;을(를) 클릭합니다.

   - **[!UICONTROL Category Name]**&#x200B;을(를) 입력하고 **[!UICONTROL Parent Category]**&#x200B;을(를) 선택하여 메뉴 구조에서 위치를 결정합니다.

   - **[!UICONTROL Create Category]**&#x200B;을(를) 클릭합니다.

1. **[!UICONTROL Country of Manufacture]** 선택.

   속성 세트에 따라 추가 속성이 나타날 수 있습니다. 나중에 완료할 수 있습니다.

### 5단계: 저장 및 계속

작업을 저장하기에 좋은 시간입니다. 오른쪽 상단의 **[!UICONTROL Save]**&#x200B;을(를) 클릭합니다. 다음 단계에서는 각 변형에 대한 구성을 설정합니다.

## 2단계: 제품 변형 추가

다음 단계에서는 여러 변형에 대한 구성을 추가하는 방법을 보여줍니다. 페이지 상단의 진행률 표시줄은 프로세스의 현재 위치를 보여줍니다.

**예:** 3가지 색상과 3가지 크기의 셔츠의 경우 고유 SKU를 사용하는 9가지 간단한 제품(조합당 하나)을 만듭니다. 기본적으로 각 변형에 대한 제품 이름과 SKU는 속성 값과 상위 제품 이름 또는 SKU를 기반으로 합니다.

### 6단계: 변형 속성 선택

1. _[!UICONTROL Configurations]_&#x200B;섹션까지 아래로 스크롤한 다음&#x200B;**[!UICONTROL Create Configurations]**&#x200B;을(를) 클릭합니다.

   ![구성](./assets/product-configurable-create-configurations.png){width="600" zoomable="yes"}

1. 변형으로 포함할 각 속성의 확인란을 선택합니다.

   이 예제에서는 `color` 및 `size`을(를) 선택합니다.

   ![특성 선택](./assets/product-create-configurable-step1.png){width="600" zoomable="yes"}

   목록에는 구성 가능한 제품에서 사용할 수 있는 속성 세트의 모든 속성이 포함됩니다.

1. 특성을 추가해야 하는 경우 **[!UICONTROL Create New Attribute]**&#x200B;을(를) 클릭하고 다음을 수행합니다.

   - 속성 속성을 완료합니다.

   - **[!UICONTROL Save Attribute]**&#x200B;을(를) 클릭합니다.

   - 속성에 대한 확인란을 선택합니다.

1. 오른쪽 상단의 **[!UICONTROL Next]**&#x200B;을(를) 클릭합니다.

### 7단계: 속성 값 선택

1. 각 속성에 대해 제품에 적용되는 값의 확인란을 선택합니다.

   ![특성 값](./assets/product-create-configurable-step2.png){width="600" zoomable="yes"}

1. 특성을 다시 정렬하려면 _순서 바꾸기_( ![정렬 순서 아이콘](../assets/icon-sort-order.png)) 아이콘을 선택하고 섹션을 새 위치로 이동하십시오.

   이 순서는 제품 페이지에서 드롭다운 목록의 위치를 결정합니다.

1. 진행률 표시줄에서 **[!UICONTROL Next]**&#x200B;을(를) 클릭합니다.

### 8단계: 이미지, 가격 및 인벤토리 구성

이 단계에서는 각 구성에 대한 이미지, 가격 및 수량을 결정합니다. 사용 가능한 옵션은 각각에 대해 동일합니다. 모든 SKU에 동일한 설정을 적용하거나, 각 SKU에 고유한 설정을 적용하거나, 설정을 지금 건너뛸 수 있습니다.

#### 이미지 구성

적용되는 구성 옵션을 선택합니다.

**옵션 1: 모든 SKU에 단일 이미지 집합 적용**

1. **[!UICONTROL Apply single set of images to all SKUs]**&#x200B;을(를) 선택합니다.

1. 제품 갤러리에 포함할 각 이미지를 찾아보거나 상자로 이미지를 드래그합니다.

![모든 SKU에 동일한 이미지 사용](./assets/product-configurations-images-apply-single-set.png){width="600" zoomable="yes"}

**옵션 2: 각 SKU에 고유한 이미지 적용**

상위 제품 이미지가 이미 업로드되었으므로 이 옵션을 사용하여 각 변형에 대한 이미지를 업로드합니다. 누군가 특정 변형을 구매할 때 장바구니에 표시되는 다른 이미지를 추가할 수 있습니다.

1. **[!UICONTROL Apply unique images by attribute to each SKU]**&#x200B;을(를) 선택합니다.

1. 이미지가 나타내는 **[!UICONTROL Attribute]**&#x200B;을(를) 선택합니다(예: `color`).

1. 각 속성 값에 대해 해당 구성에 사용할 이미지를 찾아보거나 상자로 드래그합니다.

   이미지를 값 상자로 드래그하면 다른 값의 섹션에도 표시됩니다. 이미지를 삭제하려면 _휴지통_(![휴지통 아이콘](../assets/icon-delete-trashcan-solid.png)) 아이콘을 클릭합니다.

   ![SKU당 고유 이미지](./assets/product-configurable-create-configurations-add-images-unique.png){width="600" zoomable="yes"}

#### 가격 구성

>[!NOTE]
>
>구성 가능한 제품은 카탈로그에 자체 가격이 없습니다. 구성 가능한 제품 가격은 해당 [!UICONTROL In Stock] 하위 제품에서 파생되었습니다.

적용되는 구성 옵션을 선택합니다.

**옵션 1: 모든 SKU에 동일한 가격 적용**

1. 가격이 모든 변형에 대해 동일하면 **[!UICONTROL Apply single price to all SKUs]**&#x200B;을(를) 선택합니다.

1. **[!UICONTROL Price]** 입력.

   ![SKU당 동일 가격](./assets/product-configurable-create-configurations-price-all-skus.png){width="600" zoomable="yes"}

**옵션 2: 각 SKU에 대해 다른 가격 적용**

1. 각 변형 또는 일부 변형에 대해 가격이 다른 경우 **[!UICONTROL Apply unique prices by attribute to each SKU]**&#x200B;을(를) 선택하십시오.

1. 가격 차이의 기준이 되는 **[!UICONTROL Attribute]**&#x200B;을(를) 선택하십시오.

1. 각 특성 값에 대해 **[!UICONTROL Price]**&#x200B;을(를) 입력하십시오.

   이 예에서는 XL 크기가 더 비쌉니다.

   ![SKU당 고유 가격](./assets/product-configurable-create-configurations-price-unique.png){width="600" zoomable="yes"}

#### 인벤토리 구성

적용되는 구성 옵션을 선택합니다.

**옵션 1: 모든 SKU에 동일한 수량을 적용**

수량이 모든 SKU에 대해 동일하면 **[!UICONTROL Apply single quantity to each SKU]**&#x200B;을(를) 선택하고 수량을 지정하십시오.

단일 Source 판매자(_S):_

**[!UICONTROL Quantity]** 입력.

[Inventory management &#x200B;](../inventory-management/introduction.md):_을(를) 사용하는 여러 Source 판매자(_M)

생성된 모든 제품 변형에 대해 출처를 지정하고 수량을 추가합니다.

1. **[!UICONTROL Apply single quantity to each SKU]** 옵션을 선택하십시오.

1. 원본을 추가하려면 **[!UICONTROL Assign Sources]**&#x200B;을(를) 클릭하십시오.

1. 추가할 소스를 검색하거나 검색합니다. 제품 소스 옆에 있는 확인란을 선택합니다.

1. 출처당 현재고 금액을 입력합니다.

   ![모든 SKU에 대한 단일 수량, 원본 할당](./assets/inventory-configure-product-quantity.png){width="600" zoomable="yes"}

**옵션 2: 특성별로 다른 수량을 적용**

단일 Source 판매자(_S):_

각 특성 값에 대해 **[!UICONTROL Quantity]**&#x200B;을(를) 입력하십시오.

[Inventory management &#x200B;](../inventory-management/introduction.md):_을(를) 사용하는 여러 Source 판매자(_M)

생성된 모든 제품 변형에 대해 출처를 지정하고 수량을 추가합니다.

1. **[!UICONTROL Apply unique quantity by attribute to each SKU]**&#x200B;을(를) 선택합니다.

1. 각 변형에 대해 **[!UICONTROL Quantity]**&#x200B;을(를) 입력하십시오.

   ![속성당 다른 수량](./assets/product-configurations-quantity-different.png){width="600" zoomable="yes"}

이미지, 가격 및 수량 구성이 완료되면 오른쪽 상단의 **[!UICONTROL Next]**&#x200B;을(를) 클릭합니다.

### 9단계: 제품 구성 생성

제품 목록이 나타날 때까지 잠시 기다렸다가 다음 중 하나를 수행합니다.

- 구성에 만족하면 **[!UICONTROL Generate Products]**&#x200B;을(를) 클릭합니다.

- 수정하려면 **[!UICONTROL Back]**&#x200B;을(를) 클릭하십시오.

![제품 변형을 생성하기 전에 요약 검토](./assets/product-create-configurable-summary.png){width="600" zoomable="yes"}

현재 제품 변형이 _구성_ 섹션 하단에 나타납니다.

![현재 구성](./assets/product-create-configurable-generated.png){width="600" zoomable="yes"}

### 10단계: 제품 이미지 추가

1. 아래로 스크롤하여 ![&#x200B; 섹션에서 &#x200B;](../assets/icon-display-expand.png)확장 선택기&#x200B;_[!UICONTROL Images and Videos]_&#x200B;를 확장합니다.

1. _카메라_ 타일을 클릭하고 구성 가능한 제품에 사용할 기본 이미지를 찾습니다.

자세한 내용은 [이미지 및 비디오](product-images-and-video.md)를 참조하세요.

### 11단계: 전체 제품 정보

아래로 스크롤하여 필요에 따라 다음 섹션의 정보를 작성합니다.

- [콘텐츠](product-content.md)

- [관련 제품, 상향 판매 및 교차 판매](related-products-up-sells-cross-sells.md)

- [검색 엔진 최적화](product-search-engine-optimization.md)

- [사용자 정의 가능한 옵션](settings-advanced-custom-options.md)

- [웹 사이트의 제품](settings-basic-websites.md)

- [디자인](settings-advanced-design.md)

- [선물 옵션](product-gift-options.md)

## 3단계: 제품 게시

### 12단계: 제품 게시

1. 제품을 카탈로그에 게시할 준비가 되면 **[!UICONTROL Enable Product]**&#x200B;을(를) `Yes`(으)로 설정하십시오.

1. 다음 중 하나를 수행합니다.

   **메서드 1: 저장 및 미리 보기**

   - 오른쪽 상단에서 **[!UICONTROL Save]**&#x200B;을(를) 클릭합니다.

   - 스토어에서 제품을 보려면 **[!UICONTROL Customer View]**&#x200B;관리자&#x200B;_(_&#x200B;메뉴 화살표![) 메뉴에서 &#x200B;](../assets/icon-menu-down-arrow-black.png)을(를) 선택하십시오.

   저장소가 새 브라우저 탭에서 열립니다.

   ![고객 보기](./assets/product-admin-customer-view.png){width="600" zoomable="yes"}

   **메서드 2: 저장 및 닫기**

   _[!UICONTROL Save]_( ![메뉴 화살표](../assets/icon-menu-down-arrow-red.png){width="25"}) 메뉴에서&#x200B;**[!UICONTROL Save & Close]**&#x200B;을(를) 선택합니다.

## 재고 상태 구성

구성 가능한 제품 스톡 상태는 단순 제품 스톡 상태와 다릅니다. 구성 가능한 제품의 경우 재고 상태는 **_multi-criteria_** 계산의 일부입니다.

### 재고 상태 작동 방식

재고 상태 동작의 주요 원칙:

| 상태를 다음으로 설정: | 결과 | 하위 제품에 의해 제어됩니까? |
|---|---|---|
| `Out of Stock`(수동) | 항상 Admin 및 Storefront에 `Out of Stock`을(를) 표시합니다. | 아니요 - 수동으로 `In Stock`(으)로 변경될 때까지 유지됩니다. |
| `In Stock`(수동) | 하위 제품을 기반으로 상태가 동적입니다. | 부분 - 아래 세부 정보 참조 |

{style="table-layout:auto"}

### &quot;재고&quot;로 설정된 경우

구성 가능한 제품 재고 상태를 `In Stock`(으)로 수동으로 설정하는 경우 재고 설정에 따라 다르게 동작합니다.

**기본 원본/주식만 있음:**

- **관리자 및 상점:** 재고 상태가 하위 제품 가용성을 자동으로 반영합니다.

**하나 이상의 사용자 지정 원본/재고 있음:**

- **Storefront:** 재고 상태가 하위 제품 가용성을 자동으로 반영합니다.
- **관리자:**&#x200B;은(는) 수동으로 변경될 때까지 `In Stock`(하위 제품으로 제어되지 않음) 상태로 유지됩니다

>[!NOTE]
>
>사용자 지정 재고 및 원본은 [Inventory management](../inventory-management/sources-stocks.md) 확장의 일부입니다. 이 도구를 스톡 및 소스 관리에만 사용하는 것이 좋습니다. 기본 원본 및 스톡 함수는 이제 더 이상 사용되지 않는 `CatalogInventory` 모듈의 일부입니다.

### 수동 재고 상태 변경

관리 사용자 작업, 파일 가져오기 또는 API 호출을 통해 재고 상태를 수동으로 `Out of Stock`(으)로 설정하는 경우 수동으로 다시 `Out of Stock`(으)로 변경할 때까지 관리 및 상점 모두에서 `In Stock` 상태로 유지됩니다. 하위 제품 재고 상태의 영향을 받지 않습니다.

## 시스템 구성(선택 사항)

### 장바구니 썸네일에 변형 이미지 표시

각 변형에 대해 서로 다른 이미지가 있는 경우 장바구니 썸네일에 대한 올바른 이미지를 표시하도록 시스템을 구성할 수 있습니다.

1. _관리자_ 사이드바에서 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**(으)로 이동합니다.

1. 왼쪽 패널에서 **[!UICONTROL Sales]**&#x200B;을(를) 확장하고 **[!UICONTROL Checkout]**&#x200B;을(를) 선택합니다.

1. ![&#x200B; 섹션에서 &#x200B;](../assets/icon-display-expand.png)확장 선택기&#x200B;_[!UICONTROL Shopping Cart]_&#x200B;를 확장합니다.

1. **[!UICONTROL Configurable Product Image]**&#x200B;을(를) `Product Thumbnail Itself`(으)로 설정합니다.

1. **[!UICONTROL Save Config]**&#x200B;을(를) 클릭합니다.

   ![장바구니 - 구성 가능한 제품 이미지](./assets/config-checkout-configurable-product.png){width="600" zoomable="yes"}

## 주요 고려 사항

- **변형 유형:** 구매자는 드롭다운, 다중 선택, 시각적 견본 및 텍스트 견본 입력 유형에서 옵션을 선택할 수 있습니다. 각 옵션은 별도의 간단한 제품입니다.

- **인벤토리 추적:** 사용자 지정 옵션이 있는 간단한 제품과 달리 구성 가능한 제품은 각 변형에 대한 인벤토리를 독립적으로 추적합니다.

- **하위 제품 유형:** 하위 제품은 사용자 지정 옵션이 없는 **단순 또는 가상 제품일 수 있습니다**. 하위 제품을 가상화하려면 각 하위 제품에 대한 `Тhis item has no weight` 설정에 대해 **[!UICONTROL Weight]**&#x200B;을(를) 선택하십시오.

- **전역 할당:** 하위 제품은 모든 웹 사이트, 스토어 및 스토어 보기에서 동시에 구성 가능한 제품 **전역**&#x200B;에서 할당되고 할당이 해제됩니다.

- **가격 책정:** 구성 가능한 제품의 가격이 카탈로그에 없습니다. 표시된 가격은 [!UICONTROL In Stock] 하위 제품에서 나옵니다.

- **특성:** 변형 특성에는 전역 범위가 있어야 하며 고객은 값을 선택해야 합니다. 속성은 구성 가능한 제품에 사용되는 속성 세트에 포함되어야 합니다.

- **장바구니 썸네일:** 장바구니 썸네일은 구성 가능한 제품 레코드 또는 제품 변형의 이미지를 표시할 수 있습니다. 위의 [시스템 구성](#system-configuration-optional)을 참조하십시오.

- **특성 편집 페이지에서**&#x200B;을(를) [(으)로 설정하여 견본을 선택할 때 견본 동작:](swatches.md#create-swatches-for-products) **[!UICONTROL Update Product Preview Image]**&#x200B;견본 특성`No`이(가) 해당 단순 제품 이미지를 표시하지 않도록 구성할 수 있습니다.

- **이미지 갤러리 동작:** 테마는 사용자가 제품 구성 사이를 전환할 때 이미지 갤러리가 작동하는 방식을 제어합니다. _Blank_ 테마에 대한 기본 동작은 선택한 변형을 사용하여 상위 구성 가능한 제품 이미지를 재정의합니다. Luma 테마의 경우 기본 동작은 선택한 변형 이미지를 상위 구성 가능한 제품 이미지에 앞에 추가하는 것입니다.
