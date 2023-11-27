---
title: 반환
description: 반품 워크플로우와 반품 승인 발행에 대해 알아봅니다.
exl-id: 9dde0360-aa99-4fc4-92ff-976d9874ffec
feature: Returns
source-git-commit: 8b5af316ab1d2e632ed5fc2066974326830ab3f7
workflow-type: tm+mt
source-wordcount: '687'
ht-degree: 0%

---

# 반환

A _반송된 상품 승인_ (RMA)는 교환 또는 환불을 위해 품목을 반품하도록 요청하는 고객에게 부여될 수 있습니다. 일반적으로 고객은 가맹점에 연락하여 환불을 요청합니다. 승인된 경우, 반품 제품을 식별하기 위해 고유한 RMA 번호가 지정됩니다. 구성에서 모든 제품에 대해 RMA를 활성화하거나 특정 제품에 대해서만 RMA를 허용할 수 있습니다. 다음 _[!UICONTROL Returns]_그리드는 현재 반품된 상품 요청(RMA)을 나열하며 새로운 반품 요청을 입력하는 데 사용됩니다.

![그리드 반환](./assets/return.png){width="600" zoomable="yes"}

RMA는 단순, 그룹화, 구성 및 번들 제품 유형에 대해 발급할 수 있습니다. 단, 가상 상품, 다운로드 가능 상품, 기프트 카드 등에는 RMA를 사용할 수 없다.

## 열 설명

| 열 | 설명 |
|--- |--- |
| [!UICONTROL Select] | 반환에 대한 확인란을 선택하여 작업을 적용하거나 열 머리글에서 선택 컨트롤을 사용합니다. 옵션: `Select All` / `Deselect All` / `Select Visible` / `Unselect Visible` |
| [!UICONTROL RMA] | 각 반환에 할당된 고유한 숫자 식별자 |
| [!UICONTROL Requested] | 반환 날짜 및 시간 |
| [!UICONTROL Order] | 원래 주문의 고유 번호 |
| [!UICONTROL Ordered] | 주문이 이루어진 날짜와 시간 |
| [!UICONTROL Customer] | 주문을 한 고객 또는 구매자의 이름 |
| [!UICONTROL Status] | 반환 상태. 옵션: `Pending` / `Authorized` / `Partially Authorized` / `Approved` / `Rejected` / `Processed and Closed` / `Closed` |
| [!UICONTROL Action] | **[!UICONTROL View]** 편집 모드에서 반환을 엽니다. |

{style="table-layout:auto"}

## RMA 및 반품 워크플로우

1. **요청 수신** - 경우 [활성화됨](rma-configure.md#enable-rmas-for-your-store) 상점의 경우 등록 고객과 게스트 모두 RMA를 요청할 수 있습니다. 다음을 수행할 수도 있습니다. [책임자에서 RMA 요청 제출](#create-a-return-request-in-the-admin).

2. **RMA 발행됨** - 요청을 고려한 후에는 요청을 일부, 전체 또는 취소하거나 승인할 수 있습니다. 귀하가 반품을 승인하고 반품 배송에 대한 지불에 동의하는 경우, 지원되는 운송업자와 함께 관리자로부터 선적 주문을 생성할 수 있습니다.

3. **상품 입고 및 제품 반품 처리됨** - 다음 순서도는 반품 프로세스를 완료하기 위한 운영 순서에 대해 설명합니다.

   ![제품 반환 워크플로우](./assets/workflow-customer-returns.png){width="500"}

## RMA 상태

라이프사이클 동안 반품된 상품 승인(RMA)은 많은 지정된 상태(예: 보류 중 또는 승인)를 가질 수 있습니다. RMA 상태는 사용자 또는 판매자가 제기한 RMA 요청의 진행 상황을 나타냅니다.

| 상태 | 설명 |
|--- |--- |
| [!UICONTROL Pending] | 상점의 사용자 또는 관리자의 판매자가 RMA 요청을 제기할 때 할당된 초기 상태. |
| [!UICONTROL Authorized] | 이 상태는 요청된 모든 품목이 반품에 대해 관리자의 상인이 인증한 경우 RMA에 할당됩니다. |
| [!UICONTROL Partially Authorized] | 요청된 품목 중 하나라도 거부되고 다른 제품이 승인된 경우 이 상태는 RMA에 할당됩니다. |
| [!UICONTROL Denied] | 요청 품목이 모두 반품에 대해 관리자의 판매자에 의해 거부된 경우 이 상태는 RMA에 할당됩니다. |
| [!UICONTROL Return Received] | 이 상태는 요청된 품목이 사용자로부터 입고될 때 판매자가 RMA에 지정합니다. |
| [!UICONTROL Return Partially Received] | 요청된 품목이 부분적으로 반품되고 일부 품목의 처리가 거부되면 판매자는 이 상태를 RMA에 지정합니다. |
| [!UICONTROL Approved] | 이 상태는 요청된 품목이 추가 처리를 위해 승인될 때 판매자가 RMA에 지정합니다. |
| [!UICONTROL Rejected] | 요청된 품목이 추가 처리를 거부하는 경우 판매자는 이 상태를 RMA에 지정합니다. |
| [!UICONTROL Processed and Closed] | 요청된 모든 품목이 추가 처리를 위해 승인될 때 판매자는 이 상태를 RMA에 지정합니다. |
| [!UICONTROL Closed] | 요청된 품목이 반품처리를 거부하는 경우 판매자는 이 상태를 RMA에 지정합니다. |

{style="table-layout:auto"}

## 책임자에서 반환 요청 만들기

판매자는 관리자로부터 고객을 대신하여 반환 요청을 생성할 수 있습니다. 고객은 다음을 수행할 수 있습니다. [반환 요청 만들기](rma-customer-experience.md) Adobe Commerce 매장 앞에요.

1. 다음에서 _관리자_ 사이드바, 이동 **[!UICONTROL Sales]** > **[!UICONTROL Returns]**.

1. 클릭 **[!UICONTROL New Return Request]**.

1. 반환 요청을 만들려면 `Complete` 상태.

1. 아래 _[!UICONTROL Return Information]_섹션에서&#x200B;**[!UICONTROL Return Items]**탭.

1. 반환할 항목을 추가하려면 **[!UICONTROL Add Items]**.

1. 필요한 제품에 대한 확인란을 선택하고 **[!UICONTROL Add Selected Product to returns]**.

1. 대상 **[!UICONTROL Requested]**&#x200B;를 클릭하고 반환할 항목 수를 입력합니다.

1. 설정 **[!UICONTROL Return Reason]** 다음 중 하나를 수행합니다.

   - `Wrong Color`
   - `Wrong Size`
   - `Out of Service`
   - `Other`

   반환 이유가 나열된 선택 사항과 다른 경우, 다음을 선택하면 사용자 이름을 입력할 수 있습니다. `Other` 옵션을 선택합니다.

1. 설정 **[!UICONTROL Item Condition]** 다음 중 하나를 수행합니다.

   - `Unopened`
   - `Opened`
   - `Damaged`

1. 설정 **[!UICONTROL Resolution]** 다음 중 하나를 수행합니다.

   - `Exchange`
   - `Refund`
   - `Store Credit`

1. 반환을 생성하려면 다음을 클릭합니다. **[!UICONTROL Submit Returns]**.

   ![요청된 RMA 항목](./assets/return-item-request.png){width="600" zoomable="yes"}

   새로 제출된 RMA 요청이 **[!UICONTROL Returns]** 이 포함된 페이지 `Pending` 상태.
