---
title: Ukončení konfigurací v globálním úložišti RCS
description: Toto téma popisuje, jak ukončit konfigurace v globálním úložišti RCS.
author: JaneA07
manager: AnnBe
ms.date: 02/17/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ERSolutionTable, ERWorkspace
audience: Application User
ms.reviewer: kfend
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: janeaug
ms.search.validFrom: 2021-02-02
ms.dyn365.ops.version: AX 10.0.14
ms.openlocfilehash: 35d0af91161d898b09557a83913019609c71e836
ms.sourcegitcommit: e9d19f25e64cf4d1c1d07c8031a7081454a6f79e
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/18/2021
ms.locfileid: "5474241"
---
# <a name="discontinue-configurations-in-the-rcs-global-repository"></a><span data-ttu-id="a1469-103">Ukončení konfigurací v globálním úložišti RCS</span><span class="sxs-lookup"><span data-stu-id="a1469-103">Discontinue configurations in the RCS Global repository</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="a1469-104">Toto téma popisuje, jak ukončit konfiguraci v globálním úložišti RCS.</span><span class="sxs-lookup"><span data-stu-id="a1469-104">This topic describes how to discontinue configuration in the RCS Global repository.</span></span> <span data-ttu-id="a1469-105">Dříve bylo možné odstranit pouze konfigurace, které již nebyly potřebné.</span><span class="sxs-lookup"><span data-stu-id="a1469-105">Previously, it was possible only to delete configurations that were no longer required.</span></span> <span data-ttu-id="a1469-106">Nyní však můžete označit uvolněnou konfiguraci jako **Zrušenou** v globálním úložišti RCS.</span><span class="sxs-lookup"><span data-stu-id="a1469-106">However now you can mark a released configuration as **Discontinued** in the RCS Global repository.</span></span> <span data-ttu-id="a1469-107">Touto funkcí můžete provést také následující:</span><span class="sxs-lookup"><span data-stu-id="a1469-107">With this functionality, you can also do the following:</span></span> 
 
 - <span data-ttu-id="a1469-108">Poskytnout předem oznámení, když se plánuje ukončení konfigurace.</span><span class="sxs-lookup"><span data-stu-id="a1469-108">Provide up front notifications when a configuration is planned to be discontinued.</span></span>
 - <span data-ttu-id="a1469-109">Uvést příslušné podrobnosti o náhradní konfiguraci.</span><span class="sxs-lookup"><span data-stu-id="a1469-109">Include applicable details about the replacement configuration.</span></span>
 - <span data-ttu-id="a1469-110">Nastavit datum **Podporováno do** pro konkrétní konfiguraci s cílem informovat uživatele, kdy bude ukončena.</span><span class="sxs-lookup"><span data-stu-id="a1469-110">Set a **Supported until** date for the specific configuration to inform the user when it will be discontinued.</span></span>

<span data-ttu-id="a1469-111">Když ukončíte verzi konfigurace, můžete zadat následující volitelné informace:</span><span class="sxs-lookup"><span data-stu-id="a1469-111">When you discontinue a configuration version, you can specify the following optional information:</span></span>

  - <span data-ttu-id="a1469-112">**Náhradní konfigurace**</span><span class="sxs-lookup"><span data-stu-id="a1469-112">**Replacement configuration**</span></span>
  - <span data-ttu-id="a1469-113">**Verze náhradní konfigurace**</span><span class="sxs-lookup"><span data-stu-id="a1469-113">**Replacement configuration version**</span></span>
  - <span data-ttu-id="a1469-114">**Volná textová poznámka**: Toto pole použijte k poskytnutí odkazů na dokumentaci nebo odkazů</span><span class="sxs-lookup"><span data-stu-id="a1469-114">**Free text note**: Use this field to provide documentation links or references</span></span>
  - <span data-ttu-id="a1469-115">**Podporováno do**: Toto pole poskytuje navrhované datum, do kterého bude podporována aktuální konfigurace/verze.</span><span class="sxs-lookup"><span data-stu-id="a1469-115">**Supported until**: This field provides the proposed date up to which the current configuration/version will be supported.</span></span> <span data-ttu-id="a1469-116">Toto datum musí být aktualizováno ručně.</span><span class="sxs-lookup"><span data-stu-id="a1469-116">This date must be updated manually.</span></span>
  
<span data-ttu-id="a1469-117">Chcete-li konfiguraci ukončit, proveďte následující kroky.</span><span class="sxs-lookup"><span data-stu-id="a1469-117">To discontinue the configuration, complete the following steps.</span></span> 

1. <span data-ttu-id="a1469-118">Vyberte, zda chcete ukončit jednu verzi, nebo všechny verze se stejným nastavením v jedné operaci nastavením **Všechny verze** na **Ano**.</span><span class="sxs-lookup"><span data-stu-id="a1469-118">Select whether you want to discontinue a single version or all versions with the same settings in one operation by setting **All versions** to **Yes**.</span></span> 
2. <span data-ttu-id="a1469-119">Nastavte parametr **Ukončit** na **Ano**.</span><span class="sxs-lookup"><span data-stu-id="a1469-119">Set the **Discontinue** parameter to **Yes**.</span></span>
3. <span data-ttu-id="a1469-120">Vyberte **OK** k ukončení konfigurací.</span><span class="sxs-lookup"><span data-stu-id="a1469-120">Select **OK** to discontinue the configurations.</span></span> <span data-ttu-id="a1469-121">Pole **Datum ukončení** pole se vyplní, když uložíte změny.</span><span class="sxs-lookup"><span data-stu-id="a1469-121">The **Discontinued date** field will be populated when you save the changes.</span></span>

![Informace o ukončení konfigurace](media/Discontinue-details-2.png)
  
<span data-ttu-id="a1469-123">Konfiguraci můžete vrátit zpět na **Sdílená** nebo kdykoli upravit informace o ukončení.</span><span class="sxs-lookup"><span data-stu-id="a1469-123">You can revert configuration back to **Shared** or adjust discontinuation information at any time.</span></span> <span data-ttu-id="a1469-124">Pokud sdílíte konfiguraci, zadejte datum **Podporováno do** a všechny další informace související s ukončením, aby byly uvedeny vaše plány pro budoucí ukončení.</span><span class="sxs-lookup"><span data-stu-id="a1469-124">If you share a configuration, specify the **Supported until** date and all other information related to the discontinuation to indicate your plans for future discontinuation.</span></span>

<span data-ttu-id="a1469-125">Pokud chcete sdílet informace o plánovaném ukončení, může uživatel před vyplněním všech polí předvyplnit všechna pole související s výměnou, ale ponechat parametr **Ukončit** nastavený na **Ne**.</span><span class="sxs-lookup"><span data-stu-id="a1469-125">If you want to share information about a planned discontinuation, prior to actually discontinuing the configuration, user is able to prefill all fields related to replacement but leave the **Discontinue** parameter set to **No**.</span></span>

> [!NOTE]
> <span data-ttu-id="a1469-126">Ukončení neomezuje operace s konfiguracemi.</span><span class="sxs-lookup"><span data-stu-id="a1469-126">Discontinuation doesn't limit operations with configurations.</span></span> <span data-ttu-id="a1469-127">Konfigurace můžete nadále importovat, spouštět nebo odvozovat, tato pole jsou informační.</span><span class="sxs-lookup"><span data-stu-id="a1469-127">You can continue to import, run, or derive the configurations, these fields are informational.</span></span>

## <a name="finance-supports-displaying-this-information-starting-in-version-10014"></a><span data-ttu-id="a1469-128">Finance podporuje zobrazování těchto informací od verze 10.0.14</span><span class="sxs-lookup"><span data-stu-id="a1469-128">Finance supports displaying this information starting in version 10.0.14</span></span>

<span data-ttu-id="a1469-129">Od verze 10.0.14 Dynamics 365 Finance podporuje zobrazování informací o přerušení.</span><span class="sxs-lookup"><span data-stu-id="a1469-129">Starting in version 10.0.14, Dynamics 365 Finance supports displaying discontinuation information.</span></span> <span data-ttu-id="a1469-130">Na stránce **Globální úložiště** můžete zobrazit aktuální informace týkající se ukončení.</span><span class="sxs-lookup"><span data-stu-id="a1469-130">On the **Global repository** page, you can view up to date information related to discontinuation.</span></span> <span data-ttu-id="a1469-131">Ve výchozím nastavení jsou odfiltrovány konfigurace, které jsou přerušeny.</span><span class="sxs-lookup"><span data-stu-id="a1469-131">By default, configurations that are discontinued are filtered out.</span></span>
  
<span data-ttu-id="a1469-132">Stránka **Importované konfigurace** (ERSolutionTable) zobrazuje konfigurace, které již byly při importu ukončeny.</span><span class="sxs-lookup"><span data-stu-id="a1469-132">The **Imported configurations** (ERSolutionTable) page, shows configurations that were already discontinued when there were imported.</span></span> <span data-ttu-id="a1469-133">U těch konfigurací, které byly po importu ukončeny, lze informace o ukončení synchronizovat spuštěním úlohy **Importovat aktualizace konfigurací**.</span><span class="sxs-lookup"><span data-stu-id="a1469-133">For those configurations that were discontinued after import, the discontinuation information can be synchronized by running the **Import configurations updates** job.</span></span>


