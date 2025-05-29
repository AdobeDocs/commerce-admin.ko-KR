---
title: 사이트 맵
description: Commerce 사이트의 모든 페이지와 이미지를 색인화하기 위해 사이트 맵을 구성하는 방법에 대해 알아봅니다.
exl-id: 48c975ae-b088-4e52-80cf-cb19c2b9b00f
feature: Merchandising, Storefront, Search
badgePaas: label="PaaS만" type="Informative" url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="Adobe Commerce 온 클라우드 프로젝트(Adobe 관리 PaaS 인프라) 및 온프레미스 프로젝트에만 적용됩니다."
source-git-commit: 7e28081ef2723d4113b957edede6a8e13612ad2f
workflow-type: tm+mt
source-wordcount: '1209'
ht-degree: 0%

---

# 사이트 맵

>[!TIP]
>
>Adobe Commerce as a Cloud Service의 경우 Commerce Storefront 설명서에서 [SEO 지침](https://experienceleague.adobe.com/developer/commerce/storefront/setup/seo/indexing/)을 참조하십시오

사이트 맵은 검색 엔진이 스토어를 인덱싱하는 방식을 개선하고 웹 크롤러가 간과할 수 있는 페이지를 찾도록 설계되었습니다. 사이트 맵은 모든 페이지 및 이미지를 색인화하도록 구성할 수 있습니다.

사용하도록 설정하면 Commerce에서 지정한 위치에 설치 위치에 저장된 `sitemap.xml` 파일을 만듭니다. 이 구성을 통해 업데이트 빈도와 각 콘텐츠 유형에 대한 우선 순위를 설정할 수 있습니다. 사이트 맵은 사이트의 콘텐츠가 변경될 때마다(일별, 주별 또는 월별) 자주 업데이트해야 합니다.

사이트가 개발 중인 동안에는 사이트 색인화를 방지하기 위해 웹 크롤러에 대한 지침을 `robots.txt` 파일에 포함할 수 있습니다. 그런 다음 론치 전에 지침을 변경하여 사이트를 인덱싱할 수 있습니다.

자세한 내용은 _Commerce on Cloud Infrastructure Guide_&#x200B;에서 [사이트 맵 및 robots.txt 추가][1]를 참조하십시오.

![사이트 맵 표](./assets/marketing-sitemap-grid-generated.png){width="700" zoomable="yes"}

## 1단계. 사이트 맵 구성

포함된 항목과 사이트 맵의 업데이트 빈도를 확인하려면 [XML 사이트 맵 구성](#site-map-configuration)을 완료하십시오.

## 2단계. 사이트 맵 생성

1. _관리자_ 메뉴에서 **[!UICONTROL Marketing]** > _[!UICONTROL SEO & Search]_>**[!UICONTROL Site Map]**(으)로 이동합니다.

1. **[!UICONTROL Add Site Map]**&#x200B;을(를) 클릭합니다.

   ![사이트 맵 표](./assets/marketing-sitemap.png){width="700" zoomable="yes"}

1. 사이트 맵 **[!UICONTROL Filename]**&#x200B;을(를) 입력하십시오. 예: `sitemap.xml`

1. **[!UICONTROL Path]**&#x200B;을(를) 입력하여 서버에서 사이트 맵 파일이 있는 위치를 결정합니다. 경로에 쓸 수 있는지 확인하십시오.

   - `/sitemap/` - 사이트 맵 파일을 _사이트 맵_&#x200B;이라는 디렉터리에 배치합니다.

   - `/` - 사이트 맵 파일을 Commerce 설치의 기본 경로 또는 루트에 배치합니다.

   ![새 사이트 맵](./assets/marketing-sitemap-new.png){width="600" zoomable="yes"}

1. 완료되면 **[!UICONTROL Save & Generate]**&#x200B;을(를) 클릭합니다.

   사이트 맵이 그리드에 표시되는 데 몇 분 정도 걸릴 수 있습니다.

## 3단계. robots.txt 구성 및 활성화(선택 사항)

인덱싱할 사이트의 부분을 크롤링하도록 검색 엔진에 지시하는 지침과 함께 [검색 엔진 로봇](seo-overview.md#search-engine-robots) 구성을 완료하십시오.

## 4단계. 검색 엔진에 사이트 맵 제출

Commerce 설치에서 `sitemap.xml` 파일에 대한 링크를 제공하여 사이트 맵을 다른 검색 엔진에 제출할 수 있습니다. 링크를 복사하려면 다음을 수행합니다.

1. _사이트 맵_ 목록에서 **[!UICONTROL Link for Google]** 열의 URL을 마우스 오른쪽 단추로 클릭합니다.

1. 메뉴에서 **[!UICONTROL Copy Link Address]**&#x200B;을(를) 선택합니다.

자세한 내용은 특정 검색 엔진에 대한 지침을 참조하십시오. 다음은 두 개의 상위 검색 엔진에 대한 지침 링크입니다.

- [Google][2]
- [Microsoft® Bing][3]

## 5단계: 이전 로봇 지침 복원(선택 사항)

이제 원래(기본) 제한 사항을 복원할 수 있습니다.

## 여러 웹 사이트에 대한 사이트 맵 및 robots.txt 관리

여러 웹 사이트가 있는 경우 사이트 맵을 만들고 제출하는 프로세스를 단순화할 수 있습니다. 확인된 모든 저장소의 URL이 포함된 사이트 맵을 [하나 이상 만들고](#site-map-configuration)한 다음 사이트 맵을 단일 위치에 저장하면 됩니다. [Google 검색 콘솔](https://support.google.com/webmasters/answer/7451001)에서 모든 사이트를 확인해야 합니다.

다중 저장소 인스턴스에 대한 사이트 맵을 만들려면 다음을 수행하십시오.

1. 웹 사이트의 루트에 `sitemaps` 폴더를 만든 다음 각 도메인에 대해 하위 폴더를 만듭니다.

       /sitemaps/domain_1/
       /사이트 맵/도메인_2/
   
1. _관리자_ 사이드바에서 **[!UICONTROL Marketing]** > _[!UICONTROL SEO & Search]_>**[!UICONTROL Site Map]**(으)로 이동합니다.

1. 각 스토어에 대한 사이트 맵 목록을 만들거나 편집하고 **[!UICONTROL Path]**&#x200B;을(를) 스토어에 대해 만든 것으로 설정합니다.

   `/sitemaps/domain_1/`
   `/sitemaps/domain_2/`

1. 필요한 경우 robots.txt 파일을 업데이트합니다.

   검색 엔진 스파이더가 새 사이트 맵으로 올바르게 이동되었는지 확인하려면 robots.txt 파일을 업데이트하거나 만들 수 있습니다. 맨 위에 다음 줄을 추가합니다.

       웹 사이트 사이트 맵
       사이트 맵: https://www.domain_1.com/sitemaps/domain_1/sitemap.xml
       사이트 맵: https://www.domain_2.com/sitemaps/domain_2/sitemap.xml
   
>[!NOTE]
>
>사이트에서 [Apache](https://experienceleague.adobe.com/docs/commerce-operations/installation-guide/prerequisites/web-server/apache.html) 웹 서버 엔진을 사용하는 경우 웹 사이트의 루트에서 [`.htaccess`](https://httpd.apache.org/docs/current/howto/htaccess.html) 파일을 업데이트하여 다른 사이트 맵 요청을 적절한 위치로 이동해야 합니다.

## 열 설명

| 열 | 설명 |
|------|-----------|
| [!UICONTROL ID] | 현재 사이트 맵의 순차적 레코드 번호입니다. |
| [!UICONTROL Filename] | 사이트 맵의 파일 이름입니다. |
| [!UICONTROL Path] | 서버에서 사이트 맵이 있는 위치입니다. 예: <br/>`/sitemap/` - 사이트 맵 파일을 _사이트 맵_(이)라는 디렉터리에 배치합니다. 이 디렉터리는 Commerce 설치의 루트 한 수준 아래에 있습니다. <br/>`/` - 사이트 맵 파일을 Commerce 설치의 기본 경로 또는 루트에 배치합니다. |
| [!UICONTROL Link for Google] | Google 및 기타 검색 엔진에 제출할 사이트 맵의 URL입니다. |
| [!UICONTROL Last Generated] | 사이트 맵이 마지막으로 생성된 날짜와 시간을 나타냅니다. |
| [!UICONTROL Store View] | 사이트 맵이 적용되는 스토어 보기. |
| [!UICONTROL Generate] | 사이트 맵을 다시 생성합니다. |

{style="table-layout:auto"}

## 사이트 맵 구성

사이트 맵은 사이트의 콘텐츠가 변경될 때마다 매일, 매주 또는 매월 업데이트해야 합니다. 구성을 통해 각 콘텐츠 유형에 대한 빈도와 우선 순위를 설정할 수 있습니다.

### 1단계. 콘텐츠 업데이트 빈도 및 우선 순위 설정

1. _관리자_ 사이드바에서 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**(으)로 이동합니다.

1. 왼쪽 패널에서 **[!UICONTROL Catalog]**&#x200B;을(를) 확장하고 **[!UICONTROL XML Sitemap]**&#x200B;을(를) 선택합니다.

1. **[!UICONTROL Categories Options]** 섹션에서 ![확장 선택기](../assets/icon-display-expand.png)를 확장하고 다음을 수행합니다.

   >[!NOTE]
   >
   >필요한 경우 **[!UICONTROL Use system value]** 확인란의 선택을 취소하여 이 설정을 변경합니다.

   - **[!UICONTROL Frequency]**&#x200B;을(를) 다음 중 하나로 설정합니다.

      - `Always`
      - `Hourly`
      - `Daily`
      - `Weekly`
      - `Monthly`
      - `Yearly`
      - `Never`

   - **[!UICONTROL Priority]**&#x200B;에 대해 `0.0`에서 `1.0` 사이의 값을 입력하십시오. 0이 가장 낮은 우선 순위를 갖습니다.

   ![XML 사이트 맵 - 범주 옵션](../configuration-reference/catalog/assets/xml-sitemap-categories-options.png){width="600" zoomable="yes"}

   이러한 옵션에 대한 자세한 목록이 필요하면 _구성 참조_&#x200B;에서 [범주 옵션](../configuration-reference/catalog/xml-sitemap.md#categories-options)을 참조하십시오.

1. **[!UICONTROL Products Options]** 섹션에서 ![확장 선택기](../assets/icon-display-expand.png)를 확장하고 필요에 따라 **[!UICONTROL Frequency]** 및 **[!UICONTROL Priority]** 설정을 완료합니다.

   이러한 옵션에 대한 자세한 목록은 _구성 참조_&#x200B;에서 [제품 옵션](../configuration-reference/catalog/xml-sitemap.md#products-options)을 참조하십시오.

1. 사이트 맵에 이미지가 포함되는 범위를 확인하려면 **[!UICONTROL Add Images into Sitemap]**&#x200B;을(를) 다음 중 하나로 설정하십시오.

   - `None`
   - `Base Only`
   - `All`

   ![카탈로그 구성 - XML 사이트 맵 제품](../configuration-reference/catalog/assets/xml-sitemap-products-options.png){width="600" zoomable="yes"}

1. **[!UICONTROL CMS Pages Options]** 섹션에서 ![확장 선택기](../assets/icon-display-expand.png)를 확장하고 필요에 따라 **[!UICONTROL Frequency]** 및 **[!UICONTROL Priority]** 설정을 완료합니다.

   ![카탈로그 구성 - XML 사이트 맵 CMS 페이지](../configuration-reference/catalog/assets/xml-sitemap-cms-pages-options.png){width="600" zoomable="yes"}

   이러한 옵션에 대한 자세한 목록이 필요하면 _구성 참조_&#x200B;에서 [CMS 페이지 옵션](../configuration-reference/catalog/xml-sitemap.md#cms-pages-options)을 참조하십시오.

1. **[!UICONTROL Store Url Options]** 섹션에서 ![확장 선택기](../assets/icon-display-expand.png)를 확장하고 필요에 따라 **[!UICONTROL Frequency]** 및 **[!UICONTROL Priority]** 설정을 완료합니다.

   ![카탈로그 구성 - XML 사이트 맵 저장소 URL](./assets/xml-sitemap.png){width="600" zoomable="yes"}

   이러한 옵션에 대한 자세한 목록이 필요하면 _구성 참조_&#x200B;에서 [URL 옵션 저장](../configuration-reference/catalog/xml-sitemap.md#store-url-options)을 참조하십시오.

1. 완료되면 **[!UICONTROL Save Config]**&#x200B;을(를) 클릭합니다.

### 2단계. 생성 설정 완료

1. **[!UICONTROL Generation Settings]** 섹션에서 ![확장 선택기](../assets/icon-display-expand.png)를 확장합니다.

   필요한 경우 **시스템 값 사용** 확인란의 선택을 취소하여 이러한 설정을 변경합니다.

   ![카탈로그 구성 - XML 사이트 맵 생성 설정](../configuration-reference/catalog/assets/xml-sitemap-generation-settings.png){width="600" zoomable="yes"}

   이러한 옵션에 대한 자세한 목록이 필요하면 _구성 참조_&#x200B;에서 [생성 설정](../configuration-reference/catalog/xml-sitemap.md#generation-settings)을 참조하십시오.

1. 사이트 맵을 생성하려면 **[!UICONTROL Enabled]**&#x200B;을(를) `Yes`(으)로 설정하고 다음을 수행합니다.

   - 사이트 맵을 업데이트할 시간, 분, 초로 **[!UICONTROL Start Time]**&#x200B;을(를) 설정합니다.

   - **[!UICONTROL Frequency]**&#x200B;을(를) 다음 중 하나로 설정합니다.

      - `Daily`
      - `Weekly`
      - `Monthly`

   - **[!UICONTROL Error Email Recipient]**&#x200B;의 경우 사이트 맵을 업데이트하는 동안 오류가 발생하면 알림을 받을 사람의 전자 메일 주소를 입력하십시오.

   - 오류 알림을 보낸 사람으로 표시되는 저장소 연락처로 **[!UICONTROL Error Email Sender]**&#x200B;을(를) 설정합니다.

   - 오류 알림에 사용되는 템플릿으로 **[!UICONTROL Error Email Template]**&#x200B;을(를) 설정합니다.

### 3단계. 사이트 맵 파일 제한 설정

1. **[!UICONTROL Sitemap File Limits]** 섹션에서 ![확장 선택기](../assets/icon-display-expand.png)를 확장합니다.

   ![카탈로그 구성 - XML 사이트 맵 파일 제한](../configuration-reference/catalog/assets/xml-sitemap-sitemap-file-limits.png){width="600" zoomable="yes"}

   이러한 옵션에 대한 자세한 목록이 필요하면 _구성 참조_&#x200B;에서 [사이트 맵 파일 제한](../configuration-reference/catalog/xml-sitemap.md#sitemap-file-limits)을 참조하십시오.

1. **[!UICONTROL Maximum No of URLs per File]**&#x200B;의 경우 사이트 맵에 포함할 수 있는 최대 URL 수를 입력하십시오.

   기본적으로 제한은 50,000입니다.

1. **[!UICONTROL Maximum File Size]**&#x200B;의 경우 사이트 맵에 할당된 최대 크기(바이트)를 입력하십시오.

   기본 크기는 10,485,760바이트입니다.

### 4단계. 검색 엔진 제출 설정 설정

1. **[!UICONTROL Search Engine Submission Settings]** 섹션에서 ![확장 선택기](../assets/icon-display-expand.png)를 확장합니다.

   ![카탈로그 구성 - XML 사이트 맵 검색 엔진 제출 설정](../configuration-reference/catalog/assets/xml-sitemap-search-engine-submission-settings.png){width="600" zoomable="yes"}

1. `robots.txt` 파일을 사용하여 사이트를 크롤링하는 검색 엔진에 대한 지침을 제공하는 경우 **[!UICONTROL Enable Submission to Robots.txt]**&#x200B;을(를) `Yes`(으)로 설정하십시오.

1. 완료되면 **[!UICONTROL Save Config]**&#x200B;을(를) 클릭합니다.

[1]: https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/configure-store/robots-sitemap.html
[2]: https://support.google.com/webmasters/answer/183669?hl=en
[3]: https://www.bing.com/webmasters/help/Sitemaps-3b5cf6ed
