---
title: 미디어 갤러리 이미지 최적화
description: ' [!DNL Commerce] 미디어 자산에 대해 이미지 최적화를 사용하는 방법을 알아봅니다.'
exl-id: ba75e90a-406b-4b14-b049-0b78c4a27188
feature: Page Content, Media
source-git-commit: a93e96353f4be0e771064cdcfbdf794772386a28
workflow-type: tm+mt
source-wordcount: '174'
ht-degree: 0%

---

# 미디어 갤러리 이미지 최적화

새 [미디어 갤러리](media-gallery.md)에서는 성능을 개선하고 상점의 미디어 파일 크기를 줄이는 _이미지 최적화_ 기능을 제공합니다. 이 최적화는 기본적으로 활성화되어 있으며 저장소 구성 설정에서 수정할 수 있습니다.

## 이미지 최적화 구성

1. _관리자_ 사이드바에서 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**(으)로 이동합니다.

1. 왼쪽 패널에서 **[!UICONTROL Advanced]**&#x200B;을(를) 확장하고 **[!UICONTROL System]**&#x200B;을(를) 선택합니다.

1. ![확장 선택기](../assets/icon-display-expand.png) **[!UICONTROL Media Gallery Image Optimization]**&#x200B;을(를) 확장하고 다음을 수행합니다.

   - **[!UICONTROL Enable Image Optimization]**&#x200B;을(를) `Yes`(으)로 설정합니다.
   - 필요에 따라 **[!UICONTROL Maximum Width]** 및 **[!UICONTROL Maximum Height]** 값을 픽셀 단위로 입력하십시오.

## 비헤이비어

미디어 갤러리 이미지 최적화 기능을 사용하면 원본 파일 대신 [미디어 갤러리](media-gallery.md)의 콘텐츠에 최적화된 이미지 복사본이 자동으로 삽입됩니다.

구성에서 _최대 너비_ 및 _최대 높이_ 값이 변경되면 이전에 삽입한 기존의 최적화된 모든 이미지가 업데이트됩니다.

Media Gallery 이미지 최적화를 사용하려면 구성을 변경할 때 최적화된 이미지를 다시 생성하기 위해 `media.gallery.renditions.update` 큐 소비자가 실행 중이어야 합니다. 자세한 내용은 _구성 가이드_&#x200B;의 [메시지 큐 관리](https://experienceleague.adobe.com/docs/commerce-operations/configuration-guide/message-queues/manage-message-queues.html?lang=ko)를 참조하십시오.

{{$include /help/_includes/image-optimization-animated-gif-note.md}}
