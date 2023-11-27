---
title: 사이트, 스토어 및 보기 범위
description: 고객을 위한 쇼핑 경험을 전달하는 데 사용할 수 있는 웹 사이트, 스토어 및 스토어 조회수의 계층 구조에 대해 알아봅니다.
exl-id: 80fc1b73-c869-4f1c-b1a1-d61823b91d83
feature: System, Site Management
source-git-commit: 370131cd73a320b04ee92fa9609cb24ad4c07eca
workflow-type: tm+mt
source-wordcount: '678'
ht-degree: 0%

---

# 사이트, 스토어 및 보기 범위

모든 Adobe Commerce 및 Magento Open Source 설치에는 [계층](../stores-purchase/stores.md) 웹 사이트, 스토어 및 스토어 조회수 용어 _범위_ 계층 구조에서 제품, 속성 또는 범주와 같은 데이터베이스 엔티티 컨텐츠 요소 또는 구성 설정이 적용되는 위치를 결정합니다. 웹 사이트, 스토어 및 스토어 보기에는 일대다 상위/하위 관계가 있습니다. 단일 설치에는 여러 웹 사이트가 있을 수 있으며 각 웹 사이트에는 여러 스토어와 스토어 보기가 있을 수 있습니다.

>[!NOTE]
>
>자세한 내용은 다음을 참조하십시오. [여러 웹 사이트 또는 스토어](https://experienceleague.adobe.com/docs/commerce-operations/configuration-guide/multi-sites/ms-overview.html) 다음에서 [!DNL Commerce] 개발자 설명서.

## 웹 사이트

설치는 단일 설치로 시작합니다. [웹 사이트](../stores-purchase/stores.md#add-websites), 호출됩니다. _기본 웹 사이트_ 기본적으로. 단일 설치에 대해 각각 고유한 IP 주소와 도메인이 있는 여러 웹 사이트를 설정할 수도 있습니다.

## 스토어

단일 웹 사이트에는 여러 개의 [스토어](../stores-purchase/stores.md#add-stores), 각각 고유의 메인 메뉴가 있습니다. 상점에서는 제품 카탈로그를 공유하지만 다양한 제품 및 디자인을 선택할 수 있습니다. 동일한 웹 사이트의 모든 스토어는 관리 및 체크아웃을 공유합니다.

## 보기 저장

고객이 이용할 수 있는 매장은 특정 매장에 따라 제시된다 _[보기](../stores-purchase/store-views.md)_. 처음에는 스토어에 단일 기본 보기가 있습니다. 다른 언어를 지원하거나 다른 목적으로 스토어 보기를 추가할 수 있습니다. 고객은 헤더에서 언어 선택기를 사용하여 스토어 보기를 변경할 수 있습니다.

웹 사이트, 스토어 및 스토어 조회수를 사용하여 작업할 때 다음 사항에 유의하십시오.

- 상거래 인스턴스에는 글로벌 → 웹 사이트 → 스토어 → 스토어 보기의 캐스케이드 모델이 있습니다.
- 모든 웹 사이트에는 최소 하나의 기본 스토어 및 스토어 보기가 있습니다.
- 각 스토어 보기에는 서로 다른 기본 URL이 있을 수 있습니다.
- 웹 사이트의 기본 기능은 최상위 기능 구성입니다.
- 저장소의 기본 기능은 루트 범주 구성입니다.
- 스토어 보기의 주요 기능은 번역 정보 및 통화 기호 구성입니다.

## 범위 설정

Adobe Commerce 또는 Magento Open Source 설치 시 웹 사이트, 스토어 또는 보기 계층이 있는 경우 컨텍스트를 설정하거나 _범위_ 구성 설정. 또한 많은 데이터베이스 엔티티의 컨텍스트에 특정 범위를 지정하여 저장소 계층에서 사용되는 방식을 결정할 수 있습니다. 자세한 내용은 다음을 참조하십시오. [제품 범위](../catalog/introduction.md#product-scope) 및 [가격 범위](../catalog/catalog-price-scope.md).

우편 번호와 같은 일부 구성 설정에는 시스템 전체에서 동일한 값이 사용되므로 전역 범위가 있습니다. 다음 [웹 사이트](../stores-purchase/stores.md#add-websites) 범위는 모든 스토어와 해당 보기를 포함하여 계층 구조에서 해당 수준 아래에 있는 모든 스토어에 적용됩니다. 범위의 모든 항목 [스토어 뷰](../stores-purchase/store-views.md) 는 일반적으로 여러 언어를 지원하는 데 사용되는 각 스토어 보기에 대해 다르게 설정할 수 있습니다. 구성 설정의 기본값을 무시하려면 다음을 참조하십시오. [범위 설정](../configuration-reference/scope-change.md#set-the-scope).

스토어가 실행 중인 경우가 아니면 [단일 스토어 모드](#single-store-mode), 각 구성 설정의 범위는 필드 레이블 아래에 작은 텍스트로 표시됩니다. 설치에 여러 웹 사이트, 스토어 또는 보기가 포함된 경우 [스토어 뷰](../stores-purchase/store-views.md) 변경하기 전에 설정이 적용되는 위치.

![웹 사이트, 스토어 및 스토어 조회수 계층](./assets/scope-multisite.svg){width="550"}

| 범위 | 설명 |
|--- |--- |
| [!UICONTROL Global] | 설치 전체에서 사용할 수 있는 시스템 전체 설정 및 리소스 |
| [!UICONTROL Website] | 현재 웹 사이트로 제한된 설정 및 리소스입니다. 각 웹 사이트에는 기본 스토어가 있습니다. |
| [!UICONTROL Store] | 현재 스토어로 제한된 설정 및 리소스입니다. 각 스토어에는 기본 루트 카테고리(메인 메뉴) 및 기본 스토어 보기가 있습니다. |
| [!UICONTROL Store View] | 현재 저장소 보기로 제한된 및 리소스 설정. |

{style="table-layout:auto"}

## 단일 스토어 모드

Commerce 설치에 단일 스토어 및 스토어 뷰만 있는 경우 모든 스토어 뷰 옵션 및 범위 표시기를 꺼서 표시를 단순화할 수 있습니다. 다음을 수행하는 경우 단일 스토어 모드가 재정의됩니다. [더 많은 스토어 조회수 추가](../stores-purchase/store-views.md) 나중에.

![범위 - 단일 보기](./assets/scope-single-view.svg){width="550"}

1. 다음에서 _관리자_ 사이드바, 이동 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. 아래 **[!UICONTROL General]**, 페이지 아래쪽으로 스크롤하여 를 확장합니다. **[!UICONTROL Single-Store Mode]** 섹션.

1. 설정 **[!UICONTROL Enable Single-Store Mode]** 끝 `Yes`.

   ![일반 구성 - 단일 스토어 모드 활성화](./assets/general-single-store-mode.png){width="400"}

1. 클릭 **[!UICONTROL Save Config]**.

1. 캐시를 새로 고치라는 메시지가 표시되면 다음을 수행합니다.

   - 다음을 클릭합니다. **[!UICONTROL Cache Management]** 페이지 맨 위에 있는 시스템 메시지의 링크입니다.

     ![시스템 메시지 - 캐시 관리](../catalog/assets/msg-cache-management.png){width="600" zoomable="yes"}

   - 다음 항목 선택 **[!UICONTROL Page Cache]** 확인란.

   - 포함 **[!UICONTROL Actions]** 을 로 설정 `Refresh`, 클릭 **[!UICONTROL Submit]**
