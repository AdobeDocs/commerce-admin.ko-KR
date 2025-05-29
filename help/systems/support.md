---
title: 지원 도구
description: 시스템에서 문제를 식별하는 데 사용할 수 있는 제공된 지원 도구에 대해 알아봅니다.
exl-id: f67616e6-7879-4fd3-947a-16856f8447ba
badgePaas: label="PaaS만" type="Informative" url="https://experienceleague.adobe.com/ko/docs/commerce/user-guides/product-solutions" tooltip="Adobe Commerce 온 클라우드 프로젝트(Adobe 관리 PaaS 인프라) 및 온프레미스 프로젝트에만 적용됩니다."
source-git-commit: addde8c3e41b641712f5b08107c1d68b40cd4159
workflow-type: tm+mt
source-wordcount: '618'
ht-degree: 0%

---

# 지원 도구

{{ee-feature}}

지원 도구는 시스템의 알려진 문제를 식별하도록 설계되었습니다. 개발 및 최적화 프로세스 동안 리소스로 사용할 수 있으며, 지원 팀이 문제를 식별하고 해결하는 데 도움이 되는 진단 도구로 사용할 수 있습니다.

## 시스템 보고서

시스템 보고 도구를 사용하면 시스템의 스냅샷을 정기적으로 전체 또는 부분적으로 수행한 다음 나중에 참조할 수 있도록 저장할 수 있습니다. 코드 개발 주기 전후의 성능 설정 또는 서버 설정 변경 사항을 비교할 수 있습니다. 시스템 보고 도구를 사용하면 조사에 필요한 정보를 준비하고 제출하는 데 소요되는 시간을 크게 줄일 수 있습니다.

시스템 보고서 그리드에서 기존 보고서를 보고 다운로드하고, 보고서를 삭제하고, 보고서를 만들 수 있습니다.

### 시스템 보고서 액세스

_관리자_ 사이드바에서 **[!UICONTROL System]** > _[!UICONTROL Support]_>**[!UICONTROL System Report]**(으)로 이동합니다.

![관리자 - 시스템 보고서](./assets/reports.png){width="600" zoomable="yes"}

### 보고서 생성

1. **[!UICONTROL New Report]**&#x200B;을(를) 클릭합니다.

1. **[!UICONTROL Groups]** 목록에서 보고서에 포함할 각 정보 집합을 선택합니다. 기본적으로 모든 그룹이 선택됩니다.

   ![시스템 보고서 - 그룹 선택](./assets/report-create.png){width="600" zoomable="yes"}

1. 오른쪽 상단에서 **[!UICONTROL Create]**&#x200B;을(를) 클릭합니다.

   선택한 보고서 유형의 수에 따라 보고서가 생성되는 데 몇 분 정도 걸릴 수 있습니다. 보고서가 준비되면 생성된 날짜 및 시간과 함께 표 맨 위에 나타납니다.

### 모듈 정보 보기

설치된 모듈에 대한 유용한 정보를 찾을 수 있습니다.

**_설치된 각 모듈에 대한 보고서 정보를 보려면:_**

1. _관리자_ 사이드바에서 **[!UICONTROL System]** > _[!UICONTROL Support]_>**[!UICONTROL System Report]**(으)로 이동합니다.
1. **[!UICONTROL New Report]**&#x200B;을(를) 클릭합니다.
1. **[!UICONTROL Groups]** 목록에서 `Modules`을(를) 선택합니다.
1. **[!UICONTROL Create]**&#x200B;을(를) 클릭합니다.
1. 보고서가 생성되면 **[!UICONTROL Select]**&#x200B;을(를) 클릭한 다음 **[!UICONTROL View]**&#x200B;을(를) 클릭하여 모든 모듈 버전을 확인합니다.
1. 보고서를 다운로드하려면 **[!UICONTROL Download]**&#x200B;을(를) 클릭하십시오.

### 시스템 보고서 관리

그리드의 **[!UICONTROL Action]** 열에서 다음 중 하나를 선택합니다.

- `View` - 이 함수를 사용하여 보고서의 세부 정보를 봅니다.
- `Delete` - 이 함수를 사용하여 생성된 보고서를 목록에서 삭제합니다.
- `Download` - 이 함수를 사용하여 보고서를 HTML 파일로 저장합니다.

### 시스템 보고서 세부 정보 보기

1. 필요한 보고서에 대해 _[!UICONTROL Actions]_&#x200B;열에서&#x200B;**[!UICONTROL View]**&#x200B;을(를) 선택합니다.

1. 왼쪽 패널에서 보고서의 각 섹션을 ![확장 선택기](../assets/icon-display-expand.png)로 확장하여 세부 정보를 봅니다.

   ![일반 시스템 보고서 정보](./assets/report-information.png){width="600" zoomable="yes"}

### 사용 가능한 시스템 보고서

| 보고서 그룹 | 포함된 정보 |
| ------------ | -------------------- |
| [!UICONTROL General] | Adobe Commerce 버전<br>데이터 수<br>캐시 상태<br>인덱스 상태 |
| [!UICONTROL Environment] | 환경 정보<br>MySQL 상태 |
| [!UICONTROL Data] | URL 키별 중복 범주<br>URL 키별 중복 제품<br>SKU별 중복 제품<br>증분 Id별 중복 주문<br>전자 메일별 중복 사용자<br>손상된 범주 데이터 |
| [!UICONTROL Modules] | 사용자 지정 모듈 목록<br>비활성화된 모듈 목록<br>모든 모듈 목록 |
| [!UICONTROL Configuration] | 구성<br>`app/etc/env.php`<br>배송 방법<br>결제 방법<br>결제 기능 매트릭스의 데이터 |
| [!UICONTROL Logs] | 로그 파일<br>상위 시스템 메시지<br>오늘의 상위 시스템 메시지<br>상위 디버그 메시지<br>오늘의 상위 디버그 메시지<br>상위 예외 메시지<br>오늘의 상위 예외 메시지 |
| [!UICONTROL Attributes] | 사용자 정의 EAV 특성<br>새 EAV 특성<br>엔티티 유형<br>모든 EAV 특성<br>범주 EAV 특성<br>제품 EAV 특성<br>고객 EAV 특성<br>고객 주소 EAV 특성<br>RMA 항목 EAV 특성 |
| [!UICONTROL Events] | 사용자 지정 전역 이벤트<br>사용자 지정 관리 이벤트<br>사용자 지정 프런트 엔드 이벤트<br>사용자 지정 문서 이벤트<br>사용자 지정 Crontab 이벤트<br>사용자 지정 REST 이벤트<br>사용자 지정 SOAP 이벤트<br>핵심 전역 이벤트<br>핵심 관리 이벤트<br>핵심 프런트 엔드 이벤트<br>핵심 문서 이벤트<br>핵심 Crontab 이벤트<br>핵심 REST 이벤트<br>핵심 SOAP SOAP 이벤트<br>모든 전역 이벤트<br>모든 관리 이벤트<br>모든 프런트 엔드 이벤트<br>모든 Doc 이벤트<br>모든 REST 이벤트<br>모든 이벤트 이벤트<br>모든 Crontab 이벤트 |
| [!UICONTROL Cron] | 상태 코드별 Cron 일정<br>작업 코드별 Cron 일정<br>Cron 일정 큐의 오류<br>Cron 일정 목록<br>사용자 지정 글로벌 Cron 작업<br>사용자 지정 구성 가능한 Cron 작업<br>핵심 글로벌 Cron 작업<br>핵심 구성 가능한 Cron 작업<br>모든 글로벌 Cron 작업<br>모든 구성 가능한 Cron 작업 |
| [!UICONTROL Design] | Adminhtml 테마 목록<br>프론트엔드 테마 목록 |
| [!UICONTROL Stores] | 웹 사이트 트리<br>웹 사이트 목록<br>스토어 목록<br>스토어 보기 목록 |
| OMS 커넥터&#x200B;<br>_(OMS 통합에 표시됨)_ | 커넥터 버전<br>커넥터 모니터링<br>메시지 처리 결과 |

{style="table-layout:auto"}
