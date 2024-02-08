---
title: 구매자에 대한 견적 시작
description: 판매자가 협상 프로세스를 시작하기 위해 특정 구매자에 대한 견적을 생성하는 방법에 대해 알아봅니다. 판매자는 선택한 웹 사이트에서 회사 계정과 연계된 고객에 대해서만 견적을 제출할 수 있습니다.
exl-id: 7bbb281f-7b6a-45fa-b906-da314d159bc8
feature: B2B, Quotes
role: Admin, User
source-git-commit: 8130ccb809a6aec80db63c5a6ea9f47488248805
workflow-type: tm+mt
source-wordcount: '700'
ht-degree: 0%

---

# 구매자에 대한 견적 시작

다음에서 인용 부호가 활성화된 경우: [영업 기능 구성](configure-quotes.md), 영업 사원은 관리자로부터 견적을 생성하여 회사 구매자와 협상 프로세스를 시작할 수 있습니다.

- 초안 견적은 판매자에게만 표시됩니다.
- 구매자를 위한 초기 오퍼를 생성할 수 있도록 영업 담당자가 품목, 관련 할인 및 메모를 추가할 때까지 초안 견적을 제출할 수 없습니다.
- 판매자는 Quotes 또는 Customer Grid에서 Quote 를 생성할 수 있습니다.

영업 사원은 구매자에게 견적을 전송하여 협상 프로세스를 시작합니다. 다음을 참조하십시오 [견적 협상](quote-price-negotiation.md).

## 영업 담당자 견적 생성 경험

Sales Rep 는 Quote 또는 Customer Grid에서 Quote 를 생성할 수 있습니다.

>[!NOTE]
>
>판매자가 구매자를 위한 견적을 작성하는 비디오 데모는 다음을 참조하십시오. [영업 담당자가 견적 시작](https://experienceleague.adobe.com/docs/commerce-learn/tutorials/b2b/b2b-quote/sales-rep-initiates-quote.html) 위치: _Commerce 비디오 및 Tutorials_.

### Quote 그리드에서 Quote 작성

1. 영업 담당자는 를 사용하여 관리자로 관리자에 로그인합니다. [Sales Operations 권한](../systems/permissions.md) 견적을 관리합니다.

1. 관리자에서 [!UICONTROL Quotes] 다음을 선택하여 격자 표시 **[!UICONTROL Sales]**&#x200B;을 선택한 다음 을 선택합니다 **[!UICONTROL Quotes]**.

1. 구매자를 위한 견적을 생성합니다.

   - Quotes 그리드에서 **[!UICONTROL Create New Quote]**.

     ![판매자가 관리자의 구매자 견적을 시작하는 중](./assets/quote-draft-from-admin.png){width="700" zoomable="yes"}

   - 다음에서 [!UICONTROL Create New Quote] 페이지에서 고객(회사 구매자)을 선택하여 견적을 생성합니다.

     ![새 견적에 대한 고객 선택](./assets/quote-draft-from-admin-select-buyer.png){width="700" zoomable="yes"}

     새 견적이 다음에 표시됩니다. `Draft` 상태.

     ![판매자가 만든 새 초안 견적](./assets/quote-create-by-seller.png){width="700" zoomable="yes"}

   - 견적명을 업데이트하고 필요에 따라 만료 날짜를 수정합니다.

   - 견적을 초안으로 저장합니다.

## 구매자를 위한 견적 준비

초안 견적을 작성한 후 견적에 주석 및 관련 파일을 추가하여 제품 품목을 추가하고 할인을 적용하고 구매자와 소통합니다. 그런 다음 구매자에게 견적을 보내 검토하거나 초안으로 저장합니다.

1. 을(를) 선택하여 견적에 항목 추가 **[!UICONTROL Add Product By SKU]**. SKU 번호와 수량을 입력한 다음 을(를) 선택합니다. **[!UICONTROL Add Product]**.

   ![판매자가 구매자를 위한 초안 견적에 항목 추가](./assets/quote-draft-add-items.png){width="675" zoomable="yes"}

1. 필요에 따라 제품에 라인 항목 할인을 적용합니다.

   - 다음에서 [!UICONTROL Select] 작업 메뉴, 선택 **[!UICONTROL Discount Item]**.

   - 다음에서 [!UICONTROL Discount Line item] 양식을 선택하고 **[!UICONTROL Discount Type]**.

     ![견적에 라인 항목 할인 적용](./assets/quote-discount-line-item.png){width="675" zoomable="yes"}

   - 다음에서 [!UICONTROL Discount] 필드에 할인 유형의 값을 입력합니다. 예를 들어 퍼센트 할인을 선택한 경우 10을 입력하여 라인 품목에 10% 할인을 적용합니다.

   - [!BADGE 1.5.0 베타 기능]{type=Informative url="/help/b2b/release-notes.md" tooltip="Beta 프로그램 참가자만 사용 가능"}

     변경을 확인한 후 제품 격자의 라인 항목 속성이 업데이트되어 적용된 할인 금액이 표시됩니다. 할인이 잠기면 잠금 아이콘이 표시됩니다.

1. 필요에 따라 견적 수준 할인 적용:

   - 다음에서 [!UICONTROL Quote Totals - Negotiated Price] 섹션에서 할인 유형을 선택한 다음 적용할 값을 입력합니다.

     ![판매자가 견적 수준 할인을 추가합니다.](./assets/quote-draft-total-discount.png){width="700" zoomable="yes"}

   제품 격자가 업데이트되어 할인이 표시됩니다.

1. 구매자를 위한 추가 정보를 추가합니다.

   다음에서 **[!UICONTROL Negotiation - Comments]** 탭에서 메모를 추가하고 구매자에게 필요한 지원 파일을 첨부합니다.

   ![판매자가 구매자를 위한 정보를 추가합니다.](./assets/quote-draft-add-info-for-buyer.png){width="700" zoomable="yes"}

   기본적으로 [첨부 파일](configure-quotes.md) 최대 2MB의 파일 포맷(DOC, DOCX, XLS, XLSX, PDF, TXT, JPG 또는 JPEG, PNG).

1. 견적을 처리합니다.

   견적을 초안으로 저장하거나 구매자에게 전송합니다.

   - 견적을 초안으로 저장하면 상태가 다음으로 갱신됩니다. `Draft` 확인 메시지가 표시됩니다.

   - 구매자에게 견적을 발송하면 상태가 다음으로 변경됩니다. `Submitted`. 구매자는 견적을 검토하기 위해 이메일 알림을 받습니다. 구매자가 추가 협상을 위해 견적을 반환할 때까지 견적이 잠깁니다. 판매자는 Quote 표 또는 Customer 표에서 Quote 를 볼 수 있습니다.

## 고객 그리드에서 견적 조회 및 생성

1. 관리자에서 [!UICONTROL Customer] 다음을 선택하여 격자 표시 **[!UICONTROL Customers]**&#x200B;을 선택한 다음 을 선택합니다 **[!UICONTROL All Customers]**.

1. 회사 구매자의 고객 ID를 선택합니다.

   ![구매자에게 제출된 확인 초안 견적](./assets/quote-view-customer-quotes.png){width="700" zoomable="yes"}

1. 선택 **[!UICONTROL Edit]** 고객 정보를 조회합니다.

1. 다음을 선택하여 고객에 대한 견적을 생성합니다. **[!UICONTROL Create Quote]** 초안 견적을 업데이트하고 고객에게 보내는 프로세스를 따릅니다.

1. 를 선택하여 고객의 기존 견적을 확인합니다. **[!UICONTROL Quotes]**.

   ![구매자에게 제출된 확인 초안 견적](./assets/quote-list-from-customer-information.png){width="700" zoomable="yes"}

1. 다음을 선택하여 견적 열기 **[!UICONTROL View]**.

견적 협상 프로세스 관리에 대한 자세한 내용은 [견적 협상](quote-price-negotiation.md)
