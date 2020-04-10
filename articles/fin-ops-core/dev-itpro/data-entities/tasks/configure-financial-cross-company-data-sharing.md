---
title: Konfigurace sdílení finančních dat mezi společnostmi
description: Tento postup popisuje, jak nakonfigurovat, povolit, ověřit a vyřešit konflikty při sdílení dat mezi společnostmi.
author: aprilolson
manager: AnnBe
ms.date: 06/26/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DataManagementWorkspace, DMFQuickImportExportRnr, DMFExecutionHistoryWorkspace, DMFExecutionHistorySummary, DMFExecutionHistoryEntities,  SysDataSharingConfiguration, SysDataSharingDiscrepencies
audience: Application User
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 98eeae9f50238aae172e4a217d40be39ee46a0b8
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/18/2020
ms.locfileid: "3142954"
---
# <a name="configure-financial-cross-company-data-sharing"></a><span data-ttu-id="8ae9c-103">Konfigurace sdílení finančních dat mezi společnostmi</span><span class="sxs-lookup"><span data-stu-id="8ae9c-103">Configure financial cross-company data sharing</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="8ae9c-104">Tento postup popisuje, jak nakonfigurovat, povolit, ověřit a vyřešit konflikty při sdílení dat mezi společnostmi.</span><span class="sxs-lookup"><span data-stu-id="8ae9c-104">This procedure shows how to configure, enable, validate, and resolve conflicts when sharing data between companies.</span></span> <span data-ttu-id="8ae9c-105">Použije společnost USMF a šablonu sdílení finančních dat.</span><span class="sxs-lookup"><span data-stu-id="8ae9c-105">It uses the USMF company and the Financial data sharing template.</span></span>

<span data-ttu-id="8ae9c-106">Tento průvodce úkolem vyžaduje platformu Dynamics AX 7.1 nebo novější.</span><span class="sxs-lookup"><span data-stu-id="8ae9c-106">This task guide requires Dynamics AX platform 7.1 or later.</span></span>

1. <span data-ttu-id="8ae9c-107">Přejděte do **navigačního podokna > Moduly > Správa systému > Pracovní prostory > Správa dat**.</span><span class="sxs-lookup"><span data-stu-id="8ae9c-107">Go to **Navigation pane > Modules > System administration > Workspaces > Data management**.</span></span>
2. <span data-ttu-id="8ae9c-108">Klikněte na **Importovat**.</span><span class="sxs-lookup"><span data-stu-id="8ae9c-108">Click **Import**.</span></span>
3. <span data-ttu-id="8ae9c-109">Zadejte hodnotu do pole **Název**.</span><span class="sxs-lookup"><span data-stu-id="8ae9c-109">In the **Name** field, type a value.</span></span>
4. <span data-ttu-id="8ae9c-110">V poli **Formát dat zdroje** vyberte typ ‚balíčku‘.</span><span class="sxs-lookup"><span data-stu-id="8ae9c-110">In the **Source data format** field, select the 'Package' type.</span></span> <span data-ttu-id="8ae9c-111">Klepněte na položku **Odeslat**.</span><span class="sxs-lookup"><span data-stu-id="8ae9c-111">Click **Upload**.</span></span> <span data-ttu-id="8ae9c-112">Přejděte k umístění souboru s balíčkem šablony pro sdílení finančních dat a vyberte soubor.</span><span class="sxs-lookup"><span data-stu-id="8ae9c-112">Navigate to the location of the Financial data sharing template package file and select that file.</span></span>
5. <span data-ttu-id="8ae9c-113">Klikněte na možnost **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="8ae9c-113">Click **Save**.</span></span>
6. <span data-ttu-id="8ae9c-114">Označte v seznamu vybraný řádek.</span><span class="sxs-lookup"><span data-stu-id="8ae9c-114">In the list, mark the selected row.</span></span> <span data-ttu-id="8ae9c-115">Vyberte zásady sdílení dat, které jste právě vytvořili.</span><span class="sxs-lookup"><span data-stu-id="8ae9c-115">Select the data sharing policy that was just created.</span></span>  
7. <span data-ttu-id="8ae9c-116">Klikněte na **Importovat**.</span><span class="sxs-lookup"><span data-stu-id="8ae9c-116">Click **Import**.</span></span>
8. <span data-ttu-id="8ae9c-117">Klepněte na tlačítko **Zavřít**.</span><span class="sxs-lookup"><span data-stu-id="8ae9c-117">Click **Close**.</span></span>
9. <span data-ttu-id="8ae9c-118">Aktualizujte stránku.</span><span class="sxs-lookup"><span data-stu-id="8ae9c-118">Refresh the page.</span></span>
10. <span data-ttu-id="8ae9c-119">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="8ae9c-119">Close the page.</span></span>
11. <span data-ttu-id="8ae9c-120">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="8ae9c-120">Close the page.</span></span>
12. <span data-ttu-id="8ae9c-121">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="8ae9c-121">Close the page.</span></span>
13. <span data-ttu-id="8ae9c-122">Přejděte na **Navigační podokno > Moduly > Správa systému > Nastavení > Konfigurovat sdílení dat mezi společnostmi**.</span><span class="sxs-lookup"><span data-stu-id="8ae9c-122">Go to **Navigation pane > Modules > System administration > Setup > Configure cross-company data sharing**.</span></span>
14. <span data-ttu-id="8ae9c-123">V seznamu vyhledejte a vyberte **Dny platby**.</span><span class="sxs-lookup"><span data-stu-id="8ae9c-123">In the list, find and select **Payment days**.</span></span>
15. <span data-ttu-id="8ae9c-124">Klikněte na tlačítko **Přidat**.</span><span class="sxs-lookup"><span data-stu-id="8ae9c-124">Click **Add**.</span></span>
16. <span data-ttu-id="8ae9c-125">Označte v seznamu vybraný řádek.</span><span class="sxs-lookup"><span data-stu-id="8ae9c-125">In the list, mark the selected row.</span></span>
17. <span data-ttu-id="8ae9c-126">Zadejte hodnotu USSI do pole **Společnost**.</span><span class="sxs-lookup"><span data-stu-id="8ae9c-126">In the **Company** field, type 'USSI'.</span></span>
18. <span data-ttu-id="8ae9c-127">Klikněte na tlačítko **Přidat**.</span><span class="sxs-lookup"><span data-stu-id="8ae9c-127">Click **Add**.</span></span>
19. <span data-ttu-id="8ae9c-128">Zadejte hodnotu USMF do pole **Společnost**.</span><span class="sxs-lookup"><span data-stu-id="8ae9c-128">In the **Company** field, type 'USMF'.</span></span>
20. <span data-ttu-id="8ae9c-129">Klikněte na možnost **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="8ae9c-129">Click **Save**.</span></span>
21. <span data-ttu-id="8ae9c-130">Klikněte na tlačítko **Povolit**.</span><span class="sxs-lookup"><span data-stu-id="8ae9c-130">Click **Enable**.</span></span>
22. <span data-ttu-id="8ae9c-131">Klepněte na tlačítko **Ano**.</span><span class="sxs-lookup"><span data-stu-id="8ae9c-131">Click **Yes**.</span></span>
23. <span data-ttu-id="8ae9c-132">Klikněte na **Vyhledat potíže se sdílením**.</span><span class="sxs-lookup"><span data-stu-id="8ae9c-132">Click **Find sharing issues**.</span></span>
24. <span data-ttu-id="8ae9c-133">Klepněte na tlačítko **Ano**.</span><span class="sxs-lookup"><span data-stu-id="8ae9c-133">Click **Yes**.</span></span>
25. <span data-ttu-id="8ae9c-134">Klikněte na **Aktualizovat hodnotu pole**.</span><span class="sxs-lookup"><span data-stu-id="8ae9c-134">Click **Update field value**.</span></span>
26. <span data-ttu-id="8ae9c-135">Klikněte na **Použít hodnotu pro společnost 1**.</span><span class="sxs-lookup"><span data-stu-id="8ae9c-135">Click **Use value from company 1**.</span></span>
27. <span data-ttu-id="8ae9c-136">Aktualizujte stránku.</span><span class="sxs-lookup"><span data-stu-id="8ae9c-136">Refresh the page.</span></span>
28. <span data-ttu-id="8ae9c-137">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="8ae9c-137">Close the page.</span></span>

