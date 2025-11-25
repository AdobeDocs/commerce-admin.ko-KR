---
title: 결제 개요
description: Adobe Commerce 및 Magento Open Source에서 기본적으로 지원되는 결제 방법 및 서비스에 대해 알아봅니다.
exl-id: 474bf6df-96e2-4db3-ad3c-1804b5de33b0
feature: Payments
source-git-commit: 15118877bb8cc533b2323819db34da0513899e25
workflow-type: tm+mt
source-wordcount: '753'
ht-degree: 0%

---

# 결제 개요

Adobe Commerce과 Magento Open Source은 매우 다양한 결제 방법 및 서비스를 지원합니다. 여기에는 수표나 금전주문에 의한 결제, COD(Cash on Delivery)를 비롯한 여러 오프라인 결제 방식이 포함된다. 또한 공급업체가 개발한 번들 확장으로 Braintree을 포함하여 수많은 온라인 결제 솔루션 및 게이트웨이에 대한 기본 통합이 있습니다.

>[!TIP]
>
>Adobe Commerce 및 Magento Open Source용 결제 서비스는 강력하고 안전한 결제 처리를 위해 샌드박스 테스트 및 간단한 설정을 포함한 턴키 셀프 서비스 솔루션을 제공합니다. 이 강력한 도구 집합에 대해 자세히 알아보고 구매자에게 최상의 경험을 제공하기 위해 필요한 insight 및 제어 기능을 제공하는 방법에 대해 알아보려면 [결제 서비스 사용 안내서](https://experienceleague.adobe.com/docs/commerce/payment-services/guide-overview.html)를 참조하세요. [Adobe Commerce as a Cloud Service](https://experienceleague.adobe.com/en/docs/commerce/cloud-service/overview)의 기본 결제 솔루션입니다.

>[!NOTE]
>
>인터넷을 통해 신용 카드로 결제하는 비즈니스의 경우 PCI(결제 카드 업계)에서 설정한 요구 사항을 요약한 [PCI 준수 지침](../getting-started/compliance-pci.md)을 검토하십시오.

## 2.4의 변경 사항

[!BADGE PaaS만]{type=Informative url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="Adobe Commerce 온 클라우드 프로젝트(Adobe 관리 PaaS 인프라) 및 온프레미스 프로젝트에만 적용됩니다."}

일부 결제 통합 및 번들 확장은 2.4.x 릴리스에서 제거되고 Commerce Marketplace으로 이동되었습니다. [Commerce Marketplace](https://marketplace.magento.com/extensions/payments-security.html){:target="_blank"}에서 최신 공식 결제 통합 확장을 찾을 수 있습니다.

- **Amazon Pay** 및 **Klarna**: Adobe Commerce 및 Magento Open Source 릴리스 2.4.0 - 2.4.3에는 이러한 공급업체에서 개발한 확장이 포함되어 있습니다. 2.4.4 릴리스부터 이러한 확장은 더 이상 핵심 릴리스와 번들로 제공되지 않으며 Commerce Marketplace에서 설치하고 업데이트해야 합니다. Marketplace에서는 확장 개발자가 제공하는 현재 설명서에 대한 액세스도 제공합니다.

  이러한 번들형 확장 기능 중 하나를 활성화하고 구성한 경우 2.4.4 업그레이드 프로세스의 일부로 composer.json 파일을 업데이트하고 확장 업데이트를 앞으로 관리해야 합니다. 자세한 내용은 [업그레이드 안내서](https://experienceleague.adobe.com/docs/commerce-operations/upgrade-guide/modules/upgrade.html)의 _업그레이드 모듈_&#x200B;을 참조하십시오.

- **Worldpay**, **Eway**, **CyberSource** 및 **Authorize.Net**: 이러한 결제 통합에서 안전하게 전환하는 방법에 대한 자세한 내용은 [DevBlog](https://community.magento.com/t5/Magento-DevBlog/Deprecation-of-Magento-core-payment-integrations/ba-p/426445){:target="_blank"}를 참조하십시오.

## 오프라인 결제 방법

Adobe Commerce 및 Magento Open Source에는 서드파티 결제 처리 회사의 서비스가 필요 없는 몇 가지 내장된 오프라인 결제 방법이 포함되어 있습니다.

- [제로 소계 체크아웃](zero-subtotal-checkout.md)
- [게재 시 현금 결제](cash-on-delivery.md)
- [은행 송금 결제](bank-transfer.md)
- [수표/우편환](check-money-order.md)
- [구매 주문](purchase-order.md)
- [계정에서 결제](../b2b/enable-basic-features.md#configure-payment-on-account) ![Adobe Commerce B2B](../assets/b2b.svg)(Adobe Commerce B2B에서 사용 가능)

## 온라인 결제 방법

Adobe Commerce과 Magento Open Source은 전 세계 모든 지역에서 판매자 서비스를 제공하는 다양한 결제 솔루션을 지원합니다. 다른 사이트로 제어권을 넘겨 거래를 완료하는 결제 솔루션과 달리 결제 게이트웨이를 사용하면 고객이 사이트를 떠나지 않고도 매장에서 직접 신용카드 결제를 받을 수 있습니다.

### 권장 솔루션

- [결제 서비스](https://experienceleague.adobe.com/docs/commerce/payment-services/guide-overview.html)
- [!BADGE PaaS 전용]{type=Informative url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="Adobe Commerce 온 클라우드 프로젝트(Adobe 관리 PaaS 인프라) 및 온프레미스 프로젝트에만 적용됩니다."} [PayPal 빠른 체크아웃](paypal-express-checkout.md)
- [!BADGE PaaS만]{type=Informative url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="Adobe Commerce 온 클라우드 프로젝트(Adobe 관리 PaaS 인프라) 및 온프레미스 프로젝트에만 적용됩니다."} [Braintree](braintree.md)

### 기타 PayPal 결제 솔루션

[!BADGE PaaS만]{type=Informative url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="Adobe Commerce 온 클라우드 프로젝트(Adobe 관리 PaaS 인프라) 및 온프레미스 프로젝트에만 적용됩니다."}

PayPal 결제 방법 옵션에 대한 자세한 내용은 [PayPal 결제 솔루션](paypal.md)을 참조하세요.

#### 올인원 PayPal 솔루션

[!BADGE PaaS만]{type=Informative url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="Adobe Commerce 온 클라우드 프로젝트(Adobe 관리 PaaS 인프라) 및 온프레미스 프로젝트에만 적용됩니다."}

- [PayPal 결제 고급](paypal-payments-advanced.md)
- [PayPal 결제 프로](paypal-payments-pro.md)
- [PayPal 결제 표준](paypal-payments-standard.md)

#### PayPal 결제 게이트웨이

[!BADGE PaaS만]{type=Informative url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="Adobe Commerce 온 클라우드 프로젝트(Adobe 관리 PaaS 인프라) 및 온프레미스 프로젝트에만 적용됩니다."}

- [Paypal Payflow Pro](paypal-payflow-pro.md)
- [PayPal 결제 링크](paypal-payflow-link.md)

## 사기 방지

[!BADGE PaaS만]{type=Informative url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="Adobe Commerce 온 클라우드 프로젝트(Adobe 관리 PaaS 인프라) 및 온프레미스 프로젝트에만 적용됩니다."}

사기 방지 서비스 및 필터는 거래가 처리되기 전에 제출된 주문을 검사하여 부정 주문을 감지하고 비용 부담으로부터 고객을 보호합니다. Adobe Commerce 및 Magento Open Source은 다음과 같은 사기 방지 솔루션을 지원합니다.

- [PayPal 사기 행위 관리 필터](paypal.md#paypal-fraud-management-filters)

- [마켓플레이스의 사기 행위 방지 솔루션][1]

>[!NOTE]
>
>보안 규정 준수를 위한 업데이트를 지원하기 위해 2.4.0 릴리스부터 Commerce에서 Signifyd 사기 방지 기능이 제거됩니다. 2.3.x 또는 이전 릴리스에서 Signifyd 통합을 사용한 경우 [Signifyd 사기 및 비용 산출 보호 확장](https://marketplace.magento.com/signifyd-module-connect.html){:target="_blank"}(으)로 전환하는 것이 좋습니다. 공급업체 지침에 따라 확장에 대한 업데이트를 유지해야 합니다.

## 리소스 문제 해결

[!BADGE PaaS만]{type=Informative url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="Adobe Commerce 온 클라우드 프로젝트(Adobe 관리 PaaS 인프라) 및 온프레미스 프로젝트에만 적용됩니다."}

결제 문제 해결에 대한 도움말은 [지원 기술 자료](https://experienceleague.adobe.com/docs/commerce-knowledge-base/kb/overview.html)를 참조하십시오.

[1]: https://marketplace.magento.com/catalogsearch/result?q=fraud%20protection
