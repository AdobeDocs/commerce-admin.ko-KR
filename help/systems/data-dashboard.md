---
title: 데이터 관리 대시보드
description: 카탈로그 서비스, 라이브 검색, 제품 Recommendations의 데이터 스트림에 대한 인사이트에 액세스하는 방법에 대해 알아봅니다.
feature: Products, Customers, Data Import/Export
source-git-commit: eed80afd8755d416d979c362f8c21fe97ce2d2ba
workflow-type: tm+mt
source-wordcount: '258'
ht-degree: 0%

---


# 데이터 관리 대시보드

데이터 관리 대시보드는 Adobe Commerce SaaS 제품에 대한 데이터 스트림에 대한 통찰력을 제공합니다. 사용자 [!DNL Live Search], [!DNL Product Recommendations], 및 [!DNL Catalog Service] 단일 대시보드에서 제품 동기화 상태를 보고 데이터를 다시 동기화할 수 있습니다.

데이터 관리 대시보드는 다음 위치에 있습니다. *시스템* > 데이터 전송 > *데이터 관리 대시보드*.

![데이터 관리 대시보드](assets/data-management-dashboard.png)

## 설정

다음 **[!UICONTROL Settings]** 페이지 오른쪽에 있는 버튼을 클릭하면 카탈로그 데이터를 다시 동기화할 수 있는 대화 상자가 열립니다.

카탈로그 데이터를 다시 동기화하면 서비스는 상거래 데이터베이스에서 데이터를 다시 가져옵니다. 이 작업은 일반적으로 몇 시간 동안 카탈로그 동기화가 실행되지 않은 첫 번째 온보딩 중에 사용됩니다.

## 동기화 상태

다음 _[!UICONTROL Sync]_상태 패널은 지난 3시간 동안 동기화된 제품 수를 보고합니다. 카탈로그를 자주 업데이트하지 않는 경우 이 값은 0인 경우가 많습니다. 클릭&#x200B;**[!UICONTROL Refresh]**카운트를 새로 고칩니다.

## 제품 수

제품 수 패널은 서비스에 사용할 수 있는 총 카탈로그 제품 수를 반영합니다.

다음 [!DNL Product Recommendations] 및 [!DNL Live Search] 대시보드에 다음의 총 수가 표시됨 _표시 가능_ 제품. [!DNL Catalog Service] 은 표시 가능으로 제품을 필터링하지 않으므로 두 가지가 모두 있는 경우 [!DNL Catalog Service] 및 [!DNL Live Search] 또는 [!DNL Product Recommendations] 설치되면 두 대시보드에서 제품 수에 대한 두 개의 다른 값을 표시할 수 있습니다.

## 동기화된 제품

Synced Products 테이블은 인덱스의 제품에 대한 세부 정보를 제공합니다. 기본적으로 이 테이블은 &#39;최근 업데이트&#39;별로 정렬됩니다.

특정 제품을 찾으려면 다음을 사용하십시오. **[!UICONTROL Search by SKU]** 필드 .
표시할 열을 제어하려면 **[!UICONTROL Customize Table]** 테이블 오른쪽에 있습니다.
