---
title: 위젯을 사용하여 블록 배치
description: 정적 블록 위젯을 사용하여 기존 컨텐츠를 스토어 내 어디에나 배치하는 방법에 대해 알아봅니다.
exl-id: 174deef2-33c4-4f1a-8ca8-4969be209bc7
source-git-commit: b659c7e1e8f2ae9883f1e24d8045d6dd1e90cfc0
workflow-type: tm+mt
source-wordcount: '566'
ht-degree: 0%

---

# 위젯을 사용하여 블록 배치

다음 _CMS 정적 블록_ [위젯](widgets.md) 은(는) 기존 을(를) 배치하는 기능을 제공합니다. [콘텐츠 차단](blocks.md) 가게 어디에나 있습니다.

![위젯](./assets/widgets.png){width="700" zoomable="yes"}

## 1단계: 위젯 유형 선택

1. 다음에서 _관리자_ 사이드바, 이동 **[!UICONTROL Content]** > _[!UICONTROL Elements]_>**[!UICONTROL Widgets]**.

1. 오른쪽 위 모서리에서 을(를) 클릭합니다. **[!UICONTROL Add Widget]**.

1. 다음에서 _설정_ 섹션, 설정 **[!UICONTROL Type]** 끝 `CMS Static Block` 및 클릭 **[!UICONTROL Continue]**.

1. 다음을 확인합니다 **[!UICONTROL Design Theme]** 이 현재 테마로 설정되어 있습니다. **[!UICONTROL Continue]**.

   ![위젯 설정](./assets/widget-settings.png){width="600" zoomable="yes"}

1. 다음에서 _[!UICONTROL Storefront Properties]_섹션에서 다음을 수행합니다.

   - 대상 **[!UICONTROL Widget Title]**&#x200B;을 클릭하고 위젯에 대한 설명 제목을 입력합니다.

     이 제목은 _관리자_.

   - 대상 **[!UICONTROL Assign to Store Views]**&#x200B;위젯이 표시되는 스토어 보기를 선택합니다.

     특정 스토어 보기를 선택하거나 `All Store Views`. 여러 뷰를 선택하려면 Ctrl 키(PC) 또는 Command 키(Mac)를 누른 상태에서 각 옵션을 클릭합니다.

   - (선택 사항) **[!UICONTROL Sort Order]**&#x200B;을 클릭하고, 페이지의 같은 부분에서 이 항목이 다른 항목과 함께 표시되는 순서를 결정하는 숫자를 입력합니다. (`0` = 첫 번째, `1` = 초, `3` = 세 번째 등입니다.)

     ![Storefront 속성](./assets/widget-storefront-properties.png){width="600" zoomable="yes"}

## 2단계: 위젯 레이아웃 업데이트 완료

1. 다음에서 _[!UICONTROL Layout Updates]_섹션, 클릭&#x200B;**[!UICONTROL Add Layout Update]**.

1. 설정 **[!UICONTROL Display On]** 블록을 표시할 카테고리, 제품 또는 페이지로 이동합니다.

1. 특정 페이지에 블록을 배치하려면 다음 작업을 수행하십시오.

   - 다음을 선택합니다. **[!UICONTROL Page]** 블록을 표시할 위치입니다.

   - 다음을 선택합니다. **[!UICONTROL Block Reference]** 블록을 페이지에서 표시하는 위치를 식별합니다.

   - 의 기본 설정 적용 **[!UICONTROL Template]**, 로 설정되어 있습니다. `CMS Static Block Default Template`.

     ![레이아웃 업데이트](./assets/widget-layout-update-home-page.png){width="600" zoomable="yes"}

### 레이아웃 업데이트 옵션

| 필드 | 설명 |
|--- |--- |
| **_[!UICONTROL Categories]_** |  |
| [!UICONTROL Anchor Categories] | 앵커 범주 페이지에 위젯을 표시합니다.<br/>**[!UICONTROL Categories]**- 앵커가 표시되는 카테고리입니다. 옵션: `All` /`Specific Categories`<br/>**[!UICONTROL Container]** - 컨테이너를 위젯을 표시할 페이지 레이아웃의 일부로 설정합니다.<br/>**[!UICONTROL Template]**- 레이아웃의 테마를 결정합니다. |
| [!UICONTROL Non-Anchor Categories] | 비앵커 카테고리 페이지에 위젯을 표시합니다.<br/>**[!UICONTROL Categories]**- 앵커가 표시되는 카테고리입니다. 옵션: `All` /`Specific Categories`<br/>**[!UICONTROL Container]** - 컨테이너를 위젯을 표시할 페이지 레이아웃의 일부로 설정합니다.<br/>**[!UICONTROL Template]**- 레이아웃의 테마를 결정합니다. |
| **_[!UICONTROL Products]_** |  |
| 모든 제품 유형 | 특정 유형의 제품 페이지나 모든 제품 페이지에서 위젯을 표시합니다. <br/>**[!UICONTROL Products]**- 위젯이 표시되는 제품. 옵션: `All` /` Specific Products`<br/>**[!UICONTROL Container]** - 컨테이너를 위젯을 표시할 페이지 레이아웃의 일부로 설정합니다.<br/>**[!UICONTROL Template]**- 레이아웃의 테마를 결정합니다. |
| **_[!UICONTROL Generic Pages]_** |  |
| [!UICONTROL All Pages] | 모든 페이지에 위젯을 표시합니다. <br/>**[!UICONTROL Container]**- 컨테이너를 위젯을 표시할 페이지 레이아웃의 일부로 설정합니다.<br/>**[!UICONTROL Template]** - 레이아웃의 테마를 결정합니다. |
| [!UICONTROL Specified Page] | 특정 페이지에 위젯을 표시합니다. 옵션:<br/>**[!UICONTROL Page]**- 위젯이 표시되는 페이지입니다.<br/>**[!UICONTROL Container]** - 컨테이너를 위젯을 표시할 페이지 레이아웃의 일부로 설정합니다.<br/>**템플릿** - 레이아웃의 테마를 결정합니다. |
| [!UICONTROL Page Layouts] | 특정 레이아웃으로 페이지에 위젯을 표시합니다. <br/>**[!UICONTROL Page]**- 위젯이 표시되는 페이지입니다.<br/>**[!UICONTROL Container]** - 컨테이너를 위젯을 표시할 페이지 레이아웃의 일부로 설정합니다.<br/>**[!UICONTROL Template]**- 레이아웃의 테마를 결정합니다. |

{style="table-layout:auto"}

## 3단계: 블록 배치

1. 왼쪽 패널에서 을 선택합니다 **[!UICONTROL Widget Options]**.

1. 클릭 **[!UICONTROL Select Block…]** 목록에서 배치할 블록을 선택합니다.

1. 완료되면 다음을 클릭하십시오. **[!UICONTROL Save]**.

   이제 앱이 목록에 표시됩니다.

1. 메시지가 표시되면 페이지 상단에 있는 지침에 따라 인덱스와 페이지 캐시를 업데이트합니다.

1. 상점으로 돌아가서 블록이 올바른 위치에 표시되는지 확인하십시오.

   블록을 이동하려면 위젯을 다시 열거나 다른 페이지나 블록 참조를 시도할 수 있습니다.
