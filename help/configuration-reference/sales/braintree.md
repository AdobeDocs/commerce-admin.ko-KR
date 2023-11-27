---
title: '[!UICONTROL Sales] &gt; [!UICONTROL Payment Methods] &gt; [!UICONTROL Braintree]'
description: 다음에 대한 구성 설정을 검토합니다. [!UICONTROL Braintree] 다음에 대한 섹션 [!UICONTROL Sales] &gt; [!UICONTROL Payment Methods] 상거래 관리자의 페이지입니다.
exl-id: cf08bc4d-8d88-45e7-af71-f1ff90023766
feature: Configuration, Payments
source-git-commit: 1f84bf9ab20aeccacf56eab396b2778140964d17
workflow-type: tm+mt
source-wordcount: '2330'
ht-degree: 0%

---

# [!UICONTROL Sales] > [!UICONTROL Payment Methods] > [!UICONTROL Braintree]

>[!IMPORTANT]
>
>**Commerce 2.4 마이그레이션:**<br/>
>2.4.0 이전 버전의 Adobe Commerce 및 Magento Open Source의 경우, 판매자는 다음에서 공식 Braintree 결제 통합 확장 기능을 설치하고 구성하는 것이 좋습니다. [Commerce Marketplace](https://marketplace.magento.com/catalogsearch/result/?q=braintree) 핵심 통합을 대체합니다. 2.4.0부터 확장이 이제 코어 릴리스에 포함됩니다.
><br/><br/>
>Commerce 2.4로 마이그레이션할 때 판매자는 Marketplace에 배포된 확장을 제거해야 합니다(`paypal/module-braintree` 또는 `gene/module-braintree`) 및 를 사용하도록 코드 사용자 지정 항목을 업데이트합니다. `PayPal_Braintree` 대신 네임스페이스 사용 `Magento_Braintree`. Commerce용 번들 확장의 구성 설정과 Commerce Marketplace에 배포된 확장이 유지됩니다. 해당 버전의 확장 기능으로 지불된 지불은 정상적으로 캡처, 무효화 또는 환불됩니다.
><br/><br/>
>Commerce 2.4.0으로 업그레이드하고 이전 2.3.x 버전에서 권장 Commerce Marketplace 확장 기능을 사용하지 않는 경우 다중 주소 기능이 2.4.0 버전의 Braintree에서 작동하지 않습니다. 쇼핑객이 선택할 때 _여러 주소에 게재_ 에서 Braintree 결제 방법이 나타나지 않습니다. 이전에 2.3.x에 대해 권장된 Commerce Marketplace 확장에 이 다중 주소 문제가 있습니다.

{{config}}

{{beta2-updates}}

## [!UICONTROL Basic Braintree Settings]

![기본 Braintree 설정](./assets/payment-methods-braintree-basic-config.png)<!-- zoom -->

| 필드 | [범위](../../getting-started/websites-stores-views.md#scope-settings) | 설명 |
|--- |--- |--- |
| [!UICONTROL Title] | 스토어 뷰 | 기본값: `Credit Card` (Braintree) |
| [!UICONTROL Environment] | 스토어 뷰 | 옵션: `Sandbox` / `Production` |
| [!UICONTROL Payment Action] | 스토어 뷰 | 결제가 처리될 때 Braintree이 취하는 조치를 결정합니다. 옵션: <br/>**`Authorize`**- 고객의 신용카드에 있는 자금은 승인되지만 계좌에서 이체되지 않습니다. 주문이 스토어 관리자에서 생성됩니다. 나중에 판매를 캡처하고 송장을 생성할 수 있습니다.<br/>**`Intent Sale`** (이전 `Authorize and Capture` 이전 릴리스) - 고객의 신용 카드에 있는 자금은 Braintree에 의해 승인되고 캡처되며, 주문 및 송장이 상점 관리자에서 생성됩니다. |
| [!UICONTROL Sandbox Merchant ID] | 스토어 뷰 | 전체 샌드박스 게이트웨이 계정에 대한 고유 식별자입니다. (으)로도 알려짐 _공개 ID_ 또는 _프로덕션 ID_, 판매자 ID가 프로덕션 및 샌드박스 게이트웨이에 대해 다릅니다. 이 필드는 다음 경우에 나타납니다. _[!UICONTROL Environment]_필드가 로 설정됨 `Sandbox`. |
| [!UICONTROL Sandbox Public Key] | 스토어 뷰 | 암호화된 데이터에 대한 액세스를 제한하는 사용자별 공용 식별자입니다. 샌드박스 Braintree 게이트웨이와 연결된 각 사용자에게는 고유한 샌드박스 공개 키가 있습니다. 이 필드는 다음 경우에 나타납니다. _[!UICONTROL Environment]_필드가 로 설정됨 `Sandbox`. |
| [!UICONTROL Sandbox Private Key] | 스토어 뷰 | 암호화된 데이터에 대한 액세스를 제한하는 사용자별 개인 식별자입니다. 샌드박스 Braintree 게이트웨이와 연결된 각 사용자에게는 샌드박스에 대한 자체 개인 키가 있습니다. 이 필드는 다음 경우에 나타납니다. _[!UICONTROL Environment]_필드가 로 설정됨 `Sandbox`. |
| [!UICONTROL Merchant ID] | 스토어 뷰 | 게이트웨이에 있을 수 있는 여러 판매자 계정을 포함하여 전체 게이트웨이 계정에 대한 고유 식별자입니다. (으)로도 알려짐 _공개 ID_ 또는 _프로덕션 ID_, 판매자 ID가 프로덕션 및 샌드박스 게이트웨이에 대해 다릅니다. 이 필드는 다음 경우에 나타납니다. _[!UICONTROL Environment]_필드가 로 설정됨 `Production`. |
| [!UICONTROL Public Key] | 스토어 뷰 | 암호화된 데이터에 대한 액세스를 제한하는 사용자별 공용 식별자입니다. Braintree 게이트웨이와 연결된 각 사용자에게는 고유한 공개 키가 있습니다. 이 필드는 다음 경우에 나타납니다. _[!UICONTROL Environment]_필드가 로 설정됨 `Production`. |
| [!UICONTROL Private Key] | 스토어 뷰 | 암호화된 데이터에 대한 액세스를 제한하는 사용자별 개인 식별자입니다. Braintree 게이트웨이와 연결된 각 사용자는 고유한 개인 키를 가집니다. 이 필드는 다음 경우에 나타납니다. _[!UICONTROL Environment]_필드가 로 설정됨 `Production`. |
| [!UICONTROL Enable Card Payments] | 웹 사이트 | 고객이 Braintree 신용카드 결제 방법을 결제 방법으로 사용할 수 있는지 여부를 결정합니다. 옵션: `Yes` / `No` |
| [!UICONTROL Enable Vault for Card Payments] | 웹 사이트 | 활성화하면 은 고객 결제 정보를 위한 안전한 저장소를 제공하므로 고객은 구매 시마다 신용 카드 정보를 다시 입력할 필요가 없습니다. 옵션: `Yes` / `No` |
| [!UICONTROL Enable Vault CVV Reverification] | 웹 사이트 | 활성화하면 Braintree 계정의 CVV 규칙 설정에 대한 유효성 검사가 수행됩니다. 옵션: `Yes` / `No` |

{style="table-layout:auto"}

## [!UICONTROL Advanced Braintree Settings]

![Braintree 고급 설정](./assets/payment-methods-braintree-advanced-config.png){width="550" zoomable="yes"}

| 필드 | [범위](../../getting-started/websites-stores-views.md#scope-settings) | 설명 |
|--- |--- |--- |
| [!UICONTROL Vault Title] | 웹 사이트 | 고객 카드 정보가 저장된 자격 증명 모음을 식별하는 참조용 설명 제목입니다. |
| [!UICONTROL Merchant Account ID] | 웹 사이트 | 이 웹 사이트의 Braintree 거래와 연결할 판매자 계정 ID입니다. 비워 두면 Braintree 계정의 기본 머천트 계정이 사용됩니다. |
| [!UICONTROL Skip Fraud Checks on Admin Orders] | 웹 사이트 | 트랜잭션을 평가의 일부로 보낼 수 없습니다. [!DNL Advanced Fraud Tools] (으)로 설정된 경우에만 관리자를 통해 주문한 주문에 대해 확인 `Yes`.<br/>옵션: `Yes` / `No` |
| [!UICONTROL Bypass Fraud Protection Threshold] | 웹 사이트 | `Advanced Fraud Protection` 임계값이 충족되거나 초과되면 검사를 건너뜁니다. 이 필드를 비워 두면 이 옵션이 비활성화됩니다. |
| [!UICONTROL Debug] | 웹 사이트 | Braintree 시스템과 저장소 간의 통신이 로그 파일에 기록되는지 여부를 결정합니다. 옵션: `Yes` / `No` |
| [!UICONTROL CVV Verification] | 웹 사이트 | 고객이 신용 카드 뒷면에서 세 자리 보안 코드를 제공해야 하는지 여부를 결정합니다. 옵션: `Yes` / `No` |
| [!UICONTROL Send Card Line Items] | 웹 사이트 | 모든 결제 방법에 대한 장바구니 라인 항목을 보냅니다. 옵션: `Yes` / `No` |
| [!UICONTROL Credit Card Types] | 웹 사이트 | Braintree 결제로 수락하는 각 신용 카드를 지정합니다. 길게 누르기 `Ctrl` (또는 `Command` Mac에서)를 클릭하여 카드 조합을 선택합니다. 옵션: `American Express` / `Visa` / `MasterCard` / `Discover` / `JCB` / `Diners` / `Maestro International` |
| [!UICONTROL Sort Order] | 웹 사이트 | 체크아웃 시 Braintree이 다른 결제 방법과 함께 나열되는 순서를 결정합니다. |

## [!UICONTROL Braintree Webhooks Settings]

![Braintree 웹후크 설정](./assets/payment-methods-braintree-webhooks-config.png)<!-- zoom -->

| 필드 | [범위](../../getting-started/websites-stores-views.md#scope-settings) | 설명 |
|--- |--- |--- |
| [!UICONTROL Enable Webhook] | 웹 사이트 | 사기 방지를 위한 웹후크 기능, ACH 결제 및 로컬 결제 방법을 활성화합니다. 옵션: `Yes` / `No` |
| [!UICONTROL Fraud Protection URL] | 웹 사이트 | 이 URL을 Braintree 계정에 다음으로 추가 [!UICONTROL Webhook Destination URL]. **이 URL은 안전하고 공개적으로 액세스할 수 있어야 합니다.** |
| [!UICONTROL Fraud Protection Approve Order Status] | 웹 사이트 | Braintree이 사기 방지를 승인하면 선택한 주문 상태가 상거래 주문에 지정됩니다. 이 상태는 ACH 결제 방법이 사용되는 주문의 상태와 다음으로 이동하는 시기를 업데이트하는 데 사용됩니다. `SETTLED` Braintree. |
| [!UICONTROL Fraud Protection Reject Order Status] | 웹 사이트 | Braintree이 사기 방지를 거부하면 선택한 주문 상태가 상거래 주문에 지정됩니다. 이 상태는 ACH 결제 방법이 사용되는 주문의 상태 및 시기를 업데이트하는 데 사용됩니다. `SETTLEMENT` 은(는) `DECLINED` Braintree. |

{style="table-layout:auto"}

## [!UICONTROL Country Specific Settings]

![국가별 설정](./assets/payment-methods-braintree-country-specific-config.png)<!-- zoom -->

| 필드 | [범위](../../getting-started/websites-stores-views.md#scope-settings) | 설명 |
|--- |--- |--- |
| [!UICONTROL Payment from Applicable Countries] | 웹 사이트 | 모든 국가에서 Braintree으로 처리된 지급을 수락할지 또는 특정 국가에서만 수락할지를 결정합니다. 옵션: `All Allowed Countries` / `Specific Countries` |
| [!UICONTROL Payment from Specific Countries] | 웹 사이트 | 해당하는 경우 는 Braintree에서 처리한 지급을 수락하는 특정 국가를 식별합니다. |
| [!UICONTROL Country Specific Credit Card Types] | 웹 사이트 | Braintree에서 처리한 결제에 대해 국가별로 허용되는 신용 카드를 식별합니다. 각 국가별로 레코드가 저장됩니다. 옵션: <br/>**`Country`**- 국가를 선택합니다.<br/>**`Allowed Card Types`** - 국가에서 Braintree 결제로 수락되는 각 신용 카드를 선택합니다. <br/>**`Add`**- 다른 국가의 신용 카드를 허용하는 줄을 추가합니다.<br/>**`Action`** - 국가에 허용된 신용 카드 기록을 삭제합니다. |

{style="table-layout:auto"}

## [!UICONTROL ACH through Braintree]

![ACH 스루 Braintree](./assets/payment-methods-braintree-ach-config.png)<!-- zoom -->

| 필드 | [범위](../../getting-started/websites-stores-views.md#scope-settings) | 설명 |
|--- |--- |--- |
| [!UICONTROL Enabled ACH Direct Debit] | 웹 사이트 | 다음 여부를 결정합니다. [!DNL ACH Direct Debit] Braintree을 통한 결제 방법으로 포함됩니다. 옵션: `Yes` / `No` |
| [!UICONTROL Sort Order] | 웹 사이트 | 다음 순서를 결정합니다. [!DNL ACH Direct Debit] 체크아웃하는 동안 다른 결제 방법과 함께 나열됩니다. |

{style="table-layout:auto"}

## [!UICONTROL Apple Pay through Braintree]

![Apple Braintree 결제](./assets/payment-methods-braintree-applepay-config.png)<!-- zoom -->

| 필드 | [범위](../../getting-started/websites-stores-views.md#scope-settings) | 설명 |
|--- |--- |--- |
| [!UICONTROL Enable ApplePay through Braintree] | 웹 사이트 | Apple 페이가 Braintree을 통한 결제 수단으로 포함되는지 여부를 결정합니다. 옵션: `Yes` / `No` <br/><br/> 도메인은 다음과 같아야 합니다. [Braintree 계정에서 먼저 확인됨](https://developer.paypal.com/braintree/docs/guides/apple-pay/configuration/javascript/v3). |
| [!UICONTROL Payment Action] | 웹 사이트 | 결제가 처리될 때 Braintree이 취하는 조치를 결정합니다. 옵션: <br/>**`Authorize`**- 고객 카드의 자금이 승인되지만 고객 계정에서 이체되지 않습니다. 주문이 스토어 관리자에서 생성됩니다. 나중에 판매를 캡처하고 송장을 생성할 수 있습니다.<br/>**`Intent Sale`** - 고객 카드의 자금은 Braintree이 승인하고 캡처하며 매장 관리자에서 주문 및 청구서가 생성됩니다. **_참고:_** 이 은(는) `Authorize and Capture` 2.3.x 및 이전 릴리스에서. |
| [!UICONTROL Merchant Name] | 스토어 뷰 | ApplePay 팝업에 고객에게 표시되는 레이블입니다. |
| [!UICONTROL Sort Order] | 웹 사이트 | 체크아웃 시 Apple Pay가 다른 결제 방법과 함께 나열되는 순서를 결정합니다. |

{style="table-layout:auto"}

## [!UICONTROL Local Payment Methods]

![로컬 결제 방법](./assets/payment-methods-braintree-local-payment-config.png)<!-- zoom -->

| 필드 | [범위](../../getting-started/websites-stores-views.md#scope-settings) | 설명 |
|--- |--- |--- |
| [!UICONTROL Enabled Local Payment Methods] | 웹 사이트 | Braintree을 통해 로컬 결제 방법을 결제 방법으로 포함할지 여부를 결정합니다. 옵션: `Yes` / `No` |
| [!UICONTROL Title] | 웹 사이트 | 체크아웃 결제 방법 섹션에 표시되는 레이블입니다. 기본값: `Local Payments` |
| [!UICONTROL Allowed Payment Method] | 웹 사이트 | 사용할 로컬 결제 방법을 선택합니다. 옵션: `Bancontact` / `EPS` / `giropay` / `iDeal` / `Klarna Pay Now` / `SOFORT` / `MyBank` / `P24` / `SEPA/ELV Direct Debit` (아직 지원되지 않음) |
| [!UICONTROL Sort Order] | 웹 사이트 | 체크아웃 시 로컬 결제 방법이 다른 결제 방법과 함께 나열되는 순서를 결정합니다. |

{style="table-layout:auto"}

>[!NOTE]
>
>번들형 Braintree 확장은 다음에 나열된 모든 로컬 결제 방법을 지원하지 않습니다. [Braintree 개발자 설명서](https://developer.paypal.com/braintree/docs/guides/local-payment-methods/overview). 다른 로컬 결제 방법은 향후 릴리스에서 지원될 예정입니다.

## [!UICONTROL GooglePay through Braintree]

![Braintree을 통한 GooglePay](./assets/payment-methods-braintree-googlepay-config.png)<!-- zoom -->

| 필드 | [범위](../../getting-started/websites-stores-views.md#scope-settings) | 설명 |
|--- |--- |--- |
| [!UICONTROL Enabled GooglePay through Braintree] | 웹 사이트 | 다음 여부를 결정합니다. [!DNL Google Pay] Braintree을 통한 결제 수단으로 결제가 포함되어 있다. 옵션: `Yes` / `No` |
| [!UICONTROL Payment Action] | 웹 사이트 | 결제가 처리될 때 Braintree이 취하는 조치를 결정합니다. 옵션: <br/>**`Authorize`**- 고객 카드의 자금이 승인되지만 고객 계정에서 이체되지 않습니다. 주문이 스토어 관리자에서 생성됩니다. 나중에 판매를 캡처하고 송장을 생성할 수 있습니다.<br/>**`Intent Sale`** - 고객 카드의 자금은 Braintree이 승인하고 캡처하며 매장 관리자에서 주문 및 청구서가 생성됩니다. **_참고:_** 이 은(는) `Authorize and Capture` 2.3.x 및 이전 릴리스에서. |
| [!UICONTROL Button Color] | 웹 사이트 | 의 색상을 결정합니다. [!DNL Google Pay] 단추를 클릭합니다. 옵션: `White` / `Black` |
| [!UICONTROL Merchant ID] | 스토어 뷰 | Google에서 제공한 ID를 여기에 입력해야 합니다. |
| [!UICONTROL Accepted Cards] | 웹 사이트 | 고객이 다음을 사용하여 주문하는 데 사용할 수 있는 카드 유형 선택 [!DNL Google Pay]. |
| [!UICONTROL Sort Order] | 웹 사이트 | 체크아웃 시 Google Pay가 다른 결제 방법과 함께 나열되는 순서를 결정합니다. |

{style="table-layout:auto"}

## [!UICONTROL Venmo through Braintree]

![Braintree을 통한 벤](./assets/payment-methods-braintree-venmo-config.png)<!-- zoom -->

| 필드 | [범위](../../getting-started/websites-stores-views.md#scope-settings) | 설명 |
|--- |--- |--- |
| [!UICONTROL Enable Venmo through Braintree] | 웹 사이트 | 다음 여부를 결정합니다. [!DNL Venmo] Braintree을 통한 결제 방법으로 포함됩니다. 옵션: `Yes` / `No` |
| [!UICONTROL Payment Action] | 웹 사이트 | 결제가 처리될 때 Braintree이 취하는 조치를 결정합니다. 옵션: <br/>**`Authorize`**- 고객 카드의 자금이 승인되지만 고객 계정에서 이체되지 않습니다. 주문이 스토어 관리자에서 생성됩니다. 나중에 판매를 캡처하고 송장을 생성할 수 있습니다.<br/>**`Intent Sale`** - 고객 카드의 자금은 Braintree이 승인하고 캡처하며 매장 관리자에서 주문 및 청구서가 생성됩니다. **_참고:_** 이 은(는)  _승인 및 캡처_ 2.3.x 및 이전 릴리스에서. |
| [!UICONTROL Sort Order] | 웹 사이트 | 체크아웃 시 Venmo가 다른 결제 방법과 함께 나열되는 순서를 결정합니다. |

{style="table-layout:auto"}

## [!UICONTROL PayPal through Braintree]

![PayPal 스루 Braintree](./assets/payment-methods-braintree-paypal-config.png){width="550" zoomable="yes"}

| 필드 | [범위](../../getting-started/websites-stores-views.md#scope-settings) | 설명 |
|--- |--- |--- |
| [!UICONTROL Enable PayPal through Braintree] | 웹 사이트 | PayPal이 Braintree을 통해 결제 방법으로 포함되는지 여부를 결정합니다. 옵션: `Yes` / `No` |
| [!UICONTROL Enable PayPal Credit through Braintree] | 웹 사이트 | Braintree을 통해 결제 방법으로 PayPal 크레딧이 포함되는지 여부를 결정합니다. 옵션: `Yes` / `No`. 이 필드는 다음 경우에 표시됩니다. `Enable PayPal through Braintree` 이(가) (으)로 설정됨 `Yes` |
| [!UICONTROL Enable PayPal PayLater through Braintree] | 웹 사이트 | PayPal PayLater가 Braintree을 통해 결제 수단으로 포함되는지 여부를 결정합니다. 옵션: `Yes` / `No`. 이 필드는 다음 경우에 표시됩니다. `Enable PayPal through Braintree` 이(가) (으)로 설정됨 `Yes` |
| [!UICONTROL Title] | 스토어 뷰 | 체크아웃 중에 고객에게 Braintree을 통해 PayPal을 식별하는 레이블입니다. 기본값: `PayPal` |
| [!UICONTROL Vault Enabled] | 웹 사이트 | 활성화하면 은 고객 결제 정보를 위한 안전한 저장소를 제공하므로 고객은 구매 시마다 자신의 PayPal 정보를 다시 입력할 필요가 없습니다. 옵션: `Yes` / `No` |
| [!UICONTROL Sort Order] | 웹 사이트 | 체크아웃 시 PayPal through Braintree이 다른 결제 방법과 함께 나열되는 순서를 결정하는 숫자입니다. |
| [!UICONTROL Override Merchant Name] | 스토어 뷰 | 각 스토어 조회수에 대해 판매자를 식별하는 데 사용할 수 있는 대체 이름. |
| [!UICONTROL Payment Action] | 웹 사이트 | 지불이 처리될 때 Braintree을 통해 PayPal이 취하는 조치를 결정합니다. 옵션: <br/>**`Authorize`**- 고객 카드의 자금이 승인되지만 고객 계정에서 이체되지 않습니다. 주문이 스토어 관리자에서 생성됩니다. 나중에 판매를 캡처하고 송장을 생성할 수 있습니다.<br/>**`Authorize and Capture`** - 고객 카드의 자금은 Braintree을 통해 PayPal에 의해 승인되고 캡처되며, 주문 및 송장은 매장 관리자에서 생성됩니다. |
| [!UICONTROL Payment from Applicable Countries] | 웹 사이트 | 모든 국가의 Braintree을 통해 PayPal에서 처리한 결제를 수락할지 또는 특정 국가에서만 결제할지 결정합니다. 옵션: `All Allowed Countries` / `Specific Countries` |
| [!UICONTROL Payment from Specific Countries] | 웹 사이트 | 해당하는 경우 는 Braintree에서 처리한 지급을 수락하는 특정 국가를 식별합니다. |
| [!UICONTROL Require Customer's Billing Address] | 웹 사이트 | 주문을 제출하는 데 고객의 청구 주소가 필요한지 여부를 결정합니다. 옵션: `Yes` / `No` |
| [!UICONTROL Debug] | 웹 사이트 | Braintree 시스템을 통한 PayPal과 저장소 간의 통신이 로그 파일에 기록되는지 여부를 결정합니다. 옵션: `Yes` / `No` |
| [!UICONTROL Display on Shopping Cart] | 웹 사이트 | PayPal 단추가 [미니 카트](../../stores-purchase/cart-configuration.md#mini-cart) 및 [장바구니](../../stores-purchase/cart.md) 페이지를 가리키도록 업데이트하는 중입니다. 옵션: `Yes` / `No` |

{style="table-layout:auto"}

### [!UICONTROL Styling]

![PayPal 스타일](./assets/payment-methods-braintree-paypal-styling.png)<!-- zoom -->

| 필드 | [범위](../../getting-started/websites-stores-views.md#scope-settings) | 설명 |
|--- |--- |--- |
| [!UICONTROL Location] | 웹 사이트 | 상점 첫 화면에서 PayPal 단추 및 메시지를 렌더링할 위치를 결정합니다. 옵션: `Mini-Cart and Cart Page` / `Checkout Page` / `Product Page` |

{style="table-layout:auto"}

**[!UICONTROL Mini-Cart and Cart Page]**

이 섹션의 옵션 및 설정은 의 설정에 따라 다릅니다. _[!UICONTROL Location]_필드.

| 필드 | [범위](../../getting-started/websites-stores-views.md#scope-settings) | 설명 |
|--- |--- |--- |
| [!UICONTROL PayPal Button Type] | 웹 사이트 | 버튼을 다음 세 가지 유형 중 하나로 설정합니다. `PayPal Button` / `PayPal Pay Later Button` / `PayPal Credit Button` |

**[!UICONTROL PayPal Button]**

이 섹션의 옵션 및 설정은 _[!UICONTROL PayPal Button Type]_필드.

| 필드 | [범위](../../getting-started/websites-stores-views.md#scope-settings) | 설명 |
|--- |--- |--- |
| [!UICONTROL Show PayPal Button] | 웹 사이트 | 선택한 위치에서 PayPal 단추의 위치를 결정합니다. 옵션: `Yes` / `No` |
| [!UICONTROL Button Label] | 웹 사이트 | PayPal 단추의 레이블을 결정합니다. 옵션: `Paypal` / `Checkout` / `Buy Now` / `Pay` |
| [!UICONTROL Color] | 웹 사이트 | PayPal 단추의 색상을 결정합니다. 옵션: `Blue` / `Black` / `Gold` / `Silver` |
| [!UICONTROL Shape] | 웹 사이트 | PayPal 단추의 모양을 결정합니다. 옵션: `Pill` / `Rectangle` |
| [!UICONTROL Size] | 웹 사이트 | PayPal 단추의 크기를 결정합니다. 옵션: `Medium` / `Large` / `Responsive` |

{style="table-layout:auto"}

**[!UICONTROL PayLater Messaging]**

| 필드 | [범위](../../getting-started/websites-stores-views.md#scope-settings) | 설명 |
|--- |--- |--- |
| [!UICONTROL Show PayLater Messaging] | 웹 사이트 | 선택한 위치에서 PayLater 메시지를 활성화합니다. 옵션: `Yes` / `No`. 활성화되면 사용 가능한 오퍼에 대한 PayLater 메시지를 표시합니다([제한 적용](https://developer.paypal.com/docs/checkout/pay-later/us/)). |
| [!UICONTROL Message Layout] | 웹 사이트 | PayLater 메시지 레이아웃을 결정합니다. 옵션: `Text` / `Flex` |
| [!UICONTROL Logo] | 웹 사이트 | PayPal 단추에 사용되는 로고 유형을 결정합니다. 옵션: `Inline` / `Primary` / `Alternative` / `None` |
| [!UICONTROL Logo Position] | 웹 사이트 | PayPal 단추의 로고 위치를 결정합니다. 옵션: `Left` / `Right` / `Top` |
| [!UICONTROL Text Color] | 웹 사이트 | PayPal 단추의 텍스트 색을 결정합니다. 옵션: `Black` / `White` / `Monochrome` / `Grayscale` |

{style="table-layout:auto"}

이러한 옵션이 설정되면 PayPal 버튼과 PayLater 메시지의 미리 보기를 볼 수 있습니다. 설정을 적용하거나 값을 재설정하는 데 사용할 수 있는 컨트롤이 있습니다.

| 필드 | [범위](../../getting-started/websites-stores-views.md#scope-settings) | 설명 |
|--- |--- |--- |
| [!UICONTROL Apply] | 웹 사이트 | 단추 및 PayLater 메시지에 대해 선택한 스타일 설정을 저장하고 현재 위치 및 현재 단추 유형에 적용합니다. |
| [!UICONTROL Apply to All Buttons] | 웹 사이트 | 단추 및 PayLater 메시지 값에 대해 선택한 스타일 설정을 저장하고 모든 단추 유형 및 위치에 적용합니다. |
| [!UICONTROL Reset to Recommended Defaults] | 웹 사이트 | 단추 및 PayLater 메시지에 대한 권장 기본값으로 스타일 설정을 반환하고 모든 단추 유형 및 위치에 적용합니다. |

{style="table-layout:auto"}

## 3d 보안 확인 설정

![3D 보안 확인 설정](./assets/payment-methods-braintree-3d-secure-verify-config.png)<!-- zoom -->

| 필드 | [범위](../../getting-started/websites-stores-views.md#scope-settings) | 설명 |
|--- |--- |--- |
| [!UICONTROL 3D Secure Verification] | 웹 사이트 | 고객이 프로그램에 등록될 때 트랜잭션이 추가 확인 프로세스를 통과해야 하는지 여부를 결정합니다. _VISA에 의해 확인됨_. 옵션: `Yes` / `No` |
| [!UICONTROL Always request 3DS] | 웹 사이트 | 모든 트랜잭션에 대해 항상 3D 보안 요청에 도전합니다. 옵션: `Yes` / `No` |
| [!UICONTROL Threshold Amount] | 웹 사이트 | 단일 주문에서 처리하도록 승인된 최대 주문 금액을 결정합니다. Braintree은 주문 금액이 이 임계값 금액을 초과하는 경우 승인을 거부합니다. |
| [!UICONTROL Verify for Applicable Countries] | 웹 사이트 | 결제를 확인해야 하는 국가를 결정합니다. 옵션: `All Allowed Countries` / `Specific Countries` |
| [!UICONTROL Verify for Specific Countries] | 웹 사이트 | 해당하는 경우 Braintree 결제를 확인해야 하는 특정 국가를 식별합니다. |

{style="table-layout:auto"}

## [!UICONTROL Dynamic Descriptors]

![동적 설명자](./assets/payment-methods-braintree-dynamic-config.png)<!-- zoom -->

| 필드 | [범위](../../getting-started/websites-stores-views.md#scope-settings) | 설명 |
|--- |--- |--- |
| [!UICONTROL Name] | 스토어 뷰 | 이름 설명자에는 별표(*)로 구분된 두 부분이 있습니다. 설명자의 첫 번째 부분은 회사 또는 DBA를 식별하고 두 번째 부분은 제품을 식별합니다. 예: `company*myproduct`  <br/><br/>설명자의 회사 및 제품 부분의 길이는 최대 22자의 조합 길이에 대해 다음과 같은 방법으로 할당할 수 있습니다. <br/>**`Option 1`**- 회사는 3자여야 하며 제품은 최대 18자까지 사용할 수 있습니다.<br/>**`Option 2`** - 회사는 7자여야 하며 / 제품은 최대 14자까지 사용할 수 있습니다. <br/>**`Option 3`**- 회사는 12자여야 하며 제품은 최대 9자까지 사용할 수 있습니다. |
| [!UICONTROL Phone] | 스토어 뷰 | 전화 설명자 길이는 10~14자여야 하며 숫자, 대시, 괄호 및 마침표만 포함할 수 있습니다. For example: `9999999999` `(999) 999-9999` `999.999.9999` |
| [!UICONTROL URL] | 스토어 뷰 | URL 설명자는 도메인 이름을 나타내며 최대 13자까지 사용할 수 있습니다. For example: `company.com` |

{style="table-layout:auto"}
