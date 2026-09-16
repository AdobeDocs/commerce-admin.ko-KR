---
title: 검색어 리디렉션 및 Storefront 라우팅
description: Adobe Commerce 및 Edge Delivery Services용 배포로 검색어 리디렉션, URL 재작성, 라이브 검색 규칙 또는 상점 경로 지정을 선택하는 방법을 알아봅니다.
feature: Merchandising, Search
role: Admin, User
level: Intermediate
topic: Commerce, Administration
autotag-review: '2026-09-10T17:42:01.349Z'
TQID: 'https://experienceleague.adobe.com/Vxw3B0zOzLZfAm3qn8gJKHGSNtVhkN2Bfmcauhj0sdM'
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
    internal-label: Commerce
feature_v2:
  - id: d1e21356-0064-4f48-9089-16e3f0dbd2a6
    internal-label: Storefront
  - id: dac87252-6066-4d6e-a9d2-f6d84c323de7
    internal-label: Configuration
topic_v2:
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
    internal-label: Administration
source-git-commit: 67a00b294f1946da5795cd8fb7ea9fac1c80edcd
workflow-type: tm+mt
source-wordcount: '970'
ht-degree: 0%
---
# 검색어 리디렉션 및 상점 첫 화면 라우팅

검색어 리디렉션, URL 리디렉션 및 검색 머천다이징은 다양한 문제를 해결합니다. [!DNL Edge Delivery Services]에서 제공하는 표준 [!DNL Adobe Commerce] 검색, [!DNL Live Search] 및 [!DNL Commerce Storefront]에 적합한 기능을 선택하려면 이 안내서를 사용하십시오.

## 리디렉션 유형 이해

이러한 기능은 동작을 트리거하는 항목과 쇼핑객이 보는 항목에서 다릅니다.

* **검색어 리디렉션**&#x200B;은(는) 특정 검색어를 입력한 쇼핑객을 지정된 페이지로 보냅니다.

* **URL 리디렉션**&#x200B;은(는) 일반적으로 HTTP 301 또는 302 응답을 사용하여 이전 URL에 대한 요청을 새 URL로 보냅니다. 브라우저 주소 표시줄이 새 URL로 변경됩니다.

* **머천다이징 검색** 요청된 URL을 변경하지 않고 검색 결과에 나타나는 제품 또는 순서를 변경합니다.

* **URL 다시 작성**&#x200B;은(는) 한 URL을 서버의 다른 URL에 매핑합니다. [!DNL Adobe Commerce] URL 다시 작성 도구는 이전 URL에 대한 영구 리디렉션(301)을 만듭니다. 자세한 내용은 [URL 다시 쓰기](url-rewrite.md)를 참조하십시오.

## 라우팅 기능 선택

다음 지침을 사용하여 요구 사항과 일치하는 기능을 식별합니다.

| 요구 사항 | 권장 기능 |
| --- | --- |
| 표준 [!DNL Adobe Commerce] 검색에서 페이지로 특정 쿼리 보내기 | 지원되는 경우 [검색어 관리](../catalog/search-terms.md)에서 검색어를 구성하십시오. |
| 제품 순위 또는 검색 결과의 가시성 변경 | [!DNL Live Search] [동의어](https://experienceleague.adobe.com/en/docs/commerce/live-search/live-search-admin/synonyms/synonyms) 또는 [머천다이징 규칙](https://experienceleague.adobe.com/en/docs/commerce/live-search/live-search-admin/rules/rules-add)을 사용하십시오. |
| 이전 제품, 카테고리 또는 CMS URL 리디렉션 | 배포에 적용되는 경우 Commerce [URL 다시 작성](url-rewrite.md) 도구를 사용하십시오. |
| [!DNL Edge Delivery Services] 경로 리디렉션 | Storefront 또는 CDN 라우팅을 사용합니다. |
| Storefront 마이그레이션 후 기존 URL 유지 | 기존-새 URL 리디렉션 맵을 만들고 테스트합니다. |

## 표준 Commerce 검색

표준 카탈로그 검색을 사용하면 검색어를 구성하여 배포에서 이 기능을 지원하는 콘텐츠 페이지, 카테고리 페이지, 제품 페이지 또는 외부 페이지를 열 수 있습니다. 쇼핑객이 입력한 쿼리(예: `gift cards` 또는 `returns`)가 캠페인 또는 정보 페이지를 열어야 할 때 사용합니다.

이 유형의 리디렉션을 만들거나 업데이트하려면 [검색어 관리](../catalog/search-terms.md)를 참조하십시오. 트리거가 기존 URL이 아닌 구매자 쿼리이므로 검색어 구성은 URL 재작성 도구와 별개입니다.

>[!NOTE]
>
>Storefront가 표준 카탈로그 검색을 사용하고 기본 검색어 리디렉션을 지원하는지 확인합니다. 동작 및 사용 가능한 구성은 [!DNL Live Search], [!DNL Adobe Commerce as a Cloud Service] 또는 Headless Storefront에 따라 다를 수 있습니다.

## URL 리디렉션 및 재작성

소스가 구매자가 입력한 검색어가 아닌 기존 URL인 경우 URL 재작성을 사용하십시오. 일반적인 예로는 리디렉션이 있습니다.

* 이전 제품 URL과 새 제품 URL.

* 대체 범주 URL에 대한 폐기된 범주 URL.

* 새 컨텐츠 페이지 URL에 대한 오래된 CMS 페이지 URL입니다.

URL 다시 작성 도구를 지원하는 배포의 경우 **[!UICONTROL Marketing]** > **[!UICONTROL SEO & Search]** > **[!UICONTROL URL Rewrites]**(으)로 이동하여 리디렉션을 만드십시오. 단계별 지침은 [URL 다시 쓰기](url-rewrite.md)를 참조하십시오.

>[!NOTE]
>
>[URL 재작성](url-rewrite.md) 항목은 PaaS에만 적용됩니다. [!DNL Adobe Commerce as a Cloud Service] 또는 [!DNL Edge Delivery Services] Storefront의 경우 해당 Storefront에 대한 라우팅 지침을 대신 사용하십시오.

## 라이브 검색

[!DNL Live Search]은(는) 기본 Storefront 검색 환경을 대체하며 동의어, 패싯 및 머천다이징 규칙과 같은 기능을 제공합니다.

검색 관련성, 제품 순위 또는 제품 가시성을 변경해야 하는 경우 [!DNL Live Search]을(를) 사용하십시오. 다른 단어가 유사한 제품을 반환해야 할 때 동의어를 사용하십시오. 제품을 부스팅하거나, 묻거나, 다른 등급으로 매겨야 하는 경우 머천다이징 규칙을 사용합니다.

[!DNL Live Search] 검색 동작은 모든 기본 Commerce 검색어 구성에 대해 드롭인 대체 항목으로 간주해서는 안 됩니다. 쿼리가 콘텐츠 또는 캠페인 페이지로 이동해야 하는 경우 요청을 수신하는 상점 또는 에지 라우팅 계층에서 리디렉션을 구현합니다. 자세한 내용은 [[!DNL Live Search] 설명서](https://experienceleague.adobe.com/en/docs/commerce/live-search/overview)를 참조하세요.

## Edge Delivery Services

[!DNL Edge Delivery Services]에서 제공하는 Storefront의 경우 Storefront 또는 Edge-routing 계층에서 리디렉션을 관리합니다. [!DNL Adobe Commerce] 관리자 URL이 모든 요청에 대한 제어를 다시 작성한다고 가정하지 마십시오.

문서 작성을 사용하는 경우 사이트의 리디렉션 구성에서 리디렉션 매핑을 유지 관리합니다. 요청이 원본에 도달하기 전에 실행해야 하는 리디렉션의 경우 적절한 CDN 또는 Edge 구성을 사용하십시오. 관련 SEO 지침은 [Commerce Storefront에 대한 SEO 지침](https://experienceleague.adobe.com/developer/commerce/storefront/setup/seo/indexing/)을 참조하세요.

## Luma에서 마이그레이션

리디렉션 마이그레이션을 Storefront 마이그레이션의 일부로 처리합니다. 고객 여정과 SEO 의도를 유지한 다음 대상 상점에 대한 라우팅을 다시 구현합니다.

트래픽을 새 상점 전면으로 전환하기 전에:

1. 기존 Luma URL 및 검색어 랜딩 페이지를 내보내고 인벤토리를 수행합니다.

1. 각 항목을 검색어 리디렉션, URL 리디렉션 또는 머천다이징 규칙으로 분류합니다.

1. 모든 기존 URL을 새 상점 경로에 매핑합니다.

1. 요청을 수신하는 계층에서 각 리디렉션을 구현합니다.

1. 상태 코드, 쿼리 매개 변수, 표준 URL, 로케일 경로 및 리디렉션 루프를 테스트합니다.

1. 실행 후 로그 및 분석에서 확인되지 않은 기존 URL을 모니터링합니다.

## 리디렉션 문제 해결

[!DNL Adobe Commerce] 검색, 상점 라우팅 및 저장소 보기에서 리디렉션이 예상대로 작동하지 않을 때 다음 검사를 사용하십시오.

| 문제 | 확인할 사항 |
| --- | --- |
| 검색어가 리디렉션되지 않음 | 상점이 표준 카탈로그 검색을 사용하고, 검색 쿼리가 구성된 용어와 일치하며, 검색어가 올바른 스토어 보기에 할당되었는지 확인합니다. [!DNL Live Search]이(가) 활성화된 경우 리디렉션이 상점 또는 에지 레이어에 구현되었는지 확인하십시오. |
| 리디렉션은 Luma에서 작동하지만 Edge Delivery Services에서는 작동하지 않습니다. | [!DNL Edge Delivery Services] 상점 또는 CDN 라우팅 계층에 리디렉션이 구성되어 있는지 확인합니다. [!DNL Adobe Commerce] 관리자 URL 재작성은 요청을 받지 못할 수 있습니다. |
| 라이브 검색은 리디렉션 대신 결과를 반환합니다. | 제품 순위 및 가시성에 [!DNL Live Search] 규칙을 사용합니다. 콘텐츠 또는 캠페인 페이지로 탐색하려면 상점 또는 Edge 레이어에서 리디렉션을 구성합니다. |
| 리디렉션은 하나의 스토어 보기에서 작동하지만 다른 스토어 보기에서는 작동하지 않습니다 | 검색어 또는 URL 규칙에 지정된 스토어 보기를 확인합니다. 영향을 받는 각 저장소 보기에서 전체 로케일 경로 및 쿼리를 테스트합니다. |

## 이 항목에 대한 추가 도움말

* [SEO 개요 및 우수 사례](seo-overview.md)

* [가게 앞이 뭐죠?](../getting-started/storefront.md)

* [검색어 관리](../catalog/search-terms.md)

* [URL 재작성](url-rewrite.md)
