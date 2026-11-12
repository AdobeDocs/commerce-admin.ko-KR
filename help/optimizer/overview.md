---
title: 머천다이징 서비스 개요
description: CCDM으로 프로비저닝된 Adobe Commerce as a Cloud Service 인스턴스의 카탈로그 구성, 머천다이징, 보고 및 모니터링 도구에 대해 알아봅니다.
recommendations: noCatalog
badgeSaas: label="SaaS만" type="Positive" url="https://experienceleague.adobe.com/ko/docs/commerce/user-guides/product-solutions" tooltip="CCDM으로 프로비저닝된 Adobe Commerce as a Cloud Service 인스턴스(Adobe 관리 SaaS 인프라)에만 적용됩니다."
exl-id: f9516d4c-fbae-4db2-a1a9-cda3684a8122
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
    internal-label: Commerce
  - id: de2e2e68-c5d7-4efe-be7b-27528698f06b
    internal-label: Commerce as a Cloud Service
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
    internal-label: Admin
  - id: f8a45b24-4be7-4f1b-909b-60d06b483a20
    internal-label: Leader
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
source-git-commit: a6a5a899ba60097bd6baf2a5de14063a0af2f313
workflow-type: tm+mt
source-wordcount: '710'
ht-degree: 0%
---
# CCDM을 통한 머천다이징 서비스 개요

CCDM(Composable Catalog Data Model)으로 프로비저닝된 Adobe Commerce as a Cloud Service 인스턴스는 [Adobe 통합 경험의 Commerce 관리](../getting-started/admin-unified-experience.md)에서 카탈로그 구성, 머천다이징, 보고 및 모니터링 도구를 제공합니다. CCDM은 Adobe Commerce Optimizer을 지원하는 것과 동일한 카탈로그 기반입니다.

머천다이징 서비스를 사용하여 다음과 같은 작업을 수행할 수 있습니다.

- Adobe Commerce as a Cloud Service 인스턴스의 카탈로그 데이터를 사용하여 상점 경험을 지원합니다.
- 카탈로그 보기 및 정책을 구성하여 상점 제품 분류를 정의합니다.
- 모든 카탈로그 보기에 머천다이징 규칙을 적용하거나 특정 보기에 맞게 조정합니다.
- 제품 권장 사항, 검색 패싯 및 동의어를 구성합니다.
- 성공 지표 및 검색 성능 보고를 통해 상점 성과를 검토하십시오.
- 카탈로그 동기화 및 캡처된 상점 이벤트 모니터링.

Commerce Foundation은 제품 및 가격에 대한 신뢰할 수 있는 소스로 유지되며 장바구니, 체크아웃 및 기타 트랜잭션 작업을 지속적으로 관리합니다.

## 둘러보기

>[!BEGINTABS]

>[!TAB 카탈로그 구성]

상점 앞에서 사용할 수 있는 카탈로그 컨텍스트를 구성합니다.

- **카탈로그 보기** - 카탈로그 원본, 정책 및 가격 장부를 결합하여 상점에서 검색할 수 있는 제품 및 가격을 정의합니다. [카탈로그 보기](./setup/catalog-view.md)를 참조하세요.
- **카탈로그 계층** - 원본 데이터를 변경하지 않고 선택한 제품 특성을 무시합니다. 제품 이미지에 AEM Assets을 사용하는 경우 제품 비주얼을 통해 AEM-Assets 레이어가 적용됩니다. [카탈로그 계층](./setup/catalog-layer.md)을 참조하세요.
- **개인 카탈로그 보기** - 카탈로그 보기의 데이터를 검색할 때 유효한 서명된 토큰이 필요하도록 카탈로그 보호를 사용하도록 설정하십시오. [비공개 카탈로그 보기](./setup/private-catalog-view.md)를 참조하세요.

>[!TAB 정책]

정책은 제품 특성에 따라 카탈로그 보기를 통해 사용할 수 있는 제품을 필터링합니다. 예를 들어, 정책은 특정 브랜드 또는 제품 카테고리로 분류를 제한할 수 있습니다.

정책은 사용 가능한 제품 분류를 결정합니다. 개인 카탈로그 보기에 대한 액세스를 제어하는 카탈로그 보호는 대체되지 않습니다.

>[!TAB 머천다이징]

구매자가 제품을 검색하는 방법과 사용 가능한 제품군 내에서 제품이 홍보되는 방법을 구성합니다.

- **기회** - 제품 성과, 쇼핑객 행동 및 검색 트렌드를 검토하여 머천다이징 개선을 위한 영역을 식별합니다.
- **권장 사항**—Commerce 관리에서 권장 사항 단위를 만들고 관리합니다. 권장 사항은 카탈로그 데이터 및 집계된 쇼핑객 행동을 사용하여 &quot;이 제품을 본 고객이 본 경우도 본 경우&quot;와 같은 관련 제품을 제안합니다.
- **머천다이징 규칙** - 제품의 홍보 및 등급 지정 방법을 제어합니다. 규칙은 모든 카탈로그 보기에 적용되거나 특정 보기에 맞게 조정할 수 있습니다. [머천다이징 규칙 만들기](https://experienceleague.adobe.com/ko/docs/commerce/optimizer/merchandising/rules/add#create-a-rule)를 참조하십시오.
- **패싯** - 쇼핑객이 브랜드, 크기, 가격 등의 특성별로 제품 결과를 좁히는 데 사용하는 필터를 구성합니다.
- **동의어** - 동일한 검색어를 연결하여 구매자가 동일한 개념에 대해 다른 단어를 사용하여 제품을 찾을 수 있도록 합니다.
- **설정**—가격 패싯, 언어 및 고급 검색을 포함한 검색 및 머천다이징 옵션을 구성합니다.

정책은 카탈로그 보기를 통해 사용할 수 있는 제품을 결정합니다. 머천다이징 규칙은 해당 분류 내의 제품이 홍보되고 등급이 지정되는 방법을 제어합니다.

검색 결과의 일치 및 등급 지정 방법에 대한 자세한 내용은 [일치 및 등급 지정](./manage-results/search-relevance-matching.md)을 참조하십시오.

>[!TAB 보고서]

보고서를 사용하여 상점 활동을 검토하고 머천다이징 결정을 알립니다.

- **성공 지표** - storefront 활동을 기반으로 매출, 전환, 참여, 획득 및 바운스 비율을 검토합니다.
- **검색 성능**—구매자가 사용하는 검색어와 성능을 검토하여 제품 검색을 개선할 영역을 지정하십시오.

보고는 구현에서 수집한 상점 활동 데이터에 따라 다릅니다.

>[!TAB 시스템 구성]

카탈로그 동기화 및 상점 이벤트 수집을 모니터링하여 데이터 가용성 및 구현 문제를 조사합니다.

- **카탈로그 동기화** - Commerce Foundation에서 전송된 카탈로그 데이터의 동기화 상태를 검토합니다.
- **이벤트** - 제품 검색, 권장 사항 및 보고에 사용되는 캡처된 상점 이벤트를 검토합니다. 이벤트 페이지를 사용하여 동작 데이터 수집을 확인하고 누락되거나 예기치 않은 이벤트를 조사할 수 있습니다.

>[!ENDTABS]
<!--
Watch the following video for a high-level overview of [!DNL Adobe Commerce Optimizer]:

>[!VIDEO](https://video.tv.adobe.com/v/3450470?captions=kor)
-->

## 인스턴스가 CCDM을 사용하는지 확인

1. 통합 쉘을 통해 Commerce 관리자에 로그인한 다음 원하는 Adobe Commerce as a Cloud Service 인스턴스를 선택합니다.
1. 인스턴스 탐색에서 카탈로그 보기 및 정책과 같은 CCDM 머천다이징 페이지를 사용할 수 있는지 확인합니다.
1. 해당 페이지를 사용할 수 없는 경우 올바른 인스턴스를 선택했으며 통합 셸을 사용 중인지 확인하십시오.

   Adobe 지원 또는 Commerce 프로비저닝 팀에 문의하여 인스턴스의 CCDM 프로비저닝 상태를 확인합니다.

인스턴스의 준비 상태는 인스턴스의 프로비저닝되었음을 확인하지만, 인스턴스의 자체는 CCDM을 사용하는지 확인하지 않습니다.

