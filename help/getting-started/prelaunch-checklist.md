---
title: 사전 실행 검사 목록
description: 이 목록을 사용하여 스토어가 프로덕션으로 전환되기 전에 모든 것이 올바른지 확인하는 데 필요한 구성 설정을 확인하십시오.
exl-id: 649809c2-7217-4274-b365-c682bfff24ba
feature: Site Management, System
role: Admin, Leader
source-git-commit: 370131cd73a320b04ee92fa9609cb24ad4c07eca
workflow-type: tm+mt
source-wordcount: '415'
ht-degree: 0%

---

# 사전 실행 검사 목록

스토어의 디자인, 개발 및 테스트를 완료한 후 스토어 전에 다음 구성 설정을 확인하여 모든 것이 올바른지 확인하십시오 _실행_. 모든 구성 설정에 대한 포괄적인 설명은 [_구성 참조_](../configuration-reference/guide-overview.md).

## 일반 설정

- [URL 저장](../stores-purchase/store-urls.md) - 상점 및 관리자의 스토어 URL이 라이브 프로덕션 환경에 맞는지 확인합니다.
- 보안 인증서 - 저장소를 시작하기 전에 기본 URL에 지정된 도메인에 대해 100% 서명되고 신뢰할 수 있는 보안 인증서를 설치합니다.
- [이메일 주소 저장](../getting-started/store-details.md#store-email-addresses) - 새 주문, 송장, 배송, 대변 메모, 제품 가격 알림 및 뉴스레터 등 이메일 알림을 보내고 받는 데 사용되는 모든 이메일 주소를 완료합니다. 각 필드에 올바른 회사 이메일 주소가 포함되어 있는지 확인하십시오.

## 마케팅 설정

- [이메일 템플릿](../systems/email-templates.md) - 브랜드를 반영하도록 기본 이메일 템플릿을 업데이트합니다. 템플릿을 만드는 경우 구성을 업데이트해야 합니다.
- [영업 커뮤니케이션](../stores-purchase/introduction.md#order-management-and-operations) - 송장 및 포장 명세서에 올바른 비즈니스 정보가 포함되어 있는지 확인하고 브랜드를 반영하십시오.
- [Google 도구](../merchandising-promotions/google-tools.md) - [!DNL Commerce] 에서는 Google API와 통합하여 귀사에서 Google Analytics 및 Google AdWords를 사용할 수 있도록 합니다.

## 판매 설정

- [장바구니 옵션](../stores-purchase/cart-configuration.md) - 장바구니 구성 설정을 확인하여 장바구니에 최소 주문 금액 및 가격 수명 설정과 같이 변경할 사항이 있는지 확인합니다.
- [체크아웃 옵션](../stores-purchase/checkout-process.md#checkout-options) - 체크아웃 옵션에서 약관 설정, 게스트 체크아웃 구성 등과 같이 변경할 사항이 있는지 확인합니다.
- [세금](../stores-purchase/taxes.md) - 영업세 규칙 및 현지 요구 사항에 따라 세금이 올바르게 구성되었는지 확인하십시오.
- [게재 방법](../stores-purchase/delivery.md) - 회사에서 사용할 모든 통신사 및 배송 방법을 활성화합니다.
- [PayPal](../stores-purchase/paypal.md) - 고객에게 PayPal 결제 편의를 제공하려면 PayPal 가맹점 계정을 열고 결제 방법을 설정합니다. 저장소가 라이브로 전환되기 전에 샌드박스 모드에서 일부 테스트 트랜잭션을 실행합니다.
- [결제 방법](../stores-purchase/payments.md) - 사용할 결제 방법을 활성화하고 올바르게 구성되었는지 확인합니다. 주문 상태 설정, 허용된 통화, 허용된 국가 등을 확인합니다.

## 시스템 설정

[크론(예약된 작업)](../systems/cron.md) - Cron 작업은 이메일, 카탈로그 가격 규칙, 뉴스레터, 고객 알림, Google 사이트맵, 환율 업데이트 등을 처리하는 데 사용됩니다. Cron 작업이 적절한 시간 간격(분)으로 실행되도록 설정되어 있는지 확인하십시오.
