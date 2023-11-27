---
title: 이메일 커뮤니케이션 구성
description: 반환된 이메일 라우팅 또는 특정 이메일 주소에 대한 회신을 포함하여 이메일 통신을 구성하는 방법에 대해 알아봅니다.
exl-id: 7e62e9c5-f214-4fd5-becc-99dcb093cd5c
feature: Communications, Configuration
source-git-commit: 64ccc2d5016e915a554c2253773bb50f4d33d6f4
workflow-type: tm+mt
source-wordcount: '310'
ht-degree: 0%

---

# 이메일 커뮤니케이션 구성

다음 _메일 전송 설정_ 반환된 이메일을 라우팅하거나 특정 주소로 이메일에 회신할 수 있습니다. 저장소가 SMTP 또는 Windows 서버에서 실행 중인 경우 호스트 및 포트 설정을 확인할 수 있습니다.

>[!IMPORTANT]
>
>**보안 알림** 모든 판매자는 최근에 식별된 잠재적인 원격 코드 실행 악용으로부터 보호하기 위해 메일 전송 구성을 즉시 설정해야 합니다. 이 문제가 해결될 때까지 사용을 피하는 것이 좋습니다 [!DNL Sendmail] 이메일 통신용. 다음에서 _[!UICONTROL Mail Sending Settings]_, 다음을 확인합니다._[!UICONTROL Set Return Path]_ 이(가) (으)로 설정됨 `No`.

구성 설정에 대한 자세한 목록이 필요하면 를 참조하십시오. [_[!UICONTROL Mail Sending Settings]_](../configuration-reference/advanced/system.md) 다음에서 _구성 참조_.

## 이메일 커뮤니케이션 구성

1. 다음에서 _관리자_ 사이드바, 이동 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. 왼쪽 패널에서 를 확장합니다. **[!UICONTROL Advanced]** 및 선택 **[!UICONTROL System]**.

1. 확장 ![확장 선택기](../assets/icon-display-expand.png) 다음 **[!UICONTROL Mail Sending Settings]** 섹션을 참조하고 다음을 수행합니다.

   ![고급 구성 - 메일 전송 설정](../configuration-reference/advanced/assets/system-mail-sending-settings.png){width="600" zoomable="yes"}

   - 필요한 경우 다음을 설정합니다. **[!UICONTROL Disable Email Communications]** 끝 `No`.

   - 대상 **[!UICONTROL Transport]**&#x200B;저장소에서 전자 메일 통신에 대한 전송 유형을 선택합니다. `Sendmail` 또는 `SMTP`

   - SMTP 또는 Windows 서버에서 실행 중인 경우 다음 설정을 확인하십시오.

      - **[!UICONTROL Host]** - `localhost` 또는 기타

      - **[!UICONTROL Port (25)]** - `25` 또는 기타

   - 대상 **[!UICONTROL Set Return Path]**, 다음 옵션 중 하나를 선택합니다.

      - `No` - (권장 보안 조치) 루트가 기본 스토어 이메일 주소로 이메일을 반환했습니다.
      - `Yes` - 루트가 기본 스토어 이메일 주소로 이메일을 반환했습니다.
      - `Specified` - 경로에 지정된 이메일 주소로 반송됨 **[!UICONTROL Return Path Email]**.

   - SMTP 서버에서 실행 중인 경우 연결을 구성합니다.

      - **[!UICONTROL Username]** - SMTP 서버의 로그인 사용자 이름을 입력합니다.
      - **[!UICONTROL Password]** - SMTP 서버 로그인의 암호를 입력합니다.
      - **[!UICONTROL Auth]** - SMTP 서버 연결에 대한 인증 유형 선택: `NONE` , `PLAIN`, 또는 `LOGIN`
      - **[!UICONTROL SSL]** - 서버 보안 인증서에 대한 확인 유형을 선택합니다. `SSL` 또는 `TLS`

     ![고급 구성 - 메일 전송 설정](../configuration-reference/advanced/assets/system-mail-sending-settings-smtp.png){width="600" zoomable="yes"}

1. 왼쪽 패널에서 를 확장합니다. **[!UICONTROL Sales]** 및 선택 **[!UICONTROL Sales Emails]**.

1. 확장 ![확장 선택기](../assets/icon-display-expand.png) 다음 **[!UICONTROL General Settings]** 섹션.

1. 설정 **[!UICONTROL Asynchronous sending]** 끝 `Enable`.

   ![판매 구성 - 이메일 일반 설정](../configuration-reference/sales/assets/sales-emails-general-settings.png){width="600" zoomable="yes"}

   구성 설정에 대한 자세한 목록이 필요하면 를 참조하십시오. [_일반 설정_](../configuration-reference/sales/sales-emails.md) 다음에서 _구성 참조_.

1. 완료되면 다음을 클릭하십시오. **[!UICONTROL Save Config]**.
