---
title: 견적 템플릿 사용 사례 및 워크플로
description: 기존 견적에서 견적 템플리트를 생성하여 반복 주문에 대한 견적 협상을 간소화합니다.
feature: B2B, Quotes
source-git-commit: 3000d9abab467a86e37c7eca6e7db16b39c763ab
workflow-type: tm+mt
source-wordcount: '970'
ht-degree: 0%

---


# 견적 템플릿 사용 사례 및 워크플로

Quote Template 기능을 통해 구매자와 판매자는 재사용 및 사용자 지정 가능한 Quote Template 을 작성하여 Quote 프로세스를 간소화할 수 있습니다.

- **사용자 지정 가능한 견적** - 구매자는 사전 승인된 템플릿에서 연결된 견적을 생성하여 라인 항목 수량 및 선택 사항과 같은 지정된 매개 변수 내에서 사용자 지정할 수 있습니다.
- **주문 임계값**—판매자는 최소 및 최대 주문 약정을 설정하여 구매자가 합의된 구매 수량을 준수하도록 할 수 있습니다.
- **만료 날짜**—지정한 기간 내에서만 약관을 적용할 수 있도록 템플릿에 유효 기간이 있을 수 있습니다.
- **할인 및 가격책정**- 판매자는 동일한 라인 항목, 견적 레벨 및 납품가 할인 기능을 견적과 함께 사용하여 반복 주문에 대한 할인을 설정할 수 있으므로 협상 프로세스를 단순화할 수 있습니다.
- **추적 및 보고**—시스템에서 템플릿에서 생성된 연결된 견적 수를 추적하고 주문을 성공적으로 완료하여 합의된 주문 할당량의 이행에 대한 통찰력을 제공합니다.

## 사용 사례

회사 구매자는 견적 템플리트를 사용하여 일정 기간 동안 특정 제품 세트를 주문할 수 있습니다. 구매자는 다음과 같은 견적 템플리트 옵션을 구성하여 견적 프로세스를 보다 효율적이고 일관적이며 전략적 구매 계약에 맞게 만듭니다.

- 주문 임계값 - 협상된 가격책정에 적합한 최소 및 최대 주문 수를 지정합니다. 계약 계약에 지정된 주문 할당량을 적용하고 추적하는 데 사용할 수 있습니다.

- 수량 임계값(최소/최대 수량) 템플리트는 수량 임계값을 지정하여 각 주문에 대해 구매할 수 있는 최소 및 최대 수량을 설정하여 판매자가 재고 레벨을 효과적으로 관리할 수 있도록 하는 동시에 구매자가 필요에 따라 수량을 조정할 수 있는 유연성을 제공합니다.

## 견적 템플릿 워크플로

견적 템플리트는 구매자나 판매자가 시작할 수 있습니다.

**1단계: 견적 템플릿 만들기(신규)**

- **구매자가 견적 템플릿을 만듭니다**

  기존 견적 템플리트를 검토할 때 구매자는 회사가 향후 1년 동안 여러 개의 주문을 제출해야 한다고 판단하고, 재구매를 기준으로 추가 할인을 요청하려고 합니다. 견적에 대해 *[!UICONTROL Create quote template]* 액션을 사용하여 견적 템플릿을 만듭니다. 그런 다음 새 템플릿을 판매자에게 전송하여 검토를 시작하여 협상을 시작합니다.

  구매자는 상점 첫 화면의 *[!UICONTROL My Quote Templates]** 페이지에서 직접 견적 템플릿을 만들 수도 있습니다.

- **영업 담당자** — 영업 담당자는 특정 회사 구매자를 대신하여 책임자로부터 견적 템플릿을 만들 수 있습니다. 영업 사원은 기존 견적 또는 [!UICONTROL Quote Templates] 그리드에서 관리자의 견적 템플릿을 만들어 `draft`(으)로 저장하거나 구매자에게 보내 협상을 시작할 수 있습니다. 초안 상태에서 견적은 판매자에게만 표시됩니다. 견적이 전송되면 상태는 `Submitted`입니다. 구매자가 반송하기 전까지는 판매자가 수정할 수 없습니다.

  ![판매자가 관리자의 견적 그리드에서 구매자 견적을 시작하는 중](./assets/quote-template-create-from-grid.png){width="700" zoomable="yes"}

**2단계: 견적 검토 및 협상(검토)**

견적 템플리트 검토 또는 협상에는 수량 변경, 품목 제거, 라인 품목 주석 추가, 라인 품목 또는 견적 할인 적용(판매자), 운송 주소 추가(구매자) 등이 포함될 수 있습니다.

- **판매자가 요청을 보고 응답을 보냅니다** - 관리자의 경우 판매자는 *[!UICONTROL Quote Templates]** 그리드에서 견적 템플릿을 보거나 이메일 알림의 링크에서 견적 템플릿을 엽니다. 상점 첫 화면에서 견적의 상태가 `Pending`(으)로 변경되며 구매자는 변경할 수 없습니다. [견적 협상](quote-price-negotiation.md)에 대해 동일한 프로세스를 수행하면 판매자는 가격 할인을 제공하고 필요에 따라 수량과 품목을 조정하여 응답하고 설명을 입력한 다음 구매자에게 견적을 다시 보냅니다. 구매자와 영업 사원은 판매자가 응답한 것을 이메일로 통보받는다.

- **구매자가 판매자의 견적 템플릿을 보고 응답을 보냅니다** - 구매자가 이메일 알림의 링크를 클릭하여 견적 템플릿을 열거나 계정 대시보드의 _내 견적 템플릿_ 페이지에서 견적을 엽니다. 구매자는 라인 품목이나 견적 레벨에서 판매자에게 메모를 남겨두고 수량을 변경하고 품목을 제거할 수 있습니다.

구매자와 판매자는 계약에 도달하거나 판매자가 견적 템플리트를 거부할 때까지 협상 프로세스를 계속합니다. 구매자가 견적을 변경할 경우(제품 추가 또는 제거 또는 제품 수량 변경), 견적을 판매자에게 반환하여 검토해야 합니다.

- **구매자가 배송 주소를 추가합니다** - 견적 템플릿에 배송 주소가 없는 경우 구매자가 이를 추가해야 합니다. 구매자가 주소를 추가한 후에 판매자는 배송 및 배송 옵션을 제공할 수 있습니다. 표시되는 배송 방법은 Storefront 구성에 따라 다릅니다.

구매자가 운송 주소를 추가할 경우, 협상 계약을 검토해야 하며, 판매자는 계약에 도달하거나 판매자가 견적 템플리트를 거부하기 전까지 협상 프로세스를 계속할 수 있습니다.

**3단계: 구매자가 견적 템플릿 수락**

구매자는 협상된 조건을 템플릿에서 수락합니다. 견적 템플리트가 수락되면 구매자는 이를 사용하여 추가 협상 없이 주문을 실행하는 데 사용할 수 있는 사전 승인된 연결 견적을 생성할 수 있습니다.

체크아웃 시 배송 옵션이 잠겨 있습니다.

### 견적 템플리트 조회

1. 레코드에 대한 **[!UICONTROL Actions]** 열에서 **[!UICONTROL View]**&#x200B;을(를) 클릭합니다.

1. 고객 요청에 응답하려면 지침에 따라 협상 견적에 사용된 것과 동일한 [가격 협상](quote-price-negotiation.md) 프로세스를 시작합니다.

### 견적 템플릿 활동 보기

[!UICONTROL Comments] 및 [!UICONTROL History Log]에서 협상 타임라인, 통신 및 기타 견적 활동을 확인합니다. 여기에는 상태 변경, 고객 및 배송 정보에 대한 업데이트, 품목 및 가격 업데이트 및 기타 중요한 정보가 포함됩니다.

1. 견적 템플리트를 엽니다.

1. **[!UICONTROL Negotiation]**(으)로 스크롤하고 **[!UICONTROL Comments]** 및 **[!UICONTROL History Log]**&#x200B;을(를) 선택하여 견적 협상 설명 및 내역을 봅니다.

   ![내역 보기](./assets/quote-view-history.png){width="400"}

1. 내역은 라인 항목 레벨에서도 추적됩니다.

   ![라인 항목 기록 보기](./assets/quote-view-line-item-history.png){width="400"}


### 견적 템플릿 거부

`In Review` 상태의 견적 템플릿만 거부할 수 있습니다.

1. *[!UICONTROL Quote Templates]* 그리드에서 거절할 견적 템플릿을 엽니다.

1. 견적 템플릿에서 **[!UICONTROL Decline]**&#x200B;을(를) 클릭합니다.

1. 메시지가 표시되면 견적이 거절된 이유를 입력하고 **[!UICONTROL Confirm]**&#x200B;을(를) 클릭합니다.