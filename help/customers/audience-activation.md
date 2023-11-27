---
title: "[!DNL Audience Activation]"
description: Adobe Commerce에서 Real-Time CDP 대상을 활성화하여 스토어에서 개인화를 추진하는 방법에 대해 알아봅니다.
exl-id: b53908f2-c0c1-42ad-bb9e-c762804a744b
feature: Customers, Configuration, Personalization
topic: Commerce, Personalization
level: Experienced
source-git-commit: f7b8e47aa5a8113fac768b8086ace3bf673193c5
workflow-type: tm+mt
source-wordcount: '1222'
ht-degree: 0%

---

# [!DNL Audience Activation]

다음 [!DNL Audience Activation] 확장을 사용하면 Adobe Commerce에서 Real-Time CDP 대상을 활성화하여 장바구니에서 고유한 오퍼를 만들 수 있습니다. 이러한 오퍼와 인센티브에는 다음과 같은 일반적인 전자 상거래 머천다이징 기술이 포함됩니다. _2개 구입 1개 무료_, 영웅 배너는 해당 고객에 맞게 조정되었으며 다양한 오퍼를 통해 제품 가격을 수정했습니다. Real-Time CDP에 구축된 대상은 ERP(전사적 자원 관리), CRM(고객 관계 관리), POS(판매 지점), 마케팅 시스템과 같은 다양한 엔터프라이즈 시스템의 데이터를 기반으로 합니다. 고객 세그먼트 정보는 지속적으로 새로 고쳐지기 때문에 고객은 스토어에서 쇼핑할 때 세그먼트와 연결 및 연결 해제될 수 있습니다.

Luma 상점 첫 화면에서 대상자를 활성화하거나 [headless](#headless-support) 가게 앞이야 Luma 상점 첫 화면에서 대상 정보(세그먼트 멤버십)는 상거래 측의 쿠키에 저장됩니다. 헤드리스 상점 첫 화면에서 대상 정보는 GraphQL API 헤더에 이라는 매개 변수로 전달됩니다. `aep-segments-membership`.

## 릴리스 정보

이 섹션에는 Audience Activation 확장 업데이트에 대한 정보가 포함되어 있으며 다음 내용이 포함됩니다.

![신규](../assets/new.svg) - 새로운 기능
![수정](../assets/fix.svg) - 수정 사항 및 향상된 기능
![버그](../assets/bug.svg) - 알려진 문제

다음을 참조하십시오 [예정된 릴리스](https://experienceleague.adobe.com/docs/commerce-operations/release/planning/schedule.html) 릴리스 일정 및 지원에 대해 알아봅니다.

개발자 설명서 를 참조하여 다음을 수행합니다 [제품 호환성에 대해 알아보기](https://experienceleague.adobe.com/docs/commerce-operations/release/product-availability.html).

## 지원되는 서비스 업데이트

이러한 릴리스 노트는 Audience Activation에서 사용하는 확장과 관련된 기능 변경 사항 및 수정 사항에 대해 설명합니다.

+++지원되는 서비스 업데이트

_2023년 8월 15일_

![수정](../assets/new.svg) - 을(를) 업데이트함 [Real-Time CDP 대상 대시보드](#real-time-cdp-audiences-dashboard) 필터링을 단순화합니다.

_2023년 6월 27일_

![수정](../assets/fix.svg) - 의 PHP 8.2에 대한 지원을 추가했습니다. `magento/module-data-services-graphql` 패키지.

_2023년 5월 30일_

![신규](../assets/new.svg) - 을(를) 업데이트함 [Real-Time CDP 대상 대시보드](#real-time-cdp-audiences-dashboard) Adobe Commerce 인스턴스 내에서 활성 대상을 정렬, 검색 및 필터링할 수 있는 기능을 포함합니다.

+++

### 2.0.0

[!BADGE 호환성]{type=Informative tooltip="호환성"}

_2023년 10월 10일_

![신규](../assets/new.svg) - 다음을 수행하는 경우 OAuth 2.0에 대한 지원이 추가됨: [구성](#configure-the-extension) Audience Activation 확장.
![수정](../assets/fix.svg) - 안정성 향상.

### 1.2.0

[!BADGE 호환성]{type=Informative tooltip="호환성"}

_2023년 8월 15일_

![수정](../assets/fix.svg) - UI 구성 요소 버전을 업데이트했습니다.

### 1.1.0

_2023년 5월 30일_

[!BADGE 호환성]{type=Informative tooltip="호환성"}

![신규](../assets/new.svg) - 다음에 대한 지원이 추가되었습니다. [동적 블록](#headless-support) 헤드리스 상점 앞에서요.

### 1.0.1

_2023년 5월 11일_

[!BADGE 호환성]{type=Informative tooltip="호환성"}

![수정](../assets/fix.svg) - 동적 블록 또는 장바구니 가격 규칙이 상점 앞에 적용되지 않던 문제를 수정했습니다.
![수정](../assets/fix.svg) - 판매자가 동적 블록을 만들거나 업데이트하려고 할 때 Audience Activation 확장의 구성되지 않은 설치로 인해 오류가 발생하는 문제를 해결했습니다.

### 1.0.0

_2023년 3월 31일_

[!BADGE 호환성]{type=Informative tooltip="호환성"}

![신규](../assets/new.svg) - 일반 가용성 릴리스

## 구현

다음 작업은 Luma 및 헤드리스 상점 구현 모두에 적용됩니다. Adobe Commerce에서 대상을 활성화하려면 다음을 수행해야 합니다.

- Adobe Commerce 버전 2.4.4 이상 설치
- [활성화](https://experienceleague.adobe.com/docs/experience-platform/destinations/catalog/personalization/adobe-commerce.html) Real-Time CDP에서 대상으로서의 Adobe Commerce
- [설치](#install-the-extension) 다음 [!DNL Audience Activation] 관리자의 확장
- [구성](#configure-the-extension) 다음 [!DNL Audience Activation] 관리자의 확장

### 확장 설치

설치 [!DNL Audience Activation] 에서 확장명 [마켓플레이스](https://commercemarketplace.adobe.com/magento-audiences.html)또는 다음 명령을 실행합니다.

```bash
composer require magento/audiences
```

### 확장 구성

를 설치한 후 [!DNL Audience Activation] 확장을 사용하려면 Commerce 관리자에 로그인하고 다음을 완료해야 합니다.

1. 다음에서 _관리자_ 사이드바, 이동 **[!UICONTROL System]** > _[!UICONTROL Services]_>**[!UICONTROL Commerce Services Connector]**.

1. [로그인](https://experienceleague.adobe.com/docs/commerce-merchant-services/user-guides/integration-services/saas.html#organizationid) 을 Adobe 계정에 추가하고 조직 ID를 선택합니다.

1. 다음에서 _관리자_ 사이드바, 이동 **[!UICONTROL System]** > _[!UICONTROL Services]_>**[!UICONTROL [!DNL Data Connection]]**.

1. 다음에서 **[!UICONTROL Datastream ID]** 필드에 생성 시 생성한 데이터 스트림의 ID를 붙여넣습니다. [활성화됨](https://experienceleague.adobe.com/docs/experience-platform/destinations/catalog/personalization/adobe-commerce.html#parameters) Real-Time CDP의 대상으로서의 Adobe Commerce.

   이 데이터 스트림은 Commerce 웹 사이트의 데이터를 Real-Time CDP으로 전송하여 쇼핑객이 대상자에 속하는지 확인합니다. 데이터 스트림을 아직 만들지 않은 경우 [만들기](https://experienceleague.adobe.com/docs/experience-platform/datastreams/configure.html#create) 1명 Experience Platform, [추가](https://experienceleague.adobe.com/docs/experience-platform/destinations/catalog/personalization/adobe-commerce.html) Real-Time CDP의 Commerce 대상 및 [[!DNL Data Connection]](https://experienceleague.adobe.com/docs/commerce-merchant-services/data-connection/fundamentals/connect-data.html#data-collection) 관리자 확장명.

   >[!NOTE]
   >
   >데이터 스트림 ID를 지정할 때 [특정 웹 사이트에 연결](https://experienceleague.adobe.com/docs/commerce-merchant-services/data-connection/fundamentals/connect-data.html#data-collection) 다음에서 [!DNL Data Connection] 확장명. 상거래 스토어에 여러 웹 사이트가 있는 경우 [대상 만들기](https://experienceleague.adobe.com/docs/experience-platform/destinations/ui/connect-destination.html) Real-Time CDP의 각 웹 사이트에 대해 서로 다른 데이터 스트림 ID를 사용하십시오.

1. 다음에서 _관리자_ 사이드바, 이동 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. 확장 **[!UICONTROL Services]** 및 선택 **[!UICONTROL [!DNL Data Connection]]**.

1. 다음에서 [[!DNL Data Connection]](https://experienceleague.adobe.com/docs/commerce-merchant-services/data-connection/fundamentals/connect-data.html#send-historical-order-data) 안내서에서 1단계를 수행합니다. **Adobe Developer 콘솔에서 프로젝트 만들기**, 및 2: **구성 파일 다운로드**. 그 결과는에 복사하여 붙여넣는 파일입니다. **[!UICONTROL [!DNL Data Connection]]** 구성 페이지:

   ![Real-Time CDP 대상 관리자 구성](./assets/epc-admin-config.png){width="700" zoomable="yes"}

1. 클릭 **구성 저장**.

Adobe Commerce 인스턴스에 활성화된 대상자를 통해 다음을 수행할 수 있습니다.

- [장바구니 가격 규칙 만들기](../merchandising-promotions/price-rules-cart-create.md#set-a-condition-using-real-time-cdp-audiences) 대상자가 정보 제공
- [동적 블록 만들기](../content-design/dynamic-blocks.md#use-real-time-cdp-audiences-in-dynamic-blocks) 대상자가 정보 제공

## Real-Time CDP 대상 대시보드

를 사용하여 Adobe Commerce 인스턴스 내에서 개인화할 수 있는 모든 활성 대상을 볼 수 있습니다. **Real-Time CDP 대상** 대시보드입니다. 귀하가 원하는 모든 대상자 [활성화됨](https://experienceleague.adobe.com/docs/experience-platform/destinations/ui/activate/activate-edge-personalization-destinations.html) Real-Time CDP의 Adobe Commerce 대상에서 이 대시보드에 표시됩니다.

에 액세스하려면 **Real-Time CDP 대상** 대시보드에서 로 이동합니다. _관리자_ 사이드바, 다음으로 이동 **[!UICONTROL Customers]** > **[!UICONTROL Real-time CDP Audience]**.

대시보드에는 다음 필드가 포함되어 있습니다.

| 열 | 설명 |
|--- |--- |
| `Hide filters` | 대시보드에 적용할 수 있는 필터를 표시하거나 숨길 수 있습니다. 현재 적용할 수 있는 유일한 필터는 다음과 같습니다. `Last updated`. 이 필터를 사용하면 대상이 마지막으로 업데이트된 시간을 기준으로 대상의 날짜 범위를 선택할 수 있습니다. |
| `Search` | 상거래 인스턴스에서 활성 대상을 검색할 수 있도록 해줍니다. |
| `Name` | Real-Time CDP에서 대상에게 지정된 이름입니다. |
| `Origin` | 대상이 어디에서 왔는지를 나타냅니다. 예: `Experience Platform`. |
| `Last updated` | Real-Time CDP에서 대상이 수정된 시기를 나타냅니다. |
| `Sync now` | Real-Time CDP에서 새 대상자 또는 업데이트된 대상자를 검색합니다. |
| `Customize table` | 다음을 표시하거나 숨길 수 있습니다. `Origin` 및 `Last updated` 열. |

{style="table-layout:auto"}

## 헤드리스 지원

AEM 및 PWA과 같은 Headless Adobe Commerce 인스턴스에서 대상을 활성화하여 대상을 기반으로 하는 장바구니 가격 규칙이나 동적 블록을 표시할 수 있습니다.

### 장바구니 가격 규칙

장바구니 가격 규칙의 경우, 헤드리스 매장은 다음을 통해 Experience Platform과 커뮤니케이션합니다. [Commerce integration framework(CIF)](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/content-and-commerce/integrations/magento.html). 프레임워크는 GraphQL을 사용하여 구현된 서버측 API를 제공합니다. 쇼핑객 세그먼트와 같은 대상 정보는 라는 GraphQL 헤더 매개 변수를 통해 Commerce로 전달됩니다. `aep-segments-membership`.

전반적인 아키텍처는 다음과 같습니다.

![Headless Storefront에서 백엔드로 데이터 보내기](./assets/aem-commerce-architecture.png){width="700" zoomable="yes"}

이후 [설치](#install-the-extension) 및 [구성](#configure-the-extension) 확장 기능인 Experience Platform 웹 SDK에는 세그먼트 멤버십 형식으로 대상 정보가 포함되어 있습니다.

SDK에서 이러한 세그먼트 멤버십을 캡처하려면 다음을 참조하십시오. [코드 조각](https://experienceleague.adobe.com/docs/experience-platform/destinations/catalog/personalization/custom-personalization.html#example-response-for-custom-personalization-with-attributes).

검색되면 해당 세그먼트를 GraphQL 헤더 내의 Commerce에 전달할 수 있습니다. For example:

```bash
curl 'http://magento.config/graphql' -H 'Authorization: Bearer abc123' -H 'aep-segments-membership: urlencoded_list_of_segments' -H 'Content-Type: application/json' --data-binary '{"query":"query {\ncustomer {\nfirstname\nlastname\nemail\n}\n}"}'
```

### 동적 블록

동적 블록의 경우 GraphQL `dynamicBlocks` 쿼리에 다음을 포함할 수 있습니다 `audience_id` 입력 속성입니다. 하나 이상을 지정하는 경우 `audience_id` 의 값 `dynamicBlocks` query를 반환하면 해당 대상자에게 할당된 동적 블록 목록이 반환됩니다.

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

에 대해 자세히 알아보기 `dynamicBlocks` 의 GraphQL 쿼리 [개발자 설명서](https://developer.adobe.com/commerce/webapi/graphql/schema/store/queries/dynamic-blocks/).

## Adobe Experience Platform Mobile SDK를 사용하여 대상자 검색

Adobe Experience Platform Mobile SDK를 사용하여 Real-Time CDP 대상을 검색하려면 먼저 다음과 같이 하십시오. [모바일 상거래 사이트에 대한 SDK 설치 및 구성](https://experienceleague.adobe.com/docs/commerce-merchant-services/data-connection/fundamentals/mobile-sdk-epc.html).

>[!IMPORTANT]
>
>iOS용 Adobe Experience Platform Mobile SDK는 iOS 11 이상을 지원합니다.

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

데이터가 검색되면 이를 사용하여 대상자에게 정보를 제공할 수 있습니다 [장바구니 가격 규칙](../merchandising-promotions/price-rules-cart-create.md#set-a-condition-using-real-time-cdp-audiences) 및 [동적 블록](../content-design/dynamic-blocks.md#use-real-time-cdp-audiences-in-dynamic-blocks) Commerce 앱에서
