---
title: '[!UICONTROL Security] &gt; [!UICONTROL Security.txt]'
description: Commerce 관리자의 [!UICONTROL Security] &gt; [!UICONTROL Security.txt] 페이지에서 구성 설정을 검토하십시오.
exl-id: 26385864-cfd8-456b-91b2-bf5d019c09e1
feature: Configuration, Security, Site Management
source-git-commit: b710c0368dc765e3bf25e82324bffe7fb8192dbf
workflow-type: tm+mt
source-wordcount: '349'
ht-degree: 0%

---

# [!UICONTROL Security] > [!UICONTROL Security.txt]

이러한 구성 설정 변경에 대한 자세한 내용은 [보안 문제 보고](../../systems/security-issue-reporting.md)를 참조하십시오.

{{config}}

## [!UICONTROL General]

![일반](./assets/txt-general.png)<!-- zoom -->

| 필드 | [범위](../../getting-started/websites-stores-views.md#scope-settings) | 설명 |
|--- |--- |--- |
| [!UICONTROL Enable] | 웹 사이트 | 활성화되면 보안 연구자가 잠재적인 취약성을 보고하는 데 필요한 정보가 포함된 `security.txt` 파일이 저장됩니다. 옵션:<br />**`Yes`**- _연락처 정보_ 및 _기타 정보_ 섹션에 입력한 정보를 기반으로 `security.txt` 파일을 만듭니다.<br />**`No`** - (기본값) `security.txt` 파일을 만들지 않습니다. |

{style="table-layout:auto"}

## [!UICONTROL Contact information]

![연락처 정보](./assets/txt-contact-info.png)<!-- zoom -->

| 필드 | [범위](../../getting-started/websites-stores-views.md#scope-settings) | 설명 |
|--- |--- |--- |
| [!UICONTROL Email] | 웹 사이트 | 보안 보고서를 보낼 수 있는 이메일 주소입니다. |
| [!UICONTROL Phone] | 웹 사이트 | 보안 문제를 보고하는 데 사용할 수 있는 전화번호. |
| [!UICONTROL Contact Page] | 웹 사이트 | 보안 연락처를 나열하는 사이트의 페이지 URL 또는 _연락처_ 페이지입니다. 예: <br/>`https://mystore.com/security-contact.html`<br/>`https://mystore.com/contact/` |

{style="table-layout:auto"}

## [!UICONTROL Other information]

![기타 정보](./assets/txt-other-info.png)<!-- zoom -->

| 필드 | [범위](../../getting-started/websites-stores-views.md#scope-settings) | 설명 |
|--- |--- |--- |
| [!UICONTROL Encryption] | 웹 사이트 | 보안 연구자가 암호화된 통신을 전송하는 데 사용할 수 있는 암호화 키의 위치를 가리키는 URL입니다. _**이 필드에 암호화 키를 입력하지 마십시오.**_ <br/><br/>신뢰할 수 있는 원본에서 가져온 키인지 확인하는 것은 연구자의 책임입니다. 연구자들은 그 키가 디지털 서명을 생성하는데 사용된 것과 같다고 가정해서는 안 된다. 예: <br />웹 서버의 OpenPGP 키 - `https://mystore.com/pgp-key.txt` |
| [!UICONTROL Acknowledgments] | 웹 사이트 | 보안 연구자가 인정되는 스토어의 페이지를 가리키는 URL(예: `https://mystore.com/hall-of-fame.html`). 향후 공격을 방지하려면 취약성 문제에 대한 구체적인 정보를 밝히지 않고 일반적인 설명만 포함하십시오. 예:<br />다음 연구자에게 감사드립니다.<br />(yyyy/mm/dd) Justin Thyme - SQL 삽입 |
| [!UICONTROL Preferred Languages] | 웹 사이트 | 최소 하나 이상의 기본 보안 보고 언어를 지정합니다. 여러 개의 두 문자 [언어 코드](https://en.wikipedia.org/wiki/List_of_ISO_639-1_codes)는 쉼표로 구분하십시오. 지정한 모든 언어의 우선 순위는 동일합니다. 예를들어, 영어, 스페인어, 프랑스어를 지정하려면 `en, es, fr`을(를) 입력합니다. |
| [!UICONTROL Hiring] | 웹 사이트 | 보안 관련 작업 위치를 나열하는 사이트의 페이지 URL. 예: `https://mystore.com/jobs.html` |
| [!UICONTROL Policy] | 웹 사이트 | 보안 정책 및 취약성 보고 사례를 설명하는 페이지의 URL입니다. 예: `https://mystore.com/security-reporting.html` 기본값: `https://mystore.com/security` |
| [!UICONTROL Signature] | 웹 사이트 | 디지털 서명 파일에 대한 링크입니다. 디지털 서명은 명령줄에서 생성되어야 하며 서버의 `.well-known` 폴더에 저장됩니다. 자세한 내용은 GitHub의 [Security.txt](https://github.com/magento/security-package/blob/1.0-develop/Securitytxt/README.md)를 참조하십시오. 예: `https://mystore.com/.well-known/security.txt.sig` |

{style="table-layout:auto"}
