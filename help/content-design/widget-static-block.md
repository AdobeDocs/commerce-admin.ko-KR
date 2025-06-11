---
title: 위젯을 사용하여 블록 배치
description: 정적 블록 위젯을 사용하여 기존 컨텐츠를 스토어 내 어디에나 배치하는 방법에 대해 알아봅니다.
exl-id: 174deef2-33c4-4f1a-8ca8-4969be209bc7
badgePaas: label="PaaS만" type="Informative" url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="Adobe Commerce 온 클라우드 프로젝트(Adobe 관리 PaaS 인프라) 및 온프레미스 프로젝트에만 적용됩니다."
source-git-commit: 57a913b21f4cbbb4f0800afe13012ff46d578f8e
workflow-type: tm+mt
source-wordcount: '586'
ht-degree: 0%

---

# 위젯을 사용하여 블록 배치

_CMS 정적 블록_ [위젯](widgets.md)을(를) 사용하면 기존 [콘텐츠 블록](blocks.md)을(를) 저장소의 어디에나 배치할 수 있습니다.

![위젯](./assets/widgets.png){width="700" zoomable="yes"}

## 1단계: 위젯 유형 선택

1. _관리자_ 사이드바에서 **[!UICONTROL Content]** > _[!UICONTROL Elements]_>**[!UICONTROL Widgets]**(으)로 이동합니다.

1. 오른쪽 상단에서 **[!UICONTROL Add Widget]**&#x200B;을(를) 클릭합니다.

1. _설정_ 섹션에서 **[!UICONTROL Type]**&#x200B;을(를) `CMS Static Block`(으)로 설정하고 **[!UICONTROL Continue]**&#x200B;을(를) 클릭합니다.

1. **[!UICONTROL Design Theme]**&#x200B;이(가) 현재 테마로 설정되어 있는지 확인하고 **[!UICONTROL Continue]**&#x200B;을(를) 클릭합니다.

   ![위젯 설정](./assets/widget-settings.png){width="600" zoomable="yes"}

1. _[!UICONTROL Storefront Properties]_&#x200B;섹션에서 다음을 수행합니다.

   - **[!UICONTROL Widget Title]**&#x200B;의 경우 위젯에 대한 설명 제목을 입력합니다.

     이 제목은 _관리자_&#x200B;에서만 볼 수 있습니다.

   - **[!UICONTROL Assign to Store Views]**&#x200B;의 경우 위젯이 표시되는 스토어 보기를 선택하십시오.

     특정 스토어 보기 또는 `All Store Views`을(를) 선택할 수 있습니다. 여러 뷰를 선택하려면 Ctrl 키(PC) 또는 Command 키(Mac)를 누른 상태에서 각 옵션을 클릭합니다.

   - (선택 사항) **[!UICONTROL Sort Order]**&#x200B;의 경우 숫자를 입력하여 이 항목이 페이지의 동일한 부분에 있는 다른 항목과 함께 표시되는 순서를 결정합니다. (`0` = 첫 번째, `1` = 두 번째, `3` = 세 번째 등)

     ![Storefront 속성](./assets/widget-storefront-properties.png){width="600" zoomable="yes"}

## 2단계: 위젯 레이아웃 업데이트 완료

1. _[!UICONTROL Layout Updates]_&#x200B;섹션에서&#x200B;**[!UICONTROL Add Layout Update]**&#x200B;을(를) 클릭합니다.

1. 블록을 표시할 범주, 제품 또는 페이지로 **[!UICONTROL Display On]**&#x200B;을(를) 설정합니다.

1. 특정 페이지에 블록을 배치하려면 다음 작업을 수행하십시오.

   - 블록을 표시할 **[!UICONTROL Page]**&#x200B;을(를) 선택하십시오.

   - 페이지에서 블록이 표시되는 위치를 식별하는 **[!UICONTROL Block Reference]**&#x200B;을(를) 선택합니다.

   - `CMS Static Block Default Template`(으)로 설정된 **[!UICONTROL Template]**&#x200B;에 대한 기본 설정을 적용합니다.

     ![레이아웃 업데이트](./assets/widget-layout-update-home-page.png){width="600" zoomable="yes"}

### 레이아웃 업데이트 옵션

| 필드 | 설명 |
|--- |--- |
| **_[!UICONTROL Categories]_** |  |
| [!UICONTROL Anchor Categories] | 앵커 범주 페이지에 위젯을 표시합니다.<br/>**[!UICONTROL Categories]**- 앵커가 표시되는 범주. 옵션: `All` /`Specific Categories`<br/>**[!UICONTROL Container]** - 컨테이너를 위젯을 표시할 페이지 레이아웃의 일부로 설정합니다.<br/>**[!UICONTROL Template]**- 레이아웃의 테마를 결정합니다. |
| [!UICONTROL Non-Anchor Categories] | 비앵커 카테고리 페이지에 위젯을 표시합니다.<br/>**[!UICONTROL Categories]**- 앵커가 표시되는 범주. 옵션: `All` /`Specific Categories`<br/>**[!UICONTROL Container]** - 컨테이너를 위젯을 표시할 페이지 레이아웃의 일부로 설정합니다.<br/>**[!UICONTROL Template]**- 레이아웃의 테마를 결정합니다. |
| **_[!UICONTROL Products]_** |  |
| 모든 제품 유형 | 특정 유형의 제품 페이지나 모든 제품 페이지에서 위젯을 표시합니다. <br/>**[!UICONTROL Products]**- 위젯이 표시되는 제품입니다. 옵션: `All` /` Specific Products`<br/>**[!UICONTROL Container]** - 컨테이너를 위젯을 표시할 페이지 레이아웃의 일부로 설정합니다.<br/>**[!UICONTROL Template]**- 레이아웃의 테마를 결정합니다. |
| **_[!UICONTROL Generic Pages]_** |  |
| [!UICONTROL All Pages] | 모든 페이지에 위젯을 표시합니다. <br/>**[!UICONTROL Container]**- 컨테이너를 위젯을 표시할 페이지 레이아웃의 일부로 설정합니다.<br/>**[!UICONTROL Template]** - 레이아웃의 테마를 결정합니다. |
| [!UICONTROL Specified Page] | 특정 페이지에 위젯을 표시합니다. 옵션:<br/>**[!UICONTROL Page]**- 위젯이 표시되는 페이지입니다.<br/>**[!UICONTROL Container]** - 컨테이너를 위젯을 표시할 페이지 레이아웃의 일부로 설정합니다.<br/>**템플릿** - 레이아웃의 테마를 결정합니다. |
| [!UICONTROL Page Layouts] | 특정 레이아웃으로 페이지에 위젯을 표시합니다. <br/>**[!UICONTROL Page]**- 위젯이 표시되는 페이지입니다.<br/>**[!UICONTROL Container]** - 컨테이너를 위젯을 표시할 페이지 레이아웃의 일부로 설정합니다.<br/>**[!UICONTROL Template]**- 레이아웃의 테마를 결정합니다. |

{style="table-layout:auto"}

## 3단계: 블록 배치

1. 왼쪽 패널에서 **[!UICONTROL Widget Options]**&#x200B;을(를) 선택합니다.

1. **[!UICONTROL Select Block…]**&#x200B;을(를) 클릭하고 목록에서 배치할 블록을 선택합니다.

1. 완료되면 **[!UICONTROL Save]**&#x200B;을(를) 클릭합니다.

   이제 앱이 목록에 표시됩니다.

1. 메시지가 표시되면 페이지 상단에 있는 지침에 따라 인덱스와 페이지 캐시를 업데이트합니다.

1. 상점으로 돌아가서 블록이 올바른 위치에 표시되는지 확인하십시오.

   블록을 이동하려면 위젯을 다시 열거나 다른 페이지나 블록 참조를 시도할 수 있습니다.
