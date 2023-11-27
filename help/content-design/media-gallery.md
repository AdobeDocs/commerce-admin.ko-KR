---
title: 다음 [!DNL Media Gallery]
description: 미디어 갤러리를 사용하여 서버에서 미디어 파일을 구성하고 관리합니다.
exl-id: bf730e46-70f3-405c-88cf-62d0a3e8634f
feature: Page Content, Media
source-git-commit: b659c7e1e8f2ae9883f1e24d8045d6dd1e90cfc0
workflow-type: tm+mt
source-wordcount: '319'
ht-degree: 0%

---

# 다음 [!DNL Media Gallery]

Adobe Commerce 또는 Magento Open Source 2.4를 사용하면 판매자가 새 제품을 사용할 수 있습니다 _고급_ [!DNL Media Gallery] 서버에서 미디어 파일을 구성하고 관리합니다. 이 새로운 항목 [!DNL Media Gallery] 는 기존 미디어 스토리지와 동일한 기능을 포함하지만 향상된 사용자 인터페이스와 보다 긴밀한 통합을 제공합니다. [Adobe Stock][adobe-stock].

![미디어 갤러리 격자에 표시된 이미지](./assets/media-gallery-grid.png){width="700" zoomable="yes"}

>[!NOTE]
>
>에 추가된 제품 이미지 [_[!UICONTROL Images and Videos]_제품 섹션](../catalog/product-image.md#upload-an-image) 이(가) 관리하지 않음 [!DNL Media Gallery]. 에 사용된 이미지만_[!UICONTROL Content]_ 제품 섹션 필드가 표시되고 새 항목에서 필터링됩니다. [!DNL Media Gallery].

## 새 항목 활성화 [!DNL Media Gallery]

1. 다음에서 _관리자_ 사이드바, 이동 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. 왼쪽 패널에서 를 확장합니다. **[!UICONTROL Advanced]** 및 선택 **[!UICONTROL System]**.

1. 확장 ![확장 선택기](../assets/icon-display-expand.png) **[!UICONTROL Media Gallery]**.

   ![고급 구성 - [!DNL Media Gallery]](./assets/system-media-gallery.png){width="600" zoomable="yes"}

1. 설정 **[!UICONTROL Enable Old Media Gallery]** 끝 `No`.

1. 클릭 **[!UICONTROL Save Config]**.

1. 메시지가 표시되면 **[!UICONTROL Cache Management]** 시스템 메시지에 연결하고 잘못된 캐시를 새로 고칩니다.

   다음 [[!UICONTROL Content] 메뉴](/help/content-design/content-menu.md) 이제 새 _[!UICONTROL Media Gallery]_옵션을 선택합니다.

>[!NOTE]
>
>새로운 기능을 위한 전체 기능 [!DNL Media Gallery] 필수 `media.gallery.synchronization` 및 `media.content.synchronization` 초기 동기화를 위해 시작할 큐 소비자입니다. 다음을 참조하십시오 [메시지 대기열 관리](https://experienceleague.adobe.com/docs/commerce-operations/configuration-guide/message-queues/manage-message-queues.html) 다음에서 _구성 안내서_ 을 참조하십시오.

## 새 항목 액세스 [!DNL Media Gallery]

새로운 [!DNL Media Gallery] 는 콘텐츠 메뉴에서 액세스할 수 있거나 [페이지 추가 또는 편집](/help/content-design/page-add.md). 다음 경우에 액세스할 수도 있습니다. [범주 만들기 또는 편집](/help/catalog/category-create.md)또는 다음을 수행하는 경우 [콘텐츠 편집기를 사용하여 이미지 삽입](/help/content-design/editor-insert-image.md).

새 항목에 액세스 [!UICONTROL Media Gallery] 다음을 통해 [!UICONTROL Content] 메뉴:

- 다음에서 _관리자_ 사이드바, 이동 **[!UICONTROL Content]** > _[!UICONTROL Media]_>**[!UICONTROL Media Gallery]**.

페이지를 추가하거나 편집할 때 새 미디어 갤러리에 액세스하려면 다음 작업을 수행하십시오.

1. 다음에서 _관리자_ 사이드바, 이동 **[!UICONTROL Content]** > _[!UICONTROL Elements]_>**[!UICONTROL Pages]**.

1. 클릭 **[!UICONTROL Add a New Page]**.

   기존 페이지를 편집하려는 경우 _[!UICONTROL Action]_클릭할 열&#x200B;**[!UICONTROL Select]**및 선택&#x200B;**[!UICONTROL Edit]**.

1. 확장 ![확장 선택기](../assets/icon-display-expand.png) 다음 **[!UICONTROL Content]** 섹션을 참조하고 다음을 수행합니다.

   - 다음을 보유한 경우: [페이지 빌더 활성화됨](../page-builder/setup.md)를 확장합니다. **[!UICONTROL Media]** 패널 및 드래그 **[!UICONTROL Image]** 대상 컨테이너에 대한 자리 표시자 그런 다음 **[!UICONTROL Select from Gallery]**.

     ![이미지를 스테이지로 드래그](./assets/pb-media-image-drag.png){width="600" zoomable="yes"}

   - 다음 항목이 있는 경우 [WYSIWYG 편집기 활성화됨](/help/content-design/editor.md), 클릭 **[!UICONTROL Show/Hide Editor]** 그런 다음 을 클릭합니다. **[!UICONTROL Insert Image]**.

## [!DNL Media Gallery] 데모

에 대해 자세히 알아보려면 [!DNL Media Gallery], 이 비디오 보기:

>[!VIDEO](https://video.tv.adobe.com/v/343785?quality=12)

[adobe-stock]: https://stock.adobe.com

