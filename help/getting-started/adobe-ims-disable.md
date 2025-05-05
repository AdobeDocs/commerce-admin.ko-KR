---
title: Adobe ID과 Commerce Admin Integration 비활성화
description: Adobe IMS와 Adobe Commerce Admin 통합을 비활성화하려면 이 선택적 절차를 따르십시오.
exl-id: 0cd02b23-873e-4e65-ae1f-dbe4f7d0a476
feature: Identity Management
source-git-commit: 53c3b6c9fa9c152e6619528a43580b0acc71a2a5
workflow-type: tm+mt
source-wordcount: '302'
ht-degree: 0%

---

# Adobe ID과 Commerce Admin Integration 비활성화

{{ee-feature}}

Commerce 인스턴스를 Adobe IMS 인증 워크플로와 통합한 판매자는 이 선택적 통합을 비활성화해야 할 수 있습니다.

IMS 통합이 비활성화된 후 Commerce 배포는 기본 Commerce 인증 워크플로 및 암호 정책으로 되돌아갑니다. 이 통합이 활성화되거나 비활성화될 때 관리자 사용자 워크플로우만 영향을 받습니다.

Commerce 관리자 로그인에 대한 개요는 [관리자 계정](https://experienceleague.adobe.com/docs/commerce-admin/start/admin/admin-signin.html?lang=ko)을 참조하세요.

## 1단계: 통합 비활성화

책임자에서 이 통합을 비활성화할 수 없습니다. Commerce과의 Adobe IMS 통합을 비활성화하고 Commerce 인증을 기본 상태로 되돌리려면 명령줄 인터페이스에서 통합을 비활성화해야 합니다.

통합을 비활성화하려면 다음을 수행합니다.

```bash
bin/magento admin:adobe-ims:disable
```

Adobe Commerce은 성공 시 다음 메시지를 표시합니다.

```
Admin Adobe IMS integration is disabled.
```

## 2단계: Commerce 암호 만들기 또는 검색

통합을 비활성화한 후 관리자는 Commerce 암호를 사용하여 관리자에 로그인해야 합니다.

* 기존 Commerce 암호(즉, IMS 통합 전에 만든 Commerce 암호)를 기억하는 Commerce 관리자 사용자는 이 암호를 사용하여 관리자에 로그인할 수 있습니다.

* 기존 Commerce 암호가 없거나 Commerce 암호를 잊어버린 관리자 사용자는 새 암호를 만들어야 합니다. 새 암호를 만들려면 관리자는 Commerce 로그인 페이지에서 [!UICONTROL Forgot your password?] 기능을 사용하여 새 암호를 만들 수 있습니다. [고객 암호 재설정](https://experienceleague.adobe.com/docs/commerce-admin/customers/customer-accounts/configure/password-reset.html?lang=ko)을 참조하세요. Commerce은 빈 암호 필드를 허용하지 않습니다.

## 통합을 비활성화한 후

IMS 통합이 비활성화되고 관리자 사용자에게 암호를 입력하라는 메시지가 다시 표시되면 기본 Commerce 인증 워크플로가 다시 시작됩니다.

IMS 통합을 사용하지 않도록 설정하면 Commerce 구성 파일에서 통합이 사용되도록 설정될 때 입력한 자격 증명(`Organization ID`, `Client ID` 및 `Client Secret` 값)이 삭제됩니다.
