---
title: "Domovská stránka Hlavní kniha a Finanční výkaznictví"
description: "Pomocí hlavní knihy definujte a spravujte finanční záznamy právnické osoby. Hlavní kniha je registr položek na straně má dáti a dal. Tyto položky jsou klasifikovány pomoc účtů, které jsou uvedeny v účtové osnově."
author: twheeloc
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 65431
ms.assetid: d2c604df-daae-42cd-82d9-c80e3dee4a60
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: 08c38aada355583c5a6872f75b57db95d9b81786
ms.openlocfilehash: 78f3d9c27767c089ac686f333cae3cb50c03ee18
ms.contentlocale: cs-cz
ms.lasthandoff: 07/18/2017

---

# <a name="general-ledger"></a><span data-ttu-id="e7118-105">Hlavní kniha</span><span class="sxs-lookup"><span data-stu-id="e7118-105">General ledger</span></span> 

[!include[banner](../includes/banner.md)]


<span data-ttu-id="e7118-106">Pomocí hlavní knihy definujte a spravujte finanční záznamy právnické osoby.</span><span class="sxs-lookup"><span data-stu-id="e7118-106">Use General ledger to define and manage the legal entity’s financial records.</span></span> <span data-ttu-id="e7118-107">Hlavní kniha je registr položek na straně má dáti a dal.</span><span class="sxs-lookup"><span data-stu-id="e7118-107">The general ledger is a register of debit and credit entries.</span></span> <span data-ttu-id="e7118-108">Tyto položky jsou klasifikovány pomoc účtů, které jsou uvedeny v účtové osnově.</span><span class="sxs-lookup"><span data-stu-id="e7118-108">These entries are classified using the accounts that are listed in a chart of accounts.</span></span> 

<span data-ttu-id="e7118-109">Můžete přidělovat nebo distribuovat peněžní částky na jeden či na více účtů nebo pro kombinace účet a dimenze na základě pravidel přidělení.</span><span class="sxs-lookup"><span data-stu-id="e7118-109">You can allocate, or distribute, monetary amounts to one or more accounts or account and dimension combinations based on allocation rules.</span></span> <span data-ttu-id="e7118-110">Existují dva typy přidělení: pevné a proměnné.</span><span class="sxs-lookup"><span data-stu-id="e7118-110">There are two types of allocations: fixed and variable.</span></span> <span data-ttu-id="e7118-111">Lze také vyrovnávat transakce mezi účty hlavní knihy a přeceňovat částky měn.</span><span class="sxs-lookup"><span data-stu-id="e7118-111">You can also settle transactions between ledger accounts and revalue currency amounts.</span></span> <span data-ttu-id="e7118-112">Na konci fiskálního roku musíte vygenerovat transakce uzávěrky a připravit účty na další fiskální rok.</span><span class="sxs-lookup"><span data-stu-id="e7118-112">At the end of a fiscal year, you must generate closing transactions and prepare your accounts for the next fiscal year.</span></span> <span data-ttu-id="e7118-113">Funkci konsolidace můžete použít ke kombinaci finančních výsledků několika dceřiných právnických osob do výsledků pro jednu konsolidovanou organizaci.</span><span class="sxs-lookup"><span data-stu-id="e7118-113">You can use the consolidation functionality to combine the financial results for several subsidiary legal entities into results for a single, consolidated organization.</span></span> <span data-ttu-id="e7118-114">Dceřiné společnosti mohou být umístěny ve stejné databázi aplikace Microsoft Dynamics 365 for Finance and Operations nebo v samostatných databázích.</span><span class="sxs-lookup"><span data-stu-id="e7118-114">The subsidiaries can be in the same Microsoft Dynamics 365 for Finance and Operations database or in separate databases.</span></span>

# <a name="sales-tax"></a><span data-ttu-id="e7118-115">DPH</span><span class="sxs-lookup"><span data-stu-id="e7118-115">Sales tax</span></span>
<span data-ttu-id="e7118-116">Každá společnost shromažďuje a odvádí daně různým finančním úřadům.</span><span class="sxs-lookup"><span data-stu-id="e7118-116">Every company collects and pays taxes to various tax authorities.</span></span> <span data-ttu-id="e7118-117">Pravidla a sazby se liší v jednotlivých zemích/regionech, státech, krajích a městech.</span><span class="sxs-lookup"><span data-stu-id="e7118-117">The rules and rates vary by country/region, state, county, and city.</span></span> <span data-ttu-id="e7118-118">Kromě toho pravidla musí být aktualizována pravidelně, když finanční úřad změní jejich požadavky.</span><span class="sxs-lookup"><span data-stu-id="e7118-118">In addition, the rules must be updated periodically when tax authorities change their requirements.</span></span> <span data-ttu-id="e7118-119">Kódy DPH obsahují základní informace o způsobu výběru a odvádění daní finančním úřadům.</span><span class="sxs-lookup"><span data-stu-id="e7118-119">Sales tax codes contain the basic information about how much you collect and pay to the authorities.</span></span> <span data-ttu-id="e7118-120">Při nastavení daňových kódů je třeba definovat částky nebo procentuální hodnoty, které musí být vybrány.</span><span class="sxs-lookup"><span data-stu-id="e7118-120">When you set up sales tax codes, you define the amounts or percentages that must be collected.</span></span> <span data-ttu-id="e7118-121">Můžete také definovat různé metody, podle kterých se tyto částky nebo procentuální sazby uplatní na transakční částky.</span><span class="sxs-lookup"><span data-stu-id="e7118-121">You also define the various methods by which those amounts or percentages are applied to transaction amounts.</span></span> <span data-ttu-id="e7118-122">Témata v tomto oddílu poskytují informace o způsobu nastavení kódů DPH pro metody a sazby, které váš finanční úřad vyžaduje.</span><span class="sxs-lookup"><span data-stu-id="e7118-122">The topics in this section provide information about how to set up sales tax codes for the methods and rates that your tax authorities require.</span></span>







