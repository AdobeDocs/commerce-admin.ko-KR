---
title: 데이터 관리 대시보드
description: 데이터 관리 대시보드에 대해 알아보기
feature: Products, Customers, Data Import/Export
source-git-commit: 925af4d3841f2972dfffcd52125a41c4a4b28815
workflow-type: tm+mt
source-wordcount: '291'
ht-degree: 0%

---

# 데이터 관리 대시보드

데이터 관리 대시보드는 Adobe Commerce SaaS 제품에 대한 데이터 스트림에 대한 통찰력을 제공합니다. 사용자 [!DNL Live Search], [!DNL Product Recommendations], 및 [!DNL Catalog Service] 단일 대시보드에서 제품 동기화 상태를 보고 데이터를 다시 동기화할 수 있습니다.

데이터 관리 대시보드는 다음 위치에 있습니다. *시스템* > 데이터 전송 > *데이터 관리 대시보드*.

![데이터 관리 대시보드](assets/data-management-dashboard.png)

## 설정

페이지 오른쪽에 있는 설정 버튼을 클릭하면 [[!DNL Catalog Sync]](https://experienceleague.adobe.com/docs/commerce-merchant-services/user-guides/data-services/catalog-sync.html) 설정 대화 상자.

일반적으로 [!DNL Catalog Sync] 프로세스는 한 시간에 한 번 자동으로 실행됩니다.

카탈로그 데이터를 다시 동기화하면 서비스가 상거래 데이터베이스에서 데이터를 다시 가져오게 되므로 최신 변경 사항이 서비스 및 사이트에 반영됩니다. 몇 가지 제품 변경을 수행했으며 일반적인 자동 동기화 프로세스 전에 이러한 변경 사항을 업데이트해야 하는 경우 이 버튼을 사용합니다.

## 동기화 상태

다음 _[!UICONTROL Sync]_상태 패널은 지난 3시간 동안 동기화된 제품 수를 보고합니다. 카탈로그를 자주 업데이트하지 않는 경우 이 값은 0인 경우가 많습니다. 클릭&#x200B;**[!UICONTROL Refresh]**카운트를 새로 고칩니다.

## 제품 수

제품 수 패널은 서비스에 사용할 수 있는 총 카탈로그 제품 수를 반영합니다.

다음 [!DNL Catalog Service] 대시보드는 서비스에 사용할 수 있는 카탈로그의 총 제품 수를 반영합니다. 일반적으로 상거래 데이터베이스의 모든 제품입니다.

Product Recommendations 및 Live Search 대시보드에는 총 [_검색 가능_](https://experienceleague.adobe.com/docs/commerce-admin/catalog/catalog/search/search.html) 제품. 일부 제품이 검색 가능하도록 설정되지 않은 경우, 이는 간의 제품 합계 차이를 설명합니다. [!DNL Product Recommendations] 및 [!DNL Live Search], 및 [!DNL Catalog Service].

## 동기화된 제품

Synced Catalog Products 테이블은 인덱스의 제품에 대한 세부 정보를 제공합니다. 기본적으로 이 테이블은 &#39;최근 업데이트&#39;별로 정렬됩니다.

특정 제품을 찾으려면 다음을 사용하십시오**[!UICONTROL Search by SKU]** 필드 .
표시할 열을 제어하려면 **[!UICONTROL Customize Table]** 테이블 오른쪽에 있습니다.
