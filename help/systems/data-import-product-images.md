---
title: 제품 이미지 가져오기
description: 각 이미지의 경로 및 파일 이름을 사용하여 제품 이미지를 가져오는 방법을 알아봅니다.
exl-id: 991550e6-9ce2-4472-becb-3492bd4c9582
feature: Products, Data Import/Export, Media
source-git-commit: 64ccc2d5016e915a554c2253773bb50f4d33d6f4
workflow-type: tm+mt
source-wordcount: '835'
ht-degree: 0%

---

# 제품 이미지 가져오기

각 유형의 여러 제품 이미지를 Adobe Commerce 및 Magento Open Source으로 가져와서 특정 제품과 연결할 수 있습니다. 각 제품 이미지의 경로와 파일 이름을 CSV 파일에 입력하고, 가져올 이미지 파일을 Commerce 서버나 외부 서버의 해당 경로에 업로드합니다.

Commerce는 알파벳순으로 구성된 제품 이미지에 대해 고유한 디렉토리 구조를 만듭니다. 기존 이미지가 포함된 제품 데이터를 CSV 파일로 내보낼 때 각 이미지의 파일 이름 앞에 알파벳순으로 배열된 경로가 표시됩니다. 그러나 새 이미지를 가져올 때는 Commerce에서 디렉터리 구조를 자동으로 관리하기 때문에 경로를 지정할 필요가 없습니다. 가져올 각 이미지의 파일 이름 앞에 가져오기 디렉토리의 상대 경로를 입력해야 합니다.

이미지를 업로드하려면 로그인 자격 증명과 서버의 상거래 폴더에 액세스할 수 있는 올바른 권한이 있어야 합니다. 올바른 자격 증명을 사용하여 모든 SFTP 유틸리티를 사용하여 데스크탑 컴퓨터에서 서버로 파일을 업로드할 수 있습니다.

많은 이미지를 가져오기 전에 사용할 가져오기 메서드의 단계를 검토하고 몇 가지 제품을 사용하여 프로세스를 실행합니다. 작동 방식을 이해하면 대량의 이미지를 가져올 수 있다는 자신감이 생깁니다.

>[!IMPORTANT]
>
>메모장++과 같은 CSV 파일을 편집하려면 UTF-8 인코딩을 지원하는 프로그램을 사용하는 것이 좋습니다. Microsoft® Excel에서는 CSV 파일의 열 헤더에 추가 문자가 삽입되므로 데이터를 Commerce로 다시 가져올 수 없습니다.

## 방법 1: 로컬 서버에서 이미지 가져오기

1. Commerce 서버에서 이미지 파일을 `var/import/images` 폴더 또는 하위 폴더(예: ) `var/import/images/product_images`. 제품 이미지를 가져오기 위한 기본 루트 폴더입니다.

   ```terminal
   <Magento root folder>/var/import/images
   ```

   >[!NOTE]
   >
   Adobe Commerce 및 Magento Open Source 시작 `2.3.2` 릴리스 (에 지정된 경로) **[!UICONTROL Images File Directory]** 이미지 기본 디렉토리로 가져오기 위해 연결 - `<Magento-root-folder>/var/import/images`. 이전 Adobe Commerce 및 Magento Open Source 릴리스의 경우 가져오기 프로세스 중에 폴더 경로가 지정되는 한 Commerce 서버에서 다른 폴더를 사용할 수 있습니다.

1. CSV 데이터에서 올바른 행에 가져올 각 이미지 파일의 이름을 다음과 같이 입력합니다. `sku`, 이미지 유형에 따라 올바른 열의 및`base_image`, `small_image`, `thumbnail_image`, 또는 `additional_images`).

   >[!NOTE]
   >
   기본 가져오기 폴더의 이미지(`var/import/images`) CSV 데이터에서 파일 이름 앞의 경로를 포함하지 마십시오.

   CSV 파일에는 다음 항목만 포함되어야 합니다. `sku` 열과 관련 이미지 열

   ![예 - CSV 이미지 데이터 가져오기](./assets/data-import-csv-image-files-default-local.png){width="600" zoomable="yes"}

1. 다음 지침을 따르십시오 [가져오기](data-import.md) 데이터.

1. 가져올 파일을 선택한 후 다음에 상대 경로를 입력합니다 **[!UICONTROL Images File Directory]**.

   ```terminal
   var/import/images
   ```

   ![데이터 가져오기 이미지 파일 디렉터리](./assets/data-import-file-to-import.png){width="600" zoomable="yes"}

   >[!TIP]
   >
   나가기 _[!UICONTROL Images File Directory]_을(를) 사용하려면 비어 있음 `<Magento-root-folder>/var/import/images` 디렉토리. Adobe Commerce 및 Magento Open Source 버전 2.3.2부터 기본 가져오기 이미지 기본 디렉토리입니다.

   단일 로 여러 이미지를 가져오는 경우 `sku`, 라는 열에 이미지 삽입 `additional_images` (아직 추가되지 않은 경우 열 추가), 쉼표로 구분합니다. 예: `image02.jpg,image03.jpg`

## 방법 2: 외부 서버에서 이미지 가져오기

1. 외부 서버의 지정된 폴더로 가져올 이미지를 업로드합니다.

1. CSV 데이터에서 각 이미지 파일의 전체 URL을 이미지 유형별로 올바른 열에 입력합니다(`base_image`, `small_image`, `thumbnail_image`, 또는 `additional_images`).

   ```terminal
   https://example.com/images/image.jpg
   ```

1. 다음 지침을 따르십시오 [가져오기](data-import.md) 데이터.

## 방법 3: 원격 저장소로 이미지 가져오기

1. 원격 스토리지 모듈에서 이미지 파일을 `var/import/images` 폴더 또는 하위 폴더(예: ) `var/import/images/product_images`. 제품 이미지를 가져오기 위한 기본 루트 폴더입니다.

   ```terminal
   <remote-storage-root-folder>/var/import/images
   ```

   >[!NOTE]
   >
   Adobe Commerce 및 Magento Open Source 시작 `2.3.2` 릴리스 (에 지정된 경로) _[!UICONTROL Images File Directory]_이미지 기본 디렉토리로 가져오기 위해 를 연결합니다. `<remote-storage-root-folder>/var/import/images`. 이전 Adobe Commerce 및 Magento Open Source 릴리스의 경우 가져오기 프로세스 중에 폴더 경로가 지정되는 한 Commerce 서버에서 다른 폴더를 사용할 수 있습니다.

1. CSV 데이터에서 올바른 행에 가져올 각 이미지 파일의 이름을 다음과 같이 입력합니다. `sku`, 이미지 유형에 따라 올바른 열의 및`base_image`, `small_image`, `thumbnail_image`, 또는 `additional_images`).

   >[!NOTE]
   >
   기본 가져오기 폴더의 이미지(`var/import/images`) CSV 데이터에서 파일 이름 앞의 경로를 포함하지 마십시오.

   CSV 파일에는 다음 항목만 포함되어야 합니다. `sku` 열과 관련 이미지 열

   ![예 - CSV 이미지 데이터 가져오기](./assets/data-import-csv-image-files-default-local.png){width="600" zoomable="yes"}

1. 다음 지침을 따르십시오 [가져오기](data-import.md) 데이터.

1. 가져올 파일을 선택한 후 다음에 상대 경로를 입력합니다 **[!UICONTROL Images File Directory]**.

   ```terminal
   var/import/images/product_images
   ```

   >[!TIP]
   >
   나가기 _[!UICONTROL Images File Directory]_을(를) 사용하려면 비어 있음 `<Magento-root-folder>/var/import/images` 디렉토리. Adobe Commerce 및 Magento Open Source 버전 2.3.2부터 기본 가져오기 이미지 기본 디렉토리입니다.

   단일 로 여러 이미지를 가져오는 경우 `sku`, 라는 열에 이미지 삽입 `additional_images` (아직 추가되지 않은 경우 열 추가), 쉼표로 구분: `image02.jpg,image03.jpg`

원격 스토리지 모듈 사용 및 관리에 대한 자세한 내용은 [원격 스토리지 구성](https://experienceleague.adobe.com/docs/commerce-operations/configuration-guide/storage/remote-storage/remote-storage.html) 다음에서 _구성 안내서_.

>[!NOTE]
>
제품 이미지를 가져오더라도 이미지 크기 조정은 시작되지 않습니다. 제품 이미지 크기는 다음 방법으로 프런트 엔드에서 조절됩니다. `pub/get.php`. 다음을 확인하십시오. `pub/get.php` 이(가) 제대로 작동하지 않습니다. 그렇지 않으면 이미지 크기가 조정되지 않을 수 있습니다.
