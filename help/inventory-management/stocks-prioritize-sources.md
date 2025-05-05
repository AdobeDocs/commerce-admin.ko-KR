---
title: 재고에 대한 재고 출처 우선 순위 지정
description: 출처를 선적 및 재고 공제를 결정할 때 사용되는 우선순위에서 맨위에서 맨아래로 정렬하는 방법에 대해 알아봅니다.
exl-id: 16db3ee3-ce99-40dd-b1a3-fcb145b1298f
feature: Inventory, Configuration
source-git-commit: 4d89212585fa846eb94bf83a640d0358812afbc5
workflow-type: tm+mt
source-wordcount: '210'
ht-degree: 0%

---

# 재고에 대한 소스 우선 순위 지정

[stock](stocks-manage.md)에 [소스](sources-manage.md)을(를) 추가한 후 주문을 이행하기 위해 우선 순위를 위에서 아래로 조정하십시오. Source 선택 알고리즘(SSA)은 선적 및 재고 공제를 결정할 때 이 순서를 사용하는 알고리즘 우선 순위를 제공합니다.

재고에 대한 출처 우선순위는 제품 재고를 편집할 때 지정된 출처에 영향을 주지 않습니다.

이 예에서 UK Stock은 London에 한 개의 상점과 두 개의 창고 및 Berlin에 한 개의 창고에 대해 주문되지 않은 소스가 할당되어 있습니다.

![우선 순위 지정 전 Source 순서](assets/inventory-priority-before.png){width="350" zoomable="yes"}

상인은 더 큰 베를린 창고에서 우선 출하하는 것을 선호하며, 그 다음으로는 런던 창고, 런던 범람 장소, 그리고 마지막으로 런던의 상점으로부터 우선 출하하는 것을 선호합니다. 순서를 변경하려면 항목을 원하는 순서로 드래그하여 놓습니다.

1. _관리자_ 사이드바에서 **[!UICONTROL Stores]** > _[!UICONTROL Inventory]_>**[!UICONTROL Stocks]**(으)로 이동합니다.

1. _편집_ 모드로 주식을 엽니다.

1. 필요한 경우 _[!UICONTROL Sources]_&#x200B;탭을 확장합니다.

1. ![정렬 아이콘](assets/icon-sort.png)을 사용하여 소스를 맨 위(첫 번째)에서 맨 아래(마지막)로 우선 순위에 놓습니다.

   이 주문은 배송 주문 시 중요합니다. SSA는 출처의 순서에 따라 배송을 추천합니다

1. 변경 내용을 저장하려면 **[!UICONTROL Save & Continue]**&#x200B;을(를) 클릭합니다.

![우선 순위 지정 후 Source 순서](assets/inventory-stock-priority-after.png){width="350" zoomable="yes"}
