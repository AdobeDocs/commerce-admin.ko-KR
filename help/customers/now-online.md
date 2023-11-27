---
title: 이제 고객이 온라인 상태임
description: 의 _Now Online_ 옵션 [!UICONTROL Customers ]메뉴에는 현재 스토어에 있는 모든 고객과 방문자가 나열됩니다.
exl-id: 69af669d-f9aa-471b-9d62-5657f3fb2103
source-git-commit: c855a691ed33e1e6e74865ebdfb30ddad21ad83e
workflow-type: tm+mt
source-wordcount: '338'
ht-degree: 0%

---

# 이제 고객이 온라인 상태임

다음 **[!UICONTROL Now Online]** 옵션 [!DNL Customers] 메뉴에는 현재 스토어에 있는 모든 고객과 방문자가 나열됩니다. 고객이 현재 온라인으로 표시되는 시간 간격은 구성에 설정되며 [!DNL Customer's] 활동은 책임자로부터 볼 수 있습니다. 기본적으로 간격은 15분입니다. 이 시간 동안 키보드를 사용하지 않으면 세션이 종료되며 고객은 쇼핑을 계속하려면 계정에 다시 로그인해야 합니다. 카트의 콘텐츠는 나중에 액세스할 수 있도록 저장됩니다.

![온라인 고객](assets/customers-now-online.png){width="700" zoomable="yes"}

고객의 온라인 상태는 고객 로그인, 등록 또는 기타 상태 변경 이벤트 시에만 업데이트됩니다. 여기에는 제품 추가, 제거 및 수정과 같은 장바구니 관련 이벤트가 포함됩니다.

>[!NOTE]
>
>페이지 방문만으로는 고객의 온라인 상태가 업데이트되지 않습니다. 이러한 정보를 수집하려면 다음 작업을 수행하는 것이 좋습니다. [Google Analytics 설정](../merchandising-promotions/google-analytics.md) (단독으로 또는 와 함께) [Google 태그 관리자](../merchandising-promotions/google-tag-manager.md))하거나 Adobe Commerce에서 다른 analytics 소프트웨어를 사용하십시오.

## 현재 온라인 상태인 모든 고객 보기

다음에서 _관리자_ 사이드바, 이동 **[!UICONTROL Customers]** > **[!UICONTROL Online Now]**.

>[!TIP]
>
>온라인 고객이 구매를 완료할 수 있도록 지원하는 방법에 대한 자세한 내용은 [쇼핑 지원](../stores-purchase/introduction.md#shopping-assistance).

## 시간 간격 구성

1. 다음에서 _관리자_ 사이드바, 이동 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. 왼쪽 패널에서 를 확장합니다. **[!UICONTROL Customers]** 및 선택 **[!UICONTROL Customer Configuration]**.

1. 확장 **[!UICONTROL Online Customers Options]** 섹션을 참조하고 다음을 수행합니다.

   ![온라인 고객 옵션](../configuration-reference/customers/assets/customer-configuration-online-customers-options.png){width="600" zoomable="yes"}

   - 대상 **[!UICONTROL Online Minutes Interval]**&#x200B;에서 관리자로부터 고객 세션을 표시할 시간(분)을 입력합니다. 기본 간격 15분을 사용하려면 필드를 비워 둡니다.

   - 대상 **[!UICONTROL Customer Data Lifetime]**: 고객이 입력한 저장되지 않은 데이터가 만료될 때까지 걸리는 시간(분)을 입력합니다.

1. 완료되면 다음을 클릭하십시오. **[!UICONTROL Save Config]**.

## 열 설명

| 열 | 설명 |
| --- | --- |
| **[!UICONTROL ID]** | 등록된 고객의 고객 ID입니다. |
| **[!UICONTROL First Name]** | 등록된 고객의 이름. |
| **[!UICONTROL Last Name]** | 등록된 고객의 성. |
| **[!UICONTROL Email]** | 등록된 고객의 이메일 주소입니다. |
| **[!UICONTROL Last Activity]** | 고객이 스토어에서 마지막으로 활동한 날짜 및 시간입니다. |
| **[!UICONTROL Type]** | 옵션: `Customer` / `Visitor` |
| **[!UICONTROL Last URL]** | 고객이 방문한 마지막 URL입니다. |
| **[!UICONTROL Company]** | 사용자가 속한 회사의 이름입니다. |

{style="table-layout:auto"}
