---
title: '''[!DNL Adobe Commerce B2B] 릴리스 정보'
description: 의 변경 사항에 대한 자세한 내용은 릴리스 정보 를 참조하십시오. [!DNL Adobe Commerce B2B] 릴리스.
exl-id: 77d8c20d-6667-41e3-8889-252f36e56fd8
feature: B2B, Release Notes
source-git-commit: 17eec4e7755ce4e83fb0533940bdce6c96ddc717
workflow-type: tm+mt
source-wordcount: '6867'
ht-degree: 0%

---

# [!DNL Adobe Commerce B2B] 릴리스 정보

B2B 확장에 대한 이러한 릴리스 노트는 다음을 포함하여 Adobe이 릴리스 주기 동안 추가한 추가 및 수정 사항을 캡처합니다.

![신규](../assets/new.svg) 새로운 기능
![해결된 문제](../assets/fix.svg) 수정 사항 및 향상된 기능
![알려진 문제](../assets/bug.svg) 알려진 문제

>[!NOTE]
>
>다음을 참조하십시오 [제품 가용성](https://experienceleague.adobe.com/docs/commerce-operations/release/product-availability.html) 사용 가능한 Adobe Commerce 릴리스에서 지원되는 B2B Commerce 확장 버전에 대한 정보입니다.

## B2B 1.5.0-베타

{{$include /help/_includes/b2b-beta-note.md}}

*2023년 11월 13일*

[!BADGE 지원됨]{type=Informative tooltip="지원됨"}

B2B v1.5.0 베타 릴리스에는 새로운 기능, 품질 개선 및 버그 수정이 포함되어 있습니다.

![신규](../assets/new.svg) 견적 기능을 개선하면 구매자와 판매자가 견적 및 견적 협상을 보다 효과적으로 관리할 수 있습니다.

- **견적을 초안으로 저장**<!--B2B-2566-->- 를 생성할 때 [견적 요청](quote-request.md) 이제 구매자는 장바구니에서 을(를) 선택하여 견적을 초안으로 저장할 수 있습니다. **[!UICONTROL Save as Draft]** 다음에 있음 [!UICONTROL Request a Quote] 양식.

  초안 견적에 만료일이 없습니다. 구매자는 다음 위치에서 초안 견적을 검토하고 업데이트할 수 있습니다. [!UICONTROL My Quotes] 섹션에 있는 마지막 항목이 될 필요가 없습니다.

- **견적 이름 바꾸기**<!--B2B-2596-->—이제 구매자는 [견적 세부 정보](account-dashboard-my-quotes.md#quote-actions) 페이지를 만드는 방법 **[!UICONTROL Rename]** 옵션을 선택합니다. 이 옵션은 승인된 구매자가 견적을 편집할 때 사용할 수 있습니다. 이름 변경 이벤트는 Quote 내역 로그에 기록됩니다.

- **견적 복제**<!--B2B-2701-->—구매자와 판매자가 기존 견적을 복사하여 새 견적을 작성할 수 있습니다. Quote 세부 정보 보기에서 다음을 선택하여 Copy 를 생성합니다.  **[!UICONTROL Create Copy]** 다음에 있음 [견적 세부 정보 보기](quote-price-negotiation.md#button-bar) 관리자 또는 [상점 첫 화면](account-dashboard-my-quotes.md#quote-actions).

- **라인 항목 할인 잠금**<!--B2B-2597-->- 견적 협상 중에 판매자는 할인을 적용할 때 보다 유연하게 라인 항목 할인 잠금을 사용할 수 있습니다. 예를 들어, 판매자는 품목에 특별 라인 품목 할인을 적용하고 추가 할인을 방지하기 위해 품목을 잠글 수 있습니다. 품목이 잠기면 견적 레벨 할인이 적용될 때 품목 가격을 갱신할 수 없습니다. 다음을 참조하십시오 [구매자에 대한 견적 시작](sales-rep-initiates-quote.md).

![신규&#x200B;](../assets/new.svg)**회사 관리**<!--B2B-2901-->—상인은 이제 지정된 상위 회사에 회사를 할당하여 Adobe Commerce 회사를 계층적 조직으로 보고 관리할 수 있습니다. 회사가 상위에 할당된 경우 상위 회사 관리자가 회사 계정을 관리할 수 있습니다. 승인된 관리자 사용자만 회사 할당을 추가하고 관리할 수 있습니다. 자세한 내용은 [회사 계층 관리](assign-companies.md).

- 회사 페이지에서 새 **[!UICONTROL Company Type]** 필드는 상위 및 하위 회사를 식별합니다. 판매자는 회사 유형별로 회사 보기를 필터링하고 라인 항목이나 대량 작업을 사용하여 회사를 관리할 수 있습니다.

- 판매자는 새 앱에서 회사 할당을 추가하고 관리할 수 있습니다. **[!UICONTROL Company Hierarchy]** 다음에 대한 섹션 [!UICONTROL Company Account] 페이지를 가리키도록 업데이트하는 중입니다.

- API 개발자는 새 회사 관계 REST API 엔드포인트를 사용할 수 있습니다. `/V1/company/{parentId}/relations` 을 눌러 회사 할당을 생성, 조회 및 제거합니다. 다음을 참조하십시오 [회사 오브젝트 관리](https://developer.adobe.com/commerce/webapi/rest/b2b/company-object/) 다음에서 *웹 API 개발자 안내서*.

![해결된 문제](../assets/fix.svg)<!--ACP2E-1984-->판매자 클릭 **[!UICONTROL Print]** 이제 Admin 의 Quote 세부 정보 보기에 있는 Button에 Quote 를 PDF으로 저장하라는 메시지가 표시됩니다. 이전에는 판매자가 견적 세부 정보가 포함된 페이지로 리디렉션되었습니다.

![해결된 문제](../assets/fix.svg) <!--ACP2E-1742-->이전에는 고객 견적을 0%로 보내고 수량을 변경할 때 관리자가 예외를 발생시켰지만 수량을 저장했습니다. 이 수정 사항이 적용되면 `0 percentage` 메시지와 함께 적절한 예외가 throw됩니다.

![해결된 문제](../assets/fix.svg) <!--ACP2E-1742-->견적 협상 중에 판매자는 이제 `0%` 견적 할인 필드에 있는 할인입니다. 그리고 견적을 구매자에게 다시 보냅니다. 이전에는 판매자가 0% 할인을 입력하고 견적을 구매자에게 다시 보내면 관리자가 을 반환했습니다. `Exception occurred during quote sending` 오류 메시지입니다.

![해결된 문제](../assets/fix.svg) <!--ACP2E-2097-->이제 ReCaptcha V3이 상점 전면 체크아웃에 대해 구성된 경우 B2B 견적에 대한 체크아웃 프로세스 중에 ReCaptcha 유효성 검사가 올바르게 작동합니다. 이전에는 을(를) 통해 유효성 검사가 실패했습니다. `recaptcha validation failed, please try again` 오류 메시지입니다.

![해결된 문제](../assets/fix.svg) <!--ACP2E-1825-->회사가 차단된 후에는 더 이상 회사와 연결된 사용자가 구매 발주를 수행할 수 없습니다. 이전에는 회사가 차단되면 회사와 연관된 사용자가 구매 주문을 할 수 있었습니다.

![해결된 문제](../assets/fix.svg)<!--ACP2E-1933-->이제 회사 관리자는 상점 첫 화면에서 회사 사용자를 추가할 수 있습니다. 이전에는 Commerce에서 관리자가 새 사용자를 추가하려고 할 때 오류를 기록했습니다. `CRITICAL: Error: Call to a member function __toArray() on null in app/code/Magento/LoginAsCustomerLogging/Observer/LogSaveCustomerObserver.php:123`.

## B2B v1.4.2-p1

[!BADGE 지원됨]{type=Informative tooltip="지원됨"}

![신규](../assets/new.svg) Adobe Commerce 2.4.7-p1 및 2.4.6-p6 보안 패치 릴리스와의 호환성을 추가했습니다.


## B2B v1.4.2

*2023년 10월 10일*

[!BADGE 지원됨]{type=Informative tooltip="지원됨"}

B2B v1.4.2 릴리스에는 품질 개선 사항 및 버그 수정이 포함되어 있습니다

![해결된 문제](../assets/fix.svg) <!--B2B-2897-->판매자가 구매자 회사와 연계된 공유 카탈로그에서 사용할 수 없는 제품 SKU를 포함하는 구매자 견적을 생성하는 경우, 시스템에 오류 메시지가 표시됩니다 `The SKU you entered is not available in the shared catalog. Please check the SKU and try again`.  판매자는 사용할 수 없는 제품을 제거할 때까지 견적을 저장할 수 없습니다. 이전에는 견적이 사용할 수 없는 SKU와 함께 저장되었으며, 상점 첫 화면에서 견적이 로드되지 않았습니다.

## B2B v1.4.1

*2023년 8월 7일*

[!BADGE 지원됨]{type=Informative tooltip="지원됨"}[Adobe Commerce 2.4.6-p2](https://experienceleague.adobe.com/docs/commerce-operations/release/notes/security-patches/2-4-6-p1.html). Adobe Commerce 2.4.7-beta1과 호환됩니다.

B2B v1.4.1 릴리스에는 품질 개선 사항 및 버그 수정이 포함되어 있습니다.

![해결된 문제](../assets/fix.svg) <!--ACP2E-1825-->회사가 차단된 후에는 더 이상 회사와 연결된 사용자가 구매 발주를 수행할 수 없습니다. 이전에는 회사가 차단되면 회사와 연관된 사용자가 구매 주문을 할 수 있었습니다.

![해결된 문제](../assets/fix.svg) <!--ACP2E-1943-->이제 제품 미납 주문 상태가 상점 정면에 올바르게 표시됩니다. 이전에는 배송 가능한 제품이 미납주문으로 잘못 식별되었습니다.

![해결된 문제](../assets/fix.svg) <!--ACP2E-1862-->회사 등록 양식에 고객 파일 유형 속성이 포함된 경우, 이제 회사를 만든 후 등록 프로세스 중에 업로드된 파일이 회사 관리자의 계정 정보에 포함됩니다. 이전에는 첨부 파일이 없습니다.

![해결된 문제](../assets/fix.svg) <!--ACP2E-1793-->구성 가능한 제품의 견본 선택기가 이제 구매요청 목록 품목 구성 페이지에 예상대로 표시됩니다. 이전에는 견본 선택기가 구매요청 목록 품목 구성 페이지에 드롭다운 필드로 표시되었습니다.

![해결된 문제](../assets/fix.svg) <!--ACP2E-1968-->사용 시 [회사 GraphQL 쿼리](https://developer.adobe.com/commerce/webapi/graphql/schema/b2b/company/queries/company/#return-the-company-structure) 회사 세부 정보를 반환하기 위해 이제 결과가 오류 없이 성공적으로 반환됩니다.

## B2B v1.4.0

*2023년 6월 13일*

[!BADGE 지원됨]{type=Informative tooltip="지원됨"}[Adobe Commerce 2.4.6-p1](https://experienceleague.adobe.com/docs/commerce-operations/release/notes/security-patches/2-4-6-p1.html). Adobe Commerce 2.4.7-beta1과 호환

이 릴리스에는 B2B 협상 가능 견적 및 여러 버그 수정에 대한 새로운 기능 및 개선 사항이 포함되어 있습니다.

![신규](../assets/new.svg) Adobe Commerce 2.4.7-beta1과의 호환성을 추가했습니다.

![신규](../assets/new.svg) **판매자가 시작한 견적**- 이제 Sellers 는 관리자의 Quote 및 Customer 그리드에서 직접 구매자에 대한 Quote 를 시작할 수 있습니다. 이 기능은 견적 프로세스를 간소화하고 고객의 복잡성을 줄여 줍니다. 고객이 주문을 시작하지 않은 경우 판매자가 고객을 대신하여 신속하게 견적을 생성하고 협상 프로세스를 시작할 수 있습니다. 이전에는 구매자나 판매자가 고객으로 로그인한 경우에만 상점 앞에서만 견적을 작성할 수 있었습니다.

![신규](../assets/new.svg) **라인 항목 할인 및 협상**—<!--B2B-2440--> 견적 내에서 B2B 구매자와 판매자는 이제 라인 항목 수준에서 협상할 수 있으며, 합의에 도달할 때까지 할인을 적용하고 어음을 교환할 수 있습니다. 메모 작성 및 업데이트가 라인 항목 및 견적 내역에 포함되어 커뮤니케이션을 추적합니다. 기존에는 구매자와 판매자가 견적 레벨에서만 어음을 교환하고 할인을 적용할 수 있었다.

![해결된 문제](../assets/fix.svg) 이제 Adobe Commerce은 구매 주문 옵션이 활성화되고 PayPal 결제 옵션으로 생성된 가상 견적이 선택되면 결제 중에 올바른 세부 정보를 표시합니다. 이전에는 이러한 조건에서 합계가 0으로 표시되었습니다.

![해결된 문제](../assets/fix.svg) <!--ACP2E-1504--> 신용 한도가 999를 초과하는 회사를 저장하려고 할 때 유효성 검사 오류가 더 이상 발생하지 않습니다. 이전에는 회사 신용 한도가 999보다 큰 경우 Adobe 커머스에서 쉼표 구분 기호를 삽입했습니다. 이로 인해 유효성 검사 오류가 발생하여 업데이트가 저장되지 않았습니다.

![해결된 문제](../assets/fix.svg) <!--ACP2E-1474-->  이제 협상 가능한 견적이 있는 주문을 할 때 선택한 배송 주소는 변경되지 않습니다. 이전에는 주문 시 선택한 배송 주소가 기본 배송 주소로 변경되었습니다.

![해결된 문제](../assets/fix.svg) <!--ACP2E-1429--> B2B 기능에 대한 저장 구성 설정에서 **[!UICONTROL Enable Shared Catalog direct products price assigning]** 이제 필드가 자동으로 비활성화됩니다. 상점에서는 다음과 같은 경우 숨겨집니다. **[!UICONTROL Enable Company]** 설정 또는 **[!UICONTROL Enable Shared Catalog]** 설정이 로 설정되어 있습니다. **[!UICONTROL No]**.

![해결된 문제](../assets/fix.svg) <!--ACP2E-1683--> 상점 첫 화면에서 회사 계정을 만들 때 이제 Commerce이 회사 등록을 처리하기 전에 이메일 주소를 확인합니다. 이메일 주소가 올바르지 않으면 작업이 실패하고 계정 업데이트가 처리되지 않습니다. 기존에는 이메일 주소가 잘못돼 회사 계정 생성 요청이 실패해도 고객 계정이 생성됐다.

![해결된 문제](../assets/fix.svg) <!--ACP2E-1664--> 공유 카탈로그 및 가격 구조에 큰따옴표가 포함된 제품 SKU에서 더 이상 관리자의 오류가 발생하지 않습니다.

![해결된 문제](../assets/fix.svg) <!--ACP2E-1498--> 게스트 사용자가 다른 고객 그룹의 데이터를 볼 수 없도록 Commerce 애플리케이션에 대한 Vannish 구성을 업데이트했습니다.

### 알려진 문제

에 B2B 1.4.0을 설치하거나 업그레이드하는 경우 [Adobe Commerce 버전 2.4.6-p1](https://experienceleague.adobe.com/docs/commerce-operations/release/notes/security-patches/2-4-6-p1.html), 다음 오류가 발생합니다.

```terminal
Your requirements could not be resolved to an installable set of packages.

  Problem 1
    - Root composer.json requires magento/extension-b2b 1.4.0 -> satisfiable by magento/extension-b2b[1.4.0].
    - magento/extension-b2b 1.4.0 requires magento/security-package-b2b 1.0.4-beta1 -> found magento/security-package-b2b[1.0.4-beta1] but it does not match your minimum-stability.

Installation failed, reverting ./composer.json and ./composer.lock to their original content.
```

B2B 보안 패키지에 대한 수동 종속성을 추가하여 B2B 보안 패키지에 대한 수동 종속성을 추가하여 이 문제를 해결할 수 있습니다. [안정성 태그](https://getcomposer.org/doc/04-schema.md#package-links). 자세한 내용은 [Adobe Commerce 기술 자료](https://experienceleague.adobe.com/docs/commerce-knowledge-base/kb/troubleshooting/installation-and-upgrade/b2b-1.4.0-installation-fails-on-adobe-commerce-2.4.6-p1-on-premises.html).

## B2B v1.3.5

*2023년 3월 14일*

[!BADGE 지원됨]{type=Informative tooltip="지원됨"}

![신규](../assets/new.svg) Adobe Commerce 2.4.6-p2와의 호환성을 지원하기 위해 B2B 버전 1.3.5-p2가 릴리스되었습니다.

![신규](../assets/new.svg) Adobe Commerce 2.4.6-p1과의 호환성을 지원하기 위해 B2B 버전 1.3.5-p1이 릴리스되었습니다.

>[!NOTE]
>
>Commerce을 2.4.6에서 [최신 릴리스](https://experienceleague.adobe.com/docs/commerce-operations/release/versions.html#2.4.6)지원되는 B2B 1.3.5 패치 릴리스로 업데이트해야 합니다. 또는 B2B 확장을 버전 1.3.5에서 버전 1.4.0 이상으로 업그레이드하여 최신 기능을 받으십시오.

![신규](../assets/new.svg) Adobe Commerce 2.4.6에 대한 지원이 추가되었습니다.

![해결된 문제](../assets/fix.svg) <!--- ACP2E-689--> 이제 Adobe Commerce은 구매 주문 옵션이 활성화되고 PayPal 결제 옵션으로 생성된 가상 견적이 선택되면 결제 중에 올바른 세부 정보를 표시합니다. 이전에는 이러한 조건에서 합계가 0으로 표시되었습니다.

![해결된 문제](../assets/fix.svg) <!--- ACP2E-609--> 에 대한 고객 그룹 목록 **범주 검색 허용** 설정에 공유 카탈로그와 관련된 고객 그룹이 더 이상 포함되지 않습니다.

![해결된 문제](../assets/fix.svg) <!--- ACP2E-1244--> 이제 세금/VAT 번호 고객 속성은 관리자 및 상점 모두의 회사 관리자 계정에서 예상대로 작동합니다. 사용자 정의 세금/VAT 속성은 더 이상 회사 계정을 만드는 데 필요하지 않습니다. 이전에는 판매자가 사용자 정의 세금/VAT 속성으로 회사 계정을 만들 때 Adobe Commerce에서 상점 및 관리자 모두에 유효성 검사 오류가 발생했습니다.

![해결된 문제](../assets/fix.svg) <!--- ACP2E-1236--> 이제 특정 범위에서 공유 카탈로그 기능을 비활성화하는 것이 제대로 작동합니다. 이전에는 판매자가 공유 카탈로그 구성을 저장하면 Adobe Commerce이 잘못된 범위를 설정했습니다.

![해결된 문제](../assets/fix.svg) <!--- ACP2E-1203--> 이제 관리자 사용자는 회사 사용자에 대한 고객 사용자 지정 속성 값을 저장할 수 있습니다. 이전에는 회사 사용자의 고객 사용자 지정 특성을 저장할 수 없었습니다.

![해결된 문제](../assets/fix.svg) <!--- ACP2E-1221--> 이미 많은 회사 권한이 할당된 경우 GraphQL을 통해 제공된 회사 권한의 유효성 검사로 성능 문제가 해결됩니다.

![해결된 문제](../assets/fix.svg) <!--- ACP2E-1242--> 빠른 주문 을 사용하여 사용 가능한 재고를 초과하는 수량의 제품을 장바구니에 추가하면 Adobe Commerce에서 더 이상 오류가 장바구니에 표시되지 않습니다.

![해결된 문제](../assets/fix.svg) <!--- ACP2E-1090--> 의 성능 `SELECT` 회사 권한 작업이 개선되었습니다.

![해결된 문제](../assets/fix.svg) <!--- ACP2E-2456--> 이제 쿼리 중인 카테고리에 명시적으로 설정된 카테고리 권한이 없는 경우 카테고리 쿼리는 스토어 구성 설정에 따라 제품 가격을 반환합니다.

![해결된 문제](../assets/fix.svg) <!--- ACP2E-6829--> 다음 **[!UICONTROL Place Order]** 승인된 견적 요청으로 구매를 완료할 때 버튼이 예상대로 작동합니다. 협상 가능한 견적 문제 `negotiableQuoteCheckoutSessionPlugin` 플러그인이 해결되었습니다.

## B2B v1.3.4

*2022년 8월 9일*

[!BADGE 지원됨]{type=Informative tooltip="지원됨"}

![신규](../assets/new.svg) Adobe Commerce 2.4.5에 대한 지원이 추가되었습니다.

![해결된 문제](../assets/fix.svg) <!--- ACP2E-453-->Adobe Commerce은 API 호출로 기존 회사를 업데이트할 때마다 더 이상 이메일 알림을 보내지 않습니다. 이제 회사가 만들어질 때만 이메일이 전송됩니다.

![해결된 문제](../assets/fix.svg) <!--- ACP2E-406-->이제 Adobe Commerce은 다음과 같은 경우에 협상 가능한 견적의 총계를 올바르게 계산합니다. **[!UICONTROL Enable Cross Border Trade]** 세금 계산 설정을 사용할 수 있습니다.

![해결된 문제](../assets/fix.svg) <!--- ACP2E-322-->구성 가능한 제품은 이제 재고가 업데이트된 후 제품 목록의 마지막 위치로 이동됩니다. **[!UICONTROL Move out of stock to the bottom]** 설정이 활성화되었습니다. 이제 Elasticsearch 색인 정렬 순서가 관리자가 사용할 수 있는 정렬 순서를 따르도록 새 사용자 지정 데이터베이스 쿼리가 구현됩니다. 이전에는 이 설정을 활성화할 때 구성 가능한 제품 및 해당 하위 제품이 목록의 맨 아래로 이동되지 않았습니다.

![해결된 문제](../assets/fix.svg) <!--- ACP2E-308-->이제 구매 주문 이메일에는 다중 사이트 배포에 있는 각 웹 사이트의 이메일 전송 설정이 적용됩니다. 다음에 대한 확인: **[!UICONTROL Disable Email Communications]** 설정이 이메일 큐의 사용자 지정 논리에 추가됩니다. 이전에는 Adobe Commerce이 보조 웹 사이트에 대한 이메일 전송 설정을 준수하지 않았습니다.

![해결된 문제](../assets/fix.svg) <!--- ACP2E-302-->빠른 주문 페이지의 SKU 필드 제목이 명확성을 위해 변경되었습니다.

![해결된 문제](../assets/fix.svg) <!--- ACP2E-543-->이제 Adobe Commerce은 구매자가 다음에 잘못된 SKU를 입력하면 더 자세한 오류 메시지를 표시합니다. **SKU 또는 제품 이름 입력** 필드.

![해결된 문제](../assets/fix.svg) <!--- ACP2E-1753-->다음 **[!UICONTROL Account Created in]** 이제 회사 관리자의 필드는 회사를 저장한 후 예상대로 값을 유지합니다.

![해결된 문제](../assets/fix.svg) <!--- ACP2E-722 -->다음 `customer` 쿼리가 필터링 된 구매요청 목록을 검색할 때 더 이상 빈 결과를 반환하지 않음 `uid`.

![해결된 문제](../assets/fix.svg) <!--- ACP2E-210 -->이(가) 다음 앞에 플러그인을 추가했습니다. `collectQuoteTotals` 스토어 크레딧이 한 번만 적용되도록 를 호출합니다.

![해결된 문제](../assets/fix.svg) <!--- ACP2E-665 -->이제 관리자가 관리자에서 계정을 삭제하면 고객이 로그인 페이지로 리디렉션됩니다. 이전에는 Adobe Commerce에서 오류가 발생했습니다. 플러그인(`SessionPlugin`) 코드 블록은 이제 `try…catch` 차단합니다. 이전에는 이 코드가 일반 예외 처리 블록 내에 래핑되지 않았습니다.

![해결된 문제](../assets/fix.svg) <!--- ACP2E-661 --> 모바일 모드의 빠른 주문 페이지에서 **입력** 유효한 제품 이름 또는 SKU를 입력하면 이제 구매자가 예상대로 다음 필드로 이동합니다.

![해결된 문제](../assets/fix.svg) <!--- ACP2E-607 -->이제 회사 이름이 체크아웃 워크플로의 청구 및 배송 주소 섹션에 예상대로 표시됩니다.

![해결된 문제](../assets/fix.svg) <!--- ACP2E-375 -->다음 경우에 스토어 크레딧을 사용할 수 없습니다. **[!UICONTROL Zero Subtotal Checkout]** 결제 방법을 사용할 수 없습니다. 이전에는 관리자가 주문을 배치하는 동안 크레딧 저장 확인란이 작동하지 않았습니다. 애플리케이션에서 스토어 크레딧을 사용하여 주문하지 않았으며 다음 오류를 표시했습니다. `The requested Payment Method is not available`.

## B2B v1.3.3

*2022년 8월 9일*

[!BADGE 지원됨]{type=Informative tooltip="지원됨"}

![신규](../assets/new.svg) Adobe Commerce 2.4.4에 대한 지원이 추가되었습니다.

![해결된 문제](../assets/fix.svg) <!--- MC-41985--> 100,000개 이상의 회사 역할을 가진 배포에서 Adobe Commerce 2.3.x에서 Adobe Commerce 2.4.x로 업그레이드하는 데 필요한 시간이 크게 단축되었습니다.

![해결된 문제](../assets/fix.svg) <!--- MC-42153--> POST `V1/order/:orderId/invoice` 이제 요청은 다음과 같은 경우에 부분 송장 생성을 지원합니다. **[!UICONTROL Payment on Account]** 결제 방법을 사용할 수 있습니다. 이전에는 Adobe Commerce에서 다음 오류가 발생했습니다. `An invoice for partial quantities cannot be issued for this order. To continue, change the specified quantity to the full quantity`. [GitHub-32428](https://github.com/magento/magento2/issues/32428)

![해결된 문제](../assets/fix.svg) <!--- MC-41975--> 이제 PayPal Payflow Pro는 고객의 장바구니에 다른 제품이 포함되어 있을 때 B2B 협상가능 견적에 대해 예상대로 작동합니다. 이제 Adobe Commerce이 주문을 성공적으로 처리하고 예상대로 고객에게 이메일을 전송합니다. 이전에는 Adobe Commerce에서 치명적인 오류가 발생했으며 값이 0인 확인 이메일을 고객에게 보냈습니다.

![해결된 문제](../assets/fix.svg) <!--- MC-41819--> 이제 공유 카탈로그의 일부 제품을 제외한 후 페이지 매김이 카탈로그 검색 결과 페이지에 올바르게 표시됩니다.

![해결된 문제](../assets/fix.svg) <!--- MC-42886--> 이제 고객 사용자 지정 특성은 관리자에서 회사 사용자를 생성하거나 저장할 때 예상대로 저장됩니다.

![해결된 문제](../assets/fix.svg) <!--- MC-42927--> 다음 **[!UICONTROL Submit]** 이제 한 번의 클릭으로 여러 양식을 제출할 수 없게 되면 새 회사 만들기 양식의 단추가 비활성화됩니다. 이전에는 이 버튼을 반복적으로 클릭하여 이 양식을 여러 번 제출할 수 있었는데 오류가 발생했습니다.

![해결된 문제](../assets/fix.svg) <!--- MC-42787--> Adobe Commerce은 구매자가 재주문이 비활성화된 스토어에 로그인할 때 더 이상 상점 앞에 순서 변경 링크를 표시하지 않습니다.

![해결된 문제](../assets/fix.svg) <!--- MC-43115--> 공유 카탈로그가 활성화되면 이제 SKU의 빠른 주문 검색은 대소문자를 구분하지 않습니다.

![해결된 문제](../assets/fix.svg) <!--- MC-42203--> 이제 회사를 만들 때 고객 특성에 대한 파일을 업데이트할 수 있습니다. 이전에는 형식의 첨부 파일이 있는 회사를 만들려고 할 때 `File`, Adobe Commerce이 회사를 만들지 않고 예외 로그에 이 오류를 기록했습니다. `Something went wrong while saving file`.

![해결된 문제](../assets/fix.svg) <!--- MC-42242--> 이제 ( )이 있는 사용자 지정 특성이 있는 고객 계정으로 회사를 만들 수 있습니다.`File`) 또는 (`Image`) 유형. 이전에는 계정에 이러한 사용자 지정 가능한 옵션 중 하나가 있는 경우 회사 편집 페이지 로더가 확인되지 않았으므로 회사 세부 정보를 편집할 수 없었습니다.

![해결된 문제](../assets/fix.svg) <!--- MC-42268--> 다음 `products` 이제 쿼리가 정확한 값을 반환합니다. `total_count` 공유 카탈로그가 활성화된 경우 필드.

![해결된 문제](../assets/fix.svg) <!--- MC-42203-->  이제 회사를 만들 때 고객 특성에 대한 파일을 업데이트할 수 있습니다. 이전에는 형식의 첨부 파일이 있는 회사를 만들려고 할 때 `File`, Adobe Commerce이 회사를 만들지 않고 예외 로그에 이 오류를 기록했습니다. `Something went wrong while saving file`.

![해결된 문제](../assets/fix.svg) <!--- MC-43178--> 다음 _회사 구성_ 및 _회사 만들기_ 이제 온라인 배송 방법을 사용하지 않도록 설정한 후에도 페이지가 예상대로 작동합니다. 비활성화된 배송 모듈을 처리하지 못하도록 확인이 추가되었습니다. 이전에는 Adobe Commerce에 다음 오류가 표시되었습니다. `Type Error occurred when creating object: Magento\CompanyShipping\Model\Source\ShippingMethod, Too few arguments to function Magento\CompanyShipping\Model\Source\ShippingMethod::__construct(), 1 passed in /var/www/html/elmtup/vendor/magento/framework/ObjectManager/Factory/AbstractFactory.php on line 121 and exactly 2 expected`.

![해결된 문제](../assets/fix.svg) <!--- MC-42214--> 다음 _범주_ 이제 부분 인덱싱 중에 권한이 생성되는 동안 페이지에 일관된 제품 데이터가 표시됩니다. 디렉터리 권한에 대한 새 부분 인덱서가 이 프로세스에 추가되었습니다. 이전에는 인덱서가 실행되는 동안 표시되는 데이터가 올바르지 않았습니다.

![해결된 문제](../assets/fix.svg) <!--- MC-42567--> 다음 `categoryList` 이제 카탈로그 권한이 사용되고 제품이 공유 카탈로그에 할당된 경우 query에서 올바른 제품 수를 반환합니다.

![해결된 문제](../assets/fix.svg) <!--- MC-42528--> 다음 `categoryList` 이제 쿼리는 범주 권한을 준수하며 허용된 범주만 반환합니다. 이전에는 할당 및 할당 해제된 모든 카테고리를 반환했습니다.

![해결된 문제](../assets/fix.svg) <!--- MC-42399--> 다음 `rest/V1/company/{id}` 이제 요청이 반환됩니다. `is_purchase_order_enabled` 속성 값을 예상대로 지정합니다.

![해결된 문제](../assets/fix.svg) <!--- ACP2E-128--> 이제 사용자 지정 고객 속성이에 예상대로 표시됩니다. _회사 관리자_ 탭.

![해결된 문제](../assets/fix.svg) <!--- ACP2E-130--> 이제 내 계정 페이지의 내 위시리스트 블록이 회사 관리자 및 회사 사용자에게 예상대로 표시됩니다.

![해결된 문제](../assets/fix.svg) <!--- ACP2E-133--> 빠른 주문 오류가 더 이상 장바구니에 표시되지 않습니다. 이전에는 카탈로그에서 SKU를 찾을 수 없을 때 Adobe Commerce이 장바구니에 이 오류를 표시했습니다.  `The SKU was not found in the catalog`.

![해결된 문제](../assets/fix.svg) <!--- ACP2E-194--> 공유 카탈로그 저장 작업이 더 빨리 실행되도록 최적화되었습니다. 이전에는 많은 고객 그룹과 공유 카탈로그를 저장하는 데 몇 분이 걸릴 수 있었습니다.

![해결된 문제](../assets/fix.svg) <!--- MC-42240--> 이제 Adobe Commerce에서 모든 하위 범주 권한을 삭제합니다. `sharedcatalog_category_permissions` 상위 카테고리가 삭제되는 경우 테이블. 이전에는 상위 범주 데이터만 제거되었습니다.

## B2B v1.3.2

*2022년 8월 29일*

[!BADGE 지원됨]{type=Informative tooltip="지원됨"}

![신규](../assets/new.svg) Adobe Commerce 2.4.3에 대한 지원이 추가되었습니다.

![해결된 문제](../assets/fix.svg) <!--- MC-39862--> 이제 Adobe Commerce에서 만료된 협상 가능 견적에 대한 업데이트 이메일을 성공적으로 보냈습니다. 이전에는 협상 가능 견적이 만료되면 Adobe Commerce에서 업데이트 이메일을 보내지 않았습니다.

![해결된 문제](../assets/fix.svg) <!--- MC-40682--> 이제 Adobe Commerce은 다음과 같은 경우에 곧 만료되고 만료된 협상 가능 견적에 대한 업데이트 이메일을 성공적으로 전송합니다. `cron` 작업이 누락되었습니다.

### 회사

![해결된 문제](../assets/fix.svg) <!--- MC-41542--> 새 회사 계정 만들기 페이지 국가 드롭다운 필드에 더 이상 빈 옵션 값이 나열되지 않습니다. 이전에는 처음 두 개의 옵션 값과 국가 코드가 있었습니다 `AN` 이(가) 비어 있습니다.

![해결된 문제](../assets/fix.svg) <!--- MC-41260--> 클릭 **[!UICONTROL Return]** 이제 회사 사용자가 만든 주문에 대한 단추가 예상대로 관리 사용자를 반환 만들기 페이지로 리디렉션합니다. 이전에는 관리자가 주문 내역 페이지로 리디렉션되었습니다.

![해결된 문제](../assets/fix.svg) <!--- MC-40798--> Adobe Commerce은 을 실행할 때 더 이상 메모리 부족 오류와 함께 실패하지 않습니다. `app/code/Magento/PurchaseOrder/Setup/Patch/Data/InitPermissions.php::apply` 다음 기간 동안 메서드 `bin/magento setup:upgrade`. 이전에는 Adobe Commerce에서 권한을 초기화할 때 일괄 처리 크기를 사용하지 않고 대신 모든 회사 역할의 컬렉션을 로드했습니다.

![해결된 문제](../assets/fix.svg) <!--- MC-40551--> 이제 회사 사용자는 고객 사용자 지정 속성 값을 편집하고 업데이트할 수 있습니다. 이전에는 이러한 속성이 작성 및 편집 사용자 양식과 제대로 바인딩되지 않았습니다. 회사 사용자가 다른 속성 값을 입력할 수 있지만 Adobe Commerce이 이러한 값을 올바르게 저장하지 않았습니다.

![해결된 문제](../assets/fix.svg) <!--- MC-32653--> 이제 회사 역할 권한에 대한 리소스 트리를 예상대로 번역할 수 있습니다. 이전에는 올바른 번역 파일이 있어도 권한 트리가 번역되지 않았습니다.

![해결된 문제](../assets/fix.svg) <!--- MC-40358--> 이제 Adobe Commerce은 예상대로 B2B 사용자에 대한 사용자 지정 고객 속성 값을 저장합니다. 이전에는 사용자 지정 고객 특성이 포함된 회사 계정을 만들면 템플릿 오류가 발생했으며, Adobe Commerce에서 양식을 성공적으로 로드하지 못했습니다. 의 레이아웃에 인수 추가 `company_create_account` 이 문제가 해결되었습니다.

![해결된 문제](../assets/fix.svg) <!--- MC-41721--> 모든 사용자 표시, 활성 사용자 표시 및 비활성 사용자 표시와 같은 회사 사용자 필터가 이제 예상대로 작동합니다. 이전에는 회사 사용자 페이지에서 작업을 필터링하면 JavaScript 오류가 발생했습니다.

### 회사 신용

![해결된 문제](../assets/fix.svg) <!--- MC-41551--> 이제 웹 사이트 수준 권한만 포함하는 제한된 계정을 가진 관리자는 웹 사이트와 다른 통화를 사용하는 회사를 만들 수 있습니다.

![해결된 문제](../assets/fix.svg) <!--- MC-41523--> 이제 Adobe Commerce에서 올바른 회사 이메일을 보냅니다. `from` 이메일 주소 및 범위. 이전에는 Adobe Commerce에서 회사 크레딧 할당 또는 업데이트 이메일을 보낼 때 웹 사이트 범위를 고려하지 않았습니다.

### 빠른 주문

![해결된 문제](../assets/fix.svg) <!--- MC-42104--> CSV 파일에서 빠른 주문을 사용하여 주문을 만들면 이제 존재하지 않는 SKU에서 예상대로 작동합니다.

![해결된 문제](../assets/fix.svg) <!--- MC-40268--> 이제 빠른 주문을 사용하여 여러 SKU를 검색하면 예상대로 작동합니다. 이전에는 결과에 중복된 항목이 포함되어 있었습니다.

![해결된 문제](../assets/fix.svg) <!--- MC-40261--> 이제 빠른 주문 동안 SKU를 사용하여 여러 제품을 선택할 때 추가된 제품 목록 표시에 소문자 및 대문자로 입력된 SKU가 동일하게 처리됩니다.

![해결된 문제](../assets/fix.svg) <!--- MC-40225--> 이제 빠른 주문을 사용하면 구매자가 지정한 수량으로 제품이 추가됩니다. 기존에는 Adobe Commerce이 구매자 지정 수량이 1개를 초과하는 경우에만 제품 1개를 추가했다.

![해결된 문제](../assets/fix.svg) <!--- MC-41283--> 이제 빠른 주문 자동 완성 기능이 일부 SKU에서 작동합니다.

![해결된 문제](../assets/fix.svg) <!--- MC-41299--> 이제 Adobe Commerce에 로 구성된 제품이 표시됩니다. **개별적으로 표시되지 않음** 빠른 주문 페이지의 자동 제안 목록 및 검색 결과에서 참조할 수 있습니다.

![해결된 문제](../assets/fix.svg) <!--- MC-42402--> 이제 구매자는 빠른 주문 양식을 사용하여 대소문자 문자가 포함된 SKU별 여러 제품을 추가할 수 있습니다. 이전에는 첫 번째 제품만 추가되었습니다.

### 협상 가능한 견적

![해결된 문제](../assets/fix.svg) <!--- MC-41232--> 이제 구매자는 URL 필드에 협상 가능 견적에 대한 링크를 붙여넣고 성공적으로 로그인한 후 협상 가능 견적 페이지로 리디렉션됩니다. 이전에는 쇼핑객이 내 계정 페이지로 리디렉션되었습니다.

![해결된 문제](../assets/fix.svg) <!--- MC-39317--> 이제 재정렬은 체크아웃 중에 생성된 고객 계정에 대해 사용자 정의 가능 날짜 옵션이 있는 제품이 포함된 주문에 대해 예상대로 작동합니다. 이전에는 Adobe Commerce에서 순서 변경을 처리하지 않고 이 오류를 표시했습니다. `The product has required options. Enter the options and try again`.

![해결된 문제](../assets/fix.svg) <!--- MC-39063--> 구매 발주 모듈이 비활성화되면 체크아웃 중에 더 이상 협상 가능 견적의 배송 주소를 편집할 수 없습니다. 이 동작은 의 이전 수정 사항에서 발생했습니다. `isQuoteAddressLocked` 은(는) 협상 견적 체크아웃 렌더러에서 제거되었습니다.

![해결된 문제](../assets/fix.svg) <!--- MC-38967--> 이제 판매자는 관리자의 협상 가능한 견적에 제품을 추가할 수 있습니다.

### 구매 주문

![해결된 문제](../assets/fix.svg) <!--- MC-39983--> 이제 Adobe Commerce은 PayPal Express Checkout을 사용하여 구매 주문을 할 때 예상대로 다음과 같은 오류 메시지를 표시합니다. **[!UICONTROL Name Prefix]** 속성이 로 설정되어 있습니다. `required`. 이전에는 Adobe Commerce에서 주문을 하거나 오류 메시지를 표시하지 않았습니다.

![해결된 문제](../assets/fix.svg) <!--- MC-39620--> 이제 Google Tag Manager가 활성화되면 구매 주문 모듈의 청구 주소에 대한 UI 구성 요소에서 견적 주소를 올바르게 사용합니다. 이전에는 결제 페이지에서 JavaScript 오류가 발생했습니다.

### 구매요청 목록

![해결된 문제](../assets/fix.svg) <!--- MC-40426--> 판매자는 이제 POST을 사용할 수 있습니다. `rest/all/V1/requisition_lists` 고객에 대한 구매요청 목록을 생성하는 끝점입니다. 이전에는 Adobe Commerce에서 구매요청 목록을 만들려고 할 때 이 400 오류가 발생했습니다. `Could not save Requisition List`.

![해결된 문제](../assets/fix.svg) <!--- MC-41123--> 다음 **[!UICONTROL Add to Requisition List]** 장바구니에 품절된 제품이 포함되어 있을 때 장바구니의 재고 제품에 대한 버튼이 표시됩니다. 이전에는 장바구니에 두 개의 제품이 들어 있는데 그 중 하나가 품절이면 _[!UICONTROL Add to Requisition List]_제품 중 하나에 단추가 표시되지 않았습니다.

![해결된 문제](../assets/fix.svg) <!--- MC-40877--> 이제 REST API를 사용하여 구매요청 목록에 제품을 추가할 수 있습니다.

![해결된 문제](../assets/fix.svg) <!--- MC-40155--> 구매요청 목록 **[!UICONTROL Latest Activity Date]** 이제 값이 로케일 형식을 따릅니다.

![해결된 문제](../assets/fix.svg) <!--- MC-39580--> Adobe Commerce은 요청 목록에서 번들 제품을 편집할 때 더 이상 치명적인 오류를 표시하지 않습니다.

![해결된 문제](../assets/fix.svg) <!--- MC-40454--> 이제 사용자 지정 가능한 옵션이 있는 제품을 추가할 때 Adobe Commerce에 올바른 제품 가격이 표시됩니다 `(File)` 구매요청 목록에서 위시리스트로 이동합니다. 업로드된 파일에 대한 링크도 예상대로 표시됩니다. 이전에는 Adobe Commerce에 잘못된 제품 가격이 표시되고 파일에 대한 링크가 표시되지 않았습니다.

![해결된 문제](../assets/fix.svg) <!--- MC-36383--> 사용자 지정 가능한 옵션이 있는 제품 `(File)` 이제 구매요청 목록에서 장바구니에 추가할 수 있습니다.

### 공유된 카탈로그

![해결된 문제](../assets/fix.svg) <!--- MC-40497--> 이제 특정 웹 사이트로 역할이 제한된 관리자는 공유 카탈로그를 만들고 보고 편집할 수 있습니다. 이전에는 제한된 역할을 가진 관리자가 공유 카탈로그를 만들려고 할 때 Adobe Commerce에서 치명적인 오류가 발생했습니다.

![해결된 문제](../assets/fix.svg) <!--- MC-41337--> 이제 계층화된 탐색 결과에 필터링된 속성을 사용하는 제품의 정확한 수가 포함되어 구매자는 여러 필터를 적용할 수 있습니다. 이전에는 필터를 하나만 적용할 수 있었지만 Adobe Commerce은 계층 탐색에서 부정확한 제품 수를 표시했습니다.

![해결된 문제](../assets/fix.svg) <!--- MC-40779--> 이제 Adobe Commerce은 검색 결과의 계층화된 탐색 필터에 제품 수를 올바르게 표시합니다. 이전에는 검색 결과 페이지에 대한 플러그인이 Elasticsearch을 사용하지 않았지만 데이터베이스에 새 쿼리를 발행했습니다.

![해결된 문제](../assets/fix.svg) <!--- MC-39978--> 판매자가 기본 공유 카탈로그에서 모든 제품을 삭제할 때 Adobe Commerce은 더 이상 계층 가격을 삭제하지 않습니다.

![해결된 문제](../assets/fix.svg) <!--- MC-39802--> 이제 필터가 현재 카테고리로 필터링되고 공유 카탈로그가 활성화될 때 모든 페이지에 올바르게 표시됩니다. 이전에는 필터가 현재 페이지에 대해서만 잘못 계산되었으며 현재 카테고리로 필터링되지 않았습니다.

![해결된 문제](../assets/fix.svg) <!--- MC-39522--> 더 GraphQL `products` 공유 카탈로그가 활성화되면 쿼리는 더 이상 공유 카탈로그에 할당되지 않은 제품에 대한 제품의 가격 범위와 범주를 반환하지 않습니다. 이전에는 의 제품 자체가 반환되지 않았더라도 쿼리에서 제품의 집계를 반환했습니다 `items` 배열입니다.

## B2B v1.3.1

*2021년 2월 9일*

[!BADGE 지원됨]{type=Informative tooltip="지원됨"}

![신규](../assets/new.svg) Adobe Commerce 2.4.2에 대한 지원이 추가되었습니다.

![신규](../assets/new.svg) 이제 온라인 결제 방법이 구매 발주에 대해 지원됩니다.

![해결된 문제](../assets/fix.svg) 구성 가능한 제품을 이전 주문에 사용한 경우 구매요청 목록에서 직접 장바구니에 추가하면 시스템 오류가 더 이상 반환되지 않습니다.

![해결된 문제](../assets/fix.svg) 이제 분할 데이터베이스 구성이 배포될 때 Adobe Commerce에 구매 발주에 대한 내 승인 필요 탭이 올바르게 표시됩니다.

![해결된 문제](../assets/fix.svg) 이제 Adobe Commerce은 구매 주문을 볼 때 번들 제품 및 기프트 카드에 대한 세부 정보를 표시합니다.

![해결된 문제](../assets/fix.svg) 이제 쇼핑객은 스토어에서 탐색하는 동안 계정에 로그인한 후 예상대로 리디렉션됩니다. **[!UICONTROL Website Restriction]** 활성화됨 및 **[!UICONTROL Restriction Mode]** 이(가) (으)로 설정됨 `Private Sales: Login Only`. 이전에는 쇼핑객이 상점 홈 페이지로 리디렉션되었습니다. <!--- MC-38934-->

![해결된 문제](../assets/fix.svg) 이제 주문 내역이 많은 고객(13000보다 큼)을 포함하는 B2B 회사 계층이 있는 배포의 회사 관리자 계정 대시보드 페이지에 예상대로 로드됩니다. 이전에는 주문 내역이 느리게 로드되거나 전혀 로드되지 않았고 Adobe Commerce에 503 오류가 표시되었습니다. <!--- MC-38830-->

![해결된 문제](../assets/fix.svg) 사용자 정의 가능한 옵션이 있는 구성되지 않은 제품을 범주 페이지에서 구매요청 목록에 추가할 때 Adobe Commerce에 더 이상 동일한 경고 메시지가 여러 개 표시되지 않습니다. <!--- MC-38342-->

![해결된 문제](../assets/fix.svg) 이제 B2B 공유 카탈로그가 활성화되면 카테고리 페이지에 예상대로 새 제품과 중복 제품이 표시됩니다. <!--- MC-38307-->

![해결된 문제](../assets/fix.svg) 이제 Adobe Commerce이 올바른 을(를) 유지 관리합니다. `store_id` 회사의 고객 그룹이 업데이트될 때 회사 관리자와 연결됩니다. 이전에는 `store_id` 그룹이 업데이트되면 기본 저장소로 변경되었습니다. <!--- MC-38196-->

![해결된 문제](../assets/fix.svg) 이제 Adobe Commerce은 그룹화된 제품을 장바구니에 추가하는 것과 동일한 방식으로 그룹화된 제품을 구매요청 목록에 간단한 제품 목록으로 저장합니다. 이전에는 Adobe Commerce이 그룹화된 제품을 저장한 방식으로 인해 구매요청 목록의 그룹화된 제품에 대한 링크가 그룹화된 제품이 아닌 항상 간단한 제품으로 리디렉션되었습니다. <!--- MC-38049-->

![해결된 문제](../assets/fix.svg) 이제 다음을 기준으로 주문을 필터링할 수 있습니다. **[!UICONTROL Company Name]** CSV 형식으로 주문 정보를 내보낼 때 필드. 이전에는 Adobe Commerce이에 오류를 기록했습니다. `var/export/{file-id}`. <!--- MC-37785-->

![해결된 문제](../assets/fix.svg) 이제 상점에서 새 구매요청 목록 생성 탭을 선택하면 Adobe Commerce에 구매요청 목록 생성 팝업이 예상대로 표시됩니다. <!--- MC-37915-->

![해결된 문제](../assets/fix.svg) 이제 구매요청 목록에는 목록에 추가된 모든 그룹화된 제품 및 수량이 포함됩니다. 이전에는 판매자가 제품 세부 사항 페이지에서 제품을 추가한 후 구매요청 목록으로 이동하면 Adobe Commerce에 다음 오류가 표시되었습니다. `1 product(s) require your attention - Options were updated. Please review available configurations`. <!--- MC-37621-->

![해결된 문제](../assets/fix.svg) 이제 다중 사이트 배포에서 회사를 만들 때 올바른 스토어 보기가 관련 웹 사이트와 연결됩니다. 이전에는 회사를 만들 수 없었고 Adobe Commerce에 다음 오류가 표시되었습니다. `The store view is not in the associated website`. <!--- MC-37488-->

![해결된 문제](../assets/fix.svg) 빠른 주문을 사용하여 SKU별로 제품을 주문하면 더 이상 CSV 파일에 중복 제품 수량이 발생하지 않습니다. <!--- MC-37427-->

![해결된 문제](../assets/fix.svg) 다음 **[!UICONTROL Add to Cart]** 버튼을 클릭할 때 더 이상 차단되지 않습니다. _[!UICONTROL Enter Multiple SKUs]_빠른 주문 페이지의 섹션에 빈 값이 있습니다. 대신 이제 Adobe Commerce에 유효한 SKU를 입력하라는 메시지가 표시됩니다. <!--- MC-37387-->

![해결된 문제](../assets/fix.svg) 이제 구매요청 목록에서 제품 검토를 실행할 때 Adobe Commerce은 제품 페이지에 이 메시지를 표시합니다. `You submitted your review for moderation`. 리뷰는 보류 중인 리뷰 페이지(관리자)에도 표시됩니다 **[!UICONTROL Marketing]** > **[!UICONTROL Pending Reviews]**). 이전에는 Adobe Commerce이 보류 중인 검토 목록에 검토를 추가했지만 제품 페이지에 404 오류가 발생했습니다. <!--- MC-37119-->

![해결된 문제](../assets/fix.svg) 의 성능 `sharedCatalogUpdateCategoryPermissions` 소비자는 향상되었습니다. 공유 카탈로그를 만든 후 카탈로그 권한 인덱서가 이제 모든 고객 그룹이 아닌 공유 카탈로그의 고객 그룹 ID만 사용합니다. <!--- MC-36770-->

![해결된 문제](../assets/fix.svg) 이제 구매자의 기본이 아닌 주소와 연결된 사용자 지정 고객 주소 속성 필드가 storefront 체크아웃 워크플로우에서 예상대로 저장됩니다. <!--- MC-36630-->

![해결된 문제](../assets/fix.svg) 이제 관리자 REST API( 를 통해 스토어의 기본 공유 카탈로그에 속하는 제품을 구매자에게 주문할 수 있습니다.`rest/V1/carts/{<CART_ID>/items`)을 참조하십시오. 이제 Adobe Commerce은에서 공유 카탈로그 권한을 확인하기 전에 제품이 공개 카탈로그에 할당되었는지 확인합니다. `\Magento\SharedCatalog\Plugin\Quote\Api\ValidateAddProductToCartPlugin::beforeSave`. 이전에는 Adobe Commerce이 제품을 구매자의 장바구니에 추가하지 않았으며 다음 오류를 표시했습니다. `No such shared catalog entity`. <!--- MC-36535-->

![해결된 문제](../assets/fix.svg) 이제 Adobe Commerce은 Adobe Commerce 스토어 주소에서 새 회사 사용자 등록 이메일을 보냅니다. 이전에는 회사 관리자 주소로 이 이메일을 보냈습니다. <!--- MC-36480-->

![해결된 문제](../assets/fix.svg) 이제 Adobe Commerce은 판매자가 새 속성을 저장하도록 허용하기 전에 사용자 지정 속성에서 예약된 회사 속성 이름이 중복되는지 확인합니다. <!--- MC-36282-->

![해결된 문제](../assets/fix.svg) 다음 `credit_history` 이제 질의는 최초 할당 금액과 구매 금액 모두에 대해 지정된 회사의 신용 내역을 반환합니다. 이전에는 이 쿼리에서 오류를 반환했습니다.

![해결된 문제](../assets/fix.svg) 다음 **[!UICONTROL Company]** 및  **[!UICONTROL Job Title]** 계정 정보 편집 페이지의 필드는 더 이상 편집할 수 없습니다.

### 알려진 문제

- B2B 구매자는 온라인 결제 방법을 사용하여 일반적인 구매 발주 흐름을 우회할 수 있습니다. 이 시나리오는 구매자가 전체 체크아웃 합계를 0으로(예: 프로모션 코드나 기프트 카드) 줄인 다음 코드나 기프트 카드를 제거할 수 있는 경우에 발생할 수 있습니다. 이러한 상황에서도 Adobe Commerce은 여전히 지정된 카탈로그에 있는 항목의 가격을 기반으로 정확한 금액을 주문합니다. **_해결 방법_**: 구매 주문 승인을 위해 온라인 결제 방법이 활성화된 경우 기프트 카드 및 쿠폰 코드를 비활성화합니다. <!--- B2B-1603-->

- 구매자는 PayPal Express Checkout을 사용하여 구매 주문에서 주문하려고 할 때 장바구니로 리디렉션됩니다. **[!UICONTROL In-Context Mode]** 이(가) 비활성화되었습니다. <!--- B2B-1604-->

- 구매자가 구매 주문을 만든 다음 체크아웃 페이지로 이동할 때 Adobe Commerce에 404 오류가 표시되는 경우가 있습니다. 이 오류는 구매자가 이전에 온라인 결제 방법으로 다른 구매 발주를 만든 후 이전 구매를 완료하지 않고 체크아웃 페이지로 이동한 경우 발생합니다. 구매자는 여전히 구매 발주를 할 수 있습니다. **_해결 방법_**: 없음. <!--- B2B-1605-->

- 특정 결제 방법에 대한 할인은 구매자가 최종 체크아웃 중에 결제 방법을 변경하는 경우에도 구매 발주에 대한 체크아웃 중에 유지됩니다. 이에 따라 고객은 자신이 받을 수 없는 할인을 받을 수 있다. 이 문제는 결제 방법이 변경되더라도 원래 결제 방법에 대한 장바구니 규칙이 계속 적용되기 때문에 발생합니다. **_해결 방법_**: 없음. 다음을 참조하십시오. [Adobe Commerce 2.4.2 B2B 알려진 문제: 결제 방법이 변경된 후에도 온라인 구매 발주에 대한 할인이 유지됩니다](https://experienceleague.adobe.com/docs/commerce-knowledge-base/kb/troubleshooting/payments/magento-2.4.2-b2b-discount-remains-pay-method-change.html) _기술 자료_ 기사. <!-- B2B-1012 -->

- 다음 `deleteRequisitionListOutput` 질의는 나머지 구매요청 목록 대신 삭제된 구매요청 목록에 대한 상세내역을 반환합니다. <!--- MC-39894-->

## B2B v1.3.0

*2020년 10월 15일*

[!BADGE 지원됨]{type=Informative tooltip="지원됨"}

이 릴리스에는 주문 승인, 배송 방법, 장바구니 및 관리 작업 로깅에 대한 개선 사항이 포함되어 있습니다.

![신규](../assets/new.svg) Adobe Commerce 2.4.1에 대한 지원이 추가되었습니다.

![신규](../assets/new.svg) B2B 주문 승인을 개선하여 사용성을 개선하고 구매 발주에 대한 대량 작업을 수행할 수 있습니다.

![신규](../assets/new.svg) 이제 B2B 판매자는 각 회사에 제공되는 배송 방법을 제어할 수 있습니다.<!--- BUNDLE-160 161 162 -->

![신규](../assets/new.svg) 판매자는 이제 사용자가 단일 작업으로 장바구니의 콘텐츠를 지우고 각 웹 사이트에서 독립적으로 이 기능을 구성할 수 있습니다 <!--- BUNDLE-108 -->

![신규](../assets/new.svg) 이제 B2B 구매자는 개별 품목 또는 장바구니의 전체 콘텐츠를 구매요청 목록에 바로 추가할 수 있습니다. <!--- BUNDLE-145 144-->

![신규](../assets/new.svg) B2B 판매자는 결제 방법으로 계정에서 결제를 사용하여 고객을 대신하여 관리자의 주문을 생성할 수 있습니다. <!--- BUNDLE-166 178-->

![신규](../assets/new.svg) 이제 판매자는 고객의 세부 정보 페이지에서 사용자와 연결된 모든 견적을 직접 볼 수 있습니다. <!--- BUNDLE-139 -->

![신규](../assets/new.svg) 판매자는 이제 Customers Now Online 표를 회사별로 필터링할 수 있습니다. <!--- BUNDLE-137 -->

![신규](../assets/new.svg) 이제 관리자는 Sales Rep 가 Admin에서 고객을 필터링할 수 있습니다. <!--- BUNDLE-110 -->

![신규](../assets/new.svg) 사기 또는 스팸 계정 생성을 줄이기 위해 상인은 이제 상점의 새 회사 요청 양식에서 Google reCAPTCHA를 활성화할 수 있습니다. <!--- BUNDLE-154 -->

![신규](../assets/new.svg) 회사 모듈에서 수행한 관리 작업이 이제 관리 작업 로그에 기록됩니다. 작업은 모든 관련 회사 모듈에서 기록됩니다. `Company`, `NegotiableQuote`, `CompanyCredit`, `SharedCatalog`.  <!--- BUNDLE-180 181 182 183 -->

![해결된 문제](../assets/fix.svg) Adobe Commerce에 더 이상 **[!UICONTROL Delete customer]** 단추 **고객** B2B가 설치된 배포에서 로그인한 관리자가 고객을 삭제할 권한이 없는 경우 페이지를 표시합니다. <!--- MC-35655-->

![해결된 문제](../assets/fix.svg) 고객 그리드에서 고객을 편집할 때 회사에 할당된 고객에 대해 고객 그룹은 더 이상 자동으로 변경되지 않습니다. <!--- MC-35254-->

![해결된 문제](../assets/fix.svg) 판매자가 공유 카탈로그를 만들 때 이제 권한이 자동으로 다음으로 설정됩니다. `Allow` 대상: **[!UICONTROL Display Product Prices]** 및 **[!UICONTROL Add to Cart]** 고객 그룹에 카탈로그 권한 설정에서 이 액세스 권한이 할당될 때 카테고리 내 기능. 이전에는 이러한 설정이 자동으로 로 설정되었습니다. `Deny` 카탈로그 권한이 다음으로 설정된 경우에도 `Allow`.<!--- MC-34792-->

![해결된 문제](../assets/fix.svg) 제품 편집 페이지에서 제품을 편집할 때 더 이상 공유 카탈로그 범주 권한을 덮어쓰지 않습니다.<!--- MC-34777-->

![해결된 문제](../assets/fix.svg) 이제 Adobe Commerce에서 상인이 다음을 활성화할 때 고객이 지정된 신용 한도를 초과할 수 있는 권한이 있음을 확인하는 이메일 알림을 보냅니다. **[!UICONTROL Allow To Exceed Credit Limit]** 설정. 이전에는 Adobe Commerce에서 보낸 알림 이메일에 고객이 한도를 초과할 권한이 없음을 표시했습니다. <!--- MC-34584-->

![해결된 문제](../assets/fix.svg) 이제 번들 제품의 하위 항목에 대해 구매요청 목록의 제품 가격을 둘러싸는 HTML 컨테이너가 올바로 렌더링됩니다. <!--- MC-36331-->

![해결된 문제](../assets/fix.svg) 이제 판매자는 다국어 배포에서 회사를 만들 때 회사 사용자 이메일을 보낼 언어를 지정할 수 있습니다. 이전에는 상인이 적절한 스토어 보기를 선택할 수 있는 드롭다운 메뉴가 표시되지 않았으며 언어는 표시되지 않았습니다.  <!--- MC-35777-->

![해결된 문제](../assets/fix.svg) 이제 사용자 지정 고객 주소 속성 필드가 상점 첫 체크아웃 워크플로우에서 예상대로 표시됩니다. <!--- MC-35607-->

![해결된 문제](../assets/fix.svg) 이제 B2B 기능 구성 탭이 올바르게 열립니다. <!--- MC-35458-->이제 QuickOrder를 사용하여 장바구니에 제품을 추가한 다음 항목을 성공적으로 제거할 수 있습니다. 이전에는 쇼핑객이 QuickOrder를 사용하여 장바구니에 여러 제품을 추가한 다음 제품을 제거해도 제품이 제거되지 않았습니다. <!--- MC-35327-->

![해결된 문제](../assets/fix.svg) 이제 REST API PUT을 사용하여 회사를 업데이트할 수 있습니다. `/V1/company/:companyId` 을(를) 지정하지 않고 요청 `region_id` 상태가 (으)로 구성된 경우 **필요하지 않음**. 이전에는 `region_id` 이(가) 필수가 아닙니다. Adobe Commerce에서 지정하지 않은 경우 오류가 발생합니다. <!--- MC-35304-->

![해결된 문제](../assets/fix.svg) REST API를 사용하여 B2B 회사를 만들거나 업데이트하는 경우(`http://magento.local/rest/V1/company/2`, 여기서 `2` 는 회사 ID를 나타냄), 응답에는 이제 다음에 대한 설정이 포함됩니다. `applicable_payment_method` 또는 `available_payment_methods` 예상대로 <!--- MC-35248-->

![해결된 문제](../assets/fix.svg) 판매자가 를 사용할 때 Adobe Commerce에는 더 이상 404 페이지가 표시되지 않습니다. **입력** 버튼을 클릭합니다. **[!UICONTROL Save]** 상점에 구매요청 목록을 생성할 때 버튼<!--- MC-35094-->

![해결된 문제](../assets/fix.svg) 새 제품이 공개 공유 카탈로그에 할당되면 카테고리 권한이 더 이상 변경되지 않습니다. 이전에는 범주 권한이 중복되었습니다. <!--- MC-34386-->

![해결된 문제](../assets/fix.svg) REST API 끝점 PUT `rest/default/V1/company/{id}`회사 이메일을 업데이트하는 데 사용되는 는 더 이상 대소문자를 구분하지 않습니다. <!--- MC-34308-->

![해결된 문제](../assets/fix.svg) 보상 모듈을 비활성화하면 고객 계정의 B2B 기능에 더 이상 영향을 주지 않습니다. 이전에는 보상 모듈이 비활성화되면 회사 프로필, 회사 사용자 및 역할 및 권한과 같은 B2B 관련 탭이 표시되지 않았습니다.<!--- MC-34191-->

![해결된 문제](../assets/fix.svg) 이제 Adobe Commerce은 회사 계정이 변경될 때 이메일 알림에 올바른 발신자 이름을 사용합니다. 이전에는 Adobe Commerce에서 모든 이메일에 대해 기본 범위에 정의된 일반 연락처 발신자 이름을 사용했습니다. <!--- MC-33917-->

![해결된 문제](../assets/fix.svg) 이제 실제 제품과 가상 제품이 모두 포함된 주문에 대해 다중 배송을 성공적으로 구현할 수 있습니다. <!--- MC-33818-->

![해결된 문제](../assets/fix.svg) 판매자는 이제 _[!UICONTROL Company Users]_다음과 같은 경우 내 계정 및 회사 구조 페이지의 섹션&#x200B;**[!UICONTROL Access Restriction]**활성화됨 및&#x200B;**[!UICONTROL Restriction Mode]**이(가) (으)로 설정됨 `Sales: Login Only`. 이전에는 판매자가 사용자를 만들려고 할 때 Adobe Commerce에서 이 오류가 발생했습니다. `Can not register new customer due to restrictions are enabled`. <!--- MC-33608-->

![해결된 문제](../assets/fix.svg) 고객이 계정 정보를 저장할 때 Adobe Commerce은 더 이상 고객의 고객 그룹을 기본값으로 재설정하지 않습니다. <!--- MC-33554-->

![해결된 문제](../assets/fix.svg) 관리자가 활성 장바구니가 있는 고객을 고객 그룹에 지정할 때 Adobe Commerce에서 더 이상 치명적인 오류가 발생하지 않습니다. <!--- MC-33313-->

![해결된 문제](../assets/fix.svg) Adobe Commerce은 이제 `addToCart` 빠른 주문 및 구매 요청 목록 페이지에 대한 DataLayer 이벤트.  <!--- MC-33295-->

![해결된 문제](../assets/fix.svg) 이제 회사에 할당된 영업 담당자에게 전송되는 알림 이메일에 할당된 회사 로고가 포함됩니다. 이전에는 알림 이메일에 업로드된 회사 로고가 아닌 기본 LUMA 로고가 포함되었습니다. <!--- MC-33232-->

![해결된 문제](../assets/fix.svg) 이제 구매요청 목록에는 목록에 추가된 모든 그룹화된 제품 및 수량이 포함됩니다. 이전에는 판매자가 제품 세부 사항 페이지에서 제품을 추가한 후 구매요청 목록으로 이동하면 Adobe Commerce에 다음 오류가 표시되었습니다. `1 product(s) require your attention - Options were updated. Please review available configurations`. <!--- MC-32877-->

![해결된 문제](../assets/fix.svg) 다음 `products` 이제 쿼리가 정확한 값을 반환합니다. `total_count` 공유 카탈로그가 활성화된 경우 필드. <!--- MC-42268-->

![해결된 문제](../assets/fix.svg) 이제 온라인 배송 방법을 사용하지 않도록 설정한 후 회사 구성 및 회사 만들기 페이지가 예상대로 작동합니다. 비활성화된 배송 모듈을 처리하지 못하도록 확인이 추가되었습니다. 이전에는 Adobe Commerce에 다음 오류가 표시되었습니다. `Type Error occurred when creating object: Magento\CompanyShipping\Model\Source\ShippingMethod, Too few arguments to function Magento\CompanyShipping\Model\Source\ShippingMethod::__construct(), 1 passed in /var/www/html/elmtup/vendor/magento/framework/ObjectManager/Factory/AbstractFactory.php on line 121 and exactly 2 expected`. <!--- MC-43178-->

![해결된 문제](../assets/fix.svg) 통합 테스트 메모리 사용량이 감소하여 테스트 성능이 향상되고 테스트 완료에 필요한 시간이 단축됩니다. <!--- AC-266-->

## B2B v1.2.0

*2020년 7월 28일*

[!BADGE 지원됨]{type=Informative tooltip="지원됨"}

![신규](../assets/new.svg) Adobe Commerce 2.4.0에 대한 지원이 추가되었습니다.

![신규](../assets/new.svg) Storefront Order Search, Marek Mularczyk 의 기여에 대한 추가 감사 [디반테](https://www.divante.com/) 및 커뮤니티 구성원.

![신규](../assets/new.svg) 구매 주문이 향상되고 다시 작성됩니다. 이제 Adobe Commerce에 기본적으로 포함됩니다.

![신규](../assets/new.svg) 구매 주문 승인 규칙이 구현되었습니다. 이러한 규칙을 사용하여 사용자는 주문에 대한 구매 규칙을 생성하여 구매 발주 워크플로우를 제어할 수 있습니다.

![신규](../assets/new.svg) 고객으로 로그인 이 이제 Adobe Commerce에 기본적으로 포함됩니다. 이 기능을 사용하면 사이트 직원이 고객으로 로그인하여 고객이 본 것을 확인할 수 있도록 지원할 수 있습니다.

![해결된 문제](../assets/fix.svg) 이제 속성 집계가 Elasticsearch을 사용하는 계층화된 탐색에 대해 올바르게 작동합니다.

![해결된 문제](../assets/fix.svg) 이제 특수 문자로 주문 검색이 제대로 작동합니다.

![해결된 문제](../assets/fix.svg) 클릭 **[!UICONTROL Clear All]** 이제 Button은 필터를 축소하지 않고 모든 필터를 확장합니다.

![해결된 문제](../assets/fix.svg) 제품 SKU/이름이 이제 주문 내역 검색 필터 요약에 포함됩니다.

![해결된 문제](../assets/fix.svg) 이제 정렬 표시기가 내 구매 발주 그리드에 제대로 표시됩니다.

![해결된 문제](../assets/fix.svg) 이제 승인, 취소, 거부 및 구매 발주 버튼을 한 번만 클릭할 수 있습니다. 이전에는 버튼을 여러 번 클릭할 수 있었습니다.

![해결된 문제](../assets/fix.svg) 이제 구매 주문 승인, 거부, 취소 및 유효성 검사 버튼이 모바일 장치에서 올바르게 렌더링됩니다.

![해결된 문제](../assets/fix.svg) 이전에는 할인이 만료된 구매 발주를 승인하면 전체 금액으로 주문이 처리되었으며 구매 발주 합계는 업데이트되지 않았습니다. 이제 구매 주문 합계가 올바른 합계를 표시하도록 업데이트됩니다.

![해결된 문제](../assets/fix.svg) 2.3.4에서 사용자 정의 확장 속성이 고객 주소에서 견적 주소로 복사되지 않는 문제가 도입되었습니다. 이 문제가 수정되었습니다.

![해결된 문제](../assets/fix.svg) B2B가 설치된 경우 공유 카탈로그에 범주를 할당할 때 SQL 오류가 표시됩니다. 이 문제가 수정되었습니다.

![해결된 문제](../assets/fix.svg) 잘못된 변수 유형 값으로 인해 관리자가 구성 가능한 제품을 주문에 추가할 수 없습니다. 옵션 드롭다운이 채워지지 않습니다. 이 기능은 이제 제대로 작동합니다.

![해결된 문제](../assets/fix.svg) 이전에는 로그인되지 않음 그룹에 대한 범주 권한을 편집할 때 변경 사항을 저장할 때 오류가 발생했습니다. 이 문제가 수정되었습니다.

![해결된 문제](../assets/fix.svg) 스토어 관리자가 공유 카탈로그에 없는 주문에 제품을 추가할 수 있도록 수정 사항이 추가되었습니다. 이전에는 카탈로그에 없는 항목을 추가할 때 오류 메시지가 표시되었습니다.

![해결된 문제](../assets/fix.svg) 이전에는 명령을 실행한 후 `php bin/magento indexer:set-dimensions-mode catalog_product_price website` 공유 카탈로그를 만들려고 하면 오류가 발생합니다. 이 문제가 수정되었습니다.

![해결된 문제](../assets/fix.svg) 회사를 추가하고 기본이 아닌 웹 사이트에 회사 관리자를 할당할 때 잘못된 사이트 ID가 전송되어 오류가 발생했습니다. 이 문제가 수정되었습니다.

![해결된 문제](../assets/fix.svg) 이전에는 고객이 다른 고객 그룹으로 이동한 후 를 사용하여 주문에 제품을 추가했습니다. _빠른 주문_ 은 오류와 함께 실패합니다. 이 문제가 수정되었습니다.

![해결된 문제](../assets/fix.svg) 이전에는 B2B 견적과 함께 WebAPI를 사용하여 체크아웃하려고 할 때 잘못된 값이 API로 전송되어 오류가 발생했습니다. 이 문제가 수정되었습니다.

![해결된 문제](../assets/fix.svg) 이전에는 API를 통해 회사를 &quot;활성&quot;으로 설정할 때 오류가 발생했습니다. 이 문제는 이제 수정되었습니다.

![해결된 문제](../assets/fix.svg) 필요 없는 일로 `form` 태그, 제안된 배송 비용을 변경한 후 Enter 키를 누르면 주문 페이지가 자동으로 새로 고쳐집니다. 이 문제가 수정되었습니다.

![해결된 문제](../assets/fix.svg) 이전에는 카탈로그 페이지에서 제품 표시 제한을 설정할 때 해당 제한이 총 제품 수보다 적으면 오류가 발생했습니다. 이제 해당 기능이 예상대로 작동합니다.

![해결된 문제](../assets/fix.svg) 이전에는 회사 관리자를 변경할 때 원래 관리자 주소가 새 관리자에게 복사되어 두 개의 주소를 제공했습니다. 이제 올바른 주소만 추가됩니다.

![해결된 문제](../assets/fix.svg) 이전에는 git이 &quot;허용됨 및 고객에게 알림&quot;으로 설정되어 있을 때 API를 사용하여 견적 항목을 저장하면 오류가 발생했습니다. 이제 이 API 호출이 예상대로 작동합니다.

![해결된 문제](../assets/fix.svg) 이제 고정 제품 세금이 견적 세부 정보 페이지에 표시됩니다.

![해결된 문제](../assets/fix.svg) 이전에는 내 견적 페이지의 설명 탭에서 첨부 파일을 클릭하면 파일을 다운로드할 수 없었습니다. 이제 이 동작이 예상대로 작동합니다.

### 알려진 문제

- Adobe Commerce은 다중 웹 사이트 배포에서 B2B 1.2.0으로 업그레이드하는 동안 예외를 throw합니다. 날짜 `setup:upgrade` 실행, 이 오류는 `PurchaseOrder` 모듈: `Module Magento_PurchaseOrder: Unable to apply data patch Magento\PurchaseOrder\Setup\Patch\Data\InitPurchaseOrderSalesSequence for moduleMagento_PurchaseOrder`. **해결 방법**: 설치 `B2B-716 Add NonTransactionableInterface` 인터페이스 `InitPurchaseOrderSalesSequence` 데이터 패치 핫픽스 - 이제 **내 계정** > **다운로드** 섹션 / `magento.com`.
- PO(구매 발주)가 승인되기 전에 할인 코드가 만료되면 PO는 할인된 금액을 계속 표시하지만 PO가 승인되면 주문이 할인되지 않은 합계에 배치됩니다. **해결 방법**: 설치 `B2B-709 Purchase Order Discount patch` 이 문제에 대한 핫픽스이며, 이제 다음에서 사용할 수 있습니다. **내 계정** > **다운로드** 섹션 / `magento.com`.
- 구매 발주의 품목이 품절되거나 구매 발주를 실제 주문으로 전환할 때 수량이 부족한 경우 오류가 발생합니다. 미납주문이 사용으로 설정된 경우 주문이 정상적으로 처리됩니다.
