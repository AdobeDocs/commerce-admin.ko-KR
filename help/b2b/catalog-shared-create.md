---
title: 공유 카탈로그 만들기
description: 공유 카탈로그를 만들고 기존 공유 카탈로그를 복제하는 방법에 대해 알아봅니다.
exl-id: 969c352c-ff88-4902-8347-334ee8b79afb
feature: B2B, Companies, Catalog Management
role: Admin
source-git-commit: 61df9a4bcfaf09491ae2d353478ceb281082fa74
workflow-type: tm+mt
source-wordcount: '871'
ht-degree: 0%

---

# 공유 카탈로그 만들기

다음과 같은 경우 [공유된 카탈로그](catalog-shared.md) 가 만들어지면 시스템에서 자동으로 [고객 그룹](account-company-customer-group.md) 같은 이름으로. 예를 들어 이라는 공유 카탈로그를 만드는 경우 _카탈로그_&#x200B;로 나열된 상태로 남아 있는 문제를 해결했습니다 _카탈로그_ 고객 그룹. 공유 사용자 지정 카탈로그에 회사를 할당하는 것은 고객 그룹에 할당하는 것과 본질적으로 동일합니다.

새 공유 카탈로그에는 제품, 사용자 지정 가격 또는 회사 연결이 포함되지 않습니다. 공유 카탈로그가 활성화될 때 생성되는 기본 공유 카탈로그인 공개 카탈로그는 회사와 관련이 없는 게스트 및 고객에게 자동으로 할당됩니다.

![공유 카탈로그](./assets/shared-catalogs-grid.png){width="700" zoomable="yes"}

공유 카탈로그를 사용하려면 먼저 다음 측면을 설정해야 합니다.

- 카탈로그 범위
- 제품 선택
- 사용자 정의 가격
- 회사 할당

## 가격 범위

다중 사이트 설치가 있는 경우 공유 카탈로그를 만들기 전에 가격 범위를 구성해야 합니다. 다음 [가격 범위](../catalog/catalog-price-scope.md) 을 로 설정할 수 있습니다. `Global` 또는 `Website`. 단, 설정 프로세스의 시작 부분에서만 설정할 수 있습니다. 웹 사이트 선택기는 의 2단계 중에 나타납니다. [공유 카탈로그 설정](catalog-shared-pricing-structure.md).

![웹 사이트 선택기](./assets/shared-catalog-scope-pricing.png){width="600" zoomable="yes"}

1. 다음에서 _관리자_ 사이드바, 이동 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. 왼쪽 패널에서 를 확장합니다. **카탈로그** 및 선택 **카탈로그** 밑에.

1. 확장 ![확장 선택기](../assets/icon-display-expand.png) 다음 **가격** 섹션.

1. 설정 **카탈로그 가격 범위** 끝 `Website`.

   ![카탈로그 가격 범위](../configuration-reference/catalog/assets/catalog-price.png){width="600" zoomable="yes"}

1. 클릭 **[!UICONTROL Save Config]**.

## 1단계: 공유 카탈로그 만들기

두 가지 방법으로 공유 카탈로그를 만들 수 있습니다. 두 유형 중 하나의 공유 카탈로그를 만들거나 기존 공유 카탈로그를 복제할 수 있습니다. 새 공유 카탈로그에 제품이 포함되어 있지 않고 아직 회사에 할당되지 않았습니다.

### 방법 1: 새 공유 카탈로그 추가

1. 다음에서 _관리자_ 사이드바, 이동 **[!UICONTROL Catalog]** > **[!UICONTROL Shared Catalogs]**.

1. 오른쪽 위 모서리에서 을(를) 클릭합니다. **[!UICONTROL Add Shared Catalog]** 다음을 수행합니다.

   - 입력 **[!UICONTROL Name]** 공유 카탈로그용.

     지정하는 이름은 해당하는 경우 공유 카탈로그를 참조하기 위해 관리 및 고객 대시보드 전체에 사용됩니다. 또한 해당 고객 그룹의 이름이 됩니다.

   - 선택 **[!UICONTROL Type]** : `Custom` 또는 `Public`.

   - 적절한 항목 선택 **[!UICONTROL Customer Tax Class]** 이는 공유 카탈로그에서 수행한 구매에 적용됩니다.

     세금 분류 설정 및 정의에 대한 자세한 내용은 [세금 등급](../stores-purchase/tax-class.md).

     다음 예는 특정 도매 고객을 위한 새로운 사용자 정의 카탈로그를 보여 줍니다.

     ![새 공유 카탈로그](./assets/shared-catalog-new.png){width="600" zoomable="yes"}

   - 입력 **[!UICONTROL Description]**

1. 완료되면 다음을 클릭: **[!UICONTROL Save]**.

   새 카탈로그가 다음 위치에 나타납니다. _[!UICONTROL Shared Catalogs]_그리드.

### 방법 2: 기존 공유 카탈로그 복제

중복 사용자 정의 카탈로그는 원본의 가격 책정 모델 및 구조를 유지하지만 회사 연결은 유지하지 않습니다. 해당 고객 그룹도 중복 카탈로그와 동일한 이름으로 만들어집니다. 기본적으로 중복 카탈로그에 이름이 지정됩니다 _중복_ 원본 카탈로그.

공개 공유 카탈로그가 중복되면 중복 카탈로그의 유형은 다음과 같이 변경됩니다. `custom`.

1. 다음에서 _관리자_ 사이드바, 이동 **[!UICONTROL Catalog]** > **[!UICONTROL Shared Catalogs]**.

1. 복제할 그리드의 공유 카탈로그에 대해 **[!UICONTROL Action]** 열 및 선택 **[!UICONTROL General Settings]**.

1. 페이지 상단의 옵션에서 을(를) 클릭합니다. **[!UICONTROL Duplicate]**.

   ![공유 카탈로그 복제](./assets/shared-catalog-duplicate.png){width="600" zoomable="yes"}

1. 새 카탈로그에 대한 다음 필드를 업데이트합니다.

   - **[!UICONTROL Name]**
   - **[!UICONTROL Type]**
   - **[!UICONTROL Customer Tax Class]**
   - **[!UICONTROL Description]**

1. 완료되면 다음을 클릭: **[!UICONTROL Save]**.

   중복 항목이 _[!UICONTROL Shared Catalogs]_고유 ID가 있는 그리드.

## 2단계: 설정 완료

새 공유 카탈로그를 만든 후 적절한 제품 선택 사항으로 구성해야 합니다. [회사 할당](catalog-shared-assign-companies.md), 및 [범주 권한](../catalog/category-permissions.md). 계속하려면 다음을 참조하십시오. [가격 및 구조 설정](catalog-shared-pricing-structure.md).

>[!NOTE]
>
>**[B2B 릴리스 1.3.0](release-notes.md#b2b-v130) 및 나중에** — 공유 카탈로그를 만들 때 각각 [범주 권한](../catalog/category-permissions.md) 카탈로그가 다음으로 설정됨: _[!UICONTROL Allow for the Display Product Prices]_및_[!UICONTROL Add to Cart]_ 카탈로그 권한 설정에서 이 액세스 권한이 할당된 고객 그룹의 경우. 이전에는 이러한 설정이 자동으로 로 설정되었습니다. `Deny` 카탈로그 권한이 다음으로 설정된 경우에도 `Allow`.

## 공유된 카탈로그 데모

공유 카탈로그 관리에 대한 데모를 보려면 다음 비디오를 시청하십시오.

>[!VIDEO](https://video.tv.adobe.com/v/344446?quality=12&learn=on)

## 공유 카탈로그 페이지 참조

### 단추 막대

| 단추 | 설명 |
|--- |--- |
| [!UICONTROL Back] | 새 공유 카탈로그를 저장하지 않고 공유 카탈로그 페이지로 돌아갑니다. |
| [!UICONTROL Reset] | 저장하지 않은 변경 내용의 양식을 지우고 원래 카탈로그 세부 정보를 복원합니다. |
| [!UICONTROL Save and Continue Edit] | 모든 변경 사항을 저장하고 편집 모드에서 양식을 열어 둡니다. |
| [!UICONTROL Save] | 변경 사항을 저장하고, 양식을 닫은 다음 공유 카탈로그 페이지로 돌아갑니다. |

{style="table-layout:auto"}

### 카탈로그 세부 정보

| 필드 | 설명 |
|--- |--- |
| [!UICONTROL Name] | 관리자 전체와 사용 가능한 고객 계정에서 공유 카탈로그를 식별합니다. 카탈로그 이름은 설명적이어야 하며 길이는 32자 이하여야 합니다. 이름이 같은 두 개의 공유 카탈로그를 가질 수 없습니다. 최대 문자 수: 32 |
| [!UICONTROL Type] | **[!UICONTROL Custom]** - 지정된 특정 회사에만 사용할 수 있는 사용자 지정 가격 책정 카탈로그를 식별합니다.<br/>**[!UICONTROL Public]**- 모든 게스트 방문자 및 회사와 연관되지 않은 로그인 고객에게 사용할 수 있는 공유 카탈로그를 식별합니다. 다음과 같은 경우 기본 공개 공유 카탈로그가 만들어집니다. [!DNL Adobe Commerce B2B] 이(가) 설치되었지만 저장소 관리자가 구성해야 합니다. 공개 공유 카탈로그는 한 번에 하나만 존재할 수 있습니다. |
| [!UICONTROL Customer Tax Class] | 카탈로그에서 구매한 항목에 사용할 세금 분류를 결정합니다. 옵션에는 사용 가능한 모든 세금 분류가 포함됩니다. |
| [!UICONTROL Description] | 카탈로그 사용 방법에 대한 간단한 설명. |

{style="table-layout:auto"}

### 그리드 열

| 필드 | 설명 |
|--- |--- |
| [!UICONTROL ID] | 공유 카탈로그 엔티티에 할당된 고유 숫자 식별자입니다. |
| [!UICONTROL Name] | 공유 카탈로그의 이름입니다. |
| [!UICONTROL Type] | 공유 카탈로그의 유형을 나타냅니다. 다음과 같을 수 있습니다. `Public` 또는 `Custom`. |
| [!UICONTROL Created At] | 시스템에서 공유 카탈로그를 만든 날짜입니다. |
| [!UICONTROL Created By] | 공유 카탈로그를 만든 관리자 사용자의 이름입니다. |
| [!UICONTROL Action] | 작업 목록입니다. 옵션: `Set Pricing and Structure`, `Assign Companies`, `General Settings`, `Delete`. |

{style="table-layout:auto"}
