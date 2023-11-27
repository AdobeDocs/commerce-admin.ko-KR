---
title: 레이아웃 업데이트
description: 레이아웃 업데이트를 사용하여 페이지 레이아웃을 사용자 지정하는 방법을 알아봅니다.
exl-id: e2d8261f-cae1-4bd4-a047-f861dd7ca14e
source-git-commit: b659c7e1e8f2ae9883f1e24d8045d6dd1e90cfc0
workflow-type: tm+mt
source-wordcount: '1007'
ht-degree: 0%

---

# 레이아웃 업데이트

사용자 지정 레이아웃 업데이트 작업을 시작하기 전에 저장소의 페이지 구성 방법과 용어 간의 차이점을 이해하는 것이 중요합니다 *레이아웃* 및 *레이아웃 업데이트*. 레이아웃은 페이지의 시각적 및 구조적 구성을 나타냅니다. 레이아웃 업데이트는 페이지 작성 방법을 재정의하거나 사용자 지정할 수 있는 특정 XML 명령 집합을 나타냅니다.

의 XML 레이아웃 [!DNL Commerce] 저장소는 컨테이너와 블록의 계층 구조입니다. 일부 요소는 모든 페이지에 표시되고 다른 요소는 특정 페이지에만 표시됩니다. 레이아웃, 컨테이너 및 블록에 대한 자세한 내용은 [레이아웃 개요](https://developer.adobe.com/commerce/frontend-core/guide/layouts/) 다음에서 _프론트엔드 개발자 안내서_.

다음 [위젯](widgets.md) 도구는 기존 을 손쉽게 추가할 수 있는 방법입니다. [콘텐츠 차단](blocks.md) 를 페이지의 기본 레이아웃으로 설정합니다. 고급 업데이트를 수행하려면 서버에 XML 레이아웃 업데이트 코드를 저장한 다음 관리자로부터 사용자 지정 레이아웃 업데이트로 파일을 참조해야 합니다. 프로세스에 대한 개요는 를 참조하십시오. [레이아웃 업데이트 사용](layout-updates.md#place-a-block-using-layout-updates).

다음 다이어그램에서 컨테이너를 참조하는 이름은 검정색이고 블록 유형 또는 블록 클래스 경로는 파란색입니다.

![표준 블록 레이아웃 다이어그램](./assets/page-layout-default.png){width="500" zoomable="yes"}

| 블록 유형 | 설명 |
|--- |--- |
| `page/html` | 이 블록의 이름은 입니다. `root` 레이아웃에 있는 몇 가지 루트 블록 중 하나입니다. 자신만의 블록을 만들고 이름을 지정할 수도 있습니다 `root`: 이 유형의 블록에 대한 표준 이름입니다. 페이지당 이 유형의 블록은 하나만 있을 수 있습니다. |
| `page/html_head` | 블록 이름은 입니다. `head` 루트 블록의 하위 항목입니다. 이 유형의 블록은 페이지당 하나만 있을 수 있으며 제거해서는 안 됩니다. |
| `page/html_notices` | 블록 이름은 입니다. `global_notices` 루트 블록의 하위 항목입니다. 이 블록을 레이아웃에서 제거하면 글로벌 알림이 페이지에 표시되지 않습니다. 페이지당 이 유형의 블록은 하나만 있을 수 있습니다. |
| `page/html_header` | 블록 이름은 입니다. `header` 루트 블록의 하위 항목입니다. 이 블록은 페이지 상단에 있는 시각적 헤더에 해당하며 여러 표준 블록을 포함합니다. 이 유형의 블록은 페이지당 하나만 있을 수 있으며 제거해서는 안 됩니다. |
| `page/html_wrapper` | 이 블록은 기본 레이아웃에 포함되어 있지만 더 이상 사용되지 않으며 이전 버전과의 호환성을 위해 포함되어 있습니다. 이 유형의 블록은 사용하지 마십시오. |
| `page/html_breadcrumbs` | 이 블록의 이름은 입니다. `breadcrumbs` 헤더 블록의 하위 항목입니다. 이 블록에는 현재 페이지의 이동 경로가 표시됩니다. 페이지당 이 유형의 블록은 하나만 있을 수 있습니다. |
| `page/html_footer` | 블록 이름은 입니다. `footer` 루트 블록의 하위 항목입니다. 바닥글 블록은 페이지 하단에 있는 시각적 바닥글에 해당하며 여러 표준 블록을 포함합니다. 이 유형의 블록은 페이지당 하나만 있을 수 있으며 제거해서는 안 됩니다. |
| `page/template_links` | 표준 레이아웃에는 이 유형의 두 개의 블록이 있습니다. 다음 `top.links` 블록은 헤더 블록의 하위 항목이며 위쪽 탐색 메뉴에 해당합니다. 다음 `footer_links` 블록은 바닥글 블록의 하위 항목이며 아래쪽 탐색 메뉴에 해당합니다. <br/><br/>**_참고:_**예제에서와 같이 템플릿 링크를 조작할 수 있습니다. |
| `page/switch` | 표준 레이아웃에는 이 유형의 두 개의 블록이 있습니다. 다음 `store_language` block은 헤더 블록의 하위 항목이며 최상위 언어 전환기에 해당합니다. 다음 `store_switcher` block은 바닥글 블록의 하위 항목이며 아래쪽 스토어 전환기에 해당합니다. |
| 코어/메시지 | 표준 레이아웃에는 이 유형의 두 개의 블록이 있습니다. 다음 `global_messages` 블록은 글로벌 메시지를 표시합니다. 다음 `messages` 블록은 다른 모든 메시지를 표시하는 데 사용됩니다. 이러한 블록을 제거하면 고객에게 메시지가 표시되지 않습니다. |
| `core/text_list` | 이러한 형태의 블록은 광범위하게 사용된다 [!DNL Commerce] 자식 블록을 렌더링하기 위한 자리 표시자입니다. |
| `core/profiler` | 페이지당 이러한 유형의 블록 인스턴스는 한 개만 있습니다. 내부용으로 사용됩니다. [!DNL Commerce] 프로파일러이며 다른 용도로 사용해서는 안 됩니다. |

{style="table-layout:auto"}

## 레이아웃 업데이트를 사용하여 블록 배치

[레이아웃 업데이트](layout-updates.md) 페이지 레이아웃을 사용자 정의할 수 있도록 합니다. 레이아웃 업데이트는 보다 많은 유연성을 제공합니다. [위젯](widgets.md)를 사용하려면 서버에 대한 액세스와 XML에 대한 기본 지식이 필요합니다.

다음 단계에서는 레이아웃 업데이트를 사용하여 페이지에 블록을 배치하는 방법을 보여 줍니다. 구문에 대한 특정 예제와 도움말은 를 참조하십시오. [일반적인 레이아웃 사용자 지정 작업](https://developer.adobe.com/commerce/frontend-core/guide/layouts/) 다음에서 _프론트엔드 개발자 안내서_.

### 1단계: 블록 만들기

1. 만들기 [차단](block-add.md) 원하는 대로 사용하십시오.

1. 다음 사항에 유의하십시오. `block_id`레이아웃 업데이트 지침에 사용되기 때문입니다.

### 2단계: XML로 레이아웃 업데이트 작성

1. XML로 레이아웃 지침을 구성하여 [CMS 블록 참조](https://developer.adobe.com/commerce/frontend-core/guide/layouts/xml-manage/).

1. 저장 [레이아웃 지침](https://developer.adobe.com/commerce/frontend-core/guide/layouts/xml-instructions/) 테마에 맞게 XML 파일이 저장되는 레이아웃 폴더의 서버에서.

   For example:

   `<theme_dir>/<Namespace>_<Module>/layout`

   레이아웃 핸들은 로 시작하는 파일 이름입니다. `cms_page_view_selectable_`, CMS 페이지의 URL 키, 레이아웃 업데이트 옵션 및 `xml` 파일 접미사. 다음 예제에서는 `customer-service` 는 페이지의 URL 키이고, `ChatTool` 은 레이아웃 업데이트를 페이지에 적용하기 위해 선택하는 옵션입니다.

   `cms_page_view_selectable_`&lt;`customer-service`>`_`&lt;`ChatTool`>`.xml`

   | 요소 | 설명 |
   |--- |--- |
   | CMS 페이지 식별자 | 슬래시()가 있는 페이지의 URL 키`/`)가 밑줄( )로 대체되었습니다.`_`). |
   | 레이아웃 업데이트 이름 | 다음에 대해 표시되는 옵션 _사용자 정의 레이아웃 업데이트_. |

   {style="table-layout:auto"}

### 3단계: 페이지에서 레이아웃 업데이트 참조

1. 다음에서 _관리자_ 사이드바, 이동 **[!UICONTROL Content]** > _[!UICONTROL Elements]_>**[!UICONTROL Pages]**.

1. 블록을 배치할 페이지를 찾아 편집 모드로 엽니다.

1. 아래로 스크롤하고 확장합니다. ![확장 선택기](../assets/icon-display-expand.png) 다음 **[!UICONTROL Design]** 섹션.

1. 페이지와 연결된 사용 가능한 모든 레이아웃 업데이트를 표시하려면 **[!UICONTROL Custom Layout Update]** 메뉴 아래의 제품에서 사용할 수 있습니다.

   ![사용자 정의 레이아웃 업데이트 목록](./assets/page-design-custom-layout-update.png){width="400" zoomable="yes"}

1. 페이지에 적용할 레이아웃 업데이트를 선택합니다.

### 4단계: 캐시 저장 및 새로 고침

1. 완료되면 다음을 클릭하십시오. **[!UICONTROL Save & Close]**.

1. 작업 영역 상단에 있는 메시지에서 **[!UICONTROL Cache Management]** 및 모든 잘못된 캐시 항목을 새로 고칩니다.
