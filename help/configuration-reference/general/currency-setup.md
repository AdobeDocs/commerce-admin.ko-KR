---
title: '[!UICONTROL General] &gt; [!UICONTROL Currency Setup]'
description: 에서 구성 설정을 검토합니다. [!UICONTROL General] &gt; [!UICONTROL Currency Setup] 상거래 관리자의 페이지입니다.
exl-id: a84be30f-f2eb-4c86-942c-2d49e5cf23af
role: Admin
feature: Currency, Configuration, Data Import/Export
source-git-commit: 370131cd73a320b04ee92fa9609cb24ad4c07eca
workflow-type: tm+mt
source-wordcount: '371'
ht-degree: 2%

---

# [!UICONTROL General] > [!UICONTROL Currency Setup]

{{config}}

>[!NOTE]
>
>다음을 참조하십시오 [통화 구성](../../stores-purchase/currency-configuration.md) 이러한 구성에 대한 자세한 내용은 을 참조하십시오.

## [!UICONTROL Currency Options]

![통화 설정 > 통화 옵션](./assets/currency-setup-currency-options.png)<!-- zoom -->

| 필드 | [범위](../../getting-started/websites-stores-views.md#scope-settings) | 설명 |
|--- |--- |--- |
| [!UICONTROL Base Currency] | 웹 사이트 | 모든 온라인 결제 거래에 사용되는 기본 통화. 여러 스토어를 조회하는 경우 가격 범위는 [카탈로그](../catalog/catalog.md) 구성. |
| [!UICONTROL Default Display Currency] | 스토어 뷰 | 가격을 표시하는 데 사용되는 기본 통화. |
| [!UICONTROL Allowed Currencies] | 스토어 뷰 | 스토어에서 결제 시 허용한 통화. |

{:style=&quot;table-layout:auto&quot;}

## [!UICONTROL Fixer.io (legacy)]

>[!IMPORTANT]
>
>2.4.6 릴리스부터 [[!DNL Fixer.io]](https://fixer.io/) 서비스는 더 이상 사용되지 않으며 [[!DNL Fixer API] (APILayer)](https://apilayer.com/marketplace/fixer-api) 서비스. 더 이상 사용되지 않는 계정 대신 APILayer 계정을 사용하는 것이 좋습니다 [!DNL Fixer.io] 계정입니다.

![통화 설정 > Fixer.io](./assets/currency-setup-fixer.png)<!-- zoom -->

| 필드 | [범위](../../getting-started/websites-stores-views.md#scope-settings) | 설명 |
|--- |--- |--- |
| [!UICONTROL API key] | 글로벌 | 를 통해 전환 서비스에 액세스하는 데 사용되는 키 [!DNL fixer.io] 계정입니다. 자세한 내용은 [[!DNL fixer.io]](https://fixer.io/). |
| [!UICONTROL Connection Timeout in Seconds] | 글로벌 | Fixer.io 세션이 시간 초과되기 전의 비활성 시간(초)을 결정합니다. 기본값: `100` |

{:style=&quot;table-layout:auto&quot;}

## [!UICONTROL Fixer Api (APILayer)]

![통화 설정 > Fixer Api(APILayer)](./assets/currency-setup-fixer-api.png)<!-- zoom -->

| 필드 | [범위](../../getting-started/websites-stores-views.md#scope-settings) | 설명 |
|--- |--- |--- |
| [!UICONTROL API key] | 글로벌 | 를 통해 전환 서비스에 액세스하는 데 사용되는 키 [!DNL APILayer] 계정입니다. 자세한 내용은 [[!DNL APILayer]](https://apilayer.com/). |
| [!UICONTROL Connection Timeout in Seconds] | 글로벌 | 다음 시간 이전의 비활성 시간(초)을 결정합니다. [!DNL APILayer] 세션 시간이 초과되었습니다. 기본값은 입니다. `100`. |

{:style=&quot;table-layout:auto&quot;}

## [!UICONTROL Currency Converter API]

![통화 설정 > 통화 변환기 API](./assets/currency-setup-converter.png)<!-- zoom -->

| 필드 | [범위](../../getting-started/websites-stores-views.md#scope-settings) | 설명 |
|--- |--- |--- |
| [!UICONTROL API key] | 글로벌 | 전환 서비스에 액세스하는 데 사용되는 키입니다. 자세한 내용은 [[!DNL Currency Convertor] API](https://free.currencyconverterapi.com/). |
| [!UICONTROL Connection Timeout in Seconds] | 글로벌 | 다음 시간 이전의 비활성 시간(초)을 결정합니다. [!DNL Currency Converter] 세션 시간이 초과되었습니다. 기본값:`100` |

{:style=&quot;table-layout:auto&quot;}

## [!UICONTROL Scheduled Import Settings]

![통화 설정 > 예약된 가져오기 설정](./assets/currency-setup-scheduled-import-settings.png)<!-- zoom -->

| 필드 | [범위](../../getting-started/websites-stores-views.md#scope-settings) | 설명 |
|--- |--- |--- |
| [!UICONTROL Enabled] | 스토어 뷰 | 환율에 대해 예약된 가져오기를 사용할지 여부를 결정합니다. 옵션: `Yes` / `No` |
| [!UICONTROL Service] | 스토어 뷰 | 예약된 가져오기에 대한 데이터를 제공하는 서비스를 지정합니다. 기본값은 입니다.`fixer.io` |
| [!UICONTROL Start Time] | 스토어 뷰 | 24시간 시계를 기준으로 시간, 분, 초별로 시작 시간을 나타냅니다. |
| [!UICONTROL Frequency] | 스토어 뷰 | 예약된 가져오기가 발생하는 빈도를 결정합니다. 옵션: `Daily` / `Weekly` / `Monthly` |
| [!UICONTROL Error Email Recipient] | 스토어 뷰 | 예약된 가져오기 오류에 대한 이메일 알림을 받는 각 사용자의 이메일 주소를 식별합니다. 여러 수신자의 경우 각 항목을 쉼표로 구분하십시오. |
| [!UICONTROL Error Email Sender] | 웹 사이트 | 오류 이메일 알림을 보낸 사람으로 표시되는 스토어 연락처를 식별합니다. 기본 발신자: `General Contact` |
| [!UICONTROL Error Email Template] | 웹 사이트 | 오류 이메일 알림의 기반으로 사용되는 템플릿을 지정합니다. 기본 템플릿: `Currency Update Warnings` |

{:style=&quot;table-layout:auto&quot;}
