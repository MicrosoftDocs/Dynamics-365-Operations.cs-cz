---
title: Přidání QR kódu nebo čárového kód do transakčních a přijímacích e-mailů
description: Toto téma vysvětluje, jak vložit QR kódy a čárové kódy, které představují ID objednávky, do transakčních a příjmových e-mailů v Microsoft Dynamics 365 Commerce.
author: bicyclingfool
ms.date: 03/04/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Commerce, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: stuharg
ms.search.validFrom: 2021-02-16
ms.dyn365.ops.version: Release 10.0.18
ms.openlocfilehash: f8d9408090846799c1bb421c4b6e5e248d37fa07
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/31/2021
ms.locfileid: "5797496"
---
# <a name="add-a-qr-code-or-bar-code-to-transactional-and-receipt-emails"></a><span data-ttu-id="2c057-103">Přidání QR kódu nebo čárového kód do transakčních a přijímacích e-mailů</span><span class="sxs-lookup"><span data-stu-id="2c057-103">Add a QR code or bar code to transactional and receipt emails</span></span>

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

<span data-ttu-id="2c057-104">Toto téma vysvětluje, jak vložit QR kódy a čárové kódy, které představují ID objednávky, do transakčních a příjmových e-mailů v Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="2c057-104">This topic explains how to insert QR codes and bar codes that represent order IDs into transactional and receipt emails in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="2c057-105">Do transakčních e-mailů můžete snadno zahrnout QR kódy a čárové kódy, které vám pomohou urychlit proces vyhledávání objednávek v maloobchodním prostředí.</span><span class="sxs-lookup"><span data-stu-id="2c057-105">You can easily include QR codes and bar codes in transactional emails to help speed up the order lookup process in a retail environment.</span></span> <span data-ttu-id="2c057-106">K vkládání QR kódů a čárových kódů do e-mailů používáte HTML značku **\<img\>**, která si vyžádá obrázek QR kódu nebo čárového kódu ze služby generování a vykreslování.</span><span class="sxs-lookup"><span data-stu-id="2c057-106">To insert QR codes and bar codes into emails, you use an HTML **\<img\>** tag that requests a QR code or bar code image from a generation and rendering service.</span></span> <span data-ttu-id="2c057-107">Společnost Microsoft tuto službu neposkytuje.</span><span class="sxs-lookup"><span data-stu-id="2c057-107">Microsoft doesn't provide this service.</span></span> <span data-ttu-id="2c057-108">Existuje však mnoho bezplatných nebo levných služeb, které mohou obsluhovat QR kódy nebo čárové kódy, které se dynamicky generují na základě hodnoty předané v řetězci dotazu.</span><span class="sxs-lookup"><span data-stu-id="2c057-108">However, there are many free or inexpensive services that can serve QR codes or bar codes that are dynamically generated based on a value that is passed in a query string.</span></span>

## <a name="add-a-qr-code-or-bar-code-to-a-transactional-email"></a><span data-ttu-id="2c057-109">Přidání QR kódu nebo čárového kód do transakčního e-mailu</span><span class="sxs-lookup"><span data-stu-id="2c057-109">Add a QR code or bar code to a transactional email</span></span>

<span data-ttu-id="2c057-110">Chcete-li vložit QR kód nebo čárový kód do transakčního e-mailu, který je odeslán jako součást nákupu v elektronickém obchodu, postupujte takto.</span><span class="sxs-lookup"><span data-stu-id="2c057-110">To insert a QR code or bar code into a transactional email that is sent as part of an e-commerce purchase, follow these steps.</span></span>

1. <span data-ttu-id="2c057-111">Otevřete zdrojový kód HTML pro šablonu transakčního e-mailu a přidejte značku HTML **\<img\>**, která odkazuje na vaši službu QR kódu nebo čárového kódu.</span><span class="sxs-lookup"><span data-stu-id="2c057-111">Open the source HTML for the transactional email template, and add an HTML **\<img\>** tag that points to your QR code or bar code service.</span></span> <span data-ttu-id="2c057-112">Následuje příklad.</span><span class="sxs-lookup"><span data-stu-id="2c057-112">Here is an example.</span></span>

    ```HTML
    <img src="https://YOUR_QR_CODE_BAR_CODE_SERVICE?data=%salesid%&param1=value1&param2=value2" alt="%salesid%" />
    ```

    <span data-ttu-id="2c057-113">Následuje vysvětlení předchozího příkladu:</span><span class="sxs-lookup"><span data-stu-id="2c057-113">Here is an explanation of the preceding example:</span></span>

    - <span data-ttu-id="2c057-114">**VAŠE\_SLUŽBA\_QR\_KÓDU\_ČÁROVÉHO\_KÓDU** představuje doménu vaší služby QR kódu nebo čárových kódů.</span><span class="sxs-lookup"><span data-stu-id="2c057-114">**YOUR\_QR\_CODE\_BAR\_CODE\_SERVICE** represents the domain of your QR code or bar code service.</span></span>
    - <span data-ttu-id="2c057-115">**data** představuje parametr, který služba QR kódu nebo čárového kódu používá k přijetí obsahu, který by měl být vykreslen jako QR kód nebo čárový kód.</span><span class="sxs-lookup"><span data-stu-id="2c057-115">**data** represents the parameter that the QR code or bar code service uses to receive the content that should be rendered as a QR code or bar code.</span></span>

        <span data-ttu-id="2c057-116">Hodnota **%salesid%** musí být tomuto parametru přiřazena.</span><span class="sxs-lookup"><span data-stu-id="2c057-116">The value **%salesid%** must be assigned to this parameter.</span></span> <span data-ttu-id="2c057-117">V tomto příkladu si všimněte, že hodnota se také používá jako alternativní text pro obrázek.</span><span class="sxs-lookup"><span data-stu-id="2c057-117">In this example, notice that the value is also used as alt text for the image.</span></span>

    - <span data-ttu-id="2c057-118">**param1** a **param2** představují další volitelné parametry.</span><span class="sxs-lookup"><span data-stu-id="2c057-118">**param1** and **param2** represent additional optional parameters.</span></span>

1. <span data-ttu-id="2c057-119">Přejděte na **Retail a Commerce \> Nastavení centrály \> Parametry \> E-mailové šablony organizace** a nahrajte aktualizovaný HTML do příslušné šablony transakčního e-mailu.</span><span class="sxs-lookup"><span data-stu-id="2c057-119">Go to **Retail and Commerce \> Headquarters setup \> Parameters \> Organization email templates**, and upload the updated HTML to the appropriate transactional email template.</span></span>

> [!NOTE]
> <span data-ttu-id="2c057-120">U poskytovatelů služeb QR kódu a čárových kódů se parametry mohou lišit.</span><span class="sxs-lookup"><span data-stu-id="2c057-120">Parameters might differ among QR code and bar code service providers.</span></span> <span data-ttu-id="2c057-121">Nezapomeňte proto kontaktovat svého poskytovatele služeb a potvrdit parametry, kterým musíte hodnoty přiřadit.</span><span class="sxs-lookup"><span data-stu-id="2c057-121">Therefore, be sure to contact your service provider to confirm the parameters that you must assign values to.</span></span>

## <a name="add-a-qr-code-or-bar-code-to-a-receipt-email"></a><span data-ttu-id="2c057-122">Přidání QR kódu nebo čárového kód do příjmového e-mailu</span><span class="sxs-lookup"><span data-stu-id="2c057-122">Add a QR code or bar code to a receipt email</span></span> 

<span data-ttu-id="2c057-123">Chcete-li vložit QR kód nebo čárový kód do e-mailu s potvrzením, který lze odeslat po provedení nákupu v místě prodeje (POS), postupujte takto.</span><span class="sxs-lookup"><span data-stu-id="2c057-123">To insert a QR code or bar code into a receipt email that can be sent after a purchase is made at the point of sale (POS), follow these steps.</span></span>

1. <span data-ttu-id="2c057-124">Otevřete zdrojový kód HTML pro šablonu e-mailu potvrzení a přidejte značku HTML **\<img\>**, která odkazuje na vaši službu QR kódu nebo čárového kódu.</span><span class="sxs-lookup"><span data-stu-id="2c057-124">Open the source HTML for the receipt email template, and add an HTML **\<img\>** tag that points to your QR code or bar code service.</span></span> <span data-ttu-id="2c057-125">Zde je příklad.</span><span class="sxs-lookup"><span data-stu-id="2c057-125">Here is an example below.</span></span>

    ```HTML
    <img src="https://YOUR_QR_CODE_BAR_CODE_SERVICE?data=%receiptid%&param1=value1&param2=value2" alt="%receiptid%" />
    ```

    <span data-ttu-id="2c057-126">Následuje vysvětlení předchozího příkladu:</span><span class="sxs-lookup"><span data-stu-id="2c057-126">Here is an explanation of the preceding example:</span></span>

    - <span data-ttu-id="2c057-127">**VAŠE\_SLUŽBA\_QR\_KÓDU\_ČÁROVÉHO\_KÓDU** představuje doménu vaší služby QR kódu nebo čárových kódů.</span><span class="sxs-lookup"><span data-stu-id="2c057-127">**YOUR\_QR\_CODE\_BAR\_CODE\_SERVICE** represents the domain of your QR code or bar code service.</span></span>
    - <span data-ttu-id="2c057-128">**data** představuje parametr, který služba QR kódu nebo čárového kódu používá k přijetí obsahu, který by měl být vykreslen jako QR kód nebo čárový kód.</span><span class="sxs-lookup"><span data-stu-id="2c057-128">**data** represents the parameter that the QR code or bar code service uses to receive the content that should be rendered as a QR code or bar code.</span></span>

        <span data-ttu-id="2c057-129">Hodnota **%receiptid%** musí být tomuto parametru přiřazena.</span><span class="sxs-lookup"><span data-stu-id="2c057-129">The value **%receiptid%** must be assigned to this parameter.</span></span> <span data-ttu-id="2c057-130">V tomto příkladu si všimněte, že hodnota se také používá jako alternativní text pro obrázek.</span><span class="sxs-lookup"><span data-stu-id="2c057-130">In this example, notice that the value is also used as alt text for the image.</span></span>

    - <span data-ttu-id="2c057-131">**param1** a **param2** představují další volitelné parametry.</span><span class="sxs-lookup"><span data-stu-id="2c057-131">**param1** and **param2** represent additional optional parameters.</span></span>

1. <span data-ttu-id="2c057-132">Přejděte na **Retail a Commerce \> Nastavení centrály \> Parametry \> E-mailové šablony organizace** a nahrajte aktualizovaný HTML do šablony e-mailu, která má ID e-mailu **emailrecpt**.</span><span class="sxs-lookup"><span data-stu-id="2c057-132">Go to **Retail and Commerce \> Headquarters setup \> Parameters \> Organization email templates**, and upload the updated HTML to the email template that has the email ID **emailrecpt**.</span></span>

> [!NOTE]
> <span data-ttu-id="2c057-133">U poskytovatelů služeb QR kódu a čárových kódů se parametry mohou lišit.</span><span class="sxs-lookup"><span data-stu-id="2c057-133">Parameters might differ among QR code and bar code service providers.</span></span> <span data-ttu-id="2c057-134">Nezapomeňte proto kontaktovat svého poskytovatele služeb a potvrdit parametry, kterým musíte hodnoty přiřadit.</span><span class="sxs-lookup"><span data-stu-id="2c057-134">Therefore, be sure to contact your service provider to confirm the parameters that you must assign values to.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="2c057-135">Další prostředky</span><span class="sxs-lookup"><span data-stu-id="2c057-135">Additional resources</span></span>

[<span data-ttu-id="2c057-136">Odesílání účtenek e-mailem z Modern POS (MPOS)</span><span class="sxs-lookup"><span data-stu-id="2c057-136">Send email receipts from Modern POS (MPOS)</span></span>](email-receipts.md)

[<span data-ttu-id="2c057-137">Vytvoření e-mailových šablon pro transakční události</span><span class="sxs-lookup"><span data-stu-id="2c057-137">Create email templates for transactional events</span></span>](email-templates-transactions.md)
