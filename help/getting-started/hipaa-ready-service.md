---
title: Adobe Commerce의 HIPAA 준비
description: Adobe Commerce HIPAA 준비 모듈을 추가하고 HIPAA 의무를 준수할 수 있는 추가 기능 및 기능을 얻는 방법에 대해 알아봅니다.
feature: Security, Compliance
exl-id: 4b3eb5b0-4475-47df-92a9-10d12fec1e66
source-git-commit: 7e132d66523feba579baf0bae14e1de9de4d6591
workflow-type: tm+mt
source-wordcount: '1542'
ht-degree: 0%

---

# Adobe Commerce의 HIPAA 준비

>[!IMPORTANT]
>
>**법적 면책 조항**<br/>
>이 정보는 Adobe 고객이 Adobe의 HIPAA 지원 서비스에 대한 질문에 답변할 수 있도록 돕기 위한 것입니다. 그것은 법률적인 조언이 되지 않는다. 상인은 HIPAA에 따른 의무와 Adobe 제품의 적절한 사용 및 구성을 이해하기 위해 자체 법률 자문과 상담해야 합니다.

>[!BEGINSHADEBOX]

**건강 보험 이동성 및 책임에 관한 법률(HIPAA)**

HIPAA(Health Insurance Portability and Accountability Act)는 미국의 주요 연방 의료 개인정보 보호법이며 미국 보건복지부(HHS)에서 시행하고 있습니다. HIPAA 적용 대상 _포함된 엔티티_ (의료 기관, 보험사, 청산 주택 등) 및 _비즈니스 어소시에이츠_ (적용 엔티티에 서비스를 제공하는 엔티티 등). HIPAA 요구 사항은 개인 정보 보호 규칙, 보안 규칙 및 위반 알림 규칙의 세 가지 규칙에 따라 설정됩니다. Adobe은 특정 제품에 대해 비즈니스 동료 역할을 하며, Adobe은 이를 &quot;HIPAA 준비 서비스&quot;로 분류합니다. HIPAA에 의해 규제되는 데이터는 다음과 같습니다. _보호된 상태 정보_ 또는 PHI입니다. PHI는 (1) 의료 제공자, 의료 계획 또는 의료 정보 교환소가 생성 또는 수신하는 건강 정보의 하위 집합이며, (2) 개인의 과거, 현재 또는 미래의 신체적 또는 정신적 건강 또는 상태, 개인에 대한 의료 서비스 제공 또는 개인에 대한 의료 서비스 제공에 대한 과거, 현재 또는 미래 지불에 관한 것이고, (3) 개인을 식별하거나 해당 정보가 개인을 식별하는 데 사용될 수 있다고 믿을 수 있는 합리적인 근거가 있는 것입니다. HIPAA 개인 정보 보호 및 보안 규칙은 피보험 기업이 비즈니스 관련 계약 또는 BAA의 형태로 비즈니스 관계자로부터 서면 보증을 받도록 요구하여 비즈니스 관련자가 피보험 기업의 ʼ PHI의 개인 정보 보호 및 보안을 보호하도록 요구합니다. 자세한 내용은 [HIPAA 및 Adobe 제품 및 서비스](https://www.adobe.com/trust/compliance/hipaa-ready.html) Adobe 트러스트 센터에서 확인하십시오.

>[!ENDSHADEBOX]

## Adobe Commerce HIPAA 지원

Adobe Commerce HIPAA-Ready에는 상인이 각각의 HIPAA 의무를 준수할 수 있는 추가 기능 및 기능이 있습니다.

Adobe Commerce HIPAA 지원 은 Adobe Commerce 확장, `magento/hipaa-ee` 클라우드 인프라의 Adobe Commerce 또는 Adobe Managed Services 프로젝트에 사용할 수 있습니다. Adobe Commerce HIPAA 준비 설치 프로세스는 HIPAA 요구 사항을 준수하기 위해 일부 기본 서비스 및 기능을 비활성화합니다. 다음을 참조하십시오 [비활성화된 서비스 및 기능](#disabled-services-and-features).

*이러한 자료는 정보 제공 목적으로만 작성되었습니다. 이 정보의 제공은 수취인에게 어떠한 계약상의 권리나 다른 권리에 대한 자격을 부여하지 않는다. 제공된 날짜 현재 정보의 정확성을 보장하기 위해 노력했지만, 그러한 정보가 정확하고 완전하다는 표현은 하지 않습니다. Adobe은 법률 또는 Adobe의 제품이 변경될 때 이 정보를 업데이트할 의무가 없습니다. 또한 본 문서는 Adobe의 서면 동의 없이 의도한 수신자 이외의 당사자에게 배포되지 않습니다.*

## 시스템 요구 사항

Adobe Commerce은 버전 2.4.6-p3 이상(베타 버전 없음)의 Adobe Commerce Managed Services 또는 클라우드 인프라의 Adobe Commerce에 배포해야 합니다.

## 설치

최신 버전의 Adobe의 HIPAA 준비 서비스 확장(`magento/hipaa-ee`) Adobe Commerce 버전 2.4.6-p3 이상을 실행 중인 인스턴스에서 확장은 다음에서 작성기 메타패키지로 전달됩니다. [repo.magento.com](https://repo.magento.com) 리포지토리.

>[!BEGINSHADEBOX]

**전제 조건**

다음에 대한 액세스 권한이 있어야 합니다. [repo.magento.com](https://repo.magento.com) 확장을 설치합니다. 키 생성 및 필요한 권한 획득에 대한 자세한 내용은 [인증 키 받기](https://experienceleague.adobe.com/docs/commerce-operations/installation-guide/prerequisites/authentication-keys.html).

>[!ENDSHADEBOX]

1. 로컬 워크스테이션에서 Adobe Commerce on cloud infrastructure 프로젝트의 프로젝트 디렉터리로 변경합니다.

   >[!NOTE]
   >
   >Commerce 프로젝트 환경을 로컬로 관리하는 방법에 대한 자세한 내용은  [CLI를 사용하여 분기 관리](https://experienceleague.adobe.com/en/docs/commerce-cloud-service/user-guide/develop/cli-branches) 다음에서 _Adobe Commerce on Cloud Infrastructure 사용 안내서_.

1. Adobe Commerce Cloud CLI를 사용하여 업데이트할 환경 분기를 체크아웃합니다.

   ```shell
   magento-cloud environment:checkout <environment-id>
   ```

1. 메타패키지 추가 `magento/hipaa-ee` composer CLI를 사용하여 composer 구성으로 변환

   ```shell
   composer require "magento/hipaa-ee" --no-update
   ```

1. 패키지 종속성을 업데이트합니다.

   ```shell
   composer update "magento/hipaa-ee"
   ```

1. 업데이트된 코드를 클라우드 환경에 추가, 커밋 및 푸시합니다.

   ```shell
   git add -A
   git commit -m "Add HIPAA-Ready Services modules"
   git push origin <branch-name>
   ```

   업데이트를 푸시하면 [Commerce 클라우드 배포 프로세스](https://experienceleague.adobe.com/en/docs/commerce-cloud-service/user-guide/develop/deploy/process) 를 눌러 변경 사항을 적용합니다. 에서 배포 상태를 확인합니다. [로그 배포](https://experienceleague.adobe.com/en/docs/commerce-cloud-service/user-guide/develop/test/log-locations#deploy-log).

### 설치 확인

업데이트가 배포된 후 다음을 확인합니다. `Hipaa*` 확장이 설치됨

1. SSH를 사용하여 원격 클라우드 환경에 로그인합니다.

   ```shell
   magento-cloud ssh
   ```

1. 명령줄에서 Adobe Commerce CLI를 사용하여 모듈 상태를 확인합니다.

   ```shell
   bin/magento module:status
   ```

1. 활성화된 모듈 목록에 HIPAA 모듈이 포함되어 있는지 확인합니다.

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
   <truncated for brevity>
   ```

   접두사가 있는 모든 모듈 `Magento_Hipaa` 은(는) 활성화된 모듈 섹션에 있어야 합니다.

## HIPAA 준비를 위한 기능 개선 사항

다음 `magento/hipaa-ee` 패키지는 기본 Commerce 제품에 대한 몇 가지 변경 사항 및 개선 사항을 도입했습니다. 다음 섹션은 이러한 변경 사항과 기본 제품을 변경하는 방법에 대한 세부 정보를 제공합니다.

### 작업 로그

감사 로깅은 HIPAA 요구 사항입니다. Adobe Commerce에서 [작업 로그](https://experienceleague.adobe.com/docs/commerce-admin/systems/action-logs/action-log.html?lang=en) 기능은 스토어에서 근무하는 관리 사용자가 수행한 모든 변경 사항을 기록합니다. 감사 로그에 대한 HIPAA 요구 사항을 충족하기 위해 관리 UI 및 API 호출을 통해 수행된 모든 관리 사용자 및 고객 작업을 기록하도록 기능이 업데이트되었습니다.

#### 작업 로그 보고서

다음 _작업 로그_ 보고서 그리드 (**[!UICONTROL System]** > 작업 로그 > 보고서)가 관리 UI 및 API를 통해 수행되는 고객 작업에 맞게 수정되었습니다.

1. 다음 두 개의 열이 추가되었습니다.
   - ***소스***: 작업이 수행된 위치를 표시합니다.
값: `Admin UI` / `Customer UI` / `REST API` / `SOAP API` / `GraphQL API`
   - ***클라이언트 유형***: 클라이언트 유형을 표시합니다.
값: 고객 | 관리자 | 통합

2. 이름이 변경됨 ***사용자 이름*** 열 위치: ***클라이언트 식별자***
   - ***클라이언트 식별자***: 작업을 수행한 사용자의 로그인 ID를 표시합니다.
값:
      - 클라이언트 유형이 고객인 경우 이메일
      - 클라이언트 유형이 관리자인 경우 사용자 이름
      - 클라이언트 유형이 통합인 경우 이름

3. 이름이 변경됨 ***전체 작업 이름*** 열 위치: ***Target***
   - ***Target***: 작업 이름을 표시합니다.
값:
      - 소스가 REST API 또는 SOAP API인 경우 엔드포인트
      - GraphQL API인 경우 쿼리 또는 돌연변이 이름
      - 관리 UI 또는 고객 UI인 경우 작업 이름입니다.

#### 로깅에 대한 관리 작업 구성

모든 작업을 기본적으로 기록해야 하므로 이 기능을 사용할 수 없습니다.

### 가져오기 및 내보내기 기능

가져오기 및 내보내기 기능의 개선 사항은 관리 경험을 개선하고 사용자 작업에 대한 더 나은 가시성을 제공하는 데 중점을 둡니다.

>[!NOTE]
>
>다음 ***개선 사항은 가져오기 및 내보내기 코어 논리를 변경하지 않습니다***&#x200B;오히려 기능을 확장하여 보다 포괄적인 로깅과 향상된 데이터 속성을 제공합니다. 수입과 수출의 기본 기능은 변함이 없습니다. 사용자는 중단 없이 기존 기능 및 워크플로를 계속 사용할 수 있습니다.

#### 관리 작업 로깅

가져오기 및 내보내기 기능의 주요 개선 사항 중 하나는 관리 작업의 로깅 향상입니다. 이 향상된 기능은 데이터 가져오기 및 내보내기와 관련된 활동을 자세히 분석하는 기능을 도입하여 추적 및 감사 기능을 개선하는 데 기여합니다. 이제 다음 작업이 기록되어 다음에 반영됩니다. **[!UICONTROL System]> _[!UICONTROL Action Logs]_>[!UICONTROL Report]**격자:

| 유형 | 작업 |
| ---- | ------- |
| 가져오기 | <ul><li>관리자 사용자가 가져오기를 실행합니다.<li>관리자가 가져온 파일을 다운로드합니다.<li>관리자 사용자가 오류 파일을 다운로드합니다<ul/> |
| 내보내기 | <ul><li>관리자 사용자 요청<li>관리자 사용자가 내보낸 파일을 다운로드합니다<ul/> |
| 예약된 가져오기/내보내기 | <ul><li>관리자 사용자가 내보내기 일정 예약<li>관리자가 예약된 내보내기를 편집합니다.<li>관리자 사용자가 예약된 내보내기를 실행합니다.<li>관리자 사용자가 예약된 내보내기를 삭제합니다.<li>관리자 사용자가 가져오기를 예약합니다.<li>관리자가 예약된 가져오기를 편집합니다.<li>관리자 사용자가 예약된 가져오기를 실행합니다.<li>관리자 사용자가 예약된 가져오기를 삭제합니다.<li>관리자 사용자가 가져오기/내보내기 작업의 일괄 삭제를 실행합니다.<ul/> |

### 향상된 표시 기능 및 향상된 필터링 및 정렬

관리 사용자에게 보다 유용한 그리드를 제공할 수 있도록 HIPAA 지원 서비스에서는 데이터를 표시, 필터링 및 정렬할 수 있는 몇 가지 개선 사항을 제공합니다.

#### 가져오기 기록([!UICONTROL System] > _[!UICONTROL Data Transfer]_> [!UICONTROL Import History])

- 을(를) 제외한 모든 열에 대해 필터링을 활성화했습니다. **[!UICONTROL Imported File]**, **[!UICONTROL Error File]**, **[!UICONTROL Execution Time]**, 및 **[!UICONTROL Summary]**.

#### 내보내기([!UICONTROL System] > _[!UICONTROL Data Transfer]_> [!UICONTROL Export])

- 을(를) 추가함 **[!UICONTROL ID]** 열.
- 을(를) 추가함 **[!UICONTROL Requested At]** 열 (_내보내기가 요청된 날짜 및 시간_).
- 을(를) 추가함 **[!UICONTROL User]** 열 (_요청을 수행한 관리자의 사용자 이름_).
- 을(를) 제거함 **[!UICONTROL Action]** 열.
- 이동함 **[!UICONTROL Download]** 에 대한 링크 **[!UICONTROL File name]** 열 (_가져오기 기록 그리드_).
- 내보낸 파일의 삭제를 담당하는 작업을 비활성화했습니다(_추적을 개선하려면_).
- 을(를) 제외한 모든 열에 대해 정렬을 활성화했습니다. **[!UICONTROL File name]**.
- 모든 열에 대해 필터링을 사용하도록 설정했습니다.

#### 예약된 가져오기 및 내보내기([!UICONTROL System] > _[!UICONTROL Data Transfer]_> [!UICONTROL Scheduled Import/Export])

- 을(를) 추가함 **[!UICONTROL ID]** 열.
- 을(를) 추가함 **[!UICONTROL Scheduled At]** 열 ( _가져오기 또는 내보내기가 예약된 날짜 및 시간_).
- 을(를) 추가함 **[!UICONTROL User]** 열 ( _가져오기 또는 내보내기를 예약한 관리자의 사용자 이름_).

## 비활성화된 서비스 및 기능

HIPAA 요구 사항을 준수하기 위해 Adobe Commerce에서 지원하는 일부 서비스 및 기능은 사용할 수 없거나 기본적으로 비활성화되어 있습니다. 판매자는 이러한 서비스와 기능을 자신의 책임하에 다시 활성화하거나 사용할 수 있는 옵션을 가지고 있습니다.

### 서비스

- **Adobe Commerce 서비스**—HIPAA 준비 서비스에서는 Adobe Commerce 서비스 또는 확장성 서비스를 사용할 수 없습니다. 이러한 서비스에는 다음이 포함되지만 이에 국한되지 않습니다.

   - 라이브 검색
   - API 메쉬
   - App Builder
   - 카탈로그 서비스

- **[SendGrid 서비스](https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/project/sendgrid.html)**—애플리케이션이 HIPAA를 준수하지 않으므로 이 서비스는 기본적으로 비활성화됩니다. 가맹점은 발송그리드를 활성화하기 위해 지원요청서를 제출할 수 있지만, 서비스 이용에 대한 위험을 감수하고 있다는 점을 인정해야 한다.

### 기본적으로 비활성화된 기능

다음 기능은 HIPAA 준비 모듈에서 기본적으로 비활성화됩니다. 판매자는 자신의 책임으로 이러한 기능을 사용할 수 있습니다.

- **[게스트 체크아웃](../stores-purchase/checkout-guest.md)**—이 기능은 로깅, 액세스 제어, PHI 위생 및 계보 등을 포함하여 HIPAA의 다양한 측면에 대한 잠재적 위험을 제공합니다.

- **[뉴스레터 기능](../merchandising-promotions/newsletters.md)**- 이 기능은 마케팅 컨텍스트에서 PHI가 사용되지 않도록 비활성화됩니다.

- **[고급 보고 서비스 설정](../getting-started/business-intelligence.md)**— PHI가 분석 및 보고에 사용되지 않도록 하기 위해 이 구성 설정을 사용할 수 없습니다.
