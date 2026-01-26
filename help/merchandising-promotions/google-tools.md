---
title: Google 사이트 도구
description: 콘텐츠를 최적화하고, 트래픽을 분석하고, 카탈로그를 쇼핑 집계자 및 마켓플레이스에 연결하는 데 사용할 수 있는 Google 도구 통합에 대해 알아봅니다.
exl-id: 09c48f1e-792b-4553-82fc-cd1a119b15d0
feature: Marketing Tools, Integration
source-git-commit: cace9d1de00955494d8bc607c017778ff7df4806
workflow-type: tm+mt
source-wordcount: '645'
ht-degree: 0%

---

# Google 사이트 도구

스토어 구성은 다음의 Google 도구와 통합되어 콘텐츠를 최적화하고, 트래픽을 분석하고, 카탈로그를 쇼핑 집선 및 마켓플레이스에 연결하는 데 도움이 됩니다.

- [Google Analytics](google-analytics.md) - _Google Universal Analytics_&#x200B;을(를) 사용하여 추적을 위한 추가 사용자 지정 차원 및 지표를 정의하고 오프라인 및 모바일 앱 상호 작용과 지속적인 업데이트에 액세스할 수 있습니다.

- [Google 태그 관리자](google-tag-manager.md) - ![Adobe Commerce](../assets/adobe-logo.svg)(Adobe Commerce 전용) Google 태그 관리자를 사용하여 마케팅 캠페인 이벤트와 관련된 여러 태그를 관리합니다.

- [Google AdWords](google-adwords.md) - Google AdWords 캠페인을 만들고 스토어에 대한 전환을 추적합니다.

{{gtag-api-note}}

## Google 개인 정보 설정

비즈니스가 [GDPR](../getting-started/compliance-gdpr.md) 또는 [CCPA](../getting-started/compliance-ccpa.md)와 같은 개인 정보 보호 규정을 준수해야 하는 경우 개인 정보 보호 요구 사항을 충족하도록 Google 도구의 기본 설정을 변경하십시오. 다음 단계에 따라 고객 데이터 사용이 지속적으로 준수되도록 하십시오.

### 1단계: Google 설정 업데이트

1. 회사의 Google Analytics 계정에 [로그인](https://www.google.com/analytics/){: target="_blank"}.

1. 왼쪽 사이드바 아래에서 **[!UICONTROL Admin]**&#x200B;을(를) 선택한 다음 편집할 계정으로 이동합니다(해당하는 경우).

1. **[!UICONTROL Account]** 열에서 **[!UICONTROL Account Settings]**&#x200B;을(를) 클릭합니다.

1. 개인 정보 보호 규정 요구 사항을 충족하기 위해 데이터 공유를 끕니다.

   기본 Google Analytics 설정은 회사 데이터를 Google 및 다른 당사자와 공유합니다. 데이터 공유를 해제하려면 다음 설정에 대한 선택 확인란의 선택을 취소하십시오.

   - Google 제품 및 서비스
   - 벤치마킹
   - 기술 지원
   - 계정 전문가

1. _데이터 처리 수정_&#x200B;에 동의합니다.

   Google 광고 데이터 처리 약관은 Google에서 데이터를 처리하는 방법과 GDPR의 적용을 받는 비즈니스의 데이터 보안을 보장하기 위해 취하는 조치를 설명합니다. 또한 법인과 연락처 정보에 대한 기록이 개정과 함께 유지됩니다. [자세히 알아보기](https://support.google.com/analytics/answer/3379636){: target="_blank"}하려면 페이지 상단의 메시지에서 링크를 클릭하십시오.

   - 페이지를 아래로 스크롤하여 **[!UICONTROL Data Processing Amendment]**(으)로 이동합니다.
   - **[!UICONTROL Review Amendment]** Google 광고 데이터 처리 용어&#x200B;_를 읽으려면_&#x200B;을(를) 클릭하십시오.
   - **[!UICONTROL Accept]**&#x200B;을(를) 클릭합니다.
   - **[!UICONTROL Save]**&#x200B;을(를) 클릭합니다.

1. _DPA 관리_ 세부 정보를 완료합니다.

   - 연락처 및 조직의 엔터티를 편집할 수 있는 DPA 관리 페이지를 열려면 **[!UICONTROL Manage DPA Details]**&#x200B;을(를) 클릭하십시오.

   - **[!UICONTROL Legal Entities]** 섹션에서 _편집_( ![Google 편집 아이콘](./assets/google-icon-edit.png) ) 아이콘을 클릭하고 조직에 등록된 이름을 하나 이상 추가합니다. 완료되면 **[!UICONTROL Save]**&#x200B;을(를) 클릭합니다.

   - **연락처** 섹션에서 _추가_( ![Google 추가 아이콘](./assets/google-icon-add.png)) 아이콘을 클릭하고 첫 번째 연락처에 대한 정보를 입력합니다. 그런 다음 적용 가능한 각 역할의 확인란을 선택하고 **[!UICONTROL Add]**&#x200B;을(를) 클릭합니다.

      - 기본 담당자 - (통지 이메일 주소) 통지를 발송하는 담당자입니다.
      - 데이터 보호 관리자 - (해당되는 경우) 개인정보 보호 규정 준수를 용이하게 하도록 지정된 사람.
      - EEA(European Economic Area) 담당자 - (해당되는 경우) GDPR 의무와 관련하여 EU 이외의 고객을 대표하는 사람입니다.

     해당되는 경우 이 과정을 반복하여 다른 연락처를 추가합니다.

### 2단계: Google JS 라이브러리 수정

Google에서는 Google 제품에 따라 웹 사이트 사용량을 측정하기 위해 `gtag.js`, `analytics.js` 및 `ga.js` JavaScript 라이브러리 세 개를 지원합니다. 개인 정보 보호 요구 사항을 충족하기 위해 표준 코드를 다음과 같이 수정할 수 있습니다.

#### IP 주소 익명화

**_Google Universal Analytics_**&#x200B;에서 사용하는 IP 주소를 익명화하려면 웹 서버의 `analytics.js` 라이브러리에 다음 코드 조각을 추가하십시오.

analytics.js

```
: `ga('set', 'anonymizeIp', true);`
```

자세한 내용은 Google 도움말의 [Analytics.js 필드 참조](https://developers.google.com/analytics/devguides/collection/analyticsjs/field-reference){: target="_blank"}를 참조하세요.

기존 `ga.js` 라이브러리를 사용하는 경우 다음 코드 조각을 추가합니다.

ga.js

```
: `ga('set', 'anonymizeIp', true);`
```

**_Google 태그 관리자_**&#x200B;에서 사용하는 IP 주소를 익명으로 처리하려면 웹 서버의 `anonymize_ip` 라이브러리에서 `true` 매개 변수를 `gtag.js`(으)로 설정하십시오.

gtag.js

```
: `gtag('event', 'your_event', { 'anonymize_ip': true })`
```

자세한 내용은 Google 도움말의 [Analytics에서 IP 익명화](https://support.google.com/analytics/answer/2763052)를 참조하십시오.

#### SSL 강제 적용

SSL(Secure Socket Layer)을 통해 모든 Google 데이터를 강제로 전송하려면 웹 서버의 `analytics.js` 라이브러리에 다음 코드 조각을 추가하십시오.

analytics.js

```
: `ga('set', 'forceSSL', true);`
```

### 3단계: 개인정보 처리방침 업데이트

[개인정보 처리방침](../getting-started/privacy-policy.md)을 업데이트하여 회사에 알립니다.

- Google Analytics 사용
- 개인 정보를 숨기기 위해 IP 주소 마스크
- 이(가) Google 데이터 공유를 해제함
- Google Analytics 쿠키와 함께 다른 Google 서비스를 사용하지 않음
