---
title: 크론(예약된 작업)
description: 관리자로부터 Commerce cron 작업의 실행 및 일정을 제어하는 방법을 알아봅니다.
exl-id: e0da08ab-212f-4977-9387-0b4b40560cfb
feature: System, Configuration
badgePaas: label="PaaS만" type="Informative" url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="Adobe Commerce 온 클라우드 프로젝트(Adobe 관리 PaaS 인프라) 및 온프레미스 프로젝트에만 적용됩니다."
source-git-commit: 9a68d9702cec9b812414d39e8d04c71751121a37
workflow-type: tm+mt
source-wordcount: '415'
ht-degree: 0%

---

# 크론(예약된 작업)

Adobe Commerce 및 Magento Open Source은 정기적으로 스크립트를 실행하여 예정된 대로 일부 작업을 수행합니다. 책임자로부터 Commerce cron 작업의 실행 및 일정을 제어할 수 있습니다. cron 일정에 따라 실행되는 저장소 작업에는 다음이 포함되지만 이에 국한되지는 않습니다.

- [이메일](email-communications.md)
- [카탈로그 가격 규칙](../merchandising-promotions/price-rules-catalog.md)
- [뉴스레터](../merchandising-promotions/newsletters.md)
- [XML 사이트 맵 생성](../merchandising-promotions/sitemap-xml.md)
- [환율 업데이트](../stores-purchase/currency-update.md)
- [Inventory management](../inventory-management/introduction.md)

>[!IMPORTANT]
>
>핵심 구성 요소와 일부 타사 확장이 예상대로 작동하는지 확인하려면 Commerce 서비스를 crontab에 설치해야 합니다. crontab에 서비스를 설치하는 방법에 대한 자세한 내용은 _설치 안내서_[&#128279;](https://experienceleague.adobe.com/docs/commerce-operations/installation-guide/next-steps/configuration.html)의 지침을 참조하십시오.

또한 cron 일정에 따라 실행되도록 다음을 구성할 수 있습니다.

- 시스템 그리드 업데이트 및 리인덱싱 주문
- 보류 중인 지급 수명

cron 작업 중에 생성된 URL이 정확하도록 저장소의 [기본 URL](../stores-purchase/store-urls.md)이(가) 올바르게 설정되어 있는지 확인하십시오. 클라우드 인프라의 Adobe Commerce에 대해서는 _Cloud Infrastructure의 Commerce 안내서_&#x200B;에서 [cron 작업 설정](https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/configure/app/properties/crons-property.html)을 참조하십시오. 온-프레미스의 경우 _구성 가이드_&#x200B;에서 [구성 및 실행 ](https://experienceleague.adobe.com/docs/commerce-operations/configuration-guide/cli/configure-cron-jobs.html)을(를) 참조하십시오.

## cron 구성

1. _관리자_ 사이드바에서 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**(으)로 이동합니다.

1. 왼쪽 패널에서 **[!UICONTROL Advanced]**&#x200B;을(를) 확장하고 **[!UICONTROL System]**&#x200B;을(를) 선택합니다.

1. **[!UICONTROL Cron]** 섹션에서 ![확장 선택기](../assets/icon-display-expand.png)를 확장합니다.

   ![고급 구성 - cron 작업](../configuration-reference/advanced/assets/system-cron.png){width="600" zoomable="yes"}

1. **[!UICONTROL Index]** 및 **[!UICONTROL Default]** 그룹에 대해 다음 설정을 완료하십시오.

   설정은 각 섹션에서 동일합니다.

   - **[!UICONTROL Generate Schedules Every]** - 일정이 생성되는 빈도(분)를 정의합니다. 일정은 데이터베이스에 저장됩니다.
   - **[!UICONTROL Schedule Ahead for]** - 사전 크론 작업이 예약되는 거리(분)를 정의합니다. 예를 들어 이 설정이 `10`(으)로 설정되고 cron이 실행되면 cron 작업이 다음 10분 동안 예약됩니다.
   - **[!UICONTROL Missed if not Run Within]** - 누락된 작업을 확인하는 데 사용되는 시간(분)을 정의합니다. cron 작업이 예약된 시간에 실행되지 않고 지정된 시간이 경과하면 실행할 수 없으며 상태가 `Missed`(으)로 설정됩니다.
   - **[!UICONTROL History Cleanup Every]** - 종료된 작업 기록을 데이터베이스에서 지우는 시간(분)을 정의합니다.
   - **[!UICONTROL Success History Lifetime]** - `Successful` 상태의 cron 작업 기록이 데이터베이스에 남아 있는 시간(분)을 정의합니다.
   - **[!UICONTROL Failure History Lifetime]** - `Error` 상태의 cron 작업 기록이 데이터베이스에 남아 있는 시간(분)을 정의합니다.
   - **[!UICONTROL Use Separate Process]** - 그룹의 모든 cron 작업이 별도의 시스템 프로세스에서 실행되는지 여부를 정의합니다. 옵션: `Yes` / `No`

   ![고급 구성 - 크론 그룹 인덱스](../configuration-reference/advanced/assets/system-cron-group-index.png){width="600" zoomable="yes"}

1. 완료되면 **[!UICONTROL Save Config]**&#x200B;을(를) 클릭합니다.
