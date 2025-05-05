---
title: '[!UICONTROL Advanced] &gt; [!UICONTROL System]'
description: Commerce 관리자의 [!UICONTROL Advanced] &gt; [!UICONTROL System] 페이지에서 구성 설정을 검토하십시오.
exl-id: ffdaf7b5-c508-4fab-93ec-21f28cff6d3d
role: Admin, Developer
feature: Configuration, System
source-git-commit: 5a4417373f6dc720e8e14f883c27348a475ec255
workflow-type: tm+mt
source-wordcount: '1664'
ht-degree: 1%

---

# [!UICONTROL Advanced] > [!UICONTROL System]

{{config}}

## [!UICONTROL Cron (Scheduled Tasks)]

![고급 구성 - Cron(예약된 작업)](./assets/system-cron.png)<!-- zoom -->

이러한 구성 설정 변경에 대한 자세한 내용은 [Cron(예약된 작업)](../../systems/cron.md)을 참조하십시오.

### [!UICONTROL index]

![고급 구성 - 크론 그룹: 인덱스](./assets/system-cron-group-index.png)<!-- zoom -->

| 필드 | [범위](../../getting-started/websites-stores-views.md#scope-settings) | 설명 |
|--- |--- |--- |
| [!UICONTROL Generate Schedules Every] | 글로벌 | 일정이 생성되는 빈도를 분 단위로 결정합니다. |
| [!UICONTROL Schedule Ahead for] | 글로벌 | 일정이 생성되는 시간(분)을 미리 결정합니다. |
| [!UICONTROL Missed if Not Run Within] | 글로벌 | 아직 실행되지 않은 cron job이 missed로 표시되기까지의 시간(분)을 결정합니다. |
| [!UICONTROL History Cleanup Every] | 글로벌 | 크론 기록을 정리하기 전까지 경과되는 시간(분)을 결정합니다. |
| [!UICONTROL Success History Lifetime] | 글로벌 | 성공적으로 완료된 cron 작업 레코드가 데이터베이스에 유지되는 시간(분)을 결정합니다. |
| [!UICONTROL Failure History Lifetime] | 글로벌 | 실패한 cron 작업의 레코드가 데이터베이스에 유지되는 시간(분)을 결정합니다. |
| [!UICONTROL Use Separate Process] | 글로벌 | cron 작업이 별도의 프로세스로 동시에 실행되는지 여부를 결정합니다. 옵션: `Yes` / `No` |

{style="table-layout:auto"}

### [!UICONTROL default]

![크론 그룹: 기본값](./assets/system-cron-group-default.png)<!-- zoom -->

| 필드 | [범위](../../getting-started/websites-stores-views.md#scope-settings) | 설명 |
|--- |--- |--- |
| [!UICONTROL Generate Schedules Every] | 글로벌 | 일정이 생성되는 빈도를 분 단위로 결정합니다. |
| [!UICONTROL Schedule Ahead for] | 글로벌 | 일정이 생성되는 시간(분)을 미리 결정합니다. |
| [!UICONTROL Missed if Not Run Within] | 글로벌 | 아직 실행되지 않은 cron job이 missed로 표시되기까지의 시간(분)을 결정합니다. |
| [!UICONTROL History Cleanup Every] | 글로벌 | 크론 기록을 정리하기 전까지 경과되는 시간(분)을 결정합니다. |
| [!UICONTROL Success History Lifetime] | 글로벌 | 성공적으로 완료된 cron 작업 레코드가 데이터베이스에 유지되는 시간(분)을 결정합니다. |
| [!UICONTROL Failure History Lifetime] | 글로벌 | 실패한 cron 작업의 레코드가 데이터베이스에 유지되는 시간(분)을 결정합니다. |
| [!UICONTROL Use Separate Process] | 글로벌 | cron 작업이 별도의 프로세스로 동시에 실행되는지 여부를 결정합니다. 옵션: `Yes` / `No` |

{style="table-layout:auto"}

## [!UICONTROL MySQL Message Queue Cleanup]

{{ee-feature}}

![고급 구성 - MySQL 메시지 큐 정리](./assets/system-mysql-message-queue-cleanup.png)<!-- zoom -->

| 필드 | [범위](../../getting-started/websites-stores-views.md#scope-settings) | 설명 |
|--- |--- |--- |
| [!UICONTROL Successful Messages Lifetime] | 글로벌 | 성공한 메시지의 라이프타임(분)을 결정합니다. 정리를 건너뛰려면 0을 입력합니다. 기본값: `10080`(7일) |
| [!UICONTROL New Messages Lifetime] | 글로벌 | 새 메시지의 라이프타임(분)을 결정합니다. 정리를 건너뛰려면 0을 입력합니다. 기본값: `10080`(7일) |
| [!UICONTROL Failed Messages Lifetime] | 글로벌 | 실패한 메시지의 라이프타임(분)을 결정합니다. 정리를 건너뛰려면 0을 입력합니다. 기본값: `10080`(7일) |
| [!UICONTROL Retry Messages in Progress After] | 글로벌 | 시스템이 다시 시도하기 전에 진행 중인 메시지를 기다리는 시간을 결정합니다. 기본값: `1440`(24시간) |

{style="table-layout:auto"}

## [!UICONTROL Mail Sending Settings]

![고급 구성 - 메일 전송 설정](./assets/system-mail-sending-settings.png)<!-- zoom -->

이러한 설정 변경에 대한 자세한 내용은 _관리 시스템 안내서_&#x200B;에서 [전자 메일 통신 구성](../../systems/email-communications.md)을 참조하십시오.

>[!IMPORTANT]
>
>**보안 알림** 최근에 식별된 잠재적인 원격 코드 실행 악용으로부터 보호하기 위해 모든 판매자가 메일 전송 구성을 즉시 설정하는 것이 좋습니다. 이 문제가 해결될 때까지 전자 메일 통신에 [!DNL Sendmail]을(를) 사용하지 않는 것이 좋습니다. [!UICONTROL Mail Sending Settings]에서 [!UICONTROL Set Return Path]이(가) `No`(으)로 설정되어 있는지 확인하십시오.

| 필드 | [범위](../../getting-started/websites-stores-views.md#scope-settings) | 설명 |
|--- |--- |--- |
| [!UICONTROL Disable Email Communications] | 스토어 뷰 | 스토어에 대해 이메일 통신이 활성화되었는지 여부를 확인합니다. 옵션: `Yes` / `No` |
| [!UICONTROL Transport] | 스토어 뷰 | 스토어에서 이메일 커뮤니케이션의 전송 유형을 결정합니다. 옵션: `Sendmail` / `SMTP` |
| [!UICONTROL Host] | 스토어 뷰 | (SMTP 및 Windows 서버만 해당) 호스트를 참조하는 데 사용할 이름을 결정합니다. 기본값: `localhost` |
| [!UICONTROL Port (25)] | 스토어 뷰 | (SMTP 및 Windows 서버만 해당) 전자 메일 통신에 사용되는 포트를 식별합니다. 기본값: `25` |
| [!UICONTROL Set Return-Path] | 스토어 뷰 | 반송된 이메일에 라우팅 주소를 사용하는지 여부를 결정합니다. 옵션: `No` / `Yes` / `Specified` |

{style="table-layout:auto"}

### SMTP 옵션

전송 유형에서 SMTP를 선택하면 SMTP 서버 연결을 구성하는 추가 옵션을 사용할 수 있습니다.

![고급 구성 - SMTP를 사용한 메일 전송 설정](./assets/system-mail-sending-settings-smtp.png)<!-- zoom -->

| 필드 | [범위](../../getting-started/websites-stores-views.md#scope-settings) | 설명 |
|--- |--- |--- |
| [!UICONTROL Username] | 스토어 뷰 | SMTP 서버의 로그인 사용자 이름입니다. |
| [!UICONTROL Password] | 스토어 뷰 | SMTP 서버 로그인 암호. |
| [!UICONTROL Auth] | 스토어 뷰 | SMTP 서버 연결에 대한 인증 유형을 결정합니다. 옵션: `NONE` / `PLAIN` / `LOGIN` |
| [!UICONTROL SSL] | 스토어 뷰 | 호스트 보안 인증서의 확인 유형을 결정합니다. 옵션: `SSL` / `TLS` |

{style="table-layout:auto"}

## [!UICONTROL Currency]

![고급 구성 - 통화](./assets/system-currency.png)<!-- zoom -->

이 설정을 변경하는 방법에 대한 자세한 내용은 _저장 및 구매 경험 안내서_&#x200B;에서 [통화 구성](../../stores-purchase/currency-configuration.md)을 참조하세요.

| 필드 | [범위](../../getting-started/websites-stores-views.md#scope-settings) | 설명 |
|--- |--- |--- |
| [!UICONTROL Installed Currencies] | 글로벌 | 현재 Commerce 설치에 사용할 수 있는 통화를 나타냅니다. 옵션에는 설치된 통화가 선택된 사용 가능한 모든 통화가 포함됩니다. |

{style="table-layout:auto"}

## [!UICONTROL Security]

![고급 구성 - 보안](./assets/system-security.png)<!-- zoom -->

이러한 설정 변경에 대한 자세한 내용은 _관리 시스템 안내서_&#x200B;에서 [세션 관리](../../systems/security-session-management.md)를 참조하십시오.

| 필드 | [범위](../../getting-started/websites-stores-views.md#scope-settings) | 설명 |
|--- |--- |--- |
| [!UICONTROL Max Session Size in Admin] | 글로벌 | 최대 세션 크기를 바이트 단위로 제한합니다. `0`을(를) 사용하여 비활성화하십시오. |
| [!UICONTROL Max Session Size in Storefront] | 글로벌 | 최대 세션 크기를 바이트 단위로 제한합니다. `0`을(를) 사용하여 비활성화하십시오. |

{style="table-layout:auto"}

## [!UICONTROL Notifications]

![고급 구성 - 알림](./assets/system-notifications.png)<!-- zoom -->

이러한 설정 변경에 대한 자세한 내용은 _관리 시스템 안내서_&#x200B;에서 [시스템 알림](../../systems/notifications.md)을 참조하십시오.

| 필드 | [범위](../../getting-started/websites-stores-views.md#scope-settings) | 설명 |
|--- |--- |--- |
| [!UICONTROL Use HTTPS to Get Feed] | 글로벌 | 보안 채널을 통해 관리자 알림이 전달되는지 여부를 결정합니다. 옵션: `Yes` / `No` |
| 업데이트 주기 | 글로벌 | 관리 메시지 업데이트 빈도를 결정합니다. 옵션: `1 Hour` / `2 Hours` / `6 Hours` / `12 Hours` / `24 Hours` |
| [!UICONTROL Last Update] | 글로벌 | 마지막 메시지 업데이트 날짜 및 시간을 나타냅니다. |

{style="table-layout:auto"}

## [!UICONTROL Backup Settings]

![고급 구성 - 백업 설정](./assets/system-scheduled-backup-settings.png)<!-- zoom -->

{{$include /help/_includes/backups-note.md}}

이러한 설정 변경에 대한 자세한 내용은 _관리 시스템 안내서_&#x200B;에서 [시스템 백업](../../systems/backups.md)을 참조하십시오.

| 필드 | [범위](../../getting-started/websites-stores-views.md#scope-settings) | 설명 |
|--- |--- |--- |
| [!UICONTROL Enable Backup] | 글로벌 | Commerce 인스턴스에서 백업을 허용하는지 여부를 결정합니다. 옵션: `Yes` / `No` |
| [!UICONTROL Enable Scheduled Backup] | 글로벌 | (_[!UICONTROL Enable Backup]_&#x200B;이(가) `Yes`(으)로 설정되면 표시됩니다.) Commerce 인스턴스가 정기적으로 자동으로 백업되는지 여부를 결정합니다. 옵션: `Yes` / `No` |
| [!UICONTROL Scheduled Backup Type] | 글로벌 | (_[!UICONTROL Enable Scheduled Backup]_&#x200B;이(가) `Yes`(으)로 설정된 경우 표시됩니다.) 백업에 포함된 Commerce 인스턴스의 요소를 결정합니다. 옵션: `Database` / `Database and Media` / `System` / `System (excluding Media)` |
| [!UICONTROL Start Time] | 글로벌 | ([!UICONTROL Enable Scheduled Backup]이(가) `Yes`(으)로 설정되면 표시됩니다.) 예약된 백업이 시작되는 시간, 분, 초를 지정합니다. |
| [!UICONTROL Frequency] | 글로벌 | ([!UICONTROL Enable Scheduled Backup]이(가) `Yes`(으)로 설정되어 있을 때 표시됩니다.) 예약된 백업이 수행되는 빈도를 결정합니다. 옵션: `Daily` / `Weekly` / `Monthly` |
| [!UICONTROL Maintenance Mode] | 글로벌 | ([!UICONTROL Enable Scheduled Backup]이(가) `Yes`(으)로 설정되면 표시됩니다.) 예약된 백업 동안 저장소가 유지 관리 모드에 있는지 여부를 확인합니다. 옵션: `Yes` / `No` |

{style="table-layout:auto"}

## [!UICONTROL Admin Actions Log Archiving]

{{ee-feature}}

![고급 구성 - 관리 작업 로그 보관](./assets/system-admin-actions-log-archiving.png)<!-- zoom -->

이러한 설정 변경에 대한 자세한 내용은 _관리 시스템 안내서_&#x200B;에서 [작업 로그 보관](../../systems/action-log-archive.md)을 참조하십시오.

| 필드 | [범위](../../getting-started/websites-stores-views.md#scope-settings) | 설명 |
|--- |--- |--- |
| [!UICONTROL Log Entry Lifetime, Days] | 스토어 뷰 | 관리 작업이 관리 작업 아카이브에 보관되는 일 수를 결정합니다. 기본값: `60` |
| [!UICONTROL Log Archiving Frequency] | 스토어 뷰 | 관리 작업 로그가 보관되는 빈도를 결정합니다. 옵션: `Daily` / `Weekly` / `Monthly` |

{style="table-layout:auto"}

## [!UICONTROL Full Page Cache]

![고급 구성 - 전체 페이지 캐시](./assets/system-full-page-cache.png)<!-- zoom -->

이러한 설정 변경에 대한 자세한 내용은 _관리 시스템 안내서_&#x200B;에서 [전체 페이지 캐싱](../../systems/cache-management.md#full-page-caching)을 참조하십시오.

![고급 구성 - 바니시 구성](./assets/system-full-page-cache-varnish.png)<!-- zoom -->

| 필드 | [범위](../../getting-started/websites-stores-views.md#scope-settings) | 설명 |
|--- |--- |--- |
| [!UICONTROL Caching Application] | 글로벌 | 전체 페이지 캐시를 관리하는 데 사용할 응용 프로그램을 결정합니다. 옵션: <br/>**`Built-in Application`**- 프로덕션 환경에는 권장되지 않습니다.<br/>**`Varnish Caching`** - 프로덕션 환경에 권장됩니다. |
| [!UICONTROL TTL for public content] | 글로벌 | 공개 콘텐츠 캐시의 라이프타임(초)을 결정합니다. 기본값: `120` |
| [!UICONTROL Handles param size] | 글로벌 | [`{BASE-URL}/page_cache/block/esi`](https://experienceleague.adobe.com/docs/commerce-operations/configuration-guide/cache/use-varnish-esi.html?lang=ko) HTTP 끝점에서 처리할 최대 [레이아웃 핸들](https://developer.adobe.com/commerce/frontend-core/guide/layouts/#layout-handles) 수를 지정합니다. 크기를 제한하면 보안과 성능을 향상시킬 수 있습니다. 기본값: `100` |
| **[!UICONTROL Varnish Configuration]** |  |  |
| [!UICONTROL Access list] | 글로벌 | 구성 파일을 생성하기 위해 바니시 구성을 제거할 수 있는 IP 주소를 지정합니다. 여러 항목은 쉼표로 구분하십시오. 기본값: `localhost` |
| [!UICONTROL Backend host] | 글로벌 | 구성 파일을 생성하는 백엔드 호스트를 지정합니다. 기본값: `localhost` |
| [!UICONTROL Backend port] | 글로벌 | 구성 파일을 생성하는 데 사용되는 백엔드 포트를 지정합니다. 기본값: `8080` |
| [!UICONTROL Grace period] | 글로벌 | 백엔드가 응답하지 않는 경우 Vannish가 오래된 콘텐츠를 제공하는 기간을 결정합니다. 기본값: `300` |
| **[!UICONTROL Export Configuration]** |  |  |
| [!UICONTROL Export VCL for Varnish 4] | 글로벌 | 버전 4의 `varnish.vcl` 파일을 내보냅니다. |
| [!UICONTROL Export VCL for Varnish 5] | 글로벌 | 버전 5의 `varnish.vcl` 파일을 내보냅니다. |
| [!UICONTROL Export VCL for Varnish 6] | 글로벌 | 버전 6의 `varnish.vcl` 파일을 내보냅니다. |

{style="table-layout:auto"}

## [!UICONTROL Storage Configuration for Media]

![고급 구성 - 미디어 - 파일 시스템에 대한 저장소 구성](./assets/system-storage-config-media.png)<!-- zoom -->

이러한 설정 변경에 대한 자세한 내용은 _콘텐츠 및 디자인 가이드_&#x200B;에서 [미디어 데이터베이스 사용](../../content-design/media-storage-database.md)을 참조하십시오.

| 필드 | [범위](../../getting-started/websites-stores-views.md#scope-settings) | 설명 |
|--- |--- |--- |
| [!UICONTROL Media Storage] | 글로벌 | 미디어 파일을 저장하는 데 사용할 방법을 결정합니다. 기본 설정: `File System` |
| [!UICONTROL Environment Update Time] | 글로벌 | 미디어 파일 환경 업데이트 빈도를 초 단위로 결정합니다. 기본값: `3600` |

{style="table-layout:auto"}

![고급 구성 - 미디어 - 데이터베이스에 대한 저장소 구성](./assets/database-storage-deprecated.png)<!-- zoom -->

>[!IMPORTANT]
>
>데이터베이스 미디어 저장 방법은 Adobe Commerce 및 Magento Open Source 2.4.3부터 더 이상 사용되지 않습니다.

| 필드 | [범위](../../getting-started/websites-stores-views.md#scope-settings) | 설명 |
|--- |--- |--- |
| [!UICONTROL Media Storage] | 글로벌 | 미디어 파일을 저장하는 데 사용되는 메서드로 데이터베이스를 지정합니다. |
| [!UICONTROL Select Media Database] | 글로벌 | 미디어 스토리지에 사용되는 데이터베이스의 이름을 식별합니다. 기본 설정: `default_setup` |
| [!UICONTROL Synchronize] |  | 지정한 데이터베이스 위치에 모든 미디어의 전송을 동기화합니다. |
| 환경 업데이트 시간 | 글로벌 | 미디어 파일 환경 업데이트 빈도를 초 단위로 결정합니다. 기본값: `3600` |

{style="table-layout:auto"}

## [!UICONTROL Bulk Actions]

{{ee-feature}}

![고급 구성 - 일괄 작업](./assets/system-bulk-actions.png)<!-- zoom -->

이러한 설정 변경에 대한 자세한 내용은 _관리 시스템 안내서_&#x200B;에서 [일괄 작업](../../systems/action-log-bulk-actions.md)을 참조하십시오.

| 필드 | [범위](../../getting-started/websites-stores-views.md#scope-settings) | 설명 |
|--- |--- |--- |
| [!UICONTROL Days Saved in Log] | 글로벌 | 일괄 작업이 _일괄 작업 로그_ 보관 파일에 보관되는 일 수를 결정합니다. 기본값: `60` |

{style="table-layout:auto"}

## [!UICONTROL Scheduled Import/Export File History Cleaning]

{{ee-feature}}

![고급 구성 - 예약된 가져오기/내보내기 파일 기록 정리](./assets/system-schedule-history-cleaning.png)<!-- zoom -->

이러한 설정 변경에 대한 자세한 내용은 _관리 시스템 안내서_&#x200B;에서 [예약된 가져오기 및 내보내기](../../systems/data-scheduled-import-export.md)를 참조하십시오.

| 필드 | [범위](../../getting-started/websites-stores-views.md#scope-settings) | 설명 |
|--- |--- |--- |
| [!UICONTROL Save File, Days] | 글로벌 | 기록 파일 가져오기/내보내기 파일을 저장하는 일 수를 결정합니다. |
| [!UICONTROL Enable Scheduled File History Cleaning] | 글로벌 | 가져오기/내보내기 파일의 예약된 파일 정리를 활성화합니다. 옵션: `Yes` / `No` |
| [!UICONTROL Clean Now] |  | 예약된 정리를 무시하고 가져오기/내보내기 기록 파일을 즉시 정리합니다. |
| [!UICONTROL Start Time] | 글로벌 | 가져오기/내보내기 기록 파일 정리의 시간, 분, 초를 지정합니다. |
| [!UICONTROL Frequency] | 글로벌 | 가져오기/내보내기 기록 파일을 정리하는 빈도를 결정합니다. 옵션: `Daily` / `Weekly` / `Monthly` |
| [!UICONTROL Error Email Recipient] | 글로벌 | 파일 가져오기/내보내기 기록을 정리하는 동안 오류가 발생할 경우 알림을 받을 사람의 이메일 주소입니다. 여러 주소는 쉼표로 구분합니다. |
| [!UICONTROL Error Email Sender] | 글로벌 | 알림을 보낸 사람으로 표시되는 스토어 연락처를 식별합니다. 기본 보낸 사람: `General Contact` |
| [!UICONTROL Error Email Template] | 글로벌 | 가져오기/내보내기 파일 정리 오류 알림에 사용되는 이메일 템플릿을 식별합니다. 기본 템플릿: `File History Clean Failed` |

{style="table-layout:auto"}

## [!UICONTROL Image Upload Configuration]

![고급 구성 - 이미지 업로드 구성](./assets/system-image-upload-configuration.png)<!-- zoom -->

<!-- [Image Upload Configuration](https://experienceleague.adobe.com/ko/docs/commerce-admin/systems/action-logs/action-log-bulk-actions) -->

| 필드 | [범위](../../getting-started/websites-stores-views.md#scope-settings) | 설명 |
|--- |--- |--- |
| [!UICONTROL Quality] | 글로벌 | 크기 조정된 이미지의 JPG 품질을 결정합니다. 품질이 낮을수록 파일 크기가 줄어듭니다. 고품질로 파일 크기를 줄이려면 80~90%를 사용하십시오. 기본값: `80` |
| [!UICONTROL Enable Frontend Resize] | 글로벌 | 이 설정을 사용하면 _제품 세부 정보_ 페이지에 대해 업로드할 수 있는 큰 크기의 Commerce 이미지 크기를 조정할 수 있습니다. Commerce은 파일을 업로드하기 전에 JavaScript을 사용하여 이미지 파일의 크기를 조정합니다. 이미지 크기를 조정할 때 [최대 폭] 또는 [최대 높이]의 가장 큰 크기를 초과하지 않는 정확한 비율을 유지합니다. 기본값: `Yes` |
| [!UICONTROL Maximum Width] | 글로벌 | 이미지의 최대 픽셀 너비를 결정합니다. 이미지 크기를 조정할 때 이 너비를 초과하지 않습니다. 기본값: `1920` |
| [!UICONTROL Maximum Height] | 글로벌 | 이미지의 최대 픽셀 높이를 결정합니다. 이미지 크기를 조정할 때 이 높이를 초과하지 않습니다. 기본값: `1200` |

{style="table-layout:auto"}

## [!UICONTROL Media Gallery]

![고급 구성 - 미디어 갤러리](./assets/system-media-gallery.png)<!-- zoom -->

| 필드 | [범위](../../getting-started/websites-stores-views.md#scope-settings) | 설명 |
|--- |--- |--- |
| [!UICONTROL Enable Old Media Gallery] | 글로벌 | 이전 미디어 갤러리를 활성화하거나 비활성화합니다. |

{style="table-layout:auto"}

## [!UICONTROL Media Gallery Image Optimization]

![고급 구성 - 미디어 갤러리 이미지 최적화](./assets/system-media-image-optimization.png)<!-- zoom -->

| 필드 | [범위](../../getting-started/websites-stores-views.md#scope-settings) | 설명 |
|--- |--- |--- |
| [!UICONTROL Enable Image Optimization] | 글로벌 | 콘텐츠에 삽입된 이미지의 파일 크기를 줄이기 위해 이미지 크기를 조절할지 여부를 결정합니다. 원본 이미지는 미디어 갤러리에서 보존됩니다. |
| [!UICONTROL Maximum Width] | 글로벌 | 미디어 갤러리에서 컨텐츠로 삽입되는 이미지의 최대 너비(픽셀 단위)입니다. |
| [!UICONTROL Maximum Height] | 글로벌 | 미디어 갤러리에서 컨텐츠로 삽입되는 이미지의 최대 높이(픽셀 단위)입니다. |

{style="table-layout:auto"}

## [!UICONTROL Adobe Stock Integration]

![고급 구성 - Adobe Stock 통합](./assets/system-adobe-stock-integration.png)<!-- zoom -->

이러한 설정 구성에 대한 자세한 내용은 _콘텐츠 및 디자인 가이드_&#x200B;에서 [Adobe Stock 통합](../../content-design/adobe-stock.md)을 참조하십시오.

| 필드 | [범위](../../getting-started/websites-stores-views.md#scope-settings) | 설명 |
|--- |--- |--- |
| [!UICONTROL Enabled Adobe Stock] | 글로벌 | Adobe Stock 통합을 활성화하거나 비활성화합니다. |
| [!UICONTROL API Key (Client ID)] | 글로벌 | 스토어를 Adobe Stock 서비스에 연결하려면 API 키가 필요합니다. |
| [!UICONTROL Client Secret] | 글로벌 | Adobe Stock 통합을 위한 클라이언트 암호가 필요합니다. |
| [!UICONTROL Test Connection] |  | 테스트를 실행하여 API 키가 Adobe Stock 서비스에 사용할 수 있는지 확인합니다. |

{style="table-layout:auto"}
