---
title: Vytvoření výrobní zakázky
description: Tato procedura popisuje způsob vytváření výrobní zakázky.
author: johanhoffmann
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProdTableListPage, ProdTableCreate, ProdTable, ProdBOM, ProdRoute
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: c16413b25a8d2a11b478b148cb3e96c3a677c6eb
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/02/2020
ms.locfileid: "3210886"
---
# <a name="create-a-production-order"></a><span data-ttu-id="e0c60-103">Vytvoření výrobní zakázky</span><span class="sxs-lookup"><span data-stu-id="e0c60-103">Create a production order</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="e0c60-104">Tato procedura popisuje způsob vytváření výrobní zakázky.</span><span class="sxs-lookup"><span data-stu-id="e0c60-104">This procedure shows how to create a production order.</span></span> <span data-ttu-id="e0c60-105">K vytvoření tohoto postupu jsou použita ukázková data společnosti USMF.</span><span class="sxs-lookup"><span data-stu-id="e0c60-105">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="e0c60-106">Jedná se o první proceduru ze sedmi, která vysvětluje životního cyklus výrobní zakázky.</span><span class="sxs-lookup"><span data-stu-id="e0c60-106">This is the first procedure out of seven which explains the production order lifecycle.</span></span>


## <a name="create-a-production-order"></a><span data-ttu-id="e0c60-107">Vytvoření výrobní zakázky</span><span class="sxs-lookup"><span data-stu-id="e0c60-107">Create a production order</span></span>
1. <span data-ttu-id="e0c60-108">Přejděte na Řízení výroby > Výrobní zakázky > Všechny výrobní zakázky.</span><span class="sxs-lookup"><span data-stu-id="e0c60-108">Go to Production control > Production orders > All production orders.</span></span>
2. <span data-ttu-id="e0c60-109">Klikněte na možnost Nová výrobní zakázka.</span><span class="sxs-lookup"><span data-stu-id="e0c60-109">Click New production order.</span></span>
3. <span data-ttu-id="e0c60-110">Do pole Číslo položky zadejte D0001.</span><span class="sxs-lookup"><span data-stu-id="e0c60-110">In the Item number field, type 'D0001'.</span></span>
4. <span data-ttu-id="e0c60-111">Do pole Dodání zadejte datum.</span><span class="sxs-lookup"><span data-stu-id="e0c60-111">In the Delivery field, enter a date.</span></span>
    * <span data-ttu-id="e0c60-112">Datum dodání označuje, kdy by měla skončit výrobní zakázka pro provedení včas.</span><span class="sxs-lookup"><span data-stu-id="e0c60-112">The delivery date indicates when the production order should end in order to deliver on time.</span></span> <span data-ttu-id="e0c60-113">Toto datum lze použít v procesu plánování.</span><span class="sxs-lookup"><span data-stu-id="e0c60-113">This date can be used in the scheduling process.</span></span> <span data-ttu-id="e0c60-114">Můžete například naplánovat objednávku zpětně od data dodání.</span><span class="sxs-lookup"><span data-stu-id="e0c60-114">For example, you can schedule the order backward from the delivery date.</span></span>  
5. <span data-ttu-id="e0c60-115">Nastavte množství na hodnotu 20.</span><span class="sxs-lookup"><span data-stu-id="e0c60-115">Set Quantity to '20'.</span></span>
    * <span data-ttu-id="e0c60-116">Poznámka: V poli s číslem kusovníku se automaticky zobrazí počet aktivního kusovníku pro stávající položku, avšak kusovník můžete změnit z výrobní zakázky výběrem aktivního kusovníku ze seznamu schválených verzí kusovníku.</span><span class="sxs-lookup"><span data-stu-id="e0c60-116">Note: The BOM number field automatically displays the number of any active BOM for the current item, but you can change the BOM for the production order by selecting an active BOM from the list of approved BOM versions.</span></span>    <span data-ttu-id="e0c60-117">V poli s číslem postupu se automaticky zobrazí počet aktivního postupu pro stávající položku, avšak postup můžete změnit z výrobní zakázky výběrem aktivního postupu ze seznamu schválených verzí postupu.</span><span class="sxs-lookup"><span data-stu-id="e0c60-117">The Route number field automatically displays the number of any active Route for the current item, but you can change the Route for the production order by selecting an active Route from the list of approved Route versions.</span></span>  
6. <span data-ttu-id="e0c60-118">Klikněte na položku Vytvořit.</span><span class="sxs-lookup"><span data-stu-id="e0c60-118">Click Create.</span></span>

## <a name="validate-the-production-order"></a><span data-ttu-id="e0c60-119">Ověření výrobní zakázky</span><span class="sxs-lookup"><span data-stu-id="e0c60-119">Validate the production order</span></span>
1. <span data-ttu-id="e0c60-120">Klikněte na odkaz na vybraném řádku v seznamu.</span><span class="sxs-lookup"><span data-stu-id="e0c60-120">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="e0c60-121">Klepněte na odkaz na číslo výrobní zakázky, kterou jste právě vytvořili.</span><span class="sxs-lookup"><span data-stu-id="e0c60-121">Click the link for the production order number that you have just created.</span></span> <span data-ttu-id="e0c60-122">To otevře stránku s podrobnostmi o objednávce.</span><span class="sxs-lookup"><span data-stu-id="e0c60-122">This will open the details page for the order.</span></span>  
2. <span data-ttu-id="e0c60-123">Klikněte na položku Upravit.</span><span class="sxs-lookup"><span data-stu-id="e0c60-123">Click Edit.</span></span>
3. <span data-ttu-id="e0c60-124">Do pole Dodání zadejte datum.</span><span class="sxs-lookup"><span data-stu-id="e0c60-124">In the Delivery field, enter a date.</span></span>
    * <span data-ttu-id="e0c60-125">Můžete například změnit data dodání výrobní zakázky.</span><span class="sxs-lookup"><span data-stu-id="e0c60-125">For example, you can change the delivery date for the production order.</span></span>  
4. <span data-ttu-id="e0c60-126">Klikněte na položku Uložit.</span><span class="sxs-lookup"><span data-stu-id="e0c60-126">Click Save.</span></span>
5. <span data-ttu-id="e0c60-127">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="e0c60-127">Close the page.</span></span>

## <a name="update-the-bom"></a><span data-ttu-id="e0c60-128">Aktualizace kusovníku</span><span class="sxs-lookup"><span data-stu-id="e0c60-128">Update the BOM</span></span>
1. <span data-ttu-id="e0c60-129">V podokně akcí klikněte na položku Výrobní zakázka.</span><span class="sxs-lookup"><span data-stu-id="e0c60-129">On the Action Pane, click Production order.</span></span>
2. <span data-ttu-id="e0c60-130">Klikněte na položku Kusovník.</span><span class="sxs-lookup"><span data-stu-id="e0c60-130">Click BOM.</span></span>
    * <span data-ttu-id="e0c60-131">Otevřete stránku kusovníku a ověřte data kusovníku, která byla zkopírována z výchozích dat při vytvoření výrobní zakázky.</span><span class="sxs-lookup"><span data-stu-id="e0c60-131">Open the BOM page to validate the BOM data that was copied from the default data when the production order was created.</span></span> <span data-ttu-id="e0c60-132">V tomto postupu je nutné aktualizovat množství pro kusovník.</span><span class="sxs-lookup"><span data-stu-id="e0c60-132">In this procedure, you need to update the quantity for a BOM.</span></span>  
3. <span data-ttu-id="e0c60-133">Klikněte na položku Upravit.</span><span class="sxs-lookup"><span data-stu-id="e0c60-133">Click Edit.</span></span>
4. <span data-ttu-id="e0c60-134">Zadejte číslo do pole Množství.</span><span class="sxs-lookup"><span data-stu-id="e0c60-134">In the Quantity field, enter a number.</span></span>
    * <span data-ttu-id="e0c60-135">Změna množství na řádku kusovníku má vliv na odhad nákladů spotřeby materiálu pro výrobní zakázku.</span><span class="sxs-lookup"><span data-stu-id="e0c60-135">Changing the quantity on the BOM line affects the cost estimate of material consumption for the production order.</span></span>  
5. <span data-ttu-id="e0c60-136">Klikněte na položku Uložit.</span><span class="sxs-lookup"><span data-stu-id="e0c60-136">Click Save.</span></span>
6. <span data-ttu-id="e0c60-137">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="e0c60-137">Close the page.</span></span>

## <a name="update-the-production-route"></a><span data-ttu-id="e0c60-138">Aktualizace výrobního postupu</span><span class="sxs-lookup"><span data-stu-id="e0c60-138">Update the production route</span></span>
1. <span data-ttu-id="e0c60-139">V podokně akcí klikněte na položku Výrobní zakázka.</span><span class="sxs-lookup"><span data-stu-id="e0c60-139">On the Action Pane, click Production order.</span></span>
2. <span data-ttu-id="e0c60-140">Klikněte na Postup.</span><span class="sxs-lookup"><span data-stu-id="e0c60-140">Click Route.</span></span>
    * <span data-ttu-id="e0c60-141">Otevřete stránku Směrování a ověřte data výrobního postupu, která byla zkopírována z výchozích dat při vytvoření zakázky.</span><span class="sxs-lookup"><span data-stu-id="e0c60-141">Open the Route page to validate the data of the production route that was copied from the default data when the order was created.</span></span> <span data-ttu-id="e0c60-142">V tomto postupu je nutné aktualizovat množství pro jednu operaci ve výrobním postupu.</span><span class="sxs-lookup"><span data-stu-id="e0c60-142">In this procedure, you need to update the quantity for one of the operations in the production route.</span></span>  
3. <span data-ttu-id="e0c60-143">Vyhledejte na seznamu požadovaný záznam a vyberte ho.</span><span class="sxs-lookup"><span data-stu-id="e0c60-143">In the list, find and select the desired record.</span></span>
4. <span data-ttu-id="e0c60-144">Klikněte na položku Upravit.</span><span class="sxs-lookup"><span data-stu-id="e0c60-144">Click Edit.</span></span>
5. <span data-ttu-id="e0c60-145">Do pole Množství procesu zadejte číslo.</span><span class="sxs-lookup"><span data-stu-id="e0c60-145">In the Process qty. field, enter a number.</span></span>
    * <span data-ttu-id="e0c60-146">Změna času zpracování se projeví na odhadované spotřebě a nákladech výrobní zakázky.</span><span class="sxs-lookup"><span data-stu-id="e0c60-146">Changing the process time affects the estimated route consumption and the cost of the production order.</span></span>  
6. <span data-ttu-id="e0c60-147">Klikněte na položku Uložit.</span><span class="sxs-lookup"><span data-stu-id="e0c60-147">Click Save.</span></span>
7. <span data-ttu-id="e0c60-148">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="e0c60-148">Close the page.</span></span>

