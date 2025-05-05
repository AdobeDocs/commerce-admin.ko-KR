---
title: Visual Merchandiser 개요
description: 제품을 포지셔닝하고 범주 목록에 표시되는 제품을 결정할 수 있도록 해 주는 Visual Merchandiser 도구에 대해 알아봅니다.
exl-id: 00fe8b7f-0c33-4f06-a3cd-1f0bd18079f1
feature: Categories, Merchandising, Products
badgePaas: label="PaaS만" type="Informative" url="https://experienceleague.adobe.com/ko/docs/commerce/user-guides/product-solutions" tooltip="Adobe Commerce 온 클라우드 프로젝트(Adobe 관리 PaaS 인프라) 및 온프레미스 프로젝트에만 적용됩니다."
source-git-commit: 6d782e3aafa7460a0e0d5ca07a2bde2ae371a9ea
workflow-type: tm+mt
source-wordcount: '382'
ht-degree: 0%

---

# Visual Merchandiser

{{ee-feature}}

_시각적 머천다이저_&#x200B;는 제품을 배치하고 범주 목록에 표시되는 제품을 결정하는 조건을 적용할 수 있는 고급 도구 세트입니다. 그 결과 카탈로그의 변경 사항에 맞게 조정되는 제품을 동적으로 선택할 수 있습니다. 각 제품을 격자에 타일로 표시하는 _시각적 모드_&#x200B;에서 작업하거나 범주의 제품 목록에서 작업할 수 있습니다. 각 모드에서 동일한 도구를 사용할 수 있으며 오른쪽 위 모서리에 있는 버튼을 사용하여 각 디스플레이 유형 간에 전환할 수 있습니다.

타일 보기의 ![범주 제품](./assets/category-products-visual-with-stock.png){width="600" zoomable="yes"}

## Visual Merchandiser 액세스

1. _관리자_ 사이드바에서 **[!UICONTROL Catalog]** > **[!UICONTROL Categories]**(으)로 이동합니다.

1. 범주 트리를 드릴다운하고 편집할 범주를 클릭합니다.

1. 아래로 스크롤하여 **[!UICONTROL Products in Category]** 섹션에서 ![확장 선택기](../assets/icon-display-expand.png)를 확장합니다.

1. _타일로 보기_( ![타일로 보기](../assets/icon-view-tiles.png) ) 단추를 클릭하여 제품을 눈금으로 표시합니다.

1. 완료되면 **[!UICONTROL Save Category]**&#x200B;을(를) 클릭합니다.

## 제품 위치 변경

1. 이동할 제품을 보려면 [정렬 순서](../catalog/navigation-product-listings.md)를 사용하십시오.

   - **메서드 1: 끌어서 놓기**

     제품 타일의 오른쪽 위 모서리에서 _Drag_(![Drag 아이콘](../assets/icon-move.png)) 컨트롤을 가져와서 제품을 제위치에 놓습니다. 새로운 포지션을 반영하기 위해 제품별 개수가 조정된다.

   - **메서드 2: 위치 값 설정**

     제품 타일의 _위치_ 컨트롤러(![위치 필드](../assets/control-position.png))에 제품을 표시할 번호를 입력하십시오. `0`을(를) 입력하여 제품을 목록의 맨 위에 배치합니다.

1. 완료되면 **[!UICONTROL Save Category]**&#x200B;을(를) 클릭합니다.

>[!NOTE]
>
>깔끔한 설치에서 Adobe Commerce은 기본 저장소의 루트 카탈로그에 대해 범주 ID `2`을(를) 예약합니다. Visual Merchandiser는 ID 번호가 `3` 이상인 카테고리만 사용할 수 있습니다.

## Workspace 컨트롤

| 제어 | 설명 |
|--- |--- |
| ![목록 보기 아이콘](../assets/icon-view-list.png) | 목록으로 보기 |
| ![타일로 보기 아이콘](../assets/icon-view-tiles.png) | 타일로 보기 |
| ![규칙별 일치 토글 - 아니요](../assets/toggle-no.png) | 규칙별 일치 - 아니요 |
| ![규칙별 일치 토글 - 예](../assets/toggle-yes.png) | 규칙별 일치 - 예 |
| ![이동 아이콘](../assets/icon-move.png) | 드래그 |
| ![위치 컨트롤러](../assets/control-position.png) | 위치 |
| ![범주 아이콘에서 제거](../assets/icon-delete-x.png) | 범주에서 제거 |
| ![페이지 컨트롤당 항목 수](../assets/control-items-per-page.png) | 페이지당 보기 |
| ![페이지 표시 변경](../assets/control-page-display.png) | 다음/이전으로 이동 |

{style="table-layout:auto"}
