---
title: 범주 권한
description: 카테고리를 사용하여 제품 가격 표시를 제어하고, 장바구니에 제품을 추가할 수 있는 고객 그룹을 결정하고 랜딩 페이지를 지정하는 방법을 알아봅니다.
exl-id: d80a0545-918e-4c08-9f37-4aa3cd7771f4
feature: Catalog Management, Categories, Customers, Configuration
source-git-commit: 01148770946a236ece2122be5a88b963a0f07d1f
workflow-type: tm+mt
source-wordcount: '777'
ht-degree: 0%

---

# 범주 권한

{{ee-feature}}

범주 액세스는 특정 고객 그룹으로 제한하거나 완전히 제한할 수 있습니다. 제품 가격 표시를 제어하고 장바구니에 제품을 추가할 수 있는 고객 그룹을 결정하고 랜딩 페이지를 지정할 수 있습니다.

>[!NOTE]
>
>카테고리 권한에는 전역 범위가 있으며 활성화된 경우 개별 권한에 따라 각 카테고리에 대한 액세스를 제한합니다. 기본적으로 카테고리 권한은 활성화되어 있지 않습니다.

예를 들어 도매 고객에게만 판매하는 경우, 모든 사람이 카탈로그를 검색하도록 허용하지만 가격은 표시하고 다음에 있는 쇼핑객에 대해서만 구매를 허용할 수 있습니다. _도매_ 고객 그룹. 다음 예에서는 로그인한 사용자만 &quot;컬렉션&quot; 카테고리에 액세스할 수 있습니다. 게스트의 경우 &quot;컬렉션&quot; 옵션이 메인 메뉴에 나타나지 않습니다.

![로그인한 사용자에게 &quot;컬렉션&quot; 카테고리가 표시됨](./assets/storefront-category-permissions-logged-in.png){width="600" zoomable="yes"}

활성화되면 새 항목 _[!UICONTROL Category Permissions]_[범주] 페이지에 각 범주에 필요한 액세스 권한을 적용할 수 있는 섹션이 나타납니다. 서로 다른 웹 사이트 및 고객 그룹에 대해 각 카테고리에 여러 권한 규칙을 추가할 수 있습니다.

## 1단계: 범주 권한 구성

>[!IMPORTANT]
>
>모든 기존 항목 [그룹 권한 설정](../configuration-reference/catalog/catalog.md#category-permissions) 은(는) 다음을 무시합니다. **_모두_** 카탈로그에 있는 범주 **_[!UICONTROL Shared Catalog]_** 기능이 활성화되었습니다. [!UICONTROL Shared Catalog] 카탈로그가 활성화되면 카탈로그의 모든 범주 권한을 완전히 제어합니다.

1. 다음에서 _관리자_ 사이드바, 이동 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. 왼쪽 패널에서 를 확장합니다. **[!UICONTROL Catalog]** 및 선택 **[!UICONTROL Catalog]** 밑에.

1. 확장 ![확장 선택기](../assets/icon-display-expand.png) 다음 **[!UICONTROL Category Permissions]** 섹션.

   ![범주 권한](../configuration-reference/catalog/assets/catalog-category-permissions.png){width="600" zoomable="yes"}

   이러한 옵션에 대한 자세한 목록은 다음을 참조하십시오. [범주 권한](../configuration-reference/catalog/catalog.md#category-permissions) 다음에서 _구성 참조_.

1. 설정 **[!UICONTROL Enable]** 끝 `Yes`.

1. 스토어에서 허용하거나 제한할 내용에 따라 다른 옵션을 완료합니다(다음 섹션 참조).

1. 완료되면 다음을 클릭하십시오. **[!UICONTROL Save Config]**.

1. 캐시를 업데이트하라는 메시지가 표시되면 **[!UICONTROL Cache Management]** 시스템 메시지에 연결하고 지침에 따라 캐시를 새로 고칩니다.

### [!UICONTROL Allow Browsing Category]

이 옵션은 의 모든 범주에 적용됩니다. [웹 사이트](../getting-started/websites-stores-views.md).

의 구성원을 허용하려면 **_특정 고객 그룹_** 범주 제품을 찾아보려면 다음을 수행합니다.

1. 설정 **[!UICONTROL Allow Browsing Category]** 끝 `Specified Customer Groups`.

1. 다음에서 **[!UICONTROL Customer Groups]** 상자에서 카테고리의 제품을 검색할 수 있는 각 그룹을 선택합니다.

   여러 그룹을 선택하려면 Ctrl 키(PC) 또는 Command 키(Mac)를 누른 채 각 그룹을 클릭합니다.

   ![도매 고객 그룹별 검색 허용](./assets/category-permissions-allow-browsing-customer-groups.png){width="600" zoomable="yes"}

종료 **_액세스 제한 및 랜딩 페이지로 리디렉션_**&#x200B;를 사용하여 다음을 수행합니다.

1. 설정 **[!UICONTROL Allow Browsing Category]** 끝 `No, Redirect to Landing Page`.

1. 다음을 선택합니다. **[!UICONTROL Landing Page]** 방문자가 리디렉션되는 위치입니다.

   ![홈 페이지로 리디렉션](./assets/category-permissions-browse-category-landing-page.png){width="600" zoomable="yes"}

   >[!NOTE]
   >
   >하지만 _[!UICONTROL Allow Browsing Category]_설정은 웹 사이트의 모든 카테고리에 적용되며, 각 스토어 보기에 대해 다른 랜딩 페이지를 구성할 수 있습니다.

### [!UICONTROL Display Product Prices]

이 옵션은 의 모든 범주에 적용됩니다. [웹 사이트](../getting-started/websites-stores-views.md).

다음의 멤버만 허용하려면 **_특정 고객 그룹_** 이 범주의 제품 가격을 보려면 다음을 수행하십시오.

1. 설정 **[!UICONTROL Display Product Prices]** 끝 `Yes, for Specified Customer Groups`.

1. 다음에서 **[!UICONTROL Customer Groups]** 박스에서 범주 내 제품 가격을 볼 수 있는 각 그룹을 선택합니다.

   여러 그룹을 선택하려면 Ctrl 키(PC) 또는 Command 키(Mac)를 누른 채 각 그룹을 클릭합니다.

   ![도매 고객 그룹만 가격을 볼 수 있습니다.](./assets/category-permissions-price-customer-groups.png){width="600" zoomable="yes"}

### [!UICONTROL Allow Adding to Cart]

이 옵션은 의 모든 범주에 적용됩니다. [웹 사이트](../getting-started/websites-stores-views.md).

다음의 멤버만 허용하려면 **_특정 고객 그룹_** 범주 제품을 장바구니에 넣으려면 다음을 수행하십시오.

1. 설정 **[!UICONTROL Allow Adding to Cart]** 끝 `Yes, for Specified Customer Groups`.

1. 다음에서 **[!UICONTROL Customer Groups]** 상자에서 카테고리에서 장바구니에 제품을 추가할 수 있는 각 그룹을 선택합니다.

   여러 그룹을 선택하려면 Ctrl 키(PC) 또는 Command 키(Mac)를 누른 채 각 그룹을 클릭합니다.

   ![도매 고객 그룹만 장바구니에 제품을 넣을 수 있습니다.](./assets/category-permissions-cart-customer-groups.png){width="600" zoomable="yes"}

### [!UICONTROL Disallow Catalog Search]

특정 고객 그룹의 구성원이 카탈로그 검색을 사용하지 않도록 하려면 이 옵션을 설정하십시오. 의 모든 카테고리에 적용됩니다. [웹 사이트](../getting-started/websites-stores-views.md).

- 허용하려면 **_로그인한 고객만_** 카탈로그 검색을 사용하려면 다음을 선택합니다. `NOT LOGGED IN`.

- 허용하려면 **_특정 고객 그룹만_** 카탈로그 검색을 사용하려면 범주 검색 사용에서 제외할 각 그룹을 선택합니다.

  여러 그룹을 선택하려면 Ctrl 키(PC) 또는 Command 키(Mac)를 누른 채 각 그룹을 클릭합니다.

  ![일반 고객 그룹에 카탈로그 검색이 허용되지 않음](./assets/category-permissions-disallow-category-search.png){width="600" zoomable="yes"}

## 2단계: 범주 권한 적용

1. 다음에서 _관리자_ 사이드바, 이동 **[!UICONTROL Catalog]** > **[!UICONTROL Categories]**.

1. 범주 트리에서 대상 범주를 선택합니다.

1. 확장 ![확장 선택기](../assets/icon-display-expand.png) **[!UICONTROL Category Permissions]** 페이지에서 다음을 수행합니다.

   - 권한 규칙을 만들려면 **[!UICONTROL New Permission]**.

     ![범주 권한 섹션](./assets/category-permissions-section-admin.png){width="600" zoomable="yes"}

   - 해당 항목 선택 **[!UICONTROL Website]** 및 **[!UICONTROL Customer Group]**.

   - 필요에 따라 개별 권한을 설정합니다.

   >[!NOTE]
   >
   >날짜 `Browsing Category` = `Deny` 권한이 상위 범주에 대해 설정되어 있지만 [이동 경로](navigation-breadcrumb-trail.md) 하위 범주 페이지에서 참조할 수 있습니다.

1. 완료되면 다음을 클릭하십시오. **[!UICONTROL Save]**.

>[!NOTE]
>
>있는 경우 **_허용_** 다음에 대한 권한이 설정됨: `Root Category`를 입력하면 모든 하위 범주 및 내에 있는 모든 제품에 이러한 권한이 자동으로 적용됩니다. `Catalog`. 제품이 여러 범주에 할당되고 있는 경우 **_허용_** 하나 이상의 카테고리에 대한 권한이 자동으로 동일합니다. **_허용_** 할당된 모든 범주에 대한 권한.
