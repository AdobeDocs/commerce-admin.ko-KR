---
title: 마크업 태그
description: 스토어의 개체를 참조할 수 있는 코드 조각이 포함된 마크업 태그에 대해 알아봅니다.
exl-id: 0d6f5a9b-983d-473e-b641-0dceba40974f
feature: Page Content, Communications, Variables
source-git-commit: 64ccc2d5016e915a554c2253773bb50f4d33d6f4
workflow-type: tm+mt
source-wordcount: '1010'
ht-degree: 0%

---

# 마크업 태그

마크업 태그는 변수, URL, 이미지 또는 블록과 같은 저장소의 개체에 대한 상대 참조가 있는 코드 조각을 포함하는 지시문입니다. 마크업 태그는 편집기를 사용할 수 있는 모든 위치에서 사용할 수 있으며 의 HTML에 통합됩니다. [이메일](email-templates.md) 및 [뉴스레터](../merchandising-promotions/newsletter-template.md) 템플릿 및 기타 형식 [콘텐츠](../content-design/introduction.md#content).

마크업 태그는 중괄호로 묶이며 [위젯 도구]를 통해 생성하거나 HTML 컨텐츠에 직접 입력할 수 있습니다. 예를 들어 전체 경로를 페이지에 하드 코딩하는 대신 마크업 태그를 사용하여 스토어 URL을 나타낼 수 있습니다. 다음 예에 포함된 마크업 태그는 다음과 같습니다.

{{$include /help/_includes/directives-caution.md}}

## 사용자 지정 변수

변수 마크업 태그를 사용하여 [사용자 지정 변수](variables-custom.md) 이메일 템플릿, 블록, 뉴스레터 및 콘텐츠 페이지로.

\{\{CustomVar code= &quot;my_custom_variable&quot;}}

## URL 저장

저장소 URL 마크업 태그는 웹 사이트의 기본 URL을 나타내며 도메인 이름을 포함하여 전체 URL의 첫 번째 부분을 대체하는 데 사용됩니다. 이 마크업 태그는 두 가지 버전이 있습니다. 하나는 저장소로 직접 이동하고 다른 하나는 슬래시(`/`)을 클릭하여 제품에서 사용할 수 있습니다.

\{\{store url=&#39;apparel/shoes/womens&#39;}}

## 미디어 URL

Dynamic media URL 마크업 태그는 CDN(Content Delivery Network)에 저장된 이미지의 위치와 파일 이름을 나타냅니다. 태그를 사용하여 페이지, 블록, 배너 또는 이메일 템플릿에 이미지를 배치할 수 있습니다.

\{\{media url=&#39;shoe-sale.jpg&#39;}}

## 블록 ID

블록 ID 마크업 태그는 사용하기 쉬운 태그 중 하나이며, 블록을 CMS 페이지에 직접 배치하는 데 사용하거나 다른 블록 내에 중첩할 수도 있습니다. 이 기술을 사용하여 다양한 프로모션 또는 언어에 대한 블록을 수정할 수 있습니다. 블록 ID 마크업 태그는 해당 식별자로 블록을 참조합니다.

\{\{block id=&#39;block-id&#39;}}

## 템플릿 태그

템플릿 태그는 PHTML 템플릿 파일을 참조하며 CMS 페이지나 정적 블록에 블록을 표시하는 데 사용할 수 있습니다. 다음 예제의 코드를 페이지나 블록에 추가하여 Contact Us 양식을 표시할 수 있습니다.

\{\{block class=&quot;Magento\Contact\Block\ContactForm&quot; name=&quot;contactForm&quot; template=&quot;Magento_Contact::form.phtml&quot;}}

다음 예제의 코드는 페이지 또는 블록에 추가하여 카테고리 ID별로 특정 카테고리의 제품 목록을 표시할 수 있습니다.

\{\{block type=&quot;catalog/product_list&quot; category_id=&quot;22&quot; template=&quot;catalog/product/list.phtml&quot;}}

## 위젯 코드

위젯 도구를 사용하여 제품 목록을 표시하거나 제품 ID를 기반으로 특정 제품 페이지로 이동하는 링크와 같은 복잡한 링크를 삽입할 수 있습니다. 생성되는 코드는 블록 참조, 코드 모듈의 위치 및 대응하는 PHTML 템플릿을 포함한다. 코드가 생성되면 한 위치에서 다른 위치로 복사하여 붙여넣을 수 있습니다.

다음 예제의 코드를 페이지나 블록에 추가하여 새 제품 목록을 표시할 수 있습니다.

\{\{widget type=&quot;catalog/product_widget_new&quot; display_type=&quot;new_products&quot; products_count=&quot;10&quot; template=&quot;catalog/product/widget/new/content/new_grid.phtml&quot;}}

다음 예제의 코드는 페이지 또는 블록에 추가하여 제품 ID별로 특정 제품에 대한 링크를 표시할 수 있습니다.

\{\{widget type=&quot;catalog/product_widget_link&quot; anchor_text=&quot;내 제품 링크&quot; title=&quot;내 제품 링크&quot; template=&quot;catalog/product/widgetlink/link_block.phtml&quot; id_path=&quot;product/31&quot;}}

## 링크의 마크업 태그 사용

HTML 앵커 태그와 함께 마크업 태그를 사용하고 스토어의 모든 페이지에 직접 연결할 수 있습니다. 링크는 콘텐츠 페이지, 블록 또는 이메일 및 뉴스레터 템플릿에 통합할 수 있습니다. 이 기술을 사용하여 이미지를 특정 페이지에 연결할 수도 있습니다.

### 1단계. 대상 URL 식별

가능하면 연결할 페이지로 이동한 다음 브라우저의 주소 표시줄에서 전체 URL을 복사합니다. 필요한 URL 부분은 다음 뒤에 옵니다. `.com/`. 그렇지 않으면 링크 대상으로 사용할 CMS 페이지에서 URL 키를 복사합니다.

#### 카테고리 페이지의 전체 URL

`https://mystore.com/apparel/shoes/womens`
`https://mystore.com/apparel/shoes/womens.html`

#### 제품 페이지의 전체 URL

`https://mystore.com/apparel/shoes/womens/nine-west-pump`
`https://mystore.com/apparel/shoes/womens/nine-west-pump.html`

#### CMS 페이지의 전체 URL

`https://mystore.com/about-us`

### 2단계. URL에 마크업 추가

스토어 URL 태그는 웹 사이트의 기본 URL을 나타내며 도메인 이름 및 을 포함하여 스토어 URL의 HTTP 주소 부분에 대한 대용으로 사용됩니다 `.com`. 태그에는 달성하려는 결과에 따라 사용할 수 있는 두 가지 버전이 있습니다.

`store direct_url` - 페이지로 바로 연결됩니다.

`store url` - 추가 참조를 경로로 추가할 수 있도록 끝에 슬래시를 배치합니다.

다음 예제에서 URL 키는 작은 따옴표로 묶여 있고 전체 마크업 태그는 중괄호로 묶여 있습니다. 앵커 태그와 함께 사용할 경우 마크업 태그는 앵커의 큰따옴표 안에 배치됩니다. 혼동을 피하기 위해 중첩된 각 따옴표에 대해 작은 따옴표와 큰 따옴표를 번갈아 사용할 수 있습니다.

전체 URL로 시작하는 경우 HTTP 주소(`http://` 또는 `https://`) URL의 일부(다음을 통해 포함) `.com/`. 그 자리에 여는 작은 따옴표를 통해 위에 있는 저장소 URL 마크업 태그를 입력합니다.

#### URL 마크업 태그 저장

`https://mystore.com/apparel/shoes/womens`

`{{store url='apparel/shoes/womens'}}`

그렇지 않으면 저장 URL 마크업 태그의 첫 번째 부분을 입력하고 이전에 복사한 URL 키 또는 경로를 붙여넣습니다.

### URL 키로 URL 마크업 태그 저장

`{{store url=`

마크업 태그를 완료하려면 닫는 큰따옴표와 큰중괄호를 입력합니다.

`{{store url='apparel/shoes/womens'}}`

### 3단계. 앵커 태그를 완료합니다

대상 URL 대신 마크업 태그를 사용하여 앵커 태그 내에 완료된 마크업 태그를 래핑합니다. 그런 다음 링크 텍스트와 닫는 앵커 태그를 추가합니다.

#### 앵커 태그의 마크업

\&lt;a href=&quot;\{\{markup tag goes here}}&quot;>텍스트 연결\&lt;/a>

링크를 표시할 CMS 페이지, 블록, 배너 또는 이메일 템플릿의 코드에 완료된 앵커 태그를 붙여넣습니다.

### 마크업을 사용한 전체 링크

\&lt;a href=&quot;\{\{store url=&amp;#39;apparel/shoes&amp;#39;}}&quot;> 신발 판매\&lt;/a>
