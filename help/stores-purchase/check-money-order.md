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

Adobe Commerce 및 Magento Open Source을 사용하면 수표나 우편환으로 결제를 받을 수 있습니다. 기본적으로 스토어에 대해 _수표/주문_ 결제 방법을 사용할 수 있습니다. 특정 국가에서만 수표와 금전 주문을 수락할 수 있으며 최소 및 최대 주문 총 한도로 구성을 미세 조정할 수 있습니다.

**_수표 또는 금전 주문으로 결제를 구성하려면:_**

1. _관리자_ 사이드바에서 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**(으)로 이동합니다.

1. 왼쪽 패널에서 **[!UICONTROL Sales]**&#x200B;을(를) 확장하고 **[!UICONTROL Payment Methods]**&#x200B;을(를) 선택합니다.

1. _[!UICONTROL Other Payment Methods]_&#x200B;에서&#x200B;**[!UICONTROL Check / Money Order]**&#x200B;섹션의 ![확장 선택기](../assets/icon-display-expand.png)를 확장합니다.

   ![주문 확인/금액](../configuration-reference/sales/assets/payment-methods-check-money-order.png){width="600" zoomable="yes"}

   이러한 각 구성 설정에 대한 자세한 설명은 _구성 참조 안내서_&#x200B;에서 [주문 확인/금액](../configuration-reference/sales/payment-methods.md#check--money-order)을 참조하세요.

   >[!NOTE]
   >
   >필요한 경우 먼저 **[!UICONTROL Use system value]** 확인란의 선택을 취소하여 이러한 설정을 변경합니다.

1. 수표나 우편환으로 결제하려면 **[!UICONTROL Enabled]**&#x200B;을(를) `Yes`(으)로 설정하십시오.

1. **[!UICONTROL Title]**&#x200B;의 경우 체크아웃 중 수표/주문 결제 방법을 식별하는 제목을 입력합니다.

1. 일반적으로 주문이 승인 대기 중인 경우 승인될 때까지 기본 **[!UICONTROL New Order Status]**&#x200B;을(를) `Pending"`(으)로 수락합니다.

   원하는 경우 이 결제 방법을 사용하여 새 주문에 대해 `Processing` 또는 `Suspected Fraud` 상태를 사용할 수 있습니다.

1. **[!UICONTROL Payment from Applicable Countries]**&#x200B;을(를) 다음 중 하나로 설정합니다.

   - `All Allowed Countries` - 스토어 구성에 지정된 모든 [국가](../getting-started/store-details.md#country-options)의 고객이 이 결제 방법을 사용할 수 있습니다.
   - `Specific Countries` - 이 옵션을 선택하면 _[!UICONTROL Payment from Specific Countries]_&#x200B;목록이 나타납니다. 여러 국가를 선택하려면 Ctrl 키(PC) 또는 Command 키(Mac)를 누른 채 각 옵션을 클릭합니다.

1. **[!UICONTROL Make Check Payable To]**&#x200B;의 경우 수표를 결제해야 하는 당사자의 이름을 입력하십시오.

1. **[!UICONTROL Send Check To]**&#x200B;의 경우 수표를 우편으로 보낼 주소 또는 사서함 주소를 입력하십시오.

1. 이 결제 방법을 사용하는 데 필요한 주문 금액으로 **[!UICONTROL Minimum Order Total]** 및 **[!UICONTROL Maximum Order Total]**&#x200B;을(를) 설정합니다.

   >[!NOTE]
   >
   >합계가 최소 또는 최대 합계 값 사이에 속하거나 정확히 일치하는 경우 주문이 적합합니다.

1. **[!UICONTROL Sort Order]**&#x200B;의 경우 체크아웃 중에 표시되는 결제 방법 목록에 이 항목의 위치를 결정하는 번호를 입력하십시오.

   이 번호는 다른 결제 방법과 관련이 있습니다. (`0` = 첫 번째, `1` = 두 번째, `2` = 세 번째 등)

1. 완료되면 **[!UICONTROL Save Config]**&#x200B;을(를) 클릭합니다.
