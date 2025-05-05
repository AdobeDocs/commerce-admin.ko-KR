---
title: 번들 제품 가져오기
description: 번들 제품에 대한 제품 데이터 가져오기의 예를 검토하십시오.
exl-id: 52146979-9911-449b-9f14-54377e2ae9f4
feature: Products, Data Import/Export
source-git-commit: 64ccc2d5016e915a554c2253773bb50f4d33d6f4
workflow-type: tm+mt
source-wordcount: '628'
ht-degree: 0%

---

# 번들 제품 가져오기

번들 제품은 선택 품목을 제시하며 고객이 구매하고자 하는 품목을 선택할 수 있도록 한다. 번들을 구성하는 모든 항목이 카탈로그에 [단순 제품](../catalog/product-create-simple.md) 또는 [가상 제품](../catalog/product-create-virtual.md) 중 하나로 존재합니다. 일반적으로 번들 제품은 관리자에서 만들어지고 업데이트됩니다. 그러나 데이터를 가져와서 번들 제품을 만들거나 기존 번들 제품을 내보내고 데이터를 편집한 후 다시 카탈로그로 가져올 수도 있습니다. Sprite Yoga Companion Kit는 다음 예에서 사용하는 샘플 데이터의 번들 제품입니다.

![제품 번들](../catalog/assets/product-bundle.png){width="700" zoomable="yes"}

## 번들 항목의 순서 변경

묶음 상품에 있는 물건의 순서를 바꾸는 방법은 두 가지가 있다.

### 방법 1: 드래그 앤 드롭

관리자의 [번들](../catalog/product-create-bundle.md) 제품으로 작업할 때 항목 및 섹션을 위치로 끌어다 놓을 수 있습니다.

![번들 항목](../catalog/assets/product-bundle-items-move.png){width="600" zoomable="yes"}

### 방법 2: 제품 데이터 편집

번들 제품의 구조를 이해하는 가장 좋은 방법은 제품을 내보내고 스프레드시트의 데이터를 검사하는 것입니다. 제품을 내보내고 각 항목의 데이터에 위치 매개 변수를 추가하여 번들 항목의 순서를 변경할 수 있습니다. 항목 데이터는 내보낸 제품의 `bundle_values` 열에 있습니다. 스프레드시트에서 열면 제품과 연관된 모든 항목이 긴 텍스트 문자열로 단일 셀에 있습니다. `bundle_values` 열에는 각 항목에 대해 다음 요소가 포함되어 있습니다.

- 항목 섹션의 이름
- 입력 제어
- 필수 항목 표시기
- SKU
- 색상
- 가격
- 기본 옵션 표시기
- 기본 수량
- 가격 유형
- 편집 가능한 수량 표시기

#### 1단계: 번들 제품 내보내기

이 단계에서는 스프라이트 요가 컴패니언 키트를 ([CSV](data-csv.md)) 파일로 내보냅니다. 카탈로그에 있는 다른 번들 제품을 사용할 수 있습니다.

1. _관리자_ 사이드바에서 **[!UICONTROL System]** > _[!UICONTROL Data Transfer]_>**[!UICONTROL Export]**(으)로 이동합니다.

1. _내보내기 설정_&#x200B;에서 **[!UICONTROL Entity Type]**&#x200B;을(를) `Products`(으)로 설정합니다.

1. 제품 특성 목록에서 **[!UICONTROL SKU]**(으)로 스크롤하여 내보낼 번들 제품의 SKU를 입력합니다.

   이 예제의 제품에 대한 SKU는 `24-WG080`입니다.

1. 섹션 아래쪽으로 스크롤하여 **[!UICONTROL Continue]**&#x200B;을(를) 클릭합니다.

1. _[!UICONTROL File name]_&#x200B;그리드의&#x200B;_[!UICONTROL Action]_ 열에서 **[!UICONTROL Select]**&#x200B;을(를) 클릭하고 `Download`을(를) 선택합니다.

   파일이 브라우저에서 사용하는 다운로드 위치에 나타납니다.

#### 2단계: 데이터 편집

1. 스프레드시트에서 다운로드한 CSV 파일을 엽니다.

1. `bundle_values` 열이 표시될 때까지 맨 오른쪽으로 스크롤합니다.

   `bundle_values` 데이터에서 각 요소는 쉼표로 구분되고, 각 번들 항목은 세로 막대를 사용하여 그 다음 항목과 구분됩니다. 마지막 항목은 세로 막대로 끝나지 않습니다. 내보낸 번들 데이터는 다음 예와 유사해야 합니다.

   ![번들 값](./assets/product-bundle-values-export-data.png){width="600" zoomable="yes"}

1. 쉽게 편집할 수 있도록 `bundle_values` 데이터를 복사하여 텍스트 편집기에 붙여 넣은 다음 각 항목 뒤에 줄 바꿈을 추가하여 각 항목이 별도의 줄에 있도록 할 수 있습니다.

1. 데이터를 편집한 후 줄 바꿈을 조심스럽게 제거하고 편집된 데이터를 `bundle_values` 열에 다시 붙여 넣습니다.

   다음 그림에서는 각 요가 스트랩에 `position=[number]` 매개 변수가 추가되어 스토어 목록에 있는 항목의 순서를 변경합니다.

   ![위치 매개 변수](./assets/product-bundle-values-position-parameter.png){width="500" zoomable="yes"}

1. 데이터를 편집한 후 CSV 파일을 **[!UICONTROL Save]**&#x200B;합니다.

#### 3단계: 업데이트된 제품 가져오기

1. _관리자_ 사이드바에서 **[!UICONTROL System]** > _[!UICONTROL Data Transfer]_>**[!UICONTROL Import]**(으)로 이동합니다.

1. _[!UICONTROL Import Settings]_&#x200B;에서&#x200B;**[!UICONTROL Entity Type]**&#x200B;을(를) `Products`(으)로 설정합니다.

1. **[!UICONTROL Import Behavior]**&#x200B;을(를) `Replace`(으)로 설정합니다.

   이 옵션은 변경 사항을 추가 항목으로 추가하지 않고 번들 제품에 대한 이전 데이터를 덮어씁니다.

1. _가져올 파일_ 섹션까지 아래로 스크롤한 다음 **[!UICONTROL Choose File]**&#x200B;을(를) 클릭합니다.

1. 편집한 CSV 파일을 선택합니다.

1. **[!UICONTROL Check Data]**&#x200B;을(를) 클릭하고 데이터를 확인할 때까지 잠시 기다립니다.

1. 파일이 올바른 경우 **[!UICONTROL Import]**&#x200B;을(를) 클릭합니다.

1. 프로세스가 완료되면 **[!UICONTROL System]** > _[!UICONTROL Tools]_>**[!UICONTROL Cache Management]**(으)로 이동하여&#x200B;**[!UICONTROL Flush Cache Storage]**&#x200B;을(를) 클릭합니다.

   이렇게 하면 업데이트된 제품을 매장 전면에서 즉시 사용할 수 있습니다.
