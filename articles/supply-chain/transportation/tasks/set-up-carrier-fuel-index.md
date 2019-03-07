---
title: Nastavení indexu paliva dopravce
description: Tato příručka popisuje vytváření oblast indexu paliva, indexu paliva a indexu paliva dopravce.
author: ShylaThompson
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: b6f72de7ad54a2b2dc1bf40fd8cb86d8b055e2d1
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 01/29/2019
ms.locfileid: "366574"
---
# <a name="set-up-a-carrier-fuel-index"></a><span data-ttu-id="2bd73-103">Nastavení indexu paliva dopravce</span><span class="sxs-lookup"><span data-stu-id="2bd73-103">Set up a carrier fuel index</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="2bd73-104">Tato příručka popisuje vytváření oblast indexu paliva, indexu paliva a indexu paliva dopravce.</span><span class="sxs-lookup"><span data-stu-id="2bd73-104">This guide shows how to create a fuel index region, a fuel index and a carrier fuel index.</span></span> <span data-ttu-id="2bd73-105">Oblast indexu paliva určuje, pro které oblasti má být index paliva použit, a index paliva určuje cenu paliva pro určitý časový úsek.</span><span class="sxs-lookup"><span data-stu-id="2bd73-105">The fuel index region specifies which region the fuel index should apply to, and the fuel index specifies a fuel price for a particular period of time.</span></span> <span data-ttu-id="2bd73-106">Pokud chcete, aby se projevily změny cen paliva v čase, je možné přiřadit více indexů paliva k dopravci.</span><span class="sxs-lookup"><span data-stu-id="2bd73-106">To reflect the change in fuel prices over time, you can associate multiple fuel indexes with a carrier.</span></span>  <span data-ttu-id="2bd73-107">Tyto úlohy běžně provádí koordinátor přepravy.</span><span class="sxs-lookup"><span data-stu-id="2bd73-107">These tasks are normally done by a transportation coordinator.</span></span> <span data-ttu-id="2bd73-108">Tento postup můžete použít s ukázkovými daty společnosti USMF nebo pomocí vlastních dat.</span><span class="sxs-lookup"><span data-stu-id="2bd73-108">You can use this procedure in demo data company USMF or using your own data.</span></span>


## <a name="create-a-fuel-index-region"></a><span data-ttu-id="2bd73-109">Vytvoření oblasti indexu paliva</span><span class="sxs-lookup"><span data-stu-id="2bd73-109">Create a fuel index region</span></span>
1. <span data-ttu-id="2bd73-110">Přejděte na Správa přepravy > Nastavení > Indexy paliva > Oblasti indexu paliva.</span><span class="sxs-lookup"><span data-stu-id="2bd73-110">Go to Transportation management > Setup > Fuel indexes > Fuel index regions.</span></span>
    * <span data-ttu-id="2bd73-111">Nejprve je třeba vytvořit různé oblasti, které probíhá provoz a výpočet různých palivových příplatků.</span><span class="sxs-lookup"><span data-stu-id="2bd73-111">First you have to create the different regions, where you operate and calculate different fuel surcharges.</span></span>  
2. <span data-ttu-id="2bd73-112">Klikněte na položku Nová.</span><span class="sxs-lookup"><span data-stu-id="2bd73-112">Click New.</span></span>
3. <span data-ttu-id="2bd73-113">Zadejte hodnotu do pole Oblast.</span><span class="sxs-lookup"><span data-stu-id="2bd73-113">In the Region field, type a value.</span></span>
4. <span data-ttu-id="2bd73-114">Zadejte hodnotu do pole Název.</span><span class="sxs-lookup"><span data-stu-id="2bd73-114">In the Name field, type a value.</span></span>
5. <span data-ttu-id="2bd73-115">Klikněte na položku Uložit.</span><span class="sxs-lookup"><span data-stu-id="2bd73-115">Click Save.</span></span>

## <a name="create-a-fuel-index"></a><span data-ttu-id="2bd73-116">Vytvoření indexu paliva</span><span class="sxs-lookup"><span data-stu-id="2bd73-116">Create a fuel index</span></span>
1. <span data-ttu-id="2bd73-117">Přejděte na Správa přepravy > Nastavení > Indexy paliva > Indexy paliva.</span><span class="sxs-lookup"><span data-stu-id="2bd73-117">Go to Transportation management > Setup > Fuel indexes > Fuel indexes.</span></span>
    * <span data-ttu-id="2bd73-118">Pro nastavené oblasti je nutné zadat aktuální ceny paliva.</span><span class="sxs-lookup"><span data-stu-id="2bd73-118">For the regions you have set up you need to enter the current prices for the fuel.</span></span>  
2. <span data-ttu-id="2bd73-119">Klikněte na položku Nová.</span><span class="sxs-lookup"><span data-stu-id="2bd73-119">Click New.</span></span>
3. <span data-ttu-id="2bd73-120">V poli Oblast kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.</span><span class="sxs-lookup"><span data-stu-id="2bd73-120">In the Region field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="2bd73-121">Klikněte na odkaz na vybraném řádku v seznamu.</span><span class="sxs-lookup"><span data-stu-id="2bd73-121">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="2bd73-122">V poli Cena za galon zadejte číslo.</span><span class="sxs-lookup"><span data-stu-id="2bd73-122">In the Price per gallon field, enter a number.</span></span>
6. <span data-ttu-id="2bd73-123">Zadejte datum a čas do pole Datum a čas platnosti.</span><span class="sxs-lookup"><span data-stu-id="2bd73-123">In the Effective start date and time field, enter a date and time.</span></span>
7. <span data-ttu-id="2bd73-124">Klikněte na položku Uložit.</span><span class="sxs-lookup"><span data-stu-id="2bd73-124">Click Save.</span></span>

## <a name="create-a-carrier-fuel-index"></a><span data-ttu-id="2bd73-125">Vytvoření indexu paliva pro dopravce</span><span class="sxs-lookup"><span data-stu-id="2bd73-125">Create a Carrier fuel index</span></span>
1. <span data-ttu-id="2bd73-126">Přejděte na Správa přepravy > Nastavení > Indexy paliva > Indexy paliva pro dopravce.</span><span class="sxs-lookup"><span data-stu-id="2bd73-126">Go to Transportation management > Setup > Fuel indexes > Carrier fuel indexes.</span></span>
2. <span data-ttu-id="2bd73-127">Klikněte na položku Nová.</span><span class="sxs-lookup"><span data-stu-id="2bd73-127">Click New.</span></span>
3. <span data-ttu-id="2bd73-128">Zadejte hodnotu do pole Index paliva dopravce.</span><span class="sxs-lookup"><span data-stu-id="2bd73-128">In the Carrier fuel index field, type a value.</span></span>
4. <span data-ttu-id="2bd73-129">Zadejte nějakou hodnotu do pole Popis.</span><span class="sxs-lookup"><span data-stu-id="2bd73-129">In the Description field, type a value.</span></span>
5. <span data-ttu-id="2bd73-130">Klepněte na možnost Nový.</span><span class="sxs-lookup"><span data-stu-id="2bd73-130">Click New.</span></span>
6. <span data-ttu-id="2bd73-131">Zadejte datum a čas do pole Datum a čas platnosti.</span><span class="sxs-lookup"><span data-stu-id="2bd73-131">In the Effective start date and time field, enter a date and time.</span></span>
7. <span data-ttu-id="2bd73-132">V poli Od PPG zadejte číslo.</span><span class="sxs-lookup"><span data-stu-id="2bd73-132">In the PPG From field, enter a number.</span></span>
    * <span data-ttu-id="2bd73-133">V tomto příkladu nastavíte v poli Od PPG hodnotu 1,95.</span><span class="sxs-lookup"><span data-stu-id="2bd73-133">In this example, you can set PPG From field to 1.95.</span></span>  
8. <span data-ttu-id="2bd73-134">Do pole Do PPG zadejte číslo.</span><span class="sxs-lookup"><span data-stu-id="2bd73-134">In the PPG To field, enter a number.</span></span>
    * <span data-ttu-id="2bd73-135">V tomto příkladu nastavíte v poli Do PPG hodnotu 2.</span><span class="sxs-lookup"><span data-stu-id="2bd73-135">In this example you can set the PPG To field to 2.</span></span>  
9. <span data-ttu-id="2bd73-136">V poli Procento zadejte požadované číslo.</span><span class="sxs-lookup"><span data-stu-id="2bd73-136">In the Percentage field, enter a number.</span></span>
    * <span data-ttu-id="2bd73-137">V tomto příkladu nastavíte podíl na hodnotu 3.</span><span class="sxs-lookup"><span data-stu-id="2bd73-137">In this example you can set the percentage to 3.</span></span>  
10. <span data-ttu-id="2bd73-138">V poli Měna kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.</span><span class="sxs-lookup"><span data-stu-id="2bd73-138">In the Currency field, click the drop-down button to open the lookup.</span></span>
11. <span data-ttu-id="2bd73-139">Vyhledejte na seznamu požadovaný záznam a vyberte ho.</span><span class="sxs-lookup"><span data-stu-id="2bd73-139">In the list, find and select the desired record.</span></span>
12. <span data-ttu-id="2bd73-140">Klikněte na odkaz na vybraném řádku v seznamu.</span><span class="sxs-lookup"><span data-stu-id="2bd73-140">In the list, click the link in the selected row.</span></span>
13. <span data-ttu-id="2bd73-141">Klikněte na položku Uložit.</span><span class="sxs-lookup"><span data-stu-id="2bd73-141">Click Save.</span></span>

