---
title: '[!DNL Page Builder] 사용 안내서'
description: Adobe Commerce 및 Magento Open Source 관리자를 위한  [!DNL Page Builder] 에 대한 포괄적인 정보입니다.
seo-title: Adobe Commerce [!DNL Page Builder] User Guide
seo-description: Describes how to use the [!DNL Page Builder] module in Adobe Commerce or Magento Open Source.
exl-id: 983ef3a8-b803-40ff-a9f5-07eb895df31c
source-git-commit: dbc0057f02bddf681d769bdaebfaf6b526c8dbd2
workflow-type: tm+mt
source-wordcount: '443'
ht-degree: 0%

---

# [!DNL Page Builder] 사용 안내서

이 안내서는 Adobe Commerce 및 Magento Open Source 관리자에서 작업 중인 관리자를 위한 것입니다. 기본 콘텐츠 구성 요소 작성을 위한 3단계 과정을 포함하여 [!DNL Page Builder] 기능에 대한 자세한 정보를 제공합니다. 이는 핵심 [!DNL Commerce] 구성 및 기능에 대한 기본적인 이해를 전제로 합니다.

[!DNL Page Builder]에는 저장소 관리자를 위한 두 개의 영역이 있습니다.

- 관리자: 이 영역을 사용하여 구성 UI에 액세스하고 페이지 빌더 도구를 사용합니다.
- 명령줄 인터페이스: 이 도구를 사용하여 설치 및 백엔드 구성 작업을 실행합니다.

이 안내서에서는 다음 주제를 다룹니다.

| 제목 | 설명 |
| ------- | ----------- |
| [소개](introduction.md) | [!DNL Page Builder]이란? 또한 Adobe Commerce 및 Magento Open Source 사이트의 콘텐츠 생성을 어떻게 향상시킵니까? |
| [릴리스 정보](release-notes.md) | 각 [!DNL Page Builder] 모듈 릴리스에 제공된 업데이트를 검토합니다. |
| [설치](setup.md) | 기본 설정을 업데이트하려면 기본 페이지 레이아웃을 변경하고 더 많은 고급 [!DNL Page Builder] 기능을 사용하도록 설정할 수 있습니다. [!DNL Google Maps]을(를) 통합하여 위치 콘텐츠를 페이지에 통합할 수도 있습니다. |
| [Workspace](workspace.md) | [!DNL Page Builder] 작업 영역의 구성 요소와 이를 통해 스토어에 대한 매력적인 콘텐츠를 만드는 방법을 검토하십시오. |
| 연습 | [!DNL Page Builder]을(를) 처음 시작하는 경우 연습 연습을 완료하여 빠르게 시작할 수 있습니다.<br>[1 - 샘플 페이지](1-simple-page.md)<br>[2 - 재사용 가능한 콘텐츠 블록](2-blocks.md)<br>[3 - 제품 목록의 카탈로그 페이지](3-catalog-content.md) |
| [Workspace](workspace.md) | 기본 페이지, 제품 및 카탈로그 페이지, 블록 및 동적 블록을 만들 때 [!DNL Page Builder] 작업 영역에서 사용할 수 있는 도구를 살펴봅니다. |
| 레이아웃 | _패널의_&#x200B;레이아웃[!DNL Page Builder] 섹션을 살펴보고 다음 도구를 사용하여 레이아웃 구성 요소를 [!DNL Page Builder] 단계에 추가하는 방법을 확인하십시오. <br>[행](row.md)<br>[열](column.md)<br>[탭](tabs.md) |
| 요소 | _패널의_&#x200B;요소[!DNL Page Builder] 섹션 및 이러한 도구를 사용하여 [!DNL Page Builder] 단계의 레이아웃 컨테이너에 기본 요소를 추가하는 방법을 살펴보십시오. <br>[텍스트](text.md)<br>[제목](heading.md)<br>[단추](buttons.md)<br>[분할자](divider.md)<br>[HTML 코드](html-code.md) |
| 미디어 | _패널의_&#x200B;미디어[!DNL Page Builder] 섹션 및 이러한 도구를 사용하여 [!DNL Page Builder] 단계의 모든 레이아웃 컨테이너에 미디어 항목을 추가하는 방법을 살펴보십시오. <br>[이미지](image.md)<br>[비디오](video.md)<br>[배너](banner.md)<br>[슬라이더](slider.md)<br>[[!DNL Google Maps]](map.md) |
| 콘텐츠 추가 | _패널의_&#x200B;콘텐츠 추가[!DNL Page Builder] 섹션 및 [!DNL Page Builder] 단계에 콘텐츠 구성 요소를 추가하는 방법을 살펴봅니다. <br>[블록](block.md)<br>[동적 블록](dynamic-block.md)<br>[제품](products.md)<br>[제품 권장 사항](recommendations.md)(Adobe Commerce만 해당) |
| [템플릿](templates.md) | 기존 [!DNL Page Builder] 콘텐츠를 템플릿으로 저장한 다음 다른 영역에 해당 템플릿을 적용하여 빠르고 일관된 콘텐츠를 만듭니다. |

{style="table-layout:auto"}

Adobe Commerce 및 Magento Open Source의 핵심 기능은 다루지 않습니다.

## 추가 설명서

{{docs-links}}

## [!DNL Page Builder] 개발자 정보

[!DNL Page Builder]은(는) 기본적으로 모든 기능이 활성화된 Adobe Commerce 2.4.x 및 Magento Open Source 2.4.3 이상에서 설치됩니다. 모듈 릴리스에 포함된 변경 사항에 대한 자세한 내용은 [[!DNL Page Builder] 릴리스 정보](release-notes.md)를 참조하세요. [[!DNL Page Builder] 개발자 안내서](https://developer.adobe.com/commerce/frontend-core/page-builder/)에서는 모듈 아키텍처 및 사용자 지정에 대한 자세한 정보를 제공합니다.

## 리소스 문제 해결

[!DNL Page Builder] 문제를 해결하는 데 대한 도움말을 보려면 다음 [!DNL Commerce] 지원 기술 문서를 참조하십시오.

- [DotDigital을 저장할 때 빈 페이지 [!DNL Page Builder] 양식을 저장](https://experienceleague.adobe.com/docs/commerce-knowledge-base/kb/troubleshooting/miscellaneous/magento-2.4.1-empty-page-when-dotdigital-page-builder-form-saved.html)
