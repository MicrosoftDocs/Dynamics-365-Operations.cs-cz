---
title: "Domovská stránka Hlavní kniha a Finanční výkaznictví"
description: "Pomocí hlavní knihy definujte a spravujte finanční záznamy právnické osoby."
author: twheeloc
manager: AnnBe
ms.date: 08/31/2017
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
ms.translationtype: HT
ms.sourcegitcommit: fc8102d945faf9ad533f57ec1a45b0e0dc344963
ms.openlocfilehash: 2f52f4afbdd90b3f6a9a42f0fc85c3e083f0cf30
ms.contentlocale: cs-cz
ms.lasthandoff: 09/29/2017

---

# <a name="general-ledger"></a><span data-ttu-id="3eb96-103">Hlavní kniha</span><span class="sxs-lookup"><span data-stu-id="3eb96-103">General ledger</span></span> 

[!include[banner](../includes/banner.md)]


<span data-ttu-id="3eb96-104">Pomocí hlavní knihy definujte a spravujte finanční záznamy právnické osoby.</span><span class="sxs-lookup"><span data-stu-id="3eb96-104">Use General ledger to define and manage the legal entity’s financial records.</span></span> <span data-ttu-id="3eb96-105">Hlavní kniha je registr položek na straně má dáti a dal.</span><span class="sxs-lookup"><span data-stu-id="3eb96-105">The general ledger is a register of debit and credit entries.</span></span> <span data-ttu-id="3eb96-106">Tyto položky jsou klasifikovány pomoc účtů, které jsou uvedeny v účtové osnově.</span><span class="sxs-lookup"><span data-stu-id="3eb96-106">These entries are classified using the accounts that are listed in a chart of accounts.</span></span> 

 - [<span data-ttu-id="3eb96-107">Plánování účetní osnovy</span><span class="sxs-lookup"><span data-stu-id="3eb96-107">Plan your chart of accounts</span></span>](plan-chart-of-accounts.md)
 - [<span data-ttu-id="3eb96-108">Typy hlavního účtu</span><span class="sxs-lookup"><span data-stu-id="3eb96-108">Main account types</span></span>](main-account-types.md)

<span data-ttu-id="3eb96-109">Můžete přidělovat nebo distribuovat peněžní částky na jeden či na více účtů nebo pro kombinace účet a dimenze na základě pravidel přidělení.</span><span class="sxs-lookup"><span data-stu-id="3eb96-109">You can allocate, or distribute, monetary amounts to one or more accounts or account and dimension combinations based on allocation rules.</span></span> <span data-ttu-id="3eb96-110">Existují dva typy přidělení: pevné a proměnné.</span><span class="sxs-lookup"><span data-stu-id="3eb96-110">There are two types of allocations: fixed and variable.</span></span> <span data-ttu-id="3eb96-111">Lze také vyrovnávat transakce mezi účty hlavní knihy a přeceňovat částky měn.</span><span class="sxs-lookup"><span data-stu-id="3eb96-111">You can also settle transactions between ledger accounts and revalue currency amounts.</span></span> <span data-ttu-id="3eb96-112">Na konci fiskálního roku musíte vygenerovat transakce uzávěrky a připravit účty na další fiskální rok.</span><span class="sxs-lookup"><span data-stu-id="3eb96-112">At the end of a fiscal year, you must generate closing transactions and prepare your accounts for the next fiscal year.</span></span> <span data-ttu-id="3eb96-113">Funkci konsolidace můžete použít ke kombinaci finančních výsledků několika dceřiných právnických osob do výsledků pro jednu konsolidovanou organizaci.</span><span class="sxs-lookup"><span data-stu-id="3eb96-113">You can use the consolidation functionality to combine the financial results for several subsidiary legal entities into results for a single, consolidated organization.</span></span> <span data-ttu-id="3eb96-114">Dceřiné společnosti mohou být umístěny ve stejné databázi aplikace Microsoft Dynamics 365 for Finance and Operations nebo v samostatných databázích.</span><span class="sxs-lookup"><span data-stu-id="3eb96-114">The subsidiaries can be in the same Microsoft Dynamics 365 for Finance and Operations database or in separate databases.</span></span>

- [<span data-ttu-id="3eb96-115">Přehled konsolidace a vyloučení</span><span class="sxs-lookup"><span data-stu-id="3eb96-115">Consolidation and elimination overview</span></span>](../budgeting/consolidation-elimination-overview.md)
- [<span data-ttu-id="3eb96-116">Účetní zůstatky hlavní knihy</span><span class="sxs-lookup"><span data-stu-id="3eb96-116">General ledger account balances</span></span>](general-ledger-account-balances.md)
- [<span data-ttu-id="3eb96-117">Finanční dimenze</span><span class="sxs-lookup"><span data-stu-id="3eb96-117">Financial dimensions</span></span>](financial-dimensions.md)

<span data-ttu-id="3eb96-118">[![Obchodní proces](./media/GL-process.PNG)](./media/GL-process.PNG)</span><span class="sxs-lookup"><span data-stu-id="3eb96-118">[![Business process](./media/GL-process.PNG)](./media/GL-process.PNG)</span></span>

# <a name="sales-tax"></a><span data-ttu-id="3eb96-119">DPH</span><span class="sxs-lookup"><span data-stu-id="3eb96-119">Sales tax</span></span>
<span data-ttu-id="3eb96-120">Každá společnost shromažďuje a odvádí daně různým finančním úřadům.</span><span class="sxs-lookup"><span data-stu-id="3eb96-120">Every company collects and pays taxes to various tax authorities.</span></span> <span data-ttu-id="3eb96-121">Pravidla a sazby se liší v jednotlivých zemích/regionech, státech, krajích a městech.</span><span class="sxs-lookup"><span data-stu-id="3eb96-121">The rules and rates vary by country/region, state, county, and city.</span></span>
<span data-ttu-id="3eb96-122">Kromě toho pravidla musí být aktualizována pravidelně, když finanční úřad změní jejich požadavky.</span><span class="sxs-lookup"><span data-stu-id="3eb96-122">In addition, the rules must be updated periodically when tax authorities change their requirements.</span></span> <span data-ttu-id="3eb96-123">Kódy DPH obsahují základní informace o způsobu výběru a odvádění daní finančním úřadům.</span><span class="sxs-lookup"><span data-stu-id="3eb96-123">Sales tax codes contain the basic information about how much you collect and pay to the authorities.</span></span> <span data-ttu-id="3eb96-124">Při nastavení daňových kódů je třeba definovat částky nebo procentuální hodnoty, které musí být vybrány.</span><span class="sxs-lookup"><span data-stu-id="3eb96-124">When you set up sales tax codes, you define the amounts or percentages that must be collected.</span></span> <span data-ttu-id="3eb96-125">Můžete také definovat různé metody, podle kterých se tyto částky nebo procentuální sazby uplatní na transakční částky.</span><span class="sxs-lookup"><span data-stu-id="3eb96-125">You also define the various methods by which those amounts or percentages are applied to transaction amounts.</span></span> <span data-ttu-id="3eb96-126">Témata v tomto oddílu poskytují informace o způsobu nastavení kódů DPH pro metody a sazby, které váš finanční úřad vyžaduje.</span><span class="sxs-lookup"><span data-stu-id="3eb96-126">The topics in this section provide information about how to set up sales tax codes for the methods and rates that your tax authorities require.</span></span>

 - [<span data-ttu-id="3eb96-127">Přehled DPH</span><span class="sxs-lookup"><span data-stu-id="3eb96-127">Sales tax overview</span></span>](indirect-taxes-overview.md)
 - [<span data-ttu-id="3eb96-128">Sazby DPH na základě polí Základ marže a Metody výpočtu</span><span class="sxs-lookup"><span data-stu-id="3eb96-128">Sales tax rates based on the Marginal base and Calculation methods</span></span>](marginal-base-field.md)
 - [<span data-ttu-id="3eb96-129">Platby DPH a pravidla zaokrouhlení</span><span class="sxs-lookup"><span data-stu-id="3eb96-129">Sales tax payments and rounding rules</span></span>](round-sales-tax-payments.md)


### <a name="additional-resources"></a><span data-ttu-id="3eb96-130">Další zdroje</span><span class="sxs-lookup"><span data-stu-id="3eb96-130">Additional resources</span></span>

#### <a name="whats-new-and-in-development"></a><span data-ttu-id="3eb96-131">Co je nového a na čem se pracuje</span><span class="sxs-lookup"><span data-stu-id="3eb96-131">What's new and in development</span></span>

<span data-ttu-id="3eb96-132">Přejděte na [Microsoft Dynamics 365 Roadmap](https://roadmap.dynamics.com/) a zjistěte, jaké nové funkce se vydávají a jaké se chystají.</span><span class="sxs-lookup"><span data-stu-id="3eb96-132">Go to the [Microsoft Dynamics 365 Roadmap](https://roadmap.dynamics.com/) to see what new features have been released and what new features are in development.</span></span> 

#### <a name="blogs"></a><span data-ttu-id="3eb96-133">Blogy</span><span class="sxs-lookup"><span data-stu-id="3eb96-133">Blogs</span></span>

<span data-ttu-id="3eb96-134">Názory, novinky a jiné informace o modulu Závazky a jiných řešeních naleznete v [blogu Microsoft Dynamics 365](https://community.dynamics.com/b/msftdynamicsblog?c=Enterprise).</span><span class="sxs-lookup"><span data-stu-id="3eb96-134">You can find opinions, news, and other information about Accounts payable and other solutions on the [Microsoft Dynamics 365 blog](https://community.dynamics.com/b/msftdynamicsblog?c=Enterprise).</span></span>

<span data-ttu-id="3eb96-135">Existuje mnoho příspěvků o modulu Hlavní kniha na [blogu týmu produktu Microsoft Dynamics AX](https://blogs.msdn.microsoft.com/dax/).</span><span class="sxs-lookup"><span data-stu-id="3eb96-135">There are many posts about General ledger on the [Microsoft Dynamics AX product team blog](https://blogs.msdn.microsoft.com/dax/).</span></span> <span data-ttu-id="3eb96-136">Ačkoliv některé z těchto článků byly vytvořeny pro předchozí verzi modulu Hlavní kniha, stále se používají stejné koncepty a postupy jsou podobné jako v aktuální verzi.</span><span class="sxs-lookup"><span data-stu-id="3eb96-136">Although some of these posts were written for the previous version of General ledger, the same concepts still apply, and the procedures are also similar in the current version.</span></span>

<span data-ttu-id="3eb96-137">[Microsoft Dynamics Operations Partner Community Blog](https://community.dynamics.com/partner/b/operationspartnercommunityblog) představuje pro partnery Microsoft Dynamics jediný zdroj informací o tom, co je nového a co se chystá v rámci MBS Operations.</span><span class="sxs-lookup"><span data-stu-id="3eb96-137">The [Microsoft Dynamics Operations Partner Community Blog](https://community.dynamics.com/partner/b/operationspartnercommunityblog) gives Microsoft Dynamics Partners a single resource where they can learn what is new and trending in MBS Operations.</span></span>

#### <a name="task-guides"></a><span data-ttu-id="3eb96-138">Průvodci záznamem úloh</span><span class="sxs-lookup"><span data-stu-id="3eb96-138">Task guides</span></span>
<span data-ttu-id="3eb96-139">V aplikaci Finance and Operations je k dispozici další nápověda v podobě průvodců záznamem úloh.</span><span class="sxs-lookup"><span data-stu-id="3eb96-139">Additional help is available as task guides inside Finance and Operations.</span></span> <span data-ttu-id="3eb96-140">Průvodce záznamem úloh zobrazíte kliknutím na tlačítko Nápověda na kterékoliv stránce.</span><span class="sxs-lookup"><span data-stu-id="3eb96-140">To access task guides, click the Help button on any page.</span></span>

#### <a name="videos"></a><span data-ttu-id="3eb96-141">Videa</span><span class="sxs-lookup"><span data-stu-id="3eb96-141">Videos</span></span>

<span data-ttu-id="3eb96-142">Prohlédněte si instruktážní videa, která jsou nyní k dispozici na kanálu [Microsoft Dynamics 365 YouTube Channel](https://www.youtube.com/channel/UCJGCg4rB3QSs8y_1FquelBQ).</span><span class="sxs-lookup"><span data-stu-id="3eb96-142">Check out the how-to videos that are now available on the [Microsoft Dynamics 365 YouTube Channel](https://www.youtube.com/channel/UCJGCg4rB3QSs8y_1FquelBQ).</span></span>


