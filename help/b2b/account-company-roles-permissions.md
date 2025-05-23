---
title: 회사 역할 및 권한
description: 회사 관리자가 회사 사용자에게 적용할 수 있는 역할 및 권한에 대해 알아보고, 주문 정보 및 리소스에 대한 다양한 수준의 액세스를 허용합니다.
exl-id: 9fe20d6a-2c9c-4618-a395-805d64dcf0de
feature: B2B, Companies, Roles/Permissions
role: Admin
source-git-commit: bad59798a1a6d97826dc421fe8614ef511e067bd
workflow-type: tm+mt
source-wordcount: '521'
ht-degree: 0%

---

# 회사 역할 및 권한

회사 사용자를 위한 역할은 판매 정보 및 리소스에 액세스할 수 있는 다양한 수준의 권한으로 설정됩니다. 기본적으로 회사 관리자는 전체 권한이 있는 _슈퍼 사용자_&#x200B;입니다. 사용자에게 페이지에 액세스할 수 있는 권한이 없는 경우 [액세스 거부됨](../content-design/pages.md#access-denied) 페이지가 나타납니다.

![기본 역할을 가진 역할 및 권한 페이지](./assets/company-roles-permissions.png){width="700" zoomable="yes"}

시스템에 사전 정의된 기본 사용자 역할이 하나 있습니다. 이 역할은 _있는 그대로_&#x200B;를 사용하거나 필요에 맞게 수정할 수 있습니다. 다음과 같이 회사 구조 및 조직 책임을 일치시키는 데 필요한 만큼 많은 역할을 만들 수 있습니다.

- **기본 사용자** - 기본 사용자는 판매 및 견적 관련 활동에 대한 전체 액세스 권한과 회사 프로필 및 신용 정보에 대한 보기 전용 액세스 권한을 갖습니다.

- **수석 구매자** — 선임 구매자는 모든 판매 및 견적 리소스에 액세스할 수 있으며 회사 프로필, 사용자 및 팀, 결제 정보, 회사 크레딧에 대한 보기 전용 권한을 가질 수 있습니다.

- **보조 구매자** — 보조 구매자는 _견적을 사용한 체크아웃_&#x200B;을 사용하여 주문하고 회사 프로필에서 주문, 견적 및 정보를 볼 수 있는 권한이 있을 수 있습니다.

## 역할 및 권한 관리

1. 회사 관리자가 스토어 계정에 로그인합니다.

1. 왼쪽 패널에서 **[!UICONTROL Roles and Permissions]**&#x200B;을(를) 선택합니다.

1. 다음 작업 중 하나를 완료합니다.

### 역할 만들기

1. **[!UICONTROL Add New Role]**&#x200B;을(를) 클릭합니다.

   ![새 역할 추가](./assets/company-roles-permissions-add-storefront.png){width="600" zoomable="yes"}

1. 설명 **[!UICONTROL Role Name]**&#x200B;을(를) 입력합니다.

1. _[!UICONTROL Role Permissions]_&#x200B;에서 다음 중 하나를 수행합니다.

   - 역할을 할당한 사용자에게 액세스 권한이 있는 각 리소스 또는 활동의 확인란을 선택합니다.

   - **[!UICONTROL All]** 확인란을 선택하고 역할에 할당된 사용자가 액세스할 수 있는 권한이 없는 각 리소스 또는 활동의 확인란을 선택 취소합니다.

1. **[!UICONTROL Save Role]**&#x200B;을(를) 클릭합니다.

1. 다음 단계를 반복하여 필요한 만큼 역할을 만듭니다.

### 역할 수정

1. 역할을 수정하려면 회사 관리자가 _[!UICONTROL Actions]_&#x200B;열에서&#x200B;**[!UICONTROL Edit]**&#x200B;을(를) 클릭합니다.

1. 필요한 경우 이름 및 권한 설정을 변경합니다.

1. 완료되면 **[!UICONTROL Save Role]**&#x200B;을(를) 클릭합니다.

### 역할 복제

1. 역할을 복제하려면 회사 관리자가 _[!UICONTROL Actions]_&#x200B;열에서&#x200B;**[!UICONTROL Duplicate]**&#x200B;을(를) 클릭합니다.

1. 필요한 경우 이름 및 권한 설정을 변경합니다.

1. 완료되면 **[!UICONTROL Save Role]**&#x200B;을(를) 클릭합니다.

### 역할 삭제

1. 회사 관리자가 역할 목록에서 삭제할 역할을 찾습니다.

   할당된 사용자가 없는 역할만 삭제할 수 있습니다.

1. _[!UICONTROL Actions]_&#x200B;열에서&#x200B;**[!UICONTROL Delete]**&#x200B;을(를) 클릭합니다.

1. 확인 메시지가 표시되면 **[!UICONTROL OK]**&#x200B;을(를) 클릭합니다.

## 작업

| 작업 | 설명 |
|-----------| ----------- |
| [!UICONTROL Duplicate] | 선택한 역할의 복사본을 만듭니다. 중복 역할 이름에 끝에 `- Duplicated`이(가) 추가되었습니다. |
| [!UICONTROL Edit] | 이름 및/또는 권한 집합을 변경합니다. |
| [!UICONTROL Delete] | 역할을 삭제합니다. 할당된 사용자가 없는 역할만 삭제할 수 있습니다. |

{style="table-layout:auto"}

## 역할 권한

회사 관리자는 [!UICONTROL Edit action]을(를) 선택한 다음 **역할 권한** 목록에서 권한을 선택하거나 제거하여 역할에 대한 권한 구성을 업데이트할 수 있습니다.

![역할 및 권한 목록](./assets/role-permissions-list.png){width="700" zoomable="yes"}

## 회사 사용자에게 역할 할당

필요한 역할을 정의한 후 회사 관리자가 각 회사 사용자에게 역할을 할당합니다.

1. 회사 관리자로 회사 계정에 로그인합니다.

1. 왼쪽 패널에서 **[!UICONTROL Company Users]**&#x200B;을(를) 선택합니다.

   ![회사 사용자](./assets/company-users-list-storefront.png){width="700" zoomable="yes"}

1. 목록에서 사용자를 찾아 **[!UICONTROL Edit]**&#x200B;을(를) 클릭합니다.

1. 사용자에게 적절한 **[!UICONTROL User Role]**&#x200B;을(를) 선택합니다.

   ![사용자 편집 - 사용자 역할 선택](./assets/company-user-assign-role.png){width="700" zoomable="yes"}

1. **[!UICONTROL Save]**&#x200B;을(를) 클릭합니다.
