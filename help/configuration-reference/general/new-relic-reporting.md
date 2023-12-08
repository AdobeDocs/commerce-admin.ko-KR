---
title: '[!UICONTROL General] &gt; [!UICONTROL New Relic Reporting]'
description: 에서 구성 설정을 검토합니다. [!UICONTROL General] &gt; [!UICONTROL New Relic Reporting] 상거래 관리자의 페이지입니다.
exl-id: d6bf4810-81a3-420d-abc9-9b87c1e92551
feature: Configuration, System, Reporting
source-git-commit: 1aec5c618d1f3f7f083523956d2aee62b777faca
workflow-type: tm+mt
source-wordcount: '241'
ht-degree: 0%

---

# [!UICONTROL General] > [!UICONTROL New Relic Reporting]

{{config}}

>[!NOTE]
>이러한 구성 옵션은 클라우드 인프라의 Adobe Commerce에는 적용되지 않습니다.
>
>Pro 플랜을 사용하는 경우 New Relic은 이미 [사전 구성되어 있고 기본적으로 활성화되어 있습니다.](https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/monitor/new-relic/new-relic-service.html). Starter 플랜에 속해 있는 경우 다음을 완료해야 합니다. [New Relic 구성 단계](https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/monitor/new-relic/account-management.html#configure-new-relic-for-starter-environment) 설정 프로세스의 일부입니다.

## [!UICONTROL General]

![일반](./assets/new-relic-reporting-general.png)<!-- zoom -->

<!-- [General](https://docs.magento.com/user-guide/reports/new-relic-reporting.html) -->

| 필드 | [범위](../../getting-started/websites-stores-views.md#scope-settings) | 설명 |
|--- |--- |--- |
| [!UICONTROL Enable New Relic Integration] | 스토어 뷰 | 스토어를 와 함께 사용할 수 있는지 확인합니다. [!DNL New Relic] 보고. 옵션: `Yes` / `No` |
| [!UICONTROL New Relic API URL] | 스토어 뷰 | New Relic API가 배포되는 URL입니다. 예: `https://api.newrelic.com/deployments.xml` |
| Insights API URL | 스토어 뷰 | Insights API가 배포되는 URL입니다. 퍼센트 기호(%)를 사용하여 계정 ID를 나타냅니다. 예: `https://insights-collector.newrelic.com/v1/accounts/%s/events` |
| [!UICONTROL New Relic Account ID] | 스토어 뷰 | 에 할당된 계정 ID [!DNL New Relic] 계정입니다. |
| [!UICONTROL New Relic Application ID] | 스토어 뷰 | 에 할당된 애플리케이션 ID [!DNL New Relic] commerce 통합을 위한 계정입니다. |
| [!UICONTROL New Relic API Key] | 스토어 뷰 | 에 대한 액세스 권한을 얻기 위해 사용자에게 할당된 키 [!DNL New Relic] API. |
| [!UICONTROL Insights API Key] | 스토어 뷰 | Insights에 액세스하기 위해 사용자에게 할당된 키입니다. |
| [!UICONTROL New Relic Application Name] | 스토어 뷰 | 에 할당한 이름 [!DNL New Relic] 통합. |
| [!UICONTROL Send Adminhtml and Frontend as Separate Apps] | 스토어 뷰 | 상점 및 관리자를 위해 수집된 보고서 데이터를 별도의 앱으로 New Relic에 전송하는 옵션입니다. 이 옵션을 사용하려면 다음에 대해 입력한 이름이 필요합니다. [!UICONTROL New Relic Application Name]. 이 기능은 수집된 앱 데이터에 밑줄이 있는 애플리케이션 이름을 추가합니다. 예: `MyStore_Adminhtml`, `MyStore_frontend` |

{style="table-layout:auto"}

## [!UICONTROL Cron]

![크론](./assets/new-relic-reporting-cron.png)<!-- zoom -->

<!-- Cron](https://docs.magento.com/user-guide/system/cron.html) -->

| 필드 | [범위](../../getting-started/websites-stores-views.md#scope-settings) | 설명 |
|--- |--- |--- |
| [!UICONTROL Enable Cron] | 스토어 뷰 | 다음 여부를 결정합니다. [!DNL New Relic] 보고서는 다음 방법으로 일정에 따라 실행할 수 있습니다. [크론](../../systems/cron.md). 옵션: `Yes` / `No` |

{style="table-layout:auto"}
