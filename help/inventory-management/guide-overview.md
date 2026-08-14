---
title: '[!DNL Inventory Management] 안내서'
description: Adobe Commerce 및 Magento Open Source의  [!DNL Inventory Management] 재고, 소스, 수량, 구성, 주문 및 배송에 대한 관리 및 CLI 가이드.
seo-title: Adobe Commerce Inventory Management Guide
seo-description: Describes how to use the [!DNL Inventory Management] module in Adobe Commerce or Magento Open Source.
exl-id: 8013bc13-b057-4ad7-bbed-ee00c2f6e4eb
TQID: https://experienceleague.adobe.com/AFaKjUXrfZOMSYWjcW-dyD9OBMlQj6PkILIQiuT8YJU
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2:
  - id: c1256247-af4b-46d8-9dca-0c654ecfa157
  - id: d1e21356-0064-4f48-9089-16e3f0dbd2a6
  - id: dac87252-6066-4d6e-a9d2-f6d84c323de7
  - id: e8818fe6-9c8b-4bc0-9ef8-377a10b7bc75
  - id: f42e0a1a-0d79-488d-a83f-f2c30672b137
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: f8a45b24-4be7-4f1b-909b-60d06b483a20
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2:
  - id: aa2f3246-cb95-4b30-8899-fdf7d73550cc
  - id: c1579802-ddd4-4214-8a91-97b2066abe11
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: 94e419120b8e16848cc1d449650f023f361a2af7
workflow-type: tm+mt
source-wordcount: 329
ht-degree: 1%

---

# [!DNL Inventory Management] 개요

이 안내서는 Adobe Commerce 및 Magento Open Source의 여러 위치에서 재고를 관리하는 관리자를 위한 것입니다. [!DNL Inventory Management] 모듈에 대한 구성 및 관리 절차를 제공하며 핵심 [!DNL Commerce] 기능에 대한 기본적인 이해를 전제로 합니다.

구성, 보고 및 일상적인 인벤토리 작업에 **관리자**&#x200B;를 사용하십시오. 설치, 업그레이드 및 백엔드 구성에 **명령줄 인터페이스**&#x200B;를 사용하십시오.

이 안내서에서는 다음 주제를 다룹니다.

| 제목 | 설명 |
| ------- | ----------- |
| [소개](introduction.md) | 기능, 용어 및 [!DNL Inventory Management]이(가) 스토어에 맞는 방법입니다. |
| [릴리스 정보](release-notes.md) | 모듈 릴리스 내역 및 알려진 문제 |
| [인벤토리 기본 사항](sources-stocks.md) | [재고 및 소스](sources-stocks.md), [소스 선택 및 예약](selection-reservations.md), [주문 및 예약 상태](order-status.md) 및 [제품 유형](product-types.md)에 대한 개념입니다. |
| 시작하기 | [Commerce 업그레이드](migrate.md), [설치 및 업데이트](install-update.md), [판매자 소싱 유형](merchant-sourcing.md) 및 [인벤토리 재구성](expand-restructure.md). |
| [구성](configuration.md) | 상점 첫 화면 표시 및 배송에 대한 글로벌, 제품 및 알고리즘 설정. |
| [소스 관리](sources-manage.md) | 이행 위치를 생성하고 관리합니다. |
| [재고 관리](stocks-manage.md) | 소스를 판매 채널에 매핑. |
| [수량 관리](quantities-manage.md) | 출처당 제품 수량을 지정 및 갱신합니다. |
| [주문 및 배송 관리](shipments.md) | 주문을 이행하고 재고에서 납품을 관리합니다. |
| [CLI 참조](cli.md) | 명령줄 인벤토리 및 구성 작업. |

{style="table-layout:auto"}

## 개발자 정보

API, 사용자 정의 및 모듈 아키텍처를 위한 고급 리소스에 액세스합니다. API 및 알고리즘 사용자 지정에 대한 기술적인 세부 정보는 REST API 개발자 설명서에서 [[!DNL Inventory Management]](https://developer.adobe.com/commerce/webapi/rest/inventory/)을(를) 참조하십시오.

## Commerce 설명서

Adobe Commerce의 모든 부분에 도움이 되는 판매자, 클라우드 및 개발자 안내서를 찾아보십시오. 이러한 리소스는 모든 설정 또는 관리 요구 사항에 사용합니다.

{{docs-links}}

## 문제 해결 및 지원

지원 문서 및 티켓 시스템을 사용하여 인벤토리 문제를 신속하게 해결할 수 있습니다. 재고 상태 또는 제품 관리에 대한 추가 도움을 받으십시오.

이 안내서에서 다루지 않는 정보가 필요하거나 질문이 있는 경우 다음 리소스를 사용하십시오.

- [재고 설치 후 재고 상태가 잘못됨](https://experienceleague.adobe.com/docs/commerce-knowledge-base/kb/troubleshooting/miscellaneous/stock-status-incorrect-after-magento-inventory-install.html)
- [지원 티켓](https://experienceleague.adobe.com/docs/commerce-knowledge-base/kb/help-center-guide/magento-help-center-user-guide.html#submit-ticket)—추가 지원을 받으려면 티켓을 제출하세요.
