---
title: Konfigurace standardních nákladů pro práci a výdaje
description: Toto téma vysvětluje způsob nastavení standardních nákladů na práci a výdaje na projekt.
author: KimANelson
manager: AnnBe
ms.date: 08/02/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjCostPriceHour, ProjSalesPriceHour, ProjCostPriceExpense, ProjSalesPriceCost
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Service industries
ms.author: knelson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 60ab8eb94d4a8a0fb2c1e732ec7b25bfd5e7611e
ms.sourcegitcommit: a368682f9cf3897347d155f1a2d4b33e555cc2c4
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/08/2019
ms.locfileid: "1867719"
---
# <a name="configure-standard-costs-for-labor-and-expenses"></a><span data-ttu-id="8337d-103">Konfigurace standardních nákladů pro práci a výdaje</span><span class="sxs-lookup"><span data-stu-id="8337d-103">Configure standard costs for labor and expenses</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="8337d-104">Toto téma vysvětluje způsob nastavení standardních nákladů na práci a výdaje na projekt.</span><span class="sxs-lookup"><span data-stu-id="8337d-104">This topic explains how to set up standard costs for labor and expenses for a project.</span></span> <span data-ttu-id="8337d-105">Tato úloha používá sadu dat USSI.</span><span class="sxs-lookup"><span data-stu-id="8337d-105">This task uses the USSI data set.</span></span>

1. <span data-ttu-id="8337d-106">V navigačním podokně přejděte na **Moduly > Řízení a účetnictví projektů > Nastavení > Ceny > Nákladová cena (hodina)**.</span><span class="sxs-lookup"><span data-stu-id="8337d-106">In the navigation pane, go to **Modules > Project management and accounting > Setup > Prices > Cost price (hour)**.</span></span>
2. <span data-ttu-id="8337d-107">Zvolte **Nové**.</span><span class="sxs-lookup"><span data-stu-id="8337d-107">Select **New**.</span></span>
3. <span data-ttu-id="8337d-108">Zadejte datum do pole **Datum platnosti**.</span><span class="sxs-lookup"><span data-stu-id="8337d-108">In the **Effective date** field, enter a date.</span></span>
4. <span data-ttu-id="8337d-109">Zadejte číslo do pole **Nákladová cena.**</span><span class="sxs-lookup"><span data-stu-id="8337d-109">In the **Cost price** field, enter a number.</span></span> <span data-ttu-id="8337d-110">Můžete nastavit standardní nákladovou cenu pro kategorii projektu nebo můžete nastavit nákladovou cenu podle čísla pracovníka, čísla projektu, kategorie, data nebo jejich kombinace.</span><span class="sxs-lookup"><span data-stu-id="8337d-110">You can set up a standard cost price for the project category, or you can set up a cost price by worker number, project number, category, date, or any combination of these.</span></span> <span data-ttu-id="8337d-111">Použitá nákladová cena je nákladová cena s nejvyšší úrovní podrobností.</span><span class="sxs-lookup"><span data-stu-id="8337d-111">The cost price that is applied is the cost price with the highest level of detail.</span></span>  
5. <span data-ttu-id="8337d-112">Zvolte **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="8337d-112">Select **Save**.</span></span>
6. <span data-ttu-id="8337d-113">V navigačním podokně přejděte na **Moduly > Řízení a účetnictví projektů > Nastavení > Ceny > Prodejní cena (hodina)**.</span><span class="sxs-lookup"><span data-stu-id="8337d-113">In the navigation pane, go to **Modules > Project management and accounting > Setup > Prices > Sales price (hour)**.</span></span>
7. <span data-ttu-id="8337d-114">Zvolte **Nové**.</span><span class="sxs-lookup"><span data-stu-id="8337d-114">Select **New**.</span></span>
8. <span data-ttu-id="8337d-115">Zadejte datum do pole **Datum platnosti**.</span><span class="sxs-lookup"><span data-stu-id="8337d-115">In the **Effective date** field, enter a date.</span></span>
9. <span data-ttu-id="8337d-116">Vyberte volbu v poli **Platné pro**.</span><span class="sxs-lookup"><span data-stu-id="8337d-116">In the **Valid for** field, select an option.</span></span>
10. <span data-ttu-id="8337d-117">Do pole **Oceňování** zadejte číslo.</span><span class="sxs-lookup"><span data-stu-id="8337d-117">In the **Pricing** field, enter a number.</span></span> <span data-ttu-id="8337d-118">Je možné nastavit standardní prodejní cenu pro hodinové transakce nebo pro kategorii projektu.</span><span class="sxs-lookup"><span data-stu-id="8337d-118">You can set up a standard sales price for hour transactions or for a project category.</span></span> <span data-ttu-id="8337d-119">Můžete rovněž nastavit prodejní ceny podle čísla pracovníka, čísla projektu, kategorie, data transakce či jejich libovolné kombinace.</span><span class="sxs-lookup"><span data-stu-id="8337d-119">You can also set up sales prices by worker number, project number, category, transaction date, or any combination of these.</span></span> <span data-ttu-id="8337d-120">Skutečná prodejní cena, která se použije, když pracovník zadá transakci do deníku hodin, je prodejní cena s nejvyšší úrovní podrobnosti.</span><span class="sxs-lookup"><span data-stu-id="8337d-120">The actual sales price, which is applied when a worker enters a transaction in the Hour journal, is the sales price with the highest level of detail.</span></span> <span data-ttu-id="8337d-121">Je-li například nastavena jak všeobecná prodejní cena, tak i specifická prodejní cena pro daného pracovníka, použije se prodejní cena specifická pro daného pracovníka.</span><span class="sxs-lookup"><span data-stu-id="8337d-121">For example, if both a general sales price and a worker-specific sales price are set up, the worker-specific sales price is used.</span></span>  
11. <span data-ttu-id="8337d-122">Zvolte **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="8337d-122">Select **Save**.</span></span>
12. <span data-ttu-id="8337d-123">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="8337d-123">Close the page.</span></span>
13. <span data-ttu-id="8337d-124">V navigačním podokně přejděte na **Moduly > Řízení a účetnictví projektů > Nastavení > Ceny > Nákladová cena (výdaje)**.</span><span class="sxs-lookup"><span data-stu-id="8337d-124">In the navigation pane, go to **Modules > Project management and accounting > Setup > Prices > Cost price (expense)**.</span></span>
14. <span data-ttu-id="8337d-125">Zvolte **Nové**.</span><span class="sxs-lookup"><span data-stu-id="8337d-125">Select **New**.</span></span>
15. <span data-ttu-id="8337d-126">Zadejte datum do pole **Datum platnosti**.</span><span class="sxs-lookup"><span data-stu-id="8337d-126">In the **Effective date** field, enter a date.</span></span>
16. <span data-ttu-id="8337d-127">Zadejte číslo do pole **Nákladová cena.**</span><span class="sxs-lookup"><span data-stu-id="8337d-127">In the **Cost price** field, enter a number.</span></span> <span data-ttu-id="8337d-128">Lze vyplnit více polí, ale toto je minimum nutné pro uložení záznamu.</span><span class="sxs-lookup"><span data-stu-id="8337d-128">Multiple fields can be filled in, but this is the minimum needed to save the record.</span></span>  
17. <span data-ttu-id="8337d-129">Zvolte **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="8337d-129">Select **Save**.</span></span>
18. <span data-ttu-id="8337d-130">V navigačním podokně přejděte na **Moduly > Řízení a účetnictví projektů > Nastavení > Ceny > Prodejní cena (výdaje)**.</span><span class="sxs-lookup"><span data-stu-id="8337d-130">In the navigation pane, go to **Modules > Project management and accounting > Setup > Prices > Sales price (expense)**.</span></span>
19. <span data-ttu-id="8337d-131">Zvolte **Nové**.</span><span class="sxs-lookup"><span data-stu-id="8337d-131">Select **New**.</span></span>
20. <span data-ttu-id="8337d-132">Zadejte datum do pole **Datum platnosti**.</span><span class="sxs-lookup"><span data-stu-id="8337d-132">In the **Effective date** field, enter a date.</span></span>
21. <span data-ttu-id="8337d-133">Vyberte volbu v poli **Platné pro**.</span><span class="sxs-lookup"><span data-stu-id="8337d-133">In the **Valid for** field, select an option.</span></span>
22. <span data-ttu-id="8337d-134">Do pole **Oceňování** zadejte číslo.</span><span class="sxs-lookup"><span data-stu-id="8337d-134">In the **Pricing** field, enter a number.</span></span> <span data-ttu-id="8337d-135">Skutečná prodejní cena, která se použije, když pracovník zadá transakci do deníku výdajů, je prodejní cena s nejvyšší úrovní podrobnosti.</span><span class="sxs-lookup"><span data-stu-id="8337d-135">The actual sales price, which is applied when a worker enters transactions in an expense journal, is the sales price with the highest level of detail.</span></span> <span data-ttu-id="8337d-136">Je-li například nastavena jak všeobecná prodejní cena, tak i specifická prodejní cena pro daného pracovníka, použije se prodejní cena specifická pro daného pracovníka.</span><span class="sxs-lookup"><span data-stu-id="8337d-136">For example, if both a general and a worker-specific sales price are set up, the worker-specific sales price is used.</span></span>  
23. <span data-ttu-id="8337d-137">Zvolte **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="8337d-137">Select **Save**.</span></span>

