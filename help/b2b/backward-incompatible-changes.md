---
title: Adobe Commerce B2B 이전 버전과 호환 불가능한 변경 사항
description: 사용자 지정 코드를 업데이트해야 할 수 있는 Adobe Commerce B2B 릴리스의 변경 사항에 대해 알아봅니다.
exl-id: 79b66843-3f34-4fe9-9670-53d19b749eb4
source-git-commit: 29663b8a88abc581b9543621ddb475f7d7903027
workflow-type: tm+mt
source-wordcount: '137'
ht-degree: 0%

---

# Adobe Commerce B2B 이전 버전과 호환 불가능한 변경 사항

Adobe Commerce 릴리스용 B2B에서 이전 버전과 호환되지 않는 모든 변경 사항에 대한 높은 수준의 참조 정보를 검토하십시오. 중요한 영향을 미치며 자세한 설명과 특별한 지침이 필요한 호환되지 않는 변경 사항에 대해서는 강조 표시 섹션을 참조하십시오.

## 강조 표시

### 1.4.2~1.5.0

다중 회사 할당이 추가되어 회사 사용자 계정에 여러 `company_id` 값이 있을 수 있습니다. `Magento\Company\Api\Data\CompanyCustomerInterface`이(가) 사용자의 기본 `company_id`을(를) 설정하도록 업데이트되었습니다. 기본값은 회사 사용자 계정에 할당된 첫 번째 회사로 설정됩니다.

Adobe 이전 릴리스에서 업그레이드하는 경우 `Magento\Company\Api\Data\CompanyCustomerInterface`을(를) 사용하는 클래스에서 다음 메서드를 구현하는 것이 좋습니다.

- Magento\Company\Api\Data\CompanyCustomerInterface::getIsDefault
- Magento\Company\Api\Data\CompanyCustomerInterface::setIsDefault

## 참조

{{$include /help/_includes/backward-incompatible-changes/1.4.2-1.5.0.md}}

{{$include /help/_includes/backward-incompatible-changes/1.4.1-1.4.2.md}}

{{$include /help/_includes/backward-incompatible-changes/1.4.0-1.4.1.md}}

{{$include /help/_includes/backward-incompatible-changes/1.3.5-1.4.0.md}}

{{$include /help/_includes/backward-incompatible-changes/1.3.4-1.3.5.md}}

{{$include /help/_includes/backward-incompatible-changes/1.3.3-1.3.4.md}}
