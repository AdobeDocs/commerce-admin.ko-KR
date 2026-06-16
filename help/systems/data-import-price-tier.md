---
title: 계층 가격 가져오기
description: 계층 가격 책정 데이터를 내보내고 업데이트된 데이터를 가져오는 방법을 알아봅니다.
exl-id: b19d0208-68b3-45ba-9896-318e12ff4131
feature: Products, Data Import/Export
TQID: https://experienceleague.adobe.com/8eyWhVu-RtuzEYG81xOyqsEFdbz0s7evB-UGepUGCNw
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2:
  - id: ba9e5be9-7de1-4f71-a5d2-baead0e425ee
  - id: d1e21356-0064-4f48-9089-16e3f0dbd2a6
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: f8a45b24-4be7-4f1b-909b-60d06b483a20
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2:
  - id: d095671a-1355-40aa-8b5f-06c33c68080b
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 346
ht-degree: 0%

---

# 계층 가격 가져오기

각 제품에 대해 [계층 가격](../catalog/product-price-tier.md)을 수동으로 입력하는 대신 가격 데이터를 [가져오기](data-import.md)하는 것이 더 효율적일 수 있습니다. 시작하기 전에 템플릿으로 사용할 수 있는 내보낸 계층 가격 데이터의 샘플 파일을 만듭니다.

![Example storefront - 계층화된 가격 책정](./assets/storefront-tier-pricing-water-bottle.png){width="700" zoomable="yes"}

## 1단계: 계층 가격 데이터 내보내기

다음 예제에서는 단일 제품에 대한 계층 가격 데이터를 내보냅니다. 그런 다음 내보낸 데이터를 계층 가격 데이터의 대량 가져오기에 대한 템플릿으로 사용할 수 있습니다. 고급 가격 데이터를 내보내는 방법에 대한 자세한 내용은 [고급 가격 데이터](data-attributes-product.md#advanced-pricing-attributes)를 참조하십시오.

![제품 계층 가격 책정](./assets/price-tier-customer-group-discount.png){width="600" zoomable="yes"}

1. _관리자_ 사이드바에서 **[!UICONTROL System]** > _[!UICONTROL Data Transfer]_>**[!UICONTROL Export]**(으)로 이동합니다.

1. _[!UICONTROL Export Settings]_&#x200B;에서&#x200B;**[!UICONTROL Entity Type]**&#x200B;을(를) `Advanced Pricing`(으)로 설정합니다.

1. **[!UICONTROL Entity Attributes]** 그리드에서 SKU 특성으로 아래로 스크롤하여 다음을 수행합니다.

   - 할인율을 기반으로 하는 계층 가격의 경우, 내보낼 각 제품의 SKU를 쉼표로 구분하여 입력합니다.

     ![데이터 내보내기 - 제품 SKU](./assets/price-tier-export-sku.png){width="600" zoomable="yes"}

   - 고정 금액을 기준으로 하는 계층 가격의 경우 각 제품의 SKU를 입력합니다.

   - 아래로 스크롤하여 **[!UICONTROL Continue]**&#x200B;을(를) 클릭합니다.

1. 웹 브라우저의 다운로드 위치에서 내보내기 파일을 찾아 파일을 엽니다.

   ![예 - 내보낸 고객 그룹 할인 계층 가격 데이터](./assets/price-tier-customer-group-discount-export.png){width="600" zoomable="yes"}

**_내보낸 계층 가격 데이터_**

내보낸 데이터에는 다음 열이 포함됩니다.

- `sku`
- `tier_price_website`
- `tier_price_customer_group`
- `tier_price_qty`
- `tier_price`
- `tier_price_value_type`

내보낸 데이터를 계층 가격 데이터를 가져오기 위한 템플릿으로 사용합니다.

## 2단계: 데이터 업데이트

1. 필요에 따라 각 제품에 대한 계층 가격 데이터를 업데이트합니다.

   계층 가격 업데이트가 없는 모든 제품은 CSV 파일에서 삭제할 수 있습니다. 변경되지 않은 제품을 다시 가져올 필요가 없습니다.

1. 업데이트된 CSV 파일을 **[!UICONTROL Save]**&#x200B;합니다.

>[!NOTE]
>
>가져오기 파일의 크기는 2MB보다 클 수 없습니다.

## 3단계: 업데이트된 데이터 가져오기

1. _관리자_ 사이드바에서 **[!UICONTROL System]** > _[!UICONTROL Data Transfer]_>**[!UICONTROL Import]**(으)로 이동합니다.

1. _설정 가져오기_&#x200B;에서 **[!UICONTROL Entity Type]**&#x200B;을(를) `Advanced Pricing`(으)로 설정합니다.

1. **[!UICONTROL Import Behavior]**&#x200B;을(를) `Add/Update`(으)로 설정합니다.

1. **[!UICONTROL File to Import]**&#x200B;에서 **[!UICONTROL Choose File]**&#x200B;을(를) 클릭하고 디렉터리에서 가져오려고 준비한 파일을 선택합니다.

1. 오른쪽 상단에서 **[!UICONTROL Check Data]**&#x200B;을(를) 클릭합니다.

1. 파일이 올바른 경우 **[!UICONTROL Import]**&#x200B;을(를) 클릭합니다.

   그렇지 않으면 메시지에 나열된 데이터의 각 문제를 수정한 다음 파일을 다시 가져오십시오.
