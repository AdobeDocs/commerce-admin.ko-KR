---
title: '[!UICONTROL My Requisition Lists]'
description: 계정 대시보드에서 사용할 수 있는 구매요청 목록의 고객 환경에 대해 알아봅니다.
exl-id: ed1b41aa-9c36-49f8-80f2-ad0eb151b7a5
feature: B2B, Companies
source-git-commit: c94d4e8d13c32c1c1b1d37440fdb953c8527b76c
workflow-type: tm+mt
source-wordcount: '486'
ht-degree: 2%

---

# [!UICONTROL My Requisition Lists]

구매요청 목록을 유지하는 주된 이유는 제품의 재주문을 쉽게 하기 위해서입니다. 승인된 고객은 구매 요청 목록에서 장바구니에 항목을 추가하여 쉽게 재주문하고 한 목록에서 다른 목록으로 항목을 이동하거나 복사할 수 있습니다.

![내 구매요청 목록](./assets/account-dashboard-my-requisition-lists.png){width="700" zoomable="yes"}

## 구매요청 목록 열기

1. 고객은 계정 대시보드에서 다음을 선택합니다 **[!UICONTROL My Requisition Lists]**.

1. 열려는 구매요청 목록을 찾아 클릭합니다. **[!UICONTROL View]** 다음 중 하나를 수행합니다.

### 장바구니에 제품 추가

1. 고객은 다음 중 하나를 수행하여 추가할 제품을 선택합니다.

   - 각 항목의 확인란을 선택합니다.
   - 클릭수 **[!UICONTROL Select All]**.

1. 다음을 입력합니다. **[!UICONTROL Qty]** 장바구니에 추가됩니다.

1. 제품 옵션을 변경하려면 다음을 수행합니다.

   - 라인 항목에서 _편집_ (![연필 아이콘](../assets/icon-edit-pencil.png)) 아이콘.
   - 필요한 모든 옵션을 변경합니다.
   - 클릭수 **[!UICONTROL Update Requisition List]**.

1. 클릭수 **[!UICONTROL Add to Cart]**.

   ![구매요청 목록 상세내역](./assets/requisition-list-view.png){width="700" zoomable="yes"}

### 다른 목록에 항목 복사

1. 고객은 이동할 각 항목의 확인란을 선택합니다.

1. 클릭수 **[!UICONTROL Copy Selected]** 및 은 다음 중 하나를 수행합니다.

   - 기존 구매요청 목록을 선택합니다.
   - 클릭수 **[!UICONTROL Create New Requisition List]**.

### 목록 내보내기

1. 고객은 익스포트할 구매요청 목록을 엽니다.

1. 클릭 수: **[!UICONTROL Export]** 링크를 클릭합니다.

Adobe Commerce은 를 사용하여 CSV 목록을 생성하고 다운로드합니다. `sku` 및 `qty` 값.

### 항목을 다른 목록으로 이동

1. 고객은 이동할 각 항목의 확인란을 선택합니다.

1. 클릭수 **[!UICONTROL Move Selected]** 다음 중 하나를 수행합니다.

   - 기존 구매요청 목록을 선택합니다.
   - 클릭수 **[!UICONTROL Create New Requisition List]**.

### 목록 인쇄

1. 목록의 오른쪽 상단 모서리에서 고객이 클릭합니다 **[!UICONTROL Print]**.

1. 출력 장치를 확인하고 클릭합니다. **[!UICONTROL Print]**.

   ![구매요청 목록 인쇄](./assets/requisition-list-print.png){width="500" zoomable="yes"}

### 제품 옵션 편집

목록에서 제품 옵션을 편집하려면 다음과 같이 하십시오.

1. 클릭 수: _연필_ (![연필 아이콘](../assets/icon-edit-pencil.png)) 아이콘을 클릭하여 제품 페이지를 엽니다.

1. 필요한 모든 옵션을 변경합니다.

1. 클릭수 **[!UICONTROL Update Requisition List]**.

   ![구매요청 목록 갱신](./assets/requisition-list-update.png){width="700" zoomable="yes"}

구매요청 목록의 제품은 다음과 같은 경우에 편집할 수 있습니다.

- 제품에 다음이 있습니다. **[!UICONTROL all options set]** (일 때 [구성된 제품](../catalog/product-create-configurable.md) (구매요청 목록).

  제품: **[!UICONTROL added to this Requisition List]**.

- 제품: [옵션을 갖춘 간단한 제품](../catalog/settings-advanced-custom-options.md)

- 제품 유형에 대해 편집이 허용됩니다.

### 항목 제거

1. 고객은 제거할 각 항목의 확인란을 선택합니다.

1. 클릭수 **[!UICONTROL Remove Selected]**.

1. 확인 메시지가 표시되면 **[!UICONTROL Delete]**.

### 목록 이름 바꾸기

1. 목록 제목 다음에 고객이 클릭 **[!UICONTROL Rename]**.

1. 다른 항목 입력 **[!UICONTROL Requisition List Name]**.

1. 클릭수 **[!UICONTROL Save]**.

   ![구매요청 목록 이름 바꾸기](./assets/requisition-list-rename.png){width="300"}


### 구매요청 목록 제거

1. 고객이 삭제할 구매요청 목록을 엽니다.

1. 클릭수 **[!UICONTROL Delete Requisition List]**.

1. 확인 메시지가 표시되면 **[!UICONTROL Delete]**.

>[!NOTE]
>
>이 작업은 취소할 수 없습니다.

## 작업

| 작업 | 설명 |
|--- |--- |
| [!UICONTROL Rename] | 구매요청 목록의 이름을 바꾸고 설명을 갱신할 수 있습니다. |
| [!UICONTROL Export] | 구매요청 목록을 CSV 파일로 내보냅니다. |
| [!UICONTROL Print] | 현재 구매요청 목록을 인쇄합니다. |
| [!UICONTROL Select] | 작업의 주체가 될 항목 선택을 관리합니다. <br/>**[!UICONTROL Select All]**- 구매요청 목록의 모든 품목을 선택합니다.<br/>**[!UICONTROL Remove Selected]** - 구매요청 목록에서 선택한 모든 품목을 제거합니다. <br/>**[!UICONTROL Copy Selected]**- 선택한 모든 품목을 다른 구매요청 목록에 복사합니다. |
| [!UICONTROL Add to Cart] | 선택한 항목을 장바구니에 추가합니다. |
| [!UICONTROL Update List] | 수량 변경을 반영하도록 소계를 다시 계산합니다. |
| [!UICONTROL Delete Requisition List] | 회사 사용자 계정에서 구매요청 목록을 삭제합니다. |

{style="table-layout:auto"}
