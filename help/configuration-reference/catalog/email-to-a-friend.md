---
title: '[!UICONTROL Catalog] &gt; [!UICONTROL Email to a Friend]'
description: Commerce 관리자의 [!UICONTROL Catalog] &gt; [!UICONTROL Email to a Friend] 페이지에서 구성 설정을 검토하십시오.
exl-id: cd1e3a8d-14ce-47e9-a3bc-c1b1dcbe0d8c
feature: Configuration, Communications
source-git-commit: 5a4417373f6dc720e8e14f883c27348a475ec255
workflow-type: tm+mt
source-wordcount: '173'
ht-degree: 0%

---

# [!UICONTROL Catalog] > [!UICONTROL Email to a Friend]

{{config}}

## [!UICONTROL Email Templates]

![전자 메일 템플릿](./assets/email-to-a-friend-email-templates.png)<!-- zoom -->

<!-- [Email Templates](https://experienceleague.adobe.com/en/docs/commerce-admin/systems/communications/email-templates#configure-email-templates) -->

| 필드 | [범위](../../getting-started/websites-stores-views.md#scope-settings) | 설명 |
|--- |--- |--- |
| [!UICONTROL Enabled] | 스토어 뷰 | 고객이 스토어의 제품에 대해 친구에게 이메일을 보낼 수 있는 프로세스를 활성화합니다. 옵션: `Yes` / `No` |
| [!UICONTROL Select Email Template] | 스토어 뷰 | _친구에게 전자 메일 보내기_ 기능을 통해 생성된 메시지에 사용되는 전자 메일 서식 파일을 식별합니다. 기본 템플릿: `Send Product to Friend` |
| [!UICONTROL Allow for Guests] | 스토어 뷰 | 보낸 사람이 등록된 고객이어야 친구들에게 제품에 대한 이메일을 보낼 수 있는지 여부를 결정합니다. 옵션: `Yes` / `No` |
| [!UICONTROL Max Recipients] | 스토어 뷰 | 단일 이메일의 배포 목록에 포함될 수 있는 사람 수를 제한합니다. |
| [!UICONTROL Max Products Sent in 1  Hour] | 스토어 뷰 | 한 시간 동안 한 명의 사용자가 공유할 수 있는 제품 수를 제한합니다. |
| [!UICONTROL Limit Sending By] | 스토어 뷰 | 보낸 사람을 식별하는 데 사용되는 방법을 결정합니다. 옵션은 다음과 같습니다. <br/>**`IP Address`**- (권장) 제품 전자 메일을 보내는 데 사용되는 컴퓨터의 IP 주소로 보낸 사람을 식별합니다.<br/>**`Cookie (unsafe)`** - 브라우저 쿠키로 보낸 사람을 식별합니다. 사용자는 제한을 피하기 위해 쿠키를 삭제할 수 있으므로 이 방법은 안전하지 않습니다. |

{style="table-layout:auto"}
