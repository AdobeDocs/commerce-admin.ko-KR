---
title: 세부 정보 저장
description: 스토어에 대한 기본 정보를 업데이트하는 방법을 알아봅니다.
exl-id: f4910ff7-4fcc-482f-be1d-cad8564cdd86
feature: Configuration
source-git-commit: 3ff5807fd0a3ebf2e9d4f9c085852dd7777a1103
workflow-type: tm+mt
source-wordcount: '1797'
ht-degree: 0%

---

# 세부 정보 저장

매장의 기본 정보에는 매장 이름과 주소, 전화 번호 및 이메일 주소가 포함되어 있으며 이메일 메시지, 인보이스 및 고객에게 보낸 기타 통신에 표시됩니다.

![일반 구성 - 세부 정보 저장](./assets/config-general-store-details.png){width="900" zoomable="yes"}

## [!UICONTROL Store Information]

다음 _[!UICONTROL Store Information]_섹션에는 판매 문서 및 기타 통신에 표시되는 기본 정보가 나와 있습니다.

1. 다음에서 _관리자_ 사이드바, 이동 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. 아래 **[!UICONTROL General]** 왼쪽 탐색 패널에서 을 선택합니다 **[!UICONTROL General]**.

1. 확장 ![확장 선택기](../assets/icon-display-expand.png) 다음 **[!UICONTROL Store Information]** 섹션.

   ![일반 구성 - 정보 저장](./assets/general-store-information.png){width="700"}

1. 스토어 세부 정보에 따라 옵션을 설정합니다.

   - 다음을 입력합니다. **[!UICONTROL Store Name]** 모든 통신에서 사용할 수 있습니다.

   - 다음을 입력합니다. **[!UICONTROL Store Phone Number]**&#x200B;를 클릭하고, 원하는 대로 형식을 지정합니다.

   - 대상 **[!UICONTROL Store Hours of Operation]**&#x200B;에 스토어가 비즈니스를 위해 열려 있는 시간을 입력합니다. For example: `Mon - Fri, 9-5, Sat 9-noon PST`.

   - 다음 항목 선택 **[!UICONTROL Country]** 비즈니스 위치.

   - 다음 항목 선택 **[!UICONTROL Region/State]** 나라와 함께요

   - 다음을 입력합니다. **[!UICONTROL Store Address]**. 주소가 긴 경우 다음 주소에서 계속 진행하십시오. **저장소 주소란 2**.

   - 해당하는 경우 다음을 입력합니다. **[!UICONTROL VAT Number]** 스토어에서 가져왔습니다.

     번호를 확인하려면 **[!UICONTROL Validate VAT Number]** 단추를 클릭합니다. 자세한 내용은 다음을 참조하십시오. [VAT ID 유효성 검사](../stores-purchase/vat.md#vat-id-validation).

1. 완료되면 다음을 클릭하십시오. **[!UICONTROL Save Config]**.

정보 저장 구성 옵션에 대한 자세한 내용은 [_구성 참조 안내서_](../configuration-reference/general/general.md#store-information).

## [!UICONTROL Locale Options]

로케일은 저장소 전체에서 사용되는 여러 설정을 결정합니다. 그 중 일부는 다음과 같습니다.

- 언어
- 국가
- 세율
- 통화
- 가격
- 숫자 형식

로케일 설정은 각 스토어에 사용되는 시간대와 언어를 결정하고 해당 영역의 작업 요일 을 식별합니다.

1. 다음에서 _관리자_ 사이드바, 이동 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. 아래의 왼쪽 탐색 패널에서 **[!UICONTROL General]**, 선택 **[!UICONTROL General]**.

1. 확장 ![확장 선택기](../assets/icon-display-expand.png) 다음 **[!UICONTROL Locale Options]** 섹션.

   ![일반 구성 - 로케일 옵션](./assets/general-locale-options.png){width="700"}

1. 다음 항목 선택 **[!UICONTROL Timezone]** 목록에서 삭제할 수 있습니다.

1. 설정 **[!UICONTROL Locale]** 스토어 언어로.

1. 설정 **[!UICONTROL Weight Unit]** 로케일에서 발송하는 데 일반적으로 사용되는 측정 단위입니다.

1. 설정 **[!UICONTROL First Day of the Week]** 를 지역 내 첫 번째 요일로 간주되는 날짜로 변경합니다.

1. 다음에서 **[!UICONTROL Weekend Days]** 영역에 있는 주말에 해당하는 날짜를 나열합니다.

   여러 날을 선택하려면 Ctrl 키(PC) 또는 Command 키(Mac)를 누른 채 각 항목을 클릭합니다.

1. 완료되면 다음을 클릭하십시오. **[!UICONTROL Save Config]**.

로케일 구성 옵션에 대한 자세한 내용은 [구성 참조 안내서](../configuration-reference/general/general.md#locale-options).

## [!UICONTROL State Options]

많은 국가에서 주, 시/도 또는 지역은 우편 주소의 필수 부분입니다. 이 정보는 배송 및 청구 정보, 세율 계산 등에 사용됩니다. 주가 필요하지 않은 국가의 경우, 필드에서 완전히 주소에서 생략하거나 선택 필드로 포함할 수 있습니다.

표준 주소 포맷은 국가마다 다르기 때문에 송장, 포장 명세서 및 운송 라벨에 대한 주소 포맷을 지정하는 데 사용되는 템플리트를 편집할 수도 있습니다.

1. 다음에서 _관리자_ 사이드바, 이동 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. 아래 **[!UICONTROL General]** 왼쪽 탐색 패널에서 을 선택합니다 **[!UICONTROL General]**.

1. 확장 ![확장 선택기](../assets/icon-display-expand.png) 다음 **[!UICONTROL State Options]** 섹션.

   ![일반 구성 - 상태 옵션](./assets/general-state-options.png){width="700"}

1. 사용 **[!UICONTROL State is required for]** 지역/주가 필수 항목인 각 국가를 선택하는 목록입니다.

1. 설정 **[!UICONTROL Allow to Choose State if it is Optional for Country]** 다음 중 하나를 수행합니다.

   `Yes` - 상태 필드가 필수가 아닌 국가에서는 상태 필드를 선택적 항목으로 포함합니다.

   `No` - 상태 필드가 필요하지 않은 국가에서는 상태 필드를 생략합니다.

1. 완료되면 다음을 클릭하십시오. **[!UICONTROL Save Config]**.

상태 구성 옵션에 대한 자세한 내용은 [구성 참조 안내서](../configuration-reference/general/general.md#state-options).

## [!UICONTROL Country Options]

국가 옵션은 비즈니스가 위치한 국가와 지불을 수락하는 국가를 식별합니다.

### 스토어의 국가 옵션을 설정합니다.

1. 다음에서 _관리자_ 사이드바, 이동 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. 아래의 왼쪽 탐색 패널에서 **[!UICONTROL General]**, 선택 **[!UICONTROL General]**.

1. 확장 ![확장 선택기](../assets/icon-display-expand.png) 다음 **[!UICONTROL Country Options]** 섹션.

   >[!NOTE]
   >
   >필요한 경우 **[!UICONTROL Use system value]** 변경할 각 설정에 대한 확인란입니다.

   ![일반 구성 - 국가 설정](./assets/general-country-options.png){width="700"}

1. 다음을 선택합니다. **[!UICONTROL Default Country]** 비즈니스 위치.

1. 다음에서 **[!UICONTROL Allow Countries]** 목록에서 주문을 수락할 각 국가를 선택합니다.

   기본적으로 목록에 있는 모든 국가가 선택됩니다. 여러 국가를 선택하려면 Ctrl 키(PC) 또는 Command 키(Mac)를 누른 채 각 항목을 클릭합니다.

1. 사용 **[!UICONTROL Zip/Postal Code is Optional for]** 우편 번호를 거리 주소의 일부로 포함할 필요가 없는 비즈니스를 수행하는 각 국가를 선택하는 목록입니다.

1. 다음에서 **[!UICONTROL European Union Countries]** 목록에서 비즈니스를 수행하는 EU의 각 국가를 선택합니다.

   기본적으로 모든 EU 국가가 선택됩니다. 필요한 국가를 선택하려면 Ctrl 키(PC) 또는 Command 키(Mac)를 누른 채 각 항목을 클릭합니다.

1. 다음에서 **[!UICONTROL Top Destinations]** 목록에서 판매에 대해 타겟팅하는 기본 국가를 선택합니다.

1. 완료되면 다음을 클릭하십시오. **[!UICONTROL Save Config]**.

### 특정 게재 방법에 대한 국가 옵션 설정

사용 가능한 각 국가에 대해 특정 국가로의 배송을 구성할 수도 있습니다 [게재 방법](../stores-purchase/delivery.md) (UPS, FedEx 등)

1. 다음에서 _관리자_ 사이드바, 이동 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. 왼쪽 탐색 패널에서 를 확장합니다. **[!UICONTROL Sales]** 및 선택 **[!UICONTROL Delivery Methods]**.

1. 특정 국가를 적용할 운송 회사를 선택합니다.

1. 대상 **[!UICONTROL Ship to Applicable Countries]**, 선택 해제 **[!UICONTROL Use system value]** 확인란을 선택하고 **[!UICONTROL Specific Countries]** 옵션을 선택합니다.

1. 다음에서 **[!UICONTROL Top Destinations]** 목록에서 운송을 대상으로 하는 기본 국가를 선택합니다.

   ![DHL 게재 방법의 국가 옵션 설정 예](./assets/country-options-for-specific-delivery-method.png){width="700"}

1. 완료되면 다음을 클릭하십시오. **[!UICONTROL Save Config]**.

### 리소스 문제 해결

국가 구성 문제 해결에 대한 도움말을 보려면 다음을 참조하십시오 [!DNL Commerce] 지원 기술 자료 문서:

- [국가를 추가하는 방법](https://experienceleague.adobe.com/docs/commerce-knowledge-base/kb/how-to/how-to-add-a-new-country-to-magento-2.html)
- [입력한 countryId가 존재하지 않습니다.](https://experienceleague.adobe.com/docs/commerce-knowledge-base/kb/support-tools/patches/v1-0-15/mdva-33393-magento-patch-provided-countryid-does-not-exist.html)

## [!UICONTROL Merchant Location]

판매자 위치 설정은 를 구성하는 데 사용됩니다. [결제 방법](../stores-purchase/payments.md). 이 설정에 대한 값이 없으면 [기본 국가](#uicontrol-country-options) 설정이 사용됩니다.

1. 다음에서 _관리자_ 사이드바, 이동 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. 왼쪽 탐색 패널에서 를 확장합니다. **[!UICONTROL Sales]** 및 선택 **[!UICONTROL Payment Methods]**.

1. 확장 ![확장 선택기](../assets/icon-display-expand.png) 다음 **판매자 위치** 섹션 및 선택 **[!UICONTROL Merchant Country]**.

   ![판매자 위치 설정](./assets/payment-methods-merchant-location.png){width="600"}

1. 완료되면 다음을 클릭하십시오. **[!UICONTROL Save Config]**.

결제 방법 구성 옵션에 대한 자세한 내용은 [구성 참조 안내서](../configuration-reference/sales/payment-methods.md).

## 통화

통화 설정 - 기준 정의 [통화](../stores-purchase/currency-configuration.md) 및 지불로 허용되는 모든 추가 통화. 또한 통화 환율을 자동으로 업데이트하는 데 사용되는 가져오기 연결 및 일정을 설정합니다.

통화 기호 - 다음을 정의합니다. [통화 기호](../stores-purchase/currency-configuration.md#step-5-customize-currency-symbols-optional) 제품 가격 및 주문 및 송장 등의 판매 문서에 나타납니다. [!DNL Commerce] 는 전 세계 200여 개국의 통화를 지원합니다.

환율 갱신 - 환율은 다음과 같을 수 있습니다. [업데이트됨](../stores-purchase/currency-update.md) 필요에 따라 또는 사전 정의된 일정에 따라 스토어에 수동으로 또는 가져옵니다.

통화 선택기 - 여러 통화를 사용할 수 있는 경우 [통화 선택기](../stores-purchase/currency.md) 은 저장소의 헤더에서 사용할 수 있습니다.

## [!UICONTROL Store Email Addresses]

각 스토어 또는 보기에 대해 서로 다른 기능 또는 부서를 나타내는 최대 5개의 서로 다른 이메일 주소를 가질 수 있습니다. 사전 정의된 다음의 이메일 ID 외에도 필요에 따라 설정할 수 있는 몇 가지 사용자 정의 ID가 있습니다.

- 일반 연락처
- 영업 담당자
- 고객 지원

각 ID 및 관련 이메일 주소는 특정 자동 이메일 메시지와 연결될 수 있으며 스토어에서 보낸 이메일 메시지의 발신자로 표시됩니다.

### 1단계: 도메인에 대한 이메일 주소 설정

스토어에 대한 이메일 주소를 구성하려면 먼저 각 주소를 도메인에 대한 유효한 이메일 주소로 설정해야 합니다. 필요한 각 이메일 주소를 만들려면 서버 관리자 또는 이메일 호스팅 공급자의 지침을 따르십시오.

### 2단계: 스토어의 이메일 주소 구성

1. 다음에서 _관리자_ 사이드바, 이동 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. 아래 **[!UICONTROL General]** 왼쪽 탐색 패널에서 을 선택합니다 **[!UICONTROL Store Email Addresses]**.

1. 확장 ![확장 선택기](../assets/icon-display-expand.png) 다음 **[!UICONTROL General Contact]** 섹션을 참조하고 다음을 수행합니다.

   ![일반 구성 - 이메일 주소 저장](./assets/store-email-addresses-general-contact.png){width="600"}

   - 대상 **[!UICONTROL Sender Name]**&#x200B;이메일 메시지를 보낸 사람으로 나타나도록 일반 연락처 ID와 연결된 사람의 이름을 입력합니다.

   - 대상 **[!UICONTROL Sender Email]**&#x200B;연결된 이메일 주소를 입력합니다.

1. 사용할 각 저장소 이메일 주소에 대해 이 프로세스를 반복합니다.

1. 완료되면 다음을 클릭하십시오. **[!UICONTROL Save Config]**.

### 3단계: 판매 이메일 구성 업데이트

사용자 정의 이메일 주소를 사용하는 경우 올바른 ID가 발신자로 표시되도록 관련 이메일 메시지의 구성을 업데이트해야 합니다.

1. 왼쪽 탐색 패널에서 를 확장합니다. **[!UICONTROL Sales]** 및 선택 **[!UICONTROL Sales Emails]**.

   페이지에는 다음 각 항목에 대한 별도의 섹션이 있습니다.

   - 주문 및 주문 주석
   - 송장 및 송장 주석
   - 선적 및 선적 주석
   - 대변 메모 및 대변 메모 주석
   - RMA, RMA 인증, RMA 관리자 주석 및 RMA 고객 주석 ![Adobe Commerce](../assets/adobe-logo.svg) (Adobe Commerce 전용)

1. 시작 **[!UICONTROL Order]**&#x200B;를 클릭하고, 각 메시지에 대한 섹션을 확장한 다음 올바른 발신자가 선택되어 있는지 확인합니다.

   ![영업 구성 - 영업 이메일](./assets/sales-emails-order.png){width="600"}

1. 완료되면 다음을 클릭하십시오. **[!UICONTROL Save Config]**.

Sales Email 구성 옵션에 대한 자세한 내용은 [_구성 참조 안내서_](../configuration-reference/sales/sales-emails.md).

## 연락처 양식

다음 _연락처_ 매장 바닥글에 있는 링크를 통해 고객이 손쉽게 연락할 수 있습니다. 고객은 양식을 작성하여 스토어에 메시지를 보낼 수 있습니다. 표준 [!DNL Commerce] 설치 시 기본값이 표시됨 _연락처_ 양식. 양식을 제출하면 감사 메시지가 나타납니다

기본 Contact Us 양식이 CMS 페이지가 아닌 코드에서 직접 렌더링됨을 이해하는 것이 중요합니다.

![기본 연락처 페이지](./assets/page-contact-us-default.png){width="700"}

스토어 바닥글에는 스토어 전체에서 사용할 수 있는 연락처 페이지에 대한 링크가 포함되어 있습니다.

![바닥글의 연락처 링크](./assets/storefront-footer-contact-us.png){width="700"}

Luma 샘플 데이터에는 스토어에 대해 페이지를 사용자 지정하는 방법을 보여 주는 연락처 페이지에 대한 추가 정보가 포함되어 있습니다.

![연락처 페이지](./assets/storefront-contact-us.png){width="700"}

### 연락처 양식 구성

1. 다음에서 _관리자_ 사이드바, 이동 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. 아래의 왼쪽 탐색 패널에서 **[!UICONTROL General]**, 선택 **[!UICONTROL Contacts]**.

1. 확장 ![확장 선택기](../assets/icon-display-expand.png) 다음 **[!UICONTROL Contact Us]** 섹션 및 세트 **[!UICONTROL Enable Contact Us]** 끝 `Yes`.

   ![일반 구성 - 문의하기](./assets/contacts-contact-us.png){width="600"}

1. 확장 ![확장 선택기](../assets/icon-display-expand.png) 다음 **[!UICONTROL Email Options]** 섹션을 만들고 이메일 연락처 옵션을 설정합니다.

   ![일반 구성 - 이메일 옵션](./assets/contacts-email-options.png){width="600"}

   - 대상 **[!UICONTROL Send Emails to]**&#x200B;연락처 양식의 메시지를 보낼 이메일 주소를 입력합니다.

   - 설정 **[!UICONTROL Email Sender]** 연락처 양식에서 메시지를 보낸 사람으로 표시되는 스토어 ID에 대한 메시지입니다. 예: 사용자 정의 이메일 2.

   - 설정 **[!UICONTROL Email Template]** 연락처 양식에서 보낸 메시지에 사용하는 템플릿으로 보냅니다.

1. 경쟁할 때는 다음을 클릭하십시오. **[!UICONTROL Save Config]**.

### 콘텐츠 사용자 정의

다음에서 콘텐츠를 사용자 지정할 수 있습니다. _연락처_ 상점과 고객 서비스 정책의 요구 사항에 맞는 양식.

### 방법 1: 샘플 데이터 사용

Luma 샘플 데이터에는 _연락처 정보_ 스토어에 맞게 사용자 지정할 수 있는 블록입니다. 다음 `contact-us-info` [차단](../content-design/blocks.md) 연락처 페이지에 나만의 콘텐츠를 추가하도록 쉽게 수정할 수 있습니다.

1. 다음에서 _관리자_ 사이드바, 이동 **[!UICONTROL Content]** > _[!UICONTROL Elements]_>**[!UICONTROL Blocks]**.

1. 다음 찾기 **[!UICONTROL Contact Us Info]** 목록에서 차단한 다음 여는 위치 **[!UICONTROL Edit]** 모드.

   ![연락처 정보 차단](./assets/content-block-contact-us-info.png){width="700"}

1. 블록 페이지 하단에서 **[!UICONTROL Edit with Page Builder]**.

   ![콘텐츠 블록 - 문의하기 사례](./assets/content-block-contact-us-content.png){width="700"}

   >[!NOTE]
   >
   >다음을 보유한 경우: [[!DNL Page Builder] 비활성화됨](../page-builder/setup.md#disable-dnl-page-builder), 편집기를 사용할 수 있습니다 [도구 모음](../content-design/editor.md) 텍스트 서식 지정 및 추가 [이미지](../content-design/editor-insert-image.md) 및 [링크](../content-design/editor-insert-link.md).

1. HTML 컨테이너 위로 마우스를 가져가 도구 상자를 표시하고 _설정_ ( ![설정 아이콘](../page-builder/assets/pb-icon-settings.png) ) 아이콘.

1. 스토어 연락처 정보 제공에 따라 HTML 코드를 편집하고 **[!UICONTROL Save]**.

   ![콘텐츠 블록 - HTML 코드 편집](./assets/content-block-contact-us-html.png){width="700"}

1. 종료 [!DNL Page Builder] 스테이징 및 클릭 **[!UICONTROL Save Block]**.

### 방법 2: 샘플 데이터 없음

>[!IMPORTANT]
>
>2.4.0 릴리스부터 연락처 양식은 더 이상 CMS 블록 또는 CMS 페이지 내에서 를 호출할 수 없습니다. 연락처 양식의 모든 사용자 지정은 레이아웃 xml 또는 사용자 지정 테마 템플릿을 사용하여 수행해야 합니다.

기본적으로 쇼핑객은 _연락처 링크_ 상점 첫 페이지의 바닥글. 연락처 페이지 사용자 지정에 대한 자세한 내용은 [프론트엔드 개발자 안내서][theme-guide].

[theme-guide]: https://developer.adobe.com/commerce/frontend-core/guide/themes/
