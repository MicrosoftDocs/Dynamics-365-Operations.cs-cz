---
title: Plánování se záporným množstvím na skladě
description: Toto téma vysvětluje, jak je při použití optimalizace plánování zpracováno záporné množství na skladě.
author: ChristianRytt
manager: tfehr
ms.date: 02/18/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqCreatePlanWorkspace
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2020-02-18
ms.dyn365.ops.version: AX 10.0.5
ms.openlocfilehash: 72367927a11879adffe68d7242d88f5cfab73e22
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/13/2020
ms.locfileid: "4423784"
---
# <a name="planning-with-negative-on-hand-quantities"></a><span data-ttu-id="49a1e-103">Plánování se záporným množstvím na skladě</span><span class="sxs-lookup"><span data-stu-id="49a1e-103">Planning with negative on-hand quantities</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="49a1e-104">Pokud systém zobrazí záporné celkové množství na skladě, modul plánování zpracuje toto množství jako hodnotu 0 (nula), aby se zabránilo překročení dodávky.</span><span class="sxs-lookup"><span data-stu-id="49a1e-104">If the system shows a negative aggregate on-hand quantity, the planning engine treats the quantity as 0 (zero) to help avoid over-supply.</span></span> <span data-ttu-id="49a1e-105">Tato funkce funguje zde:</span><span class="sxs-lookup"><span data-stu-id="49a1e-105">Here is how this functionality works:</span></span>

1. <span data-ttu-id="49a1e-106">Funkce optimalizace plánování agreguje množství na skladě na nejnižší úrovni dimenzí disponibility.</span><span class="sxs-lookup"><span data-stu-id="49a1e-106">The planning optimization feature aggregates on-hand quantities at the lowest level of coverage dimensions.</span></span> <span data-ttu-id="49a1e-107">(Pokud například *skladové místo* není dimenze disponibility, optimalizace plánování agreguje množství na skladě na úrovni *skladu*.)</span><span class="sxs-lookup"><span data-stu-id="49a1e-107">(For example, if *location* isn't a coverage dimension, planning optimization aggregates on-hand quantities at the *warehouse* level.)</span></span>
1. <span data-ttu-id="49a1e-108">Pokud je celkové množství na skladě na nejnižší úrovni dimenzí disponibility záporné, systém předpokládá, že množství na skladě je skutečně 0 (nula).</span><span class="sxs-lookup"><span data-stu-id="49a1e-108">If the aggregate on-hand quantity at the lowest level of coverage dimensions is negative, the system assumes that the on-hand quantity is really 0 (zero).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="49a1e-109">Plánovací systém může být pouze tak přesný jako vstupní data.</span><span class="sxs-lookup"><span data-stu-id="49a1e-109">The planning system can be only as precise as the input data.</span></span> <span data-ttu-id="49a1e-110">Pokud jsou vstupní data nepřesná, záporné záznamy na skladě budou označovat, že informace o zásobách v Microsoft Dynamics 365 Supply Chain Management nejsou synchronizované se skutečným světem.</span><span class="sxs-lookup"><span data-stu-id="49a1e-110">If the input data is inaccurate, negative on-hand records will indicate that the inventory information in Microsoft Dynamics 365 Supply Chain Management is out of sync with the real world.</span></span> <span data-ttu-id="49a1e-111">Z toho vyplývá, že výsledkem plánování bude chyba.</span><span class="sxs-lookup"><span data-stu-id="49a1e-111">Therefore, the planning result will be flawed.</span></span> <span data-ttu-id="49a1e-112">Chcete-li získat přesný výsledek plánování, měli byste minimalizovat počet záznamů, které zobrazují záporné množství na skladě.</span><span class="sxs-lookup"><span data-stu-id="49a1e-112">To get a precise planning result, you should minimize the number of records that show a negative on-hand quantity.</span></span>

## <a name="example-1"></a><span data-ttu-id="49a1e-113">Příklad 1</span><span class="sxs-lookup"><span data-stu-id="49a1e-113">Example 1</span></span>

<span data-ttu-id="49a1e-114">Sklad 13 je nakonfigurován následujícím způsobem:</span><span class="sxs-lookup"><span data-stu-id="49a1e-114">Warehouse 13 is configured in the following manner:</span></span>

- <span data-ttu-id="49a1e-115">**Kód disponibility:** Min./Max.</span><span class="sxs-lookup"><span data-stu-id="49a1e-115">**Coverage code:** Min./Max.</span></span>
- <span data-ttu-id="49a1e-116">**Minimum:** 15 kusů (KS)</span><span class="sxs-lookup"><span data-stu-id="49a1e-116">**Minimum:** 15 pieces (pcs.)</span></span>
- <span data-ttu-id="49a1e-117">**Maximum:** 25 kusů</span><span class="sxs-lookup"><span data-stu-id="49a1e-117">**Maximum:** 25 pcs.</span></span>

<span data-ttu-id="49a1e-118">Nejnižší úroveň dimenzí disponibility je *sklad* a následující množství na skladě se zaznamenávají na úrovni *skladového místa*:</span><span class="sxs-lookup"><span data-stu-id="49a1e-118">The lowest level of coverage dimensions is *warehouse*, and the following on-hand quantities are recorded at the *location* level:</span></span>

- <span data-ttu-id="49a1e-119">**Pracoviště 1, sklad 13, skl. místo 1** 20 kusů.</span><span class="sxs-lookup"><span data-stu-id="49a1e-119">**Site 1, warehouse 13, location 1:** 20 pcs.</span></span>
- <span data-ttu-id="49a1e-120">**Pracoviště 1, sklad 13, skl. místo 2:** &minus;8 ks.</span><span class="sxs-lookup"><span data-stu-id="49a1e-120">**Site 1 warehouse 13, location 2:** &minus;8 pcs.</span></span>

<span data-ttu-id="49a1e-121">Proto je celkové množství na skladě pro sklad 13 12 kusů.</span><span class="sxs-lookup"><span data-stu-id="49a1e-121">Therefore, the aggregate on-hand quantity for warehouse 13 is 12 pcs.</span></span> <span data-ttu-id="49a1e-122">(= 20 ks.</span><span class="sxs-lookup"><span data-stu-id="49a1e-122">(= 20 pcs.</span></span> <span data-ttu-id="49a1e-123">&minus; 8 ks.).</span><span class="sxs-lookup"><span data-stu-id="49a1e-123">&minus; 8 pcs.).</span></span>

<span data-ttu-id="49a1e-124">V tomto případě plánovací modul využívá celkové množství na skladě 12 ks.</span><span class="sxs-lookup"><span data-stu-id="49a1e-124">In this case, the planning engine uses an aggregate on-hand quantity of 12 pcs.</span></span> <span data-ttu-id="49a1e-125">pro sklad 13.</span><span class="sxs-lookup"><span data-stu-id="49a1e-125">for warehouse 13.</span></span>

<span data-ttu-id="49a1e-126">Výsledkem je plánovaná objednávka na 13 kusů.</span><span class="sxs-lookup"><span data-stu-id="49a1e-126">The result is a planned order of 13 pcs.</span></span> <span data-ttu-id="49a1e-127">(= 25 ks.</span><span class="sxs-lookup"><span data-stu-id="49a1e-127">(= 25 pcs.</span></span> <span data-ttu-id="49a1e-128">&minus;12 kusů.) pro doplnění skladu 13 z 12 ks.</span><span class="sxs-lookup"><span data-stu-id="49a1e-128">&minus; 12 pcs.) to refill warehouse 13 from 12 pcs.</span></span> <span data-ttu-id="49a1e-129">na 25 ks.</span><span class="sxs-lookup"><span data-stu-id="49a1e-129">to 25 pcs.</span></span>

## <a name="example-2"></a><span data-ttu-id="49a1e-130">Příklad 2</span><span class="sxs-lookup"><span data-stu-id="49a1e-130">Example 2</span></span>

<span data-ttu-id="49a1e-131">Sklad 13 je nakonfigurován následujícím způsobem:</span><span class="sxs-lookup"><span data-stu-id="49a1e-131">Warehouse 13 is configured in the following manner:</span></span>

- <span data-ttu-id="49a1e-132">**Kód disponibility:** Min./Max.</span><span class="sxs-lookup"><span data-stu-id="49a1e-132">**Coverage code:** Min./Max.</span></span>
- <span data-ttu-id="49a1e-133">**Minimum:** 15 ks.</span><span class="sxs-lookup"><span data-stu-id="49a1e-133">**Minimum:** 15 pcs.</span></span>
- <span data-ttu-id="49a1e-134">**Maximum:** 25 ks.</span><span class="sxs-lookup"><span data-stu-id="49a1e-134">**Maximum:** 25 pcs.</span></span>

<span data-ttu-id="49a1e-135">Nejnižší úroveň dimenzí disponibility je *sklad* a následující množství na skladě se zaznamenávají na úrovni *skladového místa*:</span><span class="sxs-lookup"><span data-stu-id="49a1e-135">The lowest level of coverage dimensions is *warehouse*, and the following on-hand quantities are recorded at the *location* level:</span></span>

- <span data-ttu-id="49a1e-136">**Pracoviště 1, sklad 13, skl. místo 1** 4 ks.</span><span class="sxs-lookup"><span data-stu-id="49a1e-136">**Site 1, warehouse 13, location 1:** 4 pcs.</span></span>
- <span data-ttu-id="49a1e-137">**Pracoviště 1, sklad 13, skl. místo 2:** &minus;8 ks.</span><span class="sxs-lookup"><span data-stu-id="49a1e-137">**Site 1 warehouse 13, location 2:** &minus;8 pcs.</span></span>

<span data-ttu-id="49a1e-138">Proto je celkové množství na skladě pro sklad 13 je &minus;4 ks.</span><span class="sxs-lookup"><span data-stu-id="49a1e-138">Therefore, the aggregate on-hand quantity for warehouse 13 is &minus;4 pcs.</span></span> <span data-ttu-id="49a1e-139">(= 4 ks.</span><span class="sxs-lookup"><span data-stu-id="49a1e-139">(= 4 pcs.</span></span> <span data-ttu-id="49a1e-140">&minus; 8 ks.).</span><span class="sxs-lookup"><span data-stu-id="49a1e-140">&minus; 8 pcs.).</span></span> <span data-ttu-id="49a1e-141">Jinými slovy, jedná se o méně než 0 (nula).</span><span class="sxs-lookup"><span data-stu-id="49a1e-141">In other words, it's less than 0 (zero).</span></span>

<span data-ttu-id="49a1e-142">V tomto případě plánovací modul předpokládá, že množství na skladě pro sklad 13 je 0 ks.</span><span class="sxs-lookup"><span data-stu-id="49a1e-142">In this case, the planning engine assumes that the on-hand quantity for warehouse 13 is 0 pcs.</span></span> <span data-ttu-id="49a1e-143">místo &minus;4 ks.</span><span class="sxs-lookup"><span data-stu-id="49a1e-143">instead of &minus;4 pcs.</span></span>

<span data-ttu-id="49a1e-144">Výsledkem je plánovaná objednávka na 25 kusů.</span><span class="sxs-lookup"><span data-stu-id="49a1e-144">The result is a planned order of 25 pcs.</span></span> <span data-ttu-id="49a1e-145">(= 25 ks.</span><span class="sxs-lookup"><span data-stu-id="49a1e-145">(= 25 pcs.</span></span> <span data-ttu-id="49a1e-146">&minus;0 kusů.) pro doplnění skladu 13 z 0 ks.</span><span class="sxs-lookup"><span data-stu-id="49a1e-146">&minus; 0 pcs.) to refill warehouse 13 from 0 pcs.</span></span> <span data-ttu-id="49a1e-147">na 25 ks.</span><span class="sxs-lookup"><span data-stu-id="49a1e-147">to 25 pcs.</span></span>

## <a name="related-resources"></a><span data-ttu-id="49a1e-148">Související prostředky</span><span class="sxs-lookup"><span data-stu-id="49a1e-148">Related resources</span></span>

[<span data-ttu-id="49a1e-149">Přehled optimalizace plánování</span><span class="sxs-lookup"><span data-stu-id="49a1e-149">Planning Optimization overview</span></span>](planning-optimization-overview.md)

[<span data-ttu-id="49a1e-150">Začínáme s optimalizací plánování</span><span class="sxs-lookup"><span data-stu-id="49a1e-150">Get started with Planning Optimization</span></span>](get-started.md)

[<span data-ttu-id="49a1e-151">Analýza přizpůsobení pro optimalizaci plánování</span><span class="sxs-lookup"><span data-stu-id="49a1e-151">Planning Optimization fit analysis</span></span>](planning-optimization-fit-analysis.md)

[<span data-ttu-id="49a1e-152">Zobrazení historie plánu a protokolů plánování</span><span class="sxs-lookup"><span data-stu-id="49a1e-152">View plan history and planning logs</span></span>](plan-history-logs.md)

[<span data-ttu-id="49a1e-153">Zrušení úlohy plánování</span><span class="sxs-lookup"><span data-stu-id="49a1e-153">Cancel a planning job</span></span>](cancel-planning-job.md)
