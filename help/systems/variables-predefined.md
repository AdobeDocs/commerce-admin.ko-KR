---
title: 사전 정의된 변수 사용
description: 사전 정의된 변수와 이메일 템플릿에 변수를 추가하는 방법에 대해 알아봅니다.
exl-id: 01e909c4-c932-4262-9f33-bd2740a6355f
role: Admin, User
feature: System, Variables, Page Content, Communications
source-git-commit: 64ccc2d5016e915a554c2253773bb50f4d33d6f4
workflow-type: tm+mt
source-wordcount: '385'
ht-degree: 0%

---

# 사전 정의된 변수 사용

[미리 정의됨](variables-predefined.md) 변수를 사용하면 쉽게 개인화할 수 있습니다. [이메일](email-templates.md) 및 [뉴스레터](../merchandising-promotions/newsletters.md) 템플릿 및 기타 유형의 콘텐츠. 허용 목록 [미리 정의됨](variables-predefined.md) 변수는 변수 삽입 단추를 클릭하면 나타납니다. 다음 이미지에 표시된 대로 특정 이메일 템플릿에 사용할 수 있는 변수 목록은 템플릿과 연결된 데이터에 의해 결정됩니다. 다음을 참조하십시오. [변수 참조](variables-reference.md) 자주 사용하는 이메일 템플릿 및 관련 변수 목록입니다.

![이메일 템플릿에 대해 사전 정의된 변수](./assets/email-template-new-pickup-order-predefined-variables.png){width="700" zoomable="yes"}

## 이메일 템플릿에 변수 추가

1. 다음에서 _관리자_ 사이드바, 이동 **[!UICONTROL Marketing]** > _[!UICONTROL Communications]_>**[!UICONTROL Email Templates]**.

1. 다음 중 하나를 수행합니다.

   - 기존 템플릿에 변수를 추가하려면 목록에서 템플릿을 클릭하여 편집 모드로 엽니다.

   - 새 템플릿에서 변수를 사용하려면 **[!UICONTROL Add New Template]** 기본 템플릿 코드를 사용자 지정합니다. 다음을 참조하십시오 [메시지 템플릿](email-template-custom.md#message-templates).

1. 아래 _[!UICONTROL Load default template]_, 을(를) 선택합니다.**[!UICONTROL Template]**사용자 지정할 수 있습니다.

1. 템플릿을 적용하려면 **[!UICONTROL Load Template]**.

   다음 _[!UICONTROL Currently used for]_필드에는 템플릿에 대한 구성 경로가 표시됩니다. 다음_[!UICONTROL Template Subject]_ 및 _[!UICONTROL Template Content]_선택한 템플릿에 상대적으로 자동으로 생성됩니다.

   - **[!UICONTROL Template Subject]** - 이 텍스트는 이메일의 제목 줄에 표시됩니다.

   - **[!UICONTROL Template Content]** - 이 텍스트는 보낸 이메일의 전체 콘텐츠에 표시됩니다.

   ![이메일 템플릿 콘텐츠](./assets/email-template-content.png){width="600" zoomable="yes"}

1. 입력 **[!UICONTROL Template Name]**.

1. 목록: [미리 정의됨](variables-predefined.md) 이 이메일 템플릿에 사용할 수 있는 변수, 클릭 **[!UICONTROL Insert Variable]**.

   템플릿에 삽입할 변수를 결정합니다. 그런 다음 을 클릭합니다. _닫기_ (X) 오른쪽 위 모서리에서 볼 수 있습니다. (나중에 다시 돌아옵니다.)

1. 템플릿의 모형을 보려면 **[!UICONTROL Preview Template]** 을 클릭합니다.

   새 탭에서 미리보기가 열리면 다른 콘텐츠와 관련하여 변수를 배치할 위치를 결정합니다. 그런 다음 원본 탭으로 돌아가서 계속합니다.

   ![템플릿 미리 보기](./assets/email-template-new-pickup-order-preview.png){width="600" zoomable="yes"}

1. 다음에서 **[!UICONTROL Template Content]** 상자를 클릭하고 변수를 표시할 위치에 삽입 포인터를 놓은 다음 **[!UICONTROL Insert Variable...]**.

1. 사용 가능한 변수 목록에서 템플릿에 삽입할 변수를 클릭합니다.

1. 완료되면 다음을 클릭하십시오. **[!UICONTROL Save Template]**.

## 템플릿을 일반 텍스트로 변환

1. 편집 모드에서 템플릿을 엽니다.

1. 페이지 맨 위에서 을 클릭합니다. **[!UICONTROL Convert to Plain Text]**.

1. 태그를 제거하라는 메시지가 표시되면 **[!UICONTROL OK]**.

1. 일반 텍스트 버전을 저장하려면 **[!UICONTROL Save Template]**.

## HTML 버전 복원

1. 페이지 맨 위에서 을 클릭합니다. **[!UICONTROL Return HTML Version]**.

1. 템플릿의 HTML 버전을 저장하려면 을 클릭합니다. **[!UICONTROL Save Template]**.
