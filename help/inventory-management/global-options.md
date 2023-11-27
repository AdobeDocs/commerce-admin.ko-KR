---
title: "구성 [!DNL Inventory Management] 글로벌 옵션"
description: 기본 구성 방법 알아보기 [!DNL Inventory Management] 웹 사이트의 제품 및 재고에 대한 구성 옵션.
exl-id: 1a8c9605-ae61-4d45-b549-64911b329203
feature: Inventory, Configuration
source-git-commit: 7384481d1a4a2a04882d4c99448cca75abc9be31
workflow-type: tm+mt
source-wordcount: '644'
ht-degree: 1%

---

# 구성 [!DNL Inventory Management] 글로벌 옵션

웹 사이트의 제품 및 재고에 대한 기본 구성 옵션을 구성합니다. 이러한 설정 중 일부는 다음을 통해 제품당 재정의할 수 있습니다. [제품 옵션 구성](product-options.md). 거리 우선순위 설정을 구성하려면 다음을 참조하십시오. [거리 우선순위 알고리즘 구성](distance-priority-algorithm.md).

## 전 세계적으로 제품 및 스톡 옵션 구성

1. 다음에서 _관리자_ 사이드바, 이동 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. 왼쪽 패널에서 를 확장합니다. **[!UICONTROL Catalog]** 및 선택 **[!UICONTROL Inventory]**.

1. 확장 ![확장 선택기](../assets/icon-display-expand.png) 다음 **[!UICONTROL Stock Options]** 섹션을 만들고 옵션을 설정합니다.

   ![스톡 옵션](assets/config-catalog-inventory-stock-options.png){width="600" zoomable="yes"}

   - 주문 시 현재고 수량을 조정하려면 다음을 설정합니다. **[!UICONTROL Decrease Stock When Order is Placed]** 끝 `Yes`.

   - 주문이 취소된 경우 재고로 품목을 반품하려면 **[!UICONTROL Set Items' Status to be in Stock When Order in Cancelled]** 끝 `Yes`.

   - 더 이상 재고가 없는 제품을 카탈로그에 계속 표시하려면 을 설정합니다. **[!UICONTROL Display Out of Stock Products]** 끝 `Yes`.

   - If [가격 경고](alert-setup.md) 이 기능이 활성화되면 고객은 제품이 재입고될 때 알림을 받기 위해 등록할 수 있습니다.

   - 제품 페이지에 마지막 남은 재고 금액을 표시하는 시작을 설정하려면 다음에 대한 금액을 입력합니다. **[!UICONTROL Only X left Threshold]**.

     재고 수량이 임계값에 도달하면 메시지가 나타나기 시작합니다. 예를 들어 를 로 설정하면 `3`, 메시지 `Only 3 left` 재고 수량이 3에 도달하면 나타납니다. 메시지가 수량이 0이 될 때까지 재고 수량을 반영하도록 조정됩니다.

   - 제품 페이지에 &quot;재고 있음&quot; 또는 &quot;재고 없음&quot; 메시지를 표시하려면 을 설정합니다. **[!UICONTROL Display Products Availability In Stock on Storefront]** 끝 `Yes`.

   - 장바구니에서 제품을 로드할 때 인벤토리를 확인하려면 다음을 설정하십시오. **[!UICONTROL Enable Inventory Check On Cart Load]** 끝 `Yes`. 이 옵션이 비활성화되면 인벤토리 검사를 건너뜁니다. 이 옵션을 비활성화하면 특히 장바구니에 많은 항목이 있는 경우 체크아웃 속도가 빨라집니다. 그러나 사전 유효성 검사를 건너뛸 경우 나중에 체크아웃 프로세스에서 &quot;재고 부족&quot; 오류가 표시될 수 있습니다.

   - 인벤토리와 카탈로그 간의 일관성을 유지하려면 다음을 설정하십시오. **[!UICONTROL Synchronize with Catalog]** 끝 `Yes`. 이 옵션이 활성화되면 카탈로그 변경 사항(예: 제품 제거, 제품 SKU 변경 및 제품 유형 변경)에 따라 인벤토리 데이터가 조정됩니다.

1. 확장 ![확장 선택기](../assets/icon-display-expand.png) 다음 **[!UICONTROL Product Stock Options]** 섹션을 만들고 옵션을 설정합니다.

   - 활성화하려면 [재고 관리](enable.md) 카탈로그에 대해 을 설정합니다. **[!UICONTROL Manage Stock]** 끝 `Yes`.

     ![제품 스톡 옵션](assets/config-catalog-inventory-product-stock-options.png){width="600" zoomable="yes"}

   - 설정 **[!UICONTROL Backorders]** 다음 중 하나를 수행합니다.

     | 옵션 | 설명 |
     | ----- | ----- |
     | `No Backorders` | [미납 주문](backorders.md) 제품이 품절된 경우 허용되지 않습니다. |
     | `Allow Qty Below 0` | 수량이 영(0) 아래로 떨어질 때 미납주문을 받습니다. |
     | `Allow Qty Below 0 and Notify Customer` | 수량이 영(0) 아래로 떨어질 때 미납주문이 수락되며 시스템은 여전히 주문을 할 수 있음을 고객에게 알립니다. |

   - 다음을 입력합니다. **[!UICONTROL Maximum Qty Allowed in Shopping Cart]**.

   - 다음에 대한 금액 입력 **[!UICONTROL Out-of-Stock Threshold]**:

     | 값 | 설명 |
     | ----- |-----|
     | 양수 | 미납주문을 사용불능으로 설정한 상태에서 양수 금액을 입력합니다. |
     | 0 | 미납주문 사용가능 시 다음을 입력합니다. `0` 무한 미납주문을 허용합니다. |
     | 음수 금액 | 미납주문을 사용할 수 있는 경우 음수 금액을 입력하는 것이 좋습니다. 금액은 판매 가능 수량에 추가됩니다. 예를 들어, 을 입력합니다. `-50` 최대 이 수량까지 주문을 허용합니다. |

   - 다음을 입력합니다. **[!UICONTROL Minimum Qty Allowed in Shopping Cart]** 선택한 그룹 및 금액에 대해.

   - 대상 **[!UICONTROL Notify for Quantity Below]**&#x200B;품목의 재고 부족 알림을 트리거하는 재고 레벨을 입력합니다.

   - 제품에 대한 수량 증분을 활성화하려면 다음을 설정하십시오. **[!UICONTROL Enable Qty Increments]** 끝 `Yes`. 그런 다음, **[!UICONTROL Qty Increments]**&#x200B;요구 사항을 충족하기 위해 구매해야 하는 항목의 수를 입력합니다.

     예를 들어 6씩 증분하여 판매되는 품목의 수량은 다음과 같습니다 `6`, `12`, `18`등.

   - 대상 [!DNL Inventory Management], **[!UICONTROL Automatically Return Credit Memo Item to Stock]** 이(가) (으)로 설정됨 `No`. 대변 메모를 실행할 때 주식을 출처로 반품하려면 을 입력하고 선택합니다.

1. 확장 ![확장 선택기](../assets/icon-display-expand.png) 다음 **[!UICONTROL Admin bulk operations]** 섹션을 만들고 옵션을 설정합니다.

   ![관리 일괄 작업](assets/config-catalog-inventory-admin-bulk-operations.png){width="600" zoomable="yes"}

   - 설정 **[!UICONTROL Run asynchronously]** 대량 제품 조치에 대해 일괄 작업을 비동기적으로 실행하려면

     이러한 작업에는 대량 작업이 포함됩니다. [소스 할당 및 할당 해제](bulk-assignment.md), 및 [재고를 소스로 이전](inventory-transfer.md). 비동기 배치 크기까지의 벌크 작업을 수집한 다음, 해당 작업을 실행합니다. 이 옵션은 기본적으로 비활성화되어 있습니다. 활성화하기 전에 일괄 작업으로 성능을 검토하는 것이 좋습니다.

     >[!NOTE]
     >
     >구성 및 지원 _비동기 큐 관리자_, 명령줄을 사용하여 명령을 실행해야 합니다. 이 단계에는 개발자 지원이 필요할 수 있습니다. 다음을 참조하십시오 [메시지 큐 소비자 시작](https://experienceleague.adobe.com/docs/commerce-operations/configuration-guide/cli/start-message-queues.html) 다음에서 _구성 안내서_.

   - 활성화된 경우 **[!UICONTROL Asynchronous batch size]**. 기본 배치 크기는 100입니다. 벌크 프로세스가 이 양에 도달하면 시스템이 이를 트리거합니다.

1. 완료되면 다음을 클릭하십시오. **[!UICONTROL Save Config]**.
