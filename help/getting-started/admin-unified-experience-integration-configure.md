---
title: 상거래 관리자를 위한 Experience Cloud 통합 구성
description: Experience Cloud을 통해 관리자 액세스를 허용하도록 Commerce 프로젝트를 구성하는 방법에 대해 알아봅니다.
hide: false
hidefromtoc: false
feature: Integration
role: Admin, Leader
exl-id: b2522d25-8255-4219-98b5-4b764430dea2
source-git-commit: 8278d725a7377b865c118b86a57702cd2be43238
workflow-type: tm+mt
source-wordcount: '1011'
ht-degree: 0%

---

# 상거래 관리자와 Experience Cloud 통합 구성

Commerce Admin Unified Experience 및 Commerce Events 확장을 사용하도록 Commerce 애플리케이션을 구성하여 Commerce Admin과의 Experience Cloud 통합을 시작하십시오.


## 전제 조건

- Adobe Commerce은 다음을 사용하도록 구성해야 합니다. [Adobe IMS 인증](../getting-started/adobe-ims-config.md)
- 계정 프로비저닝 및 권한 - 관리자는 [비즈니스 프로필 Adobe](https://helpx.adobe.com/enterprise/kb/introducing-adobe-profiles.html#:~:text=Adobe%20profiles%20help%20you%20manage,under%20the%20same%20email%20address) 다음 리소스에 액세스하여 Experience Cloud 통합을 구성할 수 있습니다.
   - [Adobe Admin Console](https://helpx.adobe.com/enterprise/admin-guide.html)—조직의 Adobe 사용자 및 개발자 계정을 추가하고 관리합니다.
   - [Adobe Developer 콘솔](https://developer.adobe.com/developer-console/docs/guides/getting-started/)—개발자 또는 시스템 관리자 액세스 권한을 사용하여 App Builder 프로젝트를 만들고 연결 자격 증명 및 프로젝트 구성을 생성하여 Adobe I/O 이벤트 서비스 사용
   - [클라우드 인프라의 Commerce 프로젝트](https://experienceleague.adobe.com/docs/commerce-cloud-service/start/onboarding.html#get-started-with-the-project-web-interface)—필요한 모듈을 설치하고 Adobe Commerce CLI를 사용하여 Commerce 애플리케이션 서버를 구성합니다.
   - [Commerce 관리자](https://experienceleague.adobe.com/docs/commerce-admin/start/guide-overview.html)—저장소 구성 업데이트 및 Commerce 사용자 계정 관리

## 구성 개요

다음 작업을 완료하여 통합을 활성화합니다.

1. [상거래 환경 및 애플리케이션 구성 확인](#check-the-commerce-environment-and-application-configuration).

1. [Commerce Admin Unified Experience 확장 활성화](#enable-the-commerce-admin-unified-experience-extension).

1. [상거래에 대한 Adobe I/O 이벤트 설정](#set-up-adobe-io-events).

1. [통합 테스트](#test-the-integration).

## 상거래 환경 및 애플리케이션 구성 확인

Experience Cloud 통합을 구성하기 전에 프로젝트 및 상거래 애플리케이션이 요구 사항을 충족하는지 확인하십시오.

1. 로컬 워크스테이션에서 Commerce 프로젝트의 프로젝트 디렉터리로 변경합니다.

1. Experience Cloud과 통합할 인스턴스에 대한 환경 분기를 확인하십시오.

1. Adobe IMS가 활성화되어 있는지 확인합니다.

   - 사용 [SSH 액세스 URL](https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/develop/secure-connections.html) Commerce 응용 프로그램 서버에 연결할 환경용입니다.

   - 명령줄에서 Adobe Commerce CLI를 사용하여 IMS 모듈 상태를 확인합니다.

     ```bash
     bin/magento admin:adobe-ims:status
     ```

   모듈이 활성화되지 않은 경우 [ims 통합 프로젝트에 대한 조직 및 자격 증명을 사용하여 활성화](../getting-started/adobe-ims-config.md#step-3-enable-the-adminadobeims-module).

1. 관리자 사용자가 Adobe ID을 사용하여 Commerce 관리자에 로그인할 수 있는지 확인합니다.

   - 상거래 관리자 URL로 이동합니다.

   - 로그인한 경우 로그아웃합니다.

   - 관리자 사용자가 Adobe ID을 사용하여 로그인하도록 리디렉션됩니다.

     ![Adobe ID을 사용하여 Adobe Commerce 로그인](./assets/admin-adobeid-login.png){width="600" zoomable="yes"}

1. 로컬 워크스테이션의 클라우드 프로젝트 디렉터리에서 Commerce Admin Unified Experience 확장이 설치되어 있는지 확인합니다.

   ```bash
   composer show *unified-experience*
   ```

   확장이 설치되어 있으면 Composer는 확장 이름과 설명을 반환합니다.

   ```
   magento/module-unified-experience <version> Commerce module responsible for integration with Adobe Experience Cloud
   ```

   확장이 설치되지 않은 경우 작성기를 사용하여 설치합니다. 그런 다음 변경 사항을 커밋하고 클라우드 환경을 재배포합니다.

   ```
   composer require magento/module-unified-experience
   composer update
   ```

## Commerce 관리자 통합 경험 활성화

Commerce Admin 통합 경험 확장을 활성화한 다음 Experience Cloud을 통해 로그인합니다.

>[!NOTE]
>
>이 지침은 Commerce Cloud 프로젝트 관리자가 Adobe Commerce CLI를 사용하여 확장을 활성화하는 방법을 보여 줍니다. Commerce 관리자 사용자는 다음을 업데이트하여 확장을 활성화할 수도 있습니다. [상거래 저장소 구성 설정](admin-unified-experience-integration-manage.md#from-the-commerce-admin).

1. 로컬 워크스테이션에 있는 클라우드 프로젝트 환경의 루트 디렉터리에서 [magento-cloud CLI 도구](https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/dev-tools/cloud-cli/cloud-cli-overview.html) Commerce 응용 프로그램 서버에 로그인합니다.

   ```bash
   magento-cloud ssh
   ```

1. 활성화 `magento/module-unified-experience` Adobe Commerce CLI를 사용한 확장:

   ```bash
   bin/magento config:set admin/unified_experience/enabled 1
   Admin Unified Experience integration is enabled
   ```

1. 캐시를 지웁니다.

   ```bash
   bin/magento cache:clean
   ```

## 상거래에 대한 Adobe I/O 이벤트 설정

Experience Cloud 통합이 활성화되면 Adobe I/O 이벤트 서비스는 상거래 이벤트 데이터를 Experience Cloud으로 전송하여 상거래 프로젝트에 대한 관리자 액세스를 관리합니다. 서비스 설정을 사용하려면 Commerce용 Adobe I/O 이벤트 확장(`magento/commerce-eventing`)를 실행하고 관리에서 Adobe I/O 이벤트 서비스를 구성할 수 있습니다.

### 상거래 이벤트 활성화

Commerce Events 확장 활성화(`magento/commerce-eventing`)을 클릭하여 Commerce 애플리케이션에서 Adobe I/O 이벤트 서비스로 사용자 지정 이벤트 데이터를 전송합니다.

>[!NOTE]
>
>Commerce 2.4.6 이상의 경우 Commerce Events 확장이 기본적으로 설치됩니다. Commerce 2.4.5가 있는 Commerce 프로젝트의 경우 먼저 작성기를 사용하여 다음을 수행합니다 [확장 설치](https://developer.adobe.com/commerce/extensibility/events/installation/#install-adobe-io-modules-on-commerce)를 클릭한 다음 활성화합니다.

1. 로컬 상거래 프로젝트 개발 환경에서 다음 구성을 `.magento.env.yaml` 파일.

   ```yaml
   stage:
     global:
       ENABLE_EVENTING: true
     deploy:
       CRON_CONSUMERS_RUNNER:
         cron_run: true
         max_messages: 0
         consumers: []
   ```

1. 업데이트된 항목 추가, 커밋 및 배포 `.magento.env.yaml file` 클라우드 환경으로 가져갑니다.

>[!TIP]
>
>를 사용한 환경 변수 구성 및 관리에 대한 자세한 내용 `.magento.env.yaml` 파일, 참조 [배포를 위한 환경 변수 구성](https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/configure/env/configure-env-yaml.html).

### Commerce 이벤트 통합 구성

다음 작업을 완료하여 Commerce 이벤트 통합을 구성합니다. 자세한 지침은 [Commerce에 대한 이벤트 Adobe I/O](https://developer.adobe.com/commerce/extensibility/events/project-setup/) 개발자 설명서.

1. [App Builder 프로젝트 만들기](https://developer.adobe.com/commerce/extensibility/events/project-setup/) 상거래 인스턴스에서 이벤트 데이터를 수신합니다.

   Commerce 관리에서 통합을 구성하려면 App Builder 프로젝트의 자격 증명과 구성 데이터가 필요합니다.

1. Adobe I/O 이벤트를 사용하도록 Adobe Commerce을 구성합니다.

   - [Adobe I/O 이벤트 서비스에 대한 저장소 구성 설정 업데이트](https://developer.adobe.com/commerce/extensibility/events/configure-commerce/#begin-configuring-events-on-commerce).

   - [상거래 이벤트를 보내도록 이벤트 공급자 구성](https://developer.adobe.com/commerce/extensibility/events/configure-commerce/#create-an-event-provider-and-complete-the-commerce-configuration).

1. [Commerce 인스턴스에서 이벤트 데이터를 수신하도록 App Builder 프로젝트 업데이트](https://developer.adobe.com/commerce/extensibility/events/configure-commerce/#subscribe-and-register-events).

   Commerce 인스턴스에서 이벤트를 등록하거나 구독하지 않습니다. Commerce 애플리케이션에 대한 이벤트 공급자를 구성할 때 이벤트 등록이 App Builder 프로젝트에 푸시됩니다.

   이벤트 공급자를 App Builder 프로젝트에 연결한 후 `observer.uex_commerce_instance_update` 이벤트를 만들고 변경 사항을 저장합니다.

1. 연결을 설정하려면 이벤트 공급자를 통해 소비자에게 이벤트를 보냅니다.

   - 로컬 클라우드 프로젝트 디렉터리의 명령줄에서 [ssh를 사용하여 Commerce 애플리케이션 서버에 연결](https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/develop/secure-connections.html#connect-to-a-remote-environment).

     ```bash
     magento-cloud ssh
     ```

   - Adobe Commerce CLI를 사용하여 Admin Unified Experience 확장 의 상태를 확인하여 이벤트 데이터를 보냅니다.

     ```bash
     bin/magento bin/magento admin:uex:status
     ```

### 통합 테스트

Commerce 관리자가 Experience Cloud에 로그인하여 사용 가능한 Commerce 프로젝트를 보고 각 프로젝트의 관리 및 Storefront에 액세스할 수 있는지 확인합니다.

1. [Experience Cloud에 로그인](https://experiencecloud.adobe.com/library) 상거래 인스턴스와 연결된 Adobe ID 및 조직을 사용합니다.

   ![Experience Cloud 홈 페이지에서 Commerce 프로젝트에 액세스](./assets/admin-uex-home-page.png){width="600" zoomable="yes"}

1. 을(를) 선택하여 사용 가능한 상거래 프로젝트 보기 **[!UICONTROL Commerce]**.

   ![Experience Cloud을 위한 Commerce 프로젝트 작업 영역](./assets/admin-uex-commerce-projects-home.png){width="600" zoomable="yes"}

1. 을 선택하여 인스턴스에 대한 관리자를 엽니다. **[!UICONTROL Open]**.

   ![Experience Cloud 통합이 활성화된 상거래 관리자 보기](./assets/admin-dashboard.png){width="600" zoomable="yes"}

1. 예상대로 관리 작업을 수행할 수 있는지 확인합니다.

   상거래 관리자의 워크플로는 동일한 프로세스를 따라야 합니다. Experience Cloud 통합을 활성화한 후 워크플로우 변경 또는 오류가 발생하는 경우 Commerce 시스템 관리자에게 문의하거나 [Adobe 지원 티켓 제출](https://experienceleague.adobe.com/docs/commerce-knowledge-base/kb/help-center-guide/magento-help-center-user-guide.html#submit-ticket).

Experience Cloud 통합을 구성한 후 관리자 계정이 Experience Cloud을 통해 Commerce 프로젝트에 액세스할 수 있도록 올바르게 프로비저닝되었는지 확인합니다. 다음을 참조하십시오 [관리자 사용자 관리](/help/getting-started/admin-unified-experience-integration-manage.md#manage-admin-user-accounts).
