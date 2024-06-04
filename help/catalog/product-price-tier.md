---
title: 계층 가격
description: 제품 목록 또는 제품 페이지에서 계층 가격을 사용하여 수량 할인을 제공하는 방법에 대해 알아봅니다.
exl-id: b5810899-31a6-4288-9acc-09f7f4dfbd43
feature: Catalog Management, Products
source-git-commit: 61df9a4bcfaf09491ae2d353478ceb281082fa74
workflow-type: tm+mt
source-wordcount: '458'
ht-degree: 0%

---

# 계층 가격

계층 가격을 사용하면 상점 첫 화면의 제품 목록 또는 제품 페이지에서 수량 할인을 제공할 수 있습니다. 특정 매장 보기, 고객 그룹 또는 공유 카탈로그에 할인을 적용할 수 있습니다.

업데이트할 제품이 많다면 개별적으로 입력하는 것보다 계층 가격 변경 사항을 가져오는 것이 가장 효율적입니다. 자세한 내용은 [계층 가격 가져오기](../systems/data-import-price-tier.md).

![상점 첫 번째 제품 페이지의 가격](./assets/product-price-tier-storefront.png){width="700" zoomable="yes"}

제품 페이지는 수량 할인을 계산하고 다음과 같은 메시지를 표시합니다.

`Buy 6 for $5.95 each and save 15%`

상점가의 가격은 최고 수량에서 최저 수량까지 우선한다. 그 수량에 대한 계층 가격이 있다면 `5` 다음에 대한 1개 `10`그리고 고객이 장바구니에 5개, 6개, 7개, 8개 또는 9개의 품목을 추가하면 해당 수량에 대해 할인된 가격을 받습니다 `5` 계층. 고객이 열 번째 품목을 추가할 때 수량에 대해 지정된 할인된 가격 `10` 계층은 수량 만큼 계층을 대체합니다. `5`, 및 할인된 가격 `10` 적용됩니다.

## 제품에 대한 가격 계층 추가

1. 제품을 편집 모드로 엽니다.

1. 아래 _[!UICONTROL Price]_필드, 클릭&#x200B;**[!UICONTROL Advanced Pricing]**.

1. 다음에서 _[!UICONTROL Tier Price]_섹션, 클릭&#x200B;**[!UICONTROL Add]**.

   여러 가격의 계층을 만드는 경우 **[!UICONTROL Add]** 각 추가 레벨에 대해 모든 계층을 동시에 작업할 수 있습니다. 그룹의 각 계층에는 동일한 웹 사이트 및 고객 그룹 또는 공유 카탈로그 할당이 있지만 수량 및 가격은 다릅니다.

## 가격 계층 구성

1. 스토어에 여러 웹 사이트가 있는 경우 **[!UICONTROL Website]** 계층 가격이 적용되는 대상.

1. 필요한 경우 다음을 선택하여 가격 책정 계층의 가용성을 제한합니다. **[!UICONTROL Customer Group]** 또는 **[!UICONTROL Shared Catalog]** (![Adobe Commerce](../assets/b2b.svg) 사용 가능 대상 [Adobe Commerce](./b2b/../introduction.md) 만 해당).

1. 대상 **[!UICONTROL Qty]**&#x200B;할인을 받기 위해 주문해야 하는 수량을 입력합니다.

   - **방법 1:** 고정 금액으로 가격 입력

     설정 **[!UICONTROL Price]** 끝 `Fixed` 그리고 해당 계층에서 한 단위에 대해 조정된 가격을 입력합니다.

     ![고정 금액으로 책정된 가격](./assets/product-price-tier-fixed.png){width="600" zoomable="yes"}

   - **방법 2:** 백분율로 가격 입력

     설정 **[!UICONTROL Price]** 끝 `Discount` 제품의 기본 가격에서 할인된 가격의 백분율을 입력합니다.

     예를 들어 15% 할인의 경우 숫자를 입력합니다 `15`. (가격은 다음과 같이 소수점 두 자리로 저장됩니다. `15.00`.)

     >[!NOTE]
     >
     >할인된 가격을 얻으려면 정의된 백분율이 _[!UICONTROL Price]_ 필드가 아니라 _[!UICONTROL Special Price]_ 필드.

     ![백분율로 표시된 가격](./assets/product-price-tier-discount.png){width="600" zoomable="yes"}

## 가격 구성 완료

1. 다른 웹 사이트 또는 고객 그룹에 대해 다른 계층 가격 집합을 추가하려면 이전 단계를 반복합니다.

1. 완료되면 다음을 클릭하십시오. **[!UICONTROL Done]** 그런 다음 **[!UICONTROL Save]**.

>[!NOTE]
>
>다음 **_final_** 제품 가격은 다음과 같이 계산됩니다 **_최소값_** 다음 공식을 사용한 관련 가격: <br/>`Final Price=Min(Regular(Base) Price, Group(Tier) Price, Special Price, Catalog Price Rule) + Sum(Min Price per each required custom option)`

>[!NOTE]
>
>**_고정 가격_** 사용자 정의 가능한 제품 옵션 _아님_ 그룹 가격, 계층 가격, 특별 가격 또는 카탈로그 가격 규칙의 영향을 받습니다.
