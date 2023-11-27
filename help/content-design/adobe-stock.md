---
title: Adobe Stock 통합
description: Adobe Stock과 통합 [!DNL Commerce] 스토어에서 사용하기 위해 셀 수 없는 미디어 자산에 액세스하는 인스턴스.
exl-id: 0f399ea7-5726-476c-a945-c37e44a9ea55
feature: CMS, Media, Configuration, Integration
source-git-commit: b659c7e1e8f2ae9883f1e24d8045d6dd1e90cfc0
workflow-type: tm+mt
source-wordcount: '385'
ht-degree: 0%

---

# Adobe Stock 통합

스토어에서 사용할 수 있는 수많은 미디어 자산에 액세스하려면 다음을 통합하십시오. [Adobe Stock][adobe-stock] 포함 [!UICONTROL Commerce].

![Adobe Stock 검색 결과](./assets/adobe-stock-search-grid.png){width="700" zoomable="yes"}

Adobe Stock 서비스는 기업에게 모든 광고 프로젝트를 위해 고품질로 큐레이팅된 로열티가 없는 수백만 장의 사진, 벡터, 일러스트레이션, 비디오, 템플릿 및 3D 자산에 대한 액세스를 제공합니다. [!DNL Commerce] 사용자는 Adobe Stock 에셋을 빠르게 찾고, 미리 보고, 라이선스를 제공할 수 있습니다. 또한 다음을 저장할 수 있습니다 [미디어 스토리지][media-storage], 관리 작업 영역을 종료하지 않고 모든 작업을 수행할 수 있습니다.

## 전제 조건

이 통합에는 다음이 필요합니다.

- An [Adobe Developer][dev-console] account
- Adobe Commerce 또는 Magento Open Source, 2.3.4 이상

Adobe Stock 이미지에 라이선스를 부여하려면 다음 작업을 수행하십시오.

- An [Adobe 계정][adobe-signin]
- 유료 [Adobe Stock][adobe-stock] 계정과 연계된 플랜

## 통합 [!DNL Commerce] 및 Adobe Stock

Adobe Commerce에 대한 Adobe Stock 통합 구성은 두 단계 프로세스입니다.

1. [adobe.developer 통합 만들기](#create-an-adobe-developer-integration) API 키를 생성하려면
1. [Commerce 관리에서 Adobe Stock 통합 구성](#configure-the-adobe-stock-integration)

### Adobe Developer 통합 만들기

1. 다음 위치로 이동 [Adobe Developer 콘솔][dev-console].

1. 아래 _[!UICONTROL Quick Start]_, 클릭&#x200B;**[!UICONTROL Create new project]**.

1. 다음에서 _[!UICONTROL Project overview]_블록, 클릭&#x200B;**[!UICONTROL Add API]**.

1. 선택 **[!UICONTROL Adobe Stock]** 통합 목록에서 을(를) 클릭하고 **[!UICONTROL Next]**.

1. OAuth 2.0 선택 **[!UICONTROL Web App]**.

1. 다음을 지정합니다. **[!UICONTROL redirect URI]**.

   기본 리디렉션 URI의 형식은 다음과 같습니다. `${HOST}/${ADMIN_URI}/adobe_ims/oauth/callback/`, 예: `https://store.myshop.com/admin_hgkq1l/adobe_ims/oauth/callback/`, 여기서:

   - `${HOST}` 본인 [!DNL Commerce] 정규화된 도메인 이름(예: `https://store.myshop.com`).
   - `${ADMIN_URI}` 본인 [!DNL Commerce] 관리자 URI(예: `admin_hgkq1l`), 실행 시 검색할 수 있음 `magento info:adminuri`.

1. 다음을 지정합니다. **[!UICONTROL Redirect URI pattern]**: 두 가지 차이점이 있는 리디렉션 URI와 동일합니다.

   - 모든 마침표(`.`)는 두 개의 백슬래시( )를 사용하여 이스케이프해야 합니다.`\\`).
   - 추가 `.*` 를 사용하십시오.

   이전 기본 리디렉션 URI의 예를 사용하면 다음과 같습니다. `https://store\\.myshop\\.com/admin_hgkq1l/adobe_ims/oauth/callback/.*`.

1. 클릭 **[!UICONTROL Next]**.

1. 사용 가능한 범위를 검토하고 **[!UICONTROL Save configured API]**.

1. 다음 페이지에서 다음을 복사합니다. **[!UICONTROL Client ID]** (API 키) 및 **[!UICONTROL Client secret]**.

   이 정보는 다음 섹션의 단계에 사용됩니다.

### Adobe Stock 통합 구성

에서 시스템 구성을 설정하려면 [!DNL Commerce] 책임자, 사용 _API 키_ 및 _클라이언트 암호_ 에서 생성됨 [이전 섹션][create-integration].

1. 다음에서 _관리자_ 사이드바, 이동 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. 왼쪽 패널에서 를 확장합니다. **[!UICONTROL Advanced]** 및 선택 **[!UICONTROL System]**.

1. 확장 ![확장 선택기](../assets/icon-display-expand.png) **[!UICONTROL Adobe Stock Integration]** 다음을 수행합니다.

   - 설정 **[!UICONTROL Enabled Adobe Stock]** 끝 `Yes`.

   - 다음을 입력하십시오. **[!UICONTROL API Key (Client ID)]**.

   - 다음을 입력하십시오. **[!UICONTROL Client Secret]**.

   - 클릭 **[!UICONTROL Test Connection]** 키를 확인합니다.

   ![고급 구성 - Adobe Stock 통합](./assets/system-adobe-stock-integration.png){width="600" zoomable="yes"}

   몇 초 후에 유효성 검사를 수행합니다. 자격 증명이 유효한 경우 녹색으로 표시됩니다. _연결 성공!_ 메시지.

1. 완료되면 다음을 클릭하십시오. **[!UICONTROL Save Config]**.

[adobe-stock]: https://stock.adobe.com
[adobe-signin]: https://helpx.adobe.com/manage-account/using/access-adobe-id-account.html
[media-storage]: media-storage.md
[dev-console]: https://developer.adobe.com/console/home
[create-integration]: #create-an-adobeio-integration
