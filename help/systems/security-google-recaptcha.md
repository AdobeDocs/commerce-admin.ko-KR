---
title: Google recaptcha
description: 등록된 고객이 시작한 관리자 액세스 및 다양한 상점 활동을 위해 Google reCAPTCHA를 구성하는 방법에 대해 알아봅니다.
exl-id: c3b53702-0882-4ac4-9cf5-39fefc90005e
role: Admin
feature: Configuration, Security
source-git-commit: 9a68d9702cec9b812414d39e8d04c71751121a37
workflow-type: tm+mt
source-wordcount: '1061'
ht-degree: 0%

---

# Google recaptcha

[Google reCAPTCHA](https://developers.google.com/recaptcha)에서는 컴퓨터(또는 &quot;보트&quot;)가 아닌 사람이 웹 사이트와 상호 작용하고 있는지 확인합니다. 표준 Adobe Commerce 및 Magento Open Source [CAPTCHA](security-captcha.md)와 달리 Google reCAPTCHA는 다양한 표시 옵션 및 방법을 선택하여 향상된 보안을 제공합니다. 추가 웹 사이트 트래픽 정보는 Google reCAPTCHA 계정의 대시보드에서 사용할 수 있습니다.

Google reCAPTCHA는 관리자 및 상점 첫 페이지용으로 별도로 구성됩니다.

- 관리자의 경우, [로그인](../getting-started/admin-signin.md) 페이지에서 그리고 사용자가 암호 재설정을 요청할 때 Google reCAPTCHA를 사용할 수 있습니다. 표준 Commerce [CAPTCHA](security-captcha.md)도 사용하도록 설정된 경우 Google reCAPTCHA를 문제 없이 동시에 사용할 수 있습니다.

- 상점 전선의 경우 Google reCAPTCHA를 사용하여 [고객 계정](../customers/customer-sign-in.md)에 로그인하고 [문의하기](../getting-started/store-details.md#contact-us-form) 페이지에서 메시지를 보낼 수 있으며 기타 여러 상점 전선에서 메시지를 보낼 수 있습니다.

  ![Google reCAPTCHA - 고객 로그인](./assets/customer-account-login-recaptcha.png){width="700" zoomable="yes"}

Google reCAPTCHA는 다음과 같은 여러 가지 방법으로 구현할 수 있습니다.

- _reCAPTCHA v3 보이지 않음_ - 알고리즘을 사용하여 사용자 상호 작용을 평가하고 점수를 기반으로 사용자가 사람일 가능성을 결정합니다.

- _reCAPTCHA v2 보이지 않음_ — 사용자 상호 작용 없이 백그라운드 확인을 수행합니다. 사용자와 고객은 자동으로 확인되지만 문제를 완료하기 위해 특정 이미지를 선택해야 할 수도 있습니다.

- _reCAPTCHA v2(&quot;로봇이 아님&quot;)_ — _&quot;로봇이 아님&quot;_ 확인란으로 요청을 확인합니다.

>[!IMPORTANT]
>
>Google reCAPTCHA를 구성하기 전에 `PHP.ini` 파일에 다음 설정이 포함되어 있는지 확인하십시오. `allow_url_fopen = 1`. 이 경우 개발자 지원이 필요할 수 있습니다. 설치 안내서에서 [필수 PHP 설정](https://experienceleague.adobe.com/docs/commerce-operations/installation-guide/prerequisites/php-settings.html?lang=ko){:target="_blank"}을 참조하십시오.

## 1단계: Google reCAPTCHA 키 생성

Google reCAPTCHA를 사용하려면 API 키 쌍이 필요합니다. 이 키들은 reCAPTCHA 사이트를 통해 무료로 받아볼 수 있습니다. 키를 생성하기 전에 사용할 reCAPTCHA 유형을 알고 있어야 합니다.

1. Google reCAPTCHA 페이지를 열고 계정에 로그인합니다.

1. **[!UICONTROL Label]**&#x200B;의 경우 내부 참조용 키를 식별할 이름을 입력하십시오.

   Adobe Commerce 또는 Magento Open Source 설치에 사용되는 각 reCAPTCHA 유형에 하나의 키 세트가 필요합니다. 예: `Commerce Invisible`

1. **[!UICONTROL reCAPTCHA type]**&#x200B;의 경우 사용할 메서드를 선택하십시오.

   - _reCAPTCHA v3 보이지 않음_
   - _reCAPTCHA v2 보이지 않음_
   - _reCAPTCHA v2(&quot;I am not a robot&quot;)_

1. **[!UICONTROL Domain]**&#x200B;의 경우 스토어의 도메인을 입력하십시오. 예: mystore.com

   다른 도메인을 가진 저장소가 여러 개 있는 경우 각 도메인을 별도의 줄에 입력합니다.

   - 스토어 도메인 및 하위 도메인을 추가합니다.
   - 테스트를 위해 필요에 따라 `localhost`, 다른 로컬 VM 도메인 및 스테이징 도메인을 추가할 수 있습니다.

1. **[!UICONTROL Accept the reCAPTCHA Terms of Service]**&#x200B;에 대한 확인란을 선택하십시오.

1. (선택 사항) Google에서 문제 또는 의심되는 트래픽을 감지하면 알림을 보내려면 **[!UICONTROL Send alerts to owners]** 확인란을 선택하십시오.

1. 등록을 완료하고 키를 받으려면 **[!UICONTROL Submit]**&#x200B;을(를) 클릭하십시오.

   >[!IMPORTANT]
   >
   >모든 키를 모든 유형의 reCAPTCHA에 적용할 수 있는 것은 아니며, 키를 잘못 적용하면 예기치 않은 동작이 발생할 수 있습니다. 예를 들어 reCAPTCHA v2 &quot;I&#39;m not a robot&quot;에 대해 생성된 Google reCAPTCHA 키는 _reCAPTCHA v2 Invisible_&#x200B;에서 작동하지 않으며 reCAPTCHA가 활성화된 기능을 차단할 수 있습니다.

## 2단계: 관리자용 Google reCAPTCHA 구성

[!BADGE PaaS만]{type=Informative url="https://experienceleague.adobe.com/ko/docs/commerce/user-guides/product-solutions" tooltip="Adobe Commerce 온 클라우드 프로젝트(Adobe 관리 PaaS 인프라) 및 온프레미스 프로젝트에만 적용됩니다."}

1. 관리자 계정에 로그인합니다.

1. 관리 사이드바에서 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**(으)로 이동합니다.

1. 오른쪽 상단 모서리에서 **[!UICONTROL Store View]**&#x200B;을(를) `Default Config`(으)로 설정합니다.

1. 왼쪽 패널에서 **[!UICONTROL Security]**&#x200B;을(를) 확장하고 **[!UICONTROL Google reCAPTCHA Admin Panel]**&#x200B;을(를) 클릭합니다.

   >[!NOTE]
   >
   >구성할 각 필드에 대해 **[!UICONTROL Use system value]** 확인란의 선택을 취소합니다.

1. _[!DNL reCAPTCHA v2 ("I am not a robot")]_&#x200B;을(를) 사용하려면&#x200B;**[!UICONTROL reCAPTCHA v2 ("I am not a robot")]**&#x200B;섹션을 확장하고 다음을 수행하십시오.

   - **[!UICONTROL Google API Website Key]**&#x200B;의 경우 Google reCAPTCHA 계정을 등록할 때 이 reCAPTCHA 유형에 대해 만든 웹 사이트 키를 입력하십시오.

   - **[!UICONTROL Google API Secret Key]**&#x200B;의 경우 Google reCAPTCHA 계정과 연결된 비밀 키를 입력하십시오.

   - **[!UICONTROL Size]**&#x200B;의 경우 표시할 Google reCAPTCHA 상자의 크기를 선택하십시오. 옵션: `Normal (default)` / `Compact`

   - **[!UICONTROL Theme]**&#x200B;의 경우 Google reCAPTCHA 상자의 스타일을 지정하는 데 사용할 테마를 선택하십시오. 옵션: `Light Theme (default)` / `Dark Theme`

   - **[!UICONTROL Language Code]**&#x200B;의 경우 두 문자 코드를 입력하여 Google reCAPTCHA 텍스트 및 메시징에 사용되는 [언어를 지정하십시오](https://developers.google.com/recaptcha/docs/language).

   ![reCAPTCHA v2 - &quot;로봇이 아닙니다.&quot;](../configuration-reference/security/assets/recaptcha-admin-v2-not-robot.png){width="600" zoomable="yes"}

1. _[!DNL reCAPTCHA v2 Invisible]_&#x200B;을(를) 사용하려면&#x200B;**[!UICONTROL reCAPTCHA v2 Invisible]**&#x200B;섹션을 확장하고 다음을 수행하십시오.

   - **[!UICONTROL Google API Website Key]**&#x200B;의 경우 Google reCAPTCHA 계정을 등록할 때 이 reCAPTCHA 유형에 대해 만든 웹 사이트 키를 입력하십시오.

   - **[!UICONTROL Google API Secret Key]**&#x200B;의 경우 Google reCAPTCHA 계정과 연결된 비밀 키를 입력하십시오.

   - **[!UICONTROL Invisible Badge Position]**&#x200B;의 경우 각 페이지에서 사용할 배지 위치를 선택하십시오. 옵션: `Inline` / `Bottom Right` / `Bottom Left`

   - **[!UICONTROL Theme]**&#x200B;의 경우 Google reCAPTCHA 상자 스타일을 지정하는 데 사용할 테마를 선택하십시오. 옵션: `Light Theme (default)` / `Dark Theme`

   - **[!UICONTROL Language Code]**&#x200B;의 경우 Google reCAPTCHA 텍스트 및 메시지에 사용되는 [언어를 지정하는 두 문자 코드를 입력하십시오](https://developers.google.com/recaptcha/docs/language).

   ![reCAPTCHA v2 보이지 않음](../configuration-reference/security/assets/recaptcha-admin-v2-invisible.png){width="600" zoomable="yes"}

1. _[!DNL reCAPTCHA v3 Invisible]_&#x200B;을(를) 사용하려면&#x200B;**[!UICONTROL reCAPTCHA v3 Invisible]**&#x200B;섹션을 확장하고 다음을 수행하십시오.

   - **[!UICONTROL Google API Website Key]**&#x200B;의 경우 Google reCAPTCHA 계정을 등록할 때 이 reCAPTCHA 유형에 대해 만든 웹 사이트 키를 입력하십시오.

   - **[!UICONTROL Google API Secret Key]**&#x200B;의 경우 Google reCAPTCHA 계정과 연결된 비밀 키를 입력하십시오.

   - 사용자 상호 작용이 잠재적 위험으로 플래그가 지정된 시기를 식별하려면 **[!UICONTROL Minimum Score Threshold]**&#x200B;을(를) 입력하십시오. 여기서 1.0은 일반적인 사용자 상호 작용이고 0.0은 봇일 수 있습니다. 기본값: `0.5`

   - **[!UICONTROL Invisible Badge Position]**&#x200B;의 경우 각 페이지에서 사용할 위치를 선택하십시오. 옵션: `Inline` / `Bottom Right` / `Bottom Left`

   - **[!UICONTROL Theme]**&#x200B;의 경우 Google reCAPTCHA 상자 스타일을 지정하는 데 사용할 테마를 선택하십시오. 옵션: `Light Theme (default)` / `Dark Theme`

   - **[!UICONTROL Language Code]**&#x200B;의 경우 Google reCAPTCHA 텍스트 및 메시지에 사용되는 [언어를 지정하는 두 문자 코드를 입력하십시오](https://developers.google.com/recaptcha/docs/language).

   ![reCAPTCHA v3 보이지 않음](../configuration-reference/security/assets/recaptcha-admin-v3-invisible.png){width="600" zoomable="yes"}

1. **[!UICONTROL reCAPTCHA Validation Failure Messages]**&#x200B;을(를) 확장하고 유효성 검사가 실패하거나 완료할 수 없는 경우 관리자에 표시되는 메시지를 입력합니다.

   ![reCAPTCHA 오류 메시지](../configuration-reference/security/assets/recaptcha-admin-failure-messages.png){width="600" zoomable="yes"}

1. **[!UICONTROL Admin Panel]** 섹션을 확장하고 필요에 따라 다음을 구성합니다.

   - **[!UICONTROL Enable for Login]**&#x200B;을(를) 관리자 로그인 페이지에 사용할 reCAPTCHA 형식으로 설정합니다.

   - 암호 재설정 요청에 사용할 reCAPTCHA 형식으로 **[!UICONTROL Enable for Forgot Password]**&#x200B;을(를) 설정하십시오.

   ![reCAPTCHA 관리 옵션](../configuration-reference/security/assets/recaptcha-admin-panel.png){width="600" zoomable="yes"}

## 3단계: Storefront용 Google reCAPTCHA 구성

1. _[!UICONTROL Security]_&#x200B;아래의 왼쪽 패널에서&#x200B;**[!UICONTROL Google reCAPTCHA Storefront]**&#x200B;을(를) 선택합니다.

1. 상점 전면에서 사용할 각 reCAPTCHA 유형에 대한 섹션을 완료합니다.

   각 reCAPTCHA 유형의 옵션에 대한 자세한 내용은 _2단계: 관리자용 Google reCAPTCHA 구성_&#x200B;의 정보를 참조하십시오.

1. 유효성 검사가 실패하거나 완료할 수 없는 경우 **[!UICONTROL reCAPTCHA Validation Failure Messages]**&#x200B;을(를) 확장하고 상점 앞에 표시되는 메시지를 입력하십시오.

1. **[!UICONTROL Storefront]** 섹션을 확장합니다.

   >[!NOTE]
   >
   >구성할 각 필드에 대해 **[!UICONTROL Use system value]** 확인란의 선택을 취소합니다.

1. 각 storefront 위치 필드를 사용하도록 구성한 reCAPTCHA 유형으로 설정합니다.

   - [!UICONTROL Enable for Customer Login]
   - [!UICONTROL Enable for Forgot Password]
   - [!UICONTROL Enable for Create New Customer Account]
   - [!UICONTROL Enable for Edit Customer Account]
   - [!UICONTROL Enable for Create New Company Account] ![Adobe Commerce B2B](../assets/b2b.svg)(Adobe Commerce B2B에서만 사용 가능)
   - [!UICONTROL Enable for Contact Us]
   - [!UICONTROL Enable for Product Review]
   - [!UICONTROL Enable for Newsletter Subscription]
   - [!UICONTROL Enable for Gift Card] ![Adobe Commerce](../assets/adobe-logo.svg)(Adobe Commerce 전용)
   - [!UICONTROL Enable for Invitation Create Account]
   - [!UICONTROL Enable for Send To Friend]
   - [!UICONTROL Enable for Checkout/Placing Order]
   - [!UICONTROL Enable for Wishlist Sharing]
   - [!UICONTROL Enable for Coupon Codes]
   - [!UICONTROL Enable for PayPal PayflowPro payment form]

   ![Storefront 옵션 구성](../configuration-reference/security/assets/recaptcha-storefront.png){width="600" zoomable="yes"}

## 4단계: 구성 저장

1. 구성 설정이 완료되면 **[!UICONTROL Save Config]**&#x200B;을(를) 클릭합니다.

1. 작업 영역의 맨 위에 있는 메시지에서 **[!UICONTROL Cache Management]**&#x200B;을(를) 클릭하고 각각의 잘못된 캐시를 새로 고칩니다.
