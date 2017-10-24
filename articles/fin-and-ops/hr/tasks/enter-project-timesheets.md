--- 
title: "Zadávání časových rozvrhů projektů"
description: "Tato procedura vám umožní vytvořit časový rozvrh pomocí prázdného formuláře časového rozvrhu."
author: kherr75
manager: AnnBe
ms.date: 11/10/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: rschloma
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Service industries
ms.author: kherr
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 1f88fbbacde9c0bd2b3499df5682a717d0b804ab
ms.contentlocale: cs-cz
ms.lasthandoff: 09/29/2017

---
# <a name="enter-project-timesheets"></a><span data-ttu-id="ccf2f-103">Zadávání časových rozvrhů projektů</span><span class="sxs-lookup"><span data-stu-id="ccf2f-103">Enter project timesheets</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="ccf2f-104">Tato procedura vám umožní vytvořit časový rozvrh pomocí prázdného formuláře časového rozvrhu.</span><span class="sxs-lookup"><span data-stu-id="ccf2f-104">This procedure lets you create a timesheet by using an empty timesheet form.</span></span> <span data-ttu-id="ccf2f-105">Nový časový rozvrh můžete založit na informacích z dřívějšího časového rozvrhu nebo na přiřazení projektů a aktivit na stránce Oblíbené položky.</span><span class="sxs-lookup"><span data-stu-id="ccf2f-105">The new timesheet can be based on information from a previous timesheet, or from project and activity assignments in the My favourites page.</span></span> <span data-ttu-id="ccf2f-106">Standardně stránka seznamu Všechny časové rozvrhy zobrazí všechny časové rozvrhy pro aktuální období.</span><span class="sxs-lookup"><span data-stu-id="ccf2f-106">By default, the All timesheets list page displays all your timesheets for the current period.</span></span> <span data-ttu-id="ccf2f-107">Můžete použít rozevírací seznam pole Zobrazit na stránce Moje časové rozvrhy pro filtrování seznamu časových rozvrhů podle období nebo projektu nebo k zobrazení časových rozvrhů, které byly vytvořeny jménem ostatních pracovníků.</span><span class="sxs-lookup"><span data-stu-id="ccf2f-107">You can use the drop-down list for the Show field in the My timesheets page to filter the timesheet list by time period or project, or to view timesheets that were created on behalf of other workers.</span></span> <span data-ttu-id="ccf2f-108">K vytvoření tohoto postupu jsou použita ukázková data společnosti USSI.</span><span class="sxs-lookup"><span data-stu-id="ccf2f-108">The demo data company used to create this procedure is USSI.</span></span> <span data-ttu-id="ccf2f-109">Tuto proceduru zahájíte pomocí nabídky Řízení projektu a účetnictví > Časové rozvrhy > Moje časové rozvrhy.</span><span class="sxs-lookup"><span data-stu-id="ccf2f-109">To begin this procedure, go to Project management and accounting > Timesheets >My timesheets</span></span>

1. <span data-ttu-id="ccf2f-110">Chcete-li zadat nový časový rozvrh, klikněte na tlačítko Nový.</span><span class="sxs-lookup"><span data-stu-id="ccf2f-110">To enter a new timesheet, click New.</span></span>
    * <span data-ttu-id="ccf2f-111">Rozevírací seznam Prostředek zobrazí ve výchozím nastavení pracovníka přiřazeného k aktuálnímu uživateli.</span><span class="sxs-lookup"><span data-stu-id="ccf2f-111">The Resource drop-down list shows the worker assigned to the current user, by default.</span></span>  
    * <span data-ttu-id="ccf2f-112">Pokud je uživatel navržený jako delegát, budou zde uvedeny jména tak, aby uživatel mohl zadat časový rozvrh jejich jménem.</span><span class="sxs-lookup"><span data-stu-id="ccf2f-112">If the user is designated as a delegate, this will list the names so that a user can enter a timesheet on their behalf.</span></span>  
2. <span data-ttu-id="ccf2f-113">Do pole Datum zadejte datum.</span><span class="sxs-lookup"><span data-stu-id="ccf2f-113">In the Date field, enter a date.</span></span>
    * <span data-ttu-id="ccf2f-114">Pokud je vybrána tato možnost, vytvoří se nové řádky časového rozvrhu pomocí nastavení časového rozvrhu, které byly konfigurovány jako oblíbené.</span><span class="sxs-lookup"><span data-stu-id="ccf2f-114">If this option is selected, new timesheet lines will be created by using the timesheet settings that were configured as favourites.</span></span>  
3. <span data-ttu-id="ccf2f-115">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="ccf2f-115">Click OK.</span></span>
4. <span data-ttu-id="ccf2f-116">Klikněte na možnost Nový řádek.</span><span class="sxs-lookup"><span data-stu-id="ccf2f-116">Click New line.</span></span>
5. <span data-ttu-id="ccf2f-117">Označte v seznamu vybraný řádek.</span><span class="sxs-lookup"><span data-stu-id="ccf2f-117">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="ccf2f-118">V poli Právnická osoba se ve výchozím nastavení zobrazí aktuální právnická osoba.</span><span class="sxs-lookup"><span data-stu-id="ccf2f-118">The Legal Entity field displays the current Legal entity by default.</span></span>   
6. <span data-ttu-id="ccf2f-119">V poli Projekt kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.</span><span class="sxs-lookup"><span data-stu-id="ccf2f-119">In the Project field, click the drop-down button to open the lookup.</span></span>
7. <span data-ttu-id="ccf2f-120">Vyhledejte na seznamu požadovaný záznam a vyberte ho.</span><span class="sxs-lookup"><span data-stu-id="ccf2f-120">In the list, find and select the desired record.</span></span>
8. <span data-ttu-id="ccf2f-121">Klikněte na odkaz na vybraném řádku v seznamu.</span><span class="sxs-lookup"><span data-stu-id="ccf2f-121">In the list, click the link in the selected row.</span></span>
9. <span data-ttu-id="ccf2f-122">V poli Aktivita klepnutím na tlačítko rozevíracího seznamu otevřete vyhledávání.</span><span class="sxs-lookup"><span data-stu-id="ccf2f-122">In the Activity field, click the drop-down button to open the lookup.</span></span>
10. <span data-ttu-id="ccf2f-123">Vyhledejte na seznamu požadovaný záznam a vyberte ho.</span><span class="sxs-lookup"><span data-stu-id="ccf2f-123">In the list, find and select the desired record.</span></span>
11. <span data-ttu-id="ccf2f-124">Klikněte na odkaz na vybraném řádku v seznamu.</span><span class="sxs-lookup"><span data-stu-id="ccf2f-124">In the list, click the link in the selected row.</span></span>
12. <span data-ttu-id="ccf2f-125">V poli Kategorie kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.</span><span class="sxs-lookup"><span data-stu-id="ccf2f-125">In the Category field, click the drop-down button to open the lookup.</span></span>
13. <span data-ttu-id="ccf2f-126">Vyhledejte na seznamu požadovaný záznam a vyberte ho.</span><span class="sxs-lookup"><span data-stu-id="ccf2f-126">In the list, find and select the desired record.</span></span>
14. <span data-ttu-id="ccf2f-127">Klikněte na odkaz na vybraném řádku v seznamu.</span><span class="sxs-lookup"><span data-stu-id="ccf2f-127">In the list, click the link in the selected row.</span></span>
15. <span data-ttu-id="ccf2f-128">Zadejte počtu hodin odpracovaných v jednotlivých dnech.</span><span class="sxs-lookup"><span data-stu-id="ccf2f-128">Enter the number of hours worked each day.</span></span>
    * <span data-ttu-id="ccf2f-129">Počet hodin musí být zadán v desetinném formátu.</span><span class="sxs-lookup"><span data-stu-id="ccf2f-129">Hours should be entered in a decimal format.</span></span>  <span data-ttu-id="ccf2f-130">Pokud jste například pracovali dvě hodiny a patnáct minut, zadejte hodnotu 2,25.</span><span class="sxs-lookup"><span data-stu-id="ccf2f-130">For example, if you worked for two hours and fifteen minutes, enter 2.25.</span></span>   
16. <span data-ttu-id="ccf2f-131">Zadejte počtu hodin odpracovaných v jednotlivých dnech.</span><span class="sxs-lookup"><span data-stu-id="ccf2f-131">Enter the number of hours worked each day.</span></span>
    * <span data-ttu-id="ccf2f-132">Počet hodin musí být zadán v desetinném formátu.</span><span class="sxs-lookup"><span data-stu-id="ccf2f-132">Hours should be entered in a decimal format.</span></span>  <span data-ttu-id="ccf2f-133">Pokud jste například pracovali dvě hodiny a patnáct minut, zadejte hodnotu 2,25.</span><span class="sxs-lookup"><span data-stu-id="ccf2f-133">For example, if you worked for two hours and fifteen minutes, enter 2.25.</span></span>   
17. <span data-ttu-id="ccf2f-134">Zadejte počtu hodin odpracovaných v jednotlivých dnech.</span><span class="sxs-lookup"><span data-stu-id="ccf2f-134">Enter the number of hours worked each day.</span></span>
    * <span data-ttu-id="ccf2f-135">Počet hodin musí být zadán v desetinném formátu.</span><span class="sxs-lookup"><span data-stu-id="ccf2f-135">Hours should be entered in a decimal format.</span></span>  <span data-ttu-id="ccf2f-136">Pokud jste například pracovali dvě hodiny a patnáct minut, zadejte hodnotu 2,25.</span><span class="sxs-lookup"><span data-stu-id="ccf2f-136">For example, if you worked for two hours and fifteen minutes, enter 2.25.</span></span>   
18. <span data-ttu-id="ccf2f-137">Zadejte počtu hodin odpracovaných v jednotlivých dnech.</span><span class="sxs-lookup"><span data-stu-id="ccf2f-137">Enter the number of hours worked each day.</span></span>
    * <span data-ttu-id="ccf2f-138">Počet hodin musí být zadán v desetinném formátu.</span><span class="sxs-lookup"><span data-stu-id="ccf2f-138">Hours should be entered in a decimal format.</span></span>  <span data-ttu-id="ccf2f-139">Pokud jste například pracovali dvě hodiny a patnáct minut, zadejte hodnotu 2,25.</span><span class="sxs-lookup"><span data-stu-id="ccf2f-139">For example, if you worked for two hours and fifteen minutes, enter 2.25.</span></span>   
19. <span data-ttu-id="ccf2f-140">Zadejte počtu hodin odpracovaných v jednotlivých dnech.</span><span class="sxs-lookup"><span data-stu-id="ccf2f-140">Enter the number of hours worked each day.</span></span>
    * <span data-ttu-id="ccf2f-141">Počet hodin musí být zadán v desetinném formátu.</span><span class="sxs-lookup"><span data-stu-id="ccf2f-141">Hours should be entered in a decimal format.</span></span>  <span data-ttu-id="ccf2f-142">Pokud jste například pracovali dvě hodiny a patnáct minut, zadejte hodnotu 2,25.</span><span class="sxs-lookup"><span data-stu-id="ccf2f-142">For example, if you worked for two hours and fifteen minutes, enter 2.25.</span></span>   
    * <span data-ttu-id="ccf2f-143">V poli Podrobnosti řádku jsou k dispozici následující možnosti:  o	Přidání informací o daních a finančních dimenzích. </span><span class="sxs-lookup"><span data-stu-id="ccf2f-143">In Line details, the following options are available:  o  Add information about taxes and financial dimensions.</span></span>  <span data-ttu-id="ccf2f-144">o    Přidání komentářů k řádku časového rozvrhu.</span><span class="sxs-lookup"><span data-stu-id="ccf2f-144">o    Add comments about the timesheet line.</span></span>  
20. <span data-ttu-id="ccf2f-145">Kliknutím na možnost Workflow otevřete dialogové okno.</span><span class="sxs-lookup"><span data-stu-id="ccf2f-145">Click Workflow to open the drop dialog.</span></span>
21. <span data-ttu-id="ccf2f-146">Klepněte na tlačítko Odeslat.</span><span class="sxs-lookup"><span data-stu-id="ccf2f-146">Click Submit.</span></span>
22. <span data-ttu-id="ccf2f-147">Klepněte na tlačítko Odeslat.</span><span class="sxs-lookup"><span data-stu-id="ccf2f-147">Click Submit.</span></span>


