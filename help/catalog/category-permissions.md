---
title: 범주 권한
description: 카테고리를 사용하여 제품 가격 표시를 제어하고, 장바구니에 제품을 추가할 수 있는 고객 그룹을 결정하고 랜딩 페이지를 지정하는 방법을 알아봅니다.
exl-id: d80a0545-918e-4c08-9f37-4aa3cd7771f4
feature: Catalog Management, Categories, Customers, Configuration
source-git-commit: 01148770946a236ece2122be5a88b963a0f07d1f
workflow-type: tm+mt
source-wordcount: '779'
ht-degree: 0%

---

# 범주 권한

{{ee-feature}}

범주 액세스는 특정 고객 그룹으로 제한하거나 완전히 제한할 수 있습니다. 제품 가격 표시를 제어하고 장바구니에 제품을 추가할 수 있는 고객 그룹을 결정하고 랜딩 페이지를 지정할 수 있습니다.

>[!NOTE]
>
>카테고리 권한에는 전역 범위가 있으며 활성화된 경우 개별 권한에 따라 각 카테고리에 대한 액세스를 제한합니다. 기본적으로 카테고리 권한은 활성화되어 있지 않습니다.

예를 들어 도매 고객에게만 판매하는 경우, 모든 사람이 카탈로그를 검색하도록 허용하되 가격은 표시하고 _도매_ 고객 그룹의 쇼핑객에 대해서만 구매를 허용할 수 있습니다. 다음 예에서는 로그인한 사용자만 &quot;컬렉션&quot; 카테고리에 액세스할 수 있습니다. 게스트의 경우 &quot;컬렉션&quot; 옵션이 메인 메뉴에 나타나지 않습니다.

![로그인한 사용자에게 &quot;컬렉션&quot; 범주 표시](./assets/storefront-category-permissions-logged-in.png){width="600" zoomable="yes"}

활성화되면 각 범주에 필요한 액세스 권한을 적용할 수 있는 새 _[!UICONTROL Category Permissions]_&#x200B;섹션이 [범주] 페이지에 나타납니다. 서로 다른 웹 사이트 및 고객 그룹에 대해 각 카테고리에 여러 권한 규칙을 추가할 수 있습니다.

## 1단계: 범주 권한 구성

>[!IMPORTANT]
>
>**_[!UICONTROL Shared Catalog]_** 기능을 사용하도록 설정하면 카탈로그의 **_모든_** 범주에서 기존의 모든 [그룹 권한 설정](../configuration-reference/catalog/catalog.md#category-permissions)을 무시합니다. [!UICONTROL Shared Catalog]은(는) 카탈로그가 활성화되면 카탈로그의 모든 범주 권한을 완전히 제어합니다.

1. _관리자_ 사이드바에서 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**(으)로 이동합니다.

1. 왼쪽 패널에서 **[!UICONTROL Catalog]**&#x200B;을(를) 확장하고 아래의 **[!UICONTROL Catalog]**&#x200B;을(를) 선택합니다.

1. **[!UICONTROL Category Permissions]** 섹션에서 ![확장 선택기](../assets/icon-display-expand.png)를 확장합니다.

   ![범주 권한](../configuration-reference/catalog/assets/catalog-category-permissions.png){width="600" zoomable="yes"}

   이러한 옵션에 대한 자세한 목록이 필요하면 _구성 참조_&#x200B;에서 [범주 권한](../configuration-reference/catalog/catalog.md#category-permissions)을 참조하십시오.

1. **[!UICONTROL Enable]**&#x200B;을(를) `Yes`(으)로 설정합니다.

1. 스토어에서 허용하거나 제한할 내용에 따라 다른 옵션을 완료합니다(다음 섹션 참조).

1. 완료되면 **[!UICONTROL Save Config]**&#x200B;을(를) 클릭합니다.

1. 캐시를 업데이트하라는 메시지가 표시되면 시스템 메시지에서 **[!UICONTROL Cache Management]** 링크를 클릭하고 지침에 따라 캐시를 새로 고칩니다.

### [!UICONTROL Allow Browsing Category]

이 옵션은 [웹 사이트](../getting-started/websites-stores-views.md)의 모든 범주에 적용됩니다.

**_특정 고객 그룹_**&#x200B;의 구성원이 범주 제품을 검색할 수 있도록 하려면 다음을 수행하십시오.

1. **[!UICONTROL Allow Browsing Category]**&#x200B;을(를) `Specified Customer Groups`(으)로 설정합니다.

1. **[!UICONTROL Customer Groups]** 상자에서 해당 범주의 제품을 검색할 수 있는 각 그룹을 선택합니다.

   여러 그룹을 선택하려면 Ctrl 키(PC) 또는 Command 키(Mac)를 누른 채 각 그룹을 클릭합니다.

   ![도매 고객 그룹별 검색 허용](./assets/category-permissions-allow-browsing-customer-groups.png){width="600" zoomable="yes"}

**_액세스를 제한하고 랜딩 페이지로 리디렉션_**&#x200B;하려면 다음을 수행하십시오.

1. **[!UICONTROL Allow Browsing Category]**&#x200B;을(를) `No, Redirect to Landing Page`(으)로 설정합니다.

1. 방문자가 리디렉션되는 **[!UICONTROL Landing Page]**&#x200B;을(를) 선택하십시오.

   ![홈 페이지로 리디렉션](./assets/category-permissions-browse-category-landing-page.png){width="600" zoomable="yes"}

   >[!NOTE]
   >
   >_[!UICONTROL Allow Browsing Category]_&#x200B;설정이 웹 사이트의 모든 범주에 적용되지만 각 스토어 보기에 대해 다른 랜딩 페이지를 구성할 수 있습니다.

### [!UICONTROL Display Product Prices]

이 옵션은 [웹 사이트](../getting-started/websites-stores-views.md)의 모든 범주에 적용됩니다.

**_특정 고객 그룹_**&#x200B;의 구성원만 이 범주의 제품 가격을 볼 수 있도록 하려면 다음을 수행하십시오.

1. **[!UICONTROL Display Product Prices]**&#x200B;을(를) `Yes, for Specified Customer Groups`(으)로 설정합니다.

1. **[!UICONTROL Customer Groups]** 상자에서 해당 범주의 제품 가격을 볼 수 있는 각 그룹을 선택합니다.

   여러 그룹을 선택하려면 Ctrl 키(PC) 또는 Command 키(Mac)를 누른 채 각 그룹을 클릭합니다.

   ![도매 고객 그룹만 가격을 볼 수 있음](./assets/category-permissions-price-customer-groups.png){width="600" zoomable="yes"}

### [!UICONTROL Allow Adding to Cart]

이 옵션은 [웹 사이트](../getting-started/websites-stores-views.md)의 모든 범주에 적용됩니다.

**_특정 고객 그룹_**&#x200B;의 구성원만 범주 제품을 장바구니에 넣을 수 있도록 하려면 다음을 수행하십시오.

1. **[!UICONTROL Allow Adding to Cart]**&#x200B;을(를) `Yes, for Specified Customer Groups`(으)로 설정합니다.

1. **[!UICONTROL Customer Groups]** 상자에서 범주의 제품을 장바구니에 추가할 수 있는 각 그룹을 선택합니다.

   여러 그룹을 선택하려면 Ctrl 키(PC) 또는 Command 키(Mac)를 누른 채 각 그룹을 클릭합니다.

   ![도매 고객 그룹만 장바구니에 제품을 넣을 수 있습니다](./assets/category-permissions-cart-customer-groups.png){width="600" zoomable="yes"}

### [!UICONTROL Disallow Catalog Search]

특정 고객 그룹의 구성원이 카탈로그 검색을 사용하지 않도록 하려면 이 옵션을 설정하십시오. [웹 사이트](../getting-started/websites-stores-views.md)의 모든 범주에 적용됩니다.

- **_로그인한 고객만_**&#x200B;에서 카탈로그 검색을 사용할 수 있도록 하려면 `NOT LOGGED IN`을(를) 선택하십시오.

- **_특정 고객 그룹만_**&#x200B;이 카탈로그 검색을 사용할 수 있도록 하려면 범주 검색 사용 시 제외할 각 그룹을 선택하십시오.

  여러 그룹을 선택하려면 Ctrl 키(PC) 또는 Command 키(Mac)를 누른 채 각 그룹을 클릭합니다.

  ![일반 고객 그룹에 대해 카탈로그 검색이 허용되지 않음](./assets/category-permissions-disallow-category-search.png){width="600" zoomable="yes"}

## 2단계: 범주 권한 적용

1. _관리자_ 사이드바에서 **[!UICONTROL Catalog]** > **[!UICONTROL Categories]**(으)로 이동합니다.

1. 범주 트리에서 대상 범주를 선택합니다.

1. 페이지에서 ![확장 선택기](../assets/icon-display-expand.png) **[!UICONTROL Category Permissions]**&#x200B;을(를) 확장하고 다음을 수행합니다.

   - 권한 규칙을 만들려면 **[!UICONTROL New Permission]**&#x200B;을(를) 클릭합니다.

     ![범주 권한 섹션](./assets/category-permissions-section-admin.png){width="600" zoomable="yes"}

   - 적용 가능한 **[!UICONTROL Website]** 및 **[!UICONTROL Customer Group]**&#x200B;을(를) 선택하십시오.

   - 필요에 따라 개별 권한을 설정합니다.

   >[!NOTE]
   >
   >상위 범주에 대해 `Browsing Category` = `Deny` 권한이 설정된 경우 하위 범주 페이지의 [이동 경로 추적](navigation-breadcrumb-trail.md)에 표시되지 않습니다.

1. 완료되면 **[!UICONTROL Save]**&#x200B;을(를) 클릭합니다.

>[!NOTE]
>
>`Root Category`에 대해 **_허용_** 권한이 설정된 경우 이러한 권한은 `Catalog` 내의 모든 하위 범주 및 모든 제품에 자동으로 적용됩니다. 제품이 여러 범주에 할당되고 하나 이상의 범주에 대해 **_Allow_** 권한이 있는 경우 할당된 모든 범주에 대해 자동으로 동일한 **_Allow_** 권한을 갖게 됩니다.
