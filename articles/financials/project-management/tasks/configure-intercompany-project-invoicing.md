--- 
title: "Konfigurace fakturování mezipodnikového projektu"
description: "Tento postup popisuje nastavení fakturace projektu mezi dvěma společnostmi v rámci organizace."
author: KimANelson
manager: AnnBe
ms.date: 02/13/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Service industries
ms.author: knelson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: aa7889e33cff34c6679ea6e2f99c8647b89ce05b
ms.contentlocale: cs-cz
ms.lasthandoff: 04/13/2018

---
# <a name="configure-intercompany-project-invoicing"></a><span data-ttu-id="66747-103">Konfigurace fakturování mezipodnikového projektu</span><span class="sxs-lookup"><span data-stu-id="66747-103">Configure intercompany project invoicing</span></span>

[!INCLUDE [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="66747-104">Tento postup popisuje nastavení fakturace projektu mezi dvěma společnostmi v rámci organizace.</span><span class="sxs-lookup"><span data-stu-id="66747-104">This procedure shows how to set up project invoicing between two companies in your organization.</span></span> <span data-ttu-id="66747-105">Tato úloha používá sadu dat USSI.</span><span class="sxs-lookup"><span data-stu-id="66747-105">This task uses the USSI data set.</span></span>

1. <span data-ttu-id="66747-106">Přejděte do části Závazky > Dodavatelé > Všichni dodavatelé.</span><span class="sxs-lookup"><span data-stu-id="66747-106">Go to Accounts payable > Vendors > All vendors.</span></span>
2. <span data-ttu-id="66747-107">Vyhledejte na seznamu požadovaný záznam a vyberte ho.</span><span class="sxs-lookup"><span data-stu-id="66747-107">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="66747-108">V podokně akcí klikněte na možnost Obecné.</span><span class="sxs-lookup"><span data-stu-id="66747-108">On the Action Pane, click General.</span></span>
4. <span data-ttu-id="66747-109">Klikněte na možnost Mezipodnikové.</span><span class="sxs-lookup"><span data-stu-id="66747-109">Click Intercompany.</span></span>
5. <span data-ttu-id="66747-110">Nastavte položku Aktivní na hodnotu Ano, chcete-li povolit mezipodnikové obchodování.</span><span class="sxs-lookup"><span data-stu-id="66747-110">Set Active to Yes to enable intercompany trading.</span></span>
6. <span data-ttu-id="66747-111">V poli Společnost odběratele zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="66747-111">In the Customer company field, enter or select a value.</span></span>
7. <span data-ttu-id="66747-112">V poli Můj účet zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="66747-112">In the My account field, enter or select a value.</span></span>
8. <span data-ttu-id="66747-113">Klikněte na položku Uložit.</span><span class="sxs-lookup"><span data-stu-id="66747-113">Click Save.</span></span>
9. <span data-ttu-id="66747-114">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="66747-114">Close the page.</span></span>
10. <span data-ttu-id="66747-115">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="66747-115">Close the page.</span></span>
11. <span data-ttu-id="66747-116">Přejděte na Řízení a účetnictví projektů > Nastavení > Parametry modulu Řízení a účetnictví projektu.</span><span class="sxs-lookup"><span data-stu-id="66747-116">Go to Project management and accounting > Setup > Project management and accounting parameters.</span></span>
12. <span data-ttu-id="66747-117">Klikněte na kartu Mezipodnikové.</span><span class="sxs-lookup"><span data-stu-id="66747-117">Click the Intercompany tab.</span></span>
13. <span data-ttu-id="66747-118">Posuňte posuvník na Ano, abyste povolili mezipodnikové plánování prostředků a časové rozvrhy.</span><span class="sxs-lookup"><span data-stu-id="66747-118">Move the slider to Yes to enable intercompany resource scheduling and timesheets.</span></span>
14. <span data-ttu-id="66747-119">Označte v seznamu vybraný řádek.</span><span class="sxs-lookup"><span data-stu-id="66747-119">In the list, mark the selected row.</span></span>
15. <span data-ttu-id="66747-120">Klikněte na možnost Nový.</span><span class="sxs-lookup"><span data-stu-id="66747-120">Click New.</span></span>
16. <span data-ttu-id="66747-121">Označte v seznamu vybraný řádek.</span><span class="sxs-lookup"><span data-stu-id="66747-121">In the list, mark the selected row.</span></span>
17. <span data-ttu-id="66747-122">V poli Právnická osoba, která si půjčuje, zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="66747-122">In the Borrowing legal entity field, enter or select a value.</span></span>
18. <span data-ttu-id="66747-123">Zaškrtněte pole Časově rozlišené výnosy.</span><span class="sxs-lookup"><span data-stu-id="66747-123">Select the Accrue revenue check box.</span></span>
19. <span data-ttu-id="66747-124">V poli Výchozí kategorie časového rozvrhu zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="66747-124">In the Default timesheet category field, enter or select a value.</span></span>
20. <span data-ttu-id="66747-125">V poli Výchozí kategorie výdajů zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="66747-125">In the Default expense category field, enter or select a value.</span></span>
21. <span data-ttu-id="66747-126">Klikněte na položku Uložit.</span><span class="sxs-lookup"><span data-stu-id="66747-126">Click Save.</span></span>
22. <span data-ttu-id="66747-127">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="66747-127">Close the page.</span></span>
23. <span data-ttu-id="66747-128">Přejděte k Řízení a účetnictví projektu > Nastavení > Zaúčtování > Nastavení účtování hlavní knihy.</span><span class="sxs-lookup"><span data-stu-id="66747-128">Go to Project management and accounting > Setup > Posting > Ledger posting setup.</span></span>
24. <span data-ttu-id="66747-129">V poli Typy účtů hlavní knihy vyberte možnost.</span><span class="sxs-lookup"><span data-stu-id="66747-129">In the Ledger account types field, select an option.</span></span>
25. <span data-ttu-id="66747-130">Klepněte na možnost Nový.</span><span class="sxs-lookup"><span data-stu-id="66747-130">Click New.</span></span>
26. <span data-ttu-id="66747-131">Označte na seznamu vybraný řádek.</span><span class="sxs-lookup"><span data-stu-id="66747-131">In the list, mark the selected row.</span></span>
27. <span data-ttu-id="66747-132">Označte v seznamu vybraný řádek.</span><span class="sxs-lookup"><span data-stu-id="66747-132">In the list, mark the selected row.</span></span>
28. <span data-ttu-id="66747-133">Zadejte požadované hodnoty do pole Hlavní účet.</span><span class="sxs-lookup"><span data-stu-id="66747-133">In the Main account field, specify the desired values.</span></span>
29. <span data-ttu-id="66747-134">Klikněte na položku Uložit.</span><span class="sxs-lookup"><span data-stu-id="66747-134">Click Save.</span></span>
30. <span data-ttu-id="66747-135">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="66747-135">Close the page.</span></span>
31. <span data-ttu-id="66747-136">Přejděte na Řízení a účetnictví projektu > Nastavení > Ceny > Převést cenu.</span><span class="sxs-lookup"><span data-stu-id="66747-136">Go to Project management and accounting > Setup > Prices > Transfer price.</span></span>
32. <span data-ttu-id="66747-137">Klikněte na položku Nová.</span><span class="sxs-lookup"><span data-stu-id="66747-137">Click New.</span></span>
33. <span data-ttu-id="66747-138">Zadejte datum do pole Datum platnosti.</span><span class="sxs-lookup"><span data-stu-id="66747-138">In the Effective date field, enter a date.</span></span>
34. <span data-ttu-id="66747-139">V poli Právnická osoba, která si půjčuje, zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="66747-139">In the Borrowing legal entity field, enter or select a value.</span></span>
35. <span data-ttu-id="66747-140">V poli Model přenosu ceny zvolte možnost.</span><span class="sxs-lookup"><span data-stu-id="66747-140">In the Transfer price model field, select an option.</span></span>
36. <span data-ttu-id="66747-141">Do pole Oceňování zadejte číslo.</span><span class="sxs-lookup"><span data-stu-id="66747-141">In the Pricing field, enter a number.</span></span>
37. <span data-ttu-id="66747-142">Klikněte na položku Uložit.</span><span class="sxs-lookup"><span data-stu-id="66747-142">Click Save.</span></span>


