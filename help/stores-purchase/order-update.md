---
title: 주문 업데이트
description: 관리자에서 고객의 주문을 업데이트하는 방법을 알아봅니다.
exl-id: 15c73d27-f4bd-47d6-8d36-902074f9c3e6
feature: Orders, Customer Service
source-git-commit: 8b5af316ab1d2e632ed5fc2066974326830ab3f7
workflow-type: tm+mt
source-wordcount: '767'
ht-degree: 0%

---

# 주문 업데이트

주문한 고객을 도울 때는 주문 상태를 확인해야 합니다. 에 사용할 수 있는 옵션 `Pending` 주문은 의 옵션과 다릅니다. `Processing` 주문. 자세한 내용은 [주문 처리](order-processing.md).

## 보류 중인 주문

고객이 주문한 후 결제를 받기 전에 주문이 완료됩니다. `Pending` 상태. 주문을 편집하거나, 보류하거나, 완전히 취소할 수 있습니다. 보류 중인 주문의 단추 모음에는 주문에 사용할 수 있는 작업이 나열됩니다.

![보류 중인 주문 옵션](./assets/order-button-bar-pending.png){width="600" zoomable="yes"}

주문의 상당 부분을 수정하면 원래 주문이 취소되고 새 주문이 생성됩니다. 그러나 신규 주문을 생성하지 않고 청구 또는 운송 주소를 변경할 수 있습니다.

| 단추 | 설명 |
|--- |--- |
| **[!UICONTROL Back]** | 변경 사항을 저장하지 않고 주문 페이지로 돌아갑니다. |
| **[!UICONTROL Login as Customer]** | 관리자가 고객의 주문을 지원할 수 있습니다. |
| **[!UICONTROL Cancel]** | 보류 중인 주문을 취소합니다. |
| **[!UICONTROL Send Email]** | 보류 중인 주문에 대한 이메일을 고객에게 보냅니다. |
| **[!UICONTROL Hold]** / **[!UICONTROL Unhold]** | 보류 중인 주문의 상태를 다음으로 변경 `On Hold`. 보류를 해제하려면 다음을 선택합니다. _[!UICONTROL Unhold]_. |
| **[!UICONTROL Invoice]** | 다음을 생성합니다. [인보이스](invoices.md#create-an-invoice) 주문을 송장으로 변환하여 대기 중인 주문에서 주문 상태를 다음으로 변경합니다. `processing`. |
| **[!UICONTROL Ship]** | 를 만듭니다. [배송](shipments.md#create-a-shipment) 주문에 대해 기록합니다. |
| **[!UICONTROL Reorder]** | 현재 보류 주문과 중복되는 새 보류 주문을 만듭니다. |
| **[!UICONTROL Edit]** | 편집 모드에서 보류 중인 주문을 엽니다. 편집 버튼은 보류 중인 주문 또는 협상된 주문에 대해서만 사용할 수 있습니다. [따옴표](../b2b/quotes.md). |

{style="table-layout:auto"}

## 주문 처리

주문이 `Processing` 상태:

* 지급 조치가 로 설정된 경우 주문에 대한 지급이 입고/캡처되고 송장이 생성됩니다. `Authorize and Capture`.
* 주문 트랜잭션은 승인되지만 지급은 아직 캡처되지 않습니다(지급 조치가 로 설정된 경우). `Authorize`.

다음 [결제 조치 구성](../configuration-reference/sales/payment-methods.md#payment-actions) 주문이 생성된 후 사용할 수 있는 주문 작업을 결정합니다.

를 실질적으로 변경할 수 없습니다. `Processing` 주문하되, 청구 및 배송 주소를 편집할 수 있습니다.

![처리 순서 옵션](./assets/order-button-bar-processing.png){width="600" zoomable="yes"}

>[!NOTE]
>
>결제 방법의 결제 작업을 로 설정한 경우 `Authorize and Capture`(고객이 주문을 하면 송장이 자동으로 생성됩니다.) 이 경우 다음을 사용하여 자금을 환불할 수 있습니다. [대변 메모](credit-memo-create.md), 그러나 다음과 같은 작업을 수행할 수 없음 [취소](#cancel-a-pending-order) 또는 [무효](#void-a-processing-order) 명령입니다.

| 단추 | 설명 |
|--- |--- |
| **[!UICONTROL Back]** | 변경 사항을 저장하지 않고 주문 페이지로 돌아갑니다. |
| **[!UICONTROL Send Email]** | 주문에 대한 이메일을 고객에게 보냅니다. |
| **[!UICONTROL Void]** | [빈 공간](#void-a-processing-order) 주문 트랜잭션 또는 부분 주문 트랜잭션. |
| **[!UICONTROL Credit Memo]** | 만들기 프로세스를 시작합니다. [대변 메모](credit-memo-create.md). |
| **[!UICONTROL Hold]** / **[!UICONTROL Unhold]** | 판매 주문의 상태를 다음으로 변경 `On Hold`. 판매 주문에 대한 보류를 릴리즈하려면 다음을 선택합니다 _[!UICONTROL Unhold]_. |
| **[!UICONTROL Reorder]** | 현재 주문을 기반으로 새 보류 주문을 만듭니다. |
| **[!UICONTROL Create Returns]** | ![Adobe Commerce](../assets/adobe-logo.svg) (Adobe Commerce만 해당) 다음 작업을 수행하는 프로세스를 시작합니다. [반환](returns.md) 주문에서 하나 이상의 항목. |

{style="table-layout:auto"}

## 처리 순서 무효화

주문이 아직 다음 단계에 있는 경우 `Processing` 상태 및 지급 통합이 다음으로 설정됨 `Authorize` (아님) `Authorize and Capture`) 거래를 무효화하거나 주문을 취소할 수만 있습니다. [주문 취소](#cancel-a-pending-order) 또한 권한 부여가 무효화됩니다.

결제 조치가 다음으로 설정된 결제 방법을 사용하여 주문이 이루어진 경우 `Authorize and Capture` 대변 메모를 통해 자금을 환불할 수 있지만 송장이 발행되고 지급이 포착되었기 때문에 취소할 수는 없습니다.

결제 방법에 따라 사용 가능한 결제 조치가 결정됩니다. 다음을 참조하십시오 [결제 작업](../configuration-reference/sales/payment-methods.md#payment-actions) 추가 정보.

**_주문을 무효화하려면_**

1. 다음에서 _관리자_ 사이드바, 이동 **[!UICONTROL Sales]** > _[!UICONTROL Operations]_>**[!UICONTROL Orders]**.

1. 다음에서 **[!UICONTROL Action]** 편집할 주문에 대한 열을 클릭합니다. **[!UICONTROL View]**.

1. 클릭 **[!UICONTROL Void]** 주문을 무효로 합니다.

1. 프롬프트에서 다음을 클릭합니다. **[!UICONTROL OK]** 주문을 무효로 합니다.

다음을 사용하여 필요한 환불을 발행할 수 있습니다. [대변 메모](credit-memo-create.md) 자금이 포착된 후. 다음을 만들 수도 있습니다 [반품 상품 승인(RMA)](returns.md) 제품 반품에 대해 발행됨. 자세한 내용은 다음을 참조하십시오. [주문 처리](order-processing.md).

## 보류 중인 주문 편집

1. 다음에서 _관리자_ 사이드바, 이동 **[!UICONTROL Sales]** > _[!UICONTROL Operations]_>**[!UICONTROL Orders]**.

1. 다음에서 **[!UICONTROL Action]** 편집할 주문에 대한 열을 클릭합니다. **[!UICONTROL View]**.

1. 클릭 **[!UICONTROL Edit]**.

   ![순서 편집](./assets/order-edit.png){width="600" zoomable="yes"}

1. 프롬프트에서 다음을 클릭합니다. **[!UICONTROL OK]** 을 눌러 편집을 계속합니다.

1. 필요에 따라 주문을 업데이트합니다.

1. 변경 사항 적용:
   * 청구 또는 배송 주소에 대한 변경 사항을 저장하려면 **[!UICONTROL Save]**.
   * 라인 항목에 대한 변경 사항을 저장하고 주문을 재처리하려면 **[!UICONTROL Submit Order]**.

## 주문 보류

고객이 선호하는 결제 방법을 사용할 수 없거나 해당 품목이 일시적으로 품절된 경우 주문을 보류할 수 있다.

1. 다음에서 _주문 수_ 격자, 다음을 찾습니다. `Pending` 보류하려는 주문을 합니다.

1. 다음에서 _작업_ 열, 클릭 **[!UICONTROL View]**.

1. 클릭 **[!UICONTROL Hold]** 주문을 보류합니다.

주문에 대한 보류를 제거하려면 주문을 다시 편집하고 를 클릭합니다. **[!UICONTROL Unhold]**.

## 보류 중인 주문 취소

주문을 취소하면 다음에서 상태가 변경됩니다. `Pending` 끝 `Canceled`.

1. 다음에서 _[!UICONTROL Orders]_그리드에서 취소할 보류 중인 주문을 찾습니다.

1. 다음에서 _[!UICONTROL Action]_열, 클릭&#x200B;**[!UICONTROL View]**.

1. 클릭 **[!UICONTROL Cancel]** 주문을 취소합니다.

현재 주문 상태는 입니다. `Canceled`.
