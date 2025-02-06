---
title: Experience Manager Assets 구성
description: Commerce용 AEM Assets 통합을 사용하여 Adobe Commerce과 Experience Manager Assets 프로젝트 간에 에셋을 동기화하는 데 필요한 에셋 메타데이터를 추가합니다.
feature: CMS, Media, Integration
exl-id: deb7c12c-5951-4491-a2bc-542e993f1f84
source-git-commit: 6b0c8054e86ae697025626ad2eb575d633003578
workflow-type: tm+mt
source-wordcount: '668'
ht-degree: 0%

---

# Experience Manager Assets 구성

Commerce 에셋을 식별하고 관리하도록 환경 구성을 업데이트하고 Assets 메타데이터를 구성하여 Commerce 에셋을 관리하도록 AEM as a Cloud Service 환경을 준비합니다.

통합하려면 사용자 지정 `Commerce` 네임스페이스와 추가 [프로필 메타데이터](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/assets/manage/metadata-profiles) 및 [스키마 메타데이터](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/assets/manage/metadata-schemas)를 추가해야 합니다.

Adobe은 네임스페이스 및 메타데이터 스키마 리소스를 AEM Assets as a Cloud Service AEM 환경에 추가하는 프로젝트 템플릿을 제공합니다. 템플릿은 다음을 추가합니다.

- Commerce 관련 속성을 식별하기 위한 [사용자 지정 네임스페이스](https://github.com/ankumalh/assets-commerce/blob/main/ui.config/jcr_root/apps/commerce/config/org.apache.sling.jcr.repoinit.RepositoryInitializer~commerce-namespaces.cfg.json), `Commerce`입니다.

- Adobe Commerce 프로젝트와 연결된 Commerce 자산에 태그를 지정하는 레이블이 `Does it exist in Commerce?`인 사용자 지정 메타데이터 형식 `commerce:isCommerce`입니다.

- *[!UICONTROL Product Data]* 속성을 추가할 사용자 지정 메타데이터 형식 `commerce:productmetadata` 및 해당 UI 구성 요소입니다. 제품 데이터에는 Commerce 에셋을 제품 SKU와 연결하고 에셋에 대한 이미지 `role` 및 `position` 특성을 지정하는 메타데이터 속성이 포함됩니다.

  ![사용자 지정 제품 데이터 UI 컨트롤](./assets/aem-commerce-sku-metadata-fields-from-template.png){width="600" zoomable="yes"}

- Commerce 자산에 태그를 지정할 `Does it exist in Adobe Commerce?` 및 `Product Data` 필드가 포함된 Commerce 탭이 있는 메타데이터 스키마 양식입니다. 이 양식은 AEM Assets UI에서 `roles` 및 `order`(위치) 필드를 표시하거나 숨기는 옵션도 제공합니다.

  AEM Assets 메타데이터 스키마 양식에 대한 ![Commerce 탭](./assets/assets-configure-metadata-schema-form-editor.png){width="600" zoomable="yes"}

- 초기 에셋 동기화를 지원하기 위해 [샘플 Commerce 에셋이 태그되고 승인되었습니다](https://github.com/ankumalh/assets-commerce/blob/main/ui.content/src/main/content/jcr_root/content/dam/wknd/en/activities/hiking/equipment_6.jpg/.content.xml) `equipment_6.jpg`. 승인된 Commerce 자산만 AEM Assets에서 Adobe Commerce으로 동기화할 수 있습니다.

Commerce-Assets AEM 프로젝트에 대한 자세한 내용은 [추가 정보](https://github.com/ankumalh/assets-commerce)를 참조하십시오.

## AEM Assets 환경 구성 사용자 지정

>[!BEGINSHADEBOX]

**필수 구성 요소**

- 프로그램 및 배포 관리자 역할을 사용하여 [AEM Assets Cloud Manager 프로그램 및 환경에 액세스](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/onboarding/journey/cloud-manager#access-sysadmin-bo).

- [로컬 AEM 개발 환경](https://experienceleague.adobe.com/en/docs/experience-manager-learn/cloud-service/local-development-environment-set-up/overview) 및 AEM 로컬 개발 프로세스에 익숙합니다.

- [AEM 프로젝트 구조](https://experienceleague.adobe.com/ko/docs/experience-manager-cloud-service/content/implementing/developing/aem-project-content-package-structure) 및 Cloud Manager을 사용하여 사용자 지정 콘텐츠 패키지를 배포하는 방법을 이해합니다.

>[!ENDSHADEBOX]

### AEM Assets 작성 환경에 Commerce-Assets AEM 프로젝트 배포

1. 필요한 경우 Cloud Manager에서 AEM Assets 프로젝트에 대한 프로덕션 및 스테이징 환경을 만듭니다.

1. 필요한 경우 배포 파이프라인을 구성합니다.

1. GitHub에서 [Commerce-Assets AEM 프로젝트](https://github.com/ankumalh/assets-commerce)에서 표준 코드를 다운로드합니다.

1. [로컬 AEM 개발 환경](https://experienceleague.adobe.com/en/docs/experience-manager-learn/cloud-service/local-development-environment-set-up/overview)에서 사용자 지정 코드를 AEM Assets 환경 구성에 Maven 패키지로 설치하거나 코드를 기존 프로젝트 구성에 수동으로 복사합니다.

1. 변경 사항을 커밋하고 로컬 개발 분기를 Cloud Manager git 저장소로 푸시합니다.

1. Cloud Manager에서 [AEM 환경을 업데이트하도록 코드를 배포](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/implementing/using-cloud-manager/deploy-code#deploying-code-with-cloud-manager)합니다.

## 메타데이터 프로필 구성

메타데이터 프로필을 만들어 Commerce 에셋 메타데이터에 대한 기본값을 설정합니다. 설정되면 이 프로필을 AEM Asset 폴더에 적용하여 이러한 기본값을 자동으로 사용합니다. 이 선택적 설정은 수동 단계를 줄여 자산 처리를 간소화하는 데 도움이 됩니다.

1. Adobe Experience Manager 작업 영역에서 Adobe Experience Manager 아이콘을 클릭하여 AEM Assets용 작성자 컨텐츠 관리 작업 영역으로 이동합니다.

   ![AEM Assets 작성](./assets/aem-assets-authoring.png){width="600" zoomable="yes"}

1. 망치 아이콘을 선택하여 관리자 도구를 엽니다.

   ![AEM 작성자 관리자 관리 메타데이터 프로필](./assets/aem-manage-metadata-profiles.png){width="600" zoomable="yes"}

1. **[!UICONTROL Metadata Profiles]**&#x200B;을(를) 클릭하여 프로필 구성 페이지를 엽니다.

1. Commerce 통합을 위한 메타데이터 프로필을 **[!UICONTROL Create]**&#x200B;합니다.

   ![AEM 작성자 관리자가 메타데이터 프로필 추가 ](./assets/aem-create-metadata-profile.png){width="600" zoomable="yes"}

1. Commerce 메타데이터에 대한 탭을 추가합니다.

   1. 왼쪽에서 **[!UICONTROL Settings]**&#x200B;을(를) 클릭합니다.

   1. 탭 섹션에서 **[!UICONTROL +]**&#x200B;을(를) 클릭한 다음 **[!UICONTROL Tab Name]**, `Commerce`을(를) 지정합니다.

1. 양식에 `Does it exist in Commerce?` 필드를 추가하고 기본값을 `yes`(으)로 설정합니다.

   ![AEM 작성자 관리자가 프로필에 메타데이터 필드 추가](./assets/aem-edit-metadata-profile-fields.png){width="600" zoomable="yes"}

1. 업데이트를 저장합니다.

1. Commerce 자산이 저장된 폴더에 `Commerce integration` 메타데이터 프로필을 적용합니다.

   1. [!UICONTROL  Metadata Profiles] 페이지에서 Commerce 통합 프로필을 선택합니다.

   1. 작업 메뉴에서 **[!UICONTROL Apply Metadata Profiles to Folder(s)]**&#x200B;을(를) 선택합니다.

   1. Commerce 자산이 포함된 폴더를 선택합니다.

      Commerce 폴더가 없는 경우 만듭니다.

   1. **[!UICONTROL Apply]**&#x200B;을(를) 클릭합니다.

>[!TIP]
>
>메타데이터 프로필을 업데이트하여 _[!UICONTROL Review Status]_필드의 기본값을 `Approved`(으)로 설정하여 Commerce 자산이 AEM Assets 환경에 업로드될 때 자동으로 동기화할 수 있습니다. `Review Status` 필드의 속성 유형은 `./jcr:content/metadata/dam:status`입니다.


## 다음 단계

AEM 환경을 업데이트한 후 Adobe Commerce을 설정합니다.

1. [Commerce용 AEM Assets 통합 설치 및 구성](aem-assets-configure-commerce.md)
2. [에셋 동기화를 활성화하여 Adobe Commerce 프로젝트 환경과 AEM Assets 프로젝트 환경 간에 에셋을 전송합니다](aem-assets-setup-synchronization.md)
