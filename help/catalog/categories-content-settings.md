---
title: 범주 - 콘텐츠 설정
description: '[!UICONTROL Content] 설정을 사용하여 범주 페이지에 표시되는 추가 콘텐츠를 정의하는 방법에 대해 알아봅니다.'
exl-id: 988083e1-0993-4e08-b5e6-8b0855e56467
feature: Catalog Management, Categories, Page Content
source-git-commit: 01148770946a236ece2122be5a88b963a0f07d1f
workflow-type: tm+mt
source-wordcount: '449'
ht-degree: 0%

---

# 범주 - 콘텐츠 설정

_[!UICONTROL Content]_&#x200B;설정에 따라 범주 페이지에 표시되는 추가 콘텐츠가 결정됩니다. 카테고리 제품 목록 외에도 페이지에 이미지, 설명 및 CMS 블록이 포함될 수 있습니다. [[!DNL Page Builder]](../page-builder/introduction.md) 콘텐츠 도구를 사용하여 범주 설명을 정의할 수 있습니다.

## [!DNL Page Builder]에 범주 설명 추가

1. 편집 모드에서 범주를 엽니다.

1. 아래로 스크롤하여 **[!UICONTROL Content]** 섹션에서 ![확장 선택기](../assets/icon-display-expand.png)를 확장합니다.

   ![범주 콘텐츠](./assets/category-content.png){width="600" zoomable="yes"}

1. **[!UICONTROL Description]** 영역의 오른쪽 상단에서 **[!UICONTROL Edit with Page Builder]**&#x200B;을(를) 클릭합니다.

1. [[!DNL Page Builder]](../page-builder/introduction.md) 콘텐츠 도구를 사용하여 [기존 텍스트를 편집하고](../page-builder/text.md)다른 콘텐츠를 추가하십시오(필요한 경우).

## [!DNL Page Builder] 미리 보기

[!DNL Page Builder] (으)로 만든 콘텐츠가 있는 기존 범주에 대해 _콘텐츠_ 섹션을 확장하면 범주 페이지에 나타나는 대로 **[!UICONTROL Description]** 콘텐츠의 미리 보기를 표시합니다. 콘텐츠 영역을 클릭하면 필요한 업데이트를 수행할 수 있는 [!DNL Page Builder] 작업 영역이 열립니다.

![설명 미리 보기](../page-builder/assets/pb-product-category-content-preview.png){width="500" zoomable="yes"}

이 콘텐츠 미리보기는 기본적으로 제품 및 카테고리 양식에 대해 활성화됩니다. 미리 보기 로드로 인해 성능이 저하되면 [콘텐츠 관리 구성](../configuration-reference/general/content-management.md#advanced-content-tools) 설정에서 미리 보기를 비활성화할 수 있습니다.

## 편집기에서 카테고리 설명 추가

텍스트 상자에 일반 ASCII 문자만 입력합니다. 워드 프로세서에서 텍스트를 붙여넣는 경우, 먼저 일반 .TXT 파일로 저장하여 보이지 않는 제어 문자를 제거합니다.

자세한 내용은 [WYSIWYG 편집기](../content-design/editor.md)를 참조하십시오.

1. 편집 모드에서 범주를 엽니다.

1. 아래로 스크롤하여 **[!UICONTROL Content]** 섹션에서 ![확장 선택기](../assets/icon-display-expand.png)를 확장합니다.

   ![범주 콘텐츠](./assets/category-content-ce.png){width="500" zoomable="yes"}

1. **[!UICONTROL Description]** 범주를 입력하고 [편집기 도구 모음](../content-design/editor.md)을(를) 사용하여 필요에 따라 형식을 지정하십시오.

   오른쪽 아래 모서리를 드래그하여 텍스트 상자의 높이를 변경할 수 있습니다.

## 범주 페이지에 CMS 블록 추가

1. _관리자_ 사이드바에서 **[!UICONTROL Catalog]** > **[!UICONTROL Categories]**(으)로 이동합니다.

1. 범주 트리에서 편집할 범주를 선택합니다.

1. **[!UICONTROL Content]** 섹션에서 ![확장 선택기](../assets/icon-display-expand.png)를 확장합니다.

1. **[!UICONTROL Add the CMS block]**&#x200B;에 대해 추가할 블록을 선택하십시오.

1. **[!UICONTROL Display Settings]** 섹션에서 ![확장 선택기](../assets/icon-display-expand.png)를 확장합니다.

1. **[!UICONTROL Display Mode]**&#x200B;을(를) 다음 중 하나로 설정합니다.

   - `Static block only`
   - `Static block and products`

1. 완료되면 **[!UICONTROL Save]**&#x200B;을(를) 클릭하고 상점 앞에서의 블록 표시를 검토하십시오(캐시 새로 고침 필요).

## 콘텐츠 설정 참조

| 설정 | [범위](../getting-started/websites-stores-views.md#scope-settings) | 설명 |
|--- |--- |--- |
| [!UICONTROL Category Image] | 스토어 뷰 | 카테고리 페이지의 맨 위에 대한 이미지를 지정합니다. 메서드: <br/><br/>**[!UICONTROL Upload]**- 로컬 컴퓨터의 이미지 파일을 갤러리에 업로드하고 범주 이미지로 사용합니다.<br/><br/>**[!UICONTROL Select from Gallery]** - 갤러리에서 기존 이미지를 선택하라는 메시지가 표시됩니다. <br/><br/>![Page Builder 카메라 아이콘](../assets/icon-camera.png) - 이미지 파일을 카메라 타일로 드래그하거나 이미지를 찾아 로컬 파일 시스템에서 선택합니다. |
| [!UICONTROL Description] | 스토어 뷰 | 범주 페이지에 나타나는 설명을 지정합니다. <br/><br/>**[!UICONTROL Edit with Page Builder]**- 설명을 편집할 수 있는 [[!DNL Page Builder] 작업 영역](../page-builder/workspace.md)을 엽니다.<br/><br/>**[!UICONTROL Show / Hide Editor]** - WYSIWYG 편집기와 HTML 모드 간 표시를 전환합니다. |
| [!UICONTROL Add CMS Block] | 스토어 뷰 | 기존 [CMS 블록](../content-design/blocks.md)을(를) 범주 페이지에 추가합니다. |

{style="table-layout:auto"}
