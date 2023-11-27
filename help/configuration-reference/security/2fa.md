---
title: '[!UICONTROL Security] &gt; [!UICONTROL 2FA]'
description: 에서 구성 설정을 검토합니다. [!UICONTROL Security] &gt; [!UICONTROL 2FA] 상거래 관리자의 페이지입니다.
exl-id: d3f6e16b-6eba-47db-a9dd-cb3268d1a13f
feature: Configuration, Security
source-git-commit: 76bd1b1af9b55d69bd98209d70fb5518f190a3e1
workflow-type: tm+mt
source-wordcount: '280'
ht-degree: 1%

---

# [!UICONTROL Security] > [!UICONTROL 2FA]

>[!NOTE]
>
>IMS(Adobe Identity Management 서비스) 인증을 사용하도록 설정한 저장소에는 기본 Adobe Commerce 및 Magento Open Source 2단계 인증(2FA)이 사용되지 않도록 설정되어 있습니다. Adobe 자격 증명으로 Adobe Commerce 인스턴스에 로그인한 관리자는 많은 관리 작업에 대해 다시 인증할 필요가 없습니다. Adobe IMS는 관리자 가 현재 세션에 로그인할 때 인증을 처리합니다. 다음을 참조하십시오 [Adobe IMS와 Adobe Commerce 통합 개요](https://experienceleague.adobe.com/docs/commerce-admin/start/admin/ims/adobe-ims-integration-overview.html).

{{config}}

이러한 설정 변경에 대한 자세한 내용은 [이중 인증(2FA)](../../systems/security-two-factor-authentication.md) 다음에서 _관리 시스템 안내서_.

## [!UICONTROL General]

![일반](./assets/2fa-general.png)<!-- zoom -->

| 필드 | [범위](../../getting-started/websites-stores-views.md#scope-settings) | 설명 |
|--- |--- |--- |
| [!UICONTROL Providers to use] | 글로벌 | 필요한 2단계 인증 방법을 나타냅니다. 공급자를 두 개 이상 선택하는 경우 각 사용자는 다음에 로그인할 때 각 2FA 메서드를 구성해야 합니다. |
| [!UICONTROL Configuration Email URL for Web API] | 글로벌 | 사용자 지정 구현의 경우 (으)로 전송되는 대체 이메일 구성 링크의 URL _관리자_ 처음 로그인할 때 사용자. 이메일 템플릿에서 자리 표시자를 사용합니다. `:tfat` 토큰을 삽입할 위치를 나타냅니다. |

{:style=&quot;table-layout:auto&quot;}

## [!UICONTROL Google]

![Google](./assets/2fa-google.png)<!-- zoom -->

| 필드 | [범위](../../getting-started/websites-stores-views.md#scope-settings) | 설명 |
|--- |--- |--- |
| [!UICONTROL OTP Window] | 글로벌 | Google Authenticator에서 생성한 각 일회용 암호(OTP)의 수명(초)입니다. 기본값: `30` |

{:style=&quot;table-layout:auto&quot;}

## [!UICONTROL Duo Security]

![듀오 보안](./assets/2fa-duo-security.png)<!-- zoom -->

| 필드 | [범위](../../getting-started/websites-stores-views.md#scope-settings) | 설명 |
|--- |--- |--- |
| [!UICONTROL Integration Key] | 글로벌 | 의 통합 키 [!DNL Duo Security] 계정입니다. |
| [!UICONTROL Secret Key] | 글로벌 | 의 비밀 키 [!DNL Duo Security] 계정입니다. |
| [!UICONTROL API Hostname] | 글로벌 | 의 API 호스트 이름 [!DNL Duo Security] 계정입니다. |

{:style=&quot;table-layout:auto&quot;}

## [!UICONTROL Authy]

![작성](./assets/2fa-authy.png)<!-- zoom -->

| 필드 | [범위](../../getting-started/websites-stores-views.md#scope-settings) | 설명 |
|--- |--- |--- |
| [!UICONTROL API Key] | 글로벌 | 의 API 키 [!DNL Authy] 계정입니다. |
| [!UICONTROL OneTouch Message] | 글로벌 | 에 표시되는 메시지 [!DNL Authy] 로그인 시 인증자. 기본값: `Login request to your Magento Admin` |

{:style=&quot;table-layout:auto&quot;}

## [!UICONTROL U2F Key]

![U2F 키](./assets/2fa-u2f-key.png)<!-- zoom -->

| 필드 | [범위](../../getting-started/websites-stores-views.md#scope-settings) | 설명 |
|--- |--- |--- |
| [!UICONTROL WebApi Challenge Domain] | 글로벌 | 발행 및 처리에 사용되는 도메인 [!DNL WebAuthn] 사용자 지정 WebAPI 구현의 어려움. |

{:style=&quot;table-layout:auto&quot;}
