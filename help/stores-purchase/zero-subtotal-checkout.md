---
title: 0 소계 체크아웃
description: 스토어에서 오프라인 결제 방법으로 제로 소계를 설정하는 방법에 대해 알아봅니다.
exl-id: c14ce289-8292-41d9-a448-f493c784f35c
feature: Checkout, Configuration
source-git-commit: 8b5af316ab1d2e632ed5fc2066974326830ab3f7
workflow-type: tm+mt
source-wordcount: '347'
ht-degree: 0%

---

# 0 소계 체크아웃

_소계 체크아웃 제로_&#x200B;는 할인이 적용된 후 과세되는 소계가 0인 주문에 사용할 수 있습니다. 예를 들어 다음과 같은 경우에는 소계 체크아웃 0이 사용될 수 있습니다.

- 할인은 배송에 대한 추가 비용 없이 구매 가격 전체를 포함합니다.

- 고객이 장바구니에 [다운로드 가능](../catalog/product-create-downloadable.md) 또는 [가상](../catalog/product-create-virtual.md) 제품을 추가하며 가격은 0입니다.

- [simple](../catalog/product-create-simple.md) 제품의 가격이 0이며 [무료 배송](shipping-free.md) 방법을 사용할 수 있습니다.

- [쿠폰 코드](../merchandising-promotions/price-rules-cart-coupon.md)는 제품 및 배송의 전체 가격을 포함합니다.

시간을 절약하기 위해 소계 주문 0개를 자동 송장 발행으로 설정할 수 있습니다.

**_소계 체크 아웃을 구성하려면:_**

1. _관리자_ 사이드바에서 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**(으)로 이동합니다.

1. 왼쪽 패널에서 **[!UICONTROL Sales]**&#x200B;을(를) 확장하고 **[!UICONTROL Payment Methods]**&#x200B;을(를) 선택합니다.

1. _[!UICONTROL Other Payment Methods]_에서&#x200B;**[!UICONTROL Zero Subtotal Checkout]**섹션의 ![확장 선택기](../assets/icon-display-expand.png)를 확장합니다.

   ![0 소계 체크아웃](../configuration-reference/sales/assets/payment-methods-zero-subtotal-checkout.png){width="600" zoomable="yes"}

   >[!NOTE]
   >
   >필요한 경우 먼저 **[!UICONTROL Use system value]** 확인란의 선택을 취소하여 이러한 설정을 변경합니다.

1. 소계 체크아웃 0을 활성화하려면 **[!UICONTROL Enabled]**&#x200B;을(를) `Yes`(으)로 설정합니다.

1. **[!UICONTROL Title]**&#x200B;에 대해 체크아웃 중에 제로 소계 메서드를 식별하는 제목을 입력합니다.

1. 일반적으로 주문이 승인 대기 중인 경우 주문이 승인될 때까지 기본 **[!UICONTROL New Order Status]**&#x200B;을(를) `Pending"`(으)로 수락합니다.

   원하는 경우 이 결제 방법을 사용하여 새 주문에 대해 `Processing` 또는 `Suspected Fraud` 상태를 사용할 수 있습니다.

1. 잔액이 0인 모든 항목에 대해 자동으로 송장을 발행하려면 **[!UICONTROL Automatically Invoice All Items]**&#x200B;을(를) `Yes`(으)로 설정하십시오.

   이 옵션은 **[!UICONTROL New Order Status]** 옵션이 `Processing`(으)로 설정된 경우에만 사용할 수 있습니다.

   >[!NOTE]
   >
   >_[!UICONTROL New Order Status]_이(가) `Processing`(으)로 설정되고_[!UICONTROL Automatically Invoice All Items]_&#x200B;이(가) `No`(으)로 설정된 경우 [주문 상태](order-status.md#custom-order-status) 페이지에서 **[!UICONTROL Order State]** = `Pending` 및 **[!UICONTROL Default Status]** = `No` 매핑에 대해 **[!UICONTROL Order Status]** = `Processing`도 할당해야 합니다.

1. **[!UICONTROL Payment from Applicable Countries]**&#x200B;을(를) 다음 중 하나로 설정합니다.

   - `All Allowed Countries` - 스토어 구성에 지정된 모든 [국가](../getting-started/store-details.md#country-options)의 고객이 이 결제 방법을 사용할 수 있습니다.
   - `Specific Countries` - 이 옵션을 선택하면 _[!UICONTROL Payment from Specific Countries]_목록이 나타납니다. 여러 국가를 선택하려면 Ctrl 키(PC) 또는 Command 키(Mac)를 누른 채 각 옵션을 클릭합니다.

1. **[!UICONTROL Sort Order]**&#x200B;의 경우 체크아웃 중에 표시되는 결제 방법 목록에 이 항목의 위치를 결정하는 번호를 입력하십시오.

   이 번호는 다른 결제 방법과 관련이 있습니다. (`0` = 첫 번째, `1` = 두 번째, `2` = 세 번째 등)

1. 완료되면 **[!UICONTROL Save Config]**&#x200B;을(를) 클릭합니다.
