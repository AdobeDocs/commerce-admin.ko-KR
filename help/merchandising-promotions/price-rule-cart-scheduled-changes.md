---
title: 장바구니 가격 규칙에 대한 예약된 변경 사항
description: 캠페인의 일부로 일정에 따라 장바구니 가격 규칙을 적용하고 다른 콘텐츠 변경 사항과 그룹화하는 방법을 알아봅니다.
exl-id: 4c9caa04-1e11-440d-b3db-7cc5fc83a08f
feature: Merchandising, Price Rules, Shopping Cart
source-git-commit: 0ceb61e6f1629a3bef16c550362c1db25b4aefa5
workflow-type: tm+mt
source-wordcount: '489'
ht-degree: 0%

---

# 장바구니 가격 규칙에 대한 예약된 변경 사항

{{ee-feature}}

장바구니 가격 규칙은 캠페인의 일부로 일정에 따라 적용하고 다른 콘텐츠 변경 사항과 그룹화할 수 있습니다. 가격 규칙에 대한 예약된 변경 사항을 기반으로 캠페인을 생성하거나 변경 사항을 기존 캠페인에 적용할 수 있습니다.

>[!NOTE]
>
>![Adobe Commerce](../assets/adobe-logo.svg) Adobe Commerce에서 [!UICONTROL From] 및 [!UICONTROL To] 필드가 제거되었으며 장바구니 가격 규칙에서 직접 수정할 수 없습니다. 이러한 활성화를 위해 예약된 업데이트를 만들어야 합니다.

![장바구니 가격 규칙 - 예약된 변경 사항](./assets/content-staging-price-rules-cart-scheduled-changes.png){width="700" zoomable="yes"}

>[!NOTE]
>
>모든 예약된 업데이트가 연속적으로 적용됩니다. 즉, 모든 엔티티는 한 시점에서 하나의 예약된 업데이트만 가질 수 있습니다. 모든 예약된 업데이트는 해당 시간대 내의 모든 스토어 보기에 적용됩니다. 따라서 엔티티는 서로 다른 스토어 보기에 대해 동시에 서로 다른 예약된 업데이트를 가질 수 없습니다. 현재 예약된 업데이트의 영향을 받지 않는 모든 스토어 뷰 내의 모든 엔티티 속성 값은 이전 예약된 업데이트가 아닌 기본값에서 가져옵니다.

동일한 캠페인에서 여러 개의 가격 규칙이 실행되는 경우 가격 규칙의 _[!UICONTROL Priority]_&#x200B;설정에 따라 우선 순위가 결정됩니다. 자세한 내용은 [콘텐츠 스테이징](../content-design/content-staging.md)을 참조하세요.

>[!NOTE]
>
>활성 캠페인이 종료 날짜 없이 처음 만들어지는 경우 나중에 종료 날짜를 포함하도록 캠페인을 편집할 수 없습니다. 이러한 경우 중복 캠페인을 만들고 필요한 종료 날짜를 입력해야 합니다.

>[!NOTE]
>
>캠페인이 둘 이상의 장바구니 가격 규칙에 연결된 경우 [콘텐츠 스테이징 대시보드](../content-design/content-staging-dashboard.md)에서만 캠페인을 편집할 수 있습니다.

다음 주의 사항에 유의하십시오.

- 가격 규칙이 포함된 캠페인을 처음에 종료 날짜 없이 만든 경우 종료 날짜를 포함하도록 캠페인을 나중에 편집할 수 없습니다. 캠페인을 만들 때 종료 날짜를 추가하거나 기존 캠페인의 중복 버전을 만들고 필요에 따라 종료 날짜를 중복 날짜에 추가하는 것이 좋습니다.
- 예약된 업데이트를 사용하여 종료 날짜가 있는 장바구니 가격 규칙을 활성화할 때 규칙을 처음에 비활성화한 것으로 설정해야 합니다. 이미 활성화된 규칙은 종료 날짜를 준수하지 않습니다.
- 쿠폰이 장바구니 가격 규칙에 연결되어 있지 않습니다. 예약된 업데이트에서는 _[!UICONTROL Rule Information]_&#x200B;탭의&#x200B;_[!UICONTROL Coupon]_, _[!UICONTROL Coupon Code]_,_[!UICONTROL Uses per Coupon]_ 및 _[!UICONTROL Uses per Customer]_&#x200B;필드에 대한 액세스를 제공하지 않습니다. 또한&#x200B;_[!UICONTROL Manage Coupon Codes]_ 탭의 모든 설정을 사용할 수 없습니다.

>[!IMPORTANT]
>
>**_default_** 관리 시간대를 사용하여 캠페인 **[!UICONTROL Start Date]** 및 **[!UICONTROL End Date]**&#x200B;을(를) 정의해야 합니다. 이 시간대는 각 웹 사이트의 현지 시간대에서 변환됩니다. 서로 다른 시간대에 여러 개의 웹 사이트가 있지만 미국 시간대를 기반으로 하는 캠페인을 시작하려는 예를 생각해 보십시오. 이 경우 각 로컬 시간대에 대해 별도의 업데이트를 예약하고 각 로컬 웹 사이트 시간대에서 변환된 **[!UICONTROL Start Date]** 및 **[!UICONTROL End Date]**&#x200B;을(를) 기본 관리 시간대로 설정해야 합니다.
