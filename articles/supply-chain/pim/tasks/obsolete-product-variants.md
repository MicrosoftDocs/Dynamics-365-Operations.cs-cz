---
title: Nalezení zastaralých variant produktů
description: Tato procedura ukazuje, jak nalézt zastaralé uvolněné produkty nebo varianty produktu a jak přiřadit stav životního cyklu produktu k zastaralým produktům.
author: cvocph
manager: AnnBe
ms.date: 12/05/2017
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.author: conradv
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: dcd0f67bae1042cb1e81423898eacd20f921e0e2
ms.sourcegitcommit: fcb27d6a46cd544feef34f6ec7607bdd46b0c12b
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/18/2020
ms.locfileid: "3147569"
---
# <a name="find-obsolete-product-variants"></a><span data-ttu-id="472d5-103">Nalezení zastaralých variant produktů</span><span class="sxs-lookup"><span data-stu-id="472d5-103">Find obsolete product variants</span></span> 

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="472d5-104">Tato procedura ukazuje, jak nalézt zastaralé uvolněné produkty nebo varianty produktu a jak přiřadit stav životního cyklu produktu k zastaralým produktům.</span><span class="sxs-lookup"><span data-stu-id="472d5-104">This procedure shows how to find obsolete released products or product variants and how to associate a product lifecycle state to the obsolete products.</span></span> <span data-ttu-id="472d5-105">Předpoklad: Je nutné definovat nejméně jeden stav životního cyklu produktu, který není aktivní pro plánování, ještě před přehráním tohoto Průvodce záznamem úloh.</span><span class="sxs-lookup"><span data-stu-id="472d5-105">Prerequisite: You need to define at least one product lifecycle state that is inactive for planning before you can play this task guide.</span></span>


## <a name="run-a-simulation"></a><span data-ttu-id="472d5-106">Spuštění simulace ceny</span><span class="sxs-lookup"><span data-stu-id="472d5-106">Run a simulation</span></span>
1. <span data-ttu-id="472d5-107">Přejděte na Správa informací o produktech > Pravidelné úlohy > Změnit stav životního cyklu zastaralé produktů.</span><span class="sxs-lookup"><span data-stu-id="472d5-107">Go to Product information management > Periodic tasks > Change lifecycle state for obsolete products.</span></span>
2. <span data-ttu-id="472d5-108">V poli Stav cyklu životnosti nového produktu zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="472d5-108">In the New product lifecycle state field, enter or select a value.</span></span>
3. <span data-ttu-id="472d5-109">V datovém poli Spustit simulaci bez aktualizace dat produktu vyberte Ano.</span><span class="sxs-lookup"><span data-stu-id="472d5-109">Select Yes in the Run simulation without updating product data field.</span></span>
4. <span data-ttu-id="472d5-110">V poli Vyloučit produkty vytvořené za tento počet dní zadejte číslici.</span><span class="sxs-lookup"><span data-stu-id="472d5-110">In the Exclude products created within this number of days field, enter a number.</span></span>
5. <span data-ttu-id="472d5-111">V poli Vyloučit produkty používané v transakcích (za tento počet) dní zadejte číslici.</span><span class="sxs-lookup"><span data-stu-id="472d5-111">In the Exclude products used in transactions (in number of days) field, enter a number.</span></span>
6. <span data-ttu-id="472d5-112">Rozbalte oddíl Záznamy k zahrnutí.</span><span class="sxs-lookup"><span data-stu-id="472d5-112">Expand the Records to include section.</span></span>
7. <span data-ttu-id="472d5-113">Klepněte na tlačítko Filtr.</span><span class="sxs-lookup"><span data-stu-id="472d5-113">Click Filter.</span></span>
8. <span data-ttu-id="472d5-114">Označte v seznamu vybraný řádek.</span><span class="sxs-lookup"><span data-stu-id="472d5-114">In the list, mark the selected row.</span></span>
9. <span data-ttu-id="472d5-115">Zadejte hodnotu do pole Kritéria.</span><span class="sxs-lookup"><span data-stu-id="472d5-115">In the Criteria field, type a value.</span></span>
10. <span data-ttu-id="472d5-116">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="472d5-116">Click OK.</span></span>
11. <span data-ttu-id="472d5-117">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="472d5-117">Click OK.</span></span>

> [!NOTE]
> <span data-ttu-id="472d5-118">Doporučujeme spustit simulaci v dávce, pokud plánujete vyhledávat velký počet produktů.</span><span class="sxs-lookup"><span data-stu-id="472d5-118">It is recommended to run the simulation in batch if you expect to search a large number of products.</span></span> <span data-ttu-id="472d5-119">Ujistěte se také, že simulace není spuštěna během nejaktivnější pracovní doby společnosti.</span><span class="sxs-lookup"><span data-stu-id="472d5-119">Also, make sure that the simulation is not run during the most active working time of the company.</span></span>  

## <a name="review-the-simulation-results"></a><span data-ttu-id="472d5-120">Projděte si výsledky simulace.</span><span class="sxs-lookup"><span data-stu-id="472d5-120">Review the simulation results</span></span>
1. <span data-ttu-id="472d5-121">Přejděte na možnost Správa informací o produktech > Dotazy a sestavy > Historie údržby stavu životního cyklu produktu.</span><span class="sxs-lookup"><span data-stu-id="472d5-121">Go to Product information management > Inquiries and reports > Product lifecycle state maintenance history.</span></span>
   
> [!NOTE]
> <span data-ttu-id="472d5-122">Na této stránce můžete zkontrolovat výsledky simulace a vyhodnotit počet produktů a variant produktů, který bude přidružen k novému stavu životního cyklu produktu při spuštění aktualizace bez simulace.</span><span class="sxs-lookup"><span data-stu-id="472d5-122">On this page, you can review the simulation results and make an assessment of how many products and product variants will be associated with a new product lifecycle state when running the update without simulation.</span></span>  

## <a name="run-the-update-of-the-product-lifecycle-state-for-obsolete-products"></a><span data-ttu-id="472d5-123">Spuštění aktualizace stavu životního cyklu produktu pro zastaralé produkty</span><span class="sxs-lookup"><span data-stu-id="472d5-123">Run the update of the Product lifecycle state for obsolete products</span></span>
1. <span data-ttu-id="472d5-124">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="472d5-124">Close the page.</span></span>
2. <span data-ttu-id="472d5-125">Přejděte na Správa informací o produktech > Pravidelné úlohy > Změnit stav životního cyklu zastaralé produktů.</span><span class="sxs-lookup"><span data-stu-id="472d5-125">Go to Product information management > Periodic tasks > Change lifecycle state for obsolete products.</span></span>
3. <span data-ttu-id="472d5-126">Rozbalte oddíl Záznamy k zahrnutí.</span><span class="sxs-lookup"><span data-stu-id="472d5-126">Expand the Records to include section.</span></span>

> [!NOTE]
> <span data-ttu-id="472d5-127">Všimněte si, že byl uložen poslední výběr.</span><span class="sxs-lookup"><span data-stu-id="472d5-127">Note that the last selection has been saved.</span></span>  

4. <span data-ttu-id="472d5-128">V datovém poli Spustit simulaci bez aktualizace dat produktu vyberte Ne.</span><span class="sxs-lookup"><span data-stu-id="472d5-128">Select No in the Run simulation without updating product data field.</span></span>
5. <span data-ttu-id="472d5-129">Rozbalte sekci Spustit na pozadí.</span><span class="sxs-lookup"><span data-stu-id="472d5-129">Expand the Run in the background section.</span></span>

> [!NOTE]
> <span data-ttu-id="472d5-130">V závislosti na počtu ovlivněných produktů a variant produktů zvažte tuto úlohu spustit jako dávku.</span><span class="sxs-lookup"><span data-stu-id="472d5-130">Depending on how many products and product variants are affected, consider running this job in batch.</span></span> <span data-ttu-id="472d5-131">Nespouštějte velkou úlohu aktualizace během nejvíce aktivní pracovní doby ve společnosti.</span><span class="sxs-lookup"><span data-stu-id="472d5-131">Make sure that you are not running a large update job during the most active working hours in the company.</span></span>  

6. <span data-ttu-id="472d5-132">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="472d5-132">Click OK.</span></span>
7. <span data-ttu-id="472d5-133">Přejděte na možnost Správa informací o produktech > Dotazy a sestavy > Historie údržby stavu životního cyklu produktu.</span><span class="sxs-lookup"><span data-stu-id="472d5-133">Go to Product information management > Inquiries and reports > Product lifecycle state maintenance history.</span></span>

> [!NOTE]
> <span data-ttu-id="472d5-134">Zkontrolujte změněné uvolněné produkty a varianty produktu.</span><span class="sxs-lookup"><span data-stu-id="472d5-134">Review the changed released products and product variants.</span></span>  

8. <span data-ttu-id="472d5-135">Vyhledejte na seznamu požadovaný záznam a vyberte ho.</span><span class="sxs-lookup"><span data-stu-id="472d5-135">In the list, find and select the desired record.</span></span>

