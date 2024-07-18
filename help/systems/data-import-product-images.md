---
title: 제품 이미지 가져오기
description: 각 이미지의 경로 및 파일 이름을 사용하여 제품 이미지를 가져오는 방법을 알아봅니다.
exl-id: 991550e6-9ce2-4472-becb-3492bd4c9582
feature: Products, Data Import/Export, Media
source-git-commit: 53c3b6c9fa9c152e6619528a43580b0acc71a2a5
workflow-type: tm+mt
source-wordcount: '836'
ht-degree: 0%

---

# 제품 이미지 가져오기

각 유형의 여러 제품 이미지를 Adobe Commerce 및 Magento Open Source으로 가져와서 특정 제품과 연결할 수 있습니다. 각 제품 이미지의 경로와 파일 이름을 CSV 파일에 입력하고, 가져올 이미지 파일을 Commerce 서버 또는 외부 서버의 해당 경로에 업로드합니다.

Commerce은 알파벳순으로 구성된 제품 이미지에 대한 고유한 디렉토리 구조를 만듭니다. 기존 이미지가 포함된 제품 데이터를 CSV 파일로 내보낼 때 각 이미지의 파일 이름 앞에 알파벳순으로 배열된 경로가 표시됩니다. 그러나 새 이미지를 가져올 때 Commerce에서 디렉터리 구조를 자동으로 관리하기 때문에 경로를 지정할 필요가 없습니다. 가져올 각 이미지의 파일 이름 앞에 가져오기 디렉토리의 상대 경로를 입력해야 합니다.

이미지를 업로드하려면 로그인 자격 증명과 서버의 Commerce 폴더에 액세스할 수 있는 올바른 권한이 있어야 합니다. 올바른 자격 증명을 사용하여 모든 SFTP 유틸리티를 사용하여 데스크탑 컴퓨터에서 서버로 파일을 업로드할 수 있습니다.

많은 이미지를 가져오기 전에 사용할 가져오기 메서드의 단계를 검토하고 몇 가지 제품을 사용하여 프로세스를 실행합니다. 작동 방식을 이해하면 대량의 이미지를 가져올 수 있다는 자신감이 생깁니다.

>[!IMPORTANT]
>
>메모장++과 같은 CSV 파일을 편집하려면 UTF-8 인코딩을 지원하는 프로그램을 사용하는 것이 좋습니다. Microsoft® Excel은 CSV 파일의 열 헤더에 추가 문자를 삽입하므로 데이터를 Commerce으로 다시 가져올 수 없습니다.

## 방법 1: 로컬 서버에서 이미지 가져오기

1. Commerce 서버에서 `var/import/images` 폴더 또는 하위 폴더(예: `var/import/images/product_images`)에 이미지 파일을 업로드합니다. 제품 이미지를 가져오기 위한 기본 루트 폴더입니다.

   ```
   <Magento root folder>/var/import/images
   ```

   >[!NOTE]
   >
   >Adobe Commerce 및 Magento Open Source `2.3.2` 릴리스부터 **[!UICONTROL Images File Directory]**&#x200B;에 지정된 경로는 이미지 기본 디렉터리(`<Magento-root-folder>/var/import/images`)로 가져오기 위해 연결됩니다. 이전 Adobe Commerce 및 Magento Open Source 릴리스의 경우 가져오기 프로세스 중에 폴더 경로가 지정되는 한 Commerce 서버에서 다른 폴더를 사용할 수 있습니다.

1. CSV 데이터에서 이미지 유형(`base_image`, `small_image`, `thumbnail_image` 또는 `additional_images`)에 따라 올바른 행과 올바른 열에 가져올 각 이미지 파일의 이름을 `sku`씩 입력합니다.

   >[!NOTE]
   >
   >기본 가져오기 폴더(`var/import/images`)에 있는 이미지의 경우 CSV 데이터에서 파일 이름 앞의 경로를 포함하지 마십시오.

   CSV 파일에는 `sku` 열과 관련 이미지 열만 포함되어야 합니다.

   ![예 - CSV 이미지 데이터 가져오기](./assets/data-import-csv-image-files-default-local.png){width="600" zoomable="yes"}

1. 지침을 따라 데이터를 [가져오기](data-import.md)합니다.

1. 가져올 파일을 선택한 후 **[!UICONTROL Images File Directory]** 다음에 상대 경로를 입력하십시오.

   ```
   var/import/images
   ```

   ![이미지 파일 디렉터리 데이터 가져오기](./assets/data-import-file-to-import.png){width="600" zoomable="yes"}

   >[!TIP]
   >
   >`<Magento-root-folder>/var/import/images` 디렉터리를 사용하려면 _[!UICONTROL Images File Directory]_을(를) 비워 둡니다. Adobe Commerce 및 Magento Open Source 버전 2.3.2부터 기본 가져오기 이미지 기본 디렉토리입니다.

   단일 `sku`에 대해 여러 이미지를 가져오는 경우 `additional_images` 열에 이미지를 삽입합니다(아직 추가되지 않은 경우 열 추가). 쉼표로 구분합니다. 예: `image02.jpg,image03.jpg`

## 방법 2: 외부 서버에서 이미지 가져오기

1. 외부 서버의 지정된 폴더로 가져올 이미지를 업로드합니다.

1. CSV 데이터에서 이미지 유형(`base_image`, `small_image`, `thumbnail_image` 또는 `additional_images`)별로 올바른 열에 각 이미지 파일의 전체 URL을 입력합니다.

   ```
   https://example.com/images/image.jpg
   ```

1. 지침을 따라 데이터를 [가져오기](data-import.md)합니다.

## 방법 3: 원격 저장소로 이미지 가져오기

1. 원격 저장소 모듈에서 `var/import/images` 폴더 또는 하위 폴더(예: `var/import/images/product_images`)에 이미지 파일을 업로드합니다. 제품 이미지를 가져오기 위한 기본 루트 폴더입니다.

   ```bash
   <remote-storage-root-folder>/var/import/images
   ```

   >[!NOTE]
   >
   >Adobe Commerce 및 Magento Open Source `2.3.2` 릴리스부터 _[!UICONTROL Images File Directory]_에 지정된 경로가 이미지 기본 디렉터리로 가져오기 위해 연결됩니다. `<remote-storage-root-folder>/var/import/images`. 이전 Adobe Commerce 및 Magento Open Source 릴리스의 경우 가져오기 프로세스 중에 폴더 경로가 지정되는 한 Commerce 서버에서 다른 폴더를 사용할 수 있습니다.

1. CSV 데이터에서 이미지 유형(`base_image`, `small_image`, `thumbnail_image` 또는 `additional_images`)에 따라 올바른 행과 올바른 열에 가져올 각 이미지 파일의 이름을 `sku`씩 입력합니다.

   >[!NOTE]
   >
   >기본 가져오기 폴더(`var/import/images`)에 있는 이미지의 경우 CSV 데이터에서 파일 이름 앞의 경로를 포함하지 마십시오.

   CSV 파일에는 `sku` 열과 관련 이미지 열만 포함되어야 합니다.

   ![예 - CSV 이미지 데이터 가져오기](./assets/data-import-csv-image-files-default-local.png){width="600" zoomable="yes"}

1. 지침을 따라 데이터를 [가져오기](data-import.md)합니다.

1. 가져올 파일을 선택한 후 **[!UICONTROL Images File Directory]** 다음에 상대 경로를 입력하십시오.

   ```
   var/import/images/product_images
   ```

   >[!TIP]
   >
   >`<Magento-root-folder>/var/import/images` 디렉터리를 사용하려면 _[!UICONTROL Images File Directory]_을(를) 비워 둡니다. Adobe Commerce 및 Magento Open Source 버전 2.3.2부터 기본 가져오기 이미지 기본 디렉토리입니다.

   단일 `sku`에 대해 여러 이미지를 가져오는 경우 `additional_images` 열에 이미지를 삽입하십시오(아직 추가되지 않은 경우 열 추가). 쉼표로 구분하십시오. `image02.jpg,image03.jpg`

원격 저장소 모듈 사용 및 관리에 대한 자세한 내용은 _구성 가이드_&#x200B;에서 [원격 저장소 구성](https://experienceleague.adobe.com/docs/commerce-operations/configuration-guide/storage/remote-storage/remote-storage.html)을 참조하세요.

>[!NOTE]
>
>제품 이미지를 가져오더라도 이미지 크기 조정은 시작되지 않습니다. 제품 이미지 크기는 `pub/get.php`(으)로 프런트 엔드에서 조정됩니다. `pub/get.php`이(가) 제대로 작동하는지 확인하십시오. 그렇지 않으면 이미지 크기가 조정되지 않을 수 있습니다.
