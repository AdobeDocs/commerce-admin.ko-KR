---
title: '[!UICONTROL Security] &gt; [!UICONTROL Google reCAPTCHA Storefront]'
description: 에서 구성 설정을 검토합니다. [!UICONTROL Security] &gt; [!UICONTROL Google reCAPTCHA Storefront] 상거래 관리자의 페이지입니다.
exl-id: 6c03ee68-7421-4c74-bdc1-0855f088b7f9
feature: Configuration, Security
source-git-commit: 61df9a4bcfaf09491ae2d353478ceb281082fa74
workflow-type: tm+mt
source-wordcount: '1283'
ht-degree: 0%

---

# [!UICONTROL Security] > [!UICONTROL Google reCAPTCHA Storefront]

>[!IMPORTANT]
>
>Google reCAPTCHA를 구성하려면 먼저 다음을 확인해야 합니다. `PHP.ini` 파일에는 다음 설정이 포함되어 있습니다. `allow_url_fopen = 1`. 이 경우 개발자 지원이 필요할 수 있습니다. 다음을 참조하십시오 [PHP 설정](https://experienceleague.adobe.com/docs/commerce-operations/installation-guide/prerequisites/php-settings.html) 다음에서 _설치 안내서_.

{{config}}

Google reCAPTCHA를 사용하여 스토어를 보호하는 방법에 대한 자세한 내용은 Google 를 참조하십시오. [reCAPT차](../../systems/security-google-recaptcha.md) 다음에서 _관리 시스템 안내서_.

## [!UICONTROL reCAPTCHA v2 ("I am not a robot")]

![reCAPTCHA v2(&quot;I am not a robot&quot;)](./assets/recaptcha-storefront-v2-not-robot.png)<!-- zoom -->

| 필드 | [범위](../../getting-started/websites-stores-views.md#scope-settings) | 설명 |
|--|--|--|
| [!UICONTROL Google API Website Key] | 웹 사이트 | Google reCAPTCHA 계정을 등록할 때 생성되는 웹 사이트 키입니다. |
| [!UICONTROL Google API Secret Key] | 웹 사이트 | Google reCAPTCHA 계정과 연결된 비밀 키. |
| [!UICONTROL Size] | 웹 사이트 | 고객이 계정에 로그인할 때 표시되는 Google reCAPTCHA 상자의 크기입니다. 옵션: `Normal` (기본값) / `Compact` |
| [!UICONTROL Theme] | 웹 사이트 | Google reCAPTCHA 상자의 스타일을 결정합니다. 옵션: `Light Theme` (기본값) / `Dark Theme` |
| [!UICONTROL Language Code] | 스토어 보기 | 다음 [문자 코드](https://developers.google.com/recaptcha/docs/language) Google reCAPTCHA 텍스트 및 메시징에 사용되는 언어를 지정합니다. |

{style="table-layout:auto"}

## [!UICONTROL reCAPTCHA v2 Invisible]

![reCAPTCHA v2 보이지 않음](./assets/recaptcha-storefront-v2-invisible.png)<!-- zoom -->

| 필드 | [범위](../../getting-started/websites-stores-views.md#scope-settings) | 설명 |
|--|--|--|
| [!UICONTROL Google API Website Key] | 웹 사이트 | Google reCAPTCHA 계정을 등록할 때 생성되는 웹 사이트 키입니다. |
| [!UICONTROL Google API Secret Key] | 웹 사이트 | Google reCAPTCHA 계정과 연결된 비밀 키. |
| [!UICONTROL Invisible Badge Position] | 웹 사이트 | 각 페이지에서 보이지 않는 reCAPTCHA 배지의 위치입니다. 옵션: `Inline` / `Bottom Right` / `Bottom Left` |
| [!UICONTROL Theme] | 글로벌 | Google reCAPTCHA 상자의 스타일을 결정합니다. 옵션: `Light Theme` (기본값) / `Dark Theme` |
| [!UICONTROL Language Code] | 스토어 보기 | A [문자 코드](https://developers.google.com/recaptcha/docs/language) Google reCAPTCHA 텍스트 및 메시징에 사용되는 언어를 지정합니다. |

{style="table-layout:auto"}

## [!UICONTROL reCAPTCHA v3 Invisible]

![reCAPTCHA v3 보이지 않음](./assets/recaptcha-storefront-v3-invisible.png)<!-- zoom -->

| 필드 | [범위](../../getting-started/websites-stores-views.md#scope-settings) | 설명 |
|--|--|--|
| [!UICONTROL Google API Website Key] | 웹 사이트 | Google reCAPTCHA 계정을 등록할 때 생성되는 웹 사이트 키입니다. |
| [!UICONTROL Google API Secret Key] | 웹 사이트 | Google reCAPTCHA 계정과 연결된 비밀 키. |
| [!UICONTROL Minimum Score Threshold] | 글로벌 | 사용자 상호 작용을 잠재적 위험으로 식별하는 최소 점수입니다. 여기서 1.0은 일반적인 사용자 상호 작용이고 0.0은 봇일 수 있습니다. 기본값: `0.5` |
| [!UICONTROL Invisible Badge Position] | 웹 사이트 | 각 페이지에서 보이지 않는 reCAPTCHA 배지의 위치입니다. 옵션: `Inline` / `Bottom Right` / `Bottom Left` |
| [!UICONTROL Theme] | 웹 사이트 | Google reCAPTCHA 상자의 스타일을 결정합니다. 옵션: `Light Theme` (기본값) / `Dark Theme` |
| [!UICONTROL Language Code] | 스토어 보기 | A [문자 코드](https://developers.google.com/recaptcha/docs/language) Google reCAPTCHA 텍스트 및 메시징에 사용되는 언어를 지정합니다. |

{style="table-layout:auto"}

## [!UICONTROL reCAPTCHA Failure Messages]

![실패 메시지](./assets/recaptcha-storefront-failure-messages.png)<!-- zoom -->

| 필드 | [범위](../../getting-started/websites-stores-views.md#scope-settings) | 설명 |
|--|--|--|
| [!UICONTROL reCAPTCHA Validation Failure Message] | 스토어 보기 | 확인이 실패할 경우 상점 앞에 표시되는 메시지입니다. 기본 텍스트: `reCAPTCHA verification failed.` |
| [!UICONTROL reCAPTCHA Technical Failure Message] | 스토어 보기 | reCAPTCHA가 확인 결과를 반환하지 못하는 경우 상점 앞에 표시되는 메시지입니다. 기본 텍스트: `Something went wrong with reCAPTCHA. Please contact the store owner.` |

{style="table-layout:auto"}

## [!UICONTROL Storefront]

![상점 첫 화면](./assets/recaptcha-storefront.png)<!-- zoom -->

>[!NOTE]
>
>선택하는 reCAPTCHA 유형은 Google reCAPTCHA 계정의 API 키와 연결된 유형과 일치해야 합니다.

>[!WARNING]
>
>reCAPTCHA 버전 3을 사용하는 경우 점수가 낮은 정품 사용자는 진행할 수 없습니다. 버전 2의 경우 점수가 낮은 정품 사용자가 도전을 받습니다. 점수가 낮은 진짜 사용자가 문제(버전 2)를 해결할 수 있는 기회를 가져야 하는지 아니면 차단(버전 3)해야 하는지 신중히 고려하십시오.

| 필드 | [범위](../../getting-started/websites-stores-views.md#scope-settings) | 설명 |
|--|--|--|
| [!UICONTROL Enable for Customer Login] | 웹 사이트 | 고객이 사용할 때 사용되는 reCAPTCHA 형식을 지정합니다. [로그인](../../customers/customer-sign-in.md) 계정 관리. 옵션:<br/>**`No`**- (기본값) 로그인 요청을 확인하지 않습니다.<br />**`reCAPTCHA v2 ("I am not a robot")`** - 사용자가 다음을 선택해야 합니다. _난 로봇이 아니야_ 확인란.<br />**`Invisible reCAPTCHA v2`**- 점수를 기반으로 상호 작용하지 않고 백그라운드에서 사용자 행동을 확인합니다.<br/>**`Invisible reCAPTCHA v3`** - (권장) 상호 작용 점수를 기반으로 백그라운드에서 사용자 행동을 확인합니다. |
| [!UICONTROL Enable for Forgot Password] | 웹 사이트 | 고객이 를 요청할 때 사용되는 reCAPTCHA 형식을 지정합니다. [암호 재설정](../../customers/password-reset.md). 옵션:<br/>**`No`**- (기본값) 암호 재설정 요청의 유효성을 검사하지 않습니다.<br />**`reCAPTCHA v2 ("I am not a robot")`** - 사용자가 다음을 선택해야 합니다. _난 로봇이 아니야_ 확인란.<br />**`Invisible reCAPTCHA v2`**- 점수를 기반으로 상호 작용하지 않고 백그라운드에서 사용자 행동을 확인합니다.<br/>**`Invisible reCAPTCHA v3`** - (권장) 상호 작용 점수를 기반으로 백그라운드에서 사용자 행동을 확인합니다. |
| [!UICONTROL Enable for Create New Customer Account] | 웹 사이트 | 고객이 다음에 등록할 때 사용되는 reCAPTCHA의 유형을 지정합니다. [새 계정](../../customers/account-create.md). 옵션:<br/>**`No`**- (기본값) 계정 요청을 확인하지 않습니다.<br />**`reCAPTCHA v2 ("I am not a robot")`** - 사용자가 다음을 선택해야 합니다. _난 로봇이 아니야_ 확인란.<br />**`Invisible reCAPTCHA v2`**- 점수를 기반으로 상호 작용하지 않고 백그라운드에서 사용자 행동을 확인합니다.<br/>**`Invisible reCAPTCHA v3`** - (권장) 상호 작용 점수를 기반으로 백그라운드에서 사용자 행동을 확인합니다. |
| [!UICONTROL Enable for Edit Customer Account] | 웹 사이트 | 고객이 변경할 때 사용되는 reCAPTCHA 유형을 지정합니다. [계정 정보](../../customers/account-dashboard-account-information.md). 옵션:<br/>**`No`**- (기본값) 계정 요청을 확인하지 않습니다.<br />**`reCAPTCHA v2 ("I am not a robot")`** - 사용자가 다음을 선택해야 합니다. _난 로봇이 아니야_ 확인란.<br />**`Invisible reCAPTCHA v2`**- 점수를 기반으로 상호 작용하지 않고 백그라운드에서 사용자 행동을 확인합니다.<br/>**`Invisible reCAPTCHA v3`** - (권장) 상호 작용 점수를 기반으로 백그라운드에서 사용자 행동을 확인합니다. |
| [!UICONTROL Enable for Create New Company Account] | 웹 사이트 | ![Adobe Commerce](../../assets/b2b.svg) (Adobe Commerce B2B에서만 사용 가능) [회사 계정](../../b2b/account-company-create.md) 이(가) 만들어졌습니다. 옵션:<br/>**`No`**- (기본값) 계정 요청을 확인하지 않습니다.<br />**`reCAPTCHA v2 ("I am not a robot")`** - 사용자가 다음을 선택해야 합니다. _난 로봇이 아니야_ 확인란.<br />**`Invisible reCAPTCHA v2`**- 점수를 기반으로 상호 작용하지 않고 백그라운드에서 사용자 행동을 확인합니다.<br/>**`Invisible reCAPTCHA v3`** - (권장) 상호 작용 점수를 기반으로 백그라운드에서 사용자 행동을 확인합니다. |
| [!UICONTROL Enable for Contact Us] | 웹 사이트 | 에서 메시지를 보내는 데 사용되는 reCAPTCHA 형식을 지정합니다. [연락처](../../getting-started/store-details.md#contact-us-form) 스토어의 페이지입니다. 옵션:<br/>**`No`**- (기본값) 메시지 요청을 확인하지 않습니다.<br />**`reCAPTCHA v2 ("I am not a robot")`** - 사용자가 다음을 선택해야 합니다. _난 로봇이 아니야_ 확인란.<br />**`Invisible reCAPTCHA v2`**- 점수를 기반으로 상호 작용하지 않고 백그라운드에서 사용자 행동을 확인합니다.<br/>**`Invisible reCAPTCHA v3`** - (권장) 상호 작용 점수를 기반으로 백그라운드에서 사용자 행동을 확인합니다. |
| [!UICONTROL Enable for Product Review] | 웹 사이트 | 고객이 파일을 제출할 때 사용되는 reCAPTCHA 형식을 지정합니다. [제품 리뷰](../../merchandising-promotions/product-reviews.md). 옵션:<br/>**`No`**- (기본값) 제품 검토 요청을 확인하지 않습니다.<br />**`reCAPTCHA v2 ("I am not a robot")`** - 사용자가 다음을 선택해야 합니다. _난 로봇이 아니야_ 확인란.<br />**`Invisible reCAPTCHA v2`**- 점수를 기반으로 상호 작용하지 않고 백그라운드에서 사용자 행동을 확인합니다.<br/>**`Invisible reCAPTCHA v3`** - (권장) 상호 작용 점수를 기반으로 백그라운드에서 사용자 행동을 확인합니다. |
| [!UICONTROL Enable for Newsletter Subscription] | 웹 사이트 | 고객이 다음에 등록할 때 사용되는 보이지 않는 reCAPTCHA의 유형을 지정합니다. [뉴스레터 구독](../../merchandising-promotions/newsletter-subscribers.md). 옵션:<br/>**`No`**- (기본값) 뉴스레터 구독 요청을 확인하지 않습니다.<br />**`reCAPTCHA v2 ("I am not a robot")`** - 사용자가 다음을 선택해야 합니다. _난 로봇이 아니야_ 확인란.<br />**`Invisible reCAPTCHA v2`**- 점수를 기반으로 상호 작용하지 않고 백그라운드에서 사용자 행동을 확인합니다.<br/>**`Invisible reCAPTCHA v3`** - (권장) 상호 작용 점수를 기반으로 백그라운드에서 사용자 행동을 확인합니다. |
| [!UICONTROL Enable for Gift Card] | 웹 사이트 | ![Adobe Commerce](../../assets/adobe-logo.svg) (Adobe Commerce만 해당) 고객이 를 입력할 때 사용되는 reCAPTCHA의 유형을 지정합니다. [기프트 카드](../../catalog/product-gift-card-create.md) 코드. 옵션:<br/>**`No`**- (기본값) 기프트 카드 코드 제출의 유효성을 검사하지 않습니다.<br />**`reCAPTCHA v2 ("I am not a robot")`** - 사용자가 다음을 선택해야 합니다. _난 로봇이 아니야_ 확인란.<br />**`Invisible reCAPTCHA v2`**- 점수에 따라 상호 작용하지 않고 백그라운드에서 사용자 비헤이비어를 확인합니다.<br/>**`Invisible reCAPTCHA v3`** - (권장) 상호 작용 점수를 기반으로 백그라운드에서 사용자 행동을 확인합니다. |
| [!UICONTROL Enable for Invitation Create Account] | 웹 사이트 | 고객이 계정 만들기를 보낼 때 사용되는 reCAPTCHA 유형을 지정합니다 [초대](../../merchandising-promotions/invitations.md) 코드. 옵션:<br/>**`No`**- (기본값) 초대 이메일 제출의 유효성을 검사하지 않습니다.<br />**`reCAPTCHA v2 ("I am not a robot")`** - 사용자가 다음을 선택해야 합니다. _난 로봇이 아니야_ 확인란.<br />**`Invisible reCAPTCHA v2`**- 점수에 따라 상호 작용하지 않고 백그라운드에서 사용자 비헤이비어를 확인합니다.<br/>**`Invisible reCAPTCHA v3`** - (권장) 상호 작용 점수를 기반으로 백그라운드에서 사용자 행동을 확인합니다. |
| [!UICONTROL Enable for Send to Friend] | 웹 사이트 | 고객이 사용할 때 사용되는 reCAPTCHA 형식을 지정합니다. [제품 공유](../../stores-purchase/email-a-friend.md) 친구와 함께. 옵션:<br/>**`No`**- (기본값) 이메일 제출을 확인하지 않습니다.<br />**`reCAPTCHA v2 ("I am not a robot")`** - 사용자가 다음을 선택해야 합니다. _난 로봇이 아니야_ 확인란.<br />**`Invisible reCAPTCHA v2`**- 점수를 기반으로 상호 작용하지 않고 백그라운드에서 사용자 행동을 확인합니다.<br/>**`Invisible reCAPTCHA v3`** - (권장) 상호 작용 점수를 기반으로 백그라운드에서 사용자 행동을 확인합니다. |
| [!UICONTROL Enable for Wishlist Sharing] | 웹 사이트 | 고객이 사용할 때 사용되는 reCAPTCHA 형식을 지정합니다. [위시리스트 공유](../../stores-purchase/wishlist-storefront.md#share-the-wish-list). 옵션:<br/>**`No`**- (기본값) 메시지 및 이메일 제출의 유효성을 검사하지 않습니다.<br />**`reCAPTCHA v2 ("I am not a robot")`** - 사용자가 다음을 선택해야 합니다. _난 로봇이 아니야_ 확인란.<br />**`Invisible reCAPTCHA v2`**- 점수에 따라 상호 작용하지 않고 백그라운드에서 사용자 비헤이비어를 확인합니다.<br/>**`Invisible reCAPTCHA v3`** - (권장) 상호 작용 점수를 기반으로 백그라운드에서 사용자 행동을 확인합니다. |
| [!UICONTROL Enable for Coupon Codes] | 웹 사이트 | 고객이 를 입력할 때 사용되는 reCAPTCHA 형식을 지정합니다. [쿠폰 코드](../../merchandising-promotions/price-rules-cart-coupon.md). 옵션:<br/>**`No`**- (기본값) 쿠폰 코드 제출을 검증하지 않습니다.<br />**`reCAPTCHA v2 ("I am not a robot")`** - 사용자가 다음을 선택해야 합니다. _난 로봇이 아니야_ 확인란.<br />**`Invisible reCAPTCHA v2`**- 점수에 따라 상호 작용하지 않고 백그라운드에서 사용자 비헤이비어를 확인합니다.<br/>**`Invisible reCAPTCHA v3`** - (권장) 상호 작용 점수를 기반으로 백그라운드에서 사용자 행동을 확인합니다. |
| [!UICONTROL Enable for PayPal Payflow Pro payment form] | 웹 사이트 | 고객이 로 구매 비용을 지불할 때 사용되는 reCAPTCHA 유형을 지정합니다. [Paypal Payflow Pro](../../stores-purchase/paypal-payflow-pro.md). 옵션:<br/>**`No`**- (기본값) 암호 재설정 요청의 유효성을 검사하지 않습니다.<br />**`reCAPTCHA v2 ("I am not a robot")`** - 사용자가 다음을 선택해야 합니다. _난 로봇이 아니야_ 확인란.<br />**`Invisible reCAPTCHA v2`**- 점수를 기반으로 상호 작용하지 않고 백그라운드에서 사용자 행동을 확인합니다.<br/>**`Invisible reCAPTCHA v3`** - (권장) 상호 작용 점수를 기반으로 백그라운드에서 사용자 행동을 확인합니다. |

{style="table-layout:auto"}
