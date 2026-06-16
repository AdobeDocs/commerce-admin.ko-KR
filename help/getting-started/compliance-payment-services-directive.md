---
title: PSD 규정 준수
description: 스토어에 영향을 줄 수 있는 결제 서비스 지침(PSD2)의 요구 사항에 대해 알아봅니다.
exl-id: efe94cac-a170-48df-88cf-36019ca52951
feature: Compliance
TQID: https://experienceleague.adobe.com/paVa-tpYYzrINAPRFs4TOzbp4b4CLJDlxqNlL1gzp2Q
product_v2: id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2: id: b5f00040-57a0-4a6d-a39e-383b1936c2c9id: ba9e5be9-7de1-4f71-a5d2-baead0e425eeid: c32adafa-ed01-4b31-997e-2413013911b0id: dac87252-6066-4d6e-a9d2-f6d84c323de7
subfeature_v2: id: f0ca7b10-ef6c-4ee4-b63f-030819bdd1f3
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: f8a45b24-4be7-4f1b-909b-60d06b483a20
level_v2: id: b5a62a22-46f7-4f0d-b151-3fc640bef588id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2: id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87cid: cc72dcf1-72e1-48cc-b434-e7c27d62d67cid: d095671a-1355-40aa-8b5f-06c33c68080bid: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 396
ht-degree: 0%

---

# PSD 규정 준수

2019년 9월 14일부터 유럽 연합은 EU와 영국의 모든 가맹점에 대해 결제 서비스 지침(PSD2)의 [강력한 고객 인증](https://www.cardinalcommerce.com/content-hub/mandates/psd2-sca/understanding-psd2-sca)&#x200B;(SCA) 요구 사항을 준수하도록 요구합니다. 다른 모든 국가의 상인은 PSD2를 모범 사례로 준수하도록 권장됩니다.

>[!NOTE]
>
>이 항목은 정보 제공 목적으로만 사용되며 법률적인 조언으로 해석되어서는 안 됩니다. 비즈니스가 법적 의무를 준수하는지 여부 및 방법을 결정하려면 법률 고문과 상의하십시오.

강력한 고객 인증은 PSD2의 핵심 구성 요소이며 다음 중 두 가지가 필요합니다.

- 고객에게만 있는 사항(암호 또는 PIN)
- 고객만 알고 있는 사항(전화 또는 키 FOB에 의해 생성된 고유 보안 토큰)
- 고객만 있는 것(지문 또는 안면 인식과 같은 생체 인식 인증)

유럽 은행들은 요건을 충족시키지 못하는 지불을 거절할 수도 있다. 그러나 낮은 위험 및 낮은 가치의 거래는 계속 수락될 수 있으며 이후 지불은 반복 구독에서 이루어집니다.

이 중요한 변경 사항으로 인해 고객 지불이 거부되지 않도록 하기 위해 Adobe에서는 기본 [!DNL Commerce] 결제 통합에 대해 다음 변경 사항과 권장 사항을 도입했습니다.

| 결제 방법 | 규정 준수 요구 사항 |
|--- |--- |
| [PayPal](../stores-purchase/paypal.md) | 대부분의 PayPal 솔루션에서는 요구 사항이 PayPal에 의해 처리되므로 PSD2를 준수하는 데 필요한 조치가 필요하지 않습니다. 특정 솔루션에 대한 자세한 내용은 각 PayPal 항목 맨 위에 있는 메모를 참조하십시오. |
| [Braintree](../stores-purchase/braintree.md) | 2.4.0에서 설치된 확장 기능으로 전환된 것을 시작으로, 요구 사항은 포함된 Braintree 결제 모듈 내에서 처리되며 PSD2를 준수하는 데 필요한 작업은 없습니다. <br /><br />**_참고:_** 이전 릴리스에서 핵심 통합을 사용하여 PSD2를 준수하려면 다음 중 하나를 수행하십시오.<br/>- (권장) [[!DNL Adobe Commerce Marketplace]](https://marketplace.magento.com/catalogsearch/result/?q=braintree#q=braintree&idx=m2_cloud_prod_default_products&p=0&nR%5Bvisibility_search%5D%5B%3D%5D%5B0%5D=1){:target="_blank"}에서 공식 Braintree 결제 통합 확장을 설치합니다.<br/>- [!DNL Commerce] 구성에서 Braintree 결제 방법을 활성화하고 구성합니다.<br/><br/>이러한 이전 핵심 통합은 3D Secure 2.0 확인을 지원합니다. 그러나 JavaScript SDK v2에서 실행되는 Braintree 구현은 3D Secure 2.0을 지원하지 않습니다. |
| 기타 | 다른 모든 결제 통합의 경우 [[!DNL Commerce Marketplace]](https://marketplace.magento.com/extensions/payments-security/payment-integration.html?_ga=2.108129217.2105547619.1564067043-238341041.1564067043){:target="_blank"}에서 사용 가능한 확장을 확인하십시오. 결제 공급자에게 PSD2 요구 사항을 지원하는 솔루션을 추천하도록 요청하십시오. |

{style="table-layout:auto"}
