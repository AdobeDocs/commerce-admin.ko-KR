---
title: 가격 장부
description: '[!DNL Adobe Commerce]의 카탈로그 및 가격 책정 데이터에서 가격 장부를 매핑하는 방법을 알아봅니다.'
role: Admin, Developer
recommendations: noCatalog
badgeSaas: label="SaaS만" type="Positive" url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="CCDM으로 프로비저닝된 Adobe Commerce as a Cloud Service 인스턴스(Adobe 관리 SaaS 인프라)에만 적용됩니다."
TQID: 'https://experienceleague.adobe.com/8gpl-l6oQebTnrt-00-n1FEdKnzqhTQi3hRz4lrGQoE'
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
    internal-label: Commerce
  - id: de2e2e68-c5d7-4efe-be7b-27528698f06b
    internal-label: Commerce as a Cloud Service
feature_v2:
  - id: 3033d2ab-c1d2-5b52-b865-72d9e5ad2c37
    internal-label: Currency
  - id: 58c984c2-e237-5c50-9718-500e40d1e82c
    internal-label: Merchandising
  - id: dac87252-6066-4d6e-a9d2-f6d84c323de7
    internal-label: Configuration
topic_v2:
  - id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
    internal-label: Implementation
source-git-commit: 1041abe0e7d7c1212a717d5fd03180ce7fd32958
workflow-type: tm+mt
source-wordcount: '603'
ht-degree: 0%
---
# 가격 장부

Price Book은 고객 계층 및 시장에서 카탈로그 소스의 제품 가격을 정의합니다. 상위 및 하위 가격 장부의 계층을 지원합니다.

![가격 장부 계층](../assets/price-book-hier.png)

## 주요 개념

| 용어 | 설명 |
| ------ | ------------- |
| **가격표** | 카탈로그 소스의 가격(예: 특정 지역 또는 고객 계층)을 정의하고 제품 가격을 관리하는 데 사용되는 논리적 그룹입니다. |
| **가격표 대체** | 계층 구조에서 가장 가격이 높은 책입니다. 여기에는 상위 항목이 없으며 자신과 모든 하위 항목의 가격 장부를 정의하는 *only* 가격 장부입니다.<br/><br/>가격 장부를 만드는 동안 부모가 정의되지 않은 경우(API를 통해) 새 대체 가격 장부가 만들어집니다. |
| **상위 가격표** | 하위 가격에 명시적으로 설정되지 않은 경우 하위 가격 장부가 가격을 상속할 수 있는 상위 수준의 가격 장부입니다. |
| **계층 구조 깊이** | 최대 3개 수준(대체 -> 하위 -> 손자)<br/><br/>수집 시 적용되지 않습니다. |
| **통화** | 대체 가격 장부에만 정의됩니다. 모든 하위 가격표에 상속됨.<br/><br/>대체 가격 장부를 만드는 동안 통화가 지정되지 않은 경우(API를 통해) 통화 기본값은 USD입니다. |
| **제품 가격** | 특정 가격표 내의 제품(SKU)에 지정된 특정 가격. |
| **할인** | 할인은 제품 가격으로 정의됩니다. 상속되지 않음. |

## 가격 장부 구현

CCDM(Composable Catalog Data Model)과 함께 Adobe Commerce as a Cloud Service을 사용하는 경우 가격 장부는 카탈로그 및 가격 데이터에서 매핑됩니다. 수동으로 만들어지지 않습니다.

높은 수준에서 매핑은 다음과 같습니다.

- **카탈로그 원본→ 대한 스토어 보기** - 지역화된 특성을 포함한 스토어 보기 제품 데이터를 카탈로그 원본에 매핑합니다.
- **웹 사이트 → 가격 장부 또는 가격 장부** - 웹 사이트 가격 정보가 해당 가격 장부 또는 장부에 매핑됩니다.
- **고객 그룹 가격 책정 → 가격 장부 항목**—고객 그룹 가격 책정이 관련 가격 항목에 매핑됩니다.

Adobe Commerce 구성에서 소스 카탈로그, 웹 사이트 및 가격책정 구성을 유지 관리한 다음 사용 가능한 가격 장부를 구성하여 관련 카탈로그 뷰에서 매핑된 가격 장부를 지정합니다. 가격 장부가 지정되지 않은 경우, 카탈로그 뷰는 기본 가격 장부를 사용합니다.

카탈로그 보기는 카탈로그 데이터 및 정책과 함께 사용 가능한 가격 장부 구성을 사용하여 제품에 대해 반환된 가격을 포함하여 머천다이징 경험을 결정합니다.

>[!NOTE]
>
>Commerce B2B의 경우, 시스템은 공유 카탈로그 구성을 기준으로 각 카탈로그 뷰에 단일 가격 장부를 생성하고 지정합니다. 이러한 보기에 대해 가격 장부 가용성을 구성할 필요는 없습니다.

## 체크아웃 가격

가격 책자는 머천다이징 및 상점 카탈로그 경험을 지원합니다. Commerce Core는 장바구니와 체크아웃을 계속 처리합니다. CCDM에서만 사용할 수 있는 가격은 체크아웃에서 사용되는 가격이 자동으로 되지 않습니다.

가격을 Commerce 핵심 구성과 일관되게 유지하고, 구현 유효성 검사의 일부로서 표시된 가격, 장바구니에 추가, 프로모션 및 체크아웃을 테스트합니다.

## 가격 장부 보기

카탈로그 데이터 동기화가 완료되면 **[!UICONTROL Catalog views]** 작업 영역에서 사용 가능한 가격 장부와 해당 ID를 봅니다.

1. _스토어 설정_(으)로 이동한 다음 **[!UICONTROL Catalog views]**&#x200B;을(를) 클릭합니다.

1. **[!UICONTROL Create catalog view]**&#x200B;을(를) 클릭합니다.

1. 카탈로그 보기 구성의 **[!UICONTROL Price Books]** 섹션에서 사용 가능한 가격 장부를 검토하십시오.

   ![가격 장부 이름 및 ID](../assets/price-book-name-ids.png)

## 가격 장부 가용성 구성

Commerce 관리자의 카탈로그 보기 작업 영역에서 사용 가능한 가격 장부를 구성하여 매핑된 가격 장부를 카탈로그 보기와 연결합니다.

>[!NOTE]
>
>비공개 카탈로그 보기([!UICONTROL Catalog Protection]이(가) 활성화된 보기)는 하나의 가격책만 참조할 수 있습니다.

1. **[!UICONTROL Catalog views]** 작업 영역에서 구성할 카탈로그 보기를 선택합니다.

1. **[!UICONTROL Price Books]** 섹션에서 카탈로그 보기에서 지원하는 스토어에 사용할 수 있는 가격 장부를 선택합니다.
