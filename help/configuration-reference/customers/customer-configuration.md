---
title: '[!UICONTROL Customers] &gt; [!UICONTROL Customer Configuration]'
description: Commerce 관리자의 [!UICONTROL Customers] &gt; [!UICONTROL Customer Configuration] 페이지에서 구성 설정을 검토하십시오.
exl-id: 596359d7-3891-4e0c-9604-3647032188fd
feature: Configuration, Customers
source-git-commit: 5a4417373f6dc720e8e14f883c27348a475ec255
workflow-type: tm+mt
source-wordcount: '1890'
ht-degree: 0%

---

# [!UICONTROL Customers] > [!UICONTROL Customer Configuration]

{{config}}

## [!UICONTROL Account Sharing Options]

![계정 공유 옵션](./assets/customer-configuration-account-sharing-options.png)<!-- zoom -->

<!-- [Account Sharing Options](https://experienceleague.adobe.com/ko/docs/commerce-admin/customers/customer-accounts/customer-account-scope) -->

| 필드 | [범위](../../getting-started/websites-stores-views.md#scope-settings) | 설명 |
|--- |--- |--- |
| [!UICONTROL Share Customer Accounts] | 글로벌 | 저장소 계층 구조에서 고객 계정의 범위를 결정합니다. 옵션: <br/>**`Global`**- 고객 계정 정보가 모든 웹 사이트 및 Commerce 설치 저장소의 저장소와 공유됩니다.<br/>**`Per Website`** - 고객 계정 정보는 계정을 만든 웹 사이트로 제한됩니다. |

{style="table-layout:auto"}

## [!UICONTROL Online Customers Options]

![온라인 고객 옵션](./assets/customer-configuration-online-customers-options.png)<!-- zoom -->

<!-- [Online Customers Options](https://experienceleague.adobe.com/ko/docs/commerce-admin/customers/customers-menu/now-online) -->

| 필드 | [범위](../../getting-started/websites-stores-views.md#scope-settings) | 설명 |
|--- |--- |--- |
| [!UICONTROL Online Minutes Interval] | 글로벌 | 관리자로부터 고객의 온라인 활동에 액세스할 수 있는 시간을 결정합니다. 기본 간격 15분 동안 비워 둡니다. |
| [!UICONTROL Customer Data Lifetime] | 글로벌 | 고객이 입력한 저장되지 않은 데이터가 만료될 때까지의 시간(분)을 결정합니다. 기본적으로 저장되지 않은 데이터는 60분 후에 만료됩니다. |

{style="table-layout:auto"}

## [!UICONTROL Create New Account Options]

![새 계정 옵션 만들기](./assets/customer-configuration-create-new-account-options.png)<!-- zoom -->

![새 계정 옵션(VAT 필드) 만들기](./assets/customer-configuration-create-new-account-options-vat.png)<!-- zoom -->

<!-- [Create New Account Options (VAT Fields)](https://experienceleague.adobe.com/ko/docs/commerce-admin/customers/customer-accounts/configure/login-landing-page) -->

| 필드 | [범위](../../getting-started/websites-stores-views.md#scope-settings) | 설명 |
|--- |--- |--- |
| [!UICONTROL Enable Automatic Assignment to Customer Group] | 스토어 뷰 | 고객이 기본 고객 그룹에 자동으로 할당되는지 여부를 결정합니다. 스토어에서 VAT 번호를 표시하려면 스토어에서 VAT 번호 표시를 설정하고 `Yes`을(를) 선택합니다. 옵션: <br/>**`Yes`**- 시스템은 고객 VAT ID의 유효성을 자동으로 검사하지 않으며 고객 그룹을 변경하지도 않습니다.<br/>**`No`** - 시스템 동작은 평소와 같으며 기본 고객 그룹은 기본 그룹 필드에서 설정할 수 있습니다. |
| [!UICONTROL Default Group] | 스토어 뷰 | 계정이 생성될 때 지정된 초기 고객 그룹을 식별합니다. |
| [!UICONTROL Default Value for Disable Automatic Group Changes Based on VAT ID] | 글로벌 | (현재 구성 범위가 `Default Group`(으)로 설정된 경우에만 사용할 수 있습니다.) VAT ID를 기반으로 한 고객 그룹의 자동 변경 기능을 기본적으로 사용할 수 있는지 여부를 선택합니다. 이 설정은 제품 수준에서 재정의할 수 있습니다. 이 설정은 다음과 같은 상황에서 시스템 동작에 영향을 줍니다. <br/> - 고객 기본 주소의 VAT ID 또는 전체 기본 주소가 변경됩니다. <br/> - 이전에 저장된 주소가 없는 등록된 고객 또는 체크아웃 중에 등록한 고객에 대해 체크아웃 중에 고객 그룹 변경이 에뮬레이션되었습니다. <br/>자동 그룹 변경이 활성화되면 첫 번째 경우에는 고객 그룹이 자동으로 변경되고 두 번째 경우에는 일시적으로 에뮬레이트된 고객 그룹이 고객에게 할당됩니다. 자동 그룹 변경이 비활성화된 경우 관리자가 수동으로 변경하지 않는 한 할당된 고객 그룹은 변경되지 않습니다. |
| [!UICONTROL Show VAT Number on Storefront] | 웹 사이트 | VAT 번호가 스토어의 고객에게 표시되는지 여부를 결정합니다. 옵션: `Yes` / `No` <br/>은(는) B2B가 아닌 일반 고객 계정에만 영향을 줍니다. 회사 계정에는 별도의 VAT 번호 필드가 있습니다. |
| [!UICONTROL Default Email Domain] | 스토어 뷰 | 스토어의 기본 이메일 도메인을 식별합니다. 예: `mystore.com` |
| [!UICONTROL Default Welcome Email] | 스토어 뷰 | 기본 _시작_ 전자 메일에 사용된 전자 메일 템플릿을 식별합니다. |
| [!UICONTROL Default Welcome Email Without Password] | 스토어 뷰 | 아직 암호가 할당되지 않은 관리자가 만든 새 고객 계정에 사용되는 대체 시작 이메일 템플릿입니다. |
| [!UICONTROL Email Sender] | 스토어 뷰 | 환영 전자 메일의 발신자로 표시되는 스토어 연락처를 식별합니다. |
| [!UICONTROL Require Emails Confirmation] | 웹 사이트 | 계정 만들기 요청에 고객의 확인이 필요한지 여부를 결정합니다. 옵션: `Yes` / `No`. <br/><br/> _&#x200B;**참고:**&#x200B;_ 버전 2.4.7부터 고객은 브라우저에 관계없이 전자 메일 확인 후 계정에 로그인하려면 전자 메일 및 암호를 다시 입력해야 합니다. |
| [!UICONTROL Confirmation Link Email] | 스토어 뷰 | 확인 이메일에 사용되는 이메일 템플릿을 식별합니다. 기본 템플릿: `New account confirmation key` |
| [!UICONTROL Welcome Email] | 스토어 뷰 | 계정이 확인된 후 보내는 환영 메시지에 사용되는 이메일 템플릿을 식별합니다. |
| [!UICONTROL Generate Human-Friendly Customer ID] | 글로벌 | VAT ID 번호를 입력하고 저장하는 데 사용되는 필드가 상점 첫 화면에서 표시되는지 여부를 결정합니다. 옵션: `Yes` / `No` |

{style="table-layout:auto"}

## [!UICONTROL Password Options]

![암호 옵션](./assets/customer-configuration-password-options.png)<!-- zoom -->

<!-- [Password Options](https://experienceleague.adobe.com/ko/docs/commerce-admin/customers/customer-accounts/configure/password-options) -->

| 필드 | [범위](../../getting-started/websites-stores-views.md#scope-settings) | 설명 |
|--- |--- |--- |
| [!UICONTROL Password Reset Protection Type] | 스토어 뷰 | 고객 계정 암호를 재설정하는 데 사용되는 방법을 결정합니다. 옵션: <br/>**`By IP and Email`**- 관리자 계정과 연결된 전자 메일 주소로 전송된 재설정 알림에서 응답을 받은 후 암호를 온라인으로 다시 설정할 수 있습니다.<br/>**`By IP`** - 암호를 온라인으로 다시 설정할 수 있습니다. <br/>**`By Email`**- 관리자 계정과 연결된 전자 메일 주소로 전송되는 전자 메일 알림에 응답하여 암호를 재설정할 수 있습니다.<br/>**`None`** - 암호는 저장소 관리자만 재설정할 수 있습니다. |
| [!UICONTROL Max Number of Password Reset Requests] | 스토어 뷰 | 시간당 암호 재설정 요청 수를 제한합니다. 무제한 요청의 경우 0(0)을 입력합니다. |
| [!UICONTROL Min Time Between Password Reset Requests] | 스토어 뷰 | 암호 재설정 요청 사이의 시간(분)을 결정합니다. 요청 사이에 지연이 없으면 0을 입력합니다. |
| [!UICONTROL Forgot Email Template] | 스토어 뷰 | 고객이 암호를 잊어버렸을 때 사용되는 이메일 템플릿을 식별합니다. 기본 템플릿: `Forgot Password` |
| [!UICONTROL Remind Email Template] | 스토어 뷰 | 고객이 암호 미리 알림 또는 힌트를 받을 때 사용되는 이메일 템플릿을 식별합니다. 기본 템플릿: `Remind Password` |
| [!UICONTROL Reset Password Template] | 스토어 뷰 | 고객이 암호를 재설정할 때 사용할 이메일 템플릿을 결정합니다. |
| [!UICONTROL Password Template Email Sender] | 스토어 뷰 | 암호 관련 전자 메일의 발신자로 표시되는 스토어 연락처를 결정합니다. |
| [!UICONTROL Recovery Link Expiration Period (hours)] | 글로벌 | 암호 복구 링크가 만료될 때까지 걸리는 시간을 지정합니다. |
| [!UICONTROL Enable Autocomplete on login/forgot password forms] | 웹 사이트 | 로그인/암호 찾기 양식에 자동 완성을 사용할지 여부를 결정합니다. 옵션: `Yes` / `No` |
| [!UICONTROL Number of Required Character Classes] | 글로벌 | 암호에 포함해야 하는 서로 다른 문자 클래스(소문자, 대문자, 숫자 및 특수 문자)의 수를 결정합니다. |
| [!UICONTROL Maximum Login Failures to Lockout Account] | 글로벌 | 고객 계정이 잠길 때까지 실패한 로그인 시도 횟수를 결정합니다. 무제한으로 시도하려면 0(`0`)을 입력하십시오. |
| [!UICONTROL Minimum Password Length] | 글로벌 | 암호에 허용되는 최소 문자 수를 결정합니다. 숫자는 0보다 커야 합니다(`0`). |
| [!UICONTROL Lockout Time (minutes)] | 글로벌 | 로그인 시도 실패 횟수가 너무 많으면 고객 계정이 잠기는 시간(분)을 결정합니다. |

{style="table-layout:auto"}

## [!UICONTROL Account Information Options]

![계정 정보 옵션](./assets/customer-configuration-account-info-options.png)<!-- zoom -->

| 필드 | [범위](../../getting-started/websites-stores-views.md#scope-settings) | 설명 |
|--- |--- |--- |
| [!UICONTROL Change Email Template] | 스토어 뷰 | 고객이 이메일 주소를 변경할 때 사용되는 기본 이메일 템플릿을 식별합니다. |
| [!UICONTROL Change Email and Password Template] | 스토어 뷰 | 고객이 이메일 주소와 암호를 변경할 때 사용되는 기본 이메일 템플릿을 식별합니다. |

{style="table-layout:auto"}

## [!UICONTROL Name and Address Options]

### Magento Open Source 옵션

{{ce-feature}}

![이름 및 주소 옵션 - Source 열기](./assets/customer-configuration-name-address-options-ce.png)<!-- zoom -->

<!-- [Name and Address Options - Open Source](https://experienceleague.adobe.com/ko/docs/commerce-admin/customers/customer-accounts/configure/name-address-options) -->

| 필드 | [범위](../../getting-started/websites-stores-views.md#scope-settings) | 설명 |
|--- |--- |--- |
| [!UICONTROL Number of Lines in a Street Address] | 웹 사이트 | 상세 주소의 줄 수를 결정합니다. 상세 주소는 `1`부터 `4`까지 줄로 구성되어 있습니다. 필드가 비어 있으면 3줄(`3`)의 기본 주소 주소가 사용됩니다. |
| [!UICONTROL Show Prefix] | 웹 사이트 | Mr 및 Ms와 같이 고객 이름에 시작 부분에 접두사가 포함되는지 여부를 결정합니다. 옵션: `No` / `Optional` / `Required` |
| [!UICONTROL Prefix Dropdown Options] | 웹 사이트 | 접두사 옵션 목록을 정의합니다. 값을 세미콜론으로 구분합니다. 목록의 맨 위에 빈 값을 표시하려면 첫 번째 값 앞에 세미콜론을 넣습니다. |
| [!UICONTROL Show Middle Name (initial)] | 웹 사이트 | 중간 이니셜이 고객 이름의 일부로 포함되는지 여부를 결정합니다. 가운데 이니셜을 사용하는 경우 선택 필드입니다. 옵션: `Yes` / `No` |
| [!UICONTROL Show Suffix] | 웹 사이트 | 고객 이름에 Jr., Sr., III과 같은 접미사가 끝에 포함되어 있는지 확인합니다. 옵션: `No` / `Optional` / `Required` |
| [!UICONTROL Suffix Dropdown Options] | 웹 사이트 | 접미어 옵션 목록을 정의합니다. 값을 세미콜론으로 구분합니다. 목록의 맨 위에 빈 값을 표시하려면 첫 번째 값 앞에 세미콜론을 넣습니다. |
| [!UICONTROL Show Date of Birth] | 웹 사이트 | 고객의 생년월일이 이름 및 주소 양식에 포함되어 있는지 여부를 결정합니다. 옵션: `No` / `Optional` / `Required` <br><br>**_중요:_**&#x200B;현재 보안 및 개인 정보 보호 모범 사례를 준수하려면 다른 개인 식별자를 사용한 고객의 전체 생년월일(월, 일, 년) 저장과 관련된 모든 잠재적인 법적 및 보안 위험에 유의하십시오. 고객의 전체 생년월일 보관을 제한하고 고객 생년월일을 대안으로 사용하는 것이 좋습니다. |
| [!UICONTROL Show Tax/VAT Number] | 웹 사이트 | 이름 및 주소 양식에 세금 또는 [VAT 번호](../../stores-purchase/vat.md)이(가) 포함되어 있는지 여부를 결정합니다. 옵션: `No` / `Optional` / `Required` |
| [!UICONTROL Show Gender] | 웹 사이트 | 성별이 이름 및 주소 양식에 포함되는지 여부를 결정합니다. 옵션: `No` / `Optional` / `Required` |
| [!UICONTROL Show Telephone] | 웹 사이트 | 고객의 전화 번호가 이름과 주소 양식에 포함되어 있는지 여부를 결정합니다. 옵션: `No` / `Optional` / `Required` |
| [!UICONTROL Show Company] | 웹 사이트 | 고객의 회사가 이름 및 주소 양식에 포함되어 있는지 여부를 결정합니다. 옵션: `No` / `Optional` / `Required` |
| [!UICONTROL Show Fax] | 웹 사이트 | 고객의 팩스 번호가 이름과 주소 양식에 포함되어 있는지 여부를 결정합니다. 옵션: `No` / `Optional` / `Required` |

{style="table-layout:auto"}

### Adobe Commerce 옵션

{{ee-feature}}

![이름 및 주소 옵션 - Commerce](./assets/customer-configuration-name-address-options-ee.png)<!-- zoom -->

<!-- [Name and Address Options - Commerce](https://experienceleague.adobe.com/ko/docs/commerce-admin/customers/customer-accounts/configure/name-address-options) -->

| 필드 | [범위](../../getting-started/websites-stores-views.md#scope-settings) | 설명 |
|--- |--- |--- |
| [!UICONTROL Prefix Dropdown Options] | 웹 사이트 | 접두사 옵션 목록을 정의합니다. 값을 세미콜론으로 구분합니다. 목록의 맨 위에 빈 값을 표시하려면 첫 번째 값 앞에 세미콜론을 넣습니다. |
| [!UICONTROL Suffix Dropdown Options] | 웹 사이트 | 접미어 옵션 목록을 정의합니다. 값을 세미콜론으로 구분합니다. 목록의 맨 위에 빈 값을 표시하려면 첫 번째 값 앞에 세미콜론을 넣습니다. |
| [!UICONTROL Show Telephone] | 웹 사이트 | 고객의 전화 번호가 이름과 주소 양식에 포함되어 있는지 여부를 결정합니다. 옵션: `No` / `Optional` / `Required` |
| [!UICONTROL Show Company] | 웹 사이트 | 고객의 회사가 이름 및 주소 양식에 포함되어 있는지 여부를 결정합니다. 옵션: `No` / `Optional` / `Required` |
| [!UICONTROL Show Fax] | 웹 사이트 | 고객의 팩스 번호가 이름과 주소 양식에 포함되어 있는지 여부를 결정합니다. 옵션: `No` / `Optional` / `Required` |

{style="table-layout:auto"}

## [!UICONTROL Store Credit Options]

{{ee-feature}}

![크레딧 옵션 저장](./assets/customer-configuration-store-credit-options.png)<!-- zoom -->

<!-- [Store Credit Options](https://experienceleague.adobe.com/ko/docs/commerce-admin/customers/customer-accounts/store-credit/credit-configure) -->

| 필드 | [범위](../../getting-started/websites-stores-views.md#scope-settings) | 설명 |
|--- |--- |--- |
| [!UICONTROL Enable Store Credit Functionality] | 글로벌 | 스토어 크레딧이 활성화되어 있는지 여부를 결정합니다. 비활성화하면 고객 계정 및 고객 관리 페이지에서 스토어 크레딧이 제거됩니다. 옵션: `Yes` / `No`. |
| [!UICONTROL Show Store Credit History to Customers] | 웹 사이트 | 고객 계정에 잔액 내역이 표시되는지 여부를 결정합니다. 옵션: `Yes` / `No`. |
| [!UICONTROL Refund Store Credit Automatically] | 글로벌 | 매장 환불 자동 발급 여부를 결정합니다. 옵션: `Yes` / `No` |
| [!UICONTROL Store Credit Update Email Sender] | 스토어 뷰 | 고객에게 전송된 신용 업데이트 알림의 발신자로 표시되는 스토어 ID를 결정합니다. |
| [!UICONTROL Store Credit Update Email Template] | 스토어 뷰 | 크레딧 업데이트에 사용되는 이메일 템플릿을 결정합니다. |

{style="table-layout:auto"}

## [!UICONTROL Login Options]

![로그인 옵션](./assets/customer-configuration-login-options.png)<!-- zoom -->

<!-- [Login Options](https://experienceleague.adobe.com/ko/docs/commerce-admin/customers/customer-accounts/configure/login-landing-page) -->

| 필드 | [범위](../../getting-started/websites-stores-views.md#scope-settings) | 설명 |
|--- |--- |--- |
| [!UICONTROL Redirect Customer to Account Dashboard after Logging in] | 웹 사이트 | 고객이 계정에 로그인한 후 수행할 작업을 결정합니다. 고객을 계정 대시보드로 리디렉션하려면 `Yes`을(를) 선택합니다. 옵션: <br/>**`Yes`**- 고객이 계정에 로그인할 때 계정 대시보드가 나타납니다.<br/>**`No`** - 고객은 계정에 로그인한 후 계속 쇼핑을 할 수 있습니다. |

{style="table-layout:auto"}

## [!UICONTROL Address Templates]

![주소 템플릿](./assets/customer-configuration-address-templates.png)<!-- zoom -->

<!-- [Address Templates](https://experienceleague.adobe.com/ko/docs/commerce-admin/customers/customer-accounts/attributes/address-templates) -->

| 템플릿 | [범위](../../getting-started/websites-stores-views.md#scope-settings) | 설명 |
|--- |--- |--- |
| [!UICONTROL Text] | 스토어 뷰 | 템플릿은 인쇄되는 모든 주소에 사용됩니다. |
| [!UICONTROL Text One Line] | 스토어 뷰 | 이 템플릿은 고객의 장바구니 주소록 목록에 있는 주소 엔티티의 순서를 정의합니다. 체크아웃 진행 중 |
| [!UICONTROL HTML] | 스토어 뷰 | 이 템플릿은 관리 패널([!UICONTROL Customers] > [!UICONTROL Manage Customers])의 _고객 주소_ 영역 아래에 있는 주소 필드의 순서를 정의합니다. 이는 고객이 계정 페이지에서 청구 또는 배송 주소를 만들 때 _새 주소 추가_ 페이지의 사용자에게도 영향을 줍니다. |
| [!UICONTROL PDF] | 스토어 뷰 | 템플릿은 인쇄된 송장, 선적 및 대변 메모에 청구 및 운송 주소 표시를 정의합니다. |

{style="table-layout:auto"}

## [!UICONTROL Customer Segments]

{{ee-feature}}

![고객 세그먼트](./assets/customer-configuration-customer-segments.png)<!-- zoom -->

<!-- [Customer Segments](https://experienceleague.adobe.com/ko/docs/commerce-admin/customers/segments/customer-segments) -->

| 템플릿 | [범위](../../getting-started/websites-stores-views.md#scope-settings) | 설명 |
|--- |--- |--- |
| [!UICONTROL Enable Customer Segment Functionality] | 글로벌 | 고객 세그먼트를 사용하여 타깃팅된 프로모션을 만들 수 있는지 여부를 결정합니다. 옵션: `Yes` / `No` |
| [!UICONTROL Real-time Check if Customer is Matched by Segment] | 글로벌 | 고객 세그먼트의 유효성을 실시간으로 확인할지 여부를 결정합니다. 옵션: <br/>**[!UICONTROL Yes]**- 고객 세그먼트의 유효성을 실시간으로 확인합니다(기본값).<br/>**[!UICONTROL No]** - 고객 세그먼트가 결합된 단일 조건 SQL 쿼리에 의해 확인됩니다. 이렇게 하면 시스템에 고객 세그먼트가 많은 경우 세그먼트 유효성 검사 성능이 향상됩니다. 그러나 분할 데이터베이스나 등록된 고객이 없는 경우에는 유효성 검사가 작동하지 않습니다. |

{style="table-layout:auto"}

## [!UICONTROL CAPTCHA]

![CAPTCHA](./assets/customer-configuration-captcha.png)<!-- zoom -->

<!-- [CAPTCHA](https://experienceleague.adobe.com/ko/docs/commerce-admin/systems/security/captcha/security-captcha) -->

| 필드 | [범위](../../getting-started/websites-stores-views.md#scope-settings) | 설명 |
|--- |--- |--- |
| [!UICONTROL Enable CAPTCHA on Storefront] | 웹 사이트 | Commerce 웹 사이트와 연결된 스토어에서 CAPTCHA를 활성화합니다. 옵션: `Yes` / `No` |
| [!UICONTROL Font] | 웹 사이트 | CAPTCHA를 표시하는 데 사용할 글꼴을 결정합니다. 고유한 글꼴을 추가하려면 글꼴 파일을 Commerce 설치와 동일한 디렉터리에 넣고 `app/code/Magento/Captcha/etc`의 `config.xml` 파일에 선언을 추가합니다. |
| [!UICONTROL Forms] | 웹 사이트 | CAPTCHA가 사용되는 양식을 결정합니다. 옵션: <br />`Applying Coupon Code` <br />`Checkout/Placing Order`<br />`Create user` <br />`Login` <br />`Forgot password` <br />`Contact Us` <br />`Change password` <br />`Share Wishlist Form` <br />`Send to Friend Form` <br />`Payflow Pro`([보안 패치](https://experienceleague.adobe.com/docs/commerce-knowledge-base/kb/troubleshooting/payments/paypal-payflow-pro-active-carding-activity.html?lang=ko) 참조) <br />`Add Gift Card Code` ![Adobe Commerce](../../assets/adobe-logo.svg) <br />`Create company` ![Adobe Commerce](../../assets/adobe-logo.svg) <br /><br />_&#x200B;**참고:**&#x200B;_ 사용자 만들기, 암호 찾기 및 Payflow Pro 양식은 선택 시 항상 활성화됩니다. |
| [!UICONTROL Displaying Mode] | 웹 사이트 | CAPTCHA가 표시되는 시기를 결정합니다. 옵션: <br/>**`Always`**- 로그인하려면 항상 CAPTCHA가 필요합니다.<br/>**`After number of attempts to login`** - 이 옵션은 관리자 로그인 양식에만 적용됩니다. 선택하면 _[!UICONTROL Number of Unsuccessful Attempts to Login]_&#x200B;필드가 나타납니다. 허용할 로그인 시도 횟수를 입력합니다. `0`(영) 값은 [!UICONTROL Displaying Mode]을(를) `Always`(으)로 설정하는 것과 비슷합니다.<br/>_&#x200B;**참고:**&#x200B;_실패한 로그인 시도 횟수를 추적하려면 하나의 전자 메일 주소와 하나의 IP 주소에서 로그인을 시도한 횟수가 계산됩니다. 동일한 IP 주소에서 허용되는 최대 로그인 시도 횟수는 1,000회입니다. 이 제한은 CAPTCHA가 활성화된 경우에만 적용됩니다. |
| [!UICONTROL Number of Unsuccessful Attempts to Login] | 웹 사이트 | 계정이 잠기기 전에 고객이 로그인을 시도할 수 있는 횟수를 지정합니다. |
| [!UICONTROL CAPTCHA Timeout (minutes)] | 웹 사이트 | 현재 CAPTCHA의 수명을 결정합니다. CAPTCHA가 만료되면 사용자는 페이지를 다시 로드해야 합니다. |
| [!UICONTROL Number of Symbols] | 웹 사이트 | CAPTCHA에 나타나는 기호의 수를 최대 8개로 결정합니다. 예를 들어 5-8과 같은 범위를 지정할 수도 있습니다. |
| [!UICONTROL Symbols Used in CAPTCHA] | 웹 사이트 | CAPTCHA에 나타나는 문자(a-z 및 A-Z)와 숫자(0-9)를 결정합니다. `i`, `l` 또는 `1` 등의 다른 기호와 구별하기 어려운 기호는 기본 CAPTCHA 기호 집합에 포함되지 않습니다. |
| [!UICONTROL Case Sensitive] | 웹 사이트 | CAPTCHA 문자가 대/소문자를 구분하는지 여부를 결정합니다. 옵션: `Yes` / `No` |

{style="table-layout:auto"}
