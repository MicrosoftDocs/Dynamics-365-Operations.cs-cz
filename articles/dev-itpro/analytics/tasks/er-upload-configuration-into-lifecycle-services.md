---
title: Odeslání konfigurace ER do služby Lifecycle Services
description: Následující postup popisuje, jak uživatel s rolí Správce systému nebo Návrhář elektronického výkaznictví může vytvořit novou konfiguraci formátu pro elektronické výkaznictví a odeslat ji do služby Microsoft Lifecycle Services (LCS).
author: NickSelin
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ERWorkspace, ERSolutionTable, ERSolutionCreateDropDialog, ERDataModelDesigner, ERDataModelContentsItemCreationDialog, ERSolutionRepositoryTable, ERSolutionRepositoryCreateDropDialog, ERSolutionImport
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 19ae8820e5d4a798a5789e9632edb431fe9fede4
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/15/2019
ms.locfileid: "1551106"
---
# <a name="er-upload-a-configuration-into-lifecycle-services"></a><span data-ttu-id="b9e42-103">Odeslání konfigurace ER do služby Lifecycle Services</span><span class="sxs-lookup"><span data-stu-id="b9e42-103">ER Upload a configuration into Lifecycle Services</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="b9e42-104">Následující postup popisuje, jak uživatel s rolí Správce systému nebo Návrhář elektronického výkaznictví může vytvořit novou konfiguraci formátu pro elektronické výkaznictví a odeslat ji do služby Microsoft Lifecycle Services (LCS).</span><span class="sxs-lookup"><span data-stu-id="b9e42-104">The following steps explain how a user in the System Administrator or Electronic Reporting Developer role can create a new Electronic reporting (ER) configuration and upload it into Microsoft Lifecycle Services (LCS).</span></span>

<span data-ttu-id="b9e42-105">V tomto příkladu vytvoříte konfiguraci pro vzorovou společnost Litware, Inc a odešlete ji do LCS. Tyto kroky lze provést v kterékoli společnosti, protože konfigurace ER se sdílí mezi společnostmi.</span><span class="sxs-lookup"><span data-stu-id="b9e42-105">In this example, you will create a configuration and upload it to LCS for sample company, Litware, Inc. These steps can be performed in any company as ER configurations are shared among companies.</span></span> <span data-ttu-id="b9e42-106">K provedení těchto kroků musíte nejprve dokončit jednotlivé kroky v postupu "Vytvoření poskytovatele konfigurace a jeho označení jako aktivního".</span><span class="sxs-lookup"><span data-stu-id="b9e42-106">To complete these steps, you must first complete the steps in the “Create a configuration provider and mark it as active” procedure.</span></span> <span data-ttu-id="b9e42-107">K dokončení tohoto postupu je nutný také přístup k LCS.</span><span class="sxs-lookup"><span data-stu-id="b9e42-107">Access to LCS is also required for completion of these steps.</span></span>

1. <span data-ttu-id="b9e42-108">Přejděte do části Správa organizace > Pracovní prostory > Elektronické výkaznictví.</span><span class="sxs-lookup"><span data-stu-id="b9e42-108">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
2. <span data-ttu-id="b9e42-109">Vyberte Litware, Inc.</span><span class="sxs-lookup"><span data-stu-id="b9e42-109">Select ‘Litware, Inc.’</span></span> <span data-ttu-id="b9e42-110">a nastavte ji jako aktivní.</span><span class="sxs-lookup"><span data-stu-id="b9e42-110">and set it as active.</span></span>
3. <span data-ttu-id="b9e42-111">Klikněte na Konfigurace.</span><span class="sxs-lookup"><span data-stu-id="b9e42-111">Click Configurations.</span></span>

## <a name="create-a-new-data-model-configuration"></a><span data-ttu-id="b9e42-112">Vytvoření nové konfigurace datového modelu</span><span class="sxs-lookup"><span data-stu-id="b9e42-112">Create a new data model configuration</span></span>
1. <span data-ttu-id="b9e42-113">Kliknutím na možnost Vytvořit konfiguraci otevřete dialogové okno.</span><span class="sxs-lookup"><span data-stu-id="b9e42-113">Click Create configuration to open the drop dialog.</span></span>
    * <span data-ttu-id="b9e42-114">Vytvoříte konfiguraci, která obsahuje vzorový model dat pro elektronické doklady.</span><span class="sxs-lookup"><span data-stu-id="b9e42-114">You will create a configuration that contains a sample data model for electronic documents.</span></span> <span data-ttu-id="b9e42-115">Tato konfigurace modelu dat bude odeslána do LCS později.</span><span class="sxs-lookup"><span data-stu-id="b9e42-115">This data model configuration will be uploaded into LCS later.</span></span>  
2. <span data-ttu-id="b9e42-116">V poli Název zadejte Vzorová konfigurace modelu.</span><span class="sxs-lookup"><span data-stu-id="b9e42-116">In the Name field, type 'Sample model configuration'.</span></span>
    * <span data-ttu-id="b9e42-117">Vzorová konfigurace modelu</span><span class="sxs-lookup"><span data-stu-id="b9e42-117">Sample model configuration</span></span>  
3. <span data-ttu-id="b9e42-118">V poli Popis zadejte „Vzorová konfigurace modelu“.</span><span class="sxs-lookup"><span data-stu-id="b9e42-118">In the Description field, type 'Sample model configuration'.</span></span>
    * <span data-ttu-id="b9e42-119">Vzorová konfigurace modelu</span><span class="sxs-lookup"><span data-stu-id="b9e42-119">Sample model configuration</span></span>  
4. <span data-ttu-id="b9e42-120">Klepněte na možnost Vytvořit konfiguraci.</span><span class="sxs-lookup"><span data-stu-id="b9e42-120">Click Create configuration.</span></span>
5. <span data-ttu-id="b9e42-121">Klikněte na Návrhář modelů.</span><span class="sxs-lookup"><span data-stu-id="b9e42-121">Click Model designer.</span></span>
6. <span data-ttu-id="b9e42-122">Klikněte na položku Nová.</span><span class="sxs-lookup"><span data-stu-id="b9e42-122">Click New.</span></span>
7. <span data-ttu-id="b9e42-123">Do pole Název zadejte Vstupní bod.</span><span class="sxs-lookup"><span data-stu-id="b9e42-123">In the Name field, type 'Entry point'.</span></span>
    * <span data-ttu-id="b9e42-124">Vstupní bod</span><span class="sxs-lookup"><span data-stu-id="b9e42-124">Entry point</span></span>  
8. <span data-ttu-id="b9e42-125">Klepněte na možnost Přidat.</span><span class="sxs-lookup"><span data-stu-id="b9e42-125">Click Add.</span></span>
9. <span data-ttu-id="b9e42-126">Klikněte na položku Uložit.</span><span class="sxs-lookup"><span data-stu-id="b9e42-126">Click Save.</span></span>
10. <span data-ttu-id="b9e42-127">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="b9e42-127">Close the page.</span></span>
11. <span data-ttu-id="b9e42-128">Klikněte na položku Změnit stav.</span><span class="sxs-lookup"><span data-stu-id="b9e42-128">Click Change status.</span></span>
12. <span data-ttu-id="b9e42-129">Klikněte na tlačítko Dokončit.</span><span class="sxs-lookup"><span data-stu-id="b9e42-129">Click Complete.</span></span>
13. <span data-ttu-id="b9e42-130">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="b9e42-130">Click OK.</span></span>

## <a name="register-a-new--repository"></a><span data-ttu-id="b9e42-131">Registrace nového úložiště</span><span class="sxs-lookup"><span data-stu-id="b9e42-131">Register a new  repository</span></span>
1. <span data-ttu-id="b9e42-132">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="b9e42-132">Close the page.</span></span>
2. <span data-ttu-id="b9e42-133">Klikněte na možnost Úložiště.</span><span class="sxs-lookup"><span data-stu-id="b9e42-133">Click Repositories.</span></span>
    * <span data-ttu-id="b9e42-134">To umožňuje otevřít seznam úložišť pro poskytovatele konfigurace Litware, Inc.</span><span class="sxs-lookup"><span data-stu-id="b9e42-134">This enables you to open the list of repositories for the Litware, Inc. configuration provider.</span></span>  
3. <span data-ttu-id="b9e42-135">Klepnutím na možnost Přidat otevřete dialogové okno.</span><span class="sxs-lookup"><span data-stu-id="b9e42-135">Click Add to open the drop dialog.</span></span>
    * <span data-ttu-id="b9e42-136">Tímto způsobem můžete přidat nové úložiště.</span><span class="sxs-lookup"><span data-stu-id="b9e42-136">This allows you to add a new repository.</span></span>  
4. <span data-ttu-id="b9e42-137">V poli Typ úložiště konfigurace vyberte LCS.</span><span class="sxs-lookup"><span data-stu-id="b9e42-137">In the Configuration repository type field, select LCS.</span></span>
5. <span data-ttu-id="b9e42-138">Klikněte na Vytvořit úložiště.</span><span class="sxs-lookup"><span data-stu-id="b9e42-138">Click Create repository.</span></span>
6. <span data-ttu-id="b9e42-139">V poli Projekt zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="b9e42-139">In the Project field, enter or select a value.</span></span>
    * <span data-ttu-id="b9e42-140">Vyberte příslušný projekt LCS.</span><span class="sxs-lookup"><span data-stu-id="b9e42-140">Select the desired LCS project.</span></span> <span data-ttu-id="b9e42-141">Musíte mít přístup k tomuto projektu.</span><span class="sxs-lookup"><span data-stu-id="b9e42-141">You must have access to the project.</span></span>  
7. <span data-ttu-id="b9e42-142">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="b9e42-142">Click OK.</span></span>
    * <span data-ttu-id="b9e42-143">Vytvořte nový záznam v úložišti.</span><span class="sxs-lookup"><span data-stu-id="b9e42-143">Complete a new repository entry.</span></span>  
8. <span data-ttu-id="b9e42-144">Označte v seznamu vybraný řádek.</span><span class="sxs-lookup"><span data-stu-id="b9e42-144">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="b9e42-145">Vybrat záznam úložiště LCS.</span><span class="sxs-lookup"><span data-stu-id="b9e42-145">Select the LCS repository record.</span></span>  
    * <span data-ttu-id="b9e42-146">Všimněte si, registrované úložiště je označeno aktuálním poskytovatelem, tj. pouze konfigurace ve vlastnictví daného poskytovatele mohou být umístěny do tohoto úložiště a následně odeslány do vybraného projektu LCS.</span><span class="sxs-lookup"><span data-stu-id="b9e42-146">Note that a registered repository is marked by the current provider meaning that the only configurations owned by that provider can be placed to this repository and, consequently, uploaded into the selected LCS project.</span></span>  
9. <span data-ttu-id="b9e42-147">Klikněte na možnost Otevřít.</span><span class="sxs-lookup"><span data-stu-id="b9e42-147">Click Open.</span></span>
    * <span data-ttu-id="b9e42-148">Otevřete úložiště a prohlédněte si seznam konfigurací ER.</span><span class="sxs-lookup"><span data-stu-id="b9e42-148">Open the repository to view the list of ER configurations.</span></span> <span data-ttu-id="b9e42-149">Bude prázdný, pokud tento projekt nebyl dosud použit pro sdílení konfigurací ER.</span><span class="sxs-lookup"><span data-stu-id="b9e42-149">It will be empty if this project has not yet been used for ER configurations sharing.</span></span>  
10. <span data-ttu-id="b9e42-150">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="b9e42-150">Close the page.</span></span>
11. <span data-ttu-id="b9e42-151">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="b9e42-151">Close the page.</span></span>

## <a name="upload-configuration-into-lcs"></a><span data-ttu-id="b9e42-152">Odeslání konfigurace do LCS</span><span class="sxs-lookup"><span data-stu-id="b9e42-152">Upload configuration into LCS</span></span>
1. <span data-ttu-id="b9e42-153">Klikněte na Konfigurace.</span><span class="sxs-lookup"><span data-stu-id="b9e42-153">Click Configurations.</span></span>
2. <span data-ttu-id="b9e42-154">Ve stromovém zobrazení vyberte možnost Vzorová konfigurace modelu.</span><span class="sxs-lookup"><span data-stu-id="b9e42-154">In the tree, select 'Sample model configuration'.</span></span>
    * <span data-ttu-id="b9e42-155">Vyberte vytvořenou konfiguraci, která již byla dokončena.</span><span class="sxs-lookup"><span data-stu-id="b9e42-155">Select a created configuration that has been already completed.</span></span>  
3. <span data-ttu-id="b9e42-156">Vyhledejte na seznamu požadovaný záznam a vyberte ho.</span><span class="sxs-lookup"><span data-stu-id="b9e42-156">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="b9e42-157">Vyberte verzi vybrané konfigurace se stavem "Dokončeno".</span><span class="sxs-lookup"><span data-stu-id="b9e42-157">Select the version of the selected configuration with the status of ‘Completed’.</span></span>  
4. <span data-ttu-id="b9e42-158">Klikněte na položku Změnit stav.</span><span class="sxs-lookup"><span data-stu-id="b9e42-158">Click Change status.</span></span>
5. <span data-ttu-id="b9e42-159">Klepněte na Sdílet.</span><span class="sxs-lookup"><span data-stu-id="b9e42-159">Click Share.</span></span>
    * <span data-ttu-id="b9e42-160">Stav konfigurace se změní z "Dokončeno" na 'Sdíleno' během publikování v LCS.</span><span class="sxs-lookup"><span data-stu-id="b9e42-160">The configuration status will change from ‘Completed’ to ‘Shared’ when it is published in LCS.</span></span>  
6. <span data-ttu-id="b9e42-161">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="b9e42-161">Click OK.</span></span>
7. <span data-ttu-id="b9e42-162">Vyhledejte na seznamu požadovaný záznam a vyberte ho.</span><span class="sxs-lookup"><span data-stu-id="b9e42-162">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="b9e42-163">Vyberte verzi konfigurace se stavem „Sdílena“.</span><span class="sxs-lookup"><span data-stu-id="b9e42-163">Select the configuration version with the status of 'Shared'.</span></span>  
    * <span data-ttu-id="b9e42-164">Všimněte si, že stav vybrané verze se změnil z "Dokončeno" na 'Sdíleno'.</span><span class="sxs-lookup"><span data-stu-id="b9e42-164">Note that the status of the selected version has changed from ‘Completed’ to ‘Shared’.</span></span>  
8. <span data-ttu-id="b9e42-165">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="b9e42-165">Close the page.</span></span>
9. <span data-ttu-id="b9e42-166">Klikněte na možnost Úložiště.</span><span class="sxs-lookup"><span data-stu-id="b9e42-166">Click Repositories.</span></span>
    * <span data-ttu-id="b9e42-167">To umožňuje otevřít seznam úložišť pro poskytovatele konfigurace Litware, Inc.</span><span class="sxs-lookup"><span data-stu-id="b9e42-167">This enables you to open the list of repositories for the Litware, Inc. configuration provider.</span></span>  
10. <span data-ttu-id="b9e42-168">Klikněte na možnost Otevřít.</span><span class="sxs-lookup"><span data-stu-id="b9e42-168">Click Open.</span></span>
    * <span data-ttu-id="b9e42-169">Vyberte úložiště LCS a otevřete je.</span><span class="sxs-lookup"><span data-stu-id="b9e42-169">Select the LCS repository and open it.</span></span>  
    * <span data-ttu-id="b9e42-170">Všimněte si, že vybraná konfigurace je uvedena jako aktiva vybraného projektu LCS.</span><span class="sxs-lookup"><span data-stu-id="b9e42-170">Note that the selected configuration is shown as an asset of the selected LCS project.</span></span>  
    * <span data-ttu-id="b9e42-171">Otevřete LCS pomocí https://lcs.dynamics.com.</span><span class="sxs-lookup"><span data-stu-id="b9e42-171">Open LCS using https://lcs.dynamics.com.</span></span> <span data-ttu-id="b9e42-172">Otevřete projekt, který byl použit dříve pro registraci úložiště, otevřete Knihovnu majetku pro tento projekt a rozbalte obsah s typem majetku Konfigurace GER – odeslané konfigurace ER budou nyní k dispozici.</span><span class="sxs-lookup"><span data-stu-id="b9e42-172">Open a project that was used earlier for repository registration, open the ‘Asset library’ of this project, and expand the content of the ‘GER configuration’ asset type – the uploaded ER configuration will be available.</span></span> <span data-ttu-id="b9e42-173">Všimněte si, že odeslané konfigurace LCS je možné importovat do jiné instance aplikace Microsoft Dynamics 365 for Finance and Operations Enterprise edition, pokud poskytovatelé mají přístupová práva k tomuto projektu LCS.</span><span class="sxs-lookup"><span data-stu-id="b9e42-173">Note that the uploaded LCS configuration can be imported to another Microsoft Dynamics 365 for Finance and Operations, Enterprise edition instance if providers have access to this LCS project.</span></span>  

