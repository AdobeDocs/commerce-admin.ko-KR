---
title: 카탈로그 검색 구성
description: 스토어에 대한 카탈로그 검색을 구성하는 방법에 대해 알아봅니다.
exl-id: b4f22bce-39e2-4269-99a4-eb2d647df939
feature: Catalog Management, Search
source-git-commit: 06673ccb7eb471d3ddea97218ad525dd2cdcf380
workflow-type: tm+mt
source-wordcount: '729'
ht-degree: 0%

---

# 카탈로그 검색 구성

카탈로그 검색 구성에는 두 가지 변형이 있습니다. 첫 번째 메서드는 다음과 같은 경우에 사용할 수 있는 설정을 설명합니다 [라이브 검색](https://experienceleague.adobe.com/docs/commerce-merchant-services/live-search/overview.html) 이(가) 설치되었습니다. 두 번째 방법은 를 사용하는 기본 Adobe Commerce에 대한 구성 설정을 설명합니다. [Elasticsearch][1]{:target=&quot;_blank&quot;}.

## 방법 1: Adobe Commerce [!DNL Live Search]

1. 다음에서 _관리자_ 사이드바, 이동 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. 왼쪽 패널에서 를 확장합니다. **[!UICONTROL Catalog]** 및 선택 **[!UICONTROL Catalog]** 밑에.

1. 확장 ![확장 선택기](../assets/icon-display-expand.png) 다음 **[!UICONTROL Catalog Search]** 섹션.

   ![라이브 검색에 대한 카탈로그 검색](../configuration-reference/catalog/assets/catalog-search-live-search.png){width="600" zoomable="yes"}

   이러한 옵션에 대한 자세한 목록은 다음을 참조하십시오. [라이브 검색이 포함된 Adobe Commerce](../configuration-reference/catalog/catalog.md#adobe-commerce-with-live-search) 다음에서 _구성 참조_.

1. 검색 쿼리 텍스트의 길이 및 단어 수를 제한하려면 **[!UICONTROL Minimal Query Length]** 및 **[!UICONTROL Maximum Query Length]**.

1. 더 빠른 응답을 위해 캐시할 방문 빈도가 높은 검색 결과의 양을 제한하려면 **[!UICONTROL Number of top search results to cache]**.

   기본값은 입니다. `100`. 값 입력 `0` 을(를) 두 번째로 입력하면 모든 검색어와 결과를 캐시합니다.

1. 반환된 결과에 사용할 수 있는 최대 라인 수를 변경하려면 [상점 앞의 팝오버](https://experienceleague.adobe.com/docs/commerce-merchant-services/live-search/live-search-storefront/quick-tour.html), 다른 을(를) 입력합니다 **[!UICONTROL Autocomplete Limit]** 값.

   라인 수를 제한하면 검색 성능이 향상되고 반환된 목록의 크기가 줄어듭니다. 기본값은 입니다. `8` 줄.

## 방법 2: Elasticsearch과 상거래

>[!IMPORTANT]
>
>(으)로 인해 [!DNL Elasticsearch 7] 2023년 8월 지원 종료 발표에서는 모든 Adobe Commerce 고객이 OpenSearch 2.x 검색 엔진으로 마이그레이션하는 것이 좋습니다. 제품 업그레이드 중 검색 엔진 마이그레이션에 대한 자세한 내용은 [OpenSearch로 마이그레이션](https://experienceleague.adobe.com/docs/commerce-operations/upgrade-guide/prepare/opensearch-migration.html) 다음에서 _업그레이드 안내서_.

### 1단계: 일반 검색 옵션 구성

>[!NOTE]
>
>Elasticsearch을 사용하면 접미사에 의한 검색이 기본적으로 지원되지 않습니다. 예를 들어 키워드에 SKU의 끝 부분만 포함된 경우 SKU로 검색하면 예상 결과가 반환되지 않을 수 있습니다.

1. 다음에서 _관리자_ 사이드바, 이동 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. 왼쪽 패널에서 를 확장합니다. **[!UICONTROL Catalog]** 및 선택 **[!UICONTROL Catalog]** 밑에.

1. 확장 ![확장 선택기](../assets/icon-display-expand.png) 다음 **[!UICONTROL Catalog Search]** 섹션.

   ![Elasticsearch 설정](../configuration-reference/catalog/assets/catalog-search-elasticsearch.png){width="600" zoomable="yes"}

   이러한 옵션에 대한 자세한 내용은 [Elasticsearch 포함 Adobe Commerce](../configuration-reference/catalog/catalog.md#adobe-commerce-with-elasticsearch) 다음에서 _구성 참조_.

1. 검색 쿼리 텍스트의 길이 및 단어 수를 제한하려면 **[!UICONTROL Minimal Query Length]** 및 **[!UICONTROL Maximum Query Length]**.

   >[!IMPORTANT]
   >
   >이 최소 및 최대 범위에 대해 설정된 값은 Elasticsearch 검색 엔진 구성의 해당 범위 세트와 호환되어야 합니다. 예를 들어 이러한 값을 로 설정하면 `2` 및 `300` Commerce에서 검색 엔진에서 해당 값을 업데이트합니다.

1. 더 빠른 응답을 위해 캐시할 방문 빈도가 높은 검색 결과의 양을 제한하려면 **[!UICONTROL Number of top search results to cache]**.

   기본값은 입니다. `100`. 값 입력 `0` 을(를) 두 번째로 입력하면 모든 검색어와 결과를 캐시합니다.

1. 제품 EAV 인덱서를 활성화하거나 비활성화하려면 **[!UICONTROL Enable EAV Indexer]**.

   이 기능은 색인 생성 속도를 향상시키고 타사 확장에서 색인을 사용하지 못하도록 제한합니다.

1. 검색 자동 완성에 대해 표시할 최대 검색 결과 수를 제한하려면 다음에 대한 금액을 설정합니다. **[!UICONTROL Autocomplete Limit]**.

   이 양을 제한하면 검색 성능이 향상되고 표시된 목록 크기가 줄어듭니다. 기본값은 입니다. `8`.

### 2단계: Elasticsearch 연결 구성

>[!IMPORTANT]
>
>다음 **[!UICONTROL Search Engine]**, **[!UICONTROL Elasticsearch Server Hostname]**, **[!UICONTROL Elasticsearch Server Port]**, **[!UICONTROL Elasticsearch Index Prefix]**, **[!UICONTROL Enable Elasticsearch HTTP Auth]**, 및 **[!UICONTROL Elasticsearch Server Timeout]** Commerce가 설치되거나 업그레이드될 때 필드가 구성되었습니다. 이러한 값은 Elasticsearch을 업그레이드하거나 수정할 때만 변경해야 합니다.

1. 대상 **[!UICONTROL Search Engine]**, 기본값을 사용합니다. `Elasticsearch 7`.

   Elasticsearch 7.6.x는 모든 Commerce 설치에 필요합니다.

1. 대상 **[!UICONTROL Elasticsearch Server Hostname]**, Commerce 설치 시 구성된 기본값을 사용합니다.

   이 예제에서 기본값은 입니다. `elasticsearch.internal`.

1. 대상 **[!UICONTROL Elasticsearch Server Port]**, Commerce 설치 시 구성된 기본값을 사용합니다.

   이 예제에서 기본값은 입니다. `9200`.

1. 대상 **[!UICONTROL Elasticsearch Index Prefix]**&#x200B;를 클릭하고 접두사를 입력하여 Elasticsearch 색인을 식별합니다.

   기본값은 입니다. `magento2`.

1. HTTP 인증을 사용하여 Elasticsearch 서버에 액세스할 사용자 이름과 암호를 묻는 메시지를 표시하려면 다음을 설정합니다. **[!UICONTROL Enable Elasticsearch HTTP Auth]** 끝 `Yes`.

1. 대상 **[!UICONTROL Elasticsearch Server Timeout]**&#x200B;시스템 시간이 초과되기 전 시간(초)을 입력합니다.

   기본값은 입니다. `15`.

1. 구성을 확인하려면 다음을 클릭하십시오. **[!UICONTROL Test Connection]**.

### 3단계: 제안 및 권장 사항 구성

>[!NOTE]
>
>검색 제안 및 권장 사항은 서버 성능에 영향을 줄 수 있습니다.

1. 권장 사항을 제공하려면 다음을 설정하십시오. **[!UICONTROL Enable Search Recommendations]** 끝 `Yes` 다음을 수행합니다.

   - 대상 **[!UICONTROL Search Recommendation Count]**, 오퍼할 권장 사항 수를 입력합니다.

   - 각 권장 사항에 대해 발견된 결과 수를 표시하려면 다음을 설정합니다. **[!UICONTROL Show Results Count for Each Recommendation]** 끝 `Yes`.

1. 설정 **[!UICONTROL Enable Search Suggestions]** 끝 `Yes` 다음을 수행합니다.

   - 대상 **[!UICONTROL Search Suggestions Count]**&#x200B;을(를) 제안할 검색 제안 수를 입력합니다.

   - 각 제안에 대해 발견된 결과 수를 표시하려면 다음을 설정합니다. **[!UICONTROL Show Results for Each Suggestion]** 끝 `Yes`.

### 4단계: 일치시킬 최소 용어 구성

검색어 반환을 위해 검색 결과가 일치해야 하는 쿼리의 최소 용어 수를 제어하려면 다음 값을 지정합니다 **[!UICONTROL Minimum Terms to Match]**. 이 값을 지정하면 쇼핑객의 최적의 결과 관련성을 확보할 수 있습니다. 허용되는 값 목록은 다음을 참조하십시오 [minimum_should_match 매개 변수](https://www.elastic.co/guide/en/elasticsearch/reference/current/query-dsl-minimum-should-match.html) Elasticsearch 설명서에서 확인할 수 있습니다.

완료되면 다음을 클릭하십시오. **[!UICONTROL Save Config]**.

[1]: https://experienceleague.adobe.com/docs/commerce-operations/installation-guide/prerequisites/search-engine/overview.html
[2]: https://experienceleague.adobe.com/docs/commerce-operations/configuration-guide/search/overview-search.html
