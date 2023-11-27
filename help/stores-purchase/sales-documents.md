---
title: 영업 문서
description: Commerce 스토어에 대한 고객 주문 및 이행 지원을 위해 판매 문서를 구성하는 방법에 대해 알아봅니다.
exl-id: 869d79ca-688a-4032-a95c-c66ebf7f2775
feature: Invoices
source-git-commit: 8b5af316ab1d2e632ed5fc2066974326830ab3f7
workflow-type: tm+mt
source-wordcount: '465'
ht-degree: 0%

---

# 영업 문서

주문 워크플로우를 지원하고 고객이 제출한 주문에 대한 설명서를 제공하려면 스토어 브랜드를 반영하고 참조 정보를 포함하도록 관련 판매 문서를 구성합니다.

## 송장 및 포장 명세서 구성

상점 첫 페이지에 사용된 로고 이미지와 달리 PDF 인보이스 및 기타 판매 문서에 대한 로고는 고해상도 300 dpi 이미지가 될 수 있습니다. 로고 크기를 조정할 때 종횡비를 유지하도록 주의하십시오. 높이에 맞게 로고의 크기를 조정하고, 오른쪽의 사용하지 않는 공간에 대해서는 걱정하지 마십시오.

![샘플 로고](./assets/logo-pdf.png){width="200"}

필요한 크기에 맞게 로고 크기를 조정하는 한 가지 방법은 올바른 치수로 새 빈 이미지를 만드는 것입니다. 그런 다음 로고 이미지를 붙여넣고 높이에 맞게 크기를 조정합니다. 대부분의 이미지 편집 프로그램에서 종횡비를 유지하기 위해 비율을 백분율로 조절하거나 Shift 키를 누른 상태에서 이미지 크기를 수동으로 조정할 수 있습니다.

**_로고를 업데이트하려면:_**

1. 다음에서 _관리자_ 사이드바, 이동 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. 왼쪽 패널에서 를 확장합니다. **[!UICONTROL Sales]** 및 선택 **[!UICONTROL Sales]** 밑에.

1. 확장 ![확장 선택기](../assets/icon-display-expand.png) 다음 **[!UICONTROL Invoice and Packing Slip Design]** 섹션을 참조하고 다음을 수행합니다.

   ![판매 구성 - 판매 송장 및 포장 명세서 설계](../configuration-reference/sales/assets/sales-invoice-packing-slip-design.png){width="600" zoomable="yes"}

   - 업로드 **[!UICONTROL Logo for PDF Print-outs]**, 클릭 **[!UICONTROL Choose File]**&#x200B;을(를) 클릭하고 준비한 로고를 찾은 다음 **[!UICONTROL Open]**.

   - 업로드 **[!UICONTROL Logo for HTML Print View]**, 클릭 **[!UICONTROL Choose File]**&#x200B;을(를) 클릭하고 준비한 로고를 찾은 다음 **[!UICONTROL Open]**.

   - 송장 및 포장 명세서에 표시할 주소를 입력합니다.

1. 완료되면 다음을 클릭하십시오. **[!UICONTROL Save Config]**.

   참고로 업로드된 이미지의 썸네일은 각 필드 앞에 나타난다. 축소판이 왜곡되어 나타나더라도 걱정하지 마십시오. 인보이스 상의 로고 비중은 정확합니다.

### 이미지 바꾸기

1. 클릭 **[!UICONTROL Choose File]** 다른 로고 파일을 선택하십시오.

1. 다음 항목 선택 **[!UICONTROL Delete Image]** 바꿀 이미지에 대한 확인란입니다.

1. 클릭 **[!UICONTROL Save Config]**.

### 이미지 형식

| 형식 | 요구 사항 |
|--- |------------------------------------------|
| **_PDF_** |  |
| 파일 형식 | JPG(JPEG), PNG, TIF(TIFF) |
| 이미지 크기 | 최대 1080픽셀 너비 x 270픽셀 높이 |
| 해결 방법 | 300 DPI 권장 |
| **_HTML_** |  |
| 파일 형식 | JPG(JPEG), PNG, GIF |
| 이미지 크기 | 테마에 의해 결정됩니다. |
| 해결 방법 | 72 또는 96 DPI |

{style="table-layout:auto"}

## 참조 ID 추가

주문 ID와 고객 IP 주소는 주문과 함께 제공되는 영업 문서의 헤더에 포함될 수 있습니다. 기본적으로 주문 ID와 고객 IP 주소는 모두 송장, 선적 포장 명세서 및 대변 메모의 헤더에 나타납니다.

![영업 구성 - PDF 출력](./assets/config-sales-pdf-print-outs.png){width="600" zoomable="yes"}

**_주문 ID 설정을 변경하려면:_**

1. 다음에서 _관리자_ 사이드바, 이동 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. 왼쪽 패널에서 를 확장합니다. **[!UICONTROL Sales]** 및 선택 **[!UICONTROL PDF Print-outs]**.

1. 확장 ![확장 선택기](../assets/icon-display-expand.png) 다음 **인보이스** 섹션.

1. 설정 **[!UICONTROL Display Order ID in Header]** 당신의 취향에 따라.

1. 다음에 대해 반복 **[!UICONTROL Shipment]** 및 **[!UICONTROL Credit Memo]** 섹션.

1. 완료되면 다음을 클릭하십시오. **[!UICONTROL Save Config]**.

**_고객 IP 주소 설정을 변경하려면:_**

1. 다음에서 _관리자_ 사이드바, 이동 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. 왼쪽 패널에서 를 확장합니다. **[!UICONTROL Sales]** 및 선택 **[!UICONTROL Sales]** 밑에.

1. 확장 ![확장 선택기](../assets/icon-display-expand.png) 다음 **[!UICONTROL General]** 섹션.

   ![판매 구성 - 일반 판매 설정](../configuration-reference/sales/assets/sales-general.png){width="600" zoomable="yes"}

1. 설정 **[!UICONTROL Hide Customer IP]** 원하는 대로 사용하십시오.

1. 완료되면 다음을 클릭하십시오. **[!UICONTROL Save Config]**.
