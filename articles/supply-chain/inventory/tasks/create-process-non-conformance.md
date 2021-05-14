---
title: Vytvoření a zpracování neshod
description: Toto téma popisuje provádění správy neshody na základě existující objednávky kvality.
author: perlynne
ms.date: 03/23/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 06a56a694f7a80d65cb46d08744e78d8361cee3b
ms.sourcegitcommit: 8362f3bd32ce8b9a5af93c8e57daef732a93b19e
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/28/2021
ms.locfileid: "5956199"
---
# <a name="create-and-process-nonconformances"></a><span data-ttu-id="db479-103">Vytvoření a zpracování neshod</span><span class="sxs-lookup"><span data-stu-id="db479-103">Create and process nonconformances</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="db479-104">Toto téma popisuje provádění správy neshody na základě existující objednávky kvality.</span><span class="sxs-lookup"><span data-stu-id="db479-104">This topic describes how to perform nonconformance management based on an existing quality order.</span></span> <span data-ttu-id="db479-105">Řízení neshod obvykle provádí úředník pro kvalitu.</span><span class="sxs-lookup"><span data-stu-id="db479-105">Typically, nonconformance management is done by a quality clerk.</span></span> <span data-ttu-id="db479-106">Předpokladem je, že musíte mít k dispozici objednávku kvality.</span><span class="sxs-lookup"><span data-stu-id="db479-106">As a prerequisite, you must have a quality order available.</span></span> <span data-ttu-id="db479-107">(Informace o tom, jak vytvořit objednávku kvality, viz [Kontrola kvality zboží](inspect-quality-goods.md) .)</span><span class="sxs-lookup"><span data-stu-id="db479-107">(For information about how to create a quality order, see [Inspect the quality of goods](inspect-quality-goods.md).)</span></span>

<span data-ttu-id="db479-108">Než může uživatel zpracovat schválení neshody, musí mu být přiřazen pracovník v poli **Osoba** na stránce **Uživatelé**.</span><span class="sxs-lookup"><span data-stu-id="db479-108">Before a user can process the approval of a nonconformance, a worker must be assigned to them in the **Person** field on the **Users** page.</span></span> <span data-ttu-id="db479-109">Než bude uživatel moci používat poznámky k dokumentu, musí být navíc možnost **Povolit zpracování dokumentů** nastavena na *Ano* v uživatelských možnostech.</span><span class="sxs-lookup"><span data-stu-id="db479-109">Additionally, before the user can use the document notes, the **Enable document handling** option must be set to *Yes* in their user options.</span></span>

## <a name="create-a-nonconformance"></a><span data-ttu-id="db479-110">Vytvoření neshody</span><span class="sxs-lookup"><span data-stu-id="db479-110">Create a nonconformance</span></span>

<span data-ttu-id="db479-111">Pokud chcete vytvořit neshodu, postupujte takto.</span><span class="sxs-lookup"><span data-stu-id="db479-111">To create a nonconformance, follow these steps.</span></span>

1. <span data-ttu-id="db479-112">Přejděte na **Řízení zásob \> Periodické úlohy \> Správa kvality \> Neshody**.</span><span class="sxs-lookup"><span data-stu-id="db479-112">Go to **Inventory management \> Periodic tasks \> Quality management \> Non conformances**.</span></span>
1. <span data-ttu-id="db479-113">V podokně Akce zvolte **Nový**.</span><span class="sxs-lookup"><span data-stu-id="db479-113">On the Action pane, select **New**.</span></span>
1. <span data-ttu-id="db479-114">V dialogovém okně **Vytvoření neshody** v poli **Typ problému** vyberte typ problému, který byl nalezen během procesu kontroly.</span><span class="sxs-lookup"><span data-stu-id="db479-114">In the **Create non conformance** dialog box, in **Problem type** field, select the type of problem that was found during the inspection process.</span></span>
1. <span data-ttu-id="db479-115">Vyberte **OK**.</span><span class="sxs-lookup"><span data-stu-id="db479-115">Select **OK**.</span></span>

## <a name="approve-or-reject-a-nonconformance"></a><span data-ttu-id="db479-116">Schválení nebo zamítnutí neshody</span><span class="sxs-lookup"><span data-stu-id="db479-116">Approve or reject a nonconformance</span></span>

<span data-ttu-id="db479-117">Chcete-li schválit nebo zamítnout neshodu, postupujte takto.</span><span class="sxs-lookup"><span data-stu-id="db479-117">To approve or reject a nonconformance, follow these steps.</span></span>

1. <span data-ttu-id="db479-118">Přejděte na **Řízení zásob \> Periodické úlohy \> Správa kvality \> Neshody**.</span><span class="sxs-lookup"><span data-stu-id="db479-118">Go to **Inventory management \> Periodic tasks \> Quality management \> Non conformances**.</span></span>
1. <span data-ttu-id="db479-119">V seznamu vyberte neshodu, kterou chcete aktualizovat.</span><span class="sxs-lookup"><span data-stu-id="db479-119">In the list, select the nonconformance that you want to update.</span></span>

    > [!NOTE]
    > <span data-ttu-id="db479-120">Opravu můžete přidat pouze ke neshodám, které jsou schváleny.</span><span class="sxs-lookup"><span data-stu-id="db479-120">You can add a correction only to nonconformances that are approved.</span></span>

1. <span data-ttu-id="db479-121">V podokně akcí vyberte **Funkce \> Schválit neshodu** ke schválení neshody nebo **Funkce \> Odmítnout neshodu** k jejímu odmítnutí.</span><span class="sxs-lookup"><span data-stu-id="db479-121">On the Action Pane, select **Functions \> Approve non conformance** to approve the nonconformance or **Functions \> Refuse non conformance** to reject it.</span></span> <span data-ttu-id="db479-122">Schválené neshody můžete přidružit k [souvisejícím operacím](../quality-operations.md).</span><span class="sxs-lookup"><span data-stu-id="db479-122">You can associate approved nonconformances with [related operations](../quality-operations.md).</span></span> <span data-ttu-id="db479-123">Tímto způsobem můžete zaznamenat práci, která se provádí jako součást zpracování neshod a zpracování oprav.</span><span class="sxs-lookup"><span data-stu-id="db479-123">In this way, you can record work that is done as part of the nonconformance handling and the processing of correction handling.</span></span>
1. <span data-ttu-id="db479-124">Budete vyzvání k potvrzení výběru.</span><span class="sxs-lookup"><span data-stu-id="db479-124">You're prompted to confirm your selection.</span></span> <span data-ttu-id="db479-125">Pokračujte výběrem tlačítka **Ano**.</span><span class="sxs-lookup"><span data-stu-id="db479-125">Select **Yes** to continue.</span></span>

## <a name="add-operations-and-other-details-to-nonconformances"></a><span data-ttu-id="db479-126">Přidání operací a dalších údajů k neshodám</span><span class="sxs-lookup"><span data-stu-id="db479-126">Add operations and other details to nonconformances</span></span>

<span data-ttu-id="db479-127">Po vytvoření neshody můžete začít přidávat související operace a určit další informace o těchto operacích.</span><span class="sxs-lookup"><span data-stu-id="db479-127">After you've created a nonconformance, you can start to add related operations and specify additional information about those operations.</span></span> <span data-ttu-id="db479-128">Související operace můžete přidat pouze ke neshodám, které jsou schváleny.</span><span class="sxs-lookup"><span data-stu-id="db479-128">You can add related operations only to nonconformances that are approved.</span></span>

<span data-ttu-id="db479-129">Kromě základních informací můžete k operaci přidat následující údaje:</span><span class="sxs-lookup"><span data-stu-id="db479-129">Besides the basic information, you can add the following details to an operation:</span></span>

- <span data-ttu-id="db479-130">**Položky** – Můžete vytvořit seznam položek, které jsou spotřebovány k provedení opravy.</span><span class="sxs-lookup"><span data-stu-id="db479-130">**Items** – You can create a list of items that are consumed to perform the correction.</span></span> <span data-ttu-id="db479-131">Položky mohou být například výrobky, které jsou nutné k opravě zařízení, nebo přísady, které jsou nutné k přepracování hotového výrobku.</span><span class="sxs-lookup"><span data-stu-id="db479-131">For example, the items might be products that are required to repair equipment or ingredients that are required to rework a finished product.</span></span>
- <span data-ttu-id="db479-132">**Poplatky za kvalitu** – Můžete vytvořit seznam poplatků, které jsou účtovány externím zdrojům.</span><span class="sxs-lookup"><span data-stu-id="db479-132">**Quality charges** – You can create a list of charges that are incurred or billed out to external sources.</span></span>
- <span data-ttu-id="db479-133">**Rozvrh hodin** – Můžete vytvořit protokol času, který každý pracovník stráví operací.</span><span class="sxs-lookup"><span data-stu-id="db479-133">**Timesheet** – You can create a log of the time that each worker spends on the operation.</span></span>

<span data-ttu-id="db479-134">Zbývající nastavení jsou volitelná.</span><span class="sxs-lookup"><span data-stu-id="db479-134">The remaining settings are optional.</span></span> <span data-ttu-id="db479-135">Náklady na každou položku, poplatky za kvalitu a časový rozvrh jsou sečteny a zobrazeny na operaci.</span><span class="sxs-lookup"><span data-stu-id="db479-135">The cost for each item, quality charges, and the timesheet are summed and shown on the operation.</span></span> <span data-ttu-id="db479-136">Nelze přímo upravit pole **Náklady** operace.</span><span class="sxs-lookup"><span data-stu-id="db479-136">You can't directly edit the **Cost** field on the operation.</span></span>

### <a name="create-an-operation-for-a-nonconformance"></a><span data-ttu-id="db479-137">Vytvoření operace pro neshodu</span><span class="sxs-lookup"><span data-stu-id="db479-137">Create an operation for a nonconformance</span></span>

<span data-ttu-id="db479-138">Pokud chcete vytvořit operaci pro neshodu, postupujte takto.</span><span class="sxs-lookup"><span data-stu-id="db479-138">To create an operation for a nonconformance, follow these steps.</span></span>

1. <span data-ttu-id="db479-139">Přejděte na **Řízení zásob \> Periodické úlohy \> Správa kvality \> Neshody**.</span><span class="sxs-lookup"><span data-stu-id="db479-139">Go to **Inventory management \> Periodic tasks \> Quality management \> Non conformances**.</span></span>
1. <span data-ttu-id="db479-140">V seznamu vyberte neshodu, kterou chcete aktualizovat.</span><span class="sxs-lookup"><span data-stu-id="db479-140">In the list, select the nonconformance that you want to update.</span></span>

    > [!NOTE]
    > <span data-ttu-id="db479-141">Operace můžete přidat nebo aktualizovat pouze u neshod, které jsou schváleny.</span><span class="sxs-lookup"><span data-stu-id="db479-141">You can add or update operations only for nonconformances that are approved.</span></span>

1. <span data-ttu-id="db479-142">V podokně Akce vyberte možnost **Související operace**.</span><span class="sxs-lookup"><span data-stu-id="db479-142">On the Action Pane, select **Related operations**.</span></span>
1. <span data-ttu-id="db479-143">Na stránce **Související operace** v podokně Akce vyberte **Nový** a přidejte řádek do mřížky.</span><span class="sxs-lookup"><span data-stu-id="db479-143">On the **Related operations** page, on the Action pane, select **New** to add a row to the grid.</span></span> <span data-ttu-id="db479-144">Poté pro nový řádek nastavte následující pole:</span><span class="sxs-lookup"><span data-stu-id="db479-144">Then set the following fields for the new row:</span></span>

    - <span data-ttu-id="db479-145">**Operace** – Vyberte kód operace, která bude provedena pro nesoulad.</span><span class="sxs-lookup"><span data-stu-id="db479-145">**Operation** – Select the code of the operation that will be performed for the nonconformance.</span></span>
    - <span data-ttu-id="db479-146">**Důvod** – Zadejte podrobný popis, který vysvětluje, proč je operace požadována.</span><span class="sxs-lookup"><span data-stu-id="db479-146">**Reason** – Enter a detailed description that explains why the operation is required.</span></span>
    - <span data-ttu-id="db479-147">**Prodejní objednávka** – Pokud vybraný kód operace souvisí s typem prodejní objednávky, vyberte prodejní objednávku, se kterou operaci propojujete.</span><span class="sxs-lookup"><span data-stu-id="db479-147">**Sales order** – If the selected operation code is related to the sales order type, select the sales order that you're linking the operation to.</span></span>
    - <span data-ttu-id="db479-148">**Nákupní objednávka** – Pokud vybraný kód operace souvisí s typem nákupní objednávky, vyberte nákupní objednávku, se kterou operaci propojujete.</span><span class="sxs-lookup"><span data-stu-id="db479-148">**Purchase order** – If the selected operation code is related to the purchase order type, select the purchase order that you're linking the operation to.</span></span>

1. <span data-ttu-id="db479-149">Zavřete stránky.</span><span class="sxs-lookup"><span data-stu-id="db479-149">Close the pages.</span></span>

### <a name="add-items-to-an-operation"></a><span data-ttu-id="db479-150">Přidání položek do operace</span><span class="sxs-lookup"><span data-stu-id="db479-150">Add items to an operation</span></span>

<span data-ttu-id="db479-151">Chcete-li přidat položky do operace, postupujte takto.</span><span class="sxs-lookup"><span data-stu-id="db479-151">To add items to an operation, follow these steps.</span></span>

1. <span data-ttu-id="db479-152">Přejděte na **Řízení zásob \> Periodické úlohy \> Správa kvality \> Neshody**.</span><span class="sxs-lookup"><span data-stu-id="db479-152">Go to **Inventory management \> Periodic tasks \> Quality management \> Non conformances**.</span></span>
1. <span data-ttu-id="db479-153">V seznamu vyberte neshodu, kterou chcete aktualizovat.</span><span class="sxs-lookup"><span data-stu-id="db479-153">In the list, select the nonconformance that you want to update.</span></span>

    > [!NOTE]
    > <span data-ttu-id="db479-154">Operace můžete přidat nebo aktualizovat pouze u neshod, které jsou schváleny.</span><span class="sxs-lookup"><span data-stu-id="db479-154">You can add or update operations only for nonconformances that are approved.</span></span>

1. <span data-ttu-id="db479-155">V podokně Akce vyberte možnost **Související operace**.</span><span class="sxs-lookup"><span data-stu-id="db479-155">On the Action Pane, select **Related operations**.</span></span>
1. <span data-ttu-id="db479-156">Na stránce **Související operace** vyberte operaci, do které chcete přidat položky.</span><span class="sxs-lookup"><span data-stu-id="db479-156">On the **Related operations** page, select the operation that you want to add items to.</span></span>
1. <span data-ttu-id="db479-157">V podokně akcí zvolte **Položky**.</span><span class="sxs-lookup"><span data-stu-id="db479-157">On the Action Pane, select **Items**.</span></span>
1. <span data-ttu-id="db479-158">Na stránce **Související operace** v podokně Akce vyberte **Nový** a přidejte řádek do mřížky.</span><span class="sxs-lookup"><span data-stu-id="db479-158">On the **Related operations** page, on the Action pane, select **New** to add a row to the grid.</span></span> <span data-ttu-id="db479-159">Poté pro nový řádek nastavte následující pole:</span><span class="sxs-lookup"><span data-stu-id="db479-159">Then set the following fields for new row:</span></span>

    - <span data-ttu-id="db479-160">**Číslo položky** – Vyberte produkt, který bude spotřebován jako součást vybrané operace.</span><span class="sxs-lookup"><span data-stu-id="db479-160">**Item number** – Select the product that will be consumed as part of the selected operation.</span></span>
    - <span data-ttu-id="db479-161">**Množství** – Zadejte počet položek, které budou spotřebovány.</span><span class="sxs-lookup"><span data-stu-id="db479-161">**Quantity** – Enter the number of items that will be consumed.</span></span>

    > [!NOTE]
    > <span data-ttu-id="db479-162">Náklady na položku můžete zobrazit v poli **Náklady** na kartě **Obecné** záložka. Cena, která se zde zobrazuje, pochází z nákladů, které jsou nastaveny na stránce **Vydaný produkt**.</span><span class="sxs-lookup"><span data-stu-id="db479-162">You can view the cost for the item in the **Cost** field on the **General** tab. The cost that is shown there comes from the cost that is set up on the **Released product** page.</span></span> <span data-ttu-id="db479-163">Náklady nelze aktualizovat přímo na stránce **Související položka operace**.</span><span class="sxs-lookup"><span data-stu-id="db479-163">The cost can't be updated directly on the **Related operation item** page.</span></span> <span data-ttu-id="db479-164">Cena všech položek, které jsou přidány na stránku **Související položky operace**, se automaticky přidá do pole **Náklady** na stránce **Související operace**.</span><span class="sxs-lookup"><span data-stu-id="db479-164">The cost of all items that are added on the **Related operation items** page is automatically added to the **Cost** field on the **Related operations** page.</span></span>

1. <span data-ttu-id="db479-165">Opakujte předchozí krok pro každou další položku, kterou musíte přidat.</span><span class="sxs-lookup"><span data-stu-id="db479-165">Repeat the previous step for each additional item that you must add.</span></span>
1. <span data-ttu-id="db479-166">Zavřete stránky.</span><span class="sxs-lookup"><span data-stu-id="db479-166">Close the pages.</span></span>

### <a name="add-quality-charges-to-an-operation"></a><span data-ttu-id="db479-167">Přidání poplatků za kvalitu k operaci</span><span class="sxs-lookup"><span data-stu-id="db479-167">Add quality charges to an operation</span></span>

<span data-ttu-id="db479-168">Chcete-li přidat poplatky za kvalitu k operaci, postupujte takto.</span><span class="sxs-lookup"><span data-stu-id="db479-168">To add quality charges to an operation, follow these steps.</span></span>

1. <span data-ttu-id="db479-169">Přejděte na **Řízení zásob \> Periodické úlohy \> Správa kvality \> Neshody**.</span><span class="sxs-lookup"><span data-stu-id="db479-169">Go to **Inventory management \> Periodic tasks \> Quality management \> Non conformances**.</span></span>
1. <span data-ttu-id="db479-170">V seznamu vyberte neshodu, kterou chcete aktualizovat.</span><span class="sxs-lookup"><span data-stu-id="db479-170">In the list, select the nonconformance that you want to update.</span></span>

    > [!NOTE]
    > <span data-ttu-id="db479-171">Operace můžete přidat nebo aktualizovat pouze u neshod, které jsou schváleny.</span><span class="sxs-lookup"><span data-stu-id="db479-171">You can add or update operations only for nonconformances that are approved.</span></span>

1. <span data-ttu-id="db479-172">V podokně Akce vyberte možnost **Související operace**.</span><span class="sxs-lookup"><span data-stu-id="db479-172">On the Action Pane, select **Related operations**.</span></span>
1. <span data-ttu-id="db479-173">Na stránce **Související operace** vyberte operaci, do které chcete přidat poplatky za kvalitu.</span><span class="sxs-lookup"><span data-stu-id="db479-173">On the **Related operations** page, select the operation that you want to add quality charges to.</span></span>
1. <span data-ttu-id="db479-174">V podokně Akce vyberte možnost **Poplatky za kvalitu**.</span><span class="sxs-lookup"><span data-stu-id="db479-174">On the Action Pane, select **Quality charges**.</span></span>
1. <span data-ttu-id="db479-175">Na stránce **Související poplatky operace** v podokně Akce vyberte **Nový** a přidejte řádek do mřížky.</span><span class="sxs-lookup"><span data-stu-id="db479-175">On the **Related operation charges** page, on the Action pane, select **New** to add a row to the grid.</span></span> <span data-ttu-id="db479-176">Poté pro nový řádek nastavte následující pole:</span><span class="sxs-lookup"><span data-stu-id="db479-176">Then set the following fields for the new row:</span></span>

    - <span data-ttu-id="db479-177">**Kód poplatků** – Vyberte poplatek za kvalitu, který chcete přidat.</span><span class="sxs-lookup"><span data-stu-id="db479-177">**Charges code** – Select the quality charge that you want to add.</span></span>
    - <span data-ttu-id="db479-178">**Popis** - Zadejte podrobný popis typu nákladu.</span><span class="sxs-lookup"><span data-stu-id="db479-178">**Description** – Enter a detailed description of the charge.</span></span>
    - <span data-ttu-id="db479-179">**Hodnota poplatků** – Zadejte částku poplatku.</span><span class="sxs-lookup"><span data-stu-id="db479-179">**Charges value** – Enter the amount of the charge.</span></span>

1. <span data-ttu-id="db479-180">Opakujte předchozí krok pro každý poplatek, který musíte přidat.</span><span class="sxs-lookup"><span data-stu-id="db479-180">Repeat the previous step for each additional charge that you must add.</span></span>
1. <span data-ttu-id="db479-181">Zavřete stránky.</span><span class="sxs-lookup"><span data-stu-id="db479-181">Close the pages.</span></span>

> [!NOTE]
> <span data-ttu-id="db479-182">Částka v poli **Hodnota poplatků** je automaticky sečtena pro všechny poplatky za kvalitu a přidána k jakýmkoli dalším částkám v poli **Náklady** na stránce **Související operace**.</span><span class="sxs-lookup"><span data-stu-id="db479-182">The amount in the **Charges value** field is automatically summed for all quality charges and added to any other amounts in the **Cost** field on the **Related operations** page.</span></span>

### <a name="create-a-timesheet-on-an-operation"></a><span data-ttu-id="db479-183">Vytvoření časového rozvrhu operace</span><span class="sxs-lookup"><span data-stu-id="db479-183">Create a timesheet on an operation</span></span>

<span data-ttu-id="db479-184">Chcete-li časový rozvrh k operaci, postupujte takto.</span><span class="sxs-lookup"><span data-stu-id="db479-184">To add a timesheet to an operation, follow these steps.</span></span>

1. <span data-ttu-id="db479-185">Přejděte na **Řízení zásob \> Periodické úlohy \> Správa kvality \> Neshody**.</span><span class="sxs-lookup"><span data-stu-id="db479-185">Go to **Inventory management \> Periodic tasks \> Quality management \> Non conformances**.</span></span>
1. <span data-ttu-id="db479-186">V seznamu vyberte neshodu, kterou chcete aktualizovat.</span><span class="sxs-lookup"><span data-stu-id="db479-186">In the list, select the nonconformance that you want to update.</span></span>

    > [!NOTE]
    > <span data-ttu-id="db479-187">Operace můžete přidat nebo aktualizovat pouze u neshod, které jsou schváleny.</span><span class="sxs-lookup"><span data-stu-id="db479-187">You can add or update operations only for nonconformances that are approved.</span></span>

1. <span data-ttu-id="db479-188">V podokně Akce vyberte možnost **Související operace**.</span><span class="sxs-lookup"><span data-stu-id="db479-188">On the Action Pane, select **Related operations**.</span></span>
1. <span data-ttu-id="db479-189">Na stránce **Související operace** vyberte operaci, do které chcete přidat časový rozvrh.</span><span class="sxs-lookup"><span data-stu-id="db479-189">On the **Related operations** page, select the operation that you want to add a timesheet to.</span></span>
1. <span data-ttu-id="db479-190">V podokně akcí zvolte **Časový rozvrh**.</span><span class="sxs-lookup"><span data-stu-id="db479-190">On the Action Pane, select **Timesheet**.</span></span>
1. <span data-ttu-id="db479-191">Na stránce **Související časové rozvrhy operace** v podokně Akce vyberte **Nový** a přidejte řádek do mřížky.</span><span class="sxs-lookup"><span data-stu-id="db479-191">On the **Related operation time sheets** page, on the Action pane, select **New** to add a row to the grid.</span></span> <span data-ttu-id="db479-192">Poté pro nový řádek nastavte následující pole:</span><span class="sxs-lookup"><span data-stu-id="db479-192">Then set the following fields for the new row:</span></span>

    - <span data-ttu-id="db479-193">**Datum** – Uveďte datum, kdy byla práce dokončena.</span><span class="sxs-lookup"><span data-stu-id="db479-193">**Date** – Specify the date when work was done.</span></span> <span data-ttu-id="db479-194">Ve výchozím nastavení je toto pole nastaveno na aktuální datum.</span><span class="sxs-lookup"><span data-stu-id="db479-194">By default, this field is set to the current date.</span></span>
    - <span data-ttu-id="db479-195">**Pracovník** – Vyberte pracovníka, který práci provedl.</span><span class="sxs-lookup"><span data-stu-id="db479-195">**Worker** – Select the worker who did the work.</span></span> <span data-ttu-id="db479-196">Ve výchozím nastavení je toto pole nastaveno na pracovníka, který je přiřazen aktuálnímu uživateli.</span><span class="sxs-lookup"><span data-stu-id="db479-196">By default, this field is set to the worker that is assigned to the current user.</span></span>
    - <span data-ttu-id="db479-197">**Provozní doba** – Zadejte počet hodin, které byly odpracovány na vybrané operaci.</span><span class="sxs-lookup"><span data-stu-id="db479-197">**Operation hours** – Enter the number of hours that were worked on the selected operation.</span></span>
    - <span data-ttu-id="db479-198">**Fakturováno** – Toto políčko zaškrtněte, pokud byl čas účtován zákazníkovi nebo prodejci na faktuře.</span><span class="sxs-lookup"><span data-stu-id="db479-198">**Invoiced** – Select this check box if the time has been charged to a customer or vendor on an invoice.</span></span>

    > [!NOTE]
    > <span data-ttu-id="db479-199">Náklady si můžete prohlédnout v poli **Náklady** na kartě **Obecné**. Cena se vypočítá pomocí sazby, kterou definujete na stránce **Parametry správy zásob**.</span><span class="sxs-lookup"><span data-stu-id="db479-199">You can view the cost in the **Cost** field on the **General** tab. The cost is calculated by using the rate that you define on the **Inventory management parameters** page.</span></span>

1. <span data-ttu-id="db479-200">Opakujte předchozí krok pro každý řádek časového rozvrhu, který musíte přidat.</span><span class="sxs-lookup"><span data-stu-id="db479-200">Repeat the previous step for each additional timesheet line that you must add.</span></span>
1. <span data-ttu-id="db479-201">Zavřete stránky.</span><span class="sxs-lookup"><span data-stu-id="db479-201">Close the pages.</span></span>

> [!NOTE]
> <span data-ttu-id="db479-202">Částka v poli **Náklady** je sečtena pro všechny řádky časového rozvrhu a přičtena k jakýmkoli dalším částkám v poli **Náklady** na stránce **Související operace**.</span><span class="sxs-lookup"><span data-stu-id="db479-202">The amount in the **Cost** field is summed for all timesheet lines and added to any other amounts in the **Cost** field on the **Related operations** page.</span></span>

## <a name="add-a-correction-to-a-nonconformance"></a><span data-ttu-id="db479-203">Přidání opravy k neshodě</span><span class="sxs-lookup"><span data-stu-id="db479-203">Add a correction to a nonconformance</span></span>

<span data-ttu-id="db479-204">Chcete-li přidat opravu k neshodě, postupujte takto.</span><span class="sxs-lookup"><span data-stu-id="db479-204">To add a correction to a nonconformance, follow these steps.</span></span>

1. <span data-ttu-id="db479-205">Přejděte na **Řízení zásob \> Periodické úlohy \> Správa kvality \> Neshody**.</span><span class="sxs-lookup"><span data-stu-id="db479-205">Go to **Inventory management \> Periodic tasks \> Quality management \> Non conformances**.</span></span>
1. <span data-ttu-id="db479-206">V seznamu vyberte neshodu, kterou chcete aktualizovat.</span><span class="sxs-lookup"><span data-stu-id="db479-206">In the list, select the nonconformance that you want to update.</span></span>

    > [!NOTE]
    > <span data-ttu-id="db479-207">Opravu můžete přidat pouze ke neshodám, které jsou schváleny.</span><span class="sxs-lookup"><span data-stu-id="db479-207">You can add a correction only to nonconformances that are approved.</span></span>

1. <span data-ttu-id="db479-208">V podokně akcí zvolte **Opravy**.</span><span class="sxs-lookup"><span data-stu-id="db479-208">On the Action Pane, select **Corrections**.</span></span>
1. <span data-ttu-id="db479-209">Na stránce **Opravy** v podokně Akce vyberte **Nový** pro přidání řádku do mřížky.</span><span class="sxs-lookup"><span data-stu-id="db479-209">On the **Corrections** page, on the Action Pane, select **New** to add a row to the grid.</span></span> <span data-ttu-id="db479-210">Poté pro nový řádek nastavte následující pole:</span><span class="sxs-lookup"><span data-stu-id="db479-210">Then set the following fields for the new row:</span></span>

    - <span data-ttu-id="db479-211">**Diagnostika** – Vyberte typ diagnostiky, který určuje typ opravy, kterou vytváříte.</span><span class="sxs-lookup"><span data-stu-id="db479-211">**Diagnostic** – Select the diagnostic type that identifies the type of correction that you're creating.</span></span>
    - <span data-ttu-id="db479-212">**Pracovník** – Vyberte osobu, která za opravu nese odpovědnost.</span><span class="sxs-lookup"><span data-stu-id="db479-212">**Worker** – Select the person who is responsible for the correction.</span></span>
    - <span data-ttu-id="db479-213">**Priorita opravy** – Vyberte možnost a určete, jak by měla být korekce upřednostněna (*Nízký*, *Normální* nebo *Vysoký*).</span><span class="sxs-lookup"><span data-stu-id="db479-213">**Correction priority** – Select an option to indicate how the correction should be prioritized (*Low*, *Normal*, or *High*).</span></span>
    - <span data-ttu-id="db479-214">**Požadované datum** – Zadejte datum, kdy bylo požadováno nápravné opatření.</span><span class="sxs-lookup"><span data-stu-id="db479-214">**Requested date** – Enter the date when the corrective action was requested.</span></span>
    - <span data-ttu-id="db479-215">**Plánované datum** – Zadejte datum, kdy se očekává dokončení opravy.</span><span class="sxs-lookup"><span data-stu-id="db479-215">**Planned date** – Enter the date when the correction is expected to be completed.</span></span>
    - <span data-ttu-id="db479-216">**Krátkodobé řešení** – Zaškrtněte toto políčko, pokud nápravná akce opraví nesoulad pouze na krátkou dobu.</span><span class="sxs-lookup"><span data-stu-id="db479-216">**Short term solution** – Select this check box if the corrective action corrects the nonconformance only for a short time.</span></span>

1. <span data-ttu-id="db479-217">Zavřete stránky.</span><span class="sxs-lookup"><span data-stu-id="db479-217">Close the pages.</span></span>

## <a name="mark-a-correction-as-completed"></a><span data-ttu-id="db479-218">Označení opravy jako dokončené</span><span class="sxs-lookup"><span data-stu-id="db479-218">Mark a correction as completed</span></span>

<span data-ttu-id="db479-219">Chcete-li označit opravu neshody jako dokončenou, postupujte takto.</span><span class="sxs-lookup"><span data-stu-id="db479-219">To mark a nonconformance correction as completed, follow these steps.</span></span>

1. <span data-ttu-id="db479-220">Přejděte na **Řízení zásob \> Periodické úlohy \> Správa kvality \> Neshody**.</span><span class="sxs-lookup"><span data-stu-id="db479-220">Go to **Inventory management \> Periodic tasks \> Quality management \> Non conformances**.</span></span>
1. <span data-ttu-id="db479-221">V seznamu vyberte neshodu, kterou chcete aktualizovat.</span><span class="sxs-lookup"><span data-stu-id="db479-221">In the list, select the nonconformance that you want to update.</span></span>

    > [!NOTE]
    > <span data-ttu-id="db479-222">Opravu můžete přidat pouze ke neshodám, které jsou schváleny.</span><span class="sxs-lookup"><span data-stu-id="db479-222">You can add a correction only to nonconformances that are approved.</span></span>

1. <span data-ttu-id="db479-223">V podokně akcí zvolte **Opravy**.</span><span class="sxs-lookup"><span data-stu-id="db479-223">On the Action Pane, select **Corrections**.</span></span>
1. <span data-ttu-id="db479-224">Na stránce **Opravy** v mřížce vyberte opravu, kterou chcete označit jako dokončenou.</span><span class="sxs-lookup"><span data-stu-id="db479-224">On the **Corrections** page, in the grid, select the correction that you want to mark as completed.</span></span>
1. <span data-ttu-id="db479-225">V podokně akcí vyberte možnost **Označit jako dokončenou**.</span><span class="sxs-lookup"><span data-stu-id="db479-225">On the Action Pane, select **Mark complete**.</span></span>
1. <span data-ttu-id="db479-226">Budete vyzvání k potvrzení výběru.</span><span class="sxs-lookup"><span data-stu-id="db479-226">You're prompted to confirm your selection.</span></span> <span data-ttu-id="db479-227">Pokračujte volbou tlačítka **OK**.</span><span class="sxs-lookup"><span data-stu-id="db479-227">Select **OK** to continue.</span></span> <span data-ttu-id="db479-228">Pole **Datum a čas dokončení** pole je nastaveno na aktuální datum a čas a je zaškrtnuto políčko **Dokončeno**.</span><span class="sxs-lookup"><span data-stu-id="db479-228">The **Completion date and time** field is set to the current date and time, and the **Completed** check box is selected.</span></span>
1. <span data-ttu-id="db479-229">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="db479-229">Close the page.</span></span>

## <a name="reopen-a-completed-correction"></a><span data-ttu-id="db479-230">Opětovné otevření dokončené opravy</span><span class="sxs-lookup"><span data-stu-id="db479-230">Reopen a completed correction</span></span>

<span data-ttu-id="db479-231">Chcete-li otevřít dokončenou opravu, postupujte takto.</span><span class="sxs-lookup"><span data-stu-id="db479-231">To reopen a completed correction, follow these steps.</span></span>

1. <span data-ttu-id="db479-232">Přejděte na **Řízení zásob \> Periodické úlohy \> Správa kvality \> Neshody**.</span><span class="sxs-lookup"><span data-stu-id="db479-232">Go to **Inventory management \> Periodic tasks \> Quality management \> Non conformances**.</span></span>
1. <span data-ttu-id="db479-233">V seznamu vyberte neshodu, kterou chcete aktualizovat.</span><span class="sxs-lookup"><span data-stu-id="db479-233">In the list, select the nonconformance that you want to update.</span></span>
1. <span data-ttu-id="db479-234">V podokně akcí zvolte **Opravy**.</span><span class="sxs-lookup"><span data-stu-id="db479-234">On the Action pane, select **Corrections**.</span></span>
1. <span data-ttu-id="db479-235">Na stránce **Opravy** v mřížce vyberte opravu, kterou chcete znovu otevřít.</span><span class="sxs-lookup"><span data-stu-id="db479-235">On the **Corrections** page, in the grid, select the correction that you want to reopen.</span></span>
1. <span data-ttu-id="db479-236">V podokně akcí zvolte **Znovu otevřít**.</span><span class="sxs-lookup"><span data-stu-id="db479-236">On the Action Pane, select **Reopen**.</span></span>
1. <span data-ttu-id="db479-237">Budete vyzvání k potvrzení výběru.</span><span class="sxs-lookup"><span data-stu-id="db479-237">You're prompted to confirm your selection.</span></span> <span data-ttu-id="db479-238">Pokračujte volbou tlačítka **OK**.</span><span class="sxs-lookup"><span data-stu-id="db479-238">Select **OK** to continue.</span></span> <span data-ttu-id="db479-239">Hodnota je vymazána z pole **Datum a čas dokončení** a políčko **Dokončeno** není zaškrtnuto.</span><span class="sxs-lookup"><span data-stu-id="db479-239">The value is cleared from the **Completion date and time** field, and the **Completed** check box is cleared.</span></span>
1. <span data-ttu-id="db479-240">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="db479-240">Close the page.</span></span>

<span data-ttu-id="db479-241">Nyní můžete provést další úpravy nebo aktualizace opravy.</span><span class="sxs-lookup"><span data-stu-id="db479-241">You can now make additional edits or updates to the correction.</span></span> <span data-ttu-id="db479-242">Po dokončení můžete opravu znovu označit jako dokončenou.</span><span class="sxs-lookup"><span data-stu-id="db479-242">When you've finished, you can mark the correction as completed again.</span></span>

## <a name="close-a-nonconformance"></a><span data-ttu-id="db479-243">Zavření neshody</span><span class="sxs-lookup"><span data-stu-id="db479-243">Close a nonconformance</span></span>

<span data-ttu-id="db479-244">Pokud chcete zavřít neshodu, postupujte takto.</span><span class="sxs-lookup"><span data-stu-id="db479-244">To close a nonconformance, follow these steps.</span></span>

1. <span data-ttu-id="db479-245">Přejděte na **Řízení zásob \> Periodické úlohy \> Správa kvality \> Objednávky kvality**.</span><span class="sxs-lookup"><span data-stu-id="db479-245">Go to **Inventory management \> Periodic tasks \> Quality management \> Quality orders**.</span></span>
1. <span data-ttu-id="db479-246">Vyberte objednávku kvality v mřížce.</span><span class="sxs-lookup"><span data-stu-id="db479-246">Select a quality order in the grid.</span></span>
1. <span data-ttu-id="db479-247">V podokně akcí zvolte **Dotazy \> Neshody**.</span><span class="sxs-lookup"><span data-stu-id="db479-247">On the Action Pane, select **Inquiries \> Non conformances**.</span></span>
1. <span data-ttu-id="db479-248">Na stránce **Neshody** vyberte cílovou neshodu v mřížce.</span><span class="sxs-lookup"><span data-stu-id="db479-248">On the **Non conformances** page, select the target nonconformance in the grid.</span></span>
1. <span data-ttu-id="db479-249">V podokně Akce zvolte **Funkce \> Zavřít neshodu**.</span><span class="sxs-lookup"><span data-stu-id="db479-249">On the Action Pane, select **Functions \> Close non conformance**.</span></span>
1. <span data-ttu-id="db479-250">Budete vyzvání k potvrzení výběru.</span><span class="sxs-lookup"><span data-stu-id="db479-250">You're prompted to confirm your selection.</span></span> <span data-ttu-id="db479-251">Pokračujte výběrem tlačítka **Ano**.</span><span class="sxs-lookup"><span data-stu-id="db479-251">Select **Yes** to continue.</span></span>
1. <span data-ttu-id="db479-252">Zavřete stránky.</span><span class="sxs-lookup"><span data-stu-id="db479-252">Close the pages.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="db479-253">Další prostředky</span><span class="sxs-lookup"><span data-stu-id="db479-253">Additional resources</span></span>

- [<span data-ttu-id="db479-254">Přehled správy kvality</span><span class="sxs-lookup"><span data-stu-id="db479-254">Quality management overview</span></span>](../quality-management-processes.md)
- [<span data-ttu-id="db479-255">Povolit správu kvality a neshod</span><span class="sxs-lookup"><span data-stu-id="db479-255">Enable quality and nonconformance management</span></span>](../enable-quality-management.md)
- [<span data-ttu-id="db479-256">Zaměstnanci odpovědní za schvalování neshod</span><span class="sxs-lookup"><span data-stu-id="db479-256">Workers responsible for approving nonconformances</span></span>](../quality-responsible-workers.md)
- [<span data-ttu-id="db479-257">Karanténní zóny pro neshody</span><span class="sxs-lookup"><span data-stu-id="db479-257">Quarantine zones for nonconformances</span></span>](../quality-quarantine-zones.md)
- [<span data-ttu-id="db479-258">Diagnostické typy pro neshody</span><span class="sxs-lookup"><span data-stu-id="db479-258">Diagnostic types for nonconformances</span></span>](../quality-diagnostic-types.md)
- [<span data-ttu-id="db479-259">Kódy kvality pro náklady</span><span class="sxs-lookup"><span data-stu-id="db479-259">Quality charges for nonconformances</span></span>](../quality-charges.md)
- [<span data-ttu-id="db479-260">Operace pro neshody</span><span class="sxs-lookup"><span data-stu-id="db479-260">Operations for nonconformances</span></span>](../quality-operations.md)
- [<span data-ttu-id="db479-261">Správa kvality pro procesy skladu</span><span class="sxs-lookup"><span data-stu-id="db479-261">Quality management for warehouse processes</span></span>](../quality-management-for-warehouses-processes.md)

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
