---
title: 고객 데이터 속성 참조
description: 고객 데이터 가져오기 및 내보내기 작업을 수행할 때 이 고객 데이터 속성 참조를 사용합니다.
exl-id: d22ebfed-f439-4a3f-b39e-e957b65c8c21
feature: Customers, Attributes
source-git-commit: 64ccc2d5016e915a554c2253773bb50f4d33d6f4
workflow-type: tm+mt
source-wordcount: '483'
ht-degree: 0%

---

# 고객 데이터 속성 참조

다음 표에는 고객 주 파일 및 고객 주소의 일반적인 내보내기 속성이 나열되어 있습니다. 이 데이터를 내보내는 데 사용된 설치에는 샘플 데이터가 설치된 두 개의 웹 사이트와 여러 스토어 보기가 있습니다.

각 속성 또는 필드는 CSV 파일에 열로 표시되고 고객 레코드는 행으로 표시됩니다. 밑줄로 시작하는 열은 속성 또는 복잡한 데이터를 포함하는 서비스 엔티티입니다.

## 고객 주 파일

| 속성 | 설명 |
|--- |--- |
| `email` | 고객의 이메일 주소입니다. |
| `_website` |  |
| `_store` |  |
| `confirmation` | 확인 플래그. |
| `created_at` | 고객 계정이 생성된 날짜입니다. |
| `created_in` | 계정이 생성된 스토어 보기입니다. |
| `disable_auto_group_change` | VAT ID 유효성 검사 중에 고객 그룹을 동적으로 지정할 수 있는지 여부를 결정합니다. |
| `dob` | 고객의 생년월일 <br><br>**_중요:_**&#x200B;최신 보안 및 개인 정보 보호 모범 사례를 준수하려면 고객의 전체 생년월일(월, 일, 년)의 저장 및 처리를 검토하십시오. 다른 개인 식별자(예:_전체 이름&#x200B;_)와 함께 수집되는 경우 잠재적인 법적 및 보안상의 위험이 있습니다. 고객의 전체 생년월일 저장을 제한하는 것이 좋으며 대신 고객의 생년월일을 대안으로 사용할 것을 제안합니다. |
| `firstname` | 고객의 이름입니다. |
| `gender` | 고객 성별. |
| `group_id` | 고객이 할당된 고객 그룹의 ID입니다. |
| `lastname` | 고객의 성. |
| `middlename` | 고객의 가운데 이름 또는 가운데 이니셜입니다. |
| `password_hash` | 암호 해시 |
| `prefix` | 고객 이름과 함께 사용되는 모든 접두사(예: `Mr.`, `Ms.`, `Mrs.` 및 `Dr.`). |
| `rp_token` | 암호 재설정 토큰. |
| `rp_token_created_at` | 암호가 재설정된 날짜. |
| `store_id` | 스토어 ID |
| `suffix` | 고객 이름과 함께 사용되는 모든 접미사(예: `Jr.`, `Sr.` 및 `Esquire`). |
| `taxvat` |  |
| `website_id` | 고객 계정이 생성된 사이트의 웹 사이트 ID. |
| `password` | 고객 암호. |

{style="table-layout:auto"}

## 고객 주소

| 속성 | 설명 |
|--- |--- |
| `_website` |  |
| `_email` |  |
| `_entity_id` |  |
| `city` | 고객 주소가 있는 도시입니다. |
| `company` | 해당 주소에 해당하는 경우 회사 이름. |
| `country_id` | 고객 주소가 있는 국가 ID입니다. |
| `fax` | 해당하는 경우 고객의 팩스 번호. |
| `firstname` | 고객의 이름. |
| `lastname` | 고객의 성입니다. |
| `middlename` | 고객의 가운데 이름 또는 가운데 이니셜입니다. |
| `postcode` | 고객 주소가 있는 ZIP 또는 우편 번호입니다. |
| `prefix` | 고객 이름과 함께 사용되는 모든 접두사(예: `Mr.`, `Ms.`, `Mrs.` 및 `Dr.`). |
| `region` | 고객 주소가 있는 지역입니다. |
| `region_id` | 지역 ID |
| `street` | 고객의 거리 주소입니다. 구성에 지정된 경우 상세 주소의 두 번째 줄을 사용할 수 있습니다. |
| `suffix` | 사용하는 경우 고객 이름과 연결된 접미사(예: `Jr.`, `Sr.` 또는 `III`)입니다. |
| `telephone` | 주소와 연결된 고객 전화번호. |
| `vat_id` | VAT ID는 VAT 검증에서 사용할 때 고객의 VAT 번호에 대한 내부 식별자입니다. |
| `vat_is_valid` |  |
| `vat_request_date` |  |
| `vat_request_id` |  |
| `vat_request_success` |  |
| `_address_default_billing_` | 기본 청구 주소를 식별합니다. 값 `1`은(는) 해당 주소가 고객의 기본 청구 주소임을 나타냅니다. 값: 1 / 0 |
| `_address_default_shipping_` | 기본 배송 주소를 식별합니다. 값이 `1`이면 주소가 고객의 기본 배송 주소임을 나타냅니다. 값: `1` / `0` |

{style="table-layout:auto"}
