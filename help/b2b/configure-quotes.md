---
title: 따옴표 구성
description: 견적 요청, 견적 수명 및 첨부 파일에 대한 최소 필요 주문 금액을 제어하는 견적 구성에 대해 알아봅니다.
exl-id: 865f6624-df9b-4f78-abfa-1f9a3d82bc0d
feature: B2B, Companies, Configuration, Quotes
role: Admin
TQID: https://experienceleague.adobe.com/RenH7-cnfF8qVEqFQc7IPMVsIp0alug5OgvYlr5piTM
product_v2: id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2: id: bd989d82-1e15-4534-88db-f1f51dd77ffaid: dac87252-6066-4d6e-a9d2-f6d84c323de7
subfeature_v2: id: f56d26ed-050b-4fb7-b29b-8e6e994e80a2
role_v2: id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
level_v2: id: b5a62a22-46f7-4f0d-b151-3fc640bef588id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2: id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 296
ht-degree: 0%

---

# 따옴표 구성

일반 [B2B 기능](enable-basic-features.md)에서 인용 부호가 활성화된 경우 관리자에서 인용 부호에 대한 지원을 구성할 수 있습니다. Quote 구성에 따라 Quote 요청에 필요한 최소 주문 금액, Quote Lifetime 및 첨부 파일의 지원되는 파일 형식이 결정됩니다.

>[!NOTE]
>
>견적 구성 옵션 및 견적 협상 기능을 사용하는 기능은 [역할 리소스](../systems/permissions-user-roles.md#role-resources)를 사용하여 제어됩니다. 관리자 사용자 계정에 할당된 관리자 사용자 역할에 대해 이러한 역할 리소스를 선택해야 합니다. 관리자의 견적 함수에 대한 액세스 권한을 부여하려면 **[!UICONTROL System]** > _[!UICONTROL Permissions]_>**[!UICONTROL User Roles]**(으)로 이동하고 역할을 선택한 다음_&#x200B;역할 리소스&#x200B;_트리에서 [!UICONTROL Sales] > [!UICONTROL Operations] > [!UICONTROL Quotes]&#x200B;(으)로 이동합니다.

1. _관리자_ 사이드바에서 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**(으)로 이동합니다.

1. 왼쪽 패널에서 **[!UICONTROL Sales]**&#x200B;을(를) 확장하고 **[!UICONTROL Quotes]**&#x200B;을(를) 선택합니다.

1. **[!UICONTROL General]** 섹션에서 ![확장 선택기](../assets/icon-display-expand.png)를 확장하고 다음을 수행합니다.

   ![영업 견적 구성 - 일반](./assets/quotes-general.png){width="700" zoomable="yes"}

   Quotes 기능 옵션 및 함수의 전체 목록은 _구성 참조_&#x200B;의 [Quotes](../configuration-reference/sales/quotes.md)를 참조하십시오.

   - 견적에 대한 요청을 제출하기 전에 충족해야 하는 장바구니에 **[!UICONTROL Minimum Amount]**&#x200B;을(를) 입력하십시오.

   - **[!UICONTROL Minimum Amount Message]**&#x200B;의 경우 장바구니 합계가 최소 필요 금액을 충족하지 않을 때 표시할 메시지를 입력하십시오.

   - **[!UICONTROL Default Expiration Period]**&#x200B;에 견적이 유효한 **[!UICONTROL days]**, **[!UICONTROL weeks]** 또는 **[!UICONTROL months]**&#x200B;의 수를 입력하십시오.

1. **[!UICONTROL Attached files]** 섹션에서 ![확장 선택기](../assets/icon-display-expand.png)를 확장하고 다음을 수행합니다.

   - **[!UICONTROL File formats for upload]**&#x200B;에 견적에 첨부된 파일에 대해 지원하는 각 파일 형식의 접미사를 입력합니다.

     각 파일 접미사를 소문자로 입력하고 쉼표로 구분합니다.

     기본적으로 `doc`, `docx`, `xls`, `xlsx`, `pdf`, `txt`, `jpg`, `png` 및 `jpeg` 형식이 지원됩니다.

   - **[!UICONTROL Maximum file size]**&#x200B;의 경우 첨부된 파일의 최대 크기(MB)를 입력하십시오.

     입력한 값이 서버 설정에 의해 재정의될 수 있습니다.

     ![판매 견적 구성 - 첨부 파일](./assets/quotes-attached-files.png){width="600" zoomable="yes"}

1. 완료되면 **[!UICONTROL Save Config]**&#x200B;을(를) 클릭합니다.
