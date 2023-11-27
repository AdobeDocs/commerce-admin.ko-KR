---
title: 트랜잭션
description: 거래 페이지와 이 페이지를 사용하여 스토어와 결제 시스템 간의 활동을 추적하는 방법에 대해 알아봅니다.
exl-id: 5970db88-146d-4caf-aab4-d9315357a4fe
feature: Payments
source-git-commit: 8b5af316ab1d2e632ed5fc2066974326830ab3f7
workflow-type: tm+mt
source-wordcount: '318'
ht-degree: 0%

---

# 트랜잭션

다음 _트랜잭션_ 페이지는 스토어와 결제 시스템 간에 발생한 모든 결제 활동을 나열하고 보다 자세한 정보에 대한 액세스를 제공합니다.

## 트랜잭션 보기

다음에서 _관리자_ 사이드바, 이동 **[!UICONTROL Sales]** > _[!UICONTROL Operations]_>**[!UICONTROL Transactions]**.

![트랜잭션 표](./assets/transactions.png){width="600" zoomable="yes"}

| 열 | 설명 |
|--- |--- |
| [!UICONTROL ID] | 각 트랜잭션에 지정된 고유한 숫자 식별자입니다. |
| [!UICONTROL Order ID] | 고객이 주문할 때 할당되는 고유 식별자. |
| [!UICONTROL Transaction ID] | 고객이 주문을 한 후 거래가 발생할 때 할당되는 고유 숫자 식별자입니다. |
| [!UICONTROL Parent Transaction ID] | 상위 트랜잭션의 ID 번호입니다. |
| [!UICONTROL Payment Method] | 거래와 연계된 결제 방법. |
| [!UICONTROL Transaction Type] | 주문, 승인, 캡처, 무효 또는 환불 등 거래 유형. |
| [!UICONTROL Closed] | 거래가 마감되었는지 여부. |
| [!UICONTROL Created] | 트랜잭션이 생성된 시간과 날짜. |

{style="table-layout:auto"}

## 거래 세부 정보 보기

보려는 항목을 클릭합니다.

트랜잭션 세부 정보 페이지에서 트랜잭션 세부 정보 및 하위 트랜잭션 그리드를 볼 수 있습니다.

### 거래 데이터

이 섹션에는 트랜잭션과 관련된 정보가 포함되어 있으며 **주문 ID** 열.

| 열 | 설명 |
|--- |--- |
| [!UICONTROL Transaction ID] | 거래 ID 번호입니다. |
| [!UICONTROL Parent Transaction ID] | 해당하는 경우 상위 트랜잭션의 해당 ID 번호입니다. |
| [!UICONTROL Transaction Type] | 주문, 승인, 캡처, 무효 또는 환불 등 거래 유형. |
| [!UICONTROL Is Closed] | 거래가 마감되었는지 여부. |
| [!UICONTROL Created At] | 트랜잭션이 생성된 시간과 날짜. |

{style="table-layout:auto"}

### 하위 트랜잭션

하위 트랜잭션은 다음에 대한 송장을 생성한 후 그리드에 표시됩니다. [주문 수](orders.md). 이 형식을 사용하면 트랜잭션 계층 구조를 따라 트랜잭션 내역을 추적할 수 있습니다.

### [!UICONTROL Transaction Details]

이 섹션에는 지정된 트랜잭션에 대한 추가 정보가 포함되어 있습니다. 정보는 키와 값의 형태로 표시됩니다. 사용 가능한 키는 다음과 같습니다.

- authMount
- authCode
- aVSRresponse
- 청구인
- cardCodeResponse
- 고객
- customerIP
- 라인 항목
- marketType
- 주문
- 결제
- 제품
- 자동연장 청구
- responseCode
- responseReasonCode
- responseReasonDescription
- settleamount
- 솔루션
- submitTimelocal
- submitTimeUTC
- 면세
- transactionStatus

>[!NOTE]
>
>거래 세부 정보를 사용할 수 없거나 오래된 경우 **[!UICONTROL Fetch]** 을 클릭하여 업데이트합니다.
