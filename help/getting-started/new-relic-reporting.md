---
title: ' [!DNL New Relic] 보고 '
description: ' [!DNL New Relic] 새로 만들기 유물 APM 서비스에 대 한 소프트웨어가 포함 된 클라우드 인프라에서 Adobe Systems 상거래에 사용할 수 있는 보고에 대해 알아봅니다.'
exl-id: 65d08bda-da01-4dcf-9d92-189d4d303c76
role: Admin, Leader
feature: System
source-git-commit: e9a7645aed0e3b48bf565b04cdb6a31ce5d39ca0
workflow-type: tm+mt
source-wordcount: '1361'
ht-degree: 0%

---

# [!DNL New Relic] 보고

[New Relic][1] 는 애플리케이션 상호 작용을 분석하고 개선하는 데 도움이 되는 소프트웨어 분석 서비스입니다. 클라우드 인프라의 Adobe Commerce 계정에는 [!DNL New Relic APM] 서비스. 자세한 내용은 [New Relic 서비스][4] 다음에서 _클라우드 인프라의 Commerce 안내서_.

## 1단계: 다음에 등록 [!DNL New Relic] account

1. [[!DNL New Relic]][1]웹 사이트로 이동 하 여 계정에 등록 합니다.

   무료 평가판 계정 등록할 수도 있습니다.

1. 사이트의 지침을 따르십시오. 메시지가 표시 되 면 먼저 설치할 제품을 선택 합니다.

1. 계정 하는 동안 상거래 구성을 완료 하는 데 필요한 다음 자격 증명을 찾습니다.

   | 옵션 | 설명 |
   | ------ | ----------- |
   | 계정 ID | 출처: [!DNL New Relic] 계정 대시보드에서 계정 ID는 URL의 다음 번호입니다. `/accounts` |
   | 애플리케이션 ID | 출처: [!DNL New Relic] 계정 대시보드, 클릭 **[!UICONTROL New Relic APM]**. 메뉴에서 다음을 선택합니다. **[!UICONTROL Applications]**. 그런 다음 애플리케이션을 선택합니다. 애플리케이션 ID는 URL의 다음 뒤에 있는 번호입니다. `/applications/` |
   | New Relic API 키 | 출처: [!DNL New Relic] 계정 대시보드, 클릭 **[!UICONTROL Account Settings]**. 통합 아래의 왼쪽 메뉴에서 을(를) 선택합니다. **[!UICONTROL Data Sharing]**. 이 페이지에서 API 키를 생성, 재생성 또는 삭제할 수 있습니다. |
   | Insights API 키 | 출처: [!DNL New Relic] 계정 대시보드, 클릭 **[!UICONTROL Insights]**. 관리 아래의 왼쪽 메뉴에서 **[!UICONTROL API Keys]**. Insights API 키가 이 페이지에 표시됩니다. 필요한 경우 더하기 기호(**+**)을 클릭하여 키를 생성합니다. |

   {style="table-layout:auto"}

## 2단계: 설치 [!DNL New Relic] 서버의 에이전트

사용 [!DNL New Relic APM Pro] 데이터를 수집하고 전송하려면 서버에 PHP 에이전트가 설치되어 있어야 합니다.

1. 웹 에이전트를 선택하라는 메시지가 표시되면 **PHP**.

1. 서버에 PHP 에이전트를 설정하려면 지침을 따르십시오.

   도움이 필요한 경우 다음을 참조하십시오. [PHP용 New Relic][3].

1. 서버에서 cron이 실행 중인지 확인하십시오.

   자세한 내용은 다음을 참조하십시오. [cron 구성 및 실행][5] 개발자 설명서에서 참조하십시오.

## 3단계: 스토어 구성

1. 다음에서 _관리자_ 사이드바, 이동 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. 왼쪽 탐색 패널에서 **[!UICONTROL General]** 확장됨, 선택 **[!UICONTROL New Relic Reporting]** 다음을 수행합니다.

   ![New Relic 보고 구성](./assets/new-relic-reporting-general.png){width="600"}

   * 설정 **[!UICONTROL Enable New Relic Integration]** 끝 `Yes`.

   * 다음에서 **[!UICONTROL Insights API URL]**, 백분율 바꾸기(`%`) 기호를 New Relic 계정 ID로 바꿉니다.

   * 다음을 입력하십시오. **[!UICONTROL New Relic Account ID]**.

   * 다음을 입력하십시오. **[!UICONTROL New Relic Application ID]**.

   * 다음을 입력하십시오. **[!UICONTROL New Relic API Key]**.

   * 사용자 입력 **[!UICONTROL Insights API Key]**.

1. 대상 **[!UICONTROL New Relic Application Name]**&#x200B;을 클릭하고 내부 참조에 대한 구성을 식별할 이름을 입력합니다.

1. (선택 사항) **[!UICONTROL Send Adminhtml and Frontend as Separate Apps]**, 선택 `Yes` storefront 및 Admin에 대해 수집된 데이터를 별도의 앱으로 New Relic에 보냅니다.

   이 옵션을 사용 하려면에 입력 **[!UICONTROL New Relic Application Name]** 된 이름이 필요 합니다.

   >[!NOTE]
   >
   >이 기능을 활성화하면 가양성 수가 줄어듭니다 [!DNL New Relic] 경고는 구성된 모니터링을 허용하고, 경고는 프론트엔드 성능을 위해 엄격히 허용합니다. New Relic은 애플리케이션 이름이 추가된 별도의 앱 데이터 파일을 수신합니다 `Adminhtml` 프론트엔드. For example: `MyStore_Adminhtml`

1. 완료되면 다음을 클릭하십시오. **[!UICONTROL Save Config]**.

## 4단계: Cron 활성화 [!DNL New Relic] 보고

1. 섹션 선택기 ](../assets/icon-display-expand.png) 확장을 **[!UICONTROL Cron]** 확장 ![ 합니다.

   ![New Relic Cron 구성](./assets/new-relic-reporting-cron.png){width="600"}

1. 설정 **[!UICONTROL Enable Cron]** 끝 `Yes`.

1. 완료되면 다음을 클릭하십시오. **[!UICONTROL Save Config]**.

## [!DNL New Relic] 쿼리

[!DNL New Relic Insights] 데이터는 로 작성된 문을 기반으로 합니다. [!DNL New Relic Query Language] (NRQL) 및 포함할 수 있는 모든 사용자 지정 매개 변수 임시 쿼리에서 데이터를 반환하거나 대시보드에 저장된 쿼리에서 데이터를 반환할 수 있습니다. 자세한 내용은 [NRQL 참조][6] 다음에서 [!DNL New Relic] 설명서를 참조하십시오.

### 관리 이벤트

#### 활성 관리자 사용자

활성 관리자 사용자 수를 반환합니다.

    SELECT uniqueCount(AdminId)
    출처 거래
    여기서 appName=&#39;&lt;your_app_name>&#39; 15분 전부터

#### 현재 활성화 되어 있는 관리자 사용자

활성 관리자 사용자의 이름을 반환 합니다.

    &lt;your_app_name>15 분 전에 
 &lt;/your_app_name> appName = &#39; &#39; 인 트랜잭션에서 
     고유 (adminname) 
     선택
#### 최근 관리 활동

최근 관리 작업 수를 반환합니다.

    카운트(AdminId) 선택
    출처 거래
    WHERE appName =&#39;&lt;your_app_name>&#39; FACET AdminName 1일 전 이후

#### 최신 관리 활동

Admin username, duration 및 애플리케이션 이름을 포함 하 여 최근 관리 작업에 대 한 세부 정보를 반환 합니다.

    AppName = &#39;&lt;your_app_name>&#39; 및 adminname이 NULL 
     및 adminname이 아닌&lt;/your_app_name> 트랜잭션에서 
     adminname, DURATION, name 
     을 선택 하십시오.= &#39; N/A &#39; 제한 50

### Cron 이벤트

#### 범주 개수

지정된 기간 동안 카테고리별 응용 프로그램 이벤트 수를 반환합니다.

    SELECT average(CatalogCategoryCount)
    크론에서
    여기서 CatalogCategoryCount는 NULL이 아닙니다.
    AND appName = &#39;&lt;your_app_name>&#39; 시계열 2분

#### 현재 카탈로그 개수

지정된 기간 동안 카탈로그에 있는 응용 프로그램 이벤트의 카테고리별 평균 수를 반환합니다.

    SELECT average(CatalogCategoryCount)
    크론에서
    여기서 CatalogCategoryCount는 NULL이 아닙니다.
    AND CatalogCategoryCount > 0
    AND appName = &#39;&lt;your_app_name>&#39; 2분 전부터 제한 1

#### 활성 제품

지정된 기간 동안 제품별 응용 프로그램 이벤트 수를 반환합니다.

    SELECT average(CatalogProductActiveCount)
    크론에서
    여기서 CatalogProductActiveCount는 NULL이 아닙니다.
    AND appName = &#39;&lt;your_app_name>&#39; 시계열 2분

#### 활성 제품 수

지정된 기간 동안 제품별 활성 응용 프로그램 이벤트의 평균 수를 반환합니다.

    SELECT average(CatalogProductActiveCount)
    크론에서
    여기서 CatalogProductActiveCount는 NULL이 아닙니다.
    AND CatalogProductActiveCount > 0
    AND appName = &#39;&lt;your_app_name>&#39; 2분 전부터 제한 1

#### 구성 가능한 제품

지정된 기간 동안 구성 가능한 제품에 대한 평균 애플리케이션 이벤트 수를 반환합니다.

    SELECT average(CatalogProductConfigurableCount)
    크론에서
    여기서 CatalogProductConfigurableCount는 NULL이 아닙니다.
    AND appName = &#39;&lt;your_app_name>&#39; 시계열 2분

#### 구성 가능한 제품 수

지정된 기간 동안 구성 가능한 제품별 평균 애플리케이션 이벤트 수를 반환합니다.

    SELECT average(CatalogProductConfigurableCount)
    크론에서
    여기서 CatalogProductConfigurableCount는 NULL이 아닙니다.
    AND CatalogProductConfigurableCount > 0
    AND appName = &#39;&lt;your_app_name>&#39; 2분 전부터 제한 1

#### 제품 개수(모두)

모든 제품에 대한 총 응용 프로그램 이벤트 수를 반환합니다.

    SELECT average(CatalogProductCount)
    크론에서
    여기서 CatalogProductCount는 NULL이 아닙니다.
    AND appName = &#39;&lt;your_app_name>&#39; 시계열 2분

#### 현재 제품 개수(모두)

지정된 기간 동안 모든 제품에 대한 평균 응용 프로그램 이벤트 수를 반환합니다.

    SELECT average(CatalogProductCount)
    크론에서
    여기서 CatalogProductCount는 NULL이 아닙니다.
    AND CatalogProductCount > 0
    AND appName = &#39;&lt;your_app_name>&#39; 2분 전부터 제한 1

#### 고객 수

고객별 평균 애플리케이션 이벤트 수를 반환합니다.

    SELECT average(CustomerCount)
    크론에서
    여기서 CustomerCount는 NULL이 아닙니다.
    AND CustomerCount > 0&lt;
    AND appName = &#39;&lt;your_app_name>&#39; 시계열 2분

#### 현재 고객 수

지정된 기간 동안의 평균 고객 수를 반환합니다.

    SELECT average(CustomerCount)
    크론에서
    여기서 CustomerCount는 NULL이 아닙니다.
    AND 고객 수 > 0
    AND appName = &#39;&lt;your_app_name>&#39; 2분 전부터 제한 1

#### 모듈 상태

지정된 기간 동안 응용 프로그램 모듈의 사용, 사용 안 함 또는 설치 평균 횟수를 반환합니다.

    평균(ModulesDisabled), 평균(ModulesEnabled), 평균 선택
    (ModulesInstalled)
    크론에서&lt;
    여기서 appName = &#39;&lt;your_app_name>&#39; 시계열 2분

#### 현재 모듈 상태

지정된 기간 동안 모듈이 활성화, 비활성화 또는 설치된 평균 횟수를 반환합니다.

    평균(ModulesDisabled), 평균(ModulesEnabled), 평균 선택
    (ModulesInstalled)
    크론에서
    여기서 appName = &#39;&lt;your_app_name>&#39; 2분 전부터 제한 1

#### 웹 사이트 및 스토어 수

지정된 기간 동안 웹 사이트 및 저장소별 평균 응용 프로그램 이벤트 수를 반환합니다.

    SELECT average(StoreViewCount), average(WebsiteCount)
    크론에서
    여기서 appName = &#39;&amp;lt;your_app_name&amp;gt;&#39; 시계열 2분

#### 현재 웹 사이트 및 스토어 수

지정된 기간 동안의 현재 응용 프로그램 이벤트의 평균 수를 반환합니다.

    SELECT average(StoreViewCount), average(WebsiteCount)
    크론에서
    여기서 appName = &#39;&lt;your_app_name>&#39; 2분 전부터 제한 1

#### Cron - 이벤트의 모든 데이터

모든 응용 프로그램 이벤트 데이터를 반환합니다.

    선택 *
    크론에서
    여기서 appName = &#39;&lt;your_app_name>&#39;

### 고객

#### 활성 고객 수

지정된 기간 동안의 활성 고객 수를 반환합니다.

    SELECT uniqueCount(CustomerId)
    출처 거래
    여기서 appName = &#39;&lt;your_app_name>&#39; 15분 전부터

#### 활성 고객

지정 된 기간 동안 활성 고객의 이름을 반환 합니다.

    고유 (CustomerName)을 (&lt;your_app_name>를 
 )&lt;/your_app_name> 
     Transaction 
     에서 선택 하십시오.
#### 상위 고객

지정된 기간 동안 상위 고객을 반환합니다.

    SELECT count(CustomerId)
    출처 거래
    여기서 appName = &#39;&lt;your_app_name>&#39; FACET CustomerName 1일 전 이후

#### 최근 관리 활동

고객 이름과 방문 기간이 포함 된 최근 활동의 정의 된 레코드 수를 반환 합니다.

    AppName = &#39;&lt;your_app_name>&#39; 
     및 customername이 (가) NULL 
     및 customername이 (가) 아닌&lt;/your_app_name> 트랜잭션에서 
     CustomerName, duration, name 
     을 선택 하십시오.= &#39; N/A &#39; 제한 50

### 주문

#### 배치 된 주문 수

지정 된 기간 중에 배치 되는 주문 수를 반환 합니다.

    COUNT(순서) 선택
    1일 전 이후 거래에서

#### 총 주문 가격

지정된 기간 동안 주문된 라인 항목의 총 수를 반환합니다.

    SELECT sum(orderValue)
    1일 전 이후 거래에서

#### 주문한 총 라인 항목

지정된 기간 동안 주문된 라인 항목의 총 수를 반환합니다.

    SELECT sum(lineItemCount)
    1일 전 이후 거래에서


[1]: https://newrelic.com/
[3]: https://docs.newrelic.com/docs/agents/php-agent/getting-started/new-relic-php
[4]: https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/monitor/new-relic/new-relic-service.html
[5]: https://experienceleague.adobe.com/docs/commerce-operations/configuration-guide/cli/configure-cron-jobs.html
[6]: https://docs.newrelic.com/docs/insights/new-relic-insights/using-new-relic-query-language/nrql-reference
