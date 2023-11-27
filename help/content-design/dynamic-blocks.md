---
title: 동적 블록
description: 다이내믹 블록을 사용하여 가격 규칙 및 고객 세그먼트의 논리를 기반으로 하는 풍부한 대화형 컨텐츠를 생성합니다.
exl-id: 0c842ad9-2e46-48aa-9a12-2f74a54c352e
source-git-commit: b659c7e1e8f2ae9883f1e24d8045d6dd1e90cfc0
workflow-type: tm+mt
source-wordcount: '629'
ht-degree: 0%

---

# 동적 블록

{{ee-feature}}

에서 논리에 의해 유도된 풍부한 대화형 콘텐츠 만들기 [가격 규칙](../merchandising-promotions/introduction.md#price-rules) 및 [고객 세그먼트](../customers/customer-segments.md). 기존 항목 [동적 블록](../page-builder/dynamic-block.md) 에 바로 추가할 수 있습니다. [!DNL Page Builder] [단계](../page-builder/workspace.md). 동적 블록 사용에 대한 자세한 단계별 예제는 을 참조하십시오. [자습서 2: 블록](../page-builder/2-blocks.md).

>[!NOTE]
>
>다음 _[!UICONTROL Banner]_의 옵션 [[!UICONTROL Content] 메뉴](content-menu.md) 는 2.3.1에서 더 이상 사용되지 않으며 2.4.0에서 제거되었습니다. 이 기능은 동적 블록으로 대체됩니다.

![[!DNL Page Builder] - 가격 규칙 및 고객 세그먼트를 포함하는 동적 블록](../page-builder/assets/pb-tutorial2-dynamic-block-storefront.png){width="600" zoomable="yes"}

## 1단계: 동적 블록 만들기

1. 다음에서 _관리자_ 사이드바, 이동 **[!UICONTROL Content]** > _[!UICONTROL Elements]_>**[!UICONTROL Dynamic Blocks]**.

   ![동적 블록 목록](../page-builder/assets/pb-tutorial2-block-dynamic-add.png){width="600" zoomable="yes"}

1. 오른쪽 위 모서리에서 을(를) 클릭합니다. **[!UICONTROL Add Dynamic Block]**.

   ![새 동적 블록](../page-builder/assets/pb-tutorial2-block-dynamic-new.png){width="600" zoomable="yes"}

1. 해당하는 경우 다음을 설정합니다. **[!UICONTROL Store View]** 동적 블록이 표시될 특정 스토어 뷰를 표시합니다.

1. 동적 블록을 활성화하려면 다음을 설정합니다. **[!UICONTROL Enable Dynamic Block]** 끝 `Yes`.

1. 내부 참조에 설명을 입력합니다 **[!UICONTROL Dynamic Block Name]**.

1. 설정 **[!UICONTROL Dynamic Block Type]** 동적 블록을 표시할 페이지 영역으로 이동하여 **[!UICONTROL Done]**.

   ![동적 블록 유형 설정](../page-builder/assets/pb-dynamic-block-type.png){width="500" zoomable="yes"}

1. 다음에서 **[!UICONTROL Customer Segment]** 목록에서 동적 블록을 보려는 각 세그먼트의 확인란을 선택하고 **[!UICONTROL Done]** 설정을 저장합니다.

   ![고객 세그먼트 선택](../page-builder/assets/pb-dynamic-block-customer-segment.png){width="500" zoomable="yes"}

   >[!NOTE]
   >
   >- 세그먼트가 만들어지지 않으면 동적 블록이 모든 사용자에게 표시됩니다.
   >- 고객이 어떤 세그먼트에도 속하지 않고 모든 세그먼트에 대해 동적 블록이 만들어지면 동적 블록의 내용이 계속 표시됩니다.
   >- 동적 블록에 할당된 모든 고객 세그먼트가 삭제되면 해당 콘텐츠가 모든 사용자에게 표시됩니다.

### 동적 블록에서 Real-Time CDP 대상 사용

다음을 수행하는 경우 [설치됨](../customers/audience-activation.md#install-the-extension) 및 [구성됨](../customers/audience-activation.md#configure-the-extension) 다음 [!DNL Audience Activation] 확장에는 라는 섹션이 표시됩니다. **[!UICONTROL Audiences]**.

![Real-Time CDP 대상 선택](./assets/dynamic-block-rtcdp.png){width="600" zoomable="yes"}

다음에서 **[!UICONTROL Real-Time CDP Audience]** 동적 블록을 보려는 각 대상의 확인란을 선택하고 을(를) 클릭합니다. **[!UICONTROL Done]** 설정을 저장합니다.

## 2단계: 콘텐츠 완료

사용 [!DNL Page Builder] [작업 영역](../page-builder/workspace.md) 콘텐츠를 작성합니다.

![[!DNL Page Builder] - 동적 블록 작업 영역](../page-builder/assets/pb-dynamic-block-workspace.png){width="600" zoomable="yes"}

## 3단계: 관련 판촉 선택

1. 아래로 스크롤하고 확장합니다. ![확장 선택기](../assets/icon-display-expand.png) **[!UICONTROL Related Promotions]**.

1. 동적 블록과 연결할 프로모션 유형을 클릭합니다.

   - **[!UICONTROL Add Cart Price Rules]** (참조 [장바구니 가격 규칙](../merchandising-promotions/price-rules-cart.md))

   - **[!UICONTROL Add Catalog Price Rules]** (참조 [카탈로그 가격 규칙](../merchandising-promotions/price-rules-catalog.md))

   >[!NOTE]
   >
   >Real-Time CDP 대상에 대해서는 카탈로그 가격 규칙이 지원되지 않습니다.

1. 사용 가능한 규칙 목록에서 사용할 각 규칙의 확인란을 선택하고 **[!UICONTROL Add Selected]**.

1. 동적 블록이 완료되면 을 클릭합니다. **[!UICONTROL Save]**.

## 4단계: 페이지에 동적 블록 추가

1. 동적 블록을 표시할 페이지를 엽니다.

1. 사용 [[!UICONTROL Add Dynamic Block]](../page-builder/dynamic-block.md) 스테이지에 동적 블록을 추가하는 콘텐츠 유형입니다.

## 필드 및 도구 설명

| 필드 | 설명 |
|--- |--- |
| [!UICONTROL Store View] | 동적 블록을 사용할 수 있는 저장소 보기를 지정합니다. |
| [!UICONTROL Enable Dynamic Block] | 동적 블록을 활성화하거나 비활성화합니다. 옵션: 예 / 아니요 |
| [!UICONTROL Dynamic Block Name] | 관리자의 동적 블록을 식별하는 수사적 이름입니다. |
| [!UICONTROL Dynamic Block Type] | 에서 위치 식별 [표준 페이지 레이아웃](layout-updates.md) 동적 블록이 배치된 위치입니다. 옵션: <br/>**[!UICONTROL Content Area]**- 동적 블록을 기본 블록에 배치합니다. [콘텐츠 영역](layout-updates.md) 페이지의 입니다.<br/>**[!UICONTROL Footer]** - 페이지에 동적 블록을 배치합니다. [꼬리말](page-setup.md#footer). <br/>**[!UICONTROL Header]**- 페이지에 동적 블록을 배치합니다. [머리글](page-setup.md#header).<br/>**[!UICONTROL Left Column]** - 동적 블록을 [왼쪽 사이드바](page-layout.md#standard-page-layouts) 2열 또는 3열 레이아웃 <br/>**[!UICONTROL Right Column]**- 동적 블록을 [오른쪽 사이드바](page-layout.md#standard-page-layouts) 2열 또는 3열 레이아웃 |
| 고객 세그먼트 | 고객 세그먼트를 동적 블록과 연결하여 볼 수 있는 고객을 결정합니다. |
| Real-Time CDP 대상 | Associates a [Real-Time CDP 대상](../customers/audience-activation.md) 동적 블록을 사용하여 어떤 고객이 볼 수 있는지 결정합니다. |

{style="table-layout:auto"}

### 내용

| 필드 | 설명 |
|--- |--- |
| [!UICONTROL Layout] | 단계에 행, 열 또는 탭을 추가합니다. |
| [!UICONTROL Elements] | 텍스트, 머리글, 단추, 분할자 및 HTML 코드를 스테이지의 레이아웃 컨테이너에 추가합니다. |
| [!UICONTROL Media] | 이미지, 비디오, 배너, 슬라이더 및 Google 맵을 스테이지의 기존 레이아웃 컨테이너에 추가합니다. |
| [!UICONTROL Add Content] | 기존 블록, 동적 블록 및 제품을 스테이지에 추가합니다. |

{style="table-layout:auto"}

### 관련 프로모션

| 필드 | 설명 |
|--- |--- |
| [!UICONTROL Related Cart Price Rule] | **[!UICONTROL Add Cart Price Rules]** - 기존 연결 [장바구니 가격 규칙](../merchandising-promotions/price-rules-cart.md) (동적 블록을 프로모션으로 사용) |
| [!UICONTROL Related Catalog Price Rule] | **[!UICONTROL Add Catalog Price Rules]** - 기존 연결 [카탈로그 가격 규칙](../merchandising-promotions/price-rules-catalog.md) (동적 블록을 프로모션으로 사용) |

{style="table-layout:auto"}
