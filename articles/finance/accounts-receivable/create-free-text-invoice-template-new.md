---
title: Vytvoření šablony volné faktury
description: Tento postup ukazuje, jak vytvořit šablonu volné faktury.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 05/29/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: abdcb307686800e0038212982c1eac6f1c14cf8b
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/15/2021
ms.locfileid: "5217475"
---
# <a name="create-a-free-text-invoice-template"></a><span data-ttu-id="7fe8c-103">Vytvoření šablony volné faktury</span><span class="sxs-lookup"><span data-stu-id="7fe8c-103">Create a free text invoice template</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="7fe8c-104">Pro tuto ukázku použijte ukázkovou společnost USMF.</span><span class="sxs-lookup"><span data-stu-id="7fe8c-104">For this walkthrough, use the USMF demo company.</span></span> <span data-ttu-id="7fe8c-105">Tento postup je určen pro uživatele, který je odpovědný za správu a zpracování faktur pohledávek.</span><span class="sxs-lookup"><span data-stu-id="7fe8c-105">This procedure is intended for the user who is responsible for managing and processing A/R invoices.</span></span>

## <a name="create-a-template"></a><span data-ttu-id="7fe8c-106">Vytvořit šablonu</span><span class="sxs-lookup"><span data-stu-id="7fe8c-106">Create a template</span></span>

1. <span data-ttu-id="7fe8c-107">Přejděte na Pohledávky > Faktury > Opakované faktury > Šablony volných faktur.</span><span class="sxs-lookup"><span data-stu-id="7fe8c-107">Go to Accounts receivable > Invoices > Recurring invoices > Free text invoice templates.</span></span>
    * <span data-ttu-id="7fe8c-108">Tento formulář slouží k vytvoření šablon volné faktury, které mohou zahrnovat řádky faktury, náklady, šablony rozúčtování a informace o účtu hlavní knihy.</span><span class="sxs-lookup"><span data-stu-id="7fe8c-108">Use this form to create free text invoice templates that can include invoice lines, charges, an accounting distribution template, and ledger account information.</span></span>  
2. <span data-ttu-id="7fe8c-109">Klepnutím na položku Nový vytvořte novou volnou šablonu.</span><span class="sxs-lookup"><span data-stu-id="7fe8c-109">Click 'New' to create a new free text invoice template.</span></span>
3. <span data-ttu-id="7fe8c-110">Zadejte hodnotu do pole Název šablony.</span><span class="sxs-lookup"><span data-stu-id="7fe8c-110">In the Template name field, type a value.</span></span>
    * <span data-ttu-id="7fe8c-111">Název šablony jednoznačně identifikuje šablonu volné faktury.</span><span class="sxs-lookup"><span data-stu-id="7fe8c-111">‘Template name’ uniquely identifies a free text invoice template.</span></span> <span data-ttu-id="7fe8c-112">Žádné dvě šablony nemohou mít stejný šablony název.</span><span class="sxs-lookup"><span data-stu-id="7fe8c-112">No two templates can have the same ‘Template name’.</span></span>  
4. <span data-ttu-id="7fe8c-113">Do pole Popis zadejte popis šablony.</span><span class="sxs-lookup"><span data-stu-id="7fe8c-113">In the Description field, enter a description of the template.</span></span>
5. <span data-ttu-id="7fe8c-114">Rozbalte kartu s řádky faktury.</span><span class="sxs-lookup"><span data-stu-id="7fe8c-114">Expand the Invoice lines tab.</span></span>
6. <span data-ttu-id="7fe8c-115">Do pole Popis zadejte popis řádku faktury.</span><span class="sxs-lookup"><span data-stu-id="7fe8c-115">In the Description field, enter a description of the invoice line.</span></span>
7. <span data-ttu-id="7fe8c-116">V poli Hlavní účet vyberte účet výnosů.</span><span class="sxs-lookup"><span data-stu-id="7fe8c-116">In the Main account field, select a revenue account.</span></span>
    * <span data-ttu-id="7fe8c-117">Můžete vybrat účet transakcí pro vyrovnání úvěru odběratele pro celkovou částku faktury na stránce Účetní profily odběratelů.</span><span class="sxs-lookup"><span data-stu-id="7fe8c-117">You can select the offset transaction account of a customer credit for the total invoice amount in the Customer posting profiles page.</span></span>  
8. <span data-ttu-id="7fe8c-118">V poli Skupina prodejní daně kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.</span><span class="sxs-lookup"><span data-stu-id="7fe8c-118">In the Sales tax group field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="7fe8c-119">Skupina DPH pro aktuální řádek faktury, která představuje výchozí skupinu DPH pro účet odběratele.</span><span class="sxs-lookup"><span data-stu-id="7fe8c-119">The sales tax group for the current invoice line is the default sales tax group for the customer account.</span></span>  
9. <span data-ttu-id="7fe8c-120">Klikněte na odkaz na vybraném řádku v seznamu.</span><span class="sxs-lookup"><span data-stu-id="7fe8c-120">In the list, click the link in the selected row.</span></span>
10. <span data-ttu-id="7fe8c-121">V poli Skupina daně položky vyberte skupinu daně DPH položky pro aktuální řádek faktury.</span><span class="sxs-lookup"><span data-stu-id="7fe8c-121">In the Item tax group field, select the item sales tax group for the current invoice line.</span></span>
11. <span data-ttu-id="7fe8c-122">Klikněte na odkaz na vybraném řádku v seznamu.</span><span class="sxs-lookup"><span data-stu-id="7fe8c-122">In the list, click the link in the selected row.</span></span>
12. <span data-ttu-id="7fe8c-123">V poli Jednotka ceny zadejte nebo zobrazte cenu za jednotku pro řádek faktury</span><span class="sxs-lookup"><span data-stu-id="7fe8c-123">In the Unit price field, enter or view the price per unit for the invoice line</span></span>
    * <span data-ttu-id="7fe8c-124">Toto množství je násobeno hodnotou v poli Množství pro určení částky na řádku faktury.</span><span class="sxs-lookup"><span data-stu-id="7fe8c-124">This amount is multiplied by the Quantity field to determine the invoice line amount.</span></span>  
13. <span data-ttu-id="7fe8c-125">Přidejte nový řádek do šablony volné faktury.</span><span class="sxs-lookup"><span data-stu-id="7fe8c-125">Add a new line to free text invoice template.</span></span>
14. <span data-ttu-id="7fe8c-126">Do pole Popis zadejte popis řádku faktury.</span><span class="sxs-lookup"><span data-stu-id="7fe8c-126">In the Description field, enter a description of the invoice line.</span></span>
15. <span data-ttu-id="7fe8c-127">V poli Hlavní účet vyberte účet výnosů.</span><span class="sxs-lookup"><span data-stu-id="7fe8c-127">In the Main account field, select a revenue account.</span></span>
    * <span data-ttu-id="7fe8c-128">Můžete vybrat účet transakcí pro vyrovnání úvěru odběratele pro celkovou částku faktury na stránce Účetní profily odběratelů.</span><span class="sxs-lookup"><span data-stu-id="7fe8c-128">You can select the offset transaction account of a customer credit for the total invoice amount in the Customer posting profiles page.</span></span>  
16. <span data-ttu-id="7fe8c-129">V poli Skupina prodejní daně kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.</span><span class="sxs-lookup"><span data-stu-id="7fe8c-129">In the Sales tax group field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="7fe8c-130">Skupina DPH pro aktuální řádek faktury, která představuje výchozí skupinu DPH pro účet odběratele.</span><span class="sxs-lookup"><span data-stu-id="7fe8c-130">The sales tax group for the current invoice line is the default sales tax group for the customer account.</span></span>  
17. <span data-ttu-id="7fe8c-131">Klikněte na odkaz na vybraném řádku v seznamu.</span><span class="sxs-lookup"><span data-stu-id="7fe8c-131">In the list, click the link in the selected row.</span></span>
18. <span data-ttu-id="7fe8c-132">V poli Skupina DPH zboží kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.</span><span class="sxs-lookup"><span data-stu-id="7fe8c-132">In the Item sales tax group field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="7fe8c-133">Skupina DPH zboží pro aktuální řádek faktury.</span><span class="sxs-lookup"><span data-stu-id="7fe8c-133">The item sales tax group for the current invoice line.</span></span>  
19. <span data-ttu-id="7fe8c-134">Klikněte na odkaz na vybraném řádku v seznamu.</span><span class="sxs-lookup"><span data-stu-id="7fe8c-134">In the list, click the link in the selected row.</span></span>
20. <span data-ttu-id="7fe8c-135">Zadání nebo zobrazení počtu jednotek pro řádek faktury</span><span class="sxs-lookup"><span data-stu-id="7fe8c-135">Enter or view the number of units for the invoice line</span></span>
    * <span data-ttu-id="7fe8c-136">Toto číslo je násobeno hodnotou v poli Jednotková cena pro určení částky na řádku faktury.</span><span class="sxs-lookup"><span data-stu-id="7fe8c-136">This number is multiplied by the value in the Unit price field to determine the invoice line amount.</span></span>  
21. <span data-ttu-id="7fe8c-137">Zadání nebo zobrazení ceny za jednotku pro řádek faktury.</span><span class="sxs-lookup"><span data-stu-id="7fe8c-137">Enter or view the price per unit for the invoice line.</span></span> 
    * <span data-ttu-id="7fe8c-138">Toto množství je násobeno hodnotou v poli Množství pro určení částky na řádku faktury.</span><span class="sxs-lookup"><span data-stu-id="7fe8c-138">This amount is multiplied by the value in the Quantity field to determine the invoice line amount.</span></span>  
22. <span data-ttu-id="7fe8c-139">Zobrazte a upravte rozúčtování pro každý řádek a jakékoli podřízené řádky.</span><span class="sxs-lookup"><span data-stu-id="7fe8c-139">View and modify the accounting distributions for an individual line and any child lines.</span></span>
    * <span data-ttu-id="7fe8c-140">Rozúčtování slouží k definování, jak budou zaúčtovány částky, například jak budou výnosy, daně a náklady zaúčtovány na volných fakturách.</span><span class="sxs-lookup"><span data-stu-id="7fe8c-140">Accounting distributions define how an amount will be accounted for, such as how the revenue, tax, or charges will be accounted for on a free text invoice.</span></span>  
23. <span data-ttu-id="7fe8c-141">Aktualizujte rozúčtování pro vybraný řádek faktury.</span><span class="sxs-lookup"><span data-stu-id="7fe8c-141">Update the accounting distributions for the selected invoice line.</span></span>
24. <span data-ttu-id="7fe8c-142">Klikněte na tlačítko Zavřít.</span><span class="sxs-lookup"><span data-stu-id="7fe8c-142">Click Close.</span></span>

## <a name="save-a-free-text-invoice-as-a-template"></a><span data-ttu-id="7fe8c-143">Uložení volné faktury jako šablony</span><span class="sxs-lookup"><span data-stu-id="7fe8c-143">Save a free text invoice as a template</span></span>
<span data-ttu-id="7fe8c-144">Můžete také uložit existující volnou fakturu jako šablonu.</span><span class="sxs-lookup"><span data-stu-id="7fe8c-144">You can also save an existing free text invoice as a template.</span></span> <span data-ttu-id="7fe8c-145">Když zvolíte na kartě Faktura možnost Uložit jako šablonu, zadejte název a popis šablony.</span><span class="sxs-lookup"><span data-stu-id="7fe8c-145">When you select Save to template from the Invoice tab, provide a name and a description for the template.</span></span> <span data-ttu-id="7fe8c-146">Když šablona s názvem již existuje, zobrazí se upozornění, že šablona s tímto názvem již existuje.</span><span class="sxs-lookup"><span data-stu-id="7fe8c-146">If a template with the name already exists, you will see a notification that a template with that name already exists.</span></span> <span data-ttu-id="7fe8c-147">Můžete ji stále nahradit kliknutím na OK.</span><span class="sxs-lookup"><span data-stu-id="7fe8c-147">You can still click on Ok to replace it.</span></span> 


[!INCLUDE[footer-include](../../includes/footer-banner.md)]