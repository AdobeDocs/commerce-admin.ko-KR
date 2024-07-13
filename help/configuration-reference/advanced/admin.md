---
title: '[!UICONTROL Advanced] &gt; [!UICONTROL Admin]'
description: Commerce 관리자의 [!UICONTROL Advanced] &gt; [!UICONTROL Admin] 페이지에서 구성 설정을 검토하십시오.
exl-id: 546b8d01-9611-4415-ab2b-29be560316f5
role: Admin
feature: Configuration, Admin Workspace
source-git-commit: 61df9a4bcfaf09491ae2d353478ceb281082fa74
workflow-type: tm+mt
source-wordcount: '1209'
ht-degree: 0%

---

# 고급 > 관리

{{config}}

## [!UICONTROL Admin User Emails]

![관리자 전자 메일](./assets/admin-admin-user-emails.png)<!-- zoom -->

이러한 설정을 변경하는 방법에 대한 자세한 내용은 [암호를 잊어버리고 전자 메일을 다시 설정](../../systems/permissions-users-all.md#forgotten-password-and-reset-emails)을 참조하십시오.

| 필드 | [범위](../../getting-started/websites-stores-views.md#scope-settings) | 설명 |
|---------------------------------------------|------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Forgot Password Email Template] | 글로벌 | 관리자가 암호를 잊어버렸을 때 보내는 메시지에 사용되는 이메일 템플릿을 식별합니다. 기본 템플릿: `Forgot Admin Password` |
| [!UICONTROL Forgot and Reset Email Sender] | 글로벌 | _암호 찾기_ 전자 메일의 보낸 사람으로 표시되는 스토어 연락처를 식별합니다. 기본 보낸 사람: `General Contact`<br/>기타 보낸 사람 옵션: `Sales Representative`, `Customer Support`, `Custom Email` |
| [!UICONTROL User Notification Template] | 글로벌 | 관리자 알림의 기본값으로 사용되는 이메일 템플릿을 결정합니다. 기본 템플릿: `User Notification` |

{style="table-layout:auto"}

## [!UICONTROL Startup Page]

![시작 페이지](./assets/admin-startup-page.png)<!-- zoom -->

이러한 설정 변경에 대한 자세한 내용은 _시작 안내서_&#x200B;에서 [시작 페이지 변경](../../getting-started/admin-dashboard.md#change-the-startup-page)을 참조하십시오.

| 필드 | [범위](../../getting-started/websites-stores-views.md#scope-settings) | 설명 |
|---------------------------|------------------------------------------------------------------------|------------------------------------------------------------------|
| [!UICONTROL Startup Page] | 글로벌 | 로그인 후 표시되는 관리자 랜딩 페이지를 결정합니다. |

{style="table-layout:auto"}

### [!UICONTROL Startup Page] 옵션

| 영역 |                                                                                                                                                                                                                                                                                                                                                                           | 옵션 |
|---------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [`Dashboard`](../../getting-started/admin-dashboard.md) |                                                                                                                                                                                                                                                                                                                                                                           |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| `Sales` | `Operations` | [`Quotes`](../../b2b/quotes.md) ![Adobe Commerce B2B](../../assets/b2b.svg) <br/>[`Orders`](../../stores-purchase/orders.md)<br/>[`Invoices`](../../stores-purchase/invoices.md)<br/>[`Shipments`](../../stores-purchase/shipments.md)<br/>[`Credit Memos`](../../stores-purchase/credit-memos.md)<br/>[`Billing Agreements`](../../stores-purchase/paypal-billing-agreements.md)<br/>[`Returns`](../../stores-purchase/returns.md) ![Adobe Commerce](../../assets/adobe-logo.svg) </span><br/>[`Transactions`](../../stores-purchase/transactions.md)<br/>`Braintree Virtual Terminal` |
| `Catalog` | [`Inventory`](../../inventory-management/introduction.md) | [`Products`](../../catalog/products-list.md)<br/>[`Categories`](../../catalog/categories.md)<br/>[`Shared Catalog`](../../b2b/catalog-shared-create.md) ![Adobe Commerce B2B](../../assets/b2b.svg) |
| `Customers` | [`All Customers`](../../customers/customers-all.md)<br/>[`Now Online`](../../customers/now-online.md)<br/>[`Customer Groups`](../../customers/customer-groups.md)<br/>[`Segments`](../../customers/customer-segments.md) ![Adobe Commerce](../../assets/adobe-logo.svg) <br/>[`Companies`](../../b2b/account-companies.md)![Adobe Commerce B2B](../../assets/b2b.svg) |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| `Marketing` | `Promotions` | [`Catalog Price Rule`](../../merchandising-promotions/price-rules-catalog.md) <br/>[`Cart Price Rules`](../../merchandising-promotions/price-rules-cart.md)) <br/>[`Related Products Rules`](../../merchandising-promotions/product-related-rules.md) ![Adobe Commerce](../../assets/adobe-logo.svg) <br/>[`Gift Card Accounts`](../../stores-purchase/product-gift-card-accounts.md) ![Adobe Commerce](../../assets/adobe-logo.svg) |
|                                                         | [`Private Sales`](../../merchandising-promotions/events-private-sales.md) ![Adobe Commerce](../../assets/adobe-logo.svg) | [`Events`](../../merchandising-promotions/event-configure.md) <br/>[`Invitations`](../../merchandising-promotions/invitations.md) |
|                                                         | `Communications` | [`Email Templates`](../../systems/email-templates.md) <br/>[`Newsletter Template`](../../merchandising-promotions/newsletter-template.md) <br/>[`Newsletter Queue`](../../merchandising-promotions/newsletter-queue.md) <br/>[`Newsletter Subscribers`](../../merchandising-promotions/newsletter-subscribers.md) <br/>[`Email Reminders`](../../merchandising-promotions/email-reminder-rules.md) ![Adobe Commerce](../../assets/adobe-logo.svg) |
|                                                         | `SEO & Search` | [`Search Terms`](../../catalog/search-terms.md) <br/>[`Search Synonyms`](../../catalog/search-terms.md#search-synonyms) ![Adobe Commerce](../../assets/adobe-logo.svg)<br/>[`URL Rewrites`](../../merchandising-promotions/url-rewrite.md) <br/>[`Site Map`](../../merchandising-promotions/sitemap-xml.md) |
|                                                         | [`User Content`](../../catalog/settings-advanced-product-reviews.md) | [`All Reviews`](../../catalog/settings-advanced-product-reviews.md) <br/>[`Pending Reviews`](../../merchandising-promotions/product-reviews-moderate.md) <br/> |
| `Content` | `Elements` | [`Pages`](../../content-design/pages.md)<br/>[`Hierarchy`](../../content-design/page-hierarchy.md) ![Adobe Commerce](../../assets/adobe-logo.svg)<br/>[`Blocks`](../../content-design/blocks.md)<br/>[`Dynamic Blocks`](../../content-design/dynamic-blocks.md) ![Adobe Commerce](../../assets/adobe-logo.svg)<br/>[`Widgets`](../../content-design/widgets.md)<br/>[`Media Gallery`](../../content-design/media-storage.md) |
|                                                         | `Design` | [`Configuration`](../../content-design/configuration.md)<br/>[`Themes`](../../content-design/themes.md)<br/>[`Schedule`](../../content-design/schedule.md) |
|                                                         | `Content Staging` ![Adobe Commerce](../../assets/adobe-logo.svg)<br /> | [대시보드](../../content-design/content-staging.md) |
| `Reports` | [`Marketing`](../../getting-started/marketing-reports.md) | `Products in Cart`<br />`Search Terms`<br />`Abandoned Carts`<br />`Newsletter Problem Reports` |
|                                                         | [`Reviews`](../../getting-started/review-reports.md) | `By Customer`<br/> `By Products`<br/> |
|                                                         | [`Sales`](../../getting-started/sales-reports.md) | `Orders`<br/>`Tax`<br/>`Invoiced`<br/>`Shipping`<br/>`Refunds`<br/>`Coupons`<br/>`PayPal Settlement`<br/>`Braintree Settlement` |
|                                                         | `System Insights` | [`Site-Wide Analysis Tool`](https://experienceleague.adobe.com/docs/commerce-operations/tools/site-wide-analysis-tool/access.html) ![Adobe Commerce](../../assets/adobe-logo.svg) |
|                                                         | [`Customers`](../../getting-started/customer-reports.md) | `Order Total`<br/>`Order Count`<br/>`New`<br/>`Wish Lists`<br/>`Segments`<br/> |
|                                                         | [`Products`](../../getting-started/product-reports.md) | `Views`<br/>`Bestsellers`<br/>`Low Stock`<br/>`Ordered`<br/>`Downloads` |
|                                                         | [`Private Sales`](../../getting-started/private-sales-reports.md) ![Adobe Commerce](../../assets/adobe-logo.svg) | `Invitations`<br/>`Invited Customers`<br/>`Conversions` |
|                                                         | `Statistics` | [`Refresh Statistics`](../../getting-started/sales-reports.md#refresh-statistics) |
|                                                         | [`Business Intelligence`](../../getting-started/business-intelligence.md) | `Advanced Reporting`<br/>`BI Essentials`<br/> |
|                                                         | `Customer Engagement` | `Dashboard`<br/>`Importer Status`<br/>`Automation Enrollment`<br/>`Campaign Sends`<br/>`SMS Sends`<br/>`Cron Tasks`<br/>`Log Viewer`<br/>`Abandoned Carts` |
| `Stores` | `Settings` | [`All Stores`](../../stores-purchase/stores.md)<br/>[`Configuration`](../../configuration-reference/guide-overview.md)<br/>[`Terms and Conditions`](../../stores-purchase/terms-and-conditions.md)<br/>[`Order Status`](../../stores-purchase/order-status.md) |
|                                                         | [`Inventory`](../../inventory-management/introduction.md) | [`Sources`](../../inventory-management/sources-stocks.md#sources)<br/>[`Stocks`](../../inventory-management/sources-stocks.md#stocks) |
|                                                         | [`Taxes`](../../stores-purchase/taxes.md) | [`Tax Rules`](../../stores-purchase/tax-rules.md)<br/>[`Tax Zones and Rates`](../../stores-purchase/tax-zones-rates.md) |
|                                                         | [`Currency`](../../stores-purchase/currency.md) | [`Currency Rates`](../../stores-purchase/currency-configuration.md)<br/>[`Currency Symbols`](../../stores-purchase/currency-configuration.md#step-5-customize-currency-symbols-optional) |
|                                                         | `Attributes` | [`Customer`](../../systems/data-attributes-customer.md)<br/>[`Customer Address`](../../systems/data-attributes-customer.md#customer-addresses)<br/>[`Product`](../../systems/data-attributes-product.md)<br/>[`Attribute Set`](../../catalog/attribute-sets.md)<br/>[`Returns`](../../stores-purchase/attributes-returns.md)<br/>[`Ratings`](../../merchandising-promotions/product-reviews.md#create-custom-ratings) |
|                                                         | `Other Settings` | [`Reward Exchange Rates`](../../merchandising-promotions/reward-exchange-rates.md)<br/>[`Gift Wrapping`](../../stores-purchase/cart-configuration.md#gift-wrap)<br/>[`Gift Registry`](../../merchandising-promotions/gift-registry-create.md) |
| `System` | [`Data Transfer`](../../systems/data-transfer.md) | [`Import`](../../systems/data-import.md)<br/>[`Export`](../../systems/data-export.md)<br/>[`Import/Export Tax Rates`](../../systems/data-transfer-tax-rates.md)<br/>[`Import History`](../../systems/data-import.md#import-history)<br/>[`Scheduled Import/Export`](../../systems/data-scheduled-import-export.md) |
|                                                         | `Extensions` | [`Integrations`](../../systems/integrations.md) |
|                                                         | `Tools` | [`Cache Management`](../../systems/cache-management.md)<br/>[`Index Management`](../../systems/index-management.md) |
|                                                         | `Support` | [`Data Collector`](../../systems/support.md#data-collector)<br/>[`System Report`](../../systems/support.md#system-reports) |
|                                                         | `Permissions` | [`All Users`](../../systems/permissions-users-all.md)<br/>[`Locked Users`](../../systems/permissions-users-all.md#locked-users)<br/>[`User Roles`](../../systems/permissions-user-roles.md) |
|                                                         | `Action Log` ![Adobe Commerce](../../assets/adobe-logo.svg) | [`Report`](../../systems/action-log.md)<br/>[`Archive`](../../systems/action-log-archive.md)<br/>[`Bulk Actions`](../../systems/action-log-bulk-actions.md) |
|                                                         | `Other Settings` | [`Notifications`](../../systems/notifications.md)<br/>[`Custom Variables`](../../systems/variables-custom.md)<br/>[`Manage Encryption Key`](../../systems/encryption-key.md) |
| `Find Partners & Extensions` |                                                                                                                                                                                                                                                                                                                                                                           |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |

{style="table-layout:auto"}

<!-- Feature still in development 
## [!UICONTROL Unified Experience]

![Store Configuration for Unified Experience](./assets/admin-uex-configuration.png)

The [!UICONTROL Unified Experience] option is available in Adobe Commerce deployments that have the Commerce Admin Unified Experience extension loaded. This extension enables integration with Experience Cloud to streamline cross-application workflows between Commerce and other Experience Cloud solutions. See [Adobe Experience Cloud Integration for Commerce Admin](../../getting-started/admin-unified-experience-integration-overview.md).

| Field        | [Scope](../../getting-started/websites-stores-views.md#scope-settings) | Description                                                                                                                                                                                                                                                                                                                                                                    |
|--------------|------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Enable       | Global                                                                 | Determines if the Commerce instance uses the Experience Cloud integration. Before enabling this feature, review the [requirements and configuration instructions](../../getting-started/admin-unified-experience-integration-overview.md). Options: Yes/No.                                                                                                                    |
| Project Name | Global                                                                 | Identifies the instance in the Experience Cloud Commerce Projects workspace when the Unified Experience is enabled. The name can contain only alphanumeric characters and spaces. Defaults to the [cloud environment name](https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/architecture/pro-architecture.html?lang=en#pro-environment-architecture). |

{style="table-layout:auto"}

-->

## [!UICONTROL Admin Base URL]

![관리자 기본 URL](./assets/admin-admin-base-url.png)<!-- zoom -->

이러한 옵션 설정에 대한 자세한 내용은 _저장 및 구매 경험 안내서_&#x200B;에서 [기본 URL 구성](../../stores-purchase/store-urls.md#configure-the-base-url)을 참조하십시오.

| 필드 | [범위](../../getting-started/websites-stores-views.md#scope-settings) | 설명 |
|------------------------------------|------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Use Custom Admin URL] | 글로벌 | 사용자 지정 URL을 사용하여 관리자에 액세스할지 여부를 결정합니다. 옵션: `Yes` / `No` |
| [!UICONTROL Custom Admin URL] | 글로벌 | 관리자에 액세스할 사용자 지정 URL을 지정합니다. 기본적으로 관리자 URL은 기본 URL과 동일합니다.<br/>**중요:** 관리자 URL은 동일한 Commerce 설치에 있어야 하며 상점 이름과 문서 루트가 같아야 합니다. |
| [!UICONTROL Use Custom Admin Path] | 글로벌 | 사용자 지정 경로를 사용하여 관리자에 액세스하는지 여부를 결정합니다. 기본 경로는 `admin`입니다. 옵션: `Yes` / `No` |
| [!UICONTROL Custom Admin Path] | 글로벌 | 기본 관리 경로의 이름을 짐작하기 어려운 이름으로 변경합니다. 사용자 정의 경로 이름을 소문자로 입력합니다. 예: `aardvark` |

{style="table-layout:auto"}

## [!UICONTROL Security]

![보안](./assets/admin-security.png)<!-- zoom -->

이러한 옵션 설정에 대한 자세한 내용은 _관리 시스템 안내서_&#x200B;에서 [관리 보안 구성](../../systems/security-admin.md)을 참조하십시오.

| 필드 | [범위](../../getting-started/websites-stores-views.md#scope-settings) | 설명 |
|--------------------------------------------------------|------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Admin Account Sharing] | 스토어 뷰 | 관리자 사용자가 다른 장치에서 동일한 계정에 동시에 로그인할 수 있는지 여부를 결정합니다. 옵션: <br/>**`Yes`**- 동일한 관리자 계정의 여러 활성 세션을 허용합니다.<br/>**`No`** - 관리자 계정당 하나의 활성 세션만 허용합니다. |
| [!UICONTROL Password Reset Protection Type] | 스토어 뷰 | 암호 재설정 요청을 관리하는 데 사용할 방법을 결정합니다. 옵션: <br/>**`By IP and Email`**- 알림에서 응답을 받은 후 관리자 계정과 연결된 전자 메일 주소로 암호를 다시 설정할 수 있습니다.<br/>**`By IP`** - 추가 확인 없이 암호를 온라인으로 다시 설정할 수 있습니다. <br/>**`By Email`**- 관리자 계정과 연결된 전자 메일 주소로 전송된 알림에 전자 메일을 통해서만 암호를 재설정할 수 있습니다.<br/>**`None`** - 암호는 저장소 관리자만 재설정할 수 있습니다. |
| [!UICONTROL Recovery Link Expiration Period (hours)] | 글로벌 | 암호 복구 링크가 유효한 상태로 유지되는 시간을 결정합니다. |
| [!UICONTROL Max Number of Password Reset Requests] | 스토어 뷰 | 시간당 제출할 수 있는 최대 암호 요청 수를 결정합니다. |
| [!UICONTROL Min Time Between Password Reset Requests] | 스토어 뷰 | 암호 재설정 요청 사이의 최소 시간(분)을 결정합니다. |
| [!UICONTROL Add Secret Key to URLs] | 글로벌 | 활성화되면 는 악용에 대한 대비책으로 관리자 URL에 비밀 키를 추가합니다. 옵션: `Yes` / `No` |
| [!UICONTROL Login Is Case Sensitive] | 글로벌 | 사용자가 입력한 로그인 자격 증명이 저장된 로그인 자격 증명과 일치해야 하는지 여부를 결정합니다. 옵션: `Yes` / `No` |
| [!UICONTROL Admin Session Lifetime (seconds)] | 글로벌 | 관리 세션의 길이(초)를 결정합니다. |
| [!UICONTROL Maximum Login Failures to Lockout Account] | 글로벌 | 계정이 잠기기 전에 관리자가 로그인을 시도할 수 있는 횟수를 결정합니다. 필드가 비어 있으면 최소값이 설정되지 않습니다. 기본값: `6` |
| [!UICONTROL Lockout Time (minutes)] | 글로벌 | 사용자가 다시 로그인을 시도하기 전에 관리자 계정이 잠기는 시간(분)을 결정합니다. 기본값: `30` |
| [!UICONTROL Password Lifetime (days)] | 글로벌 | 관리자 암호가 만료될 때까지 남은 일 수를 결정합니다. 필드가 비어 있으면 라이프타임이 설정되지 않습니다. 기본값: `90` |
| [!UICONTROL Password Change] | 글로벌 | 관리자 사용자가 암호를 변경해야 하는지 여부를 결정합니다. 옵션: <br/>**`Forced`**- 계정을 설정한 후 관리자 사용자가 암호를 변경해야 합니다.<br/>**`Recommended`** - 계정을 설정한 후 관리자 사용자가 암호를 변경할 것을 권장합니다. |

{style="table-layout:auto"}

## [!UICONTROL Dashboard]

![대시보드](./assets/admin-dashboard.png)<!-- zoom -->

이러한 옵션 설정에 대한 자세한 내용은 _시작 안내서_&#x200B;의 [관리 대시보드](../../getting-started/admin-dashboard.md)를 참조하십시오.

| 필드 | [범위](../../getting-started/websites-stores-views.md#scope-settings) | 설명 |
|----------------------------|------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------|
| [!UICONTROL Enable Charts] | 글로벌 | 대시보드에 현재 판매 데이터에서 생성된 차트가 포함되어 있는지 여부를 결정합니다. 옵션: `Yes` / `No` |

{style="table-layout:auto"}

## [!UICONTROL Admin Grids]

![관리 그리드](./assets/admin-admin-grids.png)<!-- zoom -->

이러한 옵션 설정에 대한 자세한 내용은 _카탈로그 관리 가이드_&#x200B;의 [제품 표시 제한](../../catalog/products-list.md#limit-product-display)을 참조하세요.

>[!NOTE]
>
>큰 카탈로그의 성능을 개선하려면 그리드에 표시되는 제품 수를 제한하는 것이 좋습니다.

| 필드 | [범위](../../getting-started/websites-stores-views.md#scope-settings) | 설명 |
|-----------------------------------------------|------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Limit Number of Products in Grid] | 글로벌 | 격자에 표시되는 제품 수가 _[!UICONTROL Records Limit]_값으로 제한되는지 여부를 결정합니다. 옵션: `Yes` / `No` |
| [!UICONTROL Records Limit] | 글로벌 | 제품 격자에 있는 제품의 수 제한을 설정합니다. 기본 최소값은 `20000`입니다. |

## [!UICONTROL CAPTCHA]

![CAPTCHA](./assets/admin-captcha.png)<!-- zoom -->

이러한 옵션 설정에 대한 자세한 내용은 _관리 시스템 안내서_&#x200B;의 [CAPTCHA](../../systems/security-captcha.md)을(를) 참조하십시오.

| 필드 | [범위](../../getting-started/websites-stores-views.md#scope-settings) | 설명 |
|-------------------------------------------------------|------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Enable CAPTCHA in Admin] | 글로벌 | 관리자 로그인에 CAPTCHA를 사용합니다. 옵션: `Yes` / `No` |
| [!UICONTROL Font] | 글로벌 | CAPTCHA를 표시하는 데 사용할 글꼴을 결정합니다. 고유한 글꼴을 추가하려면 글꼴 파일을 Commerce 인스턴스와 동일한 디렉터리에 넣고 `app/code/Magento/Captcha/etc`의 config.xml 파일에 선언을 추가합니다. 기본 글꼴:` LinLibertine` |
| [!UICONTROL Forms] | 글로벌 | CAPTCHA가 사용되는 양식을 결정합니다. 옵션: `Admin Login` / `Admin Forgot Password` |
| [!UICONTROL Displaying Mode] | 글로벌 | CAPTCHA가 표시되는 시기를 결정합니다. 옵션: <br/>**`Always`**- 로그인하려면 항상 CAPTCHA가 필요합니다.<br/>**`After number of attempts to login`** - [!UICONTROL Number of Unsuccessful Attempts to Login] 필드를 표시합니다. 허용된 로그인 시도 횟수를 입력합니다. 값이 0(영)이면 표시 모드를 항상 로 설정하는 것과 비슷합니다. 이 옵션은 암호 분실 및 사용자 양식 만들기에 대해서는 다루지 않습니다. CAPTCHA가 활성화되어 있고 나타나도록 설정된 경우 폼에 항상 포함됩니다.<br />**참고**: 실패한 로그인 시도 횟수를 추적하기 위해 하나의 전자 메일 주소와 하나의 IP 주소에서 로그인을 시도한 횟수가 계산됩니다. 동일한 IP 주소에서 허용되는 최대 로그인 시도 횟수는 1,000회입니다. 이 제한은 CAPTCHA가 활성화된 경우에만 적용됩니다. |
| [!UICONTROL Number of Unsuccessful Attempts to Login] | 글로벌 | 계정이 잠기기 전에 사용자가 로그인을 시도할 수 있는 횟수를 결정합니다. 실패한 로그인 시도 횟수를 추적하기 위해 시스템은 단일 IP 주소의 한 이메일 주소에서 시도 횟수를 추적합니다. 동일한 IP 주소에서 허용되는 최대 시도 횟수는 1,000회입니다. 이 제한은 CAPTCHA가 활성화된 경우에만 적용됩니다. |
| [!UICONTROL CAPTCHA Timeout (minutes)] | 글로벌 | 현재 CAPTCHA의 수명을 결정합니다. CAPTCHA가 만료되면 사용자는 페이지를 다시 로드해야 합니다. |
| [!UICONTROL Number of Symbols] | 글로벌 | CAPTCHA에 사용되는 기호의 수를 결정합니다. 허용되는 최대값은 `8`입니다. 범위를 지정할 수도 있습니다(예: `5-8`). |
| [!UICONTROL Symbols Used in CAPTCHA] | 글로벌 | CAPTCHA에 사용할 기호를 결정합니다. 문자(a-z 및 A-Z)와 숫자(0-9)만 허용됩니다. 필드에 제안된 기본 기호 집합은 i, l 또는 1과 같이 비슷한 모양의 기호를 제외합니다. CAPTCHA에 이러한 기호를 표시하면 사용자가 CAPTCHA를 올바르게 인식할 가능성이 줄어듭니다. |
| [!UICONTROL Case Sensitive] | 글로벌 | CAPTCHA에 사용되는 문자가 대소문자를 구분하는지 여부를 결정합니다. 옵션: `Yes` / `No` |

{style="table-layout:auto"}

## [!UICONTROL Admin Actions Logging]

{{ee-feature}}

![관리자 작업 로깅](./assets/admin-actions-logging.png)<!-- zoom -->

이러한 옵션 설정에 대한 자세한 내용은 _관리 시스템 안내서_&#x200B;의 [작업 로그 보관](../../systems/action-log-archive.md)을 참조하십시오.

| 필드 | [범위](../../getting-started/websites-stores-views.md#scope-settings) | 설명 |
|-----------------------------|------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Enable Actions] | 글로벌 | 선택한 각 작업에 대해 작업 로깅을 활성화합니다. <br/>`Admin My Account` <br/>`Admin Permission Roles` <br/>`Admin Permission Users` <br/>`Admin Sign In` <br/>`CMS Blocks` <br/>`CMS Hierarchy` <br/>`CMS Pages` <br/>`Cache Management` <br/>`Cart Price Rules` <br/>`Catalog Attributes` <br/>`Catalog Categories` <br/>`Catalog Events` <br/>`Catalog Price Rules` <br/>`Catalog Product Tax Classes` <br/>`Catalog Product Templates` <br/>`Catalog Products` <br/>`Catalog Ratings` <br/>`Catalog Reviews` <br/>`Catalog Search` <br/>`Checkout Terms and Conditions` <br/>`Companies` <br/>`Company Credit` <br/>`Custom Variables` <br/>`Customer Groups` <br/>`Customer Invitations` <br/>`Customer Tax Classes` <br/>`Customers` <br/>`Design Configuration` <br/>`Gift Card Accounts` <br/>`Gift Registry Entity` <br/>`Gift Registry Type` <br/>`Index Management` <br/>`Login as a Customer` <br/>`Manage Currency Rates` <br/>`Manage Customer Address Attributes` <br/>`Manage Customer Attributes` <br/>`Manage Design` <br/>`Manage Dynamic Blocks` <br/>`Manage Segments` <br/>`Manage Store Views` <br/>`Manage Stores` <br/>`Manage Websites`} <br/>`Negotiable Quotes` <br/>`Newsletter Queue` <br/>`Newsletter Subscribers` <br/>`Newsletter Templates` <br/>`PayPal Settlement Reports` <br/>`Reports` <br/> `Reward Points Rates` <br/>`Rule-Based Product Relations` <br/>`Sales Archive` <br/>`Sales Credit Memos` <br/>`Sales Invoices` <br/>`Sales Order Status` <br/>`Sales Orders` <br/>`Sales Shipments` <br/>`Shared Catalog` <br/>`Shopping Cart Management` <br/>`Store Credit` <br/>`System Backups` <br/>`System Configuration` <br/>`Tax Rates` <br/>`Tax Rules` <br/>`Transactional Emails` <br/>`URL Rewrites` <br/>`Widget` <br/>`XML Sitemap` |

{style="table-layout:auto"}

## [!UICONTROL Admin Usage]

![관리자 사용](./assets/admin-usage.png)<!-- zoom -->

이러한 옵션 설정에 대한 자세한 내용은 _시작 안내서_&#x200B;에서 [사용 데이터 수집](../../getting-started/admin.md#usage-data-collection)을(를) 참조하십시오.

| 필드 | 범위 | 설명 |
|------------------------------------------|--------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Enable Admin Usage Tracking] | 글로벌 | _관리자_, 관련 제품 및 서비스 사용 환경을 개선하기 위해 Adobe이 관리자 사용 데이터를 수집할 수 있는 권한을 부여합니다. 데이터 수집을 허용하면 도움말, 도구 설명, 안내 안내서, 온보딩 정보, 기능 공지 등과 같은 대화형 콘텐츠를 _관리자_&#x200B;에게 전달하도록 설계된 _제품 내 지침_&#x200B;도 사용할 수 있습니다. 사용 데이터에서 개별 관리자를 식별할 수 없습니다. 옵션:<br />**`Yes`**- 데이터 수집을 허용하고 _제품 내 지침_을 사용하도록 설정합니다.<br />**`No`** - 데이터 수집을 허용하지 않으며 _제품 내 지침_&#x200B;을 사용하도록 설정하지 않습니다. |

{style="table-layout:auto"}
