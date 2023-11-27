---
title: 페이지
description: 에 포함된 핵심 콘텐츠 페이지에 대한 세부 정보 알아보기 [!DNL Commerce] 데모 스토어 및 기본 페이지 구성 변경.
exl-id: 4be7d3d6-ce36-42bc-9224-4804c3211f16
feature: Page Content, Configuration
source-git-commit: b659c7e1e8f2ae9883f1e24d8045d6dd1e90cfc0
workflow-type: tm+mt
source-wordcount: '908'
ht-degree: 0%

---

# 페이지

콘텐츠는 상점의 모든 제품과 마찬가지로 유통기한의 관점에서 볼 수 있습니다. 소셜 미디어 콘텐츠의 저장 수명이 24시간 미만이라는 것을 알고 있었습니까? 만든 콘텐츠의 잠재적 유통기한은 리소스를 투자할 위치를 결정하는 데 도움이 될 수 있습니다.

저장 수명이 긴 콘텐츠는 때로 다음과 같은 의미입니다. _항상 사용되는 콘텐츠_. 항상 사용되는 컨텐츠의 예로는 고객 성공 사례, _방법_ 지침 및 FAQ. 이와 달리 자연적으로 상하기 쉬운 내용에는 이벤트, 업계 뉴스, 보도 자료 등이 포함된다.

![샘플 Luma 스토어에 포함된 미국 정보 페이지 ](./assets/storefront-about-us.png){width="700" zoomable="yes"}

## 핵심 콘텐츠 페이지

다음 [!DNL Commerce] 데모 스토어에는 시작하는 데 도움이 되는 핵심 콘텐츠 페이지의 예가 있습니다. 이러한 모든 페이지는 사용자의 요구 사항에 맞게 수정할 수 있습니다. 스토어에서 다음 페이지를 살펴보고 콘텐츠가 메시지, 음성 및 브랜드를 전달하는지 확인하십시오.

### 홈

데모 [홈](../getting-started/storefront.md#home-page) 페이지에는 배너, 이미지 캐러셀, 링크가 있는 여러 정적 블록 및 새 제품 목록이 포함되어 있습니다.

### 개인정보 처리방침

스토어 [개인정보 처리방침](../getting-started/privacy-policy.md) 페이지는 자체 정보로 업데이트해야 합니다. 가장 좋은 방법은 개인정보 처리방침이 고객에게 회사에서 수집하는 정보의 유형과 그 사용 방법을 설명하는 것입니다.

### 404 찾을 수 없음

404 Page Not Found 페이지는 페이지를 찾을 수 없을 때 반환되는 응답 코드에 대해 이름이 지정됩니다. URL 리디렉션을 사용하면 이 페이지가 표시되는 횟수가 줄어듭니다. 그러나 필요한 경우 고객이 관심을 가질 수 있는 제품에 대한 몇 가지 링크를 제공하는 기회를 활용할 수도 있습니다.

### 액세스 거부됨

{{b2b-feature}}

다음 [액세스 거부됨](../b2b/account-company-roles-permissions.md) 회사 사용자에게 할당된 권한으로 인해 페이지에 액세스할 수 없게 되면 페이지가 표시됩니다.

### 쿠키 활성화

다음 [쿠키 활성화](../getting-started/compliance-cookie-law.md) 사이트 방문자의 브라우저에서 쿠키가 활성화되지 않은 경우 페이지가 표시됩니다. 이 페이지에서는 가장 많이 사용되는 브라우저에 대해 쿠키를 활성화하는 방법에 대해 단계별로 설명하는 지침을 제공합니다.

### 서비스를 사용할 수 없음

다음 [503 서비스를 사용할 수 없음](../configuration-reference/general/general.md) 서버를 사용할 수 없을 때 반환되는 응답 코드에 대해 page 라는 이름이 지정됩니다.

### 정보

정보 사용자 페이지는 스토어의 바닥글에서 연결됩니다. 이미지, 비디오, 보도 자료 및 공지 링크를 포함할 수 있습니다. 샘플 페이지의 오른쪽에는 이미지가 있고, 장식용 이미지는 페이지의 끝을 나타냅니다.

### 고객 서비스

고객 서비스 페이지는 페이지 계층 구조의 다른 노드입니다. 페이지의 두 헤더에는 고객이 헤더를 클릭할 때만 표시되는 콘텐츠가 있습니다.

![상점 첫 화면의 고객 서비스 페이지](./assets/storefront-customer-service.png){width="700" zoomable="yes"}

## 기본 페이지 구성

다음 _기본 페이지_ 구성은 와 관련된 랜딩 페이지를 결정합니다. [기본 URL](../stores-purchase/store-urls.md) 및 해당 홈 페이지. 또한 다음과 같은 경우에 나타나는 페이지를 결정합니다. _페이지를 찾을 수 없음_ 오류가 발생하며 [이동 경로](../catalog/navigation-breadcrumb-trail.md) 은 각 페이지의 맨 위에 나타납니다.

1. 다음에서 _관리자_ 사이드바, 이동  **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. 아래의 왼쪽 패널에서 _[!UICONTROL General]_, 선택&#x200B;**[!UICONTROL Web]**.

1. 확장 ![확장 선택기](../assets/icon-display-expand.png) 다음 **[!UICONTROL Default Pages]** 섹션.

   ![기본 페이지](./assets/web-default-pages.png){width="500" zoomable="yes"}

   | 필드 | [범위](../getting-started/websites-stores-views.md#scope-settings) | 설명 |
   |--- |--- |--- |
   | [!UICONTROL Default Web URL] | 스토어 뷰 | 기본 URL과 연결된 랜딩 페이지를 나타냅니다. 기본적으로 이 필드는 로 설정됩니다. `cms` 에서 페이지를 나타냅니다. [!DNL Commerce] 콘텐츠 관리 시스템. 블로그와 같은 다른 유형의 랜딩 페이지를 사용할 수도 있습니다. 예를 들어 다음 위치의 서버에 블로그가 설치되어 있는 경우 `magento/blog`, 폴더 이름을 입력할 수 있습니다 `blog` 를 페이지 선택에 대한 상대 경로로 사용합니다. |
   | [!UICONTROL CMS Home Page] | 스토어 뷰 | 스토어의 홈 페이지를 선택하려면 목록에서 CMS 페이지를 선택하면 됩니다. 기본적으로 CMS 홈 페이지에는 스토어에 사용할 수 있는 전체 CMS 페이지가 나열됩니다. |
   | [!UICONTROL Default No-route URL] | 스토어 뷰 | 다음과 같은 경우에 표시할 기본 페이지의 URL을 포함합니다. `404 Page not Found` 오류가 발생했습니다. 기본값은 입니다. `cms/noroute/index`. |
   | [!UICONTROL CMS No Route Page] | 스토어 뷰 | 404 페이지를 찾을 수 없음 오류가 발생할 때 표시할 특정 CMS 페이지를 식별합니다. 기본 페이지는 입니다. `404 Not Found`. |
   | [!UICONTROL CMS No Cookies Page] | 스토어 뷰 | 브라우저에 대해 쿠키가 활성화되지 않은 경우 나타나는 특정 CMS 페이지를 식별합니다. 이 페이지에서는 쿠키가 사용되는 이유와 각 브라우저에 대해 쿠키를 활성화하는 방법을 설명합니다. 기본 페이지는 입니다. `Enable Cookies`. |
   | [!UICONTROL Show Breadcrumbs for CMS Pages] | 스토어 뷰 | 카탈로그의 모든 CMS 페이지에 탐색 표시 추적이 표시되는지 여부를 결정합니다. 옵션: `Yes` / `No` |

   {style="table-layout:auto"}

1. 대상 **[!UICONTROL Default Web URL]**&#x200B;에 있는 폴더의 상대 경로를 입력합니다. [!DNL Commerce] 랜딩 페이지를 포함하는 설치.

   기본 설정, `cms`는 의 페이지를 나타냅니다. [!DNL Commerce] 콘텐츠 관리 시스템.

   >[!NOTE]
   >
   >특정 스토어 조회수를 보려면 **[!UICONTROL Use Default]** 옆에 있는 확인란 _[!UICONTROL Default Web URL]_및 변경할 기타 기본 설정이 포함되어 있습니다.

1. 설정 **[!UICONTROL CMS Home Page]** 홈 페이지로 사용할 CMS 페이지로 이동합니다. 다음과 같이 생성된 다른 페이지를 홈 페이지로 사용할 수 있습니다.

   - 독점 온라인 스토어에 오신 것을 환영합니다
   - 보상 포인트
   - 정보
   - 고객 서비스
   - 쿠키 활성화
   - 개인정보 처리방침
   - 회사: 액세스 거부됨

1. 대상 **[!UICONTROL Default No-route URL]**&#x200B;에 있는 폴더의 상대 경로를 입력합니다. [!DNL Commerce] 다음과 같은 경우 페이지가 리디렉션되는 설치 _404 페이지를 찾을 수 없음_ 오류가 발생했습니다.

   기본값은 입니다. `cms/index/noRoute`.

1. 설정 **[!UICONTROL CMS No Route Page]** 다음 경우에 표시되는 CMS 페이지로 이동 _404 페이지를 찾을 수 없음_ 오류가 발생했습니다.

1. 설정 **[!UICONTROL CMS No Cookies Page]** 브라우저에서 쿠키가 비활성화될 때 표시되는 CMS 페이지입니다. 이 페이지에서는 쿠키가 사용되는 이유와 각 브라우저에 대해 쿠키를 활성화하는 방법을 설명합니다. 기본 페이지는 입니다. `Enable Cookies`.

1. 이동 경로 추적을 모든 CMS 페이지의 맨 위에 표시하려면 을 설정합니다. **[!UICONTROL Show Breadcrumbs for CMS Pages]** 끝 `Yes`.

1. 완료되면 다음을 클릭하십시오. **[!UICONTROL Save Config]**.
