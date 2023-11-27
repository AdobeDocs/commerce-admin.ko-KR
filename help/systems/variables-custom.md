---
title: 사용자 지정 변수 추가
description: 사용자 지정 변수를 만들고 페이지, 블록 및 제품 콘텐츠에 삽입하는 방법을 알아봅니다.
exl-id: 8233518a-abcf-4889-b75b-4aa503c7cebb
role: Admin, User
feature: System, Variables, Page Content, Communications
source-git-commit: 64ccc2d5016e915a554c2253773bb50f4d33d6f4
workflow-type: tm+mt
source-wordcount: '341'
ht-degree: 2%

---

# 사용자 지정 변수 추가

비즈니스의 특정 요구 사항을 충족하기 위해 사용자 지정 변수를 만들어 에 삽입할 수 있습니다 [페이지](../content-design/pages.md), [블록](../content-design/blocks.md), 및 [이메일 템플릿](email-templates.md). 을(를) 클릭할 때 표시되는 허용된 변수 목록 _변수 삽입_ 단추에 두 항목이 모두 포함됨 [미리 정의됨](variables-predefined.md) 및 사용자 지정 변수와 함께 사용됩니다. 특정 이메일 템플릿에 사용할 수 있는 변수 목록은 템플릿과 연결된 데이터에 의해 결정됩니다. 다음을 참조하십시오. [변수 참조](variables-reference.md) 자주 사용하는 이메일 템플릿 및 관련 변수 목록입니다.

![사용자 지정 변수](./assets/variables-custom.png){width="600" zoomable="yes"}

>[!NOTE]
>
>이메일 및 뉴스레터 템플릿에서는 사전 정의된 변수나 사용자 지정 변수만 사용할 수 있습니다.

## 1단계: 사용자 지정 변수 만들기

1. 다음에서 _관리자_ 사이드바, 이동 **[!UICONTROL System]** > _[!UICONTROL Other Settings]_>**[!UICONTROL Custom Variables]**.

1. 클릭 **[!UICONTROL Add New Variable]**.

1. 다음에 대한 식별자 입력: **[!UICONTROL Variable Code]**, 공백 없이 모든 소문자 사용.

   필요한 경우 밑줄 문자 또는 하이픈을 사용하여 공백을 나타낼 수 있습니다. For example: `my_custom_variable`

1. 입력 **[!UICONTROL Variable Name]**: 내부 참조에 사용됩니다. For example: `My Custom Variable`

1. 변수와 연결된 값을 입력하려면 다음 중 하나를 수행합니다.

   - 대상 **[!UICONTROL Variable HTML Value]**&#x200B;단순 HTML 태그로 서식이 지정된 변수 값을 입력합니다. For example:

     `<b>This formatted content appears in place of the variable.</b>`

   - 대상 **[!UICONTROL Variable Plain Value]**&#x200B;을 누르고 서식 지정 없이 변수 값을 일반 텍스트로 입력합니다. For example:

     `This unformatted content appears in place of the variable.`

   >[!TIP]
   >
   >공간이 더 필요한 경우 텍스트 상자의 오른쪽 아래 모서리를 끕니다.

   ![새 사용자 지정 변수](./assets/variable-custom-add.png){width="600" zoomable="yes"}

1. 완료되면 다음을 클릭하십시오. **[!UICONTROL Save]**.

## 2단계: 콘텐츠에 사용자 지정 변수 삽입

사용 [!DNL Page Builder] 을 클릭하여 사용자 지정 변수를 삽입합니다.

1. 변수를 콘텐츠에 추가하려는 페이지, 블록, 카테고리 또는 제품을 엽니다.

1. 확장 ![확장 선택기](../assets/icon-display-expand.png) 다음 **[!UICONTROL Content]** 섹션.

1. 클릭 **[!UICONTROL Edit with Page Builder]**.

1. 왼쪽 패널에서 **[!UICONTROL Elements]** 다음 중 하나를 수행합니다.

   - 변수를 삽입할 기존 텍스트 영역을 클릭합니다.

   - 새 항목 드래그 **[!UICONTROL Text]** 스테이지의 객체로 변경되었습니다.

1. 편집기 도구 모음의 맨 오른쪽에서 ( ![변수 삽입](./assets/editor-btn-insert-variable.png) )을 클릭하여 변수를 삽입합니다.

   ![[!DNL Page Builder] 스테이지 및 패널](./assets/variable-custom-pagebuilder-stage.png){width="600" zoomable="yes"}

1. 목록에서 삽입하려는 사용자 지정 변수를 선택하고 **[!UICONTROL Insert Variable]**.

   ![새 사용자 지정 변수](./assets/variable-custom-insert-select.png){width="600" zoomable="yes"}

   변수 식별자는 편집기에 자리 표시자로 표시됩니다.

   ![[!DNL Page Builder] 단계 - 변수 자리 표시자](./assets/pagebuilder-variable-inserted.png){width="600" zoomable="yes"}

1. 완료되면 다음을 클릭하십시오. **[!UICONTROL Save]**.
