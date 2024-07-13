---
title: '[!DNL Google Content Experiments]'
description: ' [!DNL Google Content Experiments] 을(를) 사용하여 Commerce 제품, 카테고리 또는 콘텐츠 페이지의 A/B 테스트를 설정하는 방법에 대해 알아봅니다.'
exl-id: ae03bc5a-de84-4dad-932e-e79e509feebe
feature: Marketing Tools, Integration
source-git-commit: eb0fe395020dbe2e2496aba13d2f5c2bf2d0fc27
workflow-type: tm+mt
source-wordcount: '441'
ht-degree: 0%

---

# [!DNL Google Content Experiments]

다음 예는 Google Analytics 컨텐츠 실험을 사용하여 제품, 카테고리 또는 컨텐츠 페이지의 A/B 테스트를 설정하는 방법을 보여줍니다. Commerce 관리자와 [!DNL Google Analytics] 계정 사이를 왔다갔다해야 하므로 지침을 따라 작업하는 동안 두 개의 브라우저 탭을 열어 두는 것이 좋습니다.

>[!NOTE]
>
>[!DNL Google Content Experiments]은(는) 더 이상 사용되지 않으며 [Google 최적화](https://support.google.com/optimize/answer/7084762?hl=en)에 의해 대체되도록 예약되었습니다.

## 1단계. 콘텐츠 실험 활성화(Commerce)

1. Commerce 설치 관리자에 로그인합니다.

1. Commerce 구성에서 콘텐츠 실험을 통해 [Google Analytics](google-analytics.md)을(를) 활성화하려면 지침을 따르십시오.

   ![판매 구성 - Google API - Google Analytics](../configuration-reference/sales/assets/google-api-analytics-ee.png){width="600" zoomable="yes"}

## 2단계. 변형 설정(Commerce)

동일한 제품, 카테고리 또는 페이지의 여러 변형을 만듭니다.

- 각 변형에는 고유한 [URL 키](../catalog/catalog-urls.md)가 있어야 합니다.
- 각 변형에는 선택한 동일한 [스토어 보기](../getting-started/websites-stores-views.md#scope-settings)가 있어야 합니다.

테스트할 각 엔티티의 변형을 최대 10개까지 만들 수 있습니다. 제품의 경우 [저장 및 복제](../catalog/product-workspace.md)를 사용하여 시간을 절약하십시오.

## 3단계. 실험 설정(Google)

>[!NOTE]
>
>실험을 만들려면 Google 계정에 대한 적절한 권한이 있어야 합니다.

1. 다른 브라우저 탭을 열고 [Google Analytics][2] 계정에 로그인합니다.

   필요한 경우 **[!UICONTROL Account]** 및 **[!UICONTROL Property]**(으)로 이동합니다.

1. 왼쪽의 사이드바에서 **[!UICONTROL Admin]**&#x200B;을(를) 선택하고 다음 방법 중 하나를 사용하십시오.

   **메서드 1:** 기존 보기 선택

   _[!UICONTROL View]_열의 헤더에서 아래쪽 화살표를 클릭하고 실험에 데이터를 제공할 보기를 선택합니다.

   **메서드 2:** 새 보고 보기 만들기

   - _보기_ 열의 헤더에서 **[!UICONTROL Create View]**&#x200B;을(를) 클릭하고 다음을 수행합니다.

      - 실험 위치를 `Website` 또는 `Mobile app`(으)로 식별합니다.

      - 설명 **[!UICONTROL Reporting View Name]**&#x200B;을(를) 입력하십시오.

      - **[!UICONTROL Reporting Time Zone]**&#x200B;을(를) 지정하십시오.

   - 완료되면 **[!UICONTROL Create View]**&#x200B;을(를) 클릭한 다음 뒤로 화살표를 클릭하여 이전 페이지로 돌아갑니다.

1. _[!UICONTROL Reports]_아래의 왼쪽 패널에서&#x200B;**[!UICONTROL Behavior]**>**[!UICONTROL Experiments]**을(를) 선택합니다.

1. **[!UICONTROL Create experiment]**&#x200B;을(를) 클릭하고 다음을 수행합니다.

   - 리디렉션할 트래픽의 비율을 지정합니다.

   - 테스트할 각 **[!UICONTROL page variation]**&#x200B;의 **[!UICONTROL Original Page URL]** 및 URL을 지정합니다.

   - 다른 옵션을 완료합니다.

1. 실험이 설정되면 **[!UICONTROL Manually Insert the Code]**&#x200B;을(를) 클릭하고 코드 조각을 복사합니다.

## 4단계. 코드 조각 붙여넣기(Commerce)

1. Commerce 설치 관리자로 돌아가 제품, 카테고리 또는 페이지의 원래 버전을 편집 모드로 엽니다.

1. 제품, 카테고리 또는 페이지에 대한 **[!UICONTROL View Optimization]** 섹션을 확장합니다.

1. Google Analytics에서 복사한 코드 조각을 **[!UICONTROL Experiment Code]** 텍스트 상자에 붙여 넣습니다.

   >[!NOTE]
   >
   >코드 스니펫을 변형에 붙여 넣지 마십시오.

   ![제품 보기 최적화](../catalog/assets/product-view-optimization.png){width="600" zoomable="yes"}

1. 완료되면 **[!UICONTROL Save]**&#x200B;을(를) 클릭합니다.

## 5단계: 실험 검토 및 시작(Google)

1. [Google Analytics][2] 계정으로 돌아갑니다.

1. 실험 설정을 검토합니다.

1. 시작할 준비가 되면 **[!UICONTROL Start Experiment]**&#x200B;을(를) 클릭합니다.

   그렇지 않으면 **[!UICONTROL Save for Later]**&#x200B;을(를) 클릭합니다.


[2]: https://analytics.google.com/
