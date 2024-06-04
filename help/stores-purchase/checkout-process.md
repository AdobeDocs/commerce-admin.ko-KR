---
title: 체크아웃 프로세스 및 옵션
description: Adobe Commerce 및 Magento Open Source 체크아웃 프로세스에서 트랜잭션을 완료하는 데 필요한 정보를 수집하고 체크아웃 페이지에서 프로세스의 각 단계를 고객을 안내하는 방법을 알아봅니다.
exl-id: f503643b-a0bb-4763-9831-d592afb2c323
feature: Checkout
source-git-commit: 61df9a4bcfaf09491ae2d353478ceb281082fa74
workflow-type: tm+mt
source-wordcount: '1097'
ht-degree: 0%

---

# 체크아웃 프로세스 및 옵션

체크아웃 프로세스가 시작되면 트랜잭션이 안전한 암호화 채널로 이동합니다. 자물쇠 기호가 브라우저의 주소 표시줄에 나타나고 URL이 `http` 끝 `https`.

## 프로세스

체크아웃 프로세스의 목표는 트랜잭션을 완료하는 데 필요한 정보를 수집하는 것입니다. 다음 _체크아웃_ 페이지는 프로세스의 각 단계를 고객에게 안내합니다. 이미 많은 정보가 계정에 있기 때문에 계정에 로그인한 고객은 빠르게 체크아웃을 완료할 수 있습니다. 구매 주문을 사용하는 회사 계정과 연결된 고객의 워크플로는 약간 다릅니다.

### 배송

체크아웃 프로세스의 첫 단계는 고객이 배송 주소 정보를 완성하고 배송 방법을 선택하는 것입니다. 고객이 계정을 보유한 경우 배송 주소가 자동으로 입력되지만 필요한 경우 변경할 수 있습니다.

![Adobe Commerce](../assets/adobe-logo.svg) (Adobe Commerce만 해당) 수신자 및 발신자에 대한 거리 주소의 형식은 의 속성에 의해 결정됩니다 [고객 주소 속성](../customers/address-attributes.md). 입력 유효성 검사 설정은 배송 주소에 사용할 수 있는 올바른 문자를 결정합니다.

페이지 상단에 있는 진행률 표시줄은 체크아웃 프로세스의 각 단계를 따르며, 주문 요약에는 지금까지 입력한 정보가 표시됩니다.

![체크아웃 프로세스 중 배송 페이지](./assets/storefront-checkout-step1-shipping.png){width="600" zoomable="yes"}

#### 다른 주소로 배송

1. 주소록에 추가 항목이 있으면 고객은 주문을 배송할 주소를 찾습니다.

1. 주소를 선택하려면 를 클릭합니다 **[!UICONTROL Ship Here]**.

#### 주소 추가

1. 의 맨 아래에서 _[!UICONTROL Shipping Address]_섹션, 고객이 클릭&#x200B;**[!UICONTROL + New Address]**.

1. 다음을 완료합니다 _[!UICONTROL Shipping Address]_양식.

   기본적으로 고객의 이름과 성은 양식에 나타납니다.

   ![배송 주소 양식에 이름 및 주소 정보가 포함되어 있습니다.](./assets/storefront-checkout-step1-shipping-add-new-address.png){width="600" zoomable="yes"}

1. 새 주소를 주소록에 저장하려면 양식 하단에 있는 확인란을 선택합니다.

1. 클릭수 **[!UICONTROL Save Address]**.

   이제 새 주소가 배송 주소로 선택됩니다.

   ![배송 페이지에서 저장된 주소가 자동으로 선택됩니다.](./assets/storefront-checkout-step1-shipping-new-address-selected.png){width="600" zoomable="yes"}

#### 배송 방법 선택

1. 의 목록에서 [배송](delivery.md) 메서드에서 고객이 사용할 옵션을 선택합니다.

   ![배송 페이지에 배송 방법 옵션이 표시됩니다.](./assets/storefront-checkout-step1-shipping-methods.png){width="600" zoomable="yes"}

1. 클릭수 **[!UICONTROL Next]** 계속합니다.

### 검토 및 지급 - 정규 주문

체크아웃 프로세스의 두 번째 단계에서 고객은 [결제 방법](payments.md)를 누르고 프로모션 코드가 있는 모든 쿠폰을 구매에 적용합니다. 모든 정보를 검토하고 필요한 경우 편집할 수 있습니다. 활성화된 경우 고객은 주문을 하기 전에 판매 약관에 동의해야 합니다.

>[!NOTE]
>
>Commerce에서는 여러 쿠폰 코드를 구성할 수 있지만, 고객은 하나의 쿠폰 코드만 장바구니에 적용할 수 있습니다. (다음을 참조하십시오. [쿠폰 코드](../merchandising-promotions/price-rules-cart-coupon.md) 을 참조하십시오.)

![체크아웃 중 검토 및 결제 페이지](./assets/storefront-checkout-step2-payment-review.png){width="700" zoomable="yes"}

### 검토 및 지급 - 구매 발주

![Adobe Commerce](../assets/b2b.svg) (Adobe Commerce B2B에서만 사용 가능)

고객이 을 활성화한 회사와 연결된 경우 [구매 주문](../b2b/purchase-order-flow.md), 모든 주문은 구매 발주로 처리됩니다. 사용 가능한 결제 방법은 회사 계정 설정에 따라 결정됩니다.

1. 고객이 결제 방법을 선택합니다.

   사용 시 _계정입금_ 메서드, [!UICONTROL Custom Reference Number] 필드는 송장 번호를 참조하는 데 사용할 수 있습니다.

1. 고객이 클릭 **[!UICONTROL Place Purchase Order]**.

   구매 발주가 이루어집니다.

회사가 설정한 경우 [승인 규칙](../b2b/account-dashboard-approval-rules.md), 구매 주문은 승인 프로세스를 거칩니다. 그렇지 않으면 즉시 처리됩니다.

![구매 주문 검토 및 결제](./assets/checkout-storefront-step2-b2b.png){width="700" zoomable="yes"}

### 주문 요약에 표시되는 항목 수

관리자는 체크아웃 시 주문 요약에 표시되는 최대 항목 수를 변경하여 적은 수의 제품으로 표시를 간소화할 수 있습니다. 기본적으로 이 값은 10으로 설정됩니다.

![주문 요약에 표시되는 항목 수](./assets/order-summary.png){width="700" zoomable="yes"}

1. 다음에서 _관리자_ 사이드바, 이동 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. 왼쪽 패널에서 를 확장합니다. **[!UICONTROL Sales]** 및 선택 **[!UICONTROL Checkout]**.

1. 확장 ![확장 선택기](../assets/icon-display-expand.png) 다음 **[!UICONTROL Checkout Options]** 섹션.

1. 대상 **[!UICONTROL Maximum Number of Items to Display in Order Summary]**&#x200B;표시할 최대 항목 수를 입력합니다.

1. 클릭 **[!UICONTROL Save Config]**.

   이 업데이트에서는 체크아웃 중에 표시되는 주문 요약이 지정된 품목 수량으로 제한됩니다.

### 주문 확인

주문이 배치되면 주문 확인이 나타납니다. 등록된 고객의 경우, 이 페이지에는 고객 계정에 대한 링크와 영수증 생성 링크가 있는 주문 번호가 포함됩니다. 등록된 고객은 이메일로 주문 확인 및 추적 정보를 기대하라고 합니다. 고객은 주문을 추적할 계정을 만드는 것이 좋습니다. 등록된 고객은 링크를 클릭하여 영수증을 생성할 수 있습니다.

주문 확인 페이지는 또한 _성공_ 페이지 및 는 analytics 프로그램에서 전환을 추적하는 데 사용됩니다.

![주문 확인 페이지에 성공 메시지와 주문 번호가 표시됩니다.](./assets/storefront-checkout-confirmation-customer.png){width="700" zoomable="yes"}

## 체크아웃 옵션

체크아웃 옵션은 레이아웃을 포함하여 체크아웃 페이지에 대한 다양한 속성을 제어합니다. 게스트 체크아웃 허용 및 약관 계약 적용을 포함하여 체크아웃 시 제한을 두도록 구성할 수 있는 옵션이 있습니다. 체크아웃 프로세스 중에 정보 표시를 제어하는 옵션도 있습니다.

![구성 - 체크아웃 옵션](./assets/checkout-checkout-options.png){width="700" zoomable="yes"}

이러한 각 구성 설정에 대한 자세한 설명은 을 참조하십시오. [체크아웃 옵션](../configuration-reference/sales/checkout.md#checkout-options) 다음에서 _구성 참조 안내서_.

### 체크아웃 옵션 변경

1. 다음에서 _관리자_ 사이드바, 이동 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.
1. 왼쪽 패널에서 를 확장합니다. **[!UICONTROL Sales]** 및 선택 **[!UICONTROL Checkout]**.
1. 필요한 다음 옵션 중 하나를 설정합니다.
1. 클릭 **[!UICONTROL Save Config]**.

1. 확장 ![확장 선택기](../assets/icon-display-expand.png) 다음 **[!UICONTROL Checkout Options]** 섹션.

1. 특정 스토어 보기에 대한 설정인 경우 [스토어 보기 선택](../configuration-reference/scope-change.md#set-the-scope) 구성이 적용되는 위치입니다.

   메시지가 표시되면 **[!UICONTROL OK]** 계속합니다.

1. 체크아웃 옵션을 설정합니다.

1. 클릭 **[!UICONTROL Save Config]**.

### 사용 가능한 체크아웃 옵션

| 필드 | [범위](../getting-started/websites-stores-views.md#scope-settings) | 설명 |
|--- |--- |--- |
| [!UICONTROL Enable Onepage Checkout] | 스토어 뷰 | 다음 여부를 결정합니다. [한 페이지 체크아웃](checkout-one-page.md) 는 기본 체크아웃 형식입니다. 옵션: 예 / 아니요 |
| [!UICONTROL Allow Guest Checkout] | 스토어 뷰 | 게스트가 다음을 진행할 수 있는지 여부를 결정합니다. [등록하지 않고 체크아웃](checkout-guest.md) 스토어에 있는 계정입니다. 옵션: `Yes` / `No` |
| [!UICONTROL Enable Terms and Conditions] | 스토어 뷰 | 고객이 다음에 동의해야 하는지 여부를 결정합니다. [약관](terms-and-conditions.md) 구매 전 판매. 옵션: `Yes` / `No` |
| [!UICONTROL Display Billing Address On] | 스토어 뷰 | 체크아웃하는 동안 청구 주소의 위치를 결정합니다. 옵션: `Payment Method` / `Payment Page` |
| [!UICONTROL Maximum Number of Items to Display in Order Summary] | 스토어 뷰 | 체크아웃 중에 주문 요약에 표시할 수 있는 최대 항목 수를 결정합니다. 기본값은 입니다 `10`. |
| [!UICONTROL Enable Address Search] | 웹 사이트 | ![Adobe Commerce](../assets/adobe-logo.svg) (Adobe Commerce만 해당) 고객이 [주소 검색](checkout-address-search.md) 기능 _배송_&#x200B;및 _검토 및 결제_ 단계. 이 함수가 활성화되면 _[!UICONTROL Number of Customer Addresses Limit]_체크 아웃 중에 이 기능을 활성화하는 데 필요한 저장된 주소 수를 설정합니다. 옵션: `Yes` / `No` |
| [!UICONTROL Number of Customer Addresses Limit] | 웹 사이트 | ![Adobe Commerce](../assets/adobe-logo.svg) (Adobe Commerce만 해당) 주소 검색이 **[!UICONTROL Enabled]**&#x200B;체크 아웃 중에 이 기능을 활성화하는 데 필요한 저장된 주소 수를 결정합니다. 고객의 저장된 주소 수가 이 수를 충족하거나 초과하면 기본 주소만 _배송_ 및 _검토 및 결제_ 단계. 고객은 검색 기능을 사용하여 선택한 주소를 변경할 수 있습니다. 기본값은 10입니다. |

{style="table-layout:auto"}
