---
title: 새 제품 목록 위젯
description: 새 제품 목록 위젯을 사용하여 가장 최근에 추가된 제품 목록을 표시하는 방법에 대해 알아봅니다.
exl-id: bdff3655-cd14-4a19-a51f-4cabeb274d2a
feature: Page Content, Products
source-git-commit: b659c7e1e8f2ae9883f1e24d8045d6dd1e90cfc0
workflow-type: tm+mt
source-wordcount: '602'
ht-degree: 0%

---

# 새 제품 목록 위젯

새 제품 목록은 다이내믹 컨텐츠의 예제이며 제품 카탈로그에서 가져오는 라이브 데이터로 구성됩니다. 기본적으로 _새 제품_ 목록에는 가장 최근에 추가된 제품 중 처음 8개가 포함됩니다. 그러나 지정된 날짜 범위 내의 제품만 포함하도록 구성할 수도 있습니다.

![상점 첫 화면 홈 페이지의 새 제품 목록](./assets/storefront-home-page-new-products.png){width="700" zoomable="yes"}

## 1단계: 각 제품을 새 제품으로 설정

![Magento Open Source](../assets/open-source.svg) 이 단계는 Magento Open Source 에만 적용됩니다.

![Adobe Commerce](../assets/adobe-logo.svg) Adobe Commerce 스토어의 경우 [업데이트 예약](content-staging-scheduled-update.md) 그런 다음 이 페이지의 2단계로 진행합니다.

_[!UICONTROL Set Product as New]_날짜 범위 설정은 예약된 업데이트에서만 구성할 수 있습니다.

제품을 새 제품으로 설정하면 다음이 추가됩니다. _새 제품_ 목록을 표시합니다. 목록에 더 이상 포함하지 않으려는 경우 언제든지 설정을 다시 변경할 수 있습니다.

1. 다음에서 _관리자_ 사이드바, 이동 **[!UICONTROL Catalog]** > **[!UICONTROL Products]**.

1. 기능을 사용할 각 제품을 찾아 편집 모드로 엽니다.

1. 대상 **[!UICONTROL Set Product as New]**&#x200B;옵션을 전환하여 제품을 새 제품으로 설정할지 여부를 지정합니다.

   ![제품을 새 제품으로 설정](./assets/product-set-as-new.png){width="400" zoomable="yes"}

1. 완료되면 다음을 클릭하십시오. **[!UICONTROL Save]**.

1. 페이지 캐시를 다시 인덱싱하고 새로 고치라는 메시지가 표시되면 페이지 상단에 있는 링크를 클릭하고 지침을 따릅니다.

## 2단계: 위젯 만들기

새 제품 목록의 콘텐츠와 스토어에서의 배치를 결정하는 코드는 위젯 도구를 통해 생성됩니다.

1. 다음에서 _관리자_ 사이드바, 이동 **[!UICONTROL Content]** > _[!UICONTROL Elements]_>**[!UICONTROL Widgets]**.

1. 오른쪽 위 모서리에서 을(를) 클릭합니다. **[!UICONTROL Add Widget]**.

1. 다음에서 _[!UICONTROL Settings]_섹션에서 다음을 수행합니다.

   - 설정 **[!UICONTROL Type]** 끝 `Catalog New Products List`.

   - 다음을 선택합니다. **[!UICONTROL Design Theme]** 그것은 상점에서 사용하는 것입니다.

1. 클릭 **[!UICONTROL Continue]**.

   ![새 제품 목록 위젯 설정](./assets/widget-settings.png){width="600" zoomable="yes"}

1. 다음에서 _[!UICONTROL Storefront Properties]_섹션에서 다음을 수행합니다.

   - 대상 **[!UICONTROL Widget Title]**&#x200B;을 클릭하고 위젯에 대한 설명 제목을 입력합니다. (이 제목은 _관리자_.)

   - 대상 **[!UICONTROL Assign to Store Views]**&#x200B;위젯이 표시되는 스토어 보기를 선택합니다.

     특정 스토어 보기를 선택하거나 `All Store Views`. 여러 뷰를 선택하려면 Ctrl 키(PC) 또는 Command 키(Mac)를 누른 상태에서 각 옵션을 클릭합니다.

   - (선택 사항) **[!UICONTROL Sort Order]**&#x200B;을 클릭하고, 페이지의 같은 부분에서 이 항목이 다른 항목과 함께 표시되는 순서를 결정하는 숫자를 입력합니다. (`0` = 첫 번째, `1` = 초, `3` = 세 번째 등입니다.)

   ![레이아웃 업데이트](./assets/widget-layout-update-home-page.png){width="600" zoomable="yes"}

## 3단계: 위치 선택

1. 다음에서 _[!UICONTROL Layout Updates]_섹션, 클릭&#x200B;**[!UICONTROL Add Layout Update]**.

1. 설정 **[!UICONTROL Display On]** 끝 `Specified Page.`

1. 설정 **[!UICONTROL Page]** 끝 `CMS Home Page`.

1. 설정 **[!UICONTROL Block Reference]** 끝 `Main Content Area`.

1. 설정 **[!UICONTROL Template]** 다음 중 하나를 수행합니다.

   - `New Product List Template`
   - `New Products Grid Template`

     ![레이아웃 업데이트](./assets/widget-layout-update-new-products-list.png){width="600" zoomable="yes"}

1. 클릭 **[!UICONTROL Save and Continue Edit]**.

   지금은 메시지를 무시하여 캐시를 새로 고칠 수 있습니다.

## 4단계: 목록 구성

1. 왼쪽 패널에서 을 선택합니다 **[!UICONTROL Widget Options]**.

1. 설정 **[!UICONTROL Display Products]** 다음 중 하나를 수행합니다.

   - `All Products` - 가장 최근에 추가된 항목부터 시작하여 제품을 순서대로 나열합니다.
   - `New Products` - (으)로 식별된 제품만 나열합니다. _신규_. 제품은에 지정된 날짜 범위 동안 새 것으로 간주됩니다. _[!UICONTROL Set Product As New From/To]_. 새 제품을 정의하지 않고 날짜 범위가 만료되면 목록이 비어 있습니다.

1. 여러 페이지가 있는 목록에 탐색 컨트롤을 제공하려면 다음을 설정하십시오. **[!UICONTROL Display Page Control]** 끝 `Yes`.

   대상 **[!UICONTROL Number of Products per Page]**&#x200B;각 페이지에 표시할 제품 수를 입력합니다.

1. 설정 **[!UICONTROL Number of Products to Display]** 목록에 포함할 새 제품 수에 대한 옵션입니다.

   기본 설정은 다음과 같습니다. `10`.

1. 대상 **[!UICONTROL Cache Lifetime (Seconds)]**&#x200B;를 클릭하고 새 제품 목록을 새로 고치는 빈도를 선택합니다.

   기본적으로 캐시는 86,400초(24시간)로 설정됩니다.

   ![위젯 옵션](./assets/widget-options-new-product-list.png){width="600" zoomable="yes"}

1. 완료되면 다음을 클릭하십시오. **[!UICONTROL Save]**.

1. 캐시를 새로 고치라는 메시지가 표시되면 페이지 상단에 있는 메시지에서 링크를 클릭하고 지침을 따릅니다.

## 5단계: 작업 미리보기

1. 다음에서 _관리자_ 사이드바, 이동 **[!UICONTROL Content]** > _[!UICONTROL Elements]_>**[!UICONTROL Pages]**.

1. 다음 위치에 있는 표에서 페이지 찾기 _새 제품_ 목록이 나타나고 **[!UICONTROL Preview]** 링크 _[!UICONTROL Action]_열.
