---
title: 수표 및 금전 주문
description: 스토어에서 오프라인 결제 방법으로 수표와 금전을 설정하는 방법에 대해 알아봅니다.
exl-id: e004f0c3-f659-4b08-a41a-88bfc05acaab
feature: Payments
source-git-commit: 8b5af316ab1d2e632ed5fc2066974326830ab3f7
workflow-type: tm+mt
source-wordcount: '336'
ht-degree: 0%

---

# 수표 및 금전 주문

Adobe Commerce 및 Magento Open Source을 사용하면 수표나 우편환으로 결제를 받을 수 있습니다. 다음 _수표/우편환_ 결제 방법은 기본적으로 스토어에 대해 활성화되어 있습니다. 특정 국가에서만 수표와 금전 주문을 수락할 수 있으며 최소 및 최대 주문 총 한도로 구성을 미세 조정할 수 있습니다.

**_수표 또는 금전 주문으로 지급을 구성하려면_**

1. 다음에서 _관리자_ 사이드바, 이동 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. 왼쪽 패널에서 를 확장합니다. **[!UICONTROL Sales]** 및 선택 **[!UICONTROL Payment Methods]**.

1. 아래 _[!UICONTROL Other Payment Methods]_, 확장 ![확장 선택기](../assets/icon-display-expand.png) 다음&#x200B;**[!UICONTROL Check / Money Order]**섹션.

   ![수표/우편환](../configuration-reference/sales/assets/payment-methods-check-money-order.png){width="600" zoomable="yes"}

   이러한 각 구성 설정에 대한 자세한 설명은 을 참조하십시오. [수표/우편환](../configuration-reference/sales/payment-methods.md#check--money-order) 다음에서 _구성 참조 안내서_.

   >[!NOTE]
   >
   >필요한 경우 먼저 **[!UICONTROL Use system value]** 확인란을 선택하여 이 설정을 변경할 수 있습니다.

1. 수표나 우편환으로 지불을 받으려면 다음을 설정하십시오. **[!UICONTROL Enabled]** 끝 `Yes`.

1. 대상 **[!UICONTROL Title]**&#x200B;을 클릭하고 체크아웃 중에 수표/금전 주문 결제 방법을 식별하는 제목을 입력합니다.

1. 일반적으로 주문이 승인 대기 중인 경우 기본값을 수락합니다. **[!UICONTROL New Order Status]** 다음으로: `Pending"` 승인될 때까지.

   원하는 경우 `Processing` 또는 `Suspected Fraud` 해당 결제 방법을 사용한 신규 주문 상태.

1. 설정 **[!UICONTROL Payment from Applicable Countries]** 다음 중 하나를 수행합니다.

   - `All Allowed Countries` - 모든 고객의 고객 [국가](../getting-started/store-details.md#country-options) 스토어 구성에 지정된 경우 이 결제 방법을 사용할 수 있습니다.
   - `Specific Countries` - 이 옵션을 선택하면 _[!UICONTROL Payment from Specific Countries]_목록이 나타납니다. 여러 국가를 선택하려면 Ctrl 키(PC) 또는 Command 키(Mac)를 누른 채 각 옵션을 클릭합니다.

1. 대상 **[!UICONTROL Make Check Payable To]**&#x200B;수표를 지급할 당사자명을 입력합니다.

1. 대상 **[!UICONTROL Send Check To]**&#x200B;수표가 발송되는 우편 주소 또는 우편 번호를 입력합니다.

1. 설정 **[!UICONTROL Minimum Order Total]** 및 **[!UICONTROL Maximum Order Total]** 이 결제 방법에 해당하는 데 필요한 주문 금액으로 표시합니다.

   >[!NOTE]
   >
   >합계가 최소 또는 최대 합계 값 사이에 속하거나 정확히 일치하는 경우 주문이 적합합니다.

1. 대상 **[!UICONTROL Sort Order]**&#x200B;을 클릭하고 체크아웃 중에 표시되는 결제 방법 목록에 이 항목의 위치를 결정하는 번호를 입력합니다.

   이 번호는 다른 결제 방법과 관련이 있습니다. (`0` = 첫 번째, `1` = 초, `2` = 세 번째 등입니다.)

1. 완료되면 다음을 클릭하십시오. **[!UICONTROL Save Config]**.
