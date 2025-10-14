---
title: '[!DNL Google Tag Manager]'
description: ' [!DNL Google Tag Manager] 을(를) 사용하여 Adobe Commerce 사이트의 마케팅 캠페인 이벤트와 관련된 많은 태그(코드 조각)를 관리하는 방법을 알아봅니다.'
exl-id: 9c24239b-9efd-42ee-9b99-5a194f3c4347
feature: Marketing Tools, Integration
source-git-commit: 9c25196367023a44fa76e441d485693493a4c058
workflow-type: tm+mt
source-wordcount: '1437'
ht-degree: 0%

---

# [!DNL Google Tag Manager]

{{ee-feature}}

[!DNL Google Tag Manager]은(는) 마케팅 캠페인 이벤트와 관련된 다양한 태그(코드 조각)를 효율적으로 관리하고 배포하는 데 도움이 되는 강력한 도구입니다. [!DNL Google Tag Manager]에서는 사이트에 추적 태그를 추가하여 대상자를 측정하거나 검색 엔진 마케팅 이니셔티브를 개인화, 리타겟팅 또는 수행할 수 있습니다.

[!DNL Google Tag Manager]은(는) 데이터와 이벤트를 [!DNL Google Analytics], Enhanced Ecommerce 및 다른 서드파티 분석 솔루션으로 직접 전송하여 사이트, 제품 및 프로모션의 성과를 명확하게 파악합니다.

이 프로세스를 계속하려면 [!DNL Google Analytics] 및 [!DNL Tag Manager] 계정이 있어야 합니다. 다음 지침은 Google 계정을 구성하고, Commerce 스토어를 구성하고, 태그를 만드는 과정을 안내합니다.

>[!NOTE]
>
>비즈니스에 [일반 데이터 보호 규정](../getting-started/compliance-gdpr.md) 및/또는 [캘리포니아 소비자 개인정보 보호법](../getting-started/compliance-ccpa.md)과 같은 개인정보 보호 규정이 적용되는 경우 [Google 개인정보 보호 설정](google-tools.md#google-privacy-settings)을 참조하십시오.

## 1단계. [!DNL Google Analytics] 계정 구성

시작하는 데 필요한 기본 사항은 Google 도움말의 [사이트 검색 설정](https://support.google.com/analytics/answer/1012264)을 참조하십시오. [Google Analytics](https://support.google.com/analytics/answer/9304153) 및 [Google 태그 관리자](https://support.google.com/tagmanager/answer/6102821)용 Google 안내서도 참조하세요.

1. [!DNL Google Analytics] 계정에 로그인합니다.

1. **[!UICONTROL Internal Site Search Tracking]**&#x200B;을(를) 사용하려면 다음을 수행하십시오.

   - **[!UICONTROL Select View]** > **[!UICONTROL View Settings]**(으)로 이동합니다.

   - **[!UICONTROL Site Search Tracking]**&#x200B;을(를) `On`(으)로 설정합니다.

   - **[!UICONTROL Query]** 매개 변수를 `q`(으)로 설정합니다.

   - 완료되면 설정을 **[!UICONTROL Save]**&#x200B;합니다.

1. 디스플레이 기능을 활성화하려면 다음을 수행합니다.

   - **[!UICONTROL Property Settings]**&#x200B;을(를) 선택하십시오.

   - _[!UICONTROL Advertising Features]_&#x200B;에서&#x200B;**[!UICONTROL Enable Demographics and Interest Reports]**&#x200B;을(를) `On`(으)로 설정합니다.

   - **[!UICONTROL Save]** 설정입니다.

1. 전자 상거래 추적을 활성화하려면 다음 작업을 수행하십시오.

   - **[!UICONTROL Select View]** > **[!UICONTROL Ecommerce Settings]**(으)로 이동합니다.

   - **[!UICONTROL Enable Ecommerce]**&#x200B;을(를) `On`(으)로 설정합니다.

   - **[!UICONTROL Enable Enhanced Ecommerce Reporting]**&#x200B;을(를) `On`(으)로 설정합니다.

   - **[!UICONTROL Save]** 설정입니다.

1. 페이지를 다시 로드하고 모든 설정이 `On` 상태로 유지되는지 확인하십시오.

   >[!NOTE]
   >
   >일부 설정이 `On`이(가) 아닌 경우 이전 단계를 반복하여 페이지를 저장하고 다시 로드합니다. 모든 설정이 `On`(으)로 설정될 때까지 이 프로세스를 반복합니다.

## 2단계. [!DNL Google Tag Manager] 계정 구성

다음 지침은 기본 설정으로 새 컨테이너를 구성하는 방법을 보여 줍니다. 샘플 [Composer](https://developer.adobe.com/commerce/php/development/composer/) 구성(.json) 파일을 사용하여 프로세스를 단순화하고 가져오기를 통해 새 컨테이너에서 태그를 생성합니다. 이 예제에서는 기존 컨테이너를 수정하지 않고 컨테이너를 만드는 것이 좋습니다.

>[!NOTE]
>
>자세한 내용은 Google의 [컨테이너 내보내기 및 가져오기](https://support.google.com/tagmanager/answer/6106997)를 참조하십시오. 이러한 지침은 새 컨테이너에서 샘플 JSON을 가져오는 방법에 대한 설명을 제공합니다.

1. 연결된 파일 [GTM_M2_Config_json.txt](./assets/GTM_M2_Config_json.txt)를 다운로드하고 편집기에서 파일을 열고 `GTM_M2_Config.json`(으)로 저장합니다.

   json 파일이 [!DNL Google Tag Manager]에 바로 업로드됩니다.

1. **[!UICONTROL Admin]** > **[!UICONTROL Container]** > **[!UICONTROL Import Container]**(으)로 이동합니다.

1. **[!UICONTROL Choose container file]**&#x200B;을(를) 클릭하고 json 파일을 선택하십시오.

1. **[!UICONTROL Choose workspace]**&#x200B;에서 **[!UICONTROL New]**&#x200B;을(를) 클릭합니다.

1. 제목과 설명을 입력한 다음 **[!UICONTROL Save]**&#x200B;을(를) 클릭합니다.

1. 파일을 가져오려면 다음 작업 중 하나를 선택합니다.

   - 새 컨테이너에 대해 **[!UICONTROL Overwrite]** 옵션을 선택해야 합니다.

   - 기존 컨테이너를 사용하는 경우 **[!UICONTROL Merge]** 옵션을 선택해야 합니다.

1. 태그, 트리거 및 변수를 검토하려면 **[!UICONTROL Preview]**&#x200B;을(를) 클릭하십시오.

1. 변수에서 참조되는 **[!UICONTROL Google Analytics ID]**&#x200B;을(를) 편집하려면 다음을 수행하십시오.

   - **[!UICONTROL Variables]** > **[!UICONTROL User-Defined Variables]**(으)로 이동합니다.

   - **[!UICONTROL Google Analytics]**&#x200B;을(를) 선택하고 자리 표시자(`UA-xxxxxx-x`)를 **[!UICONTROL GA ID]**(으)로 업데이트하십시오.

1. 태그, 트리거 및 변수를 새 컨테이너에 추가하는 방법에 대한 Google의 지침을 따릅니다.

   사용할 다른 컨테이너에 설정이 있는 경우 새 컨테이너로 이동할 수 있습니다.

1. 완료되면 **[!UICONTROL Confirm]**&#x200B;을(를) 클릭합니다.

1. 새 컨테이너를 게시하려면 Google의 지침을 따르십시오.

## 3단계. 스토어 구성

{{gtag-api-note}}

1. Commerce 스토어의 관리자에 로그인합니다.

1. _관리자_ 사이드바에서 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**(으)로 이동합니다.

1. 왼쪽 패널에서 **[!UICONTROL Sales]**&#x200B;을(를) 확장하고 **[!UICONTROL Google API]**&#x200B;을(를) 선택합니다.

1. ![&#x200B; 섹션에서 &#x200B;](../assets/icon-display-expand.png)확장 선택기&#x200B;**[!UICONTROL Google Analytics]**&#x200B;를 확장하고 다음을 구성합니다.

   ![판매 구성 - Google Analytics](../configuration-reference/sales/assets/google-api-analytics-tag-manager.png){width="600" zoomable="yes"}

   - **[!UICONTROL Enable]**&#x200B;을(를) `Yes`(으)로 설정합니다.

   - **[!UICONTROL Account type]**&#x200B;을(를) `Google Tag Manager`(으)로 설정합니다.

   - **[!UICONTROL Container ID]** 필드에 GTM ID(`GTM-xxxxxx`)를 입력합니다.

   - 콘텐츠 실험에 Google Analytics도 사용하는 경우 **콘텐츠 실험 사용**&#x200B;을(를) `Yes`(으)로 설정하십시오.

   - 나머지 필드에 기본값을 사용합니다.

1. 완료되면 **[!UICONTROL Save Config]**&#x200B;을(를) 클릭합니다.

1. [!DNL Google Tag Manager] 설정을 테스트하고 모든 설정이 올바르게 작동하는지 확인하십시오.

>[!NOTE]
>
>각 컨테이너는 하나의 웹 사이트와 연결되어 있으며 계정당 하나의 컨테이너만 있으면 됩니다. 다중 사이트 Commerce 인스턴스가 있는 경우 별도의 컨테이너가 필요합니다.

## 필드 설명

| 필드 | 범위 | 설명 |
|--- |--- |--- |
| [!UICONTROL Enable] | 스토어 뷰 | Google Analytics Enhanced Ecommerce를 사용하여 스토어의 활동을 분석할 수 있는지 여부를 결정합니다. 옵션: `Yes` / `No` |
| [!UICONTROL Account type] | 스토어 뷰 | 저장소 활동 및 트래픽을 모니터링하는 데 사용되는 Google 추적 코드를 결정합니다. 옵션: `Google Analytics` / `Google Tag Manager` |
| [!UICONTROL Anonymize IP] | 스토어 뷰 | Google Analytics 결과에 나타나는 IP 주소에서 식별 정보가 제거되는지 여부를 결정합니다. |
| [!UICONTROL Container Id] | 스토어 뷰 | 저장소에 대해 [!DNL Google Tag Manager]이(가) 이미 설치 및 구성된 경우 컨테이너 ID가 이 필드에 자동으로 표시됩니다. |
| [!UICONTROL List property for the catalog page] | 스토어 뷰 | 카탈로그 페이지와 연결된 태그 관리자 속성을 식별합니다. 기본값: `Catalog Page` |
| [!UICONTROL List property for the cross-sell block] | 스토어 뷰 | 크로스셀 블록과 연결된 Tag Manager 속성을 식별합니다. 기본값: `Cross-sell` |
| [!UICONTROL List property for the up-sell block] | 스토어 뷰 | 업셀 블록과 연결된 Tag Manager 속성을 식별합니다. 기본값: `Up-sell` |
| [!UICONTROL List property for the related products block] | 스토어 뷰 | 관련 제품 블록과 연결된 Tag Manager 속성을 식별합니다. 기본값: `Related Products` |
| [!UICONTROL List property for the search results page] | 스토어 뷰 | 검색 결과 페이지와 연결된 태그 관리자 속성을 식별합니다. 기본값: `Search Results` |
| [!UICONTROL "Internal Promotions" for promotions field "Label"] | 스토어 뷰 | 내부 프로모션의 레이블과 연결된 태그 관리자 속성을 식별합니다. 기본값: `Label` |

{style="table-layout:auto"}

## 전환 추적을 위한 태그 만들기

Google AdWords 계정이 있는 경우 전환을 추적하는 태그를 만들 수 있습니다. 다음 예제에서는 [!DNL Google Tag Manager]과(와) [!DNL Google Analytics]을(를) 모두 사용하여 스토어의 전환 _성공_ 페이지에서 실행되는 태그를 만드는 방법을 보여 줍니다.

### 1단계. 태그 만들기

1. [!DNL Google Tag Manager] 계정에 로그인하고 스토어에 대해 만든 컨테이너에 대한 링크를 클릭합니다.

1. **[!UICONTROL New Tag]** 상자에서 **[!UICONTROL Add a new tag]**&#x200B;을(를) 클릭합니다.

1. AdWords 계정에서 다음 정보를 가져옵니다.

   - 전환 ID
   - 전환 레이블

   도움이 필요하면 Google의 [지원 사이트](https://support.google.com/tagmanager/answer/6105160)를 방문하세요.

1. [!DNL Google Tag Manager] 대시보드에서 **[!UICONTROL Google AdWords]**&#x200B;을(를) 클릭하고 다음을 수행합니다.

   - 제목 자리 표시자를 클릭하고 새 태그의 이름을 입력합니다.

   - **[!UICONTROL Choose Product]**&#x200B;에서 **[!UICONTROL Google AdWords]**&#x200B;을(를) 선택합니다.

   - _[!UICONTROL Choose a Tag Type]_&#x200B;에서&#x200B;**[!UICONTROL AdWords Conversion Tracking]**&#x200B;을(를) 선택하고&#x200B;**[!UICONTROL Continue]**&#x200B;을(를) 클릭합니다.

1. AdWords 계정에서 **[!UICONTROL Conversion ID]** 및 **[!UICONTROL Conversion Label]**&#x200B;을(를) 입력하고 **[!UICONTROL Continue]**&#x200B;을(를) 클릭합니다.

### 2단계. 규칙 만들기

[!DNL Google Tag Manager] 대시보드에서 계속하는 다음 단계는 전환 페이지에서 태그를 실행하는 규칙을 만드는 것입니다.

1. **[!UICONTROL Fire On]**&#x200B;에서 **[!UICONTROL Some Pages]**&#x200B;을(를) 클릭합니다.

1. _[!UICONTROL Choose Pages]_&#x200B;섹션에서 다음 설정을 완료합니다.

   - **[!UICONTROL Name]** - 페이지 설명의 이름을 입력합니다.

   - **[!UICONTROL Variable]** `url`

   - **작업** - `matches RegEx`

     자세한 내용은 Google 태그 관리자 도움말에서 [Regex 및 CSS 선택기 연산자](https://support.google.com/tagmanager/answer/7679109)를 참조하십시오.

   - **[!UICONTROL Value]** - `checkout/success.*`

1. 녹색 확인란을 선택하고 **[!UICONTROL Save]**&#x200B;을(를) 클릭합니다.

   설정한 트리거는 [실행] 섹션에 파란색 단추로 나타납니다.

1. 완료되면 **[!UICONTROL Save Tag]**&#x200B;을(를) 클릭합니다.

### 3단계. 미리보기 및 게시

프로세스의 다음 단계는 태그를 미리 보는 것입니다. 태그를 미리 볼 때마다 버전의 스냅샷이 저장됩니다. 결과가 만족스러우면 사용할 버전으로 이동하여 **[!UICONTROL Publish]**&#x200B;을(를) 클릭합니다.

## JavaScript을 사용한 사용자 지정 HTML 태그

이 섹션에서는 CSP(콘텐츠 보안 정책) 요구 사항을 준수하도록 체크아웃 페이지에서 실행하기 위해 CSP 임시 항목을 사용자 지정 HTML 태그 JavaScript에 추가하는 방법을 설명합니다. 이렇게 하면 승인되지 않은 스크립트가 실행되지 않으므로 사이트 보안이 강화됩니다. 자세한 내용은 [콘텐츠 보안 정책](https://developer.adobe.com/commerce/php/development/security/content-security-policies) 설명서를 참조하십시오.

>[!NOTE]
>
>`cspNonce` 전역 변수를 Google 태그 관리자로 가져오는 기능은 Adobe Commerce 버전 2.4.8 이상에서만 지원됩니다.

>[!WARNING]
>
>익숙하지 않은 스크립트를 스토어에 추가하면 데이터가 손상될 수 있습니다. 체크아웃 페이지에서 승인된 스크립트는 결제 세부 정보를 포함하여 중요한 고객 정보를 도용할 수 있습니다. Google Tag Manager 계정을 보호하기 위한 예방 조치를 취해야 합니다. 신뢰할 수 있는 스크립트만 추가하고, 정기적으로 태그를 검토 및 감사하며, 이중 인증(2FA) 및 액세스 제어와 같은 강력한 보안 조치를 구현할 수 있습니다.

### 1단계. CSP 임시 변수 만들기

변수 구성을 가져오거나 수동으로 구성하여 Google 태그 관리자 내에서 사용할 수 있는 CSP 임시 변수를 만들 수 있습니다.

#### 변수 구성 가져오기

CSP 임시 변수는 예제 컨테이너 [GTM_M2_Config_json.txt](./assets/GTM_M2_Config_json.txt)에 포함되어 있습니다. 이 코드를 작업 공간으로 가져와서 변수를 만들 수 있습니다.

#### 수동으로 변수 만들기

변수 구성을 가져올 수 없는 경우 아래 단계를 완료하여 만드십시오.

1. 작업 영역에서 사이드바의 **변수** 섹션으로 이동합니다.
1. **사용자 정의 변수** 섹션에서 페이지 하단에 있는 **새로 만들기** 단추를 클릭합니다.
1. 변수 이름을 `gtmNonce`로 지정합니다.
1. 연필 아이콘을 클릭하여 변수를 편집합니다.
1. **페이지 변수** 섹션에서 **JavaScript 변수**&#x200B;을(를) 선택합니다.
1. **전역 변수 이름** 필드에 `window.cspNonce`을(를) 입력하십시오.
1. 변수를 저장합니다.

[Google 태그 관리자 변수](https://support.google.com/tagmanager/answer/7683056?hl=en)에 대한 자세한 내용은 Google 설명서의 [웹용 사용자 정의 변수 형식](https://support.google.com/tagmanager/answer/7683362?hl=en)을 참조하십시오. 이 설명서는 사용자 지정 변수를 만들고 관리하는 데 대한 자세한 지침을 제공하여 특정 마케팅 및 분석 요구에 맞게 태그 관리를 맞춤화합니다.

### 2단계. 사용자 지정 HTML 태그 만들기

1. 작업 영역에서 사이드바의 **태그** 섹션으로 이동합니다.
1. **새로 만들기** 단추를 클릭합니다.
1. **태그 구성** 섹션에서 **사용자 지정 HTML 태그**&#x200B;를 선택합니다.
1. 텍스트 영역에 필요한 JavaScript을 입력하고 이전 단계에서 만든 변수를 가리키는 여는 `<script>` 태그에 nonce 특성을 추가합니다. For example:

   ```html
   <script nonce="{{gtmNonce}}">
       // Your JavaScript code here
   </script>
   ```

1. **지원 문서.쓰기**&#x200B;를 선택합니다.
1. **트리거** 섹션에서 원하는 트리거를 선택합니다. 예: **동의 초기화 - 모든 페이지**.

Google 태그 관리자의 [태그](https://support.google.com/tagmanager/answer/3281060)에 대한 자세한 내용은 Google 설명서의 [사용자 지정 태그](https://support.google.com/tagmanager/answer/6107167)를 참조하십시오.
