---
title: Adobe Commerce의 HIPAA 준비
description: Adobe Commerce HIPAA 지원 확장 기능을 추가하여 HIPAA 규정 준수를 지원할 수 있는 추가 기능을 사용하는 방법에 대해 알아봅니다.
feature: Security, Compliance
exl-id: 4b3eb5b0-4475-47df-92a9-10d12fec1e66
source-git-commit: 2807c36fdb4ca169c31a5e92b4dab278a45c474c
workflow-type: tm+mt
source-wordcount: '2375'
ht-degree: 1%

---

# Adobe Commerce의 HIPAA 준비

>[!IMPORTANT]
>
>**법적 고지 사항**<br/>
>이 정보는 Adobe 고객이 Adobe의 HIPAA 지원 서비스에 대한 질문에 답변할 수 있도록 돕기 위한 것입니다. 그것은 법률적인 조언이 되지 않는다. 판매자는 HIPAA에 따른 의무와 Adobe 제품의 적절한 사용 및 구성을 이해하기 위해 자체 법률 자문을 구해야 합니다.

>[!BEGINSHADEBOX]

**건강보험 양도 및 책임에 관한 법률(HIPAA)**

HIPAA(Health Insurance Portability and Accountability Act)는 미국의 주요 연방 의료 개인정보 보호법이며 미국 보건복지부(HHS)에서 시행하고 있습니다. HIPAA는 _적용 엔터티_(의료 서비스 공급자, 보험사 및 결제 서비스 등) 및 _비즈니스 연결_(적용 엔터티에 서비스를 제공하는 엔터티 등)에 적용됩니다. HIPAA 요구 사항은 개인 정보 보호 규칙, 보안 규칙 및 위반 알림 규칙의 세 가지 규칙에 따라 설정됩니다. Adobe은 특정 제품에 대해 비즈니스 동료 역할을 하며, Adobe은 이를 &quot;HIPAA 준비 서비스&quot;로 분류합니다. HIPAA에서 규제되는 데이터는 _보호 상태 정보_ 또는 PHI라고 합니다. PHI는 (1) 의료 제공자, 의료 계획 또는 의료 정보 교환소가 생성 또는 수신하는 건강 정보의 하위 집합이며, (2) 개인의 과거, 현재 또는 미래의 신체적 또는 정신적 건강 또는 상태, 개인에 대한 의료 서비스 제공 또는 개인에 대한 의료 서비스 제공에 대한 과거, 현재 또는 미래 지불에 관한 것이고, (3) 개인을 식별하거나 해당 정보가 개인을 식별하는 데 사용될 수 있다고 믿을 수 있는 합리적인 근거가 있는 것입니다. HIPAA 개인 정보 보호 및 보안 규칙은 피보험 기업이 비즈니스 관련 계약 또는 BAA의 형태로 비즈니스 관계자로부터 서면 보증을 받도록 요구하여 비즈니스 관련자가 피보험 기업의 ʼ PHI의 개인 정보 보호 및 보안을 보호하도록 요구합니다. 자세한 내용은 Adobe Trust Center에서 [HIPAA 및 Adobe 제품 및 서비스](https://www.adobe.com/trust/compliance/hipaa-ready.html)를 참조하십시오.

>[!ENDSHADEBOX]

## Adobe Commerce HIPAA 지원

Adobe Commerce HIPAA 지원 확장은 Adobe Commerce 설치에 상인이 각각의 HIPAA 의무를 준수할 수 있는 추가 기능 및 기능을 추가합니다.

Adobe Commerce HIPAA 지원 확장, `magento/hipaa-ee`은(는) 클라우드 인프라 또는 Adobe Managed Services 프로젝트의 Adobe Commerce에 사용할 수 있습니다. Adobe Commerce HIPAA 준비 설치 프로세스는 HIPAA 요구 사항을 준수하기 위해 일부 기본 서비스 및 기능을 비활성화합니다. [비활성화된 서비스 및 기능](#disabled-services-and-features)을(를) 참조하십시오.

>[!NOTE]
>
>HIPAA 지원 기능 액세스는 Adobe Commerce용 의료 서비스 추가 기능을 구입한 판매자만 사용할 수 있습니다.

*이러한 자료는 정보 제공 목적으로만 작성되었습니다. 이 정보의 제공은 수취인에게 어떠한 계약상의 권리나 다른 권리에 대한 자격을 부여하지 않는다. 제공된 날짜 현재 정보의 정확성을 보장하기 위해 노력했지만, 그러한 정보가 정확하고 완전하다는 표현은 하지 않습니다. Adobe은 법률 또는 Adobe의 제품이 변경될 때 이 정보를 업데이트할 의무가 없습니다. 또한 이 문서는 Adobe의 서면 동의 없이 의도한 수신자가 아닌 다른 사람에게 배포되지 않습니다.*

## 시스템 요구 사항

다음 표는 Adobe Commerce 버전과 HIPAA 준비 확장 기능 간의 호환성을 보여 줍니다.

| Adobe Commerce | 지원됨 | 메모 |
|----------------|-----------|-------|
| 2.4.7-p4 - 2.4.7-p5 | 1.2.0 | 2.4.7-p4 지원을 사용하려면 [핫픽스](https://experienceleague.adobe.com/en/docs/commerce-knowledge-base/kb/troubleshooting/known-issues-patches-attached/hotfix-for-hipaa-package-1-2-0-compatibility-with-adobe-commerce-2-4-7-p4)가 필요합니다. |
| 2.4.6-p9 - 2.4.6-p10 | 1.2.0 | |
| 2.4.6-p8 | 1.1.0 | [데이터 서비스](#adobe-commerce-services)에 대한 지원이 1.1.0에 도입되었습니다. |
| 2.4.6-p3 - 2.4.6-p7 | 1.0.0 | |

>[!IMPORTANT]
>
>- HIPAA 지원 확장은 Adobe Commerce on Cloud 또는 Adobe Commerce Managed Services 프로젝트에만 사용할 수 있습니다.
>- 확장은 `repo.magento.com`에서 작성기 메타패키지로 사용할 수 있습니다.
>- HIPAA 지원 기능에 액세스하려면 Adobe Commerce용 의료 서비스 추가 기능이 필요합니다.
>- Adobe Commerce 베타 버전은 지원되지 않습니다.

## 설치

**필수 구성 요소**

>[!BEGINSHADEBOX]

- Adobe은 HIPAA 준비 확장에 액세스할 수 있도록 Adobe Commerce 계정을 프로비저닝했습니다.
- 확장을 설치하려면 [repo.magento.com](https://repo.magento.com)에 액세스하십시오. 키를 생성하고 필요한 권한을 얻으려면 [인증 키 가져오기](https://experienceleague.adobe.com/docs/commerce-operations/installation-guide/prerequisites/authentication-keys.html)를 참조하십시오.

>[!ENDSHADEBOX]

Adobe Commerce 버전 2.4.7-p5 또는 2.4.6-p3에서 2.4.6-p8을 실행하는 인스턴스에 Adobe의 HIPAA 지원 서비스 확장(`magento/hipaa-ee`)의 최신 버전을 설치합니다. 확장은 [repo.magento.com](https://repo.magento.com) 리포지토리에서 작성기 메타패키지로 전달됩니다. 메타패키지에는 Adobe Commerce 인스턴스에 대해 HIPAA 기능을 활성화하는 모듈 컬렉션이 포함되어 있습니다.

>[!NOTE]
>
>Experience Platform으로 전송되는 백오피스 이벤트 데이터가 HIPAA를 사용할 수 있도록 하려면 [데이터 연결 확장 안내서](https://experienceleague.adobe.com/en/docs/commerce/data-connection/fundamentals/install#install-the-data-services-hipaa-extension)를 참조하십시오.

1. 로컬 워크스테이션에서 Adobe Commerce on cloud infrastructure 프로젝트의 프로젝트 디렉터리로 변경합니다.

   >[!NOTE]
   >
   >Commerce 프로젝트 환경을 로컬로 관리하는 방법에 대한 자세한 내용은 _Adobe Commerce on Cloud Infrastructure 사용 안내서_&#x200B;의 [CLI로 분기 관리](https://experienceleague.adobe.com/en/docs/commerce-cloud-service/user-guide/develop/cli-branches)를 참조하십시오.

1. Adobe Commerce Cloud CLI를 사용하여 업데이트할 환경 분기를 체크아웃합니다.

   ```shell
   magento-cloud environment:checkout <environment-id>
   ```

1. 작성기 CLI를 사용하여 작성기 구성에 메타패키지 `magento/hipaa-ee`을(를) 추가합니다.

   ```shell
   composer require "magento/hipaa-ee" --no-update
   ```

1. 패키지 종속성을 업데이트합니다.

   ```shell
   composer update "magento/hipaa-ee"
   ```

1. 업데이트된 코드를 추가, 커밋 및 클라우드 환경에 푸시합니다.

   ```shell
   git add -A
   git commit -m "Add HIPAA-Ready Services modules"
   git push origin <branch-name>
   ```

   업데이트를 푸시하면 변경 사항을 적용하기 위한 Commerce 클라우드 배포 프로세스가[&#128279;](https://experienceleague.adobe.com/en/docs/commerce-cloud-service/user-guide/develop/deploy/process) 시작됩니다[. 배포 로그](https://experienceleague.adobe.com/en/docs/commerce-cloud-service/user-guide/develop/test/log-locations#deploy-log)에서 배포 상태를 확인합니다.

### 설치 확인

업데이트를 배포한 후 `Hipaa*` 확장이 설치되어 있는지 확인하십시오

1. SSH를 사용하여 원격 클라우드 환경에 로그인합니다.

   ```shell
   magento-cloud ssh
   ```

1. 명령줄에서 Adobe Systems Commerce CLI를 사용하여 모듈 상태를 확인합니다.

   ```shell
   bin/magento module:status
   ```

1. HIPAA 모듈이 활성화된 모듈 목록에 포함되어 있는지 확인합니다.

   ```text
   List of enabled modules:
   <truncated for brevity>
   Magento_HipaaAnalytics
   Magento_HipaaCheckout
   Magento_HipaaLogging
   Magento_HipaaScheduledImportExport
   Magento_HipaaAdminLogging
   Magento_HipaaCustomerLogging
   Magento_HipaaNewsletter
   Magento_HipaaImportExport
   Magento_HipaaApiLogging
   Magento_HipaaSales
   Magento_HipaaCustomer
   <truncated for brevity>
   ```

   접두사가 `Magento_Hipaa` 붙은 모든 모듈은 활성화된 모듈 섹션에 있어야 합니다.

## HIPAA 준비를 위한 기능 개선 사항

`magento/hipaa-ee` 확장은 기본 Commerce 제품에 몇 가지 변경 사항 및 개선 사항을 도입했습니다. 다음 섹션은 이러한 변경 사항과 기본 제품을 변경하는 방법에 대한 세부 정보를 제공합니다.

### 작업 로그

감사 로깅은 HIPAA 요구 사항입니다. Adobe Commerce에서 [작업 로그](../../systems/action-log.md) 기능은 스토어에서 작업하는 관리자가 수행한 모든 변경 사항을 기록합니다. 감사 로그에 대한 HIPAA 요구 사항을 충족하기 위해 관리 UI 및 API 호출을 통해 수행된 모든 관리 사용자 및 고객 작업을 기록하도록 기능이 업데이트되었습니다.

Adobe 서비스가 스토어 데이터에 액세스할 때 작업 로그가 이벤트도 캡처합니다. 작업 로그 보고서에서 &quot;외부로 전송된 데이터&quot; 작업을 필터링하여 이러한 이벤트를 식별할 수 있습니다.

#### 작업 로그 보고서

_작업 로그_ 보고서 표(**[!UICONTROL System]** > 작업 로그 > 보고서)가 관리 UI 및 API를 통해 수행되는 고객 작업에 맞게 수정되었습니다.

1. 다음 두 개의 열이 추가되었습니다.
   - ***Source***: 작업이 수행된 위치를 표시합니다.
값: `Admin UI` / `Customer UI` / `REST API` / `SOAP API` / `GraphQL API`
   - ***클라이언트 형식***: 클라이언트 형식을 표시합니다.
값: 고객 | 관리자 | 통합

2. ***사용자 이름*** 열의 이름이 ***클라이언트 식별자***(으)로 바뀌었습니다.
   - ***클라이언트 식별자***: 작업을 수행한 사용자의 로그인 ID를 표시합니다.
값:
      - 클라이언트 유형이 고객인 경우 이메일
      - 클라이언트 유형이 관리자인 경우 사용자 이름
      - 클라이언트 유형이 통합인 경우 이름

3. ***전체 작업 이름*** 열의 이름이 ***Target***(으)로 변경됨
   - ***대상***: 작업 이름을 표시합니다.
값:
      - Source이 REST API 또는 SOAP API인 경우 엔드포인트
      - GraphQL API인 경우 쿼리 또는 돌연변이 이름
      - 관리 UI 또는 고객 UI인 경우 작업 이름입니다.

#### 로깅에 대한 관리 작업 구성

모든 작업을 기본적으로 기록해야 하므로 이 기능을 사용할 수 없습니다.

### HIPAA 고객 검색 결과 제한

Adobe Commerce의 HIPAA 고객 검색 결과 제한 기능은 PHI(보호 상태 정보) 및 PII(개인 식별 정보)에 대한 액세스를 제한하여 HIPAA 규정 준수를 보장합니다. 이 기능은 사용자 역할에 따라 고객 레코드를 검색 및 조회하는 기능을 제한하여 권한이 있는 사용자만 이 정보에 액세스할 수 있도록 합니다.

#### 주요 기능

- **검색 제한**: 필요한 역할이 없는 사용자는 고객 레코드를 검색하거나 볼 수 없습니다.
- **액세스 필수 검색**: 기본 Adobe Commerce 동작과 달리 검색을 수행하지 않으면 고객 정보를 볼 수 없습니다. 따라서 사용자가 고객의 정보를 찾으려면 고객에 대한 특정 세부 정보를 알고 있어야 합니다.
- **제한된 검색 결과**: 기준과 일치하는 검색 결과는 10개의 레코드로 제한되어 한 번에 관리 가능한 수의 레코드만 표시됩니다.
- **최소 필터 수**: 사용자는 검색을 수행하기 위해 최소 3개의 필터(예: 이메일, 성, 상태)를 적용하여 검색이 특정되고 타깃팅되도록 해야 합니다.
- **필터 알림**: 검색 제한이 활성화되면 사용자는 필터를 적용하여 검색 결과를 구체화하라는 알림을 받습니다.

#### 구성

검색 결과에서 고객 수를 제한하기 위한 구성은 관리 패널의 **[!UICONTROL Stores]** > **[!UICONTROL Configuration]** > **[!UICONTROL Advanced]** > **[!UICONTROL Admin]** > **[!UICONTROL Admin Grids]**&#x200B;에 있습니다. 이 구성은 `hipaa-ee` 확장이 설치되어 있는 경우 기본적으로 사용하도록 설정됩니다.

- **그리드의 고객 수 제한**: 이 설정을 사용하면 그리드 검색 결과에 표시되는 고객 수에 대한 제한을 활성화하거나 비활성화할 수 있습니다.
- **고객 그리드 검색 결과 제한**: 이 설정은 그리드 검색 결과에 표시할 수 있는 최대 고객 레코드 수를 지정합니다.

#### 영향을 받는 기능 영역

관리자 순서 만들기 페이지(**[!UICONTROL Sales]** > **[!UICONTROL Orders]** > **[!UICONTROL Create New Order]**)와 고객 페이지(**[!UICONTROL Customers]** > **[!UICONTROL All Customers]**)의 고객 그리드는 검색 결과 제한 기능의 영향을 받습니다.

- 필터는 기본적으로 열립니다.
- 사용자는 검색을 수행하려면 최소 3개의 필터를 적용해야 합니다.
- 검색 결과는 기본적으로 10개의 레코드로 제한됩니다.
- 검색 기준과 일치하는 레코드가 더 있을 경우 알림에서 결과 제한과 검색을 세분화할 필요를 사용자에게 알립니다.
- 그리드 페이지 매김을 사용할 수 없습니다.
- 페이지에서 멀리 이동할 때 적용된 이전 검색 결과와 필터는 저장되지 않습니다.

검색 결과 제한 기능은 고객 검색을 위한 REST API(`/V1/customers/search`)에도 적용됩니다.

- 필터가 적용되어 있지 않거나 필터가 충분하지 않은 경우 API는 검색을 수행하는 데 필요한 필터 수가 필요하다는 오류 메시지를 반환합니다.
- 승인된 사용자가 충분한 필터를 적용하면 API는 지정된 제한 내의 결과를 반환합니다.
- 결과가 제한되면 발견된 총 레코드 수와 현재 적용된 한계를 나타내는 메시지가 응답에 추가됩니다.

### 기능 가져오기 및 내보내기

가져오기 및 내보내기 기능에 대한 향상된 기능은 관리 경험 환경을 개선하고 사용자 작업에 대한 더 나은 가시성을 제공하는 데 중점을 둡니다.

>[!NOTE]
>
>이러한 ***향상된 기능은 가져오기 및 내보내기 핵심 논리***&#x200B;를 변경하지 않고 기능을 확장하여 보다 포괄적인 로깅 및 향상된 데이터 기여도 분석 제공합니다. 수입과 수출의 기본 기능은 변함이 없습니다. 사용자는 기존 기능과 워크플로우를 중단 없이 계속 사용할 수 있습니다.

#### 관리 작업 로깅

가져오기 및 내보내기 기능의 주요 개선 사항 중 하나는 관리 작업의 향상된 로깅 기능입니다. 이 향상된 기능은 데이터 가져오기 및 내보내기와 관련된 활동을 더 깊이 파고들 수 있는 기능을 도입하여 향상된 추적 및 감사 기능에 기여합니다. 이제 다음 작업이 기록되고 > _[!UICONTROL Action Logs]_> 그리드에 반영됩니다&#x200B;**[!UICONTROL System].[!UICONTROL Report]**

| 형 | 액션 |
| ---- | ------- |
| 수입 | <ul><li>관리자 사용자가 가져오기를 실행합니다.<li>관리자가 가져온 파일을 다운로드합니다.<li>관리자 사용자가 오류 파일을 다운로드합니다<ul/> |
| 내보내기 | <ul><li>관리자 사용자 요청<li>관리자 사용자가 내보낸 파일을 다운로드합니다<ul/> |
| 예약된 가져오기/내보내기 | <ul><li>관리자 사용자가 내보내기 일정 예약<li>관리자가 예약된 내보내기를 편집합니다.<li>관리자 사용자가 예약된 내보내기를 실행합니다.<li>관리자 사용자가 예약된 내보내기를 삭제합니다.<li>관리자 사용자가 가져오기를 예약합니다.<li>관리자가 예약된 가져오기를 편집합니다.<li>관리자 사용자가 예약된 가져오기를 실행합니다.<li>관리자 사용자가 예약된 가져오기를 삭제합니다.<li>관리자 사용자가 가져오기/내보내기 작업의 일괄 삭제를 실행합니다.<ul/> |

### 향상된 표시 기능 및 향상된 필터링 및 정렬

관리 사용자에게 보다 유용한 그리드를 제공할 수 있도록 HIPAA 지원 서비스에서는 데이터를 표시, 필터링 및 정렬할 수 있는 몇 가지 개선 사항을 제공합니다.

#### 가져오기 기록([!UICONTROL System] > _[!UICONTROL Data Transfer]_> [!UICONTROL Import History])

- **[!UICONTROL Imported File]**, **[!UICONTROL Error File]**, **[!UICONTROL Execution Time]** 및 **[!UICONTROL Summary]**&#x200B;을(를) 제외한 모든 열에 대해 필터링을 사용하도록 설정했습니다.

#### 내보내기([!UICONTROL System] > _[!UICONTROL Data Transfer]_> [!UICONTROL Export])

- **[!UICONTROL ID]** 열이 추가되었습니다.
- **[!UICONTROL Requested At]** 열이 추가되었습니다(_내보내기가 요청된 날짜 및 시간_).
- **[!UICONTROL User]** 열(_요청을 수행한 관리자의 사용자 이름_)을 추가했습니다.
- **[!UICONTROL Action]** 열을 제거했습니다.
- **[!UICONTROL Download]** 링크를 **[!UICONTROL File name]** 열로 이동했습니다(_가져오기 기록 표_&#x200B;와 같이).
- 내보낸 파일의 삭제를 담당하는 작업을 사용하지 않도록 설정했습니다(_추적을 개선하려면_).
- **[!UICONTROL File name]**&#x200B;을(를) 제외한 모든 열에 대해 정렬을 사용하도록 설정했습니다.
- 모든 열에 대해 필터링을 사용하도록 설정했습니다.

#### 예약된 가져오기 및 내보내기([!UICONTROL System] > _[!UICONTROL Data Transfer]_> [!UICONTROL Scheduled Import/Export])

- **[!UICONTROL ID]** 열이 추가되었습니다.
- **[!UICONTROL Scheduled At]** 열(가져오기 또는 내보내기가 예약된 _날짜 및 시간_)이 추가되었습니다.
- **[!UICONTROL User]** 열(가져오기 또는 내보내기를 예약한 관리자의 _사용자 이름_)을 추가했습니다.

## HIPAA 지원 서비스 및 도구

이 섹션에서는 Adobe Commerce용 HIPAA 서비스와 함께 사용할 수 있는 HIPAA 준비 Adobe 서비스에 대해 설명합니다. 또한 스토어에 대한 주요 보안 및 규정 준수 제어를 모니터링하는 데 도움이 되는 도구를 설명합니다.

| 서비스 | 프로덕션 | 스테이징 | staging_for_support | 개발 |
|---------------------------------------|------------|---------|---------------------|-------------|
| Adobe Commerce 및 의료 추가 기능 | 예 | 예 | 예 | 아니요 |
| SendGrid | 아니요 | 아니요 | 아니요 | 아니요 |
| AWS Simple Email Service | 예 | 예 | 예 | 아니요 |

### Adobe Commerce 서비스

다음 표에는 HIPAA 준비 서비스에 사용할 수 있는 Adobe Systems Commerce 서비스가 나와 있습니다. 이러한 서비스에는 다음이 포함되지만 이에 국한되지 않습니다.

| 서비스 | 비프로덕션 | 프로덕션 |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------|------------|
| [Adobe Developer App Builder](https://developer.adobe.com/app-builder/docs/overview/) | 예 | 예 |
| Adobe Developer App Builder용 [API Mesh](https://developer.adobe.com/graphql-mesh-gateway/) | 예 | 예 |
| [SaaS 데이터 내보내기](https://experienceleague.adobe.com/en/docs/commerce/saas-data-export/overview) | 예 | 예 |
| [실시간 검색](https://experienceleague.adobe.com/en/docs/commerce/live-search/overview) | 아니요 | 아니요 |
| [제품 추천](https://experienceleague.adobe.com/en/docs/commerce/product-recommendations/overview) | 아니요 | 아니요 |
| [결제 서비스](https://experienceleague.adobe.com/en/docs/commerce/payment-services/guide-overview) | 아니요 | 아니요 |
| [다시 Office 이벤트에 데이터 연결](https://experienceleague.adobe.com/en/docs/commerce/data-connection/event-forwarding/events-backoffice) | 예 | 예 |
| [데이터 연결 상점 이벤트](https://experienceleague.adobe.com/en/docs/commerce/data-connection/event-forwarding/events#storefront-events) | 아니요 | 아니요 |
| [Audience Activation](https://experienceleague.adobe.com/en/docs/commerce-admin/customers/audience-activation) | 아니요 | 아니요 |

### 도구

Adobe Commerce용 [보안 검색 도구](../../systems/security-scan.md)를 사용하면 스토어를 모니터링하여 필요한 모든 보안 컨트롤이 활성화되어 작동하는지 확인할 수 있습니다. Adobe은 표준 보안 검사 외에도 Adobe Commerce용 HIPAA 서비스를 사용하는 고객에 대한 HIPAA 관련 검사를 표시하도록 도구를 개선했습니다. 보안 검색 도구의 HIPAA 검사는 다음을 보장하도록 설계되었습니다.

- 감사 모듈이 비활성화되지 않음
- 이중 인증(2FA)이 비활성화되지 않음
- 마케팅 기능이 비활성화됨
- 허용 목록에 추가하다 설치된 모든 확장은 사전 정의된 확장과 일치합니다.
- 지원되지 않는 Adobe 서비스가 설치되지 않았습니다.

예약된 검사 또는 [수동으로 보고서를 보기](https://experienceleague.adobe.com/en/docs/commerce-cloud-service/user-guide/launch/overview#to-review-the-report)의 세부 정보를 사용하여 전자 메일 알림을 보내도록 [도구를 구성](../../systems/security-scan.md#run-a-security-scan)할 수 있습니다.

## 비활성화된 기능

HIPAA 요구 사항을 준수하기 위해 Adobe Commerce에서 지원하는 일부 기능은 사용할 수 없거나 기본적으로 비활성화되어 있습니다. 판매자는 이러한 기능을 다시 활성화하거나 위험을 감수하고 사용할 수 있습니다.

다음 기능은 HIPAA 준비 모듈에서 기본적으로 비활성화됩니다. 판매자는 자신의 책임으로 이러한 기능을 사용할 수 있습니다.

- **[트랜잭션 전자 메일](https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/project/sendgrid.html)**—서비스가 HIPAA를 사용할 수 없으므로 SendGrid가 기본적으로 비활성화됩니다. Adobe Commerce은 [AWS 간단한 이메일 서비스](https://docs.aws.amazon.com/ses/) 계정과 함께 사용할 수 있는 통합 옵션을 제공합니다. 구성에 대한 자세한 내용은 고객 기술 계정 관리자 또는 Adobe Commerce 지원 센터에 문의하십시오.

- **[게스트 체크아웃](../../stores-purchase/checkout-guest.md)**—이 기능은 로깅, 액세스 제어, PHI 위생 및 계보 등을 포함하여 HIPAA의 다양한 측면에 대한 잠재적인 위험을 제공합니다.

- **[뉴스레터 기능](../../merchandising-promotions/newsletters.md)**—마케팅 컨텍스트에서 PHI가 사용되지 않도록 이 기능을 사용하지 않습니다.

- **[고급 보고 서비스 설정](../../getting-started/business-intelligence.md)**—분석 및 보고에 PHI를 사용하지 않도록 이 구성 설정을 사용하지 않습니다.
