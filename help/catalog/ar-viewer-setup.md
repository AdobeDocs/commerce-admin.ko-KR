---
title: '[!DNL AR Viewer] Adobe Commerce 설치'
description: 를 사용하여 3D 모델 에셋 관리에 대해 알아봅니다. [!DNL AR Viewer] 제품 목록 확장명.
exl-id: e3f081ff-b994-4842-a1f3-613012d33a9c
source-git-commit: f84667a7bbc93504499279d77967796bcd11791c
workflow-type: tm+mt
source-wordcount: '307'
ht-degree: 0%

---

# 를 사용하여 제품 3D 모델 관리 [!DNL AR Viewer] Adobe Commerce용

각 제품에 대해 `.USDZ` AR 및 3D 모델을 제품 목록에 사용할 수 있도록 해 주는 파일입니다.

다음 [!DNL AR Viewer] 만 지원 `.USDZ` 파일.

## 확장 설치

[!DNL AR Viewer] 에서 확장으로 설치됩니다. [Adobe Commerce 마켓플레이스](https://commercemarketplace.adobe.com/magento-module-arviewer.html){target=_blank}.

다음을 참조하십시오. [_설치 안내서_](https://experienceleague.adobe.com/docs/commerce-operations/installation-guide/tutorials/extensions.html) 확장 설치 프로세스에 대한 자세한 내용을 보려면 .

다음 이후 [!DNL AR Viewer] 확장이 설치 및 구성되어 있으면 관리자는 3D 모델을 포함하도록 제품 목록을 설정, 사용자 지정 및 관리할 수 있습니다.

## 3D 모델 추가

1. 제품을 편집 모드로 엽니다.

1. 특정 스토어 보기로 작업하려면 **[!UICONTROL Store View]** 해당 뷰를 선택합니다.

   >[!NOTE]
   >
   >새로운 제품 3D 모델은 다음과 같습니다. _항상_ 업로드되고 표시되는 위치: _모두_ 다음과 같은 경우에도 보기 저장 `All Store Views` 업로드에는 범위가 사용되지 않습니다. <br/><br/>특정 스토어 보기에서 제품 3D 모델을 숨기려면 해당 스토어 보기로 전환한 다음 **[!UICONTROL Hide from Product Page]** 3D 모델의 확인란을 선택하고 **[!UICONTROL Save]**.

1. 아래로 스크롤하고 를 확장합니다. _[!UICONTROL Product 3D Model]_섹션.

   ![메뉴 팝업](assets/ar-viewer-product-options.png){width="700" zoomable="yes"}

1. 3D 모델 추가(`.USDZ` file)을 포함할 필요가 없습니다.

1. 클릭 **[!UICONTROL Save]**.

### 3D 모델 삭제

제품 세부 사항에서 3D 모델을 제거하려면 다음 작업을 수행하십시오.

1. 클릭 **[!UICONTROL Delete]**.

1. 클릭 **[!UICONTROL Save]**.

## 제품 3D 모델 보기

제품 세부 사항이 3D 모델로 업데이트되는 경우:

1. 다음 [!DNL AR Viewer] 는 AR 파일을 인코딩하는 제품 설명에 QR 코드를 생성합니다.

1. 고객은 제품 페이지에서 이 QR 코드를 볼 수 있습니다.

1. 고객이 모바일 장치로 QR 코드를 스캔하면 AR 경험이 모바일 장치에서 렌더링됩니다.

>[!NOTE]
>
> 사용자가 제품에 3d 모델을 추가하는 일련의 데모 비디오는 [Adobe Commerce용 AR 뷰어](https://experienceleague.adobe.com/docs/commerce-learn/tutorials/catalog/augmented-reality.html) 페이지 위치 _Commerce 비디오 및 Tutorials_.
