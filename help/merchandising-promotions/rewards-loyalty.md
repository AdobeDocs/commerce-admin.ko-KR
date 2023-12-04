---
title: 보상 및 충성도 프로그램
description: 고객 참여를 유도하고 고객 충성도를 홍보하는 데 사용할 수 있는 보상 포인트 시스템에 대해 알아봅니다.
exl-id: 2bccdcce-7936-4449-9634-d463ad29e5cc
feature: Rewards, Promotions/Events, Customers, Configuration
source-git-commit: 9d775e8e8521032dc58f6cd1ed7796595db745a0
workflow-type: tm+mt
source-wordcount: '1402'
ht-degree: 0%

---

# 보상 및 충성도 프로그램

{{ee-feature}}

다음 _보상 점수_ Adobe Commerce의 시스템은 고객 참여를 유도하고 고객 충성도를 홍보하는 고유한 프로그램을 구현하는 기능을 제공합니다. 다양한 거래 및 고객 활동에 대해 포인트를 부여할 수 있으며, 포인트 배분, 잔고 및 만기를 제어하기 위한 구성을 설정할 수 있습니다. 고객은 보상 포인트와 통화 간에 설정한 전환율에 따라 구매 시 포인트를 상환할 수 있습니다.

## 장바구니 가격 규칙

포인트는 다음을 기반으로 고객에게 보상될 수 있습니다. [장바구니 규칙](price-rules-cart.md). 그들은 가격 규칙의 유일한 행동으로서, 또는 할인과 함께 보상을 받을 수 있다.

## 고객 균형

보상 포인트 잔액은 고객당 관리자 사용자가 관리할 수 있습니다. 상점 첫 화면에서 활성화된 경우 고객은 포인트 잔고의 세부 정보를 볼 수도 있습니다.

## 포인트 제한

>[!NOTE]
>
>[보상 환율](reward-exchange-rates.md) 체크아웃 중에 고객 및 관리자 사용자가 보상 포인트를 상환하려면 구성이 필요합니다.

포인트는 체크아웃 중에 관리자 사용자 및 고객(활성화된 경우)이 상환할 수 있습니다. 결제 방법 섹션에서 활성화된 결제 방법 위에 내 보상 포인트 사용 확인란이 표시됩니다. 사용 가능한 포인트와 환율이 포함되어 있습니다. 사용 가능한 잔액이 주문 총액보다 큰 경우 추가 결제 방법이 필요하지 않습니다. 주문에 적용되는 보상 포인트의 수는 매장 신용카드나 기프트 카드와 마찬가지로 총합계에서 뺀 주문 합계와 함께 나타납니다. 매장 신용카드나 기프트 카드와 함께 보상 포인트를 사용하면 보상 포인트가 먼저 차감된다. 그러면 주문 합계가 상환 가능한 보상 포인트 수보다 큰 경우 매장 신용 또는 기프트 카드가 공제됩니다.

>[!NOTE]
>
>보상 포인트는 주문 송장이 발행될 때까지 결제 접수를 확인할 수 없기 때문에 COD 구매와 함께 사용하지 않는 것이 좋습니다.

## 보상 포인트에 대한 환불

보상 포인트가 지급된 주문은 주문 금액까지 보상 포인트 잔액으로 환불이 가능하다. 다음에서 [_새 대변 메모_ 페이지](../stores-purchase/credit-memo-create.md)고객의 잔고에 적용할 점수의 개수를 입력할 수 있다. 기본적으로 필드에는 순서에 사용된 점의 전체 개수가 포함됩니다.

## 스토어에 대한 보상 지점 작업 활성화

보상 포인트 구성은 스토어에서 보상 포인트가 표시되는 방식을 결정하고 기본 운영 매개변수를 정의합니다.

![고객 구성 - 보상 포인트](../configuration-reference/customers/assets/reward-points-reward-points.png){width="600" zoomable="yes"}

### 1단계. 보상 포인트 구성

1. 다음에서 _관리자_ 사이드바, 이동 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. 왼쪽 패널에서 를 확장합니다. **[!UICONTROL Customers]** 및 선택 **[!UICONTROL Reward Points]**.

1. 확장 ![확장 선택기](../assets/icon-display-expand.png) 다음 **[!UICONTROL Reward Points]** 섹션을 참조하고 다음을 수행합니다.

   - 보상 포인트를 활성화하려면 을 설정합니다. **[!UICONTROL Enable Reward Points Functionality]** 끝 `Yes`.

   - 고객이 자신의 보상 포인트를 적립할 수 있도록 하려면 을 설정합니다. **[!UICONTROL Enable Reward Points Functionality on Storefront]** 끝 `Yes`.

   - 고객이 보상의 자세한 내역을 볼 수 있도록 하려면 다음을 설정하십시오. **[!UICONTROL Customers May See Reward Point History]** 끝 `Yes`.

1. 대상 **[!UICONTROL Reward Points Balance Redemption Threshold]**&#x200B;를 클릭하고 상환되기 전에 발생해야 하는 포인트 수를 입력합니다(최소 값은 비어 있음).

1. 대상 **[!UICONTROL Cap Reward Points Balance At]**&#x200B;고객이 적립할 수 있는 최대 포인트 수를 입력합니다(제한이 없는 경우 공백).

1. 대상 **[!UICONTROL Reward Points Expire in (days)]**&#x200B;보상 포인트가 만료되기 전 일 수를 입력합니다(만료되지 않은 경우 공백).

1. 설정 **[!UICONTROL Reward Points Expiry Calculation]** 다음 중 하나를 수행합니다.

   - `Static` - 구성에 설정된 일수를 기반으로 보상 포인트의 남은 라이프타임을 결정합니다. 구성 내 만료 한도가 바뀌면 기존 포인트의 만료일은 바뀌지 않는다.

   - `Dynamic` - 보상 포인트 잔액이 증가할 때마다 남은 일 수를 계산합니다. 구성의 만료 제한이 변경되면 기존 모든 포인트의 만료가 그에 따라 업데이트됩니다.

1. 사용 가능한 보상 포인트를 자동으로 환급하려면 을 설정합니다. **[!UICONTROL Refund Reward Points Automatically]** 끝 `Yes`.

1. 포인트를 획득한 주문이 전체 또는 일부 환불될 때 구매를 통해 획득한 보상 포인트를 무효화하려면 다음을 설정합니다. **[!UICONTROL Deduct Reward Points from Refund Amount Automatically]** 끝 `Yes`.

   >[!NOTE]
   >
   >환불 중인 주문으로 획득한 점수만 영향을 받습니다.

1. 설정 **[!UICONTROL Landing Page]** 보상 포인트 프로그램을 설명하는 콘텐츠 페이지로 이동합니다.

   기본 보상 포인트 페이지를 사용자 고유의 정보로 업데이트해야 합니다.

1. 완료되면 다음을 클릭하십시오. **[!UICONTROL Save Config]**.

### 2단계. 고객 활동에 대해 획득한 점수 구성

이 단계에서는 다양한 고객 활동에 대해 획득 가능한 보상 포인트 개수를 명시한다. 고객이 포인트가 할당된 작업을 완료하면 획득한 포인트의 수를 나타내는 메시지가 고객에게 표시됩니다.

1. 확장 ![확장 선택기](../assets/icon-display-expand.png) 다음 **[!UICONTROL Actions for Acquiring Reward Points by Customer]** 섹션.

   ![고객 구성 - 고객이 보상 포인트를 획득하는 작업](../configuration-reference/customers/assets/reward-points-actions-for-acquiring.png){width="600" zoomable="yes"}

1. 장바구니에 구매에 대해 획득한 보상 포인트와 고객의 현재 보상 포인트 잔액이 포함된 메시지를 표시하려면 을 설정합니다. **[!UICONTROL Purchase]** 끝 `Yes`.

   >[!NOTE]
   >
   >에 대한 보상 포인트를 획득하려면 _첫 번째_ 주문, 고객은 등록되어야 합니다. _다음 이전_ 결제 방법으로 거래가 캡처됩니다. 대부분의 결제 방법을 구성하여 트랜잭션을 캡처할 수 있습니다. _자동으로_ 주문이 들어갔을 때, _다음 이전_ 고객 계정 등록이 완료되었습니다.

1. 대상 **[!UICONTROL Registration]**&#x200B;고객 계정 개설을 위해 획득한 점수 수를 입력합니다.

1. 대상 **[!UICONTROL Newsletter Signup]**&#x200B;뉴스레터를 구독하는 등록된 고객이 획득한 점수 수를 입력합니다.

1. 대상 **[!UICONTROL Converting Invitation to Customer]**&#x200B;을(를) 통해 초대장을 보낸 고객이 획득한 점수 수를 입력하면 수신자는 고객 계정을 엽니다.

   초대를 보낸 고객의 포인트를 적립하는 데 사용할 수 있는 초대 전환 수를 제한할 수 있습니다(제한 없는 경우 공백). 이렇게 하려면 **[!UICONTROL Invitation to Customer Conversions Quantity Limit]** 필드.

1. 대상 **[!UICONTROL Converting Invitation to Order]**&#x200B;을(를) 통해 고객이 받는 사람에게 초대를 보낸 후 주문을 하고 다음을 수행하는 점수 수를 입력합니다.

   - 대상 **주문 전환 수량 제한으로의 초대**(수신자가 초기 주문을 할 때 초대를 보내는 고객이 획득한 점수 수를 입력합니다(제한 없는 경우 공백).

   - 대상 **[!UICONTROL Invitation Conversion to Order Reward]**&#x200B;를 선택하고 `Each` 수신자 주문별로 점수를 획득하거나 다음을 선택합니다. `First` 수신자가 처음 주문한 주문에 대해서만 포인트를 적립하는 옵션입니다.

1. 대상 **[!UICONTROL Review Submission]**&#x200B;게시가 승인된 검토를 제출한 고객이 획득한 점수 수를 입력합니다.

1. 그런 다음 고객당 점수를 얻는 데 사용할 수 있는 리뷰 수를 제한하려면 **[!UICONTROL Rewarded Reviews Submission Quantity Limit]** 필드(제한이 없는 경우 비어 있음)

1. 완료되면 다음을 클릭하십시오. **[!UICONTROL Save Config]**.

### 3단계. 이메일 알림 설정 완료

1. 확장 ![확장 선택기](../assets/icon-display-expand.png) 다음 **[!UICONTROL Email Notification Settings]** 섹션.

   ![고객 구성 - 보상 포인트 이메일 알림](../configuration-reference/customers/assets/reward-points-email-notification-settings.png){width="600" zoomable="yes"}

1. 설정 **[!UICONTROL Email Sender]** 잔고 업데이트 및 만료 알림을 보낸 사람으로 표시되는 스토어 연락처에 대해 설명합니다.

1. 잔액 업데이트 및 예정된 만료일을 알리기 위해 기본적으로 고객을 구독하려면 다음을 설정하십시오. **[!UICONTROL Subscribe Customers by Default]** 끝 `Yes`.

1. 설정 **[!UICONTROL Balance Update Email]** 포인트 잔액이 업데이트될 때마다 고객에게 전송되는 알림에 사용되는 템플릿입니다.

1. 설정 **[!UICONTROL Reward Points Expiry Warning Email]** 일괄 처리에 대한 만료 제한에 도달했을 때 고객에게 전송되는 알림에 사용되는 템플릿입니다.

1. 대상 **[!UICONTROL Expiry Warning Before (days)]**&#x200B;알림이 전송되기 전에 포인트가 만료되는 일 수를 입력합니다.

1. 완료되면 다음을 클릭하십시오. **[!UICONTROL Save Config]**.

## 보상 포인트 잔액 업데이트

관리자는 보상 포인트 잔액을 업데이트할 수 있습니다.

1. 다음에서 _관리자_ 사이드바, 이동 **[!UICONTROL Customers]** > **[!UICONTROL All Customers]**.

1. 그리드에서 고객을 찾아 다음을 클릭합니다. **[!UICONTROL Edit]** 다음에서 _[!UICONTROL Action]_열.

1. 아래 _고객 정보_, 을(를) 선택합니다. **[!UICONTROL Reward Points]** 섹션.

1. 다음 수를 입력합니다. **[!UICONTROL Update Points]**:

   - 보상 포인트 금액을 갱신하려면 숫자를 입력하여 총 포인트 잔액을 증가시킵니다.
   - 보상 포인트 금액을 빼려면 총 포인트 잔액을 줄이려는 음수를 입력합니다.

1. 입력 **[!UICONTROL Comments]** 필요한 경우 보상 포인트 조정과 관련이 있습니다.

   ![보상 포인트 잔고](./assets/reward-points-balance.png){width="700" zoomable="yes"}

1. 필요한 경우 고객을 다음에 가입시킵니다 _보상 포인트 알림_:

   - **[!UICONTROL Subscribe for Balance Updates]**
   - **[!UICONTROL Subscribe for Points Expiration Notifications]**

1. 클릭 **[!UICONTROL Save Customer]**.

보상 포인트와 관련된 모든 작업이 고객의 _[!UICONTROL Reward Points History]_상점 앞에서 그들의 계좌를 봉쇄하다.

## 필드 설명

| 필드 | 설명 |
|--- |--- |
| [!UICONTROL Balance] | 클라이언트에 대한 보상 포인트의 현재 잔고 |
| [!UICONTROL Amount Balance] | 현재 현금 잔고 금액 |
| [!UICONTROL Points] | 가감 포인트 수 |
| [!UICONTROL Amount] | 가산 또는 감산 금액 |
| [!UICONTROL Rate] | 다음 [보상율](reward-exchange-rates.md) |
| [!UICONTROL Website] | 보상 포인트 내역이 지정된 웹 사이트 |
| [!UICONTROL Reason] | 점수 부여 이유:<br>**[!UICONTROL Making purchases]**— 고객이 구매할 때마다 포인트를 적립할 수 있습니다.<br>**[!UICONTROL Registering on the site]** - 등록 시 발생(한 번).<br>**[!UICONTROL Subscribing to a newsletter]**- 최초 구독(1회)에 대해 적립됩니다.<br>**[!UICONTROL Sending Invitations]** — 친구를 초대하여 포인트를 적립할 수 있습니다.<br>**[!UICONTROL Converting Invitations to Customer]**— 사이트에 등록하고 있는 유수의 친구들과 보내는 모든 초대에 대해 포인트를 적립합니다.<br>**[!UICONTROL Converting Invitations to Order]** — 전송된 초대장을 통해 각 판매에 대해 포인트를 적립합니다.<br>**[!UICONTROL Review Submission]**— 제품 리뷰를 제출하면 점수를 획득할 수 있습니다. |
| [!UICONTROL Created] | 보상 포인트 업데이트 날짜 및 시간 |
| [!UICONTROL Expired] | 만료된 보상 포인트 수 |
| [!UICONTROL Comment] | 포인트를 추가 또는 뺄 때의 주석 |

{style="table-layout:auto"}

## 리소스 문제 해결

보상 포인트 문제를 해결하는 데 대한 도움말을 보려면 다음 Commerce 지원 기술 문서를 참조하십시오.

- [부분 주문에 대한 충성도 포인트](https://experienceleague.adobe.com/docs/commerce-knowledge-base/kb/support-tools/patches/v1-0-8/mdva-31295-magento-patch-loyalty-points-on-partial-orders.html)
- [404 오류 - 다중 배송 체크아웃 시 보상 포인트 제거](https://experienceleague.adobe.com/docs/commerce-knowledge-base/kb/troubleshooting/storefront/magento-2.4.0-404-error-removing-rewards-points-on-multi-shipping-checkout.html)
