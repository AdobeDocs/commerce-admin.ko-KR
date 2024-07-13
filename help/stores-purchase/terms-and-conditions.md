---
title: 체크아웃 약관
description: 스토어에 대해 구성할 수 있는 약관 기능에 대해 알아봅니다.
exl-id: 59ba6385-3cc6-43e8-b984-5c26516bba88
feature: Checkout, Compliance
source-git-commit: 8b5af316ab1d2e632ed5fc2066974326830ab3f7
workflow-type: tm+mt
source-wordcount: '322'
ht-degree: 0%

---

# 체크아웃 약관

수동 _약관_ 기능을 사용하도록 설정한 경우 고객은 구매를 완료하기 전에 판매 약관에 동의해야 합니다. 판매 약관에는 일반적으로 B2C 또는 B2B 사이트에 대해 법률에 의해 필요할 수 있는 공개 정보가 포함되어 있으며 구매자와 판매자의 권한에 대해 간략하게 설명합니다. 결제 정보 뒤에 _주문_ 단추 바로 앞에 약관 메시지가 나타납니다.

![체크아웃 시 사용 약관](./assets/storefront-checkout-step2-terms-conditions.png){width="700" zoomable="yes"}

## 1단계: 체크아웃 약관 활성화

1. _관리자_ 사이드바에서 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**(으)로 이동합니다.

1. 왼쪽 패널에서 **[!UICONTROL Sales]**&#x200B;을(를) 확장하고 **[!UICONTROL Checkout]**&#x200B;을(를) 선택합니다.

1. **[!UICONTROL Checkout Options]** 섹션에서 ![확장 선택기](../assets/icon-display-expand.png)를 확장합니다.

   ![체크아웃 옵션](../configuration-reference/sales/assets/checkout-checkout-options.png){width="600" zoomable="yes"}

1. **[!UICONTROL Enable Onepage Checkout]**&#x200B;이(가) `Yes`(으)로 설정되어 있는지 확인하십시오.

1. **[!UICONTROL Enable Terms and Conditions]**&#x200B;을(를) `Yes`(으)로 설정합니다.

1. **[!UICONTROL Save Config]**&#x200B;을(를) 클릭합니다.

## 2단계: 고유한 약관 정보 추가

1. _관리자_ 사이드바에서 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Terms and Conditions]**(으)로 이동합니다.

   ![사용 약관 표](./assets/terms-conditions.png){width="600" zoomable="yes"}

1. 오른쪽 상단에서 **[!UICONTROL Add New Condition]**&#x200B;을(를) 클릭합니다.

1. 내부 참조를 위해 **[!UICONTROL Condition Name]**&#x200B;을(를) 입력하십시오.

   ![새 조건](./assets/terms-conditions-new.png){width="600" zoomable="yes"}

1. **[!UICONTROL Status]**&#x200B;을(를) `Enabled`(으)로 설정합니다.

1. **[!UICONTROL Applied]**&#x200B;을(를) 다음 중 하나로 설정합니다.

   - `Automatically` - 체크아웃 시 조건이 자동으로 수락됩니다.
   - `Manually` - 고객이 조건을 수동으로 수락하여 주문해야 합니다.

1. **[!UICONTROL Show Content as]**&#x200B;을(를) 다음 중 하나로 설정합니다.

   - `Text` - 약관 내용을 서식 없는 텍스트로 표시합니다.
   - `HTML` - 콘텐츠를 포맷할 수 있는 HTML으로 표시합니다.

1. 이 사용 약관을 사용할 각 **[!UICONTROL Store View]**&#x200B;을(를) 선택하십시오.

1. 아래로 스크롤하여 표시할 정보를 완료합니다.

   - 사용 약관 링크의 텍스트로 사용할 **[!UICONTROL Checkbox Text]**&#x200B;을(를) 입력하십시오. 예: `I understand and accept the terms and conditions of the sale`.

   - **[!UICONTROL Content]** 상자에 판매 약관의 전체 텍스트를 입력합니다.

1. (선택 사항) 체크아웃 중에 사용 약관 문이 나타나는 텍스트 상자의 높이를 결정하려면 **[!UICONTROL Content Height (css)]**&#x200B;을(를) 픽셀 단위로 입력하십시오.

   예를 들어 96dpi 디스플레이에서 텍스트 상자를 1인치 높이로 만들려면 `96`을(를) 입력합니다. 내용이 상자의 높이를 벗어나면 스크롤 막대가 나타납니다.

1. **[!UICONTROL Save Condition]**&#x200B;을(를) 클릭합니다.
