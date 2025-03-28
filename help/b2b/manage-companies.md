---
title: 회사 경영
description: 복잡한 운영 모델을 통해 B2B 조직의 관리 및 관리를 간소화합니다.
feature: B2B, Companies, Storefront
role: Admin
hide: false
hidefromtoc: false
exl-id: 8246be3d-ff9f-4f9f-875d-1b999befc534
source-git-commit: 6b06f52eb4ee8ca136a1c60fd6dc04a9ac96bbfa
workflow-type: tm+mt
source-wordcount: '313'
ht-degree: 0%

---

# 회사 경영

회사 관리는 복잡한 조직 구조를 가진 회사의 업무 운영을 간소화합니다. 관리자는 지정된 상위 회사에 회사를 할당하여 B2B 조직을 미러링하는 회사 계층을 구축할 수 있습니다. 이 할당을 통해 상위 회사 관리자가 조직 내의 회사를 보고 관리할 수 있습니다.

*[!UICONTROL Companies]* 보기에서 회사 관리 작업을 시작합니다. 관리자의 **[!UICONTROL Customers]** > **[!UICONTROL Companies]**(으)로 이동합니다.

![B2B 회사 표 관리](./assets/companies-grid-view.png){width="700" zoomable="yes"}

*[!UICONTROL Company Type]* 열은 회사가 조직의 일부로 관리되는지 아니면 별도의 회사로 관리되는지를 나타냅니다.

- `Parent`은(는) 하나 이상의 회사가 할당된 비즈니스 조직입니다. 상위 회사는 다른 회사의 하위 회사로 할당할 수 없습니다.

- `Child`은(는) 조직에 할당된 회사입니다. 회사는 하나의 모회사에만 할당할 수 있습니다.

- `Company`은(는) 단일 회사를 나타냅니다. 단일 회사는 모회사로 만들거나 기존 모회사에 할당하여 조직에 속할 수 있습니다.

상위 또는 하위 회사를 편집할 때 *[!UICONTROL Company Hierarchy]*&#x200B;을(를) 확장하여 조직의 모든 회사를 봅니다. `Current` 플래그는 편집 중인 회사를 나타냅니다.

![B2B 회사 계층 구조 표](./assets/company-detail-hierarchy-current-flag.png){width="700" zoomable="yes"}

## [!UICONTROL Company Hierarchy] 보기 및 구성

초기 회사 생성 시 *[!UICONTROL Company Hierarchy]* 그리드가 비어 있습니다. 회사가 단일 회사인 경우에도 공허하다.

![B2B 회사 계층 구조 표](./assets/company-hierarchy-grid.png){width="700" zoomable="yes"}

회사가 조직의 상위 회사이고 조직의 다른 회사 계정이 이미 Adobe Commerce에 구성된 경우 적절한 권한이 있는 관리자는 회사를 할당하고 *[!UICONTROL Company Hierarchy]* 그리드를 사용하여 다른 회사 관리 작업을 완료할 수 있습니다.

- 상위 회사와 연결된 모든 회사를 봅니다.
- 상위 회사 세부 정보 페이지에서 더 많은 회사를 조직에 지정합니다.
- *[!UICONTROL Unassign from parent]* 작업을 사용하여 조직에서 회사를 제거합니다.
- 여러 회사에 동일한 설정을 적용하려면 *[!UICONTROL Advanced Settings]* 구성을 업데이트하십시오.

자세한 지침은 [회사 계층 관리](manage-company-hierarchy.md)를 참조하십시오.

