---
title: Řešení potíží se skladovými operacemi
description: Toto téma popisuje, jak vyřešit problémy, s nimiž se můžete setkat při práci se skladovými operacemi.
author: sherry-zheng
manager: tfehr
ms.date: 12/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2020-12-03
ms.dyn365.ops.version: Release 10.0.16
ms.openlocfilehash: ee1bfbf1b5aa736e1ee5bd38403b6c94c2bd036b
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/15/2021
ms.locfileid: "5224995"
---
# <a name="troubleshoot-inventory-operations"></a><span data-ttu-id="7bfa7-103">Řešení potíží se skladovými operacemi</span><span class="sxs-lookup"><span data-stu-id="7bfa7-103">Troubleshoot inventory operations</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="7bfa7-104">Toto téma popisuje, jak vyřešit problémy, s nimiž se můžete setkat při práci se skladovými operacemi.</span><span class="sxs-lookup"><span data-stu-id="7bfa7-104">This topic describes how to fix issues that you might encounter while you work with inventory operations.</span></span>

## <a name="i-cant-find-the-workflow-drop-down-dialog-box-for-inventory-journals"></a><span data-ttu-id="7bfa7-105">Nemohu najít rozevírací dialogové okno „Pracovní postup“ pro deníky zásob.</span><span class="sxs-lookup"><span data-stu-id="7bfa7-105">I can't find the "Workflow" drop-down dialog box for inventory journals.</span></span>

### <a name="issue-description"></a><span data-ttu-id="7bfa7-106">Popis problému</span><span class="sxs-lookup"><span data-stu-id="7bfa7-106">Issue description</span></span>

<span data-ttu-id="7bfa7-107">Nemůžete najít rozevírací dialogové okno **Workflow** na stránce deníku nebo související operace pracovního postupu nejsou k dispozici.</span><span class="sxs-lookup"><span data-stu-id="7bfa7-107">You can't find the **Workflow** drop-down dialog box on the journal page, or related workflow operations aren't available.</span></span>

<span data-ttu-id="7bfa7-108">K tomuto problému může dojít ze tří důvodů, jak je popsáno v následujících podsekcích.</span><span class="sxs-lookup"><span data-stu-id="7bfa7-108">This issue can occur for three reasons, as described in the following subsections.</span></span>

### <a name="issue-resolution-1"></a><span data-ttu-id="7bfa7-109">Řešení problému 1</span><span class="sxs-lookup"><span data-stu-id="7bfa7-109">Issue resolution 1</span></span>

<span data-ttu-id="7bfa7-110">Pokud se problém týká všech uživatelů, může docházet k tomu, že pracovnímu postupu schválení nebyl přiřazen název deníku.</span><span class="sxs-lookup"><span data-stu-id="7bfa7-110">If the issue applies to all users, it might be occurring because the approval workflow hasn't been assigned to the journal name.</span></span> <span data-ttu-id="7bfa7-111">Chcete-li opravit problém, postupujte následovně.</span><span class="sxs-lookup"><span data-stu-id="7bfa7-111">To fix the issue, follow these steps.</span></span>

1. <span data-ttu-id="7bfa7-112">Přejděte na **Řízení zásob &gt; Nastavení &gt; Názvy deníků &gt; Zásoby**.</span><span class="sxs-lookup"><span data-stu-id="7bfa7-112">Go to **Inventory Management &gt; Setup &gt; Journal names &gt; Inventory**.</span></span>
1. <span data-ttu-id="7bfa7-113">V podokně seznamu vyberte ze sloupce seznamu název deníku.</span><span class="sxs-lookup"><span data-stu-id="7bfa7-113">In the list pane, select a journal name to open its settings.</span></span>
1. <span data-ttu-id="7bfa7-114">Na pevné záložce **Obecné** nastavte možnost **workflow schválení** na *Ano*.</span><span class="sxs-lookup"><span data-stu-id="7bfa7-114">On the **General** FastTab, set the **Approval workflow** option to *Yes*.</span></span> <span data-ttu-id="7bfa7-115">Vyberte **Ano** po zobrazení výzvy k potvrzení změny.</span><span class="sxs-lookup"><span data-stu-id="7bfa7-115">If you're prompted to confirm the change, select **Yes**.</span></span>
1. <span data-ttu-id="7bfa7-116">V poli **Workflow** vyberte workflow, který chcete použít pro vybraný název deníku.</span><span class="sxs-lookup"><span data-stu-id="7bfa7-116">In the **Workflow** field, select the workflow that you want to use for the selected journal name.</span></span>

### <a name="issue-resolution-2"></a><span data-ttu-id="7bfa7-117">Řešení problému 2</span><span class="sxs-lookup"><span data-stu-id="7bfa7-117">Issue resolution 2</span></span>

<span data-ttu-id="7bfa7-118">Pokud váš pracovní postup používá přizpůsobený kód, po upgradu systému mohou nastat problémy.</span><span class="sxs-lookup"><span data-stu-id="7bfa7-118">If your workflow uses customized code, issues might occur after you upgrade the system.</span></span> <span data-ttu-id="7bfa7-119">Například ve workflowu deníku může být tlačítko **Odeslat** šedé, takže jej nemůžete vybrat, chcete-li schválit odeslání.</span><span class="sxs-lookup"><span data-stu-id="7bfa7-119">For example, in the journal workflow, the **Submit** button might be grayed out so you can't select it to approve a submission.</span></span>

<span data-ttu-id="7bfa7-120">Pokud je tlačítko **Odeslat** šedé, váš pracovní postup mohl být přizpůsoben, což znamená, že metoda workflowu `canSubmitToWorkflow()` v `FormDataUtil` byla rozšířena.</span><span class="sxs-lookup"><span data-stu-id="7bfa7-120">If the **Submit** button is grayed out, your workflow might have been customized, which means the method of the workflow, `canSubmitToWorkflow()` in `FormDataUtil`, has been extended.</span></span> <span data-ttu-id="7bfa7-121">Chcete-li tento problém vyřešit, změňte způsob, jakým rozšiřujete metodu `canSubmitToWorkflow()` k použití struktury v následujícím příkladu.</span><span class="sxs-lookup"><span data-stu-id="7bfa7-121">To fix this issue, change the way that you extend the method of the `canSubmitToWorkflow()` to use the structure in the following example.</span></span>

```xpp
[ExtensionOf(formStr(InventJournalMovement))]
public final class InventJournalMovement_extension
{
    public boolean canSubmitToWorkflow()
    {
        boolean ret = YourLogicOfCanSubmitToWorkflow();

        return ret;
    }
}
```

### <a name="issue-resolution-3"></a><span data-ttu-id="7bfa7-122">Řešení problému 3</span><span class="sxs-lookup"><span data-stu-id="7bfa7-122">Issue resolution 3</span></span>

<span data-ttu-id="7bfa7-123">Pokud se problém týká pouze několika konkrétních uživatelů, nemusí mít tito uživatelé oprávnění zabezpečení, která jsou vyžadována ke spuštění operací pracovního postupu v denících zásob.</span><span class="sxs-lookup"><span data-stu-id="7bfa7-123">If the issue applies only to a few specific users, those users might not have the security privileges that are required to run workflow operations on inventory journals.</span></span> <span data-ttu-id="7bfa7-124">Ověřte, že každý ovlivněný uživatel má bezpečnostní oprávnění *Udržovat pracovní postup deníku zásob*.</span><span class="sxs-lookup"><span data-stu-id="7bfa7-124">Verify that each affected user has the *Maintain inventory journal workflow* security privilege.</span></span> <span data-ttu-id="7bfa7-125">Ve výchozím nastavení je toto oprávnění přiřazeno k povinnosti, která má stejný název, a tato povinnost je aplikována na roli *Skladník* a *Manažer skladu*.</span><span class="sxs-lookup"><span data-stu-id="7bfa7-125">By default, this privilege is assigned to a duty that has same name, and that duty is applied to the *Warehouse worker* and *Warehouse manager* roles.</span></span>

## <a name="my-inventory-journal-remains-in-system-locked-status-and-the-workflow-batch-job-doesnt-work"></a><span data-ttu-id="7bfa7-126">Můj deník zásob zůstává ve stavu uzamčeného systému a dávková úloha pracovního postupu nefunguje.</span><span class="sxs-lookup"><span data-stu-id="7bfa7-126">My inventory journal remains in system-locked status, and the workflow batch job doesn't work.</span></span>

### <a name="issue-description"></a><span data-ttu-id="7bfa7-127">Popis problému</span><span class="sxs-lookup"><span data-stu-id="7bfa7-127">Issue description</span></span>

<span data-ttu-id="7bfa7-128">Jeden z vašich deníků zásob je uzamčen nějakou operací a není uvolněn.</span><span class="sxs-lookup"><span data-stu-id="7bfa7-128">One of your inventory journals is locked by some operation and isn't being released.</span></span> <span data-ttu-id="7bfa7-129">Například pokud během zaúčtování dojde k neznámé chybě (což je operace uzamčení systému), deník může zůstat ve stavu uzamčeného systému.</span><span class="sxs-lookup"><span data-stu-id="7bfa7-129">For example, if an unknown error occurs during posting (which is a system lock operation), the journal might remain in system-locked status.</span></span> <span data-ttu-id="7bfa7-130">V tomto případě obslužná rutina pracovní položky pracovního postupu vyvolá chybu, zatímco provede ověření zámku.</span><span class="sxs-lookup"><span data-stu-id="7bfa7-130">In this case, the workflow work item handler will throw an error while it does lock validation.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="7bfa7-131">Řešení problému</span><span class="sxs-lookup"><span data-stu-id="7bfa7-131">Issue resolution</span></span>

<span data-ttu-id="7bfa7-132">Přihlaste se k instanci serveru SQL Server pro Supply Chain Management a zkontrolujte, zda je **InventJournalTable.SystemBlocked** nastaven na *1*.</span><span class="sxs-lookup"><span data-stu-id="7bfa7-132">Sign in to the SQL Server instance for Supply Chain Management, and check whether **InventJournalTable.SystemBlocked** is set to *1*.</span></span> <span data-ttu-id="7bfa7-133">Pokud ano, ujistěte se, že deník by neměl být v uzamčeném stavu, a poté resetujte **InventJournalTable.SystemBlocked** na *0*.</span><span class="sxs-lookup"><span data-stu-id="7bfa7-133">If it is, make sure that the journal should not be in locked status, and then reset **InventJournalTable.SystemBlocked** to *0*.</span></span>

## <a name="my-inventory-journal-workflow-is-never-completed-and-the-journal-cant-be-edited-or-posted"></a><span data-ttu-id="7bfa7-134">Můj pracovní postup deníku zásob není nikdy dokončen a deník nelze upravit ani zaúčtovat.</span><span class="sxs-lookup"><span data-stu-id="7bfa7-134">My inventory journal workflow is never completed, and the journal can't be edited or posted.</span></span>

### <a name="issue-description"></a><span data-ttu-id="7bfa7-135">Popis problému</span><span class="sxs-lookup"><span data-stu-id="7bfa7-135">Issue description</span></span>

<span data-ttu-id="7bfa7-136">Po odeslání pracovního postupu schválení deníku přestane zpracování pracovního toku reagovat a vy nebudete moci upravovat ani zpracovávat deníky.</span><span class="sxs-lookup"><span data-stu-id="7bfa7-136">After you submit a journal approval workflow, workflow processing stops responding, and you can't edit or process your journals.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="7bfa7-137">Řešení problému</span><span class="sxs-lookup"><span data-stu-id="7bfa7-137">Issue resolution</span></span>

<span data-ttu-id="7bfa7-138">Existuje několik důvodů, proč zpracování workflowu nemusí být provedeno.</span><span class="sxs-lookup"><span data-stu-id="7bfa7-138">There are several reasons why workflow processing might not be completed.</span></span> <span data-ttu-id="7bfa7-139">Zkontrolujte následující problémy:</span><span class="sxs-lookup"><span data-stu-id="7bfa7-139">Check for the following issues:</span></span>

- <span data-ttu-id="7bfa7-140">Jděte na **Řízení zásob &gt; Nastavení &gt; Workflowy správy skladu** a zkontrolujte konfiguraci ovlivněného workflowu.</span><span class="sxs-lookup"><span data-stu-id="7bfa7-140">Go to **Inventory management &gt; Setup &gt; Inventory management workflows**, and review the configuration of the affected workflow.</span></span> <span data-ttu-id="7bfa7-141">Další informace naleznete v tématu [Workflowy schválení deníku](inventory-journal-workflow.md).</span><span class="sxs-lookup"><span data-stu-id="7bfa7-141">For more information, see [Inventory journal approval workflows](inventory-journal-workflow.md).</span></span>
- <span data-ttu-id="7bfa7-142">Ve workflowu může docházet k výjimce nebo chybě.</span><span class="sxs-lookup"><span data-stu-id="7bfa7-142">The workflow might be encountering an exception or error.</span></span> <span data-ttu-id="7bfa7-143">Zkontrolujte historii pracovní položky ovlivněného workflowu, abyste zjistili, zda obsahuje chybu aplikace, která workflow ukončí.</span><span class="sxs-lookup"><span data-stu-id="7bfa7-143">Review the work item history of the affected workflow to see whether it includes an application error that terminates the workflow.</span></span>
- <span data-ttu-id="7bfa7-144">Deník zásob lze aktualizovat nebo upravovat, pouze pokud je schválen.</span><span class="sxs-lookup"><span data-stu-id="7bfa7-144">The inventory journal can be updated or edited only if it's approved.</span></span> <span data-ttu-id="7bfa7-145">Pokud je vyvolání aktivní, můžete se pokusit vyvolat deník.</span><span class="sxs-lookup"><span data-stu-id="7bfa7-145">If recall is active, you can try to recall the journal.</span></span> <span data-ttu-id="7bfa7-146">Provádění dávkové úlohy workflowu může být pozastaveno z několika důvodů.</span><span class="sxs-lookup"><span data-stu-id="7bfa7-146">Execution of the workflow batch job might be suspended for multiple reasons.</span></span> <span data-ttu-id="7bfa7-147">Některé z těchto důvodů mohou být způsobeny problémem rámce workflowu.</span><span class="sxs-lookup"><span data-stu-id="7bfa7-147">Some of these reasons might be caused by the workflow framework issue.</span></span>

## <a name="inventory-journal-workflow-conditions-apply-only-at-the-journal-level-not-at-the-line-level"></a><span data-ttu-id="7bfa7-148">Podmínky workflowu deníku zásob platí pouze na úrovni deníku, nikoli na úrovni řádků</span><span class="sxs-lookup"><span data-stu-id="7bfa7-148">Inventory journal workflow conditions apply only at the journal level, not at the line level</span></span>

### <a name="issue-description"></a><span data-ttu-id="7bfa7-149">Popis problému</span><span class="sxs-lookup"><span data-stu-id="7bfa7-149">Issue description</span></span>

<span data-ttu-id="7bfa7-150">K tomuto problému může dojít, pokud se například pokusíte nastavit podmínku workflowu deníku zásob na částku nákladů.</span><span class="sxs-lookup"><span data-stu-id="7bfa7-150">You might experience this issue if, for example, you try to set up an inventory journal workflow condition on the cost amount.</span></span> <span data-ttu-id="7bfa7-151">Nastavíte podmínku tak, aby byl krok 1 spuštěn pouze v případě, že částka nákladů bude nižší než 100.</span><span class="sxs-lookup"><span data-stu-id="7bfa7-151">You set up the condition so that step 1 is run only when the cost amount is less than 100.</span></span> <span data-ttu-id="7bfa7-152">Pak nastavíte jinou podmínku tak, aby byl krok 2 spuštěn pouze v případě, že částka nákladů bude vyšší nebo rovna 100.</span><span class="sxs-lookup"><span data-stu-id="7bfa7-152">You then set up another condition so that step 2 is run only when the cost amount is more than or equal to 100.</span></span> <span data-ttu-id="7bfa7-153">Poté, když je spuštěn workflow, se v historii pracovního postupu zobrazuje pouze jeden řádek a první podmínka se vždy vyhodnotí jako *skutečný*, bez ohledu na hodnotu, která je zadána.</span><span class="sxs-lookup"><span data-stu-id="7bfa7-153">Then, when the workflow is run, the workflow history shows only one line, and the first condition is always evaluated as *true*, regardless of the value that is submitted.</span></span>

### <a name="issue-workaround"></a><span data-ttu-id="7bfa7-154">Řešení problému</span><span class="sxs-lookup"><span data-stu-id="7bfa7-154">Issue workaround</span></span>

<span data-ttu-id="7bfa7-155">V aktuální verzi platí podmínky workflowu deníku zásob pouze na úrovni deníku, nikoli na úrovni řádků.</span><span class="sxs-lookup"><span data-stu-id="7bfa7-155">In the current release, inventory workflow conditions apply only at the journal level, not at the line level.</span></span> <span data-ttu-id="7bfa7-156">Toto chování je záměrné.</span><span class="sxs-lookup"><span data-stu-id="7bfa7-156">This behavior is by design.</span></span> <span data-ttu-id="7bfa7-157">Doporučujeme nastavit kritéria podmínky pouze na atributy na úrovni deníku.</span><span class="sxs-lookup"><span data-stu-id="7bfa7-157">We recommend that you set your condition criteria only on journal-level attributes.</span></span>

## <a name="the-filter-pane-on-the-on-hand-list-page-doesnt-filter-results-as-i-expect"></a><span data-ttu-id="7bfa7-158">Podokno filtru na stránce množství po ruce nefiltruje výsledky podle mého očekávání.</span><span class="sxs-lookup"><span data-stu-id="7bfa7-158">The filter pane on the On-hand list page doesn't filter results as I expect.</span></span>

### <a name="issue-description"></a><span data-ttu-id="7bfa7-159">Popis problému</span><span class="sxs-lookup"><span data-stu-id="7bfa7-159">Issue description</span></span>

<span data-ttu-id="7bfa7-160">Filtry v podokně filtru na stránce **seznam na skladě**  nefiltrují výsledky podle mého očekávání.</span><span class="sxs-lookup"><span data-stu-id="7bfa7-160">The filters in the filter pane on the **On-hand list** page don't filter results as you expect.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="7bfa7-161">Řešení problému</span><span class="sxs-lookup"><span data-stu-id="7bfa7-161">Issue resolution</span></span>

<span data-ttu-id="7bfa7-162">Toto chování je záměrné.</span><span class="sxs-lookup"><span data-stu-id="7bfa7-162">This behavior is by design.</span></span>

<span data-ttu-id="7bfa7-163">Stránka  **Seznam na skladě**  je sestavena z podrobné tabulky zásob na skladě, která obsahuje všechny dostupné rozměry.</span><span class="sxs-lookup"><span data-stu-id="7bfa7-163">The **On-hand list** page is assembled from a detailed on-hand inventory table that includes all available dimensions.</span></span> <span data-ttu-id="7bfa7-164">Seznam na této stránce je však shrnutím.</span><span class="sxs-lookup"><span data-stu-id="7bfa7-164">However, the list on this page is a summary.</span></span> <span data-ttu-id="7bfa7-165">Proto by mohl kombinovat řádky ze zdrojové tabulky agregováním hodnot podle zobrazených rozměrů.</span><span class="sxs-lookup"><span data-stu-id="7bfa7-165">Therefore, it might combine rows from the source table by aggregating values according to the dimensions that are shown.</span></span>

<span data-ttu-id="7bfa7-166">Filtry, které jsou nastaveny v podokně filtrů se vztahují na zdrojovou tabulku, nikoli na agregovaný seznam.</span><span class="sxs-lookup"><span data-stu-id="7bfa7-166">Filters that are set up in the filter pane apply to the source table, not to the aggregated list.</span></span> <span data-ttu-id="7bfa7-167">Toto chování může někdy způsobit neočekávané výsledky, jak je uvedeno v [těchto příkladech](inventory-on-hand-list.md#examples).</span><span class="sxs-lookup"><span data-stu-id="7bfa7-167">This behavior can sometimes produce unexpected results, as shown in [these examples](inventory-on-hand-list.md#examples).</span></span>

<span data-ttu-id="7bfa7-168">Nicméně  [filtry poskytované v mřížce](inventory-on-hand-list.md#grid-filters) *platí*  pro agregovaný seznam.</span><span class="sxs-lookup"><span data-stu-id="7bfa7-168">However, the [filters that are provided in the grid](inventory-on-hand-list.md#grid-filters) *do* apply to the aggregated list.</span></span> <span data-ttu-id="7bfa7-169">Tyto filtry zahrnují QuickFilter v horní části mřížky a filtr pro každou hlavičku sloupce.</span><span class="sxs-lookup"><span data-stu-id="7bfa7-169">These filters include both the QuickFilter at the top of the grid and the filter for each column heading.</span></span>

## <a name="the-unit-and-unit-quantity-arent-working-correctly-in-the-inventory-journal"></a><span data-ttu-id="7bfa7-170">Jednotka a množství jednotky nepracují správně v deníku zásob.</span><span class="sxs-lookup"><span data-stu-id="7bfa7-170">The unit and unit quantity aren't working correctly in the inventory journal.</span></span>

### <a name="issue-description"></a><span data-ttu-id="7bfa7-171">Popis problému</span><span class="sxs-lookup"><span data-stu-id="7bfa7-171">Issue description</span></span>

<span data-ttu-id="7bfa7-172">Při práci s jednotkami a množstvími v deníku zásob se můžete setkat s jedním nebo oběma z následujících problémů:</span><span class="sxs-lookup"><span data-stu-id="7bfa7-172">You might encounter one or both of the following issues when you work with units and quantities in an inventory journal:</span></span>

- <span data-ttu-id="7bfa7-173">Když je pro vydaný produkt nastavena jednotka převodu, nevidíte v deníku zásob jednotky ani množství jednotek a nemůžete jednotku v deníku zásob změnit.</span><span class="sxs-lookup"><span data-stu-id="7bfa7-173">You don't see units or unit quantities in the inventory journal while a unit of conversion is set up for the released product, and you can't change the unit in the inventory journal.</span></span>
- <span data-ttu-id="7bfa7-174">V deníku zásob vidíte pole **Množství** a **Jednotka**, ale nevidíte pole **množství jednotky**.</span><span class="sxs-lookup"><span data-stu-id="7bfa7-174">You see the **Quantity** and **Unit** fields in the inventory journal, but you don't see the **Unit quantity** field.</span></span> <span data-ttu-id="7bfa7-175">Pokud změníte jednotku, zadejte množství a zaúčtujete deník, deník stále zobrazuje původní měrnou jednotku pro toto množství.</span><span class="sxs-lookup"><span data-stu-id="7bfa7-175">If you change the unit, enter a quantity, and post the journal, the journal still shows the original unit of measurement for that quantity.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="7bfa7-176">Řešení problému</span><span class="sxs-lookup"><span data-stu-id="7bfa7-176">Issue resolution</span></span>

<span data-ttu-id="7bfa7-177">Chcete-li opravit problém, postupujte následovně.</span><span class="sxs-lookup"><span data-stu-id="7bfa7-177">To fix this issue, follow these steps.</span></span>

1. <span data-ttu-id="7bfa7-178">V pracovním prostoru **Správa funkcí** se ujistěte, že je zapnutá funkce *Použití měrné jednotky a jednotkového množství v denících zásob*.</span><span class="sxs-lookup"><span data-stu-id="7bfa7-178">In the **Feature management** workspace, make sure that the *Using unit of measure and unit quantity in inventory journals* feature is turned on.</span></span> <span data-ttu-id="7bfa7-179">Tato funkce přidává pole **Jednotka** a **Jednotkové množství** do deníku.</span><span class="sxs-lookup"><span data-stu-id="7bfa7-179">This feature adds the **Unit** and **Unit quantity** fields to the journal.</span></span>
1. <span data-ttu-id="7bfa7-180">Po zapnutí funkce použijte pole **Množství**, **Jednotkové množství**, a **Jednotka** následujícím způsobem:</span><span class="sxs-lookup"><span data-stu-id="7bfa7-180">After the feature is turned on, use the **Quantity**, **Unit quantity**, and **Unit** fields in the following way:</span></span>

    - <span data-ttu-id="7bfa7-181">**Množství** - Určete množství pomocí výchozí jednotky definované pro vydaný produkt.</span><span class="sxs-lookup"><span data-stu-id="7bfa7-181">**Quantity** – Specify the quantity by using the default unit that is defined for the released product.</span></span> <span data-ttu-id="7bfa7-182">Samotná výchozí jednotka se zde však nezobrazuje.</span><span class="sxs-lookup"><span data-stu-id="7bfa7-182">However, the default unit itself isn't shown here.</span></span> <span data-ttu-id="7bfa7-183">Pokud je nastaven převod mezi výchozí jednotkou a jednotkou vybranou v poli **Jednotka**, pole **Množství** se automaticky aktualizuje na základě výběrů v poli **Jednotkové množství** a v poli **Jednotka**.</span><span class="sxs-lookup"><span data-stu-id="7bfa7-183">If a conversion is set up between the default unit and the unit that is selected in the **Unit** field, the **Quantity** field is automatically updated, based on the selections in the **Unit quantity** and **Unit** fields.</span></span>
    - <span data-ttu-id="7bfa7-184">**Jednotkové množství** – určete množství pro měrnou jednotku vybranou v poli **Jednotka**.</span><span class="sxs-lookup"><span data-stu-id="7bfa7-184">**Unit quantity** – Specify the quantity by using the unit that is selected in the **Unit** field.</span></span>
    - <span data-ttu-id="7bfa7-185">**Jednotka** - Vyberte jednotku, která se má použít pro hodnotu v poli **Jednotkové množství**.</span><span class="sxs-lookup"><span data-stu-id="7bfa7-185">**Unit** – Select the unit to apply to the value in the **Unit quantity** field.</span></span>

## <a name="i-receive-the-following-error-message-maximum-number-of-decimals-for-the-stock-keeping-unit-is-0"></a><span data-ttu-id="7bfa7-186">Zobrazuje se následující chybová zpráva: „Maximální počet desetinných míst pro skladovou jednotku je 0.“</span><span class="sxs-lookup"><span data-stu-id="7bfa7-186">I receive the following error message: "Maximum number of decimals for the stock keeping unit is 0."</span></span>

### <a name="issue-description"></a><span data-ttu-id="7bfa7-187">Popis problému</span><span class="sxs-lookup"><span data-stu-id="7bfa7-187">Issue description</span></span>

<span data-ttu-id="7bfa7-188">Při pokusu o zaúčtování transakce zásob nebo rezervace zásob se zobrazí následující chybová zpráva: "Maximální počet desetinných míst pro jednotku udržování zásob je 0."</span><span class="sxs-lookup"><span data-stu-id="7bfa7-188">When you try to post an inventory transaction or an inventory reservation, you receive the following error message: "Maximum number of decimals for the stock keeping unit is 0."</span></span>

<span data-ttu-id="7bfa7-189">K tomuto problému dochází, když je množství transakce zásob zadáno jako desetinná hodnota, která je pod úrovní přesnosti, kterou pole podporuje.</span><span class="sxs-lookup"><span data-stu-id="7bfa7-189">This issue occurs when the inventory transaction quantity is specified as a decimal value that is below the level of precision that the field supports.</span></span> <span data-ttu-id="7bfa7-190">Například množství *0,5* bylo zadán pro transakci inventáře, ale jsou podporována pouze celočíselná množství.</span><span class="sxs-lookup"><span data-stu-id="7bfa7-190">For example, a quantity of *0.5* has been specified for an inventory transaction, but only integer quantities are supported.</span></span> <span data-ttu-id="7bfa7-191">Hodnota by proto měla být *1* namísto *0,5*.</span><span class="sxs-lookup"><span data-stu-id="7bfa7-191">Therefore, the value should be *1* instead of *0.5*.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="7bfa7-192">Řešení problému</span><span class="sxs-lookup"><span data-stu-id="7bfa7-192">Issue resolution</span></span>

1. <span data-ttu-id="7bfa7-193">Spusťte následující skript na instanci serveru SQL Server a zaokrouhlete množství v transakcích zásob.</span><span class="sxs-lookup"><span data-stu-id="7bfa7-193">Run the following script on your SQL Server instance to round quantities in the inventory transactions.</span></span> <span data-ttu-id="7bfa7-194">Tento skript opraví hodnoty v tabulce **inventTrans**.</span><span class="sxs-lookup"><span data-stu-id="7bfa7-194">This script will correct values in the **inventTrans** table.</span></span>

    ```sql
    update it set it.QTY = round(it.qty, decimalPrecisionValue) from inventtrans it where it.DATAAREAID='XXXX' and it.PARTITION=XXXXXX and it.qty <> round(it.qty, decimalPrecisionValue) and exists (select 'x' from INVENTTABLEMODULE a, unitofmeasure b where  a.unitid =b.SYMBOL and a.partition=it.partition and a.PARTITION=b.PARTITION and  MODULETYPE =0 and  b.DECIMALPRECISION=decimalPrecisionValue and a.DATAAREAID='XXXX' and a.ITEMID =it.ITEMID and it.DATAAREAID=a.DATAAREAID)
    ```

1. <span data-ttu-id="7bfa7-195">Spusťte kontrolu konzistence na skladě, kde je možnost **opravit chybu** zapnutá.</span><span class="sxs-lookup"><span data-stu-id="7bfa7-195">Run an on-hand consistency check where the **fix error** option is turned on.</span></span> <span data-ttu-id="7bfa7-196">Tato kontrola opraví hodnoty v tabulce **inventSum**.</span><span class="sxs-lookup"><span data-stu-id="7bfa7-196">This check will correct values in the **inventSum** table.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="7bfa7-197">Důrazně doporučujeme, abyste skript pečlivě upravili podle potřeby pro své prostředí, otestovali jej v testovacím prostředí a poté zkontrolovali výsledná data před spuštěním skriptu v provozním prostředí.</span><span class="sxs-lookup"><span data-stu-id="7bfa7-197">We strongly recommend that you carefully edit the script as required for your environment, test it in a test environment, and then check the resulting data before you run the script in a production environment.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]