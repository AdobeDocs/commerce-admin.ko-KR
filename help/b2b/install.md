---
title: ' [!DNL Adobe Commerce B2B] 확장 설치'
description: ' [!DNL Adobe Commerce B2B] 메타패키지를 설치하는 방법을 알아봅니다.'
feature: B2B, Install
role: Admin, Developer
exl-id: a6947212-1708-40ae-9e81-874467eba5e1
badgePaas: label="PaaS만" type="Informative" url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="Adobe Commerce 온 클라우드 프로젝트(Adobe 관리 PaaS 인프라) 및 온프레미스 프로젝트에만 적용됩니다."
source-git-commit: 25964363ca5c4ec849e231d4eccb5f60b682a499
workflow-type: tm+mt
source-wordcount: '1149'
ht-degree: 0%

---


# [!DNL Adobe Commerce B2B] 확장 설치

Adobe Commerce B2B 확장 `magento/extension-b2b`은(는) 지원되는 모든 Adobe Commerce 버전에 사용할 수 있습니다. Adobe Commerce 설치 후 설치됩니다.


## 요구 사항

- [Adobe Commerce](https://business.adobe.com/products/magento/magento-commerce.html), 지원되는 모든 버전
- PHP 8.1, 8.2 및 8.3(B2B 1.5.0 필요)
- [!DNL Composer]

>[!IMPORTANT]
>
>Adobe Commerce B2B 버전 1.4.2+는 PHP 8.3과 호환되지 않습니다. Commerce 인스턴스를 Commerce 버전 2.4.7+로 업그레이드하는 경우 인스턴스에 설치된 PHP 버전이 PHP 8.2인지 확인하여 B2B 1.4.2+와의 호환성을 유지합니다.

## 지원되는 플랫폼

- ECE(클라우드 인프라)의 Adobe Commerce
- Adobe Commerce 온-프레미스 (EE)

## 설치 단계

>[!BEGINSHADEBOX]

**필수 구성 요소**

- 확장을 다운로드하려면 [repo.magento.com](https://repo.magento.com/)에 액세스하십시오. 키를 생성하고 필요한 권한을 얻으려면 [인증 키 가져오기](https://experienceleague.adobe.com/en/docs/commerce-operations/installation-guide/prerequisites/authentication-keys)를 참조하십시오.

  [COMPOSER_HOME](https://getcomposer.org/doc/03-cli.md#composer-home) 디렉터리에 전역적으로 정의하여 설치할 인증 키를 저장합니다. 또는 Adobe Commerce 애플리케이션 루트 디렉터리의 [auth.json](https://developer.adobe.com/commerce/contributor/guides/install/clone-repository/#authentication-file) 파일에 저장하십시오.

- [B2B 확장의 지원되는 버전](https://experienceleague.adobe.com/en/docs/commerce-operations/release/product-availability)-배포된 Adobe Commerce 버전에서 지원되는 B2B 확장의 최신 버전을 확인합니다.

- 릴리스 정보에서 버전 호환성, 업데이트 또는 설치 또는 업그레이드 요구 사항에 영향을 줄 수 있는 변경 사항에 대한 최신 정보를 확인하십시오.

   - [B2B 릴리스 노트](release-notes.md)
   - [Adobe Commerce 릴리스 노트](https://experienceleague.adobe.com/en/docs/commerce-operations/release/versions)

>[!ENDSHADEBOX]

Composer를 사용하여 B2B 확장(`magento/b2b-extension`)을 설치합니다. 확장은 Adobe Commerce 인스턴스에 대한 B2B 기능을 활성화하는 모듈 컬렉션을 포함하는 작성기 메타패키지입니다. 포함된 모듈 목록은 [B2B 패키지](packages.md)를 참조하십시오.

>[!BEGINTABS]

>[!TAB 클라우드 인프라]

>[!TIP]
>
>클라우드 인프라에 Adobe Commerce Adobe B2B를 설치하는 경우 시작하기 전에 통합 또는 스테이징 환경에 Adobe Commerce 애플리케이션을 배포하는 것이 좋습니다.

Adobe은 프로젝트에 B2B 확장을 추가할 때 개발 분기에서 작업하는 것을 권장합니다. 분기가 없는 경우 [개발용 분기 만들기](https://experienceleague.adobe.com/en/docs/commerce-cloud-service/user-guide/develop/cli-branches)를 참조하세요. B2B 확장을 설치할 때 `Magento_B2b` 확장 이름이 `app/etc/config.php` 파일에 자동으로 삽입됩니다. 파일을 직접 편집할 필요는 없습니다.

**B2B 확장을 설치하려면**:

1. 로컬 워크스테이션에서 프로젝트 디렉터리로 변경합니다.

1. 개발 분기를 만들거나 체크 아웃합니다.

1. B2B 확장을 `composer.json` 파일의 `require` 섹션에 추가합니다.

   ```bash
   composer require magento/extension-b2b --no-update
   ```

1. 프로젝트 종속성을 업데이트합니다.

   ```bash
   composer update
   ```

1. 코드 변경 사항을 추가, 커밋 및 푸시합니다.

   ```bash
   git add -A
   ```

   ```bash
   git commit -m "Install the B2B extension."
   ```

   ```bash
   git push origin <branch-name>
   ```

   >[!NOTE]
   >
   >업데이트를 클라우드 환경으로 푸시하면 Commerce 클라우드 배포 프로세스가 시작되어 변경 사항이 적용됩니다. [배포 로그](https://experienceleague.adobe.com/en/docs/commerce-cloud-service/user-guide/develop/deploy/process)에서 배포 상태를 확인하십시오. 배포 오류가 발생하면 [구성 요소 오류에서 복구](https://experienceleague.adobe.com/en/docs/commerce-cloud-service/user-guide/develop/deploy/recover-failed-deployment)를 참조하십시오.

1. 빌드 및 배포가 완료되면 SSH를 사용하여 원격 환경에 로그인하고 B2B 확장이 설치 및 활성화되었는지 확인합니다.

   ```bash
   bin/magento module:status Magento_B2b
   ```

   확장 이름은 `<VendorName>_<ComponentName>` 형식을 사용합니다.

   샘플 응답:

   ```
   Magento_B2b : Module is enabled
   ```

>[!TAB 온-프레미스]

1. Adobe Commerce 응용 프로그램 루트 디렉터리에서 `composer.json`을(를) 업데이트하여 B2B 확장에 대한 종속성을 추가합니다.

   ```bash
   composer require magento/extension-b2b:<version>
   ```

   오류가 발생하는 경우, 예를 들면 다음과 같습니다.

   ```
   [InvalidArgumentException] Could not find a matching version of package magento/extension-b2b.
   ```

   패키지 철자, 버전 제약 조건 및 패키지를 사용할 수 있고 최소 안정성(안정적인) 요구 사항과 일치하는지 확인합니다.

1. 메시지가 표시되면 [인증 키](https://experienceleague.adobe.com/en/docs/commerce-operations/installation-guide/prerequisites/authentication-keys)를 입력하십시오.

   _공개 키_&#x200B;은(는) 사용자 이름이고 _개인 키_&#x200B;은(는) 암호입니다. 공개 및 개인 키를 `auth.json`에 저장한 경우 인증하라는 메시지가 표시되지 않습니다.

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
   >프로덕션 모드에서 `Please rerun Magento compile command`에게 메시지를 받을 수 있습니다. 설치 완료 명령을 입력합니다. Adobe Commerce은 개발자 모드에서 compile 명령을 실행하라는 메시지를 표시하지 않습니다.

>[!ENDTABS]

설치를 완료한 후 메시지 소비자를 구성하고 시작합니다.

## 메시지 소비자

Adobe Commerce B2B 확장은 메시지 대기열 관리에 MySQL을 사용합니다. 다음 표에는 B2B 기능을 지원하는 메시지 소비자가 나와 있습니다. 확장을 설치한 후 Commerce 스토어에 필요한 B2B 기능에 대한 메시지 소비자를 시작합니다.

| 소비자 | 설명 |
|------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `sharedCatalogUpdatePrice` | 공유 카탈로그의 각 제품에 대한 가격을 업데이트합니다. 관리 시스템 구성 설정에서 [**[!UICONTROL Shared Catalogs]**](catalog-shared.md) 옵션을 사용하도록 설정한 경우 필수입니다. |
| `sharedCatalogUpdateCategoryPermissions` | 공유 카탈로그 범주에 할당된 범주를 업데이트합니다. 관리 시스템 구성 설정에서 [**[!UICONTROL Shared Catalogs]**](catalog-shared.md) 옵션을 사용하도록 설정한 경우 필수입니다. |
| `negotiableQuotePriceUpdate` | 협상 가능한 견적의 가격을 업데이트합니다. 관리 시스템 구성 설정에서 [**[!UICONTROL Quotes]**](quotes.md) 옵션을 사용하도록 설정한 경우 필수입니다. |
| `purchaseorder.toorder` | 구매 발주를 주문으로 변환합니다. 관리 시스템 구성 설정에서 [**[!UICONTROL Purchase Orders]**](purchase-order-flow.md) 옵션을 사용하도록 설정한 경우 필수입니다. |
| `purchaseorder.transactional.email` | 구매 주문 이메일을 보냅니다. 관리 시스템 구성 설정에서 [**[!UICONTROL Purchase Orders]**](purchase-order-flow.md) 옵션을 사용하도록 설정한 경우 필수입니다. |
| `purchaseorder.validation` | 관련 [승인 규칙](account-dashboard-approval-rules.md)에 대해 구매 주문을 확인합니다. 관리 시스템 구성 설정에서 [**[!UICONTROL Purchase Orders]**](purchase-order-flow.md) 옵션을 사용하도록 설정한 경우 필수입니다. |
| `quoteItemCleaner` | 제품이 카탈로그에서 삭제되거나 장바구니에서 제거될 때 유효하지 않거나 비활성 가격 견적을 삭제합니다. 관리 시스템 구성 설정에서 [**[!UICONTROL Quotes]**](quotes.md) 옵션을 사용하도록 설정한 경우 필수입니다. |
| `inventoryQtyCounter` | 주문이 배치되거나 제품이 제거된 후 비동기적으로 주가 지수를 수정합니다. 관리자 구성 설정에서 Inventory management에 대해 [**[!UICONTROL Use deferred stock update]**](../configuration-reference/catalog/inventory.md#product-stock-options) 옵션을 사용하도록 설정한 경우 필수입니다. [성능 모범 사례](https://experienceleague.adobe.com/en/docs/commerce-operations/performance-best-practices/configuration#deferred-stock-update)를 참조하세요. |
| `async.operations.all` | 항목 가져오기 또는 내보내기, 대량 규모에 따른 가격 변경, 웨어하우스에 제품 할당 등 [일괄 작업](https://developer.adobe.com/commerce/php/development/components/message-queues/bulk-operations/)의 각 개별 작업에 대한 메시지를 만듭니다. 관리 시스템 구성 설정에서 [!DNL Inventory Management]에 대한 [**관리 대량 작업**](../configuration-reference/catalog/inventory.md#admin-bulk-operations) 옵션이 **비동기적으로 실행**(으)로 설정된 경우 필요합니다. |

{style="table-layout:auto"}

>[!NOTE]
>
>모든 Adobe Commerce 메시지 소비자 목록을 보려면 _구성 안내서_&#x200B;의 [메시지 큐 소비자](https://experienceleague.adobe.com/en/docs/commerce-operations/configuration-guide/message-queues/consumers)를 참조하십시오.

### 메시지 소비자 구성

B2B 기능에 대해 [메시지 소비자를 시작](#start-message-consumers)할 때 다음 매개 변수를 추가하여 가능한 처리 문제 또는 지연을 방지합니다.

- `--max-messages <value>`— 종료하기 전에 각 소비자가 처리해야 하는 최대 메시지 수를 지정합니다(기본값 = 10000). Adobe에서는 권장하지 않지만 0을 사용하여 소비자가 종료하지 않도록 할 수 있습니다. PHP 응용 프로그램의 가장 좋은 방법은 가능한 메모리 누수를 방지하기 위해 오래 실행되는 프로세스를 다시 시작하는 것입니다.

- `--batch-size <value>`— 소비자가 사용하는 시스템 리소스(CPU, 메모리)를 제한할 수 있습니다. 더 작은 배치를 사용하면 리소스 사용량이 감소하므로 처리 속도가 느려집니다.  지정하면 큐의 메시지가 각각 `<value>`개씩 일괄적으로 사용됩니다. 이 옵션은 일괄 처리 소비자에만 적용할 수 있습니다. `--batch-size`이(가) 정의되지 않은 경우 일괄 처리 소비자는 큐에서 사용 가능한 모든 메시지를 수신합니다.

추가 구성 옵션에 대한 자세한 내용은 [특정 구성](https://experienceleague.adobe.com//en/docs/commerce-operations/configuration-guide/message-queues/manage-message-queues#specific-configuration)을 참조하십시오.

### 메시지 소비자 시작

B2B 기능에 대한 비동기 작업을 활성화하려면 여러 메시지 소비자를 시작해야 합니다.

1. 사용 가능한 메시지 소비자를 나열합니다.

   ```bash
   bin/magento queue:consumers:list
   ```

   이 명령은 모든 [B2B 메시지 소비자](#message-consumers)를 포함하는 사용 가능한 메시지 소비자를 반환합니다.

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
>백그라운드에서 실행하려면 `&`을(를) 명령에 추가하고 프롬프트로 돌아가서 명령을 계속 실행합니다. 예: `bin/magento queue:consumers:start sharedCatalogUpdatePrice &`.

자세한 내용은 _구성 가이드_&#x200B;의 [메시지 큐 관리](https://experienceleague.adobe.com/en/docs/commerce-operations/configuration-guide/message-queues/manage-message-queues)를 참조하세요.

### cron에 메시지 소비자 추가

cron 구성 파일 [/app/code/Magento/MessageQueue/etc/crontab.xml](https://experienceleague.adobe.com/en/docs/commerce-operations/configuration-guide/message-queues/manage-message-queues#process-management)에 일정을 추가하여 `SharedCatalogUpdateCategoryPermissions` 및 `SharedCatalogUpdatePrice` 메시지 소비자에 대한 실행 일정을 자동화할 수 있습니다.

```
* * * * * ps ax | grep [s]haredCatalogUpdateCategoryPermissions >>/dev/null 2>&1 || nohup php /var/www/html/magento2/bin/magento queue:consumers:start sharedCatalogUpdateCategoryPermissions &
* * * * * ps ax | grep [s]haredCatalogUpdatePrice >>/dev/null 2>&1 || nohup php /var/www/html/magento2/bin/magento queue:consumers:start sharedCatalogUpdatePrice &
```

관리자의 [구성 설정 저장](../systems/cron.md)에서 메시지 소비자에 대한 일정을 구성할 수도 있습니다.

## 관리자에서 B2B 기능 활성화

Adobe Commerce B2B 확장을 설치하고 메시지 소비자를 시작한 후에는 [관리에서 B2B 기능을 활성화](enable-basic-features.md)해야 합니다.

