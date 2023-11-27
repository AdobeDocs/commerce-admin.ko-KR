---
title: 작업 로그 아카이브
description: 관리 작업 로그 아카이브를 구성하고 보는 방법에 대해 알아봅니다.
exl-id: a839f1c6-b5e2-4881-bfaa-267e47585441
feature: Logs, Configuration
source-git-commit: 64ccc2d5016e915a554c2253773bb50f4d33d6f4
workflow-type: tm+mt
source-wordcount: '160'
ht-degree: 0%

---

# 작업 로그 아카이브

{{ee-feature}}

관리자 [작업](action-log.md) 보관: 서버에 저장된 CSV 로그 파일을 나열합니다. 구성에서는 로그 항목이 저장되는 기간 및 아카이브되는 빈도를 지정할 수 있습니다. 기본적으로 파일 이름에는 현재 날짜가 ISO 형식으로 포함되어 있습니다.  `yyyyMMddHH`

>[!NOTE]
>
>로그 보관에는 다음이 필요합니다. [cron job](cron.md) 설정할 수 있습니다.

## 로그 아카이브 구성

1. 다음에서 _관리자_ 사이드바, 이동 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. 왼쪽 패널에서 를 확장합니다. **[!UICONTROL Advanced]** 및 선택 **[!UICONTROL System]**.

1. 확장 ![확장 선택기](../assets/icon-display-expand.png) 다음 **[!UICONTROL Admin Actions Log Archiving]** 섹션을 만들고 다음 옵션을 설정합니다.

   - **[!UICONTROL Log Entry Lifetime, Days]** — 로그 항목을 제거하기 전에 데이터베이스에 보관할 일 수를 입력합니다.
   - **[!UICONTROL Log Archiving Frequency]** — 다음으로 설정 `Daily`, `Weekly`, 또는 `Monthly`.

   ![고급 구성 - 관리 작업 로그 보관](../configuration-reference/advanced/assets/system-admin-actions-log-archiving.png){width="600" zoomable="yes"}

   구성 설정에 대한 자세한 목록이 필요하면 를 참조하십시오. [관리 작업 로그 보관](../configuration-reference/advanced/system.md) 다음에서 _구성 참조_.

1. 완료되면 다음을 클릭하십시오. **[!UICONTROL Save Config]**.

## 아카이브 보기

다음에서 _관리자_ 사이드바, 이동 **[!UICONTROL System]** > _[!UICONTROL Actions Logs]_>**[!UICONTROL Archive]**.

![작업 로그 아카이브](./assets/action-log-archive.png){width="600" zoomable="yes"}
