---
title: ' [!DNL Inventory Management] 사용'
description: 글로벌 스토어 또는 제품 수준에서  [!DNL Inventory Management] 을(를) 사용하도록 설정하는 방법에 대해 알아봅니다.
exl-id: 89bd2f8b-b9e4-4b9a-b729-f7bd71f764c9
feature: Inventory, Configuration
source-git-commit: 4d89212585fa846eb94bf83a640d0358812afbc5
workflow-type: tm+mt
source-wordcount: '335'
ht-degree: 0%

---

# [!DNL Inventory Management] 사용

제품 인벤토리를 관리하려면 글로벌 스토어 또는 제품 수준에서 [!DNL Inventory Management]을(를) 사용하도록 설정하십시오. _재고 관리_ 옵션이 활성화되면 [!DNL Inventory Management]은(는) 구성된 재고 및 소스를 통해 사이트에서 사용할 수 있는 제품 수량을 자동으로 추적합니다. 모든 기능과 옵션은 활성화되면 추가 구성 없이 추적 및 보고를 시작합니다.

비즈니스는 판매 속도로 실행되고 인벤토리가 업데이트됩니다. 고객이 쇼핑할 때 판매 채널 및 출처별로 사용 가능한 재고에 대한 정확한 업데이트 정보를 받게 됩니다. 고객이 장바구니에 제품을 추가하고 구매를 완료하고 사용자가 주문을 관리하고 납품을 생성하고 환불을 발행할 때 가용 판매 수량이 재고별로 갱신됩니다. 신규 또는 이전된 재고가 출처로 갱신되며, 즉시 온라인 판매에 이용 가능합니다. 미납주문은 무한 주문이나 추가 구성 없이 지정된 임계값까지 완료됩니다. 또한 추천과 함께 하나 이상의 출처에 대해 부분 또는 전체 출하를 입력하고 완료함으로써 주문 이행 및 현재고를 완벽하게 제어할 수 있습니다.

>[!NOTE]
>
>[!DNL Commerce]을(를) 설치하거나 업그레이드할 때 기본적으로 [!DNL Inventory Management]이(가) 활성화됩니다. 비즈니스 요구 사항에 따라 [!DNL Commerce] 내에서 추적된 [!DNL Inventory Management]을(를) 활성화하거나 비활성화할 수 있습니다.

단일 및 다중 소스 인벤토리에서 이 설정이 작동하는 방식:

- [!DNL Inventory Management]을(를) 사용하려면 _[!UICONTROL Manage Stock]_을(를) 사용하도록 설정하십시오.

- 제품 수준 구성의 [!UICONTROL Manage Stock] 설정이 저장소 구성을 재정의합니다.

- Order Management 또는 타사 서비스(예: ERP)를 사용하려면 [!UICONTROL Manage Stock]을(를) 사용하지 않도록 설정하십시오.

- 제품 수준 구성에서 시스템 기본값을 사용하는 경우 저장소 구성이 재정의됩니다.

[!DNL Inventory Management]이(가) 활성화되면 다음을 참조하여 모든 설정을 구성하십시오.

- [전역 옵션 구성](global-options.md) - 전체 카탈로그에 영향을 주는 설정이며 시스템 기본 설정으로 간주됩니다.

- [제품 옵션 구성](product-options.md) - 전역 옵션을 재정의하는 특정 제품에 대한 설정입니다.

## [!DNL Inventory Management] 사용 또는 사용 안 함

1. _관리자_ 사이드바에서 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**(으)로 이동합니다.

1. 왼쪽 패널에서 **[!UICONTROL Catalog]**&#x200B;을(를) 확장하고 **[!UICONTROL Inventory]**&#x200B;을(를) 선택합니다.

1. ![확장 선택기](../assets/icon-display-expand.png) _제품 스톡 옵션_&#x200B;을 확장하고 다음을 구성합니다.

   ![제품 재고 옵션](assets/config-catalog-inventory-product-stock-options.png){width="600" zoomable="yes"}

   - 인벤토리를 관리하고 모든 [!DNL Commerce] 기능을 사용하려면 **[!UICONTROL Manage Stock]**&#x200B;을(를) `Yes`(으)로 설정합니다(기본값).

   - [!DNL Inventory Management]을(를) 비활성화하려면 **[!UICONTROL Use system value]** 확인란의 선택을 취소하고 **[!UICONTROL Manage Stock]**&#x200B;을(를) `No`(으)로 설정하십시오.

1. 완료되면 **[!UICONTROL Save Config]**&#x200B;을(를) 클릭합니다.

## 스토어의 재고 관리

[전역 옵션 구성](global-options.md)을 참조하십시오.

## 제품에 대한 재고 관리

[제품 옵션 구성](product-options.md)을 참조하세요.
