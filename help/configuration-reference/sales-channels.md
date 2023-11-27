---
title: '[!UICONTROL Sales Channels] &gt; [!UICONTROL Global Settings]'
description: 에서 구성 설정을 검토합니다. [!UICONTROL Sales Channels] &gt; [!UICONTROL Global Settings] 상거래 관리자의 페이지입니다.
exl-id: 28a5ef4b-265e-457a-9480-96763785b5fd
feature: Configuration, Sales Channels
source-git-commit: 76bd1b1af9b55d69bd98209d70fb5518f190a3e1
workflow-type: tm+mt
source-wordcount: '243'
ht-degree: 0%

---

# [!UICONTROL Sales Channels] > [!UICONTROL Global Settings]

{{config}}

이러한 설정은 다음과 같은 경우에 사용할 수 있습니다. [[!DNL Amazon Sales Channel]](https://experienceleague.adobe.com/docs/commerce-channels/amazon/getting-started/install.html) 이(가) 설치되었습니다.

![Sales Channel 설정](./assets/config-sales-channel-global-settings.png)<!-- zoom -->

| 필드 | [범위](../getting-started/websites-stores-views.md#scope-settings) | 설명 |
|-----|---------|------|
| [!UICONTROL Clear Log History] | 글로벌 | 옵션:<br/><br/>**`Once Daily`**: 이 옵션을 선택하면 스토어의 활동 내역이 매일 한 번 지워집니다.<br/><br/>**`Once Weekly`**: 매주 한 번 스토어의 활동 내역을 지우려면 이 옵션을 선택합니다.<br/><br/>**`Once Monthly`**: (기본값) 매월 한 번씩 스토어의 활동 내역을 지우려면 이 옵션을 선택합니다. |
| [!UICONTROL Background Tasks (CRON) Source] | 글로벌 | 선택 `Magento CRON` 을(를) 지정하기 위해 [!DNL Amazon Sales Channel] 는 상거래 크론 설정을 사용하여 Amazon Seller Central과의 통신 및 데이터 동기화 간격을 결정합니다. |
| [!UICONTROL Enable Debug Logging] | 글로벌 | 선택 `Enabled` 문제 해결이 필요할 때 추가 동기화 데이터를 수집하기 위해<br/><br/>이 옵션은 기본적으로 비활성화되어 있으며 계속 로깅하면 성능에 부정적인 영향을 주므로 문제 해결을 위해 필요한 경우에만 활성화해야 합니다. 문제 해결을 위해 활성화된 경우 완료될 때 비활성화되어야 합니다.<br/><br/>**_참고&#x200B;_**: Amazon Sales Channel 로깅이 `/var/log/channel_amazon.log` 에서 볼 수 있는 파일 [개발자 모드](../systems/developer-tools.md#operation-modes). |
| [!UICONTROL Read-Only Mode] | 글로벌 | 선택 `Enabled` 나가는 모든 상태 변경 API 요청을 차단합니다. 읽기 전용 모드가 비활성화될 때까지 잠재적 변경 사항은 저장되지만 전송되지 않습니다. 데이터 전송을 다시 시작하려면 다음을 선택합니다. `Disabled`.<br/><br/>데이터베이스가 인스턴스의 새 복사본으로 마이그레이션되면(저장소의 URL이 구성에서 변경될 때 검색됨) 읽기 전용 모드가 자동으로 활성화됩니다.<br/><br/>다음과 같은 프로덕션 인스턴스의 복사본에 사용하도록 설계되었습니다. _스테이징_ 또는 _QA_, 및 는 프로덕션 인스턴스에서 사용해서는 안 됩니다.<br/><br/>**_참고&#x200B;_**: 구성 캐시를 지워야 합니다. [!UICONTROL Read-Only Mode] 활성화하려면 다음을 수행하십시오. |

{:style=&quot;table-layout:auto&quot;}
