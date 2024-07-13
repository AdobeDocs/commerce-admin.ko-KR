---
title: 범주에 대해 예약된 변경 사항
description: 마케팅 캠페인 및 스토어 프로모션을 지원하기 위해 카테고리 변경을 예약하는 방법을 알아봅니다.
exl-id: 9e25082f-4e76-4148-b76e-dca0b14971eb
feature: Catalog Management, Categories
source-git-commit: 3d04e7213d90bb4c323acce69ac31c1dbcb7ca49
workflow-type: tm+mt
source-wordcount: '411'
ht-degree: 0%

---

# 범주에 대해 예약된 변경 사항

{{ee-feature}}

범주 업데이트는 일정에 따라 적용하고 다른 콘텐츠 변경 사항과 그룹화할 수 있습니다. 범주에 대한 예약된 변경 사항을 기반으로 캠페인을 생성하거나 기존 캠페인에 변경 사항을 적용할 수 있습니다. 자세한 내용은 [콘텐츠 스테이징](../content-design/content-staging.md)을 참조하세요.

>[!NOTE]
>
>[!UICONTROL Schedule Design Update] 탭은 ![Adobe Commerce](../assets/adobe-logo.svg) Adobe Commerce에서 제거되었으며 카테고리에서 직접 수정할 수 없습니다. 이러한 활성화를 위해 예약된 업데이트를 만들어야 합니다.

>[!NOTE]
>
>모든 예약된 업데이트가 연속적으로 적용되므로 모든 엔티티에 한 번에 하나의 예약된 업데이트만 있을 수 있습니다. 모든 예약된 업데이트는 해당 시간대 내의 모든 스토어 보기에 적용됩니다. 따라서 엔티티는 서로 다른 스토어 보기에 대해 동시에 여러 개의 예약된 업데이트를 가질 수 없습니다. 현재 예약된 업데이트의 영향을 받지 않는 모든 스토어 뷰 내의 모든 엔티티 속성 값은 이전 예약된 업데이트가 아닌 기본값에서 가져옵니다.

## 범주로 업데이트 예약

1. _관리자_ 사이드바에서 **[!UICONTROL Catalog]** > **[!UICONTROL Categories]**(으)로 이동합니다.

1. 왼쪽의 범주 트리에서 수정할 범주를 선택합니다.

1. 페이지 상단의 _예약된 변경 내용_ 상자에서 **[!UICONTROL Schedule New Update]**&#x200B;을(를) 클릭합니다.

   ![예약된 변경 내용](./assets/category-scheduled-changes.png){width="600" zoomable="yes"}

1. **[!UICONTROL Save as a New Update]** 옵션을 선택한 상태에서 업데이트에 대한 기본 매개 변수를 설정합니다.

   - **[!UICONTROL Update Name]**&#x200B;의 경우 새 콘텐츠 스테이징 캠페인의 이름을 입력하십시오.

   - 업데이트의 간략한 **[!UICONTROL Description]**&#x200B;과(와) 사용 방법을 입력하십시오.

   - 일정( ![일정 아이콘](../assets/icon-calendar.png)) 도구를 사용하여 캠페인에 대한 **[!UICONTROL Start Date]** 및 **[!UICONTROL End Date]**&#x200B;을(를) 선택하십시오.

   >[!IMPORTANT]
   >
   >**_default_** 관리 시간대를 사용하여 캠페인 **[!UICONTROL Start Date]** 및 **[!UICONTROL End Date]**&#x200B;을(를) 정의해야 합니다. 이 시간대는 각 웹 사이트의 로컬 시간대에서 변환됩니다. 예를 들어 미국 시간대를 기준으로 캠페인을 시작하려는 시간대가 다른 여러 웹 사이트의 경우 각 현지 시간대에 대해 별도의 업데이트를 예약해야 합니다. 각 **[!UICONTROL Start Date]** 및 **[!UICONTROL End Date]**&#x200B;을(를) 설정했으며, 로컬 웹 사이트 시간대에서 기본 관리 시간대로 변환됩니다.

   ![예약된 변경 내용](./assets/category-scheduled-changes-new-update.png){width="600" zoomable="yes"}

1. 예약된 업데이트에 필요한 변경 작업을 수행합니다.

1. 변경 내용을 미리 보려면 오른쪽 상단 단추 모음에서 **[!UICONTROL Preview]**&#x200B;을(를) 클릭합니다.

1. 완료되면 **[!UICONTROL Save]**&#x200B;을(를) 클릭합니다.

## 기존 업데이트에 할당

1. _관리자_ 사이드바에서 **[!UICONTROL Catalog]** > **[!UICONTROL Categories]**(으)로 이동합니다.

1. 왼쪽의 범주 트리에서 수정할 범주를 선택합니다.

1. 페이지 상단의 _예약된 변경 내용_ 상자에서 **[!UICONTROL Schedule New Update]**&#x200B;을(를) 클릭합니다.

1. **[!UICONTROL Assign to Existing Campaign]**&#x200B;을(를) 선택합니다.

1. 목록에서 필요한 캠페인을 찾아 **[!UICONTROL Select]**&#x200B;을(를) 클릭합니다.

1. 예약된 업데이트에 필요한 사항을 변경합니다.

1. 완료되면 **[!UICONTROL Save]**&#x200B;을(를) 클릭합니다.
