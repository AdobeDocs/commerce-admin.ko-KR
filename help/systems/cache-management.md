---
title: 캐시 관리
description: 사이트의 성능을 개선하는 쉬운 방법을 제공하는 캐시 관리 도구를 사용하는 방법에 대해 알아봅니다.
exl-id: c87f85ca-81b9-4cbf-9817-3d779397eefd
feature: Cache, System
source-git-commit: fdf04be69754d0209772d9ceb244e3808f3b61d3
workflow-type: tm+mt
source-wordcount: '1821'
ht-degree: 0%

---

# 캐시 관리

Adobe Commerce 및 Magento Open Source 캐시 관리 시스템은 사이트의 성능을 개선하는 쉬운 방법을 제공합니다. 캐시에 새로 고침이 필요할 때마다 알림에 대한 링크가 표시됩니다 [!UICONTROL Cache Management] 새로 고침을 완료할 페이지입니다.

![제품 속성 저장 - 캐시 메시지 업데이트](./assets/product-attribute-save-msg-update-cache.png){width="500"}

다음 _[!UICONTROL Cache Management]_페이지에는 각 기본 캐시의 상태와 연관된 태그가 표시됩니다. 오른쪽 상단의 큰 버튼을 사용하여 캐시 또는 모든 항목이 포함된 캐시 저장소를 플러시할 수 있습니다. 페이지 하단에서 추가 버튼을 사용하여 카탈로그 제품 이미지 캐시와 JavaScript/CSS 캐시를 플러시할 수 있습니다.

>[!IMPORTANT]
>
>카탈로그 엔티티가 변경되면 다른 페이지에 영향을 줄 수 있으며 여러 캐시를 동시에 무효화할 수 있습니다. 캐시 관리 페이지를 검토할 때 새로 고침이 필요한 잘못된 항목이 표시될 수 있습니다 _**직접 편집되지 않음**_. 예를 들어, 이 무효화는 카탈로그에서 범주에 지정된 제품을 편집하거나 관련 제품 규칙을 변경할 때 발생합니다.

캐시를 지운 후에는 항상 브라우저를 새로 고쳐 최신 파일이 보이는지 확인합니다. 상거래 캐시를 지워도 웹 브라우저 캐시가 지워지지 않습니다. 업데이트된 콘텐츠를 보려면 브라우저 캐시를 지워야 할 수 있습니다.

Adobe Commerce 캐싱에 대한 추가 기술 정보는 [캐시 개요](https://developer.adobe.com/commerce/frontend-core/guide/caching/){:target=&quot;_blank&quot;} _Commerce 프론트엔드 개발 안내서_.

액세스 _[!UICONTROL Cache Management]_다음 중 하나를 수행하여 페이지를 만듭니다.

- 다음을 클릭합니다. **[!UICONTROL Cache Management]** 작업 영역 위의 메시지에 있는 링크.
- 다음에서 _관리자_ 사이드바, 이동 **[!UICONTROL System]** > _[!UICONTROL Tools]_>**[!UICONTROL Cache Management]**.

![캐시 관리](./assets/cache-management-invalid.png){width="700" zoomable="yes"}

## 캐싱 우수 사례

리인덱싱과 캐싱은 Commerce에서 다른 용도로 사용됩니다. [색인](index-management.md) 데이터베이스 정보를 추적하여 검색 성능 향상, 상점 데이터 검색 속도 향상 등의 이점을 얻을 수 있습니다. 캐시는 로드된 데이터, 이미지, 형식 등을 저장하여 저장소의 성능 로드 및 액세스 성능을 향상시킵니다.

- 확장/모듈을 설치한 후 항상 캐시를 플러시합니다. 확장을 하나 이상 설치한 다음 캐시를 플러시할 수 있습니다.
- Commerce를 설치한 후 캐시를 플러시합니다. 새로 설치하는 경우 색인을 다시 지정해야 합니다.
- Open Source 또는 Commerce 버전을 다른 버전으로 업그레이드한 후 캐시를 플러시합니다.
- 캐시를 플러시할 때는 캐시 유형을 고려하고 피크 시간이 아닌 동안 플러시를 예약하십시오. 예를 들어 늦은 밤이나 이른 아침과 같이 사이트를 사용하는 고객이 적은 시간을 선택합니다. 최대 수요 동안 캐시 유형을 지우면 관리자의 로드가 증가하고 작업이 완료될 때까지 사이트가 다운될 수 있습니다.
- 날짜 [리인덱싱](index-management.md), 캐시를 플러시할 필요가 없습니다.

## 캐시 관리 역할 리소스

캐시를 보고, 전환하고, 플러시하는 옵션을 포함하여 역할별로 사용자에게 특정 캐시 유지 관리 작업에 대한 액세스 권한을 할당할 수 있습니다. Adobe은 관리자 수준 사용자에 대해서만 플러시 작업을 활성화할 것을 권장합니다. 모든 캐시 관리 기능에 대한 액세스 권한을 제공하면 상점 성능에 영향을 줄 수 있습니다.

![역할 리소스 - 캐시 관리](./assets/permissions-role-resources-cache-management.png){width="600" zoomable="yes"}

관리자 사용자 계정에 대한 액세스 권한을 부여할 리소스 지정에 대한 자세한 내용은 [역할 리소스](permissions-user-roles.md#role-resources). 다음 리소스는 캐시 관리 도구에 대한 액세스를 제어합니다.

- [!UICONTROL Clean Cache Actions]

   - [!UICONTROL Flush Cache Storage]
   - [!UICONTROL Flush Magento Cache]

- [!UICONTROL Cache Type Management]

   - [!UICONTROL Toggle Cache Type]
   - [!UICONTROL Refresh Cache Type]

- [!UICONTROL Additional Cache Management]

   - [!UICONTROL Catalog Images Cache]
   - [!UICONTROL Flush Js/Css]
   - [!UICONTROL Flush Static Files]

## 특정 캐시 새로 고침

1. 새로 고침할 각 캐시에 대해 행의 시작 부분에 있는 확인란을 선택합니다.

1. 설정 **[!UICONTROL Actions]** 끝 `Refresh` 및 클릭 **[!UICONTROL Submit]**.

## 대량 작업 새로 고침 수행

1. 캐시 그룹을 선택하려면 를 설정합니다 **[!UICONTROL Mass Actions]** 다음 중 하나를 수행합니다.

   - `Select All`
   - `Select Visible`

1. 새로 고칠 각 캐시에 대한 확인란을 선택합니다.

1. 설정 **[!UICONTROL Actions]** 끝 `Refresh` 및 클릭 **[!UICONTROL Submit]**.

## 제품 이미지 캐시 초기화

1. 아래 _[!UICONTROL Additional Cache Management]_, 클릭&#x200B;**[!UICONTROL Flush Catalog Images Cache]**미리 생성된 제품 이미지 파일을 지웁니다.

   다음 `Image cache was cleaned` 작업 영역 상단에 메시지가 표시됩니다.

1. 브라우저의 캐시를 지웁니다.

## JavaScript/CSS 캐시 플러시

1. 아래 _[!UICONTROL Additional Cache Management]_를 클릭하고, 를 클릭하여 단일 파일로 병합된 Javascript 및 CSS 파일을 지웁니다.**[!UICONTROL Flush JavaScript/CSS Cache]**.

   다음 `The JavaScript/CSS cache has been cleaned` 작업 영역 상단에 메시지가 표시됩니다.

1. 브라우저의 캐시를 지웁니다.

## 명령줄을 사용하여 플러시

Commerce 애플리케이션 서버에 액세스할 수 있는 시스템 관리자 및 개발자도 Commerce CLI를 사용하여 명령줄에서 캐시 및 캐시 구성을 관리할 수 있습니다. 다음을 참조하십시오 [캐시 관리](https://experienceleague.adobe.com/en/docs/commerce-operations/configuration-guide/cli/manage-cache#clean-and-flush-cache-types){:target=&quot;_blank&quot;} _구성 안내서_.

## 컨트롤

| 제어 | 설명 |
|---------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Mass Actions] | 여러 캐시의 확인란을 선택합니다. 옵션: <br/>**[!UICONTROL Select All]**— 모든 캐시의 확인란을 선택합니다.<br/>**&#x200B;모두 선택 해제&#x200B;**— 모든 캐시의 확인란을 지웁니다.<br/>**[!UICONTROL Select Visible]** — 표시되는 모든 캐시의 확인란을 선택합니다. <br/>**[!UICONTROL Unselect Visible]**— 표시되는 모든 캐시의 확인란을 지웁니다. |
| [!UICONTROL Actions] | 선택한 모든 캐시에 적용할 작업을 결정합니다. 옵션: <br/>**[!UICONTROL Enable]**— 선택한 모든 캐시를 활성화합니다.<br/>**[!UICONTROL Disable]** — 선택한 모든 캐시를 비활성화합니다. <br/>**[!UICONTROL Refresh]**— 선택한 모든 캐시를 새로 고칩니다. |
| [!UICONTROL Submit] | 선택한 모든 캐시에 작업을 적용합니다. |

{style="table-layout:auto"}

### 버튼

| 단추 | 설명 |
|-----------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Flush Magento Cache] | 기본 상거래 캐시의 모든 항목 제거(`var/cache`)를 클릭하여 제품에서 사용할 수 있습니다. |
| [!UICONTROL Flush Cache Storage] | Commerce 태그에 관계없이 캐시에서 모든 항목을 제거합니다. 시스템에서 대체 캐시 위치를 사용하는 경우 다른 애플리케이션에서 사용하는 캐시된 파일은 프로세스에서 제거됩니다. |
| [!UICONTROL Flush Catalog Images Cache] | 에 저장된 자동 크기 조정 및 워터마크가 지정된 모든 카탈로그 이미지 제거 `media/catalog/product/cache`. 최근에 업로드한 이미지가 카탈로그에 반영되지 않은 경우 카탈로그를 플러시하고 브라우저를 새로 고치십시오. |
| [!UICONTROL Flush JavaScript/CSS Cache] | 캐시에서 JavaScript 및 CSS 파일의 병합된 복사본을 제거합니다. 스타일 시트 또는 JavaScript에 대한 최근 변경 내용이 스토어에 반영되지 않은 경우 JavaScript/CSS 캐시를 플러시하고 브라우저를 새로 고치십시오. |
| [!UICONTROL Flush Static Files Cache] | 사전 처리된 보기 파일 및 정적 파일을 제거합니다. |

{style="table-layout:auto"}

### 캐시

다음 [!UICONTROL Cache Management] 현재 상태로 관리자에서 관리할 수 있는 캐시 유형이 페이지에 나열됩니다. 이 섹션에서는 Adobe Commerce에서 지원하는 기본 캐시 유형을 설명합니다. 다음 _캐시 태그_ 및 _캐시 ID_ 열은 Commerce 애플리케이션 코드에 사용된 값을 설명합니다.

- `cache_type_id` 캐시 유형에 대한 고유 식별자를 정의합니다.

- `%CACHE_TYPE_TAG%` 캐시 유형 범위 지정에 사용할 고유 태그를 정의합니다.

개발자와 시스템 통합자는 Adobe Commerce을 사용자 정의하거나 통합(예: GraphQL API를 사용한 통합 개발)할 때 이러한 값을 사용하여 캐싱을 구성하고 관리합니다. 다음 `cache type id` Commerce CLI를 사용하여 application server 명령줄에서 캐시를 관리하는 데에도 사용됩니다. 예를 들어, ` bin/magento cache:status config` 구성 캐시의 현재 상태를 표시합니다.

>[!NOTE]
>
>개발자와 시스템 통합자는 Commerce 캐시 관리 시스템을 사용자 정의하고 확장하여 사용자 정의 모듈 및 통합을 지원할 수 있습니다. 자세한 내용은 [캐싱 구성](https://experienceleague.adobe.com/en/docs/commerce-operations/configuration-guide/cache/caching-overview) 다음에서 _Adobe Commerce 구성 안내서_.

<!-- prettier-ignore -->

#### 캐시 목록 세부 정보

| 캐시 | 설명 | 캐시 태그 | 캐시 ID |
|-------|------------|----------|----------|
| [!UICONTROL Configuration] | Commerce는 모든 모듈에서 XML 구성을 수집하고 병합한 다음 병합된 결과를 캐시에 저장합니다.<br>**[!UICONTROL System]**-  `config.xml`,`local.xml`<br>**[!UICONTROL Module]** - `config.xml`<br><br>또한 이 캐시에는 파일 시스템 및 데이터베이스에 저장된 저장소 관련 설정이 포함되어 있습니다. 구성 파일을 수정한 후 이 캐시 유형을 정리하거나 플러시합니다. | `CONFIG` | `config` |
| [!UICONTROL Layouts] | 컴파일된 페이지 레이아웃(모든 구성 요소의 레이아웃 구성 요소)입니다. 레이아웃 파일을 수정한 후 이 캐시 유형을 정리하거나 플러시합니다. | `LAYOUT_GENERAL_CACHE_TAG` | `layout` |
| [!UICONTROL Blocks HTML output] | 블록당 HTML 페이지 조각. 보기 레이어를 수정한 후 이 캐시 유형을 정리하거나 플러시합니다. | `BLOCK_HTML` | `block_html` |
| [!UICONTROL Collections Data] | 데이터베이스 쿼리의 결과를 저장하는 컬렉션 데이터 파일입니다. 필요한 경우 Commerce가 이 캐시를 자동으로 정리하지만 서드파티 개발자는 캐시의 모든 세그먼트에 데이터를 배치할 수 있습니다. 사용자 지정 모듈에서 Commerce에서 정리할 수 없는 캐시 항목을 생성하는 논리를 사용하는 경우 이 캐시 유형을 정리하거나 플러시합니다. | `COLLECTION_DATA` | `collections` |
| [!UICONTROL Reflections] | 일반적으로 런타임 중에 생성되는 API 인터페이스 리플렉션 데이터를 지웁니다. | `REFLECTION` | `reflection` |
| `Database DDL operations` | 데이터베이스 스키마. 필요한 경우 Commerce가 이 캐시를 자동으로 정리하지만 서드파티 개발자는 캐시의 모든 세그먼트에 데이터를 배치할 수 있습니다. 데이터베이스 스키마를 사용자 지정 변경한 후 이 캐시 유형을 정리하거나 플러시합니다. 즉, Commerce가 자체적으로 만들지 않는 업데이트입니다. 데이터베이스 스키마를 자동으로 업데이트하는 한 가지 방법은 magento 설정을 사용하는 것입니다:db-schema:upgrade 명령. | `DB_DDL` | `db_ddl` |
| [!UICONTROL Compiled Config] | 코드 컴파일 결과. | `COMPILED_CONFIG` | `compiled_config` |
| [!UICONTROL Webhooks Response Cache] | 웹후크 요청에 대한 응답을 캐시합니다. 자세한 내용은 [Webhooks 안내서](https://developer.adobe.com/commerce/extensibility/webhooks/release-notes/#enhancements-2) Commerce 개발자 설명서에서 참조하십시오. | `WEBHOOKS_RESPONSE` | `webhooks_response` |
| [!UICONTROL EAV types and attributes] | EAV(엔티티 속성 값) 속성과 관련된 메타데이터에 대한 엔티티 유형 선언을 캐시합니다. 속성에는 스토어 레이블, 관련 PHP 코드에 대한 링크, 속성 렌더링, 검색 설정 등이 포함됩니다. 일반적으로 이 캐시 유형을 정리하거나 플러시할 필요가 없습니다. | `EAV` | `eav` |
| [!UICONTROL Customer Notification] | 사용자 인터페이스에 표시되는 임시 알림입니다. | `CUSTOMER_NOTIFICATION` | `customer_notification` |
| [!UICONTROL GraphQL Query Resolver Results] | 고객, CMS 페이지, CMS 블록 및 제품 미디어 갤러리 엔터티를 위한 GraphQL 쿼리 확인자의 결과를 캐시합니다. GraphQL 성능을 향상시키기 위해 이 캐시를 활성화 상태로 유지합니다. | `GRAPHQL_QUERY_RESOLVER_RESULT` | `graphql_query_resolver_result` |
| [!UICONTROL Integrations Configuration] | 통합 구성 파일입니다. 통합을 변경하거나 추가한 후 이 캐시를 지우거나 플러시합니다. | `INTEGRATION` | `config_integration` |
| [!UICONTROL Integrations API Configuration] | 스토어 통합을 위해 컴파일된 통합 API 구성입니다. | `INTEGRATION_API_CONFIG` | `config_integration_api` |
| [!UICONTROL Admin UI SDK Cache] | 관리자가 사용자 지정한 내용을 캐시합니다. 다음을 참조하십시오 [관리자 구성 및 테스트](https://developer.adobe.com/commerce/extensibility/admin-ui-sdk/configuration/) 다음에서 _관리자 UI SDK 안내서_. | `ADMIN_UI_SDK` | `admin_ui_sdk` |
| [!UICONTROL Page Cache] | 전체 페이지 캐싱. | `FPC` | `full_page` |
| [!UICONTROL Target Rule] | 대상 규칙 색인 | `TARGET_RULE` | `target_rule` |
| [!UICONTROL Web Services Configuration] | 웹 API 구조 캐싱. | `WEBSERVICE` | `config_webservice` |
| [!UICONTROL Translations] | 번역 파일. | `TRANSLATE` | `translate` |

{style="table-layout:auto"}

## 전체 페이지 캐싱

Adobe Commerce 및 Magento Open Source은 서버에서 전체 페이지 캐싱을 사용하여 범주, 제품 및 CMS 페이지를 신속하게 표시합니다. 전체 페이지 캐싱은 응답 시간을 향상시키고 서버의 로드를 줄입니다. 캐싱을 사용하지 않으면 각 페이지에서 코드 블록을 실행하고 데이터베이스에서 정보를 검색해야 할 수 있습니다. 그러나 전체 페이지 캐싱이 활성화되면 캐시에서 직접 완전히 생성된 페이지를 읽을 수 있습니다.

>[!NOTE]
>
>다음을 권장합니다. [바니시 캐시](https://varnish-cache.org/){:target=&quot;_blank&quot;}는 프로덕션 환경에서만 사용할 수 있습니다.

캐시된 콘텐츠를 사용하여 유사한 유형의 방문에서 요청을 처리할 수 있습니다. 따라서 일반 방문자에게 표시되는 페이지는 고객에게 표시되는 페이지와 다를 수 있습니다. 캐싱을 위해 각 방문은 다음 세 가지 유형 중 하나입니다.

- `Non-sessioned` - 비방문 기간 동안 쇼핑객은 페이지를 보지만 스토어와 상호 작용하지 않습니다. 시스템은 본 각 페이지의 콘텐츠를 캐시하고 다른 비세션 쇼핑객에게 제공합니다.
- `Sessioned` - 세션 방문 중에 스토어와 상호 작용하는 쇼핑객에게는 세션 ID가 지정됩니다. 상호 작용에는 제품 비교나 장바구니에 제품 추가와 같은 활동이 포함됩니다. 세션 중에 생성된 캐시된 페이지는 세션 중에 해당 쇼핑객만 사용됩니다.
- `Customer` - 고객 세션은 등록된 계정을 사용하여 로그인하고 쇼핑하는 고객을 위해 생성됩니다. 세션 중에 고객에게 할당된 고객 그룹에 따라 특별 오퍼, 프로모션 및 가격을 제공할 수 있습니다.

기술 정보는 다음을 참조하십시오. [바니시 구성 및 사용](https://experienceleague.adobe.com/docs/commerce-operations/configuration-guide/cache/varnish/config-varnish.html){:target=&quot;_blank&quot;} 및 [상거래 페이지 및 기본 캐시에 Redis 사용](https://experienceleague.adobe.com/docs/commerce-operations/configuration-guide/cache/redis/redis-pg-cache.html){:target=&quot;_blank&quot;} _구성 안내서_.

**_전체 페이지 캐시를 구성하려면 다음을 수행합니다._**

1. 다음에서 _관리자_ 사이드바, 이동 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. 왼쪽 패널에서 를 확장합니다. **[!UICONTROL Advanced]** 및 선택 **[!UICONTROL System]**.

1. 확장 ![확장 선택기](../assets/icon-display-expand.png) 다음 **[!UICONTROL Full Page Cache]** 섹션.

   ![고급 구성 - 전체 페이지 캐시](../configuration-reference/advanced/assets/system-full-page-cache.png){width="600" zoomable="yes"}

1. 설정 **[!UICONTROL Caching Application]** 다음 중 하나를 수행합니다.

   - `Built-in Application`
   - `Varnish Caching`

1. 페이지 캐시에 대한 시간 제한을 설정하려면 **[!UICONTROL TTL for public content]**. (기본값은 입니다. `86400`)

1. 의 최대 수를 지정하려면 [레이아웃 핸들](https://developer.adobe.com/commerce/frontend-core/guide/layouts/#layout-handles) 을(를) 처리하려면 [`{BASE-URL}/page_cache/block/esi`](https://experienceleague.adobe.com/docs/commerce-operations/configuration-guide/cache/use-varnish-esi.html) HTTP 끝점을 입력합니다. **[!UICONTROL Handles param size]**. 크기를 제한하면 보안과 성능을 향상시킬 수 있습니다. (기본값은 입니다. `100`)

1. Vanish를 사용하는 경우 다음을 완료합니다. **[!UICONTROL Varnish Configuration]** 다음과 같은 섹션:

   - **[!UICONTROL Access list]** - Varnish 구성을 제거하여 구성 파일을 생성할 수 있는 IP 주소를 입력합니다. 여러 항목은 쉼표로 구분하십시오. 기본값은 입니다. `localhost`.

   - **[!UICONTROL Backend host]** - 구성 파일을 생성하는 백엔드 호스트의 IP 주소를 입력합니다. 기본값은 입니다. `localhost`.

   - **[!UICONTROL Backend port]** - 구성 파일을 생성하는 데 사용되는 백엔드 포트를 식별합니다. 기본값은 다음과 같습니다. `8080`.

   - **[!UICONTROL Grace period]** - 구성 파일을 생성하기 위한 유예 기간으로 사용할 시간(초)을 지정합니다. 다음을 참조하십시오 [고급 바니시 구성](https://experienceleague.adobe.com/docs/commerce-operations/configuration-guide/cache/config-varnish-advanced.html) 다음에서 _구성 안내서_.

   - 구성을 로 내보내려면 `varnish.vcl` 파일에서 사용하는 바니시 버전 버튼을 클릭합니다.

   ![고급 구성 - 전체 페이지 캐시 바니시](../configuration-reference/advanced/assets/system-full-page-cache-varnish.png){width="600" zoomable="yes"}

1. 완료되면 다음을 클릭하십시오. **[!UICONTROL Save Config]**.
