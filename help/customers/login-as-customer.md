---
title: 쇼핑객 지원 제공
description: 고객으로 로그인 기능을 사용하면 고객이 본 내용을 확인하고 고객을 대신하여 업데이트할 수 있습니다.
exl-id: 6842ae7a-6440-45f1-af18-e6427088d29d
feature: Customers, Customer Service
source-git-commit: 29f3a8bb019d464e6d7646e0ebc7a4fa2ed0dd74
workflow-type: tm+mt
source-wordcount: '1077'
ht-degree: 0%

---

# 쇼핑객 지원 제공

고객은 때때로 주문에 대한 도움이 필요합니다. 스토어 관리자는 _고객으로 로그인_&#x200B;을 사용하여 고객이 보는 항목을 보고 업데이트할 수 있습니다.

고객으로 로그인된 상태에서 수행한 모든 작업은 실제 고객의 계정에 적용됩니다.

>[!BEGINTABS]

>[!TAB Adobe Commerce]

[!BADGE PaaS만]{type=Informative url="https://experienceleague.adobe.com/ko/docs/commerce/user-guides/product-solutions" tooltip="Adobe Commerce 온 클라우드 프로젝트(Adobe 관리 PaaS 인프라) 및 온프레미스 프로젝트에만 적용됩니다."}

_관리자_ 사용자에 대해 _[!UICONTROL Login as Customer]_&#x200B;단추가 활성화되면 여러 페이지에 표시됩니다.

* [고객 편집 페이지](../customers/update-account.md)
* [주문 보기 페이지](../stores-purchase/order-processing.md)
* [송장 보기 페이지](../stores-purchase/invoices.md)
* [배송 조회 페이지](../stores-purchase/shipments.md)
* [대변 메모 보기 페이지](../stores-purchase/credit-memo-create.md)

![고객으로 로그인](assets/login-as-customer.png){width="600" zoomable="yes"}

>[!TAB Adobe Commerce as a Cloud Service]

[!BADGE SaaS만]{type=Positive url="https://experienceleague.adobe.com/ko/docs/commerce/user-guides/product-solutions" tooltip="Adobe Commerce as a Cloud Service 및 Adobe Commerce Optimizer 프로젝트에만 적용됩니다(Adobe 관리 SaaS 인프라)."}

Adobe Commerce as a Cloud Service에서 고객으로 로그인 기능은 직접 로그인 대신 **OTC(일회성 코드)** 워크플로우를 사용합니다. 관리자는 고객을 위해 단기간 동안 사용할 수 있는 코드를 생성합니다. 그런 다음 GraphQL을 통해 고객 액세스 토큰으로 이 코드를 교환할 수 있으므로 판매자 지원 쇼핑 시나리오를 위한 고객 워크플로우로 암호 없는 로그인을 가능하게 합니다.

이 기능은 다음 구성 요소로 구성됩니다.

* **관리자 UI** - 고객 편집 페이지에서 관리자는 고객으로 직접 로그인하지 않고 OTC(일회용 코드)를 요청할 수 있습니다.
* **[REST API](https://developer.adobe.com/commerce/webapi/rest/saas-integrations/login-as-customer/)** - 관리 스크립트 및 서드파티 통합에 유용한 OTC 생성을 위한 프로그래밍 종단점입니다.
* **GraphQL API** - 상점 또는 헤드리스 상거래 흐름을 위한 고객 액세스 토큰으로 OTC를 교환하는 돌연변이.

>[!ENDTABS]

## 고객으로 로그인 활성화

_고객으로 로그인_&#x200B;을(를) 활성화하려면 Commerce 인스턴스에서 기능을 활성화한 다음 사용자 역할 권한에서 관리자 사용자에 대한 액세스를 활성화해야 합니다.

### 기능 활성화

1. 관리 사이드바에서 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**(으)로 이동합니다.

1. 왼쪽 패널에서 **[!UICONTROL Customers]**&#x200B;을(를) 확장하고 **[!UICONTROL Login as Customer]**&#x200B;을(를) 선택합니다.

   ![구성 옵션 - 고객으로 로그인](../configuration-reference/customers/assets/login-as-customer.png){width="600" zoomable="yes"}

1. **[!UICONTROL Enable Login as Customer]**&#x200B;을(를) `Yes`(으)로 설정합니다.

1. _(선택 사항)_ 관리자 사용자가 고객으로 로그인할 때 페이지 캐시를 활성화하려면 **[!UICONTROL Disable Page Cache for Admin User]**&#x200B;을(를) `No`(으)로 설정합니다.

   >[!WARNING]
   >
   > 페이지 캐시(`Yes` - 기본값)를 비활성화하면 사용자로 로그인한 사용자가 캐시되지 않은 새 데이터를 받게 됩니다.

1. _(선택 사항)_ 다중 사이트 및/또는 다중 스토어 설정이 있고 관리자로 로그인할 때 관리자가 스토어 보기를 선택하게 하려면 **[!UICONTROL Store View to Log in]**&#x200B;을(를) `Manual Selection`(으)로 설정합니다.

1. 완료되면 **[!UICONTROL Save Config]**&#x200B;을(를) 클릭합니다.

### 관리 사용자에 대한 액세스 활성화

1. _관리자_ 사이드바에서 **[!UICONTROL System]** > _권한_ > **[!UICONTROL User Roles]**(으)로 이동합니다.

1. 목록에서 역할을 클릭합니다.

1. [!UICONTROL _역할 정보_] 왼쪽 패널에서 **[!UICONTROL Role Resources]**&#x200B;을(를) 클릭합니다.

1. 페이지의 **[!UICONTROL Role Resources]**&#x200B;을(를) `Custom`(으)로 변경합니다.

   >[!INFO]
   >
   > 이 옵션을 선택하면 페이지에 리소스 계층 구조가 표시됩니다.

1. **[!UICONTROL Customers]** 상위 항목 및 그 아래의 **[!UICONTROL Login as Customer]** 항목으로 스크롤합니다. 그런 다음 역할에 대해 활성화할 리소스를 선택합니다.

   * **[!UICONTROL Allow Login as Customer]** - 관리자가 _고객으로 로그인_ 기능을 사용할 수 있습니다.
   * **[!UICONTROL View Login as Customer Log]** - 관리자가 _고객으로 로그인_ 로그를 볼 수 있습니다.

   ![역할 리소스 - 고객으로 로그인](assets/customers-login-as-customer-role-resources.png){width="400" zoomable="yes"}

1. **[!UICONTROL Save Role]**&#x200B;을(를) 클릭합니다.

## 원격 쇼핑 지원을 위한 고객 계정 권한

관리자의 스토어 지원 직원에 대한 계정 액세스를 활성화하려면 고객은 자신의 계정에 대해 기능을 활성화해야 합니다.

>[!BEGINTABS]

>[!TAB Adobe Commerce]

[!BADGE PaaS만]{type=Informative url="https://experienceleague.adobe.com/ko/docs/commerce/user-guides/product-solutions" tooltip="Adobe Commerce 온 클라우드 프로젝트(Adobe 관리 PaaS 인프라) 및 온프레미스 프로젝트에만 적용됩니다."}

1. 고객이 **[!UICONTROL Account Information]** 페이지로 이동합니다.

1. **[!UICONTROL Allow remote shopping assistance]** 확인란을 선택합니다.

1. 고객이 **[!UICONTROL Save]**&#x200B;을(를) 클릭합니다.

![계정 정보 페이지](assets/permission.png){width="700" zoomable="yes"}

>[!TAB Adobe Commerce as a Cloud Service]

[!BADGE SaaS만]{type=Positive url="https://experienceleague.adobe.com/ko/docs/commerce/user-guides/product-solutions" tooltip="Adobe Commerce as a Cloud Service 및 Adobe Commerce Optimizer 프로젝트에만 적용됩니다(Adobe 관리 SaaS 인프라)."}

고객은 `login_as_customer_assistance_allowed` 확장 특성을 **2**(으)로 설정해야 합니다. 이는 관리자의 **고객 편집** 페이지에서 구성하거나 고객을 만들거나 편집할 때 GraphQL을 통해 구성할 수 있습니다.

>[!WARNING]
>
>이 권한이 없으면 관리자 사용자는 이 고객으로 로그인할 수 없습니다.

![고객 편집 페이지의 고객 동의 확장 특성 구성](assets/customer-consent-attribute.png){width="600" zoomable="yes"}

기존 고객 계정에 대해 GraphQL을 사용하여 이 권한을 설정하려면 `allow_remote_shopping_assistance` `true` 또는 [`updateCustomerV2`](https://developer.adobe.com/commerce/webapi/graphql/schema/customer/mutations/update-v2/) 돌연변이를 사용하여 [`createCustomerV2` 입력을 &#x200B;](https://developer.adobe.com/commerce/webapi/graphql/schema/customer/mutations/create-v2/)&#x200B;(으)로 설정하십시오.

>[!ENDTABS]

## 관리자에서 고객으로 로그인

>[!BEGINTABS]

>[!TAB Adobe Commerce]

[!BADGE PaaS만]{type=Informative url="https://experienceleague.adobe.com/ko/docs/commerce/user-guides/product-solutions" tooltip="Adobe Commerce 온 클라우드 프로젝트(Adobe 관리 PaaS 인프라) 및 온프레미스 프로젝트에만 적용됩니다."}

1. _관리자_ 사이드바에서 **[!UICONTROL Customers]** > [!UICONTROL _모든 고객_]&#x200B;(으)로 이동합니다.

1. 편집 모드에서 사용자를 엽니다.

1. **[!UICONTROL Customer Information]** 패널에서 **[!UICONTROL Account Information]** 섹션을 선택합니다.

1. **[!UICONTROL Allow remote shopping assistance]**&#x200B;을(를) `Yes`(으)로 설정합니다.

   >[!INFO]
   >
   >이제 관리자는 상점 첫 화면에서 권한 없이 사용자로 로그인할 수 있습니다.

>[!TAB Adobe Commerce as a Cloud Service]

[!BADGE SaaS만]{type=Positive url="https://experienceleague.adobe.com/ko/docs/commerce/user-guides/product-solutions" tooltip="Adobe Commerce as a Cloud Service 및 Adobe Commerce Optimizer 프로젝트에만 적용됩니다(Adobe 관리 SaaS 인프라)."}

>[!NOTE]
>
>REST를 사용하여 이 기능을 구현하는 방법에 대한 지침은 [고객으로 로그인](https://developer.adobe.com/commerce/webapi/rest/saas-integrations/login-as-customer/) REST API 설명서를 참조하십시오.

### 책임자에게 일회용 코드(OTC) 요청

1. **[!UICONTROL Customers]**(으)로 이동하여 편집 페이지를 열 고객을 선택하십시오.

1. 고객 편집 페이지에서 **[!UICONTROL Get Customer Login OTC]**&#x200B;을(를) 클릭합니다.

   ![고객 편집 페이지의 고객 로그인 OTC 가져오기 단추](assets/get-customer-login-otc-button.png){width="600" zoomable="yes"}

1. **[!UICONTROL Reason]**(필수)을(를) 입력하고 **[!UICONTROL Request]**&#x200B;을(를) 클릭합니다.

   이유 필드가 있는 ![OTC 요청 양식](assets/otc-reason-modal.png){width="600" zoomable="yes"}

   >[!NOTE]
   >
   >**이유** 필드는 필수입니다. OTP 생성 플로우로 전달되며 향후 감사 및 이벤트 로깅 기능에서 사용하도록 예약됩니다.

1. 생성된 OTC가 모달에 표시됩니다. 고객 인증을 위해 이 코드를 `generateCustomerToken` 또는 `exchangeOtpForCustomerToken` GraphQL 돌연변이와 함께 사용하십시오.

   ![생성된 OTC가 모달에 표시됨](assets/otc-generated-code.png){width="300" zoomable="yes"}

>[!IMPORTANT]
>
>생성된 일회용 코드 OTC는 기본적으로 30초 동안 유효하며 한 번 사용 후 무효화됩니다. [지원 티켓](https://experienceleague.adobe.com/home?lang=ko&support-tab=home#support)을 제출하여 TTL을 구성할 수 있습니다.

일회용 코드가 생성되면 상점으로 이동하여 다음 자격 증명을 사용하여 로그인하면 일회용 코드를 사용할 수 있습니다.

* **이메일**: 고객의 이메일 주소
* **암호**: 생성된 일회용 코드(OTC)

>[!ENDTABS]

## 고객으로 로그인 사용

>[!INFO]
>
>_고객으로 로그인_&#x200B;을 사용하려면 관리자가 앞에서 설명한 대로 구성되어 있는지 확인하십시오.

_고객으로 로그인_&#x200B;을 통해 고객처럼 사이트를 볼 수 있으며 문제를 해결하고 고객을 위해 다른 조치를 취할 수 있습니다. 필요한 권한이 있는 할당된 사용자 역할이 있는 경우:

1. 이전 섹션에 나열된 페이지에서 **[!UICONTROL Login as Customer]**&#x200B;을(를) 클릭합니다.
1. 고객으로 로그인 작업은 작업 보고서에서 사용할 수 있습니다.

>[!WARNING]
>
>[!UICONTROL _as Customer_]&#x200B;에 로그인하는 동안 수행한 모든 작업(예: 제품 추가/제거)이 실제 고객의 주문에 적용됩니다. `logged in as customer_name`일 때 상점 앞에는 특수 상태를 알리는 배너가 표시됩니다.

## 고객 로그인으로 로그인

{{ee-feature}}

Adobe Commerce은 _고객으로 로그인_ 작업에 대한 로깅을 제공합니다. 이 목록에는 관리 사용자가 기능에 액세스하는 모든 세션이 나열됩니다. 기록된 작업에 액세스하려면 [관리자 작업 보고서](../systems/action-log-report.md)(으)로 이동하십시오.

보고서 설정 **[!UICONTROL Action Group]**&#x200B;을(를) `Login As Customer`(으)로 필터링하고 **[!UICONTROL Search]**&#x200B;을(를) 클릭할 수 있습니다.

![작업 보고서 필터링](assets/customers-login-as-customer-log-filter.png){width="700" zoomable="yes"}
