---
title: URL 재작성
description: URL 재작성에 대해 알아보고 Commerce URL 재작성 도구를 사용하여 제품, 카테고리 또는 CMS 페이지와 연결된 URL을 변경하는 방법에 대해 알아봅니다.
exl-id: 91e65f7f-7e33-4da5-b0a1-538ace56328a
feature: Categories, Products, Configuration
badgePaas: label="PaaS만" type="Informative" url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="Adobe Commerce 온 클라우드 프로젝트(Adobe 관리 PaaS 인프라) 및 온프레미스 프로젝트에만 적용됩니다."
source-git-commit: 2f2db4926ff92adfa27692eeca872c1765fd31d6
workflow-type: tm+mt
source-wordcount: '905'
ht-degree: 0%

---

# URL 재작성

>[!TIP]
>
>Adobe Commerce as a Cloud Service의 경우 Commerce Storefront 설명서에서 [SEO 지침](https://experienceleague.adobe.com/developer/commerce/storefront/setup/seo/indexing/)을 참조하십시오

URL 재작성 도구를 사용하면 제품, 카테고리 또는 CMS 페이지와 연결된 모든 URL을 변경할 수 있습니다. URL 재작성을 만들 때, Commerce은 자동으로 영구 리디렉션을 만들기(301)하므로 이전 URL을 가리키는 모든 링크는 새 주소로 리디렉션됩니다.

>[!NOTE]
>
>여러 제품 또는 모든 제품에 대한 URL 재쓰기를 동시에 업데이트하려면 [여러 URL 재쓰기](url-rewrite-product.md#multiple-url-rewrites)를 참조하세요.

>[!BEGINSHADEBOX &quot;다시 쓰기 및 리디렉션 이해&quot;]

_다시 작성_&#x200B;과(와) _리디렉션_&#x200B;이라는 용어가 서로 바꿔서 사용되는 경우가 많지만, 서로 다른 작업입니다.

* **URL 다시 작성** — 브라우저의 주소 표시줄에 나타나는 내용을 변경하지 않고 한 URL을 내부적으로 다른 URL에 매핑하는 서버측 프로세스입니다. 방문자가 URL을 요청하면 서버는 이 URL을 백그라운드에서 다른 URL로 처리하지만 브라우저는 원본 URL을 계속 표시합니다.

* **URL 리디렉션** — 다른 URL로 이동하라는 HTTP 응답을 브라우저에 보냅니다. 브라우저의 주소 표시줄이 업데이트되어 새 URL이 표시됩니다. 리디렉션은 임시(302) 또는 영구(301)일 수 있습니다.

>[!ENDSHADEBOX]

## 재작성 도구 작동 방식

Adobe Commerce에서 URL 재작성 도구는 제품, 카테고리 또는 페이지의 URL 키를 변경할 때 SEO 값을 유지하기 위해 기본적으로 영구 리디렉션(301)을 만듭니다. 이 비헤이비어는 기존 링크가 계속 작동하고 검색 엔진 순위가 유지되도록 합니다.

기본적으로 스토어에 대해 [자동 URL 리디렉션](url-redirect-product-automatic.md)이 활성화되고 각 제품의 URL 키 필드 아래에서 **이전 URL에 대한 영구 리디렉션 만들기** 확인란이 선택됩니다.

{{url-rewrite-skip}}

![검색 엔진 최적화 - 영구 URL 리디렉션 만들기](./assets/product-search-engine-optimization-create-permanent-redirect.png){width="600" zoomable="yes"}

{{url-rewrite-params}}

## URL이 데모 재작성

다음 비디오를 통해 URL 재작성 관리에 대해 알아보십시오.

>[!VIDEO](https://video.tv.adobe.com/v/343751?quality=12&learn=on)

## URL 재작성 만들기

URL 재작성 도구를 사용하여 스토어의 모든 페이지에 대한 제품 및 카테고리 리디렉션 및 사용자 지정 리디렉션을 만듭니다. URL 재작성 구성이 적용되면 이전 URL을 가리키는 기존 링크는 새 주소로 원활하게 리디렉션됩니다.

다음 위치에 URL 재작성을 만들 수 있습니다.

* 가치가 높은 키워드를 추가하여 검색 엔진에서 제품이 색인화되는 방식을 개선합니다.

* 임시 시즌 변경 또는 영구 변경에 대한 추가 URL을 추가합니다.

* CMS 컨텐츠 페이지를 포함한 페이지에 대한 유효한 경로를 추가합니다. 예를 들어, 내부 ID로 제품과 카테고리를 항상 참조하는 시스템에 더 많은 사용자 URL 또는 SEO에 친숙한 URL을 만들기 위한 URL을 만들 수 있습니다.

사용자가 만드는 URL 재작성은 사이트 구조를 변경하지 않고 기존 카테고리 또는 사용자 지정 페이지로 리디렉션할 수 있으므로 마케팅 캠페인에 기억할 수 있는 URL을 쉽게 만들 수 있습니다.

![URL이 표 재작성](./assets/url-rewrites.png){width="700" zoomable="yes"}

Commerce은 다음과 같은 URL 재작성 유형을 제공합니다.

* [제품 리쓰기](url-rewrite-product.md)
* [범주 재작성](url-rewrite-category.md)
* [CMS 페이지 재작성](url-rewrite-cms-page.md)
* [사용자 지정 재작성](url-rewrite-custom.md)

### 사용 사례 및 예

URL 재작성은 일반적으로 다음 시나리오에서 사용됩니다.

#### 내부 시스템 URL을 SEO에 친숙한 URL로 변경

Commerce은 내부적으로 ID 기반 URL을 사용하지만 고객을 위해 SEO에 친숙한 URL을 만들 수 있습니다.

**시스템 URL(내부):**

    http://www.example.com/catalog/category/id/6

**고객 응대 URL:**

    http://www.example.com/peripherals/keyboard.html

#### 제품 리브랜딩 또는 URL 최적화

제품 이름을 바꾸거나 SEO용 URL을 개선하려는 경우 기존 링크를 유지하는 리디렉션을 만듭니다.

**원본 URL:**

    http://www.example.com/peripherals/keyboard.html

**새로 최적화된 URL:**

    http://www.example.com/ergonomic-keyboard.html

재작성 도구는 이전 URL에서 새 URL로 301 리디렉션을 자동으로 만들기 때문에 고객과 검색 엔진이 원활하게 올바른 페이지로 이동됩니다.

#### 프로모션 랜딩 페이지

마케팅 캠페인에 대한 임시 또는 영구 사용자 지정 URL 만들기:

**프로모션 URL:**

    http://www.example.com/all-on-sale.html
    http://www.example.com/save-now/spring-sale

## 추가 URL 관리 구성

다음 섹션에서는 Commerce에 대해 웹 서버 재작성 및 표준 URL을 구성하는 방법을 설명합니다.

### 웹 서버 재작성 구성

>[!NOTE]
>
>이 섹션에서는 URL 재작성 도구 기능과는 다른 웹 서버 수준의 URL 재작성에 대해 설명합니다. 웹 서버 다시 쓰기는 기술 URL 서식을 처리하는(예: `index.php` 제거) 반면, URL 다시 쓰기 도구는 콘텐츠 변경 내용에 대한 리디렉션을 관리합니다.

웹 서버 재작성 활성화는 초기 Commerce 설정의 일부이며 일반적으로 설치 중에 구성됩니다. 사용하도록 설정하면 웹 서버(Apache 또는 Nginx)가 URL에서 파일 이름 `index.php`을(를) 자동으로 제거하여 보다 깔끔하고 SEO에 친숙한 주소를 만듭니다.
다음 예에서는 웹 서버 재쓰기를 사용하는 경우와 사용하지 않는 경우에 URL이 표시되는 방식을 보여 줍니다.

**웹 서버를 다시 작성하지 않은 URL**

    http://www.yourdomain.com/magento/index.php/storeview/url-identifier

**웹 서버 다시 쓰기가 포함된 URL**

    http://www.yourdomain.com/magento/storeview/url-identifier

#### 웹 서버 재작성 활성화 또는 비활성화:

1. _관리자_ 사이드바에서 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**(으)로 이동합니다.

1. **[!UICONTROL General]**&#x200B;이(가) 확장된 왼쪽 패널에서 **[!UICONTROL Web]**&#x200B;을(를) 선택합니다.

1. ![ 섹션에서 ](../assets/icon-display-expand.png)확장 선택기&#x200B;**[!UICONTROL Search Engine Optimization]**&#x200B;를 확장합니다.

   ![일반 구성 - 웹 검색 엔진 최적화](../configuration-reference/general/assets/web-search-engine-optimization.png){width="600" zoomable="yes"}

1. **[!UICONTROL Use Web Server Rewrites]**&#x200B;을(를) 기본 설정으로 설정합니다.

1. 완료되면 **[!UICONTROL Save Config]**&#x200B;을(를) 클릭합니다.

### 정식 URL 지정

SEO를 위해 각 웹 페이지에는 하나의 고유한 URL만 있어야 합니다.

여러 URL로 액세스할 수 있는 단일 페이지가 있거나 유사한 콘텐츠를 가진 서로 다른 페이지가 있는 경우 Google은 이러한 페이지를 동일한 페이지의 중복 버전으로 봅니다. Google은 하나의 URL을 표준 버전으로 선택하고 크롤링하며, 다른 모든 URL은 중복 URL로 간주되고 덜 자주 크롤링됩니다.

Google에 어떤 URL이 정식 URL인지 명시적으로 알리지 않는 경우, 자동으로 선택되거나 두 URL을 모두 동일한 가중치로 간주할 수 있습니다. 이로 인해 원치 않는 동작이 발생할 수 있으며 비효율적인 크롤링 예산과 낮은 배포 백링크가 위험합니다.

웹 사이트를 설정하는 방법에 따라 색인에 다음과 같은 여러 버전의 사이트가 있을 수 있습니다.

    https://www.example.com
    https://www.example.com/
    http://www.example.com
    https://example.com
    https://www.example.com/index.html

정식 페이지를 지정하려면 [Google Search Central 설명서](https://developers.google.com/search/docs/crawling-indexing/consolidate-duplicate-urls)를 참조하십시오.
