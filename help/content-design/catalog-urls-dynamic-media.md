---
title: Dynamic Media URL
description: 이미지 또는 기타 미디어 에셋에 대한 상대 참조로 Dynamic Media URL을 사용하는 방법에 대해 알아봅니다.
exl-id: 41aabde2-f6cc-4b83-8d56-9753a7aa93e9
feature: CMS, Media
source-git-commit: d3b9b4cd0d12f8d5feb2bad0bf601970f9ee1a36
workflow-type: tm+mt
source-wordcount: '272'
ht-degree: 0%

---

# Dynamic Media URL

Dynamic media URL은 이미지 또는 기타 미디어 에셋에 대한 상대 참조입니다. 활성화된 경우 Dynamic Media URL을 사용하여 서버의 에셋 또는 [컨텐츠 전달 네트워크](media-storage-content-delivery-network.md). Dynamic Media URL의 사용은 카탈로그 성능 및 [편집자](editor.md#configure-the-editor) 정적 또는 dynamic media URL을 사용하도록 구성할 수 있습니다.

모두와 마찬가지로 [태그 표시](../systems/markup-tags.md)를 지정하면 지시문이 중괄호로 묶입니다. Dynamic Media URL의 형식은 다음과 같습니다.

`\{\{media url="path/to/image.jpg"}}`

페이지가 상점 첫 화면에서 렌더링될 때 저장된 HTML 콘텐츠에서 동적 URL 지시문이 처리됩니다. 페이지가 렌더링될 때마다 컨텐츠가 스캔됩니다. `\{\{media url="..."}}` 그리고 각 지시문은 해당 미디어 URL로 대체됩니다.

{{$include /help/_includes/directives-caution.md}}

## 정적 미디어 URL 구성

기본적으로 WYSIWYG 편집기에서 카탈로그에 삽입된 이미지에는 상대적인 동적 URL이 있습니다. 정적 URL을 사용하려는 경우 구성 설정을 변경할 수 있습니다.

1. 다음에서 _관리자_ 사이드바, 이동 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. 아래의 왼쪽 패널에서 _[!UICONTROL General]_, 선택&#x200B;**[!UICONTROL Content Management]**.

1. 확장 ![확장 선택기](../assets/icon-display-expand.png) 다음 **[!UICONTROL WYSIWYG Options]** 섹션.

   ![WYSIWYG 옵션](./assets/content-management-wysiwyg-options.png){width="600" zoomable="yes"}

1. 설정 **[!UICONTROL Use Static URLs for Media Content in WYSIWYG]** 다음 중 하나를 수행합니다.

   - `Yes` - WYSIWYG 편집기와 함께 삽입된 미디어 콘텐츠에 정적 URL을 사용합니다. 정적 URL은 절대 URL이며 [기본 URL](../stores-purchase/store-urls.md) / 스토어가 변경됩니다.

   - `No` - (기본값) WYSIWYG 편집기와 함께 삽입된 미디어 콘텐츠에 대해 다음을 기반으로 동적 URL을 사용합니다. `\{\{media url="..."}}` 지시문입니다. 동적 URL은 상대적이며 저장소의 기본 URL이 변경되는 경우 중단되지 않습니다.

1. 완료되면 다음을 클릭하십시오. **[!UICONTROL Save Config]**.
