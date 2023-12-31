---
title: Adobe ID과의 Commerce Admin Integration 비활성화
description: Adobe IMS와 Adobe Commerce Admin 통합을 비활성화하려면 이 선택적 절차를 따르십시오.
exl-id: 0cd02b23-873e-4e65-ae1f-dbe4f7d0a476
feature: Identity Management
source-git-commit: f84667a7bbc93504499279d77967796bcd11791c
workflow-type: tm+mt
source-wordcount: '313'
ht-degree: 0%

---

# Adobe ID과의 Commerce Admin Integration 비활성화

{{ee-feature}}

상거래 인스턴스를 Adobe IMS 인증 워크플로와 통합한 판매자는 이 선택적 통합을 비활성화해야 할 수 있습니다.

IMS 통합이 비활성화되면 상거래 배포는 기본 상거래 인증 워크플로 및 암호 정책으로 되돌아갑니다. 이 통합이 활성화되거나 비활성화될 때 관리자 사용자 워크플로우만 영향을 받습니다.

다음을 참조하십시오 [관리자 계정](https://experienceleague.adobe.com/docs/commerce-admin/start/admin/admin-signin.html) Commerce 관리자 로그인에 대한 개요입니다.

## 1단계: 통합 비활성화

책임자에서 이 통합을 비활성화할 수 없습니다. Commerce와의 Adobe IMS 통합을 비활성화하고 상거래 인증을 기본 상태로 되돌리려면 명령줄 인터페이스에서 통합을 비활성화해야 합니다.

통합을 비활성화하려면 다음을 수행합니다.

```bash
bin/magento admin:adobe-ims:disable
```

Adobe Commerce은 성공 시 다음 메시지를 표시합니다.

```terminal
Admin Adobe IMS integration is disabled.
```

## 2단계: 상거래 암호 만들기 또는 검색

통합을 비활성화한 후 관리자는 상거래 암호를 사용하여 관리자에 로그인해야 합니다.

* 기존 상거래 암호(즉, IMS 통합 전에 만든 상거래 암호)를 기억하는 상거래 관리자 사용자는 이 암호를 사용하여 관리자에 로그인할 수 있습니다.

* 기존 Commerce 암호가 없거나 잊어버린 Commerce 관리자 사용자는 새 암호를 만들어야 합니다. 새 암호를 만들려면 관리자는 [!UICONTROL Forgot your password?] 새 암호를 만들 수 있는 상거래 로그인 페이지의 기능입니다. 다음을 참조하십시오 [고객 암호 재설정](https://experienceleague.adobe.com/docs/commerce-admin/customers/customer-accounts/configure/password-reset.html). Commerce에서 빈 암호 필드를 허용하지 않습니다.

## 통합을 비활성화한 후

IMS 통합이 비활성화되고 관리자 사용자에게 암호를 입력하라는 메시지가 다시 표시되면 기본 상거래 인증 워크플로가 다시 시작됩니다.

IMS 통합을 비활성화하면 통합이 활성화되었을 때 입력된 자격 증명이 삭제됩니다(`Organization ID`, `Client ID`, 및 `Client Secret` Commerce 구성 파일의 값)입니다.
