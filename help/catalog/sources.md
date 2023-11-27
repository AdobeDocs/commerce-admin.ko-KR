---
title: 제품 설정 - [!UICONTROL Sources]
description: 제품의 경우 [!UICONTROL Sources] 설정은 다음에 대한 액세스를 제공합니다. [!DNL Inventory Management] 제품을 배포할 수 있는 소스.
exl-id: 986f6031-0edc-4105-aa02-1c22364b3e7c
feature: Catalog Management, Products, Inventory
source-git-commit: 01148770946a236ece2122be5a88b963a0f07d1f
workflow-type: tm+mt
source-wordcount: '259'
ht-degree: 1%

---

# 제품 설정 - [!UICONTROL Sources]

다음 _[!UICONTROL Sources]_제품 설정 의 섹션에는 제품을 배포할 수 있는 소스가 나열됩니다. 소스를 지정 및 할당 해제하고 제품의 수량 및 가용성을 관리하는 데 사용됩니다. 이 섹션은 저장소에 대해 둘 이상의 소스가 정의된 경우에만 표시됩니다. 소스에 대한 자세한 내용은 [소스 관리](../inventory-management/sources-manage.md).

## 제품에 대한 소스 할당

1. 클릭 **[!UICONTROL Assign Source]**.

1. 필요한 소스에 대한 확인란을 선택합니다.

1. 클릭 **[!UICONTROL Done]**.

1. 선택 **[!UICONTROL Source Item Status]** 을(를) 입력한 후 **[!UICONTROL Qty]** 및 **[!UICONTROL Notify Qty]** 필요한 값을 지정합니다.

1. 클릭 **[!UICONTROL Save]** 변경 내용을 저장합니다.

![소스 보기](./assets/catalog-sources-list.png){width="600" zoomable="yes"}

## 필드 참조

| 필드 | 설명 |
|--- |--- |
| [!UICONTROL Name] | 소스의 고유 이름입니다. |
| [!UICONTROL Source Status] | 카탈로그에서 제품의 활성화 또는 비활성화 여부를 결정합니다. |
| [!UICONTROL Source Item Status] | 제품의 현재 가용성을 결정합니다. 옵션:<br />**[!UICONTROL In Stock]**- 제품을 구매할 수 있도록 합니다.<br />**[!UICONTROL Out of Stock]** - 미납주문을 활성화하지 않으면 는 제품을 구매할 수 없게 하고 카탈로그에서 목록을 제거합니다. |
| [!UICONTROL Qty] | 각 출처에 대한 현재고 금액. |
| [!UICONTROL Notify Qty] | 다음에 대한 금액 _수량에 대해 알림_ 다음과 같은 경우 이 특정 소스에 대해 `Notify Quantity Use Default` 이(가) 선택되지 않았습니다. |
| [!UICONTROL Notify Qty Use Default] | 의 기본 설정을 사용함을 나타냅니다. _수량에 대해 알림_ 저장소 구성의 Advanced Inventory 또는 global 설정에서. 제품의 고급 재고 설정에 대한 자세한 내용은 [고급 제품 옵션 구성](../inventory-management/product-options.md). |
| [!UICONTROL Actions] | 할당된 소스의 경우 **[!UICONTROL Unassign]** 소스를 제품에 사용할 수 없게 만들기 위해. 할당되지 않은 소스의 경우 **[!UICONTROL Assign Sources]** 소스를 제품에 사용할 수 있도록 합니다. 에 대한 자세한 내용 [!UICONTROL Assign Sources] 옵션, 참조 [제품당 소스 할당](../inventory-management/sources-assign-per-product.md). |

{style="table-layout:auto"}
