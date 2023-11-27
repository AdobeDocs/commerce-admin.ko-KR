---
title: 속성을 반환합니다.
description: 반환 특성과 스토어에서 반환을 처리하는 데 필요한 특성을 만드는 방법에 대해 알아봅니다.
exl-id: 639c1e94-1211-4a4e-8599-e54ed99b2355
feature: Attributes, Returns
source-git-commit: 8b5af316ab1d2e632ed5fc2066974326830ab3f7
workflow-type: tm+mt
source-wordcount: '305'
ht-degree: 0%

---

# 속성을 반환합니다.

{{ee-feature}}

반환 특성은 제품 반환 프로세스 중에 필요한 정보를 저장하는 데 사용됩니다. 기본 속성에는 반환된 제품의 상태, 반환 이유 및 반환이 해결된 방법을 나타내는 필드가 포함됩니다. 반환 속성을 만드는 프로세스는 를 만드는 것과 유사합니다 [고객 속성](../customers/attribute-properties.md).

![Admin - 속성을 반환합니다.](./assets/attribute-returns.png){width="700" zoomable="yes"}

## 반환 속성 만들기

1. 다음에서 _관리자_ 사이드바, 이동 **[!UICONTROL Stores]** > _[!UICONTROL Attributes]_>**[!UICONTROL Returns]**.

1. 오른쪽 위 모서리에서 을(를) 클릭합니다. **[!UICONTROL Add New Attribute]**.

   ![새 반환 - 속성 속성](./assets/attribute-returns-new-properties.png){width="600" zoomable="yes"}

### 속성 정의

1. 데이터 입력 중에 속성을 식별하려면 **[!UICONTROL Default Label]**.

1. 대상 **[!UICONTROL Attribute Code]**&#x200B;시스템 내에서 속성을 식별하는 코드를 입력합니다.

1. 데이터 입력에 사용되는 입력 컨트롤의 유형을 확인하려면 다음을 설정하십시오. **[!UICONTROL Input Type]** 다음 중 하나를 수행합니다.

   - `Text Field`
   - `Text Area`
   - `Dropdown`
   - `Yes/No`
   - `File`
   - `Image File`

1. 필드를 필수 항목으로 만들려면 다음을 설정하십시오. **[!UICONTROL Values Required]** 끝 `Yes`.

1. 필드에 초기 값을 지정하려면 **[!UICONTROL Default Value]**.

1. 레코드를 저장하기 전에 필드에 입력한 데이터의 정확성을 확인하려면 을(를) 설정합니다. **[!UICONTROL Input Validation]** 다음 중 하나를 수행합니다.

   - `None`
   - `Alphanumeric`
   - `Alphanumeric with Space`
   - `Numeric Only`
   - `Alpha Only`
   - `URL`
   - `Email`

1. 의 경우 `Text Field` 및 `Text Area` 입력 유형을 입력하고 **[!UICONTROL Minimum Text Length]** 및 **[!UICONTROL Maximum Text Length]**.

1. 전처리 필터를 적용하려면 다음을 설정합니다 **[!UICONTROL Input/Output Filter]** 다음 중 하나를 수행합니다.

   - `None`
   - `Strip HTML Tags`
   - `Escape  HTML Entities`

1. 속성을 고객에게 표시하려면 을 설정합니다. **[!UICONTROL Show on Storefront]** 끝 `Yes` 다음에서 _[!UICONTROL Storefront Properties]_섹션.

1. (선택 사항) **[!UICONTROL Sort Order]**&#x200B;을 눌러 페이지의 동일한 부분에서 다른 속성을 기준으로 이 속성이 표시되는 위치를 결정합니다. (`0` = 첫 번째, `1` = 초, `2` = 세 번째 등입니다.)

### 레이블/옵션 관리

1. 왼쪽 패널에서 을 선택합니다 **[!UICONTROL Manage Labels/Options]**.

1. 다음에서 **[!UICONTROL Manage Titles (Size, Color, etc.)]** 섹션에서 각 스토어 보기에 대한 레이블을 입력합니다.

   ![레이블 관리](./assets/return-attributes.png){width="600" zoomable="yes"}

1. 다음과 같은 경우 **[!UICONTROL Input Type]** 속성: `Dropdown`, 의 옵션을 관리합니다. **[!UICONTROL Manage Options (Values of Your Attribute)]** 섹션.

   - 옵션을 추가하려면 **[!UICONTROL Add Option]** 관리자 및 각 스토어 보기에 대한 레이블을 입력합니다.
   - 옵션을 선택한 기본값으로 설정하려면 **[!UICONTROL Is Default]**.
   - 옵션을 제거하려면 **[!UICONTROL Delete]**.

1. 변경 사항을 저장하려면 를 클릭합니다. **[!UICONTROL Save Attribute]**.
