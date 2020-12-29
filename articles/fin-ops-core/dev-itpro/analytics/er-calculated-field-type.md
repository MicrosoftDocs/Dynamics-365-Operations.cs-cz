---
title: Podpora parametrizovaných volání zdrojů dat ER typu vypočítaného pole
description: Toto téma obsahuje informace o způsobu použití typu vypočítaného pole pro zdroje dat ER.
author: NickSelin
manager: AnnBe
ms.date: 08/06/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: ''
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 3f21b323ddbf653bf8ca8dd1f879a6bdbddcdefc
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 12/05/2020
ms.locfileid: "4681249"
---
# <a name="support-parameterized-calls-of-er-data-sources-of-the-calculated-field-type"></a><span data-ttu-id="f9dfe-103">Podpora parametrizovaných volání zdrojů dat ER typu vypočítaného pole</span><span class="sxs-lookup"><span data-stu-id="f9dfe-103">Support parameterized calls of ER data sources of the Calculated field type</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="f9dfe-104">V tomto tématu je vysvětleno, jak můžete vytvořit zdroj dat Elektronického vykazování (ER) pomocí typu **Vypočítaného pole**.</span><span class="sxs-lookup"><span data-stu-id="f9dfe-104">This topic explains how you can design an Electronic reporting (ER) data source by using the **Calculated field** type.</span></span> <span data-ttu-id="f9dfe-105">Tento zdroj dat může obsahovat výraz ER, který po spuštění může být řízen hodnotami argumentů parametrů, které jsou nakonfigurovány ve vazbě, která volá tento zdroj dat.</span><span class="sxs-lookup"><span data-stu-id="f9dfe-105">This data source may contain an ER expression that, when executed, can be controlled by the values of the parameter arguments that are configured in a binding that calls this data source.</span></span> <span data-ttu-id="f9dfe-106">Konfigurací parametrizovaných volání takového zdroje dat můžete znovu použít jeden zdroj dat v mnoha vazbách, čímž snížíte celkový počet datových zdrojů, které musí být nakonfigurovány v mapování modelu ER nebo ve formátech ER.</span><span class="sxs-lookup"><span data-stu-id="f9dfe-106">By configuring parameterized calls of such a data source, you can reuse a single data source in many bindings, which reduces the total number of data sources that must be configured in ER model mappings or ER formats.</span></span> <span data-ttu-id="f9dfe-107">Také zjednodušuje konfigurovanou komponentu ER, která snižuje náklady na údržbu a náklady na použití ostatních odběratelů.</span><span class="sxs-lookup"><span data-stu-id="f9dfe-107">It also simplifies the configured ER component, which reduces the maintenance costs and the cost of use by other consumers.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="f9dfe-108">Předpoklady</span><span class="sxs-lookup"><span data-stu-id="f9dfe-108">Prerequisites</span></span>
<span data-ttu-id="f9dfe-109">Pro dokončení příkladů v tomto tématu musíte mít následující přístup:</span><span class="sxs-lookup"><span data-stu-id="f9dfe-109">To complete the examples in this topic, you must have the following access:</span></span>

- <span data-ttu-id="f9dfe-110">Přístup k jedné z těchto rolí:</span><span class="sxs-lookup"><span data-stu-id="f9dfe-110">Access to one of these roles:</span></span>

    - <span data-ttu-id="f9dfe-111">Návrhář elektronického výkaznictví</span><span class="sxs-lookup"><span data-stu-id="f9dfe-111">Electronic reporting developer</span></span>
    - <span data-ttu-id="f9dfe-112">Funkční konzultant elektronického výkaznictví</span><span class="sxs-lookup"><span data-stu-id="f9dfe-112">Electronic reporting functional consultant</span></span>
    - <span data-ttu-id="f9dfe-113">Správce systému</span><span class="sxs-lookup"><span data-stu-id="f9dfe-113">System administrator</span></span>

- <span data-ttu-id="f9dfe-114">Přístup k službám Regulatory Configuration Services (RCS), které byly zřízeny pro stejného klienta jako Finance and Operations, pro jednu z následujících rolí:</span><span class="sxs-lookup"><span data-stu-id="f9dfe-114">Access to Regulatory Configuration Services (RCS) that have been provisioned for the same tenant as Finance and Operations for one of the following roles:</span></span>

    - <span data-ttu-id="f9dfe-115">Návrhář elektronického výkaznictví</span><span class="sxs-lookup"><span data-stu-id="f9dfe-115">Electronic reporting developer</span></span>
    - <span data-ttu-id="f9dfe-116">Funkční konzultant elektronického výkaznictví</span><span class="sxs-lookup"><span data-stu-id="f9dfe-116">Electronic reporting functional consultant</span></span>
    - <span data-ttu-id="f9dfe-117">Správce systému</span><span class="sxs-lookup"><span data-stu-id="f9dfe-117">System administrator</span></span>

<span data-ttu-id="f9dfe-118">Je také nutné stáhnout a lokálně uložit následující soubory.</span><span class="sxs-lookup"><span data-stu-id="f9dfe-118">You must also download and locally store the following files.</span></span>

| <span data-ttu-id="f9dfe-119">**Obsah**</span><span class="sxs-lookup"><span data-stu-id="f9dfe-119">**Content**</span></span>                           | <span data-ttu-id="f9dfe-120">**Název souboru**</span><span class="sxs-lookup"><span data-stu-id="f9dfe-120">**File name**</span></span>                                        |
|---------------------------------------|------------------------------------------------------|
| <span data-ttu-id="f9dfe-121">Vzorová konfigurace datového modelu elektronického výkaznictví</span><span class="sxs-lookup"><span data-stu-id="f9dfe-121">Sample ER data model configuration</span></span>    | [<span data-ttu-id="f9dfe-122">Model pro informace o volání s parametry calls.version.1.xml</span><span class="sxs-lookup"><span data-stu-id="f9dfe-122">Model to learn parameterized calls.version.1.xml</span></span>](https://mbs.microsoft.com/customersource/global/AX/downloads/hot-fixes/365optelecrepeg)     |
| <span data-ttu-id="f9dfe-123">Vzorová konfigurace metadat elektronického výkaznictví</span><span class="sxs-lookup"><span data-stu-id="f9dfe-123">Sample ER metadata configuration</span></span>      | [<span data-ttu-id="f9dfe-124">Metadata pro informace o volání s parametry calls.version.1.xml</span><span class="sxs-lookup"><span data-stu-id="f9dfe-124">Metadata to learn parameterized calls.version.1.xml</span></span>](https://mbs.microsoft.com/customersource/global/AX/downloads/hot-fixes/365optelecrepeg)  |
| <span data-ttu-id="f9dfe-125">Vzorová konfigurace mapování elektronického výkaznictví</span><span class="sxs-lookup"><span data-stu-id="f9dfe-125">Sample ER model mapping configuration</span></span> | [<span data-ttu-id="f9dfe-126">Mapování pro informace o volání s parametry calls.version.1.1.xml</span><span class="sxs-lookup"><span data-stu-id="f9dfe-126">Mapping to learn parameterized calls.version.1.1.xml</span></span>](https://mbs.microsoft.com/customersource/global/AX/downloads/hot-fixes/365optelecrepeg) |
| <span data-ttu-id="f9dfe-127">Vzorová konfigurace formátu elektronického výkaznictví</span><span class="sxs-lookup"><span data-stu-id="f9dfe-127">Sample ER format configuration</span></span>        | [<span data-ttu-id="f9dfe-128">Formát pro informace o volání s parametry calls.version.1.1.xml</span><span class="sxs-lookup"><span data-stu-id="f9dfe-128">Format to learn parameterized calls.version.1.1.xml</span></span>](https://mbs.microsoft.com/customersource/global/AX/downloads/hot-fixes/365optelecrepeg)  |

## <a name="sign-in-to-your-rcs-instance"></a><span data-ttu-id="f9dfe-129">Přihlaste se k instanci RCS.</span><span class="sxs-lookup"><span data-stu-id="f9dfe-129">Sign in to your RCS instance</span></span>
<span data-ttu-id="f9dfe-130">V tomto příkladu vytvoříte konfiguraci pro vzorovou společnost Litware, Inc. Nejprve musíte v RCS dokončit krok v proceduře [Vytvoření poskytovatelů konfigurace a jejich označení jako aktivních](tasks/er-configuration-provider-mark-it-active-2016-11.md).</span><span class="sxs-lookup"><span data-stu-id="f9dfe-130">In this example, you will create a configuration for the sample company, Litware, Inc. First, in RCS, you must complete the steps in the [Create configuration providers and mark them as active](tasks/er-configuration-provider-mark-it-active-2016-11.md) procedure:</span></span>

1. <span data-ttu-id="f9dfe-131">Na výchozím řídicím panelu vyberte **Elektronické vykazování**.</span><span class="sxs-lookup"><span data-stu-id="f9dfe-131">On the default dashboard, select **Electronic reporting**.</span></span>
2. <span data-ttu-id="f9dfe-132">Vyberte **Konfigurace vykazování**.</span><span class="sxs-lookup"><span data-stu-id="f9dfe-132">Select **Reporting configurations**.</span></span>
3. <span data-ttu-id="f9dfe-133">Import stažených konfigurací do RCS v následujícím pořadí: datový model, metadata, mapování modelu, formát.</span><span class="sxs-lookup"><span data-stu-id="f9dfe-133">Import the downloaded configurations to RCS in the following sequence: data model, metadata, model mapping, format.</span></span> <span data-ttu-id="f9dfe-134">Pro každou konfiguraci ER proveďte následující kroky:</span><span class="sxs-lookup"><span data-stu-id="f9dfe-134">Complete the following steps for each ER configuration:</span></span>

    1. <span data-ttu-id="f9dfe-135">Vyberte **Exchange**.</span><span class="sxs-lookup"><span data-stu-id="f9dfe-135">Select **Exchange.**</span></span>
    2. <span data-ttu-id="f9dfe-136">Vyberte **Načíst ze souboru XML**.</span><span class="sxs-lookup"><span data-stu-id="f9dfe-136">Select **Load from XML file**.</span></span>
    3. <span data-ttu-id="f9dfe-137">Zvolte **Procházet** a pak vyberte požadovanou konfiguraci elektronického výkaznictví ve formátu XML.</span><span class="sxs-lookup"><span data-stu-id="f9dfe-137">Select **Browse**, and then select the required ER configuration in XML format.</span></span>
    4. <span data-ttu-id="f9dfe-138">Vyberte **OK**.</span><span class="sxs-lookup"><span data-stu-id="f9dfe-138">Select **OK.**</span></span>

## <a name="review-the-provided-er-solution"></a><span data-ttu-id="f9dfe-139">Zkontrolovat poskytnuté řešení ER</span><span class="sxs-lookup"><span data-stu-id="f9dfe-139">Review the provided ER solution</span></span>

### <a name="review-model-mapping"></a><span data-ttu-id="f9dfe-140">Kontrola mapování modelu</span><span class="sxs-lookup"><span data-stu-id="f9dfe-140">Review model mapping</span></span>

1. <span data-ttu-id="f9dfe-141">Ve stromu konfigurace rozbalte obsah položky **Model pro seznámení s parametrizovanými voláními**.</span><span class="sxs-lookup"><span data-stu-id="f9dfe-141">In the configuration tree, expand the content of the **Model to learn parameterized calls** item.</span></span>
2. <span data-ttu-id="f9dfe-142">Vyberte **Mapování pro informace o voláních s parametry**.</span><span class="sxs-lookup"><span data-stu-id="f9dfe-142">Select **Mapping to learn parameterized calls**.</span></span>
3. <span data-ttu-id="f9dfe-143">Vyberte možnost **Návrhář**.</span><span class="sxs-lookup"><span data-stu-id="f9dfe-143">Select **Designer**.</span></span>
4. <span data-ttu-id="f9dfe-144">Vyberte možnost **Návrhář**.</span><span class="sxs-lookup"><span data-stu-id="f9dfe-144">Select **Designer**.</span></span>  
   
    <span data-ttu-id="f9dfe-145">Toto mapování modelu ER je navrženo k následujícím akcím:</span><span class="sxs-lookup"><span data-stu-id="f9dfe-145">This ER model mapping is designed to do the following:</span></span>

    - <span data-ttu-id="f9dfe-146">Načtení seznamu daňových kódů (**Daňový** zdroj dat) nacházející se v tabulce **TaxTable**.</span><span class="sxs-lookup"><span data-stu-id="f9dfe-146">Fetch the list of tax codes (**Tax** data source) residing in the **TaxTable** table.</span></span>
    - <span data-ttu-id="f9dfe-147">Načtení seznamu daňových transakcí (**Trans** zdroj dat) nacházející se v tabulce **TaxTrans**:</span><span class="sxs-lookup"><span data-stu-id="f9dfe-147">Fetch the list of tax transactions (**Trans** data source) residing in the **TaxTrans** table:</span></span>
    
        - <span data-ttu-id="f9dfe-148">Seskupit seznam načtených transakcí (**Gr** zdroj dat) podle kódu daně</span><span class="sxs-lookup"><span data-stu-id="f9dfe-148">Group the list of fetched transactions (**Gr** data source) by tax code.</span></span>
        - <span data-ttu-id="f9dfe-149">Vypočítat pro seskupené transakce po agregovaných hodnotách podle kódu daně:</span><span class="sxs-lookup"><span data-stu-id="f9dfe-149">Calculate for grouped transactions following aggregated values per tax code:</span></span>

            - <span data-ttu-id="f9dfe-150">Součet hodnot základu daně.</span><span class="sxs-lookup"><span data-stu-id="f9dfe-150">Sum of tax base values.</span></span>
            - <span data-ttu-id="f9dfe-151">Součet hodnot daně.</span><span class="sxs-lookup"><span data-stu-id="f9dfe-151">Sum of tax values.</span></span>
            - <span data-ttu-id="f9dfe-152">Minimální hodnota uplatněné sazby daně.</span><span class="sxs-lookup"><span data-stu-id="f9dfe-152">Minimum value of applied tax rate.</span></span>

    <span data-ttu-id="f9dfe-153">Mapování modelu v této konfiguraci implementuje základní datový model pro všechny formáty ER vytvořené pro tento model a prováděné ve Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="f9dfe-153">The model mapping in this configuration implements the base data model for any of the ER formats created for this model and executed in Finance and Operations.</span></span> <span data-ttu-id="f9dfe-154">V důsledku toho je obsah zdrojů dat **Daň** a **Gr** vystaven pro formáty ER, jako jsou například abstraktní zdroje dat.</span><span class="sxs-lookup"><span data-stu-id="f9dfe-154">As a result, the content of the **Tax** and **Gr** data sources is exposed for ER formats such as abstract data sources.</span></span>

    ![Stránka Návrhář mapování modelu zobrazující zdroje dat Daň a Gr](media/er-calculated-field-type-01.png)

5.  <span data-ttu-id="f9dfe-156">Zavřete stránku **Návrhář mapování modelu**.</span><span class="sxs-lookup"><span data-stu-id="f9dfe-156">Close the **Model mapping designer** page.</span></span>
6.  <span data-ttu-id="f9dfe-157">Zavřete stránku **Mapování modelu**.</span><span class="sxs-lookup"><span data-stu-id="f9dfe-157">Close the **Model mapping** page.</span></span>

### <a name="review-format"></a><span data-ttu-id="f9dfe-158">Zkontrolovat formát</span><span class="sxs-lookup"><span data-stu-id="f9dfe-158">Review format</span></span>

1. <span data-ttu-id="f9dfe-159">Ve stromu konfigurace rozbalte obsah položky **Model pro seznámení s parametrizovanými voláními**.</span><span class="sxs-lookup"><span data-stu-id="f9dfe-159">In the configuration tree, expand the content of the **Model to learn parameterized calls** item.</span></span>
2. <span data-ttu-id="f9dfe-160">Vyberte **Formát pro informace o voláních s parametry**.</span><span class="sxs-lookup"><span data-stu-id="f9dfe-160">Select **Format to learn parameterized calls**.</span></span>
3. <span data-ttu-id="f9dfe-161">Vyberte možnost **Návrhář**.</span><span class="sxs-lookup"><span data-stu-id="f9dfe-161">Select **Designer**.</span></span> <span data-ttu-id="f9dfe-162">Tento formát ER je navržen k následujícím akcím:</span><span class="sxs-lookup"><span data-stu-id="f9dfe-162">This ER format is designed to do the following:</span></span>

    - <span data-ttu-id="f9dfe-163">Generujte daňový výkaz ve formátu XML.</span><span class="sxs-lookup"><span data-stu-id="f9dfe-163">Generate a tax statement in XML format.</span></span>
    - <span data-ttu-id="f9dfe-164">V daňovém výkazu prezentujte následující úrovně zdanění: normální, snížené a žádné.</span><span class="sxs-lookup"><span data-stu-id="f9dfe-164">Present the following levels of taxation in the tax statement: regular, reduced, and none.</span></span>
    - <span data-ttu-id="f9dfe-165">Prezentujte více podrobností na každé úrovni zdanění, které mají různý počet podrobností na každé úrovni.</span><span class="sxs-lookup"><span data-stu-id="f9dfe-165">Present multiple details at each taxation level, having a different number of details in each level.</span></span>

    ![Stránka návrháře formátu](media/er-calculated-field-type-02.png)

4. <span data-ttu-id="f9dfe-167">Vyberte **Mapování**.</span><span class="sxs-lookup"><span data-stu-id="f9dfe-167">Select **Mapping**.</span></span>
5. <span data-ttu-id="f9dfe-168">Rozbaltepoložky **Model**, **Data** a **Souhrnné** .</span><span class="sxs-lookup"><span data-stu-id="f9dfe-168">Expand the **Model**, **Data,** and **Summary** items.</span></span> 

    <span data-ttu-id="f9dfe-169">Vpočítané pole **Model.Data.Summary.Leve** obsahuje výraz vracející kód úrovně zdanění (**Pravidelný**, **Snížený**, **Žádný** nebo **Jiný**) jako textovou hodnotu pro libovolný kód daně, který lze načíst ze zdroje dat **Model.Data.Summary** za běhu.</span><span class="sxs-lookup"><span data-stu-id="f9dfe-169">The calculated field **Model.Data.Summary.Level** contains the expression that returns the code of the taxation level (**Regular**, **Reduced**, **None,** or **Other**) as a text value for any tax code that can be retrieved from the **Model.Data.Summary** data source at run time.</span></span>

    ![Stránka návrháře formátu s podrobnostmi o modelu datového modelu pro zjištění parametrizovaných hovorů](media/er-calculated-field-type-03.png)

6. <span data-ttu-id="f9dfe-171">Rozbalte položku **Model**.**Data2**.</span><span class="sxs-lookup"><span data-stu-id="f9dfe-171">Expand the **Model**.**Data2** item.</span></span>
7. <span data-ttu-id="f9dfe-172">Rozbalte položku **Model**.**Data2.Summary2**.</span><span class="sxs-lookup"><span data-stu-id="f9dfe-172">Expand the **Model**.**Data2.Summary2** item.</span></span>
   
    <span data-ttu-id="f9dfe-173">Datový zdroj **Model**.**Data2.Summary2** je konfigurováno pro seskupení podrobností transakcí datového zdroje **Model.Data.Summary** podle úrovně zdanění (vráceno vypočítaným polem **Model.Data.Summary.Level**) a výpočet agregací.</span><span class="sxs-lookup"><span data-stu-id="f9dfe-173">The **Model**.**Data2.Summary2** data source is configured to group the **Model.Data.Summary** data source transaction details by taxation level (returned by the **Model.Data.Summary.Level** calculated field) and compute the aggregations.</span></span>

    ![Stránka návrháře formátu s podrobnostmi o zdroji dat Model.Data2.Summary2](media/er-calculated-field-type-04.png)

8. <span data-ttu-id="f9dfe-175">Zkontrolujte vypočítaná pole **Model**.**Data2.Level1**, **Model**.**Data2.Level2** a **Model**.**Data2.Level3.**</span><span class="sxs-lookup"><span data-stu-id="f9dfe-175">Review the calculated fields **Model**.**Data2.Level1**, **Model**.**Data2.Level2**, and **Model**.**Data2.Level3.**</span></span> <span data-ttu-id="f9dfe-176">Tato vypočítaná pole slouží k filtrování seznamu záznamů **Model**.**Data2.Summary2** a vrátí pouze záznamy, které reprezentují určitou úroveň zdanění.</span><span class="sxs-lookup"><span data-stu-id="f9dfe-176">These calculated fields are used to filter the **Model**.**Data2.Summary2** records list and return only records that represent a particular taxation level.</span></span>
9. <span data-ttu-id="f9dfe-177">Zavřete stránku **Návrhář formátu**.</span><span class="sxs-lookup"><span data-stu-id="f9dfe-177">Close the **Format designer** page.</span></span>

## <a name="create-a-derived-format"></a><span data-ttu-id="f9dfe-178">Vytvoření odvozeného formátu</span><span class="sxs-lookup"><span data-stu-id="f9dfe-178">Create a derived format</span></span>
<span data-ttu-id="f9dfe-179">Poskytnutý formát lze zlepšit přidáním jednoho vypočítaného pole pro filtrování požadované úrovně zdanění namísto použití existujících tří polí: **Model**.**Data2.Level1**, **Model**.**Data2.Level2** a **Model**.**Data2.Level3**.</span><span class="sxs-lookup"><span data-stu-id="f9dfe-179">You can improve the provided format by adding one calculated field to filter the required taxation level instead of using the existing three fields: **Model**.**Data2.Level1**, **Model**.**Data2.Level2,** and **Model**.**Data2.Level3**.</span></span> <span data-ttu-id="f9dfe-180">Požadovanou úroveň zdanění lze zadat v místě, kde bude voláno nové vypočtené pole.</span><span class="sxs-lookup"><span data-stu-id="f9dfe-180">The required taxation level can be specified in the location where this new calculated field will be called.</span></span>

1. <span data-ttu-id="f9dfe-181">Ve stromu konfigurace rozbalte obsah položky **Model pro seznámení s parametrizovanými voláními**.</span><span class="sxs-lookup"><span data-stu-id="f9dfe-181">In the configuration tree, expand the content of the **Model to learn parameterized calls** item.</span></span>
2. <span data-ttu-id="f9dfe-182">Vyberte **Formát pro informace o voláních s parametry**.</span><span class="sxs-lookup"><span data-stu-id="f9dfe-182">Select **Format to learn parameterized calls**.</span></span>
3. <span data-ttu-id="f9dfe-183">Vyberte **Vytvořit konfiguraci**.</span><span class="sxs-lookup"><span data-stu-id="f9dfe-183">Select **Create configuration**.</span></span>
4. <span data-ttu-id="f9dfe-184">Vyberte možnost **Odvozeno od názvu: Formát pro informace o parametrizovaných volání, Microsoft**.</span><span class="sxs-lookup"><span data-stu-id="f9dfe-184">Select **Derive from Name: Format to learn parameterized calls, Microsoft**.</span></span>
5. <span data-ttu-id="f9dfe-185">Do pole **Název** zadejte **Formát pro učení parametrizovaných volání (vlastní)**.</span><span class="sxs-lookup"><span data-stu-id="f9dfe-185">In the **Name** field, enter **Format to learn parameterized calls (custom)**.</span></span>
6. <span data-ttu-id="f9dfe-186">Vyberte **Vytvořit konfiguraci**.</span><span class="sxs-lookup"><span data-stu-id="f9dfe-186">Select **Create configuration.**</span></span>

## <a name="configure-a-parameterized-calculated-field-that-returns-a-list-of-records"></a><span data-ttu-id="f9dfe-187">Konfigurace parametrizovaného vypočítaného pole, které vrací seznam záznamů</span><span class="sxs-lookup"><span data-stu-id="f9dfe-187">Configure a parameterized calculated field that returns a list of records</span></span>

### <a name="start-adding-a-new-calculated-field"></a><span data-ttu-id="f9dfe-188">Začít přidávat nové počítané pole</span><span class="sxs-lookup"><span data-stu-id="f9dfe-188">Start adding a new calculated field</span></span>

1. <span data-ttu-id="f9dfe-189">Vyberte možnost **Návrhář**.</span><span class="sxs-lookup"><span data-stu-id="f9dfe-189">Select **Designer**.</span></span>
2. <span data-ttu-id="f9dfe-190">Vyberte **Rozbalit/sbalit** pro rozbalení všechn položek formátu.</span><span class="sxs-lookup"><span data-stu-id="f9dfe-190">Select **Expand/collapse** to expand all format items.</span></span>
3. <span data-ttu-id="f9dfe-191">Vyberte **Mapování**.</span><span class="sxs-lookup"><span data-stu-id="f9dfe-191">Select **Mapping**.</span></span>
4. <span data-ttu-id="f9dfe-192">Rozbalte položku **Model**.</span><span class="sxs-lookup"><span data-stu-id="f9dfe-192">Expand the **Model** item.</span></span>
5. <span data-ttu-id="f9dfe-193">Vyberte položku **Model.Data2**.</span><span class="sxs-lookup"><span data-stu-id="f9dfe-193">Select the **Model.Data2** item.</span></span>
6. <span data-ttu-id="f9dfe-194">Vyberte **přidat**.</span><span class="sxs-lookup"><span data-stu-id="f9dfe-194">Select **Add**.</span></span>
7. <span data-ttu-id="f9dfe-195">Vyberte **Funkce\\vypočítané pole**.</span><span class="sxs-lookup"><span data-stu-id="f9dfe-195">Select **Functions\\Calculated field**.</span></span>
8. <span data-ttu-id="f9dfe-196">Do pole **Název** zadejte **Úrovně**.</span><span class="sxs-lookup"><span data-stu-id="f9dfe-196">In the **Name** field, enter **Levels**.</span></span>
9. <span data-ttu-id="f9dfe-197">Vyberte možnost **Upravit vzorec**.</span><span class="sxs-lookup"><span data-stu-id="f9dfe-197">Select **Edit formula**.</span></span>

### <a name="define-a-parameter-for-adding-a-calculated-field"></a><span data-ttu-id="f9dfe-198">Definovat parametr pro přidání vypočítaného pole</span><span class="sxs-lookup"><span data-stu-id="f9dfe-198">Define a parameter for adding a calculated field</span></span>

1. <span data-ttu-id="f9dfe-199">Vyberte **Parametry**.</span><span class="sxs-lookup"><span data-stu-id="f9dfe-199">Select **Parameters**.</span></span>
2. <span data-ttu-id="f9dfe-200">Zvolte **Nové**.</span><span class="sxs-lookup"><span data-stu-id="f9dfe-200">Select **New**.</span></span>
3. <span data-ttu-id="f9dfe-201">Do pole **Název** zadejte **Úroveň zdanění**.</span><span class="sxs-lookup"><span data-stu-id="f9dfe-201">In the **Name** field, enter **Taxation Level**.</span></span>
4. <span data-ttu-id="f9dfe-202">V poli **Typ** vyberte **Řetězec**.</span><span class="sxs-lookup"><span data-stu-id="f9dfe-202">In the **Type** field, select **String**.</span></span>

    <span data-ttu-id="f9dfe-203">K zadání typu argumentu parametru lze použít pouze primitivní datové typy.</span><span class="sxs-lookup"><span data-stu-id="f9dfe-203">Only primitive data types can be used to specify the type of the parameter’s argument.</span></span> <span data-ttu-id="f9dfe-204">Proto nelze pro tento účel použít typy **Seznam záznamů**, **Záznam** a **Výčet**.</span><span class="sxs-lookup"><span data-stu-id="f9dfe-204">Therefore, **Record list**, **Record**, and **Enum** types cannot be used for this purpose.</span></span>

    <span data-ttu-id="f9dfe-205">Maximální počet parametrů, které lze zadat pro jedno vypočtené pole, je 8.</span><span class="sxs-lookup"><span data-stu-id="f9dfe-205">The maximum number of parameters that can be specified for a single calculated field is 8.</span></span>

    ![Seznam zdroje dat parametrů](media/er-calculated-field-type-05.png)

5. <span data-ttu-id="f9dfe-207">Vyberte **OK**.</span><span class="sxs-lookup"><span data-stu-id="f9dfe-207">Select **OK**.</span></span>

<span data-ttu-id="f9dfe-208">Přidáte-li tento parametr, zadáte podmínku, která musí být na místě, aby bylo možné toto vypočtené pole volat.</span><span class="sxs-lookup"><span data-stu-id="f9dfe-208">By adding this parameter, you specify the condition that must be in place to call this calculated field.</span></span> <span data-ttu-id="f9dfe-209">Při volání tohoto vypočítaného pole je nutné zadat argument parametru **Úroveň zdanění** jako hodnotu s formátem **Řetězec**.</span><span class="sxs-lookup"><span data-stu-id="f9dfe-209">When you call this calculated field, you need to specify the argument of the **Taxation Level** parameter as a value with **String** format.</span></span>

   <span data-ttu-id="f9dfe-210">Ujistěte se, že definujete parametry pouze pro vypočítaná pole, která jsou uložena v kontejneru (**Seznam záznamů**, **Záznam** nebo **Kontejner**).</span><span class="sxs-lookup"><span data-stu-id="f9dfe-210">Make sure that you define parameters only for those calculated fields that reside in a container (either **Record list**, **Record**, or **Container**).</span></span>

   <span data-ttu-id="f9dfe-211">Konfigurovaný parametr je k dispozici v seznamu zdrojů dat pro toto vypočtené pole.</span><span class="sxs-lookup"><span data-stu-id="f9dfe-211">The configured parameter is available in the list of data sources for this calculated field.</span></span> <span data-ttu-id="f9dfe-212">Chcete-li přidat parametr do konfigurovaného výrazu, vyberte možnost **Přidat zdroj dat**.</span><span class="sxs-lookup"><span data-stu-id="f9dfe-212">You can add the parameter to the configured expression by selecting **Add data source**.</span></span>

   ![Pole zdroje dat](media/er-calculated-field-type-06.png)

### <a name="define-an-expression-for-adding-a-calculated-field"></a><span data-ttu-id="f9dfe-214">Definovat výraz pro přidání vypočítaného pole</span><span class="sxs-lookup"><span data-stu-id="f9dfe-214">Define an expression for adding a calculated field</span></span>

1. <span data-ttu-id="f9dfe-215">Do pole **Vzorec** zdejte:</span><span class="sxs-lookup"><span data-stu-id="f9dfe-215">In the **Formula** field, enter:</span></span> 

    <span data-ttu-id="f9dfe-216">**WHERE(\@.Summary2, \@.Summary2.grouped.Level =**</span><span class="sxs-lookup"><span data-stu-id="f9dfe-216">**WHERE(\@.Summary2, \@.Summary2.grouped.Level =**</span></span>
    
2. <span data-ttu-id="f9dfe-217">V seznamu zdrojů dat vyberte parametr **Úroveň zdanění**.</span><span class="sxs-lookup"><span data-stu-id="f9dfe-217">Select the **Taxation Level** parameter in the list of data sources.</span></span>
3. <span data-ttu-id="f9dfe-218">Vyberte **Přidat zdroj dat**.</span><span class="sxs-lookup"><span data-stu-id="f9dfe-218">Select **Add data source**.</span></span>
4. <span data-ttu-id="f9dfe-219">V poli **Vzorec** dokončete výraz jako:</span><span class="sxs-lookup"><span data-stu-id="f9dfe-219">In the **Formula** field, finalize the expression as:</span></span>  

    <span data-ttu-id="f9dfe-220">**WHERE(\@.Summary2, \@.Summary2.grouped.Level = 'Taxation Level')**</span><span class="sxs-lookup"><span data-stu-id="f9dfe-220">**WHERE(\@.Summary2, \@.Summary2.grouped.Level = 'Taxation Level')**</span></span>

5. <span data-ttu-id="f9dfe-221">Zvolte **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="f9dfe-221">Select **Save**.</span></span>

    ![Informace o datových zdrojových polích](media/er-calculated-field-type-07.png)

6. <span data-ttu-id="f9dfe-223">Zavřete stránku **Návrhář vzorce**.</span><span class="sxs-lookup"><span data-stu-id="f9dfe-223">Close the **Formula designer** page.</span></span>

### <a name="finish-adding-a-new-calculated-field"></a><span data-ttu-id="f9dfe-224">Dokončete přidávávání nových počítaných polí</span><span class="sxs-lookup"><span data-stu-id="f9dfe-224">Finish adding a new calculated field</span></span>

- <span data-ttu-id="f9dfe-225">Vyberte **OK**.</span><span class="sxs-lookup"><span data-stu-id="f9dfe-225">Select **OK**.</span></span>

<span data-ttu-id="f9dfe-226">Na stránce **Návrhář formátu** je v konfigurovaných vypočítaných polích **Úrovně** vyžadován argument **Řetězec**.</span><span class="sxs-lookup"><span data-stu-id="f9dfe-226">On the **Format designer** page, the configured parameterized calculated field **Levels** requires a **String** argument.</span></span>

![Rozbalený seznam úrovní vypočítaných polí](media/er-calculated-field-type-08.png)

### <a name="use-the-configured-calculated-field-for-binding-format-elements"></a><span data-ttu-id="f9dfe-228">Použít nakonfigurované počítané pole pro prvky formátu vazby</span><span class="sxs-lookup"><span data-stu-id="f9dfe-228">Use the configured calculated field for binding format elements</span></span>

1. <span data-ttu-id="f9dfe-229">Výběrem **Model.Data2.Levels** vyberte nakonfigurované počítané pole.</span><span class="sxs-lookup"><span data-stu-id="f9dfe-229">Select **Model.Data2.Levels** to select the configured calculated field.</span></span>
2. <span data-ttu-id="f9dfe-230">Vyberte prvek formátu **Statement.Taxation.Regular**.</span><span class="sxs-lookup"><span data-stu-id="f9dfe-230">Select the **Statement.Taxation.Regular** format element.</span></span>
3. <span data-ttu-id="f9dfe-231">Vyberte možnost **vazba**.</span><span class="sxs-lookup"><span data-stu-id="f9dfe-231">Select **Bind**.</span></span>
4. <span data-ttu-id="f9dfe-232">Vyberte možnost **Ano**, pokud chcete potvrdit nahrazení aktuálně používaného zdroje dat **Level1** novým zdrojem dat **Levels** ve všech vnořených formátovacích prvcích vybraného prvku formátu.</span><span class="sxs-lookup"><span data-stu-id="f9dfe-232">Select **Yes** to confirm the replacement of the currently used data source, **Level1**, by the new data source, **Levels**, in all nested format elements of the selected format element.</span></span>

    <span data-ttu-id="f9dfe-233">Použitá vazba byla sestavena jako volání parametrizovaného počítaného pole.</span><span class="sxs-lookup"><span data-stu-id="f9dfe-233">Applied binding has been built as a call of the parameterized calculated field.</span></span> <span data-ttu-id="f9dfe-234">Standardně se název prvku vázaného formátu používá jako argument pro parametrizované počítané pole za následujících podmínek:</span><span class="sxs-lookup"><span data-stu-id="f9dfe-234">By default, the name of the bound format element is used as an argument for parameterized calculated field under the following conditions:</span></span>

      - <span data-ttu-id="f9dfe-235">Vypočítané pole je nakonfigurováno pro použití jediného parametru.</span><span class="sxs-lookup"><span data-stu-id="f9dfe-235">The calculated field is configured to use a single parameter.</span></span>
      - <span data-ttu-id="f9dfe-236">Datový typ tohoto parametru je definován jako **Řetězec**.</span><span class="sxs-lookup"><span data-stu-id="f9dfe-236">The data type of this parameter is defined as **String**.</span></span>

    <span data-ttu-id="f9dfe-237">Je-li název prvku vázaného formátu prázdný, bude název zdroje dat tohoto prvku použit v použité vazbě.</span><span class="sxs-lookup"><span data-stu-id="f9dfe-237">When the name of the bound format element is blank, the data source name of this element is used in applied binding.</span></span>

5. <span data-ttu-id="f9dfe-238">Vyberte prvek formátu **Statement.Taxation.Reduced**.</span><span class="sxs-lookup"><span data-stu-id="f9dfe-238">Select the **Statement.Taxation.Reduced** format element.</span></span>
6. <span data-ttu-id="f9dfe-239">Vyberte možnost **vazba**.</span><span class="sxs-lookup"><span data-stu-id="f9dfe-239">Select **Bind**.</span></span>
7. <span data-ttu-id="f9dfe-240">Vyberte možnost **Ano**, pokud chcete potvrdit nahrazení aktuálně používaného zdroje dat **Level2** novým zdrojem dat **Levels** ve všech vnořených formátovacích prvcích vybraného prvku formátu.</span><span class="sxs-lookup"><span data-stu-id="f9dfe-240">Select **Yes** to confirm the replacement of the currently used data source, **Level2**, by the new data source, **Levels**, in all nested format elements under the selected format element.</span></span>
8. <span data-ttu-id="f9dfe-241">Vyberte prvek formátu **Statement.Taxation.None**.</span><span class="sxs-lookup"><span data-stu-id="f9dfe-241">Select the **Statement.Taxation.None** format element.</span></span>
9. <span data-ttu-id="f9dfe-242">Vyberte možnost **vazba**.</span><span class="sxs-lookup"><span data-stu-id="f9dfe-242">Select **Bind**.</span></span>
10. <span data-ttu-id="f9dfe-243">Vyberte možnost **Ano**, pokud chcete potvrdit nahrazení aktuálně používaného zdroje dat **Level3** novým zdrojem dat **Levels** ve všech vnořených formátovacích prvcích vybraného prvku formátu.</span><span class="sxs-lookup"><span data-stu-id="f9dfe-243">Select **Yes** to confirm the replacement of the currently used data source, **Level3**, by the new data source, **Levels**, in all nested format elements under the selected format element.</span></span>

   <span data-ttu-id="f9dfe-244">Když zadáte argument parametrizovaného pole pro prvek XML představující úroveň zdanění (například **Model.Data2.Levels("Reduced")** jako textovou hodnotu), nemusíte provádět stejnou akci pro vnořené atributy XML – jejich vazby automaticky zdědí hodnotu argumentu definovaného na nadřazené úrovni (**Model.Data2.Levels.aggregated.Base**, nikoli **Model.Data2.Levels("Reduced").aggregated.Base**).</span><span class="sxs-lookup"><span data-stu-id="f9dfe-244">When you specify the argument of the parameterized calculated field for the XML element representing taxation level (for example, **Model.Data2.Levels("Reduced")** as a text value), you don’t need to do the same for nested XML attributes—their bindings will automatically inherit the value of the argument defined on the parent level (**Model.Data2.Levels.aggregated.Base**, not **Model.Data2.Levels("Reduced").aggregated.Base**).</span></span>

<span data-ttu-id="f9dfe-245">Opakující se volání jakéhokoliv parametrizovaného pole nejsou podporována.</span><span class="sxs-lookup"><span data-stu-id="f9dfe-245">Recurrent calls of any parameterized calculated field are not supported.</span></span>

<span data-ttu-id="f9dfe-246">Můžete vybrat možnost **Upravit vzorec** a změnit argument vyrovnáno podle výchozího pole ve vybrané vazbě.</span><span class="sxs-lookup"><span data-stu-id="f9dfe-246">You can select **Edit formula**, and change the applied-by-default argument of the parameterized calculated field in the selected binding.</span></span> <span data-ttu-id="f9dfe-247">Pokud tento argument chybí, může způsobit chyby za běhu – uživatelé jsou informováni o takové situaci, když je aktuální formát ověřen.</span><span class="sxs-lookup"><span data-stu-id="f9dfe-247">If this argument is missing, it can cause errors at run time — users are informed about such a situation when the current format is validated.</span></span>

![Upozornění na potvrzení ověření](media/er-calculated-field-type-10.png)

## <a name="configure-a-parameterized-calculated-field-to-return-a-record"></a><span data-ttu-id="f9dfe-249">Konfigurace parametrizovaného vypočítaného pole pro návrat záznamu</span><span class="sxs-lookup"><span data-stu-id="f9dfe-249">Configure a parameterized calculated field to return a record</span></span>
<span data-ttu-id="f9dfe-250">Pokud parametrizované pole vrací záznam, je nutné podporovat vazby jednotlivých polí tohoto záznamu k formátování prvků.</span><span class="sxs-lookup"><span data-stu-id="f9dfe-250">When a parameterized calculated field returns a record, you need to support binding of individual fields of this record to format elements.</span></span> <span data-ttu-id="f9dfe-251">V takovém případě nebude existovat žádná nadřazená vazba, která obsahuje hodnotu argumentu pro volání parametrizovaného počítaného pole - tato hodnota musí být definována ve vazbě pole jednoho záznamu.</span><span class="sxs-lookup"><span data-stu-id="f9dfe-251">In such cases there will be no parent binding that contains the value of an argument to call a parameterized calculated field — this value must be defined in the binding of a single record’s field.</span></span>

### <a name="start-adding-a-new-calculated-field"></a><span data-ttu-id="f9dfe-252">Začít přidávat nové počítané pole</span><span class="sxs-lookup"><span data-stu-id="f9dfe-252">Start adding a new calculated field</span></span>

1. <span data-ttu-id="f9dfe-253">Vyberte položku **Model.Data2**.</span><span class="sxs-lookup"><span data-stu-id="f9dfe-253">Select the **Model.Data2** item.</span></span>
2. <span data-ttu-id="f9dfe-254">Vyberte **přidat**.</span><span class="sxs-lookup"><span data-stu-id="f9dfe-254">Select **Add**.</span></span>
3. <span data-ttu-id="f9dfe-255">Vyberte **Funkce\\vypočítané pole**.</span><span class="sxs-lookup"><span data-stu-id="f9dfe-255">Select **Functions\\Calculated field**.</span></span>
4. <span data-ttu-id="f9dfe-256">Do pole **Název** zadejte **LevelRecord**.</span><span class="sxs-lookup"><span data-stu-id="f9dfe-256">In the **Name** field, enter **LevelRecord**.</span></span>
5. <span data-ttu-id="f9dfe-257">Vyberte možnost **Upravit vzorec**.</span><span class="sxs-lookup"><span data-stu-id="f9dfe-257">Select **Edit formula**.</span></span>

### <a name="define-a-parameter-for-adding-a-calculated-field"></a><span data-ttu-id="f9dfe-258">Definovat parametr pro přidání vypočítaného pole</span><span class="sxs-lookup"><span data-stu-id="f9dfe-258">Define a parameter for adding a calculated field</span></span>

1. <span data-ttu-id="f9dfe-259">Vyberte **Parametry**.</span><span class="sxs-lookup"><span data-stu-id="f9dfe-259">Select **Parameters**.</span></span>
2. <span data-ttu-id="f9dfe-260">Zvolte **Nové**.</span><span class="sxs-lookup"><span data-stu-id="f9dfe-260">Select **New**.</span></span>
3. <span data-ttu-id="f9dfe-261">Do pole **Název** zadejte **Úroveň zdanění**.</span><span class="sxs-lookup"><span data-stu-id="f9dfe-261">In the **Name** field, enter **Taxation Level**.</span></span>
4. <span data-ttu-id="f9dfe-262">V poli **Typ** vyberte **Řetězec**.</span><span class="sxs-lookup"><span data-stu-id="f9dfe-262">In the **Type** field, select **String**.</span></span>
5. <span data-ttu-id="f9dfe-263">Vyberte **OK**.</span><span class="sxs-lookup"><span data-stu-id="f9dfe-263">Select **OK**.</span></span>

### <a name="define-an-expression-for-adding-a-calculated-field"></a><span data-ttu-id="f9dfe-264">Definovat výraz pro přidání vypočítaného pole</span><span class="sxs-lookup"><span data-stu-id="f9dfe-264">Define an expression for adding a calculated field</span></span>

1. <span data-ttu-id="f9dfe-265">V poli **Vzorec** zadejte následující:</span><span class="sxs-lookup"><span data-stu-id="f9dfe-265">In the **Formula** field, enter the following:</span></span>  
    
    <span data-ttu-id="f9dfe-266">**FIRSTORNULL(\@.Levels(**</span><span class="sxs-lookup"><span data-stu-id="f9dfe-266">**FIRSTORNULL(\@.Levels(**</span></span>

2. <span data-ttu-id="f9dfe-267">Vyberte parametr **Úroveň zdanění**.</span><span class="sxs-lookup"><span data-stu-id="f9dfe-267">Select the **Taxation Level** parameter.</span></span>
3. <span data-ttu-id="f9dfe-268">Vyberte **Přidat zdroj dat**.</span><span class="sxs-lookup"><span data-stu-id="f9dfe-268">Select **Add data source**.</span></span>
4. <span data-ttu-id="f9dfe-269">V poli **Vzorec** přidejte **"Úroveň zdanění"))** do stavu, který jste zadali v kroku 1 a dokončete výraz na:</span><span class="sxs-lookup"><span data-stu-id="f9dfe-269">In the **Formula** field, append **'Taxation Level'))** to what you entered in Step 1 to finalize the expression to:</span></span>  
    
    <span data-ttu-id="f9dfe-270">**FIRSTORNULL(\@.Levels('Taxation Level'))**</span><span class="sxs-lookup"><span data-stu-id="f9dfe-270">**FIRSTORNULL(\@.Levels('Taxation Level'))**</span></span>

5. <span data-ttu-id="f9dfe-271">Zvolte **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="f9dfe-271">Select **Save**.</span></span>
6. <span data-ttu-id="f9dfe-272">Zavřete stránku **Návrhář vzorce**.</span><span class="sxs-lookup"><span data-stu-id="f9dfe-272">Close **the Formula designer** page.</span></span>

### <a name="finish-adding-a-new-calculated-field"></a><span data-ttu-id="f9dfe-273">Dokončete přidávávání nových počítaných polí</span><span class="sxs-lookup"><span data-stu-id="f9dfe-273">Finish adding a new calculated field</span></span>

-   <span data-ttu-id="f9dfe-274">Vyberte **OK**.</span><span class="sxs-lookup"><span data-stu-id="f9dfe-274">Select **OK**.</span></span>

### <a name="use-the-configured-calculated-field-to-bind-format-elements"></a><span data-ttu-id="f9dfe-275">Použít nakonfigurované počítané pole pro svázání prvků formátu</span><span class="sxs-lookup"><span data-stu-id="f9dfe-275">Use the configured calculated field to bind format elements</span></span>

1. <span data-ttu-id="f9dfe-276">Rozbalením **Model.Data2.LevelRecord** vyberte nakonfigurované počítané pole.</span><span class="sxs-lookup"><span data-stu-id="f9dfe-276">Expand **Model.Data2.LevelRecord** to select the configured calculated field.</span></span>
2. <span data-ttu-id="f9dfe-277">Rozbalte kontejner **Model.Data2.LevelRecord.aggregated** nakonfigurovaného počítaného pole.</span><span class="sxs-lookup"><span data-stu-id="f9dfe-277">Expand the **Model.Data2.LevelRecord.aggregated** container of the configured calculated field.</span></span>
3. <span data-ttu-id="f9dfe-278">Vyberte pole **Model.Data2.LevelRecord.aggregated.Base**.</span><span class="sxs-lookup"><span data-stu-id="f9dfe-278">Select the **Model.Data2.LevelRecord.aggregated.Base** field.</span></span>
4. <span data-ttu-id="f9dfe-279">Vyberte prvek formátu **Statement.Taxation.None**.</span><span class="sxs-lookup"><span data-stu-id="f9dfe-279">Select the **Statement.Taxation.None** format element.</span></span>
5. <span data-ttu-id="f9dfe-280">Vyberte možnost **Zrušit vazbu**.</span><span class="sxs-lookup"><span data-stu-id="f9dfe-280">Select **Unbind**.</span></span>
6. <span data-ttu-id="f9dfe-281">Vyberte prvek formátu **Statement.Taxation.None.Base**.</span><span class="sxs-lookup"><span data-stu-id="f9dfe-281">Select the **Statement.Taxation.None.Base** format element.</span></span>
7. <span data-ttu-id="f9dfe-282">Vyberte možnost **vazba**.</span><span class="sxs-lookup"><span data-stu-id="f9dfe-282">Select **Bind**.</span></span>
8. <span data-ttu-id="f9dfe-283">Vyberte možnost **Upravit vzorec**.</span><span class="sxs-lookup"><span data-stu-id="f9dfe-283">Select **Edit formula**.</span></span>
9. <span data-ttu-id="f9dfe-284">Změňte výraz na **Model.Data2.LevelRecord("None").aggregated.Base**.</span><span class="sxs-lookup"><span data-stu-id="f9dfe-284">Change the expression to **Model.Data2.LevelRecord("None").aggregated.Base**.</span></span>

![Aktualizovaný výraz](media/er-calculated-field-type-11.png)

## <a name="remove-calculated-fields-that-are-not-used"></a><span data-ttu-id="f9dfe-286">Odebrat vypočtená pole, která nejsou použita</span><span class="sxs-lookup"><span data-stu-id="f9dfe-286">Remove calculated fields that are not used</span></span>

1. <span data-ttu-id="f9dfe-287">Vyberte **Model.Data2.Level1**.</span><span class="sxs-lookup"><span data-stu-id="f9dfe-287">Select **Model.Data2.Level1**.</span></span>
2. <span data-ttu-id="f9dfe-288">Zvolte **Odstranit**.</span><span class="sxs-lookup"><span data-stu-id="f9dfe-288">Select **Delete**.</span></span>
3. <span data-ttu-id="f9dfe-289">Vyberte **Model.Data2.Level2**.</span><span class="sxs-lookup"><span data-stu-id="f9dfe-289">Select **Model.Data2.Level2**.</span></span>
4. <span data-ttu-id="f9dfe-290">Zvolte **Odstranit**.</span><span class="sxs-lookup"><span data-stu-id="f9dfe-290">Select **Delete**.</span></span>
5. <span data-ttu-id="f9dfe-291">Vyberte **Model.Data2.Level3**.</span><span class="sxs-lookup"><span data-stu-id="f9dfe-291">Select **Model.Data2.Level3**.</span></span>
6. <span data-ttu-id="f9dfe-292">Zvolte **Odstranit**.</span><span class="sxs-lookup"><span data-stu-id="f9dfe-292">Select **Delete**.</span></span>
7. <span data-ttu-id="f9dfe-293">Zvolte **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="f9dfe-293">Select **Save**.</span></span>

  > [!NOTE]
  > <span data-ttu-id="f9dfe-294">Znovu jste použili stejný model počítaného pole **Model.Data2.Levels** několikrát ve formátu vazeb.</span><span class="sxs-lookup"><span data-stu-id="f9dfe-294">You reused the same calculated field **Model.Data2.Levels** several times in format bindings.</span></span> <span data-ttu-id="f9dfe-295">Je mnohem jednodušší použít a udržovat jedno vypočítané pole namísto více podobných polí.</span><span class="sxs-lookup"><span data-stu-id="f9dfe-295">It is much easier to use and maintain a single calculated field instead of doing this for multiple similar fields.</span></span>

8. <span data-ttu-id="f9dfe-296">Zavřete stránku **Návrhář formátu**.</span><span class="sxs-lookup"><span data-stu-id="f9dfe-296">Close the **Format designer** page.</span></span>

## <a name="complete-adjusted-version-of-a-derived-format"></a><span data-ttu-id="f9dfe-297">Dokončete upravenou verzi odvozeného formátu</span><span class="sxs-lookup"><span data-stu-id="f9dfe-297">Complete adjusted version of a derived format</span></span>

1. <span data-ttu-id="f9dfe-298">Na pevné záložce **Verze** vyberte možnost **Stav změny**.</span><span class="sxs-lookup"><span data-stu-id="f9dfe-298">In the **Versions** FastTab, select **Change status**.</span></span>
2. <span data-ttu-id="f9dfe-299">Zvolte **Dokončit**.</span><span class="sxs-lookup"><span data-stu-id="f9dfe-299">Select **Complete**.</span></span>

## <a name="export-completed-version-of-a-derived-format"></a><span data-ttu-id="f9dfe-300">Exportujte dokončenou verzi odvozeného formátu</span><span class="sxs-lookup"><span data-stu-id="f9dfe-300">Export completed version of a derived format</span></span>

1. <span data-ttu-id="f9dfe-301">Vyberte **Formát pro učení parametrizovaných volání (vlastní)** ve stromu konfigurací.</span><span class="sxs-lookup"><span data-stu-id="f9dfe-301">Select **Format to learn parameterized calls (custom)** format in the configurations tree.</span></span>
2. <span data-ttu-id="f9dfe-302">Na pevné záložce **Verze** vyberte dokončenou verzi 1.1.1.</span><span class="sxs-lookup"><span data-stu-id="f9dfe-302">In the **Versions** FastTab, select the completed version 1.1.1.</span></span>
3. <span data-ttu-id="f9dfe-303">Vyberte **Exchange**.</span><span class="sxs-lookup"><span data-stu-id="f9dfe-303">Select **Exchange**.</span></span>
4. <span data-ttu-id="f9dfe-304">Vyberte **Exportovat jako soubor XML**.</span><span class="sxs-lookup"><span data-stu-id="f9dfe-304">Select **Export as XML file**.</span></span>
5. <span data-ttu-id="f9dfe-305">Uloží staženou konfiguraci místně ve formátu XML.</span><span class="sxs-lookup"><span data-stu-id="f9dfe-305">Store the downloaded configuration locally, in XML format.</span></span>

## <a name="test-er-formats"></a><span data-ttu-id="f9dfe-306">Testovat formáty ER</span><span class="sxs-lookup"><span data-stu-id="f9dfe-306">Test ER formats</span></span> 
<span data-ttu-id="f9dfe-307">Chcete-li se ujistit, že nakonfigurovaná počítaná pole fungují správně, můžete spustit počáteční a vylepšené formáty ER.</span><span class="sxs-lookup"><span data-stu-id="f9dfe-307">You can run the initial and improved ER formats to make sure that configured parameterized calculated fields work properly.</span></span>

### <a name="import-er-configurations"></a><span data-ttu-id="f9dfe-308">Import konfigurací ER</span><span class="sxs-lookup"><span data-stu-id="f9dfe-308">Import ER configurations</span></span>
<span data-ttu-id="f9dfe-309">Revidované konfigurace lze importovat z RCS pomocí úložiště ER typu **RCS**.</span><span class="sxs-lookup"><span data-stu-id="f9dfe-309">You can import reviewed configurations from RCS by using the ER repository of the **RCS** type.</span></span> <span data-ttu-id="f9dfe-310">Pokud jste již provedli kroky v tématu, [Import konfigurací elektronického výkaznictví (ER) z Regulatory Configuration Services (RCS)](rcs-download-configurations.md), použijte nakonfigurované úložiště ER pro import konfigurací popsaných dříve v tomto tématu do vašeho prostředí.</span><span class="sxs-lookup"><span data-stu-id="f9dfe-310">If you already went through the steps in the topic, [Import Electronic reporting (ER) configurations from Regulatory Configuration Services (RCS)](rcs-download-configurations.md), use the configured ER repository to import configurations discussed earlier in this topic to your environment.</span></span> <span data-ttu-id="f9dfe-311">V opačném případě postupujte takto:</span><span class="sxs-lookup"><span data-stu-id="f9dfe-311">Otherwise, follow these steps:</span></span>

1. <span data-ttu-id="f9dfe-312">Vyberte společnost **DEMF** a na výchozím řídicím panelu vyberte možnost **Elektronické vykazování**.</span><span class="sxs-lookup"><span data-stu-id="f9dfe-312">Select the **DEMF** company and on the default dashboard, select **Electronic reporting**.</span></span>
2. <span data-ttu-id="f9dfe-313">Vyberte **Konfigurace vykazování**.</span><span class="sxs-lookup"><span data-stu-id="f9dfe-313">Select **Reporting configurations**.</span></span>
3. <span data-ttu-id="f9dfe-314">Import stažených konfigurací z Microsoft Download Center v následujícím pořadí: datový model, mapování modelu, formát.</span><span class="sxs-lookup"><span data-stu-id="f9dfe-314">Import the configurations from Microsoft Download Center in the following sequence: data model, model mapping, format.</span></span> <span data-ttu-id="f9dfe-315">Pro každou konfiguraci ER proveďte následující kroky:</span><span class="sxs-lookup"><span data-stu-id="f9dfe-315">Complete the following steps for each ER configuration:</span></span>

    1. <span data-ttu-id="f9dfe-316">Vyberte **Exchange**.</span><span class="sxs-lookup"><span data-stu-id="f9dfe-316">Select **Exchange.**</span></span>
    2. <span data-ttu-id="f9dfe-317">Vyberte **Načíst ze souboru XML**.</span><span class="sxs-lookup"><span data-stu-id="f9dfe-317">Select **Load from XML file**.</span></span>
    3. <span data-ttu-id="f9dfe-318">Zvolte **Procházet** a vyberte požadovanou konfiguraci elektronického výkaznictví ve formátu XML.</span><span class="sxs-lookup"><span data-stu-id="f9dfe-318">Select **Browse** to select the required ER configuration in XML format.</span></span>
    4. <span data-ttu-id="f9dfe-319">Vyberte **OK**.</span><span class="sxs-lookup"><span data-stu-id="f9dfe-319">Select **OK**.</span></span>

4. <span data-ttu-id="f9dfe-320">Importujte exportované z RCS dokončené verze 1.1.1 **Formát pro učení parametrizovaných volání (vlastní)**:</span><span class="sxs-lookup"><span data-stu-id="f9dfe-320">Import the exported from RCS completed version 1.1.1 of the **Format to learn parameterized calls (custom)** format:</span></span>

    1. <span data-ttu-id="f9dfe-321">Vyberte **Exchange**.</span><span class="sxs-lookup"><span data-stu-id="f9dfe-321">Select **Exchange.**</span></span>
    2. <span data-ttu-id="f9dfe-322">Vyberte **Načíst ze souboru XML**.</span><span class="sxs-lookup"><span data-stu-id="f9dfe-322">Select **Load from XML file**.</span></span>
    3. <span data-ttu-id="f9dfe-323">Vyberte **Procházet** a vyberte místně uložený soubor **Formát pro učení parametrizovaných volání (vlastní)** ve formátu XML.</span><span class="sxs-lookup"><span data-stu-id="f9dfe-323">Select **Browse** to select the locally stored **Format to learn parameterized calls (custom)** file in XML format.</span></span>
    4. <span data-ttu-id="f9dfe-324">Vyberte **OK**.</span><span class="sxs-lookup"><span data-stu-id="f9dfe-324">Select **OK**.</span></span>

### <a name="run-er-formats"></a><span data-ttu-id="f9dfe-325">Spustit formáty ER</span><span class="sxs-lookup"><span data-stu-id="f9dfe-325">Run ER formats</span></span>

1. <span data-ttu-id="f9dfe-326">Ve stromu konfigurace rozbalte obsah položky **Model pro seznámení s parametrizovanými voláními**.</span><span class="sxs-lookup"><span data-stu-id="f9dfe-326">In the configuration tree, expand the content of the **Model to learn parameterized calls** item.</span></span>
2. <span data-ttu-id="f9dfe-327">Vyberte **Formát pro informace o voláních s parametry**.</span><span class="sxs-lookup"><span data-stu-id="f9dfe-327">Select **Format to learn parameterized calls**.</span></span>
3. <span data-ttu-id="f9dfe-328">Vyberte **Spustit** na horním pásu.</span><span class="sxs-lookup"><span data-stu-id="f9dfe-328">Select **Run** on the top-most ribbon.</span></span>
4. <span data-ttu-id="f9dfe-329">Uložte místně generovaný výstup.</span><span class="sxs-lookup"><span data-stu-id="f9dfe-329">Save the locally generated output.</span></span>
5. <span data-ttu-id="f9dfe-330">Vyberte položku **Formát pro učení parametrizovaných volání (vlastní)**.</span><span class="sxs-lookup"><span data-stu-id="f9dfe-330">Select the **Format to learn parameterized calls (custom)** item.</span></span>
6. <span data-ttu-id="f9dfe-331">Vyberte **Spustit** na horním pásu.</span><span class="sxs-lookup"><span data-stu-id="f9dfe-331">Select **Run** on the top-most ribbon.</span></span>
7. <span data-ttu-id="f9dfe-332">Uložte generovaný výstup místně.</span><span class="sxs-lookup"><span data-stu-id="f9dfe-332">Save the generated output locally.</span></span> 
8. <span data-ttu-id="f9dfe-333">Porovnejte obsah generovaných výstupů.</span><span class="sxs-lookup"><span data-stu-id="f9dfe-333">Compare the contents of the generated outputs.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="f9dfe-334">Další prostředky</span><span class="sxs-lookup"><span data-stu-id="f9dfe-334">Additional resources</span></span>

- [<span data-ttu-id="f9dfe-335">Návrhář receptur v elektronickém výkaznictví</span><span class="sxs-lookup"><span data-stu-id="f9dfe-335">Formula designer in Electronic reporting (ER)</span></span>](general-electronic-reporting-formula-designer.md)
- [<span data-ttu-id="f9dfe-336">Zlepšete výkon řešení elektronického výkaznictví přidáním parametrizovaných zdrojů dat typu POČÍTANÉ POLE</span><span class="sxs-lookup"><span data-stu-id="f9dfe-336">Improve performance of ER solutions by adding parameterized CALCULATED FIELD data sources</span></span>](er-calculated-field-ds-performance.md)

