---
title: 빠른 주문
description: 빠른 주문 기능과 고객을 위한 활성화에 대해 알아봅니다.
exl-id: 7007e1b4-a64f-46fe-a235-3ca9f64e77e4
feature: B2B, Orders
source-git-commit: c94d4e8d13c32c1c1b1d37440fdb953c8527b76c
workflow-type: tm+mt
source-wordcount: '435'
ht-degree: 0%

---

# 빠른 주문

다음 _빠른 주문_ 이 기능은 주문하려는 제품의 제품 이름 또는 SKU를 알고 있는 고객의 주문 프로세스를 몇 번의 클릭으로 줄입니다. 여러 SKU가 있는 주문은 수동으로 입력하거나 빠른 주문 양식으로 가져올 수 있습니다. 빠른 주문은 계정에 로그인한 고객 및 게스트가 사용할 수 있습니다. 활성화하면 _빠른 주문_ 페이지 상단의 고객 이름 옆에 링크가 나타납니다.

![빠른 주문 링크](./assets/quick-order-link.png){width="700" zoomable="yes"}

## 스토어에 대한 빠른 주문 활성화

1. 다음에서 _관리자_ 사이드바, 이동 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. 다음에서 _[!UICONTROL General]_왼쪽 패널의 섹션에서&#x200B;**[!UICONTROL B2B Features]**.

1. 설정 **[!UICONTROL Enable Quick Order]** 끝 `Yes`.

   ![빠른 주문 활성화](./assets/quick-orders-config.png){width="600" zoomable="yes"}

1. 클릭 **[!UICONTROL Save Config]**.

1. 메시지가 표시되면 [캐시 관리](../systems/cache-management.md) 잘못된 캐시를 새로 고칩니다.

## 빠른 주문 워크플로우

고객은 다음 방법 중 하나를 사용하여 빠른 주문에 대한 제품을 지정할 수 있습니다.

### 방법 1: 개별 제품 입력

1. 고객이 클릭 **[!UICONTROL Quick Order]** 링크를 클릭합니다.

1. SKU 또는 제품 이름으로 제품을 선택합니다.

   을(를) 배치하려면 **sku별 빠른 주문**, 고객은 다음을 수행합니다.

   - 다음을 입력합니다. **[!UICONTROL SKU]**.

   - 클릭수 **[!UICONTROL Add to List]**.

     입력 줄에 SKU가 표시되며, 아래에 제품 세부 정보가 표시됩니다.

     ![빠른 주문 세부 사항](./assets/quick-order-product-detail.png){width="600" zoomable="yes"}

   을(를) 배치하려면 **제품 이름별 빠른 주문**, 고객은 다음을 수행합니다.

   - 의 처음 몇 문자를 입력합니다. **[!UICONTROL Product Name]**.

     >[!NOTE]
     >
     >를 사용하지 마십시오. _입력_ 제품 이름을 선택하는 키입니다.

   - 가능한 일치 목록이 나타나면 고객이 주문할 제품을 클릭합니다.

     ![제품 이름을 선택하려면 클릭하십시오.](./assets/quick-order-product-name.png){width="700" zoomable="yes"}

1. 다음을 입력합니다. **[!UICONTROL Qty]**.

1. 다음 입력 라인을 사용하여 필요한 횟수만큼 이 프로세스를 반복합니다.

1. 클릭수 **[!UICONTROL Add to Cart]**.

### 방법 2: 여러 제품 입력

1. 다음에서 **[!UICONTROL Enter Multiple SKUs]** box에서 고객은 다음 중 하나를 수행합니다.

   - 라인당 하나의 SKU를 입력합니다.

   - 쉼표로 구분하고 공백 없이 같은 줄에 모든 SKU를 입력합니다.

     ![여러 SKU 입력](./assets/quick-order-skus.png){width="600" zoomable="yes"}

1. 목록에 제품을 추가하려면 **[!UICONTROL Add to List]**.

1. 다음을 입력합니다. **[!UICONTROL Qty]** 목록에 있는 각 항목에 대해 주문해야 합니다.

   ![빠른 주문 목록](./assets/quick-order-skus-detail.png){width="600" zoomable="yes"}

   >[!NOTE]
   >
   >제품에 필요한 옵션이 있으면 옵션을 선택하라는 메시지가 표시됩니다. 장바구니에 도달하여 제품 옵션을 추가할 때까지 기다릴 수 있습니다.

   ![옵션 선택](./assets/quick-order-skus-product-options.png){width="600" zoomable="yes"}

### 방법 3: 제품 목록 업로드

1. 다음에서 _[!UICONTROL Add from File]_섹션, 클릭&#x200B;**[!UICONTROL Download Sample]**주문 템플릿을 다운로드하려면 다음을 수행하십시오.

   ![파일에서 추가](./assets/quick-order-skus-add-from-file.png){width="600" zoomable="yes"}

1. 다운로드한 파일을 엽니다.

1. 템플릿을 사용하여 빠른 주문 목록에 업로드할 제품 SKU를 추가합니다.

1. 완료되면 클릭 수 **[!UICONTROL Save]**.

   ![업로드할 SKU](./assets/quick-order-skus-add-from-file-sample.png){width="400" zoomable="yes"}

1. 파일을 업로드하려면 **[!UICONTROL Choose]** 시스템에서 파일을 선택합니다.

   항목이 빠른 주문 목록에 추가됩니다.

1. 준비가 되면 클릭 수 **[!UICONTROL Add to Cart]**.

고객이 빠른 주문을 만든 후 평소대로 체크아웃을 진행할 수 있습니다.

![빠른 주문](./assets/quick-order-add-to-cart.png){width="700" zoomable="yes"}
