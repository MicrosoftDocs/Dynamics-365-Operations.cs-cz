---
title: Vytvoření zmocnění k přímému debetu pro odběratele
description: Tento průvodce úkolem ukazuje, jak vytvořit zmocnění k přímému debetu a použít je ve faktuře.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CustTable, CustBankAccounts, BankAccountTable, CustPaymMode, CustDirectDebitMandate, BankAccountTableLookUp, SrsReportViewerForm,  LogisticsAddressCityLookup, CustFreeInvoice, CustTableLookup
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 7c93a1aba6ca32e783a6ed6f005c72aab3e06978
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/01/2019
ms.locfileid: "1842994"
---
# <a name="create-a-direct-debit-mandate-for-a-customer"></a><span data-ttu-id="56de3-103">Vytvoření zmocnění k přímému debetu pro odběratele</span><span class="sxs-lookup"><span data-stu-id="56de3-103">Create a direct debit mandate for a customer</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="56de3-104">Tento průvodce úkolem ukazuje, jak vytvořit zmocnění k přímému debetu a použít je ve faktuře.</span><span class="sxs-lookup"><span data-stu-id="56de3-104">This task guide demonstrates how to create a direct debit mandate and use it on an invoice.</span></span>


## <a name="create-a-bank-account"></a><span data-ttu-id="56de3-105">Vytvoření bankovního účtu</span><span class="sxs-lookup"><span data-stu-id="56de3-105">Create a bank account</span></span>
1. <span data-ttu-id="56de3-106">Přejděte na Pohledávky > Zákazníci > Všichni odběratelé.</span><span class="sxs-lookup"><span data-stu-id="56de3-106">Go to Accounts receivable > Customers > All customers.</span></span>
2. <span data-ttu-id="56de3-107">Vyberte například US-001.</span><span class="sxs-lookup"><span data-stu-id="56de3-107">For example, select US-001</span></span>
3. <span data-ttu-id="56de3-108">V podokně akcí klikněte na možnost Odběratel.</span><span class="sxs-lookup"><span data-stu-id="56de3-108">On the Action Pane, click Customer.</span></span>
4. <span data-ttu-id="56de3-109">Klikněte na možnost Bankovní účty.</span><span class="sxs-lookup"><span data-stu-id="56de3-109">Click Bank accounts.</span></span>
5. <span data-ttu-id="56de3-110">Klikněte na položku Nová.</span><span class="sxs-lookup"><span data-stu-id="56de3-110">Click New.</span></span>
6. <span data-ttu-id="56de3-111">Zadejte hodnotu do pole Bankovní účet.</span><span class="sxs-lookup"><span data-stu-id="56de3-111">In the Bank account field, type a value.</span></span>
7. <span data-ttu-id="56de3-112">Zadejte hodnotu do pole Název.</span><span class="sxs-lookup"><span data-stu-id="56de3-112">In the Name field, type a value.</span></span>
8. <span data-ttu-id="56de3-113">Zadejte hodnotu do pole IBAN.</span><span class="sxs-lookup"><span data-stu-id="56de3-113">In the IBAN field, type a value.</span></span>
9. <span data-ttu-id="56de3-114">Zadejte hodnotu do pole Měna.</span><span class="sxs-lookup"><span data-stu-id="56de3-114">In the Currency field, type a value.</span></span>
10. <span data-ttu-id="56de3-115">Klikněte na položku Uložit.</span><span class="sxs-lookup"><span data-stu-id="56de3-115">Click Save.</span></span>
11. <span data-ttu-id="56de3-116">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="56de3-116">Close the page.</span></span>
12. <span data-ttu-id="56de3-117">Přejděte do části Pokladna a banka > Bankovní účty > Bankovní účty.</span><span class="sxs-lookup"><span data-stu-id="56de3-117">Go to Cash and bank management > Bank accounts > Bank accounts.</span></span>
13. <span data-ttu-id="56de3-118">Vyhledejte na seznamu požadovaný záznam a vyberte ho.</span><span class="sxs-lookup"><span data-stu-id="56de3-118">In the list, find and select the desired record.</span></span>
14. <span data-ttu-id="56de3-119">Klikněte na odkaz na vybraném řádku v seznamu.</span><span class="sxs-lookup"><span data-stu-id="56de3-119">In the list, click the link in the selected row.</span></span>
15. <span data-ttu-id="56de3-120">Klikněte na položku Upravit.</span><span class="sxs-lookup"><span data-stu-id="56de3-120">Click Edit.</span></span>
16. <span data-ttu-id="56de3-121">Rozbalte oddíl Další identifikace.</span><span class="sxs-lookup"><span data-stu-id="56de3-121">Expand the Additional identification section.</span></span>
17. <span data-ttu-id="56de3-122">Zadejte hodnotu do pole ID přímého debetu.</span><span class="sxs-lookup"><span data-stu-id="56de3-122">In the Direct debit ID field, type a value.</span></span>
18. <span data-ttu-id="56de3-123">Zadejte hodnotu do pole IBAN.</span><span class="sxs-lookup"><span data-stu-id="56de3-123">In the IBAN field, type a value.</span></span>
19. <span data-ttu-id="56de3-124">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="56de3-124">Close the page.</span></span>
20. <span data-ttu-id="56de3-125">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="56de3-125">Close the page.</span></span>

## <a name="define-the-electronic-payment-method"></a><span data-ttu-id="56de3-126">Definování metody elektronické platby</span><span class="sxs-lookup"><span data-stu-id="56de3-126">Define the electronic payment method</span></span>
1. <span data-ttu-id="56de3-127">Přejděte do nabídky Pohledávky > Nastavení platby > Metody platby.</span><span class="sxs-lookup"><span data-stu-id="56de3-127">Go to Accounts receivable > Payments setup > Methods of payment.</span></span>
2. <span data-ttu-id="56de3-128">Klikněte na položku Nová.</span><span class="sxs-lookup"><span data-stu-id="56de3-128">Click New.</span></span>
3. <span data-ttu-id="56de3-129">V poli Způsob platby zadejte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="56de3-129">In the Method of payment field, type a value.</span></span>
4. <span data-ttu-id="56de3-130">Zadejte nějakou hodnotu do pole Popis.</span><span class="sxs-lookup"><span data-stu-id="56de3-130">In the Description field, type a value.</span></span>
5. <span data-ttu-id="56de3-131">Typ platby pro metodu platby „zmocnění k přímému debetu“ musí být elektronická platba.</span><span class="sxs-lookup"><span data-stu-id="56de3-131">The payment type for a direct debit mandate method of payment must be Electronic payment.</span></span>
6. <span data-ttu-id="56de3-132">Vyberte možnost Ano v poli Požadovat zmocnění.</span><span class="sxs-lookup"><span data-stu-id="56de3-132">Select Yes in the Require mandate field.</span></span>
7. <span data-ttu-id="56de3-133">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="56de3-133">Close the page.</span></span>

## <a name="add-a-direct-debit-mandate-to-a-customer"></a><span data-ttu-id="56de3-134">Přidejte zmocnění k přímému debetu zákazníkovi.</span><span class="sxs-lookup"><span data-stu-id="56de3-134">Add a direct debit mandate to a customer.</span></span>
1. <span data-ttu-id="56de3-135">Přejděte na Pohledávky > Zákazníci > Všichni odběratelé.</span><span class="sxs-lookup"><span data-stu-id="56de3-135">Go to Accounts receivable > Customers > All customers.</span></span>
2. <span data-ttu-id="56de3-136">Vyberte například US-001.</span><span class="sxs-lookup"><span data-stu-id="56de3-136">For example, select US-001</span></span>
3. <span data-ttu-id="56de3-137">Klikněte na položku Upravit.</span><span class="sxs-lookup"><span data-stu-id="56de3-137">Click Edit.</span></span>
4. <span data-ttu-id="56de3-138">Rozbalte položku Výchozí nastavení plateb.</span><span class="sxs-lookup"><span data-stu-id="56de3-138">Expand the Payment defaults section.</span></span>
5. <span data-ttu-id="56de3-139">V poli Metody platby zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="56de3-139">In the Method of payment field, enter or select a value.</span></span>
6. <span data-ttu-id="56de3-140">Rozbalte položku Výchozí nastavení plateb.</span><span class="sxs-lookup"><span data-stu-id="56de3-140">Expand the Payment defaults section.</span></span>
7. <span data-ttu-id="56de3-141">Rozbalte část Zmocnění k přímému debetu.</span><span class="sxs-lookup"><span data-stu-id="56de3-141">Expand the Direct debit mandates section.</span></span>
8. <span data-ttu-id="56de3-142">Klepněte na možnost Přidat.</span><span class="sxs-lookup"><span data-stu-id="56de3-142">Click Add.</span></span>
9. <span data-ttu-id="56de3-143">V poli Bankovní účet zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="56de3-143">In the Bank account field, enter or select a value.</span></span>
10. <span data-ttu-id="56de3-144">V poli Bankovní účet věřitele zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="56de3-144">In the Creditor bank account field, enter or select a value.</span></span>
11. <span data-ttu-id="56de3-145">Zadejte počet plateb, u kterých očekáváte, že budou zpracovány pro zmocnění.</span><span class="sxs-lookup"><span data-stu-id="56de3-145">Enter the number of payments that you expect to process for this mandate.</span></span>
12. <span data-ttu-id="56de3-146">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="56de3-146">Click OK.</span></span>
13. <span data-ttu-id="56de3-147">Klepněte na položku Tisk.</span><span class="sxs-lookup"><span data-stu-id="56de3-147">Click Print.</span></span>
14. <span data-ttu-id="56de3-148">Klikněte na Sestava zmocnění.</span><span class="sxs-lookup"><span data-stu-id="56de3-148">Click Mandate report.</span></span>
15. <span data-ttu-id="56de3-149">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="56de3-149">Close the page.</span></span>
16. <span data-ttu-id="56de3-150">Klikněte na položku Upravit.</span><span class="sxs-lookup"><span data-stu-id="56de3-150">Click Edit.</span></span>
17. <span data-ttu-id="56de3-151">Do pole Datum podpisu zadejte datum.</span><span class="sxs-lookup"><span data-stu-id="56de3-151">In the Signature date field, enter a date.</span></span>
18. <span data-ttu-id="56de3-152">Klepněte na tlačítko Ano.</span><span class="sxs-lookup"><span data-stu-id="56de3-152">Click Yes.</span></span>
19. <span data-ttu-id="56de3-153">Zadejte místo podpisu zmocnění.</span><span class="sxs-lookup"><span data-stu-id="56de3-153">Enter the location where the mandate was signed.</span></span>
20. <span data-ttu-id="56de3-154">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="56de3-154">Click OK.</span></span>
21. <span data-ttu-id="56de3-155">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="56de3-155">Close the page.</span></span>

## <a name="create-a-free-text-invoice-with-mandate"></a><span data-ttu-id="56de3-156">Vytvoření volné faktury se zmocněním</span><span class="sxs-lookup"><span data-stu-id="56de3-156">Create a free text invoice with mandate</span></span>
1. <span data-ttu-id="56de3-157">Přejděte na Pohledávky > Faktury > Všechny volné faktury.</span><span class="sxs-lookup"><span data-stu-id="56de3-157">Go to Accounts receivable > Invoices > All free text invoices.</span></span>
2. <span data-ttu-id="56de3-158">Klikněte na položku Nová.</span><span class="sxs-lookup"><span data-stu-id="56de3-158">Click New.</span></span>
3. <span data-ttu-id="56de3-159">Vyberte odběratele, pro kterého jste vybrali zmocnění.</span><span class="sxs-lookup"><span data-stu-id="56de3-159">Select the customer that you added the mandate to.</span></span>
4. <span data-ttu-id="56de3-160">V poli ID zmocnění k přímému debetu zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="56de3-160">In the Direct debit mandate ID field, enter or select a value.</span></span>

