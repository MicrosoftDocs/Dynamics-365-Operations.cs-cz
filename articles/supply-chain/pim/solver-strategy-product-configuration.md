---
title: "Strategie řešitele pro konfiguraci produktů"
description: "Toto téma popisuje, jak můžete použít strategii řešitele ke zlepšení výkonu konfigurace produktu."
author: cvocph
manager: AnnBe
ms.date: 01/02/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: PCCreateProductConfigurationModel, PCProductConfigurationModelListPage
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 
ms.assetid: 
ms.search.region: Global
ms.search.industry: 
ms.author: conradv
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 957dea7a37720a8f28ea5aa0568bf1f233574a8a
ms.contentlocale: cs-cz
ms.lasthandoff: 05/08/2018

---

# <a name="solver-strategy-for-product-configuration"></a><span data-ttu-id="5a85d-103">Strategie řešitele pro konfiguraci produktů</span><span class="sxs-lookup"><span data-stu-id="5a85d-103">Solver strategy for product configuration</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="5a85d-104">Toto téma popisuje, jak můžete použít strategii řešitele ke zlepšení výkonu konfigurace produktu.</span><span class="sxs-lookup"><span data-stu-id="5a85d-104">This topic describes how you can use the solver strategy to improve the performance of product configuration.</span></span>

<span data-ttu-id="5a85d-105">Koncept strategie řešitele byl poprvé představen v aktualizaci Cumulative update 7 (CU7) pro Microsoft Dynamics AX 2012 R2.</span><span class="sxs-lookup"><span data-stu-id="5a85d-105">The concept of solver strategies was first introduced in Cumulative update 7 (CU7) for Microsoft Dynamics AX 2012 R2.</span></span> <span data-ttu-id="5a85d-106">Byl rozšířen v aktualizaci Cumulative update 8 (CU8) pro Microsoft Dynamics AX 2012 R3 a Microsoft Dynamics 365 for Finance and Operations, Enterprise edition 7.3.</span><span class="sxs-lookup"><span data-stu-id="5a85d-106">It was extended in Cumulative update 8 (CU8) for Microsoft Dynamics AX 2012 R3 and Microsoft Dynamics 365 for Finance and Operations, Enterprise edition 7.3.</span></span>

<span data-ttu-id="5a85d-107">Koncept strategie řešitele se nyní skládá z následujících strategií:</span><span class="sxs-lookup"><span data-stu-id="5a85d-107">The solver strategy concept now consists of the following strategies:</span></span>

- <span data-ttu-id="5a85d-108">Výchozí</span><span class="sxs-lookup"><span data-stu-id="5a85d-108">Default</span></span>
- <span data-ttu-id="5a85d-109">Minimální domény jako první</span><span class="sxs-lookup"><span data-stu-id="5a85d-109">Minimal domains first</span></span>
- <span data-ttu-id="5a85d-110">Shora dolů</span><span class="sxs-lookup"><span data-stu-id="5a85d-110">Top-down</span></span>
- <span data-ttu-id="5a85d-111">Z3</span><span class="sxs-lookup"><span data-stu-id="5a85d-111">Z3</span></span>

## <a name="solver-strategy"></a><span data-ttu-id="5a85d-112">Strategie řešitele</span><span class="sxs-lookup"><span data-stu-id="5a85d-112">Solver strategy</span></span> 

<span data-ttu-id="5a85d-113">Model konfigurace výrobku může být formulován jako [problém omezení spokojenosti](http://aima.cs.berkeley.edu/2nd-ed/newchap05.pdf).</span><span class="sxs-lookup"><span data-stu-id="5a85d-113">A product configuration model can be formulated as a [constraint satisfaction problem (CSP)](http://aima.cs.berkeley.edu/2nd-ed/newchap05.pdf).</span></span> <span data-ttu-id="5a85d-114">Microsoft Solver Foundation (MSF) nabízí dva typy strategie řešitele k vyřešení problémů omezení spokojenosti, které lze používat z modelů konfigurace produktu.</span><span class="sxs-lookup"><span data-stu-id="5a85d-114">Microsoft Solver Foundation (MSF) provides two types of solver strategies to solve the CSPs that can be used from product configuration models.</span></span> <span data-ttu-id="5a85d-115">Tyto strategie řešitele využívají [heuristiky](https://techterms.com/definition/heuristic), která se používá k určení pořadí, ve kterém se proměnné problémů omezení spokojenosti zvažují při řešení problémů.</span><span class="sxs-lookup"><span data-stu-id="5a85d-115">These solver strategies rely on [heuristics](https://techterms.com/definition/heuristic), which are used to determine the order that the variables of the CSPs are considered in when the problem is being solved.</span></span> <span data-ttu-id="5a85d-116">Heuristika může významně ovlivnit výkon při řešení problému nebo třídy problémů.</span><span class="sxs-lookup"><span data-stu-id="5a85d-116">Heuristics can significantly affect performance when a problem or class of problems is being solved.</span></span>

<span data-ttu-id="5a85d-117">V aplikaci Finance and Operations strategie řešitele pro modely konfigurace produktu určuje řešitele, který se používá s heuristikou.</span><span class="sxs-lookup"><span data-stu-id="5a85d-117">In Finance and Operations, the solver strategy for product configuration models determines which solver is used with heuristics.</span></span> <span data-ttu-id="5a85d-118">Strategie **Výchozí**, **Minimální domény jako první** a **Shora dolů** používají dva řešitele z MSF, zatímco strategie **Z3** používá Z3 řešitele.</span><span class="sxs-lookup"><span data-stu-id="5a85d-118">The **Default**, **Minimal domains first**, and **Top-down** strategies use the two solvers from MSF, whereas the **Z3** strategy uses the Z3 solver.</span></span> 

<span data-ttu-id="5a85d-119">Reálné studie implementace odběratele ukázaly, že změna strategii řešitele pro model konfigurace produktu může zkrátit čas odezvy z minut na milisekundy.</span><span class="sxs-lookup"><span data-stu-id="5a85d-119">Real customer implementation studies have shown that a change in the solver strategy for a product configuration model can reduce the response time from minutes to milliseconds.</span></span> <span data-ttu-id="5a85d-120">Je proto vhodné se pokusit o jinou strategii řešitele k nalezení nejúčinnější strategie pro konfiguraci modelu produktu.</span><span class="sxs-lookup"><span data-stu-id="5a85d-120">Therefore, it's worth the effort to try different solver strategies to find the most efficient strategy for your product configuration model.</span></span>

## <a name="change-the-settings-for-the-solver-strategy"></a><span data-ttu-id="5a85d-121">Změna nastavení strategie řešitele</span><span class="sxs-lookup"><span data-stu-id="5a85d-121">Change the settings for the solver strategy</span></span>

<span data-ttu-id="5a85d-122">Chcete-li změnit strategii řešitele, na stránce **Modely konfigurace produktu** v podokně akcí zaškzvoltee **Vlastnosti modelu**.</span><span class="sxs-lookup"><span data-stu-id="5a85d-122">To change the solver strategy, on the **Product configuration models** page, on the Action Pane, select **Model properties**.</span></span> <span data-ttu-id="5a85d-123">V dialogovém okně **Upravit podrobnosti modelu** vyberte strategii řešitele.</span><span class="sxs-lookup"><span data-stu-id="5a85d-123">Then, in the **Edit the model details** dialog box, select a solver strategy.</span></span>

<span data-ttu-id="5a85d-124">[![Změna strategie řešitele](./media/solver-strategy.png)](./media/solver-strategy.png)</span><span class="sxs-lookup"><span data-stu-id="5a85d-124">[![Changing the solver strategy](./media/solver-strategy.png)](./media/solver-strategy.png)</span></span>

<span data-ttu-id="5a85d-125">V současné době neexistuje žádná logiká, která automaticky detekuje, jaká strategie řešitele bude nejúčinnější strategií pro konfigurace produktu na základě omezení.</span><span class="sxs-lookup"><span data-stu-id="5a85d-125">Currently, there is no logic that automatically detects which solver strategy will be the most efficient strategy for constraint-based product configuration.</span></span> <span data-ttu-id="5a85d-126">Proto musíte vyzkoušet strategie řešitele po jedné.</span><span class="sxs-lookup"><span data-stu-id="5a85d-126">Therefore, you must try the solver strategies one by one.</span></span>

<span data-ttu-id="5a85d-127">Následující tabulka poskytuje doporučení o strategii řešitele k použití různých scénářů.</span><span class="sxs-lookup"><span data-stu-id="5a85d-127">The following table provides recommendations about the solver strategy to use in various scenarios.</span></span>

| <span data-ttu-id="5a85d-128">Strategie řešitele</span><span class="sxs-lookup"><span data-stu-id="5a85d-128">Solver strategy</span></span>      | <span data-ttu-id="5a85d-129">Použití strategie v tomto scénáři</span><span class="sxs-lookup"><span data-stu-id="5a85d-129">Use the strategy in this scenario</span></span> |
|----------------------|-----------------------------------|
| <span data-ttu-id="5a85d-130">Výchozí</span><span class="sxs-lookup"><span data-stu-id="5a85d-130">Default</span></span>              | <span data-ttu-id="5a85d-131">Strategie **Výchozí** byla optimalizována pro řešení modelů, které závisí na omezení tabulky.</span><span class="sxs-lookup"><span data-stu-id="5a85d-131">The **Default** strategy has been optimized to solve models that rely on table constraints.</span></span> <span data-ttu-id="5a85d-132">Studie implementace odběratele ukázaly, že tato strategie je nejúčinnější strategií v situacích, kdy jsou omezení tabulky často používány.</span><span class="sxs-lookup"><span data-stu-id="5a85d-132">Customer implementation studies have shown that this strategy is the most efficient strategy in scenarios where table constraints are used extensively.</span></span> |
| <span data-ttu-id="5a85d-133">Minimální doména jako první</span><span class="sxs-lookup"><span data-stu-id="5a85d-133">Minimal domain first</span></span> | <span data-ttu-id="5a85d-134">Strategie **Minimální doména jako první** a **Shora dolů** spolu blízce souvisí.</span><span class="sxs-lookup"><span data-stu-id="5a85d-134">The **Minimal domain first** and **Top-down** strategies are closely related.</span></span> <span data-ttu-id="5a85d-135">Studie implementace odběratele ukázaly, že strategie **Shora dolů**, která byla uvedena v CU8, překonává strategie **Minimální doména jako první**.</span><span class="sxs-lookup"><span data-stu-id="5a85d-135">Customer implementation studies have shown that the **Top-down** strategy, which was introduced in CU8, outperforms the **Minimal domain first** strategy.</span></span> <span data-ttu-id="5a85d-136">Avšak strategie jako **Minimální doména jako první** se uchová v produktu pro zpětnou kompatibilitu.</span><span class="sxs-lookup"><span data-stu-id="5a85d-136">However, the **Minimal domain first** strategy is kept in the product for backward compatibility.</span></span> <span data-ttu-id="5a85d-137">Obě tyto strategie řešitele se ukázaly být jako efektivnější při řešení modelů, které obsahují několik aritmetických výrazů, kde se nepoužívají žádná omezení tabulky.</span><span class="sxs-lookup"><span data-stu-id="5a85d-137">Both these solver strategies have been shown to be more efficient at solving models that contain several arithmetic expressions where no table constraints are used.</span></span> <span data-ttu-id="5a85d-138">V některých případech však strategie **Výchozí** překonává výkonem tyto dvě strategie.</span><span class="sxs-lookup"><span data-stu-id="5a85d-138">However, in some cases, the **Default** strategy outperforms these two strategies.</span></span> <span data-ttu-id="5a85d-139">Nezapomeňte vyzkoušet všechny strategie.</span><span class="sxs-lookup"><span data-stu-id="5a85d-139">Therefore, remember to try each strategy.</span></span> |
| <span data-ttu-id="5a85d-140">Shora dolů</span><span class="sxs-lookup"><span data-stu-id="5a85d-140">Top-down</span></span>             | <span data-ttu-id="5a85d-141">Strategie **Minimální doména jako první** a **Shora dolů** spolu blízce souvisí.</span><span class="sxs-lookup"><span data-stu-id="5a85d-141">The **Minimal domain first** and **Top-down** strategies are closely related.</span></span> <span data-ttu-id="5a85d-142">Studie implementace odběratele ukázaly, že strategie **Shora dolů**, která byla uvedena v CU8, překonává strategie **Minimální doména jako první**.</span><span class="sxs-lookup"><span data-stu-id="5a85d-142">Customer implementation studies have shown that the **Top-down** strategy, which was introduced in CU8, outperforms the **Minimal domain first** strategy.</span></span> <span data-ttu-id="5a85d-143">Avšak strategie jako **Minimální doména jako první** se uchová v produktu pro zpětnou kompatibilitu.</span><span class="sxs-lookup"><span data-stu-id="5a85d-143">However, the **Minimal domain first** strategy is kept in the product for backward compatibility.</span></span> <span data-ttu-id="5a85d-144">Obě tyto strategie řešitele se ukázaly být jako efektivnější při řešení modelů, které obsahují několik aritmetických výrazů, kde se nepoužívají žádná omezení tabulky.</span><span class="sxs-lookup"><span data-stu-id="5a85d-144">Both these solver strategies have been shown to be more efficient at solving models that contain several arithmetic expressions where no table constraints are used.</span></span> <span data-ttu-id="5a85d-145">V některých případech však strategie **Výchozí** překonává výkonem tyto dvě strategie.</span><span class="sxs-lookup"><span data-stu-id="5a85d-145">However, in some cases, the **Default** strategy outperforms these two strategies.</span></span> <span data-ttu-id="5a85d-146">Nezapomeňte vyzkoušet všechny strategie.</span><span class="sxs-lookup"><span data-stu-id="5a85d-146">Therefore, remember to try each strategy.</span></span> |
| <span data-ttu-id="5a85d-147">Z3</span><span class="sxs-lookup"><span data-stu-id="5a85d-147">Z3</span></span>                   | <span data-ttu-id="5a85d-148">Doporučujeme používat strategii **Z3** jako výchozí strategii řešitele.</span><span class="sxs-lookup"><span data-stu-id="5a85d-148">We recommend that you use the **Z3** strategy as the default solver strategy.</span></span> <span data-ttu-id="5a85d-149">Pokud máte obavy o výkon a škálovatelnost, můžete vyhodnotit další strategie.</span><span class="sxs-lookup"><span data-stu-id="5a85d-149">If you're concerned about performance and scalability, you can evaluate the other strategies.</span></span> |

## <a name="additional-resources"></a><span data-ttu-id="5a85d-150">Další zdroje</span><span class="sxs-lookup"><span data-stu-id="5a85d-150">Additional resources</span></span>

[<span data-ttu-id="5a85d-151">Vytvoření modelu konfigurace produktu</span><span class="sxs-lookup"><span data-stu-id="5a85d-151">Build product configuration model</span></span>](build-product-configuration-model.md)

[<span data-ttu-id="5a85d-152">Heuristika</span><span class="sxs-lookup"><span data-stu-id="5a85d-152">Heuristics</span></span>](https://techterms.com/definition/heuristic)

[<span data-ttu-id="5a85d-153">Problém omezení spokojenosti</span><span class="sxs-lookup"><span data-stu-id="5a85d-153">Constraint Satisfaction Problem</span></span>](http://aima.cs.berkeley.edu/2nd-ed/newchap05.pdf)

