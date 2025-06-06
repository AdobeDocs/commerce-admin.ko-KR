---
title: '[!UICONTROL Catalog] &gt; [!UICONTROL Catalog]'
description: Commerce 관리자의 [!UICONTROL Catalog] &gt; [!UICONTROL Catalog] 페이지에서 구성 설정을 검토하십시오.
exl-id: fc25ae80-aaa7-42c4-bba2-f03d3caa7970
feature: Configuration, Catalog Management
source-git-commit: 20f97d6ab391b7f5675d6790ab2ec5d24e9dda21
workflow-type: tm+mt
source-wordcount: '3261'
ht-degree: 0%

---

# [!UICONTROL Catalog] > [!UICONTROL Catalog]

{{config}}

## [!UICONTROL Product Fields Auto-Generation]

![제품 필드 자동 생성](./assets/catalog-product-fields-auto-generation.png)<!-- zoom -->

<!-- [Product Fields Auto-Generation](https://experienceleague.adobe.com/ko/docs/commerce-admin/catalog/products/product-workspace#default-field-values) -->

| 필드 | [범위](../../getting-started/websites-stores-views.md#scope-settings) | 설명 |
|--- |--- |--- |
| [!UICONTROL Mask for SKU] | 글로벌 | 다른 필드의 자리 표시자 값과 입력된 추가 텍스트를 기반으로 SKU 필드의 기본값을 결정합니다. 기본 자리 표시자: <br/>제품 이름 - `{{name}}` |
| [!UICONTROL Mask for Meta Title] | 글로벌 | 다른 필드의 자리 표시자 값 및 입력된 추가 텍스트를 기반으로 메타 제목 필드의 기본값을 결정합니다. 기본 자리 표시자: <br/>제품 이름 - `{{name}}` |
| [!UICONTROL Mask for Meta Keywords] | 글로벌 | 다른 필드의 자리 표시자 값 및 입력된 추가 텍스트를 기반으로 _메타 키워드_ 필드의 기본값을 결정합니다. 기본 자리 표시자: <br/>제품 이름 - `{{name}}` |
| [!UICONTROL Mask for Meta Description] | 글로벌 | 다른 필드의 자리 표시자 값 및 입력된 추가 텍스트를 기반으로 메타 설명 필드의 기본값을 결정합니다. 기본 자리 표시자: <br/>제품 이름 - `{{name}}` <br/>설명 - `{{description}}` |

{style="table-layout:auto"}

## [!UICONTROL Product Reviews]

![제품 리뷰](./assets/catalog-product-reviews.png)<!-- zoom -->

<!-- [Product Reviews](https://experienceleague.adobe.com/ko/docs/commerce-admin/marketing/merchandising/product-reviews/product-reviews) -->

| 필드 | [범위](../../getting-started/websites-stores-views.md#scope-settings) | 설명 |
|--- |--- |--- |
| [!UICONTROL Enabled] | 스토어 뷰 | 제품 검토를 활성화합니다. 옵션: `Yes` / `No` |
| [!UICONTROL Allow Guests to Write Reviews] | 웹 사이트 | 고객이 제품 리뷰를 작성할 수 있도록 스토어에 계정을 열어야 하는지 여부를 결정합니다. |

{style="table-layout:auto"}

## [!UICONTROL Storefront]

![Storefront](./assets/catalog-storefront.png)<!-- zoom -->

<!-- [Storefront](https://experienceleague.adobe.com/ko/docs/commerce-admin/catalog/catalog/navigation/navigation-product-listings) -->

| 필드 | [범위](../../getting-started/websites-stores-views.md#scope-settings) | 설명 |
|--- |--- |--- |
| [!UICONTROL List Mode] | 스토어 뷰 | 검색 결과 목록의 형식을 결정합니다. 옵션: <br/>**`Grid Only`**- 행 및 열 그리드로 목록 서식을 지정합니다. 각 제품은 그리드의 단일 셀에 나타납니다.<br/>**`List Only`** - 각 제품이 있는 목록의 서식을 별도의 행에 지정합니다. <br/>**`Grid (default / List)`**- 기본적으로 제품은 눈금 보기에 표시되며 목록 보기로 전환할 수 있습니다.<br/>**`List (default / Grid)`** - 기본적으로 제품은 목록 보기에 나타나며 눈금 보기로 전환할 수 있습니다. |
| [!UICONTROL Products per Page on Grid Allowed Values] | 스토어 뷰 | 눈금 보기에 표시되는 제품 수를 결정합니다. 옵션을 선택하려면 쉼표로 구분된 여러 값을 입력하십시오. |
| [!UICONTROL Products per Page on Grid Default Value] | 스토어 뷰 | 그리드 보기에서 기본적으로 페이지당 표시되는 제품 수를 결정합니다. |
| [!UICONTROL Products per Page on List Allowed Values] | 스토어 뷰 | 목록 보기에 표시되는 제품의 수를 결정합니다. 옵션을 선택하려면 쉼표로 구분된 여러 값을 입력하십시오. |
| [!UICONTROL Products per Page on List Default Value] | 스토어 뷰 | 목록 보기에서 기본적으로 페이지당 표시되는 제품 수를 결정합니다. |
| 제품 목록 정렬 기준 | 스토어 뷰 | 검색 결과 목록의 정렬 순서를 결정합니다. 범주의 [표시 설정]과 `Used for Sorting in Product Listing`(으)로 설정된 사용 가능한 특성에 따라 옵션 선택이 결정됩니다. 기본값은 `Use All Available Attributes`(으)로 설정되며 일반적으로 가장 적합한 값, 이름, 가격을 포함합니다. 이 설정은 [!DNL Live Search] [제품 목록 페이지 위젯](https://experienceleague.adobe.com/ko/docs/commerce/live-search/live-search-storefront/plp-styling)에 적용되지 않습니다. |
| [!UICONTROL Allow All Products per Page] | 스토어 뷰 | `Yes`(으)로 설정된 경우 &quot;페이지당 표시&quot; 컨트롤에 `ALL` 옵션을 포함합니다. |
| [!UICONTROL Remember Category Pagination] | 글로벌 | `Yes`(으)로 설정하면 고객이 [제품 목록](../../catalog/navigation-product-listings.md)에서 한 범주에서 다른 범주로 탐색할 때 현재 범주 페이지 매김 값이 저장됩니다. 값을 저장하면 더 많은 캐시 저장소를 사용하며 검색 엔진이 페이지를 인덱싱하는 방식에 영향을 줄 수 있습니다. 옵션: `Yes` / `No`(기본값) |
| [!UICONTROL Use Flat Catalog Category] | 글로벌 | [단순 범주 구조](../../catalog/catalog-flat.md)를 사용하도록 설정합니다(권장하지 않음). 옵션: `Yes` / `No` |
| [!UICONTROL Use Flat Catalog Product] | 글로벌 | 플랫 제품 구조를 활성화합니다. (권장되지 않음) 옵션: `Yes` / `No` |
| [!UICONTROL Swatches per Product] | 스토어 뷰 | 각 제품에 사용할 수 있는 견본 수를 결정합니다. 기본값: `16` |
| [!UICONTROL Show Swatches in Product List] | 스토어 뷰 | 견본이 제품 목록에 표시되는지 여부를 결정합니다. 옵션: `Yes` / `No` |
| [!UICONTROL Show Swatch Tooltip] | 스토어 뷰 | 견본 도구 설명이 표시되는지 여부를 결정합니다. 옵션: `Yes` / `No` |

{style="table-layout:auto"}

## [!UICONTROL Product Alerts]

![제품 알림](./assets/catalog-product-alerts.png)<!-- zoom -->

<!-- [Product Alerts](https://experienceleague.adobe.com/ko/docs/commerce-admin/inventory/configuration/product-alerts/alert-setup) -->

| 필드 | [범위](../../getting-started/websites-stores-views.md#scope-settings) | 설명 |
|--- |--- |--- |
| [!UICONTROL Allow Alerts When Product Price Changes] | 스토어 뷰 | 제품 가격 변경에 이메일 경고를 사용할 수 있는지 여부를 결정합니다. 옵션: `Yes` / `No` |
| [!UICONTROL Price Alert Email Template] | 스토어 뷰 | 제품 가격 변경 이메일 경고에 사용되는 템플릿을 식별합니다. 기본 템플릿: `Product price alert` |
| [!UICONTROL Allow Alert When Product Comes Back in Stock] | 웹 사이트 | 제품이 재입고될 때 고객이 경고를 받도록 선택할 수 있는지 여부를 결정합니다. 옵션: `Yes` / `No` |
| [!UICONTROL Stock Alert Email Template] | 스토어 뷰 | 스톡 경고 이메일 알림에 사용되는 템플릿을 식별합니다. 기본 템플릿: `Product stock alert` |
| [!UICONTROL Alert Email Sender] | 스토어 뷰 | 제품 경고 이메일 메시지의 발신자로 표시되는 스토어 연락처를 결정합니다. 옵션: `General Contact` / `Sales Representative` / `Customer Support` / `Custom Email` |

{style="table-layout:auto"}

## [!UICONTROL Product Alerts Run Settings]

![제품 경고 실행 설정](./assets/catalog-product-alerts-run-settings.png)<!-- zoom -->

<!-- [Product Alerts Run Settings](https://experienceleague.adobe.com/ko/docs/commerce-admin/inventory/configuration/product-alerts/alert-setup) -->

| 필드 | [범위](../../getting-started/websites-stores-views.md#scope-settings) | 설명 |
|--- |--- |--- |
| [!UICONTROL Frequency] | 글로벌 | 제품 경고를 보내는 빈도를 선택합니다. 옵션: `Daily` / `Weekly` / `Monthly` |
| [!UICONTROL Start Time] | 글로벌 | 제품 경고 프로세스가 시작되는 시간대를 선택합니다. 이 시간은 가격 또는 재고 업데이트가 수행된 후여야 합니다. |
| [!UICONTROL Error Email Recipient] | 글로벌 | 제품 경고 프로세스에 오류가 있을 때 이메일 알림을 받아야 하는 사람(일반적으로 스토어 관리자)의 이메일 주소를 식별합니다. |
| [!UICONTROL Error Email Sender] | 글로벌 | 전자 메일이 `from`인 역할을 선택하십시오. |
| [!UICONTROL Error Email Template] | 글로벌 | 제품 경고 오류 알림에 사용할 이메일 템플릿을 선택합니다. |

{style="table-layout:auto"}

## [!UICONTROL Product Image Placeholders]

![제품 이미지 자리 표시자](./assets/catalog-product-image-placeholders.png)<!-- zoom -->

<!-- [Product Image Placeholders](https://experienceleague.adobe.com/ko/docs/commerce-admin/catalog/products/digital-assets/product-image-config#image-placeholders) -->

| 필드 | [범위](../../getting-started/websites-stores-views.md#scope-settings) | 설명 |
|--- |--- |--- |
| [!UICONTROL Base Image] | 스토어 뷰 | 기본 이미지에 대해 선택한 자리 표시자 파일을 식별합니다. |
| [!UICONTROL Small Image] | 스토어 뷰 | 작은 이미지에 대해 선택한 자리 표시자 파일을 식별합니다. |
| [!UICONTROL Swatch] | 스토어 뷰 | 견본에 대해 선택한 자리 표시자 파일을 식별합니다. |
| [!UICONTROL Thumbnail] | 스토어 뷰 | 썸네일에 대해 선택한 자리 표시자 파일을 식별합니다. |
| [!UICONTROL Choose File] |  | 파일로 이동하여 해당 유형의 자리 표시자 이미지로 업로드합니다. |

{style="table-layout:auto"}

## [!UICONTROL Recently Viewed/Compared Products]

![최근에 본 제품/비교한 제품](./assets/catalog-recently-viewed-and-compared-products.png)<!-- zoom -->

<!-- Recently Viewed/Compared Products](https://experienceleague.adobe.com/ko/docs/commerce-admin/stores-sales/shopper-tools/products-viewed-compared) -->

| 필드 | [범위](../../getting-started/websites-stores-views.md#scope-settings) | 설명 |
|--- |--- |--- |
| [!UICONTROL Synchronize widget products with backend storage] | 글로벌 | 제품 ID와 같은 제품 위젯 정보와 데이터베이스의 동기화를 결정합니다. 이를 통해 다른 디바이스에서 정보를 재사용할 수 있습니다. |
| [!UICONTROL Show for Current] | 웹 사이트 | 표시되는 제품을 현재 웹 사이트로 제한합니다. 옵션: `Website` / `Store` / `Store View` |
| [!UICONTROL Default Recently Viewed Products Count] | 스토어 뷰 | 목록에 나타나는 최근에 본 제품의 최대 수를 결정합니다. |
| [!UICONTROL Default Recently Compared Products Count] | 스토어 뷰 | 목록에 나타나는 최근에 비교한 제품의 최대 수를 결정합니다. |
| [!UICONTROL Lifetime of products in Recently Viewed Widget] | 글로벌 | 최근에 본 목록에 표시된 제품이 표시되는 시간을 초 단위로 결정합니다. |
| [!UICONTROL Lifetime of products in Recently Compared Widget] | 글로벌 | 최근 비교 목록에 비교된 제품이 표시되는 기간(초)을 결정합니다. |

{style="table-layout:auto"}

## [!UICONTROL Product Video]

![제품 비디오](./assets/catalog-product-video.png)<!-- zoom -->

<!-- [Product Videos](https://experienceleague.adobe.com/ko/docs/commerce-admin/catalog/products/digital-assets/product-video) -->

| 필드 | [범위](../../getting-started/websites-stores-views.md#scope-settings) | 설명 |
|--- |--- |--- |
| [!UICONTROL YouTube API key] | 스토어 뷰 | YouTube 서버에 연결하는 데 필요한 API 키를 지정합니다. |
| [!UICONTROL Autostart base video] | 스토어 뷰 | 페이지가 로드된 후 비디오를 자동으로 시작하려면 `Yes`(으)로 설정합니다. |
| [!UICONTROL Show related video] | 스토어 뷰 | 관련 비디오를 표시하려면 `Yes`(으)로 설정하십시오. |
| [!UICONTROL Auto restart video] | 스토어 뷰 | 비디오 자동 재생을 사용하려면 `Yes`(으)로 설정합니다. |

{style="table-layout:auto"}

## [!UICONTROL Price]

![가격](./assets/catalog-price.png)<!-- zoom -->

<!--Price](https://experienceleague.adobe.com/ko/docs/commerce-admin/catalog/products/pricing/catalog-price-scope) -->

| 필드 | [범위](../../getting-started/websites-stores-views.md#scope-settings) | 설명 |
|--- |--- |--- |
| [!UICONTROL Catalog Price Scope] | 글로벌 | 기본 통화의 범위를 결정합니다. 옵션: `Global` / `Website` |
| [!UICONTROL Default Product Price] | 글로벌 | ![Adobe Commerce](../../assets/adobe-logo.svg)(Adobe Commerce만 해당) 해당하는 경우 기본 제품 가격을 정의합니다. |

{style="table-layout:auto"}

## [!UICONTROL Layered Navigation]

>[!NOTE]
>
>이 섹션에 설명된 표준 검색 구성은 [실시간 검색](https://experienceleague.adobe.com/docs/commerce/live-search/overview.html?lang=ko)에 따라 다릅니다.

<!-- [Layered Navigation - Automatic (equalize price ranges)](https://experienceleague.adobe.com/ko/docs/commerce-admin/catalog/catalog/navigation/navigation-layered#configure-layered-navigation) -->

![계층화된 탐색 - 자동(가격 범위 조정)](./assets/layered-navigation-equalize-price-range.png)<!-- zoom -->

![계층화된 탐색 - 자동(제품 개수 균등화)](./assets/layered-navigation-equalize-product-counts.png)<!-- zoom -->

![계층화된 탐색 - 수동](./assets/layered-navigation-manual.png)<!-- zoom -->

| 필드 | [범위](../../getting-started/websites-stores-views.md#scope-settings) | 설명 |
|--- |--- |--- |
| [!UICONTROL Display Product Count] | 스토어 뷰 | 각 속성, 가격 범위 및 범주 뒤에 제품 카운트가 표시되는지 여부를 결정합니다. 옵션: `Yes` / `No` |
| [!UICONTROL Price Navigation Step Calculation] | 스토어 뷰 | [가격 탐색 단계](../../catalog/navigation-layered.md#configure-price-navigation))를 결정하는 데 사용되는 방법을 결정합니다. 옵션: <br/>`Automatic (equalize price ranges)` - 그룹 내 제품의 가격 범위를 기준으로 합니다. <br/>`Automatic (equalize product counts)` - 그룹 내 제품 수를 기준으로 계산합니다. 그룹의 최소 제품 수에 대한 임계값을 설정하여 더 작은 그룹으로 나누어지지 않도록 합니다. <br/>`Manual` - 가격 간격에 입력한 나누기 제한을 사용합니다. |
| [!UICONTROL Default Price Navigation Step] | 스토어 뷰 | 각 단계에 포함되는 제품 수를 결정합니다. |
| [!UICONTROL Maximum Number of Price Intervals] | 스토어 뷰 | 레이어 탐색에 나타나는 가격 간격 수에 대한 제한을 설정합니다. |

{style="table-layout:auto"}

## [!UICONTROL Category Permissions]

{{ee-feature}}

![범주 권한](./assets/catalog-category-permissions.png)<!-- zoom -->

<!-- [Category Permissions](https://experienceleague.adobe.com/ko/docs/commerce-admin/catalog/categories/category-permissions) -->

| 필드 | [범위](../../getting-started/websites-stores-views.md#scope-settings) | 설명 |
|--- |--- |--- |
| [!UICONTROL Enable] | 글로벌 | 범주 제한을 활성화합니다. 기본적으로 이 기능을 사용하면 모든 카테고리가 제한됩니다. 옵션: `Yes` / `No` |
| [!UICONTROL Allow Browsing Category] | 웹 사이트 | 범주 탐색을 허용할 사용자를 결정합니다. 옵션: <br/>`Yes, for Everyone` - 모든 방문자와 고객이 범주를 검색할 수 있도록 허용합니다. <br/>`Yes, for Specified Customer Groups` - 선택한 고객 그룹의 구성원만 범주를 탐색할 수 있습니다. <br/>`No, Redirect to Landing Page` - 범주 액세스를 거부하고 선택한 페이지로 리디렉션합니다. |
| [!UICONTROL Display Product Prices] | 웹 사이트 | 범주에 대한 제품 가격 표시를 제어합니다. 옵션: <br/>`Yes, for Everyone` - 범주의 제품 가격을 모든 사람이 볼 수 있습니다. <br/>`Yes, for Specified Customer Groups` - 선택한 고객 그룹의 구성원만 이 범주의 제품 가격을 볼 수 있습니다. <br/>`No` - 범주에 대한 제품 가격 표시를 끕니다. |
| [!UICONTROL Allow Adding to Cart] | 웹 사이트 | 범주에서 제품을 구매할 수 있는 사용자를 결정합니다. 옵션: <br/>`Yes, for Everyone` - 모든 사용자가 범주의 제품을 장바구니에 넣을 수 있습니다. <br/>`Yes, for Specified Customer Groups` - 선택한 고객 그룹의 구성원만 해당 범주의 제품을 장바구니에 넣을 수 있습니다. <br/>`No` - 다른 사람이 이 범주의 제품을 장바구니에 넣을 수 없습니다. |
| [!UICONTROL Disallow Catalog Search by] | 웹 사이트 | 카테고리에서 제품을 검색할 수 없는 고객 그룹을 식별합니다. |

{style="table-layout:auto"}

## [!UICONTROL Search Engine Optimization]

![검색 엔진 최적화](./assets/catalog-search-engine-optimization.png)<!-- zoom -->

<!-- [Search Engine Optimization](https://experienceleague.adobe.com/ko/docs/commerce-admin/catalog/products/settings/product-search-engine-optimization) -->

| 필드 | [범위](../../getting-started/websites-stores-views.md#scope-settings) | 설명 |
|--- |--- |----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Popular Search Terms] | 스토어 뷰 | _인기 검색어_&#x200B;가 스토어에서 구현되는지 여부를 결정합니다. 이 설정은 [Live Search](https://experienceleague.adobe.com/docs/commerce/live-search/overview.html?lang=ko)을(를) 사용하는 스토어에는 적용되지 않습니다. 옵션: `Enable` / `Disable` |
| [!UICONTROL Product URL Suffix] | 스토어 뷰 | html 또는 htm과 같은 접미사를 제품 URL에 적용할지 여부를 결정합니다. 접미사를 사용하면 접미사가 자동으로 적용되므로 접미사 앞에 마침표를 포함하지 마십시오. |
| [!UICONTROL Category URL Suffix] | 스토어 뷰 | html 또는 htm과 같은 접미사를 범주 URL에 적용할지 여부를 결정합니다. 접미사를 사용하면 접미사가 자동으로 적용되므로 접미사 앞에 마침표를 포함하지 마십시오. |
| [!UICONTROL Use Categories Path for Product URLs] | 스토어 뷰 | 상점 첫 화면의 제품 URL에 카테고리 경로가 포함되어 있는지 여부를 결정합니다. 이렇게 하면 여러 URL이 동일한 페이지를 가리키게 되어 검색 순위에 영향을 줄 수 있습니다. 자세한 내용은 [표준 메타 태그](../../merchandising-promotions/meta-data.md#canonical-meta-tag)를 참조하세요. |
| [!UICONTROL Create Permanent Redirect for URLs if URL Key Changed] | 스토어 뷰 | URL 키가 변경될 때마다 영구 리디렉션을 자동으로 만들지 여부를 결정합니다. 구현되면 제품 URL 키 필드 아래에 있는 이전 URL에 대한 사용자 지정 리디렉션 만들기 확인란이 기본적으로 선택됩니다. 옵션: `Yes` / `No` |
| [!UICONTROL Generate "category/product" URL Rewrites] | 글로벌 | 사용자가 많은 지정된 제품을 포함하는 카테고리를 저장할 때 Adobe Commerce이 데이터를 생성하여 다시 작성 테이블에 저장할지 여부를 결정합니다.  <br/><br/>시스템이 이 설정에 관계없이 제품 URL을 자동으로 확인하므로 이 옵션을 변경해도 Adobe Commerce에서 제품 URL을 확인하는 방법에는 영향을 주지 않습니다. <br/><br/>옵션: `Yes` / `No` <br/><br/>**_중요:_**&#x200B;생성된 데이터를 URL 재작성 테이블에 저장하면 성능이 저하될 수 있습니다. 자세한 내용은 [자동 제품 리디렉션](../../merchandising-promotions/url-redirect-product-automatic.md)을 참조하세요. |
| [!UICONTROL Apply transliteration for product URL] | 스토어 뷰 | 제품 URL을 만들거나 업데이트할 때 음역이 적용되는지 여부를 결정합니다. 옵션: `Yes` / `No`. 기본값은 `Yes`(으)로 설정됩니다. <br/><br/>특정 사용 사례의 경우 음역을 사용하지 않도록 설정해야 합니다. 예를 들어, 중국어로 온라인 스토어를 운영하는 경우 SEO 모범 사례에서는 제품 URL이 제품 이름과 일치하도록 권장합니다. 옵션을 `No`(으)로 설정하면 제품 URL에서 ASCII에 해당하는 문자 대신 한자를 사용할 수 있습니다. |
| [!UICONTROL Page Title Separator] | 스토어 뷰 | 브라우저 제목 표시줄에서 카테고리 이름과 하위 카테고리를 구분하는 문자를 식별합니다. |
| [!UICONTROL Use Canonical Link Meta Tag for Categories] | 스토어 뷰 | 동일한 카테고리 페이지를 가리키는 URL이 여러 개 있는 경우 이 옵션은 표준 메타 태그를 사용하여 검색 엔진이 인덱싱해야 하는 카테고리 URL을 식별합니다. URL에는 메타 태그를 사용하는 카테고리의 전체 이름이 포함되어 있습니다. 이렇게 하면 중복 컨텐츠가 줄어들고 SEO가 향상됩니다. 옵션: `Yes` / `No` |
| [!UICONTROL Use Canonical Link Meta Tag for Products] | 스토어 뷰 | 동일한 제품 페이지를 가리키는 URL이 여러 개 있는 경우, 이 옵션은 표준 메타 태그를 사용하여 검색 엔진이 인덱싱해야 하는 제품 URL을 식별합니다. URL에는 메타 태그를 사용하는 제품에 대한 전체 이름이 포함되어 있습니다. 이렇게 하면 중복 컨텐츠가 줄어들고 SEO가 향상됩니다. 옵션: `Yes` / `No` |

{style="table-layout:auto"}

## [!UICONTROL Category Top Navigation]

![범주 위쪽 탐색](./assets/catalog-category-top-navigation.png)<!-- zoom -->

<!-- Category Top Navigation](https://experienceleague.adobe.com/ko/docs/commerce-admin/catalog/catalog/navigation/navigation-top) -->

| 필드 | [범위](../../getting-started/websites-stores-views.md#scope-settings) | 설명 |
|--- |--- |--- |
| [!UICONTROL Maximal Depth] | 글로벌 | 위쪽 탐색에서 하위 범주 수준의 수를 결정합니다. `0`의 기본값은 수준 수에 제한을 두지 않습니다. |

{style="table-layout:auto"}

## [!UICONTROL Catalog Search]

Adobe Commerce에서 지원하는 [[!DNL Live Search]](https://experienceleague.adobe.com/docs/commerce/live-search/overview.html?lang=ko) 또는 타사 검색 엔진 서비스를 사용하여 카탈로그 검색을 구성할 수 있습니다. 설치에 대한 지침을 따르십시오.

### [!DNL Live Search]&#x200B;(으)로 Adobe Commerce

라이브 검색이 설치되면 카탈로그 검색에 다음 구성 설정이 포함됩니다.

![실시간 검색에 대한 카탈로그 검색](./assets/catalog-search-live-search.png)<!-- zoom -->

<!-- [Catalog Search for Live Search](https://experienceleague.adobe.com/ko/docs/commerce-admin/catalog/catalog/search/search-configuration) -->

| 필드 | [범위](../../getting-started/websites-stores-views.md#scope-settings) | 설명 |
|--- |--- |--- |
| [!UICONTROL Minimal Query Length] | 스토어 뷰 | 카탈로그 검색에 허용되는 최소 문자 수입니다. 이 옵션에 대해 설정된 값은 Elasticsearch 검색 엔진 구성에 있는 해당 범위 세트와 호환되어야 합니다. 예를 들어, Adobe Commerce에서 이 값을 `2`(으)로 설정하는 경우 검색 엔진에서 값을 업데이트합니다. |
| [!UICONTROL Maximum Query Length] | 스토어 뷰 | 카탈로그 검색에 허용되는 최대 문자 수. 이 옵션에 대해 설정된 값은 Elasticsearch 검색 엔진 구성에 있는 해당 범위 세트와 호환되어야 합니다. 예를 들어, Adobe Commerce에서 이 값을 300으로 설정하면 검색 엔진에서 값을 업데이트합니다. |
| [!UICONTROL Number of top search results to cache] | 스토어 뷰 | 더 빠른 응답을 위해 캐시할 인기 검색어 및 결과 수. `0` 값을 입력하면 두 번째로 입력한 검색어와 결과가 모두 캐시됩니다. 기본값: `100` |
| [!UICONTROL Autocomplete Limit] | 스토어 뷰 | [storefront 팝오버] 페이지에서 사용할 수 있는 최대 줄 수를 결정합니다. 라이브 검색 설치 시 기본값을 변경할 수 있으며 이 구성 설정을 변경하여 나중에 업데이트할 수 있습니다. 기본값: `8` |

{style="table-layout:auto"}

### 타사 검색 엔진

Adobe Commerce은 OpenSearch 및 Elasticsearch을 지원합니다. Adobe Commerce 버전 2.3.7-p3, 2.4.3-p2 및 2.4.4 이상 버전은 OpenSearch 서비스를 지원합니다. Elasticsearch 7.11 이상 버전은 Adobe Commerce on cloud infrastructure 프로젝트에서 지원되지 않습니다. Elasticsearch은 여전히 온-프레미스 설치에서 지원됩니다.

>[!IMPORTANT]
>
>- 2023년 8월에 Elasticsearch 7의 지원 종료 발표로 인해 Adobe은 모든 Adobe Commerce 고객을 OpenSearch 2.x 검색 엔진으로 마이그레이션하는 것을 권장합니다. 업그레이드하는 동안 검색 엔진을 마이그레이션하는 방법에 대한 자세한 내용은 _업그레이드 안내서_&#x200B;에서 [OpenSearch로 마이그레이션](https://experienceleague.adobe.com/docs/commerce-operations/upgrade-guide/prepare/opensearch-migration.html?lang=ko)을 참조하십시오.
>- 버전 2.4.4 및 2.4.3-p2에서는 Elasticsearch이라는 레이블이 지정된 모든 필드가 OpenSearch에도 적용됩니다. Elasticsearch 8.x에 대한 지원이 버전 2.4.6에 도입되면 Elasticsearch 구성과 OpenSearch 구성을 구별하기 위해 새 레이블이 생성되었습니다. 그러나 두 구성 옵션은 동일합니다.

![카탈로그 검색 구성 옵션](./assets/catalog-search-opensearch.png){zoomable="yes"}

| 필드 | [범위](../../getting-started/websites-stores-views.md#scope-settings) | 설명 |
|--- |--- |--- |
| [!UICONTROL Minimal Query Length] | 스토어 뷰 | 카탈로그 검색에 허용되는 최소 문자 수입니다. 이 옵션에 대해 설정된 값은 OpenSearch 또는 Elasticsearch 구성에 있는 해당 범위 세트와 호환되어야 합니다. 예를 들어, Adobe Commerce에서 이 값을 `2`(으)로 설정하는 경우 검색 엔진 구성에서도 값을 업데이트해야 합니다. 기본값: `3` |
| [!UICONTROL Maximum Query Length] | 스토어 뷰 | 카탈로그 검색에 허용되는 최대 문자 수. 이 옵션에 대해 설정된 값은 OpenSearch 또는 Elasticsearch 구성에 있는 해당 범위 세트와 호환되어야 합니다. 예를 들어, Adobe Commerce에서 이 값을 `300`(으)로 설정하는 경우 검색 엔진 구성에서 값을 업데이트해야 합니다. 기본값: `128` |
| [!UICONTROL Number of top search results to cache] | 스토어 뷰 | 더 빠른 응답을 위해 캐시할 인기 검색어 및 결과 수. `0` 값을 입력하면 두 번째로 입력한 검색어와 결과가 모두 캐시됩니다. 기본값: `100` |
| [!UICONTROL Enable EAV Indexer] | 글로벌 | 제품 EAV 인덱서의 사용 여부를 결정합니다. 이 기능은 색인 생성 속도를 향상시키고 타사 확장에서 색인을 사용하지 못하도록 제한합니다. 기본 옵션: `Yes` 사용 |
| [!UICONTROL Autocomplete Limit] | 스토어 뷰 | 검색 자동 완성을 위해 검색 필드 아래에 표시할 최대 검색 쿼리 수입니다. 이 양을 제한하면 검색 성능이 향상되고 표시된 목록 크기가 줄어듭니다. 기본값: `8` |
| 검색 엔진 | 글로벌 | 카탈로그 데이터 요청을 처리하는 데 필요한 검색 엔진을 식별합니다. 검색 엔진 구성 옵션은 OpenSearch와 Elasticsearch 모두에 대해 동일합니다. 옵션: `OpenSearch` 또는 `Elasticsearch` |
| [!UICONTROL OpenSearch Server Hostname] | 글로벌 | OpenSearch 또는 Elasticsearch 호스트 서버의 이름을 지정합니다. |
| [!UICONTROL OpenSearch Server Port] | 글로벌 | OpenSearch 또는 Elasticsearch에서 사용하는 서버 포트의 번호를 지정합니다. 기본값: `9200` |
| [!UICONTROL OpenSearch Index Prefix] | 글로벌 | OpenSearch 또는 Elasticsearch 인덱스를 식별하는 접두사를 지정합니다. 기본값: `magento2` |
| [!UICONTROL Enable OpenSearch HTTP Auth] | 글로벌 | 활성화된 경우 에서는 HTTP 인증을 사용하여 OpenSearch 또는 Elasticsearch 서버에 액세스하기 전에 사용자 이름과 암호를 묻습니다. 옵션: `Yes` / `No` |
| [!UICONTROL OpenSearch HTTP Username] | 글로벌 | _Elasticsearch HTTP 인증 사용_&#x200B;이(가) `Yes`(으)로 설정된 경우 OpenSearch 또는 Elasticsearch HTTP 인증의 사용자 이름을 지정합니다. |
| [!UICONTROL OpenSearch HTTP Password] | 글로벌 | _Elasticsearch HTTP 인증 사용_&#x200B;이(가) `Yes`(으)로 설정된 경우 OpenSearch 또는 Elasticsearch HTTP 인증의 암호를 지정합니다. |
| [!UICONTROL OpenSearch Server Timeout] | 글로벌 | OpenSearch 또는 Elasticsearch 서버에 대한 요청이 시간 초과되기 전 시간(초)을 결정합니다. 기본값: `15` |
| [!UICONTROL Test Connection] |  | OpenSearch 또는 Elasticsearch 연결을 확인합니다. |
| [!UICONTROL Enable Search Recommendations] | 스토어 뷰 | 검색 결과가 반환되지 않고 검색 결과 페이지의 `Related search terms` 섹션에 나타날 때 검색 권장 사항이 제공되는지 여부를 결정합니다. 옵션: `Yes` / `No` <br/>예로 설정하면 _[!UICONTROL Search Recommendations Count]_&#x200B;및_[!UICONTROL Shows Results Count for Each Recommendation]_&#x200B;에 대한 추가 옵션이 표시됩니다. |
| [!UICONTROL Search Recommendations Count] | 스토어 뷰 | 권장 사항으로 제공된 검색어의 수를 지정합니다. 기본적으로 5개를 넘지 않도록 표시됩니다. |
| [!UICONTROL Show Results Count for Each Recommendation] | 스토어 뷰 | `Yes`(으)로 설정하면 제안된 검색 권장 사항에 대해 검색된 제품 수가 대괄호 안에 표시됩니다. 옵션: `Yes` / `No` |
| [!UICONTROL Enable Search Suggestions] | 스토어 뷰 | 일반적인 철자 오류에 대한 검색 제안이 표시되는지 여부를 결정합니다. 활성화하면 결과를 반환하지 않고 **검색 결과** 페이지의 `Did you mean` 섹션 아래에 표시되는 모든 요청에 대해 검색 제안이 제공됩니다. 검색 제안은 검색 성능에 영향을 줄 수 있습니다. `Yes`(으)로 설정하면 검색 권장 사항 사용 및 관련 필드에 대한 추가 옵션이 표시됩니다. 옵션: `Yes` / `No` |
| [!UICONTROL Search Suggestions Count] | 스토어 뷰 | 제공되는 검색 제안 수를 결정합니다. 예: `2` |
| [!UICONTROL Show Results Count for Each Suggestion] | 스토어 뷰 | 각 제안에 대한 검색 결과 수를 표시할지 여부를 결정합니다. 테마에 따라 숫자는 제안 후 대괄호 안에 나타납니다. 옵션: `Yes` / `No` |
| [!UICONTROL Minimum Terms to Match] | 스토어 뷰 | 검색 결과가 반환되기 위해 일치해야 하는 쿼리의 용어 수에 해당하는 값을 지정합니다. 따라서 쇼핑객에게 최적의 결과 관련성이 보장됩니다. 비율 값은 숫자와 관련이 있으며 필요한 경우 내림차순 처리하여 쿼리에서 일치시킬 최소 용어 수로 사용합니다. 값은 음수 또는 양의 정수, 음수 또는 양의 퍼센트, 두 가지의 조합 또는 다중 조합일 수 있다. 자세한 내용은 OpenSearch 설명서의 [minimum_should_match 매개 변수](https://opensearch.org/docs/latest/query-dsl/minimum-should-match/)을 참조하세요. |

## [!UICONTROL Downloadable Product Options]

![다운로드 가능한 제품 옵션](./assets/catalog-downloadable-product-options.png)<!-- zoom -->

<!-- [Downloadable Product Options](https://experienceleague.adobe.com/ko/docs/commerce-admin/catalog/products/types/product-create-downloadable#configure-the-download-options) -->

| 필드 | [범위](../../getting-started/websites-stores-views.md#scope-settings) | 설명 |
|--- |--- |--- |
| [!UICONTROL Order Item Status to Enable Downloads] | 웹 사이트 | 다운로드를 사용할 수 있기 전에 주문해야 하는 상태를 결정합니다. 옵션: `Pending` / `Invoiced` |
| [!UICONTROL Default Maximum Number of Downloads] | 웹 사이트 | 고객이 사용할 수 있는 기본 다운로드 수를 결정합니다. |
| [!UICONTROL Shareable] | 웹 사이트 | 고객이 다운로드 링크에 액세스하기 위해 계정에 로그인해야 하는지 여부를 결정합니다. 옵션: <br/>**예** - 전자 메일로 링크를 보내어 다른 사용자와 공유할 수 있도록 허용합니다. <br/>**아니요** - 고객이 계정에 로그인하여 다운로드 링크에 액세스해야 합니다. |
| [!UICONTROL Default Sample Title] | 스토어 뷰 | 모든 샘플 파일의 기본 제목입니다. |
| [!UICONTROL Default Link Title] | 스토어 뷰 | 다운로드 가능한 모든 제목의 기본 링크입니다. |
| [!UICONTROL Opens Links in New Window] | 웹 사이트 | 다운로드 링크가 새 브라우저 창에서 열리는지 여부를 결정합니다. 옵션: `Yes` / `No` |
| [!UICONTROL Use Content Disposition] | 스토어 뷰 | 다운로드 가능한 콘텐츠에 대한 링크를 이메일 첨부 파일 또는 브라우저 창의 인라인 링크로 전달하는 방법을 결정합니다. 옵션: <br/>**`Attachment`**- 다운로드 링크가 전자 메일 첨부 파일로 제공됩니다.<br/>**`Inline`** - 다운로드 링크가 웹 페이지에서 인라인 링크로 제공됩니다. |
| [!UICONTROL Disable Guest Checkout if Cart Contains Downloadable Items] | 웹 사이트 | 다운로드 가능한 제품을 구입하는 게스트가 계정을 등록하고 로그인하여 체크아웃 프로세스를 완료해야 하는지 여부를 결정합니다. 옵션: <br/>**`Yes`**- 장바구니에 다운로드 가능한 제품이 포함되어 있는 경우, 게스트는 계정을 등록하거나 기존 계정에 로그인하여 구매를 완료해야 합니다.<br/>**`No`** - 다운로드 링크가 이메일 메시지 본문에서 인라인 링크로 전달됩니다.  <br/> _&#x200B;**참고:**&#x200B;_ 게스트 체크 아웃은 [공유 가능]이 `Yes`(으)로 설정된 경우에만 제품을 다운로드할 수 있습니다. |

{style="table-layout:auto"}

## [!UICONTROL Date & Time Custom Options]

![날짜 및 시간 사용자 지정 옵션](./assets/catalog-date-time-custom-options.png)<!-- zoom -->

<!-- Date & Time Custom Options](https://experienceleague.adobe.com/ko/docs/commerce-admin/catalog/product-attributes/attributes-input-types#date-and-time-options) -->

| 필드 | [범위](../../getting-started/websites-stores-views.md#scope-settings) | 설명 |
|--- |--- |--- |
| [!UICONTROL Use JavaScript Calendar] | 스토어 뷰 | JavaScript 캘린더를 날짜 필드에 대한 입력 컨트롤로 사용할지 여부를 결정합니다. 옵션: `Yes` / `No` <br/>을(를) `No`(으)로 설정하면 날짜 필드의 각 부분에 대해 별도의 드롭다운이 표시됩니다. |
| [!UICONTROL Date Fields Order] | 스토어 뷰 | 세 날짜 필드의 순서를 설정합니다. 옵션: `Day` / `Month` / `Year` |
| [!UICONTROL Time Format] | 스토어 뷰 | 시간 형식을 12시간 또는 24시간 시계로 설정합니다. 옵션: `12h AM/PM` / `24h` |
| [!UICONTROL Year Range] | 스토어 뷰 | _년_ 필드에 나타나는 연도의 시작 및 끝 범위를 정의합니다. 값을 YYYY 형식으로 입력해야 합니다. |

{style="table-layout:auto"}

## [!UICONTROL Catalog Events]

{{ee-feature}}

![카탈로그 이벤트](./assets/catalog-events.png)<!-- zoom -->

<!-- [Catalog Events](https://experienceleague.adobe.com/ko/docs/commerce-admin/marketing/promotions/events/events-private-sales) -->

| 필드 | [범위](../../getting-started/websites-stores-views.md#scope-settings) | 설명 |
|--- |--- |--- |
| [!UICONTROL Enable Catalog Events Functionality] | 웹 사이트 | 이벤트 모듈의 활성화 여부를 결정합니다. |
| [!UICONTROL Enable Catalog Event Widget on Frontend] | 스토어 뷰 | 상점 전면에서 이벤트 위젯을 사용할 수 있는지 여부를 결정합니다. 사이트의 이벤트에 대한 정보가 포함된 정적 블록입니다. |
| [!UICONTROL Number of Events to be Displayed in the Event Slider Widget] | 스토어 뷰 | 카테고리 페이지의 이벤트 슬라이더 위젯에 표시되는 이벤트 수를 결정합니다. 재정의하려면 `limit="x"` 변수를 사용하십시오. |
| [!UICONTROL Events to Scroll per Click in Event Slider Widget] | 스토어 뷰 | 홈 페이지와 같은 CMS 페이지의 이벤트 슬라이더 위젯에 표시되는 이벤트 수를 결정합니다. 재정의하려면 `scroll="x"` 변수를 사용하십시오. |

{style="table-layout:auto"}

## [!UICONTROL Rule-Based Product Relations]

{{ee-feature}}

![규칙 기반 제품 관계](./assets/catalog-rule-based-product-relations.png)<!-- zoom -->

<!-- [Rule-Based Product Relations](https://experienceleague.adobe.com/ko/docs/commerce-admin/marketing/promotions/product-relationships/product-related-rules) -->

| 필드 | [범위](../../getting-started/websites-stores-views.md#scope-settings) | 설명 |
|--- |--- |--- |
| [!UICONTROL Maximum Number of Products in Related Products List] | 글로벌 | _관련 제품_ 목록에 표시할 수 있는 최대 제품 수를 결정합니다. |
| [!UICONTROL Show Related Products] | 글로벌 | 스토어에 나타나는 관련 제품 목록을 결정합니다. 제품 정보에서 수동으로 선택한 목록, 제품 관계 규칙에 대한 응답으로 생성된 목록 또는 두 가지 모두를 조합할 수 있습니다. 옵션: `Both Selected and Rule-Based` / `Selected Only` / `Rule-Based Only` |
| [!UICONTROL Rotation Mode for Products in Related Products List] | 글로벌 | _관련 제품_ 목록의 제품이 나타나는 순서를 결정합니다. 옵션: `Do not rotate` / `Shuffle` |
| [!UICONTROL Maximum Number of Products in Cross-Sell Product List] | 글로벌 | 크로스셀 목록에 나타날 수 있는 최대 제품 수를 결정합니다. |
| [!UICONTROL Show Cross-Sell Products] | 글로벌 | 스토어에 나타나는 교차 판매 제품 목록을 결정합니다. 제품 정보에서 수동으로 선택한 목록, 제품 관계 규칙에 대한 응답으로 생성된 목록 또는 두 가지 모두를 조합할 수 있습니다. 옵션: `Both Selected and Rule-Based` / `Selected Only` / `Rule-Based Only` |
| [!UICONTROL Rotation Mode for Products in Cross-Sell Products List] | 글로벌 | 크로스셀 제품 목록의 제품이 표시되는 순서를 결정합니다. 옵션: 회전/섞지 않음 |
| [!UICONTROL Maximum Number of Products in Upsell Product List] | 글로벌 | _상향 판매 제품_ 목록에 표시할 수 있는 최대 제품 수를 결정합니다. |
| [!UICONTROL Show Upsell Products] | 글로벌 | 스토어에 나타나는 업셀 제품 목록을 결정합니다. 제품 정보에서 수동으로 선택한 목록, 제품 관계 규칙에 대한 응답으로 생성된 목록 또는 두 가지 모두를 조합할 수 있습니다. 옵션: `Both Selected and Rule-Based` / `Selected Only` / `Rule-Based Only` |
| [!UICONTROL Rotation Mode for Products in Upsell Product List] | 글로벌 | 업셀 제품 목록의 제품이 표시되는 순서를 결정합니다. 옵션: `Do not rotate` / `Shuffle` |

{style="table-layout:auto"}
