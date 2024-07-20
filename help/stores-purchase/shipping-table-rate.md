---
title: 테이블 요금 배송
description: 스토어에 대한 테이블 레이트 배송 옵션을 설정하는 방법에 대해 알아보십시오.
exl-id: f73adc9a-4c6c-477d-9553-3a3f28647bdd
feature: Shipping/Delivery
source-git-commit: 0f368e87275a85e3801e6770b8985184e2071384
workflow-type: tm+mt
source-wordcount: '1032'
ht-degree: 3%

---

# 테이블 요금 배송

_테이블 속도_ 배달 방법은 다음을 포함한 조건의 조합을 기준으로 배달 속도를 계산하는 데이터 테이블을 참조합니다.

- 가중치 대 대상
- 가격 대 대상
- 항목 수 대 대상

예를 들어, 창고가 로스앤젤레스에 있다면, 샌디에이고로 배송하는 것이 버몬트로 배송하는 것보다 비용이 덜 듭니다. 테이블 요금 운송을 사용하여 절감액을 고객에게 전달할 수 있습니다.

테이블 비율을 계산하는 데 사용되는 데이터는 스프레드시트에 준비되어 스토어로 가져옵니다. 고객이 견적을 요청하면 결과는 장바구니의 배송 예상 섹션에 표시됩니다.

>[!NOTE]
>
>한 번에 하나의 테이블 속도 데이터 세트만 활성화할 수 있습니다.

![장바구니 주문 요약의 테이블 요금 배송 옵션](./assets/storefront-cart-table-rate.png){width="700" zoomable="yes"}

## 1단계: 기본 설정 완료

첫 번째 단계는 테이블 속도에 대한 기본 설정을 완료하는 것입니다. 구성 범위를 변경하지 않고 이 단계를 완료할 수 있습니다.

1. _관리자_ 사이드바에서 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**(으)로 이동합니다.

1. 왼쪽 패널의 _[!UICONTROL Sales]_섹션에서&#x200B;**[!UICONTROL Delivery Methods]**을(를) 선택합니다.

1. **[!UICONTROL Table Rates]** 섹션에서 ![확장 선택기](../assets/icon-display-expand.png)를 확장합니다.

   >[!NOTE]
   >
   >필요한 경우 먼저 **[!UICONTROL Use system value]** 확인란의 선택을 취소하여 설명된 대로 다음 설정을 변경합니다.

   ![테이블 속도](../configuration-reference/sales/assets/delivery-methods-table-rates.png){width="600" zoomable="yes"}

1. **[!UICONTROL Enabled]**&#x200B;을(를) `Yes`(으)로 설정합니다.

1. 체크아웃하는 동안 테이블 요금 섹션에 표시할 **[!UICONTROL Title]**&#x200B;을(를) 입력하십시오.

   기본 제목은 `Best Way`입니다.

1. 장바구니에서 계산된 비율 옆에 레이블로 표시할 **[!UICONTROL Method Name]**&#x200B;을(를) 입력하십시오.

1. **[!UICONTROL Condition]**&#x200B;을(를) 다음 계산 방법 중 하나로 설정합니다.

   - `Weight v. Destination`
   - `Price v. Destination`
   - `Number of Items v. Destination`

1. 가상 제품을 포함하는 주문의 경우 계산에 가상 제품을 포함하려면 **[!UICONTROL Include Virtual Products in Price Calculation]**&#x200B;을(를) `Yes`(으)로 설정하십시오.

   >[!NOTE]
   >
   >서비스와 같은 가상 제품은 가중치가 없으므로 가중치 대 대상 조건을 기반으로 하는 계산 결과를 변경할 수 없습니다. 그러나 가상 제품은 가격 대 대상 또는 품목 수 대 대상 조건을 기반으로 하는 계산 결과를 변경할 수 있습니다.

1. 요구 사항에 따라 처리 요금 옵션을 구성합니다.

   처리 요금은 선택 사항이며 배송 비용에 추가되는 추가 비용으로 표시됩니다. 처리 수수료를 포함하려면 다음을 수행하십시오.

   - **[!UICONTROL Calculate Handling Fee]** 설정:

      - `Fixed`
      - `Percent`

   - 요금을 계산하는 데 사용된 방법에 따라 **[!UICONTROL Handling Fee]** 요금을 입력하십시오.

     예를 들어, 요금이 고정 요금을 기준으로 하는 경우 `4.90`과(와) 같이 그 금액을 소수점으로 입력하십시오. 단, 취급 수수료가 주문의 백분율을 기준으로 하는 경우 백분율로 금액을 입력합니다. 예를 들어 주문의 6%를 부과하려면 값을 `.06`(으)로 입력하십시오.

1. 필요한 경우 **[!UICONTROL Displayed Error Message]**&#x200B;을(를) 변경합니다.

   이 텍스트 상자는 기본 메시지로 사전 설정되어 있지만 이 전달 방법을 사용할 수 없는 경우 표시할 다른 메시지를 입력할 수 있습니다.

1. **[!UICONTROL Ship to Applicable Countries]** 설정:

   - `All Allowed Countries` - 스토어 구성에 지정된 모든 [국가](../getting-started/store-details.md#country-options)의 고객이 이 게재 방법을 사용할 수 있습니다.
   - `Specific Countries` - 이 옵션을 선택하면 _[!UICONTROL Ship to Specific Countries]_목록이 나타납니다. 목록에서 이 게재 방법을 사용할 수 있는 각 국가를 선택합니다.

1. 테이블 속도를 항상 표시하려면 **[!UICONTROL Show Method if Not Applicable]**&#x200B;을(를) `Yes`(으)로 설정하십시오.

1. **[!UICONTROL Sort Order]**&#x200B;의 경우 체크아웃 중에 다른 배달 방법과 함께 나열할 때 테이블 요금 배송이 표시되는 순서를 결정하는 숫자를 입력합니다.

   `0` = 첫 번째, `1` = 두 번째, `2` = 세 번째 등입니다.

1. **[!UICONTROL Save Config]**&#x200B;을(를) 클릭합니다.

## 2단계: 테이블 비율 데이터 준비

1. 왼쪽 상단 모서리에서 **[!UICONTROL Store View]**&#x200B;을(를) `Main Website` 또는 구성이 적용되는 다른 웹 사이트로 설정합니다.

   >[!NOTE]
   >
   >필요한 경우 먼저 **[!UICONTROL Use system value]** 확인란의 선택을 해제하여 설명된 대로 다음 설정을 변경합니다.

1. 필요에 따라 **[!UICONTROL Condition]**&#x200B;을(를) 변경합니다.

1. **[!UICONTROL Export CSV]**&#x200B;을(를) 클릭합니다.

   ![CSV 내보내기](./assets/shipping-table-rates-export.png){width="700" zoomable="yes"}

1. `tablerates.csv` 파일을 시스템에 저장합니다.

1. 스프레드시트 애플리케이션에서 파일을 엽니다.

1. 운송 계산 조건에 대한 적절한 값으로 테이블을 완료합니다.

   - 모든 범주에서 가능한 모든 값을 나타내는 와일드카드로 별표(*)를 사용합니다.
   - _[!UICONTROL Country]_열에는 각 행에 대해 [올바른 3자 코드][1]가 있어야 합니다.
   - 특정 위치가 목록의 맨 위에 있고 와일드카드 위치가 맨 아래에 있도록 데이터를 _[!UICONTROL Region/State]_(으)로 정렬합니다. 이 방법을 사용하면 먼저 절대값이 있는 규칙을 처리하고 나중에 와일드카드 값을 처리합니다.
   - 우편 번호 범위는 지원되지 않습니다. 영역/상태 내의 모든 코드를 허용하려면 별표(*)를 사용하거나 _[!UICONTROL Zip/Postal Code]_열에서 특정 위치에 대한 단일 코드를 지정합니다.
   - _[!UICONTROL Weight (and above)]_열의 값은 최대 소수 네 자리를 가질 수 있습니다(예: `2.5075`). 데이터에서 소수점 이하 자리 수를 더 많이 사용하면 가져오기가 실패합니다.

   ![가중치와 대상(오스트레일리아)](./assets/table-rates-weight-destination-csv.png){width="500"}

1. `tablerates.csv` 파일을 저장합니다.

## 3단계: 테이블 단가 데이터 가져오기

1. 저장소 구성의 **[!UICONTROL Table Rates]** 섹션으로 돌아갑니다.

1. 왼쪽 상단 모서리에서 이 메서드가 사용되는 웹 사이트에 **[!UICONTROL Store View]**&#x200B;을(를) 설정합니다.

1. **[!UICONTROL Import]**&#x200B;에 대해 **[!UICONTROL Choose File]**&#x200B;을(를) 클릭하고 완료된 `tablerates.csv` 파일을 선택하여 비율을 가져옵니다.

   ![테이블 속도 가져오기](./assets/shipping-table-rates-import.png){width="600" zoomable="yes"}

1. **[!UICONTROL Save Config]**&#x200B;을(를) 클릭합니다.

## 4단계: 요금 확인

테이블 요금 데이터가 정확한지 확인하려면 여러 주소로 결제 프로세스를 진행하여 배송 및 처리 요금이 올바르게 계산되었는지 확인합니다.

### 예제 1: 가격 및 대상

이 예에서는 가격 대 목적지 조건을 사용하여 미국 대륙, 알래스카 및 하와이에 대한 주문 소계 금액을 기준으로 세 가지 다른 배송률 세트를 생성합니다. 별표(*)는 모든 값을 나타내는 와일드카드입니다.

| 국가 | 지역 / 주 | 우편 번호 | 주문 소계(및 이상) | 배송 가격 |
|--- |--- |--- |--- |--- |
| 미국 | 안녕하세요. | * | 100 | 10 |
| 미국 | 안녕하세요. | * | 50 | 15 |
| 미국 | 안녕하세요. | * | 0 | 20 |
| 미국 | AK | * | 100 | 10 |
| 미국 | AK | * | 50 | 15 |
| 미국 | AK | * | 0 | 20 |
| 미국 | * | * | 100 | 5 |
| 미국 | * | * | 50 | 10 |
| 미국 | * | * | 0 | 15 |

{style="table-layout:auto"}

### 예제 2: 무게 및 대상

이 예에서는 가중치 대 목적지 조건을 사용하여 주문의 가중치에 따라 다른 배송율을 생성합니다.

| 국가 | 지역 / 주 | 우편 번호 | 무게(이상) | 배송 가격 |
|--- |--- |--- |--- |--- |
| AUS | NT | * | 9 | 39.95 |
| AUS | NT | * | 0 | 19.95 |
| AUS | VIC | * | 9 | 19.95 |
| AUS | VIC | * | 0 | 5.95 |
| AUS | WA | * | 9 | 39.95 |
| AUS | WA | * | 0 | 19.95 |
| AUS | * | * | 9 | 29.95 |
| AUS | * | * | 0 | 9.95 |

{style="table-layout:auto"}

### 예제 3: 미국 대륙으로 무료 배송 제한

1. 무료 배송을 제공할 모든 상태 대상을 포함하는 `tablerates.csv` 파일을 만듭니다.

1. 다음 설정으로 테이블 속도 구성을 완료합니다.

   | 설정 | 값 |
   |----------|-------|
   | [!UICONTROL Condition] | `Price v. Destination` |
   | [!UICONTROL Method Name] | `Free Shipping` |
   | [!UICONTROL Ship to Applicable Countries] | `Specific Countries` |
   | [!UICONTROL Ship to Specific Countries] | `Select only United States` |
   | [!UICONTROL Show method if not applicable] | `No` |

   {style="table-layout:auto"}

1. 왼쪽 상단 모서리에서 **[!UICONTROL Store View]**&#x200B;을(를) `Main Website` 또는 구성이 적용되는 다른 웹 사이트로 설정합니다.

1. **[!UICONTROL Import]**&#x200B;에 대해 **[!UICONTROL Choose File]**&#x200B;을(를) 클릭하고 완료된 `tablerates.csv` 파일을 선택하여 비율을 가져옵니다.


[1]: https://en.wikipedia.org/wiki/ISO_3166-1_alpha-3
