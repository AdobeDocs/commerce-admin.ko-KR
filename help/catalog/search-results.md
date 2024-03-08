---
title: 검색 결과
description: 제품이 빠른 검색 상자 또는 고급 검색 양식에 입력한 검색 기준과 어떻게 일치하는지 구성하는 방법에 대해 알아봅니다.
exl-id: c721fb3b-ee31-4d2b-b4ea-9ae2c80aa800
feature: Catalog Management, Search
source-git-commit: 4b2e1dd87a39c9be1adc49d867e44d306a969854
workflow-type: tm+mt
source-wordcount: '887'
ht-degree: 0%

---

# 검색 결과

>[!NOTE]
>
>이 페이지에서는 다음과 다를 수 있는 표준 검색 기능에 대해 설명합니다. [라이브 검색](https://experienceleague.adobe.com/docs/commerce-merchant-services/live-search/overview.html).

다음 _검색 결과_ 목록에는 빠른 검색 상자 또는 고급 검색 양식에 입력한 검색 기준과 일치하는 모든 제품이 포함됩니다. 카탈로그의 모든 제품 목록에는 기본적으로 동일한 컨트롤이 있습니다. 유일한 차이점은 하나는 검색 쿼리의 결과이고, 다른 차이점은 의 결과입니다 [탐색](navigation.md).

결과의 서식을 그리드 또는 목록으로 지정하고 선택한 속성별로 정렬할 수 있습니다. 페이지에 맞는 것보다 많은 제품이 있는 경우 페이지 매김 컨트롤이 나타납니다. 이러한 컨트롤을 사용하여 한 페이지에서 다음 페이지로 이동합니다. 페이지당 레코드 수는 카탈로그 프론트엔드 구성에 의해 결정됩니다. 자세한 내용은 [제품 목록](navigation-product-listings.md).

포함 **Elasticsearch**:

- 접미사에 의한 검색은 기본적으로 지원되지 않습니다. 예를 들어 키워드에 SKU의 끝 부분만 포함된 경우 SKU로 검색하면 예상 결과가 반환되지 않을 수 있습니다.
- 다음에 대한 접두사로 검색(부분 키워드 검색)을 기본적으로 지원합니다. `name` 및 `sku` 제품 속성만 해당됩니다. 다른 모든 제품 속성은 정확히 일치하는 전체 키워드로 검색됩니다.
- 검색 결과 `name` 및 `sku` 제품 속성은 정확한 일치가 아니라 관련성을 기반으로 합니다. 정확히 일치하는 항목과 같이 가장 관련성이 높은 일치 항목 _제품 이름_ 또는 _SKU_&#x200B;가 먼저 나열됩니다. 정확한 일치 항목을 검색하기 위해 고객은 검색 쿼리에 큰따옴표를 사용할 수 있습니다. 예: `WSH12-32-Red` 검색 쿼리는 관련성을 기준으로 정렬된 여러 제품을 반환할 수 있습니다. 하지만 `"WSH12-32-Red"` 검색 쿼리에서 **_정확하게_** 일치함 `sku`.

![페이지 매김 컨트롤을 사용한 검색 결과](./assets/storefront-search-results-shorts.png){width="700" zoomable="yes"}

>[!IMPORTANT]
>
>2023년 8월의 Elasticsearch 7 지원 종료 발표로 인해 모든 Adobe Commerce 고객은 OpenSearch 2.x 검색 엔진으로 마이그레이션하는 것이 좋습니다. 제품 업그레이드 중 검색 엔진 마이그레이션에 대한 자세한 내용은 [OpenSearch로 마이그레이션](https://experienceleague.adobe.com/docs/commerce-operations/upgrade-guide/prepare/opensearch-migration.html) 다음에서 _업그레이드 안내서_.

## 검색 결과를 확장하기 위한 키워드 매핑

이 기술은 속성을 사용하여 두 제품 간에 키워드 기반 연결을 만들어 두 제품 중 하나에 대한 검색 결과가 반환되도록 합니다. 키워드 매핑을 사용하여 표시되지 않는 검색 결과에서 제품을 판촉할 수 있습니다.

![키워드 매핑이 있는 검색 결과](./assets/storefront-search-results-extended.png){width="700" zoomable="yes"}

다음 예에서는 SKU를 기반으로 한 키워드 매핑을 사용합니다. 검색 상자에 SKU를 입력하면 두 제품이 모두 결과에 표시됩니다. 구성 가능한 다음 제품의 SKU는 제품 변형의 SKU가 아니라 매핑됩니다.

- 몬태나 윈드 재킷 (MJ03)
- 차즈 캥거루 후디 (MH01)

### 1단계: 속성 만들기

1. 다음에서 _[!UICONTROL Products]_목록, 열기 `Montana Wind Jacket` (MJ03) 편집 모드에 있습니다.
1. 오른쪽 위 모서리에서 을(를) 클릭합니다. **[!UICONTROL Add Attribute]**.
1. 다음에서 _속성 선택_ 페이지, 클릭 **[!UICONTROL Create New Attribute]**.
1. 다음과 같이 속성 속성을 완료합니다.

   **[!UICONTROL Attribute Properties]**

   - [!UICONTROL Attribute Label]  - `Search Keywords`
   - [!UICONTROL Catalog Input Type for Store Owner] - `Text Field`

   **[!UICONTROL Advanced Attribute Properties]**

   - [!UICONTROL Add to Column Options] - `Yes` (기본값)
   - [!UICONTROL Use in Filter Options] - `Yes` (기본값)

   **[!UICONTROL Storefront Properties]**

   - [!UICONTROL Use in Search] - `Yes`
   - [!UICONTROL Visible on Catalog Pages in the Storefront] - `No`
   - [!UICONTROL Used in Product Listings] - `No`

1. 완료되면 다음을 클릭하십시오. **[!UICONTROL Save Attribute]**.

   속성이 제품에 대한 속성 세트에 추가됩니다.

### 2단계: 첫 번째 제품 매핑

1. 제품 설정 페이지에서 아래로 스크롤하여 를 확장합니다. _[!UICONTROL Attributes]_섹션.
1. 다음에서 **[!UICONTROL Search Keywords]** 필드, SKU 입력 `MH01` 이 제품에 매핑될 예정입니다.

   검색 키워드 필드에 공백으로 구분된 여러 SKU를 입력할 수 있습니다. 이 예제에서는 하나만 입력됩니다.

   ![검색 키워드가 있는 속성 섹션](./assets/search-keywords-attribute.png){width="600" zoomable="yes"}

1. 완료되면 다음을 클릭하십시오. **[!UICONTROL Save]**.
1. 다음으로 이동 **[!UICONTROL System]** > _[!UICONTROL Tools]_>**[!UICONTROL Cache Management]**및 새로 고침&#x200B;**[!UICONTROL Page Cache]**.

### 3단계: 두 번째 제품 매핑

1. 다음에서 _[!UICONTROL Products]_목록, 열기 `Chaz Kangaroo Hoodie` (MH01) 편집 모드에 있습니다.
1. 아래로 스크롤하고 를 확장합니다. **[!UICONTROL Attributes]** 섹션.
1. 다음에서 **[!UICONTROL Search Keywords]** 필드에 다른 제품에 대한 SKU를 입력합니다. `MJ03`.
1. 클릭 **[!UICONTROL Save]**.
1. 다음으로 이동 **[!UICONTROL System]** > _[!UICONTROL Tools]_>**[!UICONTROL Cache Management]**및 새로 고침&#x200B;**[!UICONTROL Page Cache]**.

### 4단계: 상점에서 테스트합니다.

1. 가게 앞까지 가서 들어오세요 `MJ03` 다음에서 _빠른 검색_ 상자.
1. 두 제품이 검색 결과 목록에서 반환되는지 확인합니다.

## 가중 검색

카탈로그 검색에 대해 활성화된 제품 속성에 가중치를 지정하여 검색 결과에서 더 높은 값을 제공할 수 있습니다. 가중치가 큰 속성은 가중치가 낮은 속성보다 먼저 반환됩니다. 예를 들어 시스템에 두 개의 속성이 있는 경우 _색상_ 검색 가중치가 3 및 _설명_ 검색 가중치가 1인. 단어 검색 _빨강_ 다음 색상 속성 값이 있는 제품 목록을 반환합니다. `red` 검색 결과 상단에 단어 포함 설명이 있는 제품 반환 _빨강_ 검색 결과 하단에 있습니다. 이 예에서는 `color` 속성의 정의된 가중치가 다음보다 큼 `description` 특성.

>[!IMPORTANT]
>
>관련성을 기준으로 정렬하는 것은 다음에 의해 영향을 받습니다. **_복수_** 기준 및 기준 간 관계 **_동시에_**. [!UICONTROL Search Weight] 는 이러한 기준 중 하나에 불과합니다. 이는 때때로 검색 가중치가 낮은 속성이 검색 가중치가 높은 속성보다 여전히 더 많은 관련성을 가질 수 있음을 의미한다. 다른 기준에는 주어진 속성의 일치 수, 검색된 검색어의 위치 및 검색어 전후의 전체 텍스트 구조가 포함될 수 있습니다.

**_속성의 검색 가중치 등록 정보를 설정하려면 다음을 수행합니다._**

1. 다음에서 _관리자_ 사이드바, 이동 **[!UICONTROL Stores]** > _[!UICONTROL Attributes]_>**[!UICONTROL Product]**.

1. 목록에서 속성을 찾아 편집 모드로 엽니다.

1. 왼쪽 패널에서 을 선택합니다 **[!UICONTROL Storefront Properties]** 다음을 수행합니다.

   - 검색 쿼리에 속성을 포함하려면 다음을 설정합니다. **[!UICONTROL Use in Search]** 끝 `Yes`.

   - 속성의 검색 값을 설정하려면 를 설정합니다 **[!UICONTROL Search Weight]** 1에서 10 사이의 숫자로 변환, 여기서 `10` 이(가) 가장 높은 우선 순위를 갖습니다. 값을 입력하지 않으면 모든 속성의 기본값은 검색 가중치입니다. `1`.

   ![가중치 검색](./assets/search-weight.png){width="600" zoomable="yes"}

1. 완료되면 다음을 클릭하십시오. **[!UICONTROL Save Attribute]**.
