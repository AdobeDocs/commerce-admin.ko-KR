---
title: 로그 회전 구성
description: Commerce용 AEM Assets 통합에 대한 로그 순환을 구성합니다.
feature: CMS, Media, Integration
exl-id: f735d086-048c-4555-bc58-ac6736c281b0
badgePaas: label="PaaS만" type="Informative" url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="Adobe Commerce 온 클라우드 프로젝트(Adobe 관리 PaaS 인프라) 및 온프레미스 프로젝트에만 적용됩니다."
TQID: https://experienceleague.adobe.com/I6iWurcyEbPi3fJmBZAnvbPlZfOJiSS4yGR6j5xFsp4
product_v2: id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2: id: dac87252-6066-4d6e-a9d2-f6d84c323de7
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
level_v2: id: b5a62a22-46f7-4f0d-b151-3fc640bef588id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2: id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: ccaac3a13a346ce192a724efb3384ef2d612c980
workflow-type: tm+mt
source-wordcount: 157
ht-degree: 0%

---

# Experience Manager Assets 구성

Commerce용 AEM Assets 통합은 Commerce 인스턴스에 다음 로그 파일을 제공합니다.

- `/var/log/aem-assets-integration.log`
- `/var/log/aem-assets-integration-errors.log`

이러한 로그가 너무 커지지 않도록 하려면 시스템 관리자에게 로그 파일 순환 일정을 확인하도록 요청하십시오. 일부 환경에서는 로그 파일이 자동으로 회전되지만 다른 환경에서는 로그 회전을 수동으로 설정해야 합니다. 자세한 내용은 다음 항목을 참조하십시오.

- Adobe Commerce 온-프레미스 설치의 경우 시스템 관리자에게 [로그 순환](https://experienceleague.adobe.com/docs/commerce-operations/installation-guide/next-steps/configuration.html#server-settings)을 설정하도록 요청하세요.
- 클라우드 인프라 프로젝트의 Adobe Commerce에 대해서는 [로그 보기 및 관리](https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/develop/test/log-locations.html)를 참조하십시오.

