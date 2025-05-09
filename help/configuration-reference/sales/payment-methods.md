---
title: '[!UICONTROL Sales] &gt; [!UICONTROL Payment Methods]'
description: Commerce 관리자의 [!UICONTROL Sales] &gt; [!UICONTROL Payment Methods] 페이지에서 구성 설정을 검토하십시오.
exl-id: 6545b980-c8ef-460a-a884-d5315f5ad513
feature: Configuration, Payments
source-git-commit: 489c72652693a15ffe1c745277bbaa9da084dcba
workflow-type: tm+mt
source-wordcount: '1772'
ht-degree: 0%

---

# [!UICONTROL Sales] > [!UICONTROL Payment Methods]

>[!TIP]
>
>Adobe Commerce 및 Magento Open Source용 결제 서비스는 강력하고 안전한 결제 처리를 위해 샌드박스 테스트 및 간단한 설정을 포함한 턴키 셀프 서비스 솔루션을 제공합니다. 이 강력한 도구 집합에 대해 자세히 알아보고 구매자에게 최상의 경험을 제공하기 위해 필요한 insight 및 제어 기능에 대해 알아보려면 [_결제 서비스 사용 안내서_](https://experienceleague.adobe.com/docs/commerce/payment-services/guide-overview.html)를 참조하세요.

{{config}}

## [!UICONTROL Merchant Location]

[!BADGE PaaS만]{type=Informative url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="Adobe Commerce 온 클라우드 프로젝트(Adobe 관리 PaaS 인프라) 및 온프레미스 프로젝트에만 적용됩니다."}

![판매자 위치](./assets/payment-methods-merchant-location.png)<!-- zoom -->

<!-- [Merchant Location](https://experienceleague.adobe.com/en/docs/commerce-admin/start/setup/store-details#merchant-location) -->

| 필드 | [범위](../../getting-started/websites-stores-views.md#scope-settings) | 설명 |
|--- |--- |--- |
| [!UICONTROL Merchant Country] | 웹 사이트 | 판매자가 등록되어 비즈니스를 수행하는 국가를 식별합니다. |

{style="table-layout:auto"}

## 권장 솔루션

이제 막 시작하는 가맹점이 페이팔 계정이나 신용카드로 온라인 결제를 받을 수 있는 간편한 방법으로 다음의 결제 솔루션을 추천한다. 비즈니스가 성장함에 따라 이를 추가 PayPal 결제 솔루션과 결합할 수 있습니다.

- [결제 서비스](payment-services.md)
- [!BADGE PaaS 전용]{type=Informative url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="Adobe Commerce 온 클라우드 프로젝트(Adobe 관리 PaaS 인프라) 및 온프레미스 프로젝트에만 적용됩니다."} [PayPal 빠른 체크아웃](paypal-express-checkout.md)
- [!BADGE PaaS만]{type=Informative url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="Adobe Commerce 온 클라우드 프로젝트(Adobe 관리 PaaS 인프라) 및 온프레미스 프로젝트에만 적용됩니다."} [Braintree](braintree.md)

>[!NOTE]
>
>일부 결제 통합 및 번들 확장은 2.4.x 릴리스에서 제거되었으며 Commerce Marketplace으로 이동되었습니다. [Commerce Marketplace](https://marketplace.magento.com/extensions/payments-security.html){:target="_blank"}에서 최신 공식 결제 통합 확장을 찾을 수 있습니다.
><br/>
>**Amazon Pay** 및 **Klarna**: Adobe Commerce 및 Magento Open Source 릴리스 2.4.0 - 2.4.3에는 이러한 공급업체에서 개발한 확장이 포함되어 있습니다. 2.4.4 릴리스부터 이러한 확장은 더 이상 핵심 릴리스와 번들로 제공되지 않으며 Commerce Marketplace에서 설치하고 업데이트해야 합니다. Marketplace에서는 확장 개발자가 제공하는 현재 설명서에 대한 액세스도 제공합니다.
><br/>
>이러한 번들 확장을 사용 및 구성한 경우 2.4.4 업그레이드 프로세스의 일부로 `composer.json` 파일을 업데이트하고 앞으로 확장 업데이트를 관리해야 합니다. 자세한 내용은 _업그레이드 안내서_&#x200B;의 [업그레이드 모듈](https://experienceleague.adobe.com/docs/commerce-operations/upgrade-guide/modules/upgrade.html)을 참조하십시오.<br/>
><br/>
>**Worldpay**, **Eway**, **CyberSource** 및 **Authorize.Net**: 이러한 결제 통합에서 안전하게 전환하는 방법에 대한 자세한 내용은 [DevBlog](https://community.magento.com/t5/Magento-DevBlog/Deprecation-of-Magento-core-payment-integrations/ba-p/426445){:target="_blank"}을(를) 참조하십시오.

## 기타 PayPal 메서드

[!BADGE PaaS만]{type=Informative url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="Adobe Commerce 온 클라우드 프로젝트(Adobe 관리 PaaS 인프라) 및 온프레미스 프로젝트에만 적용됩니다."}

PayPal은 모든 규모의 비즈니스 요구 사항을 충족하고 전 세계에서 비즈니스에 종사하고 있는 다양한 결제 솔루션을 제공합니다. PayPal은 모든 주요 직불 카드와 신용 카드의 지불을 수락할 수 있는 기능을 제공합니다. 페이팔 계정이 없는 고객도 페이팔로 구매 대금을 결제할 수 있기 때문에 페이팔은 별도의 노력 없이 추가 편의를 제공한다.

### PayPal 올인원 메서드

[!BADGE PaaS만]{type=Informative url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="Adobe Commerce 온 클라우드 프로젝트(Adobe 관리 PaaS 인프라) 및 온프레미스 프로젝트에만 적용됩니다."}

- [PayPal 결제 고급](paypal-payments-advanced.md)
- [PayPal 결제 프로](paypal-payments-pro.md)
- [PayPal 결제 표준](paypal-payments-standard.md)

### PayPal 결제 게이트웨이

[!BADGE PaaS만]{type=Informative url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="Adobe Commerce 온 클라우드 프로젝트(Adobe 관리 PaaS 인프라) 및 온프레미스 프로젝트에만 적용됩니다."}

- [PayPal Payflow Pro](paypal-payflow-pro.md)(빠른 체크아웃 포함)
- [PayPal 결제 링크](paypal-payflow-link.md)(빠른 체크아웃 포함)

## 기본 결제 방법

다음 결제 방법은 Commerce에 기본 제공되며 서드파티 결제 공급자를 사용하여 거래를 처리하지 않습니다. 기본적인 결제 수단 중 상당수가 온라인이 아닌 오프라인에서 관리되었다.

### [!UICONTROL Check / Money Order]

![주문 확인/금액](./assets/payment-methods-check-money-order.png)<!-- zoom -->

<!-- [Check / Money Order](https://experienceleague.adobe.com/en/docs/commerce-admin/stores-sales/payments/offline/check-money-order) -->

| 필드 | [범위](../../getting-started/websites-stores-views.md#scope-settings) | 설명 |
|--- |--- |--- |
| [!UICONTROL Enabled] | 웹 사이트 | 고객이 수표로 결제할 수 있는지 아니면 금전으로 결제할 수 있는지 결정합니다. 옵션: `Yes` / `No` |
| [!UICONTROL Title] | 스토어 뷰 | 체크아웃 중에 고객에게 표시되는 이 결제 방법의 이름입니다. |
| [!UICONTROL New Order Status] | 웹 사이트 | 수표 또는 금전 주문으로 지급된 주문에 할당된 초기 [주문 상태](../../stores-purchase/order-status.md)를 결정합니다. 기본값: `Pending` |
| [!UICONTROL Payment from Applicable Countries] | 웹 사이트 | 수표나 금전 주문에 의한 지급을 수락하는 국가를 결정합니다. 옵션: `All Allowed Countries` / `Specific Countries` |
| [!UICONTROL Payment from Specific Countries] | 웹 사이트 | 수표나 금전 주문에 의한 지급을 수락하는 특정 국가를 식별합니다. |
| [!UICONTROL Make Check Payable to] | 스토어 뷰 | 수표 및 금전 지급을 이행해야 할 주체의 이름. |
| [!UICONTROL Send Check to] | 스토어 뷰 | 수표 및 금전 주문을 전송해야 하는 거리 주소 또는 PO Box. |
| [!UICONTROL Minimum Order Total] | 웹 사이트 | 수표나 우편환으로 결제할 수 있는 최소 주문 금액. |
| [!UICONTROL Maximum Order Total] | 웹 사이트 | 수표 또는 금전 주문으로 결제할 수 있는 최대 주문 금액. <br/><br/>**_참고:_**합계가 최소 또는 최대 주문 합계 사이에 있거나 일치하는 경우 주문이 유효합니다. |
| [!UICONTROL Sort Order] | 웹 사이트 | 체크아웃 중에 다른 결제 방법과 함께 나열할 때 수표 또는 금전 주문에 의한 결제가 나타나는 순서를 결정하는 숫자입니다. `0`을(를) 입력하여 목록의 맨 위에 배치합니다. |

{style="table-layout:auto"}

### [!UICONTROL Bank Transfer Payment]

![은행 계좌 이체 결제](./assets/payment-methods-bank-transfer-payment.png)<!-- zoom -->

<!-- [Bank Transfer Payment](https://experienceleague.adobe.com/en/docs/commerce-admin/stores-sales/payments/offline/bank-transfer) -->

| 필드 | [범위](../../getting-started/websites-stores-views.md#scope-settings) | 설명 |
|--- |--- |--- |
| [!UICONTROL Enabled] | 웹 사이트 | 고객이 은행에서 가맹점 계좌로 직접 결제를 이체하여 지급할 수 있는지 여부를 결정합니다. 옵션: `Yes` / `No` |
| [!UICONTROL Title] | 스토어 뷰 | 체크아웃 중에 고객에게 표시되는 이 결제 방법의 이름입니다. |
| [!UICONTROL New Order Status] | 웹 사이트 | 은행 이체별로 지급된 주문에 지정된 초기 주문 상태를 결정합니다. 기본값: `Pending` |
| [!UICONTROL Payment from Applicable Countries] | 웹 사이트 | 은행 이체로 지급을 수락하는 국가를 결정합니다. 옵션: `All Allowed Countries` / `Specific Countries` |
| [!UICONTROL Payment from Specific Countries] | 웹 사이트 | 은행 이체로 지급을 수락하는 특정 국가를 식별합니다. |
| [!UICONTROL Minimum Order Total] | 웹 사이트 | 은행 이체로 지급할 수 있는 최소 주문 금액. |
| [!UICONTROL Maximum Order Total] | 웹 사이트 | 은행 이체로 지급할 수 있는 가장 큰 주문 금액. <br/><br/>**_참고:_**합계가 최소 또는 최대 주문 합계 사이에 있거나 일치하는 경우 주문이 유효합니다. |
| [!UICONTROL Sort Order] | 웹 사이트 | 체크아웃 중에 다른 결제 방법과 함께 나열할 때 은행 이체로 지급하는 순서를 결정하는 번호가 나타납니다. `0`을(를) 입력하여 목록의 맨 위에 배치합니다. |

{style="table-layout:auto"}

### [!UICONTROL Payment on Account]

{{b2b-feature}}

![계정 결제](./assets/payment-methods-payment-on-account.png)<!-- zoom -->

<!-- [Payment on Account](https://experienceleague.adobe.com/en/docs/commerce-admin/b2b/enable-basic-features#configure-payment-on-account) -->

| 필드 | [범위](../../getting-started/websites-stores-views.md#scope-settings) | 설명 |
|--- |--- |--- |
| [!UICONTROL Enabled] | 웹 사이트 | 회사가 회사 크레딧을 사용하여 구매할 수 있는지 여부를 결정합니다. 옵션: `Yes` / `No` |
| [!UICONTROL Title] | 스토어 뷰 | 체크아웃 중에 고객에게 표시되는 이 결제 방법의 이름입니다. |
| [!UICONTROL New Order Status] | 웹 사이트 | 회사 계정에 청구된 새 주문의 상태를 결정합니다. 옵션: `Pending (default)` / `Processing` / `Suspected Fraud` |
| [!UICONTROL Payment from Applicable Countries] | 웹 사이트 | 회사가 자신의 계정에 구매를 부과할 수 있도록 허용하는 국가를 결정합니다. 옵션: `All Allowed Countries` / `Specific Countries` |
| [!UICONTROL Payment from Specific Countries] | 웹 사이트 | 기업이 자신의 계정에 구매를 부과할 수 있는 특정 국가를 식별합니다. |
| [!UICONTROL Minimum Order Total] | 웹 사이트 | 회사 계정에 부과할 수 있는 최소 주문 금액을 지정합니다. |
| [!UICONTROL Maximum Order Total] | 웹 사이트 | 회사 계정에 청구할 수 있는 최대 주문 금액. <br/><br/>**_참고:_**합계가 최소 또는 최대 주문 합계 사이에 있거나 일치하는 경우 주문이 유효합니다. |
| [!UICONTROL Sort Order] | 웹 사이트 | 체크아웃 중에 다른 결제 방법과 함께 나열할 때 계정 결제가 표시되는 순서를 결정하는 번호입니다. `0`을(를) 입력하여 목록의 맨 위에 배치합니다. |

{style="table-layout:auto"}

>[!NOTE]
>
>계정 결제는 [여러 배송 주소](../../stores-purchase/shipping-settings.md#multiple-addresses)를 가진 주문에 대해 지원되지 않으며 결제 옵션 사이에 나타나지 않습니다.

### [!UICONTROL Cash On Delivery Payment]

![배달 결제 시 현금](./assets/payment-methods-cash-on-delivery-payment.png)<!-- zoom -->

<!-- [Cash On Delivery Payment](../../stores-purchase/cash-on-delivery.html) -->

| 필드 | [범위](../../getting-started/websites-stores-views.md#scope-settings) | 설명 |
|--- |--- |--- |
| [!UICONTROL Enabled] | 웹 사이트 | 고객이 은행에서 가맹점 계좌로 직접 결제를 이체하여 지급할 수 있는지 여부를 결정합니다. 옵션: `Yes` / `No` |
| [!UICONTROL Title] | 스토어 뷰 | 체크아웃 중에 고객에게 표시되는 이 결제 방법의 이름입니다. |
| [!UICONTROL New Order Status] | 웹 사이트 | 은행 이체별로 지급된 주문에 지정된 초기 주문 상태를 결정합니다. 기본값: `Pending` |
| [!UICONTROL Payment from Applicable Countries] | 웹 사이트 | 은행 이체로 지급을 수락하는 국가를 결정합니다. 옵션: `All Allowed Countries` / `Specific Countries` |
| [!UICONTROL Payment from Specific Countries] | 웹 사이트 | 은행 이체로 지급을 수락하는 특정 국가를 식별합니다. |
| [!UICONTROL Minimum Order Total] | 웹 사이트 | 은행 이체로 지급할 수 있는 최소 주문 금액을 지정합니다. |
| [!UICONTROL Maximum Order Total] | 웹 사이트 | 은행 이체로 지급할 수 있는 가장 큰 주문 금액. <br/><br/>**_참고:_**합계가 최소 또는 최대 주문 합계 사이에 있거나 일치하는 경우 주문이 유효합니다. |
| [!UICONTROL Sort Order] | 웹 사이트 | 체크아웃 중에 다른 결제 방법과 함께 나열할 때 은행 이체로 지급하는 순서를 결정하는 번호가 나타납니다. `0`을(를) 입력하여 목록의 맨 위에 배치합니다. |

{style="table-layout:auto"}

### [!UICONTROL Zero Subtotal Checkout]

![0 소계 체크아웃](./assets/payment-methods-zero-subtotal-checkout.png)<!-- zoom -->

<!-- [Zero Subtotal Checkout](../../stores-purchase/zero-subtotal-checkout.html) -->

| 필드 | [범위](../../getting-started/websites-stores-views.md#scope-settings) | 설명 |
|--- |--- |--- |
| [!UICONTROL Title] | 스토어 뷰 | 체크아웃 시 이 결제 방법에 사용되는 이름. 기본값: 결제 정보 필요 없음 |
| [!UICONTROL Enabled] | 웹 사이트 | 저장소 관리자가 세금이 부과된 주문과 같이 소계가 0인 주문을 관리할 수 있도록 0 소계 체크아웃을 사용할 수 있는지 여부를 결정합니다. 그러나 할인으로 인해 금액이 0으로 줄어들었습니다. 옵션: `Yes` / `No` |
| [!UICONTROL New Order Status] | 웹 사이트 | 0 소계 체크아웃으로 처리된 주문에 지정된 초기 주문 상태를 결정합니다. 기본값: `Pending` |
| [!UICONTROL Payment from Applicable Countries] | 웹 사이트 | 소계 체크아웃 0을 적용할 수 있는 국가를 결정합니다. 옵션: `All Allowed Countries` / `Specific Countries` |
| [!UICONTROL Payment from Specific Countries] | 웹 사이트 | 소계 체크아웃 0이 적용될 수 있는 특정 국가를 식별합니다. |
| [!UICONTROL Sort Order] | 웹 사이트 | 체크아웃 시 다른 결제 방법과 함께 나열할 때 &quot;결제 정보가 필요하지 않음&quot;과 같이 제목이 표시되는 순서를 결정하는 번호입니다. `0`을(를) 입력하여 목록의 맨 위에 배치합니다. |

{style="table-layout:auto"}

## [!UICONTROL Payment actions]

[!BADGE PaaS만]{type=Informative url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="Adobe Commerce 온 클라우드 프로젝트(Adobe 관리 PaaS 인프라) 및 온프레미스 프로젝트에만 적용됩니다."}

결제 작업이 _결제 방법별로_&#x200B;구성되어 있습니다. 지급 조치는 자금이 수집되는 시기와 판매 주문에 대한 송장이 생성되는 시기를 결정합니다.

개별 구성 옵션에 대한 포괄적인 목록이 필요하면 각 개별 결제 방법 항목의 기본 설정 섹션을 참조하십시오.

| 결제 작업 | 설명 |
|--- |---|
| [!UICONTROL Authorization] | 구매를 승인하지만 자금을 보류합니다. 상인에게 포획될 때까지 그 금액이 인출되지 않는다. |
| [!UICONTROL Authorize] | 주문 합계에 대한 구매자 계정을 승인하지만 지급을 캡처하지 않습니다. 송장을 생성하여 지급을 파악합니다. 승인된 주문을 무효화하거나 취소할 수 있습니다. |
| [!UICONTROL Authorize and Capture] | 주문 합계에 대한 구매자 계정을 승인하고 지급을 캡처합니다. 송장은 자동으로 생성됩니다. 캡처된 자금은 대변 메모를 통해 환불 가능합니다. 결제가 수집된 후에는 주문을 취소할 수 없습니다. |
| [!UICONTROL Charge on shipment] | Amazon은 캡처 요청을 받고 송장이 Commerce에서 생성될 때 고객에게 비용을 청구합니다. |
| [!UICONTROL Charge on order] | Amazon은 송장을 생성하고 주문이 이행될 때 고객에게 비용을 청구합니다. |
| [!UICONTROL Not Capture] | 송장이 제출되면 시스템에서 지급을 캡처하지 않습니다. 나중에 Commerce을 통해 결제를 캡처한다고 가정합니다. 완료된 청구서에는 캡처 버튼이 있습니다. 수집하기 전에 송장을 취소할 수 있습니다. 캡처한 후 대변 메모를 생성하고 송장을 무효화할 수 있습니다. |
| [!UICONTROL Order] | 머천트가 정의된 기간(최대 29일) 내에 고객의 구매자 계정에서 주문 총액까지 하나 이상의 금액을 캡처할 수 있도록 하는 PayPal과의 계약을 나타냅니다. |
| [!UICONTROL Sale] | 구매 금액이 승인되어 즉시 고객의 계좌에서 인출됩니다. |

{style="table-layout:auto"}

>[!NOTE]
>
>나중에 Commerce을 통해 결제를 캡처할 것이 확실하지 않은 경우 _[!UICONTROL Not Capture]_옵션을 선택하지 마십시오. 수집 버튼을 사용하여 지급이 수집될 때까지 대변 메모를 생성할 수 없습니다.

## [!UICONTROL Purchase Order]

![구매 주문](./assets/payment-methods-purchase-order.png)<!-- zoom -->

<!-- [Purchase Order](../../stores-purchase/purchase-order.html) -->

| 필드 | [범위](../../getting-started/websites-stores-views.md#scope-settings) | 설명 |
|--- |--- |--- |
| [!UICONTROL Enabled] | 웹 사이트 | 고객이 구매 발주(PO)별로 지급할 수 있는지 여부를 결정합니다. 옵션: `Yes` / `No` |
| [!UICONTROL Title] | 스토어 뷰 | 체크아웃 중에 고객에게 표시되는 이 결제 방법의 이름. |
| [!UICONTROL New Order Status] | 웹 사이트 | PO로 지급된 주문에 할당된 초기 [주문 상태](../../stores-purchase/order-status.md)를 결정합니다. 기본값: 보류 중 |
| [!UICONTROL Payment from Applicable Countries] | 웹 사이트 | PO에 의한 지급을 수락하는 국가를 결정합니다. 옵션: `All Allowed Countries` / `Specific Countries` |
| [!UICONTROL Payment from Specific Countries] | 웹 사이트 | PO별 지급을 수락하는 특정 국가를 식별합니다. |
| [!UICONTROL Minimum Order Total] | 웹 사이트 | PO로 지급할 수 있는 최소 주문 수량입니다. |
| [!UICONTROL Maximum Order Total] | 웹 사이트 | PO로 지급할 수 있는 가장 큰 주문 금액. <br/><br/>**_참고:_**합계가 최소 또는 최대 주문 합계 사이에 있거나 일치하는 경우 주문이 유효합니다. |
| [!UICONTROL Sort Order] | 웹 사이트 | 체크아웃 중에 다른 결제 방법과 함께 나열할 때 PO별 결제 순서를 결정하는 번호가 나타납니다. `0`을(를) 입력하여 목록의 맨 위에 배치합니다. |

{style="table-layout:auto"}
