---
title: 제품 경고
description: 제품 경고와 이를 사용하여 고객에게 제품의 재고 상태 및 가격 변화에 대해 알리는 방법에 대해 알아봅니다.
exl-id: c9f736c5-7bba-4e3e-804d-5b0fe52c8f9b
feature: Inventory, Configuration
source-git-commit: 4d89212585fa846eb94bf83a640d0358812afbc5
workflow-type: tm+mt
source-wordcount: '648'
ht-degree: 0%

---

# 제품 경고

고객은 이메일로 가격 변경 경고와 재고 경고, 이렇게 두 가지 유형의 경고를 구독할 수 있습니다. 각 경고 유형에 대해 고객이 구독할 수 있는지 확인하고, 사용된 이메일 템플릿을 선택하고, 이메일 발신자를 식별할 수 있습니다.

![제품 경고에 등록](assets/product-alert-setting.png){width="600" zoomable="yes"}

## 가격 변경 경고

가격 변경 알림을 사용하도록 설정하면 모든 제품 페이지에 _가격 하락 시 알림_ 링크가 나타납니다. 고객은 링크를 클릭하여 제품과 관련된 경고를 구독할 수 있습니다. 스토어에 계정을 만들라는 메시지가 나타납니다. 가격이 변경되거나 제품이 특별 광고될 때마다 경고를 구독한 모든 사용자에게 이메일 알림이 전송됩니다.

## 재고 내 경고

재고 경고는 _이 제품이 재고가 있을 때 알림_&#x200B;이라는 링크를 만듭니다. 재고가 없는 모든 제품에 대해 이 제품이 재고가 있을 때 알림이 표시됩니다. 고객은 링크를 클릭하여 경고를 구독할 수 있습니다. 제품이 재입고되면 고객은 제품을 사용할 수 있다는 이메일 알림을 받게 됩니다. 경고가 있는 제품에는 경고를 구독한 고객을 나열하는 제품 정보 패널의 _제품 경고_ 탭이 있습니다.

![제품 및 가격 경고 구독 목록](assets/inventory-product-alerts.png){width="600" zoomable="yes"}

## 제품 경고 설정

1. _관리자_ 사이드바에서 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**(으)로 이동합니다.

1. 왼쪽 패널에서 **[!UICONTROL Catalog]**&#x200B;을(를) 확장하고 아래의 **[!UICONTROL Catalog]**&#x200B;을(를) 선택합니다.

1. _[!UICONTROL Product Alerts]_섹션을 확장하려면 클릭하고 다음을 수행합니다.

   ![제품 알림](assets/config-catalog-product-alerts.png){width="600" zoomable="yes"}

   - 가격 변경 알림을 고객에게 제공하려면 **[!UICONTROL Allow Alert When Product Price Changes]**&#x200B;을(를) `Yes`(으)로 설정하십시오.

   - 가격 알림 알림에 사용할 서식 파일로 **[!UICONTROL Price Alert Email Template]**&#x200B;을(를) 설정합니다.

   - 품절된 제품을 다시 사용할 수 있게 되면 알림을 제공하려면 **[!UICONTROL Allow Alert When Product Comes Back in Stock]**&#x200B;을(를) `Yes`(으)로 설정하십시오.

     >[!NOTE]
     >
     >_이 제품의 재고가 있을 때 알림_ 메시지는 **[!UICONTROL Display Out of Stock Products]**&#x200B;이(가) `Yes`(으)로 설정된 경우에만 나타납니다([!UICONTROL Catalog] > [!UICONTROL Inventory]의 구성에서).

   - 제품 재고 알림에 사용할 서식 파일로 **[!UICONTROL Stock Alert Email Template]**&#x200B;을(를) 설정합니다.

   - 전자 메일 경고를 보낸 사람으로 표시하려는 [스토어 연락처](../getting-started/store-details.md#store-email-addresses){target="_blank"}(으)로 **[!UICONTROL Alert Email Sender]**&#x200B;을(를) 설정합니다. 핵심 사용 안내서에서 [전자 메일 주소 저장](../configuration-reference/general/store-email-addresses.md){target="_blank"}에 대해 자세히 알아보세요.

1. 완료되면 **[!UICONTROL Save Config]**&#x200B;을(를) 클릭합니다.

## 제품 경고 이메일 템플릿 구성

다음으로, 가격 알림에 대한 이메일 템플릿을 구성, 추가 또는 수정합니다. 추가 템플릿을 만든 후 가격 경고 구성을 편집할 수 있습니다.

전자 메일 메시지 사용에 대한 자세한 내용은 _관리 시스템 안내서_&#x200B;의 [메시지 템플릿](../systems/email-template-custom.md#message-templates)을 참조하세요.

1. _관리자_ 사이드바에서 **[!UICONTROL Marketing]** > _[!UICONTROL Communications]_>**[!UICONTROL Email Templates]**(으)로 이동합니다.

1. **[!UICONTROL Add New Template]**&#x200B;을(를) 클릭합니다.

1. _기본 템플릿 로드_&#x200B;에서 사용자 지정할 **[!UICONTROL Template]**&#x200B;을(를) 선택합니다.

   테마에 포함된 경고 템플릿을 선택할 수 있습니다. 또는 _[!UICONTROL Magento_PriceAlert]_에서 `Price Alert` 또는 `Stock Alert` 템플릿을 선택할 수 있습니다.

1. **[!UICONTROL Load Template]**&#x200B;을(를) 클릭합니다.

1. **[!UICONTROL Template Name]** 입력.

   _가격 알림_ 구성에서 이 이름을 선택할 수 있습니다.

1. 기존 콘텐츠를 읽고 필요에 따라 다음 사항을 변경합니다.

   | 필드 | 설명 |
   | ----- | ----- |
   | [!UICONTROL Template Subject] | 이 텍스트는 이메일의 제목 줄에 표시됩니다. |
   | [!UICONTROL Template Content] | 이 텍스트는 보낸 이메일의 전체 콘텐츠에 표시됩니다. |

1. [!DNL Commerce] 데이터에서 생성된 정보를 추가하려면 **[!UICONTROL Insert Variable]** 옵션을 사용하여 사용 가능한 변수 목록을 사용하십시오.

1. **[!UICONTROL Save Template]**&#x200B;을(를) 클릭합니다.

## 제품 경고 실행 설정

이러한 설정을 통해 경고를 전송해야 하는 변경 내용을 [!DNL Commerce]에서 확인하는 빈도를 선택할 수 있습니다. 경고 전송이 실패하면 전송되는 이메일의 수신자, 발신자 및 템플릿을 선택할 수도 있습니다.

![제품 경고 실행 설정](assets/config-catalog-product-alerts-run-settings.png){width="600" zoomable="yes"}

1. _관리자_ 사이드바에서 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**(으)로 이동합니다.

1. 왼쪽 패널에서 **[!UICONTROL Catalog]**&#x200B;을(를) 확장하고 아래의 **[!UICONTROL Catalog]**&#x200B;을(를) 선택합니다.

1. **[!UICONTROL Product Alerts Run Settings]** 섹션에서 ![확장 선택기](../assets/icon-display-expand.png)를 확장합니다.

1. 제품 경고를 보내는 빈도를 확인하려면 **[!UICONTROL Frequency]**&#x200B;을(를) 다음 중 하나로 설정하십시오.

   - `Daily`
   - `Weekly`
   - `Monthly`

1. 제품 경고를 보내는 시간을 결정하려면 **[!UICONTROL Start Time]**&#x200B;을(를) 시간, 분, 초로 설정하십시오.

   >[!NOTE]
   >
   >제품 경고는 &quot;product_alert&quot; 소비자가 전송합니다.

1. **[!UICONTROL Error Email Recipient]**&#x200B;의 경우 오류가 발생하면 연락할 사람의 전자 메일을 입력하십시오.

1. **[!UICONTROL Error Email Sender]**&#x200B;에 대해 오류 알림을 보낸 사람으로 표시되는 저장소 ID를 선택하십시오.

1. 오류 알림에 사용할 트랜잭션 전자 메일 템플릿에 **[!UICONTROL Error Email Template]**&#x200B;을(를) 설정합니다.

1. 완료되면 **[!UICONTROL Save Config]**&#x200B;을(를) 클릭합니다.
