---
title: 범주 제품 할당
description: 사용에 대해 알아보기 [!UICONTROL Products in Category] 현재 범주에 할당된 제품을 제어하는 설정입니다.
exl-id: e7ab11c0-2d55-4824-a397-a1c858344d4f
feature: Catalog Management, Categories, Products
source-git-commit: 01148770946a236ece2122be5a88b963a0f07d1f
workflow-type: tm+mt
source-wordcount: '809'
ht-degree: 0%

---

# 범주 제품 할당

범주의 경우 _[!UICONTROL Products in Category]_섹션에 카테고리에 현재 지정된 제품을 검토할 수 있습니다. 각 열의 맨 위에 있는 검색 필터는 카테고리에서 제품을 추가하거나 제거하는 데 사용됩니다. 다음을 사용할 수도 있습니다. [범주 규칙](../merchandising-promotions/category-product-rules.md) ( ![Adobe Commerce](../assets/adobe-logo.svg) Adobe Commerce만 해당) 를 사용하여 조건 세트가 충족될 때 제품 선택을 동적으로 변경할 수 있습니다. 자세한 내용은 다음을 참조하십시오. [Visual Merchandiser](../merchandising-promotions/visual-merchandiser.md)).

>[!TIP]
>
>범주 규칙을 설정하는 동안 제품은 다음과 같습니다. _정렬됨_, _일치함_, _할당됨_, 및 _할당 해제됨_ 그 규칙에 따르면 **_전용_** 이 범주가 저장되면 새 제품을 카탈로그에 추가할 때 규칙에 따라 할당되도록 하려면 **각 범주를 다시 저장해야 함** 는 규칙에 따라 제품과 일치하도록 설정되었습니다. 또한 제품 재고 상태가 (으)로 변경된 경우 `In Stock` 또는 `Out of Stock` 및 카테고리의 제품은 다음과 같습니다 _정렬됨_ 에 따라 **자동 정렬** 규칙, 다음을 클릭해야 합니다. **[!UICONTROL Save Category]**.

![범주 제품](./assets/category-products-in-category.png){width="600" zoomable="yes"}

>[!NOTE]
>
>카테고리 페이지에서 `Out of stock` 제품은 항상 표시됩니다. **_이후_** `In Stock` 모든 정렬 유형이 포함된 제품 목록.

>[!NOTE]
>
>다음 _재고_ 열에는 다음에 대한 판매 가능한 제품 수량이 표시됩니다. _**선택한 범주 범위**_ 만 해당. 제품에 대해 여러 재고를 관리하는 경우 해당 범위 간에 전환하여 다른 범위를 표시해야 합니다 _재고_ 의 열 값 _범주 제품_ 그리드.

## 범주 규칙 적용

{{ee-feature}}

1. 설정 **[!UICONTROL Match products by rule]** 끝 `Yes`.

   자동 정렬 및 조건 옵션이 나타납니다.

   ![규칙별로 제품 일치시키기](./assets/category-match-products-by-rule.png){width="600" zoomable="yes"}

1. 설정 **[!UICONTROL Automatic Sorting]** 주문.

   이 자동 정렬은 현재 상태를 기반으로 합니다.

   - `Stock level` - 위쪽 또는 아래쪽으로 이동합니다.
   - `Special price` - 위쪽 또는 아래쪽으로 이동합니다.
   - `New Products` - 최신 제품을 먼저 나열합니다.
   - `Color` - 색상별로 알파벳순으로 정렬합니다.
   - `Name` - 이름별로 오름차순 또는 내림차순으로 정렬합니다.
   - `SKU` - SKU별로 오름차순 또는 내림차순으로 정렬
   - `Price` - 가격을 기준으로 오름차순 또는 내림차순으로 정렬합니다.

1. 클릭 **[!UICONTROL Add Condition]** 다음을 수행합니다.

   - 다음을 선택합니다. **[!UICONTROL Attribute]** 그것이 그 조건의 기초이다.
   - 다음을 선택합니다. **[!UICONTROL Operator]** 표현식을 구성하는 데 필요합니다.
   - 다음을 입력합니다. **[!UICONTROL Value]** 일치시킬 수 있습니다.

   ![범주 규칙에 조건 추가](./assets/category-rule-create.png){width="600" zoomable="yes"}

   충족될 조건을 설명하는 데 사용할 각 속성에 대해 이 프로세스를 반복합니다. 예를 들어 7일에서 30일 전에 만든 제품을 일치시키려면 다음을 수행합니다.

   - 설정 **[!UICONTROL Date Created]** 끝 `Less than 30`.
   - 설정 **[!UICONTROL Logic]** 끝 `AND`.
   - 설정 **[!UICONTROL Date Modified]** 끝 `Greater than 7`.

1. 완료되면 다음을 클릭하십시오. **[!UICONTROL Save Category]**.

### 페이지 옵션

| 옵션 | 설명 |
|--- |--- |
| [!UICONTROL Match products by rule] | 카테고리의 제품 목록이 카테고리 규칙에 의해 동적으로 생성되는지 여부를 결정합니다. 옵션: `Yes` / `No` |
| [!UICONTROL Automatic Sorting] | 범주 제품 목록에 정렬 순서를 자동으로 적용합니다. 옵션: <br/>`None`<br/>`Move low stock to top`<br/>`Move low stock to bottom`<br/>`Special price to top`<br/>`Special price to bottom`<br/>`Newest products first`<br/>`Sort by color`<br/>`Name: A - Z`<br/>`Name: Z - A`<br/>`SKU: Ascending`<br/>`SKU: Descending`<br/>`Price: High to Low`<br/>`Price: Low to High` |
| [!UICONTROL Add Condition] | 규칙에 다른 조건을 추가합니다. |

{style="table-layout:auto"}

### 페이지 조건

| 옵션 | 설명 |
|--- |--- |
| [!UICONTROL Attribute] | 조건의 기반으로 사용되는 속성을 결정합니다. 옵션: <br/>**[!UICONTROL Clone Category ID(s)]**- 분류 및 순서 없이 범주 ID를 기준으로 여러 범주의 제품을 동적으로 복제합니다.<br/>**[!UICONTROL Color]** - 색상을 기반으로 하는 제품을 포함합니다. <br/>**[!UICONTROL Date Created (days ago)]**- 제품이 카탈로그에 추가된 이후 일 수를 기준으로 제품을 포함합니다.<br/>**[!UICONTROL Date Modified (days ago)]** - 제품을 마지막으로 수정한 이후 일 수를 기반으로 하는 제품을 포함합니다. <br/>**[!UICONTROL Name]**- 제품 이름을 기반으로 하는 제품을 포함합니다.<br/>**[!UICONTROL Price]** - 가격을 기준으로 하는 제품이 포함됩니다. <br/>**[!UICONTROL Quantity]**- 재고 수량을 기반으로 하는 제품을 포함합니다.<br/>** SKU **- SKU를 기반으로 하는 제품을 포함합니다. |
| [!UICONTROL Operator] | 조건을 충족하기 위해 속성 값에 적용되는 연산자를 지정합니다. 연산자를 지정하지 않으면 `Equal` 는 기본값으로 사용됩니다. 옵션: `Equal` / `Not equal` / `Greater than` / `Greater than or equal to` / `Less than` / `Less than or equal to` / `Contains` |
| [!UICONTROL Value] | 조건을 충족하기 위해 특성이 가져야 하는 값을 지정합니다. |
| [!UICONTROL Logic] | 여러 조건을 정의하는 데 사용되며 다른 조건이 추가될 때만 나타납니다. 옵션: `OR` / `AND` |

{style="table-layout:auto"}

>[!NOTE]
>
>하위 옵션이 있는 구성 가능한 제품의 수량은 모든 판매 가능한 하위 제품 수량을 결합하여 계산됩니다. 구성 가능한 제품의 예를 생각해 보십시오. _지구력 운동 탱크_ 자주색, 빨간색 및 노란색 옵션이 있으며 각 색상의 수량이 다릅니다. 이 시나리오에서 상위 제품 수량은 자주색, 빨간색 및 노란색 하위 제품의 판매 가능 수량을 합한 것입니다.

## 컨트롤


## 페이지 컨트롤

{{ee-feature}}

| 제어 | 설명 |
|----------|--------------|
| ![목록으로 보기](../assets/icon-view-list.png) | 목록으로 보기 |
| ![타일로 보기](../assets/icon-view-tiles.png) | 타일로 보기 |
| ![아니요 전환](../assets/toggle-no.png) | 규칙별 일치 - 아니요 |
| ![예 전환](../assets/toggle-yes.png) | 규칙별 일치 - 예 |
| ![컨트롤러 이동](../assets/icon-move.png) | 드래그 앤 드롭 컨트롤을 사용하면 제품을 가져와서 그리드의 현재 페이지에서 다른 위치로 이동할 수 있습니다. 자세한 내용은 다음을 참조하십시오. [Visual Merchandiser](../merchandising-promotions/visual-merchandiser.md). |
| ![위치 컨트롤러](../assets/control-position.png) | 목록에서 제품의 위치를 결정합니다. |

{style="table-layout:auto"}

## 페이지 컨트롤

{{ce-feature}}

| 제어 | 설명 |
|----------|--------------|
| ![선택 확인란](../assets/checkbox-selected.png) | 모든 제품을 선택하거나 모든 선택 항목을 지우려면 첫 번째 열의 헤더에 있는 확인란을 사용합니다. 첫 번째 행의 컨트롤은 검색 유형을 결정하며 모든 레코드를 포함하거나 범주에 할당되거나 할당되지 않은 레코드만 포함하도록 설정할 수 있습니다. 각 행의 첫 번째 열에 있는 확인란은 범주에 추가될 제품을 식별합니다. 옵션: `Yes` / `No` / `Any` |
| [!UICONTROL Search Filters] | 각 열의 맨 위에 있는 필터 컨트롤은 모두 선택 설정에 따라 목록에서 포함하거나 생략하려는 특정 값을 입력하는 데 사용할 수 있습니다. |
| [!UICONTROL Reset Filter] | 모든 검색 필터를 지웁니다. |
| [!UICONTROL Search] | 필터 조건을 기반으로 카탈로그를 검색하고 결과를 표시합니다. |

{style="table-layout:auto"}
