---
title: 배송 레이블 및 패키지 만들기
description: 항목을 주문으로 패키징하고 배송 레이블을 만드는 방법을 알아봅니다.
exl-id: ed9be72a-0dcd-4dbf-82ba-b1d75a1e76fd
feature: Shipping/Delivery, Orders
source-git-commit: c9acf475eeadcd249467e4cc89fe61d37230bd7d
workflow-type: tm+mt
source-wordcount: '1944'
ht-degree: 0%

---

# 배송 레이블 만들기

선적 레이블을 만들려면 먼저 라벨을 지원하도록 선적 회사 계정을 설정해야 합니다. 그런 다음 프롬프트에 따라 패키지 및 해당 내용에 대한 설명을 입력합니다.

Commerce은 운송 레이블 정보를 구성하고 주문을 제출하면 운송 회사 시스템에 연결하여 주문을 제출하고 운송 레이블과 추적 번호를 수신합니다. 시스템에 이 배송에 대한 배송 레이블이 있으면 새 레이블로 교체됩니다. 그러나 기존 추적 번호는 대체되지 않습니다. 모든 새 추적 번호가 기존 추적 번호에 추가됩니다.

## 1단계: 운송 업체에 문의

시작하기 전에 배송 계정이 라벨을 처리하도록 설정되어 있는지 확인하십시오. 일부 운송업체는 배송 라벨을 계정에 추가하는 데 추가 요금을 부과할 수 있습니다.

스토어에 대한 배송 레이블을 활성화하는 데 사용하는 각 운송업체에 문의하십시오.

각 운송업체에서 제공한 지침에 따라 배송 라벨 지원을 계정에 추가합니다.

- **FedEx** - 계정의 레이블 인쇄 요구 사항에 대해 알아보려면 [FedEx Web Integration Services][1]에 문의하십시오.
- **USPS** - Shiper 지원 센터의 [Web Tools API 포털][4]을 참조하여 레이블 인쇄 자격 증명을 설정하는 방법에 대해 알아보십시오.
- **UPS**- [UPS][2]에 문의하여 계정의 배송 레이블을 지원하는지 확인하십시오. 배송 레이블을 생성하려면 UPS XML 옵션을 사용해야 합니다.
- **DHL** - 계정의 레이블 인쇄 요구 사항에 대해 알아보려면 [DHL 전자 상거래 솔루션][3]에 문의하십시오.

## 2단계: 각 통신사에 대한 구성 업데이트

1. [저장소 정보](../getting-started/store-details.md#store-information)가 완료되었는지 확인하세요.

1. _관리자_ 사이드바에서 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**(으)로 이동합니다.

1. 왼쪽 패널에서 **[!UICONTROL Sales]**&#x200B;을(를) 확장하고 **[!UICONTROL Shipping Settings]**&#x200B;을(를) 선택합니다.

1. ![&#x200B; 섹션에서 &#x200B;](../assets/icon-display-expand.png)확장 선택기&#x200B;**[!UICONTROL Origin]**&#x200B;을(를) 확장하고 **[!UICONTROL Shipping Origin Address]**&#x200B;을(를) 구성합니다.

1. 레이블 인쇄를 위해 활성화된 각 통신사 계정에 대해 아래 지침을 따르십시오.

### UPS 구성

유나이티드 택배 서비스는 국내와 해외에서 모두 수송합니다. 단, 배송 라벨은 미국 내에서 발생한 배송에 대해서만 생성할 수 있습니다.

1. 왼쪽 패널의 _[!UICONTROL Sales]_&#x200B;섹션에서&#x200B;**[!UICONTROL Delivery Methods]**&#x200B;을(를) 선택합니다.

1. ![&#x200B; 섹션에서 &#x200B;](../assets/icon-display-expand.png)확장 선택기&#x200B;**[!UICONTROL UPS]**&#x200B;를 확장합니다.

1. UPS **[!UICONTROL Shipper Number]**&#x200B;이(가) 올바른지 확인하십시오.

   [!DNL United Parcel Service XML]이(가) 활성화된 경우에만 배송자 번호가 표시됩니다.

1. **[!UICONTROL Save Config]**&#x200B;을(를) 클릭합니다.

### USPS 구성

[!DNL United States Postal Service]은(는) 국내 및 해외로 발송됩니다.

{{$include /help/_includes/usps-api-type-configuration-note.md}}

1. **[!UICONTROL Delivery Methods]** 구성을 계속 진행하여 ![&#x200B; 섹션에서 &#x200B;](../assets/icon-display-expand.png)확장 선택기&#x200B;**[!UICONTROL USPS]**&#x200B;를 확장합니다.

1. **[!UICONTROL USPS Type]**&#x200B;을(를) `USPS Rest APIs` 또는 `USPS Web Tools API`(으)로 선택합니다.

1. **[!UICONTROL Secure Gateway URL]**&#x200B;이(가) 올바른지 확인하십시오.

1. USPS에서 제공한 **[!UICONTROL Password]**&#x200B;을(를) 입력하십시오.

1. 선택한 **[!UICONTROL USPS Type]**&#x200B;을(를) 기반으로 다음 구성이 완료되었는지 확인하십시오.

   USPS Web Tools API를 사용하는 경우:
   - 사용자 ID
   - 암호

   USPS REST API를 사용하는 경우:
   - 소비자 키
   - 소비자 암호
   - 가격 옵션
   - 계정 유형
   - 계정 번호
   - 고객 등록 ID(CRID)
   - MID(Mailer Identifier)
   - 매니페스트 MID
   - AES/ITN

1. **[!UICONTROL Size]**&#x200B;을(를) `Large`(으)로 설정하고 다음 차원에 대한 값을 입력하십시오.

   - Length
   - 폭
   - 높이
   - 둘레

1. **[!UICONTROL Save Config]**&#x200B;을(를) 클릭합니다.

### FedEx 구성

FedEx는 국내외에서 선박을 운항합니다. 미국 이외의 지역에 위치한 상점에서는 국제 배송에 대해서만 FedEx 레이블을 만들 수 있습니다.

1. **[!UICONTROL Delivery Methods]** 구성을 계속 진행하여 ![&#x200B; 섹션에서 &#x200B;](../assets/icon-display-expand.png)확장 선택기&#x200B;**[!UICONTROL FedEx]**&#x200B;를 확장합니다.

1. 다음 FedEx 자격 증명이 올바른지 확인합니다.

   - 미터 번호
   - 키
   - 암호

1. **[!UICONTROL Save Config]**&#x200B;을(를) 클릭합니다.

### DHL 구성

DHL은 국제 배송 서비스를 제공합니다.

1. **[!UICONTROL Delivery Methods]** 구성을 계속 진행하여 ![&#x200B; 섹션에서 &#x200B;](../assets/icon-display-expand.png)확장 선택기&#x200B;**[!UICONTROL DHL]**&#x200B;를 확장합니다.

1. **[!UICONTROL Gateway URL]**&#x200B;이(가) 올바른지 확인하십시오.

1. 다음 자격 증명이 완료되었는지 확인합니다.

   - 액세스 ID
   - 암호
   - 계정 번호

1. **[!UICONTROL Save Config]**&#x200B;을(를) 클릭합니다.

## 3단계: 배송 레이블 만들기

### 방법 1: 새 선적에 대한 레이블 생성

1. _관리자_ 사이드바에서 **[!UICONTROL Sales]** > **[!UICONTROL Orders]**(으)로 이동합니다.

1. 그리드에서 순서를 찾아 레코드를 엽니다.

   주문 상태는 `Pending` 또는 `Processing`이어야 합니다.

1. 오른쪽 상단에서 **[!UICONTROL Ship]**&#x200B;을(를) 클릭합니다.

1. 운송업체 요구 사항에 따라 배송 정보를 확인합니다.

1. 오른쪽 아래 모서리에서 **[!UICONTROL Create Shipping Label]** 확인란을 선택합니다.

1. **[!UICONTROL Submit Shipment]**&#x200B;을(를) 클릭합니다.

1. 패키지의 제품 추가 또는 업데이트:

   - 주문의 제품을 패키지에 추가하려면 **[!UICONTROL Add Products]**&#x200B;을(를) 클릭합니다. _[!UICONTROL Quantity]_&#x200B;열은 패키지에 사용할 수 있는 최대 제품 수를 표시합니다.

   - 패키지에 추가할 각 제품의 확인란을 선택하고 각 제품의 **[!UICONTROL Quantity]**&#x200B;을(를) 입력하십시오. **[!UICONTROL Add Selected Product(s) to Package]**&#x200B;을(를) 클릭합니다.

   - 패키지를 추가하려면 **[!UICONTROL Add Package]**&#x200B;을(를) 클릭합니다.

   - 패키지를 삭제하려면 **[!UICONTROL Delete Package]**&#x200B;을(를) 클릭합니다.

   - 주문을 취소하려면 **[!UICONTROL Cancel]**&#x200B;을(를) 클릭합니다. 배송 레이블이 만들어지지 않고 _[!UICONTROL Create Shipping Label]_&#x200B;확인란이 지워졌습니다.

   >[!NOTE]
   >
   >기본값 이외의 패키지 유형을 사용하거나 서명이 필요한 경우 배송 비용이 고객에게 청구한 비용과 다를 수 있습니다. 배송비의 차이는 매장에 반영되지 않습니다.

1. **[!UICONTROL OK]**&#x200B;을(를) 클릭합니다.

   Commerce은 운송 회사 시스템에 연결하여 주문을 제출하고 각 패키지에 대한 배송 레이블 및 추적 번호를 수신합니다.

### 방법 2: 기존 선적에 대한 레이블 생성

1. _관리자_ 사이드바에서 **[!UICONTROL Sales]** > _[!UICONTROL Operations]_>**[!UICONTROL Orders]**(으)로 이동합니다.

1. 격자에서 주문을 찾아 배송 양식을 엽니다.

1. _[!UICONTROL Shipping and Tracking Information]_&#x200B;섹션에서&#x200B;**[!UICONTROL Create Shipping Label]**&#x200B;을(를) 클릭합니다.

1. 주문한 제품을 적절한 패키지에 배포하고 **[!UICONTROL OK]**&#x200B;을(를) 클릭합니다.

1. 패키지 정보를 검토하려면 **[!UICONTROL Show Packages]**&#x200B;을(를) 클릭합니다.

## 4단계: 레이블 인쇄

배송 레이블은 PDF 형식으로 생성되며, 책임자로부터 인쇄할 수 있습니다. 각 레이블에는 주문 번호와 패키지 번호가 포함됩니다.

>[!NOTE]
>
>각 패키지에 대한 개별 배송 주문이 생성되므로 단일 배송에 대해 여러 배송 라벨을 받을 수 있습니다.

### 방법 1: 선적 양식에서 라벨 인쇄

1. _관리 사이드바_&#x200B;에서 다음 페이지 중 하나로 이동한 다음 배송 기록을 찾습니다.

   - **[!UICONTROL Sales]** > **[!UICONTROL Orders]** - 그리드에서 순서를 찾아 레코드를 엽니다. 왼쪽 패널에서 **[!UICONTROL Shipments]**&#x200B;을(를) 선택합니다. 그런 다음 배송 기록을 엽니다.

   - **[!UICONTROL Sales]** > **[!UICONTROL Shipments]** - 그리드에서 배송물을 찾아 레코드를 엽니다.

1. PDF 파일을 다운로드하려면 양식의 _[!UICONTROL Shipping and Tracking]_&#x200B;섹션으로 이동하여&#x200B;**[!UICONTROL Print Shipping Label]**&#x200B;을(를) 클릭합니다.

   브라우저 설정에 따라 PDF 파일에서 직접 배송 레이블을 보고 인쇄할 수 있습니다.

   _[!UICONTROL Print Shipping Label]_&#x200B;단추는 통신사가 배송에 대한 레이블을 생성한 후에만 나타납니다. 단추가 없으면&#x200B;**[!UICONTROL Create Shipping Label]**&#x200B;을(를) 클릭하십시오. 버튼은 Commerce이 통신사에서 레이블을 받으면 나타납니다.

### 방법 2: 복수 주문에 대한 레이블 인쇄

1. _관리 사이드바_&#x200B;에서 다음 페이지 중 하나로 이동한 다음 인쇄할 주문이나 배송을 선택하십시오.

   - **[!UICONTROL Sales]** > **[!UICONTROL Orders]** - 그리드에서 인쇄할 배송 레이블이 있는 각 주문의 확인란을 선택합니다.

   - **[!UICONTROL Sales]** > **[!UICONTROL Shipments]** - 그리드에서 인쇄할 레이블이 있는 각 선적의 확인란을 선택합니다.

1. **[!UICONTROL Actions]** 컨트롤을 `Print Shipping Labels`(으)로 설정합니다.

1. **[!UICONTROL Submit]**&#x200B;을(를) 클릭합니다.

선택한 주문과 관련된 각 납품에 대해 전체 출하 라벨 세트가 인쇄됩니다.

## 필수 통신사 설정

| 필드 | 설명 |
|--- |--- |
| [!UICONTROL Type] | 패키지 유형은 통신사와 방법별로 다릅니다. 각 통신사의 기본 패키지 유형이 초기에 선택됩니다. USPS는 국내 선적에 패키지 유형이 필요하지 않습니다. |
| [!UICONTROL Customs Value] | (국제 배송만 해당) 국제 배송 내용의 신고된 값 또는 판매 가격. |
| [!UICONTROL Total Weight] | 패키지에 추가된 모든 제품의 총 무게는 자동으로 계산됩니다. 값을 수동으로 변경하고 파운드 또는 킬로그램으로 입력할 수도 있습니다. |
| [!UICONTROL Length, Width, Height] | (선택 사항) 패키지 차원은 사용자 지정 패키지에만 사용됩니다. 측정 단위를 인치 또는 센티미터로 지정할 수 있습니다.<br/><br/>**[!UICONTROL Not Required]**: 배송 회사가 게재 확인을 스토어로 보내지 않습니다.<br/><br/>**[!UICONTROL No Signature]**: 받는 사람의 서명이 없는 배달 확인서는 배송 회사가 상점으로 보냅니다.<br/><br/>**[!UICONTROL Signature Required]**: 배송 회사가 받는 사람의 서명을 받고 저장소에 인쇄된 복사본을 제공합니다.<br/><br/>**[!UICONTROL Direct]**: (FedEx만 해당) FedEx가 게재 주소에서 다른 사람의 서명을 받습니다. 패키지를 서명할 수 있는 사람이 없으면 통신사는 다른 시간에 패키지를 배달하려고 시도합니다.<br/><br/>**[!UICONTROL Indirect]**: (FedEx 주거용 게재만 해당) FedEx는 게재 주소에서 누군가(주변 또는 건물 관리자일 수 있음)의 서명을 가져옵니다. 수신자는 서명된 FedEx 문 태그를 남겨 아무도 서명하지 않고 패키지를 남길 수 있도록 승인할 수 있습니다.<br/><br/>**[!UICONTROL Contents]**: (USPS만 해당) 패키지에 대한 다음 설명 중 하나를 선택하십시오.<br/>- 선물<br/>- 문서<br/>- 상업용 샘플<br/>- 반품된 제품<br/>- 상품<br/>- 기타&#x200B;<br/><br/>**[!UICONTROL Explanation]**: (USPS만 해당) 패키지 콘텐츠에 대한 자세한 설명.<br/><br/>**[!UICONTROL Adult Required]**: 배송 회사가 성인 수신자의 서명을 받고 상점에 인쇄된 복사본을 제공합니다. |

{style="table-layout:auto"}

## 패키지 만들기

배송 레이블을 만들도록 선택하면 _[!UICONTROL Create Packages]_&#x200B;창이 나타납니다. 첫 번째 패키지 구성을 즉시 시작할 수 있습니다.

### 패키지 구성

>[!NOTE]
>
>[!UICONTROL Type]에 대해 기본값이 아닌 값을 선택하거나 서명 확인이 필요하도록 선택하는 경우 배송 가격이 고객에게 청구한 가격과 다를 수 있습니다.

1. 배송된 제품 목록을 보고 패키지에 추가하려면 **[!UICONTROL Add Products]**&#x200B;을(를) 클릭합니다.

   - 제품 및 수량을 지정합니다.

     _[!UICONTROL Qty]_&#x200B;열은 추가할 수 있는 최대 수량을 표시합니다. 첫 번째 패키지의 경우 숫자는 출하될 제품의 총 수량입니다.

   - 패키지에 제품을 추가하려면 **[!UICONTROL Add Selected Product(s) to Package]**&#x200B;을(를) 클릭합니다.

1. 패키지를 추가하려면 **[!UICONTROL Add Package]**&#x200B;을(를) 클릭합니다.

   여러 패키지를 추가하고 동시에 편집할 수 있습니다.

1. 패키지를 삭제하려면 **[!UICONTROL Delete Package]**&#x200B;을(를) 클릭합니다.

제품이 패키지에 추가된 후에는 수량을 직접 편집할 수 없습니다.

### 수량 늘리기

1. **[!UICONTROL Add Selection]**&#x200B;을(를) 클릭합니다.

1. 추가 수량을 입력합니다.

   패키지 내 이전 제품 수량에 번호가 추가됩니다.

### 수량 감소

1. 패키지에서 제품을 삭제합니다.

1. **[!UICONTROL Add Selection]**&#x200B;을(를) 클릭합니다.

1. 새롭고 더 작은 값을 입력합니다.

### 배송 레이블 생성

모든 제품을 배포한 후 사용할 총 패키지 수는 목록의 마지막 패키지 수와 같습니다. 배송된 모든 항목이 패키지로 배포되고 필요한 모든 정보가 완료될 때까지 _확인_ 단추를 사용할 수 없습니다.

레이블을 생성하려면 **[!UICONTROL OK]**&#x200B;을(를) 클릭하십시오.

필요한 경우 **[!UICONTROL Cancel]**&#x200B;을(를) 클릭하여 프로세스를 중지할 수 있습니다. 패키지가 저장되지 않고 배송 레이블 프로세스가 취소되었습니다.

### 필드 설명

| 필드 | 설명 |
|--- |--- |
| [!UICONTROL Type] | 패키지의 유형을 지정합니다. 미리 정의된 값 중 하나를 선택합니다. 사용 가능한 패키지 유형은 각 운송 업체마다 다릅니다. 패키지 생성 팝업 창이 열리면 유형 필드에 운송 회사의 기본 패키지가 나타납니다. 운송 회사가 설계하지 않은 패키지를 선택하는 경우 패키지의 차원을 입력해야 합니다. DHL, FedEx 및 UPS 배송에 대해 생성된 배송 레이블의 경우 [상품 유형] 필드가 `Merchandise`(으)로 설정됩니다. USPS의 경우 필드는 _창의_ Contents _[!UICONTROL Create Packages]_&#x200B;필드에 있는 값을 반영합니다. |
| [!UICONTROL Total Weight] | 패키지의 총 무게입니다. 필드는 패키지에 있는 제품의 총 중량으로 미리 채워집니다. 측정 단위는 파운드 또는 킬로그램으로 설정할 수 있습니다. |
| [!UICONTROL Length] | 패키지의 길이, 정수 및 부동 소수점 숫자. 사용자 지정 패키지 유형을 사용하는 경우 필드가 활성화됩니다. 측정 단위는 인치 또는 센티미터로 설정할 수 있습니다. |
| [!UICONTROL Width] | 패키지의 너비, 정수 및 부동 소수점 숫자. 사용자 지정 패키지 유형을 사용하는 경우 필드가 활성화됩니다. 측정 단위는 높이 필드 옆에 있는 드롭다운 메뉴를 사용하여 지정할 수 있습니다. 인치와 센티미터 중에서 선택합니다. |
| [!UICONTROL Height] | 패키지 높이, 정수 및 부동 소수점 숫자. 사용자 지정 패키지 유형을 사용하는 경우 필드가 활성화됩니다. 측정 단위는 높이 필드 옆에 있는 드롭다운 메뉴를 사용하여 지정할 수 있습니다. 인치와 센티미터 중에서 선택합니다. |
| [!UICONTROL Signature] | 게재 확인을 정의합니다. 옵션:<br/><br/>**[!UICONTROL Not Required]**: 배달 확인 편지를 보내지 않았습니다.<br/><br/>**[!UICONTROL No Signature]**: 받는 사람의 서명이 없는 배달 확인 편지를 보냅니다.<br/><br/>**[!UICONTROL Signature Required]**: 배송 회사가 받는 사람의 서명을 받고 인쇄된 복사본을 제공합니다.<br/><br/>**[!UICONTROL Adult Required]**: 배송 회사가 성인 수신자의 서명을 받고 인쇄된 복사본을 제공합니다.<br/><br/>**[!UICONTROL Direct (FedEx only)]**: FedEx는 배달 주소에서 다른 사람의 서명을 받고 패키지에 서명할 수 있는 사람이 없으면 배달을 다시 시도합니다.<br/><br/>**[!UICONTROL Indirect (FedEx only)]**: FedEx는 다음 세 가지 방법 중 하나로 서명을 받습니다. <br/>(1) 배달 주소의 다른 사람으로부터, <br/>(2) 이웃, 건물 관리자 또는 주소의 다른 사람으로부터, 또는 <br/>(3) 받는 사람이 아무도 없이 패키지의 릴리스를 승인하는 서명된 FedEx Door 태그를 남길 수 있습니다. 가정용 게재에만 사용할 수 있습니다. 배송 방법마다 옵션이 조금씩 다를 수 있습니다. 최신 정보는 운송 회사의 리소스를 참조하십시오. |
| [!UICONTROL Contents] | (USPS 발송에만 사용 가능) 패키지 내용물에 대한 설명. 옵션: `Gift` / `Documents` / `Commercial Sample` / `Returned Goods` / `Merchandise` / `Other` |
| [!UICONTROL Explanation] | (USPS 배송만 해당) 패키지 콘텐츠에 대한 자세한 설명. |

{style="table-layout:auto"}

[1]: https://www.fedex.com/en-us/api/get-support.html
[2]: https://www.ups.com/us/en/support/contact-us.page
[3]: https://www.dhl.com/us-en/home/our-divisions/ecommerce-solutions.html
[4]: https://www.usps.com/business/web-tools-apis/#ssc

<!-- Last updated from includes: 2025-11-26 10:55:00 -->
