---
title: '[!DNL Google Analytics]'
description: ' [!DNL Google Analytics] 을(를) 사용하여 Commerce 사이트에 유용한 지표를 수집하는 방법을 알아봅니다.'
exl-id: d4df2ef2-d67f-46bf-8569-cbee9dde77e4
feature: Marketing Tools, Integration
source-git-commit: cace9d1de00955494d8bc607c017778ff7df4806
workflow-type: tm+mt
source-wordcount: '732'
ht-degree: 0%

---

# [!DNL Google Analytics]

[!DNL Google Analytics]은(는) 오프라인 및 모바일 앱 상호 작용을 지원하고 진행 중인 업데이트에 액세스하여 추적을 위한 추가 사용자 지정 차원 및 지표를 정의할 수 있는 기능을 제공합니다. [!DNL Google Analytics] 4는 Google의 차세대 측정 솔루션이며 [!DNL Universal Analytics]을(를) 대체합니다. 2023년 7월 1일에 표준 Universal Analytics 속성은 새 히트 처리를 중지합니다.

>[!NOTE]
>
>비즈니스에 [일반 데이터 보호 규정](../getting-started/compliance-gdpr.md) 및/또는 [캘리포니아 소비자 개인정보 보호법](../getting-started/compliance-ccpa.md)과 같은 개인정보 보호 규정이 적용되는 경우 [Google 개인정보 보호 설정](google-tools.md#google-privacy-settings)을 참조하십시오.

>[!IMPORTANT]
>
>[쿠키 제한 모드](../getting-started/compliance-cookie-law.md)를 사용하면 [!DNL Google Analytics]에서 쿠키를 수락하지 않는 한 방문자에 대한 데이터를 수집하지 않습니다.

## [!DNL Google Analytics] 4

{{gtag-api-note}}

### 1단계: [!UICONTROL Google Analytics] 4 설정

사이트에 대한 [!DNL Google Analytics] 4 설정이 없는 경우 다음 방법 중 하나를 따르십시오.

- [처음으로 Analytics 데이터 수집 설정](https://support.google.com/analytics/answer/9304153)
- [사이트에 Google Analytics 4 추가 [!DNL Universal Analytics]](https://support.google.com/analytics/answer/9744165)

### 2단계: Commerce 구성 완료

1. Commerce 스토어의 관리자에 로그인합니다.

1. _관리자_ 사이드바에서 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**(으)로 이동합니다.

1. 왼쪽 패널에서 **[!UICONTROL Sales]**&#x200B;을(를) 확장하고 **[!UICONTROL Google API]**&#x200B;을(를) 선택합니다.

1. ![&#x200B; 섹션에서 &#x200B;](../assets/icon-display-expand.png)확장 선택기&#x200B;**[!UICONTROL Google GTag]**&#x200B;를 확장합니다.

1. ![&#x200B; 하위 섹션의 &#x200B;](../assets/icon-display-expand.png)확장 선택기&#x200B;**[!UICONTROL Google Analytics4]**&#x200B;를 확장하고 다음을 수행합니다.

   - **[!UICONTROL Enable]**&#x200B;을(를) `Yes`(으)로 설정합니다.

   - **[!UICONTROL Account type]**&#x200B;을(를) `Google Analytics4`(으)로 둡니다.

   - **[!UICONTROL Measurement ID]**&#x200B;을(를) 입력하십시오. 자세한 내용은 [Google Analytics 도움말](https://support.google.com/analytics/answer/9539598)을 참조하세요.

   - 콘텐츠에 대한 A/B 테스트 및 기타 성능 테스트를 수행하려면 **콘텐츠 실험**&#x200B;을 `Yes`(으)로 설정하십시오.

   ![판매 구성 - Google Analytics 4용 Google API](../configuration-reference/sales/assets/google-api-gtag-google-analytics4.png){width="600" zoomable="yes"}

1. 완료되면 **[!UICONTROL Save Config]**&#x200B;을(를) 클릭합니다.

## Google 유니버설 애널리틱스

>[!IMPORTANT]
>
>2023년 7월 1일부터 표준 Universal Analytics 속성은 더 이상 데이터를 처리하지 않습니다. [!DNL Universal Analytics]을(를) 계속 사용하는 경우 앞으로 [Google Analytics 4 사용을 준비](https://support.google.com/analytics/answer/10759417)하는 것이 좋습니다.

### 1단계: Google Universal Analytics 설정

Google 웹 사이트를 방문하여 [Google Universal Analytics](https://support.google.com/analytics/answer/2817075?hl=en) 계정에 등록하십시오.

### 2단계: Commerce 구성 완료

1. Commerce 스토어의 관리자에 로그인합니다.

1. _관리자_ 사이드바에서 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**(으)로 이동합니다.

1. 왼쪽 패널에서 **[!UICONTROL Sales]**&#x200B;을(를) 확장하고 **[!UICONTROL Google API]**&#x200B;을(를) 선택합니다.

1. ![&#x200B; 섹션에서 &#x200B;](../assets/icon-display-expand.png)확장 선택기&#x200B;**[!UICONTROL Google Analytics]**&#x200B;를 확장하고 다음을 수행합니다.

   - **[!UICONTROL Enable]**&#x200B;을(를) `Yes`(으)로 설정합니다.

   - [!DNL Google Analytics] **[!UICONTROL Account Number]**&#x200B;을(를) 입력하십시오.

   - 콘텐츠에 대해 A/B 테스트 및 기타 성능 테스트를 수행하려면 **[!UICONTROL Content Experiments]**&#x200B;을(를) `Yes`(으)로 설정하십시오.

   ![판매 구성 - Google API - Google Analytics](../configuration-reference/sales/assets/google-api-analytics-ee.png){width="600" zoomable="yes"}

1. 완료되면 **[!UICONTROL Save Config]**&#x200B;을(를) 클릭합니다.

## 향상된 전자 상거래

향상된 Ecommerce는 고객의 쇼핑 및 구매 행동에 insight을 제공하는 [!DNL Google Universal Analytics]용 플러그인입니다. 고객이 장바구니에 품목을 추가하거나, 체크아웃 프로세스를 시작하거나, 구매를 완료하는 경우와 같이 향상된 전자 상거래 기능을 사용하여 주요 고객 활동에 대한 보고서를 생성할 수 있습니다. 구매하지 않고 카트를 버리는 쇼핑객의 패턴을 식별하고 분석할 수도 있습니다.

다음 지침은 향상된 전자 상거래 데이터 및 보고서를 생성하도록 [!DNL Google Tag Manager]을(를) 사용하여 [!DNL Universal Analytics]을(를) 구성하는 방법을 보여 줍니다.

### 1단계. Google 계정에 등록

1. [Google 태그 관리자](google-tag-manager.md) 계정에 등록하고 Commerce 구성을 완료하십시오.

1. 새 [Google Universal Analytics](https://support.google.com/analytics/answer/2817075?hl=en) 계정에 등록하십시오.

### 2단계. 향상된 전자 상거래 구성

1. Google Universal Analytics 계정에 로그인합니다.

1. 다음 설정으로 향상된 전자 상거래 분석에 대한 속성을 만듭니다.

   - 상태: 켜기
   - 관련 제품: 켜기
   - 향상된 전자 상거래 보고 활성화: 켜짐
   - 체크아웃 레이블 지정: (필수 아님)

1. 완료되면 **[!UICONTROL Submit]**&#x200B;을(를) 클릭합니다.

### 3단계. 태그 및 트리거 만들기

1. [!DNL Google Tag Manager] 계정에 로그인하고 다음 트리거를 만듭니다.

   | 이름 | 이벤트 유형 | 필터 |
   |--- |--- |--- |
   | `addToCart` | 사용자 지정 이벤트 |  |
   | `checkout` | 사용자 지정 이벤트 |  |
   | `checkout only` | 페이지 보기 | 페이지 URL이 RegEx /checkout/.* |
   | `checkoutOption` | 사용자 지정 이벤트 |  |
   | `gtm.dom` | 사용자 지정 이벤트 |  |
   | `productClick` | 사용자 지정 이벤트 |  |
   | `promotionClick` | 사용자 지정 이벤트 |  |
   | `removeFromCart` | 사용자 지정 이벤트 |  |

   >[!NOTE]
   >
   >[!UICONTROL Checkout] 이벤트는 기본 제공 Commerce 기본 결제 방법(예: `Check / Money Order` 및 `Cash On Delivery Payment`)에 대해서만 트리거됩니다. 이 이벤트는 외부 리소스에서 체크아웃으로 리디렉션하는 `PayPal checkout` 및 기타 외부 결제 방법에 대해 실행되지 않습니다.

1. 동일한 기본 구성으로 다음 Universal Analytics 태그를 만듭니다.

   - 범용 Analytics 태그

     | 이름 | 유형 | 트리거 실행 |
     |--- |--- |--- |
     | `Add to cart tracking` | 범용 분석 | 추가 장바구니 |
     | `Checkout option tracking` | 범용 분석 | checkoutOption |
     | `Checkout tracking` | 범용 분석 | 체크아웃 |
     | `Pageview tracking` | 범용 분석 | gtm.dom |
     | `Product click tracking` | 범용 분석 | productClick |
     | `Promo click tracking` | 범용 분석 | promotionClick |
     | `Remove from cart tracking` | 범용 분석 | removeFromCart |

   - 기본 태그 구성

     | 설정 | 값 |
     |--- |--- |
     | [!UICONTROL Product] | Google Analytics |
     | [!UICONTROL Tag Type] | 범용 분석 |
     | [!UICONTROL Tracking ID] | UA-XXX(Universal Analytics 계정의 추적 ID) |
     | [!UICONTROL Enable Enhanced Ecommerce Features] | True |
     | [!UICONTROL Use data layer] | True |
     | [!UICONTROL Use Debug version] | True |

1. 개별 추적 구성을 완료합니다.

   - 다음 **[!UICONTROL Add to Cart]** 추적 설정을 입력하십시오.

     | 설정 | 값 |
     |--- |--- |
     | [!UICONTROL Track Type] | 이벤트 |
     | [!UICONTROL Category] | Ecommerce |
     | [!UICONTROL Action] | 장바구니에 추가 |
     | [!UICONTROL Trigger] | 추가 장바구니 |

   - 다음 **[!UICONTROL Checkout option]** 추적 설정을 입력하십시오.

     | 설정 | 값 |
     |--- |--- |
     | [!UICONTROL Track Type] | 이벤트 |
     | [!UICONTROL Category] | Ecommerce |
     | [!UICONTROL Action] | 체크아웃 옵션 |
     | [!UICONTROL Trigger] | checkoutOption |

   - 다음 **[!UICONTROL PageView]** 추적 설정을 입력하십시오.

     | 설정 | 값 |
     |--- |--- |
     | [!UICONTROL Track Type] | 페이지 보기 |
     | [!UICONTROL Trigger] | gtm.dom |

   - 다음 **[!UICONTROL Product Click]** 추적 구성을 완료하십시오.

     | 설정 | 값 |
     |--- |--- |
     | [!UICONTROL Track Type] | 이벤트 |
     | [!UICONTROL Category] | Ecommerce |
     | [!UICONTROL Action] | 제품 클릭 |
     | [!UICONTROL Trigger] | productClick |

   - 다음 **[!UICONTROL Promotion Click]** 추적 구성을 완료하십시오.

     | 설정 | 값 |
     |--- |--- |
     | [!UICONTROL Track Type] | 이벤트 |
     | [!UICONTROL Category] | Ecommerce |
     | [!UICONTROL Action] | 프로모션 클릭 |
     | [!UICONTROL Trigger] | promotionClick |

   - 다음 **[!UICONTROL Remove from Cart]** 추적 구성을 완료하십시오.

     | 설정 | 값 |
     |--- |--- |
     | [!UICONTROL Track Type] | 이벤트 |
     | [!UICONTROL Category] | Ecommerce |
     | [!UICONTROL Action] | 장바구니에서 제거 |
     | [!UICONTROL Trigger] | removeFromCart |

1. 완료되면 **[!UICONTROL Preview]**&#x200B;을(를) 클릭하고 태그가 올바르게 작동하는지 확인하십시오.

1. 설정을 확인한 후 **[!UICONTROL Publish]**&#x200B;을(를) 클릭합니다.
