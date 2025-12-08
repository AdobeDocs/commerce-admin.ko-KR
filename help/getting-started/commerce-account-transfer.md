---
title: Commerce 계정 양도
description: Commerce 계정을 다른 소유자 또는 이메일 주소로 전송하는 방법을 알아봅니다.
exl-id: f6528931-dbf1-4702-8989-232c27969c4a
feature: User Account
source-git-commit: a7b23834b00b2ae0f5fd98de47fdc6f4aa00c010
workflow-type: tm+mt
source-wordcount: '1196'
ht-degree: 0%

---

# Commerce 계정 양도

비즈니스 책임이 변경되면 Commerce 계정을 새 소유자나 다른 이메일 주소로 전송해야 할 수 있습니다. 이 전송을 수행하려면 계정과 연결된 기본 사용자 이메일을 변경해야 합니다.

다음 정보는 MAGEID(Commerce) 계정을 전송하는 프로세스를 설명합니다. 클라우드 계정(클라우드 프로젝트 또는 New Relic) 소유권에 대한 변경 사항은 포함되지 않습니다. 클라우드 프로젝트 액세스에 대한 자세한 내용은 [Commerce on Cloud Infrastructure Guide](https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/project/user-access.html)에서 _사용자 액세스 관리_&#x200B;를 참조하십시오.

>[!IMPORTANT]
>
>새 계정 소유자가 공유 액세스를 사용하여 확장을 구매한 경우 계정 전송 프로세스가 시작되자마자 해당 확장에 대한 액세스가 손실됩니다. 계정 이전을 요청하기 전에 새 소유자가 [마켓플레이스 계정](https://commercemarketplace.adobe.com/sales/order/history/)에서 구매한 항목에 대한 주문 ID를 검색하고 [마켓플레이스 팀](https://experienceleague.adobe.com/en/docs/commerce-knowledge-base/kb/help-center-guide/magento-help-center-user-guide#support-case)에서 해당 확장에 대한 환불을 요청하는지 확인하십시오. 확장 구매를 다른 계정으로 이전할 수 없습니다.

## 전송 유형 식별

Commerce 계정 전송 유형은 현재 소유자 및 새 소유자가 사용할 수 있는 Commerce 계정 자격 증명에 따라 다릅니다. 다음 시나리오에서는 이러한 자격 증명을 기반으로 하는 다양한 전송 유형을 설명합니다.

| 전송 유형 | 현재 소유자 | 새 소유자 |
| ------------- | ------------- | --------- |
| [새 Adobe ID 및 전자 메일 변경](#new-adobe-id-and-email-change) | **_이(가) Adobe 로그인 계정에 연결되어 있지_**&#x200B;않은 MAGEID가 있습니다. | MAGEID가 없으며 Adobe 로그인 계정에 연결되어 있지 않습니다. |
| [전자 메일 변경](#email-change) | Adobe 로그인 계정으로 **_연결_**&#x200B;된 MAGEID가 있습니다. | Adobe 로그인 계정이 있지만 **_Adobe 로그인 계정에 연결된 MAGEID_**&#x200B;이(가) 없습니다. |
| [Adobe ID 계정 스위치](#adobe-id-account-switch) | Adobe 로그인 계정에 **_연결_**&#x200B;된 MAGEID가 있습니다. | MAGEID가 있고 Adobe 로그인 계정에 연결되어 있습니다. |

{style="table-layout:auto"}

>[!NOTE]
>
>Adobe Commerce이 다른 Adobe 솔루션과 계속 통합됨에 따라 이제 Commerce 계정(MAGEID)에 Adobe 로그인과 연결해야 합니다. 이 Adobe ID은 Commerce 계정에 연결된 것과 동일한 이메일 주소를 사용합니다.

## 새로운 Adobe ID 및 이메일 변경

>[!IMPORTANT]
>
>[전송 형식](#identify-your-transfer-type)을(를) 검토하고 이 단계 순서에 대한 사전 조건을 충족하는지 확인하십시오.

이 전송 유형을 사용하려면 기존 Commerce 계정에 연결된 Adobe ID이 있어야 하며, 그런 다음 해당 계정을 새 소유자의 이메일 주소로 변경해야 합니다.

1. [Commerce 계정 로그인](https://account.magento.com/customer/account/login/) 페이지로 이동합니다.

1. **[!UICONTROL Sign in with Adobe ID]**&#x200B;을(를) 클릭합니다.

1. **[!UICONTROL Create an account]**&#x200B;을(를) 클릭합니다.

1. 현재 소유자의 이메일 주소와 암호를 입력합니다.

1. **[!UICONTROL Continue]**&#x200B;을(를) 클릭합니다.

   이 단계에서는 Adobe ID을 만들고 현재 Commerce 계정(MAGEID)에 연결합니다. 이 계정 링크를 사용하면 _[!UICONTROL Email]_&#x200B;필드의 변경 내용이 차단됩니다. 연관된 이메일 주소의 구성은 Adobe ID 계정에서 관리됩니다.

1. [account.adobe.com](https://account.adobe.com/)으로 이동합니다.

1. **[!UICONTROL Change Email]**&#x200B;을(를) 클릭합니다.

1. 새 소유자의 이메일 주소를 입력합니다.

   새 이메일 주소가 시스템의 다른 계정에 이미 연결되어 있는 경우 전송에 직접 사용할 수 없습니다. 대신, 변경 작업을 진행하려면 [임시 전자 메일 주소](#change-to-a-temporary-account)를 사용해야 합니다.

1. **[!UICONTROL Change]**&#x200B;을(를) 클릭합니다.

   이 단계에서는 새 이메일 주소로 전송된 확인 이메일을 생성합니다. 이메일에는 이메일 주소 변경을 완료하는 데 필요한 확인 코드가 포함되어 있습니다.

1. 새 이메일 주소로 전송된 확인 코드를 입력합니다.

1. **[!UICONTROL Verify]**&#x200B;을(를) 클릭합니다.

>[!VIDEO](https://video.tv.adobe.com/v/3435325/?learn=on)

## 이메일 변경

>[!IMPORTANT]
>
>[전송 형식](#identify-your-transfer-type)을(를) 검토하고 이 단계 순서에 대한 사전 조건을 충족하는지 확인하십시오.

이 전송 유형으로 인해 현재 계정 소유자가 다른 Adobe 제품에 액세스할 수 없습니다.

1. [account.adobe.com](https://account.adobe.com/)&#x200B;(으)로 이동하여 Adobe 로그인을 완료합니다.

1. 계정 이름 및 아바타에서 **[!UICONTROL Change Email]**&#x200B;을(를) 클릭합니다.

1. 대화 상자에서 새 소유자의 이메일 주소를 입력합니다.

   새 이메일 주소가 시스템의 다른 계정에 이미 연결되어 있는 경우 전송에 직접 사용할 수 없습니다. 대신, 변경 작업을 진행하려면 [임시 전자 메일 주소](#change-to-a-temporary-account)를 사용해야 합니다.

1. **[!UICONTROL Change]**&#x200B;을(를) 클릭합니다.

   이 단계에서는 새 이메일 주소로 전송된 확인 이메일을 생성합니다. 이메일에는 이메일 주소 변경을 완료하는 데 필요한 확인 코드가 포함되어 있습니다.

1. 새 이메일 주소로 전송된 확인 코드를 입력합니다.

1. **[!UICONTROL Verify]**&#x200B;을(를) 클릭합니다.

## Adobe ID 계정 스위치

>[!IMPORTANT]
>
>[전송 형식](#identify-your-transfer-type)을(를) 검토하고 이 단계 순서에 대한 사전 조건을 충족하는지 확인하십시오.

이 전송 유형은 현재 소유자와 새 소유자 모두에 기존 Adobe ID가 있고 두 계정을 모두 유지하려는 경우 임시 이메일 주소를 사용하여 계정 소유권을 전환합니다. 소유권 이전을 완료하려면 Adobe ID과 연결되지 않은 임시 이메일 주소를 사용해야 합니다.

### 임시 계정으로 변경

현재 소유자는 다음 단계를 완료하여 Adobe ID을 다른 임시 이메일 주소와 연결합니다.

1. [account.adobe.com](https://account.adobe.com/)&#x200B;(으)로 이동하여 Adobe 로그인을 완료합니다.

1. 계정 이름 및 아바타에서 **[!UICONTROL Change Email]**&#x200B;을(를) 클릭합니다.

1. 대화 상자에서 Adobe ID에서 사용하지 않는 유효한 임시 이메일 주소를 입력합니다.

>[!NOTE]
>
>확인 코드를 사용하여 이메일을 검색할 수 있으려면 이메일 주소에 대한 액세스 권한이 있어야 합니다.
>
>계정 이메일에 액세스할 수 없는 경우 IT 팀에 요청하여 회사 이메일 시스템에서 계정 이메일 주소에 대한 이메일 전달을 설정합니다. 전자 메일 전달을 구성할 수 없는 경우 새 계정 소유자에게 Adobe ID이 있는지 확인한 다음 [지원 요청을 제출](https://experienceleague.adobe.com/en/docs/commerce-knowledge-base/kb/help-center-guide/magento-help-center-user-guide#support-case)하여 계정 전송을 시작하는 데 필요한 모든 세부 정보를 제공합니다.

1. **[!UICONTROL Change]**&#x200B;을(를) 클릭합니다.

   이 단계에서는 임시 이메일 주소로 전송된 확인 이메일을 생성합니다. 이메일에는 이메일 주소 변경을 완료하는 데 필요한 확인 코드가 포함되어 있습니다.

1. 임시 이메일 주소로 전송된 확인 코드를 입력합니다.

1. **[!UICONTROL Verify]**&#x200B;을(를) 클릭합니다.

1. Adobe 계정에서 로그아웃합니다.

### 새 소유자 단계

현재 소유자가 임시 이메일 주소로 전송을 완료한 후 새 소유자는 다음 단계를 완료하여 현재 소유자의 원래 이메일 주소를 가리키도록 계정 구성을 변경해야 합니다.

1. [account.adobe.com](https://account.adobe.com/)&#x200B;(으)로 이동하여 Adobe 로그인을 완료합니다.

1. 계정 이름 및 아바타에서 **[!UICONTROL Change Email]**&#x200B;을(를) 클릭합니다.

1. 대화 상자에서 현재 소유자의 원래 이메일 주소를 입력합니다.

1. **[!UICONTROL Change]**&#x200B;을(를) 클릭합니다.

   이 단계에서는 현재 소유자의 원래 이메일 주소로 전송된 확인 이메일을 생성합니다. 이메일에는 이메일 주소 변경을 완료하는 데 필요한 확인 코드가 포함되어 있습니다.

1. 현재 소유자의 원래 이메일 주소로 전송된 확인 코드를 입력합니다.

1. **[!UICONTROL Verify]**&#x200B;을(를) 클릭합니다.

1. Adobe 계정에서 로그아웃합니다.

### 후속 단계

새 소유자가 현재 소유자의 원래 이메일 주소로 Adobe 계정을 성공적으로 구성한 후 다음 단계를 완료하여 소유권을 이전합니다.

1. [account.adobe.com](https://account.adobe.com/)&#x200B;(으)로 이동한 다음 [임시 계정](#change-to-a-temporary-account)의 전자 메일 주소를 사용하여 Adobe 로그인을 완료합니다.

1. 계정 이름 및 아바타에서 **[!UICONTROL Change Email]**&#x200B;을(를) 클릭합니다.

1. 대화 상자에서 새 소유자의 이메일 주소를 입력합니다.

1. **[!UICONTROL Change]**&#x200B;을(를) 클릭합니다.

   이 단계에서는 새 소유자의 이메일 주소로 전송된 확인 이메일을 생성합니다. 이메일에는 이메일 주소 변경을 완료하는 데 필요한 확인 코드가 포함되어 있습니다.

1. 새 소유자의 이메일 주소로 전송된 확인 코드를 입력합니다.

1. **[!UICONTROL Verify]**&#x200B;을(를) 클릭합니다.

## 최종 단계

새 소유자가 첫 번째 또는 세 번째 사용 사례의 단계를 완료한 후 새 소유자는 지원 팀에 전자 메일 주소 업데이트에 대해 알리려면 [지원 요청을 제출](https://experienceleague.adobe.com/en/docs/commerce-knowledge-base/kb/help-center-guide/magento-help-center-user-guide?lang=en#support-case)해야 합니다. 그런 다음 지원 팀은 [Commerce Marketplace](https://commercemarketplace.adobe.com/) 프로필의 전자 메일 주소 업데이트와 같은 추가 작업을 완료합니다. 이전 계정 소유자의 이메일 주소를 요청에 포함하십시오.