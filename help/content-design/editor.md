---
title: WYSIWYG 편집기
description: 편집기를 사용하고 _What You See Is What You Get_ (WYSIWYG) 보기에서 콘텐츠를 사용하는 방법에 대해 알아봅니다.
exl-id: 209ca9d6-973c-4ad9-b7cd-4fba58dbfbb8
source-git-commit: b659c7e1e8f2ae9883f1e24d8045d6dd1e90cfc0
workflow-type: tm+mt
source-wordcount: '284'
ht-degree: 0%

---

# WYSIWYG 편집기

편집기에서 작업하는 동안 을(를) 입력하고 형식을 지정할 수 있습니다. _보이는 것이 얻는 것입니다_ (WYSIWYG) 콘텐츠 보기. 기본 HTML 코드로 직접 작업하려는 경우 모드를 쉽게 변경할 수 있습니다. 편집기를 사용하여 콘텐츠 만들기 [페이지](pages.md), [블록](blocks.md), 및 [제품 설명](../catalog/product-content.md). 제품 세부 사항을 작업할 때 를 클릭하여 편집기에 액세스합니다. **[!UICONTROL Show / Hide Editor]**.

>[!NOTE]
>
>TinyMCE 5는 기본 WYSIWYG 편집기입니다. Adobe Commerce 및 Magento Open Source 2.4.5의 TinyMCE 5.10 라이브러리에 대한 업데이트는 일부 유형의 URL을 사용하여 이미지 또는 링크를 업데이트할 때 임의의 JavaScript 실행을 허용하는 취약성을 해결합니다. TinyMCE 3은 2.4.0 릴리스에서 더 이상 사용되지 않으며 2.4.3 릴리스에서 제거되었습니다. TinyMCE 4는 2.4.4 릴리스에서 제거되었습니다.

![편집기 도구 모음](./assets/editor-toolbar.png){width="700" zoomable="yes"}

다음 항목에서는 편집기 사용에 대한 자세한 정보를 제공합니다.

- [링크 삽입](editor-insert-link.md)
- [이미지 삽입](editor-insert-image.md)
- [위젯 삽입](editor-widget.md)
- [변수 삽입](editor-insert-variable.md)

## 편집기 구성

WYSIWYG 편집기는 기본적으로 활성화되어 있으며 CMS 페이지 및 블록, 제품 및 범주의 콘텐츠를 편집하는 데 사용할 수 있습니다. 구성에서 편집기를 활성화하거나 비활성화하고 대신 정적 을 사용하도록 선택할 수 있습니다. [동적](../catalog/catalog-urls.md#dynamic-url), 제품 및 카테고리 설명의 미디어 콘텐츠 URL

![WYSIWYG 옵션](./assets/content-management-wysiwyg-options.png){width="600" zoomable="yes"}

모든 WYSIWYG 옵션에 대한 자세한 설명은 을 참조하십시오. [콘텐츠 관리](../configuration-reference/general/content-management.md) 다음에서 _구성 참조_.

1. 다음에서 _관리자_ 사이드바, 이동 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. 아래의 왼쪽 패널에서 _[!UICONTROL General]_, 선택&#x200B;**[!UICONTROL Content Management]**.

1. 확장 ![확장 선택기](../assets/icon-display-expand.png) **[!UICONTROL WYSIWYG Options]**.

1. 설정 **[!UICONTROL Enable WYSIWYG Editor]** 원하는 대로 사용하십시오.

   편집기는 기본적으로 활성화되어 있습니다.

1. 설정 **[!UICONTROL Static URLs for Media Content in WYSIWYG]** 모든 항목에 대한 기본 설정에 [미디어 콘텐츠](../catalog/catalog-urls.md#static-url) WYSIWYG 편집기로 입력됩니다.

1. 완료되면 다음을 클릭하십시오. **[!UICONTROL Save Config]**.
