---
title: Přístup k metadatům aplikace pomocí konfigurace elektronického výkaznictví
description: Kroky v tomto tématu vysvětlují, jak může uživatel služby Regulatory Configuration Service (RCS) navrhnout nové mapování modelu elektronického výkaznictví (ER) pomocí metadat v modulu Finance and Operations.
author: NickSelin
manager: AnnBe
ms.date: 06/28/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2019-06-28
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: aa8444b081650e3d375e6f28f47866c8d4853721
ms.sourcegitcommit: fbc106af09bdadb860677f590464fb93223cbf65
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 11/06/2019
ms.locfileid: "2772456"
---
# <a name="access-application-metadata-by-using-er-configuration"></a><span data-ttu-id="29b99-103">Přístup k metadatům aplikace pomocí konfigurace elektronického výkaznictví</span><span class="sxs-lookup"><span data-stu-id="29b99-103">Access application metadata by using ER configuration</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="29b99-104">Následující kroky vysvětlují, jak může uživatel služby Regulatory Configuration Service s rolí Správce systému nebo Návrhář elektronického výkaznictví navrhnout nové mapování modelu elektronického výkaznictví (ER) pro pomocí metadat aplikace.</span><span class="sxs-lookup"><span data-stu-id="29b99-104">The following steps explain how a Regulatory configuration service (RCS) user in the System Administrator or Electronic Reporting Developer role can design a new Electronic reporting (ER) model mapping by using the application metadata.</span></span> <span data-ttu-id="29b99-105">K metadatům aplikace se přistupuje pomocí konfigurace metadat ER, která obsahuje ukázkovou sadu metadat pro přístup k transakcím zahraničního obchodu.</span><span class="sxs-lookup"><span data-stu-id="29b99-105">Application metadata will be accessed by using an ER metadata configuration that contains a sample set of metadata to access foreign trade transactions.</span></span> <span data-ttu-id="29b99-106">Provedení těchto kroků vyžaduje, abyste nejprve dokončili kroky v tématu [Vytvoření poskytovatelů konfigurace a jejich označení jako aktivních](er-configuration-provider-mark-it-active-2016-11.md).</span><span class="sxs-lookup"><span data-stu-id="29b99-106">To complete these steps, in RCS you must first complete the steps in the topic, [Create configuration providers and mark them as active](er-configuration-provider-mark-it-active-2016-11.md) procedure.</span></span> <span data-ttu-id="29b99-107">Pak proveďte kroky uvedené v tématu [Příprava použití metadat aplikace v RCS](prepare-application-metadata-rcs.md).</span><span class="sxs-lookup"><span data-stu-id="29b99-107">Then complete the steps in the topic, [Prepare application metadata to be used in RCS](prepare-application-metadata-rcs.md).</span></span>

## <a name="prerequisites"></a><span data-ttu-id="29b99-108">Předpoklady</span><span class="sxs-lookup"><span data-stu-id="29b99-108">Prerequisites</span></span>
1. <span data-ttu-id="29b99-109">Přejděte na **Všechny pracovní prostory** > **Elektronické výkaznictví**.</span><span class="sxs-lookup"><span data-stu-id="29b99-109">Go to **All workspaces** > **Electronic reporting**.</span></span> 
2. <span data-ttu-id="29b99-110">Ujistěte se, že poskytovatel konfigurace pro vzorovou společnost ‘Litware, Inc.’ je k dispozici a je označen jako **Aktivní**.</span><span class="sxs-lookup"><span data-stu-id="29b99-110">Make sure that the configuration provider for the sample company, Litware, Inc., is available and marked as **Active**.</span></span> <span data-ttu-id="29b99-111">Pokud tohoto zprostředkovatele konfigurace nevidíte, musíte nejprve dokončit jednotlivé kroky v postupu [Vytvoření poskytovatelů konfigurace a jejich označení jako aktivních](er-configuration-provider-mark-it-active-2016-11.md).</span><span class="sxs-lookup"><span data-stu-id="29b99-111">If you don’t see this configuration provider, complete the steps in the procedure [Create configuration providers and mark them as active](er-configuration-provider-mark-it-active-2016-11.md).</span></span> 

## <a name="import-metadata-configuration"></a><span data-ttu-id="29b99-112">Import konfigurace metadat</span><span class="sxs-lookup"><span data-stu-id="29b99-112">Import metadata configuration</span></span> 
1. <span data-ttu-id="29b99-113">Klikněte na **Konfigurace metadat**.</span><span class="sxs-lookup"><span data-stu-id="29b99-113">Click **Metadata configurations**.</span></span> 
2. <span data-ttu-id="29b99-114">Importujte konfiguraci metadat ER obsahující metadata, která jsou nakonfigurována pro generování elektronických dokumentů pro zahraniční obchod.</span><span class="sxs-lookup"><span data-stu-id="29b99-114">Import the ER metadata configuration that contains metadata that has been configured to generate electronic documents for foreign trade business.</span></span> <span data-ttu-id="29b99-115">Konfigurace metadat ER byla exportována jako soubor XML, zatímco byly dokončeny kroky v proceduře [Příprava metadat aplikace k použití v RCS](prepare-application-metadata-rcs.md).</span><span class="sxs-lookup"><span data-stu-id="29b99-115">This ER metadata configuration has been exported as XML file while the steps in the [Prepare application metadata to be used in RCS](prepare-application-metadata-rcs.md) procedure have been completed.</span></span> 
3. <span data-ttu-id="29b99-116">Klikněte na **Exchange**.</span><span class="sxs-lookup"><span data-stu-id="29b99-116">Click **Exchange**.</span></span> 
4. <span data-ttu-id="29b99-117">Klikněte na **Načíst ze souboru XML**.</span><span class="sxs-lookup"><span data-stu-id="29b99-117">Click **Load from XML file**.</span></span> 
5. <span data-ttu-id="29b99-118">Klikněte na **Procházet** a vyberte soubor Foreign trade metadata.xml.</span><span class="sxs-lookup"><span data-stu-id="29b99-118">Click **Browse** and select the ‘Foreign trade metadata.xml’ file.</span></span> 
6. <span data-ttu-id="29b99-119">Klikněte na tlačítko **OK**.</span><span class="sxs-lookup"><span data-stu-id="29b99-119">Click **OK**.</span></span> 
7. <span data-ttu-id="29b99-120">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="29b99-120">Close the page.</span></span> 

## <a name="create-data-model-configuration"></a><span data-ttu-id="29b99-121">Vytvoření konfigurace datového modelu</span><span class="sxs-lookup"><span data-stu-id="29b99-121">Create data model configuration</span></span>
1. <span data-ttu-id="29b99-122">Klikněte na **Konfigurace výkaznictví**.</span><span class="sxs-lookup"><span data-stu-id="29b99-122">Click **Reporting configurations**.</span></span> 
2. <span data-ttu-id="29b99-123">Kliknutím na možnost **Vytvořit konfiguraci** otevřete dialogové okno.</span><span class="sxs-lookup"><span data-stu-id="29b99-123">Click **Create configuration** to open the drop dialog.</span></span> 
3. <span data-ttu-id="29b99-124">Do pole **Název** zadejte 'Model zahraničního obchodu'.</span><span class="sxs-lookup"><span data-stu-id="29b99-124">In the **Name** field, type 'Foreign trade model'.</span></span> 
4. <span data-ttu-id="29b99-125">Klepněte na možnost **Vytvořit konfiguraci**.</span><span class="sxs-lookup"><span data-stu-id="29b99-125">Click **Create configuration**.</span></span> 
5. <span data-ttu-id="29b99-126">Klikněte na možnost **Návrhář**.</span><span class="sxs-lookup"><span data-stu-id="29b99-126">Click **Designer**.</span></span> 
6. <span data-ttu-id="29b99-127">Kliknutím na možnost **Nový** otevřete dialogové okno.</span><span class="sxs-lookup"><span data-stu-id="29b99-127">Click **New** to open the drop dialog.</span></span> 
7. <span data-ttu-id="29b99-128">Do pole **Název** zadejte Kořen.</span><span class="sxs-lookup"><span data-stu-id="29b99-128">In the **Name** field, type 'Root'.</span></span> 
8. <span data-ttu-id="29b99-129">Klikněte na tlačítko **Přidat**.</span><span class="sxs-lookup"><span data-stu-id="29b99-129">Click **Add**.</span></span> 
9. <span data-ttu-id="29b99-130">Kliknutím na možnost **Nový** otevřete dialogové okno.</span><span class="sxs-lookup"><span data-stu-id="29b99-130">Click **New** to open the drop dialog.</span></span> 
10. <span data-ttu-id="29b99-131">Do pole **Název** zadejte Transakce.</span><span class="sxs-lookup"><span data-stu-id="29b99-131">In the **Name** field, type 'Transaction'.</span></span> 
11. <span data-ttu-id="29b99-132">V poli **Typ položky** vyberte **Seznam záznamů**.</span><span class="sxs-lookup"><span data-stu-id="29b99-132">In the **Item type** field, select **Record list**.</span></span> 
12. <span data-ttu-id="29b99-133">Klikněte na tlačítko **Přidat**.</span><span class="sxs-lookup"><span data-stu-id="29b99-133">Click **Add**.</span></span> 
13. <span data-ttu-id="29b99-134">Kliknutím na možnost **Nový** otevřete dialogové okno.</span><span class="sxs-lookup"><span data-stu-id="29b99-134">Click **New** to open the drop dialog.</span></span> 
14. <span data-ttu-id="29b99-135">Do pole **Název** zadejte ID záznamu komodity.</span><span class="sxs-lookup"><span data-stu-id="29b99-135">In the **Name** field, type 'Commodity code'.</span></span> 
15. <span data-ttu-id="29b99-136">V poli **Typ položky** vyberte **Řetězec**.</span><span class="sxs-lookup"><span data-stu-id="29b99-136">In the **Item type** field, select **String**.</span></span> 
16. <span data-ttu-id="29b99-137">Klikněte na tlačítko **Přidat**.</span><span class="sxs-lookup"><span data-stu-id="29b99-137">Click **Add**.</span></span> 
17. <span data-ttu-id="29b99-138">Kliknutím na možnost **Nový** otevřete dialogové okno.</span><span class="sxs-lookup"><span data-stu-id="29b99-138">Click **New** to open the drop dialog.</span></span> 
18. <span data-ttu-id="29b99-139">Do pole **Název** zadejte Fakturovaná částka.</span><span class="sxs-lookup"><span data-stu-id="29b99-139">In the **Name** field, type 'Invoiced amount'.</span></span> 
19. <span data-ttu-id="29b99-140">V poli **Typ položky** vyberte **Reálný**.</span><span class="sxs-lookup"><span data-stu-id="29b99-140">In the **Item type** field, select **Real**.</span></span> 
20. <span data-ttu-id="29b99-141">Klikněte na tlačítko **Přidat**.</span><span class="sxs-lookup"><span data-stu-id="29b99-141">Click **Add**.</span></span> 
21. <span data-ttu-id="29b99-142">Kliknutím na možnost **Nový** otevřete dialogové okno.</span><span class="sxs-lookup"><span data-stu-id="29b99-142">Click **New** to open the drop dialog.</span></span> 
22. <span data-ttu-id="29b99-143">Do pole **Název** zadejte Datum.</span><span class="sxs-lookup"><span data-stu-id="29b99-143">In the **Name** field, type 'Date'.</span></span> 
23. <span data-ttu-id="29b99-144">V poli **Typ položky** vyberte **Datum**.</span><span class="sxs-lookup"><span data-stu-id="29b99-144">In the **Item type** field, select **Date**.</span></span> 
24. <span data-ttu-id="29b99-145">Klikněte na tlačítko **Přidat**.</span><span class="sxs-lookup"><span data-stu-id="29b99-145">Click **Add**.</span></span> 
25. <span data-ttu-id="29b99-146">Klikněte na **Kořenový odkaz**.</span><span class="sxs-lookup"><span data-stu-id="29b99-146">Click **Root reference**.</span></span> 
26. <span data-ttu-id="29b99-147">Klikněte na tlačítko **OK**.</span><span class="sxs-lookup"><span data-stu-id="29b99-147">Click **OK**.</span></span> 
27. <span data-ttu-id="29b99-148">Klikněte na možnost **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="29b99-148">Click **Save**.</span></span> 
28. <span data-ttu-id="29b99-149">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="29b99-149">Close the page.</span></span> 
29. <span data-ttu-id="29b99-150">Klikněte na položku **Změnit stav**.</span><span class="sxs-lookup"><span data-stu-id="29b99-150">Click **Change status**.</span></span> 
30. <span data-ttu-id="29b99-151">Klikněte na **Dokončit**.</span><span class="sxs-lookup"><span data-stu-id="29b99-151">Click **Complete**.</span></span> 
31. <span data-ttu-id="29b99-152">Klikněte na tlačítko **OK**.</span><span class="sxs-lookup"><span data-stu-id="29b99-152">Click **OK**.</span></span> 

## <a name="create-model-mapping-configuration"></a><span data-ttu-id="29b99-153">Vytvoření konfigurace mapování modelu</span><span class="sxs-lookup"><span data-stu-id="29b99-153">Create model mapping configuration</span></span> 
1. <span data-ttu-id="29b99-154">Kliknutím na možnost **Vytvořit konfiguraci** otevřete dialogové okno.</span><span class="sxs-lookup"><span data-stu-id="29b99-154">Click **Create configuration** to open the drop dialog.</span></span> 
2. <span data-ttu-id="29b99-155">V poli **Nový** zadejte Mapování modelu založené na datovém modelu Model zahraničního obchodu.</span><span class="sxs-lookup"><span data-stu-id="29b99-155">In the **New** field, enter 'Model Mapping based on data model Foreign trade model'.</span></span> 
3. <span data-ttu-id="29b99-156">Do pole **Název** zadejte 'Mapování zahraničního obchodu'.</span><span class="sxs-lookup"><span data-stu-id="29b99-156">In the **Name** field, type 'Foreign trade mapping'.</span></span> 
4. <span data-ttu-id="29b99-157">Klepněte na možnost **Vytvořit konfiguraci**.</span><span class="sxs-lookup"><span data-stu-id="29b99-157">Click **Create configuration**.</span></span> 
5. <span data-ttu-id="29b99-158">Rozbalte oddíl **Předpoklady**.</span><span class="sxs-lookup"><span data-stu-id="29b99-158">Expand the **Prerequisites** section.</span></span> 
6. <span data-ttu-id="29b99-159">Klikněte na možnost **Upravit**.</span><span class="sxs-lookup"><span data-stu-id="29b99-159">Click **Edit**.</span></span> 
7. <span data-ttu-id="29b99-160">Klepněte na možnost **Nový**.</span><span class="sxs-lookup"><span data-stu-id="29b99-160">Click **New**.</span></span> 
8. <span data-ttu-id="29b99-161">Označte na seznamu vybraný řádek.</span><span class="sxs-lookup"><span data-stu-id="29b99-161">In the list, mark the selected row.</span></span> 
9. <span data-ttu-id="29b99-162">V poli **Typ komponenty předpokladu** vyberte **Konfigurace**.</span><span class="sxs-lookup"><span data-stu-id="29b99-162">In the **Prerequisite component type** field, select **Configuration**.</span></span> 
10. <span data-ttu-id="29b99-163">Vyberte konfiguraci **Metadata zahraničního obchodu**.</span><span class="sxs-lookup"><span data-stu-id="29b99-163">Select **Foreign trade metadata** configuration.</span></span> 
11. <span data-ttu-id="29b99-164">Klikněte na možnost **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="29b99-164">Click **Save**.</span></span> 
12. <span data-ttu-id="29b99-165">Přidali jsme odkaz na verzi 1 konfigurace Metadata zahraničního obchodu.</span><span class="sxs-lookup"><span data-stu-id="29b99-165">We added the reference to the version 1 of the ‘Foreign trade metadata’ configuration.</span></span> <span data-ttu-id="29b99-166">Metadata aplikace z této konfigurace budou nabízena, dokud nebude toto mapování modelu navrženo.</span><span class="sxs-lookup"><span data-stu-id="29b99-166">Application metadata from this configuration will be offered while this model mapping will be designed.</span></span> 
13. <span data-ttu-id="29b99-167">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="29b99-167">Close the page.</span></span> 
14. <span data-ttu-id="29b99-168">Klikněte na možnost **Návrhář**.</span><span class="sxs-lookup"><span data-stu-id="29b99-168">Click **Designer**.</span></span> 
15. <span data-ttu-id="29b99-169">Klikněte na možnost **Návrhář**.</span><span class="sxs-lookup"><span data-stu-id="29b99-169">Click **Designer**.</span></span> 
16. <span data-ttu-id="29b99-170">Ve stromovém zobrazení vyberte možnost **Dynamics 365 for Operations\Table records**.</span><span class="sxs-lookup"><span data-stu-id="29b99-170">In the tree, select **Dynamics 365 for Operations\Table records**.</span></span> 
17. <span data-ttu-id="29b99-171">Klikněte na možnost **Přidat kořen**.</span><span class="sxs-lookup"><span data-stu-id="29b99-171">Click **Add root**.</span></span> 
18. <span data-ttu-id="29b99-172">Do pole **Název** zadejte Intrastat.</span><span class="sxs-lookup"><span data-stu-id="29b99-172">In the **Name** field, type 'Intrastat'.</span></span> 
19. <span data-ttu-id="29b99-173">Vyberte záznamy tabulky **Intrastat**.</span><span class="sxs-lookup"><span data-stu-id="29b99-173">Select **Intrastat** table records.</span></span> 
20. <span data-ttu-id="29b99-174">Klikněte na tlačítko **OK**.</span><span class="sxs-lookup"><span data-stu-id="29b99-174">Click **OK**.</span></span> 

> [!NOTE]
> <span data-ttu-id="29b99-175">Byly nabídnuty pouze dvě tabulky, protože do sady metadat, která je právě používána, byly přidány pouze dvě tabulky.</span><span class="sxs-lookup"><span data-stu-id="29b99-175">The only 2 tables were offered as the only 2 tables were added into the set of metadata which is currently in use.</span></span> 

21. <span data-ttu-id="29b99-176">Klikněte na **Vazba**.</span><span class="sxs-lookup"><span data-stu-id="29b99-176">Click **Bind**.</span></span> 
22. <span data-ttu-id="29b99-177">Ve stromu rozbalte **Intrastat**.</span><span class="sxs-lookup"><span data-stu-id="29b99-177">In the tree, expand **Intrastat**.</span></span> 
23. <span data-ttu-id="29b99-178">Ve stromovém zobrazení vyberte **Intrastat\AmountMST**.</span><span class="sxs-lookup"><span data-stu-id="29b99-178">In the tree, select **Intrastat\AmountMST**.</span></span> 
24. <span data-ttu-id="29b99-179">Ve stromovém zobrazení rozbalte **Transakce = Intrastat**.</span><span class="sxs-lookup"><span data-stu-id="29b99-179">In the tree, expand **Transaction = Intrastat**.</span></span> 
25. <span data-ttu-id="29b99-180">Ve stromovém zobrazení vyberte možnost **Transaction = Intrastat\Invoiced amount**.</span><span class="sxs-lookup"><span data-stu-id="29b99-180">In the tree, select **Transaction = Intrastat\Invoiced amount**.</span></span> 
26. <span data-ttu-id="29b99-181">Klikněte na **Vazba**.</span><span class="sxs-lookup"><span data-stu-id="29b99-181">Click **Bind**.</span></span> 
27. <span data-ttu-id="29b99-182">Ve stromovém zobrazení vyberte **Intrastat\TransDate**.</span><span class="sxs-lookup"><span data-stu-id="29b99-182">In the tree, select **Intrastat\TransDate**.</span></span> 
28. <span data-ttu-id="29b99-183">Ve stromovém zobrazení vyberte **Transakce = Intrastat\Date**.</span><span class="sxs-lookup"><span data-stu-id="29b99-183">In the tree, select **Transaction = Intrastat\Date**.</span></span> 
29. <span data-ttu-id="29b99-184">Klikněte na **Vazba**.</span><span class="sxs-lookup"><span data-stu-id="29b99-184">Click **Bind**.</span></span> 
30. <span data-ttu-id="29b99-185">Ve stromovém zobrazení rozbalte **Intrastat\>Relations**.</span><span class="sxs-lookup"><span data-stu-id="29b99-185">In the tree, expand **Intrastat\>Relations**.</span></span> 
31. <span data-ttu-id="29b99-186">Ve stromovém zobrazení rozbalte **Intrastat\>Relations\IntrastatCommodity**.</span><span class="sxs-lookup"><span data-stu-id="29b99-186">In the tree, expand **Intrastat\>Relations\IntrastatCommodity**.</span></span> 
32. <span data-ttu-id="29b99-187">Ve stromovém zobrazení vyberte **Intrastat\>Relations\IntrastatCommodity\Code**.</span><span class="sxs-lookup"><span data-stu-id="29b99-187">In the tree, select **Intrastat\>Relations\IntrastatCommodity\Code**.</span></span> 
33. <span data-ttu-id="29b99-188">Ve stromovém zobrazení vyberte **Transaction = Intrastat\Commodity code**.</span><span class="sxs-lookup"><span data-stu-id="29b99-188">In the tree, select **Transaction = Intrastat\Commodity code**.</span></span> 
34. <span data-ttu-id="29b99-189">Klikněte na **Vazba**.</span><span class="sxs-lookup"><span data-stu-id="29b99-189">Click **Bind**.</span></span> 
35. <span data-ttu-id="29b99-190">Klikněte na tlačítko **Ověřit**.</span><span class="sxs-lookup"><span data-stu-id="29b99-190">Click **Validate**.</span></span> 

> [!NOTE]
> <span data-ttu-id="29b99-191">Úspěšně jsme provedli vázání prvků datového modelu s položkami datových zdrojů, které jsou popsány pomocí podrobností metadat aplikace z odkazované konfigurace metadat ER.</span><span class="sxs-lookup"><span data-stu-id="29b99-191">We have successfully bound elements of data model with items of data sources that are described by using details of application metadata from the referred ER metadata configuration.</span></span> 
36. <span data-ttu-id="29b99-192">Klikněte na možnost **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="29b99-192">Click **Save**.</span></span> 
37. <span data-ttu-id="29b99-193">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="29b99-193">Close the page.</span></span> 
38. <span data-ttu-id="29b99-194">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="29b99-194">Close the page.</span></span> 
39. <span data-ttu-id="29b99-195">V případě potřeby můžete rozšířit stávající sadu metadat a poté exportovat novou dokončenou verzi konfigurace metadat ER.</span><span class="sxs-lookup"><span data-stu-id="29b99-195">When needed, you can extend the existing set of metadata and then export the new completed version of ER metadata configuration.</span></span> <span data-ttu-id="29b99-196">Poté ji můžete importovat do RCS a aktualizovat předpoklady konfigurace mapování konfigurovaných modelů odkazující na novou verzi importované konfigurace metadat.</span><span class="sxs-lookup"><span data-stu-id="29b99-196">You can then import it to RCS, and update the prerequisites of the configured model mapping configuration referring to a new version of imported metadata configuration.</span></span> 

> [!NOTE]
> <span data-ttu-id="29b99-197">Tento způsob získání informací o metadatech aplikace je jediný dostupný pro lokálně nasazené aplikace (v případě místních obchodních dat (LBD) nebo místně se používá model nasazení).</span><span class="sxs-lookup"><span data-stu-id="29b99-197">This way of getting information about application metadata is the only one available for locally deployed applications (when local business data (LBD), or on-premises, deployment model is used).</span></span>
        
