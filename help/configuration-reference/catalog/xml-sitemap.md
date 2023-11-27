---
title: '[!UICONTROL Catalog] &gt; [!UICONTROL XML Sitemap]'
description: 에서 구성 설정을 검토합니다. [!UICONTROL Catalog] &gt; [!UICONTROL XML Sitemap] 상거래 관리자의 페이지입니다.
exl-id: 319c34e9-bd5f-46f8-810f-bc4d5228f9c9
feature: Configuration, Site Navigation
source-git-commit: 76bd1b1af9b55d69bd98209d70fb5518f190a3e1
workflow-type: tm+mt
source-wordcount: '360'
ht-degree: 1%

---

# [!UICONTROL Catalog] > [!UICONTROL XML Sitemap]

{{config}}

## [!UICONTROL Categories Options]

![범주 옵션](./assets/xml-sitemap-categories-options.png)<!-- zoom -->

<!-- [Categories Options](https://docs.magento.com/user-guide/marketing/sitemap-xml-configure.html) -->

| 필드 | [범위](../../getting-started/websites-stores-views.md#scope-settings) | 설명 |
|--- |--- |--- |
| [!UICONTROL Frequency] | 스토어 뷰 | 사이트 맵 범주를 업데이트하는 빈도를 결정합니다. 옵션: `Always` / `Hourly` / `Daily` / `Weekly` / `Monthly` / `Yearly` / `Never` |
| [!UICONTROL Priority] | 스토어 뷰 | 다음 사이의 값 `0.0` 및 `1.0` 다른 콘텐츠와 관련하여 카테고리 사이트맵 업데이트의 우선 순위를 결정합니다. 0(`0.0`)의 우선 순위가 가장 낮습니다. |

{:style=&quot;table-layout:auto&quot;}

## [!UICONTROL Products Options]

![제품 옵션](./assets/xml-sitemap-products-options.png)<!-- zoom -->

<!-- [Products Options](https://docs.magento.com/user-guide/marketing/sitemap-xml-configure.html) -->

| 필드 | [범위](../../getting-started/websites-stores-views.md#scope-settings) | 설명 |
|--- |--- |--- |
| [!UICONTROL Frequency] | 스토어 뷰 | 사이트 맵 제품을 업데이트하는 빈도를 결정합니다. 옵션: `Always` / `Hourly` / `Daily` / `Weekly` / `Monthly` / `Yearly` / `Never` |
| [!UICONTROL Priority] | 스토어 뷰 | 다음 사이의 값 `0.0` 및 `1.0` 다른 콘텐츠와 관련하여 제품 사이트 맵 업데이트의 우선 순위를 결정합니다. 0(`0.0`)의 우선 순위가 가장 낮습니다. |
| [!UICONTROL Add Images into Sitemap] | 스토어 뷰 | 사이트 맵에 이미지가 포함되는 범위를 결정합니다. 옵션: `None` / `Base Only` / `All` |

{:style=&quot;table-layout:auto&quot;}

## [!UICONTROL CMS Pages Options]

![CMS 페이지 옵션](./assets/xml-sitemap-cms-pages-options.png)<!-- zoom -->

<!-- [CMS Pages Options](https://docs.magento.com/user-guide/marketing/sitemap-xml-configure.html) -->

| 필드 | [범위](../../getting-started/websites-stores-views.md#scope-settings) | 설명 |
|--- |--- |--- |
| [!UICONTROL Frequency] | 스토어 뷰 | 사이트 맵 CMS 페이지의 업데이트 빈도를 결정합니다. 옵션: `Always` / `Hourly` / `Daily` / `Weekly` / `Monthly` / `Yearly` / `Never` |
| [!UICONTROL Priority] | 스토어 뷰 | 다음 사이의 값 `0.0` 및 `1.0` 다른 콘텐츠와 관련된 CMS 페이지 사이트맵 업데이트의 우선 순위를 결정합니다. 0(`0.0`)의 우선 순위가 가장 낮습니다. |

{:style=&quot;table-layout:auto&quot;}

## [!UICONTROL Store Url Options]

| 필드 | [범위](../../getting-started/websites-stores-views.md#scope-settings) | 설명 |
|--- |--- |--- |
| [!UICONTROL Frequency] | 스토어 뷰 | 저장소 URL의 업데이트 빈도를 결정합니다. 옵션: `Always` / `Hourly` / `Daily` / `Weekly` / `Monthly` / `Yearly` / `Never` |
| [!UICONTROL Priority] | 스토어 뷰 | 다음 사이의 값 `0.0` 및 `1.0` 다른 콘텐츠와 관련된 스토어 URL 업데이트의 우선 순위를 결정합니다. 0(`0.0`)의 우선 순위가 가장 낮습니다. |

{:style=&quot;table-layout:auto&quot;}

## [!UICONTROL Generation Settings]

![생성 설정](./assets/xml-sitemap-generation-settings.png)<!-- zoom -->

<!-- [Generation Settings](https://docs.magento.com/user-guide/marketing/sitemap-xml-configure.html) -->

| 필드 | [범위](../../getting-started/websites-stores-views.md#scope-settings) | 설명 |
|--- |--- |--- |
| [!UICONTROL Enabled] | 스토어 뷰 | 저장소에 XML 사이트 맵을 사용할 수 있는지 여부를 결정합니다. 옵션: `Yes` / `No` |
| [!UICONTROL Start Time] | 스토어 뷰 | 사이트 맵이 업데이트되는 시간, 분 및 초를 지정합니다. |
| [!UICONTROL Frequency] | 스토어 뷰 | 사이트 맵의 업데이트 빈도를 결정합니다. 옵션: `Daily` / `Weekly` / `Monthly` |
| [!UICONTROL Error Email Recipient] | 스토어 뷰 | 사이트 맵 업데이트 프로세스 중에 오류가 발생하는 경우 알림을 받는 사람의 이메일 주소입니다. 여러 주소의 경우 쉼표로 각각 구분하십시오. |
| [!UICONTROL Error Email Sender] | 웹 사이트 | 오류 알림을 보낸 사람으로 표시되는 스토어 연락처를 식별합니다. 옵션: `General Contact` / `Sales Representative` / `Customer Support` / `Custom Email 1` / `Custom Email 2` |
| [!UICONTROL Error Email Template] | 웹 사이트 | 오류 알림에 사용되는 이메일 템플릿을 식별합니다. 기본 템플릿: `Sitemap generate Warnings` |

{:style=&quot;table-layout:auto&quot;}

## [!UICONTROL Sitemap File Limits]

![사이트 맵 파일 제한](./assets/xml-sitemap-sitemap-file-limits.png)<!-- zoom -->

<!-- [Sitemap File Limits](https://docs.magento.com/user-guide/marketing/sitemap-xml-configure.html) -->

| 필드 | [범위](../../getting-started/websites-stores-views.md#scope-settings) | 설명 |
|--- |--- |--- |
| [!UICONTROL Maximum No of URLs Per File] | 스토어 뷰 | 단일 사이트 맵에 포함할 수 있는 최대 URL 수를 결정합니다. |
| [!UICONTROL Maximum File Size] | 스토어 뷰 | 생성된 사이트 맵의 최대 크기(바이트)를 결정합니다. |

{:style=&quot;table-layout:auto&quot;}

## [!UICONTROL Search Engine Submission Settings]

![검색 엔진 제출 설정](./assets/xml-sitemap-search-engine-submission-settings.png)<!-- zoom -->

<!-- [Search Engine Submission Settings](https://docs.magento.com/user-guide/marketing/sitemap-xml-configure.html) -->

| 필드 | [범위](../../getting-started/websites-stores-views.md#scope-settings) | 설명 |
|--- |--- |--- |
| [!UICONTROL Enable Submission to Robots.txt] | 스토어 뷰 | robots.txt 파일에 대해 디렉티브를 제출할 수 있도록 합니다. 옵션: `Yes` / `No` |

{:style=&quot;table-layout:auto&quot;}
