---
title: 코드 조각
description: 특정 에디션에 적용되는 기능이나 페이지를 참고하기 위해 노트 및 시각적 요소를 재사용함
source-git-commit: 0ffeaa42e0207322da1b55a9fd6b6b2cf24ff4ba
workflow-type: tm+mt
source-wordcount: '640'
ht-degree: 0%

---

# 코드 조각

## EE 전용 기능 {#ee-feature}

<table style="border:1px solid red">
<tr><td><img alt="Adobe Commerce 기능" src="../assets/adobe-logo.svg" width="20" height="20" /> Adobe Commerce의 전용 기능(<a href="https://experienceleague.adobe.com/docs/commerce-admin/user-guides/home.html?lang=ko#product-editions">자세히 알아보기</a>)</td></tr>
</table>

## B2B 전용 기능 {#b2b-feature}

<table style="border:1px solid green">
<tr><td><img alt="Adobe Commerce B2B 기능" src="../assets/b2b.svg" width="20" height="20" /> <a href="https://experienceleague.adobe.com/docs/commerce-admin/b2b/introduction.html?lang=ko">Adobe Commerce B2B</a>에서만 사용할 수 있는 전용 기능</td></tr>
</table>

## CE 전용 기능 {#ce-feature}

<table style="border:1px solid orange">
<tr><td><img alt="Magento Open Source 기능" src="../assets/open-source.svg" width="20" height="20" /> Magento Open Source에는 대체 메서드가 필요합니다(<a href="https://experienceleague.adobe.com/docs/commerce-admin/user-guides/home.html?lang=ko#product-editions">자세히 알아보기</a>).</td></tr>
</table>

## IMS 관리자 인증 메모 {#ims-admin-note}

>[!NOTE]
>
>Adobe ID을 보유하고 있으며 Adobe Commerce 및 Adobe 비즈니스 제품에 간소화된 로그인을 원하는 Adobe Commerce 판매자는 Commerce 관리자 인증을 Adobe IMS 인증 워크플로와 통합할 수 있습니다. Commerce 스토어에 대해 이 통합이 활성화되면 각 관리 사용자는 로그인하기 위해 Commerce 계정 자격 증명이 아닌 Adobe 자격 증명을 사용해야 합니다. [Adobe IMS와 Adobe Commerce 통합 개요](/help/getting-started/adobe-ims-integration-overview.md)를 참조하십시오.

## GTag API 참고 {#gtag-api-note}

>[!NOTE]
>
>2.4.5 릴리스부터 Google 서비스 통합이 GTag API 사용을 지원하도록 업데이트됩니다. GTag는 웹 페이지에 대한 Google 기능과 통합하기 위한 통합 메커니즘으로, Google Services를 통해 컨텐츠를 추적하고 관리할 수 있는 최신 기능과 기회를 지원합니다.

## URL 재작성 자동 건너뛰기 메모 {#url-rewrite-skip}

>[!NOTE]
>
>자동 리디렉션이 활성화되어 있고 카테고리를 저장하면 모든 제품 및 카테고리 재쓰기가 실시간으로 생성되고 기본적으로 재작성 테이블에 저장됩니다. 이 프로세스는 많은 지정된 제품이 있는 카테고리의 성능 문제를 크게 초래할 수 있습니다. 해결 방법은 이 기본값을 변경하고 카테고리 저장을 위해 제품의 카테고리/제품 URL 재작성 생성을 건너뛰는 것입니다. 이 경우 표준 제품 URL에 대해서만 제품 재작성이 생성됩니다. 자세한 내용은 [자동 제품 리디렉션](/help/merchandising-promotions/url-redirect-product-automatic.md)을 참조하세요.

## URL 재작성 매개 변수 참고 {#url-rewrite-params}

>[!IMPORTANT]
>
>리디렉션 과정에서 URL에 지정된 모든 GET 매개 변수는 보안상의 이유로 제거됩니다.

## 새 가격 규칙 {#new-price-rule}

>[!NOTE]
>
>가격 규칙은 다른 시스템 규칙과 함께 자동으로 처리됩니다. 처리 빈도는 [cron 구성](https://experienceleague.adobe.com/docs/commerce-operations/configuration-guide/cli/configure-cron-jobs.html?lang=ko)에 따라 다릅니다. 가격 규칙을 만들 때 시스템에 들어갈 충분한 시간을 허용합니다. 시스템에 있는지 확인하려면 규칙을 테스트하십시오.

## 구성 설정 {#config}

저장소 구성 설정에 액세스하려면 _관리_ 사이드바에서 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**&#x200B;을(를) 선택하십시오.

## UPS API 사용 중단 {#ups-api}

>[!IMPORTANT]
>
>2024년 6월부터 Adobe Commerce 판매자는 더 이상 현재 UPS 통합과 거래할 수 없습니다. 이는 기본 Adobe Commerce 통합에서 사용하는 UPS(United Parcel Service) API가 현재 필요한 OAuth 2.0 보안 모델을 지원하지 않기 때문입니다. 통합을 사용하려면 [UPS 개발자 플랫폼에서 애플리케이션을 만들고](https://developer.ups.com/get-started)하여 OAuth 2.0에 필요한 자격 증명을 얻으십시오. Commerce UPS 배송 구성에서 새 자격 증명을 `username` 및 `password`(으)로 사용합니다. 보안 모델 변경에 대한 자세한 내용은 [개발자 포털 액세스 키 마이그레이션 안내서_](https://developer.ups.com/oauth-developer-guide)를 참조하십시오. <br/>
>
>판매자는 SOAP API에서 OAuth 2.0 인증 프로토콜을 지원하는 RESTful API로 마이그레이션하려면 스토어에 [품질 패치 업데이트를 적용](https://experienceleague.adobe.com/docs/commerce-knowledge-base/kb/troubleshooting/known-issues-patches-attached/ups-shipping-method-integration-migration-from-soap-to-restful-api.html?lang=ko)해야 합니다.


## 사용 가능한 설명서 {#docs-links}

| 설명서 리소스 | 설명 |
|----------------------- | ----------- |
| [Adobe Commerce 2.4 관리 사용 안내서](../landing/home.md) | 관리자에서 작업하는 상인을 위한 설명서 및 리소스입니다. |
| [Adobe Commerce 설명서용 서비스](https://experienceleague.adobe.com/docs/commerce/user-guides/home.html?lang=ko) | 판매자가 비즈니스의 주요 구성 요소를 스토어와 통합하는 데 도움이 되는 머천다이징 서비스 컬렉션을 지원하는 설명서입니다. |
| [Cloud Infrastructure의 Commerce 안내서](https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/overview.html?lang=ko) | 관리되고 자동화된 호스팅 클라우드 플랫폼에서의 Adobe Commerce 배포에 대한 단계별 절차. |
| [Adobe Commerce 2.4 Operational Guides](https://experienceleague.adobe.com/docs/commerce-operations/operational-guides/home.html?lang=ko) | Adobe Commerce on Cloud 및 온프레미스 프로젝트를 개발, 배포 및 유지 관리하기 위한 개념, 프로세스, 도구 및 모범 사례에 대한 시스템 설명서입니다. |
| [Adobe Commerce 2.4 개발자 설명서](https://developer.adobe.com/commerce/docs) | Adobe Commerce을 사용자 정의하고 타사 시스템과 통합하는 데 사용되는 개발자 중심의 설명서입니다. |

{style="table-layout:auto"}

## B2B 호환성 {#b2b-compatibility}

>[!IMPORTANT]
>
>Adobe Commerce B2B 버전 1.4.2+는 PHP 8.2와 호환됩니다. Commerce 인스턴스를 버전 2.4.7+로 업그레이드하는 경우 인스턴스가 PHP 버전 8.2를 사용하여 Adobe Commerce B2B 릴리스와의 호환성을 유지하는지 확인하십시오. 또한 B2B 1.4.2+ 릴리스는 [GraphQL Application Server](https://experienceleague.adobe.com/ko/docs/commerce-operations/performance-best-practices/concepts/application-server)를 지원하지 않습니다.
