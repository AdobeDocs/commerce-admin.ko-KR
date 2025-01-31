---
title: 자산 동기화 활성화
description: Adobe Commerce 및 Experience Manager Assets 프로젝트를 연결하여 이러한 두 시스템 간에 에셋을 동기화하는 방법에 대해 알아봅니다.
feature: CMS, Media
exl-id: cc3ae56b-f1c8-4c96-a284-bcd726ce2bab
source-git-commit: e9b3ede8945de0a6ed0cdb02e5675d736764d3e4
workflow-type: tm+mt
source-wordcount: '383'
ht-degree: 0%

---

# 자산 동기화 활성화

지원 프로세스 중에 AEM 작성 환경에 대한 프로그램 및 환경 ID를 사용하여 프로젝트에 대한 테넌트 ID를 등록합니다. 이러한 ID는 연결 중인 AEM Assets 프로젝트를 식별하고 Commerce과 AEM Assets 환경 간에 통신할 수 있도록 자격 증명을 제공합니다.

AEM 자산 프로젝트를 식별한 후 Adobe Commerce과 AEM Assets 간에 자산을 동기화하는 일치 규칙을 선택합니다.

- **[!UICONTROL Match by product SKU]** - 에셋이 올바른 제품과 연결되어 있는지 확인하기 위해 에셋 메타데이터의 SKU와 [Commerce 제품 SKU](https://experienceleague.adobe.com/en/docs/commerce-operations/operational-playbook/glossary#sku)가 일치하는 기본 규칙입니다.

- **[!UICONTROL Custom match]** - 사용자 지정 일치 논리가 필요한 더 복잡한 시나리오 또는 특정 비즈니스 요구 사항에 대한 일치 규칙. 사용자 지정 일치를 구현하려면 Adobe Developer App Builder에서 자산과 제품의 일치 방법을 정의하는 사용자 지정 코드를 개발해야 합니다. 자세한 내용은 곧 제공될 예정입니다.

초기 온보딩의 경우 기본 *제품별 일치 sku* 규칙을 사용하십시오.

## 전제 조건

- [Commerce 자산을 관리하도록 AEM Experience Manager Assets 구성](#aem-assets-configure-aem)

- [Commerce용 AEM Assets 통합을 설치하고 구성](#aem-assets-configure-commerce.md)하여 확장을 추가하고 확장을 사용하는 데 필요한 자격 증명과 연결을 생성합니다.

- AEM Assets 통합에 대한 활성화를 요청하려면 지원 티켓을 만드십시오. **[!UICONTROL Program ID]**, **[!UICONTROL Environment ID]** 및 **[!UICONTROL IMS Org ID]**&#x200B;을(를) 제공해야 합니다.

  >[!TIP]
  >
  > (선택 사항) 사용 가능한 경우 **[!UICONTROL Asset Selector IMS Client ID]**&#x200B;을(를) 제공합니다.

## 연결 구성

1. [AEM Assets 작성 환경](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/sites/authoring/quick-start) 프로젝트 및 환경 ID를 가져옵니다.

   1. AEM Sites 콘솔을 열고 **[!UICONTROL Assets]**&#x200B;을(를) 선택합니다.

   1. URL <br>`https://author-p[Program ID]-e[EnvironmentID].adobeaemcloud.com/`에서 프로젝트 및 환경 ID를 복사하여 저장합니다.

1. Commerce 관리자에서 AEM Assets 통합 구성을 엽니다.

   1. **[!UICONTROL Store]** > 구성 > **[!UICONTROL ADOBE SERVICES]** > **[!UICONTROL AEM Assets Integration]**(으)로 이동합니다.

      ![AEM Assets 통합을 통해 통합 사용](assets/aem-assets-integration-enable-config.png){width="600" zoomable="yes"}

1. AEM Assets 환경 **[!UICONTROL Program ID]** 및 **[!UICONTROL Environment ID]**&#x200B;을(를) 입력하십시오.

1. 가능한 경우 **[!UICONTROL Asset Selector IMS Client ID]**&#x200B;을(를) 입력하십시오.

   [IMS ID](../getting-started/adobe-ims-config.md)은(는) 범주 및/또는 [!DNL Page Builder]에 대한 이미지를 선택하는 [[!UICONTROL Assets Selector]](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/assets/manage/asset-selector/overview-asset-selector)에 필요합니다.

1. Commerce과 자산 일치 서비스 간의 요청을 인증하기 위해 [[!UICONTROL Commerce integration]](aem-assets-configure-commerce.md#add-the-integration-to-the-commerce-environment)을(를) 선택하십시오.

1. Commerce에서 **[!UICONTROL Integration enabled]**&#x200B;을(를) `Yes`(으)로 설정하여 AEM Assets에서 들어오는 업데이트를 수락하도록 허용합니다.

   통합을 활성화한 후 에셋 일치 규칙을 구성합니다.

   ![AEM Assets 통합 자산 일치 규칙 선택](assets/aem-assets-config-matching-rule.png){width="600" zoomable="yes"}

1. 자산 동기화에 대한 일치 규칙을 정의합니다.

   1. **[!UICONTROL Match by product SKU]**&#x200B;을(를) 선택합니다.

   1. 예를 들어 **[!UICONTROL Match by product SKU attribute name]** 필드 `commerce:skus`에 Commerce 제품 SKU에 대해 정의된 [AEM Assets 메타데이터 필드 이름](aem-assets-configure-aem.md#configure-metadata)을(를) 추가합니다.

   ![AEM Assets 통합 자산 일치 규칙 선택](assets/aem-assets-config-matching-rule.png){width="600" zoomable="yes"}

1. 업데이트를 적용하고 자산 동기화를 시작하려면 **[!UICONTROL Save Config]**&#x200B;을(를) 선택하십시오.
