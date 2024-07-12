---
title: Commerce용 Experience Manager Assets 통합
description: Experience Manager Assets을  [!DNL Commerce] 인스턴스와 통합하여 스토어에서 사용할 수 있는 수많은 미디어 자산에 액세스하는 방법에 대해 알아봅니다.
feature: CMS, Media, Configuration, Integration
source-git-commit: fafe8d46931cc00e58d0888639fd8e739a170f8a
workflow-type: tm+mt
source-wordcount: '459'
ht-degree: 0%

---

# Commerce용 Experience Manager Assets 통합

{{$include /help/_includes/aem-assets-integration-beta-note.md}}

Commerce과 Adobe Experience Manager(AEM) Assets 간의 통합은 AEM as a Digital Asset Management(DAM) 시스템의 강력한 기능과 Adobe Commerce을 결합하여 eCommerce 경험을 향상시킵니다. 이 통합은 AEM의 강력한 에셋 관리 기능을 활용하여 상거래 상점 전반에서 에셋을 원활하고 확장 가능하며 효율적으로 관리하고 제공할 수 있습니다.

**주요 기능**

- **중앙 집중식 자산 관리**

   - **AEM Assets as a Single Source of Truth**-AEM Assets은 모든 디지털 에셋에 대한 중앙 저장소 역할을 하여 모든 전자 상거래 플랫폼이 브랜드에서 승인된 에셋에 액세스할 수 있도록 합니다.

   - **일괄 에셋 관리**-조직은 AEM의 강력한 에셋 관리 기능 덕분에 대량의 에셋을 효율적으로 관리할 수 있습니다. 이를 통해 마케터와 머천다이저는 새 제품 라인에 대한 대규모 이미지 세트를 효율적으로 매핑할 수 있습니다.

- **개인화된 Commerce 경험**-AEM의 GenAI 서비스를 사용하여 조직은 개인화된 전자 상거래 경험에 대한 수백만 개의 제품 변형을 생성할 수 있습니다. 마케터와 머천다이저는 이러한 이미지를 사용하여 제품 출시 및 시즌 캠페인을 위한 동적 스토어를 만들 수 있으므로 참여도를 높이고 전환율을 높일 수 있습니다.

- **자동화된 자산 일치**-통합에는 SKU 또는 다른 주요 특성을 기반으로 AEM의 자산을 Adobe Commerce의 제품과 자동으로 일치시키는 규칙 엔진 서비스가 포함되어 있습니다. 이 서비스는 최신 제품 에셋 및 변형을 전자 상거래 상점 맨 앞에서도 항상 사용할 수 있도록 합니다. 또한 에셋을 관리하는 데 필요한 수작업이 줄어들어 보다 전략적인 활동에 시간을 할애할 수 있습니다.

- **간소화된 프로세스**
   - **Commerce 관리자에서 통합을 활성화하고 구성**-관리자와 개발자는 익숙한 도구 및 프로세스를 사용하여 Adobe Commerce에서 통합을 설치하고 구성할 수 있습니다.
   - **동적 업데이트**-자산 관리 시스템의 최신 변경 내용으로 제품 이미지를 최신 상태로 유지합니다. 이러한 자동 업데이트를 통해 상거래 상점 전면에는 항상 최신 제품 정보가 있습니다.
   - **효율적인 카탈로그 관리**-자산 정리 및 새로 고침을 자동화하여 제품 카탈로그를 간편하게 유지 관리할 수 있습니다.

## 통합을 활성화할 때 변경되는 사항

제품 목록 - 새 필드 [!UICONTROL Remote Media URL]

제품 세부 사항 페이지 - 변경 사항 없음. 단, 표시된 자산은 AEM DAM에서 가져옵니다.


## Commerce 및 Experience Manager Assets 통합

>[!BEGINSHADEBOX]

**필수 구성 요소**

- Adobe Commerce은 할당된 조직 ID를 사용하여 Adobe ID과 [Commerce Admin 통합](/help/getting-started/adobe-ims-config.md)을 통해 구성해야 합니다.
- Experience Manager Assets은 동일한 조직 ID에 제품으로 할당되어야 합니다.
- 통합을 구성하는 사용자는 Adobe Commerce 및 Experience Manager Assets에 액세스하려면 관리 권한이 있는 동일한 조직의 계정이 있어야 합니다.

>[!ENDSHADEBOX]


Experience Manager Assets과 Commerce 통합을 활성화하는 3단계 프로세스입니다.

1. [Commerce 자산을 관리하도록 Experience Manager Assets 프로젝트를 구성](aem-assets-configure-aem.md).

1. [Experience Manager Assets 통합 확장 설치 및 Adobe Commerce 구성](aem-assets-configure-aem.md)

1. [동기화 서비스 설정](aem-assets-setup-synchronization.md)

