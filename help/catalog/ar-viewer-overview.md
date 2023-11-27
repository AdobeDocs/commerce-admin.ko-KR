---
title: '''[!DNL AR Viewer] Adobe Commerce용'
description: 다음 방법을 알아봅니다. [!DNL AR Viewer] 는 Adobe Commerce 인스턴스 및 확장을 성공적으로 온보딩하고 설정하는 방법에 도움이 될 수 있습니다.
exl-id: 9f9f3ff3-2402-4f70-9fc7-031dd2bb3916
source-git-commit: f84667a7bbc93504499279d77967796bcd11791c
workflow-type: tm+mt
source-wordcount: '240'
ht-degree: 0%

---

# [!DNL AR Viewer] Adobe Commerce용

증강 현실(AR)은 2D 또는 3D 요소를 실제 세계에 서식하는 것처럼 보이도록 하는 방식으로 장치의 카메라에서 라이브 뷰에 추가하는 사용자 경험을 설명합니다.

다음 [!DNL AR Viewer] for Adobe Commerce 확장은 렌더링된 3D 그래픽을 사용자에게 표시하도록 설계된 원활한 경험을 제공합니다.

이 안내서의 정보는에 대한 온보딩 경험에 대한 개요를 제공합니다. [!DNL AR Viewer] Adobe Commerce 및 [!DNL AR Viewer] 은 사용자에게 이점을 제공하며 해당 여정 시 따라야 할 모범 사례도 제공합니다.

Pixar에서 개발, [범용 장면 설명(USD)](https://www.pixar.com/usd){target=_blank} 은 다양한 에셋, 소스 및 애니메이션으로 구성될 수 있는 3D 장면을 강력하고 확장 가능한 방식으로 교환하는 동시에 고도의 공동 작업 워크플로우를 개발할 수 있는 최초의 오픈 소스 소프트웨어입니다. 이 USD는 다음 범위 내에서 사용됩니다. `.USDZ` 파일. 이 `.USDZ` 파일은 사용자의 장치에 AR 및 3D 컨텐츠를 전달합니다.

>[!NOTE]
>
> 다음 [!DNL AR Viewer] 만 지원 `.USDZ` 파일.

## [!DNL AR Viewer] 요구 사항

다음 [!DNL AR Viewer] 은(는) 둘 다와 호환됩니다. [!DNL Magento Open Source] 그리고 Adobe Commerce. 다음을 참조하십시오 [수명 주기 정책](https://experienceleague.adobe.com/docs/commerce-operations/release/planning/lifecycle-policy.html){target=_blank} 를 참조하십시오.

다음을 참조하십시오 [설치 [!DNL AR Viewer] 확장](../catalog/ar-viewer-setup.md) 추가 정보.

를 사용하려면 [!DNL AR Viewer]를 사용하려면 인스턴스에 사용할 수 있는 다음 항목이 있어야 합니다.

* PHP 8.1.0
* Adobe Commerce 버전 2.4.4 이상
* Magento Open Source(CE) 버전 2.4.x

## 호환성 제한 사항

[!DNL AR Viewer] 기존 호환성 제한 사항:

* `.USDZ` 전용: 이 기능은 `.USDZ` 파일.
* `qr-code`: 필요 `endroid/qr-code` 버전 4.5.
* `Catalog module`: 필요 `magento/module-catalog` 버전 104.0.0.
