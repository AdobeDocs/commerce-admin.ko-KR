---
title: Commerce 계정 양도
description: Commerce 계정을 다른 소유자 또는 이메일 주소로 전송하는 방법을 알아봅니다.
exl-id: f6528931-dbf1-4702-8989-232c27969c4a
feature: User Account
source-git-commit: 59a88468dabfd1042b664f658225de2504b66b1b
workflow-type: tm+mt
source-wordcount: '986'
ht-degree: 0%

---

# Commerce 계정 양도

비즈니스 책임이 변경되면 기존 Commerce 계정의 소유권을 새 담당자 또는 다른 이메일 주소로 이전해야 할 수 있습니다. 이 전송을 수행하려면 계정과 연결된 기본 사용자 이메일을 변경해야 합니다.

다음 정보는 MAGEID(Commerce) 계정을 전송하는 프로세스를 설명합니다. 클라우드 계정(클라우드 프로젝트 또는 New Relic) 소유권에 대한 변경 사항은 포함되지 않습니다. 클라우드 프로젝트 액세스에 대한 자세한 내용은 [사용자 액세스 관리](https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/project/user-access.html) 다음에서 _Commerce on Cloud Infrastructure 안내서_.

## 전송 유형 식별

이 전송을 완료하는 방법은 다음 시나리오 중 계정을 현재 소유자로 설명하고 계정을 전송할 새 소유자(이메일 주소)로 사용자 상황을 설명하는 시나리오에 따라 다릅니다.

| 전송 유형 | 현재 소유자 | 새 소유자 |
| ------------- | ------------- | --------- |
| [새로운 Adobe ID 및 이메일 변경](#new-adobe-id-and-email-change) | 에 다음과 같은 MAGEID가 있습니다. **_연결되지 않음_** (Adobe 로그인 계정 포함) | MAGEID가 없으며 Adobe 로그인 계정에 연결되어 있지 않습니다. |
| [이메일 변경](#email-change) | 에 다음과 같은 MAGEID가 있습니다. **_연결됨_** 연결된 다른 Adobe 제품/서비스가 없는 Adobe 로그인 계정으로. | MAGEID가 없으며 Adobe 로그인 계정에 연결되어 있지 않습니다. |
| [Adobe ID 스위치](#adobe-id-account-switch) | 에 다음과 같은 MAGEID가 있습니다. **_연결됨_** 연결된 다른 Adobe 제품/서비스가 없는 Adobe 로그인 계정으로. | 에는 MAGEID가 있으며 연결된 다른 Adobe 제품/서비스가 없는 Adobe 로그인 계정에 연결되어 있습니다. |

{style="table-layout:auto"}

>[!NOTE]
>
>Adobe Commerce이 다른 Adobe 솔루션과 계속 통합됨에 따라 이제 Commerce 계정(MAGEID)에 Adobe 로그인이 필요합니다. 이 Adobe ID은 Commerce 계정에 연결된 것과 동일한 이메일 주소를 사용합니다.

>[!NOTE]
>
>현재 또는 새 소유자에게 다른 Adobe 제품/서비스와 연결된 Adobe 로그인 계정이 있는 경우 [지원 티켓](https://experienceleague.adobe.com/docs/commerce-knowledge-base/kb/help-center-guide/magento-help-center-user-guide.html#submit-ticket) Commerce 계정을 다른 Adobe ID으로 전송하는 데 도움이 됩니다.

## 새로운 Adobe ID 및 이메일 변경

>[!IMPORTANT]
>
>리뷰 [전송 유형](#identify-your-transfer-type) 그리고 이 일련의 단계에 대한 전제 조건을 충족하는지 확인하십시오.

이 전송 유형을 사용하려면 먼저 연결된 Adobe ID을 만든 다음 해당 계정을 새 소유자의 이메일 주소로 변경해야 합니다.

1. 다음으로 이동 [Commerce 계정](https://account.magento.com/customer/account/login/).

1. 클릭 **[!UICONTROL Sign in with Adobe ID]**.

1. 클릭 **[!UICONTROL Create an account]**.

1. 현재 소유자의 이메일 주소와 암호를 입력합니다.

1. 클릭 **[!UICONTROL Continue]**.

   이렇게 하면 Adobe ID이 만들어지고 현재 Commerce 계정(MAGEID)에 연결됩니다. 이 계정 링크를 사용하면 _[!UICONTROL Email]_필드는 모든 변경에서 차단됩니다. 연관된 이메일 주소는 Adobe ID 계정에서 관리합니다.

1. 다음으로 이동 [account.adobe.com](https://account.adobe.com/).

1. 클릭 **[!UICONTROL Change Email]**.

1. 새 소유자의 이메일 주소를 입력합니다.

1. 클릭 **[!UICONTROL Change]**.

   이렇게 하면 새 이메일 주소로 전송되는 확인 이메일이 생성됩니다. 이메일에는 이메일 주소 변경을 완료하는 데 필요한 확인 코드가 포함되어 있습니다.

1. 새 이메일 주소로 전송된 확인 코드를 입력합니다.

1. 클릭 **[!UICONTROL Verify]**.

## 이메일 변경

>[!IMPORTANT]
>
>리뷰 [전송 유형](#identify-your-transfer-type) 그리고 이 일련의 단계에 대한 전제 조건을 충족하는지 확인하십시오.

1. 다음으로 이동 [account.adobe.com](https://account.adobe.com/) Adobe 로그인을 완료합니다.

1. 계정 이름 및 아바타에서 **[!UICONTROL Change Email]**.

1. 대화 상자에서 새 소유자의 이메일 주소를 입력합니다.

1. 클릭 **[!UICONTROL Change]**.

   이렇게 하면 새 이메일 주소로 전송되는 확인 이메일이 생성됩니다. 이메일에는 이메일 주소 변경을 완료하는 데 필요한 확인 코드가 포함되어 있습니다.

1. 새 이메일 주소로 전송된 확인 코드를 입력합니다.

1. 클릭 **[!UICONTROL Verify]**.

## Adobe ID 계정 스위치

>[!IMPORTANT]
>
>리뷰 [전송 유형](#identify-your-transfer-type) 그리고 이 일련의 단계에 대한 전제 조건을 충족하는지 확인하십시오.

현재 소유자와 새 소유자가 기존 Adobe ID를 가지고 있는 경우 두 계정을 모두 유지해야 하지만 이메일 주소를 전환해야 합니다. 이를 위해 를 사용해야 합니다. _임시_ 유효하지만 및 Adobe ID과 연결되지 않은 이메일 주소.

### 임시 계정으로 변경

현재 소유자는 다음 단계를 완료하여 Adobe ID을 다른 임시 이메일 주소와 연결합니다.

1. 다음으로 이동 [account.adobe.com](https://account.adobe.com/) Adobe 로그인을 완료합니다.

1. 계정 이름 및 아바타에서 **[!UICONTROL Change Email]**.

1. 대화 상자에서 Adobe ID에서 사용하지 않는 유효한 임시 이메일 주소를 입력합니다.

   확인 코드를 사용하여 이메일을 검색할 수 있으려면 이메일 주소에 대한 액세스 권한이 있어야 합니다.

1. 클릭 **[!UICONTROL Change]**.

   이렇게 하면 임시 이메일 주소로 전송되는 확인 이메일이 생성됩니다. 이메일에는 이메일 주소 변경을 완료하는 데 필요한 확인 코드가 포함되어 있습니다.

1. 임시 이메일 주소로 전송된 확인 코드를 입력합니다.

1. 클릭 **[!UICONTROL Verify]**.

1. Adobe 계정에서 로그아웃합니다.

### 새 소유자 단계

현재 소유자가 임시 이메일 주소로 전송을 완료한 후 다음 단계를 완료하여 계정을 현재 소유자로 변경합니다.

1. 다음으로 이동 [account.adobe.com](https://account.adobe.com/) Adobe 로그인을 완료합니다.

1. 계정 이름 및 아바타에서 **[!UICONTROL Change Email]**.

1. 대화 상자에서 현재 소유자의 원래 이메일 주소를 입력합니다.

1. 클릭 **[!UICONTROL Change]**.

   그러면 해당 이메일 주소로 전송되는 확인 이메일이 생성됩니다. 이메일에는 이메일 주소 변경을 완료하는 데 필요한 확인 코드가 포함되어 있습니다.

1. 현재 소유자에게 전송된 확인 코드를 입력합니다.

1. 클릭 **[!UICONTROL Verify]**.

1. Adobe 계정에서 로그아웃합니다.

### 후속 단계

새 소유자가 Adobe 계정을 현재(현재 이전) 소유자에게 성공적으로 전송한 후 다음 단계를 완료하여 소유권을 이전합니다.

1. 다음으로 이동 [account.adobe.com](https://account.adobe.com/) (일련의 단계에서 사용되는 첫 번째 계정) 및 Adobe 로그인을 완료합니다.

   이 로그인을 사용하려면 임시 이메일 주소를 사용해야 합니다.

1. 계정 이름 및 아바타에서 **[!UICONTROL Change Email]**.

1. 대화 상자에서 새 소유자의 이메일 주소를 입력합니다.

1. 클릭 **[!UICONTROL Change]**.

   그러면 해당 이메일 주소로 전송되는 확인 이메일이 생성됩니다. 이메일에는 이메일 주소 변경을 완료하는 데 필요한 확인 코드가 포함되어 있습니다.

1. 새 소유자에게 전송된 확인 코드를 입력합니다.

1. 클릭 **[!UICONTROL Verify]**.

1. **지원 요청 제출** 계정 소유자의 이메일 주소를 업데이트했음을 지원 팀에 알리십시오.

의 이메일 주소를 업데이트하는 등 지원에서 수행해야 하는 추가 단계가 있습니다. [Commerce Marketplace](https://commercemarketplace.adobe.com/) 프로필.
