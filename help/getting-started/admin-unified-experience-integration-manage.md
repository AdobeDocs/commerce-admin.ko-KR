---
title: Experience Cloud 통합 관리
description: Experience Cloud 통합을 관리하고 문제를 해결하는 방법에 대해 알아봅니다
hide: false
hidefromtoc: false
feature: Integration
exl-id: 451bf2e1-7c38-40be-a7c1-aaf0fe9f486c
source-git-commit: 15569794c1e66ba5a93e46206244e2951522923e
workflow-type: tm+mt
source-wordcount: '514'
ht-degree: 0%

---

# Experience Cloud 통합 관리

초기 활성화 이후 Commerce 관리 통합 경험 확장을 활성화 또는 비활성화하여 Experience Cloud 통합 상태를 관리합니다.

- Commerce 관리자 통합 경험 확장이 활성화되어 있고 관리자 계정이 [올바르게 프로비저닝된 경우](#manage-admin-user-accounts) Commerce 관리자는 Adobe Experience Cloud에서 사용 가능한 Commerce 프로젝트를 보고 액세스할 수 있습니다. 관리자는 여전히 Commerce 프로젝트 환경의 관리 URL을 사용하여 개별 프로젝트에 액세스할 수 있습니다.

- Commerce 관리자 통합 경험 확장이 비활성화되어 있으면 Experience Cloud을 통한 액세스가 비활성화됩니다. 관리자는 Commerce 프로젝트 환경의 관리 URL을 사용하여 개별 프로젝트에 로그인해야 합니다.

>[!WARNING]
>
>IMS(Adobe Identity Management 서비스) 통합이 비활성화되면 Experience Cloud 통합이 자동으로 비활성화됩니다.

## 관리자의 통합 관리

1. Commerce 관리자의 왼쪽 탐색 메뉴에서 **[!UICONTROL Stores]**&#x200B;을(를) 선택하여 [저장소 구성] 메뉴를 연 다음 **[!UICONTROL Configuration]**&#x200B;을(를) 선택합니다.

1. 구성 메뉴에서 **[!UICONTROL Advanced > Admin]**&#x200B;을(를) 선택한 다음 **[!UICONTROL Unified Experience option]**&#x200B;을(를) 확장합니다.

   ![Experience Cloud 통합을 위한 관리자 저장소 구성](./assets/admin-uex-manage-settings.png){width="600" zoomable="yes"}

1. **[!UICONTROL Enable]** 값을 선택하여 통합을 활성화하거나 비활성화합니다.

1. **[!UICONTROL Project Name]** 값을 추가하거나 업데이트하여 Commerce 프로젝트 작업 영역에 표시되는 프로젝트 이름을 변경합니다.

1. 구성을 저장합니다.

1. 캐시를 지웁니다.

## Adobe Commerce CLI를 사용하여 통합 관리

Commerce 클라우드 프로젝트에 대한 관리자 액세스 권한이 있는 Commerce 시스템 관리자는 Adobe Commerce CLI 명령을 사용하여 Experience Cloud 통합을 관리할 수 있습니다.

1. 로컬 개발 환경에서 클라우드 프로젝트에 로그인합니다.

   ```bash
   magento-cloud login
   ```

1. 클라우드 프로젝트 환경의 루트 디렉토리에서 Commerce 애플리케이션 서버에 연결합니다.

   ```bash
   ssh magento-cloud
   ```

1. Admin Unified Experience 확장의 상태를 확인합니다.

   ```bash
   bin/magento admin:uex:status
   ```

1. 통합을 비활성화하려면 확장 상태를 변경하십시오.

   - **사용**—`bin/magento config:set admin/unified_experience/enabled 1`

   - **사용 안 함**—`bin/magento config:set admin/unified_experience/enabled 0`

## 관리 사용자 계정 관리

Adobe 제품 및 서비스에 액세스하려면 모든 Commerce 관리자 사용자에게 Commerce 인스턴스의 관리자 계정과 Adobe 사용자 계정(Adobe ID)이 모두 있어야 합니다. 두 계정 모두 동일한 이메일 주소와 연결되어 있어야 합니다.

- Commerce 인스턴스의 관리자로부터 **Commerce 관리자 계정**—[Commerce 관리자 사용자 관리](../systems/permissions-users-all.md)를 받습니다. Commerce 관리자의 사용자 계정에는 관리자 역할이 할당되어야 합니다.

  Commerce 프로젝트의 시스템 관리자는 [SSH를 사용하여 원격 환경에 연결](https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/develop/secure-connections.html?lang=ko#connect-to-a-remote-environment)하고 Commerce CLI `admin:user:create` 및 `admin:user:unlock` 명령을 사용하여 관리자 계정을 추가하거나 잠금 해제할 수 있습니다.

- **Adobe 사용자 계정**—Commerce 인스턴스와 연결된 Adobe 조직의 관리자는 Adobe Admin Console에 로그인하고 각 Commerce 관리자에 대한 Adobe ID을 조직에 추가해야 합니다. 그런 다음 Commerce 애플리케이션에 액세스할 수 있는 제품 권한 및 권한을 할당해야 합니다. [Adobe Admin Console에서 Adobe Commerce 사용자 구성](adobe-ims-config.md#step-4-configure-adobe-commerce-users-in-the-adobe-admin-console)을 참조하십시오.

Adobe Developer Console에서 Experience Cloud 통합에 대한 구성을 관리하는 관리자는 시스템 관리자 또는 개발자 액세스 권한이 있는 Adobe 사용자 계정이 있어야 합니다.

>[!NOTE]
>
>Adobe ID은 Experience Cloud을 통해 제품 및 서비스에 액세스하는 데 필요한 Adobe을 통해 생성되는 계정입니다. Adobe ID이 없는 Commerce 관리자는 Commerce 관리자에 로그인하는 데 사용하는 것과 동일한 이메일 주소를 사용하여 [무료 계정을 만들 수 있습니다](https://helpx.adobe.com/kr/manage-account/using/create-update-adobe-id.html).
