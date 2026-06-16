---
title: 브라우저 기능 감지
description: 고객의 브라우저 설정을 변경해야 하는 경우 브라우저 기능 감지를 구성하고 알림을 표시하는 방법에 대해 알아봅니다.
exl-id: 16caab8b-3ba5-43a1-a6f0-7c1e921be132
role: Admin
feature: Configuration, Security
badgePaas: label="PaaS만" type="Informative" url="https://experienceleague.adobe.com/ko/docs/commerce/user-guides/product-solutions" tooltip="Adobe Commerce 온 클라우드 프로젝트(Adobe 관리 PaaS 인프라) 및 온프레미스 프로젝트에만 적용됩니다."
TQID: https://experienceleague.adobe.com/zPxdplYIYblw6-tsDvxEmvKfAx-2M6opb6qjX7YL1I4
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2:
  - id: ba9e5be9-7de1-4f71-a5d2-baead0e425ee
  - id: dac87252-6066-4d6e-a9d2-f6d84c323de7
  - id: f42e0a1a-0d79-488d-a83f-f2c30672b137
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2:
  - id: aa2f3246-cb95-4b30-8899-fdf7d73550cc
  - id: d095671a-1355-40aa-8b5f-06c33c68080b
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
  - id: f4e6943a-c91a-4134-a2c7-f4f20cfff2f0
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 285
ht-degree: 0%

---

# 브라우저 기능 감지

인터넷의 대부분의 웹 사이트 및 애플리케이션과 마찬가지로 Adobe Commerce 및 Magento Open Source에서는 방문자의 브라우저가 쿠키와 JavaScript을 모두 허용하여 전체 작업을 수행해야 합니다. 그러나 사용자의 브라우저가 쿠키와 JavaScript을 모두 방지하는 가장 높은 개인 정보 보호 설정으로 설정되는 경우가 있습니다. 스토어는 각 방문자의 브라우저의 기능을 테스트하고 설정을 변경해야 하는 경우 알림을 표시하도록 구성할 수 있습니다.

- 브라우저의 개인 정보 설정에서 쿠키를 허용하지 않는 경우, 대부분의 브라우저에서 권장 설정을 만드는 방법에 대해 설명하는 [쿠키 사용](../content-design/pages.md#enable-cookies) 페이지로 자동으로 리디렉션하도록 시스템을 구성할 수 있습니다.
- 브라우저의 개인 정보 설정에서 JavaScript을 허용하지 않는 경우 모든 페이지의 헤더 위에 다음 메시지가 표시되도록 시스템을 구성할 수 있습니다.

자세한 내용은 _설치 가이드_&#x200B;의 [지원되는 브라우저](https://experienceleague.adobe.com/docs/commerce-operations/installation-guide/system-requirements.html?lang=ko#supported-browsers)를 참조하세요.

## 브라우저 기능 감지 구성

1. _관리자_ 사이드바에서 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**(으)로 이동합니다.

1. _[!UICONTROL General]_&#x200B;아래 왼쪽 패널에서&#x200B;**[!UICONTROL Web]**&#x200B;을(를) 선택합니다.

1. **[!UICONTROL Browser Capabilities Detection]** 섹션에서 ![확장 선택기](../assets/icon-display-expand.png)를 확장하고 다음을 수행합니다.

   - 쿠키를 허용하도록 브라우저를 구성하는 방법을 설명하는 지침을 표시하려면 **[!UICONTROL Redirect to CMS-page if Cookies are Disabled]**&#x200B;을(를) `Yes`(으)로 설정하십시오.

   - 사용자의 브라우저에서 JavaScript이 비활성화되어 있을 때 머리글 위에 배너를 표시하려면 **[!UICONTROL Show Notice if JavaScript is Disabled]**&#x200B;을(를) `Yes`(으)로 설정하십시오.

   - 사용자의 브라우저에서 로컬 저장소가 비활성화되어 있을 때 머리글 위에 배너를 표시하려면 **[!UICONTROL Show Notice if Local Storage is Disabled]**&#x200B;을(를) `Yes`(으)로 설정하십시오.

   ![일반 구성 - 웹 브라우저 기능 검색](../configuration-reference/general/assets/web-browser-capabilities-detection.png){width="600" zoomable="yes"}

1. 완료되면 **[!UICONTROL Save Config]**&#x200B;을(를) 클릭합니다.
