---
title: '[!UICONTROL General] &gt; [!UICONTROL Content Management]'
description: Commerce 관리자의 [!UICONTROL General] &gt; [!UICONTROL Content Management] 페이지에서 구성 설정을 검토하십시오.
exl-id: 67c5e89b-0a7c-4e4f-a5ad-10376c3ef6f9
feature: Configuration, Page Content
source-git-commit: 5eef49c10680a47574afe3d3ecfa430dca7ad9ff
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
| [!UICONTROL WYSIWYG Editor] | 웹 사이트 | WYSIWYG 편집기에 사용되는 TinyMCE 편집기의 버전을 결정합니다. 옵션: <br/>**`TinyMCE 5`**- (기본값) TinyMCE 버전 5를 기본 WYSIWYG 편집기로 사용합니다.<br><br>_**&#x200B;참고:**_Adobe Commerce 및 Magento Open Source 2.4.5의 TinyMCE 5.10 라이브러리를 업데이트하면 일부 유형의 URL을 사용하여 이미지나 링크를 업데이트할 때 임의의 JavaScript 실행이 허용된 취약성이 해결됩니다. TinyMCE 3은 2.4.0 릴리스에서 더 이상 사용되지 않으며 2.4.3 릴리스에서 제거되었습니다. TinyMCE 4는 2.4.4 릴리스에서 제거되었습니다. |
| [!UICONTROL Use Static URLs for Media Content in WYSIWYG] | 글로벌 | WYSIWYG 편집기에서 참조하는 미디어 콘텐츠에 [정적 URL](../../content-design/catalog-urls-dynamic-media.md)을(를) 사용할지 여부를 결정합니다. 이 설정은 제품, 카테고리, 페이지 및 블록을 포함하여 WYSIWYG 편집기를 사용할 수 있는 모든 위치에 적용됩니다. 옵션: <br/>**`Yes`**- WYSIWYG 편집기와 함께 삽입된 미디어 콘텐츠에 정적 URL을 사용합니다. 정적 URL은 절대 URL이며 저장소의 [기본 URL](../../stores-purchase/store-urls.md)이(가) 변경되면 중단됩니다.<br/>**`No`**(기본값) - `{{media url="..."}}` 지시문을 기반으로 WYSIWYG 편집기와 함께 삽입되는 미디어 콘텐츠에 동적 URL을 사용합니다. 동적 URL은 상대적이며 저장소의 기본 URL이 변경되는 경우 중단되지 않습니다. |

{style="table-layout:auto"}

## [!UICONTROL CMS Page Hierarchy]

{{ee-feature}}

![CMS 페이지 계층 구조](./assets/content-management-cms-page-hierarchy.png)<!-- zoom -->

<!--[CMS Page Hierarchy](https://docs.magento.com/user-guide/cms/page-hierarchy.html) -->

| 필드 | [범위](../../getting-started/websites-stores-views.md#scope-settings) | 설명 |
|--- |--- |--- |
| [!UICONTROL Enable Hierarchy Functionality] | 글로벌 | 콘텐츠 페이지에 대한 페이지 계층 구조 사용을 활성화합니다. 옵션: `Yes` / `No` |
| [!UICONTROL Enable Hierarchy Metadata] | 글로벌 | 계층의 페이지와 메타데이터를 연결하는 기능을 제공합니다. 옵션: `Yes` / `No` |
| [!UICONTROL Default Layout for Hierarchy Menu] | 글로벌 | 기본 메뉴 스타일을 결정합니다. 옵션: `Content` / `Left Column` / `Right Column` |

{style="table-layout:auto"}

## [!UICONTROL Advanced Content Tools]

![고급 콘텐츠 도구](./assets/content-management-advanced-content-tools.png)<!-- zoom -->

<!-- [Advanced Content Tools](https://docs.magento.com/user-guide/cms/page-builder-workspace.html) -->

| 필드 | [범위](../../getting-started/websites-stores-views.md#scope-settings) | 설명 |
|--- |--- |--- |
| [!UICONTROL Enable Page Builder] | 글로벌 | [!DNL Page Builder] 고급 콘텐츠 도구를 사용할 수 있는지 확인합니다. 옵션: <br/>**`Yes`**- [!DNL Page Builder] 작업 영역이 페이지, 블록, 제품 및 범주의 콘텐츠 섹션에 표시됩니다.<br/>**`No`** - 표준 CMS 편집 도구는 페이지, 블록, 제품 및 범주의 _[!UICONTROL Content]_섹션에 표시됩니다. |
| [!UICONTROL Enable Page Builder Content Preview] | 글로벌 | 제품 및 범주에 대해 [!DNL Page Builder] 콘텐츠 미리 보기를 사용할지 여부를 결정합니다. 옵션: `Yes` / `No` <br/>**_참고:_**기본적으로 `Yes`(으)로 설정되어 있지만 미리 보기를 해제하면 제품 또는 범주 양식 내에서 미리 보기를 로드하여 발생하는 성능 문제를 방지할 수 있습니다. |
| [!UICONTROL Google Maps API Key] | 글로벌 | Google 계정의 [!DNL Google Maps] API 키입니다. |
| [!UICONTROL Test Key] |  | [!DNL Google Maps] API 키의 유효성을 검사합니다. |
| [!UICONTROL Google Maps Style] | 글로벌 | 맵 콘텐츠 형식의 모양과 느낌을 변경하려면 여기에 [!DNL Google Maps] 스타일 JSON 코드를 붙여넣으십시오. |
| [!UICONTROL Default Column Grid Size] | 글로벌 | [!DNL Page Builder] 표에 있는 기본 열 수를 결정합니다. |
| [!UICONTROL Maximum Column Grid Size] | 글로벌 | [!DNL Page Builder] 표의 최대 열 수를 결정합니다. |

{style="table-layout:auto"}

>[!TIP]
>
>Page Builder를 사용하면 시각적 스토리텔링을 강화하고 고객 참여 및 충성도를 높이는 맞춤형 레이아웃을 통해 콘텐츠가 풍부한 페이지를 손쉽게 만들 수 있습니다. 이러한 기능은 품질을 향상시키고 사용자 정의 페이지를 제작하는 시간과 비용을 절감하기 위해 설계되었습니다. 이러한 기능과 이러한 기능을 사용하여 Adobe Commerce 또는 Magento Open Source 스토어의 매력적인 콘텐츠를 만드는 방법에 대한 자세한 내용은 [_Page Builder 사용 안내서_](../../page-builder/guide-overview.md)&#x200B;를 참조하십시오.
