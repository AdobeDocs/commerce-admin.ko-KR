---
title: 콘텐츠 블록 추가
description: 페이지 또는 다른 블록 내에서 재사용할 수 있는 콘텐츠의 사용자 지정 블록을 만듭니다.
exl-id: 2f104d77-a1d1-4f10-82ce-014955fe560b
source-git-commit: b659c7e1e8f2ae9883f1e24d8045d6dd1e90cfc0
workflow-type: tm+mt
source-wordcount: '520'
ht-degree: 0%

---

# 콘텐츠 블록 추가

콘텐츠의 사용자 지정 블록을 만든 다음 모든 페이지, 페이지 그룹 또는 다른 블록에 추가할 수 있습니다. 예를 들어 이미지 슬라이더를 블록에 배치한 다음 블록을 홈 페이지에 배치할 수 있습니다. 블록 작업 영역은 동일한 항목을 사용합니다 [기본 컨트롤](pages-workspace.md) (으)로 _페이지_ 사용 가능한 블록을 찾고 일상적인 유지 관리를 수행하는 데 도움이 되는 작업 영역 블록이 완료되면 다음을 사용할 수 있습니다 [위젯](widget-static-block.md) 스토어의 특정 페이지에 배치하기 위한 도구입니다.

![블록 페이지에는 기존 블록의 그리드가 표시됩니다](./assets/blocks-workspace.png){width="700" zoomable="yes"}

## 블록 만들기

1. 다음에서 _관리자_ 사이드바, 이동 **[!UICONTROL Content]** > _[!UICONTROL Elements]_>**[!UICONTROL Blocks]**.

1. 오른쪽 위 모서리에서 을(를) 클릭합니다. **새 블록 추가**.

   ![새 블록 페이지에 옵션과 컨텐츠 공간이 표시됩니다](./assets/block-detail.png){width="500" zoomable="yes"}

1. 새 블록의 기본 사용 상태를 변경하려면 다음을 설정합니다. **차단 활성화** 끝 `No`.

1. 할당 **블록 제목** 내부 참조용.

1. 고유 할당 **식별자** 블록용.

   공백 대신 밑줄이 있는 모든 소문자를 사용하십시오.

1. 각각 선택 **[!UICONTROL Store View]** 블록을 사용할 수 있는 위치입니다.

1. 표시된 콘텐츠 도구 세트를 사용하여 블록의 콘텐츠를 추가합니다.

   - If [페이지 빌더](../page-builder/introduction.md) 이(가) 활성화되었습니다. 다음을 선택하십시오. **[!UICONTROL Edit with Page Builder]** 콘텐츠의 페이지 빌더 도구 사용하기 [작업 영역](../page-builder/workspace.md).

     ![페이지 빌더 작업 영역](./assets/pb-workspace-block.png){width="500" zoomable="yes"}

     >[!NOTE]
     >
     >Page Builder를 사용하여 블록을 추가하는 방법에 대한 자세한 내용은 [자습서 2: 블록](../page-builder/2-blocks.md).

   - 사용 [편집자](editor.md) 텍스트 서식을 지정하고, 링크를 만들고, 표, 이미지, 비디오 및 오디오를 추가합니다.

     HTML 코드로 작업하려면 **편집기 표시/숨기기**.

     ![블록 편집기(숨김)](./assets/block-editor-hidden.png){width="500" zoomable="yes"}

1. 완료되면 다음을 클릭합니다. **[!UICONTROL Save]** 화살표 및 선택 **[!UICONTROL Save & Close]**.

   새 블록은 블록 격자에 있는 목록의 맨 아래에 나타납니다.

1. 사용 [위젯](widget-static-block.md) 스토어의 특정 페이지에 완료된 블록을 배치하는 도구입니다.

## 블록 삭제

사용자 지정 블록을 제거하는 방법에는 두 가지가 있습니다. 다음에서 제거할 수 있습니다. _블록_ 그리드 또는 블록 편집 페이지에서 선택할 수 있습니다.

### 방법 1: 블록 그리드에서 블록 제거

1. 다음에서 _관리자_ 사이드바, 이동 **[!UICONTROL Content]** > _[!UICONTROL Elements]_>**[!UICONTROL Blocks]**.
1. 그리드 위에서 필터를 사용하여 블록을 찾고 삭제할 하나 이상의 블록에 대한 확인란을 선택합니다.
1. 목록의 왼쪽 상단 모서리에서 을(를) 설정합니다. **[!UICONTROL Actions]** 끝 `Delete`.
1. 작업을 확인하려면 다음을 클릭합니다. **[!UICONTROL OK]**.

### 방법 2: 편집 페이지에서 블록 제거

1. 다음에서 _관리자_ 사이드바, 이동 **[!UICONTROL Content]** > _[!UICONTROL Elements]_>**[!UICONTROL Blocks]**.
1. 삭제할 블록을 찾습니다.
1. 다음에서 _작업_ 블록의 열에서 **[!UICONTROL Select]** 및 선택 **[!UICONTROL Edit]**.
1. 메뉴 모음에서 를 클릭합니다. **[!UICONTROL Delete Block]**.
1. 작업을 확인하려면 다음을 클릭합니다. **[!UICONTROL OK]**.

## 저장 메뉴

| 명령 | 설명 |
|----------|----------- |
| [!UICONTROL Save] | 현재 블록을 저장하고 작업을 계속합니다. |
| [!UICONTROL Save & Duplicate] | 현재 블록을 저장하고 닫은 다음 새 복사본을 엽니다. |
| [!UICONTROL Save & Close] | 현재 블록을 저장하고 닫은 다음 블록 그리드로 돌아갑니다. |

{style="table-layout:auto"}

## Lightbox 또는 슬라이더 추가

- 를 추가하는 것은 쉽습니다. [슬라이더](../page-builder/slider.md) (으)로 내 스토어에 [[!DNL Page Builder]](../page-builder/introduction.md). 슬라이더는 자동으로 재생되도록 설정하거나 탐색 단추를 사용하여 수동으로 제어할 수 있습니다.

  ![페이지 빌더 슬라이더](./assets/pb-tutorial3-slider-tee-shirt-promo.png){width="600" zoomable="yes"}

  에서 사용할 수 있는 jQuery 기반 이미지 lightbox의 다양한 종류가 있습니다. [[!DNL Commerce Marketplace]][1]그리고 일부는 무료입니다

- 에서 확장을 다운로드할 수도 있습니다. [!DNL Commerce Marketplace]. 추가 도움말은 확장 개발자가 제공하는 설명서를 참조하십시오.

[1]: https://marketplace.magento.com/extensions.html?q=lightbox
