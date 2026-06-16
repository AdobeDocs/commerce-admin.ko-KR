---
title: 고객 세션 수명
description: 고객 세션 수명은 고객 쇼핑 세션의 수명을 결정합니다.
exl-id: 7180631a-3233-40f3-92bf-b329fc260cf9
feature: Customers, Configuration, Security
TQID: https://experienceleague.adobe.com/cJ8Rv5zMkTvZMfrl-nj-3xy3guSPDlxa7HZ-ZG7kLFw
product_v2: id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2: id: ba9e5be9-7de1-4f71-a5d2-baead0e425eeid: bd989d82-1e15-4534-88db-f1f51dd77ffaid: dac87252-6066-4d6e-a9d2-f6d84c323de7
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
level_v2: id: b5a62a22-46f7-4f0d-b151-3fc640bef588id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2: id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377id: d095671a-1355-40aa-8b5f-06c33c68080bid: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 403
ht-degree: 0%

---

# 고객 세션 수명

고객 쇼핑 세션의 수명은 서버 세션의 길이, [영구 장바구니](../stores-purchase/cart-persistent.md)의 사용, 브라우저에 저장된 정보의 수명 등 여러 요인에 의해 결정됩니다. 동일한 고객 경험과 관련이 있지만 만료 이벤트와 수명이 다른 별도의 프로세스입니다.

| 프로세스 | 설명 |
| --- | --- |
| 세션 | 장바구니의 컨텐츠와 같이 서버에 저장된 정보입니다. 쿠키가 만료되기 전에 서버 세션이 만료되는 경우 고객이 장바구니 컨텐츠를 잃게 되어 보안 위험이 감소될 수 있습니다. |
| 세션 쿠키 | 브라우저에 문자 숫자 또는 문자열로 저장되는 정보입니다. 서버 세션 전에 세션 쿠키가 만료되면 고객이 로그아웃됩니다. 고객이 브라우저 창을 닫으면 세션 쿠키가 삭제됩니다. 기본적으로 쿠키 수명은 3,600초 또는 1시간으로 설정됩니다. 이 시간 동안 키보드 활동이 없으면 현재 세션이 종료되며 고객은 계정에 다시 로그인해야 쇼핑을 계속할 수 있습니다. |

{style="table-layout:auto"}

[영구적 장바구니](../stores-purchase/cart-persistent.md)를 사용하도록 설정하면, 다음에 고객이 계정에 로그인할 때 장바구니 콘텐츠가 저장됩니다. 영구 장바구니를 사용하는 경우 서버 세션 및 세션 쿠키의 수명을 긴 기간으로 설정하는 것이 좋습니다.

서버에서 세션 길이는 `php.ini` 파일과 여러 변수에 의해 제어됩니다. 현재 Adobe Commerce에는 서버 세션의 길이를 제어하는 관리 구성 설정이 없습니다.

## 쿠키 라이프타임 구성

1. _관리자_ 사이드바에서 [!UICONTROL **스토어**] > _[!UICONTROL Settings]_>[!UICONTROL **구성**]&#x200B;(으)로 이동합니다.

1. 저장소가 여러 개 있는 경우 오른쪽 상단의 **[!UICONTROL Store View]** 선택기를 구성이 적용되는 저장소로 설정합니다.

1. **[!UICONTROL General]** 아래의 왼쪽 패널에서 **[!UICONTROL Web]**&#x200B;을(를) 선택합니다.

1. **[!UICONTROL Default Cookie Settings]** 섹션을 확장합니다.

   ![기본 쿠키 설정](../configuration-reference/general/assets/web-default-cookie-settings.png){width="600" zoomable="yes"}

1. 기본값을 변경하려면 **[!UICONTROL Use system value]** 확인란의 선택을 취소하고 새 값을 초 단위로 입력하십시오.

1. 완료되면 **[!UICONTROL Save Config]**&#x200B;을(를) 클릭합니다.

## _내 정보 저장_ 기능 구성

보다 쉽게 로그인할 수 있도록 **[!UICONTROL Remember Me]** 기능을 사용하면 사용자 계정 보유자가 상점 앞에 들어갈 때마다 자격 증명을 입력할 필요가 없습니다. 보안상의 이유로 지속성 기능은 기본적으로 비활성화되어 있습니다.

1. _관리자_ 사이드바에서 **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**(으)로 이동합니다.

1. 왼쪽 패널에서 **[!UICONTROL Customers]**&#x200B;을(를) 확장하고 **[!UICONTROL Persistent Shopping Cart]**&#x200B;을(를) 선택합니다.

1. **[!UICONTROL General Options]** 섹션을 확장합니다.

1. **[!UICONTROL Enable Persistence]**&#x200B;의 경우 `Yes`(으)로 설정합니다. (**[!UICONTROL Use system value]** 확인란의 선택을 취소하여 기본 설정을 변경할 수 있습니다.)

1. **[!UICONTROL Enable "Remember Me"]**&#x200B;의 경우 요구 사항에 따라 `Yes` 또는 `No`(으)로 설정하십시오.

1. 완료되면 **[!UICONTROL Save Config]**&#x200B;을(를) 클릭합니다.
