--- 
title: "Import konfigurace ze služby Lifecycle Services pro elektronické výkaznictví (ER)"
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
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 0ea1e70f94e4b81919512127578d5927b36db56f
ms.contentlocale: cs-cz
ms.lasthandoff: 08/29/2017

---
# <a name="import-a-configuration-from-lifecycle-services-for-electronic-reporting-er"></a><span data-ttu-id="762b5-103">Import konfigurace ze služby Lifecycle Services pro elektronické výkaznictví (ER)</span><span class="sxs-lookup"><span data-stu-id="762b5-103">Import a configuration from Lifecycle Services for electronic reporting (ER)</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="762b5-104">Následující postup popisuje, jak uživatel s rolí Správce systému nebo Návrhář elektronického výkaznictví může importovat novou verzi konfigurace formátu pro elektronické výkaznictví ze služby Microsoft Lifecycle Services (LCS).</span><span class="sxs-lookup"><span data-stu-id="762b5-104">The following steps explain how a user in the System Administrator or Electronic Reporting Developer role can import a new version of an Electronic reporting (ER) configuration from Microsoft Lifecycle Services (LCS).</span></span>

<span data-ttu-id="762b5-105">V tomto příkladu zvolíte požadovanou verzi konfiguraci ER a importujete ji pro vzorovou společnost Litware, Inc a odešlete ji do LCS. Tyto kroky lze provést v kterékoli společnosti, protože konfigurace ER se sdílí mezi společnostmi.</span><span class="sxs-lookup"><span data-stu-id="762b5-105">In this example, you will select the desired version of the ER configuration and import it for sample company, Litware, Inc. These steps can be performed in any company as ER configurations are shared among companies.</span></span> <span data-ttu-id="762b5-106">K provedení těchto kroků musíte nejprve dokončit jednotlivé kroky v postupu "Odeslání konfigurace ER do služby Lifecycle Services".</span><span class="sxs-lookup"><span data-stu-id="762b5-106">To complete these steps, you must first complete the steps in the “Upload an ER configuration into Lifecycle Services” procedure.</span></span> <span data-ttu-id="762b5-107">K dokončení tohoto postupu je nutný také přístup k LCS.</span><span class="sxs-lookup"><span data-stu-id="762b5-107">Access to LCS is also required for completion of these steps.</span></span>

1. <span data-ttu-id="762b5-108">Přejděte do části Správa organizace > Pracovní prostory > Elektronické výkaznictví.</span><span class="sxs-lookup"><span data-stu-id="762b5-108">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
2. <span data-ttu-id="762b5-109">Klikněte na Konfigurace.</span><span class="sxs-lookup"><span data-stu-id="762b5-109">Click Configurations.</span></span>

## <a name="delete-a-shared-version-of-data-model-configuration"></a><span data-ttu-id="762b5-110">Odstranění sdílené verze konfigurace modelu dat</span><span class="sxs-lookup"><span data-stu-id="762b5-110">Delete a shared version of data model configuration</span></span>
1. <span data-ttu-id="762b5-111">Ve stromovém zobrazení vyberte možnost Vzorová konfigurace modelu.</span><span class="sxs-lookup"><span data-stu-id="762b5-111">In the tree, select 'Sample model configuration'.</span></span>
    * <span data-ttu-id="762b5-112">První verze vzorové konfigurace modelu dat byla vytvořena a publikována do LCS během procesu "Odeslání konfigurace ER do služby Lifecycle Services".</span><span class="sxs-lookup"><span data-stu-id="762b5-112">The first version of a sample data model configuration has been created and published to LCS during the “Upload an ER configuration into Lifecycle Services” procedure.</span></span> <span data-ttu-id="762b5-113">V tomto postupu tuto verzi konfigurace ER odstraníte.</span><span class="sxs-lookup"><span data-stu-id="762b5-113">In this procedure, you will delete this version of the ER configuration.</span></span> <span data-ttu-id="762b5-114">Tato verze vzorové konfigurace datového modelu bude importována ze LCS později.</span><span class="sxs-lookup"><span data-stu-id="762b5-114">This version of a sample data model configuration will be imported later from LCS.</span></span>  
2. <span data-ttu-id="762b5-115">Vyhledejte na seznamu požadovaný záznam a vyberte ho.</span><span class="sxs-lookup"><span data-stu-id="762b5-115">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="762b5-116">Vyberte verzi této konfigurace se stavem „Sdíleno“.</span><span class="sxs-lookup"><span data-stu-id="762b5-116">Select the version of this configuration that is in the ‘Shared’ status.</span></span> <span data-ttu-id="762b5-117">Tento stav označuje, že byla konfigurace publikována do LCS.</span><span class="sxs-lookup"><span data-stu-id="762b5-117">This status indicates that the configuration has been published to LCS.</span></span>  
3. <span data-ttu-id="762b5-118">Klikněte na položku Změnit stav.</span><span class="sxs-lookup"><span data-stu-id="762b5-118">Click Change status.</span></span>
4. <span data-ttu-id="762b5-119">Klikněte na Ukončit.</span><span class="sxs-lookup"><span data-stu-id="762b5-119">Click Discontinue.</span></span>
    * <span data-ttu-id="762b5-120">Změňte stav vybrané verze ze "Sdíleno" na „Ukončeno“ a umožněte tak její odstranění.</span><span class="sxs-lookup"><span data-stu-id="762b5-120">Change the status of the selected version from ‘Shared’ to ‘Discontinued’ to make it available for deletion.</span></span>  
5. <span data-ttu-id="762b5-121">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="762b5-121">Click OK.</span></span>
6. <span data-ttu-id="762b5-122">Vyhledejte na seznamu požadovaný záznam a vyberte ho.</span><span class="sxs-lookup"><span data-stu-id="762b5-122">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="762b5-123">Vyberte verzi této konfigurace se stavem „Ukončeno“.</span><span class="sxs-lookup"><span data-stu-id="762b5-123">Select the version of this configuration that has a status of ‘Discontinued’.</span></span>  
7. <span data-ttu-id="762b5-124">Klepněte na tlačítko Odstranit.</span><span class="sxs-lookup"><span data-stu-id="762b5-124">Click Delete.</span></span>
8. <span data-ttu-id="762b5-125">Klepněte na tlačítko Ano.</span><span class="sxs-lookup"><span data-stu-id="762b5-125">Click Yes.</span></span>
    * <span data-ttu-id="762b5-126">Všimněte si, že pouze 2. verze návrhu vybrané konfigurace modelu dat je k dispozici.</span><span class="sxs-lookup"><span data-stu-id="762b5-126">Note that the only draft version 2 of the selected data model configuration is available.</span></span>  
9. <span data-ttu-id="762b5-127">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="762b5-127">Close the page.</span></span>

## <a name="import-a-shared-version-of-data-model-configuration-from-lcs"></a><span data-ttu-id="762b5-128">Import sdílené verze konfigurace modelu dat z LCS</span><span class="sxs-lookup"><span data-stu-id="762b5-128">Import a shared version of data model configuration from LCS</span></span>
1. <span data-ttu-id="762b5-129">Označte v seznamu vybraný řádek.</span><span class="sxs-lookup"><span data-stu-id="762b5-129">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="762b5-130">Otevřete seznam úložišť pro poskytovatele konfigurace Litware, Inc.</span><span class="sxs-lookup"><span data-stu-id="762b5-130">Open the list of repositories for the ‘Litware, Inc.’</span></span> <span data-ttu-id="762b5-131"> </span><span class="sxs-lookup"><span data-stu-id="762b5-131">configuration provider.</span></span>  
2. <span data-ttu-id="762b5-132">Klikněte na možnost Úložiště.</span><span class="sxs-lookup"><span data-stu-id="762b5-132">Click Repositories.</span></span>
3. <span data-ttu-id="762b5-133">Klikněte na možnost Otevřít.</span><span class="sxs-lookup"><span data-stu-id="762b5-133">Click Open.</span></span>
    * <span data-ttu-id="762b5-134">Vyberte úložiště LCS a otevřete je.</span><span class="sxs-lookup"><span data-stu-id="762b5-134">Select the LCS repository and open it.</span></span>  
4. <span data-ttu-id="762b5-135">Označte v seznamu vybraný řádek.</span><span class="sxs-lookup"><span data-stu-id="762b5-135">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="762b5-136">Vyberte první verzi vzorové konfigurace modelu v seznamu verzí.</span><span class="sxs-lookup"><span data-stu-id="762b5-136">Select the first version of the 'Sample model configuration' in the versions list.</span></span>  
5. <span data-ttu-id="762b5-137">Klepněte na tlačítko Importovat.</span><span class="sxs-lookup"><span data-stu-id="762b5-137">Click Import.</span></span>
6. <span data-ttu-id="762b5-138">Klepněte na tlačítko Ano.</span><span class="sxs-lookup"><span data-stu-id="762b5-138">Click Yes.</span></span>
    * <span data-ttu-id="762b5-139">Potvrďte import vybrané verze z LCS.</span><span class="sxs-lookup"><span data-stu-id="762b5-139">Confirm the import of the selected version from LCS .</span></span>  
    * <span data-ttu-id="762b5-140">Všimněte si, že informační zpráva (nad formulářem) potvrzuje úspěšné dokončení importu vybrané verze.</span><span class="sxs-lookup"><span data-stu-id="762b5-140">Note that the information message (above the form) confirms the successful completion of the import of the selected version.</span></span>  
7. <span data-ttu-id="762b5-141">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="762b5-141">Close the page.</span></span>
8. <span data-ttu-id="762b5-142">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="762b5-142">Close the page.</span></span>
9. <span data-ttu-id="762b5-143">Klikněte na Konfigurace.</span><span class="sxs-lookup"><span data-stu-id="762b5-143">Click Configurations.</span></span>
10. <span data-ttu-id="762b5-144">Ve stromovém zobrazení vyberte možnost Vzorová konfigurace modelu.</span><span class="sxs-lookup"><span data-stu-id="762b5-144">In the tree, select 'Sample model configuration'.</span></span>
11. <span data-ttu-id="762b5-145">Vyhledejte na seznamu požadovaný záznam a vyberte ho.</span><span class="sxs-lookup"><span data-stu-id="762b5-145">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="762b5-146">Vyberte verzi této konfigurace se stavem „Sdíleno“.</span><span class="sxs-lookup"><span data-stu-id="762b5-146">Select the version of this configuration that has a status of ‘Shared’.</span></span>  
    * <span data-ttu-id="762b5-147">Všimněte si, že nově je také sdílená 1. verze vybrané konfigurace modelu dat k dispozici.</span><span class="sxs-lookup"><span data-stu-id="762b5-147">Note that the shared version 1 of the selected data model configuration is available now as well.</span></span>  


