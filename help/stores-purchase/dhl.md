---
title: DHL
description: DHL을 상점의 배송 운송업체로 설정하는 방법에 대해 알아보십시오.
exl-id: 765e5f90-3e93-43cf-a5bc-6132e00b506c
feature: Shipping/Delivery
source-git-commit: 8b5af316ab1d2e632ed5fc2066974326830ab3f7
workflow-type: tm+mt
source-wordcount: '580'
ht-degree: 0%

---

# DHL

DHL은 편지, 물품, 정보의 관리 및 전송을 위한 통합된 국제 서비스와 맞춤형 고객 중심 솔루션을 제공합니다.

## 1단계: DHL 사용

1. 다음에서 _관리자_ 사이드바, 이동 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. 왼쪽 패널에서 를 확장합니다. **[!UICONTROL Sales]** 및 선택 **[!UICONTROL Delivery Methods]**.

1. 확장 ![확장 선택기](../assets/icon-display-expand.png) 다음 **[!UICONTROL DHL]** 섹션.

   >[!NOTE]
   >
   >필요한 경우 먼저 **[!UICONTROL Use system value]** 확인란을 선택하여 설명된 대로 다음 설정을 변경합니다.

1. 설정 **[!UICONTROL Enabled for Checkout]** 끝 `Yes`.

1. 일반적으로 기본값을 사용할 수 있습니다 **[!UICONTROL Gateway URL]**.

   DHL에서 대체 URL을 제공한 경우 이 필드에 해당 값을 입력합니다.

1. DHL에서 제공한 자격 증명을 사용하여 다음 필드를 작성합니다.

   - **[!UICONTROL Access ID]**
   - **[!UICONTROL Password]**
   - **[!UICONTROL Account Number]**

![DHL 계정 설정](../configuration-reference/sales/assets/delivery-methods-dhl-account-settings.png){width="600" zoomable="yes"}

## 2단계; 패키지 설명 및 취급 수수료 입력

1. 다음에서 **[!UICONTROL Content Type]** 배송하는 패키지 유형을 가장 잘 설명하는 옵션을 나열합니다.

   - `Documents`
   - `Non documents`

1. 요구 사항에 따라 처리 요금 옵션을 구성합니다.

   처리 요금은 선택 사항이며 DHL 배송 비용에 추가되는 추가 비용으로 표시됩니다. 처리 수수료를 포함하려면 다음을 수행하십시오.

   - 대상 **[!UICONTROL Calculate Handling Fee]**&#x200B;을(를) 사용하여 처리 요금을 계산하는 데 사용할 방법을 선택합니다.

      - `Fixed`
      - `Percentage`

   - 대상 **[!UICONTROL Handling Applied]**&#x200B;을(를) 클릭하여 처리 수수료를 적용할 방법을 선택합니다.

      - `Per Order`
      - `Per Package`

   - 대상 **[!UICONTROL Handling Fee]**&#x200B;금액을 계산하기 위해 선택한 방법에 따라 청구할 금액을 입력합니다.

     예를 들어, 요금이 고정 요금을 기준으로 하는 경우 다음과 같이 금액을 소수점으로 입력합니다. `4.90`. 단, 취급 수수료가 주문의 백분율을 기준으로 하는 경우 백분율로 금액을 입력합니다. 예를 들어 주문의 6%를 부과하려면 값을 다음과 같이 입력합니다. `.06`.

   - 총 주문 중량을 나누어 정확한 운송 비용 계산을 보장하려면 다음을 설정합니다. **[!UICONTROL Divide Order Weight]** 끝 `Yes`.

   - 설정 **[!UICONTROL Weight Unit]** 패키지를 다음 중 하나로 복사합니다.

      - `Pounds`
      - `Kilograms`

   - 설정 **[!UICONTROL Size]** 다음 중 하나를 포함하는 일반적인 패키지:

      - `Regular`
      - `Specific`

     다음을 선택하는 경우 `Specific`을(를) 입력한 후 **[!UICONTROL Height]**, **[!UICONTROL Depth]**, 및 **[!UICONTROL Width]** 센티미터 단위의 소포입니다.

   ![DHL 패키지 설정](../configuration-reference/sales/assets/delivery-methods-dhl-package-settings.png){width="600" zoomable="yes"}

## 3단계: 허용된 게재 방법 지정

1. 대상 **[!UICONTROL Allowed Methods]**&#x200B;을(를) 통해 고객이 사용할 수 있도록 하려는 각 메서드를 선택합니다.

   여러 메서드를 선택하려면 Ctrl 키(PC) 또는 Command 키(Mac)를 누른 채 각 옵션을 클릭합니다.

   올바른 게재 방법 목록을 표시하려면 먼저 [시작 국가](../configuration-reference/sales/shipping-settings.md).

1. 대상 **[!UICONTROL Ready Time]**&#x200B;주문이 제출된 후 패키지를 배송할 준비가 된 시간(시)을 입력합니다.

1. 편집 **[!UICONTROL Displayed Error Message]** 필요한 경우.

   이 메시지는 선택한 메서드를 사용할 수 없을 때 표시됩니다.

1. 다음을 제공하려는 경우: [무료 배송](shipping-free.md) 옵션 DHL을 통해, 무료 배송 옵션을 설정합니다.

   - 대상 **[!UICONTROL Free Method]**&#x200B;무료 배송에 사용할 방법을 선택하십시오.

   - 설정 **[!UICONTROL Free Shipping Amount Threshold]**:

     `Enable` - 최소 주문과 함께 무료 배송을 제공하는 경우 다음을 입력합니다. **[!UICONTROL Minimum Order Amount for Free Shipping]**.

     `Disable` - 모든 주문에 대해 무료 DHL 배송을 적용하지 않습니다.

     이 설정은 표준의 설정과 유사합니다 _무료 배송_ 고객이 주문에 사용되는 방법을 알 수 있도록 DHL 섹션에 표시됩니다.

   - 대상 **[!UICONTROL Free Shipping Amount Threshold]**&#x200B;를 클릭하고 주문에 대한 최소 금액을 입력하여 무료 배송을 받을 수 있습니다.

     ![DHL 허용 메서드](../configuration-reference/sales/assets/delivery-methods-dhl-allowed-methods.png){width="600" zoomable="yes"}

## 4단계: 해당 국가 지정

1. 설정 **[!UICONTROL Ship to Applicable Countries]** 다음 중 하나를 수행합니다.

   - `All Allowed Countries`
   - `Specific Countries`

   특정 국가로 배송하는 경우 **[!UICONTROL Ship to Specific Countries]** 목록을 표시합니다.

1. 설정 **[!UICONTROL Show Method if Not Applicable]**:

   `Yes` - 주문에 적용되지 않더라도 체크아웃 중에 배송 방법으로 DHL을 표시합니다.

   `No` - 해당하는 경우에만 체크아웃 중 배송 방법으로 DHL을 표시합니다.

1. 스토어에서 발송한 DHL 배송에 대한 세부 정보로 로그 파일을 생성하려면 다음을 설정합니다. **[!UICONTROL Debug]** 끝 `Yes`.

1. 대상 **[!UICONTROL Sort Order]**&#x200B;을 클릭하고, 체크아웃 중에 다른 게재 방법과 함께 나열할 때 DHL이 표시되는 순서를 결정하는 숫자를 입력합니다.

   `0` = 첫 번째, `1` = 초, `2` = 세 번째 등입니다.

1. 클릭 **[!UICONTROL Save Config]**.

   ![DHL 적용 국가](../configuration-reference/sales/assets/delivery-methods-dhl-applicable-countries.png){width="600" zoomable="yes"}
