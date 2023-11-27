---
title: Inventory management 소개
description: 사용 방법 알아보기 [!DNL Inventory Management] 여러 위치의 재고를 관리하여 [!DNL Commerce] 저장은 총실사를 정확하게 반영합니다.
exl-id: 6a7dd27e-248f-4c40-b2db-0d70529422a1
source-git-commit: 4d89212585fa846eb94bf83a640d0358812afbc5
workflow-type: tm+mt
source-wordcount: '363'
ht-degree: 0%

---

# Inventory management 소개

[!DNL Inventory Management] 대상 [!DNL Commerce] 는 제품 인벤토리를 관리하는 도구를 제공합니다. 단일 상점을 여러 창고, 상점, 픽업 위치, 직송 업체 등에 보유한 판매자는 이러한 기능을 사용하여 판매 수량을 유지하고 납품을 처리하여 주문을 완료할 수 있습니다. 재고 수량을 추적하고, 모든 웹 사이트에 대해 고객에게 정확한 판매 가능 재고 금액을 제공하고, 거리 또는 우선순위에 따라 권장 사항에 따라 배송할 수 있습니다. 또한 모든 스토어 및 제품에 대해 전역적으로(모든 스토어 및 제품에 대해), 소스별로, 제품별로 선호하는 제품 구성을 구성할 수 있습니다. 이러한 기능은 비즈니스와 함께 확장되므로 단일 웨어하우스 또는 몇 가지 추가 설정을 통해 복잡한 배송 네트워크에서 작업할 수 있습니다.

[!DNL Inventory Management] 기능은 다음과 같습니다.

- 단일 출처 및 여러 출처에서 재고를 생성하는 판매자에 대한 다양한 구성
- 지정된 출처를 통해 사용 가능한 총괄 수량을 추적하기 위한 재고
- 동시 체크아웃 보호
- 선적 일치 알고리즘

>[!NOTE]
>
>이러한 기능은 의 일부로 개발되었습니다 [Inventory management](https://github.com/magento/inventory) (이전의 MSI) Community Engineering 프로그램을 통한 프로젝트.<br/>
>
>다음 [!DNL Inventory Management] 모듈은 기본적으로 모든 기능이 활성화된 Magento Open Source 및 Adobe Commerce과 함께 설치됩니다. 모듈 릴리스에 포함된 변경 사항에 대한 자세한 내용은 [릴리스 정보](release-notes.md).

## 기본 용어

작업하는 동안 다음 용어를 이해하는 것이 중요합니다 [!DNL Inventory Management]:

[!UICONTROL **소스**] 사용 가능한 제품을 저장 및 발송하는 물리적 위치를 나타냅니다. 이러한 위치에는 창고, 오프라인 매장, 물류 센터 및 직송인이 포함될 수 있습니다. (모든 위치를 가상 제품의 소스로 지정할 수 있습니다.)

[!UICONTROL **재고**] 소스 위치 및 현재고에 판매 채널(현재 웹 사이트로 제한됨)을 매핑합니다. 한 개의 스톡을 여러 판매 채널에 매핑할 수 있지만 한 개의 스톡에만 판매 채널을 할당할 수 있습니다.

[!UICONTROL **총 판매 가능 수량**] 은 판매 채널을 통해 판매할 수 있는 총 가상 재고입니다. 이 금액은 재고에 지정된 모든 출처에서 계산됩니다.

[!UICONTROL **예약**] 고객이 장바구니에 제품을 추가하고 체크아웃을 완료할 때 판매 가능 수량에서 공제를 추적합니다. 주문이 출하될 때, 예약은 특정 출처 재고 수량에서 출하 금액을 정산하고 공제합니다.
