---
title: 새로운 고객 계정 옵션
description: 스토어의 새 고객 계정에 대한 구성 옵션에 대해 알아봅니다.
exl-id: aa19f0e2-ffbe-433d-8bd5-c14700b67b37
feature: Customers, Configuration
source-git-commit: 7de285d4cd1e25ec890f1efff9ea7bdf2f0a9144
workflow-type: tm+mt
source-wordcount: '315'
ht-degree: 0%

---

# 새로운 고객 계정 옵션

다음에서 _[!UICONTROL Create New Account Options]_구성의 섹션에서 기본 계정 옵션은 VAT ID 유효성 검사 및 사용자 정의 통합과 관련된 고급 옵션과 결합됩니다. 다음 지침은 가장 자주 사용되는 옵션만 다룹니다. 자동 고객 그룹 지정에 대한 자세한 내용은 [VAT 검증](../stores-purchase/vat.md).

{{beta-updates}}

![새 계정 만들기 옵션](assets/customer-configuration-create-new-account-options.png){width="600" zoomable="yes"}

## 기본 고객 계정 옵션 설정

1. 다음에서 _관리자_ 사이드바, 이동 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. 왼쪽 패널에서 를 확장합니다. **[!UICONTROL Customers]** 및 선택 **[!UICONTROL Customer Configuration]**.

1. 확장 **[!UICONTROL Create New Account Options]** 섹션:

   ![새 계정 옵션 기본 설정 만들기](../configuration-reference/customers/assets/customer-configuration-create-new-account-options.png){width="600" zoomable="yes"}

1. 상점에서 지원해야 하는 고객 경험에 따라 각 옵션을 설정합니다.

   - 설정 **[!UICONTROL Default Group]** (계정이 생성될 때 새 고객에게 할당된 고객 그룹에 해당).

   - 다음 항목이 있는 경우: _부가 가치세_ 번호 및 이 값을 고객에게 보이도록 설정 **[!UICONTROL Show VAT Number on Storefront]** 끝 `Yes`.

   - 고객에 대한 관리자 주문 생성 중에 고객의 이메일을 요구하려면 다음을 설정합니다. **[!UICONTROL Email is required field for Admin order creation]** 끝 `Yes`.

   - 다음을 입력합니다. **[!UICONTROL Default Email Domain]** 스토어용, 예: `mystore.com`

   - 설정 **[!UICONTROL Default Welcome Email]** (새 고객에게 보낸 환영 전자 메일에 사용되는 템플릿)입니다.

   - 설정 **[!UICONTROL Default Welcome Email without Password]** 아직 암호가 없는 고객 계정을 만들 때 사용되는 템플릿입니다. 예를 들어 관리자로부터 생성된 고객 계정에 아직 암호가 할당되지 않았습니다.

   - 설정 **[!UICONTROL Email Sender]** 시작 이메일을 보낸 사람으로 표시되는 스토어 연락처입니다.

   - 고객이 스토어에서 계정 열기 요청을 확인하도록 하려면 다음을 설정하십시오. **[!UICONTROL Require Emails Confirmation]** 끝 `Yes`. 그런 다음 설정합니다. **[!UICONTROL Confirmation Link Email]** 확인 이메일에 사용되는 템플릿에 적용해야 합니다.

   - 설정 **[!UICONTROL Welcome Email]** 계정이 확인된 후 보내는 환영 메시지에 사용되는 템플릿으로 보냅니다.

     ![VAT가 활성화된 새 계정 옵션 생성](../configuration-reference/customers/assets/customer-configuration-create-new-account-options-vat.png){width="600" zoomable="yes"}

     이 구성 옵션 집합에서 사용할 수 있는 각 옵션에 대한 자세한 내용은 _새 계정 만들기 옵션_ [구성 참조](../configuration-reference/customers/customer-configuration.md).

1. 완료되면 다음을 클릭하십시오. **[!UICONTROL Save Config]**.
