---
title: Zadávání časových rozvrhů projektů
description: Tato procedura vám umožní vytvořit časový rozvrh pomocí prázdného formuláře časového rozvrhu.
author: andreabichsel
manager: AnnBe
ms.date: 08/08/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Operations, Human Resources
ms.search.region: Global
ms.search.industry: Service industries
ms.author: anbichse
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 10dbb43cec47a758d11362947f27932a4911911a
ms.sourcegitcommit: ba340f836e472f13f263dec46a49847c788fca44
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/04/2020
ms.locfileid: "3430272"
---
# <a name="enter-project-timesheets"></a><span data-ttu-id="6cb8d-103">Zadávání časových rozvrhů projektů</span><span class="sxs-lookup"><span data-stu-id="6cb8d-103">Enter project timesheets</span></span>



<span data-ttu-id="6cb8d-104">Tato procedura vám umožní vytvořit časový rozvrh pomocí prázdného formuláře časového rozvrhu.</span><span class="sxs-lookup"><span data-stu-id="6cb8d-104">This procedure lets you create a timesheet by using an empty timesheet form.</span></span> <span data-ttu-id="6cb8d-105">Nový časový rozvrh můžete založit na informacích z dřívějšího časového rozvrhu nebo na přiřazení projektů a aktivit na stránce **Oblíbené položky**.</span><span class="sxs-lookup"><span data-stu-id="6cb8d-105">The new timesheet can be based on information from a previous timesheet, or from project and activity assignments in the **My favorites** page.</span></span> <span data-ttu-id="6cb8d-106">Standardně stránka seznamu **Všechny časové rozvrhy** zobrazí všechny časové rozvrhy pro aktuální období.</span><span class="sxs-lookup"><span data-stu-id="6cb8d-106">By default, the **All timesheets** list page displays all your timesheets for the current period.</span></span> <span data-ttu-id="6cb8d-107">Můžete použít rozevírací seznam pole **Zobrazit** na stránce **Moje časové rozvrhy** pro filtrování seznamu časových rozvrhů podle období nebo projektu nebo k zobrazení časových rozvrhů, které byly vytvořeny jménem ostatních pracovníků.</span><span class="sxs-lookup"><span data-stu-id="6cb8d-107">You can use the drop-down list for the **Show** field in the **My timesheets** page to filter the timesheet list by time period or project, or to view timesheets that were created on behalf of other workers.</span></span> <span data-ttu-id="6cb8d-108">K vytvoření tohoto postupu jsou použita ukázková data společnosti USSI.</span><span class="sxs-lookup"><span data-stu-id="6cb8d-108">The demo data company used to create this procedure is USSI.</span></span> 

1. <span data-ttu-id="6cb8d-109">V **navigačním podokně** přejděte na **Moduly > Řízení projektů a účetnictví > Časové rozvrhy > Moje časové rozvrhy**.</span><span class="sxs-lookup"><span data-stu-id="6cb8d-109">In the **Navigation pane**, go to **Modules > Project management and accounting > Timesheets > My timesheets**.</span></span>
2. <span data-ttu-id="6cb8d-110">Chcete-li zadat nový časový rozvrh, klikněte na tlačítko **Nový**.</span><span class="sxs-lookup"><span data-stu-id="6cb8d-110">To enter a new timesheet, click **New**.</span></span>
    - <span data-ttu-id="6cb8d-111">Rozevírací seznam Prostředek zobrazí ve výchozím nastavení pracovníka přiřazeného k aktuálnímu uživateli.</span><span class="sxs-lookup"><span data-stu-id="6cb8d-111">The Resource drop-down list shows the worker assigned to the current user, by default.</span></span>  
    - <span data-ttu-id="6cb8d-112">Pokud je uživatel navržený jako delegát, budou zde uvedeny jména tak, aby uživatel mohl zadat časový rozvrh jejich jménem.</span><span class="sxs-lookup"><span data-stu-id="6cb8d-112">If the user is designated as a delegate, this will list the names so that a user can enter a timesheet on their behalf.</span></span>  
3. <span data-ttu-id="6cb8d-113">Do pole **Datum** zadejte datum.</span><span class="sxs-lookup"><span data-stu-id="6cb8d-113">In the **Date** field, enter a date.</span></span> <span data-ttu-id="6cb8d-114">Pokud je vybrána tato možnost, vytvoří se nové řádky časového rozvrhu pomocí nastavení časového rozvrhu, které byly konfigurovány jako oblíbené.</span><span class="sxs-lookup"><span data-stu-id="6cb8d-114">If this option is selected, new timesheet lines will be created by using the timesheet settings that were configured as favorites.</span></span>  
4. <span data-ttu-id="6cb8d-115">Klikněte na tlačítko **OK**.</span><span class="sxs-lookup"><span data-stu-id="6cb8d-115">Click **OK**.</span></span>
5. <span data-ttu-id="6cb8d-116">Klikněte na **Nový řádek**.</span><span class="sxs-lookup"><span data-stu-id="6cb8d-116">Click **New line**.</span></span>
6. <span data-ttu-id="6cb8d-117">Označte v seznamu vybraný řádek.</span><span class="sxs-lookup"><span data-stu-id="6cb8d-117">In the list, mark the selected row.</span></span> <span data-ttu-id="6cb8d-118">V poli **Právnická osoba** se ve výchozím nastavení zobrazí aktuální právnická osoba.</span><span class="sxs-lookup"><span data-stu-id="6cb8d-118">The **Legal Entity** field displays the current Legal entity by default.</span></span>   
7. <span data-ttu-id="6cb8d-119">V poli **Projekt** kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.</span><span class="sxs-lookup"><span data-stu-id="6cb8d-119">In the **Project** field, click the drop-down button to open the lookup.</span></span>
8. <span data-ttu-id="6cb8d-120">Vyhledejte na seznamu požadovaný záznam a vyberte ho.</span><span class="sxs-lookup"><span data-stu-id="6cb8d-120">In the list, find and select the desired record.</span></span>
9. <span data-ttu-id="6cb8d-121">Klikněte na odkaz na vybraném řádku v seznamu.</span><span class="sxs-lookup"><span data-stu-id="6cb8d-121">In the list, click the link in the selected row.</span></span>
10. <span data-ttu-id="6cb8d-122">V poli **Číslo aktivity** kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.</span><span class="sxs-lookup"><span data-stu-id="6cb8d-122">In the **Activity number** field, click the drop-down button to open the lookup.</span></span>
11. <span data-ttu-id="6cb8d-123">Vyhledejte na seznamu požadovaný záznam a vyberte ho.</span><span class="sxs-lookup"><span data-stu-id="6cb8d-123">In the list, find and select the desired record.</span></span>
12. <span data-ttu-id="6cb8d-124">Klikněte na odkaz na vybraném řádku v seznamu.</span><span class="sxs-lookup"><span data-stu-id="6cb8d-124">In the list, click the link in the selected row.</span></span>
13. <span data-ttu-id="6cb8d-125">V poli **Kategorie** kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.</span><span class="sxs-lookup"><span data-stu-id="6cb8d-125">In the **Category** field, click the drop-down button to open the lookup.</span></span>
14. <span data-ttu-id="6cb8d-126">Vyhledejte na seznamu požadovaný záznam a vyberte ho.</span><span class="sxs-lookup"><span data-stu-id="6cb8d-126">In the list, find and select the desired record.</span></span>
15. <span data-ttu-id="6cb8d-127">Klikněte na odkaz na vybraném řádku v seznamu.</span><span class="sxs-lookup"><span data-stu-id="6cb8d-127">In the list, click the link in the selected row.</span></span>
16. <span data-ttu-id="6cb8d-128">Zadejte počtu hodin odpracovaných v jednotlivých dnech.</span><span class="sxs-lookup"><span data-stu-id="6cb8d-128">Enter the number of hours worked each day.</span></span> <span data-ttu-id="6cb8d-129">Hodiny zadávejte v desetinném formátu.</span><span class="sxs-lookup"><span data-stu-id="6cb8d-129">Enter the hours in decimal format.</span></span> <span data-ttu-id="6cb8d-130">Pokud jste například pracovali dvě hodiny a patnáct minut, zadejte hodnotu 2,25.</span><span class="sxs-lookup"><span data-stu-id="6cb8d-130">For example, if you worked for two hours and fifteen minutes, enter 2.25.</span></span>   
17. <span data-ttu-id="6cb8d-131">V poli **Podrobnosti řádku** jsou k dispozici následující možnosti:</span><span class="sxs-lookup"><span data-stu-id="6cb8d-131">In **Line details**, the following options are available:</span></span>
    - <span data-ttu-id="6cb8d-132">Přidejte informace o daních a finančních dimenzích na kartě **Obecné** a **Finanční dimenze**.</span><span class="sxs-lookup"><span data-stu-id="6cb8d-132">Add information about taxes and financial dimensions in the **General** and the **Financial Dimensions** tab.</span></span>
    - <span data-ttu-id="6cb8d-133">Přidejte komentáře k řádku časového rozvrhu na kartě **Komentář**.</span><span class="sxs-lookup"><span data-stu-id="6cb8d-133">Add comments about the timesheet line in the **Comment** tab.</span></span>
20. <span data-ttu-id="6cb8d-134">V **podokně akcí** klikněte na **Workflow** a otevřete rozbalovací dialogové okno.</span><span class="sxs-lookup"><span data-stu-id="6cb8d-134">In the **Action pane**, click **Workflow** to open the drop dialog.</span></span>
21. <span data-ttu-id="6cb8d-135">Klepněte na tlačítko **Odeslat**.</span><span class="sxs-lookup"><span data-stu-id="6cb8d-135">Click **Submit**.</span></span>
22. <span data-ttu-id="6cb8d-136">Klepněte na tlačítko **Odeslat**.</span><span class="sxs-lookup"><span data-stu-id="6cb8d-136">Click **Submit**.</span></span>

