---
title: Braintree
description: 스토어에서 Braintree을 온라인 결제 솔루션으로 설정하는 방법에 대해 알아봅니다.
exl-id: 781b385f-926e-4047-b7da-6f7c090d75d8
feature: Payments
source-git-commit: fcd08ea5d8c3bd498eb4beae41bdf2f078a89f55
workflow-type: tm+mt
source-wordcount: '2625'
ht-degree: 0%

---

# Braintree

Braintree은 사기 행위 감지 및 PayPal 통합을 통해 완전히 사용자 지정 가능한 체크아웃 경험을 제공합니다. 다음을 지원합니다. [!DNL Apple Pay], [!DNL Google Pay], ACH, Venmo 및 로컬 결제 방법. Braintree은 거래가 Braintree 시스템에서 이루어지기 때문에 가맹점의 PCI 규정 준수 부담을 줄입니다. Braintree 결제 통합은에서 개발합니다. [진커머스](https://www.gene.co.uk/gene-braintree-payments/).

>[!NOTE]
>
>이전 버전의 Adobe Commerce 또는 Commerce Marketplace의 Braintree 확장이 설치된 Magento Open Source에서 2.4.x로 업그레이드하는 경우 다음을 참조하십시오. [2.4 업그레이드 정보](#24-upgrade-notes) 이 페이지의 끝에 있습니다.


## 1단계: Braintree 자격 증명 가져오기

다음으로 이동 [Braintree 결제][1] 계정을 등록합니다.

## 2단계: 기본 설정 완료

1. 다음에서 _관리자_ 사이드바, 이동 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. 왼쪽 패널에서 를 확장합니다. **[!UICONTROL Sales]** 및 선택 **[!UICONTROL Payment Methods]**.

   - Commerce 설치에 여러 웹 사이트, 스토어 또는 보기가 있는 경우 왼쪽 상단 모서리에서 **[!UICONTROL Store View]** 구성이 적용되는 위치입니다.

   - 다음에서 _[!UICONTROL Merchant Location]_섹션, 다음을 확인합니다.**[!UICONTROL Merchant Country]**이 비즈니스 위치로 설정되어 있습니다.

1. 아래 _[!UICONTROL Recommended Solutions]_,_[!UICONTROL Braintree Payments] (기준) [진커머스](https://www.gene.co.uk/gene-braintree-payments/) v4.6.1 - [릴리스 정보](https://support.gene.co.uk/support/solutions/articles/35000228529)_섹션, 클릭&#x200B;**[!UICONTROL Configure]**.

   ![구성 Braintree](./assets/braintree-payments.png){width="600" zoomable="yes"}

1. 대상 **[!UICONTROL Title]**&#x200B;을 클릭하고 체크아웃 중에 Braintree을 결제 옵션으로 식별하는 제목을 입력합니다.

1. 현재 운영 체제 설정 **[!UICONTROL Environment]** Braintree 트랜잭션 대상 `Sandbox` 또는 `Production`

   샌드박스에서 구성을 테스트할 때에는 만 사용하십시오 [신용 카드 번호][2] Braintree에서 권장합니다. Braintree을 사용하여 프로덕션으로 이동할 준비가 되면 다음을 설정합니다. **[!UICONTROL Environment]** 끝 `Production`.

   ![기본 자격 증명 설정](./assets/braintree-settings1.png){width="600" zoomable="yes"}

1. 설정 **[!UICONTROL Payment Action]** 다음 중 하나를 수행합니다.

   - `Authorize Only` - 구매를 승인하고 자금을 보류합니다. 해당 금액은 판매가 이루어질 때까지 고객의 은행 계좌에서 인출되지 않습니다 _캡처됨_ 판매자에 의해.|
   - `Intent Sale`  - 구매 금액이 승인되어 즉시 고객의 계좌에서 인출됩니다. **_참고:_** 이 값은  _승인 및 캡처_ 2.3.x 및 이전 릴리스에서

1. 다음을 입력합니다. **[!UICONTROL Sandbox Merchant ID / Merchant ID]** Braintree 계정에서.

1. Braintree 계정에서 다음 자격 증명을 입력합니다.

   - **[!UICONTROL Sandbox Public Key / Public Key]**
   - **[!UICONTROL Sandbox Private Key / Private Key]**

   >[!NOTE]
   >
   >두 필드에는 각각 다른 필드가 있습니다 **(샌드박스 및 프로덕션)** 환경 및 기타 필드는 선택한 환경에 따라 렌더링됩니다.

1. 구성을 저장하기 전에 **[!UICONTROL Validate Credentials]** 자격 증명의 유효성을 검사합니다.

1. 설정 **[!UICONTROL Enable Card Payments]** 끝 `Yes`.

   ![기본 설정](./assets/braintree-settings2.png){width="600" zoomable="yes"}

   고객이 구매할 때마다 다시 입력할 필요가 없도록 고객 정보를 안전하게 저장하는 기능을 원하는 경우 다음을 설정하십시오. **[!UICONTROL Enable Vault for Card Payments]** 끝 `Yes`.

## 3단계: 고급 설정 완료

1. 확장 ![확장 선택기](../assets/icon-display-expand.png) 다음 **[!UICONTROL Advanced Braintree Settings]** 섹션.

   ![고급 설정](../configuration-reference/sales/assets/payment-methods-braintree-advanced-config.png){width="550" zoomable="yes"}

1. 대상 **[!UICONTROL Vault Title]**&#x200B;를 클릭하고 고객 카드 정보가 저장된 자격 증명 모음을 식별하는 참조용 설명 제목을 입력합니다.

1. 다음을 입력합니다. **[!UICONTROL Merchant Account ID]** Braintree 계정에서.

   사용할 머천트 계정을 지정하지 않으면 Braintree은 기본 머천트 계정을 사용하여 거래를 처리합니다.

1. PayPal, PayLater, Apple Pay 및 Google Pay를 포함하여 체크아웃 프로세스가 시작될 때 빠른 결제 옵션을 통해 체크아웃 경험을 제공하려면 다음을 설정하십시오. **[!UICONTROL Enable Checkout Express Payments]** 끝 `Yes`.

1. 관리자를 통해 주문한 주문에 대해 고급 사기 도구 검사의 일부로 평가를 위해 트랜잭션이 전송되지 않도록 하려면 을 설정합니다. **[!UICONTROL Skip Fraud Checks on Admin Orders]** 끝 `Yes`.

1. 설정 **[!UICONTROL Bypass Fraud Protection Threshold]** 따라서 `Advanced Fraud Protection` 임계값이 충족되거나 초과되면 검사를 건너뜁니다.

   이 필드를 비워 두면 이 옵션이 비활성화됩니다.

1. 시스템이 스토어와 Braintree 간의 상호 작용에 대한 로그 파일을 저장하려면 을 설정합니다. **[!UICONTROL Debug]** 끝 `Yes`.

1. 고객이 신용 카드 뒷면에서 세 자리 보안 코드를 제공하도록 하려면 다음을 설정합니다. **[!UICONTROL CVV Verification]** 끝 `Yes`.

   CVV 인증을 사용하는 경우 _설정/처리 중_ Braintree 섹션에 있는 마지막 항목이 될 필요가 없습니다.

1. 모든 결제 방법에 대해 장바구니 라인 항목을 보내려면 다음을 설정합니다. **[!UICONTROL Send Card Line Items]** 끝 `Yes`.

1. 대상 **[!UICONTROL Credit Card Types]**&#x200B;에서 스토어에서 Braintree 결제로 승인하는 각 신용 카드를 선택합니다.

   여러 카드 유형을 선택하려면 Ctrl 키(PC) 또는 Command 키(Mac)를 누른 채 각 옵션을 클릭합니다.

1. 대상 **[!UICONTROL Sort Order]**&#x200B;을 클릭하고, 체크아웃 중에 다른 결제 방법과 함께 나열할 때 Braintree이 표시되는 순서를 결정하는 숫자를 입력합니다.

## 4단계: Braintree 웹후크 설정 완료

![Braintree 웹후크 설정](../configuration-reference/sales/assets/payment-methods-braintree-webhooks-config.png){width="600" zoomable="yes"}

1. 설정 **[!UICONTROL Enable Webhook]** 끝 `Yes` 사기 방지, ACH 결제 및 로컬 결제 방법을 위한 webhook 기능을 활성화합니다.

1. 에서 URL 복사 **[!UICONTROL Fraud Protection URL]** 필드를 추가하고 Braintree 계정에 을(를) (으)로 추가합니다. _[!UICONTROL Webhook Destination URL]_.

   >[!IMPORTANT]
   >
   >이 URL은 안전하고 공개적으로 액세스할 수 있어야 합니다.

1. 설정 **[!UICONTROL Fraud Protection Approve Order Status]** Braintree이 사기 행위 보호를 승인하는 시기를 결정하는 필드.

   선택한 주문 상태가 상거래 주문에 할당됩니다.

1. 설정 **[!UICONTROL Fraud Protection Reject Order Status]** Braintree이 사기 행위 보호를 거부하는 경우를 결정하는 필드.

   선택한 주문 상태가 상거래 주문에 할당됩니다.

## 5단계: 국가별 설정 완료

1. 설정 **[!UICONTROL Payment from Applicable Countries]** 다음 중 하나를 수행합니다.

   - `All Allowed Countries` - 모든 고객의 고객 [국가](../getting-started/store-details.md#country-options) 스토어 구성에 지정된 경우 이 결제 방법을 사용할 수 있습니다.
   - `Specific Countries` - 이 옵션을 선택한 후 _[!UICONTROL Payment from Specific Countries]_목록이 나타납니다. Ctrl 키(PC) 또는 Command 키(Mac)를 누른 채로 목록에서 고객이 스토어에서 구매할 수 있는 각 국가를 선택합니다.

   ![국가별 설정](../configuration-reference/sales/assets/payment-methods-braintree-country-specific-config.png){width="600" zoomable="yes"}

1. 설정하려면 **[!UICONTROL Country Specific Credit Card Types]**:

   - 클릭 **[!UICONTROL Add]**.

   - 설정 **[!UICONTROL Country]** 각 항목 선택 **[!UICONTROL Allowed Credit Card Type]**.

   - 각 국가에서 수락하는 신용 카드를 식별하려면 이 단계를 반복합니다.

## 6단계: Braintree 설정을 통해 ACH 완료

![ACH 스루 Braintree](../configuration-reference/sales/assets/payment-methods-braintree-ach-config.png){width="600" zoomable="yes"}

1. ACH를 Braintree 결제 옵션으로 포함하려면 다음을 설정합니다. **[!UICONTROL Enable ACH Direct Debit]** 끝 `Yes`.

1. 고객은 일회용 ACH 직불 결제 방법을 보관하고 나중에 사용할 수 있도록 저장할 수 있습니다. 저장되면 고객은 설정된 경우 결제 정보를 다시 입력하거나 인증할 필요 없이 ACH 직불카드를 재사용할 수 있습니다 **[!UICONTROL Enable Vault for ACH Direct Debit]** 끝 `Yes`.

1. 대상 **[!UICONTROL Sort Order]**&#x200B;을 눌러 체크아웃 중에 다른 결제 옵션과 함께 나열될 때 Braintree ACH 결제 옵션이 나타나는 순서를 결정합니다.

## 7단계: [!UICONTROL Apple Pay] Braintree 설정 통과

![Braintree 설정을 통한 ApplePay](../configuration-reference/sales/assets/payment-methods-braintree-applepay-config.png){width="600" zoomable="yes"}

1. 포함할 항목 [!DNL Apple Pay] Braintree을 사용하는 결제 옵션으로 다음을 설정합니다. **[!UICONTROL Enable ApplePay through Braintree]** 끝 `Yes`.

   다음을 확인하십시오. [도메인 이름 확인](https://developer.paypal.com/braintree/docs/guides/apple-pay/configuration/javascript/v3) Braintree 계정에서 먼저 확인하십시오.

1. 고객이 Apple Pay를 사용하여 구매할 때마다 다시 입력할 필요가 없도록 고객 정보를 안전하게 저장할 수 있는 기능을 원하는 경우 다음을 설정하십시오. **[!UICONTROL Enable Vault for ApplePay]** 끝 `Yes`.

1. 설정 **[!UICONTROL Payment Action]** 다음 중 하나를 수행합니다.

   - `Authorize Only` - 구매를 승인하고 자금을 보류합니다. 해당 금액은 판매가 이루어질 때까지 고객의 은행 계좌에서 인출되지 않습니다 _캡처됨_ 상인에 의해.
   - `Intent Sale` - 구매 금액이 승인되어 즉시 고객의 계좌에서 인출됩니다.

1. 대상 **[!UICONTROL Merchant Name]**, Apple 결제 대화 상자에서 고객에게 표시되는 레이블을 지정하는 텍스트를 입력합니다.

1. 대상 **[!UICONTROL Sort Order]**&#x200B;을 클릭하고, 순서를 결정할 숫자를 입력합니다. [!DNL Apple Pay] 결제 옵션은 체크아웃 중에 다른 결제 옵션과 함께 나열되면 나타납니다.

## 8단계: 로컬 결제 방법 설정 완료

1. 로컬 결제 방법을 Braintree 결제 옵션으로 포함하려면 **[!UICONTROL Enable Local Payment Methods]** 끝 `Yes`.

1. 대상 **[!UICONTROL Title]**&#x200B;결제 방법 체크아웃 섹션에 나타나는 레이블에 사용할 텍스트를 입력합니다(기본값: `Local Payments`).

1. 대상 **[!UICONTROL Fallback Button Text]**- 대체 Braintree 페이지에 나타나는 버튼에 사용할 텍스트를 입력하여 고객을 웹 사이트로 다시 안내합니다(예: `Complete Checkout`).

1. 대상 **[!UICONTROL Redirect on Fail]**&#x200B;로컬 결제 방법 트랜잭션이 취소되거나 실패하거나 오류가 발생할 때 고객을 리디렉션해야 하는 URL을 입력합니다. 체크아웃 결제 페이지여야 합니다(예: `https://www.domain.com/checkout#payment`).

1. 대상 **[!UICONTROL Allowed Payment Methods]**&#x200B;을(를) 활성화하려면 로컬 결제 방법을 선택합니다.

   옵션: `Bancontact` / `EPS` / `giropay` / `iDeal` / `Klarna Pay Now` / `SOFORT` / `MyBank` / `P24` / `SEPA/ELV Direct Debit` (아직 지원되지 않음)

   ![로컬 결제 방법 설정](../configuration-reference/sales/assets/payment-methods-braintree-local-payment-config.png){width="600" zoomable="yes"}

   >[!NOTE]
   >
   >번들형 Braintree 확장은 다음에 나열된 모든 로컬 결제 방법을 지원하지 않습니다. [Braintree 개발자 설명서](https://developer.paypal.com/braintree/docs/guides/local-payment-methods/overview). 다른 로컬 결제 방법은 향후 릴리스에서 지원될 예정입니다.

1. 대상 **[!UICONTROL Sort Order]**&#x200B;을 눌러 체크아웃 중에 다른 결제 옵션과 함께 나열될 때 로컬 결제 방법이 표시되는 순서를 결정합니다.

## 9단계: [!DNL Google Pay] Braintree 설정 통과

![Google Braintree 결제](../configuration-reference/sales/assets/payment-methods-braintree-googlepay-config.png){width="600" zoomable="yes"}

1. 포함할 항목 [!DNL Google Pay] Braintree을 사용하는 결제 옵션으로 다음을 설정합니다. **[!UICONTROL Enable GooglePay Through Braintree]** 끝 `Yes`.

1. 고객이 Google Pay를 사용하여 구매할 때마다 다시 입력할 필요가 없도록 고객 정보를 안전하게 저장할 수 있는 기능을 원하는 경우 다음을 설정하십시오. **[!UICONTROL Enable Vault for GooglePay]** 끝 `Yes`.

1. 설정 **[!UICONTROL Payment Action]** 다음 중 하나를 수행합니다.

   - `Authorize Only` - 구매를 승인하고 자금을 보류합니다. 해당 금액은 판매가 이루어질 때까지 고객의 은행 계좌에서 인출되지 않습니다 _캡처됨_ 상인에 의해.
   - `Intent Sale`  - 구매 금액이 승인되어 즉시 고객의 계좌에서 인출됩니다.

1. 설정 **[!UICONTROL Button Color]** 의 색상을 결정하려면 [!DNL Google Pay] 단추: `White` 또는 `Black`

1. 대상 **[!UICONTROL Merchant ID]**&#x200B;을(를) 통해 MerchantID(Google 제공)를 입력합니다.

1. 대상 **[!UICONTROL Accepted Cards]**&#x200B;를 사용하여 주문할 수 있는 카드 유형을 선택합니다. [!DNL Google Pay].

   옵션: `Visa` / `MasterCard` / `AMEX` / `Discover` / `JCB`

1. 대상 **[!UICONTROL Sort Order]**&#x200B;을 클릭하고, 순서를 결정할 숫자를 입력합니다. [!DNL Google Pay] 체크아웃하는 동안 다른 결제 옵션과 함께 나열되면 나타납니다.

## 10단계: Braintree 설정을 통해 Venmo 완료

1. Venmo를 Braintree 결제 옵션으로 포함하려면 다음을 설정하십시오. **[!UICONTROL Enable Venmo through Braintree]** 끝 `Yes`.

1. 설정 **[!UICONTROL Enable Vault for Venmo]** 끝 `Yes` 고객이 향후 트랜잭션을 위해 자신의 Venmo 계정에 다시 로그인할 필요가 없도록 고객의 Venmo 계정을 저장할 수 있는 보안 저장소를 사용할 수 있도록 합니다.

   ![Braintree을 통한 벤](../configuration-reference/sales/assets/payment-methods-braintree-venmo-config.png){width="600" zoomable="yes"}

1. 설정 **[!UICONTROL Payment Action]** 다음 중 하나를 수행합니다.

   - `Authorize Only` - 구매를 승인하고 자금을 보류합니다. 해당 금액은 판매가 이루어질 때까지 고객의 은행 계좌에서 인출되지 않습니다 _캡처됨_ 상인에 의해.
   - `Intent Sale`  - 구매 금액이 승인되어 즉시 고객의 계좌에서 인출됩니다.

1. 대상 **[!UICONTROL Sort Order]**&#x200B;를 클릭하고 체크아웃 중에 다른 결제 옵션과 함께 나열되면 Venmo가 표시되는 순서를 결정하는 숫자를 입력합니다.

## 11단계: Braintree 설정을 통해 PayPal 완료

![Braintree 설정을 통한 PayPal](./assets/braintree-paypal.png){width="550" zoomable="yes"}

1. PayPal을 Braintree 결제 옵션으로 포함하려면 **[!UICONTROL Enable PayPal through Braintree]** 끝 `Yes`.

1. Braintree 결제 방법을 통해 PayPal을 지정하십시오.

   >[!NOTE]
   >
   >다음 중 하나 **[!DNL PayPal Credit]** 또는 **[!DNL PayPal PayLater]** 활성화할 수 있습니다. 두 메서드를 동시에 활성화할 수 없습니다.

   - 포함할 항목 [!DNL PayPal Credit] Braintree을 사용하는 결제 옵션으로 다음을 설정합니다. **[!UICONTROL Enable PayPal Credit through Braintree]** 끝 `Yes`.

     날짜 **Braintree을 통해 PayPal 활성화** 이(가) (으)로 설정됨 `Yes`, 이 필드만 표시됩니다.

     >[!NOTE]
     >
     >PayPal 크레딧은 미국과 영국에서만 사용할 수 있습니다. 에 대해 선택한 값이 있는 경우 PayPal 크레딧이 비활성화됩니다. _[!UICONTROL Merchant Country]_필드가 아님 `US` 또는 `UK`.

   - 포함할 항목 [!DNL PayPal PayLater] Braintree을 사용하는 결제 옵션으로 다음을 설정합니다. **[!UICONTROL Enable PayPal PayLater through Braintree]** 끝 `Yes`.

     날짜 **[!UICONTROL Enable PayPal PayLater through Braintree]** 이(가) (으)로 설정됨 `Yes`, 이 필드만 표시됩니다.

     다음과 같은 오퍼에 대해 사이트에 PayLater 메시지를 표시할 수 있습니다. _3으로 지불_&#x200B;는 고객이 무이자 월 3회 지불로 지불할 수 있도록 해줍니다. Braintree 통합은 이 기능을 홍보하기 위해 사이트에 메시지를 표시할 수 있습니다. 다른 콘텐츠, 마케팅 또는 자료와 함께 PayLater 오퍼를 홍보할 수 없습니다.

1. 대상 **[!UICONTROL Title]**, 체크아웃 중에 PayPal로 결제 Braintree 옵션을 식별하는 제목을 입력합니다.

1. 설정 **[!UICONTROL Vault Enabled]** 끝 `Yes` 고객의 PayPal 계정을 저장할 수 있는 안전한 보관소를 사용할 수 있습니다. 저장된 PayPal 계정은 향후 거래에 사용할 수 있으며, 이렇게 하면 고객의 단계 수가 줄어듭니다.

1. 설정 **[!UICONTROL Send Cart Line Items for PayPal]** 끝 `Yes` 라인 품목(주문 품목)을 PayPal에 기프트 카드, 품목 선물 포장, 주문 선물 포장, 스토어 크레딧, 배송 및 세금과 함께 보낼 수 있습니다.

1. 대상 **[!UICONTROL Sort Order]**&#x200B;을 눌러 체크아웃 중에 다른 결제 옵션과 함께 나열될 때 Braintree PayPal 결제 옵션이 나타나는 순서를 결정합니다.

1. 머천트 이름을 고객에 정의된 것과 다르게 표시하려면 [구성 저장](../getting-started/store-details.md#store-information)에 이름을 입력합니다. **[!UICONTROL Override Merchant Name]** 필드를 표시하려는 대로 선택합니다.

1. 설정 **[!UICONTROL Payment Action]** 다음 중 하나를 수행합니다.

   - `Authorize Only` - 구매를 승인하고 자금을 보류합니다. 해당 금액은 판매가 이루어질 때까지 고객의 은행 계좌에서 인출되지 않습니다 _캡처됨_ 상인에 의해.
   - `Authorize and Capture` - 구매 금액이 승인되어 즉시 고객의 계좌에서 인출됩니다.

1. 설정 **[!UICONTROL Payment from Applicable Countries]** payPal에서 처리한 Braintree 거래에 대해 다음 중 하나를 수행하십시오.

   - `All Allowed Countries` - 모든 고객의 고객 [국가](../getting-started/store-details.md#country-options) 스토어 구성에 지정된 경우 이 결제 방법을 사용할 수 있습니다.
   - `Specific Countries` - 이 옵션을 선택한 후 _[!UICONTROL Payment from Specific Countries]_목록이 나타납니다. Ctrl 키(PC) 또는 Command 키(Mac)를 누른 채로 목록에서 고객이 스토어에서 구매할 수 있는 각 국가를 선택합니다.

1. 고객이 청구 주소를 제공하도록 하려면 다음을 설정합니다. **[!UICONTROL Require Customer's Billing Address]** 끝 `Yes`.

   >[!NOTE]
   >
   >이 기능은 PayPal 기술 지원에서 계정에 대해 활성화해야 합니다.

1. Braintree을 통해 스토어와 PayPal 간의 상호 작용에 대한 로그 파일을 저장하려면 을 설정합니다 **[!UICONTROL Debug]** 끝 `Yes`.

1. 미니 장바구니와 장바구니 페이지 모두에 PayPal 단추를 표시하려면 다음을 설정하십시오. **[!UICONTROL Display on Shopping Cart]** 끝 `Yes`.

## 12단계: 스타일 설정 설정

1. 대상 **[!UICONTROL Location]**, PayPal 단추 및 메시지를 렌더링할 위치를 선택합니다. `Mini-Cart and Cart Page`, `Checkout Page`, 또는 `Product Page`

   ![PayPal 스타일 설정](../configuration-reference/sales/assets/payment-methods-braintree-paypal-styling.png){width="600" zoomable="yes"}

### [!UICONTROL Mini-Cart and Cart Page]

이 섹션의 옵션 및 설정은 의 설정에 따라 다릅니다 _[!UICONTROL Location]_필드.

1. 설정 **[!UICONTROL PayPal Button Type]** 다음 세 가지 유형의 단추 중 하나를 선택합니다. `PayPal Button` / `PayPal Pay Later Button` / `PayPal Credit Button`

**[!UICONTROL PayPal Button]**

이 섹션의 옵션 및 설정은 _[!UICONTROL PayPal Button Type]_필드.

1. 선택한 위치의 상점 전면에서 PayPal 단추를 표시하려면 다음을 설정하십시오. **[!UICONTROL Show PayPal Button]** 끝 `Yes`.

1. 대상 **[!UICONTROL Button Label]**, PayPal 단추 레이블 선택: `Paypal`, `Checkout`, `Buynow`, 또는 `Pay`

1. 대상 **[!UICONTROL Color]**&#x200B;에서 PayPal 단추 색상을 선택합니다. `Blue`, `Black`, `Gold`, 또는 `Silver`

1. 대상 **[!UICONTROL Shape]**&#x200B;에서 PayPal 단추 모양을 선택합니다. `Pill` 또는 `Rectangle`

1. 대상 **[!UICONTROL Size (Deprecated)]**&#x200B;에서 PayPal 단추 크기를 선택합니다. `Medium`, `Large`, 또는 `Responsive`

>[!NOTE]
>
>다음 **[!DNL Size(Deprecated)]** 구성 필드는 더 이상 사용되지 않으며 PayPal 단추 스타일에 사용되지 않습니다.

**[!UICONTROL PayLater Messaging]**

1. 표시 [!DNL PayLater] 선택한 위치의 상점 메시지, 설정 **[!UICONTROL Show PayLater Messaging]** 끝 `Yes`.

   이 메시징에는 다음의 디스플레이가 포함됩니다. [!DNL PayLater] 사용 가능한 오퍼에 대한 메시지([제한 적용](https://developer.paypal.com/docs/checkout/pay-later/us/)).

1. 대상 **[!UICONTROL Message Layout]**&#x200B;를 선택하고 [!DNL PayLater] 메시지 레이아웃: `Text` 또는 `Flex`

1. 대상 **[!UICONTROL Logo]**, PayPal 로고 유형을 선택합니다. `Inline`, `Primary`, `Alternative`, 또는 `None`

1. 대상 **[!UICONTROL Logo Position]**, PayPal 로고 위치를 선택합니다. `Left`, `Right`, 또는 `Top`

1. 대상 **[!UICONTROL Text Color]**&#x200B;를 선택하고 [!DNL PayLater] 메시지 텍스트 색상: `Black`, `White`, `Monochrome`, 또는 `Grayscale`

이러한 옵션이 설정되면 PayPal 버튼과 PayLater 메시지의 미리 보기를 볼 수 있습니다. 설정을 적용하거나 값을 재설정하는 데 사용할 수 있는 컨트롤이 있습니다.

- 단추 및 PayLater 메시지에 대해 선택한 스타일 설정을 저장하고 현재 위치 및 현재 단추 유형에 적용하려면 **[!UICONTROL Apply]**.

- 단추 및 PayLater 메시지 값에 대해 선택한 스타일 설정을 저장하고 모든 단추 유형 및 위치에 적용하려면 **[!UICONTROL Apply to All Buttons]**.

- 단추 및 PayLater 메시지에 대한 권장 기본값으로 스타일 설정을 반환하고 모든 단추 유형 및 위치에 적용하려면 **[!UICONTROL Reset to Recommended Defaults]**.

## 13단계: 3D 확인 설정 완료

1. 인증 프로그램에 등록된 신용 카드를 사용하는 고객에 대한 인증 단계를 추가하려면(예: _VISA에 의해 확인됨_), 설정 **[!UICONTROL 3D Secure Verification]** 끝 `Yes`.

   이 프로세스 중에 검증을 위해 제출된 트랜잭션 금액이 승인을 위해 전송된 금액과 대조됩니다.

2. 모든 트랜잭션에 대해 항상 3D 보안 요청에 도전하려면 다음을 설정합니다. **[!UICONTROL Always request 3DS]** 끝 `Yes`.

3. 대상 **[!UICONTROL Threshold Amount]** 3D 확인을 트리거하는 데 필요한 최소 주문 수량을 입력합니다.

4. 설정 **[!UICONTROL Verify for Applicable Countries]** 다음 중 하나를 수행합니다.

   - `All Allowed Countries` - 모든 고객의 고객 [국가](../getting-started/store-details.md#country-options) 스토어 구성에 지정된 경우 이 결제 방법을 사용할 수 있습니다.
   - `Specific Countries` - 이 옵션을 선택한 후 _[!UICONTROL Verify for Specific Countries]_목록이 나타납니다. Ctrl 키(PC) 또는 Command 키(Mac)를 누른 채로 목록에서 고객이 스토어에서 구매할 수 있는 각 국가를 선택합니다.

   ![3D 확인 설정](../configuration-reference/sales/assets/payment-methods-braintree-3d-secure-verify-config.png){width="600" zoomable="yes"}

## 14단계: Braintree 동적 설명자 설정

다음 설명자는 고객 신용 카드 명세서에서의 구매를 식별하는 데 사용됩니다. 각 구매와 연관된 회사를 명확하게 식별하여 충전의 수를 줄일 수 있습니다. 계정에 대해 동적 설명자가 활성화되지 않은 경우 Braintree 지원 센터에 문의하십시오.

![동적 설명자](../configuration-reference/sales/assets/payment-methods-braintree-dynamic-config.png){width="600" zoomable="yes"}

1. 다음에 대한 동적 설명자 입력 **[!UICONTROL Name]**, **[!UICONTROL Phone]**, 및 **[!UICONTROL URL]** 다음 지침에 따라:

   - **[!UICONTROL Name]** - 이름 설명자에 별표(*)로 구분된 두 부분이 있습니다. For example:

     `company*myproduct`

     설명자의 첫 번째 부분은 회사 또는 DBA를 식별하고 두 번째 부분은 제품을 식별합니다. 의 길이 `company` 및 `product` 설명자의 일부는 최대 22자의 조합 길이에 대해 다음과 같은 방법으로 할당할 수 있습니다.

     **_이름 설명자의 문자_**

     _옵션 1:_ `Company` 은(는) 3자여야 합니다. `Product` 최대 18자까지 가능

     _옵션 2:_ `Company` 은(는) 7자여야 합니다. `Product` 최대 14자까지 가능

     _옵션 3_: `Company` 은(는) 12자여야 하며, `Product` 최대 9자까지 가능

   - **[!UICONTROL Phone]** - 전화 설명자 길이는 10 - 14자여야 하며 숫자, 대시, 괄호 및 마침표만 포함할 수 있습니다. For example:

     `9999999999`

     `(999) 999-9999`

     `999.999.9999`

   - **[!UICONTROL URL]** - URL 설명자는 도메인 이름을 나타내며 최대 13자까지 사용할 수 있습니다. For example:

     `company.com`

1. Braintree 구성이 완료되면 다음을 클릭하십시오. **[!UICONTROL Save Config]**.

## 2.4 업그레이드 정보

Adobe Commerce 및 Magento Open Source 2.4.0부터 Braintree 확장이 릴리스에 포함됩니다. Marketplace Braintree 확장이 설치된 2.4.0 이전 버전에서 Commerce 2.4.x로 마이그레이션하는 경우 해당 확장(`paypal/module-braintree` 또는 `gene/module-braintree`) 및 를 사용하도록 코드 사용자 지정 항목을 업데이트합니다. `PayPal_Braintree` 대신 네임스페이스 사용 `Magento_Braintree`. Commerce Marketplace에 배포된 핵심 상거래 Braintree 결제 번들 확장 기능 및 확장 기능의 구성 설정이 유지되며 이전 버전과 함께 배치된 결제는 정상적으로 캡처, 무효화 또는 환불될 수 있습니다.

[1]: https://www.braintreepayments.com/
[2]: https://developers.braintreepayments.com/reference/general/testing/php
