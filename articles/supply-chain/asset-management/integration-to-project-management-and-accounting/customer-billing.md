---
title: Účet za údržbu na majetku ve vlastnictví zákazníka
description: Toto téma vysvětluje, jak vytvořit, zpracovat a fakturovat údržbu, která se provádí u majetku, který vlastní vaši zákazníci.
author: johanhoffmann
manager: tfehr
ms.date: 01/28/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjProjectContractsListPage, ProjInvoiceTable, ProjProjectsListPage, ProjTable, EntAssetWorkOrderType, EntAssetWorkOrderProjectSetup, EntAssetObjectTable, EntAssetWorkOrderTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2021-01-28
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: a93436d101e6201c9d86279ea5b1a37fcc644fd1
ms.sourcegitcommit: 2b4809e60974e72df9476ffd62706b1bfc8da4a7
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/04/2021
ms.locfileid: "5500447"
---
# <a name="bill-for-maintenance-on-customer-owned-assets"></a><span data-ttu-id="204c6-103">Účet za údržbu na majetku ve vlastnictví zákazníka</span><span class="sxs-lookup"><span data-stu-id="204c6-103">Bill for maintenance on customer-owned assets</span></span>

[!include [banner](../../includes/banner.md)]
[!include [preview banner](../../includes/preview-banner.md)]

<span data-ttu-id="204c6-104">funkce *Fakturace pracovního příkazu* umožňuje vytvářet, zpracovávat a fakturovat práce na údržbě majetku, který vlastní vaši zákazníci.</span><span class="sxs-lookup"><span data-stu-id="204c6-104">The *Work order billing* feature lets you create, process, and bill maintenance work that is done on assets that your customers own.</span></span> <span data-ttu-id="204c6-105">Tato funkce umožňuje provádět následující úlohy:</span><span class="sxs-lookup"><span data-stu-id="204c6-105">This feature lets you perform the following tasks:</span></span>

- <span data-ttu-id="204c6-106">Připojte zákazníky k majetku, který vlastní.</span><span class="sxs-lookup"><span data-stu-id="204c6-106">Connect customers to the assets that they own.</span></span>
- <span data-ttu-id="204c6-107">Vyberte zákazníka a při vytváření pracovního příkazu zobrazte aktiva, která zákazník vlastní.</span><span class="sxs-lookup"><span data-stu-id="204c6-107">Select a customer and view the assets that customer owns when you create a work order.</span></span>
- <span data-ttu-id="204c6-108">Nastavte nadřazený projekt pro každého zákazníka.</span><span class="sxs-lookup"><span data-stu-id="204c6-108">Set up a parent project for each customer.</span></span>
- <span data-ttu-id="204c6-109">Zaregistrujte hodiny, položky, výdaje a poplatky proti pracovní objednávce a poté vytvořte návrh faktury pro zákazníka později.</span><span class="sxs-lookup"><span data-stu-id="204c6-109">Register hours, items, expenses, and fees against the work order, and then create an invoice proposal for the customer later.</span></span>

<span data-ttu-id="204c6-110">Kromě toho tato funkce poskytuje následující funkce:</span><span class="sxs-lookup"><span data-stu-id="204c6-110">In addition, the feature provides the following functionality:</span></span>

- <span data-ttu-id="204c6-111">Smlouva o projektu z nadřazeného projektu zákazníka se automaticky zkopíruje do příslušného projektu pracovního příkazu.</span><span class="sxs-lookup"><span data-stu-id="204c6-111">The project contract from a customer's parent project is automatically copied to the relevant work order project.</span></span>
- <span data-ttu-id="204c6-112">Správa majetku nyní může používat typ transakce projektu *poplatek* v prognózách pracovních objednávek i v denících pracovních objednávkách.</span><span class="sxs-lookup"><span data-stu-id="204c6-112">Asset management can now use the *fee* project transaction type on both work order forecasts and work order journals.</span></span>

## <a name="turn-on-the-customer-billing-feature"></a><span data-ttu-id="204c6-113">Zapněte funkci fakturace zákazníků:</span><span class="sxs-lookup"><span data-stu-id="204c6-113">Turn on the customer billing feature</span></span>

<span data-ttu-id="204c6-114">Než můžete použít tuto funkci, musíte ji zapnout ve svém systému.</span><span class="sxs-lookup"><span data-stu-id="204c6-114">Before you can use this feature, it must be turned on in your system.</span></span> <span data-ttu-id="204c6-115">Správci mohou pomocí nastavení [správa funkcí](../../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) zkontrolovat stav funkce a zapnout ji.</span><span class="sxs-lookup"><span data-stu-id="204c6-115">Admins can use the [feature management](../../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) settings to check the status of the feature and turn it on.</span></span> <span data-ttu-id="204c6-116">V pracovním prostoru **Správa funkcí** je tato funkce uvedena následovně:</span><span class="sxs-lookup"><span data-stu-id="204c6-116">In the **Feature management** workspace, the feature is listed in the following way:</span></span>

- <span data-ttu-id="204c6-117">**Modul:** *Správa a účtování projektu*</span><span class="sxs-lookup"><span data-stu-id="204c6-117">**Module:** *Project management and accounting*</span></span>
- <span data-ttu-id="204c6-118">**Název funkce:** *Fakturace pracovního příkazu*</span><span class="sxs-lookup"><span data-stu-id="204c6-118">**Feature name:** *Work order billing*</span></span>

## <a name="example-scenario"></a><span data-ttu-id="204c6-119">Příklad</span><span class="sxs-lookup"><span data-stu-id="204c6-119">Example scenario</span></span>

<span data-ttu-id="204c6-120">Pokud se chcete dozvědět, jak tato funkce funguje, projděte si následující ukázkový scénář.</span><span class="sxs-lookup"><span data-stu-id="204c6-120">To learn how this feature works, work through the following example scenario.</span></span>

<span data-ttu-id="204c6-121">Chcete-li s tímto scénářem pracovat pomocí zde specifikovaných ukázkových záznamů a hodnot, musíte používat systém, ve kterém jsou nainstalována standardní [ukázková data](../../../fin-ops-core/dev-itpro/deployment/deploy-demo-environment.md).</span><span class="sxs-lookup"><span data-stu-id="204c6-121">To work through this scenario by using the sample records and values that are specified here, you must be on a system where the standard [demo data](../../../fin-ops-core/dev-itpro/deployment/deploy-demo-environment.md) is installed.</span></span> <span data-ttu-id="204c6-122">Dříve než začnete, musíte vybrat právnickou osobu **USMF**.</span><span class="sxs-lookup"><span data-stu-id="204c6-122">You must select the **USMF** legal entity before you begin.</span></span>

<span data-ttu-id="204c6-123">Tento scénář můžete také použít jako vodítko pro použití této funkce při práci na produkčním systému.</span><span class="sxs-lookup"><span data-stu-id="204c6-123">You can also use this scenario as guidance for using the feature when you work on a production system.</span></span> <span data-ttu-id="204c6-124">V takovém případě však musíte nahradit uvedené hodnoty vlastními hodnotami. Také možná budete postrádat některé typy požadovaných záznamů, jež jsou součástí standardních ukázkových dat.</span><span class="sxs-lookup"><span data-stu-id="204c6-124">However, in that case, you must substitute your own values, and you might be missing some types of required records that the standard demo data provides.</span></span>

### <a name="step-1-create-a-new-project-contract-for-the-customer"></a><span data-ttu-id="204c6-125">Krok 1: Vytvořte pro zákazníka novou smlouvu na projekt</span><span class="sxs-lookup"><span data-stu-id="204c6-125">Step 1: Create a new project contract for the customer</span></span>

1. <span data-ttu-id="204c6-126">Přejděte na **Řízení projektu a účetnictví \> Projekty \> Projektové smlouvy**.</span><span class="sxs-lookup"><span data-stu-id="204c6-126">Go to **Project management and accounting \> Projects \> Project contracts**.</span></span>
1. <span data-ttu-id="204c6-127">V podokně akcí zvolte **Nový**.</span><span class="sxs-lookup"><span data-stu-id="204c6-127">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="204c6-128">V dialogovém okně **Nová projektová smlouva** nastavte následující hodnoty:</span><span class="sxs-lookup"><span data-stu-id="204c6-128">In the **New project contract** dialog box, set the following values:</span></span>

    - <span data-ttu-id="204c6-129">**Název:** *Velkoobchody Pelican*</span><span class="sxs-lookup"><span data-stu-id="204c6-129">**Name:** *Pelican Wholesales*</span></span>
    - <span data-ttu-id="204c6-130">**Typ financování:** *Zákazník*</span><span class="sxs-lookup"><span data-stu-id="204c6-130">**Funding type:** *Customer*</span></span>
    - <span data-ttu-id="204c6-131">**Zdroj financování:** *US-013* (*Velkoobchody Pelican*)</span><span class="sxs-lookup"><span data-stu-id="204c6-131">**Funding source:** *US-013* (*Pelican Wholesales*)</span></span>

1. <span data-ttu-id="204c6-132">Vyberte **OK**.</span><span class="sxs-lookup"><span data-stu-id="204c6-132">Select **OK**.</span></span>

### <a name="step-2-create-a-new-parent-project-for-the-customer"></a><span data-ttu-id="204c6-133">Krok 2: Vytvořte pro zákazníka nový nadřazený projekt</span><span class="sxs-lookup"><span data-stu-id="204c6-133">Step 2: Create a new parent project for the customer</span></span>

<span data-ttu-id="204c6-134">Nadřazený projekt, který zde vytvoříte, se použije při vytváření pracovních příkazů pro zákazníka.</span><span class="sxs-lookup"><span data-stu-id="204c6-134">The parent project that you create here will be used when work orders for the customer are created.</span></span>

1. <span data-ttu-id="204c6-135">Přejděte na **Řízení projektu a účetnictví \> Projekty \> Všechny projekty**.</span><span class="sxs-lookup"><span data-stu-id="204c6-135">Go to **Project management and accounting \> Projects \> All projects**.</span></span>
1. <span data-ttu-id="204c6-136">V podokně akcí zvolte **Nový**.</span><span class="sxs-lookup"><span data-stu-id="204c6-136">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="204c6-137">V dialogovém okně **Nový projekt** nastavte následující hodnoty:</span><span class="sxs-lookup"><span data-stu-id="204c6-137">In the **New project** dialog box, set the following values:</span></span>

    - <span data-ttu-id="204c6-138">**Typ projektu:** *Čas a materiál*</span><span class="sxs-lookup"><span data-stu-id="204c6-138">**Project type:** *Time and material*</span></span>
    - <span data-ttu-id="204c6-139">**Název projektu:** *Pracovní příkazy Pelican Wholesales*</span><span class="sxs-lookup"><span data-stu-id="204c6-139">**Project name:** *Pelican Wholesales work orders*</span></span>
    - <span data-ttu-id="204c6-140">**Skupina projektu:** *TM*</span><span class="sxs-lookup"><span data-stu-id="204c6-140">**Project group:** *TM*</span></span>
    - <span data-ttu-id="204c6-141">**ID smlouvy o projektu:** *Pelican Wholesales* (smlouva, kterou jste vytvořili dříve)</span><span class="sxs-lookup"><span data-stu-id="204c6-141">**Project contract ID:** *Pelican Wholesales* (the contract that you created earlier)</span></span>
    - <span data-ttu-id="204c6-142">**Počáteční datum:** Vyberte dnešní datum.</span><span class="sxs-lookup"><span data-stu-id="204c6-142">**Start date:** Select today's date.</span></span>

1. <span data-ttu-id="204c6-143">Zvolte **Vytvořit projekt**.</span><span class="sxs-lookup"><span data-stu-id="204c6-143">Select **Create project**.</span></span>
1. <span data-ttu-id="204c6-144">Nový projekt je otevřen.</span><span class="sxs-lookup"><span data-stu-id="204c6-144">The new project is opened.</span></span> <span data-ttu-id="204c6-145">Poznamenejte si hodnotu **ID projektu**.</span><span class="sxs-lookup"><span data-stu-id="204c6-145">Make a note of the **Project ID** value.</span></span> <span data-ttu-id="204c6-146">Budete ji muset zadat později.</span><span class="sxs-lookup"><span data-stu-id="204c6-146">You will have to enter it later.</span></span>

### <a name="step-3-create-a-new-work-order-type-in-asset-management"></a><span data-ttu-id="204c6-147">Krok 3: Vytvořte nový typ pracovního příkazu ve správě aktiv</span><span class="sxs-lookup"><span data-stu-id="204c6-147">Step 3: Create a new work order type in Asset management</span></span>

1. <span data-ttu-id="204c6-148">Jděte na **Správa majetku \> Nastavení \> Pracovní příkaz \> Typy pracovních příkazů**.</span><span class="sxs-lookup"><span data-stu-id="204c6-148">Go to **Asset management \> Setup \> Work order \> Work order types**.</span></span>
1. <span data-ttu-id="204c6-149">V podokně akcí zvolte **Nový**.</span><span class="sxs-lookup"><span data-stu-id="204c6-149">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="204c6-150">Do mřížky je přidán nový záznam.</span><span class="sxs-lookup"><span data-stu-id="204c6-150">A new record is added to the list.</span></span> <span data-ttu-id="204c6-151">Pro tento řádek nastavte následující hodnoty:</span><span class="sxs-lookup"><span data-stu-id="204c6-151">Set the following values for it:</span></span>

    - <span data-ttu-id="204c6-152">**Typ pracovního příkazu:** *Služba*</span><span class="sxs-lookup"><span data-stu-id="204c6-152">**Work order type:** *Service*</span></span>
    - <span data-ttu-id="204c6-153">**Název:** *Pracovní příkazy služby*</span><span class="sxs-lookup"><span data-stu-id="204c6-153">**Name:** *Service work orders*</span></span>
    - <span data-ttu-id="204c6-154">**Stav životního cyklu pracovního příkazu:** *Standardní*</span><span class="sxs-lookup"><span data-stu-id="204c6-154">**Work order lifecycle state:** *Standard*</span></span>

### <a name="step-4-link-the-customer-account-to-the-parent-project"></a><span data-ttu-id="204c6-155">Krok 4: Propojte zákaznický účet s nadřazeným projektem</span><span class="sxs-lookup"><span data-stu-id="204c6-155">Step 4: Link the customer account to the parent project</span></span>

<span data-ttu-id="204c6-156">Nyní musíte propojit zákaznický účet s nadřazeným projektem v nastavení projektu ve správě majetku.</span><span class="sxs-lookup"><span data-stu-id="204c6-156">You must now link the customer account to the parent project in the project setup in Asset management.</span></span>

1. <span data-ttu-id="204c6-157">Přejděte na **Správa majetku \> Nastavení \> Pracovní příkazy \> Nastavení projektu**.</span><span class="sxs-lookup"><span data-stu-id="204c6-157">Go to **Asset management \> Setup \> Work orders \> Project setup**.</span></span>
1. <span data-ttu-id="204c6-158">Na kartě **Nadřazený projekt** vyberte možnost **Přidat** a přidejte řádek.</span><span class="sxs-lookup"><span data-stu-id="204c6-158">On the **Parent project** tab, select **Add** to add a line.</span></span>
1. <span data-ttu-id="204c6-159">Na novém řádku nastavte následující hodnoty:</span><span class="sxs-lookup"><span data-stu-id="204c6-159">On the new line, set the following values:</span></span>

    - <span data-ttu-id="204c6-160">**Zákaznický účet:** *US-013* (*Pelican Wholesales*)</span><span class="sxs-lookup"><span data-stu-id="204c6-160">**Customer account:** *US-013* (*Pelican Wholesales*)</span></span>
    - <span data-ttu-id="204c6-161">**ID projektu:** Zadejte ID projektu, který jste si dříve poznamenali.</span><span class="sxs-lookup"><span data-stu-id="204c6-161">**Project ID:** Enter the project ID that you made a note of earlier.</span></span>

### <a name="step-5-link-the-project-group-and-type-to-the-work-order-project"></a><span data-ttu-id="204c6-162">Krok 5: Propojte skupinu projektů a typ s projektem pracovního příkazu</span><span class="sxs-lookup"><span data-stu-id="204c6-162">Step 5: Link the project group and type to the work order project</span></span>

<span data-ttu-id="204c6-163">Stále byste měli být na stránce **Nastavení projektu** (**Správa majetku \> Nastavení \> Pracovní příkazy \> Nastavení projektu**).</span><span class="sxs-lookup"><span data-stu-id="204c6-163">You should still be on the **Project setup** page (**Asset management \> Setup \> Work orders \> Project setup**).</span></span>

1. <span data-ttu-id="204c6-164">Na kartě **Skupina projektu** vyberte možnost **Přidat** a přidejte řádek.</span><span class="sxs-lookup"><span data-stu-id="204c6-164">On the **Project group** tab, select **Add** to add a line.</span></span>
1. <span data-ttu-id="204c6-165">Na novém řádku nastavte následující hodnoty:</span><span class="sxs-lookup"><span data-stu-id="204c6-165">On the new line, set the following values:</span></span>

    - <span data-ttu-id="204c6-166">**Typ pracovního příkazu:** *Služba* (typ pracovního příkazu, který jste vytvořili dříve)</span><span class="sxs-lookup"><span data-stu-id="204c6-166">**Work order type:** *Service* (the work order type that you created earlier)</span></span>
    - <span data-ttu-id="204c6-167">**Skupina projektu:** *TM*</span><span class="sxs-lookup"><span data-stu-id="204c6-167">**Project group:** *TM*</span></span>

> [!NOTE]
> <span data-ttu-id="204c6-168">Smlouva o projektu na zakázku se vždy dědí z nadřazeného projektu.</span><span class="sxs-lookup"><span data-stu-id="204c6-168">The project contract on the work order project is always inherited from the parent project.</span></span>

### <a name="step-6-link-an-asset-to-the-customer-id"></a><span data-ttu-id="204c6-169">Krok 6: Propojte majetek s ID zákazníka</span><span class="sxs-lookup"><span data-stu-id="204c6-169">Step 6: Link an asset to the customer ID</span></span>

1. <span data-ttu-id="204c6-170">Přejděte na **Správa majetku \> Majetek \> Aktivní majetek**.</span><span class="sxs-lookup"><span data-stu-id="204c6-170">Go to **Asset management \> Assets \> Active assets**.</span></span>
1. <span data-ttu-id="204c6-171">V poli **Filtr** zadejte *VE-102* a vyberte filtrování podle hodnoty **Majetek**.</span><span class="sxs-lookup"><span data-stu-id="204c6-171">In the **Filter** field, enter *VE-102*, and select to filter by **Asset**.</span></span>
1. <span data-ttu-id="204c6-172">Vyberte majetek a otevřete jeho nastavení.</span><span class="sxs-lookup"><span data-stu-id="204c6-172">Select the asset to open its settings.</span></span>
1. <span data-ttu-id="204c6-173">Na záložce s náhledem **Odběratel** zadejte do pole **Účet odběratele** hodnotu *US-013* (*Pelican Wholesales*).</span><span class="sxs-lookup"><span data-stu-id="204c6-173">On the **Customer** FastTab, set the **Customer account** field to *US-013* (*Pelican Wholesales*).</span></span>

    <span data-ttu-id="204c6-174">Pole **Název** se automaticky aktualizuje na *Pelican Wholesales*.</span><span class="sxs-lookup"><span data-stu-id="204c6-174">The **Name** field is automatically updated to *Pelican Wholesales*.</span></span>

### <a name="step-7-create-a-new-work-order-on-the-asset"></a><span data-ttu-id="204c6-175">Krok 7: Vytvořte nový typ pracovního příkazu v majetku</span><span class="sxs-lookup"><span data-stu-id="204c6-175">Step 7: Create a new work order on the asset</span></span>

1. <span data-ttu-id="204c6-176">Jděte na **Správa majetku \> Pracovní příkazy \> Aktivní pracovní příkazy**.</span><span class="sxs-lookup"><span data-stu-id="204c6-176">Go to **Asset management \> Work orders \> Active work orders**.</span></span>
1. <span data-ttu-id="204c6-177">V podokně akcí zvolte **Nový**.</span><span class="sxs-lookup"><span data-stu-id="204c6-177">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="204c6-178">V dialogovém okně **Vytvoření pracovního příkazu** nastavte následující hodnoty:</span><span class="sxs-lookup"><span data-stu-id="204c6-178">In the **Create work order** dialog box, set the following values:</span></span>

    - <span data-ttu-id="204c6-179">**Typ pracovního příkazu:** *Služba*</span><span class="sxs-lookup"><span data-stu-id="204c6-179">**Work order type:** *Service*</span></span>
    - <span data-ttu-id="204c6-180">**Popis:** *Opravit nákladní auto*</span><span class="sxs-lookup"><span data-stu-id="204c6-180">**Description:** *Repair Truck*</span></span>
    - <span data-ttu-id="204c6-181">**Zákaznický účet:** *US-013* (*Pelican Wholesales*)</span><span class="sxs-lookup"><span data-stu-id="204c6-181">**Customer account:** *US-013* (*Pelican Wholesales*)</span></span>
    - <span data-ttu-id="204c6-182">**Majetek:** *VE-102*</span><span class="sxs-lookup"><span data-stu-id="204c6-182">**Asset:** *VE-102*</span></span>

        > [!NOTE]
        > <span data-ttu-id="204c6-183">Hledání zobrazuje pouze majetek, který je propojen s vybraným zákaznickým účtem.</span><span class="sxs-lookup"><span data-stu-id="204c6-183">The lookup shows only assets that are linked to the selected customer account.</span></span>

    - <span data-ttu-id="204c6-184">**Typ úlohy údržby:** *Oprava*</span><span class="sxs-lookup"><span data-stu-id="204c6-184">**Maintenance job type:** *Repair*</span></span>
    - <span data-ttu-id="204c6-185">**Obchod:** *Mechanik*</span><span class="sxs-lookup"><span data-stu-id="204c6-185">**Trade:** *Mechanic*</span></span>
    - <span data-ttu-id="204c6-186">**Úroveň služeb:** *4*</span><span class="sxs-lookup"><span data-stu-id="204c6-186">**Service level:** *4*</span></span>

1. <span data-ttu-id="204c6-187">Vyberte **OK**.</span><span class="sxs-lookup"><span data-stu-id="204c6-187">Select **OK**.</span></span>

### <a name="step-8-review-the-work-order-and-start-to-work-on-it"></a><span data-ttu-id="204c6-188">Krok 8: Zkontrolujte pracovní příkaz a začněte na něm pracovat</span><span class="sxs-lookup"><span data-stu-id="204c6-188">Step 8: Review the work order and start to work on it</span></span>

<span data-ttu-id="204c6-189">V této části budete pracovat na pracovním příkazu, který jste vytvořili v předchozí části.</span><span class="sxs-lookup"><span data-stu-id="204c6-189">In this section, you will work on the work order that you created in the previous section.</span></span>

1. <span data-ttu-id="204c6-190">Pomocí těchto kroků ověřte, zda je nadřazený projekt *Pracovní příkaz Pelican Wholesales*:</span><span class="sxs-lookup"><span data-stu-id="204c6-190">Follow these steps to verify that the parent project is the *Pelican wholesales Work order* project:</span></span>

    1. <span data-ttu-id="204c6-191">V části **Práce údržby pracovních příkazů** vyberte řádek.</span><span class="sxs-lookup"><span data-stu-id="204c6-191">In the **Work order maintenance jobs** section, select a line.</span></span>
    1. <span data-ttu-id="204c6-192">Na kartě s náhledem **Podrobnosti řádku** zkontrolujte hodnotu **ID projektu**.</span><span class="sxs-lookup"><span data-stu-id="204c6-192">On the **Line details** FastTab, inspect the **Project ID** value.</span></span> <span data-ttu-id="204c6-193">Mělo by to být pomlčované číslo ve formuláři *\<Parent-Project-ID\>-\<Project-ID\>*.</span><span class="sxs-lookup"><span data-stu-id="204c6-193">It should be a hyphenated number in the form *\<Parent-Project-ID\>-\<Project-ID\>*.</span></span> <span data-ttu-id="204c6-194">Tato hodnota je odkaz.</span><span class="sxs-lookup"><span data-stu-id="204c6-194">This value is a link.</span></span>
    1. <span data-ttu-id="204c6-195">Vyberte odkaz ID projektu a otevřete stránku, kde můžete zobrazit nadřazený projekt a názvy projektů.</span><span class="sxs-lookup"><span data-stu-id="204c6-195">Select the project ID link to open a page where you can view the parent project and project names.</span></span>

1. <span data-ttu-id="204c6-196">V podokně akcí na kartě **Pracovní příkaz** ve skupině **Stav životního cyklu** vyberte **Aktualizovat stav pracovního příkazu**.</span><span class="sxs-lookup"><span data-stu-id="204c6-196">On the Action Pane, on the **Work order** tab, in the **Lifecycle state** group, select **Update work order state**.</span></span>
1. <span data-ttu-id="204c6-197">V dialogovém okně **Aktualizovat stav pracovního příkazu** ve sloupci **Vybrat** zaškrtněte políčko u řádku, kde je pole **Stav životního cyklu** nastaveno na *Probíhá*.</span><span class="sxs-lookup"><span data-stu-id="204c6-197">In the **Update work order state** dialog box, in the **Select** column, select the check box for the row where the **Lifecycle state** field is set to *In progress*.</span></span>
1. <span data-ttu-id="204c6-198">Vyberte **OK**.</span><span class="sxs-lookup"><span data-stu-id="204c6-198">Select **OK**.</span></span>
1. <span data-ttu-id="204c6-199">V dialogovém okně **Stav životního cyklu: InProgress** vyberte **OK**.</span><span class="sxs-lookup"><span data-stu-id="204c6-199">In the **Lifecycle state: InProgress** dialog box, select **OK**.</span></span>

### <a name="step-9-post-the-hours-that-were-spent-on-the-work-order-and-create-a-new-invoice-proposal"></a><span data-ttu-id="204c6-200">Krok 9: Zaúčtujte hodiny, které jste strávili na pracovním příkazu, a vytvořte nový návrh faktury</span><span class="sxs-lookup"><span data-stu-id="204c6-200">Step 9: Post the hours that were spent on the work order and create a new invoice proposal</span></span>

<span data-ttu-id="204c6-201">V této části budete dále pracovat na pracovním příkazu, na němž jste pracovali v předchozí části.</span><span class="sxs-lookup"><span data-stu-id="204c6-201">In this section, you will continue to work on the work order that you worked on in the previous section.</span></span>

1. <span data-ttu-id="204c6-202">V podokně akcí na kartě **Pracovní příkaz** ve skupině **Projekt** vyberte **Deníky**.</span><span class="sxs-lookup"><span data-stu-id="204c6-202">On the Action Pane, on the **Work order** tab, in the **Project** group, select **Journals**.</span></span>

    <span data-ttu-id="204c6-203">Zobrazí se stránka **Deníky pracovních příkazů**.</span><span class="sxs-lookup"><span data-stu-id="204c6-203">The **Work order journals** page appears.</span></span> <span data-ttu-id="204c6-204">Zde můžete zaregistrovat čas, který jste strávili na pracovním příkazu.</span><span class="sxs-lookup"><span data-stu-id="204c6-204">Here, you can register the time that you spent on the work order.</span></span>

1. <span data-ttu-id="204c6-205">Na kartě s náhledem **Hodiny** vyberte **Přidat řádek**.</span><span class="sxs-lookup"><span data-stu-id="204c6-205">On the **Hours** FastTab, select **Add line**.</span></span>
1. <span data-ttu-id="204c6-206">Na novém řádku nastavte pole **Hodiny** na *4*.</span><span class="sxs-lookup"><span data-stu-id="204c6-206">On the new, line, set the **Hours** field to *4*.</span></span>
1. <span data-ttu-id="204c6-207">V podokně akcí zvolte **Zaúčtovat deníky**.</span><span class="sxs-lookup"><span data-stu-id="204c6-207">On the Action Pane, select **Post journals**.</span></span>
1. <span data-ttu-id="204c6-208">Zavřete stránku **Deníky pracovních příkazů** pro návrat k pracovnímu příkazu.</span><span class="sxs-lookup"><span data-stu-id="204c6-208">Close the **Work order journals** page to return to the work order.</span></span>
1. <span data-ttu-id="204c6-209">V podokně akcí na kartě **Fakturace** zvolte **Návrh nové faktury**.</span><span class="sxs-lookup"><span data-stu-id="204c6-209">On the Action Pane, on the **Invoicing** tab, select **New invoice proposal**.</span></span>
1. <span data-ttu-id="204c6-210">V dialogovém okně **Vytvořit návrh faktury** v části **Transakce projektu** zaškrtněte políčko **Vybrat** u každého řádku, který chcete fakturovat.</span><span class="sxs-lookup"><span data-stu-id="204c6-210">In the **Create invoice proposal** dialog box, in the **Project transactions** section, select the **Select** check box for every line  that you want to invoice.</span></span>
1. <span data-ttu-id="204c6-211">Vyberte **OK** pro zavření dialogového okna a zobrazení nového návrhu faktury.</span><span class="sxs-lookup"><span data-stu-id="204c6-211">Select **OK** to close the dialog box and view the new invoice proposal.</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]