---
title: '[!UICONTROL Sales] > [!UICONTROL 3D Secure]'
description: Commerce 관리자의 [!UICONTROL Sales] > [!UICONTROL 3D Secure] 페이지에서 구성 설정을 검토합니다.
exl-id: 38eb3ee6-8b80-4ba3-afce-8ab82baa76a9
feature: Configuration, Security, Payments
TQID: https://experienceleague.adobe.com/WzxM9ZYbobbC1fWSIph0jv89uXLte6Wzjs5be27eMyU
product_v2: id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2: id: ba9e5be9-7de1-4f71-a5d2-baead0e425eeid: dac87252-6066-4d6e-a9d2-f6d84c323de7
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: ff6a42d2-313e-452e-93a6-792e4fad9ff8
level_v2: id: b5a62a22-46f7-4f0d-b151-3fc640bef588id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2: id: d095671a-1355-40aa-8b5f-06c33c68080bid: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 126
ht-degree: 1%

---

# [!UICONTROL Sales] > [!UICONTROL 3D Secure]

[!DNL 3-D Secure]은(는) 보안 온라인 트랜잭션을 승격하기 위해 [!DNL Visa]에 의해 개발되었습니다. 카드 네트워크에서 만든 [!DNL 3-D Secure] 솔루션의 예는 [!DNL Visa], [!DNL Mastercard SecureCode], [!DNL American Express SafeKey] 및 [!DNL CardinalCommerce Consumer Authentication]에서 확인합니다. [!DNL CardinalCommerce]은(는) 디지털 거래 인증의 글로벌 리더이며 [!DNL Visa]의 완전 자회사입니다.

[!DNL 3-D Secure] 버전 2.0에서는 고급 인증 방법 및 인증 흐름을 비롯한 다양한 개선 사항과 판매자와 발급자 간의 향상된 데이터 공유를 지원합니다.

>[!NOTE]
>
>[Braintree](../../stores-purchase/braintree.md) 결제 게이트웨이도 [!DNL 3-D Secure] 확인을 지원합니다.

{{config}}

## [!UICONTROL CardinalCommerce]

![CardinalCommerce](./assets/3d-secure-cardinalcommerce.png)<!-- zoom -->

| 필드 | [범위](../../getting-started/websites-stores-views.md#scope-settings) | 설명 |
|--- |--- |--- |
| [!UICONTROL Environment] | 웹 사이트 | [!DNL CardinalCommerce] 계정의 운영 모드를 나타냅니다. 테스트 환경에서 실행하는 경우 &#39;샌드박스&#39;를 선택합니다. 옵션: 샌드박스 / 프로덕션(기본값) |
| [!UICONTROL Org Unit ID] | 웹 사이트 | [!DNL CardinalCommerce] 판매자 계정의 조직 단위 ID입니다. |
| [!UICONTROL API Key] | 웹 사이트 | [!DNL CardinalCommerce] 판매자 계정의 API 키. |
| [!UICONTROL API Identifier] | 웹 사이트 | [!DNL CardinalCommerce] 판매자 계정의 API 식별자입니다. |
| [!UICONTROL Debug] | 웹 사이트 | 옵션: `Yes` / `No` |

{style="table-layout:auto"}
