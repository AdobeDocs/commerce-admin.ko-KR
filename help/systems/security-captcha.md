---
title: CAPTCHA
description: 등록된 고객이 시작한 관리자 액세스 및 다양한 상점 내 작업에 대해 CAPTCHA를 구성하는 방법에 대해 알아봅니다.
exl-id: b2867ad5-7d48-4e9f-b84e-3cf0a14ec16f
role: Admin
feature: Configuration, Security
source-git-commit: 61df9a4bcfaf09491ae2d353478ceb281082fa74
workflow-type: tm+mt
source-wordcount: '942'
ht-degree: 0%

---

# CAPTCHA

CAPTCHA는 컴퓨터(또는 &quot;보트&quot;)가 아닌 사람이 사이트와 상호 작용하도록 보장하는 시각적 장치입니다. CAPTCHA는 의 약어입니다 _컴퓨터와 인간을 구분하기 위해 완전히 자동화된 공공 튜링 테스트_. 관리자 액세스 및 등록된 고객이 시작한 다양한 상점 첫 번째 작업 모두에 사용할 수 있습니다. Adobe Commerce 및 Magento Open Source은 이 항목 및 [Google recaptcha](security-google-recaptcha.md).

이미지의 오른쪽 상단에 있는 다시 로드 아이콘을 클릭하여 CAPTCHA를 필요한 만큼 다시 로드할 수 있습니다. CAPTCHA는 완전히 구성 가능하며 설정될 수 있으며, 매번 또는 정의된 로그인 시도 실패 횟수가 지정된 후에만 나타납니다.

![CAPTCHA로 로그인](./assets/customer-account-login-captcha.png){width="700" zoomable="yes"}

## 관리자용 CAPTCHA 구성

보안 수준을 높이기 위해 관리자 로그인 및 암호 찾기 페이지에 CAPTCHA를 추가할 수 있습니다. 관리자 사용자는 다음을 클릭하여 표시된 CAPTCHA를 다시 로드할 수 있습니다. _다시 로드_ ![다시 로드 아이콘](./assets/CAPTCHA-icon-reload.png) 아이콘: 이미지의 오른쪽 위 모서리에 있습니다. 다시 로드 횟수는 제한이 없습니다.

![책임자 - CAPTCHA로 로그인](./assets/security-captcha-admin.png){width="300"}

1. 다음에서 _관리자_ 사이드바, 이동 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. 왼쪽 패널에서 를 확장합니다. **[!UICONTROL Advanced]** 및 선택 **[!UICONTROL Admin]**.

1. 오른쪽 상단에서 를 설정합니다. **[!UICONTROL Store View]** 끝 `Default`.

   다음과 같은 경우 [범위](../getting-started/websites-stores-views.md#scope-settings) Commerce 설치에 여러 웹 사이트가 포함된 경우 CAPTCHA 구성을 적용할 웹 사이트를 선택합니다.

1. 확장 ![확장 선택기](../assets/icon-display-expand.png) 다음 **[!UICONTROL CAPTCHA]** 섹션.

1. 설정 **[!UICONTROL Enable CAPTCHA in Admin]** 끝 `Yes`. 그런 다음 나머지 옵션을 다음과 같이 완료합니다.

   ![책임자 - CAPTCHA 구성](../configuration-reference/advanced/assets/admin-captcha.png){width="600" zoomable="yes"}

   - 의 이름을 입력합니다. **[!UICONTROL Font]** CAPTCHA 기호에 사용(기본값: `LinLibertine`).

     고유한 글꼴을 추가하려면 글꼴 파일이 Commerce 설치와 동일한 디렉터리에 있어야 하며 `config.xml` 의 Captcha 모듈 파일 `app/code/Magento/Captcha/etc`.

   - 다음 중 하나를 선택합니다 **[!UICONTROL Forms]** CAPTCHA를 사용할 위치입니다. 여러 양식을 선택하려면 Ctrl 키(PC) 또는 Command 키(Mac)를 누른 채로 선택합니다.

      - `Admin Login`
      - `Admin Forgot Password`

   - 설정 **[!UICONTROL Displaying Modes]** 다음 중 하나를 수행합니다.

      - `Always` — CAPTCHA는 항상 관리자에 로그인해야 합니다.
      - `After number of attempts to login` — 이 옵션은 관리자 로그인 양식에만 적용됩니다. 선택한 경우 _[!UICONTROL Number of Unsuccessful Attempts to Login]_필드가 나타납니다. 허용할 로그인 시도 횟수를 입력합니다. 값이 0(영)이면 표시 모드를 로 설정하는 것과 비슷합니다 `Always`.

     실패한 로그인 시도 횟수를 추적하기 위해 하나의 이메일 주소와 하나의 IP 주소에서 로그인을 시도한 각 시도가 계산됩니다. 동일한 IP 주소에서 허용되는 최대 로그인 시도 횟수는 1,000회입니다. 이 제한은 CAPTCHA가 활성화된 경우에만 적용됩니다.

   - 대상 **[!UICONTROL Number of Unsuccessful Attempts to Login]** CAPTCHA가 나타나기 전에 관리자가 로그인을 시도할 수 있는 횟수를 입력합니다. 0으로 설정된 경우(`0`), CAPTCHA는 항상 필요합니다.

   - 대상 **[!UICONTROL CAPTCHA Timeout (minutes)]**: CAPTCHA가 만료될 때까지 걸리는 시간(분)을 입력합니다. CAPTCHA가 만료되면 관리자는 페이지를 다시 로드해야 합니다.

   - 다음을 입력합니다. **[!UICONTROL Number of Symbols]** CAPTCHA에 표시 최대 8개(`8`) 기호를 사용할 수 있습니다. 각 CAPTCHA에 따라 변경되는 다양한 수의 기호에 대해 범위(예: `5-8`).

   - 대상 **[!UICONTROL Symbols Used in CAPTCHA]** CAPTCHA에 임의로 표시할 문자(a-z 및 A-Z)와 숫자(0-9)를 입력합니다. 다른 기호와 구분하기 어려운 기호(예: ) `i`, `l`, 또는 `1`는 기본 CAPTCHA 기호 집합에 포함되지 않습니다.

   - 설정 **[!UICONTROL Case Sensitive]** 끝 `Yes` 관리자가 CAPTCHA에 표시된 대로 정확히 대문자나 소문자로 입력하도록 하려면 다음을 수행합니다.

1. 완료되면 다음을 클릭하십시오. **[!UICONTROL Save Config]**.

## 상점 첫 화면의 CAPTCHA 구성

고객이 계정에 로그인할 때마다 또는 로그인을 여러 번 시도한 후 CAPTCHA를 입력해야 할 수 있습니다. 또한 상점 전체에서 사용되는 다양한 양식은 CAPTCHA에 의한 확인이 필요하도록 구성할 수 있습니다.

![체크아웃 중 CAPTCHA](./assets/storefront-checkout-payment-captcha.png){width="700" zoomable="yes"}

1. 다음에서 _관리자_ 사이드바, 이동 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. 왼쪽 패널에서 를 확장합니다. **[!UICONTROL Customers]** 및 선택 **[!UICONTROL Customer Configuration]**.

1. 확장 ![확장 선택기](../assets/icon-display-expand.png) 다음 **[!UICONTROL CAPTCHA]** 섹션.

![고객 CAPTCHA 구성](../configuration-reference/customers/assets/customer-configuration-captcha.png){width="600" zoomable="yes"}

1. 설정 **[!UICONTROL Enable CAPTCHA on Storefront]** 끝 `Yes`. 그런 다음 나머지 옵션을 다음과 같이 완료합니다.

   - 의 이름을 입력합니다. **[!UICONTROL Font]** CAPTCHA 기호에 사용(기본값: `LinLibertine`).

     고유한 글꼴을 추가하려면 글꼴 파일이 Commerce 설치와 동일한 디렉터리에 있어야 하며 `config.xml` CAPTCHA 모듈의 파일입니다.

   - 다음 중 하나를 선택합니다 **[!UICONTROL Forms]** CAPTCHA를 사용할 위치입니다. 여러 양식을 선택하려면 Ctrl 키(PC) 또는 Command 키(Mac)를 누른 채로 선택합니다.

      - `Applying coupon code`
      - `Checkout/Placing Order`
      - `Create user`
      - `Login`
      - `Forgot password`
      - `Contact Us`
      - `Change password`
      - `Share Wishlist Form`
      - `Payflow Pro` (참조 [보안 패치](https://experienceleague.adobe.com/docs/commerce-knowledge-base/kb/troubleshooting/payments/paypal-payflow-pro-active-carding-activity.html) _기술 자료_ 기사)
      - `Send to Friend Form` ![Magento Open Source](../assets/open-source.svg) (Magento Open Source 전용)
      - `Add Gift Card Code` ![Adobe Commerce](../assets/adobe-logo.svg) (Adobe Commerce 전용)
      - `Create company` ![Adobe Commerce](../assets/b2b.svg) (Adobe Commerce B2B에서만 사용 가능)

   - 설정 **[!UICONTROL Displaying Mode]** 다음 중 하나를 수행합니다.

      - `Always` — 선택한 양식에 액세스하려면 항상 CAPTCHA가 필요합니다.
      - `After number of attempts to login` — CAPTCHA가 나타나기 전에 로그인 시도 횟수를 입력합니다. 값이 0(영)이면 &quot;항상&quot;과 비슷합니다. 선택하면 실패한 로그인 시도 횟수가 표시됩니다. 이 옵션은 암호 분실 양식에는 적용되지 않으며 활성화된 경우 항상 CAPTCHA를 표시합니다.

   - 대상 **[!UICONTROL Number of Unsuccessful Attempts to Login]**&#x200B;에 CAPTCHA가 나타나기 전에 고객이 성공적으로 로그인할 수 없는 횟수를 입력합니다. 0으로 설정된 경우(`0`), CAPTCHA는 항상 사용됩니다.

   - 대상 **[!UICONTROL CAPTCHA Timeout (minutes)]**: CAPTCHA가 만료될 때까지 걸리는 시간(분)을 입력합니다. CAPTCHA가 만료되면 고객은 페이지를 다시 로드하여 새 CAPTCHA를 생성해야 합니다.

   - 다음을 입력합니다. **[!UICONTROL Number of Symbols]** CAPTCHA에 표시 최대 8개(`8`) 기호를 사용할 수 있습니다. 각 CAPTCHA에 따라 변경되는 다양한 수의 기호에 대해 범위(예: `5-8`).

   - 대상 **[!UICONTROL Symbols Used in CAPTCHA]** CAPTCHA에 임의로 표시할 문자(a-z 및 A-Z)와 숫자(0-9)를 입력합니다. 기본 문자 집합에는 다음과 같은 유사한 기호가 포함되지 않습니다. `I` 또는 `1`. 최상의 결과를 얻으려면 사용자가 쉽게 식별할 수 있는 기호를 사용하십시오.

   - 설정 **[!UICONTROL Case Sensitive]** 끝 `Yes` 고객이 CAPTCHA에 표시된 대로 정확히 대문자나 소문자로 문자를 입력하도록 하려는 경우.

1. 완료되면 다음을 클릭하십시오. **[!UICONTROL Save Config]**.
