---
title: Zpracování přidělení
description: Tento článek obsahuje informace o přiděleních, možnostech pro jejich zpracování je v aplikaci Microsoft Dynamics 365 Finance a o tom, jak je lze použít při plánování rozpočtu. Přidělení se používají k rozdělení částek mezi více kombinací účtů hlavní knihy. Díky nim lze zajistit, aby se výdaje nebo výnosy účtovaly v účetnictví na správný objekt.
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AccountingDistribution, LedgerAllocationRule, MainAccount
audience: Application User
ms.reviewer: roschlom
ms.custom: 17361
ms.assetid: 04c8548a-0af9-492b-954b-946b4f8ca023
ms.search.region: Global
ms.author: peakerbl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: b13496e764f907201a23f0dd6772ee22efffb250
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/15/2021
ms.locfileid: "5204971"
---
# <a name="process-allocations"></a><span data-ttu-id="cb126-105">Zpracování přidělení</span><span class="sxs-lookup"><span data-stu-id="cb126-105">Process allocations</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="cb126-106">Tento článek obsahuje informace o přiděleních, možnostech pro jejich zpracování a o tom, jak je lze použít při plánování rozpočtu.</span><span class="sxs-lookup"><span data-stu-id="cb126-106">This article provides information about allocations, the options for processing them, and how they can be used in budget planning.</span></span> <span data-ttu-id="cb126-107">Přidělení se používají k rozdělení částek mezi více kombinací účtů hlavní knihy.</span><span class="sxs-lookup"><span data-stu-id="cb126-107">Allocations are used to distribute amounts across multiple ledger account combinations.</span></span> <span data-ttu-id="cb126-108">Díky nim lze zajistit, aby se výdaje nebo výnosy účtovaly v účetnictví na správný objekt.</span><span class="sxs-lookup"><span data-stu-id="cb126-108">They help ensure that expenses or revenues are charged to the correct object in accounting.</span></span>

<span data-ttu-id="cb126-109">Tento proces podporují následující možnosti:</span><span class="sxs-lookup"><span data-stu-id="cb126-109">The following capabilities support this process:</span></span>

-   <span data-ttu-id="cb126-110">Ručně přidělit částky transakcí pomocí rozdělení akcí v rozúčtování nebo použitím výchozích šablon finanční dimenze v dokumentu.</span><span class="sxs-lookup"><span data-stu-id="cb126-110">Manually allocate transaction amounts by using the Split action in accounting distributions, or by applying financial dimension default templates to a document.</span></span> <span data-ttu-id="cb126-111">Další informace naleznete v tématu [Rozúčtování](../accounts-payable/accounting-distributions.md).</span><span class="sxs-lookup"><span data-stu-id="cb126-111">For more information, see [Accounting distributions](../accounts-payable/accounting-distributions.md).</span></span>
-   <span data-ttu-id="cb126-112">Automaticky přidělit částky transakce na základě podmínek přidělení definovaných v individuálním hlavním účtu.</span><span class="sxs-lookup"><span data-stu-id="cb126-112">Automatically allocate transactions amounts based on allocation terms defined on individual main account.</span></span> <span data-ttu-id="cb126-113">Položky účtu přidělení se budou generovat pro každý deník podle procenta a cílového účtu hlavní knihy, kdykoli účetní položka splní kritéria definovaná jako zdrojový účet hlavní knihy.</span><span class="sxs-lookup"><span data-stu-id="cb126-113">Allocation account entries will be generated for each journal based on the percentage and destination ledger account whenever an accounting entry meets the criteria defined as the source ledger account.</span></span> <span data-ttu-id="cb126-114">Další informace naleznete v tématu [Podmínky přidělení hlavního účtu](../general-ledger/main-account-allocation-terms.md).</span><span class="sxs-lookup"><span data-stu-id="cb126-114">For more information, see [Main account allocation terms](../general-ledger/main-account-allocation-terms.md)</span></span>
-   <span data-ttu-id="cb126-115">Automaticky přidělit zůstatky hlavní knihy nebo pevné částky na základě pravidel přidělení hlavní knihy.</span><span class="sxs-lookup"><span data-stu-id="cb126-115">Automatically allocate ledger balances or fixed amounts based on ledger allocation rules.</span></span> <span data-ttu-id="cb126-116">Pravidla přidělení hlavní knihy se zpracovávají v pravidelných intervalech pomocí deníků přidělení.</span><span class="sxs-lookup"><span data-stu-id="cb126-116">The ledger allocation rules are processed on a periodic basis using allocation journals.</span></span> <span data-ttu-id="cb126-117">Další informace naleznete v tématu [Alokační pravidla](../general-ledger/ledger-allocation-rules.md).</span><span class="sxs-lookup"><span data-stu-id="cb126-117">For more information, see [Allocation rules](../general-ledger/ledger-allocation-rules.md).</span></span>

###  <a name="allocations-in-budget-planning"></a><span data-ttu-id="cb126-118">Přidělení v plánování rozpočtu</span><span class="sxs-lookup"><span data-stu-id="cb126-118">Allocations in budget planning</span></span>

<span data-ttu-id="cb126-119">Pravidla přidělení hlavní knihy můžete použít pro plány rozpočtu.</span><span class="sxs-lookup"><span data-stu-id="cb126-119">Ledger allocation rules can be used for budget plans.</span></span> <span data-ttu-id="cb126-120">Při použití pravidla přidělení hlavní knihy v plánování rozpočtu, pravidla přidělení fungují stejným způsobem jako v hlavní knize, ale zdrojová data a cílová data pocházejí z plánu rozpočtu.</span><span class="sxs-lookup"><span data-stu-id="cb126-120">When you use ledger allocation rules in budget planning, the allocation rules work the same way they would in the ledger, but the source data and destination data comes from the budget plan.</span></span> <span data-ttu-id="cb126-121">Můžete ručně vybrat pravidla pro přidělení hlavní knihy pro použití v plánu rozpočtu.</span><span class="sxs-lookup"><span data-stu-id="cb126-121">You can manually select ledger allocation rules to use for budget plans.</span></span> <span data-ttu-id="cb126-122">Můžete také použít plán přidělení, která se spouští jako součást procesu workflowu.</span><span class="sxs-lookup"><span data-stu-id="cb126-122">Alternatively, you can use an allocation schedule that runs as part of a workflow process.</span></span>

> [!NOTE]
> <span data-ttu-id="cb126-123">Nemůžete používat mezipodniková pravidla pro přidělení hlavní knihy v plánu rozpočtu.</span><span class="sxs-lookup"><span data-stu-id="cb126-123">You can’t use intercompany ledger allocation rules for budget planning.</span></span>



[!INCLUDE[footer-include](../../includes/footer-banner.md)]