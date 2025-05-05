---
title: '[!DNL New Relic] 보고'
description: New Relic APM 서비스용 소프트웨어를 포함하여 클라우드 인프라의 Adobe Commerce 계정에서 사용할 수 있는  [!DNL New Relic] 보고에 대해 알아봅니다.
exl-id: 65d08bda-da01-4dcf-9d92-189d4d303c76
role: Admin, Leader
feature: System
source-git-commit: 0651a2489a396ab142b60a8678d6c7590fd5f9ee
workflow-type: tm+mt
source-wordcount: '1382'
ht-degree: 0%

---

# [!DNL New Relic] 보고

[New Relic][1]은(는) 응용 프로그램 상호 작용을 분석하고 개선하는 데 도움이 되는 소프트웨어 분석 서비스입니다. 클라우드 인프라의 Adobe Commerce 계정에는 [!DNL New Relic APM] 서비스용 소프트웨어가 포함되어 있습니다. 자세한 내용은 _New Relic on Cloud Infrastructure Guide_&#x200B;의 [Commerce 서비스][4]를 참조하십시오.

## 1단계: [!DNL New Relic] 계정에 등록

1. [[!DNL New Relic]][1] 웹 사이트로 이동하여 계정을 등록합니다.

   무료 체험판 계정에 가입할 수도 있습니다.

1. 사이트의 지침을 따르십시오. 메시지가 표시되면 먼저 설치할 제품을 선택합니다.

1. 계정 중에 상거래 구성을 완료하는 데 필요한 다음 자격 증명을 찾으십시오.

   | 선택 | 설명 |
   | ------ | ----------- |
   | 계정 ID | [!DNL New Relic] 계정 대시보드에서 계정 ID는 URL의 `/accounts` 뒤에 있는 숫자입니다. |
   | 애플리케이션 ID | [!DNL New Relic] 계정 대시보드에서 **[!UICONTROL New Relic APM]**&#x200B;을(를) 클릭합니다. 메뉴에서 **[!UICONTROL Applications]**&#x200B;을(를) 선택합니다. 그런 다음 애플리케이션을 선택합니다. 애플리케이션 ID는 다음 URL 뒤에 있는 번호입니다. `/applications/` |
   | Relic API 키 새로 만들기 | [!DNL New Relic] 계정 대시보드에서 **[!UICONTROL Account Settings]**&#x200B;을(를) 클릭합니다. 통합 아래의 왼쪽 메뉴에서 **[!UICONTROL Data Sharing]**&#x200B;을(를) 선택합니다. 이 페이지에서 API 키를 생성, 재생성 또는 삭제할 수 있습니다. |
   | Insights API 키 | [!DNL New Relic] 계정 대시보드에서 **[!UICONTROL Insights]**&#x200B;을(를) 클릭합니다. 관리 아래의 왼쪽 메뉴에서 **[!UICONTROL API Keys]**&#x200B;을(를) 선택합니다. Insights API 키가 이 페이지에 표시됩니다. 필요한 경우 키 삽입 옆에 있는 더하기 기호(**+**)를 클릭하여 키를 생성합니다. |

   {style="table-layout:auto"}

## 2단계: 서버에 [!DNL New Relic] 에이전트 설치

[!DNL New Relic APM Pro]을(를) 사용하여 데이터를 수집하고 전송하려면 서버에 PHP 에이전트가 설치되어 있어야 합니다.

1. 웹 에이전트를 선택하라는 메시지가 표시되면 **PHP**&#x200B;을(를) 클릭합니다.

1. 서버에 PHP 에이전트를 설정하려면 지침을 따르십시오.

   도움이 필요하면 [PHP용 New Relic][3]을 참조하세요.

1. 서버에서 cron이 실행 중인지 확인하십시오.

   자세한 내용은 개발자 설명서에서 [cron 구성 및 실행][5]을 참조하세요.

## 3단계: 스토어 구성

>[!NOTE]
>이러한 구성 옵션은 클라우드 인프라의 Adobe Commerce에는 적용되지 않습니다.
>
>Pro 플랜을 사용하는 경우 New Relic이 이미 [사전 구성되어 있고 기본적으로 활성화되어 있습니다](https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/monitor/new-relic/new-relic-service.html?lang=ko). 스타터 플랜을 사용하는 경우 설정 프로세스의 일부인 [New Relic 구성 단계](https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/monitor/new-relic/account-management.html?lang=ko#configure-new-relic-for-starter-environment)를 완료해야 합니다.

1. _관리자_ 사이드바에서 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**(으)로 이동합니다.

1. **[!UICONTROL General]**&#x200B;이(가) 확장된 왼쪽 탐색 패널에서 **[!UICONTROL New Relic Reporting]**&#x200B;을(를) 선택하고 다음을 수행합니다.

   ![New Relic 보고 구성](./assets/new-relic-reporting-general.png){width="600"}

   * **[!UICONTROL Enable New Relic Integration]**&#x200B;을(를) `Yes`(으)로 설정합니다.

   * **[!UICONTROL Insights API URL]**&#x200B;에서 백분율(`%`) 기호를 New Relic 계정 ID로 바꾸십시오.

   * **[!UICONTROL New Relic Account ID]**&#x200B;을(를) 입력하십시오.

   * **[!UICONTROL New Relic Application ID]**&#x200B;을(를) 입력하십시오.

   * **[!UICONTROL New Relic API Key]**&#x200B;을(를) 입력하십시오.

   * **[!UICONTROL Insights API Key]**&#x200B;을(를) 입력하세요.

1. **[!UICONTROL New Relic Application Name]**&#x200B;의 경우 내부 참조에 대한 구성을 식별하는 이름을 입력하십시오.

1. (선택 사항) **[!UICONTROL Send Adminhtml and Frontend as Separate Apps]**&#x200B;의 경우 `Yes`을(를) 선택하여 상점 및 관리자에 대해 수집된 데이터를 별도의 앱으로 New Relic에 보냅니다.

   이 옵션을 사용하려면 **[!UICONTROL New Relic Application Name]**&#x200B;에 이름을 입력해야 합니다.

   >[!NOTE]
   >
   >이 기능을 활성화하면 거짓 양성 [!DNL New Relic] 경고 수가 감소하고 구성된 모니터링과 프론트엔드 성능을 위한 경고를 엄격하게 사용할 수 있습니다. New Relic은 응용 프로그램 이름이 `Adminhtml` 및 프런트 엔드에 추가된 별도의 앱 데이터 파일을 받습니다. 예: `MyStore_Adminhtml`

1. 완료되면 **[!UICONTROL Save Config]**&#x200B;을(를) 클릭합니다.

## 4단계: [!DNL New Relic] 보고에 Cron 사용

1. **[!UICONTROL Cron]** 섹션에서 ![확장 선택기](../assets/icon-display-expand.png)를 확장합니다.

   ![New Relic 크론 구성](./assets/new-relic-reporting-cron.png){width="600"}

1. **[!UICONTROL Enable Cron]**&#x200B;을(를) `Yes`(으)로 설정합니다.

1. 완료되면 **[!UICONTROL Save Config]**&#x200B;을(를) 클릭합니다.

## [!DNL New Relic]개 쿼리

[!DNL New Relic Insights] 데이터는 [!DNL New Relic Query Language] (NRQL)에 작성된 문 및 포함할 수 있는 사용자 지정 매개 변수를 기반으로 합니다. 임시 쿼리에서 데이터를 반환하거나 대시보드에 저장된 쿼리에서 데이터를 반환할 수 있습니다. 자세한 내용은 [!DNL New Relic] 설명서에서 [NRQL 참조][6]를 참조하십시오.

### 관리 이벤트

#### 활성 관리자 사용자

활성 관리자 사용자 수를 반환합니다.

    SELECT uniqueCount(AdminId)
    FROM Transaction
    WHERE appName=&#39;&lt;your_app_name>&#39; 15분 전부터

#### 현재 활성 관리자 사용자

활성 관리자 사용자의 이름을 반환합니다.

    고유(AdminName) 선택
    트랜잭션에서
    15분 전부터 WHERE appName=&#39;&lt;your_app_name>&#39;

#### 최근 관리 활동

최근 관리 작업 수를 반환합니다.

    SELECT COUNT(AdminId)
    FROM 트랜잭션
    WHERE appName =&#39;&lt;your_app_name>&#39; FACET AdminName 1일 전 이후

#### 최신 관리 활동

관리자 사용자 이름, 기간 및 애플리케이션 이름을 포함하여 최근 관리자 작업에 대한 세부 정보를 반환합니다.

    SELECT AdminName, 기간, 이름
    FROM 트랜잭션
    WHERE appName=&#39;&lt;your_app_name>&#39; AND AdminName IS NOT NULL
    AND AdminName !&lt;/your_app_name>= &#39;N/A&#39; 제한 50

### Cron 이벤트

#### 범주 수

지정된 기간 동안의 범주별 애플리케이션 이벤트 수를 반환합니다.

    SELECT average(CatalogCategoryCount)
    FROM Cron
    WHERE CatalogCategoryCount IS NOT NULL
    AND appName = &#39;&lt;your_app_name>&#39; 시계열 2분

#### 현재 카탈로그 개수

지정된 기간 동안 카탈로그에 있는 응용 프로그램 이벤트의 카테고리별 평균 수를 반환합니다.

    SELECT average(CatalogCategoryCount)
    FROM Cron
    WHERE CatalogCategoryCount IS NOT NULL
    AND CatalogCategoryCount > 0
    AND appName = &#39;&lt;your_app_name>&#39; SINCE 2 minutes ago LIMIT 1
&lt;/your_app_name>

#### 활성 제품

지정된 기간 동안 제품별 응용 프로그램 이벤트 수를 반환합니다.

    SELECT average(CatalogProductActiveCount)
    FROM Cron
    WHERE CatalogProductActiveCount IS NOT NULL
    AND appName = &#39;&lt;your_app_name>&#39; TIMESERIES 2분

#### 활성 제품 수

지정된 기간 동안 제품별 활성 응용 프로그램 이벤트의 평균 수를 반환합니다.

    SELECT AVERAGE(CatalogProductActiveCount)
    FROM CRON
    WHERE CatalogProductActiveCount IS NOT NULL
    2분 전 LIMIT 1
부터 CATALOGProductActiveCount > 0
    AND APPName = &#39;&lt;your_app_name>&#39;

#### 구성 가능한 제품

지정된 기간 동안 구성 가능한 제품에 대한 평균 애플리케이션 이벤트 수를 반환합니다.

    SELECT average(CatalogProductConfigurableCount)
    FROM Cron
    WHERE CatalogProductConfigurableCount IS NOT NULL
    AND appName = &#39;&lt;your_app_name>&#39; TIMESERIES 2분

#### 구성 가능한 제품 수

지정된 기간 동안 구성 가능한 제품별 평균 애플리케이션 이벤트 수를 반환합니다.

    SELECT average(CatalogProductConfigurableCount)
    FROM CRON
    WHERE CatalogProductConfigurableCount IS NOT NULL
    2분 전 LIMIT 1
부터 CATALOGProductConfigurableCount > 0
    AND appName = &#39;&lt;your_app_name>&#39;

#### 제품 개수(모두)

모든 제품에 대한 총 응용 프로그램 이벤트 수를 반환합니다.

    SELECT average(CatalogProductCount)
    FROM Cron
    WHERE CatalogProductCount IS NOT NULL
    AND appName = &#39;&lt;your_app_name>&#39; TIMESERIES 2분

#### 현재 제품 개수(모두)

지정된 기간 동안 모든 제품에 대한 평균 응용 프로그램 이벤트 수를 반환합니다.

    SELECT AVERAGE(CatalogProductCount)
    FROM CRON
    WHERE CatalogProductCount IS NOT NULL
    2분 전 LIMIT 1
부터 CATALOGProductCount > 0
    AND APPName = &#39;&lt;your_app_name>&#39;

#### 고객 수

고객별 평균 애플리케이션 이벤트 수를 반환합니다.

    SELECT AVERAGE(CustomerCount)
    FROM CRON
    WHERE CustomerCount IS NOT NULL
    AND CustomerCount > 0&lt;
    AND APPName = &#39;&lt;your_app_name>&#39; 시계열 2분

#### 현재 고객 수

지정된 기간 동안의 평균 고객 수를 반환합니다.

    SELECT AVERAGE(CustomerCount)
    FROM CRON
    WHERE CustomerCount IS NOT NULL
    AND CustomerCount > 0
    AND APPName = &#39;&lt;your_app_name>&#39; SINCE 2분 전 LIMIT 1

#### 모듈 상태

지정된 기간 동안 응용 프로그램 모듈의 사용, 사용 안 함 또는 설치 평균 횟수를 반환합니다.

    SELECT average(ModulesDisabled), average(ModulesEnabled), average
    (ModulesInstalled)
    FROM Cron&lt;
    WHERE appName = &#39;&lt;your_app_name>&#39; 시계열 2분

#### 현재 모듈 상태

지정된 기간 동안 모듈이 활성화, 비활성화 또는 설치된 평균 횟수를 반환합니다.

    SELECT average(ModulesDisabled), average(ModulesEnabled), average
    (ModulesInstalled)
    FROM Cron
    WHERE appName = &#39;&lt;your_app_name>&#39; SINCE 2분 전 LIMIT 1

#### 웹 사이트 및 스토어 수

지정된 기간 동안 웹 사이트 및 저장소별 평균 응용 프로그램 이벤트 수를 반환합니다.

    평균(StoreViewCount), 평균(WebsiteCount) 선택
    크론에서
    WHERE appName = &#39;&lt;your_app_name&gt;&#39; 시계열 2분

#### 현재 웹 사이트 및 스토어 수

지정된 기간 동안의 현재 응용 프로그램 이벤트의 평균 수를 반환합니다.

    SELECT average(StoreViewCount), average(WebsiteCount)
    FROM Cron
    WHERE appName = &#39;&lt;your_app_name>&#39; SINCE 2분 전 제한 1

#### Cron - 이벤트의 모든 데이터

모든 응용 프로그램 이벤트 데이터를 반환합니다.

    선택 *
    크론에서
    WHERE appName = &#39;&lt;your_app_name>&#39;

### 고객

#### 활성 고객 수

지정된 기간 동안의 활성 고객 수를 반환합니다.

    SELECT uniqueCount(CustomerId)
    FROM Transaction
    15분 전부터 WHERE appName = &#39;&lt;your_app_name>&#39;

#### 활성 고객

지정된 기간 동안 활성 고객의 이름을 반환합니다.

    고유(CustomerName) 선택
    트랜잭션에서
    15분 전부터 WHERE appName=&#39;&lt;your_app_name>&#39;

#### 상위 고객

지정된 기간 동안 상위 고객을 반환합니다.

    SELECT count(CustomerId)
    FROM 트랜잭션
    WHERE appName = &#39;&lt;your_app_name>&#39; FACET 1일 전 이후 CustomerName

#### 최근 관리 활동

고객 이름과 방문 기간을 포함하여 최근 활동에 대해 정의된 수의 레코드를 반환합니다.

    SELECT CustomerName, 기간, 이름
    FROM 트랜잭션
    WHERE appName=&#39;&lt;your_app_name>&#39;
    AND CustomerName IS NOT NULL
    AND CustomerName !&lt;/your_app_name>= &#39;N/A&#39; 제한 50

### 주문

#### 발생한 주문 수

지정된 기간 동안 발생한 주문 수를 반환합니다.

    SELECT count(Order)
    FROM 트랜잭션 SINCE 1일 전

#### 총 주문 가격

지정된 기간 동안 주문된 라인 항목의 총 수를 반환합니다.

    SELECT sum(orderValue)
    FROM 트랜잭션 SINCE 1일 전

#### 주문한 총 광고 항목 수

지정된 기간 동안 주문한 총 라인 항목 수를 반환합니다.

    SELECT SUM(lineItemCount)
    1일 전 이후의 트랜잭션에서


[1]: https://newrelic.com/
[3]: https://docs.newrelic.com/docs/agents/php-agent/getting-started/new-relic-php
[4]: https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/monitor/new-relic/new-relic-service.html?lang=ko
[5]: https://experienceleague.adobe.com/docs/commerce-operations/configuration-guide/cli/configure-cron-jobs.html?lang=ko
[6]: https://docs.newrelic.com/docs/insights/new-relic-insights/using-new-relic-query-language/nrql-reference
