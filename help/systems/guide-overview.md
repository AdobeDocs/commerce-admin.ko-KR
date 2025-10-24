---
title: 관리 시스템 안내서
description: Commerce 스토어를 보호하고 권한을 관리하는 최상의 보안 사례와 데이터 가져오기 및 내보내기, 통합 및 확장 기능 관리, 반복적인 유지 관리 처리 방법을 알아보십시오.
exl-id: 9d22571e-9e09-4d1a-ba55-a889f094158d
source-git-commit: 0cda54e8d52a866151658573c6d2ace1820dab75
workflow-type: tm+mt
source-wordcount: '418'
ht-degree: 7%

---

# Adobe Commerce 관리 시스템 안내서

이 안내서는 Adobe Commerce 및 Magento Open Source 관리에서 작업하는 시스템 관리자 및 통합자를 위한 것입니다. 전자 상거래 비즈니스를 위해 여러 조직 기능에서 활동을 지원하는 관리 보안, 유지 관리 작업 및 시스템 전체 리소스에 대한 자세한 정보를 제공합니다. 핵심 Commerce 구성 및 기능에 대한 기본적인 이해를 전제로 합니다.

이 안내서에서는 다음 주제를 다룹니다.

| 제목 | 설명 |
| ------- | ----------- |
| [소개](introduction.md) | Commerce 인스턴스 내 시스템 및 통합 기능 개요 |
| [시스템 메뉴](system-menu.md) | 데이터 가져오기 및 내보내기, 시스템 캐시 및 인덱스 관리, 사용자 계정 및 권한 관리, 백업, 시스템 알림 및 사용자 지정 변수에 대한 도구에 액세스하려면 [!UICONTROL System] 메뉴를 사용하십시오. |
| [관리자 계정 및 권한](permissions.md) | 저장소 기능에 대한 액세스 권한을 부여하는 데 사용되는 관리자 사용자 계정 및 역할을 관리합니다. |
| [변수](variables-predefined.md) | 변수를 사용하면 이메일 및 뉴스레터 템플릿과 사이트 및 고객 경험을 지원하는 기타 유형의 콘텐츠를 손쉽게 개인화할 수 있습니다. |
| [전자 메일 템플릿](email-templates.md) | 이메일 템플릿은 스토어에서 전송되는 자동화된 메시지의 레이아웃, 콘텐츠 및 형식을 정의합니다. 각 트랜잭션 이메일은 특정 유형의 트랜잭션 또는 이벤트와 연결되므로 트랜잭션 이메일이라고 합니다. |
| [데이터 전송](data-transfer.md) | <ul><li>가져오기 및 내보내기 도구를 사용하면 한 번의 작업으로 여러 레코드를 관리할 수 있습니다. 새 항목을 가져올 수 있을 뿐만 아니라 기존 제품 세트를 업데이트, 대체 및 삭제할 수도 있습니다.</li><li>[[!UICONTROL Data Management Dashboard]](data-dashboard.md)에서 연결된 Commerce 서비스로 전송된 엔터티의 데이터 동기화 상태를 봅니다.</li><li>[[!UICONTROL Data Export Feed Sync Status]](data-feed-sync-status.md) 페이지에서 Commerce SaaS 서비스로 데이터 피드 내보내기에 대한 동기화 상태를 모니터링합니다.</li></ul> |
| [작업 로그](action-log.md) | Adobe Commerce의 경우 작업 로그는 스토어에서 작업하는 관리 사용자가 수행한 모든 변경 사항을 캡처합니다. 이를 통해 스토어에 대한 모든 변경 사항을 추적할 수 있습니다. |
| 도구 | [!BADGE PaaS만]{type=Informative url="https://experienceleague.adobe.com/ko/docs/commerce/user-guides/product-solutions" tooltip="Adobe Commerce 온 클라우드 프로젝트(Adobe 관리 PaaS 인프라) 및 온프레미스 프로젝트에만 적용됩니다."} 시스템 관리자에게는 사용 가능한 도구 모음이 있습니다. [지원 도구](support.md)는 시스템의 알려진 문제를 식별하도록 설계되었습니다. 시스템 도구는 일상적인 [index](index-management.md) 및 [cache](cache-management.md) 관리를 수행하고, [시스템을 백업하고](backups.md)예약된 작업을 관리하고[하며, &#x200B;](data-scheduled-import-export.md)개발자 도구[의 집합을 사용할 수 있도록 운영 지원을 제공합니다.](developer-tools.md) |
| [통합](integrations.md) | OAuth 자격 증명의 위치를 설정하고 서드파티 통합을 위한 리디렉션 URL을 제공합니다. |
| [보안](security.md) | 저장소 및 데이터의 보안을 유지하는 데 사용할 수 있는 도구 및 손상을 감지하는 경우 보안 작업 계획에 대한 지침에 대해 알아봅니다. |

{style="table-layout:auto"}

## 사용 가능한 설명서

{{docs-links}}
