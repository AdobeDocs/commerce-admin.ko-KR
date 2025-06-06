---
title: 규모에 맞게 매력적이고 개인화된 경험 만들기
description: Adobe의 기능을 알아보세요 [!DNL Commerce] 쇼핑객을 위한 개인화된 환경을 만들 수 있습니다.
feature: Customers, Storefront, Personalization
exl-id: 9546e1b8-796b-4694-8396-773a2b0e9c12
source-git-commit: 5da244a548b15863fe31b5df8b509f8e63df27c2
workflow-type: tm+mt
source-wordcount: '1808'
ht-degree: 0%

---

# 규모에 맞게 매력적이고 개인화된 경험 만들기

Adobe [!DNL Commerce]은(는) 모든 고객 접점을 개인화하여 쇼핑객 참여, 전환 및 매출을 높일 수 있는 강력한 툴킷을 제공합니다.

이 문서에서는 다음을 학습합니다.

- 개인화란?
- 개인화를 달성하는 데 필요한 데이터는 무엇입니까?
- Adobe [!DNL Commerce]에서 개인 맞춤화를 잠금 해제하는 방법은 무엇입니까?
- 사용 가능한 개인화 사용 사례

## 개인화란?

Personalization은 각 고객의 고유한 요구 사항, 컨텍스트 및 선호도를 충족하도록 각 고객의 구매 경험을 맞춤화하는 것을 의미합니다. Personalization은 사이트의 콘텐츠나 가장 적합한 제품을 추천하는 데 그치지 않고 다음을 포함하여 고객 여정의 모든 접점을 포괄합니다.

- **캠페인 및 커뮤니케이션** - 캠페인 및 커뮤니케이션을 통해 관련성 있고 일관된 메시지 전달
- **제품 검색** - 적절한 시기에 적절한 고객에게 적절한 제품 표시
- **프로모션 및 오퍼** - 각 고객이 전환하도록 유도하는 프로모션 및 오퍼에 타깃팅
- **콘텐츠 경험** - 사이트 콘텐츠를 맞춤화하여 각 고객 및 해당 여정과 밀접한 관계가 있음을 느끼도록 합니다.

![Personalization 유형](assets/types-personalization.png){width="700" zoomable="yes"}

일부 소규모 고객에게는 이러한 유형의 개인화된 경험을 달성할 수 있는 것처럼 보일 수 있지만, 모든 접점 및 채널에서 수천 또는 수백만의 고객을 대상으로 실시간으로 개인화하는 것은 모두 불가능하다고 느낄 수 있습니다. 다음 섹션에서는 Adobe [!DNL Commerce] 및 Adobe Experience Cloud이 어떻게 도움이 되는지 알아봅니다.

## 개인화를 달성하는 데 필요한 데이터는 무엇입니까?

효과적인 개인화를 위해서는 고객의 경험을 수정하는 데 사용할 수 있는 고객에 대한 정보를 제공하는 컨텍스트 또는 신호가 필요합니다. 다음 표에서는 다양한 데이터 형식과 해당 데이터의 수집 및 활성화를 지원하는 데 Adobe [!DNL Commerce]이(가) 수행하는 역할을 제공합니다.

| 데이터 유형 | Storefront 데이터(행동 이벤트) | 백오피스 데이터(서버측 이벤트) | 고객 프로필 및 세그먼트 데이터 |
|---|---|---|---|
| **정의** | 고객이 사이트에서 수행하는 클릭 또는 작업입니다. | 각 주문(과거 및 현재)의 라이프사이클 및 세부 정보에 대한 정보. | 구매자가 누구이며 어떤 세그먼트에 해당하는지 지정합니다. |
| **Adobe Commerce에서 캡처한 이벤트** | [pageView](https://experienceleague.adobe.com/ko/docs/commerce/data-connection/event-forwarding/events#pageview)<br>[productPageView](https://experienceleague.adobe.com/ko/docs/commerce/data-connection/event-forwarding/events)<br>[searchRequestSent](https://experienceleague.adobe.com/ko/docs/commerce/data-connection/event-forwarding/events#searchrequestsent)<br>[searchResponseReceived](https://experienceleague.adobe.com/ko/docs/commerce/data-connection/event-forwarding/events#searchresponsereceived)<br>[addToCart](https://experienceleague.adobe.com/ko/docs/commerce/data-connection/event-forwarding/events#addtocart)<br>[openCart](https://experienceleague.adobe.com/ko/docs/commerce/data-connection/event-forwarding/events#opencart)<br>[signIn](https://experienceleague.adobe.com/ko/docs/commerce/data-connection/event-forwarding/events#signin)<br>[signOut](https://experienceleague.adobe.com/ko/docs/commerce/data-connection/event-forwarding/events#signout)<br>[startCheckout](https://experienceleague.adobe.com/ko/docs/commerce/data-connection/event-forwarding/events#startcheckout)<br>[completeCheckout](https://experienceleague.adobe.com/ko/docs/commerce/data-connection/event-forwarding/events#completecheckout)<br>[createRequisitionList](https://experienceleague.adobe.com/ko/docs/commerce/data-connection/event-forwarding/events#createrequisitionlist)<br>[addToRequisitionList](https://experienceleague.adobe.com/ko/docs/commerce/data-connection/event-forwarding/events#addtorequisitionlist)<br>[removeFromRequisitionList](https://experienceleague.adobe.com/ko/docs/commerce/data-connection/event-forwarding/events#removefromrequisitionlist) | **주문 상태**:<br>[주문 상태](https://experienceleague.adobe.com/ko/docs/commerce/data-connection/event-forwarding/events-backoffice#orderplaced)<br>[주문 항목 반환 시작](https://experienceleague.adobe.com/ko/docs/commerce/data-connection/event-forwarding/events-backoffice#orderitemsreturnedinitiated)<br>[주문 항목 배달](https://experienceleague.adobe.com/ko/docs/commerce/data-connection/event-forwarding/events-backoffice#orderitemsshipped)<br>[주문 취소](https://experienceleague.adobe.com/ko/docs/commerce/data-connection/event-forwarding/events-backoffice#ordercancelled)<br>[**주문 내역**](https://experienceleague.adobe.com/ko/docs/commerce/data-connection/fundamentals/connect-data#send-historical-order-data):<br>- SKU, 이름, 가격 수량, 할인<br>- 제품 범주<br>- 결제 금액, 유형, 통화<br>- 배송 방법 및 금액<br>- 환불 ID, 금액, 통화<br>- 반송 이유, 조건, 해결 방법<br>- 주소<br>- 전자 메일 | [**프로필 레코드**](https://experienceleague.adobe.com/ko/docs/commerce/data-connection/event-forwarding/events-profilerecord): (이름, 성별, 주소, 충성도 상태, 전화 번호, 전자 메일 주소)<br>**계정 상태**:<br>[계정 생성됨](https://experienceleague.adobe.com/ko/docs/commerce/data-connection/event-forwarding/events-backoffice#accountcreated)<br>[계정 업데이트됨](https://experienceleague.adobe.com/ko/docs/commerce/data-connection/event-forwarding/events-backoffice#accountupdated)<br>[계정 삭제됨](https://experienceleague.adobe.com/ko/docs/commerce/data-connection/event-forwarding/events-backoffice#accountdeleted) |

이렇게 풍부한 자사 [!DNL Commerce] 데이터를 모두 사용하면 각 쇼핑객의 경험을 타겟팅하고 개인화할 수 있습니다. 다음 섹션에서는 [!DNL Commerce] 및 Adobe Experience Cloud이 개인화된 경험과 활성화할 수 있는 사용 사례를 만드는 데 어떻게 도움이 되는지에 대해 알아봅니다.

## Adobe [!DNL Commerce]은(는) 어떻게 개인화를 지원합니까?

Adobe [!DNL Commerce] 데이터 공유를 사용하면 이전 테이블의 데이터 유형을 수집하고 다른 Adobe Experience Cloud 제품에 공유하여 통합 고객 프로필 및 대상, 개인화된 캠페인, 풍부한 분석 및 통찰력을 강화할 수 있습니다.

![데이터가 Experience Platform Edge로 이동하는 방법](assets/commerce-edge.png){width="700" zoomable="yes"}

Adobe [!DNL Commerce] 데이터 공유에는 다음 두 가지 주요 구성 요소가 포함되어 있습니다.

1. [데이터 연결](https://experienceleague.adobe.com/ko/docs/commerce/data-connection/overview): 다음을 포함하여 Adobe Experience Cloud 응용 프로그램에서 사용할 수 있도록 Adobe [!DNL Commerce]의 상점, 백 오피스 및 고객 프로필 데이터를 Adobe Experience Platform edge network에 공유합니다.

   - [Adobe [!DNL Real-Time CDP]](https://experienceleague.adobe.com/ko/docs/experience-platform/rtcdp/intro/rtcdp-intro/overview): 여러 소스(ERP, CRM, POS)의 고객 데이터를 통합 프로필에 연결하고 규칙 기반 또는 AI 기반 세그먼트를 만듭니다.
   - [Adobe [!DNL Journey Optimizer]](https://experienceleague.adobe.com/ko/docs/journey-optimizer/using/get-started/get-started): 이메일 여정, SMS, 푸시 알림 등을 포함하여 개인화된 옴니채널 캠페인을 시작합니다.
   - [Customer Journey Analytics](https://experienceleague.adobe.com/ko/docs/analytics-platform/using/cja-overview/cja-overview) 및 [Adobe [!DNL Analytics]](https://experienceleague.adobe.com/ko/docs/analytics/analyze/admin-overview/analytics-overview): 고객 및 비즈니스에 대한 통찰력을 얻으십시오.
   - [Adobe [!DNL Target]](https://experienceleague.adobe.com/ko/docs/target/using/introduction/intro): 콘텐츠, 권장 제품, 오퍼, 탐색 등을 테스트하고 최적화합니다.

1. [[!DNL Audience Activation]](https://experienceleague.adobe.com/ko/docs/commerce-admin/customers/audience-activation): [!DNL Real-Time CDP] 대상을 사용하여 Adobe [!DNL Commerce] 사이트에서 동적 콘텐츠 블록, 프로모션 및 관련 제품 규칙을 개인화할 수 있습니다.

### 모든 채널에서 규모에 맞게 개인화된 Storefront 경험

Adobe [!DNL Commerce]은(는) 고성능 상점([Edge Delivery Services](https://experienceleague.adobe.com/developer/commerce/storefront/?lang=ko))을 활용하여 AI 기능을 핵심으로 하고 속도를 기반으로 모든 채널에 개인화된 경험을 제공할 수 있습니다.

Edge Delivery Services을 사용하여 다음과 같은 작업을 수행할 수 있습니다.

- **개인화된 콘텐츠 제작**: 경험을 규모에 맞게 개인화하기 위해 문서 기반 작성, 생성 AI 텍스트 및 이미지 변형을 통한 기본 실험을 사용합니다. Assets 및 생성 AI 콘텐츠 생성을 사용하여 규모에 맞게 제품 및 마케팅 이미지를 제작할 수 있습니다.

- **변형 생성**: 콘텐츠 작성자는 생성 AI를 사용하여 Adobe Firefly에서 대량의 개인화된 AI 기반 [텍스트 콘텐츠 및 이미지 변형](https://experienceleague.adobe.com/ko/docs/experience-manager-learn/sites/generative-ai/generate-variations)을 만들 수 있습니다.

- **Edge Delivery Services Storefront를 통해 배포**: 대상자를 위해 맞춤형 구매 가능한 경험을 만들기 위해, 드롭인 구성 요소에서 제공하는 Edge 및 Commerce 기능에 대한 콘텐츠입니다.

- **Commerce 및 Adobe Experience Manager Assets**: 대규모 생성 AI 제품 에셋 생성 및 변형. 모든 채널에서 컨텐츠 전달을 만들고, 전달하고, 모니터링합니다.

![드롭인: 제품 세부 정보 페이지](assets/drop-in.png){width="700" zoomable="yes"}

### 기본 제공 Personalization: 기본 Adobe [!DNL Commerce] 기능 시작

Adobe [!DNL Commerce]은(는) 기본 제공 기능으로 강력한 개인화를 제공합니다. 다음 표에서는 개인화 여정을 시작하기 위해 즉시 활성화할 수 있는 [!DNL Commerce] 기능에 대해 설명합니다.

| 범주 | 기능 |
|---|---|
| 개인화된 제품 검색 | [[!DNL Live Search]](https://experienceleague.adobe.com/ko/docs/commerce/live-search/overview): AI 기반 검색을 통한 구매자의 온사이트 행동 행동과 관심도에 따라 검색 결과를 개인화하고 최적화합니다.<br>[지능형 카테고리 머천다이징](https://experienceleague.adobe.com/ko/docs/commerce/live-search/live-search-admin/category-merch): 구매자의 현장 행동 및 관심도를 기반으로 카테고리 페이지에서 AI 기반 제품 순위를 지정합니다.<br>[제품 추천](https://experienceleague.adobe.com/ko/docs/commerce/product-recommendations/guide-overview): 구매자 행동, 트렌드 및 선호도를 기반으로 하는 AI 기반 제품 추천.<br>[관련 제품 규칙](https://experienceleague.adobe.com/ko/docs/commerce-admin/marketing/promotions/product-relationships/product-related-rules): 크로스셀 및 업셀할 수 있도록 카탈로그의 제품을 표시하는 사용자 지정 규칙을 정의합니다. |
| 개인화된 사이트 콘텐츠 | [다이내믹 콘텐츠 블록](https://experienceleague.adobe.com/ko/docs/commerce-admin/content-design/elements/dynamic-blocks/dynamic-blocks): Adobe Commerce의 고객 세그먼트를 기반으로 개인화된 콘텐츠 블록(예: 배너)을 표시합니다. |
| 개인화된 오퍼 및 프로모션 | [장바구니 가격 규칙](https://experienceleague.adobe.com/ko/docs/commerce-admin/marketing/promotions/cart-rules/price-rules-cart): Adobe [!DNL Commerce]의 고객 세그먼트를 포함한 일련의 조건을 기준으로 장바구니 항목에 할인을 적용합니다. |
| 인사이트 및 측정 | [Adobe [!DNL Commerce] 인텔리전스](https://experienceleague.adobe.com/ko/docs/commerce-business-intelligence/mbi/getting-started): 개인화 전략이 어떻게 작동하는지 이해하고 시간이 지남에 따라 개선됩니다. |

## 주요 개인화 사용 사례

Adobe [!DNL Commerce] 고객은 기본 제공 기능을 사용하고 다양한 사용 사례를 위해 Adobe Experience Cloud에 데이터를 공유합니다. 다음 섹션에서는 주요 사용 사례를 강조하고 Adobe [!DNL Commerce]만 또는 [!DNL Commerce] 및 Experience Cloud 앱을 사용하여 구현하는 방법을 설명합니다.

### 개인화된 캠페인 및 커뮤니케이션

| 사용 사례 | 솔루션 |
|---|---|
| **포기한 장바구니 및 찾아보기** - 고객이 높은 참여를 보여 준 후 장바구니 또는 탐색 세션을 중단하면 개인화된 재참여 전자 메일 또는 알림을 보냅니다. | **Adobe [!DNL Commerce]만**:<br>[Adobe Journey Optimizer이 있는 전자 메일 미리 알림](https://experienceleague.adobe.com/ko/docs/commerce-admin/marketing/communications/email-reminders/email-reminder-rules)<br>**Adobe [!DNL Commerce]**:<br>[!DNL Commerce] 데이터는 옴니채널 포기 여정의 트리거 역할을 합니다. 고객 속성, 포기한 항목, 기타 쇼핑 행동 및 과거 구매를 기반으로 해당 여정을 개인화합니다.<br>Adobe Journey Optimizer 및 Real-Time CDP이 포함된 Commerce: 높은 포기 비율 대상을 만드는 등 통합 고객 프로필과 중앙 관리되는 대상을 기반으로 포기 캠페인을 사용자 지정합니다. |
| **중앙 집중식 대상자 만들기** - 온사이트 행동, 과거 구매, 프로필 특성, 카테고리 관심도, 충성도 상태, 고객 가치 등을 기반으로 규칙 기반 또는 AI 기반 대상자를 만듭니다. | **Adobe [!DNL Commerce]만**:<br>[!DNL Commerce]명의 고객이 계정을 만들 때 고객 프로필 정보를 수집합니다. 규칙 기반 [고객 세그먼트](https://experienceleague.adobe.com/ko/docs/commerce-admin/customers/segments/customer-segments) 및 고객 그룹을 만들어 콘텐츠와 프로모션을 개인화합니다.<br>**Adobe [!DNL Commerce]&#x200B;(Adobe Real-Time CDP 포함)**:<br> 여러 데이터 소스 및 채널에서 [통합 프로필](https://experienceleague.adobe.com/ko/docs/experience-platform/segmentation/home), 규칙 기반 또는 AI 기반 대상. |
| **쇼핑객 행동에 따른 개인화된 이메일/SMS 오퍼** - 지난 구매 및 쇼핑객 행동에 따른 타겟팅된 이메일을 통해 고객에게 개인화된 오퍼를 보냅니다(예: 고객이 보거나 참여한 제품이나 범주에 대한 오퍼 보내기). | **Adobe [!DNL Commerce]만**:<br>마케팅 자동화 솔루션에 사용할 데이터를 내보냅니다.<br>**Adobe Journey Optimizer 및 Real-Time CDP이 있는 Adobe [!DNL Commerce]**:<br>[!DNL Commerce] 데이터는 이메일 또는 SMS 오퍼의 트리거 역할을 하며, 이를 기반으로 개인화할 신호(쇼핑객 행동)를 제공합니다. Real-Time CDP이 필요하지 않지만, 일반적으로 이러한 오퍼와 캠페인은 Real-Time CDP 내에서 만들고 관리하는 대상을 중심으로 만들어집니다. |
| **호환되는 제품/브랜드 교차 또는 상향 판매** - 고객이 호환되는 제품 또는 브랜드를 하나 구입하거나 다른 제품 또는 브랜드에 대한 높은 선호도를 나타내는 경우 교차 판매 전환을 유도하기 위해 캠페인(이메일/SMS)을 보냅니다. | **Adobe [!DNL Commerce]만 해당**:<br>사이트에서 특정 제품을 추천하려면 Adobe [!DNL Commerce] [제품 추천](https://experienceleague.adobe.com/ko/docs/commerce/product-recommendations/guide-overview)을 사용하세요. [관련 제품 규칙](https://experienceleague.adobe.com/ko/docs/commerce-admin/marketing/promotions/product-relationships/product-related-rules)을 사용하여 다른 제품을 제안할 수도 있습니다.[!DNL Target]**:<br>Adobe [!DNL Target]이(가) 있는 <br>**[!DNL Commerce]에도 카테고리 관심도와 같은 강력한 기능을 갖춘 제품 추천 엔진이 내장되어 있습니다. 이 값은 교차 또는 상향 판매에 사용할 수 있습니다.<br>**[!DNL Commerce] (Adobe Journey Optimizer 포함)**:<br>[!DNL Target] 또는 [!DNL Commerce]을(를) 사용하여 추천할 제품을 결정한 다음 Adobe Journey Optimizer을 통해 배달하십시오. |

### 개인화된 사이트 경험

| 사용 사례 | 솔루션 |
|---|---|
| **개인화된 사이트 콘텐츠** - 제품 검색 및 카테고리 관심도와 같은 쇼핑객 작업을 기반으로 사이트 배너 및 기타 페이지 콘텐츠를 개인화합니다. A/B 테스트 또는 비즈니스 목표 결과에 따라 최적 콘텐츠를 배포합니다. | **Adobe [!DNL Commerce]만**:<br>세그먼트별 [동적 콘텐츠 블록 배포](https://experienceleague.adobe.com/ko/docs/commerce-admin/content-design/elements/dynamic-blocks/dynamic-blocks).Real-Time CDP을 사용하는 <br>**[!DNL Commerce]**:<br>Real-Time CDP에서 프로필과 대상을 중앙 집중식으로 관리하면서 실시간 작업 및 통합 고객 프로필 데이터에 응답하는 대상별 다이내믹 콘텐츠 블록을 배포하려면 [Audience Activation](https://experienceleague.adobe.com/ko/docs/commerce-admin/customers/audience-activation)을(를) 사용합니다.<br>**[!DNL Commerce][!DNL Target]**:<br>Adobe [!DNL Target]에서 Adobe [!DNL Commerce] 데이터를 사용하여 콘텐츠, 탐색 항목, 전체 페이지 레이아웃 등 사이트 환경의 모든 부분을 개인화합니다. A/B 테스트 컨텐츠에서 각 고객에 대해 우수성이 검증된 컨텐츠를 자동으로 선택하고 배포합니다.<br>**[!DNL Commerce] (AEM Assets 포함)**:<br>모든 콘텐츠를 Adobe Experience Manager Assets에 저장합니다. Adobe Commerce 내에서 해당 콘텐츠에 기본적으로 액세스합니다. 생성 AI를 사용하여 다양한 세그먼트나 대상자를 개인화할 수 있는 콘텐츠 변형을 만듭니다. |
| **행동에 따라 개인화된 온사이트 오퍼** - 제품 검색 및 카테고리 관심도와 같은 쇼핑객 작업에 따라 프로모션을 개인화합니다. A/B 테스트 또는 비즈니스 목표에 따라 다음 최상의 오퍼를 배포합니다. | **Adobe [!DNL Commerce]만**:<br>세그먼트별 카탈로그 및 [장바구니 가격 규칙 배포](https://experienceleague.adobe.com/ko/docs/commerce-admin/marketing/promotions/cart-rules/price-rules-cart).<br>**Real-Time CDP이 있는 Adobe [!DNL Commerce]**:<br>Real-Time CDP에서 프로필/대상을 중앙에서 관리하는 동시에 대상별 오퍼를 배포하려면 [Audience Activation](https://experienceleague.adobe.com/ko/docs/commerce-admin/customers/audience-activation)을(를) 사용하십시오.<br>**Commerce([!DNL Target]** 포함): offer decisioning을 사용하여 배포할 오퍼를 결정하거나 A/B 테스트를 수행하거나 비즈니스 목표를 설정하여 Adobe Commerce에 배포된 오퍼를 안내합니다. |

### Analytics 및 인사이트

| 사용 사례 | 솔루션 |
|---|---|
| **채널별 고객 행동** - 고객이 각 채널(웹, 대면, 앱, 기타)에 참여하여 각 채널의 마케팅 전략에 영향을 미치는 방식의 미묘한 차이를 이해하고 고객 경험의 취약점과 쇼핑객 단계를 이해합니다. | **Adobe [!DNL Commerce]만**:<br>[Adobe [!DNL Commerce] 인텔리전스](https://experienceleague.adobe.com/ko/docs/commerce-business-intelligence/mbi/getting-started)는 디지털 [!DNL Commerce] 채널에서 풍부한 분석을 제공하지만 여러 채널 또는 더 광범위한 고객 여정 부분에서는 제공하지 않습니다.<br>**Customer Journey Analytics이 있는 Adobe [!DNL Commerce]**:<br>[!DNL Commerce] 데이터 피드 데이터 대시보드를 통해 고객 경험의 모든 단계(채널 간)에 대한 세부 정보를 전체적으로 볼 수 있습니다. 모든 접점과 광범위한 단계를 이해하여 고객이 이탈할 수 있는 고객 여정의 취약점을 식별합니다. |
| **구매 트렌드** - 특정 기간(예: 장바구니 분석, 제품 분석) 동안의 구매 행동을 파악하여 트렌드, 계절성을 식별하고 구매 패턴을 기반으로 마케팅을 최적화합니다. | **Adobe [!DNL Commerce]만**:<br>[Adobe [!DNL Commerce] 인텔리전스](https://experienceleague.adobe.com/ko/docs/commerce-business-intelligence/mbi/getting-started)는 디지털 [!DNL Commerce] 채널에서 풍부한 분석을 제공하지만 여러 채널 또는 더 광범위한 고객 여정 부분에서는 제공하지 않습니다.<br>**Customer Journey Analytics이 있는 Adobe [!DNL Commerce]**:<br>[!DNL Commerce] 데이터 피드 데이터 대시보드를 통해 고객 경험의 모든 단계(채널 간)에 대한 세부 정보를 전체적으로 볼 수 있습니다. 모든 접점과 광범위한 단계를 이해하여 고객이 이탈할 수 있는 고객 여정의 취약점을 식별합니다. |

## 예제 사용 사례

- Adobe Journey Optimizer을 사용하여 [포기한 장바구니 전자 메일을 보내는](https://experienceleague.adobe.com/ko/docs/commerce/data-connection/use-cases/using-ajo)방법을 알아보세요.
- Adobe [!DNL Commerce]에서 장바구니 가격 규칙을 알리기 위해 [Real-Time CDP에서 대상을 만들기](https://experienceleague.adobe.com/ko/docs/commerce/data-connection/use-cases/create-audience)하는 방법을 알아봅니다.
