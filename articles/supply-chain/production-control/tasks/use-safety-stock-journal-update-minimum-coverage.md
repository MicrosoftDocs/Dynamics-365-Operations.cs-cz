--- 
title: "Použití deníku pojistných zásob pro aktualizaci minimální disponibility"
description: "Tento postup popisuje způsob výpočtu návrhů minimální disponibility na základě historických transakcí, a pokrytí následně aktualizaci disponibility položky podle návrhů."
author: ChristianRytt
manager: AnnBe
ms.date: 10/27/2016
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
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: b9e3245af746b120117a23b3859e03bd4216e1cd
ms.contentlocale: cs-cz
ms.lasthandoff: 04/13/2018

---
# <a name="use-the-safety-stock-journal-to-update-minimum-coverage"></a><span data-ttu-id="bb116-103">Použití deníku pojistných zásob pro aktualizaci minimální disponibility</span><span class="sxs-lookup"><span data-stu-id="bb116-103">Use the safety stock journal to update minimum coverage</span></span>

[!INCLUDE [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="bb116-104">Tento postup popisuje způsob výpočtu návrhů minimální disponibility na základě historických transakcí, a pokrytí následně aktualizaci disponibility položky podle návrhů.</span><span class="sxs-lookup"><span data-stu-id="bb116-104">This procedure shows how to calculate minimum coverage proposals based on historical transactions and then update the item coverage with the proposals.</span></span> <span data-ttu-id="bb116-105">To se provádí pomocí deníku pojistných zásob.</span><span class="sxs-lookup"><span data-stu-id="bb116-105">This is done using the safety stock journal.</span></span> <span data-ttu-id="bb116-106">Tento úkol byl vytvořen pomocí ukázkových dat společnosti USMF.</span><span class="sxs-lookup"><span data-stu-id="bb116-106">The demo data company used to create this task is USMF.</span></span> <span data-ttu-id="bb116-107">Tato úloha je určena pro plánovače výroby k zachování minimální disponibility.</span><span class="sxs-lookup"><span data-stu-id="bb116-107">This task is intended for the production planner, to help maintain minimum coverage.</span></span>


## <a name="create-a-new-safety-stock-journal-name"></a><span data-ttu-id="bb116-108">Vytvoření názvu nového deníku pojistných zásob</span><span class="sxs-lookup"><span data-stu-id="bb116-108">Create a new safety stock journal name</span></span>
1. <span data-ttu-id="bb116-109">Přejděte na Názvy deníku pojistných zásob.</span><span class="sxs-lookup"><span data-stu-id="bb116-109">Go to Safety stock journal names.</span></span>
2. <span data-ttu-id="bb116-110">Klikněte na položku Nová.</span><span class="sxs-lookup"><span data-stu-id="bb116-110">Click New.</span></span>
3. <span data-ttu-id="bb116-111">Do pole Název zadejte „Materiál“.</span><span class="sxs-lookup"><span data-stu-id="bb116-111">In the Name field, type 'Material'.</span></span>
4. <span data-ttu-id="bb116-112">V poli Popis uveďte text „Materiál“.</span><span class="sxs-lookup"><span data-stu-id="bb116-112">In the Description field, type 'Material'.</span></span>
5. <span data-ttu-id="bb116-113">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="bb116-113">Close the page.</span></span>

## <a name="create-a-safety-stock-journal"></a><span data-ttu-id="bb116-114">Vytvoření deníku pojistných zásob</span><span class="sxs-lookup"><span data-stu-id="bb116-114">Create a safety stock journal</span></span>
1. <span data-ttu-id="bb116-115">Přejděte na Výpočet pojistných zásob.</span><span class="sxs-lookup"><span data-stu-id="bb116-115">Go to Safety stock calculation.</span></span>
2. <span data-ttu-id="bb116-116">Klikněte na položku Nová.</span><span class="sxs-lookup"><span data-stu-id="bb116-116">Click New.</span></span>
3. <span data-ttu-id="bb116-117">V poli Název zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="bb116-117">In the Name field, enter or select a value.</span></span>
    * <span data-ttu-id="bb116-118">Vyberte vámi vytvořený názvu deníku pojistných zásob, jako například Materiál.</span><span class="sxs-lookup"><span data-stu-id="bb116-118">Select the safety stock journal name that you created, for example, Material.</span></span>  
4. <span data-ttu-id="bb116-119">Klikněte na Vytvořit řádky.</span><span class="sxs-lookup"><span data-stu-id="bb116-119">Click Create lines.</span></span>
5. <span data-ttu-id="bb116-120">Zadejte datum do pole Od data.</span><span class="sxs-lookup"><span data-stu-id="bb116-120">In the From date field, enter a date.</span></span>
    * <span data-ttu-id="bb116-121">Nastavte datum na '2015-01-02'.</span><span class="sxs-lookup"><span data-stu-id="bb116-121">Set the date to '2015-01-02'.</span></span>  
6. <span data-ttu-id="bb116-122">Do pole Do data zadejte datum.</span><span class="sxs-lookup"><span data-stu-id="bb116-122">In the To date field, enter a date.</span></span>
    * <span data-ttu-id="bb116-123">Nastavte datum na '2015-12-30'.</span><span class="sxs-lookup"><span data-stu-id="bb116-123">Set the date to '2015-12-30'.</span></span>  
7. <span data-ttu-id="bb116-124">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="bb116-124">Click OK.</span></span>
    * <span data-ttu-id="bb116-125">Dojde tak k vytvoření řádků pro dimenze, pro něž existují skladové transakce.</span><span class="sxs-lookup"><span data-stu-id="bb116-125">This will create lines for the dimensions that have inventory transactions.</span></span>  

## <a name="calculate-proposal"></a><span data-ttu-id="bb116-126">Vypočítat návrh</span><span class="sxs-lookup"><span data-stu-id="bb116-126">Calculate proposal</span></span>
1. <span data-ttu-id="bb116-127">Klikněte na Vypočítat návrh.</span><span class="sxs-lookup"><span data-stu-id="bb116-127">Click Calculate proposal.</span></span>
2. <span data-ttu-id="bb116-128">Vyberte možnost Použít průměrný výdej během doby realizace.</span><span class="sxs-lookup"><span data-stu-id="bb116-128">Select the Use average issue during lead time option.</span></span>
3. <span data-ttu-id="bb116-129">Nastavte Koeficient násobení na 10.</span><span class="sxs-lookup"><span data-stu-id="bb116-129">Set Multiplication factor to '10'.</span></span>
    * <span data-ttu-id="bb116-130">Koeficient pro násobení slouží k úpravě návrhu.</span><span class="sxs-lookup"><span data-stu-id="bb116-130">The Multiply factor is used to adjust the proposal.</span></span> <span data-ttu-id="bb116-131">Vzhledem k tomu, že ukázková data mají pouze několik transakcí, musíte nastavit koeficient k získání reálných návrhu.</span><span class="sxs-lookup"><span data-stu-id="bb116-131">Because demo data only has a few transactions, you will need to set the factor to get a realistic proposal.</span></span>  
4. <span data-ttu-id="bb116-132">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="bb116-132">Click OK.</span></span>
    * <span data-ttu-id="bb116-133">Přejděte dolů a vyhledejte M0002 a M0003.</span><span class="sxs-lookup"><span data-stu-id="bb116-133">Scroll down to find M0002 and M0003.</span></span> <span data-ttu-id="bb116-134">Otevřete sloupec Vypočítané minimální množství.</span><span class="sxs-lookup"><span data-stu-id="bb116-134">View the Calculated minimum quantity column.</span></span>   

## <a name="update-minimum-quantity"></a><span data-ttu-id="bb116-135">Aktualizace minimálního množství</span><span class="sxs-lookup"><span data-stu-id="bb116-135">Update minimum quantity</span></span>
1. <span data-ttu-id="bb116-136">V poli Nové minimální množství zadejte číslo.</span><span class="sxs-lookup"><span data-stu-id="bb116-136">In the New minimum quantity field, enter a number.</span></span>
    * <span data-ttu-id="bb116-137">Aktualizujte Nové minimální množství tak, aby odpovídalo hodnotě Vypočítané minimální množství.</span><span class="sxs-lookup"><span data-stu-id="bb116-137">Update the New minimum quantity to match the value in the Calculated minimum quantity.</span></span> <span data-ttu-id="bb116-138">Pokud je Vypočítané minimální množství nulové, můžete zadat požadovanou budoucí hodnotu.</span><span class="sxs-lookup"><span data-stu-id="bb116-138">If the Calculated minimum is zero,  you can enter the desired future value.</span></span> <span data-ttu-id="bb116-139">Například můžete zadat Vypočítané minimální množství v tomto poli pro M0002, pro které je přiřazen sklad 12.</span><span class="sxs-lookup"><span data-stu-id="bb116-139">For example, you can enter the Calculated minimum quantity in this field for M0002 that has warehouse 12.</span></span>  
2. <span data-ttu-id="bb116-140">Vyhledejte na seznamu požadovaný záznam a vyberte ho.</span><span class="sxs-lookup"><span data-stu-id="bb116-140">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="bb116-141">Můžete například vybrat M0002 se skladem 12.</span><span class="sxs-lookup"><span data-stu-id="bb116-141">For example, you can select M0002 that has warehouse 12.</span></span>  
3. <span data-ttu-id="bb116-142">V poli Nové minimální množství zadejte číslo.</span><span class="sxs-lookup"><span data-stu-id="bb116-142">In the New minimum quantity field, enter a number.</span></span>
    * <span data-ttu-id="bb116-143">Aktualizujte Nové minimální množství tak, aby odpovídalo hodnotě Vypočítané minimální množství.</span><span class="sxs-lookup"><span data-stu-id="bb116-143">Update the New minimum quantity to match the value in the Calculated minimum quantity.</span></span> <span data-ttu-id="bb116-144">Pokud je Vypočítané minimální množství nulové, můžete zadat požadovanou budoucí hodnotu.</span><span class="sxs-lookup"><span data-stu-id="bb116-144">If the Calculated minimum is zero you can enter the desired future value.</span></span>  

## <a name="post-the-new-minimum-quantity-and-validate-the-result"></a><span data-ttu-id="bb116-145">Zaúčtování nového minimálního množství a ověření výsledku</span><span class="sxs-lookup"><span data-stu-id="bb116-145">Post the new minimum quantity and validate the result</span></span>
1. <span data-ttu-id="bb116-146">Klikněte na položku Zaúčtovat.</span><span class="sxs-lookup"><span data-stu-id="bb116-146">Click Post.</span></span>
2. <span data-ttu-id="bb116-147">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="bb116-147">Click OK.</span></span>
3. <span data-ttu-id="bb116-148">Kliknutím přejdete na odkaz v poli Číslo položky.</span><span class="sxs-lookup"><span data-stu-id="bb116-148">Click to follow the link in the Item number field.</span></span>
4. <span data-ttu-id="bb116-149">Kliknutím přejdete na odkaz v poli Číslo položky.</span><span class="sxs-lookup"><span data-stu-id="bb116-149">Click to follow the link in the Item number field.</span></span>
5. <span data-ttu-id="bb116-150">V podokně akcí klikněte na položku Plán.</span><span class="sxs-lookup"><span data-stu-id="bb116-150">On the Action Pane, click Plan.</span></span>
6. <span data-ttu-id="bb116-151">Klikněte na Disponibilita položky.</span><span class="sxs-lookup"><span data-stu-id="bb116-151">Click Item coverage.</span></span>
    * <span data-ttu-id="bb116-152">Všimněte si, že bylo aktualizováno minimální množství s novým minimálním množstvím z deníku pojistných zásob.</span><span class="sxs-lookup"><span data-stu-id="bb116-152">Notice that the Minimum quantity has been updated with the new minimum quantity from the safety stock journal.</span></span>  


