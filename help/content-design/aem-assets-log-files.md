---
title: 로그 회전 구성
description: Commerce용 AEM Assets 통합에 대한 로그 순환을 구성합니다.
feature: CMS, Media, Integration
exl-id: f735d086-048c-4555-bc58-ac6736c281b0
badgePaas: label="PaaS만" type="Informative" url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="Adobe Commerce 온 클라우드 프로젝트(Adobe 관리 PaaS 인프라) 및 온프레미스 프로젝트에만 적용됩니다."
source-git-commit: 57a913b21f4cbbb4f0800afe13012ff46d578f8e
workflow-type: tm+mt
source-wordcount: '124'
ht-degree: 0%

---

# Experience Manager Assets 구성

Commerce용 AEM Assets 통합은 Commerce 인스턴스에 다음 로그 파일을 제공합니다.

- `/var/log/aem-assets-integration.log`
- `/var/log/aem-assets-integration-errors.log`

이러한 로그가 너무 커지지 않도록 하려면 시스템 관리자에게 로그 파일 순환 일정을 확인하도록 요청하십시오. 일부 환경에서는 로그 파일이 자동으로 회전되지만 다른 환경에서는 로그 회전을 수동으로 설정해야 합니다. 자세한 내용은 다음 항목을 참조하십시오.

- Adobe Commerce 온-프레미스 설치의 경우 시스템 관리자에게 [로그 순환](https://experienceleague.adobe.com/docs/commerce-operations/installation-guide/next-steps/configuration.html#server-settings)을 설정하도록 요청하세요.
- 클라우드 인프라 프로젝트의 Adobe Commerce에 대해서는 [로그 보기 및 관리](https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/develop/test/log-locations.html)를 참조하십시오.
