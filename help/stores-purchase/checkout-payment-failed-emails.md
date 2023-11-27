---
title: 결제 실패 알림
description: 거래를 완료하지 못한 결제 방법을 위한 이메일 통신을 구성하는 방법에 대해 알아봅니다.
exl-id: c64a4463-64d5-4dad-a8ad-13bfb141b65f
feature: Payments, Communications
source-git-commit: 8b5af316ab1d2e632ed5fc2066974326830ab3f7
workflow-type: tm+mt
source-wordcount: '233'
ht-degree: 0%

---

# 결제 실패 알림

체크아웃 중에 선택한 결제 방법이 트랜잭션을 완료하지 못할 경우 스토어 연락처 또는 지정된 관리자 사용자에게 알림이 전송됩니다.

## 1단계: 이메일 템플릿 업데이트

브랜드를 반영하도록 필요한 이메일 템플릿을 업데이트했는지 확인하십시오. 전체 템플릿 목록은 다음을 참조하십시오. [이메일 템플릿 목록](../systems/email-templates.md#email-template-list).

## 2단계: 결제 실패 이메일 구성

1. 다음에서 _관리자_ 사이드바, 이동 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. 왼쪽 패널에서 를 확장합니다. **[!UICONTROL Sales]** 및 선택 **[!UICONTROL Checkout]**.

1. 확장 ![확장 선택기](../assets/icon-display-expand.png) 다음 **[!UICONTROL Payment Failed Emails]** 섹션.

   ![결제 실패 이메일](../configuration-reference/sales/assets/checkout-payment-failed-emails.png){width="600" zoomable="yes"}

1. 결제가 실패한 이메일에 대한 옵션을 설정합니다.

   - 설정 **[!UICONTROL Payment Failed Email Sender]** 메시지를 보낸 사람으로 표시되는 스토어 연락처입니다.
   - 설정 **[!UICONTROL Payment Failed Email Receiver]** 이메일 전송 실패에 대한 알림을 받을 스토어 연락처로 보냅니다.
   - 설정 **[!UICONTROL Payment Failed Template]** 체크아웃하는 동안 결제 방법이 실패할 때 보내는 이메일에 사용되는 템플릿입니다.

1. 대상 **[!UICONTROL Send Payment Failed Email Copy To]**&#x200B;에 결제 실패 알림의 사본을 받을 사용자의 이메일 주소를 입력합니다.

   여러 수신자에게 복사본을 보내는 경우 각 주소는 쉼표로 구분하십시오.

1. 설정 **[!UICONTROL Payment Failed Copy Method]** 다음 중 하나를 수행합니다.

   - `Bcc` - 을(를) 보냅니다. _무차별적 복사_ 고객에게 전송된 동일한 이메일의 헤더에 수신자를 포함하여. BCC 수신자는 고객에게 표시되지 않습니다.
   - `Separate Email` - 사본을 별도의 이메일로 전송합니다.

1. 클릭 **[!UICONTROL Save Config]**.
