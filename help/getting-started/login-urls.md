---
title: 로그인 자격 증명 및 URL
description: 관리자 및 상점 첫 화면에 대한 액세스 권한을 얻는 데 사용되는 Commerce URL 및 계정 자격 증명에 대해 알아봅니다.
exl-id: fa16b7e9-e05f-4eb8-bc32-596946c57e1c
feature: System
role: Admin, Leader
source-git-commit: 77e7eb00e9f8d5af6361059c287707993180c4c4
workflow-type: tm+mt
source-wordcount: '351'
ht-degree: 0%

---

# 로그인 자격 증명 및 URL

설정 및 구성을 계속하기 전에 스토어 관리자 및 Commerce 계정에 액세스하는 데 필요한 정보가 있는지 확인하십시오.

## Storefront URL

[storefront](storefront.md)의 주소는 일반적으로 IP 주소에 할당된 도메인입니다. 일부 저장소는 루트 또는 최상위 디렉토리에 설치됩니다. 다른 기능은 루트 아래의 디렉토리에 설치됩니다. 저장소는 주 도메인과 연관된 하위 도메인 내에 상주할 수 있습니다. 스토어 URL은 다음 중 하나와 비슷할 수 있습니다.

- `http://mydomain.com`
- `http://www.mydomain.com/mystore`
- `http://xxx.xxx.xxx.xxx`초

도메인이 아직 없는 경우 스토어 URL에는 각각 _점선 4진법_ 표기법으로 마침표로 구분된 일련의 4개의 숫자가 포함됩니다.

## 관리자 URL

설치하는 동안 저장소 [관리자](admin.md) 주소를 설정했습니다. 기본 주소는 스토어와 동일하지만 끝에 `/admin`이(가) 있습니다. 이 안내서의 예제에서 기본 디렉터리를 사용하지만 저장소에 고유한 위치에서 관리자를 실행하는 것이 가장 좋습니다.

- `http://mydomain.com/admin`
- `http://www.mydomain.com/admin`

## [!DNL Commerce] 계정

[Commerce 계정](commerce-account-create.md)에서 제품 및 서비스, 계정 설정, 청구 기록 및 지원 리소스에 대한 정보에 액세스할 수 있습니다. 계정에 액세스하려면 기본 Commerce 사이트로 이동하여 오른쪽 상단의 **[!UICONTROL My Account]**&#x200B;을(를) 클릭합니다.

## 고객 계정

스토어를 학습하는 동안 테스트 [고객 계정](../customers/account-dashboard.md)을(를) 설정해야 고객의 관점에서 스토어 및 체크아웃 프로세스를 경험할 수 있습니다.

## 샘플 데이터

[!BADGE PaaS만]{type=Informative url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="Adobe Commerce 온 클라우드 프로젝트(Adobe 관리 PaaS 인프라) 및 온프레미스 프로젝트에만 적용됩니다."}

Adobe은 250개 이상의 제품(약 200개는 구성 가능한 제품)이 있는 샘플 저장소, 카테고리, 프로모션 가격 규칙, CMS 페이지, 배너 등을 포함하는 샘플 데이터 세트를 제공합니다. 샘플 데이터는 상점 첫 화면에서 _Luma_ 테마를 사용합니다. [이 샘플 데이터 설치](https://experienceleague.adobe.com/docs/commerce-operations/installation-guide/next-steps/sample-data/overview.html)는 선택 사항이지만, 전자 상거래 비즈니스의 사용자 지정을 테스트하고 개발하는 데 도움이 될 수 있습니다.
