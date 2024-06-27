---
title: 데이터 전송
description: 데이터 유효성 검사를 포함한 데이터 전송 지원에 대해 알아봅니다.
exl-id: 5057e398-c458-42e9-8ec0-bf116a667a3c
feature: System, Data Import/Export
source-git-commit: b89d6b08d0559dc769a8c51570696f033f23c7f3
workflow-type: tm+mt
source-wordcount: '488'
ht-degree: 0%

---

# 데이터 전송

가져오기 및 내보내기 도구를 사용하여 한 번의 작업으로 여러 레코드를 관리할 수 있습니다. 새 항목을 가져오고 기존 제품 세트를 업데이트, 대체 및 삭제할 수 있습니다.

예를 들어 재고에 새 제품을 추가하고, 제품 데이터 및 고급 가격 데이터를 업데이트하고, 기존 제품 세트를 새 제품으로 바꿀 수 있습니다. 가져오기 및 내보내기 도구를 사용하면 관리자에서 여러 작업을 수행하는 대신 데이터를 내보내고 스프레드시트에서 편집한 다음 다시 스토어로 가져올 수 있으므로 대규모 제품 카탈로그를 보다 효율적으로 관리할 수 있습니다.


>[!NOTE]
>
>Adobe Commerce은 또한 SaaS 데이터 내보내기를 지원하여 제품 데이터를 Commerce 서버에서 SaaS 서비스로 전송합니다. SaaS 데이터 내보내기는 다음을 포함한 Commerce SaaS 서비스와 통합됩니다. [제품 Recommendations](https://experienceleague.adobe.com/docs/commerce-merchant-services/product-recommendations/overview.html), [라이브 검색](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/live-search/overview), 및 [카탈로그 서비스](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/catalog-service/guide-overview). 자세한 내용은 [SaaS 데이터 내보내기 안내서](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/saas-data-export/overview).

## 데이터 유효성 검사

모든 데이터는 값을 저장소로 가져오기 전에 값의 품질, 정확성 및 무결성을 보장하기 위해 유효성 검사를 통과해야 합니다. 을 클릭하면 유효성 검사가 시작됩니다. **[!UICONTROL Check Data]**. 프로세스 중에 가져오기 파일의 모든 엔티티는 다음을 확인합니다.

- **속성** - 열 헤더 이름이 시스템 데이터베이스의 해당 속성과 일치하는지 확인합니다. 각 속성의 값은 데이터 형식(decimal, integer, varchar, text 및 datetime)의 요구 사항을 충족하는지 확인하기 위해 확인됩니다.
- **복잡한 데이터** - 드롭다운 또는 다중 선택 입력 유형과 같이 정의된 집합에서 시작된 값은 정의된 집합에 값이 있는지 확인됩니다.
- **서비스 데이터** - 서비스 데이터 열의 값을 확인하여 속성 또는 복잡한 데이터 값이 시스템 데이터베이스에 이미 정의된 값과 일치하는지 확인합니다.
- **필수 값** - 새 엔티티의 경우 파일에 필요한 속성 값이 있는지 확인합니다. 기존 엔티티의 경우 필요한 속성 값이 있는지 다시 확인할 필요가 없습니다.
- **구분 기호** - 스프레드시트에서 볼 때 구분 기호가 표시되지 않지만 CSV 파일의 데이터 값은 쉼표로 구분되고 텍스트 값은 큰따옴표로 묶여 있습니다. 유효성 검사 프로세스 중에 문자 문자열을 둘러싸는 각 따옴표 세트와 구분 기호에 대한 서식이 확인됩니다.

검증 결과는 검증 결과 섹션에 나타나며 다음 정보를 포함합니다.

- 확인된 엔티티 수
- 잘못된 행 수
- 발견된 오류 수

데이터가 유효한 경우 _가져오기 성공_ 메시지가 나타납니다.

![시스템 메시지 - 파일이 유효합니다.](./assets/data-import-validation-message.png){width="500" zoomable="yes"}

유효성 검사가 실패하면 각 오류에 대한 설명을 읽고 CSV 파일에서 문제를 수정하십시오. 예를 들어 행에 유효하지 않은 SKU가 포함된 경우 가져오기 프로세스가 중지되고 해당 행과 모든 후속 행을 가져오지 않습니다. 문제가 해결되면 데이터를 다시 가져옵니다. 오류가 많이 발생하는 경우 유효성 검사를 통과하기 위해 여러 번 시도할 수 있습니다.

### 데이터 유효성 검사 메시지

#### 유효성 검사

- `Product with specified SKU not found in rows: 1`
- `URL key for specified store already exists`
- `'7z' file extension is not supported`
- `TXT file extension is not supported`

#### 오류수

- `Wrong field type. Type in the imported file %decimal%, expected type is %text%.`
- `Value is not allowed. Attribute value does not exist in the system.`
- `Field %column name% is required.Wrong value separator is used.`
- `Wrong encoding used. Supported character encoding is UTF-8 and Windows-1252.`
- `Imported file does not contain SKU field.`
- `SKU does not exist in the system.`
- `Column name %column name% is invalid. Should start with a letter. Alphanumeric.`
- `Imported file does not contain a header.`
- `%website name% website does not exist in the system.`
- `%storeview name% storeview does not exist in the system.`
- `Imported attribute %attribute name% does not exist in the system.`
- `Imported resource (image) could not be downloaded from external resource due to timeout or access permissions.`
- `Imported resource (image) does not exist in the local media storage.`
- `Product creation error displayed to the user equal to the one seen during manual product save.`
- `Advanced Price creation error displayed to the user equal to the one seen during the manual product save.`
- `Customer creation error displayed to the user equal to the one seen during the manual customer save.`
