---
title: 루트 범주 및 계층
description: 범주 계층 구조 및 범주 트리에서 주 메뉴의 컨테이너 역할을 하는 루트 범주에 대해 알아봅니다.
exl-id: b419cb45-4fe5-42c4-be20-667c7e1e4354
feature: Catalog Management, Categories, Site Navigation
source-git-commit: 01148770946a236ece2122be5a88b963a0f07d1f
workflow-type: tm+mt
source-wordcount: '436'
ht-degree: 0%

---

# 루트 범주 및 계층

기본 메뉴의 제품은 [store](../stores-purchase/stores.md#add-stores)에 할당된 루트 범주에 따라 결정됩니다. 루트 카테고리는 기본적으로 카테고리 트리의 메인 메뉴에 대한 컨테이너입니다. 완전히 새로운 제품 세트로 루트 카테고리를 만들거나 기존 루트 카테고리에서 제품을 복사할 수 있습니다. 루트 카테고리를 현재 스토어 또는 동일한 웹 사이트의 다른 스토어에 할당할 수 있습니다.

![카탈로그 계층 다이어그램](./assets/catalog-hierarchy-scope.svg){width="550"}

관리자의 경우, 범주 구조는 루트가 위에 있는 거꾸로 된 트리와 같습니다. 루트에 이름이 있지만 URL 키가 없으며 스토어의 [위쪽 탐색](navigation-top.md)에 나타나지 않습니다. 메뉴의 다른 모든 범주는 루트 아래에 중첩됩니다. 루트 카테고리는 카탈로그의 최상위 수준이므로 스토어는 한 번에 하나의 루트 카테고리만 활성화할 수 있습니다. 그러나 대체 카탈로그 구조 및 다른 저장소에 대한 추가 루트 범주를 만들 수 있습니다.

다음 예에서는 루트 카테고리를 만들어 다른 스토어에 할당하는 방법을 보여 줍니다.

## 1단계: 루트 범주 만들기

1. _관리자_ 사이드바에서 **[!UICONTROL Catalog]** > **[!UICONTROL Categories]**(으)로 이동합니다.

1. 왼쪽에서 **[!UICONTROL Add Root Category]**&#x200B;을(를) 클릭합니다.

   ![새 루트 범주](./assets/category-root-ee.png){width="600" zoomable="yes"}

1. **[!UICONTROL Category Name]** 입력.

   선택한 이름은 처음에는 모든 스토어 보기에 할당됩니다.

1. 현재 카탈로그에서 제품을 카탈로그에 추가하려면 다음을 수행합니다.

   - _범주의 제품_ 섹션에서 ![확장 선택기](../assets/icon-display-expand.png)를 확장합니다.

   - [검색 필터](../getting-started/admin-grid-controls.md)를 사용하여 원하는 제품을 찾은 다음 새 카탈로그로 복사할 각 제품에 대한 확인란을 선택하십시오.

1. 완료되면 **[!UICONTROL Save]**&#x200B;을(를) 클릭합니다.

## 2단계: 기본 메뉴 빌드

1. 왼쪽에서는 이전 단계에서 만든 새 루트 카테고리를 선택합니다.

1. 주 메뉴에 대한 [카테고리 구조](category-create.md)를 만들려면 **[!UICONTROL Add Subcategory]**&#x200B;을(를) 클릭하고 지침을 따르십시오.

## 3단계: 저장소에 루트 범주 할당

1. _관리자_ 사이드바에서 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL All Stores]**(으)로 이동합니다.

1. 그리드의 _스토어_ 열에서 새 카탈로그를 할당할 스토어를 클릭합니다.

1. **[!UICONTROL Root Category]**&#x200B;을(를) 만든 새 루트 범주로 설정합니다.

1. 저장소에 **[!UICONTROL Default Store View]**&#x200B;이(가) 할당되어 있는지 확인하십시오.

   스토어에 하나 이상의 [스토어 보기](../stores-purchase/store-views.md)가 있어야 합니다.

1. 완료되면 **[!UICONTROL Save Store]**&#x200B;을(를) 클릭합니다.

1. 저장소에 새 카탈로그가 있는지 확인하려면 다음을 수행하십시오.

   - _관리자_ 사이드바에서 **[!UICONTROL Catalog]** > **[!UICONTROL Products]**(으)로 이동합니다.

     새 카탈로그에 복사된 모든 제품이 그리드에 나타납니다.

   - 새 카탈로그와 메인 메뉴가 올바르게 작동하는지 확인하려면 상점 전면을 방문하십시오.
