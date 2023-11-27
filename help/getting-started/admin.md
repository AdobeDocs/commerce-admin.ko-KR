---
title: 관리자란 무엇입니까?
description: 에 대해 알아보기 [!DNL Commerce] 판매자가 제품 및 판촉을 설정하고 주문을 관리하고 기타 관리 작업을 수행하는 위치입니다.
exl-id: 065cf14f-80e7-4695-8922-c761a2191d72
source-git-commit: b657db7e486fec591d5a6239d554376f00707e8c
workflow-type: tm+mt
source-wordcount: '319'
ht-degree: 0%

---

# 관리자란 무엇입니까?

내 스토어 _관리자_ 판매자로서 제품 및 판촉 행사 설정, 주문 관리 및 기타 관리 작업을 수행하는 암호로 보호된 백오피스입니다. 모든 기본 구성 작업 및 저장소 관리 작업은 _관리자_.

추가 보안을 위해 _관리자_ 로그인이 다음을 통해 보호됨: [이중 인증](../systems/security-two-factor-authentication.md)및 을(를) 하나의 [CAPTCHA](../systems/security-captcha.md). 자세한 내용을 보려면 다음 위치로 이동하십시오. [관리자 보안 구성](../systems/security-admin.md).

![관리 사이드바 및 대시보드](./assets/admin-dashboard.png){width="700" zoomable="yes"}

내 이니셜 [로그인](admin-signin.md) Adobe Commerce 또는 Magento Open Source 설치 중에 자격 증명이 설정되었습니다. 암호를 잊어버린 경우 계정과 연결된 이메일 주소로 임시 암호를 보낼 수 있습니다. 보안을 강화하려면 대/소문자를 구분하는 사용자 이름과 강력한 암호가 필요하도록 스토어를 구성합니다.

기본 관리자 계정 외에도 비즈니스에서 만들 수 있는 사용자 수는 다음과 같습니다 [추가 계정](../systems/permissions-users-all.md) 스토어를 관리하고 고객 계정을 지원해야 합니다. 각 계정은 특정 계정과 연결될 수 있습니다. [역할](../systems/permissions-user-roles.md) 비즈니스 기반 액세스 수준 _알아야 할 사항_. 각 관리자 사용자 계정과 연결된 이메일 주소는 고유해야 합니다.

{{ims-admin-note}}

## 사용 데이터 수집

에 처음 로그인할 때 _관리자_, 모든 관리자 사용자에 대한 사용 데이터를 수집할 수 있는 Adobe 권한을 부여하라는 메시지가 표시됩니다. 관리자 사용 데이터 수집을 허용하면 Adobe이 Adobe Commerce 관리자, 관련 제품 및 서비스를 사용하는 경험을 향상시킬 수 있습니다.

![관리자 사용 데이터 수집 허용](./assets/admin-usage-data.png){width="600"}

개별 사용자는 사용 데이터에서 식별되지 않습니다. 내 데이터 수집 설정은 [관리자 사용](../configuration-reference/advanced/admin.md#admin-usage) 구성.

Adobe Commerce의 경우 데이터 수집을 허용하면 _제품 내 지침_: 대화형 컨텐츠를 로 가져오도록 디자인되었습니다. _관리자_. 도움말, 도구 설명, 둘러보기 안내서, 온보딩 정보, 기능 공지 등을 제공합니다.
