---
title: 뉴스레터 큐
description: 여러 뉴스레터 일괄 처리를 전송하기 위한 뉴스레터 대기열을 관리하는 방법을 알아봅니다.
exl-id: bf85b3ff-3093-49a1-8a9a-d3ea71fe3f09
feature: Customers, Communications
source-git-commit: eb0fe395020dbe2e2496aba13d2f5c2bf2d0fc27
workflow-type: tm+mt
source-wordcount: '342'
ht-degree: 0%

---

# 뉴스레터 큐

서버의 로드를 관리하기 위해 구독자가 많은 뉴스레터가 여러 배치의 대기열로 전송됩니다. 뉴스레터 큐를 정기적으로 확인하여 상태를 확인하고 처리된 메시지 수를 볼 수 있습니다. 전송 중에 발생하는 모든 문제는 _뉴스레터 문제_ 보고서에 나타납니다.

## 뉴스레터 전송

1. _관리자_ 메뉴에서 **[!UICONTROL Marketing]** > _[!UICONTROL Communications]_>**[!UICONTROL Newsletter Template]**(으)로 이동합니다.

1. 그리드에서 전송할 [뉴스레터 템플릿](newsletter-template.md)을(를) 찾아 **[!UICONTROL Action]** 열을 `Queue Newsletter`(으)로 설정합니다.

1. **[!UICONTROL Queue Date Start]**&#x200B;의 경우 달력(![달력 아이콘](../assets/icon-calendar.png))에서 전송을 시작할 날짜를 선택하십시오.

1. **[!UICONTROL Subscribers From]**&#x200B;의 경우 전자 메일 전달에 포함할 각 스토어 보기를 선택하십시오.

1. 이메일 헤더 정보를 작성합니다.

   - 전자 메일 헤더의 **[!UICONTROL Subject]** 줄에 대한 뉴스레터에 대한 간략한 설명을 입력하십시오.

   - **[!UICONTROL Sender Name]** 입력.

   - **[!UICONTROL Sender Email]**&#x200B;의 경우 보낸 사람의 전자 메일 주소를 입력하십시오.

     발신자의 기본 이름과 이메일 주소는 구성에 지정됩니다.

     ![뉴스레터 큐 정보](./assets/newsletter-queue-information1.png){width="600" zoomable="yes"}

1. 해당되는 경우 가입을 해지하는 지침 위의 **[!UICONTROL Message]** 상자에 메모를 입력하십시오.

   >[!NOTE]
   >
   >많은 관할권에서 법에 따라 요구되는 지침을 제거하지 마십시오.

1. 뉴스레터에 사용자 지정 스타일을 적용하려면 해당 스타일을 **[!UICONTROL Newsletter Styles]** 필드에 추가하십시오.

1. 완료되면 **[!UICONTROL Save and Resume]**&#x200B;을(를) 클릭합니다.

   뉴스레터가 처리 대기 중인 큐에 나타납니다.

## 문제 확인

_관리자_ 메뉴에서 **[!UICONTROL Reports]** > _[!UICONTROL Marketing]_>**[!UICONTROL Newsletter Problem Reports]**(으)로 이동합니다.

## 단추 막대

| 단추 | 설명 |
|--- |--- |
| **[!UICONTROL Back]** | 변경 사항을 저장하지 않고 뉴스레터 템플릿 페이지로 돌아갑니다. |
| **[!UICONTROL Reset]** | 대기열 정보 양식의 저장되지 않은 변경 사항을 이전 값으로 재설정합니다. |
| **[!UICONTROL Preview Template]** | 별도의 탭에서 미리보기 페이지를 엽니다. |
| **[!UICONTROL Save and Resume]** | 변경 사항을 모두 저장합니다. 뉴스레터를 큐에 넣습니다. |
| **[!UICONTROL Save Newsletter]** | 변경 사항을 모두 저장합니다. 뉴스레터를 큐에 넣습니다. |

{style="table-layout:auto"}

## 열

| 열 | 설명 |
|--- |--- |
| [!UICONTROL ID] | 각 뉴스레터 템플릿에 할당된 고유한 숫자 식별자입니다. |
| [!UICONTROL Queue Start] | 뉴스레터가 발송된 날짜. |
| [!UICONTROL Queue End] | 뉴스레터 전송이 완료된 날짜. |
| [!UICONTROL Subject] | 뉴스레터 템플릿의 제목입니다. |
| [!UICONTROL Status] | 뉴스레터 메일링 상태를 나타냅니다. 가능한 값: `Sent`, `Canceled`, `Not Sent`, `Sending` 또는 `Paused`. |
| [!UICONTROL Processed] | 얼마나 많은 뉴스레터가 전송되었는지 나타냅니다. |
| [!UICONTROL Recipients] | 구독자가 받은 뉴스레터 수를 나타냅니다. |
| [!UICONTROL Actions] | **[!UICONTROL Preview]**: 템플릿을 미리 볼 수 있는 별도의 창을 엽니다. |

{style="table-layout:auto"}
