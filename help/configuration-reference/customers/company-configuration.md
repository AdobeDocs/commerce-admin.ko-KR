---
title: '[!UICONTROL Customers] &gt; [!UICONTROL Company Configuration]'
description: Commerce 관리자의 [!UICONTROL Customers] &gt; [!UICONTROL Company Configuration] 페이지에서 구성 설정을 검토하십시오.
exl-id: 330eabeb-edab-4a9f-968e-37d0b95cdedb
feature: Configuration, Companies
source-git-commit: 61df9a4bcfaf09491ae2d353478ceb281082fa74
workflow-type: tm+mt
source-wordcount: '837'
ht-degree: 0%

---

# [!UICONTROL Customers] > [!UICONTROL Company Configuration]

{{b2b-feature}}

{{config}}

>[!TIP]
>
>Adobe Commerce B2B를 설치하고 활성화하면 회사별 기능을 사용하여 구매 경험을 개인화할 수 있습니다. Adobe Commerce B2B는 B2B 및 B2C 모델을 모두 지원하는 통합 솔루션입니다. B2B 기능에 대한 자세한 내용은 [Adobe Commerce B2B 사용 안내서](https://experienceleague.adobe.com/docs/commerce-admin/b2b/introduction.html?lang=ko)를 참조하십시오.

>[!NOTE]
>
>B2B 기능에 대한 이러한 구성 옵션에 대한 액세스는 [역할 리소스](../../systems/permissions-user-roles.md#role-resources)에 의해 제어됩니다. 이러한 역할 리소스는 관리자 사용자에게 할당된 사용자 역할에 대해 설정해야 합니다.

이러한 설정 구성에 대한 자세한 내용은 _Adobe Commerce B2B 사용 안내서_&#x200B;의 [기본 B2B 기능 사용](../../b2b/enable-basic-features.md)을 참조하세요.

## [!UICONTROL General]

![일반](./assets/company-general.png)<!-- zoom -->

| 필드 | [범위](../../getting-started/websites-stores-views.md#scope-settings) | 설명 |
|--- |--- |--- |
| [!UICONTROL Allow Company Registration from the Storefront] | 웹 사이트 | 스토어 방문자가 회사 계정 또는 개인 계정에 대해 [등록](../../customers/customer-sign-in.md)할 수 있는지 여부를 결정합니다. 옵션: `Yes` / `No` |

{style="table-layout:auto"}

## [!UICONTROL Email Options - Company Registration]

![전자 메일 옵션 - 회사 등록](./assets/company-email-options-company-registration.png)<!-- zoom -->

| 필드 | [범위](../../getting-started/websites-stores-views.md#scope-settings) | 설명 |
|--- |--- |--- |
| [!UICONTROL Company Registration Email Recipient] | 스토어 뷰 | 상점에서 회사 등록 요청이 제출되면 알려 주는 상점 연락처. 옵션: `General Contact` / `Sales Representative` / `Customer Support` / `Custom Email 1` / `Custom Email 2` |
| [!UICONTROL Send Company Registration Email Copy To] | 스토어 뷰 | 등록 알림 사본을 받을 각 사용자의 이메일 주소. 여러 이메일 주소는 쉼표로 구분합니다. |
| [!UICONTROL Send Email Copy Method] | 스토어 뷰 | 등록 이메일 사본을 전송하는 데 사용되는 이메일 메서드입니다. 옵션: `Bcc` / `Separate Email` |
| [!UICONTROL Default Company Registration Email] | 스토어 뷰 | 회사 등록 알림에 기본적으로 사용되는 이메일 템플릿입니다. 기본 템플릿: `Company Registration Request` |

{style="table-layout:auto"}

## [!UICONTROL Customer-Related Emails]

![고객 관련 전자 메일](./assets/company-email-options-customer-related-emails.png)<!-- zoom -->

| 필드 | [범위](../../getting-started/websites-stores-views.md#scope-settings) | 설명 |
|--- |--- |--- |
| [!UICONTROL Default 'Sales Rep Assigned' Email] | 스토어 뷰 | 영업 사원이 회사 계정에 할당된 경우 기본적으로 사용되는 이메일 템플릿입니다. 이 이메일은 영업 사원과 회사 관리자에게 발송됩니다. 기본 템플릿: `Sales Representative Assigned to Company` |
| [!UICONTROL Default 'Assign Company to Customer' Email] | 스토어 뷰 | 개별 고객 계정이 회사 계정에 할당될 때 기본적으로 사용되는 이메일 템플릿입니다. 이 이메일은 고객에게만 전송됩니다. 기본 템플릿: `Assign Company to Customer` |
| [!UICONTROL Default 'Assign Company Admin' Email] | 스토어 뷰 | 회사 관리자가 회사에 할당된 경우 사용되는 이메일 템플릿입니다. 이 이메일은 영업 사원과 회사 관리자에게 발송됩니다. 기본 템플릿: `Assign Company Admin` |
| [!UICONTROL Default 'Company Admin Inactive' Email] | 스토어 뷰 | 회사 관리자로 사용되는 사람의 상태가 &quot;비활성&quot;으로 변경될 때 기본적으로 사용되는 이메일 템플릿입니다. 변경 사항에 대한 이메일 알림이 새 회사 관리자와 이전 회사 관리자에게 전송됩니다. 기본 템플릿: `Company Admin Set Inactive` |
| [!UICONTROL Default 'Company Admin Changed to Member' Email] | 스토어 뷰 | 이전 회사 관리자가 회사 구성원이 될 때 기본적으로 사용되는 이메일 템플릿입니다. 이메일은 회사 구성원에게만 전송됩니다. 기본 템플릿: `Company Admin Changed to Member` |
| [!UICONTROL Default 'Customer Status Active' Email] | 스토어 뷰 | 고객 상태가 활성화될 때 기본적으로 사용되는 이메일 템플릿입니다. 이 이메일은 고객에게만 전송됩니다. 기본 템플릿: `Customer Status Active` |
| [!UICONTROL Default 'Customer Status Inactive' Email] | 스토어 뷰 | 고객의 상태가 비활성화될 때 기본적으로 사용되는 이메일 템플릿입니다. 이 이메일은 고객에게만 전송됩니다. 기본 템플릿: `Customer Status Inactive` |

{style="table-layout:auto"}

## [!UICONTROL Company Status Change]

![회사 상태 변경](./assets/company-email-options-company-status-change.png)<!-- zoom -->

| 필드 | [범위](../../getting-started/websites-stores-views.md#scope-settings) | 설명 |
|--- |--- |--- |
| [!UICONTROL Company Status Change Email Recipient] | 스토어 뷰 | 회사 상태가 변경될 때마다 알림을 받는 스토어 연락처. 옵션: `General Contact` / `Sales Representative` / `Customer Support` / `Custom Email 1` / `Custom Email 2` |
| [!UICONTROL Send Company Status Change Email Copy To] | 스토어 뷰 | 회사 상태 변경 알림의 사본을 받을 각 사용자의 이메일 주소. 여러 이메일 주소는 쉼표로 구분합니다. |
| [!UICONTROL Send Email Copy Method] | 스토어 뷰 | 상태 변경 알림의 복사본을 보내는 데 사용되는 이메일 메서드입니다. 옵션: `Bcc` / `Separate Email` |
| [!UICONTROL Default "Company Status Change to Active 1' Email] | 스토어 뷰 | 회사 상태가 _승인 보류 중_&#x200B;에서 _활성_(으)로 변경될 때 사용되는 전자 메일 템플릿입니다. 기본 템플릿: `Company Status Active 1` |
| [!UICONTROL Default 'Company Status Change to Active 2' Email] | 스토어 뷰 | 회사 상태가 _거부됨_ 또는 _차단됨_&#x200B;에서 _활성_(으)로 변경될 때 기본적으로 사용되는 전자 메일 템플릿입니다. 기본 템플릿: `Company Status Active 2` |
| [!UICONTROL Default 'Company Status Change to Rejected' Email] | 스토어 뷰 | 회사 상태가 _거부됨_(으)로 변경될 때 기본적으로 사용되는 전자 메일 템플릿입니다. 기본 템플릿: `Company Status Rejected` |
| [!UICONTROL Default 'Company Status Change to Blocked' Email] | 스토어 뷰 | 회사 상태가 _차단됨_(으)로 변경될 때 기본적으로 사용되는 전자 메일 템플릿입니다. 기본 템플릿: `Company Status Blocked` |
| [!UICONTROL Default 'Company Status Change to Pending Approval' Email] | 스토어 뷰 | 회사 상태가 _승인 보류 중_(으)로 변경될 때 기본적으로 사용되는 전자 메일 템플릿입니다. 기본 템플릿: `Company Status Pending Approval` |

{style="table-layout:auto"}

## [!UICONTROL Company Credit]

![회사 크레딧](./assets/company-email-options-company-credit.png)<!-- zoom -->

| 필드 | [범위](../../getting-started/websites-stores-views.md#scope-settings) | 설명 |
|--- |--- |--- |
| [!UICONTROL Company Credit Change Email Sender] | 스토어 뷰 | 회사 크레딧에 변경 사항이 있을 때마다 통지되는 스토어 연락처입니다. 옵션: `General Contact` / `Sales Representative` / `Customer Support` / `Custom Email 1` / `Custom Email 2` |
| [!UICONTROL Send Company Credit Change Email Copy To] | 스토어 뷰 | 회사 크레딧 변경 알림의 사본을 받을 각 사람의 이메일 주소. 여러 이메일 주소는 쉼표로 구분합니다. |
| [!UICONTROL Send Email Copy Method] | 스토어 뷰 | 신용 변경 통지의 사본을 전송하는 데 사용되는 이메일 방법입니다. 옵션: `Bcc` / `Separate Email` |
| [!UICONTROL Allocated Email Template] | 스토어 뷰 | 회사 크레딧이 할당된 경우 기본적으로 사용되는 이메일 템플릿입니다. 이 이메일은 회사 관리자에게 전송됩니다. 기본 템플릿: `Credit Limit Allocated` |
| [!UICONTROL Updated Email Template] | 스토어 뷰 | 회사의 크레딧 제한이 업데이트될 때 기본적으로 사용되는 이메일 템플릿입니다. 이 이메일은 회사 관리자에게 전송됩니다. 기본 템플릿: `Credit Limit Updated` |
| [!UICONTROL Reimbursed Email Template] | 스토어 뷰 | 회사 크레딧에 [환급](../../b2b/credit-company.md#apply-a-payment-to-a-company-account)이 적용되는 경우 기본적으로 사용되는 전자 메일 템플릿입니다. 이 이메일은 회사 관리자에게 전송됩니다. 기본 템플릿: `Credit Reimbursed` |
| [!UICONTROL Refunded Email Template] | 스토어 뷰 | 주문 금액이 회사 크레딧으로 환불될 때 기본적으로 사용되는 이메일 템플릿입니다. 이 이메일은 회사 관리자에게 전송됩니다. 기본 템플릿: `Order Refunded to Company Credit` |
| [!UICONTROL Reverted Email Template] | 스토어 뷰 | 주문이 회사 크레딧으로 돌아갈 때 기본적으로 사용되는 이메일 템플릿입니다. 이 이메일은 회사 관리자에게 전송됩니다. 기본 템플릿: `Order Reverted to Company Credit` |

{style="table-layout:auto"}
