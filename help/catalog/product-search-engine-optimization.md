---
title: 제품 설정 - [!UICONTROL Search Engine Optimization]
description: 제품의 경우 [!UICONTROL Search Engine Optimization] 설정은 검색 엔진에서 제품을 색인화하는 데 사용하는 URL 키와 메타데이터를 설정합니다.
exl-id: 78888094-759c-4e45-afcd-65858ee76159
feature: Catalog Management, Products, Search
source-git-commit: 01148770946a236ece2122be5a88b963a0f07d1f
workflow-type: tm+mt
source-wordcount: '494'
ht-degree: 0%

---

# 제품 설정 - [!UICONTROL Search Engine Optimization]

_검색 엔진 최적화_(SEO)는 검색 엔진에서 페이지를 인덱싱하는 방식을 개선하기 위해 사이트의 내용과 프레젠테이션을 미세 조정하는 방법입니다.

제품에 대한 _[!UICONTROL Search Engine Optimization]_&#x200B;설정은 검색 엔진에서 제품을 색인화하는 데 사용하는 [URL 키](catalog-urls.md) 및 [메타데이터](../merchandising-promotions/meta-data.md) 필드를 지정합니다. 일부 검색 엔진은 메타 키워드를 무시하지만 다른 검색 엔진은 계속 메타 키워드를 사용합니다. 현재 [SEO 모범 사례](../merchandising-promotions/seo-overview.md)는 메타 제목과 메타 설명에 모두 높은 값의 키워드를 통합하는 것입니다.

각 메타데이터 필드의 기본값은 구성에 지정된 값을 기반으로 자동 생성될 수 있습니다. 각 필드에는 실제 값으로 대체되는 자리 표시자가 포함됩니다. 자세한 내용은 [제품 필드 자동 생성](../configuration-reference/catalog/catalog.md#uicontrol-product-fields-auto-generation)을 참조하세요.

## SEO 필드 작성

1. 제품을 편집 모드로 엽니다.

1. 아래로 스크롤하여 _[!UICONTROL Search Engine Optimization]_&#x200B;섹션에서 ![확장 선택기](../assets/icon-display-expand.png)를 확장합니다.

![검색 엔진 최적화](./assets/product-search-engine-optimization.png){width="600" zoomable="yes"}


1. **[!UICONTROL URL Key]**(선택 사항)을 입력하십시오.

   기본 URL 키는 제품 이름을 기반으로 합니다. 기본값을 사용하거나 필요에 따라 변경할 수 있습니다. 자세한 내용은 [카탈로그 URL](catalog-urls.md)을 참조하세요.

1. **[!UICONTROL Meta Title]**(선택 사항)을 입력하십시오.

   메타 제목은 브라우저 창 맨 위에 표시되는 텍스트입니다. 제품 이름을 기반으로 하는 기본값을 사용하거나 필요에 따라 변경할 수 있습니다.

1. **[!UICONTROL Meta Keywords]**(선택 사항)을 추가합니다.

   메타 키워드는 일부 검색 엔진에서 다른 키워드보다 더 많이 사용됩니다. 제품의 가시성을 높이는 데 도움이 되도록 몇 가지 고가치 키워드를 입력하는 것이 좋습니다.

1. **[!UICONTROL Meta Description]** 입력.

   메타 설명은 검색 결과 목록에 표시되는 텍스트입니다. 최상의 결과를 얻으려면 150~160자 사이의 설명을 입력하십시오.

## 필드 참조

| 필드 | [범위](../getting-started/websites-stores-views.md#scope-settings) | 설명 |
|--- |--- |------------------|
| [!UICONTROL URL Key] | 스토어 뷰 | 제품의 온라인 주소를 결정합니다. URL 키가 저장소의 기본 URL에 추가되고 브라우저의 주소 표시줄에 나타납니다. Commerce은 처음에 제품 이름을 기반으로 하는 _검색 엔진에 친숙한_ URL을 만듭니다. URL 키는 모두 소문자여야 하며 문자 사이에 공백 대신 뒤에 붙지 않는 하이픈이 있어야 합니다. URL 키는 구성에서 관리되므로 URL 키에 `.html`과(와) 같은 접미사를 포함하지 마십시오. |
| [!UICONTROL Meta Title] | 스토어 뷰 | 제목은 브라우저의 제목 표시줄 및 탭에 나타나며 검색 엔진 결과 페이지(SERP)의 제목으로도 사용됩니다. 메타 제목은 페이지에 고유해야 하며 길이는 70자 미만이어야 합니다. 자동 생성된 값: `{{name}}` |
| [!UICONTROL Meta Keywords] | 스토어 뷰 | 제품에 대한 관련 키워드. 고객이 제품을 찾는 데 사용할 수 있는 키워드를 사용하는 것이 좋습니다. 자동 생성된 값: `{{name}}` |
| [!UICONTROL Meta Description] | 스토어 뷰 | 메타 설명은 검색 결과 목록 페이지에 대한 간략한 개요를 제공합니다. 이상적인 길이는 150~160자 사이이며 최대 255자입니다. 고객에게 표시되지 않지만 일부 검색 엔진에는 검색 결과 페이지에 메타 설명이 포함됩니다. 자동 생성된 값: `{{name}} {{description}}` |

{style="table-layout:auto"}
