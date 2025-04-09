---
title: 자동 리디렉션
description: Commerce 스토어에서 제품 또는 카테고리의 URL 키가 변경될 때마다 자동 리디렉션을 생성하도록 구성하는 방법에 대해 알아봅니다.
exl-id: fbde09d3-a1a3-4bac-a850-4c74c99fe714
feature: Categories, Products, Configuration
source-git-commit: d088d5833b9c61e7b1c90a0839fdf38527929ce5
workflow-type: tm+mt
source-wordcount: '542'
ht-degree: 0%

---

# 자동 리디렉션

제품 또는 카테고리의 URL 키가 변경될 때마다 영구 리디렉션을 자동으로 생성하도록 스토어를 구성할 수 있습니다. 검색 엔진 최적화 섹션에서 URL 키 아래의 확인란은 영구 리디렉션이 활성화되었는지 여부를 나타냅니다. 저장소가 이미 카탈로그 URL을 자동으로 리디렉션하도록 구성된 경우 리디렉션은 URL 키에 대한 간단한 업데이트입니다. 자동 리디렉션을 만드는 프로세스는 제품과 카테고리 모두에 대해 동일합니다.

>[!NOTE]
>
>자동 리디렉션이 활성화되어 있고 범주를 저장하면 모든 제품 및 범주 재작성은 실시간으로 생성되고 기본적으로 데이터베이스 테이블에 저장됩니다. 이 경우 많은 지정된 제품이 있는 카테고리의 성능에 큰 문제가 발생할 수 있습니다. 해결 방법은 이 기본값을 변경하고 범주 저장 시 제품에 대한 범주/제품 URL 재작성 생성을 건너뛰는 것입니다. 이 경우 표준 제품 URL에 대해서만 제품 재작성이 생성됩니다.

## 자동 리디렉션 설정

1. _관리자_ 사이드바에서 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**(으)로 이동합니다.

1. 왼쪽 패널에서 **[!UICONTROL Catalog]**&#x200B;을(를) 확장하고 아래의 **[!UICONTROL Catalog]**&#x200B;을(를) 선택합니다.

1. **[!UICONTROL Search Engine Optimization]** 섹션에서 ![확장 선택기](../assets/icon-display-expand.png)를 확장합니다.

   ![카탈로그 구성 - 검색 엔진 최적화](../configuration-reference/catalog/assets/catalog-search-engine-optimization.png){width="600" zoomable="yes"}

1. **[!UICONTROL Create Permanent Redirect for URLs if URL Key Changed]**&#x200B;을(를) `Yes`(으)로 설정합니다.

1. 완료되면 **[!UICONTROL Save Config]**&#x200B;을(를) 클릭합니다.


>[!NOTE]
>
> 스토어 보기 또는 웹 사이트 범위에 대해 URL 재작성을 생성할 수 있습니다. 관리자의 URL 재작성 범위를 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]****[!UICONTROL Catalog]**>**[!UICONTROL Catalog]**>**[!UICONTROL Search Engine Optimization]**로 설정합니다._[!UICONTROL Product URL Rewrite Scope]_ 필드에서 범위를 선택합니다.

## 제품 URL 자동 리디렉션

1. _관리자_ 사이드바에서 **[!UICONTROL Catalog]** > **[!UICONTROL Products]**(으)로 이동합니다.

1. 목록에서 제품을 찾은 다음 를 클릭하여 레코드를 엽니다.

1. **[!UICONTROL Search Engine Optimization]** 섹션에서 ![확장 선택기 ](../assets/icon-display-expand.png)을(를) 확장합니다.

   ![제품 검색 엔진 최적화 - 영구 리디렉션](./assets/product-search-engine-optimization-create-permanent-redirect.png){width="600" zoomable="yes"}

1. **[!UICONTROL URL Key]**&#x200B;의 경우 다음을 수행합니다.

   - **[!UICONTROL Create Permanent Redirect for old URL]** 확인란이 선택되어 있는지 확인하십시오. 그렇지 않으면 지침에 따라 [자동 리디렉션을 사용](url-rewrite.md#configure-url-rewrites)하십시오.

   - 모든 소문자와 이 문자 사이에 공백이 아닌 하이픈을 사용하여 필요에 따라 **[!UICONTROL URL Key]**&#x200B;을(를) 업데이트합니다.

1. 완료되면 **[!UICONTROL Save]**&#x200B;을(를) 클릭합니다.

1. 캐시를 새로 고치라는 메시지가 표시되면 작업 공간 상단에 있는 메시지의 링크를 따르십시오.

   이제 제품 및 관련 범주 URL에 대해 영구 리디렉션이 적용됩니다.

## 자동으로 범주 URL 리디렉션

1. _관리자_ 사이드바에서 **[!UICONTROL Catalog]** > **[!UICONTROL Categories]**(으)로 이동합니다.

1. 트리에서 범주를 찾은 다음 을(를) 클릭하여 레코드를 엽니다.

1. **[!UICONTROL Search Engine Optimization]** 섹션에서 ![확장 선택기](../assets/icon-display-expand.png)를 확장합니다.

1. **[!UICONTROL URL Key]**&#x200B;의 경우 다음을 수행합니다.

   - **[!UICONTROL Create Permanent Redirect for old URL]** 확인란이 선택되어 있는지 확인하십시오. 그렇지 않으면 지침에 따라 [자동 리디렉션을 사용](url-rewrite.md#configure-url-rewrites)하십시오.

   - 모든 소문자와 이 문자 사이에 공백이 아닌 하이픈을 사용하여 필요에 따라 **[!UICONTROL URL Key]**&#x200B;을(를) 업데이트합니다.

1. 완료되면 **[!UICONTROL Save]**&#x200B;을(를) 클릭합니다.

1. 캐시를 새로 고치라는 메시지가 표시되면 작업 공간 상단에 있는 메시지의 링크를 따르십시오.

   이제 범주 및 연결된 제품 URL에 대해 영구 리디렉션이 적용됩니다.

## 범주 저장에 대한 제품 URL 재작성 생성 건너뛰기 {#skip-rewrite}

>[!WARNING]
>
>범주/제품 URL 재쓰기의 자동 생성을 해제하면 복원할 수 없는 기존의 모든 범주/제품 유형 URL 재쓰기가 영구적으로 제거됩니다. 이 경우 해결할 URL 키의 수동 업데이트가 필요한 해결되지 않은 범주/제품 유형 URL 충돌이 발생할 수 있습니다.

1. _관리자_ 사이드바에서 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**(으)로 이동합니다.

1. 왼쪽 패널에서 **[!UICONTROL Catalog]**&#x200B;을(를) 확장하고 아래의 **[!UICONTROL Catalog]**&#x200B;을(를) 선택합니다.

1. **[!UICONTROL Search Engine Optimization]** 섹션에서 ![확장 선택기](../assets/icon-display-expand.png)를 확장합니다.

1. **[!UICONTROL Generate "category/product" URL Rewrites]**&#x200B;을(를) `No`(으)로 설정합니다.

1. 확인 대화 상자에서 **[!UICONTROL OK]**&#x200B;을(를) 클릭하여 변경 및 기존 URL 재작성 제거를 확인합니다.

   ![범주/제품 URL 재작성 끄기 - 확인](./assets/seo-rewrite-off.png){width="350"}

1. 완료되면 **[!UICONTROL Save Config]**&#x200B;을(를) 클릭합니다.
