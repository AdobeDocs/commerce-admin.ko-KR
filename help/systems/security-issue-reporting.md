---
title: 보안 문제 보고
description: 보안 연구자가 사이트에 대한 보안 문제를 보고하는 데 사용할 수 있는 연락처 정보 및 보안 관련 링크를 구성하는 방법에 대해 알아봅니다.
exl-id: 47b95505-51a3-4b7a-a4e3-dbc4b0045797
role: Admin
feature: Configuration, Security
source-git-commit: 64ccc2d5016e915a554c2253773bb50f4d33d6f4
workflow-type: tm+mt
source-wordcount: '269'
ht-degree: 0%

---

# 보안 문제 보고

`security.txt` 파일에는 보안 연구자가 사이트에 대한 보안 문제를 보고하는 데 사용할 수 있는 연락처 정보 및 보안 관련 링크가 포함되어 있습니다. 보안 정보가 시간이 지남에 따라 변경되는 경우 `security.txt` 파일의 정보가 최신 상태인지 확인하십시오.

**_security.txt를 구성하려면:_**

1. _관리자_ 사이드바에서 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**(으)로 이동합니다.

1. _[!UICONTROL Security]_아래의 왼쪽 패널에서&#x200B;**[!UICONTROL Security.txt]**을(를) 클릭합니다.

1. _[!UICONTROL General]_섹션에서&#x200B;**[!UICONTROL Enable]**을(를) `Yes`(으)로 설정합니다.

   ![일반 보안 구성](../configuration-reference/security/assets/txt-general.png){width="600" zoomable="yes"}

1. _[!UICONTROL Contact Information]_에서 다음을 입력하십시오.

   - 스토어에 대한 보안 문제를 관리하는 사람의 이메일 주소 및 전화번호.

   - 저장소 **[!UICONTROL Contact Page]**&#x200B;의 URL입니다. 이 페이지는 저장소 보안 연락처 목록이거나 _연락처_ 페이지일 수 있습니다.

   ![연락처 정보 구성](../configuration-reference/security/assets/txt-contact-info.png){width="600" zoomable="yes"}

1. _[!UICONTROL Other Information]_에서 다음을 입력하십시오.

   - 공개 **[!UICONTROL Encryption]** 키의 URL. 예: `https://example.com/pgp-key.txt`

   - 보안 연구원이 스토어를 대신하여 노력한 공로를 인정받는 **[!UICONTROL Acknowledgments]** 페이지의 URL입니다.

   - 보안 관련 통신용 **[!UICONTROL Preferred Languages]**&#x200B;입니다. 지원되는 각 언어에 대한 표준 두 문자 [언어 코드](https://en.wikipedia.org/wiki/List_of_ISO_639-1_codes)을(를) 쉼표로 구분하여 입력하십시오. 예를들어, 영어, 스페인어, 프랑스어를 지정하려면 `en, es, fr`을(를) 입력합니다. 지정한 모든 언어는 표시 순서에 관계없이 우선 순위가 동일합니다.

   - 스토어의 보안 관련 취업 기회를 나열하는 **[!UICONTROL Hiring]** 페이지의 URL입니다.

   - 보안 **[!UICONTROL Policy]** 페이지의 URL.

   - 서버에 저장된 디지털 **[!UICONTROL Signature]** 파일의 URL. 예: `https://mystore.com/.well-known/security.txt.sig`

   서버의 CLI(명령줄 인터페이스)에서 디지털 서명을 설정해야 합니다. 자세한 내용은 GitHub에서 [Security.txt](https://github.com/magento/security-package/blob/1.0-develop/Securitytxt/README.md)를 참조하세요.

   ![기타 정보](../configuration-reference/security/assets/txt-other-info.png){width="600" zoomable="yes"}

1. 완료되면 **[!UICONTROL Save Config]**&#x200B;을(를) 클릭합니다.
