---
title: 회사 계층 관리
description: 복잡한 운영 모델을 사용하는 B2B 조직을 지원하기 위해 회사 계층을 구축하고 관리합니다.
feature: B2B, Companies
role: Admin
hide: false
hidefromtoc: false
exl-id: a277ed95-7935-4d27-adb2-35116972732b
source-git-commit: 10b01db562777ef2fcc224177d7a83c0a6fc90e7
workflow-type: tm+mt
source-wordcount: '398'
ht-degree: 0%

---

# 관리 [!UICONTROL Company Hierarchy]

[!BADGE 1.5.0-베타]{type=Informative url="/help/b2b/release-notes.md" tooltip="Beta 프로그램 참가자만 사용 가능"}

관리자는 다음을 빌드할 수 있습니다. [!UICONTROL Company Hierarchy] 지정된 모회사에 관계회사를 배정하여 조직계층 상위에 있는 회사이다.

기존 회사에 할당되지 않은 회사를 편집하여 상위 회사 만들기 [!UICONTROL Company Hierarchy]및 관련 회사 할당

![회사 계층 구조 표](./assets/company-detail-view.png){width="700"}

회사가 계층에 지정된 후 [!UICONTROL Company type] 열의 **회사** 그리드는 회사를 다음으로 식별합니다. `Parent` 또는  `Child` 회사.  다음과 같은 경우 [!UICONTROL Company Type] 은(는) `Company`는 회사가 회사 계층의 일부가 아니며 상위 회사가 되거나 기존 상위 회사에 할당될 수 있습니다.

>[!NOTE]
>
>에 대한 자세한 내용은 [!UICONTROL Company Hierarchy] 표, 참조 [회사 계층](account-company-create.md#company-hierarchy) 필드 설명.

관리에서 회사를 편집한 다음 를 사용하여 회사 할당을 관리합니다. [!UICONTROL Company Hierarchy] 의 섹션 [!UICONTROL Company] 회사를 할당하거나 할당을 취소할 페이지입니다.

## 상위 회사에 회사 할당

1. 다음에서 _관리자_ 사이드바, 다음 위치로 이동 **[!UICONTROL Customers]** > **[!UICONTROL Companies]**.

   ![회사 그리드](./assets/companies-grid-view.png){width="700" zoomable="yes"}

1. 회사 그리드에서 회사 세부 정보 페이지를 열어 할당을 생성합니다.

   - 기존 상위 회사에 추가 회사를 할당하려면 다음을 선택합니다. **[!UICONTROL Edit]** 상위 회사에 대한 작업입니다.
   - 새 상위 회사를 만들려면 **[!UICONTROL Edit]** 상위로 지정된 회사에 대한 작업입니다.

     기존 상위 또는 하위 회사에서는 새 상위 회사를 만들 수 없습니다.

   ![새 회사](./assets/company-update.png){width="700" zoomable="yes"}

1. 회사 세부 정보 페이지에서 **[!UICONTROL Company Hierarchy]** 드롭다운, 선택 **[!UICONTROL Assign Companies]**.

   ![새 회사](./assets/company-hierarchy-grid.png){width="700" zoomable="yes"}

   이 뷰를 확장하면 기존 회사 할당이 있는 경우 이를 볼 수 있습니다. 상위 회사는 항상 _[!UICONTROL Company Hierarchy]_가 있는 격자 `current company indicator` 편집 중인 회사 줄에 표시됩니다.

1. 할당 가능한 회사가 그리드에 나열됩니다. 할당할 회사를 선택한 다음 을 선택합니다. **[!UICONTROL Assign Selected Companies]**.

1. 다음을 수행할 수 있습니다. **이 페이지에서 모두 선택** 또는 하나의 특정 회사 라인 항목을 클릭하고 **[!UICONTROL Assign Selected Companies]**.

   ![새 회사](./assets/assign-selected-companies.png){width="700" zoomable="yes"}

1. 메시지가 표시되면 다음을 선택하여 회사 할당을 완료합니다. **[!UICONTROL Assign]**.

## 상위 회사에서 회사 할당 해제

1. 다음에서 _관리자_ 사이드바, 다음 위치로 이동 **[!UICONTROL Customers]** > **[!UICONTROL Companies]**.

   ![회사 그리드](./assets/companies-grid-view.png){width="700" zoomable="yes"}

1. 회사 페이지에서 다음을 선택하여 상위 회사에 대한 회사 세부 정보 페이지를 엽니다. **[!UICONTROL Edit]** 작업.

   ![새 회사](./assets/company-update.png){width="700" zoomable="yes"}

1. 를 확장하여 할당된 회사 목록 보기 **[!UICONTROL Company Hierarchy]** 드롭다운입니다.

1. 회사 계층 그리드에서 다음을 선택하여 회사 할당을 취소합니다. **[!UICONTROL Select]** 회사에 대한 작업을 수행한 다음 선택 **[!UICONTROL Unassign from parent]**.

   ![새 회사](./assets/company-hierarchy-grid.png){width="700" zoomable="yes"}

1. 메시지가 표시되면 을 선택하여 지정된 회사를 계층에서 제거합니다. **[!UICONTROL Unassign]**.
