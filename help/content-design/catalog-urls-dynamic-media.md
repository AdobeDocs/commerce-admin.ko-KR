---
title: Dynamic Media URL
description: 이미지 또는 기타 미디어 에셋에 대한 상대 참조로 Dynamic Media URL을 사용하는 방법에 대해 알아봅니다.
exl-id: 41aabde2-f6cc-4b83-8d56-9753a7aa93e9
feature: CMS, Media
badgePaas: label="PaaS만" type="Informative" url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="Adobe Commerce 온 클라우드 프로젝트(Adobe 관리 PaaS 인프라) 및 온프레미스 프로젝트에만 적용됩니다."
source-git-commit: 4a3aa2aa32b692341edabd41fdb608e3cff5d8e0
workflow-type: tm+mt
source-wordcount: '289'
ht-degree: 0%

---

# Dynamic Media URL

Dynamic media URL은 이미지 또는 기타 미디어 에셋에 대한 상대 참조입니다. 사용하도록 설정하면 Dynamic Media URL을 사용하여 서버의 에셋 또는 [콘텐츠 배달 네트워크](media-storage-content-delivery-network.md)에 저장된 파일에 직접 연결할 수 있습니다. Dynamic Media URL을 사용하면 카탈로그 성능에 영향을 줄 수 있으며, 정적 또는 동적 미디어 URL을 사용하도록 [편집기](editor.md#configure-the-editor)를 구성할 수 있습니다.

모든 [markup 태그](../systems/markup-tags.md)와 마찬가지로 지시문은 중괄호로 묶입니다. Dynamic Media URL의 형식은 다음과 같습니다.

`\{\{media url="path/to/image.jpg"}}`

페이지가 상점 첫 화면에서 렌더링될 때 저장된 HTML 콘텐츠에서 동적 URL 지시문이 처리됩니다. 페이지가 렌더링될 때마다 `\{\{media url="..."}}`에 대한 콘텐츠가 스캔되고 각 지시문이 해당 미디어 URL로 대체됩니다.

{{$include /help/_includes/directives-caution.md}}

## 정적 미디어 URL 구성

기본적으로 WYSIWYG 편집기에서 카탈로그에 삽입된 이미지에는 상대적 동적 URL이 있습니다. 정적 URL을 사용하려는 경우 구성 설정을 변경할 수 있습니다.

1. _관리자_ 사이드바에서 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**(으)로 이동합니다.

1. _[!UICONTROL General]_&#x200B;아래의 왼쪽 패널에서&#x200B;**[!UICONTROL Content Management]**&#x200B;을(를) 선택합니다.

1. ![ 섹션에서 ](../assets/icon-display-expand.png)확장 선택기&#x200B;**[!UICONTROL WYSIWYG Options]**&#x200B;를 확장합니다.

   ![WYSIWYG 옵션](./assets/content-management-wysiwyg-options.png){width="600" zoomable="yes"}

1. **[!UICONTROL Use Static URLs for Media Content in WYSIWYG]**&#x200B;을(를) 다음 중 하나로 설정합니다.

   - `Yes` - WYSIWYG 편집기와 함께 삽입된 미디어 콘텐츠에 정적 URL을 사용합니다. 정적 URL은 절대 URL이며 저장소의 [기본 URL](../stores-purchase/store-urls.md)이(가) 변경되면 중단됩니다.

   - `No` - (기본값) `\{\{media url="..."}}` 지시문을 기반으로 WYSIWYG 편집기와 함께 삽입된 미디어 콘텐츠에 동적 URL을 사용합니다. 동적 URL은 상대적이며 저장소의 기본 URL이 변경되는 경우 중단되지 않습니다.

1. 완료되면 **[!UICONTROL Save Config]**&#x200B;을(를) 클릭합니다.

<!-- Last updated from includes: 2022-08-30 15:36:09 -->
