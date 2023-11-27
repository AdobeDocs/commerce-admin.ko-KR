---
title: 카탈로그 검색 개요
description: 고객이 상점에서 제품을 찾는 데 사용할 수 있는 빠른 검색 및 고급 검색 도구에 대해 알아봅니다.
exl-id: a796fa48-212a-47c7-ab6e-98edd4d040f4
feature: Catalog Management, Search
source-git-commit: 01148770946a236ece2122be5a88b963a0f07d1f
workflow-type: tm+mt
source-wordcount: '517'
ht-degree: 0%

---

# 카탈로그 검색 개요

>[!TIP]
>
>[[!DNL Live Search]](https://experienceleague.adobe.com/docs/commerce-merchant-services/live-search/overview.html) 는 빠르고, 관련성이 높고, 직관적인 검색 환경을 제공하며, Adobe Commerce에서 추가 비용 없이 사용할 수 있습니다. 이 섹션에서는 다음과 다를 수 있는 표준 검색 기능에 대해 설명합니다. [!DNL Live Search].

탐색만 의존한 고객보다 검색을 이용하는 사람이 구매를 할 가능성이 높다는 연구결과가 나왔다. 실제로 일부 연구에 따르면, 검색을 이용하는 사람들은 구매에 성공할 가능성이 거의 두 배이다.

다음 섹션에서는 기본 카탈로그 검색 기능에 대해 설명합니다. 기본 카탈로그 검색 기능을 구성하고 사용자 지정하는 방법에 대한 자세한 내용은 다음을 참조하십시오.

- [카탈로그 검색 구성](search-configuration.md)
- [검색 결과](search-results.md)
- [검색어 관리](search-terms.md)

>[!NOTE]
>
>Commerce의 기본 검색 기능은 정확한 일치 검색 결과를 제공합니다. While [!DNL Live Search]Adobe Commerce 내에서 설치 및 활성화할 수 있는 선택 모듈인 는 다르게 구현되며 그 결과는 정확한 검색 문자열로 제한되지 않습니다. 예를 들어 에 대해 숫자로 레이블이 지정된 제품이 10개인 경우 _오메가_: 다음에 대한 검색 `Omega 1` 에 대한 단일 일치 항목 검색 _오메가 1_ 기본 검색 기능 사용. 하지만 라이브 검색에서 제공하는 동일한 검색 문자열은 여러 항목을 일치시킵니다. _오메가 1_ 및 _오메가_.

## 빠른 검색

>[!NOTE]
>
>날짜 [[!DNL Live Search]](https://experienceleague.adobe.com/docs/commerce-merchant-services/live-search/live-search-storefront/quick-tour.html) 가 설치되어 있으면 검색 상자에 &quot;검색할 때&quot;라는 검색 결과가 표시됩니다.

스토어 헤더의 검색 상자는 방문자가 카탈로그에서 제품을 찾을 수 있도록 도와줍니다. 검색 텍스트는 전체 또는 부분 제품 이름 또는 제품을 설명하는 다른 단어 또는 구문일 수 있습니다. 사람들이 제품을 찾는 데 사용하는 검색어는 관리자로부터 관리할 수 있습니다.

1. 대상 **[!UICONTROL Search]**&#x200B;를 검색하는 동안 고객은 원하는 항목의 처음 몇 글자를 입력합니다.

   카탈로그에 있는 모든 일치 항목이 검색 결과 수와 함께 아래에 표시됩니다.

1. 고객이 Enter 키를 누르거나 일치하는 제품 목록에서 결과를 클릭합니다.

   ![검색](./assets/storefront-search-box.png){width="700" zoomable="yes"}

## 고급 검색

>[!NOTE]
>
>여기에 설명된 고급 양식 검색 기능은 에는 적용되지 않습니다. [[!DNL Live Search]](https://experienceleague.adobe.com/docs/commerce-merchant-services/live-search/overview.html).

고급 검색을 사용하면 쇼핑객이 양식에 입력한 값을 기반으로 카탈로그를 검색할 수 있습니다. 양식에는 여러 필드가 있으므로 단일 검색에 여러 매개 변수가 포함될 수 있습니다. 결과는 기준에 일치하는 카탈로그의 모든 제품 목록입니다. 고급 검색 링크가 저장소의 바닥글에 있습니다.

![고급 검색](./assets/storefront-search-advanced.png){width="700" zoomable="yes"}

양식의 각 필드는 제품 카탈로그의 속성에 해당합니다. 필드를 추가하려면 속성의 프론트엔드 속성을 다음으로 설정하십시오. `Include in Advanced Search`. 너무 많으면 검색 속도가 느려지기 때문에 고객이 제품을 찾는 데 사용할 가능성이 가장 높은 필드만 포함하는 것이 좋습니다.

1. 스토어의 바닥글에서 고객이 클릭 **[!UICONTROL Advanced Search]**.

1. 다음에서 _고급 검색_ form에서 전체 또는 부분 값을 필요한 수만큼 필드에 추가합니다.

1. 클릭수 **[!UICONTROL Search]** 결과를 표시합니다.

   ![검색 결과](./assets/storefront-search-advanced-results-modify.png){width="700" zoomable="yes"}

1. 고객이 검색 결과에서 찾고 있는 내용을 보지 못하면 고객이 클릭 수를 증가시킵니다 **[!UICONTROL Modify your search]** 및 은 기준의 다른 조합을 시도합니다.
