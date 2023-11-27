---
title: 이벤트 초대
description: 고객이 고객 계정의 대시보드에서 이벤트 및 개인 영업에 대한 초대를 보내고 보는 방법을 알아봅니다.
exl-id: 6a9123a0-bdb4-4cd6-99cd-658f728aa90c
feature: Promotions/Events, Communications
source-git-commit: eb0fe395020dbe2e2496aba13d2f5c2bf2d0fc27
workflow-type: tm+mt
source-wordcount: '633'
ht-degree: 0%

---

# 이벤트 초대

{{ee-feature}}

초대가 활성화되면 고객은 고객 계정의 대시보드에서 초대를 보내고 볼 수 있습니다. 초대 이메일에는 스토어의 고객 로그인 페이지에 대한 링크가 포함되어 있습니다.

## 내 초대

다음 _[!UICONTROL My Invitations]_고객 계정의 섹션에는 고객이 보낸 모든 초대가 나열됩니다. 고객은 상점 이벤트, 선물 등록, 위시리스트 등을 위해 친구 및 가족에게 초대장을 보낼 수 있습니다.

![내 초대](./assets/account-dashboard-my-invitations.png){width="700" zoomable="yes"}

### 초대 워크플로

1. **고객이 초대 준비**: 계정 대시보드에서 고객이 수신자 목록을 준비하고 초대를 완료합니다. 구성에 따라 사용자 지정 메시지를 포함할 수 있습니다.
1. **고객이 초대를 보냅니다.**: 준비가 되면 고객이 _[!UICONTROL Send Invitations]_단추를 클릭합니다.
1. **시스템에서 전송 관리**: 시스템에서 구성에 설정된 횟수에 따라 초대장을 일괄적으로 전송합니다.
1. **고객이 응답 모니터링**: 고객은 계정 대시보드에서 각 초대의 상태를 다음과 같이 모니터링합니다. `Sent`, `Accepted`, 또는 `Canceled`.

### 초대 보내기

1. 상점 앞에 있는 계정 사이드바에서 고객이 선택합니다. **[!UICONTROL My Invitations]**.

1. 다음에서 _내 초대_ 페이지, 클릭 수 **[!UICONTROL Send Invitation]**.

1. 새 초대 항목 정의:

   - 이메일 정보를 완료합니다.

   - (선택 사항) 다음을 클릭하여 다중 주소 초대를 만듭니다. **+** 다른 이메일 주소를 추가하는 중입니다.

     단일 초대에 5개의 이메일 주소 제한이 있습니다.

   - (선택 사항) 함께 제공되는 메시지를 입력합니다.

1. 완료되면 클릭 수 **[!UICONTROL Send Invitation]**.

초대 알림은 초대된 사용자의 이메일 주소로 전송되며 계정 설정에 대한 지침 링크가 있습니다.

>[!NOTE]
>
>사용자는 특정 이메일 주소에 하나의 초대장만 보낼 수 있습니다. 동일한 이메일 주소로 초대를 다시 보내려고 하면 오류 메시지가 표시되고 초대가 전송되지 않습니다.

## 스토어에 대한 초대 활성화

초대 구성은 스토어에 대한 초대를 활성화하고 전송 방법을 결정합니다.

1. 다음에서 _관리자_ 사이드바, 이동 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. 왼쪽 패널에서 를 확장합니다. **[!UICONTROL Customers]** 및 선택 **[!UICONTROL Invitations]**.

1. 확장 ![확장 선택기](../assets/icon-display-expand.png) 다음 **[!UICONTROL General]** 섹션.

   ![고객 구성 - 초대 일반 옵션](../configuration-reference/customers/assets/invitations-general.png){width="600" zoomable="yes"}

1. 설정 **[!UICONTROL Enable Invitations Functionality]** 끝 `Yes`.

1. 고객이 상점 첫 화면에서 초대를 관리할 수 있도록 하려면 다음을 설정하십시오. **Storefront에서 초대 활성화** 끝 `Yes`.

1. 설정 **[!UICONTROL Referred Customer Group]** 다음 중 하나를 수행합니다.

   - `Same as Inviter`
   - `Default Customer Group from Configuration`

1. 설정 **[!UICONTROL New Accounts Registration]** 다음 중 하나를 수행합니다.

   - `By Invitation Only`
   - `Available to All`

1. 종료 **[!UICONTROL Allow Customers to Add Custom Message to Invitation Email]**, 선택 `Yes`.

1. 한 번에 보낼 수 있는 초대 수를 제한하려면 **[!UICONTROL Max Invitations Allowed to be Sent at One Time]** 필드.

1. 확장 ![확장 선택기](../assets/icon-display-expand.png) 다음 **[!UICONTROL Email]** 섹션을 참조하고 다음을 수행합니다.

   ![고객 구성 - 초대 이메일 옵션](../configuration-reference/customers/assets/invitations-email.png){width="600" zoomable="yes"}

   - 로 사용할 스토어 ID 선택 **[!UICONTROL Customer Invitation Email Sender]**.

   - 다음 항목 선택 **[!UICONTROL Customer Invitation Email Template]** 보낸 초대에 사용됩니다.

1. 완료되면 다음을 클릭하십시오. **[!UICONTROL Save Config]**.

## 관리자에서 초대 보내기 및 관리

다음에서 [비공개 판매 보고서](../getting-started/private-sales-reports.md) 섹션에는 지정된 기간 동안 보낸 초대 수 또는 초대를 보낸 고객이 표시됩니다.

### 관리자에서 초대 만들기

1. 다음에서 _관리자_ 사이드바, 이동 **[!UICONTROL Marketing]** > _[!UICONTROL Private Sales]_>**[!UICONTROL Invitations]**.

1. 오른쪽 위 모서리에서 을(를) 클릭합니다. **[!UICONTROL Add Invitations]**.

1. 다음 화면에서는 새 고객을 초대하고 사용자 지정 메시지를 추가하고 보낸 사람을 선택한 다음 초대 그룹을 선택하는 이메일 주소를 입력합니다.

   저장소 보기가 여러 개 있는 경우 **[!UICONTROL Send From]** 초대를 보낼 저장소 보기를 지정하는 옵션입니다.

   ![초대 정보](./assets/create-invitation-page.png){width="700" zoomable="yes"}

1. 완료되면 다음을 클릭하십시오. **[!UICONTROL Save]**.

### 단일 엔터티에 대한 초대 무시

1. 다음에서 _관리자_ 사이드바, 이동 **[!UICONTROL Marketing]** > _[!UICONTROL Private Sales]_>**[!UICONTROL Invitations]**.

1. 필터를 사용하여 필요한 초대를 찾아 편집 모드로 엽니다.

1. 오른쪽 위 모서리에서 을(를) 클릭합니다. **[!UICONTROL Discard Invitation]**.

1. 작업을 확인하려면 다음을 클릭합니다. **[!UICONTROL OK]**.

### 여러 엔터티에 대한 초대 무시

1. 다음에서 _관리자_ 사이드바, 이동 **[!UICONTROL Marketing]** > _[!UICONTROL Private Sales]_>**[!UICONTROL Invitations]**.

1. 삭제할 초대를 찾아 선택합니다.

1. 왼쪽 상단에서 **[!UICONTROL Actions]** 선택할 메뉴 **[!UICONTROL Discard Selected]** 및 클릭 **[!UICONTROL Submit]**.

1. 작업을 확인하려면 다음을 클릭합니다. **[!UICONTROL OK]**.

### 필드 설명

| 필드 | 설명 |
|--- |--- |
| [!UICONTROL Select] | 확인란을 선택하여 작업에 적용할 초대를 선택하거나 열 머리글에서 선택 컨트롤을 사용합니다. 옵션: `Select All` /` Deselect All` / `Select Visible` / `Unselect Visible` |
| [!UICONTROL ID] | 초대의 내부 ID 번호 |
| [!UICONTROL Email] | 해당 고객 이메일 주소 |
| [!UICONTROL Invitee] | 초대된 사용자 이메일 |
| [!UICONTROL Sent] | 초대가 전송된 시간과 날짜 |
| [!UICONTROL Registered] | 고객이 등록된 시간 및 데이터 |
| [!UICONTROL Status] | 초대 상태. 옵션: `Sent` / `Not Sent` / `Accepted` / `Discarded` |
| [!UICONTROL Valid Website] | 해당 웹 사이트 |
| [!UICONTROL Invitee Group] | 초대받은 사람의 고객 그룹 |

{style="table-layout:auto"}
