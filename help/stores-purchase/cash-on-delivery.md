---
title: 배달 현금(COD)
description: 매장에서 오프라인 결제 방법으로 배송 시 현금을 설정하는 방법에 대해 알아봅니다.
exl-id: dcf94734-a66e-4d32-b389-b47c979ceaa9
feature: Payments
source-git-commit: 8b5af316ab1d2e632ed5fc2066974326830ab3f7
workflow-type: tm+mt
source-wordcount: '335'
ht-degree: 0%

---

# 배달 현금(COD)

Adobe Commerce 및 Magento Open Source을 사용하면 구매에 대해 _배달 시 현금_(COD) 결제를 받을 수 있습니다. 특정 국가에서만 COD 결제를 수락할 수 있으며 최소 및 최대 주문 총 한도로 구성을 세밀하게 조정할 수 있습니다.

배송 운송업체는 배송 시 고객으로부터 결제 대금을 받고, 이 대금이 귀하에게 이전됩니다. 운송 및 취급 수수료에서 운송 회사 서비스에서 부과하는 모든 수수료를 조정할 수 있습니다.

**_배달 결제 시 현금을 설정하려면:_**

1. _관리자_ 사이드바에서 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**(으)로 이동합니다.

1. 왼쪽 패널에서 **[!UICONTROL Sales]**&#x200B;을(를) 확장하고 **[!UICONTROL Payment Methods]**&#x200B;을(를) 선택합니다.

1. _기타 결제 방법_&#x200B;에서 **[!UICONTROL Cash On Delivery Payment]** 섹션에서 ![확장 선택기](../assets/icon-display-expand.png)를 확장합니다.

   ![배달 결제 현금](../configuration-reference/sales/assets/payment-methods-cash-on-delivery-payment.png){width="600" zoomable="yes"}

   이러한 각 구성 설정에 대한 자세한 설명은 _구성 참조 안내서_&#x200B;에서 [배달 시 현금 결제](../configuration-reference/sales/payment-methods.md#cash-on-delivery-payment)를 참조하십시오.

   >[!NOTE]
   >
   >필요한 경우 먼저 **[!UICONTROL Use system value]** 확인란의 선택을 취소하여 이러한 설정을 변경합니다.

1. 배달 결제 시 현금을 활성화하려면 **[!UICONTROL Enabled]**&#x200B;을(를) `Yes`(으)로 설정하십시오.

1. **[!UICONTROL Title]**&#x200B;의 경우 체크아웃하는 동안 COD 결제 방법을 식별하는 제목을 입력하십시오.

1. 결제 영수증이 확인될 때까지 **[!UICONTROL New Order Status]**&#x200B;을(를) `Pending`(으)로 설정하십시오.

   원하는 경우 이 결제 방법을 사용하여 새 주문에 대해 `Processing` 또는 `Suspected Fraud` 상태를 사용할 수 있습니다.

1. **[!UICONTROL Payment from Applicable Countries]**&#x200B;을(를) 다음 중 하나로 설정합니다.

   - `All Allowed Countries` - 스토어 구성에 지정된 모든 [국가](../getting-started/store-details.md#country-options)의 고객이 이 결제 방법을 사용할 수 있습니다.
   - `Specific Countries` - 이 옵션을 선택하면 _[!UICONTROL Payment from Specific Countries]_&#x200B;목록이 나타납니다. 여러 국가를 선택하려면 Ctrl 키(PC) 또는 Command 키(Mac)를 누른 채 각 옵션을 클릭합니다.

1. COD 주문 배달을 수락하려면 **[!UICONTROL Instructions]**&#x200B;을(를) 입력하십시오.

1. **[!UICONTROL Minimum Order Total]** 및 **[!UICONTROL Maximum Order Total]**&#x200B;을(를) COD 결제에 필요한 주문 금액으로 설정하십시오.

   >[!NOTE]
   >
   >합계가 최소 또는 최대 주문 합계 사이에 있거나 일치하는 경우 주문이 적격 처리됩니다.

1. **[!UICONTROL Sort Order]**&#x200B;의 경우 체크아웃 중에 표시되는 결제 방법 목록에 이 항목의 위치를 결정하는 번호를 입력하십시오.

   이 번호는 다른 결제 방법과 관련이 있습니다. (`0` = 첫 번째, `1` = 두 번째, `2` = 세 번째 등)

1. 완료되면 **[!UICONTROL Save Config]**&#x200B;을(를) 클릭합니다.
