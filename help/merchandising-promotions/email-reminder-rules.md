---
title: 이메일 알림 메시지
description: 특정 조건 세트가 충족될 때 고객에게 자동으로 전송될 수 있는 이메일 미리 알림에 대해 알아봅니다.
exl-id: 3293caca-9dd3-4d64-a80c-58c92a9208e5
feature: Merchandising, Communications
source-git-commit: eb0fe395020dbe2e2496aba13d2f5c2bf2d0fc27
workflow-type: tm+mt
source-wordcount: '559'
ht-degree: 0%

---

# 이메일 알림 메시지

{{ee-feature}}

이메일 미리 알림의 목적은 매장을 방문한 사람이 프로모션을 활용하고 구매하도록 장려하기 위한 것입니다. 특정 조건 세트가 충족되면 고객에게 이메일 미리 알림을 자동으로 전송할 수 있습니다. 예를 들어 장바구니 또는 위시리스트에 항목을 추가했지만 아직 구매하지 않은 고객에게 미리 알림을 보낼 수 있습니다. 이메일 미리 알림을 사용하여 고객이 스토어로 돌아가도록 유도하고 [쿠폰 코드](price-rules-cart-coupon.md) 인센티브로. 쿠폰 코드는 각 배치 이메일 미리 알림에 대해 자동으로 생성되어 각 배치와 연관된 오퍼를 제어할 수 있습니다.

이메일 미리 알림은 장바구니가 중단된 후 특정 일 수가 경과하거나 정의하려는 다른 조건에 대해 트리거될 수 있습니다. 일반적인 조건에는 총 장바구니 값, 수량, 장바구니에 있는 항목 등이 포함됩니다.

>[!NOTE]
>
>고객에게 일치하는 포기한 장바구니, 위시리스트 또는 두 가지 조합을 두 개 이상 보유한 경우, 이메일 미리 알림은 해당 고객에 대해 한 번만 트리거됩니다. 동일한 이메일 미리 알림을 다시 트리거하려면 _[!UICONTROL Repeat Schedule]_이메일 간격(일)을 설정할 필드입니다.

![이메일 알림 메시지](./assets/email-reminders.png){width="700" zoomable="yes"}

## 이메일 미리 알림 구성

이메일 미리 알림 규칙은 분, 시간 또는 일별로 일정한 간격으로 전송할 수 있습니다. 이 구성은 일괄적으로 전송되는 이메일 수와 메시지 발신자로 표시되는 스토어 ID를 결정합니다.

1. 다음에서 _관리자_ 사이드바, 이동 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. 왼쪽 패널에서 를 확장합니다. **[!UICONTROL Customers]** 및 선택 **[!UICONTROL Promotions]**.

1. 확장 ![확장 선택기](../assets/icon-display-expand.png) 다음 **[!UICONTROL Automated Email Reminder Rules]** 섹션을 참조하고 다음을 수행합니다.

   ![고객 구성 - 자동화된 이메일 미리 알림 규칙](../configuration-reference/customers/assets/promotions-automated-email-reminder-rules.png){width="600" zoomable="yes"}

   - 설정 **[!UICONTROL Enable Reminder Emails]** 끝 `Yes`.

   - 자동화된 이메일 미리 알림을 평가하는 새 고객을 위한 검사를 실행하는 빈도를 설정하려면 을(를) 설정합니다. **[!UICONTROL Frequency]** 다음 중 하나를 수행합니다.

      - `Minute Intervals`
      - `Hourly`
      - `Daily`

   - 적절한 설정 **[!UICONTROL Interval]**, 를 기반으로 함 _[!UICONTROL Frequency]_설정.

   - 설정 **[!UICONTROL Start Time]** 24시간 시계에 따라 시, 분 및 초로 이메일이 전송됩니다.

   - 일괄적으로 전송할 수 있는 이메일 수를 제한하려면 **[!UICONTROL Maximum Emails per One Run]** 필드.

   - 실패한 이메일을 보내려는 시도가 반복되지 않도록 하려면 **[!UICONTROL Email Send Failure Threshold]** 필드.

   - 설정 **[!UICONTROL Reminder Email Sender]** (으)로 [저장소 연락처](../getting-started/store-details.md#store-email-addresses) 미리 알림 이메일을 보낸 사람으로 표시됩니다.

   이러한 옵션에 대한 자세한 목록은 다음을 참조하십시오. [자동화된 이메일 미리 알림 규칙](../configuration-reference/customers/promotions.md#automated-email-reminder-rules) 다음에서 _구성 참조_.

1. 완료되면 다음을 클릭하십시오. **[!UICONTROL Save Config]**.

## 이메일 미리 알림 템플릿

기본 이메일 미리 알림 템플릿을 사용자 정의하고 다양한 프로모션을 위해 추가 템플릿을 만들 수 있습니다. 이메일 미리 알림에는 메시지에 통합할 수 있는 특정 변수의 선택이 있습니다. 이러한 변수의 정보는 설정한 이메일 미리 알림 규칙과 쿠폰과 연결된 장바구니 가격 규칙에 따라 결정됩니다. 변수 삽입 버튼을 사용하여 변수가 있는 마크업 태그를 템플릿에 삽입할 수 있습니다. 자세한 내용은 다음을 참조하십시오. [이메일](../systems/email-templates.md).

![이메일 미리 알림 미리 보기](./assets/email-reminder-preview-promotion-template.png){width="600" zoomable="yes"}

### 이메일 미리 알림 템플릿 사용자 지정

1. 다음에서 _관리자_ 사이드바, 이동 **[!UICONTROL Marketing]** > _[!UICONTROL Communications]_>**[!UICONTROL Email Templates]**.

1. 클릭 **[!UICONTROL Add New Template]**.

1. 다음에서 **[!UICONTROL Template]** 아래에 나열 `Magento_Reminder`, 을(를) 선택합니다. **[!UICONTROL Promotion Notification/Reminder]** 템플릿.

1. 클릭 **[!UICONTROL Load Template]**.

표준 준수 [지침](../systems/email-template-custom.md) 템플릿을 사용자 정의합니다.

### 이메일 미리 알림 변수

#### 쿠폰 코드

```
{{var coupon.getCode()|escape}}
```

#### 쿠폰 사용 한도

```
{{var coupon.usage_limit|escape}}
```

#### 고객당 쿠폰 사용

```
{{var coupon.usage_per_customer|escape}}
```

#### 고객 계정 URL

```
{{var this.getUrl($store,'customer/account/',[_nosid:1])}}
```

#### 고객 이름

```
{{var customer_data.name|escape}}
```

#### 이메일 바닥글 템플릿

```
{{template config_path="design/email/footer_template"}}
```

#### 이메일 헤더 템플릿

```
{{template config_path="design/email/header_template"}}
```

#### 이메일 로고 이미지 대체

```
{{var logo_alt}}
```

#### 이메일 로고 이미지 URL

```
{{var logo_url}}
```

#### 프로모션 설명

```
{{var promotion_description|escape|nl2br}}
```

#### 프로모션 이름

```
{{var promotion_name|escape}}
```

#### 저장소 이름

```
{{var store.frontend_name}}
```

#### URL 저장

```
{{store url=""}}
```
