---
title: 이중 인증(2FA)
description: 시스템 및 데이터의 보안을 보장하기 위한 이중 인증 지원에 대해 알아봅니다.
exl-id: d9eb3dd6-4a7b-411a-ac08-0441803cd59a
role: Admin
feature: Configuration, Security, User Account
source-git-commit: c391a3eef8be0dd45cc8a499b63bcb0fc32640aa
workflow-type: tm+mt
source-wordcount: '786'
ht-degree: 0%

---

# 이중 인증(2FA)

더 Commerce _관리자_ Adobe Commerce 또는 Magento Open Source 설치에서는 스토어, 주문 및 고객 데이터에 액세스할 수 있습니다. 데이터에 대한 무단 액세스를 방지하기 위해 을(를) 로그인하려는 모든 사용자 _관리자_ id를 확인하려면 인증 프로세스를 완료해야 합니다.

>[!NOTE]
>
>이 2단계 인증(2FA) 구현은 _관리자_ 고객 계정에만 및 을 사용할 수 없습니다. Commerce 계정을 보호하는 2단계 인증에는 별도의 설정이 있습니다. 자세한 내용을 보려면 다음 위치로 이동하십시오. [Commerce 계정 보안](../getting-started/commerce-account-secure.md).

2단계 인증이 널리 사용되고 있으며 동일한 앱에서 서로 다른 웹 사이트에 대한 액세스 코드를 생성하는 것이 일반적입니다. 이 추가 인증은 사용자만 사용자 계정에 로그인할 수 있도록 합니다. 암호를 분실하거나 봇이 추측하는 경우 2단계 인증을 통해 보호 계층이 추가됩니다. 예를 들어 Google Authenticator를 사용하여 스토어 관리자, Commerce 계정 및 Google 계정에 대한 코드를 생성할 수 있습니다.

![보안 구성 iphone - 2FA](./assets/google-authenticator-iphone.png){width="300"}

Adobe Commerce은 여러 공급자의 2FA 메서드를 지원합니다. 일부는 사용자가 본인 확인을 위해 로그인 시 입력하는 일회성 비밀번호(OTP)를 생성하는 앱 설치가 필요하다. 범용 제2 인자(U2F) 디바이스는 키 포브와 유사하고 신원을 확인하기 위해 고유 키를 생성한다. 다른 장치는 USB 포트에 삽입되면 ID를 확인합니다. 저장소 관리자는 사용자 ID를 확인하기 위해 사용 가능한 2FA 메서드 중 하나 이상을 요구할 수 있습니다. 2FA 구성은 Adobe Commerce 설치와 연결된 모든 웹 사이트 및 스토어에 적용됩니다.

사용자가 다음에 처음 로그인할 때 _관리자_, 각 을 설정해야 합니다. [2FA](../configuration-reference/security/2fa.md) 필요한 메서드를 사용하고 연결된 앱 또는 장치를 사용하여 id를 확인합니다. 이 초기 설정 후 사용자는 로그인할 때마다 구성된 방법 중 하나를 사용하여 인증해야 합니다. 각 사용자의 2FA 정보가 _관리자_ 계정 및 다음 작업을 수행할 수 있습니다. [재설정](security-two-factor-authentication-manage.md) 필요한 경우. 로그인 프로세스에 대해 자세히 알아보려면 [_관리자_ 로그인](../getting-started/admin-signin.md).

>[!NOTE]
>
>IMS(Adobe Identity Management 서비스) 인증을 사용하도록 설정한 스토어에는 기본 Adobe Commerce 및 Magento Open Source 2FA가 비활성화되어 있습니다. Adobe 자격 증명으로 Commerce 인스턴스에 로그인한 관리자는 많은 관리 작업에 대해 다시 인증할 필요가 없습니다. Adobe IMS는 관리자 가 현재 세션에 로그인할 때 인증을 처리합니다. 다음을 참조하십시오 [Adobe Identity Management 서비스(IMS) 통합 개요](https://experienceleague.adobe.com/docs/commerce-admin/start/admin/ims/adobe-ims-integration-overview.html).

이거 보면 돼 [비디오 데모](https://video.tv.adobe.com/v/339104?quality=12&learn=on) 관리자의 이중 인증에 대한 개요입니다.

## 필요한 2FA 공급자 구성

1. 다음에서 _관리자_ 사이드바, 이동 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. 왼쪽 패널에서 를 확장합니다. **[!UICONTROL Security]** 및 선택 **[!UICONTROL 2FA]**.

1. 다음에서 _[!UICONTROL General]_섹션에서 사용할 공급자를 선택합니다.

   | 공급자 | 함수 |
   |--- |--- |
   | [!UICONTROL Google Authenticator] | 사용자 인증을 위해 애플리케이션에서 일회용 암호를 생성합니다. |
   | [!UICONTROL Duo Security] | SMS 및 푸시 알림을 제공합니다. |
   | [!UICONTROL Authy] | 시간에 따라 달라지는 6자리 코드를 생성하고 SMS 또는 음성 호출 2FA 보호 또는 토큰을 전달합니다. |
   | [!UICONTROL U2F Devices (Yubikey and others)] | 다음과 같은 실제 장치를 사용하여 인증합니다. [[!DNL YubiKey]](https://www.yubico.com/). |

   여러 메서드를 선택하려면 Ctrl 키(PC) 또는 Command 키(Mac)를 누른 채 각 항목을 클릭합니다.

1. 필요한 각 2FA 메서드에 대한 설정을 완료합니다.

   ![보안 구성 - 2FA](../configuration-reference/security/assets/2fa-general.png){width="600" zoomable="yes"}

1. 완료되면 다음을 클릭하십시오. **[!UICONTROL Save Config]**.

   사용자가 처음으로 _관리자_&#x200B;필요한 각 2FA 메서드를 설정해야 합니다. 이 초기 설정 후에는 로그인할 때마다 구성된 방법 중 하나를 사용하여 인증해야 합니다.

## 2FA 공급자 설정

필요한 각 2FA 메서드에 대한 설정을 완료합니다.

### Google

로그인 중에 일회용 암호(OTP)를 사용할 수 있는 기간을 변경하려면 **[!UICONTROL Use system value]** 확인란. 그런 다음 원하는 시간(초)을 입력합니다 **[!UICONTROL OTP Window]** 유효해야 합니다.

>[!NOTE]
>
>Adobe Commerce 2.4.7 이상에서는 OTP 창 구성 설정이 관리자의 OTP(일회성 암호)가 만료된 후 시스템이 수락한 시간(초)을 제어합니다. 이 값은 30초 미만이어야 합니다. 시스템 기본 설정은 입니다. `1`.<br><br> 버전 2.4.6에서 OTP 창 설정은 유효한 과거 및 미래의 OTP 코드 수를 결정합니다. 값 `1` 는 현재 OTP 코드와 과거의 한 코드 및 미래의 한 코드가 주어진 시점에 유효한 상태를 유지함을 나타냅니다.

### [!DNL Duo Security]

Duo Security 계정에서 다음 자격 증명을 입력합니다.

- 통합 키
- 비밀 키
- API 호스트 이름

![보안 구성 - 듀오](../configuration-reference/security/assets/2fa-duo-security.png){width="600" zoomable="yes"}

### [!DNL Authy]

1. 에서 API 키 입력 [!DNL Authy] 계정입니다.

1. 인증 중에 나타나는 기본 메시지를 변경하려면 **[!UICONTROL Use system value]** 확인란. 그런 다음 를 입력합니다. **[!UICONTROL OneTouch Message]** 표시하려는 경우입니다.

   ![보안 구성 - 인증](../configuration-reference/security/assets/2fa-authy.png){width="600" zoomable="yes"}

### U2F 장치([!DNL Yubikey] 외)

저장소 도메인은 인증 프로세스 중에 기본적으로 사용됩니다. 사용자 정의 도메인을 사용하여 인증을 받으려면 **[!UICONTROL Use system value]** 확인란. 그런 다음 를 입력합니다. **[!UICONTROL WebAPi Challenge Domain]**.

![보안 구성 - U2F 장치](../configuration-reference/security/assets/2fa-u2f-key.png){width="600" zoomable="yes"}
