---
title: Řešení potíží s hlavním plánováním
description: Toto téma popisuje, jak vyřešit problémy, s nimiž se můžete setkat při práci s hlavním plánováním.
author: SmithaNataraj
ms.date: 11/04/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: smnatara
ms.search.validFrom: 2020-11-04
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 8e78634c0efb1c401297559ce40b2ca30519f3bf
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/01/2021
ms.locfileid: "5809463"
---
# <a name="troubleshoot-master-planning"></a><span data-ttu-id="af743-103">Řešení potíží s hlavním plánováním</span><span class="sxs-lookup"><span data-stu-id="af743-103">Troubleshoot master planning</span></span>

<span data-ttu-id="af743-104">Toto téma popisuje, jak vyřešit problémy, s nimiž se můžete setkat při práci s hlavním plánováním.</span><span class="sxs-lookup"><span data-stu-id="af743-104">This topic describes how to fix issues that you might encounter while you work with master planning.</span></span>

## <a name="bill-of-materials-explosion-behaves-differently-for-firmed-production-orders-and-for-estimated-production-orders-for-manually-created-work"></a><span data-ttu-id="af743-105">Rozpad kusovníku se chová odlišně pro potvrzené výrobní zakázky a pro odhadované výrobní zakázky pro ručně vytvořenou práci.</span><span class="sxs-lookup"><span data-stu-id="af743-105">Bill of materials explosion behaves differently for firmed production orders and for estimated production orders for manually created work.</span></span>

### <a name="issue-description"></a><span data-ttu-id="af743-106">Popis problému</span><span class="sxs-lookup"><span data-stu-id="af743-106">Issue description</span></span>

<span data-ttu-id="af743-107">Když je výrobní zakázka potvrzena, položky nebudou rozpadnuty, když rozpadnete kusovník (BOM).</span><span class="sxs-lookup"><span data-stu-id="af743-107">When a production order is firmed, the items aren't exploded when you explode the bill of materials (BOM).</span></span> <span data-ttu-id="af743-108">Když však ručně vytvoříte pracovní příkaz a poté odhadnete výrobní zakázku, položky se rozpadnou.</span><span class="sxs-lookup"><span data-stu-id="af743-108">However, when you manually create a work order and then estimate the production order, the items are exploded.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="af743-109">Řešení problému</span><span class="sxs-lookup"><span data-stu-id="af743-109">Issue resolution</span></span>

<span data-ttu-id="af743-110">Systém funguje podle očekávání.</span><span class="sxs-lookup"><span data-stu-id="af743-110">The system is working as expected.</span></span> <span data-ttu-id="af743-111">Rozpad, ke kterému dojde, když je výrobní zakázka potvrzena, bude ukazovat na plánovanou zakázku, ale nezdá se, že by v tomto případě byla plánovaná objednávka aktuálně potvrzena.</span><span class="sxs-lookup"><span data-stu-id="af743-111">The explosion that occurs when the production order is firmed will point to the planned order, but it doesn't appear that the planned order is currently firmed in this case.</span></span> <span data-ttu-id="af743-112">Pokud však byla výrobní zakázka odhadnuta, rozpad se spustí z uvolněné výrobní zakázky, kde neexistuje žádná plánovaná objednávka.</span><span class="sxs-lookup"><span data-stu-id="af743-112">However, if the production order has been estimated, the explosion is triggered from the released production order where no planned order exists.</span></span>

## <a name="the-delay-value-isnt-updated-when-i-reschedule-a-planned-order"></a><span data-ttu-id="af743-113">Hodnota zpoždění se neaktualizuje, když přeplánuji plánovanou objednávku.</span><span class="sxs-lookup"><span data-stu-id="af743-113">The Delay value isn't updated when I reschedule a planned order.</span></span>

<span data-ttu-id="af743-114">Chcete-li aktualizovat zpoždění u plánovaných zakázek, otevřete dialogové okno **Přeplánování** pro plánovanou objednávku.</span><span class="sxs-lookup"><span data-stu-id="af743-114">To update the delay for planned orders, open the **Rescheduling** dialog box for the planned order.</span></span> <span data-ttu-id="af743-115">Na záložce s náhledem **Rozpad** se ujistěte, že je možnost **Provést rozpad po přeplánování** nastavená na *Ano*.</span><span class="sxs-lookup"><span data-stu-id="af743-115">On the **Explosion** FastTab, make sure that the **Perform explosion after rescheduling** option is set to *Yes*.</span></span>

## <a name="production-scheduling-doesnt-consider-the-safety-margins-that-are-set-on-the-item-coverage-for-pegged-supply"></a><span data-ttu-id="af743-116">Plánování výroby nezohledňuje bezpečnostní rezervy, které jsou nastaveny na pokrytí položky pro doloženou dodávku.</span><span class="sxs-lookup"><span data-stu-id="af743-116">Production scheduling doesn't consider the safety margins that are set on the item coverage for pegged supply.</span></span>

### <a name="issue-description"></a><span data-ttu-id="af743-117">Popis problému</span><span class="sxs-lookup"><span data-stu-id="af743-117">Issue description</span></span>

<span data-ttu-id="af743-118">Hlavní plánování zohledňuje bezpečnostní rezervy.</span><span class="sxs-lookup"><span data-stu-id="af743-118">Master planning considers the safety margins.</span></span> <span data-ttu-id="af743-119">Při plánování plánovaných výrobních zakázek jsou však bezpečnostní rezervy ignorovány.</span><span class="sxs-lookup"><span data-stu-id="af743-119">However, the safety margins are ignored when planned production orders are scheduled.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="af743-120">Řešení problému</span><span class="sxs-lookup"><span data-stu-id="af743-120">Issue resolution</span></span>

<span data-ttu-id="af743-121">Rezervy se berou v úvahu pouze během hlavního plánování, nikoli během manuálního plánování.</span><span class="sxs-lookup"><span data-stu-id="af743-121">Margins are considered only during master planning, not during manual scheduling.</span></span> <span data-ttu-id="af743-122">Rezervy jsou navrženy tak, aby fungovaly jako nárazník během fáze plánování a aby poskytly určitou „rezervu“ pro skutečný proces.</span><span class="sxs-lookup"><span data-stu-id="af743-122">Margins are designed to act as a buffer during the planning phase, to give some "margin" for the actual process.</span></span>

<span data-ttu-id="af743-123">Chcete-li dosáhnout požadovaného výsledku, můžete odstranit rezervu.</span><span class="sxs-lookup"><span data-stu-id="af743-123">To get the desired result, you can remove the margin.</span></span> <span data-ttu-id="af743-124">Postup musí být poté aktualizován tak, aby obsahoval požadovaný čas (například jako čas fronty).</span><span class="sxs-lookup"><span data-stu-id="af743-124">The route must then be updated so that it includes the desired time (for example, as queue time).</span></span> <span data-ttu-id="af743-125">Hlavní plánování i manuální plánování by pak mělo přinést stejný výsledek.</span><span class="sxs-lookup"><span data-stu-id="af743-125">Both master planning and manual scheduling should then produce the same result.</span></span>

## <a name="planned-orders-are-generated-even-though-we-have-items-in-stock-and-production-orders-already-exist-for-them"></a><span data-ttu-id="af743-126">Plánované objednávky se generují, i když máme položky na skladě a výrobní zakázky pro ně již existují.</span><span class="sxs-lookup"><span data-stu-id="af743-126">Planned orders are generated even though we have items in stock and production orders already exist for them.</span></span>

<span data-ttu-id="af743-127">Tento problém můžete vyřešit zvýšením hodnoty **Pozitivní dny** pro příslušné skupiny na stránce **Skupina pokrytí**.</span><span class="sxs-lookup"><span data-stu-id="af743-127">You might be able to fix this issue by increasing the **Positive days** value for the relevant groups on the **Coverage group** page.</span></span> <span data-ttu-id="af743-128">Tato změna způsobí, že systém určí, zda lze pro poptávku použít zásoby na skladě.</span><span class="sxs-lookup"><span data-stu-id="af743-128">This change will cause the system to determine whether on-hand inventory can be used for the demand.</span></span> <span data-ttu-id="af743-129">Pak nebude vygenerována nová plánovaná objednávka pro položky, které jsou na skladě.</span><span class="sxs-lookup"><span data-stu-id="af743-129">Then a new planned order won't be generated for the items that are in stock.</span></span>

## <a name="master-planning-doesnt-seem-to-respect-capacity-limitations-and-is-scheduling-more-than-the-available-capacity"></a><span data-ttu-id="af743-130">Nezdá se, že by hlavní plánování respektovalo omezení kapacity a plánuje více, než je dostupná kapacita.</span><span class="sxs-lookup"><span data-stu-id="af743-130">Master planning doesn't seem to respect capacity limitations and is scheduling more than the available capacity.</span></span>

### <a name="issue-description"></a><span data-ttu-id="af743-131">Popis problému</span><span class="sxs-lookup"><span data-stu-id="af743-131">Issue description</span></span>

<span data-ttu-id="af743-132">Když používáte plánování operací, kde je konečná kapacita a kde postup určuje kombinaci požadavků jak pro skupinu zdrojů, tak pro jednotlivé zdroje, existuje malá šance na nadměrnou rezervaci kvůli způsobu, jakým algoritmus ověřuje konflikty kapacity.</span><span class="sxs-lookup"><span data-stu-id="af743-132">When you use operation scheduling where there is finite capacity, and where the route specifies a mix of requirements for both a resource group and individual resources, there is a small chance of overbooking because of the way that the algorithm validates for capacity conflicts.</span></span> <span data-ttu-id="af743-133">K této nadměrné rezervaci může dojít, když ke spuštění hlavního plánování použijete pomocníky.</span><span class="sxs-lookup"><span data-stu-id="af743-133">This overbooking can occur when you use helpers to run master planning.</span></span> <span data-ttu-id="af743-134">S největší pravděpodobností k tomu dojde, pokud existuje mnoho úloh, které mají relativně krátkou dobu běhu.</span><span class="sxs-lookup"><span data-stu-id="af743-134">It's most likely to occur if there are many jobs that have a relatively short runtime.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="af743-135">Řešení problému</span><span class="sxs-lookup"><span data-stu-id="af743-135">Issue resolution</span></span>

<span data-ttu-id="af743-136">Pokud je pro plánování operací zásadní, aby nedocházelo k nadměrné rezervaci, můžete naplánovanou část hlavního plánování nastavit na jedno vlákno zapnutím možnosti **Přesná konečná kapacita pro plánování operací** na stránce **Parametry hlavního plánování**.</span><span class="sxs-lookup"><span data-stu-id="af743-136">If it's essential that no overbooking occur for operation scheduling, you can make the scheduling part of master planning single-threaded by turning on the **Accurate finite capacity for Operation Scheduling** option on the **Master planning parameters** page.</span></span> <span data-ttu-id="af743-137">Tato možnost není k dispozici ve výchozím nastavení.</span><span class="sxs-lookup"><span data-stu-id="af743-137">This option isn't available by default.</span></span> <span data-ttu-id="af743-138">Musíte ji ručně přidat na stránku pomocí funkcí přizpůsobení.</span><span class="sxs-lookup"><span data-stu-id="af743-138">You must manually add it to the page by using personalization features.</span></span> <span data-ttu-id="af743-139">Když použijete tuto možnost, bude plánování probíhat pomaleji z důvodu nedostatku paralelního zpracování.</span><span class="sxs-lookup"><span data-stu-id="af743-139">When you use this option, scheduling will run more slowly because of the lack of parallel processing.</span></span>

## <a name="planned-orders-take-a-long-time-to-update"></a><span data-ttu-id="af743-140">Aktualizace plánovaných objednávek trvá dlouho.</span><span class="sxs-lookup"><span data-stu-id="af743-140">Planned orders take a long time to update.</span></span>

### <a name="issue-description"></a><span data-ttu-id="af743-141">Popis problému</span><span class="sxs-lookup"><span data-stu-id="af743-141">Issue description</span></span>

<span data-ttu-id="af743-142">Při aktualizaci požadovaného množství anebo data dodání u plánované objednávky uložení aktualizace obvykle trvá alespoň 30 sekund na objednávku.</span><span class="sxs-lookup"><span data-stu-id="af743-142">When updating the requirement quantity and/or delivery date on a planned order, it typically takes at least 30 seconds per order to save the update.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="af743-143">Řešení problému</span><span class="sxs-lookup"><span data-stu-id="af743-143">Issue resolution</span></span>

<span data-ttu-id="af743-144">Toto je známý problém s integrovaným modulem hlavního plánování.</span><span class="sxs-lookup"><span data-stu-id="af743-144">This is a known issue with the built-in master planning engine.</span></span> <span data-ttu-id="af743-145">Je to způsobeno podkladovým automatickým rozpadem skrz strukturu kusovníku během úprav.</span><span class="sxs-lookup"><span data-stu-id="af743-145">It is caused by the underlying auto explosion through the BOM structure during edits.</span></span> <span data-ttu-id="af743-146">Tomuto problému se věnuje optimalizace plánování, kde plánovač může aktualizovat a schválit příslušné objednávky a v případě potřeby spustit plánovací běh k aktualizaci plánovaných objednávek pro podkladovou strukturu kusovníku.</span><span class="sxs-lookup"><span data-stu-id="af743-146">This issue is addressed in Planning Optimization, where a planner can update and approve the relevant orders and, when desired, trigger a planning run to update planned orders for the underlying BOM structure.</span></span>

<span data-ttu-id="af743-147">Jedním ze způsobů, jak zlepšit výkon pomocí integrovaného modulu hlavního plánování, je provést následující:</span><span class="sxs-lookup"><span data-stu-id="af743-147">One way to improve performance with the built-in master planning engine is to do the following:</span></span>

1. <span data-ttu-id="af743-148">Přejděte na **Hlavní plánování \> Nastavení \> Plány \> Hlavní plány**.</span><span class="sxs-lookup"><span data-stu-id="af743-148">Go to **Master planning \> Setup \> Plans \> Master plans**.</span></span>
1. <span data-ttu-id="af743-149">Vyberte plán.</span><span class="sxs-lookup"><span data-stu-id="af743-149">Select a plan.</span></span>
1. <span data-ttu-id="af743-150">Rozbalte záložku s náhledem **Ochranné doby ve dnech**.</span><span class="sxs-lookup"><span data-stu-id="af743-150">Expand the **Time fence in days** FastTab.</span></span>
1. <span data-ttu-id="af743-151">Nastavte **Rozpad** na *Ano* a nastavte pole pod tímto nastavením na 0 (nula).</span><span class="sxs-lookup"><span data-stu-id="af743-151">Set **Explosion** to *Yes*, and set the field below this setting to 0 (zero).</span></span>

> [!NOTE]
> <span data-ttu-id="af743-152">Tím se omezí doba rozpadů provedených pro tento hlavní plán na jeden den.</span><span class="sxs-lookup"><span data-stu-id="af743-152">This will limit the period for explosions performed for this master plan to a single day.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]