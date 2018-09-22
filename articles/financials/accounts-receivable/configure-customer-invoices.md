---
title: "Vytvoření faktury odběratele"
description: "**Faktura odběratele pro prodejní objednávku** je účet, který se vztahuje k prodeji a který organizace předává odběrateli."
author: ShivamPandey-msft
manager: AnnBe
ms.date: 01/12/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: CustFreeInvoice
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 77772
ms.assetid: 00b4b40c-1576-4098-9aed-ac376fdeb8c5
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 4f4cb254ad2d4328e146f5dba471aafb21660986
ms.openlocfilehash: 6d7c9a61f935503b74ac27b354c875df095d84b4
ms.contentlocale: cs-cz
ms.lasthandoff: 08/14/2018

---

# <a name="create-a-customer-invoice"></a><span data-ttu-id="73ff9-103">Vytvoření faktury odběratele</span><span class="sxs-lookup"><span data-stu-id="73ff9-103">Create a customer invoice</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="73ff9-104">**Faktura odběratele pro prodejní objednávku** je účet, který se vztahuje k prodeji a který organizace předává odběrateli.</span><span class="sxs-lookup"><span data-stu-id="73ff9-104">A **customer invoice for a sales order** is a bill that is related to a sale, and that an organization gives to a customer.</span></span> <span data-ttu-id="73ff9-105">Tento typ faktury odběratele se vytváří na základě prodejní objednávky, která zahrnuje řádky objednávky a čísla položek.</span><span class="sxs-lookup"><span data-stu-id="73ff9-105">This type of customer invoice is created based on a sales order, which includes order lines and item numbers.</span></span> <span data-ttu-id="73ff9-106">Čísla položek jsou specifikována a zaúčtována v hlavní knize.</span><span class="sxs-lookup"><span data-stu-id="73ff9-106">Item numbers are specified and posted in the ledger.</span></span> <span data-ttu-id="73ff9-107">Položky dílčího hlavního deníku nejsou k dispozici pro fakturu odběratele pro prodejní objednávku.</span><span class="sxs-lookup"><span data-stu-id="73ff9-107">Subledger journal entries aren't available for a customer invoice for a sales order.</span></span> <span data-ttu-id="73ff9-108">Další informace naleznete v tématu [Vytvoření faktur prodejní objednávky](tasks/create-sales-order-invoices.md).</span><span class="sxs-lookup"><span data-stu-id="73ff9-108">For more information, see [Create sales order invoices](tasks/create-sales-order-invoices.md).</span></span>

<span data-ttu-id="73ff9-109">**Faktura s volným textem** nesouvisí s prodejní objednávkou.</span><span class="sxs-lookup"><span data-stu-id="73ff9-109">A **free text invoice** isn't related to a sales order.</span></span> <span data-ttu-id="73ff9-110">Obsahuje řádky objednávky zahrnující účty hlavní knihy, textové popisy a vámi zadanou částku prodeje.</span><span class="sxs-lookup"><span data-stu-id="73ff9-110">It contains order lines that include ledger accounts, free-text descriptions, and a sales amount that you enter.</span></span> <span data-ttu-id="73ff9-111">Číslo položky nelze u tohoto druhu faktury zadat.</span><span class="sxs-lookup"><span data-stu-id="73ff9-111">You can't enter an item number on this kind of invoice.</span></span> <span data-ttu-id="73ff9-112">Je však nutné zadat příslušné informace o DPH.</span><span class="sxs-lookup"><span data-stu-id="73ff9-112">You must enter the appropriate sales tax information.</span></span> <span data-ttu-id="73ff9-113">Hlavní účet pro prodej je uveden na každém řádku faktury, který můžete rozdělit do několika účtů hlavní knihy kliknutím na možnost **Distribuovat částky** na stránce **Volná faktura**.</span><span class="sxs-lookup"><span data-stu-id="73ff9-113">A main account for the sale is indicated on each invoice line, which you can distribute to multiple ledger accounts by clicking **Distribute amounts** on the **Free text invoice** page.</span></span> <span data-ttu-id="73ff9-114">Zůstatek odběratele je navíc zaúčtovány do souhrnného účtu z účetního profil, který se používá pro volnou fakturu.</span><span class="sxs-lookup"><span data-stu-id="73ff9-114">Additionally, the customer balance is posted to the summary account from the posting profile that is used for the free text invoice.</span></span>

<span data-ttu-id="73ff9-115">Další informace naleznete zde: </span><span class="sxs-lookup"><span data-stu-id="73ff9-115">For more information see:</span></span>

[<span data-ttu-id="73ff9-116">Vytvoření volné faktury</span><span class="sxs-lookup"><span data-stu-id="73ff9-116">Create a free text invoice</span></span>](../accounts-receivable/create-free-text-invoice-new.md)

[<span data-ttu-id="73ff9-117">Vytvoření volné šablony</span><span class="sxs-lookup"><span data-stu-id="73ff9-117">Create a free text template</span></span>](../accounts-receivable/create-free-text-invoice-template-new.md)

[<span data-ttu-id="73ff9-118">Přiřazení šablony volné faktury odběrateli</span><span class="sxs-lookup"><span data-stu-id="73ff9-118">Assign a free text invoice template to a customer</span></span>](tasks/assign-free-text-invoice-template-customer.md)

[<span data-ttu-id="73ff9-119">Generování a zaúčtování opakovaných volných faktur</span><span class="sxs-lookup"><span data-stu-id="73ff9-119">Generate and post recurring free text invoices</span></span>](tasks/post-recurring-free-text-invoices.md)


<span data-ttu-id="73ff9-120">**Proforma faktura** je faktura připravená jako odhad skutečných částek faktury před zaúčtováním faktury.</span><span class="sxs-lookup"><span data-stu-id="73ff9-120">A **pro forma invoice** is an invoice that is prepared as an estimate of the actual invoice amounts before the invoice is posted.</span></span> <span data-ttu-id="73ff9-121">Proforma fakturu lze vytisknout buď pro fakturu odběratele pro prodejní objednávku, nebo pro volnou fakturu.</span><span class="sxs-lookup"><span data-stu-id="73ff9-121">You can print a pro forma invoice either for a customer invoice for a sales order or for a free text invoice.</span></span>

## <a name="post-and-print-individual-customer-invoices-that-are-based-on-sales-orders"></a><span data-ttu-id="73ff9-122">Zaúčtování a tisk jednotlivých faktur odběratele založených na prodejních objednávkách</span><span class="sxs-lookup"><span data-stu-id="73ff9-122">Post and print individual customer invoices that are based on sales orders</span></span>
<span data-ttu-id="73ff9-123">Pomocí tohoto procesu můžete vytvořit fakturu založenou na prodejní objednávce.</span><span class="sxs-lookup"><span data-stu-id="73ff9-123">Use this process to create an invoice that is based on a sales order.</span></span> <span data-ttu-id="73ff9-124">Můžete tak učinit, pokud chcete odeslat fakturu odběrateli před dodáním zboží nebo služeb.</span><span class="sxs-lookup"><span data-stu-id="73ff9-124">You might do this if you decide to invoice the customer before you deliver the goods or services.</span></span> 

<span data-ttu-id="73ff9-125">Při zaúčtování faktury je množství v poli **Zůstatek faktury** u každé položky aktualizováno celkovým fakturovaným množstvím z vybrané prodejní objednávky.</span><span class="sxs-lookup"><span data-stu-id="73ff9-125">When you post an invoice, the **Invoice remainder** quantity for each item is updated with the total of the invoiced quantities from the selected sales order.</span></span> <span data-ttu-id="73ff9-126">Pokud bude množství **Zůstatek faktury** i množství **Zbývá dodat** pro všechny položky na prodejní objednávce nulové (0), stav prodejní objednávky se změní na hodnotu **Fakturováno**.</span><span class="sxs-lookup"><span data-stu-id="73ff9-126">If both the **Invoice remainder** quantity and the **Deliver remainder** quantity for all items on the sales order are 0 (zero), the status of the sales order is changed to **Invoiced**.</span></span> <span data-ttu-id="73ff9-127">Pokud množství v poli **Zůstatek faktury** není nulové (0), stav prodejní objednávky se nezmění a k této objednávce je možné zadat další faktury.</span><span class="sxs-lookup"><span data-stu-id="73ff9-127">If the **Invoice remainder** quantity isn't 0 (zero), the status of the sales order remains unchanged, and additional invoices can be entered for it.</span></span>

<span data-ttu-id="73ff9-128">Na stránce se seznamem **Všechny prodejní objednávky** si můžete zobrazit stav prodejních objednávek.</span><span class="sxs-lookup"><span data-stu-id="73ff9-128">You can view the status of the sales orders on the **All sales orders** list page.</span></span> <span data-ttu-id="73ff9-129">Na stránce se seznamem **Otevřené faktury odběratele** si můžete zobrazit faktury, které jste zaúčtovali.</span><span class="sxs-lookup"><span data-stu-id="73ff9-129">Use the **Open customer invoices** list page to view the invoices that you posted.</span></span>

## <a name="post-and-print-individual-customer-invoices-that-are-based-on-packing-slips-and-the-date"></a><span data-ttu-id="73ff9-130">Zaúčtování a tisk jednotlivých faktur odběratele založených na dodacích listech a datu</span><span class="sxs-lookup"><span data-stu-id="73ff9-130">Post and print individual customer invoices that are based on packing slips and the date</span></span>
<span data-ttu-id="73ff9-131">Tento proces použijte, když byl pro danou prodejní objednávku zaúčtován alespoň jeden dodací list.</span><span class="sxs-lookup"><span data-stu-id="73ff9-131">Use this process when one or more packing slips have been posted for the sales order.</span></span> <span data-ttu-id="73ff9-132">Faktura odběratele je založena na těchto dodacích listech a odráží na nich uvedená množství.</span><span class="sxs-lookup"><span data-stu-id="73ff9-132">The customer invoice is based on these packing slips and reflects the quantities from them.</span></span> <span data-ttu-id="73ff9-133">Finanční údaje pro fakturu jsou založeny na údajích zadaných při zaúčtování faktury.</span><span class="sxs-lookup"><span data-stu-id="73ff9-133">The financial information for the invoice is based on the information that is entered when you post the invoice.</span></span> 

<span data-ttu-id="73ff9-134">Můžete vytvořit fakturu odběratele založenou na položkách řádku dodacího listu, které byly odeslány k určitému datu, a to i když všechny položky pro určitou prodejní objednávku nebyly dosud odeslány.</span><span class="sxs-lookup"><span data-stu-id="73ff9-134">You can create a customer invoice that is based on the packing slip line items that have been shipped to date, even if all the items for a particular sales order haven't yet been shipped.</span></span> <span data-ttu-id="73ff9-135">To lze provést například v situaci, kdy daná právnická osoba vystavuje každému odběrateli jednu fakturu měsíčně, která zahrnuje všechny dodávky za daný měsíc.</span><span class="sxs-lookup"><span data-stu-id="73ff9-135">You might do this if, for example, your legal entity issues one invoice per customer per month that covers all the deliveries that you ship during that month.</span></span> <span data-ttu-id="73ff9-136">Každý dodací list odpovídá částečné nebo úplné dodávce položek na prodejní objednávce.</span><span class="sxs-lookup"><span data-stu-id="73ff9-136">Each packing slip represents a partial or complete delivery of the items on the sales order.</span></span> 

<span data-ttu-id="73ff9-137">Při zaúčtování faktury bude množství **Zůstatek faktury** pro každou položku aktualizováno o souhrn dodaných množství z vybraných dodacích listů.</span><span class="sxs-lookup"><span data-stu-id="73ff9-137">When you post the invoice, the **Invoice remainder** quantity for each item is updated with the total of the delivered quantities from the selected packing slips.</span></span> <span data-ttu-id="73ff9-138">Pokud bude množství **Zůstatek faktury** i množství **Zbývá dodat** pro všechny položky na prodejní objednávce nulové (0), stav prodejní objednávky se změní na hodnotu **Fakturováno**.</span><span class="sxs-lookup"><span data-stu-id="73ff9-138">If both the **Invoice remainder** quantity and the **Deliver remainder** quantity for all items on the sales order are 0 (zero), the status of the sales order is changed to **Invoiced**.</span></span> <span data-ttu-id="73ff9-139">Pokud množství v poli **Zůstatek faktury** není nulové (0), stav prodejní objednávky se nezmění a k této objednávce je možné zadat další faktury.</span><span class="sxs-lookup"><span data-stu-id="73ff9-139">If the **Invoice remainder** quantity isn't 0 (zero), the status of the sales order remains unchanged, and additional invoices can be entered for it.</span></span> 

<span data-ttu-id="73ff9-140">Skladové transakce budou aktualizovány číslem faktury a stav v poli **Stav řádku** na prodejní objednávce se změní na hodnotu **Fakturováno**.</span><span class="sxs-lookup"><span data-stu-id="73ff9-140">Inventory transactions are updated with the invoice number, and the status in the **Line status** field on the sales order is changed to **Invoiced**.</span></span> 

<span data-ttu-id="73ff9-141">Na stránce se seznamem **Všechny prodejní objednávky** si můžete zobrazit stav prodejních objednávek.</span><span class="sxs-lookup"><span data-stu-id="73ff9-141">View the status of the sales orders in the **All sales orders** list page.</span></span>

## <a name="consolidate-sales-orders-or-packing-slips-for-posting"></a><span data-ttu-id="73ff9-142">Konsolidace prodejních objednávek nebo dodacích listů pro zaúčtování</span><span class="sxs-lookup"><span data-stu-id="73ff9-142">Consolidate sales orders or packing slips for posting</span></span>
<span data-ttu-id="73ff9-143">Tento proces použijte, když jsou některé prodejní objednávky připraveny k fakturaci a vy je chcete sloučit do jedné faktury.</span><span class="sxs-lookup"><span data-stu-id="73ff9-143">Use this process when one or more sales orders are ready to be invoiced, and you want to consolidate them into a single invoice.</span></span> 

<span data-ttu-id="73ff9-144">Na stránce se seznamem **Prodejní objednávka** můžete vybrat více faktur a poté použít možnost **Generovat faktury** k jejich konsolidaci.</span><span class="sxs-lookup"><span data-stu-id="73ff9-144">You can select multiple invoices on the **Sales order** list page and then use **Generate invoices** to consolidate them.</span></span> <span data-ttu-id="73ff9-145">Na stránce **Zaúčtování faktury** můžete změnit nastavení položky **Souhrnná objednávka** tak, aby bylo shrnutí provedeno podle čísla objednávky (pokud existuje více dodacích listů pro jednu prodejní objednávku) nebo podle účtu faktury (pokud existuje více prodejních objednávek pro jeden účet faktury).</span><span class="sxs-lookup"><span data-stu-id="73ff9-145">On the **Posting invoice** page, you can change the **Summary order** setting to summarize by order number (where there are multiple packing slips for a single sales order) or by invoice account (where there are multiple sales orders for a single invoice account).</span></span> <span data-ttu-id="73ff9-146">Tlačítkem **Uspořádat** konsolidujte prodejní objednávky do jedné faktury na základě nastavení v poli **Souhrnná objednávka**.</span><span class="sxs-lookup"><span data-stu-id="73ff9-146">Use the **Arrange** button to consolidate sales orders into single invoices, based on the **Summary order** settings.</span></span>

## <a name="additional-settings-that-change-the-posting-behavior"></a><span data-ttu-id="73ff9-147">Další nastavení, která mění chování zaúčtování</span><span class="sxs-lookup"><span data-stu-id="73ff9-147">Additional settings that change the posting behavior</span></span>
<span data-ttu-id="73ff9-148">Následující pole mění chování procesu zaúčtování.</span><span class="sxs-lookup"><span data-stu-id="73ff9-148">The following fields change the behavior of the posting process.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="73ff9-149">Pole</span><span class="sxs-lookup"><span data-stu-id="73ff9-149">Field</span></span></th>
<th><span data-ttu-id="73ff9-150">Popis</span><span class="sxs-lookup"><span data-stu-id="73ff9-150">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="73ff9-151">Množství</span><span class="sxs-lookup"><span data-stu-id="73ff9-151">Quantity</span></span></td>
<td><span data-ttu-id="73ff9-152">Vyberte množství, na nichž chcete založit zaúčtování dokumentu.</span><span class="sxs-lookup"><span data-stu-id="73ff9-152">Select the quantities to base the posting of the document on.</span></span> <span data-ttu-id="73ff9-153">Dostupnost různých možností závisí na typu účtovaného dokumentu (například dodací list nebo faktura).</span><span class="sxs-lookup"><span data-stu-id="73ff9-153">The options that are available vary, depending on the type of document that you are posting, such as a packing slip or an invoice.</span></span>
<ul>
<li><span data-ttu-id="73ff9-154"><strong>Dodat nyní</strong> – výběr všech množství, která jsou zadána v poli <strong>Dodat nyní</strong>.</span><span class="sxs-lookup"><span data-stu-id="73ff9-154"><strong>Deliver now</strong> – Select all quantities that are entered in the <strong>Deliver now</strong> field.</span></span> <span data-ttu-id="73ff9-155">Tato možnost se používá pro potvrzení nebo dodání částečné objednávky.</span><span class="sxs-lookup"><span data-stu-id="73ff9-155">Use this option to confirm or deliver a partial order.</span></span></li>
<li><span data-ttu-id="73ff9-156"><strong>Vyskladněno</strong> – výběr všech množství, která byla vyskladněna.</span><span class="sxs-lookup"><span data-stu-id="73ff9-156"><strong>Picked</strong> – Select all quantities that have been picked.</span></span></li>
<li><span data-ttu-id="73ff9-157"><strong>Vše</strong> – výběr všech množství na prodejních objednávkách, která ještě nebyla aktualizována podle typu aktuálního dokumentu.</span><span class="sxs-lookup"><span data-stu-id="73ff9-157"><strong>All</strong> – Select all quantities on the sales order that haven&#39;t yet been updated by the current document type.</span></span></li>
<li><span data-ttu-id="73ff9-158"><strong>Dodací list</strong> – výběr všech množství, která byla aktualizována podle dodacího listu.</span><span class="sxs-lookup"><span data-stu-id="73ff9-158"><strong>Packing slip</strong> – Select all quantities that have been updated by a packing slip.</span></span></li>
<li><span data-ttu-id="73ff9-159"><strong>Vybráno množství a neskladované produkty</strong> – výběr všech množství, která byla vyskladněna, a všech množství produktu, která nejsou na skladě.</span><span class="sxs-lookup"><span data-stu-id="73ff9-159"><strong>Picked quantity and not stocked products</strong> – Select all quantities that have been picked and all product quantities that aren&#39;t stocked.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="73ff9-160">Zaúčtování</span><span class="sxs-lookup"><span data-stu-id="73ff9-160">Posting</span></span></td>
<td><ul>
<li><span data-ttu-id="73ff9-161">Tuto možnost vyberte, chcete-li do deníku zapsat prodejní objednávky.</span><span class="sxs-lookup"><span data-stu-id="73ff9-161">Select this option to journalize the sales order.</span></span></li>
<li><span data-ttu-id="73ff9-162">Zrušte výběr této možnosti pro tisk proformy prodejní objednávky.</span><span class="sxs-lookup"><span data-stu-id="73ff9-162">Clear this option to print a pro forma sales order.</span></span> <span data-ttu-id="73ff9-163"><strong>Poznámka:</strong> Pokud jste uzavřeli dohodu o platebním kalendáři, tento platební kalendář se na proforma prodejní objednávce nezobrazí.</span><span class="sxs-lookup"><span data-stu-id="73ff9-163"><strong>Note:</strong> If you made an agreement for a payment schedule, the payment schedule isn&#39;t shown on the pro forma sales order.</span></span> <span data-ttu-id="73ff9-164">Platební kalendáře se zobrazí pouze na aktuálních prodejních objednávkách.</span><span class="sxs-lookup"><span data-stu-id="73ff9-164">Payment schedules are shown only on actual sales orders.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="73ff9-165">Pozdější výběr</span><span class="sxs-lookup"><span data-stu-id="73ff9-165">Late selection</span></span></td>
<td><span data-ttu-id="73ff9-166">Výběrem této možnosti použijete vybraný dotaz později.</span><span class="sxs-lookup"><span data-stu-id="73ff9-166">Select this option to apply the selected query later.</span></span> <span data-ttu-id="73ff9-167">Tato možnost se využívá pro dávkové úlohy.</span><span class="sxs-lookup"><span data-stu-id="73ff9-167">This option is used for batch jobs.</span></span> <span data-ttu-id="73ff9-168">Dotaz se spustí při spuštění dávkové úlohy.</span><span class="sxs-lookup"><span data-stu-id="73ff9-168">The query is run when the batch job is run.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="73ff9-169">Snížit množství</span><span class="sxs-lookup"><span data-stu-id="73ff9-169">Reduce quantity</span></span></td>
<td><span data-ttu-id="73ff9-170">Tuto možnost vyberte, chcete-li automaticky snížit dodané množství při zaúčtování dokumentu tak, aby dodané množství se rovnalo dostupným zásobám.</span><span class="sxs-lookup"><span data-stu-id="73ff9-170">Select this option to automatically reduce the delivered quantity when the document is posted, so that the delivered quantity equals the available inventory.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="73ff9-171">Tisk</span><span class="sxs-lookup"><span data-stu-id="73ff9-171">Print</span></span></td>
<td><span data-ttu-id="73ff9-172">Vyberte, kdy chcete tisknout dokumenty:</span><span class="sxs-lookup"><span data-stu-id="73ff9-172">Select when to print documents:</span></span>
<ul>
<li><span data-ttu-id="73ff9-173"><strong>Aktuální</strong> – tisk dokumentů po aktualizaci každé faktury.</span><span class="sxs-lookup"><span data-stu-id="73ff9-173"><strong>Current</strong> – Print documents after each invoice has been updated.</span></span></li>
<li><span data-ttu-id="73ff9-174"><strong>Po</strong> – tisk dokumentů po aktualizaci všech faktur.</span><span class="sxs-lookup"><span data-stu-id="73ff9-174"><strong>After</strong> – Print documents after all the invoices have been updated.</span></span></li>
</ul><span data-ttu-id="73ff9-175">
<strong>Poznámka</strong>: Pole <strong>Tisk</strong> je k dispozici jen tehdy, vyberete-li možnost <strong>Tisk faktury</strong>, <strong>Tisk potvrzení</strong>, <strong>Tisk výdejky</strong> nebo <strong>Tisk dodacího listu</strong>.</span><span class="sxs-lookup"><span data-stu-id="73ff9-175">
<strong>Note:</strong> The <strong>Print</strong> field is available only if you select the <strong>Print invoice</strong>, <strong>Print confirmation</strong>, <strong>Print picking list</strong>, or <strong>Print packing slip</strong> option.</span></span> <span data-ttu-id="73ff9-176">Na stránce <strong>Třídění formuláře</strong> jste například nastavili, aby systém třídil informace podle účtu faktury.</span><span class="sxs-lookup"><span data-stu-id="73ff9-176">For example, on the <strong>Form sorting</strong> page, you have set up the system to sort the information by invoice account.</span></span> <span data-ttu-id="73ff9-177">Poté můžete vybrat možnost <strong>Po</strong> a vytisknout dokumenty v dávce seřazené podle účtu faktury.</span><span class="sxs-lookup"><span data-stu-id="73ff9-177">You can then select <strong>After</strong> to print the documents in a batch that is sorted by invoice account.</span></span> <span data-ttu-id="73ff9-178">V ostatních případech budou dokumenty tištěny před dokončením zpracování a nebudou uspořádány v pořadí, které je zadáno na stránce <strong>Třídění formuláře</strong>.</span><span class="sxs-lookup"><span data-stu-id="73ff9-178">Otherwise, the documents are printed before processing is completed, and the documents aren&#39;t sorted in the order that is specified on the <strong>Form sorting</strong> page.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="73ff9-179">Tisk faktury</span><span class="sxs-lookup"><span data-stu-id="73ff9-179">Print invoice</span></span></td>
<td><span data-ttu-id="73ff9-180">Volbou této možnosti zapnete tisk faktury.</span><span class="sxs-lookup"><span data-stu-id="73ff9-180">Select this option to print the invoice.</span></span> <span data-ttu-id="73ff9-181">Pokud je tato možnost vypnuta, můžete zaúčtovat fakturu bez tisku.</span><span class="sxs-lookup"><span data-stu-id="73ff9-181">If this option is turned off, you can post an invoice without printing it.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="73ff9-182">Odeslat e-mail</span><span class="sxs-lookup"><span data-stu-id="73ff9-182">Send e-mail</span></span></td>
<td><span data-ttu-id="73ff9-183">Tuto možnost vyberte, pokud chcete faktury pro prodejní objednávku po zaúčtování odeslat odběrateli jako přílohu e-mailu.</span><span class="sxs-lookup"><span data-stu-id="73ff9-183">Select this option to send the invoice for a sales order to the customer as an email attachment after the invoice is posted.</span></span> <span data-ttu-id="73ff9-184">Přílohy jsou odesílány jako soubory PDF a XML.</span><span class="sxs-lookup"><span data-stu-id="73ff9-184">Attachments are sent as PDF and XML files.</span></span> <span data-ttu-id="73ff9-185">Tato možnost je k dispozici pouze v případě, že jste na stránce <strong>Parametry elektronických faktur</strong> vybrali možnost <strong>Povolit CFD (elektronické faktury)</strong>.</span><span class="sxs-lookup"><span data-stu-id="73ff9-185">This option is available only if you select the <strong>Enable CFD (electronic invoices)</strong> option on the <strong>Electronic invoice parameters</strong> page.</span></span> <span data-ttu-id="73ff9-186"><strong>Poznámka:</strong> (MEX) Tento ovládací prvek je k dispozici pouze pro právnické osoby, jejichž primární adresa je v Mexiku.</span><span class="sxs-lookup"><span data-stu-id="73ff9-186"><strong>Note:</strong> (MEX) This control is available only to legal entities whose primary address is in Mexico.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="73ff9-187">Použít cíl správy tisku</span><span class="sxs-lookup"><span data-stu-id="73ff9-187">Use print management destination</span></span></td>
<td><span data-ttu-id="73ff9-188">Tuto možnost vyberte, chcete-li použít nastavení tisku zadané na stránce <strong>Nastavení správy tisku</strong> pro transakce, dokument nebo modul.</span><span class="sxs-lookup"><span data-stu-id="73ff9-188">Select this option to use the print settings that are specified for the transaction, document, or module on the <strong>Print management setup</strong> page.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="73ff9-189">Zkontrolovat limit úvěru</span><span class="sxs-lookup"><span data-stu-id="73ff9-189">Check credit limit</span></span></td>
<td><span data-ttu-id="73ff9-190">Vyberte informace, které se budou analyzovat při provádění kontroly limitu úvěru.</span><span class="sxs-lookup"><span data-stu-id="73ff9-190">Select the information that should be analyzed when a credit limit check is performed.</span></span>
<ul>
<li><span data-ttu-id="73ff9-191"><strong>Žádný</strong> – nejsou požadavky na kontrolu limitu úvěru.</span><span class="sxs-lookup"><span data-stu-id="73ff9-191"><strong>None</strong> – There is no requirement for the credit limit check.</span></span></li>
<li><span data-ttu-id="73ff9-192"><strong>Zůstatek</strong> – limit úvěru se kontroluje vůči zůstatku odběratele.</span><span class="sxs-lookup"><span data-stu-id="73ff9-192"><strong>Balance</strong> – The credit limit is checked against the customer balance.</span></span></li>
<li><span data-ttu-id="73ff9-193"><strong>Zůstatek + dodací list nebo příjemka produktu</strong> – limit úvěru se kontroluje vůči zůstatku odběratele a dodávkám.</span><span class="sxs-lookup"><span data-stu-id="73ff9-193"><strong>Balance + packing slip or product receipt</strong> – The credit limit is checked against the customer balance and deliveries.</span></span></li>
<li><span data-ttu-id="73ff9-194"><strong>Zůstatek + vše</strong> – limit úvěru se kontroluje vůči zůstatku odběratele, dodávkám a otevřeným objednávkám.</span><span class="sxs-lookup"><span data-stu-id="73ff9-194"><strong>Balance+All</strong> – The credit limit is checked against the customer balance, deliveries, and open orders.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="73ff9-195">Úvěrové vyrovnání</span><span class="sxs-lookup"><span data-stu-id="73ff9-195">Credit correction</span></span></td>
<td><span data-ttu-id="73ff9-196">Chcete-li v transakcích dokladu dobropis zobrazit jako MD, vyberte tuto možnost.</span><span class="sxs-lookup"><span data-stu-id="73ff9-196">Select this option to display the credit note as a debit in the voucher transactions.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="73ff9-197">Kreditovat zbývající množství</span><span class="sxs-lookup"><span data-stu-id="73ff9-197">Credit remaining quantity</span></span></td>
<td><span data-ttu-id="73ff9-198">Pokud účtujete dobropis, výběrem této možnosti ponecháte zbývající množství na objednávce.</span><span class="sxs-lookup"><span data-stu-id="73ff9-198">If you&#39;re posting a credit note, select this option to keep the remaining quantity on order.</span></span> <span data-ttu-id="73ff9-199">Pokud je zrušen výběr této možnosti, bude zbývající množství nastaveno na hodnotu 0 (nula).</span><span class="sxs-lookup"><span data-stu-id="73ff9-199">If this option is cleared, the remaining quantity is set to 0 (zero).</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="73ff9-200">Souhrnná aktualizace pro</span><span class="sxs-lookup"><span data-stu-id="73ff9-200">Summary update for</span></span></td>
<td><span data-ttu-id="73ff9-201">Vyberte, jak má být shrnuto více prodejních objednávek:</span><span class="sxs-lookup"><span data-stu-id="73ff9-201">Select how multiple sales orders should be summarized:</span></span>
<ul>
<li><span data-ttu-id="73ff9-202"><strong>Žádný</strong> – nedělat souhrn prodejních objednávek.</span><span class="sxs-lookup"><span data-stu-id="73ff9-202"><strong>None</strong> – Don&#39;t summarize sales orders.</span></span> <span data-ttu-id="73ff9-203">Pro každou prodejní objednávku bude například vytvořena samostatná faktura.</span><span class="sxs-lookup"><span data-stu-id="73ff9-203">For example, a separate invoice will be created for each sales order.</span></span></li>
<li><span data-ttu-id="73ff9-204"><strong>Účet faktury</strong> – vytvořit souhrn všech vybraných objednávek podle kritérií nastavených na stránce <strong>Parametry souhrnné aktualizace</strong>.</span><span class="sxs-lookup"><span data-stu-id="73ff9-204"><strong>Invoice account</strong> – Summarize all selected orders, based on the criteria that are set up on the <strong>Summary update parameters</strong> page.</span></span></li>
<li><span data-ttu-id="73ff9-205"><strong>Objednávka</strong> – sumarizovat vybraný rozsah objednávek do jedné objednávky, kterou zadáte.</span><span class="sxs-lookup"><span data-stu-id="73ff9-205"><strong>Order</strong> – Summarize a selected range of orders into one order that you specify.</span></span> <span data-ttu-id="73ff9-206">Vytvoří se souhrn objednávek podle kritérií nastavených na stránce <strong>Parametry souhrnné aktualizace</strong>.</span><span class="sxs-lookup"><span data-stu-id="73ff9-206">The orders are summarized based on the criteria that are set up on the <strong>Summary update parameters</strong> page.</span></span> <span data-ttu-id="73ff9-207">Je-li vybrána tato možnost, je nutné vybrat některou možnost v poli <strong>Prodejní objednávka</strong>.</span><span class="sxs-lookup"><span data-stu-id="73ff9-207">If you select this option, you must select a value in the <strong>Sales order</strong> field.</span></span></li>
<li><span data-ttu-id="73ff9-208"><strong>Automatické shrnutí</strong> – jestliže byly na stránce <strong>Parametry souhrnné aktualizace</strong> určeny všechny souhrnné aktualizace, vytvoří se souhrn všech vybraných objednávek na základě kritérií nastavených na stránce <strong>Parametry souhrnné aktualizace</strong>.</span><span class="sxs-lookup"><span data-stu-id="73ff9-208"><strong>Automatic summary</strong> – If summary updates have been specified on the <strong>Summary update</strong> page, summarize all selected orders, based on the criteria that are set up on the <strong>Summary update parameters</strong> page.</span></span> <span data-ttu-id="73ff9-209">Pokud nebyly souhrnné aktualizace určeny, objednávka se zaúčtuje samostatně.</span><span class="sxs-lookup"><span data-stu-id="73ff9-209">If summary updates haven&#39;t been specified, the order is posted separately.</span></span></li>
<li><span data-ttu-id="73ff9-210"><strong>Dodací list</strong> – pro každý dodací list se vytvoří souhrn vybraného rozsahu objednávek do jedné faktury.</span><span class="sxs-lookup"><span data-stu-id="73ff9-210"><strong>Packing slip</strong> – Summarize a selected range of orders into one invoice for each packing slip.</span></span> <span data-ttu-id="73ff9-211">Tato možnost je k dispozici jen tehdy, je-li v poli <strong>Množství</strong> vybrána možnost <strong>Dodací list</strong>.</span><span class="sxs-lookup"><span data-stu-id="73ff9-211">This option is available only if <strong>Packing slip</strong> is selected in the <strong>Quantity</strong> field.</span></span></li>
</ul></td>
</tr>
</tbody>
</table>






