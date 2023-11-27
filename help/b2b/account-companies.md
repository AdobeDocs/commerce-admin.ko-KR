---
title: 회사 계정
description: Adobe Commerce 스토어에서 관리하는 회사 계정을 통해 동일한 회사에 속하는 여러 구매자를 단일 회사 계정에 연결할 수 있는 방법을 알아봅니다.
exl-id: 0b3c3635-a1cf-4ee6-a8bc-e7cbcb4e2e63
feature: B2B, Companies, Configuration
source-git-commit: c94d4e8d13c32c1c1b1d37440fdb953c8527b76c
workflow-type: tm+mt
source-wordcount: '752'
ht-degree: 0%

---

# 회사 계정

스토어에 B2B 회사 계정을 통합할 때, 회사에서 조직의 사용자 역할에 따라 유연한 권한으로 여러 하위 계정을 만들 수 있으므로 기업 쇼핑 경험을 단순화할 수 있습니다. 기업에 따라 매장 관리자는 판촉 행사 및 가격을 자신의 요구에 맞게 조정할 수 있으며, 쇼핑객의 요구에 맞는 고도로 맞춤화된 오퍼를 만들고 주문을 늘릴 수 있습니다. 표준에 회사 계정 연결 추가 [개인](../customers/account-create.md) 고객이 회사에 대해 정의된 특정 구매 워크플로우를 사용할 수 있도록 허용합니다.

회사 계정의 장점:

- 무제한 제공 [회사 사용자](account-company-users.md) 또한 추가 계정을 생성하여 기업 구매를 간소화합니다.

- 에 대한 지원 포함 _스마트_ 다른 회사 계정 계층 [역할 및 권한](account-company-roles-permissions.md) 주문.

- 상인이 공모를 통해 소득을 높일 수 있는 메커니즘을 제공한다 [회사 스토어 크레딧](credit-company.md) 결제 수단으로 사용됩니다.

- 지원 [관리](account-company-manage.md) 을(를) 통해 관리됩니다.

## 회사 계정 보기

다음 _회사_ 상태 설정에 관계없이 그리드에 모든 활성 회사 계정 및 보류 중인 요청이 나열됩니다. 또한 다음을 위한 도구를 제공합니다. [생성 중](account-company-create.md) 및 [관리](account-company-manage.md) 회사 계정입니다. 표준 격자 컨트롤을 사용하여 목록을 필터링하고 열 레이아웃을 조정합니다. 열 설명 목록은 _열 설명_ 의 섹션 [회사 계정 관리](account-company-manage.md).

고객은 상점에서 회사 계정을 만들거나 상인은 관리에서 회사 계정을 만들 수 있습니다. 기본적으로 상점 첫 화면에서 회사 계정을 만들 수 있습니다. 구성에서 허용하는 경우 스토어 방문자는 회사 계정 열기를 요청할 수 있습니다. 회사 계정이 승인되면 회사 관리자는 회사 구조 및 사용자를 다양한 수준의 권한으로 설정할 수 있습니다.

다음에서 _관리자_ 사이드바, 이동 **[!UICONTROL Customers]** > **[!UICONTROL Companies]**.

![회사 그리드](./assets/companies-grid.png){width="700" zoomable="yes"}

다음 [!UICONTROL Companies] 그리드 에는 상태와 관계없이 모든 회사가 나열됩니다. 표시된 예에서는 &quot;ACME&quot; 회사와 &quot;Vandelay&quot; 회사, 이렇게 두 회사의 계정을 보여 줍니다.

## 회사 관리자

다음 예제는 _고객_ 초기 회사 관리자 계정으로 구분합니다.

![회사 관리자 계정으로 고객 그리드](./assets/company-admin-user-account.png){width="700" zoomable="yes"}

회사 관리자로서 역할을 수행하는 사람이 회사 내에서 여러 역할을 하게 될 가능성이 있다. 회사 관리자에 대해 별도의 이메일 주소를 입력하면 초기 회사 구조에 회사 관리자와 회사 관리자 이름에 개별 사용자 계정이 포함됩니다. 이러한 경우 회사 관리자는 회사 또는 개인 사용자로 계정에 로그인할 수 있습니다.

계정을 만든 후 회사 관리자는 의 회사 구조를 정의합니다 [팀](account-company-structure.md), 를 설정합니다. [회사 사용자](account-company-users.md), 및 설정 [역할 및 권한](account-company-roles-permissions.md) 각.

### 처음 로그인하기 전에 회사 관리자 암호 설정

1. 회사 관리자가 스토어에서 시작 이메일을 찾습니다.

   ![시작 이메일 예](./assets/company-admin-welcome-email.png){width="500"}

   >[!NOTE]
   >
   >전자 메일 주소 대상 및 전자 메일의 콘텐츠는 [회사 이메일 옵션](email-company-configuration.md) 구성.

1. 지침 및 클릭을 따릅니다. [!UICONTROL **링크**] 암호를 설정합니다.

1. 을(를) 입력합니다 [!UICONTROL **새 암호**] 계정 및 다시 확인을 위해.

   암호에는 다음 문자 유형 중 최소 세 가지 이상이 포함되어야 합니다.

   - 소문자(abc...)
   - 대문자(ABC...)
   - 숫자(1234567890)
   - 특수 문자(!@#$...)

1. 클릭수 [!UICONTROL **새 암호 설정**].

   ![고객 로그인 - 회사 관리자](./assets/company-admin-account-login.png){width="700" zoomable="yes"}

1. 다음의 경우 [!UICONTROL Customer Login] 페이지가 나타나고 고객이 을 입력합니다 [!UICONTROL **이메일**] 및 [!UICONTROL **암호**].

1. 클릭수 [!UICONTROL **로그인**] 계정 대시보드에 액세스합니다.

   ![계정 대시보드 - 회사](./assets/account-dashboard-company.png){width="700" zoomable="yes"}

## 회사 구조

비즈니스 구조를 반영하도록 회사 계정을 설정할 수 있습니다. 처음에는 회사 구조에 회사 관리자만 포함되지만 사용자 팀을 포함하도록 확장할 수 있습니다. 사용자는 팀과 연결되거나 회사 내 부서 및 하위 부서의 계층 구조로 구성될 수 있습니다. 이 구조는 의 사용을 지원하도록 설계되었습니다. [승인 규칙](account-dashboard-approval-rules.md) 대상 [구매 주문](purchase-order-flow.md) 회사 계정과 연계된 PO.

![사업부가 있는 회사 구조](./assets/company-structure-diagram.svg){width="450"}

회사 관리자의 계정 대시보드에서 회사 구조는 트리로 표시되며 처음에는 회사 관리자로만 구성됩니다.

![회사 관리자가 있는 회사 구조](./assets/company-structure-tree-admin.png){width="600"}

계정이 만들어지면 회사 관리자는 회사 이메일 주소를 사용하거나 다른 이메일 주소를 할당할 수 있습니다.

다음 예에서는 초기 회사 구조에 회사 관리자와 회사 관리자 이름의 개별 사용자 계정이 포함됩니다. 그러나 회사 관리자 기능(예: 회사 구조 및 승인 규칙)은 회사 관리자로 지정된 사용자 계정에 로그인해야 사용할 수 있습니다.

![관리자 및 사용자 계정이 있는 회사 구조](./assets/company-structure-tree-admin-user.png){width="600"}
