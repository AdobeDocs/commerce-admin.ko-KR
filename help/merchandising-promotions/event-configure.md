---
title: 이벤트 구성
description: 스토어프론트 사이드바에서 이벤트를 활성화하고 이벤트 블록을 설정하는 기본 구성을 완료하는 방법을 알아봅니다.
exl-id: 620b2d60-ce6f-4f31-93bb-18d3dd9cdce6
feature: Marketing Tools, Promotions/Events
source-git-commit: 084d2c3381f57a8a4c7e8ffde9da1abd4d8af670
workflow-type: tm+mt
source-wordcount: '467'
ht-degree: 0%

---

# 이벤트 구성

{{ee-feature}}

이벤트를 만들려면 먼저 기본 구성을 완료하여 이벤트를 활성화하고 사이드바에서 이벤트 블록을 설정해야 합니다.

## 이벤트 활성화 및 구성

1. 다음에서 _관리자_ 사이드바, 이동 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. 왼쪽 패널에서 를 확장합니다. **[!UICONTROL Catalog]** 및 선택 **[!UICONTROL Catalog]** 밑에.

1. 확장 ![확장 선택기](../assets/icon-display-expand.png) 다음 **[!UICONTROL Catalog Events]** 섹션을 참조하고 다음을 수행합니다.

   ![카탈로그 구성 - 카탈로그 이벤트](../configuration-reference/catalog/assets/catalog-events.png){width="600" zoomable="yes"}

   - 설정 **[!UICONTROL Enable Catalog Events Functionality]** 끝 `Yes`.

   - 설정 **[!UICONTROL Enable Catalog Event Widget on Storefront]** 끝 `Yes`.

   - 다음을 입력합니다. **[!UICONTROL Number of Events to be Displayed in the Event Slider Sidebar Widget]**. 기본적으로 이 값은 로 설정됩니다. `5`. 슬라이더에서 한 번에 하나의 이벤트만 표시하려면 을 입력합니다 `1`.

   - 다음 수를 입력합니다. **[!UICONTROL Events to Scroll per Click in Event Slider Sidebar Widget]**. 기본적으로 이 값은 로 설정됩니다. `2`. 슬라이더를 클릭할 때 다음 이벤트를 순서대로 표시하려면 을 입력합니다 `1`.

1. 완료되면 다음을 클릭하십시오. **[!UICONTROL Save Config]**.

## 액세스 제한 사항

프라이빗 세일, 이벤트 또는 사이트 접속은 로그인하는 등록 고객으로 제한하거나, 접속하기 전에 등록해야 하는 비등록 고객으로 확장할 수 있다.

![일반 구성 - 웹 사이트 제한 사항](../configuration-reference/general/assets/general-website-restrictions.png){width="600" zoomable="yes"}

### 액세스 제한

프라이빗 세일, 이벤트 또는 사이트 접속은 로그인하는 등록 고객으로 제한하거나, 접속하기 전에 등록해야 하는 비등록 고객으로 확장할 수 있다.

![일반 구성 - 웹 사이트 제한 사항](../configuration-reference/general/assets/general-website-restrictions.png){width="600" zoomable="yes"}

1. 다음에서 _관리자_ 사이드바, 이동 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. 왼쪽 패널에서 를 확장합니다. **[!UICONTROL General]** 및 선택 **[!UICONTROL General]** 밑에.

1. 확장 ![확장 선택기](../assets/icon-display-expand.png) 다음 **[!UICONTROL Website Restrictions]** 섹션.

1. 설정 **[!UICONTROL Access Restriction]** 끝 `Yes`.

1. 설정 **[!UICONTROL Restriction Mode]** 다음 중 하나를 수행합니다.

   - `Website Closed`
   - `Private Sales: Login Only`
   - `Private Sales: Login and Register`

1. 설정 **[!UICONTROL Startup Page]** 다음 중 하나를 수행합니다.

   - `To login form (302 Found)` - 사용자는 사이트에 액세스하기 전에 로그인 양식으로 리디렉션됩니다.

   - `To landing page (302 Found)` - 사용자가 로그인할 때까지 지정된 랜딩 페이지로 리디렉션됩니다.

     >[!IMPORTANT]
     >
     >고객이 사이트에 액세스하기 위해 로그인할 수 있도록 랜딩 페이지의 로그인 페이지에 대한 링크를 포함해야 합니다.

1. 다음을 선택합니다. **[!UICONTROL Landing Page]** 고객이 프라이빗 세일 사이트에 로그인하기 전에 표시됩니다.

1. 검색 엔진 봇과 스파이더가 랜딩 페이지가 올바르고 사이트에 색인화할 다른 페이지가 없음을 알 수 있도록 하려면 을 설정합니다. **[!UICONTROL HTTP Response]** 끝 `200 OK`.

   로 설정된 다른 모든 경우 `503 Service Unavailable`.

   >[!NOTE]
   >
   >제한 모드가 로 설정된 경우에만 적용 가능 _웹 사이트 닫힘_. 랜딩 페이지는 원시 HTML으로 렌더링됩니다.

1. 고객 로그인 및 암호 찾기 양식의 필드를 이전 항목에서 자동으로 채우려면 을(를) 설정합니다. **[!UICONTROL Enable Autocomplete on login/forgot password forms]** 끝 `Yes`.

1. 완료되면 다음을 클릭하십시오. **[!UICONTROL Save Config]**.

### 판매 제한

기본적으로 예정된 이벤트나 마감된 이벤트에 나타나는 제품은 일반 판매와 _[!UICONTROL Add to Cart]_제품 목록 또는 제품 페이지에 단추가 표시되지 않습니다.

복원하려면 _[!UICONTROL Add to Cart]_닫힘 이벤트에 대한 단추이므로 이벤트를 삭제해야 합니다(참조). [이벤트 업데이트](event-create.md#update-events)). 그러나 제품이 판매 제한이 없는 다른 카테고리와 연결된 경우 해당 버튼을 제품 페이지에서 사용할 수 있습니다. 마찬가지로 판매 제한이 없는 다른 카테고리와 제품이 연결된 경우 티커 블록이 제품 페이지에 표시되지 않습니다.
