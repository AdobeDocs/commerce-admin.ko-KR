---
title: 카탈로그 강화
description: '[!DNL Adobe Commerce] 카탈로그 데이터 보강 기능을 사용하여 AI가 제안하는 제품 복사본을 검토하고 데이터 보강 작업을 만들고 LLM 및 AI 검색에 대해 승인된 업데이트를 배포합니다.'
role: Admin, User, Leader
recommendations: noCatalog
touch: true
badgePaas or on-premises: label="Cloud or on-premises only" type="Informative" url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="Applies to Adobe Commerce on Cloud projects (Adobe-managed Cloud or on-premises infrastructure) and on-premises projects only."
autotag-review: '2026-06-23T17:36:07.142Z'
TQID: 'https://experienceleague.adobe.com/cjHuva7PP7UzP-yVhe0rkDzHgAYjfSdYEx3g5gorxwk'
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
    internal-label: Commerce
feature_v2:
  - id: bd989d82-1e15-4534-88db-f1f51dd77ffa
    internal-label: Accounts
  - id: c32adafa-ed01-4b31-997e-2413013911b0
    internal-label: Integrations
  - id: d1e21356-0064-4f48-9089-16e3f0dbd2a6
    internal-label: Storefront
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
    internal-label: Admin
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
  - id: f8a45b24-4be7-4f1b-909b-60d06b483a20
    internal-label: Leader
level_v2:
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
    internal-label: Beginner
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
    internal-label: Intermediate
topic_v2:
  - id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
    internal-label: Implementation
  - id: cdd65e7e-8839-44a2-bc21-0e03623b5dd1
    internal-label: Optimization
  - id: e0eb8757-182f-49f3-94a4-1587d16f5094
    internal-label: Personalization
  - id: e1e0219c-f879-479f-8427-888ed2a6e9c2
    internal-label: Insights
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
    internal-label: Administration
source-git-commit: b2a1abb72839717a7249e9a34b13266b8e384189
workflow-type: tm+mt
source-wordcount: '1976'
ht-degree: 0%
---
# 카탈로그 강화

카탈로그 보강은 기본 [!DNL Adobe Commerce] 기능으로, 쇼핑객이 제품 조사 및 검색을 위해 LLM 및 AI 도우미를 사용할 때 카탈로그가 더 정확하게 표시되도록 제품 이름과 긴 설명을 개선하는 데 도움이 됩니다.

## 작동 방식 {#how-it-works}

[!DNL Adobe Commerce] 제품 카탈로그는 이름, 설명, 특성, 가격 및 인벤토리와 같은 제품 데이터의 기록 시스템입니다. [!DNL Adobe Commerce]이(가) 라이브 카탈로그 데이터를 Adobe AI 경험에 연결합니다. 여기에서 카탈로그 에이전트는 제품 이름과 긴 설명의 차이를 식별하고, 개선 사항을 제안하고, 승인된 변경 사항을 Commerce에 다시 작성하여 Commerce 관리자에서 검토할 수 있습니다.

카탈로그 강화를 통해 다음과 같은 작업을 수행할 수 있습니다.

- LLM이 제품을 해석하는 방식에 영향을 주는 제품 이름과 긴 설명의 간격 및 불일치를 식별합니다.
- 타당성, 전후 비교 등 제안된 개선 사항을 지원 컨텍스트로 검토합니다.
- 승인된 업데이트를 Commerce 카탈로그에 직접 적용하여 관리자, 상점 및 해당 필드를 읽는 기타 채널이 맞게 정렬되도록 합니다.

제품 이름과 긴 설명은 Commerce에 있으므로 한 번 사본을 개선하면 해당 제품 데이터를 사용하는 모든 채널에 도움이 될 수 있습니다. 이 이점은 시스템을 새로 고치는 방법과 시기에 따라 다릅니다.

| 방향 | 목적 |
| --- | --- |
| Commerce 카탈로그 -> 분석 | 카탈로그 및 에이전트 트래픽 신호가 데이터 보강 제안을 찾아냅니다. |
| 데이터 보강 -> Commerce 카탈로그 | 업데이트를 승인하면 제품 이름 및 설명에 대한 변경 사항이 Commerce 카탈로그에 저장되므로 관리자 및 상점 첫 화면의 최적화된 값이 반영됩니다. |

### 카탈로그 강화 액세스

시작하기 전에 배포별 [AI 제품 검색 사전 요구 사항](prerequisites.md)을 검토하십시오. Commerce 플랫폼에 대한 설정을 완료한 후 관리자의 **[!UICONTROL AI Product Discovery]** > **[!UICONTROL Catalog Enrichment]**(으)로 이동합니다.

![카탈로그 보강 대시보드](assets/catalog-enrich-dashboard.png){zoomable="yes"}

카탈로그 데이터 보강 작업 공간에는 **[!UICONTROL Optimizations]**, **[!UICONTROL Brand governance]** 및 **[!UICONTROL Settings]** 탭이 있습니다.

- 에이전트 트래픽 기반 검색 신호를 검토하고 데이터 보강 작업을 관리하려면 **[!UICONTROL Optimizations]** 탭을 사용합니다.
- **[!UICONTROL Brand Governance]** 탭을 사용하여 [!DNL Commerce Catalog Agent]에서 생성한 제품 이름 및 설명에 대한 [요구 사항을 정의](brand-governance.md)할 수 있습니다.
- **[!UICONTROL Settings]** 탭을 사용하여 AI 제품 검색에 [Commerce 인스턴스를 연결](settings.md)합니다.

공유 확장을 사용하면 PDP 데이터 보강 기능도 사용할 수 있습니다. PDP 데이터 보강 기능에는 구조화된 제품 팩트를 AI 에이전트에 노출하는 별도의 워크플로우가 있습니다. [제품 세부 정보 페이지 보강](pdp-enrichment.md)을 참조하세요.

## 카탈로그 보강의 두 가지 경로

카탈로그 보강물을 받는 경로에는 두 가지가 있습니다.

- **에이전트 트래픽** - 이 데이터 보강 유형은 Commerce 인스턴스를 구성한 후 24-48시간 후에 자동으로 시작되며 **최적화** 탭에 결과를 표시합니다.
- **데이터 보강 관리자** - 가맹점은 **[!UICONTROL Create enrichment]** 단추를 클릭하고 데이터 보강 대상 SKU를 수동으로 선택할 때 이러한 데이터 보강 기능을 구성합니다. [데이터 보강 관리자](#create-an-enrichment-job)에 대해 자세히 알아보세요.

### 카탈로그 보강 검토 및 적용 {#review-and-apply}

카탈로그 데이터 보강이 사용 및 구성된 후 **[!UICONTROL Optimizations]** 탭을 사용하여 검색 및 에이전트 트래픽 인사이트를 검토하고 데이터 보강 작업을 관리합니다.

### 월별 에이전트 트래픽 검토

각 월별 에이전트 트래픽 감사는 트래픽이 많은 SKU를 식별하고 권장 일괄 처리를 사용할 수 있도록 합니다. 검토를 위한 최적화는 에이전트 트래픽이 많은 SKU에 대해 자동으로 생성됩니다. 이러한 최적화는 &#39;기본&#39; 거버넌스 규칙을 기반으로 자동 생성됩니다. 월별 카드에는 제품 수, AI 에이전트 방문 및 작업 상태가 표시됩니다. 에이전트 트래픽과 자체 선택된 배치는 동일한 규칙 선택, 확인, 실행, 검토 및 배포 워크플로우를 사용합니다.

### 주의가 필요한 작업 검토

**[!UICONTROL Needs your attention]** 섹션에는 검토를 위해 준비된 완료된 작업을 포함하여 작업이 필요한 작업이 강조 표시됩니다. 배포하기 전에 제안된 제품 변경 사항을 검토하려면 완료된 작업을 여십시오.

### 작업 찾기

**[!UICONTROL All jobs]** 표에는 각 작업 ID, 이름, 원본, SKU 수, 사용된 규칙, 시작 시간 및 상태가 나열됩니다. 출처는 일괄 처리가 에이전트 트래픽에서 자체 선택되었는지 또는 권장되었는지를 식별합니다. **[!UICONTROL Queued]**, **[!UICONTROL Running]**, **[!UICONTROL Completed]** 또는 **[!UICONTROL Failed]**(으)로 처리 상태를 추적합니다. 최적화 작업 영역에서는 이러한 작업이 실행되는 동안 **[!UICONTROL Generating]**, 생성이 완료된 경우 **[!UICONTROL Ready to review]**, 승인된 변경 내용이 배포된 후 **[!UICONTROL Deployed]**(으)로 나타날 수도 있습니다. 여러 작업을 동시에 실행할 수 있습니다. **[!UICONTROL Retry]**(으)로 실패한 작업을 다시 시도하십시오.

### 데이터 보강 작업 만들기

**카탈로그 데이터 보강 만들기:**

![카탈로그 보강 만들기](./assets/create-cat-enrich.png){zoomable="yes"}

1. **[!UICONTROL Optimizations]**&#x200B;에서 **[!UICONTROL Create enrichment]**&#x200B;을(를) 클릭합니다.
1. **데이터 보강 이름**&#x200B;을 입력하십시오(예: &quot;2026년 블랙 프라이데이&quot;).
1. **범주**&#x200B;을 선택합니다(예: &quot;커피&quot;).
1. &quot;보조프로그램&quot;과 같은 **특성 집합**&#x200B;을(를) 선택하십시오.
1. &quot;단순 제품&quot;과 같은 **제품 유형**&#x200B;을(를) 선택하십시오.
1. **가격 범위**&#x200B;를 선택하십시오.
1. **[!UICONTROL Apply filters]**&#x200B;을(를) 클릭합니다.

   데이터 보강 기준과 일치하는 제품을 미리 보고 **사용자 지정**&#x200B;을 클릭하여 데이터 보강 기준에 맞는 제품의 범위를 추가로 지정할 수 있습니다.

1. **[!DNL Next]**&#x200B;을(를) 클릭하고 데이터 보강에 적용되는 [거버넌스 규칙](brand-governance.md)을(를) 미리 봅니다.
1. 보강할 특정 제품을 확인하려면 **[!DNL Next]**&#x200B;을(를) 클릭하십시오.
1. **[!DNL Run enrichment]**&#x200B;을(를) 클릭합니다.

   데이터 보강 작업이 실행되고 최적화 테이블에 표시됩니다. 실행이 완료되면 최적화를 [검토 및 배포](#review-deploy-catalog)할 수 있습니다.

### 데이터 보강 작업 검토 및 배포 {#review-deploy-catalog}

데이터 보강 작업을 엽니다.

![카탈로그 데이터 보강 URL 목록](./assets/catalog-enrich-urls.png){zoomable="yes"}

**제안이 있는 URL** 표에는 데이터 보강 기회가 있는 모든 제품이 나열되어 있습니다. 각 제품에 대해 다음을 수행할 수 있습니다.

- AI 분석 및 제안된 데이터 보강 기능을 보려면 **행을 확장**&#x200B;하십시오.
- 브랜드 음성 및 머천다이징 지침에 맞추기 위해 적용하기 전에 제안된 제품 이름 또는 설명을 **편집**&#x200B;하십시오.
- 보강할 제품에 대해 **최적화를 배포**&#x200B;하고 Adobe Commerce 카탈로그에 직접 게시합니다.
- 데이터 보강이 검토 및 적용되면 **고정으로 표시**.
- 카탈로그 전략과 관련이 없는 제안을 **무시**&#x200B;합니다.

제안은 다음 세 가지 보기로 구성됩니다. **현재 제안**, **수정 제안** 및 **무시된 제안**. 데이터 보강이 적용되면 상태가 **적용됨**&#x200B;이고 동작이 **카탈로그에서 보기**&#x200B;인 수정 제안으로 이동하여 Adobe Commerce에서 업데이트를 확인합니다. 적용된 보강은 언제든지 롤백하여 원래 제품 이름과 설명을 복원할 수 있습니다.

## 관리자에서 데이터 보강 확인 {#verify-in-admin}

**적용된 카탈로그 데이터 보강 확인:**

1. Commerce 관리자의 **[!UICONTROL Catalog]** > **[!UICONTROL Products]**(으)로 이동합니다.
1. 필요에 따라 필터 및 **[!UICONTROL Store View]** 선택기를 사용합니다(예: **[!UICONTROL Default Store View]**).
1. SKU를 검색합니다.
1. 제품을 편집 모드로 엽니다.

   제품 양식에는 보강된 제품 이름 및/또는 설명이 표시됩니다.

   ![보강된 제품 이름](./assets/enriched-product-name.png){zoomable="yes"}

1. 선택 사항: 대신 수동으로 입력한 이름을 유지하려면 **[!UICONTROL Override Catalog Agent provided Product Name]**&#x200B;을(를) 선택하십시오.

   수동 재정의는 제안이 카탈로그와 계속 동기화되는 방식에 영향을 줍니다. 자세한 내용은 [관리자의 수동 재정의](#manual-override-in-the-admin)를 참조하십시오.

1. **[!UICONTROL Content]** 섹션을 확장하고 설명 필드를 찾습니다.

   설명 변경을 적용하면 보강된 설명이 나타납니다.

   ![제품 설명 보강](./assets/enrich-product-description.png){zoomable="yes"}

1. 선택 사항: 수동으로 입력한 설명을 대신 유지하려면 **[!UICONTROL Override Catalog Agent provided Description]**&#x200B;을(를) 선택합니다.

수동 재정의는 제안이 카탈로그와 계속 동기화되는 방식에 영향을 줍니다. 자세한 내용은 [관리자의 수동 재정의](#manual-override-in-the-admin)를 참조하십시오.

## 상점 첫 화면에서 데이터 보강 확인 {#verify-storefront}

**Storefront에서 데이터 보강 확인:**

1. 상점에서 SKU를 검색합니다.
1. 제품 페이지를 엽니다.
1. 제품 이름 및 설명이 승인한 내용과 일치하는지 확인합니다.

   상점에 풍요로움이 나타나려면 시간이 좀 걸릴 수 있습니다.

1. 긴 설명을 표시하는 지역이 승인한 지역과 일치하는지 확인합니다.
1. 선택 사항: 롤아웃과 관련이 있는 경우 동일한 카탈로그 속성을 사용하는 다운스트림 채널을 확인합니다.

## 재정의, 수집 및 오래된 제안 {#overrides-ingestion}

카탈로그 보강으로 제품의 이름이나 설명이 업데이트되면 다른 수집 시스템에서 동일한 필드를 변경할 수 있습니다. 예로는 REST API 호출, CSV 가져오기 및 PIM 피드가 있습니다.

### 원래 값 다시 수집됨 {#original-value-reingested}

외부 프로세스가 원래 이름 또는 설명(보강이 적용되기 전의 값)을 작성하는 경우 Commerce은 카탈로그 보강 규칙에 따라 해당 필드에 대해 보강된 값을 계속 적용합니다. 해당 수집만으로는 제안을 자동으로 되돌릴 수 없습니다.

### 새 값 다시 수집됨 {#new-value-reingested}

외부 프로세스가 데이터 보강 전 텍스트 반복이 아닌 새 값을 전송하는 경우 Commerce은 새 카탈로그 값을 적용합니다. 예를 들어 &quot;Red Shoes&quot;에서 &quot;Iconic Red Shoes&quot;로 이름을 바꾸면 보강된 값이 바뀝니다. 라이브 카탈로그가 제안 컨텍스트와 더 이상 일치하지 않으므로 관련 데이터 보강 제안은 일반적으로 *오래됨*(으)로 표시됩니다.

### 관리자의 수동 재정의 {#manual-override-in-the-admin}

[!DNL Adobe Commerce] 관리자의 제품 이름 또는 설명을 수동으로 편집하는 경우:

- 관리자 값은 해당 수동 변경에 대한 레코드 시스템으로 성공합니다.
- 데이터 보강 제안이 *오래됨*(으)로 표시되어 있습니다.
- 제안 워크플로우는 해당 항목의 원래 상태로 되돌아가므로 분석을 다시 실행할 경우 기준을 다시 지정하거나 새 제안을 수락할 수 있습니다.

이러한 규칙은 여러 채널이 동일한 SKU를 터치할 때 카탈로그 보강, 수집 피드 또는 관리자 편집 중 어느 것이 신뢰할 수 있는지 아는 데 도움이 됩니다.

## 제한 및 고려 사항 {#limits}

- 데이터 보강은 제품 이름과 긴 설명에만 적용됩니다. 제품 세부 사항 페이지 레이아웃, 위젯 또는 기타 페이지 수준 상점 콘텐츠는 변경되지 않습니다.
- 큰 카탈로그와 높은 URL 수는 분석이 완료되는 속도와 한 번에 표시되는 제안 수에 영향을 줄 수 있습니다.
- 의미 있는 제안은 LLM 관련 보트가 관심 있는 제품 URL에 액세스할 수 있다고 가정합니다. 로봇 규칙, 인증, 지리 차단 및 과도한 개인화를 통해 적용 범위를 줄일 수 있습니다.

## 우수 사례 {#best-practices}

- PIM 또는 피드 작업이 실수로 카탈로그 보강과 충돌하지 않도록 제품 이름 및 설명에 대한 시스템 소유권을 문서화합니다.
- 제목 또는 설명을 일괄 적용하기 전에 SEO 및 브랜드 팀과 조정합니다.
- 주요 카탈로그 가져오기 후 제안을 현재 카탈로그 상태에 반영하도록 다시 동기화하거나 다시 분석합니다.

## 예

다음 예는 카탈로그 보강으로 원시 기술 특성이 쇼핑객 중심의 서사적 제품 사본으로 바뀌는 방식을 보여 줍니다. LLM은 이를 사용하여 쇼핑 질문에 답변할 수 있습니다.

### 예: 기술적 속성이 있는 커피 제품

커피 retailer의 카탈로그에는 중간 크기의 로스트 커피 원두 제품에 대한 기술 사양이 저장되는데, 원두 종류, 원산지 지역, 가공 방법, 로스트 레벨 및 고도 범위가 있습니다. 이들 분야는 제품에 대해 설명하지만 그 가치를 쇼핑객에게 전달하지 않기 때문에 AI 비서는 &quot;어떤 커피가 부드럽고 저산성 향이 나는가?&quot;와 같은 질문에 답할 때 함께 할 일이 거의 없다.

카탈로그 보강은 쇼핑객 관련 특성을 추론하기 위해 상호 작용하는 방법을 통해 기술적 특성과 이유를 읽습니다.

| 기술 속성 | 특성 유추 | 추론 |
| --- | --- | --- |
| 허니 프로세스, Medium 로스트 | 낮은 산도 | 꿀을 가공하는 과정에서 콩에 남겨진 과일 점액질이 산성을 억제하고, 미디엄 로스트는 잔류 산성 화합물을 분해한다. |
| 꿀 가공, 아라비카, Medium 로스트 | 헤이즐넛 맛 | 점액에서 나오는 과일당은 중간 굽기에서 증폭되는 아라비카의 천연 견과류와 결합합니다. |
| 아라비카 벌꿀법 | 풍부하고 부드러운 입 냄새 | 건조 시 점액에서 흡수된 기름은 점성과 신체를 더해준다. |
| 꿀 공정, 고도 900-1200m | 캐러멜 함축 | 고랭지 콩의 밀도가 높을수록 더 복잡한 당분이 생기며, 꿀 가공으로 더 깊어집니다. |

카탈로그 보강은 제품 사본에 다음과 같이 추론된 특성을 적용합니다.

- **이전**: &quot;Medium 커피 원두 로스팅 - 아라비카, 브라질 미나스 제라이스, 허니 프로세스, 900-1200m&quot;
- **후**: &quot;브라질의 미나스 제라이스에서 900-1200m에서 재배된 아라비카 콩, 꿀 가공 및 중간 배소, 독특한 헤이즐넛 특성, 캐러멜 색조 및 낮은 산도를 가진 자연적으로 달콤하고 크리미 있는 입 맛을 냅니다. 일관되고 접근 가능한 스페셜티 커피는 쏟아지는 것을 통해 가장 잘 경험합니다.&quot;

업데이트된 이름과 설명은 Commerce 카탈로그에 직접 저장되므로 상점, LLM 피드 및 이러한 필드를 읽는 기타 채널은 모두 동일한 보강된 사본을 반영합니다.

### 예: 모듈식 가구 구성

가구 retailer은 모듈형 단면 소파를 판매하며 제품 설명에 구성 코드와 패브릭 이름(예: `6 Standard Seats + 6 Standard Sides in Sapphire Navy Corded Velvet`)만 나열되어 있습니다. 이 속기는 재방문 고객이 이해할 수 있지만 AI 어시스턴트에게 제품의 작동 방식 또는 내구성이 뛰어나고 편안한 면에 대한 컨텍스트를 거의 주지 않습니다.

카탈로그 강화를 통해 구성 및 패브릭 속성을 각 구성 요소의 기능과 쇼핑객에게 중요한 이유에 대해 설명하는 설명 형식으로 확장합니다.

- **이전**: &quot;표준 좌석 6개 + 사파이어 네이비 코드 벨벳 표준 좌석 6개&quot;
- **After**: &quot;이 구성에는 6개의 표준 시트 삽입 세트와 6개의 표준 사이드 인서트가 포함되어 있습니다. 이 인서트는 팔이나 등과 같은 기능을 하며 레이아웃의 모듈식 구성 요소를 형성합니다. 각 시트에는 상승도와 처짐을 방지하기 위해 설계된 3개의 고밀도 레이어가 있는 표준 폼이 있습니다. 사파이어 네이비 코디드 벨벳 커버는 고급스러운 만큼 내구성이 강하며 은은한 광택과 부드럽고 플러시 느낌을 주는 질감의 코드가 특징이다. 커버는 정밀하고 맞춤화된 룩을 위해 손으로 꿰매어져 있으며 기계 세척이 가능하고 변경 가능하기 때문에 귀하의 공간에 따라 단면화가 가능합니다.&quot;

보강된 설명이 카탈로그에 다시 기록되므로 AI는 쇼핑객이 페이지에서 볼 수 있는 레이아웃이나 디자인을 변경하지 않고도 제품의 카탈로그 데이터를 소비하는 다운스트림 채널 또는 피드뿐만 아니라 Commerce의 제품 세부 사항 페이지에서도 사용할 수 있습니다.
