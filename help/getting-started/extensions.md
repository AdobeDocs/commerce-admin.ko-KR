---
title: Adobe의 확장
description: Adobe에서 발표한 Adobe Commerce 및 Magento Open Source 확장에 대한 정보를 검토하십시오.
exl-id: 86338edc-c32a-41c8-9594-6aec26f53ac6
feature: Extensions
badgePaas: label="PaaS만" type="Informative" url="https://experienceleague.adobe.com/ko/docs/commerce/user-guides/product-solutions" tooltip="Adobe Commerce 온 클라우드 프로젝트(Adobe 관리 PaaS 인프라) 및 온프레미스 프로젝트에만 적용됩니다."
source-git-commit: 77e7eb00e9f8d5af6361059c287707993180c4c4
workflow-type: tm+mt
source-wordcount: '1357'
ht-degree: 0%

---

# Adobe의 확장

이 항목에서는 Adobe에서 출시한 Adobe Commerce 및 Magento Open Source용 PHP 확장에 대한 정보를 제공합니다.

확장은 기능, 기능, 서비스 및 통합을 Admin 및 Storefront에 추가합니다. 이러한 확장 중 일부는 Magento Open Source 커뮤니티 기여를 통해 개발됩니다. 일부 확장은 기본적으로 설치되고, 다른 확장은 별도의 설치가 필요합니다.

+++Adobe Commerce 확장에 대해 자세히 알아보기

Adobe은 Adobe Commerce 프로젝트를 확장하거나 사용자 정의할 수 있는 두 가지 기본 접근 방식을 제공합니다.

- In-process 확장성: PHP 확장과 같이 Adobe Commerce 애플리케이션 프로세스 내에서 실행되는 사용자 지정 코드 및 확장을 사용합니다. 이러한 기존 접근 방식은 심층적인 통합을 허용하지만 업그레이드 중에 신중한 관리가 필요합니다.

- 프로세스 외부 확장성: 핵심 소프트웨어와 독립적으로 작동하는 사용자 지정 코드 및 애플리케이션을 사용합니다. 이러한 최신 접근 방식은 다음을 통해 TCO를 절감하는 데 도움이 됩니다.

   - 확장이 코어에서 분리되므로 업그레이드 단순화
   - 개발자에게 구현 시간 및 방법에 대한 더 많은 제어 제공
   - 확장 구성 요소의 독립적인 확장 및 유지 관리 활성화

Adobe Commerce은 두 가지 유형의 확장성을 모두 지원하는 전략 및 도구를 제공합니다. 자세한 내용은 [Adobe Commerce 확장성](https://developer.adobe.com/commerce/extensibility/)을 참조하세요.

+++

## 기본적으로 설치된 Adobe 확장

다음 Adobe 확장은 Adobe Commerce에 포함되어 있으며 Adobe Commerce 애플리케이션과 함께 자동으로 설치됩니다. 일부 확장은 확장 설명에 나와 있는 대로 관리자에서 추가 구성 또는 활성화가 필요합니다.

### [!DNL Inventory Management]

[!DNL Commerce] [[!DNL Inventory Management]](../inventory-management/introduction.md)은(는) 동시 체크아웃 보호 및 배송 일치 알고리즘을 사용하여 하나 이상의 위치와 판매 채널에서 향상된 재고 및 배송 관리를 제공합니다. 재고 수량을 추적하고 고객에게 정확한 판매 가능 재고 금액을 제공하고 추천이나 수동 선택에 따라 출하하여 전체 재고를 관리합니다. 전역, 소스별 및 제품별로 관리 설정을 구성합니다.

>[!NOTE]
>
>이 확장은 커뮤니티 엔지니어링 프로그램을 통해 [[!DNL Inventory Management]](https://github.com/magento/inventory)&#x200B;(이전 MSI) 프로젝트의 일부로 개발되었습니다.

기본적으로 모든 기능이 활성화된 상태로 [!DNL Inventory Management]을(를) 설치합니다. 이러한 재고 기능을 활성화하는 데 추가 단계가 필요하지 않습니다. [!DNL Inventory Management] 기능에 대한 자세한 내용은 [[!DNL Inventory Management] 사용 안내서](../inventory-management/guide-overview.md)를 참조하십시오.

### Braintree

PayPal과 Gene Commerce은 Commerce 2.4.x 스토어의 공식 Braintree 확장 프로그램을 함께 개발했습니다. 전환을 유도하도록 설계된 향상된 체크아웃 경험을 제공하는 이 업데이트에는 쇼핑 중과 체크아웃 중에 소비자에게 관련 PayLater 메시지와 버튼을 자동으로 표시하는 PayLater 옵션이 포함됩니다.

이 확장은 기본적으로 설치되지만 저장소에 대해 사용하려면 관리자의 [Braintree 계정](https://www.braintreepayments.com/) 및 구성이 필요합니다. Braintree을 사용하여 트랜잭션을 처리할 때 적용되는 요금을 결정하려면 [Braintree 가격 책정](https://www.braintreepayments.com/braintree-pricing)을 확인하세요.

관리자의 Braintree 구성에 대한 자세한 내용은 _영업 및 구매 경험 안내서_&#x200B;의 [Braintree](../stores-purchase/braintree.md) 항목을 참조하십시오.

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
>관리자에 대해 Adobe Identity Management Services(IMS) 인증을 활성화한 Adobe Commerce 스토어의 경우 기본 Commerce 2FA가 비활성화됩니다. Adobe 자격 증명으로 관리자에 로그인한 사용자는 많은 관리 작업에 대해 다시 인증할 필요가 없습니다. Adobe IMS는 관리자 가 현재 세션에 로그인할 때 인증을 처리합니다. [Adobe IMS(Identity Management 서비스) 통합 개요](./adobe-ims-integration-overview.md)를 참조하세요.

## 설치가 필요한 Adobe 확장

Adobe에서는 Composer를 사용하여 별도로 설치해야 하는 추가 확장을 제공합니다. 이러한 확장은 다양한 채널을 통해 사용할 수 있습니다.

- 저장소 액세스(repo.magento.com)

  다음 확장을 설치하려면 계정 프로비저닝 및 자격 증명이 필요합니다. 도움이 필요하면 Adobe 계정 담당자에게 문의하십시오.

   - [Adobe Commerce](#adobe-commerce-b2b)
   - [Commerce용 AEM Assets 통합](#assets-integration-for-commerce)

- Adobe Commerce 마켓플레이스

  다음 Adobe 확장은 [marketplace.magento.com](https://marketplace.magento.com)에서 공개적으로 액세스할 수 있습니다. 이러한 확장 기능은 추가 비용 없이 사용할 수 있습니다.

   - [라이브 검색](#live-search)
   - [제품 추천](#product-recommendations)
   - [카탈로그 서비스](#catalog-service)
   - [결제 서비스](#payment-services)

### [!DNL Adobe Commerce B2B]

![Adobe Commerce](../assets/adobe-logo.svg) Adobe Commerce만, 별도의 라이선스가 필요합니다.

[!DNL Adobe Commerce B2B]은(는) 표준 Commerce 스토어를 포괄적인 B2B 플랫폼으로 변환하는 통합 확장입니다. 이를 통해 회사는 통합 회사 계정에서 여러 구매자, 사용자 정의 역할 및 구매 권한으로 복잡한 조직 구조를 관리할 수 있습니다. 주요 기능에는 회사별 카탈로그 및 가격 책정, 협상 가능한 견적, 구매 발주 관리, 구매요청 목록 및 빠른 주문 기능이 포함됩니다. 이 솔루션은 단일 인스턴스에서 B2B 및 B2C 모델을 모두 지원하므로 다양한 비즈니스 요구 사항에 유연하게 대처할 수 있습니다. 확장 프로그램은 별도의 라이센스가 필요하며 Adobe Commerce의 핵심 기능과 원활하게 통합되어 완벽한 B2B 전자 상거래 솔루션을 제공합니다.

프로비저닝은 Adobe 계정 담당자에게 문의하십시오. 구현 세부 정보 및 구성 단계는 [[!DNL B2B for Adobe Commerce] 사용 안내서](https://experienceleague.adobe.com/docs/commerce-admin/b2b/introduction.html?lang=ko)를 참조하십시오.

### [!DNL AEM Assets Integration for Commerce]

![Adobe Commerce](../assets/adobe-logo.svg) Adobe Commerce에만 사용되며 Adobe Experience Manager(AEM) Assets 및 AEM Dynamic Media에 대한 라이선스도 필요합니다.

[!DNL AEM Assets Integration for Commerce]은(는) Adobe Commerce을 Adobe Experience Manager의 DAM(디지털 자산 관리) 시스템과 연결하여 모든 디지털 자산을 중앙에서 제어할 수 있도록 합니다. 이 통합을 통해 상거래 상점 간 자동 에셋 동기화, 실시간 업데이트 및 효율적인 콘텐츠 재사용이 가능합니다. AEM의 강력한 에셋 관리 기능과 Commerce을 결합함으로써 기업은 클라우드 기반 인프라를 통해 간소화된 워크플로, 일관된 브랜드 경험, 최적화된 미디어 제공 등의 이점을 누릴 수 있습니다.

프로비저닝은 Adobe 계정 담당자에게 문의하십시오. 구현 세부 정보 및 구성 단계는 [[!DNL Assets Integration] 사용 안내서](../content-design/aem-assets-integration.md)를 참조하십시오.

### [!DNL Live Search]

![Adobe Commerce](../assets/adobe-logo.svg) Adobe Commerce 전용

라이브 서치는 AI가 제공하는 검색 솔루션에 &#39;검색할 때 바로 검색&#39; 기능을 실시간으로 제공하는 Adobe Commerce 전용 기능입니다. 쇼핑객이 입력하는 동안 제품 썸네일과 함께 쇼핑 행동에 따라 필터를 자동으로 조정하는 지능형 페이스팅으로 빠르고 관련성이 높은 결과를 제공합니다. 이 솔루션에는 제품 부양 및 매립을 위한 머천다이징 기능, 동의어 관리 및 검색 분석이 포함됩니다. 추가 비용 없이 Adobe Commerce에 포함된 [!DNL Live Search]은(는) 기본 검색 기능을 보다 정교한 SaaS 기반 검색 환경으로 대체합니다. 시작하려면 최소한의 구성이 필요합니다.

구현 세부 정보 및 기술 요구 사항은 [Live Search 사용 안내서](https://experienceleague.adobe.com/docs/commerce/live-search/overview.html?lang=ko)를 참조하십시오.

### [!DNL Product Recommendations]

![Adobe Commerce](../assets/adobe-logo.svg) Adobe Commerce 전용

[!DNL Product Recommendations]은(는) Adobe Sensei AI 기술을 기반으로 하는 Adobe Commerce 전용 기능으로, 고객 쇼핑 여정 전반에 개인화된 제품 제안을 제공합니다. 이 솔루션은 구매자 행동 및 제품 관계를 실시간으로 분석하여 관련 권장 사항을 자동으로 생성하며, 수동 머천다이징 규칙이 필요하지 않습니다. 이 AI 기반 접근 방식은 전환율과 매출 잠재력을 높이는 동시에 쇼핑객을 위한 보다 매력적인 제품 검색 경험을 만드는 데 도움이 됩니다.

구현 세부 정보 및 모범 사례는 [[!DNL Product Recommendations] 사용 안내서](https://experienceleague.adobe.com/docs/commerce/product-recommendations/overview.html?lang=ko)를 참조하세요.

### [!DNL Catalog Service]

[!BADGE 지원]{type=Informative tooltip="지원됨"} Adobe Commerce 및 Magento Open Source 설치

[!DNL Catalog Service]은(는) GraphQL 끝점을 통해 카탈로그 데이터에 최적화된 액세스를 제공하는 Adobe Commerce 및 Magento Open Source용 고성능 솔루션입니다. 제품 세부 사항 및 관련 정보에 대해 별도의 동기화된 데이터베이스를 유지 관리하므로 직접적인 애플리케이션 통신을 우회하여 보다 빠른 페이지 로드 시간을 제공합니다. 이 서비스는 특히 제품 세부 사항 페이지, 카테고리 목록 및 검색 결과 페이지에 유용하며, 따라서 기존 및 Headless 상거래 구현에 모두 적합합니다.

설치 지침 및 기술적인 세부 정보는 [[!DNL Catalog Service] 사용 안내서](https://experienceleague.adobe.com/docs/commerce/catalog-service/guide-overview.html?lang=ko)를 참조하십시오.

>[!NOTE]
>
>라이브 검색 또는 제품 권장 사항이 활성화되면 카탈로그 서비스가 자동으로 설치됩니다. 수동 설치는 필요하지 않습니다.

### [!DNL Payment Services]

[!BADGE 지원]{type=Informative tooltip="지원됨"} Adobe Commerce 및 Magento Open Source 설치

[!DNL Payment Services]은(는) 포괄적인 결제 처리 기능을 제공하는 Adobe Commerce 및 Magento Open Source 스토어를 위한 턴키 결제 솔루션입니다. 이 서비스는 보안 결제 게이트웨이 기능과 내장된 사기 방지 기능을 통합하는 동시에 신용/직불 카드, PayPal, Venmo(미국), PayLater 플랜을 비롯한 다양한 결제 옵션을 제공합니다. Commerce 관리 인터페이스를 통한 통합 거래 보고 및 주문 관리 기능이 있어 가맹점이 한 곳에서 결제 추적, 현금 흐름 관리, 금융 데이터 조정 등을 모두 손쉽게 할 수 있다.

자세한 구성 단계 및 결제 방법은 [[!DNL Payment Services] 사용 안내서](https://experienceleague.adobe.com/ko/docs/commerce/payment-services/overview)를 참조하세요.
