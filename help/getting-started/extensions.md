---
title: Adobe의 확장
description: Adobe에서 발표한 Adobe Commerce 및 Magento Open Source 확장에 대한 정보를 검토하십시오.
exl-id: 86338edc-c32a-41c8-9594-6aec26f53ac6
feature: Extensions
source-git-commit: 6414a7aea7dcbe0f2379ed74455518220a1fbd64
workflow-type: tm+mt
source-wordcount: '950'
ht-degree: 0%

---

# Adobe의 확장

이 항목에서는 Adobe에서 릴리스한 Adobe Commerce 및 Magento Open Source 확장에 대한 정보를 제공합니다. 확장은 기능, 기능, 서비스 및 통합을 Admin 및 Storefront에 추가합니다. 이러한 확장 중 일부는 Magento Open Source 커뮤니티 기여를 통해 개발됩니다. 일부 확장은 별도의 설치가 필요하며 다른 확장은 기본적으로 설치됩니다.

## 설치된 확장

Adobe Commerce 또는 Magento Open Source과 함께 자동으로 설치되는 몇 가지 확장이 있습니다.

### [!DNL Inventory Management]

[!DNL Commerce] [[!DNL Inventory Management]](../inventory-management/introduction.md)은(는) 동시 체크아웃 보호 및 배송 일치 알고리즘을 사용하여 하나 이상의 위치와 판매 채널에서 향상된 재고 및 배송 관리를 제공합니다. 재고 수량을 추적하고 고객에게 정확한 판매 가능 재고 금액을 제공하고 추천이나 수동 선택에 따라 출하하여 전체 재고를 관리합니다. 전역, 소스별 및 제품별로 관리 설정을 구성합니다.

>[!NOTE]
>
>이 확장은 커뮤니티 엔지니어링 프로그램을 통해 [[!DNL Inventory Management]](https://github.com/magento/inventory)(이전 MSI) 프로젝트의 일부로 개발되었습니다.

기본적으로 모든 기능이 활성화된 상태로 [!DNL Inventory Management]을(를) 설치합니다. 이러한 재고 기능을 활성화하는 데 추가 단계가 필요하지 않습니다. [!DNL Inventory Management] 기능에 대한 자세한 내용은 [[!DNL Inventory Management] 사용 안내서](../inventory-management/guide-overview.md)를 참조하십시오.

### Braintree

PayPal과 Gene Commerce은 Commerce 2.4.x 스토어의 공식 Braintree 확장 프로그램을 함께 개발했습니다. 전환을 유도하도록 설계된 향상된 체크아웃 경험을 제공하는 이 업데이트에는 쇼핑 중과 체크아웃 중에 소비자에게 관련 PayLater 메시지와 버튼을 자동으로 표시하는 PayLater 옵션이 포함됩니다.

이 확장은 기본적으로 설치되지만 저장소에 대해 사용하려면 관리자의 [Braintree 계정](https://www.braintreepayments.com/) 및 구성이 필요합니다. Braintree을 사용하여 트랜잭션을 처리할 때 적용되는 요금을 결정하려면 [Braintree 가격](https://www.braintreepayments.com/braintree-pricing)을 확인하세요.

관리자의 Braintree 구성에 대한 자세한 내용은 _판매 및 구매 경험 안내서_&#x200B;의 [Braintree](../stores-purchase/braintree.md) 항목을 참조하십시오.

### Google recaptcha

Google reCAPTCHA는 표준 CAPTCHA에서 사용할 수 있는 것보다 상점 및 관리자 UI에 더 높은 수준의 보안을 제공하며 다음과 같은 기능을 제공합니다.

- 고객이 계정을 만들거나 암호를 검색하거나, 계정에 로그인하거나, 회사에 문의할 때 확인합니다.
- 관리자 사용자가 로그인할 때 보안을 강화합니다.

이는 Captcha 코드를 입력할 때 발생할 수 있는 사용자 오류를 줄이고 체크아웃 중에 장애물을 추가하지 않고 장바구니 변환을 권장합니다. [보이지 않는 또는 대화형 검사를 사용하여 reCAPTCHA를 활성화 및 구성](../systems/security-google-recaptcha.md)하여 [!DNL Commerce] 관리 및 상점 앞에서의 보안 액세스를 향상시킵니다.

### 이중 인증

[!DNL Commerce] 관리자는 저장소, 주문 및 고객 데이터에 대한 모든 액세스 권한을 제공합니다. [2단계 인증](../systems/security-two-factor-authentication.md)(2FA 또는 TFA)은 모든 장치에서 [!DNL Commerce] 관리자에 액세스할 수 있도록 표준 로그인 이름과 암호 외에 추가 인증을 요구하여 보안을 향상시킵니다. 확장은 Google Authenticator, Authy, [!DNL Duo] 및 U2F 키를 비롯한 여러 인증자를 지원합니다. 이 인증은 관리자 사용자에게만 적용됩니다. 상점 고객 계정에는 제공되지 않습니다.

이러한 기능은 기본적으로 활성화되어 있습니다. 각 관리자는 지원되는 인증자 중 하나를 설치하고 구성해야 합니다.

>[!NOTE]
>
>관리자에 대해 Adobe Identity Management 서비스(IMS) 인증을 활성화한 Adobe Commerce 스토어에는 기본 Commerce 2FA가 비활성화되어 있습니다. Adobe 자격 증명으로 관리자에 로그인한 사용자는 많은 관리 작업에 대해 다시 인증할 필요가 없습니다. Adobe IMS는 관리자 가 현재 세션에 로그인할 때 인증을 처리합니다. [IMS(Identity Management 서비스) 통합 Adobe 개요](./adobe-ims-integration-overview.md)를 참조하십시오.

## 추가할 확장

[[!DNL Commerce Marketplace]](https://marketplace.magento.com/)은(는) 강력한 새 기능과 기능으로 [!DNL Commerce] 솔루션을 확장하는 응용 프로그램 및 서비스용 글로벌 전자 상거래 리소스입니다. Adobe은 향상된 통합 및 기능을 제공하기 위해 Adobe Commerce 또는 Magento Open Source 저장소 내에 설치 및 구성할 수 있는 [!DNL Marketplace]을(를) 통해 여러 확장을 릴리스합니다.

### [!DNL Live Search]

![Adobe Commerce](../assets/adobe-logo.svg) Adobe Commerce 전용

[!DNL Live Search] 확장은 스토어를 Adobe Commerce의 무료 검색 플랫폼인 라이브 검색 서비스에 연결합니다. 라이브 검색 서비스는 판매자가 AI 강화 검색 경험을 제공할 수 있도록 원활하게 권한을 부여합니다. Adobe의 인공 지능으로 구축된 Adobe Sensei, 지능형 페이스팅은 페이스팅/필터링 관련 수동 작업을 제거하여 판매자가 적은 비용으로 더 많은 작업을 수행할 수 있도록 지원합니다.

자세한 내용은 [실시간 검색 사용 안내서](https://experienceleague.adobe.com/docs/commerce-merchant-services/live-search/guide-overview.html)를 참조하십시오.

### [!DNL Product Recommendations]

![Adobe Commerce](../assets/adobe-logo.svg) Adobe Commerce 전용

[!DNL Product Recommendations] 확장은 전환, 매출 및 참여를 늘리는 데 사용할 수 있는 강력한 마케팅 도구인 Product Recommendations 서비스에 스토어를 연결합니다. [!DNL Product Recommendations]은(는) Adobe Commerce에서 빌드되었으며 전투에서 테스트한 인공 지능인 Adobe Sensei에 의해 구동되므로 사용자가 참여와 전환을 자신 있게 추진할 수 있습니다. 이 기능은 모든 구매자에게 관련 제품을 추천하기 위해 필요한 수동 작업을 제거합니다.

자세한 내용은 [[!DNL Product Recommendations] 사용 안내서](https://experienceleague.adobe.com/docs/commerce-merchant-services/product-recommendations/guide-overview.html?lang=en)를 참조하세요.

### [!DNL Catalog Service]

[!DNL Catalog Service]을(를) 사용하면 성능을 향상시키고, 확장성을 개선하고, 전환을 늘리는 동시에 고객에게 최적화된 제품 경험을 제공할 수 있습니다. 자세한 내용은 [[!DNL Catalog Service] 사용 안내서](https://experienceleague.adobe.com/docs/commerce-merchant-services/catalog-service/guide-overview.html)를 참조하세요.

### [!DNL Payment Services]

Adobe Commerce 및 Magento Open Source용 [!DNL Payment services]은(는) 결제 관리 프로세스를 간소화하고 고객에게 결제 방법을 제공할 수 있는 완전히 통합된 결제 솔루션입니다. Adobe Commerce 관리자 내에서 모든 결제 및 거래 데이터를 안전하게 조정 - 원활한 체크아웃을 제공하면서 주문과 결제를 한 곳에서 관리할 수 있습니다. 자세한 내용은 [[!DNL Payment Services] 사용 안내서](https://experienceleague.adobe.com/docs/commerce-merchant-services/payment-services/guide-overview.html)를 참조하세요.

### [!DNL Store Fulfillment]

Adobe Commerce 및 Magento Open Source을 위한 스토어 이행 기능을 통해 우수한 온라인 구매, 매장 픽업(BOPIS) 고객 경험을 제공할 수 있으며, 모바일 디바이스를 통해 구현되는 포괄적인 이행 워크플로를 제공하여 직원의 생산성을 극대화합니다. 자세한 내용은 [[!DNL Store Fulfillment] 사용 안내서](https://experienceleague.adobe.com/docs/commerce-merchant-services/store-fulfillment/guide-overview.html)를 참조하세요.

### [!DNL Amazon Sales Channel]

Adobe Commerce용 [!DNL Amazon Sales Channel]을(를) 사용하면 Amazon Seller Central 목록 데이터베이스를 [!DNL Commerce] 제품 카탈로그와 통합하고 Commerce 관리에서 Amazon 목록 및 판매를 관리할 수 있습니다. 자세한 내용은 [[!DNL Amazon Sales] 안내서 사용 안내서](https://experienceleague.adobe.com/docs/commerce-channels/amazon/guide-overview.html)를 참조하세요.

### [!DNL Channel Manager]

[!DNL Channel Manager]을(를) 사용하면 Adobe Commerce 또는 Magento Open Source 제품 카탈로그를 Walmart Marketplace와 통합하여 매출을 늘리고, 신규 고객에게 도달하고, 운영을 간소화하고, 시간을 절약할 수 있습니다. 확장을 설치하고 구성한 후 직원은 [!DNL Commerce Admin]에서 Walmart Marketplace 목록, 재고, 주문, 반품 및 환불을 원활하게 관리할 수 있습니다. 자세한 내용은 [[!DNL Channel Manager] 사용 안내서](https://experienceleague.adobe.com/docs/commerce-channels/channel-manager/guide-overview.html)를 참조하세요.
