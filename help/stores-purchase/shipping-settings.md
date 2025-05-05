---
title: 배송 설정
description: 스토어에 대한 원산지 및 배송 정책을 정의하는 배송 설정을 구성하는 방법에 대해 알아봅니다.
exl-id: 767b3039-39c7-4692-a0a8-a8fde27622cc
feature: Shipping/Delivery
source-git-commit: 61df9a4bcfaf09491ae2d353478ceb281082fa74
workflow-type: tm+mt
source-wordcount: '352'
ht-degree: 0%

---

# 배송 설정

운송 구성은 모든 운송에 대한 출처의 출처, 운송 정책 및 여러 주소에 대한 운송의 처리를 설정합니다.

## 원점

원산지는 사용자의 상점이나 창고에서 만든 출하에 대한 비용을 계산하는 데 사용되며 판매된 제품에 대한 세율도 결정합니다. [EU 세금](international-tax-guidelines.md#eu-tax-configuration)을 계산할 때 각 스토어 보기에 대한 [기본 세금 대상 계산](../configuration-reference/sales/tax.md)이 배송 설정 원본 지점에 해당하는지 확인하십시오.

![원본](../configuration-reference/sales/assets/shipping-settings-origin.png){width="600" zoomable="yes"}

1. _관리자_ 사이드바에서 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**(으)로 이동합니다.

1. 왼쪽 패널에서 **[!UICONTROL Sales]**&#x200B;을(를) 확장하고 **[!UICONTROL Shipping Settings]**&#x200B;을(를) 선택합니다.

1. **[!UICONTROL Origin]** 섹션에서 ![확장 선택기](../assets/icon-display-expand.png)를 확장하고 다음을 완료합니다.

   - [!UICONTROL Country]
   - [!UICONTROL Region / State]
   - [!UICONTROL ZIP / Postal Code]
   - [!UICONTROL City]
   - [!UICONTROL Street Address] (필요한 경우 2행)

1. **[!UICONTROL Save Config]**&#x200B;을(를) 클릭합니다.

## 배송 정책

배송 정책은 회사의 비즈니스 규칙 및 배송 지침을 설명해야 합니다. 예를 들어 무료 배송을 트리거하는 가격 규칙이 있는 경우 배송 정책의 조건을 설명할 수 있습니다.

![체크아웃 중 배송 정책](./assets/storefront-checkout-shipping-policy.png){width="700" zoomable="yes"}

체크아웃 중에 배송 정책을 표시하려면 구성에서 배송 정책 매개 변수를 완료하십시오. 체크아웃 중에 고객이 _배송 정책 보기_&#x200B;를 클릭하면 텍스트가 표시됩니다.

1. _관리자_ 사이드바에서 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**(으)로 이동합니다.

1. 왼쪽 패널에서 **[!UICONTROL Sales]**&#x200B;을(를) 확장하고 **[!UICONTROL Shipping Settings]**&#x200B;을(를) 선택합니다.

1. **[!UICONTROL Shipping Policy Parameters]** 섹션에서 ![확장 선택기](../assets/icon-display-expand.png)를 확장합니다.

1. **[!UICONTROL Apply Custom Shipping Policy]**&#x200B;을(를) `Yes`(으)로 설정합니다.

1. 텍스트 상자에 **[!UICONTROL Shipping Policy]**&#x200B;을(를) 붙여넣거나 입력합니다.

   >[!NOTE]
   >
   >워드 프로세서를 사용하여 텍스트를 작성하는 경우 문서를 .txt 파일로 저장하여 텍스트에서 제어 문자를 제거해야 합니다. 그런 다음 텍스트를 복사하여 운송 정책 텍스트 상자에 붙여넣습니다.

   ![전달 정책 매개 변수](../configuration-reference/sales/assets/shipping-settings-shipping-policy-parameters.png){width="600" zoomable="yes"}

1. **[!UICONTROL Save Config]**&#x200B;을(를) 클릭합니다.

## 여러 주소

복수 주소 운송 옵션을 사용하면 체크아웃 중에 복수 주소로 주문을 출하하고 주문을 출하할 수 있는 최대 주소 수를 결정할 수 있습니다.

1. _관리자_ 사이드바에서 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**(으)로 이동합니다.

1. 왼쪽 패널에서 **[!UICONTROL Sales]**&#x200B;을(를) 확장하고 **[!UICONTROL Multishipping Settings]**&#x200B;을(를) 선택합니다.

1. **[!UICONTROL Options]** 섹션에서 ![확장 선택기](../assets/icon-display-expand.png)를 확장합니다.

   ![여러 주소 배달 옵션](../configuration-reference/sales/assets/multishipping-settings-options.png){width="600" zoomable="yes"}

1. **[!UICONTROL Allow Shipping to Multiple Addresses]**&#x200B;을(를) `Yes`(으)로 설정합니다.

1. **[!UICONTROL Maximum Qty Allowed for Shipping to Multiple Addresses]** 입력.

1. **[!UICONTROL Save Config]**&#x200B;을(를) 클릭합니다.

>[!NOTE]
>
>![Adobe Commerce B2B](../assets/b2b.svg)(Adobe Commerce B2B) 배송 주소가 여러 개인 주문의 경우 [계정에 대한 결제](../b2b/enable-basic-features.md#configure-payment-on-account) 결제 방법이 활성화되어 있더라도 체크아웃 중에는 사용할 수 없습니다.
