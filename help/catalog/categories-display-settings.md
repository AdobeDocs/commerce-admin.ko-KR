---
title: 카테고리 - 표시 설정
description: '[!UICONTROL Display] 설정을 사용하여 범주 페이지에 표시할 콘텐츠 요소와 제품이 표시되는 순서를 정의하는 방법에 대해 알아봅니다.'
exl-id: bb3a1b00-ba56-4113-8208-860963612333
feature: Catalog Management, Categories, Page Content
TQID: https://experienceleague.adobe.com/t5UfvWvJ7R-kZb5kyMwpzwI2gfs3x3g1amlfWzQcAsw
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2:
  - id: c18ed297-2187-4aec-affb-9d9654eca6fc
subfeature_v2:
  - id: e91a50b1-0b31-436e-9033-00e4776e94cb
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: f8a45b24-4be7-4f1b-909b-60d06b483a20
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2:
  - id: cdd65e7e-8839-44a2-bc21-0e03623b5dd1
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 247
ht-degree: 0%

---

# 카테고리 - 표시 설정

표시 설정은 카테고리 페이지에 표시되는 콘텐츠 요소와 제품이 표시되는 순서를 결정합니다. _[!UICONTROL Display Settings]_&#x200B;탭에서 CMS 블록을 사용하도록 설정하고, 범주의 앵커 상태를 설정하고, 정렬 옵션을 관리할 수 있습니다. 카테고리가 상점 앞에 반영되는 방식에 대한 예는 [카탈로그 탐색](navigation.md)을 참조하십시오.

![범주에 대한 표시 설정](./assets/category-display-settings.png){width="600" zoomable="yes"}

| 필드 | 설명 |
|--- |--- |
| [!UICONTROL Display Mode] | 카테고리 페이지에 표시되는 콘텐츠 요소를 결정합니다. 옵션: `Products Only` / `Static Block Only` / `Static Block and Products` |
| [!UICONTROL Anchor] | `Yes`(으)로 설정된 경우 는 카테고리에 명시적으로 추가되지 않았더라도 카테고리의 하위 카테고리에 있는 제품을 표시하고 계층화된 탐색에서 _[!UICONTROL filter by attribute]_&#x200B;섹션을 표시할 수 있도록 합니다. 옵션: `Yes` / `No` |
| [!UICONTROL Available Product Listing Sort By] | (필수) 기본값은 `Position`, `Name` 및 `Price`입니다. 정렬 옵션을 사용자 지정하려면 **[!UICONTROL Use All Available Attributes]** 확인란의 선택을 취소하고 사용할 특성을 선택합니다. 필요에 따라 속성을 정의하고 추가할 수 있습니다. 이 설정은 [!DNL Live Search] [제품 목록 페이지 위젯](https://experienceleague.adobe.com/ko/docs/commerce/live-search/live-search-storefront/plp-styling)에 적용되지 않습니다. |
| [!UICONTROL Default Product Listing Sort By] | (필수) 기본 _[!UICONTROL Sort By]_&#x200B;옵션을 정의하려면&#x200B;**[!UICONTROL Use Config Settings]**&#x200B;확인란의 선택을 취소하고 특성을 선택합니다. 이 설정은 [!DNL Live Search] [제품 목록 페이지 위젯](https://experienceleague.adobe.com/ko/docs/commerce/live-search/live-search-storefront/plp-styling)에 적용되지 않습니다. |
| [!UICONTROL Layered Navigation Price Step] | 기본적으로 Commerce은 목록에 있는 제품에 따라 가격 범위를 10, 100 및 1000 단위로 표시합니다. 가격 단계 범위를 변경하려면 **[!UICONTROL Use Config Settings]** 확인란의 선택을 취소하십시오. |

{style="table-layout:auto"}
