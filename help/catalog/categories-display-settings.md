---
title: 카테고리 - 표시 설정
description: '[!UICONTROL Display] 설정을 사용하여 범주 페이지에 표시할 콘텐츠 요소와 제품이 표시되는 순서를 정의하는 방법에 대해 알아봅니다.'
exl-id: bb3a1b00-ba56-4113-8208-860963612333
feature: Catalog Management, Categories, Page Content
source-git-commit: 5da244a548b15863fe31b5df8b509f8e63df27c2
workflow-type: tm+mt
source-wordcount: '224'
ht-degree: 0%

---

# 카테고리 - 표시 설정

표시 설정은 카테고리 페이지에 표시되는 콘텐츠 요소와 제품이 표시되는 순서를 결정합니다. _[!UICONTROL Display Settings]_탭에서 CMS 블록을 사용하도록 설정하고, 범주의 앵커 상태를 설정하고, 정렬 옵션을 관리할 수 있습니다. 카테고리가 상점 앞에 반영되는 방식에 대한 예는 [카탈로그 탐색](navigation.md)을 참조하십시오.

![범주에 대한 표시 설정](./assets/category-display-settings.png){width="600" zoomable="yes"}

| 필드 | 설명 |
|--- |--- |
| [!UICONTROL Display Mode] | 카테고리 페이지에 표시되는 콘텐츠 요소를 결정합니다. 옵션: `Products Only` / `Static Block Only` / `Static Block and Products` |
| [!UICONTROL Anchor] | `Yes`(으)로 설정된 경우 는 카테고리에 명시적으로 추가되지 않았더라도 카테고리의 하위 카테고리에 있는 제품을 표시하고 계층화된 탐색에서 _[!UICONTROL filter by attribute]_섹션을 표시할 수 있도록 합니다. 옵션: `Yes` / `No` |
| [!UICONTROL Available Product Listing Sort By] | (필수) 기본값은 `Position`, `Name` 및 `Price`입니다. 정렬 옵션을 사용자 지정하려면 **[!UICONTROL Use All Available Attributes]** 확인란의 선택을 취소하고 사용할 특성을 선택합니다. 필요에 따라 속성을 정의하고 추가할 수 있습니다. 이 설정은 [!DNL Live Search] [제품 목록 페이지 위젯](https://experienceleague.adobe.com/en/docs/commerce/live-search/live-search-storefront/plp-styling)에 적용되지 않습니다. |
| [!UICONTROL Default Product Listing Sort By] | (필수) 기본 _[!UICONTROL Sort By]_옵션을 정의하려면&#x200B;**[!UICONTROL Use Config Settings]**확인란의 선택을 취소하고 특성을 선택합니다. 이 설정은 [!DNL Live Search] [제품 목록 페이지 위젯](https://experienceleague.adobe.com/en/docs/commerce/live-search/live-search-storefront/plp-styling)에 적용되지 않습니다. |
| [!UICONTROL Layered Navigation Price Step] | 기본적으로 Commerce은 목록에 있는 제품에 따라 가격 범위를 10, 100 및 1000 단위로 표시합니다. 가격 단계 범위를 변경하려면 **[!UICONTROL Use Config Settings]** 확인란의 선택을 취소하십시오. |

{style="table-layout:auto"}
