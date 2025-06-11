---
title: 주문 및 반품 위젯
description: 주문 및 반품 위젯을 사용하여 고객의 주문 상태를 확인하고, 송장을 인쇄하고, 선적을 추적할 수 있는 기능을 제공하는 방법에 대해 알아봅니다.
exl-id: 1c3948e6-a0de-4ee4-8abf-10ab845a94a7
feature: Page Content, Orders, Returns
badgePaas: label="PaaS만" type="Informative" url="https://experienceleague.adobe.com/ko/docs/commerce/user-guides/product-solutions" tooltip="Adobe Commerce 온 클라우드 프로젝트(Adobe 관리 PaaS 인프라) 및 온프레미스 프로젝트에만 적용됩니다."
source-git-commit: 57a913b21f4cbbb4f0800afe13012ff46d578f8e
workflow-type: tm+mt
source-wordcount: '371'
ht-degree: 0%

---

# 주문 및 반품 위젯

_주문 및 반품_ 위젯을 통해 게스트는 주문 상태를 확인하고, 송장을 인쇄하고, 배송을 추적할 수 있습니다. 위젯이 상점 앞에 추가되면 게스트 및 계정에 로그인하지 않은 고객에게만 표시됩니다. 주문 ID, 청구 성 및 이메일 주소 또는 우편 번호를 제공하여 주문을 찾을 수 있습니다.

![상점 앞 사이드바의 주문 및 반품 위젯](./assets/storefront-widget-orders-returns-sidebar.png){width="600" zoomable="yes"}

## 상점 첫 화면의 주문 및 반품 위젯

1. 고객은 **[!UICONTROL Find Order By]** 옵션을 사용하여 다음 매개 변수 중 하나를 선택하여 주문을 찾을 수 있습니다.

   - 이메일 주소
   - 우편 번호

1. 고객이 **[!UICONTROL Order ID]** 및 **[!UICONTROL Billing Last Name]**&#x200B;을(를) 입력합니다.

1. 주문과 연결된 청구 **[!UICONTROL Email Address]** 또는 **[!UICONTROL ZIP Code]**&#x200B;을(를) 입력합니다.

1. 주문을 검색하려면 **[!UICONTROL Search]**&#x200B;을(를) 클릭합니다.

   ![상점 앞에 표시되는 주문 정보](./assets/storefront-widget-orders-returns-view.png){width="700" zoomable="yes"}

## 주문 및 반품 위젯 설정

1. _관리자_ 사이드바에서 **[!UICONTROL Content]** > _[!UICONTROL Elements]_>**[!UICONTROL Widgets]**(으)로 이동합니다.

1. 오른쪽 상단에서 **[!UICONTROL Add Widget]**&#x200B;을(를) 클릭합니다.

1. _[!UICONTROL Settings]_&#x200B;섹션에서 다음을 수행합니다.

   - **[!UICONTROL Type]**&#x200B;을(를) `Orders and Returns`(으)로 설정합니다.

   - 스토어에서 사용하는 **[!UICONTROL Design Theme]**&#x200B;을(를) 선택하십시오.

1. **[!UICONTROL Continue]**&#x200B;을(를) 클릭합니다.

1. _[!UICONTROL Storefront Properties]_&#x200B;섹션에서 다음을 수행합니다.

   - **[!UICONTROL Widget Title]**&#x200B;의 경우 위젯에 대한 설명 제목을 입력합니다.

     이 제목은 관리자만 볼 수 있습니다.

   - **[!UICONTROL Assign to Store Views]**&#x200B;의 경우 위젯이 표시되는 스토어 보기를 선택하십시오.

     특정 스토어 보기 또는 `All Store Views`을(를) 선택할 수 있습니다. 여러 뷰를 선택하려면 Ctrl 키(PC) 또는 Command 키(Mac)를 누른 상태에서 각 옵션을 클릭합니다.

   - (선택 사항) **[!UICONTROL Sort Order]**&#x200B;의 경우 숫자를 입력하여 이 항목이 페이지의 동일한 부분에 있는 다른 항목과 함께 표시되는 순서를 결정합니다. (`0` = 첫 번째, `1` = 두 번째, `3` = 세 번째 등)

1. _[!UICONTROL Layout Updates]_&#x200B;섹션에서&#x200B;**[!UICONTROL Add Layout Update]**&#x200B;을(를) 클릭하고 다음을 수행합니다.

   - 위젯을 표시할 페이지 형식으로 **[!UICONTROL Display On]**&#x200B;을(를) 설정합니다.

   - 위젯이 페이지에 표시되는 위치를 확인하려면 나머지 레이아웃 업데이트 정보를 완료하십시오.

1. 완료되면 **[!UICONTROL Save]**&#x200B;을(를) 클릭합니다.

1. 캐시를 새로 고치라는 메시지가 표시되면 페이지 상단에 있는 메시지에서 링크를 클릭하고 지침을 따릅니다.
