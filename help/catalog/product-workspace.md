---
title: 제품 작업 영역
description: 제품 작업 영역에서 사용할 수 있는 설정 및 컨트롤에 대해 알아봅니다.
exl-id: 8258b117-56d2-4d5f-9413-80d51fd5eae6
feature: Catalog Management, Products, Admin Workspace
source-git-commit: 01148770946a236ece2122be5a88b963a0f07d1f
workflow-type: tm+mt
source-wordcount: '463'
ht-degree: 0%

---

# 제품 작업 영역

사용된 속성 세트에 따라 필드 선택이 변경되지만 제품 작업 영역은 기본적으로 모든 제품 유형에 대해 동일합니다. 제품 속성은 양식 상단에 있으며 다음으로 제품 정보의 확장 가능한 섹션이 옵니다. 새 제품이 처음 저장될 때 _[!UICONTROL Store View]_선택기는 양식의 왼쪽 위에 나타납니다.

![제품 작업 영역](./assets/product-workspace-ee.png){width="700" zoomable="yes"}

## [!UICONTROL Enable Product] 설정

제품의 온라인 상태는 양식 상단에 있는 스위치로 표시됩니다. 온라인 상태를 변경하려면 다음을 설정하십시오. **[!UICONTROL Enable Product]** 다음으로 전환 `Yes` 또는 `No`.

| 제어 | 설명 |
|-------- | ----------- |
| ![예 전환](../assets/toggle-yes.png) | 제품이 온라인 상태임을 나타냅니다. |
| ![아니요 전환](../assets/toggle-no.png) | 제품이 오프라인 상태임을 나타냅니다. |

{style="table-layout:auto"}

## 속성 집합

의 이름입니다. [속성 집합](attribute-sets.md) 은 왼쪽 위 모서리에 나타나며 제품 레코드에 나타나는 필드를 결정합니다. 다른 속성 세트를 선택하려면 기본 속성 세트 이름 옆의 아래쪽 화살표를 클릭합니다.

![속성 집합](./assets/product-attribute-set.png){width="600" zoomable="yes"}

## 확장/축소

섹션을 확장하거나 축소하려면 확장 을 클릭합니다 ![확장 선택기](../assets/icon-display-expand.png) 또는 접기 ![선택기 접기](../assets/icon-display-collapse.png) 아이콘.

## [!UICONTROL Save] 메뉴

다음 _[!UICONTROL Save]_메뉴에는 저장 및 계속, 제품 저장 및 만들기, 제품 저장 및 복제 또는 저장 및 닫기를 사용할 수 있는 몇 가지 옵션이 포함되어 있습니다.

![저장 메뉴](./assets/product-save-menu.png){width="600" zoomable="yes"}

| 명령 | 설명 |
|--- |--- |
| [!UICONTROL Save] | 현재 제품을 저장하고 작업을 계속합니다. |
| [!UICONTROL Save & New] | 현재 제품을 저장하고 닫은 다음 동일한 제품 유형 및 템플릿을 기준으로 새 제품을 시작합니다. |
| [!UICONTROL Save & Duplicate] | 현재 제품을 저장하고 닫은 다음 새 복사본을 엽니다. |
| [!UICONTROL Save & Close] | 현재 제품을 저장하고 _[!UICONTROL Products]_작업 영역. |

{style="table-layout:auto"}

## 기본 필드 값

제품을 만들 때 시간을 절약하기 위해 여러 제품 필드의 기본값은 다른 필드의 값을 참조합니다. 기본값을 사용하거나 다른 값을 입력할 수 있습니다. 다음 필드에 기본값이 자동으로 생성되었습니다.

| 필드 | 기본값 |
|----- |------- |
| [!UICONTROL SKU] | 제품 이름을 기반으로 합니다. |
| [!UICONTROL Meta Title] | 제품 이름을 기반으로 합니다. |
| [!UICONTROL Meta Keywords] | 제품 이름을 기반으로 합니다. |
| [!UICONTROL Meta Description] | 제품 이름 및 설명을 기반으로 합니다. |

{style="table-layout:auto"}

다른 필드의 값을 나타내는 자리 표시자는 중괄호로 묶입니다. 제품에 포함된 모든 속성 코드 [속성 집합](attribute-sets.md) 자리 표시자로 사용할 수 있습니다.

![제품 필드 자동 생성](../configuration-reference/catalog/assets/catalog-product-fields-auto-generation.png){width="600" zoomable="yes"}

이러한 설정에 대한 자세한 목록이 필요하면 를 참조하십시오. [제품 필드 자동 생성](../configuration-reference/catalog/catalog.md#product-fields-auto-generation) 다음에서 _구성 참조_.

### 자리 표시자 값 편집

1. 다음에서 _관리자_ 사이드바, 이동 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. 왼쪽 패널에서 를 확장합니다. **[!UICONTROL Catalog]** 및 선택 **[!UICONTROL Catalog]** 밑에.

1. 확장 ![확장 선택기](../assets/icon-display-expand.png) 다음 **[!UICONTROL Product Fields Auto-Generation]** 및 를 정렬하고 필요한 대로 자리 표시자 값을 변경합니다.

   예를 들어 모든 제품에 대해 포함할 특정 키워드나 모든 메타 설명에 포함할 구문이 있는 경우 해당 필드에 직접 값을 입력합니다.

   >[!NOTE]
   >
   >기존 자리 표시자 값을 유지하려면 각 마크업 태그를 둘러싸는 이중 중괄호를 유지합니다.

1. 완료되면 다음을 클릭하십시오. **[!UICONTROL Save Config]**.

### 일반 자리 표시자

- `{{color}}`
- `{{country_of_manufacture}}`
- `{{description}}`
- `{{gender}}`
- `{{material}}`
- `{{name}}`
- `{{short_description}}`
- `{{size}}`
- `{{sku}}`
