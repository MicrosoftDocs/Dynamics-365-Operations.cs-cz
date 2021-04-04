---
title: Použití deníku pojistných zásob pro aktualizaci minimální disponibility
description: Tento postup popisuje způsob výpočtu návrhů minimální disponibility na základě historických transakcí, a pokrytí následně aktualizaci disponibility položky podle návrhů.
author: ChristianRytt
manager: tfehr
ms.date: 08/09/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqItemJournalName, ReqItemJournalSafetyStock, EcoResProductInformationDialog, EcoResProductDetailsExtended, ReqItemTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 95dec1dba97923e58cfb603434a01cab6f66a3de
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/15/2021
ms.locfileid: "5252791"
---
# <a name="use-the-safety-stock-journal-to-update-minimum-coverage"></a><span data-ttu-id="4e9d8-103">Použití deníku pojistných zásob pro aktualizaci minimální disponibility</span><span class="sxs-lookup"><span data-stu-id="4e9d8-103">Use the safety stock journal to update minimum coverage</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="4e9d8-104">Tento postup popisuje způsob výpočtu návrhů minimální disponibility na základě historických transakcí, a pokrytí následně aktualizaci disponibility položky podle návrhů.</span><span class="sxs-lookup"><span data-stu-id="4e9d8-104">This procedure shows how to calculate minimum coverage proposals based on historical transactions and then update the item coverage with the proposals.</span></span> <span data-ttu-id="4e9d8-105">To se provádí pomocí deníku pojistných zásob.</span><span class="sxs-lookup"><span data-stu-id="4e9d8-105">This is done using the safety stock journal.</span></span> <span data-ttu-id="4e9d8-106">Tento úkol byl vytvořen pomocí ukázkových dat společnosti USMF.</span><span class="sxs-lookup"><span data-stu-id="4e9d8-106">The demo data company used to create this task is USMF.</span></span> <span data-ttu-id="4e9d8-107">Tato úloha je určena pro plánovače výroby k zachování minimální disponibility.</span><span class="sxs-lookup"><span data-stu-id="4e9d8-107">This task is intended for the production planner, to help maintain minimum coverage.</span></span>


## <a name="create-a-new-safety-stock-journal-name"></a><span data-ttu-id="4e9d8-108">Vytvoření názvu nového deníku pojistných zásob</span><span class="sxs-lookup"><span data-stu-id="4e9d8-108">Create a new safety stock journal name</span></span>
1. <span data-ttu-id="4e9d8-109">V **Navigačním podokně** přejděte na **Hlavní plánování > Nastavení > Názvy deníků pojistných zásob**.</span><span class="sxs-lookup"><span data-stu-id="4e9d8-109">In the **Navigation pane**, go to **Master planning > Setup > Safety stock journal names**.</span></span>
2. <span data-ttu-id="4e9d8-110">Klepněte na možnost **Nový**.</span><span class="sxs-lookup"><span data-stu-id="4e9d8-110">Click **New**.</span></span>
3. <span data-ttu-id="4e9d8-111">Do pole **Název** zadejte „Materiál“.</span><span class="sxs-lookup"><span data-stu-id="4e9d8-111">In the **Name** field, type 'Material'.</span></span>
4. <span data-ttu-id="4e9d8-112">V poli **Popis** uveďte text „Materiál“.</span><span class="sxs-lookup"><span data-stu-id="4e9d8-112">In the **Description** field, type 'Material'.</span></span>
5. <span data-ttu-id="4e9d8-113">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="4e9d8-113">Close the page.</span></span>

## <a name="create-a-safety-stock-journal"></a><span data-ttu-id="4e9d8-114">Vytvoření deníku pojistných zásob</span><span class="sxs-lookup"><span data-stu-id="4e9d8-114">Create a safety stock journal</span></span>
1. <span data-ttu-id="4e9d8-115">V **Navigačním podokně** přejděte na **Hlavní plánování > Hlavní plánování > Spustit > Výpočet pojistných zásob**.</span><span class="sxs-lookup"><span data-stu-id="4e9d8-115">In the **Navigation pane**, go to **Master planning > Master planning > Run > Safety stock calculation**.</span></span>
2. <span data-ttu-id="4e9d8-116">Klepněte na možnost **Nový**.</span><span class="sxs-lookup"><span data-stu-id="4e9d8-116">Click **New**.</span></span>
3. <span data-ttu-id="4e9d8-117">V poli **Název** zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="4e9d8-117">In the **Name** field, enter or select a value.</span></span> <span data-ttu-id="4e9d8-118">Vyberte vámi vytvořený názvu deníku pojistných zásob, jako například Materiál.</span><span class="sxs-lookup"><span data-stu-id="4e9d8-118">Select the safety stock journal name that you created, for example, Material.</span></span>  
4. <span data-ttu-id="4e9d8-119">Klikněte na **Vytvořit řádky**.</span><span class="sxs-lookup"><span data-stu-id="4e9d8-119">Click **Create lines**.</span></span>
5. <span data-ttu-id="4e9d8-120">Do pole **Od data** zadejte datum.</span><span class="sxs-lookup"><span data-stu-id="4e9d8-120">In the **From date** field, enter a date.</span></span>  
6. <span data-ttu-id="4e9d8-121">Do pole **Do data** zadejte datum.</span><span class="sxs-lookup"><span data-stu-id="4e9d8-121">In the **To date** field, enter a date.</span></span>
7. <span data-ttu-id="4e9d8-122">Klikněte na tlačítko **OK**.</span><span class="sxs-lookup"><span data-stu-id="4e9d8-122">Click **OK**.</span></span> <span data-ttu-id="4e9d8-123">Dojde tak k vytvoření řádků pro dimenze, pro něž existují skladové transakce.</span><span class="sxs-lookup"><span data-stu-id="4e9d8-123">This will create lines for the dimensions that have inventory transactions.</span></span>  

## <a name="calculate-proposal"></a><span data-ttu-id="4e9d8-124">Vypočítat návrh</span><span class="sxs-lookup"><span data-stu-id="4e9d8-124">Calculate proposal</span></span>
1. <span data-ttu-id="4e9d8-125">Klikněte na **Vypočítat návrh**.</span><span class="sxs-lookup"><span data-stu-id="4e9d8-125">Click **Calculate proposal**.</span></span>
2. <span data-ttu-id="4e9d8-126">Vyberte možnost **Použít průměrný výdej během doby realizace**.</span><span class="sxs-lookup"><span data-stu-id="4e9d8-126">Select the **Use average issue during lead time** option.</span></span>
3. <span data-ttu-id="4e9d8-127">Nastavte **Koeficient násobení** na 10.</span><span class="sxs-lookup"><span data-stu-id="4e9d8-127">Set **Multiplication factor** to '10'.</span></span> <span data-ttu-id="4e9d8-128">Koeficient pro násobení slouží k úpravě návrhu.</span><span class="sxs-lookup"><span data-stu-id="4e9d8-128">The Multiply factor is used to adjust the proposal.</span></span> <span data-ttu-id="4e9d8-129">Vzhledem k tomu, že ukázková data mají pouze několik transakcí, musíte nastavit koeficient k získání reálných návrhu.</span><span class="sxs-lookup"><span data-stu-id="4e9d8-129">Because demo data only has a few transactions, you will need to set the factor to get a realistic proposal.</span></span>  
4. <span data-ttu-id="4e9d8-130">Klikněte na tlačítko **OK**.</span><span class="sxs-lookup"><span data-stu-id="4e9d8-130">Click **OK**.</span></span> <span data-ttu-id="4e9d8-131">Přejděte dolů a vyhledejte M0002 a M0003.</span><span class="sxs-lookup"><span data-stu-id="4e9d8-131">Scroll down to find M0002 and M0003.</span></span> <span data-ttu-id="4e9d8-132">Otevřete sloupec **Vypočítané minimální** množství.</span><span class="sxs-lookup"><span data-stu-id="4e9d8-132">View the **Calculated minimum** quantity column.</span></span>   

## <a name="update-minimum-quantity"></a><span data-ttu-id="4e9d8-133">Aktualizace minimálního množství</span><span class="sxs-lookup"><span data-stu-id="4e9d8-133">Update minimum quantity</span></span>
1. <span data-ttu-id="4e9d8-134">V poli **Nové minimální množství** zadejte číslo.</span><span class="sxs-lookup"><span data-stu-id="4e9d8-134">In the **New minimum quantity** field, enter a number.</span></span> <span data-ttu-id="4e9d8-135">Aktualizujte Nové minimální množství tak, aby odpovídalo hodnotě Vypočítané minimální množství.</span><span class="sxs-lookup"><span data-stu-id="4e9d8-135">Update the New minimum quantity to match the value in the Calculated minimum quantity.</span></span> <span data-ttu-id="4e9d8-136">Pokud je Vypočítané minimální množství nulové, můžete zadat požadovanou budoucí hodnotu.</span><span class="sxs-lookup"><span data-stu-id="4e9d8-136">If the Calculated minimum is zero,  you can enter the desired future value.</span></span> <span data-ttu-id="4e9d8-137">Například můžete zadat Vypočítané minimální množství v tomto poli pro M0002, pro které je přiřazen sklad 12.</span><span class="sxs-lookup"><span data-stu-id="4e9d8-137">For example, you can enter the Calculated minimum quantity in this field for M0002 that has warehouse 12.</span></span>  
2. <span data-ttu-id="4e9d8-138">Vyhledejte na seznamu požadovaný záznam a vyberte ho.</span><span class="sxs-lookup"><span data-stu-id="4e9d8-138">In the list, find and select the desired record.</span></span> <span data-ttu-id="4e9d8-139">Můžete například vybrat M0002 se skladem 12.</span><span class="sxs-lookup"><span data-stu-id="4e9d8-139">For example, you can select M0002 that has warehouse 12.</span></span>  
3. <span data-ttu-id="4e9d8-140">V poli **Nové minimální množství** zadejte číslo.</span><span class="sxs-lookup"><span data-stu-id="4e9d8-140">In the **New minimum quantity** field, enter a number.</span></span> <span data-ttu-id="4e9d8-141">Aktualizujte Nové minimální množství tak, aby odpovídalo hodnotě Vypočítané minimální množství.</span><span class="sxs-lookup"><span data-stu-id="4e9d8-141">Update the New minimum quantity to match the value in the Calculated minimum quantity.</span></span> <span data-ttu-id="4e9d8-142">Pokud je Vypočítané minimální množství nulové, můžete zadat požadovanou budoucí hodnotu.</span><span class="sxs-lookup"><span data-stu-id="4e9d8-142">If the Calculated minimum is zero you can enter the desired future value.</span></span>  

## <a name="post-the-new-minimum-quantity-and-validate-the-result"></a><span data-ttu-id="4e9d8-143">Zaúčtování nového minimálního množství a ověření výsledku</span><span class="sxs-lookup"><span data-stu-id="4e9d8-143">Post the new minimum quantity and validate the result</span></span>
1. <span data-ttu-id="4e9d8-144">Klikněte na možnost **Zaúčtovat**.</span><span class="sxs-lookup"><span data-stu-id="4e9d8-144">Click **Post**.</span></span>
2. <span data-ttu-id="4e9d8-145">Klikněte na tlačítko **OK**.</span><span class="sxs-lookup"><span data-stu-id="4e9d8-145">Click **OK**.</span></span>
3. <span data-ttu-id="4e9d8-146">Kliknutím přejdete na odkaz v poli **Číslo položky**.</span><span class="sxs-lookup"><span data-stu-id="4e9d8-146">Click to follow the link in the **Item number** field.</span></span>
4. <span data-ttu-id="4e9d8-147">Kliknutím přejdete na odkaz v poli **Číslo položky**.</span><span class="sxs-lookup"><span data-stu-id="4e9d8-147">Click to follow the link in the **Item number** field.</span></span>
5. <span data-ttu-id="4e9d8-148">V **podokně akcí** klikněte na možnost Plán.</span><span class="sxs-lookup"><span data-stu-id="4e9d8-148">On the **Action Pane**, click Plan.</span></span>
6. <span data-ttu-id="4e9d8-149">Klikněte na **Disponibilita položky**.</span><span class="sxs-lookup"><span data-stu-id="4e9d8-149">Click **Item coverage**.</span></span> <span data-ttu-id="4e9d8-150">Všimněte si, že bylo aktualizováno **Minimální množství** s novým minimálním množstvím z deníku pojistných zásob.</span><span class="sxs-lookup"><span data-stu-id="4e9d8-150">Notice that the **Minimum quantity** has been updated with the new minimum quantity from the safety stock journal.</span></span>  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]