---
title: '[!UICONTROL Customers] &gt; [!UICONTROL Gift Registry]'
description: Commerce 관리자의 [!UICONTROL Customers] &gt; [!UICONTROL Gift Registry] 페이지에서 구성 설정을 검토하십시오.
exl-id: c5153c4e-897a-41d2-bde1-8483855d1a37
feature: Configuration, Gift
source-git-commit: 76bd1b1af9b55d69bd98209d70fb5518f190a3e1
workflow-type: tm+mt
source-wordcount: '348'
ht-degree: 1%

---

# [!UICONTROL Customers] > [!UICONTROL Gift Registry]

{{ee-feature}}

{{config}}

이러한 설정을 사용하여 매장 고객의 선물 등록을 활성화하는 방법에 대한 자세한 내용은 [선물 등록 구성](../../merchandising-promotions/gift-registry-configure.md)을 참조하십시오. 상점에서 선물 레지스트리 검색을 포함하는 방법에 대한 자세한 내용은 [선물 레지스트리 검색 추가](../../merchandising-promotions/gift-registry-search.md)를 참조하십시오.

## [!UICONTROL General Options]

![일반 옵션](./assets/gift-registry-general-options.png)<!-- zoom -->

<!-- [General Options](https://docs.magento.com/user-guide/marketing/gift-registry-configure.html) -->

| 필드 | [범위](../../getting-started/websites-stores-views.md#scope-settings) | 설명 |
|--- |--- |--- |
| [!UICONTROL Enable Gift Registry] | 스토어 뷰 | 선물 등록기를 사용할 수 있는지 여부를 결정합니다. 옵션: <br/>**`Yes`**- 선택한 스토어 보기에 대한 선물 등록을 활성화합니다. 등록된 고객의 계정 대시보드에 선물 등록 탭이 나타납니다.<br/>**`No`** - 스토어 보기에서는 선물 등록기를 사용할 수 없습니다. |
| [!UICONTROL Maximum Registrants] | 스토어 뷰 | 고객이 선물 레지스트리에 추가할 수 있는 사람 수를 설정합니다. 고객은 각 등록자와 선물 등록부를 공유합니다. 상점에서는 최대 수에 도달할 때까지 고객이 _등록자 추가_ 단추를 사용할 수 있습니다. |

{style="table-layout:auto"}

## [!UICONTROL Owner Notification]

![소유자 알림](./assets/gift-registry-owner-notification.png)<!-- zoom -->

<!-- [Owner Notification](https://docs.magento.com/user-guide/marketing/gift-registry-configure.html) -->

| 필드 | [범위](../../getting-started/websites-stores-views.md#scope-settings) | 설명 |
|--- |--- |--- |
| [!UICONTROL Email Template] | 스토어 뷰 | 선물 레지스트리를 만들 때 전송되는 소유자 알림 이메일에 사용되는 템플릿을 결정합니다. 기본 템플릿: 선물 레지스트리 소유자 알림 |
| [!UICONTROL Email Sender] | 스토어 뷰 | 선물 레지스트리 소유자 알림 전자 메일의 보낸 사람으로 표시되는 [스토어 연락처](../../getting-started/store-details.md#store-email-addresses)를 식별합니다. 기본값: `General Contact` |

{style="table-layout:auto"}

## 선물 등록 공유

![선물 레지스트리 공유](./assets/gift-registry-gift-registry-sharing.png)<!-- zoom -->

<!-- Gift Registry Sharing](https://docs.magento.com/user-guide/marketing/gift-registry-configure.html) -->

| 필드 | [범위](../../getting-started/websites-stores-views.md#scope-settings) | 설명 |
|--- |--- |--- |
| [!UICONTROL Email Template] | 스토어 뷰 | 선물 레지스트리를 만들 때 전송되는 선물 레지스트리 공유 전자 메일에 사용되는 템플릿을 결정합니다. 소유자가 _선물 레지스트리 공유_&#x200B;를 클릭하면 각 받는 사람에게 전자 메일이 전송됩니다. 기본 템플릿: `Gift Registry Sharing` |
| [!UICONTROL Email Sender] | 스토어 뷰 | 선물 레지스트리 공유 전자 메일의 보낸 사람으로 표시되는 [스토어 연락처](../../getting-started/store-details.md#store-email-addresses)를 식별합니다. 기본값: `General Contact` |
| [!UICONTROL Maximum Sent Emails Threshold] | 스토어 뷰 | 한 번에 보낼 수 있는 선물 레지스트리 공유 전자 메일 알림 메시지의 최대 수입니다. |

{style="table-layout:auto"}

## [!UICONTROL Gift Registry Update]

![선물 레지스트리 업데이트](./assets/gift-registry-gift-registry-update.png)<!-- zoom -->

<!-- [Gift Registry Update](https://docs.magento.com/user-guide/marketing/gift-registry-configure.html) -->

| 필드 | [범위](../../getting-started/websites-stores-views.md#scope-settings) | 설명 |
|--- |--- |--- |
| [!UICONTROL Email Template] | 스토어 뷰 | 선물 레지스트리에서 구매를 할 때 선물 레지스트리 소유자에게 전송되는 선물 레지스트리 업데이트 전자 메일에 사용되는 템플릿을 결정합니다. 업데이트에는 구매한 품목 및 수량에 대한 정보가 포함되지만 주문한 사람의 이름은 포함되지 않습니다. 기본 템플릿: `Gift Registry Update` |
| [!UICONTROL Email Sender] | 스토어 뷰 | 선물 레지스트리 업데이트 전자 메일의 보낸 사람으로 표시되는 [스토어 연락처](../../getting-started/store-details.md#store-email-addresses)를 식별합니다. 기본값: `General Contact` |

{style="table-layout:auto"}
