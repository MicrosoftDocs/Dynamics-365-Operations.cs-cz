---
title: Vytvoření bankovního účtu dodavatele
description: Tato procedura popisuje způsob vytváření bankovního účtu pro dodavatele.
author: mkirknel
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: VendTable, VendBankAccounts, LogisticsPostalAddressSingle
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: deb3587667ac13b95617ec219995bfef931df00c
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/15/2019
ms.locfileid: "1546126"
---
# <a name="create-a-vendor-bank-account"></a><span data-ttu-id="dc5ad-103">Vytvoření bankovního účtu dodavatele</span><span class="sxs-lookup"><span data-stu-id="dc5ad-103">Create a vendor bank account</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="dc5ad-104">Tato procedura popisuje způsob vytváření bankovního účtu pro dodavatele.</span><span class="sxs-lookup"><span data-stu-id="dc5ad-104">This procedure shows you how to create a bank account for a vendor.</span></span> <span data-ttu-id="dc5ad-105">Tento postup můžete projít v ukázkových datech společnosti USMF.</span><span class="sxs-lookup"><span data-stu-id="dc5ad-105">You can use this procedure in demo data company USMF.</span></span>

1. <span data-ttu-id="dc5ad-106">Přejděte na Zásobování a zdroje > Dodavatelé > Všichni dodavatelé.</span><span class="sxs-lookup"><span data-stu-id="dc5ad-106">Go to Procurement and sourcing > Vendors > All vendors.</span></span>
2. <span data-ttu-id="dc5ad-107">Vyberte dodavatele, pro kterého chcete vytvořit bankovní účet, a klepněte na odkaz u ID účtu dodavatele.</span><span class="sxs-lookup"><span data-stu-id="dc5ad-107">Select the vendor that you want to create a bank account for, and then click the link on the Vendor account ID.</span></span>
3. <span data-ttu-id="dc5ad-108">V podokně akcí klikněte na možnost Dodavatel.</span><span class="sxs-lookup"><span data-stu-id="dc5ad-108">On the Action Pane, click Vendor.</span></span>
4. <span data-ttu-id="dc5ad-109">Klikněte na možnost Bankovní účty.</span><span class="sxs-lookup"><span data-stu-id="dc5ad-109">Click Bank accounts.</span></span>
5. <span data-ttu-id="dc5ad-110">Klikněte na položku Nová.</span><span class="sxs-lookup"><span data-stu-id="dc5ad-110">Click New.</span></span>
6. <span data-ttu-id="dc5ad-111">Zadejte hodnotu do pole Bankovní účet.</span><span class="sxs-lookup"><span data-stu-id="dc5ad-111">In the Bank account field, type a value.</span></span>
    * <span data-ttu-id="dc5ad-112">Toto ID se použije k určení bankovního účtu v záznamu dodavatele.</span><span class="sxs-lookup"><span data-stu-id="dc5ad-112">This ID will be used to identify the bank account on the vendor record.</span></span>  
7. <span data-ttu-id="dc5ad-113">Zadejte hodnotu do pole Název.</span><span class="sxs-lookup"><span data-stu-id="dc5ad-113">In the Name field, type a value.</span></span>
8. <span data-ttu-id="dc5ad-114">V poli Bankovní skupiny zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="dc5ad-114">In the Bank groups field, enter or select a value.</span></span>
9. <span data-ttu-id="dc5ad-115">V poli Typ směrového kódu vyberte vhodnou možnost.</span><span class="sxs-lookup"><span data-stu-id="dc5ad-115">In the Routing number type field, select an option.</span></span>
    * <span data-ttu-id="dc5ad-116">Toto je typ směrového kódu banky používaného pro mezinárodní platby.</span><span class="sxs-lookup"><span data-stu-id="dc5ad-116">This is the type of routing number that’s used for international payments.</span></span>  
10. <span data-ttu-id="dc5ad-117">Zadejte hodnotu do pole Číslo bankovního účtu.</span><span class="sxs-lookup"><span data-stu-id="dc5ad-117">In the Bank account number field, type a value.</span></span>
11. <span data-ttu-id="dc5ad-118">V poli Kód SWIFT zadejte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="dc5ad-118">In the SWIFT code field, type a value.</span></span>
12. <span data-ttu-id="dc5ad-119">Zadejte hodnotu do pole IBAN.</span><span class="sxs-lookup"><span data-stu-id="dc5ad-119">In the IBAN field, type a value.</span></span>
    * <span data-ttu-id="dc5ad-120">Číslo IBAN musí být ve správném formátu.</span><span class="sxs-lookup"><span data-stu-id="dc5ad-120">The IBAN number must be in the correct format.</span></span> <span data-ttu-id="dc5ad-121">Například DE89370400440532013000.</span><span class="sxs-lookup"><span data-stu-id="dc5ad-121">For example, you could use DE89370400440532013000.</span></span>  
    * <span data-ttu-id="dc5ad-122">Stav bankovního účtu je aktivní v případě, že bylo dosaženo aktivní datum, a nepřesáhli jste datum vypršení platnosti.</span><span class="sxs-lookup"><span data-stu-id="dc5ad-122">The status of the bank account is Active if the Active date has been reached, and the Expiration date has not been exceeded.</span></span> <span data-ttu-id="dc5ad-123">Je rovněž aktivní, pokud je prázdné aktivní datum i pole Datum vypršení platnosti.</span><span class="sxs-lookup"><span data-stu-id="dc5ad-123">It’s also active if both the Active date and Expiration date fields are blank.</span></span> <span data-ttu-id="dc5ad-124">Obsahují-li pole Aktivní datum i Datum vypršení platnosti data spadající do budoucnosti, elektronické platby nejsou k dispozici.</span><span class="sxs-lookup"><span data-stu-id="dc5ad-124">If the dates in both the Active date and Expiration date fields are in the future electronic payments are not available.</span></span> <span data-ttu-id="dc5ad-125">Lze však použít jiné typy plateb a bankovní účet je aktivní.</span><span class="sxs-lookup"><span data-stu-id="dc5ad-125">Other payment types are available and the bank account is active.</span></span>  
13. <span data-ttu-id="dc5ad-126">Rozbalte sekci Nastavení.</span><span class="sxs-lookup"><span data-stu-id="dc5ad-126">Expand the Setup section.</span></span>
14. <span data-ttu-id="dc5ad-127">V poli Kód textu zadejte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="dc5ad-127">In the Text code field, type a value.</span></span>
    * <span data-ttu-id="dc5ad-128">Toto pole určuje kód, který se zobrazí na bankovním výpisu příjemce.</span><span class="sxs-lookup"><span data-stu-id="dc5ad-128">This field specifies a code that will appear on the bank statement of the recipient.</span></span>  
15. <span data-ttu-id="dc5ad-129">Zadejte hodnotu do pole Zpráva bance.</span><span class="sxs-lookup"><span data-stu-id="dc5ad-129">In the Message to bank field, type a value.</span></span>
16. <span data-ttu-id="dc5ad-130">Zadejte hodnotu do pole Odkaz na kurz.</span><span class="sxs-lookup"><span data-stu-id="dc5ad-130">In the Exchange reference field, type a value.</span></span>
    * <span data-ttu-id="dc5ad-131">Toto je referenční číslo sazby směnného kurzu pro fixní nebo budoucí datum.</span><span class="sxs-lookup"><span data-stu-id="dc5ad-131">This is the reference number for any forward-term or fixed-term rate of exchange.</span></span>  
17. <span data-ttu-id="dc5ad-132">V poli Měna zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="dc5ad-132">In the Currency field, enter or select a value.</span></span>
    * <span data-ttu-id="dc5ad-133">Při vystavení verifikační transakce poskytuje tato část přehled stavu (v čekání nebo schválené).</span><span class="sxs-lookup"><span data-stu-id="dc5ad-133">When prenotes are issued, this section provides an overview of their status (pending or approved).</span></span>  
18. <span data-ttu-id="dc5ad-134">Rozbalte sekci Adresa.</span><span class="sxs-lookup"><span data-stu-id="dc5ad-134">Expand the Address section.</span></span>
19. <span data-ttu-id="dc5ad-135">Rozbalte sekci Verifikační transakce.</span><span class="sxs-lookup"><span data-stu-id="dc5ad-135">Expand the Prenotes section.</span></span>
20. <span data-ttu-id="dc5ad-136">Rozbalte oddíl Kontaktní informace.</span><span class="sxs-lookup"><span data-stu-id="dc5ad-136">Expand the Contact information section.</span></span>
21. <span data-ttu-id="dc5ad-137">Zadejte hodnotu do pole Telefon.</span><span class="sxs-lookup"><span data-stu-id="dc5ad-137">In the Telephone field, type a value.</span></span>
22. <span data-ttu-id="dc5ad-138">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="dc5ad-138">Close the page.</span></span>
23. <span data-ttu-id="dc5ad-139">Klikněte na položku Upravit.</span><span class="sxs-lookup"><span data-stu-id="dc5ad-139">Click Edit.</span></span>
24. <span data-ttu-id="dc5ad-140">Rozbalte sekci Platba.</span><span class="sxs-lookup"><span data-stu-id="dc5ad-140">Expand the Payment section.</span></span>
25. <span data-ttu-id="dc5ad-141">V poli Bankovní účet vyberte účet, který jste právě vytvořili.</span><span class="sxs-lookup"><span data-stu-id="dc5ad-141">In the Bank  account field, select the account that you’ve just created.</span></span>
26. <span data-ttu-id="dc5ad-142">Klikněte na položku Uložit.</span><span class="sxs-lookup"><span data-stu-id="dc5ad-142">Click Save.</span></span>
    * <span data-ttu-id="dc5ad-143">Adresa může být zděděna z bankovní skupiny, pokud je určena, nebo ji můžete přidat zde.</span><span class="sxs-lookup"><span data-stu-id="dc5ad-143">The address may be inherited from the bank group, if one is specified, or you can add it here.</span></span>  

