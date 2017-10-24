--- 
title: "Odeslání konfigurace do služby Lifecycle Services pro elektronické výkaznictví (ER)"
description: "Následující postup popisuje, jak uživatel s rolí Správce systému nebo Návrhář elektronického výkaznictví může vytvořit novou konfiguraci formátu pro elektronické výkaznictví a odeslat ji do služby Microsoft Lifecycle Services (LCS)."
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
ms.sourcegitcommit: f827b4787506cfdec8b9a91c4a68f3293190158a
ms.openlocfilehash: d24679a380ec824fe08c56aacb4bc348ff40440a
ms.contentlocale: cs-cz
ms.lasthandoff: 09/29/2017

---
# <a name="upload-a-configuration-into-lifecycle-services-for-electronic-reporting-er"></a><span data-ttu-id="3a3a3-103">Odeslání konfigurace do služby Lifecycle Services pro elektronické výkaznictví (ER)</span><span class="sxs-lookup"><span data-stu-id="3a3a3-103">Upload a configuration into Lifecycle Services for electronic reporting (ER)</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="3a3a3-104">Následující postup popisuje, jak uživatel s rolí Správce systému nebo Návrhář elektronického výkaznictví může vytvořit novou konfiguraci formátu pro elektronické výkaznictví a odeslat ji do služby Microsoft Lifecycle Services (LCS).</span><span class="sxs-lookup"><span data-stu-id="3a3a3-104">The following steps explain how a user in the System Administrator or Electronic Reporting Developer role can create a new Electronic reporting (ER) configuration and upload it into Microsoft Lifecycle Services (LCS).</span></span>

<span data-ttu-id="3a3a3-105">V tomto příkladu vytvoříte konfiguraci pro vzorovou společnost Litware, Inc a odešlete ji do LCS. Tyto kroky lze provést v kterékoli společnosti, protože konfigurace ER se sdílí mezi společnostmi.</span><span class="sxs-lookup"><span data-stu-id="3a3a3-105">In this example, you will create a configuration and upload it to LCS for sample company, Litware, Inc. These steps can be performed in any company as ER configurations are shared among companies.</span></span> <span data-ttu-id="3a3a3-106">K provedení těchto kroků musíte nejprve dokončit jednotlivé kroky v postupu "Vytvoření poskytovatele konfigurace a jeho označení jako aktivního".</span><span class="sxs-lookup"><span data-stu-id="3a3a3-106">To complete these steps, you must first complete the steps in the “Create a configuration provider and mark it as active” procedure.</span></span> <span data-ttu-id="3a3a3-107">K dokončení tohoto postupu je nutný také přístup k LCS.</span><span class="sxs-lookup"><span data-stu-id="3a3a3-107">Access to LCS is also required for completion of these steps.</span></span>

1. <span data-ttu-id="3a3a3-108">Přejděte do části Správa organizace > Pracovní prostory > Elektronické výkaznictví.</span><span class="sxs-lookup"><span data-stu-id="3a3a3-108">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
2. <span data-ttu-id="3a3a3-109">Vyberte Litware, Inc.</span><span class="sxs-lookup"><span data-stu-id="3a3a3-109">Select ‘Litware, Inc.’</span></span> <span data-ttu-id="3a3a3-110">a nastavte ji jako aktivní.</span><span class="sxs-lookup"><span data-stu-id="3a3a3-110">and set it as active.</span></span>
3. <span data-ttu-id="3a3a3-111">Klikněte na Konfigurace.</span><span class="sxs-lookup"><span data-stu-id="3a3a3-111">Click Configurations.</span></span>

## <a name="create-a-new-data-model-configuration"></a><span data-ttu-id="3a3a3-112">Vytvoření nové konfigurace datového modelu</span><span class="sxs-lookup"><span data-stu-id="3a3a3-112">Create a new data model configuration</span></span>
1. <span data-ttu-id="3a3a3-113">Kliknutím na možnost Vytvořit konfiguraci otevřete dialogové okno.</span><span class="sxs-lookup"><span data-stu-id="3a3a3-113">Click Create configuration to open the drop dialog.</span></span>
    * <span data-ttu-id="3a3a3-114">Vytvoříte konfiguraci, která obsahuje vzorový model dat pro elektronické doklady.</span><span class="sxs-lookup"><span data-stu-id="3a3a3-114">You will create a configuration that contains a sample data model for electronic documents.</span></span> <span data-ttu-id="3a3a3-115">Tato konfigurace modelu dat bude odeslána do LCS později.</span><span class="sxs-lookup"><span data-stu-id="3a3a3-115">This data model configuration will be uploaded into LCS later.</span></span>  
2. <span data-ttu-id="3a3a3-116">V poli Název zadejte Vzorová konfigurace modelu.</span><span class="sxs-lookup"><span data-stu-id="3a3a3-116">In the Name field, type 'Sample model configuration'.</span></span>
    * <span data-ttu-id="3a3a3-117">Vzorová konfigurace modelu</span><span class="sxs-lookup"><span data-stu-id="3a3a3-117">Sample model configuration</span></span>  
3. <span data-ttu-id="3a3a3-118">V poli Popis zadejte „Vzorová konfigurace modelu“.</span><span class="sxs-lookup"><span data-stu-id="3a3a3-118">In the Description field, type 'Sample model configuration'.</span></span>
    * <span data-ttu-id="3a3a3-119">Vzorová konfigurace modelu</span><span class="sxs-lookup"><span data-stu-id="3a3a3-119">Sample model configuration</span></span>  
4. <span data-ttu-id="3a3a3-120">Klepněte na možnost Vytvořit konfiguraci.</span><span class="sxs-lookup"><span data-stu-id="3a3a3-120">Click Create configuration.</span></span>
5. <span data-ttu-id="3a3a3-121">Klikněte na Návrhář modelů.</span><span class="sxs-lookup"><span data-stu-id="3a3a3-121">Click Model designer.</span></span>
6. <span data-ttu-id="3a3a3-122">Klikněte na položku Nová.</span><span class="sxs-lookup"><span data-stu-id="3a3a3-122">Click New.</span></span>
7. <span data-ttu-id="3a3a3-123">Do pole Název zadejte Vstupní bod.</span><span class="sxs-lookup"><span data-stu-id="3a3a3-123">In the Name field, type 'Entry point'.</span></span>
    * <span data-ttu-id="3a3a3-124">Vstupní bod</span><span class="sxs-lookup"><span data-stu-id="3a3a3-124">Entry point</span></span>  
8. <span data-ttu-id="3a3a3-125">Klepněte na možnost Přidat.</span><span class="sxs-lookup"><span data-stu-id="3a3a3-125">Click Add.</span></span>
9. <span data-ttu-id="3a3a3-126">Klikněte na položku Uložit.</span><span class="sxs-lookup"><span data-stu-id="3a3a3-126">Click Save.</span></span>
10. <span data-ttu-id="3a3a3-127">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="3a3a3-127">Close the page.</span></span>
11. <span data-ttu-id="3a3a3-128">Klikněte na položku Změnit stav.</span><span class="sxs-lookup"><span data-stu-id="3a3a3-128">Click Change status.</span></span>
12. <span data-ttu-id="3a3a3-129">Klikněte na tlačítko Dokončit.</span><span class="sxs-lookup"><span data-stu-id="3a3a3-129">Click Complete.</span></span>
13. <span data-ttu-id="3a3a3-130">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="3a3a3-130">Click OK.</span></span>

## <a name="register-a-new--repository"></a><span data-ttu-id="3a3a3-131">Registrace nového úložiště</span><span class="sxs-lookup"><span data-stu-id="3a3a3-131">Register a new  repository</span></span>
1. <span data-ttu-id="3a3a3-132">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="3a3a3-132">Close the page.</span></span>
2. <span data-ttu-id="3a3a3-133">Klikněte na možnost Úložiště.</span><span class="sxs-lookup"><span data-stu-id="3a3a3-133">Click Repositories.</span></span>
    * <span data-ttu-id="3a3a3-134">To umožňuje otevřít seznam úložišť pro poskytovatele konfigurace Litware, Inc.</span><span class="sxs-lookup"><span data-stu-id="3a3a3-134">This enables you to open the list of repositories for the Litware, Inc. configuration provider.</span></span>  
3. <span data-ttu-id="3a3a3-135">Klepnutím na možnost Přidat otevřete dialogové okno.</span><span class="sxs-lookup"><span data-stu-id="3a3a3-135">Click Add to open the drop dialog.</span></span>
    * <span data-ttu-id="3a3a3-136">Tímto způsobem můžete přidat nové úložiště.</span><span class="sxs-lookup"><span data-stu-id="3a3a3-136">This allows you to add a new repository.</span></span>  
4. <span data-ttu-id="3a3a3-137">V poli Typ úložiště konfigurace vyberte LCS.</span><span class="sxs-lookup"><span data-stu-id="3a3a3-137">In the Configuration repository type field, select LCS.</span></span>
5. <span data-ttu-id="3a3a3-138">Klikněte na Vytvořit úložiště.</span><span class="sxs-lookup"><span data-stu-id="3a3a3-138">Click Create repository.</span></span>
6. <span data-ttu-id="3a3a3-139">V poli Projekt zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="3a3a3-139">In the Project field, enter or select a value.</span></span>
    * <span data-ttu-id="3a3a3-140">Vyberte příslušný projekt LCS.</span><span class="sxs-lookup"><span data-stu-id="3a3a3-140">Select the desired LCS project.</span></span> <span data-ttu-id="3a3a3-141">Musíte mít přístup k tomuto projektu.</span><span class="sxs-lookup"><span data-stu-id="3a3a3-141">You must have access to the project.</span></span>  
7. <span data-ttu-id="3a3a3-142">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="3a3a3-142">Click OK.</span></span>
    * <span data-ttu-id="3a3a3-143">Vytvořte nový záznam v úložišti.</span><span class="sxs-lookup"><span data-stu-id="3a3a3-143">Complete a new repository entry.</span></span>  
8. <span data-ttu-id="3a3a3-144">Označte v seznamu vybraný řádek.</span><span class="sxs-lookup"><span data-stu-id="3a3a3-144">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="3a3a3-145">Vybrat záznam úložiště LCS.</span><span class="sxs-lookup"><span data-stu-id="3a3a3-145">Select the LCS repository record.</span></span>  
    * <span data-ttu-id="3a3a3-146">Všimněte si, registrované úložiště je označeno aktuálním poskytovatelem, tj. pouze konfigurace ve vlastnictví daného poskytovatele mohou být umístěny do tohoto úložiště a následně odeslány do vybraného projektu LCS.</span><span class="sxs-lookup"><span data-stu-id="3a3a3-146">Note that a registered repository is marked by the current provider meaning that the only configurations owned by that provider can be placed to this repository and, consequently, uploaded into the selected LCS project.</span></span>  
9. <span data-ttu-id="3a3a3-147">Klikněte na možnost Otevřít.</span><span class="sxs-lookup"><span data-stu-id="3a3a3-147">Click Open.</span></span>
    * <span data-ttu-id="3a3a3-148">Otevřete úložiště a prohlédněte si seznam konfigurací ER.</span><span class="sxs-lookup"><span data-stu-id="3a3a3-148">Open the repository to view the list of ER configurations.</span></span> <span data-ttu-id="3a3a3-149">Bude prázdný, pokud tento projekt nebyl dosud použit pro sdílení konfigurací ER.</span><span class="sxs-lookup"><span data-stu-id="3a3a3-149">It will be empty if this project has not yet been used for ER configurations sharing.</span></span>  
10. <span data-ttu-id="3a3a3-150">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="3a3a3-150">Close the page.</span></span>
11. <span data-ttu-id="3a3a3-151">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="3a3a3-151">Close the page.</span></span>

## <a name="upload-configuration-into-lcs"></a><span data-ttu-id="3a3a3-152">Odeslání konfigurace do LCS</span><span class="sxs-lookup"><span data-stu-id="3a3a3-152">Upload configuration into LCS</span></span>
1. <span data-ttu-id="3a3a3-153">Klikněte na Konfigurace.</span><span class="sxs-lookup"><span data-stu-id="3a3a3-153">Click Configurations.</span></span>
2. <span data-ttu-id="3a3a3-154">Ve stromovém zobrazení vyberte možnost Vzorová konfigurace modelu.</span><span class="sxs-lookup"><span data-stu-id="3a3a3-154">In the tree, select 'Sample model configuration'.</span></span>
    * <span data-ttu-id="3a3a3-155">Vyberte vytvořenou konfiguraci, která již byla dokončena.</span><span class="sxs-lookup"><span data-stu-id="3a3a3-155">Select a created configuration that has been already completed.</span></span>  
3. <span data-ttu-id="3a3a3-156">Vyhledejte na seznamu požadovaný záznam a vyberte ho.</span><span class="sxs-lookup"><span data-stu-id="3a3a3-156">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="3a3a3-157">Vyberte verzi vybrané konfigurace se stavem "Dokončeno".</span><span class="sxs-lookup"><span data-stu-id="3a3a3-157">Select the version of the selected configuration with the status of ‘Completed’.</span></span>  
4. <span data-ttu-id="3a3a3-158">Klikněte na položku Změnit stav.</span><span class="sxs-lookup"><span data-stu-id="3a3a3-158">Click Change status.</span></span>
5. <span data-ttu-id="3a3a3-159">Klepněte na Sdílet.</span><span class="sxs-lookup"><span data-stu-id="3a3a3-159">Click Share.</span></span>
    * <span data-ttu-id="3a3a3-160">Stav konfigurace se změní z "Dokončeno" na 'Sdíleno' během publikování v LCS.</span><span class="sxs-lookup"><span data-stu-id="3a3a3-160">The configuration status will change from ‘Completed’ to ‘Shared’ when it is published in LCS.</span></span>  
6. <span data-ttu-id="3a3a3-161">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="3a3a3-161">Click OK.</span></span>
7. <span data-ttu-id="3a3a3-162">Vyhledejte na seznamu požadovaný záznam a vyberte ho.</span><span class="sxs-lookup"><span data-stu-id="3a3a3-162">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="3a3a3-163">Vyberte verzi konfigurace se stavem „Sdílena“.</span><span class="sxs-lookup"><span data-stu-id="3a3a3-163">Select the configuration version with the status of 'Shared'.</span></span>  
    * <span data-ttu-id="3a3a3-164">Všimněte si, že stav vybrané verze se změnil z "Dokončeno" na 'Sdíleno'.</span><span class="sxs-lookup"><span data-stu-id="3a3a3-164">Note that the status of the selected version has changed from ‘Completed’ to ‘Shared’.</span></span>  
8. <span data-ttu-id="3a3a3-165">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="3a3a3-165">Close the page.</span></span>
9. <span data-ttu-id="3a3a3-166">Klikněte na možnost Úložiště.</span><span class="sxs-lookup"><span data-stu-id="3a3a3-166">Click Repositories.</span></span>
    * <span data-ttu-id="3a3a3-167">To umožňuje otevřít seznam úložišť pro poskytovatele konfigurace Litware, Inc.</span><span class="sxs-lookup"><span data-stu-id="3a3a3-167">This enables you to open the list of repositories for the Litware, Inc. configuration provider.</span></span>  
10. <span data-ttu-id="3a3a3-168">Klikněte na možnost Otevřít.</span><span class="sxs-lookup"><span data-stu-id="3a3a3-168">Click Open.</span></span>
    * <span data-ttu-id="3a3a3-169">Vyberte úložiště LCS a otevřete je.</span><span class="sxs-lookup"><span data-stu-id="3a3a3-169">Select the LCS repository and open it.</span></span>  
    * <span data-ttu-id="3a3a3-170">Všimněte si, že vybraná konfigurace je uvedena jako aktiva vybraného projektu LCS.</span><span class="sxs-lookup"><span data-stu-id="3a3a3-170">Note that the selected configuration is shown as an asset of the selected LCS project.</span></span>  
    * <span data-ttu-id="3a3a3-171">Otevřete LCS pomocí https://lcs.dynamics.com. Otevřete projekt, který byl použit dříve pro registraci úložiště, otevřete Knihovnu majetku pro tento projekt a rozbalte obsah s typem majetku Konfigurace GER – odeslané konfigurace ER budou nyní k dispozici.</span><span class="sxs-lookup"><span data-stu-id="3a3a3-171">Open LCS using https://lcs.dynamics.com. Open a project that was used earlier for repository registration, open the ‘Asset library’ of this project, and expand the content of the ‘GER configuration’ asset type – the uploaded ER configuration will be available.</span></span> <span data-ttu-id="3a3a3-172">Všimněte si, že odeslané konfigurace LCS je možné importovat do jiné instance aplikace Microsoft Dynamics365 for Finance and Operations, edice Enterprise, pokud poskytovatelé mají přístupová práva k tomuto projektu LCS.</span><span class="sxs-lookup"><span data-stu-id="3a3a3-172">Note that the uploaded LCS configuration can be imported to another Microsoft Dynamics 365 for Finance and Operations, Enterprise edition instance if providers have access to this LCS project.</span></span>  


