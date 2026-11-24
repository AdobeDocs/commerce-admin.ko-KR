---
title: 카탈로그 보강 브랜드 규칙 만들기
description: 카탈로그 강화를 위한 브랜드 거버넌스 규칙을 만들고 관리하고, 제품 복사 요구 사항을 정의하고, 카탈로그 강화 작업에 규칙을 적용하는 방법에 대해 알아봅니다.
role: Admin, User, Leader
source-git-commit: 9d7a4f4e98fe2d2d51261d96a2e072c28925babd
workflow-type: tm+mt
source-wordcount: '639'
ht-degree: 1%
---
# 카탈로그 보강 브랜드 규칙 만들기

브랜드 거버넌스 및 브랜드 거버넌스 규칙은 카탈로그 보강에만 사용할 수 있습니다. PDP 보강에는 적용되지 않습니다. 이러한 규칙은 [!DNL Commerce Catalog Agent]에서 생성한 제품 이름 및 설명에 대한 요구 사항을 정의합니다. 기본 브랜드 표준에 대한 기본 규칙을 편집하거나 구성한 다음 특정 캠페인, 제품 카테고리 또는 하위 브랜드에 대한 사용자 지정 규칙을 만듭니다. [카탈로그 보강](catalog-enrichment.md) 작업을 만들 때 규칙을 선택하십시오.

## 오픈 브랜드 거버넌스

1. 관리자에서 **[!UICONTROL AI Product Discovery]** > **[!UICONTROL Catalog Enrichment]**(으)로 이동합니다.
1. **[!UICONTROL Brand Governance]** 탭을 엽니다.

**브랜드 거버넌스** 탭에는 기본 규칙과 사용자가 만든 모든 사용자 지정 규칙이 포함되어 있습니다. 규칙을 검색하거나 규칙 테이블을 필터링할 수 있습니다.

각 행에 대해 **규칙 이름**, **필드**, **색조**, **마지막 수정** 및 **상태**&#x200B;가 표시됩니다. 기본 규칙이 **[!UICONTROL Default]**(으)로 표시되어 있습니다.

**[!UICONTROL Needs your attention]** 영역에는 설정이 필요한 초안 또는 충돌이 있는 규칙과 같이 작업이 필요한 규칙이 강조 표시됩니다. 규칙 세부 사항을 검토하고 **[!UICONTROL Finish setup]** 또는 **[!UICONTROL Fix conflict]**&#x200B;과(와) 같은 사용 가능한 작업을 사용하십시오.

## 규칙 유형 이해

카탈로그 보강은 기본 규칙과 사용자 지정 규칙을 지원합니다.

### 기본 규칙

각 [!DNL Adobe Commerce] 인스턴스에는 정확히 하나의 기본 규칙이 있습니다. [!DNL Adobe Commerce]이(가) 빈 필드를 사용하여 이 규칙을 만듭니다. 이름이 **[!UICONTROL Global]**(으)로 수정되었습니다. 규칙을 편집할 수는 있지만 삭제할 수는 없습니다.

[!DNL Adobe Commerce]은(는) 사용자 지정 규칙을 선택하지 않고 카탈로그 데이터 보강 작업을 만들 때 기본적으로 기본 규칙을 적용합니다. 기본 규칙은 카탈로그 보강에 대한 기본 거버넌스를 제공합니다.

### 사용자 정의 규칙

캠페인, 제품 카테고리 또는 하위 브랜드에 대해 원하는 수만큼 사용자 지정 규칙을 만들 수 있습니다. 사용자 지정 규칙은 자동으로 적용되지 않습니다. 카탈로그 보강 작업을 생성할 때 선택합니다.

사용자 지정 규칙은 기본 규칙에서 값을 상속하지 않습니다. 사용자 지정 규칙을 만들 때 기본 규칙의 현재 값을 일회성 시작점으로 복사할 수 있습니다. 나중에 기본 규칙을 변경해도 사용자 지정 규칙은 업데이트되지 않습니다.

사용자가 사용자 정의 규칙을 선택하지 않은 경우 적용되는 표준에 대해 기본 규칙을 사용합니다. 요구 사항이 다른 캠페인 또는 범주에 대한 사용자 지정 규칙을 만듭니다. 사용자 지정 규칙은 전역 값을 상속하지 않으므로 사용자 지정 규칙에도 필요한 전역 요구 사항을 추가합니다.

## 사용자 지정 규칙 만들기

이 섹션에서는 브랜드 거버넌스 규칙을 만드는 방법을 알아봅니다.

![브랜드 거버넌스 규칙 만들기](./assets/brand-gov-create-rule.png)

1. **브랜드 거버넌스** 탭에서 **[!UICONTROL Create Rule]**&#x200B;을(를) 클릭합니다.
1. 규칙을 시작하는 방법 선택:
   - **[!UICONTROL Blank]**: 모든 값을 직접 설정합니다.
   - **[!UICONTROL Copy Global enrichment]**: 현재 기본 규칙 값을 1회 사본으로 시작합니다.
   - **[!UICONTROL Draft with AI]**: (**곧 출시**) 브랜드 음성을 설명하여 제안된 규칙 값을 가져옵니다.
1. 캠페인, 카테고리 또는 하위 브랜드와 같이 용도를 식별하는 **규칙 이름**&#x200B;을(를) 입력하십시오.
1. **향상시킬 필드**&#x200B;에서 제품 이름 및 제품 설명 요구 사항을 구성합니다.

   제품 이름과 설명을 별도로 구성합니다. 각 필드에는 고유한 활성화 스위치 및 거버넌스 요구 사항이 있습니다.

1. **제품 이름 길이**&#x200B;를 설정합니다.

   보강된 제품 이름에 대한 최소 및 최대 이름 길이 범위를 설정합니다. 예를 들어, 규칙에는 최소 20자에서 최대 200자가 필요할 수 있습니다.

1. **대문자** 옵션을 설정합니다.

   - **[!UICONTROL Sentence case]**: `Waterproof hiking boots`
   - **[!UICONTROL Title Case]**: `Waterproof Hiking Boots`
   - **[!UICONTROL As written]**: 원본 텍스트의 대소문자를 유지합니다.

1. **브랜드 색조**&#x200B;를 설명하십시오. 자세한 내용은 [브랜드 색조 설정](#set-brand-tone)을 참조하세요.
1. 필수 및 제외 구문 설정

   **[!UICONTROL Must include]** 구를 추가합니다.
   **[!UICONTROL Never use]** 구를 추가합니다.

1. 나중에 완료하려면 **[!UICONTROL Save as draft]**&#x200B;을(를) 클릭하고, 카탈로그 데이터 보강 규칙을 만들 때 선택할 수 있는 규칙을 만들려면 **[!UICONTROL Publish rule]**&#x200B;을(를) 클릭하십시오. 저장하지 않고 나가려면 **[!UICONTROL Cancel]**&#x200B;을(를) 클릭하십시오.

1. 이제 [카탈로그 보강](catalog-enrichment.md) 작업에 규칙을 적용할 수 있습니다.

### 브랜드 색조 설정

여러 줄 **[!UICONTROL Brand tone]** 필드에 지침을 입력하여 보강된 이름의 음성 및 스타일을 설명합니다.

다음은 **설명**&#x200B;에 사용할 수 있는 색조의 몇 가지 예입니다.

- **B2B industrial**: `Write for the operator and the buyer. Open with what the unit does and where it fits in the kitchen, then throughput, utility requirements, footprint, and certifications. Plain, technical language. Mention cleaning and maintenance, because total cost of ownership drives the decision. No lifestyle language.`
- **고급 패션**: `Quiet confidence. Lead with craftsmanship and provenance (atelier, tannery, technique), then how the piece wears and ages. Short, measured sentences. Sensory detail is fine. Never compare to other brands or mention price or value.`
- **가전 제품**: `Clear and benefit-led. Turn every spec into what it does for the user. Scannable short paragraphs or bullets. Put compatibility and what's in the box up front. Don't make performance claims without a source, and don't use comparative claims like "fastest"`
- **전문 식품 및 식료품**: `Warm and appetizing, but honest. Describe taste, texture, and aroma in concrete terms, then origin and how it's made, then serving ideas. Plain, friendly language. Put allergens and dietary attributes in a consistent closing line. Don't make health claims.`
- **홈 가구**: `Inviting and practical. Open with how the piece is used, then dimensions, materials, and care. Help the shopper picture it in their space without overselling. Always mention assembly, delivery, and weight, since those drive returns.`
