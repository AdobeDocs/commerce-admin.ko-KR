---
title: 규모에 맞는 개인화
description: Adobe Commerce에서 쇼핑객을 위한 개인화된 경험을 만들 수 있는 기능을 알아봅니다.
feature: Customers, Storefront, Personalization
source-git-commit: a4eeda918adcb74ad5e7008b80eff703fa15e878
workflow-type: tm+mt
source-wordcount: '1341'
ht-degree: 0%

---

# 규모에 맞는 개인화

규모&#x200B;의 개인화를 통해 즉각적인 컨텍스트 및 이전에 관찰된 행동을 기반으로 모든 고객 접점에 대한 쇼핑 경험을 개인화할 수 있습니다. 매번 가장 관련성이 높고 개인화된 경험을 제시하는 것이 목표다.

개인화된 쇼핑 경험을 제공할 때의 이점을 이해하려면 [_규모에 맞게 개인화 시작하기_](https://business.adobe.com/resources/reports/getting-started-with-personalization-at-scale.html) 보고서.

개인화된 쇼핑 경험을 만들려면 고객 컨텍스트를 이해하는 데 필요한 데이터 유형에 대해 알아두어야 합니다. 여기에서 해당 데이터를 사용하여 개인화된 쇼핑 경험을 만드는 데 필요한 고객 인사이트를 여는 Adobe Commerce 기능에 대해 알아봅니다.

다음 이미지는 쇼핑 경험을 개인화하는 데 포함된 개념을 보여 줍니다.

![개인화 파이프라인 구축](assets/personalization-journey.png){width="700" zoomable="yes"}

이 문서에서는 위의 각 개념에 대해 보다 자세히 설명합니다.

## 쇼핑 경험을 개인화하는 방법

성공적인 개인화는 고객 컨텍스트에서 시작됩니다. 이 섹션에서는 고객 컨텍스트를 구축하는 데 도움이 되는 데이터 유형에 대해 알아봅니다.

### Storefront 데이터

행동 또는 브라우저 데이터라고도 하는 상점 데이터는 쇼핑객이 귀하의 사이트와 상호 작용하는 방법에 대한 통찰력을 보여줄 수 있습니다. For example:

- 쇼핑객들이 가장 관심 있는 제품 및 카테고리는 무엇입니까?
- 내 쇼핑객들이 가장 많이 참여하는 검색 쿼리는 무엇입니까?
- 쇼핑객들이 장바구니에 상품을 추가했다가 포기하는 건가요?
- 쇼핑객이 데스크탑 또는 모바일 브라우저를 사용하고 있습니까?

다음 Storefront 이벤트는 이러한 질문에 답변하는 데 도움이 될 수 있는 데이터를 캡처합니다.

- [pageView](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/data-connection/event-forwarding/events)
- [searchRequestSent](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/data-connection/event-forwarding/events)
- [searchResponseReceived](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/data-connection/event-forwarding/events)
- [제품 페이지 보기](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/data-connection/event-forwarding/events)
- [추가 장바구니](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/data-connection/event-forwarding/events)
- [openCart](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/data-connection/event-forwarding/events)
- [로그인](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/data-connection/event-forwarding/events)
- [로그아웃](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/data-connection/event-forwarding/events)
- [startCheck](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/data-connection/event-forwarding/events)
- [completeCheckout](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/data-connection/event-forwarding/events)
- [createRequisitionList](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/data-connection/event-forwarding/events)
- [addToRequisitionList](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/data-connection/event-forwarding/events)
- [removeFromRequisitionList](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/data-connection/event-forwarding/events)

### 백오피스 데이터

서버측 데이터라고도 하는 백오피스 데이터는 주문 수명 주기에 대한 통찰력을 보여줄 수 있습니다. For example:

- 계절에 따라 더 자주 구매하는 상품이 있나요?
- 쇼핑객들이 반품하고 있나요?
- 라이프타임 고객 가치를 계산하려면 어떻게 해야 합니까?

다음 백오피스 이벤트는 이러한 질문에 답변하는 데 도움이 될 수 있는 데이터를 캡처합니다.

- [주문](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/data-connection/event-forwarding/events-backoffice)
- [orderItemsReturnInitiated](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/data-connection/event-forwarding/events-backoffice)
- [orderItemsShipped](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/data-connection/event-forwarding/events-backoffice)
- [orderCanceled](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/data-connection/event-forwarding/events-backoffice)

### 고객 프로필 및 세그먼트 데이터

고객 프로필 데이터는 구매자가 누구이며 어떤 세그먼트에 해당되는지에 대한 인사이트를 보여줄 수 있습니다. For example:

- 이름
- 성별
- 주소
- 충성도 상태
- 전화 번호
- 이메일 주소
- 충성도 상태
- 전화 번호
- 이메일 주소
- 업그레이드 가능 여부
- 크로스 채널 쇼핑객
- 신제품 전망
- 골드, 실버 또는 브론즈 로열티 멤버

다음 프로필 이벤트는 이러한 질문에 답변하는 데 도움이 될 수 있는 데이터를 캡처합니다.

- [프로필 레코드](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/data-connection/event-forwarding/events-profilerecord)
- [accountCreated](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/data-connection/event-forwarding/events-backoffice)
- [계정 업데이트됨](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/data-connection/event-forwarding/events-backoffice)
- [accountDeleted](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/data-connection/event-forwarding/events-backoffice)

상점, 백오피스 및 프로필 데이터는 Commerce 고객 및 주문 컨텍스트의 기초를 형성하므로 고객이 보고 구매하는 제품이 무엇인지 알 수 있습니다. 그런 다음 고객의 관심사를 타겟팅하고 경험을 개인화할 수 있습니다. 다음 섹션에서는 쇼핑객과 참여할 수 있는 개인화된 경험 유형에 대해 알아봅니다.

## 개인화된 경험 유형

Commerce의 고객 및 주문 컨텍스트 데이터는 다음과 같은 유형의 개인화된 경험을 제공합니다.

| 경험 | 설명 |
|---|---|
| **제품 검색** | 다음과 같은 머천다이징 서비스를 포함합니다. [SaaS로 배포](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/user-guides/integration-services/saas). 이것은 행동 데이터, 제품 속성 및 재고 수준을 사용하여 검색 결과, 제품 권장 사항 및 검색 페이지에서 제품 검색을 자동으로 개인화할 수 있는 기능입니다. 이러한 기능은 모두 [ADOBE SENSEI AI](https://business.adobe.com/products/sensei/adobe-sensei.html). |
| **사이트 콘텐츠** | 사이트를 탐색하는 현재 고객을 기반으로 개인화된 동적 콘텐츠 블록을 배포하는 기능을 나타냅니다. |
| **오퍼 및 캠페인** | 세그먼트 데이터를 기반으로 개인화된 홍보 콘텐츠를 배포할 수 있습니다. |
| **측정** | 데이터 인텔리전스를 사용하여 매출, 채널 및 상품 성과, 프로모션 등을 포함하여 비즈니스를 더 잘 이해합니다. |

다음 두 섹션에서는 이 데이터를 사용하여에서 개인화된 경험을 만드는 방법을 알아봅니다 [Adobe Experience Platform](#using-commerce-data-in-adobe-experience-platform) 및 [기본 Commerce 기능](#using-commerce-data-in-native-commerce-features).

## Adobe Experience Platform에서 상거래 데이터 사용

모든 채널에서 쇼핑객을 위한 개인화된 경험을 만들려면 를 사용하여 상거래 데이터를 Experience Platform Edge Network로 보내십시오. [[!DNL Data Connection]](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/data-connection/overview) 확장명.

![데이터가 Experience Platform 에지로 이동하는 방법](assets/commerce-edge.png){width="700" zoomable="yes"}

위의 이미지에서 상점, 백오피스 및 고객 프로필 데이터는 SDK, API 및 소스 커넥터를 사용하여 Experience Platform Edge로 전송됩니다. 확장이 데이터 공유 복잡성을 처리하므로 이러한 부분이 어떻게 작동하는지 완전히 이해할 필요는 없습니다. 이벤트 데이터가 에지에 있으면 해당 데이터를 다른 Experience Platform 애플리케이션으로 가져올 수 있습니다.

다음 표에서는 사용 가능한 일부 Experience Platform 애플리케이션과 이러한 애플리케이션이 상거래 데이터를 사용하는 방법을 중점적으로 보여 줍니다.

| 경험 | 애플리케이션 | 상거래 데이터 사용 방법 |
|---|---|---|
| **사이트 콘텐츠** | [Adobe [!DNL Real-Time CDP]](https://experienceleague.adobe.com/en/docs/experience-platform/rtcdp/intro/rtcdp-intro/overview) | Adobe Commerce 데이터는 여러 소스(ERP, CRM, CMS, POS)의 데이터를 단일 프로필로 연결하는 Real-Time CDP을 통해 통합 고객 프로필을 향상시킵니다. Real-Time CDP은 규칙 기반 세그먼트와 AI 기반 세그먼트를 모두 만들어 마케팅 솔루션 세트에서 사용할 수도 있습니다. Real-Time CDP 대상을 사용하여 콘텐츠 블록, 프로모션 및 관련 제품 규칙을 개인화할 수도 있습니다. 다음을 참조하십시오 [[!DNL Audience Activation]](../customers/audience-activation.md) 자세히 알아보십시오&#x200B;. |
|  | [Adobe [!DNL Target]](https://experienceleague.adobe.com/en/docs/target/using/introduction/intro) | Adobe Commerce 데이터는 Adobe에서 활성화할 수 있습니다. [!DNL Target] 동적 랜딩 페이지 테스트, 최적화 및 생성을 위해. 전송된 상거래 데이터를 기반으로 설명, 사양, 검토 및 권장 제품과 같이, 콘텐츠가 페이지에 표시되는 순서를 개인화할 수 있습니다. |
| **오퍼 및 캠페인** | [Adobe [!DNL Journey Optimizer]](https://experienceleague.adobe.com/en/docs/journey-optimizer/using/get-started/get-started) | Adobe Commerce 행동 및 백 오피스 데이터는 이메일 여정, SMS, 푸시 알림 등을 포함하여 개인화된 옴니채널 캠페인에 대한 트리거 역할을 할 수 있습니다&#x200B;. |
| **측정** | [Adobe [!DNL Analytics]](https://experienceleague.adobe.com/en/docs/analytics/analyze/admin-overview/analytics-overview) 및 [고객 [!DNL Journey Analytics]](https://experienceleague.adobe.com/en/docs/analytics-platform/using/cja-overview/cja-overview) | Commerce가 상점 및 백오피스 데이터를 모두 고객에게 전송 [!DNL Journey Analytics] (및 Adobe에 대한 storefront 데이터만 해당) [!DNL Analytics])를 사용하여 매출, 상품 및 프로모션과 같은 Adobe Commerce Intelligence의 기본 지표 이상의 풍부한 분석을 수행할 수 있습니다&#x200B;. |

상거래 데이터를 Experience Platform에 보내는 방법에 대한 자세한 내용은 [데이터 연결](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/data-connection/overview).

## 기본 Commerce 기능에서 상거래 데이터 사용

다음 섹션에서는 제품 Recommendations 및 라이브 검색과 같은 기본 Commerce 기능을 사용하여 개인화된 쇼핑 경험을 만드는 방법에 대해 알아봅니다. 다음 기능에 대해서도 학습하게 됩니다. [!DNL Audience Activation]: 언급된 대로 Real-Time CDP라는 Experience Platform에서 사용할 수 있는 제품의 데이터를 사용합니다 [이전에](#using-commerce-data-in-adobe-experience-platform). Real-Time CDP은 Commerce의 기반이 아니지만 를 통해 해당 정보를 Commerce에 수집할 수 있습니다. [[!DNL Audience Activation]](../customers/audience-activation.md) 확장명.

다음 표에서는 Commerce 고객 및 주문 컨텍스트 데이터를 실행 가능한 통찰력으로 변환하는 데 사용할 수 있는 Commerce 기능을 강조 표시합니다.

| 경험 | 기능 | 설명 |
|---|---|---|
| **제품 검색** | [라이브 검색](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/live-search/guide-overview) | AI 등급 알고리즘을 사용하여 쇼핑객의 현장 행동 행동을 기반으로 검색 결과를 개인화하고 최적화하여 검색 관련성과 전환을 향상시킵니다. |
|  | [제품 Recommendations](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/product-recommendations/guide-overview) | 쇼핑객 행동, 트렌드, 제품 유사성 등을 기반으로 AI 기반 제품 권장 사항을 표시합니다. Adobe Commerce 카탈로그와 결합하면 제품 추천은 매우 매력적이고 관련성이 높으며 개인화된 경험을 제공합니다. |
|  | [카테고리 머천다이징](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/live-search/live-search-admin/category-merch) | 라이브 검색 관리자에서 액세스하는 카테고리 머천다이징은 AI를 사용하여 각 카테고리 페이지의 제품 시퀀스를 자동으로 재분류하여 모든 구매자의 관련성과 전환을 향상시킵니다. AI 기반 규칙을 만들고 관리하여 구매자 작업 및 관심도에 따라 카테고리 페이지의 제품 순서를 자동으로 재지정할 수 있습니다. |
| **사이트 콘텐츠** | [기본 Commerce 기능에서 제공하는 동적 블록](https://experienceleague.adobe.com/en/docs/commerce-admin/content-design/elements/dynamic-blocks/dynamic-blocks) | 가격 규칙 및 고객 세그먼트에 구성된 논리를 기반으로 개인화된 사이트 콘텐츠를 제공할 수 있습니다. |
|  | [Real-Time CDP 대상자가 알려주는 동적 블록](../customers/audience-activation.md) | 판매자가 Real-Time CDP에 구성된 대상을 기반으로 개인화된 사이트 콘텐츠를 제공할 수 있습니다. |
| **오퍼 및 캠페인** | [장바구니 가격 규칙](https://experienceleague.adobe.com/en/docs/commerce-admin/marketing/promotions/cart-rules/price-rules-cart) | 조건 세트에 따라 장바구니의 항목에 할인을 적용할 수 있습니다. |
|  | [기본 Commerce 기능에서 제공하는 동적 블록](https://experienceleague.adobe.com/en/docs/commerce-admin/content-design/elements/dynamic-blocks/dynamic-blocks) | Commerce에 기본적으로 구성된 고객 세그먼트를 기반으로 개인화된 배너 프로모션을 표시할 수 있습니다. |
|  | [Real-Time CDP 대상자가 알려주는 동적 블록](../customers/audience-activation.md) | Real-Time CDP에 구성된 대상을 기반으로 개인화된 프로모션을 표시할 수 있습니다. |
| **측정** | [Adobe Commerce 인텔리전스](https://experienceleague.adobe.com/en/docs/commerce-business-intelligence/mbi/getting-started) | (이전의 Magento Business Intelligence)는 데이터 기반 결정을 내리고 명확하고 정보에 입각한 조치를 취하는 데 도움이 되는 모범 사례 인사이트를 제공하는 클라우드 플랫폼입니다. Adobe Commerce Intelligence는 데이터를 분석하여 주문 증가, 고객 행동 및 홍보 전략의 효과에 대한 질문에 답변할 수 있도록 지원합니다. |
