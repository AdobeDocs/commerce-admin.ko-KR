---
title: 보안
description: 스토어와 데이터를 보호하는 데 사용할 수 있는 도구 및 손상을 감지하는 경우 보안 작업 계획에 대한 지침에 대해 알아봅니다.
exl-id: 10eef4ac-de83-4083-9ba3-e42c8eb33781
feature: Security, Site Management
source-git-commit: 671ec7015c37b24ca0acc615ae3715b8b870a453
workflow-type: tm+mt
source-wordcount: '391'
ht-degree: 0%

---

# 보안

저장소 보안 및 데이터 보안 유지 관리에는 여러 가지 방법이 있습니다.

- 설정 [이중 인증](security-two-factor-authentication.md)
- 구현 [CAPTCHA](security-captcha.md) 또는 [reCAPT차](security-google-recaptcha.md)
- 설정 [보안 검사](security-scan.md) Adobe Commerce 또는 Magento Open Source 설치의 각 도메인용.

다음 방문: [보안 센터](https://helpx.adobe.com/security.html){:target=&quot;_blank&quot;} 보안 경고 레지스트리에 참여하여 잠재적인 취약점에 대한 최신 뉴스를 확인하십시오. 보안 모범 사례에 대한 자세한 내용은 [상거래 사이트 및 인프라 보호](https://experienceleague.adobe.com/docs/commerce-operations/implementation-playbook/best-practices/launch/security-best-practices.html) 다음에서 _구현 플레이북_.

>[!NOTE]
>
>활성화된 스토어 [!DNL Adobe Identity Management Services] (IMS) 인증에는 기본 Adobe Commerce 및 Magento Open Source 2FA가 비활성화되어 있습니다. Adobe 자격 증명으로 Commerce 인스턴스에 로그인한 관리자는 많은 관리 작업에 대해 다시 인증할 필요가 없습니다. Adobe IMS는 관리자 가 현재 세션에 로그인할 때 인증을 처리합니다. 다음을 참조하십시오 [[!DNL Adobe Identity Management Service] (IMS) 통합 개요](../getting-started/adobe-ims-integration-overview.md).

![보안 센터](./assets/product-security-home.png){width="700" zoomable="yes"}

## 보안 작업 계획

Adobe Commerce 또는 Magento Open Source 사이트가 손상된 것으로 의심되는 경우 지체 없이 이 작업 계획을 따르십시오.

1. **진단**: 검사를 실행하여 Commerce 스토어의 보안 상태를 설정합니다. 상거래 [보안 검사](security-scan.md) 은(는) 알려진 보안 위험 및 맬웨어에 대해 상거래 사이트를 모니터링하고 보안 알림을 받을 수 있도록 하는 Adobe에서 제공하는 무료 서비스입니다.

1. **정리**: 고용 [자격을 갖춘 컨설턴트](https://solutionpartners.adobe.com/s/directory/?partner_type=1) 또는 모든 악성 코드의 사이트를 정리하는 온라인 서비스입니다. 일부 Commerce 커뮤니티 구성원은 다음을 추천합니다. [[!DNL Sucuri Website Malware Removal]](https://sucuri.net/website-antivirus/malware-removal). 다음 확인: `/media` 남은 실행 코드를 위한 폴더입니다. 알 수 없는 모든 관리자 사용자를 제거하고 모든 관리자 암호를 재설정합니다.

1. **Protect**: 상거래 설치를 최신 릴리스로 유지하십시오. 이전 버전을 사용하는 경우 모든 보안 패치를 사용할 수 있게 되면 적용합니다. 검토 및 팔로우 [상거래 보안 모범 사례](https://www.adobe.com/content/dam/cc/en/trust-center/ungated/whitepapers/experience-cloud/adobe-commerce-best-practices-guide.pdf). 구독 대상 [상거래 보안 경고](https://www.adobe.com/subscription/adbeSecurityNotifications.html).

1. **보고서**: Commerce에서 특정 취약성을 발견했다고 생각되는 경우 [Adobe 문제 열기](https://hackerone.com/adobe?type=team) 기술 세부 정보를 포함합니다.

1. **업그레이드**: 연중무휴 24시간 지원을 통해 안심하고 추가 지원을 받을 수 있도록 다음 대상으로의 업그레이드를 계획하십시오. [클라우드 아키텍처의 Adobe Commerce](https://business.adobe.com/products/magento/cloud-delivery.html) 지금.
