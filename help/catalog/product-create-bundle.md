---
title: 번들 제품
description: 쇼핑객이 스토어에서 사용자 지정된 제품을 작성할 수 있는 번들 제품을 만드는 방법을 알아봅니다.
exl-id: dfa31eb8-2330-44eb-889b-5d10ce56ef13
feature: Catalog Management, Products
source-git-commit: ce36104913434bb71115e1a5b497f38f75fbd3c5
workflow-type: tm+mt
source-wordcount: '1603'
ht-degree: 0%

---

# 번들 제품

번들은 사용자 지정 가능한 _자체 제품을 빌드합니다_. 번들의 각 항목은 다음 제품 유형 중 하나를 기반으로 할 수 있습니다.

- [단순 제품](product-create-simple.md)
- [가상 제품](product-create-virtual.md)

![제품 번들](./assets/product-bundle.png){width="700" zoomable="yes"}

고객이 **[!UICONTROL Customize]** 또는 **[!UICONTROL Add to Cart]**&#x200B;을(를) 클릭하면 옵션이 표시됩니다. 번들에 포함된 제품이 다르기 때문에 SKU, 가격 및 중량은 동적 또는 고정 값으로 설정할 수 있습니다.

>[!NOTE]
>
>동적 가격책정을 사용하는 번들 제품에는 MAP(최소 광고 가격)을 사용할 수 없습니다.

>[!NOTE]
>
>상위 번들 제품은 항상 모든 하위 제품에 대한 상향 판매 제품으로 표시됩니다.

[즉시 구매](../stores-purchase/checkout-instant-purchase.md)를 사용할 수 있는 경우 _즉시 구매_ 단추가 번들의 각 항목에 대한 _장바구니에 추가_ 단추 아래에 나타납니다.

![번들 사용자 지정](./assets/product-bundle-customize.png){width="600" zoomable="yes"}

다음 지침은 [제품 템플릿](attribute-sets.md), 필수 필드 및 기본 설정을 사용하여 번들 제품을 만드는 과정을 안내합니다. 각 필수 필드는 빨간색 별표(`*`)로 표시되어 있습니다. 기본 사항을 완료하면 필요에 따라 다른 제품 설정을 완료할 수 있습니다.

## 1단계: 제품 유형 선택

1. _관리자_ 사이드바에서 **[!UICONTROL Catalog]** > **[!UICONTROL Products]**(으)로 이동합니다.

1. _[!UICONTROL Add Product]_( ![메뉴 화살표](../assets/icon-menu-down-arrow-red.png){width="25"}) 메뉴의 오른쪽 상단 모서리에서&#x200B;**[!UICONTROL Bundle Product]**&#x200B;을(를) 선택합니다.

   ![번들 제품 추가](./assets/product-add-bundle.png){width="700" zoomable="yes"}

## 2단계: 속성 세트 선택

제품의 템플릿으로 사용되는 [특성 집합](attribute-sets.md)을 선택하려면 다음 중 하나를 실행하십시오.

- **[!UICONTROL Search]**&#x200B;의 경우 특성 집합의 이름을 입력하십시오.
- 목록에서 사용할 속성 세트를 선택합니다.

양식이 변경 사항을 반영하도록 업데이트됩니다.

![템플릿 선택](./assets/product-create-choose-attribute-set.png){width="600" zoomable="yes"}

## 3단계: 필요한 설정 완료

1. 제품 **[!UICONTROL Product Name]**&#x200B;을(를) 입력하십시오.

1. 제품 이름을 기반으로 하는 기본 **[!UICONTROL SKU]**&#x200B;을(를) 사용하거나 다른 값을 입력하십시오.

   각 번들 항목에 할당된 SKU 유형을 확인하려면 다음을 수행하십시오.

   - 기본 SKU에 접미사를 추가하여 각 번들 항목에 **[!UICONTROL Dynamic SKU]**&#x200B;을(를) 자동으로 할당할 수 있습니다. 기본적으로 `Yes`(으)로 설정됩니다.

   - 각 번들 항목에 대해 고유한 SKU를 할당하려면 **[!UICONTROL Dynamic SKU]**&#x200B;을(를) `No`(으)로 설정하십시오.

   ![동적 SKU 및 가격](./assets/product-bundle-manual-sku.png){width="600" zoomable="yes"}

1. 번들의 가격을 확인하려면 다음 중 하나를 수행하십시오.

   - 가격이 고객이 선택한 옵션을 반영하도록 하려면 **[!UICONTROL Dynamic Price]**&#x200B;을(를) `Yes`(으)로 설정하고 **[!UICONTROL Price]**&#x200B;을(를) 비워 둡니다. 이 경우 묶음 제품은 카탈로그에서 자체 가격이 없으며 제품 가격은 묶음에 포함된 개별 제품의 가격에서 파생됩니다.

   - 번들의 고정 가격을 부과하려면 **[!UICONTROL Dynamic Price]**&#x200B;을(를) `No`(으)로 설정하고 번들에 부과할 **[!UICONTROL Price]**&#x200B;을(를) 입력하십시오.

   >[!NOTE]
   >
   >[!UICONTROL Special Price] 및 [!UICONTROL Customer Group Price] (계층 가격)은 항상 모든 번들 제품 유형에 대한 할인율로 설정됩니다.

1. 제품을 아직 게시할 준비가 되지 않았으므로 **[!UICONTROL Enable Product]**&#x200B;을(를) `No`(으)로 설정하십시오.

1. **[!UICONTROL Save]**&#x200B;을(를) 클릭하고 계속합니다.

   제품을 저장하면 왼쪽 위 모서리에 [스토어 보기](introduction.md#product-scope) 선택기가 나타납니다.

1. 제품을 사용할 수 있는 **[!UICONTROL Store View]**&#x200B;을(를) 선택하십시오.

   ![스토어 보기 선택](./assets/product-create-store-view-choose.png){width="600" zoomable="yes"}

## 4단계: 기본 설정 완료

1. 번들에 고정 가격이 있는 경우 **[!UICONTROL Tax Class]**&#x200B;을(를) 다음 중 하나로 설정하십시오.

   - `None`
   - `Taxable Goods`

   번들에 동적 가격책정이 있는 경우 세금은 **_각_** 번들 항목에 대해 결정됩니다. 번들에 고정 가격이 있는 경우 세금은 **_whole_** 번들 제품에 대해 결정됩니다.

1. 다음 사항에 주의하십시오.

   - 각 번들 항목에 대해 값이 결정되므로 **[!UICONTROL Quantity]**&#x200B;을(를) 사용할 수 없습니다.

   - 기본적으로 **[!UICONTROL Stock Status]**&#x200B;은(는) `In Stock`(으)로 설정됩니다.

1. 번들의 무게를 확인하려면 다음 중 하나를 수행하십시오.

   - 가중치가 고객이 선택한 옵션을 반영하도록 하려면 **[!UICONTROL Dynamic Weight]**&#x200B;을(를) 설정하여 `Yes`을(를) 설정하고 **[!UICONTROL Weight]**&#x200B;을(를) 비워 둡니다.

   - 고정 가중치를 번들에 할당하려면 **[!UICONTROL Dynamic Weight]**&#x200B;을(를) `No`(으)로 설정하고 번들의 **[!UICONTROL Weight]**&#x200B;을(를) 입력하십시오.

   ![동적 가중치](./assets/product-bundle-dynamic-weight.png){width="600" zoomable="yes"}

1. [새 제품](../content-design/widget-new-products-list.md) 목록에 제품을 포함하려면 **[!UICONTROL Set Product as New]** 확인란을 선택하십시오.

1. `Catalog, Search`의 기본 **[!UICONTROL Visibility]** 설정을 사용합니다.

1. 제품에 _[!UICONTROL Categories]_&#x200B;을(를) 할당하려면&#x200B;**[!UICONTROL Select…]**&#x200B;상자를 클릭하고 다음 중 하나를 수행합니다.

   **기존 범주 선택:**

   - 일치하는 항목을 찾을 때까지 상자에 입력을 시작합니다.

   - 할당할 각 범주의 확인란을 선택합니다.

   ![번들 제품에 대해 하나 이상의 범주를 선택하십시오](./assets/product-create-categories.png){width="600" zoomable="yes"}

   **범주 만들기:**

   - **[!UICONTROL New Category]**&#x200B;을(를) 클릭합니다.

   - **[!UICONTROL Category Name]**&#x200B;을(를) 입력하고 메뉴 구조에서 위치를 결정하는 **[!UICONTROL Parent Category]**&#x200B;을(를) 선택합니다.

   - **[!UICONTROL Create Category]**&#x200B;을(를) 클릭합니다.

1. **[!UICONTROL Country of Manufacture]** 선택.

   제품을 설명하는 추가 속성이 있을 수 있습니다. 선택 내용은 속성 집합에 따라 달라지므로 나중에 완료할 수 있습니다.

## 5단계: 번들 항목 추가

_[!UICONTROL Bundle Items]_&#x200B;섹션은 번들 제품 형식에 항목을 추가하고 현재 선택한 항목을 편집하는 데 사용됩니다.

![제품에 대해 정의된 번들 항목](./assets/product-bundle-items-ball.png){width="600" zoomable="yes"}

1. _번들 항목_ 섹션까지 아래로 스크롤하고 **[!UICONTROL Ship Bundle Items]**&#x200B;을(를) 다음 중 하나로 설정합니다.

   - `Separately`
   - `Together`

   `Together`을(를) 선택하는 경우 모든 번들 항목에 동일한 [소스](../inventory-management/sources-manage.md)를 할당해야 합니다.

1. **[!UICONTROL Add Option]**&#x200B;을(를) 클릭하고 다음을 수행합니다.

   - 필드 레이블로 사용할 **[!UICONTROL Option Title]**&#x200B;을(를) 입력하십시오.

   - **[!UICONTROL Input Type]**&#x200B;을(를) 다음 중 하나로 설정합니다.

      - `Drop-down`
      - `Radio buttons`
      - `Checkbox`
      - `Multiple Select`

   - 필드를 필수 항목으로 만들려면 **[!UICONTROL Required]** 확인란을 선택하십시오.

   - **[!UICONTROL Add Products to Option]**&#x200B;을(를) 클릭하고 이 옵션에 포함할 각 제품의 확인란을 선택합니다.

     제품이 많으면 목록 필터 및 페이지 매김 컨트롤을 사용하여 필요한 제품을 찾습니다.

   - **[!UICONTROL Add Selected Products]**&#x200B;을(를) 클릭합니다.

     ![선택한 제품 추가](./assets/product-bundle-add-products-to-option.png){width="600" zoomable="yes"}

   - 항목이 _옵션_ 섹션에 나타나면 항목을 **[!UICONTROL Default]** 선택 항목으로 선택하십시오.

   - _기본 수량_ 열에 고객이 항목을 선택할 때 번들에 추가할 각 항목의 수량을 입력합니다.

   - 고객이 번들 항목의 수량을 변경할 수 있도록 하려면 **[!UICONTROL User Defined]**&#x200B;을(를) 선택합니다.


     >[!NOTE]
     >
     >수량은 사전 설정 또는 사용자 정의 값일 수 있습니다. 그러나 _[!UICONTROL User Defined]_&#x200B;속성은 확인란 또는 다중 선택 입력 유형에 할당하지 마십시오.

     기본적으로 번들 항목에 포함된 기본 수량은 고객이 변경할 수 없습니다. 단, 번들에 포함될 품목의 수량을 고객이 입력할 수 있다.

     예를 들어 Sprite 상태 공의 기본 수량이 `2`이고 고객이 해당 번들 옵션의 `4`을(를) 주문하는 경우 총 구매한 공의 총 수는 `8`입니다.

     ![항목 세부 정보](./assets/product-bundle-item-detail.png){width="600" zoomable="yes"}

1. 번들에 추가할 각 항목에 대해 이 단계를 반복합니다.

1. 번들 섹션의 항목 순서를 변경하려면 행의 시작 부분에 있는 _이동_( ![이동 아이콘](../assets/icon-move.png)) 아이콘을 클릭하고 항목을 위치로 끕니다.

   ![번들 항목의 순서 변경](./assets/product-bundle-items-move.png){width="600" zoomable="yes"}

   항목 순서는 내보낸 번들 제품의 데이터에서 변경한 다음 카탈로그로 다시 가져올 수도 있습니다. 자세한 내용은 [번들 제품 가져오기](../systems/data-transfer-bundle-products.md)를 참조하십시오.

   작업 영역을 더 잘 보려면 먼저 각 섹션을 축소한 다음 위치로 드래그합니다.

1. 번들에서 항목을 제거하려면 **[!UICONTROL Delete]** ( ![휴지통 아이콘](../assets/icon-delete-trashcan.png) ) 아이콘을 클릭하십시오.

1. 완료되면 **[!UICONTROL Save]**&#x200B;을(를) 클릭합니다.

## 6단계: 제품 정보 작성

아래로 스크롤하여 필요에 따라 다음 섹션의 정보를 작성합니다.

- [콘텐츠](product-content.md)
- [이미지 및 비디오](product-images-and-video.md)
- [검색 엔진 최적화](product-search-engine-optimization.md)
- [관련 제품, 상향 판매 및 교차 판매](related-products-up-sells-cross-sells.md)
- [사용자 정의 가능한 옵션](settings-advanced-custom-options.md)
- [웹 사이트의 제품](settings-basic-websites.md)
- [디자인](settings-advanced-design.md)
- [선물 옵션](product-gift-options.md)

## 7단계: 제품 Publish

1. 제품을 카탈로그에 게시할 준비가 되면 **[!UICONTROL Enable Product]**&#x200B;을(를) `Yes`(으)로 설정합니다(![예 전환](../assets/toggle-yes.png)).

1. 다음 중 하나를 수행합니다.

   **메서드 1:** 저장 및 미리 보기

   - 오른쪽 상단에서 **[!UICONTROL Save]**&#x200B;을(를) 클릭합니다.

   - 스토어에서 제품을 보려면 _관리자_( ![메뉴 화살표](../assets/icon-menu-down-arrow-black.png)) 메뉴에서 **[!UICONTROL Customer View]**&#x200B;을(를) 선택하십시오.

     저장소가 새 브라우저 탭에서 열립니다.

   ![고객 보기](./assets/product-admin-customer-view.png){width="600" zoomable="yes"}

   **메서드 2:** 저장 및 닫기

   _[!UICONTROL Save]_( ![메뉴 화살표](../assets/icon-menu-down-arrow-red.png){width="25"}) 메뉴에서&#x200B;**[!UICONTROL Save & Close]**&#x200B;을(를) 선택합니다.

## 입력 컨트롤

| 제어 | 설명 | 예 |
|--- |--- |--- |
| [!UICONTROL Drop-down] | 제품 이름과 가격이 포함된 옵션의 드롭다운 목록을 표시합니다. 항목은 하나만 선택할 수 있습니다. | ![드롭다운](./assets/product-bundle-input-type-drop-down.png){width="200"} |
| [!UICONTROL Radio Buttons] | 각 옵션에 대한 라디오 단추를 표시한 다음 제품 이름과 가격을 표시합니다. 항목은 하나만 선택할 수 있습니다. | ![라디오 단추](./assets/product-bundle-input-type-radio-buttons.png){width="200"} |
| [!UICONTROL Checkbox] | 각 옵션에 대한 확인란과 함께 제품 이름과 가격을 표시합니다. 여러 항목을 선택할 수 있습니다. | ![확인란](./assets/product-bundle-input-type-checkbox.png){width="200"} |
| [!UICONTROL Multiple Select] | 제품 이름과 가격이 포함된 옵션 목록을 표시합니다. 여러 항목을 선택하려면 Ctrl 키(PC) 또는 Command 키(Mac)를 누른 채 각 항목을 클릭합니다. | ![다중 선택](./assets/product-bundle-input-type-multiple-select.png){width="200"} |

{style="table-layout:auto"}

## 필드 설명

| 필드 | 설명 |
|--- |--- |
| [!UICONTROL SKU] | 각 항목에 변수 또는 동적 SKU가 할당되었는지 또는 번들에 고정 SKU가 사용되는지를 결정합니다. 옵션: `Fixed` / `Dynamic` |
| [!UICONTROL Weight] | 선택한 항목을 기반으로 가중치를 계산할지 또는 전체 번들에 대해 고정된 가중치인지 지정합니다. 옵션: `Fixed` / `Dynamic` |
| [!UICONTROL Price View] | 제품 가격이 최저 가격대에서 최고 가격대(가격 범위)까지 또는 최저 가격대(최저 가격)까지 범위로 표시되는지 여부를 결정합니다. 옵션: `Price Range` / `As Low As` |
| 번들 항목 배송 | 개별 품목을 별도로 출하할 수 있는지 여부를 지정합니다. |

{style="table-layout:auto"}

## 번들 제품 재고 상태

다음 시나리오 중 하나가 발생할 때 번들 제품 재고 상태가 **_자동으로 [재고 부족]으로 변경됨_**:

- 모든 옵션은 선택 사항이며 연결된 모든 제품은 _품절_&#x200B;입니다.

- 일부 옵션이 필요하며 필요한 옵션과 연결된 제품은 _재고 부족_&#x200B;입니다.

다음 시나리오 중 하나가 발생할 때 번들 제품 스톡 상태가 **_자동으로 [재고 부족]으로 변경되지 않음_**&#x200B;입니다.

- 모든 옵션은 선택 사항이며 연결된 제품 중 하나 이상이 _재고_&#x200B;입니다.

- 일부 옵션이 필요하며 각 필수 옵션의 하나 이상의 연결된 제품은 _재고_&#x200B;입니다.

## 기억해야 할 사항

![확인란](../assets/checkbox.png) 고객은 제품을 _직접 작성_&#x200B;할 수 있습니다.

![확인란](../assets/checkbox.png) 모든 하위 제품은 모든 웹 사이트, 스토어 및 스토어 보기에 대해 번들 제품 **_전역적으로_**&#x200B;에서 동시에 할당되거나 할당이 해제됩니다.

![Checkbox](../assets/checkbox.png) 번들 항목은 사용자 지정 옵션이 없는 단순 또는 가상 제품일 수 있습니다.

![확인란](../assets/checkbox.png) 가격 보기는 `Price Range` 또는 `As Low As` 중 하나로 설정할 수 있습니다.

![확인란](../assets/checkbox.png) SKU 및 가중치는 `Fixed` 또는 `Dynamic`일 수 있습니다.

![확인란](../assets/checkbox.png) 수량은 사전 설정 또는 사용자 정의 값일 수 있습니다. 그러나 _[!UICONTROL User Defined]_&#x200B;속성은 확인란 또는 다중 선택 입력 유형에 할당하지 마십시오.

![Checkbox](../assets/checkbox.png) 번들 항목은 함께 또는 별도로 배달할 수 있습니다.

![확인란](../assets/checkbox.png) 상위 번들 제품은 항상 모든 하위 제품에 대해 상향 판매 제품으로 표시됩니다.

![확인란](../assets/checkbox.png) [!UICONTROL Special Price] 및 [!UICONTROL Customer Group Price] (계층 가격)은 항상 모든 번들 제품 유형의 할인율로 설정됩니다.
