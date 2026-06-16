---
title: 가격 범위
description: 전역 또는 웹 사이트 수준에서 적용되도록 구성할 수 있는 제품 가격에 사용되는 범위에 대해 알아봅니다.
exl-id: 3726b16b-4ed5-4286-a7fd-69ed6677f87a
feature: Catalog Management, Products
TQID: https://experienceleague.adobe.com/4tNRviXPzBubIpyAn9vgUs8BaILjJ6BEdV4yj5ngz6Y
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2:
  - id: c18ed297-2187-4aec-affb-9d9654eca6fc
  - id: dac87252-6066-4d6e-a9d2-f6d84c323de7
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: f8a45b24-4be7-4f1b-909b-60d06b483a20
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2:
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 376
ht-degree: 0%

---

# 가격 범위

제품 가격에 사용되는 [기본 통화](../stores-purchase/currency-configuration.md)의 범위를 전역 또는 웹 사이트 수준에서 적용하도록 구성할 수 있습니다. 글로벌 수준에 적용할 경우 스토어 계층 구조 전체에서 동일한 가격이 사용됩니다. 웹 사이트 수준에 적용되는 경우 동일한 제품을 다른 웹 사이트와 연결된 스토어와 다른 가격으로 사용할 수 있습니다. 기본적으로 제품 가격 범위는 전역입니다.

서로 다른 요인이 한 장소에서 같은 제품의 가격에 영향을 줄 수 있고 다른 장소에서 영향을 줄 수 없습니다. 예를 들어 제품에 대한 추가 배포 비용과 특정 상점에서 판매되는 제품의 가격에 영향을 주는 기타 고려 사항이 있을 수 있습니다. 다음 다이어그램은 기본 통화가 웹 사이트 수준으로 설정된 다중 사이트 설치를 보여 줍니다. 각 웹 사이트와 연관된 스토어 및 스토어 보기는 웹 사이트 수준에서 설정된 제품 가격을 반영합니다.

![Adobe Commerce B2B](../assets/b2b.svg) 공유 카탈로그를 사용하는 경우 _Adobe Commerce B2B 안내서_&#x200B;의 [공유 카탈로그 가격 및 구조 설정](../b2b/catalog-shared-pricing-structure.md)을 참조하세요.

![가격 범위 다이어그램](./assets/catalog-price-scope.svg){width="550"}

## 가격 범위 구성

1. _관리자_ 메뉴에서 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**(으)로 이동합니다.

1. 왼쪽 패널에서 **[!UICONTROL Catalog]**&#x200B;을(를) 확장하고 아래의 **[!UICONTROL Catalog]**&#x200B;을(를) 선택합니다.

1. **[!UICONTROL Price]** 섹션까지 아래로 스크롤하고 **[!UICONTROL Catalog Price Scope]**&#x200B;을(를) 다음 중 하나로 설정합니다.

   - `Global`
   - `Website`

   선택하는 범위 설정은 카탈로그의 가격 필드 아래에 표시됩니다.

   ![카탈로그 가격 범위](./assets/catalog-price.png){width="600" zoomable="yes"}

1. 완료되면 **[!UICONTROL Save Config]**&#x200B;을(를) 클릭합니다.

## 범위를 사용하여 제품 가격 설정

Commerce에서는 각 스토어에 대한 제품 가격 설정을 허용하지 않습니다. 그러나 웹 사이트당 가격은 변경할 수 있습니다.

1. _관리자_ 메뉴에서 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**(으)로 이동합니다.

1. 왼쪽 패널에서 **[!UICONTROL Catalog]**&#x200B;을(를) 확장하고 아래의 **[!UICONTROL Catalog]**&#x200B;을(를) 선택합니다.

1. **[!UICONTROL Price]** 탭에서 가격 범위를 `Global` 대신 `Website`(으)로 설정합니다.

1. 제품 편집 페이지를 열고 왼쪽 상단의 범위를 선택한 다음 웹 사이트당 새 가격을 입력하여 가격을 설정합니다.

드문 경우지만 가격 범위가 `Global`(으)로 설정된 경우 Commerce 데이터베이스의 가격이 웹 사이트 수준에서 다를 수 있습니다. 이 문제는 Commerce 외부의 동기화 문제로 인해 발생할 수 있습니다. 이러한 경우 판매자는 매장 수준에서 가격 정리를 수행하고 Commerce Services와 카탈로그 동기화를 실행해야 합니다.