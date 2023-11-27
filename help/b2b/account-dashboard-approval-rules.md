---
title: 구매 주문 승인 규칙
description: 구매 주문 승인 규칙과 회사 관리자가 상점 첫 화면에서 규칙을 정의하는 방법에 대해 알아봅니다.
exl-id: e8d8bbc9-41cf-4024-85cc-92f0b0ce32d6
feature: B2B, Companies, Configuration
role: Admin
source-git-commit: 03d1892799ca5021aad5c19fc9f2bb4f5da87c76
workflow-type: tm+mt
source-wordcount: '658'
ht-degree: 0%

---

# 구매 주문 승인 규칙

대부분의 회사는 구매 발주에 대한 주문 승인을 요구합니다. 회사 계정에 대한 승인 규칙을 추가하여 구매 발주를 생성할 수 있는 사용자와 구매 가능 금액을 제어할 수 있습니다. For example:

* X보다 작은 PO는 자동으로 승인됩니다.
* X값을 초과하지만 Q보다 작은 PO는 Y의 승인을 받아야 합니다.
* X를 초과하는 모든 PO는 Y와 Z의 승인을 받아야 합니다.
* Director 수준 이상의 사용자가 만든 PO는 자동으로 승인됩니다.

회사 역할 및 권한에 따라, 사용자는 승인 규칙을 만들거나, 편집하거나, 삭제하거나, 볼 수 있습니다.

>[!IMPORTANT]
>
>승인 규칙 설정에는 정의된 항목이 필요합니다. [회사 구조](account-company-structure.md) 구매 고객의 관리자에 의한 승인을 명시하기 위해.

## 결제 방법

구매 발주 승인 흐름은 온라인 및 오프라인 결제 방법을 모두 지원합니다. 모든 기본 오프라인 결제 방법은 구매 발주 승인용으로 지원됩니다. 온라인 결제의 경우 다음과 같은 방법이 지원됩니다.

* 페이팔 익스프레스
* Braintree 결제


## 승인 규칙 설정

(필수 포함) [해당 역할에 대한 권한](account-company-roles-permissions.md), B2B 고객은 을 클릭하여 회사 정책을 적용하는 승인 규칙을 설정할 수 있습니다. **[!UICONTROL Approval Rules]** 왼쪽 패널에서 고객 계정을 검색합니다.

![회사 승인 규칙](./assets/approval-rules.png){width="700" zoomable="yes"}

승인 규칙을 만들기 위해 고객은 다음 단계를 완료합니다.

1. 클릭수 **[!UICONTROL Add New Rule]** 을 클릭하여 규칙을 만듭니다.

1. 필요한 경우 다음에서 규칙을 변경합니다. **[!UICONTROL Enabled]** 끝 **[!UICONTROL Disabled]**.

   규칙은 기본값으로 활성화되어 있지만 고객은 비활성화된 설정을 사용하여 규칙을 만든 다음 시행할 준비가 되면 나중에 활성화할 수 있습니다.

1. 대상 **[!UICONTROL Rule name]**&#x200B;를 입력하면 규칙에 대해 짧지만 설명적인 이름을 입력합니다. `Orders less than $100`.

   규칙 이름은 고유해야 합니다.

1. 대상 **[!UICONTROL Description]**&#x200B;에 더 자세한 규칙 설명을 입력합니다.

1. 대상 **[!UICONTROL Applies to]**&#x200B;에서 규칙을 적용하는 데 사용되는 회사 역할을 하나 이상 선택합니다.

1. 다음을 선택합니다. **[!UICONTROL Rule Type]** 규칙을 정의합니다.

   다음 섹션에서는 각 규칙 유형에 대한 자세한 설명과 예를 제공합니다.

   ![새 승인 규칙 만들기](./assets/approval-rules-create.png){width="700" zoomable="yes"}

1. 대상 **[!UICONTROL Requires approval from]**&#x200B;에서는 승인 유형에 따라 필요한 승인자를 한 명 이상 선택합니다.

   >[!NOTE]
   >
   >* 승인자로 역할을 할당할 때 해당 역할에 최소 한 명 이상의 사용자가 있어야 합니다.
   >* 승인자 역할이 같은 사용자가 2명 이상 있는 경우 구매 발주 작성자는 승인할 수 없습니다. 이 경우 이 승인자 역할을 가진 다른 사용자는 수동 승인이 필요합니다. 그러나 다음과 같은 경우에는 `Auto-approve POs created within this role` 옵션이에 설정됨 [역할 권한](account-company-roles-permissions.md), 구매 발주가 자동으로 승인됩니다.
   >* 승인자 역할을 가진 사용자가 한 명이고 이 사용자가 작성자인 경우 구매 발주는 항상 자동으로 승인됩니다. `Auto-approve POs created within this role` 권한 설정은 무시됩니다.

1. 클릭 **[!UICONTROL Save]**.

### [!UICONTROL Order Total]

이 규칙 유형은 세금을 포함하여 주문 합계를 기준으로 PO 승인을 요구하는 데 사용됩니다.

1. 다음 선택 **[!UICONTROL Order Total amount]** 옵션:

   * `is more than`
   * `is less than`
   * `is more than or equal to`
   * `is less than or equal to`

1. 통화 유형을 선택하고 금액을 입력합니다.

![주문 합계 승인 규칙](./assets/approval-rules-order-total.png){width="600" zoomable="yes"}

### [!UICONTROL Shipping Cost]

이 규칙 유형은 많은 회사에서 요구하는 배송 비용에 따른 PO 승인이 필요한 데 사용됩니다.

1. 를 설정합니다. **[!UICONTROL Shipping cost value]**:

   * `is more than`
   * `is less than`
   * `is more than or equal to`
   * `is less than or equal to`

1. 원하는 배송 금액을 설정합니다.

![운송비 승인 규칙](./assets/approval-rules-shipping-cost.png){width="600" zoomable="yes"}

### [!UICONTROL Number of SKUs]

이 규칙 유형은 주문의 SKU 또는 고유 제품 수를 기반으로 PO 승인이 필요한 데 사용됩니다. 주문되는 항목 수가 아니라 개별 항목 유형의 수를 제어합니다. 예를 들어 PO에는 다음이 포함될 수 있습니다.

* 흰색의 큰 셔츠 두 장이요
* 중간 크기의 흰색 셔츠 3개

이 예는 5개의 항목을 지정하지만 두 개의 개별 SKU를 지정합니다.

1. 를 설정합니다. **[!UICONTROL Number of SKUs]** 값:

   * `is more than`
   * `is less than`
   * `is more than or equal to`
   * `is less than or equal to`

1. SKU 수량을 설정합니다.

![SKU 승인 규칙 수](./assets/approval-rules-number-skus.png){width="600" zoomable="yes"}

## 승인 규칙 편집

기존 승인 규칙을 수정하려면 다음 단계를 완료할 수 있습니다.

1. 계정의 사이드바에서 고객은 다음을 선택합니다 **[!UICONTROL Approval Rules]**.

1. 편집할 승인 규칙 항목을 찾습니다.

1. 클릭수 **[!UICONTROL Edit]**.

1. 필요한 모든 변경 및 클릭 **[!UICONTROL Save]**.

## 승인 규칙 삭제

기존 승인 규칙을 제거하기 위해 고객은 다음 단계를 완료할 수 있습니다.

1. 계정의 사이드바에서 **[!UICONTROL Approval Rules]**.

1. 삭제할 승인 규칙 항목을 찾습니다.

1. 클릭수 **[!UICONTROL Delete]**.

1. 작업을 확인하려면 을 클릭합니다. **[!UICONTROL OK]**.

## 구매 주문 승인 데모

이 비디오를 통해 구매 주문 승인에 대해 알아보십시오.

>[!VIDEO](https://video.tv.adobe.com/v/344450?quality=12)
