---
title: ' [!DNL Inventory Management] 소개'
description: ' [!DNL Inventory Management] for [!DNL Commerce] 을(를) 사용하여 원본 및 재고 전체에 걸쳐 인벤토리를 관리하고, 판매 가능한 수량을 계산하고, 예약을 추적하고, 주문 이행을 지원하는 방법에 대해 알아봅니다. 관리자 를 사용하여 설정을 구성하고 보고서를 생성하며 설정 및 배경 변경을 위한 명령줄 인터페이스를 사용할 수 있습니다.'
exl-id: 6a7dd27e-248f-4c40-b2db-0d70529422a1
TQID: https://experienceleague.adobe.com/7v-G-DZEki7y-4HSmq-rJxsmu6vih26jRYYCRRUF-XY
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2:
  - id: c1256247-af4b-46d8-9dca-0c654ecfa157
  - id: dac87252-6066-4d6e-a9d2-f6d84c323de7
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: f8a45b24-4be7-4f1b-909b-60d06b483a20
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2:
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: 125a49f740639bce0ced8063074ca43d627c0eac
workflow-type: tm+mt
source-wordcount: 371
ht-degree: 0%

---

# [!DNL Inventory Management] 소개

[!DNL Commerce]에 대한 [!DNL Inventory Management]은(는) 판매자가 하나 이상의 웹 사이트와 실제 또는 가상 제품 위치에서 인벤토리를 관리할 수 있도록 지원합니다. 또한 관리 및 명령줄 인터페이스에 재고 구성, 현재고 및 총 판매 가능 수량 추적, 체크아웃 중 재고 보호 및 주문 이행 지원을 위한 도구를 제공합니다. 창고, 저장소, 픽업 위치, 직송자 및 기타 이행 위치를 포함하는 단일 소스 또는 다중 소스 네트워크에 [!DNL Inventory Management]을(를) 사용할 수 있습니다.

## [!DNL Inventory Management]을(를) 사용하는 방법

- **관리자:** 인벤토리 옵션을 설정하고 인벤토리 보고서를 생성합니다.
- **명령줄 인터페이스:** 설치 명령을 실행하고 백그라운드에서 인벤토리 변경 내용을 적용합니다.
- **구성 범위:** 인벤토리 설정을 전체적으로, 소스별로 또는 제품별로 구성합니다.

## 주요 기능

[!DNL Inventory Management] 기능은 다음과 같습니다.

- 단일 출처 또는 여러 출처에서 재고가 발생한 판매자에 대한 다양한 구성
- 지정된 출처에서 총괄 판매 수량을 추적하기 위한 재고
- 동시 체크아웃 보호
- 거리 또는 우선 순위에 따라 이행 권장 사항을 지원하는 선적 일치 알고리즘

>[!NOTE]
>
>이러한 기능은 커뮤니티 엔지니어링 프로그램을 통해 [Inventory management](https://github.com/magento/inventory)&#x200B;(이전 MSI) 프로젝트의 일부로 개발되었습니다.<br/>
>
>[!DNL Inventory Management] 모듈은 기본적으로 모든 기능이 활성화된 Magento Open Source 및 Adobe Commerce과 함께 설치됩니다. 모듈 릴리스에 포함된 변경 사항에 대한 자세한 내용은 [릴리스 정보](release-notes.md)를 참조하세요.

## 기본 용어

[!DNL Inventory Management]&#x200B;(으)로 작업할 때 다음 용어를 이해하는 것이 중요합니다.

[!UICONTROL Sources]은(는) 사용 가능한 제품을 저장하고 발송하는 실제 위치를 나타냅니다. 예제와 다이어그램은 [재고 및 원본](sources-stocks.md)을 참조하세요. (모든 위치를 가상 제품의 소스로 지정할 수 있습니다.)

[!UICONTROL Stocks] 판매 채널(현재 웹 사이트로 제한됨)을 원본 위치 및 현재고에 매핑합니다. 한 개의 스톡을 여러 판매 채널에 매핑할 수 있지만 한 개의 스톡에만 판매 채널을 할당할 수 있습니다.

[!UICONTROL Aggregate Salable Quantity]은(는) 판매 채널을 통해 판매할 수 있는 총 가상 재고입니다. 이 금액은 재고에 지정된 모든 출처에서 계산됩니다.

[!UICONTROL Reservations]은(는) 고객이 장바구니에 제품을 추가하고 체크아웃을 완료할 때 판매 가능 수량에서 공제를 추적합니다. 주문이 출하될 때, 예약은 특정 출처 재고 수량에서 출하 금액을 정산하고 공제합니다.
