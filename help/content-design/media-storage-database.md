---
title: 미디어 데이터베이스 사용
description: 미디어 데이터베이스를 사용하여  [!DNL Commerce] 미디어 파일을 저장하는 방법에 대해 알아봅니다.
exl-id: b59349fb-0cb6-4812-a126-6e0d8d37564f
feature: Page Content, Media, Configuration
level: Experienced
source-git-commit: b659c7e1e8f2ae9883f1e24d8045d6dd1e90cfc0
workflow-type: tm+mt
source-wordcount: '387'
ht-degree: 0%

---

# 미디어 데이터베이스 사용

>[!IMPORTANT]
>
>데이터베이스 미디어 저장 방법은 Adobe Commerce 및 Magento Open Source 2.4.3부터 더 이상 사용되지 않습니다.

기본적으로 [!DNL Commerce] 인스턴스의 모든 이미지, 컴파일된 CSS 파일 및 컴파일된 JavaScript 파일은 웹 서버의 파일 시스템에 저장됩니다. 이러한 파일을 데이터베이스 서버의 데이터베이스에 저장하도록 선택할 수 있습니다. 이 방법의 한 가지 이점은 웹 서버 파일 시스템과 데이터베이스 간의 자동 동기화 및 역동기화 옵션입니다. 기본 데이터베이스를 사용하여 미디어를 저장하거나 만들 수 있습니다. 새로 만든 데이터베이스를 미디어 저장소로 사용하려면 `env.php` 파일에 데이터베이스 정보 및 데이터베이스 액세스 자격 증명을 추가해야 합니다.

## 데이터베이스 워크플로우

1. **브라우저가 미디어를 요청** - 저장소의 페이지가 고객의 브라우저에서 열리고, 브라우저가 HTML에 지정된 미디어를 요청합니다.

1. **시스템이 파일 시스템에서 미디어를 찾습니다** - 시스템이 파일 시스템에서 미디어를 검색하고 검색되면 브라우저에 전달합니다.

1. **시스템에서 데이터베이스의 미디어를 찾습니다** - 파일 시스템에서 미디어를 찾을 수 없으면 구성에 지정된 데이터베이스로 미디어 요청이 전송됩니다.

1. **시스템에서 데이터베이스의 미디어를 찾습니다** - PHP 스크립트는 데이터베이스에서 파일 시스템으로 파일을 전송하고 고객의 브라우저로 전송됩니다. 미디어에 대한 브라우저 요청은 스크립트가 다음과 같이 실행되도록 트리거합니다.

   - 웹 서버 [rewrites](../merchandising-promotions/url-rewrite.md)이(가) [!DNL Commerce]에 대해 활성화되어 있고 서버에서 지원하는 경우, PHP 스크립트는 요청된 미디어를 파일 시스템에서 찾을 수 없는 경우에만 실행됩니다.
   - 웹 서버 재쓰기가 [!DNL Commerce]에 대해 사용되지 않거나 서버에서 지원되지 않는 경우 파일 시스템에서 필요한 미디어를 사용할 수 있더라도 PHP 스크립트가 실행됩니다.

## 미디어 스토리지용 데이터베이스 사용

1. _관리자_ 사이드바에서 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**(으)로 이동합니다.

1. 왼쪽 패널에서 **[!UICONTROL Advanced]**&#x200B;을(를) 확장하고 **[!UICONTROL System]**&#x200B;을(를) 선택합니다.

1. 왼쪽 상단 모서리에서 **[!UICONTROL Store View]**&#x200B;을(를) `Default Config`(으)로 설정하여 전역 수준에서 구성을 적용합니다.

1. **[!UICONTROL Storage Configuration for Media]** 섹션에서 ![확장 선택기](../assets/icon-display-expand.png)를 확장하고 다음을 수행합니다.

   ![고급 구성 - 미디어에 대한 저장소 구성](./assets/database-storage-deprecated.png){width="600" zoomable="yes"}

   - **[!UICONTROL Media Storage]**&#x200B;을(를) `Database`(으)로 설정합니다.

   - **[!UICONTROL Select Media Database]**&#x200B;을(를) 사용할 데이터베이스로 설정합니다.

   - 기존 미디어를 새로 선택한 데이터베이스로 전송하려면 **[!UICONTROL Synchronize]**&#x200B;을(를) 클릭합니다.

   - **[!UICONTROL Environment Update Time]**&#x200B;을(를) 초 단위로 입력하십시오.

1. 완료되면 **[!UICONTROL Save Config]**&#x200B;을(를) 클릭합니다.
