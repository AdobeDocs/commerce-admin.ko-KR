---
title: 역할별 카탈로그 머천다이징 작업
description: CCDM으로 프로비저닝된 Adobe Commerce as a Cloud Service 인스턴스로 작업하는 관리자, 개발자 및 머천다이저를 위한 작업 지침을 찾으십시오.
role: Admin, Developer
recommendations: noCatalog
badgeSaas: label="SaaS만" type="Positive" url="https://experienceleague.adobe.com/ko/docs/commerce/user-guides/product-solutions" tooltip="CCDM으로 프로비저닝된 Adobe Commerce as a Cloud Service 인스턴스(Adobe 관리 SaaS 인프라)에만 적용됩니다."
TQID: 'https://experienceleague.adobe.com/0PmobUkdEWspxuRSaIPL8vS1ojDDZ3gw-L-3SfPmJAg'
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
    internal-label: Commerce
  - id: de2e2e68-c5d7-4efe-be7b-27528698f06b
    internal-label: Commerce as a Cloud Service
feature_v2:
  - id: cc04bd17-78d5-5120-8c3d-1b8a57e49280
    internal-label: Integration
  - id: dec06508-d41f-555a-87e8-29e8bcdfa95a
    internal-label: Recommendations
  - id: e8818fe6-9c8b-4bc0-9ef8-377a10b7bc75
    internal-label: Architecture
  - id: f37757d8-3174-5335-b977-1161792f965d
    internal-label: Personalization
subfeature_v2:
  - id: f8ddfd3b-6194-46e8-a176-0e918039be56
    internal-label: Cloud architecture
topic_v2:
  - id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
    internal-label: Implementation
  - id: c1579802-ddd4-4214-8a91-97b2066abe11
    internal-label: Troubleshooting
  - id: dba482e5-29a8-4127-afa2-c4b913512ef8
    internal-label: Data and analytics
  - id: df401a2a-327d-468c-a5e4-b7b7ccd071a0
    internal-label: Data integration
  - id: e0eb8757-182f-49f3-94a4-1587d16f5094
    internal-label: Personalization
source-git-commit: 742236e7fdb26c56a80f66a44b0a4960210f4dac
workflow-type: tm+mt
source-wordcount: '548'
ht-degree: 0%
---

# 역할별 카탈로그 머천다이징 작업

이 작업 참조를 사용하여 CCDM(Composable Catalog Data Model)으로 프로비저닝된 Adobe Commerce as a Cloud Service 인스턴스에서 카탈로그 데이터 구성, 상점 통합, 머천다이징 관리 및 성능 검토를 위한 지침을 찾을 수 있습니다.

책임은 구현에 따라 다릅니다. 다음 섹션에서는 일반적으로 작업을 수행하는 역할별로 작업을 그룹화합니다.

- 관리자는 Commerce Foundation에서 제품, 가격 및 B2B 구성을 관리합니다.
- 개발자는 Storefront 통합을 구성하고 카탈로그 요청 및 동작 데이터 수집을 확인합니다.
- 머천다이저는 제품 검색 및 권장 사항을 구성하고 보고를 사용하여 머천다이징 관련 결정을 알립니다.

제품 및 가격 데이터는 기본 Adobe Commerce as a Cloud Service 통합을 통해 CCDM과 동기화됩니다. 별도의 커넥터 설치 또는 App Builder 앱이 필요하지 않습니다.

## 카탈로그 및 상점 준비

구현에 적용되는 작업을 완료합니다. B2C 카탈로그 보기는 수동으로 만들 수 있습니다. B2B 카탈로그 보기, 정책 및 가격 장부는 Commerce Foundation의 B2B 구성에서 생성됩니다.

| 작업 | 설명 | 리소스 |
| --- | --- | --- |
| **제품 및 가격 구성** | Commerce Foundation에서 제품 및 가격을 관리합니다. 가격 데이터는 CCDM에 가격 장부로 동기화됩니다. CCDM에서 가격을 독립적으로 작성하지는 않습니다. | [제품 목록](../catalog/products-list.md), [제품 만들기](../catalog/product-create.md), [가격 범위](../catalog/catalog-price-scope.md) 및 [고급 가격 책정](../catalog/pricing-advanced.md) |
| **저장소 보기 구성** | Commerce Foundation에서 상점에 필요한 스토어 뷰 및 지역화된 제품 데이터를 구성합니다. | [스토어 보기](../stores-purchase/store-views.md) |
| **B2B 공유 카탈로그 및 회사 설정** | B2B 구현의 경우 생성된 카탈로그 구성을 검토하기 전에 Commerce Foundation에서 공유 카탈로그 및 회사 관계를 구성합니다. | [공유 카탈로그](../b2b/catalog-shared.md) 및 [회사](../b2b/account-companies.md) |
| **B2C 카탈로그 보기 및 정책 구성** | 카탈로그 보기를 만들고 사용 가능한 제품 분류를 정의하는 정책을 선택합니다. 각 뷰에 해당 동기화 가격 장부를 연관시킵니다. | [카탈로그 보기](./setup/catalog-view.md) |
| **B2B 카탈로그 보기 검토** | 기본 동기화가 예상 카탈로그 보기, 정책 및 가격 장부를 생성했는지 확인합니다. 중복 구조를 수동으로 만들지 않고 Commerce Foundation에서 기본 B2B 구성을 관리합니다. | [B2B 카탈로그 보기](./setup/catalog-view.md#b2b-catalog-views) |
| **상점 구성** | 의도한 카탈로그 컨텍스트를 요청하도록 Storefront를 구성합니다. 사용자 지정 또는 기타 상점 통합의 경우 해당 카탈로그 요청 헤더를 검토하십시오. | [Storefront 구성](https://experienceleague.adobe.com/en/tools/commerce-storefront/setup/configuration/commerce-configuration/) |

머천다이징을 구성하기 전에 상점이 예상 제품과 가격을 반환하는지 확인하십시오. 장바구니 추가, 장바구니 및 체크아웃을 테스트하여 거래 가격이 의도한 Commerce Foundation 구성과 일치하는지 확인합니다.

## 머천다이징 구성 및 성능 검토

| 작업 | 설명 | 리소스 |
| --- | --- | --- |
| **제품 검색 구성** | 머천다이징 규칙, 패싯 및 동의어를 설정합니다. 규칙은 모든 카탈로그 보기에 적용되거나 특정 보기에 맞게 조정할 수 있습니다. | [머천다이징 개요](./merchandising/overview.md) |
| **검색 설정 검토** | 구현에 대한 검색 구성 및 사용 가능한 의미 체계 검색 옵션을 검토하십시오. | [머천다이징 설정](./settings.md) 및 [의미 체계 검색](./setup/semantic-search.md) |
| **권장 사항 구성** | 권장 사항 단위를 만들고 상점 첫 화면에서 구현에 필요한 동작 데이터를 수집하는지 확인합니다. | [권장 사항 개요](./merchandising/recommendations/overview.md) |
| **성과 검토** | 성공 지표 및 검색 성능 보고를 사용하여 상점 활동을 평가하고 머천다이징 결정을 알립니다. | [성공 지표](./manage-results/success-metrics.md) 및 [검색 성능](./manage-results/search-performance.md) |

## 다음 단계

머천다이징을 구성하고 성능을 검토한 후 필요에 따라 규칙, 패싯 및 권장 사항을 계속 모니터링하고 조정하여 상점 경험을 최적화하십시오.
