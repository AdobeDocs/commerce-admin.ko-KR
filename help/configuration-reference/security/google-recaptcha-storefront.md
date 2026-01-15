---
title: '[!UICONTROL Security] &gt; [!UICONTROL Google reCAPTCHA Storefront]'
description: Commerce 관리자의 [!UICONTROL Security] &gt; [!UICONTROL Google reCAPTCHA Storefront] 페이지에서 구성 설정을 검토하십시오.
exl-id: 6c03ee68-7421-4c74-bdc1-0855f088b7f9
feature: Configuration, Security
source-git-commit: 528e57df775b53b6137e1542ad0583c60d2f47ff
workflow-type: tm+mt
source-wordcount: '1481'
ht-degree: 0%

---

# [!UICONTROL Security] > [!UICONTROL Google reCAPTCHA Storefront]

>[!IMPORTANT]
>
>Google reCAPTCHA를 구성하려면 `PHP.ini` 파일에 다음 설정이 포함되어 있는지 확인해야 합니다. `allow_url_fopen = 1`. 이 경우 개발자 지원이 필요할 수 있습니다. [설치 안내서](https://experienceleague.adobe.com/docs/commerce-operations/installation-guide/prerequisites/php-settings.html)에서 _PHP 설정_&#x200B;을 참조하십시오.

{{config}}

Google reCAPTCHA를 사용하여 스토어를 보호하는 방법에 대한 자세한 내용은 [관리 시스템 안내서](../../systems/security-google-recaptcha.md)에서 Google _reCAPTCHA_&#x200B;을(를) 참조하십시오.

## [!UICONTROL reCAPTCHA v2 ("I am not a robot")]

![reCAPTCHA v2(&quot;I am not a robot&quot;)](./assets/recaptcha-storefront-v2-not-robot.png)<!-- zoom -->

| 필드 | [범위](../../getting-started/websites-stores-views.md#scope-settings) | 설명 |
|--|--|--|
| [!UICONTROL Google API Website Key] | 웹 사이트 | Google reCAPTCHA 계정을 등록할 때 생성되는 웹 사이트 키입니다. |
| [!UICONTROL Google API Secret Key] | 웹 사이트 | Google reCAPTCHA 계정과 연결된 비밀 키. |
| [!UICONTROL Size] | 웹 사이트 | 고객이 계정에 로그인할 때 표시되는 Google reCAPTCHA 상자의 크기입니다. 옵션: `Normal`(기본값) / `Compact` |
| [!UICONTROL Theme] | 웹 사이트 | Google reCAPTCHA 상자의 스타일을 결정합니다. 옵션: `Light Theme`(기본값) / `Dark Theme` |
| [!UICONTROL Language Code] | 스토어 보기 | Google reCAPTCHA 텍스트 및 메시징에 사용되는 언어를 지정하는 [2자 코드](https://developers.google.com/recaptcha/docs/language). |

{style="table-layout:auto"}

## [!UICONTROL reCAPTCHA v2 Invisible]

![reCAPTCHA v2 보이지 않음](./assets/recaptcha-storefront-v2-invisible.png)<!-- zoom -->

| 필드 | [범위](../../getting-started/websites-stores-views.md#scope-settings) | 설명 |
|--|--|--|
| [!UICONTROL Google API Website Key] | 웹 사이트 | Google reCAPTCHA 계정을 등록할 때 생성되는 웹 사이트 키입니다. |
| [!UICONTROL Google API Secret Key] | 웹 사이트 | Google reCAPTCHA 계정과 연결된 비밀 키. |
| [!UICONTROL Invisible Badge Position] | 웹 사이트 | 각 페이지에서 보이지 않는 reCAPTCHA 배지의 위치입니다. 옵션: `Inline` / `Bottom Right` / `Bottom Left` |
| [!UICONTROL Theme] | 글로벌 | Google reCAPTCHA 상자의 스타일을 결정합니다. 옵션: `Light Theme`(기본값) / `Dark Theme` |
| [!UICONTROL Language Code] | 스토어 보기 | Google reCAPTCHA 텍스트 및 메시징에 사용되는 언어를 지정하는 [2자 코드](https://developers.google.com/recaptcha/docs/language). |

{style="table-layout:auto"}

## [!UICONTROL reCAPTCHA v3 Invisible]

![reCAPTCHA v3 보이지 않음](./assets/recaptcha-storefront-v3-invisible.png)<!-- zoom -->

| 필드 | [범위](../../getting-started/websites-stores-views.md#scope-settings) | 설명 |
|--|--|--|
| [!UICONTROL Google API Website Key] | 웹 사이트 | Google reCAPTCHA 계정을 등록할 때 생성되는 웹 사이트 키입니다. |
| [!UICONTROL Google API Secret Key] | 웹 사이트 | Google reCAPTCHA 계정과 연결된 비밀 키. |
| [!UICONTROL Minimum Score Threshold] | 글로벌 | 사용자 상호 작용을 잠재적 위험으로 식별하는 최소 점수입니다. 여기서 1.0은 일반적인 사용자 상호 작용이고 0.0은 봇일 수 있습니다. 기본값: `0.5` |
| [!UICONTROL Invisible Badge Position] | 웹 사이트 | 각 페이지에서 보이지 않는 reCAPTCHA 배지의 위치입니다. 옵션: `Inline` / `Bottom Right` / `Bottom Left` |
| [!UICONTROL Theme] | 웹 사이트 | Google reCAPTCHA 상자의 스타일을 결정합니다. 옵션: `Light Theme`(기본값) / `Dark Theme` |
| [!UICONTROL Language Code] | 스토어 보기 | Google reCAPTCHA 텍스트 및 메시징에 사용되는 언어를 지정하는 [2자 코드](https://developers.google.com/recaptcha/docs/language). |

{style="table-layout:auto"}

## [!UICONTROL reCAPTCHA Enterprise]

[!BADGE SaaS만]{type=Positive url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="Adobe Commerce as a Cloud Service 프로젝트에만 적용됩니다(Adobe 관리 SaaS 인프라)."}

[!BADGE 샌드박스]{type=Caution tooltip="나열된 항목은 현재 샌드박스 환경에서만 사용할 수 있습니다. Adobe은 프로덕션 환경에서 릴리스를 사용하기 전에 예정된 변경 사항을 테스트할 시간을 제공하기 위해 먼저 샌드박스 환경에서 새 릴리스를 사용할 수 있도록 합니다."}

![reCAPTCHA v3 Enterprise](./assets/recaptcha-storefront-v3-enterprise.png)<!-- zoom -->

| 필드 | [범위](../../getting-started/websites-stores-views.md#scope-settings) | 설명 |
|--|--|--|
| [!UICONTROL Site Key] | 웹 사이트 | Google reCAPTCHA Enterprise 계정을 등록할 때 생성되는 사이트 키입니다. |
| [!UICONTROL Google Cloud Project ID] | 웹 사이트 | 프로젝트 ID가 프로젝트 대시보드의 **프로젝트 정보** 섹션에 표시됩니다. |
| [!UICONTROL Service Account JSON] | 웹 사이트 | Google Cloud 콘솔에서 서비스 계정 키를 다운로드하고 해당 콘텐츠를 이 필드에 붙여넣습니다. |
| [!UICONTROL Minimum Score Threshold] | 웹 사이트 | 사용자 상호 작용을 잠재적 위험으로 식별하는 최소 점수입니다. 여기서 1.0은 일반적인 사용자 상호 작용이고 0.0은 봇일 수 있습니다. 기본값: `0.5` |
| [!UICONTROL Badge Position] | 웹 사이트 | 각 페이지에서 보이지 않는 reCAPTCHA 배지의 위치입니다. 옵션: `Inline` / `Bottom Right` / `Bottom Left` |
| [!UICONTROL Theme] | 웹 사이트 | Google reCAPTCHA 상자의 스타일을 결정합니다. 옵션: `Light Theme`(기본값) / `Dark Theme` |
| [!UICONTROL Language Code] | 스토어 보기 | Google reCAPTCHA 텍스트 및 메시징에 사용되는 언어를 지정하는 [2자 코드](https://developers.google.com/recaptcha/docs/language). 사용자 브라우저의 기본 언어를 사용하려면 필드를 비워 둡니다. |
| [!UICONTROL Validation Failure Message] | 스토어 보기 | 유효성 검사 실패 시 표시되는 메시지입니다. |

{style="table-layout:auto"}

## [!UICONTROL reCAPTCHA Failure Messages]

![실패 메시지](./assets/recaptcha-storefront-failure-messages.png)<!-- zoom -->

| 필드 | [범위](../../getting-started/websites-stores-views.md#scope-settings) | 설명 |
|--|--|--|
| [!UICONTROL reCAPTCHA Validation Failure Message] | 스토어 보기 | 확인이 실패할 경우 상점 앞에 표시되는 메시지입니다. 기본 텍스트: `reCAPTCHA verification failed.` |
| [!UICONTROL reCAPTCHA Technical Failure Message] | 스토어 보기 | reCAPTCHA가 확인 결과를 반환하지 못하는 경우 상점 앞에 표시되는 메시지입니다. 기본 텍스트: `Something went wrong with reCAPTCHA. Please contact the store owner.` |

{style="table-layout:auto"}

## [!UICONTROL Storefront]

![Storefront](./assets/recaptcha-storefront.png)<!-- zoom -->

>[!NOTE]
>
>선택하는 reCAPTCHA 유형은 Google reCAPTCHA 계정의 API 키와 연결된 유형과 일치해야 합니다.

>[!WARNING]
>
>reCAPTCHA 버전 3을 사용하는 경우 점수가 낮은 정품 사용자는 진행할 수 없습니다. 버전 2의 경우 점수가 낮은 정품 사용자가 도전을 받습니다. 점수가 낮은 진짜 사용자가 문제(버전 2)를 해결할 수 있는 기회를 가져야 하는지 아니면 차단(버전 3)해야 하는지 신중히 고려하십시오.

| 필드 | [범위](../../getting-started/websites-stores-views.md#scope-settings) | 설명 |
|--|--|--|
| [!UICONTROL Enable for Customer Login] | 웹 사이트 | 고객이 계정에 [로그인](../../customers/customer-sign-in.md)할 때 사용되는 reCAPTCHA 형식을 지정합니다. 옵션:<br/>**`No`**- (기본값) 로그인 요청의 유효성을 검사하지 않습니다.<br />**`reCAPTCHA v2 ("I am not a robot")`** - 사용자가 _로봇이 아닙니다_ 확인란을 선택해야 합니다.<br />**`Invisible reCAPTCHA v2`**- 점수를 기반으로 상호 작용하지 않고 백그라운드에서 사용자 동작을 확인합니다.<br/>**`Invisible reCAPTCHA v3`** - (권장) 상호 작용 점수를 기반으로 백그라운드에서 사용자 동작을 확인합니다. |
| [!UICONTROL Enable for Forgot Password] | 웹 사이트 | 고객이 [암호 재설정](../../customers/password-reset.md)을 요청할 때 사용되는 reCAPTCHA의 유형을 지정합니다. 옵션:<br/>**`No`**- (기본값) 암호 재설정 요청의 유효성을 검사하지 않습니다.<br />**`reCAPTCHA v2 ("I am not a robot")`** - 사용자가 _로봇이 아닙니다_ 확인란을 선택해야 합니다.<br />**`Invisible reCAPTCHA v2`**- 점수를 기반으로 상호 작용하지 않고 백그라운드에서 사용자 동작을 확인합니다.<br/>**`Invisible reCAPTCHA v3`** - (권장) 상호 작용 점수를 기반으로 백그라운드에서 사용자 동작을 확인합니다. |
| [!UICONTROL Enable for Create New Customer Account] | 웹 사이트 | 고객이 [새 계정](../../customers/account-create.md)에 등록할 때 사용되는 reCAPTCHA의 유형을 지정합니다. 옵션:<br/>**`No`**- (기본값) 계정 요청의 유효성을 검사하지 않습니다.<br />**`reCAPTCHA v2 ("I am not a robot")`** - 사용자가 _로봇이 아닙니다_ 확인란을 선택해야 합니다.<br />**`Invisible reCAPTCHA v2`**- 점수를 기반으로 상호 작용하지 않고 백그라운드에서 사용자 동작을 확인합니다.<br/>**`Invisible reCAPTCHA v3`** - (권장) 상호 작용 점수를 기반으로 백그라운드에서 사용자 동작을 확인합니다. |
| [!UICONTROL Enable for Edit Customer Account] | 웹 사이트 | 고객이 [계정 정보](../../customers/account-dashboard-account-information.md)를 변경할 때 사용되는 reCAPTCHA 형식을 지정합니다. 옵션:<br/>**`No`**- (기본값) 계정 요청의 유효성을 검사하지 않습니다.<br />**`reCAPTCHA v2 ("I am not a robot")`** - 사용자가 _로봇이 아닙니다_ 확인란을 선택해야 합니다.<br />**`Invisible reCAPTCHA v2`**- 점수를 기반으로 상호 작용하지 않고 백그라운드에서 사용자 동작을 확인합니다.<br/>**`Invisible reCAPTCHA v3`** - (권장) 상호 작용 점수를 기반으로 백그라운드에서 사용자 동작을 확인합니다. |
| [!UICONTROL Enable for Create New Company Account] | 웹 사이트 | ![Adobe Commerce B2B](../../assets/b2b.svg)(Adobe Commerce B2B에서만 사용 가능) 새 [회사 계정](../../b2b/account-company-create.md)을(를) 만들 때 사용되는 reCAPTCHA 형식을 지정합니다. 옵션:<br/>**`No`**- (기본값) 계정 요청의 유효성을 검사하지 않습니다.<br />**`reCAPTCHA v2 ("I am not a robot")`** - 사용자가 _로봇이 아닙니다_ 확인란을 선택해야 합니다.<br />**`Invisible reCAPTCHA v2`**- 점수를 기반으로 상호 작용하지 않고 백그라운드에서 사용자 동작을 확인합니다.<br/>**`Invisible reCAPTCHA v3`** - (권장) 상호 작용 점수를 기반으로 백그라운드에서 사용자 동작을 확인합니다. |
| [!UICONTROL Enable for Contact Us] | 웹 사이트 | 스토어의 [연락처](../../getting-started/store-details.md#contact-us-form) 페이지에서 메시지를 보내는 데 사용되는 reCAPTCHA 형식을 지정합니다. 옵션:<br/>**`No`**- (기본값) 메시지 요청의 유효성을 검사하지 않습니다.<br />**`reCAPTCHA v2 ("I am not a robot")`** - 사용자가 _로봇이 아닙니다_ 확인란을 선택해야 합니다.<br />**`Invisible reCAPTCHA v2`**- 점수를 기반으로 상호 작용하지 않고 백그라운드에서 사용자 동작을 확인합니다.<br/>**`Invisible reCAPTCHA v3`** - (권장) 상호 작용 점수를 기반으로 백그라운드에서 사용자 동작을 확인합니다. |
| [!UICONTROL Enable for Product Review] | 웹 사이트 | 고객이 [제품 검토](../../merchandising-promotions/product-reviews.md)를 제출할 때 사용되는 reCAPTCHA 형식을 지정합니다. 옵션:<br/>**`No`**- (기본값) 제품 검토 요청의 유효성을 검사하지 않습니다.<br />**`reCAPTCHA v2 ("I am not a robot")`** - 사용자가 _로봇이 아닙니다_ 확인란을 선택해야 합니다.<br />**`Invisible reCAPTCHA v2`**- 점수를 기반으로 상호 작용하지 않고 백그라운드에서 사용자 동작을 확인합니다.<br/>**`Invisible reCAPTCHA v3`** - (권장) 상호 작용 점수를 기반으로 백그라운드에서 사용자 동작을 확인합니다. |
| [!UICONTROL Enable for Newsletter Subscription] | 웹 사이트 | 고객이 [뉴스레터 구독](../../merchandising-promotions/newsletter-subscribers.md)에 등록할 때 사용되는 보이지 않는 reCAPTCHA의 유형을 지정합니다. 옵션:<br/>**`No`**- (기본값) 뉴스레터 구독 요청의 유효성을 검사하지 않습니다.<br />**`reCAPTCHA v2 ("I am not a robot")`** - 사용자가 _로봇이 아닙니다_ 확인란을 선택해야 합니다.<br />**`Invisible reCAPTCHA v2`**- 점수를 기반으로 상호 작용하지 않고 백그라운드에서 사용자 동작을 확인합니다.<br/>**`Invisible reCAPTCHA v3`** - (권장) 상호 작용 점수를 기반으로 백그라운드에서 사용자 동작을 확인합니다. |
| [!UICONTROL Enable for Gift Card] | 웹 사이트 | ![Adobe Commerce](../../assets/adobe-logo.svg)(Adobe Commerce만 해당) 고객이 [기프트 카드](../../catalog/product-gift-card-create.md) 코드를 입력할 때 사용되는 reCAPTCHA 형식을 지정합니다. 옵션:<br/>**`No`**- (기본값) 기프트 카드 코드 제출의 유효성을 검사하지 않습니다.<br />**`reCAPTCHA v2 ("I am not a robot")`** - 사용자가 _로봇이 아닙니다_ 확인란을 선택해야 합니다.<br />**`Invisible reCAPTCHA v2`**- 점수를 기반으로 상호 작용하지 않고 배경에서 사용자 동작의 유효성을 검사합니다.<br/>**`Invisible reCAPTCHA v3`** - (권장) 상호 작용 점수를 기반으로 백그라운드에서 사용자 동작을 확인합니다. |
| [!UICONTROL Enable for Invitation Create Account] | 웹 사이트 | 고객이 계정 만들기 [초대](../../merchandising-promotions/invitations.md) 코드를 보낼 때 사용되는 reCAPTCHA 형식을 지정합니다. 옵션:<br/>**`No`**- (기본값) 초대 전자 메일 제출의 유효성을 검사하지 않습니다.<br />**`reCAPTCHA v2 ("I am not a robot")`** - 사용자가 _로봇이 아닙니다_ 확인란을 선택해야 합니다.<br />**`Invisible reCAPTCHA v2`**- 점수를 기반으로 상호 작용하지 않고 배경에서 사용자 동작의 유효성을 검사합니다.<br/>**`Invisible reCAPTCHA v3`** - (권장) 상호 작용 점수를 기반으로 백그라운드에서 사용자 동작을 확인합니다. |
| [!UICONTROL Enable for Send to Friend] | 웹 사이트 | 고객이 친구와 [제품을 공유](../../stores-purchase/email-a-friend.md)할 때 사용되는 reCAPTCHA 형식을 지정합니다. 옵션:<br/>**`No`**- (기본값) 전자 메일 제출의 유효성을 검사하지 않습니다.<br />**`reCAPTCHA v2 ("I am not a robot")`** - 사용자가 _로봇이 아닙니다_ 확인란을 선택해야 합니다.<br />**`Invisible reCAPTCHA v2`**- 점수를 기반으로 상호 작용하지 않고 백그라운드에서 사용자 동작을 확인합니다.<br/>**`Invisible reCAPTCHA v3`** - (권장) 상호 작용 점수를 기반으로 백그라운드에서 사용자 동작을 확인합니다. |
| [!UICONTROL Enable for Wishlist Sharing] | 웹 사이트 | 고객이 [위시리스트를 공유](../../stores-purchase/wishlist-storefront.md#share-the-wish-list)할 때 사용되는 reCAPTCHA 형식을 지정합니다. 옵션:<br/>**`No`**- (기본값) 메시지 및 전자 메일 제출의 유효성을 검사하지 않습니다.<br />**`reCAPTCHA v2 ("I am not a robot")`** - 사용자가 _로봇이 아닙니다_ 확인란을 선택해야 합니다.<br />**`Invisible reCAPTCHA v2`**- 점수를 기반으로 상호 작용하지 않고 배경에서 사용자 동작의 유효성을 검사합니다.<br/>**`Invisible reCAPTCHA v3`** - (권장) 상호 작용 점수를 기반으로 백그라운드에서 사용자 동작을 확인합니다. |
| [!UICONTROL Enable for Coupon Codes] | 웹 사이트 | 고객이 [쿠폰 코드](../../merchandising-promotions/price-rules-cart-coupon.md)를 입력할 때 사용되는 reCAPTCHA의 유형을 지정합니다. 옵션:<br/>**`No`**- (기본값) 쿠폰 코드 제출의 유효성을 검사하지 않습니다.<br />**`reCAPTCHA v2 ("I am not a robot")`** - 사용자가 _로봇이 아닙니다_ 확인란을 선택해야 합니다.<br />**`Invisible reCAPTCHA v2`**- 점수를 기반으로 상호 작용하지 않고 배경에서 사용자 동작의 유효성을 검사합니다.<br/>**`Invisible reCAPTCHA v3`** - (권장) 상호 작용 점수를 기반으로 백그라운드에서 사용자 동작을 확인합니다. |
| [!UICONTROL Enable for PayPal Payflow Pro payment form] | 웹 사이트 | 고객이 [PayPal Payflow Pro](../../stores-purchase/paypal-payflow-pro.md)을(를) 사용하여 구매 비용을 지불할 때 사용되는 reCAPTCHA 유형을 지정합니다. 옵션:<br/>**`No`**- (기본값) 암호 재설정 요청의 유효성을 검사하지 않습니다.<br />**`reCAPTCHA v2 ("I am not a robot")`** - 사용자가 _로봇이 아닙니다_ 확인란을 선택해야 합니다.<br />**`Invisible reCAPTCHA v2`**- 점수를 기반으로 상호 작용하지 않고 백그라운드에서 사용자 동작을 확인합니다.<br/>**`Invisible reCAPTCHA v3`** - (권장) 상호 작용 점수를 기반으로 백그라운드에서 사용자 동작을 확인합니다. |

{style="table-layout:auto"}
