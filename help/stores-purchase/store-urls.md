---
title: URL 저장
description: 스토어 URL과 기본 URL 및 스토어 코드를 구성하는 방법에 대해 알아봅니다.
exl-id: dd7a6317-b0cf-4d0c-9b31-a963c467026b
feature: Site Management, System
badgePaas: label="PaaS만" type="Informative" url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="Adobe Commerce 온 클라우드 프로젝트(Adobe 관리 PaaS 인프라) 및 온프레미스 프로젝트에만 적용됩니다."
source-git-commit: b4623ada788d44f4628930dcf5dfcb51dd88ee3a
workflow-type: tm+mt
source-wordcount: '1529'
ht-degree: 0%

---

# URL 저장

Adobe Commerce 또는 Magento Open Source 설치의 각 웹 사이트에는 상점 앞에 할당되는 기본 URL과 관리자에게 할당되는 다른 URL이 있습니다. Adobe은 변수를 사용하여 기본 URL과 관련하여 내부 링크를 정의하므로 링크를 업데이트하지 않고도 전체 스토어를 한 위치에서 다른 위치로 이동할 수 있습니다. 표준 기본 URL은 `http`(으)로 시작하고 보안 기본 URL은 `https`(으)로 시작합니다.

- **기본 URL** — `http://www.yourdomain.com/magento/`
- **보안 기본 URL** — `https://www.yourdomain.com/magento/`
- **IP 주소의 URL** — `http://###.###.###.###/magento/` 또는 `https://###.###.###.###/magento/`

>[!IMPORTANT]
>
>기본 기본 기본 URL 구성에서 관리자 URL을 변경하지 마십시오. 관리자 URL 또는 경로를 변경하려면 [사용자 지정 관리자 URL 사용](#use-a-custom-admin-url)을 참조하세요.

## 보안 프로토콜 사용

스토어의 기본 URL은 처음에 Adobe Commerce 설치 중에 설정되었습니다. 보안 인증서를 사용할 수 있는 경우 저장소, 관리자 또는 둘 다에 사용할 `HTTPS`개의 URL을 지정할 수 있습니다. Adobe Commerce 설치에 여러 스토어가 포함되어 있거나 나중에 스토어를 더 추가할 계획이라면 URL에 스토어 코드를 포함할 수 있습니다. 모든 Adobe 리소스 및 작업을 보안 프로토콜과 함께 사용할 수 있습니다.

설치 시 도메인에 대한 보안 인증서를 사용할 수 없는 경우 스토어를 시작하기 전에 구성을 업데이트해야 합니다. 도메인에 대한 보안 인증서가 설정되면 암호화된 SSL(Secure Sockets Layer) 및 [TLS(Transport Layer Security)][1] 프로토콜로 작동하도록 기본 URL 중 하나 또는 둘 다를 구성할 수 있습니다.

>[!IMPORTANT]
>
>Adobe은 보안 프로토콜을 사용하여 콘텐츠 및 제품 페이지를 포함하여 프로덕션 사이트의 모든 페이지를 전송하는 것을 강력히 권장합니다.

기본적으로 `HTTPS`을(를) 통해 모든 페이지를 전달하도록 Adobe Commerce 및 Magento Open Source을 구성할 수 있습니다. 스토어가 표준 프로토콜로 실행되고 있는 경우 [HTTP Strict Transport Security][2]&#x200B;(HSTS)를 사용하도록 설정하고 안전하지 않은 페이지 요청을 업그레이드하여 보안을 강화할 수 있습니다. HSTS는 브라우저가 지정된 도메인에 대해 비보안 프로토콜로 전송되는 표준 `HTTP` 페이지를 렌더링하지 못하도록 하는 옵트인 프로토콜입니다. 검색 엔진이 표준 `HTTP` URL로 저장소의 각 페이지를 이미 인덱싱했을 수 있으므로 Commerce에서 안전하지 않은 페이지 요청을 자동으로 `HTTPS`(으)로 업그레이드하도록 구성하면 트래픽이 손실되지 않습니다. Commerce이 Storefront와 Admin 모두에 보안 URL을 사용하도록 구성된 경우 `HSTS`을(를) 활성화할 수 있는 두 개의 추가 필드가 나타납니다.

## 기본 URL 구성

1. _관리자_ 사이드바에서 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**(으)로 이동합니다.

1. 왼쪽 패널의 _일반_&#x200B;에서 **[!UICONTROL Web]**&#x200B;을(를) 선택합니다.

1. **[!UICONTROL Base URL]** 섹션에서 ![확장 선택기](../assets/icon-display-expand.png)를 확장합니다.

   - **[!UICONTROL Base URL]** — 스토어의 정규화된 기본 URL을 입력합니다. 스토어의 추가 URL 키로 URL을 확장할 수 있도록 URL은 슬래시로 끝나야 합니다. 예: `http://yourdomain.com/`

     >[!NOTE]
     >
     >_[!UICONTROL Base Link URL]_&#x200B;필드의 자리 표시자를 변경하지 마십시오. 기본 URL에 대한 상대 링크를 만드는 데 사용되는 자리 표시자입니다.

   - **[!UICONTROL Base URL for Static View Files]** — (선택 사항) 다음 자리 표시자로 시작하는 경로를 입력하여 정적 보기 파일의 기본 URL에 대한 대체 위치를 지정합니다.

     \{\{unsecure_base_url}}

   - **[!UICONTROL Base URL for User Media Files]** — (선택 사항) 다음 자리 표시자로 시작하는 경로를 입력하여 사용자 미디어 파일의 기본 URL에 대한 대체 위치를 지정합니다.

     \{\{unsecure_base_url}}

     일반 설치의 경우 정적 보기 파일 또는 미디어 파일은 기본 URL을 기준으로 하므로 해당 경로를 업데이트할 필요가 없습니다.

   ![일반 구성 - 웹 기반 URL](../configuration-reference/general/assets/web-base-urls.png){width="600" zoomable="yes"}

   >[!NOTE]
   >
   >이중 중괄호로 묶인 자리 표시자는 변수에 대한 마크업 태그입니다.

1. 완료되면 **[!UICONTROL Save Config]**&#x200B;을(를) 클릭합니다.

## 보안 기본 URL 구성

도메인에 유효한 보안 인증서가 있는 경우 보안(https) 채널을 통해 데이터를 전송하도록 상점 및 관리자의 URL을 모두 구성할 수 있습니다. 유효한 보안 인증서가 없으면 저장소가 보안(SSL/TLS) 프로토콜로 작동할 수 없습니다.

1. ![확장 선택기](../assets/icon-display-expand.png) _[!UICONTROL Base URLs (Secure])_ 섹션을 확장하고 다음을 수행합니다.

   ![일반 구성 - 보안 기본 URL](../configuration-reference/general/assets/web-base-urls-secure.png){width="600" zoomable="yes"}

   - **[!UICONTROL Secure Base URL]** — 전체 보안 기본 URL을 입력한 다음 슬래시를 입력합니다. 예: `https://yourdomain.com/`

   - **[!UICONTROL Secure Base Link URL]** — 보안 기본 링크 URL 필드의 자리 표시자를 변경하지 마십시오. 이 변수는 보안 기본 URL에 대한 상대 링크를 만드는 데 사용됩니다.

   - **[!UICONTROL Secure Base URL for Static View Files]** — (선택 사항) 다음 자리 표시자로 시작하는 경로를 입력하여 정적 보기 파일의 보안 기본 URL에 대한 대체 위치를 지정합니다.

     \{\{secure_base_url}}

   - **[!UICONTROL Secure Base URL for User Media Files]** — (선택 사항) 다음 자리 표시자로 시작하는 경로를 입력하여 사용자 미디어 파일의 보안 기본 URL에 대한 대체 위치를 지정합니다.

     \{\{secure_base_url}}

1. 보안을 강화하려면 다음 옵션을 모두 `Yes`(으)로 설정하십시오.

   - **[!UICONTROL Use Secure URLs on Storefront]**
   - **[!UICONTROL Use Secure URLs in Admin]**

1. _[!UICONTROL Enhanced Security Settings]_&#x200B;의 경우 다음을 수행합니다.

   - **[!UICONTROL Enable HTTP Strict Transport Security (HSTS)]** — 저장소에 보안 HTTPS 페이지 요청만 표시하려면 `Yes`(으)로 설정하십시오.

   - **[!UICONTROL Upgrade Insecure Requests]** — 표준 비보안 HTTP 페이지에 대한 요청을 보안 HTTPS로 업그레이드하려면 `Yes`(으)로 설정합니다.

1. 서버에 대해 **[!UICONTROL Offloader Header]**&#x200B;을(를) 설정합니다.

   대부분의 Commerce 설치에서는 기본 `X-Forward-Proto`을(를) 사용하여 프로토콜을 `HTTP` 또는 `HTTPS`(으)로 식별합니다. 서버 구성에서 다른 offloader_header를 사용하는 경우 여기에 입력합니다.

1. 완료되면 **[!UICONTROL Save Config]**&#x200B;을(를) 클릭합니다.

## URL에 스토어 코드 포함

>[!NOTE]
>
>_URL에 스토어 코드 추가_ 옵션이 `Yes`(으)로 설정된 경우 브라우저 URL에 스토어 코드를 포함해야 합니다. 이 설정을 사용하면 _&quot;404 Page Not Found&quot;_ 오류 없이 URL 다시 쓰기가 올바르게 매핑되고 모든 페이지가 성공적으로 열립니다.

1. _관리자_ 사이드바에서 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**(으)로 이동합니다.

1. 왼쪽 패널의 _[!UICONTROL General]_&#x200B;에서&#x200B;**[!UICONTROL Web]**&#x200B;을(를) 선택합니다.

1. **[!UICONTROL URL Options]** 섹션에서 ![확장 선택기](../assets/icon-display-expand.png)를 확장합니다.

1. **[!UICONTROL Add Store Code]**&#x200B;을(를) 기본 설정으로 설정:

   - **[!UICONTROL URL with Store Code]**: `http://www.yourdomain.com/magento/[store-code]/index.php/url-identifier`
   - **[!UICONTROL URL without Store Code]**: `http://www.yourdomain.com/magento/index.php/url-identifier`

   ![일반 구성 - 웹 URL 옵션](../configuration-reference/general/assets/web-url-options.png){width="600" zoomable="yes"}

1. 완료되면 **[!UICONTROL Save Config]**&#x200B;을(를) 클릭합니다.

1. 작업 영역의 맨 위에 있는 메시지에서 **[!UICONTROL Cache Management]** 링크를 클릭합니다. 그런 다음 지침에 따라 캐시를 새로 고칩니다.

   ![캐시 관리 메시지](./assets/msg-cache-management.png)

## URL 문제 해결

구성 지침을 따른 후에도 일부 페이지가 비보안 URL(`http://`)을 사용하여 계속 제공되는 경우 다음을 수행하십시오.

- (비보안) 기본 URL을 보안 HTTPS URL로 변경합니다.
- 서버에서 `.htaccess` 파일(또는 부하 분산 장치)을 편집하여 비보안 URL이 보안 URL로 리디렉션되도록 합니다.

## 사용자 지정 관리자 URL 사용

[보안 모범 사례](https://experienceleague.adobe.com/docs/commerce-operations/implementation-playbook/best-practices/launch/security-best-practices.html)로서, Adobe에서는 기본 _관리_ 대신 고유한 관리 URL을 사용하거나 _백엔드_&#x200B;와 같은 일반적인 용어를 사용할 것을 권장합니다. 부적합한 행위자로부터 사이트를 직접 보호하지는 않지만 무단 액세스를 시도하는 스크립트에 대한 노출을 줄일 수 있습니다.

>[!NOTE]
>
>사용자 지정 관리자 URL을 구현하기 전에 호스팅 공급자에게 문의하십시오. 일부 호스팅 공급자는 방화벽 보호 규칙을 충족하기 위해 표준 URL이 필요합니다.

일반 설치에서 관리자 URL 및 경로는 기본 URL 바로 뒤에 옵니다. 관리 경로는 루트 아래에 있는 하나의 디렉토리입니다.

- **기본 기본 URL**: `http://yourdomain.com/magento/`
- **기본 관리자 경로**: `admin`
- **기본 관리자 URL 및 경로**: `http://yourdomain.com/magento/admin`

관리자 URL 및 경로를 다른 위치로 변경할 수 있지만, 모든 실수로 관리자에 대한 액세스 권한이 제거되므로 서버에서 수정해야 합니다.

>[!NOTE]
>
>서버에서 구성 파일을 편집하는 방법을 모르는 경우 사전 예방차원에서 관리자 URL을 직접 변경하지 마십시오. 클라우드 인프라에 배포된 Adobe Commerce 프로젝트의 경우 *Adobe Commerce on Cloud Infrastructure 안내서*&#x200B;의 [지침](https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/configure/env/stage/variables-admin.html?lang=en#admin-url)에 따라 관리 URL을 변경하십시오.

### 방법 1: 관리자의 변경

1. _관리자_ 사이드바에서 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**(으)로 이동합니다.

1. 왼쪽 패널에서 **[!UICONTROL Advanced]**&#x200B;을(를) 확장하고 **[!UICONTROL Admin]**&#x200B;을(를) 선택합니다.

1. **[!UICONTROL Admin Base URL]** 섹션에서 ![확장 선택기](../assets/icon-display-expand.png)를 확장합니다.

1. 사용자 지정 URL에 대한 구성 옵션을 설정합니다.

   ![고급 구성 - 관리자 기본 URL](../configuration-reference/advanced/assets/admin-admin-base-url.png){width="600" zoomable="yes"}

   필요한 경우 **[!UICONTROL Use system value]** 확인란의 선택을 취소하여 설정을 변경합니다.

   - **[!UICONTROL Use Custom Admin URL]**&#x200B;을(를) `Yes`(으)로 설정합니다.

   - **[!UICONTROL Custom Admin URL]** 입력: `http://yourdomain.com/magento/`

     >[!NOTE]
     >
     >관리자 URL은 동일한 Commerce 설치에 있어야 하며 상점 첫 글자와 동일한 문서 루트를 가져야 합니다.

   - **[!UICONTROL Custom Admin Path]**&#x200B;을(를) `Yes`(으)로 설정합니다.

   - **[!UICONTROL Custom Admin Path]**&#x200B;의 경우 사용자 지정 관리자 폴더 이름으로 사용할 경로를 입력하십시오.

     예: `sample_custom_admin`

1. 완료되면 **[!UICONTROL Save Config]**&#x200B;을(를) 클릭합니다.

1. 변경 사항이 저장되면 관리에서 로그아웃했다가 새 관리자 URL 및 경로를 사용하여 다시 로그인합니다.

### 방법 2: 서버 명령줄에서 관리 경로 변경

1. 텍스트 편집기에서 `app/etc/env.php` 파일을 열고 `backend` 섹션의 `frontName` 매개 변수의 값을 변경합니다. 그런 다음 파일을 저장합니다.

   소문자만 사용해야 합니다.

   >[!NOTE]
   >
   >   이 방법을 사용하면 관리 경로를 변경할 수 있지만 관리 URL은 변경할 수 없습니다.

   >[!TIP]
   >
   >클라우드 인프라의 Adobe Commerce의 경우 클라우드 UI에서 `ADMIN_URL` 변수를 사용하여 사용자 지정 관리 경로를 설정할 수 있습니다. _Cloud Infrastructure의 Commerce 안내서_&#x200B;에서 [관리 변수 항목](https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/configure/env/stage/variables-admin.html)을(를) 참조하십시오.

   - **기본 관리자 경로**

     ```php?start_inline=1
     'backend' => [
      'frontName' => 'admin'
     ],
     ```

   - **새 관리자 경로**

     ```php?start_inline=1
     'backend' => [
         'frontName' => 'backend'
     ],
     ```

1. 다음 방법 중 하나를 사용하여 캐시를 지웁니다.

   - _관리자_ 사이드바에서 **[!UICONTROL System]** > _[!UICONTROL Tools]_>**[!UICONTROL Cache Management]**(으)로 이동합니다.**[!UICONTROL Flush Magento Cache]**&#x200B;을(를) 클릭합니다.
   - 서버에서 다음을 실행합니다.

     ```bash
     php bin/magento cache:flush
     ```

   >[!NOTE]
   >
   >메서드 1을 사용하여 변경한 내용은 `app/etc/env.php` 파일에서 변경한 내용보다 우선 순위가 높습니다.

### 방법 3: Commerce CLI를 사용하여 관리 경로 변경

CLI `setup:config:set` 명령을 사용하여 관리 경로를 변경할 수 있습니다. 다음 예제에서는 `--backend-frontname` 옵션을 사용하여 Commerce 루트에서 새 관리 경로로 경로를 변경합니다.

```bash
bin/magento setup:config:set --backend-frontname="backend_front_name"
```

이 명령은 `app/etc/env.php` 파일의 `backend` > `frontName` 구성 옵션을 업데이트합니다.

## 기본 관리자 URL 및 관리자 경로 복원

잘못된 관리 URL 또는 관리 경로를 설정했고 백엔드에 대한 액세스 권한을 잃은 경우 명령줄에서 이를 수정하는 방법이 있습니다.

1. 기본 관리자 URL로 되돌리려면 다음 명령을 실행합니다.

   ```bash
   php bin/magento config:set admin/url/use_custom 0
   ```

1. 기본 관리 경로(메서드 2에 설명된 대로 `app/etc/env.php`에 설정됨)로 되돌리려면 이 명령을 실행합니다.

   ```bash
   php bin/magento config:set admin/url/use_custom_path 0
   ```

1. 다음 방법 중 하나를 사용하여 캐시를 지웁니다.

   - _관리자_ 사이드바에서 **[!UICONTROL System]** > _[!UICONTROL Tools]_>**[!UICONTROL Cache Management]**(으)로 이동합니다.**[!UICONTROL Flush Magento Cache]**&#x200B;을(를) 클릭합니다.
   - 서버에서 다음을 실행합니다.

     ```bash
     php bin/magento cache:flush
     ```


[1]: https://en.wikipedia.org/wiki/Transport_Layer_Security
[2]: https://en.wikipedia.org/wiki/HTTP_Strict_Transport_Security
