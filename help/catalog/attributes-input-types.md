---
title: 속성 입력 유형
description: 제품 특성에 사용할 수 있는 입력 유형에 대해 알아봅니다. 이 입력 유형은 입력할 수 있는 데이터 유형과 필드 또는 입력 컨트롤의 형식을 결정합니다.
exl-id: c35b3b9d-57b0-4c33-abdb-662ac6d0260e
feature: Catalog Management, Products
source-git-commit: 370131cd73a320b04ee92fa9609cb24ad4c07eca
workflow-type: tm+mt
source-wordcount: '637'
ht-degree: 0%

---

# 속성 입력 유형

관리자에서 볼 때 속성은 제품을 만들 때 작성하는 필드입니다. 속성에 지정된 입력 유형은 입력할 수 있는 데이터 유형과 필드 또는 입력 컨트롤의 형식을 결정합니다. 고객 관점에서 속성은 제품에 대한 정보를 제공하며, 제품을 구매하기 위해 작성해야 하는 옵션 및 데이터 입력 필드입니다.

## 입력 유형

| 속성 | 설명 |
|--- |--- |
| [!UICONTROL Text Field] | 텍스트를 위한 한 줄 입력 필드입니다. |
| [!UICONTROL Text Area] | 제품 설명과 같은 텍스트 단락을 입력하기 위한 여러 줄 입력 필드입니다. WYSIWYG 편집기를 사용하여 HTML 태그로 텍스트 서식을 지정하거나 텍스트에 태그를 직접 입력할 수 있습니다. |
| [!UICONTROL Text Editor] | 속성 위치에서 완전히 작동하는 텍스트 편집기입니다. |
| [!UICONTROL Date] | 에 날짜 값을 표시합니다. [기본 설정 형식](#date-and-time-options) 및 [시간대](../getting-started/store-details.md#locale-options). 날짜 값은 목록 또는 달력( ![달력 아이콘](../assets/icon-calendar.png) ). <br/><br/>**_참고:_**시스템 구성에 따라_관리자&#x200B;_사용자는 필드에 날짜를 직접 입력하거나 달력 또는 목록에서 날짜를 선택할 수 있습니다. 날짜 및 시간 값 지정에 대한 자세한 내용은 [날짜 및 시간 옵션](#date-and-time-options). |
| [!UICONTROL Date and Time] | 에 날짜 및 시간 값 표시 [기본 설정 형식](#date-and-time-options) 및 [시간대](../getting-started/store-details.md#locale-options). 날짜 및 시간은 수동으로 입력하거나 달력에서 선택할 수 있습니다. 예제 형식: MM/DD/YYYY HH:MM |
| [!UICONTROL Yes/No] | 의 사전 정의된 옵션이 있는 드롭다운 목록을 표시합니다. `Yes` 및 `No`. |
| 드롭다운 | 단일 선택 항목만 허용하는 값의 드롭다운 목록을 표시합니다. 드롭다운 입력 유형은 의 주요 구성 요소입니다. [구성 가능한 제품](../catalog/product-create-configurable.md). |
| [!UICONTROL Multiple Select] | 다중 선택을 허용하는 값의 드롭다운 목록을 표시합니다. |
| [!UICONTROL Price] | 이 입력 유형은 사전 정의된 속성에 추가되는 가격 필드를 생성하는 데 사용됩니다. `Price`, `Special Price`, `Tier Price`, 및 `Cost`. 사용되는 통화는 시스템 구성에 따라 결정됩니다. |
| [!UICONTROL Media Image] | 제품 로고, 관리 지침 또는 식품 라벨의 재료와 같은 추가 이미지를 제품과 연결합니다. 미디어 이미지 속성을 제품의 속성 세트에 추가하면 기본, 작은 이미지 및 썸네일과 함께 추가 이미지 유형이 됩니다. 미디어 이미지 속성을 다음에서 제외할 수 있습니다. [storefront 미디어 브라우저](catalog-images-video.md#storefront-media-browser). |
| [!UICONTROL Fixed Product Tax] | 다음을 정의할 수 있습니다. [FPT 비율](../stores-purchase/fixed-product-tax.md) 로케일의 요구 사항을 기반으로 합니다. |
| [!UICONTROL Visual Swatch] | 구성 가능한 제품의 색상, 질감 또는 패턴을 나타내는 견본을 표시합니다. A [시각적 견본](swatches.md) 16진수 색상 값으로 채울 수도 있고, 옵션의 색상, 재질, 텍스처 또는 패턴을 나타내는 업로드된 이미지를 표시할 수도 있습니다. |
| [!UICONTROL Text Swatch] | 크기에 자주 사용되는 구성 가능한 제품 옵션의 텍스트 기반 표현입니다. [텍스트 견본](swatches.md) 에는 16진수 색상 값도 포함될 수 있습니다. |
| [!UICONTROL Page Builder] | A [[!DNL Page Builder]](../page-builder/workspace.md) 제품 페이지에 매력적인 콘텐츠를 쉽게 추가할 수 있는 속성 위치의 작업 영역 |

{style="table-layout:auto"}

## 날짜 및 시간 옵션

날짜 및 시간 필드의 형식을 사용자 지정하고 데이터 입력에 사용할 입력 컨트롤을 선택할 수 있습니다. 날짜 값은 드롭다운 목록 또는 팝업 달력에서 선택할 수 있습니다.

![예 - 상점 팝업 달력](./assets/storefront-popup-calendar.png){width="700" zoomable="yes"}

**_날짜/시간 필드 서식 지정 방법:_**

1. 다음에서 _관리자_ 사이드바, 이동 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. 왼쪽의 패널에서 을 확장합니다. **[!UICONTROL Catalog]** 을(를) 클릭하고 **[!UICONTROL Catalog]** 하위 항목.

1. 확장 **[!UICONTROL Date & Time Custom Options]** 섹션.

   ![카탈로그 구성 - 날짜 및 시간 옵션](../configuration-reference/catalog/assets/catalog-date-time-custom-options.png){width="600" zoomable="yes"}

   이러한 옵션의 자세한 목록은 다음을 참조하십시오. [_날짜 및 시간 사용자 지정 옵션_](../configuration-reference/catalog/catalog.md) 다음에서 _구성 참조_.

1. 팝업 달력을 날짜 필드에 대한 입력 컨트롤로 사용하려면 다음을 설정합니다. **[!UICONTROL Use JavaScript Calendar]** 끝 `Yes`.

1. 을(를) 설정하려면 **[!UICONTROL Date Fields Order]**&#x200B;필요한 경우 날짜 필드의 각 부분 순서를 설정합니다.

   - 월
   - 일
   - 년

1. 선호하는 시간 형식을 설정하려면 다음을 설정하십시오. **시간 형식** 다음 중 하나를 수행합니다.

   - `12h AM/PM`
   - `24h`

1. 을(를) 설정하려면 **[!UICONTROL Year Range]** 드롭다운 값에 연도(YYYY)를 입력하여 **[!UICONTROL from]** 및 **[!UICONTROL to]** 날짜.

   비어 있는 경우 필드의 기본값은 현재 연도로 설정됩니다.

1. 완료되면 다음을 클릭하십시오. **[!UICONTROL Save Config]**.
