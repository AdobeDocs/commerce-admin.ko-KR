---
title: 체크아웃 약관
description: 스토어에 대해 구성할 수 있는 약관 기능에 대해 알아봅니다.
exl-id: 59ba6385-3cc6-43e8-b984-5c26516bba88
feature: Checkout, Compliance
source-git-commit: 8b5af316ab1d2e632ed5fc2066974326830ab3f7
workflow-type: tm+mt
source-wordcount: '322'
ht-degree: 1%

---

# 체크아웃 약관

수동 사용 시 _약관_ 기능이 활성화되어 있으므로 고객은 구매를 완료하기 전에 판매 약관에 동의해야 합니다. 판매 약관에는 일반적으로 B2C 또는 B2B 사이트에 대해 법률에 의해 필요할 수 있는 공개 정보가 포함되어 있으며 구매자와 판매자의 권한에 대해 간략하게 설명합니다. 약관 메시지는 결제 정보 뒤에 나타납니다. _주문_ 단추를 클릭합니다.

![체크아웃 시 사용 약관](./assets/storefront-checkout-step2-terms-conditions.png){width="700" zoomable="yes"}

## 1단계: 체크아웃 약관 활성화

1. 다음에서 _관리자_ 사이드바, 이동 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. 왼쪽 패널에서 를 확장합니다. **[!UICONTROL Sales]** 및 선택 **[!UICONTROL Checkout]**.

1. 확장 ![확장 선택기](../assets/icon-display-expand.png) 다음 **[!UICONTROL Checkout Options]** 섹션.

   ![체크아웃 옵션](../configuration-reference/sales/assets/checkout-checkout-options.png){width="600" zoomable="yes"}

1. 다음을 확인합니다. **[!UICONTROL Enable Onepage Checkout]** 이(가) (으)로 설정됨 `Yes`.

1. 설정 **[!UICONTROL Enable Terms and Conditions]** 끝 `Yes`.

1. 클릭 **[!UICONTROL Save Config]**.

## 2단계: 고유한 약관 정보 추가

1. 다음에서 _관리자_ 사이드바, 이동 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Terms and Conditions]**.

   ![사용 약관 표](./assets/terms-conditions.png){width="600" zoomable="yes"}

1. 오른쪽 위 모서리에서 을(를) 클릭합니다. **[!UICONTROL Add New Condition]**.

1. 다음을 입력합니다. **[!UICONTROL Condition Name]** 내부 참조용.

   ![새 상태](./assets/terms-conditions-new.png){width="600" zoomable="yes"}

1. 설정 **[!UICONTROL Status]** 끝 `Enabled`.

1. 설정 **[!UICONTROL Applied]** 다음 중 하나를 수행합니다.

   - `Automatically` - 체크아웃 시 조건이 자동으로 수락됩니다.
   - `Manually` - 고객은 주문 조건을 수동으로 수락해야 합니다.

1. 설정 **[!UICONTROL Show Content as]** 다음 중 하나를 수행합니다.

   - `Text` - 약관 내용을 서식 없는 텍스트로 표시합니다.
   - `HTML` - 콘텐츠를 포맷할 수 있는 HTML으로 표시합니다.

1. 각각 선택 **[!UICONTROL Store View]** 사용 약관을 사용하려는 경우.

1. 아래로 스크롤하여 표시할 정보를 완료합니다.

   - 다음을 입력합니다. **[!UICONTROL Checkbox Text]** 사용 약관 링크의 텍스트로 사용됩니다. For example, `I understand and accept the terms and conditions of the sale`.

   - 다음에서 **[!UICONTROL Content]** 상자에 판매 약관의 전체 텍스트를 입력합니다.

1. (선택 사항) **[!UICONTROL Content Height (css)]** 픽셀 단위 : 체크아웃 중에 사용 약관 문이 나타나는 텍스트 상자의 높이를 결정합니다.

   예를 들어 96dpi 디스플레이에서 텍스트 상자를 1인치 높이로 하려면 다음을 입력합니다 `96`. 내용이 상자의 높이를 벗어나면 스크롤 막대가 나타납니다.

1. 클릭 **[!UICONTROL Save Condition]**.
