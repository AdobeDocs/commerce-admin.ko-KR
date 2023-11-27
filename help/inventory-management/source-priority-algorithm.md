---
title: 소스 우선 순위 알고리즘 구성
description: 추천하기 위해 재고에서 할당된 소스의 순서에 사용되는 소스 우선 순위를 구성하는 방법에 대해 알아보십시오.
exl-id: 7b25212d-0cd0-4280-be23-c67f06db900a
feature: Inventory, Shipping/Delivery
source-git-commit: 023716935a6657b0dc2317876debe608e65bf010
workflow-type: tm+mt
source-wordcount: '271'
ht-degree: 0%

---

# 소스 우선 순위 알고리즘 구성

사용자 정의 재고에는 상점 전면을 통해 사용 가능한 제품 재고를 판매하고 배송할 지정된 소스 목록이 포함됩니다. 이 알고리즘은 스톡에 할당된 소스의 순서를 사용하여 권장 사항을 제공합니다.

실행될 때 알고리즘은 다음과 같습니다.

- 상단에서 시작하는 재고 수준에서 구성된 소스 순서를 통해 작동합니다.

- 목록의 주문, 사용 가능한 수량 및 주문 수량을 기준으로 제품당 출하 및 출고할 수량을 권장합니다.

- 주문 선적이 채워질 때까지 목록 아래로 계속

- 목록에 있는 경우 비활성화된 소스를 건너뜁니다.

구성하려면 주문 이행을 위해 해당 소스를 맨 위에서 아래로 정렬합니다. 출처선택알고리즘(SSA)에서는 출고 및 재고 공제를 결정할 때 이 순서를 이용한 알고리즘 우선순위를 제공한다. 다음을 참조하십시오 [재고에 대한 소스 우선 순위 지정](stocks-prioritize-sources.md).

## 소스의 우선 순위 구성

1. 다음에서 _관리자_ 사이드바, 이동 **[!UICONTROL Stores]** > **[!UICONTROL Inventory]** > **[!UICONTROL Stocks]**.

1. 편집 모드에서 스톡을 열고 다음으로 이동 _[!UICONTROL Sources]_영역입니다.

1. 클릭 **[!UICONTROL Assign Sources]**.

1. 다음에서 _[!UICONTROL Assign Sources]_필요한 소스에 대한 확인란을 선택하고&#x200B;**[!UICONTROL Done]**재고에 출처를 지정합니다.

>[!NOTE]
>
>사용 시 [거리 우선 순위](distance-priority-algorithm.md) 경로 및 데이터가 선택한 항목에 대해 반환되지 않는 경우 운송 알고리즘 [계산 모드](distance-priority-algorithm.md) (운전, 자전거 또는 도보) 배송의 경우 SSA는 기본적으로 소스 우선 순위 사용으로 설정됩니다.

![우선 순위 지정 후 소스 순서](assets/inventory-stock-priority-after.png)

| 아이콘 | 설명 |
|----------------------------------------------|----------------------------------------------------------------|
| ![아이콘을 드래그하여 놓아 우선 순위 설정](assets/icon-drag-and-drop-action.png) | 우선 순위에 따라 소스를 드래그하여 놓는 데 사용합니다. |
| ![소스 할당을 취소하려면 클릭 아이콘](assets/icon-delete-action.png) | 재고에 출처 지정을 취소합니다. |
