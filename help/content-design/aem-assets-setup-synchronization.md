---
title: 자산 동기화 활성화
description: Adobe Commerce 및 Experience Manager Assets 프로젝트를 연결하여 이러한 두 시스템 간에 에셋을 동기화하는 방법에 대해 알아봅니다.
feature: CMS, Media
exl-id: cc3ae56b-f1c8-4c96-a284-bcd726ce2bab
source-git-commit: 36defb137a48067fe59b95f0519a7703a38e039d
workflow-type: tm+mt
source-wordcount: '457'
ht-degree: 0%

---

# 자산 동기화 활성화

Commerce 환경 구성을 업데이트하여 Commerce을 AEM Assets 인스턴스에 연결하여 에셋 동기화를 활성화합니다. 통합을 통해 Commerce과 AEM Assets 간에 자산을 동기화할 수 있으므로 제품 이미지 및 기타 자산이 항상 최신 상태로 유지됩니다.

AEM 에셋 프로젝트를 식별한 후 Adobe Commerce과 AEM Assets 간에 에셋을 동기화하기 위한 일치 규칙을 선택합니다.

- **[!UICONTROL Match by product SKU]** - 에셋이 올바른 제품과 연결되어 있는지 확인하기 위해 에셋 메타데이터의 SKU와 [Commerce 제품 SKU](https://experienceleague.adobe.com/en/docs/commerce-operations/implementation-playbook/glossary#sku)가 일치하는 기본 규칙입니다.

- **[!UICONTROL Custom match]** - 사용자 지정 일치 논리가 필요한 더 복잡한 시나리오 또는 특정 비즈니스 요구 사항에 대한 일치 규칙. 사용자 지정 일치를 구현하려면 Adobe Developer App Builder에서 자산과 제품의 일치 방법을 정의하는 사용자 지정 코드를 개발해야 합니다. 자세한 내용은 곧 제공될 예정입니다.

초기 설정의 경우 기본 *제품별 일치 sku* 규칙을 사용하십시오.

## 전제 조건

- [Commerce 자산을 관리하도록 AEM Assets 구성](aem-assets-configure-aem.md)

- [Commerce용 AEM Assets 통합을 설치하고 구성](aem-assets-configure-commerce.md)하여 확장을 추가하고 확장을 사용하는 데 필요한 자격 증명과 연결을 생성합니다.

- AEM Assets 통합에 대한 활성화를 요청하려면 지원 티켓을 만드십시오. Commerce에 연결할 AEM Assets 제작 환경에 대해 **[!UICONTROL Program ID]**, **[!UICONTROL Environment ID]** 및 **[!UICONTROL IMS Org ID]**&#x200B;을(를) 제공해야 합니다.

  >[!TIP]
  >
  > (선택 사항) 사용 가능한 경우 **[!UICONTROL Asset Selector IMS Client ID]**&#x200B;을(를) 제공합니다. *AEM Assets 선택기* 설명서에서 [ImsAuthProps](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/assets/manage/asset-selector/asset-selector-integration/integrate-asset-selector-adobe-app)을(를) 참조하십시오.

## 연결 구성

1. [AEM Assets 작성 환경](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/sites/authoring/quick-start) 프로젝트 및 환경 ID를 가져옵니다.

   1. AEM Sites 콘솔을 열고 **[!UICONTROL Assets]**&#x200B;을(를) 선택합니다.

   1. URL <br>`https://author-p[Program ID]-e[EnvironmentID].adobeaemcloud.com/`에서 프로젝트 및 환경 ID를 복사하여 저장합니다.
1. Commerce 관리자에서 AEM Assets 통합 구성을 엽니다.

   1. **[!UICONTROL Store]** > 구성 > **[!UICONTROL ADOBE SERVICES]** > **[!UICONTROL AEM Assets Integration]**(으)로 이동합니다.

      ![AEM Assets 통합을 통해 통합 사용](assets/aem-assets-integration-enable-config.png){width="600" zoomable="yes"}

1. AEM Assets 환경 **[!UICONTROL Program ID]** 및 **[!UICONTROL Environment ID]**&#x200B;을(를) 입력하십시오.

   *[!UICONTROL Use system value]*&#x200B;에서 선택 항목을 제거하여 구성 값을 편집합니다.

1. 사용 가능한 경우 **[!UICONTROL Asset Selector IMS Client ID]**&#x200B;을(를) 입력하십시오.

   [자산 선택기 IMS 클라이언트 ID](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/assets/manage/asset-selector/asset-selector-integration/integrate-asset-selector-adobe-app#ims-auth-props)은(는) 사용자가 시각적 자산을 Commerce 제품 페이지에 직접 포함할 수 있는 AEM Assets 기능인 [!UICONTROL Assets Selector]에 필요합니다.

1. Commerce과 자산 일치 서비스 간의 요청을 인증하기 위해 [[!UICONTROL Commerce integration]](aem-assets-configure-commerce.md#add-the-integration-to-the-commerce-environment)을(를) 선택하십시오.

1. Commerce이 AEM Assets에서 들어오는 업데이트를 수락하도록 하려면 **[!UICONTROL Integration enabled]**&#x200B;을(를) `Yes`(으)로 설정하십시오.

   통합을 활성화한 후 에셋 일치 기준을 지정하는 추가 구성 옵션을 사용할 수 있습니다.

1. 자산 동기화에 대한 일치 규칙을 정의합니다.

   1. **[!UICONTROL Match by product SKU]** 또는 **[!UICONTROL Custom match (Requires App Builder)]**&#x200B;을(를) 선택합니다.

   1. 예를 들어 **[!UICONTROL Match by product SKU attribute name]** 필드 `commerce:skus`에 Commerce 제품 SKU에 대해 정의된 [AEM Assets 메타데이터 필드 이름](aem-assets-configure-aem.md#configure-metadata)을(를) 추가합니다.

1. 업데이트를 적용하고 자산 동기화를 시작하려면 **[!UICONTROL Save Config]**&#x200B;을(를) 선택하십시오.

   구성 업데이트는 초기 동기화 프로세스를 트리거하여 Commerce에서 AEM Assets의 수신 업데이트를 수락할 수 있도록 합니다. 동기화에 필요한 시간은 에셋의 양과 특정 구성에 따라 다릅니다. 통합은 자동화된 프로세스를 활용하여 동기화에 필요한 시간을 최소화합니다.

## 다음 단계

[Commerce과 함께 AEM Assets 사용](aem-assets-manage.md)
