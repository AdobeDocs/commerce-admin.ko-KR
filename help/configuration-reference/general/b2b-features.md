---
title: '[!UICONTROL General] &gt; [!UICONTROL B2B Features]'
description: Commerce 관리자의 [!UICONTROL General] &gt; [!UICONTROL B2B Features] 페이지에서 구성 설정을 검토하십시오.
exl-id: fc07a067-b92a-49c7-8512-2dfcc1c6ba0c
feature: Configuration, B2B
source-git-commit: 61df9a4bcfaf09491ae2d353478ceb281082fa74
workflow-type: tm+mt
source-wordcount: '342'
ht-degree: 1%

---

# [!UICONTROL General] > [!UICONTROL B2B Features]

{{b2b-feature}}

{{config}}

>[!TIP]
>
>Adobe Commerce B2B를 설치하고 활성화하면 회사별 기능을 사용하여 구매 경험을 개인화할 수 있습니다. Adobe Commerce B2B는 B2B 및 B2C 모델을 모두 지원하는 통합 솔루션입니다. B2B 기능에 대한 자세한 내용은 [_Adobe Commerce B2B 사용 안내서_](https://experienceleague.adobe.com/docs/commerce-admin/b2b/introduction.html)를 참조하십시오.

## [!UICONTROL B2B Features]

![B2B 기능](./assets/b2b-features.png)<!-- zoom -->

| 필드 | [범위](../../getting-started/websites-stores-views.md#scope-settings) | 설명 |
|------- |----------------------------------------------------------------------- |------------ |
| [[!UICONTROL Enable Company]](../../b2b/account-companies.md) | 웹 사이트 | 활성화되면 고객은 계정 대시보드에서 회사 할당을 관리할 수 있으며 기본적으로 공유 카탈로그 및 B2B 견적 기능도 사용할 수 있습니다. 옵션: `Yes` / `No` |
| [[!UICONTROL Enable Quick Order]](../../b2b/quick-order.md) | 웹 사이트 | 활성화되면 고객 및 게스트는 SKU 또는 제품 이름을 기반으로 신속하게 주문을 할 수 있습니다. 옵션: `Yes` / `No` |
| [[!UICONTROL Enable Requisition List]](../../b2b/configure-requisition-lists.md) | 웹 사이트 | 활성화되면 고객은 계정 대시보드에서 구매요청 목록을 생성하고 관리할 수 있습니다. |

{style="table-layout:auto"}

회사 및 공유 카탈로그가 활성화된 ![B2B 기능](./assets/b2b-features-company-enabled.png)<!-- zoom -->

회사 기능이 활성화되면 공유 카탈로그 및 B2B 견적에 추가 필드를 사용할 수 있습니다.

| 필드 | [범위](../../getting-started/websites-stores-views.md#scope-settings) | 설명 |
|------- |----------------------------------------------------------------------- |------------ |
| [[!UICONTROL Enable Shared Catalog]](../../b2b/catalog-shared.md) | 웹 사이트 | 활성화되면 세계적으로 사용할 수 있거나 특정 회사에 제한된 사용자 지정 가격으로 조정된 카탈로그를 만들 수 있습니다. 옵션: `Yes` / `No` |
| [!UICONTROL Enable Shared Catalog direct products price assigning] | 웹 사이트 | _[!UICONTROL Enable Shared Catalog]_필드를 `Yes`(으)로 설정하면 이 옵션을 사용할 수 있습니다. 활성화된 경우 공유 카탈로그에 지정된 제품만 가격 인덱스에 저장됩니다. 공유 카탈로그에 할당되지 않은 제품은 상점 앞에 표시되지 않습니다. 옵션: `Yes` / `No` |
| [[!UICONTROL Enable B2B Quote]](../../b2b/configure-quotes.md) | 웹 사이트 | 활성화되면 회사 구매자는 장바구니에서 견적에 대한 요청을 제출할 수 있습니다. 옵션: `Yes` / `No` |

{style="table-layout:auto"}

### [!UICONTROL Default B2B Payment Methods]

![B2B 구성 - 기본 결제 방법 설정](./assets/b2b-features-default-payment-methods.png)<!-- zoom -->

| 필드 | [범위](../../getting-started/websites-stores-views.md#scope-settings) | 설명 |
|------- |----------------------------------------------------------------------- |------------ |
| [!UICONTROL Applicable Payment Methods] | 글로벌 | B2B 구매자가 사용할 수 있는 결제 방법 선택을 결정합니다. 옵션: `All Payment Methods` / `Specific Payment Methods` |
| [!UICONTROL Payment Methods] | 글로벌 | B2B 구매자가 사용할 수 있는 각 결제 방법을 지정합니다. |

{style="table-layout:auto"}

### [!UICONTROL Default B2B Shipping Methods]

![B2B 구성 - 기본 배송 방법](./assets/b2b-features-shipping-methods.png)<!-- zoom -->

| 필드 | [범위](../../getting-started/websites-stores-views.md#scope-settings) | 설명 |
|------- |----------------------------------------------------------------------- |------------ |
| [!UICONTROL Applicable Shipping Methods] | 글로벌 | B2B 구매자가 기본적으로 사용할 수 있는 배송 방법의 선택을 결정합니다. 옵션: `All Shipping Methods` / `Specific Shipping Methods` |
| [!UICONTROL Shipping Methods] | 글로벌 | B2B 구매자가 기본적으로 사용할 수 있는 각 배송 방법을 지정합니다. <br/>**_참고:_**특정 [회사 계정](../../b2b/account-companies.md)에 대한 배송 방법을 제한할 수도 있습니다. |

{style="table-layout:auto"}

## [!UICONTROL Order Approval Configuration]

![B2B 기능 - 주문 승인 구성](./assets/b2b-features-order-approval.png)<!-- zoom -->

| 필드 | [범위](../../getting-started/websites-stores-views.md#scope-settings) | 설명 |
|------- |----------------------------------------------------------------------- |------------ |
| [[!UICONTROL Enable Purchase Orders]](../../stores-purchase/purchase-order.md) | 웹 사이트 | 활성화되면 회사에서 구매 발주를 생성할 수 있습니다. 옵션: `Yes` / `No` |

{style="table-layout:auto"}


