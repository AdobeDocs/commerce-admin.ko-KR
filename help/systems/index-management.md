---
title: 색인 관리
description: 리인덱싱을 트리거하는 작업과 모범 사례를 포함하여 인덱스 관리에 대해 알아봅니다.
exl-id: cbb249a2-b957-44fe-bf81-df795a8fd5d1
feature: System, Configuration
source-git-commit: 55b0672984ce8cdb853daf024299919beaf7ce0b
workflow-type: tm+mt
source-wordcount: '1308'
ht-degree: 0%

---

# 색인 관리

Adobe Commerce 및 Magento Open Source은 하나 이상의 항목이 변경될 때마다 자동으로 다시 인덱싱합니다. 리인덱싱을 트리거하는 작업에는 가격 변경, 카탈로그 또는 장바구니 가격 규칙 만들기, 새 범주 추가 등이 포함됩니다. 성능을 최적화하기 위해 Commerce에서는 인덱서를 사용하여 데이터를 특수 테이블에 누적합니다. 데이터가 변경되면 인덱싱된 테이블을 업데이트하거나 다시 인덱싱해야 합니다. 상업은 백그라운드 프로세스로 다시 인덱싱되며 프로세스 중에는 저장소에 계속 액세스할 수 있습니다.

데이터를 리인덱싱하면 처리 속도가 빨라지고 고객의 대기 시간이 줄어듭니다. 예를 들어 항목의 가격을 $4.99에서 $3.99로 변경하면 Commerce는 데이터를 다시 인덱싱하여 스토어에서 가격 변경을 표시합니다. 색인화가 없으면 Commerce는 장바구니 가격 규칙, 번들 가격, 할인, 계층 가격 등을 처리하는 모든 제품의 가격을 즉시 계산해야 합니다. 제품 가격을 로드하는 데 고객이 기다리는 시간보다 오래 걸릴 수 있습니다.

인덱서는 저장 시 업데이트 또는 예약 시 업데이트로 설정할 수 있습니다. 저장 시만 지원하는 고객 그리드를 제외하고 모든 색인이 두 옵션 중 하나를 사용할 수 있습니다. 저장 시 색인화하면 Commerce는 저장 작업에 대한 색인 재지정을 시작합니다. 색인 관리 페이지는 업데이트를 완료하고 1~2분 내에 색인 재지정 메시지가 나타나도록 캐시를 플러시합니다. 일정에서 리인덱싱하는 경우 일정에 따라 리인덱싱이 cron job으로 실행됩니다. 다음과 같은 경우 시스템 메시지가 나타납니다. [cron job](cron.md) 가 잘못된 인덱서를 업데이트하는 데는 사용할 수 없습니다. 색인 재지정 프로세스 중에는 저장소에 계속 액세스할 수 있습니다.

>[!NOTE]
> Live Search, Catalog Service 또는 Product Recommendations을 사용하는 Adobe Commerce 판매자는 [SaaS 기반 가격 인덱서](https://experienceleague.adobe.com/docs/commerce-merchant-services/price-indexer/index.html).

색인 재지정이 필요한 경우 페이지 상단에 알림이 표시됩니다. 색인 및 메시지는 색인 재지정 모드 및 수행할 수 있는 작업에 따라 지워집니다. 색인화에 대한 자세한 내용은 [애플리케이션이 색인화를 구현하는 방법](https://developer.adobe.com/commerce/php/development/components/indexing/#how-the-application-implements-indexing) 다음에서 _PHP 개발자 안내서_.

![색인 관리 - 작업](./assets/index-management.png){width="700" zoomable="yes"}

- Index Management는 플랫 제품 카탈로그에 대해 약간 다른 프레젠테이션을 제공합니다.
- 여러 관리 사용자가 자동 리인덱싱을 트리거하는 개체를 업데이트할 때 문제가 발생하지 않도록 모든 인덱서가 일정에 따라 실행되도록 설정하는 것이 좋습니다. [cron jobs](cron.md). 그렇지 않으면 개체를 저장할 때마다 상호 종속성이 있는 모든 개체가 교착 상태를 초래할 수 있습니다. 교착 상태의 증상으로는 높은 CPU 사용률과 MySQL 오류가 있습니다. 가장 좋은 방법은 예약된 색인화를 사용하는 것입니다.
- ![Adobe Commerce](../assets/adobe-logo.svg) (Adobe Commerce만 해당) 기본적으로 리인덱싱과 같은 관리자 작업은 시스템에 의해 기록되며 [작업 로그 보고서](action-log-report.md). 작업 로깅은에서 구성할 수 있습니다. [관리자 작업 로깅](action-log.md) 저장소의 고급 관리자 설정에서.

## 리인덱싱 모범 사례

리인덱싱과 캐싱은 Commerce에서 다른 용도로 사용됩니다. 인덱스는 데이터베이스 정보를 추적하여 검색 성능을 높이고, 상점에 대한 데이터 검색 속도를 향상시킵니다. [캐시](cache-management.md) 로드된 데이터, 이미지, 형식 등을 저장하여 storefront의 성능 로드 및 액세스를 향상시킵니다.

- 일반적으로 Commerce에서 데이터를 업데이트할 때 색인을 다시 지정해야 합니다.
- 대형 스토어나 여러 스토어가 있는 경우 색인 재지정의 가능성으로 인해 카테고리 및 제품과 같은 색인을 예약된 크론 작업으로 설정할 수 있습니다. 피크 시간이 아닌 시간 동안 일정에 따라 색인 재지정을 설정할 수 있습니다.
- 리인덱싱하는 경우 플러시 캐시도 수행할 필요가 없습니다.
- 새 상거래 설치의 경우 캐시를 플러시하고 다시 인덱싱해야 합니다.
- 캐시를 플러시하고 리인덱싱하는 경우 컴퓨터의 웹 브라우저 캐시가 플러시되지 않습니다. Storefront에 대한 업데이트를 완료한 후 브라우저 캐시를 지우십시오.

## 색인 모드 변경

>[!IMPORTANT]
>
>를 사용하는 스토어의 경우 [Adobe Commerce용 B2B](https://experienceleague.adobe.com/docs/commerce-admin/b2b/introduction.html) Elasticsearch을 전체 텍스트(`catalogsearch_fulltext`) 인덱서: 일괄 권한을 변경하거나 &#39;permissions&#39; 인덱서가 &#39;Scheduled&#39; 모드에 있는 경우 전체 텍스트 인덱스를 다시 실행해야 합니다.

1. 다음에서 _관리자_ 사이드바, 이동 **[!UICONTROL System]** > _[!UICONTROL Tools]_>**[!UICONTROL Index Management]**.

1. 변경할 각 인덱서의 확인란을 선택합니다.

1. 설정 **[!UICONTROL Actions]** 다음 중 하나를 수행합니다.

   - `Update on Save`
   - `Update by Schedule`
   - `Invalidate index`

   >[!IMPORTANT]
   >
   >고객 그리드는 를 통해서만 다시 인덱싱할 수 있습니다. `Update on Save`. 이 색인은 다음을 수행합니다. **_아님_** 지원 `Update by Schedule`.

1. 클릭 **[!UICONTROL Submit]** 를 눌러 선택한 각 인덱서에 변경 사항을 적용합니다.

   **인덱스 관리 열**

   | 열 | 설명 |
   | ------ | ----------- |
   | [!UICONTROL Indexer] | 인덱서의 이름입니다. |
   | [!UICONTROL Description] | 인덱서에 대한 설명. |
   | [!UICONTROL Mode] | 각 인덱서의 현재 업데이트 모드를 나타냅니다. 옵션: <br/>**[!UICONTROL Update on Save]**- 엔티티가 변경될 때마다 업데이트되도록 인덱스가 설정됩니다. 이러한 엔티티에는 제품, 카테고리 및 고객이 포함됩니다. 저장 작업이 완료되면 변경 사항을 추적하고 인덱스를 업데이트하는 일련의 단계가 시작됩니다. 색인 관리 페이지는 1~2분 내에 색인 재지정 메시지를 업데이트하고 플러시합니다.<br/>**[!UICONTROL Update on Schedule]** - 색인은 다음에 따라 일정에 따라 업데이트되도록 설정됩니다. [cron job](cron.md). cron 작업에는 실행 시 색인에 업데이트를 기록하는 색인 재지정 일정 간격이 포함됩니다. |
   | [!UICONTROL Schedule Status] | 일정 상태 업데이트를 표시합니다. |
   | [!UICONTROL Status] | 다음 중 하나를 표시합니다. <br/>**[!UICONTROL Ready]**— 색인이 최신 버전입니다.<br/>**[!UICONTROL Scheduled]** - 리인덱싱이 예정되어 있습니다. <br/>**[!UICONTROL Running]**- 리인덱싱이 실행 중입니다.<br/>**[!UICONTROL Reindex Required]** - 리인덱싱이 필요하지만 인덱서를 자동으로 업데이트할 수 없도록 변경되었습니다. 다음을 확인하십시오. [cron](cron.md) 을 사용할 수 있으며 올바로 구성하십시오. |
   | [!UICONTROL Updated] | 색인이 마지막으로 업데이트된 날짜와 시간을 나타냅니다. |

   {style="table-layout:auto"}

## 명령줄을 사용하여 색인 재지정

Commerce는 명령줄을 사용하여 추가 색인 재지정 옵션을 제공합니다. 자세한 내용 및 명령 옵션은 다음을 참조하십시오. [색인 재지정](https://experienceleague.adobe.com/docs/commerce-operations/configuration-guide/cli/manage-indexers.html#reindex)의 {:target=&quot;blank&quot;} _구성 안내서_.

## 인덱스 트리거 이벤트

## 트리거 리인덱싱

| 색인 유형 | 리인덱싱 이벤트 |
| ---------- | ---------------- |
| [!UICONTROL Product Prices] | 고객 그룹 추가<br/>구성 설정 변경 |
| [!UICONTROL Flat catalog product data] | 저장소 추가<br/>저장소 그룹 추가<br/>속성 추가, 편집 또는 삭제(검색 및 필터링용) |
| [!UICONTROL Flat catalog category data] | 저장소 추가<br/>저장소 그룹 추가<br/>속성 추가, 편집 또는 삭제(검색 및 필터링용) |
| [!UICONTROL Catalog category/product index] | 제품 추가, 편집 또는 삭제(단일, 일괄 및 가져오기)<br/>제품-카테고리 관계 변경<br/>범주 추가, 편집 또는 삭제<br/>저장소 추가 또는 삭제<br/>저장소 그룹 삭제<br/>웹 사이트 삭제 |
| [!UICONTROL Catalog search index] | 제품 추가, 편집 또는 삭제(단일, 일괄 및 가져오기)<br/>저장소 추가 또는 삭제<br/>저장소 그룹 삭제<br/>웹 사이트 삭제 |
| [!UICONTROL Stock status index] | 인벤토리 구성 설정을 변경합니다. |
| [!UICONTROL Category permissions index] | 저장소 추가<br/>저장소 그룹 추가<br/>속성 추가, 삭제 또는 업데이트(검색 및 필터링용) |

{style="table-layout:auto"}

>[!IMPORTANT]
>
>플랫 카탈로그를 사용하는 것은 더 이상 우수 사례로 권장되지 않습니다. 이 기능을 계속 사용하면 성능 저하 및 기타 인덱싱 문제가 발생하는 것으로 알려져 있습니다. 다음을 참조하십시오 [플랫 카탈로그 제품 사용](../catalog/catalog-flat.md) 추가 정보.

## 색인 작업 및 컨트롤

| 작업 | 결과 | 컨트롤 |
| ------ | ------ | -------- |
| 스토어, 새 고객 그룹 또는 나열된 작업 만들기 `Actions that Cause a Full Reindex` | 전체 색인 재지정 | 전체 리인덱싱은 Adobe Commerce 또는 Magento Open Source cron 작업에 의해 결정된 일정에 따라 수행됩니다. |
| 항목 대량 로드(상거래 가져오기/내보내기, 직접 SQL 쿼리 및 데이터를 직접 추가, 변경 또는 삭제하는 기타 방법) | 부분 색인 재지정(변경된 항목만 색인 재지정) | 상거래 cron 작업에 의해 결정된 빈도입니다. |
| 범위 변경(예: 글로벌에서 웹 사이트로) | 부분 색인 재지정(변경된 항목만 색인 재지정) | 상거래 cron 작업에 의해 결정된 빈도입니다. |

{style="table-layout:auto"}

## 전체 리인덱싱을 트리거하는 이벤트

| 인덱서 | Event |
| ------- | ----- |
| [!UICONTROL Catalog Category Flat Indexer] | 웹 스토어 만들기<br/>웹 스토어 보기 만들기<br/>다음 중 하나의 속성을 만들거나 삭제합니다.<br/>- 고급 검색에서 검색 또는 표시<br/>- 필터링 가능<br/>- 검색 시 필터링 가능<br/>- 정렬에 사용됨<br/>기존 속성을 이전 속성 중 하나로 변경합니다.<br/>플랫 카테고리 상점 옵션 활성화 |
| [!UICONTROL Catalog Product Flat Indexer] | 웹 스토어 만들기<br>웹 스토어 보기 만들기<br/>다음 중 하나의 속성을 만들거나 삭제합니다.<br/>- 고급 검색에서 검색 또는 표시<br>- 필터링 가능<br>- 검색 시 필터링 가능<br/>- 정렬에 사용됨 <br/>기존 속성을 이전 속성 중 하나로 변경합니다.<br/>플랫 카테고리 상점 옵션 활성화 |
| [!UICONTROL Stock status indexer] | 다음과 같은 경우 _카탈로그 인벤토리 옵션_ 시스템 구성 변경:<br/>`Stock Options` - 품절 제품 표시<br/>`Product Stock Options` - 재고 관리 |
| [!UICONTROL Price Indexer] | 고객 그룹 추가<br/>시스템 구성에서 다음 카탈로그 재고 옵션이 변경되는 경우:<br/>`Stock Options` - 품절 제품 표시<br/>`Product Stock Options` - 재고 관리<br/>`Price` - 카탈로그 가격 범위 |
| [!UICONTROL Category or Product Indexer] | 스토어 보기 만들기 또는 삭제<br/>스토어 삭제<br/>웹 사이트 삭제 |

{style="table-layout:auto"}
