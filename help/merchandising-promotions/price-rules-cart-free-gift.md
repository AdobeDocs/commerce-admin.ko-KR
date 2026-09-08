---
title: 무료 선물 프로모션
description: 조건 세트가 충족될 때 사은품을 제공하기 위해 장바구니 가격 규칙으로 사은품 프로모션을 구성하는 방법에 대해 알아봅니다.
feature: Merchandising, Price Rules, Shopping Cart, Shipping/Delivery
TQID: https://experienceleague.adobe.com/FR-q4Qj-ZDDzmfEKSvSj-BlwsM7ro-BqAE1yCppTaXE
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2:
  - id: c1256247-af4b-46d8-9dca-0c654ecfa157
  - id: dac87252-6066-4d6e-a9d2-f6d84c323de7
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: f8a45b24-4be7-4f1b-909b-60d06b483a20
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2:
  - id: b5520579-b31f-4df7-9281-f0d9f91e2edc
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: 3cddc90c619a27b1404e0be7bb4b2c9a3b77e443
workflow-type: tm+mt
source-wordcount: 349
ht-degree: 0%

---


# 무료 선물 프로모션

*무료 선물* 프로모션을 통해 특정 조건에서 무료 항목을 장바구니에 추가하는 [장바구니 가격 규칙](price-rules-cart.md)을 설정할 수 있습니다.

>[!NOTE]
>
>이 기능은 Luma 상점 전면에서 지원되지 않습니다. [GraphQL](https://developer.adobe.com/commerce/webapi/graphql/schema/cart/mutations/select-free-gift/)를 통해 액세스할 수 있으며 Edge Delivery Services(EDS) 상점 전면에서 사용할 수 있습니다.

## 무료 선물 프로모션 만들기

이 섹션에서는 다음 형식을 사용하여 무료 선물 프로모션을 만드는 방법에 대해 설명합니다.

**X개 제품 구입, Y개 제품 무료 구입**

1. 무료 선물 프로모션으로 [장바구니 가격 규칙을 만듭니다](price-rules-cart.md#step-1-add-a-rule).

1. 가격 규칙에 대한 조건을 정의하는 장바구니 지침의 [조건을 설명](price-rules-cart.md#step-2-describe-the-conditions)합니다. 이는 규칙에 추가할 수 있는 여러 조건 중 첫 번째이며, 규칙이 트리거되는 시기를 결정합니다. 이는 다음 항목을 조합하여 기반으로 할 수 있습니다.

   - 제품 속성
   - 제품
   - 장바구니 속성
   - Adobe Commerce 고객 세그먼트

   비워 두면 모든 장바구니에 대해 규칙이 트리거됩니다.

   ![장바구니 가격 규칙 - 조건](./assets/conditions.png){width="600" zoomable="yes"}

1. 장바구니 가격 규칙에 대한 조치를 정의합니다.

   1. **[!UICONTROL Actions]** 섹션을 (../assets/icon-display-expand.png)으로 확장하고 다음 정보를 입력합니다.

   - **[!UICONTROL Apply]**&#x200B;을(를) `Free Gift`(으)로 설정합니다.
   - **[!UICONTROL Gift SKU(s)]**&#x200B;에서 고객이 사은품으로 선택할 수 있는 SKU를 하나 이상 선택합니다.
   - **[!UICONTROL Free Gift Discount Type]**&#x200B;을(를) **[!UICONTROL Price Based]** 또는 **[!UICONTROL Discount Based]**(으)로 설정합니다.
   - **[!UICONTROL Gift Qty]**&#x200B;에서 고객이 받는 사은품의 수량을 입력합니다. 예를 들어 고객에게 2개의 무료 항목을 제공하려면 `2`을(를) 입력합니다.
   - 다른 할인이 적용되지 않도록 하려면 **[!UICONTROL Discard subsequent rules]**&#x200B;을(를) `Yes`(으)로 설정하십시오.

   1. **[!UICONTROL Save and Continue Edit]**&#x200B;을(를) 클릭하고 필요에 따라 나머지 규칙을 완료합니다.

1. [장바구니 가격 규칙 지침의 레이블을 작성](price-rules-cart.md)하여 체크아웃 중에 나타나는 레이블을 입력합니다.

![장바구니 가격 규칙 - 무료 선물 레이블](./assets/free-gift-promotion-label.png){width="600" zoomable="yes"}

{{new-price-rule}}

1. 규칙이 완료되면 **[!UICONTROL Save Rule]**&#x200B;을(를) 클릭합니다.

## 변형

다양한 방법으로 장바구니 가격 규칙을 사용자 지정할 수 있습니다. 무료 선물 기능은 두 가지 할인 유형으로 구성할 수 있습니다.

- **가격 기반** : 선물 라인 항목이 `0` 가격으로 추가됩니다.
- **할인 기반** : 선물 라인 항목에 전체 할인이 적용됩니다.
