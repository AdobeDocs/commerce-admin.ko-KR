---
title: 제품 유형
description: ' [!DNL Inventory Management] 이(가) 모든 Adobe Commerce 및 Magento Open Source 제품 유형에 대한 인벤토리 및 주문 관리를 지원하는 방법에 대해 알아봅니다.'
exl-id: c800168a-e8b2-4d72-bd3d-68f46ece8a5e
feature: Inventory, Products
TQID: https://experienceleague.adobe.com/3F5vZOseQC7ILpL0j-ksjWP-GW7c0gUN9Zy7hylzzHU
product_v2: id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2: id: c1256247-af4b-46d8-9dca-0c654ecfa157
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: f8a45b24-4be7-4f1b-909b-60d06b483a20
level_v2: id: b5a62a22-46f7-4f0d-b151-3fc640bef588id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2: id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 213
ht-degree: 0%

---

# 제품 유형

[!DNL Inventory Management]은(는) Adobe Commerce 및 Magento Open Source의 모든 제품 유형(단순, 구성 가능, 가상, 다운로드 가능, 번들 및 그룹화)에 대한 인벤토리 및 주문 관리를 지원합니다. 소스, 재고 및 배송에 대해 제품 유형별로 옵션 및 요구 사항이 다를 수 있습니다.

- [단일 소스 판매자](merchant-sourcing.md#single-source-merchants) 추가 업데이트 없이 제품 설정 및 수량을 만들고 업데이트합니다. 생성된 모든 제품과 새로 가져온 제품은 자동으로 기본 Source 및 기본 스톡에 할당되며, 활성화된 경우 즉시 고객이 사용할 수 있습니다.

- [다중 소스 판매자](merchant-sourcing.md#multi-source-merchants) 제품을 만드는 동안 또는 후에 소스, 소스당 수량 및 설정을 할당합니다. [!DNL Commerce]은(는) 새로 가져온 모든 제품을 기본 Source에 할당하므로 소스 및 수량을 할당하는 추가 편집이 필요합니다.

| 제품 유형 | 배송 및 Source 선택 알고리즘 |
|--|--|
| [[!UICONTROL Simple]](../catalog/product-create-simple.md){target="_blank"} | 배송 시 SSA 권장 사항 및 재정의를 지원합니다. |
| [[!UICONTROL Configurable]](../catalog/product-create-configurable.md){target="_blank"} | 배송 시 SSA 권장 사항 및 재정의를 지원합니다. |
| [[!UICONTROL Virtual]](../catalog/product-create-virtual.md){target="_blank"} | 항상 SSA 권장 사항을 사용합니다. 시스템은 송장을 생성할 때 알고리즘을 암시적으로 실행하고 항상 제안된 결과를 사용합니다.<br/>이 결과를 조정할 수 없습니다. |
| [[!UICONTROL Downloadable]](../catalog/product-create-downloadable.md){target="_blank"} | 항상 SSA 권장 사항을 사용합니다. 시스템은 송장을 생성할 때 알고리즘을 암시적으로 실행하고 항상 제안된 결과를 사용합니다. <br/>이 결과를 조정할 수 없습니다. |
| [[!UICONTROL Bundle]](../catalog/product-create-bundle.md){target="_blank"} | 배송 시 SSA 권장 사항 및 재정의를 지원합니다. |
| [[!UICONTROL Grouped]](../catalog/product-create-grouped.md){target="_blank"} | 배송 시 SSA 권장 사항 및 재정의를 지원합니다. |
