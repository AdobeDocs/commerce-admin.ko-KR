---
title: 로그인 자격 증명 및 URL
description: 관리자 및 상점 첫 화면에 대한 액세스 권한을 얻는 데 사용되는 상거래 URL 및 계정 자격 증명에 대해 알아봅니다.
exl-id: fa16b7e9-e05f-4eb8-bc32-596946c57e1c
feature: System
role: Admin, Leader
source-git-commit: 3ff5807fd0a3ebf2e9d4f9c085852dd7777a1103
workflow-type: tm+mt
source-wordcount: '339'
ht-degree: 0%

---

# 로그인 자격 증명 및 URL

설정 및 구성을 계속하기 전에 스토어 관리자 및 상거래 계정에 액세스하는 데 필요한 정보가 있는지 확인하십시오.

## Storefront URL

에 대한 주소 [상점 첫 화면](storefront.md) 는 일반적으로 IP 주소에 할당된 도메인입니다. 일부 저장소는 루트 또는 최상위 디렉토리에 설치됩니다. 다른 기능은 루트 아래의 디렉토리에 설치됩니다. 저장소는 주 도메인과 연관된 하위 도메인 내에 상주할 수 있습니다. 스토어 URL은 다음 중 하나와 비슷할 수 있습니다.

- `http://mydomain.com`
- `http://www.mydomain.com/mystore`
- `http://xxx.xxx.xxx.xxx`s

도메인이 아직 없는 경우 스토어 URL에는 각각 마침표로 구분된 일련의 4개의 숫자가 포함됩니다 _점선 4진수_ 표기법.

## 관리자 URL

스토어 주소 [관리자](admin.md) 설치 중에 설정됩니다. 기본 주소는 저장소와 동일하지만 `/admin` 끝에 있습니다. 이 안내서의 예제에서 기본 디렉터리를 사용하지만 저장소에 고유한 위치에서 관리자를 실행하는 것이 가장 좋습니다.

- `http://mydomain.com/admin`
- `http://www.mydomain.com/admin`

## [!DNL Commerce] account

사용자 [상거래 계정](commerce-account-create.md) 는 제품 및 서비스, 계정 설정, 청구 내역 및 지원 리소스에 대한 정보에 대한 액세스를 제공합니다. 계정에 액세스하려면 기본 상거래 사이트로 이동하여 을(를) 클릭하십시오. **[!UICONTROL My Account]** 오른쪽 상단 모서리입니다.

## 고객 계정

가게를 돌아다니는 방법을 배우는 동안, 반드시 테스트를 설치하세요 [고객 계정](../customers/account-dashboard.md)를 통해 고객의 관점에서 스토어 및 체크아웃 프로세스를 경험할 수 있습니다.

## 샘플 데이터

Adobe은 250개 이상의 제품(약 200개 제품은 구성 가능한 제품임), 카테고리, 프로모션 가격 규칙, CMS 페이지, 배너 등이 있는 샘플 스토어를 포함하는 샘플 데이터 세트를 제공합니다. 샘플 데이터는 _Luma_ 상점 앞의 테마. [이 샘플 데이터 설치](https://experienceleague.adobe.com/docs/commerce-operations/installation-guide/next-steps/sample-data/overview.html) 는 선택 사항이지만 eCommerce 비즈니스의 사용자 지정 사항을 테스트하고 개발하는 데 도움이 될 수 있습니다.
