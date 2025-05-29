---
title: 개인 영업 및 이벤트
description: 비공개 판매 및 기타 카탈로그 이벤트를 사용하여 기존 고객 기반으로 판매를 증가시키고 버즈 및 새 리드를 생성하는 방법에 대해 알아봅니다.
exl-id: 0b890463-b1e5-4327-8d8a-372afd53312a
feature: Reporting, Promotions/Events
badgePaas: label="PaaS만" type="Informative" url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="Adobe Commerce 온 클라우드 프로젝트(Adobe 관리 PaaS 인프라) 및 온프레미스 프로젝트에만 적용됩니다."
source-git-commit: 7e28081ef2723d4113b957edede6a8e13612ad2f
workflow-type: tm+mt
source-wordcount: '446'
ht-degree: 0%

---

# 개인 영업 및 이벤트

{{ee-feature}}

비공개 판매 및 기타 카탈로그 이벤트는 기존 고객 기반을 사용하여 버즈 및 신규 리드를 생성하거나 잉여 재고를 제거하는 좋은 방법입니다. 제한된 기간 영업을 만들거나, 특정 회원으로 판매를 제한하거나, 독립 실행형 개인 영업 페이지를 만들 수 있습니다. 초대 및 이벤트 세부 사항을 정의할 수도 있습니다. 최고의 고객에게 VIP 대우를 제공하여 브랜드 충성도를 높이고 논란을 일으킵니다. 회원 전용 판매 또는 개인 판매에 대한 독점적 액세스 권한을 제공하여 브랜드 충성도를 높입니다. 당신은 또한 초과 상품을 청산하기 위해 이러한 판매를 사용할 수 있습니다. 고객 그룹은 이러한 유형의 멤버만 설정하고 VIP 판매를 설정하는 데 유용합니다.

![홈 페이지의 예제 상점 - 이벤트](./assets/storefront-event-home-page.png){width="700" zoomable="yes"}

## 이벤트 관리 구성 요소

- **범주** - 각 이벤트는 카탈로그의 [범주](../catalog/category-create.md)과(와) 연결되어 있습니다.

- **이벤트** - 이벤트 판매는 시작 및 종료 날짜를 기준으로 합니다. [카운트다운 티커](#event-ticker)를 사용하여 남은 시간을 표시할 수 있습니다.

- **카탈로그 이벤트 캐러셀** - 구성에서 [카탈로그 이벤트 위젯](../content-design/widget-event-carousel.md)을(를) 사용하도록 설정하면 저장소 페이지에 종료 날짜별로 정렬된 진행 중인 이벤트 및 예정된 이벤트 목록으로 배치할 수 있습니다. 두 개 이상의 이벤트에 동일한 종료 날짜가 있는 경우 이벤트는 구성에 지정된 순서를 기반으로 정렬됩니다.

- **[!UICONTROL Websites]** - 범주 권한은 주로 [고객 그룹](../customers/customer-groups.md)을 기반으로 합니다.

- **범주 권한** - [범주 권한](../catalog/category-permissions.md)을 사용하면 특정 범주에서 발생할 수 있는 특정 활동을 완벽하게 제어할 수 있습니다.

- **액세스 제한** - 랜딩 페이지, 로그인 페이지 또는 등록 페이지로 리디렉션하여 사이트에 대한 공개 [액세스](event-configure.md#restrict-access)를 방지합니다.

- **초대** - 스토어에서 계정을 만들 수 있는 링크가 포함된 전자 메일 메시지가 전송됩니다. [초대](invitations.md)를 받는 사람으로만 계정을 만드는 기능을 제한할 수 있습니다.

- **개인 판매 보고서** - [개인 판매 보고서](../getting-started/private-sales-reports.md)에서는 보낸 초대, 초대된 고객 및 전환에 대한 정보를 제공합니다.

## 이벤트 티커

티커 블록에는 예정된 이벤트의 시작 및 종료 날짜와 함께 열린 이벤트에 대한 카운트다운 티커가 표시됩니다. 이벤트가 종료된 경우 티켓에는 시작 날짜와 종료 날짜가 표시됩니다.

![Example storefront - 이벤트 캐러셀](./assets/storefront-event-ticker-carousel.png){width="700" zoomable="yes"}

이벤트에 대해 카테고리 페이지 티커를 활성화하면 카테고리 목록의 맨 위에 티커 블록이 표시됩니다. 제품 페이지 티커가 활성화된 경우 해당 카테고리와 연관된 제품의 제품 페이지 상단에 티커 블록도 표시됩니다.

[이벤트를 만드는 중](event-create.md)에 이벤트 티커를 사용할 수 있습니다.

![상점 첫 화면 - 이벤트 사이드바](./assets/storefront-event-sidebar.png){width="700" zoomable="yes"}
