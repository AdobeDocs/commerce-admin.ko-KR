---
title: 제품 설정 - [!UICONTROL Sources]
description: 제품의 경우 [!UICONTROL Sources] 설정은 제품을 배포할 수 있는  [!DNL Inventory Management] 소스에 대한 액세스를 제공합니다.
exl-id: 986f6031-0edc-4105-aa02-1c22364b3e7c
feature: Catalog Management, Products, Inventory
source-git-commit: 01148770946a236ece2122be5a88b963a0f07d1f
workflow-type: tm+mt
source-wordcount: '259'
ht-degree: 0%

---

# 제품 설정 - [!UICONTROL Sources]

제품 설정의 _[!UICONTROL Sources]_섹션에는 제품을 배포할 수 있는 원본이 나열됩니다. 소스를 지정 및 할당 해제하고 제품의 수량 및 가용성을 관리하는 데 사용됩니다. 이 섹션은 저장소에 대해 둘 이상의 소스가 정의된 경우에만 표시됩니다. 소스에 대한 자세한 내용은 [소스 관리](../inventory-management/sources-manage.md)를 참조하십시오.

## 제품에 대한 소스 할당

1. **[!UICONTROL Assign Source]**&#x200B;을(를) 클릭합니다.

1. 필요한 소스에 대한 확인란을 선택합니다.

1. **[!UICONTROL Done]**&#x200B;을(를) 클릭합니다.

1. **[!UICONTROL Source Item Status]**&#x200B;을(를) 선택하고 필요에 따라 **[!UICONTROL Qty]** 및 **[!UICONTROL Notify Qty]** 값을 입력하십시오.

1. 변경 내용을 저장하려면 **[!UICONTROL Save]**&#x200B;을(를) 클릭합니다.

![소스 보기](./assets/catalog-sources-list.png){width="600" zoomable="yes"}

## 필드 참조

| 필드 | 설명 |
|--- |--- |
| [!UICONTROL Name] | 소스의 고유 이름입니다. |
| [!UICONTROL Source Status] | 카탈로그에서 제품의 활성화 또는 비활성화 여부를 결정합니다. |
| [!UICONTROL Source Item Status] | 제품의 현재 가용성을 결정합니다. 옵션:<br />**[!UICONTROL In Stock]**- 제품을 구매할 수 있도록 설정합니다.<br />**[!UICONTROL Out of Stock]** - 미납주문을 활성화하지 않으면 제품을 구매할 수 없게 하고 카탈로그에서 목록을 제거합니다. |
| [!UICONTROL Qty] | 각 출처에 대한 현재고 금액. |
| [!UICONTROL Notify Qty] | `Notify Quantity Use Default`을(를) 선택하지 않은 경우 이 특정 원본의 _수량에 대한 알림_&#x200B;의 양입니다. |
| [!UICONTROL Notify Qty Use Default] | 제품 Advanced Inventory의 _Notify for Quantity_&#x200B;에 대한 기본 설정 또는 스토어 구성의 글로벌 설정을 사용함을 나타냅니다. 제품의 고급 재고 설정에 대한 자세한 내용은 [고급 제품 옵션 구성](../inventory-management/product-options.md)을 참조하세요. |
| [!UICONTROL Actions] | 할당된 원본의 경우 **[!UICONTROL Unassign]**&#x200B;을(를) 클릭하여 제품에 사용할 수 없는 원본을 만드십시오. 할당되지 않은 원본의 경우 **[!UICONTROL Assign Sources]**&#x200B;을(를) 클릭하여 제품에 사용할 수 있는 원본을 만드십시오. [!UICONTROL Assign Sources] 옵션에 대한 자세한 내용은 [제품당 소스 할당](../inventory-management/sources-assign-per-product.md)을 참조하십시오. |

{style="table-layout:auto"}
