---
title: 구매요청 목록 최대값 구성
description: 각 고객 계정에 대해 유지 관리할 수 있는 최대 수를 제어하는 구매요청 목록 구성에 대해 알아봅니다.
exl-id: a36dda0e-c00f-4182-9046-717b9d811f71
feature: B2B, Companies, Configuration
role: Admin
source-git-commit: 03d1892799ca5021aad5c19fc9f2bb4f5da87c76
workflow-type: tm+mt
source-wordcount: '214'
ht-degree: 0%

---

# 구매요청 목록 최대값 구성

구매요청 목록 기능을 사용할 경우, 고객은 자주 구매하는 품목의 여러 목록을 생성하고 이러한 목록을 주문 배치에 사용할 수 있습니다. 로그인한 사용자와 게스트 모두가 사용할 수 있습니다. [B2B 기능을 구성](enable-basic-features.md)할 때 구매요청 목록을 활성화할 수 있습니다.

고객은 다양한 공급업체, 구매자, 팀, 캠페인 또는 일반적인 워크플로를 간소화하는 기타 모든 제품의 제품에 중점을 두는 여러 목록을 가질 수 있습니다. [구매요청 목록 기능](requisition-lists.md)은(는) 위시리스트와 비슷하지만 다음과 같은 차이점이 있습니다.

- 장바구니에 품목을 보낸 후 구매요청 목록이 지워지지 않습니다. 여러 번 사용할 수 있습니다.
- 구매요청 목록의 사용자 인터페이스는 많은 품목을 표시하기 위해 간결한 뷰를 사용합니다.

기본적으로 고객은 계정에 대해 최대 999개의 구매요청 목록을 유지 관리할 수 있습니다. 그러나 구성을 수정하고 더 낮은 숫자를 지정하여 스토어의 로드를 줄일 수 있습니다.

1. _관리자_ 사이드바에서 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**(으)로 이동합니다.

1. 왼쪽 패널에서 **[!UICONTROL Customers]**&#x200B;을(를) 확장하고 **[!UICONTROL Requisition Lists]**&#x200B;을(를) 선택합니다.

   ![요청 목록 - 일반 설정](./assets/requisition-lists-general.png){width="600" zoomable="yes"}

1. **[!UICONTROL Number of Requisition Lists]**&#x200B;의 경우 각 고객 계정에 대해 유지 관리할 수 있는 최대 구매요청 목록 수를 입력합니다.

   최소 숫자는 `2`이고 최대값은 `999`입니다.

1. 완료되면 **[!UICONTROL Save Config]**&#x200B;을(를) 클릭합니다.
