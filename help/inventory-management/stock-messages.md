---
title: Stock 메시지 시나리오
description: 제품 페이지와 카탈로그 페이지의 제품 목록에서 재고 가용성 메시지를 제어하는 구성 설정의 조합에 대해 알아봅니다.
exl-id: 63114305-e695-445b-91cd-9e0fb2729ec4
feature: Inventory, Configuration
source-git-commit: 4d89212585fa846eb94bf83a640d0358812afbc5
workflow-type: tm+mt
source-wordcount: '342'
ht-degree: 2%

---

# Stock 메시지 시나리오

구성 설정의 조합을 사용하여 제품 페이지와 카탈로그 페이지의 제품 목록에서 재고 가용성 메시지를 제어할 수 있습니다.

![&quot;재고 부족&quot; 메시지가 있는 그룹화된 제품](assets/storefront-out-of-stock-message.png){width="600" zoomable="yes"}

## 제품 페이지 스톡 메시지

재고 관리 및 재고 가용성 설정의 조합에 따라 제품 페이지에서 사용할 수 있는 메시징의 몇 가지 변형이 있습니다.

### 예제 1: 가용성 메시지 표시

#### 시나리오 1

이러한 설정의 조합으로 인해 각 제품의 재고 가용성에 따라 제품 페이지에 가용성 메시지가 표시됩니다.

| 스톡 옵션 | 설정 | 메시지 |
|--|--|--|
| [!UICONTROL Display product availability in stock in the frontend] | `Yes` | |
| [!UICONTROL Manage Stock] | `Yes` | |
| [!UICONTROL Stock Availability] | `In Stock` | _[!UICONTROL Availability: In Stock]_ |
| | `Out of Stock` | _[!UICONTROL Availability: Out of Stock]_ |

#### 시나리오 2

제품에 대한 재고가 관리되지 않는 경우 이 설정 조합을 사용하여 제품 페이지에 가용성 메시지를 표시할 수 있습니다.

| 스톡 옵션 | 설정 | 메시지 |
|--|--|--|
| [!UICONTROL Display product availability in stock in the frontend] | `Yes` |  |
| [!UICONTROL Manage Stock] | `No` | _[!UICONTROL Availability: In Stock]_ |

### 예제 2: 가용성 메시지 숨기기

#### 시나리오 1

이러한 구성 및 제품 설정의 조합은 제품 페이지에 가용성 메시지가 표시되지 않도록 합니다.

| 스톡 옵션 | 설정 | 메시지 |
|--|--|--|
| [!UICONTROL Display product availability in stock in the frontend] | `No` |  |
| [!UICONTROL Manage Stock] | `Yes` |  |
| [!UICONTROL Stock Availability] | `In Stock` | 없음 |
|  | `Out of Stock` | 없음 |

#### 시나리오 2

제품에 대한 재고가 관리되지 않는 경우, 이 구성 및 제품 설정의 조합으로 제품 페이지에 가용성 메시지가 표시되지 않습니다.

| 스톡 옵션 | 설정 | 메시지 |
|--|--|--|
| [!UICONTROL Display product availability in stock in the frontend] | `No` |  |
| [!UICONTROL Manage Stock] | `No` | 없음 |

## 카탈로그 페이지 스톡 메시지

제품 가용성 및 구성 설정에 따라 카테고리 및 검색 결과 목록에 대해 다음과 같은 표시 옵션을 사용할 수 있습니다.

![범주 페이지의 품절 메시지](assets/storefront-out-of-stock-catalog-page.png){width="600" zoomable="yes"}

### 예제 1: &quot;재고 부족&quot; 메시지가 있는 제품 표시

이 구성 설정 조합에는 범주 및 검색 결과 목록에 품절 제품이 포함되며 &quot;품절&quot; 메시지가 표시됩니다.

| 스톡 옵션 | 설정 | 메시지 |
|--|--|--|
| [!UICONTROL Display Out of Stock Products] | `Yes` |  |
| [!UICONTROL Display product availability in stock in the frontend] | `Yes` | _[!UICONTROL Out of stock]_ |
| [!UICONTROL Display Out of Stock Products] | `Yes` |  |
| [!UICONTROL Display product availability in stock in the frontend] | `No` | 없음 |

### 예제 2: &quot;재고 부족&quot; 메시지 없이 제품 표시

이 구성 설정 조합에는 범주 및 검색 결과 목록에 품절 제품이 포함되지만 메시지는 표시되지 않습니다.

| 스톡 옵션 | 설정 | 메시지 |
|--|--|--|
| [!UICONTROL Display Out of Stock Products] | `Yes` | 없음 |
| [!UICONTROL Display product availability in stock in the frontend] | `No` |  |

### 예제 3: 재입고까지 제품 숨기기

이 구성 설정은 재입고될 때까지 카테고리 및 검색 결과 목록에서 완전히 품절 상태를 생략합니다.

| 스톡 옵션 | 설정 | 메시지 |
|--|--|--|
| [!UICONTROL Display Out of Stock Products] | `No` | 없음 |
