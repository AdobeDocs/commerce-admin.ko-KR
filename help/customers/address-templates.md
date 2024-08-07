---
title: 고객 주소 템플릿
description: 고객 주소 템플릿을 사용자 지정하는 방법을 알아봅니다.
exl-id: 9fd32c0a-ff9a-47f9-84e2-f5d6bf307d8c
feature: Customers, Configuration
source-git-commit: 7de285d4cd1e25ec890f1efff9ea7bdf2f0a9144
workflow-type: tm+mt
source-wordcount: '146'
ht-degree: 0%

---

# 고객 주소 템플릿

{{ee-feature}}

인쇄된 송장, 선적 및 환불과 고객 계정의 주소 장부에 나타나는 고객 청구 및 운송 주소의 형식을 제어하는 템플리트를 수정할 수 있습니다. 추가 정보를 포함하려면 고객 계정 및 [주소](address-attributes.md)와 연결된 [사용자 지정 특성](attribute-properties.md)을(를) 만들어 템플릿에 통합할 수 있습니다.

## 예 1: 간단한 형식

[!UICONTROL Text One Line] 주소 템플릿의 경우:

```text
{{depend prefix}}{{var prefix}} {{/depend}}{{var firstname}} {{depend middlename}}{{var middlename}} {{/depend}}{{var lastname}}{{depend suffix}} {{var suffix}}{{/depend}}, {{var street}}, {{var city}}, {{var region}} {{var postcode}}, {{var country}}
```

## 예제 2: long 형식

[!UICONTROL Text], [!UICONTROL HTML] 및 [!UICONTROL PDF] 주소 템플릿의 경우:

```text
{{depend prefix}}{{var prefix}} {{/depend}}{{var firstname}} {{depend middlename}}{{var middlename}} {{/depend}}{{var lastname}}{{depend suffix}} {{var suffix}}{{/depend}}{{depend company}}{{var company}}{{/depend}}{{if street1}}{{var street1}}{{/if}}{{depend street2}}{{var street2}}{{/depend}}{{depend street3}}{{var street3}}{{/depend}}{{depend street4}}{{var street4}}{{/depend}}{{if city}}{{var city}},  {{/if}}{{if region}}{{var region}}, {{/if}}{{if postcode}}{{var postcode}}{{/if}}{{var country}}{{depend telephone}}T: {{var telephone}}{{/depend}}{{depend fax}}F: {{var fax}}{{/depend}}{{depend vat_id}}VAT: {{var vat_id}}{{/depend}}
```

![고객 주소 템플릿](../configuration-reference/customers/assets/customer-configuration-address-templates.png){width="600" zoomable="yes"}

## 주소 필드 순서 변경

1. _관리자_ 사이드바에서 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**(으)로 이동합니다.

1. 왼쪽 패널에서 **[!UICONTROL Customers]**&#x200B;을(를) 확장하고 **[!UICONTROL Customer Configuration]**&#x200B;을(를) 선택합니다.

1. **[!UICONTROL Address Templates]** 섹션을 확장하려면 클릭하십시오.

   섹션에는 다음 각 항목에 대한 별도의 서식 지정 지침 세트가 포함되어 있습니다.

   - [!UICONTROL Text]
   - [!UICONTROL Text One Line]
   - [!UICONTROL HTML]
   - [!UICONTROL PDF]

1. 참조에 대한 예를 사용하여 필요에 따라 각 템플릿을 편집합니다.

1. 완료되면 **[!UICONTROL Save Config]**&#x200B;을(를) 클릭합니다.
