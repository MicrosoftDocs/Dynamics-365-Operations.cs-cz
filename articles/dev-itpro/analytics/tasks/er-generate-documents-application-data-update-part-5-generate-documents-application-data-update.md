---
title: Generování dokumentů s daty aplikace
description: K dokončení kroků v tomto postupu musíte nejprve dokončit postup ER Generování dokumentů s aktualizací dat aplikace (část 4 - úprava formátu).
author: NickSelin
manager: AnnBe
ms.date: 06/19/2017
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 90c6ebc456d3e137e43022fad7d59ce3ca2cdcab
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/15/2019
ms.locfileid: "1544488"
---
# <a name="generate-documents-that-have-application-data"></a><span data-ttu-id="54bab-103">Generování dokumentů s daty aplikace</span><span class="sxs-lookup"><span data-stu-id="54bab-103">Generate documents that have application data</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="54bab-104">K dokončení kroků v tomto postupu musíte nejprve dokončit postup ER Generování dokumentů s aktualizací dat aplikace (část 4: úprava formátu).</span><span class="sxs-lookup"><span data-stu-id="54bab-104">To complete the steps in this procedure, you must first complete the procedure, “ER Generate documents with application data update (Part 4: Modify format)”.</span></span>



<span data-ttu-id="54bab-105">Kroky v tomto postupu vysvětlují návrh konfigurace elektronického vykazování (ER) k vygenerování elektronického dokumentu a aktualizaci dat aplikace.</span><span class="sxs-lookup"><span data-stu-id="54bab-105">The steps in this procedure explain how to design Electronic reporting (ER) configurations to generate an electronic document and update application data.</span></span> <span data-ttu-id="54bab-106">V rámci tohoto postupu můžete provést konfiguraci formátu ER a vygenerovat tak sestavu Intrastat a aktualizovat data aplikace pro archivaci podrobností o procesu vykazování.</span><span class="sxs-lookup"><span data-stu-id="54bab-106">In this procedure, you execute the ER format configuration to generate the Intrastat report and update application data for archiving details of the reporting process.</span></span>



<span data-ttu-id="54bab-107">Tento postup je vytvořen pro uživatele s přiřazenou rolí správce systému nebo vývojáře elektronického vykazování.</span><span class="sxs-lookup"><span data-stu-id="54bab-107">This procedure is created for users with the assigned role of system administrator or electronic reporting developer.</span></span> <span data-ttu-id="54bab-108">Tyto kroky lze dokončit za použití datové sady DEMF.</span><span class="sxs-lookup"><span data-stu-id="54bab-108">These steps can be completed using the DEMF dataset.</span></span> <span data-ttu-id="54bab-109">Před zahájením se ujistěte, že kontext země pro společnost DEMF je BEL (Belgie).</span><span class="sxs-lookup"><span data-stu-id="54bab-109">Before you begin, make sure that the country context for the DEMF company is BEL (Belgium).</span></span>


## <a name="set-up-foreign-trade-parameters"></a><span data-ttu-id="54bab-110">Nastavit parametry zahraničního obchodu</span><span class="sxs-lookup"><span data-stu-id="54bab-110">Set up foreign trade parameters</span></span>
1. <span data-ttu-id="54bab-111">Přejděte na Daň > Nastavení > Zahraniční obchod > Parametry zahraničního obchodu.</span><span class="sxs-lookup"><span data-stu-id="54bab-111">Go to Tax > Setup > Foreign trade > Foreign trade parameters.</span></span>
2. <span data-ttu-id="54bab-112">Klikněte na kartu Číselné řady.</span><span class="sxs-lookup"><span data-stu-id="54bab-112">Click the Number sequences tab.</span></span>
    * <span data-ttu-id="54bab-113">Při archivování podrobných informací o procesu vykazování Intrastat je nutné určit záznamy každého vytvořeného archivu.</span><span class="sxs-lookup"><span data-stu-id="54bab-113">Archiving details of Intrastat reporting process, we need to identify records of each archive we created.</span></span> <span data-ttu-id="54bab-114">Tato akce vyžaduje konfiguraci zvláštní číselné řady.</span><span class="sxs-lookup"><span data-stu-id="54bab-114">A special number sequence must be configured for that.</span></span>  
3. <span data-ttu-id="54bab-115">Vyberte referenci ID archivu Intrastat.</span><span class="sxs-lookup"><span data-stu-id="54bab-115">Select the ‘Intrastat archive ID’ reference.</span></span>
4. <span data-ttu-id="54bab-116">Zadejte hodnotu do pole Kód číselné řady.</span><span class="sxs-lookup"><span data-stu-id="54bab-116">In the Number sequence code field, type a value.</span></span>
    * <span data-ttu-id="54bab-117">V poli Kód číselné řady zadejte nebo vyberte hodnotu Fore_2’.</span><span class="sxs-lookup"><span data-stu-id="54bab-117">In the ‘Number sequence code’ field, enter or select the value ‘Fore_2’.</span></span>  
5. <span data-ttu-id="54bab-118">Vyřešte změny v číselné řadě Číslo.</span><span class="sxs-lookup"><span data-stu-id="54bab-118">ResolveChanges the Number sequence code.</span></span>
6. <span data-ttu-id="54bab-119">Klikněte na položku Uložit.</span><span class="sxs-lookup"><span data-stu-id="54bab-119">Click Save.</span></span>
7. <span data-ttu-id="54bab-120">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="54bab-120">Close the page.</span></span>

## <a name="run-modified-er-format"></a><span data-ttu-id="54bab-121">Spuštění upraveného formátu ER</span><span class="sxs-lookup"><span data-stu-id="54bab-121">Run modified ER format</span></span>
1. <span data-ttu-id="54bab-122">Přejděte do části Správa organizace > Elektronické výkaznictví > Konfigurace.</span><span class="sxs-lookup"><span data-stu-id="54bab-122">Go to Organization administration > Electronic reporting > Configurations.</span></span>
2. <span data-ttu-id="54bab-123">Ve stromovém zobrazení rozbalte Intrastat (model).</span><span class="sxs-lookup"><span data-stu-id="54bab-123">In the tree, expand 'Intrastat (model)'.</span></span>
3. <span data-ttu-id="54bab-124">Ve stromové struktuře vyberte Intrastat (model)\Intrastat (format).</span><span class="sxs-lookup"><span data-stu-id="54bab-124">In the tree, select 'Intrastat (model)\Intrastat (format)'.</span></span>
4. <span data-ttu-id="54bab-125">Klikněte na položku Spustit.</span><span class="sxs-lookup"><span data-stu-id="54bab-125">Click Run.</span></span>
5. <span data-ttu-id="54bab-126">Do pole Zadat název souboru zadejte intrastat2.xml.</span><span class="sxs-lookup"><span data-stu-id="54bab-126">In the Enter file name field, type 'intrastat2.xml'.</span></span>
    * <span data-ttu-id="54bab-127">intrastat2.xml</span><span class="sxs-lookup"><span data-stu-id="54bab-127">intrastat2.xml</span></span>  
6. <span data-ttu-id="54bab-128">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="54bab-128">Click OK.</span></span>

## <a name="review-er-format-executions-results"></a><span data-ttu-id="54bab-129">Kontrola výsledků spuštění formátu ER</span><span class="sxs-lookup"><span data-stu-id="54bab-129">Review ER format execution’s results</span></span>
    * <span data-ttu-id="54bab-130">Prohlédněte si vygenerovaný soubor XML.</span><span class="sxs-lookup"><span data-stu-id="54bab-130">Review the generated XML file.</span></span>  
1. <span data-ttu-id="54bab-131">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="54bab-131">Close the page.</span></span>
2. <span data-ttu-id="54bab-132">Přejděte na Daň > Deklarace > Zahraniční obchod > Intrastat.</span><span class="sxs-lookup"><span data-stu-id="54bab-132">Go to Tax > Declarations > Foreign trade > Intrastat.</span></span>
    * <span data-ttu-id="54bab-133">Otevřete tento formulář s transakcemi Intrastat, které byly zahrnuty ve vygenerovaném elektronickém dokumentu.</span><span class="sxs-lookup"><span data-stu-id="54bab-133">Open this form containing Intrastat transactions that have been included to the generated electronic document.</span></span>  
3. <span data-ttu-id="54bab-134">Klikněte na Archiv Intrastat.</span><span class="sxs-lookup"><span data-stu-id="54bab-134">Click Intrastat archive.</span></span>
    * <span data-ttu-id="54bab-135">Vzhledem k tomu, že aktivovaný formát ER nově obsahuje nastavení pro aktualizaci dat aplikace, podrobnosti dokončené sestavy Intrastat byly archivovány.</span><span class="sxs-lookup"><span data-stu-id="54bab-135">Since the executed ER format contains now settings for application data update, the details of the completed Intrastat reporting have been archived.</span></span> <span data-ttu-id="54bab-136">Pomocí tohoto formuláře můžete zobrazit záznam záhlaví vytvořeného archivu.</span><span class="sxs-lookup"><span data-stu-id="54bab-136">In this form, you can see the header record of the created archive.</span></span>  
4. <span data-ttu-id="54bab-137">Klepněte na možnost Podrobnosti.</span><span class="sxs-lookup"><span data-stu-id="54bab-137">Click Details.</span></span>
    * <span data-ttu-id="54bab-138">Pomocí tohoto formuláře můžete zobrazit podrobnosti k vytvořenému archivu.</span><span class="sxs-lookup"><span data-stu-id="54bab-138">In this form, you can see the details for the created archive.</span></span>  
5. <span data-ttu-id="54bab-139">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="54bab-139">Close the page.</span></span>
6. <span data-ttu-id="54bab-140">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="54bab-140">Close the page.</span></span>
7. <span data-ttu-id="54bab-141">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="54bab-141">Close the page.</span></span>

