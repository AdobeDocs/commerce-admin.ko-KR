---
title: 카테고리 - 디자인 설정
description: '[!UICONTROL Design] 설정을 사용하여 범주의 모양과 느낌, 연결된 모든 제품 페이지 및 페이지 레이아웃을 정의하는 방법에 대해 알아봅니다.'
exl-id: 6dc216ac-1c52-4196-9c93-e5cad19901b5
feature: Catalog Management, Categories, Page Content
source-git-commit: 01148770946a236ece2122be5a88b963a0f07d1f
workflow-type: tm+mt
source-wordcount: '372'
ht-degree: 0%

---

# 카테고리 - 디자인 설정

_[!UICONTROL Design]_&#x200B;섹션을 통해 범주의 모양과 느낌, 연결된 모든 제품 페이지 및 페이지 레이아웃을 제어할 수 있습니다. 프로모션을 위해 카테고리 페이지 및 관련 제품을 사용자 정의하거나 카테고리를 구별할 수 있습니다. 예를 들어, 브랜드나 특수 제품 라인에 대한 독특한 디자인을 개발하거나 특정 기간에 대한 업데이트를 적용할 수 있습니다.

![범주에 대한 디자인 설정](./assets/category-design.png){width="600" zoomable="yes"}

>[!NOTE]
>
>각 범주에 대해 디자인 설정이 다른 여러 범주에 동일한 제품이 할당되면 [검색 엔진 최적화 구성 옵션](../configuration-reference/catalog/catalog.md#search-engine-optimization)에서 **제품 URL에 대한 범주 경로 사용** = `Yes`을 설정하는 것이 좋습니다. 이 설정에 액세스하려면 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**(으)로 이동하여&#x200B;**[!UICONTROL Catalog]**&#x200B;을(를) 확장하고 왼쪽 패널의 아래에 있는&#x200B;**카탈로그**&#x200B;를 선택한 다음 페이지의&#x200B;**검색 엔진 최적화**&#x200B;섹션을 확장하세요.

| 필드 | 설명 |
|--- |--- |
| [!UICONTROL Use Parent Category Settings] | 현재 범주가 상위 범주에서 디자인 설정을 상속하도록 허용합니다. 이 필드를 사용하면 디자인 섹션의 다른 모든 필드를 사용할 수 없게 됩니다. 옵션: `Yes` / ` No` |
| [!UICONTROL Theme] | 사용자 지정 테마를 범주에 적용합니다. |
| [!UICONTROL Layout] | 카테고리 페이지에 다른 레이아웃을 적용합니다. 옵션: <br/>**[!UICONTROL No layout updates]**- 기본적으로 범주 페이지에는 레이아웃 업데이트를 사용할 수 없습니다.<br/>**[!UICONTROL Empty]** - 고유한 페이지 레이아웃을 정의하는 데 사용합니다. (XML에 대한 이해가 필요합니다.) <br/>**[!UICONTROL 1 column]**- 1열 레이아웃을 범주 페이지에 적용합니다.<br/>**[!UICONTROL 2 columns with left bar]** - 왼쪽 사이드바가 있는 2열 레이아웃을 범주 페이지에 적용합니다. <br/>**[!UICONTROL 2 columns with right bar]**- 오른쪽 사이드바가 있는 2열 레이아웃을 범주 페이지에 적용합니다.<br/>**[!UICONTROL 3 columns]** - 범주 페이지에 3열 레이아웃을 적용합니다.<br/>**[!UICONTROL Page -- Full Width]**- ([페이지 빌더](../page-builder/introduction.md) 필요) CMS 페이지의 전체 너비 레이아웃을 범주 페이지에 적용합니다.<br/>**[!UICONTROL Category -- Full Width]** - (페이지 빌더 필요) 범주 페이지에 대한 전체 너비 레이아웃을 범주 페이지에 적용합니다. <br/>**[!UICONTROL Product -- Full Width]**- (Page Builder 필요) 제품 페이지의 전체 너비 레이아웃을 범주 페이지에 적용합니다. |
| [!UICONTROL Custom Layout Update] | 서버에서 사용 가능한 사용자 지정 레이아웃 업데이트 파일을 나열합니다. 범주에 적용할 사용자 정의 레이아웃 업데이트를 선택합니다. |
| [!UICONTROL Apply Design to Products] | 선택하면 카테고리의 모든 제품에 사용자 지정 설정이 적용됩니다. |

{style="table-layout:auto"}

## [!UICONTROL Scheduled Design Update]

{{ce-feature}}

_[!UICONTROL Scheduled Design Update]_&#x200B;섹션은 사용자 지정 디자인을 범주 페이지에 적용할 날짜 범위를 결정합니다.

| 필드 | 설명 |
|--- |--- |
| [!UICONTROL Schedule Update From/To] | 사용자 지정 레이아웃을 범주에 적용할 때의 날짜 범위를 결정합니다. |

![예약된 디자인 업데이트](./assets/category-scheduled-design-update.png){width="600" zoomable="yes"}
