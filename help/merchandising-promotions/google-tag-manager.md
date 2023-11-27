---
title: '[!DNL Google Tag Manager]'
description: 사용 방법 알아보기 [!DNL Google Tag Manager] Adobe Commerce 사이트의 마케팅 캠페인 이벤트와 관련된 많은 태그(코드 조각)를 관리합니다.
exl-id: 9c24239b-9efd-42ee-9b99-5a194f3c4347
feature: Marketing Tools, Integration
source-git-commit: 7384481d1a4a2a04882d4c99448cca75abc9be31
workflow-type: tm+mt
source-wordcount: '1161'
ht-degree: 0%

---

# [!DNL Google Tag Manager]

{{ee-feature}}

[!DNL Google Tag Manager] 는 마케팅 캠페인 이벤트와 관련된 많은 태그(코드 조각)를 관리하는 데 도움이 됩니다. [!DNL Google Tag Manager] 은 사이트에 추적 태그를 추가하여 대상자를 측정하거나 검색 엔진 마케팅 이니셔티브를 개인화, 재타겟팅 또는 수행하는 기능을 제공합니다.

[!DNL Google Tag Manager] 데이터 및 이벤트를 (으)로 직접 전송 [!DNL Google Analytics], 향상된 Ecommerce 및 기타 서드파티 분석 솔루션을 사용하여 사이트, 제품 및 판촉 활동의 성과를 명확하게 파악할 수 있습니다.

다음 항목이 있어야 합니다. [!DNL Google Analytics] 및 [!DNL Tag Manager] 계정을 사용하여 이 프로세스를 계속합니다. 다음 지침은 Google 계정을 구성하고, Commerce 스토어를 구성하고, 태그를 만드는 과정을 안내합니다.

>[!NOTE]
>
>비즈니스에 다음과 같은 개인 정보 보호 규정이 적용되는 경우 [일반 데이터 보호 규정](../getting-started/compliance-gdpr.md) 및/또는 [캘리포니아 소비자 개인 정보 보호법](../getting-started/compliance-ccpa.md), 참조 [Google 개인 정보 설정](google-tools.md#google-privacy-settings).

## 1단계. 구성 [!DNL Google Analytics] account

다음을 참조하십시오 [사이트 검색 설정](https://support.google.com/analytics/answer/1012264) 시작에 필요한 기본 사항은 Google 도움말에서 확인하십시오. 다음에 대한 Google 안내서 참조: [Google Analytics](https://support.google.com/analytics/answer/9304153) 및 [Google 태그 관리자](https://support.google.com/tagmanager/answer/6102821).

1. 다음에 로그인 [!DNL Google Analytics] 계정입니다.

1. 활성화하려면 **[!UICONTROL Internal Site Search Tracking]**&#x200B;를 사용하여 다음을 수행합니다.

   - 다음으로 이동 **[!UICONTROL Select View]** > **[!UICONTROL View Settings]**.

   - 설정 **[!UICONTROL Site Search Tracking]** 끝 `On`.

   - 설정 **[!UICONTROL Query]** 매개 변수 `q`.

   - 완료되면, **[!UICONTROL Save]** 설정.

1. 디스플레이 기능을 활성화하려면 다음을 수행합니다.

   - 선택 **[!UICONTROL Property Settings]**.

   - 아래 _[!UICONTROL Advertising Features]_, 설정됨&#x200B;**[!UICONTROL Enable Demographics and Interest Reports]**끝 `On`.

   - **[!UICONTROL Save]** 설정.

1. 전자 상거래 추적을 활성화하려면 다음 작업을 수행하십시오.

   - 다음으로 이동 **[!UICONTROL Select View]** > **[!UICONTROL Ecommerce Settings]**.

   - 설정 **[!UICONTROL Enable Ecommerce]** 끝 `On`.

   - 설정 **[!UICONTROL Enable Enhanced Ecommerce Reporting]** 끝 `On`.

   - **[!UICONTROL Save]** 설정.

1. 페이지를 다시 로드하고 모든 설정이 유지되는지 확인합니다. `On`.

   >[!NOTE]
   >
   >일부 설정은 `On`, 이전 단계를 반복하고 페이지를 저장한 다음 다시 로드합니다. 모든 설정이 로 설정될 때까지 이 프로세스를 반복합니다 `On`.

## 2단계. 구성 [!DNL Google Tag Manager] account

다음 지침은 기본 설정으로 새 컨테이너를 구성하는 방법을 보여 줍니다. 샘플 [작성기](https://developer.adobe.com/commerce/php/development/composer/) 구성(.json) 파일을 사용하여 프로세스를 단순화하고 가져오기를 통해 새 컨테이너에 태그를 생성합니다. 이 예제에서는 기존 컨테이너를 수정하지 않고 컨테이너를 만드는 것이 좋습니다.

>[!NOTE]
>
>자세한 내용은 Google [컨테이너 내보내기 및 가져오기](https://support.google.com/tagmanager/answer/6106997). 이러한 지침은 새 컨테이너에서 샘플 JSON을 가져오는 방법에 대한 설명을 제공합니다.

1. 연결된 파일 다운로드 [GTM_M2_Config_json.txt](./assets/GTM_M2_Config_json.txt)를 클릭하고 편집기에서 파일을 열고 다른 이름으로 저장합니다. `GTM_M2_Config.json`.

   json 파일이에 바로 업로드됩니다. [!DNL Google Tag Manager].

1. 다음으로 이동 **[!UICONTROL Admin]** > **[!UICONTROL Container]** > **[!UICONTROL Import Container]**.

1. 클릭 **[!UICONTROL Choose container file]** json 파일을 선택합니다.

1. 아래 **[!UICONTROL Choose workspace]**, 클릭 **[!UICONTROL New]**.

1. 제목과 설명을 입력한 다음 **[!UICONTROL Save]**.

1. 파일을 가져오려면 다음 작업 중 하나를 선택합니다.

   - 다음 **[!UICONTROL Overwrite]** 새 컨테이너에 대해 옵션을 선택해야 합니다.

   - 다음 **[!UICONTROL Merge]** 기존 컨테이너를 사용하는 경우 옵션을 선택해야 합니다.

1. 클릭 **[!UICONTROL Preview]** 를 클릭하여 태그, 트리거 및 변수를 검토합니다.

1. 을(를) 편집하려면 **[!UICONTROL Google Analytics ID]** 변수에서 참조되는 경우 다음을 수행합니다.

   - 다음으로 이동 **[!UICONTROL Variables]** > **[!UICONTROL User-Defined Variables]**.

   - 선택 **[!UICONTROL Google Analytics]** 자리 표시자(`UA-xxxxxx-x`)을 자신의 것과 **[!UICONTROL GA ID]**.

1. 태그, 트리거 및 변수를 새 컨테이너에 추가하는 방법에 대한 Google의 지침을 따릅니다.

   사용할 다른 컨테이너에 설정이 있는 경우 새 컨테이너로 이동할 수 있습니다.

1. 클릭 **[!UICONTROL Confirm]** 완료 시.

1. 새 컨테이너를 게시하려면 Google의 지침을 따르십시오.

## 3단계. 스토어 구성

{{gtag-api-note}}

1. Commerce 스토어의 관리자에 로그인합니다.

1. 다음에서 _관리자_ 사이드바, 이동 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. 왼쪽 패널에서 를 확장합니다. **[!UICONTROL Sales]** 및 선택 **[!UICONTROL Google API]**.

1. 확장 ![확장 선택기](../assets/icon-display-expand.png) 다음 **[!UICONTROL Google Analytics]** 섹션을 만들고 다음을 구성합니다.

   ![영업 구성 - Google Analytics](../configuration-reference/sales/assets/google-api-analytics-tag-manager.png){width="600" zoomable="yes"}

   - 설정 **[!UICONTROL Enable]** 끝 `Yes`.

   - 설정 **[!UICONTROL Account type]** 끝 `Google Tag Manager`.

   - 다음에서 **[!UICONTROL Container ID]** 필드에 GTM ID를 입력합니다(`GTM-xxxxxx`).

   - 콘텐츠 실험에 Google Analytics을 사용하는 경우 다음을 설정하십시오. **콘텐츠 실험 활성화** 끝 `Yes`.

   - 나머지 필드에 기본값을 사용합니다.

1. 완료되면 다음을 클릭하십시오. **[!UICONTROL Save Config]**.

1. 테스트 [!DNL Google Tag Manager] 모든 설정이 올바르게 작동하는지 확인합니다.

>[!NOTE]
>
>각 컨테이너는 하나의 웹 사이트와 연결되어 있으며 계정당 하나의 컨테이너만 있으면 됩니다. 다중 사이트 상거래 인스턴스가 있는 경우 별도의 컨테이너가 필요합니다.

## 4단계. Adobe Commerce 스토어에 GTM 코드 추가

1. GTM 코드를 복사하려면 **[!UICONTROL Admin]** > **[!UICONTROL Install Google Tag Manager]**.

   상거래 사이트에 두 개의 GTM 코드 조각을 추가할 수 있습니다. `<head>` 태그와 의 두 번째 `<body>` 태그에 가깝게 배치하십시오.

1. Commerce 관리자에서 **[!UICONTROL Content]** > _[!UICONTROL Design]_>**[!UICONTROL Configuration]**편집 모드로 스토어 보기를 엽니다.

1. 아래 _[!UICONTROL Other Settings]_, 확장&#x200B;**[!UICONTROL HTML Head]**및 를 위해 GTM에서 복사한 코드를 `<head>` 태그 내&#x200B;**[!UICONTROL Scripts and Style Sheets]**필드.

   ![HTML 헤드에 코드 삽입](./assets/head-tag.png){width="600" zoomable="yes"}

1. 확장 **[!UICONTROL Footer]** 및 의 GTM 코드를 붙여넣습니다. `<body>` 다음에서 **[!UICONTROL Miscellaneous HTML]** 필드.

   ![바닥글에 코드 삽입](./assets/footer-tag-section.png){width="600" zoomable="yes"}

1. 완료되면 다음을 클릭하십시오. **[!UICONTROL Save Configuration]**.

## 필드 설명

| 필드 | 범위 | 설명 |
|--- |--- |--- |
| [!UICONTROL Enable] | 스토어 뷰 | Google Analytics 고급 전자 메일을 사용하여 스토어의 활동을 분석할 수 있는지 여부를 결정합니다. 옵션: `Yes` / `No` |
| [!UICONTROL Account type] | 스토어 뷰 | 저장소 활동 및 트래픽을 모니터링하는 데 사용되는 Google 추적 코드를 결정합니다. 옵션: `Google Analytics` / `Google Tag Manager` |
| [!UICONTROL Anonymize IP] | 스토어 뷰 | Google Analytics 결과에 나타나는 IP 주소에서 식별 정보가 제거되는지 여부를 결정합니다. |
| [!UICONTROL Enable Content Experiments] | 스토어 뷰 | 동일한 페이지의 서로 다른 버전을 최대 10개까지 테스트하는 데 사용할 수 있는 Google 콘텐츠 실험을 활성화합니다. 옵션: `Yes` / `No` |
| [!UICONTROL Container Id] | 스토어 뷰 | If [!DNL Google Tag Manager] 이(가) 이미 설치되고 스토어에 대해 구성되었습니다. 컨테이너 ID가 이 필드에 자동으로 표시됩니다. |
| [!UICONTROL List property for the catalog page] | 스토어 뷰 | 카탈로그 페이지와 연결된 태그 관리자 속성을 식별합니다. 기본값: `Catalog Page` |
| [!UICONTROL List property for the cross-sell block] | 스토어 뷰 | 크로스셀 블록과 연결된 Tag Manager 속성을 식별합니다. 기본값: `Cross-sell` |
| [!UICONTROL List property for the up-sell block] | 스토어 뷰 | 업셀 블록과 연결된 Tag Manager 속성을 식별합니다. 기본값: `Up-sell` |
| [!UICONTROL List property for the related products block] | 스토어 뷰 | 관련 제품 블록과 연결된 Tag Manager 속성을 식별합니다. 기본값: `Related Products` |
| [!UICONTROL List property for the search results page] | 스토어 뷰 | 검색 결과 페이지와 연결된 태그 관리자 속성을 식별합니다. 기본값: `Search Results` |
| [!UICONTROL "Internal Promotions" for promotions field "Label"] | 스토어 뷰 | 내부 프로모션의 레이블과 연결된 태그 관리자 속성을 식별합니다. 기본값: `Label` |

{style="table-layout:auto"}

## 전환 추적을 위한 태그 만들기

Google AdWords 계정이 있는 경우 전환을 추적하는 태그를 만들 수 있습니다. 다음 예에서는 두 가지를 모두 사용하는 방법을 보여 줍니다 [!DNL Google Tag Manager] 및 [!DNL Google Analytics] 스토어의 변환 시 실행되는 태그를 만들려면 _성공_ 페이지를 가리키도록 업데이트하는 중입니다.

### 1단계. 태그 만들기

1. 에 로그인 [!DNL Google Tag Manager] 계정에 추가하고 스토어에 대해 만든 컨테이너에 대한 링크를 클릭합니다.

1. 다음에서 **[!UICONTROL New Tag]** 상자, 클릭 **[!UICONTROL Add a new tag]**.

1. AdWords 계정에서 다음 정보를 가져옵니다.

   - 전환 ID
   - 전환 레이블

   도움이 필요한 경우 Google [지원 사이트](https://support.google.com/tagmanager/answer/6105160).

1. 다음에서 [!DNL Google Tag Manager] 대시보드, 클릭 **[!UICONTROL Google AdWords]** 다음을 수행합니다.

   - 제목 자리 표시자를 클릭하고 새 태그의 이름을 입력합니다.

   - 아래 **[!UICONTROL Choose Product]**, 선택 **[!UICONTROL Google AdWords]**.

   - 아래 _[!UICONTROL Choose a Tag Type]_, 선택&#x200B;**[!UICONTROL AdWords Conversion Tracking]**및 클릭&#x200B;**[!UICONTROL Continue]**.

1. 다음을 입력합니다. **[!UICONTROL Conversion ID]** 및 **[!UICONTROL Conversion Label]** AdWords 계정에서 **[!UICONTROL Continue]**.

### 2단계. 규칙 만들기

다음 항목에서 계속 [!DNL Google Tag Manager] 대시보드의 다음 단계는 전환 페이지에서 태그를 실행하는 규칙을 만드는 것입니다.

1. 아래 **[!UICONTROL Fire On]**, 클릭 **[!UICONTROL Some Pages]**.

1. 다음에서 _[!UICONTROL Choose Pages]_섹션에서 다음 설정을 완료합니다.

   - **[!UICONTROL Name]** - 페이지 설명의 이름을 입력합니다.

   - **[!UICONTROL Variable]** `url`

   - **작업** - `matches RegEx`

     자세한 내용은 다음을 참조하십시오. [Regex 및 CSS 선택기 연산자](https://support.google.com/tagmanager/answer/7679109) Google Tag Manager 도움말의 .

   - **[!UICONTROL Value]** - `checkout/success.*`

1. 녹색 확인란을 선택하고 **[!UICONTROL Save]**.

   설정한 트리거는 [실행] 섹션에 파란색 단추로 나타납니다.

1. 완료되면 다음을 클릭하십시오. **[!UICONTROL Save Tag]**.

### 3단계. 미리보기 및 게시

프로세스의 다음 단계는 태그를 미리 보는 것입니다. 태그를 미리 볼 때마다 버전의 스냅샷이 저장됩니다. 결과가 만족스러우면 사용할 버전으로 이동하여 을 클릭합니다 **[!UICONTROL Publish]**.
