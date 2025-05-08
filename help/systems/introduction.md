---
title: 관리 시스템 소개
description: 스토어 관리자가 사이트, 데이터, 통합 및 관리 사용자를 효과적으로 관리하는 데 사용할 수 있는 시스템 도구 및 기능에 대해 알아봅니다.
exl-id: 52792a89-8f6f-4230-9a04-e193b3943410
source-git-commit: 51c8b526e1f03e65ad71eb00ec3cdf82365bd33c
workflow-type: tm+mt
source-wordcount: '416'
ht-degree: 0%

---

# 관리 시스템 소개

저장소 관리자는 판매자가 제품 및 판촉을 설정하고 주문을 관리하며 기타 관리 작업을 수행하는 안전한 백오피스입니다. 모든 기본 구성 작업 및 저장소 관리 작업은 관리자로부터 수행됩니다. 관리자가 조직을 위해 관리할 수 있는 여러 스토어 기능을 지원하는 기능도 있습니다.

## 변수 및 고객 커뮤니케이션

변수는 한 번 만들어 여러 위치에서 사용할 수 있는 정보입니다. 스토어에는 [전자 메일](email-templates.md) 및 [뉴스레터](../merchandising-promotions/newsletter-template.md) 템플릿, 기타 유형의 [콘텐츠](../content-design/introduction.md#content)을(를) 개인화하는 데 쉽게 사용할 수 있는 사전 정의된 여러 변수가 포함되어 있습니다. 사용자 지정 변수를 만들어 요구 사항에 맞는 정보를 통합할 수도 있습니다.

- [사전 정의된 변수](variables-predefined.md)
- [사용자 지정 변수](variables-custom.md)

스토어를 시작하기 전에 완료해야 하는 작업 중 하나는 스토어에서 보낸 모든 통신에 사용되는 이메일 템플릿을 검토하여 브랜드가 반영되었는지 확인하는 것입니다. 여기에는 전자 메일 및 [뉴스레터 템플릿](../merchandising-promotions/newsletter-template.md), PDF 송장 및 포장 명세서 사용자 지정이 포함됩니다. 또한 변수와 [마크업 태그](markup-tags.md)를 사용하여 콘텐츠를 개인화하는 작업도 포함됩니다.

## 운영 관리

관리자는 또한 시스템 관리자가 조직 내에서 관리자 사용자를 관리하고 스토어를 운영할 수 있도록 다양한 작업을 지원합니다. 여기에는 다음 도구가 포함됩니다.

- **관리자 사용자 계정 및 권한** - 관리자의 사이트 및 기능 영역에 대한 액세스를 제어하는 연결된 [역할 및 권한](permissions-user-roles.md)뿐만 아니라 관리자 [사용자 계정](permissions-users-all.md)을 관리합니다.
- **관리 세션 및 웹 사이트 제한** - [보안](security.md) 모범 사례를 검토하고 관리 세션 및 자격 증명을 관리하고 CAPTCHA를 구현하며 웹 사이트 제한을 관리하는 방법을 알아봅니다.
- **시스템 도구** - 일상적인 [인덱스](index-management.md) 및 [캐시](cache-management.md) 관리 작업을 수행하고, 시스템을 [백업](backups.md)하고, [예약된 작업을 관리하고](data-scheduled-import-export.md)하며, [개발자 도구](developer-tools.md) 집합을 사용합니다.
- **데이터 전송** - [데이터 전송](data-transfer.md) 도구를 사용하여 데이터를 가져오고 내보내고 제품, 가격, 고객 및 세율 데이터를 관리합니다.
- **통합** - [타사 통합](integrations.md)에 대한 OAuth 자격 증명 및 리디렉션 URL의 위치를 설정하고 사용 가능한 API 리소스를 식별합니다.
- **작업 로그** - ![Adobe Commerce](../assets/adobe-logo.svg)(Adobe Commerce만 해당) 스토어에서 작업 중인 관리 사용자가 변경한 사항에 대한 레코드([작업 로그](action-log.md))에 액세스합니다.
- **지원 도구** - ![Adobe Commerce](../assets/adobe-logo.svg)(Adobe Commerce 전용) [시스템 보고서](support.md#access-system-reports)는 시스템의 알려진 문제를 식별하도록 설계되었습니다. 개발 및 최적화 프로세스 동안 리소스로 사용할 수 있으며, 지원 팀이 문제를 식별하고 해결하는 데 도움이 되는 진단 도구로 사용할 수 있습니다.
