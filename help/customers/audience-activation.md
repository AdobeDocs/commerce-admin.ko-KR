---
title: '[!DNL Audience Activation]'
description: Adobe Commerce에서 Real-Time CDP 대상을 활성화하여 스토어에서 개인화를 추진하는 방법에 대해 알아봅니다.
exl-id: b53908f2-c0c1-42ad-bb9e-c762804a744b
feature: Customers, Configuration, Personalization
topic: Commerce, Personalization
level: Experienced
source-git-commit: 90c653684be644f876937dc7acbc8f72498c5e3b
workflow-type: tm+mt
source-wordcount: '1575'
ht-degree: 1%

---

# [!DNL Audience Activation]

[!DNL Audience Activation] 확장을 사용하면 Adobe Commerce에서 Real-Time CDP 대상을 활성화하여 장바구니에서 고유한 오퍼를 만들 수 있습니다. 이러한 오퍼 및 인센티브에는 _2개 구매 무료_&#x200B;와 같은 일반적인 전자 상거래 머천다이징 기술, 해당 고객에 맞게 구성된 영웅 배너 및 다양한 오퍼를 통한 수정된 제품 가격이 포함됩니다. Real-Time CDP에 구축된 대상은 ERP(전사적 자원 관리), CRM(고객 관계 관리), POS(판매 지점), 마케팅 시스템과 같은 다양한 엔터프라이즈 시스템의 데이터를 기반으로 합니다. 고객 세그먼트 정보는 지속적으로 새로 고쳐지기 때문에 고객은 스토어에서 쇼핑할 때 세그먼트와 연결 및 연결 해제될 수 있습니다.

Luma 상점 첫 화면 또는 [headless](#headless-support) 상점 첫 화면에서 대상을 활성화할 수 있습니다. Luma 상점 첫 화면에서 대상 정보(세그먼트 멤버십)는 Commerce 측의 쿠키에 저장됩니다. Headless 상점 앞에서는 대상 정보가 GraphQL API 헤더에 `aep-segments-membership` 매개 변수로 전달됩니다.

## 릴리스 정보

이 섹션에는 Audience Activation 확장 업데이트에 대한 정보가 포함되어 있으며 다음이 포함됩니다.

![새로운 기능](../assets/new.svg) - 새로운 기능
![수정](../assets/fix.svg) - 수정 사항 및 개선 사항
![버그](../assets/bug.svg) - 알려진 문제

릴리스 일정 및 지원에 대한 자세한 내용은 [예정된 릴리스](https://experienceleague.adobe.com/docs/commerce-operations/release/planning/schedule.html)를 참조하세요.

개발자 설명서를 참조하여 [제품 호환성에 대해 알아보세요](https://experienceleague.adobe.com/docs/commerce-operations/release/product-availability.html).

## 지원되는 서비스 업데이트

이러한 릴리스 노트는 Audience Activation에서 사용하는 확장과 관련된 기능 변경 사항 및 수정 사항에 대해 설명합니다.

+++지원되는 서비스 업데이트

_2023년 8월 15일_

![수정](../assets/fix.svg) - 필터링을 간소화하기 위해 [Real-Time CDP 대상 대시보드](#real-time-cdp-audiences-dashboard)를 업데이트했습니다.

_2023년 6월 27일_

![수정](../assets/fix.svg) - `magento/module-data-services-graphql` 패키지에서 PHP 8.2에 대한 지원을 추가했습니다.

_2023년 5월 30일_

![새로 만들기](../assets/new.svg) - Adobe Commerce 인스턴스 내에서 활성 대상을 정렬, 검색 및 필터링하는 기능을 포함하도록 [Real-Time CDP 대상 대시보드](#real-time-cdp-audiences-dashboard)를 업데이트했습니다.

+++

### 2.4.0

[!BADGE 호환성]{type=Informative tooltip="호환성"}

_2025년 3월 24일_

![새로 만들기](../assets/new.svg) - PHP 8.4 지원이 추가되었습니다.

### 2.3.1

[!BADGE 호환성]{type=Informative tooltip="호환성"}

_2024년 11월 12일_

![수정](../assets/fix.svg) - 선택할 수 있는 Real-Time CDP 대상을 필터링할 때 발생하는 문제를 해결했습니다.

### 2.3.0

[!BADGE 호환성]{type=Informative tooltip="호환성"}

_2024년 7월 29일_

![새로 만들기](../assets/new.svg) - 명령줄 구문을 추가했으므로 [자격 증명을 테스트](#validate-the-connection)하여 Adobe Experience Platform에서 대상 데이터를 가져오기 위해 자격 증명을 업데이트해야 하는지 확인할 수 있습니다.

### 2.2.0

[!BADGE 호환성]{type=Informative tooltip="호환성"}

_2024년 6월 12일_

![새로운 기능](../assets/new.svg) - 대상자가 제공한 [관련 제품 규칙](../merchandising-promotions/product-related-rule-create.md)에 대한 GA 릴리스

### 2.1.1

[!BADGE 호환성]{type=Informative tooltip="호환성"}

_2024년 4월 4일_

![새로 만들기](../assets/new.svg) - PHP 8.3에 대한 지원을 추가했습니다.

### 2.2.0-Beta1

[!BADGE 호환성]{type=Informative tooltip="호환성"}

_2024년 2월 16일_

![새로 만들기](../assets/new.svg) - Beta에 참여하는 경우 `composer.json` 파일의 루트 수준이 ` "minimum-stability": "beta"`인지 확인하세요.
![새로 만들기](../assets/new.svg) - (**Beta**) 대상자가 제공한 [관련 제품 규칙](../merchandising-promotions/product-related-rule-create.md)을(를) 만드는 기능이 추가되었습니다.

### 2.1.0

[!BADGE 호환성]{type=Informative tooltip="호환성"}

_2024년 1월 24일_

![새로 만들기](../assets/new.svg) - 대상이 포함된 웹 사이트를 포함하고 해당 대상을 사용하도록 구성된 동적 블록 및 장바구니 가격 규칙을 지정하도록 [Real-Time CDP 대상 대시보드](#real-time-cdp-audiences-dashboard)를 업데이트했습니다.

### 2.0.1

[!BADGE 호환성]{type=Informative tooltip="호환성"}

_2023년 11월 16일_

![수정](../assets/fix.svg) - 안정성이 개선되었습니다.

### 2.0.0

[!BADGE 호환성]{type=Informative tooltip="호환성"}

_2023년 10월 10일_

![새로 만들기](../assets/new.svg) - Audience Activation 확장을 [구성](#configure-the-extension)할 때 OAuth 2.0에 대한 지원이 추가되었습니다.
![수정](../assets/fix.svg) - 안정성이 개선되었습니다.

### 1.2.0

[!BADGE 호환성]{type=Informative tooltip="호환성"}

_2023년 8월 15일_

![수정](../assets/fix.svg) - UI 구성 요소 버전을 업데이트했습니다.

### 1.1.0

_2023년 5월 30일_

[!BADGE 호환성]{type=Informative tooltip="호환성"}

![새로 만들기](../assets/new.svg) - Headless 상점 첫 화면에서 [동적 블록](#headless-support)에 대한 지원이 추가되었습니다.

### 1.0.1

_2023년 5월 11일_

[!BADGE 호환성]{type=Informative tooltip="호환성"}

![수정](../assets/fix.svg) - 동적 블록 또는 장바구니 가격 규칙이 상점 앞에 적용되지 않는 문제를 해결했습니다.
![수정](../assets/fix.svg) - 판매자가 동적 블록을 만들거나 업데이트하려고 할 때 Audience Activation 확장 프로그램의 구성되지 않은 설치로 인해 오류가 발생하는 문제를 해결했습니다.

### 1.0.0

_2023년 3월 31일_

[!BADGE 호환성]{type=Informative tooltip="호환성"}

![새로 만들기](../assets/new.svg) - 일반 가용성 릴리스

## 구현

다음 작업은 Luma 및 헤드리스 상점 구현 모두에 적용됩니다. Adobe Commerce에서 대상을 활성화하려면 다음을 수행해야 합니다.

- Adobe Commerce 버전 2.4.4 이상 설치
- Real-Time CDP의 대상으로 Adobe Commerce [활성화](https://experienceleague.adobe.com/docs/experience-platform/destinations/catalog/personalization/adobe-commerce.html)
- 관리자에서 [!DNL Audience Activation] 확장을 [설치](#install-the-extension)
- 관리에서 [!DNL Audience Activation] 확장을 [구성](#configure-the-extension)

### 확장 설치

[marketplace](https://commercemarketplace.adobe.com/magento-audiences.html)에서 [!DNL Audience Activation] 확장을 설치하거나 다음 명령을 실행하십시오.

```bash
composer require magento/audiences
```

### 확장 구성

[!DNL Audience Activation] 확장을 설치한 후 Commerce 관리자에 로그인하여 다음을 완료해야 합니다.

1. _관리자_ 사이드바에서 **[!UICONTROL System]** > _[!UICONTROL Services]_>**[!UICONTROL Commerce Services Connector]**(으)로 이동합니다.

1. Adobe 계정에 [로그인](https://experienceleague.adobe.com/docs/commerce/user-guides/integration-services/saas.html#organizationid)하고 조직 ID를 선택하세요.

1. _관리자_ 사이드바에서 **[!UICONTROL System]** > _[!UICONTROL Services]_>**[!UICONTROL [!DNL Data Connection]]**(으)로 이동합니다.

1. **[!UICONTROL Datastream ID]** 필드에 Adobe Commerce을 Real-Time CDP의 대상으로 [활성화](https://experienceleague.adobe.com/docs/experience-platform/destinations/catalog/personalization/adobe-commerce.html#parameters)할 때 만든 데이터 스트림의 ID를 붙여넣습니다.

   이 데이터 스트림은 Commerce 웹 사이트의 데이터를 Real-Time CDP으로 전송하여 쇼핑객이 대상자에 속하는지 확인합니다. 아직 데이터 스트림을 만들지 않은 경우 Experience Platform에서 [만들기](https://experienceleague.adobe.com/docs/experience-platform/datastreams/configure.html#create)하고, Real-Time CDP의 Commerce 대상과 관리자의 [[!DNL Data Connection]](https://experienceleague.adobe.com/docs/commerce/data-connection/fundamentals/connect-data.html#data-collection) 확장에 [추가](https://experienceleague.adobe.com/docs/experience-platform/destinations/catalog/personalization/adobe-commerce.html)합니다.

   >[!NOTE]
   >
   >데이터 스트림 ID를 지정할 때 [!DNL Data Connection] 확장에서 [특정 웹 사이트에 연결](https://experienceleague.adobe.com/docs/commerce/data-connection/fundamentals/connect-data.html#data-collection)합니다. Commerce 스토어에 여러 개의 웹 사이트가 있는 경우 Real-Time CDP의 각 웹 사이트에 대해 [대상을 만들고](https://experienceleague.adobe.com/docs/experience-platform/destinations/ui/connect-destination.html) 각각에 대해 다른 데이터 스트림 ID를 사용하십시오.

1. _관리자_ 사이드바에서 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**(으)로 이동합니다.

1. **[!UICONTROL Services]**&#x200B;을(를) 확장하고 **[!UICONTROL [!DNL Data Connection]]**&#x200B;을(를) 선택합니다.

1. [서비스 계정 및 자격 증명 세부 정보를 추가](https://experienceleague.adobe.com/docs/commerce/data-connection/fundamentals/connect-data.html#add-service-account-and-credential-details)합니다.

## Commerce에서 Real-Time CDP 대상을 사용하는 위치

[!DNL Audience Activation] 확장을 사용하면 다음 작업을 수행할 수 있습니다.

- 대상자가 제공한 [장바구니 가격 규칙 만들기](../merchandising-promotions/price-rules-cart-create.md#set-a-condition-using-real-time-cdp-audiences)
- 대상자가 제공한 [동적 블록 만들기](../content-design/dynamic-blocks.md#use-real-time-cdp-audiences-in-dynamic-blocks)
- 대상자가 제공한 [관련 제품 규칙 만들기](../merchandising-promotions/product-related-rule-create.md)

>[!TIP]
>
>[!DNL Commerce] 데이터를 Real-Time CDP으로 내보내고 대상을 작성한 다음 해당 대상을 [!DNL Commerce]에 활성화하는 방법에 대한 전체 엔드 투 엔드 사용 사례는 [이벤트 데이터를 사용하여 Real-Time CDP에서 대상 만들기 [!DNL Commerce] 를 참조하십시오](https://experienceleague.adobe.com/en/docs/commerce/data-connection/use-cases/create-audience).

## Real-Time CDP 대상 대시보드

**Real-Time CDP 대상** 대시보드를 사용하여 Adobe Commerce 인스턴스 내에서 개인화할 수 있는 모든 [활성](https://experienceleague.adobe.com/docs/experience-platform/destinations/ui/activate/activate-edge-personalization-destinations.html) 대상을 볼 수 있습니다.

**Real-Time CDP 대상** 대시보드에 액세스하려면 _관리자_ 사이드바로 이동한 다음 **[!UICONTROL Customers]** > **[!UICONTROL Real-time CDP Audience]**(으)로 이동하십시오.

![Real-Time CDP 대상 대시보드](./assets/real-time-cdp-dashboard.png){width="700" zoomable="yes"}

대시보드에는 다음 필드가 포함되어 있습니다.

| 열 | 설명 |
|--- |--- |
| `Hide filters` | 대시보드에 적용할 수 있는 필터를 표시하거나 숨길 수 있습니다. 현재 적용할 수 있는 필터는 `Last updated`뿐입니다. 이 필터를 사용하면 대상이 마지막으로 업데이트된 시간을 기준으로 대상의 날짜 범위를 선택할 수 있습니다. |
| `Search` | Commerce 인스턴스에서 활성 대상을 검색할 수 있도록 해 줍니다. |
| `Name` | Real-Time CDP에서 대상에게 지정된 이름입니다. |
| `Origin` | 대상자가 있었던 위치(예: `Experience Platform`)를 나타냅니다. |
| `Websites` | 대상을 사용하도록 구성된 웹 사이트를 나타냅니다. |
| `Dynamic Blocks` | 대상을 사용하도록 구성된 동적 블록을 나타냅니다. |
| `Cart Price Rules` | 대상자를 사용하도록 구성된 장바구니 가격 규칙을 나타냅니다. |
| `Related Product Rules` | 대상을 사용하도록 구성된 관련 제품 규칙을 나타냅니다. |
| `Last updated` | Real-Time CDP에서 대상이 수정된 시기를 나타냅니다. |
| `Sync now` | Real-Time CDP에서 새 대상자 또는 업데이트된 대상자를 검색합니다. |
| `Customize table` | `Origin`, `Websites`, `Dynamic Blocks`, `Cart Price Rules` 및 `Last updated` 열을 표시하거나 숨길 수 있습니다. |

{style="table-layout:auto"}

## 헤드리스 지원

AEM 및 PWA과 같은 Headless Adobe Commerce 인스턴스에서 대상을 활성화하여 장바구니 가격 규칙, 관련 제품 규칙 또는 대상을 기반으로 하는 동적 블록을 표시할 수 있습니다.

### 장바구니 가격 규칙 및 관련 제품 규칙

장바구니 가격 규칙 및 관련 제품 규칙의 경우, 헤드리스 상점 첫 페이지는 [Commerce integration framework(CIF)](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/content-and-commerce/integrations/magento.html)을(를) 통해 Experience Platform과 통신합니다. 프레임워크는 GraphQL을 사용하여 구현된 서버측 API를 제공합니다. 쇼핑객 세그먼트와 같은 대상 정보는 이름이 `aep-segments-membership`인 GraphQL 헤더 매개 변수를 통해 Commerce으로 전달됩니다.

전반적인 아키텍처는 다음과 같습니다.

![Headless Storefront에서 백엔드로 데이터 보내기](./assets/aem-commerce-architecture.png){width="700" zoomable="yes"}

확장을 [설치](#install-the-extension)하고 [구성](#configure-the-extension)하면 Experience Platform Web SDK에 세그먼트 멤버십 형식으로 대상 정보가 포함됩니다.

SDK에서 이러한 세그먼트 멤버십을 캡처하려면 이 [코드 조각](https://experienceleague.adobe.com/docs/experience-platform/destinations/catalog/personalization/custom-personalization.html#example-response-for-custom-personalization-with-attributes)을 참조하십시오.

검색되면 해당 세그먼트를 GraphQL 헤더 내에서 Commerce에 전달할 수 있습니다. For example:

```bash
curl 'http://magento.config/graphql' -H 'Authorization: Bearer abc123' -H 'aep-segments-membership: urlencoded_list_of_segments' -H 'Content-Type: application/json' --data-binary '{"query":"query {\ncustomer {\nfirstname\nlastname\nemail\n}\n}"}'
```

### 동적 블록

동적 블록의 경우 GraphQL `dynamicBlocks` 쿼리에 `audience_id` 입력 특성이 포함될 수 있습니다. `dynamicBlocks` 쿼리에 하나 이상의 `audience_id` 값을 지정하면 해당 대상에 할당된 동적 블록의 목록이 반환됩니다.

#### 사용 예

다음 쿼리는 여러 대상 ID와 연결된 모든 동적 블록을 반환합니다.

**요청:**

```graphql
{
  dynamicBlocks(input:
  {
    type: SPECIFIED
    audience_id: {
      in: [
        "cd29a789-9be8-40ad-a1ef-640c33b3742e"
        "92c3e14d-c72b-40d0-96b7-b96801dcc135"
      ]
    }
  })
  {
    items {
      uid
      audience_id
      content {
        html
      }
    }
    page_info {
      current_page
      page_size
      total_pages
    }
    total_count
  }
}
```

**응답:**

```json
{
  "data": {
    "dynamicBlocks": {
      "items": [
        {
          "uid": "MQ==",
          "audience_id": [
            "cd29a789-9be8-40ad-a1ef-640c33b3742e"
          ],
          "content": {
            "html": "<h2><strong>SAVE 20%</strong></h2>\r\n<p>(some restrictions apply)</p>\r\n<p>&nbsp;</p>"
          }
        },
        {
          "uid": "Mg==",
          "audience_id": [
            "cd29a789-9be8-40ad-a1ef-640c33b3742e",
            "92c3e14d-c72b-40d0-96b7-b96801dcc135"
          ],
          "content": {
            "html": "<p><img src=\"{{media url=&quot;wysiwyg/save20.png&quot;}}\" alt=\"save 20% red\"></p>"
          }
        }
      ],
      "page_info": {
        "current_page": 1,
        "page_size": 20,
        "total_pages": 1
      },
      "total_count": 2
    }
  }
}
```

[개발자 설명서](https://developer.adobe.com/commerce/webapi/graphql/schema/store/queries/dynamic-blocks/)에서 `dynamicBlocks` GraphQL 쿼리에 대해 자세히 알아보세요.

## Adobe Experience Platform Mobile SDK을 사용하여 대상자 검색

Adobe Experience Platform Mobile SDK을 사용하여 Real-Time CDP 대상을 검색할 수 있습니다.

1. Audience Activation 확장 [설치](#install-the-extension).
1. [모바일 Commerce 사이트에 대한 SDK 설치 및 구성](https://experienceleague.adobe.com/docs/commerce/data-connection/fundamentals/mobile-sdk-epc.html).

>[!IMPORTANT]
>
>iOS용 Adobe Experience Platform Mobile SDK은 iOS 11 이상을 지원합니다.

구성을 완료한 후 모바일 SDK 작업을 사용하여 대상 데이터를 검색합니다. For example:

```swift
Edge.sendEvent(experienceEvent: experienceEvent) { (handles: [EdgeEventHandle]) in
    for handle in handles {
        if handle.type == "activation:pull" {
        let payloadItems = handle.payload ?? []
            for payloadItem in payloadItems {
                if let segments = payloadItem["segments"] as? any Sequence {
                    var segmentsArr = [Any]()
                    for segment in segments {
                        let response = segment as AnyObject?
                        segmentsArr.append(response?.object(forKey: "id")! ?? "")
                    }
                    print("Saving segments ->  \(segments)")
                    storage.set(segmentsArr, forKey: "segments")
                    print("End saving segments")
                }
         
                // Show segments
                let rSegments = storage.object(forKey: "segments") ?? nil;
                print("Retrieving segments -> \(rSegments)")
            }
        }
    }
}
```

데이터를 검색한 후 이를 사용하여 Commerce 앱에서 대상자에게 제공되는 [장바구니 가격 규칙](../merchandising-promotions/price-rules-cart-create.md#set-a-condition-using-real-time-cdp-audiences), [동적 블록](../content-design/dynamic-blocks.md#use-real-time-cdp-audiences-in-dynamic-blocks) 및 [관련 제품 규칙](../merchandising-promotions/product-related-rule-create.md)을 만들 수 있습니다.

## 대상이 Commerce에 표시되지 않음

Real-Time CDP 대상이 Commerce에 표시되지 않는 이유는 다음과 같습니다.

- 잘못된 연결
- **데이터 연결** 구성 페이지에서 잘못된 인증 유형을 선택했습니다.
- 생성된 토큰에 대한 권한이 충분하지 않음

다음 섹션에서는 이러한 문제를 해결하는 방법을 설명합니다.

### 연결 유효성 검사

자격 증명과 Adobe Experience Platform의 응답을 확인하려면 다음 명령을 실행합니다.

```bash
bin/magento audiences:config:status
```

이 명령은 연결 상태를 반환합니다. 자세한 정보를 제공하려면 `-v` 플래그를 추가하십시오.

```
./bin/magento audiences:config:status -v  
```

For example:

```
+----------------------------------+---------------+---------------------------------------------+---------------------------------------------------------+--------------+
| Client ID                        | Client secret | Technical account ID                        | Technical account email                                 | Sandbox name |
+----------------------------------+---------------+---------------------------------------------+---------------------------------------------------------+--------------+
| 1234bd57fac8497d8933327c535347d8 | *****         | 12341E116638D6B00A495C80@techacct.adobe.com | 12345-b95b-4894-a41c-a4130d26bd80@techacct.adobe.com | dev          |
```

### 구성에서 잘못된 인증 유형 선택됨

1. Commerce 인스턴스를 엽니다.
1. _관리자_ 사이드바에서 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**(으)로 이동합니다.
1. **[!UICONTROL Services]**&#x200B;을(를) 확장하고 **[!UICONTROL [!DNL Data Connection]]**&#x200B;을(를) 선택합니다.
1. **[!UICONTROL Authentication Type]** 필드에 지정한 서버 간 인증 방법이 올바른지 확인하십시오. Adobe에서는 **OAuth**&#x200B;을(를) 사용하는 것이 좋습니다. JWT는 더 이상 사용되지 않습니다. [자세히 알아보기](https://developer.adobe.com/developer-console/docs/guides/authentication/ServerToServerAuthentication/migration/).

### 생성된 토큰에 대한 권한이 충분하지 않음

이 문제는 생성된 토큰에 대한 API 권한이 충분하지 않기 때문에 발생할 수 있습니다. 토큰에 올바른 권한이 있는지 확인하려면 다음을 수행하십시오.

1. 조직의 Adobe Experience Platform 시스템 관리자를 식별합니다.
1. 사용할 프로젝트 및 자격 증명을 찾습니다.
1. 기술 계정 전자 메일을 식별합니다(예: `fe3c9476-1234-1234-abcd-2a51a785009a@techacct.adobe.com`).
1. 시스템 관리자가 Adobe Experience Platform을 시작하고 **[!UICONTROL Permissions]** -> **[!UICONTROL Users]** -> **[!UICONTROL API credentials]**(으)로 이동합니다.
1. 위의 기술 계정 이메일을 사용하여 수정할 자격 증명을 검색합니다.
1. 자격 증명을 연 다음 **[!UICONTROL Roles]** -> **[!UICONTROL Add roles]**&#x200B;을(를) 선택합니다.
1. **[!UICONTROL Manage destinations]** 권한이 포함된 역할을 추가하십시오.
1. **[!UICONTROL Save]**&#x200B;을(를) 클릭합니다.
1. 콘솔에서 액세스 토큰을 [다시 생성](https://experienceleague.adobe.com/docs/experience-platform/landing/platform-apis/api-authentication.html#generate-access-token)합니다.
1. 토큰이 [Target 연결 API](https://developer.adobe.com/experience-platform-apis/references/destinations/#tag/Target-connections/operation/getTargetConnections)를 사용하여 올바른 응답을 제공하는지 확인하십시오.
