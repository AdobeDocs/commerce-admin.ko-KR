---
title: 고객 목록
description: 고객 그리드는 스토어에 계정을 등록했거나 관리자가 추가한 모든 고객을 나열합니다.
exl-id: a7d9b098-4892-492c-b937-61cc33b836d8
source-git-commit: c855a691ed33e1e6e74865ebdfb30ddad21ad83e
workflow-type: tm+mt
source-wordcount: '587'
ht-degree: 0%

---

# 고객 목록

관리자의 [!UICONTROL Customers] 격자는 스토어에 계정을 등록했거나 관리자가 추가한 모든 고객을 나열합니다. 표준 [표 형태 컨트롤](../getting-started/admin-grid-controls.md)을 사용하여 목록을 필터링하고 열 레이아웃을 조정하세요. 자세한 내용은 [고객 계정 관리](../customers/manage-account.md)를 참조하세요.

![고객 목록](assets/customer-accounts-all-grid.png){width="700" zoomable="yes"}

## 고객 정보 업데이트

1. _관리자_ 사이드바에서 **[!UICONTROL Customers]** > **[!UICONTROL All Customers]**(으)로 이동합니다.

1. 고객 레코드를 찾아 _[!UICONTROL Action]_&#x200B;열에서&#x200B;[!UICONTROL **편집**]을(를) 클릭합니다.

1. 왼쪽 패널에서 편집할 정보를 선택하고 필요한 사항을 변경합니다.

   >[!NOTE]
   >
   >자세한 내용은 [고객 계정 업데이트](../customers/update-account.md)를 참조하세요.

1. 완료되면 **[!UICONTROL Save Customer]**&#x200B;을(를) 클릭합니다.

## Workspace 컨트롤

| 제어 | 설명 |
| --- | --- |
| **[!UICONTROL Add New Customer]** | 고객 계정을 만듭니다. |
| **[!UICONTROL Search]** | 현재 필터를 기반으로 고객 검색을 시작합니다. |
| **[!UICONTROL Filters]** | [grid](../getting-started/admin-grid-controls.md)에 나타나는 레코드를 필터링하는 데 사용되는 검색 매개 변수 집합을 정의합니다. |
| **[!UICONTROL Default View]** | 그리드의 기본 열 [레이아웃](../getting-started/admin-grid-controls.md)을(를) 결정합니다. |
| **[!UICONTROL Columns]** | 그리드에서 [열](../getting-started/admin-grid-controls.md)과(와) 해당 계정의 선택을 결정합니다. 열 레이아웃을 변경하고 _보기_(으)로 저장할 수 있습니다. 기본적으로 일부 열만 격자에 포함됩니다. |
| **[!UICONTROL Export]** | 선택한 레코드를 CSV 또는 Excel XML 파일로 내보냅니다. |

{style="table-layout:auto"}

## 열

| 열 | 설명 |
| --- | --- |
| **[!UICONTROL Select]** | 작업을 적용할 고객 레코드에 대한 확인란 선택을 관리합니다. 열 머리글에서 선택 컨트롤을 사용하여 모두 선택/선택 해제할 수도 있습니다. |
| **[!UICONTROL ID]** | 고객 계정이 생성될 때 할당되는 고유 숫자 식별자입니다. |
| **[!UICONTROL Name]** | 고객의 이름과 성입니다. |
| **[!UICONTROL Email]** | 고객의 이메일 주소입니다. |
| **[!UICONTROL Group]** | 고객이 할당된 고객 그룹. |
| **[!UICONTROL Phone]** | 고객 전화번호. |
| **[!UICONTROL ZIP]** | 고객의 우편 번호입니다. |
| **[!UICONTROL Country]** | 고객이 있는 국가입니다. |
| **[!UICONTROL State/Province]** | 고객이 있는 시/도. |
| **[!UICONTROL Customer Since]** | 고객 계정이 생성된 날짜와 시간입니다. |
| **[!UICONTROL Web Site]** | 고객 계정과 연결된 저장소 계층의 웹 사이트. |
| **[!UICONTROL Confirmed Email]** | 확인 이메일이 필요한지 여부를 나타냅니다. |
| **[!UICONTROL Account Created In]** | 고객 계정이 생성된 스토어 보기를 나타냅니다. |
| **[!UICONTROL Date of Birth]** | 고객의 생년월일. <br><br>**_중요:_**&#x200B;현재 보안 및 개인 정보 보호 모범 사례를 준수하면서 다른 개인 식별자를 사용한 고객의 전체 생년월일(월, 일, 년) 저장과 관련된 모든 잠재적인 법적 및 보안 위험에 유의하십시오. 고객의 전체 생년월일 보관을 제한하는 것이 좋으며 대안으로 고객의 생년월일을 사용할 것을 제안했습니다. |
| **[!UICONTROL Tax / VAT Number]** | 해당하는 경우 고객에게 할당된 세금 번호 또는 [부가가치세](../stores-purchase/vat.md) 번호입니다. <br/><br/>이 필드는 VAT 번호와 다릅니다. |
| **[!UICONTROL Gender]** | 고객의 성별. |
| **[!UICONTROL Action]** | 편집 - 회사 계정을 편집 모드로 엽니다. |

{style="table-layout:auto"}

### 추가 열

이러한 열은 그리드의 [열 레이아웃](../getting-started/admin-grid-controls.md)을(를) 변경하여 사용할 수 있습니다.

| 열 | 설명 |
| --- | --- |
| **[!UICONTROL Company]** | 고객의 회사 이름입니다. |
| **[!UICONTROL Street Address]** | 고객의 거리 주소입니다. |
| **[!UICONTROL City]** | 고객이 위치한 도시입니다. |
| **[!UICONTROL Fax]** | 해당하는 경우 고객의 팩스 번호. |
| **[!UICONTROL Billing Firstname]** | 고객의 결제 주소에서 이름. |
| **[!UICONTROL Billing Lastname]** | 고객의 청구 주소의 성. |
| **[!UICONTROL Billing Address]** | 청구 정보를 보낼 주소. |
| **[!UICONTROL Shipping Address]** | 주문이 배송될 주소입니다. |
| **[!UICONTROL VAT Number]** | 고객 주소와 연결된 부가가치세 번호. EU에서 판매되는 [디지털 상품](../stores-purchase/taxes.md)의 경우 VAT는 고객의 청구 주소를 기준으로 합니다. <br/><br/>이 필드는 세금/VAT 번호와 다릅니다. |
| **[!UICONTROL Account Lock]** | 계정의 상태를 나타냅니다. 너무 많은 로그인을 시도한 후 보안 조치로서 고객 계정이 [잠김](../customers/password-options.md)될 수 있습니다. 값: `Locked` / `Unlocked` |

{style="table-layout:auto"}
