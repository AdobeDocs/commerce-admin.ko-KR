---
title: 이벤트 만들기 및 업데이트
description: 카탈로그에서 범주와 연결된 이벤트를 만드는 방법을 알아봅니다.
exl-id: 6c9f6a33-6785-4c3a-add6-dc2a6b16ed88
feature: Marketing Tools, Promotions/Events
source-git-commit: eb0fe395020dbe2e2496aba13d2f5c2bf2d0fc27
workflow-type: tm+mt
source-wordcount: '570'
ht-degree: 0%

---

# 이벤트 만들기 및 업데이트

{{ee-feature}}

각 이벤트는 카탈로그의 범주와 연결되고 한 번에 하나의 이벤트만 지정된 범주와 연결할 수 있습니다. 스토어에서 예정된 이벤트 목록을 표시하려면 [카탈로그 이벤트 회전](../content-design/widget-event-carousel.md) 위젯.

![이벤트 목록](./assets/category-events.png){width="700" zoomable="yes"}

## 이벤트 만들기

1. 다음에서 _관리자_ 사이드바, 이동 **[!UICONTROL Marketing]** > _[!UICONTROL Private Sales]_>**[!UICONTROL Events]**.

1. 오른쪽 위 모서리에서 을(를) 클릭합니다. **[!UICONTROL Add Catalog Event]**.

1. 범주 트리에서 이벤트와 연결할 범주를 선택합니다.

   각 카테고리는 한 번에 하나의 이벤트만 가질 수 있으므로 이벤트가 이미 있는 모든 카테고리는 비활성화됩니다.

   ![새 이벤트 - 범주 트리](./assets/catalog-events-category-tree.png){width="500" zoomable="yes"}

1. 다음을 정의합니다. **[!UICONTROL Catalog Event Information]**:

   ![카탈로그 이벤트 정보](./assets/catalog-event-information.png){width="700" zoomable="yes"}

   - 의 경우 **[!UICONTROL Start Date]** 이벤트 ( )의 달력 사용![달력 아이콘](../assets/icon-calendar.png))을 클릭하여 날짜를 선택합니다. 사용 **[!UICONTROL Hour]** 및 **[!UICONTROL Minute]** 슬라이더를 사용하여 이벤트가 시작되는 시간을 설정합니다.

   - 의 경우 **[!UICONTROL End Date]** 이벤트 ( )의 달력 사용![달력 아이콘](../assets/icon-calendar.png))을 클릭하여 날짜를 선택합니다. 사용 **[!UICONTROL Hour]** 및 **[!UICONTROL Minute]** 슬라이더를 사용하여 이벤트가 종료되는 시간을 설정합니다.

   - 업로드 **[!UICONTROL Image]** 이벤트 위젯의 경우 **[!UICONTROL Choose File]** 디렉토리에서 이미지 파일을 선택합니다.

   - 다음에서 **[!UICONTROL Sort Order]** 필드에 숫자를 입력하여 다른 이벤트와 함께 나열될 때 이 이벤트가 나타나는 순서를 나타냅니다.

   - 카운트다운 티커를 표시할 각 페이지 유형의 확인란을 선택합니다.

1. 완료되면 다음을 클릭하십시오. **[!UICONTROL Save]**.

## 이벤트 업데이트

이벤트는 이벤트 페이지 또는 이벤트와 연결된 카테고리에서 편집할 수 있습니다. 카테고리에 연관된 이벤트가 있는 경우 오른쪽 상단에 이벤트 편집 버튼이 표시됩니다.

### 방법 1: 이벤트 페이지에서 이벤트 편집

1. 다음에서 _관리자_ 사이드바, 이동 **[!UICONTROL Marketing]** > _[!UICONTROL Private Sales]_>**[!UICONTROL Events]**.

1. 목록에서 이벤트를 찾아 편집 모드로 엽니다.

1. 이벤트에 필요한 사항을 변경합니다.

1. 완료되면 다음을 클릭하십시오. **[!UICONTROL Save]**.

### 방법 2: 카테고리에서 이벤트 편집

1. 다음에서 _관리자_ 사이드바, 이동 **[!UICONTROL Catalog]** > **[!UICONTROL Categories]**.

1. 왼쪽의 카테고리 트리에서 이벤트와 관련된 카테고리를 선택합니다.

1. 오른쪽 위 모서리에서 을(를) 클릭합니다. **[!UICONTROL Edit Even]t**.

1. 이벤트에 필요한 사항을 변경합니다.

1. 완료되면 다음을 클릭하십시오. **[!UICONTROL Save]**.

## 이벤트 삭제

1. 다음에서 _관리자_ 사이드바, 이동 **[!UICONTROL Marketing]** > _[!UICONTROL Private Sales]_>**[!UICONTROL Events]**.

1. 목록에서 이벤트를 찾아 편집 모드로 엽니다.

1. 오른쪽 위 모서리에서 을(를) 클릭합니다. **[!UICONTROL Delete]**.

1. 작업을 확인하려면 을 클릭합니다. **[!UICONTROL OK]**.

## 필드 설명

| 필드 | [범위](../getting-started/websites-stores-views.md#scope-settings) | 설명 |
|--- |--- |--- |
| [!UICONTROL Category] | 글로벌 | 이벤트를 만들 때 이 필드는 범주 트리로 다시 연결됩니다. 이벤트를 편집할 때 이벤트와 관련된 카테고리 페이지로 연결됩니다. |
| [!UICONTROL Start Date] | 글로벌 | 의 이벤트 시작 날짜 및 시간 `MMDDYYYY HH;MM` 포맷. 달력 아이콘을 클릭하여 날짜를 선택합니다. |
| [!DNL End Date] | 글로벌 | 다음 위치의 이벤트 종료 날짜 및 시간 `MMDDYYYY HH;MM` 포맷. 달력 아이콘을 클릭하여 날짜를 선택합니다. |
| [!UICONTROL Image] | 스토어 뷰 | 에 표시되는 이미지를 업로드합니다. [카탈로그 이벤트 캐러셀 위젯](../content-design/widget-event-carousel.md). |
| [!UICONTROL Sort Order] | 글로벌 | 다른 이벤트와 함께 나열할 때 이 이벤트가 표시되는 시퀀스를 결정합니다. |
| [!UICONTROL Display Countdown Ticker On] | 글로벌 | 지정된 각 페이지의 헤더에 카운트다운 티커를 표시합니다. 옵션: `Category Page` / `Product Page` |
| [!UICONTROL Status] | 글로벌 | 시작 날짜 및 종료 날짜 범위를 기반으로 이벤트의 상태를 나타냅니다. 상태는 읽기 전용 값입니다. 값: `Open` / `Closed` / `Upcoming` |

{style="table-layout:auto"}

## 단추 막대

| 단추 | 설명 |
|--- |--- |
| **[!UICONTROL Back]** | 새 이벤트나 기존 이벤트의 변경 사항을 저장하지 않고 이벤트 페이지로 돌아갑니다. |
| **[!UICONTROL Delete]** | 이벤트를 삭제합니다. |
| **[!UICONTROL Reset]** | 저장하지 않은 변경 내용의 양식을 지우고 원래 이벤트 정보를 복원합니다. |
| **[!UICONTROL Save and Continue Edit]** | 모든 변경 사항을 저장하고 편집 모드에서 양식을 열어 둡니다. |
| **[!UICONTROL Save]** | 변경 사항을 저장하고, 양식을 닫은 다음 이벤트 페이지로 돌아갑니다. |

{style="table-layout:auto"}
