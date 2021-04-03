---
title: Zadávání časových rozvrhů projektů
description: Tato procedura vám umožní vytvořit časový rozvrh pomocí prázdného formuláře časového rozvrhu.
author: andreabichsel
manager: tfehr
ms.date: 08/08/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.region: Global
ms.search.industry: Service industries
ms.author: anbichse
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: cd0389584cb723b403dcd5f6bec67d2eb969048f
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/09/2021
ms.locfileid: "5564997"
---
# <a name="enter-project-timesheets"></a><span data-ttu-id="6d33c-103">Zadávání časových rozvrhů projektů</span><span class="sxs-lookup"><span data-stu-id="6d33c-103">Enter project timesheets</span></span>

<span data-ttu-id="6d33c-104">Tato procedura vám umožní vytvořit časový rozvrh pomocí prázdného formuláře časového rozvrhu.</span><span class="sxs-lookup"><span data-stu-id="6d33c-104">This procedure lets you create a timesheet by using an empty timesheet form.</span></span> <span data-ttu-id="6d33c-105">Nový časový rozvrh můžete založit na informacích z dřívějšího časového rozvrhu nebo na přiřazení projektů a aktivit na stránce **Oblíbené položky**.</span><span class="sxs-lookup"><span data-stu-id="6d33c-105">The new timesheet can be based on information from a previous timesheet, or from project and activity assignments in the **My favorites** page.</span></span> <span data-ttu-id="6d33c-106">Standardně stránka seznamu **Všechny časové rozvrhy** zobrazí všechny časové rozvrhy pro aktuální období.</span><span class="sxs-lookup"><span data-stu-id="6d33c-106">By default, the **All timesheets** list page displays all your timesheets for the current period.</span></span> <span data-ttu-id="6d33c-107">Můžete použít rozevírací seznam pole **Zobrazit** na stránce **Moje časové rozvrhy** pro filtrování seznamu časových rozvrhů podle období nebo projektu nebo k zobrazení časových rozvrhů, které byly vytvořeny jménem ostatních pracovníků.</span><span class="sxs-lookup"><span data-stu-id="6d33c-107">You can use the drop-down list for the **Show** field in the **My timesheets** page to filter the timesheet list by time period or project, or to view timesheets that were created on behalf of other workers.</span></span> <span data-ttu-id="6d33c-108">K vytvoření tohoto postupu jsou použita ukázková data společnosti USSI.</span><span class="sxs-lookup"><span data-stu-id="6d33c-108">The demo data company used to create this procedure is USSI.</span></span>  

1. <span data-ttu-id="6d33c-109">V **navigačním podokně** přejděte na **Moduly > Řízení projektů a účetnictví > Časové rozvrhy > Moje časové rozvrhy**.</span><span class="sxs-lookup"><span data-stu-id="6d33c-109">In the **Navigation pane**, go to **Modules > Project management and accounting > Timesheets > My timesheets**.</span></span>
2. <span data-ttu-id="6d33c-110">Chcete-li zadat nový časový rozvrh, klikněte na tlačítko **Nový**.</span><span class="sxs-lookup"><span data-stu-id="6d33c-110">To enter a new timesheet, click **New**.</span></span>
    - <span data-ttu-id="6d33c-111">Rozevírací seznam Prostředek zobrazí ve výchozím nastavení pracovníka přiřazeného k aktuálnímu uživateli.</span><span class="sxs-lookup"><span data-stu-id="6d33c-111">The Resource drop-down list shows the worker assigned to the current user, by default.</span></span>  
    - <span data-ttu-id="6d33c-112">Pokud je uživatel navržený jako delegát, budou zde uvedeny jména tak, aby uživatel mohl zadat časový rozvrh jejich jménem.</span><span class="sxs-lookup"><span data-stu-id="6d33c-112">If the user is designated as a delegate, this will list the names so that a user can enter a timesheet on their behalf.</span></span>  
3. <span data-ttu-id="6d33c-113">Do pole **Datum** zadejte datum.</span><span class="sxs-lookup"><span data-stu-id="6d33c-113">In the **Date** field, enter a date.</span></span> <span data-ttu-id="6d33c-114">Pokud je vybrána tato možnost, vytvoří se nové řádky časového rozvrhu pomocí nastavení časového rozvrhu, které byly konfigurovány jako oblíbené.</span><span class="sxs-lookup"><span data-stu-id="6d33c-114">If this option is selected, new timesheet lines will be created by using the timesheet settings that were configured as favorites.</span></span>  
4. <span data-ttu-id="6d33c-115">Klikněte na tlačítko **OK**.</span><span class="sxs-lookup"><span data-stu-id="6d33c-115">Click **OK**.</span></span>
5. <span data-ttu-id="6d33c-116">Klikněte na **Nový řádek**.</span><span class="sxs-lookup"><span data-stu-id="6d33c-116">Click **New line**.</span></span>
6. <span data-ttu-id="6d33c-117">Označte v seznamu vybraný řádek.</span><span class="sxs-lookup"><span data-stu-id="6d33c-117">In the list, mark the selected row.</span></span> <span data-ttu-id="6d33c-118">V poli **Právnická osoba** se ve výchozím nastavení zobrazí aktuální právnická osoba.</span><span class="sxs-lookup"><span data-stu-id="6d33c-118">The **Legal Entity** field displays the current Legal entity by default.</span></span>   
7. <span data-ttu-id="6d33c-119">V poli **Projekt** kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.</span><span class="sxs-lookup"><span data-stu-id="6d33c-119">In the **Project** field, click the drop-down button to open the lookup.</span></span>
8. <span data-ttu-id="6d33c-120">Vyhledejte na seznamu požadovaný záznam a vyberte ho.</span><span class="sxs-lookup"><span data-stu-id="6d33c-120">In the list, find and select the desired record.</span></span>
9. <span data-ttu-id="6d33c-121">Klikněte na odkaz na vybraném řádku v seznamu.</span><span class="sxs-lookup"><span data-stu-id="6d33c-121">In the list, click the link in the selected row.</span></span>
10. <span data-ttu-id="6d33c-122">V poli **Číslo aktivity** kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.</span><span class="sxs-lookup"><span data-stu-id="6d33c-122">In the **Activity number** field, click the drop-down button to open the lookup.</span></span>
11. <span data-ttu-id="6d33c-123">Vyhledejte na seznamu požadovaný záznam a vyberte ho.</span><span class="sxs-lookup"><span data-stu-id="6d33c-123">In the list, find and select the desired record.</span></span>
12. <span data-ttu-id="6d33c-124">Klikněte na odkaz na vybraném řádku v seznamu.</span><span class="sxs-lookup"><span data-stu-id="6d33c-124">In the list, click the link in the selected row.</span></span>
13. <span data-ttu-id="6d33c-125">V poli **Kategorie** kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.</span><span class="sxs-lookup"><span data-stu-id="6d33c-125">In the **Category** field, click the drop-down button to open the lookup.</span></span>
14. <span data-ttu-id="6d33c-126">Vyhledejte na seznamu požadovaný záznam a vyberte ho.</span><span class="sxs-lookup"><span data-stu-id="6d33c-126">In the list, find and select the desired record.</span></span>
15. <span data-ttu-id="6d33c-127">Klikněte na odkaz na vybraném řádku v seznamu.</span><span class="sxs-lookup"><span data-stu-id="6d33c-127">In the list, click the link in the selected row.</span></span>
16. <span data-ttu-id="6d33c-128">Zadejte počtu hodin odpracovaných v jednotlivých dnech.</span><span class="sxs-lookup"><span data-stu-id="6d33c-128">Enter the number of hours worked each day.</span></span> <span data-ttu-id="6d33c-129">Hodiny zadávejte v desetinném formátu.</span><span class="sxs-lookup"><span data-stu-id="6d33c-129">Enter the hours in decimal format.</span></span> <span data-ttu-id="6d33c-130">Pokud jste například pracovali dvě hodiny a patnáct minut, zadejte hodnotu 2,25.</span><span class="sxs-lookup"><span data-stu-id="6d33c-130">For example, if you worked for two hours and fifteen minutes, enter 2.25.</span></span>   
17. <span data-ttu-id="6d33c-131">V poli **Podrobnosti řádku** jsou k dispozici následující možnosti:</span><span class="sxs-lookup"><span data-stu-id="6d33c-131">In **Line details**, the following options are available:</span></span>
    - <span data-ttu-id="6d33c-132">Přidejte informace o daních a finančních dimenzích na kartě **Obecné** a **Finanční dimenze**.</span><span class="sxs-lookup"><span data-stu-id="6d33c-132">Add information about taxes and financial dimensions in the **General** and the **Financial Dimensions** tab.</span></span>
    - <span data-ttu-id="6d33c-133">Přidejte komentáře k řádku časového rozvrhu na kartě **Komentář**.</span><span class="sxs-lookup"><span data-stu-id="6d33c-133">Add comments about the timesheet line in the **Comment** tab.</span></span>
20. <span data-ttu-id="6d33c-134">V **podokně akcí** klikněte na **Workflow** a otevřete rozbalovací dialogové okno.</span><span class="sxs-lookup"><span data-stu-id="6d33c-134">In the **Action pane**, click **Workflow** to open the drop dialog.</span></span>
21. <span data-ttu-id="6d33c-135">Klepněte na tlačítko **Odeslat**.</span><span class="sxs-lookup"><span data-stu-id="6d33c-135">Click **Submit**.</span></span>
22. <span data-ttu-id="6d33c-136">Klepněte na tlačítko **Odeslat**.</span><span class="sxs-lookup"><span data-stu-id="6d33c-136">Click **Submit**.</span></span>



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]