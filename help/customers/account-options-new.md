---
title: 새로운 고객 계정 옵션
description: 스토어의 새 고객 계정에 대한 구성 옵션에 대해 알아봅니다.
exl-id: aa19f0e2-ffbe-433d-8bd5-c14700b67b37
feature: Customers, Configuration
source-git-commit: 06673ccb7eb471d3ddea97218ad525dd2cdcf380
workflow-type: tm+mt
source-wordcount: '368'
ht-degree: 0%

---

# 새로운 고객 계정 옵션

구성의 _[!UICONTROL Create New Account Options]_&#x200B;섹션에서 기본 계정 옵션은 VAT ID 유효성 검사 및 사용자 지정 통합과 관련된 고급 옵션과 결합됩니다. 다음 지침은 가장 자주 사용되는 옵션만 다룹니다. 자동 고객 그룹 할당에 대한 자세한 내용은 [VAT 유효성 검사](../stores-purchase/vat.md)를 참조하세요.

![새 계정 옵션 만들기](assets/customer-configuration-create-new-account-options.png){width="600" zoomable="yes"}

## 기본 고객 계정 옵션 설정

1. _관리자_ 사이드바에서 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**(으)로 이동합니다.

1. 왼쪽 패널에서 **[!UICONTROL Customers]**&#x200B;을(를) 확장하고 **[!UICONTROL Customer Configuration]**&#x200B;을(를) 선택합니다.

1. **[!UICONTROL Create New Account Options]** 섹션을 확장합니다.

   ![새 계정 옵션 기본 설정 만들기](../configuration-reference/customers/assets/customer-configuration-create-new-account-options.png){width="600" zoomable="yes"}

1. 상점에서 지원해야 하는 고객 경험에 따라 각 옵션을 설정합니다.

   - 계정을 만들 때 새 고객에게 할당된 고객 그룹에 **[!UICONTROL Default Group]**&#x200B;을(를) 설정합니다.

   - _부가가치세_ 번호가 있고 고객에게 표시되도록 하려면 **[!UICONTROL Show VAT Number on Storefront]**&#x200B;을(를) `Yes`(으)로 설정하십시오.

   - 고객에 대한 관리자 주문을 만드는 동안 고객의 전자 메일을 요구하려면 **[!UICONTROL Email is required field for Admin order creation]**&#x200B;을(를) `Yes`(으)로 설정하십시오.

   - 스토어의 **[!UICONTROL Default Email Domain]**(예: `mystore.com`) 입력

   - 새 고객에게 보낸 환영 전자 메일에 사용되는 템플릿으로 **[!UICONTROL Default Welcome Email]**&#x200B;을(를) 설정합니다.

   - 고객이 스토어에서 계정 열기 요청을 확인하도록 하려면 **[!UICONTROL Require Emails Confirmation]**&#x200B;을(를) `Yes`(으)로 설정하십시오. 그런 다음 확인 전자 메일에 사용되는 템플릿으로 **[!UICONTROL Confirmation Link Email]**&#x200B;을(를) 설정합니다.

     >[!NOTE]
     >
     >버전 2.4.7부터 고객은 브라우저에 관계없이 이메일 확인 후 계정에 로그인하려면 이메일 및 암호를 다시 입력해야 합니다.

   - 계정을 확인한 후 보내는 환영 메시지에 사용하는 템플릿으로 **[!UICONTROL Welcome Email]**&#x200B;을(를) 설정합니다.

   - 아직 암호가 없는 고객 계정을 만들 때 사용할 서식 파일로 **[!UICONTROL Default Welcome Email without Password]**&#x200B;을(를) 설정합니다. 예를 들어 관리자로부터 생성된 고객 계정에 아직 암호가 할당되지 않았습니다.

   - 환영 전자 메일의 보낸 사람으로 표시되는 스토어 연락처로 **[!UICONTROL Email Sender]**&#x200B;을(를) 설정합니다.

   - 고객이 스토어에서 계정 열기 요청을 확인하도록 하려면 **[!UICONTROL Require Emails Confirmation]**&#x200B;을(를) `Yes`(으)로 설정하십시오. 그런 다음 확인 전자 메일에 사용되는 템플릿으로 **[!UICONTROL Confirmation Link Email]**&#x200B;을(를) 설정합니다.

   ![VAT가 활성화된 새 계정 옵션 만들기](../configuration-reference/customers/assets/customer-configuration-create-new-account-options-vat.png){width="600" zoomable="yes"}

   이 구성 옵션 집합에서 사용할 수 있는 각 옵션에 대한 자세한 내용은 _새 계정 옵션 만들기_ [구성 참조](../configuration-reference/customers/customer-configuration.md)를 참조하십시오.

1. 완료되면 **[!UICONTROL Save Config]**&#x200B;을(를) 클릭합니다.
