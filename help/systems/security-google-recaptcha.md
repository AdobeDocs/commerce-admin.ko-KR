---
title: Google recaptcha
description: 등록된 고객이 시작한 관리자 액세스 및 다양한 상점 활동을 위해 Google reCAPTCHA를 구성하는 방법에 대해 알아봅니다.
exl-id: c3b53702-0882-4ac4-9cf5-39fefc90005e
role: Admin
feature: Configuration, Security
source-git-commit: 64ccc2d5016e915a554c2253773bb50f4d33d6f4
workflow-type: tm+mt
source-wordcount: '1063'
ht-degree: 0%

---

# Google recaptcha

[Google recaptcha](https://developers.google.com/recaptcha) 는 컴퓨터(또는 &quot;보트&quot;)가 아닌 사람이 웹 사이트와 상호 작용하고 있는지 확인합니다. 표준 Adobe Commerce 및 Magento Open Source과 달리 [CAPTCHA](security-captcha.md), Google reCAPTCHA는 다양한 디스플레이 옵션 및 방법을 선택하여 향상된 보안을 제공합니다. 추가 웹 사이트 트래픽 정보는 Google reCAPTCHA 계정의 대시보드에서 사용할 수 있습니다.

Google reCAPTCHA는 관리자 및 상점 첫 페이지용으로 별도로 구성됩니다.

- 관리자의 경우, Google reCAPTCHA는 [로그인](../getting-started/admin-signin.md) 사용자가 암호 재설정을 요청할 때 및 페이지입니다. 표준 Commerce [CAPTCHA](security-captcha.md) 또한 Google reCAPTCHA를 문제 없이 동시에 사용할 수 있습니다.

- 상점 앞의 경우 Google reCAPTCHA를 사용하여 [고객 계정](../customers/customer-sign-in.md)에서 메시지를 보냅니다. [연락처](../getting-started/store-details.md#contact-us-form) 페이지 및 기타 여러 상점 내 위치.

  ![Google reCAPTCHA - 고객 로그인](./assets/customer-account-login-recaptcha.png){width="700" zoomable="yes"}

Google reCAPTCHA는 다음과 같은 여러 가지 방법으로 구현할 수 있습니다.

- _reCAPTCHA v3 보이지 않음_ — 알고리즘을 사용하여 사용자 상호 작용을 평가하고 점수를 기반으로 사용자가 사람일 가능성을 결정합니다.

- _reCAPTCHA v2 보이지 않음_ — 사용자 상호 작용 없이 배경 확인을 수행합니다. 사용자와 고객은 자동으로 확인되지만 문제를 완료하기 위해 특정 이미지를 선택해야 할 수도 있습니다.

- _reCAPTCHA v2(&quot;I am not a robot&quot;)_ — 를 사용하여 요청을 확인합니다. _&quot;난 로봇이 아니야&quot;_ 확인란.

>[!IMPORTANT]
>
>Google reCAPTCHA를 구성하기 전에 `PHP.ini` 파일에는 다음 설정이 포함되어 있습니다. `allow_url_fopen = 1`. 이 경우 개발자 지원이 필요할 수 있습니다. 다음을 참조하십시오 [필수 PHP 설정](https://experienceleague.adobe.com/docs/commerce-operations/installation-guide/prerequisites/php-settings.html)설치 안내서의 {:target=&quot;_blank&quot;}

## 1단계: Google reCAPTCHA 키 생성

Google reCAPTCHA를 사용하려면 API 키 쌍이 필요합니다. 이 키들은 reCAPTCHA 사이트를 통해 무료로 받아볼 수 있습니다. 키를 생성하기 전에 사용할 reCAPTCHA 유형을 알고 있어야 합니다.

1. Google reCAPTCHA 페이지를 열고 계정에 로그인합니다.

1. 대상 **[!UICONTROL Label]**&#x200B;을 클릭하고 내부 참조용 키를 식별할 이름을 입력합니다.

   Adobe Commerce 또는 Magento Open Source 설치에 사용되는 각 reCAPTCHA 유형에 하나의 키 세트가 필요합니다. For example: `Commerce Invisible`

1. 대상 **[!UICONTROL reCAPTCHA type]**&#x200B;를 클릭하고 사용할 메서드를 선택합니다.

   - _reCAPTCHA v3 보이지 않음_
   - _reCAPTCHA v2 보이지 않음_
   - _reCAPTCHA v2(&quot;I am not a robot&quot;)_

1. 대상 **[!UICONTROL Domain]**, 스토어의 도메인을 입력합니다. 예: mystore.com

   다른 도메인을 가진 저장소가 여러 개 있는 경우 각 도메인을 별도의 줄에 입력합니다.

   - 스토어 도메인 및 하위 도메인을 추가합니다.
   - 다음을 추가할 수 있습니다. `localhost`, 테스트에 필요한 다른 로컬 VM 도메인 및 스테이징 도메인.

1. 확인란을 선택하여 **[!UICONTROL Accept the reCAPTCHA Terms of Service]**.

1. (선택 사항) **[!UICONTROL Send alerts to owners]** Google에서 문제 또는 의심되는 트래픽을 감지하면 알림을 보내는 확인란입니다.

1. 클릭 **[!UICONTROL Submit]** 등록을 완료하고 키를 받습니다.

   >[!IMPORTANT]
   >
   >모든 키를 모든 유형의 reCAPTCHA에 적용할 수 있는 것은 아니며, 키를 잘못 적용하면 예기치 않은 동작이 발생할 수 있습니다. 예를 들어 reCAPTCHA v2 &quot;I&#39;m not a robot&quot;에 대해 생성된 Google reCAPTCHA 키는 _reCAPTCHA v2 보이지 않음_ 및 은 reCAPTCHA가 활성화된 기능을 차단할 수 있습니다.

## 2단계: 관리자용 Google reCAPTCHA 구성

1. 관리자 계정에 로그인합니다.

1. 관리 사이드바에서 다음 위치로 이동하십시오. **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. 오른쪽 상단에서 를 설정합니다. **[!UICONTROL Store View]** 끝 `Default Config`.

1. 왼쪽 패널에서 를 확장합니다. **[!UICONTROL Security]** 및 클릭 **[!UICONTROL Google reCAPTCHA Admin Panel]**.

   >[!NOTE]
   >
   >지우기 **[!UICONTROL Use system value]** 구성할 각 필드에 대한 확인란입니다.

1. 사용 _[!DNL reCAPTCHA v2 ("I am not a robot")]_를 확장합니다.**[!UICONTROL reCAPTCHA v2 ("I am not a robot")]**섹션을 참조하고 다음을 수행합니다.

   - 대상 **[!UICONTROL Google API Website Key]**, Google reCAPTCHA 계정을 등록할 때 이 reCAPTCHA 유형에 대해 만든 웹 사이트 키를 입력합니다.

   - 대상 **[!UICONTROL Google API Secret Key]**, Google reCAPTCHA 계정과 연결된 비밀 키를 입력합니다.

   - 대상 **[!UICONTROL Size]**&#x200B;로 이동하여 표시할 Google reCAPTCHA 상자의 크기를 선택합니다. 옵션: `Normal (default)` / `Compact`

   - 대상 **[!UICONTROL Theme]**&#x200B;를 클릭하고 Google reCAPTCHA 상자의 스타일을 지정하는 데 사용할 테마를 선택합니다. 옵션: `Light Theme (default)` / `Dark Theme`

   - 대상 **[!UICONTROL Language Code]**&#x200B;를 클릭하고 두 문자 코드를 입력하여 [Google reCAPTCHA 텍스트 및 메시징에 사용되는 언어](https://developers.google.com/recaptcha/docs/language).

   ![reCAPTCHA v2 - &quot;I am not a robot&quot;](../configuration-reference/security/assets/recaptcha-admin-v2-not-robot.png){width="600" zoomable="yes"}

1. 사용 _[!DNL reCAPTCHA v2 Invisible]_를 확장합니다.**[!UICONTROL reCAPTCHA v2 Invisible]**섹션을 참조하고 다음을 수행합니다.

   - 대상 **[!UICONTROL Google API Website Key]**, Google reCAPTCHA 계정을 등록할 때 이 reCAPTCHA 유형에 대해 만든 웹 사이트 키를 입력합니다.

   - 대상 **[!UICONTROL Google API Secret Key]**, Google reCAPTCHA 계정과 연결된 비밀 키를 입력합니다.

   - 대상 **[!UICONTROL Invisible Badge Position]**, 각 페이지에서 사용할 배지 위치를 선택합니다. 옵션: `Inline` / `Bottom Right` / `Bottom Left`

   - 대상 **[!UICONTROL Theme]**, Google reCAPTCHA 상자 스타일을 지정하는 데 사용할 테마를 선택합니다. 옵션: `Light Theme (default)` / `Dark Theme`

   - 대상 **[!UICONTROL Language Code]**&#x200B;를 지정하는 두 문자 코드를 입력합니다. [Google reCAPTCHA 텍스트 및 메시징에 사용되는 언어](https://developers.google.com/recaptcha/docs/language).

   ![reCAPTCHA v2 보이지 않음](../configuration-reference/security/assets/recaptcha-admin-v2-invisible.png){width="600" zoomable="yes"}

1. 사용 _[!DNL reCAPTCHA v3 Invisible]_를 확장합니다.**[!UICONTROL reCAPTCHA v3 Invisible]**섹션을 참조하고 다음을 수행합니다.

   - 대상 **[!UICONTROL Google API Website Key]**, Google reCAPTCHA 계정을 등록할 때 이 reCAPTCHA 유형에 대해 만든 웹 사이트 키를 입력합니다.

   - 대상 **[!UICONTROL Google API Secret Key]**, Google reCAPTCHA 계정과 연결된 비밀 키를 입력합니다.

   - 다음을 입력합니다. **[!UICONTROL Minimum Score Threshold]** 사용자 상호 작용이 잠재적 위험으로 플래그가 지정된 시기를 식별합니다. 여기서 1.0은 일반적인 사용자 상호 작용이고 0.0은 봇일 수 있습니다. 기본값: `0.5`

   - 대상 **[!UICONTROL Invisible Badge Position]**&#x200B;각 페이지에서 사용할 위치를 선택합니다. 옵션: `Inline` / `Bottom Right` / `Bottom Left`

   - 대상 **[!UICONTROL Theme]**, Google reCAPTCHA 상자 스타일을 지정하는 데 사용할 테마를 선택합니다. 옵션: `Light Theme (default)` / `Dark Theme`

   - 대상 **[!UICONTROL Language Code]**&#x200B;를 지정하는 두 문자 코드를 입력합니다. [Google reCAPTCHA 텍스트 및 메시징에 사용되는 언어](https://developers.google.com/recaptcha/docs/language).

   ![reCAPTCHA v3 보이지 않음](../configuration-reference/security/assets/recaptcha-admin-v3-invisible.png){width="600" zoomable="yes"}

1. 확장 **[!UICONTROL reCAPTCHA Validation Failure Messages]** 유효성 검사가 실패하거나 완료할 수 없는 경우 관리자에 표시되는 메시지를 입력합니다.

   ![reCAPTCHA 실패 메시지](../configuration-reference/security/assets/recaptcha-admin-failure-messages.png){width="600" zoomable="yes"}

1. 확장 **[!UICONTROL Admin Panel]** 섹션을 만들고 필요에 따라 다음을 구성합니다.

   - 설정 **[!UICONTROL Enable for Login]** 관리자 로그인 페이지에 사용할 reCAPTCHA 형식용입니다.

   - 설정 **[!UICONTROL Enable for Forgot Password]** 암호 재설정 요청에 사용할 reCAPTCHA 유형.

   ![reCAPTCHA 관리 옵션](../configuration-reference/security/assets/recaptcha-admin-panel.png){width="600" zoomable="yes"}

## 3단계: Storefront용 Google reCAPTCHA 구성

1. 아래의 왼쪽 패널에서 _[!UICONTROL Security]_, 선택&#x200B;**[!UICONTROL Google reCAPTCHA Storefront]**.

1. 상점 전면에서 사용할 각 reCAPTCHA 유형에 대한 섹션을 완료합니다.

   다음 정보를 참조하십시오. _2단계: 관리자용 Google reCAPTCHA 구성_ 각 reCAPTCHA 유형의 옵션에 대한 자세한 내용을 보려면 을 참조하십시오.

1. 확장 **[!UICONTROL reCAPTCHA Validation Failure Messages]** 유효성 검사가 실패하거나 완료할 수 없는 경우 상점 앞에 표시되는 메시지를 입력합니다.

1. 확장 **[!UICONTROL Storefront]** 섹션.

   >[!NOTE]
   >
   >지우기 **[!UICONTROL Use system value]** 구성할 각 필드에 대한 확인란입니다.

1. 각 storefront 위치 필드를 사용하도록 구성한 reCAPTCHA 유형으로 설정합니다.

   - [!UICONTROL Enable for Customer Login]
   - [!UICONTROL Enable for Forgot Password]
   - [!UICONTROL Enable for Create New Customer Account]
   - [!UICONTROL Enable for Edit Customer Account]
   - [!UICONTROL Enable for Create New Company Account] ![Adobe Commerce용 B2B](../assets/b2b.svg) (Adobe Commerce용 B2B에서만 사용 가능)
   - [!UICONTROL Enable for Contact Us]
   - [!UICONTROL Enable for Product Review]
   - [!UICONTROL Enable for Newsletter Subscription]
   - [!UICONTROL Enable for Gift Card] ![Adobe Commerce](../assets/adobe-logo.svg) (Adobe Commerce 전용)
   - [!UICONTROL Enable for Invitation Create Account]
   - [!UICONTROL Enable for Send To Friend]
   - [!UICONTROL Enable for Checkout/Placing Order]
   - [!UICONTROL Enable for Wishlist Sharing]
   - [!UICONTROL Enable for Coupon Codes]
   - [!UICONTROL Enable for PayPal PayflowPro payment form]

   ![Storefront 옵션 구성](../configuration-reference/security/assets/recaptcha-storefront.png){width="600" zoomable="yes"}

## 4단계: 구성 저장

1. 구성 설정이 완료되면 다음을 클릭하십시오. **[!UICONTROL Save Config]**.

1. 작업 영역 상단에 있는 메시지에서 **[!UICONTROL Cache Management]** 각 잘못된 캐시를 새로 고칩니다.
