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
ms.openlocfilehash: 3d091cd835cfcb7164f83259b69e3bc1d7c09dc4
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/18/2020
ms.locfileid: "3143147"
---
# <a name="prepare-application-metadata-to-be-used-in-rcs"></a><span data-ttu-id="e730e-103">Příprava metadat aplikace k použití v RCS</span><span class="sxs-lookup"><span data-stu-id="e730e-103">Prepare application metadata to be used in RCS</span></span>
[!include [banner](../../includes/banner.md)]

<span data-ttu-id="e730e-104">Následující kroky vysvětlují, jak může uživatel v roli správce systému nebo vývojáře elektronického výkaznictví vytvořit novou konfiguraci elektronického výkaznictví, která obsahuje metadata aplikace pro navrhování konfigurací mapování modelu elektronického výkaznictví v Regulatory configuration service (RCS).</span><span class="sxs-lookup"><span data-stu-id="e730e-104">The following steps explain how a user in the System Administrator or Electronic Reporting Developer role can create a new Electronic reporting (ER) configuration that contains application metadata for designing ER model mapping configurations in Regulatory configuration service (RCS).</span></span> <span data-ttu-id="e730e-105">Tato konfigurace se použije pro návrh ukázkové konfigurace mapování modelu elektronického výkaznictví pro přístup k transakcím zahraničního obchodu.</span><span class="sxs-lookup"><span data-stu-id="e730e-105">This configuration will be used for designing a sample ER model mapping configuration to access foreign trade transactions.</span></span> <span data-ttu-id="e730e-106">V tomto příkladu vytvoříte konfiguraci pro vzorovou společnost Litware, Inc. Tyto kroky lze provést v libovolné společnosti.</span><span class="sxs-lookup"><span data-stu-id="e730e-106">In this example, you will create a configuration for sample company, Litware, Inc. These steps can be performed in any company.</span></span> <span data-ttu-id="e730e-107">K provedení těchto kroků musíte v RCS nejprve dokončit jednotlivé kroky v tématu [Vytvoření poskytovatelů konfigurace a jejich označení jako aktivních](er-configuration-provider-mark-it-active-2016-11.md).</span><span class="sxs-lookup"><span data-stu-id="e730e-107">To complete these steps, you must first complete the steps in the topic, [Create configuration providers and mark them as active](er-configuration-provider-mark-it-active-2016-11.md).</span></span>

## <a name="prerequisites"></a><span data-ttu-id="e730e-108">Předpoklady</span><span class="sxs-lookup"><span data-stu-id="e730e-108">Prerequisites</span></span>
1.    <span data-ttu-id="e730e-109">Přejděte na **Správa organizace** > **Pracovní prostory** > **Elektronické výkaznictví**.</span><span class="sxs-lookup"><span data-stu-id="e730e-109">Go to **Organization administration** > **Workspaces** > **Electronic reporting**.</span></span> 
2.    <span data-ttu-id="e730e-110">Ujistěte se, že poskytovatel konfigurace pro vzorovou společnost ‘Litware, Inc.’ je k dispozici a je označen jako **Aktivní**.</span><span class="sxs-lookup"><span data-stu-id="e730e-110">Make sure that the configuration provider for the sample company, Litware, Inc., is available and marked as **Active**.</span></span> <span data-ttu-id="e730e-111">Pokud tohoto zprostředkovatele konfigurace nevidíte, musíte nejprve dokončit jednotlivé kroky v postupu [Vytvoření poskytovatelů konfigurace a jejich označení jako aktivních](er-configuration-provider-mark-it-active-2016-11.md).</span><span class="sxs-lookup"><span data-stu-id="e730e-111">If you don't see this configuration provider, complete the steps in the procedure [Create configuration providers and mark them as active](er-configuration-provider-mark-it-active-2016-11.md).</span></span> 
3.    <span data-ttu-id="e730e-112">Klikněte na **Konfigurace metadat**.</span><span class="sxs-lookup"><span data-stu-id="e730e-112">Click **Metadata configurations**.</span></span> 
4.    <span data-ttu-id="e730e-113">Předpokládejme, že se použije RCS pro návrh řešení elektronického výkaznictví pro aplikace Finance and Operations, které budou použity k vygenerování elektronických dokumentů, které obsahují informace z cizí obchodní domény.</span><span class="sxs-lookup"><span data-stu-id="e730e-113">Assume that RCS will be used to design an ER solution for a Finance and Operation application that will generate electronic documents that contain information from foreign trade business domain.</span></span> <span data-ttu-id="e730e-114">Pro určení mapování mezi datovým modelem elektronického výkaznictví a zdroji požadovaných dat, musíme mít v RCS přístup k metadatům aplikace pro Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="e730e-114">To specify the mapping between ER data model and sources of required data, in RCS we need to have access to metadata of the Finance and Operation application.</span></span> <span data-ttu-id="e730e-115">Proto v rámci řešení elektronického výkaznictví nakonfigurujeme novou konfiguraci metadat elektronického výkaznictví, která obsahuje všechna metadata aktuálně požadovaná k vygenerování sestav elektronického výkaznictví pro vybranou obchodní doménu.</span><span class="sxs-lookup"><span data-stu-id="e730e-115">Therefore, as part of designing ER solution we configure a new ER metadata configuration containing all metadata that is currently required for generation ER reports for selected business domain.</span></span> 

## <a name="add-metadata-configuration"></a><span data-ttu-id="e730e-116">Přidání konfigurace metadat</span><span class="sxs-lookup"><span data-stu-id="e730e-116">Add metadata configuration</span></span> 
1.    <span data-ttu-id="e730e-117">Kliknutím na možnost **Vytvořit konfiguraci** otevřete dialogové okno.</span><span class="sxs-lookup"><span data-stu-id="e730e-117">Click **Create configuration** to open the drop dialog.</span></span> 
2.    <span data-ttu-id="e730e-118">Do pole **Název** zadejte 'Metadata zahraničního obchodu'.</span><span class="sxs-lookup"><span data-stu-id="e730e-118">In the **Name** field, type 'Foreign trade metadata'.</span></span> 
3.    <span data-ttu-id="e730e-119">Klepněte na možnost **Vytvořit konfiguraci**.</span><span class="sxs-lookup"><span data-stu-id="e730e-119">Click **Create configuration**.</span></span> 
4.    <span data-ttu-id="e730e-120">Klikněte na možnost **Návrhář**.</span><span class="sxs-lookup"><span data-stu-id="e730e-120">Click **Designer**.</span></span> 
5.    <span data-ttu-id="e730e-121">Klikněte na tlačítko **Přidat**.</span><span class="sxs-lookup"><span data-stu-id="e730e-121">Click **Add**.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="e730e-122">Můžete vybrat všechna metadata pro celou aplikaci, nebo pro vybrané modely nebo moduly.</span><span class="sxs-lookup"><span data-stu-id="e730e-122">You can select all metadata for the entire application or selected models or selected modules.</span></span> <span data-ttu-id="e730e-123">V tomto případě je třeba mít na paměti, že následující metadata budou automaticky přidána: tabulky záznamů, výčty a rozšířené datové typy.</span><span class="sxs-lookup"><span data-stu-id="e730e-123">Be aware that in this case the following metadata will be automatically added: tables of records, enumerations, and extended data types.</span></span> <span data-ttu-id="e730e-124">Pokud jsou požadovány další typy metadat, musí být přidány ručně.</span><span class="sxs-lookup"><span data-stu-id="e730e-124">When additional types of metadata are needed, they must be added manually.</span></span> 
 
<span data-ttu-id="e730e-125">Máme některá metadata související s transakcemi zahraničního obchodu pomocí ruční volby položek metadat.</span><span class="sxs-lookup"><span data-stu-id="e730e-125">We have some foreign trade transactions related metadata by selecting metadata items manually.</span></span> 
  
6.    <span data-ttu-id="e730e-126">Klikněte na možnost **Přidat datový zdroj**.</span><span class="sxs-lookup"><span data-stu-id="e730e-126">Click **Add data source**.</span></span> 
7.    <span data-ttu-id="e730e-127">Klikněte na **Záznamy tabulky**.</span><span class="sxs-lookup"><span data-stu-id="e730e-127">Click **Table records**.</span></span> 
8.    <span data-ttu-id="e730e-128">Použijte rychlý filtr k filtrování na poli **Název** s hodnotou Intrastat.</span><span class="sxs-lookup"><span data-stu-id="e730e-128">Use the Quick Filter to filter on the **Name** field with a value of 'Intrastat'.</span></span> 
9.    <span data-ttu-id="e730e-129">Vyberte záznam tabulky **Intrastat**.</span><span class="sxs-lookup"><span data-stu-id="e730e-129">Select the **Intrastat** table record.</span></span> 
10.    <span data-ttu-id="e730e-130">Klikněte na tlačítko **OK**.</span><span class="sxs-lookup"><span data-stu-id="e730e-130">Click **OK**.</span></span>
  
<span data-ttu-id="e730e-131">Přidali jsme informace o metadatech do tabulky záznamů Intrastat.</span><span class="sxs-lookup"><span data-stu-id="e730e-131">We added metadata information about the Intrastat table of records.</span></span> 
  
11.    <span data-ttu-id="e730e-132">Ve stromovém zobrazení rozbalte **Intrastat záznamů tabulky**\>**Vztahy**.</span><span class="sxs-lookup"><span data-stu-id="e730e-132">In the tree, expand **Table records Intrastat**\>**Relations**.</span></span> 
12.    <span data-ttu-id="e730e-133">Ve stromové struktuře vyberte **Intrastat záznamů tabulky**\>**Vztahy\IntrastatCommodity (záznamy tabulky EcoResCategory)**.</span><span class="sxs-lookup"><span data-stu-id="e730e-133">In the tree, select **Table records Intrastat**\>**Relations\IntrastatCommodity (Table records EcoResCategory)**.</span></span>     
13.    <span data-ttu-id="e730e-134">Klikněte na **Přidat metadata**.</span><span class="sxs-lookup"><span data-stu-id="e730e-134">Click **Add metadata**.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="e730e-135">Metadata o požadovaných vztazích pro vybranou tabulku záznamů je nutné přidat ručně.</span><span class="sxs-lookup"><span data-stu-id="e730e-135">Metadata about required relations for selected table of records must be added manually.</span></span> 
  
16.    <span data-ttu-id="e730e-136">Klikněte na možnost **Přidat datový zdroj**.</span><span class="sxs-lookup"><span data-stu-id="e730e-136">Click **Add data source**.</span></span> 
17.    <span data-ttu-id="e730e-137">Klikněte na **Výčet**.</span><span class="sxs-lookup"><span data-stu-id="e730e-137">Click **Enumeration**.</span></span> 
18.    <span data-ttu-id="e730e-138">Použijte rychlý filtr k filtrování na poli **Název** s hodnotou IntrastatDirection.</span><span class="sxs-lookup"><span data-stu-id="e730e-138">Use the Quick Filter to filter on the **Name** field with a value of 'IntrastatDirection'.</span></span> 
19.    <span data-ttu-id="e730e-139">Vyberte záznam **Výčet IntrastatDirection**.</span><span class="sxs-lookup"><span data-stu-id="e730e-139">Select the **IntrastatDirection enumeration** record.</span></span> 
20.    <span data-ttu-id="e730e-140">Klikněte na tlačítko **OK**.</span><span class="sxs-lookup"><span data-stu-id="e730e-140">Click **OK**.</span></span> 
21.    <span data-ttu-id="e730e-141">Klikněte na možnost **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="e730e-141">Click **Save**.</span></span>  
22.    <span data-ttu-id="e730e-142">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="e730e-142">Close the page.</span></span> 
  
## <a name="complete-the-draft-version-of-metadata-configuration"></a><span data-ttu-id="e730e-143">Dokončení návrhu konceptu konfigurace metadat</span><span class="sxs-lookup"><span data-stu-id="e730e-143">Complete the draft version of metadata configuration</span></span>
1.    <span data-ttu-id="e730e-144">Klikněte na položku **Změnit stav**.</span><span class="sxs-lookup"><span data-stu-id="e730e-144">Click **Change status**.</span></span> 
2.    <span data-ttu-id="e730e-145">Klikněte na **Dokončit**.</span><span class="sxs-lookup"><span data-stu-id="e730e-145">Click **Complete**.</span></span> 
3.    <span data-ttu-id="e730e-146">Klikněte na tlačítko **OK**.</span><span class="sxs-lookup"><span data-stu-id="e730e-146">Click **OK**.</span></span> 
4.    <span data-ttu-id="e730e-147">Vyberte dokončenou verzi **1**.</span><span class="sxs-lookup"><span data-stu-id="e730e-147">Select the completed version **1**.</span></span> 
  
## <a name="export-the-completed-version-of-metadata-configuration-from-application-as-xml-file"></a><span data-ttu-id="e730e-148">Exportujte dokončenou verzi konfigurace metadat z aplikace do souboru XML</span><span class="sxs-lookup"><span data-stu-id="e730e-148">Export the completed version of metadata configuration from application as XML file</span></span>
1.    <span data-ttu-id="e730e-149">Klikněte na **Exchange**.</span><span class="sxs-lookup"><span data-stu-id="e730e-149">Click **Exchange**.</span></span> 
2.    <span data-ttu-id="e730e-150">Klikněte na **Exportovat jako soubor XML**.</span><span class="sxs-lookup"><span data-stu-id="e730e-150">Click **Export as XML file**.</span></span> 
3.    <span data-ttu-id="e730e-151">Klikněte na tlačítko **OK**.</span><span class="sxs-lookup"><span data-stu-id="e730e-151">Click **OK**.</span></span> 
    
<span data-ttu-id="e730e-152">Vytvořená konfigurace metadat elektronického výkaznictví byla uložena jako soubor XML, který lze importovat do RCS a použít jako zdroj informací o metadatech pro obchodní doménu zahraničního obchodu v aplikaci.</span><span class="sxs-lookup"><span data-stu-id="e730e-152">The created ER metadata configuration has been saved as XML file that can be imported to RCS and used as the source of information about metadata for the foreign trade business domain.</span></span> <span data-ttu-id="e730e-153">Na základě těchto informací můžeme určit mapování mezi metadaty aplikací a datovým modelem elektronického výkaznictví.</span><span class="sxs-lookup"><span data-stu-id="e730e-153">Based on this information, we can specify the mapping between application metadata and ER data model.</span></span>
