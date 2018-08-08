--- 
title: "Nastavení hierarchie kategorií zásobování"
description: "Tento postup popisuje vytvoření nových uzlů v hierarchii kategorií zásobování a konfiguraci kategorie zásobování pro použití v procesu zásobování."
author: mkirknel
manager: AnnBe
ms.date: 11/06/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: d9747ba144d56c9410846769e5465372c89ea111
ms.openlocfilehash: 01809a8a3256342682d8a9cfb296a355310fe4ed
ms.contentlocale: cs-cz
ms.lasthandoff: 08/07/2018

---
# <a name="set-up-a-procurement-category-hierarchy"></a><span data-ttu-id="8b709-103">Nastavení hierarchie kategorií zásobování</span><span class="sxs-lookup"><span data-stu-id="8b709-103">Set up a procurement category hierarchy</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="8b709-104">Tento postup popisuje vytvoření nových uzlů v hierarchii kategorií zásobování a konfiguraci kategorie zásobování pro použití v procesu zásobování.</span><span class="sxs-lookup"><span data-stu-id="8b709-104">This procedure shows you how to create new nodes in a procurement category hierarchy and how to configure a procurement category to be used in a procurement process.</span></span> <span data-ttu-id="8b709-105">Tyto úkoly obvykle provádějí vedoucí nákupu.</span><span class="sxs-lookup"><span data-stu-id="8b709-105">These tasks would typically be carried out by a Purchasing manager.</span></span> <span data-ttu-id="8b709-106">Před zahájením tohoto postupu musí existovat hierarchie kategorií typu Zásobování.</span><span class="sxs-lookup"><span data-stu-id="8b709-106">Before you can start this procedure, there must be a category hierarchy of type Procurement.</span></span> <span data-ttu-id="8b709-107">Používáte-li ukázková data společnosti, můžete tento postup provést se společností USMF.</span><span class="sxs-lookup"><span data-stu-id="8b709-107">If you're using a demo data company, you can run this procedure in the USMF company.</span></span>


## <a name="add-a-new-procurement-category"></a><span data-ttu-id="8b709-108">Přidání nové kategorie zásobování</span><span class="sxs-lookup"><span data-stu-id="8b709-108">Add a new procurement category</span></span>
1. <span data-ttu-id="8b709-109">Přejděte do nabídky Zásobování a zdroje > Kategorie zásobování.</span><span class="sxs-lookup"><span data-stu-id="8b709-109">Go to Procurement and sourcing > Procurement categories.</span></span>
2. <span data-ttu-id="8b709-110">Klikněte na možnost Upravit hierarchii kategorií.</span><span class="sxs-lookup"><span data-stu-id="8b709-110">Click Edit category hierarchy.</span></span>
    * <span data-ttu-id="8b709-111">Aktuální hierarchie kategorií zásobování se zobrazí v levé části stránky.</span><span class="sxs-lookup"><span data-stu-id="8b709-111">The current procurement category hierarchy is displayed in the left side of the page.</span></span> <span data-ttu-id="8b709-112">Chystáte se upravit hierarchii.</span><span class="sxs-lookup"><span data-stu-id="8b709-112">You  are about to modify the hierarchy.</span></span>  
3. <span data-ttu-id="8b709-113">Klikněte na možnost Nový uzel kategorie.</span><span class="sxs-lookup"><span data-stu-id="8b709-113">Click New category node.</span></span>
    * <span data-ttu-id="8b709-114">Systém vybere ve výchozím nastavení nejvyšší uzel.</span><span class="sxs-lookup"><span data-stu-id="8b709-114">The system selects the top node by default.</span></span> <span data-ttu-id="8b709-115">Používáte-li tento postup jako úkol průvodce, lze kliknout na tlačítko Odemknout a vybrat jiný nadřazený uzel pro vložení nového uzlu.</span><span class="sxs-lookup"><span data-stu-id="8b709-115">If you are running this procedure as a task guide, you can click the Unlock button and select another parent node to insert your new node into.</span></span> <span data-ttu-id="8b709-116">Po skončení znovu zamkněte průvodce úkolem a pak klikněte na uzel Nová kategorie.</span><span class="sxs-lookup"><span data-stu-id="8b709-116">Once that is done, lock the task guide again and then click New category node.</span></span>  
4. <span data-ttu-id="8b709-117">Zadejte hodnotu do pole Název.</span><span class="sxs-lookup"><span data-stu-id="8b709-117">In the Name field, type a value.</span></span>
5. <span data-ttu-id="8b709-118">Zadejte nějakou hodnotu do pole Popis.</span><span class="sxs-lookup"><span data-stu-id="8b709-118">In the Description field, type a value.</span></span>
6. <span data-ttu-id="8b709-119">Do pole Popisný název zadejte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="8b709-119">In the Friendly name field, type a value.</span></span>
    * <span data-ttu-id="8b709-120">Popisný název je volitelný.</span><span class="sxs-lookup"><span data-stu-id="8b709-120">The friendly name is optional.</span></span> <span data-ttu-id="8b709-121">Zobrazí se ve vyhledávání kategorií společně s názvem kategorie.</span><span class="sxs-lookup"><span data-stu-id="8b709-121">It will be displayed in category lookups together with the category name.</span></span>  
7. <span data-ttu-id="8b709-122">Klikněte na položku Uložit.</span><span class="sxs-lookup"><span data-stu-id="8b709-122">Click Save.</span></span>

## <a name="add-products-to-your-new-procurement-category"></a><span data-ttu-id="8b709-123">Přidání produktů do nové kategorie zásobování</span><span class="sxs-lookup"><span data-stu-id="8b709-123">Add products to your new procurement category</span></span>
1. <span data-ttu-id="8b709-124">Přejděte do nabídky Zásobování a zdroje > Kategorie zásobování.</span><span class="sxs-lookup"><span data-stu-id="8b709-124">Go to Procurement and sourcing > Procurement categories.</span></span>
    * <span data-ttu-id="8b709-125">Vyberte uzel, který jste právě přidali.</span><span class="sxs-lookup"><span data-stu-id="8b709-125">Select the node you just added.</span></span> <span data-ttu-id="8b709-126">Pokud tento postup používáte jako průvodce úkolem, možná bude třeba průvodce odemknout, aby bylo možné uzel vybrat.</span><span class="sxs-lookup"><span data-stu-id="8b709-126">If you’re running this procedure as a task guide you might need to unlock the task guide to select the node.</span></span>  
2. <span data-ttu-id="8b709-127">Rozbalte oddíl Produkty.</span><span class="sxs-lookup"><span data-stu-id="8b709-127">Toggle the expansion of the Products section.</span></span>
3. <span data-ttu-id="8b709-128">Kliknutím na tlačítko Přidat přidružte produkty ke kategorii zásobování.</span><span class="sxs-lookup"><span data-stu-id="8b709-128">Click Add to associate products with the procurement category.</span></span>
4. <span data-ttu-id="8b709-129">Vyberte produkt, který chcete přidat do kategorie zásobování.</span><span class="sxs-lookup"><span data-stu-id="8b709-129">Select the product you want to add to the procurement category.</span></span>
5. <span data-ttu-id="8b709-130">Kliknutím na šipku vyberte produkt.</span><span class="sxs-lookup"><span data-stu-id="8b709-130">Click the arrow to select the product.</span></span>
6. <span data-ttu-id="8b709-131">Vyberte další produkt, který chcete přidat do kategorie zásobování.</span><span class="sxs-lookup"><span data-stu-id="8b709-131">Select another product to add to the procurement category.</span></span>
7. <span data-ttu-id="8b709-132">Kliknutím na šipku vyberte produkt.</span><span class="sxs-lookup"><span data-stu-id="8b709-132">Click the arrow to select the product.</span></span>
8. <span data-ttu-id="8b709-133">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="8b709-133">Click OK.</span></span>

## <a name="add-approved-and-preferred-vendors"></a><span data-ttu-id="8b709-134">Přidání schválených a upřednostňovaných dodavatelů</span><span class="sxs-lookup"><span data-stu-id="8b709-134">Add approved and preferred vendors</span></span>
1. <span data-ttu-id="8b709-135">Přepněte rozšíření oddílu Dodavatelé.</span><span class="sxs-lookup"><span data-stu-id="8b709-135">Toggle the expansion of the Vendors section.</span></span>
2. <span data-ttu-id="8b709-136">Klepněte na možnost Přidat.</span><span class="sxs-lookup"><span data-stu-id="8b709-136">Click Add.</span></span>
    * <span data-ttu-id="8b709-137">Můžete přidat dodavatele do kategorie zásobování a určit, zda se jedná o upřednostňovaného dodavatele nebo jen schváleného dodavatele pro danou kategorii.</span><span class="sxs-lookup"><span data-stu-id="8b709-137">You can add a vendor to a procurement category and specify whether a vendor is preferred or just approved for the category.</span></span> <span data-ttu-id="8b709-138">Při odstraňování dodavatele z kategorie, nebudou odstraněny historické transakce s dodavatelem v kategorii.</span><span class="sxs-lookup"><span data-stu-id="8b709-138">When you delete a vendor from a category, the historical transactions with the vendor in the category are not deleted.</span></span>   
3. <span data-ttu-id="8b709-139">Vyhledejte dodavatele, kterého chcete do kategorie přidat.</span><span class="sxs-lookup"><span data-stu-id="8b709-139">Find the vendor you want to add to the category.</span></span>
4. <span data-ttu-id="8b709-140">Kliknutím na šipku vyberte dodavatele.</span><span class="sxs-lookup"><span data-stu-id="8b709-140">Click the arrow to select the vendor.</span></span>
5. <span data-ttu-id="8b709-141">Klepněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="8b709-141">Click OK.</span></span>
6. <span data-ttu-id="8b709-142">Vyberte řádek dodavatele, který chcete upravit.</span><span class="sxs-lookup"><span data-stu-id="8b709-142">Select the vendor row that you want to modify.</span></span>
7. <span data-ttu-id="8b709-143">Vyberte možnost v poli Stav dodavatele.</span><span class="sxs-lookup"><span data-stu-id="8b709-143">In the Vendor status field, select an option.</span></span>
    * <span data-ttu-id="8b709-144">Nastavení volby dodavatele v pravidle zásad kategorie určí, zda jsou upřednostňovaní, schválení nebo všichni dodavatelé k dispozici na nákupních žádankách.</span><span class="sxs-lookup"><span data-stu-id="8b709-144">The vendor selection setting in the Category policy rule governs whether preferred, approved, or all vendors are available on purchase requisitions.</span></span>   

## <a name="add-additional-information-to-the-category"></a><span data-ttu-id="8b709-145">Přidání dalších informací do kategorie</span><span class="sxs-lookup"><span data-stu-id="8b709-145">Add additional information to the category</span></span>
1. <span data-ttu-id="8b709-146">Rozbalte oddíl Skupiny kritérií hodnocení dodavatelů.</span><span class="sxs-lookup"><span data-stu-id="8b709-146">Toggle the expansion of the Vendor evaluation criterion groups section.</span></span>
    * <span data-ttu-id="8b709-147">Na této kartě můžete definovat kritéria pro hodnocení dodavatelů v kategorii zásobování.</span><span class="sxs-lookup"><span data-stu-id="8b709-147">This tab allows you to define which criteria the vendors in the procurement category should be rated against.</span></span> <span data-ttu-id="8b709-148">Tento krok lze provést by kliknutím na tlačítko Přidat a poté zvolením skupiny hodnocení dodavatelů, která obsahuje požadovaná kritéria.</span><span class="sxs-lookup"><span data-stu-id="8b709-148">To do this you would click Add and then select a vendor evaluation group that contains the criteria you want.</span></span>  
2. <span data-ttu-id="8b709-149">Rozbalte oddíl Dotazníky.</span><span class="sxs-lookup"><span data-stu-id="8b709-149">Toggle the expansion of the Questionnaires section.</span></span>
    * <span data-ttu-id="8b709-150">Na této kartě lze přidat dotazníky, které se objeví na žádance, pokud nastavíte typ aktivity „Žádanka“.</span><span class="sxs-lookup"><span data-stu-id="8b709-150">This tab allows you to add questionnaires that will appear on the requisition, as long as you set the Activity type to "Requisition".</span></span> <span data-ttu-id="8b709-151">Žadatel potom musí vyplnit dotazník, aby mohl odeslat žádanku pro konkrétní produkt nebo produkty v kategorii zásobování.</span><span class="sxs-lookup"><span data-stu-id="8b709-151">The requester then has to fill out a questionnaire before they submit a requisition for the specific product or products in the procurement category.</span></span>  
3. <span data-ttu-id="8b709-152">Rozbalte oddíl Skupiny prodejní daně položky.</span><span class="sxs-lookup"><span data-stu-id="8b709-152">Toggle the expansion of the Item sales tax groups section.</span></span>
4. <span data-ttu-id="8b709-153">V poli Skupina DPH zboží kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.</span><span class="sxs-lookup"><span data-stu-id="8b709-153">In the Item sales tax group: field, click the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="8b709-154">Vyberte skupinu DPH.</span><span class="sxs-lookup"><span data-stu-id="8b709-154">Select a sales tax group.</span></span>
6. <span data-ttu-id="8b709-155">Rozbalte oddíl Stránka kategorie.</span><span class="sxs-lookup"><span data-stu-id="8b709-155">Toggle the expansion of the Category page section.</span></span>
    * <span data-ttu-id="8b709-156">Stránky kategorie jsou vytvořeny na stránce Hierarchie kategorií.</span><span class="sxs-lookup"><span data-stu-id="8b709-156">Category pages are created in the Category hierarchy page.</span></span> <span data-ttu-id="8b709-157">Obsahují informace o kategorii zásobování, jako jsou informace o typu produktů v kategorii, obrázky produktů v kategorii a oznámení, jako např. prodej nebo sleva, které jsou v kategorii k dispozici.</span><span class="sxs-lookup"><span data-stu-id="8b709-157">They contain information about the procurement category such as information about the type of products in a category, images of products in a category, or announcements such as the discounts that are available in a category.</span></span> <span data-ttu-id="8b709-158">Informace na stránce kategorie budou zobrazeny na nákupní žádance.</span><span class="sxs-lookup"><span data-stu-id="8b709-158">The information in a category page is displayed on purchase requisitions.</span></span>  
7. <span data-ttu-id="8b709-159">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="8b709-159">Close the page.</span></span>


