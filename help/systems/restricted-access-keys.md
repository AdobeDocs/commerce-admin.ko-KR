---
title: Commerce의 제한된 액세스 키 관리
description: Adobe Commerce Optimizer에 동기화된 B2B 공유 카탈로그 보기를 보호하는 제한된 액세스 키를 만들고, 할당하고, 삭제합니다.
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
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
    internal-label: Admin
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
    internal-label: Intermediate
topic_v2:
  - id: c1579802-ddd4-4214-8a91-97b2066abe11
    internal-label: Troubleshooting
  - id: ebde5b41-29c9-4f5e-9ef6-1197e85409e3
    internal-label: Data management
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
    internal-label: Administration
last-update: 2026-10-01
source-git-commit: 82862dcdd7667b46cfe7bd08863926ae5bafd24b
workflow-type: tm+mt
source-wordcount: '813'
ht-degree: 0%
---

# 제한된 액세스 키 관리

[!DNL Adobe Commerce Optimizer Connector for B2B]이(가) 만든 비공개 카탈로그 보기에 대한 액세스 키를 관리하려면 [제한된 액세스 키] 페이지를 사용하십시오. 커넥터가 Adobe Commerce에서 Adobe Commerce Optimizer으로 B2B 공유 카탈로그 구성을 동기화합니다.

>[!NOTE]
>
>파트너 포털과 같이 B2B가 아닌 시나리오에서 개인 카탈로그를 관리하는 데 사용되는 수동으로 만든 키의 경우 [[!DNL Adobe Commerce Optimizer Studio]](https://experienceleague.adobe.com/ko/docs/commerce/optimizer/setup/restricted-access-keys){target="_blank"}에서 키를 관리합니다.

## 대상자 및 가용성 {#audience}

[!BADGE PaaS만]{type=Informative url="https://experienceleague.adobe.com/ko/docs/commerce/user-guides/product-solutions" tooltip="Adobe Commerce 온 클라우드 인프라 및 온프레미스 프로젝트에만 적용됩니다."}

[!UICONTROL Restricted Access Keys] 페이지는 B2B 공유 카탈로그를 사용하는 Adobe Commerce on Cloud Infrastructure 및 온-프레미스 상인이 [!DNL Adobe Commerce Optimizer Connector for B2B]과(와) 사용할 수 있습니다. 커넥터가 페이지를 자동으로 설치하고 활성화합니다.

공유 카탈로그에 대해 카탈로그 보기가 처음 만들어지면 커넥터가 자동으로 키 하나를 생성하여 할당합니다. 이 페이지에서는 해당 키를 보고 추가 키를 생성, 할당 또는 삭제할 수 있습니다.

## 제한된 액세스 키 페이지에 액세스 {#access-restricted-access-keys-page}

관리 영역에서 **[!UICONTROL System]** > **[!UICONTROL Data Transfer]** > **[!UICONTROL Restricted Access Keys]**(으)로 이동합니다.

![키가 나열된 제한된 액세스 키 페이지와 할당된 카탈로그 보기](assets/restricted-access-keys.png){width="600" zoomable="yes"}

이 페이지에는 카탈로그 보기에 할당되었는지 여부에 관계없이 모든 키가 나열됩니다. 특정 카탈로그 보기에 키를 할당하려면 해당 카탈로그 보기에서 [!UICONTROL Edit Restricted Access Keys] 동작을 대신 사용하십시오. [카탈로그 보기에 키 할당](#assign-keys-to-a-catalog-view)을 참조하세요.

## 제한된 액세스 키 요약 {#restricted-access-keys-summary}

그리드에는 행당 하나의 키가 있습니다.

| 필드 | 설명 |
| --- | --- |
| **키 ID** | 고유 키 식별자. |
| **제목** | 키를 식별하기 위해 제공하는 레이블입니다. |
| **할당된 카탈로그 보기** | 카탈로그는 이 키가 현재 할당된 것으로 봅니다. |
| **다음 시간에 만료** | 키 만료 날짜입니다. |
| **작업** | 행 수준 작업입니다. [키 관리](#manage-keys)를 참조하십시오. |

## 키 관리 {#manage-keys}

- **[!UICONTROL Create Key]** - 할당되지 않은 새 키 쌍을 생성합니다. Commerce은 키 쌍을 생성하고 개인 키를 저장합니다. 카탈로그 보기에 키를 할당할 때까지 공개 키가 [!DNL Adobe Commerce Optimizer]에 등록되지 않습니다.
- **[!UICONTROL View Public Key]**—키의 공개 키에 대한 읽기 전용 보기를 열므로 필요한 경우 키를 다시 등록하거나 다시 동기화하도록 복사할 수 있습니다. 개인 키가 표시되지 않습니다.
- **[!UICONTROL Delete]**—키를 제거하고 [!DNL Adobe Commerce Optimizer]에서 해당 원격 등록을 취소합니다. 이 키로 이미 발급된 상점 토큰은 만료될 때까지 유효합니다. 이 작업은 취소할 수 없습니다.

>[!NOTE]
>
>만료된 키만 삭제할 수 있습니다. 만료된 키는 할당하거나 할당을 취소할 수 없습니다.

## 키 만들기

[!UICONTROL Restricted Access Keys] 페이지에서 **[!UICONTROL Create Key]**&#x200B;을(를) 선택하여 키를 만듭니다.

Commerce은 새 키 쌍을 생성하고 개인 키를 저장합니다. 제한된 액세스 키 테이블은 고유 키 ID를 보여주는 새 키 항목으로 업데이트됩니다. 카탈로그 보기에 키를 할당할 때 이 [!UICONTROL Key ID]을(를) 사용합니다.

카탈로그 보기에 키를 할당할 때까지 공개 키가 [!DNL Adobe Commerce Optimizer]에 등록되지 않습니다. 등록 후 제한된 액세스 키 테이블 항목이 업데이트되어 카탈로그 할당 및 만료 날짜가 표시됩니다.

## 제한된 액세스 키 할당 또는 제거 {#assign-keys-to-a-catalog-view}

{{$include /help/_includes/edit-restricted-access-keys.md}}

## 키 선택 및 회전 {#key-selection-and-rotation}

카탈로그 보기에 두 개 이상의 키가 할당되면 [!DNL Adobe Commerce]은(는) 최신 만료 날짜가 지정된 할당되고 만료되지 않은 키를 자동으로 사용하여 토큰에 서명합니다.

>[!IMPORTANT]
>
>자동 키 회전은 아직 사용할 수 없습니다. 키는 기본적으로 만료 기간이 깁니다. 키를 수동으로 회전하려면 새 키를 만들어 기존 키와 함께 카탈로그 보기에 할당합니다. 새 키를 사용 중인지 확인한 후 이전 키를 삭제합니다.

새로 만든 키에 적용되는 기본 만료 기간을 변경하려면 **[!UICONTROL Stores]** > **[!UICONTROL Configuration]** > **[!UICONTROL Services]** > **[!UICONTROL ACO Restricted Access Keys]** > **[!UICONTROL Provisioning]** > **[!UICONTROL Default key lifetime (days)]**(으)로 이동합니다. [서비스 > ACO 제한된 액세스 키](../configuration-reference/services/aco-restricted-access-keys.md)를 참조하십시오.

## 알려진 제한 사항 {#known-limitations}

- 기본 [!UICONTROL Restricted Access Keys] 표에 활성 또는 상태 표시기가 없습니다.

  [!UICONTROL Edit Restricted Access Keys] 페이지에서 링크 상태를 볼 수 있습니다. 드롭다운을 사용하여 사용 가능한 키 및 해당 상태를 봅니다. 키가 카탈로그 보기에 할당되면 연결됩니다. 할당되지 않은 경우 상태가 없습니다. 이러한 키를 편집 중인 카탈로그 보기에 할당할 수 있습니다.

  [!UICONTROL Catalog View Sync Status] 페이지에서 카탈로그 보기 세부 정보 페이지(**[!UICONTROL View details]** 동작)에서 카탈로그 보기에 연결된 키를 볼 수 있습니다. 또한 세부 사항 페이지에는 카탈로그 보기에서 할당 또는 할당 해제된 시기를 포함하여 주요 내역이 표시됩니다.

- 자동 키 회전은 아직 사용할 수 없습니다.

>[!MORELIKETHIS]
>
> - [카탈로그 보기 구성 관리](/help/b2b/catalog-views-manage.md) - 공유 카탈로그 또는 회사 계정에서 이 키를 할당합니다
> - [카탈로그 보기 동기화 상태 모니터링](catalog-view-sync-status.md) - 이 키가 보호하는 카탈로그 보기를 모니터링하고 조정합니다.
> - [서비스 > ACO 제한된 액세스 키](../configuration-reference/services/aco-restricted-access-keys.md) — 기본 키 만료 기간을 구성합니다.
> - [서비스 > ACO 카탈로그 보기](../configuration-reference/services/aco-catalog-view.md) — 상점 액세스 토큰 라이프타임을 구성하고 발급을 활성화하거나 비활성화합니다.
> - [제한된 액세스 키 관리](https://experienceleague.adobe.com/ko/docs/commerce/aco-optimizer-connector/manage-sync/catalog-view-sync/restricted-access-keys){target="_blank"}(*Adobe Commerce Optimizer Connector 안내서*) - 이러한 키가 B2B 공유 카탈로그 동기화에 어떻게 적합한지 알아봅니다.
> - *Adobe Commerce Optimizer 안내서*&#x200B;의 [제한된 액세스 키](https://experienceleague.adobe.com/ko/docs/commerce/optimizer/setup/restricted-access-keys){target="_blank"} — 비 B2B 사용 사례에 대한 수동 ACO Studio 기반 키 흐름
