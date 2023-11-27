---
title: 관리자 보안 구성
description: 스토어 관리자에 대한 보안을 구성하는 방법에 대해 알아봅니다.
exl-id: 931fd8ad-96b7-42e5-9c3e-4bb9ca85b1ba
role: Admin
feature: Admin Workspace, Configuration, Security
source-git-commit: e301cfaeec3a8427fff6138ba041bdbd7433c137
workflow-type: tm+mt
source-wordcount: '716'
ht-degree: 0%

---

# 관리자 보안 구성

매장 보안을 보호하기 위해 다각적인 방법을 사용하는 것이 좋습니다. 다음을 사용하여 시작할 수 있습니다. [사용자 지정 관리자 URL](../stores-purchase/store-urls.md#use-a-custom-admin-url) 뻔한 &quot;관리자&quot;나 &quot;백엔드&quot;가 아니라 짐작하기 쉽지 않은 말이다. 기본적으로 다음 작업을 수행하는 데 사용되는 암호가 [로그인](../getting-started/admin-signin.md) 관리자에는 7자 이상이어야 하며 문자와 숫자를 모두 포함해야 합니다. 로서의 [모범 사례](https://experienceleague.adobe.com/docs/commerce-operations/implementation-playbook/best-practices/launch/security-best-practices.html)에서는 문자, 숫자 및 기호의 조합을 포함하는 강력한 관리자 암호만 사용합니다. Adobe Commerce 및 Magento Open Source에서는 계정에 할당된 마지막 4개의 암호를 재사용할 수 없습니다.

관리자 보안 구성을 통해 다음과 같은 기능을 사용할 수 있습니다.

- URL에 비밀 키 추가
- 암호를 대소문자를 구분해야 함
- 관리 세션 길이 제한
- 암호 수명 제한
- 관리자 계정 이전에 시도할 수 있는 로그인 횟수를 제한합니다. [잠김](permissions-users-all.md#locked-users).

보안을 강화하기 위해 현재 세션이 만료되기 전에 키보드 비활성화 시간을 구성하고 사용자 이름과 암호는 대소문자를 구분해야 합니다.

이 섹션의 보안 설정 외에도 [이중 인증](security-two-factor-authentication.md) (2FA)는 앱 또는 장치에서 생성한 일회용 암호로 사용자의 ID를 확인하는 데 필요합니다. Admin에 처음 로그인할 때 2FA를 설정하라는 메시지가 표시됩니다. 보안을 강화하기 위해 관리자 로그인을 구성하여 [CAPTCHA](security-captcha.md).

>[!NOTE]
>
>활성화된 스토어 [!DNL Adobe Identity Management Services] (IMS) 인증에는 기본 Adobe Commerce 및 Magento Open Source 2FA가 비활성화되어 있습니다. Adobe 자격 증명으로 Commerce 인스턴스에 로그인한 관리자는 많은 관리 작업에 대해 다시 인증할 필요가 없습니다. Adobe IMS는 관리자 가 현재 세션에 로그인할 때 인증을 처리합니다. 다음을 참조하십시오 [[!DNL Adobe Identity Management Service] (IMS) 통합 개요](../getting-started/adobe-ims-integration-overview.md).

기술 정보는 다음을 참조하십시오. [보안 개요](https://developer.adobe.com/commerce/php/architecture/basics/security/)개발자 설명서 {:target=&quot;_blank&quot;}.

![관리자 보안](../configuration-reference/advanced/assets/admin-security.png){width="600" zoomable="yes"}

## 관리자 보안 구성

1. 다음에서 _관리자_ 사이드바, 이동 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. 아래의 왼쪽 패널에서 _[!UICONTROL Advanced]_, 선택&#x200B;**[!UICONTROL Admin]**.

1. 확장 ![확장 선택기](../assets/icon-display-expand.png) 다음 **[!UICONTROL Security]** 섹션.

1. 관리자 사용자가 다른 디바이스의 동일한 계정에서 로그인하지 못하도록 하려면 을(를) 설정합니다. **[!UICONTROL Admin Account Sharing]** 끝 `No`.

1. 암호 재설정 요청을 관리하는 데 사용되는 방법을 결정하려면 을 설정합니다. **[!UICONTROL Password Reset Protection Type]** 다음 중 하나를 수행합니다.

   - `By IP and Email` — 통지에서 관리자 계정과 연결된 이메일 주소로 응답이 수신된 후 암호를 온라인으로 재설정할 수 있습니다.
   - `By IP` — 별도의 확인 없이 암호를 온라인으로 재설정할 수 있습니다.
   - `By Email` — 관리자 계정과 연결된 이메일 주소로 전송된 알림에 이메일을 통해서만 암호를 재설정할 수 있습니다.
   - `None` — 암호는 저장소 관리자만 재설정할 수 있습니다.

1. 로그인 보안 옵션을 설정합니다.

   - 대상 **[!UICONTROL Recovery Link Expiration Period (hours)]**, 암호 복구 링크가 유효한 시간(시간)을 입력합니다.

   - 시간당 제출할 수 있는 최대 암호 요청 수를 결정하려면 다음 수를 입력합니다. **[!UICONTROL Max Number of Password Reset Requests]**.

   - 대상 **[!UICONTROL Min Time Between Password Reset Requests]**&#x200B;암호 재설정 요청 사이에 경과해야 하는 최소 시간(분)을 입력합니다.

   - 악용에 대한 예방 조치로 관리자 URL에 비밀 키를 추가하려면 을 설정합니다. **[!UICONTROL Add Secret Key to URLs]** 끝 `Yes`. 이 설정은 기본적으로 활성화되어 있습니다.

   - 입력한 로그인 자격 증명에서 대문자와 소문자를 사용하여 시스템에 저장된 내용과 일치하게 하려면 다음을 설정하십시오. **[!UICONTROL Login is Case Sensitive]** 끝 `Yes`.

   - 시간 초과되기 전의 관리 세션 길이를 확인하려면 다음 기간 동안 세션 기간(초)을 입력합니다. **[!UICONTROL Admin Session Lifetime (seconds)]** 필드. 값은 60초 이상이어야 합니다.

   - 대상 **[!UICONTROL Maximum Login Failures to Lockout Account]**&#x200B;를 클릭하고, 계정이 잠기기 전에 사용자가 관리자에 로그인할 수 있는 횟수를 입력합니다. 기본적으로 6번의 시도가 허용됩니다. 무제한 로그인을 시도하려면 필드를 비워 둡니다.

   - 대상 **[!UICONTROL Lockout Time (minutes)]**&#x200B;최대 시도 횟수를 충족할 때 관리자 계정이 잠기는 시간(분)을 입력합니다.

1. 암호 옵션 설정:

   - 관리자 암호의 수명을 제한하려면 암호가 유효한 일 수를 입력합니다 **[!UICONTROL Password Lifetime (days)]**. 무제한으로 사용하려면 필드를 비워 둡니다.

   - 설정 **[!UICONTROL Password Change]** 다음 중 하나를 수행합니다.

      - `Forced` — 계정 설정 후 관리자 사용자가 암호를 변경해야 합니다.
      - `Recommended` — 관리자 사용자는 계정 설정 후 암호를 변경할 것을 권장합니다.

1. 완료되면 다음을 클릭하십시오. **[!UICONTROL Save Config]**.

## 관리자 암호 요구 사항

기본적으로 관리자 암호는 7자 이상이어야 하며 문자와 숫자를 모두 포함해야 합니다.
