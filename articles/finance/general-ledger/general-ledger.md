---
title: Přehled hlavní knihy a finančního výkaznictví
description: Pomocí hlavní knihy definujte a spravujte finanční záznamy právnické osoby.
author: ShylaThompson
manager: AnnBe
ms.date: 08/14/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: GeneralJournalEntryWorkspace
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 65431
ms.assetid: d2c604df-daae-42cd-82d9-c80e3dee4a60
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 53d37d0a02b6771957e2516ef7e3b0bb277014a6
ms.sourcegitcommit: 71a7fb9e7133d872790ec25def5453bbbb17c627
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 09/25/2020
ms.locfileid: "3888125"
---
# <a name="general-ledger-home-page"></a><span data-ttu-id="b2b03-103">Domovská stránka hlavní knihy</span><span class="sxs-lookup"><span data-stu-id="b2b03-103">General ledger home page</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="b2b03-104">Pomocí hlavní knihy definujte a spravujte finanční záznamy právnické osoby.</span><span class="sxs-lookup"><span data-stu-id="b2b03-104">Use General ledger to define and manage the legal entity’s financial records.</span></span> <span data-ttu-id="b2b03-105">Hlavní kniha je registr položek na straně má dáti a dal.</span><span class="sxs-lookup"><span data-stu-id="b2b03-105">The general ledger is a register of debit and credit entries.</span></span> <span data-ttu-id="b2b03-106">Tyto položky jsou klasifikovány pomoc účtů, které jsou uvedeny v účtové osnově.</span><span class="sxs-lookup"><span data-stu-id="b2b03-106">These entries are classified using the accounts that are listed in a chart of accounts.</span></span> 

 - [<span data-ttu-id="b2b03-107">Plánování účetní osnovy</span><span class="sxs-lookup"><span data-stu-id="b2b03-107">Plan your chart of accounts</span></span>](plan-chart-of-accounts.md)
 - [<span data-ttu-id="b2b03-108">Typy hlavního účtu</span><span class="sxs-lookup"><span data-stu-id="b2b03-108">Main account types</span></span>](main-account-types.md)

<span data-ttu-id="b2b03-109">Můžete přidělovat nebo distribuovat peněžní částky na jeden či na více účtů nebo pro kombinace účet a dimenze na základě pravidel přidělení.</span><span class="sxs-lookup"><span data-stu-id="b2b03-109">You can allocate, or distribute, monetary amounts to one or more accounts or account and dimension combinations based on allocation rules.</span></span> <span data-ttu-id="b2b03-110">Existují dva typy přidělení: pevné a proměnné.</span><span class="sxs-lookup"><span data-stu-id="b2b03-110">There are two types of allocations: fixed and variable.</span></span> <span data-ttu-id="b2b03-111">Lze také vyrovnávat transakce mezi účty hlavní knihy a přeceňovat částky měn.</span><span class="sxs-lookup"><span data-stu-id="b2b03-111">You can also settle transactions between ledger accounts and revalue currency amounts.</span></span> <span data-ttu-id="b2b03-112">Na konci fiskálního roku musíte vygenerovat transakce uzávěrky a připravit účty na další fiskální rok.</span><span class="sxs-lookup"><span data-stu-id="b2b03-112">At the end of a fiscal year, you must generate closing transactions and prepare your accounts for the next fiscal year.</span></span> <span data-ttu-id="b2b03-113">Funkci konsolidace můžete použít ke kombinaci finančních výsledků několika dceřiných právnických osob do výsledků pro jednu konsolidovanou organizaci.</span><span class="sxs-lookup"><span data-stu-id="b2b03-113">You can use the consolidation functionality to combine the financial results for several subsidiary legal entities into results for a single, consolidated organization.</span></span> <span data-ttu-id="b2b03-114">Dceřiné společnosti mohou být umístěny ve stejné databázi nebo v samostatných databázích.</span><span class="sxs-lookup"><span data-stu-id="b2b03-114">The subsidiaries can be in the same database or in separate databases.</span></span>

- [<span data-ttu-id="b2b03-115">Přehled konsolidace a vyloučení</span><span class="sxs-lookup"><span data-stu-id="b2b03-115">Consolidation and elimination overview</span></span>](../budgeting/consolidation-elimination-overview.md)
- [<span data-ttu-id="b2b03-116">Účetní zůstatky hlavní knihy</span><span class="sxs-lookup"><span data-stu-id="b2b03-116">General ledger account balances</span></span>](general-ledger-account-balances.md)
- [<span data-ttu-id="b2b03-117">Finanční dimenze</span><span class="sxs-lookup"><span data-stu-id="b2b03-117">Financial dimensions</span></span>](financial-dimensions.md)

<span data-ttu-id="b2b03-118">[![Obchodní proces](./media/GL-process.PNG)](./media/GL-process.PNG)</span><span class="sxs-lookup"><span data-stu-id="b2b03-118">[![Business process](./media/GL-process.PNG)](./media/GL-process.PNG)</span></span>

## <a name="sales-tax"></a><span data-ttu-id="b2b03-119">DPH</span><span class="sxs-lookup"><span data-stu-id="b2b03-119">Sales tax</span></span>
<span data-ttu-id="b2b03-120">Každá společnost shromažďuje a odvádí daně různým finančním úřadům.</span><span class="sxs-lookup"><span data-stu-id="b2b03-120">Every company collects and pays taxes to various tax authorities.</span></span> <span data-ttu-id="b2b03-121">Pravidla a sazby se liší v jednotlivých zemích/regionech, státech, krajích a městech.</span><span class="sxs-lookup"><span data-stu-id="b2b03-121">The rules and rates vary by country/region, state, county, and city.</span></span>
<span data-ttu-id="b2b03-122">Kromě toho pravidla musí být aktualizována pravidelně, když finanční úřad změní jejich požadavky.</span><span class="sxs-lookup"><span data-stu-id="b2b03-122">In addition, the rules must be updated periodically when tax authorities change their requirements.</span></span> <span data-ttu-id="b2b03-123">Kódy DPH obsahují základní informace o způsobu výběru a odvádění daní finančním úřadům.</span><span class="sxs-lookup"><span data-stu-id="b2b03-123">Sales tax codes contain the basic information about how much you collect and pay to the authorities.</span></span> <span data-ttu-id="b2b03-124">Při nastavení daňových kódů je třeba definovat částky nebo procentuální hodnoty, které musí být vybrány.</span><span class="sxs-lookup"><span data-stu-id="b2b03-124">When you set up sales tax codes, you define the amounts or percentages that must be collected.</span></span> <span data-ttu-id="b2b03-125">Můžete také definovat různé metody, podle kterých se tyto částky nebo procentuální sazby uplatní na transakční částky.</span><span class="sxs-lookup"><span data-stu-id="b2b03-125">You also define the various methods by which those amounts or percentages are applied to transaction amounts.</span></span> <span data-ttu-id="b2b03-126">Témata v tomto oddílu poskytují informace o způsobu nastavení kódů DPH pro metody a sazby, které váš finanční úřad vyžaduje.</span><span class="sxs-lookup"><span data-stu-id="b2b03-126">The topics in this section provide information about how to set up sales tax codes for the methods and rates that your tax authorities require.</span></span>

 - [<span data-ttu-id="b2b03-127">Přehled DPH</span><span class="sxs-lookup"><span data-stu-id="b2b03-127">Sales tax overview</span></span>](indirect-taxes-overview.md)
 - [<span data-ttu-id="b2b03-128">Sazby DPH na základě polí Základ marže a Metody výpočtu</span><span class="sxs-lookup"><span data-stu-id="b2b03-128">Sales tax rates based on the Marginal base and Calculation methods</span></span>](marginal-base-field.md)
 - [<span data-ttu-id="b2b03-129">Platby DPH a pravidla zaokrouhlení</span><span class="sxs-lookup"><span data-stu-id="b2b03-129">Sales tax payments and rounding rules</span></span>](round-sales-tax-payments.md)


## <a name="additional-resources"></a><span data-ttu-id="b2b03-130">Další zdroje</span><span class="sxs-lookup"><span data-stu-id="b2b03-130">Additional resources</span></span>

#### <a name="whats-new-and-in-development"></a><span data-ttu-id="b2b03-131">Co je nového a na čem se pracuje</span><span class="sxs-lookup"><span data-stu-id="b2b03-131">What's new and in development</span></span>

<span data-ttu-id="b2b03-132">Přejděte na [plány vydání verzí aplikace Microsoft Dynamics 365](https://go.microsoft.com/fwlink/?linkid=2010158) a zjistěte, jaké nové funkce se plánují.</span><span class="sxs-lookup"><span data-stu-id="b2b03-132">Go to the [Microsoft Dynamics 365 release plans](https://go.microsoft.com/fwlink/?linkid=2010158) to see what new features have been planned.</span></span> 

#### <a name="financial-reporting"></a><span data-ttu-id="b2b03-133">Finanční výkaznictví</span><span class="sxs-lookup"><span data-stu-id="b2b03-133">Financial reporting</span></span>
<span data-ttu-id="b2b03-134">Přejděte na [Přehled Financial reporting](../../fin-ops-core/dev-itpro/analytics/financial-reporting-intro.md) téma pro informace o finančních zprávách.</span><span class="sxs-lookup"><span data-stu-id="b2b03-134">Go to the [Financial reporting overview](../../fin-ops-core/dev-itpro/analytics/financial-reporting-intro.md) topic for information about financial reports.</span></span>

#### <a name="blogs"></a><span data-ttu-id="b2b03-135">Blogy</span><span class="sxs-lookup"><span data-stu-id="b2b03-135">Blogs</span></span>

<span data-ttu-id="b2b03-136">Názory, novinky a jiné informace naleznete v [blogu Microsoft Dynamics 365](https://community.dynamics.com/b/msftdynamicsblog?c=Enterprise) a [Microsoft Dynamics 365 Finance and Operations - Finance](https://community.dynamics.com/365/financeandoperations/b/financials).</span><span class="sxs-lookup"><span data-stu-id="b2b03-136">You can find opinions, news, and other information on the [Microsoft Dynamics 365 blog](https://community.dynamics.com/b/msftdynamicsblog?c=Enterprise) and the [Microsoft Dynamics 365 Finance and Operations - Financials blog](https://community.dynamics.com/365/financeandoperations/b/financials).</span></span>

<span data-ttu-id="b2b03-137">[Microsoft Dynamics Operations Partner Community Blog](https://community.dynamics.com/partner/b/operationspartnercommunityblog) představuje pro partnery Microsoft Dynamics jediný zdroj informací o tom, co je nového a co se chystá v rámci Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="b2b03-137">The [Microsoft Dynamics Operations Partner Community Blog](https://community.dynamics.com/partner/b/operationspartnercommunityblog) gives Microsoft Dynamics Partners a single resource where they can learn what is new and trending in Dynamics 365.</span></span>

### <a name="videos"></a><span data-ttu-id="b2b03-138">Videa</span><span class="sxs-lookup"><span data-stu-id="b2b03-138">Videos</span></span>

<span data-ttu-id="b2b03-139">Prohlédněte si instruktážní videa, která jsou nyní k dispozici na [kanálu Microsoft Dynamics 365 YouTube](https://www.youtube.com/channel/UCJGCg4rB3QSs8y_1FquelBQ).</span><span class="sxs-lookup"><span data-stu-id="b2b03-139">Check out the how-to videos that are now available on the [Microsoft Dynamics 365 YouTube Channel](https://www.youtube.com/channel/UCJGCg4rB3QSs8y_1FquelBQ).</span></span>

#### <a name="community-blogs"></a><span data-ttu-id="b2b03-140">Blogy komunity</span><span class="sxs-lookup"><span data-stu-id="b2b03-140">Community blogs</span></span>

- [<span data-ttu-id="b2b03-141">Důležité informace o hlavní knize v Dynamics 365 for Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="b2b03-141">What you should know about ledger in Dynamics 365 for Finance and Operations</span></span>](https://financefunction.tech/2018/04/29/what-you-should-know-about-ledger-in-dynamics-365-for-finance-and-operations)

