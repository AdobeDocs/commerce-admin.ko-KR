---
title: AI 제품 검색 사전 요구 사항
description: 카탈로그 보강 및 PDP 보강 요구 사항을 검토하고 Adobe Commerce on cloud infrastructure 또는 온프레미스에 공유 보강 확장을 설치합니다.
role: Admin, Developer
source-git-commit: 591fca4f18862d289fb233997e8848cb4692d1e7
workflow-type: tm+mt
source-wordcount: '506'
ht-degree: 0%
---
# 사전 요구 사항

카탈로그 보강 또는 PDP 보강 기능을 사용하기 전에 모든 배포에 적용되는 요구 사항을 확인한 다음 Commerce 플랫폼에 대한 설정을 완료합니다.

## 모든 배포에 대한 요구 사항 {#all-deployments}

| 요구 사항 | 적용 대상 | 세부 사항 |
| --- | --- | --- |
| Edge에서 최적화 | PDP 보강 | 필수 여부. Edge에서 최적화 는 강화된 제품 데이터를 AI 에이전트에게 제공합니다. [Edge에서 최적화 가이드](https://experienceleague.adobe.com/ko/docs/brand-visibility/using/resources/optimize-at-edge/fastly-byocdn)를 참조하세요. |
| 로그 전달 | 두 워크플로우 | 선택 사항입니다. 에이전트 트래픽을 기반으로 데이터 보강 권장 사항을 활성화합니다. 이 기능이 없어도 제품 또는 제품 페이지를 수동으로 선택할 수 있습니다. [로그 전달 가이드](https://experienceleague.adobe.com/ko/docs/brand-visibility/using/log-forwarding/log-forwarding-overview)를 참조하세요. |
| 크롤링 가능 상점 | 카탈로그 강화 | 크롤링 기반 권장 사항 필수. LLM 기반 및 agentic 봇은 제품 페이지에 액세스할 수 있어야 합니다. |
| [!DNL Adobe Admin Console] 액세스 | 두 워크플로우 | 필수 여부. 설정하는 동안 [!DNL Adobe Commerce]이(가) 조직의 GenAI 라이더 상태를 확인합니다. 조직에서 GenAI 라이더를 옵트아웃하지 않은 경우 액세스할 수 있습니다. |

<!--
TBD (SME): The Optimize at Edge guide is a Brand Visibility reference, not a Commerce setup guide. Add Commerce-specific Optimize at Edge setup instructions (this might be automated by GA).
-->

## Commerce 플랫폼 설정 {#set-up}

>[!BEGINTABS]

>[!TAB 클라우드 인프라 또는 온-프레미스의 Commerce]

클라우드 인프라 또는 온프레미스의 [!DNL Adobe Commerce]에 대해 카탈로그 보강과 PDP 보강이 모두 가능한 공유 보강 확장을 설치합니다.

**시작하기 전:**

- PHP 8.3 이상에서 [!DNL Adobe Commerce] 2.4.7 이상 [릴리스 정보](release-notes.md)를 참조하세요.
- [!DNL Adobe IMS] 조직입니다. 조직에 Adobe IMS 통합 개요가 없으면 [Adobe IMS 통합 개요](https://experienceleague.adobe.com/ko/docs/commerce-admin/start/admin/ims/adobe-ims-integration-overview)를 참조하세요. 카탈로그 보강은 로그인한 관리자의 IMS 액세스 토큰을 사용합니다. Commerce 사용자 이름과 암호로만 로그인해도 이 토큰이 제공되지 않습니다.
- Commerce 응용 프로그램 서버에 대한 명령줄 액세스 및 `repo.magento.com`에서 패키지를 다운로드할 수 있는 권한입니다.

**설치 및 확인:**

1. [!DNL Live Search]과(와) [!DNL Product Recommendations] 중 어느 것도 활성화되지 않은 경우 Commerce 프로젝트 디렉터리에서 [!DNL Catalog Service]을(를) 추가하십시오.

   ```bash
   composer require magento/catalog-service --no-update
   composer update magento/catalog-service
   ```

   [!DNL Catalog Service]은(는) [!DNL Live Search] 및 [!DNL Product Recommendations]과(와) 함께 자동으로 설치되므로, 두 서비스 중 하나가 활성화된 경우 이 단계를 건너뜁니다.

1. 다른 Commerce 서비스에 대해 아직 구성되지 않은 경우 API 키 및 SaaS 데이터 공간으로 [Commerce 서비스 커넥터](https://experienceleague.adobe.com/ko/docs/commerce/user-guides/integration-services/saas)를 구성하십시오.

1. 공유 데이터 보강 확장 추가:

   ```bash
   composer require magento/module-catalog-enrichment --no-update
   composer update magento/module-catalog-enrichment
   ```

1. 변경 사항 배포:

   - **클라우드 인프라:** 변경 내용을 커밋하고 `composer.json` 및 `composer.lock`에 푸시합니다.
   - **온-프레미스:** 응용 프로그램을 업그레이드하고 캐시를 지웁니다.

     ```bash
     bin/magento setup:upgrade
     bin/magento cache:clean
     ```

1. 관리자에서 **[!UICONTROL System]** > **[!UICONTROL Data Transfer]** > **[!UICONTROL Data Feed Sync Status]**(으)로 이동하여 Commerce에서 카탈로그 데이터를 내보내는지 확인합니다.

   성공적으로 전송된 제품 레코드 수는 소스 레코드와 일치해야 하며, 실패하거나 제출 대기 중이 아닙니다. 실패한 레코드의 경우 오류 세부 사항을 검토하고 문제를 해결한 다음 영향을 받는 레코드에 대한 재동기화를 예약하십시오.

1. **[!UICONTROL System]** > **[!UICONTROL Data Transfer]** > **[!UICONTROL Data Management Dashboard]**(으)로 이동하여 [!DNL Catalog Service]에서 필요한 카탈로그 데이터를 사용할 수 있는지 확인하십시오.

상태 세부 정보 및 문제 해결은 [데이터 피드 상태 모니터링](/help/systems/data-feed-sync-status.md#monitor-data-feed-status)을 참조하세요.

>[!TAB Adobe Commerce as a Cloud Service]

[!DNL Adobe Commerce as a Cloud Service]의 경우 계정 프로비저닝 중에 [!DNL Catalog Service] 설치, 카탈로그 보강 및 PDP 보강이 처리됩니다.

사용하려는 워크플로에 적용되는 [모든 배포에 대한 요구 사항](#all-deployments)을 완료하십시오.

<!-- TBD (SME): Confirm whether merchants on Adobe Commerce as a Cloud Service should verify catalog data on the Data Management Dashboard, and whether the IMS and Admin Console requirements apply. -->

>[!ENDTABS]

## 다음 단계 {#next-step}

[데이터 보강 설정을 구성](settings.md)하여 Commerce 인스턴스를 AI 제품 검색에 연결합니다.
