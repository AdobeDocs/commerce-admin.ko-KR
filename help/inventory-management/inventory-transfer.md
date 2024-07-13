---
title: 재고를 소스로 이전
description: 멀티 소스 판매자가 한 소스 위치에서 다른 소스 위치로 제품 재고를 전송하는 방법에 대해 알아봅니다.
exl-id: 30438412-bc93-4e65-8b6a-5ddb50afa7ff
feature: Inventory, Configuration
source-git-commit: 4d89212585fa846eb94bf83a640d0358812afbc5
workflow-type: tm+mt
source-wordcount: '279'
ht-degree: 0%

---

# 재고를 소스로 이전

비즈니스 요구 및 위치 상태에 따라 다중 소스 판매자는 종종 한 소스 위치에서 다른 소스 위치로 제품 재고를 이전합니다. 예를 들어 창고 위치를 닫거나 특정 제품을 더 이상 특정 위치에서 출하하지 않고 해당 제품에 대한 모든 작업을 새 위치로 이동할 수 있습니다.

이 옵션을 사용하면 하나 이상의 제품, 재고를 이전할 출처 및 수량을 입고할 목적지 출처를 선택할 수 있습니다.

- 재고 수량, Source 품목 상태(재고 중/재고 부족) 및 선택한 출처에 대한 통지 수량이 제품별로 이동됩니다.

- 제품에 해당 소스가 없는 경우 건너뜁니다.

- 출처에 대한 모든 제품 재고가 이동됩니다. 부분 수량은 이전할 수 없습니다.

>[!NOTE]
>
>출처와 목적지 출처가 서로 다른 재고에 있을 경우, 이는 진행 중인 주문에 대한 누적 판매 수량 및 예약에 영향을 미칩니다.

재고 수량을 이전할 때 출처의 지정을 취소할 수도 있습니다.

{{$include /help/_includes/unassign-source.md}}

![다른 원본으로 인벤토리 전송](assets/inventory-bulk-transfer-source.gif)

1. _관리자_ 사이드바에서 **[!UICONTROL Catalog]** > **[!UICONTROL Products]**(으)로 이동합니다.

1. 소스를 수정할 제품을 선택합니다.

   제품을 찾아보거나 검색하여 찾고 전송할 확인란을 선택합니다.

1. 맨 위에 있는 **[!UICONTROL Actions]** 메뉴를 클릭하고 **[!UICONTROL Transfer Inventory to Source]**&#x200B;을(를) 선택합니다.

1. 확인 대화 상자에서 **[!UICONTROL OK]**&#x200B;을(를) 클릭합니다.

1. 제품을 새 대상으로 전송하려면 원본(_[!UICONTROL from]_) 원본을 선택하세요.

1. 제품을 새 대상으로 전송하려면 대상(_[!UICONTROL to]_) 원본을 선택하십시오.

1. 제품에서 원본을 제거하려면 선택적 확인란 **[!UICONTROL Unassign from origin source after transfer]**&#x200B;을(를) 선택하십시오.

   ![전송할 원본 및 대상 선택](assets/inventory-bulk-transfer-summary.png){width="600" zoomable="yes"}

1. **[!UICONTROL Transfer Inventory]**&#x200B;을(를) 클릭합니다.

   모든 제품 수량은 출처 출처에서 공제되어 목적지 출처에 추가됩니다. 수량 및 판매 가능 수량이 자동으로 업데이트됩니다.
