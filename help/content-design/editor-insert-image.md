---
title: 편집기에 이미지 삽입
description: WYSIWYG 편집기를 사용하면 미디어 저장소에서 이미지를 삽입하거나, 다른 서버에 있는 이미지에 연결하거나, Adobe Stock 에셋을 사용할 수 있습니다.
exl-id: 591830c9-6dba-4738-a6e7-cf5f93b3c319
badgePaas: label="PaaS만" type="Informative" url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="Adobe Commerce 온 클라우드 프로젝트(Adobe 관리 PaaS 인프라) 및 온프레미스 프로젝트에만 적용됩니다."
source-git-commit: 57a913b21f4cbbb4f0800afe13012ff46d578f8e
workflow-type: tm+mt
source-wordcount: '363'
ht-degree: 0%

---

# 편집기에 이미지 삽입

편집기에서 다음 세 가지 소스 유형을 사용하여 이미지를 삽입할 수 있습니다.

- [미디어 저장소](media-storage.md)에 업로드된 이미지 추가
- 다른 서버에 있는 이미지에 대한 링크
- Adobe Stock 통합을 사용하여 Adobe Stock 에셋을 검색하고 사용합니다

![미디어 저장소](./assets/media-storage.png){width="650" zoomable="yes"}

1. 편집 모드로 페이지, 블록 또는 동적 블록을 엽니다.

1. _[!UICONTROL Content]_섹션으로 이동하여 편집기를 지원하는 요소를 클릭합니다.

1. 이미지를 표시할 위치에 커서를 놓습니다.

1. 편집기 도구 모음에서 _이미지 삽입_ 아이콘을 클릭합니다.

   ![이미지 삽입 아이콘](./assets/editor-toolbar-image-button.png){width="700" zoomable="yes"}

   이 작업은 _[!UICONTROL Insert/edit image]_대화 상자를 엽니다.

1. **Source**&#x200B;의 경우 _검색_ 아이콘을 클릭하고 사용할 이미지 에셋의 위치와 일치하는 메서드를 사용하십시오.

   ![검색 아이콘 선택](./assets/editor-dialog-insert-image.png){width="250" zoomable="yes"}

   - **새 이미지 업로드**: 이 메서드를 사용하여 새 이미지 파일을 업로드합니다.

      - 트리에서 새 이미지 파일을 추가할 폴더를 선택합니다.

      - **[!UICONTROL Choose Files]**&#x200B;을(를) 클릭합니다.

      - 이미지 파일을 찾아 선택합니다.

      - 새 파일의 축소판을 클릭하고 **[!UICONTROL Add Selected]**&#x200B;을(를) 클릭합니다.

   - **기존 에셋 선택**: 이 메서드를 사용하여 미디어 저장소/갤러리에서 기존 이미지 에셋을 선택합니다.

      - 트리를 사용하여 이미지로 이동합니다.

      - 썸네일을 클릭하고 **[!UICONTROL Add Selected]**&#x200B;을(를) 클릭합니다.

   - **Adobe Stock 이미지 검색 및 선택**: 이 메서드를 사용하여 Adobe Stock에서 이미지를 찾습니다.

     >[!NOTE]
     >
     >이 메서드를 사용하려면 관리자에 대해 [Adobe Stock 통합](adobe-stock.md)이(가) 구성되어 있어야 합니다.

      - **[!UICONTROL Search Adobe Stock]**&#x200B;을(를) 클릭하고 이미지를 검색합니다.

      - 미리 보기 또는 라이선스가 부여된 이미지를 갤러리에 저장합니다.

        [Adobe Stock](https://stock.adobe.com) 자산 작업에 대한 자세한 내용은 [Adobe Stock 이미지 사용](adobe-stock-manage.md)을 참조하세요.

      - 갤러리에서 자산 축소판을 선택하고 **[!UICONTROL Add Selected]**&#x200B;을(를) 클릭합니다.

1. **[!UICONTROL Image Description]**&#x200B;의 경우 이미지에 대한 간단한 설명을 입력하십시오.

1. 페이지에서 이미지를 렌더링하려면 너비 및 높이 **[!UICONTROL Dimensions]**&#x200B;을(를) 픽셀 단위로 입력하십시오.

   이미지의 종횡비를 자동으로 유지하려면 선택한 **[!UICONTROL Constrain proportions]** 확인란을 유지하십시오.

1. 프로세스를 완료하려면 **[!UICONTROL Insert]**&#x200B;을(를) 클릭하십시오.
