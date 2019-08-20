---
title: Domovská stránka Hlavní kniha a Finanční výkaznictví
description: Pomocí hlavní knihy definujte a spravujte finanční záznamy právnické osoby.
author: ShylaThompson
manager: AnnBe
ms.date: 08/31/2017
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
ms.openlocfilehash: ee8597dfbb8b86ff770516ac8787fb07f1d4cbd5
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/01/2019
ms.locfileid: "1839128"
---
# <a name="general-ledger"></a><span data-ttu-id="66189-103">Hlavní kniha</span><span class="sxs-lookup"><span data-stu-id="66189-103">General ledger</span></span> 

[!include [banner](../includes/banner.md)]

<span data-ttu-id="66189-104">Pomocí hlavní knihy definujte a spravujte finanční záznamy právnické osoby.</span><span class="sxs-lookup"><span data-stu-id="66189-104">Use General ledger to define and manage the legal entity’s financial records.</span></span> <span data-ttu-id="66189-105">Hlavní kniha je registr položek na straně má dáti a dal.</span><span class="sxs-lookup"><span data-stu-id="66189-105">The general ledger is a register of debit and credit entries.</span></span> <span data-ttu-id="66189-106">Tyto položky jsou klasifikovány pomoc účtů, které jsou uvedeny v účtové osnově.</span><span class="sxs-lookup"><span data-stu-id="66189-106">These entries are classified using the accounts that are listed in a chart of accounts.</span></span> 

 - [<span data-ttu-id="66189-107">Plánování účetní osnovy</span><span class="sxs-lookup"><span data-stu-id="66189-107">Plan your chart of accounts</span></span>](plan-chart-of-accounts.md)
 - [<span data-ttu-id="66189-108">Typy hlavního účtu</span><span class="sxs-lookup"><span data-stu-id="66189-108">Main account types</span></span>](main-account-types.md)

<span data-ttu-id="66189-109">Můžete přidělovat nebo distribuovat peněžní částky na jeden či na více účtů nebo pro kombinace účet a dimenze na základě pravidel přidělení.</span><span class="sxs-lookup"><span data-stu-id="66189-109">You can allocate, or distribute, monetary amounts to one or more accounts or account and dimension combinations based on allocation rules.</span></span> <span data-ttu-id="66189-110">Existují dva typy přidělení: pevné a proměnné.</span><span class="sxs-lookup"><span data-stu-id="66189-110">There are two types of allocations: fixed and variable.</span></span> <span data-ttu-id="66189-111">Lze také vyrovnávat transakce mezi účty hlavní knihy a přeceňovat částky měn.</span><span class="sxs-lookup"><span data-stu-id="66189-111">You can also settle transactions between ledger accounts and revalue currency amounts.</span></span> <span data-ttu-id="66189-112">Na konci fiskálního roku musíte vygenerovat transakce uzávěrky a připravit účty na další fiskální rok.</span><span class="sxs-lookup"><span data-stu-id="66189-112">At the end of a fiscal year, you must generate closing transactions and prepare your accounts for the next fiscal year.</span></span> <span data-ttu-id="66189-113">Funkci konsolidace můžete použít ke kombinaci finančních výsledků několika dceřiných právnických osob do výsledků pro jednu konsolidovanou organizaci.</span><span class="sxs-lookup"><span data-stu-id="66189-113">You can use the consolidation functionality to combine the financial results for several subsidiary legal entities into results for a single, consolidated organization.</span></span> <span data-ttu-id="66189-114">Dceřiné společnosti mohou být umístěny ve stejné databázi Microsoft Dynamics 365 for Finance and Operations nebo v samostatných databázích.</span><span class="sxs-lookup"><span data-stu-id="66189-114">The subsidiaries can be in the same Microsoft Dynamics 365 for Finance and Operations database or in separate databases.</span></span>

- [<span data-ttu-id="66189-115">Přehled konsolidace a vyloučení</span><span class="sxs-lookup"><span data-stu-id="66189-115">Consolidation and elimination overview</span></span>](../budgeting/consolidation-elimination-overview.md)
- [<span data-ttu-id="66189-116">Účetní zůstatky hlavní knihy</span><span class="sxs-lookup"><span data-stu-id="66189-116">General ledger account balances</span></span>](general-ledger-account-balances.md)
- [<span data-ttu-id="66189-117">Finanční dimenze</span><span class="sxs-lookup"><span data-stu-id="66189-117">Financial dimensions</span></span>](financial-dimensions.md)

<span data-ttu-id="66189-118">[![Obchodní proces](./media/GL-process.PNG)](./media/GL-process.PNG)</span><span class="sxs-lookup"><span data-stu-id="66189-118">[![Business process](./media/GL-process.PNG)](./media/GL-process.PNG)</span></span>

## <a name="sales-tax"></a><span data-ttu-id="66189-119">DPH</span><span class="sxs-lookup"><span data-stu-id="66189-119">Sales tax</span></span>
<span data-ttu-id="66189-120">Každá společnost shromažďuje a odvádí daně různým finančním úřadům.</span><span class="sxs-lookup"><span data-stu-id="66189-120">Every company collects and pays taxes to various tax authorities.</span></span> <span data-ttu-id="66189-121">Pravidla a sazby se liší v jednotlivých zemích/regionech, státech, krajích a městech.</span><span class="sxs-lookup"><span data-stu-id="66189-121">The rules and rates vary by country/region, state, county, and city.</span></span>
<span data-ttu-id="66189-122">Kromě toho pravidla musí být aktualizována pravidelně, když finanční úřad změní jejich požadavky.</span><span class="sxs-lookup"><span data-stu-id="66189-122">In addition, the rules must be updated periodically when tax authorities change their requirements.</span></span> <span data-ttu-id="66189-123">Kódy DPH obsahují základní informace o způsobu výběru a odvádění daní finančním úřadům.</span><span class="sxs-lookup"><span data-stu-id="66189-123">Sales tax codes contain the basic information about how much you collect and pay to the authorities.</span></span> <span data-ttu-id="66189-124">Při nastavení daňových kódů je třeba definovat částky nebo procentuální hodnoty, které musí být vybrány.</span><span class="sxs-lookup"><span data-stu-id="66189-124">When you set up sales tax codes, you define the amounts or percentages that must be collected.</span></span> <span data-ttu-id="66189-125">Můžete také definovat různé metody, podle kterých se tyto částky nebo procentuální sazby uplatní na transakční částky.</span><span class="sxs-lookup"><span data-stu-id="66189-125">You also define the various methods by which those amounts or percentages are applied to transaction amounts.</span></span> <span data-ttu-id="66189-126">Témata v tomto oddílu poskytují informace o způsobu nastavení kódů DPH pro metody a sazby, které váš finanční úřad vyžaduje.</span><span class="sxs-lookup"><span data-stu-id="66189-126">The topics in this section provide information about how to set up sales tax codes for the methods and rates that your tax authorities require.</span></span>

 - [<span data-ttu-id="66189-127">Přehled DPH</span><span class="sxs-lookup"><span data-stu-id="66189-127">Sales tax overview</span></span>](indirect-taxes-overview.md)
 - [<span data-ttu-id="66189-128">Sazby DPH na základě polí Základ marže a Metody výpočtu</span><span class="sxs-lookup"><span data-stu-id="66189-128">Sales tax rates based on the Marginal base and Calculation methods</span></span>](marginal-base-field.md)
 - [<span data-ttu-id="66189-129">Platby DPH a pravidla zaokrouhlení</span><span class="sxs-lookup"><span data-stu-id="66189-129">Sales tax payments and rounding rules</span></span>](round-sales-tax-payments.md)


## <a name="additional-resources"></a><span data-ttu-id="66189-130">Další zdroje</span><span class="sxs-lookup"><span data-stu-id="66189-130">Additional resources</span></span>

#### <a name="whats-new-and-in-development"></a><span data-ttu-id="66189-131">Co je nového a na čem se pracuje</span><span class="sxs-lookup"><span data-stu-id="66189-131">What's new and in development</span></span>

<span data-ttu-id="66189-132">Přejděte [poznámky k verzi aplikace Microsoft Dynamics 365](https://go.microsoft.com/fwlink/?linkid=2010158) a zjistěte, jaké nové funkce se plánují.</span><span class="sxs-lookup"><span data-stu-id="66189-132">Go to the [Microsoft Dynamics 365 Release Notes](https://go.microsoft.com/fwlink/?linkid=2010158) to see what new features have been planned.</span></span> 

#### <a name="blogs"></a><span data-ttu-id="66189-133">Blogy</span><span class="sxs-lookup"><span data-stu-id="66189-133">Blogs</span></span>

<span data-ttu-id="66189-134">Názory, novinky a jiné informace naleznete na [blogu Microsoft Dynamics 365](https://community.dynamics.com/b/msftdynamicsblog?c=Enterprise) a [blogu Microsoft Dynamics 365 Finance and Operations - Financials](https://community.dynamics.com/365/financeandoperations/b/financials).</span><span class="sxs-lookup"><span data-stu-id="66189-134">You can find opinions, news, and other information on the [Microsoft Dynamics 365 blog](https://community.dynamics.com/b/msftdynamicsblog?c=Enterprise) and the [Microsoft Dynamics 365 Finance and Operations - Financials blog](https://community.dynamics.com/365/financeandoperations/b/financials).</span></span>

<span data-ttu-id="66189-135">[Microsoft Dynamics Operations Partner Community Blog](https://community.dynamics.com/partner/b/operationspartnercommunityblog) představuje pro partnery Microsoft Dynamics jediný zdroj informací o tom, co je nového a co se chystá v rámci MBS Operations.</span><span class="sxs-lookup"><span data-stu-id="66189-135">The [Microsoft Dynamics Operations Partner Community Blog](https://community.dynamics.com/partner/b/operationspartnercommunityblog) gives Microsoft Dynamics Partners a single resource where they can learn what is new and trending in MBS Operations.</span></span>

### <a name="videos"></a><span data-ttu-id="66189-136">Videa</span><span class="sxs-lookup"><span data-stu-id="66189-136">Videos</span></span>

<span data-ttu-id="66189-137">Prohlédněte si instruktážní videa, která jsou nyní k dispozici na [kanálu Microsoft Dynamics 365 YouTube](https://www.youtube.com/channel/UCJGCg4rB3QSs8y_1FquelBQ).</span><span class="sxs-lookup"><span data-stu-id="66189-137">Check out the how-to videos that are now available on the [Microsoft Dynamics 365 YouTube Channel](https://www.youtube.com/channel/UCJGCg4rB3QSs8y_1FquelBQ).</span></span>

#### <a name="community-blogs"></a><span data-ttu-id="66189-138">Blogy komunity</span><span class="sxs-lookup"><span data-stu-id="66189-138">Community blogs</span></span>

- [<span data-ttu-id="66189-139">Důležité informace o hlavní knize v Dynamics 365 for Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="66189-139">What you should know about ledger in Dynamics 365 for Finance and Operations</span></span>](https://financefunction.tech/2018/04/29/what-you-should-know-about-ledger-in-dynamics-365-for-finance-and-operations)

