---
title: 페덱스
description: FedEx를 스토어 배송업체로 설정하는 방법을 알아보십시오.
exl-id: 75bb3ed1-3ae9-418a-be90-888046b28a7b
feature: Shipping/Delivery
source-git-commit: ad5da1d77b63bf6bcc0227a5c467e369b7bb8d89
workflow-type: tm+mt
source-wordcount: '899'
ht-degree: 0%

---

# 페덱스

FedEx는 세계 최대의 운송 서비스 회사 중 하나로, 여러 수준의 우선 순위로 항공, 화물 및 육로 운송 서비스를 제공합니다.

![결제 시 FedEx 발송 옵션](./assets/storefront-checkout-shipping-fedex.png){width="700" zoomable="yes"}

>[!NOTE]
>
>FedEx는 [차원 가중치](carriers.md#dimensional-weight)를 사용하여 일부 배송 속도를 결정할 수 있습니다. 단, Adobe Commerce 및 Magento Open Source은 중량 기준 배송비 계산만 지원합니다.

## 1단계: FedEx 웹 서비스 프로덕션에 등록

FedEx Web Services Production Access에 대한 FedEx 판매자 계정 및 등록이 필요합니다. FedEx 계정을 만든 후 프로덕션 계정 정보 페이지를 읽은 다음 페이지 하단의 _프로덕션 키 가져오기_ 링크를 클릭하여 등록하고 키를 가져옵니다.

>[!NOTE]
>
>인증 키를 복사하거나 기록해야 합니다. Commerce 배송 설정에서 Fedex를 설정해야 합니다.

## 2단계: 스토어에서 FedEx 활성화

1. 관리자 사이드바에서 > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**로 이동합니다&#x200B;**[!UICONTROL Stores]**._ _

1. 왼쪽 패널에서 을 확장 **[!UICONTROL Sales]** 하고 을 선택합니다 **[!UICONTROL Delivery Methods]**.

1. **[!UICONTROL FedEx]** 섹션에서 ![확장 선택기](../assets/icon-display-expand.png)를 확장합니다.

1. **[!UICONTROL Enabled for Checkout]**&#x200B;을(를) `Yes`(으)로 설정합니다.

1. 에 **[!UICONTROL Title]**&#x200B;결제 시 FedEx 발송 방법을 나타내는 제목을 입력합니다.

1. FedEx 계정 계정에서 다음 정보를 입력합니다.

   - **[!UICONTROL Account ID]**
   - **[!UICONTROL Api Key]**
   - **[!UICONTROL Secret Key]**

1. 별도의 추적 API 자격 증명이 있는 경우 다음 구성을 활성화합니다.

   - **[!UICONTROL Enable Tracking API credentials]**

1. FedEx 계정 계정에서 다음 정보를 입력합니다.

   - **[!UICONTROL Tracking API Key]**
   - **[!UICONTROL Tracking API Secret Key]**

1. FedEx 샌드박스를 설정했으며 테스트 환경에서 작업하려면 으로 설정합니다 **[!UICONTROL Sandbox Mode]** `Yes`.

   >[!NOTE]
   >
   >샌드박스 모드를 `No` FedEx를 고객에게 배송 방법으로 제공할 준비가 되면 설정해야 합니다.

   ![FedEx 계정 설정](../configuration-reference/sales/assets/delivery-methods-fedex-account-settings.png){width="600" zoomable="yes"}

## 3단계: 패키지 설명 및 취급 수수료

1. 배송에 사용되는 픽업 방법으로 설정합니다 **[!UICONTROL Pickup Type]** .

   - `DropOff at Fedex Location` - (기본값) 현지 FedEx 사무소에서 발송물을 감소 함을 나타냅니다.
   - `Contact Fedex to Schedule` - 픽업을 요청 위해 FedEx에 연락했음을 나타냅니다.
   - `Use Scheduled Pickup` - 예약된 정기 픽업의 일부로 배송이 픽업되었음을 나타냅니다.
   - `On Call` - FedEx를 호출하여 픽업이 예약되었음을 나타냅니다.
   - `Package Return Program` - FedEx Ground Package Returns Program에서 선적을 선택함을 나타냅니다.
   - `Regular Stop` - 정기 픽업 일정에 따라 선적이 픽업됨을 나타냅니다.
   - `Tag` - 배송 픽업이 Express 태그 또는 Ground Call 태그 픽업 요청에만 해당됨을 나타냅니다. 이는 반송 레이블에만 적용됩니다.

1. 의 경우 **[!UICONTROL Packages Request Type]**&#x200B;주문을 여러 배송으로 분할할 때 기본 설정을 가장 잘 설명하는 요청 유형을 선택합니다.

   - `Divide to equal weight (one request)`
   - `Use origin weight (few requests)`

1. 의 경우 **[!UICONTROL Packaging]**&#x200B;스토어 발송에 일반적으로 사용하는 FedEx 포장 유형을 선택합니다.

1. **[!UICONTROL Weight Unit]**&#x200B;을(를) 로케일에서 사용되는 측정 단위로 설정합니다.

   - `Pounds`
   - `Kilograms`

1. FedEx 배송에 대해 허용되는 **[!UICONTROL Maximum Package Weight]**&#x200B;을(를) 입력하십시오.

   기본 FedEx 최대 중량은 150파운드입니다. 자세한 내용은 배송 담당자에게 문의하십시오. FedEx와 특별히 합의한 경우가 아니면 기본값이 권장됩니다. 자세한 내용은 용적 중량](carriers.md#dimensional-weight)을 참조하십시오[.

   ![FedEx 패키지 설정](../configuration-reference/sales/assets/delivery-methods-fedex-packaging.png){width="600" zoomable="yes"}

1. 요건에 따라 취급 수수료 옵션을 구성합니다.

   취급 수수료는 선택 사항이며 결제 시 표시되지 않습니다. 취급 수수료를 포함하려면 다음을 수행합니다.

   - 세트 **[!UICONTROL Calculate Handling Fee]**:

      - `Fixed Fee`
      - `Percentage`

   - **[!UICONTROL Handling Applied]**&#x200B;의 경우 다음 처리 수수료 관리 방법 중 하나를 선택하십시오.

      - `Per Order`
      - `Per Package`

   - **[!UICONTROL Handling Fee]** `fixed` 계산 방법에 따라 금액 또는 `percentage`으로 입력합니다.

1. B2C(비즈니스-to-Consumer) 또는 B2B(비즈니스-to-비즈니스) 여부에 따라 다음 중 하나로 설정합니다 **[!UICONTROL Residential Delivery]** .

   - `Yes` - B2C 주거용 배송용.
   - `No` - B2B 주거용 배송용.

   ![FedEx 취급 수수료 설정](../configuration-reference/sales/assets/delivery-methods-fedex-handling-fee.png){width="600" zoomable="yes"}

## 4단계: 허용되는 방법 및 적용 가능한 국가

1. 제공하려는 각 배송 방법으로 설정합니다 **[!UICONTROL Allowed Methods]** .

   방법을 선택할 때 FedEx 계정, 발송물의 빈도 및 크기, 국제 발송 허용 여부를 고려하십시오. 다음과 같이 원하는 만큼 또는 적은 수의 메서드를 제공할 수 있습니다.

   - 유럽 우선 순위
   - 납품 일자 옵션: 1일 운송비, 2일 운송비, 2일 AM, 2일 운송비
   - 국내 옵션 – Express Saver, Ground, First, Overnight, Home Delivery, Standard Overnight
   - 국제 옵션–국제 경제, 국제 이코노미 화물, 국제 우선, 국제 지상, 국제, 우선 순위 국제
   - 우선순위 옵션 - 화물, Priority Overnight
   - Smart Post – Smart Post 방법을 제공하는 경우(허브 ID **입력**)
   - 화물 옵션 – 화물, 전국 화물

1. FedEx를 통해 [무료 배송](shipping-free.md) 옵션을 제공하려면 무료 배송 옵션을 설정하십시오.

   - 무료 배송에 사용할 방법으로 설정합니다 **[!UICONTROL Free Method]** . FedEx를 통해 무료 배송을 제공하지 않으려면 `None`을(를) 선택하세요.

   - FedEx를 통한 무료 발송 주문에 적합한 최소 주문 금액을 요구하려면 로 설정합니다 **[!UICONTROL Enable Free Shipping Threshold]** `Enable`. 그런 다음 에 최소값을 **[!UICONTROL Free Shipping Amount Threshold]**&#x200B;입력합니다.

   이 설정은 표준 무료 배송 방법의 설정과 유사하지만 결제 시 FedEx 섹션에 표시되므로 고객은 주문에 어떤 방법이 사용되는지 알 수 있습니다.

1. 필요한 경우 **[!UICONTROL Displayed Error Message]**.

   이 텍스트 상자는 기본 메시지로 사전 설정되어 있지만 FedEx를 사용할 수 없는 경우 표시할 다른 메시지를 입력할 수 있습니다.

   ![FedEx 허용 게재 메서드](../configuration-reference/sales/assets/delivery-methods-fedex-delivery-methods.png){width="600" zoomable="yes"}

1. **[!UICONTROL Ship to Applicable Countries]** 설정:

   - `All Allowed Countries` - 스토어 구성에 지정된 모든 [국가](../getting-started/store-details.md#country-options)의 고객이 이 게재 방법을 사용할 수 있습니다.

   - `Specific Countries` - 이 옵션을 선택하면 _특정 국가로 배송_ 목록이 나타납니다. 목록에서 이 게재 방법을 사용할 수 있는 각 국가를 선택합니다.

1. 스토어 스토어와 FedEx 시스템 간의 모든 통신 로그를 보관하려면 로 설정합니다 **[!UICONTROL Debug]** `Yes`.

1. 세트 **[!UICONTROL Show Method if Not Applicable]**:

   - `Yes` - 가용성에 관계없이 모든 FedEx 발송 방법을 고객에게 보여줍니다.
   - `No` - 주문에 적용되는 FedEx 배송 방법만 표시합니다.

1. **[!UICONTROL Sort Order]**&#x200B;의 경우 체크아웃 중에 다른 게재 방법과 함께 나열할 때 FedEx가 표시되는 순서를 결정하는 숫자를 입력합니다.

   `0` = 첫 번째, `1` = 두 번째, `2` = 세 번째 등입니다.

1. 을 누르십시오 **[!UICONTROL Save Config]**.

   ![FedEx 적용 국가](../configuration-reference/sales/assets/delivery-methods-fedex-applicable-countries.png){width="600" zoomable="yes"}

>[!NOTE]
>
>Commerce는 배송료를 계산할 때 항상 전체 주문 가격을 FedEx에 신고합니다. 이 동작은 변경할 수 없습니다.
