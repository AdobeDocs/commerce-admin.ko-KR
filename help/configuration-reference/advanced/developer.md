---
title: '[!UICONTROL Advanced] &gt; [!UICONTROL Developer]'
description: 에서 구성 설정을 검토합니다. [!UICONTROL Advanced] &gt; [!UICONTROL Developer] 상거래 관리자의 페이지입니다.
exl-id: 2ef4ba6a-b5a5-419d-8d61-e535e3366370
role: Admin, Developer
feature: Site Management, Configuration, System
source-git-commit: 370131cd73a320b04ee92fa9609cb24ad4c07eca
workflow-type: tm+mt
source-wordcount: '835'
ht-degree: 1%

---

# [!UICONTROL Advanced] > [!UICONTROL Developer]

{{config}}

>[!NOTE]
>
>이러한 구성 설정은에서 사용할 수 있습니다. [개발자 모드](../../systems/developer-tools.md#operation-modes) 만 해당.

## [!UICONTROL Frontend Development Workflow]

![프론트엔드 개발 워크플로](./assets/developer-frontend-development-workflow.png)<!-- zoom -->

이러한 설정 변경에 대한 자세한 내용은 [프론트엔드 개발 워크플로](../../systems/developer-tools.md#frontend-development-workflow) 다음에서 _관리 시스템 안내서_.

| 필드 | [범위](../../getting-started/websites-stores-views.md#scope-settings) | 설명 |
|--- |--- |--- |
| [!UICONTROL Workflow Type] | 글로벌 | 개발 중에 클라이언트측에서 컴파일 수가 줄어드는지 아니면 서버측에서 컴파일 수가 줄어드는지 여부를 결정합니다. 옵션: <br/>**`Client side less compilation`**- 기본 less.js 라이브러리를 사용하여 브라우저에서 컴파일이 수행됩니다.<br/>**`Server side less compilation`** - 컴파일은 Less PHP 라이브러리를 사용하여 서버에서 발생합니다. 프로덕션 기본 모드입니다. |

{:style=&quot;table-layout:auto&quot;}

## [!UICONTROL Developer Client Restrictions]

![개발자 클라이언트 제한 사항](./assets/developer-developer-client-restrictions.png)<!-- zoom -->

이 설정을 변경하는 방법에 대한 자세한 내용은 [클라이언트 제한 사항](../../systems/developer-tools.md#client-restrictions) 다음에서 _관리 시스템 안내서_.

| 필드 | [범위](../../getting-started/websites-stores-views.md#scope-settings) | 설명 |
|--- |--- |--- |
| [!UICONTROL Allow IPs (comma separated)] | 스토어 뷰 | 스토어의 개발자 도구를 방해하지 않고 라이브 사이트에서 사용할 수 있는 허용 목록에 추가하다 를 만듭니다. 개발자 도구를 사용할 때 사이트에 대한 모든 변경 사항(예: _인라인 번역_&#x200B;는 허용 목록에 추가하다의 IP 주소에서만 볼 수 있습니다. |

{:style=&quot;table-layout:auto&quot;}

## [!UICONTROL Template Settings]

![템플릿 설정](./assets/developer-template-settings.png)<!-- zoom -->

이러한 설정 변경에 대한 자세한 내용은 [리소스 파일 최적화 중](../../systems/developer-tools.md#optimizing-resource-files) 다음에서 _관리 시스템 안내서_.

| 필드 | [범위](../../getting-started/websites-stores-views.md#scope-settings) | 설명 |
|--- |--- |--- |
| [!UICONTROL Allow Symlinks] | 스토어 뷰 | 활성화 중 [심볼 링크](https://en.wikipedia.org/wiki/Symbolic_link) 는 사이트를 보안 위험에 노출할 수 있으며 프로덕션 스토어에는 권장되지 않습니다. |
| [!UICONTROL Minify Html] | 스토어 뷰 | 저장소 템플릿에 대한 HTML이 최소화되는지 여부를 결정합니다. 옵션: `Yes` / `No` |

{:style=&quot;table-layout:auto&quot;}

## [!UICONTROL Debug]

![디버그](./assets/developer-debug.png)<!-- zoom -->

이러한 설정 변경에 대한 자세한 내용은 [템플릿 경로 힌트](../../systems/developer-tools.md#template-path-hints) 다음에서 _관리 시스템 안내서_.

| 필드 | [범위](../../getting-started/websites-stores-views.md#scope-settings) | 설명 |
|--- |--- |--- |
| [!UICONTROL Enable Template Path Hints for Storefront] | 스토어 뷰 | 페이지에서 사용되는 각 템플릿의 경로를 나타내는 표기법을 상점 앞에 추가합니다. 옵션: `Yes` / `No` |
| [!UICONTROL Enable Template Path Hints for Admin] | 글로벌 | 페이지에서 사용되는 각 템플릿의 경로를 나타내는 표기법을 관리자에 추가합니다. 옵션: `Yes` / `No` |
| [!UICONTROL Add Block Class Type to Hints] | 스토어 뷰 | 템플릿 경로 힌트에 블록 이름을 포함합니다. 옵션: `Yes` / `No` |

{:style=&quot;table-layout:auto&quot;}

## [!UICONTROL Translate Inline]

![인라인 번역](./assets/developer-translate-inline.png)<!-- zoom -->

이러한 설정 변경에 대한 자세한 내용은 [인라인 번역](../../systems/developer-tools.md#translate-inline) 다음에서 _관리 시스템 안내서_.

| 필드 | [범위](../../getting-started/websites-stores-views.md#scope-settings) | 설명 |
|--- |--- |--- |
| [!UICONTROL Enable for Storefront] | 스토어 뷰 | 상점 첫 화면의 인라인 번역기를 활성화합니다. 각 스토어 보기에 대해 인터페이스 텍스트를 편집할 수 있습니다. 라이브 스토어를 방해하지 않고 인라인 번역기를 사용하려면 개발자 클라이언트 제한 허용 목록에 추가하다에 IP 주소를 추가하십시오. |
| [!UICONTROL Enable for Admin] | 글로벌 | 관리자용 인라인 번역기를 활성화합니다. 상점 첫 페이지와는 달리 관리자는 여러 언어로 번역할 수 없습니다. 그러나 필드 레이블과 인터페이스의 다른 텍스트는 변경될 수 있습니다. |

{:style=&quot;table-layout:auto&quot;}

## [!UICONTROL JavaScript Settings]

![JavaScript 설정](./assets/developer-javascript-settings.png)<!-- zoom -->

이러한 설정 변경에 대한 자세한 내용은 [리소스 파일 최적화 중](../../systems/developer-tools.md#optimizing-resource-files) 다음에서 _관리 시스템 안내서_.

| 필드 | [범위](../../getting-started/websites-stores-views.md#scope-settings) | 설명 |
|--- |--- |--- |
| [!UICONTROL Merge JavaScript Files] | 스토어 뷰 | 여러 JavaScript 파일을 단일 파일로 병합하여 페이지 로드 시간을 개선합니다. |
| [!UICONTROL Enable JavaScript Bundling] | 스토어 뷰 | 여러 JavaScript 파일을 하나의 파일에 번들로 제공할 수 있는지 여부를 결정합니다. 옵션: `Yes` / `No` |
| [!UICONTROL Minify JavaScript Files] | 스토어 뷰 | 불필요한 문자, 공백 및 들여쓰기를 제거하여 코드의 크기를 줄입니다. |
| [!UICONTROL Move JS code to the bottom of the page] | 글로벌 | 활성화되면 JS 코드를 페이지 맨 아래로 이동합니다. 옵션: `Yes` / `No` |
| [!UICONTROL Translation Strategy] | 글로벌 | 시스템에서 사용하는 변환 방법을 결정합니다. 옵션: <br/>**`Dictionary`**- 상점 첫 화면에서 번역.<br/>**`Embedded`** - 관리자 측에서의 번역. |
| [!UICONTROL Log JS Errors to Session Storage] | 글로벌 | 활성화된 경우 보고용 기능 테스트에서 사용할 수 있습니다. 옵션: `Yes` / `No` |
| [!UICONTROL Log JS Errors to Session Storage Key] | 글로벌 | 수집된 js 오류를 검색하는 데 사용되는 키를 식별합니다. |

{:style=&quot;table-layout:auto&quot;}

## [!UICONTROL CSS Settings]

![CSS 설정](./assets/developer-css-settings.png)<!-- zoom -->

이러한 설정 변경에 대한 자세한 내용은 [리소스 파일 최적화 중](../../systems/developer-tools.md#optimizing-resource-files) 다음에서 _관리 시스템 안내서_.

| 필드 | [범위](../../getting-started/websites-stores-views.md#scope-settings) | 설명 |
|--- |--- |--- |
| [!UICONTROL Merge CSS Files] | 스토어 뷰 | 여러 CSS 파일을 단일 파일로 병합하여 페이지 로드 시간을 개선합니다. 옵션: `Yes` / `No` |
| [!UICONTROL Minify CSS Files] | 스토어 뷰 | 불필요한 문자, 공백 및 들여쓰기를 제거하여 코드의 크기를 줄입니다. 옵션: `Yes` / `No` |
| [!UICONTROL Use CSS critical path] | 글로벌 | 다음 _CSS 중요 경로_ 에서 축소된 중요한 CSS 인라인을 제공합니다. `<head>` 비동기적으로 로드되는 모든 중요하지 않은 스타일을 지웁니다. 옵션: `Yes` / `No` |

{:style=&quot;table-layout:auto&quot;}

## [!UICONTROL Image Processing Settings]

![이미지 처리 설정](./assets/developer-image-processing-settings.png)<!-- zoom -->

| 필드 | [범위](../../getting-started/websites-stores-views.md#scope-settings) | 설명 |
|--- |--- |--- |
| [!UICONTROL Image Adapter] | 글로벌 | 이미지를 렌더링하는 데 사용할 어댑터를 지정합니다. 어댑터 설정을 변경한 후 카탈로그 이미지 캐시를 플러시합니다. 옵션: `PHP GD2` / `ImageMagick` <br/><br/>**_참고:_**ICO 파일 형식은 ImageMagick 어댑터에서만 지원됩니다. |

{:style=&quot;table-layout:auto&quot;}

## [!UICONTROL Caching Settings]

![캐싱 설정](./assets/developer-cache-settings.png)<!-- zoom -->

| 필드 | [범위](../../getting-started/websites-stores-views.md#scope-settings) | 설명 |
|--- |--- |--- |
| [!UICONTROL Cache User Defined Attributes] | 글로벌 | 활성화되면 사용자 정의 및 시스템 EAV(엔티티 속성 값) 속성을 캐시합니다. 이 옵션을 사용하면 성능이 향상될 수 있지만 캐싱을 위한 추가 공간이 필요합니다. 옵션: `Yes` / `No` |

{:style=&quot;table-layout:auto&quot;}

## [!UICONTROL Static Files Settings]

![정적 파일 설정](./assets/developer-static-files-settings.png)<!-- zoom -->

| 필드 | [범위](../../getting-started/websites-stores-views.md#scope-settings) | 설명 |
|--- |--- |--- |
| [!UICONTROL Sign Static Files] | 글로벌 | 활성화되면 는 정적 파일의 URL에 디지털 서명을 추가하여 브라우저가 파일의 최신 버전을 사용할 수 있는 시기를 감지할 수 있도록 합니다. 파일의 서명이 브라우저의 캐시에 저장된 것과 다른 경우 파일의 최신 버전이 사용됩니다. 서명할 수 있는 정적 파일에는 JavaScript, CSS, 이미지 및 글꼴이 포함됩니다. 옵션: `Yes` / `No` |

{:style=&quot;table-layout:auto&quot;}

## [!UICONTROL Grid Settings]

![그리드 설정](./assets/developer-grid-settings.png)<!-- zoom -->

| 필드 | [범위](../../getting-started/websites-stores-views.md#scope-settings) | 설명 |
|--- |--- |--- |
| [!UICONTROL Asynchronous Indexing|Global] | 주문, 송장, 선적 및 대변 메모와 같은 주문 처리 시스템 개체가 그리드에 추가되고 다시 색인화되는 시기를 결정합니다. 비동기 인덱싱을 사용하여 저장 작업 중에 데이터가 잠기지 않도록 하고 처리 시간을 줄일 수 있습니다. 옵션: <br/>**`Disable`**- (기본값) 주문 관련 엔티티가 다양한 시간에 그리드에 추가됩니다. 저장됨.<br/>**`Enable`** - 주문 관련 엔티티는 예약된 cron 작업 중에만 그리드에 추가됩니다. Cron은 1분에 한 번 실행되도록 구성해야 합니다. |

{:style=&quot;table-layout:auto&quot;}
