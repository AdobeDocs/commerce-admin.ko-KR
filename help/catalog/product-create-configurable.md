---
title: 구성 가능한 제품
description: 쇼핑객에게 다양한 선택 항목을 제공하는 구성 가능한 제품을 만드는 방법을 알아봅니다.
exl-id: 2066fd20-5227-41e9-b213-31825a58ebd9
feature: Catalog Management, Products
source-git-commit: 01148770946a236ece2122be5a88b963a0f07d1f
workflow-type: tm+mt
source-wordcount: '2416'
ht-degree: 0%

---

# 구성 가능한 제품

구성 가능한 제품은 각 변형의 드롭다운 목록이 있는 단일 제품처럼 보입니다. 각 목록 항목은 실제로 각 제품 변형에 대한 재고를 추적할 수 있도록 하는 고유한 SKU를 사용하는 별도의 간단한 제품입니다. 사용자 지정 옵션이 있는 간단한 제품을 사용해도 각 변형에 대한 인벤토리를 추적하는 기능이 없어도 유사한 효과를 얻을 수 있습니다.

다음 지침은 [제품 템플릿](attribute-sets.md), 필수 필드 및 기본 설정. 각 필수 필드는 빨간색 별표(`*`). 기본 사항을 완료하면 필요에 따라 다른 제품 설정을 완료할 수 있습니다.

![구성 가능한 제품](./assets/product-configurable.png){width="700" zoomable="yes"}

## 1부: 구성 가능한 제품 만들기

구성 가능한 제품은 더 많은 SKU를 사용하며 처음에는 설정하는 데 시간이 조금 더 걸릴 수 있지만 결국 시간을 절약할 수 있습니다. 비즈니스를 확장하려는 경우 구성 가능한 제품 유형은 여러 옵션이 있는 제품에 적합합니다.

시작하기 전에 다음을 준비하십시오. [속성 집합](attribute-sets.md) 에는 각 제품 변형에 대해 허용되는 입력 유형 중 하나로 설정된 속성이 포함됩니다. 예를 들어, 속성 세트에는 색상 및 크기에 대한 드롭다운 속성이 포함될 수 있습니다.

구성 가능한 제품 변형에 사용되는 각 속성의 속성은 다음 설정을 가져야 합니다.

### 제품 변형 속성 요구 사항

| 속성 | 설정 |
|--- |--- |
| [!UICONTROL Scope] | `Global` |
| [!UICONTROL Catalog Input Type for Store Owner] | 제품 변형에 사용되는 속성의 입력 유형은 다음 중 하나여야 합니다. `Dropdown`, `Visual Swatch`, 또는 `Text Swatch`. |
| [!UICONTROL Values Required] | `Yes` |

{style="table-layout:auto"}

### 1단계: 제품 유형 선택

1. 다음에서 _관리자_ 사이드바, 이동  **[!UICONTROL Catalog]** > **[!UICONTROL Products]**.

1. 다음에서 _[!UICONTROL Add Product]_( ![메뉴 화살표](../assets/icon-menu-down-arrow-red.png){width="25"} ) 오른쪽 상단의 메뉴 아래에서&#x200B;**[!UICONTROL Configurable Product]**.

   ![구성 가능한 제품 추가](./assets/product-add-configurable.png){width="700" zoomable="yes"}

### 2단계: 속성 세트 선택

다음 [속성 집합](attribute-sets.md) 제품에 사용되는 필드 선택을 결정합니다. 다음 예에서 사용되는 속성 세트에는 색상 및 크기에 대한 속성이 있습니다. 속성 세트의 이름은 페이지 상단에 표시되며 초기에는 로 설정됩니다. `Default`.

1. 제품에 대해 설정된 속성을 선택하려면 페이지 상단의 필드를 클릭하고 다음 중 하나를 수행합니다.

   - 대상 **[!UICONTROL Search]**&#x200B;속성 세트의 이름을 입력합니다.
   - 목록에서 사용할 속성 세트를 선택합니다.

   양식이 변경 사항을 반영하도록 업데이트됩니다.

1. 속성 집합에 다른 속성을 추가하려면 **[!UICONTROL Add Attribute]** 의 지침을 따르십시오. [속성 추가](product-attributes-add.md).

   ![템플릿 선택](./assets/product-create-choose-attribute-set.png){width="600" zoomable="yes"}

### 3단계: 필요한 설정 완료

1. 제품 입력 **[!UICONTROL Product Name]**.

1. 기본값 적용 **[!UICONTROL SKU]** 제품 이름을 기반으로 하거나 다른 이름을 입력합니다.

1. 제품 입력 **[!UICONTROL Price]**.

1. 제품이 아직 게시할 준비가 되지 않았으므로 을(를) 설정합니다. **[!UICONTROL Enable Product]** 끝 `No`.

1. 클릭 **[!UICONTROL Save]** 계속합니다.

   제품이 저장되면 [스토어 뷰](introduction.md#product-scope) 선택기는 왼쪽 위 모서리에 나타납니다.

1. 다음을 선택합니다. **[!UICONTROL Store View]** 제품을 사용할 수 있는 위치.

   ![스토어 보기 선택](./assets/product-create-store-view-choose.png){width="600" zoomable="yes"}

### 4단계: 기본 설정 완료

1. 설정 **[!UICONTROL Tax Class]** 다음 중 하나를 수행합니다.

   - `None`
   - `Taxable Goods`

1. 다음 **[!UICONTROL Quantity]** 은 제품 변형에 의해 결정되므로 비워 둘 수 있습니다.

1. 나가기 **[!UICONTROL Stock Status]** 설정됨.

   구성 가능한 제품의 재고 상태는 연관된 각 구성에 의해 결정됩니다. 수량을 입력하지 않고 제품이 저장되었기 때문에 **[!UICONTROL Stock Status]** 이(가) (으)로 설정됨 `Out of Stock`.

   >[!NOTE]
   >
   >다음 **재고 상태** 구성 가능한 제품의 **_반수동_** 제어된 설정. 이는 자사의 하위 제품들의 재고 현황에 의해 부분적으로 통제된다. 의 일부입니다. **_다중 기준_** 재고 상태 계산: 다음에 설명되어 있습니다 [재고 상태 구성](#configure-the-stock-status) 섹션.

1. 제품 입력 **[!UICONTROL Weight]**.

>[!NOTE]
>
>구성 가능한 제품에는 항상 무게가 있어야 합니다. 다음을 선택하는 경우 **[!UICONTROL This item has no weight]** 드롭다운 목록에서 자동으로 다음으로 변경됩니다. **[!UICONTROL This item has weight]** 제품을 저장한 후.

1. 기본값 적용 **[!UICONTROL Visibility]** 설정 `Catalog, Search`.

1. 제품을 다음 목록에 표시: [새로운 제품](../content-design/widget-new-products-list.md)를 선택하고 **[!UICONTROL Set Product as New]** 확인란.

1. 제품에 범주를 할당하려면 **[!UICONTROL Select…]** 확인란을 선택하고 다음 중 하나를 수행합니다.

   **기존 범주 선택**:

   - 일치하는 항목을 찾을 때까지 상자에 입력을 시작합니다.

   - 할당할 카테고리의 확인란을 선택합니다.

   ![번들 제품에 대해 하나 이상의 범주를 선택합니다.](./assets/product-create-categories.png){width="600" zoomable="yes"}

   **범주 만들기**:

   - 클릭 **[!UICONTROL New Category]**.

   - 다음을 입력합니다. **[!UICONTROL Category Name]** 및 선택 **[!UICONTROL Parent Category]**&#x200B;를 설정하는 것이 좋습니다.

   s- 클릭 **[!UICONTROL Create Category]**.

1. 다음을 선택합니다. **[!UICONTROL Country of Manufacture]**.

   제품을 설명하는 데 사용되는 추가 속성이 있을 수 있습니다. 선택 항목은 속성 세트에 따라 다르며 나중에 완료할 수 있습니다.

### 5단계: 저장 및 계속

지금이 작업을 저장하기에 좋은 때입니다. 오른쪽 위 모서리에서 을(를) 클릭합니다. **[!UICONTROL Save]**. 다음 일련의 단계에서는 제품의 각 변형에 대한 구성을 설정합니다.

## 2부: 구성 추가

다음 예에서는 세 가지 색상 및 세 가지 크기에 대한 구성을 추가하는 방법을 보여줍니다. 모두 9개의 간단한 제품이 가능한 모든 변형 조합을 포함하도록 고유한 SKU로 만들어집니다. 기본적으로 각 변형에 대한 제품 이름과 SKU는 속성 값과 상위 제품 이름 또는 SKU를 기반으로 합니다.

페이지 맨 위에 있는 진행률 표시줄은 진행 중인 위치를 보여주며 각 단계를 안내합니다.

### 1단계: 속성 선택

1. 위에서 아래로 스크롤하여 _[!UICONTROL Configurations]_섹션 및 클릭&#x200B;**[!UICONTROL Create Configurations]**.

   ![구성](./assets/product-configurable-create-configurations.png){width="600" zoomable="yes"}

1. 구성으로 포함할 각 속성의 확인란을 선택합니다.

   이 예제의 경우 `color` 및 `size` 이(가) 선택되어 있습니다.

   ![속성 선택](./assets/product-create-configurable-step1.png){width="600" zoomable="yes"}

   목록에는 구성 가능한 제품에서 사용할 수 있는 속성 세트의 모든 속성이 포함됩니다.

1. 속성을 추가하려면 **[!UICONTROL Create New Attribute]** 다음을 수행합니다.

   - 속성 속성을 완료합니다.

   - 클릭 **[!UICONTROL Save Attribute]**.

   - 속성에 대한 확인란을 선택합니다.

1. 오른쪽 위 모서리에서 을(를) 클릭합니다. **[!UICONTROL Next]**.

### 2단계: 속성 값 입력

1. 각 속성에 대해 제품에 적용되는 값의 확인란을 선택합니다.

   ![속성 값](./assets/product-create-configurable-step2.png){width="600" zoomable="yes"}

1. 속성을 재배열하려면 _순서 바꾸기_ ( ![정렬 순서 아이콘](../assets/icon-sort-order.png) ) 아이콘을 클릭하고 섹션을 새 위치로 이동합니다.

   이 순서는 제품 페이지에서 드롭다운 목록의 위치를 결정합니다.

1. 진행률 표시줄에서 **[!UICONTROL Next]**.

### 3단계: 이미지, 가격 및 수량 구성

이 단계에서는 각 구성의 이미지, 가격 및 수량을 결정합니다. 사용 가능한 옵션은 각각에 대해 동일하며 하나만 선택할 수 있습니다. 모든 SKU에 동일한 설정을 적용하거나, 각 SKU에 고유한 설정을 적용하거나, 설정을 지금 건너뛸 수 있습니다.

적용되는 구성 옵션을 선택합니다.

다음 방법 중 하나를 사용하여 **[!UICONTROL images]**:

**방법 1:** 모든 SKU에 단일 이미지 세트 적용

1. 선택 **[!UICONTROL Apply single set of images to all SKUs]**.

1. 제품 갤러리에 포함할 각 이미지를 찾아보거나 상자로 드래그합니다.

![모든 SKU에 동일한 이미지 사용](./assets/product-configurations-images-apply-single-set.png){width="600" zoomable="yes"}

**방법 2:** 각 SKU에 고유한 이미지 적용

상위 제품의 이미지가 이미 업로드되었기 때문에 이 옵션을 사용하여 각 색상의 이미지를 업로드할 수 있습니다. 다른 사람이 특정 색상으로 제품을 구매할 때 장바구니에 표시되는 다른 이미지를 추가할 수 있습니다.

1. 선택 **[!UICONTROL Apply unique images by attribute to each SKU]**.

1. 다음 항목 선택 **[!UICONTROL Attribute]** 이미지가 나타내는 요소(예: ) `color`.

1. 각 속성 값에 대해 해당 구성에 사용할 이미지를 찾아보거나 상자로 드래그합니다.

   이미지를 값 상자로 드래그하면 다른 값의 섹션에도 표시됩니다. 이미지를 삭제하려면 _휴지통_ (![휴지통 아이콘](../assets/icon-delete-trashcan-solid.png)) 아이콘.

   ![SKU당 고유한 이미지](./assets/product-configurable-create-configurations-add-images-unique.png){width="600" zoomable="yes"}

다음 방법 중 하나를 사용하여 **[!UICONTROL prices]**:

**방법 1:** 모든 SKU에 동일한 가격 적용

1. 모든 변형에 대한 가격이 동일한 경우 다음을 선택합니다. **[!UICONTROL Apply single price to all SKUs]**.

1. 다음을 입력합니다. **[!UICONTROL Price]**.

   ![SKU당 동일 가격](./assets/product-configurable-create-configurations-price-all-skus.png){width="600" zoomable="yes"}

**방법 2:** 각 SKU에 다른 가격 적용

1. 가격이 제품마다 다르거나 제품의 일부 변형에 따라 다른 경우 다음을 선택합니다. **[!UICONTROL Apply unique prices by attribute to each SKU]**.

1. 다음 항목 선택 **[!UICONTROL Attribute]** 그것이 가격 차이의 기본입니다.

1. 다음을 입력합니다. **[!UICONTROL Price]** 각 속성 값에 대해

   이 예에서는 XL 크기가 더 비쌉니다.

   ![SKU당 고유 가격](./assets/product-configurable-create-configurations-price-unique.png){width="600" zoomable="yes"}

다음 방법 중 하나를 사용하여 **[!UICONTROL Quantity]**:

**방법 1:** 모든 SKU에 동일한 수량 적용

수량이 모든 SKU에 대해 동일한 경우 다음을 선택합니다. **[!UICONTROL Apply single quantity to each SKU]** 수량을 지정합니다.

_단일 소스 판매자_ - 다음을 입력합니다. **[!UICONTROL Quantity]**.

_를 사용하는 다중 소스 판매자 [Inventory management](../inventory-management/introduction.md)_ - 생성된 모든 제품 변형에 대해 출처를 지정하고 수량을 추가합니다.

1. 다음 항목 선택 **[!UICONTROL Apply single quantity to each SKU]** 옵션을 선택합니다.

1. 소스를 추가하려면 **[!UICONTROL Assign Sources]**.

1. 추가할 소스를 검색하거나 검색합니다. 제품에 추가할 소스 옆에 있는 확인란을 선택합니다.

1. 출처당 현재고 금액을 입력합니다.

   ![모든 SKU에 대한 단일 수량, 소스 할당](./assets/inventory-configure-product-quantity.png){width="600" zoomable="yes"}

**방법 2:** 속성별로 다른 수량 적용

_단일 소스 판매자_ - 다음을 입력합니다. **[!UICONTROL Quantity]**.

_를 사용하는 다중 소스 판매자 [Inventory management](../inventory-management/introduction.md)_ - 생성된 모든 제품 변형에 대해 출처를 지정하고 수량을 추가합니다.

1. 수량이 각 SKU에 대해 다른 경우 다음을 선택합니다. **[!UICONTROL Apply unique quantity by attribute to each SKU]**.

1. 다음을 입력합니다. **[!UICONTROL Quantity]** 각.

   ![속성당 다른 수량](./assets/product-configurations-quantity-different.png){width="600" zoomable="yes"}

이미지, 가격 및 수량 구성이 완료되면 **[!UICONTROL Next]** 오른쪽 상단 모서리입니다.

### 4단계: 제품 구성 생성

제품 목록이 나타날 때까지 잠시 기다렸다가 다음 중 하나를 수행합니다.

- 구성에 만족하면 다음을 클릭합니다. **[!UICONTROL Generate Products]**.

- 수정하려면 다음을 클릭하십시오. **[!UICONTROL Back]**.

![제품 변형을 생성하기 전에 요약 검토](./assets/product-create-configurable-summary.png){width="600" zoomable="yes"}

현재 제품 변형이 _구성_ 섹션.

![현재 구성](./assets/product-create-configurable-generated.png){width="600" zoomable="yes"}

### 5단계: 제품 이미지 추가

1. 아래로 스크롤하고 확장합니다. ![확장 선택기](../assets/icon-display-expand.png) 다음 _[!UICONTROL Images and Videos]_섹션.

1. 다음을 클릭합니다. _카메라_ 구성 가능한 제품에 사용할 기본 이미지에 타일을 지정하고 찾아봅니다.

자세한 내용은 [이미지 및 비디오](product-images-and-video.md).

### 6단계: 제품 정보 작성

아래로 스크롤하여 필요에 따라 다음 섹션의 정보를 작성합니다.

- [콘텐츠](product-content.md)

- [관련 제품, 상향 판매 및 교차 판매](related-products-up-sells-cross-sells.md)

- [검색 엔진 최적화](product-search-engine-optimization.md)

- [사용자 정의 가능한 옵션](settings-advanced-custom-options.md)

- [웹 사이트의 제품](settings-basic-websites.md)

- [디자인](settings-advanced-design.md)

- [선물 옵션](product-gift-options.md)

### 7단계: 제품 게시

1. 제품을 카탈로그에 게시할 준비가 되었으면 을 설정합니다. **[!UICONTROL Enable Product]** 끝 `Yes` 다음 중 하나를 수행합니다.

   - **방법 1:** 저장 및 미리 보기

      - 오른쪽 위 모서리에서 을(를) 클릭합니다. **[!UICONTROL Save]**.

      - 스토어에서 제품을 보려면 **[!UICONTROL Customer View]** 다음에 있음 _관리자_ ( ![메뉴 화살표](../assets/icon-menu-down-arrow-black.png) ) 메뉴 아래의 제품에서 사용할 수 있습니다.

     저장소가 새 브라우저 탭에서 열립니다.

     ![고객 보기](./assets/product-admin-customer-view.png){width="600" zoomable="yes"}

   - **방법 2:** 저장 및 닫기

     다음에서 _[!UICONTROL Save]_( ![메뉴 화살표](../assets/icon-menu-down-arrow-red.png){width="25"} ) 메뉴, 선택&#x200B;**[!UICONTROL Save & Close]**.

### 8단계: 장바구니 썸네일 구성

각 변형에 대해 다른 이미지가 있는 경우 장바구니 썸네일에 올바른 이미지를 사용하도록 구성을 설정할 수 있습니다.

1. 다음에서 _관리자_ 사이드바, 이동 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. 왼쪽 패널에서 를 확장합니다. **[!UICONTROL Sales]** 및 선택 **[!UICONTROL Checkout]** 밑에.

1. 확장 ![확장 선택기](../assets/icon-display-expand.png) 다음 _[!UICONTROL Shopping Cart]_섹션.

1. 설정 **[!UICONTROL Configurable Product Image]** 끝 `Product Thumbnail Itself`.

1. 완료되면 다음을 클릭하십시오. **[!UICONTROL Save Config]**.

   ![장바구니 - 구성 가능한 제품 이미지](./assets/config-checkout-configurable-product.png){width="600" zoomable="yes"}

## 재고 상태 구성

구성 가능한 제품 재고 상태는 제품 가용성을 직접 나타내는 단순 제품의 재고 상태와 다릅니다. 구성 가능한 제품의 경우 재고 상태는 **_다중 기준_** 재고 상태 계산.

### 개요

재고 상태 관계의 주요 원칙은 다음과 같습니다.

- 을(를) 변경할 때 **[!UICONTROL Stock Status]** 구성 가능한 제품의 `Out of Stock` 및 클릭 **[!UICONTROL Save]**, 입니다. **_제어되지 않음_** 하위 제품의 재고 상태별. 항상 다음과 같이 표시됩니다. `Out of Stock` 관리자 및 상점 첫 화면에서.

- 을(를) 설정할 때 **[!UICONTROL Stock Status]** 구성 가능한 제품의 `In Stock` 및 클릭 **[!UICONTROL Save]**, 입니다. **_부분적으로만 제어됨_** 관리자 및 상점 첫 화면에 반영되는 하위 제품의 재고 상태별.

### 자세한 설명

다음 _재고 상태_ 구성 가능한 제품 중 은 하위 제품의 재고 상태에 의해 부분적으로 제어되며, 다음에 따라 제어됩니다 **_다중 기준_** 재고 상태 계산:

#### 기본 소스/스톡만 해당:

- 구성 가능한 제품 재고 상태가 인 경우 **_수동_** 을 로 설정 `Out of Stock` 관리자 사용자, 파일 가져오기 또는 API 호출에 의해 는 로 유지됩니다. `Out of Stock` 다음 두 가지 모두에서 **_관리자_** 및 **_상점 첫 화면_** 다음 상태가 될 때까지  **_수동_** 이(가) (으)로 변경됨 `In stock` 관리자, 파일 가져오기 또는 API 호출로. 그 하위 상품의 재고 현황에 의해 통제할 수 없다.

- 구성 가능한 제품 재고 상태가 인 경우 **_수동_** 을 로 설정 `In Stock` 관리자, 파일 가져오기 또는 API 호출에 의해 재고 상태는 입니다. **_자동으로_** 두 제품에서 하위 제품의 재고 상태로 제어됩니다. **_관리자_** 및 **_상점 첫 화면_**.

>[!NOTE]
>
>사용자 지정 재고 및 소스는 [Inventory management](../inventory-management/sources-stocks.md) 확장 및 이 도구를 스톡 및 소스 관리에만 사용하는 것이 좋습니다. 기본 소스 및 스톡 함수는 `CatalogInventory` 모듈: 이제 더 이상 사용되지 않습니다.

#### 하나 이상의 사용자 지정 소스/재고 포함:

- 구성 가능한 제품 재고 상태 값이 **_수동_** 을 로 설정 `Out of Stock` 관리자 사용자, 파일 가져오기 또는 API 호출에 의해 는 로 유지됩니다. `Out of Stock` 다음 두 가지 모두에서 **_관리자_** 및 **_상점 첫 화면_** 다음 상태가 될 때까지 **_수동_** 이(가) (으)로 변경됨 `In Stock` 관리자, 파일 가져오기 또는 API 호출로. It **_할 수 없음_** 하위 제품의 재고 상태에 따라 제어됩니다.

- 구성 가능한 제품 재고 상태 값이 **_수동_** 을 로 설정 `In Stock` 관리자, 파일 가져오기 또는 API 호출에 의해 재고 상태는 입니다. **_자동으로_** 에서 하위 제품의 재고 상태로 제어됩니다. **_상점 첫 화면_** 만 해당.

- 구성 가능한 제품 재고 상태 값이 **_수동_** 을 로 설정 `In Stock` 관리자 사용자, 파일 가져오기 또는 API 호출에 의해 는 로 유지됩니다. `In Stock` 다음에서 **_관리자_** 다음 상태가 될 때까지 **_수동_** 이(가) (으)로 변경됨 `Out of Stock` 관리자, 파일 가져오기 또는 API 호출로. It **_할 수 없음_** 하위 제품의 재고 상태에 따라 제어됩니다.

## 기억해야 할 사항

- 구성 가능한 제품을 사용하면 구매자가 드롭다운, 다중 선택, 시각적 견본 및 텍스트 견본 입력 유형에서 옵션을 선택할 수 있습니다. 각 옵션은 별도의 간단한 제품입니다.

- [재고 상태](../inventory-management/sources-stocks.md) 구성 가능한 제품의 경우 반수동으로 제어되는 설정입니다. 제품 이용가능성을 직접 나타내는 단순한 제품의 재고 상태와는 다르다. 구성 가능한 제품의 경우 재고 상태는 다중 기준 재고 상태 계산의 일부입니다.

- 구성 가능한 하위 제품은 단순 또는 가상 제품일 수 있습니다. **사용자 지정 옵션 없음**. 사용자 지정 하위 제품을 가상화하려면 다음을 선택해야 합니다. `Тhis item has no weight` 대상: **[!UICONTROL Weight]** 각각에 대해 를 설정합니다.

- 제품 변형에 사용되는 특성은 범위가 전역적이어야 하며 고객은 값을 선택해야 합니다. 제품 변형 속성은 구성 가능한 제품의 템플릿으로 사용되는 속성 세트에 포함되어야 합니다.

- 구성 가능한 제품에 대한 템플릿으로 사용되는 속성 세트에는 각 제품 변형에 필요한 값이 포함된 속성이 포함되어야 합니다.

- 장바구니의 썸네일 이미지는 구성 가능한 제품 레코드 또는 제품 변형의 이미지를 표시하도록 설정할 수 있습니다.

- [견본 속성](swatches.md#create-swatches-for-products) 을 설정하여 견본을 선택할 때 해당 단순 제품 이미지를 표시하지 않도록 구성할 수 있습니다. **[!UICONTROL Update Product Preview Image]** 옵션 값: `No` ( 관리자의 속성 편집 페이지 )을 참조하십시오.

- 테마는 사용자가 제품 구성 간을 전환할 때 이미지 갤러리가 작동하는 방식을 제어합니다. 의 기본 비헤이비어 _비어 있음_ 테마는 상위 구성 가능한 제품 이미지를 선택한 제품 변형으로 재정의하는 것입니다. Luma 테마의 경우 기본 동작은 선택한 제품 변형 이미지를 상위 구성 가능한 제품 이미지에 앞에 추가하는 것입니다.
