---
title: 보기 저장
description: 스토어 보기를 추가하고 편집하는 방법에 대해 알아봅니다.
exl-id: aa1f7f1c-a6d0-4ec2-83fe-15fb9646634a
feature: Site Management, System
source-git-commit: 370131cd73a320b04ee92fa9609cb24ad4c07eca
workflow-type: tm+mt
source-wordcount: '281'
ht-degree: 0%

---

# 보기 저장

저장소 보기는 일반적으로 저장소를 다른 로케일에서 사용할 수 있도록 하는 데 사용됩니다. 쇼핑객은 매장 헤더에서 언어 선택기를 사용하여 매장 보기를 변경할 수 있습니다.

![범위 - 여러 저장소 보기](./assets/scope-multiview.svg){width="550"}

## 스토어 보기 추가

1. _관리자_ 사이드바에서 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL All Stores]**(으)로 이동합니다.

   ![모든 스토어](./assets/stores-all.png){width="700" zoomable="yes"}

1. **[!UICONTROL Create Store View]**&#x200B;을(를) 클릭합니다.

   ![스토어 보기 만들기](./assets/create-store-view.png){width="600" zoomable="yes"}

1. **[!UICONTROL Store]**&#x200B;을(를) 이 보기의 상위 저장소로 설정합니다.

1. 이 스토어 보기에 대한 **[!UICONTROL Name]**&#x200B;을(를) 입력하십시오.

   저장소 헤더의 언어 선택기에 이름이 표시됩니다. 예: `Spanish`.

1. **[!UICONTROL Code]**&#x200B;의 경우 보기를 식별하는 코드(소문자)를 입력하십시오.

   예: `spanish`.

1. 보기를 활성화하려면 **[!UICONTROL Status]**&#x200B;을(를) `Enabled`(으)로 설정합니다.

1. (선택 사항) **[!UICONTROL Sort Order]** 숫자를 입력하여 이 보기가 다른 보기와 함께 나열된 순서를 결정합니다.

1. **[!UICONTROL Save Store View]**&#x200B;을(를) 클릭합니다.

## 스토어 보기 편집

보기 이름이 언어 선택기에 표시되기 때문에 기본 보기의 이름을 좀 더 설명적인 이름으로 변경할 수 있습니다. _이름_ 필드는 단순히 레이블이므로 쉽게 변경할 수 있습니다.

Adobe Commerce 또는 Magento Open Source 설치에 다중 사이트 또는 다중 스토어 설정이 있는 경우 `index.php` 파일에서 값이 참조되지 않았는지 확인하지 않고 스토어 코드 필드를 변경하지 마십시오. 파일을 검사할 수 있는 서버 액세스 권한이 없는 경우 개발자에게 도움을 요청하십시오.

| 필드 | 원래 값 | 업데이트된 값 |
| ----- | -------------- | ------------- |
| [!UICONTROL Name] | `Default Store View` | `English` |
| [!UICONTROL Code] | `default` | `english` |

{style="table-layout:auto"}

1. _관리자_ 사이드바에서 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL All Stores]**(으)로 이동합니다.

1. 그리드의 _[!UICONTROL Store View]_&#x200B;열에서 편집할 보기의 이름을 클릭합니다.

   기본 보기를 편집할 때 _[!UICONTROL Store]_&#x200B;및_[!UICONTROL Status]_ 필드를 사용할 수 없습니다.

   ![스토어 보기 - 기본 보기 편집](./assets/edit-store-view-info.png){width="600" zoomable="yes"}

1. 필요에 따라 다음 필드를 업데이트합니다.

   - **[!UICONTROL Store]**(기본이 아닌 보기만)
   - **[!UICONTROL Name]**
   - **[!UICONTROL Code]**(`index.php`에서 사용되지 않는 경우에만)
   - **[!UICONTROL Status]**(기본이 아닌 보기만)
   - **[!UICONTROL Sort Order]**

1. **[!UICONTROL Save Store View]**&#x200B;을(를) 클릭합니다.
