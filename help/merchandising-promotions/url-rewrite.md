---
title: URL 재작성
description: URL 재작성에 대해 알아보고 Commerce URL 재작성 도구를 사용하여 제품, 카테고리 또는 CMS 페이지와 연결된 URL을 변경하는 방법에 대해 알아봅니다.
exl-id: 91e65f7f-7e33-4da5-b0a1-538ace56328a
feature: Categories, Products, Configuration
badgePaas: label="PaaS만" type="Informative" url="https://experienceleague.adobe.com/ko/docs/commerce/user-guides/product-solutions" tooltip="Adobe Commerce 온 클라우드 프로젝트(Adobe 관리 PaaS 인프라) 및 온프레미스 프로젝트에만 적용됩니다."
source-git-commit: 7e28081ef2723d4113b957edede6a8e13612ad2f
workflow-type: tm+mt
source-wordcount: '669'
ht-degree: 0%

---

# URL 재작성

>[!TIP]
>
>Adobe Commerce as a Cloud Service의 경우 Commerce Storefront 설명서에서 [SEO 지침](https://experienceleague.adobe.com/developer/commerce/storefront/setup/seo/indexing/?lang=ko)을 참조하십시오

URL 재작성 도구를 사용하면 제품, 카테고리 또는 CMS 페이지와 연결된 모든 URL을 변경할 수 있습니다. 다시 쓰기가 적용되면 이전 URL을 가리키는 모든 링크가 새 주소로 리디렉션됩니다.

>[!NOTE]
>
>여러 제품 또는 모든 제품에 대한 URL 재쓰기를 동시에 업데이트하려면 [여러 URL 재쓰기](url-rewrite-product.md#multiple-url-rewrites)를 참조하세요.

_다시 작성_&#x200B;과(와) _리디렉션_&#x200B;이라는 용어는 혼용되는 경우가 많지만 약간 다른 프로세스를 참조합니다. URL 재작성은 URL이 브라우저에 표시되는 방식을 변경합니다. URL 리디렉션은 서버에 저장된 URL을 업데이트합니다. URL 리디렉션은 임시적이거나 영구적일 수 있습니다. 스토어는 URL 재작성 및 리디렉션을 사용하여 제품, 카테고리 또는 페이지의 URL 키를 쉽게 변경하고 기존 링크를 유지할 수 있습니다.

기본적으로 스토어에 대해 [자동 URL 리디렉션](url-redirect-product-automatic.md)이 활성화되고 각 제품의 URL 키 필드 아래에서 **이전 URL에 대한 영구 리디렉션 만들기** 확인란이 선택됩니다.

{{url-rewrite-skip}}

{{url-rewrite-params}}

![검색 엔진 최적화 - 영구 URL 리디렉션 만들기](./assets/product-search-engine-optimization-create-permanent-redirect.png){width="600" zoomable="yes"}

## 표준 URL

SEO 목적으로, 은 각 웹 페이지에 하나의 고유 URL만 있는 것이 좋습니다.

여러 URL로 액세스할 수 있는 단일 페이지가 있거나 유사한 콘텐츠를 가진 서로 다른 페이지가 있는 경우 Google은 이러한 페이지를 동일한 페이지의 중복 버전으로 봅니다. Google은 하나의 URL을 표준 버전으로 선택하고 크롤링하며, 다른 모든 URL은 중복 URL로 간주되어 덜 자주 크롤링됩니다.

Google에 어떤 URL이 정식 URL인지 명시적으로 알리지 않는 경우, 자동으로 선택되거나 두 URL을 모두 동일한 가중치로 간주할 수 있습니다. 이로 인해 원치 않는 동작이 발생할 수 있으며, 비효율적인 크롤링 예산과 낮은 배포 백링크의 위험이 있습니다.

웹 사이트를 설정하는 방법에 따라 색인에는 다음을 포함한 여러 버전의 사이트가 있을 수 있습니다.

    https://www.example.com
    https://www.example.com/
    http://www.example.com
    https://example.com
    https://www.example.com/index.html

정식 페이지를 지정하려면 [Google Search Central 설명서](https://developers.google.com/search/docs/crawling-indexing/consolidate-duplicate-urls)를 참조하십시오.

## URL 재작성 구성

웹 서버 Apache 재작성 활성화는 초기 Commerce 설정의 일부입니다. Commerce에서는 일반적으로 URL 뒤에 표시되는 파일 이름 `index.php`을(를) 제거하기 위해 URL 재작성을 사용합니다. 웹 서버 다시 쓰기가 활성화되면 시스템은 각 URL을 다시 작성하여 `index.php`을(를) 생략합니다. 다시 쓰기는 검색 엔진 또는 고객에게 아무런 가치도 주지 않는 단어를 제거하며 성능이나 사이트 등급에 영향을 주지 않습니다.

웹 서버를 다시 작성하지 않은 URL

    http://www.yourdomain.com/magento/index.php/storeview/url-identifier

웹 서버 다시 쓰기가 포함된 URL

    http://www.yourdomain.com/magento/storeview/url-identifier

1. _관리자_ 사이드바에서 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**(으)로 이동합니다.

1. **[!UICONTROL General]**&#x200B;이(가) 확장된 왼쪽 패널에서 **[!UICONTROL Web]**&#x200B;을(를) 선택합니다.

1. **[!UICONTROL Search Engine Optimization]** 섹션에서 ![확장 선택기](../assets/icon-display-expand.png)를 확장합니다.

   ![일반 구성 - 웹 검색 엔진 최적화](../configuration-reference/general/assets/web-search-engine-optimization.png){width="600" zoomable="yes"}

1. **[!UICONTROL Use Web Server Rewrites]**&#x200B;을(를) 기본 설정으로 설정합니다.

1. 완료되면 **[!UICONTROL Save Config]**&#x200B;을(를) 클릭합니다.

## URL 재작성 만들기

URL 재작성 도구를 사용하여 스토어의 모든 페이지에 대한 제품 및 카테고리 재작성 및 사용자 정의 재작성을 만들 수 있습니다. 다시 쓰기가 적용되면 이전 URL을 가리키는 기존 링크는 새 주소로 원활하게 리디렉션됩니다.

URL 재작성은 가치가 높은 키워드를 추가하여 검색 엔진에서 제품이 색인화되는 방식을 개선하는 데 사용할 수 있습니다. 또한 재작성을 사용하여 임시 시즌 변경 또는 영구 변경에 대한 추가 URL을 만들 수도 있습니다. CMS 컨텐츠 페이지를 포함하여 모든 유효한 경로에 대해 재쓰기를 만들 수 있습니다. 내부적으로, 시스템은 항상 제품 및 범주를 해당 ID별로 참조합니다. URL이 얼마나 자주 변경되더라도 ID는 동일하게 유지됩니다. 다음은 URL 재작성을 사용할 수 있는 몇 가지 방법입니다.

시스템 URL

    http://www.example.com/catalog/category/id/6

원본 URL

    http://www.example.com/peripherals/keyboard.html

리디렉션된 제품 URL

    http://www.example.com/ergonomic-keyboard.html

추가 범주 URL

    http://www.example.com/all-on-sale.html
    http://www.example.com/save-now/spring-sale

![URL이 표 재작성](./assets/url-rewrites.png){width="700" zoomable="yes"}

Commerce은 다음과 같은 URL 재작성 유형을 제공합니다.

* [제품 리쓰기](url-rewrite-product.md)
* [범주 재작성](url-rewrite-category.md)
* [CMS 페이지 재작성](url-rewrite-cms-page.md)
* [사용자 지정 재작성](url-rewrite-custom.md)

## URL이 데모 재작성

이 비디오를 통해 URL 재작성 관리에 대해 알아보십시오.

>[!VIDEO](https://video.tv.adobe.com/v/3410127?quality=12&learn=on&captions=kor)
