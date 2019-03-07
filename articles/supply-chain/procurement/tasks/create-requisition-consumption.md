---
title: Vytvoření žádanky pro spotřebu
description: Tato procedura vás provede procesem vytvoření žádanky.
author: mkirknel
manager: AnnBe
ms.date: 11/03/2017
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: e81ca3966cf7dae88468ccf107b52b8c3d7b323d
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 01/29/2019
ms.locfileid: "366551"
---
# <a name="create-a-requisition-for-consumption"></a><span data-ttu-id="8c140-103">Vytvoření žádanky pro spotřebu</span><span class="sxs-lookup"><span data-stu-id="8c140-103">Create a requisition for consumption</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="8c140-104">Tato procedura vás provede procesem vytvoření žádanky.</span><span class="sxs-lookup"><span data-stu-id="8c140-104">This procedure walks you through the process of creating a requisition.</span></span> <span data-ttu-id="8c140-105">Ukazuje různé způsoby, jak vyhledávat produkty v zásobovacím katalogu a jak přidat produkt, který není ve vašem katalogu.</span><span class="sxs-lookup"><span data-stu-id="8c140-105">It shows you different ways to search for products in your procurement catalog and how to add a product that isn’t in your catalog.</span></span> <span data-ttu-id="8c140-106">Před zahájením tohoto postupu je nutné mít nastavenou zásadu nákupu s výchozím typem žádanky Spotřeba.</span><span class="sxs-lookup"><span data-stu-id="8c140-106">Before you start this procedure, you must have a purchasing policy set up with Consumption as the default type of requisition.</span></span> <span data-ttu-id="8c140-107">Tento proces můžete projít pomocí ukázkových dat společnosti USMF nebo pomocí vlastních dat.</span><span class="sxs-lookup"><span data-stu-id="8c140-107">You can walk through this procedure in demo data company USMF, or using your own data.</span></span> <span data-ttu-id="8c140-108">Postup můžete provést pouze pomocí uživatelského profilu, který je nastavený jako pracovník.</span><span class="sxs-lookup"><span data-stu-id="8c140-108">The procedure can only be carried out by a user profile that is set up as worker.</span></span>  <span data-ttu-id="8c140-109">Tento úkol běžně provádí zaměstnanec.</span><span class="sxs-lookup"><span data-stu-id="8c140-109">This task would normally be carried out by an employee.</span></span> <span data-ttu-id="8c140-110">Role zabezpečení zaměstnance vám umožní provádět úkoly a pokud používáte data USMF, můžete se přihlásit jako Alicia.</span><span class="sxs-lookup"><span data-stu-id="8c140-110">The Employee employ security role will allow you to carry out the tasks, or if you’re using USMF, you can log in as Alicia.</span></span>


## <a name="create-a-new-requisition"></a><span data-ttu-id="8c140-111">Vytvoření nové žádanky</span><span class="sxs-lookup"><span data-stu-id="8c140-111">Create a new requisition</span></span>
1. <span data-ttu-id="8c140-112">Přejděte do nabídky Zásobování a zdroje > Nákupní žádanky > Nákupní žádanky připravené mnou.</span><span class="sxs-lookup"><span data-stu-id="8c140-112">Go to Procurement and sourcing > Purchase requisitions > Purchase requisitions prepared by me.</span></span>
2. <span data-ttu-id="8c140-113">Klikněte na položku Nová.</span><span class="sxs-lookup"><span data-stu-id="8c140-113">Click New.</span></span>
3. <span data-ttu-id="8c140-114">V poli Název zadejte pro žádanku název.</span><span class="sxs-lookup"><span data-stu-id="8c140-114">In the Name field, give the requisition a name.</span></span>
4. <span data-ttu-id="8c140-115">Zadejte datum do pole Požadované datum.</span><span class="sxs-lookup"><span data-stu-id="8c140-115">In the Requested date field, enter a date.</span></span>
    * <span data-ttu-id="8c140-116">Ve výchozím nastavení je požadované datum a datum účtování zkopírováno na řádky nákupních žádanek.</span><span class="sxs-lookup"><span data-stu-id="8c140-116">By default, the requested date and accounting date are copied to the purchase requisition lines.</span></span> <span data-ttu-id="8c140-117">Ty lze měnit na úrovni řádku.</span><span class="sxs-lookup"><span data-stu-id="8c140-117">They can be changed at the line level.</span></span> <span data-ttu-id="8c140-118">Požadované datum představuje požadované datum dodávky.</span><span class="sxs-lookup"><span data-stu-id="8c140-118">The requested date is the requested delivery date.</span></span>  
5. <span data-ttu-id="8c140-119">Zadejte datum do pole Datum účtování.</span><span class="sxs-lookup"><span data-stu-id="8c140-119">In the Accounting date field, enter a date.</span></span>
    * <span data-ttu-id="8c140-120">Účetní datum je použité k záznamu účetní položky v hlavní knize a ověření dostupných rozpočtových prostředků.</span><span class="sxs-lookup"><span data-stu-id="8c140-120">The accounting date is used to record the accounting entry in the general ledger, and to validate whether budget funds are available.</span></span>  
6. <span data-ttu-id="8c140-121">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="8c140-121">Click OK.</span></span>
7. <span data-ttu-id="8c140-122">V poli Důvod kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.</span><span class="sxs-lookup"><span data-stu-id="8c140-122">In the Reason field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="8c140-123">Vybraná obchodní zdůvodnění se ve výchozím nastavení zobrazí na řádcích nákupní žádanky. Podle potřeby je však můžete změnit na úrovni řádku.</span><span class="sxs-lookup"><span data-stu-id="8c140-123">By default, the business justification reason that you select appears for the purchase requisition lines, but you can change it at the line level.</span></span>    
8. <span data-ttu-id="8c140-124">Vyhledejte na seznamu požadovaný záznam a vyberte ho.</span><span class="sxs-lookup"><span data-stu-id="8c140-124">In the list, find and select the desired record.</span></span>
9. <span data-ttu-id="8c140-125">Volba důvodu</span><span class="sxs-lookup"><span data-stu-id="8c140-125">Select the reason</span></span>
10. <span data-ttu-id="8c140-126">V poli Podrobnosti zadejte popisnější odůvodnění žádanky.</span><span class="sxs-lookup"><span data-stu-id="8c140-126">In the details field enter a more descriptive justification for the requisition</span></span>

## <a name="add-a-line-to-the-requisition"></a><span data-ttu-id="8c140-127">Přidání řádku do žádanky</span><span class="sxs-lookup"><span data-stu-id="8c140-127">Add a line to the requisition</span></span>
1. <span data-ttu-id="8c140-128">Klikněte na položku Přidat řádek.</span><span class="sxs-lookup"><span data-stu-id="8c140-128">Click Add line.</span></span>
    * <span data-ttu-id="8c140-129">Existují dva způsoby přidání řádků do nákupní žádanky.</span><span class="sxs-lookup"><span data-stu-id="8c140-129">There are two ways of adding lines to the purchase requisition.</span></span> <span data-ttu-id="8c140-130">Pokud již znáte číslo produktu nebo již víte, že požadujete produkt, který se nenachází v katalogu produktů, přidejte řádek přímo pomocí možnosti „Přidat řádek“.</span><span class="sxs-lookup"><span data-stu-id="8c140-130">If you already know the product number or you already  know that you are requesting a product that is not in the product catalog, then you can add the line directly with "Add line".</span></span> <span data-ttu-id="8c140-131">Můžete také použít možnost „Přidat produkty“ a pomocí vyhledávání a filtrování najít položky v katalogu produktů.</span><span class="sxs-lookup"><span data-stu-id="8c140-131">The other way is to use "Add products" where you can use searching and filtering to find items in the product catalog.</span></span>    
2. <span data-ttu-id="8c140-132">Klikněte na řádek, který jste právě vytvořili.</span><span class="sxs-lookup"><span data-stu-id="8c140-132">Click on the row you just created.</span></span>
    * <span data-ttu-id="8c140-133">Žadatel je pracovník, který vyžaduje žádanku.</span><span class="sxs-lookup"><span data-stu-id="8c140-133">The requester is the worker that has requested the requisition.</span></span>   
    * <span data-ttu-id="8c140-134">Ve výchozím nastavení je osoba připravující žádanku pracovníkem, který odeslal požadavek.</span><span class="sxs-lookup"><span data-stu-id="8c140-134">By default the person preparing the requisition is the worker who has requested it.</span></span> <span data-ttu-id="8c140-135">Musíte mít oprávnění k přípravě řádku žádanky jménem jiného pracovníka.</span><span class="sxs-lookup"><span data-stu-id="8c140-135">You have to be given permission to prepare a requisition line on behalf of another worker.</span></span> <span data-ttu-id="8c140-136">Pokud takové oprávnění máte, v tomto vyhledávání se zobrazí tito ostatní pracovníci.</span><span class="sxs-lookup"><span data-stu-id="8c140-136">If you have such permissions then the other workers will show up in this lookup.</span></span>  
3. <span data-ttu-id="8c140-137">Zadejte hodnotu do pole Číslo zboží.</span><span class="sxs-lookup"><span data-stu-id="8c140-137">In the Item number field, type a value.</span></span>
    * <span data-ttu-id="8c140-138">Položky, které můžete vybrat, jsou omezeny zásadami přístupu ke kategorii a zásobovacím katalogem pro kupující právnickou osobu.</span><span class="sxs-lookup"><span data-stu-id="8c140-138">The items that are available for you to choose are limited by the category access policy and the procurement catalog for the buying legal entity.</span></span>   
4. <span data-ttu-id="8c140-139">Zadejte číslo do pole Množství.</span><span class="sxs-lookup"><span data-stu-id="8c140-139">In the Quantity field, enter a number.</span></span>

## <a name="add-more-products-to-the-requisition"></a><span data-ttu-id="8c140-140">Přidání dalších produktů do žádanky</span><span class="sxs-lookup"><span data-stu-id="8c140-140">Add more products to the requisition</span></span>
1. <span data-ttu-id="8c140-141">Klikněte na možnost Přidat produkty.</span><span class="sxs-lookup"><span data-stu-id="8c140-141">Click Add products.</span></span>
    * <span data-ttu-id="8c140-142">Toto je možnost, kde lze vyhledávat produkty v katalogu produktů.</span><span class="sxs-lookup"><span data-stu-id="8c140-142">This is the option where you can search for products in the product catalog.</span></span>    
2. <span data-ttu-id="8c140-143">V poli Vyhledání uzlu kategorie zásobování zadejte první část názvu kategorie, kterou hledáte, a pak klikněte na Zadat.</span><span class="sxs-lookup"><span data-stu-id="8c140-143">In the Find procurement category node field, type the first part of the name of the category that you are looking for, and then click Enter.</span></span>
    * <span data-ttu-id="8c140-144">Zadejte například počít.</span><span class="sxs-lookup"><span data-stu-id="8c140-144">For example, type comput.</span></span>  
3. <span data-ttu-id="8c140-145">Použijte zástupce InvokeDefaultButton.</span><span class="sxs-lookup"><span data-stu-id="8c140-145">Use the InvokeDefaultButton shortcut.</span></span>
4. <span data-ttu-id="8c140-146">Pomocí filtru filtrujte seznam produktů ve vybrané kategorii.</span><span class="sxs-lookup"><span data-stu-id="8c140-146">Use the Filter to filter the list of products in the selected category.</span></span>
5. <span data-ttu-id="8c140-147">Vyberte kartu produktu, který chcete do žádanky přidat.</span><span class="sxs-lookup"><span data-stu-id="8c140-147">Select the product card that you want to add to the requisition.</span></span>
6. <span data-ttu-id="8c140-148">Klikněte na možnost Přidat na řádky.</span><span class="sxs-lookup"><span data-stu-id="8c140-148">Click Add to lines.</span></span>
7. <span data-ttu-id="8c140-149">Zadejte číslo do pole Množství.</span><span class="sxs-lookup"><span data-stu-id="8c140-149">In the Quantity field, enter a number.</span></span>
8. <span data-ttu-id="8c140-150">V poli Vyhledání uzlu kategorie zásobování zadejte první část názvu kategorie, kterou hledáte, a pak klikněte na Zadat.</span><span class="sxs-lookup"><span data-stu-id="8c140-150">In the Find procurement category node field, type the first part of the name of the category that you are looking for, and then click Enter.</span></span>
    * <span data-ttu-id="8c140-151">Zadejte například zvýraz (zvýrazňovače).</span><span class="sxs-lookup"><span data-stu-id="8c140-151">For example, type High (highlighters).</span></span>  
9. <span data-ttu-id="8c140-152">Použijte zástupce InvokeDefaultButton.</span><span class="sxs-lookup"><span data-stu-id="8c140-152">Use the InvokeDefaultButton shortcut.</span></span>
10. <span data-ttu-id="8c140-153">Klikněte na možnost Přidat neuvedené produkty na řádky, chcete-li přidat produkt neuvedený v zásobovacím katalogu.</span><span class="sxs-lookup"><span data-stu-id="8c140-153">Click Add unlisted product to lines to add a product that’s not listed in the procurement catalog.</span></span>
11. <span data-ttu-id="8c140-154">Do pole Název produktu zadejte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="8c140-154">In the Product name field, type a value.</span></span>
12. <span data-ttu-id="8c140-155">Zadejte hodnotu do pole Jednotka.</span><span class="sxs-lookup"><span data-stu-id="8c140-155">In the Unit field, type a value.</span></span>
13. <span data-ttu-id="8c140-156">Klepněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="8c140-156">Click OK.</span></span>
14. <span data-ttu-id="8c140-157">Do pole Popis položky zadejte popis produktu.</span><span class="sxs-lookup"><span data-stu-id="8c140-157">In the Item description field, add a description of the product.</span></span>
15. <span data-ttu-id="8c140-158">Zadejte číslo do pole Množství.</span><span class="sxs-lookup"><span data-stu-id="8c140-158">In the Quantity field, enter a number.</span></span>
16. <span data-ttu-id="8c140-159">Zadejte číslo do pole Jednotková cena.</span><span class="sxs-lookup"><span data-stu-id="8c140-159">In the Unit price field, enter a number.</span></span>
    * <span data-ttu-id="8c140-160">Pokud víte cenu pro určitého dodavatele (vybraného v poli Účet dodavatele), můžete cenu zadat.</span><span class="sxs-lookup"><span data-stu-id="8c140-160">If you know the price for a particular vendor (that you select in the vendor account field) then that price can be entered</span></span>   
17. <span data-ttu-id="8c140-161">V poli Účet dodavatele kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.</span><span class="sxs-lookup"><span data-stu-id="8c140-161">In the Vendor account field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="8c140-162">Dodavatelé, kteří jsou k dispozici v tomto poli, závisí na zásadách nákupu a stavu dodavatele pro aktuální kategorii zásobování.</span><span class="sxs-lookup"><span data-stu-id="8c140-162">The vendors that are available in this field depend on the purchasing policies and the status that the vendor has for the current procurement category.</span></span> <span data-ttu-id="8c140-163">Místo volby dodavatele v tomto poli můžete kliknout na tlačítko Navrhnout dodavatele.</span><span class="sxs-lookup"><span data-stu-id="8c140-163">As an alternative to selecting a vendor here, you can click the Suggest vendor button.</span></span>    
18. <span data-ttu-id="8c140-164">Ze seznamu vyberte dodavatele, kterého chcete použít.</span><span class="sxs-lookup"><span data-stu-id="8c140-164">In the list, select the vendor you want to use.</span></span>
19. <span data-ttu-id="8c140-165">Zadejte hodnotu do pole Externí číslo položky.</span><span class="sxs-lookup"><span data-stu-id="8c140-165">In the External item number field, type a value.</span></span>
    * <span data-ttu-id="8c140-166">Toto je referenční číslo produktu, který dodavatel zná.</span><span class="sxs-lookup"><span data-stu-id="8c140-166">This is a reference number for the product that is known by the vendor.</span></span> <span data-ttu-id="8c140-167">Například se může jednat o čísla položky produktu ve vlastním katalogu dodavatele.</span><span class="sxs-lookup"><span data-stu-id="8c140-167">For example, this could be the item number of the product in the vendor's own catalog.</span></span>  
20. <span data-ttu-id="8c140-168">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="8c140-168">Click OK.</span></span>

## <a name="distribute-amounts"></a><span data-ttu-id="8c140-169">Distribuovat částky</span><span class="sxs-lookup"><span data-stu-id="8c140-169">Distribute amounts</span></span>
1. <span data-ttu-id="8c140-170">Klepněte na tlačítko Finanční údaje.</span><span class="sxs-lookup"><span data-stu-id="8c140-170">Click Financials.</span></span>
2. <span data-ttu-id="8c140-171">Klikněte na možnost Distribuovat částky.</span><span class="sxs-lookup"><span data-stu-id="8c140-171">Click Distribute amounts.</span></span>
    * <span data-ttu-id="8c140-172">Tento proces ukazuje, jak rozdělit náklady pro první řádek mezi 2 účty.</span><span class="sxs-lookup"><span data-stu-id="8c140-172">This process shows you how to distribute the cost for the first line between 2 accounts.</span></span> <span data-ttu-id="8c140-173">To lze také provést později, když je požadavek ve stavu kontroly.</span><span class="sxs-lookup"><span data-stu-id="8c140-173">This can also be done later when the requisition is in review.</span></span>  
3. <span data-ttu-id="8c140-174">Kliknutím na Rozdělit vytvořte nový řádek distribuce.</span><span class="sxs-lookup"><span data-stu-id="8c140-174">Click Split to create a new distribution line.</span></span>
4. <span data-ttu-id="8c140-175">V poli Účet hlavní knihy vyberte první nákladové středisko, kde má být provedena část nákladů.</span><span class="sxs-lookup"><span data-stu-id="8c140-175">In the Ledger account field select the first cost center that should take part of the cost.</span></span>
5. <span data-ttu-id="8c140-176">Vyberte druhý řádek distribuce.</span><span class="sxs-lookup"><span data-stu-id="8c140-176">Select the other distribution line.</span></span>
6. <span data-ttu-id="8c140-177">Do pole Účet hlavní knihy zadejte druhé nákladové středisko.</span><span class="sxs-lookup"><span data-stu-id="8c140-177">In the Ledger account field specify the other cost center.</span></span>
7. <span data-ttu-id="8c140-178">Klikněte na možnost Distribuovat rovnoměrně.</span><span class="sxs-lookup"><span data-stu-id="8c140-178">Click Distribute equally.</span></span>
8. <span data-ttu-id="8c140-179">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="8c140-179">Close the page.</span></span>

## <a name="view-line-details"></a><span data-ttu-id="8c140-180">Zobrazit podrobnosti řádku</span><span class="sxs-lookup"><span data-stu-id="8c140-180">View line details</span></span>
1. <span data-ttu-id="8c140-181">Přepněte rozšíření oddílu Podrobnosti řádku.</span><span class="sxs-lookup"><span data-stu-id="8c140-181">Toggle the expansion of the Line details section.</span></span>

## <a name="submit-the-requisition"></a><span data-ttu-id="8c140-182">Odeslání žádanky</span><span class="sxs-lookup"><span data-stu-id="8c140-182">Submit the requisition</span></span>
1. <span data-ttu-id="8c140-183">Kliknutím na možnost Workflow otevřete dialogové okno.</span><span class="sxs-lookup"><span data-stu-id="8c140-183">Click Workflow to open the drop dialog.</span></span>
2. <span data-ttu-id="8c140-184">Klepněte na tlačítko Odeslat.</span><span class="sxs-lookup"><span data-stu-id="8c140-184">Click Submit.</span></span>
3. <span data-ttu-id="8c140-185">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="8c140-185">Close the page.</span></span>
4. <span data-ttu-id="8c140-186">Do pole Komentář zadejte poznámky pro schvalovatele žádanky.</span><span class="sxs-lookup"><span data-stu-id="8c140-186">In the Comment field, type a note for the approver of the requisition.</span></span>
5. <span data-ttu-id="8c140-187">Klepněte na tlačítko Odeslat.</span><span class="sxs-lookup"><span data-stu-id="8c140-187">Click Submit.</span></span>
6. <span data-ttu-id="8c140-188">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="8c140-188">Close the page.</span></span>
7. <span data-ttu-id="8c140-189">Aktualizujte stránku.</span><span class="sxs-lookup"><span data-stu-id="8c140-189">Refresh the page.</span></span>

