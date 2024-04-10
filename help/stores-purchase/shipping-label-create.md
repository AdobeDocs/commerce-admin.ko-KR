---
title: 배송 레이블 및 패키지 만들기
description: 항목을 주문으로 패키징하고 배송 레이블을 만드는 방법을 알아봅니다.
exl-id: ed9be72a-0dcd-4dbf-82ba-b1d75a1e76fd
feature: Shipping/Delivery, Orders
source-git-commit: 06673ccb7eb471d3ddea97218ad525dd2cdcf380
workflow-type: tm+mt
source-wordcount: '1889'
ht-degree: 0%

---

# 배송 레이블 만들기

선적 레이블을 만들려면 먼저 라벨을 지원하도록 선적 회사 계정을 설정해야 합니다. 그런 다음 프롬프트에 따라 패키지 및 해당 내용에 대한 설명을 입력합니다.

운송 레이블 정보를 구성하고 주문을 제출하면 Commerce는 운송 회사 시스템에 연결하여 주문을 제출하고 운송 레이블과 추적 번호를 수신합니다. 시스템에 이 배송에 대한 배송 레이블이 있으면 새 레이블로 교체됩니다. 그러나 기존 추적 번호는 대체되지 않습니다. 모든 새 추적 번호가 기존 추적 번호에 추가됩니다.

## 1단계: 운송 업체에 문의

시작하기 전에 배송 계정이 라벨을 처리하도록 설정되어 있는지 확인하십시오. 일부 운송업체는 배송 라벨을 계정에 추가하는 데 추가 요금을 부과할 수 있습니다.

스토어에 대한 배송 레이블을 활성화하는 데 사용하는 각 운송업체에 문의하십시오.

각 운송업체에서 제공한 지침에 따라 배송 라벨 지원을 계정에 추가합니다.

- **페덱스** - 연락처 [FedEx 웹 통합 서비스][1] 를 사용하여 계정의 레이블 인쇄 요구 사항에 대해 알아봅니다.
- **USPS** - 다음을 참조하십시오. [웹 도구 API 포털][4] 쉬퍼 지원 센터에서 라벨 인쇄 자격 증명을 설정하는 방법에 대해 알아보십시오.
- **UPS**- 연락처 [UPS][2] 계정이 배송 레이블을 지원하는지 확인하기 위해. 배송 레이블을 생성하려면 UPS XML 옵션을 사용해야 합니다.
- **DHL** - 연락처 [DHL 전자 상거래 솔루션][3] 를 사용하여 계정의 레이블 인쇄 요구 사항에 대해 알아봅니다.

## 2단계: 각 통신사에 대한 구성 업데이트

1. 다음을 확인하십시오. [정보 저장](../getting-started/store-details.md#store-information) 이(가) 완료되었습니다.

1. 다음에서 _관리자_ 사이드바, 이동 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. 왼쪽 패널에서 를 확장합니다. **[!UICONTROL Sales]** 및 선택 **[!UICONTROL Shipping Settings]**.

1. 확장 ![확장 선택기](../assets/icon-display-expand.png) 다음 **[!UICONTROL Origin]** 섹션 및 구성 **[!UICONTROL Shipping Origin Address]**.

1. 레이블 인쇄를 위해 활성화된 각 통신사 계정에 대해 아래 지침을 따르십시오.

### UPS 구성

유나이티드 택배 서비스는 국내와 해외에서 모두 수송합니다. 단, 배송 라벨은 미국 내에서 발생한 배송에 대해서만 생성할 수 있습니다.

1. 다음에서 _[!UICONTROL Sales]_왼쪽 패널에서 섹션 을 선택합니다.**[!UICONTROL Delivery Methods]**.

1. 확장 ![확장 선택기](../assets/icon-display-expand.png) 다음 **[!UICONTROL UPS]** 섹션.

1. UPS 확인 **[!UICONTROL Shipper Number]** 맞습니다.

   발송자 번호는 다음과 같은 경우에만 나타납니다. [!DNL United Parcel Service XML] 이(가) 활성화되었습니다.

1. 클릭 **[!UICONTROL Save Config]**.

### USPS 구성

다음 [!DNL United States Postal Service] 선박은 국내외를 막론하고 운항한다.

1. 에서 계속 **[!UICONTROL Delivery Methods]** 구성, 확장 ![확장 선택기](../assets/icon-display-expand.png) 다음 **[!UICONTROL USPS]** 섹션.

1. 다음을 확인합니다 **[!UICONTROL Secure Gateway URL]** 맞습니다.

1. 다음을 입력합니다. **[!UICONTROL Password]** usps에서 제공한 경우.

1. 설정 **[!UICONTROL Size]** 끝 `Large` 을 누르고 다음 차원에 대한 값을 입력합니다.

   - Length
   - 폭
   - 높이
   - 둘레

1. 클릭 **[!UICONTROL Save Config]**.

### FedEx 구성

FedEx는 국내외에서 선박을 운항합니다. 미국 이외의 지역에 위치한 상점에서는 국제 배송에 대해서만 FedEx 레이블을 만들 수 있습니다.

1. 에서 계속 **[!UICONTROL Delivery Methods]** 구성, 확장 ![확장 선택기](../assets/icon-display-expand.png) 다음 **[!UICONTROL FedEx]** 섹션.

1. 다음 FedEx 자격 증명이 올바른지 확인합니다.

   - 미터 번호
   - 키
   - 암호

1. 클릭 **[!UICONTROL Save Config]**.

### DHL 구성

DHL은 국제 배송 서비스를 제공합니다.

1. 에서 계속 **[!UICONTROL Delivery Methods]** 구성, 확장 ![확장 선택기](../assets/icon-display-expand.png) 다음 **[!UICONTROL DHL]** 섹션.

1. 다음을 확인합니다 **[!UICONTROL Gateway URL]** 맞습니다.

1. 다음 자격 증명이 완료되었는지 확인합니다.

   - 액세스 ID
   - 암호
   - 계정 번호

1. 클릭 **[!UICONTROL Save Config]**.

## 3단계: 배송 레이블 만들기

### 방법 1: 새 선적에 대한 레이블 생성

1. 다음에서 _관리자_ 사이드바, 이동 **[!UICONTROL Sales]** > **[!UICONTROL Orders]**.

1. 그리드에서 순서를 찾아 레코드를 엽니다.

   주문 상태는 다음 중 하나여야 합니다. `Pending` 또는 `Processing`.

1. 오른쪽 위 모서리에서 을(를) 클릭합니다. **[!UICONTROL Ship]**.

1. 운송업체 요구 사항에 따라 배송 정보를 확인합니다.

1. 오른쪽 아래 모서리에서 **[!UICONTROL Create Shipping Label]** 확인란.

1. 클릭 **[!UICONTROL Submit Shipment]**.

1. 패키지의 제품 추가 또는 업데이트:

   - 주문의 제품을 패키지에 추가하려면 **[!UICONTROL Add Products]**. 다음 _[!UICONTROL Quantity]_열에는 패키지에 사용할 수 있는 최대 제품 수가 표시됩니다.

   - 패키지에 추가할 각 제품의 확인란을 선택하고 **[!UICONTROL Quantity]** 각 그런 다음 을 클릭합니다. **[!UICONTROL Add Selected Product(s) to Package]**.

   - 패키지를 추가하려면 **[!UICONTROL Add Package]**.

   - 패키지를 삭제하려면 **[!UICONTROL Delete Package]**.

   - 주문을 취소하려면 **[!UICONTROL Cancel]**. 배송 레이블이 만들어지지 않고 _[!UICONTROL Create Shipping Label]_확인란이 선택 취소됩니다.

   >[!NOTE]
   >
   >기본값 이외의 패키지 유형을 사용하거나 서명이 필요한 경우 배송 비용이 고객에게 청구한 비용과 다를 수 있습니다. 배송비의 차이는 매장에 반영되지 않습니다.

1. 클릭 **[!UICONTROL OK]**.

   Commerce는 운송 회사 시스템에 연결하여 주문을 제출하고 각 패키지에 대한 배송 레이블 및 추적 번호를 수신합니다.

### 방법 2: 기존 선적에 대한 레이블 생성

1. 다음에서 _관리자_ 사이드바, 이동 **[!UICONTROL Sales]** > _[!UICONTROL Operations]_>**[!UICONTROL Orders]**.

1. 격자에서 주문을 찾아 배송 양식을 엽니다.

1. 다음에서 _[!UICONTROL Shipping and Tracking Information]_섹션, 클릭&#x200B;**[!UICONTROL Create Shipping Label]**.

1. 주문된 제품을 적절한 패키지에 배포하고 **[!UICONTROL OK]**.

1. 패키지 정보를 검토하려면 **[!UICONTROL Show Packages]**.

## 4단계: 레이블 인쇄

배송 레이블은 PDF 형식으로 생성되며, 책임자로부터 인쇄할 수 있습니다. 각 레이블에는 주문 번호와 패키지 번호가 포함됩니다.

>[!NOTE]
>
>각 패키지에 대한 개별 배송 주문이 생성되므로 단일 배송에 대해 여러 배송 라벨을 받을 수 있습니다.

### 방법 1: 선적 양식에서 라벨 인쇄

1. 다음에서 _관리 사이드바_&#x200B;다음 페이지 중 하나로 이동한 다음 배송 기록을 찾습니다.

   - **[!UICONTROL Sales]** > **[!UICONTROL Orders]** - 그리드에서 순서를 찾아 레코드를 엽니다. 왼쪽 패널에서 을 선택합니다 **[!UICONTROL Shipments]**. 그런 다음 배송 기록을 엽니다.

   - **[!UICONTROL Sales]** > **[!UICONTROL Shipments]** - 그리드에서 출하를 찾고 레코드를 엽니다.

1. PDF 파일을 다운로드하려면 _[!UICONTROL Shipping and Tracking]_섹션에 있는 마지막 항목이&#x200B;**[!UICONTROL Print Shipping Label]**.

   브라우저 설정에 따라 PDF 파일에서 직접 배송 레이블을 보고 인쇄할 수 있습니다.

   다음 _[!UICONTROL Print Shipping Label]_운송회사가 운송물에 대한 라벨을 생성한 후에만 버튼이 표시됩니다. 단추가 없으면&#x200B;**[!UICONTROL Create Shipping Label]**. 이 단추는 Commerce가 통신사에서 레이블을 받으면 나타납니다.

### 방법 2: 복수 주문에 대한 레이블 인쇄

1. 다음에서 _관리 사이드바_&#x200B;을 클릭하고 다음 페이지 중 하나로 이동한 다음 인쇄할 주문 또는 납품을 선택합니다.

   - **[!UICONTROL Sales]** > **[!UICONTROL Orders]** - 그리드에서 인쇄할 배송 레이블이 있는 각 주문의 확인란을 선택합니다.

   - **[!UICONTROL Sales]** > **[!UICONTROL Shipments]** - 그리드에서 인쇄할 레이블이 있는 각 선적의 확인란을 선택합니다.

1. 설정 **[!UICONTROL Actions]** 제어 대상 `Print Shipping Labels`.

1. 클릭 **[!UICONTROL Submit]**.

선택한 주문과 관련된 각 납품에 대해 전체 출하 라벨 세트가 인쇄됩니다.

## 필수 통신사 설정

| 필드 | 설명 |
|--- |--- |
| [!UICONTROL Type] | 패키지 유형은 통신사와 방법별로 다릅니다. 각 통신사의 기본 패키지 유형이 초기에 선택됩니다. USPS는 국내 선적에 패키지 유형이 필요하지 않습니다. |
| [!UICONTROL Customs Value] | (국제 배송만 해당) 국제 배송 내용의 신고된 값 또는 판매 가격. |
| [!UICONTROL Total Weight] | 패키지에 추가된 모든 제품의 총 무게는 자동으로 계산됩니다. 값을 수동으로 변경하고 파운드 또는 킬로그램으로 입력할 수도 있습니다. |
| [!UICONTROL Length, Width, Height] | (선택 사항) 패키지 차원은 사용자 지정 패키지에만 사용됩니다. 측정 단위를 인치 또는 센티미터로 지정할 수 있습니다.<br/><br/>**[!UICONTROL Not Required]**: 배송 운송업체가 매장으로 배송 확인을 보내지 않습니다.<br/><br/>**[!UICONTROL No Signature]**: 수령인의 서명이 없는 배송 확인서는 배송업체가 매장으로 보냅니다.<br/><br/>**[!UICONTROL Signature Required]**: 운송주선인이 수령인의 서명을 받고 인쇄본을 매장에 제공합니다.<br/><br/>**[!UICONTROL Direct]**: (FedEx만 해당) FedEx는 게재 주소에서 누군가의 서명을 받습니다. 패키지를 서명할 수 있는 사람이 없으면 통신사는 다른 시간에 패키지를 배달하려고 시도합니다.<br/><br/>**[!UICONTROL Indirect]**: (FedEx 주거용 게재만 해당) FedEx는 게재 주소에서 누군가(이웃 또는 건물 관리자일 수 있음)의 서명을 가져옵니다. 수신자는 서명된 FedEx 문 태그를 남겨 아무도 서명하지 않고 패키지를 남길 수 있도록 승인할 수 있습니다.<br/><br/>**[!UICONTROL Contents]**: (USPS만 해당) 패키지에 대한 다음 설명 중 하나를 선택합니다.<br/>- 선물<br/>- 문서<br/>- 상업용 샘플<br/>반품<br/>- 상품<br/>- 기타&#x200B;<br/><br/>**[!UICONTROL Explanation]**: (USPS만 해당) 패키지 콘텐츠에 대한 자세한 설명입니다.<br/><br/>**[!UICONTROL Adult Required]**: 운송업자가 성인 수령인의 서명을 받고 인쇄된 사본을 스토어에 제공합니다. |

{style="table-layout:auto"}

## 패키지 만들기

다음 _[!UICONTROL Create Packages]_배송 레이블을 만들도록 선택하면 창이 나타납니다. 첫 번째 패키지 구성을 즉시 시작할 수 있습니다.

### 패키지 구성

>[!NOTE]
>
>에 대해 기본값이 아닌 값을 선택하는 경우 [!UICONTROL Type] 또는 서명 확인이 필요하도록 선택할 경우 배송 가격이 고객에게 청구한 가격과 다를 수 있습니다.

1. 배송된 제품 목록을 보고 패키지에 추가하려면 **[!UICONTROL Add Products]**.

   - 제품 및 수량을 지정합니다.

     다음 _[!UICONTROL Qty]_열에는 추가할 수 있는 최대 수량이 표시됩니다. 첫 번째 패키지의 경우 숫자는 출하될 제품의 총 수량입니다.

   - 제품을 패키지에 추가하려면 **[!UICONTROL Add Selected Product(s) to Package]**.

1. 패키지를 추가하려면 **[!UICONTROL Add Package]**.

   여러 패키지를 추가하고 동시에 편집할 수 있습니다.

1. 패키지를 삭제하려면 **[!UICONTROL Delete Package]**.

제품이 패키지에 추가된 후에는 수량을 직접 편집할 수 없습니다.

### 수량 늘리기

1. 클릭 **[!UICONTROL Add Selection]**.

1. 추가 수량을 입력합니다.

   패키지 내 이전 제품 수량에 번호가 추가됩니다.

### 수량 감소

1. 패키지에서 제품을 삭제합니다.

1. 클릭 **[!UICONTROL Add Selection]**.

1. 새롭고 더 작은 값을 입력합니다.

### 배송 레이블 생성

모든 제품을 배포한 후 사용할 총 패키지 수는 목록의 마지막 패키지 수와 같습니다. 다음 _확인_ 배송된 모든 품목이 패키지로 배포되고 필요한 모든 정보가 완료될 때까지 버튼이 비활성화됩니다.

레이블을 생성하려면 다음을 클릭하십시오. **[!UICONTROL OK]**.

다음을 클릭할 수 있습니다. **[!UICONTROL Cancel]** 필요한 경우 프로세스를 중지합니다. 패키지가 저장되지 않고 배송 레이블 프로세스가 취소되었습니다.

### 필드 설명

| 필드 | 설명 |
|--- |--- |
| [!UICONTROL Type] | 패키지의 유형을 지정합니다. 미리 정의된 값 중 하나를 선택합니다. 사용 가능한 패키지 유형은 각 운송 업체마다 다릅니다. 패키지 생성 팝업 창이 열리면 유형 필드에 운송 회사의 기본 패키지가 나타납니다. 운송 회사가 설계하지 않은 패키지를 선택하는 경우 패키지의 차원을 입력해야 합니다. DHL, FedEx 및 UPS 선적을 위해 생성된 선적 라벨의 경우, 상품 유형 필드가 로 설정됩니다. `Merchandise`. USPS의 경우 필드는 의 값을 반영합니다. _내용_ 의 필드 _[!UICONTROL Create Packages]_창. |
| [!UICONTROL Total Weight] | 패키지의 총 무게입니다. 필드는 패키지에 있는 제품의 총 중량으로 미리 채워집니다. 측정 단위는 파운드 또는 킬로그램으로 설정할 수 있습니다. |
| [!UICONTROL Length] | 패키지의 길이, 정수 및 부동 소수점 숫자. 사용자 지정 패키지 유형을 사용하는 경우 필드가 활성화됩니다. 측정 단위는 인치 또는 센티미터로 설정할 수 있습니다. |
| [!UICONTROL Width] | 패키지의 너비, 정수 및 부동 소수점 숫자. 사용자 지정 패키지 유형을 사용하는 경우 필드가 활성화됩니다. 측정 단위는 높이 필드 옆에 있는 드롭다운 메뉴를 사용하여 지정할 수 있습니다. 인치와 센티미터 중에서 선택합니다. |
| [!UICONTROL Height] | 패키지 높이, 정수 및 부동 소수점 숫자. 사용자 지정 패키지 유형을 사용하는 경우 필드가 활성화됩니다. 측정 단위는 높이 필드 옆에 있는 드롭다운 메뉴를 사용하여 지정할 수 있습니다. 인치와 센티미터 중에서 선택합니다. |
| [!UICONTROL Signature] | 게재 확인을 정의합니다. 옵션:<br/><br/>**[!UICONTROL Not Required]**: 전송 확인 편지를 보내지 않았습니다.<br/><br/>**[!UICONTROL No Signature]**: 수신자의 서명이 없는 게재 확인 편지를 보냅니다.<br/><br/>**[!UICONTROL Signature Required]**: 배송 운송업체가 수취인의 서명을 받고 인쇄된 사본을 제공합니다.<br/><br/>**[!UICONTROL Adult Required]**: 배송 회사가 성인 수령인의 서명을 받고 인쇄된 사본을 제공합니다.<br/><br/>**[!UICONTROL Direct (FedEx only)]**: FedEx는 게재 주소에서 누군가의 서명을 받고 아무도 패키지에 서명할 수 없는 경우 게재를 재시도합니다.<br/><br/>**[!UICONTROL Indirect (FedEx only)]**: FedEx는 다음 세 가지 방법 중 하나로 서명을 받습니다.<br/>(1) 주소지에 있는 사람으로부터 <br/>(2) 이웃, 건물 관리인 또는 주소지에 있는 다른 사람으로부터; 또는 <br/>(3) 수신자는 아무도 없이 패키지의 릴리스를 승인하는 서명된 FedEx 문 태그를 남길 수 있습니다. 가정용 게재에만 사용할 수 있습니다. 배송 방법마다 옵션이 조금씩 다를 수 있습니다. 최신 정보는 운송 회사의 리소스를 참조하십시오. |
| [!UICONTROL Contents] | (USPS 발송에만 사용 가능) 패키지 내용물에 대한 설명. 옵션: `Gift` / `Documents` / `Commercial Sample` / `Returned Goods` / `Merchandise` / `Other` |
| [!UICONTROL Explanation] | (USPS 배송만 해당) 패키지 콘텐츠에 대한 자세한 설명. |

{style="table-layout:auto"}

[1]: https://www.fedex.com/en-us/api/get-support.html
[2]: https://www.ups.com/us/en/support/contact-us.page
[3]: https://www.dhl.com/us-en/home/our-divisions/ecommerce-solutions.html
[4]: https://www.usps.com/business/web-tools-apis/#ssc
