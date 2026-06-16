---
title: 주문 취소 허용
description: 고객을 위한 취소 기능을 제공하는 방법을 알아봅니다.
feature: Orders, Storefront
exl-id: 5a8ef668-f929-4188-8574-0bccdd076f3e
TQID: https://experienceleague.adobe.com/a0jMKgF4a0qXUe15oT2syai6-kGSegU1BX56PO9SSKs
product_v2: id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2: id: c1256247-af4b-46d8-9dca-0c654ecfa157id: d1e21356-0064-4f48-9089-16e3f0dbd2a6id: dac87252-6066-4d6e-a9d2-f6d84c323de7
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
level_v2: id: b5a62a22-46f7-4f0d-b151-3fc640bef588id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2: id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 291
ht-degree: 0%

---

# 주문 취소 허용

활성화되면 고객 계정에서 직접 주문을 취소할 수 있습니다. 취소는 기본적으로 비활성화되어 있습니다.

## 주문에 대해 사용할 수 있는 취소 기준

- _주문 취소 허용_ 구성 옵션을 사용하도록 설정해야 합니다.

- 주문이 `Hold`, `Canceled`, `Complete` 또는 `Closed` 상태인 경우 상점 전면에서 취소 옵션이 비활성화됩니다.

- 주문된 제품 중 하나라도 배송된 경우 상점 전면에서 취소 옵션이 비활성화됩니다.

- 일부 유료 항목이 있는 경우 취소 옵션이 활성화되고 해당 항목에 대한 환불이 생성됩니다.

- 주문이 `Pending` 또는 `Processing` 상태인 경우 상점에서 취소 옵션을 사용할 수 있습니다.

## 고객이 취소할 수 있도록 를 구성하고 취소 이유를 사용자 지정합니다.

1. _관리자_ 사이드바에서 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**(으)로 이동합니다.

1. 왼쪽 패널에서 **[!UICONTROL Sales]**&#x200B;을(를) 확장하고 **[!UICONTROL Sales]**&#x200B;을(를) 선택합니다.

1. **[!UICONTROL Order cancellation]** 섹션에서 ![확장 선택기](../assets/icon-display-expand.png)를 확장합니다.

   ![주문 취소 옵션](../configuration-reference/sales/assets/sales-order-cancellation.png){width="600" zoomable="yes"}

1. **[!UICONTROL Order cancellation through GraphQL]**&#x200B;을(를) `Yes`(으)로 설정합니다.

   이 설정을 사용하면 상점 첫 화면에서 고객 계정의 취소 기능을 사용할 수 있습니다.

1. **[!UICONTROL Order Order cancellation reasons]**&#x200B;에서 취소 이유를 추가, 삭제 또는 수정할 수 있습니다.

   이 설정을 사용하면 고객이 주문을 취소할 때 취소 사유가 상점 앞에 표시됩니다.
이유를 하나 이상 지정했는지 확인하십시오.

1. **[!UICONTROL Save Config]**&#x200B;을(를) 클릭합니다.

## 상점에서 취소

고객은 다음 세 페이지에서 특정 주문에 대한 취소 기능을 시작할 수 있습니다.

- _내 주문_ 페이지

- _주문 보기_ 페이지

- _내 계정_ 페이지

### 내 주문

주문을 취소할 수 있는 경우 _주문 취소_ 단추가 내 주문 페이지에 표시됩니다.

![상점 예시 - 내 주문 페이지](./assets/my-order-page-view-cancel.png){width="700" zoomable="yes"}

### 주문 보기 페이지

주문을 취소할 수 있는 경우 _주문 취소_ 단추가 주문 보기 페이지에 표시됩니다.

![주문 세부 사항 페이지](./assets/order-view-page-cancel.png){width="700" zoomable="yes"}

### 내 계정

주문을 취소할 수 있는 경우 _주문 취소_ 단추가 내 계정 페이지의 최근 주문 섹션에 표시됩니다.

![내 계정 페이지](./assets/my-account-page-view-cancel.png){width="700" zoomable="yes"}
