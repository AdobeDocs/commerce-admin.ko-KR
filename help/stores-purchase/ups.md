---
title: UPS(United Parcel Service)
description: UPS를 상점의 배송 운송업체로 설정하는 방법에 대해 알아보십시오.
exl-id: a7965b2f-2473-4b63-a247-3b2230cde5d8
feature: Shipping/Delivery
source-git-commit: 50b44190a9568a8d6ad38ab29177904596569d75
workflow-type: tm+mt
source-wordcount: '827'
ht-degree: 0%

---

# UPS(United Parcel Service)

United Parcel Service(UPS)는 220개 이상의 국가에 육로 및 항공으로 국내 및 국제 배송 서비스를 제공합니다.

{{ups-api}}

>[!NOTE]
>
>UPS는 다음을 사용할 수 있습니다. [차원 가중치](carriers.md#dimensional-weight) 배송료를 결정합니다. 단, Adobe Commerce은 중량 기준 배송비 계산만 지원합니다.

## 1단계: UPS 배송 계정 열기

이 배송 방법을 고객에게 제공하려면 먼저 UPS로 계정을 개설해야 합니다.

## 2단계: 스토어에 대해 UPS 활성화

{{beta2-updates}}

1. 다음에서 _관리 사이드바_&#x200B;로 이동합니다. **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. 왼쪽 패널에서 **[!UICONTROL Sales]**, 선택 **[!UICONTROL Delivery Methods]**.

1. 확장 ![확장 선택기](../assets/icon-display-expand.png) 다음 **[!UICONTROL UPS]** 섹션.

1. 설정 **[!UICONTROL Enabled for Checkout]** 끝 `Yes`.

1. UPS XML 계정(기본값)의 경우 다음을 설정합니다. **[!UICONTROL UPS Type]** 끝 `United Parcel Service XML` 다음을 수행합니다.

   - UPS 자격 증명을 입력하십시오. **[!UICONTROL User ID]**, **[!UICONTROL Access License Number]** (16자리 UPS 계정 `Access Key`), 및 **[!UICONTROL Password]**

   - 설정 **[!UICONTROL Mode]** 끝 `Live` 보안 연결을 통해 UPS 배송 시스템으로 데이터를 전송합니다. (개발 모드에서는 보안 연결을 통해 데이터를 전송하지 않습니다.)

   - 확인 **[!UICONTROL Gateway XML URL]** XML 파일로 요청을 보내는 데 필요합니다.

   - 설정 **[!UICONTROL Origin of the Shipment]** 배송이 시작되는 지역으로 이동합니다.

   - UPS와 특별 요금이 있는 경우 다음을 설정하십시오. **[!UICONTROL Enable Negotiated Rates]** 끝 `Yes` 6자리 입력 **[!UICONTROL Shipper Number]** UPS에서 귀하에게 할당했습니다.

1. 표준 UPS 계정의 경우 다음을 설정합니다 **[!UICONTROL UPS Type]** 끝 `United Parcel Service` 다음을 수행합니다.

   >[!NOTE]
   >
   >표준 유나이티드 택배 서비스 유형은 사용이 중단될 예정입니다. 새 구성의 경우 기본값을 사용해야 합니다.  `United Parcel Service XML` 유형. 을 생성하려면 XML 유형도 필요합니다. [배송 레이블](shipping-labels.md).

   - 설정 **[!UICONTROL Live Account]** 다음 중 하나를 수행합니다.

      - `Yes` - 프로덕션 모드에서 UPS를 실행하고 고객에게 배송 방법으로 UPS를 제공합니다.
      - `No` - 테스트 모드에서 UPS를 실행합니다.

   - 다음에서 **[!UICONTROL Gateway URL]** 필드에 UPS 배송 요율을 계산하는 데 사용되는 URL을 입력합니다.

     >[!IMPORTANT]
     >
     >UPS에서 현재 기본값(시스템 값)에 사용되는 HTTP에 대한 지원을 중단하고 있습니다. 지우기 **[!UICONTROL Use system value]** 확인란을 선택하고 HTTPS를 사용하도록 URL을 수정합니다. 예: `https://www.ups.com/using/services/rave/qcostcgi.cgi`

1. 대상 **[!UICONTROL Title]**&#x200B;을 클릭하고 체크아웃 중에 표시할 배송 옵션의 이름을 입력합니다.

   기본적으로 이 필드는 로 설정됩니다. `United Parcel Service`.

   ![UPS 활성화](../configuration-reference/sales/assets/delivery-methods-ups1.png){width="600" zoomable="yes"}

## 3단계: 컨테이너 설명 완료

1. 설정 **[!UICONTROL Packages Request Type]** 다음 중 하나를 수행합니다.

   - `Use origin weight (few requests)`
   - `Divide to equal weight (one request)`

1. 대상 **[!UICONTROL Container]**&#x200B;배송에 사용되는 일반적인 포장 유형을 지정합니다.

   - `Customer Packaging`
   - `UPS Letter Envelope`
   - `Customer Supplied Package`
   - `UPS Tube`
   - `PAK`
   - `UPS Express Box`
   - `UPS Worldwide 25 kilo`
   - `UPS Worldwide 10 kilo`
   - `Pallet`
   - `Small Express Box`
   - `Medium Express Box`
   - `Large Express Box`

1. 설정 **[!UICONTROL Weight Unit]** 제품 무게를 측정하는 데 사용하는 시스템으로 이동합니다.

   UPS에서 지원하는 가중치 시스템은 국가마다 다릅니다. 의심스러우면 UPS에 어떤 체중계를 사용해야 하는지 물어보세요. 옵션은 다음과 같습니다.

   - `LBS`
   - `KGS`

1. 설정 **[!UICONTROL Destination Type]** 다음 중 하나를 수행합니다.

   - `Residential` - 배송의 대부분은 비즈니스 대 소비자 (B2C)입니다.
   - `Commercial` - 배송의 대부분은 비즈니스 대 비즈니스 (B2B)입니다.

1. 다음을 입력합니다. **[!UICONTROL Maximum Package Weight]** 통신사가 허용합니다.

1. 설정 **[!UICONTROL Pickup Method]** 다음 중 하나를 수행합니다.

   - `Regular Daily Pickup`
   - `On Call Air`
   - `One Time Pickup`
   - `Letter Center`
   - `Customer Counter`

1. 다음을 입력합니다. **[!UICONTROL Minimum Package Weight]** 통신사가 허용합니다.

   ![컨테이너 설명](./assets/ups2.png){width="600" zoomable="yes"}

## 4단계: 취급 수수료 설정

처리 요금은 선택 사항이며 UPS 배송 비용에 추가되는 추가 비용으로 표시됩니다. 처리 수수료를 포함하려면 다음을 수행하십시오.

1. 설정 **[!UICONTROL Calculate Handling Fee]** 다음 방법 중 하나를 수행합니다.

   - `Fixed`
   - `Percent`

1. 처리 요금이 적용되는 방법을 결정하려면 다음을 설정하십시오. **[!UICONTROL Handling Applied]** 다음 중 하나를 수행합니다.

   - `Per Order`
   - `Per Package`

1. 금액 입력 **[!UICONTROL Handling Fee]** 청구됩니다.

   백분율을 입력하려면 십진수 형식을 사용합니다. 예를 들어, 을 입력합니다. `0.25` 25%요

   ![취급 수수료](./assets/ups3.png){width="600" zoomable="yes"}

## 5단계: 허용된 방법 및 적용 가능한 국가 지정

1. 대상 **[!UICONTROL Allowed Methods]**&#x200B;에서 고객이 사용할 수 있는 각 UPS 배송 방법을 선택하십시오.

   이 메서드는 체크아웃 중에 UPS에 표시됩니다. 여러 메서드를 선택하려면 Ctrl 키(PC) 또는 Command 키(Mac)를 누른 채 각 옵션을 클릭합니다.

1. 다음을 제공하려는 경우: [무료 배송](shipping-free.md) UPS를 통해 무료 배송 옵션을 설정합니다.

   - 설정 **[!UICONTROL Free Method]** 무료 배송에 사용하려는 방법에 대해 설명합니다. UPS를 통해 무료 배송을 제공하고 싶지 않다면 다음을 선택하십시오. `None`.

   - UPS와 함께 무료 배송에 대해 주문을 받을 수 있는 최소 주문 금액이 필요하려면 다음을 설정합니다. **[!UICONTROL Enable Free Shipping Threshold]** 끝 `Enable`. 그런 다음 의 최소값을 입력합니다. **[!UICONTROL Free Shipping Amount Threshold]**.

1. 필요한 경우 **[!UICONTROL Displayed Error Message]**.

   이 텍스트 상자는 기본 메시지가 사전 설정되어 있지만 UPS를 사용할 수 없는 경우 표시할 다른 메시지를 입력할 수 있습니다.

   ![허용된 메서드](./assets/ups4.png){width="600" zoomable="yes"}

1. 설정 **[!UICONTROL Ship to Applicable Countries]** 다음 중 하나를 수행합니다.

   - `All Allowed Countries` - 모든 고객의 고객 [국가](../getting-started/store-details.md#country-options) 저장소 구성에 지정된 경우 이 전달 방법을 사용할 수 있습니다.
   - `Specific Countries` - 이 옵션을 선택하면 _특정 국가로 배송_ 목록이 나타납니다. 목록에서 이 게재 방법을 사용할 수 있는 각 국가를 선택합니다.

1. 설정 **[!UICONTROL Show Method if Not Applicable]** 다음 중 하나를 수행합니다.

   - `Yes` - 체크아웃 시 사용할 수 있는 모든 UPS 배송 방법을 나열합니다. 여기에는 배송에 적용되지 않는 방법도 포함됩니다.
   - `No` - 납품에 적용할 수 있는 UPS 운송 방법만 나열합니다.

   ![해당 국가](./assets/ups5.png){width="600" zoomable="yes"}

1. 스토어에서 발송한 UPS 배송에 대한 세부 정보를 사용하여 로그 파일을 생성하려면 다음을 설정합니다. **[!UICONTROL Debug]** 끝 `Yes`.

1. 대상 **[!UICONTROL Sort Order]**&#x200B;을 클릭하고 체크아웃 중에 다른 게재 방법과 함께 나열할 때 UPS가 표시되는 순서를 결정하는 숫자를 입력합니다.

   `0` = 첫 번째, `1` = 초, `2` = 세 번째 등입니다.

1. 클릭 **[!UICONTROL Save Config]**.

## 단계 6: 운송 출처 주소 설정

1. 다음을 확인하십시오. [정보 저장](../getting-started/store-details.md#store-information) 이(가) 완료되었습니다.

1. 다음에서 _관리자_ 사이드바, 이동 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. 왼쪽 패널에서 를 확장합니다. **[!UICONTROL Sales]** 및 선택 **[!UICONTROL Shipping Settings]**.

1. 확장 ![확장 선택기](../assets/icon-display-expand.png) **[!UICONTROL Origin]** 페이지에서 배송 원본 주소를 구성합니다.

   ![판매 구성 - 배송 출처 주소 옵션](./assets/shipping-origin.png){width="600" zoomable="yes"}

1. 클릭 **[!UICONTROL Save Config]**.

>[!NOTE]
>
>Commerce는 운송비를 계산할 때 UPS에 전체 주문 가격을 신고하지 않습니다. 이 동작은 변경할 수 없습니다.
