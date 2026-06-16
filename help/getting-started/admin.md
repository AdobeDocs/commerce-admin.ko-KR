---
title: 관리자란 무엇입니까?
description: 판매자가 제품 및 프로모션을 설정하고 주문을 관리하며 기타 관리 작업을 수행하는 장소인  [!DNL Commerce] 관리자에 대해 알아봅니다.
exl-id: 065cf14f-80e7-4695-8922-c761a2191d72
TQID: https://experienceleague.adobe.com/A0DuYohA907-EHXQ6fyy2Sz83Y6cFZ7PDY5SmtBa14Y
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2:
  - id: ba9e5be9-7de1-4f71-a5d2-baead0e425ee
  - id: bd989d82-1e15-4534-88db-f1f51dd77ffa
  - id: c1256247-af4b-46d8-9dca-0c654ecfa157
  - id: dac87252-6066-4d6e-a9d2-f6d84c323de7
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: f8a45b24-4be7-4f1b-909b-60d06b483a20
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2:
  - id: cc72dcf1-72e1-48cc-b434-e7c27d62d67c
  - id: d095671a-1355-40aa-8b5f-06c33c68080b
  - id: d3cdead0-685a-4489-9250-4bb709942f66
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 324
ht-degree: 0%

---

# 관리자란 무엇입니까?

상인으로서 제품 및 프로모션을 설정하고, 주문을 관리하고, 기타 관리 작업을 수행하는 비밀번호로 보호된 백오피스입니다. __&#x200B;모든 기본 구성 작업과 저장소 관리 작업은 _관리자_&#x200B;에서 수행됩니다.

추가 보안을 위해 _관리자_ 로그인은 [이중 인증](../systems/security-two-factor-authentication.md)으로 보호되며 [CAPTCHA](../systems/security-captcha.md)가 필요하도록 구성할 수 있습니다. 자세한 내용을 보려면 [관리자 보안 구성](../systems/security-admin.md)(으)로 이동하십시오.

![관리 사이드바 및 대시보드](./assets/admin-dashboard.png){width="700" zoomable="yes"}

초기 [로그인](admin-signin.md) 자격 증명이 Adobe Commerce 또는 Magento Open Source 설치 중에 설정되었습니다. 암호를 잊어버린 경우 계정과 연결된 이메일 주소로 임시 암호를 보낼 수 있습니다. 보안을 강화하려면 대/소문자를 구분하는 사용자 이름과 강력한 암호가 필요하도록 스토어를 구성합니다.

기본 관리자 계정 외에, 귀사에서 스토어를 관리하고 고객 계정을 지원하는 데 필요한 [추가 계정](../systems/permissions-users-all.md)을 만들 수 있습니다. 비즈니스 _알고 있어야 함_&#x200B;을(를) 기반으로 각 계정을 특정 [역할](../systems/permissions-user-roles.md) 및 액세스 수준에 연결할 수 있습니다. 각 관리자 사용자 계정과 연결된 이메일 주소는 고유해야 합니다.

{{ims-admin-note}}

## 사용 데이터 수집

_관리자_&#x200B;에 처음 로그인하면 모든 관리자 사용자에 대한 사용 데이터를 수집할 수 있는 Adobe 권한을 부여하라는 메시지가 표시됩니다. 관리자 사용 데이터 수집을 허용하면 Adobe이 Adobe Commerce 관리자, 관련 제품 및 서비스를 사용하는 경험을 개선할 수 있습니다.

![관리자 사용 데이터 수집 허용](./assets/admin-usage-data.png){width="600"}

개별 사용자는 사용 데이터에서 식별되지 않습니다. [관리자 사용](../configuration-reference/advanced/admin.md#admin-usage) 구성에서 언제든지 데이터 수집 설정을 변경할 수 있습니다.

Adobe Commerce의 경우 데이터 수집을 허용하면 대화형 콘텐츠를 _관리자_&#x200B;에게 가져오도록 디자인된 _제품 내 지침_&#x200B;도 사용할 수 있습니다. 도움말, 도구 설명, 둘러보기 안내서, 온보딩 정보, 기능 공지 등을 제공합니다.
