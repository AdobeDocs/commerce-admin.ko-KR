---
title: 미디어 갤러리 자산 관리
description: Adobe Stock 통합을 통해 얻은 업로드된 미디어 파일 및 에셋을 관리하는 방법을 알아봅니다.
exl-id: 4fc489ae-b1e5-4aa4-832d-cd88c58d103a
feature: Page Content, Media
source-git-commit: a93e96353f4be0e771064cdcfbdf794772386a28
workflow-type: tm+mt
source-wordcount: '475'
ht-degree: 0%

---

# 미디어 갤러리 자산 관리

새로운 [미디어 갤러리](media-gallery.md) 는 업로드된 미디어 파일 및 을 통해 획득한 에셋을 관리하기 위한 도구를 제공합니다. [Adobe Stock 통합](adobe-stock.md). Adobe Stock을 저장한 경우 [이미지 미리 보기](adobe-stock-save-preview.md), 다음과 같은 작업을 수행할 수도 있습니다 [라이센스](adobe-stock-license-image.md) 새 미디어 갤러리의 이미지입니다.

## 에셋 업로드

1. 다음에서 _관리자_ 사이드바, 이동 **[!UICONTROL Content]** > _[!UICONTROL Media]_>**[!UICONTROL Media Gallery]**.

1. 클릭 **[!UICONTROL Upload Image]**.

1. 업로드할 파일을 선택합니다.

   선택한 에셋은 선택한 폴더(또는 폴더를 선택하지 않은 경우 스토리지 루트)에 자동으로 업로드됩니다.

## 자산 세부 사항 보기

1. 다음에서 _관리자_ 사이드바, 이동 **[!UICONTROL Content]** > _[!UICONTROL Media]_>**[!UICONTROL Media Gallery]**.

1. 자산 아래에 있는 세 점을 클릭합니다(![세부 정보 아이콘](./assets/media-gallery-asset-menu-icon.png){width="10" zoomable="no"})을 클릭한 다음 을 클릭합니다 **[!UICONTROL View Details]**.

   ![자산 작업](./assets/media-gallery-asset-actions.png){width="600" zoomable="yes"}

   에셋 세부 사항이 슬라이드 패널에 표시됩니다. 여기에는 에셋이 사용되는 정보가 포함됩니다.

   - **[!UICONTROL Categories]**
   - **[!UICONTROL Products]**
   - **[!UICONTROL Pages]**
   - **[!UICONTROL Blocks]**

   ![자산 세부 사항](./assets/media-gallery-asset-details.png){width="600" zoomable="yes"}

   세부 정보를 보려면 **[!UICONTROL Used In]** 링크 . 다음 예제의 표에는 특정 자산이 사용되는 모든 카테고리가 표시됩니다.

   ![범주 그리드](./assets/media-gallery-asset-categories.png){width="600" zoomable="yes"}

   에서 에셋을 삭제할 수도 있습니다. _세부 사항 보기_ 섹션.

## 에셋 편집

1. 다음에서 _관리자_ 사이드바, 이동 **[!UICONTROL Content]** > _[!UICONTROL Media]_>**[!UICONTROL Media Gallery]**.

1. 자산 아래에 있는 세 점을 클릭합니다(![에셋 메뉴 아이콘](./assets/media-gallery-asset-menu-icon.png){width="10" zoomable="no"})을 클릭한 다음 을 클릭합니다 **[!UICONTROL Edit]**.

   ![에셋 편집](./assets/media-gallery-edit-asset.png){width="600" zoomable="yes"}

1. 필요한 경우 다음 메타데이터 값 중 하나를 변경합니다.

   - **[!UICONTROL Title]**
   - **[!UICONTROL Description]**
   - **[!UICONTROL Tags/Keywords]**

   이 데이터는 데이터 베이스와 파일 메타데이터 자체에 저장됩니다. 현재 XMP 및 IPTC 형식이 지원됩니다.

   업데이트된 메타데이터로 이미지를 다운로드할 수 있습니다.

## 에셋 사용

에셋은 다음과 같이 관리자 전체에서 광범위하게 사용할 수 있습니다. [페이지 추가 또는 편집](page-add.md), [범주 만들기 또는 편집](../catalog/category-create.md), 또는 [콘텐츠 편집기에서 이미지 삽입](editor-insert-image.md).

1. 미디어 에셋을 사용할 수 있는 영역에서 새 미디어 갤러리에 액세스합니다.

1. 에셋을 선택하고 **[!UICONTROL Add Selected]**.

{{$include /help/_includes/image-optimization-animated-gif-note.md}}

## 에셋 삭제

1. 다음에서 _관리자_ 사이드바, 이동 **[!UICONTROL Content]** > _[!UICONTROL Media]_>**[!UICONTROL Media Gallery]**.

1. 클릭 **[!UICONTROL Delete Images...]** 삭제할 각 에셋에 대한 확인란을 선택합니다.

1. 확인 대화 상자에서 **[!UICONTROL Delete Image]**.

   ![삭제 확인](./assets/media-gallery-bulk-delete-confirm.png){width="500" zoomable="yes"}

## 에셋 검색

1. 다음에서 _관리자_ 사이드바, 이동 **[!UICONTROL Content]** > _[!UICONTROL Media]_>**[!UICONTROL Media Gallery]**.

1. 사용 **[!UICONTROL Search by keywords]** 키워드/태그로 이미지 검색을 수행하기 위한 입력.

   다음 예에서 검색은 특정 태그( )가 포함된 자산을 찾습니다.`mountain`).

   ![자산 검색](./assets/media-gallery-asset-search.png){width="600" zoomable="yes"}

>[!NOTE]
>
>이미지 태그를 업데이트하는 방법에 대한 자세한 내용은 _[에셋 편집](#edit-an-asset)_ 섹션.

## 자산 필터링

>[!NOTE]
>
>다음 _다음에서 사용됨_ 기능을 사용하려면 [!UICONTROL Media Gallery Image Optimization] 이(가) 다음에서 활성화됨: [구성 설정](media-gallery-image-optimization.md).

1. 다음에서 _관리자_ 사이드바, 이동 **[!UICONTROL Content]** > _[!UICONTROL Media]_>**[!UICONTROL Media Gallery]**.

1. 다음을 클릭합니다. **[!UICONTROL Filters]** 탭.

   ![필터](./assets/media-gallery-filters.png){width="600" zoomable="yes"}

1. 필터링 옵션을 설정합니다.

   엔티티의 사용에 따라 에셋을 필터링할 수 있습니다.

   - **[!UICONTROL Used in Categories]**
   - **[!UICONTROL Used in Products]**
   - **[!UICONTROL Used in Pages]**
   - **[!UICONTROL Used in Blocks]**

   다음 기준으로 자산을 필터링할 수도 있습니다. **[!UICONTROL Store View]**, **[!UICONTROL License Status]**, 및 **[!UICONTROL Content Status]**. 날짜 범위 설정 **[!UICONTROL Uploaded Date]** 및/또는 **[!UICONTROL Modification Date]** 파일 날짜에 따라 에셋을 필터링합니다.

1. 클릭 **[!UICONTROL Apply Filters]** 결과를 확인합니다.

   다음 예제의 필터링은 특정 범주( )에서 사용되는 에셋을 찾습니다.`cars`) 및 가 활성화됩니다.

   ![활성화된 에셋을 범주별로 필터링](./assets/media-gallery-filter-by-category.png){width="600" zoomable="yes"}

## 중복 이미지 찾기

1. 다음을 클릭합니다. **[!UICONTROL Filters]** 탭을 클릭하고 다음을 선택합니다. **[!UICONTROL Show duplicates]** 확인란.

1. 결과를 보려면 다음을 클릭하십시오. **[!UICONTROL Apply Filters]**.
