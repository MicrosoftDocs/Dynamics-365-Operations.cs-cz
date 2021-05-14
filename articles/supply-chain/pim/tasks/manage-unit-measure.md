---
title: Správa měrných jednotek
description: Toto téma popisuje definování měrné jednotky, poskytnutí překladů pro jednotky a jejich popisu a definování pravidel pro převod souvisejících jednotek.
author: sorenva
ms.date: 04/09/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: EcoResProductMaintainWorkspace, EcoResProductOpenCasesFormPart, UnitOfMeasure, UnitOfMeasureReportingTranslation, UnitOfMeasureTranslation, UnitOfMeasureConversion, UnitOfMeasureConversionEditOrCreate, UnitOfMeasureLookup, UnitOfMeasureCalculator, UnitOfMeasureWizard, UnitOfMeasureLookupTest
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: sorenand
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: d36839cd8e3398225d3421bf0f268068599ca49f
ms.sourcegitcommit: fa99a36c3d30d0c0577fd3f63ed6bf2f71599e40
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/20/2021
ms.locfileid: "5921334"
---
# <a name="manage-units-of-measure"></a><span data-ttu-id="dbcd0-103">Správa měrných jednotek</span><span class="sxs-lookup"><span data-stu-id="dbcd0-103">Manage units of measure</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="dbcd0-104">Toto téma popisuje definování měrné jednotky, poskytnutí překladů pro jednotky a jejich popisu a definování pravidel pro převod souvisejících jednotek.</span><span class="sxs-lookup"><span data-stu-id="dbcd0-104">This topic describes how to define a unit of measure, provide translations for the unit and its description, and define conversion rules for related units.</span></span>

## <a name="open-the-units-page"></a><span data-ttu-id="dbcd0-105">Otevřete stránku Jednotky.</span><span class="sxs-lookup"><span data-stu-id="dbcd0-105">Open the Units page</span></span>

<span data-ttu-id="dbcd0-106">Chcete-li vytvořit a pracovat s měrnými jednotkami, které jsou k dispozici ve vašem systému, přejděte na **Správa organizace \> Nastavení \> Jednotky \> Jednotky**.</span><span class="sxs-lookup"><span data-stu-id="dbcd0-106">To create and work with the units of measure that are available in your system, go to **Organization administration \> Setup \> Units \> Units**.</span></span>

<span data-ttu-id="dbcd0-107">Zbývající části tohoto tématu popisují, co můžete dělat na stránce **Jednotky**.</span><span class="sxs-lookup"><span data-stu-id="dbcd0-107">The remaining sections of this topic describe what you can do on the **Units** page.</span></span>

## <a name="create-standard-units-and-conversions"></a><span data-ttu-id="dbcd0-108">Vytvoření standardních jednotek a převodů</span><span class="sxs-lookup"><span data-stu-id="dbcd0-108">Create standard units and conversions</span></span>

<span data-ttu-id="dbcd0-109">Pokud váš systém již neobsahuje nejčastěji používané měrné jednotky pro metrický systém nebo americký obvyklý systém (USCS), může vám průvodce nastavením jednotek pomoci rychle začít se základními definicemi jednotek a převody.</span><span class="sxs-lookup"><span data-stu-id="dbcd0-109">If your system doesn't already include the most commonly used units of measure for the metric system and/or the US customary system (USCS), the unit setup wizard can help you quickly get started with basic unit definitions and conversions.</span></span> <span data-ttu-id="dbcd0-110">Chcete-li průvodce projít, vyberte **Průvodce vytvořením jednotky** v podokně Akce a poté postupujte podle pokynů na obrazovce.</span><span class="sxs-lookup"><span data-stu-id="dbcd0-110">To complete the wizard, select **Unit creation wizard** on the Action Pane, and then follow the on-screen instructions.</span></span>

## <a name="create-or-edit-a-unit-of-measure"></a><span data-ttu-id="dbcd0-111">Vytvoření nebo úprava měrné jednotky</span><span class="sxs-lookup"><span data-stu-id="dbcd0-111">Create or edit a unit of measure</span></span>

<span data-ttu-id="dbcd0-112">Chcete-li vytvořit nebo upravit měrnou jednotku, postupujte takto.</span><span class="sxs-lookup"><span data-stu-id="dbcd0-112">To create or edit a unit of measure, follow these steps.</span></span>

1. <span data-ttu-id="dbcd0-113">Proveďte jeden z následujících kroků:</span><span class="sxs-lookup"><span data-stu-id="dbcd0-113">Follow one of these steps:</span></span>

    - <span data-ttu-id="dbcd0-114">Chcete-li upravit existující jednotku, vyberte ji v podokně seznamu.</span><span class="sxs-lookup"><span data-stu-id="dbcd0-114">To edit an existing unit, select it in the list pane.</span></span>
    - <span data-ttu-id="dbcd0-115">Chcete-li vytvořit novou jednotku, vyberte **Nová** v podokně Akce.</span><span class="sxs-lookup"><span data-stu-id="dbcd0-115">To create a new unit, select **New** on the Action Pane.</span></span>

1. <span data-ttu-id="dbcd0-116">V záhlaví záznamu nastavte následující pole:</span><span class="sxs-lookup"><span data-stu-id="dbcd0-116">On the header of the record, set the following fields:</span></span>

    - <span data-ttu-id="dbcd0-117">**Jednotka** – Zadejte ID nebo symbol, který se použije k označení jednotky v systémovém jazyce.</span><span class="sxs-lookup"><span data-stu-id="dbcd0-117">**Unit** – Enter the ID or symbol to use to refer to the unit in the system language.</span></span> <span data-ttu-id="dbcd0-118">Toto ID nebo symbol je obvykle běžná zkratka pro jednotku, například *ks* pro kus nebo *cm* pro centimetr.</span><span class="sxs-lookup"><span data-stu-id="dbcd0-118">This ID or symbol is usually a common abbreviation for the unit, such as *ea* for each or *cm* for centimeter.</span></span>
    - <span data-ttu-id="dbcd0-119">**Popis** – Zadejte popisný název jednotky v systémovém jazyce.</span><span class="sxs-lookup"><span data-stu-id="dbcd0-119">**Description** – Enter a descriptive name for the unit in the system language.</span></span> <span data-ttu-id="dbcd0-120">Tento název je obvykle celé jméno jednotky, například *Kus* nebo *Centimetr*.</span><span class="sxs-lookup"><span data-stu-id="dbcd0-120">This name is usually the full name of the unit, such as *Each* or *Centimeter*.</span></span>

1. <span data-ttu-id="dbcd0-121">Na pevné záložce **Obecné** zadejte následující pole:</span><span class="sxs-lookup"><span data-stu-id="dbcd0-121">On the **General** FastTab, set the following fields:</span></span><!-- KFM: confirm this:    - **Fixed unit assignment** and **Fixed unit** – These fields have an effect only if you're using the Microsoft Retail Essentials product. If the current unit can be mapped to one of the fixed units that are used by Retail Essentials, set the **Fixed unit assignment** option to *Yes*. Then select the fixed unit in the **Fixed unit** field. -->

    - <span data-ttu-id="dbcd0-122">**Třída jednotek** – Vyberte vlastnost, kterou jednotka měří (například délku, plochu, hmotnost nebo množství).</span><span class="sxs-lookup"><span data-stu-id="dbcd0-122">**Unit class** – Select the property that the unit measures (such as length, area, mass, or quantity).</span></span>
    - <span data-ttu-id="dbcd0-123">**Systém jednotek** – Vyberte měřný systém, do kterého jednotka patří (*Metrické jednotky* nebo *Americké obvyklé jednotky*).</span><span class="sxs-lookup"><span data-stu-id="dbcd0-123">**System of units** – Select the measurement system that the unit belongs to (*Metric units* or *United States customary units*).</span></span>
    - <span data-ttu-id="dbcd0-124">**Základní jednotka** – Nastavte tuto možnost na *Ano*, chcete-li použít aktuální jednotku jako základní jednotku pro svou třídu jednotek.</span><span class="sxs-lookup"><span data-stu-id="dbcd0-124">**Base unit** – Set this option to *Yes* to use the current unit as the base unit for its unit class.</span></span> <span data-ttu-id="dbcd0-125">V tomto případě musíte zadat pouze převodní koeficient mezi základní jednotkou a každou další jednotkou ve třídě jednotek.</span><span class="sxs-lookup"><span data-stu-id="dbcd0-125">In this case, you only have to specify the conversion factor between the base unit and each additional unit in the unit class.</span></span> <span data-ttu-id="dbcd0-126">Systém pak může převádět mezi všemi jednotkami v dané třídě jednotek.</span><span class="sxs-lookup"><span data-stu-id="dbcd0-126">The system can then convert between all units in that unit class.</span></span> <span data-ttu-id="dbcd0-127">Proto je snazší nastavit převody.</span><span class="sxs-lookup"><span data-stu-id="dbcd0-127">Therefore, it's easier to set up conversions.</span></span>

        <span data-ttu-id="dbcd0-128">Například pokud je galon základní jednotkou pro třídu jednotek *Objem*, musíte nastavit pouze převodní faktory z litrů na galon a z pinty na galon.</span><span class="sxs-lookup"><span data-stu-id="dbcd0-128">For example, if gallon is the base unit for the *Volume* unit class, you only have to set up conversion factors from quart to gallon and from pint to gallon.</span></span> <span data-ttu-id="dbcd0-129">Systém pak dokáže také převádět z litrů na pintu.</span><span class="sxs-lookup"><span data-stu-id="dbcd0-129">The system can then also convert from quart to pint.</span></span>

        <span data-ttu-id="dbcd0-130">Pro každou třídu jednotek můžete mít pouze jednu základní jednotku.</span><span class="sxs-lookup"><span data-stu-id="dbcd0-130">You can have only one base unit per unit class.</span></span>

    - <span data-ttu-id="dbcd0-131">**Systémová jednotka** – Nastavte tuto možnost na *Ano*, chcete-li použít aktuální jednotku jako předpokládanou jednotku pro všechna nespecifikovaná měření pro svou třídu jednotek.</span><span class="sxs-lookup"><span data-stu-id="dbcd0-131">**System unit** – Set this option to *Yes* to use the current unit as the assumed unit for all unspecified measurements in its unit class.</span></span> <span data-ttu-id="dbcd0-132">Například pokud pole, které se používá k zadání množství, neumožňuje specifikovat jednotku (pokud uživatel nevybere jednotku), systém použije jednotku, která je nastavena jako systémová jednotka pro třídu jednotek *Množství*.</span><span class="sxs-lookup"><span data-stu-id="dbcd0-132">For example, if a field that is used to enter a quantity doesn't allow a unit to be specified (of if the user doesn't select a unit), the system uses the unit that is set as the system unit for the *Quantity* unit class.</span></span> <span data-ttu-id="dbcd0-133">Pro každou třídu jednotek můžete mít pouze jednu systémovou jednotku.</span><span class="sxs-lookup"><span data-stu-id="dbcd0-133">You can have only one system unit per unit class.</span></span>
    - <span data-ttu-id="dbcd0-134">**Desetinná přesnost** – Určete počet desetinných míst, na které mají být zaokrouhleny hodnoty zadané pro aktuální jednotku nebo na ně převedené.</span><span class="sxs-lookup"><span data-stu-id="dbcd0-134">**Decimal precision** – Specify the number of decimal places that values that are specified for the current unit or converted to it should be rounded to.</span></span>

1. <span data-ttu-id="dbcd0-135">V podokně akcí vyberte **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="dbcd0-135">On the Action Pane, select **Save**.</span></span>

## <a name="define-unit-translations"></a><span data-ttu-id="dbcd0-136">Definování překladů jednotek</span><span class="sxs-lookup"><span data-stu-id="dbcd0-136">Define unit translations</span></span>

<span data-ttu-id="dbcd0-137">Chcete-li definovat překlady pro ID nebo symbol a popis měrné jednotky, postupujte takto.</span><span class="sxs-lookup"><span data-stu-id="dbcd0-137">To define translations for the ID or symbol and the description for a unit of measure, follow these steps.</span></span>

1. <span data-ttu-id="dbcd0-138">Vytvořte nebo vyberte jednotku, pro kterou chcete vytvořit překlad.</span><span class="sxs-lookup"><span data-stu-id="dbcd0-138">Create or select the unit to create translations for.</span></span>
1. <span data-ttu-id="dbcd0-139">V podokně akcí zvolte **Texty jednotky**.</span><span class="sxs-lookup"><span data-stu-id="dbcd0-139">On the Action Pane, select **Unit texts**.</span></span>

    <span data-ttu-id="dbcd0-140">Zobrazí se stránka **Texty jednotek**.</span><span class="sxs-lookup"><span data-stu-id="dbcd0-140">The **Unit texts** page appears.</span></span> <span data-ttu-id="dbcd0-141">Tato stránka slouží k definování překladů pro ID nebo symbol pro vybranou jednotku.</span><span class="sxs-lookup"><span data-stu-id="dbcd0-141">You use this page to define translations for the ID or symbol for the selected unit.</span></span> <span data-ttu-id="dbcd0-142">Tyto překlady lze poté použít na externí dokumenty v jazycích specifických pro zákazníka nebo pro dodavatele.</span><span class="sxs-lookup"><span data-stu-id="dbcd0-142">Those translations can then be used on external documents in customer-specific or vendor-specific languages.</span></span>

1. <span data-ttu-id="dbcd0-143">V podokně akcí zvolte **Nový**.</span><span class="sxs-lookup"><span data-stu-id="dbcd0-143">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="dbcd0-144">V poli **Jednotka** vyberte jazyk, do kterého se má ID nebo symbol jednotky přeložit.</span><span class="sxs-lookup"><span data-stu-id="dbcd0-144">In the **Language** field, select the language to translate the unit ID or symbol to.</span></span>
1. <span data-ttu-id="dbcd0-145">Do pole **Text** zadejte překlad ID jednotky nebo symbolu do vybraného jazyka.</span><span class="sxs-lookup"><span data-stu-id="dbcd0-145">In the **Text** field, enter the translation of the unit ID or symbol in the selected language.</span></span>
1. <span data-ttu-id="dbcd0-146">V podokně akcí vyberte **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="dbcd0-146">On the Action Pane, select **Save**.</span></span>
1. <span data-ttu-id="dbcd0-147">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="dbcd0-147">Close the page.</span></span>
1. <span data-ttu-id="dbcd0-148">V **podokně akcí** vyberte možnost **Popisy přeložené jednotky**.</span><span class="sxs-lookup"><span data-stu-id="dbcd0-148">On the **Action Pane**, select **Translated unit descriptions**.</span></span>

    <span data-ttu-id="dbcd0-149">Zobrazí se stránka **Přeložené popisy jednotek**.</span><span class="sxs-lookup"><span data-stu-id="dbcd0-149">The **Translated unit descriptions** page appears.</span></span> <span data-ttu-id="dbcd0-150">Tato stránka slouží k definování specifických jazykových popisů pro vybranou jednotku.</span><span class="sxs-lookup"><span data-stu-id="dbcd0-150">You use this page to define language-specific descriptions for the selected unit.</span></span>

1. <span data-ttu-id="dbcd0-151">V podokně akcí zvolte **Nový**.</span><span class="sxs-lookup"><span data-stu-id="dbcd0-151">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="dbcd0-152">V poli **Jednotka** vyberte jazyk, do kterého se má popis jednotky přeložit.</span><span class="sxs-lookup"><span data-stu-id="dbcd0-152">In the **Language** field, select the language to translate the unit description to.</span></span>
1. <span data-ttu-id="dbcd0-153">Do pole **Popis** zadejte překlad popisu jednotky do vybraného jazyka.</span><span class="sxs-lookup"><span data-stu-id="dbcd0-153">In the **Description** field, enter the translation of the unit description in the selected language.</span></span>
1. <span data-ttu-id="dbcd0-154">V podokně akcí vyberte **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="dbcd0-154">On the Action Pane, select **Save**.</span></span>
1. <span data-ttu-id="dbcd0-155">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="dbcd0-155">Close the page.</span></span>

## <a name="define-unit-conversion-rules"></a><span data-ttu-id="dbcd0-156">Definování pravidel pro převod jednotek</span><span class="sxs-lookup"><span data-stu-id="dbcd0-156">Define unit conversion rules</span></span>

<span data-ttu-id="dbcd0-157">Chcete-li definovat pravidla pro převody mezi měrnými jednotkami, postupujte takto.</span><span class="sxs-lookup"><span data-stu-id="dbcd0-157">To define rules for conversions between units of measure, follow these steps.</span></span>

1. <span data-ttu-id="dbcd0-158">Vytvořte nebo vyberte jednotku, pro kterou chcete vytvořit převod.</span><span class="sxs-lookup"><span data-stu-id="dbcd0-158">Create or select the unit to define conversion rules for.</span></span>
1. <span data-ttu-id="dbcd0-159">V podokně akcí zvolte **Převody jednotek**.</span><span class="sxs-lookup"><span data-stu-id="dbcd0-159">On the Action Pane, select **Unit conversions**.</span></span>

    <span data-ttu-id="dbcd0-160">Zobrazí se stránka **Převody jednotek**.</span><span class="sxs-lookup"><span data-stu-id="dbcd0-160">The **Unit conversions** page appears.</span></span> <span data-ttu-id="dbcd0-161">Tuto stránku můžete použít k definování pravidel pro převod vybrané jednotky jiných jednotek v třídě jednotky a z nich.</span><span class="sxs-lookup"><span data-stu-id="dbcd0-161">You use this page to define rules for converting the selected unit to and from other units in the unit class.</span></span>

1. <span data-ttu-id="dbcd0-162">Vyberte jednu z následujících karet v závislosti na typu převodu, který chcete nastavit:</span><span class="sxs-lookup"><span data-stu-id="dbcd0-162">Select one of the following tabs, depending on the type of conversion that you want to set up:</span></span>

    - <span data-ttu-id="dbcd0-163">**Standardní převody** – Nastavte standardní pravidla převodu pro všechny produkty.</span><span class="sxs-lookup"><span data-stu-id="dbcd0-163">**Standard conversions** – Set up standard conversion rules for all products.</span></span>
    - <span data-ttu-id="dbcd0-164">**Konverze uvnitř třídy** – Nastavte pravidla převodu pro konkrétní produkt pro jednotky ve stejné třídě jednotek.</span><span class="sxs-lookup"><span data-stu-id="dbcd0-164">**Intra-class conversions** – Set up product-specific conversion rules for units in the same unit class.</span></span>
    - <span data-ttu-id="dbcd0-165">**Konverze mezi třídami** – Nastavte pravidla převodu pro konkrétní produkt pro jednotky mezi třídami jednotek.</span><span class="sxs-lookup"><span data-stu-id="dbcd0-165">**Inter-class conversions** – Set up product-specific conversion rules for units across unit classes.</span></span>

1. <span data-ttu-id="dbcd0-166">Proveďte jeden z následujících kroků:</span><span class="sxs-lookup"><span data-stu-id="dbcd0-166">Follow one of these steps:</span></span>

    - <span data-ttu-id="dbcd0-167">Chcete-li vytvořit nový převod, vyberte **Nová** na panelu nástrojů.</span><span class="sxs-lookup"><span data-stu-id="dbcd0-167">To create a new conversion, select **New** on the toolbar.</span></span>
    - <span data-ttu-id="dbcd0-168">Chcete-li upravit existující převod, vyberte převod v mřížce a poté vyberte **Upravit** na panelu nástrojů.</span><span class="sxs-lookup"><span data-stu-id="dbcd0-168">To edit an existing conversion, select the conversion in the grid, and then select **Edit** on the toolbar.</span></span>

1. <span data-ttu-id="dbcd0-169">V zobrazeném rozevíracím dialogovém okně nastavte následující pole:</span><span class="sxs-lookup"><span data-stu-id="dbcd0-169">In the drop-down dialog box that appears, set the following fields:</span></span>

    - <span data-ttu-id="dbcd0-170">**Produkt** – Vyberte konkrétní produkt, kterého se převod týká.</span><span class="sxs-lookup"><span data-stu-id="dbcd0-170">**Product** – Select the specific product that the conversion applies to.</span></span> <span data-ttu-id="dbcd0-171">Toto pole je k dispozici pouze pro převody v rámci třídy a mezi třídami.</span><span class="sxs-lookup"><span data-stu-id="dbcd0-171">This field is available only for intra-class and inter-class conversions.</span></span>
    - <span data-ttu-id="dbcd0-172">**Rozložení vzorce** – Nechte toto pole nastaveno na *Jednoduchý*, chcete-li určit jednoduchou konverzi, která má jediný koeficient.</span><span class="sxs-lookup"><span data-stu-id="dbcd0-172">**Formula layout** – Leave this field set to *Simple* to specify a simple conversion that has a single factor.</span></span> <span data-ttu-id="dbcd0-173">Nastavte ho na *Pokročilý*, chcete-li nastavit složitější rovnici.</span><span class="sxs-lookup"><span data-stu-id="dbcd0-173">Set it to *Advanced* to set up a more complex equation.</span></span> <span data-ttu-id="dbcd0-174">Formát pokročilých rovnic se liší v závislosti na třídě jednotek.</span><span class="sxs-lookup"><span data-stu-id="dbcd0-174">The format for advanced equations varies, depending on the unit class.</span></span>
    - <span data-ttu-id="dbcd0-175">**Z jednotky** – Toto pole zobrazuje vybranou jednotku.</span><span class="sxs-lookup"><span data-stu-id="dbcd0-175">**From unit** – This field shows the selected unit.</span></span> <span data-ttu-id="dbcd0-176">Obvykle byste neměli měnit hodnotu.</span><span class="sxs-lookup"><span data-stu-id="dbcd0-176">Usually, you should not change the value.</span></span> <span data-ttu-id="dbcd0-177">(Pokud změníte hodnotu, musíte otevřít stránku **Převody jednotek** pro vybranou jednotku, aby se po uložení zobrazil nový převod.)</span><span class="sxs-lookup"><span data-stu-id="dbcd0-177">(If you do change the value, you must open the **Unit conversions** page for the selected unit to view your new conversion after you save it.)</span></span>
    - <span data-ttu-id="dbcd0-178">**Do jednotky** – Vyberte jednotku, na kterou chcete převést.</span><span class="sxs-lookup"><span data-stu-id="dbcd0-178">**To unit** – Select the unit to convert to.</span></span>
    - <span data-ttu-id="dbcd0-179">**Zaokrouhlování** – Vyberte způsob zaokrouhlování zlomků na základě hodnoty **Desetinná přesnost** vybrané jednotky (*Na nejbližší*, *Nahoru*, nebo *Dolů*).</span><span class="sxs-lookup"><span data-stu-id="dbcd0-179">**Rounding** – Select how fractions should be rounded, based on the **Decimal precision** value of the selected unit (*To nearest*, *Up*, or *Down*).</span></span>
    - <span data-ttu-id="dbcd0-180">**Převodní vzorec** – Pomocí zbývajících polí v horní části rozevíracího dialogového okna zadejte vzorec pro převod mezi těmito dvěma jednotkami.</span><span class="sxs-lookup"><span data-stu-id="dbcd0-180">**Conversion formula** – Use the remaining fields at the top of the drop-down dialog box to specify the formula for converting between the two units.</span></span> <span data-ttu-id="dbcd0-181">Dostupná pole se liší v závislosti na vybrané třídě jednotek a rozložení vzorců.</span><span class="sxs-lookup"><span data-stu-id="dbcd0-181">The available fields vary, depending on the unit class and formula layout that you've selected.</span></span>

1. <span data-ttu-id="dbcd0-182">Vyberte **OK**.</span><span class="sxs-lookup"><span data-stu-id="dbcd0-182">Select **OK**.</span></span>
1. <span data-ttu-id="dbcd0-183">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="dbcd0-183">Close the page.</span></span>

> [!TIP]
> <span data-ttu-id="dbcd0-184">Můžete také nastavit převody jednotek na variantu produktu.</span><span class="sxs-lookup"><span data-stu-id="dbcd0-184">You can also set up unit conversions per product variant.</span></span> <span data-ttu-id="dbcd0-185">Další informace naleznete v tématu [Převod měrné jednotky pro variantu produktu](../uom-conversion-per-product-variant.md).</span><span class="sxs-lookup"><span data-stu-id="dbcd0-185">For more information, see [Unit of measure conversion per product variant](../uom-conversion-per-product-variant.md).</span></span>

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
