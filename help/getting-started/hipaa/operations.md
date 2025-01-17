---
title: 작업
description: HIPAA 지원 오퍼링으로 마이그레이션하고 문제 해결을 위해 보조 스테이징 환경을 사용하기 위한 지침
source-git-commit: 999d3126ae368000fc2c58c315473739012f3934
workflow-type: tm+mt
source-wordcount: '511'
ht-degree: 0%

---


# 작업

이 지침을 사용하여 Adobe Commerce용 HIPAA 지원 서비스로 마이그레이션하고 문제 해결을 위해 `staging_for_support` 환경을 사용하는 방법에 대해 알아보십시오.

## 마이그레이션

비 HIPAA Commerce 제품에서 HIPAA 지원 제품으로 마이그레이션하는 고객은 다음 지침을 준수해야 합니다.

1. **기존 데이터 공간 삭제**: 마이그레이션하기 전에 Adobe Commerce SaaS 계층에서 중요한 데이터와 중요하지 않은 데이터가 함께 혼합되지 않도록 기존 데이터 공간을 모두 삭제해야 합니다. 데이터 공간을 삭제하는 지원 티켓을 만듭니다.
1. **새 환경 구성**: 새 HIPAA Commerce 인스턴스의 [Commerce 서비스 커넥터](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/user-guides/integration-services/saas) 설정은 데이터 공간이 삭제된 후에만 구성해야 합니다. 새 HIPAA SaaS 환경은 이전 데이터 소스가 삭제된 후에만 사용해야 합니다. Commerce 서비스 커넥터를 설정하면 새 SaaS 데이터 공간 생성이 자동으로 트리거됩니다.
1. **마이그레이션 전략**: SaaS 데이터 공간의 삭제는 취소할 수 없는 프로세스이며 카탈로그 데이터 및 관련 구성을 모두 삭제합니다. 이전 데이터 또는 구성을 전달하려면 마이그레이션 전략이 적용되어 있어야 합니다. 이 전략은 상인의 책임이다. 기존 데이터 공간 삭제에 대한 지원 티켓은 마이그레이션 데이터 백업(해당되는 경우)이 수행된 후에만 만들어야 합니다.

>[!NOTE]
>기존 데이터 스페이스를 삭제하려면 고객이 &quot;HIPAA 마이그레이션: SaaS 데이터 스페이스 삭제&quot;라는 Adobe Commerce 지원 티켓을 만들고 `MAGEID`을(를) 제공하고 삭제해야 하는 SaaS 프로젝트 ID를 제공해야 합니다.

## Adobe Commerce 지원 관련 문제 해결

Adobe Commerce HIPAA 지원 서비스에는 문제 해결 목적으로 Adobe Commerce 지원 팀에서 사용할 수 있는 추가 `staging_for_support` 환경이 포함되어 있습니다.

고객은 `staging_for_support` 환경을 확인해야 합니다.

- PHI(Protected Health Information)와 같은 민감한 데이터를 포함하지 않습니다.
- 프로덕션 활동에는 사용할 수 없습니다.
- 혼동을 방지하기 위해 `staging_for_support`과(와) 다른 이름을 사용할 수 없습니다.
- 프로덕션 환경의 코드와 구성을 모두 사용하여 최신 상태로 유지함으로써 가능한 프로덕션에 가까운 환경에서 문제 해결을 수행할 수 있습니다.

## Commerce 서비스

- **비 HIPAA 지원 Commerce 서비스** - 고객은 HIPAA 지원 서비스가 아니므로 Live Search, Product Recommendations, Payment Services, Sales Channel 또는 Commerce Intelligence과 같은 Adobe Commerce 서비스를 사용하지 않아야 합니다. 고객은 [HIPAA 지원 서비스](overview.md)만 사용해야 합니다.

- **데이터 연결**—[데이터 연결](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/data-connection/overview) 확장 내의 백 오피스 컬렉터만 HIPAA가 준비되었습니다. 고객은 PHI를 상점 이벤트 및 Audience Activation과 같은 비 HIPAA 준비 데이터 연결 서비스로 보내지 말아야 합니다. 고객은 상점 데이터 수집이 비활성화되어 있는지 확인해야 합니다.

- **카탈로그 서비스**—기본적으로 [카탈로그 서비스](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/catalog-service/overview)는 PHI를 처리하지 않으므로 HIPAA 준비 감사 및 규정 준수 범위를 벗어납니다. 고객은 사용 사례에 대한 자체 평가와 법률 자문을 바탕으로 본 서비스를 사용하도록 할 책임이 있습니다. 또한 고객은 PHI를 비 HIPAA 지원 서비스로 전달할 위험을 방지하기 위해 페더레이션 서비스를 통해 카탈로그 서비스를 사용하면 안 됩니다.

- **SaaS 데이터 내보내기**—Adobe Commerce의 HIPAA 준비 구성 요소에 대한 데이터만 보내도록 [SaaS 데이터 내보내기](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/saas-data-export/overview) 서비스를 구성해야 합니다.
