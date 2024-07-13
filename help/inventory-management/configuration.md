---
title: " [!DNL Inventory Management] 구성"
description: 소스 가용성, 상점 제품 및 주문 선적을 결정하는  [!DNL Inventory Management] 옵션 구성에 대해 알아봅니다.
exl-id: 1696999e-77b1-45c7-9b0b-dd1512427cff
feature: Inventory, Configuration
source-git-commit: 67cbb0d05f9f63ef51ccff3580cd27df86645fd0
workflow-type: tm+mt
source-wordcount: '770'
ht-degree: 0%

---

# [!DNL Inventory Management] 구성

[!DNL Inventory Management] 모듈은 제품 및 글로벌 수준에서 재고 구성 설정을 지원하며 소스 가용성, 상점 제품 및 주문 배송에 영향을 주는 추가 설정도 제공합니다. 구성 설정은 다음에 적용됩니다.

- 전체 카탈로그: **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**(으)로 이동합니다. 그런 다음 왼쪽 패널에서&#x200B;**[!UICONTROL Catalog]**을(를) 확장하고&#x200B;**[!UICONTROL Inventory]**을(를) 선택합니다.

- 특정 제품: **[!UICONTROL Catalog]** > **[!UICONTROL Products]**(으)로 이동합니다. 그런 다음 제품을 편집 모드로 열고 _[!UICONTROL Sources]_섹션에서&#x200B;**[!UICONTROL Advanced Inventory]**을(를) 클릭합니다.

상점 앞에 인벤토리 데이터를 표시하고 활성 장바구니를 관리하는 등의 작업을 수행하도록 카탈로그를 구성할 수 있습니다. 각 항목의 사용 가능 여부를 _재고 있음_ 또는 _재고 부족_ 및 재고가 낮을 때 사용 가능한 재고로 표시합니다.

품절 임계값은 제품을 재주문해야 하는 시점을 나타내며, 재고에 대한 판매 수량에서 뺍니다. 또한 소급 주문을 활성화하거나 비활성화하도록 설정할 수 있습니다. 스토어에 대한 미납주문을 허용하여 모든 또는 특정 제품에 대한 최대 주문 수량을 설정합니다.

재고 가용성 임계값을 사용할 수 있는 또 다른 방법은 수요가 높은 제품을 관리하는 것입니다. 대량 구매자에게 판매하지 않고 신규 고객을 포착하려는 경우 최대 수량을 설정하여 단일 구매자가 전체 재고를 반출하지 못하도록 할 수 있습니다.

![예(재고 있음), 1개만 남음](assets/storefront-stock-options-1-left.png)

## 구성 옵션

[!DNL Commerce]개의 스토어 및 제품은 제품, 인벤토리, 알림 등을 관리하기 위해 다음 구성을 지원합니다. [!DNL Commerce]은(는) 대량 작업 및 거리 우선 순위 알고리즘에 대한 추가 구성 설정을 제공합니다.

| 옵션 | 설명 |
|--|--|
| [!UICONTROL Manage Stock] | [!DNL Commerce]에서 모든 인벤토리를 관리할 수 있습니다. 이 제품이나 [!DNL Commerce]의 모든 제품에 대해 재고 관리가 사용되는지 여부를 설정합니다. `Yes`(으)로 설정된 경우 더 많은 옵션을 표시합니다. |
| [!UICONTROL Only X left Threshold] | 구매 가능한 특정 금액이 남아 있는 경우 알릴 수량을 설정합니다. 이 금액은 재고 수준에서 추적됩니다. |
| [!UICONTROL Out-of-Stock Threshold] | 안전 재고, 재고 부족 알림을 트리거하고 재고 부족 위험을 완화하는 수량입니다. 이 값은 미납주문에 영향을 줍니다. 옵션:<br />**[!UICONTROL No Backorders]**: 제품이 품절되었을 때 미납주문을 허용하지 않습니다.<br />**[!UICONTROL Allow Qty Below 0]**: 수량이 0보다 작을 때 미납주문을 허용합니다.<br />**[!UICONTROL Allow Qty Below 0 and Notify Customer]**: 수량이 영(0) 아래로 떨어지면 미납 주문을 수락하지만, 주문을 계속 할 수 있음을 고객에게 알립니다.<br /><br />**[!UICONTROL Backorders disabled]**: 5 또는 25와 같이 0보다 큰 양수 값을 입력하는 것이 좋습니다. <br/>**[!UICONTROL Backorders enabled]**: -5 또는 -25와 같이 허용되는 미납 주문의 최대 수량에 대한 음수 임계값을 입력하십시오. 값이 0이면 무한 스톡으로 작동합니다. 양의 값은 무시되고 0으로 처리됩니다. |
| [!UICONTROL Minimum Qty Allowed in Shopping Cart] | 단일 주문으로 구매할 수 있는 제품의 최소 수량을 설정합니다. |
| [!UICONTROL Maximum Qty Allowed in Shopping Cart] | 단일 주문으로 구매할 수 있는 제품의 최대 수량을 설정합니다. |
| [!UICONTROL Qty Uses Decimals] | 제품 수량에 대해 정수가 아닌 십진수를 허용합니다. 이 설정은 중량, 부피 또는 길이로 판매되는 제품에 유용합니다. Source 수준에 지정되며 지정된 소스에 따라 재고 수준에서 계산됩니다. |
| [!UICONTROL Allow Multiple Boxes for Shipping] | 제품의 부품을 별도로 배송할 수 있는지 여부를 결정합니다. 이 옵션은 **[!UICONTROL Qty Uses Decimals]** = `Yes`일 때 표시됩니다. |
| [!UICONTROL Backorders] | 미납주문 허용 여부를 나타냅니다. Source 수준에 지정되며 지정된 소스에 따라 재고 수준에서 계산됩니다. 미납주문을 허용하도록 설정된 경우, 재고 부족 임계값에 대해 음수 값을 설정하는 것이 좋습니다([미납주문 구성](backorders.md) 참조). 옵션:<br />**[!UICONTROL No Backorders]**: 제품이 품절되었을 때 미납주문을 허용하지 않습니다.<br />**[!UICONTROL Allow Qty Below 0]**: 수량이 0보다 작을 때 미납주문을 허용합니다.<br />**[!UICONTROL Allow Qty Below 0 and Notify Customer]**: 수량이 영(0) 아래로 떨어지면 미납 주문을 수락하지만, 주문을 계속 할 수 있음을 고객에게 알립니다. |
| [!UICONTROL Notify for Quantity Below] | 재고 부족을 경고하는 미달 수량 통지를 트리거하는 수량을 설정합니다. 이 금액은 재고 수량이 아니라 판매 수량에 따라 차감됩니다. |
| [!UICONTROL Enable Qty Increments] | 제품이 수량 단위로 판매될 수 있는지 여부를 결정합니다. 활성화된 경우 증분 단계에서 구매해야 하는 제품의 수량을 입력합니다. 증분 은 단일 제품으로 구매해야 하는 제품 항목 수를 구성, 그룹화 및 번들 제품의 하위 항목으로 설정합니다. |
| [!UICONTROL Automatically Return Credit Memo Item to Stock] | [!DNL Inventory Management]은(는) 이 값을 사용하지 않습니다. 반품 또는 대변 메모를 완료하면 제품 수량이 영향을 받는 출처 수량으로 자동 반환됩니다. [제품 옵션 구성](product-options.md)을 참조하세요. |

## 구성 폴백 및 상속

구성은 상속 경로 _[!UICONTROL Sources]_에 재정의되거나 적용됩니다. 제품  섹션은 제품_[!UICONTROL Advanced Options]_&#x200B;을(를) 재정의합니다. 전역 _[!UICONTROL Inventory]_저장소 구성을 재정의합니다.

[!DNL Commerce]이(가) 적용할 사용자 지정 설정을 확인하면 다음 순서를 따릅니다.

1. _[!UICONTROL Sources]_섹션의 제품 수준에서 사용자 지정 설정을 확인합니다. 몇 가지 설정을 사용할 수 있습니다.

1. 제품 _[!UICONTROL Advanced Inventory]_설정을 확인합니다.

1. 제품 설정에 대해 `Use Config Settings`을(를) 선택한 경우 전역 _인벤토리_ 저장소 구성 페이지에서 값을 확인합니다.

예를 들어 다음과 유사한 구성을 사용하여 스토어에서 미납 주문을 다르게 구성할 수 있습니다.

- _전체:_ 스토어에 대해 미납주문을 사용하도록 설정하고, 재고 부족 임계값을 `-50`(으)로 설정합니다.

- _제품:_ 특정 제품에 대한 미납주문을 사용하지 않도록 설정하고, 재고 부족 임계값을 `10`(으)로 설정합니다.
