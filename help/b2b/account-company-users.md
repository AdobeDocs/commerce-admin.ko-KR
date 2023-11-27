---
title: 회사 사용자 계정 관리
description: 회사 사용자 계정과 연결된 회사 계정 내에서 작동하는 방법에 대해 알아봅니다.
exl-id: 36b55f61-e579-4eb8-8f67-0156221d378e
feature: B2B, Companies, User Account, Storefront
role: Admin, User
source-git-commit: 03d1892799ca5021aad5c19fc9f2bb4f5da87c76
workflow-type: tm+mt
source-wordcount: '390'
ht-degree: 0%

---

# 회사 사용자 계정 관리

회사 사용자는 회사 관리자에 의해 할당되며 의 책임자로부터 표시됩니다. _[!UICONTROL Customers]_고객 유형별 그리드,_[!UICONTROL Company User]_. 이러한 개인들은 일반적으로 스토어 서비스 및 리소스에 액세스할 수 있는 다양한 수준의 권한을 가진 구매자입니다.

회사 관리자가 먼저 [회사 구조](account-company-structure.md)를 누르고 필요에 따라 다음 작업을 완료합니다.

- 회사 사용자 만들기 및 팀에 사용자 할당

- 역할 및 권한 정의 및 역할에 사용자 할당

>[!IMPORTANT]
>
>회사 사용자는 회사 관리자만 추가, 편집 또는 제거할 수 있습니다. 사용자가 회사 구조에서 제거되었기 때문에 제거를 되돌릴 수 없습니다.

## 회사 사용자 추가

1. 상점에서 회사 관리자가 계정에 로그인합니다.

1. 왼쪽 패널에서 을 선택합니다 **[!UICONTROL Company Users]**.

   ![회사 사용자](./assets/company-users-list-storefront.png){width="700" zoomable="yes"}

1. 클릭수 **[!UICONTROL Add New User]** 및 은 다음을 수행합니다.

   - 다음을 입력합니다. **[!UICONTROL Job Title]** 새 사용자.

   - 적절한 항목 선택 **[!UICONTROL User Role]** 역할 및 권한이 정의된 경우. 그렇지 않으면 나중에 돌아와서 역할을 할당할 수 있습니다.

     ![새 사용자 추가](./assets/company-structure-users-add.png){width="700" zoomable="yes"}

   - 사용자의 필요에 따라 나머지 필드를 완료합니다.

      - **[!UICONTROL First Name]** 및 **[!UICONTROL Last Name]**
      - **[!UICONTROL Email]**
      - **[!UICONTROL Phone Number]**

   기본적으로 **[!UICONTROL Status]** 계정: `Active`.

1. 완료되면 클릭 수 **[!UICONTROL Save]**.

1. 필요한 만큼 회사 사용자를 만들려면 프로세스를 반복합니다.

   새 사용자가 회사 사용자 목록에 회사 관리자와 함께 표시됩니다.

첫 번째 주문 시 시간을 절약하기 위해 회사 관리자는 각 회사 사용자에게 기본 회사 청구 및 배송 주소를 추가하도록 알릴 수 있습니다 [주소록](../customers/account-dashboard-address-book.md).

## 회사 사용자 편집

1. 상점에서 회사 관리자가 계정에 로그인합니다.

1. 왼쪽 패널에서 을 선택합니다 **[!UICONTROL Company Users]**.

1. 업데이트할 사용자 레코드를 찾고 클릭합니다. **[!UICONTROL Edit]**.

1. 필요한 사항을 변경합니다.

1. 완료되면 클릭 수 **[!UICONTROL Save]**.

## 회사 사용자 제거

1. 상점에서 회사 관리자가 계정에 로그인합니다.

1. 왼쪽 패널에서 을 선택합니다 **[!UICONTROL Company Structure]**.

1. 회사 구조에서 회사 사용자를 선택합니다.

1. 클릭수 **[!UICONTROL Delete Selected]**.

   ![사용자 삭제](./assets/company-structure-delete-user.png){width="600" zoomable="yes"}

1. 확인 메시지가 표시되면 **[!UICONTROL Delete]**.

관리자에게는에 나열된 회사 사용자가 유지됩니다. [고객](../customers/customers-all.md) 격자선이지만 `Inactive` 상태.

## 필드 설명

| 필드 | 설명 |
|--------------|---------------|
| [!UICONTROL Job Title] | 회사 사용자의 직함입니다. |
| [!UICONTROL User Role] | 다음 [역할](account-company-roles-permissions.md) 회사 사용자에게 할당되었습니다. 옵션: `Default User` / (기타 역할) |
| [!UICONTROL First Name] | 회사 사용자의 이름입니다. |
| [!UICONTROL Last Name] | 회사 사용자의 성. |
| [!UICONTROL Email] | 회사 사용자의 이메일 주소입니다. |
| [!UICONTROL Phone Number] | 회사 사용자의 전화번호. |
| [!UICONTROL Status] | 회사 사용자 계정의 상태입니다. 옵션: `Active` / `Inactive` |

{style="table-layout:auto"}
