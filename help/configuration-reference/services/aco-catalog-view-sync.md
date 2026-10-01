---
title: '[!UICONTROL Services] > ACO 카탈로그 보기 동기화'
description: Commerce 관리자의 [!UICONTROL Services] > [!UICONTROL ACO Catalog View Sync] 페이지에서 구성 설정을 검토합니다.
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
source-git-commit: 9ec73be87dd329dc04e7b133885fcc156f4ffcb6
workflow-type: tm+mt
source-wordcount: '304'
ht-degree: 3%
---
# [!UICONTROL Services] > [!UICONTROL ACO Catalog View Sync]

이 설정을 사용하여 [!DNL Adobe Commerce Optimizer Connector for B2B]이(가) 카탈로그 보기, 정책, 가격 장부 및 키와 같은 B2B 공유 카탈로그 구성을 [!DNL Adobe Commerce Optimizer]에 동기화하는 방법과 두 시스템 간의 구성 차이를 해결하는 방법을 제어합니다. 이러한 설정의 결과를 모니터링하려면 [카탈로그 보기 동기화 상태 모니터링](../../systems/catalog-view-sync-status.md)을 참조하세요.

{{config}}

## [!UICONTROL Deletion]

![삭제](./assets/aco-catalog-view-sync-configuration.png)<!-- zoom -->

| 필드 | [범위](../../getting-started/websites-stores-views.md#scope-settings) | 설명 |
| --- | --- | --- |
| [!UICONTROL Deletion Grace Period (days)] | 글로벌 | 공유된 카탈로그 데이터의 보존 기간입니다. 삭제된 공유 카탈로그의 카탈로그 보기, 정책 및 메타데이터가 하드 삭제되기 전에 유지되는 일 수를 지정합니다. 기본값은 7일입니다. 즉시 하드 삭제하려면 `0`(으)로 설정하십시오. |

{style="table-layout:auto"}

## [!UICONTROL Creation]

| 필드 | [범위](../../getting-started/websites-stores-views.md#scope-settings) | 설명 |
| --- | --- | --- |
| [!UICONTROL Creation Grace Period (days)] | 글로벌 | 상태가 [!UICONTROL Pending]&#x200B;(으)로 보고되는 동안 새로 등록된 카탈로그 보기가 [!DNL Adobe Commerce Optimizer Connector for B2B]이(가) 카탈로그 보기, 정책, 가격 장부 및 주요 구성의 첫 번째 동기화를 완료할 때까지 대기할 수 있는 일 수입니다. 동기화가 성공하지 못한 채 유예 기간이 지나면 상태가 [!UICONTROL Failed]&#x200B;(으)로 변경됩니다. 기본값: `1` |

{style="table-layout:auto"}

## [!UICONTROL Drift Reconciler]

| 필드 | [범위](../../getting-started/websites-stores-views.md#scope-settings) | 설명 |
| --- | --- | --- |
| [!UICONTROL Enabled] | 글로벌 | 예약된 드리프트 조정자를 실행하여 [!DNL Adobe Commerce]에서 예상한 카탈로그 보기와 [!DNL Adobe Commerce Optimizer]의 카탈로그 보기 구성 간의 차이점을 감지하고 보고합니다. `automatically repair drift`을(를) 사용하면 복구할 수 있는 불일치도 수정됩니다. |
| [!UICONTROL Automatically Repair Drift] | 글로벌 | `Yes`(으)로 설정되면 예약된 드리프트 조정자는 [!DNL Adobe Commerce Optimizer] 구성을 [!DNL Adobe Commerce]과(와) 일치하도록 업데이트하고 구성을 다시 동기화합니다. `No`(으)로 설정된 경우 실행은 드리프트만 감지하고 보고합니다. 분리된 [!DNL Adobe Commerce Optimizer] 엔터티는 항상 보고되며 자동으로 제거되지 않습니다. |

{style="table-layout:auto"}

>[!MORELIKETHIS]
>
> - [ACO 카탈로그 보기](./aco-catalog-view.md) - 카탈로그 보기의 상점 읽기에 대한 액세스 토큰을 구성합니다.
> - [카탈로그 보기 동기화 상태 모니터링](../../systems/catalog-view-sync-status.md) - 이러한 설정을 사용하여 동기화 상태를 모니터링하고 드리프트를 조정합니다
> - [제한된 액세스 키 관리](../../systems/restricted-access-keys.md) - 동기화된 카탈로그 보기에 할당된 액세스 키를 관리합니다.
