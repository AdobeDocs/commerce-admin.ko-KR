---
title: '[!DNL Page Builder] 사용 안내서'
description: 다음에 대한 포괄적인 정보 [!DNL Page Builder] Adobe Commerce 및 Magento Open Source 관리자용
seo-title: Adobe Commerce [!DNL Page Builder] User Guide
seo-description: Describes how to use the [!DNL Page Builder] module in Adobe Commerce or Magento Open Source.
exl-id: 983ef3a8-b803-40ff-a9f5-07eb895df31c
source-git-commit: fa4030d391fc9a3b21cf8fb6f681df9e9165157d
workflow-type: tm+mt
source-wordcount: '492'
ht-degree: 1%

---

# [!DNL Page Builder] 사용 안내서

이 안내서는 Adobe Commerce 및 Magento Open Source 관리자를 위한 것입니다. 다음에 대한 자세한 정보를 제공합니다. [!DNL Page Builder] 기본 콘텐츠 구성 요소 작성을 위한 3단계 과정을 포함하는 기능입니다. 그것은 핵심을 기본적으로 이해하는 것이라고 가정한다 [!DNL Commerce] 구성 및 기능을 사용할 수 있습니다.

[!DNL Page Builder] 에는 스토어 관리자를 위한 두 가지 영역이 있습니다.

- 관리자: 이 영역을 사용하여 구성 UI에 액세스하고 페이지 빌더 도구를 사용합니다.
- 명령줄 인터페이스: 이 도구를 사용하여 설치 및 백엔드 구성 작업을 실행합니다.

이 안내서에서는 다음 주제를 다룹니다.

| 제목 | 설명 |
| ------- | ----------- |
| [소개](introduction.md) | 이란? [!DNL Page Builder]? 그리고 Adobe Commerce 및 Magento Open Source 사이트의 콘텐츠 생성을 어떻게 향상시킵니까? |
| [릴리스 정보](release-notes.md) | 각각에 제공된 업데이트 검토 [!DNL Page Builder] 모듈 릴리스. |
| [설정](setup.md) | 기본 설정을 업데이트하려면 기본 페이지 레이아웃을 변경하고 더 많은 항목을 활성화할 수 있습니다 [!DNL Page Builder] 기능. 을 통합할 수도 있습니다 [!DNL Google Maps] 를 사용하여 위치 콘텐츠를 페이지에 통합할 수 있습니다. |
| [작업 영역](workspace.md) | 의 구성 요소 검토 [!DNL Page Builder] workspace 및 이를 통해 스토어에 매력적인 콘텐츠를 만드는 방법. |
| 연습 | 을(를) 방금 시작하는 경우 [!DNL Page Builder], 연습 연습을 완료하여 속도를 빠르게 높일 수 있습니다.<br>[1 - 샘플 페이지](1-simple-page.md)<br>[2 - 재사용 가능한 콘텐츠 블록](2-blocks.md)<br>[3 - 제품 목록의 카탈로그 페이지](3-catalog-content.md) |
| [작업 영역](workspace.md) | 에서 사용할 수 있는 도구 탐색 [!DNL Page Builder] 작업 영역: 기본 페이지, 제품 및 카탈로그 페이지, 블록 및 동적 블록을 만들 때 |
| 레이아웃 | 탐색 _레이아웃_ 의 섹션 [!DNL Page Builder] 패널 및 이러한 도구를 사용하여 레이아웃 구성 요소를 [!DNL Page Builder] 단계: <br>[행](row.md)<br>[열](column.md)<br>[탭](tabs.md) |
| 요소 | 탐색 _요소_ 의 섹션 [!DNL Page Builder] 패널 및 이러한 도구를 사용하여 의 레이아웃 컨테이너에 기본 요소를 추가하는 방법 [!DNL Page Builder] 단계: <br>[텍스트](text.md)<br>[제목](heading.md)<br>[단추](buttons.md)<br>[분할자](divider.md)<br>[HTML 코드](html-code.md) |
| 미디어 | 탐색 _미디어_ 의 섹션 [!DNL Page Builder] 패널 및 이러한 도구를 사용하여 의 레이아웃 컨테이너에 미디어 항목을 추가하는 방법 [!DNL Page Builder] 단계: <br>[이미지](image.md)<br>[비디오](video.md)<br>[배너](banner.md)<br>[슬라이더](slider.md)<br>[[!DNL Google Maps]](map.md) |
| 콘텐츠 추가 | 탐색 _콘텐츠 추가_ 의 섹션 [!DNL Page Builder] 패널 및 콘텐츠 구성 요소를 추가하는 방법 [!DNL Page Builder] 단계: <br>[차단](block.md)<br>[동적 블록](dynamic-block.md)<br>[제품](products.md)<br>[제품 Recommendations](recommendations.md) (Adobe Commerce 전용) |
| [템플릿](templates.md) | 기존 저장 [!DNL Page Builder] 콘텐츠를 템플릿으로 만든 다음 해당 템플릿을 다른 영역에 적용하여 빠르고 일관성 있는 콘텐츠를 만들 수 있습니다. |

{style="table-layout:auto"}

Adobe Commerce 및 Magento Open Source의 핵심 기능은 다루지 않습니다.

## 추가 설명서

{{docs-links}}

## [!DNL Page Builder] 개발자 정보

[!DNL Page Builder] 는 Adobe Commerce 2.4.x 및 Magento Open Source 2.4.3 이상에서 설치되며, 모든 기능은 기본적으로 활성화되어 있습니다. 모듈 릴리스에 포함된 변경 사항에 대한 자세한 내용은 [[!DNL Page Builder] 릴리스 정보](release-notes.md). 다음 [[!DNL Page Builder] 개발자 안내서](https://developer.adobe.com/commerce/frontend-core/page-builder/) 는 모듈 아키텍처 및 사용자 지정에 대한 자세한 내용을 제공합니다.

## 리소스 문제 해결

문제 해결 관련 도움말 [!DNL Page Builder] 문제, 다음 참조 [!DNL Commerce] 지원 기술 자료 문서:

- [DotDigital인 경우 빈 페이지 [!DNL Page Builder] 양식 저장됨](https://experienceleague.adobe.com/docs/commerce-knowledge-base/kb/troubleshooting/miscellaneous/magento-2.4.1-empty-page-when-dotdigital-page-builder-form-saved.html)
- [[!DNL Page Builder] 미디어 갤러리를 로드하지 않음](https://experienceleague.adobe.com/docs/commerce-knowledge-base/kb/support-tools/patches/v1-0-12/mdva-32133-magento-patch-page-builder-doesn-t-load-media-gallery.html)
- [[!DNL Page Builder] 미리보기가 사이트 간 제품 가격 차이](https://experienceleague.adobe.com/docs/commerce-knowledge-base/kb/support-tools/patches/v1-0-16/mdva-33453-page-builder-preview-breaks-product-price-differs-across-sites.html)
- [용어 페이지를 저장할 수 없음](https://experienceleague.adobe.com/docs/commerce-knowledge-base/kb/support-tools/patches/v1-0-19/mdva-33614-magento-patch-can-t-save-terms-page.html)
