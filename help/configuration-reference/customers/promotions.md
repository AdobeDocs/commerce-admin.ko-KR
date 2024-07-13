---
title: '[!UICONTROL Customers] &gt; [!UICONTROL Promotions]'
description: Commerce 관리자의 [!UICONTROL Customers] &gt; [!UICONTROL Promotions] 페이지에서 구성 설정을 검토하십시오.
exl-id: 93035d46-2e9e-466d-a5e3-d69ce6b662b8
feature: Configuration, Promotions/Events
source-git-commit: b710c0368dc765e3bf25e82324bffe7fb8192dbf
workflow-type: tm+mt
source-wordcount: '331'
ht-degree: 0%

---

# [!UICONTROL Customers] > [!UICONTROL Promotions]

{{config}}

## [!UICONTROL Automated Email Reminder Rules]

{{ee-feature}}

![자동화된 전자 메일 미리 알림 규칙](./assets/promotions-automated-email-reminder-rules.png)<!-- zoom -->

<!-- [Automated Email Reminder Rules](https://docs.magento.com/user-guide/marketing/email-reminder-rules-configure.html) -->

| 필드 | [범위](../../getting-started/websites-stores-views.md#scope-settings) | 설명 |
|--- |--- |--- |
| [!UICONTROL Enable Reminder Emails] | 글로벌 | 자동 이메일 미리 알림을 활성화합니다. 이 값을 아니요로 설정하면 나머지 설정은 무시됩니다. 옵션: `Yes` / `No` |
| [!UICONTROL Frequency] | 글로벌 | Commerce에서 자동화된 이메일 미리 알림에 대한 자격이 되는 신규 고객을 확인해야 하는 빈도를 나타냅니다. 옵션: <br/>**`Minute Intervals`**- 선택한 간격에 따라 이메일을 전송합니다. (5분, 10분, 15분, 20분 또는 30분)<br/>**`Hourly`** - 지정된 시간 이후 분 단위로 이메일을 전송합니다. 0~59 사이의 값을 입력하십시오. <br/>**`Daily`**- 시작 시간부터 매일 이메일을 전송합니다. |
| [!UICONTROL Interval] | 글로벌 | 간격은 cron.php 시작 기간보다 크거나 같아야 합니다. 옵션: `5 minutes` / `10 minutes` / `15 minutes` / `20 minutes` / `30 minutes` |
| [!UICONTROL Start Time] | 글로벌 | 이메일이 전송되는 날짜, 분 및 초를 설정합니다. 서버의 시스템 시간을 기반으로 24시간 형식으로 지정됩니다. |
| [!UICONTROL Maximum Emails per One Run] | 글로벌 | 예약된 블록에서 전송되는 이메일 수를 제한합니다. |
| [!UICONTROL Email Send Failure Threshold] | 글로벌 | 미리 알림이 특정 이메일 주소로 알림을 전송하려고 시도했으나 실패한 횟수. 이 값을 0으로 설정하면 임계값이 없으며, 어떠한 실패에도 불구하고 알림이 계속 전송됩니다. |
| [!UICONTROL Reminder Email Sender] | 스토어 뷰 | 이메일 발신자로 표시되는 스토어 ID입니다. |

{style="table-layout:auto"}

## [!UICONTROL Auto Generated Specific Coupon Codes]

![특정 쿠폰 코드 자동 생성](./assets/promotions-auto-generated-specific-coupon-codes.png)<!-- zoom -->

<!-- [Auto Generated Specific Coupon Codes](https://docs.magento.com/user-guide/marketing/price-rules-cart-coupon-code-configure.md  -->

| 필드 | [범위](../../getting-started/websites-stores-views.md#scope-settings) | 설명 |
|--- |--- |--- |
| [!UICONTROL Code Length] | 글로벌 | 접두어, 접미어 및 구분 기호를 제외한 쿠폰 코드의 길이를 정의합니다. |
| [!UICONTROL Code Format] | 글로벌 | 쿠폰 코드 형식을 정의합니다. 옵션은 다음과 같습니다. <br/>**`Alphanumeric`**- 문자와 숫자의 모든 조합.<br/>**`Alphabetical`** - 문자만 <br/>**`Numeric`**- 숫자만. |
| [!UICONTROL Code Prefix] | 글로벌 | 모든 쿠폰 코드의 시작 부분에 추가되는 값입니다. 접두사를 사용하지 않으려면 필드를 비워 둡니다. |
| [!UICONTROL Code Suffix] | 글로벌 | 모든 코드의 끝에 추가되는 값입니다. 접미사를 사용하지 않으려면 필드를 비워 둡니다. |
| [!UICONTROL Dash Every X Characters] | 글로벌 | 모든 쿠폰 코드에 대시(-)를 삽입하는 간격입니다. 대시를 사용하지 않으려면 필드를 비워 둡니다. <br/>_**참고:**_ 대시 값만 다른 쿠폰 코드는 다른 코드로 간주됩니다. |

{style="table-layout:auto"}
