---
title: '[!DNL Commerce] 업그레이드'
description: Adobe Commerce 및 Magento Open Source 업그레이드가 카탈로그 및 [!DNL Inventory Management] 구성.
exl-id: ba640b91-0f29-46df-bfd9-1c43433a751f
feature: Inventory, Upgrade
source-git-commit: 4d89212585fa846eb94bf83a640d0358812afbc5
workflow-type: tm+mt
source-wordcount: '721'
ht-degree: 0%

---

# [!DNL Commerce] 업그레이드

이전 릴리스에서 단일 소스 인벤토리를 사용한 경우 이 정보는 기존 카탈로그 및 인벤토리 구성의 새로운 기능 및 변경 사항에 대한 세부 정보를 제공합니다.

[!DNL Inventory Management] Adobe Commerce 및 Magento Open Source의 경우 모든 제품 재고 관리를 개선 및 업데이트하고 새로운 기능을 추가하는 기능, 개선 사항 및 개발자 지원이 포함되어 있습니다. 주문 수량을 출처 및 주문 이행에 대응시키기 위한 출처 선택 알고리즘 및 동시작업 체크아웃을 포함하여 모든 기능을 즉시 사용할 수 있습니다. 웹 사이트, 상점 및 판매자 유형에 따라 추가 재고 및 출처를 생성하고 재고 금액을 지정하는 등의 작업을 수행할 수 있습니다. 자세한 내용은 [Inventory management](introduction.md).

Magento Open Source 2.4.x 또는 Adobe Commerce 2.4.x를 설치할 때 다음과 같은 초기 변경 사항이 발생합니다.

- [Inventory management](enable.md) 는 글로벌 스토어 또는 제품 수준에서 을 활성화합니다. 재고 관리 옵션을 사용하면 재고 수량 추적, 합산 판매 가능 수량 계산, 구매 추적 시 송장 및 선적을 위한 예약 관리를 활성화하거나 비활성화할 수 있습니다. 재고, 주문 및 납품을 관리하기 위해 ERP 및 기타 서드파티 서비스를 사용하려면 이 옵션을 비활성화할 수 있습니다. 자세한 내용은 [!DNL Inventory Management] 아래에 있는 모듈입니다.

- A [기본 소스](sources-manage.md) 및 [기본 재고](stocks-manage.md) 를 시스템에 추가합니다. 이러한 기본값을 비활성화하거나 제거하지 마십시오. [!DNL Commerce] 기존 제품 및 새로 가져온 제품을 이러한 기본값으로 할당합니다.

  >[!IMPORTANT]
  >
  >기본 재고 및 기본 출처는 페이지의 일부이므로 사용하지 않는 것이 좋습니다. `CatalogInventory` 모듈: 이제 더 이상 사용되지 않습니다. 대신 사용자 지정 재고 및 소스를 만들고 사용하는 것이 좋습니다.

   - 재고는 장바구니 및 주문을 추적하기 위한 예약과 함께 집계된 가상 판매 가능 수량을 제공하여 동시 체크아웃을 보장합니다.

   - 카탈로그의 모든 기존 제품이 기본 소스에 할당됩니다. 새 소스를 추가하기 전까지 제품 인터페이스는 변경되지 않습니다. 한 위치의 제품만 출하하는 경우 출처에 대해 다른 차이는 없습니다. 사용자 지정 항목을 만들 수 있습니다. [소스](sources-add.md) 및 [수량 지정](quantities-manage.md) 배송 위치당.

   - 소스를 픽업 위치로 구성하고 [수량 지정](quantities-manage.md) 해당 소스에 대해

   - 웹 사이트가 기본 재고에 할당합니다. 사용자 지정 항목을 만들 수 있습니다. [재고](stocks-add.md) 영업 채널(웹 사이트) 및 소스(위치)를 연결합니다.

- 추가 [구성 옵션](configuration.md) 제품 및 글로벌 스토어에 을 추가합니다. 일부 기존 구성 옵션은 업데이트된 옵션 및 비헤이비어를 받습니다.

   - 아래 수량에 대해 통지를 발송하면 판매 가능 수량에서 공제가 이루어집니다.

   - 재고 부족 임계값은 양수, 0 및 음수 금액을 지원합니다. 미납주문을 사용할 경우 양수는 무시되며 0(또는 무제한)으로 간주됩니다.

   - 미납주문은 영(무한)과 음수를 지원합니다. 사용가능으로 설정된 경우 아래 수량에 대한 통지는 판매 가능 수량에서 공제되지 않습니다.

- 신규 예약은 잠재적 판매를 추적하여 주문이 출하될 때 수량 공제로 전환합니다. 직접 액세스하거나 예약을 만들 수 없습니다. [!DNL Commerce] 주문, 배송 및 대변 메모를 통해 미결 예약을 생성하고 관리합니다.

- [주문 및 배송](shipments.md) 출처 선택 알고리즘을 사용하여 납품을 추천하고 복수 출처의 부분 납품을 지원하여 주문을 이행하는 새로운 기능을 포함합니다.

- 신규 [가져오기/내보내기 기능](inventory-import-export.md) 소스를 대량으로 추가하고, 재고 수량을 업데이트하고, 카탈로그의 모든 SKU에 대해 재고 상태(재고 부족/재고 부족)를 설정할 수 있습니다. 이러한 기능을 사용하면 하나, 선택한 소스 또는 모든 소스를 수정할 수 있습니다.

- 제품 격자 페이지 지원 일괄 처리를 통한 새로운 일괄 옵션 [소스 할당 및 할당 해제](bulk-assignment.md), 및 [재고를 소스로 이전](inventory-transfer.md).

- [!DNL Inventory Management] 는 B2B 카탈로그를 지원합니다. 현재 모든 B2B 제품은 기본 소스 및 기본 재고에 할당되어야 합니다.

## [!DNL Commerce Order Management] 및 [!DNL Inventory Management]

[Commerce Order Management(MCOM)][1] 은(는) 과(와) 호환되지 않습니다. [!DNL Inventory Management]. MCOM 모듈을 설치하면 다음과 같은 모든 인벤토리 관리 기능이 제공됩니다. [!DNL Commerce], 단일 및 다중 소스 관리, 재고, 예약 등을 포함합니다. 다음 [!DNL Inventory Management] 모듈은 기본적으로 비활성화되어 있습니다.

MCOM은 고급 옴니채널 주문 관리, 글로벌 인벤토리 및 다중 소싱, 스토어 투 웨어하우스 이행 및 중앙 집중식 고객 서비스를 위한 광범위한 기능과 서비스를 제공합니다. 전체 기능 목록은 다음을 참조하십시오 [MCOM 기능 목록][2].

[!DNL Inventory Management] 기존 확장 [!DNL Commerce] 처리 중인 주문, 현재고, 재고에 대한 사용 가능한 재고 및 확장 개발을 위한 API를 추적하는 추가 옵션이 있는 기능.

## [!DNL Inventory Management] 모듈

을(를) 비활성화할 수 있습니다. [!DNL Inventory Management] 모듈:

- 현재 Adobe Commerce 또는 Magento Open Source 2.0/2.1/2.2/2.3의 판매자를 업그레이드하고 2.4.x로 마이그레이션하는 속도를 높입니다.

- 사용자 지정 또는 서드파티 인벤토리 및 주문 관리 모듈을 사용합니다.

- 사용 [!DNL Order Management System] 재고 관리용입니다. 현재 커넥터는 을 지원하지 않습니다. [!DNL Inventory Management] 인터페이스. Adobe Commerce 2.4.0으로 업그레이드하는 OMS 판매자의 경우 이러한 모듈을 비활성화해야 합니다.

자세한 내용은 다음을 참조하십시오. [설치 및 업데이트](install-update.md).

[1]: https://omsdocs.magento.com/
[2]: https://omsdocs.magento.com/en/getting-started/feature-list/
