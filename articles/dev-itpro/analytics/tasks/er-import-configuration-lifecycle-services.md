--- 
title: "Import konfigurací elektronického výkaznictví ze služby Lifecycle Services"
description: "Následující postup popisuje, jak uživatel s rolí Správce systému nebo Návrhář elektronického výkaznictví může importovat novou verzi konfigurace formátu pro elektronické výkaznictví ze služby Microsoft Lifecycle Services (LCS)."
author: NickSelin
manager: AnnBe
ms.date: 05/13/2016
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
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: e782d33f3748524491dace28008cd9148ae70529
ms.openlocfilehash: f3b8cdb722cf49194faccc19fbb95265a230d48b
ms.contentlocale: cs-cz
ms.lasthandoff: 08/08/2018

---
# <a name="import-electronic-reporting-configurations-from-lifecycle-services"></a><span data-ttu-id="5f6e0-103">Import konfigurací elektronického výkaznictví ze služby Lifecycle Services</span><span class="sxs-lookup"><span data-stu-id="5f6e0-103">Import Electronic reporting configurations from Lifecycle Services</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="5f6e0-104">Následující postup popisuje, jak uživatel s rolí Správce systému nebo Návrhář elektronického výkaznictví může importovat novou verzi konfigurace formátu pro elektronické výkaznictví ze služby Microsoft Lifecycle Services (LCS).</span><span class="sxs-lookup"><span data-stu-id="5f6e0-104">The following steps explain how a user in the System Administrator or Electronic Reporting Developer role can import a new version of an Electronic reporting (ER) configuration from Microsoft Lifecycle Services (LCS).</span></span>

<span data-ttu-id="5f6e0-105">V tomto příkladu zvolíte požadovanou verzi konfiguraci ER a importujete ji pro vzorovou společnost Litware, Inc a odešlete ji do LCS. Tyto kroky lze provést v kterékoli společnosti, protože konfigurace ER se sdílí mezi společnostmi.</span><span class="sxs-lookup"><span data-stu-id="5f6e0-105">In this example, you will select the desired version of the ER configuration and import it for sample company, Litware, Inc. These steps can be performed in any company as ER configurations are shared among companies.</span></span> <span data-ttu-id="5f6e0-106">K provedení těchto kroků musíte nejprve dokončit jednotlivé kroky v postupu "Odeslání konfigurace ER do služby Lifecycle Services".</span><span class="sxs-lookup"><span data-stu-id="5f6e0-106">To complete these steps, you must first complete the steps in the “Upload an ER configuration into Lifecycle Services” procedure.</span></span> <span data-ttu-id="5f6e0-107">K dokončení tohoto postupu je nutný také přístup k LCS.</span><span class="sxs-lookup"><span data-stu-id="5f6e0-107">Access to LCS is also required for completion of these steps.</span></span>

1. <span data-ttu-id="5f6e0-108">Přejděte do části Správa organizace > Pracovní prostory > Elektronické výkaznictví.</span><span class="sxs-lookup"><span data-stu-id="5f6e0-108">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
2. <span data-ttu-id="5f6e0-109">Klikněte na Konfigurace.</span><span class="sxs-lookup"><span data-stu-id="5f6e0-109">Click Configurations.</span></span>

## <a name="delete-a-shared-version-of-data-model-configuration"></a><span data-ttu-id="5f6e0-110">Odstranění sdílené verze konfigurace modelu dat</span><span class="sxs-lookup"><span data-stu-id="5f6e0-110">Delete a shared version of data model configuration</span></span>
1. <span data-ttu-id="5f6e0-111">Ve stromovém zobrazení vyberte možnost Vzorová konfigurace modelu.</span><span class="sxs-lookup"><span data-stu-id="5f6e0-111">In the tree, select 'Sample model configuration'.</span></span>
    * <span data-ttu-id="5f6e0-112">První verze vzorové konfigurace modelu dat byla vytvořena a publikována do LCS během procesu "Odeslání konfigurace ER do služby Lifecycle Services".</span><span class="sxs-lookup"><span data-stu-id="5f6e0-112">The first version of a sample data model configuration has been created and published to LCS during the “Upload an ER configuration into Lifecycle Services” procedure.</span></span> <span data-ttu-id="5f6e0-113">V tomto postupu tuto verzi konfigurace ER odstraníte.</span><span class="sxs-lookup"><span data-stu-id="5f6e0-113">In this procedure, you will delete this version of the ER configuration.</span></span> <span data-ttu-id="5f6e0-114">Tato verze vzorové konfigurace datového modelu bude importována ze LCS později.</span><span class="sxs-lookup"><span data-stu-id="5f6e0-114">This version of a sample data model configuration will be imported later from LCS.</span></span>  
2. <span data-ttu-id="5f6e0-115">Vyhledejte na seznamu požadovaný záznam a vyberte ho.</span><span class="sxs-lookup"><span data-stu-id="5f6e0-115">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="5f6e0-116">Vyberte verzi této konfigurace se stavem „Sdíleno“.</span><span class="sxs-lookup"><span data-stu-id="5f6e0-116">Select the version of this configuration that is in the ‘Shared’ status.</span></span> <span data-ttu-id="5f6e0-117">Tento stav označuje, že byla konfigurace publikována do LCS.</span><span class="sxs-lookup"><span data-stu-id="5f6e0-117">This status indicates that the configuration has been published to LCS.</span></span>  
3. <span data-ttu-id="5f6e0-118">Klikněte na položku Změnit stav.</span><span class="sxs-lookup"><span data-stu-id="5f6e0-118">Click Change status.</span></span>
4. <span data-ttu-id="5f6e0-119">Klikněte na Ukončit.</span><span class="sxs-lookup"><span data-stu-id="5f6e0-119">Click Discontinue.</span></span>
    * <span data-ttu-id="5f6e0-120">Změňte stav vybrané verze ze "Sdíleno" na „Ukončeno“ a umožněte tak její odstranění.</span><span class="sxs-lookup"><span data-stu-id="5f6e0-120">Change the status of the selected version from ‘Shared’ to ‘Discontinued’ to make it available for deletion.</span></span>  
5. <span data-ttu-id="5f6e0-121">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="5f6e0-121">Click OK.</span></span>
6. <span data-ttu-id="5f6e0-122">Vyhledejte na seznamu požadovaný záznam a vyberte ho.</span><span class="sxs-lookup"><span data-stu-id="5f6e0-122">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="5f6e0-123">Vyberte verzi této konfigurace se stavem „Ukončeno“.</span><span class="sxs-lookup"><span data-stu-id="5f6e0-123">Select the version of this configuration that has a status of ‘Discontinued’.</span></span>  
7. <span data-ttu-id="5f6e0-124">Klepněte na tlačítko Odstranit.</span><span class="sxs-lookup"><span data-stu-id="5f6e0-124">Click Delete.</span></span>
8. <span data-ttu-id="5f6e0-125">Klepněte na tlačítko Ano.</span><span class="sxs-lookup"><span data-stu-id="5f6e0-125">Click Yes.</span></span>
    * <span data-ttu-id="5f6e0-126">Všimněte si, že pouze 2. verze návrhu vybrané konfigurace modelu dat je k dispozici.</span><span class="sxs-lookup"><span data-stu-id="5f6e0-126">Note that the only draft version 2 of the selected data model configuration is available.</span></span>  
9. <span data-ttu-id="5f6e0-127">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="5f6e0-127">Close the page.</span></span>

## <a name="import-a-shared-version-of-data-model-configuration-from-lcs"></a><span data-ttu-id="5f6e0-128">Import sdílené verze konfigurace modelu dat z LCS</span><span class="sxs-lookup"><span data-stu-id="5f6e0-128">Import a shared version of data model configuration from LCS</span></span>
1. <span data-ttu-id="5f6e0-129">Označte v seznamu vybraný řádek.</span><span class="sxs-lookup"><span data-stu-id="5f6e0-129">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="5f6e0-130">Otevřete seznam úložišť pro poskytovatele konfigurace Litware, Inc.</span><span class="sxs-lookup"><span data-stu-id="5f6e0-130">Open the list of repositories for the ‘Litware, Inc.’</span></span> <span data-ttu-id="5f6e0-131"> </span><span class="sxs-lookup"><span data-stu-id="5f6e0-131">configuration provider.</span></span>  
2. <span data-ttu-id="5f6e0-132">Klikněte na možnost Úložiště.</span><span class="sxs-lookup"><span data-stu-id="5f6e0-132">Click Repositories.</span></span>
3. <span data-ttu-id="5f6e0-133">Klikněte na možnost Otevřít.</span><span class="sxs-lookup"><span data-stu-id="5f6e0-133">Click Open.</span></span>
    * <span data-ttu-id="5f6e0-134">Vyberte úložiště LCS a otevřete je.</span><span class="sxs-lookup"><span data-stu-id="5f6e0-134">Select the LCS repository and open it.</span></span>  
4. <span data-ttu-id="5f6e0-135">Označte v seznamu vybraný řádek.</span><span class="sxs-lookup"><span data-stu-id="5f6e0-135">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="5f6e0-136">Vyberte první verzi vzorové konfigurace modelu v seznamu verzí.</span><span class="sxs-lookup"><span data-stu-id="5f6e0-136">Select the first version of the 'Sample model configuration' in the versions list.</span></span>  
5. <span data-ttu-id="5f6e0-137">Klepněte na tlačítko Importovat.</span><span class="sxs-lookup"><span data-stu-id="5f6e0-137">Click Import.</span></span>
6. <span data-ttu-id="5f6e0-138">Klepněte na tlačítko Ano.</span><span class="sxs-lookup"><span data-stu-id="5f6e0-138">Click Yes.</span></span>
    * <span data-ttu-id="5f6e0-139">Potvrďte import vybrané verze z LCS.</span><span class="sxs-lookup"><span data-stu-id="5f6e0-139">Confirm the import of the selected version from LCS .</span></span>  
    * <span data-ttu-id="5f6e0-140">Všimněte si, že informační zpráva (nad formulářem) potvrzuje úspěšné dokončení importu vybrané verze.</span><span class="sxs-lookup"><span data-stu-id="5f6e0-140">Note that the information message (above the form) confirms the successful completion of the import of the selected version.</span></span>  
7. <span data-ttu-id="5f6e0-141">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="5f6e0-141">Close the page.</span></span>
8. <span data-ttu-id="5f6e0-142">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="5f6e0-142">Close the page.</span></span>
9. <span data-ttu-id="5f6e0-143">Klikněte na Konfigurace.</span><span class="sxs-lookup"><span data-stu-id="5f6e0-143">Click Configurations.</span></span>
10. <span data-ttu-id="5f6e0-144">Ve stromovém zobrazení vyberte možnost Vzorová konfigurace modelu.</span><span class="sxs-lookup"><span data-stu-id="5f6e0-144">In the tree, select 'Sample model configuration'.</span></span>
11. <span data-ttu-id="5f6e0-145">Vyhledejte na seznamu požadovaný záznam a vyberte ho.</span><span class="sxs-lookup"><span data-stu-id="5f6e0-145">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="5f6e0-146">Vyberte verzi této konfigurace se stavem „Sdíleno“.</span><span class="sxs-lookup"><span data-stu-id="5f6e0-146">Select the version of this configuration that has a status of ‘Shared’.</span></span>  
    * <span data-ttu-id="5f6e0-147">Všimněte si, že nově je také sdílená 1. verze vybrané konfigurace modelu dat k dispozici.</span><span class="sxs-lookup"><span data-stu-id="5f6e0-147">Note that the shared version 1 of the selected data model configuration is available now as well.</span></span>  


