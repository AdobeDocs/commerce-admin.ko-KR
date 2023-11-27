---
title: 선물 등록
description: 고객이 선택한 제품을 선물로 구매하도록 친구와 가족을 초대할 수 있을 때 선물 등록기가 판매를 촉진하는 방법에 대해 알아봅니다.
exl-id: 2e5e3d52-e93e-444c-88a1-1eaa7f178b99
feature: Marketing Tools, Gift, Storefront
source-git-commit: eb0fe395020dbe2e2496aba13d2f5c2bf2d0fc27
workflow-type: tm+mt
source-wordcount: '379'
ht-degree: 0%

---

# 선물 등록

{{ee-feature}}

Adobe Commerce은 고객에게 특별한 경우에 사용할 선물 등록기를 만들고, 친구 및 가족이 선물 등록기에서 선물을 구입하도록 초대할 수 있는 기능을 제공합니다. Adobe Commerce은 구매한 항목과 남은 수량을 추적합니다.

![예제 storefront - 아기 선물 등록](./assets/storefront-gift-registry-create-baby-info.png){width="700" zoomable="yes"}

선물 레지스트리 소유자는 자신의 제품에서 레지스트리에 제품을 추가할 수 있습니다. [고객 대시보드](gift-registry-storefront.md#gift-registry-information). 또 위시리스트나 장바구니에서 상품 이전이 가능하다. 스토어 관리자는 고객 선물 등록기를 보고 공유할 수 있습니다. 또한 고객의 장바구니에서 항목을 추가하거나, 수량을 업데이트하거나, 선물 레지스트리를 삭제하는 등 유지 관리를 수행할 수 있습니다.

선물 레지스트리에 액세스하려면 수신자는 받은 이메일의 링크를 클릭하거나 수신자의 이름, 이메일 또는 선물 레지스트리 ID로 검색할 수 있습니다. 위치는 테마별로 다를 수 있지만 대부분의 스토어에서 각 페이지의 바닥글에 선물 등록에 대한 링크가 있습니다. 또한 [위젯](../content-design/widgets.md) 도구를 사용하여 위치를 지정할 수 있습니다. [선물 등록 검색](gift-registry-search.md) 가게 어디든지.

구매를 원하는 레지스트리 방문자는 선물 레지스트리에서 직접 장바구니에 품목을 추가할 수 있습니다. 주문이 이루어지면 선물 등록부가 업데이트되어 구매를 반영합니다.

## 선물 등록 워크플로우

1. **스토어에 대한 선물 레지스트리 구성**. 저장소 관리자 [선물 레지스트리를 활성화합니다](gift-registry-configure.md), 및 [레지스트리 유형 및 속성을 설정합니다.](gift-registry-create.md).

1. **고객이 직접 레지스트리 생성**. A [고객이 선물 레지스트리를 만듭니다.](gift-registry-storefront.md#create-a-new-gift-registry) 은(는) 가게 계정에서 예정된 기회를 제공하며 선물 레지스트리의 각 섹션에 있는 필수 필드를 완료합니다. 레지스트리에 항목을 추가 한 후 친구 및 가족과 공유 할 수 있습니다.

1. **고객이 레지스트리를 공유함**. 각 구성 요소에는 선물 등록부에 대한 링크가 포함되어 있습니다 [초대](gift-registry-storefront.md#share-a-gift-registry). If [선물 등록 검색](gift-registry-search.md) 은(는) 스토어에서 사용할 수 있으며, 고객은 이름, 이메일 주소 또는 선물 등록 ID별로 특정 선물 등록기를 검색할 수 있습니다.

1. **초대 수신자의 주문**. 초대장 또는 등록부에 대한 정보를 받은 사람은 선물 등록부에서 직접 어떤 물건이든 주문할 수 있다. 항목이 판매되면 Adobe Commerce은 선물 레지스트리 항목 수를 업데이트하고 선물 레지스트리 소유자에게 알립니다.
