---
title: '[!UICONTROL Sales] &gt; [!UICONTROL Google API]'
description: 에서 구성 설정을 검토합니다. [!UICONTROL Sales] &gt; [!UICONTROL Google API] 상거래 관리자의 페이지입니다.
exl-id: 5031ad3d-1c9a-4bc6-9bfa-683414dca979
feature: Configuration, Marketing Tools
source-git-commit: b710c0368dc765e3bf25e82324bffe7fb8192dbf
workflow-type: tm+mt
source-wordcount: '978'
ht-degree: 0%

---

# [!UICONTROL Sales] > [!UICONTROL Google API]

{{config}}

## [!UICONTROL Google Analytics]

![Google Analytics](./assets/google-api-analytics-ee.png)<!-- zoom -->

<!-- [Google Analytics](https://docs.magento.com/user-guide/marketing/google-universal-analytics.html) -->

| 필드 | [범위](../../getting-started/websites-stores-views.md#scope-settings) | 설명 |
| ----- | ------------------------------------------ | ----------- |
| [!UICONTROL Enable] | 스토어 뷰 | 사용 [!DNL Google Analytics] 스토어용. 옵션: `Yes` / `No` |
| [!UICONTROL Account Type] | 스토어 뷰 | ![Adobe Commerce](../../assets/adobe-logo.svg) (Adobe Commerce만 해당) Google Analytics 계정 유형에 따라 구성 옵션을 결정합니다. 옵션: Universal Analytics(기본값) / Google Tag Manager |
| [!UICONTROL Account Number] | 스토어 뷰 | 다음을 만들 때 지정된 계정 번호 또는 추적 코드 [!DNL Google Analytics] 계정입니다. |
| [!UICONTROL Anonymize IP] | 스토어 뷰 | IP 주소에서 식별 정보가 제거되는지 여부를 결정합니다. [!DNL Google Analytics] 결과. |
| [!UICONTROL Enable Content Experiments] | 스토어 뷰 | 활성화 [Google 콘텐츠 실험](https://support.google.com/analytics/answer/9366791?hl=en&amp;ref_topic=1745207): 동일한 페이지의 서로 다른 버전을 최대 10개까지 테스트하는 데 사용할 수 있습니다. 옵션: `Yes` / `No` |

{style="table-layout:auto"}

## [!UICONTROL Google Analytics - Google Tag Manager]

{{ee-feature}}

![Google Analytics - Google Tag Manager 계정 유형](./assets/google-api-analytics-tag-manager.png)<!-- zoom -->

날짜 **[!UICONTROL Account Type]** 이(가) (으)로 설정됨 `Google Tag Manager`에는 추가 필드가 표시됩니다.

| 필드 | [범위](../../getting-started/websites-stores-views.md#scope-settings) | 설명 |
| ----- | ------------------------------------------ | ----------- |
| [!UICONTROL Container ID] | 스토어 뷰 | 에 대한 고유 ID [!DNL Google Tag Manager] 컨테이너. 이 값은 일반적으로 다음으로 시작합니다. `GTM-`. 이 ID는 다음에 있습니다. [!DNL Google Tag Manager] 계정입니다. If [!DNL Google Tag Manager] 이(가) 이미 설치되고 스토어에 대해 구성되었습니다. 컨테이너 ID가 이 필드에 자동으로 표시됩니다. |
| [!UICONTROL List property for the catalog page] | 스토어 뷰 | 다음 항목을 식별합니다. [!DNL Google Tag Manager] 카탈로그 페이지와 연결된 속성입니다. 기본값: `Catalog Page` |
| [!UICONTROL List property for the cross-sell block] | 스토어 뷰 | 다음 항목을 식별합니다. [!DNL Google Tag Manager] 크로스셀 블록과 연결된 속성입니다. 기본값: `Cross-sell` |
| [!UICONTROL List property for the up-sell block] | 스토어 뷰 | 다음 항목을 식별합니다. [!DNL Google Tag Manager] 업셀 블록과 연결된 속성입니다. 기본값: `Up-sell` |
| [!UICONTROL List property for the related products block] | 스토어 뷰 | 다음 항목을 식별합니다. [!DNL Google Tag Manager] 관련 제품 블록과 연결된 속성입니다. 기본값: `Related Products` |
| [!UICONTROL List property for the search results page] | 스토어 뷰 | 다음 항목을 식별합니다. [!DNL Google Tag Manager] 검색 결과 페이지와 연결된 속성입니다. 기본값: `Search Results` |
| [!UICONTROL 'Internal Promotions' for promotions field "Label"] | 스토어 뷰 | 다음 항목을 식별합니다. [!DNL Google Tag Manager] 내부 프로모션의 레이블과 연결된 속성입니다. 기본값: `Label` |

{style="table-layout:auto"}

## [!UICONTROL Google AdWords]

![Google AdWords](./assets/google-api-google-adwords.png)<!-- zoom -->

<!-- [Google AdWords](https://docs.magento.com/user-guide/marketing/google-adwords.html) -->

| 필드 | [범위](../../getting-started/websites-stores-views.md#scope-settings) | 설명 |
| ----- | ------------------------------------------ | ----------- |
| [!UICONTROL Enable] | 스토어 뷰 | 스토어에 대해 Google AdWords를 활성화합니다. 옵션: `Yes` / `No` |
| [!UICONTROL Conversion ID] | 스토어 뷰 | Google AdWords 계정의 ID입니다. |
| [!UICONTROL Conversion Language] | 스토어 뷰 | AdWords 변환에 사용되는 언어입니다. 옵션: `All available languages` |
| [!UICONTROL Conversion Format] | 스토어 뷰 | 의 형식을 결정합니다 [!DNL Google Site Stats] 전환 페이지에 표시되는 알림입니다. 알림은 방문자의 방문을 추적하는 데 사용되는 쿠키에 대해 방문자에게 알려주는 페이지에 연결됩니다. 이 숫자 값은 다음에 할당됩니다. `google_conversion_format` 변수를 채우는 방법에 따라 페이지를 순서대로 표시합니다. 자세한 내용은 다음을 참조하십시오. [전환 추적 정보](https://support.google.com/google-ads/answer/1722022?hl=en) Google 웹 사이트에서. 옵션: <br/>**`1`**- 한 줄 알림을 표시합니다.<br/>**`2`** - (기본값) 2줄 알림을 표시합니다. <br/>**`3`**- 고객 알림을 표시하지 않습니다. |
| [!UICONTROL Conversion Color] | 스토어 뷰 | 전환 레이블의 색상을 결정합니다. 사용 [색상 피커](https://www.w3schools.com/colors/colors_picker.asp) 을 눌러 16진수 값을 선택합니다. 이 16진수 값은 `google_conversion_color` 변수를 채우는 방법에 따라 페이지를 순서대로 표시합니다. 예: ffffff  `var google_conversion_color = "ffffff";` |
| [!UICONTROL Conversion Label] | 스토어 뷰 | 텍스트 레이블은 [!DNL Google Site Stats] 알림입니다. 이 텍스트 문자열은 `~` 변수를 채우는 방법에 따라 페이지를 순서대로 표시합니다. 예: &quot;쇼핑해 주셔서 감사합니다!&quot; |
| [!UICONTROL Conversion Value Type] | 스토어 뷰 | 전환이 발생하는 시기를 결정하는 데 사용되는 값 유형을 지정합니다. 옵션: <br/>**`Dynamic`**- 동적 주문 금액을 기준으로 전환이 발생했는지 확인합니다.<br/>**`Constant`** - 입력한 값을 기반으로 전환이 발생했는지 확인합니다. |
| [!UICONTROL Conversion Value] | 스토어 뷰 | 다음에 사용되는 값을 지정합니다. _[!UICONTROL Constant]_전환 값 유형입니다. |
| [!UICONTROL Send Order Currency] | 스토어 뷰 | AdWords(기본 통화가 다른 웹 사이트의 경우)에서 거래별 통화 전환 값을 활성화합니다. |

{style="table-layout:auto"}

## [!UICONTROL Google GTag]

{{gtag-api-note}}

### [!UICONTROL Google Analytics4]

![GOOGLE ANALYTICS4](./assets/google-api-gtag-google-analytics4.png)<!-- zoom -->

<!-- [Google Analytics4](https://docs.magento.com/user-guide/marketing/google-universal-analytics.html) -->

| 필드 | [범위](../../getting-started/websites-stores-views.md#scope-settings) | 설명 |
| ----- | ------------------------------------------ | ----------- |
| [!UICONTROL Enable] | 스토어 뷰 | 스토어에 대해 Google Analytics 4를 활성화합니다. 옵션: `Yes` / `No` |
| [!UICONTROL Account Type] | 스토어 뷰 | ![Adobe Commerce](../../assets/adobe-logo.svg) (Adobe Commerce만 해당) Google Analytics 계정 유형에 따라 구성 옵션을 결정합니다. 옵션: `Google Analytics4` (기본값) / `Google Tag Manager` |
| [!UICONTROL Measurement ID] | 스토어 뷰 | Google Analytics 계정을 만들 때 지정된 계정 번호 또는 추적 코드입니다. |
| [!UICONTROL Anonymize IP] | 스토어 뷰 | Google Analytics 결과에 나타나는 IP 주소에서 식별 정보가 제거되는지 여부를 결정합니다. |
| [!UICONTROL Enable Content Experiments] | 스토어 뷰 | 활성화 [Google 콘텐츠 실험](https://support.google.com/analytics/answer/9366791?hl=en&amp;ref_topic=1745207): 동일한 페이지의 서로 다른 버전을 최대 10개까지 테스트하는 데 사용할 수 있습니다. 옵션: `Yes` / `No` |

{style="table-layout:auto"}

### [!UICONTROL Google Analytics4 - Google Tag Manager]

{{ee-feature}}

![Google Analytics4 - Google Tag Manager 계정 유형](./assets/google-api-gtag-google-analytics4-gtm.png)<!-- zoom -->

날짜 **[!UICONTROL Account Type]** 이(가) (으)로 설정됨 `Google Tag Manager`에는 추가 필드가 표시됩니다.

| 필드 | [범위](../../getting-started/websites-stores-views.md#scope-settings) | 설명 |
| ----- | ------------------------------------------ | ----------- |
| [!UICONTROL Container Id] | 스토어 뷰 | 에 대한 고유 ID [!DNL Google Tag Manager] 컨테이너. 이 값은 일반적으로 다음으로 시작합니다. `GTM-`. 이 ID는 Google 탭 관리자 계정에 있습니다. If [!DNL Google Tag Manager] 이(가) 이미 설치되고 스토어에 대해 구성되었습니다. 컨테이너 ID가 이 필드에 자동으로 표시됩니다. |
| [!UICONTROL List property for the catalog page] | 스토어 뷰 | 다음 항목을 식별합니다. [!DNL Google Tag Manager] 카탈로그 페이지와 연결된 속성입니다. 기본값: `Catalog Page` |
| [!UICONTROL List property for the cross-sell block] | 스토어 뷰 | 다음 항목을 식별합니다. [!DNL Google Tag Manager] 크로스셀 블록과 연결된 속성입니다. 기본값: `Cross-sell` |
| [!UICONTROL List property for the up-sell block] | 스토어 뷰 | 다음 항목을 식별합니다. [!DNL Google Tag Manager] 업셀 블록과 연결된 속성입니다. 기본값: `Up-sell` |
| [!UICONTROL List property for the related products block] | 스토어 뷰 | 다음 항목을 식별합니다. [!DNL Google Tag Manager] 관련 제품 블록과 연결된 속성입니다. 기본값: `Related Products` |
| [!UICONTROL List property for the search results page] | 스토어 뷰 | 다음 항목을 식별합니다. [!DNL Google Tag Manager] 검색 결과 페이지와 연결된 속성입니다. 기본값: `Search Results` |
| [!UICONTROL 'Internal Promotions' for promotions field "Label"] | 스토어 뷰 | 다음 항목을 식별합니다. [!DNL Google Tag Manager] 내부 프로모션의 레이블과 연결된 속성입니다. 기본값: `Label` |

{style="table-layout:auto"}

### [!UICONTROL Google AdWords]

![Google AdWords](./assets/google-api-gtag-google-adwords.png)<!-- zoom -->

<!-- -- Google AdWords](https://docs.magento.com/user-guide/marketing/google-adwords.html) -->

| 필드 | [범위](../../getting-started/websites-stores-views.md#scope-settings) | 설명 |
| ----- | ------------------------------------------ | ----------- |
| [!UICONTROL Enable] | 스토어 뷰 | 스토어에 대해 Google AdWords를 활성화합니다. 옵션: `Yes` / `No` |
| [!UICONTROL Conversion ID] | 스토어 뷰 | Google AdWords 계정의 ID입니다. |
| [!UICONTROL Conversion Language] | 스토어 뷰 | AdWords 변환에 사용되는 언어입니다. 옵션: 사용 가능한 모든 언어 |
| [!UICONTROL Conversion Format] | 스토어 뷰 | 전환 페이지에 나타나는 Google 사이트 상태 알림의 형식을 결정합니다. 알림은 방문자의 방문을 추적하는 데 사용되는 쿠키에 대해 방문자에게 알려주는 페이지에 연결됩니다. 이 숫자 값은 다음에 할당됩니다. `google_conversion_format` 변수를 채우는 방법에 따라 페이지를 순서대로 표시합니다. 자세한 내용은 다음을 참조하십시오. [전환 추적 정보](https://support.google.com/google-ads/answer/1722022?hl=en) Google 웹 사이트에서. 옵션: <br/>**`1`**- 한 줄 알림을 표시합니다.<br/>**`2`** - (기본값) 2줄 알림을 표시합니다. <br/>**`3`**- 고객 알림을 표시하지 않습니다. |
| [!UICONTROL Conversion Color] | 스토어 뷰 | 전환 레이블의 색상을 결정합니다. 사용 [색상 피커](https://www.w3schools.com/colors/colors_picker.asp) 을 눌러 16진수 값을 선택합니다. 이 16진수 값은 `google_conversion_color` 변수를 채우는 방법에 따라 페이지를 순서대로 표시합니다. 예: ffffff  `var google_conversion_color = "ffffff";` |
| [!UICONTROL Conversion Label] | 스토어 뷰 | Google 사이트 상태 알림과 함께 표시되는 텍스트 레이블입니다. 이 텍스트 문자열은 `~` 변수를 채우는 방법에 따라 페이지를 순서대로 표시합니다. 예: &quot;쇼핑해 주셔서 감사합니다!&quot; |
| [!UICONTROL Conversion Value Type] | 스토어 뷰 | 전환이 발생하는 시기를 결정하는 데 사용되는 값 유형을 지정합니다. 옵션: <br/>**`Dynamic`**- 동적 주문 금액을 기준으로 전환이 발생했는지 확인합니다.<br/>**`Constant`** - 입력한 값을 기반으로 전환이 발생했는지 확인합니다. |
| [!UICONTROL Conversion Value] | 스토어 뷰 | 다음에 사용되는 값을 지정합니다. _[!UICONTROL Constant]_전환 값 유형입니다. |
| [!UICONTROL Send Order Currency] | 스토어 뷰 | AdWords(기본 통화가 다른 웹 사이트의 경우)에서 거래별 통화 전환 값을 활성화합니다. |

{style="table-layout:auto"}
