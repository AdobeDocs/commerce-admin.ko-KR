---
title: 고객 암호 옵션
description: 고객 암호 옵션은 상점의 다양한 고객 대면 기능에 대한 보안 수준을 결정합니다.
exl-id: 84dec8e8-3363-4133-bbcc-9e58467749c4
feature: Customers, Configuration, Security
source-git-commit: ea9eeea0fc5213de2787e0b7ea2aed825ca3a9de
workflow-type: tm+mt
source-wordcount: '394'
ht-degree: 0%

---

# 고객 암호 옵션

고객 암호 옵션은 암호 재설정 요청에 사용되는 보안 수준, 고객 알림에 사용되는 이메일 템플릿 및 암호 복구 링크의 수명을 결정합니다. 고객이 자신의 암호를 변경하도록 허용하거나 스토어 관리자만 그렇게 하도록 요구할 수 있습니다.

## 고객 암호 옵션 구성

1. _관리자_ 사이드바에서 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**(으)로 이동합니다.

1. 왼쪽 패널에서 **[!UICONTROL Customers]**&#x200B;을(를) 확장하고 **[!UICONTROL Customer Configuration]**&#x200B;을(를) 선택합니다.

1. **[!UICONTROL Password Options]** 섹션을 확장합니다.

   ![암호 옵션](../configuration-reference/customers/assets/customer-configuration-password-options.png){width="600" zoomable="yes"}

1. 암호 재설정 요청을 확인하는 데 사용할 메서드로 **[!UICONTROL Password Reset Protection Type]**&#x200B;을(를) 설정하십시오.

   - `By IP and Email` - 특정 전자 메일 또는 특정 IP의 암호를 재설정하려는 이전 시도를 확인합니다.
   - `By IP` - 특정 IP에서 암호를 재설정하려는 이전 시도를 확인합니다.
   - `By Email` - 특정 전자 메일의 암호를 재설정하려는 이전 시도를 확인합니다.
   - `None` - 보호가 비활성화되었습니다(암호 재설정에 대한 제한 없음).

   **[!UICONTROL Max Number of Password Reset Requests]** 및 **[!UICONTROL Min Time Between Password Reset Requests]**&#x200B;은(는) 이 구성을 기반으로 계산됩니다.

1. 시간당 전송되는 암호 재설정 요청 수를 제한하려면 다음을 수행하십시오.

   - **[!UICONTROL Max Number of Password Reset Requests]**&#x200B;에 대해 시간당 전송할 수 있는 최대 암호 재설정 요청 수를 입력하십시오.

   - **[!UICONTROL Min Time Between Password Reset Requests]**&#x200B;에 대해 요청 사이에 경과해야 하는 최소 시간(분)을 입력하십시오.

1. 암호 재설정 이메일 알림을 구성하려면 다음 작업을 수행하십시오.

   - 암호를 잊어버린 고객에게 보내는 전자 메일에 사용되는 템플릿에 **[!UICONTROL Forgot Email Template]**&#x200B;을(를) 설정합니다.

   - 관리자 사용자가 고객 암호를 재설정할 때 사용하는 템플릿으로 **[!UICONTROL Remind Email Template]**&#x200B;을(를) 설정하십시오.

   - 고객이 암호를 변경할 때 사용되는 템플릿에 **[!UICONTROL Reset Password Template]**&#x200B;을(를) 설정합니다.

   - 암호 관련 알림의 발신자로 표시되는 [스토어 연락처](../getting-started/store-details.md)(으)로 **[!UICONTROL Password Template Email Sender]**&#x200B;을(를) 설정합니다.

1. 다음 암호 재설정 보안 옵션을 완료합니다.

   - **[!UICONTROL Recovery Link Expiration Period (hours)]**&#x200B;의 경우 암호 복구 링크가 만료될 때까지 남은 시간을 입력하십시오.

   - 고객 로그인 및 암호 찾기 양식의 필드를 이전 항목에서 자동으로 채우려면 **[!UICONTROL Enable Autocomplete on login/forgot password forms]**&#x200B;을(를) `Yes`(으)로 설정하십시오.

   - **[!UICONTROL Number of Required Character Classes]**&#x200B;의 경우 다음 문자 클래스를 기준으로 암호에 포함해야 하는 여러 문자 유형의 수를 입력합니다.

      - `Lowercase`
      - `Uppercase`
      - `Numeric`
      - `Special Characters`

   - **[!UICONTROL Maximum Login Failures to Lockout Account]**&#x200B;의 경우 고객 계정이 잠길 때까지 실패한 로그인 시도 횟수를 입력합니다. 무제한으로 시도하려면 0(`0`)을 입력하십시오.

   - **[!UICONTROL Minimum Password Length]**&#x200B;의 경우 암호에 사용할 수 있는 최소 문자 수를 입력합니다. 숫자는 0보다 커야 합니다.

   - **[!UICONTROL Lockout Time (minutes)]**&#x200B;의 경우 로그인에 실패한 횟수가 너무 많으면 고객 계정이 잠기는 시간(분)을 입력합니다.

1. 완료되면 **[!UICONTROL Save Config]**&#x200B;을(를) 클릭합니다.
