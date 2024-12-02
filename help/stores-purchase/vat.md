---
title: 부가가치세(VAT)
description: 설명 추가&gt;
exl-id: 20dbcb86-e558-47f2-968d-b5c9ec5f665b
feature: Taxes
source-git-commit: 8b5af316ab1d2e632ed5fc2066974326830ab3f7
workflow-type: tm+mt
source-wordcount: '1990'
ht-degree: 0%

---

# 부가가치세(VAT)

일부 국가에서는 재화와 용역에 대해 부가가치세 또는 부가가치세를 부과하고 있다. 고객에게 판매하는 제조 또는 유통 과정, 재료 또는 서비스의 단계에 따라 부가가치세 세율이 다를 수 있습니다. 납부세액을 정확하게 계산하기 위해 둘 이상의 VAT 세율을 적용할 수 있습니다.

Commerce은 둘 다 동일한 국가에 있는 경우 판매자 또는 고객 주소를 기준으로 부가가치세를 부과하도록 구성할 수 있습니다. 일반적으로 VAT 계산은 원산지가 아니라 선적 목적지를 기준으로 합니다. 대부분의 시나리오에서는 고객 배송 주소를 기반으로 VAT를 계산하는 구성 설정으로 충분합니다.

## 예제 시나리오

- 한 EU국가에서 다른 EU국가의 개인에게 재화를 공급하는 부가가치세 등록사업자에 대해서는 상인의 소재지를 기준으로 하여 &#39;원거리 판매&#39;로 부가가치세를 계산한다.

- 영국 주소로 배송하는 영국 상점에서 구매하는 네덜란드의 한 사업체는 영국 VAT 세율을 지불해야 합니다.

- [다운로드 가능한 제품](../catalog/product-create-downloadable.md) 또는 _디지털 상품_ 판매의 경우 VAT 세율은 판매자 위치가 아닌 배송지를 기준으로 합니다. [디지털 제품의 공급 장소](taxes.md#place-of-supply-for-digital-goods-eu)를 참조하세요.

>[!TIP]
>
>일부 국가 간 및 B2B 선적분은 더 복잡한 세금 요구 사항을 가지고 있습니다. Commerce 설치의 기본 기능을 확장하려면 [Marketplace](https://marketplace.magento.com/extensions/accounting-finance/taxes.html)에서 세금 관리 솔루션을 추가하는 것이 좋습니다.

## VAT 구성

다음 지침에는 소매 고객에 대한 판매를 위해 영국에서 20% VAT를 설정하는 샘플 절차가 포함되어 있습니다. 기타 세율 및 국가의 경우 일반 절차를 따르되 국가, VAT 세율, 고객 유형 등에 해당하는 특정 정보를 입력합니다.

>[!NOTE]
>
>진행하기 전에 해당 지역의 부가가치세에 적용되는 규칙과 규정을 확인하십시오.

일정한 기업 간 거래에서는 부가가치세를 과세하지 않는다. Commerce은 고객의 VAT ID를 확인하여 VAT가 제대로 평가(또는 평가 안 됨)되었는지 확인할 수 있습니다. [VAT ID 유효성 검사](#vat-id-validation)를 참조하십시오.

### 1단계: 고객 세금 분류 설정

세금 규칙을 만드는 프로세스는 세율을 추가하는 것으로 시작됩니다.

1. _관리자_ 사이드바에서 **[!UICONTROL Stores]** > _[!UICONTROL Taxes]_>**[!UICONTROL Tax Zones and Rates]**(으)로 이동합니다.

   ![고객 세금 클래스 설정](./assets/vat-zones.png){width="600" zoomable="yes"}

1. VAT와 함께 사용하기에 적합한 고객 세금 분류가 있는지 확인합니다.

   이 예제의 경우 _소매 고객_(이)라는 고객 세금 클래스가 있는지 확인하십시오. 이 세금 클래스가 없으면 **[!UICONTROL Add New Tax Rate]**&#x200B;을(를) 클릭하십시오.

1. 새 세금 클래스의 **[!UICONTROL Tax Identifier]**&#x200B;을(를) 입력하십시오.

   세금 규칙을 만들 때 _세금 규칙 정보_&#x200B;의 _세율_ 필드에 모든 세율이 표시됩니다.

1. 우편 번호 범위(부터/까지)를 설정하려면 **[!UICONTROL Zip/Post is Range]** 확인란을 선택하십시오.

1. 세율이 적용되는 **[!UICONTROL Country]**&#x200B;을(를) 선택합니다.

1. 구매 시 세율 계산에 사용할 **[!UICONTROL Rate Percent]**&#x200B;을(를) 입력하십시오.

1. 완료되면 **[!UICONTROL Save Rate]**&#x200B;을(를) 클릭합니다.

제출된 세율을 기반으로 후속 세금 규칙을 생성할 수 있습니다. 세율이 없는 상황에서 세칙의 신설은 불가능해진다.

### 단계 2: 제품 세금 분류 설정

1. _관리자_ 사이드바에서 **[!UICONTROL Stores]** > _[!UICONTROL Taxes]_>**[!UICONTROL Tax Rules]**(으)로 이동합니다.

1. **[!UICONTROL Add New Tax Rule]**&#x200B;을(를) 클릭합니다.

1. **[!UICONTROL Additional Settings]** 섹션에서 ![확장 선택기](../assets/icon-display-expand.png)를 확장합니다.

   ![제품 세금 클래스 설정](./assets/tax-class-additional-settings.png){width="600" zoomable="yes"}

1. _제품 세금 클래스_&#x200B;에서 **[!UICONTROL Add New Tax Class]**&#x200B;을(를) 클릭합니다.

1. 사용 가능한 제품 세금 클래스 목록에 새 클래스를 추가하고 세 개의 새 클래스를 만들려면 새 세금 클래스의 **[!UICONTROL Name]**&#x200B;을(를) 입력하고 확인 표시를 클릭합니다.

   - `VAT Standard`
   - `VAT Reduced`
   - `VAT Zero`

1. 추가하는 각 새 클래스에 대해 **[!UICONTROL Save Class]**&#x200B;을(를) 클릭합니다.

1. **[!UICONTROL Save Rule]**&#x200B;을(를) 클릭합니다.

### 단계 3: 세금 구역 및 세율 설정

1. _관리자_ 사이드바에서 **[!UICONTROL Stores]** > _[!UICONTROL Taxes]_>**[!UICONTROL Tax Zones and Rates]**(으)로 이동합니다.

   이 예에서는 미국 세율을 제거하거나 그대로 둘 수 있습니다.

1. **[!UICONTROL Add New Tax Rate]**&#x200B;을(를) 클릭합니다.

   ![세금 구역 및 세율 설정](./assets/tax-rate-create-new.png){width="600" zoomable="yes"}

1. 다음과 같이 신규 비율을 정의합니다.

   **VAT 표준**

   - 세금 식별자: `VAT Standard`
   - 국가 및 주: `United Kingdom`
   - 비율: `20.00`

   **VAT 감소**

   - 세금 식별자: `VAT Reduced`
   - 국가 및 주: `United Kingdom`
   - 비율: `5.00`

1. 각 비율에 대해 **[!UICONTROL Save Rate]**&#x200B;을(를) 클릭합니다.

### 단계 4: 세금 규칙 설정

세금 규칙은 고객 세금 분류, 제품 세금 분류 및 세율을 조합한 것입니다.

1. _관리자_ 사이드바에서 **[!UICONTROL Stores]** > _[!UICONTROL Taxes]_>**[!UICONTROL Tax Rules]**(으)로 이동합니다.

1. 다음과 같이 새 세금 규칙을 추가합니다.

   **VAT 표준**

   - 이름: `VAT Standard`
   - 고객 세금 클래스: `Retail Customer`
   - 제품 세금 클래스: `VAT Standard`
   - 세율: `VAT Standard Rate`

   **Vat 감소**

   - 이름: `VAT Reduced`
   - 고객 세금 클래스: `Retail Customer`
   - 제품 세금 클래스: `VAT Reduced`
   - 세율: `VAT Reduced Rate`

1. 각 비율에 대해 **[!UICONTROL Save Rule]**&#x200B;을(를) 클릭합니다.

### 5단계: 제품에 세금 분류 적용

1. _관리자_ 사이드바에서 **[!UICONTROL Catalog]** > **[!UICONTROL Manage Products]**(으)로 이동합니다.

1. 편집 모드로 카탈로그의 제품을 엽니다.

1. _일반_ 페이지에서 **[!UICONTROL Tax Class]** 옵션을 찾아 제품에 적용되는 **[!UICONTROL VAT Class]**&#x200B;을(를) 선택합니다.

1. 완료되면 **[!UICONTROL Save]**&#x200B;을(를) 클릭합니다.

   ![제품에 세금 클래스 적용](./assets/vat-apply-classes.png){width="600" zoomable="yes"}

## 필드 설명

### 정보 저장

Commerce은 다음 [스토어 정보 구성 설정](../configuration-reference/general/general.md#store-information)을 사용하여 판매자 정보를 기반으로 VAT를 계산합니다.

**[!UICONTROL VAT Number]** - 판매자에게 할당된 부가가치세 번호.

**[!UICONTROL Validate VAT Number]** - [VAT 유효성 검사](#vat-id-validation)에서 VAT 번호가 [유럽 위원회](https://ec.europa.eu/taxation_customs/vies/) 데이터베이스의 해당 레코드와 일치하는지 확인합니다.

### 고객 정보

Commerce은 다음 필드를 사용하여 [고객 정보](../customers/account-dashboard-account-information.md))를 기반으로 VAT를 계산합니다.

#### 계정 정보

**[!UICONTROL Tax/VAT Number]** - 해당되는 경우 고객에게 할당된 세금 번호 또는 부가가치세 번호.

#### 주소

**[!UICONTROL VAT Number]** - 해당되는 경우 고객의 특정 청구 또는 배송 주소와 연결된 부가가치세 번호. EU 내에서 [디지털 상품](taxes.md#place-of-supply-for-digital-goods-eu)) 판매의 경우 부가가치세 금액은 배송지를 기준으로 합니다.

### 고객 계정

Commerce은 다음 [고객 구성 설정](../customers/account-options-new.md)을 사용하여 VAT를 계산합니다.

**[!UICONTROL Show VAT Number on Storefront]** - 고객 계정에서 사용할 수 있는 주소록에 고객 VAT 번호 필드가 포함되어 있는지 여부를 결정합니다.

**[!UICONTROL Default Value for Disable Automatic Group Changes Based on VAT ID]** - VAT ID는 VAT 유효성 검사에 사용되는 고객의 VAT 번호에 대한 내부 식별자입니다. VAT를 확인하는 동안 Commerce은 해당 숫자가 [유럽 위원회](https://ec.europa.eu/taxation_customs/vies/) 데이터베이스와 일치하는지 확인합니다. 고객은 유효성 검사 결과에 따라 4개의 기본 고객 그룹 중 하나에 자동으로 할당할 수 있습니다.

## VAT ID 유효성 검사

_VAT ID 유효성 검사_&#x200B;는 판매자 및 고객 로케일을 기반으로 유럽 연합(EU) 내에서 발생하는 B2B 거래에 필요한 세금을 자동으로 계산합니다. Commerce은 [유럽 위원회][1] 서버의 웹 서비스를 사용하여 VAT ID 유효성 검사를 수행합니다.

>[!NOTE]
>
>부가가치세 관련 세칙은 다른 세칙에 영향을 주지 않으며, 다른 세칙의 적용을 막지 않는다. 주어진 시간에 하나의 세법만을 적용할 수 있다.

- 판매자와 고객이 동일한 EU 국가에 있는 경우 부가가치세가 부과된다.
- 가맹점과 고객이 서로 다른 EU 국가에 있고, 양 당사자가 모두 EU 등록 사업자인 경우에는 부가가치세가 부과되지 않는다.

스토어 관리자는 계정 생성, 주소 생성 또는 업데이트, 체크아웃 중에 고객에게 자동으로 할당할 수 있는 기본 고객 그룹을 두 개 이상 만듭니다. 그 결과, 다른 세법규정이 자국 내(국내)와 EU 역내 판매에 활용된다.

>[!IMPORTANT]
>
>운송이 필요하지 않은 가상 또는 다운로드 가능한 제품을 판매하는 경우, 고객의 위치 국가의 부가 가치세 비율을 조합 내 판매와 국내 판매 모두에 사용해야 합니다. 가상 제품에 해당하는 제품 세금 분류에 대한 추가 개별 세금 규칙을 생성합니다.

### 고객 등록 워크플로우

VAT ID 유효성 검사가 활성화된 경우 등록 후 각 고객은 VAT ID 번호를 입력할 것을 제안합니다. 단, VAT 등록 고객인 쇼핑객만 이 필드를 채울 것으로 예상됩니다.

고객이 VAT 번호 및 기타 주소 필드를 지정하고 저장을 선택하면 시스템이 주소를 저장하고 VAT ID 유효성 검사 요청을 유럽 위원회 서버로 전송합니다. 검증 결과에 따라 기본 그룹 중 하나가 고객에게 지정됩니다. 고객 또는 관리자가 기본 주소의 VAT ID를 변경하거나 전체 기본 주소를 변경하는 경우 이 그룹을 변경할 수 있습니다. 경우에 따라 한 페이지 체크아웃 중에 그룹을 일시적으로 변경할 수 있습니다(그룹 변경이 에뮬레이트됨).

활성화된 경우 _[!UICONTROL Customer Information]_페이지에서 확인란을 선택하여 개별 고객에 대한 VAT ID 유효성 검사를 재정의할 수 있습니다.

### 체크아웃 워크플로우

체크아웃 중에 고객의 VAT 검증을 수행하면 VAT 요청 식별자 및 VAT 요청 일자가 주문의 주석 내역 섹션에 저장됩니다.

체크아웃 중 VAT ID 유효성 검사와 고객 그룹 변경과 관련된 시스템 동작은 각 트랜잭션에 대한 유효성 검사 및 자동 그룹 변경 비활성화 설정을 구성하는 방법에 따라 다릅니다. 이 섹션에서는 프론트엔드의 체크아웃에 대한 VAT ID 유효성 검사 기능의 구현에 대해 설명합니다.

고객이 Google Express 체크아웃, PayPal Express 체크아웃 또는 다른 외부 체크아웃 방법을 사용하는 경우 외부 결제 게이트웨이에서 체크아웃이 완전히 수행됩니다. 이 시나리오에서는 체크아웃 중에 _각 트랜잭션에 대한 유효성 검사_ 설정을 적용할 수 없으며 고객 그룹을 변경할 수 없습니다.

![VAT 유효성 검사 체크 아웃 워크플로](./assets/vat-id-validation2.png){width="550" zoomable="yes"}

### VAT ID 유효성 검사 구성

VAT ID 검증을 구성하려면 먼저 필요한 고객 그룹을 설정하고 관련 세금 분류, 세율 및 규칙을 생성해야 합니다. 그런 다음 저장소에 대해 VAT ID 유효성 검사를 활성화하고 구성을 완료합니다.

다음 예는 VAT ID 검증에 세금 분류 및 세율을 사용하는 방법을 보여줍니다. 예를 검토한 다음 스토어에 필요한 세금 분류 및 규칙을 설정하는 지침을 따릅니다.

#### 예: VAT ID 검증에 필요한 최소 세금 규칙

| 세금 규칙 #1 |  |
|--- |--- |
| 고객 세금 분류 | 고객 세금 클래스에 <br />국내 고객을 위한 클래스가 포함되어야 합니다. <br />VAT ID의 형식이 잘못된 고객을 위한 클래스입니다.<br />VAT ID를 확인하지 못한 고객의 클래스입니다. |
| 제품 세금 분류 | 제품 과세 등급에는 번들 및 가상을 제외한 모든 유형의 제품에 대한 등급이 포함되어야 합니다. |
| 세율 | 세율에는 상인의 국가에 대한 부가가치세 세율이 포함되어야 한다. |

{style="table-layout:auto"}

| 세금 규칙 #2 |   |
|--- |--- |
| 고객 세금 분류 | 노조내 고객을 위한 클래스. |
| 제품 세금 분류 | 가상을 제외한 모든 유형의 제품에 대한 클래스입니다. |
| 세율 | 상인의 국가를 제외한 모든 EU 국가의 부가가치세 세율. 현재 이 비율은 0%입니다. |

{style="table-layout:auto"}

| 세금 규칙 #3 | (가상 및 다운로드 가능한 제품에 필요) |
|--- |--- |
| 고객 세금 분류 | 고객 세금 클래스에는 다음이 포함되어야 합니다. <br/>국내 고객을 위한 클래스 <br/>VAT ID가 잘못된 고객을 위한 클래스 VAT ID 유효성 검사에 실패한 고객을 위한 클래스 |
| 제품 세금 분류 | 가상 제품에 대한 클래스입니다. |
| 세율 | 판매자의 국가에 대한 VAT 비율. |

{style="table-layout:auto"}

| 세금 규칙 #4 | (가상 및 다운로드 가능한 제품에 필요) |
|--- |--- |
| 고객 세금 분류 | 노조내 고객을 위한 클래스. |
| 제품 세금 분류 | 가상 제품에 대한 클래스입니다. |
| 세율 | 상인의 국가를 제외한 모든 EU 국가의 부가가치세 세율. 현재 이 비율은 0%입니다. |

{style="table-layout:auto"}

#### 1단계: VAT 관련 고객 그룹 생성

VAT ID 검증은 VAT ID 검증 결과에 따라 4개의 기본 고객 그룹 중 하나를 고객에게 자동으로 할당합니다.

- 국내
- 유럽 연합 내
- 잘못된 VAT ID
- 유효성 검사 오류

VAT ID 검증을 위해 고객 그룹을 생성하거나 비즈니스 논리를 준수하는 경우 기존 그룹을 사용할 수 있습니다. VAT ID 검증을 구성할 때 적절한 VAT ID 검증 결과가 있는 고객에 대해 생성된 각 고객 그룹을 기본값으로 할당해야 합니다.

#### 2단계: VAT 관련 분류, 세율 및 규칙 생성

각 세금 규칙은 다음 세 가지 엔티티로 정의됩니다.

- 고객 세금 분류
- 제품 세금 분류
- 세율

VAT ID 유효성 검사를 효과적으로 사용하기 위해 [세금 규칙](tax-rules.md)을(를) 만듭니다.

- 세금 규칙에는 세율 및 [세금 등급](tax-class.md)이 포함됩니다.
- 세금 클래스는 [고객 그룹](../customers/customer-groups.md)에 할당됩니다.

#### 3단계: VAT ID 유효성 검사 활성화 및 구성

1. _관리자_ 사이드바에서 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**(으)로 이동합니다.

1. 필요한 경우 구성에 대해 **[!UICONTROL Store View]**&#x200B;을(를) 설정합니다.

1. 왼쪽 패널에서 **[!UICONTROL Customers]**&#x200B;을(를) 확장하고 **[!UICONTROL Customer Configuration]**&#x200B;을(를) 선택합니다.

1. **[!UICONTROL Create New Account Options]** 섹션에서 ![확장 선택기](../assets/icon-display-expand.png)를 확장합니다.

   다음 예에서는 VAT 검증과 관련이 없는 일반 고객 설정이 어둡습니다.

   ![새 계정 옵션 만들기](../configuration-reference/customers/assets/customer-configuration-create-new-account-options-vat.png){width="600" zoomable="yes"}

1. **[!UICONTROL Enable Automatic Assignment to Customer Group]**&#x200B;을(를) `Yes`(으)로 설정하고 필요에 따라 다음 필드를 완료합니다.

   - **[!UICONTROL Default Group]**
   - **[!UICONTROL Default Value for Disable Automatic Group Changes Based on VAT ID]**
   - **[!UICONTROL Show VAT Number on Storefront]**

1. 완료되면 **[!UICONTROL Save Config]**&#x200B;을(를) 클릭합니다.

#### 4단계: VAT ID 및 위치 국가 설정

1. 왼쪽 패널에서 **[!UICONTROL General]**&#x200B;을(를) 확장하고 아래의 **[!UICONTROL General]**&#x200B;을(를) 선택합니다.

1. **[!UICONTROL Store Information]** 섹션에서 ![확장 선택기](../assets/icon-display-expand.png)를 확장합니다.

   ![정보 저장](../configuration-reference/general/assets/general-store-information.png){width="600" zoomable="yes"}

1. **[!UICONTROL Country]**&#x200B;을(를) 선택합니다.

1. **[!UICONTROL VAT Number]**&#x200B;을(를) 입력하고 **[!UICONTROL Validate VAT Number]**&#x200B;을(를) 클릭합니다.

   결과가 즉시 나타납니다.

1. 완료되면 **[!UICONTROL Save Config]**&#x200B;을(를) 클릭합니다.

#### 5단계: EU 회원국 목록 확인

1. _일반_ 구성 페이지에서 계속 **[!UICONTROL Countries Options]** 섹션에서 ![확장 선택기](../assets/icon-display-expand.png)를 확장합니다.

   ![국가 옵션](../configuration-reference/general/assets/general-country-options.png){width="600" zoomable="yes"}

1. **[!UICONTROL European Union Countries]** 목록에서 EU의 각 회원국이 선택되었는지 확인합니다.

   기본 설정을 변경하려면 **시스템 값 사용** 확인란의 선택을 취소하십시오. Ctrl 키(PC) 또는 Command 키(Mac)를 누른 채로 추가하거나 제거할 각 국가를 클릭합니다.

1. 완료되면 **[!UICONTROL Save Config]**&#x200B;을(를) 클릭합니다.


[1]: https://ec.europa.eu/taxation_customs/vies/
