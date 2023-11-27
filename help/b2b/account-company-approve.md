---
title: 회사 계정 승인
description: 관리자에서 회사 계정 요청을 승인하는 방법을 알아봅니다.
exl-id: c7123383-0e94-4d6c-be3c-b6ca84145a59
feature: B2B, Companies, Configuration
role: Admin, User
source-git-commit: 2b86fe55f980c22839de10ecc4c9023034eb9ea1
workflow-type: tm+mt
source-wordcount: '246'
ht-degree: 0%

---

# 회사 계정 승인

회사 만들기를 위해 상점 첫 화면에서 받은 요청의 상태는 다음과 같습니다. `Pending Approval` 스토어 관리자가 요청을 검토하고 승인 또는 거부할 때까지. 회사 계정의 상태는 다음 중 하나로 설정할 수 있습니다.

- [!UICONTROL Active]
- [!UICONTROL Pending Approval]
- [!UICONTROL Rejected]
- [!UICONTROL Blocked]

다음을 사용할 수도 있습니다 [작업 제어](account-company-manage.md) 여러 회사 요청을 승인하려면 다음을 수행하십시오.

![승인 보류 중](./assets/companies-pending-approval.png){width="700" zoomable="yes"}

## 보류 중인 회사 계정 승인

1. 다음에서 _관리자_ 사이드바, 이동 **[!UICONTROL Customers]** > **[!UICONTROL Companies]**.

   다음을 사용할 수 있습니다. _[!UICONTROL Columns]_표 위에 선택기를 사용하여&#x200B;**[!UICONTROL Status]**열.

1. 다음에서 _[!UICONTROL Action]_열, 클릭&#x200B;**[!UICONTROL Edit]**.

1. 설정 **[!UICONTROL Company Status]** 끝 `Active`.

   ![회사 상태 설정](./assets/company-status-active.png){width="700" zoomable="yes"}

1. 확인을 묻는 메시지가 나타나면 **[!UICONTROL Change status]**.

   회사 관리자는 회사가 현재 활성 상태라는 이메일 알림을 받습니다.

1. 해당하는 경우 다음을 설정합니다. **[!UICONTROL Sales Representative]** 특정 관리자 계정으로.

1. 확장 ![확장 선택기](../assets/icon-display-expand.png)  다음 **[!UICONTROL Account Information]** 섹션 및 사용 **[!UICONTROL Comment]** 계정에 대한 메모를 입력하는 필드입니다.

   해당 댓글은 상점에서는 볼 수 없습니다.

1. 완료되면 다음을 클릭하십시오. **[!UICONTROL Save]**.

   회사 계정이 승인되었다는 확인 이메일이 회사 및 회사 관리자에게 전송됩니다.

## 회사 상태

| 상태 | 설명 |
|------------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Active] | 회사는 승인되었으며 회사 관리자가 상점 앞에서 관리할 수 있습니다. |
| [!UICONTROL Pending Approval] | 상점 첫 화면에서 회사 계정 만들기 요청을 제출했지만 아직 검토되지 않았습니다. |
| [!UICONTROL Rejected] | 스토어 관리자가 회사 계정 만들기 요청을 거부했습니다. |
| [!UICONTROL Blocked] | 회사 계좌는 더 이상 상태가 좋지 않습니다. 고객은 상점에서 계정에 액세스할 수 있지만 구입할 수는 없습니다. |

{style="table-layout:auto"}
