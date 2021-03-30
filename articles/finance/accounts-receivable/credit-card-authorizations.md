---
title: Nastavení platební karty, autorizace a záznam
description: Tento článek přehled autorizace platební karty v aplikaci Microsoft Dynamics 365 Finance. Obsahuje informace o způsobu nastavení platební služby, přidání platební karty do prodejní objednávky a anulování ověření.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 08/22/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CreditCardProcessors, CustTable, SalesTable
audience: Application User
ms.reviewer: roschlom
ms.custom: 3041
ms.assetid: 678f6899-bfa5-439b-aaca-b4affcc338ba
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: baeaf6c47e9d799b729bb3f0b09a5e9e4511eac6
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/15/2021
ms.locfileid: "5217451"
---
# <a name="credit-card-setup-authorization-and-capture"></a><span data-ttu-id="b0c42-104">Nastavení platební karty, autorizace a záznam</span><span class="sxs-lookup"><span data-stu-id="b0c42-104">Credit card setup, authorization, and capture</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="b0c42-105">Tento článek přehled autorizace platební karty v aplikaci Microsoft Dynamics 365 Finance.</span><span class="sxs-lookup"><span data-stu-id="b0c42-105">This article provides an overview of credit card authorization in Microsoft Dynamics 365 Finance.</span></span> <span data-ttu-id="b0c42-106">Obsahuje informace o způsobu nastavení platební služby, přidání platební karty do prodejní objednávky a anulování ověření.</span><span class="sxs-lookup"><span data-stu-id="b0c42-106">It includes information about how to set up a payment service, add a credit card to a sales order, and void an authorization.</span></span>

<a name="setting-up-the-credit-card-payment-service"></a><span data-ttu-id="b0c42-107">Nastavení služby pro platby platební kartou</span><span class="sxs-lookup"><span data-stu-id="b0c42-107">Setting up the credit card payment service</span></span>
------------------------------------------

<span data-ttu-id="b0c42-108">Pokud chcete použít platební karty, musíte nastavit a aktivovat službu pro platby na stránce Služby pro platby.</span><span class="sxs-lookup"><span data-stu-id="b0c42-108">To use credit cards, you must set up and activate a payment service on the Payment services page.</span></span> <span data-ttu-id="b0c42-109">Služba pro platby funguje jako spojovací článek mezi vaší právnickou osobou a bankou, která zpracovává kreditní kartu odběratele.</span><span class="sxs-lookup"><span data-stu-id="b0c42-109">A payment service acts as a bridge between your legal entity and the bank that processes a customer's credit card charges.</span></span> <span data-ttu-id="b0c42-110">Musíte spolupracovat s poskytovatelem kreditní karty, který je uveden v poli Konektor platby a nastavit účet u tohoto poskytovatele.</span><span class="sxs-lookup"><span data-stu-id="b0c42-110">You must work with a credit card provider that is listed in the Payment connector field and set up an account with that provider.</span></span> <span data-ttu-id="b0c42-111">Musíte poté nastavit další možnosti na stránce Služby pro platby, nastavit typy platebních karet pro American Express, Discover, MasterCard a Discover na stránce Typy platebních karet a aktivovat zprostředkovatele jako výchozího zprostředkovatele.</span><span class="sxs-lookup"><span data-stu-id="b0c42-111">You must then set up the other options on the Payment services page, set up credit card types for American Express, Discover, MasterCard, and Discover on the Credit card types page, and activate the provider as the default provider.</span></span> <span data-ttu-id="b0c42-112">Je nutné také postupovat podle těchto kroků pro dokončení instalace:</span><span class="sxs-lookup"><span data-stu-id="b0c42-112">You must also follow these steps to complete your setup:</span></span>
-   <span data-ttu-id="b0c42-113">Na stránce Parametry pohledávek zadejte parametry pro použití autorizace platební karty.</span><span class="sxs-lookup"><span data-stu-id="b0c42-113">On the Accounts receivable parameters page, specify parameters for using credit card authorizations.</span></span>
-   <span data-ttu-id="b0c42-114">Na stránce Platební podmínky nastavte platební podmínky pro platební karty.</span><span class="sxs-lookup"><span data-stu-id="b0c42-114">On the Terms of payment page, set up payment terms for credit cards.</span></span> <span data-ttu-id="b0c42-115">V poli Typ platby vyberte Kreditní karta.</span><span class="sxs-lookup"><span data-stu-id="b0c42-115">In the Payment type field, select Credit card.</span></span>
-   <span data-ttu-id="b0c42-116">Na stránce Platební karty odběratele zadejte informace o kreditní kartě odběratele.</span><span class="sxs-lookup"><span data-stu-id="b0c42-116">On the Customer credit cards page, enter credit card information for customers.</span></span>

## <a name="adding-a-new-credit-card"></a><span data-ttu-id="b0c42-117">Přidání nové platební karty</span><span class="sxs-lookup"><span data-stu-id="b0c42-117">Adding a new credit card</span></span>
<span data-ttu-id="b0c42-118">Můžete vytvořit nové záznamy kreditní karty na stránce Odběratelé pomocí polí Odběratel, Nastavení, Platební karta.</span><span class="sxs-lookup"><span data-stu-id="b0c42-118">You can create new credit card records on the Customers page by using Customer, Set up, Credit card.</span></span> <span data-ttu-id="b0c42-119">Můžete také vytvořit záznamy kreditní karty při zadávání prodejních objednávek na stránce Prodejní objednávku pomocí polí Správa, Odběratel, Kreditní karta, Registrační pokladna.</span><span class="sxs-lookup"><span data-stu-id="b0c42-119">You can also create credit card records when you enter sales orders on the Sales order page, by using Manage, Customer, Credit card, Register.</span></span>

<a name="adding-a-credit-card-to-a-sales-order"></a><span data-ttu-id="b0c42-120">Přidání platební karty do prodejní objednávky</span><span class="sxs-lookup"><span data-stu-id="b0c42-120">Adding a credit card to a sales order</span></span>
-------------------------------------

<span data-ttu-id="b0c42-121">Platební kartu lze přidat do prodejní objednávky výběrem platební karty ve vyhledávání platební karty na pevné záložce Cena a sleva na stránce Prodejní objednávky.</span><span class="sxs-lookup"><span data-stu-id="b0c42-121">You can add a credit card to a sales order by selecting a credit card in the credit card lookup on the Price and discounts FastTab on the Sales order page.</span></span> <span data-ttu-id="b0c42-122">Ke spuštění procesu ověření v podokně akcí na kartě Spravovat vyberte Kreditní karta a Ověřit.</span><span class="sxs-lookup"><span data-stu-id="b0c42-122">To start the authorization process, on the Action Pane, on the Manage tab, select Credit card and Authorize.</span></span>

<a name="authorizing-a-credit-card"></a><span data-ttu-id="b0c42-123">Autorizace platební karty</span><span class="sxs-lookup"><span data-stu-id="b0c42-123">Authorizing a credit card</span></span>
-------------------------

<span data-ttu-id="b0c42-124">Při ověření dochází nejprve k ověření jména držitele karty a potom k potvrzení disponibilního zůstatku.</span><span class="sxs-lookup"><span data-stu-id="b0c42-124">When a credit card is authorized, the card number and cardholder's name are verified, and the available credit balance is confirmed.</span></span> <span data-ttu-id="b0c42-125">V případě potřeby lze ověřit i hodnotu ověření platební karty a adresu držitele karty.</span><span class="sxs-lookup"><span data-stu-id="b0c42-125">Optionally, the card verification value and the cardholder’s address are verified.</span></span> <span data-ttu-id="b0c42-126">Disponibilní zůstatek odběratele je snížen o částku faktury.</span><span class="sxs-lookup"><span data-stu-id="b0c42-126">The customer's available credit balance is then reduced by the amount of the invoice.</span></span> <span data-ttu-id="b0c42-127">Služba pro platby odešle informaci, zda byla kreditní karta přijata nebo odmítnuta.</span><span class="sxs-lookup"><span data-stu-id="b0c42-127">The payment service sends information that the credit card has been approved or declined.</span></span> <span data-ttu-id="b0c42-128">Při fakturaci prodejní objednávky je kreditní karta zatížena (zaznamenána) částkou faktury.</span><span class="sxs-lookup"><span data-stu-id="b0c42-128">When the sales order is invoiced, the credit card is charged (captured) for the invoice amount.</span></span>

### <a name="card-verification-value"></a><span data-ttu-id="b0c42-129">Ověřovací hodnota platební karty</span><span class="sxs-lookup"><span data-stu-id="b0c42-129">Card verification value</span></span>

<span data-ttu-id="b0c42-130">Můžete vyžadovat hodnotu ověření platební karty, která se někdy nazývá bezpečnostní kód karty.</span><span class="sxs-lookup"><span data-stu-id="b0c42-130">You can require the card verification value, which is sometimes referred to as the card's security code.</span></span> <span data-ttu-id="b0c42-131">Pro American Express se jedná o čtyřcifernou hodnotu.</span><span class="sxs-lookup"><span data-stu-id="b0c42-131">For American Express, this is a four-digit value.</span></span> <span data-ttu-id="b0c42-132">Pro Discover, MasterCard a Visa se jedná o trojmístnou hodnotu.</span><span class="sxs-lookup"><span data-stu-id="b0c42-132">For Discover, MasterCard, and Visa, it is a three-digit value.</span></span>

### <a name="address-verification"></a><span data-ttu-id="b0c42-133">Ověření adresy</span><span class="sxs-lookup"><span data-stu-id="b0c42-133">Address verification</span></span>

<span data-ttu-id="b0c42-134">Informace z ověření adresy jsou vždy odeslány poskytovateli plateb.</span><span class="sxs-lookup"><span data-stu-id="b0c42-134">Address verification information is always sent to the payment provider.</span></span> <span data-ttu-id="b0c42-135">Můžete se rozhodnout, jaké informace jsou nutné pro transakce, aby byla přijata.</span><span class="sxs-lookup"><span data-stu-id="b0c42-135">You can decide how much information is required for a transaction to be accepted.</span></span> <span data-ttu-id="b0c42-136">Nezapomeňte se zeptat svého poskytovatele, zda tyto informace přijímá.</span><span class="sxs-lookup"><span data-stu-id="b0c42-136">Be sure to check with your provider to determine whether it accepts this information.</span></span> <span data-ttu-id="b0c42-137">Máte tyto možnosti k ověření adresy:</span><span class="sxs-lookup"><span data-stu-id="b0c42-137">Here are the options for address verification:</span></span>
-   <span data-ttu-id="b0c42-138">**Vždy přijmout transakci** – přijímat transakce bez ohledu na výsledky ověření adresy.</span><span class="sxs-lookup"><span data-stu-id="b0c42-138">**Always accept transaction** – Accept the transaction, regardless of address verification results.</span></span>
-   <span data-ttu-id="b0c42-139">**Držitel účtu** – porovnat jméno držitele karty z informací o společnosti platební karty pro transakci.</span><span class="sxs-lookup"><span data-stu-id="b0c42-139">**Account holder** – Compare the cardholder's name from the transaction with the credit card company’s information.</span></span>
-   <span data-ttu-id="b0c42-140">**Fakturační adresa** – porovnat jméno držitele karty a fakturační adresu z informací o společnosti platební karty pro transakci.</span><span class="sxs-lookup"><span data-stu-id="b0c42-140">**Billing address** – Compare the cardholder's name and billing address from the transaction with the credit card company’s information.</span></span>
-   <span data-ttu-id="b0c42-141">**Fakturační PSČ** – porovnat jméno držitele karty, fakturační adresu a PSČ z informací o společnosti platební karty pro transakci.</span><span class="sxs-lookup"><span data-stu-id="b0c42-141">**Billing postal code** – Compare the cardholder's name, billing address, and postal code from the transaction with the credit card company’s information.</span></span>

## <a name="data-support"></a><span data-ttu-id="b0c42-142">Podpora dat</span><span class="sxs-lookup"><span data-stu-id="b0c42-142">Data support</span></span>
<span data-ttu-id="b0c42-143">Pro každý typ platební karty, který je podporován, můžete určit úroveň podpory dat.</span><span class="sxs-lookup"><span data-stu-id="b0c42-143">For each credit card type that is supported, you can specify the level of data support.</span></span> <span data-ttu-id="b0c42-144">Úroveň určuje, nakolik jsou informace o transakci převedeny do služby pro platby.</span><span class="sxs-lookup"><span data-stu-id="b0c42-144">The level controls how much information about a transaction is transferred to the payment service.</span></span> <span data-ttu-id="b0c42-145">Nezapomeňte se zeptat svého poskytovatele, zda tyto informace poskytuje.</span><span class="sxs-lookup"><span data-stu-id="b0c42-145">Be sure to check with your provider to determine whether it can provide this information.</span></span> <span data-ttu-id="b0c42-146">Máte tyto možnosti pro úroveň podpory dat:</span><span class="sxs-lookup"><span data-stu-id="b0c42-146">Here are the options for the level of data support:</span></span>
-   <span data-ttu-id="b0c42-147">**Úroveň 1** – přenos dat transakce, částky transakce a popisu.</span><span class="sxs-lookup"><span data-stu-id="b0c42-147">**Level 1** – Transfer the transaction date, transaction amount, and description.</span></span>
-   <span data-ttu-id="b0c42-148">**Úroveň 2** – přenos informací 1. úrovně společně s dodací adresou, adresou obchodníka a informací o dani.</span><span class="sxs-lookup"><span data-stu-id="b0c42-148">**Level 2** – Transfer all Level 1 information, plus the shipping and merchant addresses, and tax information.</span></span>
-   <span data-ttu-id="b0c42-149">**Úroveň 3** – přenos všech informací 2. úrovně společně s informací o řádku objednávky.</span><span class="sxs-lookup"><span data-stu-id="b0c42-149">**Level 3** – Transfer all Level 2 information, plus order line information.</span></span>

## <a name="partial-payments"></a><span data-ttu-id="b0c42-150">Částečné platby</span><span class="sxs-lookup"><span data-stu-id="b0c42-150">Partial payments</span></span>
<span data-ttu-id="b0c42-151">Pokud dodáváte část objednávky, je zachycena částka z dílčí objednávky, a ověření, které bylo pro částku celé objednávky, je uzavřeno.</span><span class="sxs-lookup"><span data-stu-id="b0c42-151">If you ship part of an order, the amount of the partial order is captured, and the authorization, which was for the amount of the whole order, is closed.</span></span> <span data-ttu-id="b0c42-152">Nová autorizace je pak odeslána na zbývající částku objednávky, která ještě nebyla expedována.</span><span class="sxs-lookup"><span data-stu-id="b0c42-152">A new authorization is then submitted for the remaining amount of the order that hasn't been shipped.</span></span>

## <a name="voiding-an-authorization"></a><span data-ttu-id="b0c42-153">Anulování autorizace </span><span class="sxs-lookup"><span data-stu-id="b0c42-153">Voiding an authorization</span></span>
<span data-ttu-id="b0c42-154">Pro anulování autorizace platební karty můžete změnit metodu platby na jinou metodu, která nemá typ Platební karta.</span><span class="sxs-lookup"><span data-stu-id="b0c42-154">To void a credit card authorization, you can change the method of payment to another method that doesn't have a type of Credit card.</span></span>







[!INCLUDE[footer-include](../../includes/footer-banner.md)]