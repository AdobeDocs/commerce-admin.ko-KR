---
title: 쿠키 법률 준수
description: 많은 국가에서 쿠키의 사용에 관한 법률에 발맞추기 위해 Adobe Commerce 및 Magento Open Source은 상인에게 고객 동의를 얻는 방법을 선택합니다.
exl-id: 42df20cd-50a7-4618-98fd-9ced936e305b
feature: Compliance
source-git-commit: ae43d97bb3031a06ce6a0211ee304aae53e4eb08
workflow-type: tm+mt
source-wordcount: '2105'
ht-degree: 0%

---

# 쿠키 법률 준수

쿠키는 사이트를 방문하는 각 방문자의 컴퓨터에 저장되고 정보를 위한 임시 저장 위치로 사용되는 작은 파일입니다. 쿠키에 저장된 정보는 쇼핑 경험을 개인화하고, 방문자를 장바구니에 연결하며, 트래픽 패턴을 측정하고, 프로모션의 효과를 개선하는 데 사용됩니다. 많은 국가에서 쿠키의 사용에 관한 법률에 발맞추기 위해 Adobe Commerce 및 Magento Open Source은 상인에게 고객 동의를 얻는 방법을 선택합니다. Adobe Commerce 및 Magento Open Source의 기본 쿠키 목록은 [쿠키 참조](#default-cookies)를 참조하십시오.

>[!NOTE]
>
>[일반 데이터 보호 규정](compliance-gdpr.md)을 준수하도록 기본 [Google 개인 정보 보호 설정](../merchandising-promotions/google-tools.md#google-privacy-settings)을(를) 수정하는 경우 Google Analytics 쿠키 사용에 대한 사용자 동의를 얻을 필요가 없습니다.

## 방법 1: 묵시적 동의

묵시적 동의는 스토어 방문자가 쿠키가 작업의 필수 부분이라는 점을 명확히 이해하고 있으며, 사이트를 사용함으로써 쿠키의 사용 권한을 간접적으로 부여했음을 의미합니다. 묵시적인 동의를 얻는 비결은 방문자가 정보에 입각한 결정을 내릴 수 있도록 충분한 정보를 제공하는 것입니다. 많은 스토어가 모든 표준 페이지의 맨 위에 메시지를 표시하며, 이 메시지는 스토어의 개인정보 처리방침에 대한 링크와 함께 쿠키 사용 방법에 대한 간단한 개요를 제공합니다. 개인정보 처리방침은 스토어에서 수집하는 정보의 유형과 정보 사용 방법을 설명해야 합니다.

## 방법 2: 표현된 동의

_쿠키 제한 모드_&#x200B;에서 스토어를 운영하려면 방문자가 쿠키를 컴퓨터에 저장하기 전에 동의를 표시해야 합니다. 동의가 부여되지 않는 한 스토어의 많은 기능을 사용할 수 없습니다. 예를 들어 스토어에서 Google Analytics을 사용할 수 있는 경우 방문자가 쿠키를 사용할 수 있는 권한을 부여한 후에만 이 쿠키를 호출할 수 있습니다.

## 쿠키 제한 모드

쿠키 제한 모드가 활성화되면 스토어 방문자는 모든 기능을 갖춘 작업에 쿠키가 필요하다는 알림을 받게 됩니다. 테마에 따라 메시지가 머리글 위, 바닥글 아래 또는 페이지의 다른 곳에 표시될 수 있습니다. 이 메시지는 자세한 내용을 보기 위해 개인정보 처리방침으로 연결되며, 방문자가 허용 단추를 클릭하여 동의할 것을 권장합니다. 동의가 부여되면 메시지가 사라집니다.

[개인정보 처리방침](privacy-policy.md))에 상점 이름과 연락처 정보를 포함하고, 상점에서 사용하는 각 쿠키의 용도를 설명해야 합니다. 자세한 내용은 [쿠키 참조](#default-cookies)를 참조하세요.

>[!NOTE]
>
>개인정보 처리방침의 URL 키를 변경하는 경우, 사용자 지정 URL 재작성도 만들어 트래픽을 새 URL 키로 리디렉션해야 합니다. 그렇지 않으면 쿠키 제한 모드 메시지의 링크가 `404 Page Not Found`을(를) 반환합니다.

![Example storefront - 쿠키 제한 알림](./assets/storefront-cookie-restriction-message.png){width="600"}

### 1단계: 쿠키 제한 모드 활성화

1. _관리자_ 사이드바에서 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**(으)로 이동합니다.

1. **[!UICONTROL General]** 아래의 왼쪽 탐색 패널에서 **[!UICONTROL Web]**&#x200B;을(를) 선택합니다.

1. **[!UICONTROL Default Cookie Settings]** 섹션을 확장하고 다음을 수행합니다.

   ![웹 구성 - 기본 쿠키 설정](./assets/web-default-cookie-settings.png){width="600"}

   - **[!UICONTROL Cookie Lifetime]**&#x200B;을(를) 초 단위로 입력하십시오.

   - 쿠키를 다른 폴더에서 사용할 수 있도록 하려면 **[!UICONTROL Cookie Path]**&#x200B;을(를) 입력하십시오. 사이트의 어디에서나 쿠키를 사용할 수 있도록 하려면 슬래시(`/`)를 입력하십시오. 이 값은 쿠키 경로만 포함할 수 있으며 **_cannot_**&#x200B;에는 다른 쿠키 매개 변수가 포함될 수 없습니다.

   - 하위 도메인에서 쿠키를 사용할 수 있도록 하려면 **[!UICONTROL Cookie Domain]** 필드(`subdomain.yourdomain.com`)에 하위 도메인 이름을 입력하십시오. 모든 하위 도메인에서 쿠키를 사용할 수 있도록 하려면 도메인 이름 앞에 마침표(`.yourdomain.com`)를 입력하십시오. 이 값은 쿠키 도메인만 포함할 수 있으며 **_cannot_**&#x200B;에는 다른 쿠키 매개 변수가 포함될 수 없습니다.

   - JavaScript과 같은 스크립팅 언어가 쿠키에 액세스하지 못하도록 하려면 **HTTP만 사용**&#x200B;이 `Yes`(으)로 설정되어 있는지 확인하십시오.

   - **[!UICONTROL Cookie Restriction Mode]**&#x200B;을(를) `Yes`(으)로 설정합니다.

     필요한 경우 확인란의 선택을 취소하고 **[!UICONTROL OK]**&#x200B;을(를) 클릭하여 범위 전환을 확인합니다.

1. 완료되면 **[!UICONTROL Save Config]**&#x200B;을(를) 클릭합니다.

1. 캐시를 업데이트하라는 메시지가 표시되면 시스템 메시지에서 **[!UICONTROL Cache Management]** 링크를 클릭합니다. 그런 다음 각 잘못된 캐시를 새로 고칩니다.

### 2단계: 개인정보 처리방침 업데이트

회사에서 수집하는 정보와 사용 방법을 반영하도록 [개인정보 처리방침](privacy-policy.md)을 업데이트하세요.

## 기본 쿠키

Adobe Commerce 및 Magento Open Source의 기본 쿠키는 판매자가 [GDPR](compliance-gdpr.md)과 같은 개인 정보 보호 규정의 요구 사항을 충족하는 데 도움이 되도록 제외/비제외로 분류됩니다. 판매자는 이 정보를 지침으로 사용하고 포괄적인 개인 정보 보호 규정 준수 전략의 일환으로 개인 정보 보호 및 쿠키 정책을 업데이트하기 위해 법률 고문과 상담해야 합니다.

[!DNL Commerce]이(가) 온-프레미스 및 클라우드 설치를 위해 &quot;즉시 사용 가능한&quot; 쿠키를 사용합니다. 이러한 쿠키는 고객이 명시적으로 요청한 기능에 필요할 수 있습니다. 세션 쿠키의 수명에 대해 알아보려면 [세션 수명](../customers/customer-online-options.md)을 참조하세요.

이러한 쿠키 중 일부는 필요에 따라 활성화/비활성화를 포함한 구성 옵션을 제공할 수 있습니다.

### 요청된 기능 쿠키(예외)


#### `add_to_cart`

Google 태그 관리자에서 사용하는 ![Adobe Commerce](../assets/adobe-logo.svg)(Adobe Commerce 전용). 장바구니에서 제거된 제품 SKU, 이름, 가격 및 수량을 캡처하고 정보를 서드파티 스크립트로 향후 통합할 수 있도록 합니다.

#### `guest-view`

고객 구매자가 주문 상태를 검색하는 데 사용하는 주문 ID를 저장합니다. 게스트 주문 보기. _[!DNL Orders and Returns]_위젯에서 사용됩니다.

- 안전합니까? 아니요
- HTTP만 해당: 예
- 만료 정책: 세션
- 모듈: `Magento_Sales`

#### `login_redirect`

고객이 로그인으로 이동되기 전에 로드되었던 대상 페이지를 유지합니다. [미니 장바구니 표시](../stores-purchase/cart-configuration.md#mini-cart) 구성 옵션이 `Yes`(으)로 설정된 경우 로그인 고객의 미니 장바구니에서 로그인 리디렉션이 사용됩니다.

- 안전합니까? 아니요
- HTTP만 해당: 아니요
- 만료 정책: 세션
- 모듈: `Magento_Customer`

#### `mage-banners-cache-storage`

![Adobe Commerce](../assets/adobe-logo.svg)(Adobe Commerce만 해당) 배너 콘텐츠를 로컬에 저장하여 성능을 개선합니다.

#### `mage-messages`

쿠키 동의 메시지 및 다양한 오류 메시지와 같이 사용자에게 표시되는 오류 메시지 및 기타 알림을 추적합니다. 메시지가 쇼핑객에게 표시된 후 쿠키에서 삭제됩니다.

이 쿠키를 비활성화하는 옵션은 없습니다.

- 안전합니까? 아니요
- HTTP만 해당: 아니요
- 만료 정책: 기간 1년. 메시지가 사용자에게 표시되면 프론트엔드에서 지워집니다.
- 모듈: `Magento_Theme`

#### `mage-translation-storage`(로컬 저장소)

쇼핑객이 요청할 때 번역된 콘텐츠를 저장합니다. [번역 전략](../configuration-reference/advanced/developer.md)이(가) &quot;사전(상점 쪽의 번역)&quot;으로 구성된 경우 사용됩니다.

- 안전합니까? 아니요
- HTTP만 해당: 아니요
- 만료 정책: 로컬 저장소 규칙당
- 모듈: `Magento_Translation`

#### `mage-translation-file-version`(로컬 저장소)

로컬 저장소에서 번역 버전을 추적합니다. [번역 전략](../configuration-reference/advanced/developer.md)이(가) `Dictionary (Translation on Storefront side)`(으)로 구성된 경우 사용됩니다.

- 안전합니까? 아니요
- HTTP만 해당: 아니요
- 만료 정책: 로컬 저장소 규칙당
- 모듈: `Magento_Translation`

#### `product_data_storage`(로컬 저장소)

최근에 본/비교한 제품과 관련된 제품 데이터에 대한 구성을 저장합니다.

- 안전합니까? 아니요
- HTTP만 해당: 아니요
- 만료 정책: 로컬 저장소 규칙당
- 모듈: `Magento_Catalog`

#### `recently_compared_product`(로컬 저장소)

최근에 비교한 제품의 제품 ID를 저장합니다.

- 안전합니까? 아니요
- HTTP만 해당: 아니요
- 만료 정책: 로컬 저장소 규칙당
- 모듈: `Magento_Catalog`

#### `recently_compared_product_previous`(로컬 저장소)

쉽게 탐색할 수 있도록 이전에 비교한 제품의 제품 ID를 저장합니다.

- 안전합니까? 아니요
- HTTP만 해당: 아니요
- 만료 정책: 로컬 저장소 규칙당
- 모듈: `Magento_Catalog`

#### `recently_viewed_product`(로컬 저장소)

쉽게 탐색할 수 있도록 최근에 본 제품의 제품 ID를 저장합니다.

- 안전합니까? 아니요
- HTTP만 해당: 아니요
- 만료 정책: 로컬 저장소 규칙당
- 모듈: `Magento_Catalog`

#### `recently_viewed_product_previous`(로컬 저장소)

쉽게 탐색할 수 있도록 최근에 본 제품의 제품 ID를 저장합니다.

- 안전합니까? 아니요
- HTTP만 해당: 아니요
- 만료 정책: 로컬 저장소 규칙당
- 모듈: `Magento_Catalog`

#### `remove_from_cart`

[Adobe Commerce 태그 관리자](../merchandising-promotions/google-tag-manager.md)에서 사용하는 ![Google](../assets/adobe-logo.svg)(Adobe Commerce만 해당). 제품 SKU, 이름, 가격 및 장바구니에 추가된 수량을 캡처하고 정보를 서드파티 스크립트로 향후 통합할 수 있도록 합니다.

#### `stf`

SendFriend([친구에게 이메일 보내기](../stores-purchase/email-a-friend.md)) 모듈에서 메시지를 보내는 시간을 기록합니다.

- 안전합니까? 예
- HTTP만 해당: 예
- 만료 정책: 세션
- 모듈: `Magento_SendFriend`

#### `X-Magento-Vary`

Vannish 정적 콘텐츠 캐싱을 사용할 때 성능을 개선하는 구성 설정입니다.

- 안전합니까? 예
- HTTP만 해당: 예
- 만료 정책: PHP 설정 session.cookie_lifetime 기반
- 모듈: `Magento_PageCache`

#### `form_key`

CSRF(크로스 사이트 요청 위조)로부터 데이터를 보호하기 위해 모든 양식 제출에 무작위 문자열을 추가하는 보안 조치입니다.

- 안전합니까? 아니요
- HTTP만 해당: 아니요
- 만료 정책:
   - PHP: PHP 설정 session.cookie_lifetime
   - JS: 세션
- 모듈: 페이지 캐시

#### `mage-cache-sessid`

이 쿠키의 값은 로컬 캐시 저장소 정리를 트리거합니다. 백엔드 응용 프로그램에서 쿠키를 제거하면 관리자가 로컬 저장소를 정리하고 쿠키 값을 `true`(으)로 설정합니다.

- 안전합니까? 아니요
- HTTP만 해당: 아니요
- 만료 정책: 세션
- 모듈: `Magento_Customer`

#### `mage-cache-storage`

전자 상거래 기능을 활성화하는 방문자별 콘텐츠의 로컬 저장소입니다.

- 안전합니까? 아니요
- HTTP만 해당: 아니요
- 만료 정책: 세션
- 모듈: `Magento_Customer`, `Magento_Persistent`

#### `mage-cache-storage`(로컬 저장소)

전자 상거래 기능을 활성화하는 방문자별 콘텐츠의 로컬 저장소입니다.

- 안전합니까? 아니요
- HTTP만 해당: 아니요
- 만료 정책: 세션
- 모듈: `Magento_Customer`, `Magento_Persistent`, `Magento_NegotiableQuote`

#### `mage-cache-storage-section-invalidation`(로컬 저장소)

무효화해야 하는 특정 콘텐츠 섹션의 로컬 저장소를 강제 적용합니다.

- 안전합니까? 아니요
- HTTP만 해당: 아니요
- 만료 정책: 로컬 저장소당
- 모듈: `Magento_Customer`

#### `persistent_shopping_cart`

영구 장바구니의 키(ID)를 저장하여 익명 쇼핑객을 위해 장바구니를 복원할 수 있도록 합니다.

- 안전합니까? 예
- HTTP만 해당: 예
- 만료 정책: [지속적인 장바구니](../stores-purchase/cart-persistent.md) - 지속성 수명(초) 구성을 기반으로 합니다.
- 모듈: `Magento_Persistent`

#### `private_content_version`

고객 콘텐츠가 있는 페이지에 임의의 고유 번호 및 시간을 추가하여 서버에서 캐시되지 않도록 합니다.

이 변수는 PHP에서 JavaScript as a cookie로 JavaScript에서 로컬 저장소로 설정됩니다.

HTTP Only=`Yes`(요청 기반)의 경우 쿠키가 HTTPS 요청 중에 설정된 경우 안전하며 HTTP 요청 중에 설정된 경우 안전하지 않음을 의미합니다.

- 안전합니까? `Yes`(요청 기준), `No`
- HTTP만 해당: `No`
- 만료 정책: [지속적인 장바구니](../stores-purchase/cart-persistent.md) - 지속성 수명(초) 구성을 기반으로 합니다.
   - PHP: `1`년 / `315360000s`년(10년)
   - JS: `1`일
   - JS 로컬 저장소: 로컬 저장소 규칙별(영구적)
- 모듈: `Magento_PageCache`, `Magento_Customer`

#### `section_data_ids`

위시리스트 표시 및 체크아웃 정보와 같이 고객이 시작한 작업과 관련된 고객별 정보를 저장합니다.

- 안전합니까? `No`
- HTTP만 해당: `No`
- 만료 정책: `Session`
- 모듈: `Magento_Customer`

#### `store`

쇼핑객이 선택한 특정 매장 보기/로케일을 추적합니다.

- 안전합니까? `No`
- HTTP만 해당: `Yes`
- 만료 정책: `1`년
- 모듈: `Magento_Store`

#### `mage-banners-cache-storage` - 로컬 저장소

배너 기능을 위한 ![Adobe Commerce](../assets/adobe-logo.svg)(Adobe Commerce 전용) 로컬 저장소입니다.

- 안전합니까? `No`
- HTTP만 해당: `No`
- 만료 정책: 로컬 저장소 규칙당
- 모듈: `Magento_Banner`

## Google Analytics 쿠키

다음 쿠키는 [Google Analytics](../merchandising-promotions/google-analytics.md) 또는 Google Universal Analytics가 설치에 대해 완전히 활성화된 경우 사용됩니다. 개인 정보 보호 규정 준수를 위해 이러한 쿠키를 사용하지 않도록 설정하려면 [Google 개인 정보 보호 설정](../merchandising-promotions/google-tools.md#google-privacy-settings)을 참조하세요. 자세한 내용은 [웹 사이트의 Google Analytics 쿠키 사용][1]을 참조하세요.

### Google Universal Analytics 쿠키 - 비면제

![Adobe Commerce](../assets/adobe-logo.svg)(Adobe Commerce만 해당) JavaScript 라이브러리: `gtag.js` 및 `analytics.js`

- `_ga`: 사이트 방문자를 구별합니다.
- `_gid`: 사이트 방문자를 구별합니다.
- `gat`: 요청 속도를 조절하는 데 사용됩니다.
- `dc_gtm_<property-id>`: [Google 태그 관리자](../merchandising-promotions/google-tag-manager.md)를 사용하여 Google Analytics을 배포할 때 요청 속도를 조절합니다.
- `AMP_TOKEN`: AMP 클라이언트 ID 서비스에서 클라이언트 ID를 검색하는 데 사용할 수 있는 토큰을 포함합니다. 다른 가능한 값에는 옵트아웃, inflight 요청 또는 AMP 클라이언트 ID 서비스에서 클라이언트 ID를 검색하는 도중 오류가 발생했습니다.
- `_gac_<property-id>`: 사용자에 대한 캠페인 관련 정보가 포함되어 있습니다. Google Analytics이 [AdWords][2] 계정에 연결되어 있는 경우 Google AdWords 변환 태그가 이 쿠키를 읽습니다.

### Google Analytics 쿠키 - 비면제

![Adobe Commerce](../assets/adobe-logo.svg)(Adobe Commerce 전용) JavaScript 라이브러리: `ga.js`

- `__utma`: 쇼핑객과 세션을 구별합니다. 이 쿠키는 JavaScript 라이브러리가 실행되고 기존 `__utma` 쿠키가 없을 때 만들어집니다. 쿠키는 데이터가 Google Analytics에게 전송될 때마다 업데이트됩니다.
- `__utmt`: 요청 속도를 조절하는 데 사용됩니다.
- `__utmb`: 새 세션/방문을 결정합니다. 이 쿠키는 JavaScript 라이브러리가 실행되고 기존 `__utmb` 쿠키가 없을 때 만들어집니다. 쿠키는 데이터가 Google Analytics에게 전송될 때마다 업데이트됩니다.
- `_utmz`: 쇼핑객이 사이트에 도달한 방법을 설명하는 트래픽 소스 또는 캠페인을 저장합니다. 쿠키는 JavaScript 라이브러리가 실행될 때 생성되며 데이터가 Google Analytics에게 전송될 때마다 업데이트됩니다.
- `__utmv`: 방문자 수준 사용자 지정 변수 데이터를 저장합니다. 이 쿠키는 개발자가 방문자 수준 사용자 지정 변수와 함께 `_setCustomVar` 메서드를 사용할 때 만들어집니다. 이 쿠키는 데이터가 Google Analytics에게 전송될 때마다 업데이트됩니다.

## 제품 Recommendations 쿠키

![Adobe Commerce](../assets/adobe-logo.svg)(Adobe Commerce만 해당) Adobe Commerce 고객을 위한 제품 Recommendations에서 다음 쿠키를 사용합니다. 이 쿠키는 [DataServices 모듈](https://experienceleague.adobe.com/docs/commerce-merchant-services/product-recommendations/getting-started/install-configure.html)과 함께 설치됩니다.

- `mg_dnt`: 사이트에서 쿠키 동의를 관리할 사용자 지정 코드가 있는 경우 [Adobe Commerce 데이터 수집을 제한](https://experienceleague.adobe.com/docs/commerce-merchant-services/product-recommendations/developer/setting-cookie.html)할 수 있습니다.
- `user_allowed_save_cookie`: [쿠키 제한 모드](#cookie-restriction-mode)에 사용됩니다.
- `authentication_flag`: 쇼핑객이 로그인했는지 또는 로그아웃했는지 여부를 나타냅니다. 이 쿠키는 `dataservices_customer_id` 쿠키와 동시에 업데이트됩니다.
- `dataservices_customer_id`: 쇼핑객이 로그인했는지 또는 로그아웃했는지 여부를 나타냅니다. 이 쿠키에는 시스템에 있는 고객의 고유 ID가 포함되어 있습니다.
- `dataservices_customer_group`: 고객의 그룹을 나타냅니다. 이 쿠키는 고객 그룹 ID의 [sha1](https://en.wikipedia.org/wiki/SHA-1) 체크섬으로 저장됩니다.
- `dataservices_cart_id`: 쇼핑객의 장바구니 작업을 식별합니다. 이 쿠키에는 시스템에 있는 고객의 고유한 장바구니 ID가 포함되어 있습니다.
- `dataservices_product_context`: 구매자의 제품 상호 작용을 식별합니다. 이 쿠키에는 시스템에 있는 고객의 고유한 견적 ID가 포함되어 있습니다.

## 추가 쿠키

![Adobe Commerce](../assets/adobe-logo.svg)(Adobe Commerce만 해당) Adobe Commerce 고객에 대해 다음 쿠키가 설정됩니다. 이 쿠키는 [DataServices 모듈](https://experienceleague.adobe.com/docs/commerce-merchant-services/product-recommendations/getting-started/install-configure.html)과 함께 설치됩니다.

- `mg`: Snowploy JavaScript 추적기에서 설정합니다. 자세한 내용은 [Snowploy 설명서](https://docs.snowplow.io/docs/collecting-data/collecting-from-own-applications/javascript-trackers/javascript-tracker/javascript-tracker-v3/tracker-setup/initialization-options)에서 확인할 수 있습니다.
- `com.adobe.alloy.getTld`: 현재 웹 페이지의 호스트 이름을 고려할 때 이 도메인은 https://publicsuffix.org에 설명된 &quot;공용 접미사&quot;가 아닌 최상위 도메인입니다. 기본적으로 이 도메인은 쿠키를 허용할 수 있는 가장 상위 도메인입니다. 이 쿠키는 [Alloy Web SDK](https://github.com/adobe/alloy)의 일부입니다.

[1]: https://developers.google.com/analytics/devguides/collection/analyticsjs/cookie-usage
[2]: https://support.google.com/adwords/answer/7521212
