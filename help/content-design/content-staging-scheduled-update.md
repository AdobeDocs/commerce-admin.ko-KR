---
title: 콘텐츠 업데이트 예약
description: 제품에 대한 임시 가격 변경을 예약하는 데 사용되는 이 캠페인 예제를 검토하십시오.
exl-id: 36b7d7f6-4590-4192-a82b-e5f645b05f62
feature: Page Content, Staging
source-git-commit: b3897ba034770229ef8f3117231bed286abdddb9
workflow-type: tm+mt
source-wordcount: '636'
ht-degree: 0%

---

# 콘텐츠 업데이트 예약

{{ee-feature}}

다음 예는 제품에 대한 임시 가격 변경을 예약하는 방법을 보여줍니다. 변경 내용 예약 및 미리 보기, 캘린더에서 예약된 업데이트 보기 등이 포함됩니다. 이 예에는 단일 변경 사항만 포함되어 있지만 캠페인에는 제품, 가격 규칙, CMS 페이지 및 동시에 진행되도록 예약된 기타 엔티티에 대한 여러 변경 사항이 포함될 수 있습니다. 유사한 방법에 따라 의 시작/종료 날짜를 지정합니다. [!UICONTROL Set Product As New] 특성.

>[!NOTE]
>다음에 대한 시작(및 종료) 날짜를 지정하려면 예약된 업데이트를 만들어야 합니다. [!UICONTROL Set Product As New]. 대상 [!UICONTROL Special Price] 및 [!UICONTROL Design Change], 시작 날짜/종료 날짜 필드는 Adobe Commerce에서 제거되며 Magento Open Source 전용입니다.
>
>모든 예약된 업데이트가 연속적으로 적용되므로 모든 엔티티에 한 번에 하나의 예약된 업데이트만 있을 수 있습니다. 모든 예약된 업데이트는 해당 시간대 내의 모든 스토어 보기에 적용됩니다. 따라서 엔티티는 서로 다른 스토어 보기에 대해 동시에 다른 예약된 업데이트를 가질 수 없습니다. 현재 예약된 업데이트의 영향을 받지 않는 모든 스토어 뷰 내의 모든 엔티티 속성 값은 이전 예약된 업데이트가 아닌 기본값에서 가져옵니다.

## 제품에 대한 업데이트 예약

1. 다음에서 _[!UICONTROL Products]_그리드에서 제품을 편집 모드로 엽니다.

1. 다음에서 _[!UICONTROL Scheduled Changes]_페이지 상단의 상자에서&#x200B;**[!UICONTROL Schedule New Update]**.

   ![새 업데이트 예약](./assets/content-staging-product-schedule-new-update.png){width="600" zoomable="yes"}

1. 포함 **[!UICONTROL Save as a New Update]** 옵션을 선택한 경우 업데이트에 대한 기본 매개 변수를 설정합니다.

   - 대상 **[!UICONTROL Update Name]**, 새 콘텐츠 스테이징 캠페인의 이름을 입력합니다.

   - 개요 입력 **[!UICONTROL Description]** 업데이트 및 사용 방법

   - 달력(![달력 아이콘](../assets/icon-calendar.png)) 도구: **시작일** 및 **종료일** 캠페인을 위한 것입니다.

     끝이 열린 캠페인을 만들려면 종료 날짜를 지정하지 마십시오(비워 둠). 이 예제의 경우 캠페인은 2021년 1월 1일 자정(태평양 표준시 오전 12시)에 시작될 예정입니다.


     종료 일자 없이 생성된 가격 규칙 캠페인의 경우 종료 일자는 나중에 추가할 수 없습니다. 이러한 경우 캠페인을 만들고 시작 날짜를 이전 캠페인이 종료되고 새 캠페인이 시작되도록 하려는 날짜로 설정해야 합니다. 해당 시작 날짜에 이전 캠페인이 종료되고 새 캠페인이 정의된 대로 시작됩니다.

     ![제품 업데이트 예약](./assets/content-staging-campaign-schedule-update.png){width="600" zoomable="yes"}

     >[!NOTE]
     >
     >캠페인 시작 날짜 및 종료 날짜는 다음을 사용하여 정의해야 합니다. **_기본값_** 관리 시간대로, 각 웹 사이트의 로컬 시간대에서 변환됩니다. 예를 들어, 서로 다른 시간대에 여러 웹 사이트가 있지만 미국(기본) 시간대를 기반으로 하는 캠페인을 시작하려면 각 로컬 시간대에 대해 별도의 업데이트를 예약해야 합니다. 이 경우 다음을 설정합니다. **[!UICONTROL Start Date]** 및 **[!UICONTROL End Date]** 각 로컬 웹 사이트 시간대에서 기본 관리 시간대로 변환됩니다.

1. 아래로 스크롤하여 _[!UICONTROL Price]_및 클릭&#x200B;**[!UICONTROL Advanced Pricing]**.

1. 입력 **[!UICONTROL Special Price]** 예약된 캠페인 동안 제품에 대해 다음을 클릭합니다. **[!UICONTROL Done]**.

1. 완료되면 다음을 클릭하십시오. **[!UICONTROL Save]**.

   예약된 변경 사항은 캠페인의 시작 및 종료 날짜와 함께 제품 페이지의 맨 위에 표시됩니다.

   ![예약된 변경 내용](./assets/content-staging-product-scheduled-update-preview-rope.png){width="600" zoomable="yes"}

## 예약된 변경 내용 편집

1. 다음에서 _예약된 변경 사항_ 페이지 상단의 상자에서 **[!UICONTROL View/Edit]**.

1. 예약된 업데이트에 필요한 변경 작업을 수행합니다.

1. 클릭 **[!UICONTROL Save]**.

## 예약된 변경 내용 미리 보기

다음에서 _예약된 변경 사항_ 페이지 상단의 상자에서 **[!UICONTROL Preview]**.

미리보기에서는 새 브라우저 탭을 열고 예약된 캠페인 동안 제품이 표시되는 방식을 보여 줍니다.

>[!NOTE]
>
>예약된 업데이트에 대한 스테이징 미리 보기는 항상 다음에서 시작됩니다. **기본값** 스토어 보기 - 스테이징 업데이트 캠페인을 탐색하는 고객의 경험을 에뮬레이션합니다.

미리 보기 콘텐츠 도구를 사용하여 미리 보기의 날짜 및 범위를 변경하는 방법에 대한 자세한 내용은 [캠페인 미리 보기](content-staging-preview.md). 스토어 미리보기에 대한 링크를 동료와 공유할 수도 있습니다.
