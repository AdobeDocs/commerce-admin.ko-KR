---
title: 가격 표시 설정
description: 고객 구매 경험을 지원하는 카탈로그, 장바구니, 주문, 송장 및 대변 메모의 세금 표시에 대해 알아봅니다.
exl-id: 6f97c474-ef6e-4ca6-899d-812c58b993ca
feature: Checkout, Invoices, Taxes
source-git-commit: 8b5af316ab1d2e632ed5fc2066974326830ab3f7
workflow-type: tm+mt
source-wordcount: '516'
ht-degree: 0%

---

# 가격 표시 설정

가격 표시 설정은 제품 및 배송 가격에 세금이 포함되는지 또는 제외되는지 여부를 결정하거나 두 가지 버전의 가격을 표시합니다(하나는 세금이 포함됨).

제품 가격에 세금이 포함된 경우, 세금 출처와 일치하는 세금 규칙이 있거나 고객 주소가 세금 규칙과 일치하는 경우에만 세금이 표시됩니다. 일치 항목을 트리거할 수 있는 이벤트에는 고객이 계정을 만들거나, 로그인하거나, 장바구니에서 세금 및 배송 예상 항목을 생성할 때 포함됩니다.

>[!IMPORTANT]
>
>세금을 포함하고 제외하는 가격을 표시하는 것은 고객에게 혼란을 줄 수 있다. 경고 메시지가 트리거되지 않도록 하려면 [지침](international-tax-guidelines.md) 해당 국가 및 [권장 설정](taxes.md#warning-messages) 경고 메시지를 방지합니다.

![가격 표시 설정](../configuration-reference/sales/assets/tax-price-display-settings.png){width="600" zoomable="yes"}

이러한 각 구성 설정에 대한 자세한 설명은 을 참조하십시오. [가격 표시 설정](../configuration-reference/sales/tax.md#price-display-settings) 다음에서 _구성 참조 안내서_.

## 가격 표시 설정 구성

세금, 세율 및 분류에 대한 계산 구성이 완료되면 해당 설정에 따라 세금이 계산됩니다. 그러나 카탈로그, 장바구니, 주문, 송장 및 대변 메모의 세금 표시도 상점 내 고객 경험을 지원하도록 구성해야 합니다.

고객이 주문을 하기 전에 이러한 계산이 어떻게 적용되는지 알 수 있도록 연결된 세금(세금 포함 또는 세금 포함 및 세금 제외 둘 다)과 함께 가격을 표시하는 것이 좋습니다.

### 1단계: 카탈로그 가격 표시 설정 구성

1. 다음에서 _관리자_ 사이드바, 이동 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. 왼쪽 패널에서 를 확장합니다. **[!UICONTROL Sales]** 및 선택 **[!UICONTROL Tax]**.

1. 확장 ![확장 선택기](../assets/icon-display-expand.png) 다음 **[!UICONTROL Price Display Settings]** 섹션.

1. 대상 **[!UICONTROL Display Product Prices in Catalog]**, 다음 중 하나를 선택합니다.

   - `Excluding Tax`
   - `Including Tax`
   - `Including and Excluding Tax`

   >[!NOTE]
   >
   >이 옵션을 로 설정하면 `Including Tax`(으)로, 세금 출처와 일치하는 세금 규칙이 있거나 세금 규칙과 일치하는 고객 주소가 있는 경우에만 세금이 표시됩니다. 일치를 트리거할 수 있는 이벤트에는 고객 계정 생성, 로그인 또는 장바구니에서 세금 및 배송 예상 도구의 사용이 포함됩니다.

1. 대상 **[!UICONTROL Display Shipping Prices]**, 다음 중 하나를 선택합니다.

   - `Excluding Tax`
   - `Including Tax`
   - `Including and Excluding Tax`

가격(세금 포함 및 미포함)을 모두 표시하도록 선택하면 상점 전면은 다음과 비슷합니다.

![상점 첫 화면의 세금을 포함한 가격 표시의 예](./assets/catalog-prices-tax.png){width="700" zoomable="yes"}

### 2단계: 장바구니 표시 설정 구성

1. 확장 ![확장 선택기](../assets/icon-display-expand.png) 다음 **[!UICONTROL Shopping Cart Display Settings]** 섹션.

   ![장바구니 표시 설정](../configuration-reference/sales/assets/tax-shopping-cart-display-settings.png){width="600" zoomable="yes"}

1. 대상 **[!UICONTROL Display Prices]**, 다음 중 하나를 선택합니다.

   - `Excluding Tax`
   - `Including Tax`
   - `Including and Excluding Tax`

1. 대상 **[!UICONTROL Display Subtotal]**, 다음 중 하나를 선택합니다.

   - `Excluding Tax`
   - `Including Tax`
   - `Including and Excluding Tax`

1. 대상 **[!UICONTROL Display Shipping Amount]**, 다음 중 하나를 선택합니다.

   - `Excluding Tax`
   - `Including Tax`
   - `Including and Excluding Tax`

1. ![Adobe Commerce](../assets/adobe-logo.svg) (Adobe Commerce 전용) **[!UICONTROL Display Gift Wrapping Prices]**, 다음 중 하나를 선택합니다.

   - `Excluding Tax`
   - `Including Tax`
   - `Including and Excluding Tax`

1. ![Adobe Commerce](../assets/adobe-logo.svg) (Adobe Commerce 전용) **[!UICONTROL Display Printed Card Prices]**, 다음 중 하나를 선택합니다.

   - `Excluding Tax`
   - `Including Tax`
   - `Including and Excluding Tax`

1. 이러한 나머지 각 옵션에 대해 다음으로 전환 `Yes` 또는 `No` 기본 설정에 따라

   - **[!UICONTROL Include Tax in Order Total]**
   - **[!UICONTROL Display Full Tax Summary]**
   - **[!UICONTROL Display Zero Tax Subtotal]**

### 3단계: 주문, 송장 및 대변 메모 표시 설정 구성

1. 확장 ![확장 선택기](../assets/icon-display-expand.png) 다음 **[!UICONTROL Orders, Invoices, Credit Memos Display Settings]** 섹션.

   ![주문, 송장, 대변 메모 표시 설정](../configuration-reference/sales/assets/tax-orders-invoices-credit-memos-display-settings.png){width="600" zoomable="yes"}

1. 대상 **[!UICONTROL Display Prices]**, 다음 중 하나를 선택합니다.

   - `Excluding Tax`
   - `Including Tax`
   - `Including and Excluding Tax`

1. 대상 **[!UICONTROL Display Subtotal]**, 다음 중 하나를 선택합니다.

   - `Excluding Tax`
   - `Including Tax`
   - `Including and Excluding Tax`

1. 대상 **[!UICONTROL Display Shipping Amount]**, 다음 중 하나를 선택합니다.

   - `Excluding Tax`
   - `Including Tax`
   - `Including and Excluding Tax`

1. ![Adobe Commerce](../assets/adobe-logo.svg) (Adobe Commerce 전용) **[!UICONTROL Display Gift Wrapping Prices]**, 다음 중 하나를 선택합니다.

   - `Excluding Tax`
   - `Including Tax`
   - `Including and Excluding Tax`

1. ![Adobe Commerce](../assets/adobe-logo.svg) (Adobe Commerce 전용) **[!UICONTROL Display Printed Card Prices]**, 다음 중 하나를 선택합니다.

   - `Excluding Tax`
   - `Including Tax`
   - `Including and Excluding Tax`

1. 이러한 나머지 각 옵션에 대해 다음으로 전환 `Yes` 또는 `No` 기본 설정에 따라

   - **[!UICONTROL Include Tax in Order Total]**
   - **[!UICONTROL Display Full Tax Summary]**
   - **[!UICONTROL Display Zero Tax Subtotal]**

1. 완료되면 다음을 클릭하십시오. **[!UICONTROL Save Config]**.
