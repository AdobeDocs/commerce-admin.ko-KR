---
title: Adobe Stock 이미지에 라이센스 부여
description: 법적 액세스 권한을 확보하고 Adobe Stock 워터마크를 제거하려면 Adobe Stock 이미지에 라이선스를 부여하십시오.
exl-id: a2d6b7b8-e9ac-4f3e-bcd1-05e2bb74b6c2
feature: CMS, Media
source-git-commit: b659c7e1e8f2ae9883f1e24d8045d6dd1e90cfc0
workflow-type: tm+mt
source-wordcount: '372'
ht-degree: 0%

---

# Adobe Stock 이미지에 라이센스 부여

프로덕션 Adobe Commerce 및 Magento Open Source 스토어에 사용하려는 Adobe Stock 자산에 라이센스가 있어야 합니다. 이 라이센스를 통해 이미지에 대한 법적 액세스 권한을 확보하고 모든 이미지에 있는 Adobe Stock 워터마크를 제거할 수 있습니다 [이미지 미리 보기][save-preview]. 이미지에 라이선스를 부여하거나 이미 라이선스가 부여된 이미지를 저장하려면 Adobe 계정에 로그인해야 합니다.

새로운 [[!DNL Media Gallery]](media-gallery.md) 은 Adobe Stock과 직접 통합되므로 갤러리 페이지에서 직접 이미지에 라이선스를 부여하기가 쉽습니다.

## 전제 조건

이 기능을 사용하려면 [Adobe Stock 통합][adobe-stock-integration] 모듈 및 구성 라이선스 [Adobe Stock][adobe-stock] 이미지에는 유료 Adobe Stock 플랜 및 [Adobe 계정][adobe-signin].

## 새 이미지에서 이미지 라이센스 부여 [!DNL Media Gallery]

1. 다음에서 _관리자_ 사이드바, 이동 **[!UICONTROL Content]** > _[!UICONTROL Media]_>**[!UICONTROL Media Gallery]**.

1. 의 단계를 따릅니다. [Adobe Stock 이미지 사용][using-adobe-stock] 에 로그인하고 미리보기 이미지를 저장하려면 [미디어 스토리지][media-storage].

   ![저장된 미리 보기 이미지](./assets/adobe-stock-gallery-unlicensed.png){width="600" zoomable="yes"}

1. 이미지 아래의 세 점을 클릭합니다(![에셋 메뉴 아이콘](./assets/media-gallery-asset-menu-icon.png){width="10" zoomable="no"})을 클릭한 다음 **[!UICONTROL License]**.

   ![Adobe Stock 이미지 작업](./assets/adobe-stock-gallery-image-actions.png){width="600" zoomable="yes"}

   >[!NOTE]
   >
   >로그인하지 않은 경우 로그인 양식이 나타납니다. 로그인에 대한 자세한 내용은 [Adobe Stock 이미지 사용][using-adobe-stock].

1. 라이센스 확인 대화 상자에서 **[!UICONTROL Confirm]** 이미지에 라이선스를 부여합니다.

   ![라이센스 확인](./assets/adobe-stock-gallery-license-confirm.png){width="350" zoomable="yes"}

   >[!NOTE]
   >
   >사용할 수 있어야 합니다. [Adobe Stock 크레딧][stock-credits] 을(를) 통해 이미지에 라이선스를 부여하십시오.

## 표준 미디어 스토리지에서 이미지 라이센스 부여

1. [Adobe Stock 검색 그리드 액세스][access-search].

1. 종료 [이미지 세부 사항 보기][view-details]검색 그리드에서 이미지를 순서대로 클릭합니다.

1. 이미지의 현재 라이센스 상태에 따라 다음 중 하나를 수행합니다.

   - 이미지에 이미 라이선스가 부여된 경우 **[!UICONTROL Save]**.

   - 이미지가 _아님_ 라이센스 부여됨, 클릭 **[!UICONTROL License and Save]**.

     >[!NOTE]
     >
     >사용할 수 있어야 합니다. [Adobe Stock 크레딧][stock-credits] 을(를) 통해 이미지에 라이선스를 부여하십시오.

   이 작업은 이미지를 로 저장하는 데 사용되는 파일 이름을 지정하라는 메시지를 표시합니다. [미디어 스토리지][media-storage]. 기본 파일 이름이 제공되지만 기본 설정에 따라 이름을 사용자 지정할 수 있습니다.

   ![Adobe Stock 라이선스 이미지 저장](./assets/adobe-stock-save-licensed.png){width="550" zoomable="yes"}

1. 클릭 **[!UICONTROL Confirm]**.

   페이지가 미디어 스토리지로 리디렉션되고 저장된 미리보기가 표시됩니다.

[adobe-stock-integration]: adobe-stock.md
[media-storage]: media-storage.md
[using-adobe-stock]: adobe-stock-manage.md
[save-preview]: adobe-stock-save-preview.md
[access-search]: adobe-stock-manage.md#access-the-adobe-stock-search-grid
[view-details]: adobe-stock-manage.md#view-image-details
[stock-credits]: https://helpx.adobe.com/stock/help/credit-packs.html
[adobe-stock]: https://stock.adobe.com
[adobe-signin]: https://helpx.adobe.com/manage-account/using/access-adobe-id-account.html
