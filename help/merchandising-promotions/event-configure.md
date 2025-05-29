---
title: 이벤트 구성
description: 스토어프론트 사이드바에서 이벤트를 활성화하고 이벤트 블록을 설정하는 기본 구성을 완료하는 방법을 알아봅니다.
exl-id: 620b2d60-ce6f-4f31-93bb-18d3dd9cdce6
feature: Marketing Tools, Promotions/Events
badgePaas: label="PaaS만" type="Informative" url="https://experienceleague.adobe.com/ko/docs/commerce/user-guides/product-solutions" tooltip="Adobe Commerce 온 클라우드 프로젝트(Adobe 관리 PaaS 인프라) 및 온프레미스 프로젝트에만 적용됩니다."
source-git-commit: 7e28081ef2723d4113b957edede6a8e13612ad2f
workflow-type: tm+mt
source-wordcount: '484'
ht-degree: 0%

---

# 이벤트 구성

{{ee-feature}}

이벤트를 만들려면 먼저 기본 구성을 완료하여 이벤트를 활성화하고 사이드바에서 이벤트 블록을 설정해야 합니다.

## 이벤트 활성화 및 구성

1. _관리자_ 사이드바에서 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**(으)로 이동합니다.

1. 왼쪽 패널에서 **[!UICONTROL Catalog]**&#x200B;을(를) 확장하고 아래의 **[!UICONTROL Catalog]**&#x200B;을(를) 선택합니다.

1. **[!UICONTROL Catalog Events]** 섹션에서 ![확장 선택기](../assets/icon-display-expand.png)를 확장하고 다음을 수행합니다.

   ![카탈로그 구성 - 카탈로그 이벤트](../configuration-reference/catalog/assets/catalog-events.png){width="600" zoomable="yes"}

   - **[!UICONTROL Enable Catalog Events Functionality]**&#x200B;을(를) `Yes`(으)로 설정합니다.

   - **[!UICONTROL Enable Catalog Event Widget on Storefront]**&#x200B;을(를) `Yes`(으)로 설정합니다.

   - **[!UICONTROL Number of Events to be Displayed in the Event Slider Sidebar Widget]** 입력. 기본적으로 이 값은 `5`(으)로 설정됩니다. 슬라이더에서 한 번에 하나의 이벤트만 표시하려면 `1`을(를) 입력하십시오.

   - **[!UICONTROL Events to Scroll per Click in Event Slider Sidebar Widget]**&#x200B;의 수를 입력하십시오. 기본적으로 이 값은 `2`(으)로 설정됩니다. 슬라이더를 클릭할 때 다음 이벤트를 순서대로 표시하려면 `1`을(를) 입력합니다.

1. 완료되면 **[!UICONTROL Save Config]**&#x200B;을(를) 클릭합니다.

## 액세스 제한 사항

프라이빗 세일, 이벤트 또는 사이트 접속은 로그인하는 등록 고객으로 제한하거나, 접속하기 전에 등록해야 하는 비등록 고객으로 확장할 수 있다.

![일반 구성 - 웹 사이트 제한](../configuration-reference/general/assets/general-website-restrictions.png){width="600" zoomable="yes"}

### 액세스 제한

프라이빗 세일, 이벤트 또는 사이트 접속은 로그인하는 등록 고객으로 제한하거나, 접속하기 전에 등록해야 하는 비등록 고객으로 확장할 수 있다.

![일반 구성 - 웹 사이트 제한](../configuration-reference/general/assets/general-website-restrictions.png){width="600" zoomable="yes"}

1. _관리자_ 사이드바에서 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**(으)로 이동합니다.

1. 왼쪽 패널에서 **[!UICONTROL General]**&#x200B;을(를) 확장하고 아래의 **[!UICONTROL General]**&#x200B;을(를) 선택합니다.

1. **[!UICONTROL Website Restrictions]** 섹션에서 ![확장 선택기](../assets/icon-display-expand.png)를 확장합니다.

1. **[!UICONTROL Access Restriction]**&#x200B;을(를) `Yes`(으)로 설정합니다.

1. **[!UICONTROL Restriction Mode]**&#x200B;을(를) 다음 중 하나로 설정합니다.

   - `Website Closed`
   - `Private Sales: Login Only`
   - `Private Sales: Login and Register`

1. **[!UICONTROL Startup Page]**&#x200B;을(를) 다음 중 하나로 설정합니다.

   - `To login form (302 Found)` - 사용자가 사이트에 액세스하기 전에 로그인 양식으로 리디렉션됩니다.

   - `To landing page (302 Found)` - 사용자가 로그인할 때까지 지정된 랜딩 페이지로 리디렉션됩니다.

     >[!IMPORTANT]
     >
     >고객이 사이트에 액세스하기 위해 로그인할 수 있도록 랜딩 페이지의 로그인 페이지에 대한 링크를 포함해야 합니다.

1. 고객이 비공개 판매 사이트에 로그인하기 전에 표시되는 **[!UICONTROL Landing Page]**&#x200B;을(를) 선택합니다.

1. 검색 엔진 봇과 스파이더가 랜딩 페이지가 올바르고 사이트에 인덱싱할 다른 페이지가 없음을 알 수 있도록 하려면 **[!UICONTROL HTTP Response]**&#x200B;을(를) `200 OK`(으)로 설정합니다.

   다른 모든 경우에는 `503 Service Unavailable`(으)로 설정됩니다.

   >[!NOTE]
   >
   >제한 모드가 _웹 사이트 닫힘_(으)로 설정된 경우에만 적용됩니다. 랜딩 페이지는 원시 HTML으로 렌더링됩니다.

1. 고객 로그인 및 암호 찾기 양식의 필드를 이전 항목에서 자동으로 채우려면 **[!UICONTROL Enable Autocomplete on login/forgot password forms]**&#x200B;을(를) `Yes`(으)로 설정하십시오.

1. 완료되면 **[!UICONTROL Save Config]**&#x200B;을(를) 클릭합니다.

### 판매 제한

기본적으로 예정된 이벤트나 마감된 이벤트에 나타나는 제품은 일반 판매에 사용할 수 없으며 _[!UICONTROL Add to Cart]_&#x200B;단추는 제품 목록이나 제품 페이지에 나타나지 않습니다.

닫힘 이벤트에 대한 _[!UICONTROL Add to Cart]_&#x200B;단추를 복원하려면 이벤트를 삭제해야 합니다([이벤트 업데이트](event-create.md#update-events) 참조). 그러나 제품이 판매 제한이 없는 다른 카테고리와 연결된 경우 해당 버튼을 제품 페이지에서 사용할 수 있습니다. 마찬가지로 판매 제한이 없는 다른 카테고리와 제품이 연결된 경우 티커 블록이 제품 페이지에 표시되지 않습니다.
