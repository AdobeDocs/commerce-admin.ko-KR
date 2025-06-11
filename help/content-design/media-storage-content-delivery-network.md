---
title: 컨텐츠 전달 네트워크 사용
description: CDN(Content Delivery Network)을 사용하여 미디어 파일을 저장하는 방법을 알아봅니다.
exl-id: cb612b79-f3e3-4f1b-8cf9-d47886486686
feature: Page Content, Media, Configuration
level: Experienced
badgePaas: label="PaaS만" type="Informative" url="https://experienceleague.adobe.com/ko/docs/commerce/user-guides/product-solutions" tooltip="Adobe Commerce 온 클라우드 프로젝트(Adobe 관리 PaaS 인프라) 및 온프레미스 프로젝트에만 적용됩니다."
source-git-commit: 57a913b21f4cbbb4f0800afe13012ff46d578f8e
workflow-type: tm+mt
source-wordcount: '416'
ht-degree: 0%

---

# 컨텐츠 전달 네트워크 사용

CDN(Content Delivery Network)을 사용하여 미디어 파일을 저장할 수 있습니다. 클라우드 인프라의 Adobe Commerce에는 Fastly CDN이 포함되어 있습니다(_Commerce on Cloud Infrastructure Guide_&#x200B;의 [Fastly](https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/cdn/fastly.html?lang=ko) 참조). _온-프레미스_&#x200B;에 설치된 Commerce 인스턴스에는 특정 CDN과의 통합이 포함되지 않으므로 원하는 CDN을 사용할 수 있습니다.

CDN을 구성한 후에는 관리자로부터 구성을 완료해야 합니다. 글로벌 또는 웹 사이트 수준에서 변경할 수 있습니다. CDN을 미디어 저장소에 사용하면 Commerce 저장소 페이지의 미디어에 대한 모든 경로가 구성에 지정된 CDN 경로로 변경됩니다.

## CDN 워크플로

1. **브라우저에서 미디어 요청** - 스토어의 페이지가 고객의 브라우저에서 열리고, 브라우저가 HTML에 지정된 미디어를 요청합니다.
1. **CDN으로 요청 전송, 이미지를 찾아서 제공** - 요청이 먼저 CDN으로 전송됩니다. CDN에 이미지가 저장되어 있는 경우 미디어 파일을 고객의 브라우저에 제공합니다.
1. **미디어를 찾을 수 없습니다. 요청이 [!DNL Commerce] 웹 서버에 전송되었습니다.** - CDN에 미디어 파일이 없는 경우 요청이 [!DNL Commerce] 웹 서버에 전송됩니다. 미디어 파일이 파일 시스템에 있는 경우 웹 서버가 해당 파일을 고객의 브라우저로 보냅니다.

>[!IMPORTANT]
>
>보안을 위해 CDN이 미디어 스토리지로 사용되는 경우 CDN이 하위 도메인 외부에 있으면 JavaScript이 제대로 작동하지 않을 수 있습니다.

## 컨텐츠 전달 네트워크 구성

1. _관리자_ 사이드바에서 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**(으)로 이동합니다.

1. _[!UICONTROL General]_&#x200B;아래의 왼쪽 패널에서&#x200B;**[!UICONTROL Web]**&#x200B;을(를) 선택합니다.

1. 왼쪽 상단 모서리에서 필요에 따라 **[!UICONTROL Store View]**&#x200B;을(를) 설정합니다.

1. **[!UICONTROL Base URLs]** 섹션에서 ![확장 선택기](../assets/icon-display-expand.png)를 확장하고 다음을 수행합니다.

   ![일반 구성 - 웹 기반 URL](./assets/web-base-urls.png){width="600" zoomable="yes"}

   - 정적 보기 파일이 저장된 CDN의 위치 URL로 **[!UICONTROL Base URL for Static View Files]**&#x200B;을(를) 업데이트합니다.

   - CDN에 있는 JavaScript 파일의 URL로 **[!UICONTROL Base URL for User Media Files]**&#x200B;을(를) 업데이트합니다.

     이 두 필드는 비워 두거나 자리 표시자로 시작할 수 있습니다. `{% raw %}{{unsecure_base_url}}{% endraw %}`

1. **[!UICONTROL Base URLs (Secure)]** 섹션에서 ![확장 선택기](../assets/icon-display-expand.png)를 확장하고 다음을 수행합니다.

   ![일반 구성 - 웹 기반 URL(보안)](./assets/web-base-urls-secure.png){width="600" zoomable="yes"}

   - 정적 보기 파일이 저장된 CDN의 위치 URL로 **[!UICONTROL Secure Base URL for Static View Files]**&#x200B;을(를) 업데이트합니다.

   - CDN에 있는 JavaScript 파일의 URL로 **[!UICONTROL Secure Base URL for User Media Files]**&#x200B;을(를) 업데이트합니다.

     이 두 필드는 비워 두거나 자리 표시자로 시작할 수 있습니다. `{% raw %}{{unsecure_base_url}}{% endraw %}`

1. 완료되면 **[!UICONTROL Save Config]**&#x200B;을(를) 클릭합니다.
