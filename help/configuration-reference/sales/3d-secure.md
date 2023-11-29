---
title: '[!UICONTROL Sales] &gt; [!UICONTROL 3D Secure]'
description: 에서 구성 설정을 검토합니다. [!UICONTROL Sales] &gt; [!UICONTROL 3D Secure] 상거래 관리자의 페이지입니다.
exl-id: 38eb3ee6-8b80-4ba3-afce-8ab82baa76a9
feature: Configuration, Security, Payments
source-git-commit: b710c0368dc765e3bf25e82324bffe7fb8192dbf
workflow-type: tm+mt
source-wordcount: '127'
ht-degree: 0%

---

# [!UICONTROL Sales] > [!UICONTROL 3D Secure]

[!DNL 3-D Secure] 이(가) 개발했습니다. [!DNL Visa] 안전한 온라인 거래를 촉진합니다. 예 [!DNL 3-D Secure] 카드 네트워크에서 만든 솔루션은 [!DNL Visa], [!DNL Mastercard SecureCode], [!DNL American Express SafeKey], 및 [!DNL CardinalCommerce Consumer Authentication]. [!DNL CardinalCommerce] 은(는) 디지털 거래 인증 분야의 글로벌 리더이며 의 완전 소유 자회사입니다. [!DNL Visa].

[!DNL 3-D Secure] 버전 2.0은 고급 인증 방법 및 인증 흐름, 판매자와 발행자 간의 향상된 데이터 공유 등 다양한 개선 사항을 지원합니다.

>[!NOTE]
>
>다음 [Braintree](../../stores-purchase/braintree.md) 결제 게이트웨이도 [!DNL 3-D Secure] 확인.

{{config}}

## [!UICONTROL CardinalCommerce]

![CardinalCommerce](./assets/3d-secure-cardinalcommerce.png)<!-- zoom -->

| 필드 | [범위](../../getting-started/websites-stores-views.md#scope-settings) | 설명 |
|--- |--- |--- |
| [!UICONTROL Environment] | 웹 사이트 | 의 작동 모드를 나타냅니다. [!DNL CardinalCommerce] 계정입니다. 테스트 환경에서 실행하는 경우 &#39;샌드박스&#39;를 선택합니다. 옵션: 샌드박스 / 프로덕션(기본값) |
| [!UICONTROL Org Unit ID] | 웹 사이트 | 의 조직 단위 ID [!DNL CardinalCommerce] 판매자 계정. |
| [!UICONTROL API Key] | 웹 사이트 | 의 API 키 [!DNL CardinalCommerce] 판매자 계정. |
| [!UICONTROL API Identifier] | 웹 사이트 | 의 API 식별자 [!DNL CardinalCommerce] 판매자 계정. |
| [!UICONTROL Debug] | 웹 사이트 | 옵션: `Yes` / `No` |

{style="table-layout:auto"}
