---
title: Adobe Commerce의 HIPAA 준비
description: Adobe Commerce HIPAA 지원 확장 기능을 추가하여 HIPAA 규정 준수를 지원할 수 있는 추가 기능을 사용하는 방법에 대해 알아봅니다.
feature: Security, Compliance
exl-id: 4b3eb5b0-4475-47df-92a9-10d12fec1e66
source-git-commit: bce0e581e89139875e09b671038a21976eccebca
workflow-type: tm+mt
source-wordcount: '1568'
ht-degree: 1%

---

# Adobe Commerce의 HIPAA 준비

>[!IMPORTANT]
>
>**법적 고지 사항**<br/>
>이 정보는 Adobe 고객이 Adobe의 HIPAA 지원 서비스에 대한 질문에 답변할 수 있도록 돕기 위한 것입니다. 그것은 법률적인 조언이 되지 않는다. 상인은 HIPAA에 따른 의무와 Adobe 제품의 적절한 사용 및 구성을 이해하기 위해 자체 법률 자문과 상담해야 합니다.

>[!BEGINSHADEBOX]

**건강보험 양도 및 책임에 관한 법률(HIPAA)**

HIPAA(Health Insurance Portability and Accountability Act)는 미국의 주요 연방 의료 개인 정보 보호법이며 미국 보건복지부(HHS)에서 시행합니다. HIPAA는 적용 대상&#x200B;_(예: 의료 서비스 제공자, 보험사 및 정보 센터) 및_&#x200B;비즈니스 어소시에이트&#x200B;_(예: 대상 기관에 서비스를 제공하는 기관)에 적용됩니다_. HIPAA 요구 사항은 개인 정보 보호 규칙, 보안 규칙 및 위반 알림 규칙의 세 가지 개별 규칙에 따라 설정됩니다. Adobe Systems는 Adobe Systems가 &quot;HIPAA-Ready 서비스&quot;로 분류하는 특정 제품에 대한 비즈니스 어소시에이트 역할을 합니다. HIPAA에 따라 규제되는 데이터를 보호된 건강 정보&#x200B;_또는 PHI라고_&#x200B;합니다. PHI는 (1) 의료 서비스 제공자, 건강 보험 또는 의료 정보 센터에서 생성하거나 수신하고, (2) 개인의 과거, 현재 또는 미래의 신체적 또는 정신적 건강 또는 상태, 개인에 대한 의료 서비스 제공, 또는 개인에 대한 의료 서비스 제공에 대한 과거, 현재 또는 미래의 지불과 관련된 건강 정보의 하위 집합입니다.  (3) 개인을 식별하거나 정보가 개인을 식별하는 데 사용될 수 있다고 믿을 만한 합리적인 근거가 있는 경우. HIPAA 개인 정보 보호 및 보안 규칙에 따라 적용 주체는 비즈니스 어소시에이트 계약(BAA)의 형태로 비즈니스 어소시에이트로부터 서면 보증을 받아야 하며, 이는 비즈니스 어소시에이트가 해당 엔터티의 PHI의 개인 정보 보호 및 보안을 보호하도록 요구합니다. 자세한 내용은 Adobe Systems Trust Center의 HIPAA 및 Adobe Systems Products and Services](https://www.adobe.com/trust/compliance/hipaa-ready.html)를 참조하십시오[.

>[!ENDSHADEBOX]

## Adobe Systems Commerce HIPAA 지원

Adobe Commerce HIPAA 지원 확장은 Adobe Commerce 설치에 상인이 각각의 HIPAA 의무를 준수할 수 있는 추가 기능 및 기능을 추가합니다.

Adobe Commerce HIPAA 지원 확장, `magento/hipaa-ee`은(는) 클라우드 인프라의 Adobe Commerce 또는 Managed Services 프로젝트 Adobe에 사용할 수 있습니다. Adobe Commerce HIPAA 준비 설치 프로세스는 HIPAA 요구 사항을 준수하기 위해 일부 기본 서비스 및 기능을 비활성화합니다. [비활성화된 서비스 및 기능](#disabled-services-and-features)을(를) 참조하십시오.

>[!NOTE]
>
>HIPAA 지원 기능 액세스는 Adobe Commerce용 의료 서비스 추가 기능을 구입한 판매자만 사용할 수 있습니다.

*이러한 자료는 정보 제공 목적으로만 작성되었습니다. 이 정보의 제공은 수취인에게 어떠한 계약상의 권리나 다른 권리에 대한 자격을 부여하지 않는다. 제공된 날짜 현재 정보의 정확성을 보장하기 위해 노력했지만, 그러한 정보가 정확하고 완전하다는 표현은 하지 않습니다. Adobe은 법률 또는 Adobe의 제품이 변경될 때 이 정보를 업데이트할 의무가 없습니다. 또한 이 문서는 Adobe의 서면 동의 없이 의도한 수신자가 아닌 다른 사람에게 배포되지 않습니다.*

## 시스템 요구 사항

Adobe Commerce은 버전 2.4.6-p3 이상(베타 버전 없음)의 Adobe Commerce Managed Services 또는 클라우드 인프라의 Adobe Commerce에 배포해야 합니다.

## 설치

**필수 구성 요소**

>[!BEGINSHADEBOX]

- Adobe이 HIPAA 준비 확장에 액세스할 수 있도록 Adobe Commerce 계정을 프로비저닝했습니다.
- 확장을 설치하려면 [repo.magento.com](https://repo.magento.com)에 액세스하십시오. 키를 생성하고 필요한 권한을 얻으려면 [인증 키 가져오기](https://experienceleague.adobe.com/docs/commerce-operations/installation-guide/prerequisites/authentication-keys.html)를 참조하십시오.

>[!ENDSHADEBOX]

Adobe Commerce 버전 2.4.6-p3 이상을 실행 중인 인스턴스에 최신 버전의 Adobe HIPAA 지원 서비스 확장(`magento/hipaa-ee`)을 설치합니다. 확장은 [repo.magento.com](https://repo.magento.com) 리포지토리에서 작성기 메타패키지로 전달됩니다. 메타패키지에는 Adobe Commerce 인스턴스에 대해 HIPAA 기능을 활성화하는 모듈 컬렉션이 포함되어 있습니다.

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

1. 업데이트된 코드를 클라우드 환경에 추가, 커밋 및 푸시합니다.

   ```shell
   git add -A
   git commit -m "Add HIPAA-Ready Services modules"
   git push origin <branch-name>
   ```

   업데이트를 푸시하면 [Commerce 클라우드 배포 프로세스](https://experienceleague.adobe.com/en/docs/commerce-cloud-service/user-guide/develop/deploy/process)가 시작되어 변경 내용을 적용합니다. [배포 로그](https://experienceleague.adobe.com/en/docs/commerce-cloud-service/user-guide/develop/test/log-locations#deploy-log)에서 배포 상태를 확인하십시오.

### 설치 확인

업데이트가 배포된 후 extensiion이 `Hipaa*` 설치되어 있는지 확인합니다

1. SSH를 사용하여 원격 클라우드 환경에 로그인합니다.

   ```shell
   magento-cloud ssh
   ```

1. 명령줄에서 Adobe Systems Commerce CLI를 사용하여 모듈 상태를 확인합니다.

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

   `Magento_Hipaa` 접두사가 있는 모든 모듈은 사용 가능한 모듈 섹션에 있어야 합니다.

## HIPAA 준비를 위한 기능 개선 사항

`magento/hipaa-ee` 확장은 기본 Commerce 제품에 몇 가지 변경 사항 및 개선 사항을 도입했습니다. 다음 섹션은 이러한 변경 사항과 기본 제품을 변경하는 방법에 대한 세부 정보를 제공합니다.

### 작업 로그

감사 로깅은 HIPAA 요구 사항입니다. Adobe Commerce에서 [작업 로그](https://experienceleague.adobe.com/docs/commerce-admin/systems/action-logs/action-log.html?lang=en) 기능은 스토어에서 작업하는 관리자가 수행한 모든 변경 사항을 기록합니다. 감사 로그에 대한 HIPAA 요구 사항을 충족하기 위해 관리 UI 및 API 호출을 통해 수행된 모든 관리 사용자 및 고객 작업을 기록하도록 기능이 업데이트되었습니다.

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

### 가져오기 및 내보내기 기능

가져오기 및 내보내기 기능에 대한 향상된 기능은 관리 경험 환경을 개선하고 사용자 작업에 대한 더 나은 가시성을 제공하는 데 중점을 둡니다.

>[!NOTE]
>
>이러한 ***향상된 기능은 가져오기 및 내보내기 핵심 논리***&#x200B;를 변경하지 않고 기능을 확장하여 보다 포괄적인 로깅 및 향상된 데이터 기여도 분석 제공합니다. 가져오기 및 내보내기의 기본 기능은 변경되지 않습니다. 사용자는 기존 기능과 워크플로우를 중단 없이 계속 사용할 수 있습니다.

#### 관리 조치 로깅

가져오기 및 내보내기 기능의 주요 개선 사항 중 하나는 관리 작업의 향상된 로깅 기능입니다. 이 향상된 기능은 데이터 가져오기 및 내보내기와 관련된 활동을 자세히 분석하는 기능을 도입하여 추적 및 감사 기능을 개선하는 데 기여합니다. 이제 다음 작업이 기록되고 > _[!UICONTROL Action Logs]_> 그리드에 반영됩니다&#x200B;**[!UICONTROL System].[!UICONTROL Report]**

| 유형 | 작업 |
| ---- | ------- |
| 가져오기 | <ul><li>관리자 사용자가 가져오기를 실행합니다.<li>관리자가 가져온 파일을 다운로드합니다.<li>관리자 사용자가 오류 파일을 다운로드합니다<ul/> |
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

## 비활성화된 서비스 및 기능

HIPAA 요구 사항을 준수하기 위해 Adobe Commerce에서 지원하는 일부 서비스 및 기능은 사용할 수 없거나 기본적으로 비활성화되어 있습니다. 판매자는 이러한 서비스와 기능을 자신의 책임하에 다시 활성화하거나 사용할 수 있는 옵션을 가지고 있습니다.

### 서비스

- **Adobe Commerce 서비스**—HIPAA 준비 제공 서비스에서는 Adobe Commerce 서비스 또는 확장성 서비스를 사용할 수 없습니다. 이러한 서비스에는 다음이 포함되지만 이에 국한되지 않습니다.

   - 실시간 검색
   - API 메시
   - 앱 빌더

- **[SendGrid 서비스](https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/project/sendgrid.html)**—응용 프로그램이 HIPAA를 준수하지 않으므로 이 서비스는 기본적으로 사용하지 않도록 설정됩니다.

### 기본적으로 비활성화된 기능

다음 기능은 HIPAA 준비 모듈에서 기본적으로 비활성화됩니다. 판매자는 자신의 책임으로 이러한 기능을 사용할 수 있습니다.

- **[게스트 체크아웃](../stores-purchase/checkout-guest.md)**—이 기능은 로깅, 액세스 제어, PHI 위생 및 계보 등을 포함하여 HIPAA의 다양한 측면에 대한 잠재적인 위험을 제공합니다.

- **[뉴스레터 기능](../merchandising-promotions/newsletters.md)**—마케팅 컨텍스트에서 PHI가 사용되지 않도록 이 기능을 사용하지 않습니다.

- **[고급 보고 서비스 설정](../getting-started/business-intelligence.md)**— 분석 및 보고에 PHI를 사용하지 않도록 이 구성 설정을 사용하지 않습니다.
