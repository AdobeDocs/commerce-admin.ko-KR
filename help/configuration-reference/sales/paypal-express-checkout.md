---
title: '[!UICONTROL Sales] &gt; [!UICONTROL Payment Methods] &gt; [!UICONTROL PayPal Express Checkout]'
description: 에서 구성 설정을 검토합니다. [!UICONTROL PayPal Express Checkout] 다음에 대한 섹션 [!UICONTROL Sales] &gt; [!UICONTROL Payment Methods] 상거래 관리자의 페이지입니다.
exl-id: aae5b1d9-f47e-447a-b40c-924f8d2ee824
feature: Configuration, Payments
source-git-commit: 76bd1b1af9b55d69bd98209d70fb5518f190a3e1
workflow-type: tm+mt
source-wordcount: '1735'
ht-degree: 0%

---

# [!UICONTROL Sales] > [!UICONTROL Payment Methods] > [!UICONTROL PayPal Express Checkout]

>[!IMPORTANT]
>
>**PSD2 요구 사항:** <br/>
>2019년 9월 14일부터 유럽 은행들은 충족되지 않는 지불을 거절할 수 있습니다 [PSD2](../../getting-started/compliance-payment-services-directive.md) 요구 사항. 모든 요구 사항이 PayPal에 의해 처리되므로 PayPal Express Checkout에서 PSD2를 준수하는 데 필요한 작업은 없습니다.

{{config}}

## [!UICONTROL Required PayPal Settings]

![PayPal Express 체크아웃 필수 설정](./assets/paypal-express-required-settings.png)<!-- zoom -->

<!-- [PayPal Express Checkout Required Settings](../../stores-purchase/paypal-express-checkout.html) -->

| 필드 | [범위](../../getting-started/websites-stores-views.md#scope-settings) | 설명 |
|--- |--- |--- |
| [!UICONTROL Enable this Solution] | 웹 사이트 | 활성화 [!DNL PayPal Express Checkout] 고객이 사용할 수 있는 결제 수단으로 사용됩니다. 옵션: `Yes` / `No` |
| [!UICONTROL Enable In-Context Checkout Experience] | 웹 사이트 | 고객이 사용할 수 있는 결제 방법으로 간소화된 PayPal In-Context Checkout을 활성화합니다. 옵션: `Yes` / `No` |
| [!UICONTROL Enable PayPal Credit] | 웹 사이트 | 고객이 지금 구매하고 나중에 결제할 수 있도록 PayPal 크레딧을 활성화합니다. 선불은 받지만, 손님들이 낼 시간이 더 많다. 옵션: `Yes` / `No` |

{:style=&quot;table-layout:auto&quot;}

### [!UICONTROL Express Checkout]

| 필드 | [범위](../../getting-started/websites-stores-views.md#scope-settings) | 설명 |
|--- |--- |--- |
| [!UICONTROL Email Associated with PayPal Merchant Account] | 웹 사이트 | PayPal 판매자 계정을 설정할 때 지정한 이메일 주소를 지정합니다. 이메일 주소는 대/소문자를 구분하며, PayPal 시스템의 이메일 주소와 정확히 일치해야 합니다. |
| [!UICONTROL API Authentication Methods] | 웹 사이트 | API 인증에 사용되는 방법을 결정합니다. 옵션: <br/>**`API Signature`**- 다음을 표시합니다. _[!UICONTROL API Signature]_양식의 필드입니다.<br/>**`API Certificate`**- 다음을 표시합니다._[!UICONTROL API Certificate]_ 양식의 필드입니다. |
| [!UICONTROL API Username] | 웹 사이트 | PayPal 판매자 계정과 연결된 API 사용자 이름. |
| [!UICONTROL API Password] | 웹 사이트 | PayPal 판매자 계정과 연결된 API 암호입니다. |
| [!UICONTROL API Signature] | 웹 사이트 | PayPal 판매자 계정과 연결된 API 서명. |
| [!UICONTROL API Certificate] | 웹 사이트 | 이동하여 API 인증서를 업로드합니다. |
| [!UICONTROL Get Credentials from PayPal] |  | Paypal에서 API 자격 증명을 가져옵니다. |
| [!UICONTROL Sandbox Credentials] |  | PayPal에서 샌드박스 자격 증명을 가져옵니다. |
| [!UICONTROL Sandbox Mode] | 웹 사이트 | 테스트 환경에서 PayPal Express Checkout을 실행하려면 샌드박스 API 자격 증명을 입력하고 이를 다음으로 설정하십시오. `Yes`. 옵션: `Yes` / `No` |
| [!UICONTROL API Uses Proxy] | 웹 사이트 | 시스템에서 프록시 서버를 사용하여 Commerce와 PayPal 시스템 간의 연결을 설정하는 경우 이 설정을 로 설정합니다. `Yes`. 옵션: `Yes` / `No` |
| [!UICONTROL Proxy Host] | 웹 사이트 | API에서 프록시를 사용하는 경우 프록시 호스트의 IP 주소를 지정합니다. |
| [!UICONTROL Proxy Port] | 웹 사이트 | API에서 프록시를 사용하는 경우 프록시 호스트에서 사용하는 포트를 지정합니다. |

{:style=&quot;table-layout:auto&quot;}

### [!UICONTROL Advertise PayPal Credit]

![PayPal 크레딧 광고](./assets/payment-methods-paypal-payments-advanced-advertise-paypal-credit.png)<!-- zoom -->

| 필드 | [범위](../../getting-started/websites-stores-views.md#scope-settings) | 설명 |
|--- |--- |--- |
| [!UICONTROL Publisher ID] | 웹 사이트 | PayPal 신용 계정과 연결된 게시자 ID입니다. |
| [!UICONTROL Get Publisher ID from PayPal] |  | PayPal에서 게시자 ID를 가져옵니다. |
| [!UICONTROL Home Page] | 웹 사이트 | 의 위치 및 크기를 결정합니다. [!DNL PayPal Credit] 홈 페이지의 배너. 옵션: <br/>**표시** - 다음을 표시합니다.[!DNL PayPal Credit] 스토어의 홈 페이지에 배너를 추가합니다. 옵션: `Yes` / `No` <br/>**위치** - 의 위치를 결정합니다 [!DNL PayPal Credit] 홈 페이지의 배너. 옵션: 머리글(가운데) / 사이드바(오른쪽) <br/>**크기** - 크기 결정 [!DNL PayPal Credit] 홈 페이지의 배너. 옵션: `190 x 100` / `234 x 60` / `300 x 50` / `468 x 60` / `728 x 90` /` 800 x 66` |
| [!UICONTROL Catalog Category Page] | 웹 사이트 | 의 위치 및 크기를 결정합니다. [!DNL PayPal Credit] 범주 페이지의 배너. 옵션: (과 동일) [!UICONTROL Home Page]) |
| [!UICONTROL Catalog Product Page] | 웹 사이트 | 의 위치 및 크기를 결정합니다. [!DNL PayPal Credit] 제품 페이지의 배너. 옵션: (과 동일) [!UICONTROL Home Page]) |
| [!UICONTROL Checkout Cart Page] | 웹 사이트 | 의 위치 및 크기를 결정합니다. [!DNL PayPal Credit] 장바구니 페이지의 배너. 옵션: (과 동일) [!UICONTROL Home Page]) |

{:style=&quot;table-layout:auto&quot;}

## [!UICONTROL Basic Settings]

![기본 설정](./assets/payment-methods-paypal-express-checkout-basic-settings.png)<!-- zoom -->

| 필드 | [범위](../../getting-started/websites-stores-views.md#scope-settings) | 설명 |
|--- |--- |--- |
| [!UICONTROL Title] | 스토어 뷰 | 체크아웃 중 PayPal Express 체크아웃 결제 방법을 식별하는 이름입니다. |
| [!UICONTROL Sort Order] | 스토어 뷰 | 체크아웃 중에 다른 결제 방법과 함께 나열할 때 PayPal Express Checkout의 순서를 결정하는 번호가 나타납니다. 입력 `0` 목록의 맨 위에. |
| [!UICONTROL Payment Action] | 웹 사이트 | PayPal이 주문을 받으면 수행할 작업을 결정합니다. 옵션: <br/>**`Authorization`**- 구매를 승인하지만 자금을 보류합니다. 상인에게 &#39;포착&#39;되기 전까지는 그 금액이 인출되지 않는다.<br/>**`Sale`** - 구매 금액이 승인되어 즉시 고객의 계좌에서 인출됩니다. <br/>**`Order`**- 머천트가 정의된 기간 내에 고객의 구매자 계정에서 주문된 합계까지 하나 이상의 금액을 캡처할 수 있도록 해주는 PayPal과의 계약을 나타냅니다. 최대 29일이 될 수 있습니다. 자금을 수집하려면 상거래 관리에서 하나 이상의 송장을 생성해야 합니다. |
| [!UICONTROL Display on Product Details Page] | 스토어 뷰 | 제품 페이지에 &quot;PayPal로 체크아웃&quot; 단추가 표시되는지 여부를 결정합니다. 옵션은 다음과 같습니다. `Yes` / `No` |

{:style=&quot;table-layout:auto&quot;}

## [!UICONTROL Advanced Settings]

![고급 설정](./assets/payment-methods-paypal-express-checkout-advanced-settings.png)<!-- zoom -->

| 필드 | [범위](../../getting-started/websites-stores-views.md#scope-settings) | 설명 |
|--- |--- |--- |
| [!UICONTROL Display on Shopping Cart] | 스토어 뷰 | PayPal Express Checkout이 장바구니에서 결제 옵션으로 표시되는지 여부를 결정합니다. 옵션: `Yes` (PayPal 권장) / `No` |
| [!UICONTROL Payment Action Applicable From] | 웹 사이트 | 적용 가능한 국가 선택의 범위를 결정합니다. 옵션: `All Allowed Countries` / `Specific Countries` |
| [!UICONTROL Countries Payment Applicable From] | 웹 사이트 | 지불이 수락되는 각 국가를 식별합니다. 선택한 국가에 청구 주소가 있는 고객만 이 결제 방법으로 구매할 수 있습니다. |
| [!UICONTROL Debug Mode] | 웹 사이트 | 스토어와 결제 시스템 간에 전송된 메시지를 로그 파일에 기록합니다. 옵션: `Yes` / `No` <br/><br/>**_참고:_**로그 파일은 서버에 저장되며 개발자만 액세스할 수 있습니다. PCI 데이터 보안 표준에 따라 신용 카드 정보는 로그 파일에 기록되지 않습니다. |
| [!UICONTROL Enable SSL Verification] | 웹 사이트 | 호스트 보안 인증서를 확인할 수 있도록 합니다. 옵션: `Yes` / `No` |
| [!UICONTROL Transfer Cart Line Items] | 웹 사이트 | PayPal 사이트에 고객 장바구니의 라인 항목에 대한 전체 요약을 표시합니다. 옵션: `Yes` / `No` |
| [!UICONTROL Transfer Shipping Options] | 웹 사이트 | PayPal 사이트에 최대 10개의 배송 옵션이 포함됩니다. 옵션: `Yes` / `No` |
| [!UICONTROL Shortcut Buttons Flavor] | 스토어 뷰 | PayPal 수락 단추에 사용되는 이미지 유형을 결정합니다. 옵션: <br/>**`Dynamic`**- (권장) PayPal 서버에서 동적으로 변경할 수 있는 이미지를 표시합니다.<br/>**`Static`** - 동적으로 변경할 수 없는 정적 이미지를 표시합니다. |
| [!UICONTROL Enable PayPal Guest Checkout] | 웹 사이트 | PayPal 계정이 없는 고객이 PayPal Express Checkout을 사용하여 구매할 수 있도록 허용합니다. 옵션: `Yes` / `No` |
| [!UICONTROL Require Customer's Billing Address] | 웹 사이트 | 고객 청구 주소가 필요한지 여부를 결정합니다. 옵션: `Yes` / `No` / `For Virtual Quotes Only` |
| [!UICONTROL Billing Agreement Signup] | 웹 사이트 | 고객이 을 입력할 수 있는지 여부를 결정합니다. [청구 계약](../../stores-purchase/paypal-billing-agreements.md) 스토어와 함께. 옵션: <br/>**`Auto`**- 고객은 빠른 체크아웃 중에 청구 계약에 등록할 수 있습니다.<br/>**`Ask Customer`** - 고객이 청구 계약에 등록할 것인지 묻는 메시지가 표시됩니다. <br/>**`Never`**- 고객은 결제 계약에 등록할 수 있는 옵션이 제공되지 않습니다. |
| [!UICONTROL Skip Order Review Step] | 웹 사이트 | 고객이 PayPal 사이트에서 거래를 완료할 수 있는지, 아니면 주문을 제출하기 전에 상점으로 돌아가서 주문 검토 단계를 완료해야 하는지 결정합니다. 옵션: `Yes` / `No` |

{:style=&quot;table-layout:auto&quot;}

### [!UICONTROL Billing Agreement Settings]

![청구 계약 설정](./assets/payment-methods-paypal-express-checkout-billing-agreement-settings.png)<!-- zoom -->

| 필드 | [범위](../../getting-started/websites-stores-views.md#scope-settings) | 설명 |
|--- |--- |--- |
| [!UICONTROL Enabled] | 웹 사이트 | 활성화된 경우 결제 계약은 체크아웃 중에 고객에게 결제 옵션으로 표시됩니다. 옵션: `Yes` / `No` |
| [!UICONTROL Title] | 스토어 뷰 | 체크아웃 중 결제 옵션으로 표시되는 PayPal 결제 계약 옵션에 대한 레이블입니다. |
| [!UICONTROL Sort Order] | 스토어 뷰 | 체크아웃 시 청구 계약이 다른 결제 방법과 함께 나열되는 순서를 결정합니다. |
| [!UICONTROL Payment Action] | 웹 사이트 | PayPal이 트랜잭션을 관리하는 방법을 결정합니다. 옵션: <br/>**인증** - 구매를 승인하지만 자금을 보류합니다. 상인에게 &#39;포착&#39;되기 전까지는 그 금액이 인출되지 않는다. <br/>**판매** - 구매 금액이 승인되어 즉시 고객의 계좌에서 인출됩니다. |
| [!UICONTROL Payment Applicable From] | 웹 사이트 | 적용 가능한 국가 선택의 범위를 결정합니다. 옵션: 허용된 모든 국가/특정 국가 |
| [!UICONTROL Countries Payment Applicable From] | 웹 사이트 | 지불이 수락되는 각 국가를 식별합니다. 선택한 국가에 청구 주소가 있는 고객만 이 결제 방법으로 구매할 수 있습니다. |
| [!UICONTROL Debug Mode] | 웹 사이트 | 로그 파일에 결제 시스템과의 통신을 기록합니다. 옵션: `Yes` / `No` <br/><br/>**_참고:_**로그 파일은 서버에 저장되며 개발자만 액세스할 수 있습니다. PCI 데이터 보안 표준에 따라 신용 카드 정보는 로그 파일에 기록되지 않습니다. |
| [!UICONTROL Enable SSL Verification] | 웹 사이트 | 암호화된 SSL 채널을 통해 트랜잭션이 발생하는지 확인하는 단계를 활성화합니다. 옵션: `Yes` / `No` |
| [!UICONTROL Transfer Cart Line Items] | 웹 사이트 | 활성화되면 PayPal 결제 페이지에 장바구니의 라인 항목 요약을 표시합니다. 옵션: `Yes` / `No` |
| [!UICONTROL Allow in Billing Agreement Wizard] | 웹 사이트 | 활성화되면 고객은 고객 계정의 대시보드에서 청구 계약을 시작할 수 있습니다. |

{:style=&quot;table-layout:auto&quot;}

### [!UICONTROL Settlement Report Settings]

![결제 보고서 설정](./assets/payment-methods-paypal-payments-advanced-settlement-report-settings.png)<!-- zoom -->

| 필드 | [범위](../../getting-started/websites-stores-views.md#scope-settings) | 설명 |
|--- |--- |--- |
| **[!UICONTROL SFTP Credentials]** |  |  |
| [!UICONTROL Login] | 웹 사이트 | PayPal의 보안 FTP 서버에 로그인하는 데 필요한 사용자 이름입니다. |
| [!UICONTROL Password] | 웹 사이트 | PayPal의 보안 FTP 서버에 로그인하는 데 필요한 암호입니다. |
| [!UICONTROL Sandbox Mode] | 웹 사이트 | 활성화되면 는 프로덕션 환경에서 &quot;실행&quot;하기 전에 테스트 환경에서 보고서를 실행합니다. 옵션: `Yes` / `No` |
| [!UICONTROL Custom Endpoint Hostname or IP-Address] | 웹 사이트 | 결제 보고서를 관리하는 URL입니다. 기본값: `reports.paypal.com` |
| [!UICONTROL Custom Path] | 웹 사이트 | 서버에 결제 보고서가 저장되는 경로입니다. 기본값: `/ppreports/outgoing` |
| **[!UICONTROL Scheduled Fetching]** |  |  |
| [!UICONTROL Enable Automatic Fetching] | 웹 사이트 | 활성화된 경우 일정에 따라 결제 보고서를 자동으로 가져옵니다. 옵션: `Yes` / `No` |
| [!UICONTROL Schedule] | 웹 사이트 | PayPal에서 결제 보고서를 생성하는 빈도를 결정합니다. 옵션: `Daily` / `Every 3 days` / `Every 7 days` / `Every 10 days` / `Every 14 days` / `Every 30 days` / `Every 40 days` |
| [!UICONTROL Time of Day] | 웹 사이트 | 결제 보고서가 생성되는 시간, 분 및 초를 결정합니다. |

{:style=&quot;table-layout:auto&quot;}

### [!UICONTROL Frontend Experience Settings]

![프론트엔드 경험 설정 - PayPal 판매자 페이지 스타일](./assets/payment-methods-paypal-payments-advanced-frontend-experience-settings1.png)<!-- zoom -->

| 필드 | [범위](../../getting-started/websites-stores-views.md#scope-settings) | 설명 |
|--- |--- |--- |
| [!UICONTROL PayPal Product Logo] | 스토어 뷰 | 스토어에 표시되는 PayPal 로고를 결정합니다. 두 가지 크기의 기본 스타일은 네 가지입니다. 옵션: `No Logo` / `We prefer PayPal (150 x 60)` / `We prefer PayPal (150 x 40)` / `Now accepting PayPal (150 x 60)` / `Now accepting PayPal (150 x 40)` / `Payments by PayPal (150 x 60)` / `Payments by PayPal (150 x 40)` / `Shop now using (150 x 60)` / `Shop now using (150 x 40)` |
| **[!UICONTROL PayPal Merchant Pages Style]** |  |  |
| [!UICONTROL Page Style] | 스토어 뷰 | PayPal 판매자 페이지의 모양을 결정합니다. 허용되는 값: **`paypal`** - PayPal 페이지 스타일을 사용합니다. <br/>**`primary`**- 계정 프로필에서 &quot;기본&quot; 스타일로 식별한 페이지 스타일을 사용합니다.<br/>**`your_custom_value`** - 계정 프로필에 지정된 사용자 정의 결제 페이지 스타일을 사용합니다. |
| [!UICONTROL Header Image URL] | 스토어 뷰 | 체크아웃 페이지의 왼쪽 위 모서리에 표시되는 이미지의 URL입니다. 최대 크기는 750 x 90픽셀입니다. <br/><br/>**_참고:_**PayPal은 이미지가 보안(https) 서버에 저장되도록 권장합니다. 그렇지 않으면 고객의 브라우저가 &quot;페이지에 보안 및 비보안 항목이 모두 포함되어 있습니다.&quot;라고 경고할 수 있습니다. |
| [!UICONTROL Header Image Background Color] | 스토어 뷰 | 자 6 [진수 색상](https://en.wikipedia.org/wiki/Web_colors) 코드: 체크아웃 페이지 머리글의 배경색입니다. 코드를 대문자와 소문자로 입력할 수 있습니다. |
| [!UICONTROL Header Image Border Color] | 스토어 뷰 | 자 6 [진수 색상](https://en.wikipedia.org/wiki/Web_colors) 머리글 주변의 2픽셀 테두리 코드입니다. |
| [!UICONTROL Page Background Color] | 스토어 뷰 | 자 6 [진수 색상](https://en.wikipedia.org/wiki/Web_colors) 머리글 및 결제 양식 뒤에 표시되는 체크아웃 페이지의 배경색에 대한 코드입니다. |

{:style=&quot;table-layout:auto&quot;}

#### [!UICONTROL Customize Smart Buttons (Basic)]

![프론트엔드 경험 설정 - 스마트 단추 사용자 지정](./assets/payment-methods-paypal-payments-advanced-frontend-experience-settings2.png)<!-- zoom -->

| 필드 | [범위](../../getting-started/websites-stores-views.md#scope-settings) | 설명 |
|--- |--- |--- |
| [!UICONTROL Customize Button] | 스토어 보기 | PayPal 스마트 단추를 스토어의 레이아웃과 테마에 맞게 사용자 지정할 수 있는지 여부를 결정합니다. 이러한 변경 사항은 체크아웃 페이지, 제품 페이지, 장바구니 페이지 및 미니 장바구니에서 독립적으로 적용할 수 있습니다. |
| [!UICONTROL Label] | 스토어 보기 | PayPal이 스마트 결제 단추에 표시하는 텍스트입니다. 옵션: <br/>**`Checkout`**(&quot;PayPal Checkout&quot;으로 표시됨)<br/>**`Pay`** (Pay with PayPal로 표시됨) <br/>**`Buy Now`**(&quot;PayPal로 지금 구매&quot;로 표시됨)<br/>**`PayPal`** (PayPal로 표시됨) <br/>**`Installment`**(PayPal로 표시됨)<br/>**`Credit`** (&quot;PayPal CREDIT&quot;으로 표시됨) |
| [!UICONTROL Layout] | 스토어 보기 | PayPal 스마트 단추를 세로 또는 가로로 표시할지를 결정합니다. 옵션: <br/>**`Vertical`**- 구매자는 &quot;게스트 체크아웃 활성화&quot;의 선택 여부와 관계없이 PayPal에 로그인하거나 PayPal 계정을 만들어야 합니다.<br/>**`Horizontal`** - &quot;게스트 체크아웃 활성화&quot;를 선택하면 **`Pay with Debit Card or Credit Card`** PayPal 팝업 창의 단추. 그렇지 않으면 구매자가 PayPal에 로그인하거나 PayPal 계정을 만들어야 합니다. |
| [!UICONTROL Size] | 스토어 보기 | 스마트 결제 단추 크기를 설정합니다. 옵션: <br/>**`Medium`**- 250픽셀 x 35픽셀<br/>**`Large`** - 350픽셀 x 40픽셀 <br/>**`Responsive`**- (기본값) 컨테이너의 너비에 맞게 조정됩니다. 최소 너비는 100픽셀이고 최대 너비는 500픽셀입니다. 높이는 너비에 따라 동적으로 조정됩니다. |
| [!UICONTROL Shape] | 스토어 보기 | 스마트 결제 버튼의 모양을 설정합니다. 옵션: `Pill` (기본값) / `Rectangle` |
| [!UICONTROL Color] | 스토어 보기 | 스마트 결제 버튼의 색상을 설정합니다. 옵션: `Gold` (기본값) / `Blue` / `Silver` / `Black` |

{:style=&quot;table-layout:auto&quot;}

#### [!UICONTROL Customize Smart Buttons (Features)]

![프론트엔드 환경 설정 - 스마트 단추 사용자 지정(기능)](./assets/payment-methods-paypal-payments-advanced-frontend-experience-settings3.png)<!-- zoom -->

| 필드 | [범위](../../getting-started/websites-stores-views.md#scope-settings) | 설명 |
|--- |--- |--- |
| [!UICONTROL Disable Funding Options] | 스토어 보기 | 체크아웃 페이지에 표시되는 다른 PayPal 자금 옵션을 결정합니다. 선택한 옵션은 체크아웃 페이지에 표시되지 않습니다. 선택하지 않은 옵션은 PayPal이 스토어의 통화와 구매자의 위치를 지원하는 경우에만 표시됩니다. 옵션: `PayPal Credit` / `PayPal Guest Checkout` `Credit Card Icons` / `Elektronisches Lastschriftverfahren - German ELV` |

{:style=&quot;table-layout:auto&quot;}
