---
title: UPS(United Parcel Service)
description: UPS를 상점의 배송 운송업체로 설정하는 방법에 대해 알아보십시오.
exl-id: a7965b2f-2473-4b63-a247-3b2230cde5d8
feature: Shipping/Delivery
source-git-commit: 59daaca469ca1bf21c420ce8520efea6c54166fa
workflow-type: tm+mt
source-wordcount: '938'
ht-degree: 0%

---

# UPS(United Parcel Service)

United Parcel Service(UPS)는 220개 이상의 국가에 육로 및 항공으로 국내 및 국제 배송 서비스를 제공합니다.

{{ups-api}}

>[!NOTE]
>
>UPS는 [차원 가중치](carriers.md#dimensional-weight)를 사용하여 일부 배송 속도를 결정할 수 있습니다. 단, Adobe Commerce은 중량 기준 배송비 계산만 지원합니다.

## 1단계: UPS 배송 계정 열기

이 배송 방법을 고객에게 제공하려면 먼저 UPS로 계정을 개설해야 합니다.

## 2단계: 스토어에 대해 UPS 활성화

1. _관리 사이드바_&#x200B;에서 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**(으)로 이동합니다.

1. 왼쪽 패널의 **[!UICONTROL Sales]**&#x200B;에서 **[!UICONTROL Delivery Methods]**&#x200B;을(를) 선택합니다.

1. **[!UICONTROL UPS]** 섹션에서 ![확장 선택기](../assets/icon-display-expand.png)를 확장합니다.

1. **[!UICONTROL Enabled for Checkout]**&#x200B;을(를) `Yes`(으)로 설정합니다.

1. UPS REST 계정(기본값)의 경우 다음을 수행합니다.

   - UPS 자격 증명을 입력하십시오. UPS 클라이언트 ID는 **[!UICONTROL User ID]**, UPS 클라이언트 암호는 **[!UICONTROL Password]**

   - 보안 연결을 통해 UPS 배송 시스템에 데이터를 보내려면 **[!UICONTROL Mode]**&#x200B;을(를) `Live`(으)로 설정하십시오. (개발 모드에서는 보안 연결을 통해 데이터를 전송하지 않습니다.)

   - 요청을 보내는 데 필요한 **[!UICONTROL Gateway URL]**&#x200B;을(를) 확인하십시오. 테스트 모드에는 샌드박스 URL(`https://wwwcie.ups.com/`)을 사용하고 라이브 요청에는 프로덕션 URL(`https://onlinetools.ups.com`)을 사용합니다. 지정된 호스트가 있는 각 요청에 대해 각 끝점을 사용해야 합니다.

   - 추적 정보를 가져오는 데 필요한 **[!UICONTROL Tracking URL]**&#x200B;을(를) 확인하십시오. 테스트 모드에는 샌드박스 URL(`https://wwwcie.ups.com/`)을 사용하고 라이브 요청에는 프로덕션 URL(`https://onlinetools.ups.com`)을 사용합니다. 지정된 호스트가 있는 각 요청에 대해 각 끝점을 사용해야 합니다.

   - **[!UICONTROL Origin of the Shipment]**&#x200B;을(를) 배송이 시작된 지역으로 설정합니다.

   - UPS에 특별 요금이 있는 경우 **[!UICONTROL Enable Negotiated Rates]**&#x200B;을(를) `Yes`(으)로 설정하고 UPS에서 할당된 6자리 **[!UICONTROL Shipper Number]**&#x200B;을(를) 입력하십시오.

   - **[!UICONTROL Live Account]**&#x200B;을(를) 다음 중 하나로 설정합니다.

      - `Yes` - 프로덕션 모드에서 UPS를 실행하고 고객에게 배송 방법으로 UPS를 제공합니다. 게이트웨이 URL 및 추적 URL에서 올바른 끝점을 사용해야 합니다.
      - `No` - 테스트 모드에서 UPS를 실행합니다. 게이트웨이 URL 및 추적 URL에서 올바른 끝점을 사용해야 합니다.

   >[!NOTE]
   >
   >표준 유나이티드 택배 서비스 유형은 사용이 중단될 예정입니다. 새 구성의 경우 기본 `United Parcel Service REST` 형식을 사용하십시오. [배송 레이블](shipping-labels.md).<br/>을 생성하는 데에도 REST 형식이 필요합니다.
   >2.4.7 릴리스의 경우 `UPS` 및 `UPS XML` 형식이 사용 중지로 예약되어 있고 `UPS REST`이(가) 기본값이므로 **[!UICONTROL UPS Type]**&#x200B;이(가) 제거됩니다. 기본 Adobe Commerce 통합에서 사용하는 통합 택배 서비스(UPS) API는 현재 OAuth 2.0 보안 모델을 지원하지 않으므로 일시적으로 더 이상 사용되지 않습니다.

   >[!IMPORTANT]
   >
   >UPS에서 현재 기본값(시스템 값)에 사용되는 HTTP에 대한 지원을 중단하고 있습니다. **[!UICONTROL Use system value]** 확인란의 선택을 취소하고 HTTPS를 사용하도록 URL을 수정하십시오. 예: `https://www.ups.com/using/services/rave/qcostcgi.cgi`

1. **[!UICONTROL Title]**&#x200B;의 경우 체크아웃 중에 표시할 이 배송 옵션의 이름을 입력하십시오.

   기본적으로 이 필드는 `United Parcel Service`(으)로 설정됩니다.

   ![UPS 사용](../configuration-reference/sales/assets/delivery-methods-ups1.png){width="600" zoomable="yes"}

## 3단계: 컨테이너 설명 완료

1. **[!UICONTROL Packages Request Type]**&#x200B;을(를) 다음 중 하나로 설정합니다.

   - `Use origin weight (few requests)`
   - `Divide to equal weight (one request)`

1. **[!UICONTROL Container]**&#x200B;의 경우 배송에 사용되는 일반적인 패키징 유형을 지정하십시오.

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

1. 제품 무게를 측정하는 데 사용하는 시스템으로 **[!UICONTROL Weight Unit]**&#x200B;을(를) 설정합니다.

   UPS에서 지원하는 가중치 시스템은 국가마다 다릅니다. 의심스러우면 UPS에 어떤 체중계를 사용해야 하는지 물어보세요. 옵션은 다음과 같습니다.

   - `LBS`
   - `KGS`

1. **[!UICONTROL Destination Type]**&#x200B;을(를) 다음 중 하나로 설정합니다.

   - `Residential` - 대부분의 배송은 B2C(Business to Consumer)입니다.
   - `Commercial` - 대부분의 배송은 B2B(Business to Business)입니다.

1. 통신사가 허용하는 **[!UICONTROL Maximum Package Weight]**&#x200B;을(를) 입력하십시오.

1. **[!UICONTROL Pickup Method]**&#x200B;을(를) 다음 중 하나로 설정합니다.

   - `Regular Daily Pickup`
   - `On Call Air`
   - `One Time Pickup`
   - `Letter Center`
   - `Customer Counter`

1. 통신사가 허용하는 **[!UICONTROL Minimum Package Weight]**&#x200B;을(를) 입력하십시오.

   ![컨테이너 설명](./assets/ups2.png){width="600" zoomable="yes"}

## 4단계: 취급 수수료 설정

처리 요금은 선택 사항이며 UPS 배송 비용에 추가되는 추가 비용으로 표시됩니다. 처리 수수료를 포함하려면 다음을 수행하십시오.

1. **[!UICONTROL Calculate Handling Fee]**&#x200B;을(를) 다음 메서드 중 하나로 설정합니다.

   - `Fixed`
   - `Percent`

1. 처리 요금이 적용되는 방법을 확인하려면 **[!UICONTROL Handling Applied]**&#x200B;을(를) 다음 중 하나로 설정하십시오.

   - `Per Order`
   - `Per Package`

1. **[!UICONTROL Handling Fee]**&#x200B;의 청구 금액을 입력하십시오.

   백분율을 입력하려면 십진수 형식을 사용합니다. 예를 들어 25%에 대해 `0.25`을(를) 입력합니다.

   ![수수료 처리](./assets/ups3.png){width="600" zoomable="yes"}

## 5단계: 허용된 방법 및 적용 가능한 국가 지정

1. **[!UICONTROL Allowed Methods]**&#x200B;의 경우 고객이 사용할 수 있는 각 UPS 배송 방법을 선택하십시오.

   이 메서드는 체크아웃 중에 UPS에 표시됩니다. 여러 메서드를 선택하려면 Ctrl 키(PC) 또는 Command 키(Mac)를 누른 채 각 옵션을 클릭합니다.

1. UPS를 통해 [무료 배송](shipping-free.md) 옵션을 제공하려면 무료 배송 옵션을 설정하십시오.

   - 무료 배송에 사용할 메서드로 **[!UICONTROL Free Method]**&#x200B;을(를) 설정하십시오. UPS를 통해 무료 배송을 제공하지 않으려면 `None`을(를) 선택하세요.

   - UPS를 통해 무료로 배송할 수 있는 최소 주문 수량을 요구하려면 **[!UICONTROL Enable Free Shipping Threshold]**&#x200B;을(를) `Enable`(으)로 설정하십시오. **[!UICONTROL Free Shipping Amount Threshold]**&#x200B;에 최소값을 입력하십시오.

1. 필요한 경우 **[!UICONTROL Displayed Error Message]**&#x200B;을(를) 변경합니다.

   이 텍스트 상자는 기본 메시지가 사전 설정되어 있지만 UPS를 사용할 수 없는 경우 표시할 다른 메시지를 입력할 수 있습니다.

   ![허용된 메서드](./assets/ups4.png){width="600" zoomable="yes"}

1. **[!UICONTROL Ship to Applicable Countries]**&#x200B;을(를) 다음 중 하나로 설정합니다.

   - `All Allowed Countries` - 스토어 구성에 지정된 모든 [국가](../getting-started/store-details.md#country-options)의 고객이 이 게재 방법을 사용할 수 있습니다.
   - `Specific Countries` - 이 옵션을 선택하면 _특정 국가로 배송_ 목록이 나타납니다. 목록에서 이 게재 방법을 사용할 수 있는 각 국가를 선택합니다.

1. **[!UICONTROL Show Method if Not Applicable]**&#x200B;을(를) 다음 중 하나로 설정합니다.

   - `Yes` - 체크아웃 중에 사용 가능한 모든 UPS 배송 방법을 나열하며 배송에 적용되지 않는 방법도 나열합니다.
   - `No` - 배송에 적용할 수 있는 UPS 배송 방법만 나열합니다.

   ![적용 가능한 국가](./assets/ups5.png){width="600" zoomable="yes"}

1. 스토어에서 보낸 UPS 배송의 세부 정보를 사용하여 로그 파일을 만들려면 **[!UICONTROL Debug]**&#x200B;을(를) `Yes`(으)로 설정하십시오.

1. **[!UICONTROL Sort Order]**&#x200B;의 경우 체크아웃 중에 다른 게재 방법과 함께 나열할 때 UPS가 표시되는 순서를 확인하려면 숫자를 입력하십시오.

   `0` = 첫 번째, `1` = 두 번째, `2` = 세 번째 등입니다.

1. **[!UICONTROL Save Config]**&#x200B;을(를) 클릭합니다.

## 단계 6: 운송 출처 주소 설정

1. [저장소 정보](../getting-started/store-details.md#store-information)가 완료되었는지 확인하세요.

1. _관리자_ 사이드바에서 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**(으)로 이동합니다.

1. 왼쪽 패널에서 **[!UICONTROL Sales]**&#x200B;을(를) 확장하고 **[!UICONTROL Shipping Settings]**&#x200B;을(를) 선택합니다.

1. 페이지에서 ![확장 선택기](../assets/icon-display-expand.png) **[!UICONTROL Origin]**&#x200B;을(를) 확장하고 배송 원본 주소를 구성합니다.

   ![판매 구성 - 배송 원본 주소 옵션](./assets/shipping-origin.png){width="600" zoomable="yes"}

1. **[!UICONTROL Save Config]**&#x200B;을(를) 클릭합니다.

>[!NOTE]
>
>Commerce은 운송비를 계산할 때 UPS에 전체 주문 가격을 신고하지 않습니다. 이 동작은 변경할 수 없습니다.
