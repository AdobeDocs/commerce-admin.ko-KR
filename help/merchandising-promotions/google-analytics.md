---
title: '[!DNL Google Analytics]'
description: 을(를) 사용하는 방법 알아보기 [!DNL Google Analytics] 상거래 사이트에 대한 유용한 지표를 수집합니다.
exl-id: d4df2ef2-d67f-46bf-8569-cbee9dde77e4
feature: Marketing Tools, Integration
source-git-commit: eb0fe395020dbe2e2496aba13d2f5c2bf2d0fc27
workflow-type: tm+mt
source-wordcount: '735'
ht-degree: 0%

---

# [!DNL Google Analytics]

[!DNL Google Analytics] 에서는 오프라인 및 모바일 앱 상호 작용을 지원하고 진행 중인 업데이트에 액세스하여 추적을 위한 추가 사용자 정의 차원 및 지표를 정의할 수 있습니다. [!DNL Google Analytics] 4는 Google의 차세대 측정 솔루션으로, [!DNL Universal Analytics]. 2023년 7월 1일에 표준 Universal Analytics 속성은 새 히트 처리를 중지합니다.

>[!NOTE]
>
>비즈니스에 다음과 같은 개인 정보 보호 규정이 적용되는 경우 [일반 데이터 보호 규정](../getting-started/compliance-gdpr.md) 및/또는 [캘리포니아 소비자 개인 정보 보호법](../getting-started/compliance-ccpa.md), 참조 [Google 개인 정보 설정](google-tools.md#google-privacy-settings).

>[!IMPORTANT]
>
>을(를) 활성화하면 [쿠키 제한 모드](../getting-started/compliance-cookie-law.md), [!DNL Google Analytics] 은 방문자가 쿠키를 수락하지 않는 한 방문자에 대한 데이터를 수집하지 않습니다.

## [!DNL Google Analytics] 4

{{gtag-api-note}}

### 1단계: 설정 [!UICONTROL Google Analytics] 4

아직 이(가) 없는 경우 [!DNL Google Analytics] 4 사이트에 대해 설정하려면 다음 방법 중 하나를 따르십시오.

- [처음으로 Analytics 데이터 수집 설정](https://support.google.com/analytics/answer/9304153)
- [을 사용하여 사이트에 Google Analytics 4 추가 [!DNL Universal Analytics]](https://support.google.com/analytics/answer/9744165)

### 2단계: Commerce 구성 완료

1. Commerce 스토어의 관리자에 로그인합니다.

1. 다음에서 _관리자_ 사이드바, 이동 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. 왼쪽 패널에서 를 확장합니다. **[!UICONTROL Sales]** 및 선택 **[!UICONTROL Google API]**.

1. 확장 ![확장 선택기](../assets/icon-display-expand.png) 다음 **[!UICONTROL Google GTag]** 섹션.

1. 확장 ![확장 선택기](../assets/icon-display-expand.png) 다음 **[!UICONTROL Google Analytics4]** 하위 섹션을 만들고 다음을 수행합니다.

   - 설정 **[!UICONTROL Enable]** 끝 `Yes`.

   - 나가기 **[!UICONTROL Account type]** 다음으로: `Google Analytics4`.

   - 다음을 입력하십시오. **[!UICONTROL Measurement ID]**. 자세한 내용은 다음을 참조하십시오. [Google Analytics 도움말](https://support.google.com/analytics/answer/9539598).

   - 콘텐츠에 대해 A/B 테스트 및 기타 성능 테스트를 수행하려면 다음을 설정하십시오. **콘텐츠 실험** 끝 `Yes`.

   ![영업 구성 - Google Analytics 4용 Google API](../configuration-reference/sales/assets/google-api-gtag-google-analytics4.png){width="600" zoomable="yes"}

1. 완료되면 다음을 클릭하십시오. **[!UICONTROL Save Config]**.

## Google 유니버설 애널리틱스

>[!IMPORTANT]
>
>2023년 7월 1일부터 표준 Universal Analytics 속성은 더 이상 데이터를 처리하지 않습니다. 여전히 을(를) [!DNL Universal Analytics], 다음 작업을 수행하는 것이 좋습니다. [Google Analytics 4 사용 준비](https://support.google.com/analytics/answer/10759417) 앞으로 나아갑니다.

### 1단계: Google Universal Analytics 설정

Google 웹 사이트를 방문하여 [Google 유니버설 애널리틱스][1] 계정입니다.

### 2단계: Commerce 구성 완료

1. Commerce 스토어의 관리자에 로그인합니다.

1. 다음에서 _관리자_ 사이드바, 이동 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. 왼쪽 패널에서 를 확장합니다. **[!UICONTROL Sales]** 및 선택 **[!UICONTROL Google API]**.

1. 확장 ![확장 선택기](../assets/icon-display-expand.png) 다음 **[!UICONTROL Google Analytics]** 섹션을 참조하고 다음을 수행합니다.

   - 설정 **[!UICONTROL Enable]** 끝 `Yes`.

   - 다음을 입력하십시오. [!DNL Google Analytics] **[!UICONTROL Account Number]**.

   - 콘텐츠에 대해 A/B 테스트 및 기타 성능 테스트를 수행하려면 다음을 설정하십시오. **[!UICONTROL Content Experiments]** 끝 `Yes`.

   ![영업 구성 - Google API - Google Analytics](../configuration-reference/sales/assets/google-api-analytics-ee.png){width="600" zoomable="yes"}

1. 완료되면 다음을 클릭하십시오. **[!UICONTROL Save Config]**.

## 향상된 전자 상거래

향상된 전자 상거래 는 용 플러그인입니다. [!DNL Google Universal Analytics] 이를 통해 고객의 쇼핑 및 구매 행동에 대한 통찰력을 얻을 수 있습니다. 고객이 장바구니에 품목을 추가하거나, 체크아웃 프로세스를 시작하거나, 구매를 완료하는 경우와 같이 향상된 전자 상거래 기능을 사용하여 주요 고객 활동에 대한 보고서를 생성할 수 있습니다. 구매하지 않고 카트를 버리는 쇼핑객의 패턴을 식별하고 분석할 수도 있습니다.

다음 지침은 구성 방법을 보여 줍니다 [!DNL Google Tag Manager] 포함 [!DNL Universal Analytics] 향상된 전자 상거래 데이터 및 보고서를 생성합니다.

### 1단계. Google 계정에 등록

1. 에 등록 [Google 태그 관리자](google-tag-manager.md) 계정을 입력한 다음 상거래 구성을 완료합니다.

1. 새 항목에 등록 [Google 유니버설 애널리틱스][1] 계정입니다.

### 2단계. 향상된 전자 상거래 구성

1. Google Universal Analytics 계정에 로그인합니다.

1. 다음 설정으로 향상된 전자 상거래 분석에 대한 속성을 만듭니다.

   - 상태: 켜기
   - 관련 제품: 켜기
   - 향상된 전자 상거래 보고 활성화: 켜짐
   - 체크아웃 레이블 지정: (필수 아님)

1. 완료되면 다음을 클릭하십시오. **[!UICONTROL Submit]**.

### 3단계. 태그 및 트리거 만들기

1. 다음에 로그인 [!DNL Google Tag Manager] 계정을 만들고 다음 트리거를 만듭니다.

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
   >다음 [!UICONTROL Checkout] 기본 상거래 기본 결제 방법에 대해서만 이벤트가 트리거됩니다(예: `Check / Money Order` 및 `Cash On Delivery Payment`). 이 이벤트는 다음에 대해 실행되지 않습니다. `PayPal checkout` 외부 자원에서 체크아웃으로 리디렉션하는 기타 외부 결제 방법.

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

   - 다음을 입력합니다 **[!UICONTROL Add to Cart]** 추적 설정:

     | 설정 | 값 |
     |--- |--- |
     | [!UICONTROL Track Type] | Event |
     | [!UICONTROL Category] | Ecommerce |
     | [!UICONTROL Action] | 장바구니에 추가 |
     | [!UICONTROL Trigger] | 추가 장바구니 |

   - 다음을 입력합니다 **[!UICONTROL Checkout option]** 추적 설정:

     | 설정 | 값 |
     |--- |--- |
     | [!UICONTROL Track Type] | Event |
     | [!UICONTROL Category] | Ecommerce |
     | [!UICONTROL Action] | 체크아웃 옵션 |
     | [!UICONTROL Trigger] | checkoutOption |

   - 다음을 입력합니다 **[!UICONTROL PageView]** 추적 설정:

     | 설정 | 값 |
     |--- |--- |
     | [!UICONTROL Track Type] | 페이지 보기 |
     | [!UICONTROL Trigger] | gtm.dom |

   - 다음을 완료하십시오 **[!UICONTROL Product Click]** 추적 구성:

     | 설정 | 값 |
     |--- |--- |
     | [!UICONTROL Track Type] | Event |
     | [!UICONTROL Category] | Ecommerce |
     | [!UICONTROL Action] | 제품 클릭 |
     | [!UICONTROL Trigger] | productClick |

   - 다음을 완료하십시오 **[!UICONTROL Promotion Click]** 추적 구성:

     | 설정 | 값 |
     |--- |--- |
     | [!UICONTROL Track Type] | Event |
     | [!UICONTROL Category] | Ecommerce |
     | [!UICONTROL Action] | 프로모션 클릭 |
     | [!UICONTROL Trigger] | promotionClick |

   - 다음을 완료하십시오 **[!UICONTROL Remove from Cart]** 추적 구성:

     | 설정 | 값 |
     |--- |--- |
     | [!UICONTROL Track Type] | Event |
     | [!UICONTROL Category] | Ecommerce |
     | [!UICONTROL Action] | 장바구니에서 제거 |
     | [!UICONTROL Trigger] | removeFromCart |

1. 완료되면 다음을 클릭하십시오. **[!UICONTROL Preview]** 태그가 올바르게 작동하는지 확인하십시오.

1. 설정을 확인한 후 **[!UICONTROL Publish]**.


[1]: https://support.google.com/analytics/answer/2817075?hl=en
