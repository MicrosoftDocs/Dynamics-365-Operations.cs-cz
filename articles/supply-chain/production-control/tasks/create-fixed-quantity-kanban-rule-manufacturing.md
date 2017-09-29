--- 
title: "Vytvoření kanbanového pravidla pro pevné množství pro výrobu"
description: "Tento postup se zaměřuje na nastavení potřebného k vytvoření pevné výroby kanbanového pravidla pro zaměření aktivit přeměny v pracovní buňce ve štíhlém prostředí."
author: ChristianRytt
manager: AnnBe
ms.date: 03/02/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 8020a37bf0c725fc260574cfe87861aeb017519e
ms.contentlocale: cs-cz
ms.lasthandoff: 08/29/2017

---
# <a name="create-a-fixed-quantity-kanban-rule-for-manufacturing"></a><span data-ttu-id="114fe-103">Vytvoření kanbanového pravidla pro pevné množství pro výrobu</span><span class="sxs-lookup"><span data-stu-id="114fe-103">Create a fixed quantity kanban rule for manufacturing</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="114fe-104">Tento postup se zaměřuje na nastavení potřebného k vytvoření pevné výroby kanbanového pravidla pro zaměření aktivit přeměny v pracovní buňce ve štíhlém prostředí.</span><span class="sxs-lookup"><span data-stu-id="114fe-104">This procedure focuses on the setup needed to create a fixed manufacturing kanban rule for triggering transforming activities, at a work cell, in a lean environment.</span></span> <span data-ttu-id="114fe-105">K vytvoření tohoto postupu jsou použita ukázková data společnosti USMF.</span><span class="sxs-lookup"><span data-stu-id="114fe-105">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="114fe-106">Tento postup je určen pro technologa výrobních procesů nebo správce hodnotového proudu, kteří připravují výrobu nového nebo změněného výrobku.</span><span class="sxs-lookup"><span data-stu-id="114fe-106">This procedure is intended for the Process Engineer or the Value Stream Manager, as they prepare production of a new or modified product.</span></span>


## <a name="create-new-kanban-rule"></a><span data-ttu-id="114fe-107">Vytvořit nové kanbanové pravidlo</span><span class="sxs-lookup"><span data-stu-id="114fe-107">Create new kanban rule</span></span>
1. <span data-ttu-id="114fe-108">Otevřete Kanbanová pravidla.</span><span class="sxs-lookup"><span data-stu-id="114fe-108">Go to Kanban rules.</span></span>
2. <span data-ttu-id="114fe-109">Klikněte na položku Nová.</span><span class="sxs-lookup"><span data-stu-id="114fe-109">Click New.</span></span>
    * <span data-ttu-id="114fe-110">Všimněte si, že výchozí typ je výroba a strategie doplnění je pevná.</span><span class="sxs-lookup"><span data-stu-id="114fe-110">Notice that the default Type is Manufacturing and Replenishment strategy is Fixed.</span></span> <span data-ttu-id="114fe-111">Není nutné tyto parametry měnit.</span><span class="sxs-lookup"><span data-stu-id="114fe-111">You do not have to change these parameters.</span></span>  
3. <span data-ttu-id="114fe-112">V poli První aktivita plánu zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="114fe-112">In the First plan activity field, enter or select a value.</span></span>
    * <span data-ttu-id="114fe-113">Toto je aktivita, která bude provedena pro kanbany založené na tomto kanbanovém pravidlu.</span><span class="sxs-lookup"><span data-stu-id="114fe-113">This is the activity that will be performed for kanbans created based on this kanban rule.</span></span>  <span data-ttu-id="114fe-114">Vyberte hodnotu „SpeakerTestAndPackaging“.</span><span class="sxs-lookup"><span data-stu-id="114fe-114">Select 'SpeakerTestAndPackaging'.</span></span>  
4. <span data-ttu-id="114fe-115">Rozbalte sekci Podrobnosti.</span><span class="sxs-lookup"><span data-stu-id="114fe-115">Expand the Details section.</span></span>
5. <span data-ttu-id="114fe-116">V poli Produkt zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="114fe-116">In the Product field, enter or select a value.</span></span>
    * <span data-ttu-id="114fe-117">Vyberte volbu „L0050“.</span><span class="sxs-lookup"><span data-stu-id="114fe-117">Select L0050.</span></span>  
6. <span data-ttu-id="114fe-118">V poli Měrná jednotka zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="114fe-118">In the Unit of measure field, enter or select a value.</span></span>
    * <span data-ttu-id="114fe-119">Vyberte minuty.</span><span class="sxs-lookup"><span data-stu-id="114fe-119">Select minutes.</span></span>  
7. <span data-ttu-id="114fe-120">Do pole Doba realizace zadejte číslo.</span><span class="sxs-lookup"><span data-stu-id="114fe-120">In the Lead time field, enter a number.</span></span>
    * <span data-ttu-id="114fe-121">Zadejte 5.</span><span class="sxs-lookup"><span data-stu-id="114fe-121">Enter 5.</span></span>  

## <a name="set-quantities"></a><span data-ttu-id="114fe-122">Nastavit množství</span><span class="sxs-lookup"><span data-stu-id="114fe-122">Set quantities</span></span>
1. <span data-ttu-id="114fe-123">Rozbalte sekci Množství.</span><span class="sxs-lookup"><span data-stu-id="114fe-123">Expand the Quantities section.</span></span>
2. <span data-ttu-id="114fe-124">Nastavte výchozí množství na „10“.</span><span class="sxs-lookup"><span data-stu-id="114fe-124">Set Default quantity to '10'.</span></span>
    * <span data-ttu-id="114fe-125">Jedná se o množství, které bude přeneseno pro každý kanban.</span><span class="sxs-lookup"><span data-stu-id="114fe-125">This is the quantity that will be transferred for each kanban.</span></span>  
3. <span data-ttu-id="114fe-126">Zaškrtněte políčko odchylky množství produktu.</span><span class="sxs-lookup"><span data-stu-id="114fe-126">Select the Product quantity variance check box.</span></span>
    * <span data-ttu-id="114fe-127">Díky tomu lze dokončit vybrané kanbany s odchylkou od výchozího množství.</span><span class="sxs-lookup"><span data-stu-id="114fe-127">With this, selected kanbans can be completed with a variance from the default quantity.</span></span>  <span data-ttu-id="114fe-128">Umožňuje kanbany dokončit s množstvím od 8 do 12, obě odchylky nastaveny na 2.</span><span class="sxs-lookup"><span data-stu-id="114fe-128">To allow kanbans to be completed with a quantity from 8 to 12, set both variances to 2.</span></span>  
4. <span data-ttu-id="114fe-129">Nastavte odchylku menší než „2“.</span><span class="sxs-lookup"><span data-stu-id="114fe-129">Set Variance below to '2'.</span></span>
    * <span data-ttu-id="114fe-130">To vám poskytne dokončení do 10 - 2 = 8</span><span class="sxs-lookup"><span data-stu-id="114fe-130">This will allow completing down to 10 - 2 = 8</span></span>  
5. <span data-ttu-id="114fe-131">Nastavte odchylku vyšší než „2“.</span><span class="sxs-lookup"><span data-stu-id="114fe-131">Set Variance above to '2'.</span></span>
    * <span data-ttu-id="114fe-132">To vám poskytne dokončení až do 10 + 2 = 12</span><span class="sxs-lookup"><span data-stu-id="114fe-132">This will allow completing up to 10 + 2 = 12</span></span>  
6. <span data-ttu-id="114fe-133">V poli Pevné kanbanové množství zadejte číslo.</span><span class="sxs-lookup"><span data-stu-id="114fe-133">In the Fixed kanban quantity field, enter a number.</span></span>
    * <span data-ttu-id="114fe-134">To je počet kanbanů, které mají být aktivní.</span><span class="sxs-lookup"><span data-stu-id="114fe-134">This is the amount of kanbans that should be active.</span></span> <span data-ttu-id="114fe-135">V tomto případě 5 kanbanů zpracovává každých 10.</span><span class="sxs-lookup"><span data-stu-id="114fe-135">In this case, 5 kanbans processing 10 each.</span></span>  
7. <span data-ttu-id="114fe-136">V poli Minimální hranice výstrahy zadejte hodnotu „2“.</span><span class="sxs-lookup"><span data-stu-id="114fe-136">In the Alert boundary minimum field, enter '2'.</span></span>
    * <span data-ttu-id="114fe-137">Slouží ke sledování minimálního množství plných kanbanů, které mají být na místě určení.</span><span class="sxs-lookup"><span data-stu-id="114fe-137">Used to keep track of the minimum amount of full kanbans that should be at the destination.</span></span> <span data-ttu-id="114fe-138">Toto se například používá na přehled kanbanového množství.</span><span class="sxs-lookup"><span data-stu-id="114fe-138">For example, this is used on the kanban quantity overview.</span></span>  
8. <span data-ttu-id="114fe-139">V poli Maximální hranice výstrahy zadejte hodnotu „4“.</span><span class="sxs-lookup"><span data-stu-id="114fe-139">In the Alert boundary maximum field, enter '4'.</span></span>
    * <span data-ttu-id="114fe-140">Slouží ke sledování maximálního množství plných kanbanů, které mají být na místě určení.</span><span class="sxs-lookup"><span data-stu-id="114fe-140">Used to keep track of the maximum amount of full kanbans that should be at the destination.</span></span> <span data-ttu-id="114fe-141">Toto se například používá na přehled kanbanového množství.</span><span class="sxs-lookup"><span data-stu-id="114fe-141">For example, this is used on the kanban quantity overview.</span></span>  
9. <span data-ttu-id="114fe-142">Do pole Automaticky plánované množství zadejte hodnotu „1“.</span><span class="sxs-lookup"><span data-stu-id="114fe-142">In the Automatic planning quantity field, enter '1'.</span></span>
    * <span data-ttu-id="114fe-143">Toto nastavení na 1 znamená, že každý kanban bude automaticky naplánován.</span><span class="sxs-lookup"><span data-stu-id="114fe-143">Setting this to 1 means that every kanban will be automatically planned.</span></span>   <span data-ttu-id="114fe-144">Pokud zadáme 3, kanbany nebudou plánovány, dokud nebudou prázdné 3 kanbany, které jsou připraveny pro plánování.</span><span class="sxs-lookup"><span data-stu-id="114fe-144">If we entered 3, the kanbans would not be planned until 3 empty kanbans are ready for planning.</span></span> <span data-ttu-id="114fe-145">To je užitečné pro seskupení práce a jako prevence velkého nastavování.</span><span class="sxs-lookup"><span data-stu-id="114fe-145">This is useful for grouping work and avoiding too much setup.</span></span>  

## <a name="create-kanbans"></a><span data-ttu-id="114fe-146">Vytvořit kanbany</span><span class="sxs-lookup"><span data-stu-id="114fe-146">Create Kanbans</span></span>
1. <span data-ttu-id="114fe-147">Rozbalte sekci Kanbany.</span><span class="sxs-lookup"><span data-stu-id="114fe-147">Expand the Kanbans section.</span></span>
2. <span data-ttu-id="114fe-148">Klikněte na položku Uložit.</span><span class="sxs-lookup"><span data-stu-id="114fe-148">Click Save.</span></span>
    * <span data-ttu-id="114fe-149">Kanbanové pravidlo je třeba uložit, aby bylo možné vytvořit kanbany.</span><span class="sxs-lookup"><span data-stu-id="114fe-149">The kanban rule needs to be saved before kanbans can be created.</span></span>  
3. <span data-ttu-id="114fe-150">Klepněte na možnost Přidat.</span><span class="sxs-lookup"><span data-stu-id="114fe-150">Click Add.</span></span>
    * <span data-ttu-id="114fe-151">Všimněte si, že neexistují žádné aktivní kanbany, protože navržený Počet nových kanbanů je 5.</span><span class="sxs-lookup"><span data-stu-id="114fe-151">Note that there are no active kanbans, due to this the suggested 'Number of new kanbans' are 5.</span></span> <span data-ttu-id="114fe-152">To je stejné jako Pevné kanbanové množství.</span><span class="sxs-lookup"><span data-stu-id="114fe-152">This is equal to the 'Fixed kanban quantity'.</span></span>  
4. <span data-ttu-id="114fe-153">Klikněte na položku Vytvořit.</span><span class="sxs-lookup"><span data-stu-id="114fe-153">Click Create.</span></span>
    * <span data-ttu-id="114fe-154">Dojde k vytvoření 5 kanbanů.</span><span class="sxs-lookup"><span data-stu-id="114fe-154">This will create 5 kanbans.</span></span>  
    * <span data-ttu-id="114fe-155">Všimněte si, že 5 kanbanů po 10, bylo vytvořeno pro toto výrobní kanbanové pravidlo.</span><span class="sxs-lookup"><span data-stu-id="114fe-155">Note that 5 kanbans, for 10 each, was created for this manufacturing kanban rule.</span></span> <span data-ttu-id="114fe-156">Tento krok je posledním krokem v tomto postupu.</span><span class="sxs-lookup"><span data-stu-id="114fe-156">This is the last step in this procedure.</span></span>  


