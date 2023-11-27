---
title: 인보이스
description: 주문 처리 및 고객 서비스 작업을 지원하기 위해 송장을 만들고 인쇄하는 방법에 대해 알아봅니다.
exl-id: 6141b182-1467-4416-a07f-864333318428
feature: Invoices, Admin Workspace
source-git-commit: 8b5af316ab1d2e632ed5fc2066974326830ab3f7
workflow-type: tm+mt
source-wordcount: '1155'
ht-degree: 0%

---

# 인보이스

송장은 주문에 대한 지급 기록 레코드입니다. 여러 송장은 다음과 같을 수 있습니다. [생성됨](#create-an-invoice) 단일 주문의 경우, 각 주문에는 사용자가 지정하는 구매된 제품의 수만큼 또는 소수만큼 포함될 수 있습니다. 다음을 만들 수도 있습니다. [인쇄용 PDF 송장](#print-invoices) 고객을 위한 영업 문서로 사용됩니다.

다음에서 _관리자_ 사이드바, 이동 **[!UICONTROL Sales]** > _작업_ > **인보이스** 을(를) 열려면 _인보이스_ 그리드를 만들고 생성된 송장에 액세스합니다.

![인보이스 그리드](./assets/invoices.png){width="700" zoomable="yes"}

## 열 설명

| 열 | 설명 |
|--- |--- |
| [!UICONTROL Select] | 견적에 대한 확인란을 선택하여 작업에 적용하거나 열 머리글에서 선택 컨트롤을 사용합니다. 옵션: `Select All` / `Deselect All` |
| [!UICONTROL Invoice] | 관리자로부터 송장이 제출될 때 할당되는 고유 숫자 식별자입니다. 송장 상세내역을 볼 때 이 번호는 견적명 대신 페이지 상단에 나타납니다. |
| [!UICONTROL Invoice Date] | 관리자가 송장을 처음 제출한 날짜와 시간. |
| [!UICONTROL Order#] | 구매자가 주문을 할 때 할당되는 고유 숫자 식별자입니다. 송장 세부 정보를 볼 때 이 번호는 주문 및 계정 정보 블록에 링크로 표시됩니다. |
| [!UICONTROL Order Date] | 고객이 처음 주문한 날짜와 시간. |
| [!UICONTROL Bill-to Name] | 주문에 대한 결제 책임이 있는 사람의 이름. |
| [!UICONTROL Status] | 송장의 현재 상태를 나타냅니다. 매수인 또는 매도인 측의 행위에 의해서만 지위의 변경이 가능하다. |
| [!UICONTROL Grand Total (Base)] | 구매할 제품의 총 가격. 총 금액은 웹 사이트의 기본 통화 및 상점 통화로 표시됩니다. |
| [!UICONTROL Grand Total (purchase)] | 주문에서 구매한 제품의 총 합계입니다. 총 금액은 웹 사이트의 기본 통화 및 상점 통화로 표시됩니다. |
| [!UICONTROL Purchased From] | 송장이 생성된 웹 사이트/스토어/스토어 조회수. |
| [!UICONTROL Billing Address] | 주문한 고객의 청구 주소. |
| [!UICONTROL Shipping Address] | 주문이 배송될 주소입니다. |
| [!UICONTROL Customer Name] | 송장을 수령하는 고객의 이름과 성. |
| [!UICONTROL Email] | 송장을 받은 고객의 이메일 주소. |
| [!UICONTROL Customer Group] | 송장을 수령하는 고객에게 지정된 고객 그룹. |
| [!UICONTROL Payment Method] | 지급에 사용할 결제 방법. |
| [!UICONTROL Shipping Information] | 주문을 출하하는 데 사용할 방법입니다. |
| [!UICONTROL Subtotal] | 배송 및 취급 없이 주문 소계 및 세금. |
| [!UICONTROL Shipping and Handling] | 배송 및 처리에 대해 청구된 금액. |
| [!UICONTROL Action] | **[!UICONTROL View]** - 편집 모드로 송장을 엽니다. |

{style="table-layout:auto"}

## 송장 만들기

주문에 대한 송장을 생성하면 해당 주문을 취소하거나 변경할 수 없는 상태로 이동합니다. 새 송장 페이지는 일부 추가 필드가 있는 완료된 주문과 유사합니다. 주문과 관련된 모든 활동은 송장의 설명 섹션에 기재되어 있습니다.

일반적으로 주문은 배송 프로세스가 시작되면 송장이 발행되고 캡처됩니다. 결제 방법이 구매 발주이거나 [지불 조치](../configuration-reference/sales/payment-methods.md#payment-actions) 이(가) (으)로 설정됨 `Authorize and Capture`, 주문이 송장발행되고 결제가 체크아웃 중에 캡처됩니다. 포장 명세서가 있는 송장을 생성하고 운송업체 계정에서 운송 라벨을 인쇄할 수도 있습니다. 단일 주문은 부분 배송으로 나눌 수 있으며, 필요한 경우 별도로 청구됩니다.

새 주문 상태가 (으)로 설정된 경우 `Processing`, 옵션 _자동으로 모든 항목 송장 발행_ 를 구성에서 사용할 수 있습니다. 일부 신용카드 결제 방법은 다음의 경우 프로세스의 일부로 송장 발부 단계를 완료합니다. [지불 조치](../configuration-reference/sales/payment-methods.md#payment-actions) 이(가) (으)로 설정됨 `Authorize and Capture`. 이런 경우 송장 버튼이 나타나지 않고 주문이 배송될 준비가 된 것입니다.

>[!NOTE]
>
>송장은 다음을 사용하여 주문된 주문에 대해 자동으로 생성되지 않습니다. `Gift Card`, `Store Credit`, `Reward Points`또는 기타 오프라인 결제 방법을 사용할 수 있습니다.

주문에 대한 송장을 인쇄하려면 먼저 생성해야 합니다. PDF을 보거나 인쇄하려면 먼저 다음과 같은 PDF 리더를 다운로드하여 설치합니다. [Adobe Acrobat Reader][1].

**_주문의 송장을 발행하려면_**

1. 다음에서 _관리자_ 사이드바, 이동 **[!UICONTROL Sales]** > _[!UICONTROL Operations]_>**[!UICONTROL Orders]**.

1. 다음과 같은 상태의 판매 주문 찾기 `Processing` 그리드에서. 그런 다음 다음을 수행합니다.

1. 다음에서 _작업_ 열, 클릭 **[!UICONTROL View]**.

1. 판매 주문 헤더에서 다음을 선택합니다. **[!UICONTROL Invoice]** 옵션을 선택합니다.

   >[!NOTE]
   >
   >다음 _[!UICONTROL Invoice]_다음과 같은 경우에는 옵션이 표시되지 않습니다. [지불 조치](../configuration-reference/sales/payment-methods.md#payment-actions) 특정 [결제 방법](../configuration-reference/sales/payment-methods.md) 이(가) (으)로 설정됨 `Authorize and Capture`: 송장을 자동 생성합니다. 이는 주문을 하고 결제 방법에 대한 결제 작업을 로 설정한 경우에도 해당됩니다. `Authorize` 그리고 그 주문은 송장이 발행됩니다.

   ![송장 판매 주문](./assets/invoice-sales-order.png){width="700" zoomable="yes"}

   새 송장 페이지는 편집할 수 있는 추가 필드가 있는 완료된 주문 페이지와 유사합니다.

1. 품목이 출하될 준비가 되면 송장을 생성하는 동시에 선적에 대한 포장 명세서를 생성합니다.

   - 다음에서 _배송 정보_ 섹션에서 **[!UICONTROL Create Shipment]** 확인란을 선택하여 선택합니다.

     송장이 생성됨과 동시에 선적 레코드가 생성됩니다.

   - 추적 번호 포함:

      - 클릭 **[!UICONTROL Add Tracking Number]**.
      - 추적 정보 입력: _[!UICONTROL Carrier]_,_[!UICONTROL Title]_, 및 _[!UICONTROL Number]_

     ![Fedex 배송 만들기](./assets/invoice-create-shipment-fedex.png){width="600" zoomable="yes"}

   - 부분 송장을 생성합니다(선택적).

      - 다음에서 _송장 기재 항목_ 섹션, 업데이트 **[!UICONTROL Qty to Invoice]** 송장의 특정 항목만 포함하는 열.
      - 그런 다음 을 클릭합니다. **[!UICONTROL Update Qty's]**.

        ![송장 기재 항목](./assets/invoice-items-to-invoice.png){width="600" zoomable="yes"}

1. 온라인 결제 방법이 주문에 사용된 경우 다음을 설정합니다. **[!UICONTROL Amount]** 적절한 옵션을 선택합니다.

1. 송장이 생성될 때 이메일로 고객에게 알리려면 다음을 수행합니다.

   - 다음 항목 선택 **[!UICONTROL Email Copy of Invoice]** 확인란.

   - 원하는 항목 입력 **[!UICONTROL Invoice Comments]**. 알림 이메일에 설명을 포함하려면 다음을 표시하십시오. **[!UICONTROL Append Comments]** 확인란.

1. 완료되면 다음을 클릭하십시오. **[!UICONTROL Submit Invoice]** 페이지 하단에 있습니다.

   **_온라인 결제 방법:_**

   ![송장 실행 - 온라인 결제 방법](./assets/invoice-submit-invoice-capture-online.png){width="600" zoomable="yes"}

   **_오프라인 결제 방법:_**

   ![송장 실행 - 오프라인 결제 방법)](./assets/invoice-submit-invoice.png){width="600" zoomable="yes"}

   주문 상태가 다음에서 변경됨: `Pending` 끝 `Complete`.

   ![완료된 송장 요약](./assets/invoice-complete.png){width="600" zoomable="yes"}

## 인보이스 인쇄

송장은 개별적으로 또는 배치로 인쇄할 수 있습니다. 그러나 송장을 인쇄하려면 먼저 주문에 대해 송장을 생성해야 합니다. 인쇄용 PDF 송장에 고해상도 로고를 업로드하고 다음을 포함할 수 있습니다. [주문 ID](../stores-purchase/sales-documents.md#add-reference-ids) 헤더에서. 로고 및 주소로 송장 템플릿을 사용자 정의하려면 다음을 참조하십시오. [PDF 로고 요구 사항](../stores-purchase/sales-documents.md#image-formats).

>[!NOTE]
>
>PDF을 보거나 인쇄하려면 PDF 판독기가 있어야 합니다. 다음을 다운로드할 수 있습니다. [Adobe Reader][1] 무료로.

### 단일 청구서 인쇄

1. 다음에서 _관리자_ 사이드바, 이동 **[!UICONTROL Sales]** > _[!UICONTROL Operations]_>**[!UICONTROL Invoices]**.

1. 다음에서 _[!UICONTROL Invoices]_그리드에서 송장을 찾은 다음&#x200B;**[!UICONTROL View]**다음에서_&#x200B;작업&#x200B;_열.

1. 송장의 맨 위에서 **[!UICONTROL Print]** 송장의 PDF을 생성합니다.

1. 생성된 PDF을 파일에 저장하거나 인쇄합니다.

### 여러 송장 인쇄

1. 다음에서 _관리자_ 사이드바, 이동 **[!UICONTROL Sales]** > _[!UICONTROL Operations]_>**[!UICONTROL Invoices]**.

1. 다음에서 _[!UICONTROL Invoices]_그리드에서 인쇄할 각 송장의 체크박스를 선택합니다.

1. 설정 **[!UICONTROL Actions]** 제어 대상 `PDF Invoices`.

   ![여러 송장 인쇄](./assets/invoices-print-batch.png){width="600" zoomable="yes"}

인보이스는 프린터로 보내거나 저장할 수 있는 단일 PDF 파일에 저장됩니다.

## 리소스 문제 해결

송장 문제 해결에 대한 도움말은 다음을 참조하십시오. _Commerce 지원 기술 자료_ 문서:

- [가상 및 간단한 번들 제품에 대해 송장을 발행할 수 없음](https://experienceleague.adobe.com/docs/commerce-knowledge-base/kb/support-tools/patches/v1-0-9/mdva-30889-magento-patch-can-t-invoice-bundle-products-virtual-and-simple.html)
- [스토어 신용 정보가 없는 송장](https://experienceleague.adobe.com/docs/commerce-knowledge-base/kb/support-tools/patches/v1-0-8/mdva-31150-magento-patch-invoice-without-store-credit-info.html)
- [세금이 100% 할인된 송장에 표시됨](https://experienceleague.adobe.com/docs/commerce-knowledge-base/kb/support-tools/patches/v1-0-22/mdva-35773-tax-appears-on-invoice-with-100-discount.html)
- [주문 송장이 자동으로 전송되지 않음](https://experienceleague.adobe.com/docs/commerce-knowledge-base/kb/support-tools/patches/v1-0-13/mdva-32545-magento-patch-order-invoices-don-t-send-automatically.html)


[1]: https://www.adobe.com/acrobat/pdf-reader.html "Adobe Reader 가져오기"
