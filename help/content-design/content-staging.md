---
title: 컨텐츠 스테이징
description: 콘텐츠 스테이징은 비즈니스 팀이 관리자로부터 직접 스토어에 대한 광범위한 콘텐츠 업데이트를 쉽게 만들고, 미리 보고, 예약할 수 있도록 합니다.
exl-id: 929cd020-cbc7-40bf-a22c-02df35212ecf
feature: Page Content, Staging
source-git-commit: d4c5cac590bff290e81c1c8fa55a5ca7b4d9a017
workflow-type: tm+mt
source-wordcount: '887'
ht-degree: 0%

---

# 컨텐츠 스테이징

{{ee-feature}}

콘텐츠 스테이징을 사용하면 비즈니스 팀이 _관리자_&#x200B;에서 직접 스토어에 대한 다양한 콘텐츠 업데이트를 쉽게 만들고, 미리 보고, 예약할 수 있습니다. 예를 들어 페이지를 정적 페이지로 생각하기보다는 일정에 따라 _on_ 또는 _off_&#x200B;할 수 있는 다양한 요소의 컬렉션으로 간주하십시오. 콘텐츠 스테이징을 사용하여 일정에 따라 1년 동안 자동으로 변경되는 페이지를 만들 수 있습니다.

_campaign_ 용어는 예약된 변경 내용 또는 스테이징 대시보드에서 관리되는 변경 내용의 컬렉션을 나타냅니다. 변경 사항은 달력 또는 타임라인에서 볼 수 있습니다. _예약된 변경_ 및 _예약된 업데이트_&#x200B;라는 용어는 서로 교환 가능하며 단일 변경 내용을 참조합니다.

특정 기간 동안 콘텐츠 변경을 예약하면 예약된 변경 사항이 만료되면 콘텐츠가 이전 버전으로 되돌아갑니다. 이후 업데이트에 사용할 동일한 기준 콘텐츠의 여러 버전을 만들 수 있습니다. 타임라인을 통해 뒤로 이동하여 이전 버전의 콘텐츠를 볼 수도 있습니다. 초안 버전을 저장하려면 타임라인에서 프로덕션에 들어가지 않을 만큼 먼 미래의 날짜를 지정하기만 하면 됩니다.

## 컨텐츠 스테이징 개체 및 캠페인

시작 날짜 및 종료 날짜와 관련된 필드는 Adobe Commerce에서 제거되었으며 장바구니 가격 규칙, 카탈로그 가격 규칙, 제품, 범주 및 CMS 페이지에서 직접 수정할 수 없습니다. 이러한 활성화를 위해 예약된 업데이트를 만들어야 합니다.

모든 예약된 업데이트가 연속적으로 적용되므로 모든 엔티티에 한 번에 하나의 예약된 업데이트만 있을 수 있습니다. 모든 예약된 업데이트는 해당 시간대 내의 모든 스토어 보기에 적용됩니다. 따라서 엔티티는 서로 다른 스토어 보기에 대해 동시에 다른 예약된 업데이트를 가질 수 없습니다. 현재 예약된 업데이트의 영향을 받지 않는 모든 스토어 뷰 내의 모든 엔티티 속성 값은 이전 예약된 업데이트가 아닌 기본값에서 가져옵니다.

다음 개체에 대해 예약된 업데이트가 새로 만들어지면 해당 캠페인이 자리 표시자로 만들어지고 _[!UICONTROL Scheduled Changes]_상자가 페이지 맨 위에 나타납니다. 자리 표시자 캠페인에는 시작 날짜가 있지만 종료 날짜는 없습니다. 캠페인의 일부로 콘텐츠에 대한 업데이트를 예약한 다음 날짜, 시간 또는 스토어 보기별로 변경 사항을 미리 보고 공유할 수 있습니다. 한 객체에 대해 새 캠페인이 생성되면 다른 객체에 대해 예약된 업데이트로 할당할 수 있습니다.

- [제품](../catalog/product-scheduled-changes.md)
- [카테고리](../catalog/category-scheduled-changes.md)
- [카탈로그 가격 규칙](../merchandising-promotions/price-rule-catalog-scheduled-changes.md)
- [장바구니 가격 규칙](../merchandising-promotions/price-rule-cart-scheduled-changes.md)
- [CMS 페이지](pages-workspace.md#scheduled-changes)
- [CMS 블록](blocks.md)

## 콘텐츠 스테이징 워크플로

1. **기준 콘텐츠 만들기**

   기준선은 캠페인이 없는 자산의 콘텐츠이며 페이지 상단의 _[!UICONTROL Scheduled Changes]_섹션 아래에 있는 모든 것을 포함합니다. 타임라인에서 해당 위치에 대해 변경 사항이 예약된 활성 캠페인이 없는 경우 기준선 컨텐츠가 항상 사용됩니다.

1. **첫 번째 캠페인 만들기**

   필요에 따라 시작 및 종료 날짜를 사용하여 첫 번째 캠페인을 만듭니다. 캠페인을 오픈 엔드로 만들려면 종료 날짜를 비워 둡니다. 첫 번째 캠페인이 종료되면 원래 기준선 컨텐츠가 복원됩니다.

   캠페인 시작 날짜 및 종료 날짜는 각 웹 사이트의 로컬 시간대에서 변환된 **_기본_** 관리 시간대를 사용하여 정의해야 합니다. 서로 다른 시간대에 여러 웹 사이트가 있지만 미국 시간대를 기반으로 캠페인을 시작하려는 경우를 생각해 보십시오. 이 경우 각 로컬 시간대에 대해 별도의 업데이트를 예약하고 각 로컬 웹 사이트 시간대에서 기본 관리 시간대로 변환된 **[!UICONTROL Start Date]** 및 **[!UICONTROL End Date]**&#x200B;을(를) 설정해야 합니다.

1. **두 번째 캠페인 추가**

   필요에 따라 시작 및 종료 날짜를 사용하여 두 번째 캠페인을 만듭니다. 두 번째 캠페인은 완전히 다른 기간에 할당할 수 있습니다. 동일한 자산에 대해 여러 캠페인을 만들 때 캠페인은 겹칠 수 없습니다. 필요한 만큼 캠페인을 만들 수 있습니다.

   아직 시작되지 않은 기존 캠페인에 여러 자산을 할당할 수 있습니다. 예를 들어 미래 시작 일자가 있는 동일한 캠페인의 범위에서 두 개의 다른 제품 가격을 업데이트할 수 있습니다.

   >[!NOTE]
   >
   >캠페인이 둘 이상의 엔터티에 연결된 경우 [콘텐츠 준비 대시보드](content-staging-dashboard.md)에서만 캠페인을 편집할 수 있습니다.

1. **기준 콘텐츠 복원**

   모든 캠페인에 종료 날짜가 있는 경우 모든 활성 캠페인이 종료될 때마다 기준선 컨텐츠가 복원됩니다.

>[!NOTE]
>
>엔티티에 대해 스테이징 업데이트가 활성 상태인 동안 엔티티를 편집하면 현재 활성 스테이징 업데이트가 편집됩니다. 스태이징 업데이트가 종료될 때 복원되는 기본 컨텐츠에는 영향을 주지 않습니다.

## [!UICONTROL Content Staging] 대시보드

[!UICONTROL Content Staging] [대시보드](content-staging-dashboard.md)는 계획된 모든 사이트 변경 사항 및 업데이트를 볼 수 있도록 합니다. 캠페인의 모든 날짜, 날짜 범위 또는 기간을 미리 보고 다른 사용자와 공유할 수 있습니다.

![스테이징 대시보드](./assets/content-staging-dashboard-grid.png){width="600" zoomable="yes"}

## 콘텐츠 스테이징 데모

콘텐츠 스테이징에 대해 알아보려면 다음 비디오를 시청하십시오.

>[!VIDEO](https://video.tv.adobe.com/v/343784?quality=12)

## 리소스 문제 해결

콘텐츠 스테이징 문제를 해결하는 데 대한 도움말은 다음 [!DNL Commerce] 지원 기술 문서를 참조하십시오.

- [콘텐츠 스테이징 문제로 인해 모든 페이지에서 오류 404 발생](https://experienceleague.adobe.com/docs/commerce-knowledge-base/kb/troubleshooting/site-down-or-unresponsive/error-404-on-all-pages-due-to-content-staging-issue.html)
- [예약된 콘텐츠 준비 업데이트가 오래된 Fastly 캐시와 함께 표시되지 않음](https://experienceleague.adobe.com/docs/commerce-knowledge-base/kb/troubleshooting/miscellaneous/scheduled-content-staging-updates-not-displayed-with-stale-fastly-cache.html)
- [공유 카탈로그의 가격에 대한 콘텐츠 스테이징 업데이트를 예약할 수 있습니까?](https://experienceleague.adobe.com/docs/commerce-knowledge-base/kb/faq/can-i-schedule-content-staging-updates-for-prices-in-a-shared-catalog.html)
