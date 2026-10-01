---
title: '[!UICONTROL Services] > [!UICONTROL ACO Restricted Access Keys]'
description: Commerce 관리자의 [!UICONTROL Services] > [!UICONTROL ACO Restricted Access Keys] 페이지에서 구성 설정을 검토합니다.
feature: Configuration, Security
badgePaas: label="PaaS만" type="Informative" url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="Adobe Commerce 온 클라우드 프로젝트(Adobe 관리 PaaS 인프라) 및 온프레미스 프로젝트에만 적용됩니다."
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
source-git-commit: 9ec73be87dd329dc04e7b133885fcc156f4ffcb6
workflow-type: tm+mt
source-wordcount: '182'
ht-degree: 4%
---
# [!UICONTROL Services] > [!UICONTROL ACO Restricted Access Keys]

이 설정을 사용하여 [!DNL Adobe Commerce Optimizer Connector for B2B]이(가) B2B 공유 카탈로그 보기에 대해 프로비전하는 제한된 액세스 키에 적용되는 기본 만료 기간을 제어합니다. 이 키를 만들고, 할당하고, 삭제하려면 [제한된 액세스 키 관리](../../systems/restricted-access-keys.md)를 참조하세요.

{{config}}

## [!UICONTROL Provisioning]

![프로비저닝](./assets/optimizer-restricted-access-key-config.png)<!-- zoom -->

| 필드 | [범위](../../getting-started/websites-stores-views.md#scope-settings) | 설명 |
| --- | --- | --- |
| [!UICONTROL Default key expiry (days)] | 글로벌 | 새로 제공된 제한된 액세스 키의 유효 기간. [!DNL Adobe Commerce Optimizer]은(는) 모든 키에 대해 향후 1분 이상의 만료 날짜가 필요하며 만료된 키는 게이트웨이 읽기에서 제외되므로 최소 하루 이상의 값이 항상 적용됩니다. 기본값: `36500` |

{style="table-layout:auto"}

>[!NOTE]
>
>자동 키 순환을 아직 사용할 수 없으므로 기본 만료는 긴 만료 기간으로 설정됩니다. [키 선택 및 순환](../../systems/restricted-access-keys.md#key-selection-and-rotation)을 참조하세요.

>[!MORELIKETHIS]
>
> - [ACO 카탈로그 보기](./aco-catalog-view.md) — 카탈로그 보기에 대한 상점 액세스 토큰을 구성합니다.
> - [제한된 액세스 키 관리](../../systems/restricted-access-keys.md) - 제한된 액세스 키를 만들고, 할당하고, 삭제합니다.
> - [카탈로그 보기 동기화 상태 모니터링](../../systems/catalog-view-sync-status.md) — 만료 임박한 키 모니터링
