---
title: Příprava metadat specifických pro aplikaci pro RCS a ER
description: V tomto tématu je vysvětleno, jak připravit metadata specifická pro aplikaci pro službu Regulatory Configuration Service (RCS) a elektronické výkaznictví (ER).
author: NickSelin
manager: AnnBe
ms.date: 04/04/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ERWorkspace
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: global
ms.author: nselin
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: 89d36c305bc9210f7906cd4288e33e5028baecdb
ms.sourcegitcommit: fbc106af09bdadb860677f590464fb93223cbf65
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 11/06/2019
ms.locfileid: "2771253"
---
# <a name="prepare-application-specific-metadata-for-rcs-and-er"></a><span data-ttu-id="25f3a-103">Příprava metadat specifických pro aplikaci pro RCS a ER</span><span class="sxs-lookup"><span data-stu-id="25f3a-103">Prepare application-specific metadata for RCS and ER</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="25f3a-104">V tomto tématu jsou uvedeny příklady následujících úloh:</span><span class="sxs-lookup"><span data-stu-id="25f3a-104">This topic walks you through examples of the following tasks:</span></span>

- [<span data-ttu-id="25f3a-105">Příprava metadat aplikace k použití v RCS</span><span class="sxs-lookup"><span data-stu-id="25f3a-105">Prepare application metadata that can be used in RCS</span></span>](#prepare-application-metadata-that-can-be-used-in-rcs)
- [<span data-ttu-id="25f3a-106">Přístup k metadatům aplikace pomocí konfigurace elektronického výkaznictví</span><span class="sxs-lookup"><span data-stu-id="25f3a-106">Access application metadata by using an ER configuration</span></span>](#access-application-metadata-by-using-an-er-configuration)
- [<span data-ttu-id="25f3a-107">Přístup k metadatům aplikace pomocí připojených aplikací</span><span class="sxs-lookup"><span data-stu-id="25f3a-107">Access application metadata by using connected applications</span></span>](#access-application-metadata-by-using-connected-applications)

## <a name="prepare-application-metadata-that-can-be-used-in-rcs"></a><span data-ttu-id="25f3a-108">Příprava metadat aplikace k použití v RCS</span><span class="sxs-lookup"><span data-stu-id="25f3a-108">Prepare application metadata that can be used in RCS</span></span>

<span data-ttu-id="25f3a-109">V následujícím postupu je ukázáno, jak může uživatel, který má oprávnění **Správce systému** nebo **Vývojář elektronického výkaznictví** vytvořit konfiguraci elektronického výkaznictví (ER) obsahující metadata pro aplikaci , která se používá k návrhu konfigurací mapování modelu ER v rámci služby Regulatory Configuration Service (RCS).</span><span class="sxs-lookup"><span data-stu-id="25f3a-109">The following procedure shows how a user who has the **System Administrator** or **Electronic Reporting Developer** role can create an Electronic reporting (ER) configuration that contains metadata for the application, and that is used to design ER model mapping configurations in Regulatory configuration service (RCS).</span></span> <span data-ttu-id="25f3a-110">Ukázková konfigurace mapování modelu ER vytvořená v tomto příkladu bude použita pro přístup k transakcím zahraničního obchodu.</span><span class="sxs-lookup"><span data-stu-id="25f3a-110">The sample ER model mapping configuration that is created in this example will be used to access foreign trade transactions.</span></span>

<span data-ttu-id="25f3a-111">V tomto příkladu chcete použít RCS pro návrh řešení ER pro aplikaci, které bude použito k vygenerování elektronických dokumentů, které obsahují informace z cizí obchodní domény.</span><span class="sxs-lookup"><span data-stu-id="25f3a-111">For this example, you want to use RCS to design an ER solution for the application that will be used to generate electronic documents that contain information from the foreign trade business domain.</span></span> <span data-ttu-id="25f3a-112">Chcete-li určit mapování mezi datovým modelem ER a zdroji požadovaných dat, musíte mít přístup k metadatům aplikace v RCS.</span><span class="sxs-lookup"><span data-stu-id="25f3a-112">To specify the mapping between the ER data model and the sources of required data, you must have access to application metadata in RCS.</span></span> <span data-ttu-id="25f3a-113">Proto je v rámci procesu navrhování řešení ER nutné nakonfigurovat novou konfiguraci metadat ER, která obsahuje všechna metadata aktuálně požadovaná k vygenerování sestav ER pro vybranou obchodní doménu.</span><span class="sxs-lookup"><span data-stu-id="25f3a-113">Therefore, as part of the process of designing the ER solution, you must configure a new ER metadata configuration that contains all the metadata that is currently required in order to generate ER reports for the selected business domain.</span></span>

> [!NOTE]
> <span data-ttu-id="25f3a-114">V tomto příkladu vytvoříte konfiguraci pro vzorovou společnost Litware, Inc. Tyto kroky lze provést v libovolné společnosti.</span><span class="sxs-lookup"><span data-stu-id="25f3a-114">In this example, you will create a configuration for the sample company, Litware, Inc. These steps can be performed in any company.</span></span>

1. <span data-ttu-id="25f3a-115">Přejděte do části **Správa organizace \> Pracovní prostory \> Elektronické výkaznictví**.</span><span class="sxs-lookup"><span data-stu-id="25f3a-115">Go to **Organization administration \> Workspaces \> Electronic reporting**.</span></span>
2. <span data-ttu-id="25f3a-116">Ujistěte se, že poskytovatel konfigurace pro vzorovou společnost ‘Litware, Inc.’ je k dispozici a je označen jako **Aktivní**.</span><span class="sxs-lookup"><span data-stu-id="25f3a-116">Make sure that the configuration provider for the sample company, Litware, Inc., is available and marked as **Active**.</span></span> <span data-ttu-id="25f3a-117">Pokud tohoto zprostředkovatele konfigurace nevidíte, musíte nejprve dokončit jednotlivé kroky v postupu [Vytvoření zprostředkovatelů konfigurace a jejich označení jako aktivních](tasks/er-configuration-provider-mark-it-active-2016-11.md).</span><span class="sxs-lookup"><span data-stu-id="25f3a-117">If you don't see this configuration provider, complete the [Create configuration providers and mark them as active](tasks/er-configuration-provider-mark-it-active-2016-11.md) procedure.</span></span> 
3. <span data-ttu-id="25f3a-118">Vyberte **Konfigurace metadat**.</span><span class="sxs-lookup"><span data-stu-id="25f3a-118">Select **Metadata configurations**.</span></span>
4. <span data-ttu-id="25f3a-119">Vyberte **Vytvořit konfiguraci**.</span><span class="sxs-lookup"><span data-stu-id="25f3a-119">Select **Create configuration**.</span></span>
5. <span data-ttu-id="25f3a-120">V rozevíracím dialogovém okně do pole **Název** zadejte název.</span><span class="sxs-lookup"><span data-stu-id="25f3a-120">In the drop-down dialog box, in the **Name** field, enter a name.</span></span> <span data-ttu-id="25f3a-121">V tomto příkladu zadejte **metadata zahraničního obchodu**.</span><span class="sxs-lookup"><span data-stu-id="25f3a-121">For this example, enter **Foreign trade metadata**.</span></span>
6. <span data-ttu-id="25f3a-122">Vyberte **Vytvořit konfiguraci**.</span><span class="sxs-lookup"><span data-stu-id="25f3a-122">Select **Create configuration**.</span></span>
7. <span data-ttu-id="25f3a-123">Vyberte možnost **Návrhář**.</span><span class="sxs-lookup"><span data-stu-id="25f3a-123">Select **Designer**.</span></span>
8. <span data-ttu-id="25f3a-124">Vyberte **přidat**.</span><span class="sxs-lookup"><span data-stu-id="25f3a-124">Select **Add**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="25f3a-125">Můžete vybrat všechna metadata buď pro celou aplikaci, nebo pro vybrané modely nebo moduly.</span><span class="sxs-lookup"><span data-stu-id="25f3a-125">You can select all metadata either for the whole application, or for selected models or modules.</span></span> <span data-ttu-id="25f3a-126">V obou případech je třeba mít na paměti, že následující metadata budou automaticky přidána: tabulky záznamů, výčty a rozšířené datové typy (EDT).</span><span class="sxs-lookup"><span data-stu-id="25f3a-126">In both cases, be aware that the following metadata will be automatically added: tables of records, enumerations, and extended data types (EDTs).</span></span> <span data-ttu-id="25f3a-127">Pokud jsou požadovány další typy metadat, musí být přidány ručně.</span><span class="sxs-lookup"><span data-stu-id="25f3a-127">When additional types of metadata are required, they must be manually added.</span></span>

    <span data-ttu-id="25f3a-128">Je nutné přidat metadata, která se vztahují k transakcím zahraničního obchodu, a ručně vybrat položky metadat.</span><span class="sxs-lookup"><span data-stu-id="25f3a-128">You must add some metadata that is related to foreign trade transactions and manually select metadata items.</span></span>

9. <span data-ttu-id="25f3a-129">Vyberte **Přidat zdroj dat \> Záznamy tabulky**.</span><span class="sxs-lookup"><span data-stu-id="25f3a-129">Select **Add data source \> Table records**.</span></span>
10. <span data-ttu-id="25f3a-130">Vyfiltrujte hodnotu **Intrastat** v poli **Název**.</span><span class="sxs-lookup"><span data-stu-id="25f3a-130">Filter on a value of **Intrastat** in the **Name** field.</span></span>
11. <span data-ttu-id="25f3a-131">Vyberte záznam tabulky **Intrastat**.</span><span class="sxs-lookup"><span data-stu-id="25f3a-131">Select the **Intrastat** table record.</span></span>
12. <span data-ttu-id="25f3a-132">Vyberte **OK**.</span><span class="sxs-lookup"><span data-stu-id="25f3a-132">Select **OK**.</span></span>

    <span data-ttu-id="25f3a-133">Je nutné přidat informace o metadatech do tabulky záznamů Intrastat.</span><span class="sxs-lookup"><span data-stu-id="25f3a-133">You must add metadata information about the Intrastat table of records.</span></span>

13. <span data-ttu-id="25f3a-134">Ve stromové struktuře vyberte **Intrastat záznamů tabulky \> \>Vztahy \> IntrastatCommodity (záznamy tabulky EcoResCategory)**.</span><span class="sxs-lookup"><span data-stu-id="25f3a-134">In the tree, select **Table records Intrastat \> \>Relations \> IntrastatCommodity (Table records EcoResCategory)**.</span></span>
14. <span data-ttu-id="25f3a-135">Vyberte **Přidat metadata**.</span><span class="sxs-lookup"><span data-stu-id="25f3a-135">Select **Add metadata**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="25f3a-136">Metadata o požadovaných vztazích pro vybranou tabulku záznamů je nutné přidat ručně.</span><span class="sxs-lookup"><span data-stu-id="25f3a-136">Metadata about required relations for the selected table of records must be added manually.</span></span>

15. <span data-ttu-id="25f3a-137">Vyberte **Přidat zdroj dat**.</span><span class="sxs-lookup"><span data-stu-id="25f3a-137">Select **Add data source**.</span></span>
16. <span data-ttu-id="25f3a-138">Vyberte **Výčet**.</span><span class="sxs-lookup"><span data-stu-id="25f3a-138">Select **Enumeration**.</span></span>
17. <span data-ttu-id="25f3a-139">Vyfiltrujte hodnotu **IntrastatDirection** v poli **Název**.</span><span class="sxs-lookup"><span data-stu-id="25f3a-139">Filter on a value of **IntrastatDirection** in the **Name** field.</span></span>
18. <span data-ttu-id="25f3a-140">Vyberte záznam výčtu **IntrastatDirection**.</span><span class="sxs-lookup"><span data-stu-id="25f3a-140">Select the **IntrastatDirection** enumeration record.</span></span>
19. <span data-ttu-id="25f3a-141">Vyberte **OK**.</span><span class="sxs-lookup"><span data-stu-id="25f3a-141">Select **OK**.</span></span>
20. <span data-ttu-id="25f3a-142">Zvolte **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="25f3a-142">Select **Save**.</span></span>
21. <span data-ttu-id="25f3a-143">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="25f3a-143">Close the page.</span></span>
22. <span data-ttu-id="25f3a-144">Dokončete návrh konceptu konfigurace metadat:</span><span class="sxs-lookup"><span data-stu-id="25f3a-144">Complete the draft version of the metadata configuration:</span></span>

    1. <span data-ttu-id="25f3a-145">Vyberte **Změnit stav \> Dokončeno**.</span><span class="sxs-lookup"><span data-stu-id="25f3a-145">Select **Change status \> Complete**.</span></span>
    2. <span data-ttu-id="25f3a-146">Vyberte **OK**.</span><span class="sxs-lookup"><span data-stu-id="25f3a-146">Select **OK**.</span></span>
    3. <span data-ttu-id="25f3a-147">Vyberte dokončenou verzi 1.</span><span class="sxs-lookup"><span data-stu-id="25f3a-147">Select the completed version 1.</span></span>

23. <span data-ttu-id="25f3a-148">Exportujte dokončenou verzi konfigurace metadat z aplikace do souboru XML:</span><span class="sxs-lookup"><span data-stu-id="25f3a-148">Export the completed version of the metadata configuration from the application as an XML file:</span></span>

    1. <span data-ttu-id="25f3a-149">Vyberte **Exchange \> Exportovat jako soubor XML**.</span><span class="sxs-lookup"><span data-stu-id="25f3a-149">Select **Exchange \> Export as XML file**.</span></span>
    2. <span data-ttu-id="25f3a-150">Vyberte **OK**.</span><span class="sxs-lookup"><span data-stu-id="25f3a-150">Select **OK**.</span></span>

<span data-ttu-id="25f3a-151">Konfigurace metadat ER, kterou jste vytvořili, je uložena jako **Metadata zahraničního obchodu.xml**.</span><span class="sxs-lookup"><span data-stu-id="25f3a-151">The ER metadata configuration that you created is saved as the **Foreign trade metadata.xml** file.</span></span> <span data-ttu-id="25f3a-152">Nyní jej můžete importovat do RCS, aby jej bylo možné použít jako zdroj metadat pro obchodní doménu zahraničního obchodu.</span><span class="sxs-lookup"><span data-stu-id="25f3a-152">You can now import it into RCS, so that it can be used as the source of metadata for the foreign trade business domain.</span></span> <span data-ttu-id="25f3a-153">Na základě těchto informací můžete určit mapování mezi metadaty aplikací a datovým modelem ER.</span><span class="sxs-lookup"><span data-stu-id="25f3a-153">Based on this information, you can specify the mapping between application metadata and the ER data model.</span></span>

## <a name="access-application-metadata-by-using-an-er-configuration"></a><span data-ttu-id="25f3a-154">Přístup k metadatům aplikace pomocí konfigurace elektronického výkaznictví</span><span class="sxs-lookup"><span data-stu-id="25f3a-154">Access application metadata by using an ER configuration</span></span>

<span data-ttu-id="25f3a-155">Následující postup ukazuje, jak může uživatel RCS, který má roli **Správce systému** nebo **Vývojář elektronického výkaznictví**, navrhnout nové mapování modelu ER pomocí metadat z aplikace.</span><span class="sxs-lookup"><span data-stu-id="25f3a-155">The following procedure shows how an RCS user who has the **System Administrator** or **Electronic Reporting Developer** role can design a new ER model mapping by using metadata from the application.</span></span> <span data-ttu-id="25f3a-156">K metadatům aplikace se přistupuje pomocí konfigurace metadat ER, která obsahuje ukázkovou sadu metadat pro přístup k transakcím zahraničního obchodu.</span><span class="sxs-lookup"><span data-stu-id="25f3a-156">Application metadata will be accessed by using an ER metadata configuration that contains a sample set of metadata to access foreign trade transactions.</span></span>

<span data-ttu-id="25f3a-157">Než budete moci tuto proceduru dokončit, je nutné dokončit nejprve následující procedury:</span><span class="sxs-lookup"><span data-stu-id="25f3a-157">Before you can complete this procedure, you must first complete the following procedures:</span></span>

- [<span data-ttu-id="25f3a-158">Vytvoření poskytovatelů konfigurace a jejich označení jako aktivních</span><span class="sxs-lookup"><span data-stu-id="25f3a-158">Create configuration providers and mark them as active</span></span>](tasks/er-configuration-provider-mark-it-active-2016-11.md)
- [<span data-ttu-id="25f3a-159">Příprava metadat aplikace k použití v RCS</span><span class="sxs-lookup"><span data-stu-id="25f3a-159">Prepare application metadata that can be used in RCS</span></span>](#prepare-application-metadata-that-can-be-used-in-rcs)

1. <span data-ttu-id="25f3a-160">Přejděte na **Všechny pracovní prostory \> Elektronické výkaznictví**.</span><span class="sxs-lookup"><span data-stu-id="25f3a-160">Go to **All workspaces \> Electronic reporting**.</span></span>
2. <span data-ttu-id="25f3a-161">Ujistěte se, že poskytovatel konfigurace pro vzorovou společnost ‘Litware, Inc.’ je k dispozici a je označen jako **Aktivní**.</span><span class="sxs-lookup"><span data-stu-id="25f3a-161">Make sure that the configuration provider for the sample company, Litware, Inc., is available and marked as **Active**.</span></span> <span data-ttu-id="25f3a-162">Pokud tohoto zprostředkovatele konfigurace nevidíte, musíte nejprve dokončit jednotlivé kroky v postupu [Vytvoření zprostředkovatelů konfigurace a jejich označení jako aktivních](tasks/er-configuration-provider-mark-it-active-2016-11.md).</span><span class="sxs-lookup"><span data-stu-id="25f3a-162">If you don't see this configuration provider, complete the [Create configuration providers and mark them as active](tasks/er-configuration-provider-mark-it-active-2016-11.md) procedure.</span></span> 
3. <span data-ttu-id="25f3a-163">Importujte konfiguraci metadat ER obsahující metadata z aplikace, která je nakonfigurována pro generování elektronických dokumentů pro doménu zahraničního obchodu.</span><span class="sxs-lookup"><span data-stu-id="25f3a-163">Import the ER metadata configuration that contains metadata for the application, and that is configured to generate electronic documents for the foreign trade business domain.</span></span> <span data-ttu-id="25f3a-164">Tato konfigurace metadat ER byla vytvořena a exportována jako soubor XML v proceduře [Příprava metadat aplikace, která lze použít v proceduře RCS](#prepare-application-metadata-that-can-be-used-in-rcs) dříve v tomto tématu.</span><span class="sxs-lookup"><span data-stu-id="25f3a-164">You created this ER metadata configuration and exported it as an XML file in the [Prepare application metadata that can be used in RCS](#prepare-application-metadata-that-can-be-used-in-rcs) procedure earlier in this topic.</span></span>

    1. <span data-ttu-id="25f3a-165">Vyberte **Konfigurace metadat**.</span><span class="sxs-lookup"><span data-stu-id="25f3a-165">Select **Metadata configurations**.</span></span>
    2. <span data-ttu-id="25f3a-166">Vyberte **Exchange**.</span><span class="sxs-lookup"><span data-stu-id="25f3a-166">Select **Exchange**.</span></span>
    3. <span data-ttu-id="25f3a-167">Vyberte **Načíst ze souboru XML**.</span><span class="sxs-lookup"><span data-stu-id="25f3a-167">Select **Load from XML file**.</span></span>
    4. <span data-ttu-id="25f3a-168">Klikněte na Procházet a vyberte soubor **Foreign trade metadata.xml**.</span><span class="sxs-lookup"><span data-stu-id="25f3a-168">Browse to select the **Foreign trade metadata.xml** file.</span></span>
    5. <span data-ttu-id="25f3a-169">Vyberte **OK**.</span><span class="sxs-lookup"><span data-stu-id="25f3a-169">Select **OK**.</span></span>
    6. <span data-ttu-id="25f3a-170">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="25f3a-170">Close the page.</span></span>

4. <span data-ttu-id="25f3a-171">Vytvoření konfigurace datového modelu:</span><span class="sxs-lookup"><span data-stu-id="25f3a-171">Create a data model configuration:</span></span>

    1. <span data-ttu-id="25f3a-172">Vyberte **Konfigurace vykazování**.</span><span class="sxs-lookup"><span data-stu-id="25f3a-172">Select **Reporting configurations**.</span></span>
    2. <span data-ttu-id="25f3a-173">Vyberte **Vytvořit konfiguraci**.</span><span class="sxs-lookup"><span data-stu-id="25f3a-173">Select **Create configuration**.</span></span>
    3. <span data-ttu-id="25f3a-174">V rozevíracím dialogovém okně do pole **Název** zadejte **Model zahraničního obchodu**.</span><span class="sxs-lookup"><span data-stu-id="25f3a-174">In the drop-down dialog box, in the **Name** field, enter **Foreign trade model**.</span></span>
    4. <span data-ttu-id="25f3a-175">Vyberte **Vytvořit konfiguraci**.</span><span class="sxs-lookup"><span data-stu-id="25f3a-175">Select **Create configuration**.</span></span>
    5. <span data-ttu-id="25f3a-176">Vyberte možnost **Návrhář**.</span><span class="sxs-lookup"><span data-stu-id="25f3a-176">Select **Designer**.</span></span>
    6. <span data-ttu-id="25f3a-177">Kliknutím na možnost **Nový** otevřete dialogové okno.</span><span class="sxs-lookup"><span data-stu-id="25f3a-177">Select **New** to open the drop dialog.</span></span>

        1. <span data-ttu-id="25f3a-178">Do pole **Název** zadejte **Kořen**.</span><span class="sxs-lookup"><span data-stu-id="25f3a-178">In the **Name** field, type **Root**.</span></span>
        2. <span data-ttu-id="25f3a-179">Vyberte **přidat**.</span><span class="sxs-lookup"><span data-stu-id="25f3a-179">Select **Add**.</span></span>
    
    7. <span data-ttu-id="25f3a-180">Kliknutím na možnost **Nový** otevřete dialogové okno.</span><span class="sxs-lookup"><span data-stu-id="25f3a-180">Select **New** to open the drop dialog.</span></span>

        1. <span data-ttu-id="25f3a-181">Do pole **Název** zadejte **Transakce**.</span><span class="sxs-lookup"><span data-stu-id="25f3a-181">In the **Name** field, type **Transaction**.</span></span>
        2. <span data-ttu-id="25f3a-182">V poli **Typ položky** vyberte **Seznam záznamů**.</span><span class="sxs-lookup"><span data-stu-id="25f3a-182">In the **Item type** field, select **Record list**.</span></span>
        3. <span data-ttu-id="25f3a-183">Vyberte **přidat**.</span><span class="sxs-lookup"><span data-stu-id="25f3a-183">Select **Add**.</span></span>
 
    8. <span data-ttu-id="25f3a-184">Kliknutím na možnost **Nový** otevřete dialogové okno.</span><span class="sxs-lookup"><span data-stu-id="25f3a-184">Select **New** to open the drop dialog.</span></span>

        1. <span data-ttu-id="25f3a-185">Do pole **Název** zadejte **Kód komodity**.</span><span class="sxs-lookup"><span data-stu-id="25f3a-185">In the **Name** field, type **Commodity code**.</span></span>
        2. <span data-ttu-id="25f3a-186">V poli **Typ položky** vyberte **Řetězec**.</span><span class="sxs-lookup"><span data-stu-id="25f3a-186">In the **Item type** field, select **String**.</span></span>
        3. <span data-ttu-id="25f3a-187">Vyberte **přidat**.</span><span class="sxs-lookup"><span data-stu-id="25f3a-187">Select **Add**.</span></span>

    9. <span data-ttu-id="25f3a-188">Kliknutím na možnost **Nový** otevřete dialogové okno.</span><span class="sxs-lookup"><span data-stu-id="25f3a-188">Select **New** to open the drop dialog.</span></span>

        1. <span data-ttu-id="25f3a-189">Do pole Název zadejte **Fakturovaná částka**.</span><span class="sxs-lookup"><span data-stu-id="25f3a-189">In the Name field, type **Invoiced amount**.</span></span>
        2. <span data-ttu-id="25f3a-190">V poli **Typ položky** vyberte **Reálný**.</span><span class="sxs-lookup"><span data-stu-id="25f3a-190">In the **Item type** field, select **Real**.</span></span>
        3. <span data-ttu-id="25f3a-191">Vyberte **přidat**.</span><span class="sxs-lookup"><span data-stu-id="25f3a-191">Select **Add**.</span></span>

    10. <span data-ttu-id="25f3a-192">Kliknutím na možnost **Nový** otevřete dialogové okno.</span><span class="sxs-lookup"><span data-stu-id="25f3a-192">Select **New** to open the drop dialog.</span></span>

        1. <span data-ttu-id="25f3a-193">Do pole **Název** zadejte **Datum**.</span><span class="sxs-lookup"><span data-stu-id="25f3a-193">In the **Name** field, type **Date**.</span></span>
        2. <span data-ttu-id="25f3a-194">V poli **Typ položky** vyberte **Datum**.</span><span class="sxs-lookup"><span data-stu-id="25f3a-194">In the **Item type** field, select **Date**.</span></span>
        3. <span data-ttu-id="25f3a-195">Vyberte **přidat**.</span><span class="sxs-lookup"><span data-stu-id="25f3a-195">Select **Add**.</span></span>
 
    11. <span data-ttu-id="25f3a-196">Vyberte **Přidat \> Kořenová reference**.</span><span class="sxs-lookup"><span data-stu-id="25f3a-196">Select **Add \> Root reference**.</span></span>
    12. <span data-ttu-id="25f3a-197">Vyberte **OK**.</span><span class="sxs-lookup"><span data-stu-id="25f3a-197">Select **OK**.</span></span>
    13. <span data-ttu-id="25f3a-198">Zvolte **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="25f3a-198">Select **Save**.</span></span>
    14. <span data-ttu-id="25f3a-199">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="25f3a-199">Close the page.</span></span>
    15. <span data-ttu-id="25f3a-200">Vyberte **Změnit stav \> Dokončeno**.</span><span class="sxs-lookup"><span data-stu-id="25f3a-200">Select **Change status \> Complete**.</span></span>
    16. <span data-ttu-id="25f3a-201">Vyberte **OK**.</span><span class="sxs-lookup"><span data-stu-id="25f3a-201">Select **OK**.</span></span>

5. <span data-ttu-id="25f3a-202">Vytvoření konfigurace mapování modelu:</span><span class="sxs-lookup"><span data-stu-id="25f3a-202">Create a model mapping configuration:</span></span>

    1. <span data-ttu-id="25f3a-203">Vyberte **Vytvořit konfiguraci**.</span><span class="sxs-lookup"><span data-stu-id="25f3a-203">Select **Create configuration**.</span></span>
    2. <span data-ttu-id="25f3a-204">V rozevíracím dialogovém okně zadejte do pole **Nový** **Mapování modelu založené na datovém modelu Model zahraničního obchodu**.</span><span class="sxs-lookup"><span data-stu-id="25f3a-204">In the drop-down dialog box, in the **New** field, enter **Model Mapping based on data model Foreign trade model**.</span></span>
    3. <span data-ttu-id="25f3a-205">Do pole **Název** zadejte **Mapování zahraničního obchodu**'.</span><span class="sxs-lookup"><span data-stu-id="25f3a-205">In the **Name** field, enter **Foreign trade mapping**.</span></span>
    4. <span data-ttu-id="25f3a-206">Vyberte **Vytvořit konfiguraci**.</span><span class="sxs-lookup"><span data-stu-id="25f3a-206">Select **Create configuration**.</span></span>
    5. <span data-ttu-id="25f3a-207">Na pevné záložce **Předpoklady** vyberte **Upravit**.</span><span class="sxs-lookup"><span data-stu-id="25f3a-207">On the **Prerequisites** FastTab, select **Edit**.</span></span>
    6. <span data-ttu-id="25f3a-208">Zvolte **Nové**.</span><span class="sxs-lookup"><span data-stu-id="25f3a-208">Select **New**.</span></span>
    7. <span data-ttu-id="25f3a-209">V poli **Typ komponenty předpokladu** vyberte **Konfigurace**.</span><span class="sxs-lookup"><span data-stu-id="25f3a-209">In the **Prerequisite component type** field, select **Configuration**.</span></span>
    8. <span data-ttu-id="25f3a-210">Vyberte konfiguraci **Metadat zahraničního obchodu**.</span><span class="sxs-lookup"><span data-stu-id="25f3a-210">Select the **Foreign trade metadata** configuration.</span></span>
    9. <span data-ttu-id="25f3a-211">Zvolte **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="25f3a-211">Select **Save**.</span></span> <span data-ttu-id="25f3a-212">Všimněte si, že jsme přidali odkaz na verzi 1 konfigurace **Metadata zahraničního obchodu**.</span><span class="sxs-lookup"><span data-stu-id="25f3a-212">Notice that the reference is added to version 1 of the **Foreign trade metadata** configuration.</span></span> <span data-ttu-id="25f3a-213">Metadata aplikace z této konfigurace budou nabízena, dokud nebude toto mapování modelu navrženo.</span><span class="sxs-lookup"><span data-stu-id="25f3a-213">Application metadata from this configuration will be offered while the model mapping is designed.</span></span>
    10. <span data-ttu-id="25f3a-214">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="25f3a-214">Close the page.</span></span>
    11. <span data-ttu-id="25f3a-215">Vyberte možnost **Návrhář**.</span><span class="sxs-lookup"><span data-stu-id="25f3a-215">Select **Designer**.</span></span>
    12. <span data-ttu-id="25f3a-216">Vyberte možnost **Návrhář**.</span><span class="sxs-lookup"><span data-stu-id="25f3a-216">Select **Designer**.</span></span>
    13. <span data-ttu-id="25f3a-217">Ve stromovém zobrazení vyberte **Dynamics 365 for Operations \> Záznamy tabulky**.</span><span class="sxs-lookup"><span data-stu-id="25f3a-217">In the tree, select **Dynamics 365 for Operations \> Table records**.</span></span>
    14. <span data-ttu-id="25f3a-218">Vyberte **Přidat kořen**.</span><span class="sxs-lookup"><span data-stu-id="25f3a-218">Select **Add root**.</span></span>
    15. <span data-ttu-id="25f3a-219">Do pole **Název** zadejte **Intrastat**.</span><span class="sxs-lookup"><span data-stu-id="25f3a-219">In the **Name** field, enter **Intrastat**.</span></span>
    16. <span data-ttu-id="25f3a-220">Vyberte záznamy tabulky **Intrastat**.</span><span class="sxs-lookup"><span data-stu-id="25f3a-220">Select **Intrastat** table records.</span></span>
    17. <span data-ttu-id="25f3a-221">Vyberte **OK**.</span><span class="sxs-lookup"><span data-stu-id="25f3a-221">Select **OK**.</span></span>

        > [!NOTE]
        > <span data-ttu-id="25f3a-222">Jsou nabídnuty pouze dvě tabulky, protože do sady metadat, která je právě používána, byly přidány pouze dvě tabulky.</span><span class="sxs-lookup"><span data-stu-id="25f3a-222">Only two tables are offered, because only two tables were added to the set of metadata that is currently used.</span></span>

    18. <span data-ttu-id="25f3a-223">Vyberte možnost **vazba**.</span><span class="sxs-lookup"><span data-stu-id="25f3a-223">Select **Bind**.</span></span>
    19. <span data-ttu-id="25f3a-224">Ve stromovém zobrazení vyberte **Intrastat \> AmountMST**.</span><span class="sxs-lookup"><span data-stu-id="25f3a-224">In the tree, select **Intrastat \> AmountMST**.</span></span>
    20. <span data-ttu-id="25f3a-225">Ve stromovém zobrazení vyberte možnost **Transakce = Intrastat \> Fakturovaná částka**.</span><span class="sxs-lookup"><span data-stu-id="25f3a-225">In the tree, select **Transaction = Intrastat \> Invoiced amount**.</span></span>
    21. <span data-ttu-id="25f3a-226">Vyberte možnost **vazba**.</span><span class="sxs-lookup"><span data-stu-id="25f3a-226">Select **Bind**.</span></span>
    22. <span data-ttu-id="25f3a-227">Ve stromovém zobrazení vyberte **Intrastat \> TransDate**.</span><span class="sxs-lookup"><span data-stu-id="25f3a-227">In the tree, select **Intrastat \> TransDate**.</span></span>
    23. <span data-ttu-id="25f3a-228">Ve stromovém zobrazení vyberte **Transakce = Intrastat \> Date**.</span><span class="sxs-lookup"><span data-stu-id="25f3a-228">In the tree, select **Transaction = Intrastat \> Date**.</span></span>
    24. <span data-ttu-id="25f3a-229">Vyberte možnost **vazba**.</span><span class="sxs-lookup"><span data-stu-id="25f3a-229">Select **Bind**.</span></span>
    25. <span data-ttu-id="25f3a-230">Ve stromovém zobrazení vyberte **Intrastat \> \>Relations \> IntrastatCommodity \> Code**.</span><span class="sxs-lookup"><span data-stu-id="25f3a-230">In the tree, select **Intrastat \> \>Relations \> IntrastatCommodity \> Code**.</span></span>
    26. <span data-ttu-id="25f3a-231">Ve stromovém zobrazení vyberte **Transakce = Intrastat \> Commodity code**.</span><span class="sxs-lookup"><span data-stu-id="25f3a-231">In the tree, select **Transaction = Intrastat \> Commodity code**.</span></span>
    27. <span data-ttu-id="25f3a-232">Vyberte možnost **vazba**.</span><span class="sxs-lookup"><span data-stu-id="25f3a-232">Select **Bind**.</span></span>
    28. <span data-ttu-id="25f3a-233">Vyberte **Ověřit**.</span><span class="sxs-lookup"><span data-stu-id="25f3a-233">Select **Validate**.</span></span>

        > [!NOTE]
        > <span data-ttu-id="25f3a-234">Po ověření jste úspěšně jsme provedli vázání prvků datového modelu s položkami datových zdrojů, které jsou popsány pomocí podrobností metadat aplikace z odkazované konfigurace metadat ER.</span><span class="sxs-lookup"><span data-stu-id="25f3a-234">After validation is completed, you've successfully bound elements of the data model to items of the data sources that are described by using details of the application metadata from the referenced ER metadata configuration.</span></span>

    29. <span data-ttu-id="25f3a-235">Zvolte **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="25f3a-235">Select **Save**.</span></span>

<span data-ttu-id="25f3a-236">Podle požadavku můžete rozšířit existující sadu metadat v aplikaci</span><span class="sxs-lookup"><span data-stu-id="25f3a-236">As you require, you can extend the existing set of metadata in the application.</span></span> <span data-ttu-id="25f3a-237">Poté můžete exportovat novou dokončenou verzi konfigurace metadat ER, importovat ho do RCS a aktualizovat předpoklady konfigurace konfigurovaného mapování modelu odkazující na novou verzi importované konfigurace metadat.</span><span class="sxs-lookup"><span data-stu-id="25f3a-237">You can then export the new completed version of the ER metadata configuration, import it into RCS, and update the prerequisites of the configured model mapping configuration to refer to a new version of the imported metadata configuration.</span></span>

> [!NOTE]
> <span data-ttu-id="25f3a-238">Tento způsob získání informací o metadatech aplikace je jediný dostupný pro lokálně nasazené aplikace (v případě místních obchodních dat \[LBD\] nebo místně, model nasazení se používá pro aplikaci).</span><span class="sxs-lookup"><span data-stu-id="25f3a-238">This method for getting information about application metadata is the only available method for applications that are locally deployed (that is, when a local business data \[LBD\], or on-premises, deployment model is used for the application).</span></span>

## <a name="access-application-metadata-by-using-connected-applications"></a><span data-ttu-id="25f3a-239">Přístup k metadatům aplikace pomocí připojených aplikací</span><span class="sxs-lookup"><span data-stu-id="25f3a-239">Access application metadata by using connected applications</span></span>

<span data-ttu-id="25f3a-240">Následující postup ukazuje, jak může uživatel RCS, který má roli **Správce systému** nebo **Vývojář elektronického výkaznictví**, navrhnout nové mapování modelu ER pomocí metadat aplikace.</span><span class="sxs-lookup"><span data-stu-id="25f3a-240">The following procedure shows how an RCS user who has the **System Administrator** or **Electronic Reporting Developer** role can design a new ER model mapping by using metadata of the application.</span></span> <span data-ttu-id="25f3a-241">Přístup k metadatům aplikace bude probíhat online pomocí aplikace připojené k RCS.</span><span class="sxs-lookup"><span data-stu-id="25f3a-241">Application metadata will be accessed online by using RCS connected application.</span></span> <span data-ttu-id="25f3a-242">Ukázkové mapování modelu ER bude konfigurováno pro přístup k transakcím zahraničního obchodu.</span><span class="sxs-lookup"><span data-stu-id="25f3a-242">A sample ER model mapping will be configured to access foreign trade transactions.</span></span>

<span data-ttu-id="25f3a-243">K provedení kroků v tomto postupu musíte nejprve dokončit proceduru [Vytvoření zprostředkovatelů konfigurace a jejich označení jako aktivních](tasks/er-configuration-provider-mark-it-active-2016-11.md) v RCS.</span><span class="sxs-lookup"><span data-stu-id="25f3a-243">To complete this procedure, you must first complete the [Create configuration providers and mark them as active](tasks/er-configuration-provider-mark-it-active-2016-11.md) procedure in RCS.</span></span> <span data-ttu-id="25f3a-244">Pokud jste nedokončili kroky uvedené v tématu [Přístup k metadatům aplikace pomocí konfigurace ER](#access-application-metadata-by-using-an-er-configuration), přejděte na stránku [Příklady elektronického výkaznictví Dynamics 365 for Finance and Operations 8.1](https://go.microsoft.com/fwlink/?linkid=2082739) a stáhněte a uložte následující konfigurace ER a uložte je místně: **Foreign trade metadata.xml**, **Foreign trade model.xml** a **Foreign trade mapping.xml**.</span><span class="sxs-lookup"><span data-stu-id="25f3a-244">If you haven't yet completed the [Access application metadata by using an ER configuration](#access-application-metadata-by-using-an-er-configuration) procedure earlier in this topic, go to [Electronic Reporting Task Guides for Dynamics 365 for Finance and Operations 8.1](https://go.microsoft.com/fwlink/?linkid=2082739) page to download the following ER configuration files in advance and save them locally: **Foreign trade metadata.xml**, **Foreign trade model.xml**, and **Foreign trade mapping.xml**.</span></span>


### <a name="get-required-er-configurations"></a><span data-ttu-id="25f3a-245">Získání požadovaných konfigurací ER</span><span class="sxs-lookup"><span data-stu-id="25f3a-245">Get required ER configurations</span></span>

<span data-ttu-id="25f3a-246">Pokud jste již provedli kroky v postupu [Přístup k metadatům aplikace pomocí konfigurace ER](#access-application-metadata-by-using-an-er-configuration) dříve v tomto tématu, již máte v aktuální instanci RSC všechny potřebné konfigurace ER (konfigurace metadat pro zahraniční obchod, model a mapování).</span><span class="sxs-lookup"><span data-stu-id="25f3a-246">If you've already completed the [Access application metadata by using an ER configuration](#access-application-metadata-by-using-an-er-configuration) procedure earlier in this topic, you already have all the required ER configurations (the foreign trade metadata, model, and mapping configurations) in the current RCS instance.</span></span> <span data-ttu-id="25f3a-247">V takovém případě můžete tento postup vynechat.</span><span class="sxs-lookup"><span data-stu-id="25f3a-247">In that case, you can skip this procedure.</span></span>

1. <span data-ttu-id="25f3a-248">Přejděte na **Všechny pracovní prostory \> Elektronické výkaznictví**.</span><span class="sxs-lookup"><span data-stu-id="25f3a-248">Go to **All workspaces \> Electronic reporting**.</span></span>
2. <span data-ttu-id="25f3a-249">Vyberte **Konfigurace vykazování**.</span><span class="sxs-lookup"><span data-stu-id="25f3a-249">Select **Reporting configurations**.</span></span>
3. <span data-ttu-id="25f3a-250">Načtěte soubory konfigurace **Foreign trade metadata.xml**, **Foreign trade model.xml** a **Foreign trade mapping.xml** opakující následující řetězec kroků pro každý z nich:</span><span class="sxs-lookup"><span data-stu-id="25f3a-250">Load the **Foreign trade metadata.xml**, **Foreign trade model.xml**, and **Foreign trade mapping.xml** configuration files repeating the following chain of steps for each of them:</span></span>

    1. <span data-ttu-id="25f3a-251">Vyberte **Exchange**.</span><span class="sxs-lookup"><span data-stu-id="25f3a-251">Select **Exchange**.</span></span>
    2. <span data-ttu-id="25f3a-252">Vyberte **Načíst ze souboru XML**.</span><span class="sxs-lookup"><span data-stu-id="25f3a-252">Select **Load from XML file**.</span></span>
    3. <span data-ttu-id="25f3a-253">Vyberte **Procházet** a vyberte soubor.</span><span class="sxs-lookup"><span data-stu-id="25f3a-253">Select **Browse**, and select a file.</span></span>
    4. <span data-ttu-id="25f3a-254">Vyberte **OK**.</span><span class="sxs-lookup"><span data-stu-id="25f3a-254">Select **OK**.</span></span>

### <a name="register-the-connection-with-the-application"></a><span data-ttu-id="25f3a-255">Zaregistrovat připojení k aplikaci</span><span class="sxs-lookup"><span data-stu-id="25f3a-255">Register the connection with the application</span></span>

1. <span data-ttu-id="25f3a-256">Přejděte na **Všechny pracovní prostory \> Elektronické výkaznictví**.</span><span class="sxs-lookup"><span data-stu-id="25f3a-256">Go to **All workspaces \> Electronic reporting**.</span></span>
2. <span data-ttu-id="25f3a-257">Vyberte **Připojené aplikace**.</span><span class="sxs-lookup"><span data-stu-id="25f3a-257">Select **Connected applications**.</span></span>
3. <span data-ttu-id="25f3a-258">Ujistěte se, že konfigurovaná aplikace je založena na Microsoft Azure a že je obecně přístupná uživatelům RCS.</span><span class="sxs-lookup"><span data-stu-id="25f3a-258">Make sure that the configured application is based on Microsoft Azure, and that it is accessible in general to RCS users.</span></span> <span data-ttu-id="25f3a-259">Aktuální uživatel RCS musí mít přístup k vybrané aplikaci a být zaregistrován jako uživatel této aplikace, který má roli poskytující oprávnění pro přístup k metadatům aplikace.</span><span class="sxs-lookup"><span data-stu-id="25f3a-259">The current RCS user must have access to the configured application being registered as a user of this application in a role that gives him or her privileges to access the application's metadata.</span></span>
4. <span data-ttu-id="25f3a-260">Zvolte **Nové**.</span><span class="sxs-lookup"><span data-stu-id="25f3a-260">Select **New**.</span></span>
5. <span data-ttu-id="25f3a-261">Do pole **Název** zadejte **MyConnectedApp** jako název připojené aplikace.</span><span class="sxs-lookup"><span data-stu-id="25f3a-261">In the **Name** field, enter **MyConnectedApp** as the name of the connected application.</span></span>
6. <span data-ttu-id="25f3a-262">V poli **aplikace** zadejte adresu URL aplikace.</span><span class="sxs-lookup"><span data-stu-id="25f3a-262">In the **Application** field, specify the URL of the application.</span></span>
7. <span data-ttu-id="25f3a-263">V poli **Tenant** zadejte poskytovatele aplikace.</span><span class="sxs-lookup"><span data-stu-id="25f3a-263">In the **Tenant** field, specify the provider of the application.</span></span>
8. <span data-ttu-id="25f3a-264">Zvolte **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="25f3a-264">Select **Save**.</span></span> 
9. <span data-ttu-id="25f3a-265">Při kontrole připojení ke konfigurované aplikaci vyberte stránce **Připojit ke vzdálené aplikaci na** odkaz **Kliknutím sem se připojte k vybrané aplikaci**.</span><span class="sxs-lookup"><span data-stu-id="25f3a-265">When you check the connection to the configured application, on the **Connect to remote application** page, select the **Select here to connect to selected remote application** link.</span></span> 
10. <span data-ttu-id="25f3a-266">Chcete-li ověřit přístup ke konfigurované aplikaci, vyberte možnost **Zkontrolovat připojení**.</span><span class="sxs-lookup"><span data-stu-id="25f3a-266">Select **Check connection** to validate access to the configured application.</span></span>
11. <span data-ttu-id="25f3a-267">Vyberte **Zavřít**.</span><span class="sxs-lookup"><span data-stu-id="25f3a-267">Select **Close**.</span></span>

<span data-ttu-id="25f3a-268">Po dokončení této procedury a ověření úspěšného připojení budou podrobnosti o verzi a klientovi pro konfigurovanou aplikaci v aktuální mřížce aktualizovány.</span><span class="sxs-lookup"><span data-stu-id="25f3a-268">After you complete this procedure and validation of the connection succeeds, the version and tenant details for the configured application will be updated in the current grid.</span></span>

### <a name="review-the-existing-model-mapping-configuration"></a><span data-ttu-id="25f3a-269">Kontrola existující konfigurace mapování modelu ER</span><span class="sxs-lookup"><span data-stu-id="25f3a-269">Review the existing model mapping configuration</span></span>

1. <span data-ttu-id="25f3a-270">Přejděte na **Všechny pracovní prostory \> Elektronické výkaznictví**.</span><span class="sxs-lookup"><span data-stu-id="25f3a-270">Go to **All workspaces \> Electronic reporting**.</span></span>
2. <span data-ttu-id="25f3a-271">Vyberte **Konfigurace vykazování**.</span><span class="sxs-lookup"><span data-stu-id="25f3a-271">Select **Reporting configurations**.</span></span>
3. <span data-ttu-id="25f3a-272">Ve stromové struktuře vyberte **Model zahraničního obchodu \> Mapování zahraničního obchodu**.</span><span class="sxs-lookup"><span data-stu-id="25f3a-272">In the tree, select **Foreign trade model \> Foreign trade mapping**.</span></span>
4. <span data-ttu-id="25f3a-273">Na pevné záložce **Předpoklady** vyberte Upravit.</span><span class="sxs-lookup"><span data-stu-id="25f3a-273">Select the **Prerequisites** FasTab.</span></span>

    > [!NOTE]
    > <span data-ttu-id="25f3a-274">V současné době toto mapování odkazuje na konfiguraci metadat.</span><span class="sxs-lookup"><span data-stu-id="25f3a-274">Currently, this mapping refers to the metadata configuration.</span></span> <span data-ttu-id="25f3a-275">Metadata aplikace z této konfigurace budou nabízena, dokud nebude toto mapování modelu navrženo.</span><span class="sxs-lookup"><span data-stu-id="25f3a-275">Application metadata from this configuration will be offered while this model mapping is designed.</span></span>

4. <span data-ttu-id="25f3a-276">Vyberte možnost **Návrhář**.</span><span class="sxs-lookup"><span data-stu-id="25f3a-276">Select **Designer**.</span></span>
5. <span data-ttu-id="25f3a-277">Vyberte možnost **Návrhář**.</span><span class="sxs-lookup"><span data-stu-id="25f3a-277">Select **Designer**.</span></span>
6. <span data-ttu-id="25f3a-278">Ve stromovém zobrazení vyberte **Dynamics 365 for Operations \> Záznamy tabulky**.</span><span class="sxs-lookup"><span data-stu-id="25f3a-278">In the tree, select **Dynamics 365 for Operations \> Table records**.</span></span>
7. <span data-ttu-id="25f3a-279">Vyberte **Přidat kořen**.</span><span class="sxs-lookup"><span data-stu-id="25f3a-279">Select **Add root**.</span></span>
8. <span data-ttu-id="25f3a-280">V poli **Tabulka** zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="25f3a-280">In the **Table** field, enter or select a value.</span></span>

    > [!NOTE]
    > <span data-ttu-id="25f3a-281">V současné době toto mapování odkazuje na konfiguraci metadat.</span><span class="sxs-lookup"><span data-stu-id="25f3a-281">Currently, this mapping refers to the metadata configuration.</span></span> <span data-ttu-id="25f3a-282">Metadata aplikace z této konfigurace budou nabízena, dokud nebude toto mapování modelu navrženo.</span><span class="sxs-lookup"><span data-stu-id="25f3a-282">Application metadata from this configuration will be offered while this model mapping is designed.</span></span>

9. <span data-ttu-id="25f3a-283">Vyberte možnost **Zrušit**.</span><span class="sxs-lookup"><span data-stu-id="25f3a-283">Select **Cancel**.</span></span>

### <a name="assign-the-connected-application-to-a-model-mapping"></a><span data-ttu-id="25f3a-284">Přiřazení připojené aplikace k mapování modelu</span><span class="sxs-lookup"><span data-stu-id="25f3a-284">Assign the connected application to a model mapping</span></span>

1. <span data-ttu-id="25f3a-285">Vyberte možnost **Upravit**.</span><span class="sxs-lookup"><span data-stu-id="25f3a-285">Select **Edit**.</span></span>
2. <span data-ttu-id="25f3a-286">V **poli Připojená aplikace** vyberte aplikaci **MyConnectedApp**.</span><span class="sxs-lookup"><span data-stu-id="25f3a-286">In the **Connected application field**, select the **MyConnectedApp** application.</span></span>

    > [!NOTE]
    > <span data-ttu-id="25f3a-287">Toto mapování odkazuje na metadata vybrané připojené aplikace.</span><span class="sxs-lookup"><span data-stu-id="25f3a-287">This mapping refers to the metadata of the selected connected application.</span></span> <span data-ttu-id="25f3a-288">Pokud stejné mapování odkazuje na konfiguraci metadat a připojenou aplikaci současně, budou použita metadata připojené aplikace.</span><span class="sxs-lookup"><span data-stu-id="25f3a-288">If a mapping refers to the metadata configuration and the connected application at the same time, the metadata of the connected application will be used.</span></span>

3. <span data-ttu-id="25f3a-289">Vyberte možnost **Návrhář**.</span><span class="sxs-lookup"><span data-stu-id="25f3a-289">Select **Designer**.</span></span>
4. <span data-ttu-id="25f3a-290">Vyberte možnost **Návrhář**.</span><span class="sxs-lookup"><span data-stu-id="25f3a-290">Select **Designer**.</span></span>
5. <span data-ttu-id="25f3a-291">Ve stromovém zobrazení vyberte **Dynamics 365 for Operations \> Záznamy tabulky**.</span><span class="sxs-lookup"><span data-stu-id="25f3a-291">In the tree, select **Dynamics 365 for Operations \> Table records**.</span></span>
6. <span data-ttu-id="25f3a-292">Vyberte **Přidat kořen**.</span><span class="sxs-lookup"><span data-stu-id="25f3a-292">Select **Add root**.</span></span>
7. <span data-ttu-id="25f3a-293">V poli **Tabulka** zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="25f3a-293">In the **Table** field, enter or select a value.</span></span>

    > [!NOTE]
    > <span data-ttu-id="25f3a-294">Nyní byly nabídnuty více než dvě tabulky aplikace, protože toto mapování používá všechna metadata připojené aplikace, která je k ní přiřazena.</span><span class="sxs-lookup"><span data-stu-id="25f3a-294">At this point, more than two application tables are offered, because this mapping uses all the metadata of the connected application that has been assigned to it.</span></span>

8. <span data-ttu-id="25f3a-295">Vyberte možnost **Zrušit**.</span><span class="sxs-lookup"><span data-stu-id="25f3a-295">Select **Cancel**.</span></span>
9. <span data-ttu-id="25f3a-296">Vyberte **Ověřit**.</span><span class="sxs-lookup"><span data-stu-id="25f3a-296">Select **Validate**.</span></span>

<span data-ttu-id="25f3a-297">Úspěšně jste provedli vázání prvků datového modelu s položkami datových zdrojů, které jsou popsány pomocí podrobností metadat připojené aplikace, která byla přiřazena pro toto mapování.</span><span class="sxs-lookup"><span data-stu-id="25f3a-297">You've now bound elements of the data model to items of the data sources that are described by using details of the metadata of the connected application that has been assigned to this mapping.</span></span>

<span data-ttu-id="25f3a-298">Potřebujete-li vyhodnotit mapování modelu pomocí metadat jiné verze aplikace, zaregistrujte jinou připojenou aplikaci, přiřaďte ji k tomuto mapování modelu a ověřte ji proti novým metadatům.</span><span class="sxs-lookup"><span data-stu-id="25f3a-298">When you must evaluate this model mapping by using the metadata of a different version of the application, register another connected application, assign it to this model mapping, and validate it against the new metadata.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="25f3a-299">Další zdroje</span><span class="sxs-lookup"><span data-stu-id="25f3a-299">Additional resources</span></span>

<span data-ttu-id="25f3a-300">Případně můžete přehrát Průvodce záznamem úloh **Připravit metadata aplikace, která lze použít v RCS** v aplikaci a **Přístup k metadatům aplikace pomocí konfigurace ER** a **Přístup k metadatům aplikace pomocí připojených aplikací** v RCS.</span><span class="sxs-lookup"><span data-stu-id="25f3a-300">Alternatively, you can play the **Prepare application metadata that can be used in RCS** task guide in the application as as well as the **Access application metadata by using an ER configuration** and **Access application metadata by using connected applications** task guides in RCS.</span></span> <span data-ttu-id="25f3a-301">Tyto Průvodce záznamem úloh je možné stáhnout ze stránky [Průvodci záznamem úloh pro Dynamics 365 for Finance and Operations 8.1](https://go.microsoft.com/fwlink/?linkid=2082739).</span><span class="sxs-lookup"><span data-stu-id="25f3a-301">These task guides can be downloaded from the [Electronic Reporting Task Guides for Dynamics 365 for Finance and Operations 8.1](https://go.microsoft.com/fwlink/?linkid=2082739) page.</span></span>
