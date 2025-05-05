---
title: 플랫 카탈로그
description: 각 행에 제품이나 범주에 필요한 모든 데이터가 들어 있는 플랫 카탈로그를 만드는 방법에 대해 알아봅니다.
exl-id: f67bd2e0-3902-41eb-b26f-c772a7692cef
source-git-commit: f36925217230e558043078fdc274f5e69c096c1e
workflow-type: tm+mt
source-wordcount: '680'
ht-degree: 0%

---

# 플랫 카탈로그

>[!IMPORTANT]
>
>플랫 카탈로그를 사용하는 것은 더 이상 우수 사례로 권장되지 않습니다. 이 기능을 계속 사용하면 성능 저하 및 기타 인덱싱 문제가 발생하는 것으로 알려져 있습니다. 자세한 설명 및 솔루션은 [도움말 센터](https://experienceleague.adobe.com/docs/commerce-knowledge-base/kb/troubleshooting/miscellaneous/slow-performance-slow-and-long-running-crons.html?lang=ko)에서 확인할 수 있습니다.<br/><br/>영향을 받는 버전에는 다음이 포함됩니다. <br/>- 클라우드 인프라의 Adobe Commerce, 2.3.x 이상<br/>- Adobe Commerce(온-프레미스), 2.3.x 이상<br/>- Magento Open Source, 2.3.x 이상 <br/><br/>릴리스 버전에서는 일부 확장이 플랫 테이블에서만 작동하므로 플랫 테이블을 사용하지 않도록 설정하면 위험이 발생합니다. 플랫 카탈로그 인덱서를 사용하는 확장이 있는 경우 해당 값을 `No`(으)로 설정할 때 이 위험을 알고 있어야 합니다.

Commerce은 일반적으로 EAV(Entity-Attribute-Value) 모델을 기반으로 여러 테이블에 카탈로그 데이터를 저장합니다. 제품 특성은 여러 테이블에 저장되므로 SQL 쿼리는 길고 복잡한 경우가 있습니다.

반면 플랫 카탈로그는 즉시 테이블을 생성합니다. 이때 각 행에는 제품이나 범주에 필요한 모든 데이터가 포함됩니다. 플랫 카탈로그는 매분마다 또는 cron 작업에 따라 자동으로 업데이트됩니다. 플랫 카탈로그 색인화를 통해 카탈로그 및 장바구니 가격 규칙 처리 속도를 높일 수도 있습니다. 최대 50만 SKU의 카탈로그를 일반 카탈로그처럼 빠르게 인덱싱할 수 있습니다.

>[!NOTE]
>
>라이브 스토어에 대해 플랫 카탈로그를 활성화하기 전에 개발 환경에서 구성을 테스트해야 합니다.

## 1단계: 플랫 카탈로그 활성화

1. _관리자_ 사이드바에서 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**(으)로 이동합니다.

1. 왼쪽 패널에서 **[!UICONTROL Catalog]**&#x200B;을(를) 확장하고 아래의 **[!UICONTROL Catalog]**&#x200B;을(를) 선택합니다.

1. _Storefront_ 섹션을 확장하고 다음을 수행합니다.

   - **[!UICONTROL Use Flat Catalog Category]**&#x200B;을(를) `Yes`(으)로 설정합니다. 필요한 경우 **[!UICONTROL Use system value]** 확인란의 선택을 취소하십시오.

   - **[!UICONTROL Use Flat Catalog Product]**&#x200B;을(를) `Yes`(으)로 설정합니다.

   ![기본 카탈로그 구성](./assets/use-flat-catalog.png){width="700" zoomable="yes"}

1. 완료되면 **[!UICONTROL Save Config]**&#x200B;을(를) 클릭합니다.

1. 캐시를 업데이트하라는 메시지가 표시되면 시스템 메시지에서 **[!UICONTROL Cache Management]**&#x200B;을(를) 클릭하고 지침에 따라 캐시를 새로 고칩니다.

## 2단계: 결과 확인

두 가지 방법을 사용하여 결과를 확인할 수 있습니다.

### 방법 1: 단일 제품에 대한 결과 확인

1. _관리자_ 사이드바에서 **[!UICONTROL Catalog]** > **[!UICONTROL Products]**(으)로 이동합니다.

1. 제품을 편집 모드로 엽니다.

1. **[!UICONTROL Name]**&#x200B;의 경우 제품 이름 끝에 `_TEST` 텍스트를 추가하십시오.

1. **[!UICONTROL Save]**&#x200B;을(를) 클릭합니다.

1. 새 브라우저 탭에서 스토어의 홈 페이지로 이동하여 다음을 수행합니다.

   - 편집한 제품을 검색합니다.

   - 탐색을 사용하여 지정된 범주 아래의 제품을 찾습니다.

     필요한 경우 페이지를 새로 고쳐 결과를 확인합니다. 변경 사항은 분 내에 또는 [Cron](../systems/cron.md) 일정에 따라 표시됩니다.

   ![일반 카탈로그가 있는 상점](./assets/storefront-flat-catalog-enabled.png){width="700" zoomable="yes"}

### 방법 2: 범주에 대한 결과 확인

1. _관리자_ 사이드바에서 **[!UICONTROL Catalog]** > **[!UICONTROL Categories]**(으)로 이동합니다.

1. 왼쪽 상단 모서리에서 **[!UICONTROL Store View]**&#x200B;이(가) `All Store Views`(으)로 설정되어 있는지 확인합니다.

   메시지가 표시되면 **[!UICONTROL OK]**&#x200B;을(를) 클릭하여 확인합니다.

1. 범주 트리에서 기존 범주를 선택하고 **[!UICONTROL Add Subcategory]**&#x200B;을(를) 클릭한 후 다음을 수행합니다.

   - **[!UICONTROL Category Name]**&#x200B;에 대해 `Test Category`을(를) 입력하십시오.

   - 완료되면 **[!UICONTROL Save]**&#x200B;을(를) 클릭합니다.

     ![테스트 하위 범주](./assets/catalog-flat-test-category.png){width="600" zoomable="yes"}

   - **[!UICONTROL Products in Category]** 섹션에서 ![확장 선택기](../assets/icon-display-expand.png)를 확장하고 **[!UICONTROL Reset Filter]**&#x200B;을(를) 클릭하여 모든 제품을 표시합니다.

   - 새 카테고리에 추가할 여러 제품의 확인란을 선택합니다.

   - **[!UICONTROL Save]**&#x200B;을(를) 클릭합니다.

   ![범주 제품 테스트](./assets/catalog-flat-test-category-products.png){width="600" zoomable="yes"}

1. 새 브라우저 탭에서 스토어의 홈 페이지로 이동하고 스토어 탐색을 사용하여 만든 범주를 찾습니다.

   필요한 경우 페이지를 새로 고쳐 결과를 확인합니다. 변경 사항은 분 이내 또는 cron 일정에 따라 표시됩니다.

## 3단계: 테스트 데이터 제거

다음을 수행하여 테스트 데이터를 제거하고 원래 제품 이름과 카탈로그 구성을 복원합니다.

### 테스트 범주 제거

1. _관리자_ 사이드바에서 **[!UICONTROL Catalog]** > **[!UICONTROL Categories]**(으)로 이동합니다.

1. 범주 트리에서 생성한 테스트 하위 범주를 선택합니다.

1. 오른쪽 상단에서 **[!UICONTROL Delete]**&#x200B;을(를) 클릭합니다.

1. 확인 메시지가 표시되면 **[!UICONTROL OK]**&#x200B;을(를) 클릭합니다.

   이 범주를 제거해도 범주에 할당된 제품은 제거되지 않습니다.

### 원래 제품 이름 복원

1. _관리자_ 사이드바에서 **[!UICONTROL Catalog]** > **[!UICONTROL Categories]**(으)로 이동합니다.

1. 편집 모드로 테스트 제품을 엽니다.

1. **[!UICONTROL Product Name]**&#x200B;에 추가한 `_TEST` 텍스트를 제거합니다.

1. 오른쪽 상단에서 **[!UICONTROL Save]**&#x200B;을(를) 클릭합니다.

### 원래 카탈로그 구성 복원

1. _관리자_ 사이드바에서 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**(으)로 이동합니다.

1. 왼쪽 패널에서 **[!UICONTROL Catalog]**&#x200B;을(를) 확장하고 아래의 **[!UICONTROL Catalog]**&#x200B;을(를) 선택합니다.

1. _Storefront_ 섹션을 확장하고 다음을 수행합니다.

   - **[!UICONTROL Use Flat Catalog Category]**&#x200B;을(를) `No`(으)로 설정합니다.

   - **[!UICONTROL Use Flat Catalog Product]**&#x200B;을(를) `No`(으)로 설정합니다.

1. 완료되면 **[!UICONTROL Save Config]**&#x200B;을(를) 클릭합니다.

1. 메시지가 표시되면 캐시를 새로 고칩니다.
