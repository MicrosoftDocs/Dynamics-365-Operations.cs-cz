---
title: Export dat dceřiných společností do souborů
description: Toto téma vysvětluje, jak připravit export dat z aplikace Microsoft Dynamics 365 Finance a poté je importovat do konsolidované právnické osoby.
author: jinniew
manager: AnnBe
ms.date: 10/09/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: jiwo
ms.search.validFrom: 2018-5-31
ms.dyn365.ops.version: 8.0.1
ms.openlocfilehash: 33c17cc2c1dcaa57244bf0bfaa661b11b221e2f6
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/15/2021
ms.locfileid: "5205492"
---
# <a name="export-subsidiary-data-to-files"></a><span data-ttu-id="93262-103">Export dat dceřiných společností do souborů</span><span class="sxs-lookup"><span data-stu-id="93262-103">Export subsidiary data to files</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="93262-104">Stránka **Export** (**Správa systému \> Pracovní prostory \> Import/export**) slouží k přípravě exportu dat dceřiných společností do souborů, které lze poté importovat do konsolidované právnické osoby.</span><span class="sxs-lookup"><span data-stu-id="93262-104">You use the **Export** page (**System administration \> Workspaces \> Import/Export**) to prepare to export subsidiary data to files that can then be imported into a consolidated legal entity.</span></span> <span data-ttu-id="93262-105">Další informace o importu a exportu naleznete v tématu [Přehled úloh importu a exportu dat](../../fin-ops-core/dev-itpro/data-entities/data-import-export-job.md).</span><span class="sxs-lookup"><span data-stu-id="93262-105">For more information about the import and export processes, see [Data import and export jobs overview](../../fin-ops-core/dev-itpro/data-entities/data-import-export-job.md).</span></span>

1. <span data-ttu-id="93262-106">Vytvořte právnickou osobu pro proces konsolidace.</span><span class="sxs-lookup"><span data-stu-id="93262-106">Create a legal entity for the consolidation process.</span></span> <span data-ttu-id="93262-107">Další informace, jak vytvořit právnické osoby, najdete v části [Vytvoření právnícké osoby](../../fin-ops-core/fin-ops/organization-administration/tasks/create-legal-entity.md).</span><span class="sxs-lookup"><span data-stu-id="93262-107">For information about how to create legal entities, see [Create a legal entity](../../fin-ops-core/fin-ops/organization-administration/tasks/create-legal-entity.md).</span></span> <span data-ttu-id="93262-108">Další informace viz [Připrava právnické osoby pro použití v procesu konsolidace](prepare-company-for-consolidation.md) a [Založení dceřiné právnické osoby ke konsolidaci](set-up-subsidiary-company-for-consolidation.md).</span><span class="sxs-lookup"><span data-stu-id="93262-108">For more information, see [Prepare a legal entity for use in the consolidation process](prepare-company-for-consolidation.md) and [Set up a subsidiary legal entity for consolidation](set-up-subsidiary-company-for-consolidation.md).</span></span> 

2. <span data-ttu-id="93262-109">Přejděte na **Konsolidace \> Export zůstatků společnosti**.</span><span class="sxs-lookup"><span data-stu-id="93262-109">Go to **Consolidations \> Export company balances**.</span></span> <span data-ttu-id="93262-110">Na stránce **Export zůstatků společnosti** na kartě **Kritéria** zadejte podrobnosti konsolidace nastavením následujících polí.</span><span class="sxs-lookup"><span data-stu-id="93262-110">On the **Export company balances** page, on the **Criteria** tab, specify the details of the consolidation by setting the following fields.</span></span>

    | <span data-ttu-id="93262-111">Pole</span><span class="sxs-lookup"><span data-stu-id="93262-111">Field</span></span>                             | <span data-ttu-id="93262-112">popis</span><span class="sxs-lookup"><span data-stu-id="93262-112">Description</span></span> |
    |-----------------------------------|-------|
    | <span data-ttu-id="93262-113">Hlavní účet</span><span class="sxs-lookup"><span data-stu-id="93262-113">Main account</span></span>                      | <span data-ttu-id="93262-114">Určete účty, které chcete konsolidovat.</span><span class="sxs-lookup"><span data-stu-id="93262-114">Specify the accounts to consolidate.</span></span> <span data-ttu-id="93262-115">Chcete-li zahrnout všechny účty, nechte toto pole prázdné.</span><span class="sxs-lookup"><span data-stu-id="93262-115">To include all accounts, leave this field blank.</span></span> |
    | <span data-ttu-id="93262-116">Použití konsolidačního účtu</span><span class="sxs-lookup"><span data-stu-id="93262-116">Use consolidation account</span></span>         | <span data-ttu-id="93262-117">Pokud jste zadali konsolidační účty, nastavte tuto možnost na **Ano**.</span><span class="sxs-lookup"><span data-stu-id="93262-117">If you've specified consolidation accounts, set this option to **Yes**.</span></span> |
    | <span data-ttu-id="93262-118">Vybrat konsolidační účet z</span><span class="sxs-lookup"><span data-stu-id="93262-118">Select consolidation account from</span></span> | <span data-ttu-id="93262-119">Vyberte **Hlavní účet** nebo **Skupina konsolidačních účtů**.</span><span class="sxs-lookup"><span data-stu-id="93262-119">Select either **Main account** or **Consolidation account group**.</span></span> |
    | <span data-ttu-id="93262-120">Skupina konsolidačních účtů</span><span class="sxs-lookup"><span data-stu-id="93262-120">Consolidation account group</span></span>       | <span data-ttu-id="93262-121">Vyberte skupinu konsolidačních účtů pro konsolidační účet, který jste vybrali.</span><span class="sxs-lookup"><span data-stu-id="93262-121">Select a consolidation account group for the consolidation account that you selected.</span></span> |
    | <span data-ttu-id="93262-122">Období konsolidace</span><span class="sxs-lookup"><span data-stu-id="93262-122">Consolidation period</span></span>              | <span data-ttu-id="93262-123">Pro konsolidaci zadejte data „od“ a „do“.</span><span class="sxs-lookup"><span data-stu-id="93262-123">Specify "from" and "to" dates for the consolidation.</span></span> |
    | <span data-ttu-id="93262-124">Zahrnout skutečné částky</span><span class="sxs-lookup"><span data-stu-id="93262-124">Include actual amounts</span></span>            | <span data-ttu-id="93262-125">Tuto možnost nastavte na **Ano**, chcete-li zahrnout skutečné částky.</span><span class="sxs-lookup"><span data-stu-id="93262-125">Set this option to **Yes** to include actual amounts.</span></span> |
    | <span data-ttu-id="93262-126">Zahrnout rozpočtové částky</span><span class="sxs-lookup"><span data-stu-id="93262-126">Include budget amounts</span></span>            | <span data-ttu-id="93262-127">Tuto možnost nastavte na **Ano**, chcete-li zahrnout částky rozpočtu do konsolidací.</span><span class="sxs-lookup"><span data-stu-id="93262-127">Set this option to **Yes** to include budget amounts in consolidations.</span></span> |
    | <span data-ttu-id="93262-128">Rozpočtové modely</span><span class="sxs-lookup"><span data-stu-id="93262-128">Budget models</span></span>                     | <span data-ttu-id="93262-129">Zadejte rozpočtový model, který chcete zahrnout.</span><span class="sxs-lookup"><span data-stu-id="93262-129">Specify the budget model to include.</span></span> |

3. <span data-ttu-id="93262-130">Na kartě **Finanční dimenze** upřesněte podrobnosti konsolidace:</span><span class="sxs-lookup"><span data-stu-id="93262-130">On the **Financial dimensions** tab, specify the details of the consolidation:</span></span>

    - <span data-ttu-id="93262-131">Upřesněte informace o finanční dimenzi, které se mají převést z transakcí v účtech dceřiné společnosti do transakcí v konsolidovaném právním subjektu.</span><span class="sxs-lookup"><span data-stu-id="93262-131">Specify the financial dimension information that should be transferred from the transactions in the subsidiary accounts to the transactions in the consolidated legal entity.</span></span>
    - <span data-ttu-id="93262-132">Vyberte finanční dimenze v seznamu.</span><span class="sxs-lookup"><span data-stu-id="93262-132">Select financial dimensions in the list.</span></span>
    - <span data-ttu-id="93262-133">Určete správnou specifikaci pro každou finanční dimenzi, která je konsolidována.</span><span class="sxs-lookup"><span data-stu-id="93262-133">Identify the correct specification for each financial dimension that is consolidated.</span></span> <span data-ttu-id="93262-134">Dostupné možnosti zahrnují **Dimenze**, **Skupinová dimenze**, **Firemní účty** a **Účet**.</span><span class="sxs-lookup"><span data-stu-id="93262-134">The available options include **Dimension**, **Group dimension**, **Company accounts**, and **Account**.</span></span>

        > [!NOTE]
        > <span data-ttu-id="93262-135">Možnost **Skupinová dimenze** umožňuje definovat hodnotu dimenze, kterou používá skupina společností, která se konsoliduje.</span><span class="sxs-lookup"><span data-stu-id="93262-135">The **Group dimension** option lets you define the dimension value that is used by the group of companies that is being consolidated.</span></span>

    - <span data-ttu-id="93262-136">Určete pořadí segmentů, do kterých chcete konsolidovat.</span><span class="sxs-lookup"><span data-stu-id="93262-136">Specify the segment order to consolidate in.</span></span>

4. <span data-ttu-id="93262-137">Na kartě **Právnické osoby** pomocí těchto pokynů zadejte právnickou osobu, kterou exportujete:</span><span class="sxs-lookup"><span data-stu-id="93262-137">On the **Legal entities** tab, follow these steps to specify the legal entity that you're exporting:</span></span>

    1. <span data-ttu-id="93262-138">Zvolte **Nové**.</span><span class="sxs-lookup"><span data-stu-id="93262-138">Select **New**.</span></span>
    2. <span data-ttu-id="93262-139">Do pole **Zdrojová právnická osoba** zadejte právnickou osobu.</span><span class="sxs-lookup"><span data-stu-id="93262-139">In the **Source legal entity** field, enter the legal entity.</span></span>

        <span data-ttu-id="93262-140">Jestliže lze stejná kritéria použít pro několik dceřiných společností ve stejné databázi, můžete v rámci jedné operace přenést data z těchto dceřiných společností do oddělených souborů pro export:</span><span class="sxs-lookup"><span data-stu-id="93262-140">If the same criteria apply to several subsidiaries that are in the same database, you can transfer data from those subsidiaries to separate export files in a single operation:</span></span>

        1. <span data-ttu-id="93262-141">Vytvořte řádek pro každou dceřinou právnickou osobu, jejíž účty budou exportovány do souborů.</span><span class="sxs-lookup"><span data-stu-id="93262-141">Create a line for each subsidiary legal entity for which accounts should be exported to files.</span></span> <span data-ttu-id="93262-142">Tyto soubory budou importovány do konsolidované právnické osoby později.</span><span class="sxs-lookup"><span data-stu-id="93262-142">These files will be imported into the consolidated legal entity later.</span></span>
        2. <span data-ttu-id="93262-143">Pro každou dceřinou společnost zadejte název. Dále zadejte název exportního souboru, který bude vytvořen v průběhu exportní úlohy.</span><span class="sxs-lookup"><span data-stu-id="93262-143">For each subsidiary, enter the subsidiary name and the name of the export file that will be created during the export job.</span></span>

    3. <span data-ttu-id="93262-144">V poli **Typ účtu pro rozdíly převodu** vyberte **Zisky a ztráty** nebo **Rozvaha**.</span><span class="sxs-lookup"><span data-stu-id="93262-144">In **Account type of conversion differences** field, Select **Profit and loss** or **Balance sheet**.</span></span>
    4. <span data-ttu-id="93262-145">Zadejte název souboru pro exportovaný soubor, který bude vytvořen.</span><span class="sxs-lookup"><span data-stu-id="93262-145">Enter a file name for the export file that will be created.</span></span>

5. <span data-ttu-id="93262-146">Tlačítkem **OK** spustíte export.</span><span class="sxs-lookup"><span data-stu-id="93262-146">Select **OK** to run the export.</span></span>

<span data-ttu-id="93262-147">Po dokončení exportu se zobrazí zpráva s počtem záznamů uložených do každého souboru.</span><span class="sxs-lookup"><span data-stu-id="93262-147">When the export is completed, you receive a message that shows the number of records that were saved in each file.</span></span> <span data-ttu-id="93262-148">Soubory pak můžete importovat do konsolidované právnické osoby.</span><span class="sxs-lookup"><span data-stu-id="93262-148">You can then import the files into the consolidated legal entity.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]