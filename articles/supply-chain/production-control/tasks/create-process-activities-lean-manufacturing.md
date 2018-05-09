--- 
title: "Vytváření aktivit procesu pro lean manufacturing"
description: "Vytvořte aktivitu procesu pro lean manufacturing."
author: cvocph
manager: AnnBe
ms.date: 11/11/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: conradv
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: c1e7cb939c9b936a58486de13f73150aebccb548
ms.contentlocale: cs-cz
ms.lasthandoff: 05/08/2018

---
# <a name="create-process-activities-for-lean-manufacturing"></a><span data-ttu-id="c264f-103">Vytváření aktivit procesu pro lean manufacturing</span><span class="sxs-lookup"><span data-stu-id="c264f-103">Create process activities for lean manufacturing</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="c264f-104">Vytvořte aktivitu procesu pro lean manufacturing.</span><span class="sxs-lookup"><span data-stu-id="c264f-104">Create a process activity for lean manufacturing.</span></span> 

<span data-ttu-id="c264f-105">Požadavky:</span><span class="sxs-lookup"><span data-stu-id="c264f-105">Prerequisites:</span></span> 

1. <span data-ttu-id="c264f-106">Je nutné vytvořit výrobní tok a verzi, která není aktivní.</span><span class="sxs-lookup"><span data-stu-id="c264f-106">A production flow and version that is not active must be created.</span></span>

2. <span data-ttu-id="c264f-107">Musí být vytvořena pracovní buňka.</span><span class="sxs-lookup"><span data-stu-id="c264f-107">A work cell must be created.</span></span>


## <a name="find-the-production-flow-version"></a><span data-ttu-id="c264f-108">Najděte verzi výrobního toku</span><span class="sxs-lookup"><span data-stu-id="c264f-108">Find the production flow version</span></span>
1. <span data-ttu-id="c264f-109">Přejděte na Řízení výroby > Nastavení > Tok štíhlé výroby > Výrobního toky.</span><span class="sxs-lookup"><span data-stu-id="c264f-109">Go to Production control > Setup > Lean production flow > Production flows.</span></span>
2. <span data-ttu-id="c264f-110">Vyhledejte na seznamu požadovaný záznam a vyberte ho.</span><span class="sxs-lookup"><span data-stu-id="c264f-110">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="c264f-111">Klikněte na odkaz na vybraném řádku v seznamu.</span><span class="sxs-lookup"><span data-stu-id="c264f-111">In the list, click the link in the selected row.</span></span>

## <a name="create-a-new-activity"></a><span data-ttu-id="c264f-112">Vytvořte novou aktivitu</span><span class="sxs-lookup"><span data-stu-id="c264f-112">Create a new activity</span></span>
1. <span data-ttu-id="c264f-113">Klepněte na aktivity.</span><span class="sxs-lookup"><span data-stu-id="c264f-113">Click Activities.</span></span>
    * <span data-ttu-id="c264f-114">Ujistěte se, že vybraný výrobní tok má verzi v konceptu a tuto verzi vyberte.</span><span class="sxs-lookup"><span data-stu-id="c264f-114">Ensure that the selected production flow has a version in draft and select that version.</span></span>  
2. <span data-ttu-id="c264f-115">Klepněte na Vytvořit novou aktivitu plánu.</span><span class="sxs-lookup"><span data-stu-id="c264f-115">Click Create new plan activity.</span></span>
3. <span data-ttu-id="c264f-116">Klepněte na tlačítko Další.</span><span class="sxs-lookup"><span data-stu-id="c264f-116">Click Next.</span></span>
4. <span data-ttu-id="c264f-117">Zadejte hodnotu do pole Název.</span><span class="sxs-lookup"><span data-stu-id="c264f-117">In the Name field, type a value.</span></span>
5. <span data-ttu-id="c264f-118">Zadejte hodnotu do pole Název.</span><span class="sxs-lookup"><span data-stu-id="c264f-118">In the Name field, type a value.</span></span>
    * <span data-ttu-id="c264f-119">Nezapomeňte, že název musí být jedinečný pro všechny verze daného výrobního toku.</span><span class="sxs-lookup"><span data-stu-id="c264f-119">Note that the name must be unique for a given production flow for all versions.</span></span>  
6. <span data-ttu-id="c264f-120">V poli Množství procesu zadejte číslo.</span><span class="sxs-lookup"><span data-stu-id="c264f-120">In the Process quantity field, enter a number.</span></span>
    * <span data-ttu-id="c264f-121">Všimněte si, že bez ohledu na to, jaké množství úloh bude zpracováno, toto je minimální množství na úlohu pro výpočet nákladů na práci.</span><span class="sxs-lookup"><span data-stu-id="c264f-121">Note that no matter what job quantity will be processed, this is the minimum quantity per job to calculate the labor cost.</span></span> <span data-ttu-id="c264f-122">Pokud se množství úlohy liší od tohoto množství, bude vytvořena odchylka nákladů práce.</span><span class="sxs-lookup"><span data-stu-id="c264f-122">If job quantities deviate from this quantity, labor cost variance will be created.</span></span>  
7. <span data-ttu-id="c264f-123">Klepněte na tlačítko Další.</span><span class="sxs-lookup"><span data-stu-id="c264f-123">Click Next.</span></span>

## <a name="select-the-work-cell"></a><span data-ttu-id="c264f-124">Vyberte pracovní buňku</span><span class="sxs-lookup"><span data-stu-id="c264f-124">Select the work cell</span></span>
1. <span data-ttu-id="c264f-125">V poli Pracovní buňka kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.</span><span class="sxs-lookup"><span data-stu-id="c264f-125">In the Work cell field, click the drop-down button to open the lookup.</span></span>
2. <span data-ttu-id="c264f-126">Klikněte na odkaz na vybraném řádku v seznamu.</span><span class="sxs-lookup"><span data-stu-id="c264f-126">In the list, click the link in the selected row.</span></span>

## <a name="define-the-inventory-updates"></a><span data-ttu-id="c264f-127">Definujte aktualizace zásob</span><span class="sxs-lookup"><span data-stu-id="c264f-127">Define the inventory updates</span></span>
1. <span data-ttu-id="c264f-128">Zaškrtněte políčko Aktualizovat příjem na skladě nebo jeho zaškrtnutí zrušte.</span><span class="sxs-lookup"><span data-stu-id="c264f-128">Select or clear the Update on hand receipt check box.</span></span>
    * <span data-ttu-id="c264f-129">Pokud hodnota Aktualizovat zásoby na skladě = Ne, můžete definovat aktivity pro příjem polotovaru (aktivita nedosáhne další úrovně kusovníku).</span><span class="sxs-lookup"><span data-stu-id="c264f-129">If Update On hand = No, you can define the activity to receive a semi-finished product (the activity does not reach the next BOM level).</span></span>    <span data-ttu-id="c264f-130">Můžete vybrat také využívání polotovarů.</span><span class="sxs-lookup"><span data-stu-id="c264f-130">You can also select to consume semi-finished products.</span></span>  

## <a name="define-the-picking-activities"></a><span data-ttu-id="c264f-131">Definujte aktivity výdeje</span><span class="sxs-lookup"><span data-stu-id="c264f-131">Define the picking activities</span></span>
1. <span data-ttu-id="c264f-132">Klepněte na tlačítko Další.</span><span class="sxs-lookup"><span data-stu-id="c264f-132">Click Next.</span></span>
2. <span data-ttu-id="c264f-133">Označte v seznamu vybraný řádek.</span><span class="sxs-lookup"><span data-stu-id="c264f-133">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="c264f-134">Je vytvořena výchozí aktivita pro vstupní místo vybrané pracovní buňky.</span><span class="sxs-lookup"><span data-stu-id="c264f-134">A default picking activity is created for the input location of the selected work cell.</span></span>  
3. <span data-ttu-id="c264f-135">Klepněte na možnost Přidat.</span><span class="sxs-lookup"><span data-stu-id="c264f-135">Click Add.</span></span>
    * <span data-ttu-id="c264f-136">Můžete vytvořit další aktivity výdeje pro konkrétní produkty, které nejsou rozfázovány ve vstupní aktivitě pracovní buňky.</span><span class="sxs-lookup"><span data-stu-id="c264f-136">You can create additional picking activities for specific products, that are not staged at the work cell input activity.</span></span>  
4. <span data-ttu-id="c264f-137">Vyhledejte na seznamu požadovaný záznam a vyberte ho.</span><span class="sxs-lookup"><span data-stu-id="c264f-137">In the list, find and select the desired record.</span></span>
5. <span data-ttu-id="c264f-138">Zadejte hodnotu do pole Číslo zboží.</span><span class="sxs-lookup"><span data-stu-id="c264f-138">In the Item number field, type a value.</span></span>
6. <span data-ttu-id="c264f-139">V poli Sklad kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.</span><span class="sxs-lookup"><span data-stu-id="c264f-139">In the Warehouse field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="c264f-140">S touto definicí všechny materiály spotřebovávány při aktivitě jsou vydány z výchozího vstupního skladu a skladového místa s výjimkou položky, která je definována v druhé aktivitě výdeje.</span><span class="sxs-lookup"><span data-stu-id="c264f-140">With this definition, all materials consumed in the activity are picked from the default input warehouse and location except the item that is defined in the second picking activity.</span></span> <span data-ttu-id="c264f-141">Tato položka bude vydána z jiného skladu a umístění.</span><span class="sxs-lookup"><span data-stu-id="c264f-141">This item will be picked from a different warehouse and location.</span></span>  
7. <span data-ttu-id="c264f-142">Vyhledejte na seznamu požadovaný záznam a vyberte ho.</span><span class="sxs-lookup"><span data-stu-id="c264f-142">In the list, find and select the desired record.</span></span>
8. <span data-ttu-id="c264f-143">Klikněte na odkaz na vybraném řádku v seznamu.</span><span class="sxs-lookup"><span data-stu-id="c264f-143">In the list, click the link in the selected row.</span></span>
9. <span data-ttu-id="c264f-144">Zaškrtněte políčko Registrovat odpad nebo jeho zaškrtnutí zrušte.</span><span class="sxs-lookup"><span data-stu-id="c264f-144">Select or clear the Register scrap check box.</span></span>
10. <span data-ttu-id="c264f-145">Klepněte na tlačítko Další.</span><span class="sxs-lookup"><span data-stu-id="c264f-145">Click Next.</span></span>

## <a name="define-the-activity-times"></a><span data-ttu-id="c264f-146">Definujte čas aktivity</span><span class="sxs-lookup"><span data-stu-id="c264f-146">Define the activity times</span></span>
1. <span data-ttu-id="c264f-147">Vyhledejte na seznamu požadovaný záznam a vyberte ho.</span><span class="sxs-lookup"><span data-stu-id="c264f-147">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="c264f-148">Je požadována definice modulu Runtime.</span><span class="sxs-lookup"><span data-stu-id="c264f-148">The definition of a Runtime is required.</span></span> <span data-ttu-id="c264f-149">Modul Runtime se používá k výpočtu nákladů a doby propustnosti kanbanových úloh.</span><span class="sxs-lookup"><span data-stu-id="c264f-149">The Runtime is used to calculate costs and the throughput times of the kanban jobs.</span></span> <span data-ttu-id="c264f-150">Moduly Runtime nejsou používány k výpočtu vytížení kapacity a spotřeby, to je počítáno podle času cyklu, odvozeného z úlohy verze výrobního toku.</span><span class="sxs-lookup"><span data-stu-id="c264f-150">Runtimes are not used to calculate capacity load and consumption, this is calculated by cycle time, derived from the production flow version task.</span></span>  
2. <span data-ttu-id="c264f-151">Do pole Čas zadejte číslo.</span><span class="sxs-lookup"><span data-stu-id="c264f-151">In the Time field, enter a number.</span></span>
3. <span data-ttu-id="c264f-152">Zadejte hodnotu do pole Jednotka.</span><span class="sxs-lookup"><span data-stu-id="c264f-152">In the Unit field, type a value.</span></span>
4. <span data-ttu-id="c264f-153">Vyberte jednotku času.</span><span class="sxs-lookup"><span data-stu-id="c264f-153">Select the Time unit.</span></span>
5. <span data-ttu-id="c264f-154">V poli Podle množství zadejte číslo.</span><span class="sxs-lookup"><span data-stu-id="c264f-154">In the Per quantity field, enter a number.</span></span>
6. <span data-ttu-id="c264f-155">Vyhledejte na seznamu požadovaný záznam a vyberte ho.</span><span class="sxs-lookup"><span data-stu-id="c264f-155">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="c264f-156">Časy čekání jsou volitelné.</span><span class="sxs-lookup"><span data-stu-id="c264f-156">Queue times are optional.</span></span>  
7. <span data-ttu-id="c264f-157">Do pole Čas zadejte číslo.</span><span class="sxs-lookup"><span data-stu-id="c264f-157">In the Time field, enter a number.</span></span>
8. <span data-ttu-id="c264f-158">Zadejte hodnotu do pole Jednotka.</span><span class="sxs-lookup"><span data-stu-id="c264f-158">In the Unit field, type a value.</span></span>
9. <span data-ttu-id="c264f-159">Vyberte jednotku času.</span><span class="sxs-lookup"><span data-stu-id="c264f-159">Select the Time unit.</span></span>
10. <span data-ttu-id="c264f-160">V poli Podle množství zadejte číslo.</span><span class="sxs-lookup"><span data-stu-id="c264f-160">In the Per quantity field, enter a number.</span></span>
11. <span data-ttu-id="c264f-161">Klepněte na tlačítko Další.</span><span class="sxs-lookup"><span data-stu-id="c264f-161">Click Next.</span></span>
12. <span data-ttu-id="c264f-162">Klepněte na tlačítko Dokončit.</span><span class="sxs-lookup"><span data-stu-id="c264f-162">Click Finish.</span></span>
13. <span data-ttu-id="c264f-163">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="c264f-163">Close the page.</span></span>


