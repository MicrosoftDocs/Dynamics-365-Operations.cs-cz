---
title: Inicializace úrovní zásob ve skladu
description: Tento postup popisuje, jak manuálně aktualizovat zásoby na skladě pomocí deníku pohybu zásob.
author: perlynne
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventJournalMovement, InventJournalCreate, InventItemIdLookupSimple, InventLocationIdLookup, WMSLocationIdLookup
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 3f922620c7aeeafd8560316239875c1ec5486191
ms.sourcegitcommit: fcb27d6a46cd544feef34f6ec7607bdd46b0c12b
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/18/2020
ms.locfileid: "3145679"
---
# <a name="initialize-stock-levels-in-the-warehouse"></a><span data-ttu-id="377d2-103">Inicializace úrovní zásob ve skladu</span><span class="sxs-lookup"><span data-stu-id="377d2-103">Initialize stock levels in the warehouse</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="377d2-104">Tento postup popisuje, jak manuálně aktualizovat zásoby na skladě pomocí deníku pohybu zásob.</span><span class="sxs-lookup"><span data-stu-id="377d2-104">This procedure shows you how to get the on-hand inventory updated manually using an Inventory movement journal.</span></span> <span data-ttu-id="377d2-105">(Lze rovněž aktualizovat zásoby na skladě pomocí importu transakcí v datových entitách.) Tohoto průvodce můžete spustit v ukázkových datech společnosti USMF, kde všechny požadavky, jako je název deníku, nastavení položky, účetní profily nebo účty jsou k dispozici.</span><span class="sxs-lookup"><span data-stu-id="377d2-105">(It's also possible to update on-hand inventory by importing transactions in data entities.) You can run this guide in demo data company USMF where all the prerequisites like journal name, item setup, posting profiles, and accounts are available.</span></span> <span data-ttu-id="377d2-106">Průvodce navrhuje hodnoty specifické pro položku a dimenze, které se používají.</span><span class="sxs-lookup"><span data-stu-id="377d2-106">The guide suggests specific values for the item and dimensions that are used.</span></span> <span data-ttu-id="377d2-107">Pokud vyberete jinou položku, může být vyžadováno zadání hodnot pro různé dimenze.</span><span class="sxs-lookup"><span data-stu-id="377d2-107">If you choose a different item, you may need to enter values for different dimensions.</span></span>

1. <span data-ttu-id="377d2-108">Přejděte do Řízení zásob > Položky deníku > Zboží > Pohyb.</span><span class="sxs-lookup"><span data-stu-id="377d2-108">Go to Inventory management > Journal entries > Items > Movement.</span></span>
2. <span data-ttu-id="377d2-109">Klikněte na položku Nová.</span><span class="sxs-lookup"><span data-stu-id="377d2-109">Click New.</span></span>
3. <span data-ttu-id="377d2-110">V poli Název kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.</span><span class="sxs-lookup"><span data-stu-id="377d2-110">In the Name field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="377d2-111">Vyberte pohyb zboží</span><span class="sxs-lookup"><span data-stu-id="377d2-111">Select IMov.</span></span>
    * <span data-ttu-id="377d2-112">Je vhodné použít jiné šablony názvů deníků pro jiné obchodní účely.</span><span class="sxs-lookup"><span data-stu-id="377d2-112">It's a good practice to use different journal name templates for the different business purposes.</span></span>  
5. <span data-ttu-id="377d2-113">Klikněte na odkaz na vybraném řádku v seznamu.</span><span class="sxs-lookup"><span data-stu-id="377d2-113">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="377d2-114">Zadejte hodnotu „140200“ do pole Protiúčet.</span><span class="sxs-lookup"><span data-stu-id="377d2-114">In the Offset account field, specify the values '140200'.</span></span>
    * <span data-ttu-id="377d2-115">Toto je protiúčet, který bude výchozím protiúčtem na řádcích deníku.</span><span class="sxs-lookup"><span data-stu-id="377d2-115">This is the offset account that will be the default account on the journal lines.</span></span> <span data-ttu-id="377d2-116">Je možné přepsat výchozí nastavení pro přiřazení různých protiúčtů na každém řádku.</span><span class="sxs-lookup"><span data-stu-id="377d2-116">It's possible to override the default to assign different offset accounts per line.</span></span>  
7. <span data-ttu-id="377d2-117">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="377d2-117">Click OK.</span></span>
8. <span data-ttu-id="377d2-118">Klikněte na položku Nová.</span><span class="sxs-lookup"><span data-stu-id="377d2-118">Click New.</span></span>
9. <span data-ttu-id="377d2-119">V poli Číslo zboží kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.</span><span class="sxs-lookup"><span data-stu-id="377d2-119">In the Item number field, click the drop-down button to open the lookup.</span></span>
10. <span data-ttu-id="377d2-120">Vyberte položku A0001.</span><span class="sxs-lookup"><span data-stu-id="377d2-120">Select item A0001.</span></span>
11. <span data-ttu-id="377d2-121">Klikněte na odkaz na vybraném řádku v seznamu.</span><span class="sxs-lookup"><span data-stu-id="377d2-121">In the list, click the link in the selected row.</span></span>
12. <span data-ttu-id="377d2-122">Klepněte na kartu Dimenze zásob.</span><span class="sxs-lookup"><span data-stu-id="377d2-122">Click the Inventory dimensions tab.</span></span>
13. <span data-ttu-id="377d2-123">V poli Lokalita kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.</span><span class="sxs-lookup"><span data-stu-id="377d2-123">In the Site field, click the drop-down button to open the lookup.</span></span>
14. <span data-ttu-id="377d2-124">Vyberte lokalitu 1.</span><span class="sxs-lookup"><span data-stu-id="377d2-124">Select site 1.</span></span>
15. <span data-ttu-id="377d2-125">V poli Sklad kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.</span><span class="sxs-lookup"><span data-stu-id="377d2-125">In the Warehouse field, click the drop-down button to open the lookup.</span></span>
16. <span data-ttu-id="377d2-126">Vyberte sklad 13.</span><span class="sxs-lookup"><span data-stu-id="377d2-126">Select warehouse 13.</span></span>
17. <span data-ttu-id="377d2-127">Klikněte na odkaz na vybraném řádku v seznamu.</span><span class="sxs-lookup"><span data-stu-id="377d2-127">In the list, click the link in the selected row.</span></span>
18. <span data-ttu-id="377d2-128">V poli Umístění kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.</span><span class="sxs-lookup"><span data-stu-id="377d2-128">In the Location field, click the drop-down button to open the lookup.</span></span>
19. <span data-ttu-id="377d2-129">Vyberte umístění 13.</span><span class="sxs-lookup"><span data-stu-id="377d2-129">Select location 13.</span></span>
20. <span data-ttu-id="377d2-130">Zadejte číslo do pole Množství.</span><span class="sxs-lookup"><span data-stu-id="377d2-130">In the Quantity field, enter a number.</span></span>
21. <span data-ttu-id="377d2-131">Klikněte na položku Uložit.</span><span class="sxs-lookup"><span data-stu-id="377d2-131">Click Save.</span></span>
22. <span data-ttu-id="377d2-132">Klikněte na položku Zaúčtovat.</span><span class="sxs-lookup"><span data-stu-id="377d2-132">Click Post.</span></span>
23. <span data-ttu-id="377d2-133">Zaškrtněte nebo zrušte zaškrtnutí políčka Převést všechny chyby zaúčtování do nového deníku.</span><span class="sxs-lookup"><span data-stu-id="377d2-133">Check or uncheck the Transfer all posting errors to a new journal check box.</span></span>
    * <span data-ttu-id="377d2-134">Povolíte-li tuto možnost, budou do nového deníku zkopírovány všechny řádky, které se nepodařilo se zaúčtovat.</span><span class="sxs-lookup"><span data-stu-id="377d2-134">If you enable this option, any lines that fail to post will be copied to a new journal.</span></span> <span data-ttu-id="377d2-135">Informace můžete do protokolu za účelem opravy problémů a poté zaúčtovat řádky znovu.</span><span class="sxs-lookup"><span data-stu-id="377d2-135">You can use the information in the log to correct the issues and then re-post the lines.</span></span>  
24. <span data-ttu-id="377d2-136">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="377d2-136">Click OK.</span></span>
25. <span data-ttu-id="377d2-137">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="377d2-137">Close the page.</span></span>
26. <span data-ttu-id="377d2-138">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="377d2-138">Close the page.</span></span>

