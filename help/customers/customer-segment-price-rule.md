---
title: 가격 규칙의 고객 세그먼트
description: 스토어에 대한 타겟팅된 판촉을 정의할 수 있도록 고객 세그먼트를 장바구니 가격 규칙과 연결하는 방법에 대해 알아봅니다.
exl-id: eaa04e7a-c0f9-4f09-8e65-75965ccbdc69
feature: Customers, Configuration, Price Rules
TQID: https://experienceleague.adobe.com/MSMNikJwG2lQuLlQxnK82zjCOeF-u8JEjmabKFJgpZU
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2:
  - id: dac87252-6066-4d6e-a9d2-f6d84c323de7
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2:
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 232
ht-degree: 0%

---

# 가격 규칙의 고객 세그먼트

{{ee-feature}}

고객 세그먼트를 [장바구니 가격 규칙](../merchandising-promotions/price-rules-cart.md)과 연결하여 타깃팅된 프로모션에 사용할 수 있습니다.

![장바구니 가격 규칙 - 대상 고객 세그먼트](assets/price-rule-cart-condition-segments.png){width="700" zoomable="yes"}

_&#x200B;**세그먼트를 장바구니 가격 규칙에 연결하려면:**&#x200B;_

1. _관리자_ 사이드바에서 **[!UICONTROL Marketing]** > _프로모션_ > **[!UICONTROL Cart Price Rules]**(으)로 이동합니다.

1. 새 규칙 또는 기존 규칙을 엽니다.

   * 새 규칙을 사용하려면 오른쪽 상단의 **[!UICONTROL Add New Rule]**&#x200B;을(를) 클릭합니다.
   * 기존 규칙을 사용하려면 목록에서 규칙을 클릭하여 편집 모드로 엽니다.

1. 아래로 스크롤하여 **[!UICONTROL Conditions]** 섹션을 확장합니다.

1. 조건을 추가합니다.

   * 조건 목록을 표시하는 _추가_(![목록 아이콘](../assets/icon-add-green-circle.png)) 아이콘을 클릭합니다. **[!UICONTROL Customer Segment]**&#x200B;을(를) 선택합니다.

   ![장바구니 가격 규칙 - 고객 세그먼트 조건 추가](assets/condition-customer-segment.png){width="600" zoomable="yes"}

   기본적으로 조건은 일치하는 조건을 찾도록 설정됩니다. 필요한 경우 **[!UICONTROL matches]** 링크를 클릭하고 연산자를 다음 중 하나로 변경합니다.

   * `does not match`
   * `is one of`
   * `is not one of`

   ![조건 연산자](assets/price-rule-condition-customer-segment-operator.png){width="600" zoomable="yes"}

1. 특정 세그먼트를 타겟팅하려면 기타 **..** 링크를 클릭하여 추가 옵션을 표시합니다. 그런 다음 _선택기_(![목록 아이콘](../assets/icon-list-chooser.png)) 아이콘을 클릭하여 고객 세그먼트 목록을 표시합니다.

1. 목록에서 조건을 타겟팅할 각 세그먼트의 확인란을 선택합니다.

   ![장바구니 가격 규칙 - 조건 선택기 목록](assets/condition-segment-chooser-list.png){width="600" zoomable="yes"}

1. 선택한 고객 세그먼트를 조건에 배치하려면 **[!UICONTROL Select]**&#x200B;을(를) 클릭하십시오.

1. 필요에 따라 나머지 가격 규칙을 완료합니다.

1. 완료되면 **[!UICONTROL Save]**&#x200B;을(를) 클릭합니다.
