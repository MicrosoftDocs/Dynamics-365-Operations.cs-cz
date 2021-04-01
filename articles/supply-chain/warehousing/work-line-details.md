---
title: Podrobnosti řádku práce
description: Toto téma uvádí informace o stránce Podrobnosti řádku práce, která zobrazuje kompletní, řaditelný a filtrovatelný seznam jednotlivých řádků práce v systému.
author: mirzaab
manager: tfehr
ms.date: 07/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSWorkLocationChange, WHSWorkLineDetails
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-07-01
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: 0cb182242a42443d5894b864523fc5f5fea9c5b1
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/15/2021
ms.locfileid: "5245099"
---
# <a name="work-line-details"></a><span data-ttu-id="b4bb0-103">Podrobnosti řádku práce</span><span class="sxs-lookup"><span data-stu-id="b4bb0-103">Work line details</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="b4bb0-104">Stránka **Podrobnosti řádku práce** zobrazuje kompletní, řaditelný a filtrovatelný seznam jednotlivých řádků práce v systému.</span><span class="sxs-lookup"><span data-stu-id="b4bb0-104">The **Work line details** page shows a comprehensive, sortable, and filterable list of the individual work lines in your system.</span></span> <span data-ttu-id="b4bb0-105">Umožňuje zobrazit úplný přehled prací, které jsou ve skladu plánovány a realizovány.</span><span class="sxs-lookup"><span data-stu-id="b4bb0-105">It provides a complete overview of work that is being planned and executed in the warehouse.</span></span> <span data-ttu-id="b4bb0-106">Mezi zobrazením všech řádků práce a zobrazením pouze otevřených řádků práce můžete snadno přepínat.</span><span class="sxs-lookup"><span data-stu-id="b4bb0-106">You can easily switch between viewing all work lines and viewing only open work lines.</span></span> <span data-ttu-id="b4bb0-107">Podrobnosti poskytované pro každý řádek práce zahrnují stav práce, číslo položky, skladové místo, pracovní množství, ID nákladu a ID dodávky.</span><span class="sxs-lookup"><span data-stu-id="b4bb0-107">Details that are provided for each line include the work status, item number, location, work quantity, load ID, and shipment ID.</span></span>

## <a name="turn-on-the-work-line-details-feature"></a><span data-ttu-id="b4bb0-108">Zapnutí funkce podrobností řádku práce</span><span class="sxs-lookup"><span data-stu-id="b4bb0-108">Turn on the work line details feature</span></span>

<span data-ttu-id="b4bb0-109">Než můžete použít tuto funkci, musíte ji zapnout ve svém systému.</span><span class="sxs-lookup"><span data-stu-id="b4bb0-109">Before you can use this feature, it must be turned on in your system.</span></span> <span data-ttu-id="b4bb0-110">Správci mohou pomocí nastavení [správa funkcí](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) zkontrolovat stav funkce a zapnout ji, je-li to potřeba.</span><span class="sxs-lookup"><span data-stu-id="b4bb0-110">Admins can use the [feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) settings to check the status of the feature and turn it on if it's required.</span></span> <span data-ttu-id="b4bb0-111">V pracovním prostoru **Správa funkcí** je tato funkce uvedena následovně:</span><span class="sxs-lookup"><span data-stu-id="b4bb0-111">In the **Feature management** workspace, the feature is listed in the following way:</span></span>

- <span data-ttu-id="b4bb0-112">**Modul:** *Řízení skladu*</span><span class="sxs-lookup"><span data-stu-id="b4bb0-112">**Module:** *Warehouse management*</span></span>
- <span data-ttu-id="b4bb0-113">**Název funkce:** *Podrobností řádku práce*</span><span class="sxs-lookup"><span data-stu-id="b4bb0-113">**Feature name:** *Work line details*</span></span>

## <a name="open-and-use-the-work-line-details-page"></a><span data-ttu-id="b4bb0-114">Otevření a použití stránky Podrobnosti řádku práce</span><span class="sxs-lookup"><span data-stu-id="b4bb0-114">Open and use the Work line details page</span></span>

<span data-ttu-id="b4bb0-115">Chcete-li zobrazit seznam podrobností řádku práce, přejděte na **Řízení skladu \> Práce \> Podrobnosti řádku práce**.</span><span class="sxs-lookup"><span data-stu-id="b4bb0-115">To view the list of work line details, go to **Warehouse management \> Work \> Work line details**.</span></span> <span data-ttu-id="b4bb0-116">Odtud můžete provést následující akce:</span><span class="sxs-lookup"><span data-stu-id="b4bb0-116">From here, you can perform the following actions:</span></span>

- <span data-ttu-id="b4bb0-117">Pole **Filtr** umožňuje hledat řádky, jež obsahují konkrétní hodnotu některého z dostupných parametrů.</span><span class="sxs-lookup"><span data-stu-id="b4bb0-117">Use the **Filter** field to search for lines that have a specific value for any available parameter.</span></span> <span data-ttu-id="b4bb0-118">(Dostupné parametry zahrnují mnoho parametrů, jež nejsou zobrazeny, například sloupce v mřížce.)</span><span class="sxs-lookup"><span data-stu-id="b4bb0-118">(Available parameters include many parameters that aren't shown as columns in the grid.)</span></span>
- <span data-ttu-id="b4bb0-119">Přepínám pomocí zaškrtávacího políčka **Zobrazit uzavřené** můžete zobrazit nebo skrýt uzavřené řádky.</span><span class="sxs-lookup"><span data-stu-id="b4bb0-119">Use the **Show closed** check box to show or hide closed lines.</span></span>
- <span data-ttu-id="b4bb0-120">Volbou **Zobrazit dimenze** můžete otevřít dialogové okno **Zobrazení dimenzí**, kde můžete vybrat, zda chcete zobrazit nebo skrýt sloupce různých dimenzí v mřížce.</span><span class="sxs-lookup"><span data-stu-id="b4bb0-120">Select **Display dimensions** to open the **Dimensions display** dialog box, where you can choose to show or hide various dimension columns in the grid.</span></span>
- <span data-ttu-id="b4bb0-121">Výběrem libovolného záhlaví sloupce otevřete nabídku, kde si můžete vybrat třídění nebo filtrování seznamu podle hodnot v příslušném sloupci.</span><span class="sxs-lookup"><span data-stu-id="b4bb0-121">Select any column heading to open a menu where you can choose to sort or filter the list by values in that column.</span></span>
- <span data-ttu-id="b4bb0-122">Vyberte řádek práce a poté položku **Změnit skladové místo**. Otevře se dialogové okno, v němž můžete změnit skladové místo tohoto řádku práce.</span><span class="sxs-lookup"><span data-stu-id="b4bb0-122">Select a work line, and then select **Change location** to open a dialog box where you can change the location for that work line.</span></span> <span data-ttu-id="b4bb0-123">Skladové místo, které určíte, přepíše nastavení podle směrnice skladového místa.</span><span class="sxs-lookup"><span data-stu-id="b4bb0-123">The location that you specify will override the setup of the location directive.</span></span>
- <span data-ttu-id="b4bb0-124">Vyberte řádek práce a poté možnost **Zrušit řádek práce**. Otevře se dialogové okno, v němž můžete částečně nebo úplně zredukovat množství v daném řádku práce.</span><span class="sxs-lookup"><span data-stu-id="b4bb0-124">Select a work line, and then select **Cancel work line** to open a dialog box where you can partially or fully reduce the quantity of that work line.</span></span>
- <span data-ttu-id="b4bb0-125">Úpravy množství.</span><span class="sxs-lookup"><span data-stu-id="b4bb0-125">Adjust quantities.</span></span>
- <span data-ttu-id="b4bb0-126">Zobrazení transakcí spojených s řádkem práce.</span><span class="sxs-lookup"><span data-stu-id="b4bb0-126">View the transactions behind any work line.</span></span>

## <a name="try-out-the-feature"></a><span data-ttu-id="b4bb0-127">Vyzkoušejte tuto funkci</span><span class="sxs-lookup"><span data-stu-id="b4bb0-127">Try out the feature</span></span>

<span data-ttu-id="b4bb0-128">Tato část obsahuje ukázku složenou ze tří částí, jež demonstruje, jak pracovat s podrobnostmi řádku práce.</span><span class="sxs-lookup"><span data-stu-id="b4bb0-128">This section provides a three-part demo that shows how to work with work line details.</span></span>

### <a name="make-sample-data-available"></a><span data-ttu-id="b4bb0-129">Příprava ukázkových dat</span><span class="sxs-lookup"><span data-stu-id="b4bb0-129">Make sample data available</span></span>

<span data-ttu-id="b4bb0-130">Chcete-li s touto ukázkou pracovat pomocí zde specifikovaných ukázkových záznamů a hodnot, musíte používat systém, ve kterém jsou nainstalována standardní [ukázková data](../../fin-ops-core/dev-itpro/deployment/deploy-demo-environment.md).</span><span class="sxs-lookup"><span data-stu-id="b4bb0-130">To work through this demo by using the sample records and values that are specified here, you must be on a system where the standard [demo data](../../fin-ops-core/dev-itpro/deployment/deploy-demo-environment.md) is installed.</span></span> <span data-ttu-id="b4bb0-131">Kromě toho musíte dříve, než začnete, také vybrat právnickou osobu **USMF**.</span><span class="sxs-lookup"><span data-stu-id="b4bb0-131">Additionally, you must select the **USMF** legal entity before you begin.</span></span>

<span data-ttu-id="b4bb0-132">Tuto ukázku můžete také použít jako vodítko při práci na produkčním systému.</span><span class="sxs-lookup"><span data-stu-id="b4bb0-132">You can also use this demo as guidance when you work on a production system.</span></span> <span data-ttu-id="b4bb0-133">Musíte však nahradit uvedené hodnoty vlastními hodnotami. Také možná budete postrádat některé typy požadovaných záznamů, jež jsou součástí standardních ukázkových dat.</span><span class="sxs-lookup"><span data-stu-id="b4bb0-133">However, you must substitute your own values, and you might be missing some types of required records that the standard demo data provides.</span></span>

### <a name="verify-that-the-scenario-setup-includes-enough-available-inventory"></a><span data-ttu-id="b4bb0-134">Ověření, že nastavení scénáře obsahuje dostatečné dostupné zásoby</span><span class="sxs-lookup"><span data-stu-id="b4bb0-134">Verify that the scenario setup includes enough available inventory</span></span>

<span data-ttu-id="b4bb0-135">Pokud pracujete s ukázkovými daty **USMF**, měli byste se nejprve ujistit, že je váš systém nastaven tak, aby na každém relevantním skladovém místě pro výdej byly k dispozici dostatečné zásoby.</span><span class="sxs-lookup"><span data-stu-id="b4bb0-135">If you're working with the **USMF** demo data, you should first make sure that your system is set up so that enough inventory is available at each relevant pick location.</span></span> <span data-ttu-id="b4bb0-136">V rámci této ukázky se očekává, že budete mít k dispozici následující zásoby:</span><span class="sxs-lookup"><span data-stu-id="b4bb0-136">For this demo, the expectation is that you have the following inventory available:</span></span>

- <span data-ttu-id="b4bb0-137">**Položka M9200:** 45 ks</span><span class="sxs-lookup"><span data-stu-id="b4bb0-137">**Item M9200:** 45 ea.</span></span> <span data-ttu-id="b4bb0-138">(nebo více)</span><span class="sxs-lookup"><span data-stu-id="b4bb0-138">(or more)</span></span>
- <span data-ttu-id="b4bb0-139">**Položka M9202:** 10 ks</span><span class="sxs-lookup"><span data-stu-id="b4bb0-139">**Item M9202:** 10 ea.</span></span> <span data-ttu-id="b4bb0-140">(nebo více)</span><span class="sxs-lookup"><span data-stu-id="b4bb0-140">(or more)</span></span>

<span data-ttu-id="b4bb0-141">Chcete-li ověřit, že máte k dispozici dostatečné zásoby, případně provést potřebné úpravy, poustupujte podle těchto kroků.</span><span class="sxs-lookup"><span data-stu-id="b4bb0-141">Follow these steps to verify that enough inventory is available and to make any adjustments that are required.</span></span>

1. <span data-ttu-id="b4bb0-142">Přejděte do **Řízení skladu \> Nastavení \> Směrnice skladového místa** a určete, která výdejová skladová místa se používají pro výdej prodejních objednávek ve skladu 51.</span><span class="sxs-lookup"><span data-stu-id="b4bb0-142">Go to **Warehouse management \> Setup \> Location directives**, and determine which picking locations are used for sales order picking at warehouse 51.</span></span> <span data-ttu-id="b4bb0-143">(Další informace naleznete v tématu [Řízení práce ve skladu pomocí šablon práce a směrnic skladového místa](control-warehouse-location-directives.md).)</span><span class="sxs-lookup"><span data-stu-id="b4bb0-143">(For more information, see [Control warehouse work by using work templates and location directives](control-warehouse-location-directives.md).)</span></span>
1. <span data-ttu-id="b4bb0-144">Zkontrolujte úrovně zásob na příslušných skladových místech.</span><span class="sxs-lookup"><span data-stu-id="b4bb0-144">Check the inventory levels at the relevant locations.</span></span>
1. <span data-ttu-id="b4bb0-145">Dle potřeby zásoby upravte.</span><span class="sxs-lookup"><span data-stu-id="b4bb0-145">Adjust inventory as required.</span></span> <span data-ttu-id="b4bb0-146">K úpravě úrovně zásob můžete vytvořit ruční pohyby, použít doplnění nebo jakýkoli jiný tok.</span><span class="sxs-lookup"><span data-stu-id="b4bb0-146">You can create manual movements, use replenishment, or apply any other flow to adjust the inventory.</span></span>

### <a name="part-1-create-picking-work"></a><span data-ttu-id="b4bb0-147">Část 1: Vytvoření práce výdeje</span><span class="sxs-lookup"><span data-stu-id="b4bb0-147">Part 1: Create picking work</span></span>

<span data-ttu-id="b4bb0-148">Než začnete vytvářet práci, ujistěte se, že máte sklad nastaven tak, aby na požadavky na práci reagoval očekávaným způsobem.</span><span class="sxs-lookup"><span data-stu-id="b4bb0-148">Before you start to create work, make sure that your warehouse is set up to respond to work requests in the expected manner.</span></span>

<span data-ttu-id="b4bb0-149">Při vytváření práce výdeje postupujte takto:</span><span class="sxs-lookup"><span data-stu-id="b4bb0-149">Follow these steps to create some picking work.</span></span>

1. <span data-ttu-id="b4bb0-150">Přejděte na **Prodej a marketing \> Prodejní objednávky \> Všechny prodejní objednávky**.</span><span class="sxs-lookup"><span data-stu-id="b4bb0-150">Go to **Sales and marketing \> Sales orders \> All sales orders**.</span></span>
1. <span data-ttu-id="b4bb0-151">Kliknutím na možnost **Nová** otevřete dialogové okno **Vytvoření prodejní objednávky**.</span><span class="sxs-lookup"><span data-stu-id="b4bb0-151">Select **New** to open the **Create sales order** dialog box.</span></span>
1. <span data-ttu-id="b4bb0-152">V dialogovém okně **Vytvoření prodejní objednávky** nastavte následující hodnoty:</span><span class="sxs-lookup"><span data-stu-id="b4bb0-152">In the **Create sales order** dialog box, set the following values:</span></span>

    - <span data-ttu-id="b4bb0-153">Na záložce s náhledem **Odběratel** zadejte do pole **Účet odběratele** hodnotu _US-001_.</span><span class="sxs-lookup"><span data-stu-id="b4bb0-153">On the **Customer** FastTab, set the **Customer account** field to _US-001_.</span></span>
    - <span data-ttu-id="b4bb0-154">Na záložce s náhledem **Obecné** zadejte do pole **Sklad** hodnotu _51_.</span><span class="sxs-lookup"><span data-stu-id="b4bb0-154">On the **General** FastTab, set the **Warehouse** field to _51_.</span></span>

1. <span data-ttu-id="b4bb0-155">Vyberte **OK**, prodejní objednávka se vytvoří a dialogové okno se zavře.</span><span class="sxs-lookup"><span data-stu-id="b4bb0-155">Select **OK** to create the sales order and close the dialog box.</span></span>
1. <span data-ttu-id="b4bb0-156">Otevře se nová prodejní objednávka.</span><span class="sxs-lookup"><span data-stu-id="b4bb0-156">Your new sales order is opened.</span></span> <span data-ttu-id="b4bb0-157">Obsahuje nový prázdný řádek v mřížce **Řádky prodejních objednávek**.</span><span class="sxs-lookup"><span data-stu-id="b4bb0-157">It includes a new, empty row in the **Sales order lines** grid.</span></span> <span data-ttu-id="b4bb0-158">Na tomto řádku nastavte následující hodnoty:</span><span class="sxs-lookup"><span data-stu-id="b4bb0-158">On this order line, set the following values:</span></span>

    - <span data-ttu-id="b4bb0-159">**Číslo položky:** _M9200_</span><span class="sxs-lookup"><span data-stu-id="b4bb0-159">**Item number:** _M9200_</span></span>
    - <span data-ttu-id="b4bb0-160">**Množství:** _20_</span><span class="sxs-lookup"><span data-stu-id="b4bb0-160">**Quantity:** _20_</span></span>
    - <span data-ttu-id="b4bb0-161">**Jednotka:** _EA_</span><span class="sxs-lookup"><span data-stu-id="b4bb0-161">**Unit:** _ea_</span></span>

1. <span data-ttu-id="b4bb0-162">Vyberte nový řádek objednávky a poté v nabídce **Zásoby** vyberte možnost **Rezervace**. Otevře se stránka **Rezervace**.</span><span class="sxs-lookup"><span data-stu-id="b4bb0-162">Select the new order line, and then, on the **Inventory** menu, select **Reservation** to open the **Reservation** page.</span></span>
1. <span data-ttu-id="b4bb0-163">Na stránce **Rezervace** klikněte na **Rezervovat šarži**. Ve skladu se provede rezervace celého množství vybraného řádku.</span><span class="sxs-lookup"><span data-stu-id="b4bb0-163">On the **Reservation** page, select **Reserve lot** to reserve the selected line's full quantity in the warehouse.</span></span>
1. <span data-ttu-id="b4bb0-164">Zavřete stránku **Rezervace** a vraťte se k prodejní objednávce.</span><span class="sxs-lookup"><span data-stu-id="b4bb0-164">Close the **Reservation** page to return to the sales order.</span></span>
1. <span data-ttu-id="b4bb0-165">V podokně Akce na kartě **Sklad** vyberte možnost **Uvolnit do skladu**.</span><span class="sxs-lookup"><span data-stu-id="b4bb0-165">On the Action Pane, on the **Warehouse** tab, select **Release to warehouse**.</span></span> <span data-ttu-id="b4bb0-166">Systém vytvoří dodávku, přidá ji k novému nákladu a vytvoří požadovanou práci.</span><span class="sxs-lookup"><span data-stu-id="b4bb0-166">The system creates a shipment, adds it to a new load, and creates the required work.</span></span>
1. <span data-ttu-id="b4bb0-167">Vytvořte druhou prodejní objednávku pro stejný účet odběratele a sklad, jaké jste použili pro první objednávku.</span><span class="sxs-lookup"><span data-stu-id="b4bb0-167">Create a second sales order for the same customer account and warehouse that you used for the first order.</span></span> <span data-ttu-id="b4bb0-168">K této objednávce přidejte následující dva řádky objednávky:</span><span class="sxs-lookup"><span data-stu-id="b4bb0-168">Add the following two order lines to this order:</span></span>

    - <span data-ttu-id="b4bb0-169">**Řádek 1:** Nastavte v poli **Číslo položky** hodnotu _M9200_, v poli **Množství** hodnotu _25_ a v poli **Jednotka** hodnotu _ks_.</span><span class="sxs-lookup"><span data-stu-id="b4bb0-169">**Line 1:** Set the **Item number** field to _M9200_, the **Quantity** field to _25_, and the **Unit** field to _ea_.</span></span>
    - <span data-ttu-id="b4bb0-170">**Řádek 2:** Nastavte v poli **Číslo položky** hodnotu _M9202_, v poli **Množství** hodnotu _10_ a v poli **Jednotka** hodnotu _ks_.</span><span class="sxs-lookup"><span data-stu-id="b4bb0-170">**Line 2:** Set the **Item number** field to _M9202_, the **Quantity** field to _10_, and the **Unit** field to _ea_.</span></span>

1. <span data-ttu-id="b4bb0-171">Zopakujte kroky 6 až 8 a rezervujte zásoby pro každý řádek objednávky (vždy po jednom). Poté zopakujte krok 9 a uvolněte objednávku do skladu.</span><span class="sxs-lookup"><span data-stu-id="b4bb0-171">Repeat steps 6 through 8 to reserve the inventory for each order line (one at a time), and then repeat step 9 to release the order to the warehouse.</span></span>

### <a name="part-2-change-the-location-for-a-work-line"></a><span data-ttu-id="b4bb0-172">Část 2: Změna skladového místa pro řádek práce</span><span class="sxs-lookup"><span data-stu-id="b4bb0-172">Part 2: Change the location for a work line</span></span>

1. <span data-ttu-id="b4bb0-173">Přejděte do nabídky **Řízení skladu \> Práce \> Podrobnosti řádku práce**.</span><span class="sxs-lookup"><span data-stu-id="b4bb0-173">Go to **Warehouse management \> Work \> Work line details**.</span></span>
1. <span data-ttu-id="b4bb0-174">Najděte a vyberte jeden řádek práce, který jste v rámci této ukázky vytvořili.</span><span class="sxs-lookup"><span data-stu-id="b4bb0-174">Find and select one of the work lines that you created for this demo.</span></span>
1. <span data-ttu-id="b4bb0-175">Vyberte možnost **Změnit skladové místo**. Otevře se dialogové okno **Výběr nového skladového místa**.</span><span class="sxs-lookup"><span data-stu-id="b4bb0-175">Select **Change location** to open the **Select new location** dialog box.</span></span>
1. <span data-ttu-id="b4bb0-176">V dialogovém okně **Výběr nového skladového místa** vyberte v poli **Skladové místo** nové skladové místo pro řádek práce.</span><span class="sxs-lookup"><span data-stu-id="b4bb0-176">In the **Select new location** dialog box, in the **Location** field, select a new location for the work line.</span></span>
1. <span data-ttu-id="b4bb0-177">Vyberte **OK**, pokud chcete změnu použít. Dialogové okno se zavře.</span><span class="sxs-lookup"><span data-stu-id="b4bb0-177">Select **OK** to apply your change and close the dialog box.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="b4bb0-178">Změnu skladového místa můžete zadat, pouze když je na novém skladovém místě k dispozici dostatek zásob (pro výdej) nebo pokud skladové místo předává ověření typu skladového místa (pro vložení).</span><span class="sxs-lookup"><span data-stu-id="b4bb0-178">You can submit location changes only if the new location has enough inventory available (for a pick), or if it passes location-type validation (for a put).</span></span>

### <a name="part-3-change-the-quantity-of-a-work-line-or-cancel-a-work-line"></a><span data-ttu-id="b4bb0-179">Část 3: Změna množství na řádku práce nebo zrušení řádku práce</span><span class="sxs-lookup"><span data-stu-id="b4bb0-179">Part 3: Change the quantity of a work line or cancel a work line</span></span>

1. <span data-ttu-id="b4bb0-180">Přejděte do nabídky **Řízení skladu \> Práce \> Podrobnosti řádku práce**.</span><span class="sxs-lookup"><span data-stu-id="b4bb0-180">Go to **Warehouse management \> Work \> Work line details**.</span></span>
1. <span data-ttu-id="b4bb0-181">Najděte a vyberte jeden řádek práce, který jste v rámci této ukázky vytvořili.</span><span class="sxs-lookup"><span data-stu-id="b4bb0-181">Find and select one of the work lines that you created for this demo.</span></span> <span data-ttu-id="b4bb0-182">Množství můžete zrušit nebo změnit pouze pro řádky práce, kde je typ práce _Výdej_.</span><span class="sxs-lookup"><span data-stu-id="b4bb0-182">Note that you can cancel or change quantities only for work lines where the work type is _pick_.</span></span>
1. <span data-ttu-id="b4bb0-183">Vyberte možnost **Zrušit řádek práce**, otevře se dialogové okno **Množství ke zrušení**.</span><span class="sxs-lookup"><span data-stu-id="b4bb0-183">Select **Cancel work line** to open the **Quantity to cancel** dialog box.</span></span>
1. <span data-ttu-id="b4bb0-184">V dialogovém okně **Množství ke zrušení** zadejte do pole **Množství** hodnotu odpovídající množství, jež se má *odečíst od* množství, jež je na řádku aktuálně zadáno.</span><span class="sxs-lookup"><span data-stu-id="b4bb0-184">In the **Quantity to cancel** dialog box, change the value in the **Quantity** field to specify the quantity that should be *subtracted from* the quantity that is currently specified for the line.</span></span> <span data-ttu-id="b4bb0-185">Ve výchozím nastavení se v poli **Množství** zobrazuje plné množství.</span><span class="sxs-lookup"><span data-stu-id="b4bb0-185">By default, the **Quantity** field shows the full quantity.</span></span>

    - <span data-ttu-id="b4bb0-186">Pokud zrušíte celé množství, změní se hodnota položky **Stav práce** na _Zrušeno_. V poli **Množství práce** se ale bude stále zobrazovat původní hodnota.</span><span class="sxs-lookup"><span data-stu-id="b4bb0-186">If you cancel the full quantity, the **Work status** value will be changed to _Canceled_, but the **Work quantity** field will still show the original value.</span></span>
    - <span data-ttu-id="b4bb0-187">Pokud zrušíte pouze část množství, hodnota v poli **Množství práce** se změní a bude zobrazovat novou hodnotu, Hodnota **Stav práce** se nezmění.</span><span class="sxs-lookup"><span data-stu-id="b4bb0-187">If you cancel just part of the quantity, the **Work quantity** field will be updated to show the new value, but the **Work status** value won't change.</span></span>

1. <span data-ttu-id="b4bb0-188">Vyberte **OK**, pokud chcete změnu použít. Dialogové okno se zavře.</span><span class="sxs-lookup"><span data-stu-id="b4bb0-188">Select **OK** to apply your change and close the dialog box.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="b4bb0-189">Pokud zrušíte jen část množství řádku práce, musíte také odstranit již neplatné množství z řádku nákladu.</span><span class="sxs-lookup"><span data-stu-id="b4bb0-189">If you cancel just part of the quantity for a work line, you must also remove the obsolete quantity from the load line.</span></span> <span data-ttu-id="b4bb0-190">V opačném případě, pokud nebude dodávka nastavena správně, nebude možné potvrdit řádek nákladu k odeslání.</span><span class="sxs-lookup"><span data-stu-id="b4bb0-190">Otherwise, unless under-delivery is set up correctly, the load line can't be ship-confirmed.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]