---
title: Import konfigurace ER ze služby Lifecycle Services
description: Následující postup popisuje, jak uživatel s rolí Správce systému nebo Návrhář elektronického výkaznictví může importovat novou verzi konfigurace formátu pro elektronické výkaznictví ze služby Microsoft Lifecycle Services (LCS).
author: NickSelin
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ERWorkspace, ERSolutionTable,  ERSolutionRepositoryTable, ERSolutionImport
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 036d7e7e3f79e0945d6fef866a30edd41e688c07
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/15/2019
ms.locfileid: "1551315"
---
# <a name="er-import-a-configuration-from-lifecycle-services"></a><span data-ttu-id="2e043-103">Import konfigurace ER ze služby Lifecycle Services</span><span class="sxs-lookup"><span data-stu-id="2e043-103">ER Import a configuration from Lifecycle Services</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="2e043-104">Následující postup popisuje, jak uživatel s rolí Správce systému nebo Návrhář elektronického výkaznictví může importovat novou verzi konfigurace formátu pro elektronické výkaznictví ze služby Microsoft Lifecycle Services (LCS).</span><span class="sxs-lookup"><span data-stu-id="2e043-104">The following steps explain how a user in the System Administrator or Electronic Reporting Developer role can import a new version of an Electronic reporting (ER) configuration from Microsoft Lifecycle Services (LCS).</span></span>

<span data-ttu-id="2e043-105">V tomto příkladu zvolíte požadovanou verzi konfiguraci ER a importujete ji pro vzorovou společnost Litware, Inc a odešlete ji do LCS. Tyto kroky lze provést v kterékoli společnosti, protože konfigurace ER se sdílí mezi společnostmi.</span><span class="sxs-lookup"><span data-stu-id="2e043-105">In this example, you will select the desired version of the ER configuration and import it for sample company, Litware, Inc. These steps can be performed in any company as ER configurations are shared among companies.</span></span> <span data-ttu-id="2e043-106">K provedení těchto kroků musíte nejprve dokončit jednotlivé kroky v postupu "Odeslání konfigurace ER do služby Lifecycle Services".</span><span class="sxs-lookup"><span data-stu-id="2e043-106">To complete these steps, you must first complete the steps in the “Upload an ER configuration into Lifecycle Services” procedure.</span></span> <span data-ttu-id="2e043-107">K dokončení tohoto postupu je nutný také přístup k LCS.</span><span class="sxs-lookup"><span data-stu-id="2e043-107">Access to LCS is also required for completion of these steps.</span></span>

1. <span data-ttu-id="2e043-108">Přejděte do části Správa organizace > Pracovní prostory > Elektronické výkaznictví.</span><span class="sxs-lookup"><span data-stu-id="2e043-108">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
2. <span data-ttu-id="2e043-109">Klikněte na Konfigurace.</span><span class="sxs-lookup"><span data-stu-id="2e043-109">Click Configurations.</span></span>

## <a name="delete-a-shared-version-of-data-model-configuration"></a><span data-ttu-id="2e043-110">Odstranění sdílené verze konfigurace modelu dat</span><span class="sxs-lookup"><span data-stu-id="2e043-110">Delete a shared version of data model configuration</span></span>
1. <span data-ttu-id="2e043-111">Ve stromovém zobrazení vyberte možnost Vzorová konfigurace modelu.</span><span class="sxs-lookup"><span data-stu-id="2e043-111">In the tree, select 'Sample model configuration'.</span></span>
    * <span data-ttu-id="2e043-112">První verze vzorové konfigurace modelu dat byla vytvořena a publikována do LCS během procesu "Odeslání konfigurace ER do služby Lifecycle Services".</span><span class="sxs-lookup"><span data-stu-id="2e043-112">The first version of a sample data model configuration has been created and published to LCS during the “Upload an ER configuration into Lifecycle Services” procedure.</span></span> <span data-ttu-id="2e043-113">V tomto postupu tuto verzi konfigurace ER odstraníte.</span><span class="sxs-lookup"><span data-stu-id="2e043-113">In this procedure, you will delete this version of the ER configuration.</span></span> <span data-ttu-id="2e043-114">Tato verze vzorové konfigurace datového modelu bude importována ze LCS později.</span><span class="sxs-lookup"><span data-stu-id="2e043-114">This version of a sample data model configuration will be imported later from LCS.</span></span>  
2. <span data-ttu-id="2e043-115">Vyhledejte na seznamu požadovaný záznam a vyberte ho.</span><span class="sxs-lookup"><span data-stu-id="2e043-115">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="2e043-116">Vyberte verzi této konfigurace se stavem „Sdíleno“.</span><span class="sxs-lookup"><span data-stu-id="2e043-116">Select the version of this configuration that is in the ‘Shared’ status.</span></span> <span data-ttu-id="2e043-117">Tento stav označuje, že byla konfigurace publikována do LCS.</span><span class="sxs-lookup"><span data-stu-id="2e043-117">This status indicates that the configuration has been published to LCS.</span></span>  
3. <span data-ttu-id="2e043-118">Klikněte na položku Změnit stav.</span><span class="sxs-lookup"><span data-stu-id="2e043-118">Click Change status.</span></span>
4. <span data-ttu-id="2e043-119">Klikněte na Ukončit.</span><span class="sxs-lookup"><span data-stu-id="2e043-119">Click Discontinue.</span></span>
    * <span data-ttu-id="2e043-120">Změňte stav vybrané verze ze "Sdíleno" na „Ukončeno“ a umožněte tak její odstranění.</span><span class="sxs-lookup"><span data-stu-id="2e043-120">Change the status of the selected version from ‘Shared’ to ‘Discontinued’ to make it available for deletion.</span></span>  
5. <span data-ttu-id="2e043-121">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="2e043-121">Click OK.</span></span>
6. <span data-ttu-id="2e043-122">Vyhledejte na seznamu požadovaný záznam a vyberte ho.</span><span class="sxs-lookup"><span data-stu-id="2e043-122">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="2e043-123">Vyberte verzi této konfigurace se stavem „Ukončeno“.</span><span class="sxs-lookup"><span data-stu-id="2e043-123">Select the version of this configuration that has a status of ‘Discontinued’.</span></span>  
7. <span data-ttu-id="2e043-124">Klepněte na tlačítko Odstranit.</span><span class="sxs-lookup"><span data-stu-id="2e043-124">Click Delete.</span></span>
8. <span data-ttu-id="2e043-125">Klepněte na tlačítko Ano.</span><span class="sxs-lookup"><span data-stu-id="2e043-125">Click Yes.</span></span>
    * <span data-ttu-id="2e043-126">Všimněte si, že pouze 2. verze návrhu vybrané konfigurace modelu dat je k dispozici.</span><span class="sxs-lookup"><span data-stu-id="2e043-126">Note that the only draft version 2 of the selected data model configuration is available.</span></span>  
9. <span data-ttu-id="2e043-127">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="2e043-127">Close the page.</span></span>

## <a name="import-a-shared-version-of-data-model-configuration-from-lcs"></a><span data-ttu-id="2e043-128">Import sdílené verze konfigurace modelu dat z LCS</span><span class="sxs-lookup"><span data-stu-id="2e043-128">Import a shared version of data model configuration from LCS</span></span>
1. <span data-ttu-id="2e043-129">Označte v seznamu vybraný řádek.</span><span class="sxs-lookup"><span data-stu-id="2e043-129">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="2e043-130">Otevřete seznam úložišť pro poskytovatele konfigurace Litware, Inc.</span><span class="sxs-lookup"><span data-stu-id="2e043-130">Open the list of repositories for the ‘Litware, Inc.’</span></span> <span data-ttu-id="2e043-131"> </span><span class="sxs-lookup"><span data-stu-id="2e043-131">configuration provider.</span></span>  
2. <span data-ttu-id="2e043-132">Klikněte na možnost Úložiště.</span><span class="sxs-lookup"><span data-stu-id="2e043-132">Click Repositories.</span></span>
3. <span data-ttu-id="2e043-133">Klikněte na možnost Otevřít.</span><span class="sxs-lookup"><span data-stu-id="2e043-133">Click Open.</span></span>
    * <span data-ttu-id="2e043-134">Vyberte úložiště LCS a otevřete je.</span><span class="sxs-lookup"><span data-stu-id="2e043-134">Select the LCS repository and open it.</span></span>  
4. <span data-ttu-id="2e043-135">Označte v seznamu vybraný řádek.</span><span class="sxs-lookup"><span data-stu-id="2e043-135">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="2e043-136">Vyberte první verzi vzorové konfigurace modelu v seznamu verzí.</span><span class="sxs-lookup"><span data-stu-id="2e043-136">Select the first version of the 'Sample model configuration' in the versions list.</span></span>  
5. <span data-ttu-id="2e043-137">Klepněte na tlačítko Importovat.</span><span class="sxs-lookup"><span data-stu-id="2e043-137">Click Import.</span></span>
6. <span data-ttu-id="2e043-138">Klepněte na tlačítko Ano.</span><span class="sxs-lookup"><span data-stu-id="2e043-138">Click Yes.</span></span>
    * <span data-ttu-id="2e043-139">Potvrďte import vybrané verze z LCS.</span><span class="sxs-lookup"><span data-stu-id="2e043-139">Confirm the import of the selected version from LCS .</span></span>  
    * <span data-ttu-id="2e043-140">Všimněte si, že informační zpráva (nad formulářem) potvrzuje úspěšné dokončení importu vybrané verze.</span><span class="sxs-lookup"><span data-stu-id="2e043-140">Note that the information message (above the form) confirms the successful completion of the import of the selected version.</span></span>  
7. <span data-ttu-id="2e043-141">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="2e043-141">Close the page.</span></span>
8. <span data-ttu-id="2e043-142">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="2e043-142">Close the page.</span></span>
9. <span data-ttu-id="2e043-143">Klikněte na Konfigurace.</span><span class="sxs-lookup"><span data-stu-id="2e043-143">Click Configurations.</span></span>
10. <span data-ttu-id="2e043-144">Ve stromovém zobrazení vyberte možnost Vzorová konfigurace modelu.</span><span class="sxs-lookup"><span data-stu-id="2e043-144">In the tree, select 'Sample model configuration'.</span></span>
11. <span data-ttu-id="2e043-145">Vyhledejte na seznamu požadovaný záznam a vyberte ho.</span><span class="sxs-lookup"><span data-stu-id="2e043-145">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="2e043-146">Vyberte verzi této konfigurace se stavem „Sdíleno“.</span><span class="sxs-lookup"><span data-stu-id="2e043-146">Select the version of this configuration that has a status of ‘Shared’.</span></span>  
    * <span data-ttu-id="2e043-147">Všimněte si, že nově je také sdílená 1. verze vybrané konfigurace modelu dat k dispozici.</span><span class="sxs-lookup"><span data-stu-id="2e043-147">Note that the shared version 1 of the selected data model configuration is available now as well.</span></span>  

