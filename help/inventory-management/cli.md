---
title: '[!DNL Inventory Management] CLI 참조'
description: 인벤토리 데이터 및 구성 설정을 관리하기 위해  [!DNL Inventory Management] 모듈에서 제공하는 명령에 대해 알아봅니다.
exl-id: d92dffce-94a1-443c-8c72-98fecbbd5320
level: Experienced
feature: Inventory, Configuration
badgePaas: label="PaaS만" type="Informative" url="https://experienceleague.adobe.com/ko/docs/commerce/user-guides/product-solutions" tooltip="Adobe Commerce 온 클라우드 프로젝트(Adobe 관리 PaaS 인프라) 및 온프레미스 프로젝트에만 적용됩니다."
source-git-commit: b4623ada788d44f4628930dcf5dfcb51dd88ee3a
workflow-type: tm+mt
source-wordcount: '843'
ht-degree: 0%

---

# [!DNL Inventory Management] CLI 참조

[!DNL Inventory Management]은(는) 인벤토리 데이터 및 구성 설정을 관리하는 명령을 제공합니다.

이러한 명령에는 다음이 포함됩니다.

- 판매 가능 수량에 영향을 주는 예약 불일치 확인 및 해결
- 거리 우선순위 알고리즘에 대한 지오코드 추가

## 예약 불일치 해결

예약은 재고에 따라 제품 SKU에 대한 판매 가능 수량을 보류합니다. 주문을 출하, 추가, 취소 또는 환불 시 보상 예약이 입력되어 이러한 보류를 배치하거나 정산합니다.

[!DNL Inventory Management]은(는) 두 가지 명령을 제공하여 예약 불일치를 확인하고 해결합니다.

- [&#39;인벤토리:reservation:목록 불일치&#39;](#list-inconsistencies-command)
- [&#39;인벤토리:reservation:만들기-보상&#39;](#create-compensations-command)

### 예약 불일치의 원인

[!DNL Inventory Management]은(는) 주요 이벤트에 대한 예약을 생성합니다.

- 주문 배치(초기 예약)
- 주문 출하(보상 예약)
- 환불 주문 또는 대변 메모 발행(보상 예약)
- 주문 취소(보상 예약)

다음과 같은 경우 예약 불일치가 발생할 수 있습니다.

- [!DNL Inventory Management]은(는) 초기 예약을 상실하고 너무 많은 예약 보상을 입력합니다(너무 많이 보상하여 금액이 일치하지 않음).
- [!DNL Inventory Management]은(는) 초기 예약을 올바르게 지정하지만 보상 예약은 손실됩니다.

`inventory_reservation` 테이블에서 수동으로 예약을 검토하고 확인할 수 있습니다.

다음 구성 및 이벤트로 인해 예약 불일치가 발생할 수 있습니다.

- **최종 상태(완료, 취소됨 또는 마감됨)가 아닌 주문과 함께 2.3.x로 업그레이드하십시오.** [!DNL Inventory Management]이(가) 이러한 주문에 대해 보상 예약을 만들지만 판매 가능 수량에서 차감하는 초기 예약을 입력하거나 사용하지 않습니다. 2.1.x 또는 2.2.x에서 Adobe Commerce 또는 Magento Open Source v2.3.x로 업그레이드한 후 이러한 명령을 사용하는 것이 좋습니다. 대기 중인 주문이 있는 경우 명령은 판매 가능 수량 및 판매 및 주문 이행에 대한 예약을 올바르게 갱신합니다.
- **재고를 관리하지 않고 나중에 이 구성을 변경합니다.** 구성에서 **[!UICONTROL Manage Stock]**&#x200B;이(가) `No`(으)로 설정된 2.3.x를 사용할 수 있습니다. [!DNL Commerce]은(는) 주문 배치 및 배송 이벤트에 예약하지 않습니다. 나중에 **[!UICONTROL Manage Stock]** 구성을 사용하도록 설정하고 일부 주문이 만들어지면 해당 주문을 처리하고 이행할 때 보상 예약으로 판매 가능 수량이 손상됩니다.
- **주문이 웹 사이트에 제출되는 동안 웹 사이트에 대한 재고를 다시 할당합니다**. 초기 예약은 초기 재고에 대해 입력하고 모든 보상 예약은 신규 재고에 대해 입력합니다.
- **모든 예약의 합계가 `0`(으)로 확인되지 않을 수 있습니다.** 최종 상태(완료, 취소됨, 마감됨)의 주문 범위에 있는 모든 예약은 `0`(으)로 확인되어야 하며 판매 가능한 수량 보류가 모두 지워집니다.

### 목록 불일치 명령

`list-inconsistencies` 명령은 모든 예약 불일치를 감지하고 나열합니다. 명령 옵션을 사용하여 완료 또는 미완료 주문만 선택하거나 모두 확인합니다.

```bash
bin/magento inventory:reservation:list-inconsistencies
```

명령 옵션:

- `-c`, `--complete-orders` - 완료된 주문의 불일치를 반환합니다. 완료된 주문에 대해 잘못된 예약이 여전히 보류 중일 수 있습니다.
- `-i`, `--incomplete-orders` - 불완전한 주문(부분적으로 배송됨, 배송되지 않음)에 대한 불일치를 반환합니다. 잘못된 예약은 주문에 대해 너무 많거나 충분한 판매 수량을 보유하지 못할 수 있습니다.
- `-b`, `--bunch-size` - 한 번에 로드할 주문 수를 정의합니다.
- `-r`, `--raw` - 원시 출력입니다.

`-r`을(를) 사용한 응답이 `<ORDER_INCREMENT_ID>:<SKU>:<QUANTITY>:<STOCK-ID>` 형식으로 반환됩니다.

- 주문 ID는 불일치 범위를 나타냅니다.
- SKU는 불일치가 있는 제품을 나타냅니다.
- 수량은 예약 보상에 대해 입력할 금액을 설정합니다.
- 재고 ID는 예약을 사용하여 판매 가능한 수량을 계산하는 재고 범위를 정의합니다.

예:

```bash
bin/magento inventory:reservation:list-inconsistencies

Inconsistencies found on following entries:
Order 172:
- Product bike-123 should be compensated by +2.000000 for stock 1
```

```bash
bin/magento inventory:reservation:list-inconsistencies -r

172:bike-123:+2.000000:1
```

문제가 발견되지 않으면 이 메시지는 주문 불일치가 발견되지 않았음을 반환합니다.

### 보상 만들기 명령

`create-compensations` 명령은 보상 예약을 만듭니다. 문제에 따라 판매 가능 수량을 보류하거나 릴리즈하기 위해 신규 예약이 생성됩니다.

예약을 만들려면 `172:bike-123:+2.000000:1`과(와) 같은 `<ORDER_INCREMENT_ID>:<SKU>:<QUANTITY>:<STOCK-ID>` 형식을 사용하여 보상을 제공하십시오.

```bash
bin/magento inventory:reservation:create-compensations
```

명령 옵션:

- `-r`, `--raw` - 원시 출력을 반환합니다.

요청 형식이 올바르지 않으면 다음 메시지가 표시됩니다.

```
Error while parsing argument "your_incorrect_format_argument". Given argument does not match pattern "/(?P<increment_id>.*):(?P<sku>.*):(?P<quantity>.*):(?P<stock_id>.*)/".
```

이 명령은 예약을 만들 때 SKU, 주문 및 재고 별 업데이트를 나타내는 메시지를 표시합니다.

```bash
bin/magento inventory:reservation:create-compensations 172:bike-123:+2.000000:1

Following reservations were created:
- Product bike-123 was compensated by +2.000000 for stock 1
```

보상 항목에 대한 SKU에 공백이 포함된 경우 SKU를 따옴표로 묶습니다.

```bash
bin/magento inventory:reservation:create-compensations 172:"bike 123":+2.000000:1
```

### 불일치 항목 탐지 및 보상 만들기

파이프를 사용하여 `list-inconsistencies`과(와) `create-compensations`을(를) 모두 실행하여 불일치를 감지하고 즉시 보상을 만들 수 있습니다. `-r` 명령 옵션을 사용하여 원시 데이터를 생성하여 `create-compensations`에 제출합니다.

```bash
bin/magento inventory:reservation:list-inconsistencies -r | bin/magento inventory:reservation:create-compensations
```

응답 예:

```bash
bin/magento inventory:reservation:list-inconsistencies -r | bin/magento inventory:reservation:create-compensations
```

```
Following reservations were created:
- Product bike-123 was compensated by +2.000000 for stock 1
- Product bikehat-456 was compensated by +1.000000 for stock 1
```

업데이트가 완료되면 list 명령을 실행하여 다음을 확인합니다.

```bash
bin/magento inventory:reservation:list-inconsistencies -r
```

```
No order inconsistencies were found.
```

불일치 항목을 감지하고 불완전 주문(`-i`) 또는 완전 주문(`-c`)에 대한 보상만 생성하도록 명령을 파이프할 수도 있습니다.

```bash
bin/magento inventory:reservation:list-inconsistencies -r -i | bin/magento inventory:reservation:create-compensations
```

```bash
bin/magento inventory:reservation:list-inconsistencies -r -c | bin/magento inventory:reservation:create-compensations
```

## 지역 코드 가져오기

[!DNL Inventory Management]은(는) 전체 또는 부분 주문을 배송하는 데 가장 적합한 옵션을 결정하는 데 도움이 되는 [거리 우선 순위 알고리즘](distance-priority-algorithm.md)을 제공합니다. 이 알고리즘은 GPS 정보 또는 지오코드를 사용하여 주문에서 각 품목의 출처(창고 또는 기타 물리적 위치)와 운송 주소 간의 거리를 계산합니다. 알고리즘에서는 이러한 결과를 기반으로 각 항목을 순서대로 발송하는 데 사용해야 하는 소스를 권장합니다.

판매자는 거리 계산에 필요한 GPS 또는 지역 코드 데이터 제공업체를 선택합니다.

- **Google MAP**&#x200B;은(는) [Google Maps Platform](https://mapsplatform.google.com/) 서비스를 사용하여 배송 대상 주소와 원본 위치 간의 거리 및 시간을 계산합니다. 이 옵션을 사용하려면 Google 결제 플랜이 필요하며 Google을 통해 요금이 발생할 수 있습니다.

- **오프라인 계산**&#x200B;은(는) [geonames.org](https://www.geonames.org/)에서 다운로드하고 명령을 사용하여 Commerce으로 가져온 데이터를 사용하여 거리를 계산합니다. 이 옵션은 무료입니다.

오프라인 계산을 위해 지오코드를 가져오려면 다음을 수행합니다.

공백으로 구분된 [ISO-3166 alpha2 국가 코드](https://www.geonames.org/countries/) 목록과 함께 다음 명령을 입력하십시오.

```bash
bin/magento inventory-geonames:import <country code> <country code> ...
```

For example:

```bash
bin/magento inventory-geonames:import us ca gb de
```

시스템에서 지오코드 데이터를 다운로드하여 데이터베이스로 가져온 다음 `Importing <country code>: OK` 메시지를 표시합니다.
