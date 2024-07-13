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

_메일 전송 설정_&#x200B;을 통해 반환된 전자 메일 또는 전자 메일에 회신하는 기능을 특정 주소로 라우팅할 수 있습니다. 저장소가 SMTP 또는 Windows 서버에서 실행 중인 경우 호스트 및 포트 설정을 확인할 수 있습니다.

>[!IMPORTANT]
>
>**보안 알림** 모든 판매자는 최근에 식별된 잠재적인 원격 코드 실행 악용으로부터 보호하기 위해 메일 전송 구성을 즉시 설정해야 합니다. 이 문제가 해결될 때까지 전자 메일 통신에 [!DNL Sendmail]을(를) 사용하지 않는 것이 좋습니다. _[!UICONTROL Mail Sending Settings]_에서_[!UICONTROL Set Return Path]_&#x200B;이(가) `No`(으)로 설정되어 있는지 확인하십시오.

구성 설정의 자세한 목록을 보려면 _구성 참조_&#x200B;의 [_[!UICONTROL Mail Sending Settings]_](../configuration-reference/advanced/system.md)을(를) 참조하십시오.

## 이메일 커뮤니케이션 구성

1. _관리자_ 사이드바에서 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**(으)로 이동합니다.

1. 왼쪽 패널에서 **[!UICONTROL Advanced]**&#x200B;을(를) 확장하고 **[!UICONTROL System]**&#x200B;을(를) 선택합니다.

1. **[!UICONTROL Mail Sending Settings]** 섹션에서 ![확장 선택기](../assets/icon-display-expand.png)를 확장하고 다음을 수행합니다.

   ![고급 구성 - 메일 전송 설정](../configuration-reference/advanced/assets/system-mail-sending-settings.png){width="600" zoomable="yes"}

   - 필요한 경우 **[!UICONTROL Disable Email Communications]**&#x200B;을(를) `No`(으)로 설정합니다.

   - **[!UICONTROL Transport]**&#x200B;의 경우 스토어에서 전자 메일 통신에 대한 전송 형식을 선택하십시오. `Sendmail` 또는 `SMTP`

   - SMTP 또는 Windows 서버에서 실행 중인 경우 다음 설정을 확인하십시오.

      - **[!UICONTROL Host]** - `localhost` 또는 기타

      - **[!UICONTROL Port (25)]** - `25` 또는 기타

   - **[!UICONTROL Set Return Path]**&#x200B;의 경우 다음 옵션 중 하나를 선택하십시오.

      - `No` - (권장 보안 조치) 경로에서 기본 스토어 이메일 주소로 이메일을 반환했습니다.
      - `Yes` - 경로가 기본 스토어 전자 메일 주소로 전자 메일을 반환했습니다.
      - `Specified` - 경로가 **[!UICONTROL Return Path Email]**&#x200B;에 지정된 전자 메일 주소로 전자 메일을 반환했습니다.

   - SMTP 서버에서 실행 중인 경우 연결을 구성합니다.

      - **[!UICONTROL Username]** - SMTP 서버의 로그인 사용자 이름을 입력합니다.
      - **[!UICONTROL Password]** - SMTP 서버 로그인의 암호를 입력합니다.
      - **[!UICONTROL Auth]** - SMTP 서버 연결에 대한 인증 유형 선택: `NONE`, `PLAIN` 또는 `LOGIN`
      - **[!UICONTROL SSL]** - 서버 보안 인증서에 대한 확인 유형 선택: `SSL` 또는 `TLS`

     ![고급 구성 - 메일 전송 설정](../configuration-reference/advanced/assets/system-mail-sending-settings-smtp.png){width="600" zoomable="yes"}

1. 왼쪽 패널에서 **[!UICONTROL Sales]**&#x200B;을(를) 확장하고 **[!UICONTROL Sales Emails]**&#x200B;을(를) 선택합니다.

1. **[!UICONTROL General Settings]** 섹션에서 ![확장 선택기](../assets/icon-display-expand.png)를 확장합니다.

1. **[!UICONTROL Asynchronous sending]**&#x200B;을(를) `Enable`(으)로 설정합니다.

   ![판매 구성 - 전자 메일 일반 설정](../configuration-reference/sales/assets/sales-emails-general-settings.png){width="600" zoomable="yes"}

   구성 설정의 자세한 목록을 보려면 _구성 참조_&#x200B;에서 [_일반 설정_](../configuration-reference/sales/sales-emails.md)&#x200B;을 참조하십시오.

1. 완료되면 **[!UICONTROL Save Config]**&#x200B;을(를) 클릭합니다.
