---
title: Odsouhlasení nákladu ve správě přepravy
description: Toto téma popisuje proces odsouhlasení dopravného.
author: MarkusFogelberg
manager: tfehr
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TMSAuditMaster, TMSFreightBillInvoiceReconcile, TMSFreightBillSummary, TMSFreightBillType, TMSFreightMatchReason, TMSFBDetailReconcile, TMSInvoiceTable,TMSInvoiceLineReconcile,TMSReconcileInvoice, TMSFreightBillDetail, TMSFreightBillTypeAssignment, TMSRejectInvoiceLine, TMSMiscellaneousCharge
audience: Application User
ms.reviewer: kamaybac
ms.custom: 89983
ms.assetid: bc34a9b1-0c11-4797-b463-25409cf98ca8
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mafoge
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: ac07155e4dde77689b1994abfb8b30f45d5a5a30
ms.sourcegitcommit: b6686265314499056690538eaa95ca51cff7c720
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 01/15/2021
ms.locfileid: "5014501"
---
# <a name="reconcile-freight-in-transportation-management"></a><span data-ttu-id="36a0c-103">Odsouhlasení nákladu ve správě přepravy</span><span class="sxs-lookup"><span data-stu-id="36a0c-103">Reconcile freight in transportation management</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="36a0c-104">Toto téma popisuje proces odsouhlasení dopravného.</span><span class="sxs-lookup"><span data-stu-id="36a0c-104">This topic describes the freight reconciliation process.</span></span>

<span data-ttu-id="36a0c-105">Odsouhlasení dopravného lze provádět ručně, nebo je můžete nastavit automaticky.</span><span class="sxs-lookup"><span data-stu-id="36a0c-105">Freight reconciliation can be done manually, or it can be set up to occur automatically.</span></span> <span data-ttu-id="36a0c-106">Chcete-li použít automatické odsouhlasení dopravného, musíte vytvořit předlohu auditu, kde definujete kritéria určující, které účty dopravného jsou spárovány automaticky.</span><span class="sxs-lookup"><span data-stu-id="36a0c-106">To use automatic freight reconciliation, you must set up an audit master where you can define criteria that determine which freight bills are matched automatically.</span></span>

## <a name="the-freight-reconciliation-process"></a><span data-ttu-id="36a0c-107">Proces odsouhlasení dopravného</span><span class="sxs-lookup"><span data-stu-id="36a0c-107">The freight reconciliation process</span></span>

<span data-ttu-id="36a0c-108">Sazby dopravného se vypočítají podle sazebního modulu, který je spojen s odpovídajícím dopravcem.</span><span class="sxs-lookup"><span data-stu-id="36a0c-108">Freight rates are calculated by the rate engine that is associated with the relevant shipping carrier.</span></span> <span data-ttu-id="36a0c-109">Po potvrzení nákladu je generován účet dopravného, do kterého jsou přeneseny sazby za přepravu.</span><span class="sxs-lookup"><span data-stu-id="36a0c-109">When a load is confirmed, a freight bill is generated, and the freight rates are transferred to it.</span></span> <span data-ttu-id="36a0c-110">Sazby za přepravu jsou rozděleny jako vedlejší náklady do příslušného zdrojového dokladu (nákupní objednávky, prodejní objednávky nebo převodní příkaz) v závislosti na nastavení, které se používá pro normální proces fakturace.</span><span class="sxs-lookup"><span data-stu-id="36a0c-110">The freight rates are apportioned as miscellaneous charges to the relevant source document (purchase order, sales order, and/or transfer order), depending on the setup that is used for the regular billing process.</span></span> <span data-ttu-id="36a0c-111">Proces odsouhlasení dopravného (známý také jako proces spárování) můžete spustit ihned po přijetí faktury dopravného od dopravce.</span><span class="sxs-lookup"><span data-stu-id="36a0c-111">The freight reconciliation process (which is also known as the matching process) can start as soon as the freight invoice arrives from the shipping carrier.</span></span> <span data-ttu-id="36a0c-112">Fakturu lze přijímat elektronicky nebo papírově.</span><span class="sxs-lookup"><span data-stu-id="36a0c-112">The invoice can be received electronically or on paper.</span></span> <span data-ttu-id="36a0c-113">Pokud je faktura přijata papírově, může vygenerovat elektronickou fakturu pomocí účtu dopravného coby předlohy.</span><span class="sxs-lookup"><span data-stu-id="36a0c-113">If the invoice is received on paper, you can generate an electronic invoice by using the freight bill as a template.</span></span>

<span data-ttu-id="36a0c-114">[![Proces odsouhlasení dopravného](./media/freight-reconcilation-process.jpg)](./media/freight-reconcilation-process.jpg)</span><span class="sxs-lookup"><span data-stu-id="36a0c-114">[![Freight reconciliation process](./media/freight-reconcilation-process.jpg)](./media/freight-reconcilation-process.jpg)</span></span>

## <a name="manual-reconciliation"></a><span data-ttu-id="36a0c-115">Ruční odsouhlasení</span><span class="sxs-lookup"><span data-stu-id="36a0c-115">Manual reconciliation</span></span>

<span data-ttu-id="36a0c-116">Pokud provádíte odsouhlasení dopravného ručně, musíte spárovat každý řádek faktury s řádkem/řádky účtu dopravného pro náklad, který se fakturuje.</span><span class="sxs-lookup"><span data-stu-id="36a0c-116">If you're reconciling freight manually, you must match each invoice line with the freight bill line or lines for the load that is being invoiced.</span></span> <span data-ttu-id="36a0c-117">Toto párování provádíte na stránce **Spárování účtů dopravného a faktur**.</span><span class="sxs-lookup"><span data-stu-id="36a0c-117">You do this matching on the **Freight bill and invoice matching** page.</span></span> <span data-ttu-id="36a0c-118">Pokud částka na řádku faktury neodpovídá částce na účtu dopravného, je nutné vybrat důvod odsouhlasení pro tento rozdíl.</span><span class="sxs-lookup"><span data-stu-id="36a0c-118">If the amount on the invoice line doesn’t match the freight bill amount, you must select a reconciliation reason for the difference.</span></span> <span data-ttu-id="36a0c-119">Pokud existuje více důvodů k odsouhlasení, je možné rozdělit nespárované částky mezi ně.</span><span class="sxs-lookup"><span data-stu-id="36a0c-119">If there are multiple reasons for reconciliation, you can split the unmatched amount across them.</span></span> <span data-ttu-id="36a0c-120">Důvod odsouhlasení určuje, jak jsou rozdílné částky zaúčtovány v hlavní knize.</span><span class="sxs-lookup"><span data-stu-id="36a0c-120">The reconciliation reason determines how the difference amounts are posted in the general ledger.</span></span> <span data-ttu-id="36a0c-121">Pokud zohledňujete odsouhlasení celé fakturované částky, je částka odeslána ke schválení, a následně je zaúčtován deník.</span><span class="sxs-lookup"><span data-stu-id="36a0c-121">When the reconciliation of the whole invoice amount is accounted for, it's submitted for approval, and then the journal is posted.</span></span> <span data-ttu-id="36a0c-122">Následující obrázek ukazuje, jak generovat fakturu za dopravné a provádět odsouhlasení dopravného.</span><span class="sxs-lookup"><span data-stu-id="36a0c-122">The following illustration shows how to generate a freight invoice and do freight reconciliation.</span></span>

<span data-ttu-id="36a0c-123">[![Úlohy odsouhlasení dopravného](./media/processflowforfreightreconciliation.jpg)](./media/processflowforfreightreconciliation.jpg)</span><span class="sxs-lookup"><span data-stu-id="36a0c-123">[![Freight reconciliation tasks](./media/processflowforfreightreconciliation.jpg)](./media/processflowforfreightreconciliation.jpg)</span></span>

## <a name="automatic-reconciliation"></a><span data-ttu-id="36a0c-124">Automatické odsouhlasení</span><span class="sxs-lookup"><span data-stu-id="36a0c-124">Automatic reconciliation</span></span>

<span data-ttu-id="36a0c-125">Chcete-li použít automatické odsouhlasení, je nutné zadat plán odsouhlasení, stejně jako faktury a dopravce, které chcete použít.</span><span class="sxs-lookup"><span data-stu-id="36a0c-125">To use automatic reconciliation, you must specify the schedule for reconciliation, and the invoices and shipping carriers to use.</span></span> <span data-ttu-id="36a0c-126">Párování řádků faktury a účtů dopravného se provádí podle nastavení v hlavním auditu a podle typu účtu dopravného.</span><span class="sxs-lookup"><span data-stu-id="36a0c-126">The matching of the invoice lines and freight bills is done according to the setup of the audit master and freight bill type.</span></span> <span data-ttu-id="36a0c-127">Po spuštění automatického odsouhlasení musíte zpracovat všechny faktury, které systém nespáruje.</span><span class="sxs-lookup"><span data-stu-id="36a0c-127">After you run the automatic reconciliation, you must handle any invoices that the system can't match.</span></span> <span data-ttu-id="36a0c-128">Tyto faktury musíte poté ručně zpracovat, než budete moci zaúčtovat všechny faktury pro platbu.</span><span class="sxs-lookup"><span data-stu-id="36a0c-128">You must then process these invoices manually before you can post all the invoices for payment.</span></span>

## <a name="match-freight-bills-with-freight-invoices-using-automatic-or-manual-reconciliation"></a><span data-ttu-id="36a0c-129">Spárujte přepravní faktury s přepravními fakturami pomocí automatického nebo ručního odsouhlasení</span><span class="sxs-lookup"><span data-stu-id="36a0c-129">Match freight bills with freight invoices using automatic or manual reconciliation</span></span>

<span data-ttu-id="36a0c-130">*Párování* je proces hledání účtů za přepravu, které odpovídají každé faktuře za přepravu.</span><span class="sxs-lookup"><span data-stu-id="36a0c-130">*Matching* is the process of finding the freight bills that correspond to each freight invoice.</span></span> <span data-ttu-id="36a0c-131">To lze provést párováním jednotlivých řádků faktur (ruční párování) nebo párováním všech dostupných faktur najednou (automatické párování).</span><span class="sxs-lookup"><span data-stu-id="36a0c-131">This can be done by matching the invoice lines one-by-one (manual matching), or by matching all available invoices at once (auto matching).</span></span>

### <a name="auto-matching"></a><span data-ttu-id="36a0c-132">Automatické párování</span><span class="sxs-lookup"><span data-stu-id="36a0c-132">Auto matching</span></span>

<span data-ttu-id="36a0c-133">Při párování více faktur za přepravu se stejným účtem za přepravu funguje proces automatického párování následovně:</span><span class="sxs-lookup"><span data-stu-id="36a0c-133">When matching multiple freight invoices to the same freight bill, the process for auto matching works as follows:</span></span>

1. <span data-ttu-id="36a0c-134">Všechny faktury za přepravu, které se neshodují, jsou seřazeny podle částky, s největší částkou jako první.</span><span class="sxs-lookup"><span data-stu-id="36a0c-134">All freight invoices not matched are sorted by amount, with largest amount first.</span></span>
1. <span data-ttu-id="36a0c-135">Faktury za přepravu se spárují jedna po druhé, dokud na faktuře za přepravu nezůstane žádná kladná částka.</span><span class="sxs-lookup"><span data-stu-id="36a0c-135">The freight invoices are matched one-by-one, until the freight bill has no positive amount remaining.</span></span>
1. <span data-ttu-id="36a0c-136">V závislosti na nastavení hlavního auditoru a zbývající částky na fakturách za přepravu je nastavena zbývající částka.</span><span class="sxs-lookup"><span data-stu-id="36a0c-136">Depending on the setup of the audit master and the remaining amount on the freight invoices, the remaining amount is set.</span></span>

### <a name="manual-matching"></a><span data-ttu-id="36a0c-137">Ruční párování</span><span class="sxs-lookup"><span data-stu-id="36a0c-137">Manual matching</span></span>

<span data-ttu-id="36a0c-138">Ke spárování budou k dispozici všechny účty za přepravu s kladnými částkami.</span><span class="sxs-lookup"><span data-stu-id="36a0c-138">All freight bills with positive amounts will be available for matching.</span></span> <span data-ttu-id="36a0c-139">Podobně jako automatické přiřazování bude uživatel moci pouze spárovat přepravní faktury se zápornými částkami s přepravními doklady, které nejsou plně uzavřeny.</span><span class="sxs-lookup"><span data-stu-id="36a0c-139">Similar to auto matching, the user will only be able to match freight invoices with negative amounts to freight bills not fully matched.</span></span>

### <a name="example"></a><span data-ttu-id="36a0c-140">Příklad</span><span class="sxs-lookup"><span data-stu-id="36a0c-140">Example</span></span>

<span data-ttu-id="36a0c-141">Předpokládejme, že máte přepravní doklad (FB) za částku 1 500 a že jste vytvořili tři přepravní faktury za přepravní doklad s jedním řádkem faktury pro každou fakturu s následujícím nastavením:</span><span class="sxs-lookup"><span data-stu-id="36a0c-141">Suppose that you have a freight bill (FB) for an amount of 1500 and you have created three freight invoices for the freight bill with one invoice line for each invoice with following settings:</span></span>

- <span data-ttu-id="36a0c-142">Původní nákladní list (FB): Částka 1 500</span><span class="sxs-lookup"><span data-stu-id="36a0c-142">Original freight bill (FB): Amount 1500</span></span>
- <span data-ttu-id="36a0c-143">Faktura 1 (Inv1): Částka 1 000</span><span class="sxs-lookup"><span data-stu-id="36a0c-143">Invoice 1 (Inv1): Amount 1000</span></span>
- <span data-ttu-id="36a0c-144">Faktura 2 (Inv2): Částka 600</span><span class="sxs-lookup"><span data-stu-id="36a0c-144">Invoice 2 (Inv2): Amount 600</span></span>
- <span data-ttu-id="36a0c-145">Faktura 3 (Inv3): Částka -100</span><span class="sxs-lookup"><span data-stu-id="36a0c-145">Invoice 3 (Inv3): Amount -100</span></span>

#### <a name="automatic-matching-result"></a><span data-ttu-id="36a0c-146">Výsledek automatického párování</span><span class="sxs-lookup"><span data-stu-id="36a0c-146">Automatic matching result</span></span>

<span data-ttu-id="36a0c-147">Automatické přiřazování se provede v následujícím pořadí:</span><span class="sxs-lookup"><span data-stu-id="36a0c-147">Auto matching will execute in following order:</span></span>

1. <span data-ttu-id="36a0c-148">Seřadit všechny přepravní faktury sestupně podle částky: Inv1 -> Inv2 -> Inv3.</span><span class="sxs-lookup"><span data-stu-id="36a0c-148">Sort all freight invoices descending by amount: Inv1 -> Inv2 -> Inv3.</span></span>
1. <span data-ttu-id="36a0c-149">Spárujte Inv1 s FB.</span><span class="sxs-lookup"><span data-stu-id="36a0c-149">Match Inv1 with FB.</span></span> <span data-ttu-id="36a0c-150">Inv1 má 1000 spárováno a FB má zbývající částku 500, takže stav je nastaven na *Částečně spárováno*.</span><span class="sxs-lookup"><span data-stu-id="36a0c-150">Inv1 has 1000 matched and FB has 500 amount remaining, so the status is set to *Partially matched*.</span></span>
1. <span data-ttu-id="36a0c-151">Spárujte Inv2 s FB.</span><span class="sxs-lookup"><span data-stu-id="36a0c-151">Match Inv2 with FB.</span></span> <span data-ttu-id="36a0c-152">Inv2 má 500 spárováno a FB má zbývající částku 0, takže stav je nastaven na *Plně spárováno*.</span><span class="sxs-lookup"><span data-stu-id="36a0c-152">Inv2 has 500 matched and FB has 0 remaining, so the status is set to *Fully matched*.</span></span>
1. <span data-ttu-id="36a0c-153">Protože FB je nyní plně uzavřeno, Inv3 nebude zpracována.</span><span class="sxs-lookup"><span data-stu-id="36a0c-153">Because FB is now fully matched, Inv3 won't be processed.</span></span>

#### <a name="manual-matching-result"></a><span data-ttu-id="36a0c-154">Výsledek ručního párování</span><span class="sxs-lookup"><span data-stu-id="36a0c-154">Manual matching result</span></span>

<span data-ttu-id="36a0c-155">U ručního párování se výsledky liší v závislosti na pořadí párování, jak je znázorněno v následujících příkladech.</span><span class="sxs-lookup"><span data-stu-id="36a0c-155">For manual matching, the results vary depending on the order of the matching, as illustrated in the following example cases.</span></span>

##### <a name="manual-matching-case-1"></a><span data-ttu-id="36a0c-156">Ruční párování, případ 1</span><span class="sxs-lookup"><span data-stu-id="36a0c-156">Manual matching case 1</span></span>

<span data-ttu-id="36a0c-157">Jedním ze způsobů ručního párování v tomto příkladu je tento postup:</span><span class="sxs-lookup"><span data-stu-id="36a0c-157">One way to do manual matching for this example is to proceed as follows:</span></span>

1. <span data-ttu-id="36a0c-158">Spárujte FB s Inv1.</span><span class="sxs-lookup"><span data-stu-id="36a0c-158">Match FB with Inv1.</span></span> <span data-ttu-id="36a0c-159">FB má zbývající částku 500, takže stav je nastaven na *Částečně spárováno*.</span><span class="sxs-lookup"><span data-stu-id="36a0c-159">FB has 500 amount remaining, so the status set to *Partially matched*.</span></span>
1. <span data-ttu-id="36a0c-160">Spárujte Inv2 s FB.</span><span class="sxs-lookup"><span data-stu-id="36a0c-160">Match Inv2 with FB.</span></span> <span data-ttu-id="36a0c-161">Inv2 má 500 spárováno a FB má zbývající částku 0, takže stav je nastaven na *Plně spárováno*.</span><span class="sxs-lookup"><span data-stu-id="36a0c-161">Inv2 has 500 matched and FB has 0 remaining, so the status is set to *Fully matched*.</span></span>
1. <span data-ttu-id="36a0c-162">Když ručně spárujete Inv3, nenajdete žádné nespárované účty za přepravu.</span><span class="sxs-lookup"><span data-stu-id="36a0c-162">When manually matching Inv3, you won't find any unmatched freight bills.</span></span>

<span data-ttu-id="36a0c-163">Tento případ je v podstatě stejný jako automatické párování</span><span class="sxs-lookup"><span data-stu-id="36a0c-163">This case is essentially the same as auto matching</span></span>

##### <a name="manual-matching-case-2"></a><span data-ttu-id="36a0c-164">Ruční párování, případ 2</span><span class="sxs-lookup"><span data-stu-id="36a0c-164">Manual matching case 2</span></span>

<span data-ttu-id="36a0c-165">Dalším ze způsobů ručního párování v tomto příkladu je tento postup:</span><span class="sxs-lookup"><span data-stu-id="36a0c-165">Another way to do manual matching for this example is to proceed as follows:</span></span>

1. <span data-ttu-id="36a0c-166">Spárujte Inv3 s FB.</span><span class="sxs-lookup"><span data-stu-id="36a0c-166">Match Inv3 with FB.</span></span> <span data-ttu-id="36a0c-167">Nyní má FB zbývající částku 1600, což je stejné jako odečtení záporných 100 nad 1500.</span><span class="sxs-lookup"><span data-stu-id="36a0c-167">Now FB has amount remaining 1600, which is the same as subtracting negative 100 on top of 1500.</span></span> <span data-ttu-id="36a0c-168">FB i Inv3 mají shodné množství -100.</span><span class="sxs-lookup"><span data-stu-id="36a0c-168">Both FB and Inv3 have a matched quantity of -100.</span></span>
1. <span data-ttu-id="36a0c-169">Spárujte Inv1 a Inv 2 s FB jeden po druhém.</span><span class="sxs-lookup"><span data-stu-id="36a0c-169">Match Inv1 and Inv 2 with FB one after another.</span></span> <span data-ttu-id="36a0c-170">FB je plně uzavřeno.</span><span class="sxs-lookup"><span data-stu-id="36a0c-170">FB is fully matched.</span></span>

<span data-ttu-id="36a0c-171">Jak ukazuje tento příklad, párování faktur za přepravu se zápornými částkami by se mělo provádět pouze ručně.</span><span class="sxs-lookup"><span data-stu-id="36a0c-171">As this example shows, matching freight invoices with negative amounts should only be done manually.</span></span> <span data-ttu-id="36a0c-172">Tím zajistíte, že je vždy možné spárovat přepravní faktury se zápornými částkami k přepravnímu dokladu, který není plně uzavřen, protože vám to umožňuje řídit odpovídající sekvenci.</span><span class="sxs-lookup"><span data-stu-id="36a0c-172">This will ensure that it is always possible to match the freight invoices with negative amounts to a freight bill not fully matched because that enables you to control the matching sequence.</span></span>
