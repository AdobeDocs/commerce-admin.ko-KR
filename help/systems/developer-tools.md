---
title: 개발자 도구
description: 사용자 지정 프로젝트에서 작업하는 개발자를 지원하는 데 사용할 수 있는 고급 개발자 도구에 대해 알아봅니다.
exl-id: 34529aa9-201f-4817-b53b-a15b6a78a923
role: Admin, Developer
source-git-commit: 64ccc2d5016e915a554c2253773bb50f4d33d6f4
workflow-type: tm+mt
source-wordcount: '1711'
ht-degree: 0%

---

# 개발자 도구

고급 도구를 사용하여 프론트엔드 개발 모드를 결정하고, IP 주소 허용 목록 중 개발자 및 템플릿 경로 힌트를 표시합니다. 상점 및 관리자의 인터페이스에서 텍스트를 쉽게 스팟 변경할 수 있는 도구도 있습니다.

- [작업 로그](action-log.md) ![Adobe Commerce](../assets/adobe-logo.svg) (Adobe Commerce 전용)
- [프론트엔드 개발 워크플로](#frontend-development-workflow)
- [정적 파일 서명 사용](#static-file-signatures)
- [리소스 파일 최적화](#optimizing-resource-files)
- [개발자 클라이언트 제한 사항](#client-restrictions)
- [템플릿 경로 힌트](#template-path-hints)
- [인라인 번역](#translate-inline)

## 작업 모드

Adobe Commerce 또는 Magento Open Source 인스턴스를 배포하여 다음 중 하나에서 실행할 수 있습니다. _production_ 또는 _개발자 모드_. 개발자를 위해 특별히 설계된 도구 및 구성 설정은에서 스토어가 실행되는 동안에만 액세스할 수 있습니다. _개발자 모드_.

적절한 권한이 있는 사용자가 서버의 명령줄에서만 작업 모드를 변경할 수 있습니다. 다음을 참조하십시오 [작업 모드 설정](https://experienceleague.adobe.com/docs/commerce-operations/configuration-guide/cli/set-mode.html) 다음에서 _구성 안내서_ 추가 정보.

판매자 설명서의 대부분의 항목은 프로덕션 모드에서 실행되는 상거래 인스턴스에 적용됩니다. 그러나 다음 구성 설정 및 도구는 설치가 개발자 모드에서 실행되는 경우에만 사용할 수 있습니다.

## 프론트엔드 개발 워크플로

프론트엔드 개발 워크플로 유형은 개발 중에 클라이언트측에서 컴파일이 적게 발생하는지 또는 서버측에서 컴파일이 적게 발생하는지를 결정합니다. 추가 기능 및 규칙이 있고 간소화된 코드를 생성하는 CSS의 확장이 더 적습니다. 테마 개발에는 클라이언트측 컴파일 작업을 사용하지 않는 것이 좋습니다. 서버 측 컴파일이 기본 모드입니다. 프로덕션 모드의 저장소에는 개발 워크플로우 옵션을 사용할 수 없습니다.
다음을 참조하십시오 [클라이언트측 LESS 컴파일과 서버측 비교](https://developer.adobe.com/commerce/frontend-core/guide/css/quickstart/compilation-mode/)Commerce 개발자 설명서에서 {:target=&quot;_blank&quot;}.

>[!NOTE]
>
>프론트엔드 개발 워크플로 구성은에서 사용할 수 있습니다. [개발자 모드](../systems/developer-tools.md#operation-modes) 만 해당.

![고급 구성 - 프론트엔드 개발 워크플로](../configuration-reference/advanced/assets/developer-frontend-development-workflow.png){width="600" zoomable="yes"}

1. 다음에서 _관리자_ 사이드바, 이동 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. 왼쪽 패널에서 를 확장합니다. **[!UICONTROL Advanced]** 및 선택 **[!UICONTROL Developer]**.

1. 확장 ![확장 선택기](../assets/icon-display-expand.png) 다음 **[!UICONTROL Front-end Development Workflow]** 섹션.

1. 설정 **[!UICONTROL Workflow Type]** 다음 중 하나를 수행합니다.

   - `Client side less compilation` - 브라우저의 기본 파일을 사용하여 컴파일 `less.js` 라이브러리입니다.
   - `Server side less compilation` - 컴파일은 Less PHP 라이브러리를 사용하여 서버에서 발생합니다. 프로덕션 기본 모드입니다.

1. 완료되면 다음을 클릭하십시오. **[!UICONTROL Save Config]**.

## 정적 파일 서명

정적 파일의 URL에 디지털 서명을 추가하면 브라우저는 파일의 최신 버전을 사용할 수 있는 시기를 감지할 수 있습니다. 디지털 서명으로 추적할 수 있는 정적 파일에는 JavaScript, CSS, 이미지 및 글꼴이 포함됩니다. 서명은 기본 URL 바로 뒤에 경로에 추가됩니다. 파일의 서명이 브라우저의 캐시에 저장된 것과 다른 경우 파일의 최신 버전이 사용됩니다.

다음을 참조하십시오 [정적 콘텐츠 서명](https://experienceleague.adobe.com/docs/commerce-operations/configuration-guide/cache/static-content-signing.html)Commerce 개발자 설명서에서 {:target=&quot;_blank&quot;}.

>[!NOTE]
>
>정적 파일 설정 구성은에서 작업할 때만 사용할 수 있습니다. [개발자 모드](../systems/developer-tools.md#operation-modes).

![고급 구성 - 정적 파일 설정](../configuration-reference/advanced/assets/developer-static-files-settings.png){width="600" zoomable="yes"}

구성 설정에 대한 자세한 목록이 필요하면 를 참조하십시오. [_정적 파일 설정_](../configuration-reference/advanced/developer.md) 다음에서 _구성 참조_.

**_서명된 정적 파일을 활성화하려면_**

1. 다음에서 _관리자_ 사이드바, 이동 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. 왼쪽 패널에서 를 확장합니다. **[!UICONTROL Advanced]** 및 선택 **[!UICONTROL Developer]**.

1. 확장 ![확장 선택기](../assets/icon-display-expand.png) 다음 **[!UICONTROL Static Files Settings]** 섹션.

1. 설정 **[!UICONTROL Sign Static Files]** 끝 `Yes`.

1. 완료되면 다음을 클릭하십시오. **[!UICONTROL Save Config]**.

## 리소스 파일 최적화

파일을 병합하고 번들로 묶어 코드를 최소화함으로써 리소스 파일을 로드하는 데 걸리는 시간을 줄일 수 있습니다.

- 병합하면 동일한 유형의 개별 파일이 단일 파일로 결합됩니다.
- 번들링 은 페이지를 로드하는 데 필요한 HTTP 요청 수를 줄이기 위해 개별 파일을 그룹화하는 기술입니다.
- 축소는 공백, 줄 바꿈 및 주석을 제거하지만 코드의 기능에는 영향을 주지 않습니다. 최소화된 파일은 편집할 수 없으므로 프로덕션으로 이동할 준비가 된 경우에만 프로세스를 적용해야 합니다.

기본적으로 Adobe Commerce 및 Magento Open Source은 파일을 병합, 번들 또는 최소화하지 않으며 프로젝트 개발자가 사용해야 하는 파일 최적화 방법을 결정해야 합니다.

다음을 참조하십시오 [성능 모범 사례](https://experienceleague.adobe.com/docs/commerce-operations/performance-best-practices/overview.html) 추가 정보.

>[!NOTE]
>
>CSS 및 JavaScript 파일은에서 최적화할 수 있습니다. [개발자 모드](../systems/developer-tools.md#operation-modes) 만 해당.

| 파일 유형 | 지원되는 작업 |
| --------------- | -------------------- |
| CSS 파일 | `MergeMinify` |
| JavaScript 파일 | `MergeBundleMinify` |
| 템플릿 파일 | `Minify` |

{style="table-layout:auto"}

**_리소스 파일을 최적화하려면 다음을 수행합니다._**

1. 다음에서 _관리자_ 사이드바, 이동 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. 왼쪽 패널에서 를 확장합니다. **[!UICONTROL Advanced]** 및 선택 **[!UICONTROL Developer]**.

1. CSS 파일을 최적화하려면 ![확장 선택기](../assets/icon-display-expand.png) 다음 **[!UICONTROL CSS Settings]** 섹션을 참조하고 다음을 수행합니다.

   - 설정 **[!UICONTROL Merge CSS Files]** 끝 `Yes`.
   - 설정 **[!UICONTROL Minify CSS Files]** 끝 `Yes`.

   ![고급 구성 - CSS 설정](../configuration-reference/advanced/assets/developer-css-settings.png){width="600" zoomable="yes"}

[_CSS 설정_](../configuration-reference/advanced/developer.md)

1. JavaScript 파일을 최적화하려면 를 확장합니다. ![확장 선택기](../assets/icon-display-expand.png) 다음 **[!UICONTROL JavaScript Settings]** 섹션을 참조하고 다음을 수행합니다.

   - 설정 **[!UICONTROL Merge JavaScript Files]** 끝 `Yes`.
   - 설정 **[!UICONTROL Minify JavaScript Files]** 끝 `Yes`.

   ![고급 구성 - JavaScript 설정](../configuration-reference/advanced/assets/developer-javascript-settings.png){width="600" zoomable="yes"}

1. PHTML 템플릿 파일을 축소하려면 ![확장 선택기](../assets/icon-display-expand.png) 다음 **[!UICONTROL Template Settings]** 섹션 및 세트 **[!UICONTROL Minify Html]** 끝 `Yes`.

   ![고급 구성 - 템플릿 설정](../configuration-reference/advanced/assets/developer-template-settings.png){width="600" zoomable="yes"}

1. 완료되면 다음을 클릭하십시오. **[!UICONTROL Save Config]**.

## 클라이언트 제한 사항

다음과 같은 도구를 사용하기 전에 [템플릿 경로 힌트](#template-path-hints)허용 목록에 추가하다 를 설치한 후 스토어에서 고객의 쇼핑 경험이 중단되는 것을 방지하기 위해 개발자 클라이언트 Restrictions에 IP 주소를 추가해야 합니다. IP 주소를 모르면 온라인에서 검색할 수 있습니다.

>[!NOTE]
>
>Developer Client Restrictions는에서 설정할 수 있습니다. [개발자 모드](../systems/developer-tools.md#operation-modes) 만 해당.

기술 정보는 다음을 참조하십시오. [요청을 허용하기 위한 사용자 지정 VCL](https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/cdn/custom-vcl-snippets/fastly-vcl-allowlist.html) 다음에서 _클라우드 인프라의 Commerce 안내서_.

**_IP 주소를 허용 목록에 추가하려면:_**

1. 다음에서 _관리자_ 사이드바, 이동 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. 왼쪽 패널에서 를 확장합니다. **[!UICONTROL Advanced]** 및 선택 **[!UICONTROL Developer]**.

1. 확장 ![확장 선택기](../assets/icon-display-expand.png) 다음 **[!UICONTROL Developer Client Restrictions]** 섹션.

   ![고급 구성 - 개발자 클라이언트 제한 사항](../configuration-reference/advanced/assets/developer-developer-client-restrictions.png){width="600" zoomable="yes"}

1. 대상 **[!UICONTROL Allow IPs]** IP 주소를 입력합니다.

   여러 IP 주소에서 액세스해야 하는 경우 쉼표로 각각 구분하십시오.

1. 완료되면 다음을 클릭하십시오. **[!UICONTROL Save Config]**.

1. 메시지가 표시되면 잘못된 캐시를 새로 고칩니다.

## 템플릿 경로 힌트

템플릿 경로 힌트는 페이지에서 사용되는 각 템플릿에 경로와 함께 표기법을 추가하는 진단 도구입니다. 상점 또는 관리자에 대해 템플릿 경로 힌트를 활성화할 수 있습니다.

>[!NOTE]
>
>템플릿 경로 힌트는에서 편집할 수 있습니다. [개발자 모드](../systems/developer-tools.md#operation-modes) 만 해당.

다음을 참조하십시오 [템플릿, 레이아웃 및 스타일 찾기](https://developer.adobe.com/commerce/frontend-core/guide/themes/debug/)Commerce 개발자 설명서에서 {:target=&quot;_blank&quot;}.

![예제 storefront - 템플릿 경로 힌트](./assets/storefront-template-path-hints.png){width="700" zoomable="yes"}

### 단계 1: 허용 목록에 추가하다에 IP 주소 추가

템플릿 경로 힌트를 사용하기 전에 IP 주소를 [허용 목록](#client-restrictions) 상점에서 쇼핑하는 손님에게 방해가 되지 않도록 하기 위해서. 완료되면 상거래 캐시를 지워 저장소에서 모든 힌트를 제거해야 합니다.

![고급 구성 - 개발자 클라이언트 제한 사항](../configuration-reference/advanced/assets/developer-developer-client-restrictions.png){width="600" zoomable="yes"}

### 2단계: 템플릿 경로 힌트 활성화

1. 다음에서 _관리자_ 사이드바, 이동 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. 왼쪽 패널에서 를 확장합니다. **[!UICONTROL Advanced]** 및 선택 **[!UICONTROL Developer]**.

1. 확장 ![확장 선택기](../assets/icon-display-expand.png) 다음 **[!UICONTROL Debug]** 섹션을 참조하고 다음을 수행합니다.

   ![고급 구성 - 디버그](../configuration-reference/advanced/assets/developer-debug.png){width="600" zoomable="yes"}

   - 저장소에 대한 템플릿 경로 힌트를 활성화하려면 다음을 설정하십시오. **[!UICONTROL Enabled Template Path Hints for Storefront]** 끝 `Yes`.

   - URL에 다음이 포함된 경우에만 저장소에 대한 템플릿 경로 힌트를 활성화하려면 `templatehints` 매개 변수, 설정 **URL 매개 변수로 Storefront에 대한 힌트 활성화** 끝 `Yes`. 그런 다음 필요한 경우 매개 변수의 값을 설정합니다. 기본값은 입니다. `magento`, 하지만 사용자 지정 값을 사용할 수 있습니다. 예를 들어 값을 로 변경하는 경우 `lorem`, 다음을 사용합니다. `mymagento.com?templatehints=lorem` 템플릿 힌트를 표시합니다.

   - 관리자에 대한 템플릿 경로 힌트를 활성화하려면 다음을 설정하십시오. **[!UICONTROL Enabled Template Path Hints for Admin]** 끝 `Yes`.

   - 블록 이름을 포함하려면 를 설정합니다. **[!UICONTROL Add Block Class Type to Hints]** 끝 `Yes`.

1. 완료되면 다음을 클릭하십시오. **[!UICONTROL Save Config]**.

### 3단계: 캐시 지우기

1. 다음에서 _관리자_ 사이드바, 이동 **[!UICONTROL System]** > _[!UICONTROL Tools]_>**[!UICONTROL Cache Management]**.

1. 오른쪽 위 모서리에서 을(를) 클릭합니다. **[!UICONTROL Flush Magento Cache]**.

## 인라인 번역

에서 인라인 번역 도구를 사용할 수 있습니다. [개발자 모드](../systems/developer-tools.md#operation-modes) 을 입력하여 인터페이스에서 텍스트를 터치하여 사용자의 음성 및 브랜드를 반영합니다. 인라인 번역 모드가 활성화되면 편집할 수 있는 페이지의 모든 텍스트가 빨간색으로 윤곽선이 표시됩니다. 상점 및 관리자 전체에 표시되는 필드 레이블, 메시지 및 기타 텍스트를 쉽게 편집할 수 있습니다. 예를 들어 많은 테마는 다음과 같은 용어를 사용합니다. _내 계정_, _내 위시리스트_, 및 _내 대시보드_&#x200B;고객이 자신의 진로를 찾을 수 있도록 지원합니다. 하지만, 여러분은 단순히 그 단어들을 사용하는 것을 더 선호할 수도 있어요 _계정_, _위시리스트_, 및 _대시보드_.

>[!NOTE]
>
>인라인 번역 도구는 에서 작업할 때만 사용할 수 있습니다. [개발자 모드](../systems/developer-tools.md#operation-modes).

다음을 참조하십시오 [번역 개요](https://developer.adobe.com/commerce/frontend-core/guide/translations/) Commerce 개발자 설명서에서 참조하십시오.

![예제 storefront - 변환 가능한 텍스트](./assets/storefront-translate-inline.png){width="700" zoomable="yes"}

스토어를 여러 언어로 사용할 수 있는 경우 로케일에 대한 번역된 텍스트를 세밀하게 조정할 수 있습니다. 서버에서 인터페이스 텍스트는 각 출력 블록에 대해 별도의 CSV 파일로 유지 관리되며 로케일로 구성됩니다. 대체 접근 방식으로 _인라인 번역_ 도구에서 서버에서 직접 CSV 파일을 편집할 수도 있습니다. 번역 파일은에 저장됩니다. `app/code/Magento/<module_name>/i18n/<language_locale>.csv`.

>[!NOTE]
>
>인라인 번역 도구를 사용하려면 브라우저에서 팝업을 허용해야 합니다.

### 1단계: 출력 캐시 비활성화

1. 다음에서 _관리자_ 사이드바, 이동 **[!UICONTROL System]** > _[!UICONTROL Tools]_>**[!UICONTROL Cache Management]**.

1. 다음 확인란을 선택합니다.

   - `Blocks HTML output`
   - `Page Cache`
   - `Translations`

1. 설정 **[!UICONTROL Actions]** 제어 대상 `Disable` 및 클릭 **[!UICONTROL Submit]**.

### 2단계: 인라인 번역 도구 활성화

1. 다음에서 _관리자_ 사이드바, 이동 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. 특정 스토어 보기로 작업하려면 **[!UICONTROL Store View]** 업데이트해야 합니다.

1. 왼쪽 패널에서 를 확장합니다. **[!UICONTROL Advanced]** 및 선택 **[!UICONTROL Developer]**.

1. 확장 ![확장 선택기](../assets/icon-display-expand.png) 다음 **[!UICONTROL Translate Inline]** 섹션.

   지우기 **[!UICONTROL Use Website]** 확인란을 선택하여 설정을 수정할 수 있습니다.

   다음 _[!UICONTROL Enabled for Admin]_특정 스토어 보기를 편집할 때는 옵션을 사용할 수 없습니다.

   ![고급 구성 - 인라인 번역](../configuration-reference/advanced/assets/developer-translate-inline.png){width="600" zoomable="yes"}

1. 설정 **[!UICONTROL Enabled for Storefront]** 끝 `Yes`.

1. 완료되면 다음을 클릭하십시오. **[!UICONTROL Save Config]**.

1. 메시지가 표시되면 유효하지 않은 캐시를 새로 고치지만 비활성화된 캐시는 그대로 둡니다.

### 3단계: 텍스트 업데이트

1. 브라우저에서 상점을 열고 편집할 페이지로 이동합니다.

   필요한 경우 언어 선택기를 사용하여 스토어 보기를 변경합니다. 번역할 수 있는 각 텍스트 문자열은 빨간색으로 윤곽선이 표시됩니다. 텍스트 상자 위로 마우스를 가져가면 책 아이콘( ![책 아이콘](../assets/icon-book.png) )가 표시됩니다.

1. 책 아이콘을 클릭하여 _번역_ 창을 열고 다음을 수행합니다.

   - 특정 스토어 보기에 대한 변경 사항인 경우 **[!UICONTROL Store View Specific]** 확인란.

   - 새 항목 입력 **[!UICONTROL Custom]** 텍스트를 입력하십시오.

1. 완료되면 다음을 클릭하십시오. **[!UICONTROL Submit]**.

   ![사용자 정의 텍스트 입력](./assets/storefront-translate-inline-detail.png){width="700" zoomable="yes"}

1. 스토어에서 변경 사항을 보려면 브라우저를 새로 고치십시오.

1. 변경할 저장소의 모든 요소에 대해 이 프로세스를 반복합니다.

### 4단계: 원래 설정 복원

1. 스토어의 관리자로 돌아갑니다.

1. 다음에서 _관리자_ 사이드바, 이동 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. 설정 **[!UICONTROL Store View]** 을 추가하여 편집한 특정 보기에 대해 이해할 수 있습니다.

1. 왼쪽 패널에서 를 확장합니다. **[!UICONTROL Advanced]** 및 선택 **[!UICONTROL Developer]**.

1. 확장 ![확장 선택기](../assets/icon-display-expand.png) 다음 **[!UICONTROL Translate Inline]** 섹션.

1. 설정 **[!UICONTROL Enabled for Frontend]** 끝 `No`.

1. 완료되면 다음을 클릭하십시오. **[!UICONTROL Save Config]**.

1. 다음에서 _관리자_ 사이드바, 이동 **[!UICONTROL System]** > _[!UICONTROL Tools]_>**[!UICONTROL Cache Management]**.

1. 이전에 비활성화되었던 다음 출력 캐시의 확인란을 선택합니다.

   - `Blocks HTML output`
   - `Page Cache`
   - `Translations`

1. 설정 **[!UICONTROL Actions]** 제어 대상 `Enable` 및 클릭 **[!UICONTROL Submit]**.

1. 메시지가 표시되면 잘못된 캐시를 새로 고칩니다.

### 5단계: 스토어에서 변경 사항 확인

상점으로 이동하여 업데이트된 각 페이지를 검사하여 변경 사항이 올바른지 확인하십시오. 이 예에서는 `Customer Login` 이(가) (으)로 변경되었습니다. `Customer Sign In`. 특정 보기가 변경된 경우 언어 선택기를 사용하여 올바른 보기로 전환합니다.

![예제 storefront - 번역된 고객 로그인](./assets/storefront-translate-inline-customer-sign-in.png){width="700" zoomable="yes"}
