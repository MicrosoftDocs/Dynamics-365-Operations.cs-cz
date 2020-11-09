---
title: Doplnění prahu zóny
description: Doplňování na základě zón používá strategii minimálního/maximálního (min./max.) doplňování, ale místo pouze jednotlivých skladových míst vyhodnocuje celé skladové zóny. Skladoví manažeři mohou díky tomu rychleji zjistit, když je třeba do zóny vychystávání dodat další zásoby.
author: Mirzaab
manager: tfehr
ms.date: 07/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSReplenishmentTemplates, WHSLocDirHint, WHSLocDirTable
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-07-01
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: e13b5fd895fca7f8fe77809348d63ed8867dea9e
ms.sourcegitcommit: a36a4f9915ae3eb36bf8220111cf1486387713d9
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/16/2020
ms.locfileid: "4017315"
---
# <a name="zone-threshold-replenishment"></a><span data-ttu-id="1125d-104">Doplnění prahu zóny</span><span class="sxs-lookup"><span data-stu-id="1125d-104">Zone threshold replenishment</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="1125d-105">Doplňování na základě zón používá strategii minimálního/maximálního (min./max.) [doplňování](replenishment.md), ale místo pouze jednotlivých skladových míst vyhodnocuje celé skladové zóny.</span><span class="sxs-lookup"><span data-stu-id="1125d-105">Zone-based replenishment uses a minimum/maximum (min/max) [replenishment](replenishment.md) strategy, but it evaluates whole warehouse zones instead of just individual locations.</span></span> <span data-ttu-id="1125d-106">Skladoví manažeři mohou díky tomu rychleji zjistit, když je třeba do zóny vychystávání dodat další zásoby.</span><span class="sxs-lookup"><span data-stu-id="1125d-106">Therefore, warehouse managers can more quickly learn when additional inventory is required in a picking zone.</span></span>

<span data-ttu-id="1125d-107">Nastavení se u této funkce podobá nastavení pro doplňování podle skladového místa.</span><span class="sxs-lookup"><span data-stu-id="1125d-107">The setup for this feature resembles the setup for location-based replenishment.</span></span> <span data-ttu-id="1125d-108">Když však nastavíte šablonu pro min./max. doplňování, můžete také určit, zda má být příslušná mezní hodnota vyhodnocována podle skladového místa nebo zóny.</span><span class="sxs-lookup"><span data-stu-id="1125d-108">However, when you set up a template for min/max replenishment, you can also specify whether the threshold should be evaluated per location or per zone.</span></span> <span data-ttu-id="1125d-109">Pokud nastavíte vyhodnocování podle zón, musíte do dotazu pro výběr zóny přidat konkrétní zóny.</span><span class="sxs-lookup"><span data-stu-id="1125d-109">If you set up evaluation that is based on zones, you must add specific zones to the zone selection query.</span></span>

<span data-ttu-id="1125d-110">Podobně jako u min./max. doplňování na základě skladového místa je min./max. doplňování na základě zón založeno na nastavení mezní hodnoty minimálních zásob, jež spouští vytvoření úlohy doplnění vybraných položek.</span><span class="sxs-lookup"><span data-stu-id="1125d-110">Like location-based min/max replenishment, zone-based min/max replenishment is based the setup of a minimum inventory threshold that triggers the creation of replenishment work for selected items.</span></span> <span data-ttu-id="1125d-111">Tato doplňovací úloha zvýší zásoby až do maximální mezní hodnoty stanovené pro zónu.</span><span class="sxs-lookup"><span data-stu-id="1125d-111">This replenishment work will increase inventory up to the specified maximum threshold for the zone.</span></span>

> [!NOTE]
> <span data-ttu-id="1125d-112">V aktuální vydané verzi nejsou podporovány procesy doplňování podle zón pro varianty produktů.</span><span class="sxs-lookup"><span data-stu-id="1125d-112">Zone replenishment processes for product variants aren't supported in the current release.</span></span>


<span data-ttu-id="1125d-113">Na rozdíl od min./max. doplňování založeného na skladovém místě nevyžaduje min./max. doplňování založené na zónách, aby se u pevných skladových míst vyhodnocovalo, zda lze daná skladová místa využít k uskladnění konkrétní položky.</span><span class="sxs-lookup"><span data-stu-id="1125d-113">Unlike location-based min/max replenishment, zone-based min/max replenishment doesn't require fixed locations to evaluate whether locations should store a specific item.</span></span> <span data-ttu-id="1125d-114">Proto umožňuje doplňování podle zón použít min./max. doplňování, i když nemáte pevná skladová místa pro každou položku nebo variantu položky ve skladu.</span><span class="sxs-lookup"><span data-stu-id="1125d-114">Therefore, zone-based replenishment lets you use min/max replenishment even if you don't have fixed locations for each item or item variant in the warehouse.</span></span> <span data-ttu-id="1125d-115">Když množství v zóně klesne pod stanovenou mezní hodnotu, vytvoří se doplňovací úloha.</span><span class="sxs-lookup"><span data-stu-id="1125d-115">When a quantity in the zone falls below the specified minimum threshold, replenishment work is created.</span></span> <span data-ttu-id="1125d-116">Směrnice skladových míst určují, na která konkrétní skladová místa mají být zásoby umístěny.</span><span class="sxs-lookup"><span data-stu-id="1125d-116">Location directives will determine which specific location the inventory should be put into.</span></span>

## <a name="turn-on-the-zone-threshold-replenishment-feature"></a><span data-ttu-id="1125d-117">Zapnutí funkce Zónové doplňování podle mezních hodnot</span><span class="sxs-lookup"><span data-stu-id="1125d-117">Turn on the Zone threshold replenishment feature</span></span>

<span data-ttu-id="1125d-118">Než můžete použít funkci *Zónové doplňování podle mezních hodnot* , musíte ji v systému zapnout.</span><span class="sxs-lookup"><span data-stu-id="1125d-118">Before you can use the *Zone threshold replenishment* feature, it must be turned on in your system.</span></span> <span data-ttu-id="1125d-119">Správci mohou pomocí nastavení [správa funkcí](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) zkontrolovat stav funkce a zapnout ji, je-li to potřeba.</span><span class="sxs-lookup"><span data-stu-id="1125d-119">Admins can use the [feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) settings to check the status of the feature and turn it on if it's required.</span></span> <span data-ttu-id="1125d-120">V pracovním prostoru **Správa funkcí** je tato funkce uvedena následovně:</span><span class="sxs-lookup"><span data-stu-id="1125d-120">In the **Feature management** workspace, the feature is listed in the following way:</span></span>

- <span data-ttu-id="1125d-121">**Modul:** *Řízení skladu*</span><span class="sxs-lookup"><span data-stu-id="1125d-121">**Module:** *Warehouse management*</span></span>
- <span data-ttu-id="1125d-122">**Název funkce:** *Zónové doplňování podle mezních hodnot*</span><span class="sxs-lookup"><span data-stu-id="1125d-122">**Feature name:** *Zone threshold replenishment*</span></span>

## <a name="set-up-zone-based-replenishment"></a><a name="setup"></a><span data-ttu-id="1125d-123">Nastavení zónového doplňování</span><span class="sxs-lookup"><span data-stu-id="1125d-123">Set up zone-based replenishment</span></span>

<span data-ttu-id="1125d-124">Chcete-li nastavit doplňování podle zón, musíte v systému nakonfigurovat několik částí.</span><span class="sxs-lookup"><span data-stu-id="1125d-124">To set up zone-based replenishment, you must configure several parts of the system.</span></span> <span data-ttu-id="1125d-125">Tato část představuje různá nastavení a uvádí ukázkové datové hodnoty, které můžete zadat, pokud chcete využít scénář na konci tohoto tématu.</span><span class="sxs-lookup"><span data-stu-id="1125d-125">This section introduces the various settings and provides demo data values that you can enter if you want to work through the scenario at the end of this topic.</span></span>

### <a name="set-up-directive-codes"></a><span data-ttu-id="1125d-126">Nastavení kódů předpisů</span><span class="sxs-lookup"><span data-stu-id="1125d-126">Set up directive codes</span></span>

<span data-ttu-id="1125d-127">[Kódy předpisů](control-warehouse-location-directives.md) vám umožňují být konkrétnější při definování šablony skladového místa, jež se používá v šabloně práce.</span><span class="sxs-lookup"><span data-stu-id="1125d-127">[Directive codes](control-warehouse-location-directives.md) let you be more specific when you define the location template that is used in a work template.</span></span> <span data-ttu-id="1125d-128">Každý kód vytváří společnou hodnotu, na kterou lze při konfiguraci šablony každého typu odkázat.</span><span class="sxs-lookup"><span data-stu-id="1125d-128">Each code establishes a common value that you can refer to when you configure each type of template.</span></span>

#### <a name="view-and-edit-directive-codes"></a><span data-ttu-id="1125d-129">Zobrazení a úpravy kódů předpisů</span><span class="sxs-lookup"><span data-stu-id="1125d-129">View and edit directive codes</span></span>

<span data-ttu-id="1125d-130">Chcete-li zobrazit nebo upravit kódy předpisů, přejděte do **Řízení skladu \> Nastavení \> Kódy předpisů**.</span><span class="sxs-lookup"><span data-stu-id="1125d-130">To view or edit your directive codes, go to **Warehouse management \> Setup \> Directive codes**.</span></span>

#### <a name="prepare-demo-data-directive-codes"></a><span data-ttu-id="1125d-131">Příprava ukázkových dat kódů předpisů</span><span class="sxs-lookup"><span data-stu-id="1125d-131">Prepare demo data directive codes</span></span>

<span data-ttu-id="1125d-132">Tento příklad ukazuje, jak připravit kódy předpisů.</span><span class="sxs-lookup"><span data-stu-id="1125d-132">This example shows how to prepare a directive code.</span></span> <span data-ttu-id="1125d-133">Pokud plánujete využít scénář uvedený na konci tohoto tématu, použijte zde uvedené hodnoty ukázkových dat.</span><span class="sxs-lookup"><span data-stu-id="1125d-133">If you're planning to work through the scenario at the end of this topic, use the demo data values that are provided here.</span></span> <span data-ttu-id="1125d-134">Pokud ne, použijte vlastní hodnoty.</span><span class="sxs-lookup"><span data-stu-id="1125d-134">Otherwise, use your own values.</span></span>

1. <span data-ttu-id="1125d-135">Pro práci s ukázkovými daty vyberte právnickou osobu **USMF**.</span><span class="sxs-lookup"><span data-stu-id="1125d-135">Select the **USMF** legal entity to work with the demo data.</span></span>
1. <span data-ttu-id="1125d-136">Přejděte na **Řízení skladu \> Nastavení \> Kódy předpisů**.</span><span class="sxs-lookup"><span data-stu-id="1125d-136">Go to **Warehouse management \> Setup \> Directive codes**.</span></span>
1. <span data-ttu-id="1125d-137">V podokně Akce vyberte možnost **Nový**. Tím se přidá řádek do mřížky.</span><span class="sxs-lookup"><span data-stu-id="1125d-137">On the Action Pane, select **New** to add a row to the grid.</span></span>
1. <span data-ttu-id="1125d-138">Na novém řádku nastavte následující hodnoty:</span><span class="sxs-lookup"><span data-stu-id="1125d-138">In the new row, set the following values:</span></span>

    - <span data-ttu-id="1125d-139">**Kód předpisu:** _Zone replen_</span><span class="sxs-lookup"><span data-stu-id="1125d-139">**Directive code:** _Zone replen_</span></span>
    - <span data-ttu-id="1125d-140">**Popis předpisu:**_Doplňování podle zóny_</span><span class="sxs-lookup"><span data-stu-id="1125d-140">**Directive description:** _Zone replenishment_</span></span>

1. <span data-ttu-id="1125d-141">Kliknutím na tlačítko **Uložit** uložte nový kód.</span><span class="sxs-lookup"><span data-stu-id="1125d-141">Select **Save** to save the new code.</span></span>

### <a name="set-up-replenishment-templates"></a><span data-ttu-id="1125d-142">Nastavit šablony doplnění</span><span class="sxs-lookup"><span data-stu-id="1125d-142">Set up replenishment templates</span></span>

<span data-ttu-id="1125d-143">[Šablony doplnění metodou min/max.](tasks/set-up-min-max-replenishment-process.md) jsou primární mechanismus pro udržování optimálních úrovní zásob na výdejních skladových místech.</span><span class="sxs-lookup"><span data-stu-id="1125d-143">[Min/max replenishment templates](tasks/set-up-min-max-replenishment-process.md) are the primary mechanism for maintaining optimal levels in picking locations.</span></span> <span data-ttu-id="1125d-144">V těchto šablonách musíte nastavit pravidla, která budou použita k doplňování skladových zásob.</span><span class="sxs-lookup"><span data-stu-id="1125d-144">In these templates, you must set up the rules that will be used to replenish inventory in the warehouse.</span></span> <span data-ttu-id="1125d-145">Tyto šablony lze mimo jiné použít i pro doplňování podle zón.</span><span class="sxs-lookup"><span data-stu-id="1125d-145">The replenishment that the templates can be used for includes zone-based replenishment.</span></span>

#### <a name="view-and-edit-replenishment-templates"></a><span data-ttu-id="1125d-146">Zobrazení a úprava šablon doplňování</span><span class="sxs-lookup"><span data-stu-id="1125d-146">View and edit replenishment templates</span></span>

<span data-ttu-id="1125d-147">Šablona doplnění je sada pravidel, která určuje, kdy a jak je skladové místo doplňováno.</span><span class="sxs-lookup"><span data-stu-id="1125d-147">A replenishment template is a set of rules that control when and how a location is replenished.</span></span> <span data-ttu-id="1125d-148">Vyberete šablonu, která určuje, kdy a jak má být doplňování prováděno.</span><span class="sxs-lookup"><span data-stu-id="1125d-148">You select a template to control when and how replenishment is done.</span></span> <span data-ttu-id="1125d-149">Chcete-li zobrazit nebo upravit šablony doplňování, přejděte na **Řízení skladu \> Nastavení \> Doplnění \> Šablony doplnění**.</span><span class="sxs-lookup"><span data-stu-id="1125d-149">To view or edit your replenishment templates, go to **Warehouse management \> Setup \> Replenishment \> Replenishment templates**.</span></span>

#### <a name="prepare-a-demo-data-replenishment-template"></a><span data-ttu-id="1125d-150">Příprava ukázkových dat pro šablonu doplnění</span><span class="sxs-lookup"><span data-stu-id="1125d-150">Prepare a demo data replenishment template</span></span>

<span data-ttu-id="1125d-151">Tento příklad ukazuje, jak připravit šablonu doplnění.</span><span class="sxs-lookup"><span data-stu-id="1125d-151">This example shows how to prepare a replenishment template.</span></span> <span data-ttu-id="1125d-152">Pokud plánujete využít scénář uvedený na konci tohoto tématu, použijte zde uvedené hodnoty ukázkových dat.</span><span class="sxs-lookup"><span data-stu-id="1125d-152">If you're planning to work through the scenario at the end of this topic, use the demo data values that are provided here.</span></span> <span data-ttu-id="1125d-153">Pokud ne, použijte vlastní hodnoty.</span><span class="sxs-lookup"><span data-stu-id="1125d-153">Otherwise, use your own values.</span></span>

1. <span data-ttu-id="1125d-154">Pro práci s ukázkovými daty vyberte právnickou osobu **USMF**.</span><span class="sxs-lookup"><span data-stu-id="1125d-154">Select the **USMF** legal entity to work with the demo data.</span></span>
1. <span data-ttu-id="1125d-155">Přejděte na **Řízení skladu \> Nastavení \> Doplnění \> Šablony doplnění**.</span><span class="sxs-lookup"><span data-stu-id="1125d-155">Go to **Warehouse management \> Setup \> Replenishment \> Replenishment templates**.</span></span>
1. <span data-ttu-id="1125d-156">Vyberte možnost **Upravit** , tím přepnete stránku do režimu úprav.</span><span class="sxs-lookup"><span data-stu-id="1125d-156">Select **Edit** to put the page into edit mode.</span></span>
1. <span data-ttu-id="1125d-157">V podokně Akce vyberte možnost **Nový**. Tím se přidá řádek do mřížky **Přehled**.</span><span class="sxs-lookup"><span data-stu-id="1125d-157">On the Action Pane, select **New** to add a row to the **Overview** grid.</span></span>
1. <span data-ttu-id="1125d-158">Na novém řádku nastavte následující hodnoty.</span><span class="sxs-lookup"><span data-stu-id="1125d-158">In the new row, set the following values.</span></span> <span data-ttu-id="1125d-159">Potvrďte výchozí hodnoty pro všechna ostatní pole.</span><span class="sxs-lookup"><span data-stu-id="1125d-159">Accept the default values for all other fields.</span></span>

    - <span data-ttu-id="1125d-160">**Šablona doplnění:** _Zone min/max replen_</span><span class="sxs-lookup"><span data-stu-id="1125d-160">**Replenish template:** _Zone min/max replen_</span></span>
    - <span data-ttu-id="1125d-161">**Popis:** _Doplňování metodou min./max. podle zón_</span><span class="sxs-lookup"><span data-stu-id="1125d-161">**Description:** _Zone min/max replenishment_</span></span>
    - <span data-ttu-id="1125d-162">**Typ doplňování:** _Minimum nebo maximum_</span><span class="sxs-lookup"><span data-stu-id="1125d-162">**Replenishment type:** _Minimum or maximum_</span></span>

1. <span data-ttu-id="1125d-163">Zvolte **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="1125d-163">Select **Save**.</span></span>
1. <span data-ttu-id="1125d-164">Zatímco je nový řádek stále vybrán v mřížce **Přehled** , stiskněte tlačítko **Nový** nad mřížkou **Podrobnosti šablony doplnění**. Tím přidáte řádek, který bude přiřazen k právě vytvořené šabloně doplnění *Zone Min/Max replen*.</span><span class="sxs-lookup"><span data-stu-id="1125d-164">While the new row is still selected in the **Overview** grid, select **New** above the **Replenishment Template Details** grid to add a row that is associated with the *Zone Min/Max replen* replenishment template that you just created.</span></span>
1. <span data-ttu-id="1125d-165">Na novém řádku nastavte následující hodnoty:</span><span class="sxs-lookup"><span data-stu-id="1125d-165">In the new row, set the following values:</span></span>

    - <span data-ttu-id="1125d-166">**Pořadové číslo:** Zadejte _1_.</span><span class="sxs-lookup"><span data-stu-id="1125d-166">**Sequence number:** Enter _1_.</span></span>
    - <span data-ttu-id="1125d-167">**Popis:** Zadejte _Doplnění ve výdejové zóně_.</span><span class="sxs-lookup"><span data-stu-id="1125d-167">**Description:** Enter _Pick zone replenishment_.</span></span>
    - <span data-ttu-id="1125d-168">**Jednotka doplnění:** Vyberte _ks_.</span><span class="sxs-lookup"><span data-stu-id="1125d-168">**Replenishment unit:** Select _ea_.</span></span>
    - <span data-ttu-id="1125d-169">**Typ požadavku:** Toto pole ponechte prázdné.</span><span class="sxs-lookup"><span data-stu-id="1125d-169">**Request type:** Leave this field blank.</span></span>
    - <span data-ttu-id="1125d-170">**Kód předpisu:** toto pole spojuje šablonu doplnění se směrnicí skladového místa.</span><span class="sxs-lookup"><span data-stu-id="1125d-170">**Directive code:** This field links the replenishment template with a location directive.</span></span> <span data-ttu-id="1125d-171">Vyberte předtím vybraný kód předpisu z ukázkových dat ( _Zone replen_ ).</span><span class="sxs-lookup"><span data-stu-id="1125d-171">Select the demo data directive code that you created earlier ( _Zone replen_ ).</span></span>
    - <span data-ttu-id="1125d-172">**Šablona práce:** Toto pole ponechte prázdné.</span><span class="sxs-lookup"><span data-stu-id="1125d-172">**Work template:** Leave this field blank.</span></span>
    - <span data-ttu-id="1125d-173">**Minimální množství:** Toto pole určuje množství, při kterém bude aktivováno doplnění.</span><span class="sxs-lookup"><span data-stu-id="1125d-173">**Minimum quantity:** This field sets the quantity that replenishment will be triggered at.</span></span> <span data-ttu-id="1125d-174">Zadejte _50_.</span><span class="sxs-lookup"><span data-stu-id="1125d-174">Enter _50_.</span></span>
    - <span data-ttu-id="1125d-175">**Maximální množství:** Toto pole nastavuje maximální množství položky, jež se může v zóně nacházet.</span><span class="sxs-lookup"><span data-stu-id="1125d-175">**Maximum quantity:** This field sets the maximum quantity of an item that can be present in a zone.</span></span> <span data-ttu-id="1125d-176">Vygenerované práce doplnění zvýší zásoby na toto množství.</span><span class="sxs-lookup"><span data-stu-id="1125d-176">Generated replenishment work will increase inventory to this quantity.</span></span> <span data-ttu-id="1125d-177">Zadejte _150_.</span><span class="sxs-lookup"><span data-stu-id="1125d-177">Enter _150_.</span></span>
    - <span data-ttu-id="1125d-178">**Jednotka:** Toto pole určuje jednotku pro hodnoty minimálního a maximálního množství.</span><span class="sxs-lookup"><span data-stu-id="1125d-178">**Unit:** This field sets the unit for the minimum and maximum values.</span></span> <span data-ttu-id="1125d-179">Vyberte _ks_.</span><span class="sxs-lookup"><span data-stu-id="1125d-179">Select _ea_.</span></span>
    - <span data-ttu-id="1125d-180">**Přírůstek poptávky:** Vyberte možnost _Zaokrouhlit nahoru_.</span><span class="sxs-lookup"><span data-stu-id="1125d-180">**Demand increment:** Select _Round up_.</span></span>
    - <span data-ttu-id="1125d-181">**Doplnit prázdná pevná skladová místa:** Zaškrtněte toto políčko.</span><span class="sxs-lookup"><span data-stu-id="1125d-181">**Replenish empty fixed locations:** Select this check box.</span></span>
    - <span data-ttu-id="1125d-182">**Doplnit pouze pevná skladová místa** Zrušte zaškrtnutí tohoto políčka.</span><span class="sxs-lookup"><span data-stu-id="1125d-182">**Replenish only fixed locations:** Clear this check box.</span></span>
    - <span data-ttu-id="1125d-183">**Režim dotazu na produkt:** Vyberte _Dotaz na produkt_.</span><span class="sxs-lookup"><span data-stu-id="1125d-183">**Product query mode:** Select _Product query_.</span></span>
    - <span data-ttu-id="1125d-184">**Obor mezní hodnoty doplnění:** Toto pole určuje, zda má šablona provádět vyhodnocování podle zóny nebo podle konkrétního skladového místa.</span><span class="sxs-lookup"><span data-stu-id="1125d-184">**Replenishment threshold scope:** This field defines whether the template should evaluate by zone or by specific location.</span></span> <span data-ttu-id="1125d-185">Vyberte _Zóna_.</span><span class="sxs-lookup"><span data-stu-id="1125d-185">Select _Zone_.</span></span>
    - <span data-ttu-id="1125d-186">**Sklad:** Vyberte _61_.</span><span class="sxs-lookup"><span data-stu-id="1125d-186">**Warehouse:** Select _61_.</span></span>

1. <span data-ttu-id="1125d-187">Klikněte na **Vybrat produkty** nad mřížkou **Podrobnosti šablony doplnění**.</span><span class="sxs-lookup"><span data-stu-id="1125d-187">Select **Select products** above the **Replenishment Template Details** grid.</span></span>
1. <span data-ttu-id="1125d-188">V dialogovém okně **Dotaz na produkt** klikněte na kartu **Oblast** a tlačítkem **Přidat** přidejte řádek mřížky.</span><span class="sxs-lookup"><span data-stu-id="1125d-188">In the **Product query** dialog box, on the **Range** tab, select **Add** to add a row to the grid.</span></span>
1. <span data-ttu-id="1125d-189">Na novém řádku nastavte následující hodnoty:</span><span class="sxs-lookup"><span data-stu-id="1125d-189">In the new row, set the following values:</span></span>

    - <span data-ttu-id="1125d-190">**Tabulka:** _Položky_</span><span class="sxs-lookup"><span data-stu-id="1125d-190">**Table:** _Items_</span></span>
    - <span data-ttu-id="1125d-191">**Odvozená tabulka:** _Položky_</span><span class="sxs-lookup"><span data-stu-id="1125d-191">**Derived table:** _Items_</span></span>
    - <span data-ttu-id="1125d-192">**Pole:** _Číslo položky_</span><span class="sxs-lookup"><span data-stu-id="1125d-192">**Field:** _Item number_</span></span>
    - <span data-ttu-id="1125d-193">**Kritéria:** _A0001_</span><span class="sxs-lookup"><span data-stu-id="1125d-193">**Criteria:** _A0001_</span></span>

1. <span data-ttu-id="1125d-194">Vyberte **OK** , uložte svůj dotaz a zavřete dialogové okno.</span><span class="sxs-lookup"><span data-stu-id="1125d-194">Select **OK** to save your query and close the dialog box.</span></span>
1. <span data-ttu-id="1125d-195">Klikněte na **Vybrat zóny pro doplnění** nad mřížkou **Podrobnosti šablony doplnění**.</span><span class="sxs-lookup"><span data-stu-id="1125d-195">Select **Select zones to replenish** above the **Replenishment Template Details** grid.</span></span>
1. <span data-ttu-id="1125d-196">V dialogovém okně **Dotaz na zónu** na kartě **Oblast** přidejte řádek mřížky.</span><span class="sxs-lookup"><span data-stu-id="1125d-196">In the **Zone query** dialog box, on the **Range** tab, add a row to the grid.</span></span>
1. <span data-ttu-id="1125d-197">Na novém řádku nastavte následující hodnoty:</span><span class="sxs-lookup"><span data-stu-id="1125d-197">In the new row, set the following values:</span></span>

    - <span data-ttu-id="1125d-198">**Tabulka:** _Skladová zóna_</span><span class="sxs-lookup"><span data-stu-id="1125d-198">**Table:** _Warehouse zone_</span></span>
    - <span data-ttu-id="1125d-199">**Odvozená tabulka:** _Skladová zóna_</span><span class="sxs-lookup"><span data-stu-id="1125d-199">**Derived table:** _Warehouse zone_</span></span>
    - <span data-ttu-id="1125d-200">**Pole:** _ID zóny_</span><span class="sxs-lookup"><span data-stu-id="1125d-200">**Field:** _Zone ID_</span></span>
    - <span data-ttu-id="1125d-201">**Kritéria:** _PODLAHA_</span><span class="sxs-lookup"><span data-stu-id="1125d-201">**Criteria:** _FLOOR_</span></span>

1. <span data-ttu-id="1125d-202">Vyberte **OK** , uložte svůj dotaz a zavřete dialogové okno.</span><span class="sxs-lookup"><span data-stu-id="1125d-202">Select **OK** to save your query and close the dialog box.</span></span>

### <a name="set-up-location-directives"></a><span data-ttu-id="1125d-203">Nastavit směrnice skladových míst</span><span class="sxs-lookup"><span data-stu-id="1125d-203">Set up location directives</span></span>

<span data-ttu-id="1125d-204">Na rozdíl od doplňování na základě minimálního/maximálního množství platí, že doplňování na bázi zón vyžaduje nastavení směrnice výdejového skladového místa i směrnice zaskladňovacího skladového místa, protože systém vyhodnocuje celou zónu a nikoli pouze výdejové skladové místo pro výstupní práci.</span><span class="sxs-lookup"><span data-stu-id="1125d-204">Unlike location-based min/max replenishment, zone-based min/max replenishment requires that you set up both pick location directives and put location directives, because the system evaluates the whole zone instead of just the pick location for outbound work.</span></span>

#### <a name="view-and-edit-location-directives"></a><span data-ttu-id="1125d-205">Zobrazení a úpravy směrnic skladových míst</span><span class="sxs-lookup"><span data-stu-id="1125d-205">View and edit location directives</span></span>

<span data-ttu-id="1125d-206">Chcete-li zobrazit nebo upravit směrnice skladových míst, přejděte do **Řízení skladu \> Nastavení \> Směrnice skladových míst**.</span><span class="sxs-lookup"><span data-stu-id="1125d-206">To view or edit your location directives, go to **Warehouse management \> Setup \> Location directives**.</span></span>

<span data-ttu-id="1125d-207">Příklady zobrazující, jak použít nastavení k vytvoření požadovaných směrnic výdejových a zaskladňovacích skladových míst, naleznete v další části.</span><span class="sxs-lookup"><span data-stu-id="1125d-207">For examples that show how to use the settings to create the required pick location directives and put location directives, see the next section.</span></span>

#### <a name="prepare-demo-data-location-directives"></a><span data-ttu-id="1125d-208">Příprava ukázkových dat směrnic skladových míst</span><span class="sxs-lookup"><span data-stu-id="1125d-208">Prepare demo data location directives</span></span>

<span data-ttu-id="1125d-209">Chcete-li připravit ukázková data, aby se dala použít ve scénáři uvedeném na konci tohoto tématu, musíte vytvořit dvě směrnice skladových míst: jednu pro výdej a druhou pro zaskladňování.</span><span class="sxs-lookup"><span data-stu-id="1125d-209">To prepare demo data so that it can be used in the scenario at the end of this topic, you must create two location directives: one for pick and one for put.</span></span>

##### <a name="create-a-replenishment-pick-directive"></a><span data-ttu-id="1125d-210">Vytvoření směrnice skladového místa pro výdej</span><span class="sxs-lookup"><span data-stu-id="1125d-210">Create a replenishment pick directive</span></span>

1. <span data-ttu-id="1125d-211">Pro práci s ukázkovými daty vyberte právnickou osobu **USMF**.</span><span class="sxs-lookup"><span data-stu-id="1125d-211">Select the **USMF** legal entity to work with the demo data.</span></span>
1. <span data-ttu-id="1125d-212">Přejděte na **Řízení skladu \> Nastavení \> Směrnice skladového místa**.</span><span class="sxs-lookup"><span data-stu-id="1125d-212">Go to **Warehouse management \> Setup \> Location directives**.</span></span>
1. <span data-ttu-id="1125d-213">V levém podokně nastavte v poli **Typ pracovního příkazu** hodnotu _Doplnění_.</span><span class="sxs-lookup"><span data-stu-id="1125d-213">In the left pane, set the **Work order type** field to _Replenishment_.</span></span>
1. <span data-ttu-id="1125d-214">V podokně Akce vyberte možnost **Nová** , vytvoří se nová směrnice.</span><span class="sxs-lookup"><span data-stu-id="1125d-214">On the Action Pane, select **New** to create a new directive.</span></span>
1. <span data-ttu-id="1125d-215">Nastavte následující hodnoty:</span><span class="sxs-lookup"><span data-stu-id="1125d-215">Set the following values:</span></span>

    - <span data-ttu-id="1125d-216">**Pořadové číslo:** Přijměte výchozí hodnotu.</span><span class="sxs-lookup"><span data-stu-id="1125d-216">**Sequence number:** Accept the default value.</span></span>
    - <span data-ttu-id="1125d-217">**Název:** Zadejte _Zone pick_.</span><span class="sxs-lookup"><span data-stu-id="1125d-217">**Name:** Enter _Zone pick_.</span></span>
    - <span data-ttu-id="1125d-218">**Typ práce:** Vyberte _Výdej_.</span><span class="sxs-lookup"><span data-stu-id="1125d-218">**Work type:** Select _Pick_.</span></span>
    - <span data-ttu-id="1125d-219">**Lokalita:** Vyberte _6_.</span><span class="sxs-lookup"><span data-stu-id="1125d-219">**Site:** Select _6_.</span></span>
    - <span data-ttu-id="1125d-220">**Sklad:** Vyberte _61_.</span><span class="sxs-lookup"><span data-stu-id="1125d-220">**Warehouse:** Select _61_.</span></span>
    - <span data-ttu-id="1125d-221">**Kód směrnice:** Toto pole nechte prázdné.</span><span class="sxs-lookup"><span data-stu-id="1125d-221">**Directive code:** Leave this field blank.</span></span>
    - <span data-ttu-id="1125d-222">**Více SKU:** U této možnosti nastavte hodnotu _Ne_.</span><span class="sxs-lookup"><span data-stu-id="1125d-222">**Multi SKU:** Set this option to _No_.</span></span>

1. <span data-ttu-id="1125d-223">Vyberte **Uložit**. Vytvoří se směrnice obsahující vámi dosud nakonfigurované nastavení.</span><span class="sxs-lookup"><span data-stu-id="1125d-223">Select **Save** to create a directive that has the settings that you've configured so far.</span></span>
1. <span data-ttu-id="1125d-224">Na záložce s náhledem **Řádky** přidejte řádek do mřížky výběrem možnosti **Nový**.</span><span class="sxs-lookup"><span data-stu-id="1125d-224">On the **Lines** FastTab, select **New** to add a line to the grid.</span></span>
1. <span data-ttu-id="1125d-225">Na novém řádku nastavte následující hodnoty:</span><span class="sxs-lookup"><span data-stu-id="1125d-225">On the new line, set the following values:</span></span>

    - <span data-ttu-id="1125d-226">**Pořadové číslo:** Zadejte _1_.</span><span class="sxs-lookup"><span data-stu-id="1125d-226">**Sequence number:** Enter _1_.</span></span>
    - <span data-ttu-id="1125d-227">**Od množství:** Zadejte _0_.</span><span class="sxs-lookup"><span data-stu-id="1125d-227">**From quantity:** Enter _0_.</span></span>
    - <span data-ttu-id="1125d-228">**Do množství:** Zadejte _10000000_.</span><span class="sxs-lookup"><span data-stu-id="1125d-228">**To quantity:** Enter _10000000_.</span></span>
    - <span data-ttu-id="1125d-229">**Jednotka:** Pole ponechejte prázdné.</span><span class="sxs-lookup"><span data-stu-id="1125d-229">**Unit:** Leave this field blank.</span></span>
    - <span data-ttu-id="1125d-230">**Vyhledat množství:** Vyberte _Žádné_.</span><span class="sxs-lookup"><span data-stu-id="1125d-230">**Locate quantity:** Select _None_.</span></span>
    - <span data-ttu-id="1125d-231">**Omezit podle jednotky:** Zrušte zaškrtnutí tohoto políčka.</span><span class="sxs-lookup"><span data-stu-id="1125d-231">**Restrict by unit:** Clear this check box.</span></span>
    - <span data-ttu-id="1125d-232">**Zaokrouhlení na jednotku:** Zrušte zaškrtnutí tohoto políčka.</span><span class="sxs-lookup"><span data-stu-id="1125d-232">**Round up to unit:** Clear this check box.</span></span>
    - <span data-ttu-id="1125d-233">**Vyhledat množství balení:** Zrušte zaškrtnutí tohoto políčka.</span><span class="sxs-lookup"><span data-stu-id="1125d-233">**Locate packing quantity:** Clear this check box.</span></span>
    - <span data-ttu-id="1125d-234">**Povolit rozdělení:** Zaškrtněte toto políčko.</span><span class="sxs-lookup"><span data-stu-id="1125d-234">**Allow split:** Select this check box.</span></span>

1. <span data-ttu-id="1125d-235">Kliknutím na tlačítko **Uložit** uložte nový řádek.</span><span class="sxs-lookup"><span data-stu-id="1125d-235">Select **Save** to save the new line.</span></span>
1. <span data-ttu-id="1125d-236">Zatímco je nový řádek stále ještě vybrán v mřížce **Řádky** , vyberte možnost **Nový** na záložce s náhledem **Akce směrnice skladového místa**. Přidáte tak nový řádek do mřížky.</span><span class="sxs-lookup"><span data-stu-id="1125d-236">While your new line is still selected in the **Lines** grid, select **New** on the **Location Directive Actions** FastTab to add a row to the grid.</span></span>
1. <span data-ttu-id="1125d-237">Na novém řádku nastavte následující hodnoty:</span><span class="sxs-lookup"><span data-stu-id="1125d-237">In the new row, set the following values:</span></span>

    - <span data-ttu-id="1125d-238">**Pořadové číslo:** Zadejte _1_.</span><span class="sxs-lookup"><span data-stu-id="1125d-238">**Sequence number:** Enter _1_.</span></span>
    - <span data-ttu-id="1125d-239">**Název:** Zadejte _Pick from bulk_.</span><span class="sxs-lookup"><span data-stu-id="1125d-239">**Name:** Enter _Pick from bulk_.</span></span>
    - <span data-ttu-id="1125d-240">**Využití pevného skladového místa:** Vyberte _Pevná a nepevná skladová místa_.</span><span class="sxs-lookup"><span data-stu-id="1125d-240">**Fixed location usage:** Select _Fixed and non-fixed locations_.</span></span>
    - <span data-ttu-id="1125d-241">**Povolit záporný stav zásob:** Zrušte zaškrtnutí tohoto políčka.</span><span class="sxs-lookup"><span data-stu-id="1125d-241">**Allow negative inventory:** Clear this check box.</span></span>
    - <span data-ttu-id="1125d-242">**Dávka povolena:** Zrušte zaškrtnutí tohoto políčka.</span><span class="sxs-lookup"><span data-stu-id="1125d-242">**Batch enabled:** Clear this check box.</span></span>
    - <span data-ttu-id="1125d-243">**Strategie:** Vyberte _Žádná_.</span><span class="sxs-lookup"><span data-stu-id="1125d-243">**Strategy:** Select _None_.</span></span>

1. <span data-ttu-id="1125d-244">Kliknutím na tlačítko **Uložit** uložte novou akci.</span><span class="sxs-lookup"><span data-stu-id="1125d-244">Select **Save** to save the new action.</span></span>
1. <span data-ttu-id="1125d-245">Dokud je nová akce stále ještě vybrána, klikněte na **Upravit dotaz** nad mřížkou **Akce směrnice skladového místa**.</span><span class="sxs-lookup"><span data-stu-id="1125d-245">While your new action still selected, select **Edit query** above the **Location Directive Actions** grid.</span></span>
1. <span data-ttu-id="1125d-246">Zobrazí se dialogové okno dotazu. Zde můžete vybrat skladová místa, z nichž se má provést doplnění.</span><span class="sxs-lookup"><span data-stu-id="1125d-246">A query dialog box appears, where you can select the locations to replenish from.</span></span> <span data-ttu-id="1125d-247">Na kartě **Oblast** přidejte řádek do mřížky výběrem možnosti **Přidat**.</span><span class="sxs-lookup"><span data-stu-id="1125d-247">On the **Range** tab, select **Add** to add a row to the grid.</span></span>
1. <span data-ttu-id="1125d-248">Na novém řádku nastavte následující hodnoty:</span><span class="sxs-lookup"><span data-stu-id="1125d-248">In the new row, set the following values:</span></span>

    - <span data-ttu-id="1125d-249">**Tabulka:** _umístění_</span><span class="sxs-lookup"><span data-stu-id="1125d-249">**Table:** _Locations_</span></span>
    - <span data-ttu-id="1125d-250">**Odvozená tabulka:** _Skladová místa_</span><span class="sxs-lookup"><span data-stu-id="1125d-250">**Derived table:** _Locations_</span></span>
    - <span data-ttu-id="1125d-251">**Pole:** _ID zóny_</span><span class="sxs-lookup"><span data-stu-id="1125d-251">**Field:** _Zone ID_</span></span>
    - <span data-ttu-id="1125d-252">**Kritéria:** _BULK_</span><span class="sxs-lookup"><span data-stu-id="1125d-252">**Criteria:** _BULK_</span></span>

1. <span data-ttu-id="1125d-253">Vyberte **OK** , uložte svůj dotaz a zavřete dialogové okno.</span><span class="sxs-lookup"><span data-stu-id="1125d-253">Select **OK** to save your query and close the dialog box.</span></span>
1. <span data-ttu-id="1125d-254">Směrnici skladového místa uložíte výběrem možnosti **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="1125d-254">Select **Save** to save your location directive.</span></span>

##### <a name="create-a-replenishment-put-directive"></a><span data-ttu-id="1125d-255">Vytvoření směrnice skladového místa pro zaskladnění</span><span class="sxs-lookup"><span data-stu-id="1125d-255">Create a replenishment put directive</span></span>

1. <span data-ttu-id="1125d-256">Na stránce **Směrnice skladového místa** zkontrolujte v levém podokně, že je v poli **Typ pracovního příkazu** sále ještě zadána hodnota _Doplnění_.</span><span class="sxs-lookup"><span data-stu-id="1125d-256">On the **Location directives** page, in the left pane, make sure that the **Work order type** field is still set to _Replenishment_.</span></span>
1. <span data-ttu-id="1125d-257">V podokně Akce vyberte možnost **Nová** , vytvoří se další nová směrnice.</span><span class="sxs-lookup"><span data-stu-id="1125d-257">On the Action Pane, select **New** to create another new directive.</span></span>
1. <span data-ttu-id="1125d-258">Nastavte následující hodnoty:</span><span class="sxs-lookup"><span data-stu-id="1125d-258">Set the following values:</span></span>

    - <span data-ttu-id="1125d-259">**Pořadové číslo:** Přijměte výchozí hodnotu.</span><span class="sxs-lookup"><span data-stu-id="1125d-259">**Sequence number:** Accept the default value.</span></span>
    - <span data-ttu-id="1125d-260">**Název:** Zadejte _Zone put_.</span><span class="sxs-lookup"><span data-stu-id="1125d-260">**Name:** Enter _Zone put_.</span></span>
    - <span data-ttu-id="1125d-261">**Typ pracovního příkazu:** Vyberte _Zaskladnění_.</span><span class="sxs-lookup"><span data-stu-id="1125d-261">**Work order type:** Select _Put_.</span></span>
    - <span data-ttu-id="1125d-262">**Lokalita:** Vyberte _6_.</span><span class="sxs-lookup"><span data-stu-id="1125d-262">**Site:** Select _6_.</span></span>
    - <span data-ttu-id="1125d-263">**Sklad:** Vyberte _61_.</span><span class="sxs-lookup"><span data-stu-id="1125d-263">**Warehouse:** Select _61_.</span></span>
    - <span data-ttu-id="1125d-264">**Kód předpis:** Vyberte _Zone replen_. Tím směrnici skladového místa propojíte se šablonou doplnění, kterou jste vytvořili dříve pomocí předtím vytvořeného kódu.</span><span class="sxs-lookup"><span data-stu-id="1125d-264">**Directive code:** Select _Zone replen_ to link this location directive with the replenishment template that you created earlier by using the code that you created earlier.</span></span>
    - <span data-ttu-id="1125d-265">**Více SKU:** U této možnosti nastavte hodnotu _Ne_.</span><span class="sxs-lookup"><span data-stu-id="1125d-265">**Multi SKU:** Set this option to _No_.</span></span>

1. <span data-ttu-id="1125d-266">Vyberte **Uložit**. Vytvoří se směrnice obsahující vámi dosud nakonfigurované nastavení.</span><span class="sxs-lookup"><span data-stu-id="1125d-266">Select **Save** to create a directive that has the settings that you've configured so far.</span></span>
1. <span data-ttu-id="1125d-267">Na záložce s náhledem **Řádky** přidejte řádek do mřížky výběrem možnosti **Nový**.</span><span class="sxs-lookup"><span data-stu-id="1125d-267">On the **Lines** FastTab, select **New** to add a line to the grid.</span></span>
1. <span data-ttu-id="1125d-268">Na novém řádku nastavte následující hodnoty:</span><span class="sxs-lookup"><span data-stu-id="1125d-268">On the new line, set the following values:</span></span>

    - <span data-ttu-id="1125d-269">**Pořadové číslo:** Zadejte _1_.</span><span class="sxs-lookup"><span data-stu-id="1125d-269">**Sequence number:** Enter _1_.</span></span>
    - <span data-ttu-id="1125d-270">**Od množství:** Zadejte _0_.</span><span class="sxs-lookup"><span data-stu-id="1125d-270">**From quantity:** Enter _0_.</span></span>
    - <span data-ttu-id="1125d-271">**Do množství:** Zadejte _10000000_.</span><span class="sxs-lookup"><span data-stu-id="1125d-271">**To quantity:** Enter _10000000_.</span></span>
    - <span data-ttu-id="1125d-272">**Jednotka:** Pole ponechejte prázdné.</span><span class="sxs-lookup"><span data-stu-id="1125d-272">**Unit:** Leave this field blank.</span></span>
    - <span data-ttu-id="1125d-273">**Vyhledat množství:** Vyberte _Žádné_.</span><span class="sxs-lookup"><span data-stu-id="1125d-273">**Locate quantity:** Select _None_.</span></span>
    - <span data-ttu-id="1125d-274">**Omezit podle jednotky:** Zrušte zaškrtnutí tohoto políčka.</span><span class="sxs-lookup"><span data-stu-id="1125d-274">**Restrict by unit:** Clear this check box.</span></span>
    - <span data-ttu-id="1125d-275">**Zaokrouhlení na jednotku:** Zrušte zaškrtnutí tohoto políčka.</span><span class="sxs-lookup"><span data-stu-id="1125d-275">**Round up to unit:** Clear this check box.</span></span>
    - <span data-ttu-id="1125d-276">**Vyhledat množství balení:** Zrušte zaškrtnutí tohoto políčka.</span><span class="sxs-lookup"><span data-stu-id="1125d-276">**Locate packing quantity:** Clear this check box.</span></span>
    - <span data-ttu-id="1125d-277">**Povolit rozdělení:** Zaškrtněte toto políčko.</span><span class="sxs-lookup"><span data-stu-id="1125d-277">**Allow split:** Select this check box.</span></span>

1. <span data-ttu-id="1125d-278">Kliknutím na tlačítko **Uložit** uložte nový řádek.</span><span class="sxs-lookup"><span data-stu-id="1125d-278">Select **Save** to save the new line.</span></span>
1. <span data-ttu-id="1125d-279">Zatímco je nový řádek stále ještě vybrán v mřížce **Řádky** , vyberte možnost **Nový** na záložce s náhledem **Akce směrnice skladového místa**. Přidáte tak nový řádek do mřížky.</span><span class="sxs-lookup"><span data-stu-id="1125d-279">While your new line is still selected in the **Lines** grid, select **New** on the **Location Directive Actions** FastTab to add a row to the grid.</span></span>
1. <span data-ttu-id="1125d-280">Na novém řádku nastavte následující hodnoty:</span><span class="sxs-lookup"><span data-stu-id="1125d-280">In the new row, set the following values:</span></span>

    - <span data-ttu-id="1125d-281">**Pořadové číslo:** Zadejte _1_.</span><span class="sxs-lookup"><span data-stu-id="1125d-281">**Sequence number:** Enter _1_.</span></span>
    - <span data-ttu-id="1125d-282">**Název:** Zadejte _Zone put_.</span><span class="sxs-lookup"><span data-stu-id="1125d-282">**Name:** Enter _Zone put_.</span></span>
    - <span data-ttu-id="1125d-283">**Využití pevného skladového místa:** Vyberte _Pevná a nepevná skladová místa_.</span><span class="sxs-lookup"><span data-stu-id="1125d-283">**Fixed location usage:** Select _Fixed and non-fixed locations_.</span></span>
    - <span data-ttu-id="1125d-284">**Povolit záporný stav zásob:** Zrušte zaškrtnutí tohoto políčka.</span><span class="sxs-lookup"><span data-stu-id="1125d-284">**Allow negative inventory:** Clear this check box.</span></span>
    - <span data-ttu-id="1125d-285">**Dávka povolena:** Zrušte zaškrtnutí tohoto políčka.</span><span class="sxs-lookup"><span data-stu-id="1125d-285">**Batch enabled:** Clear this check box.</span></span>
    - <span data-ttu-id="1125d-286">**Strategie:** Vyberte _Konsolidovat_.</span><span class="sxs-lookup"><span data-stu-id="1125d-286">**Strategy:** Select _Consolidate_.</span></span>

1. <span data-ttu-id="1125d-287">Kliknutím na tlačítko **Uložit** uložte novou akci.</span><span class="sxs-lookup"><span data-stu-id="1125d-287">Select **Save** to save the new action.</span></span>
1. <span data-ttu-id="1125d-288">Dokud je nová akce stále ještě vybrána, klikněte na **Upravit dotaz** nad mřížkou **Akce směrnice skladového místa**.</span><span class="sxs-lookup"><span data-stu-id="1125d-288">While your new action is still selected, select **Edit query** above the **Location Directive Actions** grid.</span></span>
1. <span data-ttu-id="1125d-289">Zobrazí se dialogové okno dotazu. Zde můžete vybrat zónu, z níž se má provést doplnění.</span><span class="sxs-lookup"><span data-stu-id="1125d-289">A query dialog box appears, where you can select the zone to replenish to.</span></span> <span data-ttu-id="1125d-290">Tato zóna by měla být stejná jako zóna uvedená v šabloně doplnění.</span><span class="sxs-lookup"><span data-stu-id="1125d-290">This zone should be the same zone that is specified in the replenishment template.</span></span> <span data-ttu-id="1125d-291">Na kartě **Oblast** přidejte řádek do mřížky výběrem možnosti **Přidat**.</span><span class="sxs-lookup"><span data-stu-id="1125d-291">On the **Range** tab, select **Add** to add a row to the grid.</span></span>
1. <span data-ttu-id="1125d-292">Na novém řádku nastavte následující hodnoty:</span><span class="sxs-lookup"><span data-stu-id="1125d-292">In the new row, set the following values:</span></span>

    - <span data-ttu-id="1125d-293">**Tabulka:** _umístění_</span><span class="sxs-lookup"><span data-stu-id="1125d-293">**Table:** _Locations_</span></span>
    - <span data-ttu-id="1125d-294">**Odvozená tabulka:** _Skladová místa_</span><span class="sxs-lookup"><span data-stu-id="1125d-294">**Derived table:** _Locations_</span></span>
    - <span data-ttu-id="1125d-295">**Pole:** _ID zóny_</span><span class="sxs-lookup"><span data-stu-id="1125d-295">**Field:** _Zone ID_</span></span>
    - <span data-ttu-id="1125d-296">**Kritéria:** _PODLAHA_</span><span class="sxs-lookup"><span data-stu-id="1125d-296">**Criteria:** _FLOOR_</span></span>

1. <span data-ttu-id="1125d-297">Vyberte **OK** , uložte svůj dotaz a zavřete dialogové okno.</span><span class="sxs-lookup"><span data-stu-id="1125d-297">Select **OK** to save your query and close the dialog box.</span></span>
1. <span data-ttu-id="1125d-298">Směrnici skladového místa uložíte výběrem možnosti **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="1125d-298">Select **Save** to save your location directive.</span></span>

## <a name="scenario"></a><span data-ttu-id="1125d-299">Scénář</span><span class="sxs-lookup"><span data-stu-id="1125d-299">Scenario</span></span>

<span data-ttu-id="1125d-300">Tato část obsahuje ukázkový scénář, který ilustruje, jak s touto funkcí pracovat.</span><span class="sxs-lookup"><span data-stu-id="1125d-300">This section provides a sample scenario that shows how to work with the feature.</span></span>

### <a name="prepare-the-sample-data-that-is-required-for-the-sample-scenario"></a><span data-ttu-id="1125d-301">Připravte ukázková data, jež potřebujete pro scénář</span><span class="sxs-lookup"><span data-stu-id="1125d-301">Prepare the sample data that is required for the sample scenario</span></span>

<span data-ttu-id="1125d-302">Než začnete pracovat na scénáři, musíte ukázková data aktivovat a nastavit funkci tak, jak se popisuje v této části a v předchozích částech tohoto tématu.</span><span class="sxs-lookup"><span data-stu-id="1125d-302">Before you start to work through the scenario, you must activate sample data and set up the feature as described in this section and in the previous sections of this topic.</span></span>

#### <a name="use-the-usmf-legal-entity"></a><span data-ttu-id="1125d-303">Použijte právnickou osobu USMF</span><span class="sxs-lookup"><span data-stu-id="1125d-303">Use the USMF legal entity</span></span>

<span data-ttu-id="1125d-304">Chcete-li se scénářem pracovat pomocí zde specifikovaných ukázkových záznamů a hodnot, musíte používat systém, ve kterém jsou nainstalována standardní [ukázková data](../../fin-ops-core/dev-itpro/deployment/deploy-demo-environment.md).</span><span class="sxs-lookup"><span data-stu-id="1125d-304">To work through the scenario by using the sample records and values that are specified here, you must be on a system where the standard [demo data](../../fin-ops-core/dev-itpro/deployment/deploy-demo-environment.md) is installed.</span></span> <span data-ttu-id="1125d-305">Kromě toho musíte dříve, než začnete, také vybrat právnickou osobu **USMF**.</span><span class="sxs-lookup"><span data-stu-id="1125d-305">Additionally, you must select the **USMF** legal entity before you begin.</span></span>

#### <a name="prepare-additional-sample-data"></a><span data-ttu-id="1125d-306">Příprava dalších ukázkových dat</span><span class="sxs-lookup"><span data-stu-id="1125d-306">Prepare additional sample data</span></span>

<span data-ttu-id="1125d-307">Po výběru právnické osoby **USMF** přidejte další ukázková data, jak jsou potřeba. Postupujte podle popisu v sekci [Nastavení zónového doplňování](#setup) tohoto tématu.</span><span class="sxs-lookup"><span data-stu-id="1125d-307">After you've selected the **USMF** legal entity, add the additional sample data that is required, as described in the [Set up zone-based replenishment](#setup) section earlier in this topic.</span></span>

#### <a name="check-your-on-hand-inventory"></a><span data-ttu-id="1125d-308">Zkontrolujte množství na skladě.</span><span class="sxs-lookup"><span data-stu-id="1125d-308">Check your on-hand inventory</span></span>

<span data-ttu-id="1125d-309">Postupujte podle těchto kroků a ujistěte se, že váš systém obsahuje dostatek zásob, aby bylo možné ukázkový scénář realizovat.</span><span class="sxs-lookup"><span data-stu-id="1125d-309">Follow these steps to make sure that your system includes enough inventory to support the sample scenario.</span></span>

1. <span data-ttu-id="1125d-310">Ujistěte se, že máte k dispozici zásoby položky *A0001* ve dvou různých skladových místech v oblasti výdeje ( *PODLAHA* ), jež je uvedena v šabloně doplňování.</span><span class="sxs-lookup"><span data-stu-id="1125d-310">Make sure that there is on-hand inventory for item *A0001* at two different locations in the pick zone ( *FLOOR* ) that is specified in the replenishment template.</span></span> <span data-ttu-id="1125d-311">Celkové zásoby by však měly být nižší než požadované minimální množství ( *50* ), jež je uvedeno v šabloně doplnění.</span><span class="sxs-lookup"><span data-stu-id="1125d-311">However, the total inventory should be less than the required minimum quantity ( *50* ) that is specified on the replenishment template.</span></span> <span data-ttu-id="1125d-312">Tímto způsobem můžete simulovat výpočet pro celou zónu, nikoli pouze pro jedno skladové místo.</span><span class="sxs-lookup"><span data-stu-id="1125d-312">In this way, you can simulate how the calculation occurs for the whole zone instead of just for a single location.</span></span> <span data-ttu-id="1125d-313">**Upravte zásoby pomocí některého ze skladových procesů dle potřeby.**</span><span class="sxs-lookup"><span data-stu-id="1125d-313">**Use any of the warehouse processes to adjust inventory as required.**</span></span>
1. <span data-ttu-id="1125d-314">Ujistěte se, že máte dostatečné zásoby položky *A0001* na hromadném skladovém místě, které je určeno ve směrnici skladového místa, kde se při práci doplnění má provádět výdej položek ze zóny s ID *BULK*.</span><span class="sxs-lookup"><span data-stu-id="1125d-314">Make sure that there is enough inventory for item *A0001* at a bulk location that is specified in the zone pick location directive where the replenishment work should pick the items from zone ID *BULK*.</span></span> <span data-ttu-id="1125d-315">Celkové zásoby však musí být vyšší než požadované maximální množství ( *150* ), jež je uvedeno v šabloně doplnění.</span><span class="sxs-lookup"><span data-stu-id="1125d-315">The total inventory must be more than the required maximum quantity ( *150* ) that is specified in the replenishment template.</span></span>
1. <span data-ttu-id="1125d-316">Volitelné, ale doporučené: Chcete-li vytvořit deník úprav zásob postupujte takto:</span><span class="sxs-lookup"><span data-stu-id="1125d-316">Optional but recommended: Follow these steps to create an inventory adjustment journal:</span></span>

    1. <span data-ttu-id="1125d-317">Přejděte do **Řízení zásob \> Položky deníku \> Položky \> Úprava zásob**.</span><span class="sxs-lookup"><span data-stu-id="1125d-317">Go to **Inventory management \> Journal entries \> Items \> Inventory adjustment**.</span></span>
    1. <span data-ttu-id="1125d-318">Zvolte **Nové**.</span><span class="sxs-lookup"><span data-stu-id="1125d-318">Select **New**.</span></span>
    1. <span data-ttu-id="1125d-319">V dialogovém okně **Vytvořit deník zásob** vyberte v poli **Sklad** hodnotu *61*.</span><span class="sxs-lookup"><span data-stu-id="1125d-319">In the **Create inventory journal** dialog box, in the **Warehouse** field, select *61*.</span></span>
    1. <span data-ttu-id="1125d-320">Vyberte **OK**.</span><span class="sxs-lookup"><span data-stu-id="1125d-320">Select **OK**.</span></span>
    1. <span data-ttu-id="1125d-321">Na záložce s náhledem **Řádky deníku** použijte tlačítko **Nový**. Do mřížky přidejte tři řádky a nastavte následující hodnoty.</span><span class="sxs-lookup"><span data-stu-id="1125d-321">On the **Journal lines** FastTab, use the **New** button to add three lines to the grid, and set the following values.</span></span> <span data-ttu-id="1125d-322">Po dokončení nastavení každého řádku klikněte na **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="1125d-322">After you've finished setting up each line, select **Save**.</span></span>

        - <span data-ttu-id="1125d-323">**Řádek 1:**</span><span class="sxs-lookup"><span data-stu-id="1125d-323">**Line 1:**</span></span>

            - <span data-ttu-id="1125d-324">**Číslo položky:** *A0001*</span><span class="sxs-lookup"><span data-stu-id="1125d-324">**Item number:** *A0001*</span></span>
            - <span data-ttu-id="1125d-325">**Lokalita:** *6*</span><span class="sxs-lookup"><span data-stu-id="1125d-325">**Site:** *6*</span></span>
            - <span data-ttu-id="1125d-326">**Sklad:** *61*</span><span class="sxs-lookup"><span data-stu-id="1125d-326">**Warehouse:** *61*</span></span>
            - <span data-ttu-id="1125d-327">**Skladové místo:** *02A01R1S1B*</span><span class="sxs-lookup"><span data-stu-id="1125d-327">**Location:** *02A01R1S1B*</span></span>
            - <span data-ttu-id="1125d-328">**Registrační značka:** Vyberte existující registrační značku ze seznamu nebo vytvořte novou registrační značku.</span><span class="sxs-lookup"><span data-stu-id="1125d-328">**License plate:** Select an existing license plate in the list, or create a new license plate.</span></span>
            - <span data-ttu-id="1125d-329">**Množství:** *1000*</span><span class="sxs-lookup"><span data-stu-id="1125d-329">**Quantity:** *1000*</span></span>

        - <span data-ttu-id="1125d-330">**Řádek 2:**</span><span class="sxs-lookup"><span data-stu-id="1125d-330">**Line 2:**</span></span>

            - <span data-ttu-id="1125d-331">**Číslo položky:** *A0001*</span><span class="sxs-lookup"><span data-stu-id="1125d-331">**Item number:** *A0001*</span></span>
            - <span data-ttu-id="1125d-332">**Lokalita:** *6*</span><span class="sxs-lookup"><span data-stu-id="1125d-332">**Site:** *6*</span></span>
            - <span data-ttu-id="1125d-333">**Sklad:** *61*</span><span class="sxs-lookup"><span data-stu-id="1125d-333">**Warehouse:** *61*</span></span>
            - <span data-ttu-id="1125d-334">**Skladové místo:** *07A01R2S1B*</span><span class="sxs-lookup"><span data-stu-id="1125d-334">**Location:** *07A01R2S1B*</span></span>
            - <span data-ttu-id="1125d-335">**Registrační značka:** Vyberte existující registrační značku ze seznamu nebo vytvořte novou registrační značku.</span><span class="sxs-lookup"><span data-stu-id="1125d-335">**License plate:** Select an existing license plate in the list, or create a new license plate.</span></span>
            - <span data-ttu-id="1125d-336">**Množství:** *15*</span><span class="sxs-lookup"><span data-stu-id="1125d-336">**Quantity:** *15*</span></span>

        - <span data-ttu-id="1125d-337">**Řádek 3:**</span><span class="sxs-lookup"><span data-stu-id="1125d-337">**Line 3:**</span></span>

            - <span data-ttu-id="1125d-338">**Číslo položky:** *A0001*</span><span class="sxs-lookup"><span data-stu-id="1125d-338">**Item number:** *A0001*</span></span>
            - <span data-ttu-id="1125d-339">**Lokalita:** *6*</span><span class="sxs-lookup"><span data-stu-id="1125d-339">**Site:** *6*</span></span>
            - <span data-ttu-id="1125d-340">**Sklad:** *61*</span><span class="sxs-lookup"><span data-stu-id="1125d-340">**Warehouse:** *61*</span></span>
            - <span data-ttu-id="1125d-341">**Skladové místo:** *07A01R1S1B*</span><span class="sxs-lookup"><span data-stu-id="1125d-341">**Location:** *07A01R1S1B*</span></span>
            - <span data-ttu-id="1125d-342">**Registrační značka:** Vyberte existující registrační značku ze seznamu nebo vytvořte novou registrační značku.</span><span class="sxs-lookup"><span data-stu-id="1125d-342">**License plate:** Select an existing license plate in the list, or create a new license plate.</span></span>
            - <span data-ttu-id="1125d-343">**Množství:** *10*</span><span class="sxs-lookup"><span data-stu-id="1125d-343">**Quantity:** *10*</span></span>

    1. <span data-ttu-id="1125d-344">V podokně Akce klikněte na možnost **Ověřit**.</span><span class="sxs-lookup"><span data-stu-id="1125d-344">On the Action Pane, select **Validate**.</span></span> <span data-ttu-id="1125d-345">Vyřešte všechny chyby, které se vyskytnou. Poté přejděte k dalšímu kroku.</span><span class="sxs-lookup"><span data-stu-id="1125d-345">Address any errors that are found before you move on to the next step.</span></span>
    1. <span data-ttu-id="1125d-346">V podokně Akce vyberte možnost **Zaúčtovat**. Tím se provede zaúčtování zásob do skladu.</span><span class="sxs-lookup"><span data-stu-id="1125d-346">On the Action Pane, select **Post** to post the inventory to the warehouse.</span></span>

### <a name="sample-scenario-run-zone-based-minmax-replenishment"></a><span data-ttu-id="1125d-347">Ukázkový scénář: Spuštění min./max. doplňování založeného na zónách</span><span class="sxs-lookup"><span data-stu-id="1125d-347">Sample scenario: Run zone-based min/max replenishment</span></span>

<span data-ttu-id="1125d-348">Po zajištění všech nezbytných ukázkových dat můžete spustit doplňování takto.</span><span class="sxs-lookup"><span data-stu-id="1125d-348">After all the prerequisite sample data is in place, you can trigger replenishment by following these steps.</span></span>

1. <span data-ttu-id="1125d-349">Přejděte na **Řízení skladu \> Doplnění \> Doplnění**.</span><span class="sxs-lookup"><span data-stu-id="1125d-349">Go to **Warehouse management \> Replenishment \> Replenishments**.</span></span>
1. <span data-ttu-id="1125d-350">V dialogovém okně **Doplnění** na záložce s náhledem **Záznamy k zahrnutí** vyberte **Filtr**.</span><span class="sxs-lookup"><span data-stu-id="1125d-350">In the **Replenishment** dialog box, on the **Records to include** FastTab, select **Filter**.</span></span>
1. <span data-ttu-id="1125d-351">V dialogovém okně **Dotaz** na kartě **Oblast** upravte výchozí řádek tabulky následujícím způsobem:</span><span class="sxs-lookup"><span data-stu-id="1125d-351">In the **Inquiry** dialog box, on the **Range** tab, edit the default table row in the following way:</span></span>

    - <span data-ttu-id="1125d-352">**Tabulka:** Vyberte _Šablony doplnění_.</span><span class="sxs-lookup"><span data-stu-id="1125d-352">**Table:** Select _Replenishment templates_.</span></span>
    - <span data-ttu-id="1125d-353">**Odvozená tabulka:** Vyberte _Šablony doplnění_.</span><span class="sxs-lookup"><span data-stu-id="1125d-353">**Derived table:** Select _Replenishment templates_.</span></span>
    - <span data-ttu-id="1125d-354">**Pole:** Vyberte _Šablona doplnění_.</span><span class="sxs-lookup"><span data-stu-id="1125d-354">**Field:** Select _Replenishment template_.</span></span>
    - <span data-ttu-id="1125d-355">**Kritéria:** Vyberte _Min./max. doplnění na bázi zón_.</span><span class="sxs-lookup"><span data-stu-id="1125d-355">**Criteria:** Select _Zone min/max replen_.</span></span> <span data-ttu-id="1125d-356">Tuto šablonu doplnění jste vytvořili během přípravy ukázkových dat pro tento scénář.</span><span class="sxs-lookup"><span data-stu-id="1125d-356">This replenishment template is the replenishment template that you created while you were preparing the demo data for this scenario.</span></span>

1. <span data-ttu-id="1125d-357">Klikněte na **OK** , uložte dotaz a vraťte se do dialogového okna **Doplnění**.</span><span class="sxs-lookup"><span data-stu-id="1125d-357">Select **OK** to save the query and go back to the **Replenishment** dialog box.</span></span>
1. <span data-ttu-id="1125d-358">Kliknutím na **OK** spusťte šablonu doplnění.</span><span class="sxs-lookup"><span data-stu-id="1125d-358">Select **OK** to run the replenishment template.</span></span>

<span data-ttu-id="1125d-359">Práce doplnění jsou nyní vytvořeny pro výdej zásob ze zóny *BULK* a doplnění se provede do zóny *PODLAHA*.</span><span class="sxs-lookup"><span data-stu-id="1125d-359">Replenishment work is now created to pick inventory from the *BULK* zone and replenish it to the *FLOOR* zone.</span></span>

## <a name="notes-and-tips"></a><span data-ttu-id="1125d-360">Poznámky a tipy</span><span class="sxs-lookup"><span data-stu-id="1125d-360">Notes and tips</span></span>

<span data-ttu-id="1125d-361">Zde je několik poznámek a tipů pro práci s touto funkcí:</span><span class="sxs-lookup"><span data-stu-id="1125d-361">Here are a few notes and tips for working with the feature:</span></span>

- <span data-ttu-id="1125d-362">Chcete-li nastavit práci doplnění, jež přejde do požadované zóny, můžete propojit řádky šablony doplnění a směrnice skladového místa některým z následujících způsobů:</span><span class="sxs-lookup"><span data-stu-id="1125d-362">To set up replenishment work that goes to the desired zone, you can link the replenishment template lines and location directives in either of the following ways:</span></span>

    - <span data-ttu-id="1125d-363">Upravte záhlaví směrnice skladového místa a filtrujte vybrané řádky šablony doplnění.</span><span class="sxs-lookup"><span data-stu-id="1125d-363">Edit the location directive header query, and filter the selected replenishment template lines.</span></span>
    - <span data-ttu-id="1125d-364">Použijte kód směrnice na řádku šablony doplnění a srovnávejte jej se zaskladňovací směrnicí skladového místa.</span><span class="sxs-lookup"><span data-stu-id="1125d-364">Use a directive code on the replenishment template line, and match it to the put location directive.</span></span>

- <span data-ttu-id="1125d-365">Pokud používáte dynamická skladová místa, vytvoří se práce doplnění pro první dostupné skladové místo nebo pro skladové místo, které již obsahuje zásoby, je-li akce směrnice skladového místa nastavena k použití strategie **Konsolidovat**.</span><span class="sxs-lookup"><span data-stu-id="1125d-365">If you're using dynamic locations, replenishment work will be created either for the first available location or for a location that already contains inventory, if the location directive action is set up to use the **Consolidate** strategy.</span></span>
- <span data-ttu-id="1125d-366">Pokud místo zón používáte pevná skladová místa, měli byste použít [standardní min./max. doplnění](tasks/set-up-min-max-replenishment-process.md).</span><span class="sxs-lookup"><span data-stu-id="1125d-366">If you're using fixed locations instead of zones, you should use [standard min/max replenishment](tasks/set-up-min-max-replenishment-process.md).</span></span>
