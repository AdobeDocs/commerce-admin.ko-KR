---
title: 은행 송금
description: 스토어에서 오프라인 결제 방법으로 은행 송금을 설정하는 방법에 대해 알아봅니다.
exl-id: 34b2163c-2edd-4741-b002-3d8fb561fc78
feature: Payments
source-git-commit: 8b5af316ab1d2e632ed5fc2066974326830ab3f7
workflow-type: tm+mt
source-wordcount: '275'
ht-degree: 0%

---

# 은행 송금

Adobe Commerce 및 Magento Open Source을 사용하면 고객 은행 계좌에서 이체되어 머천트 은행 계좌로 입금되는 결제를 수락할 수 있습니다.

**_은행 이체 지급을 구성하려면_**

1. 다음에서 _관리자_ 사이드바, 이동 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. 왼쪽 패널에서 를 확장합니다. **[!UICONTROL Sales]** 및 선택 **[!UICONTROL Payment Methods]**.

1. 아래 _기타 결제 방법_, 확장 ![확장 선택기](../assets/icon-display-expand.png) 다음 **[!UICONTROL Bank Transfer Payment]** 섹션.

   ![은행 송금 결제](../configuration-reference/sales/assets/payment-methods-bank-transfer-payment.png){width="600" zoomable="yes"}

   >[!NOTE]
   >
   >필요한 경우 먼저 **[!UICONTROL Use system value]** 확인란을 선택하여 이 설정을 변경할 수 있습니다.

1. 은행 이체를 활성화하려면 다음을 설정합니다. **[!UICONTROL Enabled]** 끝 `Yes`.

1. 대상 **[!UICONTROL Title]**&#x200B;을 누르고 체크아웃 중 은행 이체 결제 방법을 식별하는 제목을 입력합니다.

1. 설정 **[!UICONTROL New Order Status]** 끝 `Pending` 결제가 승인될 때까지

1. 설정 **[!UICONTROL Payment from Applicable Countries]** 다음 중 하나를 수행합니다.

   - `All Allowed Countries` - 모든 고객의 고객 [국가](../getting-started/store-details.md#country-options) 스토어 구성에 지정된 경우 이 결제 방법을 사용할 수 있습니다.

   - `Specific Countries` - 이 옵션을 선택하면 _[!UICONTROL Payment from Specific Countries]_목록이 나타납니다. 여러 국가를 선택하려면 Ctrl 키(PC) 또는 Command 키(Mac)를 누른 채 각 옵션을 클릭합니다.

1. 다음을 입력합니다. **[!UICONTROL Instructions]** 고객이 은행 이체를 설정할 때 따라야 합니다.

   은행이 위치한 국가와 은행의 요구 사항에 따라 다음 정보를 포함할 수 있습니다.

   - 은행 계좌 이름
   - 은행 계좌 번호
   - 은행 라우팅 코드
   - 은행명
   - 은행 주소

1. 설정 **[!UICONTROL Minimum Order Total]** 및 **[!UICONTROL Maximum Order Total]** 이 결제 방법을 사용할 자격이 있는 데 필요한 금액.

   >[!NOTE]
   >
   >합계가 최소 또는 최대 합계 값 사이에 속하거나 정확히 일치하는 경우 주문이 적합합니다.

1. 대상 **[!UICONTROL Sort Order]**&#x200B;을 클릭하고 체크아웃 중에 표시되는 결제 방법 목록에 이 항목의 위치를 결정하는 번호를 입력합니다.

   이 번호는 다른 결제 방법과 관련이 있습니다. (`0` = 첫 번째, `1` = 초, `2` = 세 번째 등입니다.)

1. 완료되면 다음을 클릭하십시오. **[!UICONTROL Save Config]**.
