---
title: 카탈로그 및 제품 URL
description: 카탈로그 제품의 URL 형식 유형 및 구성 방법에 대해 알아봅니다.
exl-id: 47405dc6-9b5e-4ca8-87eb-5a222de40793
feature: Catalog Management, Products, Search, Categories
source-git-commit: 1edab49fd8d52a1b7414eb207a21c5c03200e75e
workflow-type: tm+mt
source-wordcount: '909'
ht-degree: 0%

---

# 카탈로그 및 제품 URL

제품 및 범주에 할당하는 URL은 검색 엔진이 사이트를 얼마나 잘 색인화하는지 결정하는 데 중요한 역할을 합니다. 카탈로그 작성을 시작하기 전에 사용 가능한 옵션을 고려하십시오. 현재 URL 형식을 보려면 상점으로 이동하여 카탈로그에 있는 제품으로 이동하십시오. URL의 형식은 페이지를 찾는 데 사용하는 현재 구성 설정 및 메서드에 따라 다릅니다.

## URL 형식

### 동적 URL

동적 URL은 _바로_&#x200B;에 만들어지며 제품 ID, 정렬 순서 및 요청이 수행된 페이지에 대한 변수가 포함된 쿼리 문자열을 포함할 수 있습니다. 고객이 스토어에서 제품을 검색할 때 결과 URL은 다음과 같을 수 있습니다.

- `http://mystore.com/catalogsearch/result/?q=racer+back`
- `http://mystore.com/women/tops-women.html?style_general=135`

### 정적 URL

정적 URL은 특정 페이지의 고정 주소입니다. 정적 URL은 검색 엔진에 친숙한 형식 또는 ID별로 제품 및 범주를 참조하는 형식으로 표시할 수 있습니다. 이러한 URL에는 사람들이 제품을 찾는 데 사용할 수 있는 단어가 포함되어 있으며 웹 서버 재작성을 활성화해야 합니다. 정적 URL이 있는 파일은 일반적으로 제품 및 범주 페이지, 콘텐츠 페이지 및 [테마 에셋](../content-design/theme-assets.md)에 사용됩니다.

- `http://mystore.com/antonia-racer-tank.html`

## URL 구성 요소

### URL 키

URL 키는 제품 또는 범주를 설명하는 정적 URL의 일부입니다. 제품이나 카테고리를 만들면 이름을 기반으로 초기 URL 키가 자동으로 생성됩니다. URL 키를 변경하려면 제품 정보의 [검색 엔진 최적화](product-search-engine-optimization.md) 섹션을 참조하세요.

>[!NOTE]
>
>기본적으로, 악센트 부호가 있는 특수 문자는 URL 키에서 악센트 부호가 없는 일반 버전으로 자동 대체됩니다. 예를 들어 `ñ`은(는) `n`(으)로 자동 교체됩니다. _[!UICONTROL Search Engine Optimization: Apply transliteration for product URL]_&#x200B;구성 옵션을 `No`(으)로 설정하여 이 동작을 비활성화할 수 있습니다. [카탈로그 URL 구성](#configure-catalog-urls)을 참조하세요.

URL 키는 단어를 구분하기 위해 문자 사이에 하이픈이 아닌 소문자로 구성되어야 합니다. URL 키의 시작 또는 끝에는 하이픈을 사용할 수 없습니다. 잘 설계된 &quot;검색 엔진 친화적&quot; URL 키에는 제품 이름과 주요 단어가 포함되어 검색 엔진에서 색인화되는 방식을 개선할 수 있습니다. URL 키가 변경되는 경우 자동 리디렉션을 만들도록 URL 키를 구성할 수 있습니다.

>[!NOTE]
>
>지역화된 URL과 같은 URL 사용자 지정을 확장하려면 [URL 다시 쓰기](../merchandising-promotions/url-rewrite.md)를 참조하십시오.

### HTML 접미사

범주 및 제품 URL의 일부로 접미사를 포함하거나 제외하도록 카탈로그를 구성할 수 있습니다. 사람들이 이 접미사를 사용하거나 생략하도록 선택하는 이유는 다양합니다. 어떤 사람들은 접미사가 더 이상 유용한 기능을 하지 않으며, 접미사가 없는 페이지가 검색 엔진에 의해 더 효과적으로 색인화된다고 믿는다. 그러나 회사에 접미사가 필요한 URL에 대해 표준화된 형식이 있을 수 있습니다.

접미사는 시스템 구성에 의해 제어되므로 범주나 제품의 URL 키에 직접 입력해서는 안 됩니다. (이렇게 하면 URL 끝에 이중 접미사가 붙습니다.) 접미어 사용 여부에 관계없이 일관되게 모든 제품 및 카테고리 페이지에 동일한 설정을 사용하십시오. 다음은 접미사가 있는 URL과 없는 URL의 예입니다.

#### HTML 접미사가 있는 URL

- `http://mystore.com/helena-hooded-fleece.html`
- `http://mystore.com/helena-hooded-fleece.htm`

#### HTML 접미사가 없는 URL

- `http://mystore.com/helena-hooded-fleece`

### 범주 경로

환경 설정에 따라 카테고리 경로를 포함하거나 제외하도록 제품 URL을 구성할 수 있습니다. 기본적으로 카테고리 경로는 제품 URL에 포함되지 않습니다. 그러나 중첩된 카테고리는 항상 상점의 URL에 전체 카테고리 경로를 표시하여 카테고리 탐색의 명확성과 일관성을 보장합니다. 다음 예는 카테고리 경로가 있는 것과 없는 것과 동일한 제품 URL을 보여줍니다.

#### 범주 경로가 있는 제품 URL

- `http://mystore.com/women/tops-women/hoodies-and-sweatshirts-women/helena-hooded-fleece.html`

#### 카테고리 경로가 없는 제품 URL

- `http://mystore.com/helena-hooded-fleece.html`

검색 엔진이 동일한 컨텐츠로 이어지는 여러 URL을 색인화하지 못하도록 하려면 URL에서 카테고리 경로를 제외할 수 있습니다. 또 다른 방법은 표준 메타 태그를 사용하여 인덱싱할 URL과 무시할 URL을 검색 엔진에 알려주는 것입니다. 기본적으로 Commerce은 제품 URL에 카테고리 경로를 포함하지 않습니다.

## 카탈로그 URL 구성

1. _관리자_ 사이드바에서 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**(으)로 이동합니다.

1. 왼쪽 패널에서 **[!UICONTROL Catalog]**&#x200B;을(를) 확장하고 아래의 **[!UICONTROL Catalog]**&#x200B;을(를) 선택합니다.

1. **[!UICONTROL Search Engine Optimizations]** 섹션에서 ![확장 선택기](../assets/icon-display-expand.png)를 확장하고 옵션을 설정합니다.

   - **[!UICONTROL Product URL Suffix]**&#x200B;을(를) `html` 또는 `htm`(으)로 설정합니다. 접미사가 자동으로 적용되므로 마침표 없이 접미사를 입력합니다.

   - **[!UICONTROL Category URL Suffix]**&#x200B;을(를) `html` 또는 `htm`(으)로 설정합니다. 접미사가 자동으로 적용되므로 마침표 없이 접미사를 입력합니다.

   - **[!UICONTROL Use Categories Path for Product URLs]**&#x200B;을(를) 기본 설정으로 설정합니다.

   ![검색 엔진 최적화](../configuration-reference/catalog/assets/catalog-search-engine-optimization.png){width="600" zoomable="yes"}

   이러한 옵션에 대한 자세한 목록이 필요하면 _구성 참조_&#x200B;에서 [검색 엔진 최적화](../configuration-reference/catalog/catalog.md#search-engine-optimization)를 참조하십시오.

1. 완료되면 **[!UICONTROL Save Config]**&#x200B;을(를) 클릭합니다.

1. 메시지가 표시되면 시스템 메시지에서 **[!UICONTROL Cache Management]** 링크를 클릭하고 잘못된 캐시를 새로 고칩니다.

   ![캐시 새로 고침](./assets/msg-cache-management.png){width="450" zoomable="yes"}

   이러한 옵션에 대한 자세한 내용은 [캐시 새로 고침](../systems/cache-management.md#refresh-specific-caches)을 참조하십시오.

## 카탈로그 미디어 URL 형식 구성

1. _관리자_ 사이드바에서 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**(으)로 이동합니다.

1. 왼쪽 패널에서 **[!UICONTROL General]**&#x200B;을(를) 확장하고 **[!UICONTROL Web]**&#x200B;을(를) 선택합니다.

1. **[!UICONTROL Url Options]** 섹션에서 ![확장 선택기](../assets/icon-display-expand.png)를 확장하고 옵션을 설정합니다.

![웹 > 일반 옵션](../configuration-reference/general/assets/web-url-options.png){width="600" zoomable="yes"}

| 필드 | [범위](../getting-started/websites-stores-views.md#scope-settings) | 설명 |
|--- |--- |--- |
| [!UICONTROL Add Store Code to URLs] | 글로벌 | 웹 서버 재쓰기가 활성화된 경우 이 설정을 활성화하면 현재 보기의 스토어 코드가 URL에 삽입됩니다. 옵션: `Yes` / `No` |
| [!UICONTROL Auto-redirect to Base URL] | 글로벌 | (단일 스토어 설정의 경우) 사이트에 끊어진 링크가 있으면 이 링크가 트래픽을 &quot;404 페이지를 찾을 수 없음&quot; 메시지가 있는 페이지가 아닌 기본 URL로 리디렉션합니다. 옵션: `No` / `Yes (302 Found)` / `Yes (301 Moved Permanently)` <br /><br />**_중요!_**&#x200B;다중 스토어 설정에 기본 URL로 자동 리디렉션을 사용하지 마십시오. |
| [!UICONTROL Catalog media URL format] | 글로벌 | 제품 및 범주에 할당된 URL 형식을 정의합니다. 옵션: <br />**[!UICONTROL Unique hash per image variant (Legacy mode)]**- 변환된 파일 이름을 고유한 해시 값으로 정의합니다.<br />**[!UICONTROL Image optimization based on query parameters]** - 쿼리 매개 변수에 따라 [이미지 최적화](../content-design/media-gallery-image-optimization.md) 프로세스를 정의합니다. |

{style="table-layout:auto"}
