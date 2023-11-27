---
title: 따옴표 구성
description: 견적 요청, 견적 수명 및 첨부 파일에 대한 최소 필요 주문 금액을 제어하는 견적 구성에 대해 알아봅니다.
exl-id: 865f6624-df9b-4f78-abfa-1f9a3d82bc0d
feature: B2B, Companies, Configuration, Quotes
role: Admin
source-git-commit: d4c3ea4b49e30ae3af249516d32fb28437d218b8
workflow-type: tm+mt
source-wordcount: '297'
ht-degree: 0%

---

# 따옴표 구성

일반에서 견적이 활성화된 경우 [B2B 기능](enable-basic-features.md), 관리에서 따옴표에 대한 지원을 구성할 수 있습니다. Quote 구성에 따라 Quote 요청에 필요한 최소 주문 금액, Quote Lifetime 및 첨부 파일의 지원되는 파일 형식이 결정됩니다.

>[!NOTE]
>
>견적 구성 옵션 및 견적 협상 기능을 사용하는 기능은 다음을 사용하여 제어됩니다. [역할 리소스](../systems/permissions-user-roles.md#role-resources). 관리자 사용자 계정에 할당된 관리자 사용자 역할에 대해 이러한 역할 리소스를 선택해야 합니다. 관리자의 견적 기능에 대한 액세스 권한을 부여하려면 **[!UICONTROL System]** > _[!UICONTROL Permissions]_>**[!UICONTROL User Roles]**, 역할을 선택하고 다음 위치로 이동합니다. [!UICONTROL Sales] > [!UICONTROL Operations] > [!UICONTROL Quotes] 다음에서_&#x200B;역할 리소스&#x200B;_트리.

1. 다음에서 _관리자_ 사이드바, 이동 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. 왼쪽 패널에서 를 확장합니다. **[!UICONTROL Sales]** 및 선택 **[!UICONTROL Quotes]**.

1. 확장 ![확장 선택기](../assets/icon-display-expand.png) 다음 **[!UICONTROL General]** 섹션을 참조하고 다음을 수행합니다.

   ![영업 견적 구성 - 일반](./assets/quotes-general.png){width="700" zoomable="yes"}

   다음을 참조하십시오 [따옴표](../configuration-reference/sales/quotes.md) 다음에서 _구성 참조_ 따옴표 기능 옵션 및 해당 기능의 전체 목록을 보려면 다음을 수행하십시오.

   - 다음을 입력합니다. **[!UICONTROL Minimum Amount]** 견적 요청을 제출하기 전에 충족해야 하는 장바구니에서.

   - 대상 **[!UICONTROL Minimum Amount Message]**&#x200B;장바구니 합계가 최소 필요 금액을 충족하지 않을 때 표시할 메시지를 입력합니다.

   - 대상 **[!UICONTROL Default Expiration Period]**, 숫자를 입력합니다. **[!UICONTROL days]**, **[!UICONTROL weeks]**, 또는 **[!UICONTROL months]** 유효한 견적을 유지합니다.

1. 확장 ![확장 선택기](../assets/icon-display-expand.png) 다음 **[!UICONTROL Attached files]** 섹션을 참조하고 다음을 수행합니다.

   - 대상 **[!UICONTROL File formats for upload]**&#x200B;견적에 첨부된 파일에 대해 지원하는 각 파일 유형의 접미사를 입력합니다.

     각 파일 접미사를 소문자로 입력하고 쉼표로 구분합니다.

     기본적으로 다음 형식이 지원됩니다. `doc`, `docx`, `xls`, `xlsx`, `pdf`, `txt`, `jpg`, `png`, 및 `jpeg`

   - 대상 **[!UICONTROL Maximum file size]**&#x200B;에 첨부된 파일의 최대 크기를 입력합니다(MB).

     입력한 값이 서버 설정에 의해 재정의될 수 있습니다.

     ![영업 견적 구성 - 첨부 파일](./assets/quotes-attached-files.png){width="600" zoomable="yes"}

1. 완료되면 다음을 클릭하십시오. **[!UICONTROL Save Config]**.
