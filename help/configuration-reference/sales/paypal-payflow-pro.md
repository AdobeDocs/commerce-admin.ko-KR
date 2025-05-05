---
title: '[!UICONTROL Sales] &gt; [!UICONTROL Payment Methods] &gt;  [!UICONTROL PayPal Payflow Pro]'
description: Commerce 관리자의 [!UICONTROL Sales] &gt; [!UICONTROL Payment Methods] 페이지에서 [!UICONTROL PayPal Payflow Pro] 섹션의 구성 설정을 검토하십시오.
exl-id: 2aae038b-15c0-452a-98bc-4d97efbb60f6
feature: Configuration, Payments
source-git-commit: b710c0368dc765e3bf25e82324bffe7fb8192dbf
workflow-type: tm+mt
source-wordcount: '645'
ht-degree: 0%

---

# [!UICONTROL Sales] > [!UICONTROL Payment Methods] >  [!UICONTROL PayPal Payflow Pro]

>[!IMPORTANT]
>
>**PSD2 요구 사항:** <br/>
>2019년 9월 14일부터 유럽 은행은 [PSD2](../../getting-started/compliance-payment-services-directive.md) 요구 사항을 충족하지 않는 결제를 거절할 수 있습니다. PSD2를 준수하려면 [!DNL PayPal Payflow Pro]을(를) [!DNL Cardinal Commerce]에 통합해야 합니다. 자세한 내용은 [Payflow용 3D 보안](https://developer.paypal.com/api/nvp-soap/payflow/3d-secure-overview/)을 참조하세요.

{{config}}

## [!UICONTROL Required Settings]

![필수 설정](./assets/paypal-payflow-pro-settings.png)<!-- zoom -->

| 필드 | [범위](../../getting-started/websites-stores-views.md#scope-settings) | 설명 |
|--- |--- |--- |
| [!UICONTROL Email Associated with PayPal Merchant Account] | 웹 사이트 | (선택 사항) PayPal 판매자 계정과 연결된 모든 이메일 주소. 이메일 주소는 대소문자를 구분하며, 계정에 있는 주소와 정확히 일치해야 합니다. |
| [!UICONTROL Partner] | 웹 사이트 | 해당되는 경우 PayPal 파트너 ID입니다. |
| [!UICONTROL Vendor] | 웹 사이트 | PayPal 사용자 로그인 이름입니다. |
| 사용자 | 웹 사이트 | PayPal 계정에 있는 다른 사용자의 ID. |
| [!UICONTROL Password] | 웹 사이트 | PayPal 판매자 계정과 연결된 암호입니다. |
| [!UICONTROL Test Mode] | 웹 사이트 | 활성화되면 은 테스트 환경에서 PayPal Payflow Pro를 실행합니다. 프로덕션 모드에서 &quot;실행&quot;할 준비가 되면 테스트 모드를 끕니다. 옵션: `Yes` / `No` |
| [!UICONTROL Use Proxy] | 웹 사이트 | 서버 방화벽이 PayPal 서버에 대한 직접 액세스를 차단하는 경우 프록시를 사용하여 트래픽을 리디렉션할 수 있습니다. 해당하는 경우 는 PayPal 서버와의 연결을 설정하는 데 사용되는 프록시 서버를 식별합니다. 옵션: `Yes` / `No` <br/><br/>활성화된 경우 프록시 옵션: <br/>**`Proxy Host`**- 프록시 호스트의 IP 주소를 설정하십시오.<br/>**`Proxy Port`** - 프록시 포트의 수입니다. |
| [!UICONTROL Enable this Solution] | 웹 사이트 | PayPal Payflow Pro를 결제 방법으로 고객에게 사용할 수 있는지 결정합니다. |
| [!UICONTROL Enable PayPal Credit] | 웹 사이트 | 고객이 PayPal 크레딧을 결제 옵션으로 사용할 수 있는지 여부를 결정합니다. |

{style="table-layout:auto"}

## [!UICONTROL Advertise PayPal Credit]

![PayPal 크레딧 알림](./assets/payment-methods-paypal-payments-advanced-advertise-paypal-credit.png)<!-- zoom -->

| 필드 | [범위](../../getting-started/websites-stores-views.md#scope-settings) | 설명 |
|--- |--- |--- |
| [!UICONTROL Publisher ID] | 웹 사이트 | PayPal 신용 계정과 연결된 게시자 ID입니다. |
| [!UICONTROL Get Publisher ID from PayPal] |  | PayPal에서 게시자 ID를 가져옵니다. |
| [!UICONTROL Home Page] | 웹 사이트 | 홈 페이지에서 [!DNL PayPal Credit] 배너의 위치와 크기를 결정합니다. 옵션: <br/>**`Display`**- 스토어의 홈 페이지에 [!DNL PayPal Credit] 배너가 표시되는지 여부를 결정합니다. 옵션: `Yes` / `No`<br/>**`Position`** - 홈 페이지에서 [!DNL PayPal Credit] 배너의 위치를 결정합니다. 옵션: 헤더(가운데)/사이드바(오른쪽) <br/>**`Size`**- 홈 페이지에서 [!DNL PayPal Credit] 배너의 크기를 결정합니다. 옵션: `190 x 100` / `234 x 60` / `300 x 50` / `468 x 60` / `728 x 90` /` 800 x 66` |
| [!UICONTROL Catalog Category Page] | 웹 사이트 | 범주 페이지에서 [!DNL PayPal Credit] 배너의 위치와 크기를 결정합니다. 옵션: ([!UICONTROL Home Page]과(와) 동일) |
| [!UICONTROL Catalog Product Page] | 웹 사이트 | 제품 페이지에서 [!DNL PayPal Credit] 배너의 위치와 크기를 결정합니다. 옵션: ([!UICONTROL Home Page]과(와) 동일) |
| [!UICONTROL Checkout Cart Page] | 웹 사이트 | 장바구니 페이지에서 [!DNL PayPal Credit] 배너의 위치와 크기를 결정합니다. 옵션: ([!UICONTROL Home Page]과(와) 동일) |

{style="table-layout:auto"}

## [!UICONTROL Basic Settings - PayPal Payflow Pro]

![기본 설정](./assets/payment-methods-paypal-payflow-pro-basic-settings.png)<!-- zoom -->

| 필드 | [범위](../../getting-started/websites-stores-views.md#scope-settings) | 설명 |
|--- |--- |--- |
| [!UICONTROL Title] | 스토어 뷰 | 체크아웃 시 결제 수단으로 PayPal Payflow Pro를 식별하는 이름입니다. |
| [!UICONTROL Sort Order] | 스토어 뷰 | 체크아웃 중에 다른 결제 방법과 함께 나열할 때 PayPal Payflow Pro가 표시되는 순서를 결정하는 숫자입니다. |
| [!UICONTROL Payment Action] | 웹 사이트 | 주문이 제출될 때 PayPal에서 취하는 조치를 결정합니다. 옵션: <br/>**`Authorization`**- 구매를 승인하지만 자금을 보류합니다. 상인에게 &#39;포착&#39;되기 전까지는 그 금액이 인출되지 않는다.<br/>**`Sale`** - 구매 금액이 승인되어 고객 계정에서 즉시 인출됩니다. |
| **[!UICONTROL Credit Card Settings]** |  |  |
| [!UICONTROL Allowed Credit Cart Types] | 웹 사이트 | 체크아웃 중에 고객이 사용할 수 있는 신용 카드를 결정합니다. 지원되는 카드를 각각 선택하십시오. 옵션: `American Express`(추가 계약 필요) / `Visa` / `MasterCard` / `Discover` / `JCB` |

{style="table-layout:auto"}

## [!UICONTROL Advanced Settings]

![고급 설정](./assets/payment-methods-paypal-payflow-pro-advanced-settings.png)<!-- zoom -->

| 필드 | [범위](../../getting-started/websites-stores-views.md#scope-settings) | 설명 |
|--- |--- |--- |
| 장바구니에 표시 | 스토어 뷰 | PayPal Express Checkout이 장바구니에서 결제 옵션으로 표시되는지 여부를 결정합니다. 옵션: 예(권장) / 아니요 |
| [!UICONTROL Payment Action Applicable From] | 웹 사이트 | 적용 가능한 국가 선택의 범위를 결정합니다. 옵션: 허용된 모든 국가/특정 국가 |
| [!UICONTROL Countries Payment Applicable From] | 웹 사이트 | 지불이 수락되는 각 국가를 식별합니다. 선택한 국가에 청구 주소가 있는 고객만 이 결제 방법으로 구매할 수 있습니다. |
| [!UICONTROL Debug Mode] | 웹 사이트 | 스토어와 PayPal 결제 시스템 간에 전송된 메시지를 로그 파일에 기록합니다. 옵션: `Yes` / `No` <br/><br/>**_참고:_**&#x200B;로그 파일은 서버에 저장되며 개발자만 액세스할 수 있습니다. PCI 데이터 보안 표준에 따라 신용 카드 정보는 로그 파일에 기록되지 않습니다. |
| [!UICONTROL Enable SSL Verification] | 웹 사이트 | 호스트 보안 인증서를 확인할 수 있도록 합니다. 옵션: `Yes` / `No` |
| [!UICONTROL Transfer Cart Line Items] | 웹 사이트 | PayPal 사이트에 고객 장바구니의 라인 항목에 대한 전체 요약을 표시합니다. 옵션: `Yes` / `No` |
| [!UICONTROL Skip Order Review Step] | 웹 사이트 | 고객이 PayPal 사이트에서 거래를 완료할 수 있는지, 아니면 주문을 제출하기 전에 상점으로 돌아가서 주문 검토 단계를 완료해야 하는지 결정합니다. 옵션: `Yes` / `No` |

{style="table-layout:auto"}
