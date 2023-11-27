---
title: 보기 저장
description: 스토어 보기를 추가하고 편집하는 방법에 대해 알아봅니다.
exl-id: aa1f7f1c-a6d0-4ec2-83fe-15fb9646634a
feature: Site Management, System
source-git-commit: 370131cd73a320b04ee92fa9609cb24ad4c07eca
workflow-type: tm+mt
source-wordcount: '281'
ht-degree: 2%

---

# 보기 저장

저장소 보기는 일반적으로 저장소를 다른 로케일에서 사용할 수 있도록 하는 데 사용됩니다. 쇼핑객은 매장 헤더에서 언어 선택기를 사용하여 매장 보기를 변경할 수 있습니다.

![범위 - 여러 스토어 보기](./assets/scope-multiview.svg){width="550"}

## 스토어 보기 추가

1. 다음에서 _관리자_ 사이드바, 이동 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL All Stores]**.

   ![모든 스토어](./assets/stores-all.png){width="700" zoomable="yes"}

1. 클릭 **[!UICONTROL Create Store View]**.

   ![스토어 보기 만들기](./assets/create-store-view.png){width="600" zoomable="yes"}

1. 설정 **[!UICONTROL Store]** (이 보기의 상위 스토어로)를 참조하십시오.

1. 입력 **[!UICONTROL Name]** 이 스토어 조회수.

   저장소 헤더의 언어 선택기에 이름이 표시됩니다. For example: `Spanish`.

1. 대상 **[!UICONTROL Code]**&#x200B;보기를 식별하는 코드(소문자)를 입력합니다.

   For example: `spanish`.

1. 보기를 활성화하려면 를 설정합니다. **[!UICONTROL Status]** 끝 `Enabled`.

1. (선택 사항) **[!UICONTROL Sort Order]** 다른 보기와 함께 이 보기가 나열되는 순서를 결정하는 번호입니다.

1. 클릭 **[!UICONTROL Save Store View]**.

## 스토어 보기 편집

보기 이름이 언어 선택기에 표시되기 때문에 기본 보기의 이름을 좀 더 설명적인 이름으로 변경할 수 있습니다. 다음 _이름_ 필드는 단순히 레이블이며 쉽게 변경할 수 있습니다.

Adobe Commerce 또는 Magento Open Source 설치 시 다중 사이트 또는 다중 스토어 설정이 있는 경우 다음 위치에서 값이 참조되지 않았는지 확인하지 않고 스토어 코드 필드를 변경하지 마십시오 `index.php` 파일. 파일을 검사할 수 있는 서버 액세스 권한이 없는 경우 개발자에게 도움을 요청하십시오.

| 필드 | 원래 값 | 업데이트된 값 |
| ----- | -------------- | ------------- |
| [!UICONTROL Name] | `Default Store View` | `English` |
| [!UICONTROL Code] | `default` | `english` |

{style="table-layout:auto"}

1. 다음에서 _관리자_ 사이드바, 이동 **[!UICONTROL Stores]** >  _[!UICONTROL Settings]_>**[!UICONTROL All Stores]**.

1. 다음에서 _[!UICONTROL Store View]_그리드의 열에서 편집할 뷰의 이름을 누릅니다.

   기본 보기를 편집할 때 _[!UICONTROL Store]_및_[!UICONTROL Status]_ 필드를 사용할 수 없습니다.

   ![저장소 보기 - 기본 보기 편집](./assets/edit-store-view-info.png){width="600" zoomable="yes"}

1. 필요에 따라 다음 필드를 업데이트합니다.

   - **[!UICONTROL Store]** (기본값이 아닌 보기만)
   - **[!UICONTROL Name]**
   - **[!UICONTROL Code]** (에서 사용되지 않는 경우에만 해당) `index.php`)
   - **[!UICONTROL Status]** (기본값이 아닌 보기만)
   - **[!UICONTROL Sort Order]**

1. 클릭 **[!UICONTROL Save Store View]**.
