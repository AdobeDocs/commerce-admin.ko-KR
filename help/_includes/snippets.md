---
title: 코드 조각
description: 특정 에디션에 적용되는 기능이나 페이지를 참고하기 위해 노트 및 시각적 요소를 재사용함
source-git-commit: 911ae6ec19d7497bf5246b0aaa384471749c5d64
workflow-type: tm+mt
source-wordcount: '553'
ht-degree: 0%

---

# 코드 조각

## EE 전용 기능 {#ee-feature}

<table style="border:1px solid red">
<tr><td><img alt="Adobe Commerce 기능" src="../assets/adobe-logo.svg" width="20" height="20" /> Adobe Commerce에서만 사용할 수 있는 전용 기능 (<a href="https://experienceleague.adobe.com/docs/commerce-admin/user-guides/home.html#product-editions">자세히 알아보기</a>)</td></tr>
</table>

## B2B 전용 기능 {#b2b-feature}

<table style="border:1px solid green">
<tr><td><img alt="Adobe Commerce용 B2B 기능" src="../assets/b2b.svg" width="20" height="20" /> 독점 기능은 다음에서만 사용할 수 있습니다. <a href="https://experienceleague.adobe.com/docs/commerce-admin/b2b/introduction.html?lang=en">Adobe Commerce용 B2B</a></td></tr>
</table>

## CE 전용 기능 {#ce-feature}

<table style="border:1px solid orange">
<tr><td><img alt="Magento Open Source 기능" src="../assets/open-source.svg" width="20" height="20" /> Magento Open Source에 대체 방법 필요(<a href="https://experienceleague.adobe.com/docs/commerce-admin/user-guides/home.html#product-editions">자세히 알아보기</a>)</td></tr>
</table>

## IMS 관리자 인증 메모 {#ims-admin-note}

>[!NOTE]
>
>Adobe ID을 보유하고 있으며 Adobe Commerce 및 Adobe 비즈니스 제품에 간소화된 로그인을 원하는 Adobe Commerce 판매자는 Commerce 관리자 인증을 Adobe IMS 인증 워크플로와 통합할 수 있습니다. Commerce 스토어에 대해 이 통합이 활성화되면 각 관리 사용자는 로그인하기 위해 Commerce 계정 자격 증명이 아닌 Adobe 자격 증명을 사용해야 합니다. 다음을 참조하십시오 [Adobe IMS와 Adobe Commerce 통합 개요](/help/getting-started/adobe-ims-integration-overview.md).

## GTag API 참고 {#gtag-api-note}

>[!NOTE]
>
>2.4.5 릴리스부터 Google 서비스 통합이 GTag API 사용을 지원하도록 업데이트됩니다. GTag는 웹 페이지에 대한 Google 기능과 통합하기 위한 통합 메커니즘으로, Google Services를 통해 컨텐츠를 추적하고 관리할 수 있는 최신 기능과 기회를 지원합니다. 자세한 내용은 [Google Analytics 개발자 설명서](https://developers.google.com/analytics/devguides/collection/gtagjs).

## URL 재작성 자동 건너뛰기 메모 {#url-rewrite-skip}

>[!NOTE]
>
>자동 리디렉션이 활성화되어 있고 카테고리를 저장하면 모든 제품 및 카테고리 재쓰기가 실시간으로 생성되고 기본적으로 재작성 테이블에 저장됩니다. 이 프로세스는 많은 지정된 제품이 있는 카테고리의 성능 문제를 크게 초래할 수 있습니다. 해결 방법은 이 기본값을 변경하고 카테고리 저장을 위해 제품의 카테고리/제품 URL 재작성 생성을 건너뛰는 것입니다. 이 경우 표준 제품 URL에 대해서만 제품 재작성이 생성됩니다. 다음을 참조하십시오 [자동 제품 리디렉션](/help/merchandising-promotions/url-redirect-product-automatic.md) 추가 정보.

## URL 재작성 매개 변수 참고 {#url-rewrite-params}

>[!IMPORTANT]
>
>리디렉션 과정에서 보안상의 이유로 URL에 지정된 모든 GET 매개 변수가 제거됩니다.

## 새 가격 규칙 {#new-price-rule}

>[!NOTE]
>
>가격 규칙은 다른 시스템 규칙과 함께 자동으로 처리됩니다. 처리 빈도는 [cron 구성](https://experienceleague.adobe.com/docs/commerce-operations/configuration-guide/cli/configure-cron-jobs.html). 가격 규칙을 만들 때 시스템에 들어갈 충분한 시간을 허용합니다. 시스템에 있는지 확인하려면 규칙을 테스트하십시오.

## 구성 설정 {#config}

저장소 구성 설정에 액세스하려면 다음을 선택합니다 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**다음에서_&#x200B;관리자&#x200B;_사이드바.

## UPS API 사용 중단 {#ups-api}

>[!IMPORTANT]
>
>2024년 6월부터 Adobe Commerce 판매자는 더 이상 현재 UPS 통합과 거래할 수 없습니다. 이는 기본 Adobe Commerce 통합에서 사용하는 UPS(United Parcel Service) API가 현재 필요한 OAuth 2.0 보안 모델을 지원하지 않기 때문입니다. 이 변경 내용에 대한 자세한 내용은 [_개발자 포털 액세스 키 마이그레이션 안내서_](https://developer.ups.com/oauth-developer-guide). <br/>
>
>상인은 [품질 패치 업데이트 적용](https://experienceleague.adobe.com/docs/commerce-knowledge-base/kb/troubleshooting/known-issues-patches-attached/ups-shipping-method-integration-migration-from-soap-to-restful-api.html) SOAP API에서 OAuth 2.0 인증 프로토콜을 지원하는 RESTful API로 마이그레이션할 저장소에 전송됩니다.


## 사용 가능한 설명서 {#docs-links}

| 설명서 리소스 | 설명 |
|----------------------- | ----------- |
| [Adobe Commerce 2.4 Merchant 설명서](../landing/home.md) | Adobe Commerce에 대한 판매자 중심 설명서 |
| [Adobe Commerce 설명서를 위한 서비스](https://experienceleague.adobe.com/docs/commerce-merchant-services/user-guides/home.html) | 판매자가 비즈니스의 주요 구성 요소를 스토어와 통합하는 데 도움이 되는 서비스 컬렉션을 지원하는 설명서입니다. |
| [클라우드 인프라의 Commerce 안내서](https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/overview.html) | 관리되고 자동화된 호스팅 클라우드 플랫폼에서의 Adobe Commerce 배포에 대한 단계별 절차. |
| [Adobe Commerce 2.4 운영 안내서](https://experienceleague.adobe.com/docs/commerce-operations/operational-guides/home.html) | Adobe Commerce 프로젝트 개발, 배포 및 유지 관리를 위한 개념, 프로세스, 도구 및 모범 사례에 대한 시스템 설명서입니다. |
| [Adobe Commerce 2.4 개발자 설명서](https://developer.adobe.com/commerce/docs) | Adobe Commerce을 사용자 정의하고 서드파티 시스템과 통합하는 데 사용되는 개발자 중심의 설명서 |

{style="table-layout:auto"}
