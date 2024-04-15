---
title: '''[!DNL Inventory Management] 릴리스 정보'
description: 모든 항목에 대한 자세한 내용은 릴리스 정보 를 참조하십시오 [!DNL Inventory Management] 릴리스.
exl-id: 856b9503-7621-4beb-ac2f-3eb1a240cebc
feature: Inventory, Release Notes
source-git-commit: 01d8a1d50f574330f3ce7e8bf03a018f0079f5db
workflow-type: tm+mt
source-wordcount: '3445'
ht-degree: 0%

---

# [!DNL Inventory Management] 릴리스 정보

이 릴리스 노트는 의 릴리스에 대해 설명합니다. [!DNL Inventory Management] 및 포함:

![신규](../assets/new.svg) 새로운 기능
![해결된 문제](../assets/fix.svg) 수정 사항 및 향상된 기능
![알려진 문제](../assets/bug.svg) 알려진 문제

[!DNL Inventory Management] 는 기여자에게 공개되는 Magento Open Source 커뮤니티 엔지니어링 특별 프로젝트입니다. 참가하고 기여하려면 다음을 참조하십시오. [GitHub 프로젝트](https://github.com/magento/inventory) 저장소 및 [wiki](https://github.com/magento/inventory/wiki) 시작합니다. 프로젝트에 대해 논의하려면 [Slack](https://magentocommeng.slack.com/?redir=%2Farchives%2FC5FU5E2HY) 채널 ([자가 등록](https://opensource.magento.com/slack)).

[릴리스 일정](https://experienceleague.adobe.com/docs/commerce-operations/release/planning/schedule.html){target="_blank"} 지원되는 릴리스 및 호환되는 릴리스에 대해 알아보십시오.

## v1.2.7

[!DNL Inventory Management] 1.2.7 릴리스 노트는 [core 2.4.7 릴리스 노트](https://experienceleague.adobe.com/en/docs/commerce-operations/release/notes/adobe-commerce/2-4-7#inventory-management-1).

## v1.2.6

[!DNL Inventory Management] 1.2.6 (모듈 버전: `magento/inventory-metapackage = 1.2.6`)는 버전 2.4.6에서 지원되며 Adobe Commerce 버전 2.4.0, 클라우드 인프라의 Adobe Commerce 및 Magento Open Source 코드 베이스와 호환됩니다.

![해결된 문제](../assets/fix.svg) 이제 매진 완료된 하위 제품이 재고로 반환되면 상점 앞에 복합 제품(구성 가능, 번들 및 그룹화)이 재고로 표시됩니다. 앞서 상점가에서는 이 같은 조건에서 해당 복합제품의 재고가 부족하다는 의견을 냈다. <!-- ACP2E-1106-->

![해결된 문제](../assets/fix.svg) 수량이 0 및 로 설정된 상태에서 옵션을 만든 경우 구성 가능한 제품 옵션이 이제 상점 첫 화면에서 재고가 없는 것으로 예상되어 표시됩니다. **[!UICONTROL Display out-of-stock products]** 이(가) 활성화되었습니다. <!-- ACP2E-1148-->

![해결된 문제](../assets/fix.svg) 재고 수량이 변경되고 제품이 아직 재고가 있는 경우 카테고리 페이지 캐시는 더 이상 무효화되지 않습니다. 이제 Adobe Commerce은 storefront 카테고리 페이지의 제품 수량(및 기타 사항)이 변경되면 캐시에서 페이지를 다시 생성하는 대신 로드합니다. <!-- ACP2E-118-->

![해결된 문제](../assets/fix.svg) 단일 소스 모드에서 Inventory를 와 함께 사용할 때 카테고리 목록 제품 수가 정확합니다. **[!UICONTROL Display Out-Of-Stock Products]** 설정이 활성화되었습니다. 이제 Adobe Commerce은 계산할 때 제품이 판매가능한지 여부를 확인합니다. <!-- ACP2E-1033-->

![해결된 문제](../assets/fix.svg) 이제 재고가 활성화되면 매장 내 배송에 대한 장바구니 가격 규칙이 예상대로 작동합니다. 이전에는 이러한 조건에서 장바구니 가격 규칙이 생성한 할인이 적용되지 않았습니다. <!-- ACP2E-1015-->

![해결된 문제](../assets/fix.svg) 예약된 모드에서 제품 인벤토리를 업데이트하면 더 이상 모든 캐시가 지워지지 않습니다. 이전에는 인벤토리 인덱서가 모든 구성 캐시를 지웠습니다. <!-- ACP2E-1003-->

![해결된 문제](../assets/fix.svg) 에 대한 값 **[!UICONTROL Allow Multiple Boxes for Shipping]** 이제 Advanced Inventory의 제품에 대한 속성이 예상대로 저장됩니다. <!-- ACP2E-992-->

![해결된 문제](../assets/fix.svg) Adobe Commerce은 매장 내 픽업이 진행된 주문에 대해 부분 환불 대변 메모 후 정확한 예약 보상을 발행한다. 이전에는 잘못된 예약이 `inventory_reservation` 관리 사용자가 다음을 선택하지 않고 대변 메모를 만든 경우 테이블 **[!UICONTROL Return to Stock]** 확인란. <!-- ACP2E-979-->

![해결된 문제](../assets/fix.svg) Adobe Commerce은 다중 소스 인벤토리를 구현하는 배포에서 변형 중 하나가 수동으로 재고로 반환된 경우 더 이상 구성 가능한 제품을 재고가 없는 것으로 상점 앞에 표시하지 않습니다. <!-- ACP2E-952-->

![해결된 문제](../assets/fix.svg) 제품 그리드의 열 위치(**[!UICONTROL Catalog]** > **[!UICONTROL Products]**)는 여러 인벤토리 소스가 구성된 배포에서 페이지를 다시 로드한 후 더 이상 이전 위치로 되돌아가지 않습니다. <!-- ACP2E-925-->

![해결된 문제](../assets/fix.svg) 가상 제품에 대한 대변 메모가 발행된 후 재고 수량이 수정되었습니다. **[!UICONTROL Back to stock]** 확인란이 선택되지 않았습니다. <!-- ACP2E-908-->

![해결된 문제](../assets/fix.svg) 이제 자동 제품 정렬 및 기본값이 아닌 재고에 할당된 범위를 사용하여 범주를 저장할 수 있습니다. 이전에는 Adobe Commerce이 카테고리를 저장하지 않고 이 오류를 표시했습니다. `Something went wrong while saving the category`. <!-- ACP2E-859-->

![해결된 문제](../assets/fix.svg) 구성 가능한 제품 스톡 상태는 이제 모든 재고 부족 구성 가능한 변형으로 제품을 만들 때 예상대로 업데이트됩니다. <!-- ACP2E-813-->

![해결된 문제](../assets/fix.svg) 이제 구성 가능한 제품, 번들 제품 및 그룹화된 제품이 포함된 부분적으로 제공된 주문에서 예약 불일치 분석기 도구가 올바르게 작동합니다. 이제 복합 제품 유형을 분석합니다. 이전에는 구성 및 함께 제공되는 번들 제품의 하위 제품 주문 항목이 아닌 상위 제품에 대해서만 취소 및 환불이 저장되었습니다. <!-- ACP2E-924-->

![해결된 문제](../assets/fix.svg) 관리자가 재고 또는 제품에 200개 이상의 재고 소스를 할당하려고 할 때 Adobe Commerce에 더 이상 오류가 표시되지 않습니다. <!-- ACP2E-1180-->

![해결된 문제](../assets/fix.svg) 이제 Adobe Commerce에서는 제품이 삭제된 주문에 대한 대변 메모 만들기를 지원합니다. 이전에는 송장이 생성된 후 주문에서 제품이 삭제되면 상인이 대변 메모를 생성할 수 없었습니다. 응용 프로그램에 다음 오류가 표시되었습니다. `Following products with requested skus were not found: s00001`. t. <!-- ACP2E-1138-->

![해결된 문제](../assets/fix.svg) 이제 저장소는 단일 및 여러 저장소 ID를 기반으로 필터링됩니다. 다음 `event` 예약된 속성 코드 목록에 제품 속성 코드가 추가되었습니다. 이전에는 재고 부족 보고서에서 재고 모듈이 설치되었을 때 예외를 throw했습니다. <!-- ACP2E-1017-->

![해결된 문제](../assets/fix.svg) 이제 계층화된 탐색 필터가 예상대로 작동하며 품절된 제품이 이제 상점 카테고리 제품 목록에 추가됩니다. 새로운 `is_out_of_stock` 정렬 속성은 storefront 제품 컬렉션에 Elasticsearch 동적 필드 매퍼를 사용합니다. <!-- ACP2E-748-->

![해결된 문제](../assets/fix.svg) 복합 제품(번들, 그룹화 및 구성 가능) 재고 상태는 하위 제품 재고 상태가 REST에 의해 변경될 때 예상대로 업데이트됩니다 `POST /rest/V1/inventory/source-items` 호출합니다. <!-- ACP2E-1209-->

## v1.2.5

[!DNL Inventory Management] 1.2.5 (모듈 버전: `magento/inventory-metapackage = 1.2.5`)는 버전 2.4.5에서 지원되며 Adobe Commerce 버전 2.4.0, 클라우드 인프라의 Adobe Commerce 및 Magento Open Source 코드 베이스와 호환됩니다.

![해결된 문제](../assets/fix.svg) 이제 판매자가 관리자로부터 납품을 생성할 때 번들 및 그룹화된 제품의 기본 재고 재고 상태가 예상대로 업데이트됩니다. 이전에는 배송이 생성된 후에도 이러한 제품의 상태가 변경되지 않았습니다. <!--- ACP2E-418-->

![해결된 문제](../assets/fix.svg) 구성 가능한 제품은 이제 다음 조건 중 하나가 충족되면 재고로 반환됩니다. 1. 상위 제품에 하나 이상의 저장된 하위 항목이 있습니다. 2. 구성 가능한 제품 자체가 업데이트되고 다음으로 설정됨 **재고 있음** 그리고 적어도 한 명의 아이를 낳았습니다. <!--- ACP2E-443-->

![해결된 문제](../assets/fix.svg) 이제 REST API를 통해 구현된 인벤토리 변경 사항이 제품 세부 사항 페이지에 예상대로 반영됩니다. 이제 마지막 및 현재 재고 상태를 비교한 후 카탈로그 제품의 캐시가 정리됩니다. 이전에는 콜백 함수를 생략하면 재고 상태 변경 사항이 잘못 평가되어 필요한 캐시 정리가 트리거되지 않았습니다. 그 결과 매장은 재고 변동이 반영되지 않았다. <!--- ACP2E-161-->

![해결된 문제](../assets/fix.svg) 기본 재고에 할당되고 이전에 재고가 없던 제품은 이제 소스 항목이 를 사용하여 업데이트된 후 상점 맨 앞에 표시됩니다. `/V1/inventory/source-items`. 이전에는 이 REST API 엔드포인트가 잘못 설정되었습니다. `stock_status`. <!--- ACP2E-562-->

![해결된 문제](../assets/fix.svg) 일괄 작업을 통해 재고 출처 지정 취소(**[!UICONTROL Catalog]** > **[!UICONTROL Products]** > **[!UICONTROL Select Products]** > **[!UICONTROL Actions - Unassign Inventory Source]**)는 이제 소스에 앞에 0을 제외하고 중복되는 SKU가 포함된 경우 예상대로 작동합니다(예: `01234` 및 `1234`). 이전에는 애플리케이션에서 인벤토리 소스에 대한 할당을 취소하지 않고 오류가 발생했습니다. <!--- ACP2E-2641-->

![해결된 문제](../assets/fix.svg) 이제 제품 재고 상태는 항상 입니다. **재고 있음** 무한 미납주문이 활성화되어 있고 미납주문 수량에 관계없이 제품이 사용자 정의 재고에 지정되는 경우 상점 첫 화면의 . 기존에는 백오더가 활성화된 상태에서도 상품이 품절됐다. <!--- ACP2E-664-->

![해결된 문제](../assets/fix.svg) 구성 가능한 제품 상위 및 하위 제품 스톡은 이제 소스 품목이 로 업데이트된 후 올바르게 업데이트됩니다. `POST /V1/inventory/source-items`. 하위 제품이 API를 통해 업데이트되면 기본 재고 확인을 위한 새 재고 플러그인이 추가되고 구성 가능한 제품 수량 및 상태가 업데이트됩니다. <!--- ACP2E-442-->

![해결된 문제](../assets/fix.svg) 품절된 그룹화된 제품은 더 이상 상점 첫 번째 카테고리 페이지에 나열되지 않습니다. <!--- ACP2E-2082-->

![해결된 문제](../assets/fix.svg) 의 패키지 이름이 수정되었습니다. `CatalogInventory` `composer.json`. <!--- ACP2E-2914-->

![해결된 문제](../assets/fix.svg) 다중 소스/재고 배포에서 수량이 0인 제품을 주문한 후 이제 관리자에서 미납 주문 상태가 올바르게 표시됩니다. [GitHub-33756](https://github.com/magento/magento2/issues/33756) <!--- ACP2E-713-->

![해결된 문제](../assets/fix.svg) 번들 제품이 재고 섹션에서 업데이트될 때 재고 부족 번들 제품이 더 이상 상점 카테고리 페이지에 표시되지 않습니다. <!--- ACP2E-2012-->

![해결된 문제](../assets/fix.svg) PHP 7.4의 호환성 문제가 해결되었습니다. <!--- AC-3192-->

![해결된 문제](../assets/fix.svg) 여러 옵션(여러 100개)이 포함된 번들 제품을 포함하는 저장 작업의 성능이 향상되었습니다. 이전에는 이러한 대용량 번들 제품을 저장하는 데 몇 분이 소요되었으며, 경우에 따라 인벤토리 서비스가 활성화된 배포에서 시간 초과가 발생하기도 했습니다. [GitHub-34732](https://github.com/magento/magento2/issues/34732) <!--- AC-1901-->

![해결된 문제](../assets/fix.svg) 제품 벌크 작업 도구(**[!UICONTROL Select Products]** > **[!UICONTROL Actions]** > **[!UICONTROL Assign Inventory Source]**)는 이제 행간을 제외하고 SKU가 복제될 때 여러 제품에 인벤토리 소스를 할당할 때 예상대로 작동합니다 `0` (예: `01234` 및 `1234`). 이전에는 하나의 제품에만 재고 출처가 할당되었습니다. [GitHub-35171](https://github.com/magento/magento2/issues/35171) <!--- AC-2584-->

![해결된 문제](../assets/fix.svg) 다음 `ProductInterface.only_x_left_in_stock` 이제 inventory 가 0이면 필드가 0을 반환합니다. 이전에는 null을 반환했습니다. [GitHub-29932](https://github.com/magento/magento2/issues/29932) <!--- AC-1806-->

![해결된 문제](../assets/fix.svg) 이제 관리자에서 기본 주식을 편집할 수 있습니다 **[!UICONTROL Stores]** > **[!UICONTROL Inventory]** > **[!UICONTROL Stocks]**. 이전에는 웹 사이트를 기본 스톡에 할당할 수 있었지만 기본 스톡에서 소스를 추가하거나 제거하려고 하면 콘솔에 JavaScript 오류가 표시되었습니다. <!--- ACP2E-545-->

![해결된 문제](../assets/fix.svg) <!--- ACP2E-274--> 재고 단일 소스 모드를 사용할 때 범주 목록 제품 수가 이제 올바릅니다. **[!UICONTROL Display Out-Of-Stock Products]** 설정이 활성화되었습니다. 이제 새 플러그인이 `AreProductsSalableInterface` 및 `StockConfigurationInterface` 을 클릭하여 총 제품 수를 확인합니다. 이전에는 범주 제품 목록에서 잘못된 제품 수량을 반환했습니다.

![해결된 문제](../assets/fix.svg) <!--- ACP2E-322--> 구성 가능한 제품은 이제 재고가 업데이트된 후 제품 목록의 마지막 위치로 이동됩니다. **[!UICONTROL Move out of stock to the bottom]** 설정이 활성화되었습니다. 관리자가 활성화된 정렬 순서를 무시하는 Elasticsearch 인덱스 정렬 순서를 무효화하기 위해 새 사용자 지정 데이터베이스 쿼리가 구현됩니다. 이전에는 이 설정을 활성화할 때 구성 가능한 제품 및 해당 하위 제품이 목록의 맨 아래로 이동되지 않았습니다.

## v1.2.4

Inventory management 1.2.4 (모듈 버전: `magento/inventory-metapackage = 1.2.4`)는 버전 2.4.4에서 지원되며 Adobe Commerce 버전 2.4.0, 클라우드 인프라의 Adobe Commerce 및 Magento Open Source 코드 베이스와 호환됩니다.

![해결된 문제](../assets/fix.svg) 이제 Commerce에 관리 제품 목록 보기에 모든 제품에 대한 정확한 판매 가능 수량 값이 표시됩니다. 이전에는 특수 문자가 포함된 SKU가 있는 재고 제품의 판매 가능 수량에 대해 빈 값이 표시되었습니다. <!--- MC-41936-->

![해결된 문제](../assets/fix.svg) 많은(약 10,000개) 인벤토리 소스가 있는 배포에서 제품을 장바구니에 추가하는 것과 같은 장바구니 및 체크아웃 작업의 성능이 향상되었습니다. <!--- MC-42570-->

![해결된 문제](../assets/fix.svg) 다음 `bin/magento inventory:reservation:list-inconsistencies` 이제 명령은 데이터베이스에서 예약이 누락되고 캐시가 지워진 경우에도 부분 선적이 있는 주문을 올바르게 처리합니다. 이전에는 미리 지운 캐시로 이 명령을 실행할 때 Commerce에 다음 오류가 표시되었습니다. `Area code is not set`. <!--- MC-42142-->

![해결된 문제](../assets/fix.svg) 그룹화된 제품 하위 제품의 증분 색인화로 인해 하위 항목이 공유될 때 다른 그룹화된 제품이 더 이상 잘못 색인화되지 않습니다. <!--- MC-41963-->

![해결된 문제](../assets/fix.svg) 이제 API로 카테고리에서 제품을 제거한 후 상점 카테고리 페이지에 올바른 제품 수가 표시됩니다. 이전에는 리인덱싱이 발생할 때까지 카테고리 페이지 제품 수가 올바르지 않았습니다. <!--- MC-42287-->

![해결된 문제](../assets/fix.svg) 이제 다음과 같은 경우에 대변 메모를 생성할 때 구성 가능한 제품을 재고로 반품할 수 있습니다. **[!UICONTROL Manage Stock]** 옵션이 비활성화되었습니다. 이전에는 Commerce에서 **주식으로 돌아가기** 이 옵션이 비활성화되었을 때 대변 메모 작성 페이지의 확인란입니다. <!--- MC-42002-->

![해결된 문제](../assets/fix.svg) 1만 개 초과 재고품 관리가 개선되었습니다. 이전에는 성능 문제로 인해 판매자가 웹 사이트를 시작하기 전에 관리자에서 재고를 편집할 수 없었던 경우가 있었습니다. <!--- MC-42643-->

![해결된 문제](../assets/fix.svg) 다음 **[!UICONTROL User Roles]** 관리자의 페이지가 업데이트되어 관리자에게 전달 방법 구성에 대한 제한된 권한 액세스 권한을 제공합니다. 다음 _배송 방법_ 섹션 이름이 (으)로 바뀌었습니다. _[!UICONTROL Delivery methods]_, 및_[!UICONTROL In-Store Pickup]_ 다음 아래로 이동됨: _[!UICONTROL Delivery methods]_섹션. [GitHub-30053](https://github.com/magento/magento2/issues/30053)  <!--- MC-41545-->

![해결된 문제](../assets/fix.svg) Adobe Commerce은 API에 의해 대변 메모가 업데이트된 후 더 이상 중복 제품 예약을 만들지 않습니다. <!--- MC-41757-->

![해결된 문제](../assets/fix.svg) 에서 전환 _[!UICONTROL Pick up in Store]_에 대한 탭_[!UICONTROL Shipping]_ 매장 픽업 배달만 사용할 수 있는 경우 체크아웃 워크플로의 탭에서 JavaScript 오류가 더 이상 트리거되지 않습니다. <!--- MC-42808-->

![해결된 문제](../assets/fix.svg) 판매 가능 제품 수량 및 재고 내 제품 수량이 이제 올바르게 동기화됩니다. 이전에는 취소된 주문에 대해 재고 예약 보상이 다시 생성되지 않았습니다. <!--- MC-42485-->

![해결된 문제](../assets/fix.svg) 유효성 검사기의 성능은 배송 유형이 있는 번들 제품의 하위 제품에 새 소스를 추가하지 않도록 최적화되어 있습니다 `Ship Together`. <!--- MC-43039-->

## 1.2.3

[!DNL Inventory Management] 1.2.3 (모듈 버전: `magento/inventory-metapackage = 1.2.3`)는 버전 2.4.3에서 지원되며 Adobe Commerce 버전 2.4.0, 클라우드 인프라의 Adobe Commerce 및 Magento Open Source 코드 베이스와 호환됩니다.

![해결된 문제](../assets/fix.svg) 프론트엔드의 복합 제품 가시성과 관련된 몇 가지 문제를 수정했습니다.

![해결된 문제](../assets/fix.svg) 최소 필요 수량으로 장바구니 페이지 관리 성능이 개선되었습니다.

![해결된 문제](../assets/fix.svg) 출처 생성, 재고 부족 품목, 재고 소싱, 할당된 출처 정렬, 매장 납품 및 재고 명령 관련 문제를 해결하기 위한 몇 가지 수정 사항이 타깃팅되었습니다.

![해결된 문제](../assets/fix.svg) [!DNL Commerce] 는 이제 매장 내 배송을 위해 3자리 캐나다 우편 번호를 지원합니다. 에 설정된 제한 사항으로 인해 6자리 코드는 지원되지 않습니다. `geonames.org`.

![해결된 문제](../assets/fix.svg) 이제 관리자는 비활성화된 제품에 대한 올바른 기본 재고 수량을 **제품** 표 및 **제품 편집** 다중 스토어 배포를 위한 페이지입니다.

![해결된 문제](../assets/fix.svg) [!DNL Commerce] 이제 번들 제품이 재입고되는 경우 카테고리 제품 캐시를 새로 고칩니다.

## 1.2.2

[!DNL Inventory Management] 1.2.2 (모듈 버전: `magento/inventory-metapackage = 1.2.2`)는 버전 2.4.2에서 지원되며 Adobe Commerce 버전 2.4.0, 클라우드 인프라의 Adobe Commerce 및 Magento Open Source 코드 베이스와 호환됩니다.

![해결된 문제](../assets/fix.svg) 프론트엔드의 복합 제품 가시성과 관련된 몇 가지 문제를 수정했습니다.

![해결된 문제](../assets/fix.svg) B2B에서 수량을 업데이트하는 동안 장바구니 페이지 성능이 개선되었습니다.

![해결된 문제](../assets/fix.svg) 매장 내 픽업, 대량 업데이트 및 재고 임계값 문제를 해결하기 위한 몇 가지 수정 사항이 타깃팅되었습니다.

![신규](../assets/new.svg) **기능 테스트.** 새로운 기능 테스트를 도입하고 기존 테스트에 대한 수정 사항을 제공하여 보다 안정적입니다.

## 1.2.1

[!DNL Inventory Management] 1.2.1(모듈 버전: `magento/inventory-metapackage = 1.2.1`)는 버전 2.4.1에서 지원되며 Adobe Commerce 버전 2.4.0, 클라우드 인프라의 Adobe Commerce 및 Magento Open Source 코드 베이스와 호환됩니다.

![해결된 문제](../assets/fix.svg) 와 관련된 알려진 문제가 해결되었습니다. `inventory_cleanup_reservations` cron job 을 통해 번들 제품의 매장 픽업 기능과 관련된 문제가 해결되었습니다. 이 업데이트에는 스톡 계산, 번들 제품 지원 및 미납주문 기능에 대한 일반적인 개선 사항도 포함됩니다.

![신규](../assets/new.svg) **기능 테스트.** 매장 내 픽업 기능에 대한 추가 기능을 제공하는 새로운 기능 테스트를 도입했습니다.

## 1.2.0

[!DNL Inventory Management] 1.2.0(모듈 버전: `magento/inventory-metapackage = 1.2.0`)는 Adobe Commerce 버전 2.4.0, 클라우드 인프라 기반 Adobe Commerce 및 Magento Open Source 코드 베이스에서 지원됩니다.

![해결된 문제](../assets/fix.svg) 소스 할당, 확장 가능한 환경 기능 지원, PHP 7.4, MySQL 8 및 PHPUNIT 9와의 호환성 문제를 해결하기 위해 여러 가지 수정 사항이 있습니다.

![신규](../assets/new.svg) **매장 내 게재 방법.** 사용자가 체크아웃 중에 픽업 위치로 사용할 소스를 선택할 수 있는 옵션이 추가되었습니다. 다음을 참조하십시오 [매장 내 게재](../stores-purchase/shipping-in-store-delivery.md) 다음에서 _영업 및 구매 경험 안내서_.

![신규](../assets/new.svg) **다중 소스 모드에 대한 번들 제품 지원.** 재고는 여러 출처가 있는 모든 제품 유형을 지원합니다.

![신규](../assets/new.svg) **비동기 재고 리인덱싱입니다.** 비동기적으로 재색인화하는 기능이 추가되었으며 여러 중요한 시나리오의 성능이 향상되었습니다.

![신규](../assets/new.svg) **대량 인터페이스.** 판매 가능성 확인을 위한 새로운 벌크 인터페이스 도입: `\Magento\InventorySalesApi\Api\AreProductsSalableInterface`, `\Magento\InventorySalesApi\Api\AreProductsSalableForRequestedQtyInterface`.

![신규](../assets/new.svg) **향상된 테스트 범위.** 새로운 기능은 발견된 문제 및 해결된 문제에 대한 확장 적용 범위를 포함하여 자동화된 테스트로 제공됩니다.

![알려진 문제](../assets/bug.svg) **알려진 문제.** 의 부재 `object_id` 예약 메타데이터의 필드에서 `inventory_cleanup_reservations` cron 작업이 제대로 작동하지 않습니다. 이 문제는에서 도입되었습니다. [magento/inventory#3046](https://github.com/magento/inventory/pull/3046).

**해결 방법:** 다음 MySQL 쿼리를 실행하여 예약을 수동으로 정리합니다.

```sql
SELECT GROUP_CONCAT(reservation_id) FROM inventory_reservation GROUP BY stock_id, sku HAVING SUM(quantity) = 0;
DELETE FROM inventory_reservation where reservation_id IN (result_of_the_first_query);
```

## 1.1.6

[!DNL Inventory Management] 1.1.6 (모듈 버전: `inventory-composer-metapackage = 1.1.6`)는 버전 2.3.6에서 지원되며 Adobe Commerce의 버전 2.3.5, 2.3.4, 2.3.3, 2.3.2, 2.3.1 및 2.3.0, 클라우드 인프라의 Adobe Commerce 및 Magento Open Source 코드 베이스와 호환됩니다.

![해결된 문제](../assets/fix.svg) 미납 주문, 대변 메모, 낮은 재고 보고서 그리드, &quot;불일치 해결&quot; CLI 도구와 관련된 문제 해결 및 일반적인 개선 사항.

![신규](../assets/new.svg) **비동기 재고 리인덱싱입니다.** 비동기적으로 재색인화하는 기능이 추가되었으며 여러 중요한 시나리오의 성능이 향상되었습니다.

## 1.1.5

[!DNL Inventory Management] 1.1.5 (모듈 버전: `inventory-composer-metapackage = 1.1.5`)는 버전 2.3.5에서 지원되며 Adobe Commerce, 클라우드 인프라의 Adobe Commerce 및 Magento Open Source 코드 베이스의 버전 2.3.4, 2.3.3, 2.3.2, 2.3.1 및 2.3.0과 호환됩니다.

![신규](../assets/new.svg) **제품 SKU가 변경되면 인벤토리를 업데이트합니다.** 새 비헤이비어 &quot;카탈로그와 동기화&quot;로 전환하기 위한 새 구성 설정이 도입되었습니다.

![신규](../assets/new.svg) **기능 테스트.** 테스트 범위 차이를 없애기 위해 새로운 기능 테스트를 도입했습니다. 몇 가지 문제를 해결하여 테스트를 보다 안정적이고 신뢰할 수 있도록 했습니다.)

![알려진 문제](../assets/bug.svg) 제품 과잉 판매를 방지하기 위한 수정 사항, 상점에서의 &quot;재고 부족&quot; 제품 가시성, 확장 가능한 환경 지원에 대한 수많은 수정 사항 및 사용자 인터페이스 개선 사항.

## 1.1.4

[!DNL Inventory Management] 1.1.4 (모듈 버전: `inventory-composer-metapackage = 1.1.4`)는 버전 2.3.4에서 지원되며 Adobe Commerce의 버전 2.3.3, 2.3.2, 2.3.1 및 2.3.0, 클라우드 인프라의 Adobe Commerce 및 Magento Open Source 코드 베이스와 호환됩니다.

![해결된 문제&#x200B;](../assets/fix.svg)**향상된 성능.** 메모리 사용을 줄이고 프로세스가 응답 없이 중단되는 경우를 방지하기 위해 인벤토리 예약 CLI 명령에 대한 번칭 논리를 도입했습니다.

![신규&#x200B;](../assets/new.svg)**향상된 테스트 범위.** 새로운 기능 테스트가 많이 도입되었습니다. 거의 모든 수동 인벤토리 시나리오는 자동화된 테스트로 다룹니다.

![알려진 문제](../assets/bug.svg) 대변 메모, 그룹화된 제품, 출처 및 재고 일괄 조치 관련 문제를 해결하기 위한 다양한 수정 사항이 있습니다.

## 1.1.3

[!DNL Inventory Management] 1.1.3 (모듈 버전: `inventory-composer-metapackage = 1.1.3`)는 버전 2.3.3에서 지원되며 Adobe Commerce 버전 2.3.2, 2.3.1 및 2.3.0, 클라우드 인프라의 Adobe Commerce 및 Magento Open Source 코드 베이스와 호환됩니다.

![해결된 문제&#x200B;](../assets/fix.svg)**Adobe Commerce 및 B2B 기능과의 통합 개선.** [!DNL Inventory Management] 이제 기본이 아닌 인벤토리 소스 및 재고를 사용하는 웹 사이트에 대해 다음 기능이 올바르게 작동합니다.

- SKU별 주문(Adobe Commerce)
- 빠른 주문(B2B)
- 구매요청 목록(B2B)

![신규&#x200B;](../assets/new.svg)**향상된 성능.** 기본 재고 및 소스를 실행하는 웹 사이트에 대해 상점 카탈로그 검색 성능이 개선되었습니다.

![신규&#x200B;](../assets/new.svg)**향상된 테스트 범위.** 자동화된 기능 및 통합 테스트 범위가 크게 증가했습니다.

## 1.1.2

[!DNL Inventory Management] 1.1.2 (모듈 버전: `inventory-composer-metapackage = 1.1.2`)는 버전 2.3.2에서 지원되며 Adobe Commerce의 버전 2.3.1 및 2.3.0, 클라우드 인프라의 Adobe Commerce 및 Magento Open Source 코드 베이스와 호환됩니다.

![해결된 문제](../assets/fix.svg) 추가됨 `source_code` GET에 대한 응답으로 `/V1/shipments` REST 엔드포인트 <!-- https://github.com/magento/inventory/pull/2142 -->

![해결된 문제](../assets/fix.svg) 출하되지 않은 주문에 대해 대변 메모를 발행한 후 예약을 올바르게 지우고 제품 수량을 갱신하기 위해 문제를 해결했습니다. 다음 옵션을 선택하는 경우 <!-- https://github.com/magento/inventory/pull/2179 -->

![해결된 문제](../assets/fix.svg) 제품 생성 중 수량을 입력할 때 구성 가능한 제품 하위 항목에 대한 수량을 올바르게 저장하는 문제가 해결되었습니다. <!-- https://github.com/magento/inventory/pull/2158 -->

의 새로운 모듈 [!DNL Inventory Management] 1.1.2 베타 버전은 다음과 같습니다.

```php
        'Magento_InventoryGraphQl' => 1,
        'Magento_InventoryReservations' => 1,
        'Magento_InventoryReservationsApi' => 1,
        'Magento_InventoryReservationCli' => 1,
        'Magento_InventoryExportStock' => 0,
        'Magento_InventoryExportStockApi' => 0,
```

![신규](../assets/new.svg) **대량 부분 스톡 전송 끝점이 추가되었습니다.** - 현재 벌크 전송 끝점은 지정된 모든 수량을 원본에서 대상 원본으로 이동합니다. 새로운 `/rest/V1/inventory/bulk-partial-source-transfer` 끝점을 사용하면 판매자가 부분 주식을 소스에서 소스로 일괄 작업으로 전송할 수 있습니다. 특정 수량을 이전하려면 다음을 사용하여 끝점에 요청을 입력합니다 `sku`, `qty`, `origin_source_code`, 및 `destination_source_code`. 전송 소스가에 할당되었는지 확인 `sku`: 전송할 수 있는 충분한 수량이 있습니다. 다음을 참조하십시오 [재고 일괄 조치](https://developer.adobe.com/commerce/webapi/rest/inventory/bulk-inventory/){target="_blank"} REST API 설명서에서 참조하십시오. <!-- https://github.com/magento/inventory/pull/2117 -->

![신규](../assets/new.svg) **예약 CLI 추가** - 새로운 명령을 사용하면 예약 불일치를 감지하고 해결할 수 있습니다. 주문이 제출되고 상태가 변경되면, [!DNL Inventory Management] 초기 예약을 생성하고 보상 예약을 통해 업데이트합니다. 이러한 명령은 주문 ID, SKU 및 Stock ID별로 발견된 불일치 목록을 반환하고 해결할 예약을 만듭니다. 다음을 참조하십시오. [CLI 참조](cli.md) 추가 정보. <!-- https://github.com/magento/inventory/pull/2199 https://github.com/magento/inventory/pull/2184 https://github.com/magento/inventory/pull/2171 https://github.com/magento/inventory/pull/2148  -->

![신규](../assets/new.svg) **소스 및 SSA 옵션의 성능 개선** - 출고 중 출처를 정렬하고 선택하면 출처가 많은 종목의 경우 성능이 저하됩니다. 이번 릴리스는 배송에서 SSA 옵션을 검토하고 선택할 때 사용 가능한 소스를 나열하고 정렬하는 데 상당한 성능 향상을 제공합니다. <!-- https://github.com/magento/inventory/pull/2056 https://github.com/magento/inventory/pull/2090 -->

![신규](../assets/new.svg) **Inventory management에 대한 GraphQL 지원 추가됨** - 이 릴리스에는 새 기능이 설치됩니다. `magento/module-inventory-graph-ql` 모듈. 더 GraphQL [ProductInterface 특성](https://developer.adobe.com/commerce/webapi/graphql/schema/products/interfaces/attributes/){target="_blank"} 이제 다음을 포함합니다. `only_x_left_in_stock` 및 `stock_status` 다음에 대한 속성 [!DNL Inventory Management] 지원. <!-- https://github.com/magento/inventory/pull/2124 -->

![신규](../assets/new.svg) **할당된 소스에 대한 간소화된 UI** - 제품 페이지의 할당된 소스 테이블에는 더 쉬운 업데이트와 많은 소스를 표시할 때 성능 향상을 위해 컨텐츠가 단순화되었습니다. 소스 이름별 모든 소스 목록(마우스로 가리키면 다음이 표시됩니다. `source_code`).

![신규](../assets/new.svg) **집계된 재고 서비스 내보내기** - 이번 릴리스에서는 Amazon, eBay 및 Google 쇼핑 광고와 같은 외부 Sales Channel을 지원하기 위해 새로운 내보내기 집계 재고 서비스(시스템에 예약 유지)를 제공합니다.  <!-- https://github.com/magento/inventory/pull/2067 -->

## 1.1.0

[!DNL Inventory Management] 1.1.0(모듈 버전: `inventory-composer-metapackage = 1.1.0`)가 지원되며 Adobe Commerce 버전 2.3.0, 클라우드 인프라의 Adobe Commerce 및 Magento Open Source 코드 베이스와 호환됩니다. [!DNL Inventory Management] 1.1.1은 패키지 이름 업데이트로만 릴리스되고, 버전 2.3.1에 대해 지원되며, Adobe Commerce 버전 2.3.0, 클라우드 인프라의 Adobe Commerce 및 Magento Open Source 코드 베이스와 호환됩니다.

![해결된 문제](../assets/fix.svg) **단일 및 다중 소스 모드에 대한 Elasticsearch 지원을 추가했습니다** — 이제 사용자 지정 재고로 Elasticsearch을 구성하고 사용할 수 있습니다. 다음을 참조하십시오 [Elasticsearch 서비스 설정](https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/configure/service/elasticsearch.html){target="_blank"} 를 참조하십시오. <!-- PR https://github.com/magento/inventory/pull/1943 -->

![해결된 문제](../assets/fix.svg) Default Stock 의 성능 문제를 해결하여 다양한 작업을 통해 성능을 크게 향상시켰습니다. 향상된 기능은 단일 소스 모드, 재고를 소스로 이전, 상점 카테고리 페이지 및 판매 가능 수량 계산에 대한 성능을 향상시킵니다.

<!-- All Performance Track issues resolved https://github.com/magento/inventory/issues?q=is%3Aopen+is%3Aissue+label%3APerformance -->

![해결된 문제](../assets/fix.svg) 구성 가능하고 그룹화된 제품에 대해 재고 부족 상태 및 대량으로 재고로 이전 문제가 해결되었습니다. 상위 제품을 선택하고 일괄 작업을 수행해도 제품 상태에 영향을 주지 않습니다. 상위 제품이 재고에 있으면 재고에 남아 있습니다.

<!-- PR https://github.com/magento/inventory/pull/1972 -->

![신규](../assets/new.svg) **거리 우선 순위 알고리즘** — 거리 우선순위 알고리즘은 거리 기반 배송 권장 사항에 대한 새로운 기본 소스 선택 알고리즘입니다. 이 알고리즘은 출하 목적지 주소의 위치를 출처 위치와 비교하여 출하를 이행할 가장 가까운 출처를 결정합니다. 거리는 가져온 지오코드 위치 데이터 또는 Google 방향(주행, 보행 또는 자전거)을 사용하여 물리적 거리 또는 한 위치에서 다른 위치로 이동하는 데 걸린 시간에 의해 결정될 수 있습니다.

![신규](../assets/new.svg) **확장된 소스 수량 목록** — 소스 수가 많은 판매자는 제품 그리드를 통해 제품당 모든 소스를 쉽게 마우스로 가리키고 볼 수 있습니다. 각 제품에는 최소 5개의 소스와 해당 수량이 표시됩니다. 소스를 마우스로 가리키면 전체 소스 목록과 현재 수량을 스크롤할 수 있습니다.

![알려진 문제](../assets/bug.svg) Magento Open Source 및 Adobe Commerce v2.3.1의 알려진 문제 - 소스 간 데이터의 비동기 마이그레이션은 PHP 클래스 및 메서드 이름을 반영하는 항목 이름이 있는 비동기 API의 변경으로 인해 문제가 발생합니다. 동기 작업 사용, 설정 **[!UICONTROL Run asynchronously]** 끝 `No`를 사용하는 것이 좋습니다.
