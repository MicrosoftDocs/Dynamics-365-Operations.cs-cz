---
title: Konfigurace sdílení finančních dat mezi společnostmi
description: Tento postup popisuje, jak nakonfigurovat, povolit, ověřit a vyřešit konflikty při sdílení dat mezi společnostmi.
author: aprilolson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DataManagementWorkspace, DMFQuickImportExportRnr, DMFExecutionHistoryWorkspace, DMFExecutionHistorySummary, DMFExecutionHistoryEntities,  SysDataSharingConfiguration, SysDataSharingDiscrepencies
audience: Application User
ms.reviewer: margoc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 784a925fa06148cad780b494c88b9a7af1809c9d
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/15/2019
ms.locfileid: "1551023"
---
# <a name="configure-financial-cross-company-data-sharing"></a><span data-ttu-id="1245d-103">Konfigurace sdílení finančních dat mezi společnostmi</span><span class="sxs-lookup"><span data-stu-id="1245d-103">Configure financial cross-company data sharing</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="1245d-104">Tento postup popisuje, jak nakonfigurovat, povolit, ověřit a vyřešit konflikty při sdílení dat mezi společnostmi.</span><span class="sxs-lookup"><span data-stu-id="1245d-104">This procedure shows how to configure, enable, validate, and resolve conflicts when sharing data between companies.</span></span> <span data-ttu-id="1245d-105">Použije společnost USMF a šablonu sdílení finančních dat.</span><span class="sxs-lookup"><span data-stu-id="1245d-105">It uses the USMF company and the Financial data sharing template.</span></span>



<span data-ttu-id="1245d-106">Tento průvodce úkolem vyžaduje platformu Dynamics AX 7.1 nebo novější.</span><span class="sxs-lookup"><span data-stu-id="1245d-106">This task guide requires Dynamics AX platform 7.1 or later.</span></span>

1. <span data-ttu-id="1245d-107">Přejděte do nabídky Správa systému > Pracovní prostory > Správa dat.</span><span class="sxs-lookup"><span data-stu-id="1245d-107">Go to System administration > Workspaces > Data management.</span></span>
2. <span data-ttu-id="1245d-108">Klepněte na tlačítko Importovat.</span><span class="sxs-lookup"><span data-stu-id="1245d-108">Click Import.</span></span>
3. <span data-ttu-id="1245d-109">Zadejte hodnotu do pole Název.</span><span class="sxs-lookup"><span data-stu-id="1245d-109">In the Name field, type a value.</span></span>
4. <span data-ttu-id="1245d-110">V poli Formát dat zdroje vyberte typ balíčku.</span><span class="sxs-lookup"><span data-stu-id="1245d-110">In the Source data format field, select the Package type.</span></span>
    * <span data-ttu-id="1245d-111">Klepněte na položku Odeslat.</span><span class="sxs-lookup"><span data-stu-id="1245d-111">Click Upload.</span></span> <span data-ttu-id="1245d-112">Přejděte k umístění souboru s balíčkem šablony pro sdílení finančních dat a vyberte soubor.</span><span class="sxs-lookup"><span data-stu-id="1245d-112">Navigate to the location of the Financial data sharing template package file and select that file.</span></span>  
5. <span data-ttu-id="1245d-113">Klikněte na položku Uložit.</span><span class="sxs-lookup"><span data-stu-id="1245d-113">Click Save.</span></span>
6. <span data-ttu-id="1245d-114">Označte v seznamu vybraný řádek.</span><span class="sxs-lookup"><span data-stu-id="1245d-114">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="1245d-115">Vyberte zásady sdílení dat, které jste právě vytvořili.</span><span class="sxs-lookup"><span data-stu-id="1245d-115">Select the data sharing policy that was just created.</span></span>  
7. <span data-ttu-id="1245d-116">Klepněte na tlačítko Importovat.</span><span class="sxs-lookup"><span data-stu-id="1245d-116">Click Import.</span></span>
8. <span data-ttu-id="1245d-117">Klikněte na tlačítko Zavřít.</span><span class="sxs-lookup"><span data-stu-id="1245d-117">Click Close.</span></span>
9. <span data-ttu-id="1245d-118">Aktualizujte stránku.</span><span class="sxs-lookup"><span data-stu-id="1245d-118">Refresh the page.</span></span>
10. <span data-ttu-id="1245d-119">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="1245d-119">Close the page.</span></span>
11. <span data-ttu-id="1245d-120">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="1245d-120">Close the page.</span></span>
12. <span data-ttu-id="1245d-121">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="1245d-121">Close the page.</span></span>
13. <span data-ttu-id="1245d-122">Přejděte na Správa systému > Nastavení > Konfigurovat sdílení dat mezi společnostmi.</span><span class="sxs-lookup"><span data-stu-id="1245d-122">Go to System administration > Setup > Configure cross-company data sharing.</span></span>
14. <span data-ttu-id="1245d-123">V seznamu vyhledejte a vyberte Dny platby.</span><span class="sxs-lookup"><span data-stu-id="1245d-123">In the list, find and select Payment days.</span></span>
15. <span data-ttu-id="1245d-124">Klepněte na možnost Přidat.</span><span class="sxs-lookup"><span data-stu-id="1245d-124">Click Add.</span></span>
16. <span data-ttu-id="1245d-125">Označte v seznamu vybraný řádek.</span><span class="sxs-lookup"><span data-stu-id="1245d-125">In the list, mark the selected row.</span></span>
17. <span data-ttu-id="1245d-126">Zadejte hodnotu USSI do pole Společnost.</span><span class="sxs-lookup"><span data-stu-id="1245d-126">In the Company field, type 'USSI'.</span></span>
18. <span data-ttu-id="1245d-127">Klepněte na možnost Přidat.</span><span class="sxs-lookup"><span data-stu-id="1245d-127">Click Add.</span></span>
19. <span data-ttu-id="1245d-128">Zadejte hodnotu USMF do pole Společnost.</span><span class="sxs-lookup"><span data-stu-id="1245d-128">In the Company field, type 'USMF'.</span></span>
20. <span data-ttu-id="1245d-129">Klikněte na položku Uložit.</span><span class="sxs-lookup"><span data-stu-id="1245d-129">Click Save.</span></span>
21. <span data-ttu-id="1245d-130">Klikněte na tlačítko Povolit.</span><span class="sxs-lookup"><span data-stu-id="1245d-130">Click Enable.</span></span>
22. <span data-ttu-id="1245d-131">Klepněte na tlačítko Ano.</span><span class="sxs-lookup"><span data-stu-id="1245d-131">Click Yes.</span></span>
23. <span data-ttu-id="1245d-132">Klikněte na Vyhledat potíže se sdílením.</span><span class="sxs-lookup"><span data-stu-id="1245d-132">Click Find sharing issues.</span></span>
24. <span data-ttu-id="1245d-133">Klepněte na tlačítko Ano.</span><span class="sxs-lookup"><span data-stu-id="1245d-133">Click Yes.</span></span>
25. <span data-ttu-id="1245d-134">Klikněte na Aktualizovat hodnotu pole</span><span class="sxs-lookup"><span data-stu-id="1245d-134">Click Update field value.</span></span>
26. <span data-ttu-id="1245d-135">Klikněte na Použít hodnotu pro společnost 1.</span><span class="sxs-lookup"><span data-stu-id="1245d-135">Click Use value from company 1.</span></span>
27. <span data-ttu-id="1245d-136">Aktualizujte stránku.</span><span class="sxs-lookup"><span data-stu-id="1245d-136">Refresh the page.</span></span>
28. <span data-ttu-id="1245d-137">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="1245d-137">Close the page.</span></span>

