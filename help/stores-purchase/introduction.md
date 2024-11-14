---
title: 스토어 및 구매 경험 소개
description: 온라인 스토어를 구성하고 관리하는 데 사용되는 기능과 고객을 위한 구매 환경에 대해 알아봅니다.
exl-id: 7ced9cbc-49b4-48f7-aae2-fcb48fdb888f
source-git-commit: 7288a4f47940e07c4d083826532308228d271c5e
workflow-type: tm+mt
source-wordcount: '671'
ht-degree: 0%

---

# 스토어 및 구매 경험 소개

Adobe Commerce 및 Magento Open Source은 온라인 스토어와 구매 경험을 구축하고 관리할 수 있는 포괄적인 기능 세트를 제공합니다. Commerce 인스턴스 내에서 웹 사이트, 스토어 및 보기의 스토어 계층을 관리할 수 있습니다. 제품 및 고객 그룹에 대한 세금 분류를 포함하여 여러 로케일에 대한 저장소를 실행하는 데 필요한 세금 및 통화 요금을 구성할 수도 있습니다.

## 구조 저장

Adobe Commerce 또는 Magento Open Source의 단일 인스턴스는 다양한 속성 및 콘텐츠를 사용하는 여러 사이트, 스토어 또는 스토어 보기를 지원할 수 있습니다. 일반적인 시나리오는 도메인마다 옵션이 다른 저장소를 설정하는 것입니다. 예를 들어, 한 도메인에 하나의 범주 및 제품 세트를 두고 다른 도메인에 다른 언어로 다른 범주 및 제품 세트를 원할 수 있습니다. 상인은 관리자에서 웹 사이트, 스토어 및 스토어 보기를 구성할 수 있습니다.

[계층](stores.md)이(가) 정의된 경우 각 사이트, 스토어 및 스토어 보기에서 원하는 제품 카탈로그 및 상점 경험을 제공하도록 [범위](../getting-started/websites-stores-views.md#scope-settings)에 따라 구성 설정을 적용할 수 있습니다.

## 구매 지점

Adobe Commerce 및 Magento Open Source은 주문이 제출되기 전에 모든 품목의 SKU 및 가용성을 자동으로 확인하여 주문 오류를 줄입니다. 트랜잭션에서 게재를 통해 최적의 구매 환경을 제공하도록 [장바구니](cart.md) 및 [체크아웃 옵션](checkout-process.md)을(를) 구성할 수 있습니다. 이미 많은 정보가 계정에 있기 때문에 계정에 로그인한 고객은 빠르게 체크아웃을 완료할 수 있습니다. _체크아웃_ 페이지는 주문 트랜잭션을 완료하는 프로세스의 각 단계를 안내합니다. [즉시 구매](checkout-instant-purchase.md)를 활성화하면 고객은 계정에 저장된 정보를 사용하여 체크아웃 프로세스를 빠르게 진행할 수 있습니다.

>[!TIP]
>
>![Adobe Commerce B2B](../assets/b2b.svg) Adobe Commerce B2B를 설치하고 활성화하면 회사 계정과 연결된 고객에 대해 _빠른 주문_&#x200B;을 구성할 수 있습니다. 이 기능은 주문하려는 제품의 이름이나 SKU를 알고 있는 경우 주문 프로세스를 몇 번의 클릭으로 줄입니다. 회사 계정에 대해 협상 가능한 견적에 대한 지원을 구성할 수도 있습니다. B2B 기능에 대한 자세한 내용은 [Adobe Commerce B2B 사용 안내서](https://experienceleague.adobe.com/docs/commerce-admin/b2b/introduction.html)를 참조하십시오.

## 쇼핑 지원

경우에 따라 고객이 구매를 완료하기 위해 지원이 필요합니다. 어떤 고객들은 온라인 쇼핑을 좋아하지만, 전화로 주문하는 것을 선호한다. 귀하의 스토어에 계정을 등록한 고객과 고객 모두에게 즉시 도움을 제공할 수 있습니다.

- [장바구니 관리](shopping-assisted-cart-manage.md)
- 등록된 고객에 대해 [주문 만들기](customer-account-create-order.md)
- [주문 업데이트](order-update.md)

![장바구니](./assets/storefront-cart-price-group-discount.png){width="700" zoomable="yes"}

이 비디오를 시청하여 판매자 지원 쇼핑에 대해 알아보십시오.

>[!VIDEO](https://video.tv.adobe.com/v/343662/?quality=12&learn=on)

## 주문 관리 및 운영

관리자에서 주문 워크플로의 각 단계에 있는 정보에 액세스하고 주문을 처리할 수 있습니다.

- [주문](orders.md) 페이지에서는 판매자에게 현재 모든 주문에 대해 쉽게 액세스할 수 있는 목록을 제공하며 기존 주문을 편집 및 처리하고 고객을 대신하여 주문을 만들 수 있는 도구를 포함합니다.

- [송장](invoices.md) 페이지에 임시 판매 주문을 기반으로 하는 송장이 나열되어 있으며, 이 주문에 대한 영구 기록을 제공합니다.

- [배송](shipments.md) 페이지에는 배송 준비가 된 각 송장의 배송 기록이 나열됩니다.

- [대변 메모](credit-memos.md) 페이지에서 상인은 고객에게 지불해야 할 금액을 표시하는 문서인 대변 메모를 처리하고 관리할 수 있습니다. 해당 금액은 구매에 적용되거나 고객에게 환불될 수 있습니다.

- ![Adobe Commerce](../assets/adobe-logo.svg)(Adobe Commerce만 해당) [반품](returns.md) 페이지에는 현재 반품된 상품 요청(RMA)이 나열되며 새 반품 요청을 입력하는 데 사용됩니다.

- [거래](transactions.md) 페이지에는 스토어와 결제 시스템 간에 발생한 모든 결제 활동이 나열되며 보다 자세한 정보에 대한 액세스 권한이 제공됩니다.

## 배송 및 배송

고객에게 여러 [게재 방법](delivery.md) 중 하나를 선택할 수 있는 스토어가 단일 방법을 사용하는 스토어보다 전환율이 높다는 연구 결과가 있습니다. 관리자는 판매자가 여러 배달 방법과 [배달 회사](carriers.md)를 설정하고 [배달 레이블](shipping-labels.md)을 인쇄하는 데 사용할 수 있는 다양한 도구를 제공합니다.
