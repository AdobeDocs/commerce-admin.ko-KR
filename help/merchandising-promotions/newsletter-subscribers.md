---
title: 뉴스레터 구독자 관리
description: 간단한 활성 구독 목록을 사용하여 뉴스레터 구독자를 관리하는 방법을 알아봅니다.
exl-id: c7e8e642-e3fd-4979-9ea3-2d96839730b2
feature: Customers, Communications
source-git-commit: eb0fe395020dbe2e2496aba13d2f5c2bf2d0fc27
workflow-type: tm+mt
source-wordcount: '499'
ht-degree: 0%

---

# 뉴스레터 구독자 관리

구독 목록을 정기적으로 관리하고 구독 취소 요청을 처리하는 것이 좋습니다. 일부 관할권에서는 특정 기간 내에 가입 해지 요청을 처리하는 것이 법률상 요구된다.

간단한 활성 구독 목록을 사용하여 구독자를 쉽게 관리할 수 있습니다. 고객이 구독 취소 요청을 제출하면 선택한 하나 이상의 구독에 _구독 취소_ 액션을 적용할 수 있습니다.

여러 스토어 보기가 있는 단일 사이트 설정에서 고객 계정 구독은 특정 스토어 보기와 연결될 수 있습니다.

글로벌 [고객 계정 범위](../customers/customer-account-scope.md)가 있는 다중 스토어 및 다중 사이트 설정에서 고객 계정은 여러 사이트/스토어의 뉴스레터를 구독할 수 있습니다. 이 경우 고객 계정을 편집하여 구독 그룹을 관리하거나 특정 사이트/스토어에 대한 구독을 취소하여 요청을 수락할 수 있습니다.

서드파티 서비스를 사용하여 뉴스레터를 전송하려면 구독 목록을 CSV 또는 XML 파일로 내보낼 수 있습니다.

## 고객에 대한 구독 관리

1. _관리자_ 사이드바에서 **[!UICONTROL Customers]** > **[!UICONTROL All Customers]**(으)로 이동합니다.

1. 그리드에서 고객을 찾고 _[!UICONTROL Action]_열에서&#x200B;**[!UICONTROL Edit]**을(를) 클릭합니다.

1. 왼쪽 패널에서 **[!UICONTROL Newsletter]**&#x200B;을(를) 클릭합니다.

1. 사이트/스토어 설정에 따라 고객에 대한 구독을 수정합니다.

   단일 사이트/단일 저장소 설정의 경우 **[!UICONTROL Subscribed to Newsletter]** 확인란을 선택하거나 선택을 취소할 수 있습니다.

   ![단일 스토어 고객 뉴스레터 구독 확인란](./assets/newsletter-customer-single-store.png){width="500" zoomable="yes"}

   단일 사이트/다중 스토어 설정의 경우 **[!UICONTROL Subscribed to Newsletter]** 확인란을 선택하거나 선택을 취소하고 **[!UICONTROL Subscribed on Store View]**&#x200B;을(를) 구독에 대한 올바른 스토어 보기로 설정할 수 있습니다.

   ![다중 스토어 고객 뉴스레터 구독 확인란 및 스토어 보기 선택기](./assets/newsletter-customer-multi-store.png){width="500" zoomable="yes"}

   글로벌 고객 계정 범위를 사용하는 다중 사이트/다중 스토어 설정의 경우 페이지에 모든 사이트에 대한 구독 상태가 표시됩니다. **[!UICONTROL Subscribed]** 확인란을 선택 또는 선택 취소하거나 구독의 **[!UICONTROL Store View]**&#x200B;을(를) 변경할 수 있습니다.

   ![다중 사이트 고객 뉴스레터 구독 확인란 및 스토어 보기 선택기](./assets/newsletter-customer-multi-site.png){width="500" zoomable="yes"}

1. **[!UICONTROL Save Customer]**&#x200B;을(를) 클릭합니다.

## 구독자 목록에서 구독 취소

1. _관리자_ 사이드바에서 **[!UICONTROL Marketing]** > _[!UICONTROL Communications]_>**[!UICONTROL Newsletter Subscribers]**(으)로 이동합니다.

   일부 고객이 둘 이상의 사이트에 대한 구독을 갖는 다중 사이트 설정의 경우 각 구독이 그리드에 라인 항목으로 표시됩니다.

1. 그리드에서 가입자를 찾은 다음 첫 번째 열에서 확인란을 선택합니다.

   >[!NOTE]
   >
   >일괄 가입을 해지하려면 취소할 각 가입자의 확인란을 선택합니다.

1. _[!UICONTROL Action]_컨트롤을&#x200B;**[!UICONTROL Unsubscribe]**(으)로 설정하고&#x200B;**[!UICONTROL Submit]**을(를) 클릭합니다.

   ![뉴스레터 구독 취소](./assets/newsletter-unsubscribe.png){width="600" zoomable="yes"}

   레코드의 상태가 `Unsubscribed`(으)로 변경됩니다.

## 구독자 목록 내보내기

1. _[!UICONTROL Newsletter Subscribers]_목록에서 필터 컨트롤을 사용하여_&#x200B;상태&#x200B;_가 `Subscribed`인 레코드와 적절한 웹 사이트, 스토어 또는 스토어 보기에 대한 레코드만 포함합니다.

1. **[!UICONTROL Export to]** 컨트롤을 다음 중 하나로 설정합니다.

   - `CSV`
   - `XML`

1. **[!UICONTROL Export]**&#x200B;을(를) 클릭하고 화면 아래쪽에서 프롬프트를 찾아 파일을 저장합니다.

   ![뉴스레터 구독자 내보내기](./assets/newsletter-subscribers-export.png){width="600" zoomable="yes"}

## 구독자 목록에서 구독자를 삭제합니다.

1. _관리자_ 사이드바에서 **[!UICONTROL Marketing]** > _[!UICONTROL Communications]_>**[!UICONTROL Newsletter Subscribers]**(으)로 이동합니다.

1. 그리드에서 가입자를 찾은 다음 첫 번째 열에서 확인란을 선택합니다.

1. _[!UICONTROL Action]_컨트롤을&#x200B;**[!UICONTROL Delete]**(으)로 설정하고&#x200B;**[!UICONTROL Submit]**을(를) 클릭합니다.

1. 확인 메시지가 표시되면 **[!UICONTROL OK]**&#x200B;을(를) 클릭합니다.
