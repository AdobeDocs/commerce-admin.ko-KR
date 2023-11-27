---
title: 이메일 템플릿
description: 이메일 템플릿과 이를 사용하여 고객에 대한 커뮤니케이션을 지원하고 브랜드를 강화하는 방법에 대해 알아봅니다.
exl-id: dfe28c77-607e-41e4-b872-3a07bcd67962
feature: Communications, Configuration
source-git-commit: 64ccc2d5016e915a554c2253773bb50f4d33d6f4
workflow-type: tm+mt
source-wordcount: '1151'
ht-degree: 0%

---

# 이메일 템플릿

이메일 템플릿은 스토어에서 전송되는 자동화된 메시지의 레이아웃, 콘텐츠 및 형식을 정의합니다. 각 트랜잭션 이메일은 특정 유형의 트랜잭션 또는 이벤트와 연결되므로 트랜잭션 이메일이라고 합니다.

Commerce에는 스토어 작업 중에 발생하는 다양한 이벤트에 의해 트리거되는 반응형 이메일 템플릿 세트가 포함되어 있습니다. 각 템플릿은 모든 화면 크기에 맞게 최적화되며, 태블릿과 모바일 장치뿐만 아니라 데스크탑에서도 볼 수 있습니다. 고객 활동, 판매, 제품 알림, 관리자 작업 및 시스템 메시지와 관련된 다양한 준비된 이메일 템플릿이 있습니다 [사용자 지정](email-template-custom.md) 브랜드를 반영하기 위해

상거래 이메일은 HTML 및 일반 텍스트 이메일 클라이언트가 렌더링할 수 있습니다. 이메일이 렌더링되는 방식에 따라 클라이언트 간에 약간의 차이가 있을 수 있습니다.

## 이메일 로고 준비

로고는 다음 파일 유형 중 하나로 저장할 수 있습니다. 투명 배경의 로고는 .PNG 또는 .GIF 파일로 저장할 수 있습니다.

- JPG/JPEG
- GIF
- PNG

헤더 템플릿에 지정된 차원이 있습니다. 그러나 고해상도 디바이스에서 로고가 잘 렌더링되도록 하려면 업로드된 이미지가 이 크기의 3배여야 합니다. 일반적으로 원본 로고 아트웍은 벡터 이미지로 만들어지므로 해상도를 잃지 않고 크기를 늘릴 수 있습니다. 그런 다음 이미지를 지원되는 비트맵 이미지 형식 중 하나로 저장할 수 있습니다.

<!-- ![Logo 3X display size](./assets/email-logo-third-size.png)-->

헤더에서 제한된 세로 공간을 활용하려면 이미지를 자르면 위쪽이나 아래쪽의 낭비되는 공간을 없앨 수 있습니다. 이미지를 편집할 때는 로고의 종횡비를 유지하도록 주의해야 높이와 너비의 크기가 비례적으로 조정됩니다.

일반적으로 이미지를 원본보다 작게 만들 수 있지만 해상도를 손실하지 않고 더 크게 만들 수는 없습니다. 작은 이미지를 찍은 후 사진 편집기에서 확대하면 이미지 해상도가 낮아집니다. 예를 들어, 머리글 템플릿에서 로고의 표시 치수가 168픽셀 너비 x 48픽셀 높이인 경우 업로드된 이미지는 504픽셀 너비 x 144픽셀 높이여야 합니다.

| 로고 Dimension | 1 x (디스플레이 크기) | 3 x (이미지 크기) |
|----------|----|----|
| 너비: | 168픽셀 | 504픽셀 |
| 높이: | 48픽셀 | 144픽셀 |

{style="table-layout:auto"}

## 이메일 템플릿 구성

구성은 기본 헤더 템플릿에 표시되는 로고와 모든 사용자 지정 항목을 결정합니다 [머리글](email-template-custom.md#header-template) 및 [꼬리말](email-template-custom.md#footer-template) 스토어에서 보낸 트랜잭션 이메일 메시지에 사용할 템플릿입니다.

![트랜잭션 이메일 디자인](./assets/design-configuration-transactional-emails.png){width="600" zoomable="yes"}

구성 설정에 대한 자세한 목록이 필요하면 를 참조하십시오. [_트랜잭션 이메일_](../content-design/configuration.md) 다음에서 _콘텐츠 및 디자인 안내서_.

## 1단계. 로고 업로드

1. 다음에서 _관리자_ 사이드바, 이동 **[!UICONTROL Content]** > _[!UICONTROL Design]_>**[!UICONTROL Configuration]**.

1. 구성할 스토어 보기를 찾아 다음을 클릭합니다. **[!UICONTROL Edit]** 다음에서 _[!UICONTROL Action]_열.

1. 아래 _[!UICONTROL Other Settings]_, 확장 ![확장 선택기](../assets/icon-display-expand.png) 다음&#x200B;**[!UICONTROL Transactional Emails]**섹션.

1. 준비한 항목을 업로드하려면 **[!UICONTROL Logo Image]**, 클릭 **[!UICONTROL Upload]** 시스템에서 파일을 선택합니다.

1. 대상 **[!UICONTROL Logo Image Alt]**&#x200B;이미지를 식별할 대체 텍스트를 입력합니다.

1. 다음을 입력합니다. **[!UICONTROL Logo Width]** 및 **[!UICONTROL Logo Height]** 픽셀 단위.

   각 값을 숫자(다음 포함 안 함)로 입력하십시오. `px` 약어입니다. 이 값은 실제 이미지 크기가 아니라 헤더에 있는 로고의 표시 차원을 참조합니다.

## 2단계. 머리글 및 바닥글 템플릿 선택

스토어 또는 다른 스토어에 대한 사용자 지정 머리글 및 바닥글 템플릿이 있는 경우 각각에 사용할 템플릿을 [범위](../getting-started/websites-stores-views.md#scope-settings) 을 참조하십시오. 그렇지 않으면 기본 템플릿이 사용됩니다. 자세한 내용은 다음을 참조하십시오. [이메일 템플릿 맞춤화](email-template-custom.md).

1. 다음을 선택합니다. **[!UICONTROL Header Template]** 모든 트랜잭션 이메일 메시지에 사용됩니다.

1. 다음을 선택합니다. **[!UICONTROL Footer Template]** 모든 트랜잭션 이메일 메시지에 사용됩니다.

1. 완료되면 다음을 클릭하십시오. **[!UICONTROL Save Config]**.

## 이메일 템플릿 목록

이메일 템플릿 목록은 모듈별로 알파벳순으로 구성됩니다.

### [!DNL Amazon_Payment]

| 템플릿 | 구성 경로 |
|--- |--- |
| `Hard-declined Authorization` | 해당 사항 없음 |
| `Soft-declined Authorization` | 해당 사항 없음 |

{style="table-layout:auto"}

### [!DNL Magento_Checkout]

| 템플릿 | 구성 경로 |
|--- |--- |
| `Payment Failed` | **페이지:** [!UICONTROL Sales] > [[!UICONTROL Checkout]](../configuration-reference/sales/checkout.md)<br/>**섹션:** [!UICONTROL Payment Failed Emails]<br/>**필드:** [!UICONTROL Payment Failed Template] |

{style="table-layout:auto"}

### [!DNL Magento_Company]

![Adobe Commerce용 B2B](../assets/b2b.svg) (Adobe Commerce용 B2B에서만 사용 가능)

| 템플릿 | 구성 경로 |
|--- |--- |
| `Assign Company Admin` | **페이지:** [!UICONTROL Customers] > [[!UICONTROL Company Configuration]](../configuration-reference/customers/company-configuration.md)<br/>**섹션:** [!UICONTROL Customer-Related Emails]<br/>**필드:** [!UICONTROL Default 'Assign Company Admin' Email] |
| `Assign Company to Customer` | **페이지:** [!UICONTROL Customers] > [회사 구성&#x200B;](../configuration-reference/customers/company-configuration.md)<br/>**섹션:** [!UICONTROL Customer-Related Emails] <br/>**필드:** [!UICONTROL Default 'Assign Company to Customer' Email] |
| `Company Admin Changed to Member` | **페이지:** [!UICONTROL Customers] > [[!UICONTROL Company Configuration]](../configuration-reference/customers/company-configuration.md)<br/>**섹션:** [!UICONTROL Customer-Related Emails]<br/>**필드:** [!UICONTROL Default 'Company Admin Changed To Member' Email] |
| `Company Admin Set Inactive` | **페이지:** [!UICONTROL Customers] > [[!UICONTROL Company Configuration]](../configuration-reference/customers/company-configuration.md)<br/>**섹션:** [!UICONTROL Customer-Related Emails]<br/>**필드:** [!UICONTROL Default 'Customer Status Inactive' Email] |
| `Company Invite` | 해당 사항 없음 |
| `Company Registration Request` | **페이지:** [!UICONTROL Customers] > [[!UICONTROL Company Configuration]](../configuration-reference/customers/company-configuration.md)<br/>**섹션:** [!UICONTROL Email Options - Company Registration]<br/>**필드:** [!UICONTROL Default Company Registration Email] |
| `Company Status Active1` | **페이지:** [!UICONTROL Customers] > [[!UICONTROL Company Configuration]](../configuration-reference/customers/company-configuration.md)<br/>**섹션:** [!UICONTROL Company Status Change]<br/>**필드:** [!UICONTROL Default 'Company Status Change To Active 1" Email] |
| `Company Status Active2` | **페이지:** [!UICONTROL Customers] > [[!UICONTROL Company Configuration]](../configuration-reference/customers/company-configuration.md)<br/>**섹션:** [!UICONTROL Company Status Change]<br/>**필드:** [!UICONTROL Default 'Company Status Change To Active 2" Email] |
| `Company Status Blocked` | **페이지:** [!UICONTROL Customers] > [[!UICONTROL Company Configuration]](../configuration-reference/customers/company-configuration.md)<br/>**섹션:** [!UICONTROL Company Status Change]<br/>**필드:** [!UICONTROL Default 'Company Status Change To Blocked" Email] |
| `Company Status Pending Approval` | **페이지:** [!UICONTROL Customers] > [[!UICONTROL Company Configuration]](../configuration-reference/customers/company-configuration.md)<br/>**섹션:** [!UICONTROL Company Status Change]<br/>**필드:** [!UICONTROL Default 'Company Status Change To Pending Approval" Email] |
| `Company Status Rejected` | **페이지:** [!UICONTROL Customers] > [[!UICONTROL Company Configuration]](../configuration-reference/customers/company-configuration.md)<br/>**섹션:** [!UICONTROL Company Status Change]<br/>**필드:** [!UICONTROL Default 'Company Status Change To Rejected" Email] |
| `Customer Status Active` | **페이지:** [!UICONTROL Customers] > [[!UICONTROL Company Configuration]](../configuration-reference/customers/company-configuration.md)<br/>**섹션:** [!UICONTROL Customer-Related Emails]<br/>**필드:** [!UICONTROL Default 'Customer Status Active' Email] |
| `Customer Status Inactive` | **페이지:** [!UICONTROL Customers] > [[!UICONTROL Company Configuration]](../configuration-reference/customers/company-configuration.md)<br/>**섹션:** [!UICONTROL Customer-Related Emails]<br/>**필드:** [!UICONTROL Default 'Company Admin Inactive' Email] |
| `Sales Representative Assigned to Company` | **페이지:** [!UICONTROL Customers] > [[!UICONTROL Company Configuration]](../configuration-reference/customers/company-configuration.md)<br/>**섹션:** [!UICONTROL Customer-Related Emails]<br/>**필드:** [!UICONTROL Default 'Sales Rep Assigned' Email] |

{style="table-layout:auto"}

### [!DNL Magento_CompanyCredit]

![Adobe Commerce용 B2B](../assets/b2b.svg) (Adobe Commerce용 B2B에서만 사용 가능)

| 템플릿 | 구성 경로 |
|--- |--- |
| `Credit Limit Allocated` | **페이지:** [!UICONTROL Customers] > [[!UICONTROL Company Configuration]](../configuration-reference/customers/company-configuration.md)<br/>**섹션:** [!UICONTROL Company Credit]<br/>**필드:** [!UICONTROL Allocated Email Template] |
| `Credit Limit Updated` | **페이지:** [!UICONTROL Customers] > [[!UICONTROL Company Configuration]](../configuration-reference/customers/company-configuration.md)<br/>**섹션:** [!UICONTROL Company Credit]<br/>**필드:** [!UICONTROL Updated Email Template] |
| `Credit Reimbursed` | **페이지:** [!UICONTROL Customers] > [[!UICONTROL Company Configuration]](../configuration-reference/customers/company-configuration.md)<br/>**섹션:** [!UICONTROL Company Credit]<br/>**필드:** [!UICONTROL Reimbursed Email Template] |
| `Order Refunded to Company Credit` | **페이지:** [!UICONTROL Customers] > [[!UICONTROL Company Configuration]](../configuration-reference/customers/company-configuration.md)<br/>**섹션:** [!UICONTROL Company Credit]<br/>**필드:** [!UICONTROL Refunded Email Template] |
| `Order Reverted to Company Credit` | **페이지:** [!UICONTROL Customers] > [[!UICONTROL Company Configuration]](../configuration-reference/customers/company-configuration.md)<br/>**섹션:** [!UICONTROL Company Credit]<br/>**필드:** [!UICONTROL Reverted Email Template] |

{style="table-layout:auto"}

### [!DNL Magento_Contact]

| 템플릿 | 구성 경로 |
|--- |--- |
| `Contact Form` | **페이지:** [!UICONTROL General] > [[!UICONTROL Contacts]](../configuration-reference/general/contacts.md)<br/>**섹션:** [!UICONTROL Email Options]<br/>**필드:** [!UICONTROL Email Template] |

{style="table-layout:auto"}

### [!UICONTROL Magento_Customer]

| 템플릿 | 구성 경로 |
|--- |--- |
| `Change Email` | **페이지:** [!UICONTROL Customers] > [[!UICONTROL Customer Configuration]](../configuration-reference/customers/customer-configuration.md)<br/>**섹션:** [!UICONTROL Account Information Options]<br/>**필드:** [!UICONTROL Change Email Template] |
| 이메일 및 암호 변경 | **페이지:** [!UICONTROL Customers] > [[!UICONTROL Customer Configuration]](../configuration-reference/customers/customer-configuration.md)<br/>**섹션:** [!UICONTROL Account Information Options]<br/>**필드:** [!UICONTROL Change Email and Password Template] |
| `Forgot Password` | **페이지:** [!UICONTROL Customers] > [[!UICONTROL Customer Configuration]](../configuration-reference/customers/customer-configuration.md)<br/>**섹션:** [!UICONTROL Password Options]<br/>**필드:** 이메일 템플릿 잊음 |
| `New Account` | **페이지:** [!UICONTROL Customers] > [[!UICONTROL Customer Configuration]](../configuration-reference/customers/customer-configuration.md)<br/>**섹션:** [!UICONTROL Create New Account Options]<br/>**필드:** 기본 환영 전자 메일 |
| `New Account (Magento/luma)` | **페이지:** [!UICONTROL Customers] > [[!UICONTROL Customer Configuration]](../configuration-reference/customers/customer-configuration.md)<br/>**섹션:** [!UICONTROL Create New Account Options]<br/>**필드:** 기본 환영 전자 메일 |
| `New Account Confirmation Key` | **페이지:** [!UICONTROL Customers] > [[!UICONTROL Customer Configuration]](../configuration-reference/customers/customer-configuration.md)<br/>**섹션:** [!UICONTROL Create New Account Options]<br/>**필드:** 확인 링크 이메일 |
| `New Account Confirmed` | **페이지:** [!UICONTROL Customers] > [[!UICONTROL Customer Configuration]](../configuration-reference/customers/customer-configuration.md)<br/>**섹션:** [!UICONTROL Create New Account Options]<br/>**필드:** 환영 전자 메일 |
| `New Account Without Password` | **페이지:** [!UICONTROL Customers] > [[!UICONTROL Customer Configuration]](../configuration-reference/customers/customer-configuration.md)<br/>**섹션:** [!UICONTROL Create New Account Options]<br/>**필드:** 암호 없는 기본 환영 이메일 |
| `Remind Password` | **페이지:** [!UICONTROL Customers] > [[!UICONTROL Customer Configuration]](../configuration-reference/customers/customer-configuration.md)<br/>**섹션:** [!UICONTROL Password Options]<br/>**필드:** 이메일 템플릿 미리 알림 |
| `Reset Password` | **페이지:** [!UICONTROL Customers] > [[!UICONTROL Customer Configuration]](../configuration-reference/customers/customer-configuration.md)<br/>**섹션:** [!UICONTROL Password Options] <br/>**필드:** 암호 재설정 템플릿 |

{style="table-layout:auto"}

### [!DNL Magento_CustomerBalance]

![Adobe Commerce](../assets/adobe-logo.svg) (Adobe Commerce 전용)

| 템플릿 | 구성 경로 |
|--- |--- |
| `Store Credit Update` | **페이지:** [!UICONTROL Customers] > [[!UICONTROL Customer Configuration]](../configuration-reference/customers/customer-configuration.md)<br/>**섹션:** [!UICONTROL Store Credit Options]<br/>**필드:** [!UICONTROL Store Credit Update Email Template] |

{style="table-layout:auto"}

### [!UICONTROL Magento_Directory]

| 템플릿 | 구성 경로 |
|--- |--- |
| `Currency Update Warnings` | **페이지:** [!UICONTROL General] > [[!UICONTROL Currency Setup]](../configuration-reference/general/currency-setup.md)<br/>**섹션:** [!UICONTROL Scheduled Import Settings]<br/>**필드:** [!UICONTROL Error Email Template] |

{style="table-layout:auto"}

### [!UICONTROL Magento_Email]

| 템플릿 | 구성 경로 |
|--- |--- |
| `Footer` | 해당 사항 없음 |
| `Footer (Magento/luma)` | 해당 사항 없음 |
| `Header` | 해당 사항 없음 |

{style="table-layout:auto"}

### [!UICONTROL Magento_GiftCard]

![Adobe Commerce](../assets/adobe-logo.svg) (Adobe Commerce 전용)

| 템플릿 | 구성 경로 |
|--- |--- |
| `Gift Card(s) Purchase` | **페이지:** [!UICONTROL Sales] > [[!UICONTROL Gift Cards]](../catalog/product-gift-card-create.md)<br/>**섹션:** [!UICONTROL Gift Card Email Settings]<br/>**필드:** [!UICONTROL Gift Card Notification Email Template] |

{style="table-layout:auto"}

### [!DNL Magento_GiftCardAccount]

| 템플릿 | 구성 경로 |
|--- |--- |
| `Gift Card Code/Balance` | **페이지:** [!UICONTROL Sales] > [[!UICONTROL Gift Cards]](../catalog/product-gift-card-create.md)<br/>**섹션:** [!UICONTROL Email Sent from Gift Card Account Management]<br/>**필드:** [!UICONTROL Gift Card Template] |

{style="table-layout:auto"}

### [!DNL Magento_GiftRegistry]

| 템플릿 | 구성 경로 |
|--- |--- |
| `New Registry` | **페이지:** [!UICONTROL  Customers] > [[!UICONTROL  Gift Registry]](../configuration-reference/customers/gift-registry.md) <br/>**섹션:** [!UICONTROL Owner Notification]<br/>**필드:** [!UICONTROL Email Template] |
| `Registry Sharing` | **페이지:** [!UICONTROL  Customers] > [[!UICONTROL  Gift Registry]](../configuration-reference/customers/gift-registry.md) <br/>**섹션:** [!UICONTROL Gift Registry Sharing]<br/>**필드:** [!UICONTROL Email Template] |
| `Registry Update` | **페이지:** [!UICONTROL  Customers] > [[!UICONTROL  Gift Registry]](../configuration-reference/customers/gift-registry.md) <br/>**섹션:** [!UICONTROL Gift Registry Update]<br/>**필드:** [!UICONTROL Email Template] |

{style="table-layout:auto"}

### [!DNL Magento_InventoryInStorePickupSales]

| 템플릿 | 구성 경로 |
|--- |--- |
| `Order is Ready for Pickup` | **페이지:** [!UICONTROL  Sales] > [[!UICONTROL  Sales Emails]](../configuration-reference/sales/sales-emails.md) <br/>**섹션:** [!UICONTROL Order Ready For Pickup in Store]<br/>**필드:** [!UICONTROL Order Ready For Pickup Email Template] |
| `Order is Ready for Pickup For Guest` | **페이지:** [!UICONTROL  Sales] > [[!UICONTROL  Sales Emails]](../configuration-reference/sales/sales-emails.md) <br/>**섹션:** [!UICONTROL Order Ready For Pickup in Store]<br/>**필드:** [!UICONTROL Order Ready For Pickup Email Template for Guest] |

{style="table-layout:auto"}

### [!DNL Magento_Invitation]

| 템플릿 | 구성 경로 |
|--- |--- |
| `Customer Invitation` | **페이지:** [!UICONTROL Customers] > [[!UICONTROL Invitation]](../configuration-reference/customers/invitations.md)<br/>**섹션:** [!UICONTROL Email]<br/>**필드:** [!UICONTROL Customer Invitation Email Template] |

{style="table-layout:auto"}

### [!DNL Magento_NegotiableQuote]

![Adobe Commerce용 B2B](../assets/b2b.svg) (Adobe Commerce용 B2B에서만 사용 가능)

| 템플릿 | 구성 경로 |
|--- |--- |
| `Declined Quote` | **페이지:** [!UICONTROL  Sales] > [[!UICONTROL  Sales Emails]](../configuration-reference/sales/sales-emails.md) <br/>**섹션:** [!UICONTROL Quote]<br/>**필드:** [!UICONTROL Declined Quote Template (to Buyer)] |
| `Expiration Date Reset` | **페이지:** [!UICONTROL  Sales] > [[!UICONTROL  Sales Emails]](../configuration-reference/sales/sales-emails.md) <br/>**섹션:** [!UICONTROL Quote]<br/>**필드:** [!UICONTROL Expiration Date Reset] | **페이지:** [!UICONTROL Sales] > [[!UICONTROL  Sales Emails]](../configuration-reference/sales/sales-emails.md) <br/>**섹션:** [!UICONTROL Quote]<br/>**필드:** [!UICONTROL Order Ready For Pickup Email Template] |
| `Expiration Warning` | **페이지:** [!UICONTROL  Sales] > [[!UICONTROL  Sales Emails]](../configuration-reference/sales/sales-emails.md) <br/>**섹션:** [!UICONTROL Quote]<br/>**필드:** [!UICONTROL Quote Expiration (in 48 hrs)] |
| `Expiration Warning1` | **페이지:** [!UICONTROL  Sales] > [[!UICONTROL  Sales Emails]](../configuration-reference/sales/sales-emails.md) <br/>**섹션:** [!UICONTROL Quote]<br/>**필드:** [!UICONTROL Quote Expiration (in 24 hrs)] |
| `New Quote` | **페이지:** [!UICONTROL  Sales] > [[!UICONTROL  Sales Emails]](../configuration-reference/sales/sales-emails.md) <br/>**섹션:** [!UICONTROL Quote]<br/>**필드:** [!UICONTROL New Quote Template (to Seller)] |
| `Updated Quote` | **페이지:** [!UICONTROL  Sales] > [[!UICONTROL  Sales Emails]](../configuration-reference/sales/sales-emails.md) <br/>**섹션:** [!UICONTROL Quote]<br/>**필드:** [!UICONTROL Updated Quote Template (to Seller)] |

{style="table-layout:auto"}

### [!DNL Magento_Newsletter]

| 템플릿 | 구성 경로 |
|--- |--- |
| `Subscription Confirmation` | **페이지:** [!UICONTROL Customers] > [[!UICONTROL Newsletter]](../configuration-reference/customers/newsletter.md)<br/>**섹션:** [!UICONTROL  Subscription Options]<br/>**필드:** [!UICONTROL Confirmation Email Template] |
| `Subscription Success` | **페이지:** [!UICONTROL Customers] > [[!UICONTROL Newsletter]](../configuration-reference/customers/newsletter.md)<br/>**섹션:** [!UICONTROL  Subscription Options]<br/>**필드:** [!UICONTROL Success Email Template] |
| `Unsubscription Success` | **페이지:** [!UICONTROL Customers] > [[!UICONTROL Newsletter]](../configuration-reference/customers/newsletter.md)<br/>**섹션:** [!UICONTROL  Subscription Options]<br/>**필드:** [!UICONTROL Unsubscription Email Template] |

{style="table-layout:auto"}

### [!DNL Magento_ProductAlert]

| 템플릿 | 구성 경로 |
|--- |--- |
| `Cron Error Warning` | **페이지:** [!UICONTROL Catalog] > [[!UICONTROL Catalog]](../configuration-reference/catalog/catalog.md)<br/>**섹션:** [!UICONTROL Product Alerts Run Settings]<br/>**필드:** [!UICONTROL Error Email Template] |
| `Price Alert` | **페이지:** [!UICONTROL Catalog] > [[!UICONTROL Catalog]](../configuration-reference/catalog/catalog.md)<br/>**섹션:** [!UICONTROL Product Alerts]<br/>**필드:** [!UICONTROL Price Alert Email Template] |
| `Stock Alert` | **페이지:** [!UICONTROL Catalog] > [[!UICONTROL Catalog]](../configuration-reference/catalog/catalog.md)<br/>**섹션:** [!UICONTROL Product Alerts]<br/>**필드:** [!UICONTROL Stock Alert Email Template] |

{style="table-layout:auto"}

### [!DNL Magento_PurchaseOrder]

| 템플릿 | 구성 경로 |
|--- |--- |
| `Approved Purchase Order` | **페이지:** [!UICONTROL  Sales] > [[!UICONTROL  Sales Emails]](../configuration-reference/sales/sales-emails.md) <br/>**섹션:** [!UICONTROL Purchase Order Approval]<br/>**필드:** [!UICONTROL Approved Purchase Order] |
| `Approved, requires payment` | **페이지:** [!UICONTROL  Sales] > [[!UICONTROL  Sales Emails]](../configuration-reference/sales/sales-emails.md) <br/>**섹션:** [!UICONTROL Purchase Order Approval]<br/>**필드:** [!UICONTROL Approved, requires payment details (to Buyer)] |
| `Comment added to Purchase Order` | **페이지:** [!UICONTROL  Sales] > [[!UICONTROL  Sales Emails]](../configuration-reference/sales/sales-emails.md) <br/>**섹션:** [!UICONTROL Purchase Order Approval]<br/>**필드:** [!UICONTROL Comment added to Purchase Order] |
| `Created and Auto-approved Purchase Order` | **페이지:** [!UICONTROL  Sales] > [[!UICONTROL  Sales Emails]](../configuration-reference/sales/sales-emails.md) <br/>**섹션:** [!UICONTROL Purchase Order Approval]<br/>**필드:** [!UICONTROL Created and Automatically approved Purchase Order (to Buyer)] |
| `Created and automatically approved, requires payment details` | **페이지:** [!UICONTROL  Sales] > [[!UICONTROL  Sales Emails]](../configuration-reference/sales/sales-emails.md) <br/>**섹션:** [!UICONTROL Purchase Order Approval]<br/>**필드:** [!UICONTROL Created and automatically approved, requires payment details (to Buyer)] |
| `Created and requires Approval Purchase Order` | **페이지:** [!UICONTROL  Sales] > [[!UICONTROL  Sales Emails]](../configuration-reference/sales/sales-emails.md) <br/>**섹션:** [!UICONTROL Purchase Order Approval]<br/>**필드:** [!UICONTROL Created and requires Approval Purchase Order (to Buyer)] |
| `Error creating Order from Purchase Order` | **페이지:** [!UICONTROL  Sales] > [[!UICONTROL  Sales Emails]](../configuration-reference/sales/sales-emails.md) <br/>**섹션:** [!UICONTROL Purchase Order Approval]<br/>**필드:** [!UICONTROL Error creating Order from Purchase Order (to Buyer)] |
| `Purchase Order requires Approval` | **페이지:** [!UICONTROL  Sales] > [[!UICONTROL  Sales Emails]](../configuration-reference/sales/sales-emails.md) <br/>**섹션:** [!UICONTROL Purchase Order Approval]<br/>**필드:** [!UICONTROL Purchase Order requires Approval (to Approver)] |
| `Rejected Purchase Order` | **페이지:** [!UICONTROL  Sales] > [[!UICONTROL  Sales Emails]](../configuration-reference/sales/sales-emails.md) <br/>**섹션:** [!UICONTROL Purchase Order Approval]<br/>**필드:** [!UICONTROL Rejected Purchase Order (to Buyer)] |

{style="table-layout:auto"}

### [!DNL Magento_Reminder]

![Adobe Commerce](../assets/adobe-logo.svg) (Adobe Commerce 전용)

| 템플릿 | 구성 경로 |
|--- |--- |
| `Promotion Notification/Reminder` | **페이지:** [!UICONTROL Customers] > [[!UICONTROL Promotions]](../configuration-reference/customers/promotions.md)<br/>**섹션:** [!UICONTROL Automated Email Reminder Rules]<br/>**필드:** [!UICONTROL Reminder Email Sender] |

{style="table-layout:auto"}

### [!DNL Magento_Reward]

![Adobe Commerce](../assets/adobe-logo.svg) (Adobe Commerce 전용)

| 템플릿 | 구성 경로 |
|--- |--- |
| `Balance Update` | **페이지:** [!UICONTROL Customers] > [[!UICONTROL Reward Points]](../configuration-reference/customers/reward-points.md)<br/>**섹션:** [!UICONTROL Email Notification Settings]<br/>**필드:** [!UICONTROL Balance Update Email] |
| `Points Expiry Warning` | **페이지:** [!UICONTROL Customers] > [[!UICONTROL Reward Points]](../configuration-reference/customers/reward-points.md)<br/>**섹션:** [!UICONTROL Email Notification Settings]<br/>**필드:** [!UICONTROL Reward Points Expiry Warning Email] |

{style="table-layout:auto"}

### [!DNL Magento_Rma]

![Adobe Commerce](../assets/adobe-logo.svg) (Adobe Commerce 전용)

| 템플릿 | 구성 경로 |
|--- |--- |
| `New RMA` | **페이지:** [!UICONTROL  Sales] > [[!UICONTROL  Sales Emails]](../configuration-reference/sales/sales-emails.md) <br/>**섹션:** [!UICONTROL  RMA]<br/>**필드:** [!UICONTROL RMA Email Template] |
| `New RMA for Guest` | **페이지:** [!UICONTROL  Sales] > [[!UICONTROL  Sales Emails]](../configuration-reference/sales/sales-emails.md) <br/>**섹션:** [!UICONTROL  RMA]<br/>**필드:** [!UICONTROL RMA Email Template for Guest] |
| `RMA Admin Comments` | **페이지:** [!UICONTROL  Sales] > [[!UICONTROL  Sales Emails]](../configuration-reference/sales/sales-emails.md) <br/>**섹션:** [!UICONTROL  RMA Admin Comments]<br/>**필드:** [!UICONTROL RMA Comment Email Template] |
| `RMA Admin Comments for Guest` | **페이지:** [!UICONTROL  Sales] > [[!UICONTROL  Sales Emails]](../configuration-reference/sales/sales-emails.md) <br/>**섹션:** [!UICONTROL  RMA Admin Comments]<br/>**필드:** [!UICONTROL RMA Comment Email Template for Guest] |
| `RMA Authorization` | **페이지:** [!UICONTROL  Sales] > [[!UICONTROL  Sales Emails]](../configuration-reference/sales/sales-emails.md) <br/>**섹션:** [!UICONTROL  RMA Authorization]<br/>**필드:** [!UICONTROL RMA Authorization Email Template] |
| `RMA Authorization for Guest` | **페이지:** [!UICONTROL  Sales] > [[!UICONTROL  Sales Emails]](../configuration-reference/sales/sales-emails.md) <br/>**섹션:** [!UICONTROL  RMA Authorization]<br/>**필드:** [!UICONTROL RMA Authorization Email Template for Guest] |
| `RMA Customer Comments` | **페이지:** [!UICONTROL  Sales] > [[!UICONTROL  Sales Emails]](../configuration-reference/sales/sales-emails.md) <br/>**섹션:** [!UICONTROL RMA Customer Comments]<br/>**필드:** [!DNL RMA Comment Email Template] |

{style="table-layout:auto"}

### [!DNL Magento_Sales]

| 템플릿 | 구성 경로 |
|--- |--- |
| `Credit Memo Update` | **페이지:** [!UICONTROL  Sales] > [[!UICONTROL  Sales Emails]](../configuration-reference/sales/sales-emails.md)<br/>**섹션:** [!UICONTROL Credit Memo Contents]<br/>**필드:** [!UICONTROL Credit Memo Comment Email Template] |
| `Credit Memo Update (Magento/luma)` | **페이지:** [!UICONTROL  Sales] > [[!UICONTROL  Sales Emails]](../configuration-reference/sales/sales-emails.md)<br/>**섹션:** [!UICONTROL Credit Memo Comments]<br/>**필드:** [!UICONTROL Credit Memo Comment Email Template] |
| `Credit Memo Update for Guest` | **페이지:** [!UICONTROL  Sales] > [[!UICONTROL  Sales Emails]](../configuration-reference/sales/sales-emails.md)<br/>**섹션:** [!UICONTROL Credit Memo Comments]<br/>**필드:** [!UICONTROL Credit Memo Comment Email Template for Guest] |
| `Credit Memo Update for Guest (Magento/luma)` | **페이지:** [!UICONTROL  Sales] > [[!UICONTROL  Sales Emails]](../configuration-reference/sales/sales-emails.md)<br/>**섹션:** [!UICONTROL Credit Memo Comments]<br/>**필드:** [!UICONTROL Credit Memo Comment Email Template for Guest] |
| `Invoice Update` | **페이지:** [!UICONTROL  Sales] > [[!UICONTROL  Sales Emails]](../configuration-reference/../configuration-reference/sales/sales-emails.md)<br/>**섹션:** [!UICONTROL Invoice Comments]<br/>**필드:** [!UICONTROL Invoice Comment Email Template] |
| `Invoice Update (Magento/luma)` | **페이지:** [!UICONTROL  Sales] > [[!UICONTROL  Sales Emails]](../configuration-reference/sales/sales-emails.md)<br/>**섹션:** [!UICONTROL Invoice Comments]<br/>**필드:** [!UICONTROL Invoice Comment Email Template] |
| `Invoice Update for Guest` | **페이지:** [!UICONTROL  Sales] > [[!UICONTROL  Sales Emails]](../configuration-reference/sales/sales-emails.md)<br/>**섹션:** [!UICONTROL Invoice Comments]<br/>**필드:** [!UICONTROL Invoice Comment Email Template for Guest] |
| `Invoice Update for Guest (Magento/luma)` | **페이지:** [!UICONTROL  Sales] > [[!UICONTROL  Sales Emails]](../configuration-reference/sales/sales-emails.md)<br/>**섹션:** [!UICONTROL Invoice Comments]<br/>**필드:** [!UICONTROL Invoice Comment Email Template for Guest] |
| `New Credit Memo` | **페이지:** [!UICONTROL  Sales] > [[!UICONTROL  Sales Emails]](../configuration-reference/sales/sales-emails.md)<br/>**섹션:** [!UICONTROL Credit Memo]<br/>**필드:** [!UICONTROL Credit Memo Email Template] |
| `New Credit Memo (Magento/luma)` | **페이지:** [!UICONTROL  Sales] > [[!UICONTROL  Sales Emails]]../configuration-reference/sales/sales-emails.md)<br/>**섹션:** [!UICONTROL Credit Memo]<br/>**필드:** [!UICONTROL Credit Memo Email Template] |
| `New Credit Memo for Guest` | **페이지:** [!UICONTROL  Sales] > [[!UICONTROL  Sales Emails]](../configuration-reference/sales/sales-emails.md)<br/>**섹션:** [!UICONTROL Credit Memo]<br/>**필드:** [!UICONTROL Credit Memo Email Template for Guest] |
| `New Credit Memo for Guest (Magento/luma)` | **페이지:** [!UICONTROL  Sales] > [[!UICONTROL  Sales Emails]](../configuration-reference/sales/sales-emails.md)<br/>**섹션:** [!UICONTROL Credit Memo]<br/>**필드:** [!UICONTROL Credit Memo Email Template for Guest] |
| `New Invoice` | **페이지:** [!UICONTROL  Sales] > [[!UICONTROL  Sales Emails]](../configuration-reference/sales/sales-emails.md)<br/>**섹션:** [!UICONTROL Invoice]<br/>**필드:** [!UICONTROL Invoice Email Template] |
| `New Invoice (Magento/luma)` | **페이지:** [!UICONTROL  Sales] > [[!UICONTROL  Sales Emails]](../configuration-reference/sales/sales-emails.md)<br/>**섹션:** [!UICONTROL Invoice]<br/>**필드:** [!UICONTROL Invoice Email Template] |
| `New Invoice for Guest` | **페이지:** [!UICONTROL  Sales] > [[!UICONTROL  Sales Emails]](../configuration-reference/sales/sales-emails.md)<br/>**섹션:** [!UICONTROL Invoice]<br/>**필드:** [!UICONTROL Invoice Email Template for Guest] |
| `New Invoice for Guest (Magento/luma)` | **페이지:** [!UICONTROL  Sales] > [[!UICONTROL  Sales Emails]](../configuration-reference/sales/sales-emails.md)<br/>**섹션:** [!UICONTROL Invoice]<br/>**필드:** [!UICONTROL Invoice Email Template for Guest] |
| `New Order` | **페이지:** [!UICONTROL  Sales] > [[!UICONTROL  Sales Emails]](../configuration-reference/sales/sales-emails.md)<br/>**섹션:** [!UICONTROL Order]<br/>**필드:** [!UICONTROL New Order Confirmation Template] |
| `New Order (Magento/luma)` | **페이지:** [!UICONTROL  Sales] > [[!UICONTROL  Sales Emails]](../configuration-reference/sales/sales-emails.md)<br/>**섹션:** [!UICONTROL Order]<br/>**필드:** [!UICONTROL New Order Confirmation Template] |
| `New Order for Guest` | **페이지:** [!UICONTROL  Sales] > [[!UICONTROL  Sales Emails]](../configuration-reference/sales/sales-emails.md)<br/>**섹션:** [!UICONTROL Order]<br/>**필드:** [!UICONTROL New Order Confirmation Template for Guest] |
| `New Order for Guest (Magento/luma)` | **페이지:** [!UICONTROL  Sales] > [[!UICONTROL  Sales Emails]](../configuration-reference/sales/sales-emails.md)<br/>**섹션:** [!UICONTROL Order]<br/>**필드:** [!UICONTROL New Order Confirmation Template for Guest] |
| `New Shipment` | **페이지:** [!UICONTROL  Sales] > [[!UICONTROL  Sales Emails]](../configuration-reference/sales/sales-emails.md)<br/>**섹션:** [!UICONTROL Shipment]<br/>**필드:** [!UICONTROL Shipment Email Template] |
| `New Shipment (Magento/luma)` | **페이지:** [!UICONTROL  Sales] > [[!UICONTROL  Sales Emails]](../configuration-reference/sales/sales-emails.md)<br/>**섹션:** [!UICONTROL Shipment]<br/>**필드:** [!UICONTROL Shipment Email Template] |
| `New Shipment for Guest` | **페이지:** [!UICONTROL  Sales] > [[!UICONTROL  Sales Emails]](../configuration-reference/sales/sales-emails.md)<br/>**섹션:** [!UICONTROL Shipment]<br/>**필드:** [!UICONTROL Shipment Email Template for Guest] |
| `New Shipment for Guest (Magento/luma)` | **페이지:** [!UICONTROL  Sales] > [[!UICONTROL  Sales Emails]](../configuration-reference/sales/sales-emails.md)<br/>**섹션:** [!UICONTROL Shipment]<br/>**필드:** [!UICONTROL Shipment Email Template for Guest] |
| `Order Update` | **페이지:** [!UICONTROL  Sales] > [[!UICONTROL  Sales Emails]](../configuration-reference/sales/sales-emails.md)<br/>**섹션:** [!UICONTROL Order Comments]<br/>**필드:** [!UICONTROL Order Comment Email Template] |
| `Order Update (Magento/luma)` | **페이지:** [!UICONTROL  Sales] > [[!UICONTROL  Sales Emails]](../configuration-reference/sales/sales-emails.md)<br/>**섹션:** [!UICONTROL Order Comments]<br/>**필드:** [!UICONTROL Order Comment Email Template] |
| `Order Update for Guest` | **페이지:** [!UICONTROL  Sales] > [[!UICONTROL  Sales Emails]](../configuration-reference/sales/sales-emails.md)<br/>**섹션:** [!UICONTROL Order Comments]<br/>**필드:** [!UICONTROL Order Comment Email Template for Guest] |
| `Order Update for Guest (Magento/luma)` | **페이지:** [!UICONTROL  Sales] > [[!UICONTROL  Sales Emails]](../configuration-reference/sales/sales-emails.md)<br/>**섹션:** [!UICONTROL Order Comments]<br/>**필드:** [!UICONTROL Order Comment Email Template for Guest] |
| `Shipment Update` | **페이지:** [!UICONTROL  Sales] > [[!UICONTROL  Sales Emails]](../configuration-reference/sales/sales-emails.md)<br/>**섹션:** [!UICONTROL Shipment Comments]<br/>**필드:** [!UICONTROL Shipment Comment Email Template] |
| `Shipment Update (Magento/luma)` | **페이지:** [!UICONTROL  Sales] > [[!UICONTROL  Sales Emails]](../configuration-reference/sales/sales-emails.md)<br/>**섹션:** [!UICONTROL Shipment Comments]<br/>**필드:** [!UICONTROL Shipment Comment Email Template] |
| `Shipment Update for Guest` | **페이지:** [!UICONTROL  Sales] > [[!UICONTROL  Sales Emails]](../configuration-reference/sales/sales-emails.md)<br/>**섹션:** [!UICONTROL Shipment Comments]<br/>**필드:** [!UICONTROL Shipment Comment Email Template for Guest] |
| `Shipment Update for Guest (Magento/luma)` | **페이지:** [!UICONTROL  Sales] > [[!UICONTROL  Sales Emails]](../configuration-reference/sales/sales-emails.md)<br/>**섹션:** [!UICONTROL Shipment Comments]<br/>**필드:** [!UICONTROL Shipment Comment Email Template for Guest] |

{style="table-layout:auto"}

### [!DNL Magento_ScheduledImportExport]

![Adobe Commerce](../assets/adobe-logo.svg) (Adobe Commerce 전용)

| 템플릿 | 구성 경로 |
|--- |--- |
| `Export Failed` | **페이지:** [!UICONTROL Advanced] > [[!UICONTROL System]](../configuration-reference/advanced/system.md)<br/>**섹션:** [!UICONTROL Scheduled Import/Export File History Cleaning]<br/>**필드:** [!UICONTROL Export Failed Template] |
| `File History Clean Failed` | **페이지:** [!UICONTROL Advanced] > [[!UICONTROL System]](../configuration-reference/advanced/system.md)<br/>**섹션:** [!UICONTROL Scheduled Import/Export File History Cleaning]<br/>**필드:** [!UICONTROL Error Email Template] |
| `Import Failed` | **페이지:** [!UICONTROL Advanced] > [[!UICONTROL System]](../configuration-reference/advanced/system.md)<br/>**섹션:** [!UICONTROL Scheduled Import/Export File History Cleaning]<br/>**필드:** [!UICONTROL Import Failed Template] |

{style="table-layout:auto"}

### [!DNL Magento_SendFriend]

| 템플릿 | 구성 경로 |
|--- |--- |
| `Send Product Link to Friend` | **페이지:** [!UICONTROL Catalog] > [[!UICONTROL Email to a Friend]](../configuration-reference/catalog/email-to-a-friend.md)<br/>**섹션:** [!UICONTROL Email Templates]<br/>**필드:** [!UICONTROL Select Email Template] |

{style="table-layout:auto"}

### [!DNL Magento_Sitemap]

| 템플릿 | 구성 경로 |
|--- |--- |
| `Sitemap Generation Settings` | **페이지:** [!UICONTROL Catalog] > [[!UICONTROL XML Sitemap]](../configuration-reference/catalog/xml-sitemap.md)<br/>**섹션:** [!UICONTROL Generation Settings]<br/>**필드:** [!UICONTROL Error Email Template] |

{style="table-layout:auto"}

### [!DNL Magento_TwoFactorAuth]

| 템플릿 | 구성 경로 |
|--- |--- |
| `2FA Configuration Required by User` | 해당 사항 없음 |
| `2FA Configuration Required for the Application` | 해당 사항 없음 |

{style="table-layout:auto"}

### [!DNL Magento_User]

| 템플릿 | 구성 경로 |
|--- |--- |
| `Forgot Admin Password` | **페이지:** [!UICONTROL Advanced] > [[!UICONTROL Admin]](../configuration-reference/advanced/admin.md)<br/>**섹션:** [!UICONTROL Admin User Emails]<br/>**필드:** 암호 찾기 이메일 템플릿 |
| `User Notification` | **페이지:** [!UICONTROL Advanced] > [[!UICONTROL Admin]](../configuration-reference/advanced/admin.md)<br/>**섹션:** [!UICONTROL Admin User Emails]<br/>**필드:** 사용자 알림 템플릿 |
| `New User Notification` | **페이지:** [!UICONTROL Advanced] > [[!UICONTROL Admin]](../configuration-reference/advanced/admin.md)<br/>**섹션:** [!UICONTROL Admin User Emails]<br/>**필드:** [!UICONTROL New User Notification Template] |

{style="table-layout:auto"}

### [!DNL Magento_Wishlist]

| 템플릿 | 구성 경로 |
|--- |--- |
| `Magento Wish List Sharing` | **페이지:** [!UICONTROL Customers] > [[!UICONTROL Wish List]](../configuration-reference/customers/wishlist.md)<br/>**섹션:** [!UICONTROL Share Options]<br/>**필드:** [!UICONTROL Email Template] |

{style="table-layout:auto"}
