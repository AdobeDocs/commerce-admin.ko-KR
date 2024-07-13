---
title: 속성 집합
description: 속성을 그룹으로 구성하여 제품 레코드에서 표시되는 위치를 결정하는 방법을 알아봅니다.
exl-id: de0c5fa2-158c-44ff-b84d-e4904ed8aa7d
feature: Catalog Management, Products
source-git-commit: 01148770946a236ece2122be5a88b963a0f07d1f
workflow-type: tm+mt
source-wordcount: '376'
ht-degree: 0%

---

# 속성 집합

제품을 만들 때 첫 번째 단계 중 하나는 제품 레코드의 템플릿으로 사용되는 속성 세트를 선택하는 것입니다. 속성 세트는 데이터 입력 중에 사용할 수 있는 필드와 고객에게 표시되는 값을 결정합니다.

속성은 제품 레코드에서 표시되는 위치를 결정하는 그룹으로 구성됩니다. 스토어에는 일반적으로 사용되는 특성 집합을 포함하는 초기 특성 집합(_default_)이 있습니다. 일부 속성만 추가하려면 이 기본 속성 집합에 추가할 수 있습니다. 특정 유형의 정보가 필요한 제품을 판매하는 경우 제품에 필요한 특정 속성이 포함된 전용 속성 세트를 만드는 것이 좋습니다.

![특성 집합](./assets/attribute-sets.png){width="700" zoomable="yes"}

## 속성 집합 만들기

1. _관리자_ 사이드바에서 **[!UICONTROL Stores]** > _[!UICONTROL Attributes]_>**[!UICONTROL Attribute Set]**(으)로 이동합니다.

1. **[!UICONTROL Add New Set]**&#x200B;을(를) 클릭합니다.

   ![특성 집합 - 이름 편집](./assets/attribute-set-new.png){width="600" zoomable="yes"}

1. 특성 집합에 대한 **[!UICONTROL Name]**&#x200B;을(를) 입력하십시오.

1. **[!UICONTROL Based On]**&#x200B;을(를) 템플릿으로 사용할 기존 특성 집합으로 설정하십시오.

1. **[!UICONTROL Save]**&#x200B;을(를) 클릭합니다.

   다음 페이지에는 다음이 표시됩니다.

   - 왼쪽 열에는 속성 세트의 이름이 표시됩니다. 이름은 내부 참조용이며 필요에 따라 변경할 수 있습니다.
   - 페이지의 중앙에는 현재 선택된 속성 그룹이 나열됩니다.
   - 오른쪽 열에는 현재 속성 집합에 할당되지 않은 속성 선택 항목이 나열됩니다.

1. 집합에 특성을 추가하려면 **[!UICONTROL Unassigned Attributes]** 목록의 특성을 **[!UICONTROL Groups]** 열의 적절한 폴더로 끕니다.

   >[!NOTE]
   >
   >시스템 특성이 점으로 표시되어 _[!UICONTROL Groups]_목록에서 제거할 수 없습니다. 그러나 속성 세트의 다른 그룹으로 드래그할 수 있습니다.

1. 완료되면 **[!UICONTROL Save]**&#x200B;을(를) 클릭합니다.

![특성 집합 - 편집](./assets/attribute-set-edit.png){width="600" zoomable="yes"}

## 속성 그룹 만들기

1. 특성 집합의 _[!UICONTROL Groups]_열에서&#x200B;**[!UICONTROL Add New]**을(를) 클릭합니다.

1. 새 그룹의 **[!UICONTROL Name]**&#x200B;을(를) 입력하고 **[!UICONTROL OK]**&#x200B;을(를) 클릭합니다.

1. 다음 중 하나를 수행합니다.

   - **[!UICONTROL Unassigned Attributes]**&#x200B;을(를) 새 그룹으로 드래그합니다.
   - 다른 그룹의 속성을 새 그룹으로 드래그합니다.

   새 그룹은 속성 세트를 기반으로 하는 모든 제품에서 속성의 섹션이 됩니다.

## 속성 집합 삭제

1. _관리자_ 사이드바에서 **[!UICONTROL Stores]** > _[!UICONTROL Attributes]_>**[!UICONTROL Attribute Set]**(으)로 이동합니다.

1. 목록에서 속성 세트를 선택하고 편집 모드로 엽니다.

1. **[!UICONTROL Delete]**&#x200B;을(를) 클릭합니다.

1. 확인 메시지가 표시되면 **[!UICONTROL OK]**&#x200B;을(를) 클릭합니다.
