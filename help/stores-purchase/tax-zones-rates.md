---
title: 조세 구역 및 세율
description: 세금을 징수 및 송금하는 각 지리적 영역에 대한 세율을 정의하는 방법을 알아봅니다.
exl-id: d8eb0743-d277-438d-91ed-fc711a6ba3ae
feature: Taxes
source-git-commit: 8b5af316ab1d2e632ed5fc2066974326830ab3f7
workflow-type: tm+mt
source-wordcount: '377'
ht-degree: 0%

---

# 조세 구역 및 세율

세율은 일반적으로 특정 지리적 지역 내에서 이루어지는 거래에 적용된다. 사용 _세금 구역 및 세율_ 세금을 징수 및 송금하는 각 지리적 영역에 대한 세율을 지정하는 도구입니다. 각 조세 구역 및 세율에는 고유 식별자가 있으므로 주어진 지리적 영역(예: 음식이나 의약품에 과세하지 않지만 다른 품목에 과세하는 장소)에 대해 여러 세율을 가질 수 있습니다.

상점세는 상점의 주소를 기준으로 계산됩니다. 주문에 대한 실제 고객 세금은 고객이 주문 정보를 완료한 후에 계산됩니다. 그런 다음 상점은 점포의 세금 구성에 따라 세금을 계산합니다.

![세금 구역 및 세율](./assets/tax-zones-rates.png){width="600" zoomable="yes"}

## 새 세율 정의

1. 다음에서 _관리자_ 사이드바, 이동 **[!UICONTROL Stores]** > _[!UICONTROL Taxes]_>**[!UICONTROL Tax Zones and Rates]**.

1. 오른쪽 위 모서리에서 을(를) 클릭합니다. **[!UICONTROL Add New Tax Rate]**.

   ![새 세율](./assets/tax-rate-new.png){width="600" zoomable="yes"}

1. 입력 **[!UICONTROL Tax Identifier]**.

1. 단일 우편 번호에 세율을 적용하려면 다음 코드를 입력합니다. **[!UICONTROL Zip/Post Code]**.

   별표 와일드카드(`*`)는 코드에서 최대 10자를 일치시키는 데 사용할 수 있습니다. 예를 들어, `90*` 는 90000부터 90999까지의 모든 우편번호를 나타냅니다.

1. ZIP 또는 우편 번호 범위에 세율을 적용하려면 다음을 수행합니다.

   - 다음 항목 선택 **[!UICONTROL Zip/Post is Range]** 확인란을 선택하고 범위의 첫 번째 및 마지막 ZIP 또는 우편번호를 입력하여 범위를 정의합니다. **[!UICONTROL Range From]** 및 **[!UICONTROL Range To]**.

     ![ZIP/게시물이 범위임](./assets/tax-rate-new-zip-post-range.png){width="600" zoomable="yes"}

   - 다음을 선택합니다. **[!UICONTROL State]** 세율이 적용되는 곳.

   - 다음을 선택합니다. **[!UICONTROL Country]** 세율이 적용되는 곳.

   - 다음을 입력합니다. **[!UICONTROL Rate Percent]** 세율 계산에 사용됩니다.

1. 여러 스토어가 있는 경우 다음을 설정할 수 있습니다 **[!UICONTROL Tax Titles]** 각 스토어 조회수.

   >[!NOTE]
   >
   >세금 식별자를 사용하려면 이 필드를 비워 둡니다.

1. 완료되면 다음을 클릭하십시오. **[!UICONTROL Save Rate]**.

## 기존 세율 편집

1. 다음에서 _관리자_ 사이드바, 이동 **[!UICONTROL Stores]** > _[!UICONTROL Taxes]_>**[!UICONTROL Tax Zones and Rates]**.

1. 세율을에서 찾습니다. _[!UICONTROL Tax Zones and Rates]_표를 표시하고 편집 모드로 레코드를 엽니다.

   목록에 요금이 많은 경우 [필터 컨트롤](../getting-started/admin-grid-controls.md) 필요한 비율을 찾습니다.

1. 필요한 사항을 변경합니다. **[!UICONTROL Tax Rate Information]**.

1. 업데이트 **[!UICONTROL Tax Titles]** 필요한 경우.

1. 완료되면 다음을 클릭하십시오. **[!UICONTROL Save Rate]**.

## 세율 삭제

1. 다음에서 _관리자_ 사이드바, 이동 **[!UICONTROL Stores]** > _[!UICONTROL Taxes]_>**[!UICONTROL Tax Zones and Rates]**.

1. 삭제할 세율을 찾아 편집 모드로 엽니다.

1. 메뉴 모음에서 를 클릭합니다. **[!UICONTROL Delete Rate]**.

1. 작업을 확인하려면 다음을 클릭합니다. **[!UICONTROL OK]**.
