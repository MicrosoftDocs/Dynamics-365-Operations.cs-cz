---
title: Konfigurace fakturování mezipodnikového projektu
description: Tento postup popisuje nastavení fakturace projektu mezi dvěma společnostmi v rámci organizace.
author: KimANelson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: VendTable, InterCompanyTradingRelationSetupVendor, SysDataAreaSelectLookup, ProjParameters, ProjPosting, ProjTransferPrice
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Service industries
ms.author: knelson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 2fe06978d3a1c41a1133a568cca61df05b49d235
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/15/2019
ms.locfileid: "1572412"
---
# <a name="configure-intercompany-project-invoicing"></a><span data-ttu-id="e64df-103">Konfigurace fakturování mezipodnikového projektu</span><span class="sxs-lookup"><span data-stu-id="e64df-103">Configure intercompany project invoicing</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="e64df-104">Tento postup popisuje nastavení fakturace projektu mezi dvěma společnostmi v rámci organizace.</span><span class="sxs-lookup"><span data-stu-id="e64df-104">This procedure shows how to set up project invoicing between two companies in your organization.</span></span> <span data-ttu-id="e64df-105">Tato úloha používá sadu dat USSI.</span><span class="sxs-lookup"><span data-stu-id="e64df-105">This task uses the USSI data set.</span></span>

1. <span data-ttu-id="e64df-106">Přejděte do části Závazky > Dodavatelé > Všichni dodavatelé.</span><span class="sxs-lookup"><span data-stu-id="e64df-106">Go to Accounts payable > Vendors > All vendors.</span></span>
2. <span data-ttu-id="e64df-107">Vyhledejte na seznamu požadovaný záznam a vyberte ho.</span><span class="sxs-lookup"><span data-stu-id="e64df-107">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="e64df-108">V podokně akcí klikněte na možnost Obecné.</span><span class="sxs-lookup"><span data-stu-id="e64df-108">On the Action Pane, click General.</span></span>
4. <span data-ttu-id="e64df-109">Klikněte na možnost Mezipodnikové.</span><span class="sxs-lookup"><span data-stu-id="e64df-109">Click Intercompany.</span></span>
5. <span data-ttu-id="e64df-110">Nastavte položku Aktivní na hodnotu Ano, chcete-li povolit mezipodnikové obchodování.</span><span class="sxs-lookup"><span data-stu-id="e64df-110">Set Active to Yes to enable intercompany trading.</span></span>
6. <span data-ttu-id="e64df-111">V poli Společnost odběratele zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="e64df-111">In the Customer company field, enter or select a value.</span></span>
7. <span data-ttu-id="e64df-112">V poli Můj účet zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="e64df-112">In the My account field, enter or select a value.</span></span>
8. <span data-ttu-id="e64df-113">Klikněte na položku Uložit.</span><span class="sxs-lookup"><span data-stu-id="e64df-113">Click Save.</span></span>
9. <span data-ttu-id="e64df-114">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="e64df-114">Close the page.</span></span>
10. <span data-ttu-id="e64df-115">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="e64df-115">Close the page.</span></span>
11. <span data-ttu-id="e64df-116">Přejděte na Řízení a účetnictví projektů > Nastavení > Parametry modulu Řízení a účetnictví projektu.</span><span class="sxs-lookup"><span data-stu-id="e64df-116">Go to Project management and accounting > Setup > Project management and accounting parameters.</span></span>
12. <span data-ttu-id="e64df-117">Klikněte na kartu Mezipodnikové.</span><span class="sxs-lookup"><span data-stu-id="e64df-117">Click the Intercompany tab.</span></span>
13. <span data-ttu-id="e64df-118">Posuňte posuvník na Ano, abyste povolili mezipodnikové plánování prostředků a časové rozvrhy.</span><span class="sxs-lookup"><span data-stu-id="e64df-118">Move the slider to Yes to enable intercompany resource scheduling and timesheets.</span></span>
14. <span data-ttu-id="e64df-119">Označte v seznamu vybraný řádek.</span><span class="sxs-lookup"><span data-stu-id="e64df-119">In the list, mark the selected row.</span></span>
15. <span data-ttu-id="e64df-120">Klikněte na možnost Nový.</span><span class="sxs-lookup"><span data-stu-id="e64df-120">Click New.</span></span>
16. <span data-ttu-id="e64df-121">Označte v seznamu vybraný řádek.</span><span class="sxs-lookup"><span data-stu-id="e64df-121">In the list, mark the selected row.</span></span>
17. <span data-ttu-id="e64df-122">V poli Právnická osoba, která si půjčuje, zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="e64df-122">In the Borrowing legal entity field, enter or select a value.</span></span>
18. <span data-ttu-id="e64df-123">Zaškrtněte pole Časově rozlišené výnosy.</span><span class="sxs-lookup"><span data-stu-id="e64df-123">Select the Accrue revenue check box.</span></span>
19. <span data-ttu-id="e64df-124">V poli Výchozí kategorie časového rozvrhu zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="e64df-124">In the Default timesheet category field, enter or select a value.</span></span>
20. <span data-ttu-id="e64df-125">V poli Výchozí kategorie výdajů zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="e64df-125">In the Default expense category field, enter or select a value.</span></span>
21. <span data-ttu-id="e64df-126">Klikněte na položku Uložit.</span><span class="sxs-lookup"><span data-stu-id="e64df-126">Click Save.</span></span>
22. <span data-ttu-id="e64df-127">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="e64df-127">Close the page.</span></span>
23. <span data-ttu-id="e64df-128">Přejděte k Řízení a účetnictví projektu > Nastavení > Zaúčtování > Nastavení účtování hlavní knihy.</span><span class="sxs-lookup"><span data-stu-id="e64df-128">Go to Project management and accounting > Setup > Posting > Ledger posting setup.</span></span>
24. <span data-ttu-id="e64df-129">V poli Typy účtů hlavní knihy vyberte možnost.</span><span class="sxs-lookup"><span data-stu-id="e64df-129">In the Ledger account types field, select an option.</span></span>
25. <span data-ttu-id="e64df-130">Klepněte na možnost Nový.</span><span class="sxs-lookup"><span data-stu-id="e64df-130">Click New.</span></span>
26. <span data-ttu-id="e64df-131">Označte na seznamu vybraný řádek.</span><span class="sxs-lookup"><span data-stu-id="e64df-131">In the list, mark the selected row.</span></span>
27. <span data-ttu-id="e64df-132">Označte v seznamu vybraný řádek.</span><span class="sxs-lookup"><span data-stu-id="e64df-132">In the list, mark the selected row.</span></span>
28. <span data-ttu-id="e64df-133">Zadejte požadované hodnoty do pole Hlavní účet.</span><span class="sxs-lookup"><span data-stu-id="e64df-133">In the Main account field, specify the desired values.</span></span>
29. <span data-ttu-id="e64df-134">Klikněte na položku Uložit.</span><span class="sxs-lookup"><span data-stu-id="e64df-134">Click Save.</span></span>
30. <span data-ttu-id="e64df-135">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="e64df-135">Close the page.</span></span>
31. <span data-ttu-id="e64df-136">Přejděte na Řízení a účetnictví projektu > Nastavení > Ceny > Převést cenu.</span><span class="sxs-lookup"><span data-stu-id="e64df-136">Go to Project management and accounting > Setup > Prices > Transfer price.</span></span>
32. <span data-ttu-id="e64df-137">Klikněte na položku Nová.</span><span class="sxs-lookup"><span data-stu-id="e64df-137">Click New.</span></span>
33. <span data-ttu-id="e64df-138">Zadejte datum do pole Datum platnosti.</span><span class="sxs-lookup"><span data-stu-id="e64df-138">In the Effective date field, enter a date.</span></span>
34. <span data-ttu-id="e64df-139">V poli Právnická osoba, která si půjčuje, zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="e64df-139">In the Borrowing legal entity field, enter or select a value.</span></span>
35. <span data-ttu-id="e64df-140">V poli Model přenosu ceny zvolte možnost.</span><span class="sxs-lookup"><span data-stu-id="e64df-140">In the Transfer price model field, select an option.</span></span>
36. <span data-ttu-id="e64df-141">Do pole Oceňování zadejte číslo.</span><span class="sxs-lookup"><span data-stu-id="e64df-141">In the Pricing field, enter a number.</span></span>
37. <span data-ttu-id="e64df-142">Klikněte na položku Uložit.</span><span class="sxs-lookup"><span data-stu-id="e64df-142">Click Save.</span></span>

