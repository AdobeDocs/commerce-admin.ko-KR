---
title: 페이지 레이아웃
description: 페이지 레이아웃 섹션 및 기본 레이아웃을 구성하는 방법에 대해 알아봅니다.
exl-id: 397a92cf-6f20-4729-8d7c-c5f672fc1c9a
source-git-commit: b659c7e1e8f2ae9883f1e24d8045d6dd1e90cfc0
workflow-type: tm+mt
source-wordcount: '871'
ht-degree: 0%

---

# 페이지 레이아웃

저장소에 있는 각 페이지의 레이아웃은 페이지의 머리글, 바닥글 및 컨텐츠 영역을 정의하는 고유한 섹션 또는 컨테이너로 구성됩니다. 레이아웃에 따라 각 페이지에는 1개, 2개, 3개 또는 그 이상의 열이 있을 수 있습니다. 레이아웃은 다음과 같이 생각할 수 있습니다. _평면도_ 을 클릭하고, CMS, 제품 및 카테고리 페이지의 기본값으로 사용할 특정 레이아웃을 할당합니다.

페이지에서 콘텐츠 블록은 의 섹션에 따라 사용 가능한 공간을 채우기 위해 부동됩니다. [페이지 레이아웃](layout-updates.md) 할당된 위치에 표시됩니다. 레이아웃을 3열에서 2열 레이아웃으로 변경하면 기본 영역의 콘텐츠가 확장되어 사용 가능한 공간을 채웁니다. 또한 사용되지 않은 사이드바와 연관된 모든 블록이 사라지는 것처럼 보입니다. 그러나 3열 레이아웃을 복원하면 블록이 다시 나타납니다. 이 유동적 접근법, 또는 _유동적 배치_&#x200B;를 사용하면 콘텐츠를 다시 작업하지 않고도 페이지 레이아웃을 변경할 수 있습니다. 개별 HTML 페이지로 작업하는 데 익숙한 경우 이 모듈에서는 _빌딩 블록_ 접근 방식은 다른 사고 방식을 필요로 한다.

![왼쪽 막대 페이지 레이아웃이 있는 표준 2열](./assets/storefront-2-column-ee.png){width="700" zoomable="yes"}

## 기본 레이아웃 구성

1. 다음에서 _관리자_ 사이드바, 이동 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. 아래의 왼쪽 패널에서 _[!UICONTROL General]_, 선택&#x200B;**[!UICONTROL Web]**.

1. 확장 ![확장 선택기](../assets/icon-display-expand.png) 다음 **[!UICONTROL Default Layouts]** 섹션.

   ![기본 레이아웃](./assets/web-default-layouts.png){width="600" zoomable="yes"}

1. 다음을 선택합니다. **[!UICONTROL Default Product Layout]** 제품 페이지에 사용할 수 있습니다.

   이 설정은 제품 페이지에 기본적으로 사용되는 레이아웃을 결정합니다.

   - `No layout updates` - 제품 페이지에 대해 레이아웃 업데이트를 사용할 수 없습니다.
   - `Empty` - 제품 페이지에 빈 레이아웃을 사용합니다.
   - `1 column` - 제품 페이지에 단일 열 레이아웃을 사용합니다.
   - `2 columns with left bar` - 제품 페이지의 왼쪽에 사이드바가 있는 2열 레이아웃을 사용합니다.
   - `2 columns with right bar` - 제품 페이지의 오른쪽에 사이드바가 있는 2열 레이아웃을 사용합니다.
   - `3 columns` - 제품 페이지의 왼쪽 및 오른쪽에 사이드바가 있는 3열 레이아웃을 사용합니다.

   날짜 [페이지 빌더](../page-builder/introduction.md) 이(가) 활성화되어 있으면 추가 전체 너비 옵션을 사용할 수 있습니다. 그런 다음 페이지 빌더 콘텐츠 도구를 사용하여 제품 페이지의 레이아웃을 디자인할 수 있습니다.

   - `Page -- Full Width` - 를 사용합니다. _페이지 - 전체 너비_  제품 페이지 레이아웃.
   - `Category -- Full Width` - 를 사용합니다. _범주 - 전체 폭_ 제품 페이지 레이아웃.
   - `Product -- Full Width` - (권장) _제품 - 전체 폭_ 제품 페이지 레이아웃.

1. 다음을 선택합니다. **[!UICONTROL Default Category Layout]** 범주 페이지에 사용할 수 있습니다.

   이 설정은 범주 페이지에 기본적으로 사용되는 레이아웃을 결정합니다.

   - `No layout updates` - 범주 페이지에는 레이아웃 업데이트를 사용할 수 없습니다.
   - `Empty` - 범주 페이지에 빈 레이아웃을 사용합니다.
   - `1 column` - 범주 페이지에 단일 열 레이아웃을 사용합니다.
   - `2 columns with left bar` - 범주 페이지의 왼쪽에 사이드바가 있는 2열 레이아웃을 사용합니다.
   - `2 columns with right bar` - 범주 페이지의 오른쪽에 사이드바가 있는 2열 레이아웃을 사용합니다.
   - `3 columns` - 범주 페이지의 왼쪽 및 오른쪽에 사이드바가 있는 3열 레이아웃을 사용합니다.

   날짜 [페이지 빌더](../page-builder/introduction.md) 이(가) 활성화되어 있으면 추가 전체 너비 옵션을 사용할 수 있습니다. 그런 다음 페이지 빌더 콘텐츠 도구를 사용하여 범주 페이지의 레이아웃을 디자인할 수 있습니다.

   - `Page -- Full Width` - 를 사용합니다. _페이지 - 전체 너비_ 카테고리 페이지를 위한 레이아웃입니다.
   - `Category -- Full Width` - (권장) _범주 - 전체 폭_ 카테고리 페이지를 위한 레이아웃입니다.
   - `Product -- Full Width` - 를 사용합니다. _제품 - 전체 폭_ 카테고리 페이지를 위한 레이아웃입니다.

1. 다음을 선택합니다. **[!UICONTROL Default Page Layout]** CMS 페이지에 사용할 수 있습니다.

   이 설정은 CMS 페이지에 기본적으로 사용되는 레이아웃을 결정합니다.

   - `No layout updates` - CMS 페이지에 대해 레이아웃 업데이트를 사용할 수 없습니다.
   - `Empty` - CMS 페이지에 대해 빈 레이아웃을 사용합니다.
   - `1 column` - CMS 페이지에 대해 단일 열 레이아웃을 사용합니다.
   - `2 columns with left bar` - CMS 페이지의 왼쪽에 사이드바가 있는 2열 레이아웃을 사용합니다.
   - `2 columns with right bar` - CMS 페이지의 오른쪽에 사이드바가 있는 2열 레이아웃을 사용합니다.
   - `3 columns` - CMS 페이지의 왼쪽 및 오른쪽에 사이드바가 있는 3열 레이아웃을 사용합니다.

   날짜 [페이지 빌더](../page-builder/introduction.md) 이(가) 활성화되어 있으면 추가 전체 너비 옵션을 사용할 수 있습니다. 그런 다음 페이지 빌더 콘텐츠 도구를 사용하여 CMS 페이지의 레이아웃을 디자인할 수 있습니다.

   - `Page -- Full Width` - (권장) _페이지 - 전체 너비_ cms 페이지에 대한 레이아웃입니다.
   - `Category - Full Width` - 를 사용합니다. _범주 - 전체 폭_ cms 페이지에 대한 레이아웃입니다.
   - `Product - Full Width` - 를 사용합니다. _제품 - 전체 폭_ cms 페이지에 대한 레이아웃입니다.

1. 완료되면 다음을 클릭하십시오. **[!UICONTROL Save Config]**.

## 표준 페이지 레이아웃

### 1열

![다이어그램 - 1열 레이아웃](./assets/layout-1-col-th.png){zoomable=&quot;yes&quot;}

다음 _[!UICONTROL 1 Column]_레이아웃을 사용하여 큰 이미지 또는 초점을 갖는 극적인 홈 페이지를 만들 수 있습니다. 또한 랜딩 페이지나 텍스트, 이미지 및 비디오의 조합이 있는 다른 페이지에 적합합니다.

### 왼쪽 막대가 있는 2열

![다이어그램 - 왼쪽 막대가 있는 2열 레이아웃](./assets/layout-2-col-lft-bar-th.png){zoomable=&quot;yes&quot;}

다음 _[!UICONTROL 2 Columns with Left Bar]_레이아웃은 계단식 탐색이 있는 카탈로그 또는 검색 결과 페이지와 같이 왼쪽에 탐색이 있는 페이지에 자주 사용됩니다. 또한 추가 탐색이 필요한 홈 페이지나 왼쪽에 있는 지원 콘텐츠 블록을 위한 탁월한 선택입니다.

### 오른쪽 막대가 있는 두 열

![다이어그램 - 오른쪽 막대가 있는 2열 레이아웃](./assets/layout-2-col-rt-bar-th.png){zoomable=&quot;yes&quot;}

포함 _[!UICONTROL 2 Columns with Right Bar]_레이아웃에서 기본 컨텐츠 영역은 시선을 사로잡는 이미지나 배너에 충분히 큽니다. 이 레이아웃은 오른쪽에 지원 콘텐츠 블록이 있는 제품 페이지에도 자주 사용됩니다.

### 3열

![다이어그램 - 3열 레이아웃](./assets/layout-3-col-th.png){zoomable=&quot;yes&quot;}

다음 _[!UICONTROL 3 Column]_레이아웃에는 페이지의 기본 텍스트를 충분히 크게 볼 수 있는 가운데 열이 있으며 양쪽에 추가 탐색을 위한 공간과 지원 콘텐츠 블록이 있습니다.

### 비어 있음

![다이어그램 - 빈 레이아웃](./assets/layout-blank-th.png){zoomable=&quot;yes&quot;}

다음 _[!UICONTROL Empty]_레이아웃을 사용하여 사용자 지정 페이지 레이아웃을 정의할 수 있습니다.
