---
title: 공유 카탈로그 가격 및 구조 설정
description: Adobe Commerce B2B를 사용하여 공유 카탈로그의 가격 및 구조를 설정하는 방법에 대해 알아봅니다.
exl-id: 67caf56f-1b31-44bb-98dc-ea6ea7d8a4d5
feature: B2B, Companies, Catalog Management
role: Admin
source-git-commit: 61df9a4bcfaf09491ae2d353478ceb281082fa74
workflow-type: tm+mt
source-wordcount: '1305'
ht-degree: 0%

---

# 공유 카탈로그 가격 및 구조 설정

공유 카탈로그의 가격 및 구조를 설정하는 작업은 두 단계로 진행됩니다. 프로세스의 현재 위치는 페이지 상단의 진행률 표시줄에 숫자가 강조 표시됩니다. 진행률 표시줄을 클릭하여 언제든지 프로세스의 다른 단계를 볼 수 있습니다. 예를 들어 사용자 지정 가격 책정 작업을 수행하는 경우 제품 선택 페이지로 돌아가 참조할 수 있습니다. 페이지 상단의 진행률 표시줄에서 **[!UICONTROL Products]**&#x200B;을(를) 클릭한 다음 **[!UICONTROL Pricing]**&#x200B;을(를) 클릭하여 사용자 지정 가격 페이지로 돌아가기만 하면 됩니다. 이 과정에서 귀하의 작업은 손실되지 않습니다.

카탈로그의 ![제품](./assets/shared-catalog-products-workspace.png){width="700" zoomable="yes"}

표준 범주 트리에서 루트 범주는 최상위 컨테이너이며 샘플 데이터에서 _기본 범주_&#x200B;라고 합니다. 그러나 공유 카탈로그를 사용하도록 설정하면 범주 트리에 _루트 카탈로그_&#x200B;라는 외부 컨테이너가 있습니다. 루트 카탈로그는 시스템에 존재하는 다른 모든 범주 구조를 포함합니다. 자세한 내용은 [카탈로그 범위](../catalog/introduction.md#catalog-scope)를 참조하세요.

## 1단계: 공유 카탈로그 가격 책정 및 구조 구성을 엽니다.

1. _관리자_ 사이드바에서 **[!UICONTROL Catalog]** > **[!UICONTROL Shared Catalogs]**(으)로 이동합니다.

1. 격자에 있는 공유 카탈로그의 경우 _[!UICONTROL Action]_&#x200B;열로 이동하여&#x200B;**[!UICONTROL Set Pricing and Structure]**&#x200B;을(를) 클릭합니다.

   ![공유 카탈로그의 가격 및 구조 설정](./assets/shared-catalog-set-pricing-structure.png){width="700" zoomable="yes"}

1. 공유 카탈로그가 처음 구성되면 **[!UICONTROL Configure]**&#x200B;을(를) 클릭하여 다음 단계를 계속합니다.

## 2단계: 제품 선택

프로세스의 첫 번째 단계는 공유 카탈로그에 포함할 제품을 선택하는 것입니다. 제품 선택 페이지의 왼쪽에는 [범주 트리](../catalog/category-create.md)가 표시되고 오른쪽에는 동기화된 제품 그리드가 표시됩니다. 트리에서 카테고리를 클릭하면 카테고리의 제품이 그리드에 나타납니다.

공유 카탈로그를 상점 전면에서 볼 때 선택한 제품이 있는 범주만 [위쪽 탐색](../catalog/navigation-top.md)에 표시됩니다. 기본적으로 상점 탐색에는 처음 세 가지 카테고리 수준만 포함되며 루트 카테고리는 포함되지 않습니다.

1. **스토어** 선택기를 사용하여 구성의 [범위](../catalog/introduction.md#product-scope)을(를) 설정합니다.

   공유 카탈로그를 처음 저장하기 전에만 구성 범위를 설정할 수 있습니다. 나중에 제품 선택을 편집하면 스토어 선택기를 사용할 수 없습니다.

   ![스토어 선택](./assets/shared-catalog-products-scope.png){width="600" zoomable="yes"}

1. 범주 트리에서 다음 중 하나를 수행합니다.

   - 모든 제품을 포함하려면 **[!UICONTROL Select all]**&#x200B;을(를) 클릭하거나 상위 범주의 확인란을 선택하십시오.
   - 특정 제품 카테고리를 포함하려면 포함하려는 각 카테고리의 확인란을 선택합니다.
   - 개별 제품을 포함하거나 제외하려면 제품 확인란을 선택하거나 선택 취소합니다.

   트리의 각 카테고리 아래에 있는 표기법에는 현재 공유 카탈로그에 포함된 카테고리의 제품 수가 표시됩니다. [루트 범주](../catalog/category-root.md) 아래의 표기법에는 현재 공유 카탈로그에 대해 선택된 모든 범주의 총 제품 수가 표시됩니다.

1. 그리드에서 카테고리 제품을 보려면 트리에서 카테고리 이름을 클릭합니다. 카테고리를 선택하면 다음 상황이 발생합니다.

   - 그리드의 첫 번째 열에서 토글이 선택한 각 제품에 대해 녹색 _켜짐_ 위치로 설정됩니다.
   - 제품이 여러 범주에 할당되어 있고 이 중 하나에서 선택되지 않은 경우 다른 범주를 통해 사용할 수 있으며 [카탈로그 검색](../catalog/search.md)을 사용할 때도 사용할 수 있습니다.
   - 선택한 제품에 대해 [범주 권한](../catalog/category-permissions.md)을(를) `Allow`(으)로 자동 설정합니다.

1. 필요한 경우 필터 및 기타 격자 컨트롤을 사용하여 공유 카탈로그에 포함할 제품을 찾습니다.

   첫 번째 열에서 전환을 클릭하여 개별 제품을 개별적으로 선택하거나 생략할 수 있습니다.

   제품이 없지만 CMS 콘텐츠 또는 외부 링크에 연결된 카테고리를 선택하면 상점 첫 화면의 위쪽 탐색에 표시됩니다.

   만든 범주 설정은 구성이 저장될 때까지 데이터베이스에 영구적으로 기록되지 않습니다. 단, 구조 및 가격 작업을 수행할 때 일시적으로 저장됩니다.

1. **[!UICONTROL Next]**&#x200B;을(를) 클릭합니다.

   ![카탈로그에 대한 제품 선택](./assets/shared-catalog-select-products-step-1.png){width="600" zoomable="yes"}

## 3단계: 사용자 정의 가격 설정

각 제품에 대해 개별적으로 사용자 지정 가격을 설정하거나 _[!UICONTROL Action]_&#x200B;컨트롤을 사용하여 여러 제품 레코드에 대한 고정 금액 또는 백분율로 사용자 지정 가격을 설정할 수 있습니다.

- **[!UICONTROL Fixed]**: 최종 제품 가격을 지정합니다. 예를 들어 고정 가격 $10.00를 입력하면 해당 회사의 상점 가격은 $10.00입니다.

  >[!NOTE]
  >
  >기준 가격과 입력된 고정 값 사이의 최소값이 최종 제품 가격으로 사용됩니다.

  >[!NOTE]
  >
  >**_고정 가격_** 제품 사용자 지정 가능 옵션은 그룹 가격, 계층 가격, 특별 가격 또는 카탈로그 가격 규칙의 영향을 받지 _않습니다_.

- **[!UICONTROL Percentage]**: 할인율을 기준으로 사용자 지정 가격을 결정합니다. 예를 들어 10% 할인을 제공하려면 사용자 지정 가격 유형을 `Percentage`(으)로 설정하고 `10`을(를) 입력합니다. 할인된 맞춤 가격은 원래 제품 가격의 90%입니다.

다음 제품 유형에 대해 고정 금액 또는 백분율로 할인을 설정하려면 표의 _[!UICONTROL Custom Price]_&#x200B;열을 사용하십시오.

- [단순](../catalog/product-create-simple.md)(구성 가능한 제품 변형 포함)
- [번들](../catalog/product-create-bundle.md)
- [다운로드 가능](../catalog/product-create-downloadable.md)
- [가상](../catalog/product-create-virtual.md)

[구성 가능한](../catalog/product-create-configurable.md) 및 [그룹화된](../catalog/product-create-grouped.md) 제품 유형과 [기프트 카드](../catalog/product-gift-card-create.md)의 경우 사용자 지정 가격 열이 비어 있습니다.

_사용자 지정 가격_ 페이지에서 그리드의 제품 선택을 변경할 수 없습니다. 그러나 페이지 상단의 진행률 표시기를 사용하여 이전 단계로 돌아가서 제품 선택을 변경할 수 있습니다.

![카탈로그에 대한 제품 선택](./assets/shared-catalog-custome-prices-step-3.png){width="600" zoomable="yes"}

### 사용자 정의 가격 적용

1. 다중 사이트 설치의 경우 사용자 지정 가격이 적용되는 웹 사이트로 **[!UICONTROL Website]**&#x200B;을(를) 설정합니다.

   ![웹 사이트 선택](./assets/shared-catalog-scope-pricing.png){width="600" zoomable="yes"}

1. 다음 방법 중 하나를 사용하여 사용자 정의 가격을 적용할 제품을 선택합니다.

   - 카테고리 트리를 사용하여 특정 카테고리의 모든 제품을 선택합니다.
   - 헤더의 _[!UICONTROL Mass Actions]_&#x200B;컨트롤을 `Select All`(으)로 설정합니다.
   - 개별 제품의 확인란을 선택합니다.

   표에는 현재 선택한 범주에 있는 제품이 표시되며 표준 컨트롤을 사용하여 제품을 찾고 목록을 필터링할 수 있습니다.

   ![모두 선택](./assets/shared-catalog-custom-pricing-mass-actions.png){width="600" zoomable="yes"}

1. **[!UICONTROL Actions]**&#x200B;을(를) 다음 중 하나로 설정합니다.

   - `Set Discount` - 선택한 모든 제품에 할인율을 적용합니다. 영향을 받는 각 제품 가격이 **_할인_** 가격으로 표시됩니다.
   - `Adjust Fixed Price` - 선택한 모든 제품에 고정 가격 할인율을 적용합니다. 영향을 받는 각 제품 가격이 **_조정된 고정_** 가격으로 표시됩니다.

   ![작업 제어 - 할인 설정](./assets/shared-catalog-set-custom-prices-discount-action.png){width="600" zoomable="yes"}

1. 메시지가 표시되면 할인 또는 가격 조정을 입력하고 **[!UICONTROL Apply]**&#x200B;을(를) 클릭합니다.

   ![할인 설정](./assets/shared-catalog-set-custom-prices-discount.png){width="400"}<br/>

   ![고정 가격 조정](./assets/shared-catalog-set-custom-fixed-prices.png){width="400"}

   선택한 모든 제품에 할인이 적용되며 _사용자 지정 가격_ 열에 적용되는 할인 유형 및 금액이 반영됩니다.

   ![할인이 포함된 사용자 지정 가격 열](./assets/shared-catalog-set-custom-prices-discount-applied.png){width="600" zoomable="yes"}

### 계층 가격 적용

[계층 가격](../catalog/product-price-tier.md)을 사용하면 공유 카탈로그의 제품에 대해 수량 할인을 제공할 수 있습니다. 그리드의 _계층 가격_ 열에는 공유 카탈로그에만 적용되는 _고급 가격 설정_ 옵션에 대한 링크가 포함되어 있습니다. 제품에 이미 계층 가격이 포함되어 있는 경우 링크 뒤에 기존 계층의 수가 괄호 안에 표시됩니다.

다음 지침은 단일 제품에 계층 가격을 적용하는 방법을 보여 줍니다. 여러 제품에 계층 가격을 적용하려면 [계층 가격 가져오기](../systems/data-import-price-tier.md)를 참조하세요.

1. 표의 제품에 대해 _계층 가격_ 열로 이동하여 **[!UICONTROL Configure]**&#x200B;을(를) 클릭합니다.

   ![계층 가격 구성](./assets/shared-catalog-tier-price-configure.png){width="600" zoomable="yes"}

1. _고급 가격_ 페이지에서 **[!UICONTROL Add Price]**&#x200B;을(를) 클릭하고 다음을 수행합니다.

   ![카탈로그 및 계층 가격](./assets/shared-catalog-tier-price-configure-add-price.png){width="600" zoomable="yes"}

   - 계층 가격이 적용되는 웹 사이트로 **[!UICONTROL Website]**&#x200B;을(를) 설정합니다.
   - 할인을 받기 위해 구매해야 하는 제품의 수량을 입력합니다.
   - **[!UICONTROL Price]**&#x200B;을(를) 다음 할인 유형 중 하나로 설정합니다.
      - `Fixed`
      - `Discount`
   - 할인 금액을 입력합니다.
   - 다른 계층을 입력하려면 **가격 추가**&#x200B;를 클릭하고 프로세스를 반복하여 다음 계층을 정의하십시오.

   ![여러 계층 가격](./assets/shared-catalog-tier-price-configure-multiple-tiers.png){width="600" zoomable="yes"}

1. 완료되면 **[!UICONTROL Done]**&#x200B;을(를) 클릭합니다.

   그리드에서 계층 수는 _[!UICONTROL Tier Price]_&#x200B;열에서 괄호로 묶어 표시됩니다.

   ![여러 계층](./assets/shared-catalog-tier-price-configure-parentheses.png){width="600" zoomable="yes"}

## 구조 및 가격 책정 저장

사용자 지정 가격 책정이 완료되면 **[!UICONTROL Generate Catalog]**&#x200B;을(를) 클릭한 다음 **[!UICONTROL Save]**&#x200B;을(를) 클릭합니다.

이제 공유 카탈로그가 데이터베이스에 저장됩니다. 해당 이름이 _[!UICONTROL Products]_&#x200B;표의&#x200B;_[!UICONTROL Shared Catalog]_ 열에 나타납니다. 다음 단계는 [공유 카탈로그를 회사에 할당](./catalog-shared-assign-companies.md)하는 것입니다.
