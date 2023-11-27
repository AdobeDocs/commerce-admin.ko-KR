---
title: 인벤토리 토큰 추가
description: 재고를 추가하고 판매 채널(웹 사이트)에 소스를 매핑하여 판매 가능한 수량 및 제품 재고에 대한 직접적인 링크를 제공하는 방법에 대해 알아봅니다.
exl-id: d0032ed7-c0d6-4654-b182-43a165e7dcf6
source-git-commit: 4d89212585fa846eb94bf83a640d0358812afbc5
workflow-type: tm+mt
source-wordcount: '409'
ht-degree: 1%

---

# 스톡 추가

재고는 판매 채널(또는 웹 사이트)에 출처를 매핑하여 판매 가능한 수량 및 제품 재고에 대한 직접적인 링크를 제공합니다.

사용자 지정 스톡을 만들 때 웹 사이트 및 소스를 할당합니다. 소스에는 활성화 및 비활성화 소스가 포함될 수 있습니다. 예를 들어 재고에 창고를 추가하여 재고 관리 및 선적 완료를 위한 위치를 열 준비를 할 수 있습니다.

소스를 추가한 후 소스 순서를 최상위(첫 번째)에서 최하위(마지막)로 정렬해야 합니다. 이 주문은 주문 배송 중 권장 사항에 영향을 줍니다.

![새 재고](assets/inventory-stock-new.png){width="600" zoomable="yes"}

## 재고 재고 추가

1. 다음에서 _관리자_ 사이드바, 이동 **[!UICONTROL Stores]** > _[!UICONTROL Inventory]_>**[!UICONTROL Stock]**.

1. 클릭 **[!UICONTROL Add New Stock]**.

1. 확장 ![확장 선택기](../assets/icon-display-expand.png) 다음 **[!UICONTROL General]** 섹션에 고유한 값을 입력하십시오. **[!UICONTROL Name]** 새 재고를 식별합니다.

   ![일반 스톡 옵션](assets/inventory-stock-general.png){width="350" zoomable="yes"}

1. 확장 ![확장 선택기](../assets/icon-display-expand.png) 다음 **[!UICONTROL Sales Channels]** 섹션을 선택하고 **[!UICONTROL Websites]** 이 재고를 사용할 수 있는 곳.

   다중 사이트 설치의 경우 Ctrl 키(PC) 또는 Command 키(Mac)를 누른 채로 각 웹 사이트를 클릭합니다.

   >[!NOTE]
   >
   >다른 주식에 할당된 웹 사이트 또는 판매 채널을 선택하면 해당 주식에서 할당이 해제됩니다. Sales Channel 지정 재고에 지정되지 않은 모든 사용자는 기본 재고에 지정됩니다.

   ![주식에 대한 Sales Channel 옵션](assets/inventory-sales-channel.png){width="350" zoomable="yes"}

1. 확장 ![확장 선택기](../assets/icon-display-expand.png) 다음 **[!UICONTROL Sources]** 섹션에 추가하고 기본값 이외의 모든 스톡에 대해 다음 작업을 수행합니다.

   - 클릭 **[!UICONTROL Assign Sources]**.

   ![지정된 소스](assets/inventory-stock-sources.png){width="350" zoomable="yes"}

   - 재고에 지정할 모든 출처의 체크박스를 선택합니다.

   >[!IMPORTANT]
   >
   >동일한 출처를 여러 주식에 지정할 경우 해당 출처에 지정된 제품이 초과 판매될 수 있습니다.

   - 클릭 **[!UICONTROL Done]**.

     추가된 소스는 할당된 소스에 표시됩니다.

     ![재고에 출처 지정](assets/inventory-assign-sources.png){width="600" zoomable="yes"}

1. 사용 ![정렬 아이콘](assets/icon-sort.png) 소스를 맨 위(첫 번째)에서 맨 아래(마지막)의 우선 순위로 끌어다 놓습니다.

   출고 지시 시 출처 주문이 중요합니다.

   ![지정된 소스 예](assets/inventory-stock-priority-after.png){width="600" zoomable="yes"}

1. 다음에서 _[!UICONTROL Save]_(![메뉴 화살표](../assets/icon-menu-down-arrow-red.png)) 메뉴, 선택&#x200B;**[!UICONTROL Save & Close]**.

## 필드 설명

| 필드 | 설명 |
|--|--|
| **[!UICONTROL General]** | |
| [!UICONTROL Name] | 재고 이름. For example: `UK Stock`, `US Stock` |
| **[!UICONTROL Sales Channels]** | |
| [!UICONTROL Websites] | 다음을 정의합니다 [범위](../getting-started/websites-stores-views.md#scope-settings) 특정 웹 사이트에 재고를 할당하여 재고의 일부를 다음과 같이 _판매 채널_. 종목당 하나 이상의 웹 사이트를 선택합니다. 각 웹 사이트는 하나의 주식에만 할당할 수 있습니다. |
| **[!UICONTROL Sources]** | |
| [!UICONTROL Assign Sources] | 이 재고에 재고 출처를 지정합니다. 사용자 지정 소스를 기본 스톡에 할당할 수 없습니다. |
| [!UICONTROL Assigned Sources] | 지정된 소스 목록. 다음을 사용하여 소스 드래그 앤 드롭 ![정렬 아이콘](assets/icon-sort.png) 주문 이행 및 배송을 위해 우선 순위가 지정된 주문으로.<br/><br/>**[!UICONTROL Code]**- 소스에 대한 고유 코드 ID.<br/>**[!UICONTROL Name]** - 소스에 대한 이름 설명입니다.<br/>**[!UICONTROL Unassign]**- 다음을 사용하여 스톡에서 지정된 소스 제거 ![휴지통 아이콘](../assets/icon-delete-trashcan-solid.png). |
