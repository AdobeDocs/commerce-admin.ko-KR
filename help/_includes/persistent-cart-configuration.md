---
title: 영구 장바구니의 구성 참조
description: 영구적 장바구니의 구성 참조에 재사용 가능한 콘텐츠.
source-git-commit: 5a4417373f6dc720e8e14f883c27348a475ec255
workflow-type: tm+mt
source-wordcount: '358'
ht-degree: 0%

---


# [!UICONTROL General Options]

![일반 옵션](/help/configuration-reference/customers/assets/persistent-shopping-cart-general.png)<!-- zoom -->

<!-- [General Options](https://experienceleague.adobe.com/en/docs/commerce-admin/stores-sales/point-of-purchase/cart/cart-persistent#configure-a-persistent-cart) -->

| 필드 | [범위](/help/getting-started/websites-stores-views.md#scope-settings) | 설명 |
|--- |------------------------------------------------------------------------|--- |
| [!UICONTROL Enable Persistence] | 웹 사이트 | 지속성 기능을 사용할지 여부를 결정합니다. |
| [!UICONTROL Persistence Lifetime (seconds)] | 웹 사이트 | 영구적 쿠키의 수명을 초 단위로 정의합니다. 최대 허용 값은 34560000초(400일)입니다. 이는 최대 권장 쿠키 수명의 제한입니다. |
| [!UICONTROL Enable "Remember Me"] | 웹 사이트 | 저장소의 로그인 및 등록 페이지에 _내 정보 저장_ 확인란이 표시되는지 여부를 정의합니다. 옵션: <br/>**`Yes`**- _내 정보 저장_ 확인란을 표시합니다.<br/>**`No`** - _내 정보 저장_ 확인란이 표시되지 않으며 영구 쿠키는 이미 있는 고객에게만 사용됩니다. |
| [!UICONTROL "Remember Me" Default Value] | 웹 사이트 | _내 정보 저장_ 확인란의 기본 상태를 정의합니다. |
| [!UICONTROL Clear Persistence on Log Out] | 웹 사이트 | 스토어 고객이 로그아웃할 때 영구 쿠키를 삭제할지 여부를 정의합니다. 이 옵션이 어떻게 구성되든 고객이 로그아웃하지 않지만 세션 쿠키가 만료되면 영구적 쿠키가 계속 사용됩니다. |
| [!UICONTROL Persist Shopping Cart] | 웹 사이트 | 영구적 쿠키를 사용하여 해당 계정의 장바구니 데이터에 액세스할 수 있는지 여부를 정의합니다. 옵션: <br/>**`Yes`**또는&#x200B;**`No`**. |
| [!UICONTROL Persist Wish List] | 웹 사이트 | ![Adobe Commerce](/help/assets/adobe-logo.svg)(Adobe Commerce만 해당) 세션이 종료될 때 고객 희망 목록의 상태가 유지되는지 여부를 결정합니다. 옵션: <br/>**`Yes`**- 세션이 종료되면 위시리스트 콘텐츠가 저장됩니다.<br/>**`No`** - 세션이 종료될 때 위시리스트가 저장되지 않습니다. |
| [!UICONTROL Persist Recently Ordered Items] | 웹 사이트 | ![Adobe Commerce](/help/assets/adobe-logo.svg)(Adobe Commerce만 해당) 세션이 종료될 때 최근에 주문한 항목의 상태가 저장되는지 여부를 결정합니다. 옵션: <br/>**`Yes`**또는&#x200B;**`No`**. |
| [!UICONTROL Persist Currently Compared Products] | 웹 사이트 | ![Adobe Commerce](/help/assets/adobe-logo.svg)(Adobe Commerce만 해당) 세션이 종료될 때 현재 비교되는 제품의 상태를 유지할지 여부를 결정합니다. 옵션: <br/>**`Yes`**또는&#x200B;**`No`**. |
| [!UICONTROL Persist Comparison History] | 웹 사이트 | ![Adobe Commerce](/help/assets/adobe-logo.svg)(Adobe Commerce만 해당) 세션이 종료될 때 비교 기록의 상태가 유지되는지 여부를 결정합니다. 옵션: <br/>**`Yes`**또는&#x200B;**`No`**. |
| [!UICONTROL Persist Recently Viewed Products] | 웹 사이트 | ![Adobe Commerce](/help/assets/adobe-logo.svg)(Adobe Commerce만 해당) 세션이 끝날 때 최근에 본 제품의 상태를 유지할지 여부를 결정합니다. 옵션: <br/>**`Yes`**또는&#x200B;**`No`**. |
| [!UICONTROL Persist Customer Group Membership and Segmentation] | 웹 사이트 | ![Adobe Commerce](/help/assets/adobe-logo.svg)(Adobe Commerce만 해당) 세션이 종료될 때 고객의 그룹 멤버십 및 세분화 조건 상태가 유지되는지 여부를 결정합니다. 옵션: <br/>**`Yes`**- 세션이 끝날 때 고객의 그룹 멤버십 및 세분화 데이터의 상태가 저장됩니다.<br/>**`No`** - 세션이 끝날 때 고객의 그룹 멤버십 및 세분화 데이터가 저장되지 않습니다. |

{style="table-layout:auto"}
