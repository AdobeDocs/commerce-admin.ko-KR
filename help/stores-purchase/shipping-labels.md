---
title: 배송 레이블
description: 정기적 배송의 배송 라벨 워크플로우 및 반품 상품 권한이 있는 제품에 대해 알아봅니다.
exl-id: 5da03cf9-5e92-4bb8-ba53-67c6469665ed
feature: Shipping/Delivery, Orders
TQID: https://experienceleague.adobe.com/Cjf9-372TRGIfWXpWR20OUII5XorPdfO1qgG-b2yPYI
product_v2: id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2: id: c1256247-af4b-46d8-9dca-0c654ecfa157
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
level_v2: id: b5a62a22-46f7-4f0d-b151-3fc640bef588id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2: id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 314
ht-degree: 0%

---

# 배송 레이블

Commerce에는 주요 운송 회사와의 높은 수준의 통합이 포함되어 있으므로 운송 회사 운송 시스템에 액세스하여 주문을 추적하고 운송 레이블을 만드는 등의 작업을 수행할 수 있습니다. 반품상품 허가를 받은 정규 선적 및 제품에 대해 선적 라벨을 생성할 수 있습니다. 라벨에는 운송회사가 제공하는 정보 외에도 Commerce 주문 번호, 패키지 번호, 운송을 위한 총 패키지 수량도 포함됩니다.

![USPS 우선 순위 배송 레이블](./assets/shipping-usps-priority-label.png){width="300"}

- [배송 레이블 구성](shipping-label-configure.md)
- [배송 레이블 및 패키지 만들기](shipping-label-create.md)

## 배송 레이블 워크플로

선적 레이블은 선적이 생성된 시점 또는 그 이후에 생성될 수 있습니다. 배송 레이블은 PDF 형식으로 저장되고 컴퓨터로 다운로드됩니다.

### 1단계: 판매자가 운송 레이블 요청을 실행합니다.

판매자/점포 관리자는 라벨을 생성하는 데 필요한 정보를 완료하고 요청을 제출합니다.

### 2단계: 통신사에 전송된 요청

Commerce은 운송 회사에 연락하여 운송 회사의 시스템에서 주문을 생성합니다. 배송되는 각 패키지에 대해 별도의 주문이 생성됩니다.

### 3단계: 운송업체가 레이블 및 추적 번호를 보냄

운송업체는 운송물에 대한 배송 레이블과 추적 번호를 보냅니다.

- 여러 패키지가 있는 단일 선적은 여러 선적 레이블을 받습니다.

- 동일한 배송 레이블을 여러 번 생성하는 경우 원래 추적 번호가 유지됩니다.

- RMA 번호가 있는 반품된 제품의 경우 이전 추적 번호가 새 번호로 교체됩니다.

### 4단계: 판매자가 레이블을 다운로드하고 인쇄합니다.

배송 라벨이 생성된 후, 새로운 배송이 저장되고 라벨이 인쇄될 수 있습니다. 연결의 문제 또는 다른 이유로 배송 레이블을 만들 수 없는 경우 배송이 만들어지지 않습니다. 브라우저 설정에 따라 PDF 파일을 열고 인쇄할 수 있습니다. 각 레이블은 PDF의 별도 페이지에 표시됩니다.
