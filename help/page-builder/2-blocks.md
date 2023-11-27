---
title: '''[!DNL Page Builder] 2부: 블록'
description: 를 사용할 때 단순 블록과 동적 블록의 차이점에 대해 알아봅니다 [!DNL Page Builder].
exl-id: 864a3078-8cb3-4add-bdb7-14189aba535e
feature: Page Builder, Page Content
source-git-commit: 2299beb6c11af801076d3aff0b026d41b9dbd212
workflow-type: tm+mt
source-wordcount: '2053'
ht-degree: 0%

---

# [!DNL Page Builder] 2부: 블록

다음 연습에서는 의 차이점을 보여 줍니다. [단순 블록](../content-design/blocks.md) 및 [동적 블록](dynamic-block.md), 및 사용 방법 [!DNL Page Builder] 각 유형의 블록을 만듭니다.

>[!NOTE]
>
>[!DNL Page Builder] 에는 라는 새로운 콘텐츠 유형이 있습니다. _배너_, 이는 첫 번째 연습 연습에서 다뤄지며 이전 배너 기능과 관련이 없습니다. 이전에는 의 배너 옵션이 무엇입니까? [콘텐츠 메뉴](../content-design/content-menu.md), 현재 _동적 블록_.

![상점 첫 화면의 동적 블록](./assets/pb-tutorial2-dynamic-block-storefront.png){width="700" zoomable="yes"}

이 연습에서는 이 작업을 완료했다고 가정합니다 [1부: 단순 페이지](1-simple-page.md), 사전 요구 사항 및 [다운로드한 샘플 파일](./assets/simple-page-assets.zip). 이 연습 연습의 각 부분을 순서대로 따르십시오.

>[!NOTE]
>
>이 연습 연습은 최근 변경 사항을 반영하여 업데이트됩니다 [!DNL Page Builder] 2.4.1 릴리스의 작업 영역 이전 Adobe Commerce 릴리스를 사용하는 경우 [!DNL Page Builder] 에 포함된 연습 [[!DNL Commerce] 2.3 사용 안내서](https://docs.magento.com/user-guide/v2.3/cms/page-builder-learn.html).

## 1부: 간단한 블록 만들기

이 연습 연습에서는 의 콘텐츠로 간단한 블록을 만듭니다. [!DNL Google Maps]. 단순 블록은 종종 호출됩니다. _CMS 블록_ 또는 _정적 블록_&#x200B;콘텐츠가 변경되지 않기 때문입니다. 단순 블록은 재사용할 수 있는 콘텐츠에 이상적입니다.

### 1단계: 블록 만들기

1. 다음에서 _관리자_ 사이드바, 이동 **[!UICONTROL Content]** > _[!UICONTROL Elements]_>**[!UICONTROL Blocks]**.

1. 오른쪽 위 모서리에서 을(를) 클릭합니다. **[!UICONTROL Add New Block]**.

1. 대상 **[!UICONTROL Block Title]**, 입력 `Google Map`.

1. 대상 **[!UICONTROL Identifier]**, 입력 `google-map`.

1. 다음을 선택합니다. **[!UICONTROL Store View]** 블록을 사용할 수 있는 위치입니다.

   ![블록 정보](./assets/pb-tutorial2-block-new-google-map.png){width="600" zoomable="yes"}

1. 오른쪽 위 모서리에서 을(를) 클릭합니다. **[!UICONTROL Save]**.

### 2단계: 추가 [!DNL Google Map]

1. 아래로 스크롤하여 [!DNL Page Builder] 콘텐츠 미리보기 (현재 비어 있음) 및 클릭 **[!UICONTROL Edit with Page Builder]**.

1. 다음에서 [!DNL Page Builder] 패널, 확장 **[!UICONTROL Media]** 드래그 **[!UICONTROL Map]** 자리 표시자가 스테이지에 표시됩니다.

   ![스테이지로 맵 드래그](./assets/pb-media-map-drag.png){width="600" zoomable="yes"}

   다음과 같은 경우 스토어 위치에 대한 맵이 나타납니다. [!DNL Google Maps] 은(는) 스토어에 대해 구성됩니다.

   ![스토어에 대해 Google 맵 구성됨](./assets/pb-tutorial2-google-map.png){width="600" zoomable="yes"}

   자리 표시자 맵은 [!DNL Google Maps] 은(는) 아직 스토어에 대해 구성되지 않았습니다.

   ![[!DNL Google Maps] 자리 표시자](./assets/pb-tutorial2-media-map-not-configured.png){width="600" zoomable="yes"}

1. 스테이지의 오른쪽 위 모서리에서 _전체 화면 닫기_ (![전체 화면 아이콘 닫기](./assets/pb-icon-reduce.png)) 아이콘.

   이 아이콘을 클릭하면 _[!UICONTROL Content]_미리보기가 표시된 블록의 섹션입니다.

1. 오른쪽 위 모서리에서 **[!UICONTROL Save]** 화살표 및 선택 **[!UICONTROL Save & Close]**.

### 3단계: 구성 [!DNL Google Maps]

If [!DNL Google Maps] 이(가) 스토어에 대해 이미 구성되어 있습니다. 이 단계를 건너뛰고 다음 단계로 진행할 수 있습니다.

1. 로 이동 [Google 클라우드 플랫폼 콘솔](https://console.cloud.google.com/google/maps-apis/overview).

1. 프로젝트 드롭다운을 클릭하고 API 키를 추가할 프로젝트를 선택하거나 만듭니다.

1. API 자격 증명을 구성하려면 다음을 수행합니다. [지침][1] 다음에서 [!DNL Google Maps] 설명서를 참조하십시오.

1. API 키를 클립보드에 복사합니다.

1. (으)로 돌아가기 [!DNL Commerce] 책임자 및 이동 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. 아래의 왼쪽 패널에서 _[!UICONTROL General]_, 선택&#x200B;**[!UICONTROL Content Management]**.

1. 확장 ![확장 선택기](../assets/icon-display-expand.png) **[!UICONTROL Advanced Content Tools]**.

   ![고급 콘텐츠 도구](../configuration-reference/general/assets/content-management-advanced-content-tools.png){width="600" zoomable="yes"}

   에 대한 자세한 내용은 [!UICONTROL Content Management Advanced Tools] 구성 옵션을 보려면 다음을 참조하십시오. [_구성 참조 안내서_](../configuration-reference/general/content-management.md).

1. 대상 **[!UICONTROL Google Maps API Key]**&#x200B;를 클릭하고 복사한 키를 붙여넣습니다.

1. 클릭 **[!UICONTROL Test Key]**.

   키에 문제가 있는 경우 [!DNL Google Maps] 플랫폼 사이트로 이동하여 문제를 해결하십시오. 그런 다음 다시 시도하십시오.

1. 키를 확인한 후 **[!UICONTROL Save Config]**.

### 4단계: 페이지에 블록 추가

1. 다음에서 _관리자_ 사이드바, 이동 **[!UICONTROL Content]** > _[!UICONTROL Elements]_>**[!UICONTROL Pages]**.

1. 그리드에서 _[!UICONTROL Simple Page]_첫 번째 자습서에서 만든 다음&#x200B;**[!UICONTROL Edit]**다음에서_[!UICONTROL Action]_ 열.

1. 확장 ![확장 선택기](../assets/icon-display-expand.png) 다음 **[!UICONTROL Content]** 섹션 및 클릭 **[!UICONTROL Edit with Page Builder]** 또는 콘텐츠 미리 보기 영역 내부에 있습니다.

1. 다음에서 [!DNL Page Builder] 패널 아래 _[!UICONTROL Layout]_, 드래그&#x200B;**[!UICONTROL Row]**자리 표시자를 스테이지 맨 위에 추가합니다.

   ![단계 맨 위에 행 추가](./assets/pb-tutorial2-elements-row-drag-top.png){width="600" zoomable="yes"}

1. 다음에서 [!DNL Page Builder] 패널, 확장 **[!UICONTROL Add Content]** 드래그 **[!UICONTROL Block]** 자리 표시자를 새 행에 추가합니다.

1. 빈 블록 컨테이너에 마우스를 가져다 대고 도구 상자를 표시하고 _설정_ (![설정 아이콘](./assets/pb-icon-settings.png){width="20"} ) 아이콘.

   ![도구 상자 차단](./assets/pb-add-content-block-toolbox.png){width="600" zoomable="yes"}

1. 블록 편집 페이지에서 **[!UICONTROL Select Block]**.

   ![블록 선택](./assets/pb-add-content-block-settings-block-select.png){width="600" zoomable="yes"}

1. 검색 상자에 을 입력합니다. `map` 그리고 Enter/Return 키를 눌러 만든 블록을 찾습니다.

   ![목록에서 블록 찾기](./assets/pb-add-content-block-settings-block-find.png){width="600" zoomable="yes"}

1. 그리드에서 **[!UICONTROL Select]** 선택: [!DNL Google Maps] 차단합니다.

1. 오른쪽 위 모서리에서 을(를) 클릭합니다. **[!UICONTROL Save]** 설정을 저장하고 [!DNL Page Builder] 작업 영역.

1. 스테이지의 오른쪽 위 모서리에서 _전체 화면 닫기_ (![전체 화면 아이콘 닫기](./assets/pb-icon-reduce.png)) 아이콘.

   이 아이콘을 클릭하면 _[!UICONTROL Content]_미리보기가 표시된 페이지의 섹션입니다.

1. 오른쪽 위 모서리에서 **[!UICONTROL Save]** 화살표 및 선택 **[!UICONTROL Save & Close]**.

**축하합니다!** 블록 연습의 첫 번째 부분을 완료했습니다. 참고용으로 작업한 것을 잊지 말아라.

## 2부: 동적 블록 만들기

동적 블록에는 블록 표시 위치, 시기 및 대상을 결정하는 논리가 포함되어 있습니다. 이 연습에서는 가격 규칙 조건이 충족될 때 트리거되고 특정 고객 세그먼트에만 표시되는 프로모션에 대한 동적 블록을 만듭니다. 이 예제의 결과는 첫 번째 연습에서 만든 배너와 유사하지만 상점 첫 번째 연습에서 나타나는 시점을 제어하는 논리를 사용합니다.

![샘플 Luma 티 프로모션](./assets/pb-tutorial2-dynamic-block-row-page.png){width="600" zoomable="yes"}

### 1단계: 새 동적 블록 만들기

1. 다음에서 _관리자_ 사이드바, 이동 **[!UICONTROL Content]** > _[!UICONTROL Elements]_>**[!UICONTROL Dynamic Blocks]**.

   ![동적 블록 목록](./assets/pb-tutorial2-block-dynamic-add.png){width="700" zoomable="yes"}

1. 오른쪽 위 모서리에서 을(를) 클릭합니다. **[!UICONTROL Add Dynamic Block]**.

   ![새 동적 블록 페이지](./assets/pb-tutorial2-block-dynamic-new.png){width="600" zoomable="yes"}

1. 새 동적 블록에 대한 기본 설정을 완료합니다.

   - 설정 **[!UICONTROL Enable Dynamic Block]** 끝 `Yes`.

   - 대상 **[!UICONTROL Dynamic Block Name]**, 입력 `Tee Shirt Promo`.

   - 설정 **[!UICONTROL Dynamic Block Type]** 끝 `Content Area` 및 클릭 **[!UICONTROL Done]**.

     동적 블록 유형은 [페이지 레이아웃](../content-design/page-layout.md) 블록을 배치합니다. 스토어에 대한 동적 블록을 설정할 때는 페이지 레이아웃과 을 모두 고려하십시오. [테마](../content-design/themes.md)사용 가능한 공간을 적절하게 사용할 수 있습니다. 일부 스토어에는 고정된 너비로 제한된 활성 콘텐츠 영역이 있는 반면, 다른 스토어는 화면의 전체 너비를 확장합니다.

     ![동적 블록 유형 설정](./assets/pb-dynamic-block-type.png){width="600" zoomable="yes"}

   - 대상 **[!UICONTROL Customer Segment]**&#x200B;을 클릭하고, 동적 블록에 적용할 각 세그먼트의 확인란을 선택한 다음 을 클릭합니다. **완료** 세그먼트 목록을 저장합니다.

     다음 예에는 두 가지가 있습니다 [고객 세그먼트](../customers/customer-segments.md) 등록된 고객을 성별을 기준으로 식별합니다. 이 동적 블록은 매장에서 쇼핑하는 동안 계정에 로그인한 등록된 여성 고객에게만 표시됩니다.

     ![고객 세그먼트 선택](./assets/pb-dynamic-block-customer-segment.png){width="600" zoomable="yes"}

### 2단계: 설정 완료

아래로 스크롤하여 _[!UICONTROL Content]_섹션: 비어 있음 [!DNL Page Builder] 컨텐츠 미리 보기 및 클릭&#x200B;**[!UICONTROL Edit with Page Builder]**. 그런 다음 다음 다음 작업을 완료하십시오.

**작업 1:** 배경 이미지 추가

1. 행 컨테이너 위로 마우스를 가져가면 도구 상자가 표시되고 _설정_ (![설정 아이콘](./assets/pb-icon-settings.png){width="20"} ) 아이콘.

1. 아래 _[!UICONTROL Appearance]_, 선택&#x200B;**[!UICONTROL Full Bleed]**.

1. 대상 **[!UICONTROL Minimum Height]**, 입력 `400px`.

1. 다음으로 스크롤 _[!UICONTROL Background]_섹션 및 설정&#x200B;**[!UICONTROL Background Image]**다음을 클릭:**[!UICONTROL Select from Gallery]**및 선택 `wide-banner-background.png` 첫 번째 자습서에서 업로드한 이미지입니다.

1. 오른쪽 위 모서리에서 을(를) 클릭합니다. **[!UICONTROL Save]** 설정을 적용하고 로 돌아가려면 [!DNL Page Builder] 작업 영역.

   ![이미지가 있는 행](./assets/pb-tutorial2-row-image.png){width="600" zoomable="yes"}

**작업 2:** 열 추가

다음에서 [!DNL Page Builder] 패널 아래 _[!UICONTROL Layout]_, 드래그&#x200B;**[!UICONTROL Column]**행 위의 자리 표시자

![열 유형을 행으로 드래그](./assets/pb-tutorial2-column-drag.png){width="600" zoomable="yes"}

이제 행이 동일한 너비의 두 열로 나뉩니다.

**작업 3:** 텍스트 추가

1. 다음에서 [!DNL Page Builder] 패널, 확장 **[!UICONTROL Elements]** 드래그 **텍스트** 자리 표시자를 두 번째 열로 보냅니다.

   ![텍스트 상자를 두 번째 열로 드래그](./assets/pb-tutorial2-column-text-drag.png){width="600" zoomable="yes"}

1. 편집기에 다음 세 줄의 텍스트를 입력합니다.

   `Even more ways to mix and match.`

   `Buy 3 Luma tees and get a 4th free.`

   `Shop Tees >`

   ![열에 대한 텍스트 입력](./assets/pb-tutorial2-column-text-editor.png){width="600" zoomable="yes"}

1. 세 줄의 텍스트를 모두 선택하고 도구 모음을 사용하여 **선 높이** 끝 `40px`.

   ![선 높이 설정](./assets/pb-tutorial2-column-text-editor-line-height.png){width="600" zoomable="yes"}

1. 설정 **[!UICONTROL Font Size]** 각 행에 대해 다음과 같이 지정합니다.

   | 라인 | 글꼴 크기 |
   |-----| ---------- |
   | 1행: | `28px` |
   | 2행: | `24px` |
   | 3행: | `18px` |

   이 블록은 페이지의 어디에나 배치할 수 있으므로 제목 수준이 아닌 기본 단락 스타일을 사용하십시오. 또한 텍스트가 아직 열에 올바르게 감싸지지 않을 수도 있습니다.  

   ![서식 있는 텍스트](./assets/pb-tutorial2-column-text-editor-text-formatted.png){width="600" zoomable="yes"}

**작업 4:** 링크 추가

첫 번째 연습에서는 를 사용하는 방법을 배웠습니다. [단추](buttons.md) 링크를 만들 컨텐츠 유형입니다. 이 예에서는 편집기 도구 모음에서 링크를 삽입하는 방법을 보여 줍니다.

1. 다른 브라우저 탭에서 스토어프런트를 열고 링크의 대상 페이지로 이동합니다.

   저장소 도메인에 대한 참조를 생략하는 상대 URL 또는 정규화된 URL을 사용할 수 있습니다.

   전체 URL: `https://mystore.com/women/tops-women/tees-women.html`

   상대 URL : `../women/tops-women/tees-women.html`

1. (으)로 돌아가기 [!DNL Page Builder] 작업 영역 탭과 텍스트 편집기에서 `Shop Tees >` 세 번째 줄의 텍스트를 선택하고 **굵게** (![굵게 버튼](./assets/editor-btn-bold.png))을 클릭하여 제품에서 사용할 수 있습니다.

1. 포함 `Shop Tees >` 세 번째 줄의 텍스트가 여전히 선택되었습니다. **링크 삽입/편집** (![링크 삽입/편집 단추](./assets/pb-icon-add-link.png))을 클릭하여 제품에서 사용할 수 있습니다.

   ![링크 삽입](./assets/pb-tutorial2-column-text-editor-link-insert.png){width="600" zoomable="yes"}

1. 대상 **[!UICONTROL URL]**&#x200B;를 클릭하고 준비한 상대 링크를 입력합니다.

1. 설정 **[!UICONTROL Target]** 끝 `None`.

   이 설정은 새 탭을 열지 않고 동일한 브라우저 창에서 페이지를 엽니다.

1. 대상 **[!UICONTROL Title]**, 입력 `Shop Tees`.

   Title 링크 속성은 일부 브라우저에서 툴팁으로 사용됩니다.

1. 링크를 저장하고 [!DNL Page Builder] 작업 영역, 클릭 **[!UICONTROL OK]**.

   ![링크 세부 정보](./assets/pb-tutorial2-column-text-editor-link-insert-detail.png){width="600" zoomable="yes"}

1. 스테이지의 오른쪽 위 모서리에서 _전체 화면 닫기_ (![전체 화면 아이콘 닫기](./assets/pb-icon-reduce.png)) 아이콘.

   이 아이콘을 클릭하면 _[!UICONTROL Content]_미리보기가 표시된 동적 블록에 대한 섹션입니다.

1. 오른쪽 위 모서리에서 을(를) 클릭합니다. **[!UICONTROL Save]**.

### 3단계: 가격 규칙 추가

1. 를 엽니다. _Tee Shirt 프로모션_ 편집 모드의 동적 블록을 다시 시작합니다.

1. 확장 ![확장 선택기](../assets/icon-display-expand.png) 다음 **[!UICONTROL Related Promotions]** 섹션 및 클릭 **[!UICONTROL Add Cart Price Rules]**.

   ![관련 프로모션](./assets/pb-dynamic-blocks-related-promotions.png){width="600" zoomable="yes"}

1. 다음에서 _관련 장바구니 가격 규칙 추가_ 페이지에서 다음에 대한 확인란을 선택합니다 _티셔츠 3개 구매하시면 4회까지 무료입니다_ 가격 규칙 및 클릭 **[!UICONTROL Add Selected]**.

   ![관련 장바구니 가격 규칙 추가](./assets/pb-dynamic-block-add-related-cart-price-rules.png){width="600" zoomable="yes"}

   가격 규칙은에 표시됩니다. _관련 프로모션_ 섹션, 아래 _관련 장바구니 가격 규칙_. 여러 가격 규칙을 동적 블록과 연관시킬 수 있습니다. 그러나 이 간단한 예제는 하나만 사용합니다.

   ![선택한 장바구니 가격 규칙](./assets/pb-dynamic-block-related-cart-price-rule-list.png){width="600" zoomable="yes"}

1. 오른쪽 위 모서리에서 을(를) 클릭합니다. **[!UICONTROL Save]**.

### 4단계: 페이지에 동적 블록 추가

1. 다음에서 _관리자_ 사이드바, 이동 **[!UICONTROL Content]** > _[!UICONTROL Elements]_>**[!UICONTROL Pages]**

1. 다음 찾기 _단순 페이지_ 에서 생성한 항목 [첫 번째 연습 연습](1-simple-page.md) 편집 모드로 엽니다.

1. 확장 ![확장 선택기](../assets/icon-display-expand.png) 다음 **[!UICONTROL Content]** 섹션 및 클릭 **[!UICONTROL Edit with Page Builder]**.

1. 동적 블록과 동일한 이미지를 사용하여 맨 위 행에 마우스를 가져다 대면 도구 상자와 _제거_ ( ![제거 아이콘](./assets/pb-icon-remove.png){width="20"} ) 아이콘.

   페이지에서 행 제거를 확인하려면  **[!UICONTROL OK]** .

1. 다음에서 [!DNL Page Builder] 패널 아래 _[!UICONTROL Layout]_, 새 항목 드래그&#x200B;**[!UICONTROL Row]**자리 표시자를 스테이지 맨 위에 추가합니다.

1. 다음에서 [!DNL Page Builder] 패널, 확장 **[!UICONTROL Add Content]** 드래그 **[!UICONTROL Dynamic Block]** 자리 표시자를 새 행에 추가합니다.

   ![동적 블록을 행으로 드래그](./assets/pb-dynamic-block-drag.png){width="600" zoomable="yes"}

1. 동적 블록 컨테이너에 마우스를 가져다 대고 도구 상자를 표시한 다음 _설정_ ( ![설정 아이콘](./assets/pb-icon-settings.png){width="20"} ) 아이콘.

   ![동적 블록 도구 상자](./assets/pb-dynamic-block-settings.png){width="600" zoomable="yes"}

1. 다음에서 _[!UICONTROL Edit Dynamic Block]_페이지, 클릭&#x200B;**[!UICONTROL Select Dynamic Block]**.

   ![동적 블록 선택](./assets/pb-dynamic-block-select.png){width="600" zoomable="yes"}

1. 다음 찾기 _[!DNL Tee Shirt Promo]_만든 동적 블록 및 클릭&#x200B;**[!UICONTROL Select]**.

   동적 블록 정보의 요약이 아래에 나타납니다.

   ![동적 블록 정보](./assets/pb-tutorial2-dynamic-block-edit.png){width="600" zoomable="yes"}

1. 기본값 적용 **[!UICONTROL Template]**, `Dynamic Block Block Template`.

1. 완료되면 다음을 클릭하십시오. **[!UICONTROL Save]** 설정을 저장하고 [!DNL Page Builder] 작업 영역.

   ![페이지 미리보기의 동적 블록](./assets/pb-tutorial2-dynamic-block-on-page.png){width="600" zoomable="yes"}

1. 스테이지의 오른쪽 위 모서리에서 _전체 화면 닫기_ (![전체 화면 아이콘 닫기](./assets/pb-icon-reduce.png)) 아이콘.

   이 아이콘을 클릭하면 _[!UICONTROL Content]_미리보기가 표시된 페이지의 섹션입니다.

1. 오른쪽 위 모서리에서 **[!UICONTROL Save]** 화살표 및 선택 **[!UICONTROL Save & Close]**.

블록 연습의 두 번째 부분을 완료했습니다. 참고용으로 작업한 것을 잊지 말아라.

## 3부: 동적 블록 업데이트

연습의 마지막 부분에서는 페이지가 스토어에서 라이브되는 동안 동적 블록을 편집합니다. 그런 다음 고객 세그먼트의 멤버로 스토어에 로그인하여 블록이 나타나도록 합니다.

![상점 첫 화면의 샘플 동적 블록](./assets/pb-tutorial2-dynamic-block-storefront.png){width="600" zoomable="yes"}

### 1단계: 동적 블록 편집

1. 다음에서 _관리자_ 사이드바, 이동 **[!UICONTROL Content]** > _[!UICONTROL Elements]_>**[!UICONTROL Dynamic Blocks]**.

1. 다음 항목 찾기 _[!DNL Tee Shirt Promo]_그리드에서 동적 블록을 열고 편집 모드로 엽니다.

1. 확장 ![확장 선택기](../assets/icon-display-expand.png) 다음 **[!UICONTROL Content]** 섹션 및 클릭 **[!UICONTROL Edit with Page Builder]**.

1. 열 너비를 변경합니다.

   - 두 열 사이의 테두리를 마우스로 가리킵니다.

   - 마우스 단추를 누른 채 테두리 두 구획을 왼쪽으로 드래그합니다.

     ![격자 나누기](./assets/pb-tutorial2-dynamic-block-edit-column-width.png){width="600" zoomable="yes"}

     이제 첫 번째 열은 12개(4/12) 격자 분할 중 4개 너비이고 두 번째 열은 12개(8/12) 분할 중 8개 너비입니다.

     ![같지 않은 두 열](./assets/pb-tutorial2-dynamic-block-edit-column-width-changed.png){width="600" zoomable="yes"}

1. 텍스트 색상 변경:

   - 처음 두 줄의 텍스트를 선택합니다.

   - 편집기 도구 모음에서 를 선택합니다 **[!UICONTROL Text Color]** 을(를) 클릭하고 **[!UICONTROL White]** 견본.

   ![텍스트 색상](./assets/pb-tutorial2-dynamic-block-edit-text-color.png){width="600" zoomable="yes"}

1. 스테이지의 오른쪽 위 모서리에서 _전체 화면 닫기_ (![전체 화면 아이콘 닫기](./assets/pb-icon-reduce.png)) 아이콘.

   이 아이콘을 클릭하면 _[!UICONTROL Content]_미리보기가 표시된 동적 블록에 대한 섹션입니다.

1. 오른쪽 위 모서리에서 을(를) 클릭합니다. **[!UICONTROL Save]**.

### 2단계: 동적 블록 보기

이 동적 블록은 특정 고객 세그먼트의 구성원에게만 표시되므로 고객 세그먼트의 구성원인 고객으로 로그인하여 판촉을 확인해야 합니다. 이 예에서는 블록이 여성 고객에게만 표시됩니다.

1. 상점으로 브라우저 창을 엽니다.

1. 샘플 페이지를 보려면 주소 표시줄의 URL을 다음과 같이 수정하십시오.

   mystore.com/sample-page

   스토어에서 html 접미사를 포함하도록 구성한 경우 접미사를 다음과 같이 포함하십시오.

   mystore.com/sample-page.html

1. 여성 고객으로 로그인:

   - 홈 페이지의 오른쪽 위 모서리에서 **[!UICONTROL Sign In]**.

   - 샘플 Luma 데이터가 시스템에 설치된 경우 다음 자격 증명을 사용합니다.

     **[!UICONTROL Email]** - `roni_cost@example.com`

     **[!UICONTROL Password]** -  `roni_cost3@example.com`

   - 클릭 **[!UICONTROL Sign In]**.

   - Tee Shirt 프로모션으로 만든 다이내믹 블록을 보려면 샘플 페이지로 돌아갑니다.

   ![고객 세그먼트에 대해 표시되는 동적 블록](./assets/pb-tutorial2-dynamic-block-storefront.png){width="700" zoomable="yes"}

차단 연습을 완료했습니다. 참고용으로 작업한 것을 잊지 말아라.

준비가 되면 다음 작업을 수행하십시오. [3부: 카탈로그 컨텐츠](3-catalog-content.md)

[1]: https://developers.google.com/maps/documentation/javascript/get-api-key
