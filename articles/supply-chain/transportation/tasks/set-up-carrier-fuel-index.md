--- 
title: "Nastavení indexu paliva dopravce"
description: "Tato příručka popisuje vytváření oblast indexu paliva, indexu paliva a indexu paliva dopravce."
author: BibiSp
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: bis
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 81f3244ff42cf13cd93ac10656c47f8a9204ef99
ms.contentlocale: cs-cz
ms.lasthandoff: 08/29/2017

---
# <a name="set-up-a-carrier-fuel-index"></a><span data-ttu-id="d6a23-103">Nastavení indexu paliva dopravce</span><span class="sxs-lookup"><span data-stu-id="d6a23-103">Set up a carrier fuel index</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="d6a23-104">Tato příručka popisuje vytváření oblast indexu paliva, indexu paliva a indexu paliva dopravce.</span><span class="sxs-lookup"><span data-stu-id="d6a23-104">This guide shows how to create a fuel index region, a fuel index and a carrier fuel index.</span></span> <span data-ttu-id="d6a23-105">Oblast indexu paliva určuje, pro které oblasti má být index paliva použit, a index paliva určuje cenu paliva pro určitý časový úsek.</span><span class="sxs-lookup"><span data-stu-id="d6a23-105">The fuel index region specifies which region the fuel index should apply to, and the fuel index specifies a fuel price for a particular period of time.</span></span> <span data-ttu-id="d6a23-106">Pokud chcete, aby se projevily změny cen paliva v čase, je možné přiřadit více indexů paliva k dopravci.</span><span class="sxs-lookup"><span data-stu-id="d6a23-106">To reflect the change in fuel prices over time, you can associate multiple fuel indexes with a carrier.</span></span>  <span data-ttu-id="d6a23-107">Tyto úlohy běžně provádí koordinátor přepravy.</span><span class="sxs-lookup"><span data-stu-id="d6a23-107">These tasks are normally done by a transportation coordinator.</span></span> <span data-ttu-id="d6a23-108">Tento postup můžete použít s ukázkovými daty společnosti USMF nebo pomocí vlastních dat.</span><span class="sxs-lookup"><span data-stu-id="d6a23-108">You can use this procedure in demo data company USMF or using your own data.</span></span>


## <a name="create-a-fuel-index-region"></a><span data-ttu-id="d6a23-109">Vytvoření oblasti indexu paliva</span><span class="sxs-lookup"><span data-stu-id="d6a23-109">Create a fuel index region</span></span>
1. <span data-ttu-id="d6a23-110">Přejděte na Správa přepravy > Nastavení > Indexy paliva > Oblasti indexu paliva.</span><span class="sxs-lookup"><span data-stu-id="d6a23-110">Go to Transportation management > Setup > Fuel indexes > Fuel index regions.</span></span>
    * <span data-ttu-id="d6a23-111">Nejprve je třeba vytvořit různé oblasti, které probíhá provoz a výpočet různých palivových příplatků.</span><span class="sxs-lookup"><span data-stu-id="d6a23-111">First you have to create the different regions, where you operate and calculate different fuel surcharges.</span></span>  
2. <span data-ttu-id="d6a23-112">Klikněte na položku Nová.</span><span class="sxs-lookup"><span data-stu-id="d6a23-112">Click New.</span></span>
3. <span data-ttu-id="d6a23-113">Zadejte hodnotu do pole Oblast.</span><span class="sxs-lookup"><span data-stu-id="d6a23-113">In the Region field, type a value.</span></span>
4. <span data-ttu-id="d6a23-114">Zadejte hodnotu do pole Název.</span><span class="sxs-lookup"><span data-stu-id="d6a23-114">In the Name field, type a value.</span></span>
5. <span data-ttu-id="d6a23-115">Klikněte na položku Uložit.</span><span class="sxs-lookup"><span data-stu-id="d6a23-115">Click Save.</span></span>

## <a name="create-a-fuel-index"></a><span data-ttu-id="d6a23-116">Vytvoření indexu paliva</span><span class="sxs-lookup"><span data-stu-id="d6a23-116">Create a fuel index</span></span>
1. <span data-ttu-id="d6a23-117">Přejděte na Správa přepravy > Nastavení > Indexy paliva > Indexy paliva.</span><span class="sxs-lookup"><span data-stu-id="d6a23-117">Go to Transportation management > Setup > Fuel indexes > Fuel indexes.</span></span>
    * <span data-ttu-id="d6a23-118">Pro nastavené oblasti je nutné zadat aktuální ceny paliva.</span><span class="sxs-lookup"><span data-stu-id="d6a23-118">For the regions you have set up you need to enter the current prices for the fuel.</span></span>  
2. <span data-ttu-id="d6a23-119">Klikněte na položku Nová.</span><span class="sxs-lookup"><span data-stu-id="d6a23-119">Click New.</span></span>
3. <span data-ttu-id="d6a23-120">V poli Oblast kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.</span><span class="sxs-lookup"><span data-stu-id="d6a23-120">In the Region field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="d6a23-121">Klikněte na odkaz na vybraném řádku v seznamu.</span><span class="sxs-lookup"><span data-stu-id="d6a23-121">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="d6a23-122">V poli Cena za galon zadejte číslo.</span><span class="sxs-lookup"><span data-stu-id="d6a23-122">In the Price per gallon field, enter a number.</span></span>
6. <span data-ttu-id="d6a23-123">Zadejte datum a čas do pole Datum a čas platnosti.</span><span class="sxs-lookup"><span data-stu-id="d6a23-123">In the Effective start date and time field, enter a date and time.</span></span>
7. <span data-ttu-id="d6a23-124">Klikněte na položku Uložit.</span><span class="sxs-lookup"><span data-stu-id="d6a23-124">Click Save.</span></span>

## <a name="create-a-carrier-fuel-index"></a><span data-ttu-id="d6a23-125">Vytvoření indexu paliva pro dopravce</span><span class="sxs-lookup"><span data-stu-id="d6a23-125">Create a Carrier fuel index</span></span>
1. <span data-ttu-id="d6a23-126">Přejděte na Správa přepravy > Nastavení > Indexy paliva > Indexy paliva pro dopravce.</span><span class="sxs-lookup"><span data-stu-id="d6a23-126">Go to Transportation management > Setup > Fuel indexes > Carrier fuel indexes.</span></span>
2. <span data-ttu-id="d6a23-127">Klikněte na položku Nová.</span><span class="sxs-lookup"><span data-stu-id="d6a23-127">Click New.</span></span>
3. <span data-ttu-id="d6a23-128">Zadejte hodnotu do pole Index paliva dopravce.</span><span class="sxs-lookup"><span data-stu-id="d6a23-128">In the Carrier fuel index field, type a value.</span></span>
4. <span data-ttu-id="d6a23-129">Zadejte nějakou hodnotu do pole Popis.</span><span class="sxs-lookup"><span data-stu-id="d6a23-129">In the Description field, type a value.</span></span>
5. <span data-ttu-id="d6a23-130">Klepněte na možnost Nový.</span><span class="sxs-lookup"><span data-stu-id="d6a23-130">Click New.</span></span>
6. <span data-ttu-id="d6a23-131">Zadejte datum a čas do pole Datum a čas platnosti.</span><span class="sxs-lookup"><span data-stu-id="d6a23-131">In the Effective start date and time field, enter a date and time.</span></span>
7. <span data-ttu-id="d6a23-132">V poli Od PPG zadejte číslo.</span><span class="sxs-lookup"><span data-stu-id="d6a23-132">In the PPG From field, enter a number.</span></span>
    * <span data-ttu-id="d6a23-133">V tomto příkladu nastavíte v poli Od PPG hodnotu 1,95.</span><span class="sxs-lookup"><span data-stu-id="d6a23-133">In this example, you can set PPG From field to 1.95.</span></span>  
8. <span data-ttu-id="d6a23-134">Do pole Do PPG zadejte číslo.</span><span class="sxs-lookup"><span data-stu-id="d6a23-134">In the PPG To field, enter a number.</span></span>
    * <span data-ttu-id="d6a23-135">V tomto příkladu nastavíte v poli Do PPG hodnotu 2.</span><span class="sxs-lookup"><span data-stu-id="d6a23-135">In this example you can set the PPG To field to 2.</span></span>  
9. <span data-ttu-id="d6a23-136">V poli Procento zadejte požadované číslo.</span><span class="sxs-lookup"><span data-stu-id="d6a23-136">In the Percentage field, enter a number.</span></span>
    * <span data-ttu-id="d6a23-137">V tomto příkladu nastavíte podíl na hodnotu 3.</span><span class="sxs-lookup"><span data-stu-id="d6a23-137">In this example you can set the percentage to 3.</span></span>  
10. <span data-ttu-id="d6a23-138">V poli Měna kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.</span><span class="sxs-lookup"><span data-stu-id="d6a23-138">In the Currency field, click the drop-down button to open the lookup.</span></span>
11. <span data-ttu-id="d6a23-139">Vyhledejte na seznamu požadovaný záznam a vyberte ho.</span><span class="sxs-lookup"><span data-stu-id="d6a23-139">In the list, find and select the desired record.</span></span>
12. <span data-ttu-id="d6a23-140">Klikněte na odkaz na vybraném řádku v seznamu.</span><span class="sxs-lookup"><span data-stu-id="d6a23-140">In the list, click the link in the selected row.</span></span>
13. <span data-ttu-id="d6a23-141">Klikněte na položku Uložit.</span><span class="sxs-lookup"><span data-stu-id="d6a23-141">Click Save.</span></span>


