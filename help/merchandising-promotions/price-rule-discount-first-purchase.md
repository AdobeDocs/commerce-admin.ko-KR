---
title: 장바구니 가격 규칙 예 - 첫 구매와 함께 할인
description: 장바구니 가격 규칙을 사용하여 처음 고객에게 할인을 제공하는 예를 검토하십시오.
exl-id: 46add769-6fa9-40e0-9f4f-af2215f36283
feature: Merchandising, Price Rules, Shopping Cart
source-git-commit: dbe31fa6e7b83ac852e6e4988ac61627e30d9089
workflow-type: tm+mt
source-wordcount: '737'
ht-degree: 0%

---

# 장바구니 가격 규칙 예 - 첫 구매와 함께 할인

{{ee-feature}}

장바구니 가격 규칙은 쿠폰이 필요 없이 첫 번째 구매 시 고객에게 자동으로 할인을 제공하는 데 사용할 수 있습니다.

처음 고객을 대상으로 하는 할인을 제공하려면 다음을 수행할 수 있습니다.

- 주문이 없는 _구매자_(으)로 정의된 고객 세그먼트를 만든 다음
- 새 고객 세그먼트를 타겟팅하는 장바구니 가격 규칙을 만듭니다.

>[!NOTE]
>
>고객 세그먼트 기능이 활성화되어 있는지 확인합니다. [고객 세그먼트 만들기](../customers/customer-segment-create.md)를 참조하세요.

## 1단계. 고객 세그먼트 만들기

1. _관리자_ 사이드바에서 **[!UICONTROL Customers]** > **[!UICONTROL Segments]**(으)로 이동합니다.

1. 오른쪽 상단에서 **[!UICONTROL Add Segment]**&#x200B;을(를) 클릭합니다.

1. **[!UICONTROL General Properties]** 정의.

   - 고객 세그먼트를 식별하려면 **[!UICONTROL Segment Name]**&#x200B;을(를) 입력하십시오(예: _처음 방문하는 고객_).

   - **[!UICONTROL Assigned to Website]**&#x200B;의 경우 고객 세그먼트를 사용할 수 있는 웹 사이트를 선택하십시오.

   - **[!UICONTROL Status]**&#x200B;에 대해 `Active`을(를) 선택합니다.

   - **[!UICONTROL Apply to]**&#x200B;에 대해 `Visitors and Registered Customers`을(를) 선택합니다.

   - 완료되면 **[!UICONTROL Save and Continue Edit]**&#x200B;을(를) 클릭합니다.

     왼쪽 패널에서 추가 옵션을 사용할 수 있습니다.

   ![고객 세그먼트 속성](./assets/customer-segment-first-time.png){width="600" zoomable="yes"}

1. **[!UICONTROL Conditions]** 정의.

   이 예제에서 조건은 _총 주문 수가 1_&#x200B;보다 작은 고객을 대상으로 합니다.

   - 왼쪽 패널에서 **[!UICONTROL Conditions]**&#x200B;을(를) 선택합니다.

     기본 조건은 &quot;다음 조건이 모두 TRUE인 경우&quot;로 시작됩니다.

   - _추가_(![추가 아이콘](../assets/icon-add-green-circle.png))을 클릭하고 `Number of Orders`을(를) 선택합니다.

   - **[!UICONTROL is]**&#x200B;을(를) 클릭하고 `less than`을(를) 선택합니다.

   - **..**&#x200B;을(를) 클릭하고 필드에 `1`을(를) 입력합니다.

   - 녹색 확인 표시( ![녹색 확인 표시](../assets/icon-checkmark-green-circle.png))를 클릭하여 조건 설정을 저장합니다.

   ![고객 세그먼트 조건](./assets/customer-segment-first-time-condition.png){width="600" zoomable="yes"}

1. **[!UICONTROL Save]**&#x200B;을(를) 클릭합니다.

고객 세그먼트가 만들어지고 _[!UICONTROL Customer Segments]_&#x200B;그리드에 표시됩니다.

>[!TIP]
>
>세그먼트 ID를 기록해 둡니다. 이 ID 번호를 사용하여 장바구니 가격 규칙을 만듭니다.

## 2단계. 장바구니 가격 규칙 만들기

1. _관리자_ 사이드바에서 **[!UICONTROL Marketing]** > _[!UICONTROL Promotions]_>**[!UICONTROL Cart Price Rule]**(으)로 이동합니다.

1. 오른쪽 상단에서 **[!UICONTROL Add New Rule]**&#x200B;을(를) 클릭합니다.

   **[!UICONTROL Rule Information]** 섹션이 기본적으로 표시되며 **[!UICONTROL Conditions]** 및 **[!UICONTROL Conditions]**&#x200B;의 확장 가능한 섹션이 있습니다.

1. **[!UICONTROL Rule Information]** 정의.

   - **[!UICONTROL Rule Name]** 및 **[!UICONTROL Description]** 필드를 완료합니다. 이 필드는 내부 참조용입니다.

   - **[!UICONTROL Websites]**&#x200B;의 경우 규칙을 사용할 수 있는 웹 사이트를 선택하십시오.

   - **[!UICONTROL Customer Groups]**&#x200B;에 대해 이 규칙이 적용되는 고객 그룹을 선택하십시오.

     여러 그룹을 선택하려면 Ctrl 키(PC) 또는 Command 키(Mac)를 누른 채 각 옵션을 클릭합니다.

     >[!NOTE]
     >
     >이 목록의 옵션은 **[!UICONTROL Customers]** > **[!UICONTROL Customer Groups]**&#x200B;에서 만들고 관리하는 고객 그룹에 따라 다릅니다.

   - **[!UICONTROL Coupon]**&#x200B;에 대해 `No Coupon`을(를) 선택합니다.

   - **[!UICONTROL Uses per Customer]**&#x200B;에 대해 `1`을(를) 입력하십시오.

   - **[!UICONTROL Priority]**&#x200B;에 숫자를 입력하여 다른 규칙과 관련하여 이 규칙의 우선 순위를 설정하십시오.

     >[!NOTE]
     >
     >동일한 카탈로그 제품이 두 개 이상의 가격 규칙에 대해 설정된 조건을 충족할 경우 우선순위 설정이 중요합니다. 우선 순위가 가장 높은 설정이 있는 규칙이 고객에 대해 활성화됩니다. 가장 높은 우선 순위는 1입니다. 이 예에서 `1`을(를) 입력하면 이 규칙이 다른 가격 규칙보다 먼저 적용됩니다. 이 값은 **[!UICONTROL Action]** 섹션의 **[!UICONTROL Discard Subsequent Rules]** 설정에서 사용됩니다.

   - 완료되면 **[!UICONTROL Save and Continue Edit]**&#x200B;을(를) 클릭합니다.

     왼쪽 패널에서 추가 옵션을 사용할 수 있습니다.

   ![장바구니 가격 규칙 정보](./assets/rule-information-first-time.png){width="600" zoomable="yes"}

1. **[!UICONTROL Conditions]** 정의.

   - 아래로 스크롤하여 **[!UICONTROL Conditions]** 섹션에서 ![확장 선택기](../assets/icon-display-expand.png)를 확장합니다.

     기본 규칙은 &quot;이 모든 조건이 TRUE인 경우:&quot;로 시작됩니다.

   - _추가_(![추가 아이콘](../assets/icon-add-green-circle.png))을 클릭하고 `Customer Segment`을(를) 선택합니다.

     한정자 필드의 기본값은 `matches`입니다.

   - **..**&#x200B;을(를) 클릭하고 타깃팅할 고객 세그먼트의 세그먼트 ID를 입력합니다.

     이 예제에서 1단계에서 만든 새 세그먼트의 세그먼트 ID는 `2`입니다.

     >[!NOTE]
     >
     >세그먼트 ID를 모를 경우 선택기 아이콘(![목록 아이콘](../assets/icon-list-chooser.png) )을 클릭하여 고객 세그먼트 목록을 표시합니다. 필드에 ID를 수동으로 입력하거나 원하는 세그먼트의 확인란을 선택하여 필드를 자동으로 채울 수 있습니다.

   - 녹색 확인 표시( ![녹색 확인 표시](../assets/icon-checkmark-green-circle.png))를 클릭하여 조건 설정을 저장합니다.

   - 완료되면 **[!UICONTROL Save and Continue Edit]**&#x200B;을(를) 클릭합니다.

     이 규칙 행은 고객 세그먼트 ID 2와 일치하는 모든 고객에게 적용됩니다.

   ![고객 세그먼트 조건](./assets/customer-segment-matches.png){width="400"}

1. 아래로 스크롤하여 ![확장 선택기](../assets/icon-display-expand.png)**[!UICONTROL Conditions]** 섹션을 확장하고 규칙에 대한 작업을 정의합니다.

   이 섹션에서는 할인 유형 및 처음 고객에게 적용할 할인의 값/금액을 정의합니다. 이 예에서는 정의된 조건을 충족하는 모든 고객에 대해 10% 할인을 정의합니다. 사용 가능한 다른 옵션에 대한 자세한 내용은 [장바구니 가격 규칙 만들기](price-rules-cart-create.md)를 참조하십시오.

   - **[!UICONTROL Apply]**&#x200B;에 대해 제품 가격 할인의 백분율을 선택하십시오.

   - **[!UICONTROL Discount Amount]**&#x200B;에 대해 `10`을(를) 입력하십시오.

   - 제품 금액에만 이 가격 규칙을 적용하려면 **[!UICONTROL Apply to Shipping Amount]**&#x200B;을(를) `No`(으)로 설정합니다.

   - 시스템이 동일한 제품에 여러 가격 규칙을 적용하지 않도록 하려면 **[!UICONTROL Discard Subsequent Rules]**&#x200B;을(를) `Yes`(으)로 설정하십시오.

   - 완료되면 **[!UICONTROL Save]**&#x200B;을(를) 클릭합니다.

   ![장바구니 가격 규칙 작업](./assets/actions-first-time.png){width="600" zoomable="yes"}

새 규칙은 일반적으로 한 시간 내에 사용할 수 있습니다. 규칙을 테스트하여 정의한 대로 작동하는지 확인합니다.

## 3단계: 규칙 저장 및 테스트

{{new-price-rule}}

1. 규칙이 완료되면 **[!UICONTROL Save Rule]**&#x200B;을(를) 클릭합니다.

1. 규칙이 올바르게 작동하는지 테스트합니다.
