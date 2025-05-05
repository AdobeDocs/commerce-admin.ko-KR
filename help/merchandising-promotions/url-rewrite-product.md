---
title: 제품 URL 재작성
description: 제품 URL 재작성을 사용하여 링크를 Commerce 스토어에 있는 다른 제품의 URL로 리디렉션하는 방법에 대해 알아봅니다.
exl-id: 42b28ff7-e148-44f2-b6b4-63a38458e752
feature: Products, Configuration
badgePaas: label="PaaS만" type="Informative" url="https://experienceleague.adobe.com/ko/docs/commerce/user-guides/product-solutions" tooltip="Adobe Commerce 온 클라우드 프로젝트(Adobe 관리 PaaS 인프라) 및 온프레미스 프로젝트에만 적용됩니다."
source-git-commit: 6d782e3aafa7460a0e0d5ca07a2bde2ae371a9ea
workflow-type: tm+mt
source-wordcount: '897'
ht-degree: 0%

---

# 제품 URL 재작성

시작하기 전에 리디렉션에서 수행할 작업을 정확히 이해했는지 확인하십시오. _target_ / _원래 요청_ 또는 _리디렉션 대상_ / _리디렉션 대상_&#x200B;을 고려하십시오. 사람들이 검색 엔진 또는 오래된 링크에서 이전 페이지로 계속 이동할 수 있지만 리디렉션으로 인해 저장소가 새 대상으로 전환됩니다.

스토어에 대해 [자동 리디렉션](url-redirect-product-automatic.md)을 사용하도록 설정한 경우 제품 [URL 키](../catalog/catalog-urls.md)를 변경할 때 다시 작성하지 않아도 됩니다.

{{url-rewrite-skip}}

## 1단계. 다시 작성 계획

실수를 방지하려면 _리디렉션 대상_ 경로와 _리디렉션 대상_ 경로를 기록하고 URL 키와 접미사를 포함하십시오(해당하는 경우).

확실하지 않은 경우 스토어의 각 제품 페이지를 열고 브라우저의 주소 표시줄에서 경로를 복사합니다. 제품 리디렉션을 만들 때 [범주 경로](../catalog/catalog-urls.md)을 포함하거나 제외할 수 있습니다. 이 예제에서는 카테고리 경로 없이 제품 리디렉션을 만듭니다.

### 범주 경로가 있는 제품

`gear/bags/impulse-duffle.html`(으)로 리디렉션

리디렉션 원본: `gear/bags/overnight-duffle.html`

### 범주 경로가 없는 제품

`impulse-duffle.html`(으)로 리디렉션

리디렉션 원본: `overnight-duffle.html`

## 2단계. 다시 작성 만들기

{{url-rewrite-params}}

1. _관리자_ 사이드바에서 **[!UICONTROL Marketing]** > _[!UICONTROL SEO & Search]_>**[!UICONTROL URL Rewrites]**(으)로 이동합니다.

1. 계속하기 전에 다음을 수행하여 요청 경로를 사용할 수 있는지 확인합니다.

   - **[!UICONTROL Request Path]** 열 위쪽에 있는 검색 필터에 리디렉션할 페이지의 URL 키를 입력하고 **[!UICONTROL Search]**&#x200B;을(를) 클릭합니다.

   - 페이지에 대한 리디렉션 레코드가 여러 개 있는 경우 해당 스토어 보기와 일치하는 레코드를 찾아 편집 모드로 엽니다.

   - 오른쪽 상단에서 **[!UICONTROL Delete]**&#x200B;을(를) 클릭합니다. 메시지가 표시되면 **[!UICONTROL OK]**&#x200B;을(를) 클릭하여 확인합니다.

1. URL 재작성 페이지의 오른쪽 상단 모서리에서 **URL 재작성 추가**&#x200B;를 클릭합니다.

1. **[!UICONTROL Create URL Rewrite]**&#x200B;을(를) `For product`(으)로 설정합니다.

1. 그리드에서 리디렉션의 대상(대상)인 제품을 찾은 다음 행을 클릭합니다.

   ![URL 재작성 - 제품](./assets/url-rewrite-product.png){width="700" zoomable="yes"}

1. 범주 트리 아래에서 **[!UICONTROL Skip Category Selection]**&#x200B;을(를) 클릭합니다.

   이 예제에서 리디렉션은 카테고리를 포함하지 않습니다.

   ![제품 URL 다시 작성 - 범주 선택 건너뛰기](./assets/url-rewrite-skip-category-selection.png){width="600" zoomable="yes"}

   제품에 대한 URL 재작성 추가 페이지는 왼쪽 상단 모서리에 대상에 대한 링크를 표시하고 대상 경로 필드에 변경할 수 없는 경로의 시스템 버전이 표시됩니다. 처음에는 리디렉션 경로 필드에 대상 경로도 표시됩니다.

   - 저장소 보기가 여러 개인 경우 **[!UICONTROL Store]**&#x200B;을(를) 다시 쓰기가 적용되는 보기로 설정하십시오. 그렇지 않으면 각 보기에 대해 다시 작성됩니다.

   - **[!UICONTROL Request Path]**&#x200B;의 경우 원본 제품 요청의 URL 키와 접미사(해당하는 경우)를 입력하여 기본값을 바꾸십시오. 계획 단계에서 식별한 _리디렉션 원본_ 제품입니다.

     >[!NOTE]
     >
     >지정한 저장소에 대한 요청 경로는 고유해야 합니다. 동일한 요청 경로를 사용하는 리디렉션이 이미 있는 경우 리디렉션을 저장하려고 하면 오류가 표시됩니다. 리디렉션을 만들려면 먼저 이전 리디렉션을 삭제해야 합니다.

   - **[!UICONTROL Redirect Type]**&#x200B;을(를) 다음 중 하나로 설정합니다.

      - `Temporary (302)`
      - `Permanent (301)`

   - 참조를 위해 간단한 **[!UICONTROL Description]**&#x200B;의 다시 작성을 입력하십시오.

   ![제품 URL 다시 작성 - 정보](./assets/url-rewrite-product-permanent-301.png){width="600" zoomable="yes"}

1. 리디렉션을 저장하기 전에 다음을 검토하십시오.

   - 왼쪽 위 모서리에 있는 링크에 대상 제품의 이름이 표시됩니다.
   - 요청 경로에 원래 _리디렉션 원본_ 제품에 대한 경로가 포함되어 있습니다.

1. 완료되면 **[!UICONTROL Save]**&#x200B;을(를) 클릭합니다.

   이제 새 제품 다시 쓰기가 URL 다시 쓰기 표의 맨 위에 나타납니다.

## 3단계. 결과 테스트

1. 스토어의 홈페이지로 이동합니다.

1. 다음 중 하나를 수행합니다.

   - 원래 _리디렉션 원본_ 제품 요청 페이지로 이동합니다.
   - 브라우저의 주소 표시줄에서 스토어 URL 바로 뒤에 원래 _리디렉션 원본_ 제품의 경로를 입력하고 **Enter**&#x200B;을 누릅니다.

   원래 제품 요청 대신 새 타겟 제품이 나타납니다.

## 필드 설명

| 필드 | 설명 |
|--- |--- |
| [!UICONTROL Create URL Rewrite] | 다시 작성 유형을 나타냅니다. 다시 작성을 만든 후에는 유형을 변경할 수 없습니다. 옵션: `Custom` / `For category` / `For product` / `For CMS page` |
| [!UICONTROL Request Path] | 리디렉션할 제품입니다. 구성에 따라 요청 경로에 `.html` 또는 `.htm` 접미사 및 범주가 포함될 수 있습니다. 요청 경로는 고유해야 하며 다른 리디렉션에서 사용할 수 없습니다. 요청 경로가 존재한다는 오류가 표시되면 기존 리디렉션을 삭제하고 다시 시도하십시오. |
| [!UICONTROL Target Path] | 리디렉션 대상을 가리키기 위해 시스템에서 사용하는 내부 경로입니다. 대상 경로가 회색으로 표시되어 편집할 수 없습니다. |
| [!UICONTROL Redirect] | 리디렉션 유형을 결정합니다. 옵션: <br/>**[!UICONTROL No]**- 리디렉션이 지정되지 않았습니다. 많은 작업에서 이 유형의 리디렉션 요청을 만듭니다. 예를 들어 카테고리에 제품을 추가할 때마다 각 스토어 보기에 대해 `No` 유형의 리디렉션이 만들어집니다.<br/>**[!UICONTROL Temporary (302)]** - 검색 엔진에 제한된 시간 동안 다시 쓰기를 나타냅니다. 검색 엔진은 일반적으로 임시 재작성에 대한 페이지 등급 정보를 유지하지 않습니다. <br/>**[!UICONTROL Permanent (301)]**- 검색 엔진에 다시 쓰기가 영구적임을 나타냅니다. 검색 엔진은 일반적으로 영구적인 재작성을 위해 페이지 등급 정보를 유지합니다. |
| [!UICONTROL Description] | 내부 참조를 위해 다시 쓰는 목적에 대해 설명합니다. |

{style="table-layout:auto"}

## 여러 URL 재작성

다음 단계를 사용하여 여러 제품 또는 모든 제품에 대한 URL 재작성을 동시에 빠르게 업데이트할 수 있습니다.

1. _관리자_ 사이드바에서 **[!UICONTROL Catalog]** > **[!UICONTROL Products]**(으)로 이동합니다.

1. URL 재작성을 업데이트할 모든 제품을 선택합니다.

1. _[!UICONTROL Actions]_&#x200B;에서&#x200B;**[!UICONTROL Update attributes]**&#x200B;을(를) 선택하여 여러 번 또는 모든 다시 쓰기를 업데이트합니다.

1. _[!UICONTROL PRODUCTS INFORMATION]_&#x200B;에서&#x200B;**[!UICONTROL Websites]**&#x200B;탭을 클릭합니다.

1. _[!UICONTROL Add Product To Websites]_&#x200B;섹션에서 URL 재작성을 복원할 모든 웹 사이트를 선택합니다.

1. 업데이트할 준비가 되면 **[!UICONTROL Save]**&#x200B;을(를) 클릭합니다.

>[!NOTE]
>
>선택한 모든 제품을 선택한 웹 사이트로 읽고 URL 재작성을 다시 생성합니다.

![특성 업데이트 - 여러 URL 다시 쓰기 업데이트](./assets/url-rewrites-update.png){width="600" zoomable="yes"}
