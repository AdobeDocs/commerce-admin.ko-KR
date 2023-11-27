---
title: 인벤토리 가져오기 및 내보내기
description: 를 확장하여 기본 가져오기 및 내보내기 기능 사용 [!DNL Inventory Management] sku별로 출처 및 수량을 업데이트하는 옵션.
exl-id: cb2d2e0d-aef8-4b18-b013-9a7b0ab448bd
feature: Inventory, Data Import/Export
source-git-commit: 4d89212585fa846eb94bf83a640d0358812afbc5
workflow-type: tm+mt
source-wordcount: '503'
ht-degree: 0%

---

# 인벤토리 가져오기 및 내보내기

많은 제품이 있는 카탈로그의 경우 확장된 기본 가져오기 및 내보내기 기능을 사용하십시오 [!DNL Inventory Management] sku별로 출처 및 수량을 업데이트하는 옵션. 이러한 옵션을 사용하여 신규 출처를 추가하고 모든 출처 또는 특정 출처에 대한 재고 수량을 갱신할 수 있습니다. 예를 들어 프랑스, 영국 또는 미국의 소스에 대한 제품 정보에 영향을 주지 않고 독일 소스에 대한 제품을 내보낼 수 있습니다.

- [!DNL Commerce] 업그레이드 시 제품에 기본 소스 자동 할당 [!DNL Commerce] 또는 새 제품을 가져오는 중. 사용자 지정 소스가 지정된 제품을 가져오는 경우 기본 소스가 여전히 0의 수량으로 추가됩니다. 출처 및 수량을 갱신하려면 다음 임포트 지시사항을 사용합니다.

- 단일 소스 판매자는 가져오기를 사용하여 제품 수량만 업데이트합니다. 기존 및 추가된 모든 제품이 기본 소스에 지정됩니다.

- 다중 소스 판매자는 가져오기를 사용하여 SKU당 행당 여러 소스 및 수량을 추가합니다.

업데이트를 가져오려면 먼저 특정 소스 또는 모든 소스에 대한 CSV 파일을 내보냅니다. CSV 파일을 편집하고 각 소스 및 수량에 대해 SKU당 행을 추가합니다. 출처를 추가하고 재고의 수량을 추가할 때 출처의 코드가 필요합니다. 가져오기-내보내기 기능을 사용하여 재고를 추가하거나 업데이트할 수 없습니다.

## CSV 파일 콘텐츠

내보내기-가져오기 파일에는 소스에 따라 다음 정보가 포함됩니다.

- `source_code` - 의 소스 코드 [!DNL Commerce]. 각 소스 및 SKU에 대한 행이 있습니다.
- `sku` - 의 제품에 대한 SKU [!DNL Commerce]. SKU는 올바르게 업데이트하려면 스토어의 제품과 일치해야 합니다 [!DNL Inventory Management] 데이터.
- `status` - 0(재고 부족)입니다. 재고 1개. 이 소스에서 주식을 구매하려면 이 값이 1이어야 합니다.
- `quantity` - 이 SKU 및 소스에 사용할 수 있는 총 재고량입니다.

CSV 파일을 사용하여 여러 제품 및 할당된 소스를 빠르게 업데이트하여 애플리케이션 인터페이스를 통해 한 번에 하나씩 업데이트하지 않고 인벤토리 레코드의 부정확성을 모두 업데이트 및 수정합니다. 기본 파일의 경우 먼저 내보내고 필요에 따라 업데이트합니다.

![가져오기 - 인벤토리 데이터 내보내기에 대한 CSV 파일 예](assets/inventory-import-export-data.png){width="600" zoomable="yes"}

## 모든 소스에 대한 제품 데이터 내보내기

1. 다음에서 _관리자_ 사이드바, 이동 **[!UICONTROL System]** > _[!UICONTROL Data Transfer]_>**[!UICONTROL Export]**.

1. 대상 **[!UICONTROL Entity Type]**, 선택 `Stock Sources`.

   내보내기는 SKU가 있는 제품에 대한 데이터만 추출합니다.

1. 클릭 **[!UICONTROL Continue]**.

   이 파일은 를 생성하고 다운로드하여 열고 편집합니다.

재고 금액 및 제품 데이터를 업데이트한 후 파일을 다시 로 가져옵니다. [!DNL Commerce].

![제품 데이터 및 소스에 대한 재고 소스 내보내기](assets/inventory-export-stock-sources.png){width="350" zoomable="yes"}

## 특정 소스에 대한 제품 데이터 내보내기

1. 다음에서 _관리자_ 사이드바, 이동 **[!UICONTROL System]** > _[!UICONTROL Data Transfer]_>**[!UICONTROL Export]**.

1. 대상 **[!UICONTROL Entity Type]**, 선택 `Stock Sources`.

   내보내기는 SKU가 있는 제품에 대한 데이터만 추출합니다.

1. 사용 **[!UICONTROL Entity Attributes]** 특정 소스에 대해 내보낸 제품을 필터링합니다.

   대상 `source_code`를 클릭하고 필터 필드에 소스의 코드를 입력합니다.

1. 클릭 **[!UICONTROL Continue]**.

   이 파일은 를 생성하고 다운로드하여 열고 편집합니다.

재고 금액 및 제품 데이터를 업데이트한 후 파일을 다시 로 가져옵니다. [!DNL Commerce].

## 제품 데이터 가져오기

1. 다음에서 _관리자_ 사이드바, 이동 **[!UICONTROL System]** > _[!UICONTROL Data Transfer]_>**[!UICONTROL Import]**.

1. 대상 **[!UICONTROL Entity Type]**, 선택 `Stock Sources`.

   내보내기는 SKU가 있는 제품에 대한 데이터만 추출합니다.

1. 다음에 대한 구성 선택 **[!UICONTROL Import Behavior]**.

1. 가져올 .csv 파일을 선택하십시오.

1. 클릭 **[!UICONTROL Check Data]** 가져오기를 완료합니다.

![제품 데이터 및 소스 가져오기](assets/inventory-import-sources.png){width="600" zoomable="yes"}
