---
title: 세금 규칙
description: 제품 분류, 고객 분류 및 세율을 사용하여 세금 규칙을 정의하는 방법을 알아봅니다.
exl-id: 38d65998-7769-49ce-9814-e65df9d77bba
feature: Taxes, Currency
source-git-commit: 370131cd73a320b04ee92fa9609cb24ad4c07eca
workflow-type: tm+mt
source-wordcount: '434'
ht-degree: 0%

---

# 세금 규칙

세금 규칙은 제품 분류, 고객 분류 및 세율의 조합을 통합합니다. 각 고객은 고객 분류에 지정되고 각 제품은 제품 분류에 지정됩니다. Commerce는 각 고객의 장바구니를 분석하고, 고객 및 상품 등급과 지역에 따라 적절한 세금을 산출한다. 지역은 고객의 배송 주소, 청구 주소 또는 배송 출처를 기반으로 합니다.

>[!NOTE]
>
>수많은 세율이 정의되어야 할 때 이를 수입하여 프로세스를 단순화할 수 있다.

![세금 규칙](./assets/tax-rules.png){width="600" zoomable="yes"}

## 1단계: 세금 규칙 정보 완료

1. 다음에서 _관리자_ 사이드바, 이동 **[!UICONTROL Stores]** > _[!UICONTROL Taxes]_>**[!UICONTROL Tax Rules]**.

1. 오른쪽 위 모서리에서 을(를) 클릭합니다. **[!UICONTROL Add New Tax Rule]**.

1. 아래 _세금 규칙 정보_, 를 입력합니다. **[!UICONTROL Name]** 새 규칙용입니다.

   ![세금 규칙 정보](./assets/tax-rule-information.png){width="600" zoomable="yes"}

1. 다음을 선택합니다. **[!UICONTROL Tax Rate]** 규칙에 적용됩니다.

   기존 세율을 편집하려면 다음을 수행합니다.

   - 세율 위로 마우스를 가져간 후 _편집_ ![연필 아이콘](../assets/icon-edit-pencil.png) 아이콘.

   - 필요에 따라 양식을 업데이트하고 을(를) 클릭합니다 **[!UICONTROL Save]**.

1. 세율을 입력하려면 다음 방법 중 하나를 사용합니다.

### 방법 1: 세율을 수동으로 입력

1. 클릭 **[!UICONTROL Add New Tax Rate]**.

1. 필요에 따라 양식을 작성합니다( 참조). [조세 구역 및 세율](tax-zones-rates.md)).

1. 완료되면 다음을 클릭하십시오. **[!UICONTROL Save]**.

   ![새 세율](./assets/tax-rate-create-new.png){width="600" zoomable="yes"}

### 방법 2: 수입 세율

1. 페이지 하단에 있는 섹션으로 스크롤합니다.

1. 세율을 가져오려면 다음을 수행합니다.

   - 클릭 **[!UICONTROL Choose File]** 가져올 세율이 있는 CSV 파일로 이동합니다.

   - 클릭 **[!UICONTROL Import Tax Rates]**.

1. 세율을 내보내려면 **[!UICONTROL Export Tax Rates]** (참조 [가져오기/내보내기 세율](../systems/data-transfer-tax-rates.md)).

![가져오기/내보내기 세율](./assets/tax-rule-new-import-export.png){width="600" zoomable="yes"}

## 2단계: 추가 설정 완료

1. 섹션을 열려면 를 클릭합니다. **[!UICONTROL Additional Settings]**.

   ![세금 규칙에 대한 추가 설정](./assets/tax-class-additional-settings.png){width="600" zoomable="yes"}

1. 다음을 선택합니다. **[!UICONTROL Customer Tax Class]** 규칙이 적용되는 대상.

   - 고객 세금 분류를 편집하려면 _편집_ ![연필 아이콘](../assets/icon-edit-pencil.png) 아이콘을 클릭하고 필요에 따라 양식을 업데이트한 다음 **[!UICONTROL Save]**.

   - 세금 분류를 생성하려면 **[!UICONTROL Add New Tax Class]**&#x200B;을 클릭하고 필요에 따라 양식을 작성한 다음 을 클릭합니다. **[!UICONTROL Save]**.

1. 다음을 선택합니다. **[!UICONTROL Product Tax Class]** 규칙이 적용되는 대상.

   - 제품 세금 분류를 편집하려면 _편집_ ![연필 아이콘](../assets/icon-edit-pencil.png) 아이콘을 클릭하고 필요에 따라 양식을 업데이트한 다음 **[!UICONTROL Save]**.

   - 세금 분류를 생성하려면 **[!UICONTROL Add New Tax Class]**&#x200B;을 클릭하고 필요에 따라 양식을 작성한 다음 을 클릭합니다. **[!UICONTROL Save]**.

1. 두 개 이상의 세금이 적용되는 경우 숫자를 입력하여 다음에 대한 이 세금의 우선순위를 나타냅니다. **[!UICONTROL Priority]**.

   우선순위가 같은 두 가지 세칙이 적용되면 세금이 추가된다. 우선 순위 설정이 다른 두 세금이 적용되는 경우 세금이 합산됩니다.

1. 주문 소계를 기준으로 세금을 계산하려면 다음을 선택합니다. **[!UICONTROL Calculate off Subtotal Only]** 확인란.

1. 대상 **[!UICONTROL Sort Order]**&#x200B;와 함께 나열될 때 이 세금 규칙의 순서를 나타내는 숫자를 입력합니다.

1. 완료되면 다음을 클릭하십시오. **[!UICONTROL Save Rule]**.

## 통화 및 세금 규칙 데모

이 비디오를 통해 통화 및 세금 규칙 관리에 대해 알아보십시오.

>[!VIDEO](https://video.tv.adobe.com/v/343657/?quality=12)
