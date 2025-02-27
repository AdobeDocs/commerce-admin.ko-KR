---
title: 카탈로그 가격 규칙
description: 정의된 조건 집합을 기준으로 할인된 가격으로 구매자에게 제품을 제공하는 데 사용할 수 있는 카탈로그 가격 규칙에 대해 알아봅니다.
exl-id: 8da95076-d724-41f6-b3ca-e61ff1906b72
feature: Merchandising, Price Rules, Catalog Management
source-git-commit: f8254db7d69e58c8e9a78948ee6e40f5ea88cea0
workflow-type: tm+mt
source-wordcount: '468'
ht-degree: 0%

---

# 카탈로그 가격 규칙

카탈로그 가격 규칙은 정의된 조건 세트에 따라 할인된 가격으로 구매자에게 제품을 제공하는 데 사용할 수 있습니다. 카탈로그 가격 규칙은 제품을 장바구니에 담기 전에 트리거되므로 [쿠폰 코드](price-rules-cart-coupon.md)를 사용하지 않습니다.

예를 들어 충족될 때 특별 또는 판촉 가격이 있는 제품을 자동으로 표시하는 가격 규칙에 대한 조건을 정의하고 설정할 수 있습니다. 정의된 규칙 속성에는 고객 그룹, 제품 카테고리, 할인 금액 또는 백분율, 제품 색상, 제품 크기 또는 스토어에 설정된 제품 속성 정보가 포함될 수 있습니다. 규칙에 정의한 일자에 판촉을 자동으로 시작 및 정지하는 가격 규칙의 시작 및 종료 일자를 설정할 수 있습니다. 저장된 규칙의 속성은 필요에 따라 업데이트하거나 수정할 수 있습니다.

- ![Adobe Commerce](../assets/adobe-logo.svg)(Adobe Commerce만 해당) 정의된 규칙을 [동적 블록](../content-design/dynamic-blocks.md)에 연결하여 스토어에서 이벤트 또는 제품을 홍보할 수도 있습니다.

- ![Magento Open Source](../assets/open-source.svg)(Magento Open Source 전용) 되풀이하는 프로모션의 경우 프로모션을 실행할 때마다 저장된 규칙을 _활성_ 또는 _비활성_ 상태로 수동으로 설정할 수 있습니다.

## 카탈로그 가격 규칙 액세스

1. _관리자_ 사이드바에서 **[!UICONTROL Marketing]** > _[!UICONTROL Promotions]_>**[!UICONTROL Catalog Price Rules]**(으)로 이동합니다.

   ![카탈로그 가격 규칙](./assets/price-rule-catalog.png){width="700" zoomable="yes"}

1. 규칙 속성 업데이트:

   - ![Adobe Commerce](../assets/adobe-logo.svg)(Adobe Commerce만 해당) _규칙 정보_ 페이지를 표시하려면 **[!UICONTROL Edit]**&#x200B;을(를) 클릭합니다.

   - ![Magento Open Source](../assets/open-source.svg)(Magento Open Source 전용) 목록에서 규칙을 클릭하여 규칙 정보 페이지를 표시합니다.

   여기에서 규칙에 대한 설정을 변경할 수 있습니다([규칙 만들기](price-rules-catalog-create.md)와 유사).

## 필터 옵션

| 필드 | 설명 |
|--- |--- |
| [!UICONTROL ID] | 특정 규칙 ID 번호에 대한 목록을 필터링하려면 텍스트를 입력하십시오. |
| [!UICONTROL Rule] | 규칙을 만들 때 정의된 규칙 이름을 기준으로 목록을 필터링할 텍스트를 입력합니다. |
| [!UICONTROL Priority] | ![Adobe Commerce](../assets/adobe-logo.svg)(Adobe Commerce만 해당) 규칙에 대해 정의된 우선 순위를 기준으로 목록을 필터링하려면 이 필드에 텍스트를 입력하십시오. |
| [!UICONTROL Web Site] | ![Adobe Commerce](../assets/adobe-logo.svg)(Adobe Commerce만 해당) 이 옵션을 사용하여 규칙에 정의된 웹 사이트를 기준으로 목록을 필터링합니다. |
| [!UICONTROL Action] | ![Adobe Commerce](../assets/adobe-logo.svg)(Adobe Commerce만 해당) **[!UICONTROL Edit]**&#x200B;을(를) 클릭하여 규칙 정보를 표시하고 규칙 설정을 업데이트합니다(규칙 만들기와 유사). |
| [!UICONTROL Start] | ![Magento Open Source](../assets/open-source.svg)(Magento Open Source 전용) 규칙을 만들 때 정의된 규칙의 시작 날짜를 기준으로 목록을 필터링하려면 동적 일정 필드(받는 사람: 및 보낸 사람:)를 사용합니다. |
| [!UICONTROL End] | ![Magento Open Source](../assets/open-source.svg)(Magento Open Source 전용) 규칙을 만들 때 정의된 규칙의 종료 날짜를 기준으로 목록을 필터링하려면 동적 일정 필드(받는 사람: 및 보낸 사람:)를 사용합니다. |
| [!UICONTROL Status] | ![Magento Open Source](../assets/open-source.svg)(Magento Open Source 전용) 규칙 상태(`Active` 또는 `Inactive`)를 기준으로 목록을 필터링하려면 이 옵션을 사용합니다. |

{style="table-layout:auto"}
