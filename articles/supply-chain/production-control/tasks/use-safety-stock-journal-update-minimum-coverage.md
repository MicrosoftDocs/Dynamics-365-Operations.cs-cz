---
title: Použití deníku pojistných zásob pro aktualizaci minimální disponibility
description: Tento postup popisuje způsob výpočtu návrhů minimální disponibility na základě historických transakcí, a pokrytí následně aktualizaci disponibility položky podle návrhů.
author: ChristianRytt
manager: AnnBe
ms.date: 08/09/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqItemJournalName, ReqItemJournalSafetyStock, EcoResProductInformationDialog, EcoResProductDetailsExtended, ReqItemTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 478dd85abebf76dd264e93bcbe3f218a0ff0a5a8
ms.sourcegitcommit: cbcf344b3b552acca56c3e27606eac7f2f124afe
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/22/2019
ms.locfileid: "1916799"
---
# <a name="use-the-safety-stock-journal-to-update-minimum-coverage"></a><span data-ttu-id="abcd2-103">Použití deníku pojistných zásob pro aktualizaci minimální disponibility</span><span class="sxs-lookup"><span data-stu-id="abcd2-103">Use the safety stock journal to update minimum coverage</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="abcd2-104">Tento postup popisuje způsob výpočtu návrhů minimální disponibility na základě historických transakcí, a pokrytí následně aktualizaci disponibility položky podle návrhů.</span><span class="sxs-lookup"><span data-stu-id="abcd2-104">This procedure shows how to calculate minimum coverage proposals based on historical transactions and then update the item coverage with the proposals.</span></span> <span data-ttu-id="abcd2-105">To se provádí pomocí deníku pojistných zásob.</span><span class="sxs-lookup"><span data-stu-id="abcd2-105">This is done using the safety stock journal.</span></span> <span data-ttu-id="abcd2-106">Tento úkol byl vytvořen pomocí ukázkových dat společnosti USMF.</span><span class="sxs-lookup"><span data-stu-id="abcd2-106">The demo data company used to create this task is USMF.</span></span> <span data-ttu-id="abcd2-107">Tato úloha je určena pro plánovače výroby k zachování minimální disponibility.</span><span class="sxs-lookup"><span data-stu-id="abcd2-107">This task is intended for the production planner, to help maintain minimum coverage.</span></span>


## <a name="create-a-new-safety-stock-journal-name"></a><span data-ttu-id="abcd2-108">Vytvoření názvu nového deníku pojistných zásob</span><span class="sxs-lookup"><span data-stu-id="abcd2-108">Create a new safety stock journal name</span></span>
1. <span data-ttu-id="abcd2-109">V **Navigačním podokně** přejděte na **Hlavní plánování > Nastavení > Názvy deníků pojistných zásob**.</span><span class="sxs-lookup"><span data-stu-id="abcd2-109">In the **Navigation pane**, go to **Master planning > Setup > Safety stock journal names**.</span></span>
2. <span data-ttu-id="abcd2-110">Klepněte na možnost **Nový**.</span><span class="sxs-lookup"><span data-stu-id="abcd2-110">Click **New**.</span></span>
3. <span data-ttu-id="abcd2-111">Do pole **Název** zadejte „Materiál“.</span><span class="sxs-lookup"><span data-stu-id="abcd2-111">In the **Name** field, type 'Material'.</span></span>
4. <span data-ttu-id="abcd2-112">V poli **Popis** uveďte text „Materiál“.</span><span class="sxs-lookup"><span data-stu-id="abcd2-112">In the **Description** field, type 'Material'.</span></span>
5. <span data-ttu-id="abcd2-113">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="abcd2-113">Close the page.</span></span>

## <a name="create-a-safety-stock-journal"></a><span data-ttu-id="abcd2-114">Vytvoření deníku pojistných zásob</span><span class="sxs-lookup"><span data-stu-id="abcd2-114">Create a safety stock journal</span></span>
1. <span data-ttu-id="abcd2-115">V **Navigačním podokně** přejděte na **Hlavní plánování > Hlavní plánování > Spustit > Výpočet pojistných zásob**.</span><span class="sxs-lookup"><span data-stu-id="abcd2-115">In the **Navigation pane**, go to **Master planning > Master planning > Run > Safety stock calculation**.</span></span>
2. <span data-ttu-id="abcd2-116">Klepněte na možnost **Nový**.</span><span class="sxs-lookup"><span data-stu-id="abcd2-116">Click **New**.</span></span>
3. <span data-ttu-id="abcd2-117">V poli **Název** zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="abcd2-117">In the **Name** field, enter or select a value.</span></span> <span data-ttu-id="abcd2-118">Vyberte vámi vytvořený názvu deníku pojistných zásob, jako například Materiál.</span><span class="sxs-lookup"><span data-stu-id="abcd2-118">Select the safety stock journal name that you created, for example, Material.</span></span>  
4. <span data-ttu-id="abcd2-119">Klikněte na **Vytvořit řádky**.</span><span class="sxs-lookup"><span data-stu-id="abcd2-119">Click **Create lines**.</span></span>
5. <span data-ttu-id="abcd2-120">Do pole **Od data** zadejte datum.</span><span class="sxs-lookup"><span data-stu-id="abcd2-120">In the **From date** field, enter a date.</span></span>  
6. <span data-ttu-id="abcd2-121">Do pole **Do data** zadejte datum.</span><span class="sxs-lookup"><span data-stu-id="abcd2-121">In the **To date** field, enter a date.</span></span>
7. <span data-ttu-id="abcd2-122">Klikněte na tlačítko **OK**.</span><span class="sxs-lookup"><span data-stu-id="abcd2-122">Click **OK**.</span></span> <span data-ttu-id="abcd2-123">Dojde tak k vytvoření řádků pro dimenze, pro něž existují skladové transakce.</span><span class="sxs-lookup"><span data-stu-id="abcd2-123">This will create lines for the dimensions that have inventory transactions.</span></span>  

## <a name="calculate-proposal"></a><span data-ttu-id="abcd2-124">Vypočítat návrh</span><span class="sxs-lookup"><span data-stu-id="abcd2-124">Calculate proposal</span></span>
1. <span data-ttu-id="abcd2-125">Klikněte na **Vypočítat návrh**.</span><span class="sxs-lookup"><span data-stu-id="abcd2-125">Click **Calculate proposal**.</span></span>
2. <span data-ttu-id="abcd2-126">Vyberte možnost **Použít průměrný výdej během doby realizace**.</span><span class="sxs-lookup"><span data-stu-id="abcd2-126">Select the **Use average issue during lead time** option.</span></span>
3. <span data-ttu-id="abcd2-127">Nastavte **Koeficient násobení** na 10.</span><span class="sxs-lookup"><span data-stu-id="abcd2-127">Set **Multiplication factor** to '10'.</span></span> <span data-ttu-id="abcd2-128">Koeficient pro násobení slouží k úpravě návrhu.</span><span class="sxs-lookup"><span data-stu-id="abcd2-128">The Multiply factor is used to adjust the proposal.</span></span> <span data-ttu-id="abcd2-129">Vzhledem k tomu, že ukázková data mají pouze několik transakcí, musíte nastavit koeficient k získání reálných návrhu.</span><span class="sxs-lookup"><span data-stu-id="abcd2-129">Because demo data only has a few transactions, you will need to set the factor to get a realistic proposal.</span></span>  
4. <span data-ttu-id="abcd2-130">Klikněte na tlačítko **OK**.</span><span class="sxs-lookup"><span data-stu-id="abcd2-130">Click **OK**.</span></span> <span data-ttu-id="abcd2-131">Přejděte dolů a vyhledejte M0002 a M0003.</span><span class="sxs-lookup"><span data-stu-id="abcd2-131">Scroll down to find M0002 and M0003.</span></span> <span data-ttu-id="abcd2-132">Otevřete sloupec **Vypočítané minimální** množství.</span><span class="sxs-lookup"><span data-stu-id="abcd2-132">View the **Calculated minimum** quantity column.</span></span>   

## <a name="update-minimum-quantity"></a><span data-ttu-id="abcd2-133">Aktualizace minimálního množství</span><span class="sxs-lookup"><span data-stu-id="abcd2-133">Update minimum quantity</span></span>
1. <span data-ttu-id="abcd2-134">V poli **Nové minimální množství** zadejte číslo.</span><span class="sxs-lookup"><span data-stu-id="abcd2-134">In the **New minimum quantity** field, enter a number.</span></span> <span data-ttu-id="abcd2-135">Aktualizujte Nové minimální množství tak, aby odpovídalo hodnotě Vypočítané minimální množství.</span><span class="sxs-lookup"><span data-stu-id="abcd2-135">Update the New minimum quantity to match the value in the Calculated minimum quantity.</span></span> <span data-ttu-id="abcd2-136">Pokud je Vypočítané minimální množství nulové, můžete zadat požadovanou budoucí hodnotu.</span><span class="sxs-lookup"><span data-stu-id="abcd2-136">If the Calculated minimum is zero,  you can enter the desired future value.</span></span> <span data-ttu-id="abcd2-137">Například můžete zadat Vypočítané minimální množství v tomto poli pro M0002, pro které je přiřazen sklad 12.</span><span class="sxs-lookup"><span data-stu-id="abcd2-137">For example, you can enter the Calculated minimum quantity in this field for M0002 that has warehouse 12.</span></span>  
2. <span data-ttu-id="abcd2-138">Vyhledejte na seznamu požadovaný záznam a vyberte ho.</span><span class="sxs-lookup"><span data-stu-id="abcd2-138">In the list, find and select the desired record.</span></span> <span data-ttu-id="abcd2-139">Můžete například vybrat M0002 se skladem 12.</span><span class="sxs-lookup"><span data-stu-id="abcd2-139">For example, you can select M0002 that has warehouse 12.</span></span>  
3. <span data-ttu-id="abcd2-140">V poli **Nové minimální množství** zadejte číslo.</span><span class="sxs-lookup"><span data-stu-id="abcd2-140">In the **New minimum quantity** field, enter a number.</span></span> <span data-ttu-id="abcd2-141">Aktualizujte Nové minimální množství tak, aby odpovídalo hodnotě Vypočítané minimální množství.</span><span class="sxs-lookup"><span data-stu-id="abcd2-141">Update the New minimum quantity to match the value in the Calculated minimum quantity.</span></span> <span data-ttu-id="abcd2-142">Pokud je Vypočítané minimální množství nulové, můžete zadat požadovanou budoucí hodnotu.</span><span class="sxs-lookup"><span data-stu-id="abcd2-142">If the Calculated minimum is zero you can enter the desired future value.</span></span>  

## <a name="post-the-new-minimum-quantity-and-validate-the-result"></a><span data-ttu-id="abcd2-143">Zaúčtování nového minimálního množství a ověření výsledku</span><span class="sxs-lookup"><span data-stu-id="abcd2-143">Post the new minimum quantity and validate the result</span></span>
1. <span data-ttu-id="abcd2-144">Klikněte na možnost **Zaúčtovat**.</span><span class="sxs-lookup"><span data-stu-id="abcd2-144">Click **Post**.</span></span>
2. <span data-ttu-id="abcd2-145">Klikněte na tlačítko **OK**.</span><span class="sxs-lookup"><span data-stu-id="abcd2-145">Click **OK**.</span></span>
3. <span data-ttu-id="abcd2-146">Kliknutím přejdete na odkaz v poli **Číslo položky**.</span><span class="sxs-lookup"><span data-stu-id="abcd2-146">Click to follow the link in the **Item number** field.</span></span>
4. <span data-ttu-id="abcd2-147">Kliknutím přejdete na odkaz v poli **Číslo položky**.</span><span class="sxs-lookup"><span data-stu-id="abcd2-147">Click to follow the link in the **Item number** field.</span></span>
5. <span data-ttu-id="abcd2-148">V **podokně akcí** klikněte na možnost Plán.</span><span class="sxs-lookup"><span data-stu-id="abcd2-148">On the **Action Pane**, click Plan.</span></span>
6. <span data-ttu-id="abcd2-149">Klikněte na **Disponibilita položky**.</span><span class="sxs-lookup"><span data-stu-id="abcd2-149">Click **Item coverage**.</span></span> <span data-ttu-id="abcd2-150">Všimněte si, že bylo aktualizováno **Minimální množství** s novým minimálním množstvím z deníku pojistných zásob.</span><span class="sxs-lookup"><span data-stu-id="abcd2-150">Notice that the **Minimum quantity** has been updated with the new minimum quantity from the safety stock journal.</span></span>  

