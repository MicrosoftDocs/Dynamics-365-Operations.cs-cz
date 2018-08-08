---
title: "Zpracování přidělení"
description: "Tento článek obsahuje informace o přiděleních, možnostech pro jejich zpracování v aplikaci Microsoft Dynamics 365 for Finance and Operations a o tom, jak je lze použít při plánování rozpočtu. Přidělení se používají k rozdělení částek mezi více kombinací účtů hlavní knihy. Díky nim lze zajistit, aby se výdaje nebo příjmy účtovaly v účetnictví na správný objekt."
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: AccountingDistribution, LedgerAllocationRule, MainAccount
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 17361
ms.assetid: 04c8548a-0af9-492b-954b-946b4f8ca023
ms.search.region: Global
ms.author: peakerbl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: d9747ba144d56c9410846769e5465372c89ea111
ms.openlocfilehash: ac531726e04ebec4da9062f47726568723364cce
ms.contentlocale: cs-cz
ms.lasthandoff: 08/07/2018

---

# <a name="process-allocations"></a><span data-ttu-id="b56ce-105">Zpracování přidělení</span><span class="sxs-lookup"><span data-stu-id="b56ce-105">Process allocations</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="b56ce-106">Tento článek obsahuje informace o přiděleních, možnostech pro jejich zpracování v aplikaci Microsoft Dynamics 365 for Finance and Operations a o tom, jak je lze použít při plánování rozpočtu.</span><span class="sxs-lookup"><span data-stu-id="b56ce-106">This article provides information about allocations, the options for processing them in Microsoft Dynamics 365 for Finance and Operations, and how they can be used in budget planning.</span></span> <span data-ttu-id="b56ce-107">Přidělení se používají k rozdělení částek mezi více kombinací účtů hlavní knihy.</span><span class="sxs-lookup"><span data-stu-id="b56ce-107">Allocations are used to distribute amounts across multiple ledger account combinations.</span></span> <span data-ttu-id="b56ce-108">Díky nim lze zajistit, aby se výdaje nebo příjmy účtovaly v účetnictví na správný objekt.</span><span class="sxs-lookup"><span data-stu-id="b56ce-108">They help guarantee that expenses or revenue is charged to the correct object in accounting.</span></span>

<span data-ttu-id="b56ce-109">Microsoft Dynamics 365 for Finance and Operations poskytuje pro podporu tohoto procesu následující možnosti:</span><span class="sxs-lookup"><span data-stu-id="b56ce-109">Microsoft Dynamics 365 for Finance and Operations provides the following capabilities to support this process:</span></span>

-   <span data-ttu-id="b56ce-110">Ručně přidělit částky transakcí pomocí rozdělení akcí v rozúčtování nebo použitím výchozích šablon finanční dimenze v dokumentu.</span><span class="sxs-lookup"><span data-stu-id="b56ce-110">Manually allocate transaction amounts by using the Split action in accounting distributions, or by applying financial dimension default templates to a document.</span></span> <span data-ttu-id="b56ce-111">Další informace naleznete v tématu [Rozúčtování.](../accounts-payable/accounting-distributions.md)</span><span class="sxs-lookup"><span data-stu-id="b56ce-111">For more information, see [Accounting distributions.](../accounts-payable/accounting-distributions.md)</span></span>
-   <span data-ttu-id="b56ce-112">Automaticky přidělit částky transakce na základě podmínek přidělení definovaných v individuálním hlavním účtu.</span><span class="sxs-lookup"><span data-stu-id="b56ce-112">Automatically allocate transactions amounts based on allocation terms defined on individual main account.</span></span> <span data-ttu-id="b56ce-113">Položky účtu přidělení se budou generovat pro každý deník podle procenta a cílového účtu hlavní knihy, kdykoli účetní položka splní kritéria definovaná jako zdrojový účet hlavní knihy.</span><span class="sxs-lookup"><span data-stu-id="b56ce-113">Allocation account entries will be generated for each journal based on the percentage and destination ledger account whenever an accounting entry meets the criteria defined as the source ledger account.</span></span>
-   <span data-ttu-id="b56ce-114">Automaticky přidělit zůstatky hlavní knihy nebo pevné částky na základě pravidel přidělení hlavní knihy.</span><span class="sxs-lookup"><span data-stu-id="b56ce-114">Automatically allocate ledger balances or fixed amounts based on ledger allocation rules.</span></span> <span data-ttu-id="b56ce-115">Pravidla přidělení hlavní knihy se zpracovávají v pravidelných intervalech pomocí deníků přidělení.</span><span class="sxs-lookup"><span data-stu-id="b56ce-115">The ledger allocation rules are processed on a periodic basis using allocation journals.</span></span> 

###  <a name="allocations-in-budget-planning"></a><span data-ttu-id="b56ce-116">Přidělení v plánování rozpočtu</span><span class="sxs-lookup"><span data-stu-id="b56ce-116">Allocations in budget planning</span></span>

<span data-ttu-id="b56ce-117">Pravidla přidělení hlavní knihy můžete použít pro plány rozpočtu.</span><span class="sxs-lookup"><span data-stu-id="b56ce-117">Ledger allocation rules can be used for budget plans.</span></span> <span data-ttu-id="b56ce-118">Při použití pravidla přidělení hlavní knihy v plánování rozpočtu, pravidla přidělení fungují stejným způsobem jako v hlavní knize, ale zdrojová data a cílová data pocházejí z plánu rozpočtu.</span><span class="sxs-lookup"><span data-stu-id="b56ce-118">When you use ledger allocation rules in budget planning, the allocation rules work the same way they would in the ledger, but the source data and destination data comes from the budget plan.</span></span> <span data-ttu-id="b56ce-119">Můžete ručně vybrat pravidla pro přidělení hlavní knihy pro použití v plánu rozpočtu.</span><span class="sxs-lookup"><span data-stu-id="b56ce-119">You can manually select ledger allocation rules to use for budget plans.</span></span> <span data-ttu-id="b56ce-120">Můžete také použít plán přidělení, která se spouští jako součást procesu workflowu.</span><span class="sxs-lookup"><span data-stu-id="b56ce-120">Alternatively, you can use an allocation schedule that runs as part of a workflow process.</span></span>

> [!NOTE]
> <span data-ttu-id="b56ce-121">Nemůžete používat mezipodniková pravidla pro přidělení hlavní knihy v plánu rozpočtu.</span><span class="sxs-lookup"><span data-stu-id="b56ce-121">You can’t use intercompany ledger allocation rules for budget planning.</span></span>






