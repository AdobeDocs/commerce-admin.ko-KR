---
title: 보안 문제 보고
description: 보안 연구자가 사이트에 대한 보안 문제를 보고하는 데 사용할 수 있는 연락처 정보 및 보안 관련 링크를 구성하는 방법에 대해 알아봅니다.
exl-id: 47b95505-51a3-4b7a-a4e3-dbc4b0045797
role: Admin
feature: Configuration, Security
source-git-commit: 64ccc2d5016e915a554c2253773bb50f4d33d6f4
workflow-type: tm+mt
source-wordcount: '282'
ht-degree: 1%

---

# 보안 문제 보고

다음 `security.txt` 파일에는 보안 연구자가 사이트에 대한 보안 문제를 보고하는 데 사용할 수 있는 연락처 정보 및 보안 관련 링크가 포함되어 있습니다. 보안 정보가 시간이 지남에 따라 변경되는 경우 `security.txt` 파일이 최신 상태입니다.

**_security.txt를 구성하려면:_**

1. 다음에서 _관리자_ 사이드바, 이동 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. 아래의 왼쪽 패널에서 _[!UICONTROL Security]_, 클릭&#x200B;**[!UICONTROL Security.txt]**.

1. 다음에서 _[!UICONTROL General]_섹션, 설정&#x200B;**[!UICONTROL Enable]**끝 `Yes`.

   ![일반 보안 구성](../configuration-reference/security/assets/txt-general.png){width="600" zoomable="yes"}

1. 아래 _[!UICONTROL Contact Information]_를 클릭하고 다음을 입력합니다.

   - 스토어에 대한 보안 문제를 관리하는 사람의 이메일 주소 및 전화번호.

   - 스토어 URL **[!UICONTROL Contact Page]**. 이 페이지는 저장소 보안 연락처 목록이거나 _연락처_ 페이지를 가리키도록 업데이트하는 중입니다.

   ![연락처 정보 구성](../configuration-reference/security/assets/txt-contact-info.png){width="600" zoomable="yes"}

1. 아래 _[!UICONTROL Other Information]_를 클릭하고 다음을 입력합니다.

   - 공개 URL **[!UICONTROL Encryption]** 키. For example: `https://example.com/pgp-key.txt`

   - 의 URL **[!UICONTROL Acknowledgments]** 보안 연구원이 스토어를 대신하여 노력한 공로를 인정받는 페이지입니다.

   - 사용자 **[!UICONTROL Preferred Languages]** 보안 관련 커뮤니케이션. 표준 2문자 입력 [언어 코드](https://en.wikipedia.org/wiki/List_of_ISO_639-1_codes) 지원되는 각 언어에 대해 쉼표로 구분합니다. 예를 들어, 영어, 스페인어 및 프랑스어를 지정하려면 `en, es, fr`. 지정한 모든 언어는 표시 순서에 관계없이 우선 순위가 동일합니다.

   - 의 URL **[!UICONTROL Hiring]** 스토어의 보안 관련 취업 기회를 나열하는 페이지입니다.

   - 보안 URL **[!UICONTROL Policy]** 페이지를 가리키도록 업데이트하는 중입니다.

   - 디지털 URL **[!UICONTROL Signature]** 서버에 저장된 파일입니다. For example: `https://mystore.com/.well-known/security.txt.sig`

   서버의 CLI(명령줄 인터페이스)에서 디지털 서명을 설정해야 합니다. 자세한 내용은 다음을 참조하십시오. [Security.txt](https://github.com/magento/security-package/blob/1.0-develop/Securitytxt/README.md) GitHub에서.

   ![기타 정보](../configuration-reference/security/assets/txt-other-info.png){width="600" zoomable="yes"}

1. 완료되면 다음을 클릭하십시오. **[!UICONTROL Save Config]**.
