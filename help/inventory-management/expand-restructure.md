---
title: 인벤토리 확장 및 재구성
description: 다중 소스 판매자로 확장하거나 단일 소스 판매자로 축소하는 방법에 대해 알아봅니다.
exl-id: 880474e3-6533-4b2f-adf7-4312787ff736
feature: Inventory, Configuration
TQID: https://experienceleague.adobe.com/w4TV-BQrg0RzlHn4DVSdHFPD2M5CF11wA7I5OyA7jsY
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2:
  - id: c1256247-af4b-46d8-9dca-0c654ecfa157
  - id: dac87252-6066-4d6e-a9d2-f6d84c323de7
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: f8a45b24-4be7-4f1b-909b-60d06b483a20
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2:
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 219
ht-degree: 0%

---

# 인벤토리 확장 및 재구성

비즈니스가 성장하고 변화함에 따라 [!DNL Inventory Management]에서 사용자의 요구 사항을 지원합니다. 멀티 소스 판매자로 확장하거나 단일 소스 판매자로 쉽게 축소할 수 있습니다.

## 다중 소스로 확장

1인 가맹점은 새로운 점포, 창고, 적하 화주 등을 추가할 수 있다. 확장을 사용하려면 다중 소싱으로 확장하기 위해 몇 가지 추가 및 재고 업데이트만 필요합니다.

1. 각 새 위치에 대해 [사용자 지정 소스](sources-add.md)를 추가하십시오.

   번들 제품에는 기본 Source만 사용합니다.

1. 필요에 따라 새 소스에 [사용자 지정 재고](stocks-add.md)를 추가합니다.

   예를 들어 웹 사이트, 국가, 로케일 또는 기타 방법별로 주식을 만들 수 있습니다. 소스를 사용자 정의 재고에 지정할 수 있습니다. 번들 제품에는 기본 스톡만 사용합니다.

1. 제품에 대한 [소스 할당 및 수량](quantities-manage.md)을(를) 업데이트합니다.

   [일괄 작업 도구](bulk-assignment.md) 및 [가져오기-내보내기](inventory-import-export.md) 기능을 사용하여 소스와 제품 데이터를 빠르게 추가할 수도 있습니다.

## 단일 소스로 재구성

온라인 판매를 한 곳으로 줄여 출하하려는 복수 출처 상인의 경우 출처, 재고 및 수량을 수정하여 갱신합니다.

1. [사용자 지정 원본](sources-disable.md)을 사용하지 않도록 설정하십시오.

1. 제품 인벤토리를 기본 Source으로 전송합니다.

   대량 작업을 사용하는 것이 좋습니다. [Source으로 인벤토리 전송](inventory-transfer.md)을 참조하세요.

1. [기본 재고](stocks-manage.md)에 모든 웹 사이트를 할당하십시오.
