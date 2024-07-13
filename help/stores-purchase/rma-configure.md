---
title: 반환 구성
description: 스토어에 대한 반품을 활성화하고 지원되는 배송 방법을 구성하는 방법에 대해 알아봅니다.
exl-id: a1b508fc-7e42-4d37-bf7e-dea17a40d39b
feature: Returns, Configuration
source-git-commit: 8b5af316ab1d2e632ed5fc2066974326830ab3f7
workflow-type: tm+mt
source-wordcount: '353'
ht-degree: 0%

---

# 반환 구성

{{ee-feature}}

활성화하면 상점에서 고객이 RMA 요청을 제출할 수 있습니다. RMA는 반품할 수 있는 품목이 주문에 있는 경우에만 생성할 수 있습니다. 개별 항목에 대한 반환 요청은 각 제품 레코드의 _RMA 사용_ 특성에 의해 관리됩니다. 기본적으로 구성 설정이 제품에 적용됩니다(_[!UICONTROL Use Config Settings]_이(가) 선택됨)._[!UICONTROL Enable RMA]_&#x200B;이(가) `No`(으)로 설정된 경우 반품할 수 있는 항목 목록에 제품이 표시되지 않습니다. _RMA 사용_ 설정을 변경하면 새 주문과 기존 주문 모두에 적용됩니다.

## 스토어에 대한 RMA 활성화

1. _관리자_ 사이드바에서 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**(으)로 이동합니다.

1. 왼쪽 패널에서 **[!UICONTROL Sales]**&#x200B;을(를) 확장하고 아래의 **[!UICONTROL Sales]**&#x200B;을(를) 선택합니다.

1. **[!UICONTROL RMA Settings]** 섹션에서 ![확장 선택기](../assets/icon-display-expand.png)를 확장합니다.

   ![RMA 설정](../configuration-reference/sales/assets/sales-rma-settings.png){width="600" zoomable="yes"}

1. **[!UICONTROL Enable RMA on Storefront]**&#x200B;을(를) `Yes`(으)로 설정합니다.

   이 설정은 고객이 상점에서 RMA 요청을 만들고 볼 수 있는지 여부를 결정합니다. RMA는 신규 및 기존 주문 모두에 적용할 수 있습니다.

1. **[!UICONTROL Enable RMA on Product Level]**&#x200B;을(를) `Yes`(으)로 설정합니다.

   이 설정은 상점 앞의 개별 제품에 대한 _RMA 사용_ 특성의 동작을 결정합니다.

   - [!UICONTROL Enable RMA on Product Level]이(가) `Yes`(으)로 설정되면 상점 첫 화면의 고객은 모든 개별 제품을 반환할 수 있습니다. 여기에는 _[!UICONTROL Enable RMA]_= `Yes` 및_[!UICONTROL Enable RMA]_ = `No` 제품 특성 값이 모두 포함됩니다.
   - [!UICONTROL Enable RMA on Product Level]이(가) `No`(으)로 설정된 경우 상점 첫 화면의 고객은 _[!UICONTROL Enable RMA]_= `Yes` 제품 특성 값이 있는 제품만 반환할 수 있습니다.

1. **[!UICONTROL Use Store Address]**&#x200B;을(를) 다음 값 중 하나로 설정합니다.

   - `Yes` - 반환된 제품을 스토어 주소로 보냅니다.
   - `No` - 제품 반품에 대한 대체 주소를 입력하십시오.

   ![대체 주소가 있는 RMA 설정](../configuration-reference/sales/assets/sales-rma-settings.png){width="600" zoomable="yes"}

1. **[!UICONTROL Save Config]**&#x200B;을(를) 클릭합니다.

## 반품에 대한 배송 방법 구성

1. _관리자_ 사이드바에서 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**(으)로 이동합니다.

1. 왼쪽 패널에서 **[!UICONTROL Sales]**&#x200B;을(를) 확장하고 **[!UICONTROL Delivery Methods]**&#x200B;을(를) 선택합니다.

1. 반환 서비스에 사용할 통신사의 섹션을 확장합니다(예: **[!UICONTROL UPS]**).

   ![통신사에 대해 RMA 서비스 사용](./assets/rma-delivery-method.png){width="600" zoomable="yes"}

1. **[!UICONTROL Enabled for RMA]**&#x200B;을(를) `Yes`(으)로 설정합니다.

1. **[!UICONTROL Save Config]**&#x200B;을(를) 클릭합니다.

## 제품 수준에서 허용된 RMA 변경

스토어에 대해 RMA를 활성화하고 카탈로그에 반품이 허용되지 않아야 하는 제품이 포함되어 있는 경우 제품 수준에서 설정을 수정할 수 있습니다.

1. 제품을 편집 모드로 엽니다.

1. 아래로 스크롤하여 **[!UICONTROL Autosettings]** 섹션에서 ![확장 선택기](../assets/icon-display-expand.png)를 확장합니다.

1. 필요한 경우 **[!UICONTROL Use Config Setting]** 확인란의 선택을 취소합니다.

1. **[!UICONTROL Enable RMA]** 설정을 `No`(으)로 전환합니다.

   ![제품에 대한 RMA 사용 안 함](./assets/product-advanced-autosettings-enable-rma.png){width="600" zoomable="yes"}

1. **[!UICONTROL Save]**&#x200B;을(를) 클릭합니다.
