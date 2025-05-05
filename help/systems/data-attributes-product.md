---
title: 제품 데이터 속성 참조
description: 제품 데이터 가져오기 및 내보내기 작업을 수행할 때 이 제품 데이터 속성 참조를 사용합니다.
exl-id: 9ffa4d1f-cbf8-4a08-bb79-33f21e698a74
feature: Products, Attributes
source-git-commit: 976efad9fb4bb53f6f102fde534001d254cd3b9c
workflow-type: tm+mt
source-wordcount: '2496'
ht-degree: 0%

---

# 제품 데이터 속성 참조

다음 표에는 일반적인 제품 내보내기의 속성이 표시되는 기본 순서로 나열되어 있습니다. 각 속성은 CSV 파일에 열로 표시되고 제품 레코드는 행으로 표시됩니다. 밑줄로 시작하는 열에는 복잡한 데이터에 대한 속성 또는 옵션 값과 같은 서비스 데이터가 포함됩니다. 카탈로그에서 제품을 [내보내기](data-export.md)하여 각 특성이 데이터에 어떻게 표시되는지 확인할 수 있습니다.

이 데이터를 내보내는 데 사용되는 설치에는 샘플 데이터가 설치되어 있으며 두 개의 웹 사이트와 여러 스토어 보기가 있습니다. 이 목록에는 일반적으로 내보내는 모든 열이 포함되어 있지만 `sku`만 필요한 값입니다. 데이터를 가져오려면 변경 내용이 있는 열만 포함할 수 있습니다. `sku`이(가) 첫 번째 열이어야 하지만 나머지 특성의 순서는 중요하지 않습니다.

## 간단한 제품 CSV 파일 구조

| 속성 | 설명 |
|--- |--- |
| `sku` | (필수) 재고 유지 단위는 재고를 추적하는 데 사용되는 고유한 영숫자 식별자입니다. SKU는 최대 64자까지 사용할 수 있습니다. 예: `sku123`<br/>**_참고:_**&#x200B;SKU가 64자를 초과하면 가져오기가 실패합니다. |
| `store_view_code` | 제품을 사용할 수 있는 특정 스토어 보기를 식별합니다. 비어 있는 경우 기본 스토어 보기에서 제품을 사용할 수 있습니다. 예: `storeview1`, `english`, `spanish` |
| `attribute_set_code` | 제품 유형에 따라 제품을 특정 속성 세트 또는 제품 템플릿에 할당합니다. 예를 들어 `default`<br><br>제품을 만든 후에는 가져오기 기능을 사용하여 특성 집합을 변경할 수 없습니다. 그러나 관리자에서 속성 세트를 변경하고 제품을 다시 내보내 CSV 파일 을 업데이트할 수 있습니다. |
| `product_type` | 제품 유형을 나타냅니다. 값:<br/>`simple` — 일반적으로 단일 단위로 판매되거나 고정 수량으로 판매되는 유형 품목.<br/>`grouped` — 세트로 판매되는 별도의 제품 그룹입니다.<br/>`configurable` — 구매하기 전에 고객이 선택해야 하는 여러 옵션이 있는 제품입니다. 개별 SKU를 사용하는 개별 제품을 나타내므로 각 변형 세트에 대해 인벤토리를 관리할 수 있습니다. 예를 들어 구성 가능한 제품에 대한 색상 및 크기의 조합은 카탈로그의 특정 SKU와 연결됩니다.<br/>`virtual` — 배송이 필요하지 않고 재고에 보관되지 않는 유형의 제품이 아닙니다. 서비스, 멤버십 및 구독이 이러한 예입니다.<br/>`bundle` — 함께 판매되는 간단한 제품의 사용자 지정 가능한 제품 세트입니다. |
| `categories` | 제품에 할당된 각 카테고리를 나타냅니다. 슬래시로 범주와 하위 범주를 구분합니다. 여러 범주 경로를 나타내려면 파이프 \| 로 각 경로를 구분합니다 기호. 예: `Default Category/Gear\|Default Category/Gear/Bags` |
| `product_websites` | 제품을 사용할 수 있는 각 웹 사이트의 웹 사이트 코드. 단일 제품을 여러 웹 사이트에 할당하거나 하나로 제한할 수 있습니다. 여러 웹 사이트를 지정하는 경우 쉼표로, 공백 없이 각각 구분하십시오. 예: `base` 또는 `base,website2` |
| `name` | 제품 이름은 모든 제품 목록에 표시되며 고객이 제품을 식별하는 데 사용하는 이름입니다. |
| `description` | 제품 설명은 제품에 대한 자세한 정보를 제공하며 간단한 HTML 태그를 포함할 수 있습니다. |
| `short_description` | 짧은 제품 설명의 사용은 테마에 따라 다릅니다. 제품 목록에 나타날 수 있으며 때로는 쇼핑 사이트로 전송된 RSS 피드 목록에 사용됩니다. |
| `weight` | 개별 제품의 무게. 실제 제품 중량은 운송인이 선적 시에 결정한다. |
| product_online | 제품을 스토어에서 판매할 수 있는지 여부를 결정합니다. 값: <br/>`1` — (예) 제품을 사용할 수 있으며 판매할 수 있습니다.<br/>`2` — (아니요) 제품이 비활성화되어 판매에 사용할 수 없습니다. |
| `tax_class_name` | 이 제품과 연계된 세금 분류의 이름. |
| `visibility` | 제품이 카탈로그에 표시되는지, 그리고 검색할 수 있게 되는지를 결정합니다. 값:<br/>`Not Visible Individually` — 다른 제품의 변형으로 사용할 수 있지만 해당 제품은 제품 목록에 포함되지 않습니다.<br/>`Catalog` — 제품이 모든 카탈로그 목록에 나타납니다.<br/>`Search` —제품을 검색 작업에 사용할 수 있습니다.<br/>`Catalog, Search` — 제품이 카탈로그 목록에 포함되어 있으며 검색할 수도 있습니다. |
| `price` | 해당 제품이 매장에서 판매되는 가격입니다. |
| `special_price` | 지정된 날짜 범위 동안 제품의 할인된 가격. |
| `special_price_from_date` | 특별가격이 유효한 기간의 시작일. |
| `special_price_to_date` | 특별 가격이 유효한 기간의 마지막 일자. |
| `url_key` | 제품을 식별하는 URL의 부분입니다. 기본값은 제품 이름을 기반으로 합니다. 예: `product-name` |
| save_rewrites_history | 새 `url_key`(으)로 값 `1`이(가) 제공된 경우 이전 URL이 새 URL로 리디렉션되도록 새 301 URL 다시 쓰기가 생성됩니다. |
| `meta_title` | 메타 제목은 브라우저의 제목 표시줄 및 탭과 검색 결과 목록에 나타납니다. 메타 제목은 제품에 고유해야 하고, 고가치 키워드를 통합해야 하며, 길이가 70자 미만이어야 합니다. |
| `meta_keywords` | 메타 키워드는 검색 엔진에만 표시되며 일부 검색 엔진에서는 무시됩니다. 높은 값의 키워드를 쉼표로 구분하여 선택합니다. 예: `keyword1`, `keyword2`, `keyword3` |
| `meta_description` | 메타 설명은 검색 결과 목록에 대한 제품에 대한 간략한 개요를 제공합니다. 메타 설명은 150-160자 사이여야 하지만 필드에는 최대 255자를 사용할 수 있습니다. |
| `base_image` | 제품 페이지의 기본 이미지에 대한 상대 경로입니다. Commerce은 파일을 알파벳 폴더 구조로 내부적으로 저장합니다. 내보낸 데이터에서 각 이미지의 정확한 위치를 확인할 수 있습니다. 예를 들어 `/sample_data/m/b/mb01-blue-0.jpg`<br/>새 이미지를 업로드하거나 기존 이미지에 쓰려면 파일 이름 앞에 슬래시를 입력하십시오. 예: `/image.jpg` |
| `base_image_label` | 기본 이미지와 연결된 레이블입니다. |
| `small_image` | 카탈로그 페이지에 사용되는 작은 이미지의 파일 이름으로, 앞에 슬래시가 붙습니다. 예: `/image.jpg` |
| `small_image_label` | 작은 이미지와 연결된 레이블입니다. 예: `Small Image 1`, `Small Image 2` |
| `thumbnail_image` | 제품 페이지의 갤러리에 표시할 썸네일 이미지의 파일 이름 앞에는 슬래시가 표시됩니다. 예: `/image.jpg` |
| `thumbnail_image_label` | 썸네일 이미지와 연결된 레이블입니다. 예: `Thumbnail 1`, `Thumbnail 2` |
| `created_at` | 제품이 생성된 날짜를 나타냅니다. 날짜는 제품이 만들어질 때 자동으로 생성되지만, 나중에 편집할 수 있습니다. |
| `updated_at` | 제품이 마지막으로 업데이트된 날짜를 나타냅니다. |
| `new_from_date` | 새 제품 목록의 &quot;시작&quot; 날짜를 지정하고 제품이 새 제품으로 포함되는지 여부를 결정합니다. |
| `new_to_date` | 새 제품 목록의 &quot;종료&quot; 날짜를 지정하고 제품이 새 제품으로 포함되는지 여부를 결정합니다. |
| `display_product_options_in` | 제품에 여러 옵션이 있는 경우 는 제품 페이지에서 옵션이 표시되는 위치를 결정합니다. 값: 제품 정보 열/정보 열 뒤 블록 |
| `map_price` | 제품의 최소 광고 가격. (MAP이 활성화된 경우에만 표시됩니다.) |
| `msrp_price` | 제품에 대한 제조업체의 권장 소매 가격. (MAP이 활성화된 경우에만 표시됩니다.) |
| `map_enabled` | 구성에서 최소 광고 가격 이 활성화되어 있는지 여부를 결정합니다. 값: <br/>`1` — (예) MAP이 활성화되어 있습니다.<br/>`0`(또는 비어 있음) — (아니요) MAP이 활성화되지 않았습니다. |
| `gift_message_available` | 선물 메시지를 제품 구매에 포함할 수 있는지 여부를 결정합니다. 값: <br/>`1` — (예) 선물 메시지를 포함하는 옵션이 고객에게 제공됩니다.<br/>`0`(또는 비어 있음) — (아니요) 선물 메시지를 포함하는 옵션이 고객에게 제공되지 않습니다. |
| `custom_design` | 제품 페이지에 적용할 수 있는 사용 가능한 테마를 나열합니다. |
| `custom_design_from` | 선택한 테마를 제품 페이지에 적용할 시작 날짜를 지정합니다. |
| `custom_design_to` | 선택한 테마를 제품 페이지에 적용할 종료 날짜를 지정합니다. |
| `custom_layout_update` | 제품 페이지에 레이아웃 업데이트로 적용되는 추가 XML 코드입니다. |
| `page_layout` | 제품 페이지의 페이지 레이아웃을 결정합니다. 값: <br/>`No layout updates` — 페이지 레이아웃이 변경되지 않습니다.<br/>`1 column` — 제품 페이지에 1열 레이아웃을 적용합니다.<br/>`2 columns with left bar` — 왼쪽 사이드바가 있는 2열 레이아웃을 제품 페이지에 적용합니다.<br/>`2 columns with right bar` — 오른쪽 사이드바가 있는 2열 레이아웃을 제품 페이지에 적용합니다.<br/>`3 columns` — 3열 레이아웃을 제품 페이지에 적용합니다.<br/>`empty` — 빈 레이아웃을 제품 페이지에 적용합니다. |
| `product_options_container` | 제품에 여러 옵션이 있는 경우 는 제품 페이지에서 옵션이 표시되는 위치를 결정합니다. 값: 제품 정보 열/정보 열 뒤 블록 |
| `msrp_display_actual_price_type` | 제품의 실제 가격이 고객에게 표시되는 위치를 결정합니다. 값:<br/>`In Cart` — 장바구니의 실제 제품 가격을 표시합니다.<br/>`Before Order Confirmation` — 주문이 확정되기 바로 전 체크아웃 프로세스가 끝날 때 실제 제품 가격을 표시합니다.<br/>`On Gesture` — 고객이 _가격 클릭_ 또는 _을 클릭하면 실제 제품 가격이 팝업으로 표시됩니다._ 링크입니다. |
| `country_of_manufacture` | 제품이 제조된 국가를 식별합니다. |
| `additional_attributes` | 제품에 대해 생성된 추가 속성입니다. 예: <br/>`has_options=0,required_options=0color=Black,has_options=0,required_options=0,size_general=XS` |
| `qty` | 현재 재고가 있는 제품의 수량입니다. |
| `out_of_stock_qty` | 제품이 품절 상태임을 결정하는 재고 수준입니다. |
| `use_config_min_qty` | 구성의 기본값이 사용되는지 여부를 확인하고 구성 설정 사용 확인란에 해당합니다. 값: <br/>`1` — (예) 이 특성의 값에 기본 구성 설정이 사용됩니다.<br/>`0`(또는 비어 있음) — (아니요) 이 특성 값에 대해 기본 구성을 재정의할 수 있습니다. |
| `is_qty_decimal` | 수량 속성에 십진수 값이 있는지 여부를 결정합니다. 값: <br/>`1` — (예) qty 속성의 값은 십진수 값입니다.<br/>`0`(또는 비어 있음) — (아니요) qty 속성의 값은 정수(정수)입니다. |
| `allow_backorders` | 스토어에서 미납 주문을 허용하는지 여부와 미납 주문 관리 방법을 결정합니다. |
| `use_config_backorders` | 미납 주문에 대한 기본 구성 설정이 사용되고 있는지 확인하고 구성 설정 사용 확인란의 상태에 해당합니다. 값: <br/>`1` — (예) qty 속성의 값은 십진수 값입니다.<br/>`0`(또는 비어 있음) — (아니요) qty 속성의 값은 정수(정수)입니다. |
| `min_cart_qty` | 단일 주문으로 구매할 수 있는 품목의 최소 수량을 지정합니다. |
| `use_config_min_sale_qty` | 최소 수량에 대한 기본 구성 설정을 사용할지 여부를 결정하며, 구성 설정 사용 확인란의 상태에 해당합니다. 값: <br/>`1` — (예)<br/>`0`(또는 비어 있음) — (아니요) |
| `max_cart_qty` | 단일 주문으로 구매할 수 있는 제품의 최대 수량을 지정합니다. |
| `use_config_max_sale_qty` | 최대 수량에 대한 기본 구성 설정을 사용할지 여부를 결정하고 구성 설정 사용 확인란의 상태에 해당합니다. 값: <br/>`1` — (예)<br/>`0`(또는 비어 있음) — (아니요) |
| `is_in_stock` | 제품의 재고 여부를 나타냅니다. |
| `notify_on_stock_below` | _재고 부족_ 알림을 트리거하는 재고 수준을 지정합니다. |
| `use_config_notify_stock_qty` | 재고 수준 알림을 트리거하는 데 기본 구성 설정을 사용하는지, 그리고 이 설정이 구성 설정 사용 확인란의 상태에 해당하는지 여부를 결정합니다. 값: <br/>`1` — (예)<br/>`0`(또는 비어 있음) — (아니요) |
| `manage_stock` | 재고 관리를 사용하여 제품을 관리할지 여부를 결정합니다. 값: <br/>`1` — (예) 전체 재고 관리를 활성화하여 제품의 재고 수준을 관리합니다.<br/>`0`(또는 비어 있음) — (아니요) 시스템이 현재 재고가 있는 항목의 수를 추적하지 않습니다. |
| `use_config_manage_stock` | 재고 관리에 대한 기본 구성 설정을 사용하는지 여부를 확인하고 구성 설정 사용 확인란의 상태에 해당합니다. 값: <br/>`1` — (예)<br/>`0`(또는 비어 있음) — (아니요) |
| `use_config_qty_increments` | 수량 증분에 대한 기본 구성 설정을 사용할지 여부를 결정하고 구성 설정 사용 확인란의 상태에 해당합니다. 값: <br/>`1` — (예)<br/>`0`(또는 비어 있음) — (아니요) |
| `qty_increments` | 수량 증분을 구성하는 제품 수를 설정합니다. |
| `use_config_enable_qty_inc` | 수량 증분을 활성화하는 기본 구성 설정이 사용되는지 여부를 확인하고 구성 설정 사용 확인란의 상태에 해당합니다. 값: <br/>`1` — (예)<br/>`0`(또는 비어 있음) — (아니요) |
| `enable_qty_increments` | 제품에 대해 수량 증분이 활성화되어 있는지 여부를 결정합니다. |
| `is_decimal_divided` | 제품의 부품을 별도로 배송할 수 있는지 여부를 결정합니다. 옵션: `Yes` / `No` |
| `website_id` | 여러 웹 사이트가 설치된 경우 는 제품을 사용할 수 있는 특정 웹 사이트를 식별합니다. 비어 있는 경우 모든 웹 사이트에서 제품을 사용할 수 있습니다. |
| `related_skus` | 관련 제품으로 식별된 각 제품의 SKU를 나열합니다. 예: `24-WG080,24-UG03,24-UG01,24-UG02` |
| `related_position` | related_skus 열에 관련 제품으로 나열되는 SKU의 위치(정렬 순서)를 결정합니다. 예: `1,2,3,4` |
| `crosssell_skus` | 크로스셀로 식별된 각 제품의 SKU를 나열합니다. |
| `crosssell_position` | `crosssell_skus` 열에서 교차 판매 제품으로 나열된 SKU의 위치(정렬 순서)를 결정합니다. |
| `upsell_skus` | 상향 판매로 식별된 각 제품의 SKU를 나열합니다. |
| `upsell_position` | `upsell_skus` 열에서 상향 판매 제품으로 나열된 SKU의 위치(정렬 순서)를 결정합니다. |
| `additional_images` | 슬래시가 앞에 오는 제품과 연결할 추가 이미지의 파일 이름입니다. 예: `/image.jpg` |
| `additional_image_labels` | 추가 이미지와 연결된 레이블입니다. 예: `Label 1`, `Label 2` |
| `custom_options` | 각 사용자 지정 옵션에 할당된 속성 및 값을 지정합니다. 예: <br/>`name=Color, type=drop_down, required=1, price= price_type=fixed, sku=, option_title=Black|name=Color, type=drop_down, required=1, price=, price_type=fixed, sku=, option_title=White` |

{style="table-layout:auto"}

## 제품 변형에 대한 서비스 데이터

| 속성 | 설명 | 적용 대상 |
|--- |--- | --- |
| `_super_products_sku` | 구성 가능한 제품 변형에 대해 생성된 SKU입니다. 예: WB03-XS-Green | 구성 가능한 제품 |
| `_super_attribute_code` | 구성 가능한 제품 변형의 속성 코드입니다. 예: color | 구성 가능한 제품 |
| `_super_attribute_option` | 구성 가능한 제품 변형의 값입니다. 예: 녹색 | 구성 가능한 제품 |
| `_super_attribute_price_corr` | 구성 가능한 제품 변동과 연관된 가격 조정입니다. | 구성 가능한 제품 |
| `_associated_sku` | 그룹화된 제품과 연계된 제품의 SKU. | 그룹화된 제품 <br/>번들 제품 |
| `_associated_default_qty` | 포함된 관련 제품의 수량을 결정합니다. | 구성 가능한 제품<br/>그룹화된 제품<br/>번들 제품 |
| `_associated_position` | 다른 관련 제품과 함께 나열될 때 관련 제품의 위치를 결정합니다. | 구성 가능한 제품<br/>그룹화된 제품<br/>번들 제품 |

{style="table-layout:auto"}

## 복잡한 제품 데이터 속성

복합 데이터라는 용어는 여러 제품 옵션과 관련된 데이터를 나타냅니다. 다음 제품 유형은 별도의 제품에서 가져온 데이터를 사용하여 제품 변형과 여러 옵션을 만듭니다.

- [구성 가능](../catalog/product-create-configurable.md)
- [그룹화](../catalog/product-create-grouped.md)
- [번들](../catalog/product-create-bundle.md)

구성 가능한 제품을 내보내는 경우 간단한 제품을 구성하는 표준 속성과 복잡한 데이터를 관리하는 데 필요한 추가 속성을 찾을 수 있습니다.

![구성 가능한 제품 - 내보낸 데이터](./assets/data-exported-configurable-product.png){width="600" zoomable="yes"}

### 구성 가능한 제품

| 속성 | 설명 |
|--- |--- |
| `configurable_variation_labels` | 제품 변형을 식별하는 레이블입니다. 예: `Choose Color:` 또는 `Choose Size:` |
| `configurable_variations` | 제품 변형과 관련된 값을 설명합니다. 예: `sku=sku-red xs,color=red,size=xs,price=10.99,display=1,image=/pub/media/import/image1.png|sku=sku-red-m,color=red,size=m,price=20.88,display=1,image=/pub/media/import/image2.png` |

{style="table-layout:auto"}

### 그룹화된 제품

| 속성 | 설명 |
|--- |--- |
| `associated_skus` | 그룹을 구성하는 개별 제품의 SKU를 식별합니다. |

{style="table-layout:auto"}

### 번들 제품

| 속성 | 설명 |
|--- |--- |
| `bundle_price_type` | 번들 항목의 가격이 고정인지 동적인지 여부를 결정합니다. |
| `bundle_sku_type` | 각 항목에 변수, 동적 SKU가 할당되었는지 또는 번들에 고정 SKU가 사용되는지를 결정합니다. 옵션: 고정 / 동적 |
| `bundle_weight_type` | 번들 항목의 가중치가 가변인지 아니면 고정인지를 결정합니다. |
| `bundle_values` | 번들 옵션과 연결된 teach 값에 대해 설명합니다. 예: `name=Bundle Option One,type=dropdown; required=1, sku=sku-option2,price=10, price_type=fixed` |

{style="table-layout:auto"}

## 고급 가격책정 속성

고급 가격 가져오기/내보내기를 사용하면 제품 그룹 및 계층 가격에 대한 가격 정보를 빠르게 업데이트할 수 있습니다. [가져오기](data-import.md) 및 [내보내기](data-export.md) 고급 가격 데이터에 대한 프로세스는 다른 엔터티 형식과 동일합니다. 샘플 CSV 파일에는 고급 가격을 지원하는 각 제품 유형의 계층 및 그룹 가격이 포함되어 있습니다. 고급 가격을 변경해도 나머지 제품 레코드에는 영향을 주지 않습니다.

![데이터 내보내기 예 - 고급 가격 책정](./assets/data-advanced-pricing-export-sample.png){width="600" zoomable="yes"}

| 속성 | 설명 |
|--- |--- |
| `sku` | (필수) 재고 유지 단위는 재고를 추적하는 데 사용되는 고유한 영숫자 식별자입니다. SKU는 최대 64자까지 사용할 수 있습니다. 예: `sku123`<br/>**_참고:_**&#x200B;SKU가 64자를 초과하면 가져오기가 실패합니다. |
| `tier_price_website` | [웹 사이트 코드](../stores-purchase/stores.md#add-websites)은(는) 계층 가격을 사용할 수 있는 각 웹 사이트를 식별합니다. 예: `-  website1 -  All Websites [USD]` |
| `tier_price_customer` | 계층 가격을 사용할 수 있는 [고객 그룹](../customers/customer-groups.md)을(를) 식별합니다. 예: `-  ALL GROUPS -  NOT LOGGED IN -  General -  Wholesale -  Retailer` |
| `tier_price_customer_group` | 계층 가격을 사용할 수 있는 고객 그룹을 식별합니다. 예: `-  ALL GROUPS -  NOT LOGGED IN -  General -  Wholesale -  Retailer` |
| `tier_price_qty` | 계층 가격 할인을 받기 위해 주문해야 하는 제품의 수량입니다. |
| `tier_price` | 제품의 할인된 계층 가격. [번들 제품](../catalog/product-create-bundle.md)의 경우 계층 가격은 백분율로 계산됩니다. |
| `group_price_website` | 그룹 가격을 사용할 수 있는 각 웹 사이트의 [웹 사이트 코드](../stores-purchase/stores.md#add-websites). 여러 웹 사이트를 지정하는 경우 쉼표로, 공백 없이 각각 구분하십시오. 예: `-  website1 -  All Websites [USD]` |
| `group_price_customer_group` | 그룹 가격을 사용할 수 있는 고객 그룹을 식별합니다. 예: `-  NOT LOGGED IN -  General -  Wholesale -  Retailer` |
| `group_price` | 제품의 할인된 그룹 가격. [번들 제품](../catalog/product-create-bundle.md)의 경우 그룹 가격은 백분율로 계산됩니다. |

{style="table-layout:auto"}
