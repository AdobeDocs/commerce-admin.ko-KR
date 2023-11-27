---
title: 사용자 계정에 대한 2단계 인증 설정
description: 초기 관리자 로그인 동안 이중 인증을 설정하고 지원되는 장치 앱을 사용하여 ID를 인증하는 방법을 알아봅니다.
exl-id: 1ea7f09e-4753-40fa-b9d4-376ba5d8f58f
role: Admin, User
feature: Configuration, Security, User Account
source-git-commit: 64ccc2d5016e915a554c2253773bb50f4d33d6f4
workflow-type: tm+mt
source-wordcount: '778'
ht-degree: 0%

---

# 사용자 계정에 대한 2단계 인증 설정

이 지침은 Adobe Commerce 또는 Magento Open Source에 처음 로그인하는 동안 이중 인증을 설정하는 방법과 다음 앱 및 장치를 사용하여 신원을 인증하는 방법을 보여 줍니다.

전체 지침은 [관리자 로그인](../getting-started/admin-signin.md).

>[!NOTE]
>
>활성화된 스토어 [!DNL Adobe Identity Management Services] (IMS) 인증에는 기본 Adobe Commerce 및 Magento Open Source 2FA가 비활성화되어 있습니다. Adobe 자격 증명으로 Commerce 인스턴스에 로그인한 관리자는 많은 관리 작업에 대해 다시 인증할 필요가 없습니다. Adobe IMS는 관리자 가 현재 세션에 로그인할 때 인증을 처리합니다. 다음을 참조하십시오 [[!DNL Adobe Identity Management Service] (IMS) 통합 개요](../getting-started/adobe-ims-integration-overview.md).

## [!DNL Google Authenticator]

### 1단계: 설정 [!DNL Google Authenticator]

1. 계정 자격 증명을 입력하고 _관리자_. QR 코드와 함께 새 인증자 화면이 나타납니다.

1. 를 엽니다. **[!UICONTROL Google Authenticator]** 모바일 장치의 앱입니다.

1. 더하기 기호( **+** ) 항목을 추가하고 스마트 폰의 카메라로 스캔할 QR 코드와 함께 빨간색 상자를 정렬합니다.

1. 휴대폰에서 QR 코드를 인식하고 항목을 추가하면 _관리자_ **[!UICONTROL Authenticator code]** 필드.

1. 완료되면 다음을 클릭하십시오. **[!UICONTROL Confirm]**.

   ![Google Authenticator QR 코드](./assets/storefront-2fa-google-qrcode.png){width="300"}

### 2단계: 다음으로 로그인 [!DNL Google Authenticator]

1. 계정 자격 증명을 입력하고 Commerce에 로그인합니다 _관리자_.

   ![Google Authenticator - 로그인](./assets/storefront-2fa-google-code.png){width="300"}

1. 열기 [!DNL Google Authenticator] 모바일 디바이스에서.

1. 메시지가 표시되면 6자리 인증 코드를 입력합니다.

1. 나중에 로그인할 수 있도록 인증을 저장하려면 **[!UICONTROL Trust this device, do not ask again]** 확인란.

1. 완료되면 다음을 클릭하십시오. **[!UICONTROL Confirm]**.

## [!DNL Duo Security]

[!DNL Duo] 은 무료 평가판을 제공하며 계정과 연결된 사용자 수에 따라 요금이 부과됩니다. 팔로우 [계정 설정 및 앱 다운로드 지침](https://duo.com/product/multi-factor-authentication-mfa/duo-mobile-app).

### 1단계: 설정 [!DNL Duo Security]

1. 계정 자격 증명을 입력하고 _관리자_.

1. 다음의 경우 [!DNL Duo] 설정 페이지가 나타나면 **[!UICONTROL Start setup]** 다음을 수행합니다.

   ![Storefront - Duo 설정 예](./assets/storefront-2fa-duo-user1.png){width="300"}

1. 장치를 선택합니다.

1. 메시지가 표시되면 전화 번호를 입력하고 **[!UICONTROL Continue]**.

   이 예제에서는 모바일 장치를 사용하고 있으므로 전화 번호를 요청합니다.

1. 설치 여부를 묻는 메시지가 나타나면 [!DNL Duo Mobile] 휴대폰 유형의 경우 **[!UICONTROL I have Duo Mobile]**.

1. 열기 [!DNL Duo Mobile] 및 QR 코드를 스캔하여 인증자를 Adobe Commerce과 동기화합니다. 활성화가 완료되면 확인 표시가 나타납니다.

1. 장치에 대한 설정을 구성하려면 로그인할 때 수행할 작업을 선택합니다.

   - `Ask me to choose an authenticator method` — 사용자가 로그인하고 로그인할 때 선택할 수 있도록 해줍니다. _관리자_.
   - `Automatically send this device a Duo Push` — 장치에 액세스를 허용하거나 거부하라는 메시지를 보냅니다.
   - `Automatically call this device` — 를 호출하고 액세스하기 위해 입력할 암호를 제공합니다.

   ![듀오 확인 작업](./assets/storefront-2fa-duo-user7.png){width="300"}

### 2단계: 다음으로 로그인 [!DNL Duo Security]

다음 예는 다음 옵션을 보여줍니다. `Ask me to choose an authenticator method`:

1. 메시지가 표시되면 _관리자_ 로그인할 자격 증명입니다.

   ![Duo - 로그인](./assets/storefront-2fa-duo-auth.png){width="300"}

1. 인증에 사용할 방법을 선택합니다.

   - `Send Me a Push` — 푸시 알림을 받으려면 클릭합니다. [!DNL Duo Mobile]. 수락하여 인증합니다.
   - `Call Me` — 이 옵션을 클릭하고 코드가 있는 호출을 받은 다음 암호를 입력합니다.
   - `Enter a Passcode` — 암호를 받고 입력하려면 이 옵션을 클릭하십시오.

1. 푸시 또는 코드를 완료하여에 완전히 로그인합니다. _관리자_.

## [!DNL Authy]

[!DNL Authy] 은 사용자에게 무료로 앱과 서비스를 제공합니다. 해당 지침에 따라 디바이스 또는 브라우저용 앱을 다운로드하여 설정합니다. 자세한 내용은 [[!DNL Authy] 설명서](https://authy.com/features/setup/).

### 1단계: 인증 설정

1. 계정 자격 증명을 입력하고 _관리자_.

   ![[!DNL Authy] 등록](./assets/storefront-2fa-authy-auth.png){width="300"}

1. Authy에 직접 등록하라는 메시지가 표시되면 다음을 수행합니다.

   - 국가를 선택합니다.

   - 전화 번호를 입력합니다.

   - 다음 항목 선택 **[!UICONTROL Verification method]**: `SMS` 또는 `Call Me`

   클릭 **[!UICONTROL Continue]**. SMS 문자 또는 전화를 통해 휴대폰으로 메시지를 보냅니다.

1. 받은 인증 코드를 입력하고 **[!UICONTROL Verify]**.

1. 완료되면 다음을 클릭하십시오. **[!UICONTROL Confirm]**.

   ![[!DNL Authy] 인증 코드](./assets/storefront-2fa-authy-verify.png){width="300"}

### 2단계: 다음으로 로그인 [!DNL Authy]

1. 계정 자격 증명을 입력하고 _관리자_.

   ![[!DNL Authy] - 로그인](./assets/storefront-2fa-authy-access.png){width="300"}

1. 다음 방법 중 하나를 선택하여 인증합니다.

   - `Use one touch` — 경고 메시지를 보냅니다. [!DNL Authy] 앱. 앱에서 액세스 권한을 수락합니다.
   - `Use authy token` — 다음에서 코드를 입력하라는 메시지를 표시합니다. [!DNL Authy] 앱.

1. 로그인에 문제가 있는 경우 코드를 받는 데 사용할 방법을 선택하십시오. 그런 다음 받은 코드를 입력하여 _관리자_.

   앱에는 다음과 같은 추가 응급 방법이 포함되어 있습니다.

   - `Send me a code via SMS` — 구성된 모바일 장치로 텍스트 SMS 메시지가 전송됩니다.
   - `Send me a code via phone call` — 사용자가 코드가 있는 전화를 받습니다.

   계정이 확인되고 열립니다.

## U2F ([!DNL Yubikey] 및 기타 장치)

솔루션 공급자의 지침에 따라 U2F 장치를 구성합니다. 자세한 내용은 다음과 같은 공급업체 설명서를 참조하십시오. [[!DNL YubiKey]](https://support.yubico.com/hc/en-us/articles/360013790339-Getting-Started-with-Your-YubiKey) 작성자: [!UICONTROL Yubico].

1. 계정 자격 증명을 입력하고 _관리자_.

   ![U2F 키 액세스](./assets/storefront-2fa-u2f.png){width="300"}

1. 키에 있는 버튼을 누르세요

   인증이 즉시 트리거되고 _관리자_.

1. 삽입 **[!UICONTROL U2F key]** 를 컴퓨터의 USB 포트에 연결합니다.
