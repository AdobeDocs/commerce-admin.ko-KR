---
title: 고객 세그먼트 보고서
description: 고객 세그먼트 보고서 는 각 세그먼트의 고객 수에 대한 정보를 제공합니다.
exl-id: a767ee80-7b6e-4acd-9772-2f8adcf3233e
TQID: https://experienceleague.adobe.com/asBYmrf5lkWyfH6xf8o-OxZwK25rr4okrtsyON3Fv1s
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2:
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 247
ht-degree: 0%

---

# 고객 세그먼트 보고서

{{ee-feature}}

고객 세그먼트 보고서는 각 세그먼트의 고객 수에 대한 정보를 제공합니다.

![고객 세그먼트 보고서](assets/customer-segments-reports.png){width="700" zoomable="yes"}

| 열 | 설명 |
|--- |--- |
| **[!UICONTROL Select]** | 작업의 대상이 될 각 세그먼트에 대한 확인란을 선택하거나 열 머리글에서 선택 컨트롤을 사용합니다. 옵션: `Select All` / `Deselect All` / `Select Visible` / `Unselect Visible` |
| **[!UICONTROL ID]** | 각 세그먼트에 할당된 고유 숫자 식별자 |
| **[!UICONTROL Segment]** | 세그먼트 이름 |
| **[!UICONTROL Status]** | 세그먼트 상태. 옵션: `Active` / `Inactive` |
| **[!UICONTROL Website]** | 세그먼트가 할당된 웹 사이트 |
| **[!UICONTROL Customers]** | 세그먼트에 할당된 고객 수 |

{style="table-layout:auto"}

세그먼트의 고객 목록으로 드릴다운하여 데이터를 내보낼 수 있습니다.

![고객 데이터로 드릴다운](assets/customer-segment-drilldown.png){width="600" zoomable="yes"}

최신 데이터를 확보하려면 세그먼트 데이터를 새로 고쳐야 합니다. 세그먼트 데이터를 사용할 수 없거나 오래된 경우 단추 모음에서 **[!UICONTROL Refresh Segment Data]**&#x200B;을(를) 클릭하여 업데이트합니다.

1. **[!UICONTROL Export to]**&#x200B;의 경우 내보내기 형식을 선택하십시오.

   * CSV - 일반 텍스트 데이터를 포함하는 쉼표로 구분된 값 파일입니다.
   * Excel XML - XML 기반의 스프레드시트 데이터 형식입니다.

1. **[!UICONTROL Export]**&#x200B;을(를) 클릭합니다.

   | 열 | 설명 |
   |--- |--- |
   | **[!UICONTROL ID]** | 각 사용자에게 할당된 고유 숫자 식별자입니다 |
   | **[!UICONTROL Name]** | 고객 이름 |
   | **[!UICONTROL Email]** | 등록된 고객의 이메일 주소 |
   | **[!UICONTROL Group]** | 고객이 할당된 고객 그룹 |
   | **[!UICONTROL Phone]** | 고객 전화번호 |
   | **[!UICONTROL ZIP]** | 고객이 있는 우편 번호 |
   | **[!UICONTROL Country]** | 고객이 있는 국가 |
   | **[!UICONTROL State/Province]** | 고객이 위치한 주 또는 시/도 |
   | **[!UICONTROL Customer Since]** | 고객 계정이 생성된 날짜와 시간 |

   {style="table-layout:auto"}

1. 생성된 파일은 로컬 컴퓨터에 자동으로 저장됩니다.
