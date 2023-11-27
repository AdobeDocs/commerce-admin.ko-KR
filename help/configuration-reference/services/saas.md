---
title: '[!UICONTROL Services] &gt; [!UICONTROL Commerce Services Connector]'
description: 에서 구성 설정을 검토합니다. [!UICONTROL Services] &gt; [!UICONTROL Commerce Services Connector] 상거래 관리자의 페이지입니다.
exl-id: 3570e846-c8ab-4a36-b020-1b536bbd377d
feature: Configuration, Saas
source-git-commit: 76bd1b1af9b55d69bd98209d70fb5518f190a3e1
workflow-type: tm+mt
source-wordcount: '222'
ht-degree: 1%

---

# [!UICONTROL Services] > [!UICONTROL Commerce Services Connector]

스토어를 Adobe Commerce 서비스에 연결하는 방법은 다음을 참조하십시오. [상거래 서비스](https://experienceleague.adobe.com/docs/commerce-merchant-services/user-guides/integration-services/saas.html).

{{config}}

## [!UICONTROL Sandbox API Keys]

![샌드박스 API 키](./assets/sandbox-key-saas-configuration.png)<!-- zoom -->

| 필드 | [범위](../../getting-started/websites-stores-views.md#scope-settings) | 설명 |
|--- |--- |--- |
| [!UICONTROL Sandbox public API key] | 글로벌 | 작성자 및 해당 권한(있는 경우)을 식별하는 API 키. |
| [!UICONTROL Sandbox private API key] | 글로벌 | API 키와 연결된 개인 키. |

{:style=&quot;table-layout:auto&quot;}

## [!UICONTROL Production Keys]

![프로덕션 API 키](./assets/prod-key-saas-configuration.png)<!-- zoom -->

| 필드 | [범위](../../getting-started/websites-stores-views.md#scope-settings) | 설명 |
|--- |--- |--- |
| [!UICONTROL Production public API key] | 글로벌 | 작성자 및 해당 권한(있는 경우)을 식별하는 API 키. |
| [!UICONTROL Production private API key] | 글로벌 | API 키와 연결된 개인 키. |

{:style=&quot;table-layout:auto&quot;}

## [!UICONTROL SaaS Identifier]

![SaaS 식별자](./assets/saas-identifier.png)<!-- zoom -->

| 필드 | [범위](../../getting-started/websites-stores-views.md#scope-settings) | 설명 |
|--- |--- |--- |
| [!UICONTROL Project] | 글로벌 | 모든 SaaS 데이터 공간을 그룹화하는 SaaS 프로젝트의 이름입니다. A _프로젝트 만들기_ SaaS 프로젝트가 없는 경우 버튼이 표시됩니다. |
| [!UICONTROL Data Space] | 글로벌 | 지정된 SaaS 프로젝트의 SaaS 데이터 공간을 나열합니다. SaaS 데이터 공간 수는 다음에 따라 다릅니다. [상거래 라이선스](https://experienceleague.adobe.com/docs/commerce-merchant-services/user-guides/integration-services/saas.html):<br />Adobe Commerce - 프로덕션 데이터 공간 1개, 테스트 데이터 공간 2개,<br />Magento Open Source - 프로덕션 데이터 공간 1개, 테스트 데이터 공간 없음 |

{:style=&quot;table-layout:auto&quot;}

## [!UICONTROL IMS Organization]

![IMS 조직](./assets/ims-organization.png)<!-- zoom -->

| 필드 | 설명 |
|--- |--- |
| [!UICONTROL Sign in using Adobe ID] | Adobe ID은 일반적으로 멤버십을 시작하거나 Adobe 애플리케이션 또는 서비스를 구매할 때 처음 사용한 이메일 주소입니다. Adobe ID은 Adobe 계정에 액세스하는 데 필요한 키입니다. |

{:style=&quot;table-layout:auto&quot;}
