---
title: 공유 카탈로그에 제품 추가
description: 제품을 공유 카탈로그에 개별적으로 또는 범주별 그룹으로 추가하는 방법에 대해 알아봅니다.
exl-id: c88b46b4-cea8-4f65-b7e4-6681bab64d41
feature: B2B, Companies, Catalog Management
source-git-commit: 01148770946a236ece2122be5a88b963a0f07d1f
workflow-type: tm+mt
source-wordcount: '402'
ht-degree: 0%

---

# 공유 카탈로그에 제품 추가

제품은 개별적으로 또는 카테고리별로 여러 제품 그룹으로 공유 카탈로그에 추가할 수 있습니다.

복잡한 제품(예: 번들, 그룹화 또는 구성 가능)을 공유 카탈로그의 상점 맨 위에 표시하려면 다음 요구 사항을 충족해야 합니다.

- 모든 [관련 제품](../catalog/product-configurations.md) 및 옵션은 동일한 공유 카탈로그에 할당되고 기본 카탈로그에서 활성화되어야 합니다.
- [구성 가능](../catalog/product-create-configurable.md) 및 [그룹화된](../catalog/product-create-grouped.md) 제품의 경우 활성화된 관련 제품만 표시됩니다.
- [번들](../catalog/product-create-bundle.md) 제품의 경우 모든 옵션이 공유 카탈로그에 포함되어야 합니다.

  ![카탈로그에 대한 제품 선택](./assets/shared-catalog-select-products-step-1.png){width="600" zoomable="yes"}

## 방법 1: 단일 제품 추가

1. _관리자_ 사이드바에서 **[!UICONTROL Catalog]** > **[!UICONTROL Products]**(으)로 이동합니다.

1. 추가할 그리드의 제품에 대해 _[!UICONTROL Action]_열로 이동하여&#x200B;**[!UICONTROL Edit]**을(를) 클릭합니다.

1. 아래로 스크롤하여 _[!UICONTROL Product in Shared Catalogs]_섹션에서 ![확장 선택기](../assets/icon-display-expand.png)를 확장하고 다음을 수행합니다.

   - 제품이 표시되어야 하는 각 공유 카탈로그의 확인란을 선택합니다. 모든 카탈로그를 선택하려면 **[!UICONTROL Select all]**&#x200B;을(를) 클릭하십시오.

     공유 카탈로그의 ![제품](./assets/shared-catalog-assign-from-product.png){width="600" zoomable="yes"}

     선택한 각 카탈로그의 이름이 _[!UICONTROL Shared Catalogs]_필드에 나타납니다.

     ![공유된 카탈로그 할당됨](./assets/shared-catalog-assigned.png){width="600" zoomable="yes"}

   - 설정을 저장하려면 **[!UICONTROL Done]**&#x200B;을(를) 클릭합니다.

1. 완료되면 **[!UICONTROL Save]**&#x200B;을(를) 클릭합니다.

## 방법 2: 여러 제품 추가

1. _관리자_ 사이드바에서 **[!UICONTROL Catalog]** > **[!UICONTROL Shared Catalogs]**(으)로 이동합니다.

1. 격자에 있는 공유 카탈로그의 경우 _[!UICONTROL Action]_열로 이동하여&#x200B;**[!UICONTROL Set Pricing and Structure]**을(를) 선택합니다.

1. 범주 트리에서 다음 중 하나를 수행합니다.

   - 모든 제품을 포함하려면 **[!UICONTROL Select all]**&#x200B;을(를) 클릭하거나 상위 범주의 확인란을 선택하십시오.
   - 특정 제품 카테고리를 포함하려면 포함하려는 각 카테고리의 확인란을 선택합니다.
   - 개별 제품을 포함하거나 제외하려면 제품 확인란을 선택하거나 선택 취소합니다.

   트리의 각 카테고리 아래에 있는 표기법에는 현재 공유 카탈로그에 포함된 카테고리의 제품 수가 표시됩니다. [루트 범주](../catalog/category-root.md) 아래의 표기법에는 현재 공유 카탈로그에 대해 선택된 모든 범주의 총 제품 수가 표시됩니다.

1. 그리드에서 카테고리 제품을 보려면 트리에서 카테고리 이름을 클릭합니다.

   카테고리를 선택하면 다음 상황이 발생합니다.

   - 선택한 각 제품에 대해 그리드의 첫 번째 열에 있는 토글이 `On`(으)로 설정됩니다.
   - 제품이 여러 범주에 할당되고 그 중 하나에서 생략되는 경우 다른 범주와 [카탈로그 검색](../catalog/search.md)을 통해 사용할 수 있습니다.
   - 선택한 제품에 대해 [범주 권한](../catalog/category-permissions.md)을(를) `Allow`(으)로 자동 설정합니다.
