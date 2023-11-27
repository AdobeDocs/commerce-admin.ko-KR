---
title: 인벤토리 확장 및 재구성
description: 다중 소스 판매자로 확장하거나 단일 소스 판매자로 축소하는 방법에 대해 알아봅니다.
exl-id: 880474e3-6533-4b2f-adf7-4312787ff736
feature: Inventory, Configuration
source-git-commit: 4d89212585fa846eb94bf83a640d0358812afbc5
workflow-type: tm+mt
source-wordcount: '209'
ht-degree: 0%

---

# 인벤토리 확장 및 재구성

비즈니스가 성장하고 변화함에 따라 [!DNL Inventory Management] 은(는) 귀하의 요구 사항을 지원합니다. 멀티 소스 판매자로 확장하거나 단일 소스 판매자로 쉽게 축소할 수 있습니다.

## 다중 소스로 확장

1인 가맹점은 새로운 점포, 창고, 적하 화주 등을 추가할 수 있다. 확장을 사용하려면 다중 소싱으로 확장하기 위해 몇 가지 추가 및 재고 업데이트만 필요합니다.

1. 추가 [사용자 정의 소스](sources-add.md) 각 새 위치에 대해.

   번들 제품에는 기본 소스만 사용합니다.

1. 추가 [사용자 정의 재고](stocks-add.md) 필요한 경우 새 소스에 추가합니다.

   예를 들어 웹 사이트, 국가, 로케일 또는 기타 방법별로 주식을 만들 수 있습니다. 소스를 사용자 정의 재고에 지정할 수 있습니다. 번들 제품에는 기본 스톡만 사용합니다.

1. 업데이트 [출처 지정 및 수량](quantities-manage.md) 을 참조하십시오.

   다음을 사용할 수도 있습니다 [일괄 작업 도구](bulk-assignment.md) 및 [Import-Export](inventory-import-export.md) 소스 및 제품 데이터를 빠르게 추가하는 기능입니다.

## 단일 소스로 재구성

온라인 판매를 한 곳으로 줄여 출하하려는 복수 출처 상인의 경우 출처, 재고 및 수량을 수정하여 갱신합니다.

1. 사용 안 함 [사용자 정의 소스](sources-disable.md).

1. 제품 재고를 기본 출처로 이전합니다.

   대량 작업을 사용하는 것이 좋습니다. 다음을 참조하십시오 [재고를 출처로 이전](inventory-transfer.md).

1. 에 모든 웹 사이트 할당 [기본 재고](stocks-manage.md).
