---
title: Archivace skladových transakcí
description: Toto téma popisuje, jak archivovat data skladových transakcí za účelem zlepšení výkonu systému.
author: sherry-zheng
manager: tfehr
ms.date: 03/01/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventTransArchiveProcessForm
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2021-03-01
ms.dyn365.ops.version: Release 10.0.18
ms.openlocfilehash: 3a0fa65eb728e4ce96bdfc3f7a0f04901551ccea
ms.sourcegitcommit: 70b1567d316f19c15a4b032b4897f15c8dcdca09
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/08/2021
ms.locfileid: "5556409"
---
# <a name="archive-inventory-transactions"></a><span data-ttu-id="a45e7-103">Archivace skladových transakcí</span><span class="sxs-lookup"><span data-stu-id="a45e7-103">Archive inventory transactions</span></span>

[!include [banner](../../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

<span data-ttu-id="a45e7-104">V průběhu času bude tabulka skladových transakcí (`InventTrans`) i nadále růst a zabírat více prostoru v databázi.</span><span class="sxs-lookup"><span data-stu-id="a45e7-104">Over time, the inventory transactions table (`InventTrans`) will continue to grow and consume more database space.</span></span> <span data-ttu-id="a45e7-105">Proto se dotazy spouštěné proti této tabulce postupně zpomalí.</span><span class="sxs-lookup"><span data-stu-id="a45e7-105">Therefore, queries that are made against the table will gradually become slower.</span></span> <span data-ttu-id="a45e7-106">Toto téma popisuje, jak můžete používat funkci *Archivace skladových transakcí* pro archivaci dat o skladových transakcích, která pomůže zlepšit výkon systému.</span><span class="sxs-lookup"><span data-stu-id="a45e7-106">This topic describes how you can use the *Inventory transactions archive* feature to archive data about inventory transactions to help improve system performance.</span></span>

> [!NOTE]
> <span data-ttu-id="a45e7-107">Ve vybraném uzavřeném období hlavní knihy lze archivovat pouze finančně aktualizované skladové transakce.</span><span class="sxs-lookup"><span data-stu-id="a45e7-107">Only financially updated inventory transactions can be archived in a selected closed ledger period.</span></span> <span data-ttu-id="a45e7-108">Finančně aktualizované odchozí skladové transakce, které chcete archivovat, musejí mít stav výdeje s hodnotou *Prodáno*, a příchozí skladové transakce musejí mít stav přijetí *Zakoupeno*.</span><span class="sxs-lookup"><span data-stu-id="a45e7-108">To be archived, financially updated outbound inventory transactions must have an issue status of *Sold*, and inbound inventory transactions must have a receipt status of *Purchased*.</span></span>

<span data-ttu-id="a45e7-109">Když archivujete skladové transakce, všechny související transakce se přesunou do tabulky `InventTransArchive`.</span><span class="sxs-lookup"><span data-stu-id="a45e7-109">When you archive inventory transactions, all related transactions are moved to the `InventTransArchive` table.</span></span> <span data-ttu-id="a45e7-110">Transakce výdeje ze skladu a transakce příjmu na sklad se archivují samostatně na základě kombinace ID položky (`itemId`) a ID dimenze zásob (`inventDimId`), a jsou vloženy do transakcí souhrnného výdeje a souhrnných příjmů.</span><span class="sxs-lookup"><span data-stu-id="a45e7-110">Inventory issue transactions and inventory receipt transactions are archived separately, based on the combination of the item ID (`itemId`) and inventory dimension ID (`inventDimId`), and they are put into the summarized issue and summarized receipt transactions.</span></span>

<span data-ttu-id="a45e7-111">Když kombinace `itemId` a `inventDimId` obsahuje pouze jednu transakci příjmu nebo výdeje, transakce nebude archivována.</span><span class="sxs-lookup"><span data-stu-id="a45e7-111">If an `itemId` and `inventDimId` combination contains only one receipt or issue transaction, the transaction won't be archived.</span></span>

## <a name="turn-on-the-feature-in-your-system"></a><span data-ttu-id="a45e7-112">Zapnutí funkce ve vašem systému</span><span class="sxs-lookup"><span data-stu-id="a45e7-112">Turn on the feature in your system</span></span>

<span data-ttu-id="a45e7-113">Pokud váš systém ještě neobsahuje funkce popsané v tomto tématu, přejděte na stránku [Správa funkcí](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) a zapněte funkci *Archivace skladových transakcí*.</span><span class="sxs-lookup"><span data-stu-id="a45e7-113">If your system doesn't already include the features that is described in this topic, go to [Feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md), and turn on the *Inventory transactions archive* feature.</span></span>

## <a name="things-to-consider-before-you-archive-inventory-transactions"></a><span data-ttu-id="a45e7-114">Co je třeba zvážit před archivací skladových transakcí</span><span class="sxs-lookup"><span data-stu-id="a45e7-114">Things to consider before you archive inventory transactions</span></span>

<span data-ttu-id="a45e7-115">Před archivací skladových transakcí byste měli zvážit následující obchodní scénáře, protože budou touto operací ovlivněny:</span><span class="sxs-lookup"><span data-stu-id="a45e7-115">Before you archive inventory transactions, you should consider the following business scenarios, because they will be affected by the operation:</span></span>

- <span data-ttu-id="a45e7-116">Když auditujete skladové transakce ze souvisejících dokumentů, jako jsou řádky nákupní objednávky, zobrazí se jako archivované.</span><span class="sxs-lookup"><span data-stu-id="a45e7-116">When you audit inventory transactions from related documents, such as purchase order lines, they will be shown as archived.</span></span> <span data-ttu-id="a45e7-117">Chcete-li zkontrolovat archivované transakce, musíte přejít do nabídky **Řízení zásob \> Pravidelné úkoly \> Vyčistit \> Archivace skladových transakcí**.</span><span class="sxs-lookup"><span data-stu-id="a45e7-117">To review the archived transactions, you must go to **Inventory management \> Periodic tasks \> Clean up \> Inventory transactions archive**.</span></span>
- <span data-ttu-id="a45e7-118">Uzávěrku skladu nelze zrušit pro archivovaná období.</span><span class="sxs-lookup"><span data-stu-id="a45e7-118">Inventory closing can't be canceled for archived periods.</span></span> <span data-ttu-id="a45e7-119">Než budete moci zrušit uzávěrku inventáře, musíte stornovat archivaci skladových transakcí pro příslušné období.</span><span class="sxs-lookup"><span data-stu-id="a45e7-119">Before you can cancel an inventory closing, you must reverse the inventory transaction archive for the relevant period.</span></span>
- <span data-ttu-id="a45e7-120">Standardní konverzi nákladů nelze provést pro archivovaná období.</span><span class="sxs-lookup"><span data-stu-id="a45e7-120">Standard cost conversion can't be done for archived periods.</span></span> <span data-ttu-id="a45e7-121">Než budete moci provést standardní konverzi nákladů, musíte stornovat archivaci skladových transakcí pro příslušné období.</span><span class="sxs-lookup"><span data-stu-id="a45e7-121">Before you can do standard cost conversion, you must reverse the inventory transaction archive for the relevant period.</span></span>
- <span data-ttu-id="a45e7-122">Sestavy zásob, které vycházejí ze skladových transakcí, budou při archivaci skladových transakcí ovlivněny.</span><span class="sxs-lookup"><span data-stu-id="a45e7-122">Inventory reports that are sourced from inventory transactions will be affected when you archive inventory transactions.</span></span> <span data-ttu-id="a45e7-123">Mezi tyto sestavy patří sestava prodlení zásob a sestavy hodnoty skladu.</span><span class="sxs-lookup"><span data-stu-id="a45e7-123">These reports include the inventory aging report and inventory value reports.</span></span>
- <span data-ttu-id="a45e7-124">Prognózy zásob mohou být ovlivněny, pokud jsou spuštěny v časovém horizontu archivovaných období.</span><span class="sxs-lookup"><span data-stu-id="a45e7-124">Inventory forecasts might be affected if they are run during the time horizon of archived periods.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="a45e7-125">Předpoklady</span><span class="sxs-lookup"><span data-stu-id="a45e7-125">Prerequisites</span></span>

<span data-ttu-id="a45e7-126">Skladové transakce lze archivovat pouze během období, kdy jsou splněny následující podmínky:</span><span class="sxs-lookup"><span data-stu-id="a45e7-126">Inventory transactions can be archived only during periods where the following conditions are met:</span></span>

- <span data-ttu-id="a45e7-127">Období hlavní knihy musí být uzavřeno.</span><span class="sxs-lookup"><span data-stu-id="a45e7-127">The ledger period must be closed.</span></span>
- <span data-ttu-id="a45e7-128">Uzávěrka zásob musí být spuštěna k datu archivu Období do nebo po něm.</span><span class="sxs-lookup"><span data-stu-id="a45e7-128">Inventory closing must be run on or after the to-period date of the archive.</span></span>
- <span data-ttu-id="a45e7-129">Období musí být nejméně jeden rok před datem archivu Období od.</span><span class="sxs-lookup"><span data-stu-id="a45e7-129">The period must be at least one year before the from-period date of the archive.</span></span>
- <span data-ttu-id="a45e7-130">Nesmí existovat žádné stávající přepočty skladu.</span><span class="sxs-lookup"><span data-stu-id="a45e7-130">There must not be any existing inventory recalculations.</span></span>

## <a name="archive-inventory-transactions"></a><span data-ttu-id="a45e7-131">Archivace skladových transakcí</span><span class="sxs-lookup"><span data-stu-id="a45e7-131">Archive inventory transactions</span></span>

<span data-ttu-id="a45e7-132">Chcete-li archivovat skladové transakce, postupujte takto.</span><span class="sxs-lookup"><span data-stu-id="a45e7-132">To archive inventory transactions, follow these steps.</span></span>

1. <span data-ttu-id="a45e7-133">Přejděte do nabídky **Řízení zásob** \> **Pravidelné úkoly** \> **Vyčistit** \> **Archivace skladových transakcí**.</span><span class="sxs-lookup"><span data-stu-id="a45e7-133">Go to **Inventory management** \> **Periodic tasks** \> **Clean up** \> **Inventory transaction archive**.</span></span>

    <span data-ttu-id="a45e7-134">Zobrazí se stránka **Archivace skladových transakcí** se seznamem archivovaných záznamů procesu.</span><span class="sxs-lookup"><span data-stu-id="a45e7-134">The **Inventory transactions archive** page appears and shows a list of archived process records.</span></span>

    <span data-ttu-id="a45e7-135">![Stránka Archivace skladových transakcí](media/archive-inventory-empty.png "Stránka Archivace skladových transakcí")</span><span class="sxs-lookup"><span data-stu-id="a45e7-135">![Inventory transactions archive page](media/archive-inventory-empty.png "Inventory transactions archive page")</span></span>

1. <span data-ttu-id="a45e7-136">V podokně akcí vyberte příkaz **Archivace skladových transakcí** pro vytvoření archivu skladových transakcí.</span><span class="sxs-lookup"><span data-stu-id="a45e7-136">On the Action Pane, select **Inventory transactions archive** to create an inventory transaction archive.</span></span>
1. <span data-ttu-id="a45e7-137">V dialogovém okně **Archivace skladových transakcí** na záložce **Parametry** nastavte následující pole:</span><span class="sxs-lookup"><span data-stu-id="a45e7-137">In the **Inventory transactions archive** dialog box, on the **Parameters** FastTab, set the following fields:</span></span>

    - <span data-ttu-id="a45e7-138">**Od data v uzavřeném účetním období** - Vyberte nejstarší datum transakce, které chcete zahrnout do archivu.</span><span class="sxs-lookup"><span data-stu-id="a45e7-138">**From date in closed ledger period** – Select the earliest transaction date to include in the archive.</span></span>
    - <span data-ttu-id="a45e7-139">**Do data v uzavřeném účetním období** - Vyberte nejnovější datum transakce, které chcete zahrnout do archivu.</span><span class="sxs-lookup"><span data-stu-id="a45e7-139">**To date in closed ledger period** – Select the latest transaction date to include in the archive.</span></span>

    <span data-ttu-id="a45e7-140">![Dialogové okno Archivace skladových transakcí](media/archive-inventory-dates.png "Dialogové okno Archivace skladových transakcí")</span><span class="sxs-lookup"><span data-stu-id="a45e7-140">![Inventory transactions archive dialog box](media/archive-inventory-dates.png "Inventory transactions archive dialog box")</span></span>

    > [!NOTE]
    > <span data-ttu-id="a45e7-141">Vybrat bude možné pouze období, která splňují [předpoklady](#prerequisites).</span><span class="sxs-lookup"><span data-stu-id="a45e7-141">Only periods that meet the [prerequisites](#prerequisites) will be available for selection.</span></span>

1. <span data-ttu-id="a45e7-142">Na záložce **Spustit na pozadí** nastavte detaily dávkového zpracování podle potřeby.</span><span class="sxs-lookup"><span data-stu-id="a45e7-142">On the **Run in the background** FastTab, set up batch processing details as you require.</span></span> <span data-ttu-id="a45e7-143">Postupujte podle obvyklých kroků pro dávkové úlohy v Microsoftu Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="a45e7-143">Follow the usual steps for batch jobs in Microsoft Dynamics 365 Supply Chain Management.</span></span>
1. <span data-ttu-id="a45e7-144">Vyberte **OK**.</span><span class="sxs-lookup"><span data-stu-id="a45e7-144">Select **OK**.</span></span>
1. <span data-ttu-id="a45e7-145">Zobrazí se zpráva s výzvou k potvrzení, že chcete pokračovat.</span><span class="sxs-lookup"><span data-stu-id="a45e7-145">You receive a message that prompts you to confirm that you want to continue.</span></span> <span data-ttu-id="a45e7-146">Přečtěte si pozorně zprávu a poté vyberte **Ano**, pokud chcete pokračovat.</span><span class="sxs-lookup"><span data-stu-id="a45e7-146">Read the message carefully, and then select **Yes** if you want to continue.</span></span>

    <span data-ttu-id="a45e7-147">Zobrazí se zpráva, že vaše úloha archivace skladových transakcí byla přidána do fronty dávek.</span><span class="sxs-lookup"><span data-stu-id="a45e7-147">You receive a message that states that your inventory transactions archive job has been added to the batch queue.</span></span> <span data-ttu-id="a45e7-148">Úloha nyní začne archivovat skladové transakce od vybraného období.</span><span class="sxs-lookup"><span data-stu-id="a45e7-148">The job will now start to archive inventory transactions from the selected period.</span></span>

## <a name="view-archived-inventory-transactions"></a><span data-ttu-id="a45e7-149">Zobrazit archivované transakce zásob</span><span class="sxs-lookup"><span data-stu-id="a45e7-149">View archived inventory transactions</span></span>

<span data-ttu-id="a45e7-150">Stránka **Archivace skladových transakcí** zobrazuje vaši úplnou historii archivace.</span><span class="sxs-lookup"><span data-stu-id="a45e7-150">The **Inventory transactions archive** page shows your full archiving history.</span></span> <span data-ttu-id="a45e7-151">Každý řádek v mřížce zobrazuje informace, jako je datum vytvoření archivu, jméno uživatele, který jej vytvořil, a jeho stav.</span><span class="sxs-lookup"><span data-stu-id="a45e7-151">Each row in the grid shows information such as the date when the archive was created, the user who created it, and its status.</span></span>

<span data-ttu-id="a45e7-152">![Historie archivace na stránce Archivace skladových transakcí](media/archive-inventory-full.png "Historie archivace na stránce Archivace skladových transakcí")</span><span class="sxs-lookup"><span data-stu-id="a45e7-152">![Archiving history on the Inventory transactions archive page](media/archive-inventory-full.png "Archiving history on the Inventory transactions archive page")</span></span>

<span data-ttu-id="a45e7-153">Chcete-li filtrovat archivy zobrazené v mřížce, vyberte v rozevíracím seznamu v horní části stránky jednu z následujících hodnot:</span><span class="sxs-lookup"><span data-stu-id="a45e7-153">In the drop-down list at the top of the page select one of the following values to filter the archives that are shown in the grid:</span></span>

- <span data-ttu-id="a45e7-154">**Aktivní** – Zobrazí pouze aktivní archivy, nikoli stornované archivy.</span><span class="sxs-lookup"><span data-stu-id="a45e7-154">**Active** – Show only active archives, not reversed archives.</span></span>
- <span data-ttu-id="a45e7-155">**Vše** – Zobrazí všechny archivy, aktivní i stornované.</span><span class="sxs-lookup"><span data-stu-id="a45e7-155">**All** – Show all archives, both active and reversed.</span></span>

<span data-ttu-id="a45e7-156">U každého archivu v mřížce jsou k dispozici následující informace:</span><span class="sxs-lookup"><span data-stu-id="a45e7-156">For each archive in the grid, the following information is provided:</span></span>

- <span data-ttu-id="a45e7-157">**Aktivní** – Zaškrtnutí označuje, že archiv je aktivní.</span><span class="sxs-lookup"><span data-stu-id="a45e7-157">**Active** – A check mark indicates that the archive is active.</span></span>
- <span data-ttu-id="a45e7-158">**Od data** – Datum nejstarší transakce, kterou lze zahrnout do archivu.</span><span class="sxs-lookup"><span data-stu-id="a45e7-158">**From date** – The date of the oldest transaction that can be included in the archive.</span></span>
- <span data-ttu-id="a45e7-159">**Do data** – Datum nejnovější transakce, kterou lze zahrnout do archivu.</span><span class="sxs-lookup"><span data-stu-id="a45e7-159">**To date** – The date of the latest transaction that can be included in the archive.</span></span>
- <span data-ttu-id="a45e7-160">**Naplánoval(a)** – Uživatelský účet, který vytvořil archiv.</span><span class="sxs-lookup"><span data-stu-id="a45e7-160">**Scheduled by** – The user account that created the archive.</span></span>
- <span data-ttu-id="a45e7-161">**Provedeno** – Datum vytvoření archivu.</span><span class="sxs-lookup"><span data-stu-id="a45e7-161">**Executed** – The date when the archive was created.</span></span>
- <span data-ttu-id="a45e7-162">**Stornováno** – Zaškrtnutí označuje, že archiv byl stornován.</span><span class="sxs-lookup"><span data-stu-id="a45e7-162">**Reverse** – A check mark indicates that the archive has been reversed.</span></span>
- <span data-ttu-id="a45e7-163">**Zastavit aktuální aktualizaci** – Zaškrtnutí označuje, že archivace právě probíhá, ale byla pozastavena.</span><span class="sxs-lookup"><span data-stu-id="a45e7-163">**Stop current update** – A check mark indicates that the archive is in progress, but it has been paused.</span></span>
- <span data-ttu-id="a45e7-164">**Stav** – Stav zpracování archivu.</span><span class="sxs-lookup"><span data-stu-id="a45e7-164">**State** – The processing status of the archive.</span></span> <span data-ttu-id="a45e7-165">Možné hodnoty jsou *Čekání*, *Probíhá*, a *Dokončeno*.</span><span class="sxs-lookup"><span data-stu-id="a45e7-165">The possible values are *Waiting*, *In progress*, and *Finished*.</span></span>

<span data-ttu-id="a45e7-166">Panel nástrojů nad mřížkou poskytuje následující tlačítka, která můžete použít k práci s vybraným archivem:</span><span class="sxs-lookup"><span data-stu-id="a45e7-166">The toolbar above the grid provides the following buttons that you can use to work with a selected archive:</span></span>

- <span data-ttu-id="a45e7-167">**Archivované transakce** – Zobrazí všechny podrobnosti o vybraném archivu.</span><span class="sxs-lookup"><span data-stu-id="a45e7-167">**Archived transactions** – View the full details of the selected archive.</span></span> <span data-ttu-id="a45e7-168">Stránka **Archivované transakce**, která se zobrazí, ukazuje všechny transakce v archivu.</span><span class="sxs-lookup"><span data-stu-id="a45e7-168">The **Archived transactions** page that appears shows all the transactions in the archive.</span></span>

    <span data-ttu-id="a45e7-169">![Stránka archivovaných transakcí](media/archive-inventory-transactions.png "Stránka archivovaných transakcí")</span><span class="sxs-lookup"><span data-stu-id="a45e7-169">![Archived transactions page](media/archive-inventory-transactions.png "Archived transactions page")</span></span>

    <span data-ttu-id="a45e7-170">Chcete-li zobrazit více informací o konkrétní transakci na stránce **Archivované transakce**, vyberte ji v mřížce a poté v podokně akcí vyberte **Detaily archivované transakce**.</span><span class="sxs-lookup"><span data-stu-id="a45e7-170">To view more information about a specific transaction on the **Archived transactions** page, select it in the grid, and then, on the Action Pane, select **Archived transaction details**.</span></span> <span data-ttu-id="a45e7-171">Stránka **Detaily archivované transakce**, která se zobrazí, ukazuje například účtování do hlavní knihy, související odkazy na dílčí hlavní knihu a finanční dimenze.</span><span class="sxs-lookup"><span data-stu-id="a45e7-171">The **Archived transaction details** page that appears shows information such as the ledger posting, related subledger references, and financial dimensions.</span></span>

- <span data-ttu-id="a45e7-172">**Pozastavit archivaci** – Pozastaví vybraný archiv, který se právě zpracovává.</span><span class="sxs-lookup"><span data-stu-id="a45e7-172">**Pause archiving** – Pause a selected archive that is currently being processed.</span></span> <span data-ttu-id="a45e7-173">Pauza se projeví až po vygenerování úlohy archivace.</span><span class="sxs-lookup"><span data-stu-id="a45e7-173">The pause takes effect only after the archiving task has been generated.</span></span> <span data-ttu-id="a45e7-174">Proto může dojít k krátkému zpoždění, než se pozastavení projeví.</span><span class="sxs-lookup"><span data-stu-id="a45e7-174">Therefore, there might be a short delay before the pause takes effect.</span></span> <span data-ttu-id="a45e7-175">Pokud byl archiv pozastaven, objeví se značka zaškrtnutí v jeho poli **Zastavit aktuální aktualizaci**.</span><span class="sxs-lookup"><span data-stu-id="a45e7-175">If an archive has been paused, a check mark appears in its **Stop current update** field.</span></span>
- <span data-ttu-id="a45e7-176">**Pokračovat v archivaci** – Obnoví zpracování vybraného archivu, který je právě pozastaven.</span><span class="sxs-lookup"><span data-stu-id="a45e7-176">**Resume archiving** – Resume processing for a selected archive that is currently paused.</span></span>
- <span data-ttu-id="a45e7-177">**Stornovat** – Stornuje vybraný archiv.</span><span class="sxs-lookup"><span data-stu-id="a45e7-177">**Reverse** – Reverse the selected archive.</span></span> <span data-ttu-id="a45e7-178">Archiv můžete stornovat, pouze pokud je jeho **Stav** nastaven na *Dokončeno*.</span><span class="sxs-lookup"><span data-stu-id="a45e7-178">You can reverse an archive only if its **State** field is set to *Finished*.</span></span> <span data-ttu-id="a45e7-179">Pokud byl archiv stornován, objeví se značka zaškrtnutí v jeho poli **Stornováno**.</span><span class="sxs-lookup"><span data-stu-id="a45e7-179">If an archive has been reversed, a check mark appears in its **Reverse** field.</span></span>