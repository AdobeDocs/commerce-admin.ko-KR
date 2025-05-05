---
title: 이동 경로 추적
description: 다양한 이동 경로 추적 패턴과 콘텐츠 및 카탈로그 페이지에 표시되도록 구성하는 방법에 대해 알아봅니다.
exl-id: 2f60d48e-960f-437c-8f8f-a3d06cc0840a
feature: Catalog Management, Categories, Site Navigation, Page Content
source-git-commit: 01148770946a236ece2122be5a88b963a0f07d1f
workflow-type: tm+mt
source-wordcount: '390'
ht-degree: 0%

---

# 이동 경로 추적

_이동 경로_&#x200B;은(는) 고객이 저장소의 다른 페이지와 관련하여 현재 있는 위치를 보여 주는 링크 집합입니다. 이동 경로의 링크를 클릭하여 이전 페이지로 돌아갈 수 있습니다.

이동 경로는 콘텐츠 페이지 및 카탈로그 페이지에 나타나도록 구성할 수 있습니다. 이동 경로의 형식과 위치는 테마에 따라 다르지만 일반적으로 헤더 바로 아래에 있습니다. 기본적으로 이동 경로 기록이 CMS 페이지에 표시됩니다.

![상점 앞에 표시되는 이동 경로](./assets/storefront-breadcrumb-trail.png){width="700" zoomable="yes"}

## 빵가루의 일반적인 종류

이동 경로는 크게 세 가지 유형으로 나눌 수 있는데, 그 목적에 따라 차이가 있다. 각 종류의 빵 부스러기를 구현하는 본질과 주요 원리는 다음과 같다.

### 계층 구조 기반 탐색 표시

이러한 이동 경로는 사이트에 설정된 범주 계층 구조를 기반으로 합니다. 표시된 체인은 구조 내에서 사용자에게 위치를 알려 줍니다. 이 경우 각 텍스트 링크는 이전 페이지보다 한 단계 높은 페이지를 대상으로 합니다.

예: `Men > Tops > Hoodies & Sweatshirts`

이 유형의 장점은 사용자가 자신이 속한 카테고리 수준을 쉽게 볼 수 있고 카탈로그 페이지 간 탐색에 쉽게 액세스할 수 있다는 것입니다.

### 기록 기반 이동 경로

기록(또는 경로) 기반 탐색은 브라우저의 뒤로 버튼과 유사합니다. 이러한 유형의 탐색을 사용하면 변경 없이 방문했던 이전 페이지로 빠르게 돌아갈 수 있습니다.

이 유형의 장점은 고객이 카테고리 페이지에서 여러 필터를 선택한 후 이전 페이지로 돌아가고자 할 때 가장 도움이 된다는 것입니다.

예: `Home > What's New > Gear > Bags`

### 속성 기반 탐색 표시

이 유형의 이동 경로는 범주 페이지에서 선택한 속성을 표시합니다. 다른 유형과 주요 차이점은 속성 기반 탐색 표시가 특정 제품(예: 가격, 품질 및 색상)에 대해 고객이 탐색 계층에서 선택한 필터 및 옵션을 나타낸다는 것입니다.

예: `Home > Suits > All Suits > Refined by > Slim Fit`

## CMS 페이지에서 이동 경로 추가/제거

1. _관리자_ 사이드바에서 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**(으)로 이동합니다.

1. _[!UICONTROL General]_&#x200B;아래의 왼쪽 패널에서&#x200B;**[!UICONTROL Web]**&#x200B;을(를) 선택합니다.

   ![CMS 페이지에 대한 탐색 표시](../configuration-reference/general/assets/web-default-pages.png){width="600" zoomable="yes"}

1. _[!UICONTROL Default Pages]_&#x200B;섹션을 확장합니다.

1. **[!UICONTROL Use system value]** 확인란의 선택을 취소합니다.

1. **[!UICONTROL Show Breadcrumbs for CMS Pages]**&#x200B;을(를) `No` 또는 `Yes`(으)로 설정합니다.

1. 완료되면 **[!UICONTROL Save Config]**&#x200B;을(를) 클릭합니다.

>[!NOTE]
>
>상위 범주가 `Browsing Category`= `Deny` [범주 권한](category-permissions.md) 설정이 있는 경우 하위 범주 페이지의 이동 경로 추적에 상위 범주가 표시되지 않습니다.
