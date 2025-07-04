---
title: Commerce용 AEM Assets 통합 설정
description: 스토어에 대한 Commerce 에셋을 관리하기 위해 Experience Manager Assets 환경을 설정하고 구성하는 방법에 대해 알아봅니다.
feature: CMS, Media, Configuration
exl-id: 699f517e-1545-4c22-aa8d-9c8d60d352af
badgePaas: label="PaaS만" type="Informative" url="https://experienceleague.adobe.com/ko/docs/commerce/user-guides/product-solutions" tooltip="Adobe Commerce 온 클라우드 프로젝트(Adobe 관리 PaaS 인프라) 및 온프레미스 프로젝트에만 적용됩니다."
source-git-commit: 57a913b21f4cbbb4f0800afe13012ff46d578f8e
workflow-type: tm+mt
source-wordcount: '258'
ht-degree: 0%

---

# Commerce용 AEM Assets 통합 설정

Commerce용 Adobe Experience Manager Assets 통합을 설정하려면 관리 액세스 권한이 있어야 애플리케이션 및 환경 구성을 사용자 정의할 수 있습니다.

- AEM Assets as a Cloud Service 환경이 프로비저닝되는 Cloud Manager 프로그램에 대한 관리 액세스 권한.

- Adobe Commerce 환경에 대한 관리 액세스 및 인증에 필요한 API 키를 검색하거나 생성하는 기능입니다.

## 통합 사용 요구 사항

이러한 통합을 활용하려면 기업은 다음 요구 사항을 충족해야 합니다.

- Adobe Commerce, Adobe Experience Manager Assets 및 [AEM Dynamic Media](https://experienceleague.adobe.com/ko/docs/experience-manager-65/content/assets/dynamic/administering-dynamic-media)에 대한 활성 라이선스입니다.

- Adobe Commerce 2.4.5+

- Adobe Experience Manager은 [Adobe Experience Manager Assets as a Cloud Service](https://experienceleague.adobe.com/ko/docs/experience-manager-cloud-service/content/assets/overview)로 프로비전되었습니다.

- 통합을 구성하는 Adobe Commerce 사용자는 AEM Assets 프로젝트가 프로비저닝된 [IMS 조직](https://experienceleague.adobe.com/ko/docs/core-services/interface/administration/organizations#concept_EA8AEE5B02CF46ACBDAD6A8508646255)에 액세스할 수 있어야 합니다.

## 주요 이점

- **추가 비용 없음**—이 통합은 라이선스 요구 사항을 충족하는 판매자에게 무료로 제공됩니다.

- **공식 Adobe 솔루션** - Adobe에서 개발, 유지 관리 및 완전히 지원하여 안정성과 향후 플랫폼 개선 사항과의 정렬을 보장합니다.

- **Adobe 관리 지원 모델**—Adobe은 지원 및 문제 해결을 처리하므로 안심하고 문제를 해결할 수 있습니다.

## 다음 단계

Experience Manager Assets과 Commerce 통합을 활성화하는 3단계 프로세스입니다.

1. [AEM Assets 패키지 설치](aem-assets-configure-aem.md).

1. [Adobe Commerce 패키지 설치](aem-assets-configure-aem.md).

1. [통합 자산을 구성합니다](aem-assets-setup-synchronization.md).
