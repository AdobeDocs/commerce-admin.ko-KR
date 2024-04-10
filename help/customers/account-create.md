---
title: 개별 고객 계정 만들기
description: 방문자는 쉽게 개별 고객 계정을 만들어 구매를 관리할 수 있습니다.
exl-id: 8d08c0e1-f3ba-4423-98a7-ffa8ba5a1b8b
feature: Customers, Storefront
source-git-commit: 06673ccb7eb471d3ddea97218ad525dd2cdcf380
workflow-type: tm+mt
source-wordcount: '1268'
ht-degree: 0%

---

# 개별 고객 계정 만들기

스토어 방문자는 계정을 열어 구매 및 활동을 관리할 수 있습니다. 고객은 일반적으로 스토어에서 자신의 계정을 만듭니다. 그러나 관리자로부터 직접 고객 계정을 만들 수도 있으므로 전화상으로 고객을 지원하는 데 유용합니다.

다음 지침은 기본 고객 계정 구성을 나타냅니다. 양식의 일부 필드 선택 및 동작을 변경하려면 다음을 참조하십시오. [고객 계정 구성](../customers/customer-account-scope.md).

저장소 관리자는 [새 계정 옵션](../customers/account-options-new.md) 등록된 계정이 유효한지 확인하는 데 도움이 되는 확인 이메일을 새로 등록된 고객에게 보냅니다.

>[!NOTE]
>
>버전 2.4.7부터 고객은 브라우저에 관계없이 이메일 확인 후 계정에 로그인하려면 이메일 및 암호를 다시 입력해야 합니다.

## 상점 첫 화면에서 계정 만들기

상점 고객이 상점 앞에 계정을 만듭니다.

1. 상점에서 클릭 수 **[!UICONTROL Create an Account]** 머리글의 오른쪽 상단에 있습니다.

   ![계정 만들기](assets/storefront-create-an-account-link.png){width="700" zoomable="yes"}

1. 아래 **[!UICONTROL Personal Information]**, 입력 **[!UICONTROL First Name]** 및 **[!UICONTROL Last Name]**.

   ![개인 정보](assets/storefront-create-account-personal-information.png){width="600" zoomable="yes"}

1. 고객이 뉴스레터 구독자 목록에 이름과 이메일 주소를 추가하려면 **[!UICONTROL Sign Up for Newsletter]** 확인란.

   >[!INFO]
   >
   > 이 옵션은 스토어에서 뉴스레터를 게시하지 않는 경우에도 표시됩니다.

1. 매장 지원 직원이 다음 작업을 수행하기를 원할 경우 [표시되는 항목 보기](../customers/login-as-customer.md) 원격 지원을 제공할 경우 고객은 **[!UICONTROL Allow remote shopping assistance]** 확인란.

1. 아래 **[!UICONTROL Sign-in Information]**, 입력 **[!UICONTROL Email]** 주소.

   >[!INFO]
   >
   > 이 이메일 주소는 로그인 자격 증명의 일부가 되며 다른 고객 계정과 연결될 수 없습니다.

   ![로그인 정보](assets/storefront-create-account-signin-information.png){width="600" zoomable="yes"}

1. 을(를) 입력합니다 **[!UICONTROL Password]** 여기에는 다음 세 가지 유형의 정보가 포함됩니다.

   - 소문자
   - 대문자
   - 숫자
   - 특수 문자

   누른 후 **[!UICONTROL Enter]**&#x200B;를 입력하면 암호의 강도가 평가되고 필드 아래에 표시됩니다. 암호가 다음과 같은 경우 _약함_&#x200B;로 평가될 때까지 다른 작업 시도 _강력함_.

   ![강력한 암호를 사용하는 것이 좋습니다.](assets/storefront-customer-account-create-password-strong.png){width="600" zoomable="yes"}

1. 그런 다음 고객이 다시 입력합니다. **[!UICONTROL Confirm Password]**.

1. 필요한 경우 클릭 수 **[!UICONTROL Show Password]** 입력한 암호를 확인합니다.

1. 완료되면 클릭 수 **계정 만들기**.

그런 다음 고객은 이메일 주소와 암호를 사용하여 [로그인](../customers/customer-sign-in.md) 계정 및 주소 정보를 작성합니다.

## 책임자로부터 계정 만들기

판매자는 관리자로부터 고객 계정을 생성할 수 있습니다.

1. 다음에서 _관리자_ 사이드바, 이동 **[!UICONTROL Customers]** > **[!UICONTROL All Customers]**.

1. 클릭 **[!UICONTROL Add New Customer]**.

### 1단계: 계정 정보 작성

![고객 정보](assets/new-information.png){width="700" zoomable="yes"}

1. 다음에서 **[!UICONTROL Account Information]** 섹션에서 다음을 수행합니다.

   - 다중 사이트 설치의 경우 다음을 설정합니다. **[!UICONTROL Associate to Website]** 고객 계정이 적용되는 웹 사이트로 이동합니다.
   - 해당하는 경우 고객을 다른 사용자에게 할당합니다 **[!UICONTROL Customer Group]**.
   - 을 사용하는 경우 [VAT ID 유효성 검사](../stores-purchase/vat.md) 및 다음을 원합니다. **[!UICONTROL Disable Automatic Group Change Based on VAT ID]**&#x200B;확인란을 선택합니다.

1. 필수 필드를 작성합니다.

   - **[!UICONTROL First Name]**
   - **[!UICONTROL Last Name]**
   - **[!UICONTROL Email]**

1. 필요에 따라 선택적 필드를 완료합니다.

   - **[!UICONTROL Name Prefix]**
   - **[!UICONTROL Middle Name/Initial]**
   - **[!UICONTROL Name Suffix]**
   - **[!UICONTROL Date of Birth]**
   - **[!UICONTROL Tax/VAT Number]**
   - **[!UICONTROL Gender]**

   >[!WARNING]
   >
   >현재 보안 및 개인 정보 보호 모범 사례를 준수하면서 다른 개인 식별자를 사용한 고객의 전체 생년월일(월, 일, 년) 저장과 관련된 잠재적 법적 및 보안 위험에 대해 알아두어야 합니다. 고객의 전체 생년월일 보관을 제한하는 것이 좋으며 대안으로 고객의 생년월일을 사용할 것을 제안했습니다.

1. 설정 **[!UICONTROL Send Welcome Email From]** 을 시작할 스토어 보기로 _시작_ 이메일이 전송됩니다.

   >[!INFO]
   >
   > 스토어에 서로 다른 보기가 있는 경우 [언어](../stores-purchase/store-localize.md), 이 설정은 시작 이메일의 언어를 결정합니다.

1. 클릭 **[!UICONTROL Save and Continue Edit]** 을 클릭합니다.

   >[!INFO]
   >
   >고객 계정이 저장되면 전체 옵션 세트가 왼쪽 패널과 페이지 상단의 메뉴에 나타납니다. 다음 _[!UICONTROL Customer View]_탭에는 계정의 요약이 표시됩니다.

   ![고객 보기](assets/customer-account-create-saved.png){width="600" zoomable="yes"}

### 2단계: 주소 정보 작성

1. 왼쪽 패널에서 을 선택합니다 **[!UICONTROL Addresses]** 및 클릭 **[!UICONTROL Add New Addresses]**.

1. 청구와 배송 모두에 동일한 주소가 사용되는 경우 두 옵션을 모두 전환합니다.

   - **[!UICONTROL Default Billing Address]**
   - **[!UICONTROL Default Shipping Address]**

   ![고객 주소 정보 추가](assets/information-addresses.png){width="600" zoomable="yes"}

1. 아래로 스크롤하여 두 번째 열의 필수 주소 필드를 작성합니다.

   - **[!UICONTROL Street Address]**
   - **[!UICONTROL City]**
   - **[!UICONTROL Country]**
   - **[!UICONTROL State/Province]**
   - **[!UICONTROL ZIP/Postal Code]**

1. 다음을 입력합니다. **[!UICONTROL Phone Number]** 이 주소입니다.

1. 해당하는 경우 다음을 입력합니다. **[!UICONTROL VAT Number]** 고객과 연관되어 있습니다.

1. 이 주소만 계정에 필요한 경우 **[!UICONTROL Save]**.

   그렇지 않으면 **[!UICONTROL Save and Continue Edit]** 주소를 추가하려면 이전 단계를 반복하십시오.

   새 주소는 [!UICONTROL Addresses] 페이지가 선택됨 _[!UICONTROL Default Billing]_및_[!UICONTROL Default Shipping]_ 주소는 전체 목록 위에 있습니다.

   ![주소 보기](assets/address-list.png){width="600" zoomable="yes"}

### 3단계: 암호 재설정

책임자로부터 생성된 고객 계정에는 처음에 할당된 암호가 없습니다.

1. 표에서 새 고객 계정을 찾습니다.

1. 클릭 **[!UICONTROL Edit]** 다음에서 _[!UICONTROL Action]_열.

1. 페이지 상단의 메뉴 모음에서 를 클릭합니다. **[!UICONTROL Reset Password]**.

1. 암호 설정 지침과 함께 알림이 계정 소유자에게 전송됩니다.

## 단추 막대

프로파일을 처음 저장하면 추가 버튼을 사용할 수 있습니다. 자세한 내용은 다음을 참조하십시오. [고객 프로필 업데이트](../customers/update-account.md).

| 단추 | 설명 |
|--- |--- |
| **[!UICONTROL Back]** | 로 돌아갑니다. _[!UICONTROL Customers]_변경 사항을 저장하지 않은 페이지입니다. |
| **[!UICONTROL Delete Customer]** | 현재 고객을 삭제합니다. 고객과 연관된 완료된 주문은 제거되지 않습니다. |
| **[!UICONTROL Reset]** | 고객 양식에서 저장되지 않은 변경 사항을 이전 값으로 재설정합니다. |
| **[!UICONTROL Create Order]** | 고객에 대한 주문을 생성합니다. |
| **[!UICONTROL Reset Password]** | 전송: [암호 재설정](../customers/password-reset.md) 이메일로 고객에게 연결합니다. |
| **[!UICONTROL Force Sign-in]** | 고객 계정과 연결된 OAuth 액세스 토큰을 취소합니다. 이 함수는 웹 API의 일부로 OAuth 토큰이 할당된 고객 계정에서만 사용할 수 있습니다 [통합](../systems/integrations.md). 자세한 내용은 다음을 참조하십시오. [OAuth 기반 인증](https://developer.adobe.com/commerce/webapi/get-started/authentication/gs-authentication-oauth/) 개발자 설명서에서 참조하십시오. |
| **[!UICONTROL Manage Shopping Cart]** | 관리자가 고객의 장바구니를 관리할 수 있습니다. |
| **[!UICONTROL Save and Continue Edit]** | 변경 사항을 저장하고 고객 프로필을 열어 둡니다. |
| **[!UICONTROL Save Customer]** | 변경 사항을 저장하고 고객 프로필을 닫습니다. |

{style="table-layout:auto"}

## 필드 설명

### [!UICONTROL Account Information]

| 필드 | 설명 |
|--- |--- |
| **[!UICONTROL Associate to Website]** | 고객 계정과 연결된 웹 사이트를 식별합니다. |
| **[!UICONTROL Group]** | 다음 항목을 식별합니다. [고객 그룹](../customers/customer-groups.md) 고객이 멤버인 경우. 해당하는 경우 확인란을 선택하여 VAT에 따른 자동 그룹 변경을 비활성화합니다. |
| **[!UICONTROL Name Prefix]** | 사용되는 경우 고객 이름과 연결된 접두사(예: Mr, Ms, 또는 Dr). 접두사 값은 다음에 의해 결정됩니다. [구성](../configuration-reference/customers/customer-configuration.md). 구성에 따라 입력 컨트롤은 텍스트 필드이거나 옵션 목록일 수 있습니다. |
| **[!UICONTROL First Name]** | 고객의 이름. |
| **[!UICONTROL Middle Name / Initial]** | 고객의 중간 이름 또는 이니셜입니다. 이 필드는에 지정된 경우에만 포함됩니다 [구성](../configuration-reference/customers/customer-configuration.md) 주제. |
| **[!UICONTROL Last Name]** | 고객의 성입니다. |
| **[!UICONTROL Name Suffix]** | 사용되는 경우 고객 이름과 연결된 접미사(예: Jr., Sr. 또는 III). 접미사 값은 다음에 의해 결정됩니다. [구성](../configuration-reference/customers/customer-configuration.md). 구성에 따라 입력 컨트롤은 텍스트 필드이거나 옵션 드롭다운 목록일 수 있습니다. |
| **[!UICONTROL Email]** | 고객의 이메일 주소입니다. |
| **[!UICONTROL Date of Birth]** | 고객의 생년월일 생년월일은 다음에 지정된 경우 포함됩니다. [구성](../configuration-reference/customers/customer-configuration.md) 주제. <br><br>현재 보안 및 개인 정보 보호 모범 사례를 준수하면서 다른 개인 식별자를 사용한 고객의 전체 생년월일(월, 일, 년) 저장과 관련된 잠재적 법적 및 보안 위험에 대해 알아두어야 합니다. 고객의 전체 생년월일 보관을 제한하고 고객 생년월일을 대안으로 사용하는 것이 좋습니다. |
| **[!UICONTROL Tax / VAT Number]** | 해당되는 경우 고객의 세금 또는 부가가치세 번호. |
| **[!UICONTROL Gender]** | 고객의 성별을 식별합니다. 성별은 다음에 지정된 경우 포함됩니다. [구성](../configuration-reference/customers/customer-configuration.md). 옵션: `Male` / `Female` / `Not Specified` |
| **[!UICONTROL Send Welcome Email From]** | 스토어 보기가 여러 개 있는 경우 이 설정은 시작 메시지가 전송되는 스토어 보기를 식별합니다. 스토어 보기가 다른 언어에 사용되는 경우 이 설정은 시작 이메일의 언어를 결정합니다. |

### [!UICONTROL Addresses]

| 필드 | 설명 |
|--- |--- |
| **[!UICONTROL New Addresses]** | 새 주소의 유형을 식별합니다. 옵션: `Default Billing Address` / `Default Shipping Address` |
| **[!UICONTROL Add New Addresses]** | 입력할 주소의 유형을 식별하는 다른 새 주소 섹션을 표시합니다. |
| **[!UICONTROL Company]** | 해당 주소에 해당하는 경우 회사 이름. |
| **[!UICONTROL Street Address]** | 고객의 거리 주소입니다. 다음에 지정된 경우 상세 주소의 두 번째 줄을 사용할 수 있습니다. [구성](../configuration-reference/customers/customer-configuration.md) 주제. |
| **[!UICONTROL City]** | 고객 주소가 있는 도시입니다. |
| **[!UICONTROL Country]** | 고객 주소가 있는 국가입니다. |
| **[!UICONTROL State/Province]** | 고객 주소가 있는 시/도입니다. |
| **[!UICONTROL Zip/Postal Code]** | 고객 주소가 있는 ZIP 또는 우편 번호입니다. |
| **[!UICONTROL Phone Number]** | 주소와 연결된 고객 전화번호. |
| **[!UICONTROL VAT Number]** | 해당되는 경우, 이 주소의 고객에게 적용되는 부가가치세 번호. |
