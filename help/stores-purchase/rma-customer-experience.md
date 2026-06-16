---
title: 상점 경험을 반환합니다.
description: 고객이 상점 내 계정에서 제품 반품을 관리하는 방법을 알아봅니다.
exl-id: c276ca2c-3d8b-4019-a9aa-e7631080f331
feature: Returns, Storefront
TQID: https://experienceleague.adobe.com/erAT7FtUSif5CxrBLlANMQY2aowkv0MDzkqXQnzzF7Q
product_v2: id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2: id: bd989d82-1e15-4534-88db-f1f51dd77ffaid: c1256247-af4b-46d8-9dca-0c654ecfa157id: d1e21356-0064-4f48-9089-16e3f0dbd2a6
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
level_v2: id: b5a62a22-46f7-4f0d-b151-3fc640bef588id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2: id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 208
ht-degree: 0%

---

# 상점 경험을 반환합니다.

{{ee-feature}}

고객은 다음 중 하나를 사용하여 상점에서 RMA를 요청할 수 있습니다.

- 사이드바의 [주문 및 반품 위젯](../content-design/widget-orders-returns.md)
- 바닥글의 _주문 및 반환_ 링크

가장 좋은 방법은 고객 서비스 정책에 RMA 요구 사항 및 프로세스에 대한 설명을 포함하는 것입니다.

>[!NOTE]
>
>반환과 관련된 추가 정보를 수집하려면 사용자 지정 [반환 특성](attributes-returns.md)을(를) 추가할 수 있습니다.

모든 고객 RMA 정보가 고객 계정 대시보드의 **[!UICONTROL My Returns]** 페이지에 표시됩니다.

![내 반환](./assets/my-returns-page.png){width="700" zoomable="yes"}

## RMA 요청

고객이 상점 첫 화면에서 다음 단계를 완료하여 RMA를 제출합니다.

1. 바닥글에서 **[!UICONTROL Orders and Returns]**&#x200B;을(를) 클릭합니다.

1. 주문 정보를 입력합니다.

   - 주문 ID
   - 청구 성
   - 이메일

1. **[!UICONTROL Continue]**&#x200B;을(를) 클릭합니다.

   ![주문 및 반환](./assets/storefront-orders-and-returns.png){width="700" zoomable="yes"}

1. 주문 날짜 아래에서 **[!UICONTROL Return]**&#x200B;을(를) 클릭합니다.

   ![주문 세부 정보](./assets/storefront-orders-and-returns-order-information.png){width="700" zoomable="yes"}

1. 반환할 항목을 선택하고 **[!UICONTROL Quantity to Return]**&#x200B;을(를) 입력합니다.

1. **[!UICONTROL Resolution]**&#x200B;을(를) 다음 중 하나로 설정합니다.

   - Exchange
   - [환불](../customers/refunds-customer-account.md)
   - [스토어 크레딧](../customers/store-credit-using.md)

1. **[!UICONTROL Item Condition]**&#x200B;을(를) 다음 중 하나로 설정합니다.

   - `Unopened`
   - `Opened`
   - `Damaged`

1. **[!UICONTROL Reason to Return]**&#x200B;을(를) 다음 중 하나로 설정합니다.

   - `Wrong Color`
   - `Wrong Size`
   - `Out of Service`
   - `Other`

   ![새 반환 만들기](./assets/storefront-orders-and-returns-create-new-return.png){width="700" zoomable="yes"}

1. 필요한 경우 **[!UICONTROL Contact Email Address]** 및 **[!UICONTROL Comments]**&#x200B;을(를) 설정합니다.

   >[!NOTE]
   >
   >주문에 여러 항목이 포함되어 있고 고객이 다른 항목을 반환하려는 경우 **[!UICONTROL Add Item To Return]**&#x200B;을(를) 클릭하고 항목을 선택한 다음 언급된 모든 옵션을 설정할 수 있습니다.

1. **[!UICONTROL Submit]**&#x200B;을(를) 클릭합니다.
