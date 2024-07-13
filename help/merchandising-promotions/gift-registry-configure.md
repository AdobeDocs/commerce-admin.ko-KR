---
title: 선물 등록 구성
description: 선물 등록을 활성화하고 관련 이메일 알림을 구성하는 방법을 알아봅니다.
exl-id: 48193621-731d-4640-8ea8-5b201915cdf1
feature: Gift, Storefront, Configuration
source-git-commit: eb0fe395020dbe2e2496aba13d2f5c2bf2d0fc27
workflow-type: tm+mt
source-wordcount: '358'
ht-degree: 0%

---

# 선물 등록 구성

{{ee-feature}}

고객에게 선물 등록기를 제공하려면 먼저 선물 등록기를 활성화하고 관련 이메일 알림을 구성해야 합니다. Adobe Commerce은 선물 레지스트리 워크플로의 이벤트에 대한 응답으로 다음 이메일 알림을 보냅니다.

- 새 선물 레지스트리가 만들어지면 공유할 수 있는 레지스트리 링크가 있는 이메일이 소유자에게 전송됩니다.
- 선택적으로, 스토어는 선물 등록소 소유자의 친구 및 가족에게 선물 등록소에 대한 링크와 함께 통지를 보낼 수 있다.
- 소유자는 기프트 등록에서 품목을 구매하면 통지를 받지만 구매자를 나타내지는 않습니다.

Adobe Commerce에는 브랜드에 맞게 사용자 지정할 수 있는 이러한 각 이메일 메시지에 대한 사전 정의된 템플릿이 있습니다.

## 1단계. 선물 등록 활성화

1. _관리자_ 사이드바에서 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**(으)로 이동합니다.

1. 왼쪽 패널에서 **[!UICONTROL Customers]**&#x200B;을(를) 확장하고 **[!UICONTROL Gift Registry]**&#x200B;을(를) 선택합니다.

1. **[!UICONTROL General Options]** 섹션에서 ![확장 선택기](../assets/icon-display-expand.png)를 확장하고 다음을 수행합니다.

   ![고객 구성 - 선물 레지스트리 일반](../configuration-reference/customers/assets/gift-registry-general-options.png){width="600" zoomable="yes"}

   - 선물 레지스트리는 기본적으로 활성화되어 있습니다. 필요한 경우 **[!UICONTROL Enable Gift Registry]**&#x200B;을(를) `Yes`(으)로 설정합니다.

   - **[!UICONTROL Maximum Registrants]**&#x200B;의 경우 선물 등록 이벤트에 참여하도록 초대할 수 있는 최대 인원을 입력하십시오.

## 2단계. 이메일 알림 구성

1. **[!UICONTROL Owner Notification]** 섹션에서 ![확장 선택기](../assets/icon-display-expand.png)를 확장하고 다음을 수행합니다.

   ![고객 구성 - 선물 레지스트리 소유자 알림](../configuration-reference/customers/assets/gift-registry-owner-notification.png){width="600" zoomable="yes"}

   - 등록을 만들 때 선물 레지스트리 소유자에게 알리는 **[!UICONTROL Email Template]**&#x200B;을(를) 선택하십시오.

   - 메시지의 **[!UICONTROL Email Sender]**(으)로 표시되는 [연락처 저장](../getting-started/store-details.md#store-email-addresses)을(를) 선택하십시오.

1. **[!UICONTROL Gift Registry Sharing]** 섹션에서 ![확장 선택기](../assets/icon-display-expand.png)를 확장하고 다음을 수행합니다.

   ![고객 구성 - 선물 레지스트리 공유](../configuration-reference/customers/assets/gift-registry-gift-registry-sharing.png){width="600" zoomable="yes"}

   - 레지스트리를 받는 사람과 공유할 때 선물 레지스트리 받는 사람에게 알리는 **[!UICONTROL Email Template]**&#x200B;을(를) 선택하십시오.

   - 메시지의 **[!UICONTROL Email Sender]**(으)로 표시되는 스토어 식별을 선택합니다.

   - **[!UICONTROL Maximum Sent Emails Threshold]**&#x200B;의 경우 한 번에 보낼 수 있는 최대 전자 메일 수를 입력합니다.

1. **[!UICONTROL Gift Registry Update]** 섹션에서 ![확장 선택기](../assets/icon-display-expand.png)를 확장하고 다음을 수행합니다.

   ![고객 구성 - 선물 레지스트리 업데이트](../configuration-reference/customers/assets/gift-registry-gift-registry-update.png){width="600" zoomable="yes"}

   - 레지스트리에 대한 변경 내용을 선물 레지스트리 소유자에게 알리는 **[!UICONTROL Email Template]**&#x200B;을(를) 선택하십시오.

   - 메시지의 **[!UICONTROL Email Sender]**(으)로 표시되는 스토어 식별을 선택합니다.

1. 완료되면 **[!UICONTROL Save Config]**&#x200B;을(를) 클릭합니다.

1. 메시지가 표시되면 캐시를 업데이트합니다.

   캐시를 새로 고치면 선물 레지스트리가 기타 설정 아래의 저장소 메뉴에 나타나고 고객 계정에서 사용할 수 있게 됩니다.
