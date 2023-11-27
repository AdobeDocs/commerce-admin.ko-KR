---
title: 고정 제품 세금(FPT)
description: 특정 유형의 제품에 추가되어야 하는 고정 제품 세금(FPT)을 설정하는 방법에 대해 알아봅니다.
exl-id: f1b475cb-a6fe-4b51-a0c3-7d0a202bd332
feature: Checkout, Invoices, Taxes, Products
source-git-commit: 8b5af316ab1d2e632ed5fc2066974326830ab3f7
workflow-type: tm+mt
source-wordcount: '867'
ht-degree: 0%

---

# 고정 제품 세금(FPT)

일부 과세관할에는 특정 유형의 상품에 추가되어야 하는 고정세가 있다. 다음을 설정할 수 있습니다. _고정 제품세_ (FPT) 스토어의 세금 계산에 필요한. 일부 국가에서는 FPT를 사용하여 Waste Electrical and Electronic Equipment (WEEE) 세금을 책정할 수 있습니다. 이 세금은 다음과 같이 알려집니다. _생태학적 세금_ 또는 _환경 세금_&#x200B;및 는 재활용 비용을 상쇄하기 위해 특정 유형의 전자기기에 수집됩니다. 제품 가격의 백분율이 아닌 고정 금액입니다.

고정 제품 세금은 제품을 기준으로 품목 레벨에서 적용됩니다. 일부 관할권에서는 이 세금에 대해 추가 % 세금 계산이 적용됩니다. 세금 관할 구역에는 세금이 있든 없든 제품 가격이 고객에게 표시되는 방식에 대한 규칙도 있을 수 있습니다. 규칙을 이해하고 그에 따라 FPT 표시 옵션을 설정해야 합니다.

이메일에서 FPT 가격을 인용할 때에는 가격의 차이가 주문에 대한 고객의 신뢰도에 영향을 미칠 수 있으므로 주의하십시오. 예를 들어 FPT를 표시하지 않고 주문 검토 가격을 표시하는 경우 관련 FPT가 있는 품목을 구매하는 고객은 FPT 세액이 포함된 합계를 볼 수 있지만 항목별 분류는 없습니다. 가격 차이로 인해 일부 고객은 총 금액이 예상 금액과 다르기 때문에 카트를 포기해야 할 수 있습니다.

## FPT 표시 가격

| FPT | 설정 및 계산 표시 | |
|--- |--- |---|
| 과세되지 않음 | **[!UICONTROL Excluding FPT]** | FPT는 장바구니에 별도의 행으로 표시되며 값은 적절한 세금 계산에 사용됩니다. |
| | **[!UICONTROL Including FPT]** | FPT는 항목의 기준 가격에 추가되지만 세금 규칙 기반 계산에는 포함되지 않습니다. |
| | **[!UICONTROL Excluding FPT, FPT Description, Final Price]** | 가격은 FPT 금액이나 설명 없이 나타납니다. FPT는 세금 규칙 기반 계산에 포함되지 않습니다. |
| 과세 | **[!UICONTROL Excluding FPT]** | FPT는 장바구니에 별도의 행으로 표시되며 값은 적절한 세금 계산에 사용됩니다. |
| | **[!UICONTROL Including FPT]** | FPT는 품목의 가격에 포함되므로 세금 계산에 대한 변경은 필요하지 않습니다. |
| | **[!UICONTROL Excluding FPT, FPT Description, Final Price]** | 가격은 FPT 금액이나 설명 없이 나타납니다. 그러나 FPT는 세금 규칙 기반 계산에 포함됩니다. |

{style="table-layout:auto"}

## FPT 구성

고정 제품 세금(FPT) [입력 유형](../catalog/attributes-input-types.md) 각 지역의 세금 관리를 위한 필드의 섹션을 생성합니다.

다음 지침은 &quot;에코 세금&quot;을 예로 사용하여 스토어에 대한 고정 제품 세금을 설정하는 방법을 보여 줍니다. 세금의 범위와 세금이 적용되는 국가 및 주를 설정한 후 선택한 옵션에 따라 입력 필드가 현지 요구 사항에 따라 변경될 수 있습니다. 자세한 내용은 다음을 참조하십시오. [제품 속성 만들기](../catalog/attribute-product-create.md).

### 1단계: 고정 제품 세금 사용

1. 다음에서 _관리자_ 사이드바, 이동 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. 왼쪽 패널에서 를 확장합니다. **[!UICONTROL Sales]** 및 선택 **[!UICONTROL Tax]**.

1. 확장 ![확장 선택기](../assets/icon-display-expand.png) 다음 **[!UICONTROL Fixed Product Taxes]** 섹션.

1. 설정 **[!UICONTROL Enable FPT]** 끝 `Yes`.

1. 고정 제품 세금이 매장 가격에 사용되는 방법을 결정하려면 다음 가격 표시 위치 각각에 대한 FPT 설정을 선택합니다.

   - **[!UICONTROL Display Prices in Product Lists]**
   - **[!UICONTROL Display Prices on Product View Page]**
   - **[!UICONTROL Display Prices in Sales Modules]**
   - **[!UICONTROL Display Prices in Emails]**

   옵션(각각에 대해 동일함):

   - `Including FPT Only`
   - `Including FPT and FPT description`
   - `Excluding FPT. Including FPT description and final price`
   - `Excluding FPT`

1. 설정 **[!UICONTROL Apply Tax to FPT]** 필요한 경우.

1. 설정 **[!UICONTROL Include FPT in Subtotal]** 필요한 경우.

   ![고정 제품 세금](../configuration-reference/sales/assets/tax-fixed-product-taxes.png){width="600" zoomable="yes"}

   이러한 각 구성 설정에 대한 자세한 설명은 을 참조하십시오. [고정 제품 세금](../configuration-reference/sales/tax.md#fixed-product-taxes) 다음에서 _구성 참조 안내서_.

1. 완료되면 다음을 클릭하십시오. **[!UICONTROL Save Config]**.

### 2단계: FPT 속성 만들기

1. 다음에서 _관리자_ 사이드바, 이동 **[!UICONTROL Stores]** > _[!UICONTROL Attributes]_>**[!UICONTROL Product]**.

1. 오른쪽 위 모서리에서 을(를) 클릭합니다. **[!UICONTROL Add New Attribute]** 다음을 수행합니다.

   - 대상 **[!UICONTROL Default Label]**&#x200B;속성을 식별하는 레이블을 입력합니다.

   - 설정 **[!UICONTROL Catalog Input for Store Owner]** 끝 `Fixed Product Tax`.

   ![속성 속성](./assets/tax-fpt-attribute-properties.png){width="600" zoomable="yes"}

1. 확장 ![확장 선택기](../assets/icon-display-expand.png) 다음 **[!UICONTROL Advanced Attribute Properties]** 섹션을 만들고 속성 옵션을 설정합니다.

   - **[!UICONTROL Attribute Code]** - 고유 식별자를 공백이나 특수 문자 없이 소문자로 입력합니다. 최대 길이는 30자입니다. 기본 레이블 필드의 텍스트에 필드를 비워 둘 수 있습니다.

   - **[!UICONTROL Add to Column Options]** - FPT 필드를 [제품 목록](../catalog/products-list.md), 다음으로 설정 `Yes`.

   - **[!UICONTROL Use in Filter Options]** - 다음을 수행할 수 있는 경우: [필터](../getting-started/admin-workspace.md) fpt 필드의 값을 기반으로 하는 그리드의 제품을으로 설정합니다. `Yes`.

   ![고급 속성 속성](./assets/tax-fpt-advanced-attribute-properties.png){width="600" zoomable="yes"}

1. (선택 사항) 왼쪽 패널에서 **[!UICONTROL Manage Labels]** 각 스토어 보기에 대한 기본 레이블 대신 사용할 레이블을 입력합니다.

   ![레이블 관리](./assets/attribute-new-manage-labels.png){width="600" zoomable="yes"}

1. 완료되면 다음을 클릭하십시오. **[!UICONTROL Save Attribute]**.

1. 메시지가 표시되면 [캐시](../systems/cache-management.md).

### 3단계: 속성 세트에 FPT 속성 추가

1. 다음에서 _관리자_ 사이드바, 이동 **[!UICONTROL Stores]** > _[!UICONTROL Attributes]_>**[!UICONTROL Attribute Set]**.

1. 목록에서 속성 세트를 클릭하여 레코드를 편집 모드로 엽니다.

   ![속성 집합 목록](./assets/attribute-sets-list.png){width="600" zoomable="yes"}

1. 다음 목록에서 FPT 속성을 드래그합니다. **[!UICONTROL Unassigned Attributes]** 의 오른쪽에 **[!UICONTROL Groups]** 가운데 열에 나열합니다.

   각 그룹 폴더는 제품 정보의 섹션에 해당합니다. 편집 모드에서 제품이 열려 있을 때 속성을 표시할 위치에 배치할 수 있습니다.

   ![속성 집합 편집](./assets/tax-fpt-attribute-set-drag.png){width="600" zoomable="yes"}

1. 완료되면 다음을 클릭하십시오. **[!UICONTROL Save]**.

1. 고정 제품 세금을 포함해야 하는 각 속성 세트에 대해 이 단계를 반복합니다.

### 4단계: 특정 제품에 FPT 적용

1. 다음에서 _관리자_ 사이드바, 이동 **[!UICONTROL Catalog]** > **[!UICONTROL Products]**.

1. 편집 모드에서 고정 제품 세금이 필요한 제품을 엽니다.

1. 다음 찾기 **[!UICONTROL FPT]** 속성 집합에 추가한 필드의 섹션에 있는 **[!UICONTROL Add Tax]**.

1. 제품에 적용할 세금을 지정합니다.

   ![캐나다에 대한 고정 제품세](./assets/tax-product-fpt-canada.png){width="600" zoomable="yes"}

   - 상거래 인스턴스에 여러 웹 사이트가 있는 경우 적절한 을(를) 선택합니다 **[!UICONTROL Website]** 및 기본 통화. 이 예제에서 필드는 기본적으로 로 설정됩니다 `All Websites [USD]`.

   - 설정 **[!UICONTROL Country/State]** 고정 제품 세금이 적용되는 지역에 적용됩니다.

   - 대상 **[!UICONTROL Tax]**&#x200B;고정 제품 세금을 10진 금액으로 입력합니다.

1. 고정 제품 세금을 더 추가하려면 **[!UICONTROL Add Tax]** 이 과정을 반복합니다.

1. 완료되면 다음을 클릭하십시오. **[!UICONTROL Save]**.
