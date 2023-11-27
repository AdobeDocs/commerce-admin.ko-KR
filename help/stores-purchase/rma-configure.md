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

활성화하면 상점에서 고객이 RMA 요청을 제출할 수 있습니다. RMA는 반품할 수 있는 품목이 주문에 있는 경우에만 생성할 수 있습니다. 개별 항목 반환에 대한 요청은 _RMA 활성화_ 각 제품 레코드의 특성. 기본적으로 구성 설정은 제품(_[!UICONTROL Use Config Settings]_이(가) 선택되어 있습니다. If_[!UICONTROL Enable RMA]_ 이(가) (으)로 설정됨 `No`, 제품이 반환할 수 있는 항목 목록에 표시되지 않습니다. 을(를) 변경하면 _RMA 활성화_ 이 설정은 새 주문과 기존 주문 모두에 적용됩니다.

## 스토어에 대한 RMA 활성화

1. 다음에서 _관리자_ 사이드바, 이동 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. 왼쪽 패널에서 를 확장합니다. **[!UICONTROL Sales]** 및 선택 **[!UICONTROL Sales]** 밑에.

1. 확장 ![확장 선택기](../assets/icon-display-expand.png) 다음 **[!UICONTROL RMA Settings]** 섹션.

   ![RMA 설정](../configuration-reference/sales/assets/sales-rma-settings.png){width="600" zoomable="yes"}

1. 설정 **[!UICONTROL Enable RMA on Storefront]** 끝 `Yes`.

   이 설정은 고객이 상점에서 RMA 요청을 만들고 볼 수 있는지 여부를 결정합니다. RMA는 신규 및 기존 주문 모두에 적용할 수 있습니다.

1. 설정 **[!UICONTROL Enable RMA on Product Level]** 끝 `Yes`.

   이 설정은 의 동작을 결정합니다. _RMA 활성화_ 상점 첫 화면의 개별 제품에 대한 특성:

   - 날짜 [!UICONTROL Enable RMA on Product Level] 이(가) (으)로 설정됨 `Yes`, 상점 내 고객은 모든 개별 제품을 반환할 수 있습니다. 여기에는 두 가지가 모두 포함됩니다 _[!UICONTROL Enable RMA]_= `Yes` 및_[!UICONTROL Enable RMA]_ = `No` 제품 속성 값.
   - 날짜 [!UICONTROL Enable RMA on Product Level] 이(가) (으)로 설정됨 `No`, 상점 첫 화면의 고객은 _[!UICONTROL Enable RMA]_= `Yes` 제품 속성 값입니다.

1. 설정 **[!UICONTROL Use Store Address]** 다음 값 중 하나로 변환:

   - `Yes` - 반품된 제품을 매장 주소로 보냅니다.
   - `No` - 제품 반품에 대한 대체 주소를 입력합니다.

   ![대체 주소가 있는 RMA 설정](../configuration-reference/sales/assets/sales-rma-settings.png){width="600" zoomable="yes"}

1. 클릭 **[!UICONTROL Save Config]**.

## 반품에 대한 배송 방법 구성

1. 다음에서 _관리자_ 사이드바, 이동 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. 왼쪽 패널에서 를 확장합니다. **[!UICONTROL Sales]** 및 선택 **[!UICONTROL Delivery Methods]**.

1. 반환 서비스에 사용할 통신사의 섹션을 확장합니다. 예: **[!UICONTROL UPS]**.

   ![통신사에 대한 RMA 서비스 활성화](./assets/rma-delivery-method.png){width="600" zoomable="yes"}

1. 설정 **[!UICONTROL Enabled for RMA]** 끝 `Yes`.

1. 클릭 **[!UICONTROL Save Config]**.

## 제품 수준에서 허용된 RMA 변경

스토어에 대해 RMA를 활성화하고 카탈로그에 반품이 허용되지 않아야 하는 제품이 포함되어 있는 경우 제품 수준에서 설정을 수정할 수 있습니다.

1. 제품을 편집 모드로 엽니다.

1. 아래로 스크롤하고 확장합니다. ![확장 선택기](../assets/icon-display-expand.png) 다음 **[!UICONTROL Autosettings]** 섹션.

1. 지우기 **[!UICONTROL Use Config Setting]** 필요한 경우 확인란

1. 전환 **[!UICONTROL Enable RMA]** 설정 `No`.

   ![제품에 대한 RMA 비활성화](./assets/product-advanced-autosettings-enable-rma.png){width="600" zoomable="yes"}

1. 클릭 **[!UICONTROL Save]**.
