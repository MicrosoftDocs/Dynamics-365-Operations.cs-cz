---
title: Skladová místa
description: Skladová místa se používají se základní funkcí skladu (WMS I) k určení toho, kde jsou položky uskladněny, a kde se položky vybírají v rámci skladu WMS I.
author: perlynne
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WMSLocation
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 2134
ms.assetid: 69bf6922-4151-447f-b678-4ba95637f54c
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: ce1e33fab6704dd3387f0c2034a8a950a858b2e0
ms.sourcegitcommit: 57bc7e17682e2edb5e1766496b7a22f4621819dd
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 11/18/2019
ms.locfileid: "2814299"
---
# <a name="inventory-locations"></a><span data-ttu-id="0f67f-103">Skladová místa</span><span class="sxs-lookup"><span data-stu-id="0f67f-103">Inventory locations</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="0f67f-104">Skladová místa se používají se základní funkcí skladu (WMS I) k určení toho, kde jsou položky uskladněny, a kde se položky vybírají v rámci skladu WMS I.</span><span class="sxs-lookup"><span data-stu-id="0f67f-104">Inventory locations are used with basic warehousing (WMS I) to determine where items are stored and where items are picked from in a WMS I warehouse.</span></span>

<span data-ttu-id="0f67f-105">V tomto tématu se týká funkcí v modulu Správa zboží.</span><span class="sxs-lookup"><span data-stu-id="0f67f-105">This topic applies to features in the Inventory management module.</span></span> <span data-ttu-id="0f67f-106">Nevztahuje se na funkce v modulu Řízení skladu.</span><span class="sxs-lookup"><span data-stu-id="0f67f-106">It does not apply to features in the Warehouse management module.</span></span>

<span data-ttu-id="0f67f-107">Termín skladové místo je definován jako místo, ze kterého se vybírají, a kam se ukládají položky.</span><span class="sxs-lookup"><span data-stu-id="0f67f-107">The term location refers to the place that items are stored and drawn from.</span></span>

<span data-ttu-id="0f67f-108">Lze také určit místo vložení položky pro každé skladové místo.</span><span class="sxs-lookup"><span data-stu-id="0f67f-108">For each location, the place where the item is inserted can also be specified.</span></span> <span data-ttu-id="0f67f-109">Implicitně jsou totožná.</span><span class="sxs-lookup"><span data-stu-id="0f67f-109">By default, they are the same.</span></span> <span data-ttu-id="0f67f-110">Položky se obvykle ukládají a vybírají ze stejné strany skladového místa, ale ne vždy.</span><span class="sxs-lookup"><span data-stu-id="0f67f-110">Items are usually inserted and drawn from the same side of a location, but not always.</span></span> <span data-ttu-id="0f67f-111">Například položky uložené v průběžných regálech se vkládají z jedné uličky a vybírají se z druhé uličky.</span><span class="sxs-lookup"><span data-stu-id="0f67f-111">For example, items that are stored in live storage racks are inserted from one aisle and drawn from another.</span></span> <span data-ttu-id="0f67f-112">Hlavním vstupním údajem je název skladového místa, který je obvykle určen svými souřadnicemi: sklad, ulička, stojan, police a přihrádka.</span><span class="sxs-lookup"><span data-stu-id="0f67f-112">The main input is given by a location name, which is usually determined by its coordinates: warehouse, aisle, rack, shelf, and bin.</span></span> <span data-ttu-id="0f67f-113">Tento název nebo ID lze zadat ručně nebo vytvořit ze souřadnic skladového místa – například 01-02-03-4, kde platí, že ulička = 1, stojan = 2, police = 3, přihrádka = 4 (stránka Skladové místo).</span><span class="sxs-lookup"><span data-stu-id="0f67f-113">This name or ID can be entered manually or generated from the location coordinates—for example, 01-02-03-4 for aisle 1, rack 2, shelf 3, bin 4 in the Inventory locations page.</span></span>
<span data-ttu-id="0f67f-114">Vlastnosti skladového místa</span><span class="sxs-lookup"><span data-stu-id="0f67f-114">Location properties</span></span>

<span data-ttu-id="0f67f-115">Skladové místo má následující charakteristiky:</span><span class="sxs-lookup"><span data-stu-id="0f67f-115">A location has the following characteristics:</span></span>
-   <span data-ttu-id="0f67f-116">Velikost (výška, šířka a hloubka a tím také objem)</span><span class="sxs-lookup"><span data-stu-id="0f67f-116">Size (height, width, depth, and thereby volume)</span></span>
-   <span data-ttu-id="0f67f-117">Sklad, Ulička, Stojan, Police a Přihrádka</span><span class="sxs-lookup"><span data-stu-id="0f67f-117">Warehouse, aisle, rack, shelf, and bin position</span></span>
-   <span data-ttu-id="0f67f-118">Typ skladového místa (velkosklad, výdejní skladové místo, vstupní přepraviště, výstupní přepraviště, vstupní místo výroby, inspekční umístění nebo kanbanový zásobník materiálu)</span><span class="sxs-lookup"><span data-stu-id="0f67f-118">Location type (bulk location, picking location, inbound dock, outbound dock, production input location, inspection location, or kanban supermarket)</span></span>

<span data-ttu-id="0f67f-119">V online systémech lze pomocí kontrolního textu ověřit, že operátor pro určitou položku vybral správné skladové místo.</span><span class="sxs-lookup"><span data-stu-id="0f67f-119">Check text can be used in online systems to verify that the operator has selected the correct location for a specific item.</span></span> <span data-ttu-id="0f67f-120">Tento kontrolní text lze vytvořit ručně nebo lze použít výchozí.</span><span class="sxs-lookup"><span data-stu-id="0f67f-120">This check text can be created manually or by default.</span></span>

## <a name="sort-codes"></a><span data-ttu-id="0f67f-121">Kódy třídění</span><span class="sxs-lookup"><span data-stu-id="0f67f-121">Sort codes</span></span>
<span data-ttu-id="0f67f-122">Kódy třídění se používají k optimalizaci zpracování řádků výdeje, ve kterých jsou uvedeny informace nutné pro výdej položek ze skladu včetně objednávky výdeje.</span><span class="sxs-lookup"><span data-stu-id="0f67f-122">Use sort codes to optimize the handling of picking lines, which describe the information that is required for picking items from inventory, including the picking order.</span></span> <span data-ttu-id="0f67f-123">Kódy třídění lze určovat podle uličky a dalších souřadnic nebo je lze přiřazovat skladovému místu ručně.</span><span class="sxs-lookup"><span data-stu-id="0f67f-123">Sort codes can be specified by the aisle and other coordinates, or assigned manually for the location.</span></span>

## <a name="blocked-locations"></a><span data-ttu-id="0f67f-124">Blokovaná skladová místa</span><span class="sxs-lookup"><span data-stu-id="0f67f-124">Blocked locations</span></span>
<span data-ttu-id="0f67f-125">Příležitostně je nutné skladové místo na určitou dobu zablokovat, například kvůli opravám.</span><span class="sxs-lookup"><span data-stu-id="0f67f-125">Occasionally, you might want to indicate that a location is blocked for a period of time, for example, to allow for repairs.</span></span> <span data-ttu-id="0f67f-126">Jindy bude třeba spustit blokování jen pro vstup nebo výstup.</span><span class="sxs-lookup"><span data-stu-id="0f67f-126">At other times, you may want to indicate blocking of only the input or only output.</span></span>

## <a name="tree-structure"></a><span data-ttu-id="0f67f-127">Stromová struktura</span><span class="sxs-lookup"><span data-stu-id="0f67f-127">Tree structure</span></span>

<span data-ttu-id="0f67f-128">Na stránce Skladová místa můžete zobrazit rozvržení skladu ve stromové struktuře podle souřadnic umístění zásob, a to v definovaném formátu zobrazení.</span><span class="sxs-lookup"><span data-stu-id="0f67f-128">In the Inventory locations page, you can view the warehouse layout in a tree structure based on the coordinates of inventory locations, in a defined display format.</span></span>

## <a name="maintain-inventory-locations-via-the-warehouse-form"></a><span data-ttu-id="0f67f-129">Spravovat skladová místa pomocí formuláře Sklad</span><span class="sxs-lookup"><span data-stu-id="0f67f-129">Maintain inventory locations via the warehouse form</span></span>

<span data-ttu-id="0f67f-130">Je možné kopírovat umístění z jednoho skladu do jiného a vytvořit umístění pomocí průvodce.</span><span class="sxs-lookup"><span data-stu-id="0f67f-130">It is possible to copy locations from one warehouse to another and to create locations via a wizard.</span></span> <span data-ttu-id="0f67f-131">Před spuštěním průvodce se ujistěte, že jste definovali výchozí názvy skladového místa na stránce Sklad.</span><span class="sxs-lookup"><span data-stu-id="0f67f-131">Before you run the wizard you should make sure that you have defined the default location names on the Warehouse page.</span></span>



<a name="additional-resources"></a><span data-ttu-id="0f67f-132">Další zdroje</span><span class="sxs-lookup"><span data-stu-id="0f67f-132">Additional resources</span></span>
--------

[<span data-ttu-id="0f67f-133">Vytvoření nového rozvržení skladu</span><span class="sxs-lookup"><span data-stu-id="0f67f-133">Create a new warehouse layout</span></span>](tasks/create-new-warehouse-layout.md)
