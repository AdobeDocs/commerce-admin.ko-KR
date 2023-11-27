---
title: 미디어 - 맵
description: 다음에서 맵을 추가하는 데 사용되는 맵 콘텐츠 유형에 대해 알아봅니다. [!DNL Google Maps] 플랫폼으로 이동 [!DNL Page Builder] 스테이지.
exl-id: 91fea8f8-d48a-43f1-ba2a-212c7130cee9
feature: Page Builder, Page Content
source-git-commit: 167e9d906cebb645f76a5112fa629a73ba823ebc
workflow-type: tm+mt
source-wordcount: '1583'
ht-degree: 0%

---

# 미디어 - 맵

사용 _맵_ 맵을 추가할 콘텐츠 유형 [[!DNL Google Maps] 플랫폼][1] (으)로 [[!DNL Page Builder] 단계](workspace.md#stage). 예를 들어 블록에 맵을 추가한 다음 블록을 [정보](../content-design/pages.md#about-us) 및 [연락처](../getting-started/store-details.md#contact-us-form) 페이지.

을 최대한 활용하려면 [!DNL Google Maps] 플랫폼, 맵을 사용자 지정하고, 스토어 위치를 강조 표시하고, Google을 사용할 수 있습니다. [위치][2] 저장소에 대한 다양한 정보를 모두 추가하려면 [!DNL Google Maps].

## Google 맵 포함의 이점

1. 구매자에게 사이트에 대한 모든 범위의 정보(전화 번호, 웹 사이트, 리뷰, 별점 등)를 제공합니다.

1. Google 지도는 일반적으로 인근 명소, 공원, 레스토랑 등을 강조 표시합니다. 이 정보는 고객이 실제 위치를 결정하고 여행을 계획하는 데 도움이 됩니다.

1. 고객이 새 브라우저 창을 열고 사이트를 떠날 필요 없이 실제 스토어의 주소를 쉽게 찾을 수 있습니다.

1. 물리적 스토어 체인이 있는 경우 사이트에 Google 맵을 추가하면 강조 표시된 항목의 형태로 브랜드 인지도와 신뢰성을 높이는 데 도움이 됩니다.

![예제 storefront - 위치를 사용한 맵](./assets/pb-media-maps-storefront.png){width="700" zoomable="yes"}

{{$include /help/_includes/page-builder-save-timeout.md}}

## 맵 도구 상자

맵 컨테이너 위로 마우스를 가져가면 맵 도구 상자가 나타납니다.

| 도구 | 아이콘 | 설명 |
|--- |--- |--- |
| 이동 | ![이동 아이콘](./assets/pb-icon-move.png){width="25"} | 맵을 스테이지의 다른 위치로 이동합니다. |
| (레이블) | [!UICONTROL Map] | 현재 콘텐츠 컨테이너를 맵으로 식별합니다. 맵 컨테이너 위로 마우스를 가져가면 도구 상자를 볼 수 있습니다. |
| 설정 | ![설정 아이콘](./assets/pb-icon-settings.png){width="25"} | 맵과 컨테이너의 속성을 변경할 수 있는 맵 편집 페이지를 엽니다. |
| 숨기기 | ![아이콘 숨기기](./assets/pb-icon-hide.png){width="25"} | 현재 맵을 숨깁니다. |
| 표시 | ![아이콘 표시](./assets/pb-icon-show.png){width="25"} | 숨겨진 맵을 표시합니다. |
| 복제 | ![중복 아이콘](./assets/pb-icon-duplicate.png){width="25"} | 맵을 복사합니다. |
| 제거 | ![제거 아이콘](./assets/pb-icon-remove.png){width="25"} | 스테이지에서 맵을 삭제합니다. |

{style="table-layout:auto"}

{{$include /help/_includes/page-builder-hidden-element-note.md}}

## 구성 [!DNL Google Maps] 관리자용

맵을 추가하기 전에 먼저 [account][3] 의 무료 체험판을 위하여 [!DNL Google Maps] 플랫폼. 무료 체험은 12개월 동안 지속되며 300달러의 크레딧이 포함됩니다. 크레딧을 소진하면 Google에서 귀하의 허가 없이 귀하의 계정에 청구하지 않습니다.

### 1단계: 가져오기 [!DNL Google Maps] API 키

이미 다음 항목이 있는지 여부에 따라 [!DNL Google Maps] 키, 다음 절차 중 하나를 사용하여 구성에 필요한 API 키를 가져옵니다. 을(를) 설정하려면 [!DNL Google Maps] 키. 계정에 대한 결제를 활성화할 수 있는 권한이 있는 사이트 관리자여야 합니다. 을(를) 설정할 준비가 되지 않았다면 [!DNL Google Maps] Platform 계정에서 이 단계를 건너뛰고 지금은 자리 표시자 맵을 사용할 수 있습니다.

1. 로 이동 [Google 클라우드 플랫폼 콘솔](https://cloud.google.com/console/google/maps-apis/overview).

1. 프로젝트 드롭다운을 클릭하고 API 키를 추가할 프로젝트를 선택하거나 만듭니다.

1. API 자격 증명을 구성하려면 다음을 수행합니다. [지침][4] 다음에서 [!DNL Google Maps] 설명서를 참조하십시오.

1. API 키를 클립보드에 복사합니다.

### 2단계: 구성 [!DNL Google Maps] 위치: [!DNL Commerce]

1. 다음에서 _관리자_ 사이드바, 이동 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. 아래의 왼쪽 패널에서 _[!UICONTROL General]_, 선택&#x200B;**[!UICONTROL Content Management]**.

1. 확장 ![확장 선택기](../assets/icon-display-expand.png) **[!UICONTROL Advanced Content Tools]**.

   ![고급 콘텐츠 도구](../configuration-reference/general/assets/content-management-advanced-content-tools.png){width="600" zoomable="yes"}

   콘텐츠 관리 고급 도구 구성 옵션에 대한 자세한 내용은 [구성 참조 안내서](../configuration-reference/general/content-management.md).

1. 대상 **[!UICONTROL Google Maps API Key]** 1단계에서 복사한 키를 붙여넣습니다.

1. 클릭 **[!UICONTROL Test Key]**.

   키에 문제가 있는 경우 [!DNL Google Maps] 플랫폼 사이트로 이동하여 문제를 해결하십시오. 그런 다음 다시 시도하십시오.

1. 키를 확인한 후 **[!UICONTROL Save Config]**.

## 스테이지에 맵 추가

1. 페이지, 블록 또는 동적 블록을 열고 [!DNL Page Builder] 작업 영역.

1. 다음에서 [!DNL Page Builder] 패널, 확장 **[!UICONTROL Media]** 드래그 **[!UICONTROL Map]** 자리 표시자가 스테이지에 표시됩니다.

   ![스테이지로 맵 드래그](./assets/pb-media-map-drag.png){width="600" zoomable="yes"}

   If [!DNL Google Maps] 플랫폼이 스토어에 대해 구성되면 스토어 위치에 대한 맵이 표시됩니다.

   ![[!DNL Google Maps]](./assets/pb-tutorial2-google-map.png){width="600" zoomable="yes"}

   If [!DNL Google Maps] 스토어에 대해 플랫폼이 아직 구성되지 않았습니다. 대신 자리 표시자 맵이 표시됩니다.

   ![[!DNL Google Maps] 자리 표시자](./assets/pb-tutorial2-media-map-not-configured.png){width="600" zoomable="yes"}

## 사용자 정의 맵 위치 추가

1. 맵 컨테이너 위로 마우스를 가져가 도구 상자를 표시하고 _설정_ ( ![설정 아이콘](./assets/pb-icon-settings.png){width="20"} ) 아이콘.

1. 의 오른쪽 위 모서리에서 _[!UICONTROL Edit Map]_페이지, 클릭&#x200B;**[!UICONTROL Add Location]**.

1. 다음을 입력합니다. **[!UICONTROL Location Name]** 지도에서 pin과 연결하려고 합니다.

1. 사용자 지정 위치에 사용할 위치 좌표를 수집합니다.

   또는 **[!UICONTROL Position]** 상자에서 표시된 맵의 핀을 드래그할 수 있습니다.

   필요한 경우 [[!DNL Google Maps]][5] 새 브라우저 창에서 다음 방법 중 하나를 사용하여 좌표를 가져옵니다.

   ![맵 좌표](./assets/pb-media-maps-settings-add-location-coordinates.png){width="600" zoomable="yes"}

   **방법 1:** URL에서 복사

   - 왼쪽 상단 모서리에서 **[!UICONTROL Search]** 상자를 클릭하고 _검색_ ( ![검색 아이콘](../assets/icon-magnify-search.png){width="20"} ) 아이콘.

   - URL에서 좌표를 복사하여 메모장에 붙여넣습니다.

   **방법 2:** &quot;여기 뭐가 있지?&quot;에서 복사해

   - 지도에서 위치를 표시하는 빨간색 핀을 마우스 오른쪽 단추로 클릭하고 를 선택합니다 **[!UICONTROL What's here?]** 메뉴에서 을 클릭합니다.

   - 표시된 레이블에서 좌표를 포함한 텍스트를 복사하여 메모장에 붙여넣습니다.

1. 각 필드에 쉼표 없이 숫자를 입력합니다. **[!UICONTROL Coordinates]** 상자.

   나머지 정보 중 맵에 사용할 수 있는 만큼만 입력할 수도 있습니다.

1. 맵 위치와 연결할 다른 모든 정보를 비교합니다.

   | 옵션 | 설명 |
   | ------ | ----------- |
   | [!UICONTROL Phone Number] | 위치의 전화 번호입니다. |
   | [!UICONTROL Street Address] | 위치의 거리 주소입니다. |
   | [!UICONTROL City] | 위치의 도시입니다. |
   | [!UICONTROL Region/State] | 위치의 지역 또는 상태입니다. |
   | [!UICONTROL Zip/Postal Code] | 위치의 ZIP 또는 우편 번호입니다. |
   | [!UICONTROL Country] | 위치의 국가입니다. |
   | [!UICONTROL Comment] | 포함할 모든 주석입니다. |

   {style="table-layout:auto"}

1. 완료되면 다음을 클릭하십시오. **[!UICONTROL Save]**.

   새 위치는 맵과 의 맵 위치 그리드에 나타납니다. _[!UICONTROL Edit Map]_페이지를 가리키도록 업데이트하는 중입니다.

   ![[!DNL Page Builder] - 위치 그리드 매핑](./assets/pb-media-maps-settings-add-location-grid.png){width="600" zoomable="yes"}

## 맵 스타일 지정 {#styling}

사용 [!DNL Google Maps] 미리 정의된 6개의 테마 중 하나를 적용하거나 사용자 지정 테마를 만드는 플랫폼 스타일 지정 마법사 맵 스타일 속성 또는 스타일이 지정된 맵에 대한 링크를 사용하여 JSON 파일을 생성할 수 있습니다.

### 맵 스타일 변경

1. 다음에서 _관리자_ 사이드바, 이동 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. 아래의 왼쪽 패널에서 _[!UICONTROL General]_, 선택&#x200B;**[!UICONTROL Content Management]**.

1. 확장 ![확장 선택기](../assets/icon-display-expand.png) **[!UICONTROL Advanced Content Tools]**.

1. 아래 **[!UICONTROL Google Maps Style]** 텍스트 상자에서 [맵 스타일 만들기][6].

   이 작업을 수행하면 [[!DNL Google Maps] 플랫폼 스타일 마법사][6] 에 대한 스타일을 정의할 수 있는 별도의 탭에서 [!DNL Google Maps] 플랫폼 프로젝트.

1. 클릭 **[!UICONTROL Create a Style]** 제공된 지침을 따르십시오.

   완료되면 다음을 클릭하십시오. **[!UICONTROL Finish]**.

1. 완료된 스타일을 JSON 코드 또는 URL로 내보내 [!DNL Commerce] 구성.

   - **JSON**: 생성된 JSON 코드가 있는 상자 아래에서 **[!UICONTROL Copy JSON]**.

   - **[!UICONTROL URL]**: 생성된 URL이 있는 상자 아래에서 **[!UICONTROL Copy URL]**.

1. 관리 브라우저 탭으로 돌아가서 생성된 코드 또는 URL을 **Google 맵 스타일** 상자.

   URL을 사용하는 경우 `YOUR_API_KEY` 을(를) 사용한 자리 표시자 [!DNL Google Maps] API 키. 이 URL은 스타일이 지정된 Google 맵에 연결됩니다.

1. 오른쪽 위 모서리에서 을(를) 클릭합니다. **[!UICONTROL Save Config]**.

### 맵 설정 변경

1. 맵 컨테이너 위로 마우스를 가져가면 도구 상자가 표시되고 _설정_ ( ![설정 아이콘](./assets/pb-icon-settings.png){width="20"} ) 아이콘.

1. 필요에 따라 기본 설정을 변경합니다.

   | 옵션 | 설명 |
   | ------ | ----------- |
   | [!UICONTROL Height] | 표시된 지도의 높이를 픽셀 단위로 지정합니다. |
   | [!UICONTROL Show Controls] | 표준 Google 맵 컨트롤이 표시되는지 여부를 결정합니다. |

   {style="table-layout:auto"}

1. 수정 _[!UICONTROL Advanced]_필요한 경우 설정:

   - 컨테이너에 추가된 맵 콘텐츠의 가로 위치를 제어하려면 **[!UICONTROL Alignment]**:

     | 옵션 | 설명 |
     | ------ | ----------- |
     | `Default` | 현재 테마의 스타일시트에 지정된 정렬 기본 설정을 적용합니다. |
     | `Left` | 지정된 패딩을 허용하여 맵 컨테이너의 왼쪽 테두리를 따라 콘텐츠를 정렬합니다. |
     | `Center` | 지정된 패딩을 허용하여 맵 컨테이너의 가운데에 내용을 맞춥니다. |
     | `Right` | 지정된 패딩을 허용하여 맵 컨테이너의 오른쪽 테두리를 따라 콘텐츠를 정렬합니다. |

     {style="table-layout:auto"}

   - 설정 **[!UICONTROL Border]** 맵 컨테이너의 네 면에 적용된 스타일:

     | 옵션 | 설명 |
     | ------ | ----------- |
     | `Default` | 연관된 스타일 시트에서 지정한 기본 테두리 스타일을 적용합니다. |
     | `None` | 컨테이너 테두리를 시각적으로 표시하지 않습니다. |
     | `Dotted` | 컨테이너 테두리가 점선으로 표시됩니다. |
     | `Dashed` | 컨테이너 테두리는 파선으로 표시됩니다. |
     | `Solid` | 컨테이너 테두리가 실선으로 표시됩니다. |
     | `Double` | 컨테이너 테두리는 이중 선으로 표시됩니다. |
     | `Groove` | 컨테이너 테두리는 홈이 있는 선으로 표시됩니다. |
     | `Ridge` | 컨테이너 테두리는 절선으로 표시됩니다. |
     | `Inset` | 컨테이너 테두리는 인세트 선으로 표시됩니다. |
     | `Outset` | 컨테이너 테두리는 외곽선으로 표시됩니다. |

     {style="table-layout:auto"}

   - 테두리 스타일을 설정할 때 `None`테두리 표시 옵션을 완료합니다.

     ![테두리 색상](./assets/pb-settings-border-color.png){width="600" zoomable="yes"}

     | 옵션 | 설명 |
     | ------ |------------ |
     | [!UICONTROL Border Color] | 색상 견본을 선택하거나 색상 선택기를 클릭하거나 유효한 색상 이름 또는 이에 해당하는 16진수 값을 입력하여 색상을 지정합니다. |
     | [!UICONTROL Border Width] | 테두리 라인 너비의 픽셀 수를 입력합니다. |
     | [!UICONTROL Border Radius] | 테두리의 각 모퉁이를 둥글게 만드는 데 사용되는 반경의 크기를 정의하려면 픽셀 수를 입력합니다. |

     {style="table-layout:auto"}

   - (선택 사항) 다음 이름을 지정합니다 **[!UICONTROL CSS classes]** 맵 컨테이너에 적용할 현재 스타일 시트에서 가져옵니다.

     여러 클래스 이름은 공백으로 구분합니다.

   - 다음에 대한 값을 픽셀 단위로 입력하십시오. **[!UICONTROL Margins and Padding]** 를 클릭하여 맵 컨테이너의 외부 여백 및 내부 패딩을 지정합니다.

     맵 컨테이너 다이어그램에 해당하는 각 값을 입력합니다.

     | 컨테이너 영역 | 설명 |
     | -------------- | ----------- |
     | [!UICONTROL Margins] | 컨테이너의 모든 면 바깥쪽 가장자리에 적용되는 빈 공간의 양입니다. |
     | [!UICONTROL Padding] | 컨테이너의 모든 측면 안쪽 가장자리에 적용되는 빈 공간의 양입니다. |

     {style="table-layout:auto"}

     >[!NOTE]
     >
     >맵 콘텐츠 유형에는 패딩을 사용할 수 없습니다.

1. 완료되면 다음을 클릭하십시오. **[!UICONTROL Save]** 설정을 적용하고 로 돌아가려면 [!DNL Page Builder] 작업 영역.

### 격자 크기 변경

그리드 크기는 와 관련된 맵의 크기를 결정합니다. [열](column.md) 다음에 있음 [!DNL Page Builder] 스테이지. 기본적으로 맵은 너비가 12열이며 최대 16열입니다.

1. 다음에서 _관리자_ 사이드바, 이동 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. 아래의 왼쪽 패널에서 _[!UICONTROL General]_, 선택&#x200B;**[!UICONTROL Content Management]**.

1. 확장 ![확장 선택기](../assets/icon-display-expand.png) **[!UICONTROL Advanced Content Tools]**.

1. 필요에 따라 격자선 옵션을 업데이트합니다.

   >[!NOTE]
   >
   >필요한 경우 **[!UICONTROL Use system value]** 확인란을 선택하여 이 설정을 수정합니다.

   - 대상 **[!UICONTROL Default Column Grid Size]**&#x200B;그리드의 기본 크기에 대한 새 값을 입력합니다.

   - 대상 **[!UICONTROL Maximum Column Grid Size]**&#x200B;기본 최대 격자 크기에 대한 새 값을 입력합니다.

   ![열 격자 크기 설정](./assets/pb-configure-advanced-content-tools-grid-size.png){width="600" zoomable="yes"}

1. 완료되면 다음을 클릭하십시오. **[!UICONTROL Save Config]**.

[1]: https://cloud.google.com/maps-platform/
[2]: https://cloud.google.com/maps-platform/places/
[3]: https://cloud.google.com/maps-platform/user-guide/
[4]: https://developers.google.com/maps/documentation/javascript/get-api-key
[5]: https://www.google.com/maps
[6]: https://mapstyle.withgoogle.com/
