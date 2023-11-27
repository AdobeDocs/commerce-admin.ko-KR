---
title: 페이지 추가 및 제거
description: 에 사용된 콘텐츠 페이지를 추가 및 제거하는 방법을 알아봅니다. [!DNL Commerce] 저장.
exl-id: a7a503ea-3631-4be2-81e4-aed2ae9419dc
source-git-commit: b659c7e1e8f2ae9883f1e24d8045d6dd1e90cfc0
workflow-type: tm+mt
source-wordcount: '1091'
ht-degree: 0%

---

# 페이지 추가 및 제거

콘텐츠 페이지를 스토어에 추가하는 프로세스는 기본적으로 만들려는 모든 페이지 유형에 대해 동일합니다. 텍스트, 이미지, 콘텐츠 블록, 변수 및 위젯을 포함할 수 있습니다. 대부분의 콘텐츠 페이지는 검색 엔진별로 먼저 읽고 사람이 두 번째로 읽도록 디자인되었습니다. 페이지 제목 및 URL을 선택할 때와 메타 데이터 및 컨텐츠를 작성할 때 이러한 서로 다른 두 대상의 요구 사항을 염두에 두십시오. 페이지가 완료되면 저장소 탐색에 추가하거나, 다른 페이지에 연결하거나, 저장소의 바닥글에서 연결하거나, 새 페이지로 사용할 수 있습니다 [홈 페이지](page-home-new.md).

![페이지 그리드](./assets/pages-grid.png){width="700" zoomable="yes"}

## 페이지 추가

다음 지침은 기본 페이지를 만드는 각 단계를 설명합니다. 일부 고급 기능은 생략되었지만 다른 항목에서 다룹니다.

### 1단계: 페이지 만들기

1. 다음에서 _관리자_ 사이드바, 이동 **[!UICONTROL Content]** > _[!UICONTROL Elements]_>**[!UICONTROL Pages]**.

1. 클릭 **[!UICONTROL Add New Page]**.

   ![새 페이지](./assets/pages-new-page.png){width="600" zoomable="yes"}

1. 페이지를 즉시 게시하지 않으려면 을(를) 설정합니다 **[!UICONTROL Enable Page]** 끝 `No`.

1. 다음을 입력합니다. **[!UICONTROL Page Title]**.

   페이지 제목이 다음에 표시됩니다. [이동 경로](../catalog/navigation-breadcrumb-trail.md) 탐색.

### 2단계: 콘텐츠 완료

다음에 따라 [고급 콘텐츠 도구 구성](../configuration-reference/general/content-management.md), 페이지 콘텐츠를 추가합니다.

#### 페이지 빌더 콘텐츠 도구 사용

1. 확장 ![확장 선택기](../assets/icon-display-expand.png) **[!UICONTROL Content]**.

   ![페이지 빌더가 있는 콘텐츠](../page-builder/assets/pb-page-content.png){width="600" zoomable="yes"}

1. 다음에서 **[!UICONTROL Content Heading]** 상자에 페이지 맨 위에 표시할 머리글을 입력합니다.

   활성화된 경우 [페이지 빌더](../page-builder/introduction.md) 단계 및 패널이 콘텐츠 제목 아래에 표시됩니다. 자세한 내용은 [작업 영역](../page-builder/workspace.md). If _페이지 빌더_ 가 활성화되어 있지 않으면 편집기가 WYSIWYG 모드로 열리고 도구 모음이 맨 위에 있습니다.

1. 콘텐츠를 완성하고 필요에 따라 텍스트 서식을 지정합니다.

#### 편집기 도구 모음 사용

1. 확장 ![확장 선택기](../assets/icon-display-expand.png) **[!UICONTROL Content]**.

   ![콘텐츠](./assets/page-content-editor.png){width="600" zoomable="yes"}

1. 다음에서 **[!UICONTROL Content Heading]** 상자에 페이지 맨 위에 표시할 머리글을 입력합니다.

1. 콘텐츠를 완성하고 필요에 따라 텍스트 형식을 지정합니다.

   다음을 추가할 수 있습니다. [이미지](media-storage.md), [변수](../systems/variables-predefined.md), 및 [위젯](widgets.md) 필요한 경우. 자세한 내용은 [편집기 사용](editor.md).

### 3단계: SEO 정보 작성

1. 확장 ![확장 선택기](../assets/icon-display-expand.png) **[!UICONTROL Search Engine Optimization]**.

   ![검색 엔진 최적화](./assets/page-search-engine-optimization.png){width="600" zoomable="yes"}

1. 기본값을 사용하거나 다른 값을 입력하십시오. **[!UICONTROL URL Key]** 모든 소문자로 구성되며 공백 대신 하이픈이 사용됩니다.

   기본 URL 키는 페이지가 저장될 때 생성되었으며 콘텐츠 머리글을 기반으로 합니다.

1. 입력 **[!UICONTROL Meta Title]** 을 참조하십시오.

   메타 제목은 70자 미만이어야 하며 브라우저 제목 표시줄 및 탭에 표시됩니다.

1. 선택한 고가치 항목 입력 **[!UICONTROL Meta Keywords]** 해당 검색 엔진은 를 사용하여 페이지를 색인화할 수 있습니다.

   여러 단어는 쉼표로 구분하십시오. 메타 키워드는 일부 검색 엔진에서 무시되지만 다른 검색 엔진에서 사용됩니다.

1. 대상 **[!UICONTROL Meta Description]**: 검색 결과 목록 페이지에 대한 간단한 설명을 입력합니다.

   설명은 150~160자 길이여야 하며 최대 255자로 제한됩니다.

1. 클릭 **[!UICONTROL Save]**.

### 4단계: 페이지 범위 지정

1. 확장 ![확장 선택기](../assets/icon-display-expand.png) **[!UICONTROL Page in Websites]**.

   ![웹 사이트의 페이지](./assets/page-in-websites.png){width="600" zoomable="yes"}

1. 다음에서 **[!UICONTROL Store View]** 목록에서 페이지를 사용할 수 있는 각 보기를 선택합니다.

   설치에 여러 웹 사이트가 있는 경우 페이지를 사용할 수 있는 각 웹 사이트 및 스토어 보기를 선택합니다.

### 5단계: 상위 페이지 식별(해당되는 경우)

{{ee-feature}}

1. 확장 ![확장 선택기](../assets/icon-display-expand.png) **[!UICONTROL Hierarchy]**.

   ![계층](./assets/page-hierarchy.png){width="600" zoomable="yes"}

1. 이 페이지가 다른 페이지의 하위 페이지인 경우 **[!UICONTROL Parent page]**.

### 6단계: 설계 변경 사항 입력(선택 사항)

1. 페이지 레이아웃을 변경하려면 ![확장 선택기](../assets/icon-display-expand.png) **[!UICONTROL Design]**.

   ![디자인](./assets/page-design.png){width="600" zoomable="yes"}

1. 페이지의 열 레이아웃을 변경하려면 **[!UICONTROL Layout]** 다음 중 하나를 수행합니다.

   - `Empty`
   - `1 column`
   - `2 columns with left bar`
   - `2 columns with right bar`
   - `3 columns`
   - `Page -- Full Width` (필수 [페이지 빌더](../page-builder/introduction.md))
   - `Category -- Full Width` (페이지 빌더 필요)
   - `Product -- Full Width` (페이지 빌더 필요)

1. 를 적용하려면 **[!UICONTROL Custom Layout Update]**&#x200B;목록에서 파일 이름을 선택합니다.

   자세한 내용은 [레이아웃 업데이트](layout-updates.md).

1. 페이지의 테마를 변경하려면 다음을 설정하십시오. **[!UICONTROL New Theme]** 다음 중 하나를 수행합니다.

   - `Magento Black`
   - `Magento Luma`

1. ![Magento Open Source](../assets/open-source.svg) (Magento Open Source 전용) 디자인 변경을 예약하려면 ![확장 선택기](../assets/icon-display-expand.png) **[!UICONTROL Custom Design Update]** 다음을 수행합니다.

   ![사용자 정의 디자인 업데이트](./assets/page-custom-design-update.png){width="600" zoomable="yes"}

   - 달력(![달력 아이콘](../assets/icon-calendar.png))을 클릭하여 선택합니다 **[!UICONTROL From]** 및 **[!UICONTROL To]** 변경 사항이 적용되는 날짜.

   - 페이지에 다른 테마를 적용하려면 **[!UICONTROL New Theme]**.

   - 페이지의 열 레이아웃을 변경하려면 **[!UICONTROL Layout]** 을(를) 적용합니다.

### 7단계: 페이지 미리보기

1. 다음을 클릭합니다. **[!UICONTROL Save]** 화살표 및 선택 **[!UICONTROL Save & Close]** 을 클릭하여 페이지 그리드로 돌아갑니다.

1. 그리드에서 페이지를 찾아 다음을 선택합니다. **[!UICONTROL View]** 다음에서 _[!UICONTROL Action]_열.

1. 그리드로 돌아가려면 **[!UICONTROL Back]** 을 클릭합니다.

### 8단계: 페이지 게시

1. 선택 **[!UICONTROL Edit]** 다음에서 _[!UICONTROL Action]_표의 열입니다.

1. 설정 **[!UICONTROL Enable Page]** 끝 `Yes`.

1. 다음을 클릭합니다. **[!UICONTROL Save]** 화살표 및 선택 **[!UICONTROL Save & Close]**.

## 페이지 복제

컨텐츠 페이지는 템플릿으로 사용할 수 있으며, 중복으로 저장할 수 있습니다. 이 시간 절약 기법을 사용하여 사이트 전체의 콘텐츠 페이지에 대해 일관된 디자인을 만들 수 있습니다. 중복 페이지는 원본의 페이지 제목을 유지하지만 URL 키 및 상태 필드는 업데이트해야 합니다.

![저장 및 복제](./assets/page-duplicate-save-menu.png){width="600" zoomable="yes"}

1. 다음에서 _관리자_ 사이드바, 이동 **[!UICONTROL Content]** > _[!UICONTROL Elements]_>**[!UICONTROL Pages]**.

1. 그리드에서 복제할 페이지를 찾은 다음 를 클릭합니다. **[!UICONTROL Edit]** 다음에서 _[!UICONTROL Action]_열.

1. 다음을 클릭합니다. **[!UICONTROL Save]** 화살표 및 선택 **[!UICONTROL Save & Duplicate]**.

1. 페이지가 저장되고 복제되었다는 메시지가 표시되면 다음을 클릭합니다. **[!UICONTROL Back]** 맨 위 단추 모음에서 그리드로 돌아갑니다.

1. 그리드에서 중복 페이지를 찾아 다음 사항에 유의하십시오.

   - 페이지 제목 은 원본과 동일합니다.
   - 고유하지만 임시 URL 키가 할당됩니다.
   - 페이지의 상태는 다음과 같습니다. `Disabled`.

1. 에서 중복 페이지를 엽니다. _편집_ 을 클릭하고 다음을 수행합니다.

   - 페이지를 즉시 게시하려면 을(를) 설정합니다 **[!UICONTROL Enable Page]** 끝 `Yes`.

   - 업데이트 **[!UICONTROL Page Title]**, 필요한 경우.

   - 확장 ![확장 선택기](../assets/icon-display-expand.png) 다음 **[!UICONTROL Search Engine Optimization]** 섹션을 만들고 고유 항목 입력 **[!UICONTROL URL Key]** 중복 페이지에 사용할 수 있습니다.

     ![임시 URL 키](./assets/page-search-engine-optimization-url-key-duplicate.png){width="600" zoomable="yes"}

   - 필요에 따라 나머지 페이지 콘텐츠를 업데이트합니다.

1. 다음을 클릭합니다. **[!UICONTROL Save]** 화살표 및 선택 **[!UICONTROL Save & Close]**.

   그리드의 중복 페이지는 변경 사항을 반영합니다.

## 저장 메뉴

| 명령 | 설명 |
|--- |--- |
| [!UICONTROL Save] | 현재 페이지를 저장하고 작업을 계속합니다. |
| [!UICONTROL Save & New] | 현재 페이지를 저장하고 닫은 다음 새 페이지를 시작합니다. |
| [!UICONTROL Save & Duplicate] | 현재 페이지를 저장하고 닫은 다음 새 복사본을 엽니다. |
| [!UICONTROL Save & Close] | 현재 페이지를 저장하고 닫은 다음 페이지 그리드로 돌아갑니다. |

{style="table-layout:auto"}

## 페이지 삭제

생성된 페이지를 제거하는 방법에는 두 가지가 있습니다. 다음에서 제거할 수 있습니다. _[!UICONTROL Pages]_격자선 또는_[!UICONTROL Edit]_ 페이지를 가리키도록 업데이트하는 중입니다.

### 방법 1: 페이지 그리드에서 페이지 제거

1. 다음에서 _관리자_ 사이드바, 이동 **[!UICONTROL Content]** > _[!UICONTROL Elements]_>**[!UICONTROL Pages]**.

1. 그리드 위에서 필터를 사용하여 페이지를 찾은 다음 삭제할 하나 이상의 페이지에 대한 확인란을 선택합니다.

1. 목록의 왼쪽 상단 모서리에서 을(를) 설정합니다. **[!UICONTROL Actions]** 끝 `Delete`.

1. 작업을 확인하려면 다음을 클릭합니다. **[!UICONTROL OK]**.

### 방법 2: 편집 페이지에서 페이지 제거

1. 다음에서 _관리자_ 사이드바, 이동 **[!UICONTROL Content]** > _[!UICONTROL Elements]_>**[!UICONTROL Pages]**.

1. 삭제할 페이지를 찾습니다.

1. 다음에서 _[!UICONTROL Actions]_페이지 엔티티의 열을 클릭합니다.**[!UICONTROL Select]**및 선택&#x200B;**[!UICONTROL Edit]**.

1. 단추 모음에서 **[!UICONTROL Delete Page]**.

1. 작업을 확인하려면 다음을 클릭합니다. **[!UICONTROL OK]**.
