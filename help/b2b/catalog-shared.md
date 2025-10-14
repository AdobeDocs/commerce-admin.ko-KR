---
title: 공유 카탈로그 개요
description: Adobe Commerce B2B에서 제공하는 공유 카탈로그와 이를 사용하여 다양한 회사 계정의 사용자 지정 가격으로 제어된 카탈로그를 유지 관리하는 방법에 대해 알아봅니다.
exl-id: cf7c9099-9b7d-407b-adb9-06a4815624ee
feature: B2B, Companies, Catalog Management
source-git-commit: 61df9a4bcfaf09491ae2d353478ceb281082fa74
workflow-type: tm+mt
source-wordcount: '595'
ht-degree: 0%

---

# 공유 카탈로그 개요

Adobe Commerce B2B를 사용하면 다른 회사의 사용자 지정 가격으로 제어된 _공유_ 카탈로그를 유지 관리할 수 있습니다. 표준 _기본_ 제품 카탈로그 외에도 가격 구조가 다른 두 가지 유형의 공유 카탈로그에 대한 고객 액세스를 제공합니다.

구성에서 [공유 카탈로그 기능](enable-basic-features.md)을(를) 사용하도록 설정한 경우, 원래 기본 카탈로그는 관리자로부터 계속 표시되지만 기본(일반) 공용 공유 카탈로그만 상점에서 표시됩니다. 또한 특정 [회사](account-companies.md) 계정의 구성원에게만 표시되는 사용자 지정 카탈로그를 만들 수 있습니다.

`Default (General)` 공용 공유 카탈로그의 경우 상점에 카탈로그를 표시할 제품을 할당해야 합니다. 기본적으로 비어 있으며 어떤 제품도 포함되어 있지 않습니다.

>[!NOTE]
>
>**[B2B 릴리스 1.3.0](release-notes.md#b2b-v130) 이상** — 공유 카탈로그를 만들 때 카탈로그 권한 설정에서 이 액세스 권한이 할당된 고객 그룹에 대해 카탈로그에 대한 각 [범주 권한](../catalog/category-permissions.md)이 _[!UICONTROL Allow for the Display Product Prices]_&#x200B;및&#x200B;_[!UICONTROL Add to Cart]_(으)로 설정됩니다. 이전에는 카탈로그 권한이 `Allow`(으)로 설정되어 있어도 이 설정이 `Deny`(으)로 자동 설정되었습니다.

>[!IMPORTANT]
>
>**_[!UICONTROL Shared Catalog]_** 기능을 사용하도록 설정하면 카탈로그의 **_모든_** 범주에서 기존의 모든 [그룹 권한 설정](../configuration-reference/catalog/catalog.md#category-permissions)을 무시합니다. [!UICONTROL Shared Catalog]은(는) 카탈로그가 활성화되면 카탈로그의 모든 범주 권한을 완전히 제어합니다.

_[!UICONTROL Shared Catalogs]_&#x200B;페이지에서는 공유 카탈로그 관리에 사용되는 도구에 액세스할 수 있습니다. 페이지는 필터 및 작업 컨트롤이 있는 표준 [관리 작업 영역](../getting-started/admin-workspace.md)과(와) 유사합니다. 그리드는 기본 공개 공유 카탈로그를 비롯한 모든 공유 카탈로그와 설정한 사용자 지정 카탈로그를 나열합니다.

![공유된 카탈로그](./assets/shared-catalogs-grid.png){width="700" zoomable="yes"}

## [!UICONTROL Shared Catalogs] 페이지 액세스

_관리자_ 사이드바에서 **[!UICONTROL Catalog]** > **[!UICONTROL Shared Catalogs]**(으)로 이동합니다.

## 작업 컨트롤

왼쪽 위 모서리에 있는 [actions 컨트롤](../getting-started/admin-actions-control.md)은(는) mass actions 컨트롤과 함께 사용하여 더 이상 필요하지 않은 선택된 공유 카탈로그를 삭제할 수 있습니다. 격자에 있는 _[!UICONTROL Actions]_&#x200B;열에는 공유 카탈로그를 관리하기 위한 전체 도구가 포함되어 있습니다.

![공유된 카탈로그 작업](./assets/shared-catalog-grid-action-column-controls.png){width="350"}

| 제어 | 설명 |
|------|-----------|
| [[!UICONTROL Set Pricing and Structure]](catalog-shared-pricing-structure.md) | 공유 카탈로그에서 사용할 수 있는 제품 선택 및 사용자 지정 가격을 결정합니다. |
| [[!UICONTROL Assign Companies]](catalog-shared-assign-companies.md) | 공유 카탈로그에 액세스할 수 있는 회사를 결정합니다. |
| [[!UICONTROL General Settings]](catalog-shared-manage.md) | 이름, 카탈로그 유형, 고객 세금 분류 및 설명을 포함한 카탈로그 세부 정보를 결정합니다. |
| [!UICONTROL Delete] | 선택한 공유 카탈로그를 삭제합니다. |

{style="table-layout:auto"}

## 열 설명

| 제목 | 설명 |
|--- |--- |
| [!UICONTROL Select] | 작업을 적용할 공유 카탈로그 레코드를 선택합니다. 헤더의 컨트롤은 그리드에서 모든 공유 카탈로그 레코드를 선택하거나 선택을 해제하는 데 사용할 수 있습니다. 개별 공유 카탈로그를 선택하려면 확인란을 선택합니다. |
| [!UICONTROL ID] | 카탈로그가 생성될 때 순차적으로 할당되는 고유 숫자 식별자입니다. |
| [!UICONTROL Name] | 공유 카탈로그의 이름입니다. 기본적으로 기본(일반) 공유 카탈로그를 사용할 수 있습니다. |
| [!UICONTROL Type] | 공유 카탈로그의 형식을 <br/>**[!UICONTROL Public]**(으)로 식별합니다. Adobe Commerce B2B가 설치되면 기본 공용 공유 카탈로그가 자동으로 만들어집니다. 처음에는 `General` 및 `Not Logged In` 고객 그룹에 할당되며 회사와 연결되지 않은 게스트 및 개별 로그인 고객에게 표시됩니다. 시스템은 한 번에 하나의 공개 공유 카탈로그만 지원합니다.<br/>**[!UICONTROL Custom]** - 사용자 지정 공유 카탈로그에는 할당된 회사 계정의 로그인한 동료에게만 표시되는 가격이 포함되어 있습니다. 필요한 만큼 사용자 정의 공유 카탈로그를 만들 수 있습니다. |
| [!UICONTROL Customer Tax Class] | 해당 고객 그룹에 지정된 세금 분류. 이 열은 기본 그리드에 나타나지 않지만 열 레이아웃을 변경하여 추가할 수 있습니다. |
| [!UICONTROL Created At] | 공유 카탈로그가 생성된 날짜와 시간입니다. |
| [!UICONTROL Created By] | 공유 카탈로그를 만든 스토어 관리자의 이름과 성입니다. |
| [!UICONTROL Action] | 선택한 카탈로그에 적용되는 작업을 나열합니다. 옵션: `Set Pricing and Structure` / `Assign Companies` / `General Settings` / `Delete` |

{style="table-layout:auto"}
