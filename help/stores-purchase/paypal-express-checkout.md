---
title: PayPal Express 체크아웃
description: 스토어에서 온라인 결제 솔루션으로 PayPal Express Checkout을 설정하는 방법에 대해 알아봅니다.
exl-id: 0cd90306-cf47-4a5f-8994-6ae96904ae2f
feature: Payments
source-git-commit: 8b5af316ab1d2e632ed5fc2066974326830ab3f7
workflow-type: tm+mt
source-wordcount: '3113'
ht-degree: 0%

---

# PayPal Express 체크아웃

PayPal Express Checkout은 고객에게 신용카드 또는 개인 PayPal 계정의 보안을 통해 결제할 수 있는 기능을 제공함으로써 판매 증대에 도움이 됩니다. 체크아웃 중에 고객이 보안 PayPal 사이트로 리디렉션되어 결제 정보를 완료합니다. 그런 다음 고객이 저장소로 돌아가 나머지 체크아웃 프로세스를 완료합니다. &#39;익스프레스 체크아웃&#39;을 선택하면 익숙한 &#39;페이팔&#39; 버튼이 매장에 추가돼 매출을 높이는 것으로 알려졌다.

>[!IMPORTANT]
>
>**PSD2 요구 사항:** <br/>
>2019년 9월 14일부터 유럽 은행들은 충족되지 않는 지불을 거절할 수 있습니다 [PSD2](../getting-started/compliance-payment-services-directive.md) 요구 사항. 모든 요구 사항이 PayPal에 의해 처리되므로 PayPal Express Checkout에서 PSD2를 준수하는 데 필요한 작업은 없습니다.

현재 PayPal 계정이 있는 고객은 _[!UICONTROL Check out with PayPal]_단추를 클릭합니다. Express Checkout은 독립 실행형으로 사용하거나 PayPal 올인원 솔루션 중 하나와 함께 사용할 수 있습니다. 이미 온라인에서 신용카드를 받고 있다면, 페이팔로 결제하기를 선호하는 신규 고객을 유치하기 위한 추가 옵션으로 &#39;익스프레스 체크아웃&#39;을 제공하면 된다.

>[!NOTE]
>
>PayPal은 PayPal Express Checkout을 통해 디지털 상품 판매를 더 이상 지원하지 않으며 다음 중 하나를 사용할 것을 권장합니다. [PayPal 결제 표준](paypal-payments-standard.md) 또는 다음을 포함하는 주문을 처리하는 다른 PayPal 결제 게이트웨이 [가상 제품](../catalog/product-create-virtual.md).

## 요구 사항

- 판매자: [비즈니스 PayPal 계정][1]
- 고객: [개인 PayPal 계정][2]

## 빠른 체크아웃 워크플로우

다른 결제 방식과 달리 페이팔 익스프레스 체크아웃은 제품 페이지, 미니 장바구니, 장바구니에서 일반적인 체크아웃 워크플로 시작 시 고객이 체크아웃할 수 있도록 했다.

1. **고객 주문** - 고객이 다음을 클릭/탭함 _[!UICONTROL Check out with PayPal]_단추를 클릭합니다.
1. **고객이 PayPal 사이트로 리디렉션됨** - 고객이 PayPal 사이트로 리디렉션되어 트랜잭션을 완료합니다.
1. **고객이 PayPal 계정에 로그인함** - 고객이 PayPal 계정에 로그인하여 트랜잭션을 완료해야 합니다. 결제 시스템은 PayPal 계정의 청구 및 배송 정보를 사용합니다.
1. **고객이 체크아웃 페이지로 돌아가기** - 고객이 주문을 검토하도록 스토어의 체크아웃 페이지로 다시 리디렉션됩니다.
1. **고객 주문** - 고객이 주문하고 주문 정보가 PayPal에 제출됩니다.
1. **PayPal로 거래 결제** - PayPal이 주문을 받고 거래를 정산합니다.

>[!NOTE]
>
>PayPal Express Checkout은 여러 주소가 있는 주문을 지원하지 않습니다.

## 컨텍스트 내 체크아웃

PayPal _직접 체크아웃_ 그 어느 때보다 온라인 결제가 쉬워졌습니다. 고객은 이 간단한 1~2번의 클릭으로 매끄러운 체크아웃을 수행하는 동안 스토어를 놓치지 않습니다. Mac과 PC에서도 상황에 맞는 체크아웃 기능이 동일하게 작동하며 데스크탑 컴퓨터, 태블릿 및 모바일 장치에서 일관된 경험을 제공합니다. 자세한 내용은 다음을 참조하십시오. [Express Checkout에서 직접 체크아웃][5].

![PayPal 컨텍스트 내 체크아웃 데모](./assets/storefront-paypal-in-context.png){width="700" zoomable="yes"}

[_PayPal 컨텍스트 내 체크아웃 데모_][6]

다음에 대한 저장소를 구성할 때 [!DNL PayPal Express Checkout], 이 옵션을 활성화할 수 있습니다.

## PayPal 계정 구성

Commerce Admin에서 PayPal Express Checkout을 설정하기 전에 PayPal 웹 사이트에서 판매자 계정을 구성해야 합니다.

1. 에서 PayPal 고급 계정에 로그인합니다. [manager.paypal.com][3].

1. 다음으로 이동 **[!UICONTROL Service Settings]** > **[!UICONTROL Hosted Checkout Pages]** > **[!UICONTROL Set Up]** 을 설정하고 다음 설정을 수행합니다.

   - **[!UICONTROL AVS]**: `No`
   - **[!UICONTROL CSC]**: `No`
   - **[!UICONTROL Enable Secure Token]**: `Yes`

1. 클릭 **[!UICONTROL Save Changes]**.

1. 다른 사용자 설정(PayPal 권장):

   - 다음으로 이동 [manager.paypal.com][3] 계정에 로그인합니다.

   - 다른 사용자를 설정하려면 지침을 따르십시오.

   - 클릭 **[!UICONTROL Update]**.

## Commerce에서 PayPal Express 체크아웃 설정

두 개의 PayPal 솔루션이 동시에 활성화될 수 있습니다. PayPal Express Checkout 및 올인원 솔루션입니다. 다른 솔루션을 활성화하면 이전에 사용한 솔루션이 자동으로 비활성화됩니다.

>[!NOTE]
>
>클릭 **[!UICONTROL Save Config]** 언제든지 진행 상황을 저장할 수 있습니다.

### 1단계: 구성 시작

1. 다음에서 _관리자_ 사이드바, 이동 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. 왼쪽 패널에서 를 확장합니다. **[!UICONTROL Sales]** 및 선택 **[!UICONTROL Payment Methods]**.

1. 설치에 여러 웹 사이트, 스토어 또는 보기가 있는 경우 다음을 설정합니다. **[!UICONTROL Store View]** 이 구성을 적용할 저장소 보기로 이동합니다.

1. 다음에서 _[!UICONTROL Merchant Location]_섹션에서&#x200B;**[!UICONTROL Merchant Country]**비즈니스 위치.

   이 설정은 구성에 나타나는 PayPal 솔루션의 선택을 결정합니다.

   ![상선 국가](../configuration-reference/sales/assets/payment-methods-merchant-location.png){width="600" zoomable="yes"}

1. 아래 _[!UICONTROL Recommended Solutions]_, 클릭&#x200B;**[!UICONTROL Configure]**대상&#x200B;**[!UICONTROL PayPal Express Checkout]**.

   ![PayPal Express 체크아웃 구성](./assets/paypal-express-checkout.png){width="600"}

### 2단계: PayPal 계정 활성화 및 연결

1. 필요한 경우 를 확장합니다. ![확장 선택기](../assets/icon-display-expand.png) 다음 **[!UICONTROL Required PayPal Settings]** 섹션.

   ![PayPal 계정 연결](./assets/paypal-express-required.png){width="600" zoomable="yes"}

1. 테스트 또는 프로덕션용 계정 연결:

   - 테스트(개발) 모드의 경우 **[!UICONTROL Sandbox Credentials]** 및 을(를) 입력합니다. [PayPal 샌드박스][7] 자격 증명.
   - 프로덕션 모드의 경우 **[!UICONTROL Connect with PayPal]** 프로덕션 계정 자격 증명을 입력합니다.

   연결이 확인되면 계속 진행할 수 있습니다.

1. 설정 **[!UICONTROL Enable this Solution]** 끝 `Yes`.

1. 활성화하려면 [PayPal 컨텍스트 체크아웃](#in-context-checkout):

   - 설정 **[!UICONTROL Enable In-Context Checkout Experience]** 끝 `Yes`.

   - PayPal 입력 **[!UICONTROL Merchant Account ID]**.

     판매자 계정 ID는 PayPal 비즈니스 계정 프로필에 있습니다.

>[!NOTE]
>
>[PayPal 신용](paypal.md#paypal-credit-and-pay-later) 은(는) 이 결제 옵션에 대해 기본적으로 활성화되어 있습니다.

### 3단계: 필요한 PayPal 설정 완료

1. 필요한 경우 를 확장합니다. ![확장 선택기](../assets/icon-display-expand.png) 다음 **[!UICONTROL Express Checkout]** 섹션.

   ![PayPal Express 체크아웃 필수 설정](./assets/paypal-express-settings.png){width="600" zoomable="yes"}

1. (선택 사항) **[!UICONTROL Email Associated with PayPal Merchant Account]**.

   >[!IMPORTANT]
   >
   >이메일 주소는 대소문자를 구분합니다. 결제를 받으려면 입력한 이메일 주소가 PayPal 판매자 계정에 지정된 이메일 주소와 일치해야 합니다.

   PayPal 계정이 없는 경우 **[!UICONTROL Start accepting payments via PayPal]**.

1. 설정 **[!UICONTROL API Authentication Methods]** 다음 중 하나를 수행합니다.

   - `API Signature` - 이 PayPal 인증 방법은 구현하기 가장 쉬운 방법이며 사용자 이름, 암호 및 계정을 식별하는 문자 및 숫자의 고유한 문자열을 기반으로 합니다. API 서명 자격 증명이 만료되지 않습니다.
   - `API Certificate` - 이 PayPal 인증 방법은 보다 안전하며 사용자 이름, 암호 및 다운로드 가능한 인증서를 기반으로 합니다. API 자격 증명은 3년 후에 만료되며 갱신해야 합니다.

   필요한 경우 다음을 완료합니다.

   - **[!UICONTROL API Username]**
   - **[!UICONTROL API Password]**
   - **[!UICONTROL API Signature]**

1. 샌드박스 계정의 자격 증명을 사용하는 경우 다음을 설정합니다. **[!UICONTROL Sandbox Mode]** 끝 `Yes`.

   샌드박스에서 구성을 테스트할 때에는 만 사용하십시오 [신용 카드 번호][4] 페이팔에서 추천합니다. 프로덕션으로 이동할 준비가 되면 구성으로 돌아가 샌드박스 모드 를 로 설정합니다. `No` 프로덕션 PayPal 계정에 연결합니다.

1. 시스템이 프록시 서버를 사용하여 Commerce와 PayPal 결제 시스템 간의 연결을 설정하는 경우 다음을 설정하십시오. **[!UICONTROL API Uses Proxy]** 끝 `Yes` 다음을 완료합니다.

   - **[!UICONTROL Proxy Host]**
   - **[!UICONTROL Proxy Port]**

이 단계 순서가 끝나면 필요한 PayPal 설정이 완료됩니다. 기본 및 고급 설정을 계속 사용하거나 **[!UICONTROL Save Config]** 구성을 조정하려면 나중에 다시 돌아가기

### 단계 4: Advertising PayPal 크레딧/Advertising PayPal PayLater 설정(선택 사항)

2.4.3 릴리스부터 PayPal PayLater는 PayPal이 포함된 배포에서 지원됩니다. 이 기능을 통해 구매자는 구매 시 전체 금액을 지불하는 대신 2주 단위로 주문 금액을 지불하는 것이 가능하다. PayPal 크레딧 경험은 더 이상 사용되지 않습니다.

설정 **[!UICONTROL Enable PayPal PayLater Experience]** 다음 중 하나를 수행합니다.

- `Yes` - PayPal PayLater 광고를 설정하려면
- `No` - PayPal 크레딧을 광고하려면

>[!NOTE]
>
>다음 **[!UICONTROL Enable PayPal PayLater Experience]** 이 설정해도 [!DNL PayPal PayLater] 기능 및 제거 안 함 **_[!UICONTROL PayPal PayLater]_** 상점 앞 단추. 둘 다 비활성화하려면 **_[!UICONTROL PayPal PayLater]_** 및 **_[!UICONTROL PayPal Credit]_** 상점 앞의 버튼을 클릭하면 `PayPal Credit` 값: **[!UICONTROL Disable Funding Options]** 설정 ([!UICONTROL Advanced Settings] 아래에 [!UICONTROL Frontend Experience Settings]).

#### PayPal 크레딧 광고

1. 확장 ![확장 선택기](../assets/icon-display-expand.png) 다음 **[!UICONTROL Advertise PayPal Credit]** 섹션.

1. 계정 정보를 얻으려면 다음을 클릭하십시오. **[!UICONTROL Get Publisher ID from PayPal]** 지침을 따르십시오.

1. 다음을 입력하십시오. **[!UICONTROL Publisher ID]**.

   ![PayPal 크레딧 광고](../configuration-reference/sales/assets/payment-methods-paypal-payments-advanced-advertise-paypal-credit.png){width="600" zoomable="yes"}

1. 확장 ![확장 선택기](../assets/icon-display-expand.png) 다음 **[!UICONTROL Home Page]** 섹션.

1. 페이지에 배너를 배치하려면 다음을 설정하십시오. **[!UICONTROL Display]** 끝 `Yes`.

1. 설정 **[!UICONTROL Position]** 다음 중 하나를 수행합니다.

   - `Header (center)`
   - `Sidebar (right)`

1. 설정 **[!UICONTROL Size]** 다음 중 하나를 수행합니다.

   - `190 x 100`
   - `234 x 60`
   - `300 x 50`
   - `468 x 60`
   - `728 x 90`
   - `800 x 66`

   ![PayPal 크레딧 홈페이지 설정 광고](../configuration-reference/sales/assets/payment-methods-paypal-payments-advanced-advertise-paypal-credit-home-page.png){width="600" zoomable="yes"}

1. 확장 ![확장 선택기](../assets/icon-display-expand.png) 나머지 섹션 및 이전 단계를 반복합니다.

   - [!UICONTROL Catalog Category Page]
   - [!UICONTROL Catalog Product Page]
   - [!UICONTROL Checkout Cart Page]

#### PayPal PayLater 광고

1. 확장 ![확장 선택기](../assets/icon-display-expand.png) 다음 **[!UICONTROL Advertise PayPal PayLater]** 섹션.

1. 설정 **[!UICONTROL Enable PayPal PayLater]** 끝 `Yes`.

1. 확장 ![확장 선택기](../assets/icon-display-expand.png) 다음 **[!UICONTROL Home Page]** 섹션.

1. 페이지에 배너를 배치하려면 다음을 설정하십시오. **[!UICONTROL Display]** 끝 `Yes`.

1. 설정 **[!UICONTROL Position]** 다음 중 하나를 수행합니다.

   - `Header (center)`
   - `Sidebar`

1. 설정 **[!UICONTROL Style Layout]** 다음 중 하나를 수행합니다.

   - `Text`
   - `Flex`

1. 대상 [!UICONTROL Style Layout] **[!UICONTROL Text]** 만, 설정 **[!UICONTROL Logo Type]** 다음 중 하나를 수행합니다.

   - `Primary`
   - `Alternative`
   - `Inline`
   - `None`

1. 대상 [!UICONTROL Style Layout] **[!UICONTROL Text]** 만, 설정 **[!UICONTROL Logo Position]** 다음 중 하나를 수행합니다.

   - `Left`
   - `Right`
   - `Top`

1. 대상 [!UICONTROL Style Layout] **[!UICONTROL Text]** 만, 설정 **[!UICONTROL Text Color]** 다음 중 하나를 수행합니다.

   - `Black`
   - `White`
   - `Monochrome`
   - `Grayscale`

1. 대상 [!UICONTROL Style Layout] **[!UICONTROL Text]** 만, 설정 **[!UICONTROL Text Size]** 다음 중 하나를 수행합니다.

   - `10px`
   - `11px`
   - `12px`
   - `13px`
   - `14px`
   - `15px`
   - `16px`

1. 대상 [!UICONTROL Style Layout] **[!UICONTROL Flex]** 만, 설정 **[!UICONTROL Ratio]** 다음 중 하나를 수행합니다.

   - `1x1`
   - `1x4`
   - `8x1`
   - `20x1`

1. 대상 [!UICONTROL Style Layout] **[!UICONTROL Flex]** 만, 설정 **[!UICONTROL Color]** 다음 중 하나를 수행합니다.

   - `Blue`
   - `Black`
   - `White`
   - `White No Border`
   - `Gray`
   - `Monochrome`
   - `Grayscale`

   ![PayPal 크레딧 홈페이지 설정 광고](../configuration-reference/sales/assets/payment-methods-paypal-payments-advanced-advertise-paypal-paylater-home-page.png){width="600" zoomable="yes"}

1. 확장 ![확장 선택기](../assets/icon-display-expand.png) 나머지 섹션 및 이전 단계를 반복합니다.

   - [!UICONTROL Catalog Product Page]
   - [!UICONTROL Checkout Cart Page]
   - [!UICONTROL Checkout Payment Step]
   - [!UICONTROL Catalog Category Page]

### 5단계: 기본 설정 완료

1. 확장 ![확장 선택기](../assets/icon-display-expand.png) 다음 **[!UICONTROL Basic Settings - PayPal Express Checkout]** 섹션.

   ![기본 설정](../configuration-reference/sales/assets/payment-methods-paypal-express-checkout-basic-settings.png){width="600" zoomable="yes"}

1. 대상 **[!UICONTROL Title]**&#x200B;을 클릭하고 체크아웃 중에 이 결제 방법을 식별하는 제목을 입력합니다.

   제목을 사용하는 것이 좋습니다 _PayPal_ 모든 스토어 조회수.

1. 여러 결제 방법을 제공하는 경우 숫자를 입력합니다. **[!UICONTROL Sort Order]** 다른 결제 방법과 함께 나열할 때 PayPal Express Checkout이 표시되는 순서를 결정합니다.

   이 번호는 다른 결제 방법과 관련이 있습니다. (`0` = 첫 번째, `1` = 초, `2` = 세 번째 등입니다.)

1. 설정 **[!UICONTROL Payment Action]** 다음 중 하나를 수행합니다.

   - `Authorization` - 구매를 승인하고 자금을 보류합니다. 그 금액은 그때까지 인출되지 않는다 _캡처됨_ 상인에 의해.
   - `Sale` - 구매 금액이 승인되어 즉시 고객의 계좌에서 인출됩니다.
   - `Order` - 주문 금액은 PayPal의 고객 잔고, 은행 계좌 또는 신용 카드에 수집되거나 승인되지 않습니다. 주문 결제 행위는 PayPal 결제 시스템과 가맹점 간의 계약을 나타냅니다. 머천트는 최대 29일 동안 고객 구매자 계정에서 주문된 총액까지 하나 이상의 금액을 캡처할 수 있습니다. 펀드가 주문된 후 판매사는 이후 29일 동안 언제든지 펀드를 캡처할 수 있다. 하나 이상의 송장을 생성하여 주문 금액을 캡처하는 작업은 상거래 관리자에서만 수행할 수 있습니다.

1. 다음을 표시합니다. _[!UICONTROL Check out with PayPal]_제품 페이지의 단추, 설정&#x200B;**[!UICONTROL Display on Product Details Page]**끝 `Yes`.

1. 지급 조치가 다음으로 설정된 경우 `Order`, 다음을 완료합니다

   - **[!UICONTROL Authorization Honor Period (days)]** - 기본 권한 부여가 유효한 기간을 결정합니다. 값은 PayPal 판매자 계정의 해당 값과 같아야 합니다. PayPal 판매자 계정의 기본값은 입니다. `3`. 이 수를 늘리려면 PayPal에 문의해야 합니다. 미국 태평양 표준시 기준 마지막 날 오후 11시 49분에 인증이 유효하지 않게 됩니다.

   - **[!UICONTROL Order Valid Period (days)]** - 주문이 유효한 기간을 결정합니다. 주문이 무효화되면 더 이상 그에 대한 송장을 생성할 수 없습니다. PayPal 판매자 계정의 주문 유효 기간 값과 같은 값을 지정하십시오. PayPal 판매자 계정의 기본값은 입니다. `29`. 이 번호를 변경하려면 PayPal에 문의해야 합니다.

   - **[!UICONTROL Number of Child Authorizations]** - 단일 주문에 대한 최대 승인 수를 지정하여 주문에 대해 생성할 수 있는 온라인 부분 송장의 최대 수를 결정합니다. 이 값은 PayPal 판매자 계정의 해당 설정과 같아야 합니다. PayPal 계정의 기본 자녀 인증 수는 다음과 같습니다. `1`. 이 수를 늘리려면 PayPal에 문의해야 합니다.

### 6단계: 고급 설정 완료

1. 확장 ![확장 선택기](../assets/icon-display-expand.png) 다음 **[!UICONTROL Advanced Settings]** 섹션.

   ![고급 설정 - PayPal Express 체크아웃](../configuration-reference/sales/assets/payment-methods-paypal-express-checkout-advanced-settings.png){width="600" zoomable="yes"}

1. 설정 **[!UICONTROL Display on Shopping Cart]** 끝 `Yes`.

1. 설정 **[!UICONTROL Payment Applicable From]** 다음 중 하나를 수행합니다.

   - `All Allowed Countries` - 스토어 구성에 지정된 모든 국가의 고객이 이 결제 방법을 사용할 수 있습니다.
   - `Specific Countries` - 이 옵션을 선택한 후 _[!UICONTROL Payment from Specific Countries]_목록이 나타납니다. 여러 국가를 선택하려면 Ctrl 키(PC) 또는 Command 키(Mac)를 누른 채 각 항목을 클릭합니다.

1. 결제 시스템과의 통신을 로그 파일에 기록하려면 다음을 설정합니다. **[!UICONTROL Debug Mode]** 끝 `Yes`.

   PayPal Payments Advanced 로그 파일은 `_payflow_advanced.log`.

   >[!NOTE]
   >
   >PCI 데이터 보안 표준에 따라 신용 카드 정보는 로그 파일에 기록되지 않습니다.

1. 호스트 신뢰성을 확인하려면 다음을 설정하십시오. **[!UICONTROL Enable SSL Verification]** 끝 `Yes`.

1. PayPal 사이트에서 라인 항목별로 고객 주문의 전체 요약을 표시하려면 다음을 설정합니다. **[!UICONTROL Transfer Cart Line Items]** 끝 `Yes`.

1. 요약에 최대 10개의 운송 옵션을 포함하려면 다음을 설정합니다. **[!UICONTROL Transfer Shipping Options]** 끝 `Yes`. 이 옵션은 라인 항목이 이전으로 설정된 경우에만 나타납니다.

1. PayPal 수락 단추에 사용되는 이미지 유형을 확인하려면 다음을 설정하십시오. **[!UICONTROL Shortcut Buttons Flavor]** 다음 중 하나를 수행합니다.

   - `Dynamic` - (권장) PayPal 서버에서 동적으로 변경할 수 있는 이미지를 표시합니다.
   - `Static` - 동적으로 변경할 수 없는 특정 이미지를 표시합니다.

1. PayPal 계정이 없는 고객이 이 방법으로 구매할 수 있도록 하려면 다음을 설정하십시오. **[!UICONTROL Enable PayPal Guest Checkout]** 끝 `Yes`.

1. 설정 **[!UICONTROL Require Customer's Billing Address]** 다음 중 하나를 수행합니다.

   - `Yes` - 모든 구매에 대해 고객의 청구 주소가 필요합니다.
   - `No` - 구매 시 고객의 청구 주소가 필요하지 않습니다.
   - `For Virtual Quotes Only` - 가상 견적에 대해서만 고객의 청구 주소가 필요합니다.

   >[!NOTE]
   >
   >이 기능은 PayPal 기술 지원을 통해 판매자 계정에 대해 활성화되어야 합니다.

1. (선택 사항) **[!UICONTROL Billing Agreement Signup]** 고객이 서명하도록 허용 [청구 계약](paypal-billing-agreements.md) 고객 계정에 사용 가능한 활성 청구 계약이 없을 때 PayPal 결제 시스템에 스토어를 통해 결제:

   - `Auto` - 고객은 빠른 체크아웃 플로우 중에 청구 계약에 서명하거나 다른 결제 방법을 사용할 수 있습니다.
   - `Ask Customer` - 고객은 빠른 체크아웃 플로우 중에 청구 계약에 서명할지 여부를 결정할 수 있습니다.
   - `Never` - 빠른 체크아웃 플로우 중에는 고객이 청구 계약에 서명할 수 없습니다.

   >[!NOTE]
   >
   >상인들은 물어봐야 한다 [PayPal 판매자 기술 지원](https://developer.paypal.com/support/) 계정에서 청구 계약을 사용할 수 있도록 설정합니다. 다음 _청구 계약 등록_ 이 매개변수는 PayPal이 귀하의 판매자 계정에 대해 청구 계약을 사용할 수 있음을 확인한 후에만 사용할 수 있습니다.

1. 고객이 주문 검토를 위해 스토어로 돌아가지 않고 PayPal 사이트에서 거래를 완료할 수 있도록 하려면 다음을 설정하십시오. **[!UICONTROL Skip Order Review Step]** 끝 `Yes`.

1. 스토어에 필요한 경우 추가 섹션을 완료합니다.

   - [PayPall 청구 계약 설정](#paypal-billing-agreement-settings)
   - [결제 보고서 설정](#settlement-report-settings)
   - [프론트엔드 경험 설정](#frontend-experience-settings)
   - [스마트 단추 사용자 지정](#customize-smart-buttons)
   - [기능](#features)

1. 완료되면 다음을 클릭하십시오. **[!UICONTROL Save Config]**.

#### PayPal 청구 계약 설정

A [청구 계약](paypal-billing-agreements.md) 은 여러 주문과 함께 사용하도록 PayPal에서 승인한 판매자와 고객 간의 판매 계약입니다. 체크아웃 프로세스 중에 청구 계약 결제 옵션은 이미 귀사와 청구 계약을 체결한 고객에게만 표시됩니다. PayPal이 계약을 승인한 후에는 결제 시스템에서 고유한 참조 ID를 발행하여 계약과 연관된 각 주문을 식별합니다. 구매 주문과 마찬가지로 고객이 귀사와 설정할 수 있는 청구 계약 수에는 제한이 없습니다.

1. 확장 ![확장 선택기](../assets/icon-display-expand.png) 다음 **[!UICONTROL PayPal Billing Agreement Settings]** 섹션.

   ![청구 계약 설정](../configuration-reference/sales/assets/payment-methods-paypal-express-checkout-billing-agreement-settings.png){width="600" zoomable="yes"}

1. 설정 **[!UICONTROL Enabled]** 끝 `Yes`.

1. 대상 **[!UICONTROL Title]**&#x200B;을 클릭하고 체크아웃 중에 PayPal 결제 계약 방법을 식별하는 제목을 입력합니다.

1. 여러 결제 방법을 제공하는 경우 **[!UICONTROL Sort Order]** 체크아웃 중에 다른 결제 방법과 함께 나열될 때 청구 계약이 표시되는 순서를 결정하는 필드입니다.

1. 설정 **[!UICONTROL Payment Action]** 다음 중 하나를 수행합니다.

   - `Authorization` - 구매를 승인하고 자금을 보류합니다. 상인에게 &#39;포착&#39;되기 전까지는 그 금액이 인출되지 않는다.
   - `Sale` - 구매 금액이 승인되어 즉시 고객의 계좌에서 인출됩니다.

1. 설정 **[!UICONTROL Payment Applicable From]** 다음 중 하나를 수행합니다.

   - `All Allowed Countries` - 스토어 구성에 지정된 모든 국가의 고객이 이 결제 방법을 사용할 수 있습니다.
   - `Specific Countries` - 이 옵션을 선택한 후 _[!UICONTROL Payment from Specific Countries]_목록이 나타납니다. 여러 국가를 선택하려면 Ctrl 키(PC) 또는 Command 키(Mac)를 누른 상태에서 각 국가를 클릭합니다.

1. 로그 파일에 결제 시스템과의 통신을 기록하려면 다음을 설정합니다 **[!UICONTROL Debug Mode]** 끝 `Yes`.

   >[!NOTE]
   >
   >로그 파일은 서버에 저장되며 개발자만 액세스할 수 있습니다. PCI 데이터 보안 표준에 따라 신용 카드 정보는 로그 파일에 기록되지 않습니다.

1. SSL 인증을 활성화하려면 다음을 설정하십시오. **[!UICONTROL Enable SSL Verification]** 끝 `Yes`.

1. PayPal 결제 페이지에서 고객 주문에 있는 각 라인 항목의 요약을 표시하려면 다음을 설정합니다. **[!UICONTROL Transfer Cart Line Items]** 끝 `Yes`.

1. 고객이 고객 계정의 대시보드에서 청구 계약을 시작할 수 있도록 하려면 다음을 설정합니다. **[!UICONTROL Allow in Billing Agreement Wizard]** 끝 `Yes`.

#### 결제 보고서 설정

1. 확장 ![확장 선택기](../assets/icon-display-expand.png) 다음 **[!UICONTROL Settlement Report Settings]** 섹션.

   ![결제 보고서 설정](../configuration-reference/sales/assets/payment-methods-paypal-payments-advanced-settlement-report-settings.png){width="600" zoomable="yes"}

1. 대상 **[!UICONTROL SFTP Credentials]**&#x200B;를 사용하여 다음을 수행합니다.

   - PayPal 보안 FTP 서버에 등록한 경우 다음 SFTP 로그인 자격 증명을 입력하십시오.

      - 로그인
      - 암호

   - 다음 시간 이전에 테스트 보고서를 실행하려면 _실행 중_ 사이트에 Express Checkout을 사용하여 다음을 설정합니다. **[!UICONTROL Sandbox Mode]** 끝 `Yes`.

   - 다음을 입력합니다. **[!UICONTROL Custom Endpoint Hostname or IP Address]**.

     기본적으로 값은 다음과 같습니다. `reports.paypal.com`

   - 다음을 입력합니다. **[!UICONTROL Custom Path]** 보고서가 저장되는 위치입니다.

     기본적으로 값은 다음과 같습니다. `/ppreports/outgoing`

1. 일정에 따라 보고서를 생성하려면 다음을 완료하십시오. **[!UICONTROL Scheduled Fetching]** 설정:

   - 설정 **[!UICONTROL Enable Automatic Fetching]** 끝 `Yes`.

   - 설정 **[!UICONTROL Schedule]** 다음 중 하나를 수행합니다.

      - `Daily`
      - `Every 3 Days`
      - `Every 7 Days`
      - `Every 10 Days`
      - `Every 14 Days`
      - `Every 30 Days`
      - `Every 40 Days`

     PayPal은 45일 동안 각 보고서를 유지합니다.

   - 설정 **[!UICONTROL Time of Day]** 보고서를 생성할 시간, 분 및 초로 설정합니다.

#### 프론트엔드 경험 설정

프론트엔드 경험 설정을 사용하여 사이트에 표시할 PayPal 로고를 선택하고 PayPal 판매자 페이지의 모양을 사용자 지정합니다.

1. 확장 ![확장 선택기](../assets/icon-display-expand.png) 다음 **[!UICONTROL Frontend Experience Settings]** 섹션.

   ![프론트엔드 경험 설정](../configuration-reference/sales/assets/payment-methods-paypal-payments-advanced-frontend-experience-settings1.png){width="600" zoomable="yes"}

1. 다음 항목 선택 **[!UICONTROL PayPal Product Logo]** 스토어의 PayPal 블록에 표시하려는 경우입니다.

   PayPal 로고는 4가지 스타일과 2가지 크기로 제공됩니다.

   - `No Logo`
   - `We Prefer PayPal (150 x 60 or 150 x 40)`
   - `Now Accepting PayPal (150 x 60 or 150 x 40)`
   - `Payments by PayPal (150 x 60 or 150 x 40)`
   - `Shop Now Using PayPal (150 x 60 or 150 x 40)`

1. PayPal 판매자 페이지의 모양을 사용자 지정하려면 다음을 수행하십시오.

   - 의 이름을 입력합니다. **[!UICONTROL Page Style]** PayPal 판매자 페이지에 적용할 대상:

      - `paypal` - PayPal 페이지 스타일을 사용합니다.
      - `primary` - 로 식별한 페이지 스타일을 사용합니다. _기본_ 계정 프로필에서 스타일을 지정합니다.
      - `your_custom_value` - 계정 프로필에 지정된 사용자 정의 결제 페이지 스타일을 사용합니다.

   - 대상 **[!UICONTROL Header Image URL]**&#x200B;결제 페이지의 왼쪽 위 모서리에 표시할 이미지의 URL을 입력합니다. 최대 파일 크기는 750픽셀 너비 x 90픽셀 높이입니다.

     >[!NOTE]
     >
     >PayPal은 이미지가 보안(https) 서버에 있는 것을 권장합니다. 그렇지 않으면 브라우저가 다음을 경고할 수 있습니다. _페이지에 보안 및 비보안 항목이 모두 포함되어 있습니다._.

   - 페이지의 색상을 설정하려면 6자의 16진수 코드를 `#` 기호, 각 항목:

      - **[!UICONTROL Header Background Color]** - 체크아웃 페이지 헤더의 배경색입니다.
      - **[!UICONTROL Header Border Color]** - 헤더 주위의 2픽셀 테두리 색입니다.
      - **[!UICONTROL Page Background Color]** - 체크아웃 페이지 및 헤더와 결제 양식 주변의 배경색입니다.

#### 스마트 단추 사용자 지정

다음 _스마트 결제 단추_ 이 기능을 사용하면 결제, 제품 세부 사항, 장바구니 및 미니 장바구니 페이지에 표시할 수 있는 PayPal 단추를 사용자 지정할 수 있습니다. PayPal의 내부 연구는 기본 옵션이 쉽게 인식할 수 있고 구매율을 높일 수 있지만, 기본 옵션이 스토어 스타일과 일치하지 않을 수 있다는 것을 시사합니다. 다음을 선택할 수 있습니다.

- PayPal 단추의 크기, 색상 및 모양
- PayPal 단추에 나타나는 텍스트
- 레이아웃입니다. 여러 개의 단추가 표시되는 경우(가로 또는 세로)

단추를 사용자 지정하려면 다음을 확장합니다. ![확장 선택기](../assets/icon-display-expand.png) 다음 각 섹션을 참조하고 설정을 조정합니다.

- **[!UICONTROL Checkout Page]**
- **[!UICONTROL Product Pages]**
- **[!UICONTROL Cart Page]**
- **[!UICONTROL Mini Cart]**

![체크아웃 페이지 설정](../configuration-reference/sales/assets/payment-methods-paypal-payments-advanced-frontend-experience-settings2.png){width="600" zoomable="yes"}

**_각 페이지 유형에 대한 단추 표시를 구성하려면 다음 작업을 수행하십시오._**

1. 확장 ![확장 선택기](../assets/icon-display-expand.png) 섹션.

1. 설정 **[!UICONTROL Customize Button]** 끝 `Yes`.

1. PayPal이 스마트 결제 단추에 표시하는 텍스트를 설정하려면 다음을 설정합니다. **[!UICONTROL Label]** 다음 중 하나를 수행합니다.

   - `Checkout` - PayPal 결제
   - `Pay` - PayPal 결제
   - `Buy Now` - PayPal로 지금 구입
   - `PayPal` - PayPal
   - `Installment`  - PayPal
   - `Credit` - PayPal 신용

1. 설정 **[!UICONTROL Layout]** 다음 중 하나를 수행합니다.

   - `Vertical` - (기본값) PayPal 스마트 단추를 세로로 표시합니다. 구매자는 PayPal에 로그인하거나 여부에 관계없이 PayPal 계정을 만들어야 합니다 **[!UICONTROL Enable Guest Checkout]** 이(가) 선택되어 있습니다.
   - `Horizontal` - PayPal 스마트 단추를 가로로 표시합니다. 날짜 **[!UICONTROL Enable Guest Checkout]** 이(가) 선택되어 있으면 **[!UICONTROL Pay with Debit Card or Credit Card]** PayPal 팝업 창에 단추가 표시됩니다. 그렇지 않으면 구매자가 PayPal에 로그인하거나 PayPal 계정을 만들어야 합니다.

1. 설정 **[!UICONTROL Size]** 다음 중 하나를 수행합니다.

   - `Medium` - 250픽셀 x 35픽셀.
   - `Large` - 350픽셀 x 40픽셀.
   - `Responsive` - (기본값) 컨테이너의 너비에 맞게 조정됩니다. 최소 너비는 100픽셀이고 최대 너비는 500픽셀입니다. 높이는 너비에 따라 동적으로 조정됩니다.

1. 설정 **[!UICONTROL Shape]** 다음 중 하나를 수행합니다.

   - `Pill` - (기본값) 단추 모양이 알약 모양(가운데가 길고 끝이 구부러짐)입니다.
   - `Rectangle` - 사각형 안에 커브가 없는 사각형 모양.

1. 설정 **[!UICONTROL Color]** 다음 중 하나를 수행합니다.

   - `Gold` (기본값)
   - `Blue`
   - `Silver`
   - `Black`

#### 기능

기능 설정을 사용하면 이 PayPal 솔루션과 관련된 특정 기능을 비활성화할 수 있습니다.

1. 확장 ![확장 선택기](../assets/icon-display-expand.png) 다음 **[!UICONTROL Features]** 섹션.

   ![체크아웃 페이지 설정](../configuration-reference/sales/assets/payment-methods-paypal-payments-advanced-frontend-experience-settings3.png){width="600" zoomable="yes"}

1. 설정 **[!UICONTROL Disable Funding Options]** 에 표시되는 다른 PayPal 자금 옵션을 결정하려면 _체크아웃_ 페이지를 가리키도록 업데이트하는 중입니다.

   선택한 옵션이에 표시되지 않음 _체크아웃_ 페이지를 가리키도록 업데이트하는 중입니다. 선택하지 않은 옵션은 PayPal이 스토어 통화 및 구매자 위치를 지원하는 경우에만 표시됩니다. 옵션은 다음과 같습니다.

   - PayPal 신용
   - 벤모
   - PayPal Guest 체크아웃 신용카드 아이콘
   - Elektronisches Lastschriftverfahren - 독일어 ELV

[1]: https://www.paypal.com/webapps/mpp/how-to-sell-online
[2]: https://www.paypal.com/webapps/mpp/buying-online
[3]: https://manager.paypal.com/
[4]: https://www.paypalobjects.com/en_AU/vhelp/paypalmanager_help/credit_card_numbers.htm
[5]: https://www.paypal.com/rs/webapps/mpp/express-checkout
[6]: https://demo.paypal.com/us/demo/navigation?merchant=bigbox&amp;amp;page=incontextProductCheckout
[7]: https://developer.paypal.com/docs/api-basics/sandbox/
