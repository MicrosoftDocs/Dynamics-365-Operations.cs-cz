---
title: Přepravní kontejnery
description: Toto téma popisuje, jak nastavit přepravní kontejnery pro modul nákladů za doručení.
author: sherry-zheng
ms.date: 12/09/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ITMContainerTypeTable, ITMContainerTable, ITMContainerUnitTypeTable, ITMRefrigerationTypeTable, ITMContainersListPage, ITMContainers
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2020-12-09
ms.dyn365.ops.version: Release 10.0.17
ms.openlocfilehash: 2f7e9435aa3d0d06e1cc51457a6343b807d76dc7
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/01/2021
ms.locfileid: "5833706"
---
# <a name="shipping-container-setup"></a><span data-ttu-id="6e116-103">Nastavení přepravního kontejneru</span><span class="sxs-lookup"><span data-stu-id="6e116-103">Shipping container setup</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="6e116-104">Toto téma popisuje, jak nastavit přepravní kontejnery pro modul **Náklady za doručení**.</span><span class="sxs-lookup"><span data-stu-id="6e116-104">This topic describes how to set up shipping containers for the **Landed cost** module.</span></span>

## <a name="set-up-shipping-container-types"></a><a id="shipping-container-types"></a><span data-ttu-id="6e116-105">Nastavení typů přepravních kontejnerů</span><span class="sxs-lookup"><span data-stu-id="6e116-105">Set up shipping container types</span></span>

<span data-ttu-id="6e116-106">Typy přepravních kontejnerů definují typy přepravních kontejnerů, které jsou k dispozici pro použití během přepravy a plavby.</span><span class="sxs-lookup"><span data-stu-id="6e116-106">Shipping container types define the types of shipping containers that are available for use during shipping and voyages.</span></span>

<span data-ttu-id="6e116-107">Chcete-li pracovat s typy přepravních kontejnerů, přejděte na **Náklady na doručení \> Nastavení kontejnerů \> Typy přepravních kontejnerů**.</span><span class="sxs-lookup"><span data-stu-id="6e116-107">To work with the shipping container types, go to **Landed cost \> Containers setup \> Shipping container types**.</span></span> <span data-ttu-id="6e116-108">Zde můžete prohlížet, přidávat a odebírat záznamy o vašich typech kontejnerů.</span><span class="sxs-lookup"><span data-stu-id="6e116-108">There, you can view, add, and remove records for your container types.</span></span> <span data-ttu-id="6e116-109">V následující tabulce jsou popsána pole, která jsou k dispozici pro každý záznam.</span><span class="sxs-lookup"><span data-stu-id="6e116-109">The following table describes the fields that are available for each record.</span></span>

| <span data-ttu-id="6e116-110">Pole</span><span class="sxs-lookup"><span data-stu-id="6e116-110">Field</span></span> | <span data-ttu-id="6e116-111">popis</span><span class="sxs-lookup"><span data-stu-id="6e116-111">Description</span></span> |
|---|---|
| <span data-ttu-id="6e116-112">Typ přepravního kontejneru</span><span class="sxs-lookup"><span data-stu-id="6e116-112">Shipping container type</span></span> | <span data-ttu-id="6e116-113">Zadejte jedinečný identifikační název/číslo přepravního kontejneru.</span><span class="sxs-lookup"><span data-stu-id="6e116-113">Enter a unique identification name/number for the shipping container type.</span></span> |
| <span data-ttu-id="6e116-114">popis</span><span class="sxs-lookup"><span data-stu-id="6e116-114">Description</span></span> | <span data-ttu-id="6e116-115">Zadejte popis skupiny typů nákladů přepravních kontejnerů.</span><span class="sxs-lookup"><span data-stu-id="6e116-115">Enter a description of the shipping container type.</span></span> |
| <span data-ttu-id="6e116-116">Objem</span><span class="sxs-lookup"><span data-stu-id="6e116-116">Volume</span></span> | <span data-ttu-id="6e116-117">Zadejte maximální povolený objem v přepravních kontejnerech tohoto typu.</span><span class="sxs-lookup"><span data-stu-id="6e116-117">Enter the maximum volume that is allowed in shipping containers of this type.</span></span> |
| <span data-ttu-id="6e116-118">Váha</span><span class="sxs-lookup"><span data-stu-id="6e116-118">Weight</span></span> | <span data-ttu-id="6e116-119">Zadejte maximální povolenou hmotnost v přepravních kontejnerech tohoto typu.</span><span class="sxs-lookup"><span data-stu-id="6e116-119">Enter the maximum weight that is allowed in shipping containers of this type.</span></span> |
| <span data-ttu-id="6e116-120">Vratný</span><span class="sxs-lookup"><span data-stu-id="6e116-120">Returnable</span></span> | <span data-ttu-id="6e116-121">Určete, zda lze přepravní kontejnery tohoto typu vrátit prodejci po jejich použití během plavby.</span><span class="sxs-lookup"><span data-stu-id="6e116-121">Specify whether shipping containers of this type can be returned to the vendor after they are used during a voyage.</span></span> <span data-ttu-id="6e116-122">Pokud je tato možnost nastavena na *Ano*, mohou se na vrácení přepravních kontejnerů tohoto typu do přístavu původu vztahovat další náklady.</span><span class="sxs-lookup"><span data-stu-id="6e116-122">If this option is set to *Yes*, additional costs might apply for the return of shipping containers of this type to the port of origin.</span></span> |

## <a name="set-up-shipping-containers"></a><span data-ttu-id="6e116-123">Nastavení přepravních kontejnerů</span><span class="sxs-lookup"><span data-stu-id="6e116-123">Set up shipping containers</span></span>

<span data-ttu-id="6e116-124">Záznamy přepravních kontejnerů slouží k identifikaci každého kontejneru, který používáte během plavby.</span><span class="sxs-lookup"><span data-stu-id="6e116-124">You use shipping container records to identify each container that you use during voyages.</span></span> <span data-ttu-id="6e116-125">Když vytvoříte cestu, můžete pro ni vybrat konkrétní kontejner v seznamu všech záznamů přepravního kontejneru, které jste zde definovali.</span><span class="sxs-lookup"><span data-stu-id="6e116-125">When you create a voyage, you can select a specific container for it in the list of all the shipping container records that you've defined here.</span></span> <span data-ttu-id="6e116-126">Tato funkce je obzvláště užitečná, pokud má vaše společnost vlastní přepravní kontejnery.</span><span class="sxs-lookup"><span data-stu-id="6e116-126">This feature is especially useful if your company owns its own shipping containers.</span></span>

<span data-ttu-id="6e116-127">U přepravních kontejnerů, které budou použity pouze jednou, nemusíte zadávat čísla přepravních kontejnerů.</span><span class="sxs-lookup"><span data-stu-id="6e116-127">You don't have to enter shipping container numbers for shipping containers that will be used only one time.</span></span> <span data-ttu-id="6e116-128">Místo toho můžete při vytváření cesty přidat číslo přepravního kontejneru.</span><span class="sxs-lookup"><span data-stu-id="6e116-128">Instead, you can add the shipping container number when you create a voyage.</span></span>

<span data-ttu-id="6e116-129">Záznamy přepravního kontejneru se používají pouze v nákladech za doručení.</span><span class="sxs-lookup"><span data-stu-id="6e116-129">Shipping container records are used only in Landed cost.</span></span> <span data-ttu-id="6e116-130">Nejsou k dispozici ve standardním modulu **Správa přepravy** (TMS).</span><span class="sxs-lookup"><span data-stu-id="6e116-130">They aren't available in the standard **Transportation management** module (TMS).</span></span>

<span data-ttu-id="6e116-131">Chcete-li pracovat s přepravními kontejnery, přejděte na **Náklady na doručení \> Nastavení kontejnerů \> Přepravní kontejnery**.</span><span class="sxs-lookup"><span data-stu-id="6e116-131">To work with shipping containers, go to **Landed cost \> Containers setup \> Shipping containers**.</span></span> <span data-ttu-id="6e116-132">Zde můžete prohlížet, přidávat a odebírat záznamy o vašich přepravních kontejnerech.</span><span class="sxs-lookup"><span data-stu-id="6e116-132">There, you can view, add, and remove records your shipping containers.</span></span> <span data-ttu-id="6e116-133">V následující tabulce jsou popsána pole, která jsou k dispozici pro každý záznam.</span><span class="sxs-lookup"><span data-stu-id="6e116-133">The following table describes the fields that are available for each record.</span></span>

| <span data-ttu-id="6e116-134">Pole</span><span class="sxs-lookup"><span data-stu-id="6e116-134">Field</span></span> | <span data-ttu-id="6e116-135">popis</span><span class="sxs-lookup"><span data-stu-id="6e116-135">Description</span></span> |
|---|---|
| <span data-ttu-id="6e116-136">Přepravní kontejner</span><span class="sxs-lookup"><span data-stu-id="6e116-136">Shipping container</span></span> | <span data-ttu-id="6e116-137">Zadejte jedinečný identifikační název/číslo přepravního kontejneru.</span><span class="sxs-lookup"><span data-stu-id="6e116-137">Enter a unique identification name/number for the shipping container.</span></span> |
| <span data-ttu-id="6e116-138">Typ přepravního kontejneru</span><span class="sxs-lookup"><span data-stu-id="6e116-138">Shipping container type</span></span> | <span data-ttu-id="6e116-139">Vyberte typ přepravního kontejneru.</span><span class="sxs-lookup"><span data-stu-id="6e116-139">Select the type of shipping container.</span></span> <span data-ttu-id="6e116-140">Další informace naleznete v části [Nastavení typů přepravních kontejnerů](#shipping-container-types) dříve v tomto tématu.</span><span class="sxs-lookup"><span data-stu-id="6e116-140">For more information, see the [Set up shipping container types](#shipping-container-types) section earlier in this topic.</span></span> |

> [!NOTE]
> - <span data-ttu-id="6e116-141">Nastavení přepravního kontejneru je volitelné.</span><span class="sxs-lookup"><span data-stu-id="6e116-141">The shipping container setup is optional.</span></span> <span data-ttu-id="6e116-142">Obvykle jej použijete, pouze pokud má vaše společnost vlastní přepravní kontejnery nebo často znovu používá stejné přepravní kontejnery.</span><span class="sxs-lookup"><span data-stu-id="6e116-142">Typically, you will use it only if your company owns its own shipping containers or often reuses the same shipping containers.</span></span>
> - <span data-ttu-id="6e116-143">Pro čísla přepravních kontejnerů se nepočítají žádné kontrolní číslice.</span><span class="sxs-lookup"><span data-stu-id="6e116-143">No check digits are calculated for shipping container numbers.</span></span>

## <a name="set-up-unit-types"></a><a name="unit-types"></a><span data-ttu-id="6e116-144">Nastavení typů jednotky</span><span class="sxs-lookup"><span data-stu-id="6e116-144">Set up unit types</span></span>

<span data-ttu-id="6e116-145">Typy jednotek vytvářejí další seskupení a způsoby identifikace přepravních kontejnerů.</span><span class="sxs-lookup"><span data-stu-id="6e116-145">Unit types establish additional groupings and identification methods for shipping containers.</span></span> <span data-ttu-id="6e116-146">Typ jednotky se obvykle používá k identifikaci typu kontejneru, do kterého je zboží zabaleno, jako jsou palety nebo sudy.</span><span class="sxs-lookup"><span data-stu-id="6e116-146">The unit type is typically used to identify the type of container that goods are packaged in, such as pallets or drums.</span></span> <span data-ttu-id="6e116-147">Při nastavování typu kontejneru na stránce **všechny přepravní kontejnery** můžete vybrat typ jednotky.</span><span class="sxs-lookup"><span data-stu-id="6e116-147">You can select a unit type when you set up a container on the **All shipping containers** page.</span></span>

<span data-ttu-id="6e116-148">Typy jednotek se používají pouze v ceně nákladů za doručení.</span><span class="sxs-lookup"><span data-stu-id="6e116-148">Unit types are used only in Landed cost.</span></span> <span data-ttu-id="6e116-149">Nejsou k dispozici v TMS.</span><span class="sxs-lookup"><span data-stu-id="6e116-149">They aren't available in TMS.</span></span>

<span data-ttu-id="6e116-150">Chcete-li pracovat s typy jednotky, přejděte na **Náklady na doručení \> Nastavení kontejnerů \> Typy jednotky**.</span><span class="sxs-lookup"><span data-stu-id="6e116-150">To work with unit types, go to **Landed cost \> Containers setup \> Unit types**.</span></span> <span data-ttu-id="6e116-151">Zde můžete prohlížet, přidávat a odebírat záznamy o vašich typech jednotky.</span><span class="sxs-lookup"><span data-stu-id="6e116-151">There, you can view, add, and remove records for your unit types.</span></span> <span data-ttu-id="6e116-152">V následující tabulce jsou popsána pole, která jsou k dispozici pro každý záznam.</span><span class="sxs-lookup"><span data-stu-id="6e116-152">The following table describes the fields that are available for each record.</span></span>

| <span data-ttu-id="6e116-153">Pole</span><span class="sxs-lookup"><span data-stu-id="6e116-153">Field</span></span> | <span data-ttu-id="6e116-154">popis</span><span class="sxs-lookup"><span data-stu-id="6e116-154">Description</span></span> |
|---|---|
| <span data-ttu-id="6e116-155">Typ jednotky</span><span class="sxs-lookup"><span data-stu-id="6e116-155">Unit type</span></span> | <span data-ttu-id="6e116-156">Zadejte jedinečný identifikační název/číslo typu jednotky.</span><span class="sxs-lookup"><span data-stu-id="6e116-156">Enter a unique identification name/number for the unit type.</span></span> |
| <span data-ttu-id="6e116-157">popis</span><span class="sxs-lookup"><span data-stu-id="6e116-157">Description</span></span> | <span data-ttu-id="6e116-158">Zadejte popis typu jednotky.</span><span class="sxs-lookup"><span data-stu-id="6e116-158">Enter a description of the unit type.</span></span> |

## <a name="set-up-refrigeration-types"></a><a name="refrigeration-types"></a><span data-ttu-id="6e116-159">Nastavení typů chlazení</span><span class="sxs-lookup"><span data-stu-id="6e116-159">Set up refrigeration types</span></span>

<span data-ttu-id="6e116-160">Typy chlazení nastavují další metody seskupení a identifikace pro dopravní kontejnery (obvykle chlazené kontejnery).</span><span class="sxs-lookup"><span data-stu-id="6e116-160">Refrigeration types establish additional groupings and identification methods for shipping containers (usually refrigerated containers).</span></span> <span data-ttu-id="6e116-161">Při nastavování typu kontejneru na stránce **všechny přepravní kontejnery** můžete vybrat typ chlazení.</span><span class="sxs-lookup"><span data-stu-id="6e116-161">You can select a refrigeration type when you set up a container on the **All shipping containers** page.</span></span>

<span data-ttu-id="6e116-162">Chcete-li pracovat s typy chlazení, přejděte na **Náklady na doručení \> Nastavení kontejnerů \> Typy chlazení**.</span><span class="sxs-lookup"><span data-stu-id="6e116-162">To work with refrigeration types, go to **Landed cost \> Containers setup \> Refrigeration types**.</span></span> <span data-ttu-id="6e116-163">Zde můžete prohlížet, přidávat a odebírat záznamy o vašich typech chlazení.</span><span class="sxs-lookup"><span data-stu-id="6e116-163">There, you can view, add, and remove records for your refrigeration types.</span></span> <span data-ttu-id="6e116-164">V následující tabulce jsou popsána pole, která jsou k dispozici pro každý záznam.</span><span class="sxs-lookup"><span data-stu-id="6e116-164">The following table describes the fields that are available for each record.</span></span>

| <span data-ttu-id="6e116-165">Pole</span><span class="sxs-lookup"><span data-stu-id="6e116-165">Field</span></span> | <span data-ttu-id="6e116-166">popis</span><span class="sxs-lookup"><span data-stu-id="6e116-166">Description</span></span> |
|---|---|
| <span data-ttu-id="6e116-167">Typ chlazení</span><span class="sxs-lookup"><span data-stu-id="6e116-167">Refrigeration type</span></span> | <span data-ttu-id="6e116-168">Zadejte jedinečný identifikační název/číslo typu chlazení.</span><span class="sxs-lookup"><span data-stu-id="6e116-168">Enter a unique identification name/number for the refrigeration type.</span></span> |
| <span data-ttu-id="6e116-169">popis</span><span class="sxs-lookup"><span data-stu-id="6e116-169">Description</span></span> | <span data-ttu-id="6e116-170">Zadejte stručný popis typu chlazení.</span><span class="sxs-lookup"><span data-stu-id="6e116-170">Enter a description of the refrigeration type.</span></span> |
