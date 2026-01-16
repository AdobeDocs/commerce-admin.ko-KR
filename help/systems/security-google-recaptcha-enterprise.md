---
title: Google reCAPTCHA 엔터프라이즈
description: 봇 및 사기 행위로부터 Adobe Commerce as a Cloud Service 매장을 보호하기 위해 Google reCAPTCHA Enterprise를 구성하는 방법을 알아봅니다.
role: Admin
feature: Configuration, Security
badgeSaas: label="SaaS만" type="Positive" url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="Adobe Commerce as a Cloud Service 프로젝트에만 적용됩니다(Adobe 관리 SaaS 인프라)."
source-git-commit: dde1d634a1c6c7435668a8ad6084b926cc0d6193
workflow-type: tm+mt
source-wordcount: '574'
ht-degree: 0%

---

# Google reCAPTCHA 엔터프라이즈

[!BADGE 샌드박스]{type=Caution tooltip="나열된 항목은 현재 샌드박스 환경에서만 사용할 수 있습니다. Adobe은 예정된 변경 사항이 프로덕션에 롤아웃되기 전에 테스트할 수 있도록 먼저 샌드박스에 대한 업데이트를 릴리스합니다."}

[Google reCAPTCHA Enterprise](https://cloud.google.com/security/products/recaptcha#protect-against-fraud-and-abuse-with-modern-bot-protection-and-fraud-prevention-platform)는 사람 사용자와 보트를 구별하기 위해 적응형 위험 분석 및 머신 러닝을 사용하여 Adobe Commerce as a Cloud Service 상점 앞에 고급 봇 보호를 제공합니다. 이를 통해 사이트에서 사기성 활동, 스팸 및 남용을 방지할 수 있습니다.

>[!NOTE]
>
>이 기능은 관리자에 대한 reCAPTCHA 지원을 제공하지 않습니다.

다른 Google reCAPTCHA 버전 구성에 대한 자세한 내용은 [Google reCAPTCHA V3 및 V2](security-google-recaptcha.md)을(를) 참조하십시오.

## 기능

Google reCAPTCHA Enterprise에는 다음 기능이 포함되어 있습니다.

- **고급 보트 감지**: 고급 보트 감지를 위해 Google Cloud의 머신 러닝 모델을 사용합니다.
- **위험 점수 분석**: 각 상호 작용에 대한 자세한 위험 점수(0.0-1.0)를 제공합니다.
- **구성 가능한 임계값**: 테넌트당 허용되는 최소 위험 점수 설정
- **다중 테넌트 지원**: 격리된 Google Cloud 프로젝트를 사용하는 테넌트별 구성
- **암호화된 자격 증명**: 데이터베이스에 암호화된 상태로 저장된 서비스 계정 자격 증명
- **양식 보호**: 로그인, 체크아웃, 제품 검토 등을 포함하여 모든 표준 Commerce 양식을 보호합니다.

## 사전 요구 사항

Adobe Commerce as a Cloud Service 스토어프론트에 대해 Google reCAPTCHA Enterprise를 구성하려면 다음 리소스가 필요합니다.

- reCAPTCHA Enterprise가 활성화된 활성 Google Cloud 계정.
- Google 클라우드 콘솔에 액세스하여 reCAPTCHA 엔터프라이즈 키를 생성하고 관리합니다.

다중 임차인 Adobe Commerce as a Cloud Service 설치에서 각 임차인은 자체 Google Cloud 프로젝트 및 reCAPTCHA Enterprise 키가 있어야 합니다.

## 1단계: Google reCAPTCHA Enterprise 설정

다음 일반 단계에 따라 상점용 Google reCAPTCHA Enterprise를 설정합니다. 자세한 지침은 [Google reCAPTCHA Enterprise 설명서](https://docs.cloud.google.com/recaptcha/docs/overview)를 참조하십시오.

1. reCAPTCHA Enterprise 구현을 위해 [Google Cloud 프로젝트를 만듭니다](https://developers.google.com/workspace/guides/create-project).

1. [reCAPTCHA Enterprise API](https://docs.cloud.google.com/recaptcha/docs/prepare-environment)를 사용하도록 설정합니다.

1. 점수 기반 reCAPTCHA Enterprise [사이트 키](https://docs.cloud.google.com/recaptcha/docs/choose-key-type)를 만듭니다.

1. `roles/recaptchaenterprise.admin` IAM 역할을 사용하여 서비스 계정을 만듭니다.

1. Google reCAPTCHA Enterprise로 Adobe Commerce as a Cloud Service 스토어를 인증하는 데 필요한 자격 증명이 포함된 서비스 계정 JSON 키 파일을 다운로드합니다.

## 2단계: Storefront용 Google reCAPTCHA 구성

1. _[!UICONTROL Security]_&#x200B;아래의 왼쪽 패널에서&#x200B;**[!UICONTROL Google reCAPTCHA Storefront]**&#x200B;을(를) 선택합니다.

1. 다음과 같이 **[!UICONTROL reCAPTCHA Enterprise]** 섹션을 완료합니다.

   - **[!UICONTROL Site Key]**&#x200B;의 경우 Google 클라우드 콘솔에서 reCAPTCHA Enterprise 사이트 키를 복사하여 붙여넣으십시오.

   - **[!UICONTROL Google Cloud Project ID]**&#x200B;의 경우 Google Cloud 프로젝트에서 프로젝트 ID를 복사하여 붙여 넣으십시오.

   - **[!UICONTROL Service Account JSON]**&#x200B;의 경우 [1단계: Google reCAPTCHA Enterprise 설정](#step-1-set-up-google-recaptcha-enterprise)에서 다운로드한 서비스 계정 JSON 키 파일의 내용을 복사합니다.

   - **[!UICONTROL Minimum Score Threshold]**&#x200B;에 사용자 인터랙션에 잠재적 위험이 있는 것으로 플래그가 지정된 경우를 식별하려면 최소 점수(0.0-1.0)를 입력하십시오. 점수 1.0은 일반적인 사용자 상호 작용이며 0.0은 봇일 가능성이 높습니다.

   - **[!UICONTROL Badge Position]**&#x200B;의 경우 각 페이지에서 보이지 않는 reCAPTCHA 배지의 위치를 선택하십시오. 옵션: `Inline` / `Bottom Right` / `Bottom Left`.

   - **[!UICONTROL Theme]**&#x200B;의 경우 `Light Theme`(기본값) 또는 `Dark Theme`을(를) 선택하여 Google reCAPTCHA 상자의 스타일을 결정합니다.

   - **[!UICONTROL Language Code]**&#x200B;의 경우 Google reCAPTCHA 텍스트 및 메시징에 사용되는 언어를 지정하는 [2자 코드](https://developers.google.com/recaptcha/docs/language)를 입력하십시오.

   - **[!UICONTROL Validation Failure Message]**&#x200B;의 경우, 유효성 검사가 성공하지 못할 때 선택적으로 상점 앞에 표시되는 메시지를 변경합니다.


1. **[!UICONTROL Storefront]** 섹션을 확장하고 보호할 각 상점 양식을 **[!UICONTROL reCAPTCHA Enterprise]**(으)로 설정합니다.

   {{recaptcha-forms-list}}

   ![Storefront 옵션 구성](../configuration-reference/security/assets/recaptcha-storefront.png){width="600" zoomable="yes"}

## 3단계: 구성 저장

1. 구성 설정이 완료되면 **[!UICONTROL Save Config]**&#x200B;을(를) 클릭합니다.

1. 작업 영역의 맨 위에 있는 메시지에서 **[!UICONTROL Cache Management]**&#x200B;을(를) 클릭하고 각각의 잘못된 캐시를 새로 고칩니다.
