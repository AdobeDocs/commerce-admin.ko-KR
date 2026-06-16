---
title: '[!UICONTROL Sales] > [!UICONTROL Quotes]'
description: Commerce 관리자의 [!UICONTROL Sales] > [!UICONTROL Quotes] 페이지에서 구성 설정을 검토합니다.
exl-id: 9382552d-1be5-47f2-b0e3-931e5c6298d4
feature: Configuration, Quotes
TQID: https://experienceleague.adobe.com/puZjB2YCCyZXT0U6AdDBd-YjxopU637-yxgOaB6hkvM
product_v2: id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2: id: dac87252-6066-4d6e-a9d2-f6d84c323de7
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: ff6a42d2-313e-452e-93a6-792e4fad9ff8
level_v2: id: b5a62a22-46f7-4f0d-b151-3fc640bef588id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2: id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 193
ht-degree: 1%

---

# [!UICONTROL Sales] > [!UICONTROL Quotes]

{{b2b-feature}}

>[!TIP]
>
>Adobe Commerce B2B를 설치하고 활성화하면 회사별 기능을 사용하여 구매 경험을 개인화할 수 있습니다. Adobe Commerce B2B는 B2B 및 B2C 모델을 모두 지원하는 통합 솔루션입니다. B2B 기능에 대한 자세한 내용은 [Adobe Commerce B2B 사용 안내서](https://experienceleague.adobe.com/docs/commerce-admin/b2b/introduction.html)를 참조하십시오.

{{config}}

<!-- [Quotes](https://experienceleague.adobe.com/en/docs/commerce-admin/b2b/quotes/quotes) -->

## [!UICONTROL General]

![일반](./assets/quotes-general.png)<!-- zoom -->

| 필드 | [범위](../../getting-started/websites-stores-views.md#scope-settings) | 설명 |
|--- |--- |--- |
| [!UICONTROL Minimum Amount] | 웹 사이트 | 고객이 견적에 대한 요청을 제출하기 전에 필요한 할인 후 장바구니 소계의 최소 금액입니다. 기본값: `0` |
| [!UICONTROL Minimum Amount Message] | 스토어 뷰 | 고객이 견적에 대한 요청을 제출하려고 하지만 필요한 최소 금액이 충족되지 않을 때 장바구니에 표시되는 메시지입니다. |
| [!UICONTROL Default Expiration Period] | 웹 사이트 | 견적에 대한 요청이 제출된 날로부터 [견적](../../b2b/quote-price-negotiation.md)의 기본 수명을 기간으로 결정합니다. 옵션: `Days` / `Weeks` / `Months` |

{style="table-layout:auto"}

## [!UICONTROL Attached Files]

![첨부 파일](./assets/quotes-attached-files.png)<!-- zoom -->

| 필드 | [범위](../../getting-started/websites-stores-views.md#scope-settings) | 설명 |
|--- |--- |--- |
| [!UICONTROL File formats for upload] | 글로벌 | 견적에 첨부할 수 있는 파일 형식을 결정합니다. 지원되는 기본값: `doc`, `docx`, `xls`, `xlsx`, `pdf`, `txt`, `jpg`, `png` 및 `jpeg` |
| [!UICONTROL Maximum file size] | 글로벌 | 견적에 첨부되는 파일의 최대 크기를 결정합니다. 이 설정은 서버 구성으로 재정의할 수 있습니다. |

{style="table-layout:auto"}
