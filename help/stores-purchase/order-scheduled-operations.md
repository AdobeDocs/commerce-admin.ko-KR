---
title: 예약된 주문 작업
description: 이 기능을 지원하는 예약된 주문 작업 및 주문 cron 설정에 대해 알아봅니다.
exl-id: 330fe75a-d901-4696-946e-fa7af9ea3d40
feature: Orders, Configuration
source-git-commit: db859c40cd6f052a8f1153e245c23d9f1ea97d33
workflow-type: tm+mt
source-wordcount: '235'
ht-degree: 0%

---

# 예약된 주문 작업

[Cron](../systems/cron.md) 작업을 사용하여 다음 주문 처리 작업을 예약하십시오.

![주문 표](./assets/orders-grid.png){width="700" zoomable="yes"}

## 보류 중인 결제 주문 수명 설정

보류 중인 결제가 있는 주문의 수명은 _주문 크론 설정_ 구성에 의해 결정됩니다. 기본값은 8시간인 480분으로 설정되어 있습니다.

1. _관리자_ 사이드바에서 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**(으)로 이동합니다.

1. 왼쪽 패널에서 **[!UICONTROL Sales]** 섹션을 확장하고 아래의 **[!UICONTROL Sales]**&#x200B;을(를) 선택합니다.

1. **[!UICONTROL Orders Cron Settings]** 섹션에서 ![확장 선택기](../assets/icon-display-expand.png)를 확장합니다.

   ![주문 크론 설정](../configuration-reference/sales/assets/sales-orders-cron-settings.png){width="600" zoomable="yes"}

1. **[!UICONTROL Pending Payment Order Lifetime (minutes)]**&#x200B;의 경우 보류 중인 지급이 만료될 때까지 시간(분)을 입력하십시오.

1. **[!UICONTROL Save Config]**&#x200B;을(를) 클릭합니다.

## 예약된 그리드 업데이트 및 리인덱싱 활성화

그리드 설정 구성은 다음 Order Management 그리드에 대한 업데이트를 예약하며 [Cron](../systems/cron.md)에 의해 예약된 대로 데이터를 다시 인덱싱합니다.

- [주문 수](orders.md#orders-workspace)
- [인보이스](invoices.md)
- [배송](shipments.md)
- [대변 메모](credit-memos.md)

이러한 작업을 예약하면 데이터를 저장할 때 발생하는 잠금을 방지하고 처리 시간을 줄일 수 있습니다. 활성화되면 예약된 cron 작업 중에만 업데이트가 발생합니다. 최상의 결과를 얻으려면 Cron 이 1분에 한 번 실행되도록 구성해야 합니다.

**_업데이트 및 리인덱싱을 사용하려면:_**

[프로덕션 모드](https://experienceleague.adobe.com/docs/commerce-operations/configuration-guide/setup/application-modes.html#production-mode)(클라우드 인프라의 Adobe Commerce에서 사용되는 기본 모드)가 활성화되면 다음 명령을 실행합니다.

``bin/magento config:set dev/grid/async_indexing 1``

[기본 모드](https://experienceleague.adobe.com/docs/commerce-operations/configuration-guide/setup/application-modes.html#default-mode)를 사용하면 다음 단계를 완료하십시오.

1. _관리자_ 사이드바에서 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**(으)로 이동합니다.

1. 왼쪽 패널에서 **[!UICONTROL Advanced]** 섹션을 확장하고 **[!UICONTROL Developer]**&#x200B;을(를) 선택합니다.

1. **[!UICONTROL Grid Settings]** 섹션에서 ![확장 선택기](../assets/icon-display-expand.png)를 확장합니다.

1. **[!UICONTROL Asynchronous Indexing]**&#x200B;을(를) `Enable`(으)로 설정합니다.

   ![눈금 설정](../configuration-reference/advanced/assets/developer-grid-settings.png){width="600" zoomable="yes"}

1. **[!UICONTROL Save Config]**&#x200B;을(를) 클릭합니다.
