---
title: 세율 데이터 업데이트
description: 내보내기 및 가져오기 작업을 사용하여 스토어의 세율을 업데이트하는 방법에 대해 알아봅니다.
exl-id: a3ef718d-b296-41d7-a1b8-ae8274da71b6
feature: Taxes, Data Import/Export
source-git-commit: 64ccc2d5016e915a554c2253773bb50f4d33d6f4
workflow-type: tm+mt
source-wordcount: '609'
ht-degree: 0%

---

# 세율 데이터 업데이트

여러 주에서 사업을 진행하고 다량의 제품을 출하하는 경우, 세율을 수동으로 입력하는 것은 매우 시간이 많이 소요될 수 있습니다. 우편 번호로 세율을 다운로드하여 Commerce으로 가져오는 것이 더 빠르고 효율적입니다. 다음 예에서는 신뢰할 수 있는 소스에서 다운로드한 주별 세율 집합을 가져오는 방법을 보여 줍니다. Avalara는 미국의 모든 우편번호에 대해 무료로 다운로드할 수 있는 [세율 표](https://www.avalara.com/taxrates/en/download-tax-tables.html)를 제공합니다.

>[!NOTE]
>
>판매 자동화와 세금 규정 준수 및 보고에 관심이 있는 경우 [Commerce 파트너](https://solutionpartners.adobe.com/s/directory/?solution=commerce) 사이트에서 Commerce에서 신뢰하는 옵션을 찾을 수 있습니다.

## 1단계: Commerce 세율 데이터 내보내기

1. _관리자_ 사이드바에서 **[!UICONTROL System]** > _[!UICONTROL Data Transfer]_>**[!UICONTROL Import/Export Tax Rates]**(으)로 이동합니다.

1. **[!UICONTROL Export Tax Rates]**&#x200B;을(를) 클릭합니다.

1. 웹 브라우저의 다운로드 위치에서 파일을 찾습니다.

1. 파일을 저장하고 스프레드시트로 엽니다.

   이 예제에서는 [!DNL OpenOffice Calc]을(를) 사용합니다.

   내보낸 Commerce 세율 데이터에는 다음 열이 포함되어 있습니다.
   - 코드
   - 국가
   - 시/도
   - Zip/Post 코드
   - 비율
   - 범위 시작
   - 범위 종료
   - 각 스토어 보기에 대한 열

   ![내보낸 데이터 - 세율](./assets/data-exported-tax-rates.png){width="500" zoomable="yes"}

1. 스프레드시트의 두 번째 인스턴스에서 새 세율 데이터를 열어 나란히 볼 수 있습니다.

1. 새 세율 데이터에서 데이터를 가져오기 전에 스토어에서 설정해야 할 추가 세율 데이터를 기록합니다.

   예를 들어, 캘리포니아에 대한 세율 데이터에는 다음도 포함됩니다.

   - `TaxRegionName`
   - `CombinedRate`
   - `StateRate`
   - `CountyRate`
   - `CityRate`
   - `SpecialRate`

   추가 [세금 구역 및 세율](../stores-purchase/tax-zones-rates.md)을(를) 가져오려면 먼저 저장소 관리자로부터 이를 정의하고 필요에 따라 [세금 규칙](../stores-purchase/tax-rules.md)을(를) 업데이트해야 합니다. 그런 다음 데이터를 내보내고 참조에 사용할 수 있도록 텍스트 편집기에서 파일을 엽니다. 그러나 이 예를 단순하게 유지하기 위해 표준 세율 열만 가져옵니다.

## 2단계: 가져오기 데이터 준비

두 개의 스프레드시트가 나란히 열려 있습니다. 하나는 Commerce 내보내기 파일 구조를 포함하고 다른 하나는 가져오려는 새 세율 데이터를 포함합니다.

1. 새 세율 데이터를 사용하여 스프레드시트에서 작업할 위치를 만들려면 맨 오른쪽에 빈 열을 필요한 수만큼 삽입하여 Commerce 내보내기 파일의 데이터를 추가합니다. 잘라내기 및 붙여넣기 기능을 사용하여 데이터를 추가한 다음 Commerce 내보내기 데이터 파일의 순서와 일치하도록 열을 다시 정렬합니다.

1. Commerce 내보내기 데이터와 일치하도록 열 헤더 이름을 변경합니다.

1. 데이터가 없는 열을 삭제합니다.

   그렇지 않으면 가져오기 파일의 구조가 원래 Commerce 내보내기 데이터와 일치해야 합니다.

1. 파일을 저장하기 전에 아래로 스크롤하여 세율 열에 숫자 데이터만 포함되어 있는지 확인합니다.

   세율 열에 있는 모든 텍스트는 데이터를 가져올 수 없습니다.

1. 준비된 데이터를 .CSV 파일로 저장합니다.

   메시지가 표시되면 쉼표를 필드 구분 기호로 사용하고 큰따옴표를 텍스트 구분 기호로 사용하는지 확인합니다. **[!UICONTROL OK]**&#x200B;을(를) 클릭합니다.

## 3단계: 세율 가져오기

1. _관리자_ 사이드바에서 **[!UICONTROL System]** > _[!UICONTROL Data Transfer]_>**[!UICONTROL Import/Export Tax Rates]**(으)로 이동합니다.

1. **[!UICONTROL Choose File]**&#x200B;을(를) 클릭하고 가져오려고 준비한 CSV 세율 파일을 선택합니다.

1. **[!UICONTROL Import Tax Rates]**&#x200B;을(를) 클릭합니다.

   데이터를 가져오는 데 몇 분 정도 걸릴 수 있습니다. 프로세스가 완료되면 `The tax rate has been imported` 메시지가 나타납니다. 오류 메시지가 표시되면 데이터의 문제를 수정한 후 다시 시도하십시오.

1. _관리자_ 사이드바에서 **[!UICONTROL Stores]** > _[!UICONTROL Taxes]_>**[!UICONTROL Tax Zones and Rates]**(으)로 이동합니다.

   가져온 비율이 목록에 나타납니다.

1. 페이지 컨트롤을 사용하여 새 세율을 봅니다.

   ![데이터 가져오기 세율](../stores-purchase/assets/tax-zones-rates.png){width="600" zoomable="yes"}

1. 새 세율이 올바로 작동하도록 다른 우편 번호의 고객과 함께 스토어에서 일부 테스트 거래를 실행합니다.
