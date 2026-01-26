---
title: 제품 비디오 추가
description: Google 계정의 YouTube 데이터 API 키가 필요한 스토어에 대한 제품 비디오를 구성하고 제품에 대한 비디오 링크를 추가하는 방법에 대해 알아봅니다.
exl-id: 0cfcee67-a2e2-41cb-ac70-304452f5db6d
feature: Catalog Management, Products, Media
source-git-commit: cace9d1de00955494d8bc607c017778ff7df4806
workflow-type: tm+mt
source-wordcount: '653'
ht-degree: 0%

---

# 제품 비디오 추가

제품 비디오를 추가하려면 먼저 Google 계정에서 API 키를 가져와 스토어 구성에 입력해야 합니다. 그런 다음 제품에서 비디오에 연결할 수 있습니다.

## 1단계: YouTube API 키 가져오기

1. Google 계정에 로그인하고 [Google 개발자 콘솔](https://console.developers.google.com/)을 방문합니다.

1. 맨 위의 검색 필드에 `YouTube Data API v3`을(를) 입력하고 검색 아이콘을 클릭합니다.

1. API 페이지가 표시되면 활성화되어 있는지 확인합니다.

1. 왼쪽 패널에서 **[!UICONTROL Credentials]**&#x200B;을(를) 선택합니다.

1. 자격 증명 보유 여부에 따라 다음 중 하나를 수행합니다.

   - 필요한 자격 증명이 이미 있는 경우 _API 키_ 테이블의 키를 복사합니다.

   - 이 API에 대한 자격 증명이 없는 경우 맨 위에 있는 **[!UICONTROL Create Credentials]**&#x200B;을(를) 클릭하고 프롬프트에 따라 필요한 자격 증명을 만드십시오. _자격 증명 가져오기_&#x200B;에서 API 키를 복사하고 **[!UICONTROL Done]**&#x200B;을(를) 클릭합니다.

1. API 키를 클립보드에 복사합니다.

1. 오른쪽의 편집 아이콘을 클릭하고 제한 사항을 설정하여 API 키가 올바른 레퍼러로 제한되어 있는지 확인합니다.

1. 키를 생성하는 동안 잠시 기다렸다가 클립보드에 키를 복사합니다.

   다음 단계에서는 키를 저장소의 구성에 붙여 넣습니다.

## 2단계: Commerce에서 키 구성

1. _관리자_ 사이드바에서 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**(으)로 이동합니다.

1. 왼쪽 패널에서 **[!UICONTROL Catalog]**&#x200B;을(를) 확장하고 아래의 **[!UICONTROL Catalog]**&#x200B;을(를) 선택합니다.

1. ![ 섹션에서 ](../assets/icon-display-expand.png)확장 선택기&#x200B;_[!UICONTROL Product Video]_를 확장하고&#x200B;**[!UICONTROL YouTube API key]**을(를) 붙여 넣습니다.

   ![제품 비디오 구성](../configuration-reference/catalog/assets/catalog-product-video.png){width="600" zoomable="yes"}

1. 완료되면 **[!UICONTROL Save Config]**&#x200B;을(를) 클릭합니다.

1. 메시지가 표시되면 캐시를 새로 고칩니다.

## 3단계: 비디오 링크

1. 제품을 편집 모드로 엽니다.

1. _[!UICONTROL Images and Videos]_섹션으로 스크롤한 다음 확장합니다.

   ![이미지 및 비디오](./assets/product-simple-images-videos.png){width="600" zoomable="yes"}

1. **[!UICONTROL Add Video]**&#x200B;을(를) 클릭합니다.

   YouTube API 키를 아직 구성하지 않은 경우 계속하려면 **[!UICONTROL OK]**&#x200B;을(를) 클릭하십시오. YouTube 비디오에 연결할 수 없지만 프로세스를 진행할 수 있습니다.

1. **[!UICONTROL Url]**&#x200B;의 경우 YouTube 또는 Vimeo 비디오의 URL을 입력하십시오.

   ![제품용 새 비디오](./assets/product-video-add.png){width="600" zoomable="yes"}

1. 필드 외부를 클릭하고 API 키 또는 비디오에 대한 피드백을 기다립니다.

   모든 항목이 체크아웃되면 YouTube에서 비디오의 기본 정보를 제공합니다

1. 비디오의 **[!UICONTROL Title]** 및 **[!UICONTROL Description]**&#x200B;을(를) 입력하십시오.

1. **[!UICONTROL Preview Image]**&#x200B;을(를) 업로드하려면 이미지를 찾은 다음 파일을 선택하십시오.

   >[!NOTE]
   >
   >업로드 후 표시되는 미리보기 이미지는 외부 비디오 서비스 공급자에 의해 자동으로 생성됩니다. Adobe Commerce 관리자의 이미지는 편집할 수 없습니다.

1. 비디오 메타데이터를 사용하려면 **[!UICONTROL Get Video Information]**&#x200B;을(를) 클릭합니다.

1. 스토어에서 비디오가 사용되는 방식을 결정하려면 적용되는 각 **[!UICONTROL Role]**&#x200B;의 확인란을 선택하십시오.

   - `Base Image`
   - `Small Image`
   - `Swatch Image`
   - `Thumbnail`
   - `Hide from Product Page`

1. 완료되면 **[!UICONTROL Save]**&#x200B;을(를) 클릭합니다.

   >[!NOTE]
   >
   >_[!UICONTROL Autostart base video]_구성 옵션이 `Yes`(으)로 설정되어 있지만 비디오가 자동으로 재생되지 않는 경우, 브라우저에 의해 시행되고 Adobe Commerce에서 제어할 수 없는 자동 재생 정책 때문일 수 있습니다. 지원되는 각 브라우저에는 시간이 지남에 따라 변경될 수 있는 자체 자동 재생 정책이 있으며 비디오가 나중에 자동 재생되지 않을 수 있습니다. 권장되는 우수 사례로서, 비즈니스 크리티컬 기능에 대해 자동 재생에 의존해서는 안 되며 지원되는 각 브라우저로 스토어에서 비디오 자동 재생 동작을 테스트해야 합니다.

## API 액세스 유지

Google 개발자 [약관](https://developers.google.com/youtube/terms/developer-policies#d.-accessing-youtube-api-services)에 따르면 YouTube은 90일 이상 비활성 상태인 계정에 대해 API 액세스를 비활성화할 수 있습니다. 이 경우 비디오가 표시되지 않을 수 있습니다. API 액세스를 최신 상태로 유지하려면 cron 작업을 사용하여 정기적으로 API를 ping하십시오.

```code
30 10 1 * * curl -i -G -e https://yourdomain.com/ -d "part=snippet&maxResults=1&q=test&key=YOUTUBEAPIKEY" https://www.googleapis.com/youtube/v3/search >/dev/null 2>&1
```

## 필드 참조

| 필드 | 설명 |
|--- |--- |
| [!UICONTROL URL] | 연결된 비디오의 URL입니다. |
| [!UICONTROL Title] | 비디오 제목입니다. |
| [!UICONTROL Description] | 비디오 설명입니다. |
| [!UICONTROL Preview Image] | 스토어에서 비디오의 미리보기로 사용되는 업로드된 이미지. |
| [!UICONTROL Get Video Information] | 호스트 서버에 저장된 비디오 메타데이터를 검색합니다. 원본 데이터를 사용하거나 필요에 따라 업데이트할 수 있습니다. |
| [!UICONTROL Role] | 스토어에서 미리보기 이미지가 사용되는 방법을 결정합니다. `Base Image`, `Small Image`, `Thumbnail`, `Swatch Image`, `Hide from Product Page` 옵션 조합을 선택할 수 있습니다. |

{style="table-layout:auto"}
