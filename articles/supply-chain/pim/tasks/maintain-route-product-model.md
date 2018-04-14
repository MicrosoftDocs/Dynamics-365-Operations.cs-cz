--- 
title: "Udržování postupu pro model produktu"
description: "Spuštění této procedury vyžaduje, aby model konfigurace produktu existoval."
author: YuyuScheller
manager: AnnBe
ms.date: 03/02/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.author: bis
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: 2173527d7f4ea8d92e9daf5d0dd1818b975fd1e3
ms.contentlocale: cs-cz
ms.lasthandoff: 04/13/2018

---
# <a name="maintain-a-route-for-a-product-model"></a><span data-ttu-id="5d9dd-103">Udržování postupu pro model produktu</span><span class="sxs-lookup"><span data-stu-id="5d9dd-103">Maintain a route for a product model</span></span>

[!INCLUDE [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="5d9dd-104">Spuštění této procedury vyžaduje, aby model konfigurace produktu existoval.</span><span class="sxs-lookup"><span data-stu-id="5d9dd-104">Running this procedure requires that a product configuration model exists.</span></span> <span data-ttu-id="5d9dd-105">Při provádění celým procesem tento postup používá model špičkový model reproduktoru v ukázkové společnosti USMF.</span><span class="sxs-lookup"><span data-stu-id="5d9dd-105">This procedure uses the High end speaker model in the demo company USMF to walk you through the process.</span></span>


## <a name="add-a-route-operation"></a><span data-ttu-id="5d9dd-106">Přidání postupu operace</span><span class="sxs-lookup"><span data-stu-id="5d9dd-106">Add a route operation</span></span>
1. <span data-ttu-id="5d9dd-107">Klepněte na Definice modelu varianty produktu.</span><span class="sxs-lookup"><span data-stu-id="5d9dd-107">Click Product variant model definition.</span></span>
2. <span data-ttu-id="5d9dd-108">Klepněte na Modely konfigurace produktu.</span><span class="sxs-lookup"><span data-stu-id="5d9dd-108">Click Product configuration models.</span></span>
3. <span data-ttu-id="5d9dd-109">Vyhledejte na seznamu požadovaný záznam a vyberte ho.</span><span class="sxs-lookup"><span data-stu-id="5d9dd-109">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="5d9dd-110">Pro toto cvičení vyberte model špičkového reproduktoru.</span><span class="sxs-lookup"><span data-stu-id="5d9dd-110">Select the High end speaker model for this exercise.</span></span>  
4. <span data-ttu-id="5d9dd-111">Klikněte na odkaz na vybraném řádku v seznamu.</span><span class="sxs-lookup"><span data-stu-id="5d9dd-111">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="5d9dd-112">Rozbalte sekci Operace postupu.</span><span class="sxs-lookup"><span data-stu-id="5d9dd-112">Expand the Route operations section.</span></span>
6. <span data-ttu-id="5d9dd-113">Klepněte na možnost Přidat.</span><span class="sxs-lookup"><span data-stu-id="5d9dd-113">Click Add.</span></span>
7. <span data-ttu-id="5d9dd-114">Zadejte hodnotu do pole Název.</span><span class="sxs-lookup"><span data-stu-id="5d9dd-114">In the Name field, type a value.</span></span>
8. <span data-ttu-id="5d9dd-115">Zadejte nějakou hodnotu do pole Popis.</span><span class="sxs-lookup"><span data-stu-id="5d9dd-115">In the Description field, type a value.</span></span>
9. <span data-ttu-id="5d9dd-116">Klikněte na položku Uložit.</span><span class="sxs-lookup"><span data-stu-id="5d9dd-116">Click Save.</span></span>

## <a name="enter-route-operation-details"></a><span data-ttu-id="5d9dd-117">Zadání podrobností operace postupu</span><span class="sxs-lookup"><span data-stu-id="5d9dd-117">Enter route operation details</span></span>
1. <span data-ttu-id="5d9dd-118">Klepněte na Podrobnosti operace postupu.</span><span class="sxs-lookup"><span data-stu-id="5d9dd-118">Click Route operation details.</span></span>
2. <span data-ttu-id="5d9dd-119">V poli Operace zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="5d9dd-119">In the Operation field, enter or select a value.</span></span>
3. <span data-ttu-id="5d9dd-120">V číslu operace</span><span class="sxs-lookup"><span data-stu-id="5d9dd-120">In the Oper.</span></span> <span data-ttu-id="5d9dd-121">Č.</span><span class="sxs-lookup"><span data-stu-id="5d9dd-121">No.</span></span> <span data-ttu-id="5d9dd-122">zadejte číslo.</span><span class="sxs-lookup"><span data-stu-id="5d9dd-122">field, enter a number.</span></span>
    * <span data-ttu-id="5d9dd-123">Čísla operace určující pořadí v postupu.</span><span class="sxs-lookup"><span data-stu-id="5d9dd-123">Operation numbers determine the route sequence.</span></span>  
    * <span data-ttu-id="5d9dd-124">Každá vlastnost při operaci postupu může získat statickou hodnotu nebo namapování na atribut.</span><span class="sxs-lookup"><span data-stu-id="5d9dd-124">Each property on a route operation can get a static value or be mapped to an attribute.</span></span> <span data-ttu-id="5d9dd-125">Mapování na atribut způsobí, že hodnota bude nastavena v rámci konfigurace.</span><span class="sxs-lookup"><span data-stu-id="5d9dd-125">Mapping to an attribute will result in the value being set as part of the configuration.</span></span>  
4. <span data-ttu-id="5d9dd-126">V poli Skupina postupů zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="5d9dd-126">In the Route group field, enter or select a value.</span></span>
    * <span data-ttu-id="5d9dd-127">Skupina postupů určuje základní chování pro náklady, spotřebu a nastavení.</span><span class="sxs-lookup"><span data-stu-id="5d9dd-127">The route group determines essential behavior for costing, consumption, and setup.</span></span>  
5. <span data-ttu-id="5d9dd-128">Klikněte na záložku Nastavení.</span><span class="sxs-lookup"><span data-stu-id="5d9dd-128">Click the Setup tab.</span></span>
6. <span data-ttu-id="5d9dd-129">Klepněte na kartu Časy.</span><span class="sxs-lookup"><span data-stu-id="5d9dd-129">Click the Times tab.</span></span>
7. <span data-ttu-id="5d9dd-130">Do pole Množství procesu zadejte číslo.</span><span class="sxs-lookup"><span data-stu-id="5d9dd-130">In the Process qty. field, enter a number.</span></span>
    * <span data-ttu-id="5d9dd-131">Určuje, kolik se zpracuje při jedné operaci.</span><span class="sxs-lookup"><span data-stu-id="5d9dd-131">Determine how many will be processed during one operation.</span></span>  
8. <span data-ttu-id="5d9dd-132">Do pole Hodiny/čas zadejte číslo.</span><span class="sxs-lookup"><span data-stu-id="5d9dd-132">In the Hours/time field, enter a number.</span></span>
    * <span data-ttu-id="5d9dd-133">Zadejte časový úsek.</span><span class="sxs-lookup"><span data-stu-id="5d9dd-133">Enter the time ratio.</span></span>  
9. <span data-ttu-id="5d9dd-134">Zaškrtněte políčko položky Nastavit.</span><span class="sxs-lookup"><span data-stu-id="5d9dd-134">Select the Set check box.</span></span>
10. <span data-ttu-id="5d9dd-135">Do pole Operační čas zadejte číslo.</span><span class="sxs-lookup"><span data-stu-id="5d9dd-135">In the Run time field, enter a number.</span></span>
    * <span data-ttu-id="5d9dd-136">Určete čas zpracování pro množství, které jste zadali.</span><span class="sxs-lookup"><span data-stu-id="5d9dd-136">Determine the processing time for the quantity that you have specified.</span></span>  
11. <span data-ttu-id="5d9dd-137">Klepněte na kartu Požadavky na zdroj.</span><span class="sxs-lookup"><span data-stu-id="5d9dd-137">Click the Resource requirements tab.</span></span>
12. <span data-ttu-id="5d9dd-138">Klepněte na možnost Přidat.</span><span class="sxs-lookup"><span data-stu-id="5d9dd-138">Click Add.</span></span>
13. <span data-ttu-id="5d9dd-139">Označte v seznamu vybraný řádek.</span><span class="sxs-lookup"><span data-stu-id="5d9dd-139">In the list, mark the selected row.</span></span>
14. <span data-ttu-id="5d9dd-140">V poli Typ požadavku vyberte možnost.</span><span class="sxs-lookup"><span data-stu-id="5d9dd-140">In the Requirement type field, select an option.</span></span>
    * <span data-ttu-id="5d9dd-141">Rozhodněte, zda chcete zadat určité zdroje nebo možností, které musí mít.</span><span class="sxs-lookup"><span data-stu-id="5d9dd-141">Decide if you want to specify specific resources or capabilities that they must possess.</span></span>  
15. <span data-ttu-id="5d9dd-142">V poli Požadavek zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="5d9dd-142">In the Requirement field, enter or select a value.</span></span>
16. <span data-ttu-id="5d9dd-143">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="5d9dd-143">Click OK.</span></span>


