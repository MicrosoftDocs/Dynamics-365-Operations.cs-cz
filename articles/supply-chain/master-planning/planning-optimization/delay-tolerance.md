---
title: Tolerance zpoždění (záporné dny)
description: Toto téma poskytuje informace o výpočtu tolerance zpoždění a o tom, jak ovlivňuje plánované vytváření objednávek v Optimalizaci plánování.
author: crytt
ms.date: 07/30/2021
ms.topic: article
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: crytt
ms.search.validFrom: 2021-07-30
ms.dyn365.ops.version: 10.0.21
ms.openlocfilehash: 748e047e89747f2eabccc04a40c79bcb1e6f3dea
ms.sourcegitcommit: f21659f1c23bc2cd65bbe7fb7210910d5a8e1cb9
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/24/2021
ms.locfileid: "6306456"
---
# <a name="delay-tolerance-negative-days"></a><span data-ttu-id="b2ff1-103">Tolerance zpoždění (záporné dny)</span><span class="sxs-lookup"><span data-stu-id="b2ff1-103">Delay tolerance (negative days)</span></span>

[!include [banner](../../includes/banner.md)]
[!INCLUDE [preview-banner](../../includes/preview-banner.md)]

<span data-ttu-id="b2ff1-104">Funkce tolerance zpoždění umožňuje Optimalizaci plánování zohlednit hodnotu **Negativní dny**, která je nastavena pro skupiny pokrytí.</span><span class="sxs-lookup"><span data-stu-id="b2ff1-104">The delay tolerance functionality enables Planning Optimization to consider the **Negative days** value that is set for coverage groups.</span></span> <span data-ttu-id="b2ff1-105">Používá se k prodloužení doby tolerance zpoždění, která se použije během hlavního plánování.</span><span class="sxs-lookup"><span data-stu-id="b2ff1-105">It's used to extend the delay tolerance period that is applied during master planning.</span></span> <span data-ttu-id="b2ff1-106">Tímto způsobem se můžete vyhnout vytváření nových objednávek dodávek, pokud stávající nabídka bude schopna pokrýt poptávku po krátké prodlevě.</span><span class="sxs-lookup"><span data-stu-id="b2ff1-106">In this way, you can avoid creating new supply orders if existing supply will be able to cover the demand after a short delay.</span></span> <span data-ttu-id="b2ff1-107">Účelem této funkce je určit, zda má smysl vytvořit novou objednávku dodávky pro danou poptávku.</span><span class="sxs-lookup"><span data-stu-id="b2ff1-107">The purpose of the functionality is to determine whether it makes sense to create a new supply order for a given demand.</span></span>

## <a name="turn-on-the-feature-in-your-system"></a><span data-ttu-id="b2ff1-108">Zapnutí funkce ve vašem systému</span><span class="sxs-lookup"><span data-stu-id="b2ff1-108">Turn on the feature in your system</span></span>

<span data-ttu-id="b2ff1-109">Chcete-li funkci tolerance zpoždění ve svém systému zpřístupnit, přejděte na [Správu funkcí](../../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) a zapněte funkci *Záporné dny pro optimalizaci plánování*.</span><span class="sxs-lookup"><span data-stu-id="b2ff1-109">To make the delay tolerance functionality available in your system, go to [Feature management](../../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md), and turn on the *Negative days for Planning Optimization* feature.</span></span>

## <a name="delay-tolerance-in-planning-optimization"></a><span data-ttu-id="b2ff1-110">Tolerance zpoždění v Optimalizaci plánování</span><span class="sxs-lookup"><span data-stu-id="b2ff1-110">Delay tolerance in Planning Optimization</span></span>

<span data-ttu-id="b2ff1-111">Tolerance zpoždění představuje počet dní po dodací lhůtě, kterou jste ochotni počkat, než si objednáte nové doplnění, když je již plánovaná stávající dodávka.</span><span class="sxs-lookup"><span data-stu-id="b2ff1-111">Delay tolerance represents the number of days beyond the lead time that you're willing to wait before you order new replenishment when existing supply is already planned.</span></span> <span data-ttu-id="b2ff1-112">Tolerance zpoždění je definována pomocí kalendářních dnů, nikoli pracovních dnů.</span><span class="sxs-lookup"><span data-stu-id="b2ff1-112">Delay tolerance is defined by using calendar days, not business days.</span></span>

<span data-ttu-id="b2ff1-113">Když systém v době hlavního plánování vypočítá toleranci zpoždění, vezme v úvahu nastavení **Záporné dny**.</span><span class="sxs-lookup"><span data-stu-id="b2ff1-113">At the time of master planning, when the system calculates the delay tolerance, it considers the **Negative days** setting.</span></span> <span data-ttu-id="b2ff1-114">Hodnotu **Záporné dny** lze zadat na stránce **Skupiny disponibility** nebo **Disponibilita položky**.</span><span class="sxs-lookup"><span data-stu-id="b2ff1-114">You can set the **Negative days** value on either the **Coverage groups** page or the **Item coverage** page.</span></span>

<span data-ttu-id="b2ff1-115">Systém spojuje výpočet tolerance zpoždění s *nejbližším datem doplnění*, což se rovná dnešnímu datu plus dodací lhůta.</span><span class="sxs-lookup"><span data-stu-id="b2ff1-115">The system links the delay tolerance calculation to the *earliest replenishment date*, which equals today's date plus the lead time.</span></span> <span data-ttu-id="b2ff1-116">Tolerance zpoždění se vypočítá pomocí následujícího vzorce, kde *max()* najde větší ze dvou hodnot:</span><span class="sxs-lookup"><span data-stu-id="b2ff1-116">The delay tolerance is calculated by using following formula, where *max()* finds the larger of two values:</span></span>

<span data-ttu-id="b2ff1-117">*max(nejbližší datum doplnění, termín splnění doplnění)* – *termín splnění doplnění* + *záporné dny*</span><span class="sxs-lookup"><span data-stu-id="b2ff1-117">*max(Earliest replenishment date, Demand due date)* – *Demand due date* + *Negative days*</span></span>

<span data-ttu-id="b2ff1-118">Tento vzorec zajišťuje, že hlavní plánování nevytváří nové objednávky dodávek, pokud existuje dostatečná zásoba během doby realizace produktu.</span><span class="sxs-lookup"><span data-stu-id="b2ff1-118">This formula ensures that master planning doesn't create new supply orders when enough supply exists during the product lead time.</span></span>

> [!NOTE]
> <span data-ttu-id="b2ff1-119">Výpočet tolerance zpoždění v Optimalizaci plánování vždy používá výpočet dynamických záporných dnů z integrovaného hlavního plánování.</span><span class="sxs-lookup"><span data-stu-id="b2ff1-119">The delay tolerance calculation in Planning Optimization always uses the dynamic negative days calculation from built-in master planning.</span></span> <span data-ttu-id="b2ff1-120">Nastavení **Použít dynamické záporné dny** na stránce **Parametry hlavního plánování** nemá na toto chování žádný vliv.</span><span class="sxs-lookup"><span data-stu-id="b2ff1-120">The **Use dynamic negative days** setting on the **Master planning parameters** page has no effect on this behavior.</span></span>

<span data-ttu-id="b2ff1-121">Pokud stávající nabídka implikuje zpoždění poptávky, které je menší nebo rovné vypočítané toleranci zpoždění, Optimalizace plánování spojí stávající nabídku s poptávkou.</span><span class="sxs-lookup"><span data-stu-id="b2ff1-121">If the existing supply implies a demand delay that is less than or equal to the calculated delay tolerance, Planning Optimization pegs existing supply with the demand.</span></span> <span data-ttu-id="b2ff1-122">V některých případech je lepší odložit poptávku, než skončit s nadměrnou dodávkou.</span><span class="sxs-lookup"><span data-stu-id="b2ff1-122">In some cases, it's better to delay the demand than to end up with oversupply.</span></span>

<span data-ttu-id="b2ff1-123">Následující podsekce poskytují příklady, které ukazují, jak tolerance zpoždění ovlivňuje vytváření plánovaných objednávek v Optimalizaci plánování.</span><span class="sxs-lookup"><span data-stu-id="b2ff1-123">The following subsections provide examples that show how delay tolerance affects the creation of planned orders in Planning Optimization.</span></span>

### <a name="example-1"></a><span data-ttu-id="b2ff1-124">Příklad 1</span><span class="sxs-lookup"><span data-stu-id="b2ff1-124">Example 1</span></span>

<span data-ttu-id="b2ff1-125">Produkt má následující konfiguraci:</span><span class="sxs-lookup"><span data-stu-id="b2ff1-125">A product has the following configuration:</span></span>

- <span data-ttu-id="b2ff1-126">**Doba realizace:** *10*</span><span class="sxs-lookup"><span data-stu-id="b2ff1-126">**Lead time:** *10*</span></span>
- <span data-ttu-id="b2ff1-127">**Záporné dny:** *2*</span><span class="sxs-lookup"><span data-stu-id="b2ff1-127">**Negative days:** *2*</span></span>

<span data-ttu-id="b2ff1-128">Po produktu existuje následující nabídka a poptávka:</span><span class="sxs-lookup"><span data-stu-id="b2ff1-128">The following supply and demand exist for the product:</span></span>

- <span data-ttu-id="b2ff1-129">**Poptávka pro dnešek:** Prodejní objednávka na množství 10</span><span class="sxs-lookup"><span data-stu-id="b2ff1-129">**Demand for today:** A sales order for a quantity of 10</span></span>
- <span data-ttu-id="b2ff1-130">**Dodávka za 12 dnů:** Nákupní objednávka na množství 10</span><span class="sxs-lookup"><span data-stu-id="b2ff1-130">**Supply in 12 days:** A purchase order for a quantity of 10</span></span>

<span data-ttu-id="b2ff1-131">Stávající nabídka může pokrýt poptávku do 12 dnů a toto období se rovná toleranci zpoždění.</span><span class="sxs-lookup"><span data-stu-id="b2ff1-131">Existing supply can cover the demand within 12 days, and that period equals the delay tolerance.</span></span> <span data-ttu-id="b2ff1-132">Proto při spuštění hlavního plánování nejsou vytvářeny žádné plánované objednávky.</span><span class="sxs-lookup"><span data-stu-id="b2ff1-132">Therefore, when master planning runs, no planned orders are created.</span></span>

### <a name="example-2"></a><span data-ttu-id="b2ff1-133">Příklad 2</span><span class="sxs-lookup"><span data-stu-id="b2ff1-133">Example 2</span></span>

<span data-ttu-id="b2ff1-134">Produkt má následující konfiguraci:</span><span class="sxs-lookup"><span data-stu-id="b2ff1-134">A product has the following configuration:</span></span>

- <span data-ttu-id="b2ff1-135">**Doba realizace:** *10*</span><span class="sxs-lookup"><span data-stu-id="b2ff1-135">**Lead time:** *10*</span></span>
- <span data-ttu-id="b2ff1-136">**Záporné dny:** *0*</span><span class="sxs-lookup"><span data-stu-id="b2ff1-136">**Negative days:** *0*</span></span>

<span data-ttu-id="b2ff1-137">Po produktu existuje následující nabídka a poptávka:</span><span class="sxs-lookup"><span data-stu-id="b2ff1-137">The following supply and demand exist for the product:</span></span>

- <span data-ttu-id="b2ff1-138">**Poptávka pro dnešek:** Prodejní objednávka na množství 10</span><span class="sxs-lookup"><span data-stu-id="b2ff1-138">**Demand for today:** A sales order for a quantity of 10</span></span>
- <span data-ttu-id="b2ff1-139">**Dodávka za 12 dnů:** Nákupní objednávka na množství 10</span><span class="sxs-lookup"><span data-stu-id="b2ff1-139">**Supply in 12 days:** A purchase order for a quantity of 10</span></span>

<span data-ttu-id="b2ff1-140">Stávající nabídka může pokrýt poptávku až po 12 dnech.</span><span class="sxs-lookup"><span data-stu-id="b2ff1-140">Existing supply can cover the demand only after 12 days.</span></span> <span data-ttu-id="b2ff1-141">Tolerance zpoždění je však 10 dní.</span><span class="sxs-lookup"><span data-stu-id="b2ff1-141">However, the delay tolerance is 10 days.</span></span> <span data-ttu-id="b2ff1-142">Při spuštění hlavního plánování se proto vytvoří plánovaná objednávka pro množství 10.</span><span class="sxs-lookup"><span data-stu-id="b2ff1-142">Therefore, when master planning runs, a planned order for a quantity of 10 is created.</span></span>

### <a name="example-3"></a><span data-ttu-id="b2ff1-143">Příklad 3</span><span class="sxs-lookup"><span data-stu-id="b2ff1-143">Example 3</span></span>

<span data-ttu-id="b2ff1-144">Produkt má následující konfiguraci:</span><span class="sxs-lookup"><span data-stu-id="b2ff1-144">A product has the following configuration:</span></span>

- <span data-ttu-id="b2ff1-145">**Doba realizace:** *10*</span><span class="sxs-lookup"><span data-stu-id="b2ff1-145">**Lead time:** *10*</span></span>
- <span data-ttu-id="b2ff1-146">**Záporné dny:** *2*</span><span class="sxs-lookup"><span data-stu-id="b2ff1-146">**Negative days:** *2*</span></span>

<span data-ttu-id="b2ff1-147">Po produktu existuje následující nabídka a poptávka:</span><span class="sxs-lookup"><span data-stu-id="b2ff1-147">The following supply and demand exist for the product:</span></span>

- <span data-ttu-id="b2ff1-148">**Poptávka za 11 dnů:** Prodejní objednávka na množství 10</span><span class="sxs-lookup"><span data-stu-id="b2ff1-148">**Demand in 11 days:** A sales order for a quantity of 10</span></span>
- <span data-ttu-id="b2ff1-149">**Dodávka za 14 dnů:** Nákupní objednávka na množství 10</span><span class="sxs-lookup"><span data-stu-id="b2ff1-149">**Supply in 14 days:** A purchase order for a quantity of 10</span></span>

<span data-ttu-id="b2ff1-150">Stávající nabídka může pokrýt poptávku až po třech dnech.</span><span class="sxs-lookup"><span data-stu-id="b2ff1-150">Existing supply can cover the demand only after three days.</span></span> <span data-ttu-id="b2ff1-151">Tolerance zpoždění jsou však 2 dny.</span><span class="sxs-lookup"><span data-stu-id="b2ff1-151">However, the delay tolerance is two days.</span></span> <span data-ttu-id="b2ff1-152">(V tomto případě tolerance zpoždění zahrnuje pouze dva záporné dny.</span><span class="sxs-lookup"><span data-stu-id="b2ff1-152">(In this case, the delay tolerance includes only the two negative days.</span></span> <span data-ttu-id="b2ff1-153">Datum poptávky není zahrnuto, protože je po dodací lhůtě produktu.) Proto se při spuštění hlavního plánování vytvoří plánovaná objednávka na množství 10.</span><span class="sxs-lookup"><span data-stu-id="b2ff1-153">The demand date isn't included because it's after the product lead time.) Therefore, when master planning runs, a planned order for a quantity of 10 is created.</span></span>
