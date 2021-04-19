---
title: Fiktivní položky
description: Toto téma podrobně popisuje, jakým způsobem lze použít fiktivní typ řádku pro řádky kusovníku a receptury v aplikaci Dynamics 365 Supply Chain Management.
author: ShylaThompson
ms.date: 06/15/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SysOperationTemplateForm
audience: Application User
ms.reviewer: kamaybac
ms.custom: 1705903
ms.search.region: Global
ms.author: kamaybac
ms.search.validfrom: ''
ms.dyn365.ops.version: 8.0999999999999996
ms.openlocfilehash: 1118d7334602e450e5d503632895f73ba19066a1
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/01/2021
ms.locfileid: "5814771"
---
# <a name="phantom-items"></a><span data-ttu-id="a0927-103">Fiktivní položky</span><span class="sxs-lookup"><span data-stu-id="a0927-103">Phantom items</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="a0927-104">Toto téma podrobně popisuje, jakým způsobem lze použít fiktivní typ řádku pro řádky kusovníku a receptury.</span><span class="sxs-lookup"><span data-stu-id="a0927-104">This topic describes, in detail, how the Phantom line type can be used for the lines of a bill of materials (BOM) and a formula.</span></span> <span data-ttu-id="a0927-105">Na následujícím obrázku, (a) je kusovník pro produkt H a části F a G, a (b) je tabulka postupů pro produkty H a část F.</span><span class="sxs-lookup"><span data-stu-id="a0927-105">In the following illustration, (a) is the BOM for product H and parts F and G, and (b) is the route sheet for products H and part F.</span></span>

![Produkt H a část F](media/product-H-part-F.png)


<span data-ttu-id="a0927-107">Na obrázku je uveden příklad struktury kusovníku ve dvou úrovních.</span><span class="sxs-lookup"><span data-stu-id="a0927-107">This illustration shows an example of a BOM structure in two levels.</span></span> <span data-ttu-id="a0927-108">Dokončený produkt H představuje produkt pro sestavení stroje.</span><span class="sxs-lookup"><span data-stu-id="a0927-108">Finished product H represents a product for a machine assembly.</span></span> <span data-ttu-id="a0927-109">Sestavení stroje se skládá ze dvou částí, z elektrické jednotky (F), která má dva materiály (A a B), a skupiny obalových materiálů (G), která má rovněž dva materiály (C a D).</span><span class="sxs-lookup"><span data-stu-id="a0927-109">The machine assembly consists of two parts, an electrical unit (F) that has two materials (A and B) and a group of packaging materials (G) that also has two materials (C and D).</span></span> <span data-ttu-id="a0927-110">Další materiál (E) se používá při obecném sestavení stroje.</span><span class="sxs-lookup"><span data-stu-id="a0927-110">Another material (E) is used during the general assembly of the machine.</span></span>

![Produkt H a část F](media/product-H-part-B.png)

<span data-ttu-id="a0927-112">Předcházející obrázek představuje vývojový kusovník pro produkt H. Tato struktura poskytuje dobrý přehled o součástech a komponentách celkového sestavení stroje.</span><span class="sxs-lookup"><span data-stu-id="a0927-112">The preceding illustration represents the Engineering BOM for product H. This structure provides a good overview of the parts and components of the overall machine assembly.</span></span> <span data-ttu-id="a0927-113">I když návrháři produktu mohou upřednostňovat zobrazení kusovníku tímto způsobem, tato struktura nemusí správně představovat způsob, jakým je stroj sestaven na dílně.</span><span class="sxs-lookup"><span data-stu-id="a0927-113">However, although product designers might prefer to see the BOM represented in this way, this structure might not correctly represent the way that the machine is built on the shop floor.</span></span> 

<span data-ttu-id="a0927-114">Například vývojový kusovník na předcházejícím obrázku označuje, že elektrická jednotka F je sestavena jako samostatná část na samostatné pracovní objednávce.</span><span class="sxs-lookup"><span data-stu-id="a0927-114">For example, the Engineering BOM in the preceding illustration indicates that electrical unit F is assembled as a separate part on a separate work order.</span></span> <span data-ttu-id="a0927-115">V dílně však mohou usoudit, že je optimálnější sestavit elektrickou jednotku jako součást celkového sestavení stroje, nikoliv jako samostatný pracovní příkaz.</span><span class="sxs-lookup"><span data-stu-id="a0927-115">However, on the shop floor, it might be judged more optimal to assemble the electrical unit as part of the overall machine assembly, not as a separate work order.</span></span>

<span data-ttu-id="a0927-116">Tento vývojový kusovník také označuje, že část G je samostatná část.</span><span class="sxs-lookup"><span data-stu-id="a0927-116">This Engineering BOM also indicates that part G is a separate part.</span></span> <span data-ttu-id="a0927-117">V této struktuře však část G nereprezentuje fyzickou část, ale kolekci obalových materiálů.</span><span class="sxs-lookup"><span data-stu-id="a0927-117">However, in this structure, part G doesn’t represent a physical part but a collection of packaging materials.</span></span> 

<span data-ttu-id="a0927-118">Proto i když vývojový kusovník poskytuje velkou hodnotu pro návrh produktu a údržbu tohoto návrhu, nemusí se jednat o nejlogičtější způsob podpory proces provádění výroby produktu.</span><span class="sxs-lookup"><span data-stu-id="a0927-118">Therefore, although an Engineering BOM provides great value for the design of a product and maintenance of that design, it might not be the most logical way to support the manufacturing execution process of the product.</span></span> <span data-ttu-id="a0927-119">Naopak výrobní kusovník představuje nejlepší způsob sestavení produktu.</span><span class="sxs-lookup"><span data-stu-id="a0927-119">By contrast, a Manufacturing BOM represents the best way to build a product.</span></span>

<span data-ttu-id="a0927-120">Následující obrázek znázorňuje, jak je předchozí vývojový kusovník převeden na výrobní kusovník.</span><span class="sxs-lookup"><span data-stu-id="a0927-120">The following illustration shows how the preceding Engineering BOM is transitioned into a Manufacturing BOM.</span></span> <span data-ttu-id="a0927-121">Na tomto obrázku (a) je kusovník pro produkt H a b je tabulka postupů pro produkt H.</span><span class="sxs-lookup"><span data-stu-id="a0927-121">In this illustration, (a) is the BOM for product H, and b is the route sheet for product H.</span></span>

<span data-ttu-id="a0927-122">V této struktuře můžete vidět, že neexistuje zmínka o částech F a G, a že materiály, ze kterých se tyto části skládají, byly povýšeny na další úroveň kusovníku.</span><span class="sxs-lookup"><span data-stu-id="a0927-122">In this structure, you can see that there is no notion of parts F and G, and the materials that these parts consist of have been elevated to the next BOM level.</span></span> 

<span data-ttu-id="a0927-123">Na rozdíl od vývojového kusovníku, který měl dva listy operací, výrobní kusovník obsahuje pouze jeden list operací.</span><span class="sxs-lookup"><span data-stu-id="a0927-123">Unlike the Engineering BOM, which had two operations sheets, the Manufacturing BOM has only one operations sheet.</span></span> <span data-ttu-id="a0927-124">Operace balení, která byla navázána na část G, byla také povýšena a je nyní součástí listu operací pro produkt H. Sestavení elektrické jednotky je první operace.</span><span class="sxs-lookup"><span data-stu-id="a0927-124">The packaging operation that was linked to part G has also been elevated and is now part of the operations sheet for product H. The assembly of the electrical unit is the first operation.</span></span> <span data-ttu-id="a0927-125">Tento výrobní příkaz dává smysl, vzhledem k tomu, že tato jednotka se používá v další operace, kterou je sestavení stroje.</span><span class="sxs-lookup"><span data-stu-id="a0927-125">This order makes good sense, because this unit is used in the next operation, which is the machine assembly.</span></span> <span data-ttu-id="a0927-126">Poslední operace je operace balení, které spotřebuje dva obalové materiály (C a D).</span><span class="sxs-lookup"><span data-stu-id="a0927-126">The last operation is the packaging operation, which consumes two packing materials (C and D).</span></span>

<span data-ttu-id="a0927-127">Přechod mezi vývojovým kusovníkem a výrobním kusovníkem povolen prostřednictvím typu řádku kusovníku Phantom.</span><span class="sxs-lookup"><span data-stu-id="a0927-127">The transition between the Engineering BOM and the Manufacturing BOM is enabled through the Phantom BOM line type.</span></span> <span data-ttu-id="a0927-128">Jako naznačuje termín „fiktivní“, části F a G během převodu mezi dvěma typy kusovníku zmizely.</span><span class="sxs-lookup"><span data-stu-id="a0927-128">As the term “phantom” indicates, parts F and G have disappeared during the transition between the two BOM types.</span></span> <span data-ttu-id="a0927-129">V tomto příkladu je fiktivní typ řádku použit na řádky kusovníku pro části F a G ve vývojovém kusovníku.</span><span class="sxs-lookup"><span data-stu-id="a0927-129">In this example, the Phantom line type is applied to the BOM lines for parts F and G in the Engineering BOM.</span></span> <span data-ttu-id="a0927-130">Když je vytvořena výrobní zakázka nebo dávková objednávka, je vývojový kusovník zkopírován do výrobní zakázky nebo dávkové objednávky.</span><span class="sxs-lookup"><span data-stu-id="a0927-130">When a production or batch order is created, the Engineering BOM is copied to the production or batch order.</span></span> <span data-ttu-id="a0927-131">Když je pak zakázka oceněna, dojde k přechodu z vývojového kusovníku na výrobní kusovník, jak je uvedeno na předchozím obrázku.</span><span class="sxs-lookup"><span data-stu-id="a0927-131">Then, when the order is estimated, the transition from the Engineering BOM to the Manufacturing BOM occurs, as shown in the preceding illustrations.</span></span> <span data-ttu-id="a0927-132">Z listu operace na druhém obrázku jsou obalové materiály C a D vstupem pro operaci.</span><span class="sxs-lookup"><span data-stu-id="a0927-132">From the operations sheet in the second illustration, packaging materials C and D are input for the operation.</span></span> 

## <a name="multilevel-phantom-bom-structures"></a><span data-ttu-id="a0927-133">Víceúrovňové struktury fiktivního kusovníku</span><span class="sxs-lookup"><span data-stu-id="a0927-133">Multilevel phantom BOM structures</span></span>
<span data-ttu-id="a0927-134">Fiktivní typ řádku typu lze použít ve víceúrovňových strukturách kusovníku, jak je uvedeno na následujícím obrázku.</span><span class="sxs-lookup"><span data-stu-id="a0927-134">The Phantom line type can be used in multilevel BOM structures, as shown in the following illustration.</span></span> <span data-ttu-id="a0927-135">Na tomto obrázku je (a) kusovník pro produkt G a (b) je tabulka postupů pro části E a F a produkt G.</span><span class="sxs-lookup"><span data-stu-id="a0927-135">In this illustration, (a) is the BOM for product G, and (b) is the route sheet for parts E and F and product G.</span></span> 

![Produkt G a část F s tabulkami postupů](media/product-G-route-sheet-G.png)


<span data-ttu-id="a0927-137">Následující obrázek znázorňuje výsledný výrobní kusovník a tabulku postupu, pokud jsou řádky kusovníku pro části E a F nakonfigurovány tak, aby byl typ řádku fiktivní.</span><span class="sxs-lookup"><span data-stu-id="a0927-137">The following illustration shows the resulting Manufacturing BOM and route sheet if the BOM lines for parts E and F are configured so that the line type is Phantom.</span></span> <span data-ttu-id="a0927-138">Na tomto obrázku (a) je kusovník pro produkt G a (b) je tabulka postupů pro produkt G.</span><span class="sxs-lookup"><span data-stu-id="a0927-138">In this illustration, (a) is the BOM for product G, and (b) is the route sheet for product G.</span></span>

![Produkt G](media/product-G.png)


## <a name="phantom-and-route-network"></a><span data-ttu-id="a0927-140">Fiktivní a síťový postup</span><span class="sxs-lookup"><span data-stu-id="a0927-140">Phantom and route network</span></span>
<span data-ttu-id="a0927-141">Fiktivní kusovníky lze také použít pro kusovník, který má síťový postup.</span><span class="sxs-lookup"><span data-stu-id="a0927-141">Phantom BOMs can also be used for a BOM that has a route network.</span></span> <span data-ttu-id="a0927-142">V síťovém postupu běží jedna nebo více operací současně.</span><span class="sxs-lookup"><span data-stu-id="a0927-142">In a route network, one or more operations run in parallel.</span></span> <span data-ttu-id="a0927-143">Následující obrázek znázorňuje příklad síťového postupu, který se používá ve víceúrovňovém kusovníku.</span><span class="sxs-lookup"><span data-stu-id="a0927-143">The following illustration shows an example of a route network that is used in a multilevel BOM.</span></span> <span data-ttu-id="a0927-144">Na tomto obrázku je (a) kusovník pro produkt G a část F a (b) je tabulka postupů pro produkt G a část F, která má síťový postup.</span><span class="sxs-lookup"><span data-stu-id="a0927-144">In this illustration, (a) is the BOM for product G and part F, and (b) is the route sheet for product G and part F, which has a route network.</span></span>

![Produkt G a část F](media/product-G-part-F.png)


<span data-ttu-id="a0927-146">Na následujícím obrázku, (a) je kusovník pro produkt G a část F, a (b) je tabulka postupů pro produkt G a část F.</span><span class="sxs-lookup"><span data-stu-id="a0927-146">In the following illustration, (a) is the BOM for product G and part F, and (b) is the route sheet for product G and part F.</span></span>

![Produkt G a část F s tabulkami postupů](media/product-G-part-F-with-route-sheet.png)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]