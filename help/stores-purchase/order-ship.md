---
title: 주문 배송
description: 처리 주문에 대한 배송 정보를 완료하고 배송 및 추적 정보를 조회하는 방법에 대해 알아봅니다.
exl-id: 60b0e66a-8ee6-4091-94ce-179cc2fdf57a
feature: Orders, Shipping/Delivery
source-git-commit: 8b5af316ab1d2e632ed5fc2066974326830ab3f7
workflow-type: tm+mt
source-wordcount: '450'
ht-degree: 0%

---

# 주문 배송

이미 지불되었지만 배송 대기 중인 주문의 상태는 `Processing`입니다. 출하 레코드에는 해당 주문과 연관된 이행 프로세스의 상세 내역이 포함됩니다. 주문이 이행될 때까지 부분 선적을 할 수 있습니다.

1. _관리자_ 사이드바에서 **[!UICONTROL Sales]** > **[!UICONTROL Orders]**&#x200B;을(를) 선택합니다.

1. _[!UICONTROL Orders]_목록에서 배송할 주문을 찾은 다음 클릭하여 엽니다.

1. 오른쪽 상단에서 **[!UICONTROL Ship]** 단추를 클릭합니다.

1. 청구 또는 배송 주소를 업데이트하려면 섹션의 오른쪽 상단에 있는 **[!UICONTROL Edit]** 링크를 클릭하십시오.

   필요한 사항을 변경하고 **[!UICONTROL Save Order Address]**&#x200B;을(를) 클릭합니다.

1. 통신사가 배송 레이블을 생성하려면 **[!UICONTROL Create Shipping Label]** 확인란을 선택하고 옵션을 설정합니다.

   - 추적 번호를 추가하려면 _[!UICONTROL Shipping Information]_섹션까지 아래로 스크롤한 다음&#x200B;**[!UICONTROL Add Tracking Number]**을(를) 클릭합니다.

   - 다음 중 하나를 수행합니다.

      - **[!UICONTROL Carrier]**&#x200B;을(를) 선택하고 추적 **[!UICONTROL Number]**&#x200B;을(를) 입력하십시오.

      - **[!UICONTROL Carrier]**&#x200B;을(를) `Custom Value`(으)로 설정하고 사용자 지정 통신사에 대한 **[!UICONTROL Title]**&#x200B;을(를) 입력한 다음 추적 **[!UICONTROL Number]**&#x200B;을(를) 입력하십시오.

      - [추적 정보 보기](#track-the-shipment).

1. 부분 선적을 하려면 Items to Ship 섹션으로 스크롤한 후 각 항목에 대해 **[!UICONTROL Qty to Ship]**&#x200B;을(를) 입력하십시오.

1. 고객에게 발송을 이메일로 알리려면 다음을 수행합니다.

   - **[!UICONTROL Shipment Comments]** 상자에 포함할 주석을 입력하십시오.

   - 고객에게 보낸 알림 전자 메일에 설명을 포함하려면 **[!UICONTROL Append Comments]** 확인란을 선택하세요.

   - 배달 전자 메일의 복사본을 직접 보내려면 **[!UICONTROL Email Copy of Shipment]** 확인란을 선택하세요.

     송장 전자 메일의 상태가 발송됨 또는 발송되지 않음으로 완료된 송장의 송장 번호 옆에 나타납니다.

1. 완료되면 **[!UICONTROL Submit Shipment]**&#x200B;을(를) 클릭합니다.

   주문 상태가 `Processing`에서 `Complete`(으)로 변경됩니다.

>[!NOTE]
>
>주문이 &#39;매장 배송&#39;으로 이루어진 경우 배송 옵션을 사용할 수 없습니다. 고객에게 전자 메일을 트리거하려면 **[!UICONTROL Notify Order is Ready for Pickup]**&#x200B;을(를) 클릭하십시오. 그러면 주문 상태가 `Complete`(으)로 변경됩니다.

## 배송 세부 사항 보기

1. _관리자_ 사이드바에서 **[!UICONTROL Sales]** > **[!UICONTROL Shipments]**(으)로 이동합니다.

1. 목록에서 납품을 찾은 다음 를 클릭하여 레코드를 엽니다.

1. 주문에 주석을 추가하려면 _[!UICONTROL Comments History]_섹션까지 아래로 스크롤한 다음 상자에 설명을 입력하십시오.

   - 고객에게 전자 메일로 댓글을 보내려면 **[!UICONTROL Notify Customer by Email]** 확인란을 선택하십시오.

   - 고객 계정에 댓글을 게시하려면 **[!UICONTROL Visible on Frontend]** 확인란을 선택하십시오.

1. **[!UICONTROL Submit Comment]**&#x200B;을(를) 클릭합니다.

## 배송 추적

주문 정보 탭의 **메서드 1:**

1. _관리자_ 사이드바에서 **[!UICONTROL Sales]** > **[!UICONTROL Orders]**(으)로 이동합니다.

1. 그리드에서 배달 주문을 찾은 다음 **[!UICONTROL View]**&#x200B;을(를) 클릭합니다.

1. _[!UICONTROL Shipping & Handling Information]_섹션까지 아래로 스크롤한 다음&#x200B;**[!UICONTROL Track Order]**을(를) 클릭합니다.

   사용 가능한 모든 추적 정보가 팝업 창에 나타납니다.

1. 준비가 되면 **[!UICONTROL Close Window]**&#x200B;을(를) 클릭합니다.

주문 배송 탭의 **방법 2:**

1. _관리자_ 사이드바에서 **[!UICONTROL Sales]** > **[!UICONTROL Shipments]**(으)로 이동합니다.

1. 목록에서 납품을 찾은 다음 를 클릭하여 레코드를 엽니다.

1. **[!UICONTROL Track this Shipment]**&#x200B;을(를) 클릭합니다.

   사용 가능한 모든 추적 정보가 팝업 창에 나타납니다.

1. 준비가 되면 **[!UICONTROL Close Window]**&#x200B;을(를) 클릭합니다.
