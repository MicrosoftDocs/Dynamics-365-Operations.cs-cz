---
title: Konfigurace standardních nákladů pro práci a výdaje
description: Tento postup ukazuje způsob nastavení standardních nákladů na práci a výdaje na projekt.
author: KimANelson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjCostPriceHour, ProjSalesPriceHour, ProjCostPriceExpense, ProjSalesPriceCost
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Service industries
ms.author: knelson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: f89590c87aec1a7200e95aeac6b2765fc64bb623
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 01/29/2019
ms.locfileid: "339388"
---
# <a name="configure-standard-costs-for-labor-and-expenses"></a><span data-ttu-id="01aa4-103">Konfigurace standardních nákladů pro práci a výdaje</span><span class="sxs-lookup"><span data-stu-id="01aa4-103">Configure standard costs for labor and expenses</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="01aa4-104">Tento postup ukazuje způsob nastavení standardních nákladů na práci a výdaje na projekt.</span><span class="sxs-lookup"><span data-stu-id="01aa4-104">This procedure shows you how to set up standard costs for labor and expenses for a project.</span></span> <span data-ttu-id="01aa4-105">Tato úloha používá sadu dat USSI.</span><span class="sxs-lookup"><span data-stu-id="01aa4-105">This task uses the USSI data set.</span></span>

1. <span data-ttu-id="01aa4-106">Přejděte na Řízení a účetnictví projektů > Nastavení > Ceny > Nákladová cena (hodina).</span><span class="sxs-lookup"><span data-stu-id="01aa4-106">Go to Project management and accounting > Setup > Prices > Cost price (hour).</span></span>
2. <span data-ttu-id="01aa4-107">Klikněte na položku Nová.</span><span class="sxs-lookup"><span data-stu-id="01aa4-107">Click New.</span></span>
3. <span data-ttu-id="01aa4-108">Zadejte datum do pole Datum platnosti.</span><span class="sxs-lookup"><span data-stu-id="01aa4-108">In the Effective date field, enter a date.</span></span>
4. <span data-ttu-id="01aa4-109">Zadejte číslo do pole Nákladová cena.</span><span class="sxs-lookup"><span data-stu-id="01aa4-109">In the Cost price field, enter a number.</span></span>
    * <span data-ttu-id="01aa4-110">Můžete nastavit standardní nákladovou cenu pro kategorii projektu nebo můžete nastavit nákladovou cenu podle čísla pracovníka, čísla projektu, kategorie, data nebo jejich kombinace.</span><span class="sxs-lookup"><span data-stu-id="01aa4-110">You can set up a standard cost price for the project category, or you can set up a cost price by worker number, project number, category, date, or any combination of these.</span></span> <span data-ttu-id="01aa4-111">Použitá nákladová cena je nákladová cena s nejvyšší úrovní podrobností.</span><span class="sxs-lookup"><span data-stu-id="01aa4-111">The cost price that is applied is the cost price with the highest level of detail.</span></span>  
5. <span data-ttu-id="01aa4-112">Klikněte na položku Uložit.</span><span class="sxs-lookup"><span data-stu-id="01aa4-112">Click Save.</span></span>
6. <span data-ttu-id="01aa4-113">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="01aa4-113">Close the page.</span></span>
7. <span data-ttu-id="01aa4-114">Přejděte na Řízení a účetnictví projektu > Nastavení > Ceny > Prodejní cena (hodina).</span><span class="sxs-lookup"><span data-stu-id="01aa4-114">Go to Project management and accounting > Setup > Prices > Sales price (hour).</span></span>
8. <span data-ttu-id="01aa4-115">Klikněte na položku Nová.</span><span class="sxs-lookup"><span data-stu-id="01aa4-115">Click New.</span></span>
9. <span data-ttu-id="01aa4-116">Zadejte datum do pole Datum platnosti.</span><span class="sxs-lookup"><span data-stu-id="01aa4-116">In the Effective date field, enter a date.</span></span>
10. <span data-ttu-id="01aa4-117">Vyberte volbu v poli Platné pro.</span><span class="sxs-lookup"><span data-stu-id="01aa4-117">In the Valid for field, select an option.</span></span>
11. <span data-ttu-id="01aa4-118">Do pole Oceňování zadejte číslo.</span><span class="sxs-lookup"><span data-stu-id="01aa4-118">In the Pricing field, enter a number.</span></span>
    * <span data-ttu-id="01aa4-119">Je možné nastavit standardní prodejní cenu pro hodinové transakce nebo pro kategorii projektu.</span><span class="sxs-lookup"><span data-stu-id="01aa4-119">You can set up a standard sales price for hour transactions or for a project category.</span></span> <span data-ttu-id="01aa4-120">Můžete rovněž nastavit prodejní ceny podle čísla pracovníka, čísla projektu, kategorie, data transakce či jejich libovolné kombinace.</span><span class="sxs-lookup"><span data-stu-id="01aa4-120">You can also set up sales prices by worker number, project number, category, transaction date, or any combination of these.</span></span> <span data-ttu-id="01aa4-121">Skutečná prodejní cena, která se použije, když pracovník zadá transakci do deníku hodin, je prodejní cena s nejvyšší úrovní podrobnosti.</span><span class="sxs-lookup"><span data-stu-id="01aa4-121">The actual sales price, which is applied when a worker enters a transaction in the Hour journal, is the sales price with the highest level of detail.</span></span> <span data-ttu-id="01aa4-122">Je-li například nastavena jak všeobecná prodejní cena, tak i specifická prodejní cena pro daného pracovníka, použije se prodejní cena specifická pro daného pracovníka.</span><span class="sxs-lookup"><span data-stu-id="01aa4-122">For example, if both a general sales price and a worker-specific sales price are set up, the worker-specific sales price is used.</span></span>  
12. <span data-ttu-id="01aa4-123">Klikněte na položku Uložit.</span><span class="sxs-lookup"><span data-stu-id="01aa4-123">Click Save.</span></span>
13. <span data-ttu-id="01aa4-124">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="01aa4-124">Close the page.</span></span>
14. <span data-ttu-id="01aa4-125">Přejděte na Řízení a účetnictví projektu >Nastavení > Ceny > Nákladová cena (výdaj).</span><span class="sxs-lookup"><span data-stu-id="01aa4-125">Go to Project management and accounting > Setup > Prices > Cost price (expense).</span></span>
15. <span data-ttu-id="01aa4-126">Klikněte na položku Nová.</span><span class="sxs-lookup"><span data-stu-id="01aa4-126">Click New.</span></span>
16. <span data-ttu-id="01aa4-127">Zadejte datum do pole Datum platnosti.</span><span class="sxs-lookup"><span data-stu-id="01aa4-127">In the Effective date field, enter a date.</span></span>
17. <span data-ttu-id="01aa4-128">Zadejte číslo do pole Nákladová cena.</span><span class="sxs-lookup"><span data-stu-id="01aa4-128">In the Cost price field, enter a number.</span></span>
    * <span data-ttu-id="01aa4-129">Lze vyplnit více polí, ale toto je minimum nutné pro uložení záznamu.</span><span class="sxs-lookup"><span data-stu-id="01aa4-129">Multiple fields can be filled in, but this is the minimum needed to save the record.</span></span>  
18. <span data-ttu-id="01aa4-130">Klikněte na položku Uložit.</span><span class="sxs-lookup"><span data-stu-id="01aa4-130">Click Save.</span></span>
19. <span data-ttu-id="01aa4-131">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="01aa4-131">Close the page.</span></span>
20. <span data-ttu-id="01aa4-132">Přejděte na Řízení a účetnictví projektů > Nastavení > Ceny > Prodejní cena (výdaj).</span><span class="sxs-lookup"><span data-stu-id="01aa4-132">Go to Project management and accounting > Setup > Prices > Sales price (expense).</span></span>
21. <span data-ttu-id="01aa4-133">Klikněte na položku Nová.</span><span class="sxs-lookup"><span data-stu-id="01aa4-133">Click New.</span></span>
22. <span data-ttu-id="01aa4-134">Zadejte datum do pole Datum platnosti.</span><span class="sxs-lookup"><span data-stu-id="01aa4-134">In the Effective date field, enter a date.</span></span>
23. <span data-ttu-id="01aa4-135">Vyberte volbu v poli Platné pro.</span><span class="sxs-lookup"><span data-stu-id="01aa4-135">In the Valid for field, select an option.</span></span>
24. <span data-ttu-id="01aa4-136">Do pole Oceňování zadejte číslo.</span><span class="sxs-lookup"><span data-stu-id="01aa4-136">In the Pricing field, enter a number.</span></span>
    * <span data-ttu-id="01aa4-137">Skutečná prodejní cena, která se použije, když pracovník zadá transakci do deníku výdajů, je prodejní cena s nejvyšší úrovní podrobnosti.</span><span class="sxs-lookup"><span data-stu-id="01aa4-137">The actual sales price, which is applied when a worker enters transactions in an expense journal, is the sales price with the highest level of detail.</span></span> <span data-ttu-id="01aa4-138">Je-li například nastavena jak všeobecná prodejní cena, tak i specifická prodejní cena pro daného pracovníka, použije se prodejní cena specifická pro daného pracovníka.</span><span class="sxs-lookup"><span data-stu-id="01aa4-138">For example, if both a general and a worker-specific sales price are set up, the worker-specific sales price is used.</span></span>  
25. <span data-ttu-id="01aa4-139">Klikněte na položku Uložit.</span><span class="sxs-lookup"><span data-stu-id="01aa4-139">Click Save.</span></span>

