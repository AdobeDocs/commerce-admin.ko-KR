---
title: Experience Manager Assets 통합 설치 및 구성
description: " [!DNL AEM Assets Integration for Adobe Commerce]을(를) 설치하고 구성하는 방법에 대해 알아봅니다."
feature: CMS, Media
source-git-commit: 65a4339f0f6d4e9eb280ce90d6173caf671fde0f
workflow-type: tm+mt
source-wordcount: '1261'
ht-degree: 0%

---

# Commerce용 AEM Assets 통합 설치 및 구성

{{$include /help/_includes/aem-assets-integration-beta-note.md}}

확장을 Commerce 애플리케이션에 추가하고, Commerce SaaS 서비스에 연결하고, 이벤트 서비스를 Adobe I/O 하고, Commerce SaaS에 연결하여 Commerce용 AEM Assets 통합을 설치하고 구성합니다.

## 시스템 요구 사항

**소프트웨어 요구 사항**

- Adobe Commerce 2.4.5+
- PHP 8.1, 8.2, 8.3
- 작성기: 2.x

**구성 요구 사항**

- [Adobe IMS 인증](/help/getting-started/adobe-ims-config.md)을 사용하도록 Adobe Commerce을 구성해야 합니다.
- 계정 프로비저닝 및 권한
   - [Commerce 클라우드 프로젝트 관리자](https://experienceleague.adobe.com/en/docs/commerce-cloud-service/user-guide/project/user-access) - 필요한 확장을 설치하고 관리자 또는 명령줄에서 Commerce 응용 프로그램 서버를 구성합니다.
   - [Commerce 관리자](https://experienceleague.adobe.com/en/docs/commerce-admin/start/guide-overview) - 저장소 구성을 업데이트하고 Commerce 사용자 계정을 관리합니다.

## 구성 개요

다음 작업을 완료하여 통합을 활성화합니다.

1. [AEM Assets 통합 확장(`aem-assets-integration`)을 설치합니다](#install-the-aem-assets-integration-extension).
1. [Commerce 서비스 커넥터를 구성](#configure-the-commerce-services-connector)하여 Adobe Commerce 인스턴스와 Adobe Commerce 및 AEM Assets 간에 데이터를 전송할 수 있는 서비스에 연결합니다.
1. [Commerce에 대한 Adobe I/O 이벤트 구성](#configure-adobe-io-events-for-commerce)
1. [API 액세스에 대한 인증 자격 증명 가져오기](#get-authentication-credentials-for-api-access)

## AEM Assets 통합 확장 설치

>[!BEGINSHADEBOX]

**필수 구성 요소**

- 확장을 설치하려면 [repo.magento.com](https://repo.magento.com/admin/dashboard)에 액세스하세요. 키를 생성하고 필요한 권한을 얻으려면 [인증 키 가져오기](https://experienceleague.adobe.com/en/docs/commerce-operations/installation-guide/prerequisites/authentication-keys)를 참조하십시오. 클라우드 설치의 경우 [클라우드 인프라의 Commerce 안내서](https://experienceleague.adobe.com/en/docs/commerce-cloud-service/user-guide/develop/authentication-keys)를 참조하십시오.

- Adobe Commerce 애플리케이션 서버의 명령줄에 액세스합니다.

>[!ENDSHADEBOX]

Adobe Commerce 2.4.4 이상을 실행하는 Adobe Commerce에 최신 버전의 AEM Assets 통합 확장(`aem-assets-integration`)을 설치합니다. AEM Asset 통합은 [repo.magento.com](https://repo.magento.com/admin/dashboard) 리포지토리에서 작성기 메타패키지로 제공됩니다.

>[!BEGINTABS]

>[!TAB 클라우드 인프라]

이 메서드를 사용하여 Commerce Cloud 인스턴스에 대한 [!DNL AEM Assets Integration] 확장을 설치합니다.

1. 로컬 워크스테이션에서 Adobe Commerce on cloud infrastructure 프로젝트의 프로젝트 디렉터리로 변경합니다.

   >[!NOTE]
   >
   >Commerce 프로젝트 환경을 로컬로 관리하는 방법에 대한 자세한 내용은 _Adobe Commerce on Cloud Infrastructure 사용 안내서_&#x200B;의 [CLI로 분기 관리](https://experienceleague.adobe.com/en/docs/commerce-cloud-service/user-guide/develop/cli-branches)를 참조하십시오.

1. Adobe Commerce Cloud CLI를 사용하여 업데이트할 환경 분기를 확인하십시오.

   ```shell
   magento-cloud environment:checkout <environment-id>
   ```

1. Commerce용 AEM Assets 통합 확장 추가.

   ```shell
   composer require "magento/aem-assets-integration" "<version-tbd>" --no-update
   ```

1. 패키지 종속성을 업데이트합니다.

   ```shell
   composer update "magento/aem-assets-integration"
   ```

1. `composer.json` 및 `composer.lock` 파일에 대한 코드 변경 내용을 커밋하고 푸시합니다.

1. `composer.json` 및 `composer.lock` 파일에 대한 코드 변경 내용을 클라우드 환경에 추가, 커밋 및 푸시합니다.

   ```shell
   git add -A
   git commit -m "Install AEM Assets Integration extension for Adobe Commerce"
   git push origin <branch-name>
   ```

   업데이트를 푸시하면 [Commerce 클라우드 배포 프로세스](https://experienceleague.adobe.com/en/docs/commerce-cloud-service/user-guide/develop/deploy/process)가 시작되어 변경 내용을 적용합니다. [배포 로그](https://experienceleague.adobe.com/en/docs/commerce-cloud-service/user-guide/develop/test/log-locations#deploy-log)에서 배포 상태를 확인하십시오.

>[!TAB 온-프레미스]

이 메서드를 사용하여 온-프레미스 인스턴스에 대한 [!DNL AEM Assets Integration] 확장을 설치합니다.

1. 작성기를 사용하여 Commerce용 AEM Assets 통합 확장 기능을 프로젝트에 추가합니다.

   ```shell
   composer require "magento/aem-assets-integration" --no-update
   ```

1. 종속성을 업데이트하고 확장을 설치합니다.

   ```shell
   composer update  "magento/aem-assets-integration"
   ```

1. Adobe Commerce 업그레이드:

   ```shell
   bin/magento setup:upgrade
   ```

1. 캐시를 지웁니다.

   ```shell
   bin/magento cache:clean
   ```

   >[!TIP]
   >
   >경우에 따라, 특히 프로덕션에 배포 시 시간이 걸릴 수 있으므로 컴파일된 코드를 지우지 않는 것이 좋습니다. 변경하기 전에 시스템을 백업해야 합니다.

>[!ENDTABS]

## Commerce 서비스 커넥터 구성

Commerce 서비스 커넥터를 사용하면 Commerce 인스턴스, Asset Rule Engine 서비스 및 기타 지원 서비스 간에 데이터를 동기화하고 통신할 수 있습니다.

>[!NOTE]
>
>Commerce 서비스 커넥터 설정은 [Adobe Commerce SaaS 서비스](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/user-guides/integration-services/saas#availableservices)를 사용하는 데 필요한 일회성 프로세스입니다. 다른 서비스에 대한 커넥터를 이미 구성한 경우 **[!UICONTROL Systems]** > [!UICONTROL Services] > **[!UICONTROL Commerce Services Connector]**&#x200B;을(를) 선택하여 Commerce 관리에서 기존 구성을 볼 수 있습니다.

Adobe Commerce 인스턴스와 AEM Assets 통합을 활성화하는 서비스 간에 데이터를 전송하려면 다음과 같이 Commerce 서비스 커넥터를 구성합니다.

- 인증을 위해 프로덕션 및 샌드박스 API 키로 Commerce 인스턴스를 구성합니다.
- 보안 클라우드 저장소에 대한 데이터 공간(SaaS 식별자)을 지정하십시오.
- AEM Assets에 액세스하는 데 사용하는 것과 동일한 IMS 조직에 로그인하여 데이터 세트와 Adobe Experience Platform 간의 연결을 설정하십시오.

자세한 지침은 [Commerce 서비스 커넥터](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/user-guides/integration-services/saas#organizationid)를 참조하십시오.

Commerce 서비스 커넥터를 구성하면 시스템에서 SaaS 프로젝트 및 데이터베이스 ID를 생성합니다. 테넌트 온보딩 프로세스 중에 이러한 ID가 필요합니다.

AEM Assets 통합을 위한 ![SaaS 프로젝트 및 데이터 공간 ID](assets/aem-saas-project-config.png){width="600" zoomable="yes"}

## Commerce에 대한 Adobe I/O 이벤트 구성

AEM Assets 통합은 Adobe I/O 이벤트 서비스를 사용하여 Commerce 인스턴스와 Experience Cloud 간에 사용자 지정 이벤트 데이터를 보냅니다. 이벤트 데이터는 AEM Assets 통합을 위한 워크플로를 조정하는 데 사용됩니다.

>[!BEGINSHADEBOX]

**필수 구성 요소**

- RabbitMQ이 활성화되어 있고 이벤트를 수신하는지 확인합니다.
   - [Adobe Commerce 온-프레미스에 대한 RabbitMQ 설정](https://experienceleague.adobe.com/en/docs/commerce-cloud-service/user-guide/configure/service/rabbitmq)
   - [클라우드 인프라에서 Adobe Commerce에 대한 RabbitMQ 설정](https://experienceleague.adobe.com/en/docs/commerce-cloud-service/user-guide/configure/service/rabbitmq)

>[!ENDSHADEBOX]

>[!NOTE]
>
>Commerce의 Adobe I/O 이벤트에 대한 자세한 내용은 Adobe Developer 사이트에서 [Commerce의 이벤트 Adobe I/O](https://developer.adobe.com/commerce/extensibility/events/) 설명서를 참조하십시오.

설정하려면 다음 단계가 필요합니다.

1. 애플리케이션 서버와 관리자에서 Adobe I/O 이벤트를 구성하여 Commerce 이벤트 프레임워크를 활성화합니다.
1. Assets 규칙 엔진 서비스 API를 사용하여 연결을 구성하여 Adobe Commerce과 AEM Assets 간의 데이터 동기화를 활성화합니다.
1. 관리자에서 AEM Assets 통합을 활성화합니다.

### Commerce 이벤트 프레임워크 활성화

Commerce 프로젝트가 배포된 환경에 대한 지침을 사용하여 Commerce 이벤트 프레임워크를 활성화합니다.

>[!BEGINTABS]

>[!TAB 클라우드 인프라]

1. [!DNL Store Settings Configuration] 메뉴에서 Adobe I/O 이벤트 서비스를 사용하도록 설정합니다.

   1. 책임자에서 **[!UICONTROL Stores]** > [!UICONTROL Settings] > **[!UICONTROL Configuration]** > **[!UICONTROL Adobe Services]** > **이벤트 Adobe I/O**(으)로 이동합니다.

   1. **[!UICONTROL Commerce events]** 확장.

   1. **[!UICONTROL Enabled]**&#x200B;을(를) `Yes`(으)로 설정합니다.

      ![Adobe I/O 이벤트 Commerce 관리 구성 - Commerce 이벤트 사용](assets/aem-enable-io-event-admin-config.png){width="600" zoomable="yes"}

      >[!NOTE]
      >
      >[cron을 사용](https://developer.adobe.com/commerce/extensibility/events/configure-commerce/#check-cron-and-message-queue-configuration)하여 Commerce이 API 끝점에 이벤트를 전송하여 통합을 위한 통신 및 워크플로를 관리할 수 있도록 합니다.

1. 클라우드 프로젝트 구성을 업데이트합니다.

   1. 작업 저장소에 `app/etc/config.php` 파일 추가:

   ```shell
   git add app/etc/config.php
   ```

   1. `composer info magento/ece-tools` 명령을 실행하여 ece-tools 버전을 확인합니다. 버전이 `2002.1.13`보다 작은 경우 [최신 버전으로 업데이트](https://experienceleague.adobe.com/en/docs/commerce-cloud-service/user-guide/dev-tools/ece-tools/update-package)하십시오.

   1. `.magento.env.yaml` 파일에서 이벤트 사용:

      ```yaml
      stage:
         global:
            ENABLE_EVENTING: true
      ```

   1. 업데이트된 파일을 커밋하고 클라우드 환경으로 푸시합니다.

>[!TAB 온-프레미스]

1. [!DNL Store Settings Configuration] 메뉴에서 Adobe I/O 이벤트 서비스를 사용하도록 설정합니다.

   1. 책임자에서 **[!UICONTROL Stores]** > [!UICONTROL Settings] > **[!UICONTROL Configuration]** > **[!UICONTROL Adobe Services]** > **이벤트 Adobe I/O**(으)로 이동합니다.

   1. **[!UICONTROL Commerce events]** 확장.

   1. **[!UICONTROL Enabled]**&#x200B;을(를) `Yes`(으)로 설정합니다.

      ![Adobe I/O 이벤트 Commerce 관리 구성 - Commerce 이벤트 사용](assets/aem-enable-io-event-admin-config.png){width="600" zoomable="yes"}

      >[!NOTE]
      >
      >Commerce에서 AEM assets와 Commerce 간의 통신 및 워크플로를 관리하기 위해 이벤트를 전송할 수 있도록 [cron 작업을 사용](https://developer.adobe.com/commerce/extensibility/events/configure-commerce/#check-cron-and-message-queue-configuration)합니다.

>[!ENDTABS]

## API 액세스에 대한 인증 자격 증명 가져오기

Commerce용 AEM Assets 통합에는 Commerce 인스턴스에 대한 API 액세스를 허용하기 위한 OAuth 인증 자격 증명이 필요합니다. 테넌트 온보딩 중에 Assets 규칙 엔진 서비스에 Commerce 프로젝트를 등록하고 Adobe Commerce과 AEM Assets 간에 에셋을 관리하기 위한 API 요청을 제출하려면 이러한 자격 증명이 필요합니다.

Commerce 인스턴스에 통합을 추가하고 활성화하여 자격 증명을 생성합니다.

### Commerce 환경에 통합 추가

1. 책임자에서 **시스템** > 확장 > **통합**(으)로 이동한 다음 **새 통합 추가**&#x200B;를 클릭합니다.

1. 통합에 대한 정보를 입력합니다.

   **일반** 섹션에서 통합 **이름** 및 **전자 메일**&#x200B;만 지정하십시오. Commerce 및 Experience Manager Assets이 배포된 조직에 액세스할 수 있는 Adobe IMS 계정용 이메일을 사용합니다.

   ![Commerce 관리자 구성을 위한 AEM Assets 통합](assets/aem-add-commerce-integration.png){width="600" zoomable="yes"}

1. **ID 확인**&#x200B;을 클릭하여 ID를 확인하세요.

   시스템은 Adobe ID로 Experience Cloud에 인증하여 ID를 확인합니다.

1. API 리소스를 구성합니다.

   1. 왼쪽 패널에서 **[!UICONTROL API]**을(를) 클릭합니다.
E
   1. 외부 미디어 리소스 **[!UICONTROL Catalog > Inventory > Products > External Media]**&#x200B;을(를) 선택하십시오.

   ![API 리소스에 대한 관리자 통합 구성](assets/aem-commerce-integration-api-resources.png){width="600" zoomable="yes"}

1. **[!UICONTROL Save]**&#x200B;을(를) 클릭합니다.

### 자격 증명 생성

통합 페이지에서 Assets 통합을 위해 **활성화**&#x200B;를 클릭하여 OAuth 인증 자격 증명을 생성합니다. Commerce 프로젝트를 Assets 규칙 엔진 서비스에 등록하고 API 요청을 제출하여 Adobe Commerce과 AEM Assets 간에 에셋을 관리하려면 이러한 자격 증명이 필요합니다.

1. 통합 페이지에서 **[!UICONTROL Activate]**&#x200B;을(를) 클릭하여 자격 증명을 생성합니다.

   ![Assets 통합을 위해 Commerce 구성 활성화](assets/aem-activate-commerce-integration.png){width="600" zoomable="yes"}

1. 나중에 사용할 수 있도록 소비자 키 및 액세스 토큰에 대한 자격 증명을 저장합니다.

API 요청을 인증하기 위한 ![OAuth 자격 증명](./assets/aem-commerce-integration-credentials.png){width="600" zoomable="yes"}

1. **[!UICONTROL Done]**&#x200B;을(를) 클릭합니다.

>[!NOTE]
>
>Adobe Commerce API를 사용하여 인증 자격 증명을 생성할 수도 있습니다. 이 프로세스에 대한 자세한 내용과 Adobe Commerce의 OAuth 기반 인증에 대한 자세한 내용은 Adobe Developer 설명서의 [OAuth 기반 인증](https://developer.adobe.com/commerce/webapi/get-started/authentication/gs-authentication-oauth/)을 참조하십시오.
