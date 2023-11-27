---
title: 'Inventory management 안내서 [!DNL Inventory Management] 가이드'
description: 다음에 대한 포괄적인 정보 [!DNL Inventory Management] Adobe Commerce 및 Magento Open Source 관리자(마이그레이션 및 구성 포함)
seo-title: Adobe Commerce Inventory Management Guide
seo-description: Describes how to use the [!DNL Inventory Management] module in Adobe Commerce or Magento Open Source.
exl-id: 8013bc13-b057-4ad7-bbed-ee00c2f6e4eb
source-git-commit: 4d89212585fa846eb94bf83a640d0358812afbc5
workflow-type: tm+mt
source-wordcount: '418'
ht-degree: 1%

---

# [!DNL Inventory Management] 안내서 개요

이 안내서는 Adobe Commerce 및 Magento Open Source 관리자를 위한 것입니다. 기능 구성 및 관리를 포함하여 이 모듈 활성화에 대한 자세한 정보를 제공합니다. 그것은 핵심을 기본적으로 이해하는 것이라고 가정한다 [!DNL Commerce] 구성 및 기능.

[!DNL Inventory Management] 에는 관리자를 위한 두 가지 영역이 있습니다.

- 관리자: 이 영역을 사용하여 구성 UI 및 보고에 액세스합니다.
- 명령줄 인터페이스: 이 도구를 사용하여 설치 및 백엔드 구성 작업을 실행합니다.

이 안내서에서는 다음 주제를 다룹니다.

| 제목 | 설명 |
| ------- | ----------- |
| [소개](introduction.md) | 개요 [!DNL Inventory Management] 상거래 스토어에서 실제 인벤토리를 정확하게 반영할 수 있도록 여러 위치의 재고를 관리하는 데 사용할 수 있는 기능입니다. |
| [릴리스 정보](release-notes.md) | 모든 항목에 대한 자세한 내용은 릴리스 정보 를 참조하십시오 [!DNL Inventory Management] 릴리스. |
| 인벤토리 기본 사항 | 인벤토리 관리에 대한 기본 사항을 알아봅니다. [재고 및 소스](sources-stocks.md), [소스 선택 및 예약](selection-reservations.md), [주문 및 예약 상태](order-status.md), 및 [제품 유형](product-types.md) |
| 시작 | 에 대해 알아보기 [!DNL Inventory Management] 모듈 및 Commerce 인스턴스 및 스토어 작업에 맞는 방법: [상거래 업그레이드](migrate.md), [모듈 설치 및 업데이트](install-update.md), [판매자 소싱 유형](merchant-sourcing.md), 및 [소싱 구조 변경](expand-restructure.md) |
| [구성](configuration.md) | 의 구성에 대해 알아보기 [!DNL Inventory Management] 소스 가용성, 상점 제품 및 주문 선적을 결정하는 옵션. |
| [소스 관리](sources-manage.md) | 주문 이행을 위해 제품 재고를 관리하고 배송하는 물리적 위치 또는 서비스를 사용할 수 있는 위치를 소스 및 정의하는 방법에 대해 알아봅니다. |
| [재고 관리](stocks-manage.md) | 재고를 사용하여 판매 채널 소스에 대한 가상 집계된 제품 재고를 나타내는 방법을 알아봅니다. |
| [수량 관리](quantities-manage.md) | 새 제품에 대한 소스 및 수량을 할당하거나 기존 제품을 변경하는 방법에 대해 알아봅니다. |
| [주문 및 배송 관리](shipments.md) | 추가 기능에 대해 알아보기 [!DNL Inventory Management] 선적 프로세스를 통해 재고 수량을 관리하기 위한 기능 및 옵션. |
| [CLI 참조](cli.md) | 에서 제공하는 명령에 대해 알아봅니다. [!DNL Inventory Management] 모듈 을 사용하여 인벤토리 데이터 및 구성 설정을 관리할 수 있습니다. |

{style="table-layout:auto"}

## 개발자 정보

다음을 참조하십시오 [[!DNL Inventory Management]](https://developer.adobe.com/commerce/webapi/rest/inventory/) 모듈 아키텍처, API 및 알고리즘 사용자 지정에 대한 자세한 내용은 개발자 설명서에서 참조하십시오.

## Commerce 설명서

{{docs-links}}

## 문제 해결 및 지원

이 안내서에서 다루지 않는 정보가 필요하거나 질문이 있는 경우 다음 리소스를 사용하십시오.

- [큰 숫자 예약 불일치](https://experienceleague.adobe.com/docs/commerce-knowledge-base/kb/support-tools/patches/v1-0-8/mdva-30112-magento-patch-large-number-reservation-inconsistencies.html)
- [인벤토리 불일치 문제](https://experienceleague.adobe.com/docs/commerce-knowledge-base/kb/support-tools/patches/v1-0-14/mdva-33281-magento-patch-inventory-inconsistency-issues.html)
- [취소선 인벤토리가 &quot;0&quot;에 도달하지 않는 견본](https://experienceleague.adobe.com/docs/commerce-knowledge-base/kb/support-tools/patches/v1-0-17/mdva-34850-swatches-not-strike-through-inventory-reaches-0.html)
- [재고 설치 후 재고 상태가 잘못됨](https://experienceleague.adobe.com/docs/commerce-knowledge-base/kb/troubleshooting/miscellaneous/stock-status-incorrect-after-magento-inventory-install.html)
- [지원 티켓](https://experienceleague.adobe.com/docs/commerce-knowledge-base/kb/help-center-guide/magento-help-center-user-guide.html#submit-ticket)- 추가 지원을 받으려면 티켓을 제출합니다.
