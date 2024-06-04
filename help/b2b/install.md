---
title: 설치 [!DNL Adobe Commerce B2B] 확장
description: 설치 방법 알아보기 [!DNL Adobe Commerce B2B] 메타패키지.
feature: B2B, Install
role: Admin, Developer
exl-id: a6947212-1708-40ae-9e81-874467eba5e1
source-git-commit: 61df9a4bcfaf09491ae2d353478ceb281082fa74
workflow-type: tm+mt
source-wordcount: '873'
ht-degree: 0%

---


# 설치 [!DNL Adobe Commerce B2B] 확장

Adobe Commerce B2B 확장 기능은 Adobe Commerce v2.2.0 이상에서만 사용할 수 있습니다. Adobe Commerce 설치 후 설치됩니다.

배포된 Adobe Commerce 버전에서 지원되는 최신 버전의 B2B 확장을 설치합니다.

>[!NOTE]
>
>이러한 설치 지침은 온프레미스에 배포된 Adobe Commerce에 적용됩니다. 클라우드 인프라에 배포된 Commerce 프로젝트용 B2B 확장을 설치하려면 다음을 참조하십시오. [Commerce Cloud 인프라 안내서](https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/configure-store/b2b-module.html).

## 요구 사항

- Adobe Commerce 버전 2.3.x 이상
- [지원되는 B2B 확장 버전](https://experienceleague.adobe.com/docs/commerce-operations/release/product-availability.html#compatibility)
- 유효 [인증 키](https://experienceleague.adobe.com/docs/commerce-operations/installation-guide/prerequisites/authentication-keys.html) Adobe Commerce 확장을 다운로드하려면 다음을 수행하십시오.

  에서 전역적으로 정의하여 설치에 대한 인증 키를 저장합니다. [COMPOSER_홈](https://getcomposer.org/doc/03-cli.md#composer-home) 디렉토리. 또는 다음 위치에 저장하십시오. [auth.json](https://developer.adobe.com/commerce/contributor/guides/install/clone-repository/#authentication-file) Adobe Commerce 애플리케이션 루트 디렉토리에 있는 파일입니다.

B2B 확장을 설치하거나 업그레이드하기 전에 릴리스 정보에서 버전 호환성, 업데이트 또는 설치 또는 업그레이드 요구 사항에 영향을 줄 수 있는 변경 사항에 대한 최신 정보를 확인하십시오.

- [B2B 릴리스 노트](release-notes.md)
- [Adobe Commerce 릴리스 노트](https://experienceleague.adobe.com/docs/commerce-operations/release/versions.html?lang=en)

## 설치 단계

1. Adobe Commerce 애플리케이션 루트 디렉토리에서 `composer.json` B2B 확장에 대한 종속성을 추가하려면 다음을 수행합니다.

   ```bash
   composer require magento/extension-b2b:<version>
   ```

   오류가 발생하는 경우, 예를 들면 다음과 같습니다.

   ```terminal
   [InvalidArgumentException] Could not find a matching version of package magento/extension-b2b.
   ```

   패키지 철자, 버전 제약 조건 및 패키지를 사용할 수 있고 최소 안정성(안정적인) 요구 사항과 일치하는지 확인합니다.

1. 메시지가 표시되면 [인증 키](https://experienceleague.adobe.com/docs/commerce-operations/installation-guide/prerequisites/authentication-keys.html).

   사용자 _공개 키_ 은 사용자 이름입니다. 는 _개인 키_ 는 암호입니다. 공개 및 개인 키를 `auth.json`인증하라는 메시지가 표시되지 않습니다.

1. Composer에서 모듈 업데이트를 완료한 후 다음 명령을 실행합니다.

   ```bash
   bin/magento setup:upgrade
   ```

   ```bash
   bin/magento setup:di:compile
   ```

   ```bash
   bin/magento setup:static-content:deploy -f
   ```

   ```bash
   bin/magento cache:clean
   ```

   >[!NOTE]
   >
   >프로덕션 모드에서는 다음 대상에게 메시지를 수신할 수 있습니다. `Please rerun Magento compile command`. 설치 완료 명령을 입력합니다. Adobe Commerce은 개발자 모드에서 compile 명령을 실행하라는 메시지를 표시하지 않습니다.

설치를 완료한 후 다음을 포함한 메시지 소비자를 구성하고 시작합니다. [메시지 소비자에 대한 매개 변수 지정](#configure-message-consumers).

## 메시지 소비자

Adobe Commerce B2B 확장은 메시지 대기열 관리에 MySQL을 사용합니다. 다음 표에는 B2B 기능을 지원하는 메시지 소비자가 나와 있습니다. 확장을 설치한 후 Commerce 스토어에 필요한 B2B 기능에 대한 메시지 소비자를 시작합니다.

| 소비자 | 설명 |
|------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `sharedCatalogUpdatePrice` | 공유 카탈로그의 각 제품에 대한 가격을 업데이트합니다. 필요한 경우: [**[!UICONTROL Shared Catalogs]**](catalog-shared.md) 옵션은 관리 시스템 구성 설정에서 활성화됩니다. |
| `sharedCatalogUpdateCategoryPermissions` | 공유 카탈로그 범주에 할당된 범주를 업데이트합니다. 필요한 경우: [**[!UICONTROL Shared Catalogs]**](catalog-shared.md) 옵션은 관리 시스템 구성 설정에서 활성화됩니다. |
| `negotiableQuotePriceUpdate` | 협상 가능한 견적의 가격을 업데이트합니다. 필요한 경우: [**[!UICONTROL Quotes]**](quotes.md) 옵션은 관리 시스템 구성 설정에서 활성화됩니다. |
| `purchaseorder.toorder` | 구매 발주를 주문으로 변환합니다. 필요한 경우: [**[!UICONTROL Purchase Orders]**](purchase-order-flow.md) 옵션은 관리 시스템 구성 설정에서 활성화됩니다. |
| `purchaseorder.transactional.email` | 구매 주문 이메일을 보냅니다. 필요한 경우: [**[!UICONTROL Purchase Orders]**](purchase-order-flow.md) 옵션은 관리 시스템 구성 설정에서 활성화됩니다. |
| `purchaseorder.validation` | 관련성이 있는 구매 발주를 검증합니다. [승인 규칙](account-dashboard-approval-rules.md). 필요한 경우: [**[!UICONTROL Purchase Orders]**](purchase-order-flow.md) 옵션은 관리 시스템 구성 설정에서 활성화됩니다. |
| `quoteItemCleaner` | 제품이 카탈로그에서 삭제되거나 장바구니에서 제거될 때 유효하지 않거나 비활성 가격 견적을 삭제합니다. 필요한 경우: [**[!UICONTROL Quotes]**](quotes.md) 옵션은 관리 시스템 구성 설정에서 활성화됩니다. |
| `inventoryQtyCounter` | 주문이 배치되거나 제품이 제거된 후 비동기적으로 주가 지수를 수정합니다. 필요한 경우: [**[!UICONTROL Use deferred stock update]**](../configuration-reference/catalog/inventory.md#product-stock-options) 옵션은 관리자 구성 설정에서 Inventory management에 대해 활성화되어 있습니다. 다음을 참조하십시오 [성능 모범 사례](https://experienceleague.adobe.com/docs/commerce-operations/performance-best-practices/configuration.html#deferred-stock-update). |
| `async.operations.all` | 의 각 개별 작업에 대한 메시지 만들기 [대량 작업](https://developer.adobe.com/commerce/php/development/components/message-queues/bulk-operations/)예를 들어, 항목을 가져오거나 내보내고, 가격을 대량으로 변경하고, 제품을 창고에 지정하는 등의 작업을 수행할 수 있습니다. 필요한 경우: [**관리 일괄 작업**](../configuration-reference/catalog/inventory.md#admin-bulk-operations) 옵션 [!DNL Inventory Management] 이(가) (으)로 설정됨 **비동기적으로 실행** 관리자 시스템 구성 설정에서 을 참조하십시오. |

{style="table-layout:auto"}

>[!NOTE]
>
>모든 Adobe Commerce 메시지 소비자 목록은 을 참조하십시오. [메시지 대기열 소비자](https://experienceleague.adobe.com/docs/commerce-operations/configuration-guide/message-queues/consumers.html) 다음에서 _구성 안내서_.

### 메시지 소비자 구성

다음을 수행할 때 다음 매개 변수를 추가하여 가능한 처리 문제 또는 지연을 방지하십시오. [메시지 소비자 시작](#start-message-consumers) B2B 기능용

- `--max-messages <value>`— 종료하기 전에 각 소비자가 처리해야 하는 최대 메시지 수를 지정합니다(기본값 = 10000). 권장하지는 않지만 0을 사용하여 소비자가 종료하지 않도록 할 수 있습니다. PHP 응용 프로그램의 가장 좋은 방법은 가능한 메모리 누수를 방지하기 위해 오래 실행되는 프로세스를 다시 시작하는 것입니다.

- `--batch-size <value>`— 고객이 사용하는 시스템 리소스(CPU, 메모리)를 제한할 수 있습니다. 더 작은 배치를 사용하면 리소스 사용량이 감소하므로 처리 속도가 느려집니다.  지정하면 대기열의 메시지가 다음의 배치로 사용됩니다. `<value>` 각. 이 옵션은 일괄 처리 소비자에만 적용할 수 있습니다. If `--batch-size` 가 정의되지 않은 경우 일괄 처리 소비자가 대기열에서 사용 가능한 모든 메시지를 수신합니다.

추가 구성 옵션에 대한 자세한 내용은 [특정 구성](https://experienceleague.adobe.com/docs/commerce-operations/configuration-guide/message-queues/manage-message-queues.html#specific-configuration).

### 메시지 소비자 시작

B2B 기능에 대한 비동기 작업을 활성화하려면 여러 메시지 소비자를 시작해야 합니다.

1. 사용 가능한 메시지 소비자를 나열합니다.

   ```bash
   bin/magento queue:consumers:list
   ```

   이 명령은 다음을 포함한 사용 가능한 메시지 소비자를 반환합니다. [B2B 메시지 소비자](#message-consumers).

1. 각 소비자를 개별적으로 시작:

   ```bash
   bin/magento queue:consumers:start [--max-messages=<value>] [--batch-size=<value>] <consumer_name>
   ```

   For example:

   ```bash
   bin/magento queue:consumers:start quoteItemCleaner
   ```

>[!TIP]
>
>백그라운드에서 실행하려면 다음을 추가합니다 `&` 명령을 실행한 다음 프롬프트로 돌아가서 명령을 계속 실행합니다. 예: `bin/magento queue:consumers:start sharedCatalogUpdatePrice &`.

자세한 내용은 [메시지 대기열 관리](https://experienceleague.adobe.com/docs/commerce-operations/configuration-guide/message-queues/manage-message-queues.html) 다음에서 _구성 안내서_.

### cron에 메시지 소비자 추가

에 대한 실행 일정을 자동화하는 옵션이 있습니다. `SharedCatalogUpdateCategoryPermissions` 및 `SharedCatalogUpdatePrice` cron 구성 파일에 일정을 추가하여 메시지 소비자 [/app/code/Magento/MessageQueue/etc/crontab.xml](https://experienceleague.adobe.com/docs/commerce-operations/configuration-guide/message-queues/manage-message-queues.html#process-management).

```terminal
* * * * * ps ax | grep [s]haredCatalogUpdateCategoryPermissions >>/dev/null 2>&1 || nohup php /var/www/html/magento2/bin/magento queue:consumers:start sharedCatalogUpdateCategoryPermissions &
* * * * * ps ax | grep [s]haredCatalogUpdatePrice >>/dev/null 2>&1 || nohup php /var/www/html/magento2/bin/magento queue:consumers:start sharedCatalogUpdatePrice &
```

에서 메시지 소비자에 대한 일정을 구성할 수도 있습니다. [구성 설정 저장](../systems/cron.md) 관리에서.

## 관리자에서 B2B 기능 활성화

Adobe Commerce B2B 확장을 설치하고 메시지 소비자를 시작한 후 다음을 수행해야 합니다 [관리자에서 B2B 기능 활성화](enable-basic-features.md).
