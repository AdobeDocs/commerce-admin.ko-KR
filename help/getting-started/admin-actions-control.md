---
title: 작업 제어
description: Actions 컨트롤을 사용하여 관리자에서 하나 이상의 레코드에 작업을 적용하는 방법에 대해 알아봅니다.
exl-id: 03f313a9-bc17-4151-a2c8-8906342f025d
TQID: https://experienceleague.adobe.com/N8RFNMBc2i4Surct0luNp7z-qF0lbP6r8T-uEMQ7y-w
product_v2: id: eadea719-cf89-469b-a6fd-a236a7138047
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: f8a45b24-4be7-4f1b-909b-60d06b483a20
level_v2: id: b5a62a22-46f7-4f0d-b151-3fc640bef588id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2: id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 430
ht-degree: 0%

---

# 작업 제어

그리드에서 레코드 컬렉션을 사용하여 작업할 때 Actions 컨트롤을 사용하여 하나 이상의 레코드에 작업을 적용할 수 있습니다. Actions 컨트롤은 특정 유형의 데이터에 사용할 수 있는 각 작업을 나열합니다. 예를들어 Actions 컨트롤을 사용하여 선택한 제품의 특성을 업데이트하거나, 상태를 `Disabled`에서 `Enabled`(으)로 변경하거나, 데이터베이스에서 레코드를 삭제할 수 있습니다.

필요한 만큼 변경한 다음 한 단계에서 레코드를 업데이트할 수 있습니다. 각 제품에 대해 개별적으로 설정을 변경하는 것보다 훨씬 효율적입니다. 레코드 일괄 처리에 편집 내용을 적용하는 것은 비동기 작업으로, 작업이 완료될 때까지 기다리지 않고 관리자 작업을 계속할 수 있도록 백그라운드에서 실행됩니다. 작업이 완료되면 시스템이 메시지를 표시합니다.

사용 가능한 작업의 선택은 목록마다 다르며, 선택한 작업에 따라 추가 옵션이 나타날 수 있습니다. 예를들어 레코드 그룹의 상태를 변경할 때 추가 옵션을 사용하여 Actions 컨트롤 옆에 _[!UICONTROL Status]_상자가 나타납니다.

## 1단계: 레코드 선택

목록의 첫 번째 열에 있는 확인란은 작업의 타겟이 되는 각 레코드를 식별합니다. [필터 컨트롤](admin-grid-controls.md)을(를) 사용하여 작업을 대상으로 할 레코드로 목록을 좁힐 수 있습니다.

1. 필요한 경우 포함할 레코드만 표시하도록 각 열의 맨 위에 필터를 설정합니다.

1. 작업의 대상이 되는 각 레코드의 확인란을 선택하거나 열 선택기를 사용하여 일괄 선택을 선택합니다.

![페이지에서 모두 또는 모두 선택 또는 선택 해제](./assets/action-change-selection.png){width="500"}

## 2단계: 선택한 레코드에 작업 적용

1. **[!UICONTROL Actions]** 컨트롤을 적용할 작업으로 설정하십시오.

   **_Example:_** 업데이트 특성

   - 목록에서 업데이트할 각 레코드의 확인란을 선택합니다.

   - **[!UICONTROL Actions]** 컨트롤을 `Update Attributes`(으)로 설정합니다.

     ![특성 업데이트 작업 선택](./assets/action-select.png){width="450"}

   - **[!UICONTROL Submit]**&#x200B;을(를) 클릭합니다.

     속성 업데이트 페이지에는 사용 가능한 모든 속성이 왼쪽 패널의 그룹별로 나열되어 있습니다.

     ![특성 업데이트 페이지](./assets/action-update-attributes.png){width="700" zoomable="yes"}

   - 각 특성 옆의 **[!UICONTROL Change]** 확인란을 선택하고 필요한 변경을 수행합니다.

   - 선택한 레코드 그룹의 특성을 업데이트하려면 **[!UICONTROL Save]**&#x200B;을(를) 클릭하십시오.

1. 완료되면 **[!UICONTROL Submit]**&#x200B;을(를) 클릭합니다.

## 확인란 작업

| 액션 | 설명 |
|--- |--- |
| [!UICONTROL Select All] | 목록에 있는 모든 레코드의 확인란을 선택합니다. |
| [!UICONTROL Unselect All] | 목록의 모든 레코드 확인란을 선택 취소합니다. |
| [!UICONTROL Select All on This Page] | 현재 페이지에 표시된 레코드의 확인란을 선택합니다. |
| [!UICONTROL Deselect All on This Page] | 현재 페이지에 표시된 레코드의 확인란을 지웁니다. |

{style="table-layout:auto"}
