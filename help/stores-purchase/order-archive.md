---
title: 주문 보관
description: 주문 아카이브를 구성하여 성능을 개선하고 조직의 Commerce를 간소화하는 방법에 대해 알아봅니다.
exl-id: 12025591-bfe2-4f44-9358-a38ea4493b5c
feature: Orders, Configuration
source-git-commit: 47f170f1a1dd1c236b99c2e7139bb119368abf47
workflow-type: tm+mt
source-wordcount: '745'
ht-degree: 0%

---

# 주문 보관

{{ee-feature}}

정기적으로 주문을 아카이빙하면 성능이 향상되고 불필요한 정보가 작업 공간에 남아 있지 않으므로 현재 비즈니스에 집중할 수 있습니다. 송장, 선적 및 대변 메모는 자동 또는 수동으로 보관할 수 있으며 언제든지 조회할 수 있습니다.

>[!NOTE]
>
>다음 _[!UICONTROL Archive]_옵션이에 표시됨 [[!UICONTROL Sales] 메뉴](sales-menu.md) 보관이 다음과 같은 경우에만 [활성화됨](../configuration-reference/sales/sales.md).

## 주문 아카이브 구성

지정된 일수가 지난 후 주문, 송장, 선적 및 대변 메모를 보관하도록 스토어를 구성할 수 있습니다. 주문 및 주문 관련 문서를 아카이브로 이동하거나 이전 상태로 복원할 수 있습니다. 보관된 주문은 삭제되지 않고 관리자로부터 계속 사용할 수 있습니다. 보관된 데이터를 CSV 파일로 내보내고 스프레드시트로 열 수 있습니다. 활성화하면 _보관_ 작업이 작업 영역의 맨 위에 나타납니다.

1. 다음에서 _관리자_ 사이드바, 이동 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. 왼쪽 패널에서 를 확장합니다. **[!UICONTROL Sales]** 섹션 및 선택 **[!UICONTROL Sales]** 밑에.

1. 확장 ![확장 선택기](../assets/icon-display-expand.png) 다음 **[!UICONTROL Orders, Invoices, Shipments, Credit Memos Archiving]** 섹션.

   ![주문, 송장, 선적, 대변 메모 보관 구성 설정](../configuration-reference/sales/assets/sales-orders-invoices-shipments-credit-memos-archiving.png){width="600" zoomable="yes"}

1. 설정 **[!UICONTROL Enable Archiving]** 끝 `Yes`.

   >[!NOTE]
   >
   >나중에 보관을 해제하기로 결정한 경우 보관된 모든 주문이 이전 상태로 복원됩니다.

1. 설정 **[!UICONTROL Archive Orders Purchased]** 완료된 주문이 보관되기 전까지 대기할 일 수입니다.

   기본적으로 주문은 구매 후 30일 후에 보관됩니다.

1. 다음에서 **[!UICONTROL Order Statuses to be Archived]** 목록에서 보관할 주문을 식별하는 데 사용할 각 주문 상태를 선택합니다.

   여러 항목을 선택하려면 Ctrl 키(Windows) 또는 Command 키(Mac)를 누른 채 각 항목을 클릭합니다.

1. 클릭 **[!UICONTROL Save Config]**.

1. 메시지가 표시되면 잘못된 캐시를 새로 고칩니다.

## 보관된 문서 보기

1. 다음에서 _[!UICONTROL Sales]_아래 메뉴_[!UICONTROL Archive]_&#x200B;를 클릭하고 다음 중 하나를 선택합니다.

   - **[!UICONTROL Orders]**
   - **[!UICONTROL Invoices]**
   - **[!UICONTROL Shipments]**
   - **[!UICONTROL Credit Memos]**

1. 세부 정보를 보려면 목록에서 보관된 문서를 클릭합니다.

## 보관된 문서에 작업 적용

각 문서를 작업 대상으로 선택하고 다음 중 하나를 선택합니다 **[!UICONTROL Actions]**:

- `Cancel`
- `Hold`
- `Unhold`
- `Print`
- `Move to Orders Management`

## 문서 수동 보관

1. 다음 중에서 보관할 문서 유형을 선택합니다.

   - **[!UICONTROL Orders]**
   - **[!UICONTROL Invoices]**
   - **[!UICONTROL Shipments]**
   - **[!UICONTROL Credit Memos]**

1. 보관하려는 각 항목의 확인란을 선택합니다.

1. 오른쪽 상단에서 를 설정합니다. **[!UICONTROL Actions]** 끝 `Move to Archive`.

1. 클릭 **[!UICONTROL Submit]** 을 눌러 선택한 문서를 보관합니다.

## 보관된 문서 복원

1. 복원할 문서 유형을 선택합니다.

1. 다음 옵션 중 하나를 사용하여 문서를 선택합니다.

   - 보이는 모든 문서를 선택하려면 왼쪽 상단 모서리에서 **[!UICONTROL Select Visible]**.

   - 복원할 각 문서의 확인란을 수동으로 선택합니다.

1. 오른쪽 상단에서 를 설정합니다. **[!UICONTROL Action]** 끝 `Move to Orders Management`.

1. 클릭 **[!UICONTROL Submit]** 문서를 복원합니다.

## 보관된 문서 내보내기

1. 내보낼 문서 유형을 선택합니다.

1. 오른쪽 위 메뉴에서 을(를) 설정합니다. **[!UICONTROL Export to:]** 다음 값 중 하나로 변환:

   - `CSV`
   - `Excel`

1. 클릭 **[!UICONTROL Export]**.

지정된 일수가 지난 후 주문, 송장, 선적 및 대변 메모를 보관하도록 스토어를 구성할 수 있습니다. 주문 및 주문 관련 문서를 아카이브로 이동하거나 이전 상태로 복원할 수 있습니다. 보관된 주문은 삭제되지 않고 관리자로부터 계속 사용할 수 있습니다. 보관된 데이터를 CSV 파일로 내보내고 스프레드시트로 열 수 있습니다. 활성화하면 _[!UICONTROL Archive]_작업 영역 상단에 명령이 나타납니다.

## 수동으로 주문 보관

1. 다음에서 _관리자_ 사이드바, 이동 **[!UICONTROL Sales]** > _[!UICONTROL Operations]_>**[!UICONTROL Orders]**.

1. 그리드에서 순서를 선택하려면 첫 번째 열에서 확인란을 선택합니다.

1. 설정 **[!UICONTROL Actions]** 제어 대상 `Move to Archive` 주문이 보관되었다는 메시지를 찾습니다.

   ![선택한 주문을 아카이브로 이동 ](./assets/order-move-to-archive.png){width="700" zoomable="yes"}

>[!TIP]
>
>보관할 수 있는 주문 상태 목록을 지정하려면 다음을 참조하십시오 [주문 아카이브 구성](#configure-the-order-archive).

## 보관된 주문 보기

1. 다음 방법 중 하나를 사용하여 아카이브 보기를 엽니다.

   - 위의 버튼 막대에서 _[!UICONTROL Orders]_그리드, 클릭&#x200B;**[!UICONTROL Go to Archive]**.

   - 다음에서 _관리자_ 사이드바, 이동 **[!UICONTROL Sales]** > _[!UICONTROL Archive]_>**[!UICONTROL Orders]**.

   >[!NOTE]
   >
   >주문 페이지와 마찬가지로 보관된 주문 페이지의 제목은 다음과 같습니다. _[!UICONTROL Orders]_. 유일한 차이점은 다음 작업을 수행하는 버튼 막대의 옵션입니다._[!UICONTROL Return to Orders Management]_. 또한 페이지의 URL은 주문 보관 상태임을 나타냅니다.

1. 다음에서 _작업_ 열, 클릭 **[!UICONTROL View]**.

   ![보관된 주문 보기](./assets/order-archived-view.png){width="600" zoomable="yes"}

## 보관된 주문 복원

>[!NOTE]
>
>보관된 주문에서 복원된 주문은 [!UICONTROL Archive Orders Purchased] 설정(참조) [주문 아카이브 구성](#configure-the-order-archive)). 일수는 다음에 대해 계산됩니다. [!UICONTROL Updated At] 주문의 날짜. 주문은 아카이브에서 이동될 때 변경됩니다.

1. 다음에서 _관리자_ 사이드바, 이동 **[!UICONTROL Sales]** > _[!UICONTROL Operations]_>**[!UICONTROL Orders]**.

1. 단추 모음에서 **[!UICONTROL Go to Archive]**.

1. 복원할 레코드를 찾은 다음 확인란을 클릭하여 선택합니다.

   ![복원할 순서 선택](./assets/order-archived-select-to-restore.png){width="600" zoomable="yes"}

1. 설정 **[!UICONTROL Actions]** 제어 값 대상 `Move to Order Management`.

아카이브된 주문이 아카이브에서 제거되었다는 메시지를 찾습니다.

## 보관된 주문 내보내기

1. 다음에서 _관리자_ 사이드바, 이동 **[!UICONTROL Sales]** > _[!UICONTROL Operations]_>**[!UICONTROL Orders]**.

1. 작업 메뉴에서 다음을 클릭합니다. **[!UICONTROL Export]** 을(를) 클릭하고 원하는 형식을 선택합니다.
