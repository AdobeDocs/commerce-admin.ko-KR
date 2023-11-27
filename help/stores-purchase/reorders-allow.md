---
title: 재주문 허용
description: 고객을 위한 순서 조정 기능을 제공하는 방법에 대해 알아봅니다.
exl-id: 9fe4c4fb-8596-4fd0-a93b-927ebdfc0c94
feature: Orders, Storefront
source-git-commit: 8b5af316ab1d2e632ed5fc2066974326830ab3f7
workflow-type: tm+mt
source-wordcount: '427'
ht-degree: 0%

---

# 재주문 허용

사용하도록 설정하면 고객 계정에서 직접 또는 _관리자_. 재주문은 기본적으로 활성화되어 있습니다.

![관리자의 고객 재주문 링크](./assets/customer-reorder.png){width="700" zoomable="yes"}

## 주문에 사용할 수 있는 순서 조정 기준

- 다음 _순서 재지정 허용_ 구성 옵션을 활성화해야 합니다.

- 주문된 경우 `Hold` 또는 `Payment Review` 상태, 순서 조정 옵션이 비활성화됩니다.

- 주문된 항목을 사용할 수 없거나, 재고가 없거나, 비활성화된 경우 상점 전면에서 재주문 옵션이 비활성화됩니다.

- An _관리자_ 재고가 없거나 비활성화된 항목이라도 재주문을 할 수 있습니다.

## 고객 재주문을 허용하도록 구성

1. 다음에서 _관리자_ 사이드바, 이동 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. 왼쪽 패널에서 를 확장합니다. **[!UICONTROL Sales]** 및 선택 **[!UICONTROL Sales]** 밑에.

1. 확장 ![확장 선택기](../assets/icon-display-expand.png) 다음 **[!UICONTROL Reorder]** 섹션.

   ![옵션 순서 바꾸기](../configuration-reference/sales/assets/sales-reorder.png){width="600" zoomable="yes"}

1. 설정 **[!UICONTROL Allow Reorder]** 끝 `Yes`.

   이 설정을 사용하면 관리자의 상점 또는 주문 목록에 있는 고객 계정의 순서 조정 기능을 사용할 수 있습니다.

1. 클릭 **[!UICONTROL Save Config]**.

## 상점 앞에서 순서 바꾸기

고객은 다음 두 페이지에서 특정 주문에 대한 순서 조정 기능을 시작할 수 있습니다.

- _내 주문_ 페이지

- _주문 보기_ 페이지

### 내 주문

다음 _순서 바꾸기_ 주문의 모든 제품을 재주문에 사용할 수 없는 경우에도 버튼은 항상 주문과 함께 목록에 표시됩니다.

![예제 storefront - 내 주문 페이지](./assets/my-order-page-view.png){width="700" zoomable="yes"}

**사례 1.** 주문의 모든 제품은 다음과 같습니다. **사용 가능** 순서 재지정용

사용자가 장바구니로 리디렉션되고 모든 제품이 장바구니에 추가됩니다

![장바구니](./assets/shopping-cart-page.png){width="700" zoomable="yes"}

**사례 2.** 주문의 일부/모든 제품은 다음과 같습니다 **사용할 수 없음** 순서 재지정용

>[!NOTE]
>
>순서를 변경할 수 있습니다. `Not Visible Individually` 제품.

다음 _순서 바꾸기_ 단추가 _내 주문_ 및 _주문 보기_ 페이지.

![내 주문 페이지 1](./assets/my-orders-view-page1.png){width="700" zoomable="yes"}

### 주문 보기 페이지

**사례 1.** 주문의 모든 제품은 재주문이 가능합니다

사용자가 장바구니로 리디렉션되고 모든 제품이 장바구니에 추가됩니다

**사례 2.** 주문의 일부/모든 제품은 다음과 같습니다 **사용할 수 없음** 순서 재지정용

>[!NOTE]
>
>순서를 변경할 수 있습니다. `Not Visible Individually` 제품.

다음 _순서 바꾸기_ 단추가 _내 주문_ 및 _주문 보기_ 페이지.

![주문 세부 사항 페이지](./assets/order-view-page.png){width="700" zoomable="yes"}

### 장바구니가 비어 있지 않음

장바구니가 비어 있지 않고 사용자가 를 클릭하는 경우 **[!UICONTROL Reorder]** (다음에서) _내 주문_  또는 _주문 보기_ page), 기존 제품은 추가된 재주문 제품과 함께 장바구니에 남아 있습니다.

![항목 순서 바꾸기](./assets/shopping-cart-view1.png){width="700" zoomable="yes"}

## 책임자로부터 순서 바꾸기

1. 다음에서 _관리자_ 사이드바, 이동 **[!UICONTROL Sales]** > **[!UICONTROL Orders]**.

1. 주문을 찾아서 엽니다. **[!UICONTROL View]** 모드.

1. 클릭 **[!UICONTROL Reorder]** 맨 위 단추 모음에 표시됩니다.

   ![관리자의 주문 세부 사항](./assets/order-view-admin.png){width="600" zoomable="yes"}

   을(를) 클릭한 후 **[!UICONTROL Reorder]**, _새 주문 만들기_ 제품 순서 변경 페이지가 열립니다.

   ![순서 바꾸기 만들기](./assets/create-reorder-page.png){width="600" zoomable="yes"}

1. 필요에 따라 모든 필수 필드를 완료합니다.

1. 주문을 제출하려면 **[!UICONTROL Submit Order]**.
