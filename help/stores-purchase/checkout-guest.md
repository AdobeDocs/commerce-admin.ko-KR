---
title: 게스트 체크아웃
description: 스토어에서 게스트 체크아웃 기능을 활성화하는 방법을 알아봅니다.
exl-id: ce25eba3-7503-46aa-a5cd-9b7d5662164b
feature: Checkout
source-git-commit: 347321ec5b0722f06240780136cb29816aab559f
workflow-type: tm+mt
source-wordcount: '237'
ht-degree: 0%

---

# 게스트 체크아웃

구매하기 전에 쇼핑객이 계정을 개설하도록 스토어를 구성할 수 있습니다. 기본 설정을 사용하면 게스트가 결제 프로세스를 완료한 후 계정을 등록할 수 있는 옵션과 함께 구매를 수행할 수 있습니다.

![Luma 스토어에서 게스트로 체크 아웃 표시](./assets/storefront-checkout-as-guest.png){width="600" zoomable="yes"}

**_게스트 체크아웃을 사용하지 않도록 설정하려면:_**

1. _관리자_ 사이드바에서 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**(으)로 이동합니다.

1. 왼쪽 패널에서 **[!UICONTROL Sales]**&#x200B;을(를) 확장하고 **[!UICONTROL Checkout]**&#x200B;을(를) 선택합니다.

1. ![&#x200B; 섹션에서 &#x200B;](../assets/icon-display-expand.png)확장 선택기&#x200B;**[!UICONTROL Checkout Options]**&#x200B;를 확장합니다.

   ![구성 페이지에서 확장된 체크 아웃 옵션](./assets/checkout-checkout-options.png){width="700" zoomable="yes"}

이러한 각 구성 설정에 대한 자세한 설명은 [구성 참조 안내서](../configuration-reference/sales/checkout.md#checkout-options)의 _체크아웃 옵션_&#x200B;을 참조하세요.

1. 특정 스토어 보기에 대한 설정인 경우 구성이 적용되는 [스토어 보기를 선택](../configuration-reference/scope-change.md#set-the-scope)합니다.

   메시지가 표시되면 **[!UICONTROL OK]**&#x200B;을(를) 클릭하여 계속합니다.

1. **[!UICONTROL Allow Guest Checkout]**&#x200B;을(를) `No`(으)로 설정합니다.

   필요한 경우 **[!UICONTROL Use system value]** 확인란의 선택을 취소하여 이 설정을 변경합니다.

1. **[!UICONTROL Save Config]**&#x200B;을(를) 클릭합니다.

## 등록된 이메일에 대한 게스트 주문 액세스 허용

[!BADGE SaaS만]{type=Positive url="https://experienceleague.adobe.com/ko/docs/commerce/user-guides/product-solutions" tooltip="Adobe Commerce as a Cloud Service 프로젝트에만 적용됩니다(Adobe 관리 SaaS 인프라)."}

기본적으로 비활성화되어 있는 저장소 수준 구성(선택 사항)을 사용하면 게스트 구매자가 등록된 고객 계정과 일치하는 이메일 주소를 사용하여 수행한 주문을 추적할 수 있습니다.

활성화되면 등록된 이메일과 함께 수행된 게스트 체크아웃 주문에 대한 액세스 권한이 유지되면서 고객의 주문 내역에도 표시됩니다.

이 기능을 사용하려면 **스토어** > 설정 > **구성** > 판매 > **판매** > **게스트 체크아웃**&#x200B;으로 이동하고 **등록된 전자 메일에 대한 게스트 주문 액세스 허용** 설정을 `Yes`(으)로 설정합니다.
