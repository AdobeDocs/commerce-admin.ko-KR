---
title: '[!UICONTROL Sales Channels] &gt; [!UICONTROL Global Settings]'
description: Commerce 관리자의 [!UICONTROL Sales Channels] &gt; [!UICONTROL Global Settings] 페이지에서 구성 설정을 검토하십시오.
exl-id: 28a5ef4b-265e-457a-9480-96763785b5fd
feature: Configuration, Sales Channels
source-git-commit: b710c0368dc765e3bf25e82324bffe7fb8192dbf
workflow-type: tm+mt
source-wordcount: '234'
ht-degree: 0%

---

# [!UICONTROL Sales Channels] > [!UICONTROL Global Settings]

{{config}}

이러한 설정은 [[!DNL Amazon Sales Channel]](https://experienceleague.adobe.com/docs/commerce-channels/amazon/getting-started/install.html)을(를) 설치할 때 사용할 수 있습니다.

![Sales Channel 설정](./assets/config-sales-channel-global-settings.png)<!-- zoom -->

| 필드 | [범위](../getting-started/websites-stores-views.md#scope-settings) | 설명 |
|-----|---------|------|
| [!UICONTROL Clear Log History] | 글로벌 | 옵션:<br/><br/>**`Once Daily`**: 매일 한 번 스토어의 활동 내역을 지우려면 이 옵션을 선택하십시오.<br/><br/>**`Once Weekly`**: 매주 한 번 스토어의 활동 내역을 지우려면 이 옵션을 선택하십시오.<br/><br/>**`Once Monthly`**: (기본값) 매월 한 번 스토어의 활동 내역을 지우려면 이 옵션을 선택하십시오. |
| [!UICONTROL Background Tasks (CRON) Source] | 글로벌 | [!DNL Amazon Sales Channel]이(가) Amazon Seller Central과의 통신 및 데이터 동기화 간격을 결정할 때 Commerce 크론 설정을 사용하도록 지정하려면 `Magento CRON`을(를) 선택하십시오. |
| [!UICONTROL Enable Debug Logging] | 글로벌 | 문제 해결이 필요할 때 추가 동기화 데이터를 수집하려면 `Enabled`을(를) 선택하십시오.<br/><br/>이 옵션은 기본적으로 사용하지 않도록 설정되어 있으며, 계속 로깅하면 성능에 부정적인 영향을 주므로 문제 해결을 위해 필요할 때만 사용해야 합니다. 문제 해결을 위해 활성화된 경우 완료될 때 비활성화되어야 합니다.<br/><br/>**_참고&#x200B;_**: Amazon Sales Channel 로깅은 `/var/log/channel_amazon.log` 파일에 기록되며 [개발자 모드](../systems/developer-tools.md#operation-modes)에서 볼 수 있습니다. |
| [!UICONTROL Read-Only Mode] | 글로벌 | 나가는 모든 상태 변경 API 요청을 차단하려면 `Enabled`을(를) 선택하세요. 읽기 전용 모드가 비활성화될 때까지 잠재적 변경 사항은 저장되지만 전송되지 않습니다. 데이터 전송을 다시 시작하려면 `Disabled`을(를) 선택하십시오.<br/><br/>데이터베이스가 인스턴스의 새 복사본으로 마이그레이션되면(저장소의 URL이 구성에서 변경될 때 검색됨) 읽기 전용 모드가 자동으로 활성화됩니다.<br/><br/>프로덕션 인스턴스의 복사본에 사용하도록 디자인되었습니다(예: _스테이징_ 또는 _QA_). 프로덕션 인스턴스에서는 사용할 수 없습니다.<br/><br/>**_참고&#x200B;_**: [!UICONTROL Read-Only Mode]을(를) 사용하려면 구성 캐시를 지워야 합니다. |

{style="table-layout:auto"}
