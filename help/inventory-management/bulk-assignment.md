---
title: 일괄 재고 출처 지정 및 지정 취소
description: 관리자의 일괄 소스 할당 작업을 사용하여 한 번에 많은 제품에 대한 [!DNL Inventory Management] 소스를 할당하거나 할당을 취소할 수 있습니다.
exl-id: 1f1e81a5-fb06-46b7-84ca-7feea4942093
feature: Inventory, Products
last-update: 2023-06-28
TQID: 'https://experienceleague.adobe.com/H8UQh7quyOeDq6-hSmf83fzUuJkuSLv0i2dezX-GKRA'
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
    internal-label: Commerce
feature_v2:
  - id: c1256247-af4b-46d8-9dca-0c654ecfa157
    internal-label: Order Management System
  - id: 8dc0e58b-adf0-51bb-8db5-bb36e3e656fb
    internal-label: Inventory
  - id: 4067ab89-2e97-5de1-8d98-de8318461a8d
    internal-label: Products
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
    internal-label: Admin
  - id: f8a45b24-4be7-4f1b-909b-60d06b483a20
    internal-label: Leader
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
    internal-label: Intermediate
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
    internal-label: Beginner
topic_v2:
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
    internal-label: Administration
source-git-commit: 15f1e2ee152fb047443da68dec2cc69551e6c7a0
workflow-type: tm+mt
source-wordcount: '333'
ht-degree: 0%
---
# 일괄 소스 할당 및 할당 해제

_소스 할당_ 도구를 사용하여 제품에 하나 이상의 소스를 추가하십시오. 이 도구는 사용자 지정 소스를 만들고 기본 재고 또는 사용자 지정 재고에 할당하고 새 위치와 재고를 준비할 때 도움이 됩니다.

새 사용자 지정 소스를 추가한 후 관리자를 통해 또는 [가져오기 기능](inventory-import-export.md)을 사용하여 제품당 [재고 수량](quantities-assign-per-product.md) 또는 여러 제품에 대한 재고 수량을 추가할 수 있습니다.

![선택한 제품에 대한 인벤토리 소스 추가](assets/inventory-bulk-assign-sources.gif)

## 출처 및 수량 지정

1. _관리자_ 사이드바에서 **[!UICONTROL Catalog]** > **[!UICONTROL Products]**(으)로 이동합니다.

1. 소스를 수정할 제품을 선택합니다.

   제품을 찾아보거나 검색하여 찾은 후 해당 확인란을 선택합니다.

1. 맨 위에 있는 **[!UICONTROL Actions]** 메뉴를 클릭하고 **[!UICONTROL Assign Inventory Source]**&#x200B;을(를) 선택합니다.

1. 확인 대화 상자에서 **[!UICONTROL OK]**&#x200B;을(를) 클릭합니다.

1. 제품에 추가할 모든 소스에 대해 확인란을 선택합니다.

1. **[!UICONTROL Assign Sources]**&#x200B;을(를) 클릭합니다.

   ![소스를 추가할 제품 선택](assets/inventory-bulk-assign-sources-summary.png){width="600" zoomable="yes"}

소스는 재고 수량이 0인 제품에 추가됩니다. 소스당 [재고 수량](quantities-assign-per-product.md)을 추가할 수 있습니다.

## 출처 및 수량 지정 취소

제품에서 출처의 지정을 취소할 때 해당 위치에 더 이상 제품이 입고되지 않음을 나타냅니다. 이 프로세스는 현재 제품에 지정된 소스에 대한 모든 재고 데이터를 완전히 지웁니다. 기존 인벤토리를 새 위치로 이동하려면 _인벤토리 전송_ 옵션을 사용하는 것이 좋습니다.

{{$include /help/_includes/unassign-source.md}}

출처를 제거하기 전에 해당 제품에 대한 모든 주문 및 출하를 완료하는 것이 좋습니다.

![선택한 제품에 대한 소스 할당 해제](assets/inventory-bulk-unassign-sources.gif)

1. _관리자_ 사이드바에서 **[!UICONTROL Catalog]** > **[!UICONTROL Products]**(으)로 이동합니다.

1. 소스를 수정할 제품을 선택합니다.

   제품을 찾아보거나 검색하여 찾은 후 해당 확인란을 선택합니다.

1. 맨 위에 있는 **[!UICONTROL Actions]** 메뉴를 클릭하고 **[!UICONTROL Unassign Inventory Source]**&#x200B;을(를) 선택합니다.

1. 확인 대화 상자에서 **[!UICONTROL OK]**&#x200B;을(를) 클릭합니다.

1. 제품에서 제거할 소스를 선택합니다.

   이 페이지에는 지정을 취소하면 제품에서 모든 특정 출처 및 수량 데이터가 제거된다는 경고가 표시됩니다.

1. **[!UICONTROL Unassign Sources]**&#x200B;을(를) 클릭합니다.

   ![선택한 제품에서 소스 제거](assets/inventory-bulk-unassign-sources-summary.png){width="600" zoomable="yes"}

<!-- Last updated from includes: 2022-08-30 15:36:09 -->
