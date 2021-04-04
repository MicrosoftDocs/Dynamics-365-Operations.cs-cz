---
title: Nastavení informací o doručení
description: Toto téma popisuje, jak nastavit informace o dodání pro modul nákladů za doručení.
author: sherry-zheng
manager: tfehr
ms.date: 12/09/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ITMPortTable, ITMLeadTimeTable, ITMLegTable
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2020-12-09
ms.dyn365.ops.version: Release 10.0.17
ms.openlocfilehash: 7b65e1c6bb1b6bf345fdde0f4de7015190052efa
ms.sourcegitcommit: 2b4809e60974e72df9476ffd62706b1bfc8da4a7
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/04/2021
ms.locfileid: "5500519"
---
# <a name="delivery-information-setup"></a><span data-ttu-id="6dfc5-103">Nastavení informací o doručení</span><span class="sxs-lookup"><span data-stu-id="6dfc5-103">Delivery information setup</span></span>

[!include [banner](../../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

<span data-ttu-id="6dfc5-104">Toto téma popisuje, jak nastavit informace o dodání pro modul **Náklady za doručení**.</span><span class="sxs-lookup"><span data-stu-id="6dfc5-104">This topic describes how to set up delivery information for the **Landed cost** module.</span></span>

## <a name="shipping-ports"></a><span data-ttu-id="6dfc5-105">Výchozí přístavy</span><span class="sxs-lookup"><span data-stu-id="6dfc5-105">Shipping ports</span></span>

<span data-ttu-id="6dfc5-106">Přepravní přístavy identifikují, odkud a kam je zboží přepravováno.</span><span class="sxs-lookup"><span data-stu-id="6dfc5-106">Shipping ports identify where goods are being shipped from and to.</span></span> <span data-ttu-id="6dfc5-107">Pro každou cestu je definován přístav „do“ a přístav „od“, a to na základě cesty vybrané pro plavbu.</span><span class="sxs-lookup"><span data-stu-id="6dfc5-107">For each voyage, a "to" port and a "from" port are defined, based on the journey that is selected for the voyage vessel.</span></span> <span data-ttu-id="6dfc5-108">Přepravní přístavy se používají k vybudování úseků cesty a také aktivit během plavby.</span><span class="sxs-lookup"><span data-stu-id="6dfc5-108">Shipping ports are used to build the legs of a journey and also the voyage activities.</span></span> <span data-ttu-id="6dfc5-109">Obvykle jsou definovány pomocí názvu města a země nebo regionu, kde se nachází fyzický přepravní přístav.</span><span class="sxs-lookup"><span data-stu-id="6dfc5-109">They are typically defined by using the name of the city and the country or region where the physical shipping port is located.</span></span>

<span data-ttu-id="6dfc5-110">Chcete-li pracovat s přepravními přístavy, přejděte na uzel **Náklady za doručení \> Nastavení informací o doručení \> Přepravní přístavy**.</span><span class="sxs-lookup"><span data-stu-id="6dfc5-110">To work with shipping ports, go to **Landed cost \> Delivery information setup \> Shipping ports**.</span></span> <span data-ttu-id="6dfc5-111">Zde můžete prohlížet, přidávat a odebírat záznamy o vašich přepravních přístavech.</span><span class="sxs-lookup"><span data-stu-id="6dfc5-111">There, you can view, add, and remove records for your shipping ports.</span></span> <span data-ttu-id="6dfc5-112">V následující tabulce jsou popsána pole, která jsou k dispozici pro každý záznam.</span><span class="sxs-lookup"><span data-stu-id="6dfc5-112">The following table describes the fields that are available for each record.</span></span>

| <span data-ttu-id="6dfc5-113">Pole</span><span class="sxs-lookup"><span data-stu-id="6dfc5-113">Field</span></span> | <span data-ttu-id="6dfc5-114">popis</span><span class="sxs-lookup"><span data-stu-id="6dfc5-114">Description</span></span> |
|---|---|
| <span data-ttu-id="6dfc5-115">Výchozí přístavu</span><span class="sxs-lookup"><span data-stu-id="6dfc5-115">Shipping port</span></span> | <span data-ttu-id="6dfc5-116">Zadejte jedinečný identifikační název/číslo přepravního přístavu.</span><span class="sxs-lookup"><span data-stu-id="6dfc5-116">Enter a unique identification name/number for the shipping port.</span></span> |
| <span data-ttu-id="6dfc5-117">popis</span><span class="sxs-lookup"><span data-stu-id="6dfc5-117">Description</span></span> | <span data-ttu-id="6dfc5-118">Zadejte popis přepravního přístavu.</span><span class="sxs-lookup"><span data-stu-id="6dfc5-118">Enter a description of the shipping port.</span></span> |

## <a name="tracking-control-center"></a><a name="tracking-control-center"></a><span data-ttu-id="6dfc5-119">Centrum kontroly sledování</span><span class="sxs-lookup"><span data-stu-id="6dfc5-119">Tracking control center</span></span>

<span data-ttu-id="6dfc5-120">V řídicím centru sledování nastavíte doby realizace, aktualizace stavu a tok informací, které jsou spojeny s cestou, jak se přepravní kontejnery pohybují mezi jednotlivými úseky.</span><span class="sxs-lookup"><span data-stu-id="6dfc5-120">You use the Tracking control center to set up the lead times, status updates, and flow of information that is associated with a voyage as the shipping containers move from one leg to the next.</span></span> <span data-ttu-id="6dfc5-121">Když vytvoříte řídicí záznam sledování, je spojen s konkrétním úsekem trasy cesty.</span><span class="sxs-lookup"><span data-stu-id="6dfc5-121">When you create a tracking control record, it's associated with a specific leg of a journey for a voyage.</span></span> <span data-ttu-id="6dfc5-122">Když cesta aktualizuje úsek, přidružený záznam bude aktualizován a vyplněn podle definice.</span><span class="sxs-lookup"><span data-stu-id="6dfc5-122">When a voyage updates a leg, the associated record will be updated and filled in as defined.</span></span> <span data-ttu-id="6dfc5-123">Informace o sledování jednotlivých cest můžete aktualizovat na stránce **Všechny cesty**.</span><span class="sxs-lookup"><span data-stu-id="6dfc5-123">You can update tracking information for individual voyages from the **All voyages** page.</span></span>

<span data-ttu-id="6dfc5-124">Chcete-li otevřít řídicí centrum sledování, přejděte na uzel **Náklady za doručení \> Nastavení informací o doručení \> Řídicí centrum sledování**.</span><span class="sxs-lookup"><span data-stu-id="6dfc5-124">To open the Tracking control center, go to **Landed cost \> Delivery information setup \> Tracking control center**.</span></span>

<span data-ttu-id="6dfc5-125">Řídicí centrum sledování ukazuje jedno ze tří zobrazení stránky, v závislosti na hodnotě vybrané v poli **Typ vytvoření** v podokně seznamu: *Prázdný*, *Dodací lhůta* nebo *Aktualizace stavu*.</span><span class="sxs-lookup"><span data-stu-id="6dfc5-125">The Tracking control center shows one of three page views, depending on the value that is selected in the **Create type** field in the list pane: *Blank*, *Lead time*, or *Status update*.</span></span> <span data-ttu-id="6dfc5-126">Každý typ vytvoření aktualizuje jinou sadu informací, která je přidružena k postupu cesty z výchozího místa do konečného cíle.</span><span class="sxs-lookup"><span data-stu-id="6dfc5-126">Each create type updates a different set of information that is associated with the progress of a voyage from the point of origin to the final destination.</span></span>

### <a name="common-rule-settings"></a><span data-ttu-id="6dfc5-127">Nastavení společných pravidel</span><span class="sxs-lookup"><span data-stu-id="6dfc5-127">Common rule settings</span></span>

<span data-ttu-id="6dfc5-128">Následující tabulka ukazuje pole, která jsou k dispozici pro všechny tři typy vytváření v řídicím centru sledování.</span><span class="sxs-lookup"><span data-stu-id="6dfc5-128">The following table shows the fields that are available for all three create types in the Tracking control center.</span></span>

| <span data-ttu-id="6dfc5-129">Pole</span><span class="sxs-lookup"><span data-stu-id="6dfc5-129">Field</span></span> | <span data-ttu-id="6dfc5-130">popis</span><span class="sxs-lookup"><span data-stu-id="6dfc5-130">Description</span></span> |
|---|---|
| <span data-ttu-id="6dfc5-131">Zdrojová tabulka, zdrojové pole</span><span class="sxs-lookup"><span data-stu-id="6dfc5-131">Source table, Source field</span></span> | <span data-ttu-id="6dfc5-132">Tato pole identifikují zdrojovou tabulku a pole v databázi.</span><span class="sxs-lookup"><span data-stu-id="6dfc5-132">These fields identify a source table and field in the database.</span></span> <span data-ttu-id="6dfc5-133">Pravidlo načte hodnotu v poli a poté ji použije způsobem, který je definován v jiných nastaveních pravidla.</span><span class="sxs-lookup"><span data-stu-id="6dfc5-133">The rule will load the value in the field and then use it in the way that is defined by other settings of the rule.</span></span> |
| <span data-ttu-id="6dfc5-134">Cílová tabulka, cílové pole</span><span class="sxs-lookup"><span data-stu-id="6dfc5-134">Target table, Target field</span></span> | <span data-ttu-id="6dfc5-135">Tato pole identifikují cílovou tabulku a pole v databázi.</span><span class="sxs-lookup"><span data-stu-id="6dfc5-135">These fields identify a destination table and field in the database.</span></span> <span data-ttu-id="6dfc5-136">Pravidlo načte hodnotu v poli a poté ji použije (nebo přepíše) způsobem, který je definován v jiných nastaveních pravidla.</span><span class="sxs-lookup"><span data-stu-id="6dfc5-136">The rule will load the value in the field and then use it (or overwrite it) in the way that is defined by other settings of the rule.</span></span> |
| <span data-ttu-id="6dfc5-137">Aktivita</span><span class="sxs-lookup"><span data-stu-id="6dfc5-137">Activity</span></span> | <span data-ttu-id="6dfc5-138">Toto pole určuje typ aktivity, která by měla být použita na přepravní kontejner odpovídající pravidlu.</span><span class="sxs-lookup"><span data-stu-id="6dfc5-138">This field identifies the type of activity that should be applied to a shipping container that is matched by a rule.</span></span> |
| <span data-ttu-id="6dfc5-139">Odpovídající kritéria</span><span class="sxs-lookup"><span data-stu-id="6dfc5-139">Matching criteria</span></span> | <span data-ttu-id="6dfc5-140">Toto pole určuje, jak systém identifikuje shodu s pravidlem.</span><span class="sxs-lookup"><span data-stu-id="6dfc5-140">This field determines how the system identifies a match for a rule.</span></span> <span data-ttu-id="6dfc5-141">U každé instance systém zkontroluje data ve zdrojové a cílové tabulce, aby určil, zda a kdy má být pole v cílové tabulce aktualizováno.</span><span class="sxs-lookup"><span data-stu-id="6dfc5-141">In each instance, the system reviews the data in the source and destination tables to determine whether and when a field should be updated in the target table.</span></span><p><span data-ttu-id="6dfc5-142">Například zdrojová tabulka je *Cesty* a cílová tabulka je *Záhlaví nákupu* nebo *Řádky nákupu*.</span><span class="sxs-lookup"><span data-stu-id="6dfc5-142">For example, the source table is *Voyages*, and the target table is *Purchase header* or *Purchase lines*.</span></span> <span data-ttu-id="6dfc5-143">Tabulka *Cesty* má v poli **Z přístavu** hodnotu *Hongkong* a tabulka *Záhlaví nákupu* má v poli **Z přístavu** hodnotu *Šanghaj*.</span><span class="sxs-lookup"><span data-stu-id="6dfc5-143">The *Voyages* table has a **From port** value of *Hong Kong*, and the *Purchase header* table has a **From port** value of *Shanghai*.</span></span> <span data-ttu-id="6dfc5-144">Poté se vytvoří pravidlo, které má *Hongkong* jako přístav „z“.</span><span class="sxs-lookup"><span data-stu-id="6dfc5-144">A rule is then created that has *Hong Kong* as the "from" port.</span></span> <span data-ttu-id="6dfc5-145">V tomto případě hodnoty pole **Kritéria shody** budou fungovat následujícím způsobem:</span><span class="sxs-lookup"><span data-stu-id="6dfc5-145">In this case, the values of the **Matching criteria** field will work in the following way:</span></span></p><ul><li><span data-ttu-id="6dfc5-146">**Obě** – Cílové pole nebude aktualizováno, protože jeden ze dvou přístavů se neshoduje.</span><span class="sxs-lookup"><span data-stu-id="6dfc5-146">**Both** – The target field won't be updated, because one of the two ports don't match.</span></span></li><li><span data-ttu-id="6dfc5-147">**Zdroj** – Cílové pole bude aktualizováno, protože přístav „z“ zdrojové tabulky je *Hongkong*.</span><span class="sxs-lookup"><span data-stu-id="6dfc5-147">**Source** – The target field will be updated, because the source table's "from" port is *Hong Kong*.</span></span></li><li><span data-ttu-id="6dfc5-148">**Cíl** – Cílové pole nebude aktualizováno, protože přístav „z“ cílové tabulky je *Šanghaj* (ne *Hongkong*).</span><span class="sxs-lookup"><span data-stu-id="6dfc5-148">**Target** – The target field won't be updated, because the destination table's "from" port is *Shanghai* (not *Hong Kong*).</span></span></li></ul> |
| <span data-ttu-id="6dfc5-149">Kopírovat akci</span><span class="sxs-lookup"><span data-stu-id="6dfc5-149">Copy action</span></span> | <span data-ttu-id="6dfc5-150">Dostupné hodnoty jsou *Kopírovat* a *Výchozí*.</span><span class="sxs-lookup"><span data-stu-id="6dfc5-150">The available values are *Copy* and *Default*.</span></span> <span data-ttu-id="6dfc5-151">Vyberte *Kopírovat*, chcete-li zkopírovat hodnotu ve zdrojovém poli do cílového pole.</span><span class="sxs-lookup"><span data-stu-id="6dfc5-151">Select *Copy* to copy the value in the source field to the destination field.</span></span> <span data-ttu-id="6dfc5-152">Vyberte *Výchozí*, chcete-li nastavit statickou hodnotu pro cílové pole.</span><span class="sxs-lookup"><span data-stu-id="6dfc5-152">Select *Default* to set a static value for the destination field.</span></span> |
| <span data-ttu-id="6dfc5-153">Výchozí</span><span class="sxs-lookup"><span data-stu-id="6dfc5-153">Default</span></span> | <span data-ttu-id="6dfc5-154">Když je pole **Kopírovat akci** nastaveno na *Výchozí*, pole **Výchozí** definuje výchozí hodnotu cílového pole.</span><span class="sxs-lookup"><span data-stu-id="6dfc5-154">When the **Copy action** field is set to *Default*, the **Default** field defines the default value of the destination field.</span></span> <span data-ttu-id="6dfc5-155">Například pokud akce souvisí s aktualizací přístavu a pole **Kopírovat akci** je nastaveno na *Výchozí*, pole **Výchozí** identifikuje přístav.</span><span class="sxs-lookup"><span data-stu-id="6dfc5-155">For example, if the action is related to a port update, and the **Copy action** field is set to *Default*, the **Default** field identifies a port.</span></span> |
| <span data-ttu-id="6dfc5-156">Úsek</span><span class="sxs-lookup"><span data-stu-id="6dfc5-156">Leg</span></span> | <span data-ttu-id="6dfc5-157">Toto pole identifikuje úsek cesty, ve kterém dojde ke specifikované akci, jako je nakládka nebo proclení.</span><span class="sxs-lookup"><span data-stu-id="6dfc5-157">This field identifies the leg of the journey that the specified action occurs for, such as loading or customs.</span></span> |
| <span data-ttu-id="6dfc5-158">Poskytovatel služby</span><span class="sxs-lookup"><span data-stu-id="6dfc5-158">Service provider</span></span> | <span data-ttu-id="6dfc5-159">Pokud je pro aktuální aktualizaci stavu/úseku cesty použit konkrétní poskytovatel služeb, toto pole identifikuje poskytovatele služeb.</span><span class="sxs-lookup"><span data-stu-id="6dfc5-159">If a specific service provider is used for the current status update/leg of the journey, this field identifies the service provider.</span></span> <span data-ttu-id="6dfc5-160">Poskytovatelé služeb jsou definováni v účtu dodavatele.</span><span class="sxs-lookup"><span data-stu-id="6dfc5-160">Service providers are defined in the vendor account.</span></span> |

### <a name="lead-time-rules"></a><span data-ttu-id="6dfc5-161">Pravidla doby realizace</span><span class="sxs-lookup"><span data-stu-id="6dfc5-161">Lead time rules</span></span>

<span data-ttu-id="6dfc5-162">Doba realizace je odhadovaný čas potřebný k dokončení definovaného úseku cesty.</span><span class="sxs-lookup"><span data-stu-id="6dfc5-162">The lead time is the estimated time that a voyage will require to complete a defined leg of a journey for a voyage.</span></span> <span data-ttu-id="6dfc5-163">Doba realizace každého úseku cesty se používá k výpočtu předpokládaného data dodání cesty.</span><span class="sxs-lookup"><span data-stu-id="6dfc5-163">The lead time of each leg of a journey is used to calculate the estimated delivery date of the voyage.</span></span> <span data-ttu-id="6dfc5-164">Toto datum se poté zapíše do pole **Potvrzené datum dodání** na každém nákupním řádku v cestě.</span><span class="sxs-lookup"><span data-stu-id="6dfc5-164">That date is then entered in the **Confirmed delivery date** field on every purchase line in the voyage.</span></span>

<span data-ttu-id="6dfc5-165">Ke správě aktualizací datumů používáte pravidla doby realizace.</span><span class="sxs-lookup"><span data-stu-id="6dfc5-165">You use lead time rules to manage updates of dates.</span></span> <span data-ttu-id="6dfc5-166">Aktivity se automaticky generují, když se pro cestu použije šablona cesty.</span><span class="sxs-lookup"><span data-stu-id="6dfc5-166">Activities are automatically generated when a journey template is used for a voyage.</span></span>

<span data-ttu-id="6dfc5-167">Chcete-li do řídicího centra sledování přidat pravidlo doby realizace, postupujte takto.</span><span class="sxs-lookup"><span data-stu-id="6dfc5-167">To add a lead time rule to the Tracking control center, follow these steps.</span></span>

1. <span data-ttu-id="6dfc5-168">Proveďte jeden z následujících kroků:</span><span class="sxs-lookup"><span data-stu-id="6dfc5-168">Follow one of these steps:</span></span>

    - <span data-ttu-id="6dfc5-169">Přejděte do uzlu **Náklady za doručení \> Nastavení cesty s více úseky \> Úseky**.</span><span class="sxs-lookup"><span data-stu-id="6dfc5-169">Go to **Landed cost \> Multi-leg journey setup \> Legs**.</span></span> <span data-ttu-id="6dfc5-170">Vyberte úsek, pro který chcete nastavit doby realizace, a poté v podokně akcí vyberte možnost **Řídicí centrum sledování**.</span><span class="sxs-lookup"><span data-stu-id="6dfc5-170">Select the leg that you want to set up lead times for, and then, on the Action Pane, select **Tracking control center**.</span></span> <span data-ttu-id="6dfc5-171">Řídicí centrum sledování má předem načteno informace o vybraném úseku.</span><span class="sxs-lookup"><span data-stu-id="6dfc5-171">The Tracking control center is preloaded with information about the selected leg.</span></span>
    - <span data-ttu-id="6dfc5-172">Přejděte do uzlu **Náklady na doručení \> Nastavení informací o doručení \> Řídicí centrum sledování**.</span><span class="sxs-lookup"><span data-stu-id="6dfc5-172">Go to **Landed cost \> Delivery information setup \> Tracking control center**.</span></span> <span data-ttu-id="6dfc5-173">Potom musíte ručně vybrat úsek v kroku 4 tohoto postupu.</span><span class="sxs-lookup"><span data-stu-id="6dfc5-173">You must then manually select a leg in step 4 of this procedure.</span></span>

1. <span data-ttu-id="6dfc5-174">V podokně seznamu nastavte **Typ vytvoření** na *Doba realizace*.</span><span class="sxs-lookup"><span data-stu-id="6dfc5-174">In the list pane, set the **Create type** field to *Lead time*.</span></span>
1. <span data-ttu-id="6dfc5-175">V podokně akcí zvolte **Nový**.</span><span class="sxs-lookup"><span data-stu-id="6dfc5-175">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="6dfc5-176">Pokud jste začali z řídicího centra sledování v kroku 1, nastavte pole **Úsek** na úsek, pro který chcete vytvořit pravidlo doby realizace.</span><span class="sxs-lookup"><span data-stu-id="6dfc5-176">If you started from the Tracking control center in step 1, set the **Leg** field to the leg that you want to create a lead time rule for.</span></span> <span data-ttu-id="6dfc5-177">Pokud jste začali na stránce **Úseky**, pole **Úsek** je přednastaveno na úsek, který jste vybrali před otevřením řídicího centra sledování.</span><span class="sxs-lookup"><span data-stu-id="6dfc5-177">If you started from the **Legs** page, the **Leg** field is preset to the leg that you selected before you opened the Tracking control center.</span></span>

    <span data-ttu-id="6dfc5-178">Na základě hodnoty pole **Úsek** se automaticky nastaví několik polí, jak je znázorněno zde:</span><span class="sxs-lookup"><span data-stu-id="6dfc5-178">Based on the value of the **Leg** field, several fields are automatically set, as shown here:</span></span>

    - <span data-ttu-id="6dfc5-179">**Zdrojová tabulka:** *Kontejnerové aktivity*</span><span class="sxs-lookup"><span data-stu-id="6dfc5-179">**Source table:** *Container activities*</span></span>
    - <span data-ttu-id="6dfc5-180">**Zdrojové pole:** *Datum zahájení*</span><span class="sxs-lookup"><span data-stu-id="6dfc5-180">**Source field:** *Start date*</span></span>
    - <span data-ttu-id="6dfc5-181">**Cílová tabulka:** *Kontejnerové aktivity*</span><span class="sxs-lookup"><span data-stu-id="6dfc5-181">**Target table:** *Container activities*</span></span>
    - <span data-ttu-id="6dfc5-182">**Cílové pole:** *Odhadované datum ukončení*</span><span class="sxs-lookup"><span data-stu-id="6dfc5-182">**Target field:** *Estimated end date*</span></span>

1. <span data-ttu-id="6dfc5-183">V poli **Aktivita** vyberte aktivitu, na kterou by se aktuální pravidlo mělo vztahovat.</span><span class="sxs-lookup"><span data-stu-id="6dfc5-183">In the **Activity** field, select the activity that the current rule should apply to.</span></span>
1. <span data-ttu-id="6dfc5-184">Do pole **Doba realizace** zadejte čas realizace (ve dnech), který by se měl použít při spuštění aktuálního pravidla.</span><span class="sxs-lookup"><span data-stu-id="6dfc5-184">In the **Lead time** field, enter the lead time (in days) that should be applied when the current rule is triggered.</span></span>

### <a name="status-update-rules"></a><span data-ttu-id="6dfc5-185">Pravidla aktualizace stavu</span><span class="sxs-lookup"><span data-stu-id="6dfc5-185">Status update rules</span></span>

<span data-ttu-id="6dfc5-186">Záznamy, kde je pole **Typ vytvoření** nastaveno na *Aktualizace stavu*, aktualizují stav řádků nákupní objednávky nebo stav na úrovni cesty, přepravního kontejneru nebo folia.</span><span class="sxs-lookup"><span data-stu-id="6dfc5-186">Records where the **Create type** field is set to *Status update* will update the status of purchase order lines, or the status at the voyage, shipping container, or folio level.</span></span> <span data-ttu-id="6dfc5-187">Stavy lze nastavit nezávisle.</span><span class="sxs-lookup"><span data-stu-id="6dfc5-187">The statuses can be independently set.</span></span> <span data-ttu-id="6dfc5-188">Použijte je k informování uživatele nebo oddělení o fázi cesty (například o přijatých dokladech nebo přepravovaném zboží).</span><span class="sxs-lookup"><span data-stu-id="6dfc5-188">Use them to inform the user or department about the stage of a voyage (such as documents received or goods in transit).</span></span>

<span data-ttu-id="6dfc5-189">Když je pole **Typ vytvoření** nastaveno na *Aktualizace stavu*, řídicí centrum sledování obsahuje záložku **Řádky**, kde můžete definovat nákladovou oblast a aktualizovaný stav cesty.</span><span class="sxs-lookup"><span data-stu-id="6dfc5-189">When the **Create type** field is set to *Status update*, the Tracking control center includes a **Lines** FastTab where you can define a cost area and the updated status of the voyage.</span></span> <span data-ttu-id="6dfc5-190">Například máte řádek, ve kterém je pole **Nákladová oblast** nastaveno na *Kontejner* a pole **Stav cesty** nastaveno na *Zboží v přepravě*.</span><span class="sxs-lookup"><span data-stu-id="6dfc5-190">For example, you have a line where the **Cost area** field is set to *Container*, and the **Voyage status** field is set to *Goods in transit*.</span></span> <span data-ttu-id="6dfc5-191">V tomto případě, když objednávka dokončí stanovený úsek, pole **Stav cesty** přepravního kontejneru bude aktualizováno na *Zboží na cestě*.</span><span class="sxs-lookup"><span data-stu-id="6dfc5-191">In this case, when an order completes the specified leg, the **Voyage status** field of the shipping container will be updated to *Goods in Transit*.</span></span>

<span data-ttu-id="6dfc5-192">Aktualizace stavu poskytují stav cesty během různých řádků cesty a nákupní objednávky, které jsou s touto cestou spojeny.</span><span class="sxs-lookup"><span data-stu-id="6dfc5-192">Status updates provide the status of a voyage throughout the voyage lines and purchase order lines that are associated with that voyage.</span></span> <span data-ttu-id="6dfc5-193">Jak cesta probíhá z výchozího přístavu, úseků cesty a celního odbavení až do cílového skladu, poskytuje pole záznamu cesty **Stav cesty** rychlý pohled na fázi, ve které se položky nacházejí.</span><span class="sxs-lookup"><span data-stu-id="6dfc5-193">As a voyage moves through its journey from the port, sailing, and customs, to the destination warehouse, the **Voyage status** field of the voyage record provides a quick view of the stage that the items are at.</span></span>

<span data-ttu-id="6dfc5-194">Chcete-li do řídicího centra sledování přidat pravidlo aktualizace stavu, postupujte takto.</span><span class="sxs-lookup"><span data-stu-id="6dfc5-194">To add a status update rule to the Tracking control center, follow these steps.</span></span>

1. <span data-ttu-id="6dfc5-195">Proveďte jeden z následujících kroků:</span><span class="sxs-lookup"><span data-stu-id="6dfc5-195">Follow one of these steps:</span></span>

    - <span data-ttu-id="6dfc5-196">Přejděte do uzlu **Náklady za doručení \> Nastavení cesty s více úseky \> Úseky**.</span><span class="sxs-lookup"><span data-stu-id="6dfc5-196">Go to **Landed cost \> Multi-leg journey setup \> Legs**.</span></span> <span data-ttu-id="6dfc5-197">Vyberte úsek, pro který chcete nastavit aktualizaci stavu, a poté v podokně akcí vyberte možnost **Řídicí centrum sledování**.</span><span class="sxs-lookup"><span data-stu-id="6dfc5-197">Select the leg that you want to set up a status update for, and then, on the Action Pane, select **Tracking control center**.</span></span> <span data-ttu-id="6dfc5-198">Řídicí centrum sledování má předem načteno informace o vybraném úseku.</span><span class="sxs-lookup"><span data-stu-id="6dfc5-198">The Tracking control center is preloaded with information about the selected leg.</span></span>
    - <span data-ttu-id="6dfc5-199">Přejděte do uzlu **Náklady na doručení \> Nastavení informací o doručení \> Řídicí centrum sledování**.</span><span class="sxs-lookup"><span data-stu-id="6dfc5-199">Go to **Landed cost \> Delivery information setup \> Tracking control center**.</span></span> <span data-ttu-id="6dfc5-200">Potom musíte ručně vybrat úsek v kroku 4 tohoto postupu.</span><span class="sxs-lookup"><span data-stu-id="6dfc5-200">You must then manually select a leg in step 4 of this procedure.</span></span>

1. <span data-ttu-id="6dfc5-201">V podokně seznamu nastavte **Typ vytvoření** na *Aktualizace stavu*.</span><span class="sxs-lookup"><span data-stu-id="6dfc5-201">In the list pane, set the **Create type** field to *Status update*.</span></span>
1. <span data-ttu-id="6dfc5-202">V podokně akcí zvolte **Nový**.</span><span class="sxs-lookup"><span data-stu-id="6dfc5-202">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="6dfc5-203">Pokud jste začali z řídicího centra sledování v kroku 1, nastavte pole **Úsek** na úsek, pro který chcete vytvořit pravidlo aktualizace stavu.</span><span class="sxs-lookup"><span data-stu-id="6dfc5-203">If you started from the Tracking control center in step 1, set the **Leg** field to the leg that you want to create a status update rule for.</span></span> <span data-ttu-id="6dfc5-204">Pokud jste začali na stránce **Úseky**, pole **Úsek** je přednastaveno na úsek, který jste vybrali před otevřením řídicího centra sledování.</span><span class="sxs-lookup"><span data-stu-id="6dfc5-204">If you started from the **Legs** page, the **Leg** field is preset to the leg that you selected before you opened the Tracking control center.</span></span>

    <span data-ttu-id="6dfc5-205">Na základě hodnoty pole **Úsek** se automaticky nastaví několik polí, jak je znázorněno zde:</span><span class="sxs-lookup"><span data-stu-id="6dfc5-205">Based on the value of the **Leg** field, several fields are automatically set, as shown here:</span></span>

    - <span data-ttu-id="6dfc5-206">**Zdrojová tabulka:** *Kontejnerové aktivity*</span><span class="sxs-lookup"><span data-stu-id="6dfc5-206">**Source table:** *Container activities*</span></span>
    - <span data-ttu-id="6dfc5-207">**Zdrojové pole:** *Skutečné datum ukončení*</span><span class="sxs-lookup"><span data-stu-id="6dfc5-207">**Source field:** *Actual end date*</span></span>
    - <span data-ttu-id="6dfc5-208">**Cílová tabulka:** Toto pole je prázdné.</span><span class="sxs-lookup"><span data-stu-id="6dfc5-208">**Target table:** This field is left blank.</span></span>
    - <span data-ttu-id="6dfc5-209">**Cílové pole:** Toto pole je prázdné.</span><span class="sxs-lookup"><span data-stu-id="6dfc5-209">**Target field:** This field is left blank.</span></span>

1. <span data-ttu-id="6dfc5-210">V poli **Aktivita** vyberte aktivitu, na kterou by se vaše pravidlo mělo vztahovat.</span><span class="sxs-lookup"><span data-stu-id="6dfc5-210">In the **Activity** field, select the activity that your rule should apply to.</span></span>
1. <span data-ttu-id="6dfc5-211">Na záložce **Řádky** zapište aktualizace stavu pro každou nákladovou oblast.</span><span class="sxs-lookup"><span data-stu-id="6dfc5-211">On the **Lines** FastTab, enter the status updates for each cost area.</span></span>

### <a name="blank-type-rules"></a><span data-ttu-id="6dfc5-212">Pravidla prázdného typu</span><span class="sxs-lookup"><span data-stu-id="6dfc5-212">Blank type rules</span></span>

<span data-ttu-id="6dfc5-213">Používáte záznamy, které mají v poli **Typ vytvoření** hodnotu *Prázdný* pro přepsání nebo zadání hodnoty pole na základě údajů jiného pole.</span><span class="sxs-lookup"><span data-stu-id="6dfc5-213">You use records that have a **Create type** value of *Blank* to override or enter a field value, based on the data of another field.</span></span> <span data-ttu-id="6dfc5-214">Pole z Nákladů za doručení přepíše data v jiných oblastech Microsoftu Dynamics 365 Supply Chain Management na základě pravidel, která jsou nastavena v řídicím centru sledování.</span><span class="sxs-lookup"><span data-stu-id="6dfc5-214">A field from Landed cost will overwrite data in other areas of Microsoft Dynamics 365 Supply Chain Management, based on rules that are set up in the Tracking control center.</span></span>

1. <span data-ttu-id="6dfc5-215">Přejděte do uzlu **Náklady na doručení \> Nastavení informací o doručení \> Řídicí centrum sledování**.</span><span class="sxs-lookup"><span data-stu-id="6dfc5-215">Go to **Landed cost \> Delivery information setup \> Tracking control center**.</span></span>
1. <span data-ttu-id="6dfc5-216">V podokně seznamu nastavte **Typ vytvoření** na *Prázdný*.</span><span class="sxs-lookup"><span data-stu-id="6dfc5-216">In the list pane, set the **Create type** field to *Blank*.</span></span>
1. <span data-ttu-id="6dfc5-217">V podokně akcí zvolte **Nový**.</span><span class="sxs-lookup"><span data-stu-id="6dfc5-217">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="6dfc5-218">Definujte zdrojové a cílové hodnoty, kritéria shody, akci kopírování a další relevantní parametry, jak to vyžaduje vaše pravidlo.</span><span class="sxs-lookup"><span data-stu-id="6dfc5-218">Define the source and destination values, matching criteria, copy action, and other relevant parameters, as required for your rule.</span></span>

### <a name="required-tracking-control-setup"></a><span data-ttu-id="6dfc5-219">Požadované nastavení kontroly sledování</span><span class="sxs-lookup"><span data-stu-id="6dfc5-219">Required tracking control setup</span></span>

<span data-ttu-id="6dfc5-220">Pro každou šablonu cesty musí být v řídicím centru sledování nastaveny dva záznamy.</span><span class="sxs-lookup"><span data-stu-id="6dfc5-220">For every journey template, two records must be set up in the Tracking control center.</span></span> <span data-ttu-id="6dfc5-221">Oba tyto záznamy mají v poli **Typ vytvoření** hodnotu *Prázdný* a používají se ve všech implementacích nákladů za doručení.</span><span class="sxs-lookup"><span data-stu-id="6dfc5-221">Both these records have a **Create type** value of *Blank* and are used in all Landed cost implementations.</span></span> <span data-ttu-id="6dfc5-222">Pomáhají zajistit, aby datum potvrzení nákupu a očekávaná data zboží v přepravě byla aktualizována očekávaným způsobem pro cesty a související řádky nákupní objednávky.</span><span class="sxs-lookup"><span data-stu-id="6dfc5-222">They help ensure that the purchase confirmed date and goods in transit expected dates are updated for voyages and on related purchase order lines in the expected way.</span></span>

<span data-ttu-id="6dfc5-223">K aktualizaci řádků nákupu je vyžadován první záznam.</span><span class="sxs-lookup"><span data-stu-id="6dfc5-223">The first record is required to update purchase lines.</span></span> <span data-ttu-id="6dfc5-224">Musí mít následující nastavení:</span><span class="sxs-lookup"><span data-stu-id="6dfc5-224">It must have the following settings:</span></span>

- <span data-ttu-id="6dfc5-225">**Zdrojová tabulka:** *Kontejnerové aktivity*</span><span class="sxs-lookup"><span data-stu-id="6dfc5-225">**Source table:** *Container activities*</span></span>
- <span data-ttu-id="6dfc5-226">**Zdrojové pole:** *Odhadované datum ukončení*</span><span class="sxs-lookup"><span data-stu-id="6dfc5-226">**Source field:** *Estimated end date*</span></span>
- <span data-ttu-id="6dfc5-227">**Cílová tabulka:** *Nákupní řádky*</span><span class="sxs-lookup"><span data-stu-id="6dfc5-227">**Target table:** *Purchase lines*</span></span>
- <span data-ttu-id="6dfc5-228">**Cílové pole:** *Potvrzeno nebo datum dodání*</span><span class="sxs-lookup"><span data-stu-id="6dfc5-228">**Target field:** *Confirmed or delivery date*</span></span>

<span data-ttu-id="6dfc5-229">Druhý záznam je nutný k aktualizaci zboží v přepravních transakcích.</span><span class="sxs-lookup"><span data-stu-id="6dfc5-229">The second record is required to update goods in transit transactions.</span></span> <span data-ttu-id="6dfc5-230">Musí mít následující nastavení:</span><span class="sxs-lookup"><span data-stu-id="6dfc5-230">It must have the following settings:</span></span>

- <span data-ttu-id="6dfc5-231">**Zdrojová tabulka:** *Kontejnerové aktivity*</span><span class="sxs-lookup"><span data-stu-id="6dfc5-231">**Source table:** *Container activities*</span></span>
- <span data-ttu-id="6dfc5-232">**Zdrojové pole:** *Odhadované datum ukončení*</span><span class="sxs-lookup"><span data-stu-id="6dfc5-232">**Source field:** *Estimated end date*</span></span>
- <span data-ttu-id="6dfc5-233">**Cílová tabulka:** *Objednávka přepravovaného zboží*</span><span class="sxs-lookup"><span data-stu-id="6dfc5-233">**Target table:** *Goods in transit order*</span></span>
- <span data-ttu-id="6dfc5-234">**Cílové pole:** *Očekávané datum*</span><span class="sxs-lookup"><span data-stu-id="6dfc5-234">**Target field:** *Expected date*</span></span>