---
title: 여러 SKU가 있는 카탈로그 가격 규칙
description: 단일 카탈로그 가격 규칙을 여러 SKU에 적용하는 방법을 알아봅니다.
exl-id: 99023460-0501-45cd-8990-5f2b9ed7b4a2
feature: Merchandising, Price Rules, Catalog Management
source-git-commit: 01148770946a236ece2122be5a88b963a0f07d1f
workflow-type: tm+mt
source-wordcount: '365'
ht-degree: 0%

---

# 여러 SKU가 있는 카탈로그 가격 규칙

단일 카탈로그 가격 규칙을 여러 SKU에 적용할 수 있으므로 제품, 브랜드 또는 카테고리를 기반으로 다양한 프로모션을 만들 수 있습니다. 이 규칙을 만들 때 선택한 SKU와 일치하는 조건을 설정해야 합니다. 규칙을 작성할 때 그리드에서 SKU를 쉽게 검색하고 선택할 수 있습니다.

## 1단계. 제품 특성의 Storefront 속성 확인

시작하기 전에 [Storefront 속성](../catalog/attribute-product-create.md#step-4-describe-the-storefront-properties) / `sku` 속성이 로 설정되어 있습니다. `Use in Promo Rules`.

1. 다음에서 _관리자_ 사이드바, 이동 **[!UICONTROL Stores]** > _[!UICONTROL Attributes]_>**[!UICONTROL Product]**.

1. 검색 필터 내 _[!UICONTROL Attribute Code]_열, 입력 `sku` 및 클릭&#x200B;**[!UICONTROL Search]**.

1. 클릭하여 열기 `sku` 속성(편집 모드)입니다.

1. 왼쪽 패널에서 **[!UICONTROL Storefront Properties]** 및 다음을 확인합니다 **[!UICONTROL Use for Promo Rule Conditions]** 이(가) (으)로 설정됨 `Yes`.

1. 속성 값을 변경한 경우 **[!UICONTROL Save Attribute]**.

## 2단계. 여러 SKU에 가격 규칙 적용

1. 다음에서 _관리자_ 사이드바, 이동 **[!UICONTROL Marketing]** > _[!UICONTROL Promotions]_>**[!UICONTROL Catalog Price Rules]**.

1. 다음 중 하나를 수행합니다.

   - 지침에 따라 [카탈로그 가격 규칙](price-rules-catalog.md).
   - 기존 카탈로그 가격 규칙을 엽니다.

1. 확장 ![확장 선택기](../assets/icon-display-expand.png) 다음 **[!UICONTROL Conditions]** 섹션을 참조하고 다음을 수행합니다.

   - 첫 번째 행에서 첫 번째 매개변수를 로 설정합니다. `ANY`.

     ![카탈로그 가격 규칙 조건 - 임의](./assets/multiple-skus-condition1.png){width="600" zoomable="yes"}

   - 클릭 _추가_ (![추가 아이콘](../assets/icon-add-green-circle.png))를 클릭하여 제품에서 사용할 수 있습니다 **[!UICONTROL Product Attribute]**, 클릭 `SKU`.

     ![카탈로그 가격 규칙 조건 - SKU는 다음 중 하나입니다](./assets/multiple-skus-condition1a.png){width="600" zoomable="yes"}

   - 비교를 위해 옵션을 사용할 수 있습니다. SKU 목록에서 하나 이상을 찾으려면 `select is one of`. 모두 해당해야 하는 SKU 그룹을 찾으려면 을 선택합니다. `is`. 을(를) 선택하는 것이 좋습니다 `is one of`.

     ![카탈로그 가격 규칙 조건 - SKU는 다음 중 하나입니다](./assets/multiple-skus-condition1b.png){width="600" zoomable="yes"}

   - 조건을 완료하려면 자세히(**...**) 링크를 클릭하고 _선택기_ (![목록 아이콘](../assets/icon-list-chooser.png)) 아이콘으로 표시됩니다.

     ![카탈로그 가격 규칙 조건 - 여러 SKU](./assets/multiple-skus-condition2b.png){width="600" zoomable="yes"}

   - 추가할 SKU를 검색, 필터링 또는 검색하여 찾습니다. 목록에서 포함할 각 제품의 확인란을 선택합니다.

   - 클릭 **[!UICONTROL Save and Apply]** 조건에 SKU를 추가합니다.

     ![카탈로그 가격 규칙 조건 - 여러 SKU](./assets/multiple-skus-condition2.png){width="600" zoomable="yes"}

1. 다음을 포함하여 규칙을 완료합니다. [작업](price-rules-catalog.md) 조건이 충족될 때 취해야 합니다.

1. 규칙이 완료되면 다음을 클릭하십시오. **[!UICONTROL Save]**.

{{new-price-rule}}
