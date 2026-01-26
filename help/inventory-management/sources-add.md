---
title: 인벤토리 소스 추가
description: 창고, 오프라인 매장, 물류 센터 또는 직송업체와 같은 위치에 대한 소스를 만드는 방법에 대해 알아봅니다.
exl-id: 1bff9986-8722-4fb5-ac83-41de82325f7b
feature: Inventory, Products
source-git-commit: cace9d1de00955494d8bc607c017778ff7df4806
workflow-type: tm+mt
source-wordcount: '855'
ht-degree: 0%

---

# 소스 추가

사용자 정의 소스를 사용하여 여러 위치의 재고 및 주문 이행을 관리합니다. 창고, 오프라인 매장, 물류 센터, 직송업체 등 각 위치에 대한 출처를 생성합니다. 제품당 소스 할당 및 수량 업데이트

기본 Source을 편집하는 경우 이름 및 코드를 제외한 모든 구성을 편집할 수 있습니다. 단일 소스 판매자의 위치에 일치하는 정보를 추가하는 것이 좋습니다.

## 인벤토리 소스 추가

1. _관리자_ 사이드바에서 **[!UICONTROL Stores]** > _[!UICONTROL Inventory]_>**[!UICONTROL Sources]**(으)로 이동합니다.

1. **[!UICONTROL Add New Source]**&#x200B;을(를) 클릭합니다.

   ![소스 관리](assets/inventory-sources.png)

1. ![ 섹션에서 ](../assets/icon-display-expand.png)확장 선택기&#x200B;**[!UICONTROL General]**&#x200B;를 확장하고 다음을 수행합니다.

   - 인벤토리 원본을 식별하려면 고유한 **[!UICONTROL Name]**&#x200B;을(를) 입력하십시오.

   - 고유한 **[!UICONTROL Code]**&#x200B;을(를) 입력하십시오.

     이 코드는 대문자와 소문자, 숫자, 대시 및 밑줄을 지원합니다. 코드는 스톡 할당 및 데이터 내보내기/가져오기 시 사용되는 고유 ID입니다.

   - 이 인벤토리 원본을 사용할 준비가 되면 **[!UICONTROL Is Enabled]**&#x200B;을(를) `Yes`(으)로 설정하십시오.

   - 빠른 참조 또는 추가 세부 정보를 보려면 이 위치에 대한 간략한 **[!UICONTROL Description]**&#x200B;을(를) 입력하십시오.

   - **[!UICONTROL Latitude]** 및 **[!UICONTROL Longitude]**&#x200B;의 경우 협업공간 위치의 GPS(Global Positioning System) 좌표를 입력하십시오.

     [Google 지도](https://www.google.com/maps)를 사용하여 GPS 좌표를 찾으려면 검색 상자에 주소를 입력하십시오. 맵에서 마커를 마우스 오른쪽 단추로 클릭하고 **[!UICONTROL What's here?]**&#x200B;을(를) 선택합니다. GPS 좌표는 거리 주소 아래의 세부 정보 상자에 나타납니다.

     ![일반 소스 옵션](assets/inventory-source-general.png)

   - 이 인벤토리 원본이 픽업 위치인 경우 **[!UICONTROL Use as Pickup Location]**&#x200B;을(를) `Yes`(으)로 설정하십시오.

     기본 Source은 매장 픽업 주문의 픽업 위치로 사용할 수 없습니다.

1. ![ 섹션에서 ](../assets/icon-display-expand.png)확장 선택기&#x200B;**[!UICONTROL Contact Info]**&#x200B;를 확장하고 다음을 수행합니다.

   - **[!UICONTROL Contact Name]**&#x200B;의 경우 해당 위치에 기본 연락처의 전체 이름을 입력하십시오.

   - 해당 위치에 연결할 **[!UICONTROL Email]** 주소를 입력하십시오.

   - **[!UICONTROL Phone]**&#x200B;의 경우 지역 번호와 전화 번호를 입력하십시오.

   - **[!UICONTROL Fax]**&#x200B;에 사용할 수 있는 경우 팩스의 지역 번호와 전화 번호를 입력하십시오.

     ![연락처 정보](assets/inventory-source-contact-info.png)

1. ![ 섹션에서 ](../assets/icon-display-expand.png)확장 선택기&#x200B;**[!UICONTROL Address Data]**&#x200B;를 확장하고 다음을 수행합니다.

   - **[!UICONTROL Country]** 선택.

   - **[!UICONTROL State/Province]**&#x200B;의 경우 주 또는 시/도의 표준 약어를 입력하십시오.

   - **[!UICONTROL City]** 입력.

   - 실제 **[!UICONTROL Street]** 주소를 입력하십시오.

   - **[!UICONTROL Postcode]**&#x200B;의 경우 ZIP 또는 우편번호를 입력하십시오.

     ![주소 데이터](assets/inventory-source-address.png)

1. 이전 단계에서 원본을 픽업 위치로 설정한 경우 ![ 섹션에서 ](../assets/icon-display-expand.png)확장 선택기&#x200B;**[!UICONTROL Pickup Location]**&#x200B;를 확장하고 위치에 대한 자세한 정보를 제공합니다.

   - 픽업 위치의 **[!UICONTROL Frontend Name]**&#x200B;을(를) 입력하십시오.

   - 픽업 위치의 **[!UICONTROL Frontend Description]**&#x200B;을(를) 입력하십시오. 이 텍스트 상자를 사용하여 매장 시간, 다른 랜드마크와 상대적인 위치 또는 고객이 올바른 픽업 위치를 선택하는 데 도움이 되는 기타 유용한 정보를 표시할 수 있습니다.

     ![픽업 위치](assets/inventory-pickup-location.png)

   소스를 픽업 위치로 사용할 때 전자 메일 알림을 구성하는 방법에 대한 자세한 내용은 [구성 참조 안내서](../configuration-reference/sales/sales-emails.md)의 _판매 전자 메일_&#x200B;을(를) 참조하십시오.

1. 작업을 저장하려면 다음 중 하나를 수행합니다.

   - 작업을 저장하고 편집을 계속하려면 **[!UICONTROL Save & Continue]**&#x200B;을(를) 클릭합니다.

   - 작업을 저장하고 [소스 관리] 페이지로 돌아가려면 아래쪽 화살표(![메뉴 화살표](../assets/icon-menu-down-arrow-red.png))를 클릭하고 **[!UICONTROL Save & Close]**&#x200B;을(를) 선택합니다.

   - 현재 원본 레코드에 작업을 저장하고 새 원본을 입력하려면 **[!UICONTROL Save & New]**&#x200B;을(를) 선택하세요.

## 단추 막대

| 단추 | 설명 |
|--|--|
| [!UICONTROL Back] | 소스 관리 페이지로 돌아갑니다. |
| [!UICONTROL Reset] | 양식의 모든 필드를 마지막 저장 시 해당 값으로 복원합니다. |
| [!UICONTROL Save & Continue] | 모든 변경 내용을 저장하고 추가 편집을 위해 양식을 열어 둡니다. 추가 옵션을 보려면 아래쪽 화살표를 클릭하십시오. <br/>**[!UICONTROL Save & Close]**- 현재 레코드에 대한 변경 내용을 저장하고, 양식을 닫은 다음 [소스 관리] 페이지로 돌아갑니다.<br/>**[!UICONTROL Save & New]** - 변경 내용을 저장하고 현재 레코드를 닫은 다음 새 양식을 엽니다. |

## 필드 설명

| 필드 | 설명 |
|--|--|
| **[!UICONTROL General]** | |
| [!UICONTROL Name] | (필수) 관리자의 인벤토리 소스를 식별하는 고유한 이름입니다. |
| [!UICONTROL Code] | (필수) 시스템에서 재고 출처를 식별하는 데 사용되는 고유한 영숫자 코드입니다. 코드를 공백 없이 대문자 또는 소문자 및/또는 숫자로 입력하십시오. 필요한 경우 공백 대신 하이픈이나 밑줄을 사용할 수 있습니다. 소스를 만든 후에는 코드를 편집할 수 없습니다. 소스를 주식에 할당하고 제품 데이터를 내보내기 및/또는 가져올 때 사용되는 고유 ID입니다. |
| [!UICONTROL Is Enabled] | 인벤토리 소스를 사용할 수 있는지 여부를 결정합니다. 옵션: 예 / 아니요 |
| [!UICONTROL Description] | 재고 출처 위치에 대한 간략한 설명. 관리자 사용자에게 유용한 세부 정보를 포함합니다. |
| [!UICONTROL Latitude] | GPS용 인벤토리 소스의 위도 좌표를 지정합니다. 필요에 따라 더하기 또는 빼기 기호 앞에 숫자로 값을 입력합니다. 차수 기호와 글자는 허용되지 않습니다. 예: Latitude 32.7555 |
| [!UICONTROL Longitude] | GPS용 인벤토리 소스의 경도 좌표를 지정합니다. 필요에 따라 더하기 또는 빼기 기호 앞에 숫자로 값을 입력합니다. 차수 기호와 글자는 허용되지 않습니다. 예: `-97.3308` |
| **[!UICONTROL Contact Info]** | |
| [!UICONTROL Contact Name] | 재고 출처 위치에 있는 기본 담당자의 이름입니다. |
| [!UICONTROL Email] | 기본 연락처의 이메일입니다. |
| [!UICONTROL Phone] | 원하는 형식을 사용하여 기본 연락처의 지역 번호 및 전화 번호입니다. 예: `(123) 456-7890` 또는 `123-456-7890` |
| [!UICONTROL Fax] | 기본 연락처의 지역 번호 및 팩스 번호입니다. |
| **[!UICONTROL Address Data]** | |
| [!UICONTROL Country] | (필수) 재고 출처가 있는 국가입니다. |
| [!UICONTROL State/Province] | 인벤토리 소스가 있는 주 또는 시/도입니다. |
| [!UICONTROL City] | 인벤토리 소스가 있는 도시입니다. |
| [!UICONTROL Street] | 인벤토리 소스의 거리 주소입니다. |
| [!UICONTROL Postcode] | (필수) 재고 출처의 우편 번호입니다. |
| **[!UICONTROL Pickup Location]** | |
| [!UICONTROL Frontend Name] | 상점 앞에 표시되는 소스의 픽업 위치 이름. |
| [!UICONTROL Frontend Description] | 상점 앞에 표시되는 소스의 픽업 위치에 대한 설명. 첨부된 이미지를 포함할 수 있습니다. |
