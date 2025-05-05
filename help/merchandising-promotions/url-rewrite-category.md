---
title: 범주 URL 재작성
description: 카테고리 URL 재작성을 사용하여 링크를 Commerce 스토어에 있는 다른 카테고리의 URL로 리디렉션하는 방법에 대해 알아봅니다.
exl-id: fc18f472-4aa8-4203-ade9-7ca576689d61
feature: Categories, Configuration
badgePaas: label="PaaS만" type="Informative" url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="Adobe Commerce 온 클라우드 프로젝트(Adobe 관리 PaaS 인프라) 및 온프레미스 프로젝트에만 적용됩니다."
source-git-commit: 6d782e3aafa7460a0e0d5ca07a2bde2ae371a9ea
workflow-type: tm+mt
source-wordcount: '700'
ht-degree: 0%

---

# 범주 URL 재작성

범주가 카탈로그에서 제거된 경우 범주 재작성을 사용하여 링크를 스토어에 있는 다른 범주의 URL로 리디렉션할 수 있습니다. _target_ / _원래 요청_ 또는 _리디렉션 대상_ / _리디렉션 대상_&#x200B;을 고려하십시오. 사람들이 검색 엔진 또는 오래된 링크에서 이전 페이지로 계속 이동할 수 있지만 리디렉션으로 인해 저장소가 새 대상으로 전환됩니다.

스토어에 대해 [자동 리디렉션](url-redirect-product-automatic.md)을 사용하도록 설정한 경우 범주 [URL 키](../catalog/catalog-urls.md)를 변경할 때 다시 작성할 필요가 없습니다.

{{url-rewrite-skip}}

## 1단계. 다시 작성 계획

실수를 방지하려면 _리디렉션 대상_ 경로와 _리디렉션 대상_ 경로를 기록하고 URL 키와 접미사를 포함하십시오(해당하는 경우).

확실하지 않은 경우 스토어에서 각 카테고리 페이지를 열고 브라우저의 주소 표시줄에서 경로를 복사합니다.

**예:**

`gear/backpacks-and-bags.html`(으)로 리디렉션

리디렉션 원본: `gear/bags.html`

## 2단계. 다시 작성 만들기

{{url-rewrite-params}}

1. _관리자_ 사이드바에서 **[!UICONTROL Marketing]** > _[!UICONTROL SEO & Search]_>**[!UICONTROL URL Rewrites]**(으)로 이동합니다.

1. 계속하기 전에 다음을 수행하여 요청 경로를 사용할 수 있는지 확인합니다.

   - **[!UICONTROL Request Path]** 열 상단의 검색 필터에 리디렉션할 범주의 URL 키를 입력하고 **[!UICONTROL Search]**&#x200B;을(를) 클릭합니다.

   - 페이지에 대한 리디렉션 레코드가 여러 개 있는 경우 해당 저장소 보기와 일치하는 레코드를 찾아 편집 모드로 리디렉션 레코드를 엽니다.

   - 오른쪽 상단에서 **[!UICONTROL Delete]**&#x200B;을(를) 클릭합니다. 메시지가 표시되면 **[!UICONTROL OK]**&#x200B;을(를) 클릭하여 확인합니다.

1. _[!UICONTROL URL Rewrites]_&#x200B;페이지로 돌아오면&#x200B;**[!UICONTROL Add URL Rewrite]**&#x200B;을(를) 클릭합니다.

1. **[!UICONTROL Create URL Rewrite]**&#x200B;을(를) `For category`(으)로 설정하고 리디렉션의 대상인 트리에서 대상 범주를 선택합니다.

   ![URL 다시 작성 - 범주 선택](./assets/url-rewrite-category-choose.png){width="700" zoomable="yes"}

1. _URL 다시 작성_ 섹션에서 다음을 수행합니다.

   - 저장소가 여러 개 있는 경우 다시 쓰기가 적용되는 **[!UICONTROL Store]**&#x200B;을(를) 선택하십시오.

   - **[!UICONTROL Request Path]**&#x200B;에 대해 고객이 요청하는 범주의 URL 키를 입력하십시오. _다음에서 리디렉션_ 범주입니다.

     >[!NOTE]
     >
     >지정한 저장소에 대한 요청 경로는 고유해야 합니다. 동일한 요청 경로를 사용하는 리디렉션이 이미 있는 경우 리디렉션을 저장하려고 하면 오류가 표시됩니다. 리디렉션을 만들려면 먼저 이전 리디렉션을 삭제해야 합니다.

   - **[!UICONTROL Redirect]**&#x200B;을(를) 다음 중 하나로 설정합니다.

      - `Temporary (302)`
      - `Permanent (301)`

   - 참조용으로 재작성에 대한 간단한 설명을 입력합니다.

   ![범주에 대한 URL 다시 작성 추가](./assets/url-rewrite-for-category.png){width="700" zoomable="yes"}

1. 리디렉션을 저장하기 전에 다음을 검토하십시오.

   - 왼쪽 위 모서리에 있는 링크에 대상 카테고리의 이름이 표시됩니다.
   - 요청 경로에 원래 _리디렉션 원본_ 범주에 대한 경로가 포함되어 있습니다.

1. 완료되면 **[!UICONTROL Save]** 단추를 클릭하십시오.

   새 범주 다시 작성은 URL 다시 작성 그리드 맨 위에 나타납니다.

## 3단계. 결과 테스트

1. 스토어의 홈페이지로 이동합니다.

1. 다음 중 하나를 수행합니다.

   - 원래 _리디렉션 원본_ 범주로 이동합니다.
   - 브라우저의 주소 표시줄에서 저장소 URL 바로 뒤에 원래 _리디렉션 원본_ 범주의 경로를 입력하고 **[!UICONTROL Enter]**&#x200B;을(를) 누릅니다.

   원래 범주 요청 대신 새 대상 범주가 나타납니다.

## 필드 설명

| 필드 | 설명 |
|--- |--- |
| [!UICONTROL Create URL Rewrite] | 다시 작성 유형을 나타냅니다. 다시 작성을 만든 후에는 유형을 변경할 수 없습니다. 옵션: `Custom` / `For category` / `For product` / `For CMS page` |
| [!UICONTROL Request Path] | 리디렉션할 카테고리입니다. 구성에 따라 요청 경로에 .html 또는 .htm 접미사와 상위 카테고리가 포함될 수 있습니다. 요청 경로는 고유해야 하며 다른 리디렉션에서 사용할 수 없습니다. 요청 경로가 존재한다는 오류가 표시되면 기존 리디렉션을 삭제하고 다시 시도하십시오. |
| [!UICONTROL Target Path] | 리디렉션 대상을 가리키기 위해 시스템에서 사용하는 내부 경로입니다. 대상 경로가 회색으로 표시되어 편집할 수 없습니다. |
| [!UICONTROL Redirect] | 리디렉션 유형을 결정합니다. 옵션: <br/>**[!UICONTROL No]**- 리디렉션이 지정되지 않았습니다. 많은 작업에서 이 유형의 리디렉션 요청을 만듭니다. 예를 들어 카테고리에 제품을 추가할 때마다 각 스토어 보기에 대해 `No` 유형의 리디렉션이 만들어집니다.<br/>**[!UICONTROL Temporary (302)]** - 검색 엔진에 제한된 시간 동안 다시 쓰기를 나타냅니다. 검색 엔진은 일반적으로 임시 재작성에 대한 페이지 등급 정보를 유지하지 않습니다. <br/>**[!UICONTROL Permanent (301)]**- 검색 엔진에 다시 쓰기가 영구적임을 나타냅니다. 검색 엔진은 일반적으로 영구적인 재작성을 위해 페이지 등급 정보를 유지합니다. |
| [!UICONTROL Description] | 내부 참조를 위해 다시 쓰는 목적에 대해 설명합니다. |

{style="table-layout:auto"}
