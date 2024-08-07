---
title: 자산 동기화 활성화
description: Adobe Commerce 및 Experience Manager Assets 프로젝트를 연결하여 이러한 두 시스템 간에 에셋을 동기화하는 방법에 대해 알아봅니다.
feature: CMS, Media
exl-id: cc3ae56b-f1c8-4c96-a284-bcd726ce2bab
source-git-commit: 508e9e1d23a4b6e70ada22e2a22c0dcd401393a9
workflow-type: tm+mt
source-wordcount: '417'
ht-degree: 0%

---

# 자산 동기화 활성화

>[!BEGINSHADEBOX]

**필수 구성 요소**

- [Commerce 자산을 관리하도록 AEM Experience Manager Assets 구성](#aem-assets-configure-aem)
- [Commerce용 AEM Assets 통합을 설치하고 구성](#aem-assets-configure-commerce.md)하여 확장을 추가하고 확장을 사용하는 데 필요한 자격 증명과 연결을 생성합니다.

>[!ENDSHADEBOX]

이 지원 프로세스 중에 AEM 작성 환경에 대한 프로그램 및 환경 ID를 제공하여 테넌트 ID를 등록합니다. 이러한 ID는 연결 중인 AEM Assets 프로젝트를 식별하고 Commerce과 AEM Assets 간에 통신 및 워크플로우를 가능하게 하는 자격 증명을 제공합니다.

AEM 자산 프로젝트를 식별한 후 Adobe Commerce과 AEM Assets 간에 자산을 동기화하는 데 사용할 일치 규칙을 선택합니다.

Commerce용 AEM Assets 통합은 Adobe Commerce과 AEM Assets 간에 에셋을 동기화하는 두 개의 일치 규칙을 지원합니다.

- **제품별 일치 SKU**—제품의 SKU(Stock Keeping Unit)를 기반으로 하여 에셋과 일치하는 기본 일치 규칙입니다. SKU는 각 제품에 대한 고유 식별자입니다. 이 규칙은 에셋 메타데이터의 SKU를 Commerce 제품 SKU와 일치시켜 에셋이 올바른 제품과 연결되었는지 확인합니다.

- **사용자 지정 일치**—이 일치 규칙은 사용자 지정 일치 논리가 필요한 더 복잡한 시나리오 또는 특정 비즈니스 요구 사항에 사용됩니다. 이 규칙을 사용하려면 Adobe Developer App Builder에서 자산과 제품의 일치 방법을 정의하는 사용자 지정 코드가 구현되어야 합니다. 자세한 내용은 곧 제공될 예정입니다.

초기 온보딩의 경우 기본 `Match by product sku` 규칙을 사용합니다. 필요한 경우 나중에 일치 규칙을 변경할 수 있습니다.

## 통합 활성화

1. [AEM Assets 작성 환경](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/sites/authoring/quick-start)에 대한 프로젝트 및 환경 ID를 가져옵니다.

   1. AEM Sites 콘솔을 열고 **[!UICONTROL Assets]**&#x200B;을(를) 선택합니다.

   1. URL <br>`https://author-p[Program ID]-e[EnvironmentID].adobeaemcloud.com/`에서 프로젝트 및 환경 ID를 복사하여 저장합니다.

1. Commerce 관리자에서 AEM Assets 통합 구성을 엽니다.

   1. **[!UICONTROL Store]** > 구성 > **[!UICONTROL CATALOG]** > **[!UICONTROL Catalog]**&#x200B;을(를) 선택합니다.

   1. **[!UICONTROL Experience Manager Assets integration]** 확장.

      ![AEM Assets 통합을 통해 통합 사용](assets/aem-assets-integration-enable-config.png){width="600" zoomable="yes"}

1. **[!UICONTROL Program ID]** 및 **[!UICONTROL Environment ID]**&#x200B;을(를) 입력하여 연결할 Experience Manager Assets 프로젝트를 식별합니다.

1. **[[!UICONTROL Commerce integration]](aem-assets-configure-commerce.md#add-the-integration-to-the-commerce-environment)**(예: `Assets integration`)을(를) 선택하여 Adobe Commerce과 ARES 서비스 간의 API 요청을 인증하기 위해 OAUTH 자격 증명을 추가합니다.

1. Commerce에서 **[!UICONTROL Enable integration]**&#x200B;을(를) `Yes`(으)로 설정하여 AEM Assets에서 들어오는 업데이트를 수락하도록 허용합니다.

   통합을 활성화한 후 에셋 일치 규칙을 구성할 수 있습니다.

   ![AEM Assets 통합 자산 일치 규칙 선택](assets/aem-assets-config-matching-rule.png){width="600" zoomable="yes"}

1. 자산 동기화에 대한 일치 규칙을 정의합니다.

   1. **[!UICONTROL Match by product SKU]**&#x200B;을(를) 선택합니다.

   1. 예를 들어 **[!UICONTROL Match by product SKU attribute name]** 필드 `commerce:skus`에 Commerce 제품 SKU에 대해 정의된 [AEM Assets 메타데이터 필드 이름](aem-assets-configure-aem.md#configure-metadata)을(를) 추가합니다.

1. 구성을 적용하고 **[!UICONTROL Save Config]**&#x200B;을(를) 선택하여 동기화 프로세스를 시작합니다.
