---
title: 관리자 계정
description: 관리자 계정과 2단계 인증을 사용하여 관리자에 로그인하는 방법에 대해 알아봅니다.
exl-id: ad576533-5914-49d1-8e73-3f59c55543a5
feature: Admin Workspace, User Account
source-git-commit: fff3464c9da50927bbe9773a17b0f6858360d788
workflow-type: tm+mt
source-wordcount: '964'
ht-degree: 0%

---

# 관리자 계정

기본 관리자 계정은 설치 중에 처음 설정되었으며 초기 자리 표시자 정보 또는 샘플 데이터 정보를 포함할 수 있습니다. 이 계정의 지정된 소유자는 사용자 이름과 암호를 개인화하고 언제든지 이름, 성 및 이메일 주소를 업데이트할 수 있습니다. 이 계정, a _슈퍼 사용자_ 기본적으로 모든 권한을 사용하여에서 비즈니스에 필요한 관리자 계정을 생성합니다.

- 다음을 참조하십시오 [사용자 만들기](../systems/permissions-users-all.md#create-a-user) 사용자 추가 또는 편집에 대한 정보를 제공합니다.

- 다음을 참조하십시오 [권한](../systems/permissions.md) 및 [사용자 역할](../systems/permissions-user-roles.md) 관리자 및 사용자 역할에 대한 자세한 정보.

{{ims-admin-note}}

## 관리자 로그인

다음 [!DNL Commerce] _관리자_ 은 저장소, 주문 및 고객 데이터에 대한 무단 액세스를 방지하기 위해 여러 계층의 보안 조치를 통해 보호됩니다. 에 처음 로그인할 때 _관리자_, 사용자 이름과 암호를 입력하고 를 설정해야 합니다 [이중 인증](../systems/security-two-factor-authentication.md) (2FA).

저장소 구성에 따라 다음과 같은 항목이 있을 수 있습니다. [CAPTCHA](../systems/security-google-recaptcha.md) 일련의 키보드 문자 입력, 퍼즐 해결 또는 공통 테마가 있는 일련의 이미지 클릭 등 해결해야 할 과제. 이러한 테스트는 자동화된 봇이 아닌 사람으로 사용자를 식별하도록 설계되었습니다.

추가 보안을 위해 _관리자_ 각 사용자는 [권한](../systems/permissions.md) 액세스 및 제한 횟수 [로그인 시도 횟수](../configuration-reference/advanced/admin.md). 기본적으로 6회 시도하면 계정이 잠기고 사용자는 몇 분 정도 기다린 후 다시 시도해야 합니다. [잠긴 계정](../systems/permissions-users-all.md#locked-users) 에서 재설정할 수도 있습니다. _관리자_.

>[!NOTE]
>
>에 처음 로그인할 때 _관리자_&#x200B;을 선택하라는 메시지가 표시됩니다. _관리자 사용 데이터 수집 허용_. 다음을 참조하십시오 [사용 데이터 수집](admin.md#usage-data-collection) 추가 정보.

![관리자 로그인](./assets/admin-login.png){width="400"}

### 1단계: 이중 인증 설정

에 로그인하기 전에 _관리자_ 스토어의 2단계 인증 솔루션을 설정하고 사용할 준비가 되어 있어야 합니다. 각 솔루션에서 사용하는 인증 프로세스에 대한 자세한 내용은 [이중 인증 사용](../systems/security-two-factor-authentication-use.md). 기본적으로, [!DNL Commerce] 지원 [Google Authenticator][1].

다음 사용자에게 묻기 [!DNL Commerce] 스토어에 대해 지원되는 2FA 솔루션은 시스템 관리자입니다. 그런 다음 공급자의 지침에 따라 선호하는 2FA 솔루션의 설정을 완료합니다.

### 2단계: 관리자에 로그인

1. 다음을 입력합니다. _관리자_ 다음 기간 동안 지정된 URL [!DNL Commerce] 설치.

   기본값 _관리자_ URL의 형태는 다음과 같습니다. `https://www.yourdomain.com/your-custom-admin-domain`.

   >[!NOTE]
   >
   >이 설명서에서는 `admin` 대부분의 예에서 기본 URL로 고유하고 예측하기 어려운 을 선택하는 것이 좋습니다 [사용자 정의 URL](../stores-purchase/store-urls.md) 대상: _관리자_ 스토어에서 가져왔습니다.

   페이지에 책갈피를 추가하거나 바탕 화면에 바로 가기를 저장하여 쉽게 액세스할 수 있습니다.

1. 다음을 입력하십시오. _관리자_ **[!UICONTROL Username]** 및 **[!UICONTROL Password]**.

1. (선택 사항) 스토어에 대해 CAPTCHA가 활성화되어 있으면 화면의 지침에 따라 문제를 해결합니다.

   자세한 내용은 다음을 참조하십시오. [CAPTCHA](../systems/security-captcha.md) 및 [reCAPT차](../systems/security-google-recaptcha.md).

1. 클릭 **[!UICONTROL Sign in]**.

   에 처음 로그인한 경우 _관리자_ 계정에서 구성 지침에 대한 링크가 포함된 이메일을 받게 됩니다.

### 3단계: 2FA 구성 완료

다음 예는 를 쌍으로 연결하는 방법을 보여 줍니다. _관리자_ Google Authenticator를 사용하여 계정을 만듭니다.

1. QR 코드가 나타나면 다음 방법 중 하나를 사용하여 코드를 캡처하고 Google Authenticator를 와 연결합니다. _관리자_ 계정입니다.

   ![Google Authenticator 설정](./assets/admin-login-google-auth-setup.png){width="400"}

   - 스마트 폰을 사용하여 QR 코드 캡처

     스마트폰에서 Google Authenticator를 시작합니다. 탭 _더하기 기호_ (+) 기호를 클릭하여 앱의 오른쪽 상단에 배치합니다. 그런 다음 화면 하단에서 을 누릅니다. **[!UICONTROL Scan Barcode]** 그리고 QR코드를 찍으세요

   - 브라우저에서 QR 코드 캡처

     Google Authenticator가 브라우저에 확장으로 설치된 경우 **인증자** 아이콘을 클릭하여 페이지를 캡처합니다.

   - QR 코드 수동 입력

     QR 코드 아래에 있는 텍스트 문자열을 복사합니다. 스마트폰이나 브라우저를 사용하여 Google Authenticator를 실행하고 더하기 기호(+)를 클릭합니다. 그런 다음 을(를) 선택합니다 **[!UICONTROL Manual Entry]**. 아래 **[!UICONTROL Account]**&#x200B;와(과) 연결된 이메일 주소를 입력합니다. _관리자_ QR 코드 문자열을 계정에 붙여 넣습니다. **[!UICONTROL Key]** 필드.

1. 에 로그인하려면 _관리자_ 이중 인증을 사용할 경우 Google Authenticator에서 생성한 6자리 코드를 **[!UICONTROL Authenticator code]** 필드를 클릭한 다음 **[!UICONTROL Confirm]**.

   ![인증자 코드 입력](./assets/admin-login-2fa-google.png){width="400"}

## 암호 재설정

계정에 할당된 마지막 4개의 암호 재사용은 허용되지 않습니다.

1. 다음을 입력합니다. **[!UICONTROL Email Address]** 와(과) 연결된 _관리자_ 계정입니다.

   ![잊어버린 암호](./assets/admin-sign-in-forgot-password.png){width="400"}

1. 클릭 **[!UICONTROL Retrieve Password]**.

   계정이 이메일 주소와 연결된 경우 암호를 재설정하기 위해 이메일이 전송됩니다.

   >[!NOTE]
   >
   >An _관리자_ 암호는 7자 이상이어야 하며 문자와 숫자를 모두 포함해야 합니다. 다음을 참조하십시오 [구성 _관리자_ 보안](../systems/security-admin.md) 암호 옵션에 대한 정보를 보려면 를 참조하십시오.

## 관리자에서 로그아웃

1. 오른쪽 위 모서리에서 _계정_ (![계정](../assets/icon-admin-user.png)) 아이콘.

1. 클릭 **[!UICONTROL Sign Out]**.

   ![로그아웃](./assets/admin-sign-out.png){width="700" zoomable="yes"}

다음 _[!UICONTROL Sign In]_로그아웃되었다는 메시지가 페이지에 표시됩니다. 에서 로그아웃_&#x200B;관리자&#x200B;_컴퓨터를 방치할 때마다.

## 계정 정보 편집

1. 다음을 클릭합니다. _계정_ (![계정 아이콘](../assets/icon-admin-user.png)) 아이콘.

1. 클릭 **[!UICONTROL Account Setting]**.

   ![계정 정보](./assets/admin-account-information.png){width="700" zoomable="yes"}

1. 계정 정보에 필요한 사항을 변경합니다.

   로그인 자격 증명을 변경하는 경우 보안 위치에 저장해야 합니다.

1. 현재 계정 암호를 입력합니다.

1. 클릭 **[!UICONTROL Save Account]**.

## 여러 관리자 로그인 허용

관리자는 주문, 고객, 제품, 배송 및 결제 기능을 관리할 수 있는 액세스 권한을 제공합니다. 기본 구성은 보안 모범 사례로서 관리자 사용자 계정에 대한 여러 로그인을 허용하지 않도록 설정되어 있습니다. 그러나 이 설정을 변경하여 관리자가 비즈니스 워크플로를 수용하도록 여러 장치에서 로그인할 수 있도록 할 수 있습니다.

1. 다음에서 _관리자_ 사이드바, 이동 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. 왼쪽 탐색 패널에서 를 확장합니다. **[!UICONTROL Advanced]** 및 선택 **[!UICONTROL Admin]**.

1. 확장 ![확장 선택기](../assets/icon-display-expand.png) 다음 **[!UICONTROL Security]** 섹션.

1. 대상 **관리자 계정 공유**, 선택 `Yes`.

   ![관리자 계정 공유 허용](./assets/multiple-admin-login.png){width="700" zoomable="yes"}

1. 클릭 **[!UICONTROL Save Config]**.

## 관리자 사용자 로그인 이름을 대소문자를 구분하도록 설정

1. 다음에서 _관리자_ 사이드바, 이동 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. 왼쪽 탐색 패널에서 를 확장합니다. **[!UICONTROL Advanced]** 및 선택 **[!UICONTROL Admin]**.

1. 확장 ![확장 선택기](../assets/icon-display-expand.png) 다음 **[!UICONTROL Security]** 섹션.

1. 설정 **[!UICONTROL Login is Case Sensitive]** 필드 대상 `Yes`.

1. 클릭 **[!UICONTROL Save Config]**.

[1]: https://play.google.com/store/apps/details?id=com.google.android.apps.authenticator2&amp;hl=en_US
