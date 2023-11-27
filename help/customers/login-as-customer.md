---
title: 쇼핑객 지원 제공
description: 고객으로 로그인 기능을 사용하면 고객이 본 내용을 확인하고 고객을 대신하여 업데이트할 수 있습니다.
exl-id: 6842ae7a-6440-45f1-af18-e6427088d29d
feature: Customers, Customer Service
source-git-commit: 7de285d4cd1e25ec890f1efff9ea7bdf2f0a9144
workflow-type: tm+mt
source-wordcount: '587'
ht-degree: 0%

---

# 쇼핑객 지원 제공

고객은 때때로 주문에 대한 도움이 필요합니다. 스토어 관리자는 _고객으로 로그인_&#x200B;를 통해 고객이 보는 것을 확인하고 업데이트를 하여 고객 지원을 받을 수 있습니다.

고객으로 로그인된 상태에서 수행한 모든 작업은 실제 고객의 계정에 적용됩니다.

다음에 대해 활성화될 때 _관리자_ 사용자, _[!UICONTROL Login as Customer]_단추가 여러 페이지에 표시됩니다.

* [고객 편집 페이지](../customers/update-account.md)
* [주문 보기 페이지](../stores-purchase/order-processing.md)
* [송장 보기 페이지](../stores-purchase/invoices.md)
* [배송 조회 페이지](../stores-purchase/shipments.md)
* [대변 메모 보기 페이지](../stores-purchase/credit-memo-create.md)

![고객으로 로그인](assets/login-as-customer.png){width="600" zoomable="yes"}

## 고객으로 로그인 활성화

활성화 중 _고객으로 로그인_ 를 사용하려면 Commerce 인스턴스에서 기능을 활성화한 다음 사용자 역할 권한에서 관리자 사용자에 대한 액세스를 활성화해야 합니다.

### 기능 활성화

1. 관리 사이드바에서 다음 위치로 이동하십시오.  **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. 왼쪽 패널에서 를 확장합니다. **[!UICONTROL Customers]** 및 선택  **[!UICONTROL Login as Customer]**.

   ![구성 옵션 - 고객으로 로그인](../configuration-reference/customers/assets/login-as-customer.png){width="600" zoomable="yes"}

1. 설정 **[!UICONTROL Enable Login as Customer]** 끝 `Yes`.

1. _(선택 사항)_ 설정 **[!UICONTROL Disable Page Cache for Admin User]** 끝 `No` 관리자 사용자가 고객으로 로그인할 때 페이지 캐시를 활성화합니다.

   >[!WARNING]
   >
   > 페이지 캐시 비활성화(`Yes` - 기본값) 고객으로 로그인하는 사용자가 캐시되지 않은 새 데이터를 가져오도록 합니다.

1. _(선택 사항)_ 설정 **[!UICONTROL Store View to Log in]** 끝 `Manual Selection` 다중 사이트 및/또는 다중 스토어 설정이 있고 관리자로 로그인할 때 관리자가 스토어 보기를 선택하게 하려는 경우.

1. 완료되면 다음을 클릭하십시오. **[!UICONTROL Save Config]**.

### 관리 사용자에 대한 액세스 활성화

1. 다음에서 _관리자_ 사이드바, 이동 **[!UICONTROL System]** > _권한_ > **[!UICONTROL User Roles]**.

1. 목록에서 역할을 클릭합니다.

1. 다음에서 [!UICONTROL _역할 정보_] 왼쪽 패널에서 클릭 **[!UICONTROL Role Resources]**.

1. 변경 **[!UICONTROL Role Resources]** (으)로 이동 `Custom`.

   >[!INFO]
   >
   > 이 옵션을 선택하면 페이지에 리소스 계층 구조가 표시됩니다.

1. 다음으로 스크롤  **[!UICONTROL Customers]** 상위 항목 및 **[!UICONTROL Login as Customer]** 항목 아래에 있습니다. 그런 다음 역할에 대해 활성화할 리소스를 선택합니다.

   * **[!UICONTROL Allow Login as Customer]** - 관리자 사용자가 _고객으로 로그인_ 기능.
   * **[!UICONTROL View Login as Customer Log]** - 관리 사용자가 다음을 볼 수 있습니다. _고객으로 로그인_ 로그합니다.

   ![역할 리소스 - 고객으로 로그인](assets/customers-login-as-customer-role-resources.png){width="400" zoomable="yes"}

1. 클릭 **[!UICONTROL Save Role]**.

## 관리자에서 고객으로 로그인

1. 다음에서 _관리자_ 사이드바, 이동 **[!UICONTROL Customers]** > [!UICONTROL _모든 고객_].

1. 편집 모드에서 사용자를 엽니다.

1. 다음에서 **[!UICONTROL Customer Information]** 패널, 선택 **[!UICONTROL Account Information]** 섹션.

1. 설정 **[!UICONTROL Allow remote shopping assistance]** 끝 `Yes`.

   >[!INFO]
   >
   >이제 관리자는 상점 첫 화면에서 권한 없이 사용자로 로그인할 수 있습니다.

## 원격 쇼핑 지원을 위한 고객 계정 권한

관리자의 스토어 지원 직원에 대한 계정 액세스를 활성화하려면 고객은 자신의 계정에 대해 기능을 활성화해야 합니다.

1. 고객이 다음으로 이동 **[!UICONTROL Account Information]** 페이지를 가리키도록 업데이트하는 중입니다.

1. 다음을 선택합니다. **[!UICONTROL Allow remote shopping assistance]** 확인란.

1. 고객이 클릭 **[!UICONTROL Save]**.

![계정 정보 페이지](assets/permission.png){width="700" zoomable="yes"}

>[!WARNING]
>
>이 권한이 없으면 관리자 사용자는 이 고객으로 로그인할 수 없습니다.

## 고객으로 로그인 사용

>[!INFO]
>
>사용 _고객으로 로그인_, 관리자가 앞에서 설명한 대로 구성되었는지 확인합니다.

_고객으로 로그인_ 을 사용하면 고객과 마찬가지로 사이트를 볼 수 있으며 문제를 해결하고 고객을 위해 다른 조치를 취할 수 있습니다. 필요한 권한이 있는 할당된 사용자 역할이 있는 경우:

1. 다음을 클릭할 수 있습니다. **[!UICONTROL Login as Customer]** 이전 섹션에 나열된 페이지에서 참조할 수 있습니다.
1. 고객으로 로그인 작업은 작업 보고서에서 사용할 수 있습니다.

>[!WARNING]
>
>로그인 중 수행한 모든 작업 [!UICONTROL _고객으로_] (예: 제품 추가/제거)는 실제 고객의 주문에 적용됩니다. 가게 앞에는 다음과 같은 경우에 배너가 표시됩니다. `logged in as customer_name` 특별 상태를 상기시키다.

## 고객 로그인으로 로그인

{{ee-feature}}

Adobe Commerce은에 대한 로깅을 제공합니다. _고객으로 로그인_ 작업. 이 목록에는 관리 사용자가 기능에 액세스하는 모든 세션이 나열됩니다. 기록된 작업에 액세스하려면 다음으로 이동합니다. [관리자 작업 보고서](../systems/action-log-report.md).

보고서 설정을 필터링할 수 있습니다 **[!UICONTROL Action Group]** 끝 `Login As Customer` 페이지 맨 위에서 **[!UICONTROL Search]**.

![작업 보고서 필터링](assets/customers-login-as-customer-log-filter.png){width="700" zoomable="yes"}
