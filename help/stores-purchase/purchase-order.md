---
title: 구매 주문
description: 스토어에서 오프라인 결제 방법으로 구매 발주를 설정하는 방법에 대해 알아봅니다.
exl-id: 493c1b59-2155-449f-a08a-eb1aa2af9b3e
feature: Purchase Orders
source-git-commit: 8b5af316ab1d2e632ed5fc2066974326830ab3f7
workflow-type: tm+mt
source-wordcount: '296'
ht-degree: 0%

---

# 구매 주문

A _구매 주문_ PO(상업용 고객)는 PO 번호를 참조하여 승인된 구매에 대해 지불할 수 있습니다. 발주서는 구매 기업이 미리 승인하고 발급하는 방식이다. 체크아웃 시 고객은 결제 방법으로 구매 발주를 선택합니다. 청구서를 접수하면, 회사는 AP 시스템에서 지급을 처리하고 구매에 대해 지불합니다.

구매 발주에 의한 지불을 수락하기 전에 항상 상업 고객의 신용도를 설정하십시오.

**_구매 발주별 지급을 구성하려면_**

1. 다음에서 _관리자_ 사이드바, 이동 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. 왼쪽 패널에서 를 확장합니다. **[!UICONTROL Sales]** 및 선택 **[!UICONTROL Payment Methods]**.

1. 아래 _[!UICONTROL Other Payment Methods]_, 확장 ![확장 선택기](../assets/icon-display-expand.png) 다음&#x200B;**[!UICONTROL Purchase Order]**섹션.

   ![구매 주문](../configuration-reference/sales/assets/payment-methods-purchase-order.png){width="600" zoomable="yes"}

   이러한 각 구성 설정에 대한 자세한 설명은 을 참조하십시오. [구매 주문](../configuration-reference/sales/payment-methods.md#purchase-order) 다음에서 _구성 참조 안내서_.

   >[!NOTE]
   >
   >필요한 경우 먼저 **[!UICONTROL Use system value]** 확인란을 선택하여 이 설정을 변경할 수 있습니다.

1. 이 결제 방법을 활성화하려면 다음을 설정하십시오. **[!UICONTROL Enabled]** 끝 `Yes`.

1. 대상 **[!UICONTROL Title]**&#x200B;을 클릭하고 체크아웃 중에 이 결제 방법을 식별하는 제목을 입력합니다.

1. 설정 **[!UICONTROL New Order Status]** 끝 `Pending` 결제가 승인될 때까지

1. 설정 **[!UICONTROL Payment from Applicable Countries]** 다음 중 하나를 수행합니다.

   - `All Allowed Countries` - 모든 고객의 고객 [국가](../getting-started/store-details.md#country-options) 스토어 구성에 지정된 경우 이 결제 방법을 사용할 수 있습니다.
   - `Specific Countries` - 이 옵션을 선택하면 _[!UICONTROL Payment from Specific Countries]_목록이 나타납니다. 여러 국가를 선택하려면 Ctrl 키(PC) 또는 Command 키(Mac)를 누른 채 각 옵션을 클릭합니다.

1. 설정 **[!UICONTROL Minimum Order Total]** 및 **[!UICONTROL Maximum Order Total]** 이 결제 방법에 해당하는 데 필요한 금액.

   >[!NOTE]
   >
   >합계가 최소 또는 최대 합계 값 사이에 속하거나 정확히 일치하는 경우 주문이 적합합니다.

1. 대상 **[!UICONTROL Sort Order]**&#x200B;을 클릭하고 체크아웃 중에 표시되는 결제 방법 목록에 이 항목의 위치를 결정하는 번호를 입력합니다.

   이 번호는 다른 결제 방법과 관련이 있습니다. (`0` = 첫 번째, `1` = 초, `2` = 세 번째 등입니다.)

1. 완료되면 다음을 클릭하십시오. **[!UICONTROL Save Config]**.
