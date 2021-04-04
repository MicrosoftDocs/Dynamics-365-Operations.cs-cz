---
title: Návrh konfigurací pro generování dokumentů s daty aplikace
description: Toto téma popisuje, jak navrhnout konfigurace elektronického výkaznictví (ER) ke generování elektronického dokumentu. (Část 1 - konfigurace importu).
author: NickSelin
manager: AnnBe
ms.date: 06/19/2017
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 217eca9bd1502d4327857720fb2d32a3ec3508ef
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/09/2021
ms.locfileid: "5563167"
---
# <a name="design-configurations-to-generate-documents-that-have-application-data"></a><span data-ttu-id="30a02-104">Návrh konfigurací pro generování dokumentů s daty aplikace</span><span class="sxs-lookup"><span data-stu-id="30a02-104">Design configurations to generate documents that have application data</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="30a02-105">K dokončení kroků v tomto postupu musíte nejprve dokončit postup ER Generování dokumentů s aktualizací dat aplikace (část 1: konfigurace importování).</span><span class="sxs-lookup"><span data-stu-id="30a02-105">To complete the steps in this procedure, you must first complete the procedure, ER Generate documents with application data update (Part 1: Import configurations).</span></span>



<span data-ttu-id="30a02-106">Kroky v tomto postupu vysvětlují návrh konfigurace elektronického vykazování (ER) k vygenerování elektronického dokumentu.</span><span class="sxs-lookup"><span data-stu-id="30a02-106">The steps in this procedure explain how to design Electronic reporting (ER) configurations to generate an electronic document.</span></span> <span data-ttu-id="30a02-107">V tomto postupu spustíte importovanou konfiguraci formátu ER vytvořenou pro vzorovou společnost Litware, Inc. k vygenerování elektronických dokumentů.</span><span class="sxs-lookup"><span data-stu-id="30a02-107">In this procedure, you run the ER imported format configuration that has been created for the sample company, Litware, Inc. to generate electronic documents.</span></span>



<span data-ttu-id="30a02-108">Tento postup je vytvořen pro uživatele s přiřazenou rolí správce systému nebo vývojáře elektronického vykazování.</span><span class="sxs-lookup"><span data-stu-id="30a02-108">This procedure is created for users with the assigned role of system administrator or electronic reporting developer.</span></span> <span data-ttu-id="30a02-109">Tyto kroky lze dokončit za použití datové sady DEMF.</span><span class="sxs-lookup"><span data-stu-id="30a02-109">These steps can be completed using the DEMF dataset.</span></span> 



<span data-ttu-id="30a02-110">Před zahájením práce změňte kontext země společnosti DEMF z DEU (Německo) na BEL (Belgie).</span><span class="sxs-lookup"><span data-stu-id="30a02-110">Before you begin, change the country context for the DEMF company from DEU (Germany) to BEL (Belgium).</span></span> <span data-ttu-id="30a02-111">Klepněte na položku Správa organizace > Organizace > Právní entity a aktualizujte kód země na primární adrese právnické osoby DEMF.</span><span class="sxs-lookup"><span data-stu-id="30a02-111">Click Organization administration > Organizations > Legal entities to update the country code in the primary address of the legal entity DEMF.</span></span> <span data-ttu-id="30a02-112">Restartujte aplikaci.</span><span class="sxs-lookup"><span data-stu-id="30a02-112">Restart your application.</span></span>


## <a name="run-imported-er-format"></a><span data-ttu-id="30a02-113">Spuštění importovaného formátu ER</span><span class="sxs-lookup"><span data-stu-id="30a02-113">Run imported ER format</span></span>
1. <span data-ttu-id="30a02-114">Přejděte do části Správa organizace > Elektronické výkaznictví > Konfigurace.</span><span class="sxs-lookup"><span data-stu-id="30a02-114">Go to Organization administration > Electronic reporting > Configurations.</span></span>
2. <span data-ttu-id="30a02-115">Ve stromovém zobrazení rozbalte Intrastat (model).</span><span class="sxs-lookup"><span data-stu-id="30a02-115">In the tree, expand 'Intrastat (model)'.</span></span>
3. <span data-ttu-id="30a02-116">Ve stromové struktuře vyberte Intrastat (model)\Intrastat (format).</span><span class="sxs-lookup"><span data-stu-id="30a02-116">In the tree, select 'Intrastat (model)\Intrastat (format)'.</span></span>
4. <span data-ttu-id="30a02-117">Klikněte na položku Spustit.</span><span class="sxs-lookup"><span data-stu-id="30a02-117">Click Run.</span></span>
    * <span data-ttu-id="30a02-118">Spusťte pracovní verzi konfigurace formátu ER pro vygenerování sestavy Intrastat.</span><span class="sxs-lookup"><span data-stu-id="30a02-118">Run the draft version of the ER format configuration to generate the Intrastat report.</span></span>  
5. <span data-ttu-id="30a02-119">Do pole Zadat název souboru zadejte intrastat.xml.</span><span class="sxs-lookup"><span data-stu-id="30a02-119">In the Enter file name field, type 'intrastat.xml'.</span></span>
    * <span data-ttu-id="30a02-120">Zadejte název souboru.</span><span class="sxs-lookup"><span data-stu-id="30a02-120">Specify the name of the file.</span></span>  
6. <span data-ttu-id="30a02-121">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="30a02-121">Click OK.</span></span>
    * <span data-ttu-id="30a02-122">Prohlédněte si vygenerovaný soubor XML.</span><span class="sxs-lookup"><span data-stu-id="30a02-122">Review the generated XML file.</span></span>  
7. <span data-ttu-id="30a02-123">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="30a02-123">Close the page.</span></span>
8. <span data-ttu-id="30a02-124">Přejděte na Daň > Deklarace > Zahraniční obchod > Intrastat.</span><span class="sxs-lookup"><span data-stu-id="30a02-124">Go to Tax > Declarations > Foreign trade > Intrastat.</span></span>
    * <span data-ttu-id="30a02-125">Otevřením tohoto formuláře zobrazíte transakce Intrastat, které jsou zahrnuty ve vygenerovaném elektronickém dokumentu.</span><span class="sxs-lookup"><span data-stu-id="30a02-125">Open this form to view the Intrastat transactions that are included in the generated electronic document.</span></span>  
9. <span data-ttu-id="30a02-126">Klikněte na Archiv Intrastat.</span><span class="sxs-lookup"><span data-stu-id="30a02-126">Click Intrastat archive.</span></span>
    * <span data-ttu-id="30a02-127">Vzhledem k tomu, že aktivovaný formát ER neobsahuje žádné nastavení pro aktualizaci dat aplikace, podrobnosti dokončené sestavy Intrastat nebyly archivovány.</span><span class="sxs-lookup"><span data-stu-id="30a02-127">Because the executed ER format does not contain any settings for application data update, the details of the completed Intrastat report have not been archived.</span></span>  
10. <span data-ttu-id="30a02-128">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="30a02-128">Close the page.</span></span>
11. <span data-ttu-id="30a02-129">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="30a02-129">Close the page.</span></span>



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]