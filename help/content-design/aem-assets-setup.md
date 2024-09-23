---
title: AEM Assets 통합 설정
description: Adobe Commerce과 AEM Assets as a Cloud Service 간의 통합을 설정하는 요구 사항 및 단계에 대해 알아봅니다.
feature: CMS, Media, Configuration, Integration
source-git-commit: df21ea9a797a4f11d0104cf34134ced3bbabbdf4
workflow-type: tm+mt
source-wordcount: '241'
ht-degree: 0%

---


# AEM Assets 통합 설정

AEM Assets 환경을 설정하고 Commerce용 AEM Assets 통합을 설치 및 구성하여 고급 에셋 관리 기능을 활성화합니다.

통합이 활성화되면 관리자는 Experience Manager Assetsas a Cloud Service 를 트루 에셋 생성 및 관리를 위한 단일 소스로 사용하고 중앙 디지털 에셋 관리 도구(DAM)로 사용하여 Commerce 프로젝트에 대한 에셋을 생성, 관리, 구성 및 배포할 수 있습니다.

## 요구 사항

- Adobe Commerce 2.4.5+
   - PHP 8.1, 8.2, 8.3
   - 작성기: 2.x
- Adobe Experience Manager은 [Adobe Experience Manager Assets as a Cloud Service](https://experienceleague.adobe.com/ko/docs/experience-manager-cloud-service/content/assets/overview)(으)로 프로비저닝되었습니다.
- 통합을 구성하는 Adobe Commerce 사용자는 AEM Assets 프로젝트가 프로비저닝된 [IMS 조직](https://experienceleague.adobe.com/en/docs/core-services/interface/administration/organizations#concept_EA8AEE5B02CF46ACBDAD6A8508646255)에 액세스할 수 있어야 합니다.

## 통합 설정

>[!BEGINSHADEBOX]

**필수 구성 요소**

AEM Assets 통합을 설정하려면 관리 액세스 권한이 있어야 애플리케이션 및 환경 구성을 사용자 정의할 수 있습니다.

- AEM Assets as a Cloud Service 환경에 대한 Cloud Manager 액세스 권한이 프로비저닝되는 관리 액세스 프로그램입니다.
- Adobe Commerce 환경에 대한 관리 액세스 및 인증에 필요한 API 키를 검색하거나 생성하는 기능입니다.

>[!ENDSHADEBOX]

Experience Manager Assets과 Commerce 통합을 활성화하는 3단계 프로세스입니다.

1. [Commerce 자산을 관리하도록 Experience Manager Assets 프로젝트를 구성](aem-assets-configure-aem.md).

1. [Experience Manager Assets 통합 확장 설치 및 Adobe Commerce 구성](aem-assets-configure-aem.md).

1. [자산 동기화 사용](aem-assets-setup-synchronization.md).
