---
title: 고객 암호 재설정
description: 고객은 일반적으로 상점에서 암호를 재설정하지만 상점 관리자는 암호 재설정 또는 관리자의 강제 로그인을 시작할 수 있습니다.
exl-id: bca1ef3e-2bc6-4146-ac86-d6c58c8995e4
feature: Customers, Configuration, Security
source-git-commit: 7de285d4cd1e25ec890f1efff9ea7bdf2f0a9144
workflow-type: tm+mt
source-wordcount: '386'
ht-degree: 0%

---

# 고객 암호 재설정

고객은 일반적으로 를 클릭하여 상점에서 암호를 재설정합니다. _[!UICONTROL Forgot Your Password?]_. 그러나 저장소 관리자는 관리자의 암호 재설정 또는 강제 로그인을 시작할 수 있습니다.

| 함수 | 설명 |
| --- | --- |
| 암호 재설정 | 암호 재설정 이메일은 고객의 이메일 계정으로 직접 전송됩니다. 스토어 관리자가 고객 암호에 액세스할 수 없습니다. |
| 강제 로그인 | 고객 계정과 연결된 OAuth 액세스 토큰을 취소합니다. 웹 API의 일부로 OAuth 토큰이 할당된 고객 계정에서만 사용할 수 있습니다 [통합](../systems/integrations.md). 자세한 내용은 다음을 참조하십시오. [OAuth 기반 인증](https://developer.adobe.com/commerce/webapi/get-started/authentication/gs-authentication-oauth/) 개발자 설명서에서 참조하십시오. <br/><br/>상점 또는 관리자로부터 생성된 표준 고객 계정에는 OAuth 토큰이 없습니다. |

{style="table-layout:auto"}

## 상점 첫 화면에서 암호 재설정

1. 로그인 페이지에서 고객이 클릭 **[!UICONTROL Forgot Your Password?]**.

1. 메시지가 표시되면 를 입력합니다. **[!UICONTROL Email Address]** 계정 및 클릭과 연결된 계정 **[!UICONTROL Reset My Password]**.

   ![암호를 잊으셨습니까?](assets/forgot-password.png){width="600" zoomable="yes"}

   >[!INFO]
   >
   >입력한 이메일 주소가 계정과 연결된 이메일 주소와 일치하는 경우 고객은 암호를 재설정할 수 있는 링크가 있는 암호 재설정 확인 이메일을 수신합니다.

1. 이메일이 도착하면 고객이 _암호 재설정_ 링크 및 입력 **[!UICONTROL New Password]** 메시지가 표시되면

1. 다시 입력하여 확인하고 클릭합니다. **[!UICONTROL Reset Password]**.

   >[!IMPORTANT]
   >
   >새 암호 길이는 공백 없이 6자 이상이어야 합니다. 암호가 업데이트되었다는 확인을 받으면 새 암호를 사용하여 계정에 로그인할 수 있습니다. 기본적으로 _암호 재설정_ 링크는 24시간 동안 유효합니다.

## 관리자의 암호 재설정

1. 다음에서 _관리자_ 사이드바, 이동 **[!UICONTROL Customers]** > **[!UICONTROL All Customers]**.

1. 표에서 고객 계정을 찾은 다음 를 클릭합니다. **[!UICONTROL Edit]** 다음에서 _작업_ 열.

1. 페이지 상단의 옵션 세트에서 **[!UICONTROL Reset Password]**.

   한 시간 내에 허용되는 암호 재설정 요청 수는 [구성](../configuration-reference/customers/customer-configuration.md) 주제.

## 고객의 OAuth 토큰 취소

>[!IMPORTANT]
>
>API 인증을 완전히 이해하지 못한 경우 계속 진행하지 마십시오.

1. 다음에서 _관리자_ 사이드바, 이동 **[!UICONTROL Customers]** > **[!UICONTROL All Customers]**.

1. 표에서 고객 계정을 찾은 다음 를 클릭합니다. **[!UICONTROL Edit]** 다음에서 _작업_ 열.

1. 페이지 상단의 옵션 세트에서 **[!UICONTROL Force Sign In]**.

1. 확인을 묻는 메시지가 나타나면 **확인**.
