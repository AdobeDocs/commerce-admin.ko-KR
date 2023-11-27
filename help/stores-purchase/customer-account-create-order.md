---
title: 주문 만들기
description: Commerce 관리에서 고객에 대한 주문을 만드는 방법을 알아봅니다.
exl-id: 8a766a5b-55d6-4d78-859e-38937e0183d3
feature: Orders, Customer Service
source-git-commit: 8b5af316ab1d2e632ed5fc2066974326830ab3f7
workflow-type: tm+mt
source-wordcount: '366'
ht-degree: 1%

---

# 주문 만들기

지원이 필요한 등록 고객의 경우 책임자로부터 직접 전체 주문을 만들 수 있습니다. 다음 _[!UICONTROL Create New Order]_양식에는 고객 계정 대시보드의 활동 요약과 함께 일반 체크아웃 프로세스에 필요한 모든 정보가 포함됩니다.

![고객에 대한 주문 생성](./assets/create-new-order.png){width="700" zoomable="yes"}

## 1단계: 주문 만들기

1. 다음에서 _관리자_ 사이드바, 클릭 **[!UICONTROL Customers]**.

1. 그리드에서 고객을 찾습니다.

1. 다음에서 _작업_ 열, 클릭 **[!UICONTROL Edit]**.

1. 작업 영역 헤더에서 **[!UICONTROL Create Order]**.

   ![작업 영역 헤더](./assets/order-create-buttons.png){width="700" zoomable="yes"}

   다음 항목에서 주문을 만들 수도 있습니다. [작업 영역 순서 지정](orders.md#orders-workspace) 다음을 클릭: **[!UICONTROL Create New Order]**.

## 2단계: 제품 추가

스토어에 여러 개의 보기가 있는 경우 주문을 넣을 스토어 보기를 선택합니다.

### 에서 제품 추가 [!UICONTROL Customer's Activities] 사이드바

고객의 위시리스트나 최근에 본 항목, 비교한 항목 또는 주문한 항목을 장바구니에 전송할 수 있습니다.

1. 확장 ![확장 선택기](../assets/icon-display-expand.png) 다음 섹션 중 하나:

   - **[!UICONTROL Wish List]**
   - **[!UICONTROL Last Ordered Items]**
   - **[!UICONTROL Products in Comparison List]**
   - **[!UICONTROL Recently Compared Products]**
   - **[!UICONTROL Recently Viewed Products]**

1. 왼쪽 패널에서 각 제품의 확인란을 선택합니다.

1. 아래로 스크롤하여 클릭 **[!UICONTROL Update Changes]**.

   항목이 주문 양식에 나타납니다.

   ![장바구니에 추가](./assets/create-order-add-wishlist.png){width="600" zoomable="yes"}

### 카탈로그에서 제품 추가

1. 클릭 **[!UICONTROL Add Products]**.

   ![제품 추가](./assets/account-add-wishlist-product.png){width="600" zoomable="yes"}

1. 그리드에서 장바구니에 추가할 각 제품의 확인란을 선택하고 **[!UICONTROL Qty]** 구매해야 합니다.

   ![제품 선택](./assets/create-order-from-catalog.png){width="600" zoomable="yes"}

   >[!NOTE]
   >
   >제품 선택 그리드는 항상 할인과 장바구니 또는 그룹 가격 규칙이 적용되지 않은 제품에 대한 일반 기본 가격을 표시합니다. 최종 제품 가격은 제품이 주문/장바구니에 추가된 경우에만 계산됩니다.

1. 사용 가능한 제품 옵션 구성:

   - 클릭 **[!UICONTROL Configure]**.

   - 필요에 따라 옵션을 완료합니다.

   - 클릭 **[!UICONTROL OK]**.

   - 클릭 **[!UICONTROL Add Selected Product(s) to Order]** 장바구니를 업데이트합니다.

1. 제품에 대해 가 구성된 경우 [선물 옵션](../catalog/product-gift-options.md)필요한 경우 옵션을 설정합니다.

1. 필요한 경우 품목 가격 대체:

   - 다음 항목 선택 **[!UICONTROL Custom Price]** 확인란을 선택하고 아래 상자에 새 가격을 입력합니다.

   - 장바구니 합계를 업데이트하려면 다음을 클릭하십시오. **[!UICONTROL Update Items and Quantities]**.

   ![사용자 정의 가격](./assets/create-order-custom-price.png){width="600" zoomable="yes"}

1. 주문에 필요한 경우 다음 섹션을 완료합니다.

   - [!UICONTROL Order Currency]
   - [!UICONTROL Apply Coupon Codes / Gift Card Code]
   - [!UICONTROL Payment Method]
   - [!UICONTROL Shipping Method]
   - [!UICONTROL Order Comments]

>[!NOTE]
>
>다음을 참조하십시오. [결제 서비스 안내서](https://experienceleague.adobe.com/docs/commerce-merchant-services/payment-services/create-order.html) 결제 서비스 확장이 설치 및 구성된 경우 이 기능을 지원하는 결제 방법에 대한 자세한 내용을 보려면 를 참조하십시오.

## 3단계: 주문 실행

클릭 **[!UICONTROL Submit Order]**.

확인이 고객에게 전송되고 고객은 계정에서 주문 세부 사항을 볼 수 있습니다.
