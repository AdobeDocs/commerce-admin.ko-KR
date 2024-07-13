---
title: 고객 속성 속성
description: 고객 속성 속성을 구성하는 방법을 알아봅니다.
exl-id: d464f846-6a1f-43bd-876a-6834605ef794
feature: Customers, Configuration
source-git-commit: 7de285d4cd1e25ec890f1efff9ea7bdf2f0a9144
workflow-type: tm+mt
source-wordcount: '1796'
ht-degree: 0%

---

# 고객 속성 속성

{{ee-feature}}

고객 속성은 주문, 이행 및 고객 관리 프로세스를 지원하는 데 필요한 정보를 제공합니다. 비즈니스가 고유하므로 시스템에서 제공하는 기본 항목 외에 필드가 필요할 수 있습니다. 고객 계정의 계정 정보, 주소록 및 청구 정보 섹션에 사용자 지정 속성을 추가할 수 있습니다. [주소 특성](address-attributes.md)은(는) 체크아웃 중 또는 게스트가 계정을 등록할 때 _청구 정보_ 섹션에서 사용할 수도 있습니다.

![고객 특성](./assets/attributes-customer.png){width="700" zoomable="yes"}

## 1단계: 속성 속성 완료

1. _관리자_ 사이드바에서 **[!UICONTROL Stores]** > _[!UICONTROL Attributes]_>**[!UICONTROL Customer]**(으)로 이동합니다.

1. 오른쪽 상단에서 **[!UICONTROL Add New Attribute]**&#x200B;을(를) 클릭합니다.

   ![고객 특성 속성](./assets/attribute-customer-new.png){width="600" zoomable="yes"}

1. **[!UICONTROL Attribute Properties]** 섹션에서 다음을 수행합니다.

   - 데이터를 입력하는 동안 특성을 식별하는 **[!UICONTROL Default Label]**&#x200B;을(를) 입력하십시오.

   - 시스템 내에서 특성을 식별하는 **[!UICONTROL Attribute Code]**&#x200B;을(를) 입력하십시오.

   속성 코드는 문자로 시작해야 하며 소문자(a-z)와 숫자(0-9)의 조합을 포함할 수 있습니다. 코드는 길이가 30자 미만이어야 하며 특수 문자 또는 공백을 포함할 수 없습니다. 밑줄 문자(`_`)를 사용하여 공백을 나타낼 수 있습니다.

   >[!TIP]
   >
   >**바로 가기:** 필수 필드만 완료하려면 _[!UICONTROL Storefront Properties]_(으)로 스크롤하여_[!UICONTROL Sort Order]_&#x200B;을(를) 입력한 다음 저장하십시오.

1. 데이터 입력 속성을 완료합니다.

   - 데이터 입력에 사용되는 입력 컨트롤의 형식을 확인하려면 **[!UICONTROL Input Type]**&#x200B;을(를) 다음 중 하나로 설정하십시오.

     | 유형 | 설명 |
     |----|-----------|
     | `Text Field` | 한 줄 텍스트 필드. |
     | `Text Area` | 제품 설명과 같은 텍스트 단락을 입력하기 위한 여러 줄 입력 필드입니다. WYSIWYG 편집기를 사용하여 HTML 태그로 텍스트 서식을 지정하거나 텍스트에 태그를 직접 입력할 수 있습니다. |
     | `Multiple Line` | 여러 줄 거리 주소와 유사하게 속성에 대해 여러 텍스트 줄을 만듭니다. 개별 데이터 입력 라인의 수는 2개에서 20개까지 지정할 수 있습니다. 필드의 초기 값을 지정하려면 `Default Value`을(를) 사용하십시오. |
     | `Date` | 선호하는 날짜 형식 및 시간대로 날짜 값을 표시합니다. 날짜 값은 목록 또는 달력(![달력 아이콘](../assets/icon-calendar.png))에서 선택할 수 있습니다. <br/><br/>**_참고:_**시스템 구성에 따라_관리자&#x200B;_사용자는 필드에 날짜를 직접 입력하거나 일정 또는 목록에서 날짜를 선택할 수 있습니다. 날짜 및 시간 값 지정에 대한 자세한 내용은 [날짜 및 시간 옵션](../catalog/attributes-input-types.md#date-and-time-options)을 참조하세요. |
     | `Yes/No` | `Yes` 및 `No`의 사전 정의된 옵션이 있는 드롭다운 목록을 표시합니다. |
     | `Dropdown` | 단일 선택 항목만 허용하는 값의 드롭다운 목록을 표시합니다. 드롭다운 입력 유형은 [구성 가능한 제품](../catalog/product-create-configurable.md)의 주요 구성 요소입니다. |
     | `Multiple Select` | 여러 값을 선택할 수 있는 드롭다운 목록입니다. |
     | `File (attachment)` | 파일을 업로드하고 고객 속성과 첨부 파일로 연결할 수 있는 필드입니다. |
     | `Image File` | 갤러리에 이미지를 업로드하고 고객 속성과 연결할 수 있는 필드입니다. |

   - 고객이 필드에 값을 입력해야 하는 경우 **[!UICONTROL Values Required]**&#x200B;을(를) `Yes`(으)로 설정하십시오.

   - 필드에 초기 값을 할당하려면 **[!UICONTROL Default Value]**&#x200B;을(를) 입력하십시오.

   - 레코드를 저장하기 전에 필드에 입력한 데이터의 정확성을 확인하려면 필드에 사용할 수 있는 데이터 형식으로 **[!UICONTROL Input Validation]**&#x200B;을(를) 설정하십시오. 사용 가능한 값은 지정된 [!UICONTROL Input Type]에 따라 다릅니다.

     | 값 | 설명 |
     |-----|-----------|
     | `None` | 데이터를 입력하는 동안 필드에 입력 유효성 검사가 없습니다. |
     | `Alphanumeric` | 데이터를 입력하는 동안 숫자(0-9)와 영문자(a-z, A-Z)의 조합을 사용할 수 있습니다. 특수 문자를 포함하려면 _HTML 엔터티 이스케이프_&#x200B;를 참조하십시오. |
     | `Alphanumeric with Space` | 데이터를 입력하는 동안 숫자(0-9), 알파벳 문자(a-z, A-Z) 및 공백을 모두 허용합니다. |
     | `Numeric Only` | 데이터를 입력하는 동안 숫자(0-9)만 허용합니다. |
     | `Alpha Only` | 데이터를 입력하는 동안 알파벳 문자(a-z, A-Z)만 허용합니다. |
     | `URL` | 데이터를 입력하는 동안 URL만 허용합니다. |
     | `Email` | 데이터를 입력하는 동안 이메일 주소만 허용합니다. |
     | `Length Only` | 필드에 입력한 데이터의 길이를 기반으로 입력을 확인합니다. |

   - 텍스트 필드 및 텍스트 영역 입력 유형의 크기를 제한하려면 **[!UICONTROL Minimum Text Length]** 및 **[!UICONTROL Maximum Text Length]**&#x200B;을(를) 입력하십시오.

   - 텍스트 필드, 텍스트 영역 또는 여러 줄 입력 형식에 입력한 값에 전처리 필터를 적용하려면 **[!UICONTROL Input/Output Filter]**&#x200B;을(를) 다음 중 하나로 설정합니다.

     | 값 | 설명 |
     |-----|-----------|
     | `None` | 필드에 입력한 텍스트에는 필터를 적용하지 않습니다. |
     | `Strip HTML Tags` | 텍스트에서 HTML 태그를 제거합니다. 이 필터는 HTML 태그가 포함된 다른 소스의 필드에 붙여넣은 데이터를 정리하는 데 도움이 될 수 있습니다. |
     | `Escape  HTML Entities` | 텍스트에 있는 특수 문자를 유효한 HTML 이스케이프 시퀀스(예: `&;`)로 변환합니다. 이스케이프 시퀀스는 앰퍼샌드와 세미콜론 사이에 있으며, 타이포그래퍼의 스마트 따옴표, 저작권 및 상표 기호에 자주 사용됩니다. 이스케이프 시퀀스를 사용하여 보다 작음(`<`) 및 보다 큼(`>`) 기호, 코드에서도 사용되는 앰퍼샌드 문자 등의 문자를 식별합니다. 이 필터는 워드 프로세서에서 데이터베이스 필드에 붙여넣는 특수 문자를 정리하는 데 도움이 될 수 있습니다. |

1. 고객 그리드 및 세그먼트 속성을 완료합니다.

   - Customers 표에 열을 포함하려면 **[!UICONTROL Add to Column Options]**&#x200B;을(를) `Yes`(으)로 설정하십시오.

   - 이 특성으로 Customers 그리드를 필터링하려면 **[!UICONTROL Use in Filter Options]**&#x200B;을(를) `Yes`(으)로 설정합니다.

   - 필터 일치 조건이 다른 텍스트 특성별로 Customers 그리드를 필터링하려면 **[!UICONTROL Grid Filter Condition Type]**&#x200B;을(를) `Partial Match`, `Prefix Match` 또는 `Full Match`(으)로 설정하십시오. 눈금에 대한 _키워드로 검색_ 필드에는 영향을 주지 않습니다.

   - 이 특성으로 고객 그리드를 검색하려면 **[!UICONTROL Use in Search Options]**&#x200B;을(를) `Yes`(으)로 설정합니다.

   - 이 특성을 [고객 세그먼트](customer-segments.md)에서 사용할 수 있도록 하려면 **[!UICONTROL Use in Customer Segment]**&#x200B;을(를) `Yes`(으)로 설정하십시오.

## 2단계: 상점 속성 완료

1. **[!UICONTROL Storefront Properties]** 섹션까지 아래로 스크롤합니다.

   ![고객 특성 - 상점 속성](./assets/attribute-customer-storefront-properties.png){width="600" zoomable="yes"}

1. 특성이 고객에게 표시되도록 하려면 **[!UICONTROL Show on Storefront]**&#x200B;을(를) `Yes`(으)로 설정하십시오.

1. **[!UICONTROL Sort Order]** 필드에 숫자를 입력하여 다른 특성과 함께 나열될 때 나타나는 순서를 결정합니다.

1. 특성을 포함할 각 양식에 **[!UICONTROL Forms to Use]**&#x200B;을(를) 설정합니다. 여러 옵션을 선택하려면 Ctrl 키를 누른 채 각 양식을 클릭합니다.

   - [&#39;고객 등록&#39;](customer-sign-in.md)
   - [&#39;고객 계정 편집&#39;](account-create.md)
   - [&#39;관리자 체크아웃&#39;](../stores-purchase/checkout-process.md)

## 3단계: 레이블 작성 및 저장

1. 왼쪽 패널에서 **[!UICONTROL Manage Labels/Options]**&#x200B;을(를) 선택합니다.

1. **[!UICONTROL Manage Titles]**&#x200B;에서 각 [스토어 보기](../getting-started/websites-stores-views.md)에 대한 특성을 식별하는 레이블을 입력합니다.

1. 완료되면 **[!UICONTROL Save Attribute]**&#x200B;을(를) 클릭합니다.

   ![고객 특성 - 레이블/옵션](./assets/attribute-customer-manage-label-options.png){width="600" zoomable="yes"}

## 필드 설명

### [!UICONTROL Attribute Properties]

| 필드 | 설명 |
|--- |--- |
| [!UICONTROL Default Label] | 관리자 및 상점 첫 화면에서 속성을 식별하는 기본 레이블입니다. |
| [!UICONTROL Attribute Code] | 시스템 내에서 속성을 식별하는 고유 코드입니다. 코드는 길이가 최대 60자이며 공백이나 특수 문자를 포함할 수 없습니다. 공백 대신 밑줄 기호를 사용할 수 있습니다. |
| [!UICONTROL Input Type] | 데이터 입력에 사용되는 입력 컨트롤을 결정합니다. 옵션: <br/>**`Text Field`**- 한 줄 텍스트 필드입니다.<br/>**`Text Area`** - 여러 줄 텍스트 영역입니다. <br/>**`Multiple Line`**- 여러 줄 주소(여러 줄 주소)와 유사하게 특성에 대해 여러 텍스트 줄을 만듭니다. 개별 데이터 입력 라인의 수는 2개에서 20개까지 지정할 수 있습니다.<br/>**`Date`** - 팝업 달력이 있는 날짜 필드를 표시합니다.<br/>**`Dropdown`**- 하나의 값만 선택할 수 있는 드롭다운 목록입니다.<br/>**`Multiple Select`** - 여러 값을 선택할 수 있는 드롭다운 목록입니다. <br/>**`Yes/No`**- `Yes` 또는 `No` 값을 선택할 수 있는 필드입니다.<br/>**`File (attachment)`** - 파일을 업로드하고 고객 특성과 연결할 수 있는 필드입니다. <br/>**`Image File`**- 갤러리에 이미지를 업로드하고 고객 특성과 연결할 수 있는 필드입니다. |
| [!UICONTROL Values Required] | 필드에 값을 입력해야 하는지 여부를 결정합니다. 옵션: `Yes` / `No` |
| [!UICONTROL Default Value] | 특성의 초기 값을 지정합니다. |
| [!UICONTROL Input Validation] | 옵션 선택은 입력 유형에 따라 결정됩니다. 옵션: <br/>**`None`**- 데이터 입력 중에 필드에 입력 유효성 검사가 없습니다.<br/>**`Alphanumeric`** - 데이터를 입력하는 동안 숫자(0-9)와 영문자(a-z, A-Z)의 조합을 사용할 수 있습니다. <br/>**`Alphanumeric with Space`**- 거리 주소의 공백이 통신사의 최대 길이 요구 사항을 준수하도록 허용합니다. 체크아웃 시 고객은 수신자 및 발신자의 거리 주소에 숫자(0-9), 알파벳 문자(a-z, A-Z) 및 공백의 조합을 입력할 수 있습니다. 주소를 저장하면 추가 공백이 트리밍됩니다.<br/>**`Numeric Only`** - 데이터를 입력하는 동안 숫자(0-9)만 허용합니다. <br/>**`Alpha Only`**- 데이터를 입력하는 동안 영문자만 허용합니다(a-z, A-Z).<br/>**`URL`** - 데이터를 입력하는 동안 URL만 허용합니다. <br/>**`Email`**- 데이터를 입력하는 동안 전자 메일 주소만 허용합니다.<br/>**`Length Only`** - 필드에 입력한 데이터의 길이를 기반으로 입력의 유효성을 검사합니다. |
| [!UICONTROL Input/Output Filter] | 레코드가 저장되기 전에 텍스트 필드, 텍스트 영역 또는 여러 줄 입력 유형에 입력된 값에 전처리 필터를 적용합니다. 옵션: <br/>**`None`**- 필드에 입력한 텍스트에 필터를 적용하지 않습니다.<br/>**`Strip HTML Tags`** - 텍스트에서 HTML 태그를 제거합니다. 이 필터는 HTML 태그가 포함된 다른 소스의 필드에 붙여넣은 데이터를 정리하는 데 도움이 될 수 있습니다. <br/>**`Escape HTML Entities`**- 텍스트에 있는 특수 문자를 유효한 HTML 이스케이프 시퀀스(예: `amp;`)로 변환합니다. 이스케이프 시퀀스는 앰퍼샌드와 세미콜론 사이에 있으며, 타이포그래퍼의 스마트 따옴표, 저작권 기호 및 상표 기호에 자주 사용됩니다. 이스케이프 시퀀스를 사용하여 보다 작음(`<`) 및 보다 큼(`>`) 기호, 코드에서도 사용되는 앰퍼샌드 문자 등의 문자를 식별합니다. 이 필터는 워드 프로세서에서 데이터베이스 필드에 붙여넣는 특수 문자를 정리하는 데 도움이 될 수 있습니다. |
| [!UICONTROL Add to Column Options] | 특성이 [Customers](customers-all.md) 표에 열로 포함되는지 여부를 지정합니다. 옵션: `Yes` / `No` |
| [!UICONTROL Use in Filter Options] | 특성이 그리드에서 검색 작업을 위한 필터로 사용될 수 있는지 여부를 지정합니다. 옵션: `Yes` / `No` |
| [!UICONTROL Grid Filter Condition Type] | 표에서 검색 작업을 위한 속성에 대한 필터 일치 조건을 지정합니다. 눈금에 대한 _키워드로 검색_ 필드에는 영향을 주지 않습니다. 옵션: `Partial Match` / `Prefix Match` / `Full Match` |
| [!UICONTROL Use in Search Options] | 속성 값을 검색 작업에서 키워드로 사용할 수 있는지 여부를 지정합니다. 옵션: `Yes` / `No` |
| [!UICONTROL Use in Customer Segment] | 특성이 [고객 세그먼트](customer-segments.md) 조건에 포함되는지 여부를 결정합니다. 옵션: `Yes` / `No` |

### [!UICONTROL Storefront Properties]

| 필드 | 설명 |
|--- |--- |
| [!UICONTROL Show on Storefront] | 속성이 상점 앞의 고객 정보에 필드로 표시되는지 여부를 결정합니다. 옵션: `Yes` / `No` |
| [!UICONTROL Sort Order] | 다른 고객 특성과 관련하여 이 특성의 정렬 순서를 지정합니다. 정렬 순서는 키보드 탐색을 사용할 때 데이터 입력 중에 필드가 포커스를 받는 순서를 결정합니다. |
| [!UICONTROL Forms to Use in] | 속성이 표시되는 데이터 항목 양식이 있는 페이지를 결정합니다. 옵션: <br/>[`Customer Registration`](account-dashboard-account-information.md) <br/>[`Customer Account Edit`](account-create.md) <br/>[`Admin Checkout`](../stores-purchase/checkout-process.md) |

## 기본 고객 속성

| 속성 코드 | 설명 |
| --------------- | ------------------ |
| `created_at` | 고객 계정이 생성된 날짜입니다. |
| `updated_at` | 고객 계정이 마지막으로 업데이트된 날짜. |
| `website_id` | 고객 계정이 생성된 사이트의 웹 사이트 ID. |
| `store_id` | 고객 계정이 생성된 사이트의 스토어 ID입니다. |
| `created_in` | 계정이 생성된 스토어 보기입니다. |
| `group_id` | 고객이 할당된 고객 그룹의 ID입니다. |
| `disable_auto_group_change` | [VAT ID 유효성 검사](../stores-purchase/vat.md#configure-vat-id-validation) 중에 고객 그룹을 동적으로 할당할 수 있는지 여부를 결정합니다. |
| `prefix` | 고객 이름과 함께 사용되는 모든 접두사(예: Mr, Ms. 또는 Dr). |
| `firstname` | 고객의 이름입니다. |
| `middlename` | 고객의 가운데 이름 또는 가운데 이니셜입니다. |
| `lastname` | 고객의 성. |
| `suffix` | 고객 이름과 함께 사용되는 모든 접미사. (예: Jr., Sr. 또는 Esquire) |
| `email` | 고객의 이메일 주소입니다. |
| `dob` | 고객의 생년월일  <br><br>**_중요:_**현재 보안 및 개인 정보 보호 모범 사례를 준수하면서 다른 개인 식별자를 사용한 고객의 전체 생년월일(월, 일, 년) 저장과 관련된 모든 잠재적인 법적 및 보안 위험에 유의하십시오. 고객의 전체 생년월일 보관을 제한하고 고객 생년월일을 대안으로 사용하는 것이 좋습니다. |
| `taxvat` | 고객에게 할당된 부가가치세(VAT) ID입니다. 이 특성의 기본 레이블은 `VAT Number`입니다. VAT 번호 필드는 관리자로부터 볼 때 모든 운송 및 청구 고객 주소에 항상 표시되지만 필수 필드는 아닙니다. |
| `gender` | 고객 성별. |

## 고객 속성 데모

고객 특성 만들기에 대한 시연은 다음 비디오에서 살펴보십시오.

>[!VIDEO](https://video.tv.adobe.com/v/343661?quality=12)
