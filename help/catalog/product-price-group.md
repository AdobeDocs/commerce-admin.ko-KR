---
title: 그룹 가격 책정
description: 그룹 가격을 사용하여 스토어의 고객 그룹에 따라 할인된 항목의 가격을 설정하는 방법에 대해 알아봅니다.
exl-id: bc5be23f-64eb-47c3-beda-01168abfbf96
feature: Catalog Management, Products, Customers
source-git-commit: 61df9a4bcfaf09491ae2d353478ceb281082fa74
workflow-type: tm+mt
source-wordcount: '332'
ht-degree: 0%

---

# 그룹 가격 책정

관리자의 제품 구성 설정을 사용하여 스토어의 고객 그룹을 기반으로 할인된 항목의 가격을 설정할 수 있습니다. 이 전략적 가격 책정 모델을 _그룹 가격 책정_&#x200B;이라고 합니다.

특정 고객 그룹의 구성원은 쇼핑객이 계정에 로그인하면 제품의 할인된 가격을 제공 받을 수 있습니다. 고객군의 가격은 정가와 함께 상품 페이지에 표시돼 쇼핑객이 쉽게 가격을 비교하며 그에 따른 행동을 할 수 있도록 했다. 장바구니에 제품을 추가하면 정가는 해당 고객 그룹을 기반으로 한 그룹 가격으로 대체됩니다.

고객 그룹의 가격은 [계층화된 가격](product-price-tier.md)의 구성 요소이며 유사한 방식으로 설정됩니다. 유일한 차이는 고객 그룹 가격의 수량이 1이라는 것입니다.

![고객 그룹 할인](./assets/storefront-price-group.png){width="600" zoomable="yes"}

## 그룹 가격 사용의 이점

- 도매 구매자에게 적합

- 고객이 할인 혜택을 활용하기 위해 고객 그룹을 업그레이드할 수 있는 인센티브

- 타겟팅된 마케팅 캠페인

- 단골 고객에게 보람을 주어 신뢰와 신뢰를 구축합니다.

## 그룹 가격 설정

1. 제품을 편집 모드로 엽니다.

1. _[!UICONTROL Price]_필드 아래에서&#x200B;**[!UICONTROL Advanced Pricing]**을(를) 클릭합니다.

1. _[!UICONTROL Customer Group Price]_섹션에서&#x200B;**[!UICONTROL Add]**을(를) 클릭합니다.

   스토어에 [Adobe Commerce B2B](../b2b/introduction.md)이(가) 포함되어 있고 [공유 카탈로그](../b2b/catalog-shared.md)가 활성화되어 있는 경우 이 섹션에는 _[!UICONTROL Catalog and Tier Price]_(으)로 레이블이 지정됩니다.

   ![고급 가격](./assets/product-price-group.png){width="600" zoomable="yes"}

1. 그룹 가격을 구성합니다.

   - 다중 사이트 설치의 경우 그룹 가격이 적용되는 **[!UICONTROL Website]**&#x200B;을(를) 선택하십시오.

   - 할인을 받을 **[!UICONTROL Customer Group]**&#x200B;을(를) 선택하십시오.

   - **[!UICONTROL Quantity]**/`1`을(를) 입력하십시오.

   - **[!UICONTROL Price]**&#x200B;의 경우 가격 책정 유형 및 금액을 설정하십시오.

      - `Fixed` - 할인된 제품 가격을 입력합니다.

      - `Discount` - 제품 가격의 할인된 가격을 백분율로 입력합니다.

     ![고객 그룹 가격](./assets/product-price-group-discount.png){width="600" zoomable="yes"}

1. 다른 그룹 가격을 추가하려면 **[!UICONTROL Add]**&#x200B;을(를) 클릭하고 이전 단계를 반복합니다.

1. 완료되면 **[!UICONTROL Done]**&#x200B;을(를) 클릭한 다음 **[!UICONTROL Save]**&#x200B;을(를) 클릭합니다.

>[!NOTE]
>
>**_final_** 제품 가격은 다음 공식을 사용하여 **_minimum_** 관련 가격으로 계산됩니다. <br/>`Final Price=Min(Regular(Base) Price, Group(Tier) Price, Special Price, Catalog Price Rule) + Sum(Min Price per each required custom option)`

>[!NOTE]
>
>**_고정 가격_** 제품 사용자 지정 가능 옵션은 그룹 가격, 계층 가격, 특별 가격 또는 카탈로그 가격 규칙의 영향을 받지 _않습니다_.
