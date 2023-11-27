---
title: 관리 대시보드
description: 일반적으로 로그인할 때 나타나는 첫 번째 페이지인 관리 대시보드에 대해 알아봅니다.
exl-id: 56957c0a-1618-444b-a37a-ecf0d7b27eae
source-git-commit: 7b6d70e2f3052af69075790cec1f396e2505bf8b
workflow-type: tm+mt
source-wordcount: '718'
ht-degree: 0%

---

# 관리 대시보드

일반적으로 대시보드는에 로그인할 때 나타나는 첫 번째 페이지입니다 _관리자_ 은 판매 및 고객 활동에 대한 실시간 개요를 제공할 수 있습니다. 대시보드 데이터는 라이프타임 판매, 평균 주문 금액, 최근 주문 및 검색어의 스냅샷을 제공합니다. 이 차트는 선택한 날짜 범위에 대해 완료된 주문 및 금액을 보여주며 동적, 실시간 데이터 또는 내역 집계된 데이터에서 생성할 수 있습니다. 하단의 탭은 베스트셀러 제품, 가장 많이 본 제품, 신규 고객 및 가장 많이 구매한 고객에 대한 빠른 보고서를 제공합니다.

처리할 데이터가 많은 경우 차트를 꺼서 성능을 향상시킬 수 있습니다. 다음 예제의 대시보드는 실시간 데이터를 사용하도록 구성되어 있으며 지난 24시간 동안 시간별로 완료된 주문을 표시합니다. 차트는 완료된 각 주문에 대해 업데이트됩니다.

![대시보드](./assets/dashboard-full.png){zoomable=&quot;yes&quot;}

[고급 보고](business-intelligence.md#advanced-reporting) 는 제품, 주문 및 고객 데이터를 기반으로 개인화된 대시보드를 표시합니다.

![고급 보고](./assets/dashboard-advanced-reporting.png){zoomable=&quot;yes&quot;}

## 대시보드 구성

1. 다음에서 _관리자_ 사이드바, 이동 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**다음 설정을 완료합니다.

1. 구성이 완료되면 다음을 클릭합니다. **[!UICONTROL Save Config]**.

1. 변경 사항을 저장한 후 **[!UICONTROL Cache Management]** 모든 잘못된 캐시를 새로 고칩니다.

### 차트 활성화

처리할 데이터가 많은 경우 차트 표시를 해제하여 성능을 향상시킬 수 있습니다. 활성화되지 않은 경우 아래의 요약 합계가 여전히 생성되지만 차트 대신 &quot;데이터를 찾을 수 없음&quot; 메시지가 표시됩니다.

1. 아래의 왼쪽 탐색 패널에서 **[!UICONTROL Advanced]**, 선택 **[!UICONTROL Admin]**.

1. 필요한 경우 **[!UICONTROL Dashboard]** 섹션.

   ![고급 구성 - 차트 활성화](./assets/admin-dashboard-config.png){width="600"}

1. 기본값을 변경하려면 **[!UICONTROL Use system value]** 확인란.

1. 설정 **차트 활성화** 끝 `Yes`.

관리자 구성 옵션에 대한 자세한 내용은 [구성 참조 안내서](../configuration-reference/advanced/admin.md).

### 시작 페이지 변경

대시보드가 기본값입니다 [시작 페이지](../configuration-reference/advanced/admin.md) 관리자만 다른 시작 페이지를 구성할 수 있습니다.

1. 관리자 구성 옵션이 아직 열려 있지 않은 경우 다음을 선택합니다. **[!UICONTROL Admin]** 아래에 _[!UICONTROL Advanced]_을 클릭합니다.

1. 를 클릭하여 확장합니다. **시작 페이지** 섹션.

   ![관리 대시보드 - 시작 페이지 설정](./assets/admin-startup-page.png){width="600"}

1. 지우기 **[!UICONTROL Use system value]** 확인란을 선택하고 **시작 페이지** 관리자에 로그인할 때 표시되는 옵션입니다.

### 시작 날짜 선택

1. 아래의 왼쪽 탐색 패널에서 **[!UICONTROL General]**, 선택 **보고서**.

1. 페이지에서 를 확장합니다. **[!UICONTROL Dashboard]** 섹션.

1. 지우기 **[!UICONTROL Use system value]** 날짜 설정에 대한 확인란을 선택하고 다음을 수행합니다.

   - 설정 **연간 누계 시작** (으)로 **월** 및 **일**.

   - 설정 **현재 월 시작** (으)로 **일**.

   ![관리 대시보드 - 날짜 설정](./assets/reports-dashboard.png){width="600"}

에 대한 자세한 내용은 [!UICONTROL Reports] 구성 옵션을 보려면 다음을 참조하십시오. [_구성 참조 안내서_](../configuration-reference/general/reports.md).

### 데이터 소스 구성

실시간으로 또는 집계된 내역 데이터를 사용하여 대시보드 차트를 생성할 수 있습니다. 성능이 문제인 경우 집계된 데이터를 사용하여 작업 속도를 높일 수 있습니다.

1. 왼쪽 탐색 패널에서 를 클릭하여 확장합니다. **판매** 및 선택 **판매** 밑에.

1. 페이지에서 를 확장합니다. **[!UICONTROL Dashboard]** 섹션.

   ![관리 대시보드 - 데이터 소스 설정](./assets/config-sales-dashboard.png){width="600"}

1. 지우기 **[!UICONTROL Use system value]** 확인란 및 설정 **[!UICONTROL Use Aggregated Data]** 다음 중 하나를 수행합니다.

   - 기록, 집계된 데이터의 경우 `Yes`.
   - 실시간 데이터의 경우 `No`.

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
| [!UICONTROL Go to Advanced Reporting] | 제품, 주문 및 고객 데이터를 기반으로 동적 차트 및 보고서의 개인화된 대시보드를 표시합니다. 보다 광범위한 분석은 다음을 참조하십시오. [고급 보고](business-intelligence.md#advanced-reporting). |

{style="table-layout:auto"}
