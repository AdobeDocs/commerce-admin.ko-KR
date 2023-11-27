---
title: 고객 주소 템플릿
description: 고객 주소 템플릿을 사용자 지정하는 방법을 알아봅니다.
exl-id: 9fd32c0a-ff9a-47f9-84e2-f5d6bf307d8c
feature: Customers, Configuration
source-git-commit: 7de285d4cd1e25ec890f1efff9ea7bdf2f0a9144
workflow-type: tm+mt
source-wordcount: '144'
ht-degree: 0%

---

# 고객 주소 템플릿

{{ee-feature}}

인쇄된 송장, 선적 및 환불과 고객 계정의 주소 장부에 나타나는 고객 청구 및 운송 주소의 형식을 제어하는 템플리트를 수정할 수 있습니다. 추가 정보를 포함하려면 다음을 만들 수 있습니다. [사용자 지정 속성](attribute-properties.md) 고객 계정 및 과(와) 연결된 [주소](address-attributes.md)을 클릭하고 템플릿에 통합합니다.

## 예 1: 간단한 형식

대상 [!UICONTROL Text One Line] 주소 템플릿:

```text
{{depend prefix}}{{var prefix}} {{/depend}}{{var firstname}} {{depend middlename}}{{var middlename}} {{/depend}}{{var lastname}}{{depend suffix}} {{var suffix}}{{/depend}}, {{var street}}, {{var city}}, {{var region}} {{var postcode}}, {{var country}}
```

## 예제 2: long 형식

대상 [!UICONTROL Text], [!UICONTROL HTML], 및 [!UICONTROL PDF] 주소 템플릿:

```text
{{depend prefix}}{{var prefix}} {{/depend}}{{var firstname}} {{depend middlename}}{{var middlename}} {{/depend}}{{var lastname}}{{depend suffix}} {{var suffix}}{{/depend}}{{depend company}}{{var company}}{{/depend}}{{if street1}}{{var street1}}{{/if}}{{depend street2}}{{var street2}}{{/depend}}{{depend street3}}{{var street3}}{{/depend}}{{depend street4}}{{var street4}}{{/depend}}{{if city}}{{var city}},  {{/if}}{{if region}}{{var region}}, {{/if}}{{if postcode}}{{var postcode}}{{/if}}{{var country}}{{depend telephone}}T: {{var telephone}}{{/depend}}{{depend fax}}F: {{var fax}}{{/depend}}{{depend vat_id}}VAT: {{var vat_id}}{{/depend}}
```

![고객 주소 템플릿](../configuration-reference/customers/assets/customer-configuration-address-templates.png){width="600" zoomable="yes"}

## 주소 필드 순서 변경

1. 다음에서 _관리자_ 사이드바, 이동 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. 왼쪽 패널에서 를 확장합니다. **[!UICONTROL Customers]** 및 선택 **[!UICONTROL Customer Configuration]**.

1. 를 클릭하여 확장합니다. **[!UICONTROL Address Templates]** 섹션.

   섹션에는 다음 각 항목에 대한 별도의 서식 지정 지침 세트가 포함되어 있습니다.

   - [!UICONTROL Text]
   - [!UICONTROL Text One Line]
   - [!UICONTROL HTML]
   - [!UICONTROL PDF]

1. 참조에 대한 예를 사용하여 필요에 따라 각 템플릿을 편집합니다.

1. 완료되면 다음을 클릭하십시오. **[!UICONTROL Save Config]**.
