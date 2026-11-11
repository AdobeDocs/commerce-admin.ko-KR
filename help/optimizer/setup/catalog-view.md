---
title: 카탈로그 보기
description: 카탈로그 보기가 무엇이며 이를 만들어 비즈니스 구조, 정책 및 가격별로 제품 카탈로그를 구성하는 방법에 대해 알아봅니다.
role: Admin, Developer
recommendations: noCatalog
badgeSaas: label="SaaS만" type="Positive" url="https://experienceleague.adobe.com/ko/docs/commerce/user-guides/product-solutions" tooltip="CCDM으로 프로비저닝된 Adobe Commerce as a Cloud Service 인스턴스(Adobe 관리 SaaS 인프라)에만 적용됩니다."
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
    internal-label: Commerce
  - id: de2e2e68-c5d7-4efe-be7b-27528698f06b
    internal-label: Commerce as a Cloud Service
topic_v2:
  - id: a004cc84-67b9-4a33-a3a7-8ec7273ef4dc
    internal-label: Metadata
  - id: cdd65e7e-8839-44a2-bc21-0e03623b5dd1
    internal-label: Optimization
  - id: e0eb8757-182f-49f3-94a4-1587d16f5094
    internal-label: Personalization
source-git-commit: 8fbcfcdeb13c452a45e872d939e129703ac5abab
workflow-type: tm+mt
source-wordcount: '997'
ht-degree: 0%
---

# 카탈로그 보기

카탈로그 보기는 상점이 검색할 수 있는 제품 및 가격을 정의합니다. CCDM(Composable Catalog Data Model)으로 프로비저닝된 Adobe Commerce as a Cloud Service 인스턴스에서 카탈로그 보기는 Adobe Commerce Optimizer을 구동하는 것과 동일한 카탈로그 기반을 사용합니다.

카탈로그 보기는 카탈로그 소스, 정책 및 가격 장부를 결합하여 상점의 카탈로그 컨텍스트를 정의합니다. 정책은 사용 가능한 제품 분류를 결정합니다. 머천다이징 규칙은 해당 분류 내의 제품이 프로모션되고 순위가 지정되는 방법을 제어하며 모든 카탈로그 보기에 적용되거나 특정 보기에 맞게 조정될 수 있습니다. [머천다이징 규칙 만들기](../merchandising/rules/add.md)를 참조하십시오.

Commerce 파운데이션은 제품과 가격에 대한 진실의 원천으로 남아 있습니다. 제품 및 가격 데이터는 별도의 커넥터 설치 또는 App Builder 앱 없이 기본 Adobe Commerce as a Cloud Service 통합을 통해 CCDM에 대한 한 가지 방법을 동기화합니다. 웹 사이트, 스토어 및 스토어 뷰 구성은 장바구니, 체크아웃, 프로모션, 고객, 주문 및 결제를 관리하는 Commerce Foundation에 유지됩니다.

>[!NOTE]
>
>CCDM으로 프로비저닝된 인스턴스의 경우 [Adobe 통합 경험의 Commerce 관리](../../getting-started/admin-unified-experience.md)를 사용하여 카탈로그 보기 및 정책을 구성하고 동기화된 가격표를 카탈로그 보기와 연결합니다. 라이브 검색 및 제품 추천과 함께 카탈로그 서비스를 사용하는 인스턴스는 이러한 카탈로그 관리 화면에 액세스할 수 없습니다.

## 카탈로그 보기 작동 방식

카탈로그 뷰는 Storefront 컨텍스트에 대한 카탈로그 데이터와 구성을 취합합니다. 비즈니스 단위, 브랜드, 지역 또는 기타 상점 경험을 나타내는 데 사용할 수 있습니다.

- **[카탈로그 원본](catalog-sources.md)**&#x200B;에서 카탈로그 경험에 대한 제품 데이터를 제공합니다.
- **[정책](policies.md)**&#x200B;은(는) 카탈로그 보기에 대한 제품 데이터를 필터링합니다.
- **[가격 장부](pricebooks.md)**&#x200B;는 카탈로그 보기와 관련된 가격 데이터를 제공합니다.

카탈로그 보기가 Adobe Commerce as a Cloud Service의 웹 사이트, 스토어 및 스토어-뷰 구조를 바꾸지 않습니다. Commerce Foundation에서는 이러한 구조 및 트랜잭션 작업을 계속 관리합니다.

카탈로그 데이터는 Commerce Foundation에서 CCDM으로 한 가지 방식으로 동기화됩니다. CCDM은 상점 카탈로그 경험 및 제품 검색을 지원합니다. Commerce Foundation에서는 장바구니, 체크아웃, 프로모션, 고객 및 주문을 계속 처리합니다.

## 시작하기 전에

카탈로그 보기를 구성하기 전에:

- [Adobe Commerce as a Cloud Service 인스턴스가 CCDM을 사용하는지 확인](../overview.md).
- Storefront에 필요한 카탈로그 데이터가 채워져 있고 [동기화됨](data-sync.md)인지 확인하십시오.
- Storefront 컨텍스트에 필요한 [카탈로그 원본](catalog-sources.md), [정책](policies.md) 및 [가격 책](pricebooks.md)을(를) 식별합니다.
- B2C 카탈로그 보기를 수동으로 생성할지 또는 기본 동기화에서 생성된 B2B 카탈로그 보기를 검토할지 여부를 결정합니다.

>[!NOTE]
>
>B2B 구현의 경우 기본 동기화는 Commerce Foundation의 B2B 구성에서 카탈로그 보기, 정책 및 가격 장부를 생성합니다. 이렇게 자동으로 생성된 구조의 복제본을 수동으로 만들지 마십시오.

## B2C 구현을 위한 카탈로그 보기 만들기

B2C 구현에서 카탈로그 보기를 수동으로 구성해야 하는 경우 이 워크플로우를 사용하십시오.

1. 통합 경험에서 [Commerce 관리자](../../getting-started/admin-unified-experience.md)에 로그인하고 CCDM으로 프로비저닝된 Adobe Commerce as a Cloud Service 인스턴스를 선택합니다.
1. 왼쪽 탐색에서 **[!UICONTROL Catalog]** > **[!UICONTROL Catalog Views]**(으)로 이동합니다.
1. **[!UICONTROL Create catalog view]**&#x200B;을(를) 선택합니다.
1. 카탈로그 보기의 이름을 입력합니다.
1. Storefront 컨텍스트의 [카탈로그 원본](catalog-sources.md)을(를) 선택하십시오.
1. 관련 [정책](policies.md)을(를) 카탈로그 보기와 연결합니다.
1. [가격 장부 가용성을 구성](pricebooks.md)하여 관련 가격 장부를 카탈로그 보기와 연결합니다.
1. 카탈로그 보기를 만듭니다.

## B2B 카탈로그 보기

B2B 구현의 경우 기본 동기화는 Commerce Foundation의 B2B 구성에서 카탈로그 보기, 정책 및 가격 장부를 생성합니다. CCDM에서 중복 구조를 수동으로 만드는 대신 Commerce Foundation에서 기본 B2B 카탈로그 및 회사 관계를 관리합니다.

설치 지침은 [공유 카탈로그 만들기](../../b2b/catalog-shared-create.md) 및 [공유 카탈로그에 회사 할당](../../b2b/catalog-shared-assign-companies.md)을 참조하십시오.

B2B 관계를 구성한 후:

1. [동기화](data-sync.md)가 완료되었는지 확인합니다.
2. [통합 환경의 Commerce 관리](../../getting-started/admin-unified-experience.md)에서 생성된 카탈로그 보기, [정책](policies.md) 및 [가격 책자](pricebooks.md)를 검토하십시오.
3. 상점에 회사의 예상 제품 구성 및 가격이 표시되는지 확인합니다.
4. 장바구니 추가, 장바구니 및 체크아웃을 테스트하여 제품 가용성 및 거래 가격이 의도한 B2B 구성과 일치하는지 확인합니다.

## 가격 장부 및 체크아웃

가격 장부는 카탈로그 보기를 통해 사용할 수 있는 가격 데이터를 제공합니다. Adobe Commerce as a Cloud Service에서 Commerce Foundation은 가격에 대한 소스로 유지되며 가격 데이터는 기본 통합을 통해 CCDM과 동기화됩니다. 카탈로그 보기를 구성할 때 CCDM에서 독립적으로 가격을 작성하지 않고 해당하는 동기화된 가격 장부를 사용합니다.

장바구니와 체크아웃은 Commerce Foundation 가격을 사용합니다. 표시된 상점 가격이 해당 장바구니 및 체크아웃 가격과 일치하는지 확인하십시오.

## 카탈로그 보기 검토 및 유효성 검사

카탈로그 보기를 구성한 후 전체 상점 경험을 확인합니다.

- 의도한 카탈로그 데이터가 [동기화됨](data-sync.md)인지 확인하십시오.
- 카탈로그 보기가 의도한 [정책](policies.md) 및 [가격 책](pricebooks.md)과 연결되어 있는지 확인하십시오.
- 상점이 예상되는 제품 종류를 반환하는지 확인합니다.
- 표시된 가격을 해당 Commerce Foundation 가격과 비교하여 확인합니다.
- 장바구니 추가, 장바구니 및 체크아웃을 테스트합니다.

B2B 구현의 경우 동기화에 의해 생성된 카탈로그 구조가 의도한 회사 및 카탈로그 구성과 일치하는지 확인합니다.

## 문제 해결

### 상점에서 제품이 누락되었습니다

- [인스턴스가 CCDM을 사용하는지 확인](../overview.md).
- 카탈로그 데이터에 [동기화됨](data-sync.md)이 있는지 확인하십시오.
- 상점 전면이 의도한 카탈로그 컨텍스트를 사용하고 있는지 확인합니다.
- 카탈로그 보기와 연결된 [정책](policies.md)을(를) 검토하십시오.

### 표시된 가격이 예기치 않습니다.

- 의도한 [가격 장부](pricebooks.md)가 카탈로그 보기와 연결되어 있는지 확인하십시오.
- 가격 데이터가 [동기화됨](data-sync.md)이고 Commerce Foundation과 일치하는지 확인하십시오.

  웹 사이트 및 고객 그룹 가격 매핑은 [가격 장부](pricebooks.md)를 참조하십시오.

- 장바구니와 체크아웃에서 가격을 다시 확인합니다.

### CCDM 카탈로그 화면이 Commerce 관리자에 표시되지 않음

[선택한 인스턴스가 CCDM을 사용하는지 확인](../overview.md) 및 [통합 경험의 Commerce 관리자에 액세스 중인지 확인](../../getting-started/admin-unified-experience.md). 카탈로그 서비스 v1을 실행하는 인스턴스에는 CCDM 관리 화면이 없습니다.

## 관련 콘텐츠

- [Adobe Commerce as a Cloud Service 시작하기](https://experienceleague.adobe.com/ko/docs/commerce/cloud-service/getting-started)
- [Adobe Commerce B2B 공유 카탈로그 개요](../../b2b/catalog-shared.md)
- [Adobe Commerce as a Cloud Service 릴리스 노트](https://experienceleague.adobe.com/ko/docs/commerce/cloud-service/release-notes)
- [카탈로그 동기화](data-sync.md)
