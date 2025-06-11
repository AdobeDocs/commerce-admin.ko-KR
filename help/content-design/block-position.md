---
title: 콘텐츠 블록 배치
description: 코드를 작성하지 않고 페이지의 특정 위치, 심지어 특정 제품이나 카테고리에 블록을 배치합니다
exl-id: cfc9eb2c-19c8-43f1-937d-4162b5011b8a
badgePaas: label="PaaS만" type="Informative" url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="Adobe Commerce 온 클라우드 프로젝트(Adobe 관리 PaaS 인프라) 및 온프레미스 프로젝트에만 적용됩니다."
source-git-commit: 57a913b21f4cbbb4f0800afe13012ff46d578f8e
workflow-type: tm+mt
source-wordcount: '473'
ht-degree: 0%

---

# 콘텐츠 블록 배치

블록의 페이지 레이아웃과 배치를 제어하는 코드는 XML [위젯](widgets.md)에 작성됩니다. 이러한 위젯을 사용하면 코드를 작성하지 않고도 페이지의 특정 위치 및 특정 제품이나 카테고리에 블록을 쉽게 배치할 수 있습니다. 가능한 모든 조합을 기억하기보다는 목록에서 각 옵션을 선택할 수 있습니다.

다음 목록은 일반적으로 블록이 배치되는 페이지 유형별 위치를 설명합니다. 페이지의 영역을 정의하는 방법에 대한 자세한 내용은 [표준 페이지 레이아웃](page-layout.md#standard-page-layouts)을 참조하십시오.

## 카테고리 및 CMS 페이지

| 참조 차단 | 위치 |
|----------|-------- |
| [!UICONTROL Breadcrumbs] | 현재 위치를 링크로 표시하는 많은 페이지 맨 위에 있는 탐색 도구입니다. 이동 경로 참조에 배치된 추가 콘텐츠는 표시되는 경우 이동 경로의 오른쪽에 표시됩니다. |
| [!UICONTROL Left Column] | 콘텐츠가 왼쪽 열에 추가됩니다. |
| [!UICONTROL Main Content Area] | 컨텐츠가 주 컨텐츠 영역에 추가됩니다. |
| [!UICONTROL My Cart Extra Actions] | 고객이 페이지 상단에 있는 장바구니 아이콘을 클릭하면 _장바구니 소계_ 아래에 콘텐츠가 표시됩니다. |
| [!UICONTROL Navigation Bar] | 기본 탐색 모음 아래에 콘텐츠가 표시됩니다. |
| [!UICONTROL Page Bottom] | 콘텐츠가 페이지 하단에 나타납니다. |
| [!UICONTROL Page Footer] | 콘텐츠는 페이지의 바닥글 위에 나타납니다. |
| [!UICONTROL Page Header] | 콘텐츠는 페이지 헤더 아래에 나타납니다. |
| [!UICONTROL Page Top] | 페이지 상단에 콘텐츠가 표시됩니다. |
| [!UICONTROL Right Column] | 오른쪽 열에 콘텐츠가 나타납니다. |
| [!UICONTROL Store Language] | 컨텐츠가 헤더의 왼쪽 위 모서리에 나타납니다. |

{style="table-layout:auto"}

## 제품 페이지

| 참조 차단 | 위치 |
|----------|-------- |
| [!UICONTROL Alert URLs] | 제품 세부 사항 페이지의 제품 제목 아래에 콘텐츠가 표시됩니다. |
| [!UICONTROL Bottom Block Options Wrapper] | 사용자 지정 옵션이 추가되면 _장바구니에 추가_ 단추 아래에 콘텐츠가 표시됩니다. |
| [!UICONTROL Breadcrumbs] | 콘텐츠는 탐색 모음 아래에 표시되는 경로로 링크를 제공하는 탐색 도우미인 탐색 경로의 오른쪽에 나타납니다. |
| [!UICONTROL Info Column Options Wrapper] | 사용자 지정 옵션이 추가되면 콘텐츠가 오른쪽에 나타납니다. 구성 가능한 옵션에도 동일한 위치가 적용됩니다. |
| [!UICONTROL Left Column] | 왼쪽 열 블록 아래에 콘텐츠가 표시됩니다. |
| [!UICONTROL Main Content Area] | 기본 컨텐츠 영역 아래에 컨텐츠가 표시됩니다. |
| [!UICONTROL My Cart Extra Actions] | 고객이 페이지 상단에 있는 장바구니 아이콘을 클릭하면 _장바구니 소계_ 아래에 콘텐츠가 표시됩니다. |
| [!UICONTROL Navigation Bar] | 기본 탐색 모음 아래에 콘텐츠가 표시됩니다. |
| [!UICONTROL Page Bottom] | 콘텐츠가 페이지 하단에 나타납니다. |
| [!UICONTROL Page Footer] | 콘텐츠는 페이지의 바닥글 위에 나타납니다. |
| [!UICONTROL Page Header] | 콘텐츠는 페이지 헤더 아래에 나타납니다. |
| [!UICONTROL Page Top] | 페이지 상단에 콘텐츠가 표시됩니다. |
| [!UICONTROL PayPal Express Checkout (Payflow Edition) Shortcut Wrapper] | PayPal 결제 방법을 사용하는 경우 해당 콘텐츠가 _PayPal 구매_ 단추 아래에 나타납니다. |
| [!UICONTROL PayPal Express Checkout Shortcut Wrapper] | PayPal 결제 방법을 사용하는 경우 해당 콘텐츠가 _PayPal 구매_ 단추 아래에 나타납니다. |
| [!UICONTROL Product Tags List] | 콘텐츠는 제품 태그 표시줄 아래에 나타납니다. |
| [!UICONTROL Product View Extra Hint] | 콘텐츠는 제품의 주요 상위 가격 아래에 표시됩니다. |
| [!UICONTROL Right Column] | 오른쪽 열 블록 아래에 콘텐츠가 표시됩니다. |
| [!UICONTROL Store Language] | 언어 선택기의 오른쪽에 콘텐츠가 나타납니다. |
| [!UICONTROL Tags List Before] | 콘텐츠가 _[!UICONTROL Add Your Tags]_&#x200B;필드 위에 나타납니다. |

{style="table-layout:auto"}
