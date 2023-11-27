---
title: 세션 관리
description: 관리 및 상점 보안을 위해 세션 관리를 구성하는 방법에 대해 알아봅니다.
exl-id: ad954218-aa3e-44e6-b23f-008de7fc7543
role: Admin
feature: Configuration, Security
source-git-commit: 64ccc2d5016e915a554c2253773bb50f4d33d6f4
workflow-type: tm+mt
source-wordcount: '846'
ht-degree: 0%

---

# 세션 관리

[세션 관리](https://cheatsheetseries.owasp.org/cheatsheets/Session_Management_Cheat_Sheet.html) 는 API 보안을 위한 DoS(서비스 거부 방지) 모범 사례입니다. 세션은 방문자가 사이트에서 보낸 시간을 나타내며 관리자 또는 고객이 계정에 로그인한 시간과 관련이 없습니다.

세션은 동일한 사용자와 연관된 네트워크 HTTP 요청 및 응답 트랜잭션의 시퀀스입니다. 이는 클라이언트(관리자)가 서버에 액세스할 때 해당 데이터와 연결하는 방법입니다. 세션은 액세스 권한 및 현지화 설정과 같은 변수를 설정하는 데 사용됩니다. 이러한 변수는 세션 중에 사용자가 웹 애플리케이션과 갖는 모든 상호 작용에 적용됩니다.

## 세션 크기

다음 구성 설정을 사용하여 관리자 사용자 및 상점 방문자의 최대 세션 크기를 제한하십시오.

- **[!UICONTROL Max Session Size in Admin]**—최대 세션 크기를 바이트 단위로 제한합니다. 사용 `0` 비활성화합니다.
- **[!UICONTROL Max Session Size in Storefront]**—최대 세션 크기를 바이트 단위로 제한합니다. 사용 `0` 비활성화합니다.

>[!TIP]
>
>두 설정 모두 바이트 단위로 측정되며 기본값은 입니다. `256000` 바이트(또는 256KB).

**_최대 세션 크기를 구성하려면 다음을 수행합니다._**

1. 다음에서 _관리자_ 사이드바, 이동 **[!UICONTROL Stores]**  > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. 왼쪽 패널에서 를 확장합니다. **[!UICONTROL Advanced]** 및 선택 **[!UICONTROL System]**.

1. 확장 ![확장 선택기](../assets/icon-display-expand.png) 다음 **[!UICONTROL Security]** 세션 설정에 액세스하기 위한 섹션입니다.

   ![세션 설정](../configuration-reference/advanced/assets/system-security.png){width="600" zoomable="yes"}

1. 새 세션 크기를 바이트 단위로 입력하십시오.

   >[!WARNING]
   >
   >값을 너무 낮게 설정하면 문제가 발생할 수 있습니다. 기본값(256000바이트) 아래에 있는 옵션 중 하나를 설정하면 경고 메시지가 표시됩니다. 다음을 클릭: **[!UICONTROL No]**&#x200B;로 설정하면 값이 로 변경됩니다. `256000`.

1. 클릭 **[!UICONTROL Save Config]**.

### 관리 세션

최대 세션 크기를 초과하면 오류 메시지가 표시되고 시스템은 세션 크기 제한을 `var/log` 디렉토리.

세션 크기를 너무 낮게 설정한 후 관리자에 대한 액세스 권한을 잃을 경우 CLI를 사용하여 구성을 재설정하십시오.

```bash
bin/magento config:set system/security/max_session_size_admin 256000
```

### Storefront 세션

최대 세션 크기를 초과하면 오류가 표시되지 않지만 시스템은 세션 크기 제한을 `var/log` 디렉토리.

## 세션 유효성 검사

Adobe Commerce 및 Magento Open Source을 사용하면 가능한 세션 고정 공격이나 사용자 세션을 포이즌 또는 납치하려는 시도에 대한 보호 조치로 세션 변수의 유효성을 확인할 수 있습니다. 세션 유효성 검사 설정은 각 저장소 방문 동안 세션 변수의 유효성 검사 방법과 세션 ID가 저장소의 URL에 포함되어 있는지 여부를 결정합니다.

기술 정보는 다음을 참조하십시오. [세션 스토리지에 Redis 사용](https://experienceleague.adobe.com/docs/commerce-operations/configuration-guide/cache/redis/redis-session.html) 다음에서 _구성 안내서_.

![일반 구성 - 웹 세션 유효성 검사](../configuration-reference/general/assets/web-session-validation-settings.png){width="600" zoomable="yes"}

유효성 검사는 유효성 검사 변수의 값을 에 저장된 세션 데이터와 비교하여 방문자가 자신이 말한 사람인지 확인합니다 `$_SESSION` 사용자의 데이터입니다. 정보가 예상대로 전송되지 않고 해당 변수가 비어 있으면 유효성 검사가 실패합니다. 세션 유효성 검사 설정에 따라 세션 변수가 유효성 검사 프로세스에 실패하면 클라이언트 세션이 즉시 종료됩니다.

모든 유효성 검사 변수를 활성화하면 공격을 방지하는 데 도움이 될 수 있지만, 서버 성능에도 영향을 줄 수 있습니다. 기본적으로 모든 세션 변수 유효성 검사는 비활성화되어 있습니다. 설정을 실험하여 Adobe Commerce 또는 Magento Open Source 설치에 가장 적합한 조합을 찾는 것이 좋습니다. 모든 유효성 검사 변수를 활성화하면 너무 제한적일 수 있으며, 프록시 서버를 통하거나 방화벽 뒤에서 시작되는 인터넷 연결을 사용하는 고객에 대한 액세스가 차단될 수 있습니다. 세션 변수 및 그 사용에 대한 자세한 내용은 Linux® 시스템의 시스템 관리 설명서를 참조하십시오.

**_세션 유효성 검사를 구성하려면 다음을 수행합니다._**

1. 다음에서 _관리자_ 사이드바, 이동  **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. 왼쪽 패널에서 를 확장합니다. _[!UICONTROL General]_및 선택&#x200B;**[!UICONTROL Web]**.

1. 확장 ![확장 선택기](../assets/icon-display-expand.png) 다음 **[!UICONTROL Session Validation Settings]** 섹션.

1. 각 구성 옵션을 설정합니다.

   - **[!UICONTROL Validate REMOTE_ADDR]** — 다음으로 설정 `Yes` 요청의 IP 주소가 `$_SESSION` 변수를 채우는 방법에 따라 페이지를 순서대로 표시합니다.

   - **[!UICONTROL Validate HTTP_VIA]** — 다음으로 설정 `Yes` 들어오는 요청의 프록시 주소가 `$_SESSION` 변수를 채우는 방법에 따라 페이지를 순서대로 표시합니다.

   - **[!UICONTROL Validate HTTP_X_FORWARDED_FOR]** — 다음으로 설정 `Yes` 요청의 forwarded-for 주소가 `$_SESSION` 변수를 채우는 방법에 따라 페이지를 순서대로 표시합니다.

   - **[!UICONTROL Validate HTTP_USER_AGENT]** — 다음으로 설정 `Yes` 세션 중에 저장소에 액세스하는 데 사용되는 브라우저 또는 장치가 `$_SESSION` 변수를 채우는 방법에 따라 페이지를 순서대로 표시합니다.

1. 완료되면 다음을 클릭하십시오. **[!UICONTROL Save Config]**.

## 관리 세션 수명

보안 조치로서 _관리자_ 는 처음에 키보드 활동이 없는 상태로 900초(15분) 후에 시간 초과로 설정됩니다. 작업 스타일에 맞게 세션 수명을 조정할 수 있습니다.

**_관리 세션 수명을 조정하려면 다음을 수행하십시오._**

1. 다음에서 _관리자_ 사이드바, 이동 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. 아래로 스크롤하고 확장합니다. **[!UICONTROL Advanced]** 왼쪽 패널에서

1. 클릭 **[!UICONTROL Admin]**.

1. 확장 ![확장 선택기](../assets/icon-display-expand.png) 다음 _[!UICONTROL Security]_섹션.

1. 대상 **[!UICONTROL Admin Session Lifetime (seconds)]**&#x200B;세션이 시간 초과되기 전에 활성 상태로 유지되는 시간(초)을 입력합니다.

   ![고급 구성 - 관리자 보안 설정](../configuration-reference/advanced/assets/admin-security.png){width="600" zoomable="yes"}

1. 완료되면 다음을 클릭하십시오. **[!UICONTROL Save Config]**.## 관리자 세션 수명

보안 조치로서 _관리자_ 는 처음에 키보드 활동이 없는 상태로 900초(15분) 후에 시간 초과로 설정됩니다. 작업 스타일에 맞게 세션 수명을 조정할 수 있습니다.

**_관리 세션 수명을 조정하려면 다음을 수행하십시오._**

1. 다음에서 _관리자_ 사이드바, 이동 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. 아래로 스크롤하고 확장합니다. **[!UICONTROL Advanced]** 왼쪽 패널에서

1. 클릭 **[!UICONTROL Admin]**.

1. 확장 ![확장 선택기](../assets/icon-display-expand.png) 다음 _보안_ 섹션.

1. 대상 **[!UICONTROL Admin Session Lifetime (seconds)]**&#x200B;세션이 시간 초과되기 전에 활성 상태로 유지되는 시간(초)을 입력합니다.

   ![고급 구성 - 관리자 보안 설정](../configuration-reference/advanced/assets/admin-security.png){width="600" zoomable="yes"}

1. 완료되면 다음을 클릭하십시오. **[!UICONTROL Save Config]**.
