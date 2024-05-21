---
title: 카테고리 - 표시 설정
description: 사용에 대해 알아보기 [!UICONTROL Display] 카테고리 페이지에 표시되는 콘텐츠 요소 및 제품이 표시되는 순서를 정의하는 설정입니다.
exl-id: bb3a1b00-ba56-4113-8208-860963612333
feature: Catalog Management, Categories, Page Content
source-git-commit: a47e744cf4cc5163ca2ba0718ccb78eb65a7d404
workflow-type: tm+mt
source-wordcount: '224'
ht-degree: 0%

---

# 카테고리 - 표시 설정

표시 설정은 카테고리 페이지에 표시되는 콘텐츠 요소와 제품이 표시되는 순서를 결정합니다. CMS 블록을 활성화하고, 범주의 앵커 상태를 설정하고, _[!UICONTROL Display Settings]_탭. 카테고리가 상점 앞에 반영되는 방식에 대한 예는 다음을 참조하십시오. [카탈로그 탐색](navigation.md).

![범주에 대한 설정 표시](./assets/category-display-settings.png){width="600" zoomable="yes"}

| 필드 | 설명 |
|--- |--- |
| [!UICONTROL Display Mode] | 카테고리 페이지에 표시되는 콘텐츠 요소를 결정합니다. 옵션: `Products Only` / `Static Block Only` / `Static Block and Products` |
| [!UICONTROL Anchor] | 로 설정된 경우 `Yes`는 카테고리에 명시적으로 추가되지 않았더라도 카테고리의 하위 카테고리 제품을 표시하고 의 표시를 활성화합니다. _[!UICONTROL filter by attribute]_레이어 탐색의 섹션입니다. 옵션: `Yes` / `No` |
| [!UICONTROL Available Product Listing Sort By] | (필수) 기본값은 입니다. `Position`, `Name`, 및 `Price`. 정렬 옵션을 사용자 정의하려면 **[!UICONTROL Use All Available Attributes]** 확인란을 선택하고 사용할 속성을 선택합니다. 필요에 따라 속성을 정의하고 추가할 수 있습니다. 이 설정은 [!DNL Live Search] [제품 목록 페이지 위젯](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/live-search/live-search-storefront/plp-styling). |
| [!UICONTROL Default Product Listing Sort By] | (필수) 기본값을 정의하려면 _[!UICONTROL Sort By]_옵션을 선택한 다음&#x200B;**[!UICONTROL Use Config Settings]**확인란을 선택하고 속성을 선택합니다. 이 설정은 [!DNL Live Search] [제품 목록 페이지 위젯](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/live-search/live-search-storefront/plp-styling). |
| [!UICONTROL Layered Navigation Price Step] | 기본적으로 Commerce은 목록에 있는 제품에 따라 가격 범위를 10, 100 및 1000 단위로 표시합니다. 가격 단계 범위를 변경하려면 다음을 선택 취소합니다. **[!UICONTROL Use Config Settings]** 확인란. |

{style="table-layout:auto"}
