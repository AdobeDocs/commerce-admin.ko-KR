---
title: 페이지 설정
description: 저장소 페이지의 기본 부분에 대한 기본값을 구성하는 방법에 대해 알아봅니다.
exl-id: a4310940-0d4f-4948-a271-382f03905bfd
badgePaas: label="PaaS만" type="Informative" url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="Adobe Commerce 온 클라우드 프로젝트(Adobe 관리 PaaS 인프라) 및 온프레미스 프로젝트에만 적용됩니다."
source-git-commit: 57a913b21f4cbbb4f0800afe13012ff46d578f8e
workflow-type: tm+mt
source-wordcount: '959'
ht-degree: 0%

---

# 페이지 설정

페이지의 기본 섹션은 부분적으로 표준 HTML 태그 세트에 의해 제어됩니다. 이러한 태그 중 일부는 페이지의 각 섹션에서 사용되는 글꼴, 색상, 크기, 배경색 및 이미지의 선택을 결정하는 데 사용할 수 있습니다. 기타 설정은 머리글의 로고 및 바닥글의 저작권 표시와 같은 페이지 요소를 제어합니다. 이러한 섹션은 HTML 페이지의 기본 구조에 해당하며 대부분의 기본 속성은 관리자에서 설정할 수 있습니다.

- [HTML 헤드](#html-head)
- [머리글](#header)
- [바닥글](#footer)

![HTML 페이지 섹션](./assets/storefront-home-html-inspect.png){width="700" zoomable="yes"}

## HTML 헤드

HTML Head 섹션의 설정은 HTML 페이지의 `<head>` 태그에 해당하며 각 스토어 보기에 대해 구성할 수 있습니다. 페이지 제목, 설명 및 키워드에 대한 메타데이터 외에도 섹션에는 favicon 및 기타 스크립트에 대한 링크가 포함되어 있습니다. 검색 엔진 로봇에 대한 지침 및 스토어 데모 알림의 표시도 이 섹션에서 구성됩니다.

### HTML 헤드 구성

1. _관리자_ 사이드바에서 **[!UICONTROL Content]** > _[!UICONTROL Design]_>**[!UICONTROL Configuration]**(으)로 이동합니다.

1. 구성할 저장소 보기를 찾은 다음 _[!UICONTROL Action]_열에서&#x200B;**[!UICONTROL Edit]**을(를) 클릭합니다.

1. _기타 설정_&#x200B;에서 **[!UICONTROL HTML Head]** 섹션의 ![확장 선택기](../assets/icon-display-expand.png)을 확장합니다.

   ![HTML 헤드 구성 설정](./assets/configuration-html-head.png){width="500" zoomable="yes"}

1. 필요한 경우 [favicon](../getting-started/storefront-branding.md#add-a-favicon)을 업데이트하십시오.

1. 필요에 따라 페이지 제목 설정을 업데이트합니다.

   - **[!UICONTROL Default Page Title]**
   - **[!UICONTROL Page Title Prefix]**
   - **[!UICONTROL Page Title Suffix]**

   기본 제목에 접미사 및/또는 접두사를 사용하여 두 부분 또는 세 부분 제목을 생성할 수 있습니다. 접두사 또는 접미사와 기본 제목 사이에 세로 막대 또는 콜론을 구분 기호로 추가할 수 있습니다.

1. SEO(검색 엔진 최적화)를 지원하고 고객이 검색 결과에서 매장으로 이동할 수 있도록 도와주는 메타데이터를 추가하거나 수정합니다.

   - **[!UICONTROL Default Meta Description]**
   - **[!UICONTROL Default Meta Keywords]**

1. 필요에 따라 **[!UICONTROL Scripts and Style Sheets]**&#x200B;을(를) 입력합니다.

   >[!NOTE]
   >
   >[!UICONTROL Scripts and Style Sheets] 필드에 입력한 모든 JavaScript은 CSP(콘텐츠 보안 정책) 설정에서 화이트리스트에 추가되어야 합니다. 그렇지 않으면 체크아웃 페이지에서 실행되지 않습니다. 자세한 내용은 [콘텐츠 보안 정책](https://developer.adobe.com/commerce/php/development/security/content-security-policies)을 참조하세요.


1. 필요한 경우 [데모 스토어 알림](../getting-started/storefront-branding.md#set-the-store-demo-notice)을 활성화하거나 비활성화합니다.

1. 완료되면 **[!UICONTROL Save Configuration]**&#x200B;을(를) 클릭합니다.

### HTML Head 필드 설명

| 필드 | 범위 | 설명 |
|--- |--- |--- |
| [!UICONTROL Favicon Icon] | 스토어 뷰 | 브라우저의 주소 표시줄과 탭에 나타나는 작은 그래픽 이미지를 업로드합니다. 허용되는 파일 형식: ICO, PNG, APNG, GIF 및 JPG(JPEG). 모든 브라우저가 이러한 형식을 지원하는 것은 아닙니다. |
| [!UICONTROL Default Page Title] | 스토어 뷰 | 브라우저에서 볼 때 각 페이지의 제목 표시줄에 나타나는 제목입니다. 개별 페이지에 대해 다른 제목을 지정하지 않는 한 모든 페이지에 기본 제목이 사용됩니다. |
| [!UICONTROL Page Title Prefix] | 스토어 뷰 | 제목 앞에 접두사를 추가하여 2부분 또는 3부분 제목을 만들 수 있습니다. 주 제목의 텍스트와 구분하기 위해 접두어 끝에 세로 막대 또는 콜론을 구분 기호로 사용할 수 있습니다. |
| [!UICONTROL Page Title Suffix] | 스토어 뷰 | 제목 뒤에 접미사를 추가하여 두 부분 또는 세 부분 제목을 만들 수 있습니다. 주 제목의 텍스트와 구분하기 위해 접두어 끝에 세로 막대 또는 콜론을 구분 기호로 사용할 수 있습니다. |
| [!UICONTROL Default Meta Description] | 스토어 뷰 | 설명은 검색 엔진 목록에 대한 사이트 요약을 제공하며 길이는 160자를 초과할 수 없습니다. |
| [!UICONTROL Default Meta Keywords] | 스토어 뷰 | 저장소를 설명하는 일련의 키워드로서, 각각 쉼표로 구분됩니다. |
| [!UICONTROL Scripts and Style Sheets] | 스토어 뷰 | `<head>` 태그를 닫기 전에 HTML에 포함해야 하는 스크립트를 포함합니다. 예를 들어 `<body>` 태그 앞에 배치해야 하는 모든 서드파티 JavaScript을 여기에 입력할 수 있습니다. |
| [!UICONTROL Display Demo Store Notice] | 스토어 뷰 | 페이지 상단에 있는 데모 스토어 알림 표시를 제어합니다. 옵션: `Yes` / `No` |

{style="table-layout:auto"}

## 머리글

헤더 구성은 스토어 로고 경로를 식별하고 로고 대체 텍스트 및 환영 메시지를 지정합니다.

![헤더 구성 설정](./assets/configuration-header.png){width="400" zoomable="yes"}

### 헤더 구성

1. _관리자_ 사이드바에서 **[!UICONTROL Content]** > _[!UICONTROL Design]_>**[!UICONTROL Configuration]**(으)로 이동합니다.

1. 구성할 저장소 보기를 찾은 다음 _[!UICONTROL Action]_열에서&#x200B;**[!UICONTROL Edit]**을(를) 클릭합니다.

1. _기타 설정_&#x200B;에서 **[!UICONTROL Header]** 섹션의 ![확장 선택기](../assets/icon-display-expand.png)을 확장합니다.

1. 스토어 보기에 필요한 변경 작업을 수행합니다.

   - [로고](../getting-started/storefront-branding.md#upload-your-logo) 설정
   - [환영 메시지](../getting-started/storefront-branding.md#change-the-welcome-message) 설정

1. 완료되면 **[!UICONTROL Save Configuration]**&#x200B;을(를) 클릭합니다.

### 헤더 필드 설명

| 필드 | 범위 | 설명 |
|--- |--- |--- |
| [!UICONTROL Logo Image] | 스토어 뷰 | 헤더에 나타나는 로고 경로를 식별합니다. 지원되는 파일 유형: PNG, GIF, JPG(JPEG) |
| [!UICONTROL Logo Attribute Width] | 스토어 뷰 | 로고 이미지의 너비(픽셀 단위)입니다. |
| [!UICONTROL Logo Attribute Height] | 스토어 뷰 | 로고 이미지의 높이(픽셀 단위)입니다. |
| [!UICONTROL Welcome Text] | 스토어 뷰 | 시작 메시지는 페이지 헤더에 표시되며 로그인한 고객의 이름이 포함됩니다. |
| [!UICONTROL Logo Image Alt] | 스토어 뷰 | 로고와 연결된 대체 텍스트입니다. |
| [!UICONTROL Translate Title] | 스토어 뷰 | `Page Title` 또는 `Meta Title`을(를) 변환할지 여부를 결정합니다. |

{style="table-layout:auto"}

## 바닥글

바닥글 구성 섹션에서는 페이지 하단에 나타나는 [저작권 공지](../getting-started/storefront-branding.md#change-the-copyright-notice)를 업데이트하고, 닫는 `<body>` 태그 앞에 배치해야 하는 기타 스크립트를 입력할 수 있습니다.

![바닥글 구성 설정](./assets/configuration-footer.png){width="400" zoomable="yes"}

### 바닥글 구성

1. _관리자_ 사이드바에서 **[!UICONTROL Content]** > _[!UICONTROL Design]_>**[!UICONTROL Configuration]**(으)로 이동합니다.

1. 구성할 저장소 보기를 찾은 다음 _[!UICONTROL Action]_열에서&#x200B;**[!UICONTROL Edit]**을(를) 클릭합니다.

1. _기타 설정_&#x200B;에서 **[!UICONTROL Footer]** 섹션의 ![확장 선택기](../assets/icon-display-expand.png)을 확장합니다.

1. **[!UICONTROL Copyright]** 및 **[!UICONTROL Miscellaneous HTML]** 설정에 필요한 변경 작업을 수행합니다.

   >[!NOTE]
   >
   >[!UICONTROL Miscellaneous HTML] 필드에 입력한 모든 JavaScript은 CSP(콘텐츠 보안 정책) 설정에서 화이트리스트에 추가되어야 합니다. 그렇지 않으면 체크아웃 페이지에서 실행되지 않습니다. 자세한 내용은 [콘텐츠 보안 정책](https://developer.adobe.com/commerce/php/development/security/content-security-policies)을 참조하세요.

1. 완료되면 **[!UICONTROL Save Configuration]**&#x200B;을(를) 클릭합니다.

## 바닥글 필드 설명

| 필드 | 범위 | 설명 |
|--- |--- |--- |
| [!UICONTROL Miscellaneous HTML] | 스토어 뷰 | 닫기 `<body>` 태그 바로 앞에 배치해야 하는 서버에 기타 스크립트를 업로드할 수 있는 입력 상자입니다. |
| [!UICONTROL Copyright] | 스토어 뷰 | 각 페이지의 맨 아래에 표시되는 저작권 선언문입니다. 저작권 기호를 포함하려면 다음과 같이 HTML 문자 엔터티 `\&copy;`을(를) 사용합니다. `\&copy; 2021 Commerce Demo Store. All Rights Reserved.` 샘플 저작권 알림을 자신의 것으로 바꾸십시오. |
| [!UICONTROL Display Report Bugs Link] | 스토어 뷰 | 버그 보고서 링크(일부 테마에 대해 지원됨)의 활성화 또는 비활성화 여부를 결정합니다. |

{style="table-layout:auto"}
