---
title: 위쪽 탐색
description: 서로 다른 부서에 대한 디렉터리와 같은 기능을 하는 저장소의 기본 메뉴를 정의하는 방법을 알아봅니다.
exl-id: 8b71fe73-2716-4820-9e57-4cb1e6888132
feature: Catalog Management, Categories, Site Navigation
source-git-commit: 01148770946a236ece2122be5a88b963a0f07d1f
workflow-type: tm+mt
source-wordcount: '569'
ht-degree: 0%

---

# 위쪽 탐색

스토어의 메인 메뉴는 스토어의 다른 부서로 연결되는 디렉토리와 같습니다. 각 옵션은 다른 제품 카테고리를 나타냅니다. 상단 탐색의 위치와 프레젠테이션은 테마별로 다를 수 있지만 작동 방식은 본질적으로 동일합니다.

![위쪽 탐색](./assets/storefront-top-navigation.png){width="700" zoomable="yes"}

카탈로그의 범주 구조는 검색 엔진이 사이트를 얼마나 잘 인덱싱하는지에 영향을 줄 수 있습니다. 카테고리가 더 깊이 중첩될수록 철저하게 색인화될 가능성이 줄어듭니다. 일반적으로 1개~3개의 표시 수준을 사용하는 것이 가장 효과적입니다. 다음 [루트 범주](category-root.md) 는 메뉴에 나타나지 않지만 첫 번째 레벨로 계산됩니다. 위쪽 탐색에서 사용할 수 있는 최대 수준 수는 구성에 의해 결정됩니다. 또한 스토어 테마에서 지원하는 메뉴 수준의 수에 제한이 있을 수 있습니다. 예를 들어 샘플 Luma 테마는 루트를 포함하여 최대 5개의 수준을 지원합니다.

## 메뉴 레벨 계산

| 항목 | 설명 |
|--- |--- |
| 레벨 1 | 첫 번째 수준은 루트 카테고리이며 샘플 데이터에서 이름이 &quot;기본 카테고리&quot;입니다. 루트는 메뉴의 컨테이너이며, 그 이름은 메뉴에 옵션으로 나타나지 않습니다. |
| 레벨 2 | 데스크탑 디스플레이에서 상단 탐색은 페이지 상단에 표시되는 기본 메뉴입니다. 모바일 디바이스에서 메인 메뉴는 일반적으로 옵션의 플라이아웃 메뉴로 표시됩니다. Luma 스토어의 두 번째 수준 옵션은 다음과 같습니다 _새로운 기능_, _여성_, _남성_, _톱니바퀴_, _교육_, 및 _판매_. |
| 레벨 3 | 세 번째 수준은 각 기본 메뉴 옵션 아래에 나타납니다. 예, 다음 _여성_, 세 번째 수준 옵션은 다음과 같습니다 _탑스_ 및 _하단_. |
| 레벨 4 | 네 번째 수준 옵션은 세 번째 수준 옵션에서 날아오는 하위 범주입니다. 예, 다음 _탑스_&#x200B;네 번째 수준 메뉴 옵션은 다음과 같습니다 _재킷_, _후디 &amp; 스웨트 셔츠_, _티_, 및 _브래스 앤 탱크_. |

{style="table-layout:auto"}

## 위쪽 탐색 설정

스토어의 위쪽 탐색에 범주가 나타나게 하려면 다음 단계를 완료하십시오.

### 1단계: 범주 만들기

1. 다음에서 _관리자_ 사이드바, 이동 **[!UICONTROL Catalog]** > **[!UICONTROL Categories]**.

1. 설정 **[!UICONTROL Store View]** 을 클릭하여 새 카테고리를 사용할 수 있는 위치를 결정합니다.

1. 범주 트리에서 새 범주의 상위 범주를 선택합니다.

   데이터 없이 처음부터 시작하는 경우 목록에 두 개의 카테고리만 있을 수 있습니다. _기본 범주_, 루트 및 _예제 카테고리_.

1. 클릭 **[!UICONTROL Add Subcategory]**.

1. 다음 설정으로 기본 정보를 작성합니다.

   - **[!UICONTROL Enable Category]** 을 로 설정 `Yes`
   - **[!UICONTROL Include in Menu]** 을 로 설정 `Yes`

1. 디스플레이 설정 집합에서 **[!UICONTROL Anchor]** 끝 `Yes`.

1. 기타 모든 필수 사항 완료 [범주 설정](category-create.md).

1. 완료되면 다음을 클릭하십시오. **[!UICONTROL Save]**.

다중 스토어 설치의 경우 다른 메인 메뉴를 로 할당할 수 있습니다. [루트 범주](category-root.md) 각 [스토어](../stores-purchase/stores.md#add-stores).

### 2단계: 위쪽 탐색의 깊이 설정

1. 다음에서 _관리자_ 사이드바, 이동 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. 왼쪽 패널에서 를 확장합니다. **[!UICONTROL Catalog]** 및 선택 **[!UICONTROL Catalog]** 밑에.

1. 확장 **[!UICONTROL Category Top Navigation]** 섹션.

   ![범주 위쪽 탐색](../configuration-reference/catalog/assets/catalog-category-top-navigation.png){width="600" zoomable="yes"}

   상단 탐색의 깊이가 전역 속성을 갖기 때문입니다. [구성 범위](../getting-started/websites-stores-views.md#scope-settings), 설정은 Commerce 설치의 모든 웹 사이트, 스토어 및 스토어 보기에 적용됩니다. 다음 _[!UICONTROL Category Top Navigation]_구성 섹션은 다음과 같은 경우에만 사용할 수 있습니다._[!UICONTROL Store View]_ 왼쪽 상단 모서리에서 을(를) (으)로 설정합니다. `Default Config`.

   이러한 옵션에 대한 자세한 목록은 다음을 참조하십시오. [범주 위쪽 탐색](../configuration-reference/catalog/catalog.md#layered-navigation) 다음에서 _구성 참조_.

1. 위쪽 탐색에 나타나는 하위 범주의 수를 제한하려면 다음 숫자를 입력합니다. **[!UICONTROL Maximal Depth]**.

   기본값은 입니다. `0`(하위 범주 수준의 수에 제한을 두지 않음)

1. 완료되면 다음을 클릭하십시오. **[!UICONTROL Save Config]**.
