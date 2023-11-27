---
title: 주문 배송
description: 처리 주문에 대한 배송 정보를 완료하고 배송 및 추적 정보를 조회하는 방법에 대해 알아봅니다.
exl-id: 60b0e66a-8ee6-4091-94ce-179cc2fdf57a
feature: Orders, Shipping/Delivery
source-git-commit: 8b5af316ab1d2e632ed5fc2066974326830ab3f7
workflow-type: tm+mt
source-wordcount: '448'
ht-degree: 0%

---

# 주문 배송

지불되었지만 배송 대기 중인 주문은 `Processing` 상태. 출하 레코드에는 해당 주문과 연관된 이행 프로세스의 상세 내역이 포함됩니다. 주문이 이행될 때까지 부분 선적을 할 수 있습니다.

1. 다음에서 _관리자_ 사이드바, 선택 **[!UICONTROL Sales]** > **[!UICONTROL Orders]**.

1. 다음에서 _[!UICONTROL Orders]_목록에서 출하할 주문을 찾은 다음 을(를) 클릭하여 엽니다.

1. 오른쪽 위 모서리에서 **[!UICONTROL Ship]** 단추를 클릭합니다.

1. 청구 또는 배송 주소를 업데이트하려면 다음을 클릭하십시오. **[!UICONTROL Edit]** 섹션의 오른쪽 상단에 있는 링크.

   필요한 사항을 변경한 다음 **[!UICONTROL Save Order Address]**.

1. 운송업체가 운송 레이블을 생성하게 하려면 다음을 선택합니다. **[!UICONTROL Create Shipping Label]** 확인란을 선택하고 옵션을 설정합니다.

   - 추적 번호를 추가하려면 아래로 스크롤합니다 _[!UICONTROL Shipping Information]_섹션, 클릭&#x200B;**[!UICONTROL Add Tracking Number]**.

   - 다음 중 하나를 수행합니다.

      - 다음 항목 선택 **[!UICONTROL Carrier]** 및 추적 입력 **[!UICONTROL Number]**.

      - 설정 **[!UICONTROL Carrier]** 끝 `Custom Value`, 를 입력합니다. **[!UICONTROL Title]** 사용자 지정 통신사에 대해 추적을 입력합니다. **[!UICONTROL Number]**.

      - [추적 정보 보기](#track-the-shipment).

1. 부분 선적을 하려면 납품할 품목 섹션까지 아래로 스크롤한 다음 **[!UICONTROL Qty to Ship]** 각 항목에 대해.

1. 고객에게 발송을 이메일로 알리려면 다음을 수행합니다.

   - 에 포함할 주석을 입력하십시오. **[!UICONTROL Shipment Comments]** 상자.

   - 고객에게 전송된 알림 이메일에 설명을 포함하려면 **[!UICONTROL Append Comments]** 확인란.

   - 배송 전자 메일의 복사본을 자신에게 보내려면 다음을 선택합니다. **[!UICONTROL Email Copy of Shipment]** 확인란.

     송장 전자 메일의 상태가 발송됨 또는 발송되지 않음으로 완료된 송장의 송장 번호 옆에 나타납니다.

1. 완료되면 다음을 클릭하십시오. **[!UICONTROL Submit Shipment]**.

   주문 상태가 다음에서 변경됨: `Processing` 끝 `Complete`.

>[!NOTE]
>
>주문이 &#39;매장 배송&#39;으로 이루어진 경우 배송 옵션을 사용할 수 없습니다. 클릭 **[!UICONTROL Notify Order is Ready for Pickup]** (으)로 이메일을 보냅니다. 그런 다음 주문 상태가 (으)로 변경됩니다. `Complete`.

## 배송 세부 사항 보기

1. 다음에서 _관리자_ 사이드바, 이동 **[!UICONTROL Sales]** > **[!UICONTROL Shipments]**.

1. 목록에서 납품을 찾은 다음 를 클릭하여 레코드를 엽니다.

1. 주문에 주석을 추가하려면 아래로 스크롤합니다. _[!UICONTROL Comments History]_섹션에 설명을 입력하고 상자에 설명을 입력합니다.

   - 고객에게 전자 메일로 댓글을 보내려면 **[!UICONTROL Notify Customer by Email]** 확인란.

   - 고객 계정에 댓글을 게시하려면 **[!UICONTROL Visible on Frontend]** 확인란.

1. 클릭 **[!UICONTROL Submit Comment]**.

## 배송 추적

**방법 1:** 주문 정보 탭에서

1. 다음에서 _관리자_ 사이드바, 이동 **[!UICONTROL Sales]** > **[!UICONTROL Orders]**.

1. 그리드에서 납품 주문을 찾은 다음 **[!UICONTROL View]**.

1. 아래로 스크롤하여 _[!UICONTROL Shipping & Handling Information]_섹션 및 클릭&#x200B;**[!UICONTROL Track Order]**.

   사용 가능한 모든 추적 정보가 팝업 창에 나타납니다.

1. 준비가 되면 다음을 클릭합니다. **[!UICONTROL Close Window]**.

**방법 2:** 주문 납품 탭에서

1. 다음에서 _관리자_ 사이드바, 이동 **[!UICONTROL Sales]** > **[!UICONTROL Shipments]**.

1. 목록에서 납품을 찾은 다음 를 클릭하여 레코드를 엽니다.

1. 클릭 **[!UICONTROL Track this Shipment]**.

   사용 가능한 모든 추적 정보가 팝업 창에 나타납니다.

1. 준비가 되면 다음을 클릭합니다. **[!UICONTROL Close Window]**.
