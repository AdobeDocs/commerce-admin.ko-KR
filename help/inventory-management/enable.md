---
title: "사용 [!DNL Inventory Management]"
description: 활성화 방법 알아보기 [!DNL Inventory Management] 글로벌 스토어 또는 제품 수준에서.
exl-id: 89bd2f8b-b9e4-4b9a-b729-f7bd71f764c9
feature: Inventory, Configuration
source-git-commit: 4d89212585fa846eb94bf83a640d0358812afbc5
workflow-type: tm+mt
source-wordcount: '335'
ht-degree: 0%

---

# 사용 [!DNL Inventory Management]

제품 인벤토리를 관리하려면 [!DNL Inventory Management] 글로벌 스토어 또는 제품 수준에서. 다음의 경우 _재고 관리_ 옵션이 활성화되었습니다. [!DNL Inventory Management] 구성된 재고 및 소스를 통해 사이트에서 사용할 수 있는 제품 수량을 자동으로 추적합니다. 모든 기능과 옵션은 활성화되면 추가 구성 없이 추적 및 보고를 시작합니다.

비즈니스는 판매 속도로 실행되고 인벤토리가 업데이트됩니다. 고객이 쇼핑할 때 판매 채널 및 출처별로 사용 가능한 재고에 대한 정확한 업데이트 정보를 받게 됩니다. 고객이 장바구니에 제품을 추가하고 구매를 완료하고 사용자가 주문을 관리하고 납품을 생성하고 환불을 발행할 때 가용 판매 수량이 재고별로 갱신됩니다. 신규 또는 이전된 재고가 출처로 갱신되며, 즉시 온라인 판매에 이용 가능합니다. 미납주문은 무한 주문이나 추가 구성 없이 지정된 임계값까지 완료됩니다. 또한 추천과 함께 하나 이상의 출처에 대해 부분 또는 전체 출하를 입력하고 완료함으로써 주문 이행 및 현재고를 완벽하게 제어할 수 있습니다.

>[!NOTE]
>
>기본적으로, [!DNL Inventory Management] 설치 또는 업그레이드 시 활성화됨 [!DNL Commerce]. 비즈니스 요구 사항에 따라 추적된 을 활성화하거나 비활성화할 수 있습니다 [!DNL Inventory Management] 다음 범위 내 [!DNL Commerce].

단일 및 다중 소스 인벤토리에서 이 설정이 작동하는 방식:

- 사용 [!DNL Inventory Management], 활성화 _[!UICONTROL Manage Stock]_.

- [!UICONTROL Manage Stock] 제품 수준 구성의 설정은 저장소 구성을 재정의합니다.

- Order Management 또는 타사 서비스(예: ERP)를 사용하려면 [!UICONTROL Manage Stock].

- 제품 수준 구성에서 시스템 기본값을 사용하는 경우 저장소 구성이 재정의됩니다.

포함 [!DNL Inventory Management] 활성화하면 다음을 참조하여 모든 설정을 구성합니다.

- [전역 옵션 구성](global-options.md) - 전체 카탈로그에 영향을 주는 설정이며, 시스템 기본 설정으로 간주됩니다.

- [제품 옵션 구성](product-options.md) - 글로벌 옵션을 재정의하는 특정 제품에 대한 설정입니다.

## 활성화 또는 비활성화 [!DNL Inventory Management]

1. 다음에서 _관리자_ 사이드바, 이동 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. 왼쪽 패널에서 를 확장합니다. **[!UICONTROL Catalog]** 및 선택 **[!UICONTROL Inventory]**.

1. 확장 ![확장 선택기](../assets/icon-display-expand.png) _제품 스톡 옵션_ 및 구성:

   ![제품 스톡 옵션](assets/config-catalog-inventory-product-stock-options.png){width="600" zoomable="yes"}

   - 인벤토리를 관리하고 모두 사용하려면 [!DNL Commerce] 기능, 설정 **[!UICONTROL Manage Stock]** 끝 `Yes` (기본값).

   - 비활성화하려면 [!DNL Inventory Management], 선택 해제 **[!UICONTROL Use system value]** 확인란 및 설정 **[!UICONTROL Manage Stock]** 끝 `No`.

1. 완료되면 다음을 클릭하십시오. **[!UICONTROL Save Config]**.

## 스토어의 재고 관리

다음을 참조하십시오 [글로벌 옵션 구성](global-options.md).

## 제품에 대한 재고 관리

다음을 참조하십시오 [제품 옵션 구성](product-options.md).
