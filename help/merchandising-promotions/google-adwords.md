---
title: Google AdWords
description: 판매 또는 기타 중요한 작업으로 이어지는 광고 클릭을 측정하기 위해 Google AdWords 전환 추적을 위해 Commerce 스토어를 구성하는 방법에 대해 알아봅니다.
exl-id: 3dd3beba-edcf-4f9e-a527-7ed3609ef1ae
feature: Marketing Tools, Integration
source-git-commit: eb0fe395020dbe2e2496aba13d2f5c2bf2d0fc27
workflow-type: tm+mt
source-wordcount: '654'
ht-degree: 0%

---

# Google AdWords

[Google AdWords][1] 는 Google 검색 결과와 Google Display Network의 회사 페이지에 광고를 배치하는 데 사용할 수 있는 서비스입니다. AdWords 대시보드에는 캠페인을 관리하고, 응답을 추적하고, 결과를 측정하는 도구가 포함되어 있습니다.

전환 추적은 판매 또는 기타 중요한 작업으로 이어지는 광고 클릭 수를 보여줍니다. 다음 _성공_ 주문이 제출된 후 고객에게 표시되는 페이지는 판매 후에만 표시되므로 전환을 추적하는 데 사용됩니다. 스토어에 대한 Google AdWords 구성을 완료한 후에는 Commerce에 이미 필요한 정보가 있으므로 전환 추적 스크립트를 성공 페이지에 복사할 필요가 없습니다. 자세한 내용은 다음을 참조하십시오. [Google AdWords 도움말][2].

![Google 검색 결과에서 광고 Adobe](./assets/google-adwords-adobe-ad.png){width="500"}

## 1단계. Google AdWords 캠페인 만들기

1. 방문 [Google AdWords][3]을 클릭하고 계정에 등록하십시오.

1. 지침에 따라 캠페인을 만듭니다.

1. 캠페인에 대한 전환 추적을 설정하려면 다음을 수행하십시오.

   - 다음에서 **[!UICONTROL Tools]** AdWords 대시보드의 탭에서 **[!UICONTROL Conversions]** 및 클릭 **[!UICONTROL Conversion]**.

   - 변환 소스를 입력하라는 메시지가 표시되면 다음을 선택합니다. **[!UICONTROL Website]**.

   - 추적할 변환 작업의 이름을 입력하고 클릭합니다 **[!UICONTROL Done]**.

   - 클릭 **[!UICONTROL Value]** 그리고 해당하는 경우 전환에 값을 할당합니다. For example:

      - 매 판매마다 5달러를 벌면 `Each time it happens` 및 값 할당 `$5`.
      - 각 판매의 값이 달라지면 값을 비워 둡니다.

     완료하려면 **[!UICONTROL Done]**.

   - 클릭 **[!UICONTROL Conversion windows]** 및 설정을 완료하여 전환을 추적할 기간, 보고 범주 및 속성 모델을 결정합니다.

1. 완료되면 다음을 클릭하십시오. **[!UICONTROL Save and Continue]**.

## 2단계. 전환 태그 가져오기

1. 아래 **[!UICONTROL Install your tag]**, 다음에 대한 전환 수를 계산하도록 선택 **[!UICONTROL Page load]**.

1. 옵션으로 다음을 추가할 수 있습니다. **[!UICONTROL Google Site Stats]** 전환 페이지에 대한 알림입니다.

   알림은 아래 모서리에 Google의 보안 표준 및 쿠키 사용에 대한 링크와 함께 표시됩니다.

1. AdWords 태그를 관리하는 방법을 선택하려면 다음 중 하나를 수행하십시오.

   - 스토어에 스크립트를 직접 추가하려면 다음을 선택하십시오. **[!UICONTROL Save instructions and tag]**.
   - 다른 사용자가 스토어에 스크립트를 추가하도록 하려면 다음을 선택하십시오. **[!UICONTROL Email instructions and tag]**.

1. 완료되면 다음을 클릭하십시오. **[!UICONTROL Done]**.

## 3단계. 스토어 구성

{{gtag-api-note}}

1. 다음에서 _관리자_ 사이드바, 이동 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. 특정 스토어 보기에 대해 Google AdWords를 구성하는 경우 다음을 수행합니다.

   - 왼쪽 상단 모서리에서 **[!UICONTROL Store View]** 이를 구성해야 합니다.

   - 범위 전환을 확인하는 메시지가 표시되면 **[!UICONTROL OK]**.

1. 왼쪽 패널에서 를 확장합니다. **[!UICONTROL Sales]** 및 선택 **[!UICONTROL Google API]**.

1. 확장 ![확장 선택기](../assets/icon-display-expand.png) 다음 **[!UICONTROL Google AdWords]** 섹션을 참조하고 다음을 수행합니다.

   - 설정 **[!UICONTROL Enable]** 끝 `Yes`.

   - 다음을 입력합니다. **[!UICONTROL Conversion ID]** Google AdWords 스크립트에서

   ![영업 구성 - Google Ads API](../configuration-reference/sales/assets/google-api-google-adwords.png){width="600" zoomable="yes"}

1. Google Sites Stat 알림의 형식을 지정하려면 다음을 수행합니다.

   - 설정 **[!UICONTROL Conversion Language]** Google AdWords 스크립트에서 식별된 언어로.

   - 다음을 입력합니다. **[!UICONTROL Conversion Format]** 전환 페이지의 Google Sites 상태 알림에 사용됩니다.

      - `1`  - Google 추적에 대한 자세한 내용을 볼 수 있는 링크가 있는 한 줄 알림을 표시합니다.
      - `2` - Google 추적에 대한 자세한 내용을 볼 수 있는 링크가 있는 두 줄 알림을 표시합니다.
      - `3` - 고객 알림을 표시하지 않습니다.

   - 다음을 입력합니다. [16진수 코드][4]{:target=&quot;_blank&quot;} **[!UICONTROL Conversion Color]** Google Site Stats 알림 레이블에 사용하려는 경우

   - 다음에 대한 암호화된 텍스트 입력 **[!UICONTROL Conversion Label]** Google Sites 상태 알림에 표시됩니다.

     For example: `MlEYCOKBnGoQz6CZoAM`

     **샘플 Google AdWords 태그 코드**

     ```html
     <!-- Google Code for Back to School Sale Conversion Page -->
     <script type="text/javascript">
     /* <![CDATA[ */
     var google_conversion_id = 999999999;
     var google_conversion_language = "en";
     var google_conversion_format = "3";
     var google_conversion_color = "ffffff";
     var google_conversion_label = "MlEYCOKBnGoQz6CZoAM";
     var google_remarketing_only = false;
     /* ]]> */
     </script>
     
     <script type="text/javascript" src="//www.googleadservices.com/pagead/conversion.js">
     </script>
     <noscript>
     <div style="display:inline;">
     <img height="1" width="1" style="border-style:none;" alt="" src="//www.googleadservices.com/pagead/conversion/872829007/?label=MlEYCOKBnGoQz6CZoAM&amp;guid=ON&amp;script=0"/>
     
     </noscript>
     ```

1. 설정 **[!UICONTROL Conversion Value Type]** 다음 중 하나를 수행합니다.

   - `Dynamic` - 동적 주문 금액 값을 기반으로 전환이 발생했는지 확인합니다.
   - `Constant` - 입력된 특정 값을 기준으로 전환이 발생했는지 확인합니다.

   의 경우 _상수_ 전환 값 유형, 특정 항목 입력 **[!UICONTROL Value]** 대상: _[!UICONTROL Order Amount]_변환 자격을 얻습니다.

1. 완료되면 다음을 클릭하십시오. **[!UICONTROL Save Config]**.

## 4단계. 구성 확인

몇 시간 지나지 않아 Google AdWords 대시보드의 추적 상태가에서 변경됩니다. `Unverified` 끝 `No recent conversions` 또는 `Recording conversions`. 누군가 광고를 클릭하여 구매하면 대시보드 및 캠페인 보고서의 전환 작업 페이지에 전환이 표시됩니다.

[1]: https://www.google.com/adwords/
[2]: https://support.google.com/adwords/answer/6095821
[3]: https://ads.google.com/
[4]: https://www.w3schools.com/colors/colors_picker.asp
