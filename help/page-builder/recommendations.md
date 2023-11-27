---
title: 컨텐츠 추가 - 제품 Recommendations
description: 에 권장 사항 목록을 추가하는 데 사용되는 Product Recommendations 콘텐츠 유형에 대해 알아봅니다. [!DNL Page Builder] 스테이지.
exl-id: ca90c10d-8d7a-42a2-bb13-2602aa9d6eef
feature: Page Builder, Page Content, Recommendations
source-git-commit: 13d00168e1253a7d2698b898caa30d9ca2ad3800
workflow-type: tm+mt
source-wordcount: '950'
ht-degree: 0%

---

# 컨텐츠 추가 - 제품 Recommendations

사용 _제품 Recommendations_ 기존 활성 콘텐츠를 추가할 콘텐츠 유형 [추천 단위](https://experienceleague.adobe.com/docs/commerce-merchant-services/product-recommendations/admin/create.html) (으)로 [[!DNL Page Builder] 단계](workspace.md#stage) CMS 페이지, 블록 또는 동적 블록의 경우.

>[!NOTE]
>
>다음 [!DNL Page Builder] _제품 Recommendations_ 컨텐츠 유형은 Adobe Commerce 2.4.4 이상에서 지원되며 다음에서 사용할 수 있습니다. [제품 Recommendations 메타패키지 버전 3.0.x 이상](https://marketplace.magento.com/magento-product-recommendations.html). 추가하려면 [!DNL Page Builder] 제품 Recommendations 지원, [설치 정보 보기](https://experienceleague.adobe.com/docs/commerce-merchant-services/product-recommendations/getting-started/install-configure.html#pbsupport). **이 컨텐츠 유형은 Magento Open Source에 사용할 수 없습니다.**

{{$include /help/_includes/page-builder-save-timeout.md}}

## 제품 Recommendations 도구 상자

| 도구 | 아이콘 | 설명 |
| --- | --| --- |
| 이동 | ![이동 아이콘](./assets/pb-icon-move.png){width="25"} | 제품 추천 컨테이너 및 해당 콘텐츠를 스테이지의 다른 위치로 이동합니다. |
| 설정 | ![설정 아이콘](./assets/pb-icon-settings.png){width="25"} | 추천 단위를 선택하고 컨테이너의 속성을 변경할 수 있는 제품 추천 편집 페이지를 엽니다. |
| 숨기기 | ![아이콘 숨기기](./assets/pb-icon-hide.png){width="25"} | 현재 제품 추천 컨테이너 및 해당 콘텐츠를 숨깁니다. |
| 표시 | ![아이콘 표시](./assets/pb-icon-show.png){width="25"} | 숨겨진 제품 추천 컨테이너 및 해당 콘텐츠를 표시합니다. |
| 복제 | ![중복 아이콘](./assets/pb-icon-duplicate.png){width="25"} | 제품 추천 컨테이너 및 해당 콘텐츠의 복사본을 만듭니다. |
| 제거 | ![제거 아이콘](./assets/pb-icon-remove.png){width="25"} | 스테이지에서 제품 추천 컨테이너 및 해당 콘텐츠를 삭제합니다. |

{style="table-layout:auto"}

{{$include /help/_includes/page-builder-hidden-element-note.md}}

## 기존 추천 단위 추가

1. 이미 가지고 있는지 확인하십시오. [추천 단위를 만들었습니다.](https://experienceleague.adobe.com/docs/commerce-merchant-services/product-recommendations/admin/create.html) 대상: [!DNL Page Builder] 페이지 유형.

>[!NOTE]
>
>다음에 대한 추천 단위를 만들 수 있습니다. [!DNL Page Builder] 기본 저장소 보기에서만 페이지 유형을 사용할 수 있습니다.

1. 편집 모드로 페이지, 블록 또는 동적 블록을 엽니다.

1. 확장 _[!UICONTROL Content]_섹션 및 클릭&#x200B;**[!UICONTROL Edit with Page Builder]**또는 콘텐츠 미리보기 영역 내에서 [!DNL Page Builder] 작업 영역.

1. 다음에서 [!DNL Page Builder] 패널 아래 _[!UICONTROL Layout]_, 드래그&#x200B;**[!UICONTROL Row]**자리 표시자가 스테이지에 표시됩니다.

1. 다음에서 [!DNL Page Builder] 패널 아래 _[!UICONTROL Add Content]_, 드래그&#x200B;**[!UICONTROL Product Recommendation]**행 자리 표시자

   ![제품 추천 콘텐츠 유형 추가](./assets/pb-add-prex-drag.png){width="600" zoomable="yes"}

1. 다음 중 하나를 수행합니다.

   - 클릭 **[!UICONTROL Edit Product Recommendation]**.
   - 빈 컨테이너에 마우스를 가져다 대고 도구 상자를 표시한 다음 _설정_ (![설정 아이콘](./assets/pb-icon-settings.png){width="20"} ) 아이콘.

   ![제품 추천 편집](./assets/pb-prex-toolbox.png){width="600" zoomable="yes"}

1. 다음에서 _[!UICONTROL Selection]_섹션, 클릭&#x200B;**[!UICONTROL Select]**.

1. 활성 제품 권장 사항 목록에서 추가하려는 권장 사항 단위가 있는 행을 찾아 **[!UICONTROL Select]** 마지막 열에서

   ![선택한 제품 추천](./assets/pb-prex-select.png){width="600" zoomable="yes"}

1. 오른쪽 위 모서리에서 을(를) 클릭합니다. **[!UICONTROL Add Selected]**.

   선택한 제품 추천의 이름이 _[!UICONTROL Selection]_의 섹션_[!UICONTROL Edit Product Recommendation]_ 페이지를 가리키도록 업데이트하는 중입니다.

1. 필요한 변경 작업을 수행합니다. [고급 설정](#advanced-settings).

   ![제품 추천 편집](./assets/pb-prex-edit.png){width="600" zoomable="yes"}

1. 완료되면 다음을 수행합니다.

   - 브라우저 창을 최대화한 채 작업하는 경우 _전체 화면 닫기_ (![전체 화면 아이콘 닫기](./assets/pb-icon-reduce.png)) 아이콘은 작업 공간의 오른쪽 위 모서리에 있습니다.

   - 클릭 **[!UICONTROL Save]** 설정을 적용하고 로 돌아가려면 [!DNL Page Builder] 작업 영역.

   스테이지로 돌아가면 제품 자리 표시자 이미지가 컨테이너에 나타납니다.

## 추천 단위 설정 편집

1. 권장 사항 단위 컨테이너에 마우스를 가져다 대고 도구 상자를 표시한 다음 _설정_ (![설정 아이콘](./assets/pb-icon-settings.png){width="20"} ) 아이콘.

   ![권장 사항 도구 상자](./assets/pb-placeholder-toolbox.png){width="600" zoomable="yes"}

1. 필요한 변경 작업을 수행합니다. [고급 설정](#advanced-settings).

1. 완료되면 다음을 클릭하십시오. **[!UICONTROL Save]** 설정을 적용하고 로 돌아가려면 [!DNL Page Builder] 작업 영역.

## 추천 단위 복제

1. 권장 사항 단위 컨테이너에 마우스를 가져다 대고 도구 상자를 표시한 다음 _복제_ ( ![인스턴스 복제](./assets/pb-icon-duplicate.png){width="20"} ) 아이콘을 클릭합니다.

   복제본이 원본 바로 아래에 나타납니다.

1. 복제된 추천 단위를 새 위치로 이동하려면 컨테이너를 마우스로 가리킨 다음 _이동_ ( ![이동 아이콘](./assets/pb-icon-move.png){width="20"} ) 아이콘을 클릭합니다.

1. 빨간색 지침이 새 위치에 나타날 때까지 추천 단위를 선택하고 드래그합니다.

   각 컨테이너의 위쪽 및 아래쪽 테두리는 추천 단위가 이동하는 동안 파선으로 표시됩니다.

## 스테이지에서 추천 단위 제거

1. 추천 단위 컨테이너 위로 마우스를 가져간 후 _제거_ ( ![제거 아이콘](./assets/pb-icon-remove.png){width="20"} ) 아이콘을 클릭합니다.

1. 확인을 묻는 메시지가 나타나면 **[!UICONTROL OK]**.

## 고급 설정

1. 상위 컨테이너 내에서 제품 Recommendations 장치의 위치를 제어하려면 **[!UICONTROL Alignment]**:

   | 옵션 | 설명 |
   | ------ | ----------- |
   | `Default` | 현재 테마의 스타일시트에 지정된 정렬 기본 설정을 적용합니다. |
   | `Left` | 지정된 패딩을 허용하여 부모 컨테이너의 왼쪽 테두리를 따라 단위를 정렬합니다. |
   | `Center` | 부모 컨테이너의 중앙에 있는 단위를 지정된 패딩에 대한 허용으로 맞춥니다. |
   | `Right` | 지정된 패딩을 허용하여 부모 컨테이너의 오른쪽 테두리를 따라 단위를 정렬합니다. |

   {style="table-layout:auto"}

1. 설정 **[!UICONTROL Border]** 제품 Recommendations 단위의 네 면에 모두 적용되는 스타일:

   | 옵션 | 설명 |
   | ------ | ----------- |
   | `Default` | 연관된 스타일 시트에서 지정한 기본 테두리 스타일을 적용합니다. |
   | `None` | 장치 테두리를 시각적으로 표시하지 않습니다. |
   | `Dotted` | 장치 테두리가 점선으로 표시됩니다. |
   | `Dashed` | 단위 테두리는 파선으로 표시됩니다. |
   | `Solid` | 단위 테두리는 실선으로 표시됩니다. |
   | `Double` | 단위 테두리는 이중 선으로 표시됩니다. |
   | `Groove` | 단위 테두리는 홈이 있는 선으로 표시됩니다. |
   | `Ridge` | 단위 테두리는 절선으로 표시됩니다. |
   | `Inset` | 단위 테두리는 인세트 선으로 표시됩니다. |
   | `Outset` | 단위 테두리는 외곽선으로 표시됩니다. |

   {style="table-layout:auto"}

1. 테두리 스타일을 설정할 때 `None`테두리 표시 옵션을 완료합니다.

   | 옵션 | 설명 |
   | ------ |------------ |
   | [!UICONTROL Border Color] | 색상 견본을 선택하거나 색상 선택기를 클릭하거나 유효한 색상 이름 또는 이에 해당하는 16진수 값을 입력하여 색상을 지정합니다. |
   | [!UICONTROL Border Width] | 테두리 라인 너비의 픽셀 수를 입력합니다. |
   | [!UICONTROL Border Radius] | 테두리의 각 모퉁이를 둥글게 만드는 데 사용되는 반경의 크기를 정의하려면 픽셀 수를 입력합니다. |

   {style="table-layout:auto"}

1. (선택 사항) 다음 이름을 지정합니다 **[!UICONTROL CSS classes]** 현재 스타일 시트에서 단위에 적용할 수 있습니다.

   여러 클래스 이름은 공백으로 구분합니다.

1. 다음에 대한 값을 픽셀 단위로 입력하십시오. **[!UICONTROL Margins and Padding]** 을 클릭하여 장치의 외부 여백 및 내부 패딩을 결정합니다.

   다이어그램에 해당 값을 입력합니다.

   | 컨테이너 영역 | 설명 |
   | ------ | ----------- |
   | [!UICONTROL Margins] | 장치의 모든 면 바깥쪽 가장자리에 적용되는 빈 공간의 양입니다. 옵션: `Top` / `Right` / `Bottom` / `Left` |
   | [!UICONTROL Padding] | 장치의 모든 측면 안쪽 가장자리에 적용되는 빈 공간의 양입니다. 옵션: `Top` / `Right` / `Bottom` / `Left` |

   {style="table-layout:auto"}
