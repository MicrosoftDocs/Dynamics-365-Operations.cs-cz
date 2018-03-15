--- 
title: "Vytvoření konfigurace mapování modelu (ER)"
description: "Tento postup slouží k navržení nové konfigurace mapování modelu elektronického výkaznictví a použití integrovaných funkcí ER k efektivním agregovaným výpočtům."
author: NickSelin
manager: AnnBe
ms.date: 12/12/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: kfend
ms.search.scope: Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 74606b1378e94e8a6945a408520c8b68648970d8
ms.openlocfilehash: f7206126bfa6150078f1bfb4f7e07c1cf2819ce0
ms.contentlocale: cs-cz
ms.lasthandoff: 02/07/2018

---
# <a name="create-a-model-mapping-configuration-er"></a><span data-ttu-id="428ba-103">Vytvoření konfigurace mapování modelu (ER)</span><span class="sxs-lookup"><span data-stu-id="428ba-103">Create a model mapping configuration (ER)</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="428ba-104">Tento postup slouží k navržení nové konfigurace mapování modelu elektronického výkaznictví a použití integrovaných funkcí ER k efektivním agregovaným výpočtům.</span><span class="sxs-lookup"><span data-stu-id="428ba-104">Use this procedure to design a new Electronic reporting (ER) model mapping configuration and use built-in ER functions for efficient aggregate calculations.</span></span> <span data-ttu-id="428ba-105">V tomto postupu vytvoříte konfiguraci pro vzorovou společnost Litware, Inc.</span><span class="sxs-lookup"><span data-stu-id="428ba-105">In this procedure, you will create a configuration for sample company, Litware, Inc.</span></span> 

<span data-ttu-id="428ba-106">Tento postup je vytvořen pro použití s přiřazenou rolí správce systému nebo vývojáře elektronického vykazování.</span><span class="sxs-lookup"><span data-stu-id="428ba-106">This procedure is created for uses with the assigned role of System administrator or Electronic reporting developer.</span></span>

<span data-ttu-id="428ba-107">Tyto kroky lze dokončit za použití libovolné datové sady.</span><span class="sxs-lookup"><span data-stu-id="428ba-107">These steps can be completed using any dataset.</span></span> <span data-ttu-id="428ba-108">K provedení těchto kroků musíte nejprve dokončit jednotlivé kroky v proceduře "Vytvoření poskytovatele konfigurace a jeho označení jako aktivního".</span><span class="sxs-lookup"><span data-stu-id="428ba-108">To complete these steps, you must first complete the steps in the procedure, “Create a configuration provider and mark it as active.”</span></span>

1. <span data-ttu-id="428ba-109">Přejděte do části Správa organizace > Pracovní prostory > Elektronické výkaznictví.</span><span class="sxs-lookup"><span data-stu-id="428ba-109">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
    * <span data-ttu-id="428ba-110">Ujistěte se, že poskytovatel konfigurace pro vzorovou společnost ‘Litware, Inc.’ je k dispozici a je označen jako Aktivní.</span><span class="sxs-lookup"><span data-stu-id="428ba-110">Make sure that the configuration provider for the sample company, Litware, Inc., is available and marked as Active.</span></span> <span data-ttu-id="428ba-111">Pokud tohoto zprostředkovatele konfigurace nevidíte, musíte nejprve dokončit jednotlivé kroky v postupu „Vytvoření poskytovatele konfigurace a jeho označení jako aktivního“.</span><span class="sxs-lookup"><span data-stu-id="428ba-111">If you don’t see this configuration provider, complete the steps in the procedure, “Create a configuration provider and mark it as active”.</span></span>  
2. <span data-ttu-id="428ba-112">Klikněte na Konfigurace výkaznictví.</span><span class="sxs-lookup"><span data-stu-id="428ba-112">Click Reporting configurations.</span></span>
3. <span data-ttu-id="428ba-113">Klepněte na tlačítko Zobrazit filtry.</span><span class="sxs-lookup"><span data-stu-id="428ba-113">Click Show filters.</span></span>
4. <span data-ttu-id="428ba-114">Do pole Název zadejte hodnotu filtru Intrastat a použijte operaci filtru "začíná na".</span><span class="sxs-lookup"><span data-stu-id="428ba-114">In the "Name" field, enter the filter value, "Intrastat" and use the filter operator "begins with".</span></span>
    * <span data-ttu-id="428ba-115">Tento filtr použijte k vyhledání konfigurace datového modelu ‘Intrastat’.</span><span class="sxs-lookup"><span data-stu-id="428ba-115">Apply this filter to find the ‘Intrastat’ data model configuration.</span></span> <span data-ttu-id="428ba-116">Tento model již může existovat ve stromu konfigurace.</span><span class="sxs-lookup"><span data-stu-id="428ba-116">This model may already exist in the configurations tree.</span></span> <span data-ttu-id="428ba-117">Pokud ano, vynechejte další dílčí úkol.</span><span class="sxs-lookup"><span data-stu-id="428ba-117">If it does, skip the next sub-task.</span></span>   

## <a name="get-the-intrastat-model-configuration-provided-by-microsoft"></a><span data-ttu-id="428ba-118">Získání modelové konfigurace Intrastat dodané společností Microsoft</span><span class="sxs-lookup"><span data-stu-id="428ba-118">Get the Intrastat model configuration provided by Microsoft</span></span>
1. <span data-ttu-id="428ba-119">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="428ba-119">Close the page.</span></span>
2. <span data-ttu-id="428ba-120">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="428ba-120">Close the page.</span></span>
3. <span data-ttu-id="428ba-121">Přejděte do části Správa organizace > Pracovní prostory > Elektronické výkaznictví.</span><span class="sxs-lookup"><span data-stu-id="428ba-121">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
4. <span data-ttu-id="428ba-122">Vyhledejte na seznamu požadovaný záznam a vyberte ho.</span><span class="sxs-lookup"><span data-stu-id="428ba-122">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="428ba-123">Vyberte dlaždici poskytovatele společnosti Microsoft.</span><span class="sxs-lookup"><span data-stu-id="428ba-123">Select the Microsoft provider tile.</span></span>  
5. <span data-ttu-id="428ba-124">Klikněte na možnost Úložiště.</span><span class="sxs-lookup"><span data-stu-id="428ba-124">Click Repositories.</span></span>
    * <span data-ttu-id="428ba-125">V dlaždici poskytovatele Microsoft klikněte na Úložiště.</span><span class="sxs-lookup"><span data-stu-id="428ba-125">Click Repositories in the Microsoft provider tile.</span></span>  
6. <span data-ttu-id="428ba-126">Klepněte na tlačítko Zobrazit filtry.</span><span class="sxs-lookup"><span data-stu-id="428ba-126">Click Show filters.</span></span>
7. <span data-ttu-id="428ba-127">Do pole Název typu zadejte hodnotu filtru “zdroje” a použijte operaci filtru "obsahuje".</span><span class="sxs-lookup"><span data-stu-id="428ba-127">In the "Type name" field, enter the filter value, “resources” and use the filter operator "contains".</span></span> 
8. <span data-ttu-id="428ba-128">Klikněte na možnost Otevřít.</span><span class="sxs-lookup"><span data-stu-id="428ba-128">Click Open.</span></span>
9. <span data-ttu-id="428ba-129">Ve stromovém zobrazení vyberte 'Intrastat model'.</span><span class="sxs-lookup"><span data-stu-id="428ba-129">In the tree, select 'Intrastat model'.</span></span>
10. <span data-ttu-id="428ba-130">Klepněte na tlačítko Importovat.</span><span class="sxs-lookup"><span data-stu-id="428ba-130">Click Import.</span></span>
11. <span data-ttu-id="428ba-131">Klepněte na tlačítko Ano.</span><span class="sxs-lookup"><span data-stu-id="428ba-131">Click Yes.</span></span>
    * <span data-ttu-id="428ba-132">Importovali jste konfiguraci modelu ER, která obsahuje datový model, který použijete k zjištění, jak bude možné používat novou funkci ER.</span><span class="sxs-lookup"><span data-stu-id="428ba-132">You imported the ER model configuration that contains the data model that you will use to explore how the new ER functionality can be used.</span></span>  
12. <span data-ttu-id="428ba-133">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="428ba-133">Close the page.</span></span>
13. <span data-ttu-id="428ba-134">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="428ba-134">Close the page.</span></span>
14. <span data-ttu-id="428ba-135">Klikněte na Konfigurace výkaznictví.</span><span class="sxs-lookup"><span data-stu-id="428ba-135">Click Reporting configurations.</span></span>

## <a name="add-a-new-model-mapping-configuration"></a><span data-ttu-id="428ba-136">Přidání nové konfigurace mapování modelu</span><span class="sxs-lookup"><span data-stu-id="428ba-136">Add a new model mapping configuration</span></span>
1. <span data-ttu-id="428ba-137">Ve stromovém zobrazení vyberte 'Intrastat model'.</span><span class="sxs-lookup"><span data-stu-id="428ba-137">In the tree, select 'Intrastat model'.</span></span>
2. <span data-ttu-id="428ba-138">Kliknutím na možnost Vytvořit konfiguraci otevřete dialogové okno.</span><span class="sxs-lookup"><span data-stu-id="428ba-138">Click Create configuration to open the drop dialog.</span></span>
3. <span data-ttu-id="428ba-139">V poli Nový zadejte 'Mapování modelu založené na datovém modelu Intrastat'.</span><span class="sxs-lookup"><span data-stu-id="428ba-139">In the New field, enter 'Model Mapping based on data model Intrastat'.</span></span>
4. <span data-ttu-id="428ba-140">V poli Název zadejte Mapování ukázky Intrastat.</span><span class="sxs-lookup"><span data-stu-id="428ba-140">In the Name field, type 'Intrastat sample mapping'.</span></span>
    * <span data-ttu-id="428ba-141">Mapování ukázky Intrastat</span><span class="sxs-lookup"><span data-stu-id="428ba-141">Intrastat sample mapping</span></span>  
5. <span data-ttu-id="428ba-142">Klepněte na možnost Vytvořit konfiguraci.</span><span class="sxs-lookup"><span data-stu-id="428ba-142">Click Create configuration.</span></span>


