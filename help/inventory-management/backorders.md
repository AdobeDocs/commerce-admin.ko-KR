---
title: "구성 [!DNL Inventory Management] 미납 주문"
description: 품절 제품 판매를 지원하기 위해 미납주문을 구성하는 방법에 대해 알아봅니다.
exl-id: 2fe778df-781e-4cda-8b85-47cf973c9e94
feature: Inventory, Orders
source-git-commit: 4d89212585fa846eb94bf83a640d0358812afbc5
workflow-type: tm+mt
source-wordcount: '735'
ht-degree: 0%

---

# 구성 [!DNL Inventory Management] 미납 주문

미납주문을 사용하면 수량이 0이 되거나 재고가 사실상 소진된 후에도 스토어에서 제품을 계속 판매할 수 있습니다. 고객 주문이 미납주문인 경우 자금이 즉시 승인되고 수집되며, 주문의 처리 상태가 변경되지 않으며, 재고를 사용할 수 있을 때까지 배송이 보류 상태로 유지됩니다.

스토어와 판매에 따라 다음 레벨에서 미납주문을 사용가능 또는 사용불능으로 설정할 수 있습니다.

- **[!UICONTROL Global]** - 사이트 수준의 카탈로그에 있는 모든 제품

- **[!UICONTROL Product]** - 사이트, 소스 및 재고에 대한 설정을 오버라이드하는 특정 제품

## 미납 주문 설정 이해

미납 주문을 가장 잘 지원하기 위해 특정 임계값 및 설정을 구성하는 것이 좋습니다.

### 재고 부족 임계값

이 임계값에 대해 음수 값을 사용하여 제품이 실제로 품절로 간주되기 전에 미납주문될 수 있는 제품의 최대 수량을 설정합니다. 이 금액은 판매 가능한 수량에 추가됩니다. 제품 수준에서 설정된 값은 글로벌 수준에서 설정된 모든 값을 무시합니다.

판매 가능 수량의 공식은 다음과 같습니다. `(Quantity - (Out-of-Stock Threshold))`.

다음은 한 예입니다.

- 수량: 25
- 아래 수량에 대해 알림: 10
- X만 왼쪽 임계값: 5
- 재고 부족 임계값: -50

이 제품의 판매 수량은 다음과 같습니다. `75 (25 - (-50))`.

![미납주문 사용 전 판매 가능 수량 예](assets/inventory-backorders-before.png){width="600" zoomable="yes"}

![미납주문 사용가능 후 판매 가능 수량 예](assets/inventory-backorders-after.png){width="600" zoomable="yes"}

고객이 사용 가능한 25개 제품을 구매하면 신규 주문은 미납주문으로 입력됩니다. 제품의 판매 가능 수량이 5개(70개 품목이 판매됨)로 감소함에 따라 _제품_ 페이지에 메시지가 표시됨 `Only 5 left` 가게 앞에서요 판매 가능 수량이 다음과 같을 때 `0`, 제품이 로 표시됩니다. `Out of Stock` 가게 앞에서요

>[!NOTE]
>
>고객이 다음을 사용하여 주문하는 경우 _[!UICONTROL backorder qty]_, [!DNL Inventory Management] 판매 가능 수량에서 수량을 자동으로 뺍니다. 주문이 출하되지 않고 취소된 경우 수량은 집계된 가상 판매 가능 수량으로 반환됩니다. 다음&#x200B;**_취소된 주문 수량이 어떤 소스에도 지정되지 않음_**, 그러나 은 판매 가능한 총 제품 수(_[!UICONTROL Salable Quantity]_ 제품 표의 열).

<!--### Notify for Quantity Below JIRA MDVA-8099 MDVA-33783

The _Notify for Quantity Below_ configuration option is configurable at the global, source, and product levels. When it is enabled, the system sends an email notification when the product quantity reaches a level at or below the configured value. For this example, a notification is triggered when the product has a quantity of 10 or less. When backorders are enabled, _Notify for Quantity Below_ is determined by the Salable Quantity (`Salable Quantity = Quantity - (Out-of-Stock Threshold)`). -->

### 재고 상태

제품을 로 설정해야 합니다. `In Stock` 미납주문을 활성화할 때의 상태입니다. 다음에서 이 값을 설정할 수 있습니다. _제품_ 페이지를 가리키도록 업데이트하는 중입니다. 다중 소스 판매자의 경우 적어도 하나의 소스가 다음으로 표시되어야 합니다. `In Stock`. 액세스 및 다음을 통해 상태 설정 _제품_ 페이지 및 할당됨 _소스_ 그리드.

## 전체적으로 미납 주문 구성

이 단계를 통해 사이트 레벨의 모든 제품에 대해 미납주문을 사용할 수 있습니다.

1. 다음에서 _관리자_ 사이드바, 이동 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. 설정 **[!UICONTROL Store View]** 끝 `Default Config`.

1. 왼쪽 패널에서 를 확장합니다. **[!UICONTROL Catalog]** 및 선택 **[!UICONTROL Inventory]**.

1. 확장 ![확장 선택기](../assets/icon-display-expand.png) **[!UICONTROL Product Stock Options]**.

1. 대상 **[!UICONTROL Backorders]**, 선택 해제 **[!UICONTROL Use system value]** 확인란을 선택하고 다음 옵션을 선택합니다.

   | 옵션 | 설명 |
   | -- | -- |
   | `No Backorders` | 제품이 품절되었을 때 미납주문을 수락하지 않습니다. |
   | `Allow Qty Below 0` | 수량이 영(0) 아래로 떨어질 때 미납주문을 수락합니다. |
   | `Allow Qty Below 0 and Notify Customer` | 수량이 영(0) 아래로 떨어질 때 미납주문을 수락하고 고객에게 주문을 계속 진행할 수 있음을 알립니다. |

1. 대상 **[!UICONTROL Out-of-Stock Threshold]**, 선택 해제 **[!UICONTROL Use system value]** 확인란을 선택하고 다른 금액을 입력합니다.

   | 값 | 설명 |
   | -- | -- |
   | 양수 | 미납주문을 비활성화한 상태에서 양수 값을 입력합니다. |
   | 0 | 미납주문 사용가능 시 다음을 입력합니다. `0` 무한 미납주문을 허용합니다. |
   | 음수 금액 | 미납주문을 사용할 수 있는 경우 음수 값을 입력하는 것이 좋습니다. 금액은 판매 가능 수량에 추가됩니다. 예를 들어, 을 입력합니다. `-50` 최대 이 수량까지 주문을 허용합니다. |

1. 클릭 **[!UICONTROL Save Config]**.

## 제품에 대한 미납 주문 구성

제품 수준 구성은 전역 구성을 재정의합니다. 글로벌 스토어 또는 소스 레벨에서 설정을 재정의하기 위해 제품 레벨에서 미납주문을 구성할 수 있습니다. 예를 들어 스토어가 전체적으로 미납주문을 지원할 수 있습니다. 제품 설정을 사용하면 다른 제품 및 소스에 영향을 주지 않고 미납주문을 비활성화하거나 재고 부족 임계값을 변경할 수 있습니다.

1. 다음에서 _관리자_ 사이드바, 이동 **[!UICONTROL Catalog]** > **[!UICONTROL Products]**.

1. 에서 제품 열기 **[!UICONTROL Edit]** 을(를) 클릭하고 페이지를 아래로 스크롤하여 _[!UICONTROL Sources]_영역입니다.

   없이 구성된 제품의 경우 [!DNL Inventory Management], 탭이 표시되지 않습니다. 다음 `Advanced Inventory` 아래에 단추가 표시됩니다. _[!UICONTROL Quantity]_필드.

1. 클릭 **[!UICONTROL Advanced Inventory]**.

   이 작업은 제품별 구성의 페이지를 표시합니다. 나열된 모든 설정 `global` 저장소에 대한 현재 글로벌 설정을 표시합니다.

1. 대상 **[!UICONTROL Backorders]**, 선택 해제 **[!UICONTROL Use Config Setting]** 확인란을 선택하고 다음 옵션을 선택합니다.

   | 옵션 | 설명 |
   | -- | -- |
   | `No Backorders` | 제품이 품절되었을 때 미납주문을 수락하지 않습니다. |
   | `Allow Qty Below 0` | 수량이 영(0) 아래로 떨어질 때 미납주문을 수락합니다. |
   | `Allow Qty Below 0 and Notify Customer` | 수량이 영(0) 아래로 떨어질 때 미납주문을 수락하고 고객에게 주문을 계속 진행할 수 있음을 알립니다. |

1. 대상 **[!UICONTROL Out-of-Stock Threshold]**, 선택 해제 **[!UICONTROL Use Config Setting]** 확인란을 선택하고 금액을 입력합니다.

   | 값 | 설명 |
   | -- | -- |
   | 양수 | 미납주문을 비활성화한 상태에서 양수 값을 입력합니다. |
   | 0 | 미납주문 사용가능 시 다음을 입력합니다. `0` 무한 미납주문을 허용합니다. |
   | 음수 금액 | 미납주문을 사용할 수 있는 경우 음수 값을 입력하는 것이 좋습니다. 금액은 판매 가능 수량에 추가됩니다. 예를 들어, 을 입력합니다. `-50` 최대 주문 수 허용. |

   ![미납주문에 대해 구성된 고급 재고](assets/inventory-backorders-product-settings.png){width="600" zoomable="yes"}

1. 클릭 **[!UICONTROL Done]**, 및 **[!UICONTROL Save]**.
