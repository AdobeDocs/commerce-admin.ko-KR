---
title: 카탈로그 관리 안내서
description: Adobe Commerce 및 Magento Open Source 관리자와 전자 상거래 판매업체를 위한 제품 카탈로그 기능에 대한 포괄적인 정보입니다.
seo-title: Adobe Commerce Catalog Management Guide
seo-description: Describes how to use the product catalog features for Adobe Commerce and Magento Open Source.
exl-id: 894b7cc3-8dc5-43aa-ab9c-ebc6480c7b2f
TQID: https://experienceleague.adobe.com/HJiD3cpDixdbHlBXmMhkHpEd40eyjEfNBu3MzEDhBL0
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
    internal-label: Commerce
feature_v2:
  - id: c18ed297-2187-4aec-affb-9d9654eca6fc
    internal-label: Catalog management
  - id: dac87252-6066-4d6e-a9d2-f6d84c323de7
    internal-label: Configuration
subfeature_v2:
  - id: e91a50b1-0b31-436e-9033-00e4776e94cb
    internal-label: Categories
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
    internal-label: Admin
  - id: f8a45b24-4be7-4f1b-909b-60d06b483a20
    internal-label: Leader
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
    internal-label: Intermediate
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
    internal-label: Beginner
topic_v2:
  - id: cdd65e7e-8839-44a2-bc21-0e03623b5dd1
    internal-label: Optimization
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
    internal-label: Administration
source-git-commit: c425649d00a0a57f84ce4042d33f6d0c5eabe99c
workflow-type: tm+mt
source-wordcount: '498'
ht-degree: 3%
---
# Adobe Commerce 카탈로그 관리 안내서

이 안내서는 Adobe Commerce 및 Magento Open Source 관리자에서 일하는 제품 머천다이저 및 인벤토리 관리자를 대상으로 합니다. 카탈로그의 탐색 구조 구축을 포함하여 제품 카탈로그 기능에 대한 자세한 정보를 제공합니다. 이는 핵심 [!DNL Commerce] 구성 및 기능에 대한 기본적인 이해를 전제로 합니다.

이 안내서에서는 다음 주제를 다룹니다.

| 제목 | 설명 |
| ------- | ----------- |
| [소개](introduction.md) | 고객이 스토어에서 제품을 찾는 방법을 반영하도록 카탈로그 관리 기능을 사용하는 방법에 대한 개요입니다. |
| [카탈로그 메뉴](catalog-menu.md) | [!UICONTROL Catalog] 메뉴를 사용하여 상점의 카탈로그, 범주 및 제품을 관리하기 위한 여러 기능에 액세스합니다. |
| [카탈로그 및 제품 URL](catalog-urls.md) | 기본 URL 유형과 검색 엔진 최적화를 최대화하기 위해 URL을 디자인하는 방법을 검토하십시오. |
| [카탈로그 탐색](navigation.md) | 탐색 도구를 사용하여 쇼핑객이 상점 전체에서 페이지에서 페이지로 이동하는 방식을 정의합니다. |
| [카탈로그 검색](search.md) | 고객이 상점 첫 화면에서 제품을 찾는 데 사용할 수 있는 도구를 검토하고 제품 카탈로그에 따라 검색 환경을 구성합니다. |
| [범주](categories.md) | 상점에서의 쇼핑객 경험을 최적화하는 방식으로 카탈로그의 기본 카테고리 구조를 구축합니다. |
| [제품](products-list.md) | 여러 옵션, 견본, 사용자 정의 가능한 번들을 사용하여 간단한 것부터 복잡한 것까지 제품을 만들 수 있습니다. 다운로드 가능한 제품 및 서비스 및 기타 유형의 항목이 아닌 가상 제품을 만들 수 있습니다. |
| [공유된 카탈로그](../b2b/enable-basic-features.md) | 공유 카탈로그를 통해 판매자는 다양한 회사에 조정된 제품 구성 및 사용자 지정 가격을 제공할 수 있습니다. 회사 계정 및 공유 카탈로그 기능을 포함하여 Adobe Commerce B2B 라이선싱 및 구성이 필요합니다. |
| [카탈로그 보강](catalog-enrichment.md) | 카탈로그가 LLM 및 AI 지원 검색에서 정확하게 표현되도록 AI가 제안한 개선 사항을 검토하고 제품 이름 및 설명에 적용합니다. |
| [제품 특성](product-attributes.md) | 제품 옵션에 대한 입력 컨트롤을 사용하여 속성을 만들고 제품 페이지에 추가 정보를 제공합니다. |
| [카탈로그 보기](../optimizer/setup/catalog-view.md) [!BADGE SaaS만 해당]{type=Positive url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="Adobe Commerce as a Cloud Service 및 Adobe Commerce Optimizer 프로젝트에만 적용됩니다(Adobe 관리 SaaS 인프라)."} | CCDM(Composable Catalog Data Model)이 포함된 머천다이징 서비스를 사용하는 Commerce 배포의 경우 각 브랜드, 지역, 비즈니스 단위 또는 채널에 대한 카탈로그 소스, 카탈로그 레이어, 정책 및 가격 책자를 결합하여 클라이언트가 검색할 수 있는 제품 및 가격을 정의합니다. 선택적으로 카탈로그 보기를 비공개로 만들도록 제한합니다. |
| [정책](../optimizer/setup/policies.md) [!BADGE SaaS만 해당]{type=Positive url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="Adobe Commerce as a Cloud Service 및 Adobe Commerce Optimizer 프로젝트에만 적용됩니다(Adobe 관리 SaaS 인프라)."} | CCDM을 사용하는 Commerce 배포의 경우 각 카탈로그 보기가 제공하는 제품을 제어하는 데이터 액세스 필터를 정의하면 올바른 콘텐츠가 올바른 대상으로 전송됩니다. |

{style="table-layout:auto"}

>[!TIP]
>
>Adobe Commerce B2B는 다양한 회사에 대한 사용자 지정 가격으로 제어된 공유 카탈로그를 유지 관리할 수 있는 기능을 제공합니다. 표준, 기본, 제품 카탈로그 외에도 가격 구조가 다른 두 가지 유형의 공유 카탈로그에 대한 고객 액세스를 제공합니다. 공유 카탈로그 기능에 대한 자세한 내용은 [Adobe Commerce B2B 사용 안내서](../b2b/catalog-shared.md)를 참조하십시오.

## 사용 가능한 설명서

{{docs-links}}
