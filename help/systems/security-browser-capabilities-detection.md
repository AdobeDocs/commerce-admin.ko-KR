---
title: 브라우저 기능 감지
description: 고객의 브라우저 설정을 변경해야 하는 경우 브라우저 기능 감지를 구성하고 알림을 표시하는 방법에 대해 알아봅니다.
exl-id: 16caab8b-3ba5-43a1-a6f0-7c1e921be132
role: Admin
feature: Configuration, Security
source-git-commit: 64ccc2d5016e915a554c2253773bb50f4d33d6f4
workflow-type: tm+mt
source-wordcount: '254'
ht-degree: 0%

---

# 브라우저 기능 감지

인터넷에 있는 대부분의 웹 사이트 및 애플리케이션과 마찬가지로, Adobe Commerce 및 Magento Open Source은 방문자의 브라우저가 전체 운영을 위해 쿠키와 JavaScript를 모두 허용해야 합니다. 그러나 경우에 따라 사용자의 브라우저가 쿠키와 JavaScript를 모두 방지하는 가장 높은 개인 정보 보호 설정으로 설정됩니다. 스토어는 각 방문자의 브라우저의 기능을 테스트하고 설정을 변경해야 하는 경우 알림을 표시하도록 구성할 수 있습니다.

- 브라우저의 개인 정보 설정에서 쿠키를 허용하지 않는 경우 쿠키를 로 자동으로 리디렉션하도록 시스템을 구성할 수 있습니다. [쿠키 활성화](../content-design/pages.md#enable-cookies) 페이지: 대부분의 브라우저에서 권장 설정을 만드는 방법을 설명합니다.
- 브라우저의 개인 정보 설정이 JavaScript를 허용하지 않는 경우 모든 페이지의 헤더 위에 다음 메시지를 표시하도록 시스템을 구성할 수 있습니다.

기술 정보는 다음을 참조하십시오. [지원되는 브라우저](https://experienceleague.adobe.com/docs/commerce-operations/installation-guide/system-requirements.html#supported-browsers) 다음에서 _설치 안내서_.

## 브라우저 기능 감지 구성

1. 다음에서 _관리자_ 사이드바, 이동 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. 왼쪽 아래에 있는 패널에서 _[!UICONTROL General]_, 선택&#x200B;**[!UICONTROL Web]**.

1. 확장 ![확장 선택기](../assets/icon-display-expand.png) 다음 **[!UICONTROL Browser Capabilities Detection]** 섹션을 참조하고 다음을 수행합니다.

   - 쿠키를 허용하도록 브라우저를 구성하는 방법을 설명하는 지침을 표시하려면 을 설정합니다. **[!UICONTROL Redirect to CMS-page if Cookies are Disabled]** 끝 `Yes`.

   - 사용자의 브라우저에서 JavaScript가 비활성화되어 있을 때 머리글 위에 배너를 표시하려면 을 설정합니다 **[!UICONTROL Show Notice if JavaScript is Disabled]** 끝 `Yes`.

   - 사용자의 브라우저에서 로컬 저장소가 비활성화되어 있을 때 머리글 위에 배너를 표시하려면 을 설정합니다 **[!UICONTROL Show Notice if Local Storage is Disabled]** 끝 `Yes`.

   ![일반 구성 - 웹 브라우저 기능 감지](../configuration-reference/general/assets/web-browser-capabilities-detection.png){width="600" zoomable="yes"}

1. 완료되면 다음을 클릭하십시오. **[!UICONTROL Save Config]**.
