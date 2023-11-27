---
title: 장바구니 가격 규칙 예 - 최소 구매와 함께 할인
description: 최소 구매로 할인을 제공하기 위해 장바구니 가격 규칙을 사용하는 예를 검토하십시오.
exl-id: dc06cd12-d23b-4836-9ad2-93ca60dac927
feature: Merchandising, Price Rules, Shopping Cart
source-git-commit: eb0fe395020dbe2e2496aba13d2f5c2bf2d0fc27
workflow-type: tm+mt
source-wordcount: '337'
ht-degree: 0%

---

# 장바구니 가격 규칙 예 - 최소 구매와 함께 할인

장바구니 가격 규칙을 사용하여 최소 구매를 기준으로 퍼센트 할인을 제공할 수 있습니다. 다음 예에서는 특정 범주의 $200.00 이상 모든 구매에 25% 할인이 적용됩니다. 할인 형식은 다음과 같습니다.

X% 모든 Y (범주) / $Z 달러

## 1단계. 장바구니 규칙 만들기

기본 사항 따르기 [지침](price-rules-cart.md) 장바구니 규칙을 만듭니다.

## 2단계. 조건 정의

1. 아래로 스크롤하고 확장합니다. ![확장 선택기](../assets/icon-display-expand.png) 다음 **[!UICONTROL Conditions]** 섹션.

1. 클릭 _추가_ (![추가 아이콘](../assets/icon-add-green-circle.png)) 및 선택 **[!UICONTROL Product Attribute Combination]**.

   ![장바구니 가격 규칙 조건 - 제품 속성 조합](./assets/condition1.png){width="500" zoomable="yes"}

1. 클릭 _추가_ (![추가 아이콘](../assets/icon-add-green-circle.png))를 클릭하여 제품에서 사용할 수 있습니다 **[!UICONTROL Product Attribute]**, 선택 **[!UICONTROL Category]**.

   - (**...**) _기타_ 추가 옵션을 표시하기 위한 링크.

     ![장바구니 가격 규칙 조건 - 범주 옵션](./assets/condition3.png){width="600" zoomable="yes"}

   - 다음을 클릭합니다. _선택기_ (![목록 아이콘](../assets/icon-list-chooser.png)) 아이콘을 클릭하여 사용 가능한 범주를 확인합니다. 카테고리 트리에서 포함할 각 카테고리의 확인란을 선택합니다. 확인 아이콘을 클릭하여 범주 선택 사항을 적용합니다.

     ![장바구니 가격 규칙 조건 - 범주](./assets/condition4.png){width="600" zoomable="yes"}

1. 클릭 _추가_ (![추가 아이콘](../assets/icon-add-green-circle.png))를 클릭하여 다음 줄의 맨 앞에 놓고 다음을 수행합니다.

   - 아래 목록에서 **[!UICONTROL Cart Item Attribute]**, 선택 **[!UICONTROL Price in cart]**.

     ![장바구니 가격 규칙 조건 - 장바구니 항목 속성](./assets/condition5.png){width="500"}

   - 클릭 **은(는)** 및 선택 `equals or greater than`.

   - 클릭 **...** 조건을 충족하기 위해 장바구니에 가격이 있어야 하는 금액을 입력합니다. 예를 들어, 을 입력합니다. `30`.

     ![장바구니 가격 규칙 조건 - 장바구니 내 가격](./assets/condition6.png){width="500"}

1. 클릭 **[!UICONTROL Save and Continue Edit]**.

## 3단계. 작업 정의

1. 확장 ![확장 선택기](../assets/icon-display-expand.png) 다음 **[!UICONTROL Actions]** 섹션을 참조하고 다음을 수행합니다.

   ![장바구니 가격 규칙 작업](./assets/minimum-discount-actions.png){width="600" zoomable="yes"}

   - 설정 **[!UICONTROL Apply]** 끝 `Percent of product price discount`.

   - 다음을 입력합니다. **[!UICONTROL Discount Amount]**. 예를 들어, 을 입력합니다. `10` 10퍼센트 할인해 주세요.

   - 구매에 추가 판촉 행사가 적용되지 않도록 하려면 을 설정합니다. **[!UICONTROL Discard subsequent rules]** 끝 `Yes`.

1. 클릭 **[!UICONTROL Save and Continue Edit]** 필요한 경우 규칙을 완료합니다.

## 4단계. 레이블 작성

완료 [4단계](price-rules-cart.md) 체크아웃하는 동안 표시되는 모든 레이블을 입력하는 장바구니 가격 규칙 지침

## 5단계: 규칙 저장 및 테스트

{{new-price-rule}}

1. 규칙이 완료되면 다음을 클릭하십시오. **[!UICONTROL Save Rule]**.

1. 규칙이 올바르게 작동하는지 테스트합니다.
