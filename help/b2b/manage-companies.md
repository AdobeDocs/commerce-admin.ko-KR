---
title: 회사 경영
description: 복잡한 운영 모델을 통해 B2B 조직의 관리 및 관리를 간소화합니다.
feature: B2B, Companies, Storefront
role: Admin
hide: false
hidefromtoc: false
exl-id: 8246be3d-ff9f-4f9f-875d-1b999befc534
source-git-commit: 582f15c422e43af9acec6313c7b777b3126030f8
workflow-type: tm+mt
source-wordcount: '276'
ht-degree: 0%

---

# 회사 경영

[!BADGE 1.5.0-베타]{type=Informative url="/help/b2b/release-notes.md" tooltip="Beta 프로그램 참가자만 사용 가능"}

회사 관리는 복잡한 조직 구조를 가진 회사의 업무 운영을 간소화합니다. 관리자는 지정된 상위 회사에 회사를 할당하여 B2B 조직을 미러링하는 회사 계층을 구축할 수 있습니다. 이 할당을 통해 상위 회사 관리자가 조직 내의 회사를 보고 관리할 수 있습니다.

에서 회사 관리 작업 시작 *[!UICONTROL Companies]* 보기. 관리에서 로 이동합니다.  **[!UICONTROL Customers]** > **[!UICONTROL Companies]**.

![B2B 회사 관리 그리드](./assets/companies-grid-view.png){width="700" zoomable="yes"}

다음에서 *[!UICONTROL Companies grid]*, *[!UICONTROL Company Type]* 회사가 조직의 일부로 관리되는지 또는 별도의 회사로 관리되는지 여부를 나타냅니다.

- `Parent` 하나 이상의 지정된 회사가 있는 비즈니스 조직입니다. 상위 회사는 다른 회사의 하위 회사로 할당할 수 없습니다.

- `Child` 는 조직에 지정된 회사입니다. 회사는 하나의 모회사에만 할당할 수 있습니다.

- `Company` 는 단일 회사를 나타냅니다. 단일 회사는 모회사로 만들거나 기존 모회사에 할당하여 조직에 속할 수 있습니다.

상위 또는 하위 회사를 편집할 때 다음을 확장합니다. *[!UICONTROL Company Hierarchy]* 조직의 모든 회사를 봅니다. A `Current` 편집 중인 회사를 나타내는 플래그입니다.

![B2B 회사 계층 구조 표](./assets/company-detail-hierarchy-current-flag.png){width="700" zoomable="yes"}


## 보기 및 구성 [!UICONTROL Company Hierarchy]

초기 회사 생성 시 [!UICONTROL Company Hierarchy] 그리드가 비어 있습니다. 회사가 단일 회사인 경우에도 공허하다.

![B2B 회사 계층 구조 표](./assets/company-hierarchy-grid.png){width="700" zoomable="yes"}

상위 회사의 경우 적절한 권한이 있는 관리자는 다음 작업을 완료할 수 있습니다.

- 새 상위 조직을 만들거나 기존 상위 조직을 업데이트하여 회사 계층을 구축합니다.
- 회사를 추가하거나 제거할 기존 조직을 관리합니다.

자세한 내용은 [회사 계층 관리](assign-companies.md).
