---
title: 로컬라이제이션 저장
description: 스토어 또는 스토어 보기를 현지화하는 방법에 대해 알아봅니다.
exl-id: 64e1b431-f599-444c-9d39-207bb95f0400
topic: Commerce, Localization
source-git-commit: 8b5af316ab1d2e632ed5fc2066974326830ab3f7
workflow-type: tm+mt
source-wordcount: '735'
ht-degree: 0%

---

# 로컬라이제이션 저장

스토어 전체의 페이지에 하드 코딩된 것으로 보이는 대부분의 텍스트는 보기의 로케일을 변경하여 즉시 다른 언어로 변경할 수 있습니다. 로케일을 변경해도 실제로 텍스트가 단어 단위로 번역되지는 않지만 스토어 전체에 사용되는 인터페이스 텍스트를 제공하는 다른 번역 표를 참조합니다. 변경할 수 있는 텍스트에는 다음과 같은 탐색 제목, 레이블, 단추 및 링크가 포함됩니다. _내 장바구니_ 및 _내 계정_. 다음을 사용할 수도 있습니다 [인라인 번역](../configuration-reference/advanced/developer.md) 인터페이스의 텍스트를 표시하는 도구입니다.

언어 팩은 다음에서 찾을 수 있습니다. [번역 및 로컬라이제이션][1]Commerce Marketplace 시 {:target=&quot;_blank&quot;} 새로운 확장 기능은 Marketplace에 지속적으로 추가되므로 자주 다시 확인하십시오.

## 1단계: 언어 팩 설치

언어 팩 확장 설치에 대한 표준 지침을 따르십시오. 확장 설치에 대한 자세한 내용은 [일반 CLI 설치][2] 다음에서 _확장 안내서_.

## 2단계: 언어에 대한 스토어 보기 만들기

1. 다음에서 _관리자_ 사이드바, 이동 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL All Stores]**.

1. 클릭 **[!UICONTROL Create Store View]**.

1. 새 저장소 보기에 대한 옵션을 설정합니다.

   - **[!UICONTROL Store]** — 뷰의 상위 저장소를 선택합니다.

   - **[!UICONTROL Name]** — 스토어 뷰의 이름을 입력합니다. 예를 들어 포르투갈어입니다.

     저장소 헤더에 이름이 _언어 선택기_.

   - **[!UICONTROL Code]** — 보기를 식별하는 코드를 소문자로 입력합니다. For example: `portuguese`.

   - **[!UICONTROL Status]** — 뷰를 활성화하려면 를 로 설정합니다. `Enabled`.

   - **[!UICONTROL Sort Order]** — (선택 사항) 이 뷰가 다른 뷰와 함께 나열되는 순서를 결정하는 숫자를 입력합니다.

1. 완료되면 다음을 클릭하십시오. **[!UICONTROL Save Store View]**.

## 3단계: 스토어 보기의 로케일 변경

1. 다음에서 _관리자_ 사이드바, 이동 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. 왼쪽 상단 모서리에서 을(를) 설정합니다. **[!UICONTROL Store View]** 구성을 적용할 특정 보기에 대해 설명합니다.

1. 범위 전환을 확인하는 메시지가 표시되면 **[!UICONTROL OK]**.

1. 확장 ![확장 선택기](../assets/icon-display-expand.png) 다음 **[!UICONTROL Locale Options]** 섹션.

1. 지우기 **[!UICONTROL Use Website]** 확인란 및 설정 **[!UICONTROL Locale]** 를 뷰에 지정하려는 언어로 바꿉니다.

   사용할 수 있는 언어의 변형이 여러 개 있는 경우 특정 지역이나 언어에 대한 변형을 선택해야 합니다.

1. 완료되면 다음을 클릭하십시오. **[!UICONTROL Save Config]**.

   로케일의 언어를 변경하면 제품 이름 및 설명, 카테고리, [CMS](../content-design/page-translate.md) 각 스토어 보기에 대해 페이지 및 블록을 별도로 번역해야 합니다.

## 제품 현지화

스토어에 서로 다른 언어로 된 보기가 여러 개 있는 경우 각 스토어 보기에서 동일한 제품을 사용할 수 있습니다. 언어에 관계없이 SKU, 가격 및 재고 수준과 같은 동일한 기본 제품 정보를 사용할 수 있습니다. 그런 다음 각 언어에 필요한 제품 이름, 설명 필드 및 메타데이터만 번역합니다.

### 1단계: 제품 필드 번역

1. 다음에서 _관리자_ 사이드바, 이동  **[!UICONTROL Catalog]** > **[!UICONTROL Products]**.

1. 그리드에서 번역할 제품을 찾아 편집 모드로 엽니다.

1. 왼쪽 상단 모서리에서 을(를) 설정합니다. **[!UICONTROL Store View]** 뷰로 이동하여 번역 **[!UICONTROL OK]** 확인을 묻는 메시지가 나타나면

1. 편집할 각 필드에 대해 다음을 수행합니다.

   - 선택 취소 **[!UICONTROL Use Default Value]** 필드의 오른쪽에 있는 확인란

   - 번역된 텍스트를 필드에 붙여넣거나 입력합니다.

   다음을 포함한 모든 텍스트 필드를 번역해야 합니다. [이미지](../catalog/catalog-images-video.md) 레이블 및 대체 텍스트, [검색 엔진 최적화](../catalog/product-search-engine-optimization.md) 필드 및 모두 [사용자 정의 옵션](../catalog/settings-advanced-custom-options.md) 정보.

1. 완료되면 다음을 클릭하십시오. **[!UICONTROL Save]**.

### 2단계: 필드 레이블 번역

1. 다음에서 _관리자_ 사이드바, 이동 **[!UICONTROL Stores]** > _[!UICONTROL Attributes]_>**[!UICONTROL Product]**.

1. 목록에서 번역할 속성을 찾아 편집 모드로 엽니다.

1. 왼쪽 패널에서 을 선택합니다 **[!UICONTROL Manage Labels]**.

1. 다음에서 _[!UICONTROL Manage Titles]_섹션에서 각 스토어 보기에 대해 번역된 레이블을 입력합니다.

   ![번역된 레이블 입력](./assets/product-attribute-labels-translate.png){width="600" zoomable="yes"}

1. 완료되면 다음을 클릭하십시오. **[!UICONTROL Save Attribute]**.

### 3단계: 모든 범주 번역

1. 다음에서 _관리자_ 사이드바, 이동 **[!UICONTROL Catalog]** > **카테고리**.

1. 왼쪽 상단 모서리에서 을 설정합니다. **[!UICONTROL Store View]** 뷰로 이동하여 번역 **[!UICONTROL OK]** 확인을 묻는 메시지가 나타나면

1. 트리에서 번역할 범주를 찾아 편집 모드로 엽니다.

1. 대상 _기본 정보_, 번역 **[!UICONTROL Category Name]**.

1. 확장 ![확장 선택기](../assets/icon-display-expand.png) 다음 _[!UICONTROL Content]_섹션 및 번역&#x200B;**[!UICONTROL Description]**.

1. 확장 ![확장 선택기](../assets/icon-display-expand.png) 다음 **[!UICONTROL Search Engine Optimization Settings]** 섹션을 만들고 다음 필드를 번역합니다.

   - **[!UICONTROL Meta Title]**
   - **[!UICONTROL Meta Keywords]**
   - **[!UICONTROL Meta Description]**

1. 아래 _[!UICONTROL Search Engine Optimization Settings]_섹션에서 다음을 수행하여&#x200B;**[!UICONTROL URL Key]**:

   - 지우기 **[!UICONTROL Use Default Value]** 필드의 오른쪽에 있는 확인란

   - 번역된 텍스트를 입력합니다.

   - 다음을 확인하십시오. **[!UICONTROL Create Permanent Redirect for old URL]** 확인란이 선택되어 있습니다.

   ![URL 키 번역](./assets/category-translate-url-key.png)

1. 완료되면 다음을 클릭하십시오. **[!UICONTROL Save Category]**.

1. 스토어에서 사용되는 모든 카테고리에 대해 이 프로세스를 반복합니다.

### 4단계: 제품 속성 및 속성 옵션 번역

1. 다음에서 _관리자_ 사이드바, 이동 **[!UICONTROL Stores]** > _[!UICONTROL Attributes]_>**[!UICONTROL Product]**.

1. 번역할 속성을 선택합니다.

1. 선택 **[!UICONTROL Manage Labels]** 을(를) 왼쪽 버튼으로 설정하고 **[!UICONTROL Managed Titles]** 속성 제목 번역을 정의하는 옵션입니다.

1. 선택 **[!UICONTROL Properties]** 왼쪽에 있는 번역된 속성 옵션을 **[!UICONTROL Manage Options]** 섹션.

   ![옵션 관리](./assets/manage-option-tab.png){width="600" zoomable="yes"}

1. 완료되면 다음을 클릭하십시오. **[!UICONTROL Save Attribute]**.


[1]: https://marketplace.magento.com/extensions/content-customizations/translations-localization.html
[2]: https://experienceleague.adobe.com/docs/commerce-operations/installation-guide/tutorials/extensions.html
