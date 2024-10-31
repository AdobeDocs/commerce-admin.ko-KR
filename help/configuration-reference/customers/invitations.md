---
title: '[!UICONTROL Customers] &gt; [!UICONTROL Invitations]'
description: Commerce 관리자의 [!UICONTROL Customers] &gt; [!UICONTROL Invitations] 페이지에서 구성 설정을 검토하십시오.
exl-id: edafeaed-9c4f-4d9f-b35c-381ae5f43b67
feature: Configuration, Promotions/Events
source-git-commit: 5a4417373f6dc720e8e14f883c27348a475ec255
workflow-type: tm+mt
source-wordcount: '252'
ht-degree: 0%

---

# [!UICONTROL Customers] > [!UICONTROL Invitations]

{{ee-feature}}

{{config}}

## [!UICONTROL General]

![일반](./assets/invitations-general.png)<!-- zoom -->

<!-- [General](https://experienceleague.adobe.com/en/docs/commerce-admin/marketing/promotions/events/invitations#enable-invitations-for-your-store) -->

| 필드 | [범위](../../getting-started/websites-stores-views.md#scope-settings) | 설명 |
|--- |--- |--- |
| [!UICONTROL Enable Invitations Functionality] | 글로벌 | 초대 모듈의 사용 여부를 결정합니다. 옵션: `Yes` / `No` |
| [!UICONTROL Enable Invitations on Frontend] | 웹 사이트 | 상점 첫 화면에서 초대를 관리할 수 있는지 여부를 결정합니다. 옵션: `Yes` / `No` |
| [!UICONTROL Referred Customer Group] | 스토어 뷰 | 초대받은 사람의 고객 그룹을 결정합니다. 옵션: <br/>**`Same as Inviter`**- 초대된 사용자가 초대된 고객과 동일한 고객 그룹에 자동으로 할당됩니다.<br/>**`Default Customer Group from Configuration`** - 초대받은 사람에게 자동으로 기본 [고객 그룹](../../customers/customer-groups.md)이(가) 있습니다. |
| [!UICONTROL New Accounts Registration] | 스토어 뷰 | 초대받은 사람이 계정을 만드는 방법을 결정합니다. 옵션: <br/>**`By Invitation Only`**- 초대받은 사람이 계정을 만들려면 초대 전자 메일의 링크를 따라야 합니다.<br/>**`Available to All`** - 초대받은 사람은 스토어에서 사용할 수 있는 계정 등록 양식을 사용할 수 있습니다. |
| [!UICONTROL Allow Customers to Add Custom Message to Invitation Email] | 스토어 뷰 | 초대 양식에 초대자가 전자 메일을 통해 초대자에게 보내는 사용자 지정 메시지를 추가할 수 있는 필드가 있는지 여부를 결정합니다. 이는 초대에 메시지를 추가하는 관리자의 기능에 영향을 주지 않습니다. 옵션: `Yes` / `No`. |
| [!UICONTROL Max Invitations Allowed to be Sent at One Time] | 스토어 뷰 | 초대자가 한 번에 보낼 수 있는 최대 초대 수를 결정합니다. 초대가 양식에 포함된 각 이메일 주소로 다른 초대를 보냅니다. 이렇게 하면 대량의 초대가 한 번에 전송되지 않도록 하여 서버 리소스를 보호하고 초대가 스팸으로 전송될 가능성을 줄일 수 있습니다. |

{style="table-layout:auto"}

## [!UICONTROL Email]

![전자 메일](./assets/invitations-email.png)<!-- zoom -->

<!-- [Email](https://experienceleague.adobe.com/en/docs/commerce-admin/marketing/promotions/events/invitations#enable-invitations-for-your-store) -->

| 필드 | [범위](../../getting-started/websites-stores-views.md#scope-settings) | 설명 |
|--- |--- |--- |
| [!UICONTROL Customer Invitation Email Sender] | 스토어 뷰 | 초대 이메일을 보낼 때 초대인이 받는 이메일의 발신자를 결정합니다. 기본값: `General Contact` |
| [!UICONTROL Customer Invitation Email Template] | 스토어 뷰 | 초대 이메일을 보낼 때 초대받은 사람이 받는 전자 메일의 템플릿을 결정합니다. 기본 템플릿: `Customer Invitation` |

{style="table-layout:auto"}
