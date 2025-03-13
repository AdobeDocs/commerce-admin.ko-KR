---
title: '[!UICONTROL General] &gt; [!UICONTROL General]'
description: Commerce 관리자의 [!UICONTROL General] &gt; [!UICONTROL General] 페이지에서 구성 설정을 검토하십시오.
exl-id: 67760d24-ad12-4c49-9649-0607c57f5cf0
feature: Configuration, System
source-git-commit: 5da244a548b15863fe31b5df8b509f8e63df27c2
workflow-type: tm+mt
source-wordcount: '999'
ht-degree: 0%

---

# [!UICONTROL General] > [!UICONTROL General]

{{config}}

## [!UICONTROL Country Options]

이러한 구성 필드 및 옵션에 대한 자세한 내용은 [국가 옵션](../../getting-started/store-details.md#country-options)을 참조하세요.

![일반 > 국가 옵션](./assets/general-country-options.png)<!-- zoom -->

| 필드 | [범위](../../getting-started/websites-stores-views.md#scope-settings) | 설명 |
|--- |--- |--- |
| [!UICONTROL Default Country] | 스토어 뷰 | 스토어가 있는 국가입니다. |
| [!UICONTROL Allow Countries] | 웹 사이트 | 주문을 받는 국가입니다. |
| [!UICONTROL Zip/Postal Code is Optional for] | 글로벌 | 배송 주소에 우편 번호가 필요하지 않은 국가. |
| [!UICONTROL European Union Countries] | 글로벌 | 유럽 연합 회원국. |
| [!UICONTROL Top Destinations] | 스토어 뷰 | 판매를 목표로 하는 기본 국가. |

{style="table-layout:auto"}

## [!UICONTROL State Options]

이러한 구성 필드 및 옵션에 대한 자세한 내용은 [상태 옵션](../../getting-started/store-details.md#state-options)을 참조하세요.

![일반 > 상태 옵션](./assets/general-state-options.png)<!-- zoom -->

| 필드 | [범위](../../getting-started/websites-stores-views.md#scope-settings) | 설명 |
|--- |--- |--- |
| [!UICONTROL State is required for] | 글로벌 | 우편 주소에 지역 또는 주를 포함해야 하는 국가(사업을 수행하는 경우). |
| [!UICONTROL Allow to Choose State if It is Optional for Country] | 글로벌 | 필요하지 않은 국가의 경우 _지역/주_ 필드가 고객의 우편 주소에 포함되어 있는지 확인합니다.<br /> <br />**`Yes`**- 국가가 필요하지 않더라도 고객 주소에 _지역/주_ 필드를 포함합니다.<br />**`No`** - 국가에서 필요하지 않은 경우 고객 주소에서 지역/주 필드를 생략합니다. |

{style="table-layout:auto"}

## [!UICONTROL Locale Options]

이러한 구성 필드 및 옵션에 대한 자세한 내용은 [로케일 옵션](../../getting-started/store-details.md#locale-options)을 참조하십시오.

![일반 > 로케일 옵션](./assets/general-locale-options.png)<!-- zoom -->

| 필드 | [범위](../../getting-started/websites-stores-views.md#scope-settings) | 설명 |
|--- |--- |--- |
| [!UICONTROL Timezone] | 웹 사이트 | 웹 사이트에서 제공하는 기본 마켓의 시간대. 일반적으로 시간대는 비즈니스의 실제 위치에 사용되는 시간대와 동일합니다. |
| [!UICONTROL Locale] | 스토어 뷰 | 스토어 보기에서 제공하는 마켓에서 사용되는 언어, 통화 및 측정 시스템. |
| [!UICONTROL Weight Unit] | 스토어 뷰 | 일반적으로 로케일에서 발송하는 데 사용되는 측정 단위. 옵션: `lbs` / `kgs` |
| [!UICONTROL First Day of Week] | 스토어 뷰 | 스토어 보기에서 제공하는 시장에서 첫 번째 요일로 간주되는 날짜입니다. |
| [!UICONTROL Weekend Days] | 스토어 뷰 | 주말에 마켓에 있는 요일 중 스토어 보기에서 제공하는 요일입니다. |

{style="table-layout:auto"}

## [!UICONTROL Website Restrictions]

{{ee-feature}}

![일반 > 웹 사이트 제한](./assets/general-website-restrictions.png)<!-- zoom -->

이러한 설정 변경에 대한 자세한 내용은 _머천다이징 및 프로모션 안내서_&#x200B;의 [액세스 제한](../../merchandising-promotions/event-configure.md#access-restrictions)을 참조하십시오.

| 필드 | [범위](../../getting-started/websites-stores-views.md#scope-settings) | 설명 |
|--- |--- |--- |
| [!UICONTROL Access Restriction] | 웹 사이트 | 웹 사이트가 제한된 모드에서 작동하는지 확인합니다.<br /> <br />**`Yes`**- 아래 필드에 설정된 방식으로 웹 사이트 액세스가 제한됩니다.<br />**`No`** - 제한이 비활성화되며 다음 설정은 영향을 주지 않습니다. |
| [!UICONTROL Restriction Mode] | 웹 사이트 | 웹 사이트에 적용되는 액세스 제한 유형을 결정합니다.<br /> <br />**`Website Closed`**- storefront에 대한 모든 액세스가 제한되고 상점 URL이 일시적으로 랜딩 페이지로 리디렉션됩니다. 이 설정은 사이트 유지 관리 중 또는 시작 전에 유용할 수 있습니다.<br />**`Private Sales: Login Only`** - 등록된 고객만 로그인하여 상점에 액세스할 수 있습니다. 모든 storefront URL은 지정된 랜딩 페이지나 로그인 양식으로 일시적으로 리디렉션됩니다. 사용자는 이 모드에서 계정을 만들 수 없습니다.<br />**`Private Sales: Login and Register`**- 사용자가 상점 앞에 액세스하려면 로그인해야 합니다. 사용자가 로그인할 때까지 모든 상점 URL이 일시적으로 로그인 양식으로 리디렉션됩니다. 사이트가 이 모드에 있는 동안 사용자는 계정에 등록할 수 있습니다. |
| [!UICONTROL Startup Page] | 스토어 뷰 | 웹 사이트가 비공개 판매 모드에 있는 경우 이 설정은 고객이 로그인할 때까지 표시되는 페이지를 결정합니다.<br />  <br />**`To login form`**- 사용자가 로그인할 때까지 로그인 양식으로 리디렉션됩니다.<br />**`To landing page`** - 사용자가 로그인할 때까지 아래에 지정된 정적 페이지로 리디렉션됩니다.<br /> <br />**_중요!_**고객이 로그인하여 전체 사이트에 액세스할 수 있도록 지정한 랜딩 페이지의 로그인 페이지에 대한 링크를 포함해야 합니다. |
| [!UICONTROL Landing Page] | 스토어 뷰 | 웹 사이트가 비공개 판매 모드에 있을 때 나타나는 첫 번째 페이지를 결정합니다. |
| [!UICONTROL HTTP Response] | 웹 사이트 | 웹 사이트가 닫히고 보트, 크롤러 또는 스파이더가 연결을 시도할 때 전송되는 HTTP 응답을 결정합니다.<br /> <br />**`503 Service unavailable`**- 페이지를 사용할 수 없지만 스파이더가 인덱스를 업데이트해서는 안 됩니다.<br />**`200 OK`** - 랜딩 페이지가 올바르며 사이트의 유일한 페이지로 스파이더가 처리해야 합니다. |
| [!UICONTROL Enable Autocomplete on login/forgot password forms] | 웹 사이트 | _로그인_ 및 _암호 찾기_ 양식의 필드를 이전 항목에서 자동으로 채울지 여부를 결정합니다. 옵션: `Yes` / `No` |

{style="table-layout:auto"}

## [!UICONTROL Store Information]

![일반 > 정보 저장](./assets/general-store-information.png)<!-- zoom -->

이러한 설정 변경에 대한 자세한 내용은 _시작 안내서_&#x200B;에서 [정보 저장](../../getting-started/store-details.md)을 참조하세요.

| 필드 | [범위](../../getting-started/websites-stores-views.md#scope-settings) | 설명 |
|--- |--- |--- |
| [!UICONTROL Store Name] | 스토어 뷰 | 스토어 보기와 연관된 스토어의 이름입니다. |
| [!UICONTROL Store Phone Number] | 스토어 뷰 | (스토어 보기와 연관된) 스토어의 기본 전화 번호가 비즈니스를 위해 열려 있습니다. 예: 월 - 금, 9-5, 토 9-정오 PST |
| 국가 | 웹 사이트 | 웹 사이트를 운영하는 비즈니스의 국가입니다. |
| [!UICONTROL Region/State] | 웹 사이트 | 웹 사이트를 운영하는 비즈니스의 지역 또는 상태입니다. |
| [!UICONTROL ZIP/Postal Code] | 웹 사이트 | 웹 사이트를 운영하는 비즈니스의 우편 번호입니다. |
| [!UICONTROL City] | 웹 사이트 | 웹 사이트를 운영하는 비즈니스의 도시 위치입니다. |
| [!UICONTROL Street Address] | 웹 사이트 | 웹 사이트를 운영하는 회사의 거리 또는 우편 주소. |
| [!UICONTROL Street Address Line 2|]웹 사이트 | 필요한 경우 근무처 번지의 두 번째 줄입니다. |
| [!UICONTROL VAT Number] | 웹 사이트 | Commerce 설치를 소유하는 비즈니스의 부가가치세 번호(해당하는 경우). |
| [!UICONTROL Validate VAT Number] |  | 부가가치세 식별 번호를 확인합니다. |

{style="table-layout:auto"}

## [!UICONTROL Single-Store Mode]

![일반 > 단일 스토어 모드](./assets/general-single-store-mode.png)<!-- zoom -->

이러한 설정 변경에 대한 자세한 내용은 _시작 안내서_&#x200B;에서 [단일 저장소 모드](../../getting-started/websites-stores-views.md#single-store-mode)를 참조하십시오.

| 필드 | [범위](../../getting-started/websites-stores-views.md#scope-settings) | 설명 |
|--- |--- |--- |
| [!UICONTROL Enable Single-Store Mode] | 글로벌 | 단일 저장소 설치를 사용하도록 설정한 경우 구성 범위 상자 및 관련 필드 레이블을 숨깁니다. 옵션: `Yes` / `No` <br/>**_참고:_**보기가 둘 이상인 저장소의 경우 단일 저장소 모드가 무시됩니다.<br/> 단일 스토어 모드를 사용하면 모든 카탈로그 및 제품 스토어 특정 데이터가 기본 스토어 보기에서 모든 스토어 보기 범위로 복사됩니다. 스토어에 하나의 스토어 뷰만 있는 경우 카탈로그 및 제품 데이터만 복사됩니다. 저장소에 비활성화된 저장소와 활성화된 저장소가 한 개 있는 경우 카탈로그 및 제품 데이터가 복사되지 않습니다.<br/> 단일 저장소 모드를 사용하면 콘텐츠 관련 데이터에 대한 storeview 관련 구성 설정이 무시됩니다. 대신 전역 수준 범위에 정의된 구성 설정을 사용하여 관리 UI와 상점 간 일관성을 보장합니다. |

{style="table-layout:auto"}

## [!UICONTROL Data Services]

![일반 > 데이터 서비스](./assets/general-data-services.png)<!-- zoom -->

| 필드 | [범위](../../getting-started/websites-stores-views.md#scope-settings) | 설명 |
|--- |--- |--- |
| [!UICONTROL Commerce Events Enabled] | 글로벌 | 의료 서비스 고객이고 [데이터 서비스 HIPAA](https://experienceleague.adobe.com/en/docs/commerce/data-connection/hipaa-readiness) 확장을 설치한 경우 이 구성은 기본적으로 꺼져 있습니다. 따라서 라이브 검색 및 제품 추천에 사용되는 상점 이벤트 데이터는 더 이상 캡처되지 않습니다. 이는 storefront 이벤트 데이터가 클라이언트측에서 생성되기 때문입니다. [실시간 검색](https://experienceleague.adobe.com/en/docs/commerce/live-search/overview) 및 [제품 추천](https://experienceleague.adobe.com/en/docs/commerce/product-recommendations/guide-overview) 서비스에서 사용할 상점 이벤트 데이터를 계속 캡처하고 보내려면 **Commerce 이벤트 사용**&#x200B;을(를) `Yes`(으)로 설정하십시오. |

{style="table-layout:auto"}
