---
title: '[!DNL Page Builder] 설정'
description: 다음에 대해 알아보기 [!DNL Page Builder] Adobe Commerce 및 Magento Open Source 관리의 기능 구성.
exl-id: 48396045-0fef-4f4f-8138-e6d969560e42
feature: Page Builder, Configuration
source-git-commit: 2299beb6c11af801076d3aff0b026d41b9dbd212
workflow-type: tm+mt
source-wordcount: '427'
ht-degree: 0%

---

# [!DNL Page Builder] 설정

구성에서 활성화된 경우 [!DNL Page Builder] 는 CMS 페이지, 블록 및 동적 블록에 대한 기본 콘텐츠 생성 도구입니다. 또한 _[!UICONTROL Enable Advanced CMS]_오퍼 단추 [!DNL Page Builder] 카테고리 및 제품에 대한 옵션입니다. 기본값을 선택할 수도 있습니다 [페이지 레이아웃](../content-design/page-layout.md) 제품, 카테고리 및 CMS 페이지에 사용할 수 있습니다. [!DNL Page Builder] 는 WYSIWYG를 사용하는 뉴스레터 콘텐츠에 사용할 수 없습니다. [편집자](../content-design/editor.md).

>[!NOTE]
>
>설치 시, [!DNL Page Builder] 에 대한 기본 설정을 재정의합니다. [!UICONTROL Mask for Meta Description] 구성 필드. 값이에서 변경됨 `{{name}} {{description}}` 끝 `{{name}}`.
><br>
>로 이동하면 이 설정에 액세스할 수 있습니다. [!UICONTROL Stores] > _[!UICONTROL Settings]_> [!UICONTROL Configuration], 확장 [!UICONTROL Catalog], 및 선택 [!UICONTROL Catalog] 밑에. 다음 [!UICONTROL Mask for Meta Description] 필드는 다음에 있습니다. [!UICONTROL Product Fields Auto-generation] 섹션.

>[!NOTE]
>
>관리자는 다음을 보유해야 합니다. [!UICONTROL Content] 에 대한 권한 [역할 범위](../systems/permissions-user-roles.md) 보기 [!UICONTROL Edit with Page Builder] 단추를 클릭하여 페이지 빌더를 사용할 수 있습니다.

콘텐츠 관리 고급 도구 구성 옵션에 대한 자세한 내용은 [_구성 참조 안내서_](../configuration-reference/general/content-management.md).

## Configure [!DNL Page Builder]

1. 다음에서 _관리자_ 사이드바, 이동 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. 아래의 왼쪽 패널에서 _[!UICONTROL General]_, 선택&#x200B;**[!UICONTROL Content Management]**.

1. 확장 ![확장 선택기](../assets/icon-display-expand.png) **[!UICONTROL Advanced Content Tools]** 및 확인 **[!UICONTROL Enable Page Builder]** 이(가) (으)로 설정됨 `Yes`.

   ![고급 콘텐츠 도구](../configuration-reference/general/assets/content-management-advanced-content-tools.png){width="600" zoomable="yes"}

1. 설정할 준비가 되면 [!DNL Google Maps]를 사용하여 다음을 수행합니다.

   - 필요한 경우 [API 키 가져오기][1] 지침, 복사 및 붙여넣기 **[!UICONTROL Google Maps API Key]**.

   - 을(를) 변경하려면 **[!UICONTROL Google Maps Style]**&#x200B;에 의해 생성된 JSON 코드를 붙여 넣습니다. [[!DNL Google Maps] API 스타일 마법사][2].

   >[!NOTE]
   >
   >다음을 참조하십시오 [미디어 - 맵](map.md) 사용에 대한 자세한 내용 [!DNL Google Maps] (으)로 [!DNL Page Builder] 콘텐츠.

1. 의 지침 수를 구성하려면 [!DNL Page Builder] 열 그리드에서 다음을 수행합니다.

   - 대상 **[!UICONTROL Default Column Grid Size]**&#x200B;그리드에 표시할 기본 열 수를 입력합니다.

   - 대상 **[!UICONTROL Maximum Column Grid Size]**&#x200B;그리드에서 사용할 수 있게 하려는 열 수를 가장 많이 입력합니다.

   >[!NOTE]
   >
   >다음을 참조하십시오 [레이아웃 - 열](column.md) 를 사용하여 작업할 때 열 그리드를 사용하는 방법에 대한 자세한 내용 [!DNL Page Builder] 콘텐츠.

1. 완료되면 다음을 클릭하십시오. **[!UICONTROL Save Config]**.

## 기본 레이아웃 구성

1. 다음에서 _관리자_ 사이드바, 이동 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. 아래의 왼쪽 패널에서 _[!UICONTROL General]_, 선택&#x200B;**[!UICONTROL Web]**.

1. 확장 ![확장 선택기](../assets/icon-display-expand.png) **[!UICONTROL Default Layouts]** 다음을 수행합니다.

   ![기본 레이아웃](../configuration-reference/general/assets/web-default-layouts.png){width="600" zoomable="yes"}

   웹 구성 옵션에 대한 자세한 내용은 [_구성 참조 안내서_](../configuration-reference/general/web.md#default-layouts).

   - 다음을 선택합니다. **[!UICONTROL Default Product Layout]** 제품 페이지에 사용할 수 있습니다.

   - 다음을 선택합니다. **[!UICONTROL Default Category Layout]** 범주 페이지에 사용할 수 있습니다.

   - 다음을 선택합니다. **[!UICONTROL Default Page Layout]** CMS 페이지에 사용할 수 있습니다.

1. 완료되면 다음을 클릭하십시오. **[!UICONTROL Save Config]**.

## 사용 안 함 [!DNL Page Builder]

>[!NOTE]
>
>비활성화 중 [!DNL Page Builder] 고급 콘텐츠 도구를 WYSIWYG로 바꿉니다. [편집자](../content-design/editor.md), 이로 인해 상점 첫 화면에서 디스플레이 오류가 발생할 수 있습니다. 이전에 만든 콘텐츠 [!DNL Page Builder] 관리자에서는 편집할 수 없습니다.

1. 다음에서 _관리자_ 사이드바, 이동 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. 아래의 왼쪽 패널에서 _[!UICONTROL General]_, 선택&#x200B;**[!UICONTROL Content Management]**.

1. 확장 ![확장 선택기](../assets/icon-display-expand.png) **[!UICONTROL Advanced Content Tools]** 및 설정 **[!UICONTROL Enable Page Builder]** 끝 `No`.

1. 확인을 묻는 메시지가 나타나면 **[!UICONTROL Turn Off]**.

1. 완료되면 다음을 클릭하십시오. **[!UICONTROL Save Config]**.

1. 메시지가 표시되면 [새로 고침](../systems/cache-management.md) 모든 잘못된 캐시.

[1]: https://developers.google.com/maps/documentation/javascript/get-api-key
[2]: https://mapstyle.withgoogle.com/
