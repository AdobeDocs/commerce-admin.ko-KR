---
title: '[!UICONTROL Adobe Services] > [!UICONTROL Email Suppression]'
description: Commerce 관리자의 [!UICONTROL Adobe Services] > [!UICONTROL Email Suppression] 페이지에서 구성 설정을 검토합니다.
feature: Configuration, Communications
badgeSaas: label="SaaS만" type="Positive" url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="Adobe Commerce as a Cloud Service 및 Adobe Commerce Optimizer 프로젝트에만 적용됩니다(Adobe 관리 SaaS 인프라)."
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2:
  - id: dac87252-6066-4d6e-a9d2-f6d84c323de7
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2:
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: f4d7033067a99421224ab2159b1b95775e5e949f
workflow-type: tm+mt
source-wordcount: 316
ht-degree: 0%

---

# [!UICONTROL Adobe Services] > [!UICONTROL Email Suppression]

{{config}}

[!UICONTROL Email Suppression]을(를) 사용하면 관리자가 스토어의 나머지 전자 메일에 영향을 주거나 개발자 개입이 필요 없이 특정 범주의 자동화된 시스템 전자 메일을 끌 수 있습니다. 이 기능을 사용하여 특정 알림을 일시적으로 또는 영구적으로 중지합니다(예: 데이터 마이그레이션 중 이메일 주문 또는 마케팅 이메일).

>[!IMPORTANT]
>
>이중 인증 코드 및 관리자 암호 재설정 이메일과 같은 보안 관련 관리자 알림은 이 기능으로 인해 억제되지 않습니다.

이 페이지의 설정은 [스토어 보기](../../getting-started/websites-stores-views.md#scope-settings)에 따라 적용되므로 스토어마다 다른 전자 메일 범주를 표시하지 않을 수 있습니다.

>[!NOTE]
>
>제외를 해제하면 즉시 일반 이메일 게재가 복원되지만 금지 기간 동안 전송된 이메일은 큐에 올라가지 않습니다.

## [!UICONTROL Email Suppression]

![전자 메일 비표시](./assets/email-suppression.png)<!-- zoom -->

| 필드 | [범위](../../getting-started/websites-stores-views.md#scope-settings) | 설명 |
|--- |--- |--- |
| [!UICONTROL Enable Email Suppression] | 스토어 뷰 | 이 기능에 대한 기본 on/off 스위치입니다. `No`(기본값)로 설정하면 이 페이지의 다른 모든 설정이 무시되고 모든 전자 메일이 정상적으로 전송됩니다. |
| [!UICONTROL Disabled Functional Areas] | 스토어 뷰 | 이메일이 제외된 비즈니스 카테고리를 하나 이상 선택합니다. 각 범주에 포함되는 내용은 [비즈니스 범주](#business-categories)를 참조하십시오. |
| [!UICONTROL Disabled Template IDs] | 스토어 뷰 | 범주에 관계없이 개별적으로 표시하지 않도록 쉼표로 구분된 특정 이메일 템플릿 목록(선택 사항)입니다. 템플릿 코드(예: `customer_password_forgot_email_template`) 또는 관리자에서 만든 사용자 지정 템플릿에 대한 숫자 템플릿 ID를 사용하십시오. |

{style="table-layout:auto"}

### 비즈니스 카테고리 {#business-categories}

| 카테고리 | 포함된 일반적인 이메일 |
|--- |--- |
| 고객 계정 | 계정 생성, 암호 재설정, 계정 정보 변경. |
| Order Management | 주문 확인, 송장, 선적, 대변 메모, 주문 취소. |
| 반환(RMA) | 상품 승인 알림을 반환합니다. |
| 체크아웃 및 결제 | 체크아웃 및 링크별 지불 관련 이메일. |
| 마케팅 | 뉴스레터, 제품 알림, 위시리스트 공유, 친구에게 이메일 보내기, 미리 알림, 초대, 선물 등록. |
| 크레딧 및 보상 저장 | 기프트 카드, 보상 포인트, 스토어 크레딧 잔액 변경. |
| B2B | 회사, 협상 가능한 견적 및 구매 발주 통지. |
| 시스템 알림 | 예약된 가져오기, 내보내기 및 연락처 양식 이메일과 같은 작업 알림. |

{style="table-layout:auto"}
