---
title: 데이터 관리 대시보드
description: ' [!DNL Catalog Service], [!DNL Live Search] 및 [!DNL Product Recommendation]의 데이터 스트림에 대한 인사이트에 액세스하는 방법에 대해 알아봅니다.'
feature: Products, Customers, Data Import/Export
exl-id: 63c261c1-1a52-46f7-93f8-81055edf1f7b
source-git-commit: 5da244a548b15863fe31b5df8b509f8e63df27c2
workflow-type: tm+mt
source-wordcount: '682'
ht-degree: 0%

---

# 데이터 관리 대시보드

데이터 관리 대시보드는 Commerce 데이터베이스에서 Commerce SaaS 서비스로 전송되는 제품 데이터의 동기화 상태에 대한 개요를 제공합니다. 사용자는 제품 동기화 상태를 편리하게 모니터링하고 통합 대시보드에서 데이터 재동기화를 시작할 수 있습니다. 이 기능은 상점 데이터의 가용성에 대한 중요한 통찰력을 제공하여 구매자에게 즉시 표시되도록 합니다.

## 대상자

활성 라이선스가 있는 [[!DNL Product Recommendations v6.0.0]](https://experienceleague.adobe.com/ko/docs/commerce/product-recommendations/guide-overview), [[!DNL Live Search v4.1.0]](https://experienceleague.adobe.com/ko/docs/commerce/live-search/guide-overview) 또는 [[!DNL Catalog Service v1.17]](https://experienceleague.adobe.com/ko/docs/commerce/catalog-service/guide-overview)을(를) 사용하는 모든 Commerce 가맹점에서 추가 비용 없이 데이터 관리 대시보드를 사용할 수 있습니다.

데이터 관리 대시보드는 *시스템* > 데이터 전송 > *데이터 관리 대시보드*&#x200B;에 있습니다.

![데이터 관리 대시보드](assets/data-management-dashboard.png)

대시보드에는 다음 필드가 포함되어 있습니다.

| 필드 | 설명 |
|--- |--- |
| 범위 | 동기화된 데이터에 대한 특정 웹 사이트입니다. |
| [!DNL Product Recommendations] | 동기화 상태, 동기화된 제품 수 및 [!DNL Product Recommendations]에 대해 [표시 가능](https://experienceleague.adobe.com/ko/docs/commerce-admin/config/catalog/inventory#stock-options) 동기화된 제품 테이블을 표시합니다. |
| [!DNL Live Search] | 동기화 상태, 동기화된 제품 수 및 [!DNL Live Search]에 대해 [표시 가능](https://experienceleague.adobe.com/ko/docs/commerce-admin/config/catalog/inventory#stock-options) 동기화된 제품 테이블을 표시합니다. |
| [!DNL Catalog Service] | [!DNL Catalog Service]에 대해 동기화 상태, 동기화된 제품 수 및 동기화된 제품 테이블을 표시합니다. |
| 설정 | [카탈로그 데이터를 수동으로 다시 동기화](#resync-catalog-data)할 수 있는 대화 상자를 엽니다. |
| 동기화 상태 | 지난 3시간 내에 Commerce 데이터베이스에서 SaaS 서비스로 전송된 제품 수를 표시합니다. 카탈로그를 자주 업데이트하지 않는 경우 이 값은 0인 경우가 많습니다. 동기화가 진행 중이면 **[!UICONTROL Refresh]**&#x200B;을(를) 클릭하여 업데이트된 개수를 가져옵니다. |
| 제품 수 | 서비스에 사용할 수 있는 총 카탈로그 제품 수를 반영합니다. [!DNL Product Recommendations] 및 [!DNL Live Search] 대시보드에는 총 _표시 가능_ 제품 수가 표시됩니다. [!DNL Catalog Service]은(는) 표시 가능한 제품별로 제품을 필터링하지 않으므로 [!DNL Catalog Service]과(와) [!DNL Live Search] 또는 [!DNL Product Recommendations]이(가) 모두 설치되어 있는 경우 두 대시보드에서 제품 수에 대한 두 개의 다른 값을 표시할 수 있습니다. |
| 동기화된 제품 | 핵심 Commerce 인덱스의 제품에 대한 세부 정보를 제공합니다. 기본적으로 이 테이블은 &#39;최근 업데이트&#39;별로 정렬됩니다. 특정 제품을 찾으려면 **[!UICONTROL Search by SKU]** 필드를 사용하십시오. 표시할 열을 제어하려면 표 오른쪽의 **[!UICONTROL Customize Table]**&#x200B;을(를) 클릭합니다. |

## 데이터 관리 대시보드 사용

Commerce 데이터베이스에서 제품을 업데이트하면 시스템 구성에 따라 제품 데이터가 SaaS 서비스로 전송됩니다. 동기화 프로세스가 시작되면 **제품 수**&#x200B;는 SaaS 서비스로 보낸 제품 수를 나타냅니다.

>[!IMPORTANT]
>
>동기화를 완료하는 데 걸리는 시간은 카탈로그 크기 및 업데이트된 데이터의 볼륨에 따라 다릅니다.

처리된 제품 수가 업데이트된 제품 수와 일치하면 동기화가 완료되었음을 나타냅니다.

>[!NOTE]
>
>Adobe은 또한 개발자와 시스템 통합자가 Commerce SaaS 서비스의 동기화 작업을 관리 및 추적하고 오류를 해결하는 데 사용할 수 있는 명령줄 인터페이스와 시스템 로그를 제공합니다. 자세한 내용은 [SaaS 데이터 내보내기 안내서](https://experienceleague.adobe.com/ko/docs/commerce/saas-data-export/overview)를 참조하십시오.

### 동기화된 제품 목록

동기화된 제품에 대한 세부 정보를 보려면 표에서 제품을 클릭합니다.

![제품 세부 정보 동기화](assets/sync-product-detail.png)

### 카탈로그 데이터 재동기화

Commerce SaaS 서비스가 항상 최신 제품 정보를 제공하도록 하려면 카탈로그 데이터를 동기화하기 위해 [일정을 구현](https://experienceleague.adobe.com/ko/docs/commerce-operations/configuration-guide/cli/manage-indexers#reindex)해야 합니다.

Commerce 데이터베이스에서 SaaS 서비스로 카탈로그 데이터 재동기화를 [수동으로 시작](#manually-resync-catalog)할 수 있지만 하드웨어 리소스의 로드를 늘릴 수 있으므로 권장되지 않습니다. 그러나 다음 시나리오에서는 카탈로그를 수동으로 다시 동기화해야 할 수 있습니다.

- 새 제품 추가, 제품 세부 사항 업데이트 또는 범주 수정과 같이 제품 카탈로그에 중요한 변경 사항이 적용될 때마다

- 상점에 제품 데이터를 표시할 때 불일치나 성능 문제가 발생하는 경우

- Commerce 데이터베이스와 SaaS 서비스 간의 통합에 대한 모든 업데이트 또는 변경 사항 준수

- 제품 데이터 관리 또는 동기화 프로세스에 영향을 주는 사용자 지정 또는 구성 배포 시

이러한 지침을 준수하고 필요에 따라 사전 예방적으로 카탈로그 데이터를 재동기화함으로써 Adobe Commerce 에코시스템 전반에서 데이터 일관성, 정확성 및 안정성을 유지할 수 있습니다.

#### 수동으로 카탈로그 재동기화

카탈로그 데이터를 다시 동기화해야 하는 경우 페이지 오른쪽의 **[!UICONTROL Settings]**&#x200B;을(를) 클릭하여 다시 동기화를 시작할 수 있는 대화 상자를 표시합니다. 카탈로그 데이터를 다시 동기화하면 서비스가 Commerce 데이터베이스의 데이터를 SaaS 서비스로 다시 가져옵니다.

![수동으로 제품 동기화](assets/resync-data.png)
