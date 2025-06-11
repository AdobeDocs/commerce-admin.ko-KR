---
title: 디자인 구성
description: 디자인 구성 을 사용하면 설정을 단일 페이지에 표시하여 디자인 관련 규칙과 구성 설정을 쉽게 편집할 수 있습니다.
exl-id: 43fec57f-d76d-45a9-812b-ba1947cea46d
feature: Page Content, Configuration
source-git-commit: 57a913b21f4cbbb4f0800afe13012ff46d578f8e
workflow-type: tm+mt
source-wordcount: '351'
ht-degree: 0%

---

# 디자인 구성

디자인 구성을 사용하면 단일 페이지에 설정을 표시하여 디자인 관련 규칙과 구성 설정을 쉽게 편집할 수 있습니다.

![디자인 구성 페이지](./assets/configuration.png){width="700" zoomable="yes"}

## 디자인 구성 변경

1. _관리자_ 사이드바에서 **[!UICONTROL Content]** > _[!UICONTROL Design]_>**[!UICONTROL Configuration]**(으)로 이동합니다.

1. 구성할 저장소 보기를 찾은 다음 _[!UICONTROL Action]_&#x200B;열에서&#x200B;**[!UICONTROL Edit]**&#x200B;을(를) 클릭합니다.

   이 페이지에는 스토어 보기에 대한 현재 디자인 설정이 표시됩니다.

1. 기본 테마를 변경하려면 **[!UICONTROL Applied Theme]**&#x200B;을(를) 보기에 적용할 테마로 설정하십시오.

   테마를 지정하지 않으면 시스템 기본 테마가 사용됩니다. 일부 타사 확장은 시스템 기본 테마를 수정합니다.

1. [!BADGE PaaS만]{type=Informative url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="Adobe Commerce 온 클라우드 프로젝트(Adobe 관리 PaaS 인프라) 및 온프레미스 프로젝트에만 적용됩니다."} 테마를 특정 장치에만 사용하려면 **[!UICONTROL User Agent Rules]**&#x200B;을(를) 설정하십시오.

   ![사용자 에이전트 규칙](./assets/configuration-user-agent-rules.png){width="400" zoomable="yes"}

   테마를 지정할 각 장치 유형에 대해 다음 작업을 수행하십시오.

   - **[!UICONTROL Add New User Agent Rule]**&#x200B;을(를) 클릭합니다.

   - **[!UICONTROL Search String]**&#x200B;의 경우 특정 장치의 브라우저 ID를 입력하십시오.

     검색 문자열은 일반 표현식 또는 PCRE(Perl Compatible Regular Expression)일 수 있습니다(자세한 내용은 [사용자 에이전트](https://en.wikipedia.org/wiki/User_agent) 참조). 다음 검색 문자열은 Firefox를 식별합니다.

         /^mozilla/i
     
   - **[!UICONTROL Theme Name]**&#x200B;의 경우 지정된 장치에 사용할 테마를 선택하십시오.

   >[!NOTE]
   >
   >지정하려는 장치에 대해 여러 규칙을 추가할 수 있습니다. 검색 문자열은 입력한 순서대로 일치합니다.

1. _[!UICONTROL Other Settings]_&#x200B;에서 각 섹션을 확장하고 연결된 항목의 지침에 따라 필요에 따라 설정을 편집합니다.

   - [[!UICONTROL Pagination]](../catalog/navigation-product-listings.md#pagination-controls) [!BADGE PaaS만]{type=Informative url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="Adobe Commerce 온 클라우드 프로젝트(Adobe 관리 PaaS 인프라) 및 온프레미스 프로젝트에만 적용됩니다."}
   - [[!UICONTROL HTML Head]](page-setup.md#html-head) [!BADGE PaaS만]{type=Informative url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="Adobe Commerce 온 클라우드 프로젝트(Adobe 관리 PaaS 인프라) 및 온프레미스 프로젝트에만 적용됩니다."}
   - [[!UICONTROL Header]](page-setup.md#header) [!BADGE PaaS만]{type=Informative url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="Adobe Commerce 온 클라우드 프로젝트(Adobe 관리 PaaS 인프라) 및 온프레미스 프로젝트에만 적용됩니다."}
   - [[!UICONTROL Footer]](page-setup.md#footer) [!BADGE PaaS만]{type=Informative url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="Adobe Commerce 온 클라우드 프로젝트(Adobe 관리 PaaS 인프라) 및 온프레미스 프로젝트에만 적용됩니다."}
   - [[!UICONTROL Search Engine Robots]](../merchandising-promotions/seo-overview.md#search-engine-robots) [!BADGE PaaS만]{type=Informative url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="Adobe Commerce 온 클라우드 프로젝트(Adobe 관리 PaaS 인프라) 및 온프레미스 프로젝트에만 적용됩니다."}
   - [[!UICONTROL Product Image Watermarks]](../catalog/product-image.md#watermarks)
   - [[!UICONTROL Transactional Emails]](../systems/email-templates.md#configure-email-templates)

   ![디자인에 영향을 주는 다른 설정](./assets/configuration-other-settings.png){width="500" zoomable="yes"}

1. 완료되면 **[!UICONTROL Save Configuration]**&#x200B;을(를) 클릭합니다.
