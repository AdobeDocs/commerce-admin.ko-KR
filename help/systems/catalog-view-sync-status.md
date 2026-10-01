---
title: 카탈로그 보기 동기화 상태 모니터링
description: B2B 공유 카탈로그 프로젝션 상태를 모니터링하고 Adobe Commerce Optimizer 커넥터에 대한 카탈로그 보기, 정책, 가격 장부 및 액세스 키를 조정합니다.
feature: Products, Customers, Data Import/Export
role: Admin
level: Intermediate
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
    internal-label: Commerce
  - id: b974b164-8a4e-43b8-a9e2-8e67ec131677
    internal-label: Commerce on Prem
  - id: cdf0c6dd-1717-4e20-9530-a24eee57088b
    internal-label: Commerce on Cloud
feature_v2:
  - id: ba9e5be9-7de1-4f71-a5d2-baead0e425ee
    internal-label: Security
  - id: dac87252-6066-4d6e-a9d2-f6d84c323de7
    internal-label: Configuration
  - id: f42e0a1a-0d79-488d-a83f-f2c30672b137
    internal-label: Reporting
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
    internal-label: Admin
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
    internal-label: Intermediate
topic_v2:
  - id: aa2f3246-cb95-4b30-8899-fdf7d73550cc
    internal-label: Reporting
  - id: c1579802-ddd4-4214-8a91-97b2066abe11
    internal-label: Troubleshooting
  - id: ebde5b41-29c9-4f5e-9ef6-1197e85409e3
    internal-label: Data management
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
    internal-label: Administration
source-git-commit: 9ec73be87dd329dc04e7b133885fcc156f4ffcb6
workflow-type: tm+mt
source-wordcount: '1332'
ht-degree: 0%
---

# 카탈로그 보기 동기화 상태 모니터링

[카탈로그 뷰 동기화 상태] 페이지에서는 동기화를 모니터링하고 Adobe Commerce Optimizer에 투영된 카탈로그 뷰 문제를 해결할 수 있습니다. [!DNL Adobe Commerce Optimizer Connector for B2B]은(는) 각 사용자 지정 공유 카탈로그에 대해 공유 카탈로그의 웹 사이트 범위 내의 모든 스토어 보기에 대한 카탈로그 보기를 만듭니다. 각 카탈로그 보기는 연결 가격 정책, 제한된 액세스 토큰의 유효성을 검사하는 데 사용되는 공개 키로 구성됩니다. Adobe Commerce은 개인 키 및 기본 Price Book ID를 포함하여 해당 카탈로그 보기 메타데이터를 유지합니다.

>[!NOTE]
>
>카탈로그 데이터 피드의 동기화 상태를 추적하려면 [[!UICONTROL Data Feed Sync Status]](data-feed-sync-status.md) 페이지를 사용하십시오.

## 대상자 및 가용성 {#audience}

[!BADGE PaaS만]{type=Informative url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="Adobe Commerce 온 클라우드 인프라 및 온프레미스 프로젝트에만 적용됩니다."}

[!DNL Adobe Commerce Optimizer Connector for B2B] 통합으로 B2B 공유 카탈로그를 사용하는 Adobe Commerce on Cloud Infrastructure 및 온-프레미스 상인이 [!UICONTROL Catalog View Sync Status] 페이지를 사용할 수 있습니다. Connector 확장이 설치되면 페이지가 자동으로 설치되고 활성화됩니다.

## 카탈로그 동기화 상태 보기 페이지에 액세스 {#access-catalog-view-sync-status-page}

관리 영역에서 **[!UICONTROL System]** > **[!UICONTROL Data Transfer]** > **[!UICONTROL Catalog View Sync Status]**(으)로 이동합니다.

![동기화 상태가 있는 카탈로그 보기를 나열하는 카탈로그 보기 동기화 상태 페이지](assets/catalog-view-sync-status.png){width="600" zoomable="yes"}

이 페이지에는 세 개의 탭이 있습니다.

- **[!UICONTROL Catalog Views]** - 커넥터가 만든 카탈로그 보기로, 각 항목에 대한 동기화 상태가 있습니다. [카탈로그 보기 동기화 상태 요약](#catalog-view-sync-status-summary)을 참조하세요.
- **[!UICONTROL Orphaned in ACO]**—해당 [!DNL Adobe Commerce] 원본이 없는 [!DNL Adobe Commerce Optimizer]에 있는 엔터티. [ACO 탭에서 고립됨](#orphaned-in-aco-tab)을 참조하십시오.
- **[!UICONTROL Deleted]** - 공유된 카탈로그가 삭제되어 카탈로그 보기 예측 레코드가 제거되었습니다. [삭제된 탭](#deleted-tab)을 참조하세요.

## 카탈로그 보기 동기화 상태 요약 {#catalog-view-sync-status-summary}

페이지 상단에 있는 요약 카드는 각 상태 의 카탈로그 보기 수와 30일 이내에 만료되는 제한된 액세스 키 수를 보여줍니다.

| 카드 | 설명 |
| --- | --- |
| **정상** | 감지된 드리프트가 없는 카탈로그 보기. |
| **성능 저하** | 수리 가능한 드리프트가 있는 카탈로그 보기. |
| **실패** | 만들어진 적이 없거나 [!DNL Adobe Commerce Optimizer]에서 직접 삭제된 카탈로그 보기입니다. |
| **키 ≤ 30D** | 30일 이내에 만료되는 제한된 액세스 키. |

그리드는 카탈로그 보기당 하나의 행을 나열합니다.

| 필드 | 설명 |
| --- | --- |
| **카탈로그 보기** | [!DNL Adobe Commerce Optimizer]에 예상된 카탈로그 보기의 식별자입니다. |
| **Source** | 카탈로그 보기가 투영된 공유 카탈로그입니다. 링크를 선택하여 관리자에서 공유 카탈로그를 엽니다. |
| **보기 저장** | 카탈로그 보기가 나타내는 스토어 보기. |
| **회사** | 현재 이 카탈로그 보기에 연결된 회사의 수입니다. |
| **상태** | 카탈로그 보기의 전체 동기화 상태입니다. [동기화 상태 값](#sync-status-values)을 참조하세요. |
| **정책** | 이 카탈로그 보기에 할당된 정렬 정책이 [!DNL Adobe Commerce] 구성과 일치하는지 여부입니다. |
| **가격표** | 이 카탈로그 보기에 할당된 가격 장부가 [!DNL Adobe Commerce] 구성과 일치하는지 여부입니다. |
| **액세스 키** | 제한된 액세스 키가 이 카탈로그 보기에 연결되어 있는지 여부입니다. |
| **키 만료** | 카탈로그 보기의 제한된 액세스 키의 만료 날짜 및 남은 일 수입니다. |
| **드리프트** | 감지된 드리프트 유형(있는 경우). |
| **마지막으로 조정됨** | 조정 프로세스에서 이 카탈로그 보기를 마지막으로 확인한 시기 |
| **작업** | **[!UICONTROL View details]**&#x200B;이(가) 현재 상태, 드리프트, 액세스 키 및 최근 이벤트를 볼 수 있는 [카탈로그 동기화 상태 보기] 세부 정보 페이지를 엽니다. **[!UICONTROL Open in ACO admin]**&#x200B;이(가) [!DNL Adobe Commerce Optimizer] Studio에서 카탈로그 보기 세부 정보 페이지를 엽니다. **[!UICONTROL Copy ID]**&#x200B;이(가) 참조할 카탈로그 보기 ID를 복사합니다. [이동 조정 및 복구](#reconcile-and-repair-drift)를 참조하십시오. |

## 동기화 상태 값 {#sync-status-values}

| 상태 | 의미 |
| --- | --- |
| **정상** | 드리프트가 감지되지 않았습니다. 카탈로그 보기, 정책, 가격표 및 키가 [!DNL Adobe Commerce] 구성과 일치합니다. |
| **성능 저하** | 드리프트가 감지되었으며 복구할 수 있습니다. 예를 들어 정책 또는 가격 책자가 [!DNL Adobe Commerce Optimizer]에서 직접 변경되었습니다. |
| **실패** | 카탈로그 보기가 만들어지지 않았거나 [!DNL Adobe Commerce Optimizer]에서 직접 삭제되었습니다. |
| **보류 중** | 카탈로그 보기가 아직 조정되지 않았거나 첫 번째 프로젝션을 기다리고 있습니다. |
| **중단** | 공유된 카탈로그가 [!DNL Adobe Commerce]에서 삭제되었으며 카탈로그 보기가 삭제 유예 기간 내에 있습니다. |
| **삭제됨** | 카탈로그 뷰 투영이 유예 기간 후에 제거되었습니다. [!UICONTROL Deleted] 탭에 90일 동안 레코드로 유지됩니다. |
| **고립됨** | 카탈로그 보기 또는 키가 [!DNL Adobe Commerce Optimizer]에 있지만 해당 [!DNL Adobe Commerce] 원본이 없습니다. [ACO 탭에서 고립됨](#orphaned-in-aco-tab)을 참조하십시오. |

### 삭제 유예 기간 구성 {#configure-the-deletion-grace-period}

삭제 유예 기간은 연결된 공유 카탈로그가 삭제된 후 카탈로그 보기 및 연결된 데이터에 대한 데이터 보존 기간을 지정합니다. 기본값은 7일입니다.
기간이 만료되면 모든 데이터가 제거됩니다.

#### 데이터 보존 설정 변경

1. [!DNL Adobe Commerce] 관리자를 엽니다.

1. **[!UICONTROL Stores]** 메뉴에서 **[!UICONTROL Configuration]** > **[!UICONTROL Services]** > **[!UICONTROL ACO Catalog View Sync]** > **[!UICONTROL Deletion]** > **[!UICONTROL Deletion Grace Period (days)]**&#x200B;을(를) 선택합니다.

1. 필요에 따라 **[!UICONTROL Deletion Grace Period (days)]** 값을 업데이트합니다.

   공유 카탈로그를 삭제한 후 바로 카탈로그 보기 ACO 프로젝션을 제거하려면 이 값을 `0`(으)로 설정하십시오.

1. **[!UICONTROL Save Config]**&#x200B;을(를) 선택합니다.

사용 가능한 모든 동기화 및 드리프트 조정자 설정에 대한 자세한 내용은 [서비스 > ACO 카탈로그 동기화 보기](../configuration-reference/services/aco-catalog-view-sync.md)를 참조하십시오.

## 구성 차이점 조정 및 복구 {#reconcile-and-repair-drift}

[!DNL Adobe Commerce]은(는) B2B 공유 카탈로그 프로젝션의 신뢰할 수 있는 소스입니다. 조정은 [!DNL Adobe Commerce] 구성을 [!DNL Adobe Commerce Optimizer]과(와) 비교하고 차이점을 보고하거나 복구합니다.

>[!IMPORTANT]
>
>[!DNL Adobe Commerce Optimizer]에서 커넥터 관리 카탈로그 보기, 정책, 가격 장부 또는 키로 직접 변경한 내용은 중요한 원인이 아닙니다. 조정에서는 이러한 구성 차이로 보고하며, 복구할 때 [!DNL Adobe Commerce]과(와) 일치하도록 되돌립니다. [!DNL Adobe Commerce Optimizer]이(가) 아닌 [!DNL Adobe Commerce]에서 구성을 변경합니다. 수리는 커넥터 관리 정책과 함께 수동으로 추가한 정책을 제거하지 않습니다.

페이지 수준 단추를 사용하여 다음을 조정합니다.

- **[!UICONTROL Reconcile]** - 구성 차이점을 확인하고 [!DNL Adobe Commerce Optimizer]에서 변경하지 않고 동기화 상태를 업데이트합니다.

- **[!UICONTROL Reconcile & Repair]** - 구성 차이점을 확인하고 복구 가능한 차이점에 대한 예상 구성을 자동으로 복원합니다.

  **[!UICONTROL Reconcile & Repair]**&#x200B;을(를) 선택하면 비동기 조정 요청이 전송되며 복구가 실행되기 전에 반환됩니다. 확인 메시지에 상태가 곧 새로 고쳐진다고 표시되지만 페이지가 자동으로 다시 로드되지 않습니다. 처리가 완료될 때까지 기다린 다음 그리드를 새로 고쳐 결과를 확인합니다.

행에서 **[!UICONTROL Action]** 메뉴를 사용하여 다음을 수행할 수 있습니다.

- **[!UICONTROL View details]** - 현재 상태, 드리프트, 액세스 키 및 최근 이벤트를 보려면 [카탈로그 동기화 상태 보기] 세부 정보 페이지를 엽니다.
- **[!UICONTROL Open in ACO admin]** - [!DNL Adobe Commerce Optimizer] Studio에서 카탈로그 보기 세부 정보 페이지를 엽니다.
- **[!UICONTROL Copy ID]** - 참조할 카탈로그 보기 ID를 복사합니다.

## ACO 탭에서 고립됨 {#orphaned-in-aco-tab}

**[!UICONTROL Orphaned in ACO]** 탭에는 [!DNL Adobe Commerce Optimizer]에 있지만 해당 [!DNL Adobe Commerce] 원본이 없는 카탈로그 보기 및 제한된 액세스 키(예: 커넥터가 아닌 [!DNL Adobe Commerce Optimizer] Studio에서 수동으로 만든 엔터티)가 나열됩니다. 이 엔터티와 일치하는 [!DNL Adobe Commerce] 레코드가 없으므로 이 엔터티를 기본 격자에 표시할 수 없습니다.

![Adobe Commerce 소스가 없는 엔터티를 나열하는 ACO 탭에서 고립됨](assets/catalog-view-sync-orphan.png){width="600" zoomable="yes"}

| 필드 | 설명 |
| --- | --- |
| **유형** | 분리된 엔터티의 범주: [!UICONTROL Catalog View] 또는 [!UICONTROL Access Key]. |
| **ACO ID** | [!DNL Adobe Commerce Optimizer]에 있는 엔터티의 식별자입니다. |
| **세부 정보** | 정책에 대한 추가 컨텍스트입니다. |
| **처음 표시** | 조정에서 이 엔티티를 처음 감지한 경우 |
| **작업** | 엔터티 식별자를 복사하려면 **[!UICONTROL Copy ID]**&#x200B;을(를) 선택하십시오. 복사된 ID를 사용하여 [!DNL Adobe Commerce Optimizer] Studio 카탈로그 보기에서 엔터티를 찾아 제거합니다. |

>[!NOTE]
>
>이 탭은 보고서 전용입니다. 조정은 분리된 엔티티를 삭제하지 않습니다. 더 이상 필요하지 않은 경우 [!DNL Adobe Commerce Optimizer] Studio에서 직접 제거하십시오.

## 삭제된 탭 {#deleted-tab}

**[!UICONTROL Deleted]** 탭에는 공유된 카탈로그가 [!DNL Adobe Commerce]에서 삭제되어 제거된 카탈로그 보기 예상이 나열됩니다. 공유 카탈로그 및 해당 카탈로그 보기가 더 이상 존재하지 않으므로 이러한 행은 아무 곳에도 연결되지 않습니다. 제거된 항목에 대한 기록으로만 유지됩니다.

![공유된 카탈로그 삭제 후 제거된 카탈로그 보기 프로젝션을 나열하는 삭제된 탭](assets/catalog-view-sync-deleted.png){width="600" zoomable="yes"}

| 필드 | 설명 |
| --- | --- |
| **카탈로그 보기** | 제거된 카탈로그 보기의 식별자입니다. |
| **Source** | 삭제된 공유된 카탈로그. |
| **보기 저장** | 저장소는 표시된 카탈로그 보기를 표시합니다. |
| **삭제된 시간** | 투영이 제거되었을 때입니다. |

이 탭의 행은 90일 후에 자동으로 지워집니다.

## 알려진 제한 사항

- 커넥터 관리 카탈로그 보기와 수동으로 만든 카탈로그 보기를 구별하는 시각적 표시기가 [!DNL Adobe Commerce Optimizer] Studio에 없습니다. [!DNL Adobe Commerce Optimizer] Studio UI가 아닌 이 페이지를 사용하여 커넥터가 관리하는 항목을 결정합니다.
- **[!UICONTROL Orphaned in ACO]** 탭의 **[!UICONTROL ACO ID]** 열은 고유 식별자가 아닌 카탈로그 보기, 정책 또는 액세스 키를 식별합니다. 열 이름은 변경될 수 있습니다.

>[!MORELIKETHIS]
>
> - [카탈로그 보기 구성 관리](/help/b2b/catalog-views-manage.md) - 공유 카탈로그 또는 회사 계정에서 카탈로그 보기 검토
> - [데이터 피드 동기화 상태](data-feed-sync-status.md)
> - [서비스 > ACO 카탈로그 보기 동기화](../configuration-reference/services/aco-catalog-view-sync.md) - 삭제 및 만들기 유예 기간 및 드리프트 조정자를 구성합니다.
> - [제한된 액세스 키 관리](restricted-access-keys.md) — 이 페이지에서 만료가 표시되는 키를 관리합니다.
> - *Adobe Commerce Optimizer Connector 안내서*&#x200B;의 [B2B 공유 카탈로그에 대한 카탈로그 보기 동기화 모니터링](https://experienceleague.adobe.com/en/docs/commerce/aco-optimizer-connector/manage-sync/catalog-view-sync/catalog-view-sync-status)
> - [비공개 카탈로그 보기](https://experienceleague.adobe.com/en/docs/commerce/optimizer/setup/private-catalog-view)
> - [제한된 액세스 키](https://experienceleague.adobe.com/en/docs/commerce/optimizer/setup/restricted-access-keys)
