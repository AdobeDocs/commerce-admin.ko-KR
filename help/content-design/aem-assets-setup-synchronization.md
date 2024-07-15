---
title: 동기화 서비스 설정
description: "Adobe Commerce 및 Experience Manager Assets 프로젝트를 Assets 규칙 엔진 서비스와 연결하여 이 두 시스템 간에 에셋 동기화를 활성화하는 방법에 대해 알아봅니다."
feature: CMS, Media
source-git-commit: 939fa5caeeb7a8913457c3492484362a1d3471be
workflow-type: tm+mt
source-wordcount: '1309'
ht-degree: 0%

---


# 동기화 서비스 설정

ARES(Asset Rules Engine Service)는 AEM Assets과 Adobe Commerce을 통합하는 다중 테넌트 서비스입니다. 이 서비스는 Adobe Commerce과 Experience Manager 간의 자산을 동기화합니다. ARES 서비스는 SKU 또는 기타 주요 속성을 기반으로 AEM의 에셋과 Adobe Commerce의 제품을 자동으로 일치시킵니다. 또한 최신 제품 에셋 및 변형을 전자 상거래 사이트에서 항상 사용할 수 있도록 합니다.

서비스를 설정하려면 ARES GraphQL API를 사용하여 테넌트 ID를 등록하고 에셋 동기화를 위한 일치 규칙을 선택해야 합니다.

## 일치하는 전략 선택

Commerce용 AEM Assets 통합은 Adobe Commerce과 AEM Assets 간에 자산을 동기화하는 두 가지 일치하는 전략을 지원합니다.

- **MatchBySku**-제품의 SKU(Stock Keeping Unit)에 따라 에셋과 일치하는 기본 일치 규칙입니다. SKU는 각 제품에 대한 고유 식별자입니다. 이 규칙은 에셋 메타데이터의 SKU를 Commerce 제품 SKU와 일치시켜 에셋이 올바른 제품과 연결되었는지 확인합니다.

- **ExternalMatcher**-이 일치 규칙은 사용자 지정 일치 논리를 필요로 하는 더 복잡한 시나리오 또는 특정 비즈니스 요구 사항을 위한 것입니다. 이 규칙을 사용하려면 Adobe Developer App Builder에서 자산과 제품의 일치 방법을 정의하는 사용자 지정 코드가 구현되어야 합니다.

초기 온보딩의 경우 `MatchBySku` 전략을 사용하십시오. 필요한 경우 나중에 일치 전략을 변경할 수 있습니다.

## 테넌트 등록

>[!BEGINSHADEBOX]

**필수 구성 요소**

- [자산 매핑에 필요한 Commerce 메타데이터로 AEM Assets 프로젝트가 구성되었습니다](aem-assets-configure-aem.md).

- [Adobe Commerce에서 Experience Manager Assets 통합 설치 및 구성](aem-assets-configure-commerce.md).

>[!ENDSHADEBOX]

## 자격 증명 수집

Commerce 프로젝트 환경 및 AEM Assets 프로젝트 환경을 Commerce SaaS 서비스와 인증하고 연결하려면 다음 자격 증명이 필요합니다.

| 필수 데이터 | Source | 찾을 수 있는 위치 |
| ---------- | ------ | ------------- |
| Magento 계정의 API 키 | Commerce | 스테이징 또는 프로덕션을 사용 중인 Commerce 환경에 대한 공개 API 키를 제공합니다. [관리]의 [Commerce Service Connector 설정](aem-assets-configure-commerce.md#configure-the-commerce-services-connector) 페이지 또는 [!UICONTROL API Portal] 섹션의 [!UICONTROL My Account] 페이지에서 프로덕션 및 스테이징 환경에 대한 API 키를 찾을 수 있습니다. |
| Commerce SaaS 프로젝트 식별자 <ul><li>`magento-environment-Id`</li><li>`Project ID`</li></ul> | Commerce 관리자 | 이러한 값은 연결할 Commerce 환경 및 SaaS 데이터 공간과 프로젝트를 식별합니다. 값은 [Commerce 서비스 커넥터 SaaS 식별자 구성](aem-assets-configure-commerce.md#configure-the-commerce-services-connector)에서 가져옵니다. |
| AEM `programId` 및<br>`environmentId` | [AEM Assets 작성 환경](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/sites/authoring/quick-start) | AEM Sites 페이지를 열고 **[!UICONTROL Assets]**&#x200B;을(를) 선택합니다.  URL <br>`https://author-p[Program ID]-e[EnvironmentID].adobeaemcloud.com/`에서 프로젝트 및 환경 ID 복사 |
| baseURL | Commerce 상점 | Commerce 상점 첫 화면의 [기본 URL](../stores-purchase/store-urls.md). |
| API 액세스에 대한 OAuth 자격 증명 | Commerce 관리자 | 이러한 자격 증명은 Commerce [Assets 통합에 대한 구성 설정](aem-assets-configure-commerce.md#experience-manager-assets-integration-for-adobe-commerce-10-release)에서 찾을 수 있습니다. |

## 임차인 등록

Assets 규칙 엔진 서비스에 인증 자격 증명 및 테넌트 ID 추가 요청을 제출하여 테넌트 등록을 완료합니다. 요청에는 서비스, Commerce 프로젝트 및 Experience Manager Assets 프로젝트 간의 연결을 설정하는 데 필요한 자격 증명과 프로젝트 식별자가 포함되어 있습니다.

GraphQL 클라이언트 또는 cURL을 사용하여 요청을 보냅니다.

>[!BEGINTABS]

>[!TAB GraphQL 요청]

GraphQL 클라이언트를 사용하여 API 끝점 `https://commerce.adobe.io/assets-integration/graphql`에 POST 요청을 보냅니다.

**필수 헤더**

요청에 대해 다음 HTTP 헤더를 지정합니다.

- `x-api-key`: Magento 계정의 API 키
- `magento-environment-Id`: SaaS 식별자
- `x-gw-signature`: MAGEID와 연결된 JWT 토큰

**요청:**

**구문**

```graphql
mutation registerTenant($tenantInput: TenantInput!) {
   registerTenant(tenantInput: $tenantInput) {
      tenantId
      userErrors {
         message
         path
      }
    }
}
```

**사용 예시**

테넌트를 등록하고 `matchBySku` 규칙을 선택하여 Adobe Commerce과 AEM Assets 프로젝트 간에 에셋을 매핑합니다.

**요청:**

```graphql
   {
      "tenantInput": {
         "enabled": true,
         "projectId": "8231afb6-90cd-65e8-84ba-d9abac0f94e6",
         "aem": {
               "programId": "11111",
               "environmentId": "222222"
         },
         "commerce": {
               "baseUrl": "***",
               "credentials": {
                  "consumerKey": "***",
                  "consumerSecret": "***",
                  "accessToken": "***",
                  "accessTokenSecret": "***"
               }
         },
         "rule": {
            "type": "matchBySKU"
            "matchBySkuRule": {
               "metadataField": "commerce:skus"
            }
         }
      }
   }
```

**응답**

```graphql
{
    "data": {
        "registerTenant": {
            "tenantId": "b65d5da7-2756-46a1-9ff1-14fb5d925fee",
            "userErrors": []
        }
    }
}
```

>[!TAB cURL 요청]

```shell
curl --request POST \
  --url https://commerce.adobe.io/assets-integration/graphql \
  --header 'Content-Type: application/json' \
  --header 'Magento-Environment-Id: ****' \
  --header 'x-api-key: ****' \
  --header 'x-gw-signature: *****' \
  --data '{"query":"mutation registerTenant($tenantInput: TenantInput!) {\n\tregisterTenant(tenantInput: $tenantInput) {\n\t\ttenantId\n\t\tuserErrors {\n\t\t\tmessage\n\t\t\tpath\n\t\t}\n\t}\n}\n","operationName":"registerTenant","variables":{"tenantInput":{"enabled":true,"threshold":100,"projectId":"5d6faa03-e200-4623-9008-da144e4eefd8","aem":{"programId":"***","environmentId":"***"},"commerce":{"version":"2.4.6-p2","extensionVersion":"0.0.1","baseUrl":"***","credentials":{"consumerKey":"***","consumerSecret":"***","accessToken":"***","accessTokenSecret":"***"}},"rule":{"type":"matchBySKU","matchBySkuRule":{"metadataField":"commerce:skus"}}}}}'
```

>[!ENDTABS]

### 입력 필드

#### AemInput

Commerce 에셋을 저장하기 위한 AEM Assets 인스턴스를 식별합니다. 이 정보는 Cloud Manager 내 프로그램 보기 또는 컨텐츠 작성 URL에서 가져올 수 있습니다.

| 필드 | 데이터 유형 | 설명 |
| ----- | --------- | ----------- |
| `programId` | 문자열! | AEM Cloud Service 내 프로젝트의 고유 식별자 |
| `environmentId` | 문자열! | 프로덕션, 스테이징 또는 개발 등 사용 중인 프로젝트 환경의 ID |

#### CommerceInput

이 입력 필드는 Commerce 카탈로그에 대한 API 액세스에 대한 OAuth 인증 자격 증명을 제공합니다. 이러한 자격 증명은 Commerce [Assets 통합에 대한 구성 설정](aem-assets-configure-commerce.md#experience-manager-assets-integration-for-adobe-commerce-10-release)에서 찾을 수 있습니다.

| 필드 | 데이터 유형 | 설명 |
| ----- | --------- | ----------- |
| `baseUrl` | 문자열 | Commerce 상점 첫 화면의 [기본 URL](../stores-purchase/store-urls.md). |
| `credentials` | [CommerceCredentialsInput](#commercecredentialsinput) | Commerce 인스턴스에 액세스할 자격 증명을 지정합니다. |
| `extensionVersion` | 문자열 | 선택 사항입니다. Commerce 인스턴스에 설치된 Commerce 확장용 AEM Assets 통합 버전입니다. |
| `version` | 문자열 | 선택 사항입니다. Commerce 인스턴스에 설치된 Commerce 애플리케이션 버전입니다. |

#### CommerceCredentialInput

이 입력 필드는 Commerce 카탈로그에 대한 API 액세스에 대한 OAuth 자격 증명을 제공합니다. 이러한 자격 증명은 Commerce [Assets 통합에 대한 구성 설정](aem-assets-configure-commerce.md#experience-manager-assets-integration-for-adobe-commerce-10-release)에서 찾을 수 있습니다.

| 필드 | 데이터 유형 | 설명 |
| ----- | --------- | ----------- |
| `accessToken` | 문자열! | Assets 통합을 위해 생성된 액세스 토큰입니다. |
| `accessTokenSecret` | 문자열! | Assets 통합을 위해 생성된 액세스 토큰 암호입니다. |
| `consumerKey` | 문자열! | Assets 통합을 위해 생성된 소비자 키입니다. |
| `consumerSecret` | 문자열! | Assets 통합을 위해 생성된 소비자 암호입니다. |

#### 외부 일치 항목 입력

| 필드 | 데이터 유형 | 설명 |
| ----- | --------- | ----------- |
| assetToProductUrl | 문자열! | <!--Add field description--> |
| productToAssetUrl | 문자열! | <!--Add field description--> |
| 자격 증명 | [ExternalMatcherCredentialsInput](#externalmatchercredentials) | Commerce용 AEM Assets 통합을 위한 App Builder 프로젝트에 액세스하기 위한 자격 증명입니다. |

#### 외부 일치 자격 증명

| 필드 | 데이터 유형 | 설명 |
| ----- | --------- | ----------- |
| `oauthServerUrl` | 문자열! |    |
| `clientId` | 문자열! |      |
| `clientSecret` | 문자열! |    |
| `imsOrgId` | 문자열! | AEM Assets 및 Adobe Commerce이 프로비저닝되는 IMS 조직. |

#### MatchBySkuRuleInput

| 필드 | 데이터 유형 | 설명 |
| ----- | --------- | ----------- |
| metadataField | 문자열! | 일치에 사용할 에셋 메타데이터 필드를 지정합니다. `commerce:skus` 사용 |

#### RuleInput

Adobe Commerce과 AEM Assets 간에 자산을 동기화하는 데 사용할 일치 규칙을 지정합니다.

| 필드 | 데이터 유형 | 설명 |
| ----- | --------- | ----------- |
| 외부 일치 | [ExternalMatcherInput](#externalmatcherinput) | 에셋 일치를 위해 externalMatcher 규칙을 선택하고 이 규칙을 사용하는 데 필요한 데이터를 지정합니다. |
| MatchBySkuRule | [MatchBySkuRuleInput](#matchbyskuruleinput) | 자산 일치를 위해 MatchBySkuRule을 선택하고 이 규칙을 사용하는 데 필요한 데이터를 지정합니다. |

#### RuleTypeInput

| 필드 | 데이터 유형 | 설명 |
| ----- | --------- | ----------- |
| 규칙 유형 | enum | Commerce용 AEM Assets 통합에 사용할 수 있는 자산 일치 규칙 목록을 지정합니다. 사용 가능한 값은 `matchBySKU` 또는 `externalMatcher`입니다. |

#### TenantInput

| 필드 | 데이터 유형 | 설명 |
| ----- | --------- | ----------- |
| `aem` | [AemInput!](#aeminput) | Commerce 에셋을 저장하는 AEM Cloud Service 내에서 AEM Assets 인스턴스를 식별합니다. |
| `commerce` | [CommerceInput!](#commerceinput) | API 액세스를 위한 Commerce 프로젝트 정보 및 자격 증명 제공 |
| `enabled` | 부울! | Adobe Commerce과 AEM Assets 간의 에셋 동기화를 활성화하거나 비활성화합니다. |
| `projectId` | 문자열! | [Commerce 서비스 커넥터 SaaS 식별자 구성](aem-assets-configure-commerce.md#configure-the-commerce-services-connector)의 SaaS 프로젝트 Id입니다. |
| `rule` | [RuleInput!](#ruleinput) | Adobe Commerce과 AEM Assets 간에 자산을 동기화하는 데 사용할 일치 규칙을 지정합니다. `[matchBySkuRule](#matchbyskuruleinput)` 또는 `[externalMatcher](#externalmatcherinput)`을(를) 지정하십시오. |

### 출력 필드

| 필드 | 데이터 유형 | 설명 |
| ----- | --------- | ----------- |
| 데이터 | [registerTenant] | 서버의 테넌트 등록 정보와 오류 메시지를 반환합니다. |

#### RegisterTenantResponse

| 필드 | 데이터 유형 | 설명 |
| ----- | --------- | ----------- |
| tenantId | 문자열! | 등록된 테넌트 ID를 반환합니다. 이 ID를 사용하면 Commerce용 AEM Assets 통합에 대한 데이터를 Commerce 환경과 연결된 SaaS 데이터 공간에서 저장하고 검색할 수 있습니다. |
| 사용자 오류 | [[사용자 오류!]!](#usererror) | 요청에서 생성된 모든 오류 메시지를 반환합니다. |

#### 사용자 오류

| 오류 | 설명 |
|:------|:------------|
| `IMS Org ID not associated to this Commerce` | 이 오류는 `Magento-Environment-Id` 헤더에 지정된 환경 ID가 IMS 계정에 할당되지 않은 경우에 발생합니다. 이 오류는 [Commerce 서비스 커넥터](aem-assets-configure-commerce.md#configure-the-commerce-services-connector)가 Commerce 인스턴스에 대해 구성된 경우 IMS 계정이 연결되지 않았기 때문에 발생할 수 있습니다. |
| `Client ID is invalid` | `x-api-key` 헤더가 잘못되었습니다. |
| `Client ID is missing` | `x-api-key` 헤더가 제공되지 않았습니다. |
| `JWT is required` | `x-gw-signature` 헤더가 제공되지 않았습니다. |
| `JWT is invalid` | `x-gw-signature` 헤더가 제공되지 않았습니다. |
| `Tenant already exists` | 지정된 `mageID`(JWT 토큰에서 가져옴) 및 `saasId`(`Magento-Environment-Id` 헤더에서 제공됨)을(를) 가진 테넌트가 이미 등록되었습니다. |
| `Unexpected error when connecting with AEM Assets` | 이 오류는 잘못되었거나 존재하지 않는 `programId` 또는 `environmentId` 값으로 인해 발생합니다. |
| `Unable to connect with AEM Assets` | 이 오류에는 두 가지 이유가 있습니다.<br>1. AEM 자산 계정이 Adobe Commerce에 대해 제공된 ID가 아닌 다른 IMS 조직 ID와 연결되어 있습니다.<br>2. `commerce:isCommerce` 메타데이터가 AEM Assets에 없으므로 AEM Assets에서 Commerce 인스턴스로 보낼 승인된 자산이 없습니다. |
| `Unexpected error when connecting with Commerce` | 이 오류는 잘못된 상거래 `baseURL`이(가) 제공되었을 때 발생합니다. |
| `Unable to connect with Commerce, unauthorized` | 잘못된 상거래 자격 증명이 제공되어 무단 액세스가 발생했습니다. |
| `Invalid rule. The value must be matchBySKU or externalMatcher` | `Rule` 필드에 잘못된 값이 있습니다. RegisterTenant 요청의 경우 사용 가능한 규칙 유형은 [RuleTypeInput](#ruletypeinput) 열거형으로 정의됩니다. |

## Experience Manager Assets 통합 활성화

테넌트를 등록한 후 온보딩 프로세스의 마지막 단계는 관리자에서 Commerce용 Experience Manager Assets 통합 확장을 활성화하는 것입니다.

1. 확장을 활성화합니다.

   1. **스토어** > 설정 > **구성** > **카탈로그**(으)로 이동합니다.

   1. **[!UICONTROL Catalog]**&#x200B;을(를) 선택하여 카탈로그 구성을 엽니다.

   1. **[!UICONTROL AEM Assets integration]** 확장.

   1. **[!UICONTROL Integration enabled]**&#x200B;을(를) `yes`(으)로 설정합니다.

      ![Commerce 관리자 구성을 위한 AEM Assets 통합](assets/aem-integration-admin-enable.png){width="600" zoomable="yes"}
