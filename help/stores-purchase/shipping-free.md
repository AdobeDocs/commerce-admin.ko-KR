---
title: 무료 배송
description: 스토어에 대한 무료 배송 옵션을 설정하는 방법에 대해 알아보십시오.
exl-id: 3ce69583-0f7f-4c23-b3e3-7d2502bc1bca
feature: Shipping/Delivery
source-git-commit: 8b5af316ab1d2e632ed5fc2066974326830ab3f7
workflow-type: tm+mt
source-wordcount: '395'
ht-degree: 0%

---

# 무료 배송

_무료 배송_&#x200B;은(는) 제공할 수 있는 가장 효과적인 프로모션 중 하나입니다. 최소 구매를 기준으로 하거나 조건 집합이 충족될 때 적용되는 [장바구니 가격 규칙](../merchandising-promotions/price-rules-cart.md)(으)로 설정할 수 있습니다. 둘 다 동일한 주문에 적용되는 경우 구성 설정이 장바구니 규칙보다 우선합니다.

>[!NOTE]
>
>무료 배송에 필요할 수 있는 추가 설정에 대해서는 배송 회사 구성을 확인하십시오.

## 1단계: 무료 배송 구성

1. _관리자_ 사이드바에서 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**(으)로 이동합니다.

1. 왼쪽 패널에서 **[!UICONTROL Sales]**&#x200B;을(를) 확장하고 **[!UICONTROL Delivery Methods]**&#x200B;을(를) 선택합니다.

1. **[!UICONTROL Free Shipping]** 섹션에서 ![확장 선택기](../assets/icon-display-expand.png)를 확장합니다.

   >[!NOTE]
   >
   >필요한 경우 먼저 **[!UICONTROL Use system value]** 확인란의 선택을 해제하여 설명된 대로 다음 설정을 변경합니다.

1. **[!UICONTROL Enabled]**&#x200B;을(를) `Yes`(으)로 설정합니다.

1. **[!UICONTROL Title]**&#x200B;의 경우 체크아웃 중에 무료 배송 방법을 식별하는 제목을 입력하고 이를 설명하는 **[!UICONTROL Method Name]**&#x200B;을(를) 입력하십시오.

1. **[!UICONTROL Minimum Order Amount]**&#x200B;에 대해 무료 배송에 적합한 최소 합계 값을 입력하십시오.

   >[!TIP]
   >
   >[테이블 속도](shipping-table-rate.md)와(과) 함께 무료 배송을 사용하려면 _[!UICONTROL Minimum Order Amount]_&#x200B;을(를) 충족되지 않도록 높게 만드십시오. 이 높은 값을 사용하면 가격 규칙에 의해 트리거되지 않는 한 무료 배송이 적용되지 않습니다.

1. **[!UICONTROL Include Tax to Amount]** 설정:

   - `Yes` - 최소 주문 금액 계산 시 세금을 포함합니다(소계 + 세금 - 할인).
   - `No` - 최소 주문 금액(소계 - 할인)을 계산할 때 세금을 포함하지 않습니다.

   ![무료 배송](../configuration-reference/sales/assets/delivery-methods-free-shipping.png){width="600" zoomable="yes"}

1. **[!UICONTROL Displayed Error Message]**&#x200B;의 경우 무료 배송이 불가능한 경우 표시할 메시지를 입력하십시오.

1. **[!UICONTROL Ship to Applicable Countries]** 설정:

   - `All Allowed Countries` - 스토어 구성에 지정된 모든 [국가](../getting-started/store-details.md#country-options)의 고객은 무료 배송을 사용할 수 있습니다.

   - `Specific Countries` - 이 값을 선택하면 _[!UICONTROL Ship to Specific Countries]_&#x200B;목록이 나타납니다. 목록에서 무료 배송을 사용할 수 있는 각 국가를 선택합니다.

1. **[!UICONTROL Show Method if Not Applicable]** 설정:

   - `Yes` - 해당되지 않는 경우에도 항상 무료 배송 방법을 표시합니다.
   - `No` - 해당하는 경우에만 무료 배송 방법을 표시합니다.

1. **[!UICONTROL Sort Order]**&#x200B;의 경우 체크아웃 중에 배달 방법 목록에 무료 배송의 위치를 결정하는 번호를 입력하십시오.

   `0` = 첫 번째, `1` = 두 번째, `2` = 세 번째 등입니다.

1. **[!UICONTROL Save Config]**&#x200B;을(를) 클릭합니다.

## 2단계: 운송업체 구성에서 무료 배송 활성화

무료 배송에 사용할 각 운송업체에 필요한 구성을 완료해야 합니다. 예를 들어 [UPS 구성](ups.md)이 완료되지 않은 경우 다음 설정을 업데이트하여 무료 배송을 활성화하고 구성하십시오.

1. _[!UICONTROL Delivery Methods]_&#x200B;구성에서&#x200B;**[!UICONTROL UPS]**&#x200B;섹션에서 ![확장 선택기](../assets/icon-display-expand.png)를 확장합니다.

1. **[!UICONTROL Free Method]**&#x200B;을(를) `UPS Ground` 또는 무료 배송을 위해 지정할 다른 형식으로 설정하십시오.

1. 무료 배송을 위해 최소 주문을 요구하려면 **[!UICONTROL Enable Free Shipping Threshold]**&#x200B;을(를) `Enable`(으)로 설정하십시오.

   최소 주문을 사용하려면 **[!UICONTROL Free Shipping Amount Threshold]**&#x200B;에 필요한 금액을 입력하십시오.

1. **[!UICONTROL Save Config]**&#x200B;을(를) 클릭합니다.
