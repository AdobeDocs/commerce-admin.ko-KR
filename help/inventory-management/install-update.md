---
title: ' [!DNL Inventory Management] 설치, 업데이트 및 제거'
description: ' [!DNL Inventory Management] 메타패키지를 관리하는 방법을 알아봅니다.'
exl-id: d088ff35-c0e1-41c8-89fb-78180eaefbf7
level: Experienced
feature: Inventory, Install
badgePaas: label="PaaS만" type="Informative" url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="Adobe Commerce 온 클라우드 프로젝트(Adobe 관리 PaaS 인프라) 및 온프레미스 프로젝트에만 적용됩니다."
source-git-commit: b4623ada788d44f4628930dcf5dfcb51dd88ee3a
workflow-type: tm+mt
source-wordcount: '620'
ht-degree: 0%

---

# [!DNL Inventory Management] 설치, 업데이트 및 제거

[!DNL Inventory Management] 모듈은 단일 및 다중 소스 판매자가 판매 채널의 제품 수량과 재고를 관리할 수 있도록 모든 재고 기능과 옵션을 제공합니다. 이러한 기능은 Adobe Commerce 및 Magento Open Source 2.4.x 릴리스에서 사용할 수 있습니다.

이러한 기능과 확장은 Magento Open Source 커뮤니티 엔지니어링 프로그램을 통해 [인벤토리 프로젝트](https://github.com/magento/inventory)의 일부로 개발되었습니다.

[!DNL Inventory Management]은(는) 기본적으로 모든 기능이 활성화된 Adobe Commerce 및 Magento Open Source의 2.3.x 및 2.4.x 릴리스에 설치됩니다. 이러한 재고 기능을 활성화하는 데 추가 단계가 필요하지 않습니다. v2.1.x 또는 2.2.x에서 업그레이드하려면 추가 단계가 필요할 수 있습니다. [Inventory management 업그레이드](#upgrade-inventory-management)를 참조하십시오.

[빠른 시작 온-프레미스 설치](https://experienceleague.adobe.com/docs/commerce-operations/installation-guide/composer.html){target="_blank"}에 따른 설치가 권장됩니다. 모든 [!DNL Inventory Management] 모듈을 받으려면 메타패키지로 설치하십시오.

`composer.json` 메타패키지에 있는 다음 줄은 [!DNL Inventory Management]을(를) 설치합니다.

```json
        magento/inventory-composer-metapackage = 1.1.3
```

[!DNL Inventory Management] 메타패키지 버전 목록을 보려면 [릴리스 정보](release-notes.md)를 참조하세요.

[!DNL Inventory Management] 설치 프로세스는 모든 모듈을 `<Magento_installation_directory>/app/etc/config.php` 파일에 추가합니다. `1` 값은 해당 모듈이 활성화되었음을 나타냅니다. 다음 모듈 목록이 추가됩니다.

```php
        'Magento_Inventory' => 1,
        'Magento_InventoryAdminUi' => 1,
        'Magento_InventoryAdvancedCheckout' => 1,
        'Magento_InventoryApi' => 1,
        'Magento_InventoryBundleProduct' => 1,
        'Magento_InventoryBundleProductAdminUi' => 1,
        'Magento_InventoryCatalog' => 1,
        'Magento_InventorySales' => 1,
        'Magento_InventoryCatalogAdminUi' => 1,
        'Magento_InventoryCatalogApi' => 1,
        'Magento_InventoryCatalogSearch' => 1,
        'Magento_InventoryConfigurableProduct' => 1,
        'Magento_InventoryConfigurableProductAdminUi' => 1,
        'Magento_InventoryConfigurableProductIndexer' => 1,
        'Magento_InventoryConfiguration' => 1,
        'Magento_InventoryConfigurationApi' => 1,
        'Magento_InventoryDistanceBasedSourceSelection' => 1,
        'Magento_InventoryDistanceBasedSourceSelectionAdminUi' => 1,
        'Magento_InventoryDistanceBasedSourceSelectionApi' => 1,
        'Magento_InventoryElasticsearch' => 1,
        'Magento_InventoryExportStockApi' => 1,
        'Magento_InventoryIndexer' => 1,
        'Magento_InventorySalesApi' => 1,
        'Magento_InventoryGroupedProduct' => 1,
        'Magento_InventoryGroupedProductAdminUi' => 1,
        'Magento_InventoryGroupedProductIndexer' => 1,
        'Magento_InventoryImportExport' => 1,
        'Magento_InventoryCache' => 1,
        'Magento_InventoryLowQuantityNotification' => 1,
        'Magento_InventoryLowQuantityNotificationApi' => 1,
        'Magento_InventoryMultiDimensionalIndexerApi' => 1,
        'Magento_InventoryProductAlert' => 1,
        'Magento_InventoryRequisitionList' => 1,
        'Magento_InventoryReservations' => 1,
        'Magento_InventoryReservationCli' => 1,
        'Magento_InventoryReservationsApi' => 1,
        'Magento_InventoryExportStock' => 1,
        'Magento_InventorySalesAdminUi' => 1,
        'Magento_InventorySalesFrontendUi' => 1,
        'Magento_InventorySetupFixtureGenerator' => 1,
        'Magento_InventoryShipping' => 1,
        'Magento_InventorySourceDeductionApi' => 1,
        'Magento_InventorySourceSelection' => 1,
        'Magento_InventorySourceSelectionApi' => 1,
        'Magento_InventoryLowQuantityNotificationAdminUi' => 1,
        'Magento_InventoryShippingAdminUi' => 1,
        'Magento_InventoryGraphQl' => 1,
```

## [!DNL Inventory Management]개 기능 사용

설치, 업그레이드 또는 업데이트 시 Admin의 _[!UICONTROL Manage Stock]_옵션이 기본적으로 사용됩니다. 이 옵션을 사용하면 인벤토리 추적 및 관리를 사용할 수 있지만 모듈 상태에는 영향을 주지 않습니다. 모듈을 비활성화하려면 다음 섹션을 참조하십시오.

구성에 대한 자세한 내용은 [Inventory management 구성](configuration.md)을 참조하십시오.

## Inventory management 비활성화

>[!IMPORTANT]
>
>기본 [!DNL Inventory Management] 모듈을 사용하는 것이 좋습니다. [!DNL Inventory Management] 모듈이 비활성화된 시스템에 사용되는 대체 [!DNL CatalogInventory] 모듈이 이제 더 이상 사용되지 않습니다. [!DNL Inventory Management] 모듈을 사용하지 않도록 설정하면 시스템이 불안정해지고 여러 가지 문제가 발생할 수 있습니다.

[!DNL Inventory Management] 모듈을 사용하지 않도록 설정하여 다음을 수행할 수 있습니다.

* 2.0.x, 2.1.x, 2.2.x 또는 2.3.x에서 2.4.x로 마이그레이션하는 상인의 업그레이드 프로세스 속도를 높입니다.
* 사용자 지정 또는 서드파티 재고 및 주문 관리 시스템 모듈을 사용합니다.

해당 모듈을 사용하지 않도록 설정하는 방법에 대한 자세한 내용은 _설치 안내서_&#x200B;의 [모듈 사용 또는 사용 안 함](https://experienceleague.adobe.com/docs/commerce-operations/installation-guide/tutorials/manage-modules.html) 페이지를 참조하십시오.

완료되면 시스템은 `<Magento_installation_directory>/app/etc/config.php`에 다음과 같이 시작하는 모듈 및 값 목록을 제공합니다.

```php
   'Magento_Inventory' => 0,
   'Magento_InventoryAdminUi' => 0,
   'Magento_InventoryAdvancedCheckout' => 0,
   ...
```

>[!IMPORTANT]
>
>OMS 커넥터 모듈이 설치되어 있는 경우 커넥터 모듈인 `Magento_InventoryMessageBus` 모듈을 비활성화하지 않도록 하십시오. OMS에서 커넥터를 사용해야 합니다.

## Inventory management 제거

>[!IMPORTANT]
>
>기본 [!DNL Inventory Management] 모듈을 사용하는 것이 좋습니다. [!DNL Inventory Management] 모듈이 제거된 시스템에 사용되는 대체 [!DNL CatalogInventory] 모듈이 이제 더 이상 사용되지 않습니다. [!DNL Inventory Management] 모듈을 제거하면 시스템이 불안정해지고 다양한 문제가 발생할 수 있습니다.

[!DNL Inventory Management] 기능을 사용하지 않도록 선택하면 이러한 모듈을 제거(제거)할 수 있습니다. 작성기 파일을 통해 모든 모듈을 제거하려면 `composer.json`에 다음을 추가하십시오.

```
"replace": {
        "magento/module-inventory": "*",
        "magento/module-inventory-admin-ui": "*",
        "magento/module-inventory-advanced-checkout": "*",
        "magento/module-inventory-api": "*",
        "magento/module-inventory-bundle-product": "*",
        "magento/module-inventory-bundle-product-admin-ui": "*",
        "magento/module-inventory-cache": "*",
        "magento/module-inventory-catalog": "*",
        "magento/module-inventory-catalog-admin-ui": "*",
        "magento/module-inventory-catalog-api": "*",
        "magento/module-inventory-catalog-search": "*",
        "magento/module-inventory-configurable-product": "*",
        "magento/module-inventory-configurable-product-admin-ui": "*",
        "magento/module-inventory-configurable-product-indexer": "*",
        "magento/module-inventory-configuration": "*",
        "magento/module-inventory-configuration-api": "*",
        "magento/module-inventory-distance-based-source-selection": "*",
        "magento/module-inventory-distance-based-source-selection-admin-ui": "*",
        "magento/module-inventory-distance-based-source-selection-api": "*",
        "magento/module-inventory-export-stock": "*",
        "magento/module-inventory-export-stock-api": "*",
        "magento/module-inventory-elasticsearch": "*",
        "magento/module-inventory-graph-ql": "*",
        "magento/module-inventory-grouped-product": "*",
        "magento/module-inventory-grouped-product-admin-ui": "*",
        "magento/module-inventory-grouped-product-indexer": "*",
        "magento/module-inventory-import-export": "*",
        "magento/module-inventory-indexer": "*",
        "magento/module-inventory-low-quantity-notification": "*",
        "magento/module-inventory-low-quantity-notification-admin-ui": "*",
        "magento/module-inventory-low-quantity-notification-api": "*",
        "magento/module-inventory-multi-dimensional-indexer-api": "*",
        "magento/module-inventory-product-alert": "*",
        "magento/module-inventory-requisition-list": "*",
        "magento/module-inventory-reservations": "*",
        "magento/module-inventory-reservations-api": "*",
        "magento/module-inventory-reservation-cli": "*",
        "magento/module-inventory-sales": "*",
        "magento/module-inventory-sales-admin-ui": "*",
        "magento/module-inventory-sales-api": "*",
        "magento/module-inventory-sales-frontend-ui": "*",
        "magento/module-inventory-setup-fixture-generator": "*",
        "magento/module-inventory-shipping": "*",
        "magento/module-inventory-shipping-admin-ui": "*",
        "magento/module-inventory-source-deduction-api": "*",
        "magento/module-inventory-source-selection": "*",
        "magento/module-inventory-source-selection-api": "*",
        "magento/module-inventory-visual-merchandiser": "*",
        "magento/module-inventory-swatches-frontend-ui": "*",
        "magento/module-inventory-quote-graph-ql": "*",
        "magento/module-inventory-in-store-pickup": "*",
        "magento/module-inventory-in-store-pickup-sales": "*",
        "magento/module-inventory-in-store-pickup-admin-ui": "*",
        "magento/module-inventory-in-store-pickup-sales-admin-ui": "*",
        "magento/module-inventory-in-store-pickup-api": "*",
        "magento/module-inventory-in-store-pickup-sales-api": "*",
        "magento/module-inventory-in-store-pickup-frontend": "*",
        "magento/module-inventory-in-store-pickup-shipping": "*",
        "magento/module-inventory-in-store-pickup-graph-ql": "*",
        "magento/module-inventory-in-store-pickup-shipping-admin-ui": "*",
        "magento/module-inventory-in-store-pickup-multishipping": "*",
        "magento/module-inventory-in-store-pickup-shipping-api": "*",
        "magento/module-inventory-in-store-pickup-quote": "*",
        "magento/module-inventory-in-store-pickup-webapi-extension": "*",
        "magento/module-inventory-in-store-pickup-quote-graph-ql": "*",
        "magento/module-inventory-configurable-product-frontend-ui": "*",
        "magento/module-inventory-catalog-search-configurable-product": "*",
        "magento/module-inventory-catalog-search-bundle-product": "*",
        "magento/module-inventory-catalog-frontend-ui": "*",
        "magento/module-inventory-bundle-import-export": "*",
        "magento/module-inventory-bundle-product-indexer": "*"
    }
```

이 변경 사항이 완료되면 작성기 설치 를 실행하고 이러한 Inventory management 모듈이 자동으로 제거됩니다.

## Inventory management 업그레이드

### 이전 [!DNL Commerce] 버전

기존 2.1.x, 2.2.x 또는 2.3.x 설치를 Adobe Commerce 또는 Magento Open Source 2.4.x로 업그레이드하거나 업데이트하는 경우 기본적으로 [!DNL Inventory Management] 모듈이 비활성화됩니다. 이 기본 설정은 역으로 호환되지 않는 업그레이드를 방지하고 OMS(Order Management)를 더 잘 지원하기 위한 예방 조치입니다.

>[!NOTE]
>
>Order Management은 [!DNL Inventory Management]을(를) 지원하지 않습니다. 업그레이드할 때 [!DNL Inventory Management] 모듈이 비활성화되어 OMS 및 [!DNL Commerce] 2.3.x가 원활하게 작동할 수 있습니다.


[!DNL Inventory Management] 모듈을 사용하려면:

1. `<Commerce_installation_directory>/app/etc/config.php` 파일을 편집합니다.
1. 활성화하려면 모든 인벤토리 모듈을 `0`에서 `1`(으)로 수정하십시오.
1. 데이터베이스 업데이트:

   ```bash
   bin/magento setup:upgrade
   ```

1. 캐시를 정리합니다.

   ```bash
   bin/magento cache:clean
   ```

업그레이드한 후 [예약 불일치 명령](cli.md)을 사용하는 것이 좋습니다. 업그레이드할 때 모든 제품이 기본 재고에 추가됩니다. 대기 중인 주문이 있는 경우 명령은 판매 가능 수량 및 판매 및 주문 이행에 대한 예약을 올바르게 갱신합니다.

### 이전 [!DNL Inventory Management] 버전

[!DNL Inventory Management]의 이전 릴리스에서 최신 버전으로 업그레이드할 때는 일반적인 확장 업그레이드 단계를 따르십시오.

최신 버전의 경우 다음과 같이 메타 패키지 버전을 업데이트합니다.

```json
        magento/inventory-composer-metapackage = 1.1.3
```

Commerce 업그레이드에 대한 자세한 내용은 다음 안내서를 참조하십시오.

* [Commerce 업데이트 안내서](https://experienceleague.adobe.com/docs/commerce-operations/upgrade-guide/overview.html){target="_blank"}
* [모듈 사용 또는 사용 안 함](https://experienceleague.adobe.com/docs/commerce-operations/installation-guide/tutorials/manage-modules.html){target="_blank"}
