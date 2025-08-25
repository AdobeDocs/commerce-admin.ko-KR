---
title: 회사 계정 만들기
description: Adobe Commerce 관리 및 상점 첫 화면에서 회사 계정 만들기에 대해 알아봅니다.
exl-id: 8c06395b-102b-4a41-8eb3-e6a344feac70
feature: B2B, Companies, Configuration, Storefront
role: Admin, User
source-git-commit: 2e119bcb8278432bde1c12f3f44a112cde59fb18
workflow-type: tm+mt
source-wordcount: '2444'
ht-degree: 0%

---

# 회사 계정 만들기

회사 계정을 사용하면 B2B 기업이 Adobe Commerce 내에서 구매, 사용자 및 크레딧을 관리할 수 있습니다. 이 주제에서는 회사 계정을 만들고, 구성하고, 활성화하는 전체 프로세스를 다룹니다.

## 회사 계정 생성 개요

각기 다른 비즈니스 시나리오에 적합한 두 가지 방법을 통해 회사 계정을 만들 수 있습니다.

* **Storefront 등록**—기업의 셀프서비스 계정 요청
* **관리자 만들기**—사전 구성된 세부 정보를 사용하여 판매 지원 계정 설정

모든 회사 계정은 활성화되기 전에 관리자 승인이 필요하므로 적절한 검사 및 구성이 보장됩니다.

## 사전 요구 사항

회사 계정을 만들기 전에 다음 요구 사항이 충족되었는지 확인하십시오.

* **시스템 요구 사항:**
   * Adobe Commerce 설치 시 [B2B 기능이 활성화됨](enable-basic-features.md)
   * 상점 만들기에 회사 등록을 사용할 수 있습니다.
   * 전자 메일 알림이 승인 워크플로우에 대해 구성되어 있습니다.

* **비즈니스 요구 사항:**
   * 승인 프로세스 및 정책 수립
   * 영업 담당자가 할당됩니다(관리자 생성 계정의 경우).
   * 신용 정책이 정의됩니다(회사 신용을 사용하는 경우).
   * 고객 그룹 및 공유 카탈로그가 구성됨

* **관리 액세스:**
   * 회사 관리에 적절한 권한
   * 고객 및 회사 관리 섹션에 액세스

시스템은 상점에서 회사 계정을 설정하는 사람에게 [회사 관리자](account-company-admin.md) 역할을 할당합니다. 관리자가 관리자에서 회사 계정 생성 요청을 승인하면 회사 관리자가 계정 암호를 설정하고 계정에 로그인할 수 있습니다.

## 방법 1: 고객이 상점 첫 화면에서 계정을 만듭니다.

**이 메서드를 사용해야 하는 경우:**

* Self-Service Business 등록 선호
* 고객은 필요한 모든 비즈니스 정보를 즉시 사용할 수 있습니다.
* 표준 승인 워크플로로 충분함
* 특별한 구성이나 미리 채우기가 필요하지 않습니다.

>[!IMPORTANT]
>
>이 방법을 지원하려면(고객이 상점 앞에서 회사를 등록할 수 있도록 허용) [B2B 기능](enable-basic-features.md)이 사용하도록 설정되어 있는지 확인하십시오.

1. storefront 헤더의 오른쪽 상단 모서리에서 고객이 **[!UICONTROL Create an Account]**&#x200B;을(를) 클릭하고 **[!UICONTROL Create New Company Account]**&#x200B;을(를) 선택합니다.

   ![새 회사 계정 만들기](./assets/company-account-create-storefront-options.png){width="700" zoomable="yes"}

   >[!NOTE]
   >
   >방문자가 등록된 사용자 계정에 로그인하면 _[!UICONTROL Customer Profile]_>**[!UICONTROL Company Structure]**>**[!UICONTROL Create a Company Account]**(으)로 이동하여 회사 계정을 만들 수 있습니다.

1. _[!UICONTROL Company Information]_섹션에서 고객은 다음을 수행합니다.

   * 필수 필드를 완료합니다.

      * **[!UICONTROL Company Name]**
      * **[!UICONTROL Company Email]**

   * 해당되는 경우 나머지 필드를 완료합니다.

      * **[!UICONTROL Company Legal Name]**
      * **[!UICONTROL VAT/TAX ID]**
      * **[!UICONTROL Reseller ID]**

   ![회사 정보](./assets/company-information-storefront.png){width="700" zoomable="yes"}

1. _[!UICONTROL Legal Address]_섹션의 필수 필드를 완료합니다.

   * **[!UICONTROL Street Address]**
   * **[!UICONTROL City]**
   * **[!UICONTROL Country]**
   * **[!UICONTROL State/Province]**
   * **[!UICONTROL ZIP/Postal Code]**
   * **[!UICONTROL Phone Number]**

   ![법적 주소](./assets/company-legal-address-storefront.png){width="700" zoomable="yes"}

1. _[!UICONTROL Company Administrator]_섹션에서 다음을 수행합니다.

   * 회사 관리자의 **[!UICONTROL Email address]**&#x200B;을(를) 입력합니다.

     회사 관리자의 이메일 주소는 회사 이메일 주소와 동일하거나 다른 이메일 주소일 수 있습니다. 다른 이메일 주소를 입력하면 회사 관리자 계정 외에 회사 사용자 계정이 생성됩니다.

   * 회사 관리자의 **[!UICONTROL First Name]** 및 **[!UICONTROL Last Name]**&#x200B;을(를) 입력합니다.

   * 선택적으로 다음 필드를 완료합니다.

      * **[!UICONTROL Job Title]**
      * **[!UICONTROL Work Phone Number]**
      * **[!UICONTROL Gender]**

   ![회사 관리자](./assets/company-administrator-account-storefront.png)

1. 이 storefront 함수에 대해 reCAPTCHA가 활성화된 경우 유효성 검사를 완료합니다.

1. 정보가 완료되면 **[!UICONTROL Submit]**&#x200B;을(를) 선택합니다.

   판매자가 회사 계정 생성 요청을 승인하면 시스템에서 회사 관리자에게 이메일 알림을 보냅니다.

   ![환영 전자 메일 예제](./assets/company-admin-welcome-email.png){width="500"}

   암호를 설정하면 회사 관리자가 계정에 [로그인](../customers/customer-sign-in.md)할 수 있습니다.

## 방법 2: 판매자가 관리자에서 계정을 만듭니다.

**이 메서드를 사용해야 하는 경우:**

* 영업 지원 계정 생성이 선호됩니다.
* 기존 비즈니스 관계에서 계정 세부 정보 미리 채우기
* 사용자 정의 구성이 필요합니다(크레딧 제한, 특별 가격).
* 승인 워크플로우 없이 즉시 활성화해야 함

관리자로부터 회사를 만드는 프로세스는 기본적으로 상점 첫 방문과 동일하지만 추가 필드가 있습니다.

![관리자로부터 새 회사 추가](./assets/company-add-new.png){width="700" zoomable="yes"}

1. _관리자_ 사이드바에서 **[!UICONTROL Customers]** > **[!UICONTROL Companies]**(으)로 이동합니다.

1. **[!UICONTROL Add New Company]**&#x200B;을(를) 클릭하고 다음을 수행합니다.

   * 다음 필수 필드를 완료하십시오.

      * **[!UICONTROL Company Name]**
      * **[!UICONTROL Company Email]**

   * 계정을 활성화할 준비가 되지 않은 경우 **[!UICONTROL Status]**&#x200B;을(를) `Pending Approval`(으)로 설정하십시오. 기본적으로 `Active`(으)로 설정됩니다.

   * 해당하는 경우 계정을 관리할 **[!UICONTROL Sales Representative]**&#x200B;의 관리자 계정을 선택하십시오.

1. _[!UICONTROL Account Information]_섹션에서 다음을 수행합니다.

   * 해당되는 경우 다음 필드를 작성합니다.

      * **[!UICONTROL Company Legal Name]**
      * **[!UICONTROL VAT/TAX ID]**
      * **[!UICONTROL Reseller ID]**

   * **[!UICONTROL Comment]**&#x200B;의 경우 필요할 수 있는 고객에 대한 추가 정보를 입력하십시오.

     주석은 관리자만 볼 수 있습니다.

   ![계정 정보](./assets/company-create-account-information-admin.png){width="700" zoomable="yes"}

1. 처음 회사를 만들 때 확장할 때 _[!UICONTROL Company Hierarchy]_그리드가 비어 있습니다. 회사를 저장한 후 회사 계층에 포함할 수 있습니다. [회사 관리](manage-companies.md)를 참조하세요.

1. _[!UICONTROL Legal Address]_섹션에서 다음 필수 필드를 작성합니다.

   * **[!UICONTROL Street Address]**
   * **[!UICONTROL City]**
   * **[!UICONTROL Country]**
   * **[!UICONTROL ZIP/Postal Code]**
   * **[!UICONTROL Phone Number]**

1. _[!UICONTROL Company Admin]_섹션에서 다음을 수행합니다.

   * 다음 필수 필드를 완료하십시오.

      * **[!UICONTROL Email]**
      * **[!UICONTROL First Name]**
      * **[!UICONTROL Last Name]**

   * 일부 고객 이름에 다른 고객보다 더 많이 적용할 수 있으며 재량에 따라 사용할 수 있는 이름의 다음 선택적 부분을 작성합니다.

      * **[!UICONTROL Prefix]**
      * **[!UICONTROL Middle Name/Initial]**
      * **[!UICONTROL Suffix]**

   * 정보를 사용할 수 있는 경우 회사 관리자를 설명하는 나머지 필드를 작성합니다.

      * **[!UICONTROL Website]**
      * **[!UICONTROL Job Title]**
      * **[!UICONTROL Work Phone Number]**
      * **[!UICONTROL Gender]**
      * **[!UICONTROL Send Welcome Email From]**

   ![회사 관리자](./assets/company-create-company-admin.png){width="700" zoomable="yes"}

1. 고객의 신용 활동에 대한 요약을 표시하는 _[!UICONTROL Company Credit]_섹션에서 섹션의 아래 부분에 있는 필드를 해당하는 수만큼 작성합니다.

   * **[!UICONTROL Credit Currency]**
   * **[!UICONTROL Credit Limit]**
   * **[!UICONTROL Allow to Exceed Credit Limit]**
   * **[!UICONTROL Reason for Change]**

   ![회사 크레딧](./assets/company-create-credit-admin.png){width="700" zoomable="yes"}

1. _[!UICONTROL Advanced Settings]_섹션에서 다음을 수행합니다.

   >[!NOTE]
   >
   >고객 그룹 지정은 회사와 사원이 사용할 수 있는 공유 카탈로그를 결정합니다. 기본적으로 시스템은 기본값으로 구성된 고객 그룹에 회사를 할당합니다.

   * 회사 및 해당 직원에 대한 **[!UICONTROL Customer Group]** 할당을 다른 공유 카탈로그에 액세스할 수 있는 그룹 또는 표준 고객 그룹으로 변경할 수 있습니다. 그룹을 변경하기 전에 확인하라는 메시지가 표시됩니다.

     ![고객 그룹 변경](./assets/company-advanced-settings-customer-group-admin.png){width="600"}

   * 회사 직원이 계정에서 견적을 생성하도록 허용하려면 **[!UICONTROL Allow Quotes]**&#x200B;을(를) `Yes`(으)로 설정하십시오.

   * 회사 직원이 해당 계정의 구매 주문을 만들고 사용할 수 있도록 하려면 **[!UICONTROL Enable Purchase Orders]**&#x200B;을(를) `Yes`(으)로 설정하십시오.

   * 회사에서 사용할 수 있는 **[!UICONTROL Applicable Payment Methods]**&#x200B;을(를) 변경하려면 **[!UICONTROL Use config settings]** 확인란의 선택을 취소하고 다음 중 하나를 선택하십시오.

     | 옵션 | 설명 |
     |-------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
     | `B2B Payment Methods` | (기본값) B2B 주문에 대해 기본값으로 설정된 모든 [결제 방법](../configuration-reference/general/b2b-features.md#default-b2b-payment-methods)을 사용하도록 설정합니다. |
     | `All Enabled Payment Methods` | 회사 계정과 연결된 고객 계정에 대해 [활성화된 모든 결제 방법](../configuration-reference/sales/payment-methods.md)을 사용할 수 있도록 합니다. |
     | `Selected Payment Methods` | 회사 계정과 연계된 고객 계정에 사용할 수 있는 결제 방법을 선택할 수 있습니다. 여러 결제 방법을 선택하려면 Ctrl 키(PC) 또는 Command 키(Mac)를 누른 상태에서 각 옵션을 선택합니다. |

     {style="table-layout:auto"}

   * 회사에서 사용할 수 있는 **[!UICONTROL Applicable Shipping Methods]**&#x200B;을(를) 변경하려면 **[!UICONTROL Use config settings]** 확인란의 선택을 취소하고 다음 중 하나를 선택하십시오.

     | 옵션 | 설명 |
     |--------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
     | `B2B Shipping Methods` | (기본값) B2B 주문에 대해 기본값으로 설정된 모든 [배송 방법](../configuration-reference/general/b2b-features.md#default-b2b-shipping-methods)을 사용하도록 설정합니다. |
     | `All Enabled Shipping Methods` | 회사 계정과 연결된 고객 계정에 대해 [활성화된 모든 배송 방법](../configuration-reference/sales/delivery-methods.md)을 사용할 수 있도록 합니다. |
     | `Selected Shipping Methods` | 회사 계정과 연계된 고객 계정에 사용할 수 있는 배송 방법을 선택할 수 있습니다. 여러 배송 방법을 선택하려면 Ctrl 키(PC) 또는 Command 키(Mac)를 누른 상태에서 각 옵션을 선택합니다. |

     {style="table-layout:auto"}

1. 완료되면 **[!UICONTROL Save]**&#x200B;을(를) 선택합니다.

   판매자가 회사 계정 생성 요청을 승인하면 회사 관리자의 이메일 주소로 이메일 알림이 전송됩니다.

   암호를 설정하면 회사 관리자가 계정에 [로그인](../customers/customer-sign-in.md)할 수 있습니다.

## 계정 생성 후

회사 계정이 만들어지면 다음 프로세스가 수행됩니다.

### &#x200B;1. 승인 작업 과정

* **보류 중 상태** - 새 계정이 관리자 검토 대기 중입니다.
* **프로세스 검토** - 저장소 관리자가 비즈니스 정보를 확인하고 요청을 승인/거부합니다.
* **상태 업데이트**—회사에서 승인 상태 변경에 대한 전자 메일 알림을 받습니다.

### &#x200B;2. 계정 활성화

* **환영 전자 메일** - 승인된 회사 관리자의 설정 지침 수신
* **암호 설정**—관리자가 계정 액세스를 위해 보안 암호를 만듭니다.
* **초기 로그인**—회사 대시보드 및 기능에 처음 액세스

### &#x200B;3. 회사 관리자의 다음 단계

활성화 후 회사 관리자는 다음 작업을 수행해야 합니다.

* **[회사 구조 구성](account-company-structure.md)**—부서 및 사용자 계층 구조 설정
* **[회사 사용자 관리](account-company-users.md)**—직원 추가 및 역할 할당
* **[구매 주문 설정](purchase-order-flow.md)**—필요한 경우 승인 워크플로 구성
* **[크레딧 설정 검토](credit-company.md)** - 회사 크레딧을 이해하고 관리합니다(활성화된 경우).

## 일반적인 문제 및 문제 해결

### 계정 생성 문제

**등록 양식을 전송하지 못했습니다**

* 모든 필수 필드가 올바르게 완료되었는지 확인
* 이메일 주소가 유효하고 고유한지 확인
* B2B 기능이 활성화되어 있고 회사 등록이 허용되는지 확인합니다.
* 브라우저 캐시를 지우고 다시 시도하십시오

**회사 이름이 이미 있음**

* 고유한 회사 이름 선택
* 오류라고 생각되면 관리자에게 문의하십시오
* 위치 또는 사업부 식별자를 추가하는 것이 좋습니다.

**전자 메일 주소 문제**

* 개인 이메일 주소가 아닌 회사 이메일 주소 사용
* 회사 관리자 이메일에 액세스할 수 있는지 확인
* 도메인이 이메일 필터에 의해 차단되지 않았는지 확인

### 승인 및 활성화 문제

**승인 전자 메일을 받지 못함**

* 스팸/정크 메일 폴더 확인
* 등록 중에 이메일 주소를 올바르게 입력했는지 확인
* 수동 승인 상태를 확인하려면 저장소 관리자에게 문의하십시오.
* 업무일 동안 24-48시간 처리 가능

**승인 후 암호를 설정할 수 없음**

* 승인 이메일에 제공된 정확한 링크 사용
* 활성화 링크가 만료되었는지 확인
* 관리자에게 새 활성화 이메일 요청

**활성화 후 액세스 문제**

* 올바른 회사 계정 포털을 통해 로그인하고 있는지 확인합니다.
* 계정 상태가 &quot;활성&quot;인지 확인
* 회사 관리자 자격 증명을 사용 중인지 확인
* 권한이 올바르지 않은 경우 지원 팀에 문의

## 보안 모범 사례

회사 계정을 만들고 관리할 때:

* **강력한 암호 사용**—회사 관리자를 위한 복잡한 암호가 필요합니다.
* **비즈니스 정보 확인**—승인 프로세스 중에 회사 세부 정보의 유효성을 검사합니다.
* **계정 활동 모니터링**—회사 사용자 액세스 및 권한을 정기적으로 검토합니다.
* **중요 데이터 보호**—신용 및 재무 정보가 올바르게 보호되는지 확인

## 회사 계정 사용자 인터페이스 참조

### 단추 막대

| 단추 | 설명 |
|---------------------------|------------------------------------------------------------------|
| [!UICONTROL Back] | 변경 사항을 저장하지 않고 회사 페이지로 돌아갑니다. |
| [!UICONTROL Reset] | 변경 내용이 저장되지 않은 모든 필드로 원래 값을 복원합니다. |
| [!UICONTROL Save] | 회사에 대한 변경 사항을 저장하고 프로필을 열어 둡니다. |
| [!UICONTROL Save & Close] | 회사에 대한 변경 사항을 저장하고 프로필을 닫습니다. |

{style="table-layout:auto"}

### 필드 설명

| 필드 | 설명 |
|-----------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Company Name] | 회사 이름은 회사 계정을 처음 만들 때 입력되며, 전체 법적 이름의 약식 버전일 수 있습니다. |
| [!UICONTROL Status] | (관리자만) 회사 계정의 현재 상태를 나타냅니다. 옵션: <br/>**[!UICONTROL Active]**- 스토어 관리자가 회사 계정을 승인했습니다. 회사 관리자 및 관련 회원은 상점에서 계정에 로그인하여 구매할 수 있습니다.<br/>**[!UICONTROL Pending Approval]** - 회사 계정 열기 요청이 제출되었지만 저장소 관리자가 아직 승인하지 않았습니다. <br/>**[!UICONTROL Rejected]**- 회사 계정 열기 요청이 제출되었지만 스토어 관리자가 승인하지 않았습니다. 요청을 제출하는 데 사용된 초기 로그인 자격 증명이 차단됩니다.<br/>**&#x200B;차단됨&#x200B;**- 회사 구성원은 로그인하여 카탈로그에 액세스할 수 있지만 구입할 수 없습니다. 스토어 관리자가 상태가 좋지 않은 회사 계정을 차단할 수 있습니다. 계정의 블록은 언제든지 저장소 관리자가 제거할 수 있습니다. |
| [!UICONTROL Company Email] | 회사 계정과 연결된 이메일 주소. |
| [!UICONTROL Sales Representative] | (관리자만) 회사 계정의 기본 연락처인 관리자 사용자입니다. |

{style="table-layout:auto"}

#### [!UICONTROL Account Information]

| 필드 | 설명 |
|---------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Company Legal Name] | 회사의 전체 법적 이름. |
| [!UICONTROL VAT / TAX ID] | 세금 보고 목적으로 일부 관할 구역에서 회사에 할당된 [부가가치세](../stores-purchase/vat.md) 번호입니다. 상점 앞에 나타나도록 고객 VAT/세금 ID를 구성하려면 [새 계정 옵션 만들기](../configuration-reference/customers/customer-configuration.md)를 참조하십시오. <br/> **_참고:_** 회사 관리자와 다른 회사 사용자는 고객 계정에 별도의 VAT/TAX ID 번호를 가지고 있지 않습니다. |
| [!UICONTROL Reseller ID] | 세금 보고 목적으로 회사에 지정된 재판매 번호. |
| [!UICONTROL Comment] | (관리자만) 회사 계정에 대한 이러한 참고는 참조용이며 관리자만 볼 수 있습니다. |

{style="table-layout:auto"}

#### [!UICONTROL Company Hierarchy]

| 필드 | 설명 |
|-----------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Company ID] | 회사의 ID 번호입니다. |
| [!UICONTROL Company Name] | 회사의 전체 이름. <br/>편집 중인 회사 줄에 `current company indicator`이(가) 나타납니다. |
| [!UICONTROL Company Email] | 회사 계정과 연결된 이메일 주소. |
| [!UICONTROL Phone Number] | 회사의 기본 전화번호. |
| [!UICONTROL Country] | 회사를 등록하여 비즈니스를 수행하는 국가. |
| [!UICONTROL State/Province] | 회사가 등록되어 사업을 수행하는 주 또는 시/도입니다. |
| [!UICONTROL City] | 비즈니스를 수행하기 위해 회사가 등록된 도시입니다. |
| [!UICONTROL Group/Shared Catalog] | (관리자만) 회사에 할당된 [고객 그룹](../customers/customer-groups.md) 또는 [공유 카탈로그](catalog-shared.md)를 표시합니다. |
| [!UICONTROL Company Admin] | 회사 관리자의 전체 이름. |
| [!UICONTROL Action] | 해당 회사 라인에 대해 가능한 작업 목록입니다. |

{style="table-layout:auto"}

#### [!UICONTROL Legal Address]

| 필드 | 설명 |
|------------------------------|-----------------------------------------------------------------------------|
| [!UICONTROL Street Address] | 회사가 사업을 하기 위해 등록한 거리 주소. |
| [!UICONTROL City] | 비즈니스를 수행하기 위해 회사가 등록된 도시입니다. |
| [!UICONTROL Country] | 회사를 등록하여 비즈니스를 수행하는 국가. |
| [!UICONTROL State/Province] | 회사가 등록되어 사업을 수행하는 주 또는 시/도입니다. |
| [!UICONTROL ZIP/Postal Code] | 회사가 등록되어 비즈니스를 수행하는 ZIP 또는 우편 번호입니다. |
| [!UICONTROL Phone Number] | 회사의 기본 전화번호. |

{style="table-layout:auto"}

#### [!UICONTROL Company Admin]

| 필드 | 설명 |
|--------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Website] | 회사 관리자가 속한 웹 사이트를 결정합니다. |
| [!UICONTROL Job Title] | 회사 계정을 관리하는 회사 관리자의 제목입니다. |
| [!UICONTROL Work Phone Number] | 회사 계정을 관리하는 회사 관리자의 전화번호. |
| [!UICONTROL Email] | 회사 관리자의 이메일 주소는 회사 이메일 주소와 같을 수 있습니다. 다른 이메일 주소를 입력하면 회사 계정 외에 회사 관리자를 위한 별도의 개별 계정이 만들어집니다. |
| [!UICONTROL Prefix] | 해당하는 경우 회사 관리자 이름과 연결된 접두사(예: `Mr.`, `Ms.`, `Mrs.` 또는 `Dr.`)입니다. 구성에 따라 입력 필드는 텍스트 필드 또는 목록일 수 있습니다. |
| [!UICONTROL First Name] | 회사 관리자의 이름입니다. |
| [!UICONTROL Middle Name/Initial] | 회사 관리자의 중간 이름 또는 이니셜입니다. |
| [!UICONTROL Last Name] | 회사 관리자의 성. |
| [!UICONTROL Suffix] | 해당되는 경우 회사 관리자의 이름과 연결된 접미사(예: `Jr.`, `Sr.` 또는 `III.`)입니다. 구성에 따라 입력 필드는 텍스트 필드 또는 목록일 수 있습니다. |
| [!UICONTROL Gender] | 회사 관리자의 성별. 옵션: `Male` / `Female` / `Not Specified` |
| [!UICONTROL Send Welcome Email From] | 시스템이 환영 이메일을 보내는 스토어 보기입니다. |

{style="table-layout:auto"}

#### [!UICONTROL Company Credit]

| 필드 | 설명 |
|-------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Credit Currency] | (관리자만) 회사 크레딧 구매에 대해 스토어에서 수락하는 통화입니다. |
| [!UICONTROL Credit Limit] | (관리자만) 회사 계정에 대한 크레딧 제한입니다. |
| [!UICONTROL Allow to Exceed Credit Limit] | (관리자만) 회사에 신용 한도를 초과할 권한이 있는지 여부를 나타냅니다. 옵션: `Yes` / `No` |
| [!UICONTROL Reason for Change] | (관리자만) 회사가 크레딧 제한을 초과할 수 없는 이유를 설명하는 참고 사항입니다. 이 필드는 크레딧 제한 초과 권한이 변경된 경우에만 활성화됩니다. |

{style="table-layout:auto"}

#### [!UICONTROL Advanced Settings]

개별 회사에 대한 고급 설정을 구성할 수 있습니다. 회사 계층을 만드는 경우, 각 하위 회사를 개별적으로 구성하는 대신 상위 회사에 대한 설정을 구성하고 이러한 설정을 모든 하위 회사 또는 선택한 하위 회사에 적용하여 설정 구성을 간소화할 수 있습니다. 자세한 내용은 [회사 계층 관리](manage-company-hierarchy.md)를 참조하십시오.

| 필드 | 설명 |
|------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Customer Group] | (관리자만) 회사에 할당된 [고객 그룹](../customers/customer-groups.md) 또는 [공유 카탈로그](catalog-shared.md)를 표시합니다. |
| [!UICONTROL Allow Quotes] | (관리자만) 회사 구성원이 회사를 대신하여 협상 가능한 견적을 준비하고 제출할 수 있는지 여부를 결정합니다. |
| [!UICONTROL Enable Purchase Orders] | (관리자만) 회사 구성원이 회사를 대신하여 주문을 [구매 주문](account-dashboard-my-purchase-orders.md)(으)로 제출할 수 있는지 여부를 결정합니다. |
| 해당 결제 방법 | (관리자만) 회사 구매에 사용할 수 있는 결제 방법을 나타냅니다. 옵션: `B2B Payment Methods` / `All Enabled Payment Methods` / `Selected Payment Methods` |
| [!UICONTROL Payment Methods] | (관리자만) 특정 결제 방법을 활성화하면 활성화됩니다. 회사 계정에 여러 결제 방법을 사용할 수 있도록 하려면 Ctrl 키(PC) 또는 Command 키(Mac)를 누른 채 각 옵션을 선택합니다. |
| [!UICONTROL Applicable Shipping Methods] | (관리자만) 회사 구매에 사용할 수 있는 배송 방법을 나타냅니다. 옵션: `B2B Shipping Methods` / `All Enabled Shipping Methods` / `Selected Shipping Methods` |
| [!UICONTROL Shipping Methods] | (관리자만) 특정 배송 방법을 활성화하면 활성화됩니다. 회사 계정에 여러 배송 방법을 사용할 수 있도록 하려면 Ctrl 키(PC) 또는 Command 키(Mac)를 누른 채 각 옵션을 선택합니다. |

{style="table-layout:auto"}

>[!MORELIKETHIS]
>
>* [B2B 기능 사용](enable-basic-features.md)—기본 B2B 기능 구성
>* [회사 계정 구조](account-company-structure.md)—상점에서 사용자 및 부서 구성
>* [회사 사용자 관리](account-company-users.md)—상점에서 직원 계정을 추가하고 구성합니다.
>* [회사 관리자 역할](account-company-admin.md)—관리자 권한 이해
>* [회사 관리](manage-companies.md)—회사 관리에 대한 관리 개요
>* [회사 크레딧 관리](credit-company.md)—관리자의 회사 크레딧을 설정하고 관리합니다.
>* [구매 주문 워크플로](purchase-order-flow.md)—관리자의 승인 프로세스 구성
>* [회사 역할 및 권한](account-company-roles-permissions.md)—관리자의 사용자 액세스 수준 제어
>* [B2B 구성 참조](../configuration-reference/general/b2b-features.md)—자세한 시스템 설정
