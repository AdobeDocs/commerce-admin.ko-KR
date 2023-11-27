---
title: 콘텐츠 페이지 번역
description: 특정 스토어 보기에서 사용할 수 있는 각 페이지의 번역된 버전을 만드는 방법을 알아봅니다.
exl-id: e8743ea5-0c8e-4970-987d-c9ac7c1e2a66
feature: Page Content
topic: Commerce, Localization
source-git-commit: b659c7e1e8f2ae9883f1e24d8045d6dd1e90cfc0
workflow-type: tm+mt
source-wordcount: '338'
ht-degree: 0%

---

# 콘텐츠 페이지 번역

스토어에 서로 다른 보기가 여러 개 있는 경우 [언어](../stores-purchase/store-localize.md), 그리고 각 보기의 로케일을 다른 언어로 설정했는데 그 결과가 부분적으로 번역된 사이트입니다. 다음 단계는 특정 스토어 보기에서 사용할 수 있는 각 페이지의 번역된 버전을 만드는 것입니다. 다음 [!UICONTROL Store View] 열 _[!UICONTROL Manage Pages]_목록에는 번역된 페이지 버전이 있는 각 보기가 표시됩니다.

콘텐츠 페이지를 번역하려면 원본과 동일한 URL 키를 가지지만 특정 스토어 보기에 할당된 다른 페이지를 만들어야 합니다. 그런 다음 특정 보기에 대한 페이지를 번역된 텍스트로 업데이트합니다. 다음 예제에서는 의 번역된 버전을 만드는 방법을 보여줍니다. _정보_ 스페인어 스토어 조회수를 위한 페이지입니다.

## 1단계: 번역할 페이지의 URL 키 복사

1. 다음에서 _관리자_ 사이드바, 이동 **[!UICONTROL Content]** > _[!UICONTROL Elements]_>**[!UICONTROL Pages]**.

1. 그리드에서 번역할 페이지를 찾아서 엽니다. _편집_ 모드.

1. 확장 ![확장 선택기](../assets/icon-display-expand.png) 다음 **[!UICONTROL Search Engine Optimization]** 섹션 및 복사 **[!UICONTROL URL Key]** 클립보드에 복사합니다.

1. 로 돌아가려면 _[!UICONTROL Pages]_그리드, 클릭&#x200B;**[!UICONTROL Back]**을 클릭합니다.

## 2단계: 번역된 콘텐츠의 페이지 추가

1. 클릭 **[!UICONTROL Add New Page]**.

1. 번역된 항목 입력 **[!UICONTROL Page Title]**.

1. 확장 ![확장 선택기](../assets/icon-display-expand.png) 다음 **[!UICONTROL Content]** 페이지를 번역하고 번역된 텍스트를 작성합니다.

1. 확장 ![확장 선택기](../assets/icon-display-expand.png) 다음 **[!UICONTROL Search Engine Optimization]** 섹션을 참조하고 다음을 수행합니다.

   - 붙여넣기 **[!UICONTROL URL Key]** 원본 페이지에서 복사한 내용입니다.

   - 다음에 대한 번역된 텍스트 입력 **[!UICONTROL Meta Title]**, **[!UICONTROL Meta Keywords]**, 및 **[!UICONTROL Meta Description]**.

1. 확장 ![확장 선택기](../assets/icon-display-expand.png) 다음 **[!UICONTROL Page in Websites]** 섹션 및 세트 **[!UICONTROL Store View]** 페이지를 사용할 수 있는 스토어 뷰로 이동합니다.

1. 확장 ![확장 선택기](../assets/icon-display-expand.png) 다음 **[!UICONTROL Design]** 섹션 및 열 설정 **[!UICONTROL Layout]** 페이지의 입니다.

1. 클릭 **[!UICONTROL Save]**.

1. 메시지가 표시되면 잘못된 항목을 새로 고칩니다. [캐시](../systems/cache-management.md).

## 3단계: 번역 확인

번역을 확인하려면 매장으로 이동하여 언어 선택기를 사용하여 매장 보기를 변경합니다.

페이지에 회사 바닥글 링크를 포함하여 번역해야 하는 일부 요소가 여전히 있습니다 [차단](block-add.md), [시작 메시지](../getting-started/storefront-branding.md#change-the-welcome-message), 및 [제품 정보](../stores-purchase/store-localize.md#localize-products).
