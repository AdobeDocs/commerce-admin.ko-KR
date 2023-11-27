---
title: 제품 견본
description: 구성 가능한 제품 목록에 대한 견본을 정의하는 방법을 알아봅니다.
exl-id: 6163cec4-5d84-4e2c-ba5c-3c22ac4e3f28
feature: Catalog Management, Products
source-git-commit: 01148770946a236ece2122be5a88b963a0f07d1f
workflow-type: tm+mt
source-wordcount: '1160'
ht-degree: 0%

---

# 제품 견본

고객은 색상 선택에 대한 높은 기대를 가지며 제품 설명이 사용 가능한 각 색상, 패턴 또는 질감을 정확하게 나타내는 것이 중요합니다. 예를 들어 다음 예제의 바지는 빨강, 녹색 및 파랑으로 사용할 수 없습니다. 오히려, 그들은 아마도 이 제품에서 고유한 빨강, 초록, 파랑의 특정한 음영에서만 이용 가능합니다.

![제품 페이지의 견본](./assets/storefront-color-swatches.png){width="700" zoomable="yes"}

대상 [구성 가능한 제품](product-create-configurable.md), 색상은 시각적 견본, 텍스트 견본 또는 입력 컨트롤로 표시할 수 있습니다. 견본은 제품 페이지, 제품 목록 및 [계층화된 탐색](navigation-layered.md). 제품 페이지에서 견본은 견본이 선택되면 동기화되어 해당 제품 이미지를 표시합니다. 고객이 견본을 선택하면 해당 값이 입력 필드에 나타나고 현재 선택 항목으로 견본의 윤곽이 표시됩니다.

>[!NOTE]
>
>을 설정하여 견본을 선택할 때 해당 단순 제품 이미지가 표시되지 않도록 견본 속성을 구성할 수 있습니다. _[!UICONTROL Update Product Preview Image]_옵션 값: `No` 다음에 있음 [!UICONTROL Attribute Edit] 페이지 를 지정합니다.

## 텍스트 기반 견본

견본에 이미지를 사용할 수 없는 경우 속성 값이 텍스트로 표시됩니다. 텍스트 기반 색상 견본은 텍스트 레이블이 있는 버튼과 같으며, 이미지가 있는 색상 견본과 같은 방식으로 동작합니다. 텍스트 기반 견본을 사용하여 사용 가능한 크기를 표시하면 사용할 수 없는 모든 크기가 제외됩니다.

![텍스트 기반 견본 선택에 재고 부족 크기가 표시됩니다.](./assets/storefront-swatch-size-out-of-stock.png){width="700" zoomable="yes"}

## 레이어 탐색의 색상 견본

다음과 같은 경우 레이어 탐색에서 색상 견본을 사용할 수도 있습니다. _[!UICONTROL Use in Layered Navigation]_color 속성의 속성이 로 설정되어 있습니다. `Yes`. 다음 예제에서는 레이어 탐색의 텍스트 기반 및 색상 이미지 견본을 모두 보여 줍니다.

![레이어 탐색에 표시되는 견본](./assets/storefront-swatches-layered-navigation.png){width="700" zoomable="yes"}

## 제품에 대한 색상 견본 만들기

견본은 의 구성 요소로 정의할 수 있습니다. `color` 속성 또는 특정 제품에 대해 로컬로 설정하고 [제품 이미지](product-image.md#upload-an-image).

앞의 예에서 &quot;Sylvia Capri&quot; 바지는 의 특정 값으로 사용할 수 있습니다. `red`, `green`, 및 `blue`. 색상 견본은 제품 이미지에서 가져온 것이므로 각각이 색상을 실제로 표현한 것입니다. 다음 `color` 속성은 모든 제품 색상 및 견본에 대한 정보를 관리하는 데 사용됩니다.

### 1단계: 견본 만들기

다음 방법 중 하나를 사용하여 제품에 대한 색상 견본을 생성합니다.

#### 방법 1: 색상 견본 추가

1. 제품의 실제 색상을 캡처하려면 사진 편집기에서 이미지를 열고 스포이드 도구를 사용하여 정확한 색상을 식별하고 동등한 16진수 값을 기록합니다.

   ![16진수 색상 값](./assets/swatch-hex-values.png){width="400"}

1. 다음에서 _관리자_ 사이드바, 이동 **[!UICONTROL Stores]** > _[!UICONTROL Attributes]_>**[!UICONTROL Product]**.

1. 그리드에서 _색상_ 속성(편집 모드)입니다.

1. 다음을 확인합니다. **[!UICONTROL Catalog Input Type for Store Owner]** 이(가) (으)로 설정됨 `Visual Swatch`.

1. 제품 표시 페이지에서 견본이 선택되어 있을 때 해당하는 간단한 제품 이미지를 표시하지 않으려면 를 설정합니다 **[!UICONTROL Update Product Preview Image]** 끝 `No`.

1. 아래 _[!UICONTROL Manage Swatch (Values of Your Attribute)]_, 클릭&#x200B;**[!UICONTROL Add Swatch]**다음을 수행합니다.

   ![견본 값 관리](./assets/attribute-color-manage-swatch-values.png){width="600" zoomable="yes"}

   - 다음에서 _견본_ 열에서 새 견본을 클릭하고 선택 **[!UICONTROL Choose a color]** 메뉴에서 삭제할 수 있습니다.

     ![견본 색상 선택](./assets/attribute-color-swatch-menu.png){width="500" zoomable="yes"}

   - 색상 피커에서 커서를 **#** 필드에 현재 값을 삭제하고 새 색상의 6자리 16진수 값을 입력합니다.

     ![16진수 값 입력](./assets/attribute-swatch-color-picker-hex-value.png){width="500" zoomable="yes"}

   - 견본을 저장하려면 _색상 휠_ ( ![색상 아이콘](../assets/icon-color-wheel.png) ) 아이콘은 색상 피커의 오른쪽 아래 모서리에 있습니다.

   - 다음에서 _관리자_ 열에서 저장소 관리자에게 색상을 설명하는 레이블을 입력합니다.

     해당하는 경우 지원되는 각 언어에 대한 색상 번역을 입력할 수도 있습니다. 다음 예에서는 참조용으로 SKU가 포함되어 있습니다. _관리자_ 색상은 특정 제품에만 사용되기 때문에 레이블을 지정합니다. 레이블에 공백 또는 밑줄을 포함할 수 있지만 하이픈은 포함할 수 없습니다.

   - 다음에서 _기본임_ 열에서 기본 옵션으로 사용할 견본을 선택합니다.

   - 색상 견본의 순서를 변경하려면 _[!UICONTROL Order]_![정렬 순서 아이콘](../assets/icon-sort-order.png) 아이콘을 클릭하고 항목을 목록의 새 위치로 드래그합니다.

     ![견본 레이블](./assets/attribute-swatch-labels.png){width="400"}

1. 완료되면 다음을 클릭하십시오. **[!UICONTROL Save Attribute]** 메시지가 표시되면 캐시를 새로 고칩니다.

1. 각 제품을 편집 모드로 열고 **색상** 속성을 올바른 견본과 함께 사용합니다.

   여러 제품을 동시에 업데이트하려면 아래 단계를 따르십시오.

#### 방법 2: 견본 이미지 업로드

1. 견본의 이미지를 캡처하려면 사진 편집기에서 제품 이미지를 열고 색상, 패턴 또는 질감을 나타내는 이미지의 사각형 영역을 저장합니다.

   필요한 경우 제품의 각 변형에 대해 이 작업을 반복할 수 있습니다.

   견본의 크기와 치수는 테마에 의해 결정됩니다. 일반적으로 이미지를 사각형으로 저장하면 패턴의 종횡비를 유지하는 데 도움이 됩니다.

   ![견본 이미지](./assets/swatch-samples.png){width="400"}

1. 다음에서 _관리자_ 사이드바, 이동 **[!UICONTROL Stores]** > _[!UICONTROL Attributes]_>**[!UICONTROL Product]**.

1. 그리드에서 **[!UICONTROL color]** 속성(편집 모드)입니다.

1. 다음을 확인합니다. **[!UICONTROL Catalog Input Type for Store Owner]** 이(가) (으)로 설정됨 `Visual Swatch`.

1. 제품 표시 페이지에서 견본이 선택되어 있을 때 해당하는 간단한 제품 이미지를 표시하지 않으려면 를 설정합니다 **[!UICONTROL Update Product Preview Image]** 끝 `No`.

1. 아래 _[!UICONTROL Manage Swatch]_(속성 값), 클릭&#x200B;**[!UICONTROL Add Swatch]**다음을 수행합니다.

   - 다음에서 _[!UICONTROL Swatch]_열에서 새 견본을 클릭하여 메뉴를 표시하고 선택합니다.**[!UICONTROL Upload a file]**.

   - 준비한 견본 파일로 이동하여 업로드할 파일을 선택합니다.

   - 각 견본 이미지에 대해 이 단계를 반복합니다.

   - 관리자 및 상점 첫 화면의 레이블을 입력합니다.

     이 예에서 SKU는 특정 제품에만 사용되므로 참조를 위해 관리 레이블에 포함됩니다. 레이블에 공백 또는 밑줄을 포함할 수 있지만 하이픈은 포함할 수 없습니다.

     ![레이블 입력](./assets/swatch-upload.png){width="500" zoomable="yes"}

1. 완료되면 다음을 클릭하십시오. **[!UICONTROL Save Attribute]** 메시지가 표시되면 캐시를 새로 고칩니다.

1. 각 제품을 편집 모드로 열고 **[!UICONTROL Color]** 속성을 올바른 견본과 함께 사용합니다.

   여러 제품을 동시에 업데이트하려면 아래 단계를 따르십시오.

### 2단계: 제품 업데이트

1. 다음에서 _관리자_ 사이드바, 이동 **[!UICONTROL Catalog]** > **[!UICONTROL Products]**.

1. 사용 **[!UICONTROL Filter]** 이름 또는 SKU별로 목록을 표시하고 적용 가능한 제품만 포함합니다.

1. 그리드에서 견본이 적용되는 각 제품의 확인란을 선택합니다.

1. 설정 **[!UICONTROL Actions]** 끝 `Update Attributes`.

   이 예에서, 바지의 모든 파란색 구성이 선택된다.

   ![제품 견본 속성 업데이트](./assets/swatch-apply-update-attributes.png){width="600" zoomable="yes"}

1. 아래로 스크롤하여 **[!UICONTROL Color]** 속성을 지정하고 다음을 선택합니다. **[!UICONTROL Change]** 확인란.

   ![확인란 변경](./assets/swatch-update-attributes-choose-color.png){width="400"}

1. 선택한 제품에 적용되는 견본을 선택하고 **[!UICONTROL Save]**.

1. 메시지가 표시되면 캐시를 새로 고칩니다.

   ![상점 앞에 표시되는 견본](./assets/swatch-blue-schmear.png){width="200"}

## 단순 제품에 색상 견본 추가

1. 다음에서 _관리자_ 사이드바, 이동 **[!UICONTROL Catalog]** > **[!UICONTROL Products]**.

1. 편집 모드에서 제품을 열고 제품 상태를 확인합니다(활성화되어야 함).

1. 클릭 **[!UICONTROL Create Configurations]** 단추(아래) `Configurations` 탭).

1. 팝업 창에서 색상 속성을 선택하고 **[!UICONTROL Next]**.

1. 이 제품에 포함할 속성에서 색상 견본을 선택합니다.

1. 진행률 표시줄에서 **[!UICONTROL Next]**.

1. [이미지, 가격 및 수량 구성](product-create-configurable.md#step-3-configure-the-images-price-and-quantity).

   이 단계에서는 각 구성의 이미지, 가격 및 수량을 설정합니다. 사용 가능한 옵션은 각각에 대해 동일하며 하나만 선택할 수 있습니다. 모든 SKU에 동일한 설정을 적용하거나, 각 SKU에 고유한 설정을 적용하거나, 설정을 지금 건너뛸 수 있습니다.

1. 이미지, 가격 및 수량 구성이 완료되면 **[!UICONTROL Next]** 오른쪽 상단 모서리입니다.

   구성 섹션의 하단에 현재 제품 변형이 나타납니다. 구성에 만족하면 다음을 클릭합니다. **[!UICONTROL Generate Products]**.
