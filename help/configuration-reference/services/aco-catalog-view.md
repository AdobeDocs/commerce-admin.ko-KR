---
title: '[!UICONTROL Services] > ACO 카탈로그 보기'
description: Commerce 관리자의 [!UICONTROL Services] > [!UICONTROL ACO Catalog View] 페이지에서 Adobe Commerce Optimizer 구성 설정을 검토하고 업데이트합니다.
feature: Configuration, Security
badgePaas: label="PaaS만" type="Informative" url="https://experienceleague.adobe.com/ko/docs/commerce/user-guides/product-solutions" tooltip="Adobe Commerce 온 클라우드 프로젝트(Adobe 관리 PaaS 인프라) 및 온프레미스 프로젝트에만 적용됩니다."
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
    internal-label: Commerce
feature_v2:
  - id: ba9e5be9-7de1-4f71-a5d2-baead0e425ee
    internal-label: Security
  - id: dac87252-6066-4d6e-a9d2-f6d84c323de7
    internal-label: Configuration
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
    internal-label: Admin
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
    internal-label: Developer
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
    internal-label: Intermediate
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
    internal-label: Beginner
topic_v2:
  - id: d095671a-1355-40aa-8b5f-06c33c68080b
    internal-label: Security
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
    internal-label: Administration
source-git-commit: b32c28afffe75b3f684f0fef81bd61e9cdcb485a
workflow-type: tm+mt
source-wordcount: '211'
ht-degree: 3%
---
# [!UICONTROL Services] > [!UICONTROL ACO Catalog View]

[!DNL Adobe Commerce Optimizer Connector for B2B]에서 발급한 액세스 토큰을 제어하려면 이 설정을 사용하십시오. 상점은 이러한 토큰을 사용하여 관리자에 구성된 사용자 지정 공유 카탈로그에서 동기화된 데이터로 채워진 Commerce Optimizer 개인 카탈로그 보기를 인증합니다.

{{config}}

![ACO 카탈로그 보기 액세스 토큰 설정을 보여 주는 Adobe Commerce 관리자로서 3,600초 TTL 및 토큰 발급을 사용할 수 있습니다.](./assets/aco-catalog-view-access-token-config.png)<!-- zoom -->

## [!UICONTROL Access Token Configuration]

| 필드 | [범위](../../getting-started/websites-stores-views.md#scope-settings) | 설명 |
| --- | --- | --- |
| [!UICONTROL Token TTL (seconds)] | 글로벌 | 액세스 토큰이 생성된 후에도 유효한 상태로 유지되는 시간(초). 이 설정은 기본 범위에서 읽기 전용입니다. 웹 사이트 또는 스토어 뷰 범위에 구성된 값은 무시됩니다. 기본값은 3,600초입니다. |
| [!UICONTROL Issue Access Tokens] | 스토어 뷰 | 상점 측에서 카탈로그 보기에 대한 액세스 토큰을 얻을 수 있는지 여부를 제어합니다. `No`(으)로 설정하면 `Company.catalogViewContext`이(가) 카탈로그 보기 ID를 반환하지만 액세스 토큰은 반환하지 않으므로 상점이 Adobe Commerce에서 동기화된 [!DNL Adobe Commerce Optimizer]개의 개인 카탈로그 보기에서 읽기 위해 인증할 수 없습니다. |

{style="table-layout:auto"}

>[!MORELIKETHIS]
>
> - [ACO 카탈로그 보기 동기화](./aco-catalog-view-sync.md) - 카탈로그 보기가 [!DNL Adobe Commerce Optimizer]에 동기화되는 방법을 구성합니다.
> - [카탈로그 보기 동기화 상태 모니터링](../../systems/catalog-view-sync-status.md) - 동기화 상태를 모니터링하고 드리프트를 조정합니다.
