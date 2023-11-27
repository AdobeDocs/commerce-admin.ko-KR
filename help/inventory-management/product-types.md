---
title: 제품 유형
description: 방법 알아보기 [!DNL Inventory Management] 는 모든 Adobe Commerce 및 Magento Open Source 제품 유형에 대한 재고 및 주문 관리를 지원합니다.
exl-id: c800168a-e8b2-4d72-bd3d-68f46ece8a5e
feature: Inventory, Products
source-git-commit: 4d89212585fa846eb94bf83a640d0358812afbc5
workflow-type: tm+mt
source-wordcount: '211'
ht-degree: 0%

---

# 제품 유형

[!DNL Inventory Management] 는 Adobe Commerce 및 Magento Open Source의 모든 제품 유형(단순, 구성 가능, 가상, 다운로드 가능, 번들 및 그룹화)에 대한 재고 및 주문 관리를 지원합니다. 소스, 재고 및 배송에 대해 제품 유형별로 옵션 및 요구 사항이 다를 수 있습니다.

- [단일 소스 판매자](merchant-sourcing.md#single-source-merchants) 추가 업데이트 없이 제품 설정 및 수량을 만들고 업데이트합니다. 생성되거나 새로 임포트된 모든 제품은 기본 출처 및 기본 재고에 자동으로 지정되며, 활성화된 경우 즉시 고객에게 제공됩니다.

- [멀티 소스 판매자](merchant-sourcing.md#multi-source-merchants) 제품 생성 중 또는 후에 소스, 소스당 수량 및 설정을 지정합니다. [!DNL Commerce] 새로 가져온 모든 제품을 기본 출처에 할당하므로 출처와 수량을 할당하는 추가 편집이 필요합니다.

| 제품 유형 | 배송 및 소스 선택 알고리즘 |
|--|--|
| [[!UICONTROL Simple]](../catalog/product-create-simple.md){target="_blank"} | 배송 시 SSA 권장 사항 및 재정의를 지원합니다. |
| [[!UICONTROL Configurable]](../catalog/product-create-configurable.md){target="_blank"} | 배송 시 SSA 권장 사항 및 재정의를 지원합니다. |
| [[!UICONTROL Virtual]](../catalog/product-create-virtual.md){target="_blank"} | 항상 SSA 권장 사항을 사용합니다. 시스템은 송장을 생성할 때 알고리즘을 암시적으로 실행하고 항상 제안된 결과를 사용합니다.<br/>이러한 결과는 조정할 수 없습니다. |
| [[!UICONTROL Downloadable]](../catalog/product-create-downloadable.md){target="_blank"} | 항상 SSA 권장 사항을 사용합니다. 시스템은 송장을 생성할 때 알고리즘을 암시적으로 실행하고 항상 제안된 결과를 사용합니다. <br/>이러한 결과는 조정할 수 없습니다. |
| [[!UICONTROL Bundle]](../catalog/product-create-bundle.md){target="_blank"} | 배송 시 SSA 권장 사항 및 재정의를 지원합니다. |
| [[!UICONTROL Grouped]](../catalog/product-create-grouped.md){target="_blank"} | 배송 시 SSA 권장 사항 및 재정의를 지원합니다. |
