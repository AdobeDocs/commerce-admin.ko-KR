---
title: 재고 수량 관리
description: 새 제품에 대한 소스 및 수량을 할당하거나 기존 제품을 변경하는 방법에 대해 알아봅니다.
exl-id: b3d4a4c0-725a-4e62-854f-efb6a5709f73
feature: Inventory, Products
source-git-commit: 4d89212585fa846eb94bf83a640d0358812afbc5
workflow-type: tm+mt
source-wordcount: '319'
ht-degree: 0%

---

# 재고 수량 관리

다음 정보에서는 신규 제품에 대한 출처와 수량을 지정하거나 기존 제품을 변경하는 방법에 대해 자세히 설명합니다.

제품을 생성할 때 제품을 생성하는 동안 소스와 수량을 지정합니다. 자세한 지침은 [제품 만들기](../catalog/product-create.md)를 참조하세요. 이러한 페이지에는 출처와 출처당 수량에 대한 단일 및 다중 출처 정보가 포함되어 있습니다.

[!DNL Inventory Management]을(를) 사용하여 업그레이드된 [!DNL Commerce]에 처음 액세스하면 모든 제품 및 수량이 기본 Source에 할당됩니다. .csv 파일을 통해 새 제품을 가져오면 기본 Source에도 할당됩니다.

단일 및 다중 소스 판매자는 제품당 또는 대량으로 소스, 재고 수량 및 임계값을 업데이트할 수 있습니다.

- 단일 소스 판매자는 기본 Source에 대한 제품 수량을 업데이트할 수 있습니다. 이 수량은 판매 가능한 제품의 총 수입니다.

- 복수 출처 판매자는 각 위치(창고, 상점, 직송 업체 등)에 대해 제품당 복수 출처와 수량을 지정할 수 있습니다. 제품 재고 금액을 설정하기 전에 소스를 추가하는 것이 좋습니다.

제품에 출처 및 수량을 추가할 때 제품 그리드를 통해 금액을 조회할 수 있습니다. 원본 수가 많은 경우 _[!UICONTROL Quantity per Source]_&#x200B;위로 마우스를 가져가면 현재 수량이 있는 스크롤 가능한 전체 원본 목록을 볼 수 있습니다.

![소스당 제품 수량](assets/inventory-product-quantity.png){width="600" zoomable="yes"}

다음 옵션을 사용하여 제품에 재고를 지정할 수 있습니다.

- [제품당 소스 할당](sources-assign-per-product.md) - 카탈로그의 제품당 소스를 수동으로 할당합니다.

- [제품당 수량 할당](quantities-assign-per-product.md) - 소스당 제품에 현재고 금액을 추가합니다. 이 정보는 다중 소스 판매자에만 적용됩니다.

- [일괄 소스 할당 및 할당 해제](bulk-assignment.md) - 일괄 작업으로 선택한 제품에 소스를 할당합니다. 인벤토리를 전송하고 소스를 제거하려면 [Source으로 인벤토리 전송](inventory-transfer.md) 옵션을 사용하십시오.

- [Source으로 인벤토리 전송](inventory-transfer.md) - 모든 인벤토리를 하나의 원본 원본에서 대상 원본으로 일괄 전송합니다.

- [수량 가져오기 및 내보내기](inventory-import-export.md) - 가져오기 및 내보내기 기능을 사용하여 여러 제품 SKU를 소스 및 재고 수량으로 업데이트합니다.
