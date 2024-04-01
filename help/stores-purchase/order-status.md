---
title: 주문 상태
description: 사전 정의된 순서 상태와 운영 요구 사항에 맞게 사용자 정의 순서 상태를 정의하는 방법에 대해 알아봅니다.
exl-id: d1153558-a721-4643-a70c-7fc20072983c
feature: Orders
source-git-commit: c2d5e9b41a76ba58d1343a8b3ee5122104d5bfe0
workflow-type: tm+mt
source-wordcount: '1223'
ht-degree: 0%

---

# 주문 상태

모든 주문에는 주문 처리의 단계와 연관된 주문 상태가 있습니다 [워크플로우](order-processing.md).\
주문 상태와 주문 상태의 차이점은 다음과 같습니다 **[!UICONTROL order states]** 는 프로그래밍 방식으로 사용됩니다. 고객 또는 관리자 사용자는 볼 수 없습니다. 주문의 흐름과 특정 상태의 주문에 대해 가능한 작업을 결정합니다.\
**[!UICONTROL Order statuses]** 은 고객 및 관리자 사용자에게 주문 상태를 전달하는 데 사용됩니다.
운영 요구 사항에 맞게 추가 주문 상태를 생성할 수 있습니다. 주문 상태는 주문 피킹 및 납품 진행률과 같이 Adobe Commerce 외부의 진행률을 표시하는 데 편리합니다. 주문 처리 워크플로에는 영향을 주지 않습니다.\
각 주문 상태는 주문 상태와 연관됩니다. 스토어에는 사전 정의된 주문 상태 및 주문 상태 설정 세트가 있습니다.

![주문 상태 및 상태](./assets/order-states-and-statuses.png){width="700" zoomable="yes"}

각 주문의 상태는 _상태_ 열 _주문 수_ 그리드.

![주문 상태](./assets/stores-order-status-column.png){width="700" zoomable="yes"}

>[!TIP]
>
>부분적으로 환불된 주문은 다음 단계에 남아 있습니다. `Processing` 종료 상태 **_모두_** 주문된 품목(환불 품목 포함)은 배송됩니다. 주문 상태가 (으)로 변경되지 않음 `Complete` 주문의 모든 품목이 배송될 때까지.

## 주문 상태 워크플로

![주문 상태 워크플로](./assets/order-state-workflow.png)

## 사전 정의된 상태

| 주문 상태 | 상태 코드 |                                                                                                                                                                                                                                                                                        |
|--------------------------|----------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 받음 | `received` | 이 상태는 비동기 주문 배치가 활성화된 경우 주문의 초기 상태입니다. |
| 사기 혐의 | `fraud` | 경우에 따라 PayPal 또는 다른 결제 게이트웨이를 통해 결제된 주문이 _사기 혐의_. 이 상태는 주문에 발급된 송장이 없으며 확인 이메일도 전송되지 않음을 의미합니다. |
| 처리 중 | `processing` | 새 주문의 상태가 &#39;처리 중&#39;으로 설정되면 _자동으로 모든 항목 송장 발행_ 구성에서 옵션을 사용할 수 있게 됩니다. 인보이스는 기프트 카드, 스토어 크레딧, 보상 포인트 또는 기타 오프라인 결제 방법을 사용하여 수행한 주문에 대해 자동으로 생성되지 않습니다. |
| 보류 중인 결제 | `pending_payment` | 주문이 생성되고 PayPal 또는 유사한 결제 방법이 사용되는 경우 이 상태가 사용됩니다. 고객이 결제 게이트웨이 홈페이지로 이동했지만 아직 반품 정보가 들어오지 않았다는 의미다. 이 상태는 고객이 결제할 때 변경됩니다. |
| 결제 검토 | `payment_review` | 이 상태는 PayPal 결제 검토가 켜져 있을 때 나타납니다. |
| 보류 중 | `pending` | 이 상태는 송장 및 선적이 실행되지 않았음을 나타냅니다. |
| 보류 중 | `holded` | 이 상태는 수동으로만 할당할 수 있습니다. 어떤 주문이든 보류하실 수 있습니다. |
| 완료 | `complete` | 이 상태는 주문이 생성되고 지급되며 고객에게 출하되었음을 의미합니다. |
| 종료됨 | `closed` | 이 상태는 주문에 대변 메모가 지정되었고 고객이 환불을 받았음을 나타냅니다. |
| 취소됨 | `canceled` | 이 상태는 고객이 지정된 시간 내에 지불하지 않을 때 관리자에서 수동으로 할당되거나 일부 결제 게이트웨이의 경우 할당됩니다. |
| 거부됨 | `rejected` | 이 상태는 비동기 주문 처리 중 주문이 거부되었음을 의미합니다. 이 문제는 비동기 주문 배치 중에 오류가 발생할 때 발생합니다. |
| PayPal 취소 취소 | `paypay_canceled_reversal` | 이 상태는 PayPal이 취소를 취소했음을 의미합니다. |
| 보류 중인 PayPal | `pending_paypal` | 이 상태는 PayPal로 주문을 받았지만 아직 결제가 처리되지 않았음을 의미합니다. |
| PayPal 취소됨 | `paypal_reversed` | 이 상태는 PayPal이 거래를 취소했음을 의미합니다. |

{style="table-layout:auto"}

## 사용자 정의 주문 상태

사전 설정된 주문 상태 설정 외에도 사용자 지정 주문 상태 설정을 만들어 주문 상태에 할당하고 주문 상태에 대한 기본 주문 상태를 설정할 수 있습니다. 주문 상태는 주문 처리 워크플로우 내의 주문 위치를 나타내며 주문 상태는 주문 위치에 의미 있는 번역 가능한 레이블을 지정합니다. 예를 들어 다음과 같은 사용자 지정 주문 상태가 필요할 수 있습니다. `packaging"`, `backordered`또는 특정 요구 사항에만 해당하는 상태입니다. 사용자 지정 상태에 대한 수사적 이름을 만들어 워크플로우의 관련 주문 상태에 할당할 수 있습니다.

>[!NOTE]
>
>주문 워크플로우에서는 기본 사용자 지정 주문 상태 값만 사용됩니다. 기본값으로 설정되지 않은 사용자 지정 상태 값은 순서의 설명 섹션에서만 사용할 수 있습니다.

![주문 상태 설정](./assets/order-status.png){width="700" zoomable="yes"}

### 사용자 정의 주문 상태 만들기

1. 다음에서 _관리자_ 사이드바, 이동 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Order Status]**.

1. 오른쪽 위 모서리에서 을(를) 클릭합니다. **[!UICONTROL Create New Status]**.

   ![새 주문 상태 만들기](./assets/order-status-new.png){width="600" zoomable="yes"}

1. 업데이트 _[!UICONTROL Order Status Information]_섹션:

   - 입력 **[!UICONTROL Status Code]** 내부 참조용. 첫 번째 문자는 문자(a-z)여야 하고 나머지 문자는 문자와 숫자의 모든 조합(0-9)일 수 있습니다. 공백 대신 밑줄 문자를 사용하십시오.

   - 대상 **[!UICONTROL Status Label]**, 관리 및 상점 모두의 상태 설정을 식별하는 레이블을 입력합니다.

1. 다음에서 _[!UICONTROL Store View Specific Labels]_섹션에서 다양한 스토어 보기에 필요한 레이블을 입력합니다.

1. 클릭 **[!UICONTROL Save Status]**.

### 상태에 주문 상태 할당

1. 다음에서 _주문 상태_ 페이지, 클릭 **[!UICONTROL Assign Status to State]**.

   ![상태 할당](./assets/store-status-assign-status.png){width="600" zoomable="yes"}

1. 업데이트 **[!UICONTROL Assignment Information]** 섹션에서 다음을 수행합니다.

   - 다음을 선택합니다. **[!UICONTROL Order Status]** 을(를) 지정합니다. 상태 레이블별로 나열됩니다.

   - 설정 **[!UICONTROL Order State]** 주문 상태가 속한 워크플로우의 위치로 이동합니다.

     >[!NOTE]
     >
     >**_[!UICONTROL Order State]_** 목록에는 기본 지정된 주문 상태가 포함됩니다. 예를 들어 `Pending` 대신 기본 주문 상태가 표시됩니다. `New` 주문 상태 값입니다.

   - 이 상태를 주문 상태의 기본값으로 설정하려면 **[!UICONTROL Use Order Status as Default]** 확인란.

     >[!NOTE]
     >
     >주문 워크플로우에서는 기본 주문 상태만 사용됩니다. 기본값이 아닌 상태는 **[!UICONTROL Order Comments]** 섹션에 있는 마지막 항목이 될 필요가 없습니다.

   - 상점 첫 화면에서 이 상태를 표시하려면 **[!UICONTROL Visible On Storefront]** 확인란.

   ![상태에 상태 할당](./assets/order-status-assign-state.png){width="600" zoomable="yes"}

1. 클릭 **[!UICONTROL Save Status Assignment]**.

### 기존 주문 상태 편집

1. 다음에서 _[!UICONTROL Order Status]_그리드에서 상태 레코드를 편집 모드로 엽니다.

1. 필요에 따라 상태 설정을 업데이트합니다.

1. 클릭 **[!UICONTROL Save Status]**.

### 지정된 상태에서 주문 상태 제거

>[!NOTE]
>
>상태가 사용 중이면 상태에서 상태 설정을 할당 해제할 수 없습니다.

1. 다음에서 _[!UICONTROL Order Status]_그리드에서 미지정될 주문 상태 레코드를 찾습니다.

1. 다음에서 _[!UICONTROL Action]_행의 맨 오른쪽에 있는 열에서&#x200B;**[!UICONTROL Unassign]**링크를 클릭합니다.

   작업 영역 상단에 주문 상태가 할당 해제되었다는 메시지가 나타납니다. 주문 상태 레이블이 목록에 계속 표시되지만 더 이상 상태에 할당되지 않습니다. 주문 상태 설정은 삭제할 수 없습니다.

>[!NOTE]
>
>기본 주문 상태가 주문 상태에서 할당 해제된 경우 _**또 다른**_ 주문 상태: _**자동으로 설정**_ (이 주문 상태의 기본값)

## 알림

고객은 다음 방법으로 주문 상태를 추적할 수 있습니다. [RSS 피드](../merchandising-promotions/social-rss.md) 구성에서 RSS 피드 순서 지정이 활성화된 경우 활성화하면 각 주문에 RSS 피드에 대한 링크가 나타납니다.

### 주문 상태 알림 활성화

1. 다음에서 _관리자_ 사이드바, 이동 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. 왼쪽 패널에서 를 확장합니다. **[!UICONTROL Catalog]** 및 선택 **[!UICONTROL RSS Feeds]** 밑에.

1. 확장 ![확장 선택기](../assets/icon-display-expand.png) 다음 **[!UICONTROL Order]** 섹션.

1. 설정 **[!UICONTROL Customer Order Status Notification]** 끝 `Enable`.

   ![고객 주문 상태 알림](../configuration-reference/catalog/assets/rss-feeds-order.png){width="600" zoomable="yes"}

1. 완료되면 다음을 클릭하십시오. **[!UICONTROL Save Config]**.

### 새 주문 이메일 알림 구성

1. 다음에서 _관리자_ 사이드바, 이동 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. 왼쪽 패널에서 를 확장합니다. **[!UICONTROL Sales]** 및 선택 **[!UICONTROL Sales Emails]** 밑에.

1. 확장 ![확장 선택기](../assets/icon-display-expand.png) 다음 **[!UICONTROL Order]** 섹션.

   ![구성 - 주문 옵션](../configuration-reference/sales/assets/sales-emails-order.png){width="600" zoomable="yes"}

1. 설정 **[!UICONTROL New Order Confirmation Email Sender]** 다음 중 하나를 수행합니다.

   - `General Contact`
   - `Sales Representative`
   - `Customer Support`
   - `Custom Email 1`
   - `Custom Email 2`

1. 각 고객 유형에 사용할 템플릿을 선택합니다.

   - **[!UICONTROL New Order Confirmation Template]** - 스토어 계정이 등록된 고객에 사용할 템플릿을 선택합니다.
   - **[!UICONTROL New Order Confirmation Template for Guest]** - 등록된 스토어 계정이 없는 게스트 고객에 사용할 템플릿을 선택하십시오.

1. 다른 사람(예: 비즈니스 관리자)에게 새 주문에 대해 알리려면 다음으로 전자 메일 주소를 입력합니다. **[!UICONTROL Send Order Email Copy To]**.

   두 명 이상의 수신자가 필요한 경우 여러 개의 이메일 주소를 추가할 수 있습니다.

1. 설정 **[!UICONTROL Send Order Email Copy Method]** 다음 중 하나를 수행합니다.

   - `Bcc` - 신규 주문에 대한 하나의 이메일만 고객과 추가 수신자 모두에게 전송되지만 고객은 받은 이메일이 추가 수신자에게도 전송되었는지 확인하지 않습니다.
   - `Separate Email` - 두 개의 개별 이메일이 전송됩니다. 하나는 수신자에게, 하나는 고객에게 전송됩니다.

1. 완료되면 다음을 클릭하십시오. **[!UICONTROL Save Config]**.
