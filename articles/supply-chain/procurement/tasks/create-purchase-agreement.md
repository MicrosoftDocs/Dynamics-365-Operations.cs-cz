--- 
title: "Vytvoření nákupní smlouvy"
description: "Tento postup vám pomůže vytvořit nákupní smlouvu."
author: mkirknel
manager: AnnBe
ms.date: 11/14/2016
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
ms.openlocfilehash: 46b8ff64fd950aae9178133b8aba7a9a2888b074
ms.contentlocale: cs-cz
ms.lasthandoff: 08/07/2018

---
# <a name="create-a-purchase-agreement"></a><span data-ttu-id="6b902-103">Vytvoření nákupní smlouvy</span><span class="sxs-lookup"><span data-stu-id="6b902-103">Create a purchase agreement</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="6b902-104">Tento postup vám pomůže vytvořit nákupní smlouvu.</span><span class="sxs-lookup"><span data-stu-id="6b902-104">This procedure guides you through the creation of a purchase agreement.</span></span> <span data-ttu-id="6b902-105">Toto by obvykle prováděl vedoucí nákupu.</span><span class="sxs-lookup"><span data-stu-id="6b902-105">This would typically be done by a purchasing manager.</span></span> <span data-ttu-id="6b902-106">Tento postup můžete použít s ukázkovými daty společnosti USMF nebo pomocí vlastních dat.</span><span class="sxs-lookup"><span data-stu-id="6b902-106">You can use this procedure in demo data company USMF or on your own data.</span></span> <span data-ttu-id="6b902-107">Než začnete, je třeba nastavit klasifikace nákupní smlouvy.</span><span class="sxs-lookup"><span data-stu-id="6b902-107">You need to have set up purchase agreement classifications before you start.</span></span> <span data-ttu-id="6b902-108">Vytvořenou smlouvu můžete použít při vytváření nákupní objednávky; tím se zkopírují podmínky nákupní smlouvy do záhlaví a jakýchkoli řádků objednávky ovlivněných touto smlouvou.</span><span class="sxs-lookup"><span data-stu-id="6b902-108">Once you've created an agreement you can use it when you create a PO, and this will copy the purchase agreement conditions to the header and to any lines in the order that are affected by the agreement.</span></span>


## <a name="create-a-new-purchase-agreement"></a><span data-ttu-id="6b902-109">Vytvoření nové nákupní smlouvy</span><span class="sxs-lookup"><span data-stu-id="6b902-109">Create a new purchase agreement</span></span>
1. <span data-ttu-id="6b902-110">Přejděte do nabídky Zásobování a zdroje > Nákupní smlouvy > Nákupní smlouvy.</span><span class="sxs-lookup"><span data-stu-id="6b902-110">Go to Procurement and sourcing > Purchase agreements > Purchase agreements.</span></span>
2. <span data-ttu-id="6b902-111">Klikněte na položku Nová.</span><span class="sxs-lookup"><span data-stu-id="6b902-111">Click New.</span></span>
3. <span data-ttu-id="6b902-112">V poli Účet dodavatele kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.</span><span class="sxs-lookup"><span data-stu-id="6b902-112">In the Vendor account field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="6b902-113">Vyhledejte na seznamu požadovaný záznam a vyberte ho.</span><span class="sxs-lookup"><span data-stu-id="6b902-113">In the list, find and select the desired record.</span></span>
5. <span data-ttu-id="6b902-114">Klikněte na odkaz na vybraném řádku v seznamu.</span><span class="sxs-lookup"><span data-stu-id="6b902-114">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="6b902-115">V poli Klasifikace nákupní smlouvy kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.</span><span class="sxs-lookup"><span data-stu-id="6b902-115">In the Purchase agreement classification field, click the drop-down button to open the lookup.</span></span>
7. <span data-ttu-id="6b902-116">Vyhledejte na seznamu požadovaný záznam a vyberte ho.</span><span class="sxs-lookup"><span data-stu-id="6b902-116">In the list, find and select the desired record.</span></span>
8. <span data-ttu-id="6b902-117">Klikněte na odkaz na vybraném řádku v seznamu.</span><span class="sxs-lookup"><span data-stu-id="6b902-117">In the list, click the link in the selected row.</span></span>
9. <span data-ttu-id="6b902-118">Rozbalte sekci Obecné.</span><span class="sxs-lookup"><span data-stu-id="6b902-118">Expand the General section.</span></span>
10. <span data-ttu-id="6b902-119">Do pole Datum vypršení platnosti zadejte datum.</span><span class="sxs-lookup"><span data-stu-id="6b902-119">In the Expiration date field, enter a date.</span></span>
    * <span data-ttu-id="6b902-120">Toto datum vypršení platnosti bude výchozí pro všechny řádky závazků a určí, jak dlouho budou jednotlivé závazky platné.</span><span class="sxs-lookup"><span data-stu-id="6b902-120">This expiration date will be the default for all commitment lines and will determine how long each specific commitment is valid.</span></span>  
11. <span data-ttu-id="6b902-121">V poli Název dokumentu zadejte název nákupní smlouvy.</span><span class="sxs-lookup"><span data-stu-id="6b902-121">In the Document title field, type a name for your purchase agreement.</span></span>
    * <span data-ttu-id="6b902-122">Ponechejte pole Výchozí závazek nastavené na hodnotu Závazek – množství produktu (nebo pokud je nastavená jiná hodnota, změňte ji).</span><span class="sxs-lookup"><span data-stu-id="6b902-122">Leave the Default commitment field set to Product quantity commitment (or change it if it’s not set to this).</span></span>  
    * <span data-ttu-id="6b902-123">Výchozí hodnota závazku určuje možnosti na řádcích smlouvy.</span><span class="sxs-lookup"><span data-stu-id="6b902-123">The default commitment value determines your options on the agreement lines.</span></span> <span data-ttu-id="6b902-124">Pokud potřebujete nový typ závazku při vytváření řádků smlouvy, je nutné změnit výchozí závazek v záhlaví.</span><span class="sxs-lookup"><span data-stu-id="6b902-124">If you need a new commitment type when you’re creating the agreement lines, you need to change the default commitment on the header.</span></span>  <span data-ttu-id="6b902-125">Jsou k dispozici 4 typy závazků: „Závazek – množství produktu“ pro určité množství produktu; „Závazek – hodnota produktu“ pro konkrétní částku měny pro produkt; „Závazek – hodnota kategorie produktu“ pro konkrétní částku měny v kategorii zásobování, kde částka může být pro katalogovou položku nebo nekatalogovou položku; „Závazek ohledně hodnoty“ pro konkrétní částku měny, která může být splněna jakýmkoli produktem nebo jakoukoli kategorií zásobování.</span><span class="sxs-lookup"><span data-stu-id="6b902-125">There are 4 types of commitments: Product quantity commitment - for a specific quantity of a product; Product value commitment - for a specific currency amount of a product; Product category value commitment - for a specific currency amount in a procurement category where the amount can be for a catalog item or a non-catalog item; Value commitment - for a specific currency amount which can be fulfilled by any product or by any procurement category.</span></span>  
12. <span data-ttu-id="6b902-126">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="6b902-126">Click OK.</span></span>

## <a name="add-a-commitment"></a><span data-ttu-id="6b902-127">Přidání závazku</span><span class="sxs-lookup"><span data-stu-id="6b902-127">Add a commitment</span></span>
1. <span data-ttu-id="6b902-128">Klikněte na položku Přidat řádek.</span><span class="sxs-lookup"><span data-stu-id="6b902-128">Click Add line.</span></span>
2. <span data-ttu-id="6b902-129">Označte v seznamu vybraný řádek.</span><span class="sxs-lookup"><span data-stu-id="6b902-129">In the list, mark the selected row.</span></span>
3. <span data-ttu-id="6b902-130">V poli Číslo zboží kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.</span><span class="sxs-lookup"><span data-stu-id="6b902-130">In the Item number field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="6b902-131">Vyberte produkt, pro který chcete přidat závazek.</span><span class="sxs-lookup"><span data-stu-id="6b902-131">Select the product you want to add a commitment for.</span></span>
5. <span data-ttu-id="6b902-132">Klikněte na odkaz na vybraném řádku v seznamu.</span><span class="sxs-lookup"><span data-stu-id="6b902-132">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="6b902-133">Zadejte číslo do pole Množství.</span><span class="sxs-lookup"><span data-stu-id="6b902-133">In the Quantity field, enter a number.</span></span>
    * <span data-ttu-id="6b902-134">Toto je celkového množství, které podle dohody zakoupíte od dodavatele.</span><span class="sxs-lookup"><span data-stu-id="6b902-134">This is the total quantity that you have agreed to buy from your vendor.</span></span>  
7. <span data-ttu-id="6b902-135">Zadejte číslo do pole Jednotková cena.</span><span class="sxs-lookup"><span data-stu-id="6b902-135">In the Unit price field, enter a number.</span></span>
8. <span data-ttu-id="6b902-136">Rozbalte sekci Podrobnosti řádku.</span><span class="sxs-lookup"><span data-stu-id="6b902-136">Expand the Line details section.</span></span>
9. <span data-ttu-id="6b902-137">Nastavte možnost Max je vynuceno na hodnotu Ano.</span><span class="sxs-lookup"><span data-stu-id="6b902-137">Set the Max is enforced option to Yes.</span></span>
    * <span data-ttu-id="6b902-138">Možnost Max je vynuceno omezuje použití závazku.</span><span class="sxs-lookup"><span data-stu-id="6b902-138">The Max is enforced option limits the use of the commitment.</span></span> <span data-ttu-id="6b902-139">Můžete produkt zakoupit pouze do množství zadaného v poli Množství pro daný řádek.</span><span class="sxs-lookup"><span data-stu-id="6b902-139">You can only purchase up to the quantity that's specified in the Quantity field for the line.</span></span>  
10. <span data-ttu-id="6b902-140">Sbalte oddíl Podrobnosti řádku.</span><span class="sxs-lookup"><span data-stu-id="6b902-140">Collapse the Line details section.</span></span>

## <a name="add-header-conditions"></a><span data-ttu-id="6b902-141">Přidání podmínek záhlaví</span><span class="sxs-lookup"><span data-stu-id="6b902-141">Add header conditions</span></span>
1. <span data-ttu-id="6b902-142">V podokně akcí klikněte na Možnosti.</span><span class="sxs-lookup"><span data-stu-id="6b902-142">On the Action Pane, click Options.</span></span>
2. <span data-ttu-id="6b902-143">Klikněte na tlačítko Změnit zobrazení.</span><span class="sxs-lookup"><span data-stu-id="6b902-143">Click Change view.</span></span>
3. <span data-ttu-id="6b902-144">Klikněte na možnost Zobrazení záhlaví.</span><span class="sxs-lookup"><span data-stu-id="6b902-144">Click Header view.</span></span>
4. <span data-ttu-id="6b902-145">Rozbalte část Podmínky.</span><span class="sxs-lookup"><span data-stu-id="6b902-145">Expand the Terms section.</span></span>
5. <span data-ttu-id="6b902-146">V poli Způsob platby kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.</span><span class="sxs-lookup"><span data-stu-id="6b902-146">In the Method of payment field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="6b902-147">Zde jsou ve výchozím nastavení zobrazené platební podmínky z účtu dodavatele.</span><span class="sxs-lookup"><span data-stu-id="6b902-147">The payment terms from the vendor account are shown here by default.</span></span>       
6. <span data-ttu-id="6b902-148">Vyhledejte na seznamu požadovaný záznam a vyberte ho.</span><span class="sxs-lookup"><span data-stu-id="6b902-148">In the list, find and select the desired record.</span></span>
7. <span data-ttu-id="6b902-149">Klikněte na odkaz na vybraném řádku v seznamu.</span><span class="sxs-lookup"><span data-stu-id="6b902-149">In the list, click the link in the selected row.</span></span>
8. <span data-ttu-id="6b902-150">V poli Způsob dodání kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.</span><span class="sxs-lookup"><span data-stu-id="6b902-150">In the Mode of delivery field, click the drop-down button to open the lookup.</span></span>
9. <span data-ttu-id="6b902-151">Klikněte na odkaz na vybraném řádku v seznamu.</span><span class="sxs-lookup"><span data-stu-id="6b902-151">In the list, click the link in the selected row.</span></span>
10. <span data-ttu-id="6b902-152">V poli Dodací podmínky kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.</span><span class="sxs-lookup"><span data-stu-id="6b902-152">In the Delivery terms field, click the drop-down button to open the lookup.</span></span>
11. <span data-ttu-id="6b902-153">Klikněte na odkaz na vybraném řádku v seznamu.</span><span class="sxs-lookup"><span data-stu-id="6b902-153">In the list, click the link in the selected row.</span></span>

## <a name="confirm-and-activate-the-agreement"></a><span data-ttu-id="6b902-154">Potvrzení a aktivace smlouvy</span><span class="sxs-lookup"><span data-stu-id="6b902-154">Confirm and activate the agreement</span></span>
1. <span data-ttu-id="6b902-155">V podokně akcí klikněte na možnost Nákupní smlouva.</span><span class="sxs-lookup"><span data-stu-id="6b902-155">On the Action Pane, click Purchase agreement.</span></span>
2. <span data-ttu-id="6b902-156">Klikněte na možnost Potvrzení.</span><span class="sxs-lookup"><span data-stu-id="6b902-156">Click Confirmation.</span></span>
    * <span data-ttu-id="6b902-157">Nastavte možnost Označit smlouvu jako platnou na hodnotu Ano.</span><span class="sxs-lookup"><span data-stu-id="6b902-157">Set the Mark agreement as effective option to Yes.</span></span>  
3. <span data-ttu-id="6b902-158">Klepněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="6b902-158">Click OK.</span></span>
4. <span data-ttu-id="6b902-159">V podokně akcí klikněte na možnost Nákupní smlouva.</span><span class="sxs-lookup"><span data-stu-id="6b902-159">On the Action Pane, click Purchase agreement.</span></span>
5. <span data-ttu-id="6b902-160">Klikněte na možnost Potvrzení nákupní smlouvy.</span><span class="sxs-lookup"><span data-stu-id="6b902-160">Click Purchase agreement confirmations.</span></span>
    * <span data-ttu-id="6b902-161">Možnost Náhled/tisk umožňuje generovat dokument pro nákupní smlouvu, který pak můžete vytisknout nebo odeslat dodavateli.</span><span class="sxs-lookup"><span data-stu-id="6b902-161">The Preview/Print option allows you to generate a document for the purchase agreement which you can then print or send to the vendor.</span></span> <span data-ttu-id="6b902-162">Pokud smlouvu aktualizujete a znovu potvrdíte později, zobrazí se zde obě verze.</span><span class="sxs-lookup"><span data-stu-id="6b902-162">If you update the agreement later on and re-confirm it, both versions will be shown here.</span></span>  
6. <span data-ttu-id="6b902-163">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="6b902-163">Close the page.</span></span>


