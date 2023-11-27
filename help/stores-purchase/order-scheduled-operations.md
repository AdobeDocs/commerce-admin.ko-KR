---
title: 예약된 주문 작업
description: 이 기능을 지원하는 예약된 주문 작업 및 주문 cron 설정에 대해 알아봅니다.
exl-id: 330fe75a-d901-4696-946e-fa7af9ea3d40
feature: Orders, Configuration
source-git-commit: db859c40cd6f052a8f1153e245c23d9f1ea97d33
workflow-type: tm+mt
source-wordcount: '248'
ht-degree: 0%

---

# 예약된 주문 작업

사용 [크론](../systems/cron.md) 다음 주문 처리 작업을 예약하는 작업:

![주문 그리드](./assets/orders-grid.png){width="700" zoomable="yes"}

## 보류 중인 결제 주문 수명 설정

보류 중인 지급이 있는 주문 수명은 다음에 의해 결정됩니다. _주문 크론 설정_ 구성. 기본값은 8시간인 480분으로 설정되어 있습니다.

1. 다음에서 _관리자_ 사이드바, 이동 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. 왼쪽 패널에서 를 확장합니다. **[!UICONTROL Sales]** 섹션 및 선택 **[!UICONTROL Sales]** 밑에.

1. 확장 ![확장 선택기](../assets/icon-display-expand.png) 다음 **[!UICONTROL Orders Cron Settings]** 섹션.

   ![주문 크론 설정](../configuration-reference/sales/assets/sales-orders-cron-settings.png){width="600" zoomable="yes"}

1. 대상 **[!UICONTROL Pending Payment Order Lifetime (minutes)]**&#x200B;을(를) 클릭하고 보류 중인 지급이 만료되기 전 시간(분)을 입력합니다.

1. 클릭 **[!UICONTROL Save Config]**.

## 예약된 그리드 업데이트 및 리인덱싱 활성화

그리드 설정 구성은 다음 Order Management 그리드에 대한 갱신을 예약하고 예약된 대로 데이터를 다시 인덱싱합니다 [크론](../systems/cron.md):

- [주문 수](orders.md#orders-workspace)
- [인보이스](invoices.md)
- [배송](shipments.md)
- [대변 메모](credit-memos.md)

이러한 작업을 예약하면 데이터를 저장할 때 발생하는 잠금을 방지하고 처리 시간을 줄일 수 있습니다. 활성화되면 예약된 cron 작업 중에만 업데이트가 발생합니다. 최상의 결과를 얻으려면 Cron 이 1분에 한 번 실행되도록 구성해야 합니다.

**_업데이트 및 색인 재지정을 활성화하려면 다음을 수행하십시오._**

날짜 [프로덕션 모드](https://experienceleague.adobe.com/docs/commerce-operations/configuration-guide/setup/application-modes.html#production-mode) (클라우드 인프라의 Adobe Commerce에 사용되는 기본 모드)이 활성화되어 있으면 다음 명령을 실행합니다.

``bin/magento config:set dev/grid/async_indexing 1``

날짜 [기본 모드](https://experienceleague.adobe.com/docs/commerce-operations/configuration-guide/setup/application-modes.html#default-mode) 이(가) 활성화되면 다음 단계를 완료하십시오.

1. 다음에서 _관리자_ 사이드바, 이동 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. 왼쪽 패널에서 를 확장합니다. **[!UICONTROL Advanced]** 섹션 및 선택 **[!UICONTROL Developer]**.

1. 확장 ![확장 선택기](../assets/icon-display-expand.png) 다음 **[!UICONTROL Grid Settings]** 섹션.

1. 설정 **[!UICONTROL Asynchronous Indexing]** 끝 `Enable`.

   ![그리드 설정](../configuration-reference/advanced/assets/developer-grid-settings.png){width="600" zoomable="yes"}

1. 클릭 **[!UICONTROL Save Config]**.
