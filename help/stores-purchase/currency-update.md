---
title: 환율 업데이트
description: 환율을 수동으로 설정하거나 스토어로 가져오는 방법에 대해 알아봅니다.
exl-id: 316a7bc8-1118-46e7-82ff-891ada04cd13
feature: Currency, Configuration, Data Import/Export
source-git-commit: 370131cd73a320b04ee92fa9609cb24ad4c07eca
workflow-type: tm+mt
source-wordcount: '273'
ht-degree: 0%

---

# 환율 업데이트

환율은 수동으로 설정하거나 스토어로 가져올 수 있습니다. 스토어에서 최신 환율을 사용하도록 하려면 일정에 따라 통화 환율을 자동으로 업데이트하도록 구성할 수 있습니다.

환율을 가져오기 전에 다음을 완료하십시오. [통화 환율 설정](currency-configuration.md) 를 사용하여 수락할 통화를 지정하고 가져오기 연결 및 일정을 설정합니다.

![통화 환율](./assets/stores-currency-rate-update.png){width="600" zoomable="yes"}

## 수동으로 환율 업데이트

1. 다음에서 _관리자_ 사이드바, 이동 **[!UICONTROL Stores]** > _[!UICONTROL Currency]_>**[!UICONTROL Currency Rates]**.

1. 변경할 환율을 클릭하고 지원되는 각 통화에 대한 새 값을 입력합니다.

1. 완료되면 다음을 클릭하십시오. **[!UICONTROL Save Currency Rates]**.

## 환율 가져오기

1. 다음에서 _관리자_ 사이드바, 이동 **[!UICONTROL Stores]** > _[!UICONTROL Currency]_>**[!UICONTROL Currency Rates]**.

1. 설정 **[!UICONTROL Import Service]** 통화 환율 공급자에 문의하십시오.

   기본 공급자는 입니다. `fixer.io (legacy)`.

   >[!IMPORTANT]
   >
   >2.4.6 릴리스부터 [[!DNL Fixer.io]](https://fixer.io/) 서비스는 더 이상 사용되지 않으며 [[!DNL Fixer API] (APILayer)](https://apilayer.com/marketplace/fixer-api) 서비스. 더 이상 사용되지 않는 계정 대신 APILayer 계정을 사용하는 것이 좋습니다 [!DNL Fixer.io] 계정입니다.

1. 클릭 **[!UICONTROL Import]**.

   업데이트된 요금은 다음에 표시됩니다. _[!UICONTROL Currency Rates]_목록을 표시합니다. 마지막 업데이트 이후 요금이 변경된 경우 이전 요금이 참조용으로 아래에 표시됩니다.

1. 완료되면 다음을 클릭하십시오. **[!UICONTROL Save Currency Rates]**.

1. 캐시를 업데이트하라는 메시지가 표시되면 **[!UICONTROL Cache Management]** 잘못된 캐시를 연결하고 새로 고칩니다.

   ![시스템 메시지 - 잘못된 캐시를 새로 고칩니다.](./assets/currency-cache-update.png){width="600" zoomable="yes"}

## 일정에 따라 통화 환율 가져오기

1. 다음을 확인합니다. [크론](../systems/cron.md) 이(가) 귀하의 스토어에 대해 활성화되었습니다.

1. 수락할 통화를 지정하고 가져오기 연결 및 일정을 설정하려면 다음을 완료하십시오. [통화 환율 설정](currency-configuration.md).

1. 요금을 일정에 따라 가져오는지 확인하려면 다음을 확인하십시오. _[!UICONTROL Currency Rates]_목록을 표시합니다.

1. 일정에 대해 설정된 빈도 설정의 기간을 기다렸다가 요금을 다시 확인합니다.
