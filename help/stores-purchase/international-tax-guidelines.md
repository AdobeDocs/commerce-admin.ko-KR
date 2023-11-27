---
title: 나라별 세금 지침
description: 국가에 따라 권장된 세금 설정을 검토합니다.
exl-id: 027da0a2-0ff4-40a7-9b9c-eefad888bb7a
feature: Taxes
source-git-commit: 8b5af316ab1d2e632ed5fc2066974326830ab3f7
workflow-type: tm+mt
source-wordcount: '1324'
ht-degree: 0%

---

# 나라별 세금 지침

## 미국 세금 구성

이러한 권장 설정은 미국 내의 스토어에 대한 대부분의 세금 구성에 사용할 수 있습니다.

| 세금 옵션 | 추천 |
|--- |--- |
| 카탈로그 가격 로드 | 세금 제외 |
| FPT | 아니요, FPT는 과세되지 않기 때문입니다. |
| 과세 기준 | 배송 원본 |
| 세금 계산 | 합계 |
| 택배? | 아니요 |
| 할인 적용 | 세금 공제 전 |
| 댓글 | 모든 조세 구역은 동일한 우선 순위입니다. 이상적으로 주별 구역과 우편번호 조회를 위한 하나 이상의 구역입니다. |

{style="table-layout:auto"}

### 세금 등급

| 세금 등급 | 권장 설정 |
|--- |--- |
| 운송에 대한 세금 분류 | 없음 |

{style="table-layout:auto"}

### 계산 설정

| 옵션 | 권장 설정 |
|--- |--- |
| [!UICONTROL Tax Calculation Method Based On] | `Total` |
| [!UICONTROL Tax Calculation Based On] | `Shipping Origin` |
| [!UICONTROL Catalog Prices] | `Excluding Tax` |
| [!UICONTROL Shipping Prices] | `Excluding Tax` |
| [!UICONTROL Apply Customer Tax] | `After Discount` |
| [!UICONTROL Apply Discount on Prices] | `Excluding Tax` |

{style="table-layout:auto"}

### 기본 세금 대상 계산

| 옵션 | 권장 설정 |
|--- |--- |
| [!UICONTROL Default Country] | `United States` |
| [!UICONTROL Default State] | 비즈니스가 위치한 주입니다. |
| [!UICONTROL Default Post Code] | 세금 구역에서 사용되는 우편 번호입니다. |

{style="table-layout:auto"}

### 가격 표시 설정

| 옵션 | 권장 설정 |
|--- |--- |
| [!UICONTROL Display Product Prices in Catalog] | `Excluding Tax` |
| [!UICONTROL Display Shipping Prices] | `Excluding Tax` |

{style="table-layout:auto"}

### 장바구니 표시 설정

| 옵션 | 권장 설정 |
|--- |--- |
| [!UICONTROL Display Prices] | `Excluding Tax` |
| [!UICONTROL Display Subtotal] | `Excluding Tax` |
| [!UICONTROL Display Shipping Amount] | `Excluding Tax` |
| [!UICONTROL Display Gift Wrapping Prices] | `Excluding Tax` |
| [!UICONTROL Display Printed Card Prices] | `Excluding Tax` |
| [!UICONTROL Include Tax in Grand Total] | `Yes` |
| [!UICONTROL Display Full Tax Summary] | `Yes` |
| [!UICONTROL Display Zero Tax Subtotal] | `Yes` |

{style="table-layout:auto"}

### 주문, 송장, 대변 메모 및 표시 설정

| 옵션 | 권장 설정 |
|--- |--- |
| [!UICONTROL Display Prices] | `Excluding Tax` |
| [!UICONTROL Display Subtotal] | `Excluding Tax` |
| [!UICONTROL Display Shipping Amount] | `Excluding Tax` |
| [!UICONTROL Include Tax in Grand Total] | `Yes` |
| [!UICONTROL Display Full Tax Summary] | `Yes` |
| [!UICONTROL Display Zero Tax Subtotal] | `Yes` |

{style="table-layout:auto"}

### 고정 제품 세금(FPT)

| 옵션 | 권장 설정 |
|--- |--- |
| [!UICONTROL Enable FPT] | `No`, 캘리포니아 제외. |

{style="table-layout:auto"}

## 영국 세금 구성

이러한 권장 설정은 영국 내의 스토어에 대한 대부분의 세금 구성에 사용할 수 있습니다.

### 영국 B2C 세금 구성

| 세금 옵션 | 추천 |
|--- |--- |
| 카탈로그 가격 로드 | 세금 제외 |
| FPT | 예, FPT 및 설명 포함 |
| 과세 기준 | [!UICONTROL Shipping Address] |
| 세금 계산 | 합계 |
| 택배? | 예 |
| 할인 적용 | 세전, 세금을 포함한 가격 할인. |
| 댓글 | 공급자 송장(VAT 포함)을 표시하는 상인의 경우. |

{style="table-layout:auto"}

### 영국 B2B 세금 구성

| 세금 옵션 | 추천 |
|--- |--- |
| 카탈로그 가격 로드 | 세금 제외 |
| FPT | 예, FPT 및 설명 포함 |
| 과세 기준 | [!UICONTROL Shipping Address] |
| 세금 계산 | 항목에서 |
| 택배? | 예 |
| 할인 적용 | 세전, 세금을 포함한 가격 할인. |
| 댓글 | B2B 상인이 보다 간단한 부가가치세 공급망 고려사항을 제공할 수 있도록 하였다. 행에 대한 세금 계산도 유효합니다. 그러나 과세 관할에 문의하십시오. 설정은 상인이 공급망에 있고, 판매된 재화가 다른 공급업체가 부가 가치세 리베이트 등을 위해 사용된다고 가정합니다. 이러한 정의는 리베이트 발생 속도를 높이기 위한 항목별 조세를 쉽게 식별할 수 있도록 한다. <br/><br/>**_참고:_**일부 관할권에서는 현재 Commerce에서 지원하지 않는 다른 반올림 전략이 필요하며 일부 관할권에서는 품목 또는 행 레벨 세금을 허용하지 않습니다. |

{style="table-layout:auto"}

## 캐나다 세금 구성

>[!IMPORTANT]
>
>GST/PST 주(Montreal)에 있는 판매자는 하나의 세금 규칙을 만들고 결합된 세액을 표시해야 합니다. 질문이 있으시면 자격을 갖춘 세무서에 문의하십시오. 특정 주의 세금 요건에 대한 자세한 내용은 다음을 참조하십시오. [레베누 퀘벡][1], [서스캐처원 정부][2], 및 [공급업체에 대한 매니토바 정보][3]

| 세금 옵션 | 추천 |
|--- |--- |
| 카탈로그 가격 로드 | 세금 제외 |
| FPT | 예, FPT, 설명 및 FPT에 세금 적용. |
| 과세 기준 | 배송 원본 |
| 세금 계산 | 합계 |
| 택배? | 예 |
| 할인 적용 | 세금 공제 전 |

{style="table-layout:auto"}

다음 예제는 두 세율을 계산하고 표시하는 세금 규칙을 사용하여 캐나다의 GST 세율 및 서스캐처원주의 PST 세율을 설정하는 방법을 보여 줍니다. 이 정보는 예제 구성을 간략하게 설명합니다. 세금 관할에 대한 올바른 세율 및 규칙을 확인해야 합니다. 세금을 설정할 때는 적용 가능한 모든 상점 및 웹 사이트에 구성을 적용하도록 상점 범위를 설정합니다.

- 관련 재화에 대한 고정제품세가 제품 속성으로 포함되어 있다.
- 퀘벡에서는 PST를 TVQ라고 합니다. 퀘벡에 대한 요금을 설정하려면 TVQ를 식별자로 사용해야 합니다.

### 1단계: 세금 계산 설정 완료

1. 다음에서 _관리자_ 사이드바, 이동 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. 다중 사이트 구성의 경우 다음을 설정합니다. **[!UICONTROL Store View]** 을(를) 구성 타겟인 웹 사이트 및 스토어에 추가합니다.

1. 왼쪽 패널에서 를 확장합니다. **[!UICONTROL Sales]** 및 선택 **[!UICONTROL Tax]**.

1. 를 클릭하여 페이지의 각 섹션을 확장하고 다음 설정을 완료합니다.

#### 세금 계산 설정

| 필드 | 권장 설정 |
|--- |--- |
| [!UICONTROL Tax Calculation Method Based On] | `Total` |
| [!UICONTROL Tax Calculation Based On] | `Shipping Address` |
| [!UICONTROL Catalog Prices] | `Excluding Tax` |
| [!UICONTROL Shipping Prices] | `Excluding Tax` |
| [!UICONTROL Apply Customer Tax] | `After Discount` |
| [!UICONTROL Apply Discount on Prices] | `Excluding Tax` |
| [!UICONTROL Apply Tax On] | `Custom Price` (가능한 경우) |

{style="table-layout:auto"}

#### 세금 분류

| 필드 | 권장 설정 |
|--- |--- |
| [!UICONTROL Tax Class for Shipping] | `Shipping` (배송에는 세금이 부과됨) |

{style="table-layout:auto"}

#### 기본 세금 대상 계산

| 필드 | 권장 설정 |
|--- |--- |
| [!UICONTROL Default Country] | `Canada` |
| [!UICONTROL Default State] | (적절한 경우) |
| [!UICONTROL Default Postal Code] | `*` (별표) |

{style="table-layout:auto"}

#### 장바구니 표시 설정

| 필드 | 권장 설정 |
|--- |--- |
| [!UICONTROL Include Tax in Grand Total] | `Yes` |
| [!UICONTROL Display Full Tax Summary] | `Yes` |
| [!UICONTROL Display Zero in Tax Subtotal] | `Yes` |

{style="table-layout:auto"}

#### 고정 제품 세금

| 필드 | 권장 설정 |
|--- |--- |
| [!UICONTROL Enable FPT] | `Yes` |
| 모든 FPT 표시 설정 | `Including FPT and FPT description` |
| [!UICONTROL Apply Discounts to FPT] | `No` |
| [!UICONTROL Apply Tax to FPT] | `Yes` |
| [!UICONTROL Include FPT in Subtotal] | `No` |

{style="table-layout:auto"}

### 2단계: 캐나다 상품 및 서비스 세금(GST) 설정

송장 및 기타 판매 문서에 GST 번호를 인쇄하려면 해당 세율 이름에 GST 번호를 포함시킵니다. GST는 주문 요약에 GST 금액의 일부로 나타납니다.

#### 세금 구역 및 세율 관리

| 필드 | 권장 설정 |
|--- |--- |
| [!UICONTROL Tax Identifier] | `Canada-GST` |
| [!UICONTROL Country] | `Canada` |
| [!UICONTROL State] | `*` (별표) |
| [!UICONTROL Zip/Post is Range] | `No` |
| [!UICONTROL Zip/Post Code] | `*` (별표) |
| [!UICONTROL Rate Percent] | `5.0000` |

{style="table-layout:auto"}

### 3단계: 캐나다 지방 판매세(PST) 설정

해당 주에 대해 다른 세율을 설정합니다.

#### 세율 정보

| 필드 | 권장 설정 |
|--- |--- |
| [!UICONTROL Tax Identifier] | `Canada-SK-PST` |
| [!UICONTROL Country] | `Canada` |
| [!UICONTROL State] | `Saskatchewan` |
| [!UICONTROL Zip/Post is Range] | `No` |
| [!UICONTROL Zip/Post Code] | `*` (별표) |
| [!UICONTROL Rate Percent] | `5.0000` |

{style="table-layout:auto"}

### 4단계: GST 세금 규칙 생성

세금을 합산하지 않고 계산된 세금을 GST 및 PST에 대한 개별 라인 항목으로 올바르게 표시하려면 각 규칙에 대해 다른 우선순위를 설정하고 을 선택합니다. **소계만 계산** 확인란. 각 세금은 별도의 라인 항목으로 표시되지만 세액은 복리로 표시되지 않습니다.

#### 세금 규칙 정보

| 필드 | 권장 설정 |
|--- |--- |
| 이름 | `Retail-Canada-GST` |
| [!UICONTROL Customer Tax Class] | `Retail Customer` |
| [!UICONTROL Product Tax Class] | `Taxable GoodsShipping` |
| [!UICONTROL Tax Rate] | `Canada-GST` |
| [!UICONTROL Priority] | `0` |
| [!UICONTROL Calculate off subtotal only] | 이 확인란을 선택합니다. |
| [!UICONTROL Sort Order] | `0` |

{style="table-layout:auto"}

### 단계 5: Saskatchewan에 대한 PST 세금 규칙 만들기

이 세금 규칙의 경우 우선순위를 0으로 설정하고 다음을 선택합니다. **소계만 계산** 확인란. 각 세금은 별도의 라인 항목으로 표시되지만 세액은 복리로 표시되지 않습니다.

#### 세금 규칙 정보

| 필드 | 권장 설정 |
|--- |--- |
| [!UICONTROL Name] | `Retail-Canada-PST` |
| [!UICONTROL Customer Tax Class] | `Retail Customer` |
| [!UICONTROL Product Tax Class] | `Taxable GoodsShipping` |
| [!UICONTROL Tax Rate] | `Canada-SK-PT` |
| [!UICONTROL Priority] | `1` |
| [!UICONTROL Calculate off subtotal only] | 이 확인란을 선택합니다. |
| [!UICONTROL Sort Order] | `0` |

{style="table-layout:auto"}

### 6단계: 결과 저장 및 테스트

1. 완료되면 다음을 클릭하십시오. **[!UICONTROL Save Config]**.

1. 상점으로 돌아가서 샘플 주문을 만들어 결과를 테스트합니다.

## EU 세금 구성

다음 예는 프랑스에 본사를 두고 프랑스에서 100k+ 유로와 독일에서 100k+ 유로를 판매하는 매장을 보여줍니다.

- 세금 계산은 웹 사이트 수준에서 관리됩니다.
- 통화 변환 및 세금 표시 옵션은 저장소 보기 레벨에서 개별적으로 제어됩니다(웹 사이트 사용 체크박스를 선택하여 기본값을 대체하십시오).
- 기본 조세 국가를 설정하면 관할권에 대한 정확한 세금을 동적으로 표시할 수 있습니다.
- 관련 재화에 대한 고정제품세가 제품 속성으로 포함되어 있다.
- 카탈로그가 올바른 카테고리/웹 사이트/스토어 보기에 표시되는지 확인하기 위해 편집해야 할 수 있습니다.

### 1단계: 세 가지 제품 세금 분류 생성

이 예시에서는 부가가치세 경감형 상품세 등급이 여러 개 필요하지 않다고 가정한다.

1. VAT 표준 제품 세금 분류를 생성합니다.

1. VAT 감소 제품 세금 분류를 생성합니다.

1. VAT-Free 제품 세금 분류를 생성합니다.

### 단계 2: 프랑스와 독일에 대한 세율 생성

다음 세율을 생성합니다.

| 세율 | 설정 |
|--- |--- |
| 프랑스-StandardVAT | 국가: 프랑스 <br/>시/도/지역: * <br/>ZIP/우편 번호: * <br/>비율: 20% |
| 프랑스-부가가치세 | 국가: 프랑스 <br/>시/도/지역: * <br/>ZIP/우편 번호: * <br/>비율: 5% |
| 독일-StandardVAT | 국가: 독일 <br/>시/도/지역: * <br/>ZIP/우편 번호: * 요금: 19% |
| 독일 - VAT 절감 | 국가: 독일 <br/>시/도/지역: * <br/>ZIP/우편 번호: * <br/>비율: 7% |

{style="table-layout:auto"}

### 단계 3: 세금 규칙 설정

다음 세금 규칙을 생성합니다.

| 세금 규칙 | 설정 |
|--- |--- |
| 소매-프랑스-StandardVAT | 고객 분류: 소매 고객 <br/>세금 분류: VAT-표준 <br/>세율: 프랑스-표준VAT <br/>우선 순위: 0 <br/>정렬 순서: 0 |
| 소매-프랑스-부가가치세 | 고객 분류: 소매 고객 <br/>세금 분류: VAT 감소 <br/>세율: 프랑스-부가가치세 <br/>우선 순위: 0 <br/>정렬 순서: 0 |
| 소매-독일-StandardVAT | 고객 분류: 소매 고객 <br/>세금 분류: VAT-표준 <br/>세율: 독일-표준VAT <br/>우선 순위: 0 <br/>정렬 순서: 0 |
| 소매-독일-VAT | 고객 분류: 소매 고객 <br/>세금 분류: VAT 감소 <br/>세율: 독일 - VAT <br/>우선 순위: 0 <br/>정렬 순서: 0 |

{style="table-layout:auto"}

### 4단계: 독일에 대한 스토어 뷰 설정

1. 다음에서 _관리자_ 사이드바, 이동 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL All Stores]**.

1. 기본 웹 사이트 아래에 스토어 보기를 만듭니다. **[!UICONTROL Germany]**.

1. 그런 다음 다음을 수행합니다.

   - 다음에서 _관리자_ 사이드바, 이동 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

   - 왼쪽 상단 모서리에서 을(를) 설정합니다. **[!UICONTROL Default Config]** 프랑스 상점에서요.

   - 일반 페이지에서 를 확장합니다. ![확장 선택기](../assets/icon-display-expand.png) 다음 **[!UICONTROL Countries Options]** 섹션 및 기본 국가를 다음으로 설정 `France`.

   - 필요에 따라 로케일 옵션을 완료합니다.

1. 왼쪽 상단 모서리에서 독일어를 선택합니다 **[!UICONTROL Store View]**.

1. 다음에서 _일반_ 페이지, 확장 ![확장 선택기](../assets/icon-display-expand.png) **[!UICONTROL Countries Options]** 기본 국가를 다음으로 설정 `Germany`.

1. 필요에 따라 로케일 옵션을 완료합니다.

### 5단계: 프랑스에 대한 세금 설정 구성

다음 일반 세금 설정을 완료합니다.

| 필드 | 권장 설정 |
|--- |--- |
| [[!UICONTROL Tax Classes]](../configuration-reference/sales/tax.md#tax-classes) |  |
| [!UICONTROL Tax Class for Shipping] | `Shipping` (배송에는 세금이 부과됨) |
| [[!UICONTROL Calculation Settings]](../configuration-reference/sales/tax.md#calculation-settings) |  |
| [!UICONTROL Tax Calculation Method Based On] | `Total` |
| [!UICONTROL Tax Calculation Based On] | `Shipping Address` |
| [!UICONTROL Catalog Prices] | `Including Tax` |
| [!UICONTROL Shipping Prices] | `Including Tax` |
| [!UICONTROL Apply Customer Tax] | `After Discount` |
| [!UICONTROL Apply Discount on Prices] | `Including Tax` |
| [!UICONTROL Apply Tax On] | `Custom Price if available` |
| [[!UICONTROL Default Tax Destination Calculation]](../configuration-reference/sales/tax.md#default-tax-destination-calculation) |  |
| [!UICONTROL Default Country] | `France` |
| [!UICONTROL Default State] |  |
| [!UICONTROL Default Postal Code] | `*` (별표) |
| [[!UICONTROL Fixed Product taxes]](../configuration-reference/sales/tax.md#fixed-product-taxes) |  |
| [!UICONTROL Enable FPT] | `Yes` |
| [!UICONTROL All FPT Display Settings] | `Including FPT and FPT description` |
| [!UICONTROL Apply Discounts to FPT] | `No` |
| [!UICONTROL Apply Tax to FPT] | `Yes` |
| [!UICONTROL Include FPT in Subtotal] | `Yes` |

{style="table-layout:auto"}

### 6단계: 독일에 대한 세금 설정 구성

1. 다음에서 _관리자_ 사이드바, 이동 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. 오른쪽 상단에서 를 설정합니다. **[!UICONTROL Store View]** 독일 상점을 보려면 **[!UICONTROL OK]** 확인할 수 있습니다.

1. 왼쪽 패널에서 를 확장합니다. **[!UICONTROL Sales]** 및 선택 **[!UICONTROL Tax]**.

1. 다음에서 **[!UICONTROL Default Tax Destination Calculation]** 섹션에서 다음을 수행합니다.

   - 지우기 **[!UICONTROL Use Website]** 각 필드 뒤에 있는 확인란,

   - 사이트의 배송 설정을 일치시키려면 [원점](shipping-settings.md#point-of-origin), 다음 값을 업데이트합니다.

      - 기본 국가
      - 기본 상태
      - 기본 게시물 코드

     이 설정을 사용하면 제품 가격에 세금이 포함된 경우 세금이 올바르게 계산됩니다.

     ![기본 세금 대상 계산](./assets/destination-calc-french.png){width="600" zoomable="yes"}

1. 완료되면 다음을 클릭하십시오. **[!UICONTROL Save Config]**.

[1]: https://www.revenuquebec.ca/en/businesses/
[2]: https://www.saskatchewan.ca/finance
[3]: https://www.gov.mb.ca/finance/taxation/bulletins/004.pdf
