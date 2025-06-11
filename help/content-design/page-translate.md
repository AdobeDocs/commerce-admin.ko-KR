---
title: 콘텐츠 페이지 번역
description: 특정 스토어 보기에서 사용할 수 있는 각 페이지의 번역된 버전을 만드는 방법을 알아봅니다.
exl-id: e8743ea5-0c8e-4970-987d-c9ac7c1e2a66
feature: Page Content
topic: Commerce, Localization
badgePaas: label="PaaS만" type="Informative" url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="Adobe Commerce 온 클라우드 프로젝트(Adobe 관리 PaaS 인프라) 및 온프레미스 프로젝트에만 적용됩니다."
source-git-commit: 57a913b21f4cbbb4f0800afe13012ff46d578f8e
workflow-type: tm+mt
source-wordcount: '358'
ht-degree: 0%

---

# 콘텐츠 페이지 번역

스토어에 서로 다른 [언어](../stores-purchase/store-localize.md)의 보기가 여러 개 있고 각 보기의 로케일을 서로 다른 언어로 설정한 경우 그 결과는 부분적으로 번역된 사이트입니다. 다음 단계는 특정 스토어 보기에서 사용할 수 있는 각 페이지의 번역된 버전을 만드는 것입니다. _[!UICONTROL Manage Pages]_&#x200B;목록의 [!UICONTROL Store View] 열은 페이지의 번역된 버전을 포함하는 각 보기를 표시합니다.

콘텐츠 페이지를 번역하려면 원본과 동일한 URL 키를 가지지만 특정 스토어 보기에 할당된 다른 페이지를 만들어야 합니다. 그런 다음 특정 보기에 대한 페이지를 번역된 텍스트로 업데이트합니다. 다음 예제에서는 스페인어 스토어 보기에 대한 _정보_ 페이지의 번역된 버전을 만드는 방법을 보여 줍니다.

## 1단계: 번역할 페이지의 URL 키 복사

1. _관리자_ 사이드바에서 **[!UICONTROL Content]** > _[!UICONTROL Elements]_>**[!UICONTROL Pages]**(으)로 이동합니다.

1. 그리드에서 번역할 페이지를 찾아 _편집_ 모드로 엽니다.

1. **[!UICONTROL Search Engine Optimization]** 섹션에서 ![확장 선택기](../assets/icon-display-expand.png)를 확장하고 **[!UICONTROL URL Key]**&#x200B;을(를) 클립보드에 복사합니다.

1. _[!UICONTROL Pages]_&#x200B;그리드로 돌아가려면 맨 위 단추 모음에서&#x200B;**[!UICONTROL Back]**&#x200B;을(를) 클릭합니다.

## 2단계: 번역된 콘텐츠의 페이지 추가

1. **[!UICONTROL Add New Page]**&#x200B;을(를) 클릭합니다.

1. 번역된 **[!UICONTROL Page Title]**&#x200B;을(를) 입력하십시오.

1. **[!UICONTROL Content]** 섹션에서 ![확장 선택기](../assets/icon-display-expand.png)를 확장하고 페이지에 대한 번역된 텍스트를 완료합니다.

1. **[!UICONTROL Search Engine Optimization]** 섹션에서 ![확장 선택기](../assets/icon-display-expand.png)를 확장하고 다음을 수행합니다.

   - 원본 페이지에서 복사한 **[!UICONTROL URL Key]**&#x200B;을(를) 붙여 넣습니다.

   - **[!UICONTROL Meta Title]**, **[!UICONTROL Meta Keywords]** 및 **[!UICONTROL Meta Description]**&#x200B;에 대해 번역된 텍스트를 입력하십시오.

1. **[!UICONTROL Page in Websites]** 섹션에서 ![확장 선택기](../assets/icon-display-expand.png)을(를) 확장하고 페이지를 사용할 수 있는 저장소 보기로 **[!UICONTROL Store View]**&#x200B;을(를) 설정합니다.

1. **[!UICONTROL Design]** 섹션에서 ![확장 선택기](../assets/icon-display-expand.png)을(를) 확장하고 페이지의 **[!UICONTROL Layout]** 열을 설정합니다.

1. **[!UICONTROL Save]**&#x200B;을(를) 클릭합니다.

1. 메시지가 표시되면 잘못된 [캐시](../systems/cache-management.md)를 새로 고치십시오.

## 3단계: 번역 확인

번역을 확인하려면 매장으로 이동하여 언어 선택기를 사용하여 매장 보기를 변경합니다.

회사 바닥글 링크 [블록](block-add.md), [시작 메시지](../getting-started/storefront-branding.md#change-the-welcome-message), [제품 정보](../stores-purchase/store-localize.md#localize-products)를 포함하여 페이지에 번역해야 하는 일부 요소가 남아 있습니다.
