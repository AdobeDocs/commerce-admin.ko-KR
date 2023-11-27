---
title: 컨텐츠 스테이징
description: 콘텐츠 스테이징은 비즈니스 팀이 관리자로부터 직접 스토어에 대한 광범위한 콘텐츠 업데이트를 쉽게 만들고, 미리 보고, 예약할 수 있도록 합니다.
exl-id: 929cd020-cbc7-40bf-a22c-02df35212ecf
feature: Page Content, Staging
source-git-commit: b659c7e1e8f2ae9883f1e24d8045d6dd1e90cfc0
workflow-type: tm+mt
source-wordcount: '809'
ht-degree: 0%

---

# 컨텐츠 스테이징

{{ee-feature}}

콘텐츠 스테이징은 비즈니스 팀이에서 직접 스토어에 대한 광범위한 콘텐츠 업데이트를 쉽게 만들고, 미리 보고, 예약할 수 있도록 합니다. _관리자_. 예를 들어 페이지를 정적 페이지로 간주하지 않고 켤 수 있는 여러 요소의 컬렉션으로 간주합니다 _날짜_ 또는 _끔_ 일정에 따라. 콘텐츠 스테이징을 사용하여 일정에 따라 1년 동안 자동으로 변경되는 페이지를 만들 수 있습니다.

용어 _campaign_ 는 예약된 변경 사항의 레코드 또는 스테이징 대시보드에서 관리되는 변경 사항의 컬렉션을 나타냅니다. 변경 사항은 달력 또는 타임라인에서 볼 수 있습니다. 용어 _예약된 변경 내용_ 및 _예약된 업데이트_ 는 서로 호환되며, 단일 변경 사항을 나타냅니다.

특정 기간 동안 콘텐츠 변경을 예약하면 예약된 변경 사항이 만료되면 콘텐츠가 이전 버전으로 되돌아갑니다. 이후 업데이트에 사용할 동일한 기준 콘텐츠의 여러 버전을 만들 수 있습니다. 타임라인을 통해 뒤로 이동하여 이전 버전의 콘텐츠를 볼 수도 있습니다. 초안 버전을 저장하려면 타임라인에서 프로덕션에 들어가지 않을 만큼 먼 미래의 날짜를 지정하기만 하면 됩니다.

## 컨텐츠 스테이징 개체 및 캠페인

다음 객체에 대해 예약된 업데이트가 새로 생성되면 해당 캠페인이 자리 표시자로 생성되고 _[!UICONTROL Scheduled Changes]_상자가 페이지 맨 위에 나타납니다. 자리 표시자 캠페인에는 시작 날짜가 있지만 종료 날짜는 없습니다. 캠페인의 일부로 콘텐츠에 대한 업데이트를 예약한 다음 날짜, 시간 또는 스토어 보기별로 변경 사항을 미리 보고 공유할 수 있습니다. 한 객체에 대해 새 캠페인이 생성되면 다른 객체에 대해 예약된 업데이트로 할당할 수 있습니다.

- [제품](../catalog/product-scheduled-changes.md)
- [카테고리](../catalog/category-scheduled-changes.md)
- [카탈로그 가격 규칙](../merchandising-promotions/price-rule-catalog-scheduled-changes.md)
- [장바구니 가격 규칙](../merchandising-promotions/price-rule-cart-scheduled-changes.md)
- [CMS 페이지](pages-workspace.md#scheduled-changes)
- [CMS 블록](blocks.md)

## 콘텐츠 스테이징 워크플로

1. **기준선 콘텐츠 만들기**

   기준선은 캠페인이 없는 에셋의 콘텐츠이며 아래의 모든 것을 포함합니다. _[!UICONTROL Scheduled Changes]_페이지 상단에 있는 섹션입니다. 타임라인에서 해당 위치에 대해 변경 사항이 예약된 활성 캠페인이 없는 경우 기준선 컨텐츠가 항상 사용됩니다.

1. **첫 번째 캠페인 만들기**

   필요에 따라 시작 및 종료 날짜를 사용하여 첫 번째 캠페인을 만듭니다. 캠페인을 오픈 엔드로 만들려면 종료 날짜를 비워 둡니다. 첫 번째 캠페인이 종료되면 원래 기준선 컨텐츠가 복원됩니다.

   >[!NOTE]
   >
   >캠페인 시작 날짜 및 종료 날짜는 다음을 사용하여 정의해야 합니다. **_기본값_** 관리 시간대로, 각 웹 사이트의 로컬 시간대에서 변환됩니다. 서로 다른 시간대에 여러 웹 사이트가 있지만 미국 시간대를 기반으로 캠페인을 시작하려는 경우를 생각해 보십시오. 이 경우 각 현지 시간대에 대해 별도의 업데이트를 예약하고 을 설정해야 합니다 **[!UICONTROL Start Date]** 및 **[!UICONTROL End Date]** 를 각 로컬 웹 사이트 시간대에서 기본 관리 시간대로 변환합니다.

1. **두 번째 캠페인 추가**

   필요에 따라 시작 및 종료 날짜를 사용하여 두 번째 캠페인을 만듭니다. 두 번째 캠페인은 완전히 다른 기간에 할당할 수 있습니다. 동일한 자산에 대해 여러 캠페인을 만들 때 캠페인은 겹칠 수 없습니다. 필요한 만큼 캠페인을 만들 수 있습니다.

   >[!NOTE]
   >
   >모든 예약된 업데이트가 연속적으로 적용되므로 모든 엔티티에 한 번에 하나의 예약된 업데이트만 있을 수 있습니다. 모든 예약된 업데이트는 해당 시간대 내의 모든 스토어 보기에 적용됩니다. 따라서 엔티티는 서로 다른 스토어 보기에 대해 동시에 다른 예약된 업데이트를 가질 수 없습니다. 현재 예약된 업데이트의 영향을 받지 않는 모든 스토어 뷰 내의 모든 엔티티 속성 값은 이전 예약된 업데이트가 아닌 기본값에서 가져옵니다.

1. **기준 콘텐츠 복원**

   모든 캠페인에 종료 날짜가 있는 경우 모든 활성 캠페인이 종료될 때마다 기준선 컨텐츠가 복원됩니다.

>[!NOTE]
>
>엔티티에 대해 스테이징 업데이트가 활성 상태인 동안 엔티티를 편집하면 현재 활성 스테이징 업데이트가 편집됩니다. 스태이징 업데이트가 종료될 때 복원되는 기본 컨텐츠에는 영향을 주지 않습니다.

## [!UICONTROL Content Staging] 대시보드

다음 [!UICONTROL Content Staging] [대시보드](content-staging-dashboard.md) 계획된 모든 사이트 변경 사항 및 업데이트에 대한 가시성을 제공합니다. 캠페인의 모든 날짜, 날짜 범위 또는 기간을 미리 보고 다른 사용자와 공유할 수 있습니다.

![스테이징 대시보드](./assets/content-staging-dashboard-grid.png){width="600" zoomable="yes"}

## 콘텐츠 스테이징 데모

콘텐츠 스테이징에 대해 알아보려면 다음 비디오를 시청하십시오.

>[!VIDEO](https://video.tv.adobe.com/v/343784?quality=12)

## 리소스 문제 해결

콘텐츠 스테이징 문제 해결에 대한 도움말을 보려면 다음을 참조하십시오 [!DNL Commerce] 지원 기술 자료 문서:

- [컨텐츠 스테이징 문제로 인한 모든 페이지 오류 404](https://experienceleague.adobe.com/docs/commerce-knowledge-base/kb/troubleshooting/site-down-or-unresponsive/error-404-on-all-pages-due-to-content-staging-issue.html)
- [예약된 컨텐츠 스테이징 업데이트가 오래된 Fastly 캐시와 함께 표시되지 않음](https://experienceleague.adobe.com/docs/commerce-knowledge-base/kb/troubleshooting/miscellaneous/scheduled-content-staging-updates-not-displayed-with-stale-fastly-cache.html)
- [공유 카탈로그의 가격에 대한 콘텐츠 스테이징 업데이트를 예약할 수 있습니까?](https://experienceleague.adobe.com/docs/commerce-knowledge-base/kb/faq/can-i-schedule-content-staging-updates-for-prices-in-a-shared-catalog.html)
