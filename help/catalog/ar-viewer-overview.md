---
title: Adobe Commerce용 '[!DNL AR Viewer]'
description: ' [!DNL AR Viewer] 이(가) Adobe Commerce 인스턴스에 어떤 이점을 줄 수 있는지, 그리고 확장을 성공적으로 온보딩하고 설정하는 방법에 대해 알아봅니다.'
exl-id: 9f9f3ff3-2402-4f70-9fc7-031dd2bb3916
source-git-commit: f8254db7d69e58c8e9a78948ee6e40f5ea88cea0
workflow-type: tm+mt
source-wordcount: '239'
ht-degree: 0%

---

# Adobe Commerce용 [!DNL AR Viewer]

증강 현실(AR)은 2D 또는 3D 요소를 실제 세계에 서식하는 것처럼 보이도록 하는 방식으로 장치의 카메라에서 라이브 뷰에 추가하는 사용자 경험을 설명합니다.

[!DNL AR Viewer] for Adobe Commerce 확장은 렌더링된 3D 그래픽을 사용자에게 표시하도록 디자인된 원활한 경험을 제공합니다.

이 안내서의 정보는 Adobe Commerce의 [!DNL AR Viewer]에 대한 온보딩 경험에 대한 개요와 [!DNL AR Viewer]이(가) 사용자에게 어떤 이점을 제공하는지, 그리고 해당 여정에 따라 따라야 할 모범 사례를 제공합니다.

Pixar에서 개발한 [USD(Universal Scene Description)](https://openusd.org/release/index.html){target=_blank}은(는) 매우 다양한 에셋, 소스 및 애니메이션으로 구성될 수 있는 3D 장면을 강력하고 확장 가능한 방식으로 교환하는 동시에 고도의 공동 작업 워크플로우를 개발할 수 있는 최초의 오픈 소스 소프트웨어입니다. 이 USD는 `.USDZ`개 파일 내에서 사용됩니다. 이 `.USDZ` 파일은 AR 및 3D 콘텐츠를 사용자의 장치에 전달합니다.

>[!NOTE]
>
> [!DNL AR Viewer]은(는) `.USDZ`개의 파일만 지원합니다.

## [!DNL AR Viewer] 요구 사항

[!DNL AR Viewer]은(는) [!DNL Magento Open Source] 및 Adobe Commerce 모두와 호환됩니다. 지원되는 버전에 대한 자세한 내용은 [라이프사이클 정책](https://experienceleague.adobe.com/docs/commerce-operations/release/planning/lifecycle-policy.html){target=_blank}을 참조하십시오.

자세한 내용은 [확장 설치 [!DNL AR Viewer] 2}를 참조하십시오.](../catalog/ar-viewer-setup.md)

[!DNL AR Viewer]을(를) 사용하려면 인스턴스에 사용할 수 있는 다음 항목이 있어야 합니다.

* PHP 8.1.0
* Adobe Commerce 버전 2.4.4 이상
* Magento Open Source(CE) 버전 2.4.x

## 호환성 제한 사항

기존 호환성 제한 [!DNL AR Viewer]개:

* `.USDZ`만 해당: 이 기능은 `.USDZ`개의 파일만 지원합니다.
* `qr-code`: `endroid/qr-code` 버전 4.5가 필요합니다.
* `Catalog module`: `magento/module-catalog` 버전 104.0.0이 필요합니다.
