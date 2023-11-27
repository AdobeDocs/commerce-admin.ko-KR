---
title: 미국 우편 서비스(USPS)
description: USPS를 상점의 배송 운송업체로 설정하는 방법에 대해 알아봅니다.
exl-id: c9601fb8-f0f9-484a-a2e1-d50ee0f2dbf0
feature: Shipping/Delivery
source-git-commit: 50b44190a9568a8d6ad38ab29177904596569d75
workflow-type: tm+mt
source-wordcount: '746'
ht-degree: 0%

---

# 미국 우편 서비스(USPS)

미국 우편 서비스는 미국 정부의 독립 우편 서비스로, 육로와 항공에 의해 국내 및 국제 배송 서비스를 제공합니다.

## 1단계: USPS 배송 계정 열기

열기 [USPS 웹 도구][1] 계정입니다. 등록 프로세스를 완료하면 사용자 ID와 USPS 테스트 서버에 대한 URL을 받게 됩니다.

을 열 수도 있습니다. [USPS 웹 도구][1] 계정입니다. 등록 프로세스를 완료하면 사용자 ID와 USPS 테스트 서버에 대한 URL을 받게 됩니다. USPS 웹 도구에 대한 자세한 내용은 [기술 설명서][2].

## 2단계: 스토어에 대해 USPS 활성화

{{beta2-updates}}

1. 다음에서 _관리자_ 사이드바, 이동 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. 왼쪽 패널에서 를 확장합니다. **[!UICONTROL Sales]** 및 선택 **[!UICONTROL Delivery Methods]**.

1. 확장 ![확장 선택기](../assets/icon-display-expand.png) 다음 **[!UICONTROL USPS]** 섹션.

   >[!NOTE]
   >
   >필요한 경우 먼저 을(를) 선택 해제합니다. **[!UICONTROL Use system value]** 확인란을 선택하여 설명된 대로 다음 설정을 변경합니다.

1. 설정 **[!UICONTROL Enabled for Checkout]** 끝 `Yes`.

1. 필요한 경우 **[!UICONTROL Gateway URL]** USPS 배송 요금에 액세스하십시오.

   >[!IMPORTANT]
   >
   >2021년 6월 24일부터 USPS Web Tools 는 모든 비보안 HTTP 엔드포인트에 대한 지원을 제거합니다. 이 변경 후에는 비보안 HTTP 끝점에 대한 모든 Web Tools API 요청이 실패합니다. 다음을 확인하십시오. **[!UICONTROL Gateway URL]** 는 보안 HTTPS 끝점을 사용합니다.

   필드는 기본적으로 미리 설정되어 있으며 일반적으로 변경할 필요가 없습니다.

1. 입력 **[!UICONTROL Title]** 체크아웃하는 동안 표시되는 이 배송 방법에 대한 것입니다.

1. 다음을 입력합니다. **[!UICONTROL User ID]** 및 **[!UICONTROL Password]** USPS 계정용.

1. 설정 **[!UICONTROL Mode]** 다음 중 하나를 수행합니다.

   - `Development` - 테스트 환경에서 USPS를 실행합니다. 개발 환경에서 USPS를 실행한 후에는 나중에 다시 돌아와 모드 를 로 설정하십시오. `Live`.
   - `Live` - 라이브 프로덕션 환경에서 USPS를 실행합니다.

## 3단계: 패키징 설명 완료

1. 여러 패키지로 보낼 경우 주문을 관리하는 방법을 결정하려면 다음을 설정하십시오. **[!UICONTROL Packages Request Type]** 다음 중 하나를 수행합니다.

   - `Divide to Equal Weight` - (1개의 요청) 패키지가 동일한 가중치로 나누어진 경우 여러 패키지의 배송을 하나의 요청으로 제출할 수 있습니다.
   - `Use Origin Weight` - (복수 요청) 배송비 계산 기준으로 원산지 가중치를 사용하는 경우 복수 패키지를 별도의 요청으로 제출해야 합니다.

1. 설정 **[!UICONTROL Container]** 일반적으로 매장 주문 제품을 배송하는 데 사용되는 포장 유형으로 변경되었습니다.

1. 설정 **[!UICONTROL Size]** 매장에서 배송되는 일반 패키지 중 하나.

1. 설정 **[!UICONTROL Machinable]** 다음 중 하나를 수행합니다.

   - `Yes` - 일반적인 패키지가 컴퓨터에 의해 처리될 수 있는 경우.
   - `No` - 일반적인 패키지를 수동으로 처리해야 하는 경우.

1. 다음을 입력합니다. **[!UICONTROL Maximum Package Weight]** 통신사 요구 사항에 따라.

   ![USPS 패키징 설정](../configuration-reference/sales/assets/delivery-methods-usps-packaging.png){width="600" zoomable="yes"}

## 4단계: 취급 수수료 설정

처리 요금은 선택 사항이며 DHL 배송 비용에 추가되는 추가 비용으로 표시됩니다. 처리 수수료를 포함하려면 다음을 수행하십시오.

1. 설정 **[!UICONTROL Calculate Handling Fee]** 다음 방법 중 하나를 수행합니다.

   - `Fixed`
   - `Percent`

1. 처리 요금이 적용되는 방법을 결정하려면 다음을 설정하십시오. **[!UICONTROL Handling Applied]** 다음 중 하나를 수행합니다.

   - `Per Order`
   - `Per Package`

1. 금액 입력 **[!UICONTROL Handling Fee]** 청구됩니다.

   백분율을 입력하려면 십진수 형식을 사용합니다. 예를 들어, 을 입력합니다. `0.25` 25%요

   ![USPS 취급 수수료](../configuration-reference/sales/assets/delivery-methods-usps-handling-fee.png){width="600" zoomable="yes"}

## 5단계: 허용된 방법 및 적용 가능한 국가 지정

1. 대상 **[!UICONTROL Allowed Methods]**&#x200B;에서 고객이 사용할 수 있는 각 USPS 배송 방법을 선택합니다.

   이 메서드는 체크아웃 중에 USPS에 표시됩니다. 여러 메서드를 선택하려면 Ctrl 키(PC) 또는 Command 키(Mac)를 누른 채 각 옵션을 클릭합니다.

1. 다음을 제공하려는 경우: [무료 배송](shipping-free.md) 옵션은 USPS를 통해 무료 배송 옵션을 설정합니다.

   - 설정 **[!UICONTROL Free Method]** 무료 배송에 사용하려는 방법에 대해 설명합니다. USPS를 통해 무료 배송을 제공하고 싶지 않다면 다음을 선택하십시오. `None`.

   - USPS와 함께 무료 배송에 대한 주문을 승인하는 최소 주문 금액이 필요하려면 다음을 설정합니다. **[!UICONTROL Enable Free Shipping Threshold]** 끝 `Enable`. 그런 다음 의 최소값을 입력합니다. **[!UICONTROL Free Shipping Amount Threshold]**.

1. 필요한 경우 **[!UICONTROL Displayed Error Message]**.

   이 텍스트 상자는 기본 메시지가 사전 설정되어 있지만 USPS를 사용할 수 없는 경우 표시할 다른 메시지를 입력할 수 있습니다.

   ![USPS 허용 메서드](../configuration-reference/sales/assets/delivery-methods-usps-allowed-methods.png){width="600" zoomable="yes"}

1. 설정 **[!UICONTROL Ship to Applicable Countries]** 다음 중 하나를 수행합니다.

   - `All Allowed Countries` - 모든 고객의 고객 [국가](../getting-started/store-details.md#country-options) 저장소 구성에 지정된 경우 이 전달 방법을 사용할 수 있습니다.
   - `Specific Countries` - 이 옵션을 선택하면 _특정 국가로 배송_ 목록이 나타납니다. 목록에서 이 게재 방법을 사용할 수 있는 각 국가를 선택합니다.

   ![USPS 적용 국가](../configuration-reference/sales/assets/delivery-methods-usps-countries.png){width="600" zoomable="yes"}

1. 설정 **[!UICONTROL Show Method if Not Applicable]** 다음 중 하나를 수행합니다.

   - `Yes` - 체크아웃 중 배송에 적용되지 않는 방법을 포함하여 사용 가능한 모든 USPS 배송 방법을 나열합니다.
   - `No` - 납품에 적용할 수 있는 USPS 운송 방법만 나열합니다.

1. 저장소에서 만든 USPS 배송의 세부 정보가 포함된 로그 파일을 생성하려면 다음을 설정합니다. **[!UICONTROL Debug]** 끝 `Yes`.

1. 대상 **[!UICONTROL Sort Order]**&#x200B;을 클릭하고, 체크아웃 중에 다른 게재 방법과 함께 나열할 때 USPS가 표시되는 순서를 결정하는 숫자를 입력합니다.

   `0` = 첫 번째, `1` = 초, `2` = 세 번째 등입니다.

1. 클릭 **[!UICONTROL Save Config]**.


[1]: https://secure.shippingapis.com/registration/
[2]: https://www.usps.com/business/web-tools-apis/welcome.htm
