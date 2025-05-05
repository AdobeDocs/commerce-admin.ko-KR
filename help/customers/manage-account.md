---
title: 고객 계정 관리
description: '[!UICONTROL Customers] 그리드를 사용하여 고객 계정을 찾고 개별 고객 계정에 대한 정보에 액세스합니다.'
exl-id: 5f817ca8-9d1f-4498-b3bd-989713f0b6ad
source-git-commit: 0316475a37ee09948b9ba3649e059155212ab1ae
workflow-type: tm+mt
source-wordcount: '882'
ht-degree: 0%

---

# 고객 계정 관리

_[!UICONTROL Customers]_&#x200B;그리드를 사용하여 고객 계정을 찾습니다. 표준 [작업 공간 컨트롤](../getting-started/admin-workspace.md)을 사용하여 목록을 필터링하고, [열 레이아웃](../getting-started/admin-grid-controls.md)을 변경하고, 보기를 저장하고, 데이터를 내보낼 수 있습니다. 표 위의 [Actions 컨트롤](../getting-started/admin-actions-control.md)을 사용하여 여러 고객 레코드에 작업을 적용할 수 있습니다.

![모든 고객](assets/customers-all-customers.png){width="700" zoomable="yes"}

고객 계정을 수동으로 업데이트하는 방법에 대한 자세한 내용은 [고객 프로필 업데이트](update-account.md)를 참조하십시오.

## 고객 계정 작업

1. _관리자_ 사이드바에서 **[!UICONTROL Customers]** > **[!UICONTROL All Customers]**(으)로 이동합니다.

1. 그리드의 첫 번째 열에서 업데이트할 각 레코드의 확인란을 선택합니다.

1. 적용할 작업에 대한 지침을 따릅니다.

   >[!INFO]
   >
   >다음 작업은 단일 또는 여러 레코드에 적용할 수 있습니다.

1. 완료되면 **[!UICONTROL Save Config]**&#x200B;을(를) 클릭합니다.

### 뉴스레터 구독

글로벌 [고객 계정 범위](../customers/customer-account-scope.md)가 있는 다중 스토어 및 다중 사이트 설정에서 고객 계정은 여러 사이트 또는 스토어에서 뉴스레터를 구독할 수 있습니다. 고객 계정에 _구독_ 액션을 적용하면 기본 사이트/스토어 보기에 대해서만 뉴스레터 구독이 활성화됩니다.

* **[!UICONTROL Actions]** 컨트롤을 `Subscribe to newsletter`(으)로 설정합니다.

고객의 뉴스레터 구독 관리에 대한 자세한 내용은 [구독자 관리](../merchandising-promotions/newsletter-subscribers.md)를 참조하십시오.

### 뉴스레터 구독 취소

글로벌 [고객 계정 범위](customer-account-scope.md)가 있는 다중 스토어 및 다중 사이트 설정에서 고객 계정은 여러 사이트/스토어의 뉴스레터를 구독할 수 있습니다. 고객 계정에 _구독 취소_ 작업을 적용하면 모든 활성 구독이 구독 취소됩니다.

1. **[!UICONTROL Actions]** 컨트롤을 `Unsubscribe to newsletter`(으)로 설정합니다.

1. 확인 메시지가 표시되면 **확인**&#x200B;을 클릭합니다.

### 고객 그룹 할당

1. **[!UICONTROL Actions]** 컨트롤을 `Assign a customer group`(으)로 설정합니다.

1. 선택한 모든 고객 레코드를 할당할 고객 그룹을 선택합니다.

1. 확인 메시지가 표시되면 **[!UICONTROL OK]**&#x200B;을(를) 클릭합니다.

### 고객 계정 삭제

삭제된 고객 계정은 복원할 수 없습니다. 고객 활동 및 거래에 대한 정보는 시스템에 유지됩니다.

1. **[!UICONTROL Actions]** 컨트롤을 `Delete`(으)로 설정합니다.

1. 확인 메시지가 표시되면 **[!UICONTROL OK]**&#x200B;을(를) 클릭합니다.

## 고객 계정 내보내기

1. _관리자_ 사이드바에서 **[!UICONTROL Customers]** > **[!UICONTROL All Customers]**(으)로 이동합니다.

1. 테이블 머리글 메뉴에서 **[!UICONTROL Export]**&#x200B;을(를) 클릭하고 원하는 형식을 선택합니다.

   * CSV
   * Excel XML

1. **[!UICONTROL OK]**&#x200B;을(를) 클릭합니다.

   파일은 기본 다운로드 폴더로 이동합니다.

위의 지침은 모든 고객 계정을 내보냅니다. 제한된 세트를 내보내려면 내보낼 계정의 확인란을 선택하거나 컨트롤 패널에서 필터를 사용하여 고객 계정 범위를 선택합니다.

## 작업/제어

| 옵션 | 설명 |
|--- |--- |
| **[!UICONTROL Delete]** | 선택한 고객 계정을 삭제합니다. 고객 계정이 B2B 스토어의 회사 관리자에 속하는 경우 고객 계정을 삭제하려면 다른 회사 사용자를 관리자로 할당해야 합니다. |
| **[!UICONTROL Subscribe to Newsletter]** | 선택한 고객을 뉴스레터로 구독합니다. |
| **[!UICONTROL Unsubscribe from Newsletter]** | 뉴스레터에서 선택한 고객을 구독 취소합니다. |
| **[!UICONTROL Assign a Customer Group]** | 선택한 고객을 고객 그룹에 할당합니다. |
| **[!UICONTROL Edit]** | 선택한 단일 고객 레코드의 일부 값을 표에서 편집할 수 있습니다. 기본적으로 빠른 편집에 사용할 수 있는 값은 이메일, 그룹, 전화, 우편 번호, 웹 사이트, 세금 VAT 번호 및 성별입니다. |

{style="table-layout:auto"}

## 열

| 열 | 설명 |
|--- |--- |
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
| **[!UICONTROL Date of Birth]** | 고객의 생년월일. 현재 보안 및 개인 정보 보호 모범 사례를 준수하면서 다른 개인 식별자를 사용한 고객의 전체 생년월일(월, 일, 년) 저장과 관련된 잠재적 법적 및 보안 위험에 대해 알아두어야 합니다. 고객의 전체 생년월일 보관을 제한하고 고객 생년월일을 대안으로 사용하는 것이 좋습니다. |
| **[!UICONTROL Tax / VAT Number]** | 해당하는 경우 고객에게 할당된 세금 번호 또는 [부가가치세](../stores-purchase/vat.md) 번호입니다. <br/><br/> 이 필드는 VAT 번호와 다릅니다. |
| **[!UICONTROL Gender]** | 고객의 성별. |
| **[!UICONTROL Action]** | 편집 - 회사 계정을 편집 모드로 엽니다. |

{style="table-layout:auto"}

### 추가 열

이러한 열은 그리드의 [열 레이아웃](../getting-started/admin-grid-controls.md)을(를) 변경하여 사용할 수 있습니다.

| 열 | 설명 |
|--- |--- |
| **[!UICONTROL Company]** | 고객의 회사 이름입니다. |
| **[!UICONTROL Street Address]** | 고객의 거리 주소입니다. |
| **[!UICONTROL City]** | 고객이 위치한 도시입니다. |
| **[!UICONTROL Fax]** | 해당하는 경우 고객의 팩스 번호. |
| **[!UICONTROL Billing Firstname]** | 고객의 결제 주소에서 이름. |
| **[!UICONTROL Billing Lastname]** | 고객의 청구 주소의 성. |
| **[!UICONTROL Billing Address]** | 청구 정보를 보낼 주소. |
| **[!UICONTROL Shipping Address]** | 주문이 배송될 주소입니다. |
| **[!UICONTROL VAT Number]** | 고객 주소와 연결된 부가가치세 번호. EU에서 판매되는 [디지털 상품](../stores-purchase/taxes.md)의 경우 VAT는 고객의 청구 주소를 기준으로 합니다. <br/><br/> 이 필드는 세금/VAT 번호와 다릅니다. |
| **[!UICONTROL Account Lock]** | 계정의 상태를 나타냅니다. 너무 많은 로그인을 시도한 후 보안 조치로서 고객 계정이 [잠김](../customers/password-options.md)될 수 있습니다. 값: `Locked` / `Unlocked` |
| **[!UICONTROL Status]** | 현재 사용자 상태. 옵션: `Active` / `Inactive` |
| **[!UICONTROL Customer Type]** | 고객 분류. 옵션: `Individual user` / `Company admin` / `Company user` |
| **[!UICONTROL Sales Representative]** | 회사 계정의 연락 지점으로 할당되고 회사와 관련된 모든 자동 이메일 메시지를 받는 영업 담당자. |

{style="table-layout:auto"}
