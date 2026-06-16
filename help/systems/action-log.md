---
title: 작업 로그
description: 저장소에 대한 모든 변경 사항을 추적하는 데 도움이 되는 작업 로그 및 기록된 작업을 구성하는 방법에 대해 알아봅니다.
exl-id: a482adfe-a63f-428b-b078-7542a1e2ecee
feature: Logs, Configuration
TQID: https://experienceleague.adobe.com/UtJhP452hJXDyEyjxrknuF4WPoLza-UcnuWxP6ILtq8
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2:
  - id: ba9e5be9-7de1-4f71-a5d2-baead0e425ee
  - id: bd989d82-1e15-4534-88db-f1f51dd77ffa
  - id: dac87252-6066-4d6e-a9d2-f6d84c323de7
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: f8a45b24-4be7-4f1b-909b-60d06b483a20
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2:
  - id: d095671a-1355-40aa-8b5f-06c33c68080b
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 289
ht-degree: 0%

---

# 작업 로그

{{ee-feature}}

작업 로그는 저장소에서 작업하는 관리 사용자가 수행한 모든 변경 사항을 기록(로그)합니다. 이를 통해 스토어에 대한 모든 변경 사항을 추적할 수 있습니다. 이러한 변경 내용을 추적하고 사용자에 대한 [관리자 권한](permissions.md) 설정과 함께 원치 않는 변경 내용으로부터 스토어를 보호하는 데 도움이 될 수 있습니다.

대부분의 관리 작업의 경우, 기록된 정보에는 작업, 사용자 이름, 작업의 성공 또는 실패, 작업의 영향을 받는 객체의 ID가 포함됩니다. IP 주소 및 날짜도 기록됩니다.

기본적으로 모든 관리 작업이 활성화되고 기록됩니다. 관리 작업 로깅을 구성하려면 옵션을 검토하고 각 작업 유형에 대한 확인란을 선택하거나 선택을 취소합니다. Adobe Commerce은 확인된 유형만 기록합니다.

[작업 로그 보고서](action-log-report.md)를 보고 기록된 관리 작업 및 세부 정보를 검토하십시오.

![고급 구성 - 관리자 작업 로깅](../configuration-reference/advanced/assets/admin-actions-logging.png){width="600" zoomable="yes"}

구성 설정의 자세한 목록을 보려면 _구성 참조_&#x200B;에서 [관리 작업 로그 보관](../configuration-reference/advanced/system.md)을 참조하십시오.

## 로깅에 대한 관리 작업 구성

1. _관리자_ 사이드바에서 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**(으)로 이동합니다.

1. 왼쪽 패널에서 **[!UICONTROL Advanced]**&#x200B;을(를) 확장하고 **[!UICONTROL Admin]**&#x200B;을(를) 선택합니다.

1. **[!UICONTROL Admin Actions Logging]** 섹션에서 ![확장 선택기](../assets/icon-display-expand.png)를 확장하고 각 작업에 대해 다음 작업을 수행합니다.

   - 작업에 대한 관리자 로깅을 활성화하려면 확인란을 선택합니다.
   - 작업에 대한 관리자 로깅을 비활성화하려면 확인란의 선택을 취소합니다.

1. 완료되면 **[!UICONTROL Save Config]**&#x200B;을(를) 클릭합니다.

## 관리 작업 로그 보관

관리 작업 로그는 일 수에 관계없이 보관할 수 있습니다. 지정된 기간 후에 아카이브를 삭제할 수도 있습니다.

1. 왼쪽 패널에서 **[!UICONTROL Advanced]**&#x200B;을(를) 확장하고 **[!UICONTROL System]**&#x200B;을(를) 선택합니다.

1. **[!UICONTROL Admin Action Log Archiving]**&#x200B;을(를) 확장하고 옵션을 설정합니다.

   - **[!UICONTROL Logs Entry Lifetime, Days]** - 보관된 로그를 유지할 일 수를 설정합니다.
   - **[!UICONTROL Log Archiving Frequency]** - 아카이브 생성 빈도를 설정합니다.

1. 완료되면 **[!UICONTROL Save Config]**&#x200B;을(를) 클릭합니다.
