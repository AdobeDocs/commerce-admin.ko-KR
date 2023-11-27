---
title: 그룹 가격 책정
description: 그룹 가격을 사용하여 스토어의 고객 그룹에 따라 할인된 항목의 가격을 설정하는 방법에 대해 알아봅니다.
exl-id: bc5be23f-64eb-47c3-beda-01168abfbf96
feature: Catalog Management, Products, Customers
source-git-commit: 01148770946a236ece2122be5a88b963a0f07d1f
workflow-type: tm+mt
source-wordcount: '333'
ht-degree: 0%

---

# 그룹 가격 책정

관리자의 제품 구성 설정을 사용하여 스토어의 고객 그룹을 기반으로 할인된 항목의 가격을 설정할 수 있습니다. 이러한 전략적 가격 책정 모델을 이라고 합니다. _그룹 가격 책정_.

특정 고객 그룹의 구성원은 쇼핑객이 계정에 로그인하면 제품의 할인된 가격을 제공 받을 수 있습니다. 고객군의 가격은 정가와 함께 상품 페이지에 표시돼 쇼핑객이 쉽게 가격을 비교하며 그에 따른 행동을 할 수 있도록 했다. 장바구니에 제품을 추가하면 정가는 해당 고객 그룹을 기반으로 한 그룹 가격으로 대체됩니다.

고객 그룹에 대한 가격은 [계층형 가격](product-price-tier.md) 와 가 유사한 방식으로 설정됩니다. 유일한 차이는 고객 그룹 가격의 수량이 1이라는 것입니다.

![고객 그룹 할인](./assets/storefront-price-group.png){width="600" zoomable="yes"}

## 그룹 가격 사용의 이점

- 도매 구매자에게 적합

- 고객이 할인 혜택을 활용하기 위해 고객 그룹을 업그레이드할 수 있는 인센티브

- 타겟팅된 마케팅 캠페인

- 단골 고객에게 보람을 주어 신뢰와 신뢰를 구축합니다.

## 그룹 가격 설정

1. 제품을 편집 모드로 엽니다.

1. 아래 _[!UICONTROL Price]_필드, 클릭&#x200B;**[!UICONTROL Advanced Pricing]**.

1. 다음에서 _[!UICONTROL Customer Group Price]_섹션, 클릭&#x200B;**[!UICONTROL Add]**.

   스토어에 다음이 포함된 경우 [Adobe Commerce용 B2B](../b2b/introduction.md) 및 이(가) [공유 카탈로그](../b2b/catalog-shared.md) 활성화됨, 이 섹션에는 레이블이 지정됩니다. _[!UICONTROL Catalog and Tier Price]_.

   ![고급 가격 책정](./assets/product-price-group.png){width="600" zoomable="yes"}

1. 그룹 가격을 구성합니다.

   - 다중 사이트 설치의 경우 **[!UICONTROL Website]** 그룹 가격이 적용되는 경우.

   - 다음을 선택합니다. **[!UICONTROL Customer Group]** 그것은 할인을 받기 위함입니다.

   - 입력 **[!UICONTROL Quantity]** / `1`.

   - 대상 **[!UICONTROL Price]**, 가격책정 유형 및 금액을 설정합니다.

      - `Fixed` - 할인된 제품 가격을 입력합니다.

      - `Discount` - 제품 가격의 할인된 가격을 백분율로 입력합니다.

     ![고객 그룹 가격 책정](./assets/product-price-group-discount.png){width="600" zoomable="yes"}

1. 다른 그룹 가격을 추가하려면 **[!UICONTROL Add]** 이전 단계를 반복합니다.

1. 완료되면 다음을 클릭하십시오. **[!UICONTROL Done]** 그런 다음 **[!UICONTROL Save]**.

>[!NOTE]
>
>다음 **_final_** 제품 가격은 다음과 같이 계산됩니다 **_최소값_** 다음 공식을 사용한 관련 가격: <br/>`Final Price=Min(Regular(Base) Price, Group(Tier) Price, Special Price, Catalog Price Rule) + Sum(Min Price per each required custom option)`

>[!NOTE]
>
>**_고정 가격_** 사용자 정의 가능한 제품 옵션 _아님_ 그룹 가격, 계층 가격, 특별 가격 또는 카탈로그 가격 규칙의 영향을 받습니다.
