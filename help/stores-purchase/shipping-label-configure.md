---
title: 배송 레이블 구성
description: 배송 레이블을 생성하기 위한 스토어를 구성하는 방법을 알아봅니다.
exl-id: 0693d74b-8b36-4a36-8739-c9fe5a934ff0
feature: Shipping/Delivery, Orders
source-git-commit: 06673ccb7eb471d3ddea97218ad525dd2cdcf380
workflow-type: tm+mt
source-wordcount: '599'
ht-degree: 0%

---

# 배송 레이블 구성

제품 수준에서 그리고 레이블을 인쇄하는 데 사용되는 각 통신사의 구성에서 다음 설정을 수행해야 합니다. 레이블을 인쇄하려면 모든 통신사에서 계정을 열어야 합니다. 그런 다음 사용할 각 통신사에 대해 스토어에서 구성을 완료합니다.

## 통신사 요구 사항

| [!UICONTROL Carrier] | 요구 사항 |
|-------|--------|
| [USPS](usps.md) | USPS 계정이 필요합니다. 2018년 2월 23일부터 USPS는 모든 선적 라벨에 우표를 포함하도록 요구하고 있습니다. |
| [UPS](ups.md) | UPS 계정이 필요합니다. 배송 레이블은 미국 이외의 상점에 필요한 미국 관련 자격 증명에서 비롯된 배송에 대해서만 사용할 수 있습니다. |
| [FedEx](fedex.md) | FedEx 계정이 필요합니다. 미국 이외 지역 매장의 경우 국제 배송에 대해서만 배송 라벨이 지원됩니다. FedEx는 미국 이외의 지역에서 이루어지는 국내 선적을 허용하지 않습니다 |
| [DHL](dhl.md) | DHL 계정이 필요합니다. 배송 라벨은 미국에서 시작되는 배송에 대해서만 지원됩니다. |

{style="table-layout:auto"}

## 1단계: 제조 국가 확인

USPS와 FedEx로 국제적으로 출하되는 모든 제품에 제조국이 필요합니다. 업데이트해야 하는 제품이 많은 경우 업데이트를 [가져오거나](../systems/data-import.md)하거나 인벤토리 그리드를 사용하여 여러 레코드를 업데이트할 수 있습니다.

1. _관리자_ 사이드바에서 **[!UICONTROL Catalog]** > **[!UICONTROL Products]**(으)로 이동합니다.

1. 다음 방법 중 하나를 사용하여 운송 라벨 레코드를 갱신합니다.

### 방법 1: 단일 레코드 업데이트

1. 그리드에서 업데이트할 제품을 찾은 다음 편집 모드로 엽니다.

1. 필요에 따라 **제조 국가**&#x200B;를 업데이트합니다.

   ![제조 국가](./assets/product-country-of-manufacture.png){width="700" zoomable="yes"}

1. **[!UICONTROL Save]**&#x200B;을(를) 클릭합니다.

### 방법 2: 여러 레코드 업데이트

1. 그리드에서 업데이트할 각 제품의 확인란을 선택합니다.

   예를 들어, 중국에서 제조된 모든 제품.

1. **[!UICONTROL Actions]** 컨트롤을 `Update Attributes`(으)로 설정하고 **[!UICONTROL Submit]**&#x200B;을(를) 클릭합니다.

1. _특성 업데이트_ 양식에서 **제조 국가** 필드를 찾아 **변경** 확인란을 선택합니다.

1. 국가를 선택하세요.

1. **[!UICONTROL Save]**&#x200B;을(를) 클릭합니다.

## 2단계 저장소 정보 확인

1. _관리자_ 사이드바에서 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**(으)로 이동합니다.

1. 왼쪽 패널에서 **[!UICONTROL Sales]**&#x200B;을(를) 확장하고 **[!UICONTROL Shipping Settings]**&#x200B;을(를) 선택합니다.

1. **[!UICONTROL Origin]** 섹션에서 ![확장 선택기](../assets/icon-display-expand.png)를 확장하고 다음 필드가 완료되었는지 확인합니다.

   - **[!UICONTROL Street Address]** - 배송을 보내는 장소의 주소. 예를 들어 회사 또는 창고의 위치입니다. 이 필드는 배송 레이블에 필요합니다.
   - **[!UICONTROL Street Address Line 2]** - 층 또는 출입구와 같은 추가 주소 정보. 이 필드를 사용하는 것이 좋습니다.

   ![원본](../configuration-reference/sales/assets/shipping-settings-origin.png){width="600" zoomable="yes"}

1. 왼쪽 패널의 _판매_ 섹션에서 **[!UICONTROL Delivery Methods]**&#x200B;을(를) 선택합니다.

1. **[!UICONTROL USPS]** 섹션에서 ![확장 선택기](../assets/icon-display-expand.png)를 확장하고 다음 필드가 완료되었는지 확인합니다.

   - **[!UICONTROL Secure Gateway URL]** - 시스템에서 자동으로 게이트웨이 URL을 입력합니다.
   - **[!UICONTROL Password]** - 암호는 USPS에서 제공하며 사용자가 웹 서비스를 통해 해당 시스템에 액세스할 수 있도록 합니다.
   - **길이, 너비, 높이, 길이** - 패키지의 기본 차원입니다. 이러한 필드를 표시하려면 **[!UICONTROL Size]**&#x200B;을(를) `Large`(으)로 설정하십시오.

1. **FedEx** 섹션에서 ![확장 선택기](../assets/icon-display-expand.png)을(를) 확장하고 다음 필드가 완료되었는지 확인합니다.

   - 미터 번호
   - 키
   - 암호

   이 정보는 통신사가 제공하며 웹 서비스를 통해 시스템에 액세스하는 데 필요합니다.

1. 왼쪽 패널에서 **[!UICONTROL General]**&#x200B;을(를) 확장하고 아래의 **[!UICONTROL General]**&#x200B;을(를) 선택합니다.

1. **[!UICONTROL Store Information]** 섹션에서 ![확장 선택기](../assets/icon-display-expand.png)를 확장하고 다음 필드가 완료되었는지 확인합니다.

   - **[!UICONTROL Store Name]** - 스토어 또는 스토어 보기의 이름입니다.
   - **[!UICONTROL Store Contact Telephone]** - 스토어 또는 스토어 보기에 대한 기본 연락처의 전화 번호입니다.
   - **[!UICONTROL Country]** - 스토어의 기반이 되는 국가입니다.
   - **[!UICONTROL VAT Number]** - 해당되는 경우 스토어의 부가가치세 번호. (미국에 본사를 둔 매장에는 필요하지 않음)
   - **[!UICONTROL Store Contact Address]** - 스토어 또는 스토어 보기에 대한 기본 연락처의 거리 주소입니다.

1. 저장소가 여러 개이고 연락처 정보가 기본값과 다른 경우 각각에 대해 **[!UICONTROL Store View]**&#x200B;을(를) 설정하고 정보가 완료되었는지 확인하십시오.

   정보가 누락된 경우 레이블을 인쇄하려고 하면 오류가 나타납니다.

   ![정보 저장](../configuration-reference/general/assets/general-store-information.png){width="600" zoomable="yes"}

1. **[!UICONTROL Save Config]**&#x200B;을(를) 클릭합니다.
