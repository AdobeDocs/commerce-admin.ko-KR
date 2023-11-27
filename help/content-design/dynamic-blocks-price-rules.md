---
title: 가격 규칙의 동적 블록
description: 동적 블록을 판촉 가격 규칙과 연결합니다.
exl-id: e1564df2-1c06-4d11-a32d-6f5c0be974e3
feature: Page Content, Price Rules
source-git-commit: b659c7e1e8f2ae9883f1e24d8045d6dd1e90cfc0
workflow-type: tm+mt
source-wordcount: '289'
ht-degree: 0%

---

# 가격 규칙의 동적 블록

{{ee-feature}}

임의 [동적 블록](dynamic-blocks.md) 이 항목을 만들면 프로모션과 연결할 수 있습니다. 연결하려면 먼저 동적 블록과 를 모두 만들어야 합니다. [카탈로그 가격 규칙](../merchandising-promotions/price-rules-catalog.md) 또는 [장바구니 가격 규칙](../merchandising-promotions/price-rules-cart.md). 가격 규칙을 작업하는 동안 또는 동적 블록에서 작업할 때 연관을 만들 수 있습니다.

>[!IMPORTANT]
>
>이 연결을 만들면 동적 블록이 표시됩니다 **전용** 규칙이 실행될 때. 프로모션이 세그먼트 A로 타겟팅되면 블록이 세그먼트 A로 표시됩니다. 프로모션이 활성화되지 않으면 블록이 표시되지 않습니다.

## 동적 블록을 가격 규칙과 연결

1. 다음에서 _관리자_ 사이드바, 이동 **[!UICONTROL Marketing]** > _[!UICONTROL Promotions]_다음 중 하나를 선택합니다.

   - **[!UICONTROL Catalog Price Rules]**
   - **[!UICONTROL Cart Price Rules]**

1. 그리드에서 동적 블록과 연결할 규칙을 찾아 편집 모드로 엽니다.

1. 아래로 스크롤하고 확장합니다. ![확장 선택기](../assets/icon-display-expand.png) **[!UICONTROL Related Dynamic Blocks]**.

1. 첫 번째 열에서 필터를 다음으로 설정합니다. `Any` 및 클릭 **[!UICONTROL Reset Filter]**.

   이제 격자에 사용 가능한 모든 동적 블록이 나열됩니다.

1. 규칙과 연결할 각 동적 블록의 확인란을 선택합니다.

   ![선택한 동적 블록 추가](./assets/price-rule-cart-related-dynamic-blocks-any.png){width="600" zoomable="yes"}

1. 완료되면 다음을 클릭하십시오. **[!UICONTROL Save]**.

## 가격 규칙을 동적 블록과 연결

1. 다음에서 _관리자_ 사이드바, 이동 **[!UICONTROL Content]** > _[!UICONTROL Elements]_>**[!UICONTROL Dynamic Blocks]**.

1. 그리드에서 동적 블록을 찾아 편집 모드로 엽니다.

1. 아래로 스크롤하고 확장합니다. **[!UICONTROL Related Promotions]**.

   현재 연관된 모든 가격 규칙이 그리드에 나타납니다.

1. 새 연결된 규칙을 추가하거나 현재 연결을 제거합니다.

   - 장바구니 프로모션을 연결하려면 **[!UICONTROL Add Cart Price Rules]**.

   - 제품 관련 프로모션을 연결하려면 **[!UICONTROL Add Catalog Price Rules]**.

1. 그리드에서 동적 블록과 연결할 각 규칙의 확인란을 선택합니다.

1. 클릭 **[!UICONTROL Add Selected]**.

   ![선택한 가격 규칙을 동적 블록에 추가](./assets/pb-dynamic-block-add-related-cart-price-rules.png){width="600" zoomable="yes"}

1. 완료되면 다음을 클릭하십시오. **[!UICONTROL Save]**.
