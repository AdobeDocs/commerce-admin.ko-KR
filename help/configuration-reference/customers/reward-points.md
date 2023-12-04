---
title: '[!UICONTROL Customers] &gt; [!UICONTROL Reward Points]'
description: 에서 구성 설정을 검토합니다. [!UICONTROL Customers] &gt; [!UICONTROL Reward Points] 상거래 관리자의 페이지입니다.
exl-id: 0b7f8806-74c5-4467-87da-0faae50f164b
feature: Configuration, Rewards
source-git-commit: 1ae3e1fd10e29de690f7f159c36101a9817dea91
workflow-type: tm+mt
source-wordcount: '781'
ht-degree: 0%

---

# [!UICONTROL Customers] > [!UICONTROL Reward Points]

{{ee-feature}}

{{config}}

>[!NOTE]
>
>[보상 환율](../../merchandising-promotions/reward-exchange-rates.md) 체크아웃 중에 고객과 관리자가 보상 포인트를 상환하려면 구성이 필요합니다.

## [!UICONTROL Reward Points]

![보상 점수](./assets/reward-points-reward-points.png)<!-- zoom -->

<!-- [Reward Points](https://docs.magento.com/user-guide/marketing/reward-point-configure.html) -->

| 필드 | [범위](../../getting-started/websites-stores-views.md#scope-settings) | 설명 |
|--- |--- |----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Enable Reward Points Functionality] | 글로벌 | 보상 포인트를 활성화 또는 비활성화합니다. 옵션: `Yes` / `No`. |
| [!UICONTROL Enable Reward Points Functionality on Storefront] | 웹 사이트 | 활성화되면 고객은 활동을 통해 포인트를 획득하고 체크아웃 시 포인트를 사용할 수 있습니다. 비활성화된 경우 관리자 사용자만 고객을 대신하여 포인트를 할당하고 사용할 수 있습니다. 옵션: `Yes` / `No`. |
| [!UICONTROL Customers May See Reward Points History] | 웹 사이트 | 활성화된 경우 고객은 계정 대시보드에서 각 보상 포인트 적립, 상환 및 만료와 관련된 자세한 내역을 볼 수 있습니다. 옵션: `Yes` / `No` |
| [!UICONTROL Reward Points Balance Redemption Threshold] | 웹 사이트 | 고객이 주문에 대해 상환하기 전에 최소 포인트 잔액에 도달해야 합니다. 최소값을 지정하지 않으려면 비워 둡니다. |
| [!UICONTROL Cap Reward Points Balance At] | 웹 사이트 | 고객이 이 최대 포인트 잔액보다 더 많이 적립되지 않도록 합니다. 최대값을 지정하지 않으려면 비워 둡니다. |
| [!UICONTROL Reward Points Expire in (days)] | 웹 사이트 | 보상 포인트의 라이프타임(일)을 나타냅니다. 별도의 활동 동안 얻은 각 포인트에는 별도의 라이프타임이 있습니다. 보상 포인트 내역의 각 배치는 포인트가 만료되기 전까지 남은 일 수를 나타냅니다. 고객 계정 대시보드(활성화된 경우) 및 관리자에서 내역을 볼 수 있습니다. 만료 없이 비워 둡니다. |
| [!UICONTROL Reward Points Expiry Calculation] | 웹 사이트 | 보상 포인트가 만료되는 시기를 결정하는 데 사용되는 방법을 결정합니다. 옵션: <br/>**`Static`**- 구성에 설정된 일수를 기반으로 보상 포인트의 남은 라이프타임을 결정합니다. 구성 내 만료 한도가 바뀌면 기존 포인트의 만료일은 바뀌지 않는다.<br/>**`Dynamic`** - 보상 포인트 잔액이 증가할 때마다 남은 일수를 계산합니다. 구성의 만료 제한이 변경되면 기존 모든 포인트에 대한 만료 계산이 그에 따라 업데이트됩니다. |
| [!UICONTROL Refund Reward Points Automatically] | 글로벌 | 사용 가능한 보상 포인트가 자동으로 환급되는지 여부를 결정합니다. 옵션: `Yes` / `No` |
| [!UICONTROL Deduct Reward Points from Refund Amount Automatically] | 글로벌 | 이 기능이 활성화된 경우 구매를 통해 획득한 보상 포인트가 주문 환불 시 완전히 또는 부분적으로 무효화되는지 결정합니다. 획득한 주문의 보상 점수만 해당 주문이 환불될 때 영향을 받습니다. 옵션: `Yes` / `No`. |
| [!UICONTROL Landing Page] | 스토어 뷰 | 보상 포인트 프로그램을 설명하는 CMS 페이지를 지정합니다. 스토어에서 포인트를 획득할 수 있는 위치에 기본 보상 페이지에 대한 링크가 나타납니다. |

{style="table-layout:auto"}

## [!UICONTROL Actions for Acquiring Reward Points by Customers]

![고객이 보상 포인트를 획득하는 작업](./assets/reward-points-actions-for-acquiring.png)<!-- zoom -->

<!-- [Actions for Acquiring Reward Points by Customers](https://docs.magento.com/user-guide/marketing/reward-point-configure.html) -->

| 필드 | [범위](../../getting-started/websites-stores-views.md#scope-settings) | 설명 |
|--- |--- |----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Purchase] | 웹 사이트 | 구성된 를 기반으로 구매에 대해 보상 포인트를 획득하는지 여부를 결정합니다. [보상 환율](../../merchandising-promotions/reward-exchange-rates.md). 옵션: `Yes` / `No` |
| [!UICONTROL Registration] | 웹 사이트 | 고객 계정 개설을 위해 획득한 점수 수를 지정합니다. |
| [!UICONTROL Newsletter Signup] | 웹 사이트 | 뉴스레터를 구독하는 등록된 고객이 획득한 점수 수를 지정합니다. (게스트는 포인트를 구독할 수 없습니다.) 고객이 가입 해지했다가 다시 가입하면 두 번째 가입에는 포인트를 적립하지 않는다. |
| [!UICONTROL Converting Invitation to Customer] | 웹 사이트 | 수신자가 고객 계정을 열 때 초대를 보낸 고객이 획득한 점수 수를 지정합니다. |
| [!UICONTROL Invitation to Customer Conversions Quantity Limit] | 웹 사이트 | 초대장을 보낸 고객의 포인트를 적립하는 데 사용할 수 있는 초대 전환 수를 제한합니다. 제한을 두지 않으려면 비워 둡니다. |
| [!UICONTROL Converting Invitation to Order] | 웹 사이트 | 수신자가 초기 주문을 할 때 초대장을 보낸 고객이 얻은 점수 수를 지정합니다. |
| [!UICONTROL Invitation to Order Conversions Quantity Limit] | 웹 사이트 | 초대를 보낸 사람에 대해 점수를 획득할 수 있는 주문 전환 수를 제한합니다. 비워 두면 최대 한도는 없습니다. |
| [!UICONTROL Invitation Conversion to Order Reward] | 웹 사이트 | 초대받은 사람이 구매를 할 때 고객이 보상 포인트를 적립할 수 있는 빈도를 나타냅니다. 옵션: <br/>**`Each`**- 고객은 초대받은 사람이 보낸 각 송장 주문에 대해 보상 포인트를 받습니다. 보상 포인트는 웹사이트 및 고객 그룹의 필수 조합에 대해 설정된 환율에 따라 부여됩니다.<br/>**`First`** - 고객은 초대받은 사람이 수행한 첫 번째 인보이스 주문에 대해서만 보상 포인트를 받습니다. 두 명 이상의 초대받은 사람이 등록하고 주문하면 첫 번째 주문 금액만 보상 포인트로 전환돼 고객에게 부여된다. |
| [!UICONTROL Review Submission] | 웹 사이트 | 게시가 승인된 검토를 제출한 고객이 얻은 점수 수를 결정합니다. |
| [!UICONTROL Rewarded Reviews Submission Quantity Limit] | 웹 사이트 | 고객당 포인트를 적립하는 데 사용할 수 있는 리뷰 수를 제한합니다. 제한을 두지 않으려면 비워 둡니다. |

{style="table-layout:auto"}

## [!UICONTROL Email Notification Settings]

![이메일 알림 설정](./assets/reward-points-email-notification-settings.png)<!-- zoom -->

<!-- [Email Notification Settings](https://docs.magento.com/user-guide/marketing/reward-point-configure.html) -->

| 필드 | [범위](../../getting-started/websites-stores-views.md#scope-settings) | 설명 |
|--- |--- |--- |
| [!UICONTROL Email Sender] | 스토어 뷰 | 잔고 업데이트 및 만료 알림 이메일을 보낸 사람으로 표시되는 스토어 연락처를 결정합니다. |
| [!UICONTROL Subscribe Customers by Default] | 글로벌 | 잔액 업데이트 및 만료 알림 이메일 모두에 대한 고객의 기본 구독 상태를 결정합니다. |
| [!UICONTROL Balance Update Email] | 스토어 뷰 | 포인트 잔액이 업데이트될 때마다 고객에게 전송되는 알림에 사용되는 템플릿을 결정합니다. 기본 템플릿: `Reward Points Balance Update` |
| [!UICONTROL Reward Points Expiry Warning Email] | 스토어 뷰 | 일괄 처리에 대한 만료 경고 제한에 도달했을 때 고객이 받는 전자 메일의 템플릿을 결정합니다. 기본 템플릿: `Reward Points Expiry Warning` |
| [!UICONTROL Expiry Warning before (days)] | 글로벌 | 알림을 전송할 지점 만료 전 일 수를 지정합니다. 만료 알림을 전송하지 않으려면 비워 둡니다. 입력한 일 수가 포인트의 남은 라이프타임보다 큰 경우 알림이 전송되지 않습니다. |

{style="table-layout:auto"}
