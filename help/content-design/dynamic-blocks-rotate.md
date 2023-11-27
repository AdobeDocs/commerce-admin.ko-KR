---
title: 회전하는 동적 블록 추가
description: 회전자에 여러 동적 블록을 추가하여 상점 전면에서 대화형 컨텐츠의 슬라이드 쇼를 표시합니다.
exl-id: 3d338014-cf26-4171-b48b-d37b3d7b0e81
source-git-commit: b659c7e1e8f2ae9883f1e24d8045d6dd1e90cfc0
workflow-type: tm+mt
source-wordcount: '621'
ht-degree: 0%

---

# 회전하는 동적 블록 추가

{{ee-feature}}

대화형 컨텐츠의 슬라이드 쇼를 표시하려면 여러 항목을 추가할 수 있습니다 [동적 블록](dynamic-blocks.md) 로테이터까지. 다음 [위젯](widgets.md) 도구는 로테이터를 단일 페이지 또는 스토어 전체의 여러 페이지에 있는 특정 위치에 배치하는 데 사용됩니다.

![동적 블록 회전체](./assets/widget-dynamic-block-rotator.png){width="700" zoomable="yes"}

## 1단계: 개별 동적 블록 만들기

종료 [동적 블록 만들기](dynamic-blocks.md) 회전자에 배치하려면 다음 지침을 따르십시오.

## 2단계: 동적 블록 회전 위젯 추가

1. 다음에서 _관리자_ 사이드바, 이동 **[!UICONTROL Content]** > _[!UICONTROL Elements]_>**[!UICONTROL Widgets]**.

1. 오른쪽 위 모서리에서 을(를) 클릭합니다. **[!UICONTROL Add Widget]**.

1. 아래 _설정_, 설정됨 **[!UICONTROL Type]** 끝 `Dynamic Blocks Rotator`.

1. 현재 항목 선택 **[!UICONTROL Design Theme]** 가게의.

   이 설정은 현재 패키지를 식별하거나 [테마](themes.md) 저장소의 페이지 레이아웃을 결정합니다.

1. 클릭 **[!UICONTROL Continue]**.

   ![동적 블록 회전체 설정](./assets/widget-dynamic-block-rotator-settings.png){width="600" zoomable="yes"}

## 3단계: 옵션 완료

1. 아래 _Storefront 속성_&#x200B;옵션을 설정합니다.

   - 입력 **[!UICONTROL Title]** 로테이터용

   - 다음에서 **[!UICONTROL Assign to Store Views]** 목록에서 [스토어 조회수](../getting-started/websites-stores-views.md) 로테이터를 사용할 수 있는 경우.

   - (선택 사항) **[!UICONTROL Sort Order]** 대상 컨테이너에서 회전자의 위치를 결정하는 번호입니다. 동일한 컨테이너에 할당될 수 있는 다른 위젯과 관련이 있습니다.

   ![회전자 상점 속성](./assets/widget-dynamic-block-rotator-storefront-properties.png){width="600" zoomable="yes"}

1. 아래 _레이아웃 옵션_, 클릭 **[!UICONTROL Add Layout Update]** 다음을 수행합니다.

   - 설정 **[!UICONTROL Display on]** 회전자가 나타날 페이지 또는 페이지 유형으로 변환됩니다.

      - `Categories` - 다음 중 하나에 회전자를 표시합니다. [앵커](../catalog/navigation-layered.md) 또는 비앵커 카테고리 페이지입니다. 옵션: 앵커 카테고리 / 비앵커 카테고리
      - `Products` - 특정 유형의 제품 페이지나 모든 제품 페이지에서 회전자를 표시합니다. 옵션: 모든 제품 유형 / [단순 제품](../catalog/product-create-simple.md) /  [가상 제품](../catalog/product-create-virtual.md) / [번들 제품](../catalog/product-create-bundle.md) / [다운로드 가능한 제품](../catalog/product-create-downloadable.md) / [기프트 카드](../catalog/product-gift-card-create.md) / [구성 가능한 제품](../catalog/product-create-configurable.md) / [그룹화된 제품](../catalog/product-create-grouped.md)
      - `Generic Pages` - 모든 페이지, 특정 페이지 또는 특정 레이아웃이 있는 페이지에만 회전자를 표시합니다. 옵션: `All Pages` / `Specified Page` / `Page Layouts`

     이 예제에서 회전자는 `Specified Page`.

   - 특정 항목 선택 **[!UICONTROL Page]** 회전자가 나타날 위치.

   - 설정 **[!UICONTROL Container]** 의 일부로 [페이지 레이아웃](page-layout.md#standard-page-layouts) 회전자가 나타날 위치.

     다른 위젯이 동일한 컨테이너에 할당되면 정렬 순서에 따라 순서대로 표시됩니다.

   - Accept `Dynamic Block Template` 을 기본값으로 **[!UICONTROL Template]**.

     이 설정은 회전자가 독립형인지 또는 기존 텍스트 내부에 배치되는지를 기반으로 회전자의 서식을 지정하는 데 사용되는 템플릿을 결정합니다.

     ![회전판 레이아웃 업데이트](./assets/widget-dynamic-block-rotator-layout-updates.png){width="600" zoomable="yes"}

   - 클릭 **[!UICONTROL Save and Continue Edit]**.

1. 왼쪽 패널에서 을 선택합니다 **[!UICONTROL Widget Options]**.

1. 의 경우 **[!UICONTROL Dynamic Blocks to Display]**, 수락 `Specified Dynamic Blocks`.

   이 설정은 회전기에 포함된 동적 블록의 유형을 결정합니다.

   - `Specified Dynamic Blocks` - 특정 동적 블록만 포함합니다.
   - `Cart Price Rule Related` - 장바구니 가격 규칙과 연결된 동적 블록만 포함합니다.
   - `Catalog Price Rule Related` - 카탈로그 가격 규칙과 연결된 동적 블록만 포함합니다.

1. 종료 **[!UICONTROL Restrict the Dynamic Block Types]** 위젯과 함께 사용할 수 있는 경우 `Content Area`.

   이 설정은 배너를 페이지 레이아웃의 특정 부분으로 제한합니다.

   - `Content Area` - 페이지의 기본 콘텐츠 영역에 동적 블록을 배치합니다.
   - `Footer` - 동적 블록을 페이지 바닥글에 넣습니다.
   - `Header` - 페이지 헤더에 동적 블록을 배치합니다.
   - `Left Column` - 가능한 경우 페이지 레이아웃의 왼쪽 열에 동적 블록을 배치합니다.
   - `Right Column` - 가능한 경우 페이지 레이아웃의 오른쪽 열에 동적 블록을 배치합니다.

1. 설정 **[!UICONTROL Rotation Mode]** 다음 중 하나를 수행합니다.

   - `Display all instead of rotating` - 동적 블록 스택을 표시합니다. 여기서 모든 블록을 볼 수 있습니다.
   - `One at a time, Random` - 지정된 동적 블록을 임의의 순서로 표시합니다. 페이지를 새로 고치면 다른(및 임의) 동적 블록이 나타납니다.
   - `One at the time, Series` - 지정된 동적 블록을 추가된 시퀀스에 표시합니다. 페이지를 새로 고치면 시퀀스의 다음 동적 블록이 나타납니다.
   - `One at the time, Shuffle` - 동적 블록을 섞은 순서로 한 번에 하나씩 표시합니다. 이 옵션은 다음과 유사합니다 `One at a time, Random` 동일한 동적 블록이 반복되지 않는다는 점을 제외하고 옵션을 선택합니다.

     ![회전 위젯 옵션](./assets/widget-dynamic-block-rotator-widget-options.png){width="600" zoomable="yes"}

1. 다음에서 **[!UICONTROL Specify Dynamic Blocks]** 그리드에서 회전자에 포함할 각 동적 블록의 확인란을 선택합니다.

1. 완료되면 다음을 클릭하십시오. **[!UICONTROL Save]**.
