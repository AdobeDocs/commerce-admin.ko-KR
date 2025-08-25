---
title: 회사 계층 관리
description: 복잡한 운영 모델을 사용하는 B2B 조직을 지원하기 위해 회사 계층을 구축하고 관리합니다.
feature: B2B, Companies
role: Admin
hide: false
hidefromtoc: false
exl-id: a277ed95-7935-4d27-adb2-35116972732b
source-git-commit: 1fc1e07f20e2c22ac430f384e9e2b278edae405c
workflow-type: tm+mt
source-wordcount: '827'
ht-degree: 0%

---

# 회사 계층 관리

[!UICONTROL Company Hierarchy] 기능을 사용하면 하나의 상위 회사 구조로 여러 관련 회사를 구성할 수 있습니다. 이는 개별 회사 ID를 유지하면서 중앙 집중식 관리가 필요한 자회사, 프랜차이즈, 여러 지점 또는 복잡한 조직 구조를 가진 비즈니스에 이상적입니다.

## 사용 사례

* **관리 중앙 집중화**—단일 상위 회사의 여러 회사에 설정 및 구성을 적용합니다
* **구조 유지**—비즈니스 조직을 반영하는 논리 계층 구조로 회사를 구성합니다.
* **작업 능률화**— 전체 조직의 견적, 구매 주문, 결제 방법 및 배송 설정을 관리합니다.
* **자율성 유지**—개별 회사는 공유 구성의 혜택을 받는 동안 ID를 유지합니다.

## 사전 요구 사항

회사 계층을 만들기 전에 다음을 확인합니다.

* Commerce 설치에서 B2B 기능이 활성화됩니다
* 회사를 관리할 수 있는 관리자 액세스 권한이 있습니다.
* 모자회사는 이미 개별기업으로 만들어진 회사이다
* 상위 설정을 적용하면 기존 하위 회사 구성이 재정의됩니다

## 작동 방식

관리자는 조직 계층 구조의 맨 위에 있는 회사인 지정된 모회사에 관련 회사를 할당하여 회사 계층을 구축할 수 있습니다.

관리자로부터 개별 회사(`[!UICONTROL Company Type] = Company`)를 편집하고 [!UICONTROL Company Hierarchy] 구성에서 관련 회사를 할당하여 상위 회사를 만듭니다.

![회사 계층 구조 표](./assets/company-hierarchy-grid.png){width="700"}

>[!NOTE]
>
>[!UICONTROL Company Hierarchy] 표에 대한 자세한 내용은 [회사 계층 구조](account-company-create.md#company-hierarchy) 필드 설명을 참조하십시오.

상위 회사를 편집하고 *[!UICONTROL Company Hierarchy]* 그리드를 사용하여 회사를 추가하거나 제거하여 회사 할당을 관리합니다. *[!UICONTROL Actions]* 컨트롤을 사용하여 조직의 회사에 대한 [고급 설정 구성](#change-company-settings)을 관리하십시오.

## 상위 회사에 회사 할당

1. _관리자_ 사이드바에서 **[!UICONTROL Customers]** > **[!UICONTROL Companies]**(으)로 이동합니다.

   ![회사 표](./assets/companies-grid-view.png){width="700" zoomable="yes"}

1. [!UICONTROL Companies] 그리드에서 회사 세부 정보 페이지를 열어 할당을 만듭니다.

   * 기존 상위 회사에 추가 회사를 할당하려면 상위 회사에 대해 **[!UICONTROL Edit]** 작업을 선택하십시오.
   * 상위 회사를 만들려면 상위로 지정된 회사에 대해 **[!UICONTROL Edit]** 작업을 선택하십시오.

     기존 상위 또는 하위 회사에서는 새 상위 회사를 만들 수 없습니다.

1. 회사 세부 정보 페이지에서 **[!UICONTROL Company Hierarchy]**&#x200B;을(를) 확장한 다음 **[!UICONTROL Assign Companies]**&#x200B;을(를) 선택합니다.

   ![상위 회사 만들기](./assets/company-hierarchy-grid.png){width="675" zoomable="yes"}

1. 사용 가능한 회사 목록에서 할당할 회사를 선택한 다음 **[!UICONTROL Assign Selected Companies]**&#x200B;을(를) 선택합니다.

   ![할당할 회사 선택](./assets/company-hierarchy-select-companies-assign.png){width="675" zoomable="yes"}

1. 메시지가 표시되면 **[!UICONTROL Assign]**&#x200B;을(를) 선택하여 회사 할당을 완료하십시오.

## 상위 회사에서 회사 할당 해제

1. 회사 페이지에서 **[!UICONTROL Edit]** 작업을 선택하여 상위 회사에 대한 회사 세부 정보 페이지를 엽니다.

   ![상위 회사 세부 정보 페이지](./assets/company-update.png){width="700" zoomable="yes"}

1. **[!UICONTROL Company Hierarchy]**&#x200B;을(를) 확장하여 할당된 회사 목록을 봅니다.

1. 조직에서 회사를 제거합니다.

   * 회사가 제거할 [!UICONTROL Action] 열에서 **[!UICONTROL Select]** > **[!UICONTROL Unassign from parent]**&#x200B;을(를) 클릭합니다.

     ![조직에서 회사 제거](./assets/company-hierarchy-grid-unassign.png){width="640" zoomable="yes"}

   * 메시지가 표시되면 **[!UICONTROL Unassign]**&#x200B;을(를) 선택하여 계층에서 할당된 회사를 제거합니다.

## 조직에 대한 회사 설정 관리

조직의 [고급 설정](account-company-create.md#advanced-settings) 구성을 업데이트하십시오. 다음을 수행할 수 있습니다.

* 모든 하위 회사에 상위 구성 설정 적용
* 조직에서 선택한 회사에 동일한 설정 적용

다음 설정을 적용할 수 있습니다.

* **견적 관리** - 회사에서 견적을 요청하고 관리하는 기능을 활성화하거나 비활성화합니다.
* **구매 주문**—회사에서 구매 주문을 만들고 관리할 수 있는지 여부를 제어합니다.
* **결제 방법 구성**—회사에서 사용할 수 있는 결제 방법을 정의합니다.
* **결제 방법 설정**—특정 결제 방법 매개 변수 및 제한을 구성합니다.
* **배송 방법 가용성**—회사에서 사용할 수 있는 배송 방법을 설정합니다.
* **배송 방법 구성**—배송 방법 설정 및 제한 사항을 정의합니다.

업데이트 프로세스 중에 초기 구성 값은 기본적으로 모회사에 대해 구성된 현재 값으로 설정됩니다. 선택한 회사에 설정을 적용하려면 하나 이상의 설정에 대한 변경 확인란을 선택해야 합니다. 변경 사항을 적용하기 전에 각 설정의 기본값을 업데이트할 수도 있습니다.

>[!WARNING]
>
>상위 회사 설정을 적용하면 크레딧 제한, 결제 방법, 배송 설정 및 사용자 지정 제한을 포함한 기존 하위 회사 구성이 대체됩니다. 설정을 적용한 후에도 회사 라인 항목을 편집하여 개별 상위 및 하위 회사에 대한 고급 설정을 관리하고 사용자 지정할 수 있습니다.

### 우수 사례

상위 회사 설정을 하위 회사에 적용할 때는 다음 모범 사례를 고려하십시오.

* 상위 구성을 적용하기 전에 기존 하위 회사 설정 검토
* 단일 하위 회사의 설정 변경 사항을 먼저 테스트하십시오.
* 영향을 받을 수 있는 회사 관리자에게 변경 사항 전달

### 하위 회사에 상위 구성 설정 적용

1. _관리자_ 사이드바에서 **[!UICONTROL Customers]** > **[!UICONTROL Companies]**(으)로 이동합니다.

1. [!UICONTROL Companies] 그리드에서 **[!UICONTROL Edit]** 열에서 **[!UICONTROL Action]**&#x200B;을(를) 선택하여 상위 회사를 편집합니다.

1. 상위 회사 세부 정보 페이지에서 **[!UICONTROL Company Hierarchy]** 섹션을 확장하여 조직에 포함된 회사를 봅니다.

1. 구성할 회사를 선택합니다.

   ![회사 계층에서 회사 선택](assets/company-hierarchy-select-companies.png){width="675" zoomable="yes"}

1. 표 위의 **[!UICONTROL Actions]** 컨트롤에서 **[!UICONTROL Change company settings]**&#x200B;을(를) 선택합니다.

   ![회사 계층 구조에 대한 회사 설정 변경](assets/company-hierarchy-change-company-settings-action.png){width="675" zoomable="yes"}

1. 설정 구성을 변경합니다.

   * [!UICONTROL Change company settings] 페이지에서 수정할 구성 설정을 찾습니다.

   * 설정을 사용하려면 **[!UICONTROL Change]** 확인란을 선택하십시오.

   * 필요한 경우 값을 업데이트합니다.

     ![여러 회사에 대한 회사 설정 변경](assets/company-hierarchy-change-settings-config.png){width="575" zoomable="yes"}

1. 구성을 업데이트한 후 **[!UICONTROL Apply Changes]**&#x200B;을(를) 선택합니다.

1. 메시지가 표시되면 **[!UICONTROL Change settings]**&#x200B;을(를) 선택하여 선택한 회사에 대한 구성을 업데이트합니다.

>[!MORELIKETHIS]
>
>* [회사 계정 만들기](account-company-create.md) - 계층을 만들기 전에 개별 회사를 만드는 방법을 알아봅니다.
>* [회사 역할 및 권한](account-company-roles-permissions.md) - 회사 구조 내의 사용자 액세스 이해
>* [회사 신용 관리](credit-company.md) - 회사의 신용 한도 및 결제 조건을 구성합니다.
>* [회사 관리](manage-companies.md) - 회사 관리 기능 개요
>* [B2B 기능 사용](enable-basic-features.md) - B2B 기능 사용 및 구성
