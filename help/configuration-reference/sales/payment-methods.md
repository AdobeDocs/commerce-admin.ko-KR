---
title: '[!UICONTROL Sales] &gt; [!UICONTROL Payment Methods]'
description: 에서 구성 설정을 검토합니다. [!UICONTROL Sales] &gt; [!UICONTROL Payment Methods] 상거래 관리자의 페이지입니다.
exl-id: 6545b980-c8ef-460a-a884-d5315f5ad513
feature: Configuration, Payments
source-git-commit: b710c0368dc765e3bf25e82324bffe7fb8192dbf
workflow-type: tm+mt
source-wordcount: '1667'
ht-degree: 0%

---

# [!UICONTROL Sales] > [!UICONTROL Payment Methods]

>[!TIP]
>
>Adobe Commerce 및 Magento Open Source용 결제 서비스는 강력하고 안전한 결제 처리를 위해 샌드박스 테스트 및 간단한 설정을 포함한 턴키 셀프서비스 솔루션을 제공합니다. 이 강력한 도구 세트와 어떻게 구매자에게 최상의 경험을 제공하는 데 필요한 통찰력과 컨트롤을 제공하는지에 대해 자세히 알아보려면 다음을 참조하십시오. [_결제 서비스 사용 안내서_](https://experienceleague.adobe.com/docs/commerce-merchant-services/payment-services/guide-overview.html).

{{config}}

## [!UICONTROL Merchant Location]

![판매자 위치](./assets/payment-methods-merchant-location.png)<!-- zoom -->

<!-- [Merchant Location](https://docs.magento.com/user-guide/payment/merchant-location.html) -->

| 필드 | [범위](../../getting-started/websites-stores-views.md#scope-settings) | 설명 |
|--- |--- |--- |
| [!UICONTROL Merchant Country] | 웹 사이트 | 판매자가 등록되어 비즈니스를 수행하는 국가를 식별합니다. |

{style="table-layout:auto"}

## 권장 솔루션

이제 막 시작하는 가맹점이 페이팔 계정이나 신용카드로 온라인 결제를 받을 수 있는 간편한 방법으로 다음의 결제 솔루션을 추천한다. 비즈니스가 성장함에 따라 이를 추가 PayPal 결제 솔루션과 결합할 수 있습니다.

- [PayPal Express 체크아웃](paypal-express-checkout.md)
- [Braintree](braintree.md)
- [결제 서비스](payment-services.md)

>[!NOTE]
>
>일부 결제 통합 및 번들 확장은 2.4.x 릴리스에서 제거되었으며 Commerce Marketplace으로 이동되었습니다. 에서 최신 공식 결제 통합 확장 프로그램을 찾을 수 있습니다. [Commerce Marketplace](https://marketplace.magento.com/extensions/payments-security.html){:target=&quot;_blank&quot;}.
><br/>
>**Amazon 페이** 및 **클라르나**: Adobe Commerce 및 Magento Open Source 릴리스 2.4.0 - 2.4.3에는 공급업체에서 개발한 이러한 확장이 포함되어 있습니다. 2.4.4 릴리스부터 이러한 확장은 더 이상 핵심 릴리스와 번들로 제공되지 않으며 Commerce Marketplace에서 설치하고 업데이트해야 합니다. Marketplace에서는 확장 개발자가 제공하는 현재 설명서에 대한 액세스도 제공합니다.
><br/>
>이러한 번들 확장 기능 중 하나를 활성화하고 구성한 경우 `composer.json` 파일을 2.4.4 업그레이드 프로세스의 일부로 추가하고 앞으로 확장 업데이트를 관리합니다. 다음을 참조하십시오 [모듈 업그레이드](https://experienceleague.adobe.com/docs/commerce-operations/upgrade-guide/modules/upgrade.html) 다음에서 _업그레이드 안내서_ 추가 정보.<br/>
><br/>
>**Worldpay**, **이웨이**, **사이버 소스**, 및 **Authorize.Net**: 이러한 결제 통합에서 보안 전환을 수행하는 방법에 대한 자세한 내용은 다음을 참조하십시오. [개발 블로그](https://community.magento.com/t5/Magento-DevBlog/Deprecation-of-Magento-core-payment-integrations/ba-p/426445){:target=&quot;_blank&quot;}.

## 기타 PayPal 메서드

PayPal은 모든 규모의 비즈니스 요구 사항을 충족하고 전 세계에서 비즈니스에 종사하고 있는 다양한 결제 솔루션을 제공합니다. PayPal은 모든 주요 직불 카드와 신용 카드의 지불을 수락할 수 있는 기능을 제공합니다. 페이팔 계정이 없는 고객도 페이팔로 구매 대금을 결제할 수 있기 때문에 페이팔은 별도의 노력 없이 추가 편의를 제공한다.

### PayPal 올인원 메서드

- [PayPal 결제 고급](paypal-payments-advanced.md)
- [PayPal 결제 프로](paypal-payments-pro.md)
- [PayPal 결제 표준](paypal-payments-standard.md)

### PayPal 결제 게이트웨이

- [Paypal Payflow Pro](paypal-payflow-pro.md) (빠른 체크아웃 포함)
- [PayPal 결제 링크](paypal-payflow-link.md) (빠른 체크아웃 포함)

## 기본 결제 방법

다음 결제 방법은 Commerce에 내장되어 있으며, 제3자 결제 공급자를 사용하여 거래를 처리하지 않습니다. 기본적인 결제 수단 중 상당수가 온라인이 아닌 오프라인에서 관리되었다.

### [!UICONTROL Check / Money Order]

![수표/우편환](./assets/payment-methods-check-money-order.png)<!-- zoom -->

<!-- [Check / Money Order](https://docs.magento.com/user-guide/payment/check-money-order.html) -->

| 필드 | [범위](../../getting-started/websites-stores-views.md#scope-settings) | 설명 |
|--- |--- |--- |
| [!UICONTROL Enabled] | 웹 사이트 | 고객이 수표로 결제할 수 있는지 아니면 금전으로 결제할 수 있는지 결정합니다. 옵션: `Yes` / `No` |
| [!UICONTROL Title] | 스토어 뷰 | 체크아웃 중에 고객에게 표시되는 이 결제 방법의 이름입니다. |
| [!UICONTROL New Order Status] | 웹 사이트 | 초기 값 결정 [주문 상태](../../stores-purchase/order-status.md) 수표 또는 금전 주문으로 지급된 주문에 할당됩니다. 기본값: `Pending` |
| [!UICONTROL Payment from Applicable Countries] | 웹 사이트 | 수표나 금전 주문에 의한 지급을 수락하는 국가를 결정합니다. 옵션: `All Allowed Countries` / `Specific Countries` |
| [!UICONTROL Payment from Specific Countries] | 웹 사이트 | 수표나 금전 주문에 의한 지급을 수락하는 특정 국가를 식별합니다. |
| [!UICONTROL Make Check Payable to] | 스토어 뷰 | 수표 및 금전 지급을 이행해야 할 주체의 이름. |
| [!UICONTROL Send Check to] | 스토어 뷰 | 수표 및 금전 주문을 전송해야 하는 거리 주소 또는 PO Box. |
| [!UICONTROL Minimum Order Total] | 웹 사이트 | 수표나 우편환으로 결제할 수 있는 최소 주문 금액. |
| [!UICONTROL Maximum Order Total] | 웹 사이트 | 수표 또는 금전 주문으로 결제할 수 있는 최대 주문 금액. <br/><br/>**_참고:_**합계가 최소 또는 최대 주문 합계 사이에 있거나 일치하는 경우 주문이 적격 처리됩니다. |
| [!UICONTROL Sort Order] | 웹 사이트 | 체크아웃 중에 다른 결제 방법과 함께 나열할 때 수표 또는 금전 주문에 의한 결제가 나타나는 순서를 결정하는 숫자입니다. 입력 `0` 목록의 맨 위에 놓습니다. |

{style="table-layout:auto"}

### [!UICONTROL Bank Transfer Payment]

![은행 송금 결제](./assets/payment-methods-bank-transfer-payment.png)<!-- zoom -->

<!-- [Bank Transfer Payment](https://docs.magento.com/user-guide/payment/bank-transfer.html) -->

| 필드 | [범위](../../getting-started/websites-stores-views.md#scope-settings) | 설명 |
|--- |--- |--- |
| [!UICONTROL Enabled] | 웹 사이트 | 고객이 은행에서 가맹점 계좌로 직접 결제를 이체하여 지급할 수 있는지 여부를 결정합니다. 옵션: `Yes` / `No` |
| [!UICONTROL Title] | 스토어 뷰 | 체크아웃 중에 고객에게 표시되는 이 결제 방법의 이름입니다. |
| [!UICONTROL New Order Status] | 웹 사이트 | 은행 이체별로 지급된 주문에 지정된 초기 주문 상태를 결정합니다. 기본값: `Pending` |
| [!UICONTROL Payment from Applicable Countries] | 웹 사이트 | 은행 이체로 지급을 수락하는 국가를 결정합니다. 옵션: `All Allowed Countries` / `Specific Countries` |
| [!UICONTROL Payment from Specific Countries] | 웹 사이트 | 은행 이체로 지급을 수락하는 특정 국가를 식별합니다. |
| [!UICONTROL Minimum Order Total] | 웹 사이트 | 은행 이체로 지급할 수 있는 최소 주문 금액. |
| [!UICONTROL Maximum Order Total] | 웹 사이트 | 은행 이체로 지급할 수 있는 가장 큰 주문 금액. <br/><br/>**_참고:_**합계가 최소 또는 최대 주문 합계 사이에 있거나 일치하는 경우 주문이 적격 처리됩니다. |
| [!UICONTROL Sort Order] | 웹 사이트 | 체크아웃 중에 다른 결제 방법과 함께 나열할 때 은행 이체로 지급하는 순서를 결정하는 번호가 나타납니다. 입력 `0` 목록의 맨 위에 놓습니다. |

{style="table-layout:auto"}

### [!UICONTROL Payment on Account]

{{b2b-feature}}

![계정입금](./assets/payment-methods-payment-on-account.png)<!-- zoom -->

<!-- [Payment on Account](https://docs.magento.com/user-guide/payment/payment-on-account.html) -->

| 필드 | [범위](../../getting-started/websites-stores-views.md#scope-settings) | 설명 |
|--- |--- |--- |
| [!UICONTROL Enabled] | 웹 사이트 | 회사가 회사 크레딧을 사용하여 구매할 수 있는지 여부를 결정합니다. 옵션: `Yes` / `No` |
| [!UICONTROL Title] | 스토어 뷰 | 체크아웃 중에 고객에게 표시되는 이 결제 방법의 이름입니다. |
| [!UICONTROL New Order Status] | 웹 사이트 | 회사 계정에 청구된 새 주문의 상태를 결정합니다. 옵션: `Pending (default)` / `Processing` / `Suspected Fraud` |
| [!UICONTROL Payment from Applicable Countries] | 웹 사이트 | 회사가 자신의 계정에 구매를 부과할 수 있도록 허용하는 국가를 결정합니다. 옵션: `All Allowed Countries` / `Specific Countries` |
| [!UICONTROL Payment from Specific Countries] | 웹 사이트 | 기업이 자신의 계정에 구매를 부과할 수 있는 특정 국가를 식별합니다. |
| [!UICONTROL Minimum Order Total] | 웹 사이트 | 회사 계정에 부과할 수 있는 최소 주문 금액을 지정합니다. |
| [!UICONTROL Maximum Order Total] | 웹 사이트 | 회사 계정에 청구할 수 있는 최대 주문 금액. <br/><br/>**_참고:_**합계가 최소 또는 최대 주문 합계 사이에 있거나 일치하는 경우 주문이 적격 처리됩니다. |
| [!UICONTROL Sort Order] | 웹 사이트 | 체크아웃 중에 다른 결제 방법과 함께 나열할 때 계정 결제가 표시되는 순서를 결정하는 번호입니다. 입력 `0` 목록의 맨 위에 놓습니다. |

{style="table-layout:auto"}

>[!NOTE]
>
>다음 주문의 경우 계정입금이 지원되지 않음: [여러 배송 주소](../../stores-purchase/shipping-settings.md#multiple-addresses) 및 은 결제 옵션에 표시되지 않습니다.

### [!UICONTROL Cash On Delivery Payment]

![게재 시 현금 결제](./assets/payment-methods-cash-on-delivery-payment.png)<!-- zoom -->

<!-- [Cash On Delivery Payment](../../stores-purchase/cash-on-delivery.html) -->

| 필드 | [범위](../../getting-started/websites-stores-views.md#scope-settings) | 설명 |
|--- |--- |--- |
| [!UICONTROL Enabled] | 웹 사이트 | 고객이 은행에서 가맹점 계좌로 직접 결제를 이체하여 지급할 수 있는지 여부를 결정합니다. 옵션: `Yes` / `No` |
| [!UICONTROL Title] | 스토어 뷰 | 체크아웃 중에 고객에게 표시되는 이 결제 방법의 이름입니다. |
| [!UICONTROL New Order Status] | 웹 사이트 | 은행 이체별로 지급된 주문에 지정된 초기 주문 상태를 결정합니다. 기본값: `Pending` |
| [!UICONTROL Payment from Applicable Countries] | 웹 사이트 | 은행 이체로 지급을 수락하는 국가를 결정합니다. 옵션: `All Allowed Countries` / `Specific Countries` |
| [!UICONTROL Payment from Specific Countries] | 웹 사이트 | 은행 이체로 지급을 수락하는 특정 국가를 식별합니다. |
| [!UICONTROL Minimum Order Total] | 웹 사이트 | 은행 이체로 지급할 수 있는 최소 주문 금액을 지정합니다. |
| [!UICONTROL Maximum Order Total] | 웹 사이트 | 은행 이체로 지급할 수 있는 가장 큰 주문 금액. <br/><br/>**_참고:_**합계가 최소 또는 최대 주문 합계 사이에 있거나 일치하는 경우 주문이 적격 처리됩니다. |
| [!UICONTROL Sort Order] | 웹 사이트 | 체크아웃 중에 다른 결제 방법과 함께 나열할 때 은행 이체로 지급하는 순서를 결정하는 번호가 나타납니다. 입력 `0` 목록의 맨 위에 놓습니다. |

{style="table-layout:auto"}

### [!UICONTROL Zero Subtotal Checkout]

![제로 소계 체크아웃](./assets/payment-methods-zero-subtotal-checkout.png)<!-- zoom -->

<!-- [Zero Subtotal Checkout](../../stores-purchase/zero-subtotal-checkout.html) -->

| 필드 | [범위](../../getting-started/websites-stores-views.md#scope-settings) | 설명 |
|--- |--- |--- |
| [!UICONTROL Title] | 스토어 뷰 | 체크아웃 시 이 결제 방법에 사용되는 이름. 기본값: 결제 정보 필요 없음 |
| [!UICONTROL Enabled] | 웹 사이트 | 저장소 관리자가 세금이 부과된 주문과 같이 소계가 0인 주문을 관리할 수 있도록 0 소계 체크아웃을 사용할 수 있는지 여부를 결정합니다. 그러나 할인으로 인해 금액이 0으로 줄어들었습니다. 옵션: `Yes` / `No` |
| [!UICONTROL New Order Status] | 웹 사이트 | 0 소계 체크아웃으로 처리된 주문에 지정된 초기 주문 상태를 결정합니다. 기본값: `Pending` |
| [!UICONTROL Payment from Applicable Countries] | 웹 사이트 | 소계 체크아웃 0을 적용할 수 있는 국가를 결정합니다. 옵션: `All Allowed Countries` / `Specific Countries` |
| [!UICONTROL Payment from Specific Countries] | 웹 사이트 | 소계 체크아웃 0이 적용될 수 있는 특정 국가를 식별합니다. |
| [!UICONTROL Sort Order] | 웹 사이트 | 체크아웃 시 다른 결제 방법과 함께 나열할 때 &quot;결제 정보가 필요하지 않음&quot;과 같이 제목이 표시되는 순서를 결정하는 번호입니다. 입력 `0` 목록의 맨 위에 놓습니다. |

{style="table-layout:auto"}

## [!UICONTROL Payment actions]

결제 작업이 구성됨 _결제 방법별_. 지급 조치는 자금이 수집되는 시기와 판매 주문에 대한 송장이 생성되는 시기를 결정합니다.

개별 구성 옵션에 대한 포괄적인 목록이 필요하면 각 개별 결제 방법 항목의 기본 설정 섹션을 참조하십시오.

| 결제 작업 | 설명 |
|--- |---|
| [!UICONTROL Authorization] | 구매를 승인하지만 자금을 보류합니다. 상인에게 포획될 때까지 그 금액이 인출되지 않는다. |
| [!UICONTROL Authorize] | 주문 합계에 대한 구매자 계정을 승인하지만 지급을 캡처하지 않습니다. 송장을 생성하여 지급을 파악합니다. 승인된 주문을 무효화하거나 취소할 수 있습니다. |
| [!UICONTROL Authorize and Capture] | 주문 합계에 대한 구매자 계정을 승인하고 지급을 캡처합니다. 송장은 자동으로 생성됩니다. 캡처된 자금은 대변 메모를 통해 환불 가능합니다. 결제가 수집된 후에는 주문을 취소할 수 없습니다. |
| [!UICONTROL Charge on shipment] | Amazon은 캡처 요청을 받고 송장이 Commerce에서 생성될 때 고객에게 비용을 청구합니다. |
| [!UICONTROL Charge on order] | Amazon은 송장을 생성하고 주문이 이행될 때 고객에게 비용을 청구합니다. |
| [!UICONTROL Not Capture] | 송장이 제출되면 시스템에서 지급을 캡처하지 않습니다. 나중에 Commerce를 통해 결제를 캡처한다고 가정합니다. 완료된 청구서에는 캡처 버튼이 있습니다. 수집하기 전에 송장을 취소할 수 있습니다. 캡처한 후 대변 메모를 생성하고 송장을 무효화할 수 있습니다. |
| [!UICONTROL Order] | 머천트가 정의된 기간(최대 29일) 내에 고객의 구매자 계정에서 주문 총액까지 하나 이상의 금액을 캡처할 수 있도록 하는 PayPal과의 계약을 나타냅니다. |
| [!UICONTROL Sale] | 구매 금액이 승인되어 즉시 고객의 계좌에서 인출됩니다. |

{style="table-layout:auto"}

>[!NOTE]
>
>다음 항목을 선택하지 마십시오. _[!UICONTROL Not Capture]_나중에 Commerce를 통해 결제를 캡처할 것이 확실하지 않은 경우 옵션을 선택합니다. 수집 버튼을 사용하여 지급이 수집될 때까지 대변 메모를 생성할 수 없습니다.

## [!UICONTROL Purchase Order]

![구매 주문](./assets/payment-methods-purchase-order.png)<!-- zoom -->

<!-- [Purchase Order](../../stores-purchase/purchase-order.html) -->

| 필드 | [범위](../../getting-started/websites-stores-views.md#scope-settings) | 설명 |
|--- |--- |--- |
| [!UICONTROL Enabled] | 웹 사이트 | 고객이 구매 발주(PO)별로 지급할 수 있는지 여부를 결정합니다. 옵션: `Yes` / `No` |
| [!UICONTROL Title] | 스토어 뷰 | 체크아웃 중에 고객에게 표시되는 이 결제 방법의 이름. |
| [!UICONTROL New Order Status] | 웹 사이트 | 초기 값 결정 [주문 상태](../../stores-purchase/order-status.md) PO에서 지급한 주문에 할당됩니다. 기본값: 보류 중 |
| [!UICONTROL Payment from Applicable Countries] | 웹 사이트 | PO에 의한 지급을 수락하는 국가를 결정합니다. 옵션: `All Allowed Countries` / `Specific Countries` |
| [!UICONTROL Payment from Specific Countries] | 웹 사이트 | PO별 지급을 수락하는 특정 국가를 식별합니다. |
| [!UICONTROL Minimum Order Total] | 웹 사이트 | PO로 지급할 수 있는 최소 주문 수량입니다. |
| [!UICONTROL Maximum Order Total] | 웹 사이트 | PO로 지급할 수 있는 가장 큰 주문 금액. <br/><br/>**_참고:_**합계가 최소 또는 최대 주문 합계 사이에 있거나 일치하는 경우 주문이 적격 처리됩니다. |
| [!UICONTROL Sort Order] | 웹 사이트 | 체크아웃 중에 다른 결제 방법과 함께 나열할 때 PO별 결제 순서를 결정하는 번호가 나타납니다. 입력 `0` 목록의 맨 위에 놓습니다. |

{style="table-layout:auto"}
