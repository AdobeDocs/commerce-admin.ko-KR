---
title: 제품에 속성 추가
description: 카탈로그의 제품에 속성을 추가하는 방법을 알아봅니다.
exl-id: 1f92807a-2362-48a2-8d3a-4aef90a5671f
feature: Catalog Management, Products
source-git-commit: 99049260b4ff490845affd1c98fa4d2536edebd7
workflow-type: tm+mt
source-wordcount: '790'
ht-degree: 0%

---

# 제품에 속성 추가

속성은 주로 [스토어](../stores-purchase/stores-menu.md) 메뉴에서 새 속성을 추가할 수도 있습니다 _즉석_ 을 클릭합니다. 기존 속성 목록에서 선택하거나 속성을 만들 수 있습니다. 새 속성이 [속성 집합](../catalog/attribute-sets.md) 제품에 기준이 되는.

## 1단계: 속성 추가

1. 제품을 편집 모드로 엽니다.

1. 오른쪽 위 모서리에서 을(를) 클릭합니다. **[!UICONTROL Add Attribute]**.

   ![기본 속성 세트가 있는 새 제품](./assets/product-attribute-add.png){width="600" zoomable="yes"}

1. 기존 속성을 제품에 추가하려면 [필터 컨트롤](../getting-started/admin-grid-controls.md) 그리드에서 속성을 찾아 다음을 수행합니다.

   - 추가할 각 속성의 첫 번째 열에서 확인란을 선택합니다.

   - 클릭 **[!UICONTROL Add Selected]**.

   ![속성 선택](./assets/product-attribute-add-select.png){width="600" zoomable="yes"}

1. 새 속성을 정의하려면 **[!UICONTROL Create New Attribute]** 2단계의 항목을 완료합니다.

## 2단계: 기본 속성 속성 설명

![속성 속성](./assets/product-attribute-add-new.png){width="600" zoomable="yes"}

1. 아래 _[!UICONTROL Attribute Properties]_, 다음을 입력합니다.**[!UICONTROL Attribute Label]**속성을 식별합니다.

1. 설정 **[!UICONTROL Catalog Input Type for Store Owner]** 다음 유형으로: [입력 제어](attributes-input-types.md) 데이터 입력에 사용됩니다.

   속성이 다음에 사용되는 경우 [구성 가능한 제품](product-create-configurable.md), 선택 `Dropdown`. 그런 다음 설정합니다. **[!UICONTROL Required]** 끝 `Yes`.

1. 대상 `Dropdown` 및 `Multiple Select` 입력 유형에서 다음을 수행합니다.

   - 아래 **[!UICONTROL Values]**, 클릭 **[!UICONTROL Add Value]**.

   - 목록에 표시할 첫 번째 값을 입력합니다.

     관리자용 값 하나를 입력하고 각 스토어 보기에 대한 값의 번역을 입력할 수 있습니다. 스토어 보기가 한 개만 있는 경우 관리 값만 입력할 수 있으며 이 값은 상점 간에도 사용됩니다.

   - 클릭 **[!UICONTROL Add Value]** 목록에 포함할 각 옵션에 대해 이전 단계를 반복합니다.

   - 선택 **[!UICONTROL Is Default]** 옵션을 기본값으로 사용합니다.

   ![값](./assets/product-attribute-add-values-colors.png){width="600" zoomable="yes"}

1. 제품을 구매하기 전에 고객이 옵션을 선택하도록 하려면 다음을 설정하십시오. **[!UICONTROL Required]** 끝 `Yes`.

## 3단계: 고급 속성 설명(선택 사항)

![고급 속성 속성](./assets/product-attribute-advanced-attribute-properties.png){width="600" zoomable="yes"}

1. 고유 항목 입력 **[!UICONTROL Attribute Code]** 소문자(공백 제외)입니다.

1. 설정 **[!UICONTROL Scope]** 속성을 사용할 수 있는 저장소 계층 구조의 위치를 나타냅니다.

   속성이 다음에 사용되는 경우 [구성 가능한 제품](product-create-configurable.md), 선택 `Global`.

1. 이 속성이 이 제품에만 적용되는 경우 다음을 설정하십시오. **[!UICONTROL Unique Value]** 끝 `Yes`.

1. 텍스트 필드에 입력한 데이터의 유효성 검사를 실행하려면 **[!UICONTROL Input Validation for Store Owner]** 필드에 포함해야 하는 데이터 형식을 입력합니다.

   값이 선택된 입력 유형에는 이 필드를 사용할 수 없습니다. 입력 유효성 검사는 다음 중 하나에 사용할 수 있습니다.

   - `Decimal Number`
   - `Integer Number`
   - `Email`
   - `URL`
   - `Letters`
   - `Letters (a-z, A-Z) or Numbers (0-9)`

   ![입력 유효성 검사](./assets/product-attribute-input-validation.png){width="500"}

1. 속성을 제품 그리드에 열로 포함하려면 을 설정합니다. **[!UICONTROL Add to Column Options]** 끝 `Yes`.

1. 을(를) 필터링하려면 _[!UICONTROL Products]_이 열의 격자, 설정&#x200B;**[!UICONTROL Use in Filter Options]**끝 `Yes`.

## 4단계: 필드 레이블 입력

1. 확장 ![확장 선택기](../assets/icon-display-expand.png) 다음 **[!UICONTROL Manage titles]** 섹션.

1. 입력 **[!UICONTROL Title]** 필드의 레이블로 사용됩니다.

   스토어를 다른 언어로 사용할 수 있는 경우 각 보기에 대해 번역된 제목을 입력할 수 있습니다.

   ![제목 관리](./assets/product-attribute-add-manage-titles.png){width="600" zoomable="yes"}

## 5단계: 상점 속성 설명

1. 확장 ![확장 선택기](../assets/icon-display-expand.png) 다음 **[!UICONTROL Storefront Properties]** 섹션.

   ![Storefront 속성](./assets/product-attribute-add-storefront-properties.png){width="600" zoomable="yes"}

1. 속성을 검색에 사용할 수 있도록 하려면 을 설정합니다. **[!UICONTROL Use in Search]** 끝 `Yes`.

1. 제품 비교에 속성을 포함하려면 을 설정합니다. **[!UICONTROL Comparable on Storefront]** 끝 `Yes`.

1. 레이어 탐색에 드롭다운, 다중 선택 또는 가격 속성을 포함하려면 다음을 설정하십시오. **[!UICONTROL Use in Search Results Layered Navigation]** 다음 중 하나를 수행합니다.

   - `Filterable (with results)` - 레이어 탐색에는 일치하는 제품을 찾을 수 있는 필터만 포함됩니다. 목록에 표시된 모든 제품에 이미 적용되는 속성 값은 사용 가능한 필터로 표시되지 않습니다. 제품 일치 개수가 0인 속성 값은 사용 가능한 필터 목록에서도 생략됩니다.<br/><br/>필터링된 제품 목록에는 필터와 일치하는 제품만 포함됩니다. 제품 목록은 선택한 필터가 표시된 것을 변경하는 경우에만 업데이트됩니다.

   - `Filterable (no results)` - 계층화된 탐색에는 제품 일치가 0인 제품을 포함하여 사용 가능한 모든 속성 값과 해당 제품 수에 대한 필터가 포함됩니다. 속성 값이 견본이면 값이 필터로 표시되지만 무시됩니다.

   >[!NOTE]
   >
   >다음의 경우 _[!UICONTROL Use in Search]_설정이 로 설정되어 있습니다. `No`,_[!UICONTROL Use in Search Results Layered Navigation]_ 설정이 표시되지 않고 제품 속성이 다음으로 검색에 사용되지 않음 [!UICONTROL Use in Layered Navigation] 값을 설정하는 중입니다.

1. 검색 결과 페이지의 레이어 탐색에서 속성을 사용하려면 을 설정합니다 **[!UICONTROL Use in Search Results Layered Navigation]** 끝 `Yes` 숫자를 입력합니다. **[!UICONTROL Position]** 필드.

   위치 번호는 계층화된 탐색 블록 내에서 속성의 상대적 위치를 나타낸다.

   >[!NOTE]
   >
   >다음 _[!UICONTROL Position]_필드는 기본적으로 흐리게 표시되며, 이 설정을 수정하려면 먼저 속성을 저장해야 합니다.

1. 가격 규칙에서 속성을 사용하려면 을 설정합니다. **[!UICONTROL Use for Promo Rule Conditions]** 끝 `Yes`.

1. 텍스트 서식을 HTML으로 지정하려면 다음을 설정합니다 **[!UICONTROL Allow HTML Tags on Storefront]** 끝 `Yes`.

   이 설정을 사용하면 필드를 편집할 때 WYSIWYG 편집기를 사용할 수 있습니다.

1. 제품 페이지에 속성을 포함하려면 을 설정합니다. **[!UICONTROL Visible on Catalog Pages on Storefront]** 끝 `Yes`.

1. 테마에서 지원하는 대로 다음 설정을 완료합니다.

   - 제품 목록에 속성을 포함하려면 을 설정합니다. **[!UICONTROL Used in Product Listing]** 끝 `Yes`.

   - 제품 목록의 정렬 매개 변수로 특성을 사용하려면 을 설정합니다. **[!UICONTROL Used for Sorting in Product Listing]** 끝 `Yes`.

1. 완료되면 다음을 클릭하십시오. **[!UICONTROL Save Attribute]**.
