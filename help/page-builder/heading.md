---
title: 요소 - 제목
description: 제목 수준이 H1부터 H6까지 있는 텍스트 컨테이너를  [!DNL Page Builder] 단계까지 추가하는 데 사용되는 제목 콘텐츠 유형에 대해 알아봅니다.
exl-id: dc51e7f6-a235-49dc-a978-1419a63fa33e
feature: Page Builder, Page Content
source-git-commit: 4a3aa2aa32b692341edabd41fdb608e3cff5d8e0
workflow-type: tm+mt
source-wordcount: '941'
ht-degree: 0%

---

# 요소 - 제목

제목 수준은 콘텐츠를 구성하고 검색 엔진이 각 페이지를 색인화하는 데 도움이 되는 계층을 설정합니다. _단계_&#x200B;에서 [[!DNL Page Builder] 제목](workspace.md#stage) 콘텐츠 형식을 사용하여 H1부터 H6까지의 제목 수준이 있는 텍스트 컨테이너를 단계에 추가하십시오. 머리글은 현재 테마와 연결된 스타일시트에 따라 서식이 지정됩니다.

[&#x200B; 섹션의 &#x200B;](workspace.md)콘텐츠 제목&#x200B;_[!UICONTROL Content]_&#x200B;필드를 사용하여 H1 제목을 페이지 맨 위에 추가할 수 있습니다. 그러나 이 필드는 이전 [!DNL Commerce] 버전의 레거시이며 이전 콘텐츠를 지원하기 위해 제공됩니다. 이 필드에서는 [!DNL Page Builder]의 고급 기능을 사용하지 않습니다. 콘텐츠 제목 필드를 비워 두고 [!DNL Page Builder] 제목 콘텐츠 형식을 사용하여 모든 수준의 제목을 페이지에 추가하는 것이 좋습니다.

다음 예제에서는 Luma 테마로 서식을 지정할 때 컨텐츠 제목과 제목 컨텐츠 유형이 어떻게 표시되는지 보여줍니다.

![상점 첫 화면의 콘텐츠 제목 및 제목 수준](./assets/pb-storefront-heading-levels.png){width="700" zoomable="yes"}

_패널의_&#x200B;요소[!DNL Page Builder] 섹션에서 머리글을 스테이지의 행, 열 또는 탭 집합으로 드래그할 수 있습니다. 제목 수준과 맞춤은 스테이지의 편집기 도구 모음에서 제어하거나 _설정_( ![설정 아이콘](./assets/pb-icon-settings.png){width="20"} ) 컨트롤을 사용하여 제어할 수 있습니다.

{{$include /help/_includes/page-builder-save-timeout.md}}

## 제목 편집기

![도구 모음이 있는 제목 편집기](./assets/pb-elements-heading-toolbar.png){width="500" zoomable="yes"}

## 머리글 컨테이너 도구 상자

모든 콘텐츠 컨테이너와 마찬가지로 컨테이너 위로 마우스를 가져가면 도구 상자가 나타납니다.

![머리글 컨테이너 도구 상자](./assets/pb-elements-heading-toolbox.png){width="500" zoomable="yes"}

| 도구 | 아이콘 | 설명 |
| --------- | ----------------- | ---------------------- |
| 이동 | ![이동 아이콘](./assets/pb-icon-move.png){width="25"} | 머리글 컨테이너를 페이지의 다른 유효한 위치로 이동합니다. |
| (레이블) | 제목 | 현재 컨테이너를 머리글로 식별합니다. |
| 설정 | ![설정 아이콘](./assets/pb-icon-settings.png){width="25"} | 컨테이너의 속성을 변경할 수 있는 제목 편집 페이지를 엽니다. |
| 숨기기 | ![아이콘 숨기기](./assets/pb-icon-hide.png){width="25"} | 제목 컨테이너를 숨깁니다. |
| 표시 | ![아이콘 표시](./assets/pb-icon-show.png){width="25"} | 숨겨진 제목 컨테이너를 표시합니다. |
| 복제 | ![중복 아이콘](./assets/pb-icon-duplicate.png){width="25"} | 제목 컨테이너의 복사본을 만듭니다. |
| 제거 | ![제거 아이콘](./assets/pb-icon-remove.png){width="25"} | 스테이지에서 제목 컨테이너와 그 컨텐츠를 삭제합니다. |

{style="table-layout:auto"}

{{$include /help/_includes/page-builder-hidden-element-note.md}}

## 제목 추가

1. [!DNL Page Builder] 패널에서 **[!UICONTROL Elements]**&#x200B;을(를) 확장하고 **[!UICONTROL Heading]** 자리 표시자를 스테이지의 행, 열 또는 탭 집합으로 드래그합니다.

   ![제목을 스테이지로 드래그](./assets/pb-elements-heading-drag.png){width="600" zoomable="yes"}

1. 편집기에서 `Edit Heading Text` 자리 표시자 위에 머리글 텍스트를 입력합니다.

   기본적으로 제목 텍스트에는 레벨 2(H2) 제목 유형이 지정됩니다.

   ![제목 편집기의 자리 표시자](./assets/pb-elements-header-editor-placeholder.png){width="500" zoomable="yes"}

1. 도구 모음에서 H1과 H6 중 적절한 제목 유형을 선택합니다.

1. 필요한 경우 정렬을 변경합니다.

## 헤더 설정 편집

1. 제목 컨테이너 위로 마우스를 가져가면 도구 상자를 표시하고 _설정_(![설정 아이콘](./assets/pb-icon-settings.png){width="20"} ) 아이콘을 선택합니다.

   ![제목 도구 상자](./assets/pb-elements-heading-toolbox.png){width="500" zoomable="yes"}

1. 필요한 경우 제목 콘텐츠(**[!UICONTROL Heading Type]** 및 **[!UICONTROL Heading Text]**)를 업데이트합니다.

   머리글 편집기에서 이 콘텐츠를 업데이트할 수도 있습니다.

1. 필요에 따라 _[!UICONTROL Advanced]_&#x200B;설정을 업데이트합니다.

   - 상위 컨테이너 내의 머리글 위치를 제어하려면 **[!UICONTROL Alignment]**&#x200B;을(를) 선택하세요.

     | 옵션 | 설명 |
     | ------ | ----------- |
     | `Default` | 현재 테마의 스타일시트에 지정된 정렬 기본 설정을 적용합니다. |
     | `Left` | 지정된 패딩을 허용하여 부모 컨테이너의 왼쪽 테두리를 따라 목록을 정렬합니다. |
     | `Center` | 지정된 패딩을 허용하여 부모 컨테이너의 중앙에 있는 목록을 정렬합니다. |
     | `Right` | 지정된 패딩을 허용하여 부모 컨테이너의 오른쪽 테두리를 따라 블록을 정렬합니다. |

     {style="table-layout:auto"}

   - 제목 컨테이너의 네 면 모두에 적용되는 **[!UICONTROL Border]** 스타일을 설정합니다.

     | 옵션 | 설명 |
     | ------ | ----------- |
     | `Default` | 연관된 스타일 시트에서 지정한 기본 테두리 스타일을 적용합니다. |
     | `None` | 컨테이너 테두리를 시각적으로 표시하지 않습니다. |
     | `Dotted` | 컨테이너 테두리가 점선으로 표시됩니다. |
     | `Dashed` | 컨테이너 테두리는 파선으로 표시됩니다. |
     | `Solid` | 컨테이너 테두리가 실선으로 표시됩니다. |
     | `Double` | 컨테이너 테두리는 이중 선으로 표시됩니다. |
     | `Groove` | 컨테이너 테두리는 홈이 있는 선으로 표시됩니다. |
     | `Ridge` | 컨테이너 테두리는 절선으로 표시됩니다. |
     | `Inset` | 컨테이너 테두리는 인세트 선으로 표시됩니다. |
     | `Outset` | 컨테이너 테두리는 외곽선으로 표시됩니다. |

     {style="table-layout:auto"}

   - `None` 이외의 테두리 스타일을 설정하는 경우 테두리 표시 옵션을 완료하십시오.

     | 옵션 | 설명 |
     | ------ |------------ |
     | [!UICONTROL Border Color] | 색상 견본을 선택하거나 색상 선택기를 클릭하거나 유효한 색상 이름 또는 이에 해당하는 16진수 값을 입력하여 색상을 지정합니다. |
     | [!UICONTROL Border Width] | 테두리 라인 너비의 픽셀 수를 입력합니다. |
     | [!UICONTROL Border Radius] | 테두리의 각 모퉁이를 둥글게 만드는 데 사용되는 반경의 크기를 정의하려면 픽셀 수를 입력합니다. |

     {style="table-layout:auto"}

   - (선택 사항) 컨테이너에 적용할 현재 스타일 시트의 **[!UICONTROL CSS classes]** 이름을 지정합니다.

     여러 클래스 이름은 공백으로 구분합니다.

   - **[!UICONTROL Margins and Padding]**&#x200B;에 대한 값을 픽셀 단위로 입력하여 머리글 컨테이너의 외부 여백과 내부 패딩을 결정합니다.

     다이어그램에 해당 값을 입력합니다.

     | 컨테이너 영역 | 설명 |
     | -------------- | ----------- |
     | [!UICONTROL Margins] | 컨테이너의 모든 면 바깥쪽 가장자리에 적용되는 빈 공간의 양입니다. 옵션: `Top` / `Right` / `Bottom` / `Left` |
     | [!UICONTROL Padding] | 컨테이너의 모든 측면 안쪽 가장자리에 적용되는 빈 공간의 양입니다. 옵션: `Top` / `Right` / `Bottom` / `Left` |

     {style="table-layout:auto"}

1. 완료되면 **[!UICONTROL Save]**&#x200B;을(를) 클릭하여 설정을 적용하고 [!DNL Page Builder] 작업 영역으로 돌아갑니다.

## 제목 복제

특정 설정이 있는 서식이 지정된 머리글의 경우 새 자리 표시자로 다시 시작하는 것보다 머리글을 복제하는 것이 더 효율적입니다.

1. 제목 컨테이너 위로 마우스를 가져가면 도구 상자를 표시하고 _복제_(![복제 아이콘](./assets/pb-icon-duplicate.png){width="20"}) 아이콘을 선택합니다.

   복제본이 원본 바로 아래에 나타납니다.

   ![제목 컨테이너 복제](./assets/pb-elements-heading-duplicate.png){width="500" zoomable="yes"}

1. 새 제목 컨테이너 위로 마우스를 가져가면 도구 상자를 표시하고 _이동_( ![이동 아이콘](./assets/pb-icon-move.png){width="20"} ) 아이콘을 선택합니다.

   ![제목 이동](./assets/pb-elements-heading-move.png){width="500" zoomable="yes"}

1. 빨간색 지침이 새 위치를 표시할 때까지 제목을 선택하고 드래그합니다.

   머리글이 이동하는 동안 각 컨테이너의 위쪽 및 아래쪽 테두리가 파선으로 표시됩니다.

   ![중복된 제목을 위치로 이동](./assets/pb-elements-heading-move-guideline.png){width="500" zoomable="yes"}

1. 제목 수준을 변경하려면 제목 텍스트를 클릭하고 편집기 도구 모음에서 새 수준을 선택합니다.

   ![새 제목 수준 선택](./assets/pb-elements-heading-change-heading-level.png){width="500" zoomable="yes"}

<!-- Last updated from includes: 2023-09-11 14:30:19 -->
