---
title: '[!UICONTROL Sales] &gt; [!UICONTROL Gift Cards]'
description: Commerce 관리자의 [!UICONTROL Sales] &gt; [!UICONTROL Gift Cards] 페이지에서 구성 설정을 검토하십시오.
exl-id: 95bfdbde-633e-44d0-9d43-00dde671ab6d
feature: Configuration, Gift
source-git-commit: b710c0368dc765e3bf25e82324bffe7fb8192dbf
workflow-type: tm+mt
source-wordcount: '335'
ht-degree: 1%

---

# [!UICONTROL Sales] > [!UICONTROL Gift Cards]

{{ee-feature}}

{{config}}

## [!UICONTROL Gift Card Email Settings]

![기프트 카드 전자 메일 설정](./assets/gift-cards-gift-card-email-settings.png)<!-- zoom -->

<!-- [Gift Card Email Settings](https://docs.magento.com/user-guide/catalog/product-gift-card-account-configuration.html) -->

| 필드 | [범위](../../getting-started/websites-stores-views.md#scope-settings) | 설명 |
|--- |--- |--- |
| [!UICONTROL Gift Card Notification Email Sender] | 스토어 뷰 | 기프트 카드 알림 전자 메일의 보낸 사람으로 표시되는 [스토어 연락처](../../getting-started/store-details.md#store-email-addresses)를 식별합니다. 기본값: `General Contact` |
| [!UICONTROL Gift Card Notification Email Template] | 스토어 뷰 | 기프트 카드 알림 전자 메일에 사용되는 [템플릿](../../systems/email-templates.md)을(를) 결정합니다. |

{style="table-layout:auto"}

## [!UICONTROL Gift Card General Settings]

![기프트 카드 일반 설정](./assets/gift-cards-gift-card-general-settings.png)<!-- zoom -->

<!-- [Gift Card General Settings](https://docs.magento.com/user-guide/catalog/product-gift-card-account-configuration.html) -->

| 필드 | [범위](../../getting-started/websites-stores-views.md#scope-settings) | 설명 |
|--- |--- |--- |
| [!UICONTROL Redeemable] | 글로벌 | 기프트 카드 소지자가 그 가치를 현금으로 상환할 수 있는지 여부를 결정합니다. 옵션: `Yes` / `No`. |
| [!UICONTROL Lifetime (days)] | 글로벌 | 카드가 유효한 일수를 결정합니다. 비워 두면 카드가 만료되지 않습니다. <br/><br/>**_중요:_**일부 지역에서는 기프트 카드에 만료 데이터를 설정할 수 없습니다. 기프트 카드의 라이프타임을 정하기 전에 현지 법률을 확인하십시오. |
| [!UICONTROL Allow Gift Message] | 스토어 뷰 | 기프트 카드를 구입한 고객이 기프트 메시지를 포함하는 옵션을 사용할 수 있는지 여부를 결정합니다. 옵션: `Yes` / `No`. |
| [!UICONTROL Gift Message Maximum Length] | 스토어 뷰 | 기프트 카드 메시지에 사용할 수 있는 최대 문자 수를 결정합니다. 기본값: 255 |
| [!UICONTROL Generate Gift Card Account when Order Item is] | 글로벌 | 고객이 주문을 할 때 또는 주문 송장이 발행될 때 기프트 카드 계정이 생성되는지 여부를 결정합니다. 옵션: `Ordered` / `Invoiced` |

{style="table-layout:auto"}

## [!UICONTROL Email Sent from Gift Card Account Management]

![기프트 카드 계정 관리에서 보낸 전자 메일](./assets/gift-cards-email-sent-from-account.png)<!-- zoom -->

<!-- [Email Sent from Gift Card Account Management](https://docs.magento.com/user-guide/catalog/product-gift-card-account-configuration.html) -->

| 필드 | [범위](../../getting-started/websites-stores-views.md#scope-settings) | 설명 |
|--- |--- |--- |
| [!UICONTROL Gift Card Email Sender] | 스토어 뷰 | 기프트 카드 전자 메일을 보낸 사람으로 표시되는 [스토어 연락처](../../getting-started/store-details.md#store-email-addresses)를 식별합니다. 기본값: `General Contact` |
| [!UICONTROL Gift Card Template] | 스토어 뷰 | 기프트 카드 전자 메일에 사용할 [템플릿](../../systems/email-templates.md)을(를) 결정합니다. |

{style="table-layout:auto"}

## [!UICONTROL Gift Card Account General Settings]

![기프트 카드 계정 일반 설정](./assets/gift-cards-gift-card-account-general-settings.png)<!-- zoom -->

<!-- [Gift Card Account General Settings](https://docs.magento.com/user-guide/catalog/product-gift-card-account-configuration.html) -->

| 필드 | [범위](../../getting-started/websites-stores-views.md#scope-settings) | 설명 |
|--- |--- |--- |
| [!UICONTROL Code Length] | 글로벌 | 기프트 카드 코드의 길이를 결정합니다. |
| [!UICONTROL Code Format] | 글로벌 | 기프트 카드 코드의 형식을 결정합니다. 옵션: `Alphanumeric` / `Numeric` |
| [!UICONTROL Code Prefix] | 글로벌 | 코드 시작 부분에 추가되는 접두사를 정의합니다. |
| [!UICONTROL Code Suffix] | 글로벌 | 코드 끝에 추가된 접미사를 정의합니다. |
| [!UICONTROL Dash Every X Characters] | 글로벌 | 코드에 대시를 포함하려면 각 대시 사이의 문자 수를 결정합니다. |
| [!UICONTROL New Pool Size] | 글로벌 | 생성할 새 코드 풀의 크기를 결정합니다. |
| [!UICONTROL Low Code Pool Threshold] | 글로벌 | 풀을 보충해야 한다는 경고를 트리거하는 코드 풀의 레코드 수를 결정합니다. |
| [!UICONTROL Generate] | 글로벌 | 를 클릭하여 기프트 카드 코드 목록을 생성합니다. |

{style="table-layout:auto"}
