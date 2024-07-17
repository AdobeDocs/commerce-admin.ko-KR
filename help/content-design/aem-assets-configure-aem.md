---
title: Experience Manager Assets 구성
description: Commerce용 AEM Assets 통합을 사용하여 Adobe Commerce과 Experience Manager Assets 프로젝트 간에 에셋을 동기화하는 데 필요한 에셋 메타데이터를 추가합니다.
feature: CMS, Media, Integration
source-git-commit: d91ba86b77ef91e849d1737628b575f2309376b8
workflow-type: tm+mt
source-wordcount: '614'
ht-degree: 0%

---

# Experience Manager Assets 구성

{{$include /help/_includes/aem-assets-integration-beta-note.md}}

Commerce용 AEM Assets 통합을 사용하여 스토어의 미디어 에셋을 관리하려면 AEM Assets 프로젝트에 Commerce 에셋을 쉽게 검색하고 관리할 수 있도록 특정 메타데이터를 추가해야 합니다. 또한 이 메타데이터를 통해 Adobe Commerce과 Experience Manager Assets 간의 에셋을 손쉽게 동기화할 수 있습니다. 메타데이터 필드를 정의하면 Commerce 에셋이 Experience Manager Assets과 처음 공유될 때 이러한 필드의 초기 매핑이 자동으로 수행됩니다.

통합을 위해 두 가지 유형의 메타데이터를 구성합니다.

- **[메타데이터 프로필](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/assets/manage/metadata-profiles)**&#x200B;을(를) 사용하면 폴더 내의 자산에 기본 메타데이터를 적용할 수 있습니다. 폴더의 모든 에셋은 프로필에 구성된 기본 메타데이터를 상속합니다.

- **[메타데이터 스키마](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/assets/manage/metadata-schemas)**&#x200B;은(는) 속성 페이지의 레이아웃 및 AEM 에셋의 메타데이터 속성으로 사용할 수 있는 필드 집합을 정의합니다.

## 메타데이터 구성

초기 온보딩의 경우 AEM Assets 메타데이터 프로필과 메타데이터 스키마 모두에 다음 Commerce 메타데이터를 추가합니다.

| 필드 유형 | 레이블 | 속성 | 기본값 |
|------ | ------- | ---------- | ------------- |
| 텍스트 | **Adobe Commerce에 있습니까?** | `./jcr:content/metadata/commerce:isCommerce` | 예 |
| 다중 값 텍스트 | **SKU** | `./jcr:content/metadata/commerce:skus` | 없음 |
| 다중 값 텍스트 | **위치** | `./jcr:content/metadata/commerce:positions` | 없음 |
| 다중 값 텍스트 | **역할** | `./jcr:content/metadata/commerce:roles` | 없음 |


### 메타데이터 프로필에 Commerce 필드 추가

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

1. 양식에 [메타데이터 필드](#configure-metadata)을(를) 추가합니다.

   ![AEM 작성자 관리자가 프로필에 메타데이터 필드 추가](./assets/aem-edit-metadata-profile-fields.png){width="600" zoomable="yes"}

1. 업데이트를 저장합니다.

1. Commerce 자산이 저장된 폴더에 `Commerce integration` 메타데이터 프로필을 적용합니다.

   1. [!UICONTROL  Metadata Profiles] 페이지에서 Commerce 통합 프로필을 선택합니다.

   1. 작업 메뉴에서 **[!UICONTROL Apply Metadata Profiles to Folder(s)]**&#x200B;을(를) 선택합니다.

   1. Commerce 자산이 포함된 폴더를 선택합니다.

      Commerce 폴더가 없는 경우 만듭니다.

   1. **[!UICONTROL Apply]**&#x200B;을(를) 클릭합니다.

### 메타데이터 스키마 양식에 Commerce 필드 추가

1. Assets용 AEM Author 콘텐츠 관리 패널에서 **[!UICONTROL Metadata Schemas]**([!UICONTROL Manage metadata schema forms])을(를) 엽니다.

   ![AEM 작성자 관리자 업데이트 메타데이터 스키마](./assets/aem-assets-manage-metadata-schema.png){width="600" zoomable="yes"}

1. Commerce에 대한 메타데이터 스키마를 **[!UICONTROL Create]**&#x200B;합니다.

   ![AEM 작성자 관리자 업데이트 메타데이터 스키마](./assets/aem-assets-create-metadata-schema.png){width="600" zoomable="yes"}

1. [!UICONTROL Metadata Schema Form]에서 `Does Commerce exist?` 및 `Commerce mappings` 필드를 만들고 속성을 매핑합니다.

1. **[!UICONTROL Save]**&#x200B;을(를) 클릭합니다.


## Publish an 에셋

Commerce 자산에 대한 AEM 메타데이터 및 스키마 프로필을 구성한 후 Commerce 메타데이터 필드에 매핑하는 첫 번째 Commerce 자산을 만듭니다.

1. Experience Manager에서 [!UICONTROL Assets > Files](으)로 이동하여 **Commerce** 폴더를 선택하십시오.

1. 파일을 폴더로 끌어 놓거나 **[!UICONTROL Add Assets]**&#x200B;을(를) 클릭하여 Commerce 프로젝트에 대한 이미지를 업로드합니다.

1. 메타데이터 구성: **isCommerce**&#x200B;이(가) `true`(으)로 설정되어 있는지, `commerce:skus` 속성이 이미지와 연결된 Commerce 제품에 대한 SKU로 설정되어 있는지 확인하십시오.

1. 자산을 승인합니다.


## Commerce 폴더에 자산 추가

Commerce 메타데이터 특성이 지정된 AEM Assets Commerce 폴더에 하나 이상의 자산을 만듭니다.

이 자산은 Commerce 인스턴스와 AEM Assets 간의 동기화를 설정하는 데 필요합니다.

## 에셋의 메타데이터 매핑

Commerce 자산이 처음으로 게시되면 메타데이터가 매핑됩니다.  처음으로 Commerce에서 가져왔습니다. 기본 제공 필드 또는 사용자 지정 필드가 있는 미디어 자산은 자산을 Experience Manager Assets으로 처음 전송할 때 지정된 필드에 자동으로 매핑됩니다.

에셋 매핑을 시작하려면 먼저 다음 작업을 완료하십시오.

- [Commerce용 AEM Assets 통합 설치 및 구성](aem-assets-configure-commerce.md)
- [에셋 동기화를 활성화하여 Adobe Commerce 프로젝트 환경과 AEM Assets 프로젝트 환경 간에 에셋을 전송합니다](aem-assets-setup-synchronization.md)
