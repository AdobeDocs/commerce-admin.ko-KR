---
title: AI 제품 검색 릴리스 노트
description: 카탈로그 및 PDP 강화 기능, 수정 사항, 업그레이드 지침, 지원되는 Commerce 버전 및 알려진 문제에 대한 AI 제품 검색 릴리스 정보를 검토하십시오.
feature: Release Notes
source-git-commit: ed404fb8515374a33116ccc811c96548fb14dd35
workflow-type: tm+mt
source-wordcount: '734'
ht-degree: 0%
---
# AI 제품 검색 릴리스 정보

이 릴리스 노트에서는 새로운 기능, 수정 사항, 업그레이드 요구 사항 및 알려진 문제를 포함하여 카탈로그 보강 및 PDP 보강에 대한 업데이트를 다룹니다. 각 버전 항목은 영향을 받는 확장 또는 워크플로우를 식별합니다.

새 기능 ![개](../assets/new.svg)개
![해결된 문제](../assets/fix.svg) 수정 사항 및 개선 사항
![알려진 문제](../assets/bug.svg)알려진 문제

## 릴리스 2.1.3 {#release-2-1-3}

*2026년 11월 30일*

[!BADGE 지원됨]{type=Informative tooltip="지원됨"} [!DNL Adobe Commerce] 2.4.9, 2.4.8, 2.4.7(PHP 8.3 ~ 8.5). [!DNL Adobe Commerce as a Cloud Service]

버전 2.1.3은 제품 세부 정보 페이지 풍부화와 카탈로그 풍부화를 **AI 제품 검색**&#x200B;이라는 새 관리 메뉴 항목에 결합합니다. 또한 지원이 [!DNL Adobe Commerce as a Cloud Service]까지 확장되었습니다.

## 릴리스 2.1.2 {#release-2-1-2}

*2026년 10월 22일*

[!BADGE 지원됨]{type=Informative tooltip="지원됨"} [!DNL Adobe Commerce] 2.4.9, 2.4.8 및 2.4.7(PHP 8.3 ~ 8.5).

버전 2.1.2는 카탈로그 보강이 자체 포함된 확장을 만듭니다. 이제 별도의 [!DNL Adobe Brand Visibility] 확장(`magento/llm-optimizer`)에서 이전에 제공한 모든 내용이 포함됩니다. 승인된 제안을 카탈로그에 적용하고, 롤백하고, 자신의 편집 내용을 덮어쓰지 않도록 보호합니다.

### 이전 버전에서 업그레이드 {#upgrade-from-earlier-versions}

>[!IMPORTANT]
>
>버전 2.1.2는 [!DNL Adobe Brand Visibility] 확장과 함께 설치할 수 없습니다. 설치된 경우 업그레이드의 일부로 제거합니다.

1. 설치된 경우 [!DNL Adobe Brand Visibility] 확장을 제거합니다.

   ```bash
   composer remove magento/llm-optimizer
   ```

   `Magento/LlmoCatalog`을(를) `app/code`(으)로 복사하거나 심볼릭 링크하여 확장을 설치한 경우 해당 디렉터리를 삭제하십시오. 모듈을 사용하지 않도록 설정하기만 하면 안 됩니다. 디스크에 남아 있는 사용하지 않는 모듈로 인해 `setup:upgrade`에서 보강된 제품의 원래 값을 저장하는 테이블을 삭제할 수 있습니다.

1. 카탈로그 보강 업데이트 및 변경 사항 적용:

   ```bash
   composer require magento/module-catalog-enrichment:^2.1
   bin/magento setup:upgrade
   bin/magento cache:flush
   ```

   업그레이드 후 캐시를 플러시합니다. 업그레이드는 기존 액세스 권한을 새 권한 리소스로 이동하며 캐시를 지울 때까지 해당 권한이 적용되지 않습니다.

### 요구 사항

![새로 만들기](../assets/new.svg) **PHP 8.3 및 [!DNL Adobe Commerce] 2.4.7 이상**—PHP 8.1은 수명이 종료되고 PHP 8.2는 2026년 12월 31일에 수명이 종료되므로 지원되지 않습니다. [!DNL Adobe Commerce] 2.4.6 및 이전 버전은 지원되지 않습니다.

### 새로운 기능

![새로 만들기](../assets/new.svg) **[!UICONTROL AI Product Discovery]메뉴**—이제 카탈로그 보강 페이지의 관리 사이드바에 고유한 섹션이 있습니다. **[!UICONTROL AI Product Discovery]** > **[!UICONTROL Catalog Enrichment]**(으)로 이동합니다. 이전에는 페이지가 **[!UICONTROL Catalog]** 아래에 있었습니다.

![새로 만들기](../assets/new.svg) [!BADGE Beta]{type=Informative tooltip="아직 일반적으로 사용할 수 없음"} **[!UICONTROL Product Details Page Enrichment (Beta)]**—제품 세부 정보 페이지에 대한 데이터 보강 제안을 검토하기 위한 **[!UICONTROL AI Product Discovery]**&#x200B;의 새 페이지입니다. 제품 세부 사항 페이지 보강은 베타 버전이며 아직 사용 단계는 아닙니다.

![새로 만들기](../assets/new.svg) **승인된 제안을 적용하고 롤백합니다**—승인된 이름 및 설명 업데이트가 이 확장에 의해 카탈로그에 기록됩니다. Commerce은 처음 변경될 때 보강된 각 속성의 원래 값을 기록하므로, 동일한 속성에 여러 제안이 적용된 후에도 롤백은 항상 보강 전에 있었던 값을 복원합니다.

![새로 만들기](../assets/new.svg) **편집 내용이 준수되었습니다**—관리 제품 양식에서 **[!UICONTROL Update Attributes]**(으)로 보강된 이름 또는 설명을 변경하거나 가져오기를 통해 변경 내용을 적용하면 값이 유지되고 관련 제안 사항은 *오래됨*(으)로 표시됩니다. 기본 범위에서 변경한 내용은 값을 상속하는 저장소 보기에만 영향을 줍니다.

![새로 만들기](../assets/new.svg) **제안에 대한 읽기 전용 카탈로그 액세스**—[!DNL Commerce Catalog Agent]은(는) 제품, 범주, 특성 집합 및 제품 유형 데이터를 읽고 분석할 제품을 선택할 수 있습니다. 읽기는 **[!UICONTROL Used in Product Listing]**(으)로 표시된 특성과 보강할 수 있는 특성만 반환합니다. 카탈로그 데이터를 변경할 수 없습니다.

### 수정 사항 및 향상된 기능

![해결된 문제](../assets/fix.svg) **다시 시도된 적용 보고서 성공**—이미 완료된 후 적용 요청이 다시 시도되는 경우 다시 시도는 변경 사항을 보고하지 않고 적용된 변경 사항을 보고합니다. 아무것도 두 번 쓰여지지 않았습니다.

![문제를 해결했습니다](../assets/fix.svg) **승인된 서비스만 카탈로그를 변경할 수 있습니다**—적용 및 롤백은 [!DNL Commerce Catalog Agent]의 요청만 수락합니다. 이전에는 유효한 Adobe IMS 토큰이 모두 수락되었습니다. 이제 SOAP 요청에도 동일한 검사가 적용됩니다.

![문제 해결](../assets/fix.svg) **오류 지우기**—Adobe IMS 중단은 이제 `500` 대신 `401`을(를) 반환하므로 카탈로그에 대해 요청이 다시 시도되지 않으며 인식할 수 없는 Adobe IMS 환경은 스테이징으로 처리되지 않고 거부됩니다.

![문제 해결](../assets/fix.svg) **Adobe IMS 환경**—비프로덕션 [!DNL Commerce Services] 데이터 공간에 연결된 인스턴스를 포함하여 기본적으로 카탈로그 보강이 프로덕션 Adobe IMS 환경에 로그인됩니다. 이전에는 이러한 인스턴스가 스테이징 환경으로 전송되었습니다.

![문제 해결](../assets/fix.svg) **도메인 변경 후 로그인**—카탈로그 보강 페이지가 이제 `abv.adobe.com`에서 로드되어 이전 도메인이 리디렉션을 시작한 후 로그인 루프가 수정됩니다.[!DNL Adobe Brand Visibility]

### 알려진 문제

![알려진 문제](../assets/bug.svg) **전체 [!UICONTROL Catalog] 액세스 권한이 있는 역할**—이 릴리스 전에 저장된 모든 **[!UICONTROL Catalog]**&#x200B;이(가) 부여된 사용자 역할이 **[!UICONTROL Catalog Enrichment Service API]** 리소스에 대한 액세스 권한을 유지합니다. **[!UICONTROL System]** > **[!UICONTROL Permissions]** > **[!UICONTROL User Roles]**&#x200B;에서 이러한 역할을 검토하고 필요하지 않은 리소스의 선택을 취소하십시오.

## 릴리스 1.0.2 {#release-1-0-2}

카탈로그 보강 관리 페이지의 초기 릴리스. 카탈로그에 제안을 적용하려면 [!DNL Adobe Brand Visibility] 확장이 필요합니다.
