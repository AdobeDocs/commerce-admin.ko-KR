---
title: 미디어 갤러리 이미지 최적화
description: 에 대한 이미지 최적화를 사용하는 방법을 알아봅니다. [!DNL Commerce] 미디어 자산입니다.
exl-id: ba75e90a-406b-4b14-b049-0b78c4a27188
feature: Page Content, Media
source-git-commit: b659c7e1e8f2ae9883f1e24d8045d6dd1e90cfc0
workflow-type: tm+mt
source-wordcount: '180'
ht-degree: 0%

---

# 미디어 갤러리 이미지 최적화

새로운 [미디어 갤러리](media-gallery.md) 는 을(를) 제공합니다 _이미지 최적화_ 이 기능은 성능을 향상시키고 상점 전면의 미디어 파일 크기를 줄입니다. 이 최적화는 기본적으로 활성화되어 있으며 저장소 구성 설정에서 수정할 수 있습니다.

## 이미지 최적화 구성

1. 다음에서 _관리자_ 사이드바, 이동 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. 왼쪽 패널에서 를 확장합니다. **[!UICONTROL Advanced]** 및 선택 **[!UICONTROL System]**.

1. 확장 ![확장 선택기](../assets/icon-display-expand.png) **[!UICONTROL Media Gallery Image Optimization]** 다음을 수행합니다.

   - 설정 **[!UICONTROL Enable Image Optimization]** 끝 `Yes`.
   - 다음을 입력합니다. **[!UICONTROL Maximum Width]** 및 **[!UICONTROL Maximum Height]** 필요에 따른 값(픽셀 단위).

## 비헤이비어

Media Gallery 이미지 최적화 기능이 활성화되면 최적화된 이미지 복사본이 의 콘텐츠에 자동으로 삽입됩니다. [미디어 갤러리](media-gallery.md) 원본 파일 대신 사용합니다.

다음의 경우 _최대 폭_ 및 _최대 높이_ 구성에서 값이 변경되면 이전에 삽입한 기존의 최적화된 모든 이미지가 업데이트됩니다.

미디어 갤러리 이미지 최적화를 사용하려면 `media.gallery.renditions.update` 구성을 변경할 때 대기열 소비자는 최적화된 이미지를 재생성하기 위해 실행 중입니다. 다음을 참조하십시오 [메시지 대기열 관리](https://experienceleague.adobe.com/docs/commerce-operations/configuration-guide/message-queues/manage-message-queues.html) 다음에서 _구성 안내서_ 을 참조하십시오.
