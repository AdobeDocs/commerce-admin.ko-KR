---
title: 다운로드 가능한 제품 가져오기
description: 다운로드 가능한 제품에 대한 제품 데이터 가져오기의 예를 검토하십시오.
exl-id: e0b45ef5-dff1-4ee4-aa7e-2407162669fd
feature: Products, Data Import/Export
source-git-commit: 64ccc2d5016e915a554c2253773bb50f4d33d6f4
workflow-type: tm+mt
source-wordcount: '172'
ht-degree: 0%

---

# 다운로드 가능한 제품 가져오기

다운로드 가능한 제품을 가져오는 흐름은 [번들 제품](data-transfer-bundle-products.md) 또는 [구성 가능한 제품](data-transfer-configurable-products.md)과 동일합니다. 차이점은 다운로드 가능한 제품에 이미지가 포함된 [다운로드 가능한 링크](../catalog/product-create-downloadable.md)와 [다운로드 가능한 샘플](../catalog/product-create-downloadable.md)이 있다는 것입니다.

다운로드 가능한 링크 및 샘플의 기본 루트 디렉터리는 `<Magento-root-folder>/pub/media/import`입니다. 원격 저장소 모듈이 활성화된 경우 다운로드 가능한 링크 및 샘플의 기본 루트 디렉터리는 `<remote-storage-root-folder>/media/import` 디렉터리입니다.

CSV 파일에 `downloadable_links`과(와) `downloadable_samples`에 대한 별도의 열이 있습니다.

- **다운로드 가능한 링크 이미지** — 다음 예제에서는 다운로드 가능한 링크 이미지(`red.jpg` 및 `black.jpg`)가 `<Magento-root-folder>/pub/media/import/test` 폴더에 있습니다. 원격 저장소를 사용하는 경우 해당 이미지는 `<remote-storage-root-folder>/media/import/test` 폴더에 있습니다.

  ![예제 데이터 - 다운로드 가능한 링크가 있는 다운로드 가능한 제품](./assets/data-import-downloadable-links.png){width="600" zoomable="yes"}

- **다운로드 가능한 샘플 이미지** — 다음 예제에서는 다운로드 가능한 샘플 이미지(`white.jpg`)가 `<Magento-root-folder>/pub/media/import/test` 폴더에 있습니다. 원격 저장소를 사용하도록 설정한 경우 이 이미지는 `<remote-storage-root-folder>/media/import/test` 폴더에 있습니다.

  ![예제 데이터 - 다운로드 가능한 샘플이 있는 다운로드 가능한 제품](./assets/data-import-downloadable-samples.png){width="400" zoomable="yes"}

원격 저장소 모듈 사용 및 관리에 대한 자세한 내용은 _구성 가이드_&#x200B;의 [원격 저장소 구성](https://experienceleague.adobe.com/docs/commerce-operations/configuration-guide/storage/remote-storage/remote-storage.html?lang=ko)을 참조하세요.
