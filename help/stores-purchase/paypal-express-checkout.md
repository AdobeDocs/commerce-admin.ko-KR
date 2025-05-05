---
title: PayPal Express 체크아웃
description: 스토어에서 온라인 결제 솔루션으로 PayPal Express Checkout을 설정하는 방법에 대해 알아봅니다.
exl-id: 0cd90306-cf47-4a5f-8994-6ae96904ae2f
feature: Payments
source-git-commit: 8b5af316ab1d2e632ed5fc2066974326830ab3f7
workflow-type: tm+mt
source-wordcount: '3093'
ht-degree: 0%

---

# PayPal Express 체크아웃

PayPal Express Checkout은 고객에게 신용카드 또는 개인 PayPal 계정의 보안을 통해 결제할 수 있는 기능을 제공함으로써 판매 증대에 도움이 됩니다. 체크아웃 중에 고객이 보안 PayPal 사이트로 리디렉션되어 결제 정보를 완료합니다. 그런 다음 고객이 저장소로 돌아가 나머지 체크아웃 프로세스를 완료합니다. &#39;익스프레스 체크아웃&#39;을 선택하면 익숙한 &#39;페이팔&#39; 버튼이 매장에 추가돼 매출을 높이는 것으로 알려졌다.

>[!IMPORTANT]
>
>**PSD2 요구 사항:** <br/>
>2019년 9월 14일부터 유럽 은행은 [PSD2](../getting-started/compliance-payment-services-directive.md) 요구 사항을 충족하지 않는 결제를 거절할 수 있습니다. 모든 요구 사항이 PayPal에 의해 처리되므로 PayPal Express Checkout에서 PSD2를 준수하는 데 필요한 작업은 없습니다.

현재 PayPal 계정이 있는 고객은 _[!UICONTROL Check out with PayPal]_&#x200B;단추를 클릭하여 한 단계로 구매할 수 있습니다. Express Checkout은 독립 실행형으로 사용하거나 PayPal 올인원 솔루션 중 하나와 함께 사용할 수 있습니다. 이미 온라인에서 신용카드를 받고 있다면, 페이팔로 결제하기를 선호하는 신규 고객을 유치하기 위한 추가 옵션으로 &#39;익스프레스 체크아웃&#39;을 제공하면 된다.

>[!NOTE]
>
>PayPal은 PayPal Express Checkout을 통해 디지털 상품을 판매하는 데 더 이상 지원되지 않으며, [PayPal 결제 표준](paypal-payments-standard.md) 또는 다른 PayPal 결제 게이트웨이를 사용하여 [가상 제품](../catalog/product-create-virtual.md)을 포함하는 주문을 처리할 것을 권장합니다.

## 요구 사항

- 판매자: [Business PayPal 계정][1]
- 고객: [개인 PayPal 계정][2]

## 빠른 체크아웃 워크플로우

다른 결제 방식과 달리 페이팔 익스프레스 체크아웃은 제품 페이지, 미니 장바구니, 장바구니에서 일반적인 체크아웃 워크플로 시작 시 고객이 체크아웃할 수 있도록 했다.

1. **고객 주문** - 고객이 _[!UICONTROL Check out with PayPal]_&#x200B;단추를 클릭/탭합니다.
1. **고객이 PayPal 사이트로 리디렉션됨** - 고객이 거래를 완료하기 위해 PayPal 사이트로 리디렉션됩니다.
1. **고객이 PayPal 계정에 로그인함** - 거래를 완료하려면 고객이 PayPal 계정에 로그인해야 합니다. 결제 시스템은 PayPal 계정의 청구 및 배송 정보를 사용합니다.
1. **고객이 체크아웃 페이지로 돌아가기** - 고객이 주문을 검토하도록 스토어의 체크아웃 페이지로 다시 리디렉션됩니다.
1. **고객 주문** - 고객이 주문을 하고 주문 정보가 PayPal에 제출됩니다.
1. **PayPal로 트랜잭션 처리** - PayPal로 주문을 받고 트랜잭션을 처리합니다.

>[!NOTE]
>
>PayPal Express Checkout은 여러 주소가 있는 주문을 지원하지 않습니다.

## 컨텍스트 내 체크아웃

PayPal의 _직접 체크아웃_&#x200B;을 사용하면 보다 간편하게 온라인으로 결제할 수 있습니다. 고객은 이 간단한 1~2번의 클릭으로 매끄러운 체크아웃을 수행하는 동안 스토어를 놓치지 않습니다. Mac과 PC에서도 상황에 맞는 체크아웃 기능이 동일하게 작동하며 데스크탑 컴퓨터, 태블릿 및 모바일 장치에서 일관된 경험을 제공합니다. 자세한 내용은 [빠른 체크아웃에서 직접 체크아웃][5]을 참조하세요.

![PayPal 컨텍스트 내 체크아웃 데모](./assets/storefront-paypal-in-context.png){width="700" zoomable="yes"}

[_PayPal 컨텍스트 내 체크아웃 데모_][6]

[!DNL PayPal Express Checkout]에 대한 저장소를 구성할 때 이 옵션을 활성화할 수 있습니다.

## PayPal 계정 구성

Commerce Admin에서 PayPal Express Checkout을 설정하기 전에 PayPal 웹 사이트에서 판매자 계정을 구성해야 합니다.

1. [manager.paypal.com][3]에서 PayPal 고급 계정에 로그인합니다.

1. **[!UICONTROL Service Settings]** > **[!UICONTROL Hosted Checkout Pages]** > **[!UICONTROL Set Up]**(으)로 이동하여 다음 설정을 만듭니다.

   - **[!UICONTROL AVS]**: `No`
   - **[!UICONTROL CSC]**: `No`
   - **[!UICONTROL Enable Secure Token]**: `Yes`

1. **[!UICONTROL Save Changes]**&#x200B;을(를) 클릭합니다.

1. 다른 사용자 설정(PayPal 권장):

   - [manager.paypal.com][3] (으)로 이동하여 계정에 로그인합니다.

   - 다른 사용자를 설정하려면 지침을 따르십시오.

   - **[!UICONTROL Update]**&#x200B;을(를) 클릭합니다.

## Commerce에서 PayPal Express 체크아웃 설정

두 개의 PayPal 솔루션이 동시에 활성화될 수 있습니다. PayPal Express Checkout 및 올인원 솔루션입니다. 다른 솔루션을 활성화하면 이전에 사용한 솔루션이 자동으로 비활성화됩니다.

>[!NOTE]
>
>언제든지 **[!UICONTROL Save Config]**&#x200B;을(를) 클릭하여 진행 상황을 저장합니다.

### 1단계: 구성 시작

1. _관리자_ 사이드바에서 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**(으)로 이동합니다.

1. 왼쪽 패널에서 **[!UICONTROL Sales]**&#x200B;을(를) 확장하고 **[!UICONTROL Payment Methods]**&#x200B;을(를) 선택합니다.

1. 설치에 웹 사이트, 스토어 또는 보기가 여러 개 있는 경우 이 구성을 적용할 스토어 보기로 **[!UICONTROL Store View]**&#x200B;을(를) 설정합니다.

1. _[!UICONTROL Merchant Location]_&#x200B;섹션에서 비즈니스가 있는&#x200B;**[!UICONTROL Merchant Country]**&#x200B;을(를) 선택합니다.

   이 설정은 구성에 나타나는 PayPal 솔루션의 선택을 결정합니다.

   ![판매자 국가](../configuration-reference/sales/assets/payment-methods-merchant-location.png){width="600" zoomable="yes"}

1. _[!UICONTROL Recommended Solutions]_&#x200B;에서&#x200B;**[!UICONTROL PayPal Express Checkout]**&#x200B;에 대해&#x200B;**[!UICONTROL Configure]**&#x200B;을(를) 클릭합니다.

   ![PayPal Express 체크아웃 구성](./assets/paypal-express-checkout.png){width="600"}

### 2단계: PayPal 계정 활성화 및 연결

1. 필요한 경우 **[!UICONTROL Required PayPal Settings]** 섹션에서 ![확장 선택기](../assets/icon-display-expand.png)를 확장합니다.

   ![PayPal 계정 연결](./assets/paypal-express-required.png){width="600" zoomable="yes"}

1. 테스트 또는 프로덕션용 계정 연결:

   - 테스트(개발) 모드를 위해 **[!UICONTROL Sandbox Credentials]**&#x200B;을(를) 클릭하고 [PayPal 샌드박스][7] 자격 증명을 입력하십시오.
   - 프로덕션 모드의 경우 **[!UICONTROL Connect with PayPal]**&#x200B;을(를) 클릭하고 프로덕션 계정 자격 증명을 입력합니다.

   연결이 확인되면 계속 진행할 수 있습니다.

1. **[!UICONTROL Enable this Solution]**&#x200B;을(를) `Yes`(으)로 설정합니다.

1. [PayPal 컨텍스트 내 체크 아웃](#in-context-checkout)을 사용하려면:

   - **[!UICONTROL Enable In-Context Checkout Experience]**&#x200B;을(를) `Yes`(으)로 설정합니다.

   - PayPal **[!UICONTROL Merchant Account ID]**&#x200B;을(를) 입력하십시오.

     판매자 계정 ID는 PayPal 비즈니스 계정 프로필에 있습니다.

>[!NOTE]
>
>[PayPal 크레딧](paypal.md#paypal-credit-and-pay-later)이(가) 이 결제 옵션에 대해 기본적으로 활성화되어 있습니다.

### 3단계: 필요한 PayPal 설정 완료

1. 필요한 경우 **[!UICONTROL Express Checkout]** 섹션에서 ![확장 선택기](../assets/icon-display-expand.png)를 확장합니다.

   ![PayPal Express 체크 아웃 필수 설정](./assets/paypal-express-settings.png){width="600" zoomable="yes"}

1. (선택 사항) **[!UICONTROL Email Associated with PayPal Merchant Account]**&#x200B;을(를) 입력합니다.

   >[!IMPORTANT]
   >
   >이메일 주소는 대소문자를 구분합니다. 결제를 받으려면 입력한 이메일 주소가 PayPal 판매자 계정에 지정된 이메일 주소와 일치해야 합니다.

   PayPal 계정이 없는 경우 **[!UICONTROL Start accepting payments via PayPal]**&#x200B;을(를) 클릭합니다.

1. **[!UICONTROL API Authentication Methods]**&#x200B;을(를) 다음 중 하나로 설정합니다.

   - `API Signature` - 이 PayPal 인증 방법은 구현하기 가장 쉬운 방법이며 사용자 이름, 암호 및 계정을 식별하는 고유한 문자열과 숫자를 기반으로 합니다. API 서명 자격 증명이 만료되지 않습니다.
   - `API Certificate` - 이 PayPal 인증 방법은 보다 안전하며 사용자 이름, 암호 및 다운로드 가능한 인증서를 기반으로 합니다. API 자격 증명은 3년 후에 만료되며 갱신해야 합니다.

   필요한 경우 다음을 완료합니다.

   - **[!UICONTROL API Username]**
   - **[!UICONTROL API Password]**
   - **[!UICONTROL API Signature]**

1. 샌드박스 계정의 자격 증명을 사용하는 경우 **[!UICONTROL Sandbox Mode]**&#x200B;을(를) `Yes`(으)로 설정하십시오.

   샌드박스에서 구성을 테스트할 때 PayPal에서 권장하는 [신용 카드 번호][4]만 사용하십시오. 프로덕션으로 전환할 준비가 되면 구성으로 돌아가서 샌드박스 모드를 `No`(으)로 설정하고 프로덕션 PayPal 계정에 연결합니다.

1. 시스템이 프록시 서버를 사용하여 Commerce과 PayPal 결제 시스템 간의 연결을 설정하는 경우 **[!UICONTROL API Uses Proxy]**&#x200B;을(를) `Yes`(으)로 설정하고 다음을 완료하십시오.

   - **[!UICONTROL Proxy Host]**
   - **[!UICONTROL Proxy Port]**

이 단계 순서가 끝나면 필요한 PayPal 설정이 완료됩니다. 기본 및 고급 설정을 계속 사용하거나 **[!UICONTROL Save Config]**&#x200B;을(를) 클릭하고 나중에 돌아와서 구성을 조정할 수 있습니다

### 단계 4: Advertising PayPal 크레딧/Advertising PayPal PayLater 설정(선택 사항)

2.4.3 릴리스부터 PayPal PayLater는 PayPal이 포함된 배포에서 지원됩니다. 이 기능을 통해 구매자는 구매 시 전체 금액을 지불하는 대신 2주 단위로 주문 금액을 지불하는 것이 가능하다. PayPal 크레딧 경험은 더 이상 사용되지 않습니다.

**[!UICONTROL Enable PayPal PayLater Experience]**&#x200B;을(를) 다음 중 하나로 설정합니다.

- `Yes` - Advertising PayPal PayLater를 설정하려면
- `No` - Advertising PayPal 크레딧을 설정하려면

>[!NOTE]
>
>**[!UICONTROL Enable PayPal PayLater Experience]** 설정은 [!DNL PayPal PayLater] 기능을 사용하지 않도록 설정하지 않으며 상점 앞에서 **_[!UICONTROL PayPal PayLater]_** 단추를 제거하지 않습니다. 상점 전면에서 **_[!UICONTROL PayPal PayLater]_** 및 **_[!UICONTROL PayPal Credit]_** 단추를 모두 사용하지 않으려면 **[!UICONTROL Disable Funding Options]** 설정([!UICONTROL Frontend Experience Settings]의 [!UICONTROL Advanced Settings])에 대한 `PayPal Credit` 값을 선택해야 합니다.

#### PayPal 크레딧 광고

1. **[!UICONTROL Advertise PayPal Credit]** 섹션에서 ![확장 선택기](../assets/icon-display-expand.png)를 확장합니다.

1. 계정 정보를 보려면 **[!UICONTROL Get Publisher ID from PayPal]**&#x200B;을(를) 클릭하고 지침을 따르십시오.

1. **[!UICONTROL Publisher ID]**&#x200B;을(를) 입력하십시오.

   ![PayPal 크레딧 알림](../configuration-reference/sales/assets/payment-methods-paypal-payments-advanced-advertise-paypal-credit.png){width="600" zoomable="yes"}

1. **[!UICONTROL Home Page]** 섹션에서 ![확장 선택기](../assets/icon-display-expand.png)를 확장합니다.

1. 페이지에 배너를 배치하려면 **[!UICONTROL Display]**&#x200B;을(를) `Yes`(으)로 설정합니다.

1. **[!UICONTROL Position]**&#x200B;을(를) 다음 중 하나로 설정합니다.

   - `Header (center)`
   - `Sidebar (right)`

1. **[!UICONTROL Size]**&#x200B;을(를) 다음 중 하나로 설정합니다.

   - `190 x 100`
   - `234 x 60`
   - `300 x 50`
   - `468 x 60`
   - `728 x 90`
   - `800 x 66`

   ![PayPal 크레딧 홈 페이지 설정 알림](../configuration-reference/sales/assets/payment-methods-paypal-payments-advanced-advertise-paypal-credit-home-page.png){width="600" zoomable="yes"}

1. 나머지 ![확장 선택기](../assets/icon-display-expand.png)를 확장하고 이전 단계를 반복합니다.

   - [!UICONTROL Catalog Category Page]
   - [!UICONTROL Catalog Product Page]
   - [!UICONTROL Checkout Cart Page]

#### PayPal PayLater 광고

1. **[!UICONTROL Advertise PayPal PayLater]** 섹션에서 ![확장 선택기](../assets/icon-display-expand.png)를 확장합니다.

1. **[!UICONTROL Enable PayPal PayLater]**&#x200B;을(를) `Yes`(으)로 설정합니다.

1. **[!UICONTROL Home Page]** 섹션에서 ![확장 선택기](../assets/icon-display-expand.png)를 확장합니다.

1. 페이지에 배너를 배치하려면 **[!UICONTROL Display]**&#x200B;을(를) `Yes`(으)로 설정합니다.

1. **[!UICONTROL Position]**&#x200B;을(를) 다음 중 하나로 설정합니다.

   - `Header (center)`
   - `Sidebar`

1. **[!UICONTROL Style Layout]**&#x200B;을(를) 다음 중 하나로 설정합니다.

   - `Text`
   - `Flex`

1. [!UICONTROL Style Layout] **[!UICONTROL Text]**&#x200B;에 대해서만 **[!UICONTROL Logo Type]**&#x200B;을(를) 다음 중 하나로 설정하십시오.

   - `Primary`
   - `Alternative`
   - `Inline`
   - `None`

1. [!UICONTROL Style Layout] **[!UICONTROL Text]**&#x200B;에 대해서만 **[!UICONTROL Logo Position]**&#x200B;을(를) 다음 중 하나로 설정하십시오.

   - `Left`
   - `Right`
   - `Top`

1. [!UICONTROL Style Layout] **[!UICONTROL Text]**&#x200B;에 대해서만 **[!UICONTROL Text Color]**&#x200B;을(를) 다음 중 하나로 설정하십시오.

   - `Black`
   - `White`
   - `Monochrome`
   - `Grayscale`

1. [!UICONTROL Style Layout] **[!UICONTROL Text]**&#x200B;에 대해서만 **[!UICONTROL Text Size]**&#x200B;을(를) 다음 중 하나로 설정하십시오.

   - `10px`
   - `11px`
   - `12px`
   - `13px`
   - `14px`
   - `15px`
   - `16px`

1. [!UICONTROL Style Layout] **[!UICONTROL Flex]**&#x200B;에 대해서만 **[!UICONTROL Ratio]**&#x200B;을(를) 다음 중 하나로 설정하십시오.

   - `1x1`
   - `1x4`
   - `8x1`
   - `20x1`

1. [!UICONTROL Style Layout] **[!UICONTROL Flex]**&#x200B;에 대해서만 **[!UICONTROL Color]**&#x200B;을(를) 다음 중 하나로 설정하십시오.

   - `Blue`
   - `Black`
   - `White`
   - `White No Border`
   - `Gray`
   - `Monochrome`
   - `Grayscale`

   ![PayPal 크레딧 홈 페이지 설정 알림](../configuration-reference/sales/assets/payment-methods-paypal-payments-advanced-advertise-paypal-paylater-home-page.png){width="600" zoomable="yes"}

1. 나머지 ![확장 선택기](../assets/icon-display-expand.png)를 확장하고 이전 단계를 반복합니다.

   - [!UICONTROL Catalog Product Page]
   - [!UICONTROL Checkout Cart Page]
   - [!UICONTROL Checkout Payment Step]
   - [!UICONTROL Catalog Category Page]

### 5단계: 기본 설정 완료

1. **[!UICONTROL Basic Settings - PayPal Express Checkout]** 섹션에서 ![확장 선택기](../assets/icon-display-expand.png)를 확장합니다.

   ![기본 설정](../configuration-reference/sales/assets/payment-methods-paypal-express-checkout-basic-settings.png){width="600" zoomable="yes"}

1. **[!UICONTROL Title]**&#x200B;의 경우 체크아웃 중에 이 결제 방법을 식별하는 제목을 입력하십시오.

   모든 스토어 조회수에 _PayPal_ 제목을 사용하는 것이 좋습니다.

1. 여러 결제 방법을 제공하는 경우 **[!UICONTROL Sort Order]**&#x200B;에 대한 숫자를 입력하여 다른 결제 방법과 함께 나열될 때 PayPal Express Checkout이 표시되는 순서를 결정합니다.

   이 번호는 다른 결제 방법과 관련이 있습니다. (`0` = 첫 번째, `1` = 두 번째, `2` = 세 번째 등)

1. **[!UICONTROL Payment Action]**&#x200B;을(를) 다음 중 하나로 설정합니다.

   - `Authorization` - 구매를 승인하고 자금을 보류합니다. 판매자가 _캡처한_&#x200B;이 될 때까지 금액이 인출되지 않습니다.
   - `Sale` - 구매 금액이 승인되어 고객 계정에서 즉시 인출됩니다.
   - `Order` - 주문 금액이 PayPal의 고객 잔고, 은행 계좌 또는 신용 카드에서 수집되거나 승인되지 않습니다. 주문 결제 행위는 PayPal 결제 시스템과 가맹점 간의 계약을 나타냅니다. 머천트는 최대 29일 동안 고객 구매자 계정에서 주문된 총액까지 하나 이상의 금액을 캡처할 수 있습니다. 펀드가 주문된 후 판매사는 이후 29일 동안 언제든지 펀드를 캡처할 수 있다. 하나 이상의 송장을 생성하여 주문 금액을 캡처하는 작업은 Commerce 관리자만 수행할 수 있습니다.

1. 제품 페이지에 _[!UICONTROL Check out with PayPal]_&#x200B;단추를 표시하려면&#x200B;**[!UICONTROL Display on Product Details Page]**&#x200B;을(를) `Yes`(으)로 설정하십시오.

1. 결제 작업이 `Order`(으)로 설정된 경우 다음을 완료하십시오.

   - **[!UICONTROL Authorization Honor Period (days)]** - 기본 권한 부여가 유효한 기간을 결정합니다. 값은 PayPal 판매자 계정의 해당 값과 같아야 합니다. PayPal 판매자 계정의 기본값은 `3`입니다. 이 수를 늘리려면 PayPal에 문의해야 합니다. 미국 태평양 표준시 기준 마지막 날 오후 11시 49분에 인증이 유효하지 않게 됩니다.

   - **[!UICONTROL Order Valid Period (days)]** - 순서가 유효한 기간을 결정합니다. 주문이 무효화되면 더 이상 그에 대한 송장을 생성할 수 없습니다. PayPal 판매자 계정의 주문 유효 기간 값과 같은 값을 지정하십시오. PayPal 판매자 계정의 기본값은 `29`입니다. 이 번호를 변경하려면 PayPal에 문의해야 합니다.

   - **[!UICONTROL Number of Child Authorizations]** - 단일 주문에 대한 최대 승인 수를 지정하여 주문에 대해 생성할 수 있는 온라인 부분 송장의 최대 수를 결정합니다. 이 값은 PayPal 판매자 계정의 해당 설정과 같아야 합니다. PayPal 계정의 기본 자녀 인증 수는 `1`입니다. 이 수를 늘리려면 PayPal에 문의해야 합니다.

### 6단계: 고급 설정 완료

1. **[!UICONTROL Advanced Settings]** 섹션에서 ![확장 선택기](../assets/icon-display-expand.png)를 확장합니다.

   ![고급 설정 - PayPal Express 체크아웃](../configuration-reference/sales/assets/payment-methods-paypal-express-checkout-advanced-settings.png){width="600" zoomable="yes"}

1. **[!UICONTROL Display on Shopping Cart]**&#x200B;을(를) `Yes`(으)로 설정합니다.

1. **[!UICONTROL Payment Applicable From]**&#x200B;을(를) 다음 중 하나로 설정합니다.

   - `All Allowed Countries` - 스토어 구성에 지정된 모든 국가의 고객이 이 결제 방법을 사용할 수 있습니다.
   - `Specific Countries` - 이 옵션을 선택하면 _[!UICONTROL Payment from Specific Countries]_&#x200B;목록이 나타납니다. 여러 국가를 선택하려면 Ctrl 키(PC) 또는 Command 키(Mac)를 누른 채 각 항목을 클릭합니다.

1. 결제 시스템과의 통신을 로그 파일에 기록하려면 **[!UICONTROL Debug Mode]**&#x200B;을(를) `Yes`(으)로 설정합니다.

   PayPal Payments Advanced의 로그 파일은 `_payflow_advanced.log`입니다.

   >[!NOTE]
   >
   >PCI 데이터 보안 표준에 따라 신용 카드 정보는 로그 파일에 기록되지 않습니다.

1. 호스트 정품 인증을 사용하려면 **[!UICONTROL Enable SSL Verification]**&#x200B;을(를) `Yes`(으)로 설정하십시오.

1. PayPal 사이트의 항목별 고객 주문에 대한 전체 요약을 표시하려면 **[!UICONTROL Transfer Cart Line Items]**&#x200B;을(를) `Yes`(으)로 설정하십시오.

1. 요약에 최대 10개의 배송 옵션을 포함하려면 **[!UICONTROL Transfer Shipping Options]**&#x200B;을(를) `Yes`(으)로 설정하십시오. 이 옵션은 라인 항목이 이전으로 설정된 경우에만 나타납니다.

1. PayPal 수락 단추에 사용되는 이미지 형식을 확인하려면 **[!UICONTROL Shortcut Buttons Flavor]**&#x200B;을(를) 다음 중 하나로 설정하십시오.

   - `Dynamic` - (권장) PayPal 서버에서 동적으로 변경할 수 있는 이미지를 표시합니다.
   - `Static` - 동적으로 변경할 수 없는 특정 이미지를 표시합니다.

1. PayPal 계정이 없는 고객이 이 메서드를 사용하여 구매할 수 있도록 하려면 **[!UICONTROL Enable PayPal Guest Checkout]**&#x200B;을(를) `Yes`(으)로 설정하십시오.

1. **[!UICONTROL Require Customer's Billing Address]**&#x200B;을(를) 다음 중 하나로 설정합니다.

   - `Yes` - 모든 구매에 대해 고객의 청구 주소가 필요합니다.
   - `No` - 구매 시 고객의 결제 주소가 필요하지 않습니다.
   - `For Virtual Quotes Only` - 가상 견적에 대한 고객의 청구 주소만 필요합니다.

   >[!NOTE]
   >
   >이 기능은 PayPal 기술 지원을 통해 판매자 계정에 대해 활성화되어야 합니다.

1. (선택 사항) 고객 계정에 사용 가능한 활성 청구 계약이 없을 때 고객이 PayPal 결제 시스템의 스토어와 [청구 계약](paypal-billing-agreements.md)에 서명할 수 있도록 **[!UICONTROL Billing Agreement Signup]**&#x200B;을(를) 설정합니다.

   - `Auto` - 고객은 빠른 체크아웃 흐름 중에 청구 계약에 서명하거나 다른 결제 방법을 사용할 수 있습니다.
   - `Ask Customer` - 고객은 빠른 체크아웃 흐름 중에 청구 계약에 서명할지 여부를 결정할 수 있습니다.
   - `Never` - 고객이 빠른 체크아웃 흐름 중에 청구 계약에 서명할 수 없습니다.

   >[!NOTE]
   >
   >가맹점은 [PayPal 가맹점 기술 지원](https://developer.paypal.com/support/)에 요청하여 해당 계정에서 결제 계약을 사용하도록 설정해야 합니다. _청구 계약 등록_ 매개 변수는 PayPal에서 판매자 계정에 대해 청구 계약이 활성화되어 있음을 확인한 후에만 사용할 수 있습니다.

1. 고객이 주문 검토를 위해 스토어로 돌아가지 않고 PayPal 사이트에서 거래를 완료할 수 있도록 하려면 **[!UICONTROL Skip Order Review Step]**&#x200B;을(를) `Yes`(으)로 설정하십시오.

1. 스토어에 필요한 경우 추가 섹션을 완료합니다.

   - [PayPall 청구 계약 설정](#paypal-billing-agreement-settings)
   - [결제 보고서 설정](#settlement-report-settings)
   - [프론트엔드 경험 설정](#frontend-experience-settings)
   - [스마트 단추 사용자 지정](#customize-smart-buttons)
   - [기능](#features)

1. 완료되면 **[!UICONTROL Save Config]**&#x200B;을(를) 클릭합니다.

#### PayPal 청구 계약 설정

[청구 계약](paypal-billing-agreements.md)은(는) 여러 주문에서 사용하도록 PayPal에서 승인한 판매자와 고객 간의 판매 계약입니다. 체크아웃 프로세스 중에 청구 계약 결제 옵션은 이미 귀사와 청구 계약을 체결한 고객에게만 표시됩니다. PayPal이 계약을 승인한 후에는 결제 시스템에서 고유한 참조 ID를 발행하여 계약과 연관된 각 주문을 식별합니다. 구매 주문과 마찬가지로 고객이 귀사와 설정할 수 있는 청구 계약 수에는 제한이 없습니다.

1. **[!UICONTROL PayPal Billing Agreement Settings]** 섹션에서 ![확장 선택기](../assets/icon-display-expand.png)를 확장합니다.

   ![결제 계약 설정](../configuration-reference/sales/assets/payment-methods-paypal-express-checkout-billing-agreement-settings.png){width="600" zoomable="yes"}

1. **[!UICONTROL Enabled]**&#x200B;을(를) `Yes`(으)로 설정합니다.

1. **[!UICONTROL Title]**&#x200B;의 경우 체크아웃하는 동안 PayPal 결제 계약 방법을 식별하는 제목을 입력하십시오.

1. 여러 결제 방법을 제공하는 경우 **[!UICONTROL Sort Order]** 필드에 숫자를 입력하여 체크아웃 중에 다른 결제 방법과 함께 나열될 때 청구 계약이 표시되는 순서를 결정합니다.

1. **[!UICONTROL Payment Action]**&#x200B;을(를) 다음 중 하나로 설정합니다.

   - `Authorization` - 구매를 승인하고 자금을 보류합니다. 상인에게 &#39;포착&#39;되기 전까지는 그 금액이 인출되지 않는다.
   - `Sale` - 구매 금액이 승인되어 고객 계정에서 즉시 인출됩니다.

1. **[!UICONTROL Payment Applicable From]**&#x200B;을(를) 다음 중 하나로 설정합니다.

   - `All Allowed Countries` - 스토어 구성에 지정된 모든 국가의 고객이 이 결제 방법을 사용할 수 있습니다.
   - `Specific Countries` - 이 옵션을 선택하면 _[!UICONTROL Payment from Specific Countries]_&#x200B;목록이 나타납니다. 여러 국가를 선택하려면 Ctrl 키(PC) 또는 Command 키(Mac)를 누른 상태에서 각 국가를 클릭합니다.

1. 로그 파일에 결제 시스템과의 통신을 기록하려면 **[!UICONTROL Debug Mode]**&#x200B;을(를) `Yes`(으)로 설정합니다.

   >[!NOTE]
   >
   >로그 파일은 서버에 저장되며 개발자만 액세스할 수 있습니다. PCI 데이터 보안 표준에 따라 신용 카드 정보는 로그 파일에 기록되지 않습니다.

1. SSL 인증을 사용하려면 **[!UICONTROL Enable SSL Verification]**&#x200B;을(를) `Yes`(으)로 설정합니다.

1. PayPal 결제 페이지에서 고객 주문의 각 항목에 대한 요약을 표시하려면 **[!UICONTROL Transfer Cart Line Items]**&#x200B;을(를) `Yes`(으)로 설정하십시오.

1. 고객이 고객 계정의 대시보드에서 청구 계약을 시작할 수 있도록 하려면 **[!UICONTROL Allow in Billing Agreement Wizard]**&#x200B;을(를) `Yes`(으)로 설정하십시오.

#### 결제 보고서 설정

1. **[!UICONTROL Settlement Report Settings]** 섹션에서 ![확장 선택기](../assets/icon-display-expand.png)를 확장합니다.

   ![결제 보고서 설정](../configuration-reference/sales/assets/payment-methods-paypal-payments-advanced-settlement-report-settings.png){width="600" zoomable="yes"}

1. **[!UICONTROL SFTP Credentials]**&#x200B;의 경우 다음을 수행합니다.

   - PayPal 보안 FTP 서버에 등록한 경우 다음 SFTP 로그인 자격 증명을 입력하십시오.

      - 로그인
      - 암호

   - 사이트에서 빠른 체크아웃으로 _실행_ 전에 테스트 보고서를 실행하려면 **[!UICONTROL Sandbox Mode]**&#x200B;을(를) `Yes`(으)로 설정하십시오.

   - **[!UICONTROL Custom Endpoint Hostname or IP Address]** 입력.

     기본적으로 값은 `reports.paypal.com`입니다.

   - 보고서가 저장된 **[!UICONTROL Custom Path]**&#x200B;을(를) 입력하십시오.

     기본적으로 값은 `/ppreports/outgoing`입니다.

1. 일정에 따라 보고서를 생성하려면 **[!UICONTROL Scheduled Fetching]** 설정을 완료하십시오.

   - **[!UICONTROL Enable Automatic Fetching]**&#x200B;을(를) `Yes`(으)로 설정합니다.

   - **[!UICONTROL Schedule]**&#x200B;을(를) 다음 중 하나로 설정합니다.

      - `Daily`
      - `Every 3 Days`
      - `Every 7 Days`
      - `Every 10 Days`
      - `Every 14 Days`
      - `Every 30 Days`
      - `Every 40 Days`

     PayPal은 45일 동안 각 보고서를 유지합니다.

   - 보고서를 생성할 시간, 분, 초로 **[!UICONTROL Time of Day]**&#x200B;을(를) 설정합니다.

#### 프론트엔드 경험 설정

프론트엔드 경험 설정을 사용하여 사이트에 표시할 PayPal 로고를 선택하고 PayPal 판매자 페이지의 모양을 사용자 지정합니다.

1. **[!UICONTROL Frontend Experience Settings]** 섹션에서 ![확장 선택기](../assets/icon-display-expand.png)를 확장합니다.

   ![프론트엔드 환경 설정](../configuration-reference/sales/assets/payment-methods-paypal-payments-advanced-frontend-experience-settings1.png){width="600" zoomable="yes"}

1. 스토어의 PayPal 블록에 표시할 **[!UICONTROL PayPal Product Logo]**&#x200B;을(를) 선택하십시오.

   PayPal 로고는 4가지 스타일과 2가지 크기로 제공됩니다.

   - `No Logo`
   - `We Prefer PayPal (150 x 60 or 150 x 40)`
   - `Now Accepting PayPal (150 x 60 or 150 x 40)`
   - `Payments by PayPal (150 x 60 or 150 x 40)`
   - `Shop Now Using PayPal (150 x 60 or 150 x 40)`

1. PayPal 판매자 페이지의 모양을 사용자 지정하려면 다음을 수행하십시오.

   - PayPal 판매자 페이지에 적용할 **[!UICONTROL Page Style]**&#x200B;의 이름을 입력하십시오.

      - `paypal` - PayPal 페이지 스타일을 사용합니다.
      - `primary` - 계정 프로필에서 _primary_ 스타일로 식별한 페이지 스타일을 사용합니다.
      - `your_custom_value` - 계정 프로필에 지정된 사용자 지정 결제 페이지 스타일을 사용합니다.

   - **[!UICONTROL Header Image URL]**&#x200B;의 경우 결제 페이지의 왼쪽 위 모서리에 표시할 이미지의 URL을 입력하십시오. 최대 파일 크기는 750픽셀 너비 x 90픽셀 높이입니다.

     >[!NOTE]
     >
     >PayPal은 이미지가 보안(https) 서버에 있는 것을 권장합니다. 그렇지 않으면 _페이지에 보안 및 비보안 항목이 모두 포함되어 있습니다_.

   - 페이지의 색상을 설정하려면 다음 각 페이지에 대해 6자의 16진수 코드(기호 `#` 제외)를 입력하십시오.

      - **[!UICONTROL Header Background Color]** - 체크아웃 페이지 헤더의 배경색입니다.
      - **[!UICONTROL Header Border Color]** - 머리글 주변의 2픽셀 테두리 색입니다.
      - **[!UICONTROL Page Background Color]** - 체크아웃 페이지와 머리글 및 결제 양식 주변의 배경색입니다.

#### 스마트 단추 사용자 지정

_스마트 결제 단추_ 기능을 사용하면 결제, 제품 세부 사항, 장바구니 및 미니 장바구니 페이지에 표시할 수 있는 PayPal 단추를 사용자 지정할 수 있습니다. PayPal의 내부 연구는 기본 옵션이 쉽게 인식할 수 있고 구매율을 높일 수 있지만, 기본 옵션이 스토어 스타일과 일치하지 않을 수 있다는 것을 시사합니다. 다음을 선택할 수 있습니다.

- PayPal 단추의 크기, 색상 및 모양
- PayPal 단추에 나타나는 텍스트
- 레이아웃입니다. 여러 개의 단추가 표시되는 경우(가로 또는 세로)

단추를 사용자 지정하려면 ![확장 선택기](../assets/icon-display-expand.png)를 확장하고 다음 섹션을 각각 조정합니다.

- **[!UICONTROL Checkout Page]**
- **[!UICONTROL Product Pages]**
- **[!UICONTROL Cart Page]**
- **[!UICONTROL Mini Cart]**

![체크아웃 페이지 설정](../configuration-reference/sales/assets/payment-methods-paypal-payments-advanced-frontend-experience-settings2.png){width="600" zoomable="yes"}

**_각 페이지 유형에 대해 단추 표시를 구성하려면:_**

1. ![확장 선택기](../assets/icon-display-expand.png) 섹션을 확장합니다.

1. **[!UICONTROL Customize Button]**&#x200B;을(를) `Yes`(으)로 설정합니다.

1. PayPal이 스마트 결제 단추에 표시하는 텍스트를 설정하려면 **[!UICONTROL Label]**&#x200B;을(를) 다음 중 하나로 설정하십시오.

   - `Checkout` - PayPal 체크아웃
   - `Pay` - PayPal 체크아웃
   - `Buy Now` - PayPal로 지금 구입
   - `PayPal` - PayPal
   - `Installment` - PayPal
   - `Credit` - PayPal 신용

1. **[!UICONTROL Layout]**&#x200B;을(를) 다음 중 하나로 설정합니다.

   - `Vertical` - (기본값) PayPal 스마트 단추를 세로로 표시합니다. 구매자는 **[!UICONTROL Enable Guest Checkout]** 선택 여부와 관계없이 PayPal에 로그인하거나 PayPal 계정을 만들어야 합니다.
   - `Horizontal` - PayPal 스마트 단추를 가로로 표시합니다. **[!UICONTROL Enable Guest Checkout]**&#x200B;을(를) 선택하면 **[!UICONTROL Pay with Debit Card or Credit Card]** 단추가 PayPal 팝업 창에 표시됩니다. 그렇지 않으면 구매자가 PayPal에 로그인하거나 PayPal 계정을 만들어야 합니다.

1. **[!UICONTROL Size]**&#x200B;을(를) 다음 중 하나로 설정합니다.

   - `Medium` - 250픽셀 x 35픽셀.
   - `Large` - 350픽셀 x 40픽셀입니다.
   - `Responsive` - (기본값) 컨테이너의 너비에 맞게 조정됩니다. 최소 너비는 100픽셀이고 최대 너비는 500픽셀입니다. 높이는 너비에 따라 동적으로 조정됩니다.

1. **[!UICONTROL Shape]**&#x200B;을(를) 다음 중 하나로 설정합니다.

   - `Pill` - (기본값) 단추 모양이 알약 모양입니다(가운데 길이가 길고 끝이 구부러짐).
   - `Rectangle` - 사각형 안에 곡선이 없는 사각형 모양입니다.

1. **[!UICONTROL Color]**&#x200B;을(를) 다음 중 하나로 설정합니다.

   - `Gold`(기본값)
   - `Blue`
   - `Silver`
   - `Black`

#### 기능

기능 설정을 사용하면 이 PayPal 솔루션과 관련된 특정 기능을 비활성화할 수 있습니다.

1. **[!UICONTROL Features]** 섹션에서 ![확장 선택기](../assets/icon-display-expand.png)를 확장합니다.

   ![체크아웃 페이지 설정](../configuration-reference/sales/assets/payment-methods-paypal-payments-advanced-frontend-experience-settings3.png){width="600" zoomable="yes"}

1. **[!UICONTROL Disable Funding Options]**&#x200B;을(를) 설정하여 _체크아웃_ 페이지에 표시되는 다른 PayPal 자금 옵션을 결정합니다.

   선택한 옵션이 _체크아웃_ 페이지에 표시되지 않습니다. 선택하지 않은 옵션은 PayPal이 스토어 통화 및 구매자 위치를 지원하는 경우에만 표시됩니다. 옵션은 다음과 같습니다.

   - PayPal 신용
   - 벤모
   - PayPal Guest 체크아웃 신용카드 아이콘
   - Elektronisches Lastschriftverfahren - 독일어 ELV

[1]: https://www.paypal.com/webapps/mpp/how-to-sell-online
[2]: https://www.paypal.com/webapps/mpp/buying-online
[3]: https://manager.paypal.com/
[4]: https://www.paypalobjects.com/en_AU/vhelp/paypalmanager_help/credit_card_numbers.htm
[5]: https://www.paypal.com/rs/webapps/mpp/express-checkout
[6]: https://demo.paypal.com/us/demo/navigation?merchant=bigbox&amp;page=incontextProductCheckout
[7]: https://developer.paypal.com/docs/api-basics/sandbox/
