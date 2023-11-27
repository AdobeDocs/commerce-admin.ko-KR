---
title: 고객 이름 및 주소 옵션
description: 고객 이름 및 주소 옵션은 이름 및 주소 양식에 포함되는 필드를 결정합니다.
exl-id: 28949cfc-2c96-4d0a-a35b-b37b3aa2d1e9
feature: Customers, Configuration
source-git-commit: 7de285d4cd1e25ec890f1efff9ea7bdf2f0a9144
workflow-type: tm+mt
source-wordcount: '798'
ht-degree: 0%

---

# 고객 이름 및 주소 옵션

다음 _이름 및 주소 옵션_ 고객이 다음을 만들 때 이름 및 주소 양식에 포함할 필드 확인 [account](../customers/account-create.md) 스토어와 함께.

![고객 계정 등록 양식](assets/storefront-customer-account-address-book.png){width="500" zoomable="yes"}

이름 및 주소 옵션을 구성하는 단계는 Adobe Commerce 및 Magento Open Source에 따라 다릅니다.

## Adobe Commerce에 대한 이름 및 주소 옵션 구성

고객이 계정을 만들 때 상점 첫 화면에서 표시되는 이름과 주소 옵션을 구성할 수 있습니다.

### 1단계: 구성 범위 설정

1. 다음에서 _관리자_ 사이드바, 이동 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. 왼쪽 패널에서 를 확장합니다. **[!UICONTROL Customers]** 및 선택 **[!UICONTROL Customer Configuration]**.

1. 확장 **[!UICONTROL Name and Address Options]** 섹션.

   >[!INFO]
   >
   >이름 및 주소 옵션의 범위는 `website` 레벨.

1. 페이지 맨 위로 스크롤하고 구성 범위를 다음 중 하나로 설정합니다.

   - `Default Config`
   - `Main Website` (또는 다중 사이트 설치를 위한 특정 사이트)

   >[!INFO]
   >
   >다음 _[!UICONTROL Name and Address Options]_범위를 로 설정하면 섹션이 표시되지 않습니다. `Default Store View`.

   ![구성 범위](assets/customer-configuration-scope-ee.png){width="700" zoomable="yes"}

### 2단계: 이름 및 주소 옵션 구성

1. (으)로 돌아가기 [!UICONTROL _이름 및 주소 옵션_] 고객 구성 페이지의 섹션에 자세히 설명되어 있습니다.

   >[!INFO]
   >
   > 를 사용하지 않는 경우 `Default config` 범위 설정이므로 `Use Default` 값을 변경하기 전에 각 필드에 대한 확인란입니다.

   ![이름 및 주소 옵션](../configuration-reference/customers/assets/customer-configuration-name-address-options-ee.png){width="600" zoomable="yes"}

1. 대상 **[!UICONTROL Prefix Dropdown Options]**&#x200B;목록에 표시할 각 접두사를 세미콜론으로 구분하여 입력합니다.

   >[!IMPORTANT]
   >
   >목록의 맨 위에 빈 값을 표시하려면 첫 번째 값 앞에 세미콜론을 넣습니다.

1. 대상 **[!UICONTROL Suffix Dropdown Options]**&#x200B;목록에 표시할 각 접미사를 세미콜론으로 구분하여 입력합니다.

1. 고객 양식에 다음 필드를 포함하려면 각각의 값을 로 설정합니다. `Optional` 또는 `Required`, 필요한 경우.

   - **[!UICONTROL Show Telephone]**
   - **[!UICONTROL Show Company]**
   - **[!UICONTROL Show Fax]**

### 3단계: 저장 및 새로 고침

1. 완료되면 다음을 클릭하십시오. **[!UICONTROL Save Config]**.

1. 페이지 맨 위에 있는 메시지에서 **[!UICONTROL Cache Management]** 및 [새로 고침](../systems/cache-management.md) 각 잘못된 캐시.

## Magento Open Source에 대한 이름 및 주소 옵션 구성

고객이 계정을 만들 때 상점 첫 화면에서 표시되는 이름과 주소 옵션을 구성합니다.

![고객 계정 등록 양식](assets/storefront-customer-account-signup.png){width="500" zoomable="yes"}

### 1단계: 구성 범위 설정

1. 다음에서 _관리자_ 사이드바, 이동 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. 왼쪽 패널에서 를 확장합니다. **[!UICONTROL Customers]** 및 선택 **[!UICONTROL Customer Configuration]**.

1. 확장 **[!UICONTROL Name and Address Options]** 섹션.

   >[!IMPORTANT]
   >
   > 이름 및 주소 옵션의 범위는 `website` 레벨.

   ![이름 및 주소 옵션](../configuration-reference/customers/assets/customer-configuration-name-address-options-ce.png){width="600" zoomable="yes"}

1. 페이지 맨 위로 스크롤하여 구성 범위를 다음 중 하나로 설정합니다.

   - `Default Config`
   - `Main Website` (또는 다중 사이트 설치를 위한 특정 사이트)

   >[!NOTE]
   >
   >다음 _이름 및 주소 옵션_ 범위를 로 설정하면 섹션이 표시되지 않습니다. `Default Store View`.

   ![구성 범위](assets/configuration-scope.png){width="600" zoomable="yes"}

### 2단계: 이름 및 주소 옵션 구성

1. (으)로 돌아가기 [!UICONTROL _이름 및 주소 옵션_] 고객 구성 페이지의 섹션에 자세히 설명되어 있습니다.

   >[!INFO]
   >
   >를 사용하지 않는 경우 `Default config` 범위 설정이므로 `Use Default` 값을 변경하기 전에 각 필드에 대한 확인란입니다.

1. 대상 **상세 주소의 줄 수**, 1에서 4 사이의 숫자를 입력합니다.

   >[!WARNING]
   >
   >기본적으로 상세 주소는 세 줄입니다.

1. 접두사(예: Mr 또는 Ms)를 이름의 일부로 포함하려면 다음을 설정합니다 **접두사 표시** 끝 `Yes`.

   ![고객 등록 양식 접두사](assets/storefront-customer-account-prefix.png){width="600" zoomable="yes"}

   >[!INFO]
   >
   >대상 **접두사 드롭다운 옵션**&#x200B;목록에 표시할 각 접두사를 세미콜론으로 구분하여 입력합니다. 첫 번째 값 앞에 세미콜론을 배치하여 목록의 맨 위에 빈 값을 표시할 수 있습니다.

1. 고객의 중간 이름 또는 이니셜에 대한 선택적 필드를 포함하려면 다음을 설정하십시오. **[!UICONTROL Show Middle Name (initial)]** 끝 `Yes`.

1. 접미사(예: Jr.) 포함 또는 Sr.) 고객 이름 뒤에 를 설정합니다. **[!UICONTROL Show Suffix]** 다음 중 하나를 수행합니다.

   - `Optional`
   - `Required`

   >[!INFO]
   >
   >대상 **접미사 드롭다운 옵션**&#x200B;목록에 표시할 각 접미사를 세미콜론으로 구분하여 입력합니다. 첫 번째 값 앞에 세미콜론을 배치하여 목록의 맨 위에 빈 값을 표시할 수 있습니다.

1. 생년월일을 포함하려면 다음을 설정하십시오. **[!UICONTROL Show Date of Birth]** 다음 중 하나를 수행합니다.

   - `Optional`
   - `Required`

   >[!INFO]
   >
   >현재 보안 및 개인 정보 보호 모범 사례를 준수하면서 다른 개인 식별자를 사용한 고객의 전체 생년월일(월, 일, 년) 저장과 관련된 잠재적 법적 및 보안 위험에 대해 알아두어야 합니다. 고객의 전체 생년월일 보관을 제한하고 고객 생년월일을 대안으로 사용하는 것이 좋습니다.

   고객은 필드 뒤에 있는 캘린더 아이콘을 사용하여 팝업 달력에서 생년월일을 선택할 수 있습니다.

   ![고객 등록 양식의 생년월일](assets/storefront-customer-account-date-of-birth.png){width="600" zoomable="yes"}

1. 고객이 세금을 입력할 수 있도록 허용 [VAT](../stores-purchase/vat.md) 숫자, 설정 **[!UICONTROL Show Tax/VAT Number]** 다음 중 하나를 수행합니다.

   - `Optional`
   - `Required`

1. 고객 양식에 성별 필드를 포함하려면 다음을 설정하십시오. **[!UICONTROL Show Gender]** 다음 중 하나를 수행합니다.

   - `Optional`
   - `Required`

   ![고객 등록 양식의 성별 옵션](assets/storefront-customer-account-gender.png){width="600" zoomable="yes"}

1. 고객 양식에 다음 필드를 포함하려면 각각의 값을 로 설정합니다. `Optional` 또는 `Required`, 필요한 경우.

   - **[!UICONTROL Show Telephone]**
   - **[!UICONTROL Show Company]**
   - **[!UICONTROL Show Fax]**

### 3단계: 저장 및 새로 고침

1. 완료되면 다음을 클릭하십시오. **[!UICONTROL Save Config]**.

1. 페이지 맨 위에 있는 메시지에서 **[!UICONTROL Cache Management]** 및 [새로 고침](../systems/cache-management.md) 각 잘못된 캐시.
