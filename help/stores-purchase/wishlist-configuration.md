---
title: 위시리스트 구성
description: 스토어 고객을 위한 위시리스트 기능을 구성하는 방법에 대해 알아봅니다.
exl-id: 479455f1-282f-4277-b132-45c5867fb21c
feature: Customers, Configuration
source-git-commit: 8b5af316ab1d2e632ed5fc2066974326830ab3f7
workflow-type: tm+mt
source-wordcount: '536'
ht-degree: 0%

---

# 위시리스트 구성

위시리스트 구성은 위시리스트를 활성화하고 위시리스트를 공유할 때 사용되는 이메일 템플릿 및 이메일 메시지의 발신자를 결정합니다.

## 위시리스트 기능 활성화

1. _관리자_ 사이드바에서 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**(으)로 이동합니다.

1. 왼쪽 패널에서 **[!UICONTROL Customers]**&#x200B;을(를) 확장하고 **[!UICONTROL Wish List]**&#x200B;을(를) 선택합니다.

1. **[!UICONTROL General Options]** 섹션에서 ![확장 선택기](../assets/icon-display-expand.png)를 확장하고 다음을 수행합니다.

   ![고객 구성 - 위시리스트 일반 설정](../configuration-reference/customers/assets/wishlist-general-options.png){width="600" zoomable="yes"}

   - **[!UICONTROL Enabled]**&#x200B;을(를) `Yes`(으)로 전환하여 스토어에 대한 위시리스트 모듈을 활성화합니다.

   - ![Adobe Commerce](../assets/adobe-logo.svg)(Adobe Commerce만 해당) **[!UICONTROL Enable Multiple Wish Lists]**&#x200B;에서 `Yes`(으)로 전환하여 고객이 여러 위시리스트를 만들고 유지 관리할 수 있도록 합니다.

   - ![Adobe Commerce](../assets/adobe-logo.svg)(Adobe Commerce만 해당) 고객이 계정과 연결할 수 있는 위시리스트 수를 제한하려면 **[!UICONTROL Number of Multiple Wish Lists]** 값을 입력하십시오.

   - **[!UICONTROL Show in Sidebar]**&#x200B;을(를) `Yes`(으)로 전환하면 사이드바에 위시리스트가 표시됩니다.

1. **[!UICONTROL Share Options]** 섹션에서 ![확장 선택기](../assets/icon-display-expand.png)를 확장하고 다음을 수행합니다.

   ![고객 구성 - 위시리스트 공유 옵션](../configuration-reference/customers/assets/wishlist-share-options.png){width="600" zoomable="yes"}

   - **[!UICONTROL Email Sender]**&#x200B;을(를) 메시지 보낸 사람으로 표시되는 스토어 연락처로 설정합니다. 옵션: 일반 담당자, 영업 담당자, 고객 지원, 사용자 정의 이메일.

   - 고객이 위시리스트를 공유할 때 사용할 **[!UICONTROL Email Template]**&#x200B;을(를) 설정하십시오.

   - 고객이 보낼 수 있는 총 전자 메일 수를 제한하려면 **[!UICONTROL Max Emails Allowed to be Sent]** 값을 입력하십시오. 기본값은 10이며 최대 허용 수는 10,000입니다.

   - 메시지 크기를 제한하려면 **[!UICONTROL Email Text Length Limit]** 값을 입력하십시오. 기본값은 255입니다.

1. **[!UICONTROL My Wish List Link]** 섹션에서 ![확장 선택기](../assets/icon-display-expand.png)을(를) 확장하고 **[!UICONTROL Display Wish List Summary]**&#x200B;을(를) 다음 중 하나로 설정합니다.

   - `Display number of items in wish list`
   - `Display item quantities`

   ![고객 구성 - 위시리스트 표시](../configuration-reference/customers/assets/wishlist-my-wishlist-link.png){width="600" zoomable="yes"}

1. 완료되면 **[!UICONTROL Save Config]**&#x200B;을(를) 클릭합니다.

## 위시리스트 검색 추가

![Adobe Commerce](../assets/adobe-logo.svg)(Adobe Commerce 전용)

공개 위시리스트는 위시리스트 검색 [위젯](../content-design/widgets.md)을(를) 사용하여 찾을 수 있습니다. 위젯을 통해 고객은 위시리스트 소유자의 이름이나 이메일 주소로 검색할 수 있습니다. 스토어 고객은 다른 고객에 속한 위시리스트를 찾거나, 이를 보고 제품을 주문하거나, 제품을 자신의 위시리스트에 추가할 수 있습니다. 다른 고객이 공개 위시리스트에서 구매한 항목은 원래 위시리스트에서 제거되지 않습니다. 고객이 친구 및 가족 구성원의 위시리스트를 쉽게 찾을 수 있도록 스토어의 모든 페이지에 _위시리스트 검색_ 위젯을 추가할 수 있습니다.

![Storefront 예 - 위시리스트 검색](./assets/storefront-wishlist-search.png){width="700" zoomable="yes"}

1. _관리자_ 사이드바에서 **[!UICONTROL Content]** > _[!UICONTROL Elements]_>**[!UICONTROL Widgets]**(으)로 이동합니다.

1. 오른쪽 상단에서 **[!UICONTROL Add Widget]**&#x200B;을(를) 클릭합니다.

1. _[!UICONTROL Settings]_&#x200B;탭에서 다음을 수행합니다.

   - **[!UICONTROL Type]**&#x200B;을(를) `Wish List Search`(으)로 설정합니다.

   - **[!UICONTROL Design Theme]**&#x200B;을(를) 위시리스트가 추가된 스토어의 테마로 설정합니다.

   - **[!UICONTROL Continue]**&#x200B;을(를) 클릭합니다.

1. _[!UICONTROL Storefront Properties]_&#x200B;을(를) 완료합니다.

   - **[!UICONTROL Widget Title]** 입력.

   - 위젯을 사용할 보기 또는 웹 사이트로 **[!UICONTROL Assign to Store Views]**&#x200B;을(를) 설정합니다.

   - **[!UICONTROL Sort Order]**&#x200B;에 숫자를 입력하여 해당 컨테이너 내에서 위젯의 배치를 결정하십시오.

     `0` = 첫 번째(기본값), `1` = 두 번째, `2` = 세 번째 등입니다.

1. _[!UICONTROL Layout Updates]_&#x200B;섹션에서&#x200B;**[!UICONTROL Add Layout Update]**&#x200B;을(를) 클릭하고&#x200B;**[!UICONTROL Display on]**&#x200B;을(를) 다음 중 하나로 설정합니다.

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

1. **[!UICONTROL Container]** 목록에서 배치할 페이지 레이아웃의 영역을 선택합니다.

   ![위시리스트 검색 위젯 - 레이아웃](./assets/widget-wishlist-search-storefront.png){width="700" zoomable="yes"}

1. 왼쪽 패널에서 **[!UICONTROL Widget Options]**&#x200B;을(를) 선택합니다.

1. **[!UICONTROL Quick Search Form Types]**&#x200B;을(를) 다음 중 하나로 설정합니다.

   - `All Forms` - 고객이 사용 가능한 모든 매개 변수를 검색할 수 있습니다.
   - `Owner Name` - 고객은 소유자 이름별로 위시리스트를 검색할 수 있습니다.
   - `Owner Email` - 고객은 소유자 전자 메일 주소별로 위시리스트를 검색할 수 있습니다.

   >[!NOTE]
   >
   >배송 주소는 위시리스트에 포함되지 않습니다.

1. 필요한 경우 표준 [지침](../content-design/widget-create.md)에 따라 나머지 위젯 속성을 구성합니다.

1. 완료되면 **[!UICONTROL Save]**&#x200B;을(를) 클릭합니다.

1. 메시지가 표시되면 잘못된 캐시를 모두 새로 고칩니다.
