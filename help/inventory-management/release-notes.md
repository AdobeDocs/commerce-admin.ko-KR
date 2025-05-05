---
title: '[!DNL Inventory Management] 릴리스 정보'
description: 모든 [!DNL Inventory Management] 릴리스에 대한 정보는 릴리스 정보를 검토하십시오.
exl-id: 856b9503-7621-4beb-ac2f-3eb1a240cebc
feature: Inventory, Release Notes
source-git-commit: fdc14758788fa5cd0391371ebfafb478dadec8a4
workflow-type: tm+mt
source-wordcount: '3462'
ht-degree: 0%

---

# [!DNL Inventory Management] 릴리스 정보

이 릴리스 노트는 [!DNL Inventory Management]의 릴리스에 대해 설명하고 다음을 포함합니다.

새 기능 ![개](../assets/new.svg)개
![해결된 문제](../assets/fix.svg) 수정 사항 및 개선 사항
![알려진 문제](../assets/bug.svg)알려진 문제

[!DNL Inventory Management]은(는) 기여자에게 열려 있는 Magento Open Source Community Engineering 특별 프로젝트입니다. 참여하여 참여하려면 [GitHub 프로젝트](https://github.com/magento/inventory) 저장소 및 [Wiki](https://github.com/magento/inventory/wiki)를 참조하여 시작하십시오. 프로젝트에 대해 논의하려면 [Slack](https://magentocommeng.slack.com/?redir=%2Farchives%2FC5FU5E2HY) 채널([자체 등록](https://opensource.magento.com/slack))에 참여하십시오.

지원되는 릴리스와 호환되는 릴리스의 [릴리스 일정](https://experienceleague.adobe.com/docs/commerce-operations/release/planning/schedule.html?lang=ko){target="_blank"}.

## v1.2.7

[!DNL Inventory Management] 1.2.7 릴리스 노트는 [코어 2.4.7 릴리스 노트](https://experienceleague.adobe.com/ko/docs/commerce-operations/release/notes/adobe-commerce/2-4-7#inventory-management-1)에 포함되어 있습니다.

## v1.2.6

[!DNL Inventory Management] 1.2.6(모듈 버전: `magento/inventory-metapackage = 1.2.6`)은 버전 2.4.6에서 지원되며 Adobe Commerce 버전 2.4.0, 클라우드 인프라의 Adobe Commerce 및 Magento Open Source 코드 베이스와 호환됩니다.

![해결된 문제](../assets/fix.svg) 이제 매진 상태의 하위 제품이 재고로 반환되면 상점 앞에 복합 제품(구성 가능, 번들 및 그룹화)이 재고로 표시됩니다. 앞서 상점가에서는 이 같은 조건에서 해당 복합제품의 재고가 부족하다는 의견을 냈다. <!-- ACP2E-1106-->

![해결된 문제](../assets/fix.svg) 수량을 0으로 설정하고 **[!UICONTROL Display out-of-stock products]**&#x200B;을(를) 사용하도록 설정한 경우 구성 가능한 제품 옵션이 상점 앞에 재고가 없는 것으로 표시됩니다. <!-- ACP2E-1148-->

재고 수량이 변경되고 제품이 아직 재고가 있는 경우 ![해결된 문제](../assets/fix.svg) 범주 페이지 캐시가 더 이상 무효화되지 않습니다. 이제 Adobe Commerce은 storefront 카테고리 페이지의 제품 수량(및 기타 사항)이 변경되면 캐시에서 페이지를 다시 생성하는 대신 로드합니다. <!-- ACP2E-118-->

![해결된 문제](../assets/fix.svg) **[!UICONTROL Display Out-Of-Stock Products]** 설정이 활성화된 단일 소스 모드에서 인벤토리를 사용할 때 범주 목록 제품 수가 올바르게 됩니다. 이제 Adobe Commerce은 계산할 때 제품이 판매가능한지 여부를 확인합니다. <!-- ACP2E-1033-->

인벤토리가 활성화된 경우 ![해결된 문제](../assets/fix.svg) 매장 내 배달에 대한 장바구니 가격 규칙이 예상대로 작동합니다. 이전에는 이러한 조건에서 장바구니 가격 규칙이 생성한 할인이 적용되지 않았습니다. <!-- ACP2E-1015-->

![해결된 문제](../assets/fix.svg) 예약된 모드에서 제품 인벤토리를 업데이트하면 더 이상 모든 캐시가 지워지지 않습니다. 이전에는 인벤토리 인덱서가 모든 구성 캐시를 지웠습니다. <!-- ACP2E-1003-->

![문제가 해결되었습니다](../assets/fix.svg) 이제 Advanced Inventory의 제품에 대한 **[!UICONTROL Allow Multiple Boxes for Shipping]** 특성 값이 예상대로 저장됩니다. <!-- ACP2E-992-->

![해결된 문제](../assets/fix.svg) 이제 Adobe Commerce에서 매장 내 픽업이 적용된 주문에 대한 부분 환불 대변 메모 후에 정확한 예약 보상을 발행합니다. 이전에는 관리자가 **[!UICONTROL Return to Stock]** 확인란을 선택하지 않고 대변 메모를 만들 때 잘못된 예약이 `inventory_reservation` 테이블에 저장되었습니다. <!-- ACP2E-979-->

![해결된 문제](../assets/fix.svg) 다중 소스 인벤토리를 구현하는 배포에서 변형 중 하나가 수동으로 재고로 반환되면 Adobe Commerce은 더 이상 구성 가능한 제품을 재고가 없는 것으로 상점 앞에 표시하지 않습니다. <!-- ACP2E-952-->

![해결된 문제](../assets/fix.svg) 제품 표에서 열 위치(**[!UICONTROL Catalog]** > **[!UICONTROL Products]**)가 여러 인벤토리 원본이 구성된 배포에서 페이지를 다시 로드한 후 더 이상 이전 위치로 되돌아가지 않습니다. <!-- ACP2E-925-->

![고정 문제](../assets/fix.svg) **[!UICONTROL Back to stock]** 확인란을 선택하지 않은 경우 가상 제품에 대한 대변 메모가 발행된 후 현재 재고 수량이 올바릅니다. <!-- ACP2E-908-->

![해결된 문제](../assets/fix.svg) 이제 자동 제품 정렬과 기본값이 아닌 재고에 할당된 범위를 사용하여 범주를 저장할 수 있습니다. 이전에는 Adobe Commerce에서 범주를 저장하지 않고 다음 오류를 표시했습니다. `Something went wrong while saving the category`. <!-- ACP2E-859-->

![해결된 문제](../assets/fix.svg) 이제 모든 재고 부족 구성 가능한 변형을 사용하여 제품을 만들 때 구성 가능한 제품 재고 상태가 예상대로 업데이트됩니다. <!-- ACP2E-813-->

![문제가 해결되었습니다](../assets/fix.svg) 이제 예약 불일치 분석기 도구가 구성 가능, 번들 및 그룹화된 제품이 포함된 부분적으로 배송된 주문에서 올바르게 작동합니다. 이제 복합 제품 유형을 분석합니다. 이전에는 구성 및 함께 제공되는 번들 제품의 하위 제품 주문 항목이 아닌 상위 제품에 대해서만 취소 및 환불이 저장되었습니다. <!-- ACP2E-924-->

![해결된 문제](../assets/fix.svg) 관리자가 재고 또는 제품에 200개 이상의 재고 소스를 할당하려고 할 때 Adobe Commerce에서 더 이상 오류가 표시되지 않습니다. <!-- ACP2E-1180-->

![해결된 문제](../assets/fix.svg) 이제 Adobe Commerce에서 제품이 삭제된 주문에 대한 메모 만들기를 지원합니다. 이전에는 송장이 생성된 후 주문에서 제품이 삭제되면 상인이 대변 메모를 생성할 수 없었습니다. 응용 프로그램에 다음 오류가 표시되었습니다. `Following products with requested skus were not found: s00001`. t. <!-- ACP2E-1138-->

![해결된 문제](../assets/fix.svg) 저장소는 이제 단일 및 여러 저장소 ID를 기준으로 필터링됩니다. 예약된 특성 코드 목록에 `event` 제품 특성 코드를 추가했습니다. 이전에는 재고 부족 보고서에서 재고 모듈이 설치되었을 때 예외를 throw했습니다. <!-- ACP2E-1017-->

![해결된 문제](../assets/fix.svg) 계층화된 탐색 필터가 이제 예상대로 작동하며 품절 제품이 이제 상점 카테고리 제품 목록에 추가됩니다. 새 `is_out_of_stock` 정렬 특성은 Storefront 제품 컬렉션에 Elasticsearch 동적 필드 매퍼를 사용합니다. <!-- ACP2E-748-->

![해결된 문제](../assets/fix.svg) 하위 제품 재고 상태가 REST `POST /rest/V1/inventory/source-items` 호출에 의해 변경되면 복합 제품(번들, 그룹화 및 구성 가능) 재고 상태가 예상대로 업데이트됩니다. <!-- ACP2E-1209-->

## v1.2.5

[!DNL Inventory Management] 1.2.5(모듈 버전: `magento/inventory-metapackage = 1.2.5`)는 버전 2.4.5에서 지원되며 Adobe Commerce 버전 2.4.0, 클라우드 인프라의 Adobe Commerce 및 Magento Open Source 코드 베이스와 호환됩니다.

![해결된 문제](../assets/fix.svg) 이제 판매자가 관리자로부터 선적을 만들 때 번들 및 그룹화된 제품의 기본 재고 재고 상태가 예상대로 업데이트됩니다. 이전에는 배송이 생성된 후에도 이러한 제품의 상태가 변경되지 않았습니다. <!--- ACP2E-418-->

![해결된 문제](../assets/fix.svg) 구성 가능한 제품은 이제 다음 조건 중 하나가 충족되면 재고로 반환됩니다. 1. 상위 제품에 하나 이상의 저장된 하위 항목이 있습니다. 2. 구성 가능한 제품 자체가 업데이트되고 **재고**(으)로 설정되었으며 하나 이상의 하위 항목이 있습니다. <!--- ACP2E-443-->

![해결된 문제](../assets/fix.svg) 이제 REST API를 통해 구현된 인벤토리 변경 사항이 제품 세부 사항 페이지에 예상대로 반영됩니다. 이제 마지막 및 현재 재고 상태를 비교한 후 카탈로그 제품의 캐시가 정리됩니다. 이전에는 콜백 함수를 생략하면 재고 상태 변경 사항이 잘못 평가되어 필요한 캐시 정리가 트리거되지 않았습니다. 그 결과 매장은 재고 변동이 반영되지 않았다. <!--- ACP2E-161-->

![문제 해결](../assets/fix.svg) 기본 재고에 할당되어 이전에 재고가 없던 제품이 이제 원본 항목이 `/V1/inventory/source-items`을(를) 사용하여 업데이트된 후 상점 앞에 표시됩니다. 이전에는 이 REST API 끝점이 잘못된 `stock_status`을(를) 설정했습니다. <!--- ACP2E-562-->

![해결된 문제](../assets/fix.svg) 일괄 작업을 통해 인벤토리 원본 할당을 취소하면(**[!UICONTROL Catalog]** > **[!UICONTROL Products]** > **[!UICONTROL Select Products]** > **[!UICONTROL Actions - Unassign Inventory Source]**) 이제 원본이 선행 0을 제외하고 중복되는 SKU를 포함하는 경우(예: `01234` 및 `1234`) 예상대로 작동합니다. 이전에는 애플리케이션에서 인벤토리 소스에 대한 할당을 취소하지 않고 오류가 발생했습니다. <!--- ACP2E-2641-->

![고정 문제](../assets/fix.svg) 무한 역주문이 활성화되고 역주문 수량에 관계없이 제품이 사용자 지정 재고에 할당되면 제품 재고 상태는 이제 상점에서 항상 **재고**&#x200B;입니다. 기존에는 백오더가 활성화된 상태에서도 상품이 품절됐다. <!--- ACP2E-664-->

![문제가 해결되었습니다](../assets/fix.svg) 구성 가능한 제품 상위 및 하위 제품 재고가 소스 항목이 `POST /V1/inventory/source-items`(으)로 업데이트된 후 올바르게 업데이트됩니다. 하위 제품이 API를 통해 업데이트되면 기본 재고 확인을 위한 새 재고 플러그인이 추가되고 구성 가능한 제품 수량 및 상태가 업데이트됩니다. <!--- ACP2E-442-->

![해결된 문제](../assets/fix.svg) 품절 그룹화된 제품이 더 이상 상점 첫 화면 카테고리 페이지에 나열되지 않습니다. <!--- ACP2E-2082-->

![해결된 문제](../assets/fix.svg)이(가) `CatalogInventory` `composer.json`에서 패키지 이름을 수정했습니다. <!--- ACP2E-2914-->

![해결된 문제](../assets/fix.svg) 다중 소스/재고 배포에서 수량이 0인 제품을 주문한 후 이제 관리자에 잘못된 주문 상태가 올바르게 표시됩니다. [GitHub-33756](https://github.com/magento/magento2/issues/33756) <!--- ACP2E-713-->

![해결된 문제](../assets/fix.svg) 번들 제품이 재고 섹션에서 업데이트될 때 재고 부족 번들 제품이 더 이상 상점 범주 페이지에 표시되지 않습니다. <!--- ACP2E-2012-->

![해결된 문제](../assets/fix.svg) PHP 7.4의 호환성 문제가 해결되었습니다. <!--- AC-3192-->

![해결된 문제](../assets/fix.svg) 많은 옵션(여러 100개)이 포함된 번들 제품을 포함하는 저장 작업의 성능이 향상되었습니다. 이전에는 이러한 대용량 번들 제품을 저장하는 데 몇 분이 소요되었으며, 경우에 따라 인벤토리 서비스가 활성화된 배포에서 시간 초과가 발생하기도 했습니다. [GitHub-34732](https://github.com/magento/magento2/issues/34732) <!--- AC-1901-->

![문제 해결](../assets/fix.svg) 이제 선행 `0`(예: `01234` 및 `1234`)을 제외하고 SKU가 중복되는 경우 여러 제품에 인벤토리 소스를 할당할 때 제품 대량 작업 도구(**[!UICONTROL Select Products]** > **[!UICONTROL Actions]** > **[!UICONTROL Assign Inventory Source]**)가 예상대로 작동합니다. 이전에는 하나의 제품에만 재고 출처가 할당되었습니다. [GitHub-35171](https://github.com/magento/magento2/issues/35171) <!--- AC-2584-->

![문제가 해결되었습니다](../assets/fix.svg) 인벤토리가 0이면 `ProductInterface.only_x_left_in_stock` 필드가 0을 반환합니다. 이전에는 null을 반환했습니다. [GitHub-29932](https://github.com/magento/magento2/issues/29932) <!--- AC-1806-->

![문제가 해결되었습니다](../assets/fix.svg) 이제 관리자 **[!UICONTROL Stores]** > **[!UICONTROL Inventory]** > **[!UICONTROL Stocks]**&#x200B;에서 기본 재고를 편집할 수 있습니다. 이전에는 웹 사이트를 기본 스톡에 할당할 수 있었지만 기본 스톡에서 소스를 추가하거나 제거하려고 하면 콘솔에 JavaScript 오류가 표시되었습니다. <!--- ACP2E-545-->

![해결된 문제](../assets/fix.svg) <!--- ACP2E-274--> **[!UICONTROL Display Out-Of-Stock Products]** 설정이 활성화된 인벤토리 단일 소스 모드를 사용하는 경우 범주 목록 제품 수가 올바르게 됩니다. 이제 새 플러그인은 `AreProductsSalableInterface` 및 `StockConfigurationInterface`을(를) 사용하여 총 제품 수를 결정합니다. 이전에는 범주 제품 목록에서 잘못된 제품 수량을 반환했습니다.

![해결된 문제](../assets/fix.svg) <!--- ACP2E-322--> 구성 가능한 제품은 이제 **[!UICONTROL Move out of stock to the bottom]** 설정을 사용할 때 재고가 업데이트된 후 제품 목록의 마지막 위치로 이동됩니다. 관리자가 활성화된 정렬 순서를 무시하는 Elasticsearch 인덱스 정렬 순서를 무효화하기 위해 새 사용자 지정 데이터베이스 쿼리가 구현됩니다. 이전에는 이 설정을 활성화할 때 구성 가능한 제품 및 해당 하위 제품이 목록의 맨 아래로 이동되지 않았습니다.

## v1.2.4

Inventory management 1.2.4(모듈 버전: `magento/inventory-metapackage = 1.2.4`)는 버전 2.4.4에서 지원되며 Adobe Commerce 버전 2.4.0, Adobe Commerce on cloud infrastructure 및 Magento Open Source 코드 베이스와 호환됩니다.

![해결된 문제](../assets/fix.svg) 이제 Commerce에 관리 제품 목록 보기의 모든 제품에 대한 정확한 판매 가능 수량 값이 표시됩니다. 이전에는 특수 문자가 포함된 SKU가 있는 재고 제품의 판매 가능 수량에 대해 빈 값이 표시되었습니다. <!--- MC-41936-->

![해결된 문제](../assets/fix.svg) 많은(약 10,000개) 인벤토리 소스를 사용하는 배포에서 장바구니에 제품을 추가하는 것과 같은 장바구니 및 체크아웃 작업에 대한 성능이 향상되었습니다. <!--- MC-42570-->

![문제가 해결되었습니다](../assets/fix.svg) [!BADGE PaaS만 해당]{type=Informative url="https://experienceleague.adobe.com/ko/docs/commerce/user-guides/product-solutions" tooltip="Adobe Commerce 온 클라우드 프로젝트(Adobe 관리 PaaS 인프라) 및 온프레미스 프로젝트에만 적용됩니다."} 이제 `bin/magento inventory:reservation:list-inconsistencies` 명령은 데이터베이스에서 예약이 누락되고 캐시가 지워진 경우에도 부분 선적이 있는 주문을 올바르게 처리합니다. 이전에는 미리 지운 캐시로 이 명령을 실행했을 때 Commerce에 다음 오류가 표시되었습니다. `Area code is not set`. <!--- MC-42142-->


![해결된 문제](../assets/fix.svg) 그룹화된 제품 하위 제품의 증분 인덱싱으로 인해 하위 항목이 공유될 때 다른 그룹화된 제품이 더 이상 잘못 인덱싱되지 않습니다. <!--- MC-41963-->

![문제 해결](../assets/fix.svg) 이제 API로 범주에서 제품을 제거한 후 상점 범주 페이지에 올바른 제품 수가 표시됩니다. 이전에는 리인덱싱이 발생할 때까지 카테고리 페이지 제품 수가 올바르지 않았습니다. <!--- MC-42287-->

![해결된 문제](../assets/fix.svg) **[!UICONTROL Manage Stock]** 옵션이 비활성화되어 있는 경우 신용 메모를 만들 때 구성 가능한 제품을 재고로 반품할 수 있습니다. 이전에는 이 옵션을 사용하지 않도록 설정한 경우 Commerce에서 대변 메모 만들기 페이지에 **주식으로 돌아가기** 확인란을 표시하지 않았습니다. <!--- MC-42002-->

![해결된 문제](../assets/fix.svg) 10,000개 항목을 초과하는 재고 관리가 개선되었습니다. 이전에는 성능 문제로 인해 판매자가 웹 사이트를 시작하기 전에 관리자에서 재고를 편집할 수 없었던 경우가 있었습니다. <!--- MC-42643-->

![문제 해결](../assets/fix.svg) 관리자의 **[!UICONTROL User Roles]** 페이지가 업데이트되어 관리자에게 배달 메서드 구성에 대한 제한된 권한을 제공합니다. _배송 방법_ 섹션의 이름이 _[!UICONTROL Delivery methods]_(으)로 변경되었으며&#x200B;_[!UICONTROL In-Store Pickup]_&#x200B;이(가) _[!UICONTROL Delivery methods]_&#x200B;섹션 아래로 이동되었습니다. [GitHub-30053](https://github.com/magento/magento2/issues/30053) <!--- MC-41545-->

![해결된 문제](../assets/fix.svg) API에 의해 대변 메모가 업데이트된 후 Adobe Commerce에서 더 이상 중복 제품 예약을 만들지 않습니다. <!--- MC-41757-->

![해결된 문제](../assets/fix.svg) 체크아웃 워크플로에서 _[!UICONTROL Pick up in Store]_&#x200B;탭에서&#x200B;_[!UICONTROL Shipping]_ 탭으로 전환하면 매장 내 픽업 배달만 사용할 수 있는 경우 더 이상 JavaScript 오류가 트리거되지 않습니다. <!--- MC-42808-->

![해결된 문제](../assets/fix.svg) 판매 가능한 제품 수량과 재고 있는 제품 수량이 올바르게 동기화되었습니다. 이전에는 취소된 주문에 대해 재고 예약 보상이 다시 생성되지 않았습니다. <!--- MC-42485-->

![문제가 해결되었습니다](../assets/fix.svg) 유효성 검사기의 성능은 배송 유형이 `Ship Together`인 번들 제품의 하위 제품에 새 원본을 추가하지 않도록 최적화되어 있습니다. <!--- MC-43039-->

## 1.2.3

[!DNL Inventory Management] 1.2.3(모듈 버전: `magento/inventory-metapackage = 1.2.3`)은 버전 2.4.3에서 지원되며 Adobe Commerce 버전 2.4.0, 클라우드 인프라의 Adobe Commerce 및 Magento Open Source 코드 베이스와 호환됩니다.

![문제 해결](../assets/fix.svg) 프론트엔드의 복합 제품 가시성과 관련된 몇 가지 문제를 해결했습니다.

![해결된 문제](../assets/fix.svg) 최소 필요 수량으로 장바구니 페이지 관리 성능이 향상되었습니다.

![해결된 문제](../assets/fix.svg) 원본 만들기, 재고 부족 항목, 재고 소싱, 할당된 원본 정렬, 매장 게재 및 인벤토리 명령에 대한 문제를 해결하기 위한 몇 가지 수정 사항이 있습니다.

![해결된 문제](../assets/fix.svg) [!DNL Commerce]은(는) 이제 매장 배달을 위해 3자리 캐나다 우편 번호를 지원합니다. `geonames.org`에서 설정한 제한으로 인해 6자리 코드가 지원되지 않습니다.

![해결된 문제](../assets/fix.svg) 이제 관리자는 **제품** 그리드 및 다중 스토어 배포에 대한 **제품 편집** 페이지에 비활성화된 제품에 대한 올바른 기본 재고 수량을 표시합니다.

![해결된 문제](../assets/fix.svg) [!DNL Commerce]은(는) 이제 번들 제품이 재입고될 때 범주 제품 캐시를 새로 고칩니다.

## 1.2.2

[!DNL Inventory Management] 1.2.2(모듈 버전: `magento/inventory-metapackage = 1.2.2`)는 버전 2.4.2에서 지원되며 Adobe Commerce 버전 2.4.0, 클라우드 인프라의 Adobe Commerce 및 Magento Open Source 코드 베이스와 호환됩니다.

![문제 해결](../assets/fix.svg) 프론트엔드의 복합 제품 가시성과 관련된 몇 가지 문제를 해결했습니다.

![해결된 문제](../assets/fix.svg) B2B에서 수량을 업데이트하는 동안 장바구니 페이지 성능이 향상되었습니다.

![해결된 문제](../assets/fix.svg) 매장 내 픽업, 대량 업데이트 및 인벤토리 임계값과 관련된 문제를 해결하기 위한 몇 가지 수정 사항이 있습니다.

![새로 만들기](../assets/new.svg) **기능 테스트.** 새로운 기능 테스트를 도입하고 기존 테스트를 보다 안정적으로 만들기 위한 수정 사항을 제공했습니다.

## 1.2.1

[!DNL Inventory Management] 1.2.1(모듈 버전: `magento/inventory-metapackage = 1.2.1`)은 버전 2.4.1에서 지원되며 Adobe Commerce 버전 2.4.0, 클라우드 인프라의 Adobe Commerce 및 Magento Open Source 코드 베이스와 호환됩니다.

![문제 해결](../assets/fix.svg) `inventory_cleanup_reservations` cron 작업과 관련된 알려진 문제를 해결하고 번들 제품의 매장 픽업 기능과 관련된 문제를 해결했습니다. 이 업데이트에는 스톡 계산, 번들 제품 지원 및 미납주문 기능에 대한 일반적인 개선 사항도 포함됩니다.

![새로 만들기](../assets/new.svg) **기능 테스트.** 매장 내 픽업 기능에 대한 추가 기능을 제공하기 위해 새로운 기능 테스트를 도입했습니다.

## 1.2.0

[!DNL Inventory Management] 1.2.0(모듈 버전: `magento/inventory-metapackage = 1.2.0`)은 Adobe Commerce 버전 2.4.0, 클라우드 인프라의 Adobe Commerce 및 Magento Open Source 코드 베이스에서 지원됩니다.

![해결된 문제](../assets/fix.svg) 원본 할당, 확장 가능한 환경 기능 지원, PHP 7.4, MySQL 8 및 PHPUNIT 9와의 호환성 문제를 해결하기 위한 여러 가지 수정 사항이 있습니다.

![새로 만들기](../assets/new.svg) **매장 내 게재 방법.** 사용자가 체크아웃 중에 픽업 위치로 사용할 원본을 선택할 수 있는 옵션을 추가했습니다. _판매 및 구매 경험 안내서_&#x200B;에서 [매장 내 배달](../stores-purchase/shipping-in-store-delivery.md)을 참조하세요.

![새로 만들기](../assets/new.svg) **다중 소스 모드에 대한 번들 제품 지원.** 인벤토리는 여러 원본이 있는 모든 제품 형식을 지원합니다.

![새로 만들기](../assets/new.svg) **비동기 재고 리인덱싱입니다.**&#x200B;에 비동기적으로 재인덱싱하는 기능이 추가되어 여러 중요한 시나리오의 성능이 향상되었습니다.

![새](../assets/new.svg) **대량 인터페이스.** 판매 가능성 검사를 위한 새 대량 인터페이스를 도입했습니다. `\Magento\InventorySalesApi\Api\AreProductsSalableInterface`, `\Magento\InventorySalesApi\Api\AreProductsSalableForRequestedQtyInterface`.

![새로 만들기](../assets/new.svg) **테스트 범위가 늘어났습니다.** 새 기능은 검색된 문제 및 해결된 문제에 대한 확장 적용 범위를 포함하여 자동화된 테스트로 다룹니다.

![알려진 문제](../assets/bug.svg) **알려진 문제.** 예약 메타데이터에 `object_id` 필드가 없어 `inventory_cleanup_reservations` cron 작업이 제대로 작동하지 않습니다. 이 문제는 [magento/inventory#3046](https://github.com/magento/inventory/pull/3046)에 도입되었습니다.

**해결 방법:** 다음 MySQL 쿼리를 실행하여 예약을 수동으로 정리합니다.

```sql
SELECT GROUP_CONCAT(reservation_id) FROM inventory_reservation GROUP BY stock_id, sku HAVING SUM(quantity) = 0;
DELETE FROM inventory_reservation where reservation_id IN (result_of_the_first_query);
```

## 1.1.6

[!DNL Inventory Management] 1.1.6(모듈 버전: `inventory-composer-metapackage = 1.1.6`)은 버전 2.3.6에서 지원되며 Adobe Commerce의 버전 2.3.5, 2.3.4, 2.3.3, 2.3.2, 2.3.1 및 2.3.0, 클라우드 인프라의 Adobe Commerce 및 Magento Open Source 코드 베이스와 호환됩니다.

![문제 해결](../assets/fix.svg) 미납 주문, 대변 메모, 재고 보고서 그리드 부족, &quot;불일치 해결&quot; CLI 도구에 연결된 수정 사항 및 일반 개선 사항과 관련된 문제를 해결하기 위한 수정 사항입니다.

![새로 만들기](../assets/new.svg) **비동기 재고 리인덱싱입니다.**&#x200B;에 비동기적으로 재인덱싱하는 기능이 추가되어 여러 중요한 시나리오의 성능이 향상되었습니다.

## 1.1.5

[!DNL Inventory Management] 1.1.5(모듈 버전: `inventory-composer-metapackage = 1.1.5`)는 버전 2.3.5에서 지원되며 Adobe Commerce의 버전 2.3.4, 2.3.3, 2.3.2, 2.3.1 및 2.3.0과 호환되고, 클라우드 인프라의 Adobe Commerce 및 Magento Open Source 코드 베이스와 호환됩니다.

![새로 만들기](../assets/new.svg) **제품 SKU가 변경되면 인벤토리를 업데이트합니다.** 새 동작: &quot;카탈로그와 동기화&quot;로 전환하기 위해 새 구성 설정을 도입했습니다.

![새로 만들기](../assets/new.svg) **기능 테스트.** 테스트 검사 간격을 없애기 위해 새로운 기능 테스트를 도입했습니다. 몇 가지 문제를 해결하여 테스트를 보다 안정적이고 신뢰할 수 있도록 했습니다.)

![알려진 문제](../assets/bug.svg) 제품 오버셀링을 방지하기 위한 수정 사항, 상점의 &quot;재고 부족&quot; 제품 가시성, 확장 가능한 환경 지원 및 사용자 인터페이스 개선을 위한 다양한 수정 사항.

## 1.1.4

[!DNL Inventory Management] 1.1.4(모듈 버전: `inventory-composer-metapackage = 1.1.4`)는 버전 2.3.4에서 지원되며 Adobe Commerce의 버전 2.3.3, 2.3.2, 2.3.1 및 2.3.0과 호환되고, 클라우드 인프라의 Adobe Commerce 및 Magento Open Source 코드 베이스와 호환됩니다.

![해결된 문제&#x200B;](../assets/fix.svg)**향상된 성능.** 메모리 사용을 줄이고 응답 없이 프로세스가 중단되는 경우를 방지하기 위해 Inventory Reservations CLI 명령에 번칭 논리를 도입했습니다.

![새로 만들기&#x200B;](../assets/new.svg)**향상된 테스트 범위.**&#x200B;에서 새로운 기능 테스트를 많이 도입했습니다. 거의 모든 수동 인벤토리 시나리오는 자동화된 테스트로 다룹니다.

![알려진 문제](../assets/bug.svg) 대변 메모, 그룹화된 제품, 원본 및 재고 대량 작업 관련 문제를 해결하기 위한 다양한 수정 사항이 있습니다.

## 1.1.3

[!DNL Inventory Management] 1.1.3(모듈 버전: `inventory-composer-metapackage = 1.1.3`)은 버전 2.3.3에서 지원되며 Adobe Commerce의 버전 2.3.2, 2.3.1, 2.3.0, 클라우드 인프라의 Adobe Commerce 및 Magento Open Source 코드 베이스와 호환됩니다.

![해결된 문제&#x200B;](../assets/fix.svg)**Adobe Commerce 및 B2B 기능과의 통합 개선.** [!DNL Inventory Management]이(가) 기본이 아닌 인벤토리 원본 및 재고를 사용하는 웹 사이트에 대해 다음 기능을 올바르게 작동합니다.

- SKU별 주문(Adobe Commerce)
- 빠른 주문(B2B)
- 구매요청 목록(B2B)

![새로 만들기&#x200B;](../assets/new.svg)**향상된 성능.** 기본 재고 및 원본을 실행하는 웹 사이트에 대해 상점 카탈로그 검색 성능이 향상되었습니다.

![새로 만들기&#x200B;](../assets/new.svg)**향상된 테스트 범위.** 자동화된 기능 및 통합 테스트 범위가 크게 증가했습니다.

## 1.1.2

[!DNL Inventory Management] 1.1.2(모듈 버전: `inventory-composer-metapackage = 1.1.2`)는 버전 2.3.2에서 지원되며 Adobe Commerce 버전 2.3.1 및 2.3.0과 호환되고, 클라우드 인프라의 Adobe Commerce 및 Magento Open Source 코드 베이스와 호환됩니다.

![해결된 문제](../assets/fix.svg) GET `/V1/shipments` REST 끝점에 대한 응답에 `source_code`을(를) 추가했습니다. <!-- https://github.com/magento/inventory/pull/2142 -->

![문제가 해결되었습니다](../assets/fix.svg) 배송되지 않은 주문에 대해 대변 메모를 발행한 후 예약을 올바르게 지우고 제품 수량을 업데이트하기 위해 문제가 해결되었습니다. <!-- https://github.com/magento/inventory/pull/2179 -->에 대한 옵션을 선택하는 경우

![해결된 문제](../assets/fix.svg) 제품을 만드는 동안 수량을 입력할 때 구성 가능한 하위 제품에 대한 수량을 올바르게 저장하는 해결된 문제. <!-- https://github.com/magento/inventory/pull/2158 -->

[!DNL Inventory Management] 1.1.2 Beta에 대한 새 모듈은 다음과 같습니다.

```php
        'Magento_InventoryGraphQl' => 1,
        'Magento_InventoryReservations' => 1,
        'Magento_InventoryReservationsApi' => 1,
        'Magento_InventoryReservationCli' => 1,
        'Magento_InventoryExportStock' => 0,
        'Magento_InventoryExportStockApi' => 0,
```

![새로 만들기](../assets/new.svg) **대량 부분 스톡 전송 끝점을 추가했습니다** - 현재 대량 전송 끝점은 할당된 모든 수량을 원본에서 대상 원본으로 이동합니다. 새 `/rest/V1/inventory/bulk-partial-source-transfer` 끝점을 사용하면 판매자가 대량 작업으로 부분 주식을 소스에서 소스로 전송할 수 있습니다. 특정 수량을 전송하려면 `sku`, `qty`, `origin_source_code` 및 `destination_source_code`을(를) 사용하여 끝점에 요청을 입력하십시오. 전송: 소스가 `sku`에 할당되었는지, 전송할 충분한 수량이 있는지 확인합니다. REST API 설명서의 [일괄 작업 인벤토리](https://developer.adobe.com/commerce/webapi/rest/inventory/bulk-inventory/){target="_blank"}를 참조하십시오. <!-- https://github.com/magento/inventory/pull/2117 -->

![새로 만들기](../assets/new.svg) **추가된 예약 CLI** - 새 명령을 사용하면 예약 불일치를 감지하고 해결할 수 있습니다. 주문이 제출되고 상태가 변경되면 [!DNL Inventory Management]은(는) 초기 예약을 생성하고 보상 예약을 통해 업데이트합니다. 이러한 명령은 주문 ID, SKU 및 Stock ID별로 발견된 불일치 목록을 반환하고 해결할 예약을 만듭니다. 자세한 내용은 [CLI 참조](cli.md)를 참조하십시오. <!-- https://github.com/magento/inventory/pull/2199 https://github.com/magento/inventory/pull/2184 https://github.com/magento/inventory/pull/2171 https://github.com/magento/inventory/pull/2148  -->

![새로 만들기](../assets/new.svg) **원본 및 SSA 옵션에 대한 성능 개선** - 보내는 동안 원본을 정렬하고 선택하면 원본 수가 많은 주식의 성능이 저하됩니다. 이번 릴리스는 배송에서 SSA 옵션을 검토하고 선택할 때 사용 가능한 소스를 나열하고 정렬하는 데 상당한 성능 향상을 제공합니다. <!-- https://github.com/magento/inventory/pull/2056 https://github.com/magento/inventory/pull/2090 -->

![새로 만들기](../assets/new.svg) **Inventory management에 대한 GraphQL 지원이 추가됨** - 이 릴리스는 새 `magento/module-inventory-graph-ql` 모듈을 설치합니다. 이제 GraphQL [ProductInterface 특성](https://developer.adobe.com/commerce/webapi/graphql/schema/products/interfaces/attributes/){target="_blank"}에 [!DNL Inventory Management] 지원을 위한 `only_x_left_in_stock` 및 `stock_status` 특성이 포함됩니다. <!-- https://github.com/magento/inventory/pull/2124 -->

![새로 만들기](../assets/new.svg) **할당된 소스에 대한 간소화된 UI** - 제품 페이지의 할당된 소스 테이블에는 더 쉬운 업데이트와 많은 소스를 표시할 때 성능 향상을 위해 간소화된 콘텐츠가 있습니다. 소스 이름별 모든 소스 목록(`source_code`에 대해 마우스로 가리키기).

![새로운 기능](../assets/new.svg) **집계된 주식 내보내기 서비스** - 이 릴리스에서는 Amazon, eBay 및 Google 쇼핑 광고와 같은 외부 판매 채널을 지원하기 위해 새로운 집계된 주식 내보내기 서비스(시스템에 예약 유지)를 제공합니다.  <!-- https://github.com/magento/inventory/pull/2067 -->

## 1.1.0

[!DNL Inventory Management] 1.1.0(모듈 버전: `inventory-composer-metapackage = 1.1.0`)이 지원되며 Adobe Commerce 버전 2.3.0, 클라우드 인프라의 Adobe Commerce 및 Magento Open Source 코드 베이스와 호환됩니다. [!DNL Inventory Management] 1.1.1은 패키지 이름 업데이트로만 릴리스되며, 버전 2.3.1에 대해 지원되고, Adobe Commerce 버전 2.3.0, 클라우드 인프라의 Adobe Commerce 및 Magento Open Source 코드 베이스와 호환됩니다.

![문제가 해결되었습니다](../assets/fix.svg) **단일 및 다중 소스 모드에 대한 Elasticsearch 지원이 추가되었습니다** — 이제 사용자 지정 재고로 Elasticsearch을 구성하고 사용할 수 있습니다. 설치 정보는 [Elasticsearch 서비스 설정](https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/configure/service/elasticsearch.html?lang=ko){target="_blank"}을 참조하십시오. <!-- PR https://github.com/magento/inventory/pull/1943 -->

![해결된 문제](../assets/fix.svg) 많은 작업에서 성능을 크게 향상하기 위해 기본 스톡의 성능 문제를 해결했습니다. 개선 사항은 단일 소스 모드, Source으로 재고 이전, 상점 카테고리 페이지 및 판매 수량 계산에 대한 성능을 향상시킵니다.

<!-- All Performance Track issues resolved https://github.com/magento/inventory/issues?q=is%3Aopen+is%3Aissue+label%3APerformance -->

![해결된 문제](../assets/fix.svg) 구성 및 그룹화된 제품에 대해 재고 부족 상태와 대량의 재고로 전송되는 문제가 해결되었습니다. 상위 제품을 선택하고 일괄 작업을 수행해도 제품 상태에 영향을 주지 않습니다. 상위 제품이 재고에 있으면 재고에 남아 있습니다.

<!-- PR https://github.com/magento/inventory/pull/1972 -->

![새로 만들기](../assets/new.svg) **거리 우선 순위 알고리즘** — 거리 우선 순위 알고리즘은 거리 기반 배송 권장 사항에 대한 새로운 기본 제공 Source 선택 알고리즘입니다. 이 알고리즘은 출하 목적지 주소의 위치를 출처 위치와 비교하여 출하를 이행할 가장 가까운 출처를 결정합니다. 거리는 가져온 지오코드 위치 데이터 또는 Google 방향(주행, 보행 또는 자전거)을 사용하여 물리적 거리 또는 한 위치에서 다른 위치로 이동하는 데 걸린 시간에 의해 결정될 수 있습니다.

![새로 만들기](../assets/new.svg) **확장된 원본 수량 목록** — 원본 수가 많은 판매자는 제품 그리드를 통해 제품당 모든 원본을 쉽게 가리키고 볼 수 있습니다. 각 제품에는 최소 5개의 소스와 해당 수량이 표시됩니다. 소스를 마우스로 가리키면 전체 소스 목록과 현재 수량을 스크롤할 수 있습니다.

![알려진 문제](../assets/bug.svg) Magento Open Source 및 Adobe Commerce v2.3.1의 알려진 문제 - PHP 클래스 및 메서드 이름을 반영하는 항목 이름이 있는 비동기 API의 변경으로 인해 소스 간 데이터의 비동기 마이그레이션에 문제가 발생합니다. 동기 작업을 사용하여 **[!UICONTROL Run asynchronously]**&#x200B;을(를) `No`(으)로 설정하는 것이 좋습니다.
