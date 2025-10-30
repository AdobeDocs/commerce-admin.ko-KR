---
title: 운송 회사 설정
description: 상점에 사용할 수 있는 상업용 배송 계정에 대한 지원에 대해 알아보십시오.
exl-id: b6098068-12f3-4223-b216-98055a802b19
feature: Shipping/Delivery
source-git-commit: d5beff4d450dab21f74e5baec6b718b844963858
workflow-type: tm+mt
source-wordcount: '468'
ht-degree: 0%

---

# 운송 회사 설정

지원되는 이동통신사에 상업용 계정이 있는 경우 고객이 체크아웃 중에 해당 이동통신사를 선택할 수 있는 편의를 제공할 수 있습니다. 요금은 자동으로 다운로드되므로 정보를 조회할 필요가 없습니다.

>[!NOTE]
>
>Commerce 설치에 대한 추가 배송 서비스는 [Commerce Marketplace](../getting-started/commerce-marketplace.md)을(를) 참조하십시오.

고객에게 다양한 운송 회사를 제공하기 전에 다음 단계를 완료해야 합니다.

- 스토어의 원본 지점을 설정하려면 [배송 설정](shipping-settings.md)을 구성하세요.

- 제공할 각 통신사 서비스에 대한 설정을 구성합니다.

   - [**UPS**](ups.md) - UPS(United Parcel Service)는 220개 이상의 국가에 육상 및 항공으로 국내 및 국제 배송 서비스를 제공합니다.
   - [**USPS**](usps.md) - 미국 우편 서비스(USPS)는 미국 정부의 독립 우편 서비스입니다. USPS는 육로와 항공으로 국내 및 국제 배송 서비스를 제공합니다.
   - [**FedEx**](fedex.md) - FedEx는 220개 이상의 국가에 육로 및 항공으로 국내 및 국제 배송 서비스를 제공합니다.
   - [**DHL**](dhl.md) - DHL은 편지, 물품, 정보의 관리 및 전송을 위한 통합 국제 서비스와 맞춤형 고객 중심 솔루션을 제공합니다.

## 차원 가중치

체적 중량이라고도 불리는 치수 중량은 중량과 포장 부피의 조합에 따라 운송 가격을 결정하는 일반적인 업계 관행입니다. 단순하게 보면, 치수 중량은 운송인의 화물 영역에서 패키지가 차지하는 공간의 양을 기준으로 운임을 결정한다. 치수 중량은 일반적으로 패키지가 그 체적에 비해 상대적으로 가벼운 경우에 사용된다.

모든 주요 운송업체는 일부 배송에 치수 가중치를 적용합니다. 그러나 차원 가중치 적용 방식은 통신사마다 다르다. 귀사의 출하량이 많다면, 1년 동안 운송료의 약간의 차이는 수천 달러로 환산될 수 있습니다.

## 구성

구성 옵션은 통신사마다 다릅니다. 그러나 모두 다음 단계가 필요합니다.

1. 운송회사와 운송 계정을 개설합니다.

1. 계정 번호 또는 사용자 ID와 시스템에 대한 게이트웨이 URL을 스토어 구성에 입력합니다.

### USPS Web Tools API 사용 중단

Adobe Commerce 버전 2.4.6, 2.4.7 및 2.4.8에서는 기존 Web Tools API를 사용하여 USPS와 즉시 통합이 가능합니다. USPS는 기존 Web Tools API를 대체하는 REST 기반 플랫폼인 USPS API를 도입했습니다.

USPS는 2026년 1월 25일에 기존 Web Tools API를 중단합니다. 이 날짜 이후에 Web Tools API에 대한 모든 요청이 실패합니다.

USPS 배송 서비스의 중단을 방지하려면 2026년 1월 25일 전에 다음 작업을 수행하십시오.

- [USPS REST API 마이그레이션 품질 패치](https://experienceleague.adobe.com/docs/commerce-knowledge-base/kb/troubleshooting/known-issues-patches-attached/usps-rest-api-migration-patch.html)&#x200B;(AC-1520)를 적용하여 USPS REST API와 통합에 대한 지원을 추가하십시오.

- REST API를 사용하도록 Commerce USPS 구성을 업데이트합니다.

   - [USPS 배송 회사 구성](usps.md)

   - [배송 레이블 구성](shipping-label-create.md)

