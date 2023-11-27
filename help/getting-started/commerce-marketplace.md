---
title: '[!DNL Adobe Commerce Marketplace]'
description: 에 대해 알아보기 [!DNL Commerce Marketplace]는 판매자에게 선별된 솔루션을 제공하고 자격을 갖춘 개발자에게 번창하는 비즈니스를 구축할 수 있는 도구, 플랫폼 및 주요 위치를 제공합니다.
exl-id: e04e48f2-3b1d-45bf-b0f6-3a1ed43e78c5
feature: Extensions
source-git-commit: 1a5a00493e9994343c7decc763f2decdd11192c7
workflow-type: tm+mt
source-wordcount: '892'
ht-degree: 0%

---

# Adobe Commerce 마켓플레이스

[Adobe Commerce 마켓플레이스][1] 은 판매자에게 엄선된 솔루션을 제공하고 자격을 갖춘 개발자에게 번창하는 비즈니스를 구축할 수 있는 도구, 플랫폼 및 주요 위치를 제공하는 애플리케이션 스토어입니다. [!DNL Commerce Marketplace] 은 무료로 사용할 수 있는 다양한 확장 프로그램을 제공하며, 다른 확장 프로그램은 판매합니다. 구매는 신용 카드로 결제하거나 [PayPal][2].

사용 가능한 모든 확장 [!DNL Commerce Marketplace] 광범위한 검토를 통과했습니다. 다음 [확장 품질 프로그램][3] (EQP) 조합 [!DNL Commerce] Commerce Marketplace의 모든 확장이 코딩 표준 및 모범 사례를 충족하도록 하는 전문 지식, 개발 지침 및 확인 도구입니다. 검토 프로세스에는 자동화된 검사와 수동 QA 검토가 모두 포함됩니다. 이 과정에서 각 확장의 구조와 코드를 검사하고 바이러스/맬웨어 감염의 증거 및 표절 징후를 검사합니다. 검토에는 심층 기술 검사와 관리자가 실시하는 온전성 검사가 포함됩니다. [!DNL Commerce] 설명서, 코딩 구조, 성능, 확장성, 보안 및 과의 호환성에 중점을 둔 엔지니어 [!DNL Commerce] 코어.

다른 소스에서 확장을 구입할 수 있지만에서 사용할 수 있는 확장만 [!DNL Commerce Marketplace] 는 Extension Quality Program 내에서 광범위한 기술 및 마케팅 검토를 통해 검증됩니다.

## 앱 리소스

개발자는 전통적으로 PHP를 사용하여 Adobe Commerce에 기능, 서비스 및 통합을 추가하기 위해 처리 중인 확장을 개발했습니다. 확장과 달리 프로세스 외부 확장성으로 앱을 만들면 호환성 문제를 방지할 수 있습니다.

다음 리소스는 새 채택자가 앱에 익숙해질 수 있는 시작점을 제공합니다.

### Commerce 리소스:

- [Adobe Commerce에 대한 I/O 이벤트 설정](https://developer.adobe.com/commerce/extensibility/events/)
- [Adobe Commerce에 대한 이벤트 구성](https://developer.adobe.com/commerce/extensibility/events/configure-commerce/)
- [관리 UI SDK 설정](https://developer.adobe.com/commerce/extensibility/admin-ui-sdk/)
- [확장을 앱으로 변환](https://developer.adobe.com/commerce/extensibility/app-development/#how-do-i-port-an-extension-into-an-app)

### App Builder 리소스:

- [Commerce App Builder 개요](https://developer.adobe.com/commerce/extensibility/app-development/)
- [Adobe Developer App Builder용 API Mesh 설정](https://developer.adobe.com/graphql-mesh-gateway/gateway/getting-started/)
- [App Builder 앱 배포](https://developer.adobe.com/app-builder/docs/guides/deployment/)
- [App Builder 앱용 CI/CD](https://developer.adobe.com/app-builder/docs/guides/deployment/ci_cd_for_firefly_apps/)
- App Builder/Developer Console 시작하기
   - [App Builder 시작하기](https://developer.adobe.com/app-builder/docs/getting_started/)
   - [프로젝트 및 작업 공간 이해](https://developer.adobe.com/app-builder/docs/resources/videos/exploring/projects-and-workspaces/)

## [!DNL Marketplace] 자격 증명

에서 구입한 확장을 설치하기 전에 [!DNL Commerce Marketplace], 다음에 로그인 [!DNL Commerce] 계정 을 설정하고 활성 액세스 키가 있는지 확인하십시오. 다음에 로그인할 수 있습니다. [!DNL Commerce] 머리글의 계정 [[!DNL Marketplace]][1] 또는 [Magento.com][6].

액세스 키는 을(를) 동기화하는 데 사용되는 공개 및 비공개 키 세트입니다. [!DNL Commerce] 를 사용한 설치 [!DNL Commerce] 계정을 만들고 자격 증명을 확인합니다. 계정이 동기화된 후에는 Commerce Marketplace 또는 업그레이드에서 확장 또는 모듈을 설치할 때마다 개인 키를 입력해야 합니다. [!DNL Commerce] 설치.

다양한 용도로 여러 액세스 키를 만들고 필요에 따라 활성화하거나 비활성화할 수 있습니다. 그러나 를 설치하는 데 사용한 것과 동일한 액세스 키를 사용해야 합니다. [!DNL Commerce] 소프트웨어. 예를 들어 Magento Open Source 액세스 키를 사용하여 Adobe Commerce을 업데이트하거나 업그레이드할 수 없으며, 반대로 할 수도 없습니다. 다른 사용자 또는 의 액세스 키에 속한 액세스 키도 사용할 수 없습니다. [공유 계정](commerce-account-share.md).

### 액세스 키 만들기

1. 다음에 로그인 [!DNL Commerce] 계정입니다.

1. 다음에서 _[!UICONTROL My Account]_페이지에서&#x200B;**[!UICONTROL Marketplace]**탭.

1. 이름 옆의 오른쪽 위 모서리에서 아래쪽 화살표를 클릭하고 을 선택합니다 **[!UICONTROL My Profile]**.

   ![사용자 [!DNL Marketplace] 프로필](./assets/marketplace-profile.png){width="600"}

1. 다음에서 _[!UICONTROL Marketplace]_아래의 탭_[!UICONTROL My Products]_, 클릭 **[!UICONTROL Access Keys]**&#x200B;을 클릭하고 다음 중 하나를 수행합니다.

   - Marketplace 구매를 위한 액세스 키 세트가 이미 있는지 확인하십시오. 다양한 용도로 여러 액세스 키 세트를 만들 수 있습니다.

   ![액세스 키](./assets/access-keys.png){width="600"}

   - 클릭 **[!UICONTROL Create a New Access Key]**. 새 키 쌍의 이름을 입력하고 를 클릭합니다 **[!UICONTROL OK]**. 유효한 문자에는 대/소문자 문자와 공백 대신 하이픈이 포함됩니다.

1. 완료되면 다음을 클릭하십시오. **[!UICONTROL OK]**.

   새 액세스 키가 활성화되고 목록에 나타납니다.

   다음 사항에 주목합니다. _복사_ 각 공개 및 개인 키 뒤에 연결합니다. 다음 단계에서는 이러한 값을 복사하여 붙여넣어 저장소를 Commerce Marketplace과 동기화합니다.

## 설치 프로세스

>[!IMPORTANT]
>
>Adobe Commerce 및 Magento Open Source 2.4.0부터 웹 설치 마법사가 제거되므로 다음 작업을 수행하려면 명령줄을 사용해야 합니다. [설치](https://experienceleague.adobe.com/docs/commerce-operations/installation-guide/advanced.html) 또는 [업그레이드](https://experienceleague.adobe.com/docs/commerce-operations/upgrade-guide/implementation/perform-upgrade.html) 인스턴스. 이 요구 사항에는 다음도 포함됩니다 [모듈](https://experienceleague.adobe.com/docs/commerce-operations/upgrade-guide/modules/upgrade.html) 및 [확장](https://experienceleague.adobe.com/docs/commerce-operations/installation-guide/tutorials/extensions.html).

에 대한 설치 프로세스 [!DNL Marketplace] 다음에 대한 구매는 다릅니다. _온-프레미스_ 에 호스팅되는 설치보다 Commerce 설치 [Adobe 클라우드 아키텍처][4].

![Commerce Marketplace](./assets/marketplace.png){width="600"}

## 지원

확장 설치 또는 사용에 대한 도움이 필요한 경우 확장과 함께 제공되는 설명서를 먼저 살펴보십시오. 질문에 대한 답변을 찾을 수 없는 경우 확장 목록에 있는 연락처 정보를 사용하여 개발자에게 직접 문의하십시오.

Commerce Marketplace 시 구입한 물건이 본인의 요구를 충족하지 못할 경우 구입일로부터 25일 이내에 환불을 요청할 수 있습니다. Adobe이 모든 환불 요청을 검토하고 승인된 경우 적절한 환불을 발행합니다.

Commerce Marketplace과 관련된 지원 문제는 다음을 참조하십시오. [[!DNL Marketplace] 도움말 센터][5].

[1]: https://marketplace.magento.com/
[2]: https://www.paypal.com/us/home
[3]: https://developer.adobe.com/commerce/marketplace/guides/sellers/extension-quality-program/
[4]: https://www.adobe.com/commerce/magento/enterprise.html
[5]: https://marketplacesupport.magento.com/hc/en-us
[6]: https://business.adobe.com/products/magento/magento-commerce.html
