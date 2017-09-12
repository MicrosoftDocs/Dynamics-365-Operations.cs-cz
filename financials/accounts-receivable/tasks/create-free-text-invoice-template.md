--- 
title: "Vytvoření šablony volné faktury"
description: "Tento záznam používá ukázkovou společnost USMF."
author: ShivamPandey-msft
manager: AnnBe
ms.date: 11/11/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Operations
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: e9c9811b348d81cd735c5b75ca48e0a56a8d52be
ms.contentlocale: cs-cz
ms.lasthandoff: 08/29/2017

---
# <a name="create-a-free-text-invoice-template"></a><span data-ttu-id="25084-103">Vytvoření šablony volné faktury</span><span class="sxs-lookup"><span data-stu-id="25084-103">Create a free text invoice template</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="25084-104">Tento záznam používá ukázkovou společnost USMF.</span><span class="sxs-lookup"><span data-stu-id="25084-104">This recording uses the USMF demo company.</span></span> <span data-ttu-id="25084-105">Záznam je určen pro uživatele, který je odpovědný za správu a zpracování faktur pohledávek.</span><span class="sxs-lookup"><span data-stu-id="25084-105">The recording is intended for the user who is responsible for managing and processing A/R invoices.</span></span>

1. <span data-ttu-id="25084-106">Přejděte na Pohledávky > Faktury > Opakované faktury > Šablony volných faktur.</span><span class="sxs-lookup"><span data-stu-id="25084-106">Go to Accounts receivable > Invoices > Recurring invoices > Free text invoice templates.</span></span>
    * <span data-ttu-id="25084-107">Tento formulář slouží k vytvoření šablon volné faktury, které mohou zahrnovat řádky faktury, náklady, šablony rozúčtování a informace o účtu hlavní knihy.</span><span class="sxs-lookup"><span data-stu-id="25084-107">Use this form to create free text invoice templates that can include invoice lines, charges, an accounting distribution template, and ledger account information.</span></span>  
2. <span data-ttu-id="25084-108">Klepnutím na položku Nový vytvořte novou volnou šablonu.</span><span class="sxs-lookup"><span data-stu-id="25084-108">Click 'New' to create a new free text invoice template.</span></span>
3. <span data-ttu-id="25084-109">Zadejte hodnotu do pole Název šablony.</span><span class="sxs-lookup"><span data-stu-id="25084-109">In the Template name field, type a value.</span></span>
    * <span data-ttu-id="25084-110">Název šablony jednoznačně identifikuje šablonu volné faktury.</span><span class="sxs-lookup"><span data-stu-id="25084-110">‘Template name’ uniquely identifies a free text invoice template.</span></span> <span data-ttu-id="25084-111">Žádné dvě šablony nemohou mít stejný šablony název.</span><span class="sxs-lookup"><span data-stu-id="25084-111">No two templates can have the same ‘Template name’.</span></span>  
4. <span data-ttu-id="25084-112">Do pole Popis zadejte popis šablony.</span><span class="sxs-lookup"><span data-stu-id="25084-112">In the Description field, enter a description of the template.</span></span>
5. <span data-ttu-id="25084-113">Rozbalte kartu s řádky faktury.</span><span class="sxs-lookup"><span data-stu-id="25084-113">Expand the Invoice lines tab.</span></span>
6. <span data-ttu-id="25084-114">Do pole Popis zadejte popis řádku faktury.</span><span class="sxs-lookup"><span data-stu-id="25084-114">In the Description field, enter a description of the invoice line.</span></span>
7. <span data-ttu-id="25084-115">V poli Hlavní účet vyberte účet výnosů.</span><span class="sxs-lookup"><span data-stu-id="25084-115">In the Main account field, select a revenue account.</span></span>
    * <span data-ttu-id="25084-116">Můžete vybrat účet transakcí pro vyrovnání úvěru odběratele pro celkovou částku faktury na stránce Účetní profily odběratelů.</span><span class="sxs-lookup"><span data-stu-id="25084-116">You can select the offset transaction account of a customer credit for the total invoice amount in the Customer posting profiles page.</span></span>  
8. <span data-ttu-id="25084-117">V poli Skupina prodejní daně kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.</span><span class="sxs-lookup"><span data-stu-id="25084-117">In the Sales tax group field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="25084-118">Skupina DPH pro aktuální řádek faktury, která představuje výchozí skupinu DPH pro účet odběratele.</span><span class="sxs-lookup"><span data-stu-id="25084-118">The sales tax group for the current invoice line is the default sales tax group for the customer account.</span></span>  
9. <span data-ttu-id="25084-119">Klikněte na odkaz na vybraném řádku v seznamu.</span><span class="sxs-lookup"><span data-stu-id="25084-119">In the list, click the link in the selected row.</span></span>
10. <span data-ttu-id="25084-120">V poli Skupina daně položky vyberte skupinu daně DPH položky pro aktuální řádek faktury.</span><span class="sxs-lookup"><span data-stu-id="25084-120">In the Item tax group field, select the item sales tax group for the current invoice line.</span></span>
11. <span data-ttu-id="25084-121">Klikněte na odkaz na vybraném řádku v seznamu.</span><span class="sxs-lookup"><span data-stu-id="25084-121">In the list, click the link in the selected row.</span></span>
12. <span data-ttu-id="25084-122">V poli Jednotka ceny zadejte nebo zobrazte cenu za jednotku pro řádek faktury</span><span class="sxs-lookup"><span data-stu-id="25084-122">In the Unit price field, enter or view the price per unit for the invoice line</span></span>
    * <span data-ttu-id="25084-123">Toto množství je násobeno hodnotou v poli Množství pro určení částky na řádku faktury.</span><span class="sxs-lookup"><span data-stu-id="25084-123">This amount is multiplied by the Quantity field to determine the invoice line amount.</span></span>  
13. <span data-ttu-id="25084-124">Přidejte nový řádek do šablony volné faktury.</span><span class="sxs-lookup"><span data-stu-id="25084-124">Add a new line to free text invoice template.</span></span>
14. <span data-ttu-id="25084-125">Do pole Popis zadejte popis řádku faktury.</span><span class="sxs-lookup"><span data-stu-id="25084-125">In the Description field, enter a description of the invoice line.</span></span>
15. <span data-ttu-id="25084-126">V poli Hlavní účet vyberte účet výnosů.</span><span class="sxs-lookup"><span data-stu-id="25084-126">In the Main account field, select a revenue account.</span></span>
    * <span data-ttu-id="25084-127">Můžete vybrat účet transakcí pro vyrovnání úvěru odběratele pro celkovou částku faktury na stránce Účetní profily odběratelů.</span><span class="sxs-lookup"><span data-stu-id="25084-127">You can select the offset transaction account of a customer credit for the total invoice amount in the Customer posting profiles page.</span></span>  
16. <span data-ttu-id="25084-128">V poli Skupina prodejní daně kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.</span><span class="sxs-lookup"><span data-stu-id="25084-128">In the Sales tax group field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="25084-129">Skupina DPH pro aktuální řádek faktury, která představuje výchozí skupinu DPH pro účet odběratele.</span><span class="sxs-lookup"><span data-stu-id="25084-129">The sales tax group for the current invoice line is the default sales tax group for the customer account.</span></span>  
17. <span data-ttu-id="25084-130">Klikněte na odkaz na vybraném řádku v seznamu.</span><span class="sxs-lookup"><span data-stu-id="25084-130">In the list, click the link in the selected row.</span></span>
18. <span data-ttu-id="25084-131">V poli Skupina DPH zboží kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.</span><span class="sxs-lookup"><span data-stu-id="25084-131">In the Item sales tax group field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="25084-132">Skupina DPH zboží pro aktuální řádek faktury.</span><span class="sxs-lookup"><span data-stu-id="25084-132">The item sales tax group for the current invoice line.</span></span>  
19. <span data-ttu-id="25084-133">Klikněte na odkaz na vybraném řádku v seznamu.</span><span class="sxs-lookup"><span data-stu-id="25084-133">In the list, click the link in the selected row.</span></span>
20. <span data-ttu-id="25084-134">Zadání nebo zobrazení počtu jednotek pro řádek faktury</span><span class="sxs-lookup"><span data-stu-id="25084-134">Enter or view the number of units for the invoice line</span></span>
    * <span data-ttu-id="25084-135">Toto číslo je násobeno hodnotou v poli Jednotková cena pro určení částky na řádku faktury.</span><span class="sxs-lookup"><span data-stu-id="25084-135">This number is multiplied by the value in the Unit price field to determine the invoice line amount.</span></span>  
21. <span data-ttu-id="25084-136">Zadání nebo zobrazení ceny za jednotku pro řádek faktury.</span><span class="sxs-lookup"><span data-stu-id="25084-136">Enter or view the price per unit for the invoice line.</span></span> 
    * <span data-ttu-id="25084-137">Toto množství je násobeno hodnotou v poli Množství pro určení částky na řádku faktury.</span><span class="sxs-lookup"><span data-stu-id="25084-137">This amount is multiplied by the value in the Quantity field to determine the invoice line amount.</span></span>  
22. <span data-ttu-id="25084-138">Zobrazte a upravte rozúčtování pro každý řádek a jakékoli podřízené řádky.</span><span class="sxs-lookup"><span data-stu-id="25084-138">View and modify the accounting distributions for an individual line and any child lines.</span></span>
    * <span data-ttu-id="25084-139">Rozúčtování slouží k definování, jak budou zaúčtovány částky, například jak budou výnosy, daně a náklady zaúčtovány na volných fakturách.</span><span class="sxs-lookup"><span data-stu-id="25084-139">Accounting distributions define how an amount will be accounted for, such as how the revenue, tax, or charges will be accounted for on a free text invoice.</span></span>  
23. <span data-ttu-id="25084-140">Aktualizujte rozúčtování pro vybraný řádek faktury.</span><span class="sxs-lookup"><span data-stu-id="25084-140">Update the accounting distributions for the selected invoice line.</span></span>
24. <span data-ttu-id="25084-141">Klikněte na tlačítko Zavřít.</span><span class="sxs-lookup"><span data-stu-id="25084-141">Click Close.</span></span>


