---
title: 보안 검사
description: 향상된 보안 검사를 실행하고 각 Adobe Commerce 및 Magento Open Source 사이트를 모니터링하는 방법에 대해 알아봅니다.
exl-id: 87d4739f-496c-4e47-89a3-70d3969c0fdb
role: Admin
feature: Security, Site Management, Reporting
source-git-commit: 370131cd73a320b04ee92fa9609cb24ad4c07eca
workflow-type: tm+mt
source-wordcount: '616'
ht-degree: 0%

---

# 보안 검사

향상된 보안 검사를 통해 PWA을 포함한 각 Adobe Commerce 및 Magento Open Source 사이트를 모니터링하여 알려진 보안 위험 및 맬웨어를 확인하고 패치 업데이트 및 보안 알림을 받을 수 있습니다.

- 스토어의 실시간 보안 상태에 대한 통찰력을 얻으십시오.
- 문제 해결에 도움이 되는 모범 사례를 기반으로 제안을 받습니다.
- 매주, 매일 또는 온디맨드로 보안 검사를 실행하도록 예약합니다.
- 잠재적인 맬웨어를 식별하는 데 도움이 되는 21,000개 이상의 보안 테스트를 실행합니다.
- 사이트의 진행 상황을 추적 및 모니터링하는 기간별 보안 보고서에 액세스합니다.
- 모든 권장 작업과 함께 성공 및 실패한 검사를 표시하는 검사 보고서에 액세스합니다.

보안 검색 도구는 의 대시보드에서 무료로 사용할 수 있습니다. [상거래 계정](../getting-started/commerce-account-create.md). 기술 정보는 다음을 참조하십시오. [보안 검색 도구 설정](https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/launch/overview.html#set-up-the-security-scan-tool) 다음에서 _클라우드 인프라의 Commerce 안내서_.

![보안 검색 도구](./assets/magento-security-scan.png){width="600" zoomable="yes"}

## 보안 검사 실행

1. Commerce 홈 페이지로 이동하여 [상거래 계정](../getting-started/commerce-account-create.md) 다음을 수행합니다.

   - 왼쪽 패널에서 을 선택합니다 **[!UICONTROL Security Scan]**.
   - 클릭 **[!UICONTROL Go to Security Scan]**.
   - 읽기 **[!UICONTROL Terms and Conditions]**.
   - 클릭 **[!UICONTROL Agree]** 계속합니다.

1. 다음에서 _[!UICONTROL Monitored Websites]_페이지, 클릭&#x200B;**[!UICONTROL +Add Site]**.

   도메인이 다른 사이트가 여러 개 있는 경우 각 도메인에 대해 별도의 검사를 구성해야 합니다.

   ![모니터링되는 사이트](./assets/monitored-website.png){width="600" zoomable="yes"}

1. 확인 코드를 추가하여 사이트 도메인의 소유권을 확인하려면 다음 중 하나를 수행하십시오.

   **상거래 상점**:

   - 다음을 입력합니다. **[!UICONTROL Site URL]** 및 **[!UICONTROL Site Name]**.
   - 클릭 **[!UICONTROL Generate Confirmation Code]**.
   - 클릭 **복사** 클립보드에 확인 코드를 복사합니다.

     ![확인 코드 생성](./assets/scan-site1.png){width="400" zoomable="yes"}

   - 저장소 관리자에 전체 관리자 권한이 있는 사용자로 로그인하고 다음을 수행합니다.

      - 다음에서 _관리자_ 사이드바, 이동 **[!UICONTROL Content]** > _[!UICONTROL Design]_>**[!UICONTROL Configuration]**.
      - 목록에서 사이트를 찾은 다음 **[!UICONTROL Edit]**.
      - 확장 ![확장 선택기](../assets/icon-display-expand.png) 다음 **[!UICONTROL HTML Head]** 섹션.
      - 아래로 스크롤하여 **[!UICONTROL Scripts and Style Sheets]** 기존 코드의 끝에 있는 텍스트 상자를 클릭하고 확인 코드를 텍스트 상자에 붙여 넣습니다.

        ![스크립트 및 스타일 시트](./assets/scan-paste-code.png){width="600" zoomable="yes"}

      - 완료되면 다음을 클릭하십시오. **[!UICONTROL Save Configuration]**.

   **PWA 상점**:

   - 다음을 입력합니다. **[!UICONTROL Site URL]** 및 **[!UICONTROL Site Name]**.

   - 대상 **[!UICONTROL Confirmation Code]**, 을(를) 선택합니다. `META Tag` 옵션을 선택한 다음 **[!UICONTROL Generate Code]**.

   - 클릭 **[!UICONTROL Copy]** 생성된 확인 코드 META Tag 를 클립보드에 복사합니다.

     ![확인 코드 생성](./assets/scan-site2.png){width="400" zoomable="yes"}

   - PWA Studio 상점 프로젝트 디렉토리로 이동하여 다음을 수행합니다.

      - PWA Studio 프로젝트 디렉터리에서 `packages > venia-concept > template.html`.
      - 복사된 확인 코드(생성된 META 태그)를 HTML 헤드에 추가하고 변경 사항을 저장합니다.

        ![확인 코드 복사](./assets/code-pwa.png){width="600" zoomable="yes"}

      - PWA Studio CLI로 돌아가서 yarn을 사용하여 프로젝트 종속성을 설치하고 프로젝트 빌드 명령을 실행합니다.

        ```sh
        yarn install &&
        yarn build
        ```

      - *클라우드 프로젝트에서*, 만들기 `pwa` storefront 프로젝트 내 콘텐츠 폴더 및 복사 `dist` 폴더를 삭제합니다.

        ```sh
        mkdir pwa && cp -r <path to your storefront project>/dist/* pwa
        ```

      - Git CLI 도구를 사용하여 이러한 변경 사항을 클라우드 프로젝트에 스테이징하고, 커밋하고, 푸시합니다.

        ```sh
        git add . &&
        git commit -m "Added storefront file bundles" &&
        git push origin
        ```

        빌드 프로세스가 완료되면 변경 사항이 PWA 저장소 전면에 배포됩니다.

1. (으)로 돌아가기 _[!UICONTROL Security Scan]_상거래 계정에서 페이지를 방문한 다음&#x200B;**[!UICONTROL Verify Confirmation Code]**도메인의 소유권을 설정하기 위해

1. 확인이 성공하면 을(를) 구성합니다 **[!UICONTROL Set Automatic Security Scan]** 다음 유형 중 하나에 대한 옵션:

   **매주 스캔(권장)**:

   - 다음을 선택합니다. **[!UICONTROL Week Day]**, **[!UICONTROL Time]**, 및 **[!UICONTROL Time Zone]** 매주 스캔을 해야 합니다.
   - 기본적으로 스캔은 매주 토요일 자정(UTC)에 시작되고 일요일 초까지 계속되도록 예약되어 있습니다.

     ![매주 스캔](./assets/scan-weekly.png){width="500" zoomable="yes"}

   **매일 스캔**:

   - 다음을 선택합니다. **[!UICONTROL Time]**, 및 **[!UICONTROL Time Zone]** 스캔은 매일 실시해야 합니다.
   - 기본적으로 검색은 매일 자정(UTC)에 시작되도록 예약되어 있습니다.

     ![매일 스캔](./assets/scan-daily.png){width="500" zoomable="yes"}

1. 다음을 입력합니다. **[!UICONTROL Email Address]** 완료된 검사 및 보안 업데이트에 대한 알림을 받을 위치입니다.

   ![이메일 주소](./assets/scan-notification-email.png){width="400" zoomable="yes"}

1. 완료되면 다음을 클릭하십시오. **[!UICONTROL Submit]**.

   도메인의 소유권이 확인되면 사이트가 Commerce 계정의 모니터링되는 웹 사이트 목록에 표시됩니다.

1. 도메인이 다른 여러 웹 사이트가 있는 경우 이 프로세스를 반복하여 각각에 대한 보안 검사를 설정합니다.
