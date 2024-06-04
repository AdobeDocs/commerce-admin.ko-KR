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

스토어를 소셜 네트워크에 연결하려면 [마켓플레이스 확장](../getting-started/commerce-marketplace.md). 또한 다음과 같은 소셜 플러그인을 쉽게 추가할 수 있습니다. _좋아요_ 버튼을 클릭하여 스토어 전체에서 페이지에 통합할 수 있는 CMS 블록으로 설정합니다.

소셜 네트워킹 사이트에는 스토어에 쉽게 추가할 수 있는 다양한 플러그인이 있습니다. 또한 Commerce Marketplace에는 스토어를 소셜 미디어와 통합하는 데 사용할 수 있는 많은 확장이 있습니다. 다음 예에서는 Facebook을 추가하는 방법을 보여 줍니다 _좋아요_ 스토어에 대한 단추입니다.

>[!NOTE]
>
>Adobe Commerce에서 기본 을 제거했습니다. _소셜 Magento_ Facebook 통합 및 는 더 이상 확장을 지원하지 않습니다. 로 이동 [Commerce Marketplace](https://marketplace.magento.com/catalogsearch/result/?q=Facebook)facebook 통합을 위한 대체 확장을 찾으려면 {:target=&quot;_blank&quot;}를 클릭하십시오.

### 1단계. 단추 코드 가져오기

1. 메타 개발자 웹 사이트에서 [단추 설정](https://developers.facebook.com/docs/plugins/like-button) 페이지를 가리키도록 업데이트하는 중입니다.

1. 대상 **[!UICONTROL URL to Like]**, 스토어에 있는 사람들이 원하는 페이지의 URL을 입력합니다 _좋아요_.

   예를 들어 스토어 홈 페이지의 URL을 입력할 수 있습니다.

1. 다음을 선택합니다. **[!UICONTROL Layout]** 단추에 사용됩니다.

1. 다음을 입력합니다. **[!UICONTROL Width]** 버튼 및 관련 텍스트 메시지에 대해 사이트에서 사용할 수 있는 픽셀 단위.

1. 설정 **[!UICONTROL Action Type]** 다음 중 하나를 수행합니다.

   - `Like`
   - `Recommend`

1. 클릭 **[!UICONTROL Get Code]** 생성된 코드를 클립보드에 복사합니다.

### 2단계. 콘텐츠 블록 만들기

1. 스토어 관리자로 돌아갑니다.

1. 다음에서 _관리자_ 사이드바, 이동 **[!UICONTROL Content]** > _[!UICONTROL Elements]_>**[!UICONTROL Blocks]**.

1. 오른쪽 위 모서리에서 을(를) 클릭합니다. **[!UICONTROL Add New Block]**.

1. 설명을 입력하십시오. **[!UICONTROL Block Title]** 내부 참조용.

   예: `Facebook Like Button`.

1. 고유 할당 **[!UICONTROL Identifier]** 모두 소문자를 사용하고 공백 대신 밑줄을 사용하여 블록을 전달합니다.

   예: `facebook_like_button`.

1. Commerce 인스턴스에 여러 스토어 보기가 있는 경우 각각 을 선택합니다 **[!UICONTROL Store View]** 블록을 사용할 수 있는 위치입니다.

1. 콘텐츠 도구에 따라 코드 조각을 블록 콘텐츠에 추가합니다.

   - 사용 시 [!DNL Page Builder], 추가 [HTML 코드](../page-builder/html-code.md) 스테이지로 블록하고 Facebook 사이트에서 복사한 코드 조각을 붙여넣습니다. 그렇지 않으면 코드 조각을 **[!UICONTROL Content]** 상자.

   - 편집기를 사용하여 Facebook 사이트에서 복사한 코드 조각을 **[!UICONTROL Content]** 상자.

1. 블록을 실행할 준비가 되지 않은 경우 을(를) 설정합니다. **[!UICONTROL Enable Block]** 끝 `No`.

1. 완료되면 다음을 클릭하십시오. **[!UICONTROL Save Block]**.

### 3단계. 블록을 배치합니다

1. 콘텐츠 도구에 따라 블록을 추가합니다.

   - 사용 시 [!UICONTROL Page Builder], 다음 지침을 따르십시오. [블록 추가](../page-builder/block.md) 무대로

   - 다음에서 _관리자_ 사이드바, 이동 **[!UICONTROL Content]** > _[!UICONTROL Elements]_>**[!UICONTROL Widgets]**.

1. 오른쪽 위 모서리에서 을(를) 클릭합니다. **[!UICONTROL Add Widget]** 다음을 수행합니다.

   - ![Adobe Commerce](../assets/b2b.svg) (Adobe Commerce B2B에서만 사용 가능)에서 _설정_ 섹션, 설정 **[!UICONTROL Type]** 끝 `CMS Static Block` 및 클릭 **[!UICONTROL Continue]**.

   - 다음을 확인합니다. **[!UICONTROL Design Theme]** 이 현재 테마로 설정되어 있습니다.

   - 클릭 **[!UICONTROL Continue]**.

1. 다음에서 **[!UICONTROL Storefront Properties]** 섹션에서 다음을 수행합니다.

   - 대상 **[!UICONTROL Widget Title]**&#x200B;내부 참조에 대한 제목을 입력합니다.

   - 설정 **[!UICONTROL Assign to Store Views]** 끝 `All Store Views`또는 앱을 사용할 수 있게 하려는 뷰로 이동합니다. 여러 뷰를 선택하려면 Ctrl 키(PC) 또는 Command 키(Mac)를 누른 상태에서 각 옵션을 클릭합니다.

   - 에 숫자를 입력합니다. **[!UICONTROL Sort Order]** 블록의 순서를 결정하는 필드입니다. 지정된 블록의 순서는 다른 콘텐츠 요소와 페이지의 동일한 위치에 나타납니다. 위쪽 위치는 0입니다.

1. 다음에서 _[!UICONTROL Layout Updates]_섹션, 클릭&#x200B;**[!UICONTROL Add Layout Update]**및 설정&#x200B;**[!UICONTROL Display On]**블록을 표시할 카테고리, 제품 또는 페이지로 이동합니다.

   예를 들어 `All Pages` 블록을 머리글이나 바닥글에 놓으면 스토어의 모든 페이지에서 동일한 위치에 블록이 표시됩니다.

   특정 페이지에 블록을 배치하려면 다음 작업을 수행하십시오.

   - 설정 **[!UICONTROL Display On]** 끝 `Specified Page` 및 선택 **[!UICONTROL Page]** 블록을 표시할 위치입니다.

   - 다음을 선택합니다. **[!UICONTROL Block Reference]** 페이지에서 블록을 배치할 위치를 식별합니다.

   - 의 기본 설정 적용 **[!UICONTROL Template]**, 로 설정되어 있습니다. `CMS Static Block Default Template`.

   - 클릭 **[!UICONTROL Save and Continue Edit]**.

1. 왼쪽의 패널에서 을 선택합니다 **[!UICONTROL Widget Options]**.

1. 클릭 **[!UICONTROL Select Block…]** 배치할 블록을 선택합니다.

1. 완료되면 다음을 클릭하십시오. **[!UICONTROL Save]**.

1. 메시지가 표시되면 작업 공간 상단에 있는 지침에 따라 인덱스와 페이지 캐시를 업데이트합니다.

   이제 위젯이에 나타납니다. _[!UICONTROL Widgets]_목록을 표시합니다.

### 4단계. 스토어에서 위치 확인

스토어프론트로 돌아가서 블록이 올바른 위치에 있는지 확인하십시오. 블록을 이동하려면 위젯을 다시 열고 다른 페이지나 블록 참조를 시도할 수 있습니다.

## 피드

RSS(Really Simple Syndication)는 정보를 온라인으로 배포하는 데 사용되는 XML 기반 데이터 형식입니다. 고객은 RSS 피드를 구독하여 새로운 제품 및 프로모션에 대해 알아볼 수 있습니다. RSS 피드는 제품 정보를 쇼핑 집계 사이트에 게시하는 데 사용할 수도 있으며 뉴스레터에 포함될 수 있습니다.

RSS 피드가 활성화되면 제품, 특별 광고, 카테고리 및 쿠폰에 대한 추가 사항이 각 피드의 가입자에게 자동으로 전송됩니다. 게시하는 모든 RSS 피드에 대한 링크는 저장소의 바닥글에 있습니다.

![RSS 피드 아이콘](./assets/icon-rss.png){width="100"}<br/>

RSS 피드를 읽는 데 필요한 소프트웨어를 피드 리더라고 하며 사람들이 헤드라인, 블로그, 팟캐스트 등을 구독할 수 있도록 합니다. Google Reader은 온라인에서 무료로 사용할 수 있는 많은 피드 리더 중 하나입니다.

![예 storefront - RSS 피드](./assets/storefront-rss-feeds.png){width="700" zoomable="yes"}

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

1. 다음에서 _관리자_ 사이드바, 이동 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. 오른쪽 상단에서 를 설정합니다. **[!UICONTROL Store View]** 피드를 사용할 수 있는 뷰로 이동합니다.

   확인 메시지가 표시되면 다음을 클릭합니다. **[!UICONTROL OK]**.

1. 왼쪽 패널에서 를 확장합니다. **[!UICONTROL Catalog]** 및 선택 **[!UICONTROL RSS Feeds]**.

1. 확장 ![확장 선택기](../assets/icon-display-expand.png) 다음 **[!UICONTROL Rss Config]** 섹션 및 세트 **[!UICONTROL Enable RSS]** 끝 `Enable`.

   ![카탈로그 구성 - RSS 피드](../configuration-reference/catalog/assets/rss-feeds-rss-config.png){width="600" zoomable="yes"}

   필요한 경우 **[!UICONTROL Use Default]** 확인란을 선택하여 기본값을 변경합니다.

1. 확장 ![확장 선택기](../assets/icon-display-expand.png) 다음 **[!UICONTROL Wish List]** 섹션 및 세트 **[!UICONTROL Enable RSS]** 끝 `Enable`.

1. 확장 ![확장 선택기](../assets/icon-display-expand.png) 다음 **[!UICONTROL Catalog]** 섹션 및 기타 피드 설정 `Enable` 필요한 경우.

   - **[!UICONTROL New Products]**
   - **[!UICONTROL Special Products]**
   - **[!UICONTROL Coupons/Discounts]**
   - **[!UICONTROL Top Level Category]**

   ![카탈로그 - RSS 피드 설정](../configuration-reference/catalog/assets/rss-feeds-catalog.png){width="600" zoomable="yes"}

1. 확장 ![확장 선택기](../assets/icon-display-expand.png) 다음 **[!UICONTROL Order]** 섹션 및 세트 **[!UICONTROL Customer Order Status Notification]** 끝 `Enable`.

1. 완료되면 다음을 클릭하십시오. **[!UICONTROL Save Config]**.

1. 다음을 사용하여 상점 첫 화면에서 결과 확인 `/rss` (페이지 URL의 끝)

