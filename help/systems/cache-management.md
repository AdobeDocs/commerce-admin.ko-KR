---
title: 캐시 관리
description: 사이트의 성능을 개선하는 쉬운 방법을 제공하는 캐시 관리 도구를 사용하는 방법에 대해 알아봅니다.
exl-id: c87f85ca-81b9-4cbf-9817-3d779397eefd
feature: Cache, System
source-git-commit: 64ccc2d5016e915a554c2253773bb50f4d33d6f4
workflow-type: tm+mt
source-wordcount: '1422'
ht-degree: 0%

---

# 캐시 관리

Adobe Commerce 및 Magento Open Source 캐시 관리 시스템은 사이트의 성능을 개선하는 쉬운 방법을 제공합니다. 캐시를 새로 고쳐야 할 때마다 작업 영역 상단에 프로세스를 안내하는 알림이 표시됩니다. 캐시 관리 링크를 따라가서 유효하지 않은 캐시를 새로 고칩니다.

![제품 속성 저장 - 캐시 메시지 업데이트](./assets/product-attribute-save-msg-update-cache.png){width="500"}

>[!NOTE]
>
>카탈로그 엔티티가 변경되면 다른 페이지에 영향을 줄 수 있으며 여러 캐시를 동시에 무효화할 수 있습니다. 캐시 관리 페이지를 검토할 때 새로 고침이 필요한 잘못된 항목이 표시될 수 있습니다 _**직접 편집되지 않음**_. 예를 들어, 이 무효화는 카탈로그에서 제품을 편집하고 카테고리에 지정할 때 또는 관련 제품 규칙을 변경할 때 발생합니다.

다음 _[!UICONTROL Cache Management]_페이지에는 각 기본 캐시의 상태와 연관된 태그가 표시됩니다. 오른쪽 상단의 큰 버튼을 사용하여 캐시 또는 모든 항목이 포함된 캐시 저장소를 플러시할 수 있습니다. 페이지 하단에는 카탈로그 제품 이미지 캐시와 JavaScript/CSS 캐시를 플러시하는 추가 버튼이 있습니다.

캐시를 지운 후에는 항상 브라우저를 새로 고쳐 최신 파일이 보이는지 확인합니다. 상거래 캐시를 지워도 웹 브라우저 캐시가 지워지지 않습니다. 업데이트된 콘텐츠를 보려면 브라우저 캐시를 지워야 할 수 있습니다.

추가 기술 정보는 다음을 참조하십시오. [캐시 개요](https://developer.adobe.com/commerce/frontend-core/guide/caching/){:target=&quot;_blank&quot;} _Commerce 프론트엔드 개발 안내서_.

액세스 _[!UICONTROL Cache Management]_다음 중 하나를 수행하여 페이지를 만듭니다.

- 다음을 클릭합니다. **[!UICONTROL Cache Management]** 작업 영역 위의 메시지에 있는 링크.
- 다음에서 _관리자_ 사이드바, 이동 **[!UICONTROL System]** > _[!UICONTROL Tools]_>**[!UICONTROL Cache Management]**.

![캐시 관리](./assets/cache-management-invalid.png){width="700" zoomable="yes"}

## 캐싱 우수 사례

리인덱싱과 캐싱은 Commerce에서 다른 용도로 사용됩니다. [색인](index-management.md) 데이터베이스 정보를 추적하여 검색 성능 향상, 상점 데이터 검색 속도 향상 등의 이점을 얻을 수 있습니다. 캐시는 로드된 데이터, 이미지, 형식 등을 저장하여 저장소의 성능 로드 및 액세스 성능을 향상시킵니다.

- 확장/모듈을 설치한 후 항상 캐시를 플러시합니다. 확장을 하나 이상 설치한 다음 캐시를 플러시할 수 있습니다.
- Commerce를 설치한 후 캐시를 플러시합니다. 새로 설치하는 경우 색인을 다시 지정해야 합니다.
- Open Source 또는 Commerce 버전을 다른 버전으로 업그레이드한 후 캐시를 플러시합니다.
- 캐시를 플러시할 때는 캐시 유형을 고려하고 피크 시간이 아닌 동안 플러시를 예약하십시오. 예를 들어, 늦은 밤이나 이른 아침과 같이 적은 수의 고객이 사이트에 액세스할 수 있는 시간을 선택합니다. 피크 시간 동안 일부 캐시 유형을 지우면 관리자의 로드가 증가하고 완료될 때까지 사이트가 다운될 수 있습니다.
- 날짜 [리인덱싱](index-management.md)플러시 캐시를 수행할 필요도 없습니다.

## 캐시 관리 역할 리소스

특정 캐시 유지 관리 작업에 대한 액세스는 캐시를 보고, 전환하고, 플러시하는 옵션을 포함하여 역할별로 사용자에게 할당할 수 있습니다. Adobe은 관리자 수준 사용자에 대해서만 플러시 작업을 활성화할 것을 권장합니다. 모든 캐시 관리 기능에 대한 액세스 권한을 제공하면 상점 성능에 영향을 줄 수 있습니다.

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

1. 작업에서 타겟팅할 각 캐시의 확인란을 선택합니다.

1. 설정 **[!UICONTROL Actions]** 끝 `Refresh` 및 클릭 **[!UICONTROL Submit]**.

## 제품 이미지 캐시 초기화

1. 아래 _[!UICONTROL Additional Cache Management]_, 클릭&#x200B;**[!UICONTROL Flush Catalog Images Cache]**미리 생성된 제품 이미지 파일을 지웁니다.

   다음 `Image cache was cleaned` 작업 영역 상단에 메시지가 표시됩니다.

1. 브라우저의 캐시를 지웁니다.

## JavaScript/CSS 캐시 플러시

1. 아래 _[!UICONTROL Additional Cache Management]_, 클릭&#x200B;**[!UICONTROL Flush JavaScript/CSS Cache]**단일 파일로 병합된 모든 JavaScript 및 CSS 파일을 지웁니다.

   다음 `The JavaScript/CSS cache has been cleaned` 작업 영역 상단에 메시지가 표시됩니다.

1. 브라우저의 캐시를 지웁니다.

## 명령줄을 사용하여 플러시

Commerce는 명령줄을 사용하여 추가 플러시 캐시 옵션을 제공합니다. 이러한 옵션을 완료하려면 개발자 지원이 필요할 수 있습니다. 자세한 내용 및 명령 옵션은 다음을 참조하십시오. [캐시 관리](https://experienceleague.adobe.com/docs/commerce-operations/configuration-guide/cli/manage-cache.html){:target=&quot;_blank&quot;} _구성 안내서_.

## 컨트롤

| 제어 | 설명 |
|--- |--- |
| [!UICONTROL Mass Actions] | 여러 캐시의 확인란을 선택합니다. 옵션: <br/>**[!UICONTROL Select All]**— 모든 캐시의 확인란을 선택합니다.<br/>**&#x200B;모두 선택 해제&#x200B;**— 모든 캐시의 확인란을 지웁니다.<br/>**[!UICONTROL Select Visible]** — 표시되는 모든 캐시의 확인란을 선택합니다. <br/>**[!UICONTROL Unselect Visible]**— 표시되는 모든 캐시의 확인란을 지웁니다. |
| [!UICONTROL Actions] | 선택한 모든 캐시에 적용할 작업을 결정합니다. 옵션: <br/>**[!UICONTROL Enable]**— 선택한 모든 캐시를 활성화합니다.<br/>**[!UICONTROL Disable]** — 선택한 모든 캐시를 비활성화합니다. <br/>**[!UICONTROL Refresh]**— 선택한 모든 캐시를 새로 고칩니다. |
| [!UICONTROL Submit] | 선택한 모든 캐시에 작업을 적용합니다. |

{style="table-layout:auto"}

### 버튼

| 단추 | 설명 |
|--- |--- |
| [!UICONTROL Flush Magento Cache] | 기본 상거래 캐시의 모든 항목 제거(`var/cache`)를 클릭하여 제품에서 사용할 수 있습니다. |
| [!UICONTROL Flush Cache Storage] | Commerce 태그에 관계없이 캐시에서 모든 항목을 제거합니다. 시스템에서 대체 캐시 위치를 사용하는 경우 다른 애플리케이션에서 사용하는 캐시된 파일은 프로세스에서 제거됩니다. |
| [!UICONTROL Flush Catalog Images Cache] | 에 저장된 자동 크기 조정 및 워터마크가 지정된 모든 카탈로그 이미지 제거 `media/catalog/product/cache`. 최근에 업로드한 이미지가 카탈로그에 반영되지 않은 경우 카탈로그를 플러시하고 브라우저를 새로 고치십시오. |
| [!UICONTROL Flush JavaScript/CSS Cache] | 캐시에서 JavaScript 및 CSS 파일의 병합된 복사본을 제거합니다. 스타일 시트 또는 JavaScript에 대한 최근 변경 내용이 스토어에 반영되지 않은 경우 JavaScript/CSS 캐시를 플러시하고 브라우저를 새로 고치십시오. |
| [!UICONTROL Flush Static Files Cache] | 사전 처리된 보기 파일 및 정적 파일을 제거합니다. |

{style="table-layout:auto"}

### 캐시

| 캐시 | 설명 | 관련 태그 |
| ----- | ----------- | -------------- |
| [!UICONTROL Configuration] | 여러 모듈에 걸쳐 수집되고 병합된 다양한 XML 구성&#x200B;<br>**[!UICONTROL System]**-  `config.xml`,`local.xml`<br>**[!UICONTROL Module]** -  `config.xml` | `CONFIG` |
| [!UICONTROL Layouts] | 레이아웃 작성 지침. | `LAYOUT_GENERAL_CACHE_TAG` |
| [!UICONTROL Blocks HTML output] | 페이지 차단 HTML | `BLOCK_HTML` |
| [!UICONTROL Collections Data] | 컬렉션 데이터 파일입니다. | `COLLECTION_DATA` |
| [!UICONTROL Reflection Data] | 일반적으로 런타임 중에 생성되는 API 인터페이스 리플렉션 데이터를 지웁니다. | `REFLECTION` |
| [!UICONTROL Database DDL operations] | 테이블 또는 인덱스 설명과 같은 DDL 쿼리의 결과. | `DB_DDL` |
| [!UICONTROL Compiled Config] | 코드 컴파일 결과. | `COMPILED_CONFIG` |
| [!UICONTROL EAV types and attributes] | 엔터티 형식 선언 캐시입니다. | `EAV` |
| [!UICONTROL Customer Notification] | 사용자 인터페이스에 표시되는 임시 알림입니다. | `CUSTOMER_NOTIFICATION` |
| [!UICONTROL Integrations Configuration] | 통합 구성 파일입니다. | `INTEGRATION` |
| [!UICONTROL Integrations API Configuration] | 통합 API 구성 파일입니다. | `INTEGRATION_API_CONFIG` |
| [!UICONTROL Page Cache] | 전체 페이지 캐싱. | `FPC` |
| [!UICONTROL Translations] | 번역 파일. | `TRANSLATE` |
| [!UICONTROL Web Services Configuration] | REST 및 SOAP 구성, WSDL 파일 생성. | `WEBSERVICE` |
| [!UICONTROL Target Rule] | 대상 규칙 색인 | `TARGET_RULE` |

{style="table-layout:auto"}

## 전체 페이지 캐싱

Adobe Commerce 및 Magento Open Source은 서버에서 전체 페이지 캐싱을 사용하여 범주, 제품 및 CMS 페이지를 신속하게 표시합니다. 전체 페이지 캐싱은 응답 시간을 향상시키고 서버의 로드를 줄입니다. 캐싱을 사용하지 않으면 각 페이지에서 코드 블록을 실행하고 데이터베이스에서 정보를 검색해야 할 수 있습니다. 그러나 전체 페이지 캐싱이 활성화되면 캐시에서 직접 완전히 생성된 페이지를 읽을 수 있습니다.

>[!NOTE]
>
>다음을 권장합니다. [바니시 캐시](https://varnish-cache.org/){:target=&quot;_blank&quot;}는 프로덕션 환경에서만 사용할 수 있습니다.

캐시된 콘텐츠를 사용하여 유사한 유형의 방문에서 요청을 처리할 수 있습니다. 따라서 일반 방문자에게 표시되는 페이지는 고객에게 표시되는 페이지와 다를 수 있습니다. 캐싱을 위해 각 방문은 다음 세 가지 유형 중 하나입니다.

- `Non-sessioned` - 비방문 기간 동안 쇼핑객은 페이지를 보지만 스토어와 상호 작용하지 않습니다. 시스템은 본 각 페이지의 콘텐츠를 캐시하고 다른 비세션 쇼핑객에게 제공합니다.
- `Sessioned` - 세션 방문 중에 제품 비교나 장바구니에 제품 추가와 같은 활동을 통해 스토어와 상호 작용하는 쇼핑객에게는 세션 ID가 지정됩니다. 세션 중에 생성된 캐시된 페이지는 세션 중에 해당 쇼핑객만 사용됩니다.
- `Customer` - 계정에 로그인한 상태에서 스토어 및 쇼핑에 계정을 등록한 사용자를 위해 고객 세션이 생성됩니다. 세션 중에 고객에게 할당된 고객 그룹을 기반으로 하는 특별 오퍼, 프로모션 및 가격을 제공할 수 있습니다.

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

1. Vanish를 사용하는 경우 다음을 완료합니다. **[!UICONTROL Varnish Configuration]** 다음과 같은 섹션:

   - **[!UICONTROL Access list]** - Varnish 구성을 제거하여 구성 파일을 생성할 수 있는 IP 주소를 입력합니다. 여러 항목은 쉼표로 구분하십시오. 기본값은 입니다. `localhost`.

   - **[!UICONTROL Backend host]** - 구성 파일을 생성하는 백엔드 호스트의 IP 주소를 입력합니다. 기본값은 입니다. `localhost`.

   - **[!UICONTROL Backend port]** - 구성 파일을 생성하는 데 사용되는 백엔드 포트를 식별합니다. 기본값은 다음과 같습니다. `8080`.

   - **[!UICONTROL Grace period]** - 구성 파일을 생성하기 위한 유예 기간으로 사용할 시간(초)을 지정합니다. 다음을 참조하십시오 [고급 바니시 구성](https://experienceleague.adobe.com/docs/commerce-operations/configuration-guide/cache/config-varnish-advanced.html) 다음에서 _구성 안내서_.

   - 구성을 로 내보내려면 `varnish.vcl` 파일에서 사용하는 바니시 버전 버튼을 클릭합니다.

   ![고급 구성 - 전체 페이지 캐시 바니시](../configuration-reference/advanced/assets/system-full-page-cache-varnish.png){width="600" zoomable="yes"}

1. 완료되면 다음을 클릭하십시오. **[!UICONTROL Save Config]**.
