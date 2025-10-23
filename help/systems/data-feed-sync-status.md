---
title: 데이터 피드 상태 모니터링
description: 데이터 내보내기 동기화를 모니터링하고  [!DNL Catalog Service], [!DNL Live Search] 및 [!DNL Product Recommendations]에 대한 피드 처리와 관련된 문제 또는 지연을 식별합니다.
feature: Products, Customers, Data Import/Export
badgePaas: label="PaaS만" type="Informative" url="https://experienceleague.adobe.com/ko/docs/commerce/user-guides/product-solutions" tooltip="Adobe Commerce 온 클라우드 프로젝트(Adobe 관리 PaaS 인프라) 및 온프레미스 프로젝트에만 적용됩니다."
source-git-commit: 433d3fd4dc10a81b685262c1e3c06a0da5778841
workflow-type: tm+mt
source-wordcount: '1455'
ht-degree: 0%

---


# 데이터 피드 상태 모니터링

Adobe Commerce 관리자는 Commerce 관리자의 데이터 피드 동기화 상태 페이지를 사용하여 Adobe Commerce에서 연결된 Commerce 서비스로 내보낸 데이터의 동기화 상태를 모니터링할 수 있습니다.

![피드 항목 상태를 보고하는 데이터 피드 동기화 상태 세부 정보 페이지](assets/data-feed-sync-status.png)

이 페이지에서는 제품 및 범주 데이터를 Commerce에서 [!DNL Product Recommendations], [!DNL Live Search] 및 [!DNL Catalog Service]과 같은 외부 서비스로 전송하는 데이터 내보내기 피드의 상태와 성능에 대한 실시간 통찰력을 제공합니다.

동기화 상태 페이지에는 내보내기 상태만 표시됩니다. 성공 상태는 데이터가 게시를 위해 SaaS 데이터베이스로 성공적으로 내보내졌음을 나타냅니다. [데이터 관리 대시보드](data-dashboard.md)를 사용하여 Commerce 데이터베이스에서 연결된 서비스로 전송되는 데이터를 추적합니다.

피드 상태 모니터링은 데이터 일관성을 보장하고 내보내기 프로세스 중에 발생하는 모든 문제를 신속하게 해결할 수 있습니다. 관리자는 다음 작업을 수행할 수 있습니다.

* 모든 데이터 피드에 대해 **동기화 상태 보기**
* 피드 처리에서 **오류 식별 및 문제 해결**
* 개별 피드 항목에 대한 **자세한 상태 정보에 액세스**

다음 피드에 대해 상태가 추적됩니다.

* 제품 피드
* 제품 속성 피드
* 카테고리 피드
* 제품 재정의 피드
* 제품 가격 피드
* 제품 변형 피드

>[!TIP]
>
>데이터 동기화 프로세스에 대한 자세한 내용은 [SaaS 데이터 내보내기 안내서](https://experienceleague.adobe.com/ko/docs/commerce/saas-data-export/data-synchronization)*에서 *SaaS 데이터 내보내기와 데이터 동기화*&#x200B;를 참조하십시오.

## 확장 설치

데이터 피드 상태 페이지는 다음 Commerce 서비스에 대한 활성 라이선스가 있는 모든 Commerce 판매자가 사용할 수 있습니다.

* [[!DNL Product Recommendations v6.0.0+]](https://experienceleague.adobe.com/ko/docs/commerce/product-recommendations/guide-overview)
* [[!DNL Live Search v4.1.0+]](https://experienceleague.adobe.com/ko/docs/commerce/live-search/guide-overview)
* 활성 라이선스가 있는 [[!DNL Catalog Service v1.17+]](https://experienceleague.adobe.com/ko/docs/commerce/catalog-service/guide-overview).

**요구 사항**

* PHP 8.1, 8.2, 8.3 또는 8.4
* Adobe Commerce 2.4.4+
* [Adobe Commerce 데이터 내보내기 확장](https://experienceleague.adobe.com/ko/docs/commerce/saas-data-export/manage-extension), 버전 103.4.15 이상
* [repo.magento.com에 액세스](https://repo.magento.com)

  키를 생성하고 필요한 권한을 얻으려면 [인증 키 가져오기](https://experienceleague.adobe.com/ko/docs/commerce-operations/installation-guide/prerequisites/authentication-keys)를 참조하십시오. 클라우드 설치의 경우 [Commerce on Cloud Infrastructure Guide](https://experienceleague.adobe.com/ko/docs/commerce-on-cloud/user-guide/develop/authentication-keys)를 참조하십시오.

* Adobe Commerce 애플리케이션 서버의 명령줄에 액세스합니다.

### 설치 단계

작성기를 사용하여 `adobe-commerce/module-data-exporter-status` 모듈 추가:

```shell
composer require magento/module-data-exporter-status
```

자세한 설치 단계는 다음 안내서를 참조하십시오.

* [클라우드 인프라에서 Adobe Commerce에 확장 설치](https://experienceleague.adobe.com/ko/docs/commerce-on-cloud/user-guide/configure-store/extensions)

* [확장 Adobe Commerce 온-프레미스 설치](https://experienceleague.adobe.com/ko/docs/commerce-operations/installation-guide/tutorials/extensions)

## 데이터 피드 상태 페이지 액세스

Commerce 관리자의 **[!DNL System]** > 데이터 전송 > **[!DNL Data Feed SyncStatus]**&#x200B;에서 Commerce 관리자의 데이터 피드 상태 페이지에 액세스합니다.

데이터 피드 내보내기 활동을 요약하는 ![데이터 피드 동기화 상태 페이지](assets/data-feed-sync-status.png)

데이터 피드 상태 모니터링은 다음 두 가지 인터페이스를 제공합니다.

* 사용 가능한 피드 및 현재 상태를 나열하는 [데이터 피드 동기화 상태 요약 페이지](#data-feed-sync-status-summary)
* 선택한 피드에 대한 자세한 정보를 표시하는 [데이터 피드 동기화 상태 - 세부 정보 페이지](#data-feed-sync-status-details)입니다.

## 데이터 피드 동기화 상태 요약

피드 동기화 상태 요약 페이지는 다음 정보를 포함하여 데이터 피드 내보내기 활동에 대한 정보를 제공합니다.

| 필드 | 설명 |
|-------|-------------|
| **피드 이름** | 특정 엔티티 또는 해당 부분의 동기화를 담당하는 피드 인덱서의 이름(예: 제품 또는 제품 가격)입니다. |
| **Source 레코드** | Commerce 데이터베이스에서 내보낼 수 있는 레코드 수입니다. 각 피드 항목이 스토어 보기 코드와 같은 특정 범위에 속하기 때문에 이 숫자는 Commerce 관리자에 표시되는 레코드 수보다 클 수 있습니다. |
| **레코드를 보냈습니다** | 추가 처리를 위해 Commerce SaaS로 성공적으로 전송된 레코드 수입니다. 전송 중에 오류가 발생한 경우 외부 서비스로 성공적으로 전송된 레코드 수입니다. |
| **실패한 레코드** | 내보내기에 실패하여 주의가 필요한 레코드 수입니다. |
| **작업** | 피드에 대한 동기화 활동을 보려면 **[!UICONTROL Details]**&#x200B;을(를) 선택하십시오. |

## 데이터 피드 동기화 상태 세부 정보

데이터 피드 상태 요약 페이지에서 피드 이름을 클릭하거나 [!DNL View Details] 작업을 사용하여 피드 내의 개별 레코드에 대한 자세한 정보에 액세스합니다.

피드 항목 상태를 보고하는 ![[!UICONTROL Data Feed Sync Status - Details]페이지](assets/data-feed-sync-status-details.png)

세부 사항 보기는 각 피드 항목에 대해 다음 정보를 제공합니다.

| 필드 | 설명 |
|-------|-------------|
| **피드 항목 ID** | 피드 레코드에 대한 내부 식별자 |
| **엔터티 ID** | 소스 엔티티 ID(제품 ID, 카테고리 ID 등) |
| **내보내기 상태** | 피드 항목의 [동기화 상태](#export-status-types)입니다. 색상으로 구분된 표시기가 있는 내보내기 시도의 현재 상태 |
| **마지막 동기화 날짜** | 레코드가 Commerce 서비스로 마지막으로 전송된 타임스탬프 |
| **엔터티가 삭제되었습니까?** | Adobe Commerce에서 엔티티 또는 해당 부품(예: 제품 또는 제품 가격)이 삭제되었는지 여부를 나타냅니다. 동기화 중에 오류가 발생한 경우에만 항목이 표시됩니다. |
| **요청 ID** | 동기화 요청에 대한 고유 식별자. 특정 엔티티 업데이트 문제를 해결할 때 지원팀에 이 ID를 제공하십시오. |
| **오류** | 피드 항목 동기화에 실패한 경우 자세한 오류 정보. |

다음 컨트롤을 사용하여 보기를 관리할 수 있습니다.

* [!DNL Mass Action]: 선택한 피드 항목에 대한 재동기화를 예약합니다.
* [!DNL Filters]
* [!DNL Default View]: 필터링된 보기를 만들고 저장하고 보기 간에 전환합니다.
* 테이블에서 열을 표시하거나 숨기려면 [!DNL Columns]을(를) 사용합니다.

### 피드 상태 표시기

각 피드 세부 사항 페이지의 맨 위에서 중요 상태 표시기는 각 피드에 대한 시스템 상태를 제공합니다.

#### 인덱서 상태

* **유효**: 데이터가 동기화되어 다시 인덱싱할 필요가 없습니다.
* **잘못됨**: 원본 데이터가 변경되었습니다. 인덱스를 업데이트해야 합니다.
* **처리 중**: 인덱싱이 진행 중입니다.

>[!TIP]
>
>인덱스 처리에 대한 자세한 내용은 [인덱스 관리](https://experienceleague.adobe.com/ko/docs/commerce-admin/systems/tools/index-management) 항목을 참조하십시오.

#### 로그 백로그 변경

* **모두 동기화됨**: 프로세스에 대한 보류 중인 변경 내용이 없습니다.
* **백로그의 항목**: 처리 대기 중인 보류 중인 변경 내용 수

### 내보내기 상태 유형

시스템은 문제를 신속하게 식별하는 데 도움이 되는 상태 표시기를 제공합니다.

#### 상태 범주

| **상태** | **설명** | **필요한 작업** |
|--------|-----------|-------------|
| **서비스에 제출됨** | 피드 항목을 Commerce 서비스로 내보냈습니다. | 없음 |
| **실패, 다시 시도** | 일시적인 오류입니다. 시스템이 자동으로 다시 시도합니다. | 문제 해결 모니터링 |
| **실패, 주의 필요** | 애플리케이션 또는 데이터 오류로 인해 실패했습니다. | [!DNL Error] 열에서 문제를 조사하고 해결합니다. |
| **제출 대기 중** | 내보내기를 큐에 넣었지만 아직 처리되지 않았습니다. | 정상 처리 상태 |

## 데이터 피드 상태 모니터링

Commerce 데이터베이스에서 제품 및 카테고리 관련 엔터티를 업데이트하면 피드 구성에 따라 데이터가 Commerce 서비스로 전송됩니다. 데이터 피드 동기화 상태 요약 페이지에서 이 프로세스를 실시간으로 모니터링할 수 있습니다.

>[!IMPORTANT]
>
>데이터 동기화를 완료하는 데 걸리는 시간은 카탈로그 크기, 업데이트된 데이터의 볼륨 및 외부 서비스 성능에 따라 다릅니다.

성공적으로 전송된 레코드 수가 소스 레코드 수와 일치하면 동기화가 완료되고 모든 데이터가 성공적으로 전송되었음을 나타냅니다.

>[!NOTE]
>
>Adobe은 또한 개발자와 시스템 통합자가 동기화 작업을 관리하고 추적하는 데 사용할 수 있는 명령줄 인터페이스 도구와 시스템 로그를 제공합니다. 자세한 내용은 [SaaS 데이터 내보내기 안내서](https://experienceleague.adobe.com/ko/docs/commerce-merchant-services/saas-data-export/overview)를 참조하십시오.

### 실패한 내보내기 관리

실패한 내보내기의 세부 정보를 확인하고 수정 작업을 수행하려면 다음을 수행합니다.

1. 피드 동기화 상태 페이지에서 실패한 레코드가 있는 피드를 찾습니다.
1. **[!DNL Details]**&#x200B;을(를) 클릭합니다.

1. 특정 실패 이유에 대한 오류 메시지를 검토하십시오.

1. 대량 조치를 사용하여 실패한 품목에 대한 재동기화 작업을 스케줄링합니다.

### 실패한 데이터 재동기화

[!DNL Actions] 페이지의 [!DNL Data Feed Sync Status - Details] 메뉴를 사용하여 수동으로 실패한 데이터 피드 또는 문제가 있는 데이터 피드를 다시 동기화할 수 있습니다.

시스템이 특정 유형의 실패를 자동으로 다시 시도하는 동안 다음 시나리오에서 수동 개입이 필요할 수 있습니다.

* 인증 또는 권한 오류(401, 403 상태 코드)가 표시됩니다.
* 페이로드 오류를 일으킨 데이터 형식 문제를 해결한 후
* 외부 서비스 구성 또는 엔드포인트에 대한 다음 업데이트.
* 데이터 내보내기 프로세스에 영향을 주는 사용자 지정을 배포하고 있습니다.

피드 상태를 사전 예방적으로 모니터링하고 오류를 신속하게 해결함으로써 Commerce 에코시스템 전반에서 데이터 일관성과 안정성을 유지할 수 있습니다.

#### 피드 항목 수동 재동기화

특정 피드 항목을 다시 동기화해야 하는 경우:

1. **레코드 선택**: 주의가 필요한 실패한 레코드를 선택하려면 확인란을 사용하십시오.
2. **동작 선택**: 일괄 동작 드롭다운에서 **[!DNL Schedule Resync]**&#x200B;을(를) 선택합니다.
3. **확인**: **[!DNL Submit]**&#x200B;을(를) 클릭하고 다시 동기화 작업을 확인합니다.
4. **결과 모니터링**: 성공 메시지를 확인하고 상태 변경을 모니터링합니다.

## 우수 사례

### 정기 모니터링

1. **일별 검사**: 오류율이 높은 피드에 대한 개요 페이지를 매일 검토합니다
1. **주별 심층 분석**: 중요 피드(제품, 가격)에 대한 세부 상태를 검사합니다.
1. **월별 분석**: 내보내기 성공률 및 성능의 트렌드를 추적합니다.

### 워크플로우 문제 해결

1. **문제 식별**: 오류 및 높은 오류 수 확인
1. **인덱서 상태 확인**: 인덱서가 유효하고 백로그가 관리 가능한지 확인하십시오.
1. **오류 세부 정보 검토**: 특정 오류 메시지를 보려면 실패한 레코드를 클릭하십시오.
1. **다시 동기화 예약**: 대량 작업을 사용하여 실패한 내보내기를 다시 시도하십시오
1. **모니터 해상도**: 다시 동기화된 항목에 성공 상태가 표시되는지 확인

### 일반적인 문제 해결

#### 높은 실패율

**증상**: &quot;실패, 주의 필요&quot; 상태를 표시하는 레코드가 너무 많습니다.

**가능한 원인**:

* 외부 서비스 구성 변경 사항
* 데이터 형식 비호환성
* 인증 또는 권한 문제

**해결 단계**:

1. 외부 서비스 상태 및 구성 확인
1. 패턴에 대한 오류 메시지 검토
1. 인증 자격 증명 확인
1. 필요한 경우 외부 서비스 지원에 문의하십시오

#### 느린 내보내기 성능

**증상**: 변경 로그 백로그가 많고 상태 업데이트가 느림

**가능한 원인**:

* 인덱서 성능 문제
* 높은 데이터 볼륨
* 외부 서비스 속도 제한

**해결 단계**:

1. 인덱서 상태를 확인하고 잘못된 경우 다시 실행
2. 외부 서비스 응답 시간 모니터링
3. 사용량이 적은 시간 동안 내보내기 일정 조정 고려
4. 시스템 리소스 및 성능 검토

#### 인증 실패

**증상**: 401 또는 403 상태 코드

**해결 단계**:

1. API 자격 증명 및 토큰 확인
1. 외부 서비스 계정 권한 확인
1. 만료된 인증 토큰 갱신
1. 액세스 문제에 대해서는 서비스 공급업체에 문의하십시오

>[!MORELIKETHIS]
>
>* [데이터 관리 대시보드](https://experienceleague.adobe.com/ko/docs/commerce-admin/systems/data-transfer/data-dashboard)
>* [SaaS 데이터 내보내기 안내서](https://experienceleague.adobe.com/ko/docs/commerce-merchant-services/saas-data-export/overview)
