---
title: 관리자 메시지 받은 편지함
description: Adobe 및 의 중요하고 유용한 메시지를 제공하는 관리자 메시지 받은 편지함에 대해 알아봅니다. [!DNL Commerce] 시스템.
exl-id: c53bb0e4-9f18-4d40-8cc4-8c3b485f8d68
source-git-commit: 7b6d70e2f3052af69075790cec1f396e2505bf8b
workflow-type: tm+mt
source-wordcount: '394'
ht-degree: 0%

---

# 관리자 메시지 받은 편지함

스토어는 정기적으로 Adobe에서 메시지를 수신합니다. 메시지는 중요도별로 평가되며 시스템 업데이트, 패치, 새로운 릴리스, 예약된 유지 관리 또는 예정된 이벤트를 의미할 수 있습니다. 헤더의 벨 아이콘은 받은 편지함에서 읽지 않은 메시지 수를 나타냅니다.

![책임자 - 받는 메시지](./assets/admin-inbox-summary.png){width="700" zoomable="yes"}

다음 _[!UICONTROL Notifications]_페이지에는 날짜별로 순위가 매겨진 모든 메시지가 나열됩니다. 다음_[!UICONTROL Action]_ 명령은 개별 메시지를 읽은 상태로 표시하거나 자세한 정보를 보거나 받은 편지함에서 메시지를 제거하는 데 사용할 수 있습니다.

이 구성은 받은 편지함의 업데이트 빈도와 메시지 전달 방식을 결정합니다. 스토어 관리자에게 보안 URL이 있는 경우 HTTPS를 통해 알림이 전달되어야 합니다.

## 새로 들어오는 메시지 보기

1. 다음을 클릭합니다. **[!UICONTROL Notification]** 아이콘을 클릭하고 요약을 읽습니다.

1. 다음 중 하나를 수행합니다.

   - 필요한 경우 메시지를 클릭하여 전체 텍스트를 표시합니다.
   - 메시지를 삭제하려면 메시지 오른쪽에 있는 삭제 아이콘을 클릭합니다.
   - 전체 알림 목록을 표시하려면 **[!UICONTROL See All]**.

## 중요 메시지 해결

매우 중요한 메시지에 대해 다음 중 하나를 수행합니다.

- 클릭 **[!UICONTROL Read Details]**.
- 경고 상자를 무시하고 메시지를 활성 상태로 유지하려면 **[!UICONTROL Close]**.

## 알림 관리

1. 다음 중 하나를 수행하여 알림 페이지를 엽니다.

   - 다음을 클릭합니다. **[!UICONTROL Notification]** 아이콘으로 표시됩니다. 새 메시지가 하나 이상 표시되면 **[!UICONTROL See All]**.

   - 다음에서 _관리자_ 사이드바, 이동 **[!UICONTROL System]** > _[!UICONTROL Other Settings]_>**[!UICONTROL Notifications]**.

1. 다음에서 **[!UICONTROL Action]** column에서 다음 중 하나를 수행합니다.

   - 자세한 내용을 보려면 **[!UICONTROL Read Details]** 링크된 페이지를 새 창에서 엽니다.

   - 메시지를 받은 편지함에 보관하려면 **[!UICONTROL Mark As Read]**.

     ![책임자 - 선택한 알림을 읽은 상태로 표시](./assets/admin-notifications-mark-as-read.png){width="700" zoomable="yes"}

   - 메시지를 삭제하려면 **[!UICONTROL Remove]**.

1. 여러 메시지에 작업을 적용하려면 다음 중 하나를 수행합니다.

   - 관리할 각 메시지에 대해 첫 번째 열의 확인란을 선택합니다.
   - 여러 메시지를 선택하려면 다음을 설정하십시오. **[!UICONTROL Mass Actions]** 필요에 따라 제어합니다.

1. 설정 **[!UICONTROL Actions]** 다음 중 하나를 제어하십시오.

   - `Mark as Read`
   - `Remove`

1. 클릭 **[!UICONTROL Submit]** 을 클릭하여 프로세스를 완료합니다.

## 알림 구성

1. 다음에서 _관리자_ 사이드바, 이동 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. 왼쪽 탐색 패널에서 를 확장합니다. **[!UICONTROL Advanced]** 및 선택 **[!UICONTROL System]**.

1. 확장 ![확장 선택기](../assets/icon-display-expand.png)다음 **[!UICONTROL Notifications]** 섹션.

   ![알림 구성](./assets/system-notifications.png){width="600"}

1. 저장소 관리자가 다음을 통해 실행되는 경우 [보안 URL](../stores-purchase/store-urls.md), 설정됨 **[!UICONTROL Use HTTPS to Get Feed]** 끝 `Yes`.

1. 설정 **[!UICONTROL Update Frequency]** 받은 편지함의 업데이트 빈도를 결정합니다.

   간격은 1시간에서 24시간일 수 있습니다.

1. 완료되면 다음을 클릭하십시오. **[!UICONTROL Save Config]**.

에 대한 자세한 내용은 [!UICONTROL System] 구성 옵션을 보려면 다음을 참조하십시오. [_구성 참조 안내서_](../configuration-reference/advanced/system.md).
