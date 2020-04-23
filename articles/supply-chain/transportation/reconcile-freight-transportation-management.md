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
ms.search.form: TMSAuditMaster, TMSFreightBillInvoiceReconcile, TMSFreightBillSummary, TMSFreightBillType, TMSFreightMatchReason, TMSInvoiceTable
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 89983
ms.assetid: bc34a9b1-0c11-4797-b463-25409cf98ca8
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mafoge
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 0e1680572f1ba9816c9ec45ef52498cab1f45247
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/02/2020
ms.locfileid: "3206212"
---
# <a name="reconcile-freight-in-transportation-management"></a><span data-ttu-id="263bb-103">Odsouhlasení nákladu ve správě přepravy</span><span class="sxs-lookup"><span data-stu-id="263bb-103">Reconcile freight in transportation management</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="263bb-104">Toto téma popisuje proces odsouhlasení dopravného.</span><span class="sxs-lookup"><span data-stu-id="263bb-104">This topic describes the freight reconciliation process.</span></span>

<span data-ttu-id="263bb-105">Odsouhlasení dopravného lze provádět ručně, nebo je můžete nastavit automaticky.</span><span class="sxs-lookup"><span data-stu-id="263bb-105">Freight reconciliation can be done manually, or it can be set up to occur automatically.</span></span> <span data-ttu-id="263bb-106">Chcete-li použít automatické odsouhlasení dopravného, musíte vytvořit předlohu auditu, kde definujete kritéria určující, které účty dopravného jsou spárovány automaticky.</span><span class="sxs-lookup"><span data-stu-id="263bb-106">To use automatic freight reconciliation, you must set up an audit master where you can define criteria that determine which freight bills are matched automatically.</span></span>

## <a name="the-freight-reconciliation-process"></a><span data-ttu-id="263bb-107">Proces odsouhlasení dopravného</span><span class="sxs-lookup"><span data-stu-id="263bb-107">The freight reconciliation process</span></span>
<span data-ttu-id="263bb-108">Sazby dopravného se vypočítají podle sazebního modulu, který je spojen s odpovídajícím dopravcem.</span><span class="sxs-lookup"><span data-stu-id="263bb-108">Freight rates are calculated by the rate engine that is associated with the relevant shipping carrier.</span></span> <span data-ttu-id="263bb-109">Po potvrzení nákladu je generován účet dopravného, do kterého jsou přeneseny sazby za přepravu.</span><span class="sxs-lookup"><span data-stu-id="263bb-109">When a load is confirmed, a freight bill is generated, and the freight rates are transferred to it.</span></span> <span data-ttu-id="263bb-110">Sazby za přepravu jsou rozděleny jako vedlejší náklady do příslušného zdrojového dokladu (nákupní objednávky, prodejní objednávky nebo převodní příkaz) v závislosti na nastavení, které se používá pro normální proces fakturace.</span><span class="sxs-lookup"><span data-stu-id="263bb-110">The freight rates are apportioned as miscellaneous charges to the relevant source document (purchase order, sales order, and/or transfer order), depending on the setup that is used for the regular billing process.</span></span> <span data-ttu-id="263bb-111">Proces odsouhlasení dopravného (známý také jako proces spárování) můžete spustit ihned po přijetí faktury dopravného od dopravce.</span><span class="sxs-lookup"><span data-stu-id="263bb-111">The freight reconciliation process (which is also known as the matching process) can start as soon as the freight invoice arrives from the shipping carrier.</span></span> <span data-ttu-id="263bb-112">Fakturu lze přijímat elektronicky nebo papírově.</span><span class="sxs-lookup"><span data-stu-id="263bb-112">The invoice can be received electronically or on paper.</span></span> <span data-ttu-id="263bb-113">Pokud je faktura přijata papírově, může vygenerovat elektronickou fakturu pomocí účtu dopravného coby předlohy.</span><span class="sxs-lookup"><span data-stu-id="263bb-113">If the invoice is received on paper, you can generate an electronic invoice by using the freight bill as a template.</span></span> 

<span data-ttu-id="263bb-114">[![Proces odsouhlasení dopravného](./media/freight-reconcilation-process.jpg)](./media/freight-reconcilation-process.jpg)</span><span class="sxs-lookup"><span data-stu-id="263bb-114">[![Freight reconcilation process](./media/freight-reconcilation-process.jpg)](./media/freight-reconcilation-process.jpg)</span></span>

## <a name="manual-reconciliation"></a><span data-ttu-id="263bb-115">Ruční odsouhlasení</span><span class="sxs-lookup"><span data-stu-id="263bb-115">Manual reconciliation</span></span>
<span data-ttu-id="263bb-116">Pokud provádíte odsouhlasení dopravného ručně, musíte spárovat každý řádek faktury s řádkem/řádky účtu dopravného pro náklad, který se fakturuje.</span><span class="sxs-lookup"><span data-stu-id="263bb-116">If you're reconciling freight manually, you must match each invoice line with the freight bill line or lines for the load that is being invoiced.</span></span> <span data-ttu-id="263bb-117">Toto párování provádíte na stránce **Spárování účtů dopravného a faktur**.</span><span class="sxs-lookup"><span data-stu-id="263bb-117">You do this matching on the **Freight bill and invoice matching** page.</span></span> <span data-ttu-id="263bb-118">Pokud částka na řádku faktury neodpovídá částce na účtu dopravného, je nutné vybrat důvod odsouhlasení pro tento rozdíl.</span><span class="sxs-lookup"><span data-stu-id="263bb-118">If the amount on the invoice line doesn’t match the freight bill amount, you must select a reconciliation reason for the difference.</span></span> <span data-ttu-id="263bb-119">Pokud existuje více důvodů k odsouhlasení, je možné rozdělit nespárované částky mezi ně.</span><span class="sxs-lookup"><span data-stu-id="263bb-119">If there are multiple reasons for reconciliation, you can split the unmatched amount across them.</span></span> <span data-ttu-id="263bb-120">Důvod odsouhlasení určuje, jak jsou rozdílné částky zaúčtovány v hlavní knize.</span><span class="sxs-lookup"><span data-stu-id="263bb-120">The reconciliation reason determines how the difference amounts are posted in the general ledger.</span></span> <span data-ttu-id="263bb-121">Pokud zohledňujete odsouhlasení celé fakturované částky, je částka odeslána ke schválení, a následně je zaúčtován deník.</span><span class="sxs-lookup"><span data-stu-id="263bb-121">When the reconciliation of the whole invoice amount is accounted for, it's submitted for approval, and then the journal is posted.</span></span> <span data-ttu-id="263bb-122">Následující obrázek ukazuje, jak generovat fakturu za dopravné a provádět odsouhlasení dopravného.</span><span class="sxs-lookup"><span data-stu-id="263bb-122">The following illustration shows how to generate a freight invoice and do freight reconciliation.</span></span> 
<span data-ttu-id="263bb-123">[![Úlohy odsouhlasení dopravného](./media/processflowforfreightreconciliation.jpg)](./media/processflowforfreightreconciliation.jpg)</span><span class="sxs-lookup"><span data-stu-id="263bb-123">[![Freight reconcilation tasks](./media/processflowforfreightreconciliation.jpg)](./media/processflowforfreightreconciliation.jpg)</span></span>
## <a name="automatic-reconciliation"></a><span data-ttu-id="263bb-124">Automatické odsouhlasení</span><span class="sxs-lookup"><span data-stu-id="263bb-124">Automatic reconciliation</span></span>
<span data-ttu-id="263bb-125">Chcete-li použít automatické odsouhlasení, je nutné zadat plán odsouhlasení, stejně jako faktury a dopravce, které chcete použít.</span><span class="sxs-lookup"><span data-stu-id="263bb-125">To use automatic reconciliation, you must specify the schedule for reconciliation, and the invoices and shipping carriers to use.</span></span> <span data-ttu-id="263bb-126">Párování řádků faktury a účtů dopravného se provádí podle nastavení v hlavním auditu a podle typu účtu dopravného.</span><span class="sxs-lookup"><span data-stu-id="263bb-126">The matching of the invoice lines and freight bills is done according to the setup of the audit master and freight bill type.</span></span> <span data-ttu-id="263bb-127">Po spuštění automatického odsouhlasení musíte zpracovat všechny faktury, které systém nespáruje.</span><span class="sxs-lookup"><span data-stu-id="263bb-127">After you run the automatic reconciliation, you must handle any invoices that the system can't match.</span></span> <span data-ttu-id="263bb-128">Tyto faktury musíte poté ručně zpracovat, než budete moci zaúčtovat všechny faktury pro platbu.</span><span class="sxs-lookup"><span data-stu-id="263bb-128">You must then process these invoices manually before you can post all the invoices for payment.</span></span>



