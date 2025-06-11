---
title: 미디어 스토리지
description: 미디어 저장소를 통해 서버에 저장된 Commerce 미디어 파일을 구성하고 액세스하는 방법에 대해 알아봅니다.
exl-id: 5cf1bb20-d747-4a12-8558-e167c229efe8
feature: Page Content, Media
badgePaas: label="PaaS만" type="Informative" url="https://experienceleague.adobe.com/ko/docs/commerce/user-guides/product-solutions" tooltip="Adobe Commerce 온 클라우드 프로젝트(Adobe 관리 PaaS 인프라) 및 온프레미스 프로젝트에만 적용됩니다."
source-git-commit: 57a913b21f4cbbb4f0800afe13012ff46d578f8e
workflow-type: tm+mt
source-wordcount: '478'
ht-degree: 0%

---

# 미디어 스토리지

미디어 저장소를 사용하면 서버에 저장된 미디어 파일을 구성하고 액세스할 수 있습니다. 파일 위치에 대한 경로는 [기본 URL](../stores-purchase/store-urls.md) 구성에 의해 결정됩니다. 미디어 저장소의 파일은 페이지 및 정적 블록에서 작업하는 동안 편집기에서 액세스할 수 있습니다. 일반적으로 미디어 저장소는 [!DNL Commerce] 프로그램 파일과 동일한 서버의 파일 시스템에 있습니다.

또는 [데이터베이스](media-storage-database.md) 또는 별도의 서버나 [콘텐츠 배달 네트워크](media-storage-content-delivery-network.md)에서 미디어 파일을 관리할 수 있습니다. 대체 스토리지를 사용하는 장점은 미디어 동기화에 필요한 노력을 최소화한다는 것입니다. 동기화 성능은 동일한 이미지, CSS 파일 및 기타 미디어 파일에 액세스해야 하는 서로 다른 서버에 시스템의 여러 인스턴스가 배포될 때 특히 영향을 받습니다.

범주 또는 제품 설명의 카탈로그 콘텐츠에 정적 또는 [동적 미디어 URL](../catalog/catalog-urls.md#configure-catalog-media-url-format)을 사용하도록 편집기를 구성할 수 있습니다.

![[!DNL Commerce] 미디어 저장소](./assets/media-storage.png){width="650" zoomable="yes"}

## 미디어 저장소에 파일 추가

처음 두 단계는 이미지를 삽입하는 것과 같습니다.

1. [편집기](editor.md) 도구 모음에서 _이미지 삽입_ 아이콘을 클릭합니다.

   ![이미지 삽입 아이콘](./assets/editor-toolbar-image-button.png){width="700" zoomable="yes"}

   이 작업은 _[!UICONTROL Insert/edit image]_&#x200B;대화 상자를 엽니다.

1. _[!UICONTROL Source]_&#x200B;후_&#x200B;검색&#x200B;_아이콘(![검색 아이콘](./assets/media-gallery-icon-browse.png){width="10" zoomable="no"})을 클릭합니다.

1. 왼쪽의 디렉터리 트리에서 다음 중 하나를 수행합니다.

   - 업로드한 이미지를 저장할 폴더로 이동합니다.

   - 폴더를 만들 위치로 이동하여 **폴더 만들기**&#x200B;를 클릭합니다.

     폴더를 추가하려면 폴더 이름을 입력하고 **[!UICONTROL OK]**&#x200B;을(를) 클릭합니다.

1. 하나 이상의 파일을 미디어 저장소에 추가하려면 시스템에서 파일을 업로드하거나 [Adobe Stock 통합](adobe-stock.md)을 사용할 수 있습니다.

   시스템에서 파일을 업로드하려면 **[!UICONTROL Choose Files]**&#x200B;을(를) 클릭하고 다음을 수행하십시오.

   - 로컬 컴퓨터의 디렉토리에서 이미지 위치로 이동합니다.

   - 업로드할 각 이미지를 선택하십시오.

   - **[!UICONTROL Open]**&#x200B;을(를) 클릭합니다.

   [통합](adobe-stock.md)을 사용하여 Adobe Stock의 자산을 사용하려면 다음을 수행하십시오.

   - **[!UICONTROL Search Adobe Stock]**&#x200B;을(를) 클릭합니다.

   - Adobe Stock에서 미리 보기 또는 라이선스가 부여된 이미지를 추가합니다([Adobe Stock 이미지 사용](adobe-stock-manage.md) 참조).

이미지가 서버의 현재 Media Storage 폴더에 업로드됩니다.

![[!DNL Commerce] 미디어 저장소](./assets/media-storage.png){width="650" zoomable="yes"}

## 미디어 저장소에서 이미지 삽입

편집할 페이지 또는 블록을 엽니다. 그런 다음 다음 다음 방법 중 하나를 사용하여 미디어 저장소에서 이미지를 삽입합니다.

### 방법 1: WYSIWYG 모드

1. [편집기](editor.md) 도구 모음에서 _이미지 삽입_ 아이콘을 클릭합니다.

1. _[!UICONTROL Source]_&#x200B;후_&#x200B;검색&#x200B;_아이콘(![검색 아이콘](./assets/media-gallery-icon-browse.png){width="10" zoomable="no"})을 클릭합니다.

   ![검색 아이콘 선택](./assets/editor-dialog-insert-image.png){width="250" zoomable="yes"}

1. 왼쪽의 디렉터리 트리에서 이미지가 저장된 폴더로 이동합니다.

1. 이미지의 타일을 선택하고 **[!UICONTROL Add Selected]**&#x200B;을(를) 클릭합니다.

### 방법 2: HTML 모드

1. `<img>` 태그를 삽입할 코드에 커서를 놓습니다.

1. **[!UICONTROL Insert Image]**&#x200B;을(를) 클릭합니다.

   ![이미지 삽입(HTML 모드)](./assets/editor-html-mode-insert-image.png){width="600" zoomable="yes"}
