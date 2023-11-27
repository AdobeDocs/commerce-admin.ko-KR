---
title: 범주 제품 정렬
description: 카테고리에서 제품의 위치를 수동으로 또는 사전 정의된 정렬 순서를 적용하여 정의하는 방법에 대해 알아봅니다.
exl-id: 09c66a5d-57d4-4e78-a8d8-e3047c1bd35a
feature: Catalog Management, Categories, Products
source-git-commit: 14c3eb7d54776382bfa196efdac446d42c8dc940
workflow-type: tm+mt
source-wordcount: '433'
ht-degree: 0%

---

# 범주 제품 정렬

{{ee-feature}}

제품을 위치로 끌어다 놓거나 사전 정의된 정렬 순서를 적용하여 범주의 제품 위치를 수동으로 지정할 수 있습니다. 기본적으로 제품은 재고 수준, 연령, 색상, 이름, SKU 및 가격으로 정렬할 수 있습니다. 자동 정렬은 현재 정렬 순서를 무시하고 수동으로 설정된 모든 드래그 앤 드롭 위치를 재설정합니다. 목록에 포함될 제품에 필요한 색상 정렬 순서 및 최소 재고 수준이 다음에서 설정됩니다. [Visual Merchandiser](../configuration-reference/catalog/visual-merchandiser.md) 구성.

>[!NOTE]
>
>카테고리 페이지에서 `Out of stock` 제품은 항상 표시됩니다. **_이후_** `In Stock` 모든 정렬 유형이 포함된 제품 목록.

각 항목에 대해 별도로 카테고리 옵션을 설정할 수 있습니다 [스토어 뷰](../stores-purchase/stores.md#add-stores) 을 사용하여 제품, 목록의 상대 위치 및 범주 규칙에 사용할 수 있는 속성을 결정합니다. 하지만 싱글룸이 있는데 **_글로벌_** 카탈로그의 정렬 순서 및 제품 위치이며, 모두 공유됩니다. [스토어 조회수](../stores-purchase/store-views.md), 스토어 및 웹 사이트

## 1단계: 구성 범위 설정

1. 다음에서 _관리자_ 사이드바, 이동 **[!UICONTROL Catalog]** > **[!UICONTROL Categories]**.

1. 필요한 경우 **[!UICONTROL Store View]** 설정이 적용되는 위치.

   다중 스토어 설치의 경우 _[!UICONTROL Store View]_이 설정을 지정하면 스토어 내에서 사용 가능한 모든 보기에 정렬 순서가 적용됩니다.

1. 왼쪽의 범주 트리에서 편집할 범주를 선택합니다.

   ![범주 트리](./assets/category-selected.png){width="700" zoomable="yes"}

## 2단계: 제품 정렬

>[!NOTE]
>
>제품 특성별로 카테고리를 정렬하면 동일한 속성 값을 갖는 제품도 제품별로 정렬됩니다 _[!UICONTROL Product ID]_오름차순으로 정렬합니다.

다음에서 _[!UICONTROL Products in Category]_섹션에서 타일( ![타일 보기](../assets/icon-view-tiles.png) ) 아이콘 - 제품 타일을 격자에 표시합니다. 제품을 정렬하려면 수동 또는 자동 방법을 사용합니다.

![제품 타일](./assets/category-products-tiles.png){width="600" zoomable="yes"}

### 방법 1: 수동 정렬

1. 설정 **[!UICONTROL Sort Order]** 원하는 대로 사용하십시오.

   ![정렬 순서](./assets/category-edit-sort-order.png){width="600" zoomable="yes"}

1. 새 정렬 순서를 적용하려면 **[!UICONTROL Sort]**.

1. 정렬 순서를 저장하려면 **[!UICONTROL Save Category]**.

1. 메시지가 표시되면 잘못된 인덱서를 업데이트합니다.

### 방법 2: 자동 정렬

1. 설정 **[!UICONTROL Match products by rule]** (![예 전환](../assets/toggle-yes.png)) 받는 사람 `Yes`.


1. 설정 **[!UICONTROL Automatic Sorting]** 원하는 대로 사용하십시오.

1. 카테고리 규칙을 만들려면 다음 단계의 지침을 따릅니다.

## 3단계: 범주 규칙 만들기

1. 설정 **[!UICONTROL Match products by rule]** (![예 전환](../assets/toggle-yes.png)) 받는 사람 `Yes`.

1. 클릭 **[!UICONTROL Add Condition]**.

1. 다음을 선택합니다. **[!UICONTROL Attribute]** 그것이 그 조건의 기초이다.

1. 설정 **[!UICONTROL Operator]** 다음 중 하나를 수행합니다.

   - `Equal`
   - `Not equal`
   - `Greater than`
   - `Greater than or equal to`
   - `Less than`
   - `Less than or equal to`
   - `Contains`

1. 적절한 항목 입력 **[!UICONTROL Value]**.

   ![범주 조건](./assets/category-rule-create.png){width="600" zoomable="yes"}

1. 다른 조건을 추가하려면 **[!UICONTROL Add Condition]** 이 과정을 반복합니다.

## 4단계: 저장, 새로 고침 및 확인

1. 완료되면 다음을 클릭하십시오. **[!UICONTROL Save Category]**.

1. 캐시를 새로 고치라는 메시지가 나타나면 **[!UICONTROL Cache Management]** 각 잘못된 캐시를 새로 고칩니다.

1. 상점 첫 화면에서 제품 선택, 정렬 및 카테고리 규칙이 올바르게 작동하는지 확인합니다.

   조정해야 하는 경우 설정을 변경하고 다시 시도하십시오.
