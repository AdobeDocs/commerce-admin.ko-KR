---
title: 콘텐츠 추가 - 제품
description: 에 제품 목록을 추가하는 데 사용되는 제품 콘텐츠 유형에 대해 알아봅니다. [!DNL Page Builder] 스테이지.
exl-id: 8ef38669-a6f6-493b-b963-b0fc4e3bbff4
feature: Page Builder, Page Content, Products
source-git-commit: 167e9d906cebb645f76a5112fa629a73ba823ebc
workflow-type: tm+mt
source-wordcount: '1912'
ht-degree: 0%

---

# 콘텐츠 추가 - 제품

사용 _제품_ 제품 목록을 추가할 콘텐츠 유형 [[!DNL Page Builder] 단계](workspace.md#stage)그리드 또는 회전 메뉴 레이아웃 사용. 사용 [콘텐츠 추가 - 차단](block.md) 블록을 배치하기 위한 도구 [!DNL Page Builder] 단계를 수행한 다음 블록 내에 제품 목록을 배치합니다. 또는 제품 목록을 페이지의 행에 바로 추가할 수 있습니다.

## 제품 캐러셀 사용 지침

제품 캐러셀은 제품을 자랑할 수 있는 강력하고 매력적인 방법을 제공합니다. 이를 최대한 활용하려면 다음 지침을 권장합니다.

- 행, 탭 또는 1열 레이아웃과 같은 페이지 너비 컨테이너에 제품 회전 메뉴를 직접 추가합니다. 페이지 너비 레이아웃을 사용하면 제품을 가장 잘 반응형으로 표시할 수 있습니다. [!DNL Page Builder] 컨테이너의 너비가 아니라 페이지 너비에 따라 표시되는 제품 수를 줄입니다.

- 제품 캐러셀을 좁은 열에 추가하지 마십시오. 언급된 바와 같이, [!DNL Page Builder]는 기본적으로 열 너비가 아니라 페이지 너비를 기반으로 표시할 제품 수를 결정합니다.

- 제품 캐러셀이 계속 자동 스크롤되도록 하려면 두 옵션을 모두 설정합니다. **[!UICONTROL Autoplay]** 및 **[!UICONTROL Infinite Loop]** 끝 `Yes`. 자동 재생이 로 설정된 경우 `Yes` 그러나 무한 루프가 `No`, 자동 스크롤은 제품 목록 끝에서 중지됩니다.

- 설정 **[!UICONTROL Carousel Mode]** 끝 `Continuous` 슬라이드 내에서 한 번에 하나씩 강조 표시하고, 가운데로, 스크롤합니다. 다른 제품은 목록에 표시되지만 가운데 있는 제품을 강조하기 위해 투명합니다.

  ![연속 회전 모드의 제품 목록](./assets/pb-products-settings-carousel-continuous.png){width="600"}

- 회전 메뉴 내에서 한 번에 최대 5개의 제품을 표시하고 스크롤하려면 **[!UICONTROL Carousel Mode]** 을 로 설정 `Default`.

  ![기본 회전 모드의 제품 목록](./assets/pb-products-settings-carousel-default.png){width="600"}

다음 지침은 블록에 제품 목록을 추가하는 방법을 보여줍니다. 그런 다음 를 사용할 수 있습니다 [위젯](../content-design/widgets.md) 스토어의 페이지에서 특정 위치에 블록을 배치합니다.

{{$include /help/_includes/page-builder-save-timeout.md}}

## 제품 도구 상자

| 도구 | 아이콘 | 설명 |
| --------- | ------------- | ----------------- |
| 이동 | ![이동 아이콘](./assets/pb-icon-move.png){width="25"} | 제품 컨테이너와 해당 콘텐츠를 스테이지의 다른 위치로 이동합니다. |
| 설정 | ![설정 아이콘](./assets/pb-icon-settings.png){width="25"} | 다음을 엽니다. _제품 편집_ 제품 목록을 선택하고 컨테이너의 속성을 변경할 수 있는 페이지입니다. |
| 숨기기 | ![아이콘 숨기기](./assets/pb-icon-hide.png){width="25"} | 현재 제품 컨테이너 및 해당 콘텐츠를 숨깁니다. |
| 표시 | ![아이콘 표시](./assets/pb-icon-show.png){width="25"} | 숨겨진 제품 컨테이너와 해당 콘텐츠를 표시합니다. |
| 복제 | ![중복 아이콘](./assets/pb-icon-duplicate.png){width="25"} | 제품 컨테이너 및 해당 콘텐츠의 복사본을 만듭니다. |
| 제거 | ![제거 아이콘](./assets/pb-icon-remove.png){width="25"} | 스테이지에서 제품 컨테이너 및 해당 콘텐츠를 삭제합니다. |

{style="table-layout:auto"}

{{$include /help/_includes/page-builder-hidden-element-note.md}}

## 제품 목록 블록 만들기

1. 다음에서 _관리자_ 사이드바, 이동 **[!UICONTROL Content]** > _[!UICONTROL Elements]_>**[!UICONTROL Blocks]**.

1. 클릭 **[!UICONTROL Add New Block]**.

1. 다음을 입력합니다. **[!UICONTROL Block Title]** 및 **[!UICONTROL Identifier]**.

1. 다음을 선택합니다. **[!UICONTROL Store View]** 블록을 사용할 수 있는 위치입니다.

1. 아래로 스크롤하여 클릭 **[!UICONTROL Edit with Page Builder]** 또는 콘텐츠 미리보기 영역 내에서 [!DNL Page Builder] 작업 영역.

1. 다음에서 [!DNL Page Builder] 패널, 확장 **[!UICONTROL Add Content]** 드래그 **[!UICONTROL Products]** 자리 표시자가 스테이지에 표시됩니다.

   ![제품 콘텐츠 유형 추가](./assets/pb-add-content-products-drag.png){width="600" zoomable="yes"}

## 제품 목록 컨테이너 구성

비어 있는 항목 위로 마우스 오버 _제품_ 도구 상자를 표시하고 _설정_ (![설정 아이콘](./assets/pb-icon-settings.png){width="20"} ) 아이콘.

![제품 도구 상자](./assets/pb-add-content-products-toolbox.png){width="500" zoomable="yes"}

다음을 완료합니다. _설정_ 다음 섹션에 따라:

### 모양

1. 페이지에 제품 목록이 표시되는 방식을 결정하려면 모양 유형 중 하나를 선택합니다.

   | 유형 | 설명 |
   | ---- | ----------- |
   | 제품 격자 | 행당 5개의 제품(기본적으로)을 표시하는 그리드 내의 제품을 표시합니다. **[!UICONTROL Number of Products to Display]** 설정. |
   | 제품 회전 | 슬라이드(슬라이더라고도 함) 내의 제품을 표시합니다. 슬라이드 하나에 최대 5개의 제품이 표시됩니다. <br/><br/>**응답성 경고**: 이 모양을 선택할 때는 제품 콘텐츠 유형을 응답형 행, 탭 또는 1열 레이아웃에 직접 추가하여 작은 화면에서 한 쪽에 더 적은 수의 제품을 표시하는 것이 가장 좋습니다. 페이지 너비보다 좁은 콘텐츠 유형(예: 좁은 열)에 추가하면 슬라이드 하나에 화면 크기에 관계없이 컨테이너가 허용하는 것보다 더 많은 제품이 표시됩니다. |

   {style="table-layout:auto"}

   ![제품 모양](./assets/pb-products-appearances.png){width="300"}

   제품 캐러셀을 선택하는 경우 [회전 메뉴 설정](#carousel-settings).

1. 대상 **[!UICONTROL Select Products By]**&#x200B;제품 선택 방법을 선택합니다.

   범주, SKU 또는 조건별로 제품을 선택할 수 있습니다. 이러한 옵션은 함께 사용할 수 없습니다. 예를 들어 카테고리 옵션을 선택하고 카테고리 선택기를 사용한 다음 조건 옵션으로 전환하여 일부 조건을 추가할 수 없습니다. 제품은 다음에 대해 설정한 사항만 기준으로 선택됩니다. _1_ 세 가지 옵션 중 하나를 선택하십시오.

   - **[!UICONTROL Category]** - 선택한 카테고리를 사용하는 제품을 표시하려면 이 옵션을 선택합니다.

     ![범주별 제품 선택](./assets/pb-products-settings_category.png){width="500"}

     이 옵션을 선택하면 **[!UICONTROL Category]** 선택기. 화살표를 클릭하고 드릴다운하여 표시할 제품 카테고리를 선택합니다. 예를 들어, [!DNL Commerce] 샘플 데이터, 드릴인 및 선택 _여성 > 위쪽 > 티_ 해당 범주에 대한 모든 제품을 표시합니다.

     ![카탈로그 범주 선택](./assets/pb-select-products-by-category.png){width="500"}

   - **[!UICONTROL SKU]** - 하나 이상의 SKU를 사용하는 제품을 표시하려면 이 옵션을 선택합니다.

     이 옵션을 선택하면 **[!UICONTROL Product SKUs]** 표시할 SKU의 목록을 쉼표로 구분하여 입력해야 하는 텍스트 상자입니다.

     ![SKU별 제품 선택](./assets/pb-products-settings_sku.png){width="500"}

   - **[!UICONTROL Condition]** - 정의한 하나 이상의 조건에 따라 제품을 표시하려면 이 옵션을 선택합니다.

     이 옵션을 선택하면 제품 선택에 조건을 추가하는 데 사용할 수 있는 도구가 있습니다. 예를 들어 Gender가 Unisex로 설정된 제품만 선택할 수 있습니다.

     ![조건별 제품 선택](./assets/pb-products-settings_condition.png){width="500"}

     >[!NOTE]
     >
     >카테고리 또는 SKU 옵션을 선택하면 **[!UICONTROL Sort By]** 옵션 / `Position`. 이 정렬 옵션을 사용하면 제품이 카탈로그에 표시되는 순서와 동일한 순서로 표시됩니다.</br>
     >
     >범주 옵션의 경우 위치별로 정렬하면 카탈로그에 표시된 순서와 동일한 순서로 제품이 표시됩니다. SKU 옵션의 경우 위치별로 정렬하면 **[!UICONTROL Product SKUs]** 텍스트 상자.

1. 대상 **[!UICONTROL Sort By]**&#x200B;목록에서 제품에 대한 정렬 순서를 선택합니다.

   | 옵션 | 설명 |
   | ------ | ----------- |
   | `Position` (범주 및 SKU 옵션만 해당) | 범주 옵션을 선택하면 위치에 카탈로그에서 해당 위치와 동일한 순서로 제품이 표시됩니다. SKU 옵션을 선택하면 위치에 제품 SKU 텍스트 상자 내의 SKU와 동일한 순서로 제품이 표시됩니다. |
   | `Newest products first` | 카탈로그에 추가된 날짜별로 제품을 정렬하고 가장 최근 시작 날짜가 포함된 제품을 먼저 표시합니다. |
   | `Oldest products first` | 카탈로그에 추가된 날짜별로 제품을 정렬하고 시작 날짜가 가장 오래된 제품을 먼저 표시합니다. |
   | `Name: A - Z` | 제품을 알파벳순으로 정렬합니다. |
   | `Name: Z - A` | 제품을 알파벳 역순으로 정렬합니다. |
   | `SKU: ascending` | SKU별로 제품을 영숫자 순서로 정렬합니다. |
   | `SKU: descending` | 제품을 SKU별로 영숫자 역순으로 정렬합니다. |
   | `Stock: low stock first` | 가장 낮은 가용 재고부터 가장 높은 재고까지 제품을 정렬합니다. |
   | `Stock: high stock first` | 사용 가능한 재고가 가장 높은 항목부터 가장 낮은 항목까지 제품을 정렬합니다. |
   | `Price: high to low` | 제품을 최고 가격에서 최저 가격으로 정렬합니다. |
   | `Price: low to high` | 제품을 가장 낮은 가격부터 가장 높은 가격까지 정렬합니다. |

   {style="table-layout:auto"}

   ![제품 정렬 옵션](./assets/pb-products-sortby.png){width="300"}

1. 다음을 입력합니다. **[!UICONTROL Number of Products to Display]** 회전 메뉴 또는 그리드에서 사용할 수 있습니다.

   값은 다음에서 산출할 수 있습니다. `1` 끝 `999`. 기본값은 입니다 `5` 그리드 및 `20` 회전목마용입니다.

   >[!NOTE]
   >
   >카테고리, SKU 또는 조건 설정의 일부 제품이 제품 표 또는 회전판에 표시되지 않을 수 있습니다. 예를 들어 비활성화된 제품, 표시되지 않는 것으로 표시된 제품, 품절된 제품 및 다른 웹 사이트에 할당된 제품이 표시되지 않습니다.

   >[!IMPORTANT]
   >
   >구성 가능, 그룹화 및 번들(동적 가격) 제품의 가격은 관리자에 정의되지 않습니다. 따라서 이러한 제품은에 표시되지 않습니다 **[!UICONTROL Preview]** 가격별로 제품이 필터링되는 경우. 이 제품들은 **[!UICONTROL Preview]** 가격별로 주문하는 경우.

### 회전 메뉴 설정

1. 제품이 회전 메뉴에 표시되는 방식을 결정하려면 **[!UICONTROL Carousel Mode]**:

   | 옵션 | 설명 |
   | ------ | ----------- |
   | `Default` | 슬라이드는 기본적으로 슬라이드당 5개의 제품을 표시하며 필요에 따라 해당 숫자를 적절히 줄입니다. |
   | `Continuous` | 회전 메뉴에 기본적으로 슬라이드당 5개의 제품이 표시되지만(제품 절반 오른쪽 및 왼쪽), 한 번에 한 제품을 무한 루프로 가운데로 맞추고 스크롤합니다. 가운데 있는 제품의 좌우에 있는 제품들은 흐리게 표시되어 가운데 있는 제품이 부각되도록 한다. |

   {style="table-layout:auto"}

   이 두 모드 간에 전환하면 를 제외한 다른 회전 메뉴 설정이 유지됩니다 **[!UICONTROL Infinite Loop]** 설정, 항상 로 설정됨 `Yes` 연속 모드에서 이 필드는 비활성화됩니다.

   ![회전 메뉴 설정](./assets/pb-products-carousel-settings.png){width="600" zoomable="yes"}

1. 필요한 경우 **[!UICONTROL Autoplay]** 옵션 대상 `Yes`.

   자동 재생이 활성화되면 페이지가 로드될 때 캐러셀이 자동으로 스크롤을 시작합니다. 기본 설정을 그대로 두면(`No`) 고객은 각 슬라이드를 순서대로 표시하려면 슬라이드 탐색(점 또는 화살표)을 클릭해야 합니다.

   이 기능을 활성화하면 을 입력합니다. **[!UICONTROL Autoplay Speed]** 각 슬라이드 사이의 지연 시간(밀리초)을 지정합니다. 기본값은 입니다. `4000` (4초).

1. 필요한 경우 **[!UICONTROL Infinite Loop]** 옵션 대상 `Yes`.

   무한 루프가 활성화되면 페이지가 열려 있는 동안 슬라이드 쇼가 무기한 재생됩니다. 기본 설정을 그대로 두면(`No`) 슬라이드 쇼는 한 번만 재생됩니다.

   >[!NOTE]
   >
   >다음을 설정하는 경우 **[!UICONTROL Infinite Loop]** 끝 `No` 및 **[!UICONTROL Autoplay]** 을 로 설정 `Yes`로 설정하면 표시되는 제품 수가 끝나면 자동 재생이 중지됩니다.

1. 필요한 경우 **[!UICONTROL Show Arrows]** 옵션 대상 `Yes`.

   이 옵션을 활성화하면 각 슬라이드에 다음이 포함됩니다 _다음_ 및 _이전_ 왼쪽 및 오른쪽에 있는 탐색 화살표 기본 설정을 그대로 두면(`No`) 슬라이드는 탐색 화살표를 표시하지 않습니다.

1. 필요한 경우 **[!UICONTROL Show Dots]** 옵션 대상 `No`.

   기본 설정으로 설정된 경우(`Yes`) 탐색 점은 회전식 슬라이더 하단에 나타납니다. 이 설정을 사용하지 않으면 회전 슬라이더에 탐색 점이 표시되지 않습니다.

### 고급

1. 상위 컨테이너 내에서 제품 목록의 위치를 제어하려면 **[!UICONTROL Alignment]**:

   | 옵션 | 설명 |
   | ------ | ----------- |
   | `Default` | 현재 테마의 스타일시트에 지정된 정렬 기본 설정을 적용합니다. |
   | `Left` | 지정된 패딩을 허용하여 부모 컨테이너의 왼쪽 테두리를 따라 목록을 정렬합니다. |
   | `Center` | 지정된 패딩을 허용하여 부모 컨테이너의 중앙에 있는 목록을 정렬합니다. |
   | `Right` | 지정된 패딩을 허용하여 부모 컨테이너의 오른쪽 테두리를 따라 목록을 정렬합니다. |

   {style="table-layout:auto"}

1. 설정 **[!UICONTROL Border]** 제품 컨테이너의 네 면에 모두 적용되는 스타일:

   | 옵션 | 설명 |
   | ------ | ----------- |
   | `Default` | 연관된 스타일 시트에서 지정한 기본 테두리 스타일을 적용합니다. |
   | `None` | 컨테이너 테두리를 시각적으로 표시하지 않습니다. |
   | `Dotted` | 컨테이너 테두리가 점선으로 표시됩니다. |
   | `Dashed` | 컨테이너 테두리는 파선으로 표시됩니다. |
   | `Solid` | 컨테이너 테두리가 실선으로 표시됩니다. |
   | `Double` | 컨테이너 테두리는 이중 선으로 표시됩니다. |
   | `Groove` | 컨테이너 테두리는 홈이 있는 선으로 표시됩니다. |
   | `Ridge` | 컨테이너 테두리는 절선으로 표시됩니다. |
   | `Inset` | 컨테이너 테두리는 인세트 선으로 표시됩니다. |
   | `Outset` | 컨테이너 테두리는 외곽선으로 표시됩니다. |

   {style="table-layout:auto"}

1. 테두리 스타일을 설정할 때 `None`테두리 표시 옵션을 완료합니다.

   | 옵션 | 설명 |
   | ------ |------------ |
   | [!UICONTROL Border Color] | 색상 견본을 선택하거나 색상 선택기를 클릭하거나 유효한 색상 이름 또는 이에 해당하는 16진수 값을 입력하여 색상을 지정합니다. |
   | [!UICONTROL Border Width] | 테두리 라인 너비의 픽셀 수를 입력합니다. |
   | [!UICONTROL Border Radius] | 테두리의 각 모퉁이를 둥글게 만드는 데 사용되는 반경의 크기를 정의하려면 픽셀 수를 입력합니다. |

   {style="table-layout:auto"}

1. (선택 사항) 다음 이름을 지정합니다 **[!UICONTROL CSS classes]** 현재 스타일 시트에서 컨테이너에 적용

   여러 클래스 이름은 공백으로 구분합니다.

1. 다음에 대한 값을 픽셀 단위로 입력하십시오. **[!UICONTROL Margins and Padding]** 를 클릭하여 제품 컨테이너의 외부 여백 및 내부 패딩을 확인합니다.

   다이어그램에 해당 값을 입력합니다.

   | 컨테이너 영역 | 설명 |
   | -------------- | ----------- |
   | [!UICONTROL Margins] | 컨테이너의 모든 면 바깥쪽 가장자리에 적용되는 빈 공간의 양입니다. 옵션: `Top` / `Right` / `Bottom` / `Left` |
   | [!UICONTROL Padding] | 컨테이너의 모든 측면 안쪽 가장자리에 적용되는 빈 공간의 양입니다. 옵션: `Top` / `Right` / `Bottom` / `Left` |


## 스테이지에서 저장하고 미리 보기

오른쪽 위 모서리에서 을(를) 클릭합니다. **[!UICONTROL Save]** 설정을 적용하고 로 돌아가려면 [!DNL Page Builder] 작업 영역.

제품 캐러셀을 구성한 경우 다음 예제와 유사해야 합니다.

![스테이지의 제품 캐러셀](./assets/pb-products-admin-carousel.png){width="600"}

이제 다음을 사용할 수 있습니다. [위젯](../content-design/widgets.md) 이 블록을 스토어에 표시할 위치에 배치합니다. 또는 다음을 사용할 수 있습니다 [콘텐츠 추가 - 차단](block.md) 기존 페이지, 탭 또는 블록에 블록을 추가합니다.
