---
title: 세금 등급
description: 세금 규칙에 사용되는 세금 분류를 구성하는 방법을 알아봅니다.
exl-id: dd867eba-3f1e-45a8-9332-9e668a2092e1
feature: Taxes
source-git-commit: 8b5af316ab1d2e632ed5fc2066974326830ab3f7
workflow-type: tm+mt
source-wordcount: '501'
ht-degree: 0%

---

# 세금 등급

세금 분류는 고객, 제품 및 배송에 지정할 수 있습니다. Commerce는 각 고객의 장바구니를 분석하고, 고객의 계층과 장바구니 내 상품의 계층 및 지역에 따라 적절한 세금을 산출한다. 지역은 고객의 배송 주소, 청구 주소 또는 배송 출처에 따라 결정됩니다. 다음과 같은 경우 새 세금 분류를 생성할 수 있습니다. [세금 규칙](tax-rules.md) 이(가) 정의되었습니다.

- **고객** — 필요한 수만큼 고객 세금 분류를 생성하여 다음 위치에 지정할 수 있습니다. [고객 그룹](../customers/customer-groups.md). 예를 들어, 일부 관할권에서 도매 거래는 과세되지 않지만 소매 거래는 과세된다. 도매 고객 그룹의 구성원을 도매 세금 분류와 연관시킬 수 있습니다.

- **제품** — 제품 등급은 장바구니에 적용되는 정확한 세율을 결정하는 계산에 사용됩니다. 제품을 생성할 때 특정 세금 분류에 지정됩니다. 예를 들어, 식품에 대해 세금을 부과하지 않거나 다른 세율로 과세할 수 있습니다.

- **배송** — 상점에서 배송에 대해 추가 세금을 부과하는 경우 배송에 대한 특정 제품 세금 분류를 지정해야 합니다. 그런 다음 구성에서 배송에 사용되는 세금 분류로 지정합니다.

## 세금 분류 구성

운송에 사용되는 세금 분류 및 기본 세금 분류 [제품 및 고객](#add-a-product-tax-class) 다음에 설정됨 _[!UICONTROL Sales]_구성.

1. 다음에서 _관리자_ 사이드바, 이동 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. 왼쪽 패널에서 를 확장합니다. **[!UICONTROL Sales]** 및 선택 **[!UICONTROL Tax]**.

1. 확장 ![확장 선택기](../assets/icon-display-expand.png) 다음 **[!UICONTROL Tax Classes]** 섹션.

   ![구성 - 세금 분류](../configuration-reference/sales/assets/tax-tax-classes.png){width="600" zoomable="yes"}

1. 다음 각각에 대한 세금 분류를 선택합니다.

   - **[!UICONTROL Set Tax Class for Shipping]**
   - **[!UICONTROL Tax Class for Gift Options]**
   - **[!UICONTROL Default Tax Class for Product]**
   - **[!UICONTROL Default Tax Class for Customer]**

1. 완료되면 다음을 클릭하십시오. **[!UICONTROL Save Config]**.

## 세금 분류 추가

고객 및 제품에 대한 세목은 쉽게 추가한 다음 개별 고객 및 제품에 지정하여 세칙에 활용할 수 있다.

1. 다음에서 _관리자_ 사이드바, 이동 **[!UICONTROL Stores]** > _[!UICONTROL Taxes]_>**[!UICONTROL Tax Rules]**.

1. 클릭 **[!UICONTROL Add New Tax Rule]**.

1. 확장 ![확장 선택기](../assets/icon-display-expand.png) 다음 **[!UICONTROL Additional Settings]** 섹션.

   ![새 세금 분류 추가](./assets/tax-class-additional-settings.png){width="600" zoomable="yes"}

1. 아래 _고객 세금 분류_, 클릭 **[!UICONTROL Add New Tax Class]**.

1. 다음을 입력합니다. **[!UICONTROL Name]** 텍스트 상자에 있는 새 세금 클래스의 멤버입니다.

   ![새 세금 분류 추가](./assets/tax-class-customer-add-new.png){width="600" zoomable="yes"}

1. 사용 가능한 고객 세금 분류 목록에 새 분류를 추가하려면 확인 표시를 누릅니다.

   ![신규 세금 분류](./assets/tax-classes-updated.png){width="600" zoomable="yes"}

## 제품 세금 분류 추가

1. 아래 _제품 세금 분류_, 클릭 **[!UICONTROL Add New Tax Class]**.

1. 다음을 입력합니다. **[!UICONTROL Name]** 텍스트 상자에 있는 새 세금 클래스의 멤버입니다.

1. 사용 가능한 제품 세금 분류 목록에 새 분류를 추가하려면 확인 표시를 누릅니다.

1. 완료되면 다음을 클릭하십시오. **[!UICONTROL Back]** 단추 모음에서 다음 항목으로 돌아갑니다. _세금 규칙_ 그리드.

## 기본 세금 대상

기본 납세지 설정은 세금 계산의 기반으로 사용되는 국가, 주, 우편 번호를 결정합니다.

**_계산을 위한 기본 세금 대상을 구성하려면_**

1. 다음에서 _관리자_ 사이드바, 이동 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. 왼쪽 패널에서 를 확장합니다. **[!UICONTROL Sales]** 및 선택 **[!UICONTROL Tax]**.

1. 확장 ![확장 선택기](../assets/icon-display-expand.png) 다음 **[!UICONTROL Default Tax Destination Calculation]** 섹션.

   ![기본 세금 대상 계산](../configuration-reference/sales/assets/tax-default-tax-destination-calculation.png){width="600" zoomable="yes"}

1. 설정 **[!UICONTROL Default Country]** 세금 계산의 기반이 되는 국가.

1. 설정 **[!UICONTROL Default State]** (세금 계산의 기초로 사용되는 주 또는 시/도).

1. 설정 **[!UICONTROL Default Post Code]** (지역 세금 계산의 기초로 사용되는 우편 번호)

1. 완료되면 다음을 클릭하십시오. **[!UICONTROL Save Config]**.
