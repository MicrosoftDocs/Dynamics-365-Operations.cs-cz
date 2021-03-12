---
title: Vytváření rozpočtu z účtů transakcí a součtových účtů
description: V tomto článku je přehled procesu vytváření rozpočtů na základě součtových účtů. Také vysvětluje, jak lze zapnout kontrolu rozpočtu pro součtové účty, jestliže je požadována kontrola rozpočtu.
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: BudgetControlConfiguration, BudgetPlanGenerate
audience: Application User
ms.reviewer: roschlom
ms.custom: 13051
ms.assetid: fb1bb2d3-445c-402f-a9a3-aa6503eed78e
ms.search.region: Global
ms.author: sigitac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 2c2298a774e35bc92fafb8bc24871b288fb198d7
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 01/15/2021
ms.locfileid: "5003074"
---
# <a name="create-a-budget-from-transaction-accounts-and-total-accounts"></a><span data-ttu-id="2d659-104">Vytváření rozpočtu z účtů transakcí a součtových účtů</span><span class="sxs-lookup"><span data-stu-id="2d659-104">Create a budget from transaction accounts and total accounts</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="2d659-105">V tomto článku je přehled procesu vytváření rozpočtů na základě součtových účtů.</span><span class="sxs-lookup"><span data-stu-id="2d659-105">This article provides an overview of the process for creating budgets based on total accounts.</span></span> <span data-ttu-id="2d659-106">Také vysvětluje, jak lze zapnout kontrolu rozpočtu pro součtové účty, jestliže je požadována kontrola rozpočtu.</span><span class="sxs-lookup"><span data-stu-id="2d659-106">It also explains how to turn on budget control for total accounts, if budget control is required.</span></span>

<span data-ttu-id="2d659-107">Dokumenty plán rozpočtu a položka registru rozpočtu umožňují rozpočtování pro hlavní účty, které mají typ hlavního účtu **Součet**.</span><span class="sxs-lookup"><span data-stu-id="2d659-107">Both budget plan and budget register entry documents allow for budgeting on main accounts that have a main account type of **Total**.</span></span> <span data-ttu-id="2d659-108">Skutečné hodnoty lze zaúčtovat pouze s hlavními účty transakcí.</span><span class="sxs-lookup"><span data-stu-id="2d659-108">Actuals can be posted only to transactional main accounts.</span></span> 

<span data-ttu-id="2d659-109">Pro periodické zpracování **Generovat plán rozpočtu z hlavní knihy** na kartě **Zdroj** můžete jako kritérium zadat typ hlavního účtu **Celkem**.</span><span class="sxs-lookup"><span data-stu-id="2d659-109">For the **Generate budget plan from General ledger** periodic process, on the **Source** tab, you can specify the **Total** main account type as a criterion.</span></span> <span data-ttu-id="2d659-110">V takovém případě se každý souhrnný hlavní účet zahrne do cílového plánu rozpočtu a částka se bude rovnat celkové částce rozsahu vybraných hlavních účtů.</span><span class="sxs-lookup"><span data-stu-id="2d659-110">In this case, each total main account will be included in the target budget plan, and the amount will equal the total amount of the range of selected main accounts.</span></span> 

<span data-ttu-id="2d659-111">Pro hlavní účty typu **Celkem** můžete aktivovat kontrolu rozpočtu.</span><span class="sxs-lookup"><span data-stu-id="2d659-111">You can activate budget control for main accounts of the **Total** type.</span></span> <span data-ttu-id="2d659-112">Tato funkce je podporována použitím rozpočtových skupin.</span><span class="sxs-lookup"><span data-stu-id="2d659-112">This functionality is supported through the use of budget groups.</span></span> <span data-ttu-id="2d659-113">Pro každý souhrnný hlavní účet se musí rozpočet, který má rozpočtová skupina ovládat, vytvořit na stránce **Konfigurace kontroly rozpočtu**.</span><span class="sxs-lookup"><span data-stu-id="2d659-113">For each total main account, the budget that should be controlled for a budget group must be created on the \*\*Budget control configuration \*\*page.</span></span> <span data-ttu-id="2d659-114">Mezi zadanými kritérii musí být souhrnný hlavní účet a rozsah účtů.</span><span class="sxs-lookup"><span data-stu-id="2d659-114">The criteria that you specify must include the total main account and the range of accounts.</span></span> <span data-ttu-id="2d659-115">Abyste proces vytváření rozpočtových skupin urychlili, můžete využít datovou entitu Skupiny kontroly rozpočtu.</span><span class="sxs-lookup"><span data-stu-id="2d659-115">To speed up the process of creating budget groups, you can take advantage of the Budget control groups data entity.</span></span> 

<span data-ttu-id="2d659-116">Pokud se rozpočet používá ve vykazování, například u finančního výkazu, skládá se suma rozpočtu celkového účtu z následujících částek:</span><span class="sxs-lookup"><span data-stu-id="2d659-116">When a budget is used in reporting, such as on a financial statement, the budget sum for the total account consists of the following amounts:</span></span>

-   <span data-ttu-id="2d659-117">Rozpočty, které se vytvoří z každého účtu transakční knihy v rámci intervalu souhrnného účtu.</span><span class="sxs-lookup"><span data-stu-id="2d659-117">The budgets that are created from each transaction ledger account in the interval of the total account.</span></span>
-   <span data-ttu-id="2d659-118">Částka rozpočtu, která se zadává přímo do souhrnného účtu.</span><span class="sxs-lookup"><span data-stu-id="2d659-118">The budget amount that is entered directly on the total account.</span></span>

<span data-ttu-id="2d659-119">Můžete tak vytvořit samostatné rozpočty pro nejvýznamnější transakční účty v intervalu souhrnného účtu a poté přidat dostupnou částku rozpočtu k souhrnnému účtu.</span><span class="sxs-lookup"><span data-stu-id="2d659-119">Therefore, you can create separate budgets for the most significant transaction accounts in the interval of the total account, and then add the available budget amount to the total account.</span></span>



