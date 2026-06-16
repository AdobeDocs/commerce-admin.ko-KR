---
title: 스토어 크레딧
description: 스토어 크레딧은 고객 계좌로 회복되는 금액으로 구매 대금이나 현금 환불 등에 사용할 수 있다.
exl-id: 1fe627dd-5c49-4ff8-85e0-3c987285726d
feature: Customers, Storefront
TQID: https://experienceleague.adobe.com/kG-y-O2Yh-h1ct-oCwqylZFvS2FOCXFPD6qVIkKrpbg
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2:
  - id: bd989d82-1e15-4534-88db-f1f51dd77ffa
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
source-wordcount: 291
ht-degree: 0%

---

# 스토어 크레딧

{{ee-feature}}

스토어 크레딧은 고객 계정에 복원되는 금액입니다. 고객은 매장 크레딧을 사용하여 구매 대금을 결제하고, 관리자는 매장 크레딧을 사용하여 현금 환불할 수 있습니다. 선물 카드 잔액은 선물 카드 코드를 사용하여 나중에 구매하는 대신 고객의 계좌로 입금할 수 있습니다.

주문이 지불되고 송장이 발행되면 [대변 메모를 발행](../stores-purchase/credit-memo-create.md)하여 주문 또는 주문의 일부를 환불할 수 있습니다. 대변 메모는 차후 구매에 사용할 수 있는 고객 계정에 대변 금액이 복원되므로 환불과 다릅니다. 때로는 외상메모가 발급되는 것과 동시에 환불을 해주고 고객의 매장 외상 잔액에 대해서도 적용할 수 있다. 고객 계정에서 사용할 수 있는 스토어 크레딧 금액은 구성에 지정되어 있습니다.

>[!NOTE]
>
>저장소 크레딧이 주문 총액을 포함하는 경우 [_0개 소계 체크아웃_](../stores-purchase/zero-subtotal-checkout.md) 결제 방법을 사용하도록 설정해야 합니다.

## 신용 워크플로우 저장

1. **고객 로그인** - 체크아웃 프로세스를 시작하기 전에 고객이 계정에 로그인합니다.

1. **스토어 사용** - 크레딧 체크아웃 프로세스의 [!UICONTROL _검토 및 결제_] 단계에서 고객은 결제 옵션으로 [!UICONTROL _스토어 크레딧 사용_]&#x200B;을 선택합니다. 사용 가능한 잔액은 괄호 안에 표시됩니다. 가용 잔액이 총액보다 큰 경우 다른 결제 방법은 더 이상 표시되지 않습니다.

1. **주문에 적용된 크레딧** - 주문에 적용된 스토어 크레딧의 양이 주문 합계와 함께 나타나며 총합에서 뺍니다.

1. **고객 잔고 조정** - 주문 시 고객의 사용 가능한 잔고가 조정됩니다.
