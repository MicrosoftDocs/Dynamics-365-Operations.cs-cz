---
title: " Základní cena a obchodní smlouvy"
description: Tato procedura vás provede postupem vytváření obchodních smluv prodejních cen specifických pro kanál.
author: josaw1
manager: AnnBe
ms.date: 08/12/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PriceDiscGroup, RetailStoreTable, RetailChannelPriceGroup, EcoResProductDetailsExtended, PriceDiscAdmTable, PriceDiscAdm
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 8138b6144cc6ba09834f2bfb61cc7334767307d6
ms.sourcegitcommit: cbcf344b3b552acca56c3e27606eac7f2f124afe
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/22/2019
ms.locfileid: "1916546"
---
# <a name="base-price-and-trade-agreements"></a><span data-ttu-id="01bdd-103"> Základní cena a obchodní smlouvy</span><span class="sxs-lookup"><span data-stu-id="01bdd-103">Base price and trade agreements</span></span>

[!include[task guide banner](../includes/task-guide-banner.md)]

<span data-ttu-id="01bdd-104">Tato procedura vás provede postupem vytváření obchodních smluv prodejních cen specifických pro kanál.</span><span class="sxs-lookup"><span data-stu-id="01bdd-104">This procedure walks through creating channel-specific sales price trade agreements.</span></span> <span data-ttu-id="01bdd-105">Tato procedura používá data ukázkové společnosti USRT.</span><span class="sxs-lookup"><span data-stu-id="01bdd-105">This procedure uses the USRT demo data company.</span></span>

1. <span data-ttu-id="01bdd-106">V **navigačním podokně** přejděte na **Moduly > Maloobchodní a velkoobchodní prodej > Správa cen a slev > Cenové skupiny > Všechny cenové skupiny**.</span><span class="sxs-lookup"><span data-stu-id="01bdd-106">In the **Navigation pane**, go to **Modules > Retail and commerce > Pricing and discounts management > Price groups > All price groups**.</span></span> <span data-ttu-id="01bdd-107">Cenové skupiny představují způsob přiřazování obchodních smluv konkrétním kanálům.</span><span class="sxs-lookup"><span data-stu-id="01bdd-107">Price groups are how trade agreements are assigned to specific channels.</span></span> <span data-ttu-id="01bdd-108">Pomocí cenových skupin pro přiřazení obchodních smluv kanálu lze určovat ceny specifické pro kanál.</span><span class="sxs-lookup"><span data-stu-id="01bdd-108">Using price groups to assign trade agreements to a channel enables channel-specific pricing.</span></span>  
2. <span data-ttu-id="01bdd-109">Klepněte na možnost **Nový**.</span><span class="sxs-lookup"><span data-stu-id="01bdd-109">Click **New**.</span></span>
3. <span data-ttu-id="01bdd-110">Zadejte hodnotu do pole **Cenové skupiny**.</span><span class="sxs-lookup"><span data-stu-id="01bdd-110">In the **Price groups** field, type a value.</span></span>
4. <span data-ttu-id="01bdd-111">Zadejte hodnotu do pole **Název**.</span><span class="sxs-lookup"><span data-stu-id="01bdd-111">In the **Name** field, type a value.</span></span>
5. <span data-ttu-id="01bdd-112">Klikněte na možnost **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="01bdd-112">Click **Save**.</span></span>
6. <span data-ttu-id="01bdd-113">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="01bdd-113">Close the page.</span></span>
7. <span data-ttu-id="01bdd-114">V **Navigačním podokně** přejděte na **Moduly > Maloobchodní a velkoobchodní prodej > Kanály > Maloobchody > Všechny maloobchody**.</span><span class="sxs-lookup"><span data-stu-id="01bdd-114">In the **Navigation pane**, go to **Modules > Retail and commerce > Channels > Retail stores > All retail stores**.</span></span>
8. <span data-ttu-id="01bdd-115">Ze seznamu vyberte možnost „New York“.</span><span class="sxs-lookup"><span data-stu-id="01bdd-115">In the list, select 'New York'</span></span>
9. <span data-ttu-id="01bdd-116">V podokně akcí klikněte na možnost **Obchod**.</span><span class="sxs-lookup"><span data-stu-id="01bdd-116">On the Action Pane, click **Store**.</span></span>
10. <span data-ttu-id="01bdd-117">Klikněte na možnost **Cenové skupiny**.</span><span class="sxs-lookup"><span data-stu-id="01bdd-117">Click **Price groups**.</span></span>
11. <span data-ttu-id="01bdd-118">Klepněte na možnost **Nový**.</span><span class="sxs-lookup"><span data-stu-id="01bdd-118">Click **New**.</span></span>
12. <span data-ttu-id="01bdd-119">V poli **Cenové skupiny** kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.</span><span class="sxs-lookup"><span data-stu-id="01bdd-119">In the **Price groups** field, click the drop-down button to open the lookup.</span></span>
13. <span data-ttu-id="01bdd-120">Vyhledejte na seznamu požadovaný záznam a vyberte ho.</span><span class="sxs-lookup"><span data-stu-id="01bdd-120">In the list, find and select the desired record.</span></span>
14. <span data-ttu-id="01bdd-121">Klikněte na možnost **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="01bdd-121">Click **Save**.</span></span>
15. <span data-ttu-id="01bdd-122">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="01bdd-122">Close the page.</span></span>
16. <span data-ttu-id="01bdd-123">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="01bdd-123">Close the page.</span></span>
17. <span data-ttu-id="01bdd-124">V **navigačním podokně** přejděte na **Moduly > Maloobchodní a velkoobchodní prodej > Produkty a kategorie > Uvolněné produkty podle kategorie**.</span><span class="sxs-lookup"><span data-stu-id="01bdd-124">In the **Navigation pane**, go to **Modules > Retail and commerce > Products and categories > Released products by category**.</span></span>
18. <span data-ttu-id="01bdd-125">Klikněte na odkaz na vybraném řádku v seznamu.</span><span class="sxs-lookup"><span data-stu-id="01bdd-125">In the list, click the link in the selected row.</span></span>
19. <span data-ttu-id="01bdd-126">Klikněte na možnost **Upravit**.</span><span class="sxs-lookup"><span data-stu-id="01bdd-126">Click **Edit**.</span></span>
20. <span data-ttu-id="01bdd-127">Rozbalte záložku s náhledem **Prodej**.</span><span class="sxs-lookup"><span data-stu-id="01bdd-127">Expand the **Sell** fastTab.</span></span>
21. <span data-ttu-id="01bdd-128">Zadejte číslo do pole **Cena**.</span><span class="sxs-lookup"><span data-stu-id="01bdd-128">In the **Price** field, enter a number.</span></span> <span data-ttu-id="01bdd-129">Tato cena je použita, pokud jsou nalezeny žádné použitelné obchodní smlouvy.</span><span class="sxs-lookup"><span data-stu-id="01bdd-129">This price is used if no applicable trade agreements are found.</span></span>  
22. <span data-ttu-id="01bdd-130">Klikněte na možnost **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="01bdd-130">Click **Save**.</span></span>
23. <span data-ttu-id="01bdd-131">V **podokně akcí** klikněte na možnost **Prodej**.</span><span class="sxs-lookup"><span data-stu-id="01bdd-131">On the **Action Pane**, click **Sell**.</span></span>
24. <span data-ttu-id="01bdd-132">Klikněte na **Vytvořit obchodní smlouvy**.</span><span class="sxs-lookup"><span data-stu-id="01bdd-132">Click **Create trade agreements**.</span></span>
25. <span data-ttu-id="01bdd-133">Klepněte na možnost **Nový**.</span><span class="sxs-lookup"><span data-stu-id="01bdd-133">Click **New**.</span></span>
26. <span data-ttu-id="01bdd-134">V poli **Název** kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.</span><span class="sxs-lookup"><span data-stu-id="01bdd-134">In the **Name** field, click the drop-down button to open the lookup.</span></span>
27. <span data-ttu-id="01bdd-135">Vyberte ze seznamu možnost „Maloobchod“.</span><span class="sxs-lookup"><span data-stu-id="01bdd-135">In the list, select 'Retail'.</span></span> <span data-ttu-id="01bdd-136">V ukázkových datech má deník s názvem „Maloobchod“ výchozí vztah „Cena (prodej)“.</span><span class="sxs-lookup"><span data-stu-id="01bdd-136">In the demo data, the 'Retail' journal name has the default relation of 'Price (sales)'.</span></span> <span data-ttu-id="01bdd-137">To znamená, že všechny vytvořené nové řádky budou přednastaveny jako výchozí prodejní ceny obchodních smluv.</span><span class="sxs-lookup"><span data-stu-id="01bdd-137">That means all new lines created will default to sales price trade agreements.</span></span>  
28. <span data-ttu-id="01bdd-138">V **Podokně akcí** klikněte na **Řádky**.</span><span class="sxs-lookup"><span data-stu-id="01bdd-138">On the **Action pane**, click **Lines**.</span></span>
29. <span data-ttu-id="01bdd-139">V poli **Kód účtu** vyberte možnost „Skupina“.</span><span class="sxs-lookup"><span data-stu-id="01bdd-139">In the **Account code** field, select 'Group'.</span></span>
30. <span data-ttu-id="01bdd-140">V poli **Výběr účtu** kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.</span><span class="sxs-lookup"><span data-stu-id="01bdd-140">In the **Account selection** field, click the drop-down button to open the lookup.</span></span>
31. <span data-ttu-id="01bdd-141">Vyhledejte na seznamu požadovaný záznam a vyberte ho.</span><span class="sxs-lookup"><span data-stu-id="01bdd-141">In the list, find and select the desired record.</span></span> <span data-ttu-id="01bdd-142">Tím dokončíte propojení kanálu se skupinou cen pro obchodní smlouvu.</span><span class="sxs-lookup"><span data-stu-id="01bdd-142">This will complete the link from Channel to Price group to Trade agreement.</span></span>  
32. <span data-ttu-id="01bdd-143">Zadejte hodnotu do pole **Vztah položky**.</span><span class="sxs-lookup"><span data-stu-id="01bdd-143">In the **Item relation** field, type a value.</span></span>
33. <span data-ttu-id="01bdd-144">Zadejte číslo do pole **Částka v měně**.</span><span class="sxs-lookup"><span data-stu-id="01bdd-144">In the **Amount in currency** field, enter a number.</span></span>
34. <span data-ttu-id="01bdd-145">Na záložce s náhledem **Podrobnosti** zaškrtněte nebo zrušte zaškrtnutí políčka **Najít další**.</span><span class="sxs-lookup"><span data-stu-id="01bdd-145">In the **Details** fastTab, check or uncheck the **Find next** checkbox.</span></span> <span data-ttu-id="01bdd-146">Pokud možnost **Najít další** je nastavena na hodnotu „Ano“, bude oceňovací modul dále hledat použitelné obchodní smlouvy s nižší prodejní cenou.</span><span class="sxs-lookup"><span data-stu-id="01bdd-146">When **Find next** is set to 'Yes', the pricing engine will continue to search for applicable trade agreements with a lower sale price.</span></span> <span data-ttu-id="01bdd-147">Pokud je možnost **Najít další** nastavena na hodnotu „Ne“, oceňovací modul zastaví hledání a použije obchodní smlouvu.</span><span class="sxs-lookup"><span data-stu-id="01bdd-147">When **Find next** is set to 'No', the price engine stops searching and uses the trade agreement.</span></span>  
35. <span data-ttu-id="01bdd-148">Klikněte na možnost **Zaúčtovat**.</span><span class="sxs-lookup"><span data-stu-id="01bdd-148">Click **Post**.</span></span>
36. <span data-ttu-id="01bdd-149">Klikněte na tlačítko **OK**.</span><span class="sxs-lookup"><span data-stu-id="01bdd-149">Click **OK**.</span></span>
37. <span data-ttu-id="01bdd-150">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="01bdd-150">Close the page.</span></span>
38. <span data-ttu-id="01bdd-151">V **podokně akcí** klikněte na možnost Prodej.</span><span class="sxs-lookup"><span data-stu-id="01bdd-151">On the **Action Pane**, click Sell.</span></span>
39. <span data-ttu-id="01bdd-152">Klikněte na možnost **Prodejní cena**.</span><span class="sxs-lookup"><span data-stu-id="01bdd-152">Click **Sales price**.</span></span>

