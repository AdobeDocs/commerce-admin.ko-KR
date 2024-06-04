---
title: 가격 범위
description: 전역 또는 웹 사이트 수준에서 적용되도록 구성할 수 있는 제품 가격에 사용되는 범위에 대해 알아봅니다.
exl-id: 3726b16b-4ed5-4286-a7fd-69ed6677f87a
feature: Catalog Management, Products
source-git-commit: 61df9a4bcfaf09491ae2d353478ceb281082fa74
workflow-type: tm+mt
source-wordcount: '322'
ht-degree: 0%

---

# 가격 범위

의 범위 [기본 통화](../stores-purchase/currency-configuration.md) 제품 가격에 사용되는 값은 전역 또는 웹 사이트 수준에서 적용되도록 구성할 수 있습니다. 글로벌 수준에 적용할 경우 스토어 계층 구조 전체에서 동일한 가격이 사용됩니다. 웹 사이트 수준에 적용되는 경우 동일한 제품을 다른 웹 사이트와 연결된 스토어와 다른 가격으로 사용할 수 있습니다. 기본적으로 제품 가격 범위는 전역입니다.

서로 다른 요인이 한 장소에서 같은 제품의 가격에 영향을 줄 수 있고 다른 장소에서 영향을 줄 수 없습니다. 예를 들어 제품에 대한 추가 배포 비용과 특정 상점에서 판매되는 제품의 가격에 영향을 주는 기타 고려 사항이 있을 수 있습니다. 다음 다이어그램은 기본 통화가 웹 사이트 수준으로 설정된 다중 사이트 설치를 보여 줍니다. 각 웹 사이트와 연관된 스토어 및 스토어 보기는 웹 사이트 수준에서 설정된 제품 가격을 반영합니다.

![Adobe Commerce](../assets/b2b.svg) 공유 카탈로그를 사용하는 경우 다음을 참조하십시오. [공유 카탈로그 가격 및 구조 설정](../b2b/catalog-shared-pricing-structure.md) 다음에서 _Adobe Commerce B2B 안내서_.

![가격 범위 다이어그램](./assets/catalog-price-scope.svg){width="550"}

## 가격 범위 구성

1. 다음에서 _관리자_ 메뉴, 이동 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. 왼쪽 패널에서 를 확장합니다. **[!UICONTROL Catalog]** 및 선택 **[!UICONTROL Catalog]** 밑에.

1. 아래로 스크롤하여 **[!UICONTROL Price]** 섹션 및 세트 **[!UICONTROL Catalog Price Scope]** 다음 중 하나를 수행합니다.

   - `Global`
   - `Website`

   선택하는 범위 설정은 카탈로그의 가격 필드 아래에 표시됩니다.

   ![카탈로그 가격 범위](./assets/catalog-price.png){width="600" zoomable="yes"}

1. 완료되면 다음을 클릭하십시오. **[!UICONTROL Save Config]**.

## 범위를 사용하여 제품 가격 설정

Commerce에서는 각 스토어에 대한 제품 가격 설정을 허용하지 않습니다. 그러나 웹 사이트당 가격은 변경할 수 있습니다.

1. 다음에서 _관리자_ 메뉴, 이동 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. 왼쪽 패널에서 를 확장합니다. **[!UICONTROL Catalog]** 및 선택 **[!UICONTROL Catalog]** 밑에.

1. 다음에서 **[!UICONTROL Price]** 탭, 가격 범위를 다음으로 설정 `Website` 전역 대신

1. 제품 편집 페이지를 열고 왼쪽 상단의 범위를 선택한 다음 웹 사이트당 새 가격을 입력하여 가격을 설정합니다.
