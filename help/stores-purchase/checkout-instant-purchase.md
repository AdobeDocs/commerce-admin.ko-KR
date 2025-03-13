---
title: 즉시 구매
description: 즉시 구매 와 등록된 고객 계정에 대해 신속한 체크아웃을 제공하는 방법에 대해 알아봅니다.
exl-id: f299f364-d7e3-4567-8c7b-955129011a19
feature: Checkout
source-git-commit: 5da244a548b15863fe31b5df8b509f8e63df27c2
workflow-type: tm+mt
source-wordcount: '396'
ht-degree: 0%

---

# 즉시 구매

_즉시 구매_&#x200B;를 통해 고객은 계정에 저장된 정보를 사용하여 체크아웃 프로세스를 빠르게 진행할 수 있습니다. 활성화하면 _즉시 구매_ 단추가 제품 페이지의 _장바구니에 추가_ 단추 아래에 표시되어 요구 사항을 충족하는 고객에게 제공됩니다.

![즉시 구매 옵션이 표시된 제품 페이지](./assets/storefront-checkout-instant-purchase.png){width="700" zoomable="yes"}

## 고객 요구 사항

- 고객이 계정에 [로그인](../customers/customer-sign-in.md)되었습니다.

- 고객 계정에 [기본 청구 및 배송 주소](../customers/account-dashboard-address-book.md)가 있습니다.

- 기본 배송 주소에 지정된 국가에 대해 하나 이상의 [배송 방법](delivery.md)을 사용할 수 있습니다.

- 고객 계정에 자격 증명 모음이 활성화된 [저장된 결제](../stores-purchase/stored-payment-methods.md) 메서드가 있습니다.

  다음 결제 방법을 사용하여 저장된 신용 카드 정보에 안전하게 액세스할 수 있습니다.

   - [Braintree 신용 카드](braintree.md)(3D 보안이 활성화된 경우 즉시 구매는 Braintree 신용 카드와 함께 사용할 수 없음)
   - [PayPal이 활성화된 Braintree](braintree.md)
   - [Paypal Payflow Pro](paypal-payflow-pro.md)

## 상점 첫 화면에서 즉시 구매

1. 상점 첫 화면에서 고객은 구매해야 할 품목의 제품 페이지로 이동합니다.

1. 필요한 옵션을 선택하고 **[!UICONTROL Instant Purchase]**&#x200B;을(를) 클릭합니다.

   ![즉시 구매를 확인하는 확인 대화 상자](./assets/storefront-checkout-instant-purchase-confirmation.png){width="500" zoomable="yes"}

1. **[!UICONTROL Instant Purchase Confirmation]** 정보를 검토하고 **[!UICONTROL OK]**&#x200B;을(를) 클릭하여 트랜잭션을 완료합니다.

   제품 페이지 상단에 확인 메시지와 주문 번호가 나타납니다.

## 즉시 구매 구성

### 1단계: 구성 페이지 열기

1. _관리자_ 사이드바에서 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**(으)로 이동합니다.

### 2단계: 결제 방법 자격 증명 모음 구성

Braintree 또는 Adobe Commerce 및 Magento Open Source용 결제 서비스와 함께 즉시 구매를 사용할 수 있습니다. 구매자가 즉시 구매 기능을 사용하려면 먼저 보관을 활성화해야 합니다.

결제 방법을 구성하고 Braintree 또는 결제 서비스에 대한 저장 기능을 활성화하는 방법에 대해 알아봅니다.

- [Braintree](braintree.md)
- [결제 서비스 설명서](https://experienceleague.adobe.com/docs/commerce/payment-services/guide-overview.html)

### 3단계: 즉시 구매 활성화

1. _[!UICONTROL Sales]_섹션 아래의 왼쪽 패널에서&#x200B;**[!UICONTROL Sales]**을(를) 선택합니다.

1. **[!UICONTROL Instant Purchase]** 섹션에서 ![확장 선택기](../assets/icon-display-expand.png)를 확장합니다.

1. 이 변경 내용이 특정 스토어 보기에 대한 것이면 구성이 적용되는 [스토어 보기를 선택](../configuration-reference/scope-change.md#set-the-scope)합니다.

   메시지가 표시되면 **[!UICONTROL OK]**&#x200B;을(를) 클릭하여 계속합니다.

1. **[!UICONTROL Enabled]**&#x200B;을(를) `Yes`(으)로 설정합니다.

1. 단추에 표시할 **[!UICONTROL Button Text]**&#x200B;을(를) 입력하십시오.

   각 스토어 보기 또는 언어에 대해 단추 텍스트를 변경할 수 있습니다. 기본적으로 단추 텍스트는 `Instant Purchase`입니다.

   ![구성 - 즉시 구매 옵션](../configuration-reference/sales/assets/sales-instant-purchase.png){width="600" zoomable="yes"}

   이러한 각 구성 설정에 대한 자세한 설명은 _구성 참조 안내서_&#x200B;의 [즉시 구매](../configuration-reference/sales/sales.md#instant-purchase)를 참조하십시오.

1. **[!UICONTROL Save Config]**&#x200B;을(를) 클릭합니다.

1. 캐시를 업데이트하라는 메시지가 표시되면 시스템 메시지에서 **[!UICONTROL Cache Management]**&#x200B;을(를) 클릭하고 지침에 따라 캐시를 플러시합니다.
