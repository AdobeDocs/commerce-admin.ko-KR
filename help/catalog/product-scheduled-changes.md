---
title: 예약된 제품 업데이트
description: 캠페인 및 프로모션 프로그램을 지원하도록 제품 목록에 대한 변경 사항을 예약하는 방법을 알아봅니다.
exl-id: ce1aebe6-9032-438d-b950-4b13116b8ed3
feature: Catalog Management, Products
source-git-commit: 3d04e7213d90bb4c323acce69ac31c1dbcb7ca49
workflow-type: tm+mt
source-wordcount: '633'
ht-degree: 0%

---

# 제품 업데이트 예약

{{ee-feature}}

제품 업데이트는 일정에 따라 적용하고 다른 콘텐츠 변경 사항과 그룹화할 수 있습니다. [콘텐츠 스테이징](../content-design/content-staging.md)을 사용하여 제품에 대해 예약된 변경 내용을 기반으로 캠페인을 만들거나 기존 캠페인에 변경 내용을 적용할 수 있습니다.

>[!NOTE]
>
>[!UICONTROL Set Product as New From] 및 [!UICONTROL To] 필드와 [!UICONTROL Schedule Design Update] 탭이 ![Adobe Commerce](../assets/adobe-logo.svg) Adobe Commerce에서 제거되었으며 제품에서 직접 수정할 수 없습니다. 이러한 활성화를 위해 예약된 업데이트를 만들어야 합니다.

>[!NOTE]
>
>모든 예약된 업데이트가 연속적으로 적용되므로 모든 엔티티에 한 번에 하나의 예약된 업데이트만 있을 수 있습니다. 모든 예약된 업데이트는 해당 시간대 내의 모든 스토어 보기에 적용됩니다. 따라서 엔티티는 서로 다른 스토어 보기에 대해 동시에 서로 다른 예약된 업데이트를 가질 수 없습니다. 현재 예약된 업데이트의 영향을 받지 않는 모든 스토어 뷰 내의 모든 엔티티 속성 값은 이전 예약된 업데이트가 아닌 기본값에서 가져옵니다.

>[!NOTE]
>
>예약된 업데이트에 대한 스테이징 미리 보기는 항상 **기본** 스토어 보기에서 시작되며, 이는 스테이징 업데이트 캠페인을 탐색하는 고객의 경험을 에뮬레이션합니다.

## 예약된 업데이트 만들기

1. _관리자_ 사이드바에서 **[!UICONTROL Catalog]** > **[!UICONTROL Products]**(으)로 이동합니다.

1. 기존 제품을 선택하고 **[!UICONTROL Edit]**&#x200B;을(를) 클릭합니다.

1. **[!UICONTROL Schedule New Update]**&#x200B;을(를) 클릭합니다.

1. **[!UICONTROL Save as a New Update]**&#x200B;을(를) 선택합니다.

1. **[!UICONTROL Update Name]**&#x200B;의 경우 새 콘텐츠 스테이징 캠페인의 이름을 입력하십시오.

1. 업데이트의 간략한 **[!UICONTROL Description]**&#x200B;과(와) 사용 방법을 입력하십시오.

1. 일정(![일정 아이콘](../assets/icon-calendar.png)) 도구를 사용하여 캠페인에 대한 **[!UICONTROL Start Date]** 및 **[!UICONTROL End Date]**&#x200B;을(를) 선택하십시오.

   >[!NOTE]
   >
   >**_default_** 관리 시간대를 사용하여 캠페인 **[!UICONTROL Start Date]** 및 **[!UICONTROL End Date]**&#x200B;을(를) 정의해야 합니다. 이 시간대는 각 웹 사이트의 로컬 시간대에서 변환됩니다. 예를 들어 미국 시간대를 기준으로 캠페인을 시작하려는 시간대가 다른 여러 웹 사이트의 경우 각 현지 시간대에 대해 별도의 업데이트를 예약해야 합니다. 각각에 대해 **[!UICONTROL Start Date]** 및 **[!UICONTROL End Date]**&#x200B;을(를) 설정하고 로컬 웹 사이트 시간대에서 기본 관리 시간대로 변환됩니다.

   ![새 업데이트로 예약](./assets/product-schedule-as-new.png){width="600" zoomable="yes"}

1. 아래로 스크롤하여 _[!UICONTROL Price]_을(를) 클릭하고&#x200B;**[!UICONTROL Advanced Pricing]**을(를) 클릭합니다.

1. 예약된 캠페인 동안 제품에 대한 **[!UICONTROL Special Price]**&#x200B;을(를) 입력하고 **[!UICONTROL Done]**&#x200B;을(를) 클릭합니다.

1. 완료되면 **[!UICONTROL Save]**&#x200B;을(를) 클릭합니다.

## 기존 업데이트에 할당

1. _관리자_ 사이드바에서 **[!UICONTROL Catalog]** > **[!UICONTROL Products]**(으)로 이동합니다.

1. 기존 제품을 선택하고 **[!UICONTROL Edit]**&#x200B;을(를) 클릭합니다.

1. **[!UICONTROL Schedule New Update]**&#x200B;을(를) 클릭합니다.

1. **[!UICONTROL Assign to Existing Campaign]**&#x200B;을(를) 선택합니다.

1. 목록에서 수정할 캠페인을 선택합니다.

   ![기존 캠페인에 할당](./assets/scheduled-changes-assign-to-existing-campaign.png){width="600" zoomable="yes"}

1. ![확장 선택기](../assets/icon-display-expand.png) **[!UICONTROL Content]**&#x200B;을 확장합니다.

1. 완료되면 **[!UICONTROL Save]**&#x200B;을(를) 클릭합니다.

## 예약된 변경 내용 보기

예약된 변경 사항은 캠페인의 시작 및 종료 날짜와 함께 제품 페이지의 맨 위에 표시됩니다.

![예약된 변경](./assets/view-product-scheduled-changes.png){width="600" zoomable="yes"}

## 예약된 변경 내용 편집

1. 페이지 상단의 _[!UICONTROL Scheduled Changes]_상자에서&#x200B;**[!UICONTROL View/Edit]**을(를) 클릭합니다.

1. 예약된 업데이트에 필요한 변경 작업을 수행합니다.

1. **[!UICONTROL Save]**&#x200B;을(를) 클릭합니다.

## 예약된 변경 내용 제거

1. 페이지 상단의 _[!UICONTROL Scheduled Changes]_상자에서&#x200B;**[!UICONTROL View/Edit]**을(를) 클릭합니다.

1. 상단 표시줄에서 **[!UICONTROL Remove from Update]**&#x200B;을(를) 클릭합니다.

   ![예약된 변경 내용 제거](./assets/remove-product-scheduled-changes.png){width="600" zoomable="yes"}

1. 대화 상자에서 **[!UICONTROL Delete the Update]**&#x200B;을(를) 선택하고 **[!UICONTROL Done]**&#x200B;을(를) 클릭합니다.

   >[!NOTE]
   >
   >업데이트에서 제품이 제거되며 모든 예약된 변경 사항이 손실됩니다.

## 디자인 업데이트 예약

{{ce-feature}}

_[!UICONTROL Schedule Design Update]_섹션을 통해 제품 페이지의 모양을 임시로 변경할 수 있습니다. 시즌, 프로모션에 대한 디자인 변경을 예약하거나 새로운 항목을 만들기 위해 예약할 수 있습니다. 디자인 변경 사항은 미리 예약할 수 있으므로 정의된 일정에 따라 적용되거나_ drip _이 적용됩니다.

![예약된 디자인 업데이트](./assets/product-design-update-scheduled-ce.png){width="600" zoomable="yes"}


| 필드 | 설명 |
|--- |--- |
| [!UICONTROL Schedule Update From/To] | 사용자 지정 레이아웃을 제품에 적용할 때의 날짜 범위를 결정합니다. |
| [!UICONTROL New Theme] | 사용자 지정 테마를 제품에 적용합니다. |
| [!UICONTROL New Layout] | 제품 페이지에 다른 레이아웃을 적용합니다. 옵션: <br/>**[!UICONTROL No layout updates]**- 기본적으로 제품 페이지에서 레이아웃 업데이트를 사용할 수 없습니다.<br/>**[!UICONTROL Empty]** - 4열 페이지와 같은 고유한 레이아웃을 정의할 수 있습니다. (XML에 대한 이해가 필요합니다.) <br/>**[!UICONTROL 1 column]**- 제품 페이지에 1열 레이아웃을 적용합니다.<br/>**[!UICONTROL 2 columns with left bar]** - 왼쪽 사이드바가 있는 2열 레이아웃을 제품 페이지에 적용합니다. <br/>**[!UICONTROL 2 columns with right bar]**- 오른쪽 사이드바가 있는 2열 레이아웃을 제품 페이지에 적용합니다.<br/>**[!UICONTROL 3 columns]** - 제품 페이지에 3열 레이아웃을 적용합니다. |

{style="table-layout:auto"}
