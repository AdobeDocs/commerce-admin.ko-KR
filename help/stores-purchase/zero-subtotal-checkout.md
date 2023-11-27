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

_0 소계 체크아웃_ 할인이 적용된 후 과세되는 소계가 0인 주문에 사용할 수 있습니다. 예를 들어 다음과 같은 경우에는 소계 체크아웃 0이 사용될 수 있습니다.

- 할인은 배송에 대한 추가 비용 없이 구매 가격 전체를 포함합니다.

- 고객이 추가 [다운로드 가능해](../catalog/product-create-downloadable.md) 또는 [가상](../catalog/product-create-virtual.md) 장바구니에 제품이 추가되었으며 가격은 0입니다.

- a 가격 [단순](../catalog/product-create-simple.md) product는 0이고 [무료 배송](shipping-free.md) 메서드를 사용할 수 있습니다.

- A [쿠폰 코드](../merchandising-promotions/price-rules-cart-coupon.md) 제품 및 배송의 전체 가격을 포함합니다.

시간을 절약하기 위해 소계 주문 0개를 자동 송장 발행으로 설정할 수 있습니다.

**_소계 체크아웃 0을 구성하려면 다음을 수행합니다._**

1. 다음에서 _관리자_ 사이드바, 이동 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. 왼쪽 패널에서 를 확장합니다. **[!UICONTROL Sales]** 및 선택 **[!UICONTROL Payment Methods]**.

1. 아래 _[!UICONTROL Other Payment Methods]_, 확장 ![확장 선택기](../assets/icon-display-expand.png) 다음&#x200B;**[!UICONTROL Zero Subtotal Checkout]**섹션.

   ![제로 소계 체크아웃](../configuration-reference/sales/assets/payment-methods-zero-subtotal-checkout.png){width="600" zoomable="yes"}

   >[!NOTE]
   >
   >필요한 경우 먼저 **[!UICONTROL Use system value]** 확인란을 선택하여 이 설정을 변경할 수 있습니다.

1. 소계 체크아웃 0을 활성화하려면 다음을 설정합니다. **[!UICONTROL Enabled]** 끝 `Yes`.

1. 대상 **[!UICONTROL Title]**&#x200B;체크아웃하는 동안 제로 소계 메소드를 식별하는 제목을 입력합니다.

1. 일반적으로 주문이 승인 대기 중인 경우 기본값을 수락합니다. **[!UICONTROL New Order Status]** 다음으로: `Pending"` 주문이 승인될 때까지.

   원하는 경우 `Processing` 또는 `Suspected Fraud` 해당 결제 방법을 사용한 신규 주문 상태.

1. 설정 **[!UICONTROL Automatically Invoice All Items]** 끝 `Yes` 잔액이 0인 모든 품목에 대해 자동으로 송장을 발행하려면

   이 옵션은 다음 경우에만 사용할 수 있습니다. **[!UICONTROL New Order Status]** 옵션이 로 설정되어 있습니다. `Processing`.

   >[!NOTE]
   >
   >If _[!UICONTROL New Order Status]_이(가) (으)로 설정됨 `Processing` 및_[!UICONTROL Automatically Invoice All Items]_ 이(가) (으)로 설정됨 `No`, 또한 다음을 할당해야 합니다. **[!UICONTROL Order Status]** = `Processing` 대상: **[!UICONTROL Order State]** = `Pending` 및 **[!UICONTROL Default Status]** = `No` 다음에 대한 매핑 [주문 상태](order-status.md#custom-order-status) 페이지를 가리키도록 업데이트하는 중입니다.

1. 설정 **[!UICONTROL Payment from Applicable Countries]** 다음 중 하나를 수행합니다.

   - `All Allowed Countries` - 모든 고객의 고객 [국가](../getting-started/store-details.md#country-options) 스토어 구성에 지정된 경우 이 결제 방법을 사용할 수 있습니다.
   - `Specific Countries` - 이 옵션을 선택하면 _[!UICONTROL Payment from Specific Countries]_목록이 나타납니다. 여러 국가를 선택하려면 Ctrl 키(PC) 또는 Command 키(Mac)를 누른 채 각 옵션을 클릭합니다.

1. 대상 **[!UICONTROL Sort Order]**&#x200B;을 클릭하고 체크아웃 중에 표시되는 결제 방법 목록에 이 항목의 위치를 결정하는 번호를 입력합니다.

   이 번호는 다른 결제 방법과 관련이 있습니다. (`0` = 첫 번째, `1` = 초, `2` = 세 번째 등입니다.)

1. 완료되면 다음을 클릭하십시오. **[!UICONTROL Save Config]**.
