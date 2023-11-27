---
title: 회사 역할 및 권한
description: 회사 관리자가 회사 사용자에게 적용할 수 있는 역할 및 권한에 대해 알아보고, 주문 정보 및 리소스에 대한 다양한 수준의 액세스를 허용합니다.
exl-id: 9fe20d6a-2c9c-4618-a395-805d64dcf0de
feature: B2B, Companies, Roles/Permissions
role: Admin
source-git-commit: 03d1892799ca5021aad5c19fc9f2bb4f5da87c76
workflow-type: tm+mt
source-wordcount: '595'
ht-degree: 0%

---

# 회사 역할 및 권한

회사 사용자를 위한 역할은 판매 정보 및 리소스에 액세스할 수 있는 다양한 수준의 권한으로 설정됩니다. 기본적으로 회사 관리자는 _슈퍼 사용자_ 전체 사용 권한을 포함합니다. 다음 [액세스 거부됨](../content-design/pages.md#access-denied) 사용자에게 페이지에 액세스할 수 있는 권한이 없는 경우 페이지가 나타납니다.

![기본 역할이 있는 역할 및 권한 페이지](./assets/company-roles-permissions.png){width="700" zoomable="yes"}

시스템에는 사용자가 사용할 수 있는 사전 정의된 기본 사용자 역할이 있습니다. _있는 그대로_ 또는 필요에 맞게 수정합니다. 다음과 같이 회사 구조 및 조직 책임을 일치시키는 데 필요한 만큼 많은 역할을 만들 수 있습니다.

- **기본 사용자** — 기본 사용자는 판매 및 견적 관련 활동에 대한 전체 액세스 권한과 회사 프로필 및 신용 정보에 대한 보기 전용 액세스 권한을 갖습니다.

- **수석 구매자** — 선임 구매자는 모든 Sales 및 Quote 자원에 액세스할 수 있으며, 회사 프로필, 사용자 및 팀, 결제 정보, 회사 크레딧에 대한 보기 전용 권한을 가질 수 있습니다.

- **어시스턴트 바이어** — 보조 구매자는 다음을 사용하여 주문할 수 있는 권한을 가질 수 있습니다. _견적으로 체크아웃_&#x200B;및 을 사용하여 회사 프로필에서 주문, 견적 및 정보를 볼 수 있습니다.

## 역할 및 권한 관리

1. 회사 관리자가 스토어 계정에 로그인합니다.

1. 왼쪽 패널에서 을 선택합니다 **[!UICONTROL Roles and Permissions]**.

1. 다음 작업 중 하나를 완료합니다.

### 역할 만들기

1. 클릭수 **[!UICONTROL Add New Role]**.

   ![새 역할 추가](./assets/company-roles-permissions-add-storefront.png){width="600" zoomable="yes"}

1. 설명을 입력합니다. **[!UICONTROL Role Name]**.

1. 아래 _[!UICONTROL Role Permissions]_는 다음 중 하나를 수행합니다.

   - 역할을 할당한 사용자에게 액세스 권한이 있는 각 리소스 또는 활동의 확인란을 선택합니다.

   - 다음을 선택합니다. **[!UICONTROL All]** 확인란을 선택하고 역할에 할당된 사용자가 액세스할 권한이 없는 각 리소스 또는 활동의 확인란을 선택 취소합니다.

1. 클릭수 **[!UICONTROL Save Role]**.

1. 다음 단계를 반복하여 필요한 만큼 역할을 만듭니다.

### 역할 수정

1. 역할을 수정하려면 회사 관리자가 **[!UICONTROL Edit]** 다음에서 _[!UICONTROL Actions]_열.

1. 필요한 경우 이름 및 권한 설정을 변경합니다.

1. 완료되면 클릭 수 **[!UICONTROL Save Role]**.

### 역할 복제

1. 역할을 복제하려면 회사 관리자가 **[!UICONTROL Duplicate]** 다음에서 _[!UICONTROL Actions]_열.

1. 필요한 경우 이름 및 권한 설정을 변경합니다.

1. 완료되면 클릭 수 **[!UICONTROL Save Role]**.

### 역할 삭제

1. 회사 관리자가 역할 목록에서 삭제할 역할을 찾습니다.

   할당된 사용자가 없는 역할만 삭제할 수 있습니다.

1. 클릭수 **[!UICONTROL Delete]** 다음에서 _[!UICONTROL Actions]_열.

1. 확인 메시지가 표시되면 **[!UICONTROL OK]**.

## 작업

| 작업 | 설명 |
|-----------| ----------- |
| [!UICONTROL Duplicate] | 선택한 역할의 복사본을 만듭니다. 중복 역할의 이름입니다. `- Duplicated` 가 끝에 추가되었습니다. |
| [!UICONTROL Edit] | 이름 및/또는 권한 집합을 변경합니다. |
| [!UICONTROL Delete] | 역할을 삭제합니다. 할당된 사용자가 없는 역할만 삭제할 수 있습니다. |

{style="table-layout:auto"}

## 역할 권한

- 모두
   - 판매
      - 체크아웃 허용(주문)
         - 계정입금 방법 사용
      - 주문 보기
         - 하위 사용자의 주문 보기
- 따옴표
   - 보기
      - 요청, 편집, 삭제
      - 견적을 사용한 체크아웃
      - 하위 사용자의 견적 보기
- 주문 승인
   - 내 구매 주문 보기
      - 하위 항목에 대한 보기
      - 모든 회사에 대한 보기
   - 이 역할 내에서 생성된 PO 자동 승인
   - 다른 승인 없이 구매 발주 승인
   - 승인 규칙 보기
      - 만들기, 편집 및 삭제
- 회사 프로필
   - 계정 정보(보기)
      - 편집
   - 법적 주소
      - 편집
   - 연락처(보기)
   - 결제 정보(조회)
   - 배송 정보(조회)
- 회사 사용자 관리
   - 역할 및 권한 보기
      - 역할 및 권한 관리
   - 사용자 및 팀 보기
      - 사용자 및 팀 관리
- 회사 신용
   - 보기

## 회사 사용자에게 역할 할당

필요한 역할을 정의한 후 회사 관리자가 각 회사 사용자에게 역할을 할당합니다.

1. 회사 관리자로 회사 계정에 로그인합니다.

1. 왼쪽 패널에서 을 선택합니다 **[!UICONTROL Company Users]**.

   ![회사 사용자](./assets/company-users-list-storefront.png){width="700" zoomable="yes"}

1. 목록에서 사용자를 찾고 를 클릭합니다. **[!UICONTROL Edit]**.

1. 적절한 항목 선택 **[!UICONTROL User Role]** 사용자용입니다.

   ![사용자 편집 - 사용자 역할 선택](./assets/company-user-assign-role.png){width="700" zoomable="yes"}

1. 클릭수 **[!UICONTROL Save]**.
