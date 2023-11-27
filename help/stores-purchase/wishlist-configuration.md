---
title: 위시리스트 구성
description: 스토어 고객을 위한 위시리스트 기능을 구성하는 방법에 대해 알아봅니다.
exl-id: 479455f1-282f-4277-b132-45c5867fb21c
feature: Customers, Configuration
source-git-commit: 8b5af316ab1d2e632ed5fc2066974326830ab3f7
workflow-type: tm+mt
source-wordcount: '533'
ht-degree: 0%

---

# 위시리스트 구성

위시리스트 구성은 위시리스트를 활성화하고 위시리스트를 공유할 때 사용되는 이메일 템플릿 및 이메일 메시지의 발신자를 결정합니다.

## 위시리스트 기능 활성화

1. 다음에서 _관리자_ 사이드바, 이동 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. 왼쪽 패널에서 를 확장합니다. **[!UICONTROL Customers]** 및 선택 **[!UICONTROL Wish List]**.

1. 확장 ![확장 선택기](../assets/icon-display-expand.png) 다음 **[!UICONTROL General Options]** 섹션을 참조하고 다음을 수행합니다.

   ![고객 구성 - 위시리스트 일반 설정](../configuration-reference/customers/assets/wishlist-general-options.png){width="600" zoomable="yes"}

   - 전환 **[!UICONTROL Enabled]** 끝 `Yes`- 저장소에 대한 위시 목록 모듈을 활성화합니다.

   - ![Adobe Commerce](../assets/adobe-logo.svg) (Adobe Commerce만 해당) 전환 **[!UICONTROL Enable Multiple Wish Lists]** 끝 `Yes`: 고객이 여러 위시 목록을 만들고 유지 관리할 수 있습니다.

   - ![Adobe Commerce](../assets/adobe-logo.svg) (Adobe Commerce만 해당) 고객이 계정과 연결할 수 있는 위시리스트 수를 제한하려면 값 입력 **[!UICONTROL Number of Multiple Wish Lists]**.

   - 전환 **[!UICONTROL Show in Sidebar]** 끝 `Yes`- 사이드바에 위시 목록을 표시합니다.

1. 확장 ![확장 선택기](../assets/icon-display-expand.png) 다음 **[!UICONTROL Share Options]** 섹션을 참조하고 다음을 수행합니다.

   ![고객 구성 - 위시리스트 공유 옵션](../configuration-reference/customers/assets/wishlist-share-options.png){width="600" zoomable="yes"}

   - 설정 **[!UICONTROL Email Sender]** 메시지를 보낸 사람으로 표시되어야 하는 저장소 연락처입니다. 옵션: 일반 담당자, 영업 담당자, 고객 지원, 사용자 정의 이메일.

   - 설정 **[!UICONTROL Email Template]** 고객이 위시리스트를 공유할 때 사용됩니다.

   - 고객이 보낼 수 있는 총 이메일 수를 제한하려면 **[!UICONTROL Max Emails Allowed to be Sent]** 값. 기본값은 10이며 최대 허용 수는 10,000입니다.

   - 메시지 크기를 제한하려면 다음 값을 입력합니다. **[!UICONTROL Email Text Length Limit]**. 기본값은 255입니다.

1. 확장 ![확장 선택기](../assets/icon-display-expand.png) 다음 **[!UICONTROL My Wish List Link]** 섹션 및 세트 **[!UICONTROL Display Wish List Summary]** 다음 중 하나를 수행합니다.

   - `Display number of items in wish list`
   - `Display item quantities`

   ![고객 구성 - 위시리스트 표시](../configuration-reference/customers/assets/wishlist-my-wishlist-link.png){width="600" zoomable="yes"}

1. 완료되면 다음을 클릭하십시오. **[!UICONTROL Save Config]**.

## 위시리스트 검색 추가

![Adobe Commerce](../assets/adobe-logo.svg) (Adobe Commerce 전용)

모든 공개 위시리스트는 위시리스트 검색을 사용하여 찾을 수 있습니다. [위젯](../content-design/widgets.md). 위젯을 통해 고객은 위시리스트 소유자의 이름이나 이메일 주소로 검색할 수 있습니다. 스토어 고객은 다른 고객에 속한 위시리스트를 찾거나, 이를 보고 제품을 주문하거나, 제품을 자신의 위시리스트에 추가할 수 있습니다. 다른 고객이 공개 위시리스트에서 구매한 항목은 원래 위시리스트에서 제거되지 않습니다. 다음 _위시리스트 검색_ 위젯을 스토어의 모든 페이지에 추가하여 고객이 친구 및 가족 구성원의 위시리스트를 쉽게 찾을 수 있도록 할 수 있습니다.

![Storefront - 위시리스트 검색 예](./assets/storefront-wishlist-search.png){width="700" zoomable="yes"}

1. 다음에서 _관리자_ 사이드바, 이동 **[!UICONTROL Content]** > _[!UICONTROL Elements]_>**[!UICONTROL Widgets]**.

1. 오른쪽 위 모서리에서 을(를) 클릭합니다. **[!UICONTROL Add Widget]**.

1. 다음에서 _[!UICONTROL Settings]_탭에서 다음을 수행합니다.

   - 설정 **[!UICONTROL Type]** 끝 `Wish List Search`.

   - 설정 **[!UICONTROL Design Theme]** 위시리스트가 추가되는 매장의 테마에 매핑합니다.

   - 클릭 **[!UICONTROL Continue]**.

1. 다음을 완료합니다. _[!UICONTROL Storefront Properties]_:

   - 다음을 입력합니다. **[!UICONTROL Widget Title]**.

   - 설정 **[!UICONTROL Assign to Store Views]** 위젯을 사용할 보기 또는 웹 사이트로 이동합니다.

   - 대상 **[!UICONTROL Sort Order]**&#x200B;을 클릭하고 숫자를 입력하여 컨테이너 내에서 위젯의 배치를 결정합니다.

     `0` = 첫 번째(기본값), `1` = 초, `2` = 세 번째 등입니다.

1. 다음에서 _[!UICONTROL Layout Updates]_섹션, 클릭&#x200B;**[!UICONTROL Add Layout Update]**및 설정&#x200B;**[!UICONTROL Display on]**다음 중 하나를 수행합니다.

   - _[!UICONTROL Categories]_

      - `Anchor Categories`
      - `Non-Anchor Categories`

   - _[!UICONTROL Products]_

      - `All Product Type`
      - `Simple Product`
      - `Virtual Product`
      - `Bundle Product`
      - `Configurable Product`
      - `Downloadable Product`
      - `Gift Card`
      - `Grouped Product`

   - _[!UICONTROL Generic Page]_

      - `All Pages`
      - `Specified Page`
      - `Page Layouts`

1. 다음에서 **[!UICONTROL Container]** 목록에서 배치할 페이지 레이아웃의 영역을 선택합니다.

   ![위시리스트 검색 위젯 - 레이아웃](./assets/widget-wishlist-search-storefront.png){width="700" zoomable="yes"}

1. 왼쪽 패널에서 을 선택합니다 **[!UICONTROL Widget Options]**.

1. 설정 **[!UICONTROL Quick Search Form Types]** 다음 중 하나를 수행합니다.

   - `All Forms` - 고객이 사용 가능한 모든 매개 변수를 기준으로 검색할 수 있습니다.
   - `Owner Name` - 고객은 소유자 이름별로 위시리스트를 검색할 수 있습니다.
   - `Owner Email` - 고객은 소유자 이메일 주소별로 위시리스트를 검색할 수 있습니다.

   >[!NOTE]
   >
   >배송 주소는 위시리스트에 포함되지 않습니다.

1. 필요한 경우 표준에 따라 나머지 위젯 속성을 구성합니다 [지침](../content-design/widget-create.md).

1. 완료되면 다음을 클릭하십시오. **[!UICONTROL Save]**.

1. 메시지가 표시되면 잘못된 캐시를 모두 새로 고칩니다.
