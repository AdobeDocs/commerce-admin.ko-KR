---
title: 카탈로그 가격 규칙에 대한 예약된 변경 사항
description: 캠페인의 일부로 일정에 카탈로그 가격 규칙을 적용하고 다른 콘텐츠 변경 사항과 그룹화하는 방법을 알아봅니다.
exl-id: ec4b915f-0a27-438d-b1b0-f1bcd297af6d
feature: Merchandising, Price Rules, Catalog Management
source-git-commit: 3d04e7213d90bb4c323acce69ac31c1dbcb7ca49
workflow-type: tm+mt
source-wordcount: '827'
ht-degree: 0%

---

# 카탈로그 가격 규칙에 대한 예약된 변경 사항

{{ee-feature}}

새 가격 규칙을 저장하거나 업데이트하면 페이지 상단에 예약된 변경 상자가 나타납니다. 카탈로그 가격 규칙은 캠페인의 일부로 일정에 따라 적용하고 다른 콘텐츠 변경 사항과 그룹화할 수 있습니다. 가격 규칙에 대한 예약된 변경 사항을 기반으로 캠페인을 생성하거나 변경 사항을 기존 캠페인에 적용할 수 있습니다.

>[!NOTE]
>
>다음 [!UICONTROL From] 및 [!UICONTROL To] 다음에서 필드가 제거됨: ![Adobe Commerce](../assets/adobe-logo.svg) Adobe Commerce 및 는 카탈로그 가격 규칙에서 직접 수정할 수 없습니다. 이러한 활성화를 위해 예약된 업데이트를 만들어야 합니다.

>[!NOTE]
>
>모든 예약된 업데이트가 연속적으로 적용됩니다. 즉, 모든 엔티티는 한 시점에서 하나의 예약된 업데이트만 가질 수 있습니다. 모든 예약된 업데이트는 해당 시간대 내의 모든 스토어 보기에 적용됩니다. 따라서 엔티티는 서로 다른 스토어 보기에 대해 동시에 서로 다른 예약된 업데이트를 가질 수 없습니다. 현재 예약된 업데이트의 영향을 받지 않는 모든 스토어 뷰 내의 모든 엔티티 속성 값은 이전 예약된 업데이트가 아닌 기본값에서 가져옵니다.

동일한 캠페인에서 여러 개의 가격 규칙이 실행되는 경우 가격 규칙의 우선순위 설정에 따라 우선 순위가 결정됩니다. 자세한 내용은 다음을 참조하십시오. [컨텐츠 스테이징](../content-design/content-staging.md).

>[!IMPORTANT]
>
>가격 규칙이 포함된 캠페인을 처음에 종료 날짜 없이 만든 경우 종료 날짜를 포함하도록 캠페인을 나중에 편집할 수 없습니다. 캠페인을 만들 때 종료 날짜를 추가하거나 기존 캠페인의 중복 버전을 만들고 필요에 따라 종료 날짜를 중복에 추가하는 것이 좋습니다.

![카탈로그 가격 규칙 - 예약된 변경 사항](./assets/price-rule-catalog-scheduled.png){width="600" zoomable="yes"}

## 카탈로그 가격 규칙 업데이트 예약

1. 다음에서 _관리자_ 사이드바, 이동 **[!UICONTROL Marketing]** > _[!UICONTROL Promotions]_>**카탈로그 가격 규칙**.

1. 편집 모드에서 규칙을 엽니다.

1. 다음에서 **[!UICONTROL Scheduled Changes]** 페이지 상단의 상자에서 **[!UICONTROL Schedule New Update]**.

1. 포함 **[!UICONTROL Save as a New Update]** 옵션을 선택한 경우 다음을 수행합니다.

   - 대상 **[!UICONTROL Update Name]**&#x200B;를 클릭하고 규칙 업데이트의 이름을 입력합니다.

   - 개요 입력 **[!UICONTROL Description]** 적용 방법 또는 이유를 포함한 업데이트.

   - 사용 _캘린더_ (![달력 아이콘](../assets/icon-calendar.png))을 클릭하여 선택합니다 **[!DNL Start Date]** 및 **[!UICONTROL End Date]** 예약된 변경 사항이 적용됩니다. 끝이 열린 변경 내용을 만들려면 종료 날짜를 비워 둡니다.

   ![카탈로그 가격 규칙 - 새로운 예약된 변경 사항](./assets/price-rule-catalog-schedule-update.png){width="600" zoomable="yes"}

   >[!NOTE]
   >
   >시작 및 종료 날짜/시간은 특정 웹 사이트의 시간대가 아니라 기본 관리 패널 날짜/시간 및 시간대로 결정됩니다. 웹 사이트의 시간대를 고려하여 시작 및 종료 시간을 적절하게 결정하십시오. 특정 현지 시간에 시작 및/또는 중지해야 하는 시간대가 다른 웹 사이트에 대한 별도의 규칙을 만듭니다.

1. 아래로 스크롤하여 **[!UICONTROL Rule Information]** 섹션에 추가하고 필요에 따라 규칙을 변경합니다.

   규칙의 웹 사이트(범위)/고객 그룹, 규칙의 조건 및 규칙이 적용하는 작업을 포함하여 모든 규칙 매개 변수에 대한 변경 사항을 예약할 수 있습니다. 자세한 내용은 [카탈로그 가격 규칙 생성](price-rules-catalog-create.md).

   >[!NOTE]
   >
   >규칙 정보 매개 변수를 변경하는 경우 _[!UICONTROL Status]_가 올바르게 설정되었습니다. 를 변경하여 활성화된 규칙이 적용되도록 하려면 상태가 다음과 같아야 합니다.`Active`.

1. 완료되면 다음을 클릭하십시오. **[!UICONTROL Save]**.

   예약된 변경 사항은 캠페인의 시작 및 종료 날짜와 함께 페이지 맨 위에 표시됩니다.

## 예약된 규칙 변경 사항 편집

1. 다음에서 **[!UICONTROL Scheduled Changes]** 페이지 상단의 상자에서 **[!UICONTROL View/Edit]**.

1. 예약된 업데이트에 필요한 변경 작업을 수행합니다.

1. 클릭 **[!UICONTROL Save]**.

## 예약된 규칙 변경 내용 미리 보기

1. 다음에서 **[!UICONTROL Scheduled Changes]** 페이지 상단의 상자에서 **[!UICONTROL Preview]**.

   미리보기에서는 적용된 예약 변경 사항이 있는 상점 전면을 로드하는 새 브라우저 탭을 엽니다. 변경의 영향을 받는 제품으로 이동합니다.

   ![예약된 변경 내용 미리 보기](./assets/price-rule-catalog-scheduled-update-preview.png){width="600" zoomable="yes"}

1. 미리보기 창의 왼쪽 상단 모서리에서 을(를) 클릭합니다. **[!UICONTROL Calendar]**.

   달력 세부 정보에는 같은 날 예약된 다른 캠페인이 표시됩니다. 목록의 각 레코드는 별도의 규칙 업데이트입니다.

   ![특정 날짜에 대해 예약된 업데이트 목록](./assets/price-rule-catalog-scheduled-preview-calendar.png){width="600" zoomable="yes"}

1. 다른 날짜나 시간을 미리 보려면 **[!UICONTROL Date & Time]** 달력 ![달력 아이콘](../assets/icon-calendar.png) 다음을 수행합니다.

   - 다른 날짜 및/또는 시간을 선택하십시오.

   - 클릭 **[!UICONTROL Preview]**.

1. 캘린더로 돌아가려면 **[!UICONTROL Calendar]** 를 추가합니다.

   여기에서 다음 작업을 수행할 수 있습니다.

   **미리보기에 대한 링크 공유**

   스토어 미리 보기에 대한 링크를 동료와 공유하려면 **[!UICONTROL Share]**. 링크를 클립보드에 복사한 다음 이메일 메시지 본문에 붙여넣습니다.

   >[!NOTE]
   >
   >공유 미리 보기를 보려면 관리자 계정이 필요합니다. 다음의 경우 [역할에 액세스 권한 있음](../systems/permissions-user-roles.md) 관리자 사용자 계정을 만들려면 공유하기 전에 새 사용자에 대한 계정을 만들어야 합니다.

   **미리보기 범위 변경**

   다른 저장소 보기에 대해 예약된 변경 내용을 보려면 **[!UICONTROL Scope]** 를 추가합니다. 미리 보려는 웹 사이트, 스토어 또는 스토어 보기를 선택합니다.

1. 필요한 경우 캘린더로 돌아가서 **[!UICONTROL View/Edit]** 다음에서 _[!UICONTROL Action]_다른 예약된 업데이트를 여는 열입니다.
