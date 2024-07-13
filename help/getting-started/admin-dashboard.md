---
title: 관리 대시보드
description: 일반적으로 로그인할 때 나타나는 첫 번째 페이지인 관리 대시보드에 대해 알아봅니다.
exl-id: 56957c0a-1618-444b-a37a-ecf0d7b27eae
source-git-commit: 7b6d70e2f3052af69075790cec1f396e2505bf8b
workflow-type: tm+mt
source-wordcount: '715'
ht-degree: 0%

---

# 관리 대시보드

대시보드는 일반적으로 _관리자_&#x200B;에 로그인할 때 나타나는 첫 번째 페이지이며 판매 및 고객 활동에 대한 실시간 개요를 제공할 수 있습니다. 대시보드 데이터는 라이프타임 판매, 평균 주문 금액, 최근 주문 및 검색어의 스냅샷을 제공합니다. 이 차트는 선택한 날짜 범위에 대해 완료된 주문 및 금액을 보여주며 동적, 실시간 데이터 또는 내역 집계된 데이터에서 생성할 수 있습니다. 하단의 탭은 베스트셀러 제품, 가장 많이 본 제품, 신규 고객 및 가장 많이 구매한 고객에 대한 빠른 보고서를 제공합니다.

처리할 데이터가 많은 경우 차트를 꺼서 성능을 향상시킬 수 있습니다. 다음 예제의 대시보드는 실시간 데이터를 사용하도록 구성되어 있으며 지난 24시간 동안 시간별로 완료된 주문을 표시합니다. 차트는 완료된 각 주문에 대해 업데이트됩니다.

![대시보드](./assets/dashboard-full.png){zoomable="yes"}

[고급 보고](business-intelligence.md#advanced-reporting)에서는 제품, 주문 및 고객 데이터를 기반으로 개인화된 대시보드를 표시합니다.

![고급 보고](./assets/dashboard-advanced-reporting.png){zoomable="yes"}

## 대시보드 구성

1. _관리자_ 사이드바에서 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**(으)로 이동하여 다음 설정을 완료합니다.

1. 구성이 완료되면 **[!UICONTROL Save Config]**&#x200B;을(를) 클릭합니다.

1. 변경 내용을 저장한 후 **[!UICONTROL Cache Management]**&#x200B;을(를) 클릭하고 모든 잘못된 캐시를 새로 고치십시오.

### 차트 활성화

처리할 데이터가 많은 경우 차트 표시를 해제하여 성능을 향상시킬 수 있습니다. 활성화되지 않은 경우 아래의 요약 합계가 여전히 생성되지만 차트 대신 &quot;데이터를 찾을 수 없음&quot; 메시지가 표시됩니다.

1. **[!UICONTROL Advanced]** 아래의 왼쪽 탐색 패널에서 **[!UICONTROL Admin]**&#x200B;을(를) 선택합니다.

1. 필요한 경우 **[!UICONTROL Dashboard]** 섹션을 확장합니다.

   ![고급 구성 - 차트 사용](./assets/admin-dashboard-config.png){width="600"}

1. 기본값을 변경하려면 **[!UICONTROL Use system value]** 확인란의 선택을 취소하십시오.

1. **차트 사용**&#x200B;을(를) `Yes`(으)로 설정합니다.

관리자 구성 옵션에 대한 자세한 내용은 [구성 참조 안내서](../configuration-reference/advanced/admin.md)를 참조하십시오.

### 시작 페이지 변경

대시보드는 관리자의 기본 [시작 페이지](../configuration-reference/advanced/admin.md)이지만 다른 시작 페이지를 구성할 수 있습니다.

1. 아직 관리자 구성 옵션이 열려 있지 않은 경우 왼쪽 탐색 패널의 _[!UICONTROL Advanced]_에서&#x200B;**[!UICONTROL Admin]**을(를) 선택하십시오.

1. **시작 페이지** 섹션을 확장하려면 클릭하세요.

   ![관리자 대시보드 - 시작 페이지 설정](./assets/admin-startup-page.png){width="600"}

1. **[!UICONTROL Use system value]** 확인란의 선택을 취소하고 관리자에 로그인할 때 표시할 **시작 페이지**&#x200B;를 선택합니다.

### 시작 날짜 선택

1. **[!UICONTROL General]** 아래의 왼쪽 탐색 패널에서 **보고서**&#x200B;를 선택합니다.

1. 페이지에서 **[!UICONTROL Dashboard]** 섹션을 확장합니다.

1. 날짜 설정에 대한 **[!UICONTROL Use system value]** 확인란의 선택을 취소하고 다음을 수행합니다.

   - **연간 누계 시작**&#x200B;을(를) **월** 및 **일**(으)로 설정합니다.

   - **현재 월 시작**&#x200B;을(를) **일**(으)로 설정합니다.

   ![관리자 대시보드 - 날짜 설정](./assets/reports-dashboard.png){width="600"}

[!UICONTROL Reports] 구성 옵션에 대한 자세한 내용은 [_구성 참조 안내서_](../configuration-reference/general/reports.md)&#x200B;를 참조하십시오.

### 데이터 소스 구성

실시간으로 또는 집계된 내역 데이터를 사용하여 대시보드 차트를 생성할 수 있습니다. 성능이 문제인 경우 집계된 데이터를 사용하여 작업 속도를 높일 수 있습니다.

1. 왼쪽 탐색 패널에서 **판매**&#x200B;를 확장하고 아래의 **판매**&#x200B;을(를) 선택합니다.

1. 페이지에서 **[!UICONTROL Dashboard]** 섹션을 확장합니다.

   ![관리 대시보드 - 데이터 원본 설정](./assets/config-sales-dashboard.png){width="600"}

1. **[!UICONTROL Use system value]** 확인란의 선택을 취소하고 **[!UICONTROL Use Aggregated Data]**&#x200B;을(를) 다음 중 하나로 설정합니다.

   - 집계된 이전 데이터의 경우 `Yes`을(를) 선택하십시오.
   - 실시간 데이터의 경우 `No`을(를) 선택하십시오.

## 차트 섹션

| 섹션 | 설명 |
|--- |--- |
| [!UICONTROL Orders] | 이 탭에는 현재 스토어 조회수 및 지정된 기간에 대해 완료된 모든 주문의 실시간 차트가 표시됩니다. |
| [!UICONTROL Amounts] | 이 탭에는 현재 스토어 뷰 및 지정된 기간에 대한 완료된 모든 주문 금액의 실시간 차트가 표시됩니다. |
| [!UICONTROL Time Range] | 아래 차트 및 요약 합계에 표시되는 데이터를 결정합니다. 옵션: `Last 7 Days` / `Current Month` / `YTD` / `2YTD` |
| [!UICONTROL Summary Totals] | 차트 아래의 매출, 세금, 출하 및 수량 합계는 차트 데이터 및 현재 시간 범위 설정을 기반으로 합니다. |

{style="table-layout:auto"}

## 스냅샷 데이터

| 섹션 | 설명 |
|--- |--- |
| [!UICONTROL Lifetime Sales] | 스토어 라이프타임 동안의 총 매출액 집계입니다. |
| [!UICONTROL Average Order] | 스토어 수명 동안의 평균 주문 금액입니다. |
| [!UICONTROL Last Orders] | 최근 5개의 주문 요약. |
| [!UICONTROL Last Search Terms] | 마지막 5개 검색어. |
| [!UICONTROL Top Search Terms] | 가장 일반적으로 사용되는 검색어 5개. |

{style="table-layout:auto"}

## 보고서 탭

| 섹션 | 설명 |
|--- |--- |
| [!UICONTROL Bestsellers] | 지정된 기간 동안 가장 많이 판매된 5개 제품. |
| [!UICONTROL Most Viewed Products] | 지정된 기간 동안 가장 많이 본 다섯 가지 제품입니다. |
| [!UICONTROL New Customers] | 지정된 기간 동안 계정에 등록한 가장 최근 5명의 고객. |
| [!UICONTROL Customers] | 지정된 기간 동안 처리가 완료된 주문이 있는 마지막 5개의 고객. |

{style="table-layout:auto"}

## 대시보드 단추

| 단추 | 설명 |
|--- |--- |
| [!UICONTROL Reload Data] | 대시보드 데이터를 새로 고칩니다. |
| [!UICONTROL Go to Advanced Reporting] | 제품, 주문 및 고객 데이터를 기반으로 동적 차트 및 보고서의 개인화된 대시보드를 표시합니다. 보다 광범위한 분석은 [고급 보고](business-intelligence.md#advanced-reporting)를 참조하십시오. |

{style="table-layout:auto"}
