---
title: 미국 우편 서비스(USPS)
description: USPS를 상점의 배송 운송업체로 설정하는 방법에 대해 알아봅니다.
exl-id: c9601fb8-f0f9-484a-a2e1-d50ee0f2dbf0
feature: Shipping/Delivery
source-git-commit: c9acf475eeadcd249467e4cc89fe61d37230bd7d
workflow-type: tm+mt
source-wordcount: '762'
ht-degree: 0%

---

# 미국 우편 서비스(USPS)

미국 우편 서비스는 미국 정부의 독립 우편 서비스로, 육로와 항공에 의해 국내 및 국제 배송 서비스를 제공합니다.

## 1단계: USPS 배송 계정 열기

[USPS 웹 도구][1] 계정을 엽니다. 등록 프로세스를 완료하면 사용자 ID와 USPS 테스트 서버에 대한 URL을 받게 됩니다.

[USPS 웹 도구][1] 계정을 열 수도 있습니다. 등록 프로세스를 완료하면 사용자 ID와 USPS 테스트 서버에 대한 URL을 받게 됩니다. USPS 웹 도구에 대한 자세한 내용은 [기술 설명서][2]를 참조하세요.

## 2단계: 스토어에 대해 USPS 활성화

{{$include /help/_includes/usps-api-type-configuration-note.md}}

1. _관리자_ 사이드바에서 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**(으)로 이동합니다.

1. 왼쪽 패널에서 **[!UICONTROL Sales]**&#x200B;을(를) 확장하고 **[!UICONTROL Delivery Methods]**&#x200B;을(를) 선택합니다.

1. ![ 섹션에서 ](../assets/icon-display-expand.png)확장 선택기&#x200B;**[!UICONTROL USPS]**&#x200B;를 확장합니다.

   >[!NOTE]
   >
   >필요한 경우 먼저 **[!UICONTROL Use system value]** 확인란의 선택을 해제하여 설명된 대로 다음 설정을 변경합니다.

1. **[!UICONTROL Enabled for Checkout]**&#x200B;을(를) `Yes`(으)로 설정합니다.

1. USPS REST API를 사용하는 경우 **[!UICONTROL USPS Type]**&#x200B;을(를) `USPS Rest APIs`(으)로 설정하십시오.

   USPS Web Tools API를 사용하는 경우 **[!UICONTROL USPS Type]**&#x200B;을(를) `USPS Web Tools API`(으)로 설정하십시오.

1. 필요한 경우 **[!UICONTROL Gateway URL]**&#x200B;을(를) 입력하여 USPS 배송 속도에 액세스하십시오.

   필드는 기본적으로 미리 설정되어 있으며 일반적으로 변경할 필요가 없습니다.

1. 체크아웃 중에 표시되는 이 배송 방법에 대한 **[!UICONTROL Title]**&#x200B;을(를) 입력하십시오.

1. USPS에서 제공한 자격 증명을 사용하여 다음 필드를 완료합니다.

   USPS Rest API를 사용하는 경우 다음 자격 증명을 제공해야 합니다.

   - **[!UICONTROL Consumer Key]**
   - **[!UICONTROL Consumer Secret]**
   - **[!UICONTROL Pricing Options]**

   USPS Web Tools API를 사용하는 경우 다음 자격 증명을 제공해야 합니다.

   - **[!UICONTROL User ID]**
   - **[!UICONTROL Password]**

1. **[!UICONTROL Mode]**&#x200B;을(를) 다음 중 하나로 설정합니다.

   - `Development` - 테스트 환경에서 USPS를 실행합니다. 개발 환경에서 USPS를 실행한 후 나중에 다시 돌아와 모드를 `Live`(으)로 설정하십시오.
   - `Live` - 라이브 프로덕션 환경에서 USPS를 실행합니다.

## 3단계: 패키징 설명 완료

1. 여러 패키지로 보낼 경우 순서를 관리하는 방법을 결정하려면 **[!UICONTROL Packages Request Type]**&#x200B;을(를) 다음 중 하나로 설정합니다.

   - `Divide to Equal Weight` - (1개의 요청) 패키지가 동일한 가중치로 나누어진 경우 여러 패키지의 배송을 하나의 요청으로 제출할 수 있습니다.
   - `Use Origin Weight` - (복수 요청) 배송비 계산 기준으로 원본 가중치를 사용하는 경우 복수 패키지를 별도의 요청으로 제출해야 합니다.

1. 상점에 주문한 제품을 배송하는 데 일반적으로 사용되는 포장 형식으로 **[!UICONTROL Container]**&#x200B;을(를) 설정합니다.

1. 스토어에서 제공되는 일반 패키지의 **[!UICONTROL Size]**&#x200B;을(를) 설정합니다.

1. **[!UICONTROL Machinable]**&#x200B;을(를) 다음 중 하나로 설정합니다.

   - `Yes` - 컴퓨터에서 일반 패키지를 처리할 수 있는 경우.
   - `No` - 일반 패키지를 수동으로 처리해야 하는 경우.

1. 통신사 요구 사항에 따라 **[!UICONTROL Maximum Package Weight]**&#x200B;을(를) 입력하십시오.

   ![USPS 패키징 설정](../configuration-reference/sales/assets/delivery-methods-usps-packaging.png){width="600" zoomable="yes"}

## 4단계: 취급 수수료 설정

처리 요금은 선택 사항이며 DHL 배송 비용에 추가되는 추가 비용으로 표시됩니다. 처리 수수료를 포함하려면 다음을 수행하십시오.

1. **[!UICONTROL Calculate Handling Fee]**&#x200B;을(를) 다음 메서드 중 하나로 설정합니다.

   - `Fixed`
   - `Percent`

1. 처리 요금이 적용되는 방법을 확인하려면 **[!UICONTROL Handling Applied]**&#x200B;을(를) 다음 중 하나로 설정하십시오.

   - `Per Order`
   - `Per Package`

1. **[!UICONTROL Handling Fee]**&#x200B;의 청구 금액을 입력하십시오.

   백분율을 입력하려면 십진수 형식을 사용합니다. 예를 들어 25%에 대해 `0.25`을(를) 입력합니다.

   ![USPS 취급 수수료](../configuration-reference/sales/assets/delivery-methods-usps-handling-fee.png){width="600" zoomable="yes"}

## 5단계: 허용된 방법 및 적용 가능한 국가 지정

1. **[!UICONTROL Allowed Methods]**&#x200B;의 경우 고객이 사용할 수 있는 각 USPS 배송 방법을 선택하십시오.

   이 메서드는 체크아웃 중에 USPS에 표시됩니다. 여러 메서드를 선택하려면 Ctrl 키(PC) 또는 Command 키(Mac)를 누른 채 각 옵션을 클릭합니다.

1. USPS를 통해 [무료 배송](shipping-free.md) 옵션을 제공하려면 무료 배송 옵션을 설정하십시오.

   - 무료 배송에 사용할 메서드로 **[!UICONTROL Free Method]**&#x200B;을(를) 설정하십시오. USPS를 통한 무료 배송을 제공하지 않으려면 `None`을(를) 선택하세요.

   - USPS와 함께 무료 배송에 대한 주문을 허용하는 최소 주문 금액이 필요하려면 **[!UICONTROL Enable Free Shipping Threshold]**&#x200B;을(를) `Enable`(으)로 설정하십시오. **[!UICONTROL Free Shipping Amount Threshold]**&#x200B;에 최소값을 입력하십시오.

1. 필요한 경우 **[!UICONTROL Displayed Error Message]**&#x200B;을(를) 변경합니다.

   이 텍스트 상자는 기본 메시지가 사전 설정되어 있지만 USPS를 사용할 수 없는 경우 표시할 다른 메시지를 입력할 수 있습니다.

   ![USPS 허용 메서드](../configuration-reference/sales/assets/delivery-methods-usps-allowed-methods.png){width="600" zoomable="yes"}

1. **[!UICONTROL Ship to Applicable Countries]**&#x200B;을(를) 다음 중 하나로 설정합니다.

   - `All Allowed Countries` - 스토어 구성에 지정된 모든 [국가](../getting-started/store-details.md#country-options)의 고객이 이 게재 방법을 사용할 수 있습니다.
   - `Specific Countries` - 이 옵션을 선택하면 _특정 국가로 배송_ 목록이 나타납니다. 목록에서 이 게재 방법을 사용할 수 있는 각 국가를 선택합니다.

   ![USPS 적용 국가](../configuration-reference/sales/assets/delivery-methods-usps-countries.png){width="600" zoomable="yes"}

1. **[!UICONTROL Show Method if Not Applicable]**&#x200B;을(를) 다음 중 하나로 설정합니다.

   - `Yes` - 체크아웃 중에 사용 가능한 모든 USPS 배송 방법을 나열하며, 배송에 적용되지 않는 방법도 포함합니다.
   - `No` - 배송에 적용할 수 있는 USPS 배송 방법만 나열합니다.

1. 스토어에서 만든 USPS 배송의 세부 정보를 사용하여 로그 파일을 만들려면 **[!UICONTROL Debug]**&#x200B;을(를) `Yes`(으)로 설정합니다.

1. **[!UICONTROL Sort Order]**&#x200B;의 경우 체크아웃 중에 다른 게재 방법과 함께 나열할 때 USPS가 표시되는 순서를 결정하려면 숫자를 입력하십시오.

   `0` = 첫 번째, `1` = 두 번째, `2` = 세 번째 등입니다.

1. **[!UICONTROL Save Config]**&#x200B;을(를) 클릭합니다.

[1]: https://secure.shippingapis.com/registration/
[2]: https://www.usps.com/business/web-tools-apis/welcome.htm

<!-- Last updated from includes: 2025-11-26 10:55:00 -->
