---
title: Source 우선 순위 알고리즘 구성
description: 추천하기 위해 재고에서 할당된 소스의 순서에 사용되는 소스 우선 순위를 구성하는 방법에 대해 알아보십시오.
exl-id: 7b25212d-0cd0-4280-be23-c67f06db900a
feature: Inventory, Shipping/Delivery
source-git-commit: 023716935a6657b0dc2317876debe608e65bf010
workflow-type: tm+mt
source-wordcount: '271'
ht-degree: 0%

---

# Source 우선 순위 알고리즘 구성

사용자 정의 재고에는 상점 전면을 통해 사용 가능한 제품 재고를 판매하고 배송할 지정된 소스 목록이 포함됩니다. 이 알고리즘은 스톡에 할당된 소스의 순서를 사용하여 권장 사항을 제공합니다.

실행될 때 알고리즘은 다음과 같습니다.

- 상단에서 시작하는 재고 수준에서 구성된 소스 순서를 통해 작동합니다.

- 목록의 주문, 사용 가능한 수량 및 주문 수량을 기준으로 제품당 출하 및 출고할 수량을 권장합니다.

- 주문 선적이 채워질 때까지 목록 아래로 계속

- 목록에 있는 경우 비활성화된 소스를 건너뜁니다.

구성하려면 주문 이행을 위해 해당 소스를 맨 위에서 아래로 정렬합니다. Source 선택 알고리즘(SSA)은 선적 및 재고 공제를 결정할 때 이 순서를 사용하는 알고리즘 우선 순위를 제공합니다. [재고 소스 우선 순위 지정](stocks-prioritize-sources.md)을 참조하십시오.

## 소스의 우선 순위 구성

1. _관리자_ 사이드바에서 **[!UICONTROL Stores]** > **[!UICONTROL Inventory]** > **[!UICONTROL Stocks]**(으)로 이동합니다.

1. 편집 모드에서 스토리를 열고 _[!UICONTROL Sources]_영역으로 이동합니다.

1. **[!UICONTROL Assign Sources]**&#x200B;을(를) 클릭합니다.

1. _[!UICONTROL Assign Sources]_보기에서 필요한 원본의 확인란을 선택한 다음&#x200B;**[!UICONTROL Done]**을(를) 클릭하여 원본에 원본을 할당합니다.

>[!NOTE]
>
>배송에 [거리 우선 순위](distance-priority-algorithm.md) 알고리즘을 사용할 때, 선택한 배송 [계산 모드](distance-priority-algorithm.md)(주행, 자전거 타기 또는 걷기)에 대해 경로와 데이터가 반환되지 않는 경우, SSA는 기본적으로 Source 우선 순위를 사용합니다.

![우선 순위 지정 후 Source 순서](assets/inventory-stock-priority-after.png)

| 아이콘 | 설명 |
|----------------------------------------------|----------------------------------------------------------------|
| ![우선 순위를 설정할 아이콘을 끌어서 놓기](assets/icon-drag-and-drop-action.png) | 우선 순위에 따라 소스를 드래그하여 놓는 데 사용합니다. |
| ![소스 할당을 취소하려면 아이콘을 클릭합니다](assets/icon-delete-action.png) | 재고에 출처 지정을 취소합니다. |
