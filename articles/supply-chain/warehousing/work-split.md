---
title: Rozdělení práce
description: Toto téma obsahuje informace o funkci rozdělení práce. Tato funkce umožňuje rozdělit velké pracovní příkazy na několik menších pracovních příkazů, které pak můžete přiřadit několika pracovníkům skladu. Tímto způsobem může stejnou práci vydat současně několika pracovníky skladu.
author: mirzaab
manager: tfehr
ms.date: 10/15/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Retail, Core, Operations
ms.search.region: Global
ms.search.industry: WHSWorkTableListPage
ms.author: mirzaab
ms.search.validFrom: 2020-10-15
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: e74b630e72d70829938f0f34efd624509b1ba7c3
ms.sourcegitcommit: 531be324bf706ca727d777720df899d6ddd3c2d7
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 11/05/2020
ms.locfileid: "4424287"
---
# <a name="work-split"></a><span data-ttu-id="3dc68-105">Rozdělení práce</span><span class="sxs-lookup"><span data-stu-id="3dc68-105">Work split</span></span>

<span data-ttu-id="3dc68-106">Funkce rozdělení práce umožňuje rozdělit velké pracovní ID (tzn. pracovní příkazy obsahující několik řídků) na několik menších pracovních ID, které pak můžete přiřadit několika pracovníkům skladu.</span><span class="sxs-lookup"><span data-stu-id="3dc68-106">Work split functionality lets you split large work IDs (that is, work orders that have several lines) into several smaller work IDs that you can then assign to multiple warehouse workers.</span></span> <span data-ttu-id="3dc68-107">Tímto způsobem může stejné číslo vytvoření práce vydat současně několik pracovníků skladu.</span><span class="sxs-lookup"><span data-stu-id="3dc68-107">In this way, the same work creation number can be picked simultaneously by several warehouse workers.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="3dc68-108">Můžete rozdělit pouze pracovní příkazy, které mají stav *Otevřeno* nebo *Probíhá*.</span><span class="sxs-lookup"><span data-stu-id="3dc68-108">You can split only work orders that have a status of *Open* or *In-progress*.</span></span>

## <a name="turn-on-the-work-split-functionality"></a><span data-ttu-id="3dc68-109">Zapněte funkci rozdělení práce</span><span class="sxs-lookup"><span data-stu-id="3dc68-109">Turn on the work split functionality</span></span>

<span data-ttu-id="3dc68-110">Než budete moci použít funkci rozdělení práce, musíte zapnout funkci a její nezbytnou funkci ve vašem systému.</span><span class="sxs-lookup"><span data-stu-id="3dc68-110">Before you can use the work split functionality, you must turn on the feature and its prerequisite feature in your system.</span></span> <span data-ttu-id="3dc68-111">Správci mohou pomocí nastavení [správa funkcí](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) zkontrolovat stav funkcí a zapnout ji dle potřeby.</span><span class="sxs-lookup"><span data-stu-id="3dc68-111">Administrators can use the [feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) settings to check the status of the features and turn them on as required.</span></span>

<span data-ttu-id="3dc68-112">Nejprve zapnout požadovanou funkci *Blokování práce v celé organizaci*, pokud již není zapnutá.</span><span class="sxs-lookup"><span data-stu-id="3dc68-112">First, turn on the prerequisite *Organization-wide work blocking* feature if it isn't already turned on.</span></span> <span data-ttu-id="3dc68-113">V pracovním prostoru **Správa funkcí** je tato funkce uvedena následovně:</span><span class="sxs-lookup"><span data-stu-id="3dc68-113">In the **Feature management** workspace, this feature is listed in the following way:</span></span>

- <span data-ttu-id="3dc68-114">**Modul:** *Řízení skladu*</span><span class="sxs-lookup"><span data-stu-id="3dc68-114">**Module:** *Warehouse management*</span></span>
- <span data-ttu-id="3dc68-115">**Název funkce:** *Blokování práce napříč organizací*</span><span class="sxs-lookup"><span data-stu-id="3dc68-115">**Feature name:** *Organization-wide work blocking*</span></span>

> [!NOTE]
> <span data-ttu-id="3dc68-116">Když je tato funkce aktivována, aktualizace dat se automaticky použije po zapnutí této funkce u všech právnických osob.</span><span class="sxs-lookup"><span data-stu-id="3dc68-116">When this feature is activated, a data upgrade is automatically applied after the feature is turned on across all legal entities.</span></span>

<span data-ttu-id="3dc68-117">Dále zapněte funkci *Rozdělení práce*, která je uvedena následujícím způsobem:</span><span class="sxs-lookup"><span data-stu-id="3dc68-117">Next, turn on the *Work split* feature, which is listed in the following way:</span></span>

- <span data-ttu-id="3dc68-118">**Modul:** *Řízení skladu*</span><span class="sxs-lookup"><span data-stu-id="3dc68-118">**Module:** *Warehouse management*</span></span>
- <span data-ttu-id="3dc68-119">**Název funkce:** *Rozdělení práce*</span><span class="sxs-lookup"><span data-stu-id="3dc68-119">**Feature name:** *Work split*</span></span>

## <a name="enhancements-to-the-work-details-and-all-work-pages"></a><span data-ttu-id="3dc68-120">Vylepšení stránek Podrobnosti práce a Všechny práce</span><span class="sxs-lookup"><span data-stu-id="3dc68-120">Enhancements to the Work details and All work pages</span></span>

<span data-ttu-id="3dc68-121">Funkce *Rozdělení práce* přidá následující dvě tlačítka na kartu **Práce** v podokně Akcí na stránkách **Podrobnosti práce** a **Všechny práce**:</span><span class="sxs-lookup"><span data-stu-id="3dc68-121">The *Work split* feature adds the following two buttons to the **Work** tab on the Action Pane of the **Work details** and **All work** pages:</span></span>

- <span data-ttu-id="3dc68-122">**Rozdělení práce** - Rozdělte ID aktuální práce do několika menších ID práce, která lze zpracovat samostatnými pracovníky.</span><span class="sxs-lookup"><span data-stu-id="3dc68-122">**Split work** – Split the current work ID into multiple smaller work IDs that can be processed by separate workers.</span></span>
- <span data-ttu-id="3dc68-123">**Zrušte relaci rozdělení práce** - Zrušte relaci rozdělení práce a zpřístupněte práci ke zpracování.</span><span class="sxs-lookup"><span data-stu-id="3dc68-123">**Cancel work split session** – Cancel the work split session, and make the work available for processing.</span></span>

<span data-ttu-id="3dc68-124">![Tlačítka relace Rozdělit práci a Zrušit rozdělení práce](media/Work_split_buttons.png "Tlačítka relace Rozdělit práci a Zrušit rozdělení práce")</span><span class="sxs-lookup"><span data-stu-id="3dc68-124">![Split work and Cancel work split session buttons](media/Work_split_buttons.png "Split work and Cancel work split session buttons")</span></span>

> [!IMPORTANT]
> <span data-ttu-id="3dc68-125">Tlačítko **Rozdělit práci** nebude k dispozici, pokud bude splněna některá z následujících podmínek:</span><span class="sxs-lookup"><span data-stu-id="3dc68-125">The **Split work** button won't be available if any of the following conditions are met:</span></span>
>
> - <span data-ttu-id="3dc68-126">Stav práce je jiný než *Otevřeno* nebo *Probíhá*.</span><span class="sxs-lookup"><span data-stu-id="3dc68-126">The work status is something other than *Open* or *In progress*.</span></span>
> - <span data-ttu-id="3dc68-127">ID kontejneru je přidruženo k ID práce.</span><span class="sxs-lookup"><span data-stu-id="3dc68-127">A container ID is associated with the work ID.</span></span> <span data-ttu-id="3dc68-128">(Kontejner nelze systematicky rozdělit, protože vyžaduje fyzické akce.)</span><span class="sxs-lookup"><span data-stu-id="3dc68-128">(A container can't be systematically split, because it requires physical actions.)</span></span>
> - <span data-ttu-id="3dc68-129">Práce je spojena se seskupením.</span><span class="sxs-lookup"><span data-stu-id="3dc68-129">The work is associated with a cluster.</span></span>
> - <span data-ttu-id="3dc68-130">Typ pracovního příkazu je jiný než jeden z následujících typů:</span><span class="sxs-lookup"><span data-stu-id="3dc68-130">The work order type is something other than one of the following types:</span></span>
>
>    - <span data-ttu-id="3dc68-131">Prodejní objednávky</span><span class="sxs-lookup"><span data-stu-id="3dc68-131">Sales orders</span></span>
>    - <span data-ttu-id="3dc68-132">Výdej suroviny</span><span class="sxs-lookup"><span data-stu-id="3dc68-132">Raw material picking</span></span>
>    - <span data-ttu-id="3dc68-133">Vydání převodního příkazu</span><span class="sxs-lookup"><span data-stu-id="3dc68-133">Transfer issue</span></span>
>
> - <span data-ttu-id="3dc68-134">Práce je aktuálně rozdělena jiným uživatelem.</span><span class="sxs-lookup"><span data-stu-id="3dc68-134">The work is currently being split by another user.</span></span> <span data-ttu-id="3dc68-135">Pokud se pokusíte otevřít rozdělovací stránku pro práci, která je již rozdělena jiným uživatelem, zobrazí se následující chybová zpráva: „Práce s ID \#\#\#\# je v současné době rozdělena.</span><span class="sxs-lookup"><span data-stu-id="3dc68-135">If you try to open the splitting page for work that is already being split by another user, you receive the following error message: "The work with ID \#\#\#\# is currently being split.</span></span> <span data-ttu-id="3dc68-136">Zkuste to znovu za několik minut.</span><span class="sxs-lookup"><span data-stu-id="3dc68-136">Retry in a few minutes.</span></span> <span data-ttu-id="3dc68-137">Pokud budete nadále dostávat tuto zprávu, obraťte se na nadřízeného.“</span><span class="sxs-lookup"><span data-stu-id="3dc68-137">If you continue to receive this message, contact a supervisor."</span></span>

<span data-ttu-id="3dc68-138">Nový důvod blokování práce *Rozdělení práce* označuje, kdy je ID práce v procesu rozdělení.</span><span class="sxs-lookup"><span data-stu-id="3dc68-138">A new work blocking reason, *Split work*, indicates when the work ID is in the process of being split.</span></span> <span data-ttu-id="3dc68-139">Je to zobrazeno jak na stránce **Rozdělit práci** a v aplikaci skladu, pokud se uživatel pokusí spustit práci.</span><span class="sxs-lookup"><span data-stu-id="3dc68-139">It's shown both on the **Split work** page and in the warehouse app if a user tries to run the work.</span></span> <span data-ttu-id="3dc68-140">Pokud jsou použity důvody blokování, název pole **Blokovaná vlna** z ID práce se změní na **Blokováno**.</span><span class="sxs-lookup"><span data-stu-id="3dc68-140">When blocking reasons are used, the name of the **Blocked wave** field from the work ID is changed to **Blocked**.</span></span>

## <a name="initiate-a-work-split"></a><span data-ttu-id="3dc68-141">Zahajte rozdělení práce</span><span class="sxs-lookup"><span data-stu-id="3dc68-141">Initiate a work split</span></span>

<span data-ttu-id="3dc68-142">Funkce přidává novou stránku **Rozdělení práce**, která umožňuje uživatelům rozdělit pracovní řádky z ID práce.</span><span class="sxs-lookup"><span data-stu-id="3dc68-142">The feature adds a new **Split work** page that lets users split work lines from the work ID.</span></span> <span data-ttu-id="3dc68-143">Při prvním otevření stránky se zobrazí řádky, které mají pracovní stav *Otevřeno* a které jsou k dispozici k rozdělení.</span><span class="sxs-lookup"><span data-stu-id="3dc68-143">When the page is first opened, it shows lines that have a work status of *Open* and that are available to be split.</span></span> <span data-ttu-id="3dc68-144">V podokně akcí vyberte **Rozdělit práci** pro zpracování vybrané práce.</span><span class="sxs-lookup"><span data-stu-id="3dc68-144">On the Action Pane, select **Split work** to process the selected work.</span></span>

<span data-ttu-id="3dc68-145">Chcete-li rozdělit práci, postupujte takto.</span><span class="sxs-lookup"><span data-stu-id="3dc68-145">To split work, follow these steps.</span></span>

1. <span data-ttu-id="3dc68-146">Otevřete jednu z následujících stránek práce:</span><span class="sxs-lookup"><span data-stu-id="3dc68-146">Open one of the following work pages:</span></span>

    - <span data-ttu-id="3dc68-147">**Podrobnosti práce** (**Řízení skladu \> Práce \> Podrobnosti práce**)</span><span class="sxs-lookup"><span data-stu-id="3dc68-147">**Work details** (**Warehouse management \> Work \> Work details**)</span></span>
    - <span data-ttu-id="3dc68-148">**Všechna práce** (**Řízení skladu \> Práce \> Všechna práce**)</span><span class="sxs-lookup"><span data-stu-id="3dc68-148">**All work** (**Warehouse management \> Work \> All work**)</span></span>

1. <span data-ttu-id="3dc68-149">V mřížce vyberte ID práce k rozdělení.</span><span class="sxs-lookup"><span data-stu-id="3dc68-149">In the grid, select a work ID to split.</span></span> <span data-ttu-id="3dc68-150">Pole **Typ pracovního příkazu** musí být nastaveno na jednu z následujících hodnot:</span><span class="sxs-lookup"><span data-stu-id="3dc68-150">The **Work order type** field must be set to one of the following values:</span></span>

    - <span data-ttu-id="3dc68-151">Prodejní objednávky</span><span class="sxs-lookup"><span data-stu-id="3dc68-151">Sales orders</span></span>
    - <span data-ttu-id="3dc68-152">Výdej suroviny</span><span class="sxs-lookup"><span data-stu-id="3dc68-152">Raw material picking</span></span>
    - <span data-ttu-id="3dc68-153">Vydání převodního příkazu</span><span class="sxs-lookup"><span data-stu-id="3dc68-153">Transfer issue</span></span>

1. <span data-ttu-id="3dc68-154">V podokně Akce na kartě **Práce** ve skupině **Práce** vyberte **Rozdělit práci**.</span><span class="sxs-lookup"><span data-stu-id="3dc68-154">On the Action Pane, on the **Work** tab, in the **Work** group, select **Split work**.</span></span>

    <span data-ttu-id="3dc68-155">Stránka **Rozdělit práci** se zobrazí s pracovními řádky, které jsou otevřené a dostupné k rozdělení.</span><span class="sxs-lookup"><span data-stu-id="3dc68-155">The **Split work** page appears and shows the work lines that are open and available to be split.</span></span> <span data-ttu-id="3dc68-156">Ve výchozím nastavení jsou zobrazeny pouze dostupné pracovní řádky.</span><span class="sxs-lookup"><span data-stu-id="3dc68-156">By default, only available work lines are shown.</span></span> <span data-ttu-id="3dc68-157">Chcete-li zobrazit všechny řádky pro pracovní ID (například řádky, které mají pracovní typ *Vložit*), vyberte zaškrtávací políčko **Zobrazit všechny řádky** nad mřížkou.</span><span class="sxs-lookup"><span data-stu-id="3dc68-157">To view all lines for the work ID (for example, lines that have a work type of *Put*), select the **Show all lines** check box above the grid.</span></span>

    <span data-ttu-id="3dc68-158">Zobrazí se následující zpráva: „Uživatelé nemohou zpracovat řádky práce, dokud nedokončíte rozdělení a nezavřete tuto stránku.“</span><span class="sxs-lookup"><span data-stu-id="3dc68-158">The following message is shown: "Users can't process lines of the work until you finish splitting and close this page."</span></span>

    <span data-ttu-id="3dc68-159">Pole **Důvod blokování práce** pro aktuální práci bude nastaveno na *Rozdělit práci* a práce bude zablokována.</span><span class="sxs-lookup"><span data-stu-id="3dc68-159">The **Work blocking reason** field for the current work will be set to *Split work*, and the work will be blocked.</span></span>

    <span data-ttu-id="3dc68-160">![Důvod blokování](media/Blocking_reason.png "Důvod blokování")</span><span class="sxs-lookup"><span data-stu-id="3dc68-160">![Blocking reason](media/Blocking_reason.png "Blocking reason")</span></span>

1. <span data-ttu-id="3dc68-161">Vyberte řádky, které chcete odebrat z aktuálního ID práce a přidat do nového ID práce.</span><span class="sxs-lookup"><span data-stu-id="3dc68-161">Select the lines to remove from the current work ID and add to a new work ID.</span></span> <span data-ttu-id="3dc68-162">Dojde k následujícím událostem:</span><span class="sxs-lookup"><span data-stu-id="3dc68-162">The following events occur:</span></span>

    - <span data-ttu-id="3dc68-163">Když práci rozdělíte, vybraný řádek nebo řádky z původního ID práce se zruší a poté se zkopírují do nového ID práce.</span><span class="sxs-lookup"><span data-stu-id="3dc68-163">When you split the work, the selected line or lines from the original work ID are canceled and then copied to a new work ID.</span></span>
    - <span data-ttu-id="3dc68-164">Stávající struktura pracovní šablony a umístění vložení (a také budoucí páry vydat / vložit) jsou zachovány.</span><span class="sxs-lookup"><span data-stu-id="3dc68-164">The existing work template structure and the location of the put (and also future pick/put pairs) are preserved.</span></span> <span data-ttu-id="3dc68-165">Hodnoty pro následující pole ID práce se zkopírují z původní práce do nové práce:</span><span class="sxs-lookup"><span data-stu-id="3dc68-165">Values for the following work ID fields are copied from the original work to the new work:</span></span>

        - <span data-ttu-id="3dc68-166">ID nákladu</span><span class="sxs-lookup"><span data-stu-id="3dc68-166">Load ID</span></span>
        - <span data-ttu-id="3dc68-167">ID dodávky</span><span class="sxs-lookup"><span data-stu-id="3dc68-167">Shipment ID</span></span>
        - <span data-ttu-id="3dc68-168">Typ pracovního příkazu</span><span class="sxs-lookup"><span data-stu-id="3dc68-168">Work order type</span></span>
        - <span data-ttu-id="3dc68-169">Číslo objednávky</span><span class="sxs-lookup"><span data-stu-id="3dc68-169">Order number</span></span>
        - <span data-ttu-id="3dc68-170">Lokalita</span><span class="sxs-lookup"><span data-stu-id="3dc68-170">Site</span></span>
        - <span data-ttu-id="3dc68-171">Sklad</span><span class="sxs-lookup"><span data-stu-id="3dc68-171">Warehouse</span></span>
        - <span data-ttu-id="3dc68-172">Pracovní priorita</span><span class="sxs-lookup"><span data-stu-id="3dc68-172">Work priority</span></span>
        - <span data-ttu-id="3dc68-173">ID fondu práce</span><span class="sxs-lookup"><span data-stu-id="3dc68-173">Work pool ID</span></span>
        - <span data-ttu-id="3dc68-174">ID vlny</span><span class="sxs-lookup"><span data-stu-id="3dc68-174">Wave ID</span></span>
        - <span data-ttu-id="3dc68-175">Číslo vytvoření práce</span><span class="sxs-lookup"><span data-stu-id="3dc68-175">Work creation number</span></span>

    - <span data-ttu-id="3dc68-176">Následující pole nejsou zkopírována do nového ID práce:</span><span class="sxs-lookup"><span data-stu-id="3dc68-176">The following fields aren't copied to the new work ID:</span></span>

        - <span data-ttu-id="3dc68-177">**ID práce** - Z příslušné číselné řady je vygenerováno nové ID práce.</span><span class="sxs-lookup"><span data-stu-id="3dc68-177">**Work ID** – A new work ID is generated from the appropriate number sequence.</span></span>
        - <span data-ttu-id="3dc68-178">**Stav práce** - Toto pole je nastaveno na *Otevřeno*.</span><span class="sxs-lookup"><span data-stu-id="3dc68-178">**Work status** – This field is set to *Open*.</span></span>
        - <span data-ttu-id="3dc68-179">**Zamknul** - Toto pole je zpočátku nastaveno na prázdné.</span><span class="sxs-lookup"><span data-stu-id="3dc68-179">**Locked by** – This field is initially set to blank.</span></span>
        - <span data-ttu-id="3dc68-180">**Cílová registrační značka** - Toto pole je prázdné.</span><span class="sxs-lookup"><span data-stu-id="3dc68-180">**Target license plate ID** – This field is left blank.</span></span>
        - <span data-ttu-id="3dc68-181">**Datum a čas vytvoření** - Toto pole je nastaveno na aktuální datum a čas.</span><span class="sxs-lookup"><span data-stu-id="3dc68-181">**Created date and time** – This field is set to the current date and time.</span></span>
        - <span data-ttu-id="3dc68-182">**Blokovaná vlna** - Toto pole je přepočítáno pro původní ID práce a nové ID práce.</span><span class="sxs-lookup"><span data-stu-id="3dc68-182">**Blocked wave/frozen** – This field is recomputed for the original work ID and the new work ID.</span></span>

1. <span data-ttu-id="3dc68-183">V podokně akcí vyberte **Rozdělit práci**.</span><span class="sxs-lookup"><span data-stu-id="3dc68-183">On the Action Pane, select **Split work**.</span></span>

<span data-ttu-id="3dc68-184">Během rozdělování práce se zobrazí následující zpráva: „Zpracování - dělení práce“.</span><span class="sxs-lookup"><span data-stu-id="3dc68-184">While the work is being split, the following message is shown: "Processing operation - Split work".</span></span> <span data-ttu-id="3dc68-185">I když je tato zpráva viditelná, můžete operaci zrušit výběrem **Zrušit** v okně se zprávou.</span><span class="sxs-lookup"><span data-stu-id="3dc68-185">While this message is visible, you can cancel the operation by selecting **Cancel** in the message box.</span></span>

<span data-ttu-id="3dc68-186">Pokud není zaškrtnou políčko **Zobrazit všechny řádky**, řádek, který byla oddělena a zrušen, se již v mřížce nezobrazí.</span><span class="sxs-lookup"><span data-stu-id="3dc68-186">If the **Show all lines** check box is cleared, the line that was split off and canceled will no longer appear in the grid.</span></span> <span data-ttu-id="3dc68-187">Pokud je zaškrtnuto políčko, měli byste vidět, že hodnota **Stav práce** pro tento řádek se změnilo na *Zrušeno*.</span><span class="sxs-lookup"><span data-stu-id="3dc68-187">If the check box is selected, you should see that the value of the **Work status** field for that line has changed to *Canceled*.</span></span>

<span data-ttu-id="3dc68-188">Zobrazí se následující oznámení, které označuje, že nové ID práce bylo vytvořeno: „Práce \#\#\#\# byla vytvořena oddělením od původní práce \#\#\#\#.“</span><span class="sxs-lookup"><span data-stu-id="3dc68-188">The following notification is shown to indicate that the new work ID has been created: "Work \#\#\#\# has been created by splitting off from original work \#\#\#\#."</span></span>

<span data-ttu-id="3dc68-189">Další pracovní řádky z původního ID práce (např řádky *Vložit*) budou podle potřeby upraveny tak, aby odrážely řádky prací, které byly zrušeny.</span><span class="sxs-lookup"><span data-stu-id="3dc68-189">Other work lines from the original work ID (such as *Put* lines) will be adjusted as required to reflect the lines of work that have been canceled.</span></span> <span data-ttu-id="3dc68-190">Například, pokud původní ID práce mělo řádek *Vložit* pro množství 15 a řádky *Výdej*, kterých je celkem 10, byly zrušeny, nové množství *Vložit* na původním ID práce bude nyní 5.</span><span class="sxs-lookup"><span data-stu-id="3dc68-190">For example, if the original work ID had a *Put* line for a quantity of 15, and *Pick* lines that have a total quantity of 10 were canceled, the new *Put* quantity on the original work ID will now be 5.</span></span>

<span data-ttu-id="3dc68-191">Nová práce nebude okamžitě přiřazena žádnému uživateli.</span><span class="sxs-lookup"><span data-stu-id="3dc68-191">The new work won't immediately be assigned to any user.</span></span> <span data-ttu-id="3dc68-192">Můžete ji však nyní podle potřeby přiřadit uživateli pomocí standardní funkce na stránce **Podrobnosti o práci**.</span><span class="sxs-lookup"><span data-stu-id="3dc68-192">However, you can assign it to a user now, as required, by using the standard functionality of the **Work details** page.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="3dc68-193">Můžete rozdělit pouze ID práce, která obsahuja dva nebo více dostupných pracovních řádků.</span><span class="sxs-lookup"><span data-stu-id="3dc68-193">You can split only work IDs that contain two or more available work lines.</span></span> <span data-ttu-id="3dc68-194">Pokud vyberete **Rozdělit práci**, když existuje pouze jeden řádek práce, zobrazí se následující chybová zpráva: "V počáteční práci musí zůstat alespoň jeden řádek práce."</span><span class="sxs-lookup"><span data-stu-id="3dc68-194">If you select **Split work** when there is only one work line, you will receive the following error message: "At least one work line must remain on initial work."</span></span> <span data-ttu-id="3dc68-195">V tomto případě nedojde k rozdělení.</span><span class="sxs-lookup"><span data-stu-id="3dc68-195">In this case, no splitting will occur.</span></span>

## <a name="finish-a-work-split"></a><span data-ttu-id="3dc68-196">Dokončete rozdělení práce</span><span class="sxs-lookup"><span data-stu-id="3dc68-196">Finish a work split</span></span>

<span data-ttu-id="3dc68-197">Chcete-li dokončit rozdělení práce, důvod blokování *Rozdělit práci* musí být odstraněn.</span><span class="sxs-lookup"><span data-stu-id="3dc68-197">To finish splitting work, the *Split work* blocking reason must be removed.</span></span> <span data-ttu-id="3dc68-198">Toto lze provést dvěma způsoby:</span><span class="sxs-lookup"><span data-stu-id="3dc68-198">There are two ways to complete this step:</span></span>

- <span data-ttu-id="3dc68-199">Uživatel, který rozděluje práci, zavře stránku **Rozdělit práci** výběrem tlačítka **Zavřít** (**X**) v pravém horním rohu.</span><span class="sxs-lookup"><span data-stu-id="3dc68-199">The user who is splitting the work closes the **Split work** page by selecting the **Close** button (**X**) in the upper-right corner.</span></span> <span data-ttu-id="3dc68-200">Když je stránka zavřená, důvod blokování *Rozdělení práce* bude odstraněn.</span><span class="sxs-lookup"><span data-stu-id="3dc68-200">When the page is closed, the *Split Work* blocking reason will be removed.</span></span> <span data-ttu-id="3dc68-201">Stav *Blokováno* této práce bude přepočítán, a pokud pro tuto práci nebudou žádné zbývající blokovací důvody, bude práce odblokována.</span><span class="sxs-lookup"><span data-stu-id="3dc68-201">The *Blocked* state of this work will be recomputed and, if there are no remaining blocking reasons for this work, the work will be unblocked.</span></span>
- <span data-ttu-id="3dc68-202">Libovolný uživatel otevře ID práce a vybere tlačítko **Zrušit relaci rozdělení práce** v podokně akcí.</span><span class="sxs-lookup"><span data-stu-id="3dc68-202">Any user opens the work ID and selects the **Cancel work split session** button on the Action Pane.</span></span> <span data-ttu-id="3dc68-203">Důvod blokování *Rozdělit práci* bude odstraněn a stav *Blokováno* této práce bude přepočítán, stejně jako když je zavřená stránka **Rozdělit práci**.</span><span class="sxs-lookup"><span data-stu-id="3dc68-203">The *Split work* blocking reason will be removed, and the *Blocked* state of this work will be recomputed, just as when the **Split work** page is closed.</span></span>

<span data-ttu-id="3dc68-204">Po odstranění důvodu blokování *Rozdělit práci* lze práci spustit na mobilním zařízení, pokud je stav **Blokováno** nastaven na *Ne* na ID práce.</span><span class="sxs-lookup"><span data-stu-id="3dc68-204">After the *Split work* blocking reason is removed, the work can be run on the mobile device, provided that the **Blocked** state is set to *No* on the work ID.</span></span>

## <a name="user-blocking-on-the-warehouse-app"></a><span data-ttu-id="3dc68-205">Blokování uživatelů v aplikaci Sklad</span><span class="sxs-lookup"><span data-stu-id="3dc68-205">User blocking on the warehouse app</span></span>

<span data-ttu-id="3dc68-206">Pokud se pokusíte použít apliaci skladu pro spuštění práce výdeje proti ID práce, která je rozdělována, zobrazí se následující chybová zpráva: „Práce s ID \#\#\#\# je v současné době rozdělována."</span><span class="sxs-lookup"><span data-stu-id="3dc68-206">If you try to use the warehouse app to run picking work against a work ID that is being split, you will receive the following error message: "The work with ID \#\#\#\# is currently being split."</span></span> <span data-ttu-id="3dc68-207">Pokud se se vám zobrazí tato zpráva, vyberte **Storno**.</span><span class="sxs-lookup"><span data-stu-id="3dc68-207">If you receive this message, select **Cancel**.</span></span> <span data-ttu-id="3dc68-208">Poté můžete pokračovat ve zpracování dalších prací.</span><span class="sxs-lookup"><span data-stu-id="3dc68-208">You can then continue to process other work.</span></span>

## <a name="other-blocked-operations"></a><span data-ttu-id="3dc68-209">Další blokované operace</span><span class="sxs-lookup"><span data-stu-id="3dc68-209">Other blocked operations</span></span>

<span data-ttu-id="3dc68-210">Veškeré operace, které upravují pracovní řádky, transakce zásob práce nebo odkazy doplňování, které souvisejí s prací, která je rozdělována, se nezdaří a zobrazí se následující chybová zpráva: „Práce s ID \#\#\#\# je právě rozdělována.“</span><span class="sxs-lookup"><span data-stu-id="3dc68-210">Any operations that modify work lines, work inventory transactions, or replenishment links that are related to work that is being split will fail, and the following error message will be shown: "The work with ID \#\#\#\# is currently being split."</span></span>
