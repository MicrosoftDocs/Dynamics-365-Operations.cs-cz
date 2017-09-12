---
title: "Vytvoření faktury odběratele"
description: 
author: ShivamPandey-msft
manager: AnnBe
ms.date: 08/22/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 77772
ms.assetid: 00b4b40c-1576-4098-9aed-ac376fdeb8c5
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 2a668e390935e157d9fc7f0ef597f25c2a7b9950
ms.contentlocale: cs-cz
ms.lasthandoff: 08/29/2017

---

# <a name="create-a-customer-invoice"></a><span data-ttu-id="50a25-102">Vytvoření faktury odběratele</span><span class="sxs-lookup"><span data-stu-id="50a25-102">Create a customer invoice</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="50a25-103">**Faktura odběratele pro prodejní objednávku** je účet, který se vztahuje k prodeji a který organizace předává odběrateli.</span><span class="sxs-lookup"><span data-stu-id="50a25-103">A **customer invoice for a sales order** is a bill that is related to a sale, and that an organization gives to a customer.</span></span> <span data-ttu-id="50a25-104">Tento typ faktury odběratele se vytváří na základě prodejní objednávky, která zahrnuje řádky objednávky a čísla položek.</span><span class="sxs-lookup"><span data-stu-id="50a25-104">This type of customer invoice is created based on a sales order, which includes order lines and item numbers.</span></span> <span data-ttu-id="50a25-105">Čísla položek jsou specifikována a zaúčtována v hlavní knize.</span><span class="sxs-lookup"><span data-stu-id="50a25-105">Item numbers are specified and posted in the ledger.</span></span> <span data-ttu-id="50a25-106">Položky dílčího hlavního deníku nejsou k dispozici pro fakturu odběratele pro prodejní objednávku.</span><span class="sxs-lookup"><span data-stu-id="50a25-106">Subledger journal entries aren't available for a customer invoice for a sales order.</span></span> <span data-ttu-id="50a25-107">Další informace naleznete v tématu [Vytvoření faktur prodejní objednávky](tasks/create-sales-order-invoices.md).</span><span class="sxs-lookup"><span data-stu-id="50a25-107">For more information, see [Create sales order invoices](tasks/create-sales-order-invoices.md).</span></span>

<span data-ttu-id="50a25-108">**Faktura s volným textem** nesouvisí s prodejní objednávkou.</span><span class="sxs-lookup"><span data-stu-id="50a25-108">A **free text invoice** isn't related to a sales order.</span></span> <span data-ttu-id="50a25-109">Obsahuje řádky objednávky zahrnující účty hlavní knihy, textové popisy a vámi zadanou částku prodeje.</span><span class="sxs-lookup"><span data-stu-id="50a25-109">It contains order lines that include ledger accounts, free-text descriptions, and a sales amount that you enter.</span></span> <span data-ttu-id="50a25-110">Číslo položky nelze u tohoto druhu faktury zadat.</span><span class="sxs-lookup"><span data-stu-id="50a25-110">You can't enter an item number on this kind of invoice.</span></span> <span data-ttu-id="50a25-111">Je však nutné zadat příslušné informace o DPH.</span><span class="sxs-lookup"><span data-stu-id="50a25-111">You must enter the appropriate sales tax information.</span></span> <span data-ttu-id="50a25-112">Hlavní účet pro prodej je uveden na každém řádku faktury, který můžete rozdělit do několika účtů hlavní knihy kliknutím na možnost **Distribuovat částky** na stránce **Volná faktura**.</span><span class="sxs-lookup"><span data-stu-id="50a25-112">A main account for the sale is indicated on each invoice line, which you can distribute to multiple ledger accounts by clicking **Distribute amounts** on the **Free text invoice** page.</span></span> <span data-ttu-id="50a25-113">Zůstatek odběratele je navíc zaúčtovány do souhrnného účtu z účetního profil, který se používá pro volnou fakturu.</span><span class="sxs-lookup"><span data-stu-id="50a25-113">Additionally, the customer balance is posted to the summary account from the posting profile that is used for the free text invoice.</span></span>

<span data-ttu-id="50a25-114">Další informace naleznete zde: </span><span class="sxs-lookup"><span data-stu-id="50a25-114">For more information see:</span></span>

[<span data-ttu-id="50a25-115">Vytvoření volné faktury</span><span class="sxs-lookup"><span data-stu-id="50a25-115">Create a free text invoice</span></span>](tasks/create-free-text-invoice.md)

[<span data-ttu-id="50a25-116">Vytvoření volné šablony</span><span class="sxs-lookup"><span data-stu-id="50a25-116">Create a free text template</span></span>](tasks/create-free-text-invoice-template.md)

[<span data-ttu-id="50a25-117">Přiřazení šablony volné faktury odběrateli</span><span class="sxs-lookup"><span data-stu-id="50a25-117">Assign a free text invoice tempate to a customer</span></span>](tasks/assign-free-text-invoice-template-customer.md)

[<span data-ttu-id="50a25-118">Generování a zaúčtování opakovaných volných faktur</span><span class="sxs-lookup"><span data-stu-id="50a25-118">Generate and post recurring free text invoices</span></span>](tasks/post-recurring-free-text-invoices.md)


<span data-ttu-id="50a25-119">**Proforma faktura** je faktura připravená jako odhad skutečných částek faktury před zaúčtováním faktury.</span><span class="sxs-lookup"><span data-stu-id="50a25-119">A **pro forma invoice** is an invoice that is prepared as an estimate of the actual invoice amounts before the invoice is posted.</span></span> <span data-ttu-id="50a25-120">Proforma fakturu lze vytisknout buď pro fakturu odběratele pro prodejní objednávku, nebo pro volnou fakturu.</span><span class="sxs-lookup"><span data-stu-id="50a25-120">You can print a pro forma invoice either for a customer invoice for a sales order or for a free text invoice.</span></span>

## <a name="post-and-print-individual-customer-invoices-that-are-based-on-sales-orders"></a><span data-ttu-id="50a25-121">Zaúčtování a tisk jednotlivých faktur odběratele založených na prodejních objednávkách</span><span class="sxs-lookup"><span data-stu-id="50a25-121">Post and print individual customer invoices that are based on sales orders</span></span>
<span data-ttu-id="50a25-122">Pomocí tohoto procesu můžete vytvořit fakturu založenou na prodejní objednávce.</span><span class="sxs-lookup"><span data-stu-id="50a25-122">Use this process to create an invoice that is based on a sales order.</span></span> <span data-ttu-id="50a25-123">Můžete tak učinit, pokud chcete odeslat fakturu odběrateli před dodáním zboží nebo služeb.</span><span class="sxs-lookup"><span data-stu-id="50a25-123">You might do this if you decide to invoice the customer before you deliver the goods or services.</span></span> 

<span data-ttu-id="50a25-124">Při zaúčtování faktury je množství v poli **Zůstatek faktury** u každé položky aktualizováno celkovým fakturovaným množstvím z vybrané prodejní objednávky.</span><span class="sxs-lookup"><span data-stu-id="50a25-124">When you post an invoice, the **Invoice remainder** quantity for each item is updated with the total of the invoiced quantities from the selected sales order.</span></span> <span data-ttu-id="50a25-125">Pokud bude množství **Zůstatek faktury** i množství **Zbývá dodat** pro všechny položky na prodejní objednávce nulové (0), stav prodejní objednávky se změní na hodnotu **Fakturováno**.</span><span class="sxs-lookup"><span data-stu-id="50a25-125">If both the **Invoice remainder** quantity and the **Deliver remainder** quantity for all items on the sales order are 0 (zero), the status of the sales order is changed to **Invoiced**.</span></span> <span data-ttu-id="50a25-126">Pokud množství v poli **Zůstatek faktury** není nulové (0), stav prodejní objednávky se nezmění a k této objednávce je možné zadat další faktury.</span><span class="sxs-lookup"><span data-stu-id="50a25-126">If the **Invoice remainder** quantity isn't 0 (zero), the status of the sales order remains unchanged, and additional invoices can be entered for it.</span></span>

<span data-ttu-id="50a25-127">Na stránce se seznamem **Všechny prodejní objednávky** si můžete zobrazit stav prodejních objednávek.</span><span class="sxs-lookup"><span data-stu-id="50a25-127">You can view the status of the sales orders on the **All sales orders** list page.</span></span> <span data-ttu-id="50a25-128">Na stránce se seznamem **Otevřené faktury odběratele** si můžete zobrazit faktury, které jste zaúčtovali.</span><span class="sxs-lookup"><span data-stu-id="50a25-128">Use the **Open customer invoices** list page to view the invoices that you posted.</span></span>

## <a name="post-and-print-individual-customer-invoices-that-are-based-on-packing-slips-and-the-date"></a><span data-ttu-id="50a25-129">Zaúčtování a tisk jednotlivých faktur odběratele založených na dodacích listech a datu</span><span class="sxs-lookup"><span data-stu-id="50a25-129">Post and print individual customer invoices that are based on packing slips and the date</span></span>
<span data-ttu-id="50a25-130">Tento proces použijte, když byl pro danou prodejní objednávku zaúčtován alespoň jeden dodací list.</span><span class="sxs-lookup"><span data-stu-id="50a25-130">Use this process when one or more packing slips have been posted for the sales order.</span></span> <span data-ttu-id="50a25-131">Faktura odběratele je založena na těchto dodacích listech a odráží na nich uvedená množství.</span><span class="sxs-lookup"><span data-stu-id="50a25-131">The customer invoice is based on these packing slips and reflects the quantities from them.</span></span> <span data-ttu-id="50a25-132">Finanční údaje pro fakturu jsou založeny na údajích zadaných při zaúčtování faktury.</span><span class="sxs-lookup"><span data-stu-id="50a25-132">The financial information for the invoice is based on the information that is entered when you post the invoice.</span></span> 

<span data-ttu-id="50a25-133">Můžete vytvořit fakturu odběratele založenou na položkách řádku dodacího listu, které byly odeslány k určitému datu, a to i když všechny položky pro určitou prodejní objednávku nebyly dosud odeslány.</span><span class="sxs-lookup"><span data-stu-id="50a25-133">You can create a customer invoice that is based on the packing slip line items that have been shipped to date, even if all the items for a particular sales order haven't yet been shipped.</span></span> <span data-ttu-id="50a25-134">To lze provést například v situaci, kdy daná právnická osoba vystavuje každému odběrateli jednu fakturu měsíčně, která zahrnuje všechny dodávky za daný měsíc.</span><span class="sxs-lookup"><span data-stu-id="50a25-134">You might do this if, for example, your legal entity issues one invoice per customer per month that covers all the deliveries that you ship during that month.</span></span> <span data-ttu-id="50a25-135">Každý dodací list odpovídá částečné nebo úplné dodávce položek na prodejní objednávce.</span><span class="sxs-lookup"><span data-stu-id="50a25-135">Each packing slip represents a partial or complete delivery of the items on the sales order.</span></span> 

<span data-ttu-id="50a25-136">Při zaúčtování faktury bude množství **Zůstatek faktury** pro každou položku aktualizováno o souhrn dodaných množství z vybraných dodacích listů.</span><span class="sxs-lookup"><span data-stu-id="50a25-136">When you post the invoice, the **Invoice remainder** quantity for each item is updated with the total of the delivered quantities from the selected packing slips.</span></span> <span data-ttu-id="50a25-137">Pokud bude množství **Zůstatek faktury** i množství **Zbývá dodat** pro všechny položky na prodejní objednávce nulové (0), stav prodejní objednávky se změní na hodnotu **Fakturováno**.</span><span class="sxs-lookup"><span data-stu-id="50a25-137">If both the **Invoice remainder** quantity and the **Deliver remainder** quantity for all items on the sales order are 0 (zero), the status of the sales order is changed to **Invoiced**.</span></span> <span data-ttu-id="50a25-138">Pokud množství v poli **Zůstatek faktury** není nulové (0), stav prodejní objednávky se nezmění a k této objednávce je možné zadat další faktury.</span><span class="sxs-lookup"><span data-stu-id="50a25-138">If the **Invoice remainder** quantity isn't 0 (zero), the status of the sales order remains unchanged, and additional invoices can be entered for it.</span></span> 

<span data-ttu-id="50a25-139">Skladové transakce budou aktualizovány číslem faktury a stav v poli **Stav řádku** na prodejní objednávce se změní na hodnotu **Fakturováno**.</span><span class="sxs-lookup"><span data-stu-id="50a25-139">Inventory transactions are updated with the invoice number, and the status in the **Line status** field on the sales order is changed to **Invoiced**.</span></span> 

<span data-ttu-id="50a25-140">Na stránce se seznamem **Všechny prodejní objednávky** si můžete zobrazit stav prodejních objednávek.</span><span class="sxs-lookup"><span data-stu-id="50a25-140">View the status of the sales orders in the **All sales orders** list page.</span></span>

## <a name="consolidate-sales-orders-or-packing-slips-for-posting"></a><span data-ttu-id="50a25-141">Konsolidace prodejních objednávek nebo dodacích listů pro zaúčtování</span><span class="sxs-lookup"><span data-stu-id="50a25-141">Consolidate sales orders or packing slips for posting</span></span>
<span data-ttu-id="50a25-142">Tento proces použijte, když jsou některé prodejní objednávky připraveny k fakturaci a vy je chcete sloučit do jedné faktury.</span><span class="sxs-lookup"><span data-stu-id="50a25-142">Use this process when one or more sales orders are ready to be invoiced, and you want to consolidate them into a single invoice.</span></span> 

<span data-ttu-id="50a25-143">Na stránce se seznamem **Prodejní objednávka** můžete vybrat více faktur a poté použít možnost **Generovat faktury** k jejich konsolidaci.</span><span class="sxs-lookup"><span data-stu-id="50a25-143">You can select multiple invoices on the **Sales order** list page and then use **Generate invoices** to consolidate them.</span></span> <span data-ttu-id="50a25-144">Na stránce **Zaúčtování faktury** můžete změnit nastavení položky **Souhrnná objednávka** tak, aby bylo shrnutí provedeno podle čísla objednávky (pokud existuje více dodacích listů pro jednu prodejní objednávku) nebo podle účtu faktury (pokud existuje více prodejních objednávek pro jeden účet faktury).</span><span class="sxs-lookup"><span data-stu-id="50a25-144">On the **Posting invoice** page, you can change the **Summary order** setting to summarize by order number (where there are multiple packing slips for a single sales order) or by invoice account (where there are multiple sales orders for a single invoice account).</span></span> <span data-ttu-id="50a25-145">Tlačítkem **Uspořádat** konsolidujte prodejní objednávky do jedné faktury na základě nastavení v poli **Souhrnná objednávka**.</span><span class="sxs-lookup"><span data-stu-id="50a25-145">Use the **Arrange** button to consolidate sales orders into single invoices, based on the **Summary order** settings.</span></span>

## <a name="additional-settings-that-change-the-posting-behavior"></a><span data-ttu-id="50a25-146">Další nastavení, která mění chování zaúčtování</span><span class="sxs-lookup"><span data-stu-id="50a25-146">Additional settings that change the posting behavior</span></span>
<span data-ttu-id="50a25-147">Následující pole mění chování procesu zaúčtování.</span><span class="sxs-lookup"><span data-stu-id="50a25-147">The following fields change the behavior of the posting process.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="50a25-148">Pole</span><span class="sxs-lookup"><span data-stu-id="50a25-148">Field</span></span></th>
<th><span data-ttu-id="50a25-149">Popis</span><span class="sxs-lookup"><span data-stu-id="50a25-149">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="50a25-150">Množství</span><span class="sxs-lookup"><span data-stu-id="50a25-150">Quantity</span></span></td>
<td><span data-ttu-id="50a25-151">Vyberte množství, na nichž chcete založit zaúčtování dokumentu.</span><span class="sxs-lookup"><span data-stu-id="50a25-151">Select the quantities to base the posting of the document on.</span></span> <span data-ttu-id="50a25-152">Dostupnost různých možností závisí na typu účtovaného dokumentu (například dodací list nebo faktura).</span><span class="sxs-lookup"><span data-stu-id="50a25-152">The options that are available vary, depending on the type of document that you are posting, such as a packing slip or an invoice.</span></span>
<ul>
<li><span data-ttu-id="50a25-153"><strong>Dodat nyní</strong> – výběr všech množství, která jsou zadána v poli <strong>Dodat nyní</strong>.</span><span class="sxs-lookup"><span data-stu-id="50a25-153"><strong>Deliver now</strong> – Select all quantities that are entered in the <strong>Deliver now</strong> field.</span></span> <span data-ttu-id="50a25-154">Tato možnost se používá pro potvrzení nebo dodání částečné objednávky.</span><span class="sxs-lookup"><span data-stu-id="50a25-154">Use this option to confirm or deliver a partial order.</span></span></li>
<li><span data-ttu-id="50a25-155"><strong>Vyskladněno</strong> – výběr všech množství, která byla vyskladněna.</span><span class="sxs-lookup"><span data-stu-id="50a25-155"><strong>Picked</strong> – Select all quantities that have been picked.</span></span></li>
<li><span data-ttu-id="50a25-156"><strong>Vše</strong> – výběr všech množství na prodejních objednávkách, která ještě nebyla aktualizována podle typu aktuálního dokumentu.</span><span class="sxs-lookup"><span data-stu-id="50a25-156"><strong>All</strong> – Select all quantities on the sales order that haven't yet been updated by the current document type.</span></span></li>
<li><span data-ttu-id="50a25-157"><strong>Dodací list</strong> – výběr všech množství, která byla aktualizována podle dodacího listu.</span><span class="sxs-lookup"><span data-stu-id="50a25-157"><strong>Packing slip</strong> – Select all quantities that have been updated by a packing slip.</span></span></li>
<li><span data-ttu-id="50a25-158"><strong>Vybráno množství a neskladované produkty</strong> – výběr všech množství, která byla vyskladněna, a všech množství produktu, která nejsou na skladě.</span><span class="sxs-lookup"><span data-stu-id="50a25-158"><strong>Picked quantity and not stocked products</strong> – Select all quantities that have been picked and all product quantities that aren't stocked.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="50a25-159">Zaúčtování</span><span class="sxs-lookup"><span data-stu-id="50a25-159">Posting</span></span></td>
<td><ul>
<li><span data-ttu-id="50a25-160">Tuto možnost vyberte, chcete-li do deníku zapsat prodejní objednávky.</span><span class="sxs-lookup"><span data-stu-id="50a25-160">Select this option to journalize the sales order.</span></span></li>
<li><span data-ttu-id="50a25-161">Zrušte výběr této možnosti pro tisk proformy prodejní objednávky.</span><span class="sxs-lookup"><span data-stu-id="50a25-161">Clear this option to print a pro forma sales order.</span></span> <span data-ttu-id="50a25-162"><strong>Poznámka:</strong> Pokud jste uzavřeli dohodu o platebním kalendáři, tento platební kalendář se na proforma prodejní objednávce nezobrazí.</span><span class="sxs-lookup"><span data-stu-id="50a25-162"><strong>Note:</strong> If you made an agreement for a payment schedule, the payment schedule isn't shown on the pro forma sales order.</span></span> <span data-ttu-id="50a25-163">Platební kalendáře se zobrazí pouze na aktuálních prodejních objednávkách.</span><span class="sxs-lookup"><span data-stu-id="50a25-163">Payment schedules are shown only on actual sales orders.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="50a25-164">Pozdější výběr</span><span class="sxs-lookup"><span data-stu-id="50a25-164">Late selection</span></span></td>
<td><span data-ttu-id="50a25-165">Výběrem této možnosti použijete vybraný dotaz později.</span><span class="sxs-lookup"><span data-stu-id="50a25-165">Select this option to apply the selected query later.</span></span> <span data-ttu-id="50a25-166">Tato možnost se využívá pro dávkové úlohy.</span><span class="sxs-lookup"><span data-stu-id="50a25-166">This option is used for batch jobs.</span></span> <span data-ttu-id="50a25-167">Dotaz se spustí při spuštění dávkové úlohy.</span><span class="sxs-lookup"><span data-stu-id="50a25-167">The query is run when the batch job is run.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="50a25-168">Snížit množství</span><span class="sxs-lookup"><span data-stu-id="50a25-168">Reduce quantity</span></span></td>
<td><span data-ttu-id="50a25-169">Tuto možnost vyberte, chcete-li automaticky snížit dodané množství při zaúčtování dokumentu tak, aby dodané množství se rovnalo dostupným zásobám.</span><span class="sxs-lookup"><span data-stu-id="50a25-169">Select this option to automatically reduce the delivered quantity when the document is posted, so that the delivered quantity equals the available inventory.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="50a25-170">Tisk</span><span class="sxs-lookup"><span data-stu-id="50a25-170">Print</span></span></td>
<td><span data-ttu-id="50a25-171">Vyberte, kdy chcete tisknout dokumenty:</span><span class="sxs-lookup"><span data-stu-id="50a25-171">Select when to print documents:</span></span>
<ul>
<li><span data-ttu-id="50a25-172"><strong>Aktuální</strong> – tisk dokumentů po aktualizaci každé faktury.</span><span class="sxs-lookup"><span data-stu-id="50a25-172"><strong>Current</strong> – Print documents after each invoice has been updated.</span></span></li>
<li><span data-ttu-id="50a25-173"><strong>Po</strong> – tisk dokumentů po aktualizaci všech faktur.</span><span class="sxs-lookup"><span data-stu-id="50a25-173"><strong>After</strong> – Print documents after all the invoices have been updated.</span></span></li>
</ul><span data-ttu-id="50a25-174">
<strong>Poznámka</strong>: Pole <strong>Tisk</strong> je k dispozici jen tehdy, vyberete-li možnost <strong>Tisk faktury</strong>, <strong>Tisk potvrzení</strong>, <strong>Tisk výdejky</strong> nebo <strong>Tisk dodacího listu</strong>.</span><span class="sxs-lookup"><span data-stu-id="50a25-174">
<strong>Note:</strong> The <strong>Print</strong> field is available only if you select the <strong>Print invoice</strong>, <strong>Print confirmation</strong>, <strong>Print picking list</strong>, or <strong>Print packing slip</strong> option.</span></span> <span data-ttu-id="50a25-175">Na stránce <strong>Třídění formuláře</strong> jste například nastavili, aby systém třídil informace podle účtu faktury.</span><span class="sxs-lookup"><span data-stu-id="50a25-175">For example, on the <strong>Form sorting</strong> page, you have set up the system to sort the information by invoice account.</span></span> <span data-ttu-id="50a25-176">Poté můžete vybrat možnost <strong>Po</strong> a vytisknout dokumenty v dávce seřazené podle účtu faktury.</span><span class="sxs-lookup"><span data-stu-id="50a25-176">You can then select <strong>After</strong> to print the documents in a batch that is sorted by invoice account.</span></span> <span data-ttu-id="50a25-177">V ostatních případech budou dokumenty tištěny před dokončením zpracování a nebudou uspořádány v pořadí, které je zadáno na stránce <strong>Třídění formuláře</strong>.</span><span class="sxs-lookup"><span data-stu-id="50a25-177">Otherwise, the documents are printed before processing is completed, and the documents aren't sorted in the order that is specified on the <strong>Form sorting</strong> page.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="50a25-178">Tisk faktury</span><span class="sxs-lookup"><span data-stu-id="50a25-178">Print invoice</span></span></td>
<td><span data-ttu-id="50a25-179">Volbou této možnosti zapnete tisk faktury.</span><span class="sxs-lookup"><span data-stu-id="50a25-179">Select this option to print the invoice.</span></span> <span data-ttu-id="50a25-180">Pokud je tato možnost vypnuta, můžete zaúčtovat fakturu bez tisku.</span><span class="sxs-lookup"><span data-stu-id="50a25-180">If this option is turned off, you can post an invoice without printing it.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="50a25-181">Odeslat e-mail</span><span class="sxs-lookup"><span data-stu-id="50a25-181">Send e-mail</span></span></td>
<td><span data-ttu-id="50a25-182">Tuto možnost vyberte, pokud chcete faktury pro prodejní objednávku po zaúčtování odeslat odběrateli jako přílohu e-mailu.</span><span class="sxs-lookup"><span data-stu-id="50a25-182">Select this option to send the invoice for a sales order to the customer as an email attachment after the invoice is posted.</span></span> <span data-ttu-id="50a25-183">Přílohy jsou odesílány jako soubory PDF a XML.</span><span class="sxs-lookup"><span data-stu-id="50a25-183">Attachments are sent as PDF and XML files.</span></span> <span data-ttu-id="50a25-184">Tato možnost je k dispozici pouze v případě, že jste na stránce <strong>Parametry elektronických faktur</strong> vybrali možnost <strong>Povolit CFD (elektronické faktury)</strong>.</span><span class="sxs-lookup"><span data-stu-id="50a25-184">This option is available only if you select the <strong>Enable CFD (electronic invoices)</strong> option on the <strong>Electronic invoice parameters</strong> page.</span></span> <span data-ttu-id="50a25-185"><strong>Poznámka:</strong> (MEX) Tento ovládací prvek je k dispozici pouze pro právnické osoby, jejichž primární adresa je v Mexiku.</span><span class="sxs-lookup"><span data-stu-id="50a25-185"><strong>Note:</strong> (MEX) This control is available only to legal entities whose primary address is in Mexico.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="50a25-186">Použít cíl správy tisku</span><span class="sxs-lookup"><span data-stu-id="50a25-186">Use print management destination</span></span></td>
<td><span data-ttu-id="50a25-187">Tuto možnost vyberte, chcete-li použít nastavení tisku zadané na stránce <strong>Nastavení správy tisku</strong> pro transakce, dokument nebo modul.</span><span class="sxs-lookup"><span data-stu-id="50a25-187">Select this option to use the print settings that are specified for the transaction, document, or module on the <strong>Print management setup</strong> page.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="50a25-188">Zkontrolovat limit úvěru</span><span class="sxs-lookup"><span data-stu-id="50a25-188">Check credit limit</span></span></td>
<td><span data-ttu-id="50a25-189">Vyberte informace, které se budou analyzovat při provádění kontroly limitu úvěru.</span><span class="sxs-lookup"><span data-stu-id="50a25-189">Select the information that should be analyzed when a credit limit check is performed.</span></span>
<ul>
<li><span data-ttu-id="50a25-190"><strong>Žádný</strong> – nejsou požadavky na kontrolu limitu úvěru.</span><span class="sxs-lookup"><span data-stu-id="50a25-190"><strong>None</strong> – There is no requirement for the credit limit check.</span></span></li>
<li><span data-ttu-id="50a25-191"><strong>Zůstatek</strong> – limit úvěru se kontroluje vůči zůstatku odběratele.</span><span class="sxs-lookup"><span data-stu-id="50a25-191"><strong>Balance</strong> – The credit limit is checked against the customer balance.</span></span></li>
<li><span data-ttu-id="50a25-192"><strong>Zůstatek + dodací list nebo příjemka produktu</strong> – limit úvěru se kontroluje vůči zůstatku odběratele a dodávkám.</span><span class="sxs-lookup"><span data-stu-id="50a25-192"><strong>Balance + packing slip or product receipt</strong> – The credit limit is checked against the customer balance and deliveries.</span></span></li>
<li><span data-ttu-id="50a25-193"><strong>Zůstatek + vše</strong> – limit úvěru se kontroluje vůči zůstatku odběratele, dodávkám a otevřeným objednávkám.</span><span class="sxs-lookup"><span data-stu-id="50a25-193"><strong>Balance+All</strong> – The credit limit is checked against the customer balance, deliveries, and open orders.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="50a25-194">Úvěrové vyrovnání</span><span class="sxs-lookup"><span data-stu-id="50a25-194">Credit correction</span></span></td>
<td><span data-ttu-id="50a25-195">Chcete-li v transakcích dokladu dobropis zobrazit jako MD, vyberte tuto možnost.</span><span class="sxs-lookup"><span data-stu-id="50a25-195">Select this option to display the credit note as a debit in the voucher transactions.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="50a25-196">Kreditovat zbývající množství</span><span class="sxs-lookup"><span data-stu-id="50a25-196">Credit remaining quantity</span></span></td>
<td><span data-ttu-id="50a25-197">Pokud účtujete dobropis, výběrem této možnosti ponecháte zbývající množství na objednávce.</span><span class="sxs-lookup"><span data-stu-id="50a25-197">If you're posting a credit note, select this option to keep the remaining quantity on order.</span></span> <span data-ttu-id="50a25-198">Pokud je zrušen výběr této možnosti, bude zbývající množství nastaveno na hodnotu 0 (nula).</span><span class="sxs-lookup"><span data-stu-id="50a25-198">If this option is cleared, the remaining quantity is set to 0 (zero).</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="50a25-199">Souhrnná aktualizace pro</span><span class="sxs-lookup"><span data-stu-id="50a25-199">Summary update for</span></span></td>
<td><span data-ttu-id="50a25-200">Vyberte, jak má být shrnuto více prodejních objednávek:</span><span class="sxs-lookup"><span data-stu-id="50a25-200">Select how multiple sales orders should be summarized:</span></span>
<ul>
<li><span data-ttu-id="50a25-201"><strong>Žádný</strong> – nedělat souhrn prodejních objednávek.</span><span class="sxs-lookup"><span data-stu-id="50a25-201"><strong>None</strong> – Don't summarize sales orders.</span></span> <span data-ttu-id="50a25-202">Pro každou prodejní objednávku bude například vytvořena samostatná faktura.</span><span class="sxs-lookup"><span data-stu-id="50a25-202">For example, a separate invoice will be created for each sales order.</span></span></li>
<li><span data-ttu-id="50a25-203"><strong>Účet faktury</strong> – vytvořit souhrn všech vybraných objednávek podle kritérií nastavených na stránce <strong>Parametry souhrnné aktualizace</strong>.</span><span class="sxs-lookup"><span data-stu-id="50a25-203"><strong>Invoice account</strong> – Summarize all selected orders, based on the criteria that are set up on the <strong>Summary update parameters</strong> page.</span></span></li>
<li><span data-ttu-id="50a25-204"><strong>Objednávka</strong> – sumarizovat vybraný rozsah objednávek do jedné objednávky, kterou zadáte.</span><span class="sxs-lookup"><span data-stu-id="50a25-204"><strong>Order</strong> – Summarize a selected range of orders into one order that you specify.</span></span> <span data-ttu-id="50a25-205">Vytvoří se souhrn objednávek podle kritérií nastavených na stránce <strong>Parametry souhrnné aktualizace</strong>.</span><span class="sxs-lookup"><span data-stu-id="50a25-205">The orders are summarized based on the criteria that are set up on the <strong>Summary update parameters</strong> page.</span></span> <span data-ttu-id="50a25-206">Je-li vybrána tato možnost, je nutné vybrat některou možnost v poli <strong>Prodejní objednávka</strong>.</span><span class="sxs-lookup"><span data-stu-id="50a25-206">If you select this option, you must select a value in the <strong>Sales order</strong> field.</span></span></li>
<li><span data-ttu-id="50a25-207"><strong>Automatické shrnutí</strong> – jestliže byly na stránce <strong>Parametry souhrnné aktualizace</strong> určeny všechny souhrnné aktualizace, vytvoří se souhrn všech vybraných objednávek na základě kritérií nastavených na stránce <strong>Parametry souhrnné aktualizace</strong>.</span><span class="sxs-lookup"><span data-stu-id="50a25-207"><strong>Automatic summary</strong> – If summary updates have been specified on the <strong>Summary update</strong> page, summarize all selected orders, based on the criteria that are set up on the <strong>Summary update parameters</strong> page.</span></span> <span data-ttu-id="50a25-208">Pokud nebyly souhrnné aktualizace určeny, objednávka se zaúčtuje samostatně.</span><span class="sxs-lookup"><span data-stu-id="50a25-208">If summary updates haven't been specified, the order is posted separately.</span></span></li>
<li><span data-ttu-id="50a25-209"><strong>Dodací list</strong> – pro každý dodací list se vytvoří souhrn vybraného rozsahu objednávek do jedné faktury.</span><span class="sxs-lookup"><span data-stu-id="50a25-209"><strong>Packing slip</strong> – Summarize a selected range of orders into one invoice for each packing slip.</span></span> <span data-ttu-id="50a25-210">Tato možnost je k dispozici jen tehdy, je-li v poli <strong>Množství</strong> vybrána možnost <strong>Dodací list</strong>.</span><span class="sxs-lookup"><span data-stu-id="50a25-210">This option is available only if <strong>Packing slip</strong> is selected in the <strong>Quantity</strong> field.</span></span></li>
</ul></td>
</tr>
</tbody>
</table>






