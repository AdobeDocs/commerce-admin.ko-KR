---
title: '[!UICONTROL Sales] &gt; [!UICONTROL Payment Methods] &gt; [!UICONTROL PayPal Payments Standard]'
description: Commerce 관리자의 [!UICONTROL Sales] &gt; [!UICONTROL Payment Methods] 페이지에서 [!UICONTROL PayPal Payments Standard] 섹션의 구성 설정을 검토하십시오.
exl-id: 846d9b6f-92b9-4610-b894-625f67f4cff8
feature: Configuration, Payments
source-git-commit: b710c0368dc765e3bf25e82324bffe7fb8192dbf
workflow-type: tm+mt
source-wordcount: '1291'
ht-degree: 0%

---

# [!UICONTROL Sales] > [!UICONTROL Payment Methods] > [!UICONTROL PayPal Payments Standard]

>[!IMPORTANT]
>
>**PSD2 요구 사항:**<br/>
>2019년 9월 14일부터 유럽 은행은 [PSD2](../../getting-started/compliance-payment-services-directive.md) 요구 사항을 충족하지 않는 결제를 거절할 수 있습니다. 모든 요구 사항은 PayPal로 처리되므로 [!DNL PayPal Payments Standard]이(가) PSD2를 준수하는 데 필요한 작업은 없습니다.

{{config}}

## [!UICONTROL Required Settings]

![필수 설정](./assets/payment-methods-paypal-payments-standard-required.png)<!-- zoom -->

| 필드 | [범위](../../getting-started/websites-stores-views.md#scope-settings) | 설명 |
|--- |--- |--- |
| [!UICONTROL Email Associated with PayPal Merchant Account] | 웹 사이트 | (선택 사항) PayPal 판매자 계정과 연결된 모든 이메일 주소. 이메일 주소는 대소문자를 구분하며, 계정에 있는 주소와 정확히 일치해야 합니다. |
| [!UICONTROL Partner] | 웹 사이트 | 해당되는 경우 PayPal 파트너 ID입니다. |
| [!UICONTROL Vendor] | 웹 사이트 | PayPal 사용자 로그인 이름입니다. |
| 사용자 | 웹 사이트 | PayPal 계정에 있는 다른 사용자의 ID. |
| [!UICONTROL Password] | 웹 사이트 | PayPal 판매자 계정과 연결된 암호입니다. |
| [!UICONTROL Test Mode] | 웹 사이트 | 활성화되면 은 테스트 환경에서 PayPal Payments Pro를 실행합니다. 프로덕션 모드에서 &quot;실행&quot;할 준비가 되면 테스트 모드를 끕니다. 옵션: `Yes` / `No` |
| [!UICONTROL Use Proxy] | 웹 사이트 | 서버 방화벽이 PayPal 서버에 대한 직접 액세스를 차단하는 경우 프록시를 사용하여 트래픽을 리디렉션할 수 있습니다. 해당하는 경우 는 PayPal 서버와의 연결을 설정하는 데 사용되는 프록시 서버를 식별합니다. 옵션: `Yes` / `No` <br/><br/>활성화된 경우 옵션: <br/>**`Proxy Host`**- 프록시 호스트의 IP 주소를 설정하십시오.<br/>**`Proxy Port`** - 프록시 포트의 수입니다. |
| [!UICONTROL Enable this Solution] | 웹 사이트 | 고객이 PayPal Payments Pro를 결제 방법으로 사용할 수 있는지 여부를 결정합니다. |
| [!UICONTROL Enable PayPal Credit] | 웹 사이트 | 고객이 PayPal 크레딧을 결제 옵션으로 사용할 수 있는지 여부를 결정합니다. |

{style="table-layout:auto"}

## PayPal 크레딧 광고

![PayPal 크레딧 알림](./assets/payment-methods-paypal-payments-advanced-advertise-paypal-credit.png)<!-- zoom -->

| 필드 | [범위](../../getting-started/websites-stores-views.md#scope-settings) | 설명 |
|--- |--- |--- |
| [!UICONTROL Publisher ID] | 웹 사이트 | PayPal 신용 계정과 연결된 게시자 ID입니다. |
| [!UICONTROL Get Publisher ID from PayPal] |  | PayPal에서 게시자 ID를 가져옵니다. |
| [!UICONTROL Home Page] | 웹 사이트 | 홈 페이지에서 [!DNL PayPal Credit] 배너의 위치와 크기를 결정합니다. 옵션: <br/>**`Display`**- 스토어의 홈 페이지에 [!DNL PayPal Credit] 배너가 표시되는지 여부를 결정합니다. 옵션: `Yes` / `No`<br/>**`Position`** - 홈 페이지에서 [!DNL PayPal Credit] 배너의 위치를 결정합니다. 옵션: `Header (center)` / `Sidebar (right)` <br/>**`Size`**- 홈 페이지에서 [!DNL PayPal Credit] 배너의 크기를 결정합니다. 옵션: `190 x 100` / `234 x 60` / `300 x 50` / `468 x 60` / `728 x 90` /` 800 x 66` |
| [!UICONTROL Catalog Category Page] | 웹 사이트 | 범주 페이지에서 [!DNL PayPal Credit] 배너의 위치와 크기를 결정합니다. 옵션: ([!UICONTROL Home Page]과(와) 동일) |
| [!UICONTROL Catalog Product Page] | 웹 사이트 | 제품 페이지에서 [!DNL PayPal Credit] 배너의 위치와 크기를 결정합니다. 옵션: ([!UICONTROL Home Page]과(와) 동일) |
| [!UICONTROL Checkout Cart Page] | 웹 사이트 | 장바구니 페이지에서 [!DNL PayPal Credit] 배너의 위치와 크기를 결정합니다. 옵션: ([!UICONTROL Home Page]과(와) 동일) |

{style="table-layout:auto"}

## [!UICONTROL Basic Settings - PayPal Payments Standard]

![기본 설정](./assets/paypal-standard-basic-settings.png)<!-- zoom -->

| 필드 | [범위](../../getting-started/websites-stores-views.md#scope-settings) | 설명 |
|--- |--- |--- |
| [!UICONTROL Title] | 스토어 뷰 | 체크아웃 시 결제 수단으로 PayPal Payments Pro를 식별하는 이름입니다. |
| [!UICONTROL Sort Order] | 스토어 뷰 | 체크아웃 중에 다른 결제 방법과 함께 나열할 때 PayPal Payments Pro가 표시되는 순서를 결정하는 숫자입니다. |
| [!UICONTROL Payment Action] | 웹 사이트 | 주문이 제출될 때 PayPal에서 취하는 조치를 결정합니다. 옵션: <br/>**`Authorization`**- 구매를 승인하지만 자금을 보류합니다. 상인에게 &#39;포착&#39;되기 전까지는 그 금액이 인출되지 않는다.<br/>**`Sale`** - 구매 금액이 승인되어 고객 계정에서 즉시 인출됩니다. |
| [!UICONTROL Credit Card Settings] |  |  |
| [!UICONTROL Allowed Credit Cart Types] | 웹 사이트 | 체크아웃 중에 고객이 사용할 수 있는 신용 카드를 결정합니다. 지원되는 카드를 각각 선택하십시오. 옵션: `American Express`(추가 계약 필요) / `Visa` / `MasterCard` / `Discover` / `JCB` |

{style="table-layout:auto"}

## [!UICONTROL Advanced Settings]

![고급 설정](./assets/payment-methods-paypal-payment-standard-advanced.png)<!-- zoom -->

| 필드 | 범위 | 설명 |
|--- |--- |--- |
| [!UICONTROL Display on Shopping Cart] | 스토어 뷰 | PayPal Express Checkout이 장바구니에서 결제 옵션으로 표시되는지 여부를 결정합니다. 옵션: `Yes`(권장) / `No` |
| [!UICONTROL Payment Action Applicable From] | 웹 사이트 | 적용 가능한 국가 선택의 범위를 결정합니다. 옵션: `All Allowed Countries` / `Specific Countries` |
| [!UICONTROL Countries Payment Applicable From] | 웹 사이트 | 지불이 수락되는 각 국가를 식별합니다. 선택한 국가에 청구 주소가 있는 고객만 이 결제 방법으로 구매할 수 있습니다. |
| [!UICONTROL Debug Mode] | 웹 사이트 | 스토어와 PayPal 결제 시스템 간에 전송된 메시지를 로그 파일에 기록합니다. 옵션: `Yes` / `No` <br/><br/>**_참고:_**&#x200B;로그 파일은 서버에 저장되며 개발자만 액세스할 수 있습니다. PCI 데이터 보안 표준에 따라 신용 카드 정보는 로그 파일에 기록되지 않습니다. |
| [!UICONTROL Enable SSL Verification] | 웹 사이트 | 호스트 보안 인증서를 확인할 수 있도록 합니다. 옵션: `Yes` / `No` |
| [!UICONTROL Transfer Cart Line Items] | 웹 사이트 | PayPal 사이트에 고객 장바구니의 라인 항목에 대한 전체 요약을 표시합니다. 옵션: `Yes` / `No` |
| [!UICONTROL Transfer Shipping Options] | 웹 사이트 | PayPal 사이트에 최대 10개의 배송 옵션이 포함됩니다. 옵션: `Yes` / `No` |
| [!UICONTROL Shortcut Buttons Flavor] | 스토어 뷰 | PayPal 수락 단추에 사용되는 이미지 유형을 결정합니다. 옵션: <br/>**`Dynamic`**- (권장) PayPal 서버에서 동적으로 변경할 수 있는 이미지를 표시합니다.<br/>**`Static`** - 동적으로 변경할 수 없는 정적 이미지를 표시합니다. |
| [!UICONTROL Enable PayPal Guest Checkout] | 웹 사이트 | PayPal 계정이 없는 고객이 PayPal Express Checkout을 사용하여 구매할 수 있도록 허용합니다. 옵션: `Yes` / `No` |
| [!UICONTROL Require Customer's Billing Address] | 웹 사이트 | 고객 청구 주소가 필요한지 여부를 결정합니다. 옵션: `Yes` / `No` / `For Virtual Quotes Only` |
| [!UICONTROL Billing Agreement Signup] | 웹 사이트 | 고객이 스토어와 [청구 계약](../../stores-purchase/paypal-billing-agreements.md)을 체결할 수 있는지 여부를 결정합니다. 옵션: <br/>**`Auto`**- 고객은 빠른 체크아웃 중에 청구 계약에 등록할 수 있습니다.<br/>**`Ask Customer`** - 고객이 청구 계약에 등록할 것인지 묻는 메시지가 표시됩니다. <br/>**`Never`**- 고객은 결제 계약에 등록할 수 있는 옵션이 제공되지 않습니다. |
| [!UICONTROL Skip Order Review Step] | 웹 사이트 | 고객이 PayPal 사이트에서 거래를 완료할 수 있는지, 아니면 주문을 제출하기 전에 상점으로 돌아가서 주문 검토 단계를 완료해야 하는지 결정합니다. 옵션: `Yes` / `No` |

{style="table-layout:auto"}

## [!UICONTROL Billing Agreement Setting]

![결제 계약 설정](./assets/payment-methods-paypal-express-checkout-billing-agreement-settings.png)<!-- zoom -->

| 필드 | 범위 | 설명 |
|--- |--- |--- |
| [!UICONTROL Enabled] | 웹 사이트 | 활성화된 경우 결제 계약은 체크아웃 중에 고객에게 결제 옵션으로 표시됩니다. 옵션: `Yes` / `No` |
| [!UICONTROL Title] | 스토어 뷰 | 체크아웃 중 결제 옵션으로 표시되는 PayPal 결제 계약 옵션에 대한 레이블입니다. |
| [!UICONTROL Sort Order] | 스토어 뷰 | 체크아웃 시 청구 계약이 다른 결제 방법과 함께 나열되는 순서를 결정합니다. |
| [!UICONTROL Payment Action] | 웹 사이트 | PayPal이 거래를 관리하는 방법을 결정합니다. 옵션: <br/>**`Authorization`**- 구매를 승인하지만 자금을 보류합니다. 상인에게 &#39;포착&#39;되기 전까지는 그 금액이 인출되지 않는다.<br/>**`Sale`** - 구매 금액이 승인되어 고객 계정에서 즉시 인출됩니다. |
| [!UICONTROL Payment Applicable From] | 웹 사이트 | 적용 가능한 국가 선택의 범위를 결정합니다. 옵션: `All Allowed Countries` / `Specific Countries` |
| [!UICONTROL Countries Payment Applicable From] | 웹 사이트 | 지불이 수락되는 각 국가를 식별합니다. 선택한 국가에 청구 주소가 있는 고객만 이 결제 방법으로 구매할 수 있습니다. |
| [!UICONTROL Debug Mode] | 웹 사이트 | 로그 파일에 결제 시스템과의 통신을 기록합니다. 옵션: `Yes` / `No` <br/><br/>**_참고:_**&#x200B;로그 파일은 서버에 저장되며 개발자만 액세스할 수 있습니다. PCI 데이터 보안 표준에 따라 신용 카드 정보는 로그 파일에 기록되지 않습니다. |
| [!UICONTROL Enable SSL Verification] | 웹 사이트 | 암호화된 SSL 채널을 통해 트랜잭션이 발생하는지 확인하는 단계를 활성화합니다. 옵션: `Yes` / `No` |
| [!UICONTROL Transfer Cart Line Items] | 웹 사이트 | 활성화되면 PayPal 결제 페이지에 장바구니의 라인 항목 요약을 표시합니다. 옵션: `Yes` / `No` |
| [!UICONTROL Allow in Billing Agreement Wizard] | 웹 사이트 | 활성화되면 고객은 고객 계정의 대시보드에서 청구 계약을 시작할 수 있습니다. |

{style="table-layout:auto"}

## [!UICONTROL Settlement Report Settings]

![결제 보고서 설정](./assets/payment-methods-paypal-payments-advanced-settlement-report-settings.png)<!-- zoom -->

| 필드 | [범위](../../getting-started/websites-stores-views.md#scope-settings) | 설명 |
|--- |--- |--- |
| [!UICONTROL Login] | 웹 사이트 | PayPal의 보안 FTP 서버에 로그인하는 데 필요한 사용자 이름입니다. |
| [!UICONTROL Password] | 웹 사이트 | PayPal의 보안 FTP 서버에 로그인하는 데 필요한 암호입니다. |
| [!UICONTROL Sandbox Mode] | 웹 사이트 | 활성화되면 는 프로덕션 환경에서 &quot;실행&quot;하기 전에 테스트 환경에서 보고서를 실행합니다. 옵션: `Yes` / `No` |
| [!UICONTROL Custom Endpoint Hostname or IP-Address] | 웹 사이트 | 결제 보고서를 관리하는 URL입니다. 기본값: `reports.paypal.com` |
| [!UICONTROL Custom Path] | 웹 사이트 | 서버에 결제 보고서가 저장되는 경로입니다. 기본값: `/ppreports/outgoing` |
| [!UICONTROL Scheduled Fetching] |  |  |
| [!UICONTROL Enable Automatic Fetching] | 웹 사이트 | 활성화된 경우 일정에 따라 결제 보고서를 자동으로 가져옵니다. 옵션: `Yes` / `No` |
| [!UICONTROL Schedule] | 글로벌 | PayPal에서 결제 보고서를 생성하는 빈도를 결정합니다. 옵션: `Daily` / `Every 3 days` / `Every 7 days` / `Every 10 days` / `Every 14 days` / `Every 30 days` / `Every 40 days` |
| [!UICONTROL Time of Day] | 글로벌 | 결제 보고서가 생성되는 시간, 분 및 초를 결정합니다. |

{style="table-layout:auto"}

## [!UICONTROL Frontend Experience Settings]

![프론트엔드 환경 설정](./assets/payment-methods-paypal-payments-advanced-frontend-experience-settings.png)<!-- zoom -->

| 필드 | [범위](../../getting-started/websites-stores-views.md#scope-settings) | 설명 |
|--- |--- |--- |
| [!UICONTROL PayPal Product Logo] | 스토어 뷰 | 스토어에 표시되는 PayPal 로고를 결정합니다. 두 가지 크기의 기본 스타일은 네 가지입니다. 옵션: `No Logo` / `We prefer PayPal (150 x 60)` / `We prefer PayPal (150 x 40)` / `Now accepting PayPal (150 x 60)` / `Now accepting PayPal (150 x 40)` / `Payments by PayPal (150 x 60)` / `Payments by PayPal (150 x 40)` / `Shop now using (150 x 60)` / `Shop now using (150 x 40)` |
| [!UICONTROL PayPal Merchant Pages Style] |  |  |
| [!UICONTROL Page Style] | 스토어 뷰 | PayPal 판매자 페이지의 모양을 결정합니다. 허용되는 값: <br/>**`paypal`**- PayPal 페이지 스타일을 사용합니다.<br/>**`primary`** - 계정 프로필에서 &quot;기본&quot; 스타일로 식별한 페이지 스타일을 사용합니다. <br/>**`your_custom_value`**- 계정 프로필에 지정된 사용자 지정 결제 페이지 스타일을 사용합니다. |
| [!UICONTROL Header Image URL] | 스토어 뷰 | 체크아웃 페이지의 왼쪽 위 모서리에 표시되는 이미지의 URL입니다. 최대 크기는 750 x 90픽셀입니다. <br/><br/>**_참고:_**&#x200B;PayPal에서는 이미지를 보안(https) 서버에 저장할 것을 권장합니다. 그렇지 않으면 고객의 브라우저가 &quot;페이지에 보안 및 비보안 항목이 모두 포함되어 있습니다.&quot;라고 경고할 수 있습니다. |
| [!UICONTROL Header Image Background Color] | 스토어 뷰 | 체크아웃 페이지에서 헤더의 배경색에 대한 6자리 [16진수](https://en.wikipedia.org/wiki/Web_colors) 코드. 코드를 대문자와 소문자로 입력할 수 있습니다. |
| [!UICONTROL Header Image Border Color] | 스토어 뷰 | 헤더 주위의 2픽셀 테두리에 대한 6자 16진수 색상 코드. |
| [!UICONTROL Page Background Color] | 스토어 뷰 | 머리글 및 결제 양식 뒤에 표시되는 체크아웃 페이지의 배경색에 대한 6자리 16진수 색상 코드. |

{style="table-layout:auto"}
