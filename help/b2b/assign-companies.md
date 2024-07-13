---
title: 회사 계층 관리
description: 회사 계층을 빌드하여 복잡한 운영 모델을 사용하는 B2B 조직을 관리하는 방법을 알아봅니다
feature: B2B, Companies
role: Admin
hide: false
hidefromtoc: false
exl-id: a277ed95-7935-4d27-adb2-35116972732b
source-git-commit: 582f15c422e43af9acec6313c7b777b3126030f8
workflow-type: tm+mt
source-wordcount: '327'
ht-degree: 0%

---

# [!UICONTROL Company Hierarchy] 관리

[!BADGE 1.5.0-베타]{type=Informative url="/help/b2b/release-notes.md" tooltip="Beta 프로그램 참가자만 사용 가능"}

관리자는 조직 상단에 있는 지정된 상위 회사에 관련 회사를 할당하여 [!UICONTROL Company Hierarchy]을(를) 만들 수 있습니다. [!UICONTROL Company Type]이(가) `Company`인 경우 회사는 조직의 일부가 아니며 상위 회사가 되거나 기존 상위 회사에 할당될 수 있습니다.

관리에서 회사를 편집한 다음 [!UICONTROL Company Hierarchy] 구성을 업데이트하여 회사를 할당하거나 할당 해제하여 회사 할당을 관리합니다.

![회사 계층 구조 표](./assets/company-detail-hierarchy-current-flag.png){width="700"}

>[!NOTE]
>
>[!UICONTROL Company Hierarchy] 표에 대한 자세한 내용은 [회사 계층 구조](account-company-create.md#company-hierarchy) 필드 설명을 참조하십시오.

## 조직에 회사 할당

1. _관리자_ 사이드바에서 **[!UICONTROL Customers]** > **[!UICONTROL Companies]**(으)로 이동합니다.

   ![회사 표](./assets/companies-grid-view.png){width="700" zoomable="yes"}

1. [!UICONTROL Companies] 그리드에서 회사 세부 정보 페이지를 열어 할당을 만듭니다.

   - 기존 상위 회사에 추가 회사를 할당하려면 상위 회사에 대해 **[!UICONTROL Edit]** 작업을 선택하십시오.
   - 상위 회사를 만들려면 회사가 상위로 지정할 **[!UICONTROL Edit]** 작업을 선택하십시오.

     기존 상위 또는 하위 회사에서는 상위 회사를 만들 수 없습니다.

1. 회사 세부 정보 페이지에서 **[!UICONTROL Company Hierarchy]**&#x200B;을(를) 확장합니다.

   ![회사 계층 구조 표](./assets/company-detail-hierarchy-current-flag.png){width="700" zoomable="yes"}

   기존 회사 할당이 있는 경우 표에 표시됩니다. 상위 회사는 항상 [!UICONTROL Company Hierarchy] 표의 맨 위에 위치합니다. `[!UICONTROL Current]` 플래그는 편집 중인 회사를 나타냅니다.

1. 상위 조직에 회사를 추가합니다.

   - **[!UICONTROL Assign Companies]**&#x200B;을(를) 선택하여 사용 가능한 회사 목록 중에서 선택합니다.

   - **이 페이지에서 모두 선택** 또는 하나 이상의 특정 회사 라인 항목을 선택하십시오.

   - **[!UICONTROL Assign Selected Companies]**&#x200B;을(를) 선택합니다.

   - **[!UICONTROL Assign]**&#x200B;을(를) 선택하여 회사 할당을 완료합니다.

     ![조직에 회사 할당](./assets/assign-selected-companies-hierarchy.png){width="675" zoomable="yes"}

## 상위 회사에서 회사 할당 해제

1. _관리자_ 사이드바에서 **[!UICONTROL Customers]** > **[!UICONTROL Companies]**(으)로 이동합니다.

   ![회사 표](./assets/companies-grid-view.png){width="700" zoomable="yes"}

1. [!UICONTROL Companies] 그리드에서 **[!UICONTROL Edit]**&#x200B;을(를) 선택하여 상위 회사에 대한 회사 세부 정보 페이지를 엽니다.

1. **[!UICONTROL Company Hierarchy]**&#x200B;을(를) 확장하여 할당된 회사 목록을 봅니다.

1. [!UICONTROL Company Hierarchy] 그리드에서 **[!UICONTROL Select]** 작업 컨트롤을 사용하여 회사 할당을 취소하여 **[!UICONTROL Unassign from parent]**&#x200B;을(를) 선택하십시오.

   ![상위 조직에서 회사 할당 해제](./assets/company-hierarchy-grid-unassign.png){width="700" zoomable="yes"}

1. 메시지가 표시되면 **[!UICONTROL Unassign]**&#x200B;을(를) 선택하여 계층에서 할당된 회사를 제거합니다.
