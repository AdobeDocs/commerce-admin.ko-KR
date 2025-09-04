---
title: 가상 제품
description: 멤버십, 서비스, 보증 또는 구독과 같은 유형의 항목이 아닌 항목을 나타내는 가상 제품을 만드는 방법을 알아봅니다.
exl-id: 8788ba04-e911-429e-9e48-ce589f0c9fa1
feature: Catalog Management, Products
source-git-commit: 4a3aa2aa32b692341edabd41fdb608e3cff5d8e0
workflow-type: tm+mt
source-wordcount: '645'
ht-degree: 0%

---

# 가상 제품

가상 제품 또는 디지털 상품은 멤버십, 서비스, 보증 또는 구독 및 책, 음악, 비디오 또는 기타 제품의 디지털 다운로드와 같은 유형 이외의 항목을 나타냅니다. 가상 제품은 개별적으로 판매하거나 [그룹화된 제품](product-create-grouped.md), [구성 가능한 제품](product-create-configurable.md) 또는 [번들 제품](product-create-bundle.md) 제품 형식의 일부로 포함할 수 있습니다.

_[!UICONTROL Weight]_필드가 없는 것 외에 가상 제품과 간단한 제품을 만드는 과정은 동일합니다. 다음 지침은 [제품 템플릿](attribute-sets.md), 필수 필드 및 기본 설정을 사용하여 가상 제품을 만드는 프로세스를 보여 줍니다. 기본 사항을 완료하면 필요에 따라 다른 제품 설정을 완료할 수 있습니다.

>[!NOTE]
>
>PayPal은 PayPal Express Checkout을 통해 디지털 상품 판매를 더 이상 지원하지 않습니다. [PayPal 결제 표준](../stores-purchase/paypal-payments-standard.md) 또는 다른 PayPal 결제 게이트웨이를 사용하여 가상 제품이 포함된 주문을 처리하는 것이 좋습니다.

![가상 제품](./assets/product-virtual-membership.png){width="700" zoomable="yes"}

## 1단계: 제품 유형 선택

1. _관리자_ 사이드바에서 **[!UICONTROL Catalog]** > **[!UICONTROL Products]**(으)로 이동합니다.

1. 오른쪽 상단의 _[!UICONTROL Add Product]_( ![메뉴 화살표](../assets/icon-menu-down-arrow-red.png){width="25"}) 메뉴에서&#x200B;**[!UICONTROL Virtual Product]**을(를) 선택합니다.

   ![가상 제품 추가](./assets/product-add-virtual.png){width="700" zoomable="yes"}

## 2단계: 속성 세트 선택

제품의 템플릿으로 사용되는 [특성 집합](attribute-sets.md)을 선택하려면 다음 중 하나를 실행하십시오.

- **[!UICONTROL Attribute Set]** 필드를 클릭하고 특성 집합의 이름의 전체 또는 일부를 입력합니다.

- 표시된 목록에서 사용할 속성 세트를 선택합니다.

양식이 변경 사항을 반영하도록 업데이트됩니다.

![특성 집합 선택](./assets/product-create-choose-attribute-set.png){width="600" zoomable="yes"}

## 3단계: 필요한 설정 완료

1. **[!UICONTROL Product Name]** 입력.

1. 제품 이름을 기반으로 하는 기본 **[!UICONTROL SKU]**&#x200B;을(를) 사용하거나 다른 이름을 입력하십시오.

1. 제품 **[!UICONTROL Price]**&#x200B;을(를) 입력하십시오.

1. 제품을 아직 게시할 준비가 되지 않았으므로 **[!UICONTROL Enable Product]**&#x200B;을(를) `No`(으)로 설정하십시오.

1. **[!UICONTROL Save]**&#x200B;을(를) 클릭하고 계속합니다.

   제품을 저장하면 왼쪽 위 모서리에 [스토어 보기](introduction.md#product-scope) 선택기가 나타납니다.

1. 제품을 사용할 수 있는 **[!UICONTROL Store View]**&#x200B;을(를) 선택하십시오.

   ![스토어 보기 선택](./assets/product-create-store-view-choose.png){width="600" zoomable="yes"}

## 4단계: 기본 설정 완료

1. **[!UICONTROL Tax Class]**&#x200B;을(를) 다음 중 하나로 설정합니다.

   - `None`
   - `Taxable Goods`

1. 재고가 있는 제품의 **[!UICONTROL Quantity]**&#x200B;을(를) 입력하고 다음을 수행합니다.

   - **[!UICONTROL Stock Status]**&#x200B;의 기본 `In Stock` 설정을 사용합니다.

     가상 제품이 제공되지 않았으므로 **[!UICONTROL Weight]** 필드가 사용되지 않습니다.

   - **[!UICONTROL Visibility]**&#x200B;의 기본 `Catalog, Search` 설정을 사용합니다.

   >[!NOTE]
   >
   >[Inventory management](../inventory-management/introduction.md)을(를) 사용하도록 설정하면 단일 원본 판매자가 이 섹션에서 수량을 설정합니다. 다중 소스 판매자는 소스 섹션에서 소스 및 수량을 추가합니다. 다음 _소스 및 수량 할당(Inventory management)_ 섹션을 참조하십시오.

1. 제품에 **[!UICONTROL Categories]**&#x200B;을(를) 할당하려면 **[!UICONTROL Select…]** 상자를 클릭하고 다음 중 하나를 수행합니다.

   **기존 범주 선택**:

   - 일치하는 항목을 찾을 때까지 상자에 입력을 시작합니다.

   - 할당할 카테고리의 확인란을 선택합니다.

   **범주 만들기**:

   - **[!UICONTROL New Category]**&#x200B;을(를) 클릭합니다.

   - **[!UICONTROL Category Name]**&#x200B;을(를) 입력하고 메뉴 구조에서 위치를 결정하는 **[!UICONTROL Parent Category]**&#x200B;을(를) 선택합니다.

   - **[!UICONTROL Create Category]**&#x200B;을(를) 클릭합니다.

   제품을 설명하는 추가적인 개별 속성이 있을 수 있습니다. 선택 항목은 속성 세트에 따라 다르며 나중에 완료할 수 있습니다.

### 원본 및 수량 할당([!DNL Inventory Management])

{{$include /help/_includes/inventory-assign-sources.md}}

## 5단계: 제품 정보 작성

필요에 따라 다음 섹션의 정보를 작성합니다.

- [콘텐츠](product-content.md)
- [이미지 및 비디오](product-images-and-video.md)
- [검색 엔진 최적화](product-search-engine-optimization.md)
- [관련 제품, 상향 판매 및 교차 판매](related-products-up-sells-cross-sells.md)
- [사용자 정의 가능한 옵션](settings-advanced-custom-options.md)
- [웹 사이트의 제품](settings-basic-websites.md)
- [디자인](settings-advanced-design.md)
- [선물 옵션](product-gift-options.md)

>[!NOTE]
>
>_[!UICONTROL Is this downloadable product?]_옵션은 기본적으로 비활성화되어 있습니다. 가상 제품에 대해 이 기능을 사용하도록 설정하면 제품을 [다운로드 가능](product-create-downloadable.md#downloadable-product)합니다.

## 6단계: 제품 게시

1. 제품을 카탈로그에 게시할 준비가 되면 **[!UICONTROL Enable Product]**&#x200B;을(를) `Yes`(으)로 설정하십시오.

1. 다음 중 하나를 수행합니다.

   - **메서드 1:** 저장 및 미리 보기

      - 오른쪽 상단에서 **[!UICONTROL Save]**&#x200B;을(를) 클릭합니다.

      - 스토어에서 제품을 보려면 **[!UICONTROL Customer View]**&#x200B;관리자&#x200B;_(_&#x200B;메뉴 화살표![) 메뉴에서 ](../assets/icon-menu-down-arrow-black.png)을(를) 선택하십시오.

     저장소가 새 브라우저 탭에서 열립니다.

     ![고객 보기](./assets/product-admin-customer-view.png){width="600" zoomable="yes"}

   - **메서드 2:** 저장 및 닫기

     _[!UICONTROL Save]_(![메뉴 화살표](../assets/icon-menu-down-arrow-red.png){width="25"}) 메뉴에서&#x200B;**[!UICONTROL Save & Close]**을(를) 선택합니다.

## 기억해야 할 사항

- 가상상품은 서비스, 가입, 보증 등 비유형적 상품에 활용된다.

- 가상 제품은 단순한 제품과 매우 유사하지만 무게는 없습니다.

- 장바구니에 유형의 제품이 없는 한 체크아웃 중에는 배송 옵션이 나타나지 않습니다.

<!-- Last updated from includes: 2023-05-19 17:14:58 -->
