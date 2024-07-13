---
title: 콘텐츠 페이지 URL 재작성
description: 컨텐츠 페이지 URL 재작성을 사용하여 링크를 Commerce 스토어에 있는 다른 컨텐츠 페이지의 URL로 리디렉션하는 방법에 대해 알아봅니다.
exl-id: e29c45fd-cf25-4b51-a8ae-9e188dc2a61c
feature: Page Content, Configuration
source-git-commit: eb0fe395020dbe2e2496aba13d2f5c2bf2d0fc27
workflow-type: tm+mt
source-wordcount: '605'
ht-degree: 0%

---

# 콘텐츠 페이지 URL 재작성

시작하기 전에 리디렉션이 수행할 작업을 정확히 이해했는지 확인하십시오. _target_ / _소스_ 또는 _리디렉션 대상_ / _리디렉션 대상_&#x200B;을 고려하십시오. 사람들이 검색 엔진 또는 오래된 링크에서 이전 페이지로 계속 이동할 수 있지만 리디렉션으로 인해 저장소가 새 대상으로 전환됩니다.

![URL 재작성 - CMS 페이지](./assets/url-rewrite-cms-page.png){width="700" zoomable="yes"}

## 1단계. 다시 작성 계획

실수를 방지하려면 _리디렉션 대상_ 페이지와 _리디렉션 대상_ 페이지의 URL 키를 기록하십시오.

확실하지 않은 경우 스토어의 각 페이지를 열고 브라우저의 주소 표시줄에서 경로를 복사합니다.

### CMS 페이지 경로

`new-page`(으)로 리디렉션

리디렉션 원본: `old-page`

## 2단계. 다시 작성 만들기

{{url-rewrite-params}}

1. _관리자_ 사이드바에서 **[!UICONTROL Marketing]** > _[!UICONTROL SEO & Search]_>**[!UICONTROL URL Rewrites]**(으)로 이동합니다.

1. 계속하기 전에 다음을 수행하여 요청 경로를 사용할 수 있는지 확인합니다.

   - **[!UICONTROL Request Path]** 열 위쪽에 있는 검색 필터에 리디렉션할 페이지의 URL 키를 입력하고 **[!UICONTROL Search]**&#x200B;을(를) 클릭합니다.

   - 페이지에 대한 리디렉션 레코드가 여러 개 있는 경우 해당 스토어 보기와 일치하는 레코드를 찾아 편집 모드로 엽니다.

   - 오른쪽 상단에서 **[!UICONTROL Delete]**&#x200B;을(를) 클릭합니다. 메시지가 표시되면 **[!UICONTROL OK]**&#x200B;을(를) 클릭하여 확인합니다.

1. URL 재작성 페이지로 돌아가려면 **[!UICONTROL Add URL Rewrite]**&#x200B;을(를) 클릭합니다.

1. **[!UICONTROL Create URL Rewrite]**&#x200B;을(를) `for CMS page`(으)로 설정합니다.

1. 그리드에서 새 대상 페이지를 찾아 편집 모드로 엽니다.

   ![URL 다시 쓰기 추가 - CMS 페이지용](./assets/url-rewrite-cms-page-add.png){width="700" zoomable="yes"}

1. URL 재작성 정보에서 다음을 수행합니다.

   - 저장소 보기가 여러 개인 경우 다시 쓰기가 적용되는 **[!UICONTROL Store]**&#x200B;을(를) 선택하십시오.

   - **[!UICONTROL Request Path]**&#x200B;에 대해 고객이 요청하는 원본 페이지의 URL 키를 입력하십시오. _다음에서 리디렉션_ 페이지입니다.

     >[!NOTE]
     >
     >지정된 저장소에 대해 요청 경로가 고유해야 합니다. 동일한 요청 경로를 사용하는 리디렉션이 이미 있는 경우 리디렉션을 저장하려고 하면 오류가 표시됩니다. 리디렉션을 만들려면 먼저 이전 리디렉션을 삭제해야 합니다.

   - **[!UICONTROL Redirect]**&#x200B;을(를) 다음 중 하나로 설정합니다.

      - `Temporary (302)`
      - `Permanent (301)`

   - 참조용으로 재작성에 대한 간단한 설명을 입력합니다.

   ![URL 다시 작성 정보](./assets/url-rewrite-cms-page-information.png){width="600" zoomable="yes"}

1. 리디렉션을 저장하기 전에 다음을 검토하십시오.

   - 왼쪽 위 모서리에 있는 링크에 대상 페이지의 이름이 표시됩니다.
   - 요청 경로에 원래 _리디렉션 원본_ 페이지의 경로가 포함되어 있습니다.

1. 완료되면 **[!UICONTROL Save]**&#x200B;을(를) 클릭합니다.

   목록 맨 위의 그리드에 새 다시 쓰기가 나타납니다.

## 3단계. 결과 테스트

1. 스토어의 홈페이지로 이동합니다.

1. 다음 중 하나를 수행합니다.

   - 원래 _리디렉션 위치_ 페이지로 이동합니다.
   - 브라우저의 주소 표시줄에 저장소 URL 바로 뒤에 원래 _리디렉션 원본_ 페이지의 이름을 입력하고 **Enter**&#x200B;을 누릅니다.

   원래 페이지 요청 대신 새 대상 페이지가 나타납니다.

## 필드 설명

| 필드 | 설명 |
|--- |--- |
| [!UICONTROL Create URL Rewrite] | 다시 작성 유형을 나타냅니다. 다시 작성을 만든 후에는 유형을 변경할 수 없습니다. 옵션: `Custom` / `For category` / `For product` / `For CMS page` |
| [!UICONTROL Request Path] | 리디렉션할 CMS 페이지입니다. 요청 경로는 고유해야 하며 다른 리디렉션에서 사용할 수 없습니다. 요청 경로가 존재한다는 오류 메시지가 표시되면 기존 리디렉션을 삭제하고 다시 시도하십시오. |
| [!UICONTROL Target Path] | 시스템에서 대상을 지정하는 데 사용하는 내부 경로입니다. 대상 경로가 회색으로 표시되어 편집할 수 없습니다. |
| [!UICONTROL Redirect] | 리디렉션 유형을 결정합니다. 옵션: <br/>**[!UICONTROL No]**- 리디렉션이 지정되지 않았습니다.<br/>**[!UICONTROL Temporary (302)]** - 검색 엔진에 제한된 시간 동안 다시 쓰기를 나타냅니다. 검색 엔진은 일반적으로 임시 재작성에 대한 페이지 등급 정보를 유지하지 않습니다. <br/>**[!UICONTROL Permanent (301)]**- 검색 엔진에 다시 쓰기가 영구적임을 나타냅니다. 검색 엔진은 일반적으로 영구적인 재작성을 위해 페이지 등급 정보를 유지합니다. |
| [!UICONTROL Description] | 내부 참조를 위해 다시 쓰는 목적에 대해 설명합니다. |

{style="table-layout:auto"}
