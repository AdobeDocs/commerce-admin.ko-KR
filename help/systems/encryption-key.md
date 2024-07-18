---
title: 암호화 키
description: 보안을 개선하기 위해 정기적으로 변경되어야 하는 자체 암호화 키를 자동으로 생성하거나 추가하는 방법에 대해 알아봅니다.
exl-id: 78190afb-3ca6-4bed-9efb-8caba0d62078
role: Admin
feature: System, Security
source-git-commit: 2469b3853d074f7a7adfe822b645e41d1420259a
workflow-type: tm+mt
source-wordcount: '296'
ht-degree: 0%

---

# 암호화 키

Adobe Commerce과 Magento Open Source은 암호 및 기타 민감한 데이터를 보호하기 위해 암호화 키를 사용합니다. 업계 표준 [!DNL ChaCha20-Poly1305] 알고리즘은 암호화가 필요한 모든 데이터를 암호화하기 위해 256비트 키와 함께 사용됩니다. 여기에는 신용 카드 데이터 및 통합(결제 및 배송 모듈) 암호가 포함됩니다. 또한 강력한 보안 해시 알고리즘(SHA-256)을 사용하여 암호 해독이 필요하지 않은 모든 데이터를 해시합니다.

초기 설치 중에 Commerce에서 암호화 키를 생성하거나 자체 키 중 하나를 입력하라는 메시지가 표시됩니다. 암호화 키 도구를 사용하면 필요에 따라 키를 변경할 수 있습니다. 보안을 향상하기 위해 암호화 키를 정기적으로 변경해야 하며, 언제든지 원본 키가 손상될 수 있습니다. 키가 변경될 때마다 모든 기존 데이터는 새 키를 사용하여 다시 인코딩됩니다.

자세한 내용은 _설치 가이드_&#x200B;의 [고급 온-프레미스 설치](https://experienceleague.adobe.com/docs/commerce-operations/installation-guide/advanced.html)를 참조하십시오.

>[!IMPORTANT]
>
>다음 지침에 따라 암호화 키를 변경하기 전에 다음 파일에 쓸 수 있는지 확인하십시오. `[your store]/app/etc/env.php`

**암호화 키를 변경하려면:**

다음 지침은 터미널에 액세스해야 합니다.

1. [유지 관리 모드](https://experienceleague.adobe.com/en/docs/commerce-operations/configuration-guide/setup/application-modes#maintenance-mode)를 사용하도록 설정합니다.

   ```bash
   bin/magento maintenance:enable
   ```

1. cron 작업을 비활성화합니다.

   _클라우드 인프라 프로젝트:_

   ```bash
   ./vendor/bin/ece-tools cron:disable
   ```

   _온-프레미스 프로젝트_

   ```bash
   crontab -e
   ```

1. _관리자_ 사이드바에서 **[!UICONTROL System]** > _[!UICONTROL Other Settings]_>**[!UICONTROL Manage Encryption Key]**(으)로 이동합니다.

   ![시스템 암호화 키](./assets/encryption-key.png){width="700" zoomable="yes"}

1. 다음 중 하나를 수행합니다.

   - 새 키를 생성하려면 **[!UICONTROL Auto-generate Key]**&#x200B;을(를) `Yes`(으)로 설정하십시오.
   - 다른 키를 사용하려면 **[!UICONTROL Auto-generate Key]**&#x200B;을(를) `No`(으)로 설정하십시오. 그런 다음 **[!UICONTROL New Key]** 필드에 사용할 키를 입력하거나 붙여 넣습니다.

1. **[!UICONTROL Change Encryption Key]**&#x200B;을(를) 클릭합니다.

   >[!NOTE]
   >
   >새 키를 안전한 위치에 기록하십시오. 파일에 문제가 발생하는 경우 데이터를 해독해야 합니다.

1. 캐시를 플러시합니다.

   _클라우드 인프라 프로젝트:_

   ```bash
   magento-cloud cc
   ```

   _온-프레미스 프로젝트:_

   ```bash
   bin/magento cache:flush
   ```

1. 크론 작업을 활성화합니다.

   _클라우드 인프라 프로젝트:_

   ```bash
   ./vendor/bin/ece-tools cron:enable
   ```

   _온-프레미스 프로젝트:_

   ```bash
   crontab -e
   ```

1. 유지 관리 모드를 비활성화합니다.

   ```bash
   bin/magento maintenance:disable
   ```
