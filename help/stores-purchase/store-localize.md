---
title: 로컬라이제이션 저장
description: 스토어 또는 스토어 보기를 현지화하는 방법에 대해 알아봅니다.
exl-id: 64e1b431-f599-444c-9d39-207bb95f0400
topic: Commerce, Localization
source-git-commit: 248c60b20d8554fc73f94cfd249ac3fd7b677f62
workflow-type: tm+mt
source-wordcount: '725'
ht-degree: 0%

---

# 로컬라이제이션 저장

스토어 전체의 페이지에 하드 코딩된 것으로 보이는 대부분의 텍스트는 보기의 로케일을 변경하여 즉시 다른 언어로 변경할 수 있습니다. 로케일을 변경해도 실제로 텍스트가 단어 단위로 번역되지는 않지만 스토어 전체에 사용되는 인터페이스 텍스트를 제공하는 다른 번역 표를 참조합니다. 변경할 수 있는 텍스트에는 탐색 제목, 레이블, 단추 및 링크(예: _내 장바구니_ 및 _내 계정_)가 포함됩니다. [인라인 번역](../configuration-reference/advanced/developer.md) 도구를 사용하여 인터페이스의 텍스트를 터치할 수도 있습니다.

언어 팩은 Commerce Marketplace의 [번역 및 지역화][1]{:target="_blank"}에서 찾을 수 있습니다. 새로운 확장 기능은 Marketplace에 지속적으로 추가되므로 자주 다시 확인하십시오.

## 1단계: 언어 팩 설치

언어 팩 확장 설치에 대한 표준 지침을 따르십시오. 확장 설치에 대한 자세한 내용은 _확장 안내서_&#x200B;에서 [일반 CLI 설치][2]를 참조하십시오.

## 2단계: 언어에 대한 스토어 보기 만들기

1. _관리자_ 사이드바에서 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL All Stores]**(으)로 이동합니다.

1. **[!UICONTROL Create Store View]**&#x200B;을(를) 클릭합니다.

1. 새 저장소 보기에 대한 옵션을 설정합니다.

   - **[!UICONTROL Store]** — 보기의 상위 저장소를 선택합니다.

   - **[!UICONTROL Name]** — 스토어 보기의 이름을 입력합니다. 예를 들어 포르투갈어입니다.

     스토어의 헤더에서 _언어 선택기_&#x200B;에 이름이 표시됩니다.

   - **[!UICONTROL Code]** — 보기를 식별하는 코드를 소문자로 입력합니다. 예: `portuguese`.

   - **[!UICONTROL Status]** — 보기를 활성화하려면 `Enabled`(으)로 설정합니다.

   - **[!UICONTROL Sort Order]** — (선택 사항) 이 보기가 다른 보기와 함께 나열되는 순서를 결정하는 숫자를 입력합니다.

1. 완료되면 **[!UICONTROL Save Store View]**&#x200B;을(를) 클릭합니다.

## 3단계: 스토어 보기의 로케일 변경

1. _관리자_ 사이드바에서 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**(으)로 이동합니다.

1. **[!UICONTROL Scope]** 드롭다운에서 구성할 저장소 보기를 선택하고 메시지가 표시되면 **[!UICONTROL OK]**&#x200B;을(를) 클릭합니다.

1. *[!UICONTROL General]* 구성 페이지에서 **[!UICONTROL Locale Options]** 섹션의 ![확장 선택기](../assets/icon-display-expand.png)를 확장합니다.

1. **[!UICONTROL Use Website]** 확인란의 선택을 취소하고 보기에 할당할 언어로 **[!UICONTROL Locale]**&#x200B;을(를) 설정합니다.

   사용할 수 있는 언어의 변형이 여러 개 있는 경우 특정 지역이나 언어에 대한 변형을 선택해야 합니다.

1. 완료되면 **[!UICONTROL Save Config]**&#x200B;을(를) 클릭합니다.

   로케일의 언어를 변경하면 각 스토어 보기에 대해 제품 이름 및 설명, 카테고리, [CMS](../content-design/page-translate.md) 페이지 및 블록을 포함하여 만든 나머지 콘텐츠를 개별적으로 번역해야 합니다.

## 제품 현지화

스토어에 서로 다른 언어로 된 보기가 여러 개 있는 경우 각 스토어 보기에서 동일한 제품을 사용할 수 있습니다. 언어에 관계없이 SKU, 가격 및 재고 수준과 같은 동일한 기본 제품 정보를 사용할 수 있습니다. 그런 다음 각 언어에 필요한 제품 이름, 설명 필드 및 메타데이터만 번역합니다.

### 1단계: 제품 필드 번역

1. _관리자_ 사이드바에서 **[!UICONTROL Catalog]** > **[!UICONTROL Products]**(으)로 이동합니다.

1. 그리드에서 번역할 제품을 찾아 편집 모드로 엽니다.

1. 왼쪽 상단 모서리에서 **[!UICONTROL Store View]**&#x200B;을(를) 번역 보기로 설정하고 확인 메시지가 표시되면 **[!UICONTROL OK]**&#x200B;을(를) 클릭합니다.

1. 편집할 각 필드에 대해 다음을 수행합니다.

   - 필드 오른쪽에 있는 **[!UICONTROL Use Default Value]** 확인란의 선택을 취소합니다.

   - 번역된 텍스트를 필드에 붙여넣거나 입력합니다.

   [이미지](../catalog/catalog-images-video.md) 레이블 및 대체 텍스트, [검색 엔진 최적화](../catalog/product-search-engine-optimization.md) 필드 및 [사용자 지정 옵션](../catalog/settings-advanced-custom-options.md) 정보를 포함한 모든 텍스트 필드를 번역해야 합니다.

1. 완료되면 **[!UICONTROL Save]**&#x200B;을(를) 클릭합니다.

### 2단계: 필드 레이블 번역

1. _관리자_ 사이드바에서 **[!UICONTROL Stores]** > _[!UICONTROL Attributes]_>**[!UICONTROL Product]**(으)로 이동합니다.

1. 목록에서 번역할 속성을 찾아 편집 모드로 엽니다.

1. 왼쪽 패널에서 **[!UICONTROL Manage Labels]**&#x200B;을(를) 선택합니다.

1. _[!UICONTROL Manage Titles]_&#x200B;섹션에서 각 스토어 보기에 대해 번역된 레이블을 입력합니다.

   ![번역된 레이블 입력](./assets/product-attribute-labels-translate.png){width="600" zoomable="yes"}

1. 완료되면 **[!UICONTROL Save Attribute]**&#x200B;을(를) 클릭합니다.

### 3단계: 모든 범주 번역

1. _관리자_ 사이드바에서 **[!UICONTROL Catalog]** > **범주**(으)로 이동합니다.

1. 왼쪽 상단 모서리에서 **[!UICONTROL Store View]**&#x200B;을(를) 번역 보기로 설정하고 확인 메시지가 표시되면 **[!UICONTROL OK]**&#x200B;을(를) 클릭합니다.

1. 트리에서 번역할 범주를 찾아 편집 모드로 엽니다.

1. _기본 정보_&#x200B;의 경우 **[!UICONTROL Category Name]**&#x200B;을(를) 번역하세요.

1. _[!UICONTROL Content]_&#x200B;섹션에서 ![확장 선택기](../assets/icon-display-expand.png)를 확장하고&#x200B;**[!UICONTROL Description]**&#x200B;을(를) 번역합니다.

1. **[!UICONTROL Search Engine Optimization Settings]** 섹션에서 ![확장 선택기](../assets/icon-display-expand.png)를 확장하고 다음 필드를 번역합니다.

   - **[!UICONTROL Meta Title]**
   - **[!UICONTROL Meta Keywords]**
   - **[!UICONTROL Meta Description]**

1. _[!UICONTROL Search Engine Optimization Settings]_&#x200B;섹션에서 다음을 수행하여&#x200B;**[!UICONTROL URL Key]**&#x200B;을(를) 번역합니다.

   - 필드의 오른쪽에 있는 **[!UICONTROL Use Default Value]** 확인란의 선택을 취소합니다.

   - 번역된 텍스트를 입력합니다.

   - **[!UICONTROL Create Permanent Redirect for old URL]** 확인란이 선택되어 있는지 확인하십시오.

   ![URL 키 번역](./assets/category-translate-url-key.png)

1. 완료되면 **[!UICONTROL Save Category]**&#x200B;을(를) 클릭합니다.

1. 스토어에서 사용되는 모든 카테고리에 대해 이 프로세스를 반복합니다.

### 4단계: 제품 속성 및 속성 옵션 번역

1. _관리자_ 사이드바에서 **[!UICONTROL Stores]** > _[!UICONTROL Attributes]_>**[!UICONTROL Product]**(으)로 이동합니다.

1. 번역할 속성을 선택합니다.

1. 왼쪽에서 **[!UICONTROL Manage Labels]**&#x200B;을(를) 선택하고 **[!UICONTROL Managed Titles]** 옵션을 설정하여 속성 제목 번역을 정의합니다.

1. 왼쪽의 **[!UICONTROL Properties]**&#x200B;을(를) 선택하고 **[!UICONTROL Manage Options]** 섹션에 번역된 특성 옵션을 입력하십시오.

   ![옵션 관리](./assets/manage-option-tab.png){width="600" zoomable="yes"}

1. 완료되면 **[!UICONTROL Save Attribute]**&#x200B;을(를) 클릭합니다.


[1]: https://marketplace.magento.com/extensions/content-customizations/translations-localization.html
[2]: https://experienceleague.adobe.com/docs/commerce-operations/installation-guide/tutorials/extensions.html?lang=ko
