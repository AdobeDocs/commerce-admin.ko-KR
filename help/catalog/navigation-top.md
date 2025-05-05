---
title: 위쪽 탐색
description: 서로 다른 부서에 대한 디렉터리와 같은 기능을 하는 저장소의 기본 메뉴를 정의하는 방법을 알아봅니다.
exl-id: 8b71fe73-2716-4820-9e57-4cb1e6888132
feature: Catalog Management, Categories, Site Navigation
source-git-commit: 01148770946a236ece2122be5a88b963a0f07d1f
workflow-type: tm+mt
source-wordcount: '575'
ht-degree: 0%

---

# 위쪽 탐색

스토어의 메인 메뉴는 스토어의 다른 부서로 연결되는 디렉토리와 같습니다. 각 옵션은 다른 제품 카테고리를 나타냅니다. 상단 탐색의 위치와 프레젠테이션은 테마별로 다를 수 있지만 작동 방식은 본질적으로 동일합니다.

![위쪽 탐색](./assets/storefront-top-navigation.png){width="700" zoomable="yes"}

카탈로그의 범주 구조는 검색 엔진이 사이트를 얼마나 잘 인덱싱하는지에 영향을 줄 수 있습니다. 카테고리가 더 깊이 중첩될수록 철저하게 색인화될 가능성이 줄어듭니다. 일반적으로 1개~3개의 표시 수준을 사용하는 것이 가장 효과적입니다. [루트 범주](category-root.md)은 메뉴에 나타나지 않지만 첫 번째 수준으로 계산됩니다. 위쪽 탐색에서 사용할 수 있는 최대 수준 수는 구성에 의해 결정됩니다. 또한 스토어 테마에서 지원하는 메뉴 수준의 수에 제한이 있을 수 있습니다. 예를 들어 샘플 Luma 테마는 루트를 포함하여 최대 5개의 수준을 지원합니다.

## 메뉴 레벨 계산

| 항목 | 설명 |
|--- |--- |
| 레벨 1 | 첫 번째 수준은 루트 카테고리이며 샘플 데이터에서 이름이 &quot;기본 카테고리&quot;입니다. 루트는 메뉴의 컨테이너이며, 그 이름은 메뉴에 옵션으로 나타나지 않습니다. |
| 레벨 2 | 데스크탑 디스플레이에서 상단 탐색은 페이지 상단에 표시되는 기본 메뉴입니다. 모바일 디바이스에서 메인 메뉴는 일반적으로 옵션의 플라이아웃 메뉴로 표시됩니다. Luma 스토어의 두 번째 수준 옵션은 _새로운 기능_, _여성_, _남성_, _기어_, _교육_ 및 _판매_&#x200B;입니다. |
| 레벨 3 | 세 번째 수준은 각 기본 메뉴 옵션 아래에 나타납니다. 예를 들어 _여성_&#x200B;에서 세 번째 수준의 옵션은 _위쪽_ 및 _아래쪽_&#x200B;입니다. |
| 레벨 4 | 네 번째 수준 옵션은 세 번째 수준 옵션에서 날아오는 하위 범주입니다. 예를 들어, _Tops_&#x200B;에서 네 번째 수준 메뉴 옵션은 _재킷_, _후드 및 운동복_, _티_, _브라와 탱크_&#x200B;입니다. |

{style="table-layout:auto"}

## 위쪽 탐색 설정

스토어의 위쪽 탐색에 범주가 나타나게 하려면 다음 단계를 완료하십시오.

### 1단계: 범주 만들기

1. _관리자_ 사이드바에서 **[!UICONTROL Catalog]** > **[!UICONTROL Categories]**(으)로 이동합니다.

1. 새 범주를 사용할 수 있는 위치를 확인하려면 **[!UICONTROL Store View]**&#x200B;을(를) 설정하십시오.

1. 범주 트리에서 새 범주의 상위 범주를 선택합니다.

   데이터 없이 처음부터 시작하는 경우 목록에 루트인 _기본 범주_&#x200B;와 _예제 범주_&#x200B;의 두 가지 범주만 있을 수 있습니다.

1. **[!UICONTROL Add Subcategory]**&#x200B;을(를) 클릭합니다.

1. 다음 설정으로 기본 정보를 작성합니다.

   - **[!UICONTROL Enable Category]**&#x200B;이(가) `Yes`(으)로 설정됨
   - **[!UICONTROL Include in Menu]**&#x200B;이(가) `Yes`(으)로 설정됨

1. 디스플레이 설정에서 **[!UICONTROL Anchor]**&#x200B;을(를) `Yes`(으)로 설정했습니다.

1. 다른 필수 [범주 설정](category-create.md)을 완료합니다.

1. 완료되면 **[!UICONTROL Save]**&#x200B;을(를) 클릭합니다.

다중 스토어 설치의 경우 각 [스토어](../stores-purchase/stores.md#add-stores)에 대해 다른 기본 메뉴를 [루트 범주](category-root.md)(으)로 할당할 수 있습니다.

### 2단계: 위쪽 탐색의 깊이 설정

1. _관리자_ 사이드바에서 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**(으)로 이동합니다.

1. 왼쪽 패널에서 **[!UICONTROL Catalog]**&#x200B;을(를) 확장하고 아래의 **[!UICONTROL Catalog]**&#x200B;을(를) 선택합니다.

1. **[!UICONTROL Category Top Navigation]** 섹션을 확장합니다.

   ![범주 위쪽 탐색](../configuration-reference/catalog/assets/catalog-category-top-navigation.png){width="600" zoomable="yes"}

   위쪽 탐색의 깊이에 전역 [구성 범위](../getting-started/websites-stores-views.md#scope-settings)가 있으므로 이 설정은 Commerce 설치의 모든 웹 사이트, 스토어 및 스토어 보기에 적용됩니다. _[!UICONTROL Category Top Navigation]_&#x200B;구성 섹션은 왼쪽 상단의&#x200B;_[!UICONTROL Store View]_&#x200B;이(가) `Default Config`(으)로 설정된 경우에만 사용할 수 있습니다.

   이러한 옵션에 대한 자세한 목록이 필요하면 _구성 참조_&#x200B;에서 [범주 위쪽 탐색](../configuration-reference/catalog/catalog.md#layered-navigation)을 참조하십시오.

1. 위쪽 탐색에 나타나는 하위 범주의 수를 제한하려면 **[!UICONTROL Maximal Depth]**&#x200B;의 숫자를 입력하십시오.

   기본값은 `0`이며, 이 값은 하위 범주 수준의 수에 제한을 두지 않습니다.

1. 완료되면 **[!UICONTROL Save Config]**&#x200B;을(를) 클릭합니다.
