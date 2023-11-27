---
title: 고객 로그인
description: 상점에서의 고객 로그인 기능을 통해 고객 계정에 쉽게 액세스할 수 있습니다.
exl-id: eadcc15a-a052-4213-a818-d5b248d974d2
feature: Customers, Storefront
source-git-commit: 7de285d4cd1e25ec890f1efff9ea7bdf2f0a9144
workflow-type: tm+mt
source-wordcount: '381'
ht-degree: 0%

---

# 고객 로그인

고객은 스토어의 모든 페이지에서 계정에 쉽게 액세스할 수 있습니다. 에 따라 [구성](../customers/account-options-new.md), 고객은 계정 대시보드로 리디렉션되거나 계정에 로그인한 후 쇼핑을 계속할 수 있습니다.

If [CAPTCHA](../systems/security-captcha.md) 가 구성에서 활성화되어 있으므로, 사용자는 계정에 액세스하기 전에 자신이 사람인지 확인하는 테스트를 올바르게 완료해야 합니다.

고객이 암호를 잊어버리면 계정과 연결된 이메일 주소로 재설정 링크가 전송됩니다. 다음 [암호 옵션](../customers/password-options.md) 구성은 로그인 시도에 대한 고객 경험을 제어합니다.

- 고객이 암호를 입력할 수 있는 횟수
- 시도 간격(분)
- 계정이 잠기기 전 총 시도 횟수
- 잠금 기간

![storefront 헤더의 로그인 링크](assets/storefront-sign-in-create-account.png){width="700" zoomable="yes"}

## 고객 계정에 로그인

1. 스토어 헤더에서 고객이 클릭 **[!UICONTROL Sign in]**.

   ![고객 로그인](assets/login.png){width="700" zoomable="yes"}

1. 입력 **[!UICONTROL Email]** 주소 및 **[!UICONTROL Password]**.

1. 클릭수 **[!UICONTROL Sign in]**.

   >[!IMPORTANT]
   >
   >암호를 기억할 수 없는 경우 고객은 **[!UICONTROL Forgot Your Password?]** 다음 [지침](../customers/password-reset.md) 암호를 재설정합니다.

## 고객 로그인 후 계정 대시보드로 리디렉션을 설정합니다.

고객이 로그인하거나 쇼핑을 계속할 수 있도록 스토어를 구성하여 계정 대시보드로 리디렉션할 수 있습니다.

1. 다음에서 _관리자_ 사이드바, 이동 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. 왼쪽 패널에서 를 확장합니다. **[!UICONTROL Customers]** 및 선택 **[!UICONTROL Customer Configuration]**.

1. 확장 **[!UICONTROL Login Options]** 섹션.

1. 설정 **[!UICONTROL Redirect Customer to Account Dashboard after Logging in]** 다음 중 하나를 수행합니다.

   - `Yes` - 계정 대시보드는 고객이 계정에 로그인할 때 표시됩니다.
   - `No` - 고객은 계정에 로그인한 후 계속 쇼핑을 할 수 있습니다.

1. 완료되면 다음을 클릭하십시오. **[!UICONTROL Save Config]**.

## Amazon으로 로그인

가 구성된 저장소의 경우 [!DNL Amazon Pay] 및 [!DNL Login with Amazon] 통합하면 고객이 Amazon 구매자 계정에 로그인할 수 있습니다.

1. 스토어 헤더에서 고객이 클릭 **[!UICONTROL Sign in]**.

1. 클릭수 **[!UICONTROL Login with Amazon]**.

   ![Amazon으로 로그인](assets/amazon-pay.png){width="700" zoomable="yes"}

1. 로그인하라는 메시지가 표시되면 고객이 **[!UICONTROL email address]** 및 **[!UICONTROL password]** Amazon 구매자 계정.

   ![Amazon 자격 증명 입력](assets/amazon-popup1.png){width="700" zoomable="yes"}

1. 구매를 처리할 때 Amazon에 해당 계정의 다음 정보를 스토어와 공유할 수 있는 권한을 부여하려면 을 클릭합니다 **확인**.

   - 이름
   - 이메일 주소
   - 배송 주소

   ![데이터 공유 권한 부여](assets/amazon-popup2.png){width="700" zoomable="yes"}

## 고객 계정에서 로그아웃

1. 오른쪽 위 모서리 옆  _[!UICONTROL Welcome, Customer Name!]_, 고객이 클릭&#x200B;**[!UICONTROL v]**메뉴 선택기.

1. 선택 **[!UICONTROL Sign Out]**.

로그아웃 후 고객은 홈페이지로 리디렉션됩니다.
