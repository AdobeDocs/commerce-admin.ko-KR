---
title: '[!UICONTROL Customers] &gt; [!UICONTROL Persistent Shopping Cart]'
description: Commerce 관리자의 [!UICONTROL Customers] &gt; [!UICONTROL Persistent Shopping Cart] 페이지에서 구성 설정을 검토하십시오.
exl-id: d6c5ae46-32ed-4fcd-bcd6-ee3a07d7db5f
feature: Configuration, Shopping Cart
source-git-commit: b710c0368dc765e3bf25e82324bffe7fb8192dbf
workflow-type: tm+mt
source-wordcount: '493'
ht-degree: 0%

---

# [!UICONTROL Customers] > [!UICONTROL Persistent Shopping Cart]

{{config}}

>[!NOTE]
>
>[영구 장바구니](../../stores-purchase/cart-persistent.md)를 사용하면 장바구니에 남아 있는 구매되지 않은 항목을 유지할 수 있으며 _지속성 수명_&#x200B;에 구성된 기간 동안 저장할 수 있습니다. 고객 브라우저에서 지속적인 장바구니를 사용할 수 있도록 쿠키를 허용해야 합니다.

## [!UICONTROL General Options]

![일반 옵션](./assets/persistent-shopping-cart-general.png)<!-- zoom -->

<!-- [General Options](https://docs.magento.com/user-guide/sales/cart-persistent-configuration.html) -->

| 필드 | [범위](../../getting-started/websites-stores-views.md#scope-settings) | 설명 |
|--- |--- |--- |
| [!UICONTROL Enable Persistence] | 웹 사이트 | 지속성 활성화 여부를 결정합니다. |
| [!UICONTROL Persistence Lifetime (seconds)] | 웹 사이트 | 영구적 쿠키의 수명을 초 단위로 정의합니다. 최대 허용 값은 3153600000초(100년)입니다. |
| [!UICONTROL Enable "Remember Me"] | 웹 사이트 | 저장소의 로그인 및 등록 페이지에 _내 정보 저장_ 확인란이 표시되는지 여부를 정의합니다. 옵션: <br/>**`Yes`**- _내 정보 저장_ 확인란을 표시합니다.<br/>**`No`** - _내 정보 저장_ 확인란이 표시되지 않으며 영구 쿠키는 이미 있는 고객에게만 사용됩니다. |
| [!UICONTROL "Remember Me" Default Value] | 웹 사이트 | _내 정보 저장_ 확인란의 기본 상태를 정의합니다. |
| [!UICONTROL Clear Persistence on Log Out] | 웹 사이트 | 스토어 고객이 로그아웃할 때 영구 쿠키를 삭제할지 여부를 정의합니다. 아무리 구성해도 고객이 로그아웃하지 않고 세션 쿠키가 만료되면 영구적 쿠키가 계속 사용됩니다. |
| [!UICONTROL Persist Shopping Cart] | 웹 사이트 | 영구적 쿠키를 사용하여 해당 계정의 장바구니 데이터에 액세스할 수 있는지 여부를 정의합니다. 옵션: <br/>**`Yes`**- 장바구니 콘텐츠는 세션이 종료된 후 저장됩니다.<br/>**`No`** - 장바구니 콘텐츠는 세션이 종료된 후 저장되지 않습니다. |
| [!UICONTROL Persist Wish List] | 웹 사이트 | ![Adobe Commerce](../../assets/adobe-logo.svg)(Adobe Commerce만 해당) 세션이 종료될 때 고객 희망 목록의 상태가 유지되는지 여부를 결정합니다. 옵션: <br/>**`Yes`**- 세션이 종료되면 위시리스트 콘텐츠가 저장됩니다.<br/>**`No`** - 세션이 종료될 때 위시리스트가 저장되지 않습니다. |
| [!UICONTROL Persist Recently Ordered Items] | 웹 사이트 | ![Adobe Commerce](../../assets/adobe-logo.svg)(Adobe Commerce만 해당) 세션이 종료될 때 최근에 순서가 지정된 항목의 상태가 유지되는지 여부를 결정합니다. 옵션: <br/>**`Yes`**- 세션이 종료되면 최근에 주문한 항목의 상태가 저장됩니다.<br/>**`No`** - 세션이 끝날 때 최근에 주문한 항목의 상태가 저장되지 않습니다. |
| [!UICONTROL Persist Currently Compared Products] | 웹 사이트 | ![Adobe Commerce](../../assets/adobe-logo.svg)(Adobe Commerce만 해당) 세션이 종료될 때 현재 비교되는 제품의 상태가 유지되는지 여부를 결정합니다. 옵션: <br/>**`Yes`**- 세션이 끝날 때 현재 비교되는 제품의 상태가 저장됩니다.<br/>**`No`** - 세션이 종료될 때 현재 비교되는 제품의 상태가 저장되지 않습니다. |
| [!UICONTROL Persist Comparison History] | 웹 사이트 | ![Adobe Commerce](../../assets/adobe-logo.svg)(Adobe Commerce만 해당) 세션이 종료될 때 비교 기록의 상태가 유지되는지 여부를 결정합니다. 옵션: <br/>**`Yes`**- 세션이 종료되면 비교 기록의 상태가 저장됩니다.<br/>**`No`** - 세션이 종료될 때 비교 기록의 상태가 저장되지 않습니다. |
| [!UICONTROL Persist Recently Viewed Products] | 웹 사이트 | ![Adobe Commerce](../../assets/adobe-logo.svg)(Adobe Commerce만 해당) 세션이 종료될 때 최근에 본 제품의 상태가 유지되는지 여부를 결정합니다. 옵션: <br/>**`Yes`**- 세션이 종료되면 최근에 본 제품의 상태가 저장됩니다.<br/>**`No`** - 세션이 끝날 때 최근에 본 제품의 상태가 저장되지 않습니다. |
| [!UICONTROL Persist Customer Group Membership and Segmentation] | 웹 사이트 | ![Adobe Commerce](../../assets/adobe-logo.svg)(Adobe Commerce만 해당) 세션이 종료될 때 고객의 그룹 멤버십 및 세분화 조건 상태가 유지되는지 여부를 결정합니다. 옵션: <br/>**`Yes`**- 세션이 끝날 때 고객의 그룹 멤버십 및 세분화 데이터의 상태가 저장됩니다.<br/>**`No`** - 세션이 끝날 때 고객의 그룹 멤버십 및 세분화 데이터가 저장되지 않습니다. |

{style="table-layout:auto"}
