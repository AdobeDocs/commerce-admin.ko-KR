---
title: '[!UICONTROL Sales] > [!UICONTROL Shipping Settings]'
description: Commerce 관리자의 [!UICONTROL Sales] > [!UICONTROL Shipping Settings] 페이지에서 구성 설정을 검토합니다.
exl-id: d7d46946-f8c9-4714-96c3-2173e28f7bfa
feature: Configuration, Shipping/Delivery
TQID: https://experienceleague.adobe.com/4-Kmcd3F8pQyMgxp-NmkBFVNuEXWuYn-BOzpvxuFMhU
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2:
  - id: dac87252-6066-4d6e-a9d2-f6d84c323de7
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2:
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 204
ht-degree: 1%

---

# [!UICONTROL Sales] > [!UICONTROL Shipping Settings]

{{config}}

이러한 설정 변경에 대한 자세한 내용은 _저장 및 구매 경험 안내서_&#x200B;에서 [배송 설정](../../stores-purchase/shipping-settings.md)을 참조하세요.

## [!UICONTROL Origin]

![원본](./assets/shipping-settings-origin.png)<!-- zoom -->

| 필드 | [범위](../../getting-started/websites-stores-views.md#scope-settings) | 설명 |
|--- |--- |--- |
| [!UICONTROL Country] | 웹 사이트 | 원산지국. |
| [!UICONTROL Region/State] | 웹 사이트 | 원점 영역 또는 상태입니다. |
| [!UICONTROL ZIP/Postal Code] | 웹 사이트 | 출발지 ZIP 또는 우편 번호. |
| [!UICONTROL City] | 웹 사이트 | 원점 도시. |
| [!UICONTROL Street Address] | 웹 사이트 | 출발지 주소. |
| [!UICONTROL Street Address Line 2] | 웹 사이트 | 필요한 경우 출발지 주소 추가 줄. |

{style="table-layout:auto"}

## [!UICONTROL Shipping Policy Parameters]

![전달 정책 매개 변수](./assets/shipping-settings-shipping-policy-parameters.png)<!-- zoom -->

| 필드 | [범위](../../getting-started/websites-stores-views.md#scope-settings) | 설명 |
|--- |--- |--- |
| [!UICONTROL Apply Custom Shipping Policy] | 웹 사이트 | 체크아웃 중에 배송 정책이 표시되는지 여부를 결정합니다. 옵션: `Yes` / `No` |
| [!UICONTROL Shipping Policy] | 스토어 뷰 | 배송 정책을 텍스트로 포함합니다. |

{style="table-layout:auto"}

## [!UICONTROL Shipment Tracking URLs]

[!BADGE SaaS만]{type=Positive url="https://experienceleague.adobe.com/ko/docs/commerce/user-guides/product-solutions" tooltip="Adobe Commerce as a Cloud Service 프로젝트에만 적용됩니다(Adobe 관리 SaaS 인프라)."}

![전달 정책 매개 변수](./assets/shipping-settings-shipment-tracking-urls.png)<!-- zoom -->

| 필드 | [범위](../../getting-started/websites-stores-views.md#scope-settings) | 설명 |
|--- |--- |--- |
| [!UICONTROL Enable Custom Tracking URLs] | 스토어 뷰 | 쇼핑객 이메일에 전송된 배송 추적 번호가 링크인지 일반 텍스트인지 결정합니다. 기본값인 `No`은(는) 숫자가 일반 텍스트임을 나타냅니다. 옵션: `Yes` / `No` |
| [!UICONTROL USPS Tracking URL] | 스토어 뷰 | 미국 우편 서비스 배송에 대한 URL 템플릿입니다. |
| [!UICONTROL UPS Tracking URL] | 스토어 뷰 | 통합 소포 서비스 배송에 대한 URL 템플릿입니다. |
| [!UICONTROL FedEx Tracking URL] | 스토어 뷰 | Federal Express 배송의 URL 템플릿입니다. |
| [!UICONTROL DHL Tracking URL] | 스토어 뷰 | DHL Express 발송을 위한 URL 템플릿. |

{style="table-layout:auto"}
