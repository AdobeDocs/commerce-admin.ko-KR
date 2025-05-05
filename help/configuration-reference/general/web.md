---
title: '[!UICONTROL General] &gt; [!UICONTROL Web]'
description: Commerce 관리자의 [!UICONTROL General] &gt; [!UICONTROL Web] 페이지에서 구성 설정을 검토하십시오.
exl-id: 1809b03a-a55c-41b4-947b-f66f4bd290a1
feature: Site Management, Configuration
source-git-commit: 5a4417373f6dc720e8e14f883c27348a475ec255
workflow-type: tm+mt
source-wordcount: '1793'
ht-degree: 0%

---

# [!UICONTROL General] > [!UICONTROL Web]

{{config}}

## [!UICONTROL URL Options]

![웹 > 일반 옵션](./assets/web-url-options.png)<!-- zoom -->

<!-- [URL Options configuration settings](https://experienceleague.adobe.com/ko/docs/commerce-admin/stores-sales/site-store/store-urls) -->

| 필드 | 범위 | 설명 |
|  ---  |  ---  |  ---  |
| [!UICONTROL Add Store Code to URLs] | 글로벌 | 웹 서버 재작성을 사용하도록 설정한 경우 에서는 현재 보기의 스토어 코드를 URL에 삽입합니다. 옵션: `Yes` / `No`. <br />이 필드를 `Yes`(으)로 설정하면 URL 다시 쓰기가 올바르게 매핑되고 모든 페이지가 성공적으로 열리는지 확인하기 위해 브라우저 URL에 저장소 코드를 포함해야 합니다. _404 페이지를 찾을 수 없음_ 오류가 발생하지 않습니다. |
| [!UICONTROL Auto-redirect to Base URL] | 스토어 뷰 | (단일 스토어 설정의 경우) 사이트에 끊어진 링크가 있으면 은 트래픽을 &quot;404 페이지를 찾을 수 없음&quot; 메시지가 있는 페이지가 아닌 기본 URL로 리디렉션합니다. 옵션:` No` / `Yes (302 Found)` / `Yes (301 Moved Permanently)` <br />**_중요:_**&#x200B;다중 스토어 설정의 기본 URL로 자동 리디렉션을 사용하지 마십시오. |
| [!UICONTROL Catalog media URL format] | 글로벌 | 제품 및 범주에 할당된 [URL 형식](../../catalog/catalog-urls.md)을(를) 정의합니다. 옵션: 이미지 변형당 고유 해시(레거시 모드) 변환된 파일 이름을 고유한 해시 값으로 정의합니다. 쿼리 매개 변수를 기반으로 한 이미지 최적화는 쿼리 매개 변수에 따라 [이미지 최적화](../../content-design/media-gallery-image-optimization.md) 프로세스를 정의합니다. |

{style="table-layout:auto"}

## [!UICONTROL Search Engine Optimization]

![웹 > 검색 엔진 최적화](./assets/web-search-engine-optimization.png)<!-- zoom -->

<!-- [Search Engine Optimization configuration settings](https://experienceleague.adobe.com/ko/docs/commerce-admin/marketing/seo/url-rewrites/url-rewrite) -->

| 필드 | [범위](../../getting-started/websites-stores-views.md#scope-settings) | 설명 |
|--- |--- |--- |
| [!UICONTROL Use Web Server Rewrites] | 스토어 뷰 | PHP 기반 시스템에서는 일반적으로 루트 폴더에 `index.php` 파일을 포함합니다. 기본적으로 루트 폴더 이름 바로 뒤에 파일 이름이 URL에 나타납니다. 이 기능이 활성화되면 시스템이 URL에서 `index.php`을(를) 생략합니다. 이 유용성 모범 사례는 각 URL을 보다 간결하게 만들며 성능이나 사이트 등급에 영향을 주지 않습니다. 옵션: `Yes` / `No` |

{style="table-layout:auto"}

## [!UICONTROL Base URLs]

![웹 > 기본 URL](./assets/web-base-urls.png)<!-- zoom -->

<!-- [Base URLS configuration settings](https://experienceleague.adobe.com/ko/docs/commerce-admin/stores-sales/site-store/store-urls) -->

| 필드 | [범위](../../getting-started/websites-stores-views.md#scope-settings) | 설명 |
|--- |--- |--- |
| [!UICONTROL Base URL] | 스토어 뷰 | 암호화된(SSL) 채널을 통해 실행되고 있지 않은 Commerce 루트 폴더의 전체 주소입니다. URL은 슬래시로 끝나야 합니다. |
| [!UICONTROL Base Link URL] | 스토어 뷰 | 기본 URL의 자리 표시자로 사용되는 마크업 태그입니다. |
| [!UICONTROL Base URL for Static View Files] | 스토어 뷰 | css, 글꼴, 이미지 및 JavaScript과 같이 테마에 사용되는 정적 파일의 위치를 가리키는 경로입니다. 자리 표시자는 기본 URL을 나타내는 데 사용됩니다. Commerce 설치 시 폴더 구조가 동일한 사이트가 여러 개 있는 경우 사이트마다 다른 폴더가 있을 수 있습니다. 정적 보기 파일의 기본 URL을 입력하기 전에 구성 범위를 올바른 사이트로 설정합니다. Commerce 설치 외부에 폴더를 지정할 수도 있습니다. |
| [!UICONTROL Base URL for User Media Files] | 스토어 뷰 | 카탈로그 이미지 및 기타 미디어 파일의 위치를 가리키는 경로입니다. 자리 표시자는 기본 URL을 나타내는 데 사용됩니다. Commerce 설치 시 폴더 구조가 동일한 사이트가 여러 개 있는 경우 각각에 대해 서로 다른 미디어 폴더를 사용할 수 있습니다. 이렇게 하면 각 미디어 폴더를 개별적으로 백업하고 롤백할 수 있습니다. Commerce 설치 외부에 미디어 폴더를 지정할 수도 있습니다. |

{style="table-layout:auto"}

## [!UICONTROL Base URLs (Secure)]

![웹 > 기본 URL(보안)](./assets/web-base-urls-secure.png)<!-- zoom -->

<!-- [Base URLs (Secure) configuration settings](https://experienceleague.adobe.com/ko/docs/commerce-admin/stores-sales/site-store/store-urls) -->

| 필드 | [범위](../../getting-started/websites-stores-views.md#scope-settings) | 설명 |
|--- |--- |--- |
| [!UICONTROL Secure Base URL] | 스토어 뷰 | 암호화된 보안(SSL/TLS) 프로토콜을 통해 제공되는 Commerce 루트 폴더의 전체 주소입니다. URL은 슬래시로 끝나야 합니다. |
| [!UICONTROL Secure Base Link URL] | 스토어 뷰 | 보안 채널에서 실행되는 기본 URL의 자리 표시자로 사용되는 마크업 태그입니다. |
| [!UICONTROL Secure Base URL for Static View Files] | 스토어 뷰 | 테마에 사용되는 CSS, 글꼴, 이미지 및 JavaScript과 같은 정적 파일의 위치를 가리키는 마크업 태그입니다. 파일은 비보안 또는 보안 채널에 있을 수 있습니다. Commerce 설치 시 폴더 구조가 동일한 사이트가 여러 개 있는 경우 사이트마다 다른 폴더가 있을 수 있습니다. 정적 보기 파일의 기본 URL을 입력하기 전에 구성 범위를 올바른 사이트로 설정합니다. Commerce 설치 외부에 폴더를 지정할 수도 있습니다. |
| [!UICONTROL Secure Base URL for User Media Files] | 스토어 뷰 | 카탈로그 이미지 및 기타 미디어 파일의 위치를 가리키는 경로입니다. 파일은 비보안 또는 보안 채널에 있을 수 있습니다. 자리 표시자는 기본 URL을 나타내는 데 사용됩니다. Commerce 설치 시 폴더 구조가 동일한 사이트가 여러 개 있는 경우 각각에 대해 서로 다른 미디어 폴더를 사용할 수 있습니다. 이렇게 하면 각 미디어 폴더를 개별적으로 백업하고 롤백할 수 있습니다. Commerce 설치 외부에 미디어 폴더를 지정할 수도 있습니다. |
| [!UICONTROL Use Secure URLs on Storefront] | 스토어 뷰 | 도메인에 보안 인증서가 있는 경우 SSL 암호화를 사용하거나 사용하지 않고 Storefront를 실행하도록 선택할 수 있습니다. 옵션:<br />**`Yes`**- 저장소 URL은 `https`(으)로 시작하여 페이지가 암호화된 보안 프로토콜로 전달됨을 나타냅니다.<br />**`No`** - 저장소 URL은 `http`(으)로 시작하여 보안 프로토콜 없이 페이지가 전달됨을 나타냅니다. |
| [!UICONTROL Use Secure URLs in Admin] | 글로벌 | 도메인에 보안 인증서가 있는 경우 SSL 암호화를 사용하거나 사용하지 않고 저장소 관리자를 실행하도록 선택할 수 있습니다. 옵션: <br />**`Yes`**- 페이지가 암호화된 보안 프로토콜로 제공됨을 나타내기 위해 관리자 URL이 `https`(으)로 시작됩니다.<br />**`No`** - 관리 URL은 `http`(으)로 시작하여 보안 프로토콜 없이 페이지가 전달됨을 나타냅니다.<br /> 저장소와 관리자 모두에 대해 보안 URL을 사용하도록 설정하면 `HSTS`을(를) 사용하도록 설정하고 구성하는 두 개의 추가 필드가 나타납니다. |
| [!UICONTROL Enable HTTP Strict Transport Security (HSTS)] | 스토어 뷰 | 사용하도록 설정하면 [`HSTS`][1]에서 &quot;man in the middle&quot; 공격에 대한 보안 측정을 제공하고 사용자가 &quot;잘못된 인증서&quot; 메시지를 재정의하지 못하도록 합니다. 옵션: `Yes` / `No` |
| [!UICONTROL Upgrade Insecure Requests] | 스토어 뷰 | 사용하도록 설정하면 브라우저에서 받은 비보안(`HTTP`) 요청을 보안(`HTTPS`) 프로토콜로 변환합니다. 옵션: `Yes` / `No` |
| [!UICONTROL Offloader Header] | 글로벌 | 클라이언트와 부하 분산 장치 간의 프로토콜을 식별하기 위해 서버 구성의 `offloader_header` 값을 지정합니다. 대부분의 Commerce 설치에서는 기본값인 `X-Forwarded-Proto`(XFP)을 사용하여 프로토콜을 `HTTP` 또는 `HTTPS`(으)로 식별합니다. |

{style="table-layout:auto"}

## [!UICONTROL Default Pages]

![웹 > 기본 페이지](./assets/web-default-pages.png)<!-- zoom -->

<!-- [Default Pages configuration settings](https://experienceleague.adobe.com/ko/docs/commerce-admin/content-design/elements/pages/pages#configure-default-pages) -->

| 필드 | [범위](../../getting-started/websites-stores-views.md#scope-settings) | 설명 |
|--- |--- |--- |
| [!UICONTROL Default Web URL] | 스토어 뷰 | 기본 URL과 연결된 랜딩 페이지를 나타냅니다. Commerce 콘텐츠 관리 시스템(CMS)의 페이지를 나타내기 위해 기본적으로 &quot;cms&quot;로 설정되어 있습니다. 블로그와 같은 다른 유형의 랜딩 페이지를 사용할 수도 있습니다. 예를 들어, 서버에 블로그가 `magento/blog`에 설치된 경우 &quot;blog&quot; 폴더의 이름을 페이지 선택에 대한 상대 경로로 입력할 수 있습니다. |
| [!UICONTROL CMS Home Page] | 스토어 뷰 | 스토어의 홈 페이지를 선택하려면 목록에서 CMS 페이지를 선택하면 됩니다. 기본적으로 CMS 홈 페이지에는 스토어에 사용할 수 있는 CMS 페이지의 전체 목록이 있습니다. |
| [!UICONTROL Default No-route URL] | 스토어 뷰 | `404 Page not Found` 오류가 발생할 때 표시할 기본 페이지의 URL을 포함합니다. 기본값은 `cms/noroute/index`입니다. |
| [!UICONTROL CMS No Route Page] | 스토어 뷰 | 404 페이지를 찾을 수 없음 오류가 발생할 때 표시할 특정 CMS 페이지를 식별합니다. 기본 페이지는 404 찾을 수 없음 입니다. |
| [!UICONTROL CMS No Cookies Page] | 스토어 뷰 | 브라우저에 대해 쿠키가 활성화되지 않은 경우 나타나는 특정 CMS 페이지를 식별합니다. 이 페이지에서는 쿠키가 사용되는 이유와 각 브라우저에 대해 쿠키를 활성화하는 방법을 설명합니다. 기본 페이지는 쿠키 활성화 입니다. |
| [!UICONTROL Show Breadcrumbs for CMS Pages] | 스토어 뷰 | 이동 경로 추적이 카탈로그의 모든 CMS 페이지에 표시되는지 여부를 결정합니다. 옵션: `Yes` / `No` |

{style="table-layout:auto"}

## [!UICONTROL Default Layouts]

![기본 레이아웃](./assets/web-default-layouts.png)<!-- zoom -->

<!--[Default Layouts](https://experienceleague.adobe.com/ko/docs/commerce-admin/content-design/design/layout/page-layout) -->

| 필드 | [범위](../../getting-started/websites-stores-views.md#scope-settings) | 설명 |
|--- |--- |--- |
| [!UICONTROL Default Product Layout] | 글로벌 | 제품 페이지에 기본적으로 사용되는 [레이아웃](../../content-design/page-layout.md)을(를) 결정합니다. 옵션: <br/>**`No layout updates`**- 기본적으로 제품 페이지에 대해 레이아웃 업데이트를 사용할 수 없습니다.<br/>**`Empty`** - 기본적으로 은 제품 페이지에 빈 레이아웃을 사용합니다. <br/>**`1 column`**- 기본적으로 은 제품 페이지에 대해 단일 열 레이아웃을 사용합니다.<br/>**`2 columns with left bar`** - 기본적으로 에서는 제품 페이지의 왼쪽에 사이드바가 있는 2열 레이아웃을 사용합니다. <br/>**`2 columns with right bar`**- 기본적으로 제품 페이지의 오른쪽에 사이드바가 있는 2열 레이아웃을 사용합니다.<br/>**`3 columns`** - 기본적으로 은 제품 페이지의 왼쪽과 오른쪽에 사이드바가 있는 3열 레이아웃을 사용합니다.<br/>**`Page -- Full Width`**- ([!DNL Page Builder] 필요) 기본적으로 제품 페이지의 페이지 — 전체 너비 레이아웃을 사용합니다.<br/>**`Category - Full Width`** - ([!DNL Page Builder] 필요) 기본적으로 제품 페이지에 대해 범주 - 전체 너비 레이아웃을 사용합니다. <br/>**`Product - Full Width`**- ([!DNL Page Builder] 필요) 기본적으로 제품 페이지의 제품 - 전체 너비 레이아웃을 사용합니다. |
| [!UICONTROL Default Category Layout] | 글로벌 | 범주 페이지에 기본적으로 사용되는 [레이아웃](../../content-design/page-layout.md)을 결정합니다. 옵션: <br/>**`No layout updates`**- 기본적으로 범주 페이지에는 레이아웃 업데이트를 사용할 수 없습니다.<br/>**`Empty`** - 기본적으로, 범주 페이지에 빈 레이아웃을 사용합니다. <br/>**`1 column`**- 기본적으로 범주 페이지에 대해 단일 열 레이아웃을 사용합니다.<br/>**`2 columns with left bar`** - 기본적으로, 범주 페이지의 경우 왼쪽에 사이드바가 있는 2열 레이아웃을 사용합니다. <br/>**`2 columns with right bar`**- 기본적으로 범주 페이지의 오른쪽에 사이드바가 있는 2열 레이아웃을 사용합니다.<br/>**`3 columns`** - 기본적으로 은 범주 페이지의 왼쪽과 오른쪽에 사이드바가 있는 3열 레이아웃을 사용합니다.<br/>**`Page - Full Width`**- ([!DNL Page Builder] 필요) 기본적으로 범주 페이지에 대한 페이지 - 전체 너비 레이아웃을 사용합니다.<br/>**`Category - Full Width`** - ([!DNL Page Builder] 필요) 기본적으로 범주 페이지의 범주 - 전체 너비 레이아웃을 사용합니다. <br/>**`Product - Full Width`**- ([!DNL Page Builder] 필요) 기본적으로 범주 페이지에 대해 제품 - 전체 너비 레이아웃을 사용합니다. |
| 기본 페이지 레이아웃 | 글로벌 | CMS 페이지에 기본적으로 사용되는 [레이아웃](../../content-design/page-layout.md)을(를) 결정합니다. 옵션: <br/>**`No layout updates`**- 기본적으로 CMS 페이지에 대해 레이아웃 업데이트를 사용할 수 없습니다.<br/>**`Empty`** - 기본적으로 은(는) CMS 페이지에 대해 빈 레이아웃을 사용합니다. <br/>**`1 column`**- 기본적으로 은(는) CMS 페이지에 대해 단일 열 레이아웃을 사용합니다.<br/>**`2 columns with left bar`** - 기본적으로 은(는) CMS 페이지의 왼쪽에 사이드바가 있는 2열 레이아웃을 사용합니다.<br/>**`2 columns with right bar`**- 기본적으로 은(는) CMS 페이지의 오른쪽에 사이드바가 있는 2열 레이아웃을 사용합니다.<br/>**`3 columns`** - 기본적으로 은 CMS 페이지의 왼쪽과 오른쪽에 사이드바가 있는 3열 레이아웃을 사용합니다.<br/>**`Page - Full Width`**- ([!UICONTROL Page Builder] 필요) 기본적으로 CMS 페이지에 대한 페이지 - 전체 너비 레이아웃을 사용합니다.<br/>**`Category - Full Width`** - ([!UICONTROL Page Builder] 필요) 기본적으로 CMS 페이지에 대해 범주 - 전체 너비 레이아웃을 사용합니다. <br/>**`Product - Full Width`**- ([!DNL Page Builder] 필요) 기본적으로 CMS 페이지에 대한 제품 - 전체 너비 레이아웃을 사용합니다. |

{style="table-layout:auto"}

## [!UICONTROL Default Cookie Settings]

![웹 > 기본 쿠키 설정](./assets/web-default-cookie-settings.png)<!-- zoom -->

<!-- [Default Cookie configuration settings](https://experienceleague.adobe.com/ko/docs/commerce-admin/start/compliance/privacy/compliance-cookie-law) -->

| 필드 | [범위](../../getting-started/websites-stores-views.md#scope-settings) | 설명 |
|--- |--- |--- |
| [!UICONTROL Cookie Lifetime] | 스토어 뷰 | 쿠키가 자동으로 삭제되기 전까지 쿠키가 존재할 수 있는 기간을 결정합니다. 기본값은 3,600초(1시간)입니다. |
| [!UICONTROL Cookie Path] | 스토어 뷰 | Commerce 쿠키를 사용할 수 있는 서버의 폴더를 지정합니다. Commerce 쿠키를 설치의 모든 곳에서 사용할 수 있도록 하려면 쿠키 경로 를 슬래시(`/`)로 설정합니다. 이 값은 쿠키 경로만 포함할 수 있으며 **_cannot_**&#x200B;에는 다른 쿠키 매개 변수가 포함될 수 없습니다. |
| [!UICONTROL Cookie Domain] | 스토어 뷰 | 하위 도메인에서 Commerce 쿠키를 사용할 수 있는지 여부를 결정합니다. 예를 들어 `mysubdomain`.domain.com을 지원하려면 `.domain.com`처럼 시작 부분에 마침표를 사용하여 도메인 이름을 입력합니다. 이 값은 쿠키 도메인만 포함할 수 있으며 **_cannot_**&#x200B;에는 다른 쿠키 매개 변수가 포함될 수 없습니다. |
| [!UICONTROL Use HTTP Only] | 스토어 뷰 | Commerce 쿠키를 비보안 채널(http)에서만 사용할 수 있는지 또는 암호화된 채널(https)에서도 사용할 수 있는지 여부를 결정합니다. 옵션: `Yes` / `No` |
| [!UICONTROL Cookie Restriction Mode] | 웹 사이트 | 쿠키 제한 모드가 활성화되어 있는지 여부를 결정합니다. 옵션: `Yes` / `No` |

{style="table-layout:auto"}

## [!UICONTROL Session Validation Settings]

![웹 > 세션 유효성 검사](./assets/web-session-validation-settings.png)<!-- zoom -->

<!-- [Session Validation configuration settings](https://experienceleague.adobe.com/ko/docs/commerce-admin/systems/security/security-session-management#session-validation) -->

| 필드 | [범위](../../getting-started/websites-stores-views.md#scope-settings) | 설명 |
|--- |--- |--- |
| [!UICONTROL Validate REMOTE_ADDR] | 글로벌 | 요청의 IP 주소가 `$_SESSION` 데이터와 일치하는지 확인합니다. 다른 IP 주소가 검색되면 세션이 종료됩니다. 옵션: `Yes` / `No` |
| [!UICONTROL Validate HTTP_VIA] | 글로벌 | 들어오는 프록시 데이터를 확인하고 요청의 프록시 주소가 `$_SESSION` 데이터와 일치하는지 확인합니다. 다른 프록시 주소가 검색되면 세션이 종료됩니다. 옵션: `Yes` / `No` |
| [!UICONTROL Validate HTTP_x_FORWARDED_FOR] | 글로벌 | 나가는 프록시 데이터를 확인하고 요청의 전달된 주소가 `$_SESSION` 데이터와 일치하는지 확인합니다. 다른 forwarded-for 주소가 검색되면 세션이 종료됩니다. 옵션: `Yes` / `No` |
| [!UICONTROL Validate HTTP_USER_AGENT] | 글로벌 | `USER_AGENT`은(는) 웹 사이트에 액세스하는 데 사용되는 브라우저나 장치를 나타냅니다. 브라우저 및 운영 체제의 이름과 버전이 `$_SESSION` 데이터와 일치하는지 확인합니다. 동일한 세션의 한 요청에서 다른 요청으로 다른 사용자 에이전트가 감지되면 세션이 종료됩니다. 옵션: `Yes` / `No` |

{style="table-layout:auto"}

## [!UICONTROL Browser Capabilities Detection]

![웹 > 브라우저 기능 검색](./assets/web-browser-capabilities-detection.png)<!-- zoom -->

<!-- [Browser Capabilities Detection configuration settings](https://experienceleague.adobe.com/ko/docs/commerce-admin/systems/security/security-browser-capabilities-detection) -->

| 필드 | [범위](../../getting-started/websites-stores-views.md#scope-settings) | 설명 |
|--- |--- |--- |
| [!UICONTROL Redirect to CMS-page if Cookies are Disabled] | 스토어 뷰 | 브라우저에서 쿠키를 비활성화하면 자동으로 CMS 쿠키 없음 페이지로 리디렉션됩니다. 옵션: `Yes` / `No` |
| [!UICONTROL Show Notice if JavaScript is Disabled] | 스토어 뷰 | 브라우저에 의해 JavaScript이 비활성화되어 있으면 사용자에게 JavaScript 옵션을 활성화하라는 메시지가 표시됩니다. `Yes` / `No`(비활성화) |
| [!UICONTROL Show Notice if Local Storage is Disabled] | 스토어 뷰 | 로컬 캐시가 비활성화된 경우 메시지를 표시합니다. 옵션: `Yes` / `No` |

{style="table-layout:auto"}

[1]: https://cheatsheetseries.owasp.org/cheatsheets/HTTP_Strict_Transport_Security_Cheat_Sheet.html
