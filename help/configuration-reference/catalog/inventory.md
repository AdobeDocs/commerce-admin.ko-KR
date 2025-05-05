---
title: '[!UICONTROL Catalog] &gt; [!UICONTROL Inventory]'
description: Commerce 관리자의 [!UICONTROL Catalog] &gt; [!UICONTROL Inventory] 페이지에서 구성 설정을 검토하십시오.
exl-id: 80113a31-3585-4ee1-95af-31efc09389eb
feature: Configuration, Inventory
source-git-commit: 5a4417373f6dc720e8e14f883c27348a475ec255
workflow-type: tm+mt
source-wordcount: '1195'
ht-degree: 0%

---

# [!UICONTROL Catalog] > [!UICONTROL Inventory]

{{config}}

>[!NOTE]
>
>Adobe Commerce 및 Magento Open Source용 [!DNL Inventory Management]은(는) 제품 인벤토리를 관리하는 도구를 제공합니다. 단일 상점을 여러 창고, 상점, 픽업 위치, 직송 업체 등에 보유한 판매자는 이러한 기능을 사용하여 판매 수량을 유지하고 납품을 처리하여 주문을 완료할 수 있습니다. 이러한 기능과 이러한 기능을 사용하여 여러 위치의 주식을 관리하는 방법에 대한 자세한 내용은 [_[!DNL Inventory Management] 사용 안내서&#x200B;_](https://experienceleague.adobe.com/docs/commerce-admin/inventory/introduction.html?lang=ko)를 참조하십시오.

## [!UICONTROL Stock Options]

![재고 옵션](./assets/catalog-inventory-stock-options.png)<!-- zoom -->

<!-- [Stock Options](https://experienceleague.adobe.com/ko/docs/commerce-admin/inventory/configuration/global-options) -->

| 필드 | [범위](../../getting-started/websites-stores-views.md#scope-settings) | 설명 |
|--- |--- |--- |
| [!UICONTROL Decrease Stock When Order is Placed] | 글로벌 | `Yes`(으)로 설정하면 주문 시 재고의 수량을 줄입니다. _재고 관리_&#x200B;를 사용하도록 설정하면 주문 제품 및 수량에 대한 예약이 입력됩니다. 옵션: `Yes` / `No` |
| [!UICONTROL Set Items' Status to be in Stock When Order is Cancelled] | 스토어 뷰 | `Yes`(으)로 설정된 경우 주문이 취소되면 재고로 항목을 반환합니다. _재고 관리_&#x200B;를 사용하도록 설정하면 취소된 제품 및 수량에 대한 예약이 취소됩니다. 옵션: `Yes` / `No` |
| [!UICONTROL Display Out of Stock Products] | 글로벌 | `Yes`(으)로 설정된 경우 품절된 제품을 표시합니다. 제품 경고도 활성화된 경우 고객은 제품을 사용할 수 있게 되면 알림을 받기 위해 등록할 수 있습니다. 옵션: `Yes` / `No` |
| [!UICONTROL Only X left Threshold] | 웹 사이트 | `Only x left` 메시지의 임계값을 설정합니다. 예를 들어 3으로 설정하면 3개 이하의 항목이 재고에 있을 때 메시지가 표시됩니다. 값이 `0`(으)로 설정된 경우 메시지가 표시되지 않습니다. |
| [!UICONTROL Display products availability in Stock on Storefront] | 스토어 뷰 | `Yes`(으)로 설정된 경우 제품 페이지에 `In Stock` 또는 `Out of Stock` 메시지를 표시합니다. 옵션: `Yes` / `No` |
| [!UICONTROL Enable Inventory Check On Cart Load] | 글로벌 | 장바구니에서 제품을 로드할 때 인벤토리 검사가 수행되는지 여부를 결정합니다. 이 인벤토리 검사를 비활성화하면 체크아웃 단계의 성능이 향상될 수 있습니다(특히 장바구니에 많은 항목이 있는 경우). 그러나 사전 유효성 검사를 건너뛸 경우 나중에 체크아웃 프로세스에서 _재고 부족_ 오류가 표시될 수 있습니다. 옵션: `Yes` / `No` |
| [!UICONTROL Synchronize with Catalog] | 글로벌 | `Yes`(으)로 설정된 경우 재고 데이터는 카탈로그 변경(예: 제품 제거, 제품 SKU 변경 및 제품 유형 변경)에 따라 조정되며 재고와 카탈로그 간에 일관성을 유지합니다. 옵션: `Yes` / `No` |

{style="table-layout:auto"}

## [!UICONTROL Product Stock Options]

![제품 재고 옵션](./assets/catalog-inventory-product-stock-options.png)<!-- zoom -->

<!-- [Product Stock Options](https://experienceleague.adobe.com/ko/docs/commerce-admin/inventory/configuration/global-options) -->

| 필드 | [범위](../../getting-started/websites-stores-views.md#scope-settings) | 설명 |
|--- |--- |----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Manage Stock] | 글로벌 | 전체 재고 관리를 사용하여 카탈로그의 항목을 관리할지 여부를 결정합니다. 옵션: <br/>**예** - 전체 재고 관리를 활성화하여 현재 재고 있는 항목의 수를 추적합니다. <br/>**아니요** - 현재 재고 항목 수를 추적하지 않습니다. |
| [!UICONTROL Backorders] | 글로벌 | 스토어에서 미납 주문을 관리하는 방법을 결정합니다. 미납주문은 주문의 처리 상태를 변경하지 않습니다. 상품은 재고가 있는지 여부와 관계없이 주문 즉시 펀드가 승인 또는 포착된다. 제품을 사용할 수 있게 되면 제품이 배송됩니다. 옵션: <br/>**미납주문 없음** - 제품이 품절되었을 때 미납주문을 수락하지 않습니다. <br/>**0** 미만 수량 허용 - 수량이 영(0) 미만으로 떨어질 때 미납주문을 허용합니다. <br/>**0 이하 수량을 허용하고 고객에게 알림** - 수량이 영(0) 이하로 떨어지면 미납주문을 수락하지만 주문을 계속 할 수 있음을 고객에게 알립니다. |
| [!UICONTROL Use deferred Stock update] | 글로벌 | ![Adobe Commerce](../../assets/adobe-logo.svg)(Adobe Commerce만 해당) 미납주문이 허용되는 경우 재고 업데이트를 연기할지 여부를 결정합니다(_미납주문_ 옵션이 `No backorders` 기본값 이외의 값으로 설정됨). 단일 제품 또는 전체 웹 사이트에 대해 작동하며, 주문이 완료된 후 _작업 큐_ 메커니즘을 사용하여 재고 수량 지표를 비동기적으로 업데이트할 수 있습니다. 이 옵션은 [Inventory management](../../inventory-management/introduction.md)과(와) 함께 [비동기 주문 배치](https://experienceleague.adobe.com/docs/commerce-operations/performance-best-practices/high-throughput-order-processing.html?lang=ko#asynchronous-order-placement)에서도 작동합니다. |
| 장바구니에서 허용되는 최대 수량 | 글로벌 | 단일 주문으로 구매할 수 있는 제품의 최대 수를 결정합니다. 기본적으로 최대 수량은 10,000으로 설정됩니다. |
| [!UICONTROL Out-of-Stock Threshold] | 글로벌 | 제품이 품절된 것으로 간주되는 재고 수준을 결정합니다. 옵션: <br/>**양수** - _미납 주문_&#x200B;이 비활성화되어 있는 경우 양수를 입력하십시오. 미납주문을 사용할 경우 이 금액은 무시됩니다. <br/>**0** - _미납주문_&#x200B;이(가) 활성화된 경우 `0`을(를) 입력하면 무제한 미납주문이 허용됩니다. <br/>**음수** - _미납주문_&#x200B;을 사용하도록 설정한 경우 음수를 입력하는 것이 좋습니다. 금액은 판매 가능 수량에 추가됩니다. 예를 들어 이 수량까지 주문을 허용하려면 -50을 입력합니다. |
| [!UICONTROL Minimum Qty Allowed in Shopping Cart] | 글로벌 | 고객 그룹에 따라 구매할 수 있는 항목의 최소 금액을 결정합니다. 기본적으로 최소 수량은 1로 설정됩니다. 특정 고객 그룹에 대해 다른 값을 입력하려면 **[!UICONTROL Add Minimum Qty]**&#x200B;을(를) 클릭하십시오. |
| [!UICONTROL Notify for Quantity Below] | 글로벌 | 재고가 임계값 아래로 떨어졌다는 알림이 전송되는 재고 수준을 결정합니다. |
| [!UICONTROL Enable Qty Increments] | 글로벌 | 품목을 수량 단위로 판매할 수 있는지 여부를 결정합니다. 옵션: `Yes` / `No` |
| [!UICONTROL Qty Increments] | 글로벌 | 수량 증분을 구성하는 제품 수를 설정합니다. |
| [!UICONTROL Automatically Return Credit Memo Item to Stock] | 글로벌 | 대변 메모에 포함된 항목을 자동으로 재고로 반환할지 여부를 결정합니다. 옵션: `Yes` / `No` |

{style="table-layout:auto"}

## [!UICONTROL Admin Bulk Operations]

![관리 일괄 작업](./assets/catalog-inventory-admin-bulk-operations.png)<!-- zoom -->

<!-- [Admin Bulk Operations](https://experienceleague.adobe.com/ko/docs/commerce-admin/inventory/configuration/global-options) -->

>[!NOTE]
>
>**비동기 큐 관리자**&#x200B;를 구성하고 지원하려면 명령줄을 사용해야 합니다. 이 경우 개발자 지원이 필요할 수 있습니다. _구성 가이드_&#x200B;에서 [메시지 큐 소비자 시작](https://experienceleague.adobe.com/docs/commerce-operations/configuration-guide/cli/start-message-queues.html?lang=ko)을 참조하세요.

| 필드 | [범위](../../getting-started/websites-stores-views.md#scope-settings) | 설명 |
|--- |--- |--- |
| [!UICONTROL Run asynchronously] | 글로벌 | [일괄](../../inventory-management/bulk-assignment.md) 원본 할당, 원본 할당 해제 및 [원본을 원본으로 전송](../../inventory-management/inventory-transfer.md)을 포함한 대량 제품 작업에 대해 일괄 작업을 비동기적으로 실행할지 여부를 결정합니다. _[!UICONTROL Asynchronous batch size]_&#x200B;까지 대량 작업을 수집한 다음 해당 작업을 실행합니다. 이 기능은 기본적으로 비활성화되어 있습니다. 활성화하기 전에 일괄 작업으로 성능을 검토하는 것이 좋습니다. 옵션:<br/>**`Yes`**- [!DNL Inventory Management]에 대한 모든 대량 작업을 비동기적으로 실행합니다. 활성화하려면 비동기 큐 관리자를 구성해야 합니다.<br/>**`No`**- 기본값 대량 작업을 비동기적으로 실행하지 않습니다. |
| [!UICONTROL Asynchronous batch size] | 글로벌 | _[!UICONTROL Asynchronous batch size]_&#x200B;필드에 대한 값을 입력하려면&#x200B;**[!UICONTROL Run asynchronously]**&#x200B;을(를) `Yes`(으)로 설정하십시오. <br/>기본 일괄 처리 크기는 100입니다. 벌크 프로세스가 이 양에 도달하면 실행됩니다. |

{style="table-layout:auto"}

## [!UICONTROL Inventory Indexer Settings]

| 필드 | [범위](../../getting-started/websites-stores-views.md#scope-settings) | 설명 |
|--- |--- |--- |
| [!UICONTROL Stock/Source reindex strategy] | 글로벌 | 재고/소스 리인덱싱에 사용되는 전략을 결정합니다. 옵션: `Synchronous` / `Asynchronous`(비동기 모드에 대해 비동기 큐 관리자를 구성해야 함) |

{style="table-layout:auto"}

>[!NOTE]
>
> 주문 관련 활동에 대한 인벤토리 업데이트의 종속성으로 인해 `Synchronous` 또는 `Asynchronous` 설정에 관계없이 제품 저장 시 인벤토리 인덱서도 트리거됩니다.


## [!UICONTROL Distance Provider for Distance Based SSA]

![거리 기반 SSA에 대한 거리 공급자](./assets/catalog-inventory-distance-provider.png)<!-- zoom -->

<!-- [Distance Providers for Distance Based SSA](https://experienceleague.adobe.com/ko/docs/commerce-admin/inventory/configuration/distance-priority-algorithm) -->

| 필드 | [범위](../../getting-started/websites-stores-views.md#scope-settings) | 설명 |
|--- |--- |--- |
| [!UICONTROL Provider] | 글로벌 | 거리 우선순위 Source 선택 알고리즘에 사용할 공급자를 결정합니다. 이 기능은 기본적으로 활성화되어 있습니다. 옵션: <br/>**`Google MAP`**- Google 서비스를 사용하여 배송 대상 주소와 원본 위치(주소 및 GPS 좌표) 간의 거리 및 시간을 계산합니다. 이 옵션을 사용하려면 Google API 키가 필요하며 Google을 통해 요금이 부과될 수 있습니다.<br/>**`Offline Calculation`** - 포함된 데이터베이스를 사용하여 거리를 계산하여 배송 대상 주소와 가장 가까운 원본을 확인합니다. 이 옵션을 사용하려면 명령줄을 사용하여 배송하는 모든 국가에 대한 데이터베이스 위치 콘텐츠를 처음에 다운로드하도록 개발자 지원이 필요할 수 있습니다. |

{style="table-layout:auto"}

## [!UICONTROL Google Distance Provider]

![Google 거리 공급자](./assets/catalog-inventory-distance-provider-settings.png)<!-- zoom -->

<!-- [Google Distance Provider](https://experienceleague.adobe.com/ko/docs/commerce-admin/inventory/configuration/distance-priority-algorithm) -->

| 필드 | [범위](../../getting-started/websites-stores-views.md#scope-settings) | 설명 |
|--- |--- |--- |
| [!UICONTROL Google API key] | 글로벌 | Google MAP 공급자에 대한 Google API 키를 입력합니다. 키는 [!DNL Google Maps Platform]에서 가져온 것이므로 [!DNL Geocoding API] 및 [!DNL Distance Matrix API]을(를) 사용하도록 설정해야 합니다. 자세한 내용은 _Inventory management 안내서_&#x200B;에서 [거리 우선 순위 알고리즘 구성](../../inventory-management/distance-priority-algorithm.md#configure-the-distance-priority-algorithm)을 참조하십시오. |
| [!UICONTROL Computation mode] | 글로벌 | 배송 주소 및 재고에 지정된 모든 출처와의 거리를 계산하는 방향 및 경로를 결정합니다. 기본적으로 계산은 운전 모드를 사용합니다. 옵션: <br/>**`Driving`**- 기본 설정이며, 도로 네트워크를 사용하여 표준 주행 방향을 요청합니다.<br/>**`Walking`** - 보행자 경로 및 인도를 사용하여 보행 방향을 요청합니다(가능한 경우). <br/>**`Bicycling`**- 자전거 도로 및 기본 거리를 사용하여 자전거 방향을 요청합니다(현재 미국과 일부 캐나다 도시에서만 사용 가능). |
| [!UICONTROL Value] | 글로벌 | 운송 대상 주소까지의 출처 위치에 대한 거리 및 시간을 계산하고 반환할 사항을 나타냅니다. 거리 우선순위 알고리즘은 배송지 주소까지의 거리 또는 시간이 가장 짧은 소스를 권장하므로 배송을 이행하는 데 더 빠르고 저렴할 수 있습니다. 옵션: <br/>**`Distance`**- 지표(킬로미터 및 미터) 또는 임페리얼(마일 및 피트) 포인트 사이의 거리를 반환합니다.<br/>**`Time to Destination`** - 원본 위치에서 배송 주소로 이동하는 데 필요한 시간을 시간 및 분 단위로 반환합니다. |

{style="table-layout:auto"}
