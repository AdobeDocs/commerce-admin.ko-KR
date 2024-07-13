---
title: 소셜 미디어 및 RSS 피드
description: 소셜 미디어 및 기타 RSS 피드 통합을 추가하여 브랜드 및 제품 인지도를 구축하는 방법에 대해 알아봅니다.
exl-id: e4a48870-f53e-4848-8faa-8f2aedaf53b7
feature: Merchandising, Communications
source-git-commit: 61df9a4bcfaf09491ae2d353478ceb281082fa74
workflow-type: tm+mt
source-wordcount: '1162'
ht-degree: 0%

---

# 소셜 미디어 및 RSS 피드

많은 상인들이 브랜드와 제품 인지도를 구축하기 위해 소셜 미디어와 기타 디지털 도구를 사용한다. Marketplace 확장을 설치하거나 콘텐츠 페이지에 플러그인을 추가하여 스토어를 소셜 네트워크와 통합할 수 있습니다. RSS 피드를 사용하여 제품 정보를 쇼핑 집계 사이트에 게시하고 뉴스레터에 포함할 수도 있습니다. 고객은 RSS 피드에 가입하여 새로운 제품 및 프로모션에 대해 알아볼 수 있습니다.

## 소셜 네트워크

[Marketplace 확장](../getting-started/commerce-marketplace.md)을 설치하여 스토어를 소셜 네트워크에 연결할 수 있습니다. 또한 스토어 전체에서 페이지에 통합할 수 있는 CMS 블록에 _좋아요_ 단추와 같은 소셜 플러그인을 쉽게 추가할 수 있습니다.

소셜 네트워킹 사이트에는 스토어에 쉽게 추가할 수 있는 다양한 플러그인이 있습니다. 또한 Commerce Marketplace에는 스토어를 소셜 미디어와 통합하는 데 사용할 수 있는 많은 확장이 있습니다. 다음 예제에서는 스토어에 Facebook _Like_ 단추를 추가하는 방법을 보여 줍니다.

>[!NOTE]
>
>Adobe Commerce에서 기본 _Magento 소셜_ Facebook 통합을 제거했으며 더 이상 확장을 지원하지 않습니다. [Commerce Marketplace](https://marketplace.magento.com/catalogsearch/result/?q=Facebook){:target=&quot;_blank&quot;}(으)로 이동하여 Facebook 통합을 위한 대체 확장을 찾습니다.

### 1단계. 단추 코드 가져오기

1. 메타 개발자 웹 사이트에서 [단추 설정](https://developers.facebook.com/docs/plugins/like-button) 페이지로 이동합니다.

1. **[!UICONTROL URL to Like]**&#x200B;의 경우 스토어에서 _좋아요_&#x200B;를 설정할 페이지의 URL을 입력하세요.

   예를 들어 스토어 홈 페이지의 URL을 입력할 수 있습니다.

1. 단추의 **[!UICONTROL Layout]**&#x200B;을(를) 선택합니다.

1. 사이트에서 사용할 수 있는 단추 및 관련 텍스트 메시지에 사용할 수 있는 **[!UICONTROL Width]**&#x200B;을(를) 픽셀 단위로 입력하십시오.

1. **[!UICONTROL Action Type]**&#x200B;을(를) 다음 중 하나로 설정합니다.

   - `Like`
   - `Recommend`

1. 생성된 코드를 클립보드에 복사하려면 **[!UICONTROL Get Code]**&#x200B;을(를) 클릭합니다.

### 2단계. 콘텐츠 블록 만들기

1. 스토어 관리자로 돌아갑니다.

1. _관리자_ 사이드바에서 **[!UICONTROL Content]** > _[!UICONTROL Elements]_>**[!UICONTROL Blocks]**(으)로 이동합니다.

1. 오른쪽 상단에서 **[!UICONTROL Add New Block]**&#x200B;을(를) 클릭합니다.

1. 내부 참조에 대한 설명 **[!UICONTROL Block Title]**&#x200B;을(를) 입력하십시오.

   예: `Facebook Like Button`.

1. 모든 소문자와 공백 대신 밑줄을 사용하여 고유 **[!UICONTROL Identifier]**&#x200B;을(를) 블록에 지정하십시오.

   예: `facebook_like_button`.

1. Commerce 인스턴스에 여러 스토어 보기가 있는 경우 블록을 사용할 각 **[!UICONTROL Store View]**&#x200B;을(를) 선택하십시오.

1. 콘텐츠 도구에 따라 코드 조각을 블록 콘텐츠에 추가합니다.

   - [!DNL Page Builder]을(를) 사용하는 경우 스테이지에 [HTML 코드](../page-builder/html-code.md) 블록을 추가하고 Facebook 사이트에서 복사한 코드 조각을 붙여 넣으십시오. 그렇지 않으면 코드 조각을 **[!UICONTROL Content]** 상자에 붙여 넣으십시오.

   - 편집기를 사용하여 Facebook 사이트에서 복사한 코드 조각을 **[!UICONTROL Content]** 상자에 붙여 넣습니다.

1. 블록을 실행할 준비가 되지 않은 경우 **[!UICONTROL Enable Block]**&#x200B;을(를) `No`(으)로 설정하십시오.

1. 완료되면 **[!UICONTROL Save Block]**&#x200B;을(를) 클릭합니다.

### 3단계. 블록을 배치합니다

1. 콘텐츠 도구에 따라 블록을 추가합니다.

   - [!UICONTROL Page Builder]을(를) 사용하는 경우 지침에 따라 [블록을 단계에 추가](../page-builder/block.md)하십시오.

   - _관리자_ 사이드바에서 **[!UICONTROL Content]** > _[!UICONTROL Elements]_>**[!UICONTROL Widgets]**(으)로 이동합니다.

1. 오른쪽 상단 모서리에서 **[!UICONTROL Add Widget]**&#x200B;을(를) 클릭하고 다음을 수행합니다.

   - ![Adobe Commerce B2B](../assets/b2b.svg)(Adobe Commerce B2B에서만 사용 가능) _설정_ 섹션에서 **[!UICONTROL Type]**&#x200B;을(를) `CMS Static Block`(으)로 설정하고 **[!UICONTROL Continue]**&#x200B;을(를) 클릭합니다.

   - **[!UICONTROL Design Theme]**&#x200B;이(가) 현재 테마로 설정되어 있는지 확인하십시오.

   - **[!UICONTROL Continue]**&#x200B;을(를) 클릭합니다.

1. **[!UICONTROL Storefront Properties]** 섹션에서 다음을 수행합니다.

   - **[!UICONTROL Widget Title]**&#x200B;의 경우 내부 참조에 대한 제목을 입력하십시오.

   - **[!UICONTROL Assign to Store Views]**&#x200B;을(를) `All Store Views` 또는 앱을 사용할 수 있는 보기로 설정하십시오. 여러 뷰를 선택하려면 Ctrl 키(PC) 또는 Command 키(Mac)를 누른 상태에서 각 옵션을 클릭합니다.

   - 블록의 순서를 다른 콘텐츠 요소와 같은 페이지 위치에 나타나도록 지정할 경우 블록 순서를 결정하려면 **[!UICONTROL Sort Order]** 필드에 숫자를 입력합니다. 위쪽 위치는 0입니다.

1. _[!UICONTROL Layout Updates]_섹션에서&#x200B;**[!UICONTROL Add Layout Update]**을(를) 클릭하고 블록을 표시할 범주, 제품 또는 페이지로&#x200B;**[!UICONTROL Display On]**을(를) 설정합니다.

   예를 들어 `All Pages`을(를) 선택하고 머리글이나 바닥글에 블록을 배치하면 저장소의 모든 페이지에서 동일한 위치에 블록이 나타납니다.

   특정 페이지에 블록을 배치하려면 다음 작업을 수행하십시오.

   - **[!UICONTROL Display On]**&#x200B;을(를) `Specified Page`(으)로 설정하고 블록을 표시할 **[!UICONTROL Page]**&#x200B;을(를) 선택하십시오.

   - 페이지에서 블록을 배치할 위치를 식별하려면 **[!UICONTROL Block Reference]**&#x200B;을(를) 선택하십시오.

   - `CMS Static Block Default Template`(으)로 설정된 **[!UICONTROL Template]**&#x200B;에 대한 기본 설정을 적용합니다.

   - **[!UICONTROL Save and Continue Edit]**&#x200B;을(를) 클릭합니다.

1. 왼쪽 패널에서 **[!UICONTROL Widget Options]**&#x200B;을(를) 선택합니다.

1. **[!UICONTROL Select Block…]**&#x200B;을(를) 클릭하고 배치할 블록을 선택합니다.

1. 완료되면 **[!UICONTROL Save]**&#x200B;을(를) 클릭합니다.

1. 메시지가 표시되면 작업 공간 상단에 있는 지침에 따라 인덱스와 페이지 캐시를 업데이트합니다.

   이제 위젯이 _[!UICONTROL Widgets]_목록에 나타납니다.

### 4단계. 스토어에서 위치 확인

스토어프론트로 돌아가서 블록이 올바른 위치에 있는지 확인하십시오. 블록을 이동하려면 위젯을 다시 열고 다른 페이지나 블록 참조를 시도할 수 있습니다.

## 피드

RSS(Really Simple Syndication)는 정보를 온라인으로 배포하는 데 사용되는 XML 기반 데이터 형식입니다. 고객은 RSS 피드를 구독하여 새로운 제품 및 프로모션에 대해 알아볼 수 있습니다. RSS 피드는 제품 정보를 쇼핑 집계 사이트에 게시하는 데 사용할 수도 있으며 뉴스레터에 포함될 수 있습니다.

RSS 피드가 활성화되면 제품, 특별 광고, 카테고리 및 쿠폰에 대한 추가 사항이 각 피드의 가입자에게 자동으로 전송됩니다. 게시하는 모든 RSS 피드에 대한 링크는 저장소의 바닥글에 있습니다.

![RSS 피드 아이콘](./assets/icon-rss.png){width="100"}<br/>

RSS 피드를 읽는 데 필요한 소프트웨어를 피드 리더라고 하며 사람들이 헤드라인, 블로그, 팟캐스트 등을 구독할 수 있도록 합니다. Google Reader은 온라인에서 무료로 사용할 수 있는 많은 피드 리더 중 하나입니다.

![Example storefront - RSS 피드](./assets/storefront-rss-feeds.png){width="700" zoomable="yes"}

### RSS 피드 설정의 이점

- 스토어 또는 블로그에서 최신 업데이트 다운로드
- 라이트 광고
- 보통주
- SEO 증폭
- 매출 증대

### RSS 피드 유형

| RSS 피드 | 설명 |
|--- |--- |
| [!UICONTROL Wish List] | 활성화되면 고객 위시리스트 페이지 상단에 RSS 피드 링크가 나타납니다. 또한 위시리스트 공유 페이지에는 공유 위시리스트의 피드에 대한 링크를 포함할 수 있는 확인란이 포함되어 있습니다. |
| [!UICONTROL New Products] | 카탈로그에 추가된 새 제품에 대한 알림을 게시합니다. |
| [!UICONTROL Special Products] | 특별 가격이 적용된 제품에 대한 알림을 게시합니다. |
| [!UICONTROL Coupons / Discounts] | 스토어에서 사용할 수 있는 특별한 쿠폰이나 할인에 대한 알림을 게시합니다. |
| [!UICONTROL Top Level Category] | 카탈로그의 최상위 수준 카테고리 구조에 대한 변경 사항을 게시하며 이는 기본 메뉴에 반영됩니다. |
| [!UICONTROL Customer Order Status] | 고객에게 RSS 피드로 주문 상태를 추적할 수 있는 기능을 제공합니다. 활성화되면 RSS 피드 링크가 주문에 나타납니다. |

{style="table-layout:auto"}

### 스토어에 대한 RSS 피드 설정

1. _관리자_ 사이드바에서 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**(으)로 이동합니다.

1. 오른쪽 상단 모서리에서 피드를 사용할 수 있는 보기로 **[!UICONTROL Store View]**&#x200B;을(를) 설정합니다.

   확인 메시지가 표시되면 **[!UICONTROL OK]**&#x200B;을(를) 클릭합니다.

1. 왼쪽 패널에서 **[!UICONTROL Catalog]**&#x200B;을(를) 확장하고 **[!UICONTROL RSS Feeds]**&#x200B;을(를) 선택합니다.

1. **[!UICONTROL Rss Config]** 섹션에서 ![확장 선택기](../assets/icon-display-expand.png)을(를) 확장하고 **[!UICONTROL Enable RSS]**&#x200B;을(를) `Enable`(으)로 설정합니다.

   ![카탈로그 구성 - RSS 피드](../configuration-reference/catalog/assets/rss-feeds-rss-config.png){width="600" zoomable="yes"}

   필요한 경우 **[!UICONTROL Use Default]** 확인란의 선택을 취소하여 기본값을 변경합니다.

1. **[!UICONTROL Wish List]** 섹션에서 ![확장 선택기](../assets/icon-display-expand.png)을(를) 확장하고 **[!UICONTROL Enable RSS]**&#x200B;을(를) `Enable`(으)로 설정합니다.

1. **[!UICONTROL Catalog]** 섹션에서 ![확장 선택기](../assets/icon-display-expand.png)를 확장하고 필요에 따라 다른 피드를 `Enable`(으)로 설정합니다.

   - **[!UICONTROL New Products]**
   - **[!UICONTROL Special Products]**
   - **[!UICONTROL Coupons/Discounts]**
   - **[!UICONTROL Top Level Category]**

   ![카탈로그 - RSS 피드 설정](../configuration-reference/catalog/assets/rss-feeds-catalog.png){width="600" zoomable="yes"}

1. **[!UICONTROL Order]** 섹션에서 ![확장 선택기](../assets/icon-display-expand.png)을(를) 확장하고 **[!UICONTROL Customer Order Status Notification]**&#x200B;을(를) `Enable`(으)로 설정합니다.

1. 완료되면 **[!UICONTROL Save Config]**&#x200B;을(를) 클릭합니다.

1. 페이지 URL 끝에 `/rss`이(가) 있는 상점 첫 화면의 결과를 확인합니다.

