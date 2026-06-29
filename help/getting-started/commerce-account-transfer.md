---
title: Adobe Commerce 계정 양도
description: Adobe Commerce 계정을 새 소유자 또는 이메일 주소로 전송하는 방법을 배우고 올바른 전송 유형을 선택하고 이메일 변경 사항을 확인한 다음 지원 팀에 문의하십시오.
exl-id: f6528931-dbf1-4702-8989-232c27969c4a
feature: User Account
TQID: https://experienceleague.adobe.com/CIyzus4f8WcBH-jW9R1nCL-gkl065DLTHbjNn0K6e7E
product_v2: id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2: id: bd989d82-1e15-4534-88db-f1f51dd77ffaid: dac87252-6066-4d6e-a9d2-f6d84c323de7
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: f8a45b24-4be7-4f1b-909b-60d06b483a20
level_v2: id: b5a62a22-46f7-4f0d-b151-3fc640bef588id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2: id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: e01cba363eb149286479718e660f8cdf6526e826
workflow-type: tm+mt
source-wordcount: 1553
ht-degree: 0%

---

# Adobe Commerce 계정 양도

비즈니스 책임이 변경되면 Adobe Commerce 계정을 새 소유자나 다른 이메일 주소로 전송해야 할 수 있습니다. 이 전송을 수행하려면 계정과 연결된 기본 사용자 이메일을 변경해야 합니다.

다음 정보는 MAGEID(Adobe Commerce 계정)를 전송하는 프로세스에 대해 설명합니다. 클라우드 인프라 프로젝트 소유권 또는 [!DNL New Relic] 소유권에 대한 Adobe Commerce 변경은 포함되지 않습니다. 클라우드 프로젝트 액세스에 대한 자세한 내용은 _Commerce on Cloud Infrastructure Guide_&#x200B;에서 [사용자 액세스 관리](https://experienceleague.adobe.com/en/docs/commerce-cloud-service/user-guide/project/user-access)를 참조하십시오.

>[!IMPORTANT]
>
>새 계정 소유자가 공유 액세스를 사용하여 확장을 구매한 경우 계정 전송이 시작되자마자 해당 확장에 대한 액세스가 손실됩니다.
>
>계정 이전을 요청하기 전에 새 소유자가 [사용자의 [!DNL Commerce Marketplace] 계정](https://commercemarketplace.adobe.com/sales/order/history/)에서 구매한 항목에 대한 주문 ID를 검색하고 [[!DNL Commerce Marketplace] 팀](https://experienceleague.adobe.com/en/docs/commerce-knowledge-base/kb/help-center-guide/magento-help-center-user-guide#support-case)에 환불을 요청하는지 확인하십시오. 확장 구매는 다른 계정으로 이전할 수 없습니다.

## 전송 유형 식별

적절한 Adobe Commerce 계정 전송 프로세스는 현재 소유자 및 새 소유자의 계정 상태와 현재 소유자의 이메일 주소에 계속 액세스할 수 있는지 여부에 따라 다릅니다. 예를 들어 현재 소유자가 회사를 떠난 경우 해당 주소로 전송된 이메일에 계속 액세스해야 할 수 있습니다.

다음 시나리오에서는 이러한 조건을 기반으로 사용 가능한 전송 옵션에 대해 설명합니다.

| 전송 유형 | 현재 소유자 | 새 소유자 |
| ------------- | ------------- | --------- |
| [새 Adobe ID 및 전자 메일 변경](#new-adobe-id-and-email-change) | Adobe ID에 연결되지 않은 MAGEID가 있음 | 에는 MAGEID가 없으며 Adobe ID도 없습니다. |
| [전자 메일 변경만](#email-change) | Adobe ID에 연결된 MAGEID가 있습니다. | 에는 Adobe ID이 있지만 계정에 연결된 MAGEID는 없습니다. |
| [Adobe ID 계정 스위치](#adobe-id-account-switch) | Adobe ID에 연결된 MAGEID가 있습니다. | MAGEID가 있고 Adobe ID에 연결되어 있습니다. |

{style="table-layout:auto"}

>[!NOTE]
>
>Adobe Commerce이 다른 Adobe 솔루션과 계속 통합됨에 따라 이제 Adobe Commerce 계정(MAGEID)에는 Adobe ID과의 연결이 필요합니다. Adobe ID은 [Adobe Commerce 계정](https://experienceleague.adobe.com/en/docs/commerce-admin/start/commerce-account/commerce-account-create?lang=en#create-a-commerce-account)에 연결된 것과 동일한 전자 메일 주소를 사용합니다.

## Adobe ID 이메일 변경 사항 확인

여러 전송 경로가 [account.adobe.com](https://account.adobe.com/)에서 동일한 확인 워크플로를 사용합니다. 대상 전자 메일 주소를 입력하고 **[!UICONTROL Change]**&#x200B;을(를) 클릭한 후 다음 단계를 완료하십시오.

1. 입력한 주소로 전송된 확인 이메일을 열고 확인 코드를 찾습니다.

1. 확인 코드를 입력합니다.

1. **[!UICONTROL Verify]**&#x200B;을(를) 클릭합니다.

## 새로운 Adobe ID 및 이메일 변경

>[!IMPORTANT]
>
>[전송 형식](#identify-your-transfer-type)을(를) 검토하고 이 경로가 현재 상황과 일치하는지 확인하십시오.
>
>- 현재 주인은 아직 회사에 있습니다.
>- 현재 소유자에게 Adobe ID이 없거나 [Adobe Commerce 계정(MAGEID)](https://experienceleague.adobe.com/en/docs/commerce-admin/start/commerce-account/commerce-account-create?lang=en#create-a-commerce-account)에 연결되어 있지 않은 Adobe ID이 있습니다.
>- 새 소유자에게는 Adobe ID이 없으며 Adobe Commerce 계정이 없습니다.

현재 소유자에게 아직 Adobe ID에 연결되지 않은 MAGEID가 있는 경우 이 경로를 사용합니다. 현재 소유자는 먼저 Adobe ID을 만들고 연결한 다음 해당 Adobe ID 이메일 주소를 새 소유자의 이메일 주소로 변경합니다.

1. [Adobe Commerce 계정 로그인](https://account.magento.com/customer/account/login/) 페이지로 이동합니다.

1. **[!UICONTROL Sign in with Adobe ID]**&#x200B;을(를) 클릭합니다.

1. **[!UICONTROL Create an account]**&#x200B;을(를) 클릭합니다.

1. 현재 소유자의 이메일 주소와 암호를 입력합니다.

1. **[!UICONTROL Continue]**&#x200B;을(를) 클릭합니다.

   이 단계에서는 Adobe ID을 만들고 현재 Adobe Commerce 계정(MAGEID)에 연결합니다. 이 계정 링크를 사용하면 _[!UICONTROL Email]_필드의 변경 내용이 차단됩니다. 연관된 이메일 주소의 구성은 Adobe ID 계정에서 관리됩니다.

1. [account.adobe.com](https://account.adobe.com/)으로 이동합니다.

1. **[!UICONTROL Change Email]**&#x200B;을(를) 클릭합니다.

1. 새 소유자의 이메일 주소를 입력합니다.

   새 이메일 주소가 시스템의 다른 계정에 이미 연결되어 있는 경우 전송에 직접 사용할 수 없습니다. 대신 [Adobe ID 계정 스위치](#adobe-id-account-switch) 경로에 따라 [임시 전자 메일 주소](#change-to-a-temporary-account)를 사용하십시오.

1. [전자 메일 확인 단계](#verify-an-adobe-id-email-change)를 완료합니다.

새 소유자가 전자 메일 주소를 확인한 후 [마지막 단계](#final-steps)를 계속하면 Adobe Commerce 지원에서 [[!DNL Commerce Marketplace]](https://commercemarketplace.adobe.com/) 프로필과 같은 계정 레코드를 업데이트할 수 있습니다.

>[!VIDEO](https://video.tv.adobe.com/v/3435325/?learn=on){transcript=true}

## 이메일 변경만 {#email-change}

>[!IMPORTANT]
>
>[전송 형식](#identify-your-transfer-type)을(를) 검토하고 이 경로가 현재 상황과 일치하는지 확인하십시오.
>
>- 현재 주인은 아직 회사에 있습니다.
>- 현재 소유자에게 [MAGEID(Adobe Commerce 계정)](https://experienceleague.adobe.com/en/docs/commerce-admin/start/commerce-account/commerce-account-create?lang=en#create-a-commerce-account)에 연결된 Adobe ID이 있습니다.
>- 새 소유자에게 Adobe Commerce 계정에 연결되지 않은 Adobe ID이 있습니다.

시작하기 전에, 이 전송 유형은 현재 계정 소유자가 해당 Adobe ID에 연결된 다른 Adobe 제품에 대한 액세스 권한을 상실하는 결과를 초래합니다.

1. [account.adobe.com](https://account.adobe.com/)&#x200B;(으)로 이동하여 Adobe 로그인을 완료합니다.

1. 계정 이름 및 아바타에서 **[!UICONTROL Change Email]**&#x200B;을(를) 클릭합니다.

1. 대화 상자에서 새 소유자의 이메일 주소를 입력합니다.

   새 이메일 주소가 시스템의 다른 계정에 이미 연결되어 있는 경우 전송에 직접 사용할 수 없습니다. 대신 [Adobe ID 계정 스위치](#adobe-id-account-switch) 경로에 따라 [임시 전자 메일 주소](#change-to-a-temporary-account)를 사용하십시오.

1. [전자 메일 확인 단계](#verify-an-adobe-id-email-change)를 완료합니다.

새 소유자가 전자 메일 주소를 확인한 후 [마지막 단계](#final-steps)를 계속하면 Adobe Commerce 지원에서 [[!DNL Commerce Marketplace]](https://commercemarketplace.adobe.com/) 프로필과 같은 계정 레코드를 업데이트할 수 있습니다.

## Adobe ID 계정 스위치

>[!IMPORTANT]
>
>[전송 형식](#identify-your-transfer-type)을(를) 검토하고 이 경로가 현재 상황과 일치하는지 확인하십시오.
>
>- 현재 소유자는 더 이상 회사에 속하지 않지만 현재 소유자의 회사 이메일 주소로 전송된 이메일은 계속 액세스할 수 있습니다. 또는 IT 팀이 이러한 이메일을 인증된 담당자에게 전달할 수 있습니다.
>- 현재 소유자에게 [MAGEID(Adobe Commerce 계정)](https://experienceleague.adobe.com/en/docs/commerce-admin/start/commerce-account/commerce-account-create?lang=en#create-a-commerce-account)에 연결된 Adobe ID이 있습니다.
>- 새 소유자에게는 Adobe Commerce 계정과 연결된 Adobe ID이 있습니다.

이 전송 유형은 현재 소유자와 새 소유자 모두에 기존 Adobe ID가 있고 두 Adobe ID를 모두 보유하려는 경우 임시 이메일 주소를 사용하여 계정 소유권을 전환합니다. 소유권 이전을 완료하려면 Adobe ID과 연결되지 않은 임시 이메일 주소를 사용해야 합니다.

### 임시 계정으로 변경

다음 단계를 완료하여 현재 소유자의 Adobe ID을 임시 이메일 주소와 연결합니다. 확인 코드를 검색할 수 있으려면 해당 이메일 주소에 대한 액세스 권한이 있어야 합니다.

>[!NOTE]
>
>현재 소유자의 이메일에 액세스할 수 없는 경우 IT 팀에 요청하여 회사 이메일 시스템에서 계정 이메일 주소에 대한 이메일 전달을 설정합니다. 전자 메일 전달을 구성할 수 없는 경우 새 계정 소유자에게 Adobe ID이 있는지 확인한 다음 계정 전송을 시작하는 데 필요한 모든 세부 정보를 포함하여 [지원 요청을 제출](https://experienceleague.adobe.com/en/docs/commerce-knowledge-base/kb/help-center-guide/magento-help-center-user-guide#support-case)하십시오.

1. [account.adobe.com](https://account.adobe.com/)&#x200B;(으)로 이동하여 Adobe 로그인을 완료합니다.

1. 계정 이름 및 아바타에서 **[!UICONTROL Change Email]**&#x200B;을(를) 클릭합니다.

1. 대화 상자에서 Adobe ID에서 사용하지 않는 유효한 임시 이메일 주소를 입력합니다.

1. [전자 메일 확인 단계](#verify-an-adobe-id-email-change)를 완료합니다.

1. Adobe 계정에서 로그아웃합니다.

### 새 소유자 단계

현재 소유자가 임시 이메일 주소로 전송을 완료한 후 새 소유자는 다음 단계를 완료하여 Adobe ID 이메일 주소를 현재 소유자의 원래 이메일 주소로 변경해야 합니다.

1. [account.adobe.com](https://account.adobe.com/)&#x200B;(으)로 이동하여 Adobe 로그인을 완료합니다.

1. 계정 이름 및 아바타에서 **[!UICONTROL Change Email]**&#x200B;을(를) 클릭합니다.

1. 대화 상자에서 현재 소유자의 원래 이메일 주소를 입력합니다.

1. [전자 메일 확인 단계](#verify-an-adobe-id-email-change)를 완료합니다.

1. Adobe 계정에서 로그아웃합니다.

### 후속 단계

새 소유자가 현재 소유자의 원래 이메일 주소로 Adobe ID을 성공적으로 구성한 후 다음 단계를 완료하여 해당 이메일 주소를 새 소유자에게 할당합니다.

1. [account.adobe.com](https://account.adobe.com/)&#x200B;(으)로 이동한 다음 [임시 계정](#change-to-a-temporary-account)의 전자 메일 주소를 사용하여 Adobe 로그인을 완료합니다.

1. 계정 이름 및 아바타에서 **[!UICONTROL Change Email]**&#x200B;을(를) 클릭합니다.

1. 대화 상자에서 새 소유자의 이메일 주소를 입력합니다.

1. [전자 메일 확인 단계](#verify-an-adobe-id-email-change)를 완료합니다.

새 소유자가 전자 메일 주소를 확인한 후 [마지막 단계](#final-steps)를 계속하면 Adobe Commerce 지원에서 [[!DNL Commerce Marketplace]](https://commercemarketplace.adobe.com/) 프로필과 같은 계정 레코드를 업데이트할 수 있습니다.

## 최종 단계

[새 Adobe ID 및 전자 메일 변경](#new-adobe-id-and-email-change), [전자 메일 변경만](#email-change) 또는 [Adobe ID 계정 전환](#adobe-id-account-switch) 프로세스를 완료한 후 다음 단계를 완료하십시오.

1. 새 소유자로 [지원 요청을 제출](https://experienceleague.adobe.com/en/docs/commerce-knowledge-base/kb/help-center-guide/magento-help-center-user-guide?lang=en#support-case)합니다.

   다음 세부 정보를 포함합니다.

   - 이전 계정 소유자의 이메일 주소
   - 새 소유자의 이메일 주소
   - Adobe Commerce 계정 이전을 완료하고 Adobe ID 이메일 주소를 업데이트했다는 참고 사항

1. Adobe Commerce 지원에서 업데이트를 확인할 때까지 기다립니다.

   또한 [[!DNL Commerce Marketplace]](https://commercemarketplace.adobe.com/) 프로필의 전자 메일 주소와 같은 관련 레코드도 업데이트합니다.

지원이 요청을 완료하면 새 소유자는 Adobe ID으로 Adobe Commerce 계정에 로그인할 수 있습니다. MAGEID는 계정에 대한 권한 식별자로 유지됩니다.
