---
title: 제품 목록
description: 제품을 만들고 기존 제품을 편집할 수 있는 관리자의 _[!UICONTROL Products]_ 페이지에 대해 알아봅니다.
exl-id: 47e14f72-017f-456a-8904-6d32ef47e6f1
feature: Catalog Management, Products, Admin Workspace
source-git-commit: 270a549af1a3eeda6c01f806171ede9d8a41b5d2
workflow-type: tm+mt
source-wordcount: '884'
ht-degree: 0%

---

# 제품 목록

관리자의 _[!UICONTROL Products]_페이지에서 카탈로그의 모든 제품에 액세스할 수 있습니다. 이 페이지에서 제품을 만들고 기존 제품을 편집할 수 있습니다. 다중 사이트 설치의 경우 각 웹 사이트는 동일한 카탈로그에서 판매될 다양한 제품을 제공할 수 있습니다.

_[!UICONTROL Products]_목록에는 카탈로그에 있는 모든 제품이 포함되어 있으며 이러한 제품을 사용할 수 있는 웹 사이트 및 현재 판매가 활성화되어 있는 경우 해당 웹 사이트를 나타냅니다. [공유 카탈로그](../b2b/catalog-shared.md)가 활성화된 Adobe Commerce B2B 설치에서 그리드에는 공유 카탈로그에 대체 할인 가격이 있는 제품을 나타내는 열이 포함되어 있습니다.

목록 페이지를 페이지별로 찾아보거나 특정 제품을 검색할 수 있습니다. 표준 [컨트롤](../getting-started/admin-grid-controls.md)을 사용하여 목록을 정렬 및 필터링하고 선택한 제품에 [작업](../getting-started/admin-actions-control.md)을(를) 적용하세요.

![제품 표](./assets/products-grid.png){width="700" zoomable="yes"}

## 제품 표시 제한

큰 카탈로그의 성능을 개선하려면 그리드에 표시되는 제품 수를 제한하는 것이 좋습니다. 다음에 대해 표시되는 제품 그리드를 제한할 수 있습니다.

- 제품 페이지
- 관련/상향 판매/교차 판매 제품 추가
- 번들 제품에 제품 추가
- 그룹 제품에 제품 추가
- 주문 만들기(관리자)

제품 표시 제한에 대한 이 구성 설정은 기본적으로 비활성화되어 있습니다. 활성화하면 그리드의 제품 수를 특정 값으로 제한할 수 있습니다. 활성화된 경우 그리드 표시에 대해 일치하는 제품의 수가 레코드 제한보다 크면 제한된 레코드 컬렉션이 반환됩니다. 제한에 도달하면 검색된 총 레코드, 선택한 레코드 수 및 페이지 매김 요소가 그리드 헤더에 표시되지 않습니다.

>[!NOTE]
>
>제품 그리드를 제한하지 않으려면 필터를 더 정확하게 사용하여 _[!UICONTROL Records Limit]_필드에 지정된 개수보다 적은 항목이 있는 컬렉션을 만드십시오.

**_제품 표시 제한을 구성하려면:_**

1. _관리자_ 사이드바에서 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**(으)로 이동합니다.

1. **[!UICONTROL Advanced]**&#x200B;을(를) 확장하고 **[!UICONTROL Admin]**&#x200B;을(를) 선택합니다.

1. **[!UICONTROL Admin Grids]** 섹션에서 ![확장 선택기](../assets/icon-display-expand.png)를 확장하고 다음을 수행합니다.

   - **[!UICONTROL Limit Number of Products in Grid]**&#x200B;을(를) `Yes`(으)로 설정합니다.

   - (선택 사항) 그리드의 제품 수를 특정 값으로 제한하려면 **[!UICONTROL Records Limit]** 필드에 값을 입력합니다. 기본 최소값은 `20000`입니다.

   ![관리 그리드 구성 설정](../configuration-reference/advanced/assets/admin-admin-grids.png){width="600" zoomable="yes"}

1. 완료되면 **[!UICONTROL Save Config]**&#x200B;을(를) 클릭합니다.

## 페이지 컨트롤

| 제어 | 설명 |
|--- |--- |
| [!UICONTROL Add Product] | 새 단순 제품을 만드는 프로세스를 시작합니다. 특정 제품 유형을 선택하려면 아래쪽 화살표를 클릭합니다. 옵션: [[!UICONTROL Simple Product]](product-create-simple.md) / [[!UICONTROL Configurable Product]](product-create-configurable.md) / [[!UICONTROL Grouped Product]](product-create-grouped.md) / [[!UICONTROL Virtual Product]](product-create-virtual.md) / [[!UICONTROL Bundle Product]](product-create-bundle.md) / [[!UICONTROL Downloadable Product]](product-create-downloadable.md) / [[!UICONTROL Gift Card]](product-gift-card-create.md) |
| [!UICONTROL Actions] | 목록에서 선택한 제품에 적용할 수 있는 모든 작업을 나열합니다. 제품이나 제품 그룹에 작업을 적용하려면 각 제품의 첫 번째 열에 있는 확인란을 선택합니다. 옵션: `Delete` / `Change Status` / `Update Attributes` / `Assign Inventory Source` / `Unassign Inventory Source` / `Transfer Inventory To Source` |
| [!UICONTROL Filters] | 현재 필터를 기반으로 카탈로그 검색을 시작합니다. |
| [!UICONTROL Default View] | 현재 그리드 열 레이아웃을 나타냅니다. 저장된 격자선 열 뷰가 있는 경우 다른 뷰를 선택할 수 있습니다. |
| [!UICONTROL Columns] | 목록에서 선택한 제품에 적용할 수 있는 모든 작업을 나열합니다. 제품이나 제품 그룹에 작업을 적용하려면 각 제품의 첫 번째 열에 있는 확인란을 선택합니다. |
| [!UICONTROL Search by keyword] | 왼쪽 상단 모서리의 검색 상자는 키워드로 제품을 찾는 데 사용됩니다. |
| [!UICONTROL Edit] | 제품을 편집 모드로 엽니다. 행의 아무 곳이나 클릭하여 동일한 작업을 수행할 수 있습니다. |

{style="table-layout:auto"}

## 기본 열

| 열 | 설명 |
|--- |--- |
| (확인란) | 여러 레코드를 선택하여 작업에 적용합니다. 선택한 각 레코드의 첫 번째 열에 있는 확인란이 표시됩니다. 옵션: <br/>**[!UICONTROL Select All]**- 현재 필터 설정과 일치하는 모든 레코드를 선택합니다.<br/>**[!UICONTROL Select All on This Page]** - 필터 설정과 일치하는 현재 페이지에 있는 레코드만 선택합니다. |
| [!UICONTROL ID] | 새 제품을 처음 저장할 때 할당되는 고유한 순차적 번호입니다. |
| [!UICONTROL Thumbnail] | 기본 제품 이미지의 썸네일을 표시합니다. |
| [!UICONTROL Name] | 제품 이름입니다. |
| [!UICONTROL Type] | 제품 유형. |
| [!UICONTROL Attribute Set] | 제품의 템플릿으로 사용되는 속성 세트의 이름입니다. |
| [!UICONTROL SKU] | 제품에 지정된 고유한 Stock Keeping Unit. |
| [!UICONTROL Price] | 제품의 단가입니다. |
| [!UICONTROL Quantity] | 재고 수량. |
| [!UICONTROL Salable Quantity] | 이 제품의 사용 가능한 모든 단위의 합계입니다. |
| [!UICONTROL Visibility] | 카탈로그에서 제품이 표시되는 위치를 나타냅니다. 옵션: `Not Visible Individually` / `Catalog` / `Search` / `Catalog, Search` |
| [!UICONTROL Status] | 제품의 상태를 나타냅니다. 옵션: `Enabled` 및 `Disabled` |
| [!UICONTROL Websites] | 제품을 사용할 수 있는 웹 사이트를 나타냅니다. |
| [!UICONTROL Remote Media URL] | 제품 미디어 자산이 [Commerce용 AEM Assets 통합](../content-design/aem-assets.md)을 사용하여 관리되는 경우 이 필드에는 자산이 보관되는 중앙 저장소인 AEM Assets Digital Asset Management Store에서 Commerce 자산을 볼 수 있는 URL이 표시됩니다. 이 필드는 AEM Assets 통합이 활성화된 경우에만 표시됩니다. |
| [!UICONTROL Action] | 제품을 편집 모드로 엽니다. |
| [!UICONTROL Shared Catalog] | ![Adobe Commerce B2B](../assets/b2b.svg)([Adobe Commerce B2B](./b2b/../introduction.md)에서만 사용 가능) 제품에 대한 사용자 지정 가격 책정이 포함된 공유 카탈로그를 나타냅니다. |

{style="table-layout:auto"}

## 기타 열

| 열 | 설명 |
|--- |--- |
| [!UICONTROL Short Description] | 제품에 대한 간략한 설명. |
| [!UICONTROL Special Price From Date] | 특별 가격 프로모션의 첫 번째 날짜입니다. |
| [!UICONTROL Special Price To Date] | 특별 가격 프로모션의 마지막 날짜입니다. |
| [!UICONTROL Cost] | 항목의 실제 비용. |
| [!UICONTROL Manufacturer] | 제품 제조업체. |
| [!UICONTROL Meta Keywords] | 제품에 대한 메타 키워드입니다. |
| [!UICONTROL Color] | 제품 색상입니다. |
| [!UICONTROL Set Product as New from Date] | 새 판촉으로 설정된 제품의 첫 번째 날짜입니다. |
| [!UICONTROL Set Product as New to Date] | 새 판촉으로 설정된 제품의 마지막 날짜입니다. |
| [!UICONTROL Active From / To] | 제품 시작 및 종료 날짜. |
| [!UICONTROL Layout] | 제품 레이아웃. |
| [!UICONTROL Minimum Advertised Price] | 제품의 최소 광고 가격. |
| [!UICONTROL Allow Gift Message] | 기프트 카드를 구매하는 고객에게 보내는 기프트 메시지. |
| [!UICONTROL Special Price] | 제품에 대한 특별 가격. |
| [!UICONTROL Weight] | 제품 무게. |
| [!UICONTROL Meta Title] | 제품에 대한 메타 제목입니다. |
| [!UICONTROL Meta Description] | 제품 메타데이터 설명. |
| [!UICONTROL Country of Manufacture] | 제조 국가입니다. |
| [!UICONTROL New Theme] | 제품에 사용자 지정 테마를 적용했습니다. |
| [!UICONTROL URL Key] | 제품의 URL 키. |
| [!UICONTROL Tax Class] | 제품 세금 분류. |
| [!UICONTROL Allow Gift Message] | 제품에 대한 선물 메시지 옵션의 사용 가능 여부를 표시합니다. |

{style="table-layout:auto"}
