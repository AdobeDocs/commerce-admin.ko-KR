---
title: 캐시 관리
description: 사이트의 성능을 개선하는 쉬운 방법을 제공하는 캐시 관리 도구를 사용하는 방법에 대해 알아봅니다.
exl-id: c87f85ca-81b9-4cbf-9817-3d779397eefd
feature: Cache, System
badgePaas: label="PaaS만" type="Informative" url="https://experienceleague.adobe.com/ko/docs/commerce/user-guides/product-solutions" tooltip="Adobe Commerce 온 클라우드 프로젝트(Adobe 관리 PaaS 인프라) 및 온프레미스 프로젝트에만 적용됩니다."
source-git-commit: 9a68d9702cec9b812414d39e8d04c71751121a37
workflow-type: tm+mt
source-wordcount: '1845'
ht-degree: 0%

---

# 캐시 관리

Adobe Commerce 및 Magento Open Source 캐시 관리 시스템은 사이트의 성능을 개선하는 쉬운 방법을 제공합니다. 캐시를 새로 고쳐야 할 때마다 새로 고침을 완료할 수 있도록 [!UICONTROL Cache Management] 페이지에 대한 링크가 포함된 알림이 표시됩니다.

![제품 특성 저장 - 캐시 메시지 업데이트](./assets/product-attribute-save-msg-update-cache.png){width="500"}

_[!UICONTROL Cache Management]_&#x200B;페이지에는 각 기본 캐시의 상태와 연결된 태그가 표시됩니다. 오른쪽 상단의 큰 버튼을 사용하여 캐시 또는 모든 항목이 포함된 캐시 저장소를 플러시할 수 있습니다. 페이지 하단에서 추가 버튼을 사용하여 카탈로그 제품 이미지 캐시와 JavaScript/CSS 캐시를 플러시할 수 있습니다.

>[!IMPORTANT]
>
>카탈로그 엔티티가 변경되면 다른 페이지에 영향을 줄 수 있으며 여러 캐시를 동시에 무효화할 수 있습니다. 캐시 관리 페이지를 검토할 때 새로 고침이 필요한 잘못된 항목이 _&#x200B;**직접 편집되지 않음**&#x200B;_&#x200B;일 때 표시될 수 있습니다. 예를 들어, 이 무효화는 카탈로그에서 범주에 지정된 제품을 편집하거나 관련 제품 규칙을 변경할 때 발생합니다.

캐시를 지운 후에는 항상 브라우저를 새로 고쳐 최신 파일이 보이는지 확인합니다. Commerce 캐시를 지워도 웹 브라우저 캐시가 지워지지 않습니다. 업데이트된 콘텐츠를 보려면 브라우저 캐시를 지워야 할 수 있습니다.

Adobe Commerce 캐싱에 대한 추가 기술 정보는 _Commerce 프론트엔드 개발 안내서_&#x200B;의 [캐시 개요](https://developer.adobe.com/commerce/frontend-core/guide/caching/){:target="_blank"}에서 확인할 수 있습니다.

다음 중 하나를 수행하여 _[!UICONTROL Cache Management]_&#x200B;페이지에 액세스합니다.

- 작업 영역 위의 메시지에서 **[!UICONTROL Cache Management]** 링크를 클릭합니다.
- _관리자_ 사이드바에서 **[!UICONTROL System]** > _[!UICONTROL Tools]_>**[!UICONTROL Cache Management]**(으)로 이동합니다.

![캐시 관리](./assets/cache-management-invalid.png){width="700" zoomable="yes"}

## 캐싱 우수 사례

리인덱싱과 캐싱은 Commerce에서 서로 다른 목적을 가지고 있습니다. [인덱스](index-management.md)은(는) 데이터베이스 정보를 추적하여 검색 성능을 높이고 상점 데이터를 더 빠르게 검색하는 등의 작업을 수행합니다. 캐시는 로드된 데이터, 이미지, 형식 등을 저장하여 저장소의 성능 로드 및 액세스 성능을 향상시킵니다.

- 확장/모듈을 설치한 후 항상 캐시를 플러시합니다. 확장을 하나 이상 설치한 다음 캐시를 플러시할 수 있습니다.
- Commerce 설치 후 캐시를 플러시합니다. 새로 설치하는 경우 색인을 다시 지정해야 합니다.
- 열린 Source 또는 Commerce의 한 버전에서 다른 버전으로 업그레이드한 후 캐시를 플러시합니다.
- 캐시를 플러시할 때는 캐시 유형을 고려하고 피크 시간이 아닌 동안 플러시를 예약하십시오. 예를 들어 늦은 밤이나 이른 아침과 같이 사이트를 사용하는 고객이 적은 시간을 선택합니다. 최대 수요 동안 캐시 유형을 지우면 관리자의 로드가 증가하고 작업이 완료될 때까지 사이트가 다운될 수 있습니다.
- [리인덱싱](index-management.md)하는 경우 캐시를 플러시할 필요가 없습니다.

## 캐시 관리 역할 리소스

캐시를 보고, 전환하고, 플러시하는 옵션을 포함하여 역할별로 사용자에게 특정 캐시 유지 관리 작업에 대한 액세스 권한을 할당할 수 있습니다. Adobe에서는 관리자 수준 사용자에 대해서만 플러시 작업을 활성화할 것을 권장합니다. 모든 캐시 관리 기능에 대한 액세스 권한을 제공하면 상점 성능에 영향을 줄 수 있습니다.

![역할 리소스 - 캐시 관리](./assets/permissions-role-resources-cache-management.png){width="600" zoomable="yes"}

관리자 사용자 계정에 대한 액세스 권한을 부여할 리소스를 할당하는 방법에 대한 자세한 내용은 [역할 리소스](permissions-user-roles.md#role-resources)를 참조하십시오. 다음 리소스는 캐시 관리 도구에 대한 액세스를 제어합니다.

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

1. **[!UICONTROL Actions]**&#x200B;을(를) `Refresh`(으)로 설정하고 **[!UICONTROL Submit]**&#x200B;을(를) 클릭합니다.

## 대량 작업 새로 고침 수행

1. 캐시 그룹을 선택하려면 **[!UICONTROL Mass Actions]**&#x200B;을(를) 다음 중 하나로 설정하십시오.

   - `Select All`
   - `Select Visible`

1. 새로 고칠 각 캐시에 대한 확인란을 선택합니다.

1. **[!UICONTROL Actions]**&#x200B;을(를) `Refresh`(으)로 설정하고 **[!UICONTROL Submit]**&#x200B;을(를) 클릭합니다.

## 제품 이미지 캐시 초기화

1. _[!UICONTROL Additional Cache Management]_&#x200B;에서&#x200B;**[!UICONTROL Flush Catalog Images Cache]**&#x200B;을(를) 클릭하여 미리 생성된 제품 이미지 파일을 지웁니다.

   작업 영역 맨 위에 `Image cache was cleaned` 메시지가 나타납니다.

1. 브라우저의 캐시를 지웁니다.

## JavaScript/CSS 캐시 플러시

1. _[!UICONTROL Additional Cache Management]_&#x200B;에서&#x200B;**[!UICONTROL Flush JavaScript/CSS Cache]**&#x200B;을(를) 클릭하여 단일 파일로 병합된 Javascript 및 CSS 파일을 지웁니다.

   작업 영역 맨 위에 `The JavaScript/CSS cache has been cleaned` 메시지가 나타납니다.

1. 브라우저의 캐시를 지웁니다.

## 명령줄을 사용하여 플러시

Commerce 애플리케이션 서버에 대한 액세스 권한이 있는 시스템 관리자 및 개발자는 Commerce CLI를 사용하여 명령줄에서 캐시 및 캐시 구성을 관리할 수도 있습니다. _구성 가이드_&#x200B;에서 [캐시 관리](https://experienceleague.adobe.com/ko/docs/commerce-operations/configuration-guide/cli/manage-cache#clean-and-flush-cache-types){:target="_blank"}를 참조하십시오.

## 컨트롤

| 제어 | 설명 |
|---------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Mass Actions] | 여러 캐시의 확인란을 선택합니다. 옵션: <br/>**[!UICONTROL Select All]**— 모든 캐시의 확인란을 선택합니다.<br/>**&#x200B;모두 선택 해제&#x200B;**— 모든 캐시의 확인란을 지웁니다.<br/>**[!UICONTROL Select Visible]** — 보이는 모든 캐시의 확인란을 선택합니다. <br/>**[!UICONTROL Unselect Visible]**— 표시되는 모든 캐시의 확인란을 지웁니다. |
| [!UICONTROL Actions] | 선택한 모든 캐시에 적용할 작업을 결정합니다. 옵션: <br/>**[!UICONTROL Enable]**— 선택한 모든 캐시를 활성화합니다.<br/>**[!UICONTROL Disable]** — 선택한 모든 캐시를 비활성화합니다. <br/>**[!UICONTROL Refresh]**— 선택한 모든 캐시를 새로 고칩니다. |
| [!UICONTROL Submit] | 선택한 모든 캐시에 작업을 적용합니다. |

{style="table-layout:auto"}

### 버튼

| 단추 | 설명 |
|-----------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Flush Magento Cache] | 연결된 Commerce 태그에 따라 기본 Commerce 캐시(`var/cache`)의 모든 항목을 제거합니다. |
| [!UICONTROL Flush Cache Storage] | Commerce 태그에 관계없이 캐시에서 모든 항목을 제거합니다. 시스템에서 대체 캐시 위치를 사용하는 경우 다른 애플리케이션에서 사용하는 캐시된 파일은 프로세스에서 제거됩니다. |
| [!UICONTROL Flush Catalog Images Cache] | `media/catalog/product/cache`에 저장된 자동으로 크기가 조정되고 워터마크가 지정된 모든 카탈로그 이미지를 제거합니다. 최근에 업로드한 이미지가 카탈로그에 반영되지 않은 경우 카탈로그를 플러시하고 브라우저를 새로 고치십시오. |
| [!UICONTROL Flush JavaScript/CSS Cache] | 캐시에서 JavaScript 및 CSS 파일의 병합된 복사본을 제거합니다. 스타일시트 또는 JavaScript의 최근 변경 내용이 스토어에 반영되지 않으면 JavaScript/CSS 캐시를 플러시하고 브라우저를 새로 고치십시오. |
| [!UICONTROL Flush Static Files Cache] | 사전 처리된 보기 파일 및 정적 파일을 제거합니다. |

{style="table-layout:auto"}

### 캐시

[!UICONTROL Cache Management] 페이지에는 관리자가 현재 상태로 관리할 수 있는 캐시 형식이 나열됩니다. 이 섹션에서는 Adobe Commerce에서 지원하는 기본 캐시 유형을 설명합니다. _캐시 태그_ 및 _캐시 ID_ 열은 Commerce 응용 프로그램 코드에 사용된 값을 설명합니다.

- `cache_type_id`은(는) 캐시 유형의 고유 식별자를 정의합니다.

- `%CACHE_TYPE_TAG%`은(는) 캐시 유형 범위 지정에 사용할 고유한 태그를 정의합니다.

개발자와 시스템 통합자는 Adobe Commerce을 사용자 정의하거나 통합(예: GraphQL API를 사용한 통합 개발)할 때 이러한 값을 사용하여 캐싱을 구성하고 관리합니다.

[!BADGE PaaS 전용]{type=Informative url="https://experienceleague.adobe.com/ko/docs/commerce/user-guides/product-solutions" tooltip="Adobe Commerce 온 클라우드 프로젝트(Adobe 관리 PaaS 인프라) 및 온프레미스 프로젝트에만 적용됩니다."} `cache_type_id`은(는) Commerce CLI를 사용하여 응용 프로그램 서버 명령줄에서 캐시 관리에도 사용됩니다. 예를 들어 ` bin/magento cache:status config`은(는) 구성 캐시의 현재 상태를 표시합니다.

>[!NOTE]
>
>개발자와 시스템 통합자는 Commerce 캐시 관리 시스템을 사용자 정의 및 확장하여 사용자 정의 모듈 및 통합을 지원할 수 있습니다. 자세한 내용은 _Adobe Commerce 구성 가이드_&#x200B;에서 [캐싱 구성](https://experienceleague.adobe.com/ko/docs/commerce-operations/configuration-guide/cache/caching-overview)을 참조하십시오.

<!-- prettier-ignore -->

#### 캐시 목록 세부 정보

| 캐시 | 설명 | 캐시 태그 | 캐시 ID |
|-------|------------|----------|----------|
| [!UICONTROL Configuration] | Commerce은 모든 모듈에서 XML 구성을 수집하고 병합한 다음 병합된 결과를 캐시에 저장합니다.<br>**[!UICONTROL System]**- `config.xml`,`local.xml`<br>**[!UICONTROL Module]** - `config.xml`<br><br>이 캐시에는 파일 시스템 및 데이터베이스에 저장된 저장소 관련 설정도 포함되어 있습니다. 구성 파일을 수정한 후 이 캐시 유형을 정리하거나 플러시합니다. | `CONFIG` | `config` |
| [!UICONTROL Layouts] | 컴파일된 페이지 레이아웃(모든 구성 요소의 레이아웃 구성 요소)입니다. 레이아웃 파일을 수정한 후 이 캐시 유형을 정리하거나 플러시합니다. | `LAYOUT_GENERAL_CACHE_TAG` | `layout` |
| [!UICONTROL Blocks HTML output] | 블록당 HTML 페이지 조각. 보기 레이어를 수정한 후 이 캐시 유형을 정리하거나 플러시합니다. | `BLOCK_HTML` | `block_html` |
| [!UICONTROL Collections Data] | 데이터베이스 쿼리의 결과를 저장하는 컬렉션 데이터 파일입니다. 필요한 경우 Commerce이 이 캐시를 자동으로 정리하지만 서드파티 개발자는 캐시의 모든 세그먼트에 데이터를 배치할 수 있습니다. 사용자 정의 모듈이 Commerce에서 정리할 수 없는 캐시 항목을 생성하는 논리를 사용하는 경우 이 캐시 유형을 정리하거나 플러시합니다. | `COLLECTION_DATA` | `collections` |
| [!UICONTROL Reflections] | 일반적으로 런타임 중에 생성되는 API 인터페이스 리플렉션 데이터를 지웁니다. | `REFLECTION` | `reflection` |
| `Database DDL operations` | 데이터베이스 스키마. 필요한 경우 Commerce이 이 캐시를 자동으로 정리하지만 서드파티 개발자는 캐시의 모든 세그먼트에 데이터를 배치할 수 있습니다. 데이터베이스 스키마를 사용자 지정 변경한 후 이 캐시 유형을 정리하거나 플러시합니다. (즉, Commerce이 자체적으로 만들지 않는 업데이트입니다.) 데이터베이스 스키마를 자동으로 업데이트하는 한 가지 방법은 magento setup:db-schema:upgrade 명령을 사용하는 것입니다. | `DB_DDL` | `db_ddl` |
| [!UICONTROL Compiled Config] | 코드 컴파일 결과. | `COMPILED_CONFIG` | `compiled_config` |
| [!UICONTROL Webhooks Response Cache] | 웹후크 요청에 대한 응답을 캐시합니다. 자세한 내용은 Commerce 개발자 설명서에서 [Webhooks 안내서](https://developer.adobe.com/commerce/extensibility/webhooks/release-notes/#enhancements-2)를 참조하십시오. | `WEBHOOKS_RESPONSE` | `webhooks_response` |
| [!UICONTROL EAV types and attributes] | EAV(엔티티 속성 값) 속성과 관련된 메타데이터에 대한 엔티티 유형 선언을 캐시합니다. 속성에는 스토어 레이블, 관련 PHP 코드에 대한 링크, 속성 렌더링, 검색 설정 등이 포함됩니다. 일반적으로 이 캐시 유형을 정리하거나 플러시할 필요가 없습니다. | `EAV` | `eav` |
| [!UICONTROL Customer Notification] | 사용자 인터페이스에 표시되는 임시 알림입니다. | `CUSTOMER_NOTIFICATION` | `customer_notification` |
| [!UICONTROL GraphQL Query Resolver Results] | 고객, CMS 페이지, CMS 블록 및 제품 미디어 갤러리 엔터티를 위한 GraphQL 쿼리 확인자의 결과를 캐시합니다. GraphQL 성능을 향상시키기 위해 이 캐시를 활성화 상태로 유지합니다. | `GRAPHQL_QUERY_RESOLVER_RESULT` | `graphql_query_resolver_result` |
| [!UICONTROL Integrations Configuration] | 통합 구성 파일입니다. 통합을 변경하거나 추가한 후 이 캐시를 지우거나 플러시합니다. | `INTEGRATION` | `config_integration` |
| [!UICONTROL Integrations API Configuration] | 스토어 통합을 위해 컴파일된 통합 API 구성입니다. | `INTEGRATION_API_CONFIG` | `config_integration_api` |
| [!UICONTROL Admin UI SDK Cache] | 관리자가 사용자 지정한 내용을 캐시합니다. _관리 UI SDK 안내서_&#x200B;에서 [관리 구성 및 테스트](https://developer.adobe.com/commerce/extensibility/admin-ui-sdk/configuration/)를 참조하십시오. | `ADMIN_UI_SDK` | `admin_ui_sdk` |
| [!UICONTROL Page Cache] | 전체 페이지 캐싱. | `FPC` | `full_page` |
| [!UICONTROL Target Rule] | 대상 규칙 색인 | `TARGET_RULE` | `target_rule` |
| [!UICONTROL Web Services Configuration] | 웹 API 구조 캐싱. | `WEBSERVICE` | `config_webservice` |
| [!UICONTROL Translations] | 번역 파일. | `TRANSLATE` | `translate` |

{style="table-layout:auto"}

## 전체 페이지 캐싱

Adobe Commerce 및 Magento Open Source은 서버에서 전체 페이지 캐싱을 사용하여 카테고리, 제품 및 CMS 페이지를 신속하게 표시합니다. 전체 페이지 캐싱은 응답 시간을 향상시키고 서버의 로드를 줄입니다. 캐싱을 사용하지 않으면 각 페이지에서 코드 블록을 실행하고 데이터베이스에서 정보를 검색해야 할 수 있습니다. 그러나 전체 페이지 캐싱이 활성화되면 캐시에서 직접 완전히 생성된 페이지를 읽을 수 있습니다.

>[!NOTE]
>
>[Varnish 캐시](https://varnish-cache.org/){:target="_blank"}는 프로덕션 환경에서만 사용하는 것이 좋습니다.

캐시된 콘텐츠를 사용하여 유사한 유형의 방문에서 요청을 처리할 수 있습니다. 따라서 일반 방문자에게 표시되는 페이지는 고객에게 표시되는 페이지와 다를 수 있습니다. 캐싱을 위해 각 방문은 다음 세 가지 유형 중 하나입니다.

- `Non-sessioned` - 세션을 받지 않은 방문 중에 쇼핑객이 페이지를 보지만 스토어와 상호 작용하지 않습니다. 시스템은 본 각 페이지의 콘텐츠를 캐시하고 다른 비세션 쇼핑객에게 제공합니다.
- `Sessioned` - 세션 방문 중에 스토어와 상호 작용하는 쇼핑객에게 세션 ID가 할당됩니다. 상호 작용에는 제품 비교나 장바구니에 제품 추가와 같은 활동이 포함됩니다. 세션 중에 생성된 캐시된 페이지는 세션 중에 해당 쇼핑객만 사용됩니다.
- `Customer` - 등록된 계정을 사용하여 로그인하고 쇼핑하는 고객에 대해 고객 세션이 만들어집니다. 세션 중에 고객에게 할당된 고객 그룹에 따라 특별 오퍼, 프로모션 및 가격을 제공할 수 있습니다.

자세한 내용은 _구성 가이드_&#x200B;에서 [바니시 구성 및 사용](https://experienceleague.adobe.com/docs/commerce-operations/configuration-guide/cache/varnish/config-varnish.html?lang=ko){:target="_blank"} 및 [Commerce 페이지 및 기본 캐시에 Redis 사용](https://experienceleague.adobe.com/docs/commerce-operations/configuration-guide/cache/redis/redis-pg-cache.html?lang=ko){:target="_blank"}을 참조하십시오.

**_전체 페이지 캐시를 구성하려면:_**

1. _관리자_ 사이드바에서 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**(으)로 이동합니다.

1. 왼쪽 패널에서 **[!UICONTROL Advanced]**&#x200B;을(를) 확장하고 **[!UICONTROL System]**&#x200B;을(를) 선택합니다.

1. **[!UICONTROL Full Page Cache]** 섹션에서 ![확장 선택기](../assets/icon-display-expand.png)를 확장합니다.

   ![고급 구성 - 전체 페이지 캐시](../configuration-reference/advanced/assets/system-full-page-cache.png){width="600" zoomable="yes"}

1. **[!UICONTROL Caching Application]**&#x200B;을(를) 다음 중 하나로 설정합니다.

   - `Built-in Application`
   - `Varnish Caching`

1. 페이지 캐시에 대한 시간 제한을 설정하려면 **[!UICONTROL TTL for public content]**&#x200B;을(를) 입력하십시오. (기본값은 `86400`입니다.)

1. [`{BASE-URL}/page_cache/block/esi`](https://experienceleague.adobe.com/docs/commerce-operations/configuration-guide/cache/use-varnish-esi.html?lang=ko) HTTP 끝점에서 처리할 최대 [레이아웃 핸들](https://developer.adobe.com/commerce/frontend-core/guide/layouts/#layout-handles) 수를 지정하려면 **[!UICONTROL Handles param size]**&#x200B;을(를) 입력하십시오. 크기를 제한하면 보안과 성능을 향상시킬 수 있습니다. (기본값은 `100`입니다.)

1. Vannish를 사용하는 경우 다음과 같이 **[!UICONTROL Varnish Configuration]** 섹션을 완료합니다.

   - **[!UICONTROL Access list]** - 구성 파일을 생성하기 위해 바니시 구성을 제거할 수 있는 IP 주소를 입력합니다. 여러 항목은 쉼표로 구분하십시오. 기본값은 `localhost`입니다.

   - **[!UICONTROL Backend host]** - 구성 파일을 생성하는 백 엔드 호스트의 IP 주소를 입력합니다. 기본값은 `localhost`입니다.

   - **[!UICONTROL Backend port]** - 구성 파일을 생성하는 데 사용되는 백엔드 포트를 식별합니다. 기본값은 `8080`입니다.

   - **[!UICONTROL Grace period]** - 구성 파일을 생성하는 유예 기간으로 사용할 시간(초)을 지정합니다. _구성 가이드_&#x200B;에서 [고급 바니시 구성](https://experienceleague.adobe.com/docs/commerce-operations/configuration-guide/cache/config-varnish-advanced.html?lang=ko)을 참조하십시오.

   - 구성을 `varnish.vcl` 파일로 내보내려면 사용하는 Vannish 버전에 대한 단추를 클릭합니다.

   ![고급 구성 - 전체 페이지 캐시 바니시](../configuration-reference/advanced/assets/system-full-page-cache-varnish.png){width="600" zoomable="yes"}

1. 완료되면 **[!UICONTROL Save Config]**&#x200B;을(를) 클릭합니다.
