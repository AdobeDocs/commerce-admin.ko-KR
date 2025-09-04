---
title: 위젯
description: 다양한 콘텐츠를 표시하고 스토어의 특정 블록 참조에 배치할 수 있도록 해 주는 코드 조각을 제공하는 위젯에 대해 알아봅니다.
exl-id: 993ba2ca-a8de-4f7e-8cab-7ba7d16eebe7
badgePaas: label="PaaS만" type="Informative" url="https://experienceleague.adobe.com/ko/docs/commerce/user-guides/product-solutions" tooltip="Adobe Commerce 온 클라우드 프로젝트(Adobe 관리 PaaS 인프라) 및 온프레미스 프로젝트에만 적용됩니다."
source-git-commit: 4a3aa2aa32b692341edabd41fdb608e3cff5d8e0
workflow-type: tm+mt
source-wordcount: '634'
ht-degree: 0%

---

# 위젯

위젯은 광범위한 컨텐츠를 표시하고 저장소의 특정 블록 참조에 배치할 수 있도록 해 주는 코드 조각입니다. 많은 위젯이 실시간 동적 데이터를 표시하고 고객이 스토어와 상호 작용할 수 있는 기회를 만듭니다. [위젯 도구]를 사용하면 이미지 및 텍스트가 있는 블록, 대화형 요소 등 스토어의 모든 영역에 위젯을 쉽게 배치할 수 있습니다.

위젯을 사용하여 마케팅 캠페인용 랜딩 페이지를 만들고, 스토어 전체의 특정 위치에 홍보 콘텐츠를 표시할 수 있습니다. 위젯은 외부 검토 시스템, 비디오 채팅, 투표 및 구독 양식에 대한 대화형 요소 및 작업 블록을 추가하거나 태그 클라우드 및 이미지 슬라이더에 대한 탐색 요소를 제공하는 데 사용할 수도 있습니다.

{{$include /help/_includes/directives-caution.md}}

![새 제품 목록 위젯](./assets/storefront-home-page-new-products.png){width="700" zoomable="yes"}

## 위젯 유형

[위젯을 만들기](widget-create.md)할 때 유형을 설정해야 합니다. 이 유형은 위젯의 작동 방식을 결정합니다.

| 유형 | 설명 |
|--- |--- |
| [!UICONTROL CMS Hierarchy Node Link] | 이 옵션을 사용하여 다른 콘텐츠에 통합할 수 있는 페이지 계층의 특정 노드에 대한 링크를 표시합니다. |
| [!UICONTROL CMS Page Link] | 이 옵션을 사용하여 특정 CMS 페이지로 연결되는 사용자 지정 텍스트와 제목을 지정합니다. 링크가 완료되면 콘텐츠 페이지 및 블록에서 사용할 수 있습니다. |
| [!UICONTROL CMS Static Block] | 이 옵션을 사용하여 페이지의 특정 위치에 콘텐츠 블록을 표시합니다. |
| [!UICONTROL Catalog Category Link] | 이 옵션을 사용하여 선택한 카탈로그 범주에 대한 인라인 또는 블록 스타일 링크를 표시합니다. 링크가 완료되면 콘텐츠 페이지 및 블록에서 사용할 수 있습니다. |
| [!UICONTROL Catalog Events Carousel] | 예정된 카탈로그 이벤트 목록을 표시하려면 이 옵션을 사용합니다. |
| [!UICONTROL Catalog New Products List] | 이 옵션을 사용하여 제품 레코드에 지정된 시간 동안 새로 지정된 제품 블록을 표시합니다. |
| [!UICONTROL Catalog Product Link] | 선택한 카탈로그 제품에 대한 인라인 또는 블록 스타일 링크를 표시하려면 이 옵션을 사용합니다. 링크가 완료되면 콘텐츠 페이지 및 블록에서 사용할 수 있습니다. |
| [!UICONTROL Catalog Products List] | 이 옵션을 사용하여 카탈로그의 제품 목록을 표시합니다. |
| [!UICONTROL Dynamic Blocks Rotator] | 이 옵션을 사용하여 단일 동적 블록을 표시하거나 일련의 동적 블록을 임의 순서로 표시하거나 섞어 표시합니다. 동적 블록은 가격 규칙에 의해 트리거되고 특정 페이지 및 위치에 배치되거나 모든 페이지에 나타나도록 구성될 수 있습니다. |
| [!UICONTROL Gift Registry Search] | 이 옵션을 사용하여 쇼핑객에게 이름 또는 레지스트리 ID로 공개 선물 등록기를 검색할 수 있는 기능을 제공합니다. |
| [!UICONTROL Order by SKU] | SKU별 주문은 모든 쇼핑객을 위한 편의로 스토어에 표시하거나 특정 고객 그룹만 사용할 수 있습니다. 구매자는 SKU별 주문 블록에 SKU 및 수량 정보를 직접 입력하거나 고객 계정에서 CSV 파일을 업로드할 수 있습니다. |
| [!UICONTROL Orders and Returns] | 이 옵션을 사용하여 주문 상태를 확인하고 상품을 반품하도록 요청을 제출할 수 있습니다. 위젯은 계정에 로그인하지 않은 게스트 및 고객에게만 표시됩니다. |
| [!UICONTROL Recently Compared Products] | 최근에 비교한 제품 블록을 표시합니다. 포함된 제품 수를 지정하고 목록 또는 제품 그리드로 형식을 지정할 수 있습니다. |
| [!UICONTROL Recently Viewed Products] | 최근에 본 제품 블록을 표시하려면 이 옵션을 사용합니다. 포함된 제품 수를 지정하고 목록 또는 제품 격자로 형식을 지정할 수 있습니다. |
| [!UICONTROL Wish List Search] | 이 옵션을 사용하여 고객에게 위시리스트 소유자의 이름 또는 이메일 주소로 공개적으로 사용 가능한 위시리스트를 검색할 수 있는 기능을 제공합니다. 스토어 고객은 다른 고객에 속한 위시리스트를 찾거나, 이를 보고 제품을 주문하거나, 제품을 자신의 위시리스트에 추가할 수 있습니다. |

{style="table-layout:auto"}

<!-- Last updated from includes: 2022-08-30 15:36:09 -->
