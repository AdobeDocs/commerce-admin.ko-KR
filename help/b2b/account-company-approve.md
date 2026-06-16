---
title: 회사 계정 승인
description: 관리자에서 회사 계정 요청을 승인하는 방법을 알아봅니다.
exl-id: c7123383-0e94-4d6c-be3c-b6ca84145a59
feature: B2B, Companies, Configuration
role: Admin, User
TQID: https://experienceleague.adobe.com/ZpDdYMYaSnG1lOwV22mmrkYjBvf90pUJVZxP2r526pw
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2:
  - id: d1e21356-0064-4f48-9089-16e3f0dbd2a6
  - id: dac87252-6066-4d6e-a9d2-f6d84c323de7
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2:
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 246
ht-degree: 0%

---

# 회사 계정 승인

스토어 관리자가 요청을 검토하고 승인 또는 거부할 때까지 회사 만들기 위해 상점 첫 화면에서 받은 요청의 상태는 `Pending Approval`입니다. 회사 계정의 상태는 다음 중 하나로 설정할 수 있습니다.

- [!UICONTROL Active]
- [!UICONTROL Pending Approval]
- [!UICONTROL Rejected]
- [!UICONTROL Blocked]

[작업 컨트롤](account-company-manage.md)을 사용하여 여러 회사 요청을 승인할 수도 있습니다.

![승인 보류 중](./assets/companies-pending-approval.png){width="700" zoomable="yes"}

## 보류 중인 회사 계정 승인

1. _관리자_ 사이드바에서 **[!UICONTROL Customers]** > **[!UICONTROL Companies]**(으)로 이동합니다.

   표 위에 있는 _[!UICONTROL Columns]_&#x200B;선택기를 사용하여&#x200B;**[!UICONTROL Status]**&#x200B;열을 표시할 수 있습니다.

1. _[!UICONTROL Action]_&#x200B;열에서&#x200B;**[!UICONTROL Edit]**&#x200B;을(를) 클릭합니다.

1. **[!UICONTROL Company Status]**&#x200B;을(를) `Active`(으)로 설정합니다.

   ![회사 상태 설정](./assets/company-status-active.png){width="700" zoomable="yes"}

1. 확인 메시지가 표시되면 **[!UICONTROL Change status]**&#x200B;을(를) 클릭합니다.

   회사 관리자는 회사가 현재 활성 상태라는 이메일 알림을 받습니다.

1. 해당하는 경우 **[!UICONTROL Sales Representative]**&#x200B;을(를) 특정 관리자 계정으로 설정하십시오.

1. **[!UICONTROL Account Information]** 섹션에서 ![확장 선택기](../assets/icon-display-expand.png)를 확장하고 **[!UICONTROL Comment]** 필드를 사용하여 계정에 대한 메모를 입력합니다.

   해당 댓글은 상점에서는 볼 수 없습니다.

1. 완료되면 **[!UICONTROL Save]**&#x200B;을(를) 클릭합니다.

   회사 계정이 승인되었다는 확인 이메일이 회사 및 회사 관리자에게 전송됩니다.

## 회사 상태

| 상태 | 설명 |
|------------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Active] | 회사는 승인되었으며 회사 관리자가 상점 앞에서 관리할 수 있습니다. |
| [!UICONTROL Pending Approval] | 상점 첫 화면에서 회사 계정 만들기 요청을 제출했지만 아직 검토되지 않았습니다. |
| [!UICONTROL Rejected] | 스토어 관리자가 회사 계정 만들기 요청을 거부했습니다. |
| [!UICONTROL Blocked] | 회사 계좌는 더 이상 상태가 좋지 않습니다. 고객은 상점에서 계정에 액세스할 수 있지만 구입할 수는 없습니다. |

{style="table-layout:auto"}
