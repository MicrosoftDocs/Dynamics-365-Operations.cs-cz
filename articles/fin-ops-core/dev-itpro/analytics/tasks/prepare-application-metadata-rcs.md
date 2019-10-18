---
title: Příprava metadat aplikace k použití v RCS
description: Kroky v tomto tématu vysvětlují, jak může uživatel vytvořit novou konfiguraci elektronického výkaznictví (ER), která obsahuje metadata aplikace pro navrhování konfigurací mapování modelu elektronického výkaznictví v Regulatory configuration service (RCS).
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
ms.openlocfilehash: e3a33eefca98e14ed0435f8f1a7a9f90a69498ee
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 09/27/2019
ms.locfileid: "2182156"
---
# <a name="prepare-application-metadata-to-be-used-in-rcs"></a><span data-ttu-id="cc6c8-103">Příprava metadat aplikace k použití v RCS</span><span class="sxs-lookup"><span data-stu-id="cc6c8-103">Prepare application metadata to be used in RCS</span></span>
[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="cc6c8-104">Následující kroky vysvětlují, jak může uživatel v roli správce systému nebo vývojáře elektronického výkaznictví vytvořit novou konfiguraci elektronického výkaznictví, která obsahuje metadata aplikace pro navrhování konfigurací mapování modelu elektronického výkaznictví v Regulatory configuration service (RCS).</span><span class="sxs-lookup"><span data-stu-id="cc6c8-104">The following steps explain how a user in the System Administrator or Electronic Reporting Developer role can create a new Electronic reporting (ER) configuration that contains application metadata for designing ER model mapping configurations in Regulatory configuration service (RCS).</span></span> <span data-ttu-id="cc6c8-105">Tato konfigurace se použije pro návrh ukázkové konfigurace mapování modelu elektronického výkaznictví pro přístup k transakcím zahraničního obchodu.</span><span class="sxs-lookup"><span data-stu-id="cc6c8-105">This configuration will be used for designing a sample ER model mapping configuration to access foreign trade transactions.</span></span> <span data-ttu-id="cc6c8-106">V tomto příkladu vytvoříte konfiguraci pro vzorovou společnost Litware, Inc. Tyto kroky lze provést v libovolné společnosti.</span><span class="sxs-lookup"><span data-stu-id="cc6c8-106">In this example, you will create a configuration for sample company, Litware, Inc. These steps can be performed in any company.</span></span> <span data-ttu-id="cc6c8-107">K provedení těchto kroků musíte v RCS nejprve dokončit jednotlivé kroky v tématu [Vytvoření poskytovatelů konfigurace a jejich označení jako aktivních](er-configuration-provider-mark-it-active-2016-11.md).</span><span class="sxs-lookup"><span data-stu-id="cc6c8-107">To complete these steps, you must first complete the steps in the topic, [Create configuration providers and mark them as active](er-configuration-provider-mark-it-active-2016-11.md).</span></span>

## <a name="prerequisites"></a><span data-ttu-id="cc6c8-108">Předpoklady</span><span class="sxs-lookup"><span data-stu-id="cc6c8-108">Prerequisites</span></span>
1.  <span data-ttu-id="cc6c8-109">Přejděte na **Správa organizace** > **Pracovní prostory** > **Elektronické výkaznictví**.</span><span class="sxs-lookup"><span data-stu-id="cc6c8-109">Go to **Organization administration** > **Workspaces** > **Electronic reporting**.</span></span> 
2.  <span data-ttu-id="cc6c8-110">Ujistěte se, že poskytovatel konfigurace pro vzorovou společnost ‘Litware, Inc.’ je k dispozici a je označen jako **Aktivní**.</span><span class="sxs-lookup"><span data-stu-id="cc6c8-110">Make sure that the configuration provider for the sample company, Litware, Inc., is available and marked as **Active**.</span></span> <span data-ttu-id="cc6c8-111">Pokud tohoto zprostředkovatele konfigurace nevidíte, musíte nejprve dokončit jednotlivé kroky v postupu [Vytvoření poskytovatelů konfigurace a jejich označení jako aktivních](er-configuration-provider-mark-it-active-2016-11.md).</span><span class="sxs-lookup"><span data-stu-id="cc6c8-111">If you don’t see this configuration provider, complete the steps in the procedure [Create configuration providers and mark them as active](er-configuration-provider-mark-it-active-2016-11.md).</span></span> 
3.  <span data-ttu-id="cc6c8-112">Klikněte na **Konfigurace metadat**.</span><span class="sxs-lookup"><span data-stu-id="cc6c8-112">Click **Metadata configurations**.</span></span> 
4.  <span data-ttu-id="cc6c8-113">Předpokládejme, že se použije RCS pro návrh řešení elektronického výkaznictví pro aplikace Finance and Operations, které budou použity k vygenerování elektronických dokumentů, které obsahují informace z cizí obchodní domény.</span><span class="sxs-lookup"><span data-stu-id="cc6c8-113">Assume that RCS will be used to design an ER solution for a Finance and Operation application that will generate electronic documents that contain information from foreign trade business domain.</span></span> <span data-ttu-id="cc6c8-114">Pro určení mapování mezi datovým modelem elektronického výkaznictví a zdroji požadovaných dat, musíme mít v RCS přístup k metadatům aplikace pro Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="cc6c8-114">To specify the mapping between ER data model and sources of required data, in RCS we need to have access to metadata of the Finance and Operation application.</span></span> <span data-ttu-id="cc6c8-115">Proto v rámci řešení elektronického výkaznictví nakonfigurujeme novou konfiguraci metadat elektronického výkaznictví, která obsahuje všechna metadata aktuálně požadovaná k vygenerování sestav elektronického výkaznictví pro vybranou obchodní doménu.</span><span class="sxs-lookup"><span data-stu-id="cc6c8-115">Therefore, as part of designing ER solution we configure a new ER metadata configuration containing all metadata that is currently required for generation ER reports for selected business domain.</span></span> 

## <a name="add-metadata-configuration"></a><span data-ttu-id="cc6c8-116">Přidání konfigurace metadat</span><span class="sxs-lookup"><span data-stu-id="cc6c8-116">Add metadata configuration</span></span> 
1.  <span data-ttu-id="cc6c8-117">Kliknutím na možnost **Vytvořit konfiguraci** otevřete dialogové okno.</span><span class="sxs-lookup"><span data-stu-id="cc6c8-117">Click **Create configuration** to open the drop dialog.</span></span> 
2.  <span data-ttu-id="cc6c8-118">Do pole **Název** zadejte 'Metadata zahraničního obchodu'.</span><span class="sxs-lookup"><span data-stu-id="cc6c8-118">In the **Name** field, type 'Foreign trade metadata'.</span></span> 
3.  <span data-ttu-id="cc6c8-119">Klepněte na možnost **Vytvořit konfiguraci**.</span><span class="sxs-lookup"><span data-stu-id="cc6c8-119">Click **Create configuration**.</span></span> 
4.  <span data-ttu-id="cc6c8-120">Klikněte na možnost **Návrhář**.</span><span class="sxs-lookup"><span data-stu-id="cc6c8-120">Click **Designer**.</span></span> 
5.  <span data-ttu-id="cc6c8-121">Klikněte na tlačítko **Přidat**.</span><span class="sxs-lookup"><span data-stu-id="cc6c8-121">Click **Add**.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="cc6c8-122">Můžete vybrat všechna metadata pro celou aplikaci, nebo pro vybrané modely nebo moduly.</span><span class="sxs-lookup"><span data-stu-id="cc6c8-122">You can select all metadata for the entire application or selected models or selected modules.</span></span> <span data-ttu-id="cc6c8-123">V tomto případě je třeba mít na paměti, že následující metadata budou automaticky přidána: tabulky záznamů, výčty a rozšířené datové typy.</span><span class="sxs-lookup"><span data-stu-id="cc6c8-123">Be aware that in this case the following metadata will be automatically added: tables of records, enumerations, and extended data types.</span></span> <span data-ttu-id="cc6c8-124">Pokud jsou požadovány další typy metadat, musí být přidány ručně.</span><span class="sxs-lookup"><span data-stu-id="cc6c8-124">When additional types of metadata are needed, they must be added manually.</span></span> 
 
<span data-ttu-id="cc6c8-125">Máme některá metadata související s transakcemi zahraničního obchodu pomocí ruční volby položek metadat.</span><span class="sxs-lookup"><span data-stu-id="cc6c8-125">We have some foreign trade transactions related metadata by selecting metadata items manually.</span></span> 
  
6.  <span data-ttu-id="cc6c8-126">Klikněte na možnost **Přidat datový zdroj**.</span><span class="sxs-lookup"><span data-stu-id="cc6c8-126">Click **Add data source**.</span></span> 
7.  <span data-ttu-id="cc6c8-127">Klikněte na **Záznamy tabulky**.</span><span class="sxs-lookup"><span data-stu-id="cc6c8-127">Click **Table records**.</span></span> 
8.  <span data-ttu-id="cc6c8-128">Použijte rychlý filtr k filtrování na poli **Název** s hodnotou Intrastat.</span><span class="sxs-lookup"><span data-stu-id="cc6c8-128">Use the Quick Filter to filter on the **Name** field with a value of 'Intrastat'.</span></span> 
9.  <span data-ttu-id="cc6c8-129">Vyberte záznam tabulky **Intrastat**.</span><span class="sxs-lookup"><span data-stu-id="cc6c8-129">Select the **Intrastat** table record.</span></span> 
10. <span data-ttu-id="cc6c8-130">Klikněte na tlačítko **OK**.</span><span class="sxs-lookup"><span data-stu-id="cc6c8-130">Click **OK**.</span></span>
  
<span data-ttu-id="cc6c8-131">Přidali jsme informace o metadatech do tabulky záznamů Intrastat.</span><span class="sxs-lookup"><span data-stu-id="cc6c8-131">We added metadata information about the Intrastat table of records.</span></span> 
  
11. <span data-ttu-id="cc6c8-132">Ve stromovém zobrazení rozbalte **Intrastat záznamů tabulky**\>**Vztahy**.</span><span class="sxs-lookup"><span data-stu-id="cc6c8-132">In the tree, expand **Table records Intrastat**\>**Relations**.</span></span> 
12. <span data-ttu-id="cc6c8-133">Ve stromové struktuře vyberte **Intrastat záznamů tabulky**\>**Vztahy\IntrastatCommodity (záznamy tabulky EcoResCategory)**.</span><span class="sxs-lookup"><span data-stu-id="cc6c8-133">In the tree, select **Table records Intrastat**\>**Relations\IntrastatCommodity (Table records EcoResCategory)**.</span></span>   
13. <span data-ttu-id="cc6c8-134">Klikněte na **Přidat metadata**.</span><span class="sxs-lookup"><span data-stu-id="cc6c8-134">Click **Add metadata**.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="cc6c8-135">Metadata o požadovaných vztazích pro vybranou tabulku záznamů je nutné přidat ručně.</span><span class="sxs-lookup"><span data-stu-id="cc6c8-135">Metadata about required relations for selected table of records must be added manually.</span></span> 
  
16. <span data-ttu-id="cc6c8-136">Klikněte na možnost **Přidat datový zdroj**.</span><span class="sxs-lookup"><span data-stu-id="cc6c8-136">Click **Add data source**.</span></span> 
17. <span data-ttu-id="cc6c8-137">Klikněte na **Výčet**.</span><span class="sxs-lookup"><span data-stu-id="cc6c8-137">Click **Enumeration**.</span></span> 
18. <span data-ttu-id="cc6c8-138">Použijte rychlý filtr k filtrování na poli **Název** s hodnotou IntrastatDirection.</span><span class="sxs-lookup"><span data-stu-id="cc6c8-138">Use the Quick Filter to filter on the **Name** field with a value of 'IntrastatDirection'.</span></span> 
19. <span data-ttu-id="cc6c8-139">Vyberte záznam **Výčet IntrastatDirection**.</span><span class="sxs-lookup"><span data-stu-id="cc6c8-139">Select the **IntrastatDirection enumeration** record.</span></span> 
20. <span data-ttu-id="cc6c8-140">Klikněte na tlačítko **OK**.</span><span class="sxs-lookup"><span data-stu-id="cc6c8-140">Click **OK**.</span></span> 
21. <span data-ttu-id="cc6c8-141">Klikněte na možnost **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="cc6c8-141">Click **Save**.</span></span>  
22. <span data-ttu-id="cc6c8-142">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="cc6c8-142">Close the page.</span></span> 
  
## <a name="complete-the-draft-version-of-metadata-configuration"></a><span data-ttu-id="cc6c8-143">Dokončení návrhu konceptu konfigurace metadat</span><span class="sxs-lookup"><span data-stu-id="cc6c8-143">Complete the draft version of metadata configuration</span></span>
1.  <span data-ttu-id="cc6c8-144">Klikněte na položku **Změnit stav**.</span><span class="sxs-lookup"><span data-stu-id="cc6c8-144">Click **Change status**.</span></span> 
2.  <span data-ttu-id="cc6c8-145">Klikněte na **Dokončit**.</span><span class="sxs-lookup"><span data-stu-id="cc6c8-145">Click **Complete**.</span></span> 
3.  <span data-ttu-id="cc6c8-146">Klikněte na tlačítko **OK**.</span><span class="sxs-lookup"><span data-stu-id="cc6c8-146">Click **OK**.</span></span> 
4.  <span data-ttu-id="cc6c8-147">Vyberte dokončenou verzi **1**.</span><span class="sxs-lookup"><span data-stu-id="cc6c8-147">Select the completed version **1**.</span></span> 
  
## <a name="export-the-completed-version-of-metadata-configuration-from-application-as-xml-file"></a><span data-ttu-id="cc6c8-148">Exportujte dokončenou verzi konfigurace metadat z aplikace do souboru XML</span><span class="sxs-lookup"><span data-stu-id="cc6c8-148">Export the completed version of metadata configuration from application as XML file</span></span>
1.  <span data-ttu-id="cc6c8-149">Klikněte na **Exchange**.</span><span class="sxs-lookup"><span data-stu-id="cc6c8-149">Click **Exchange**.</span></span> 
2.  <span data-ttu-id="cc6c8-150">Klikněte na **Exportovat jako soubor XML**.</span><span class="sxs-lookup"><span data-stu-id="cc6c8-150">Click **Export as XML file**.</span></span> 
3.  <span data-ttu-id="cc6c8-151">Klikněte na tlačítko **OK**.</span><span class="sxs-lookup"><span data-stu-id="cc6c8-151">Click **OK**.</span></span> 
    
<span data-ttu-id="cc6c8-152">Vytvořená konfigurace metadat elektronického výkaznictví byla uložena jako soubor XML, který lze importovat do RCS a použít jako zdroj informací o metadatech pro obchodní doménu zahraničního obchodu v aplikaci.</span><span class="sxs-lookup"><span data-stu-id="cc6c8-152">The created ER metadata configuration has been saved as XML file that can be imported to RCS and used as the source of information about metadata for the foreign trade business domain.</span></span> <span data-ttu-id="cc6c8-153">Na základě těchto informací můžeme určit mapování mezi metadaty aplikací a datovým modelem elektronického výkaznictví.</span><span class="sxs-lookup"><span data-stu-id="cc6c8-153">Based on this information, we can specify the mapping between application metadata and ER data model.</span></span>
