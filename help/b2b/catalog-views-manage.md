---
title: 카탈로그 보기 구성 관리
description: B2B 공유 카탈로그에 대해 만들어진 Adobe Commerce Optimizer 카탈로그 보기를 검토하고 이를 보호하는 제한된 액세스 키를 할당하는 방법을 알아봅니다.
feature: B2B, Companies, Catalog Management
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
    internal-label: Commerce
feature_v2:
  - id: c18ed297-2187-4aec-affb-9d9654eca6fc
    internal-label: Catalog management
  - id: dac87252-6066-4d6e-a9d2-f6d84c323de7
    internal-label: Configuration
subfeature_v2:
  - id: f56d26ed-050b-4fb7-b29b-8e6e994e80a2
    internal-label: B2B
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
    internal-label: Admin
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
    internal-label: Intermediate
topic_v2:
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
    internal-label: Administration
last-update: 2026-10-01
source-git-commit: 82862dcdd7667b46cfe7bd08863926ae5bafd24b
workflow-type: tm+mt
source-wordcount: '363'
ht-degree: 0%
---
# 카탈로그 보기 구성 관리

[!DNL Adobe Commerce Optimizer Connector for B2B] 확장이 설치된 상태에서 [카탈로그 보기] 페이지에는 사용자 지정 공유 카탈로그에 대해 만든 [!DNL Adobe Commerce Optimizer] [카탈로그 보기 예측](https://experienceleague-review.adobe.com/en/docs/commerce/aco-optimizer-connector/b2b-shared-catalog-projection){target="_blank"}이 나열됩니다.  _projection_&#x200B;은(는) 커넥터가 공유 카탈로그 데이터를 [!DNL Adobe Commerce Optimizer]에 동기화할 때 만들어진 카탈로그 보기입니다. 커넥터는 공유 카탈로그의 각 스토어 뷰에 대해 별도의 프로젝션을 생성하므로 공유 카탈로그에는 여러 카탈로그 뷰가 있을 수 있습니다. 상점 경험에서 이러한 카탈로그 보기는 연결된 공유 카탈로그에 할당된 회사에만 액세스할 수 있습니다.

예를 들어 Acme Industrial이 EU 웹 사이트에 속한 하나의 공유 카탈로그 EU Business에 할당된다고 가정해 보겠습니다. 해당 웹 사이트에는 두 개의 스토어 보기가 있습니다.

- `English (UK)`

- `German (Germany)`

커넥터가 공유 카탈로그를 두 개의 [!DNL Adobe Commerce Optimizer] 카탈로그 보기로 프로젝션합니다.

- `EU Business – English (UK)`

- `EU Business – German (Germany)`

회사는 영어와 독일어 카탈로그 뷰를 보유하고 있지만 공유된 카탈로그 할당은 하나만 있습니다. 각 저장소 보기는 해당 카탈로그 보기의 데이터를 표시합니다.

두 카탈로그 보기는 동일한 웹 사이트와 고객 그룹 가격 범위를 사용할 때 동일한 가격 장부를 공유할 수 있습니다.

## 카탈로그 보기 인증

커넥터는 제한된 액세스 키로 카탈로그 보기를 보호합니다. Adobe Commerce은 개인 키를 사용하여 승인된 구매자를 위한 액세스 토큰에 서명합니다. 보호된 카탈로그 데이터를 반환하기 전에 [!DNL Adobe Commerce Optimizer]은(는) 요청된 카탈로그 보기와 연결된 해당 공개 키에 대해 토큰을 확인합니다.

토큰 라이프타임을 구성하거나 토큰 발급을 사용하지 않으려면 [서비스 > ACO 카탈로그 보기](/help/configuration-reference/services/aco-catalog-view.md)를 참조하세요.

공유 카탈로그의 _[!UICONTROL Catalog Views]_&#x200B;탭 또는 연결된 회사의&#x200B;_[!UICONTROL Catalog Views]_ 섹션에서 이러한 카탈로그 보기를 검토하고 할당된 키를 관리할 수 있습니다. 둘 다 동일한 카탈로그 보기와 현재 키 할당을 나열합니다. 각 위치에서 정확한 탐색 경로를 보려면 [제한된 액세스 키 편집](#edit-restricted-access-keys)을 참조하십시오.

[!DNL Adobe Commerce Optimizer]에 대한 공유 카탈로그 데이터 동기화를 모니터링하려면 [카탈로그 보기 동기화 상태 모니터링](/help/systems/catalog-view-sync-status.md)을 참조하세요.

## 카탈로그 보기 참조

{{$include /help/_includes/catalog-views-reference-table.md}}

## 제한된 액세스 키 편집

{{$include /help/_includes/edit-restricted-access-keys.md}}

자세한 내용은 [제한된 액세스 키 관리](/help/systems/restricted-access-keys.md)를 참조하십시오.

>[!MORELIKETHIS]
>
> - [B2B 공유 카탈로그 프로젝션](https://experienceleague-review.adobe.com/en/docs/commerce/aco-optimizer-connector/b2b-shared-catalog-projection){target="_blank"}
> - [서비스 > ACO 카탈로그 보기](/help/configuration-reference/services/aco-catalog-view.md)
> - [카탈로그 보기 동기화 상태 모니터링](/help/systems/catalog-view-sync-status.md)
> - [공유 카탈로그 관리](catalog-shared-manage.md)
> - [회사 계정 관리](account-company-manage.md)
