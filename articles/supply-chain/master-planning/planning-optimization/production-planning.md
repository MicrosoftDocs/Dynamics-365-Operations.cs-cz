---
title: Plánování výroby
description: Toto téma popisuje plánování výroby a vysvětluje, jak upravit plánované výrobní zakázky pomocí optimalizace plánování.
author: ChristianRytt
manager: tfehr
ms.date: 12/15/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqCreatePlanWorkspace
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2020-12-15
ms.dyn365.ops.version: 10.0.13
ms.openlocfilehash: f9b5e4122fbd83ff76e0605b2f0816e10d2d9aab
ms.sourcegitcommit: 34b8f6f5c6134b7b97a9fb41d0b2e63215c67062
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/17/2021
ms.locfileid: "5470826"
---
# <a name="production-planning"></a><span data-ttu-id="c1b2d-103">Plánování výroby</span><span class="sxs-lookup"><span data-stu-id="c1b2d-103">Production planning</span></span>

<span data-ttu-id="c1b2d-104">Optimalizace plánování podporuje několik produkčních scénářů.</span><span class="sxs-lookup"><span data-stu-id="c1b2d-104">Planning Optimizations supports several production scenarios.</span></span> <span data-ttu-id="c1b2d-105">Pokud migrujete ze stávajícího integrovaného hlavního plánovacího modulu, je důležité si uvědomit nějaké změněné chování.</span><span class="sxs-lookup"><span data-stu-id="c1b2d-105">If you're migrating from the existing, built-in master planning engine, it's important that you be aware of some changed behavior.</span></span>

<span data-ttu-id="c1b2d-106">Následující video poskytuje krátký úvod k některým konceptům pojednávaným v tomto tématu: [Dynamics 365 Supply Chain Management: Vylepšení optimalizace plánování](https://youtu.be/u1pcmZuZBTw).</span><span class="sxs-lookup"><span data-stu-id="c1b2d-106">The following video gives a short introduction to some of the concepts discussed in this topic: [Dynamics 365 Supply Chain Management: Planning Optimization enhancements](https://youtu.be/u1pcmZuZBTw).</span></span>

## <a name="planned-production-orders"></a><span data-ttu-id="c1b2d-107">Plánované výrobní zakázky</span><span class="sxs-lookup"><span data-stu-id="c1b2d-107">Planned production orders</span></span>

<span data-ttu-id="c1b2d-108">Když hlavní plánování vytvoří plánované objednávky pro splnění požadavků, je typ objednávky určen hodnotou pole **Typ plánované objednávky**.</span><span class="sxs-lookup"><span data-stu-id="c1b2d-108">When master planning creates planned orders to fulfill requirements, the order type is determined by the value of the **Planned order type** field.</span></span> <span data-ttu-id="c1b2d-109">Pokud je pole **Plánovaný typ objednávky** nastaveno na *Výroba*, jsou vytvořeny plánované výrobní zakázky.</span><span class="sxs-lookup"><span data-stu-id="c1b2d-109">If the **Planned order type** field is set to *Production*, planned production orders are created.</span></span> <span data-ttu-id="c1b2d-110">Tyto plánované výrobní zakázky obsahují informace o aktivním kusovníku (BOM) a ID trasy ze souvisejícího výrobního nastavení.</span><span class="sxs-lookup"><span data-stu-id="c1b2d-110">These planned production orders include information about the active bill of materials (BOM) and the route ID from the related production setup.</span></span>

## <a name="requirements-from-boms"></a><span data-ttu-id="c1b2d-111">Požadavky na kusovníky</span><span class="sxs-lookup"><span data-stu-id="c1b2d-111">Requirements from BOMs</span></span>

<span data-ttu-id="c1b2d-112">Informace o kusovníku se zadávají během hlavního plánování.</span><span class="sxs-lookup"><span data-stu-id="c1b2d-112">BOM information is honored during master planning.</span></span> <span data-ttu-id="c1b2d-113">Výstup plánu zahrnuje dodávku materiálu k pokrytí související materiálové poptávky po výrobě.</span><span class="sxs-lookup"><span data-stu-id="c1b2d-113">The plan output includes material supply to cover related material demand for production.</span></span>

<span data-ttu-id="c1b2d-114">Během hlavního plánování se k určení materiálů potřebných pro výrobu použije aktuální aktivní kusovník.</span><span class="sxs-lookup"><span data-stu-id="c1b2d-114">During master planning, the current, active BOM is used to determine the materials that are required for production.</span></span> <span data-ttu-id="c1b2d-115">Tento krok se provádí na všech úrovních struktury kusovníku, která souvisí s požadovanou výrobní zakázkou.</span><span class="sxs-lookup"><span data-stu-id="c1b2d-115">This step is done through all levels of the BOM structure that is related to the required production order.</span></span> <span data-ttu-id="c1b2d-116">Požadavek na materiál je splněn využitím dostupných zásob na skladě, existujícího dodání na objednávku a schválených plánovaných objednávek.</span><span class="sxs-lookup"><span data-stu-id="c1b2d-116">Material requirement is fulfilled by using available on-hand inventory, existing on-order supply, and approved planned orders.</span></span> <span data-ttu-id="c1b2d-117">Pokud je kdekoli potřeba další materiál, vytvoří se plánovaná objednávka k pokrytí poptávky.</span><span class="sxs-lookup"><span data-stu-id="c1b2d-117">If additional material is required anywhere, a planned order is created to cover the demand.</span></span>

## <a name="scheduling-during-firming"></a><span data-ttu-id="c1b2d-118">Plánování během potvrzení</span><span class="sxs-lookup"><span data-stu-id="c1b2d-118">Scheduling during firming</span></span>

<span data-ttu-id="c1b2d-119">Plánované výrobní zakázky zahrnují ID trasy, které je požadováno pro plánování výroby.</span><span class="sxs-lookup"><span data-stu-id="c1b2d-119">Planned production orders include the route ID that is required for production scheduling.</span></span> <span data-ttu-id="c1b2d-120">Podpora plánování během běhu plánování pro plánované objednávky však čeká na vyřízení.</span><span class="sxs-lookup"><span data-stu-id="c1b2d-120">However, scheduling support during the planning run for planned orders is pending.</span></span> <span data-ttu-id="c1b2d-121">ID trasy se používá k plánování plánovaných výrobních zakázek během zpevňování.</span><span class="sxs-lookup"><span data-stu-id="c1b2d-121">The route ID is used to schedule planned production orders during firming.</span></span> <span data-ttu-id="c1b2d-122">Dodací lhůta u plánovaných výrobních zakázek se proto může lišit od dodací lhůty u souvisejících naplánovaných, zpevněných výrobních zakázek, které se z nich generují, jak je popsáno zde:</span><span class="sxs-lookup"><span data-stu-id="c1b2d-122">Therefore, the lead time on planned production orders can differ from the lead time on related scheduled, firmed production orders that are generated from them, as described here:</span></span>

- <span data-ttu-id="c1b2d-123">**Plánovaná výrobní zakázka** - Dodací lhůta je založena na statické dodací době z uvolněného produktu.</span><span class="sxs-lookup"><span data-stu-id="c1b2d-123">**Planned production order** – The lead time is based on the static lead time from the released product.</span></span>
- <span data-ttu-id="c1b2d-124">**Pevná výrobní zakázka** - Dodací lhůta je založena na plánování, které využívá informace o trase a související omezení zdrojů.</span><span class="sxs-lookup"><span data-stu-id="c1b2d-124">**Firmed production order** – The lead time is based on scheduling that uses route information and related resource constraints.</span></span>

<span data-ttu-id="c1b2d-125">Další informace o očekávané dostupnosti funkcí najdete v části [Analýza přizpůsobení optimalizace plánování](planning-optimization-fit-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="c1b2d-125">For more information about expected feature availability, see [Planning Optimization fit analysis](planning-optimization-fit-analysis.md).</span></span>

<span data-ttu-id="c1b2d-126">Pokud jste závislí na produkčních funkcích, které pro optimalizaci plánování ještě nejsou k dispozici, můžete nadále používat integrovaný hlavní plánovací stroj.</span><span class="sxs-lookup"><span data-stu-id="c1b2d-126">If you depend on production functionality that isn't yet available for Planning Optimization, you can continue to use the built-in master planning engine.</span></span> <span data-ttu-id="c1b2d-127">Není nutná žádná výjimka.</span><span class="sxs-lookup"><span data-stu-id="c1b2d-127">No exception is required.</span></span>

## <a name="delays"></a><span data-ttu-id="c1b2d-128">Zpoždění</span><span class="sxs-lookup"><span data-stu-id="c1b2d-128">Delays</span></span>

<span data-ttu-id="c1b2d-129">Pokud je dodací lhůta pro požadovaný materiál delší než období mezi dnešním datem a datem požadavku na materiál, plánovaná objednávka požadovaného materiálu a související výrobní zakázka se zpozdí.</span><span class="sxs-lookup"><span data-stu-id="c1b2d-129">If the lead time for required material is longer than the period between today's date and the material requirement date, the planned order for the required material and the related production order will be delayed.</span></span> <span data-ttu-id="c1b2d-130">U plánovaných objednávek se zpoždění (ve dnech) počítá na základě doby realizace vydaného produktu.</span><span class="sxs-lookup"><span data-stu-id="c1b2d-130">For planned orders, the delay (in days) is calculated based on the lead time from the released product.</span></span> <span data-ttu-id="c1b2d-131">Informace o zpoždění se poté šíří všemi úrovněmi struktury kusovníku.</span><span class="sxs-lookup"><span data-stu-id="c1b2d-131">The delay information is then propagated through all levels of the BOM structure.</span></span> <span data-ttu-id="c1b2d-132">Proto můžete sledovat dopad zpožděné suroviny až k zákaznické prodejní objednávce.</span><span class="sxs-lookup"><span data-stu-id="c1b2d-132">Therefore, you can follow the impact of delayed raw material all the way to the customer sales order.</span></span>

## <a name="modifying-planned-orders"></a><span data-ttu-id="c1b2d-133">Změna plánovaných objednávek</span><span class="sxs-lookup"><span data-stu-id="c1b2d-133">Modifying planned orders</span></span>

<span data-ttu-id="c1b2d-134">Když změníte informace o plánované objednávce, zobrazí se následující zpráva: „Dopad manuálních změn na plánované objednávky se neprojeví ve zbytku plánu až do příštího hlavního plánování.“</span><span class="sxs-lookup"><span data-stu-id="c1b2d-134">When you change information on a planned order, you receive the following message: "Note that the impact of manual changes on planned orders won't be reflected in the rest of the plan until the next master planning run."</span></span>

<span data-ttu-id="c1b2d-135">Pokud chcete změnit informace o plánované objednávce a zjistit dopad na související požadavky na materiál, postupujte podle těchto kroků.</span><span class="sxs-lookup"><span data-stu-id="c1b2d-135">If you want to change information on a planned order and see the impact on the related material requirements, follow these steps.</span></span>

1. <span data-ttu-id="c1b2d-136">Aktualizujte plánovanou objednávku.</span><span class="sxs-lookup"><span data-stu-id="c1b2d-136">Update the planned order.</span></span>
2. <span data-ttu-id="c1b2d-137">Schvalte plánovanou objednávku.</span><span class="sxs-lookup"><span data-stu-id="c1b2d-137">Approve the planned order.</span></span>
3. <span data-ttu-id="c1b2d-138">Spusťte hlavní plánování.</span><span class="sxs-lookup"><span data-stu-id="c1b2d-138">Run master planning.</span></span>

<span data-ttu-id="c1b2d-139">Při spuštění hlavního plánování byste neměli používat filtry, pokud jsou zahrnuty plánované výrobní zakázky.</span><span class="sxs-lookup"><span data-stu-id="c1b2d-139">When you run master planning, you should not use filters if planned production orders are included.</span></span> <span data-ttu-id="c1b2d-140">Více informací naleznete v části [Filtry](#filters) v dále v tomto tématu.</span><span class="sxs-lookup"><span data-stu-id="c1b2d-140">For more information, see the [Filters](#filters) section later in this topic.</span></span>

> [!NOTE]
> <span data-ttu-id="c1b2d-141">Pokud se datum dodání plánované objednávky změní na pozdější datum, může být požadavek navázán na novou plánovanou objednávku.</span><span class="sxs-lookup"><span data-stu-id="c1b2d-141">If the delivery date of the planned order is changed to a later date, the demand might be pegged against a new planned order.</span></span> <span data-ttu-id="c1b2d-142">K tomuto chování dochází, když nové datum dodávky způsobí zpoždění pro vázanou poptávku, ale podle nastavení doby předstihu lze zpoždění zabránit.</span><span class="sxs-lookup"><span data-stu-id="c1b2d-142">This behavior occurs when the new supply date causes a delay for the pegged demand but, according to the lead time settings, the delay can be avoided.</span></span>

## <a name="explosion-page"></a><span data-ttu-id="c1b2d-143">Stránka exploze</span><span class="sxs-lookup"><span data-stu-id="c1b2d-143">Explosion page</span></span>

<span data-ttu-id="c1b2d-144">Stránku **Exploze** můžete použít pro analýzu poptávky, která je požadována pro konkrétní výrobní zakázku nebo plánovanou výrobní zakázku, související pokrytím a informacemi o fixaci.</span><span class="sxs-lookup"><span data-stu-id="c1b2d-144">You can use the **Explosion** page to analyze the demand that is required for a specific production order or planned production order, the related coverage, and pegging information.</span></span> <span data-ttu-id="c1b2d-145">Informace na stránce **Exploze** se během hlavního plánování aktualizuje.</span><span class="sxs-lookup"><span data-stu-id="c1b2d-145">Information on the **Explosion** page is updated during master planning.</span></span> <span data-ttu-id="c1b2d-146">Informace nemůžete aktualizovat přímo ze stránky **Exploze**.</span><span class="sxs-lookup"><span data-stu-id="c1b2d-146">You can't update the information directly from the **Explosion** page.</span></span>

## <a name="filters"></a><a name="filters"></a><span data-ttu-id="c1b2d-147">Filtry</span><span class="sxs-lookup"><span data-stu-id="c1b2d-147">Filters</span></span>

<span data-ttu-id="c1b2d-148">Pro scénáře plánování, které zahrnují produkci, doporučujeme vyhnout se filtrovaným běhům hlavního plánování.</span><span class="sxs-lookup"><span data-stu-id="c1b2d-148">For planning scenarios that include production, we recommend that you avoid filtered master planning runs.</span></span> <span data-ttu-id="c1b2d-149">Abyste zajistili, že optimalizace plánování obsahuje informace, které jsou požadovány k výpočtu správného výsledku, musíte zahrnout všechny produkty, které mají jakýkoli vztah k produktům, do celé struktury kusovníku plánované objednávky.</span><span class="sxs-lookup"><span data-stu-id="c1b2d-149">To ensure that Planning Optimization has the information that is required to calculate the correct result, you must include all products that have any relation to products in the whole BOM structure of the planned order.</span></span>

<span data-ttu-id="c1b2d-150">I když jsou závislé podřízené položky automaticky detekovány a zahrnuty do hlavních běhů plánování, když je použit integrovaný hlavní plánovací stroj, Optimalizace plánování tuto akci neprovede.</span><span class="sxs-lookup"><span data-stu-id="c1b2d-150">Although dependent child items are automatically detected and included in master planning runs when the built-in master planning engine is used, Planning Optimization doesn't perform this action.</span></span>

<span data-ttu-id="c1b2d-151">Například pokud se k výrobě produktu B použije také jeden šroub ze struktury kusovníku produktu A, musí být do filtru zahrnuty všechny produkty ve struktuře kusovníku produktů A a B.</span><span class="sxs-lookup"><span data-stu-id="c1b2d-151">For example, if a single bolt from the BOM structure of product A is also used to produce product B, all products in the BOM structure of products A and B must be included in the filter.</span></span> <span data-ttu-id="c1b2d-152">Protože to může být velmi složité, aby bylo zajištěno, že všechny produkty jsou součástí filtru, doporučujeme, abyste se vyhnuli filtrovaným hlavním plánovacím běhům, když jsou zahrnuty výrobní zakázky.</span><span class="sxs-lookup"><span data-stu-id="c1b2d-152">Because it can be very complex to ensure that all products are part of the filter, we recommend that you avoid filtered master planning runs when production orders are involved.</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]