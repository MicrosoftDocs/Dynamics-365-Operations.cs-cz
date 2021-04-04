---
title: Nastavení informací o přepravě
description: Toto téma popisuje, jak nastavit informace o přepravě pro modul nákladů za doručení.
author: sherry-zheng
manager: tfehr
ms.date: 12/04/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ITMGoodsDescriptionTable, ITMVesselTable, ITMExporterTable, ITMCommodityCodeTable, ITMCustomsDescription
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2020-12-04
ms.dyn365.ops.version: Release 10.0.17
ms.openlocfilehash: 90794a154eb2a63f33277383cda80323dafd77b0
ms.sourcegitcommit: 2b4809e60974e72df9476ffd62706b1bfc8da4a7
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/04/2021
ms.locfileid: "5500927"
---
# <a name="shipping-information-setup"></a><span data-ttu-id="d75c8-103">Nastavení informací o přepravě</span><span class="sxs-lookup"><span data-stu-id="d75c8-103">Shipping information setup</span></span>

[!include [banner](../../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

<span data-ttu-id="d75c8-104">Toto téma popisuje, jak nastavit informace o přepravě pro modul **nákladů za doručení**.</span><span class="sxs-lookup"><span data-stu-id="d75c8-104">This topic describes how to set up shipping information for the **Landed cost** module.</span></span>

## <a name="description-of-goods"></a><a name="description-of-goods"></a><span data-ttu-id="d75c8-105">Popis zboží</span><span class="sxs-lookup"><span data-stu-id="d75c8-105">Description of goods</span></span>

<span data-ttu-id="d75c8-106">Popisy zboží pomáhají identifikovat cestu, přepravní kontejner nebo folio zboží a zboží v něm.</span><span class="sxs-lookup"><span data-stu-id="d75c8-106">Descriptions of goods help identify a voyage, shipping container, or folio of goods, and the goods in it.</span></span> <span data-ttu-id="d75c8-107">Popis zboží můžete vybrat v záhlaví přepravního kontejneru nebo záhlaví folia.</span><span class="sxs-lookup"><span data-stu-id="d75c8-107">You can select a description of goods on the shipping container header or the folio header.</span></span>

<span data-ttu-id="d75c8-108">Chcete-li pracovat s popisy zboží, přejděte na **Náklady za doručení \> Nastavení informací o přepravě \> Popis zboží**.</span><span class="sxs-lookup"><span data-stu-id="d75c8-108">To work with descriptions of goods, go to **Landed cost \> Shipping information setup \> Description of goods**.</span></span> <span data-ttu-id="d75c8-109">Zde můžete prohlížet, otevírat, vytvářet a mazat záznamy popisů zboží.</span><span class="sxs-lookup"><span data-stu-id="d75c8-109">There, you can view, open, create, and delete records for descriptions of goods.</span></span> <span data-ttu-id="d75c8-110">V následující tabulce jsou popsána pole, která jsou k dispozici pro každý záznam.</span><span class="sxs-lookup"><span data-stu-id="d75c8-110">The following table describes the fields that are available for each record.</span></span>

| <span data-ttu-id="d75c8-111">Pole</span><span class="sxs-lookup"><span data-stu-id="d75c8-111">Field</span></span> | <span data-ttu-id="d75c8-112">popis</span><span class="sxs-lookup"><span data-stu-id="d75c8-112">Description</span></span> |
|---|---|
| <span data-ttu-id="d75c8-113">Popis zboží</span><span class="sxs-lookup"><span data-stu-id="d75c8-113">Description of goods</span></span> | <span data-ttu-id="d75c8-114">Zadejte jedinečný identifikační název / číslo pro typ zboží, které bude používat tento popis.</span><span class="sxs-lookup"><span data-stu-id="d75c8-114">Enter a unique identification name/number for the type of goods that will use this description.</span></span> |
| <span data-ttu-id="d75c8-115">popis</span><span class="sxs-lookup"><span data-stu-id="d75c8-115">Description</span></span> | <span data-ttu-id="d75c8-116">Zadejte popis typu zboží v této kategorii.</span><span class="sxs-lookup"><span data-stu-id="d75c8-116">Enter a description of the type of goods in this category.</span></span> |

## <a name="vessels"></a><a name="vessels"></a><span data-ttu-id="d75c8-117">Plavidla</span><span class="sxs-lookup"><span data-stu-id="d75c8-117">Vessels</span></span>

<span data-ttu-id="d75c8-118">Plavidlo je jedinečný název lodi nebo plavidla, který používá přepravní společnost nebo agentura.</span><span class="sxs-lookup"><span data-stu-id="d75c8-118">A vessel is the unique name of a ship or vessel that a shipping company or agency uses.</span></span> <span data-ttu-id="d75c8-119">Když vytváříte plavbu, musíte pro ni vždy vybrat nebo zadat plavidlo.</span><span class="sxs-lookup"><span data-stu-id="d75c8-119">When you create a voyage, you must always either select or enter a vessel for it.</span></span> <span data-ttu-id="d75c8-120">Pokud často používáte stejná plavidla, můžete vytvořit novou cestu rychleji a snadněji vytvořením záznamu plavidla pro každou z nich, což uživatelům umožní vybrat si plavidlo ze seznamu místo toho, abyste museli pokaždé ručně zadávat název nebo číslo.</span><span class="sxs-lookup"><span data-stu-id="d75c8-120">If you often use the same vessels, then you can make it faster and easier to create a new voyage by creating a vessel record for each of them, thereby allowing users to select the vessel from a list rather then enter the name or number manually each time.</span></span>

<span data-ttu-id="d75c8-121">Chcete-li pracovat s loďmi, přejděte na uzel **Náklady za doručení \> Nastavení informací o doručení \> Lodě**.</span><span class="sxs-lookup"><span data-stu-id="d75c8-121">To work with vessels, go to **Landed cost \> Shipping information setup \> Vessels**.</span></span> <span data-ttu-id="d75c8-122">Zde můžete prohlížet, otevírat, vytvářet a mazat záznamy lodí.</span><span class="sxs-lookup"><span data-stu-id="d75c8-122">There, you can view, open, create, and delete records for vessels.</span></span> <span data-ttu-id="d75c8-123">V následující tabulce jsou popsána pole, která jsou k dispozici pro každý záznam.</span><span class="sxs-lookup"><span data-stu-id="d75c8-123">The following table describes the fields that are available for each record.</span></span>

| <span data-ttu-id="d75c8-124">Pole</span><span class="sxs-lookup"><span data-stu-id="d75c8-124">Field</span></span> | <span data-ttu-id="d75c8-125">popis</span><span class="sxs-lookup"><span data-stu-id="d75c8-125">Description</span></span> |
|---|---|
| <span data-ttu-id="d75c8-126">Plavidlo</span><span class="sxs-lookup"><span data-stu-id="d75c8-126">Vessel</span></span> | <span data-ttu-id="d75c8-127">Zadejte jedinečný identifikační název / číslo lodi, která bude použita k přepravě zboží na cestě.</span><span class="sxs-lookup"><span data-stu-id="d75c8-127">Enter a unique identification name/number for the ship that will be used to transport goods on a voyage.</span></span> |
| <span data-ttu-id="d75c8-128">popis</span><span class="sxs-lookup"><span data-stu-id="d75c8-128">Description</span></span> | <span data-ttu-id="d75c8-129">Zadejte popis lodě.</span><span class="sxs-lookup"><span data-stu-id="d75c8-129">Enter a description of the vessel.</span></span> <span data-ttu-id="d75c8-130">Tento popis obvykle identifikuje název lodi a přepravní společnost / agenta.</span><span class="sxs-lookup"><span data-stu-id="d75c8-130">Typically, this description identifies the name of the ship and the shipping company/agent.</span></span> |
| <span data-ttu-id="d75c8-131">Způsob dodání</span><span class="sxs-lookup"><span data-stu-id="d75c8-131">Mode of delivery</span></span> | <span data-ttu-id="d75c8-132">Vyberte způsob doručení, který loď používá (např _Vzduch_, _Oceán_ nebo _Vlak_).</span><span class="sxs-lookup"><span data-stu-id="d75c8-132">Select the mode of delivery that the vessel uses (such as _Air_, _Ocean_, or _Train_).</span></span> |

## <a name="exporters"></a><span data-ttu-id="d75c8-133">Vývozci</span><span class="sxs-lookup"><span data-stu-id="d75c8-133">Exporters</span></span>

<span data-ttu-id="d75c8-134">Každý záznam vývozce identifikuje dodavatele nebo vývozce, kterého lze definovat jako prodejce pro cestu.</span><span class="sxs-lookup"><span data-stu-id="d75c8-134">Each exporter record identifies a vendor or exporter that can be defined as the vendor for a voyage.</span></span> <span data-ttu-id="d75c8-135">Vývozce může být spojen s cestou a použit pro hlášení.</span><span class="sxs-lookup"><span data-stu-id="d75c8-135">The exporter can be associated with a voyage and used for reporting.</span></span>

<span data-ttu-id="d75c8-136">Chcete-li pracovat s vývozci, přejděte na uzel **Náklady za doručení \> Nastavení informací o doručení \> Vývozci**.</span><span class="sxs-lookup"><span data-stu-id="d75c8-136">To work with exporters, go to **Landed cost \> Shipping information setup \> Exporters**.</span></span> <span data-ttu-id="d75c8-137">Zde můžete prohlížet, otevírat, vytvářet a mazat záznamy vývozců.</span><span class="sxs-lookup"><span data-stu-id="d75c8-137">There, you can view, open, create, and delete records for exporters.</span></span> <span data-ttu-id="d75c8-138">V následující tabulce jsou popsána pole, která jsou k dispozici pro každý záznam.</span><span class="sxs-lookup"><span data-stu-id="d75c8-138">The following table describes the fields that are available for each record.</span></span>

| <span data-ttu-id="d75c8-139">Pole</span><span class="sxs-lookup"><span data-stu-id="d75c8-139">Field</span></span> | <span data-ttu-id="d75c8-140">popis</span><span class="sxs-lookup"><span data-stu-id="d75c8-140">Description</span></span> |
|---|---|
| <span data-ttu-id="d75c8-141">Vývozce</span><span class="sxs-lookup"><span data-stu-id="d75c8-141">Exporter</span></span> | <span data-ttu-id="d75c8-142">Zadejte jedinečný identifikační název / číslo vývozce zboží, které se přepravuje lodí.</span><span class="sxs-lookup"><span data-stu-id="d75c8-142">Enter a unique identification name/number for the exporter of goods that are transported on a voyage.</span></span> |
| <span data-ttu-id="d75c8-143">popis</span><span class="sxs-lookup"><span data-stu-id="d75c8-143">Description</span></span> | <span data-ttu-id="d75c8-144">Zadejte popis vývozce.</span><span class="sxs-lookup"><span data-stu-id="d75c8-144">Enter a description of the exporter.</span></span> <span data-ttu-id="d75c8-145">Tento popis obvykle identifikuje celý název přepravní společnosti / agenta.</span><span class="sxs-lookup"><span data-stu-id="d75c8-145">Typically, this description identifies the full name of the shipping company/agent.</span></span> |

## <a name="commodity-codes"></a><span data-ttu-id="d75c8-146">Kódy komodit</span><span class="sxs-lookup"><span data-stu-id="d75c8-146">Commodity codes</span></span>

<span data-ttu-id="d75c8-147">Pomocí komoditních kódů pomáháte s celní identifikací a výpočtem celních sazeb za zboží na cestě.</span><span class="sxs-lookup"><span data-stu-id="d75c8-147">You use commodity codes to help with customs identification and the calculation of duty rates for goods on a voyage.</span></span> <span data-ttu-id="d75c8-148">Kódy komodit můžete vybrat na stránce **Vydané produkty**.</span><span class="sxs-lookup"><span data-stu-id="d75c8-148">You can select commodity codes on the **Released products** page.</span></span>

<span data-ttu-id="d75c8-149">Chcete-li pracovat s kódy zboží, přejděte na uzel **Náklady za doručení \> Nastavení informací o přepravě \> Kódy zboží**.</span><span class="sxs-lookup"><span data-stu-id="d75c8-149">To work with commodity codes, go to **Landed cost \> Shipping information setup \> Commodity codes**.</span></span> <span data-ttu-id="d75c8-150">Zde můžete prohlížet, otevírat, vytvářet a mazat záznamy kódů zboží.</span><span class="sxs-lookup"><span data-stu-id="d75c8-150">There, you can view, open, create, and delete records for commodity codes.</span></span> <span data-ttu-id="d75c8-151">V následující tabulce jsou popsána pole, která jsou k dispozici pro každý záznam.</span><span class="sxs-lookup"><span data-stu-id="d75c8-151">The following table describes the fields that are available for each record.</span></span>

| <span data-ttu-id="d75c8-152">Pole</span><span class="sxs-lookup"><span data-stu-id="d75c8-152">Field</span></span> | <span data-ttu-id="d75c8-153">popis</span><span class="sxs-lookup"><span data-stu-id="d75c8-153">Description</span></span> |
|---|---|
| <span data-ttu-id="d75c8-154">Kód zboží</span><span class="sxs-lookup"><span data-stu-id="d75c8-154">Commodity code</span></span> | <span data-ttu-id="d75c8-155">Zadejte jedinečný kód pro tento typ komodity.</span><span class="sxs-lookup"><span data-stu-id="d75c8-155">Enter a unique code for this type of commodity.</span></span> |
| <span data-ttu-id="d75c8-156">popis</span><span class="sxs-lookup"><span data-stu-id="d75c8-156">Description</span></span> | <span data-ttu-id="d75c8-157">Zadejte popis typu komodity.</span><span class="sxs-lookup"><span data-stu-id="d75c8-157">Enter a description of the commodity type.</span></span> |

## <a name="customs-description"></a><span data-ttu-id="d75c8-158">Popis cla</span><span class="sxs-lookup"><span data-stu-id="d75c8-158">Customs description</span></span>

<span data-ttu-id="d75c8-159">Celní popisy pomáhají identifikovat zboží pro celní účely.</span><span class="sxs-lookup"><span data-stu-id="d75c8-159">Customs descriptions help identify goods for customs purposes.</span></span> <span data-ttu-id="d75c8-160">Celní popis můžete vybrat na stránce **Vydané produkty** nebo na řádcích nákupní objednávky.</span><span class="sxs-lookup"><span data-stu-id="d75c8-160">You can select a customs description on the **Released products** page or on purchase order lines.</span></span>

<span data-ttu-id="d75c8-161">Chcete-li pracovat s celními popisy, přejděte na **Náklady za doručení \> Nastavení informací o přepravě \> Celní popis**.</span><span class="sxs-lookup"><span data-stu-id="d75c8-161">To work with customs descriptions, go to **Landed cost \> Shipping information setup \> Customs description**.</span></span> <span data-ttu-id="d75c8-162">Zde můžete prohlížet, otevírat, vytvářet a mazat záznamy celních popisů.</span><span class="sxs-lookup"><span data-stu-id="d75c8-162">There, you can view, open, create, and delete records for custom descriptions.</span></span> <span data-ttu-id="d75c8-163">V následující tabulce jsou popsána pole, která jsou k dispozici pro každý záznam.</span><span class="sxs-lookup"><span data-stu-id="d75c8-163">The following table describes the fields that are available for each record.</span></span>

| <span data-ttu-id="d75c8-164">Pole</span><span class="sxs-lookup"><span data-stu-id="d75c8-164">Field</span></span> | <span data-ttu-id="d75c8-165">popis</span><span class="sxs-lookup"><span data-stu-id="d75c8-165">Description</span></span> |
|---|---|
| <span data-ttu-id="d75c8-166">Popis cla</span><span class="sxs-lookup"><span data-stu-id="d75c8-166">Customs description</span></span> | <span data-ttu-id="d75c8-167">Zadejte jedinečný kód pro tento typ klasifikace cla.</span><span class="sxs-lookup"><span data-stu-id="d75c8-167">Enter a unique code for this type of customs classification.</span></span> <span data-ttu-id="d75c8-168">Tento kód bude často oficiálním popisem poskytovaným celním úřadem pro popis a kvalitativní hodnotu zboží.</span><span class="sxs-lookup"><span data-stu-id="d75c8-168">Often, this code will be the official description that is provided by a customs authority for the description and qualitative value of the goods.</span></span> |
| <span data-ttu-id="d75c8-169">popis</span><span class="sxs-lookup"><span data-stu-id="d75c8-169">Description</span></span> | <span data-ttu-id="d75c8-170">Zadejte popis klasifikace cla.</span><span class="sxs-lookup"><span data-stu-id="d75c8-170">Enter a description of the customs classification.</span></span> |