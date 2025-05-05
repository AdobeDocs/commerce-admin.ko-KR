---
title: 거리 우선순위 알고리즘 구성
description: 출하 목적지 주소의 위치를 출처 위치와 비교하기 위한 구성을 설정하여 출하를 이행할 가장 가까운 출처를 결정합니다.
exl-id: 4dec179a-25ac-48db-a84b-4974798272b0
feature: Inventory, Configuration
source-git-commit: 023716935a6657b0dc2317876debe608e65bf010
workflow-type: tm+mt
source-wordcount: '814'
ht-degree: 0%

---

# 거리 우선순위 알고리즘 구성

거리 우선순위 알고리즘은 출하 목적지 주소의 위치를 출처 위치와 비교하여 출하를 이행할 가장 가까운 출처를 결정합니다. 거리는 데이터베이스 데이터 또는 주행, 보행 또는 자전거 방향을 사용하여 한 위치에서 다른 위치로 이동하는 물리적 거리 또는 체류 시간에 의해 결정될 수 있다. 이 [Source 선택 알고리즘](selection-reservations.md)을 사용하여 배송 대상 주소와 가장 가까운 원본을 추천합니다.

>[!NOTE]
>
>거리 우선 순위 알고리즘을 사용하는 경우 [원본](sources-add.md)에 대한 전체 거리 주소와 GPS 좌표를 입력하는 것이 좋습니다.

운송 이행에 가장 가까운 출처를 찾기 위한 거리 및 시간을 계산하는 두 가지 옵션이 있습니다.

- **Google 맵** - [Google 맵 플랫폼][1] 서비스를 사용하여 배송 대상 주소와 원본 위치 간의 거리 및 시간을 계산합니다. 이 옵션은 소스의 위도와 경도(GPS 좌표)를 사용하며 계산 모드에 따라 거리 주소를 사용할 수 있습니다. [Geocoding API][2] 및 [Distance Matrix API][3]가 활성화된 Google API 키가 필요하며 Google을 통해 요금이 부과될 수 있습니다.

- **오프라인 계산** - 우편 번호 및 GPS 좌표를 사용하여 다운로드하고 가져온 지역 번호 데이터를 사용하여 거리를 계산하여 배송 대상 주소와 가장 가까운 원본을 결정합니다. 이 옵션을 구성하려면 명령줄 지침을 사용하여 지오코드를 처음 다운로드하고 가져올 수 있도록 개발자 지원이 필요할 수 있습니다.

>[!NOTE]
>
>여러 국가가 있는 다중 스토어 웹 사이트의 경우 각 국가별로 [기본 세금 대상](../stores-purchase/tax-class.md#default-tax-destination){target="_blank"}을 구성하십시오.

## Google 맵 사용

시작하려면 Google 계정이 필요하지 않습니다. 필요한 경우 이 프로세스에는 Google 계정 및 프로젝트 생성이 포함됩니다. 이 옵션을 사용하려면 구성을 완료하고 알고리즘을 사용하려면 Google 계정에 청구 계정 및 결제 방법이 추가됩니다.
그러나 Google MAP 거리 기반 알고리즘은 오프라인 계산에 비해 더 발전되고 정밀한 것으로 권장됩니다.

### 1단계: Google API 키 만들기

키는 [Google 맵 플랫폼][1]에서 가져온 것이며 [Geocoding API][2] 및 [Distance Matrix API][3]를 사용하도록 설정해야 합니다. 자세한 내용은 [거리 우선 순위 알고리즘 구성](distance-priority-algorithm.md)을 참조하십시오.

1. [Google 맵 플랫폼][1]을(를) 방문하여 **[!UICONTROL Get Started]**&#x200B;을(를) 클릭합니다.

1. 플랫폼을 사용하려면 **[!UICONTROL Maps, Routes, and Places]**&#x200B;을(를) 선택하고 **[!UICONTROL Continue]**&#x200B;을(를) 클릭합니다.

   ![키에 대한 Google 맵 플랫폼](assets/inventory-google-key1.png){width="350" zoomable="yes"}

1. Google 계정으로 로그인하거나 계정을 만듭니다.

1. 프로젝트 설정:

   - 프로젝트를 선택하거나 새 프로젝트 이름을 입력합니다.

   - 약관에 동의하려면 `Yes`을(를) 선택하세요.

   - **[!UICONTROL Next]**&#x200B;을(를) 클릭합니다.

1. 청구 계정을 입력하거나 만드십시오. 건너뛰고 나중에 청구 계정을 추가할 수 있습니다.

   이 서비스를 사용하려면 청구 계정이 필요합니다.

1. Google Cloud Platform 옵션을 열고 구성하려면 **[!UICONTROL Console]**&#x200B;을(를) 클릭합니다.

   - 프로젝트를 엽니다.

   - 메뉴를 확장하고 **[!UICONTROL APIs & Services]** > **[!UICONTROL Library]**&#x200B;을(를) 클릭합니다.

     ![Google API 서비스](assets/inventory-google-key2.png){width="350" zoomable="yes"}

   - [지오코딩 API][2] 및 [거리 매트릭스 API][3]를 검색합니다. 각 서비스를 선택하고 활성화합니다.

1. 메뉴를 확장하고 **[!UICONTROL APIs & Services]** > **[!UICONTROL Credentials]**&#x200B;을(를) 클릭한 다음 Google API 키를 복사합니다.

   ![Google API 키 복사](assets/inventory-google-key3.png){width="350" zoomable="yes"}

### 2단계: Google MAP 공급자 구성

1. _관리자_ 사이드바에서 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**(으)로 이동합니다.

1. 왼쪽 패널에서 **[!UICONTROL Catalog]**&#x200B;을(를) 확장하고 **[!UICONTROL Inventory]**&#x200B;을(를) 선택합니다.

1. _[!UICONTROL Distance Provider for Distance Based SSA]_&#x200B;섹션에서 ![확장 선택기](../assets/icon-display-expand.png)을(를) 확장하고&#x200B;**[!UICONTROL Provider]**&#x200B;을(를) `Google MAP`(으)로 설정합니다.

   ![거리 기반 SSA의 공급자](assets/config-catalog-inventory-distance-provider.png){width="350" zoomable="yes"}

1. _[!UICONTROL Google Distance Provider]_&#x200B;섹션에서 ![확장 선택기](../assets/icon-display-expand.png)를 확장하고 설정을 구성합니다.

   - **[!UICONTROL Google API Key]**&#x200B;의 경우 Google 계정에서 복사한 키를 입력하십시오.

   - **[!UICONTROL Computation mode]**&#x200B;의 경우 구성을 선택하십시오.

     >[!NOTE]
     >
     >배송에 이 알고리즘을 사용할 때 경로 및 데이터가 배송에 대해 선택한 계산 모드(주행, 자전거 타기 또는 걷기)에 대해 반환되지 않는 경우 SSA의 기본값은 Source 우선 순위 사용으로 설정됩니다. [종목당 원본 우선 순위](stocks-prioritize-sources.md)를 설정하는 것이 좋습니다.

     | 옵션 | 설명 |
     | ----- | ----- |
     | `Driving` | (기본값) 도로 네트워크를 사용하여 표준 주행 방향을 요청합니다. |
     | `Walking` | 보행자 경로 및 보도를 사용하여 보행 방향을 요청합니다(가능한 경우). |
     | `Bicycling` | 자전거 도로 및 기본 설정 거리(가능한 경우)를 사용하여 자전거 방향을 요청합니다. [거리 매트릭스 서비스][4]는 미국과 일부 캐나다에서만 사용할 수 있습니다. |

   - **[!UICONTROL Value]**&#x200B;의 경우 값 형식을 선택하십시오.

     | 옵션 | 설명 |
     | ----- | ----- |
     | `Distance` | (기본값) 지표(킬로미터 및 미터) 또는 임페리얼(마일 및 피트) 단위의 점 사이의 거리를 반환합니다. |
     | `Time to Destination` | 원본 위치에서 배송 주소까지 이동하는 데 필요한 시간을 시간 및 분 단위로 반환합니다. |

   ![Google 거리 공급자](assets/config-catalog-inventory-distance-provider-settings.png){width="350" zoomable="yes"}

1. 완료되면 **[!UICONTROL Save Config]**&#x200B;을(를) 클릭합니다.

## 오프라인 계산 사용

오프라인 계산에서는 국가 코드를 사용하여 배송지와 소스 주소 간의 거리를 결정합니다. 이 옵션을 구성하려면 개발자 지원이 필요할 수 있습니다. [!DNL Inventory Management] CLI 명령을 사용하여 [geonames.org][5]에서 데이터를 다운로드하고 가져옵니다.

>[!NOTE]
>
>[geonames.org][5]에서 가져온 지역 코드는 캐나다 및 아일랜드와 같은 일부 국가에 대해 제한이 있습니다. 자세한 내용은 [GeoNames 우편 번호 파일][6]을 참조하세요.

### 1단계: 지오코드 다운로드 및 가져오기

명령줄 구성을 완료하여 배송할 및 의 소스 위치가 있는 geocode 국가를 다운로드하고 가져옵니다. 이 단계에는 명령줄 작업에 대한 개발자 지원이 필요할 수 있습니다. [지역 코드 가져오기](cli.md#import-geocodes)를 참조하세요.

지오코드를 더 추가하려면 언제든지 이 명령을 완료하십시오.

### 2단계: 계산 설정

1. _관리자_ 사이드바에서 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**(으)로 이동합니다.

1. 왼쪽 패널에서 **[!UICONTROL Catalog]**&#x200B;을(를) 확장하고 **[!UICONTROL Inventory]**&#x200B;을(를) 선택합니다.

1. _[!UICONTROL Distance Provider for Distance Based SSA]_&#x200B;섹션에서 ![확장 선택기](../assets/icon-display-expand.png)를 확장합니다.

1. **[!UICONTROL Use system value]** 확인란의 선택을 취소하고 **[!UICONTROL Provider]**&#x200B;을(를) `Offline Calculation`(으)로 설정합니다.

   ![거리 기반 SSA에 대한 거리 공급자](assets/inventory-distance-offline.png){width="350" zoomable="yes"}

1. 완료되면 **[!UICONTROL Save Config]**&#x200B;을(를) 클릭합니다.

[1]: https://cloud.google.com/maps-platform/
[2]: https://developers.google.com/maps/documentation/geocoding/start
[3]: https://developers.google.com/maps/documentation/distance-matrix/start
[4]: https://developers.google.com/maps/documentation/javascript/distancematrix#travel_modes
[5]: https://www.geonames.org/
[6]: https://download.geonames.org/export/zip/readme.txt
