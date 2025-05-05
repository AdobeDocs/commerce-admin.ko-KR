---
title: Adobe Commerce 관리 사용 안내서
description: Adobe Commerce 제품 설명서 찾아보기
seo-title: Services for Adobe Commerce
seo-description: Documentation and resources for Adobe Commerce and Magento Open Source users working in the Admin.
breadcrumb-title: 관리 사용 안내서
exl-id: e30f769f-9140-4370-943e-75007b39ebc0
source-git-commit: d5120cf04de400ce875309f6eb71596430e27401
workflow-type: tm+mt
source-wordcount: '1199'
ht-degree: 0%

---

# &#x200B;<!-- use banner as heading -->![관리자 설명서](./assets/banner-user-home.png) {#documentation}

세계 최고의 디지털 상거래 플랫폼인 차세대 플랫폼에 오신 것을 환영합니다. Adobe Commerce은 온라인 상인에게 온라인 스토어의 모양, 콘텐츠 및 기능에 대한 탁월한 유연성과 통제력을 제공합니다. 관리자는 강력한 마케팅, 검색 엔진 최적화 및 제품 관리 도구를 통해 고유한 비즈니스 요구 사항에 맞는 사이트를 만들 수 있습니다.

관리 사용 안내서의 정보는 Adobe Commerce 관리 또는 Magento Open Source 코드 베이스에서 작업 중인 비즈니스 사용자를 수용하도록 설계되었습니다. Adobe Commerce 또는 확장된 기능 세트에 배타적인 기능 및 기능에 대한 표기법이 있습니다.

## Adobe Commerce {#product-editions}

Adobe Commerce은 상인과 브랜드가 온라인 및 물리적 공간에서 고객 중심의 디지털 상거래 경험을 통해 매출을 가속화할 수 있도록 하는 애자일 B2B 및 B2C 상거래 플랫폼입니다. SLA가 보장된 온프레미스 및 관리 클라우드에 이르기까지 가장 유연한 배포 모델을 제공하므로 중간 규모 및 엔터프라이즈 조직을 위한 최고의 선택입니다. Adobe Commerce은 API 우선 통합 및 완전히 맞춤화가 가능한 확장을 지원하며 마케팅부터 머천다이징 및 이행에 이르기까지 가장 풍부한 엔터프라이즈급 상거래 경험 기능 세트를 제공합니다. Adobe Commerce은 다른 상거래 플랫폼과 마찬가지로 유연성과 확장성을 제공하기 위해 오픈 소스 코드 기반으로 구축됩니다.

Adobe Commerce에 포함된 고급 기능 목록을 보려면 _릴리스 정보_&#x200B;에서 [Commerce 기능](https://experienceleague.adobe.com/docs/commerce-operations/release/features.html?lang=en)을 참조하세요.

## Magento Open Source 코드 베이스

Magento Open Source은 Adobe이 Adobe Commerce에 공식적으로 기여하고 호환성이 보장되는 코드 베이스입니다. 이 코드 베이스는 빠른 성장을 열망하는 소규모 비즈니스를 육성하고 개인 개발자에게 권한을 부여하기 위한 Adobe 이니셔티브의 일부입니다.

## 관리 사용 안내서

<table>
<tr>
   <td valign="top" width="60px">
       <img alt="시작" src="./assets/icon-lightbulb.svg" width="40" height="40" /></td>
   <td valign="top">
   <a href="https://experienceleague.adobe.com/docs/commerce-admin/start/guide-overview.html"><strong>시작</strong></a>
    <div>
    <em>리소스 및 참조 정보뿐만 아니라 대부분의 판매자가 관리자에게 처음 배울 때 갖는 "이유, 위치, 방법" 질문입니다. 이 안내서는 더 많은 고급 주제에 대한 발판이 됩니다.</em>
    <br> </div>
  </td>
  </tr>
<tr>
  <td valign="top">
      <img alt="Adobe Commerce" src="./assets/icon-building.svg" width="40" height="40"/></td>
   <td valign="top"><a href="https://experienceleague.adobe.com/docs/commerce-admin/b2b/guide-overview.html"><strong>Adobe Commerce B2B</strong></a> [!BADGE PaaS만 해당]{type=Informative url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="Adobe Commerce on Cloud 프로젝트(Adobe 관리 PaaS 인프라) 및 온-프레미스 프로젝트에만 적용됩니다."}
    <div><em>이 기능 세트는 복잡한 조직 구조와 다양한 역할 및 구매 권한 수준을 가진 여러 직원을 가진 회사를 주로 사용하는 판매자(판매자)의 요구를 충족하도록 설계되었습니다.</em>
    <br></div>
  </td>
</tr>
<tr>
  <td valign="top">
    <img alt="카탈로그 관리" src="./assets/icon-shop.svg" width="40" height="40"/></td>
   <td valign="top"><a href="https://experienceleague.adobe.com/docs/commerce-admin/catalog/guide-overview.html"><strong>카탈로그 관리</strong></a>
    <div><em>스토어를 만들고 관리하는 데 가장 중요한 영역 중 하나는 제품 카탈로그와 카테고리입니다. 관리자는 스토어와 제품 카탈로그의 초기 설정을 위한 다양한 도구를 제공합니다.</em>
    <br></div>
  </td>
    </tr>
<tr>
    <td valign="top">
       <img alt="Inventory management" src="./assets/icon-transfer.svg" width="40" height="40"/></td>
   <td valign="top"><a href="https://experienceleague.adobe.com/docs/commerce-admin/inventory/guide-overview.html"> <strong>[!DNL Inventory Management]</strong></a>
    <div><em>단일 상점을 가진 상인이 [!DNL Inventory Management] 기능을 사용하여 여러 창고, 상점, 픽업 위치, 직송 업체 등에 액세스할 수 있습니다. 이러한 기능을 사용하여 판매 수량을 관리하고 납품을 처리하여 주문을 완료합니다. </em></div>
  </td>
</tr>
<tr>
    <td valign="top">
       <img alt="머천다이징 및 프로모션" src="./assets/icon-labels.svg" width="40" height="40"/></td>
   <td valign="top"><a href="https://experienceleague.adobe.com/docs/commerce-admin/marketing/guide-overview.html"> <strong>머천다이징 및 프로모션</strong></a>
    <div><em>타깃팅된 프로모션과 고객 참여를 위한 기회를 만들어 쇼핑객을 구매자로 전환합니다. 구매 후 활동을 지원하고 재방문 고객에게 특별 할인을 제공하여 고객 관계를 관리합니다. SEO 이니셔티브를 지원하는 모범 사례 및 기법을 알아봅니다.</em></div>
  </td>
</tr>
<tr>
    <td valign="top">
       <img alt="컨텐츠 및 디자인" src="./assets/icon-color-wheel.svg" width="40" height="40"/></td>
   <td valign="top"><a href="https://experienceleague.adobe.com/docs/commerce-admin/content-design/guide-overview.html"> <strong>콘텐츠 및 디자인</strong></a>
    <div><em>콘텐츠는 고객이 스토어에 액세스할 때 볼 수 있는 페이지 및 요소를 정의합니다. 페이지의 텍스트 및 이미지와 같은 기본 요소를 정의하며, 쇼핑 환경을 개선하기 위해 대화형 및 동적 콘텐츠를 제공하는 고급 요소를 정의합니다.</em></div>
  </td>
</tr>
<tr>
    <td valign="top">
       <img alt="페이지 빌더" src="./assets/icon-web-pages.svg" width="40" height="40"/></td>
   <td valign="top"><a href="https://experienceleague.adobe.com/docs/commerce-admin/page-builder/guide-overview.html"> <strong>[!DNL Page Builder]</strong></a> [!BADGE PaaS만 해당]{type=Informative url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="Adobe Commerce on Cloud 프로젝트(Adobe 관리 PaaS 인프라) 및 온-프레미스 프로젝트에만 적용됩니다."}
    <div><em>[!DNL Page Builder]을(를) 사용하면 사용자 지정 레이아웃으로 콘텐츠가 풍부한 페이지를 쉽게 만들 수 있습니다. 이러한 기능은 품질을 향상시키고 사용자 지정 페이지를 제작하는 시간과 비용을 줄이기 위해 설계되었습니다.</em></div>
  </td>
</tr>
<tr>
    <td valign="top">
       <img alt="고객 관리" src="./assets/icon-demographic.svg" width="40" height="40"/></td>
   <td valign="top"><a href="https://experienceleague.adobe.com/docs/commerce-admin/customers/guide-overview.html"> <strong>고객 관리</strong></a>
    <div><em>스토어를 계속 유지 관리하고 확장할 때 관리에서 고객 계정과 고객 그룹을 관리하십시오.</em></div>
  </td>
</tr>
<tr>
    <td valign="top">
       <img alt="저장 및 구매 경험" src="./assets/icon-shopping-cart.svg" width="40" height="40"/></td>
   <td valign="top"><a href="https://experienceleague.adobe.com/docs/commerce-admin/stores-sales/guide-overview.html"> <strong>경험 저장 및 구매</strong></a>
    <div><em>장바구니가 구매 및 포기의 교차 지점에서 구매할 경로의 끝에 있습니다. 장바구니 항목을 완료된 주문으로 바꾸는 구매 지점 및 지원 기능을 설정합니다.</em></div>
  </td>
</tr>
<tr>
    <td valign="top">
       <img alt="관리 시스템" src="./assets/icon-globe-grid.svg" width="40" height="40"/></td>
   <td valign="top"><a href="https://experienceleague.adobe.com/docs/commerce-admin/systems/guide-overview.html"> <strong>관리 시스템</strong></a>
    <div><em>관리자가 시스템을 관리하고 성능을 최적화하는 여러 가지 도구를 제공합니다. 이 안내서에는 관련된 역할 및 권한과 함께 관리자 사용자 계정 관리에 대한 정보가 포함되어 있습니다.</em></div>
  </td>
</tr>
<tr>
    <td valign="top">
       <img alt="구성 참조" src="./assets/icon-settings.svg" width="40" height="40"/></td>
   <td valign="top"><a href="https://experienceleague.adobe.com/docs/commerce-admin/config/guide-overview.html"> <strong>구성 참조</strong></a>
    <div><em>관리자의 모든 구성 설정에 대한 필드 설명을 제공하는 빠르고 편리한 참조입니다.</em></div>
  </td>
</tr>
</table>

## 관리 사용 안내서의 새로운 기능

>[!TIP]
>
>[Commerce 서비스 설명서의 새로운 기능](https://experienceleague.adobe.com/docs/commerce/user-guides/home.html#what%E2%80%99s-new) 및 [운영 안내서의 새로운 기능](https://experienceleague.adobe.com/docs/commerce-operations/operational-guides/home.html#what%E2%80%99s-new)을 검토할 수도 있습니다.

| 설명 | 유형 | 날짜 |
| ----------- | ---- | ---- |
| **1.4.0 B2B 릴리스** - Adobe Commerce B2B 릴리스 노트는 [1.4.0 릴리스](../b2b/release-notes.md#b2b-v140)에 대한 변경 사항 및 추가 사항에 대해 설명합니다. | 업데이트 | 06/13/23 |
| **1.4.0 B2B 릴리스** - [구매자에 대한 견적 시작](../b2b/sales-rep-initiates-quote.md) 주제가 이제 _Adobe Commerce B2B 안내서_&#x200B;에 포함되어 있습니다. 판매자가 협상 프로세스를 시작하기 위해 특정 구매자에 대한 견적을 생성하는 방법에 대해 설명합니다. | 신규 | 06/13/23 |
| **1.4.0 B2B 릴리스** - [견적 협상](../b2b/quote-price-negotiation.md), [협상 가능한 견적](../b2b/quotes.md) 및 [B2B 기능 사용](../b2b/enable-basic-features.md) 주제가 판매자가 시작한 견적 및 기본 기능의 변경 사항을 반영하도록 업데이트됩니다. | 업데이트 | 06/13/23 |
| **2.2.0 Adobe IMS 통합 릴리스** - [Adobe ID과 Commerce Admin Integration 비활성화](../getting-started/adobe-ims-disable.md) 주제가 이제 _시작 안내서_&#x200B;에 포함되어 있습니다. Adobe IMS와 Adobe Commerce Admin 통합을 사용하지 않도록 설정하는 선택적 절차에 대해 설명합니다. | 신규 | 06/13/23 |
| **2.2.0 Adobe IMS 통합 릴리스** - [Adobe IMS(Identity Management Service) 통합 개요](../getting-started/adobe-ims-integration-overview.md) 및 [Adobe ID과 Commerce Admin Integration 구성](../getting-started/adobe-ims-config.md) 주제의 변경 사항으로 업데이트된 기능을 반영합니다. | 업데이트 | 06/13/23 |
| **[!DNL Audience Activation]** - [!DNL Experience Platform Connector] 구성 UI와 장바구니 가격 규칙 및 동적 블록과 함께 headless Commerce 인스턴스를 사용하는 방법을 반영하도록 [[!DNL Audience Activation]](../customers/audience-activation.md) 주제에 새로 추가되고 업데이트되고 개선된 정보가 포함되어 있습니다. | 업데이트 | 06/13/23 |
| **UPS API 사용 중단** - 새 API 키를 생성하기 위해 UPS API의 임시 사용 중단을 반영하도록 [UPS(United Parcel Service)](../stores-purchase/ups.md) 항목 및 [배달 방법](../configuration-reference/sales/delivery-methods.md#ups) 구성 참조 페이지를 업데이트했습니다. | 업데이트 | 06/08/23 |
| **2.4.6 릴리스** - 큰 카탈로그의 성능을 개선하는 데 사용할 수 있는 제품 표시 제한 사항에 대한 정보를 포함하도록 [제품 목록](../catalog/products-list.md) 및 [관리자 구성 참조](../configuration-reference/advanced/admin.md) 항목을 업데이트했습니다. | 업데이트 | 03/14/23 |
| **2.4.6 릴리스** - 세그먼트에 대한 실시간 유효성 검사에 대한 정보를 포함하도록 [고객 세그먼트 만들기 및 삭제](../customers/customer-segment-create.md) 및 [고객 구성 참조](../configuration-reference/customers/customer-configuration.md) 항목을 업데이트했습니다. | 업데이트 | 03/14/23 |
| **2.4.6 릴리스** - 번들 Braintree 통합에서 지원하는 업데이트된 및 새로운 결제 옵션을 반영하도록 [Braintree](../stores-purchase/braintree.md) 및 [Braintree 구성 참조](../configuration-reference/sales/braintree.md) 항목을 업데이트했습니다. | 업데이트 | 03/14/23 |
| **2.4.6 릴리스** - 새 [!DNL Fixer API]&#x200B;(APILayer) 옵션을 포함하도록 [통화 구성](../stores-purchase/currency-configuration.md) 및 [통화 설정 구성](../configuration-reference/general/currency-setup.md) 항목을 업데이트했습니다. | 업데이트 | 03/14/23 |
| **2.4.6 릴리스** - 전자 메일 통신에 대한 새 SMTP 옵션을 포함하도록 [전자 메일 통신 구성](../systems/email-communications.md) 및 [시스템 구성 참조](../configuration-reference/advanced/system.md#uicontrol-mail-sending-settings) 항목을 업데이트했습니다. | 업데이트 | 03/14/23 |
| **2.4.6 릴리스** - 최신 번들 확장 버전(v1.2.6)에 포함된 수정 사항에 대한 설명 목록으로 [Inventory management 릴리스 정보](../inventory-management/release-notes.md)를 업데이트했습니다. | 업데이트 | 03/14/23 |
| **2.4.6 릴리스** - 최신 확장 버전(v1.3.5)에 포함된 수정 사항에 대한 설명 목록으로 [B2B 릴리스 정보](../b2b/release-notes.md)를 업데이트했습니다. | 업데이트 | 03/14/23 |
| **새 주제** - Adobe Commerce에서 Real-Time CDP 대상을 활성화하는 방법에 대한 자세한 정보를 제공하는 _고객 관리 안내서_&#x200B;에 [대상 활성화](../getting-started/commerce-account-transfer.md) 주제를 추가했습니다. | 신규 | 03/13/23 |
| **새 주제** - [Commerce 계정 전송](../getting-started/commerce-account-transfer.md) 주제를 _시작 안내서_&#x200B;에 추가했습니다. | 신규 | 202/27/23 |

{style="table-layout:auto"}
