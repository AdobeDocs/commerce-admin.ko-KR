---
title: '[!UICONTROL General] &gt; [!UICONTROL Content Management]'
description: 에서 구성 설정을 검토합니다. [!UICONTROL General] &gt; [!UICONTROL Content Management] 상거래 관리자의 페이지입니다.
exl-id: 67c5e89b-0a7c-4e4f-a5ad-10376c3ef6f9
feature: Configuration, Page Content
source-git-commit: 76bd1b1af9b55d69bd98209d70fb5518f190a3e1
workflow-type: tm+mt
source-wordcount: '471'
ht-degree: 0%

---

# [!UICONTROL General] > [!UICONTROL Content Management]

{{config}}

## [!UICONTROL WYSIWYG Options]

![WYSIWYG 옵션](./assets/content-management-wysiwyg-options.png)<!-- zoom -->

<!-- [WYSIWYG Options](https://docs.magento.com/user-guide/cms/editor.html) -->

| 필드 | [범위](../../getting-started/websites-stores-views.md#scope-settings) | 설명 |
|--- |--- |--- |
| [!UICONTROL Enable WYSIWYG Editor] | 스토어 뷰 | 저장소에 대해 편집기를 사용할 수 있는지 여부를 결정합니다. 옵션: 기본적으로 활성화됨/기본적으로 비활성화됨/완전히 비활성화됨 |
| [!UICONTROL WYSIWYG Editor] | 웹 사이트 | WYSIWYG 편집기에 사용되는 TinyMCE 편집기의 버전을 결정합니다. 옵션: <br/>**`TinyMCE 5`**- (기본값) TinyMCE 버전 5를 기본 WYSIWYG 편집기로 사용합니다.<br><br>_**&#x200B;참고:**_Adobe Commerce 및 Magento Open Source 2.4.5의 TinyMCE 5.10 라이브러리에 대한 업데이트는 일부 유형의 URL을 사용하여 이미지 또는 링크를 업데이트할 때 임의의 JavaScript 실행을 허용하는 취약성을 해결합니다. TinyMCE 3은 2.4.0 릴리스에서 더 이상 사용되지 않으며 2.4.3 릴리스에서 제거되었습니다. TinyMCE 4는 2.4.4 릴리스에서 제거되었습니다. |
| [!UICONTROL Use Static URLs for Media Content in WYSIWYG] | 글로벌 | 다음 여부를 결정합니다. [정적 URL](../../content-design/catalog-urls-dynamic-media.md) WYSIWYG 편집기에서 참조하는 미디어 콘텐츠에 사용됩니다. 이 설정은 제품, 카테고리, 페이지 및 블록을 포함하여 WYSIWYG 편집기를 사용할 수 있는 모든 위치에 적용됩니다. 옵션: <br/>**`Yes`**- WYSIWYG 편집기와 함께 삽입된 미디어 콘텐츠에 정적 URL을 사용합니다. 정적 URL은 절대 URL이며 [기본 URL](../../stores-purchase/store-urls.md) / 스토어가 변경됩니다.<br/>**`No`** (기본값) - 를 기반으로 WYSIWYG 편집기와 함께 삽입되는 미디어 콘텐츠에 동적 URL을 사용합니다.  `{{media url="..."}}` 지시문입니다. 동적 URL은 상대적이며 저장소의 기본 URL이 변경되는 경우 중단되지 않습니다. |

{:style=&quot;table-layout:auto&quot;}

## [!UICONTROL CMS Page Hierarchy]

{{ee-feature}}

![CMS 페이지 계층](./assets/content-management-cms-page-hierarchy.png)<!-- zoom -->

<!--[CMS Page Hierarchy](https://docs.magento.com/user-guide/cms/page-hierarchy.html) -->

| 필드 | [범위](../../getting-started/websites-stores-views.md#scope-settings) | 설명 |
|--- |--- |--- |
| [!UICONTROL Enable Hierarchy Functionality] | 글로벌 | 콘텐츠 페이지에 대한 페이지 계층 구조 사용을 활성화합니다. 옵션: `Yes` / `No` |
| [!UICONTROL Enable Hierarchy Metadata] | 글로벌 | 계층의 페이지와 메타데이터를 연결하는 기능을 제공합니다. 옵션: `Yes` / `No` |
| [!UICONTROL Default Layout for Hierarchy Menu] | 글로벌 | 기본 메뉴 스타일을 결정합니다. 옵션: `Content` / `Left Column` / `Right Column` |

{:style=&quot;table-layout:auto&quot;}

## [!UICONTROL Advanced Content Tools]

![고급 콘텐츠 도구](./assets/content-management-advanced-content-tools.png)<!-- zoom -->

<!-- [Advanced Content Tools](https://docs.magento.com/user-guide/cms/page-builder-workspace.html) -->

| 필드 | [범위](../../getting-started/websites-stores-views.md#scope-settings) | 설명 |
|--- |--- |--- |
| [!UICONTROL Enable Page Builder] | 글로벌 | 다음 여부를 결정합니다. [!DNL Page Builder] 고급 콘텐츠 도구를 사용할 수 있습니다. 옵션: <br/>**`Yes`**- [!DNL Page Builder] 작업 영역은 페이지, 블록, 제품 및 범주의 콘텐츠 섹션에 표시됩니다.<br/>**`No`** - 표준 CMS 편집 도구가 _[!UICONTROL Content]_페이지, 블록, 제품 및 범주의 섹션입니다. |
| [!UICONTROL Enable Page Builder Content Preview] | 글로벌 | 다음 여부를 결정합니다. [!DNL Page Builder] 제품 및 범주에 대해 컨텐츠 미리 보기를 사용할 수 있습니다. 옵션: `Yes` / `No` <br/>**_참고:_**다음으로 설정됨: `Yes` 기본적으로 미리보기를 해제하면 제품 또는 카테고리 양식 내에서 미리보기를 로드하여 발생하는 성능 문제를 방지할 수 있습니다. |
| [!UICONTROL Google Maps API Key] | 글로벌 | 다음 [!DNL Google Maps] Google 계정의 API 키. |
| [!UICONTROL Test Key] |  | 을(를) 확인합니다. [!DNL Google Maps] API 키. |
| [!UICONTROL Google Maps Style] | 글로벌 | 붙여넣기 [!DNL Google Maps] 여기에 JSON 코드 스타일을 지정하여 맵 콘텐츠 유형의 모양과 느낌을 변경합니다. |
| [!UICONTROL Default Column Grid Size] | 글로벌 | 의 기본 열 수를 결정합니다. [!DNL Page Builder] 그리드. |
| [!UICONTROL Maximum Column Grid Size] | 글로벌 | 의 최대 열 수를 결정합니다. [!DNL Page Builder] 그리드. |

{:style=&quot;table-layout:auto&quot;}

>[!TIP]
>
>Page Builder를 사용하면 시각적 스토리텔링을 강화하고 고객 참여 및 충성도를 높이는 맞춤형 레이아웃을 통해 콘텐츠가 풍부한 페이지를 손쉽게 만들 수 있습니다. 이러한 기능은 품질을 향상시키고 사용자 정의 페이지를 제작하는 시간과 비용을 절감하기 위해 설계되었습니다. 이러한 기능과 이러한 기능을 사용하여 Adobe Commerce 또는 Magento Open Source 스토어의 매력적인 콘텐츠를 만드는 방법에 대한 자세한 내용은 [_페이지 빌더 사용 안내서_](../../page-builder/guide-overview.md).

{:style=&quot;table-layout:auto&quot;}
