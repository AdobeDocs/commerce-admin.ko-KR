---
title: '[!UICONTROL Security] &gt; [!UICONTROL Google reCAPTCHA Admin Panel]'
description: 에서 구성 설정을 검토합니다. [!UICONTROL Security] &gt; [!UICONTROL Google reCAPTCHA Admin Panel] 상거래 관리자의 페이지입니다.
exl-id: e4e6771a-487a-43ee-8b98-6acee4599aaf
feature: Configuration, Security
source-git-commit: 76bd1b1af9b55d69bd98209d70fb5518f190a3e1
workflow-type: tm+mt
source-wordcount: '582'
ht-degree: 0%

---

# [!UICONTROL Security] > [!UICONTROL Google reCAPTCHA Admin Panel]

>[!IMPORTANT]
>
>Google reCAPTCHA를 구성하려면 먼저 다음을 확인해야 합니다. `PHP.ini` 파일에는 다음 설정이 포함되어 있습니다. `allow_url_fopen = 1`. 이 경우 개발자 지원이 필요할 수 있습니다. 다음을 참조하십시오 [필수 PHP 설정](https://experienceleague.adobe.com/docs/commerce-operations/installation-guide/prerequisites/php-settings.html) 다음에서 _설치 안내서_.

{{config}}

이러한 설정 변경에 대한 자세한 내용은 [Google recaptcha](../../systems/security-google-recaptcha.md) 다음에서 _관리 시스템 안내서_.

## [!UICONTROL reCAPTCHA v2 ("I am not a robot")]

![reCAPTCHA v2(&quot;I am not a robot&quot;)](./assets/recaptcha-admin-v2-not-robot.png)<!-- zoom -->

| 필드 | [범위](../../getting-started/websites-stores-views.md#scope-settings) | 설명 |
|--|--|--|
| [!UICONTROL Google API Website Key] | 글로벌 | Google reCAPTCHA 계정을 등록할 때 생성되는 웹 사이트 키입니다. |
| [!UICONTROL Google API Secret Key] | 글로벌 | Google reCAPTCHA 계정과 연결된 비밀 키. |
| [!UICONTROL Size] | 글로벌 | 로그인 중에 표시되는 Google reCAPTCHA 상자의 크기입니다. 옵션: `Normal` (기본값) / `Compact` |
| [!UICONTROL Theme] | 글로벌 | Google reCAPTCHA 상자의 스타일을 결정합니다. 옵션: `Light Theme` (기본값) / `Dark Theme` |
| [!UICONTROL Language Code] | 글로벌 | A [문자 코드](https://developers.google.com/recaptcha/docs/language) Google reCAPTCHA 텍스트 및 메시징에 사용되는 언어를 지정합니다. |

{:style=&quot;table-layout:auto&quot;}

## [!UICONTROL reCAPTCHA v2 Invisible]

![reCAPTCHA v2 보이지 않음](./assets/recaptcha-admin-v2-invisible.png)<!-- zoom -->

| 필드 | [범위](../../getting-started/websites-stores-views.md#scope-settings) | 설명 |
|--|--|--|
| [!UICONTROL Google API Website Key] | 글로벌 | Google reCAPTCHA 계정을 등록할 때 생성되는 웹 사이트 키입니다. |
| [!UICONTROL Google API Secret Key] | 글로벌 | Google reCAPTCHA 계정과 연결된 비밀 키. |
| [!UICONTROL Invisible Badge Position] | 글로벌 | 각 페이지에서 보이지 않는 reCAPTCHA 배지의 위치입니다. 옵션: `Inline` / `Bottom Right` / `Bottom Left` |
| [!UICONTROL Theme] | 글로벌 | Google reCAPTCHA 상자의 스타일을 결정합니다. 옵션: `Light Theme` (기본값) / `Dark Theme` |
| [!UICONTROL Language Code] | 글로벌 | A [문자 코드](https://developers.google.com/recaptcha/docs/language) Google reCAPTCHA 텍스트 및 메시징에 사용되는 언어를 지정합니다. |

{:style=&quot;table-layout:auto&quot;}

## [!UICONTROL reCAPTCHA v3 Invisible]

![reCAPTCHA v3 보이지 않음](./assets/recaptcha-admin-v3-invisible.png)<!-- zoom -->

| 필드 | [범위](../../getting-started/websites-stores-views.md#scope-settings) | 설명 |
|--|--|--|
| [!UICONTROL Google API Website Key] | 글로벌 | Google reCAPTCHA 계정을 등록할 때 생성되는 웹 사이트 키입니다. |
| [!UICONTROL Google API Secret Key] | 글로벌 | Google reCAPTCHA 계정과 연결된 비밀 키. |
| [!UICONTROL Minimum Score Threshold] | 글로벌 | 사용자 상호 작용을 잠재적 위험으로 식별하는 최소 점수입니다. 여기서 1.0은 일반적인 사용자 상호 작용이고 0.0은 봇일 수 있습니다. 기본값: `0.5` |
| [!UICONTROL Invisible Badge Position] | 글로벌 | 각 페이지에서 보이지 않는 reCAPTCHA 배지의 위치입니다. 옵션: `Inline` / `Bottom Right` / `Bottom Left` |
| [!UICONTROL Theme] | 글로벌 | Google reCAPTCHA 상자의 스타일을 결정합니다. 옵션: `Light Theme` (기본값) / `Dark Theme` |
| [!UICONTROL Language Code] | 글로벌 | A [문자 코드](https://developers.google.com/recaptcha/docs/language) Google reCAPTCHA 텍스트 및 메시징에 사용되는 언어를 지정합니다. |

{:style=&quot;table-layout:auto&quot;}

## [!UICONTROL reCAPTCHA Failure Messages]

![실패 메시지](./assets/recaptcha-admin-failure-messages.png)<!-- zoom -->

| 필드 | [범위](../../getting-started/websites-stores-views.md#scope-settings) | 설명 |
|--|--|--|
| [!UICONTROL reCAPTCHA Validation Failure Message] | 글로벌 | 확인에 실패할 경우 관리자에 표시되는 메시지입니다. 기본 텍스트: `reCAPTCHA verification failed.` |
| [!UICONTROL reCAPTCHA Technical Failure Message] | 글로벌 | reCAPTCHA가 확인 결과를 반환하지 못하는 경우 관리자에 표시되는 메시지입니다. 기본 텍스트: `Something went wrong with reCAPTCHA. Please contact the store owner.` |

{:style=&quot;table-layout:auto&quot;}

## [!UICONTROL Admin Panel]

![관리 패널](./assets/recaptcha-admin-panel.png)<!-- zoom -->

>[!NOTE]
>
>선택하는 reCAPTCHA 유형은 Google reCAPTCHA 계정의 API 키와 연결된 유형과 일치해야 합니다.

>[!WARNING]
>
>reCAPTCHA 버전 3을 사용하는 경우 점수가 낮은 정품 사용자는 진행할 수 없습니다. 버전 2의 경우 점수가 낮은 정품 사용자가 도전을 받습니다. 점수가 낮은 진짜 사용자가 문제(버전 2)를 해결할 수 있는 기회를 가져야 하는지 아니면 차단(버전 3)해야 하는지 신중히 고려하십시오.

| 필드 | [범위](../../getting-started/websites-stores-views.md#scope-settings) | 설명 |
|--|--|--|
| [!UICONTROL Enable for Login] | 글로벌 | 다음에 대해 사용할 수 있는 reCAPTCHA 형식을 결정합니다. [관리자 로그인](https://experienceleague.adobe.com/docs/commerce-admin/start/admin/admin-signin.html). 옵션:<br/>**`No`**- (기본값) 관리자 로그인의 유효성을 검사하지 않습니다.<br />**`reCAPTCHA v2 ("I am not a robot")`** - 사용자가 다음을 선택해야 합니다. _난 로봇이 아니야_ 확인란.<br />**`Invisible reCAPTCHA v2`**- 점수를 기반으로 상호 작용하지 않고 백그라운드에서 사용자 행동을 확인합니다.<br/>**`Invisible reCAPTCHA v3`** - (권장) 상호 작용 점수를 기반으로 백그라운드에서 사용자 행동을 확인합니다. |
| [!UICONTROL Enable for Forgot Password] | 글로벌 | 요청을 위해 사용할 수 있는 reCAPTCHA의 유형을 결정합니다. [관리자 암호 재설정](https://experienceleague.adobe.com/docs/commerce-admin/start/admin/admin-signin.html#reset-your-password). 옵션:<br/>**`No`**- (기본값) 암호 재설정 요청의 유효성을 검사하지 않습니다.<br />**`reCAPTCHA v2 ("I am not a robot")`** - 사용자가 다음을 선택해야 합니다. _난 로봇이 아니야_ 확인란.<br />**`Invisible reCAPTCHA v2`**- 점수를 기반으로 상호 작용하지 않고 백그라운드에서 사용자 행동을 확인합니다.<br/>**`Invisible reCaptcha v3`** - (권장) 상호 작용 점수를 기반으로 백그라운드에서 사용자 행동을 확인합니다. |

{:style=&quot;table-layout:auto&quot;}
