---
title: Podpora parametrizovaných volání zdrojů dat ER typu vypočítaného pole
description: Toto téma obsahuje informace o způsobu použití typu vypočítaného pole pro zdroje dat ER.
author: NickSelin
manager: AnnBe
ms.date: 09/09/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: ''
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 20d48795b23628bbba2896bf48940936a25e0435
ms.sourcegitcommit: 75db3b75d35d27034f9b56e7119c9d0cb7666830
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/03/2019
ms.locfileid: "2550077"
---
# <a name="support-parameterized-calls-of-er-data-sources-of-the-calculated-field-type"></a><span data-ttu-id="42ee5-103">Podpora parametrizovaných volání zdrojů dat ER typu vypočítaného pole</span><span class="sxs-lookup"><span data-stu-id="42ee5-103">Support parameterized calls of ER data sources of the Calculated field type</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="42ee5-104">V tomto tématu je vysvětleno, jak můžete vytvořit zdroj dat Elektronického vykazování (ER) pomocí typu **Vypočítaného pole**.</span><span class="sxs-lookup"><span data-stu-id="42ee5-104">This topic explains how you can design an Electronic reporting (ER) data source by using the **Calculated field** type.</span></span> <span data-ttu-id="42ee5-105">Tento zdroj dat může obsahovat výraz ER, který po spuštění může být řízen hodnotami argumentů parametrů, které jsou nakonfigurovány ve vazbě, která volá tento zdroj dat.</span><span class="sxs-lookup"><span data-stu-id="42ee5-105">This data source may contain an ER expression that, when executed, can be controlled by the values of the parameter arguments that are configured in a binding that calls this data source.</span></span> <span data-ttu-id="42ee5-106">Konfigurací parametrizovaných volání takového zdroje dat můžete znovu použít jeden zdroj dat v mnoha vazbách, čímž snížíte celkový počet datových zdrojů, které musí být nakonfigurovány v mapování modelu ER nebo ve formátech ER.</span><span class="sxs-lookup"><span data-stu-id="42ee5-106">By configuring parameterized calls of such a data source, you can reuse a single data source in many bindings, which reduces the total number of data sources that must be configured in ER model mappings or ER formats.</span></span> <span data-ttu-id="42ee5-107">Také zjednodušuje konfigurovanou komponentu ER, která snižuje náklady na údržbu a náklady na použití ostatních odběratelů.</span><span class="sxs-lookup"><span data-stu-id="42ee5-107">It also simplifies the configured ER component, which reduces the maintenance costs and the cost of use by other consumers.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="42ee5-108">Předpoklady</span><span class="sxs-lookup"><span data-stu-id="42ee5-108">Prerequisites</span></span>
<span data-ttu-id="42ee5-109">Pro dokončení příkladů v tomto tématu musíte mít následující přístup:</span><span class="sxs-lookup"><span data-stu-id="42ee5-109">To complete the examples in this topic, you must have the following access:</span></span>

- <span data-ttu-id="42ee5-110">Přístup k jedné z těchto rolí:</span><span class="sxs-lookup"><span data-stu-id="42ee5-110">Access to one of these roles:</span></span>

    - <span data-ttu-id="42ee5-111">Návrhář elektronického výkaznictví</span><span class="sxs-lookup"><span data-stu-id="42ee5-111">Electronic reporting developer</span></span>
    - <span data-ttu-id="42ee5-112">Funkční konzultant elektronického výkaznictví</span><span class="sxs-lookup"><span data-stu-id="42ee5-112">Electronic reporting functional consultant</span></span>
    - <span data-ttu-id="42ee5-113">Správce systému</span><span class="sxs-lookup"><span data-stu-id="42ee5-113">System administrator</span></span>

- <span data-ttu-id="42ee5-114">Přístup k službám Regulatory Configuration Services (RCS), které byly zřízeny pro stejného klienta jako Finance and Operations, pro jednu z následujících rolí:</span><span class="sxs-lookup"><span data-stu-id="42ee5-114">Access to Regulatory Configuration Services (RCS) that have been provisioned for the same tenant as Finance and Operations for one of the following roles:</span></span>

    - <span data-ttu-id="42ee5-115">Návrhář elektronického výkaznictví</span><span class="sxs-lookup"><span data-stu-id="42ee5-115">Electronic reporting developer</span></span>
    - <span data-ttu-id="42ee5-116">Funkční konzultant elektronického výkaznictví</span><span class="sxs-lookup"><span data-stu-id="42ee5-116">Electronic reporting functional consultant</span></span>
    - <span data-ttu-id="42ee5-117">Správce systému</span><span class="sxs-lookup"><span data-stu-id="42ee5-117">System administrator</span></span>

<span data-ttu-id="42ee5-118">Z [Microsoft Download Center](https://go.microsoft.com/fwlink/?linkid=874684) stáhněte soubor zip (komprimovaný) **Podpora parametrizovaných volání zdrojů dat ER typu vypočítaného pole**.</span><span class="sxs-lookup"><span data-stu-id="42ee5-118">From the [Microsoft Download Center](https://go.microsoft.com/fwlink/?linkid=874684), download the zipped (compressed) file **Support parameterized calls of ER data sources of Calculated field type**.</span></span> <span data-ttu-id="42ee5-119">Obsahuje následující konfigurace ER, které je nutné extrahovat a uložit místně.</span><span class="sxs-lookup"><span data-stu-id="42ee5-119">It contains the following ER configurations that must be extracted and stored locally.</span></span>

| <span data-ttu-id="42ee5-120">**Obsah**</span><span class="sxs-lookup"><span data-stu-id="42ee5-120">**Content**</span></span>                           | <span data-ttu-id="42ee5-121">**Název souboru**</span><span class="sxs-lookup"><span data-stu-id="42ee5-121">**File name**</span></span>                                        |
|---------------------------------------|------------------------------------------------------|
| <span data-ttu-id="42ee5-122">Vzorová konfigurace datového modelu elektronického výkaznictví</span><span class="sxs-lookup"><span data-stu-id="42ee5-122">Sample ER data model configuration</span></span>    | <span data-ttu-id="42ee5-123">Model pro informace o volání s parametry calls.version.1.xml</span><span class="sxs-lookup"><span data-stu-id="42ee5-123">Model to learn parameterized calls.version.1.xml</span></span>     |
| <span data-ttu-id="42ee5-124">Vzorová konfigurace metadat elektronického výkaznictví</span><span class="sxs-lookup"><span data-stu-id="42ee5-124">Sample ER metadata configuration</span></span>      | <span data-ttu-id="42ee5-125">Metadata pro informace o volání s parametry calls.version.1.xml</span><span class="sxs-lookup"><span data-stu-id="42ee5-125">Metadata to learn parameterized calls.version.1.xml</span></span>  |
| <span data-ttu-id="42ee5-126">Vzorová konfigurace mapování elektronického výkaznictví</span><span class="sxs-lookup"><span data-stu-id="42ee5-126">Sample ER model mapping configuration</span></span> | <span data-ttu-id="42ee5-127">Mapování pro informace o volání s parametry calls.version.1.1.xml</span><span class="sxs-lookup"><span data-stu-id="42ee5-127">Mapping to learn parameterized calls.version.1.1.xml</span></span> |
| <span data-ttu-id="42ee5-128">Vzorová konfigurace formátu elektronického výkaznictví</span><span class="sxs-lookup"><span data-stu-id="42ee5-128">Sample ER format configuration</span></span>        | <span data-ttu-id="42ee5-129">Formát pro informace o volání s parametry calls.version.1.1.xml</span><span class="sxs-lookup"><span data-stu-id="42ee5-129">Format to learn parameterized calls.version.1.1.xml</span></span>  |

## <a name="sign-in-to-your-rcs-instance"></a><span data-ttu-id="42ee5-130">Přihlaste se k instanci RCS.</span><span class="sxs-lookup"><span data-stu-id="42ee5-130">Sign in to your RCS instance</span></span>
<span data-ttu-id="42ee5-131">V tomto příkladu vytvoříte konfiguraci pro vzorovou společnost Litware, Inc. Nejprve musíte v RCS dokončit krok v proceduře [Vytvoření poskytovatele konfigurace a jeho označení jako aktivního](tasks/er-configuration-provider-mark-it-active-2016-11.md).</span><span class="sxs-lookup"><span data-stu-id="42ee5-131">In this example, you will create a configuration for the sample company, Litware, Inc. First, in RCS, you must complete the steps in the [Create a configuration provider and mark it as active](tasks/er-configuration-provider-mark-it-active-2016-11.md) procedure:</span></span>

1. <span data-ttu-id="42ee5-132">Na výchozím řídicím panelu vyberte **Elektronické vykazování**.</span><span class="sxs-lookup"><span data-stu-id="42ee5-132">On the default dashboard, select **Electronic reporting**.</span></span>
2. <span data-ttu-id="42ee5-133">Vyberte **Konfigurace vykazování**.</span><span class="sxs-lookup"><span data-stu-id="42ee5-133">Select **Reporting configurations**.</span></span>
3. <span data-ttu-id="42ee5-134">Import stažených konfigurací do RCS v následujícím pořadí: datový model, metadata, mapování modelu, formát.</span><span class="sxs-lookup"><span data-stu-id="42ee5-134">Import the downloaded configurations to RCS in the following sequence: data model, metadata, model mapping, format.</span></span> <span data-ttu-id="42ee5-135">Pro každou konfiguraci ER proveďte následující kroky:</span><span class="sxs-lookup"><span data-stu-id="42ee5-135">Complete the following steps for each ER configuration:</span></span>

    1. <span data-ttu-id="42ee5-136">Vyberte **Exchange**.</span><span class="sxs-lookup"><span data-stu-id="42ee5-136">Select **Exchange.**</span></span>
    2. <span data-ttu-id="42ee5-137">Vyberte **Načíst ze souboru XML**.</span><span class="sxs-lookup"><span data-stu-id="42ee5-137">Select **Load from XML file**.</span></span>
    3. <span data-ttu-id="42ee5-138">Zvolte **Procházet** a pak vyberte požadovanou konfiguraci elektronického výkaznictví ve formátu XML.</span><span class="sxs-lookup"><span data-stu-id="42ee5-138">Select **Browse**, and then select the required ER configuration in XML format.</span></span>
    4. <span data-ttu-id="42ee5-139">Vyberte **OK**.</span><span class="sxs-lookup"><span data-stu-id="42ee5-139">Select **OK.**</span></span>

## <a name="review-the-provided-er-solution"></a><span data-ttu-id="42ee5-140">Zkontrolovat poskytnuté řešení ER</span><span class="sxs-lookup"><span data-stu-id="42ee5-140">Review the provided ER solution</span></span>

### <a name="review-model-mapping"></a><span data-ttu-id="42ee5-141">Kontrola mapování modelu</span><span class="sxs-lookup"><span data-stu-id="42ee5-141">Review model mapping</span></span>

1. <span data-ttu-id="42ee5-142">Ve stromu konfigurace rozbalte obsah položky **Model pro seznámení s parametrizovanými voláními**.</span><span class="sxs-lookup"><span data-stu-id="42ee5-142">In the configuration tree, expand the content of the **Model to learn parameterized calls** item.</span></span>
2. <span data-ttu-id="42ee5-143">Vyberte **Mapování pro informace o voláních s parametry**.</span><span class="sxs-lookup"><span data-stu-id="42ee5-143">Select **Mapping to learn parameterized calls**.</span></span>
3. <span data-ttu-id="42ee5-144">Vyberte možnost **Návrhář**.</span><span class="sxs-lookup"><span data-stu-id="42ee5-144">Select **Designer**.</span></span>
4. <span data-ttu-id="42ee5-145">Vyberte možnost **Návrhář**.</span><span class="sxs-lookup"><span data-stu-id="42ee5-145">Select **Designer**.</span></span>  
   
<span data-ttu-id="42ee5-146">Toto mapování modelu ER je navrženo k následujícím akcím:</span><span class="sxs-lookup"><span data-stu-id="42ee5-146">This ER model mapping is designed to do the following:</span></span>

- <span data-ttu-id="42ee5-147">Načtení seznamu daňových kódů (**Daňový** zdroj dat) nacházející se v tabulce **TaxTable**.</span><span class="sxs-lookup"><span data-stu-id="42ee5-147">Fetch the list of tax codes (**Tax** data source) residing in the   **TaxTable** table.</span></span>
- <span data-ttu-id="42ee5-148">Načtení seznamu daňových transakcí (**Trans** zdroj dat) nacházející se v tabulce **TaxTrans**:</span><span class="sxs-lookup"><span data-stu-id="42ee5-148">Fetch the list of tax transactions (**Trans** data source) residing in the   **TaxTrans** table:</span></span>
    
    - <span data-ttu-id="42ee5-149">Seskupit seznam načtených transakcí (**Gr** zdroj dat) podle kódu daně</span><span class="sxs-lookup"><span data-stu-id="42ee5-149">Group the list of fetched transactions (**Gr** data source) by tax code.</span></span>
    - <span data-ttu-id="42ee5-150">Vypočítat pro seskupené transakce po agregovaných hodnotách podle kódu daně:</span><span class="sxs-lookup"><span data-stu-id="42ee5-150">Calculate for grouped transactions following aggregated values per   tax code:</span></span>

        - <span data-ttu-id="42ee5-151">Součet hodnot základu daně.</span><span class="sxs-lookup"><span data-stu-id="42ee5-151">Sum of tax base values.</span></span>
        - <span data-ttu-id="42ee5-152">Součet hodnot daně.</span><span class="sxs-lookup"><span data-stu-id="42ee5-152">Sum of tax values.</span></span>
        - <span data-ttu-id="42ee5-153">Minimální hodnota uplatněné sazby daně.</span><span class="sxs-lookup"><span data-stu-id="42ee5-153">Minimum value of applied tax rate.</span></span>

<span data-ttu-id="42ee5-154">Mapování modelu v této konfiguraci implementuje základní datový model pro všechny formáty ER vytvořené pro tento model a prováděné ve Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="42ee5-154">The model mapping in this configuration implements the base data model for any of the ER formats created for this model and executed in Finance and Operations.</span></span> <span data-ttu-id="42ee5-155">V důsledku toho je obsah zdrojů dat **Daň** a **Gr** vystaven pro formáty ER, jako jsou například abstraktní zdroje dat.</span><span class="sxs-lookup"><span data-stu-id="42ee5-155">As a result, the content of the **Tax** and **Gr** data sources is exposed for ER formats such as abstract data sources.</span></span>

  ![Stránka Návrhář mapování modelu zobrazující zdroje dat Daň a Gr](media/er-calculated-field-type-01.png)

5.  <span data-ttu-id="42ee5-157">Zavřete stránku **Návrhář mapování modelu**.</span><span class="sxs-lookup"><span data-stu-id="42ee5-157">Close the **Model mapping designer** page.</span></span>
6.  <span data-ttu-id="42ee5-158">Zavřete stránku **Mapování modelu**.</span><span class="sxs-lookup"><span data-stu-id="42ee5-158">Close the **Model mapping** page.</span></span>

### <a name="review-format"></a><span data-ttu-id="42ee5-159">Zkontrolovat formát</span><span class="sxs-lookup"><span data-stu-id="42ee5-159">Review format</span></span>

1. <span data-ttu-id="42ee5-160">Ve stromu konfigurace rozbalte obsah položky **Model pro seznámení s parametrizovanými voláními**.</span><span class="sxs-lookup"><span data-stu-id="42ee5-160">In the configuration tree, expand the content of the **Model to learn parameterized calls** item.</span></span>
2. <span data-ttu-id="42ee5-161">Vyberte **Formát pro informace o voláních s parametry**.</span><span class="sxs-lookup"><span data-stu-id="42ee5-161">Select **Format to learn parameterized calls**.</span></span>
3. <span data-ttu-id="42ee5-162">Vyberte možnost **Návrhář**.</span><span class="sxs-lookup"><span data-stu-id="42ee5-162">Select **Designer**.</span></span> <span data-ttu-id="42ee5-163">Tento formát ER je navržen k následujícím akcím:</span><span class="sxs-lookup"><span data-stu-id="42ee5-163">This ER format is designed to do the following:</span></span>

  - <span data-ttu-id="42ee5-164">Generujte daňový výkaz ve formátu XML.</span><span class="sxs-lookup"><span data-stu-id="42ee5-164">Generate a tax statement in XML format.</span></span>
  - <span data-ttu-id="42ee5-165">V daňovém výkazu prezentujte následující úrovně zdanění: normální, snížené a žádné.</span><span class="sxs-lookup"><span data-stu-id="42ee5-165">Present the following levels of taxation in the tax statement: regular, reduced, and none.</span></span>
  - <span data-ttu-id="42ee5-166">Prezentujte více podrobností na každé úrovni zdanění, které mají různý počet podrobností na každé úrovni.</span><span class="sxs-lookup"><span data-stu-id="42ee5-166">Present multiple details at each taxation level, having a different number of details in each level.</span></span>

  ![Stránka návrháře formátu](media/er-calculated-field-type-02.png)

4. <span data-ttu-id="42ee5-168">Vyberte **Mapování**.</span><span class="sxs-lookup"><span data-stu-id="42ee5-168">Select **Mapping**.</span></span>
5. <span data-ttu-id="42ee5-169">Rozbaltepoložky **Model**, **Data** a **Souhrnné** .</span><span class="sxs-lookup"><span data-stu-id="42ee5-169">Expand the **Model**, **Data,** and **Summary** items.</span></span> 

   <span data-ttu-id="42ee5-170">Vpočítané pole **Model.Data.Summary.Leve** obsahuje výraz vracející kód úrovně zdanění (**Pravidelný**, **Snížený**, **Žádný** nebo **Jiný**) jako textovou hodnotu pro libovolný kód daně, který lze načíst ze zdroje dat **Model.Data.Summary** za běhu.</span><span class="sxs-lookup"><span data-stu-id="42ee5-170">The calculated field **Model.Data.Summary.Level** contains the expression that returns the code of the taxation level (**Regular**, **Reduced**, **None,** or **Other**) as a text value for any tax code that can be retrieved from the **Model.Data.Summary** data source at run time.</span></span>

  ![Stránka návrháře formátu s podrobnostmi o modelu datového modelu pro zjištění parametrizovaných hovorů](media/er-calculated-field-type-03.png)

6. <span data-ttu-id="42ee5-172">Rozbalte položku **Model**.**Data2**.</span><span class="sxs-lookup"><span data-stu-id="42ee5-172">Expand the **Model**.**Data2** item.</span></span>
7. <span data-ttu-id="42ee5-173">Rozbalte položku **Model**.**Data2.Summary2**.</span><span class="sxs-lookup"><span data-stu-id="42ee5-173">Expand the **Model**.**Data2.Summary2** item.</span></span>
   
   <span data-ttu-id="42ee5-174">Datový zdroj **Model**.**Data2.Summary2** je konfigurováno pro seskupení podrobností transakcí datového zdroje **Model.Data.Summary** podle úrovně zdanění (vráceno vypočítaným polem **Model.Data.Summary.Level**) a výpočet agregací.</span><span class="sxs-lookup"><span data-stu-id="42ee5-174">The **Model**.**Data2.Summary2** data source is configured to group the **Model.Data.Summary** data source transaction details by taxation level (returned by the **Model.Data.Summary.Level** calculated field) and compute the aggregations.</span></span>

  ![Stránka návrháře formátu s podrobnostmi o zdroji dat Model.Data2.Summary2](media/er-calculated-field-type-04.png)

8. <span data-ttu-id="42ee5-176">Zkontrolujte vypočítaná pole **Model**.**Data2.Level1**, **Model**.**Data2.Level2** a **Model**.**Data2.Level3.**</span><span class="sxs-lookup"><span data-stu-id="42ee5-176">Review the calculated fields **Model**.**Data2.Level1**, **Model**.**Data2.Level2**, and **Model**.**Data2.Level3.**</span></span> <span data-ttu-id="42ee5-177">Tato vypočítaná pole slouží k filtrování seznamu záznamů **Model**.**Data2.Summary2** a vrátí pouze záznamy, které reprezentují určitou úroveň zdanění.</span><span class="sxs-lookup"><span data-stu-id="42ee5-177">These calculated fields are used to filter the **Model**.**Data2.Summary2** records list and return only records that represent a particular taxation level.</span></span>
9. <span data-ttu-id="42ee5-178">Zavřete stránku **Návrhář formátu**.</span><span class="sxs-lookup"><span data-stu-id="42ee5-178">Close the **Format designer** page.</span></span>

## <a name="create-a-derived-format"></a><span data-ttu-id="42ee5-179">Vytvoření odvozeného formátu</span><span class="sxs-lookup"><span data-stu-id="42ee5-179">Create a derived format</span></span>
<span data-ttu-id="42ee5-180">Poskytnutý formát lze zlepšit přidáním jednoho vypočítaného pole pro filtrování požadované úrovně zdanění namísto použití existujících tří polí: **Model**.**Data2.Level1**, **Model**.**Data2.Level2** a **Model**.**Data2.Level3**.</span><span class="sxs-lookup"><span data-stu-id="42ee5-180">You can improve the provided format by adding one calculated field to filter the required taxation level instead of using the existing three fields: **Model**.**Data2.Level1**, **Model**.**Data2.Level2,** and **Model**.**Data2.Level3**.</span></span> <span data-ttu-id="42ee5-181">Požadovanou úroveň zdanění lze zadat v místě, kde bude voláno nové vypočtené pole.</span><span class="sxs-lookup"><span data-stu-id="42ee5-181">The required taxation level can be specified in the location where this new calculated field will be called.</span></span>

1. <span data-ttu-id="42ee5-182">Ve stromu konfigurace rozbalte obsah položky **Model pro seznámení s parametrizovanými voláními**.</span><span class="sxs-lookup"><span data-stu-id="42ee5-182">In the configuration tree, expand the content of the **Model to learn parameterized calls** item.</span></span>
2. <span data-ttu-id="42ee5-183">Vyberte **Formát pro informace o voláních s parametry**.</span><span class="sxs-lookup"><span data-stu-id="42ee5-183">Select **Format to learn parameterized calls**.</span></span>
3. <span data-ttu-id="42ee5-184">Vyberte **Vytvořit konfiguraci**.</span><span class="sxs-lookup"><span data-stu-id="42ee5-184">Select **Create configuration**.</span></span>
4. <span data-ttu-id="42ee5-185">Vyberte možnost **Odvozeno od názvu: Formát pro informace o parametrizovaných volání, Microsoft**.</span><span class="sxs-lookup"><span data-stu-id="42ee5-185">Select **Derive from Name: Format to learn parameterized calls, Microsoft**.</span></span>
5. <span data-ttu-id="42ee5-186">Do pole **Název** zadejte **Formát pro učení parametrizovaných volání (vlastní)**.</span><span class="sxs-lookup"><span data-stu-id="42ee5-186">In the **Name** field, enter **Format to learn parameterized calls (custom)**.</span></span>
6. <span data-ttu-id="42ee5-187">Vyberte **Vytvořit konfiguraci**.</span><span class="sxs-lookup"><span data-stu-id="42ee5-187">Select **Create configuration.**</span></span>

## <a name="configure-a-parameterized-calculated-field-that-returns-a-list-of-records"></a><span data-ttu-id="42ee5-188">Konfigurace parametrizovaného vypočítaného pole, které vrací seznam záznamů</span><span class="sxs-lookup"><span data-stu-id="42ee5-188">Configure a parameterized calculated field that returns a list of records</span></span>

### <a name="start-adding-a-new-calculated-field"></a><span data-ttu-id="42ee5-189">Začít přidávat nové počítané pole</span><span class="sxs-lookup"><span data-stu-id="42ee5-189">Start adding a new calculated field</span></span>

1. <span data-ttu-id="42ee5-190">Vyberte možnost **Návrhář**.</span><span class="sxs-lookup"><span data-stu-id="42ee5-190">Select **Designer**.</span></span>
2. <span data-ttu-id="42ee5-191">Vyberte **Rozbalit/sbalit** pro rozbalení všechn položek formátu.</span><span class="sxs-lookup"><span data-stu-id="42ee5-191">Select **Expand/collapse** to expand all format items.</span></span>
3. <span data-ttu-id="42ee5-192">Vyberte **Mapování**.</span><span class="sxs-lookup"><span data-stu-id="42ee5-192">Select **Mapping**.</span></span>
4. <span data-ttu-id="42ee5-193">Rozbalte položku **Model**.</span><span class="sxs-lookup"><span data-stu-id="42ee5-193">Expand the **Model** item.</span></span>
5. <span data-ttu-id="42ee5-194">Vyberte položku **Model.Data2**.</span><span class="sxs-lookup"><span data-stu-id="42ee5-194">Select the **Model.Data2** item.</span></span>
6. <span data-ttu-id="42ee5-195">Vyberte **přidat**.</span><span class="sxs-lookup"><span data-stu-id="42ee5-195">Select **Add**.</span></span>
7. <span data-ttu-id="42ee5-196">Vyberte **Funkce\\vypočítané pole**.</span><span class="sxs-lookup"><span data-stu-id="42ee5-196">Select **Functions\\Calculated field**.</span></span>
8. <span data-ttu-id="42ee5-197">Do pole **Název** zadejte **Úrovně**.</span><span class="sxs-lookup"><span data-stu-id="42ee5-197">In the **Name** field, enter **Levels**.</span></span>
9. <span data-ttu-id="42ee5-198">Vyberte možnost **Upravit vzorec**.</span><span class="sxs-lookup"><span data-stu-id="42ee5-198">Select **Edit formula**.</span></span>

### <a name="define-a-parameter-for-adding-a-calculated-field"></a><span data-ttu-id="42ee5-199">Definovat parametr pro přidání vypočítaného pole</span><span class="sxs-lookup"><span data-stu-id="42ee5-199">Define a parameter for adding a calculated field</span></span>

1. <span data-ttu-id="42ee5-200">Vyberte **Parametry**.</span><span class="sxs-lookup"><span data-stu-id="42ee5-200">Select **Parameters**.</span></span>
2. <span data-ttu-id="42ee5-201">Zvolte **Nové**.</span><span class="sxs-lookup"><span data-stu-id="42ee5-201">Select **New**.</span></span>
3. <span data-ttu-id="42ee5-202">Do pole **Název** zadejte **Úroveň zdanění**.</span><span class="sxs-lookup"><span data-stu-id="42ee5-202">In the **Name** field, enter **Taxation Level**.</span></span>
4. <span data-ttu-id="42ee5-203">V poli **Typ** vyberte **Řetězec**.</span><span class="sxs-lookup"><span data-stu-id="42ee5-203">In the **Type** field, select **String**.</span></span>

    <span data-ttu-id="42ee5-204">K zadání typu argumentu parametru lze použít pouze primitivní datové typy.</span><span class="sxs-lookup"><span data-stu-id="42ee5-204">Only primitive data types can be used to specify the type of the parameter’s argument.</span></span> <span data-ttu-id="42ee5-205">Proto nelze pro tento účel použít typy **Seznam záznamů**, **Záznam** a **Výčet**.</span><span class="sxs-lookup"><span data-stu-id="42ee5-205">Therefore, **Record list**, **Record**, and **Enum** types cannot be used for this purpose.</span></span>

    <span data-ttu-id="42ee5-206">Maximální počet parametrů, které lze zadat pro jedno vypočtené pole, je 8.</span><span class="sxs-lookup"><span data-stu-id="42ee5-206">The maximum number of parameters that can be specified for a single calculated field is 8.</span></span>

    ![Seznam zdroje dat parametrů](media/er-calculated-field-type-05.png)

5. <span data-ttu-id="42ee5-208">Vyberte **OK**.</span><span class="sxs-lookup"><span data-stu-id="42ee5-208">Select **OK**.</span></span>

<span data-ttu-id="42ee5-209">Přidáte-li tento parametr, zadáte podmínku, která musí být na místě, aby bylo možné toto vypočtené pole volat.</span><span class="sxs-lookup"><span data-stu-id="42ee5-209">By adding this parameter, you specify the condition that must be in place to call this calculated field.</span></span> <span data-ttu-id="42ee5-210">Při volání tohoto vypočítaného pole je nutné zadat argument parametru **Úroveň zdanění** jako hodnotu s formátem **Řetězec**.</span><span class="sxs-lookup"><span data-stu-id="42ee5-210">When you call this calculated field, you need to specify the argument of the **Taxation Level** parameter as a value with **String** format.</span></span>

   <span data-ttu-id="42ee5-211">Ujistěte se, že definujete parametry pouze pro vypočítaná pole, která jsou uložena v kontejneru (**Seznam záznamů**, **Záznam** nebo **Kontejner**).</span><span class="sxs-lookup"><span data-stu-id="42ee5-211">Make sure that you define parameters only for those calculated fields that reside in a container (either **Record list**, **Record**, or **Container**).</span></span>

   <span data-ttu-id="42ee5-212">Konfigurovaný parametr je k dispozici v seznamu zdrojů dat pro toto vypočtené pole.</span><span class="sxs-lookup"><span data-stu-id="42ee5-212">The configured parameter is available in the list of data sources for this calculated field.</span></span> <span data-ttu-id="42ee5-213">Chcete-li přidat parametr do konfigurovaného výrazu, vyberte možnost **Přidat zdroj dat**.</span><span class="sxs-lookup"><span data-stu-id="42ee5-213">You can add the parameter to the configured expression by selecting **Add data source**.</span></span>

   ![Pole zdroje dat](media/er-calculated-field-type-06.png)

### <a name="define-an-expression-for-adding-a-calculated-field"></a><span data-ttu-id="42ee5-215">Definovat výraz pro přidání vypočítaného pole</span><span class="sxs-lookup"><span data-stu-id="42ee5-215">Define an expression for adding a calculated field</span></span>

1. <span data-ttu-id="42ee5-216">Do pole **Vzorec** zdejte:</span><span class="sxs-lookup"><span data-stu-id="42ee5-216">In the **Formula** field, enter:</span></span> 

    <span data-ttu-id="42ee5-217">**WHERE(\@.Summary2, \@.Summary2.grouped.Level =**</span><span class="sxs-lookup"><span data-stu-id="42ee5-217">**WHERE(\@.Summary2, \@.Summary2.grouped.Level =**</span></span>
    
2. <span data-ttu-id="42ee5-218">V seznamu zdrojů dat vyberte parametr **Úroveň zdanění**.</span><span class="sxs-lookup"><span data-stu-id="42ee5-218">Select the **Taxation Level** parameter in the list of data sources.</span></span>
3. <span data-ttu-id="42ee5-219">Vyberte **Přidat zdroj dat**.</span><span class="sxs-lookup"><span data-stu-id="42ee5-219">Select **Add data source**.</span></span>
4. <span data-ttu-id="42ee5-220">V poli **Vzorec** dokončete výraz jako:</span><span class="sxs-lookup"><span data-stu-id="42ee5-220">In the **Formula** field, finalize the expression as:</span></span>  

    <span data-ttu-id="42ee5-221">**WHERE(\@.Summary2, \@.Summary2.grouped.Level = 'Taxation Level')**</span><span class="sxs-lookup"><span data-stu-id="42ee5-221">**WHERE(\@.Summary2, \@.Summary2.grouped.Level = 'Taxation Level')**</span></span>

5. <span data-ttu-id="42ee5-222">Zvolte **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="42ee5-222">Select **Save**.</span></span>

    ![Informace o datových zdrojových polích](media/er-calculated-field-type-07.png)

6. <span data-ttu-id="42ee5-224">Zavřete stránku **Návrhář vzorce**.</span><span class="sxs-lookup"><span data-stu-id="42ee5-224">Close the **Formula designer** page.</span></span>

### <a name="finish-adding-a-new-calculated-field"></a><span data-ttu-id="42ee5-225">Dokončete přidávávání nových počítaných polí</span><span class="sxs-lookup"><span data-stu-id="42ee5-225">Finish adding a new calculated field</span></span>

- <span data-ttu-id="42ee5-226">Vyberte **OK**.</span><span class="sxs-lookup"><span data-stu-id="42ee5-226">Select **OK**.</span></span>

<span data-ttu-id="42ee5-227">Na stránce **Návrhář formátu** je v konfigurovaných vypočítaných polích **Úrovně** vyžadován argument **Řetězec**.</span><span class="sxs-lookup"><span data-stu-id="42ee5-227">On the **Format designer** page, the configured parameterized calculated field **Levels** requires a **String** argument.</span></span>

![Rozbalený seznam úrovní vypočítaných polí](media/er-calculated-field-type-08.png)

### <a name="use-the-configured-calculated-field-for-binding-format-elements"></a><span data-ttu-id="42ee5-229">Použít nakonfigurované počítané pole pro prvky formátu vazby</span><span class="sxs-lookup"><span data-stu-id="42ee5-229">Use the configured calculated field for binding format elements</span></span>

1. <span data-ttu-id="42ee5-230">Výběrem **Model.Data2.Levels** vyberte nakonfigurované počítané pole.</span><span class="sxs-lookup"><span data-stu-id="42ee5-230">Select **Model.Data2.Levels** to select the configured calculated field.</span></span>
2. <span data-ttu-id="42ee5-231">Vyberte prvek formátu **Statement.Taxation.Regular**.</span><span class="sxs-lookup"><span data-stu-id="42ee5-231">Select the **Statement.Taxation.Regular** format element.</span></span>
3. <span data-ttu-id="42ee5-232">Vyberte možnost **vazba**.</span><span class="sxs-lookup"><span data-stu-id="42ee5-232">Select **Bind**.</span></span>
4. <span data-ttu-id="42ee5-233">Vyberte možnost **Ano**, pokud chcete potvrdit nahrazení aktuálně používaného zdroje dat **Level1** novým zdrojem dat **Levels** ve všech vnořených formátovacích prvcích vybraného prvku formátu.</span><span class="sxs-lookup"><span data-stu-id="42ee5-233">Select **Yes** to confirm the replacement of the currently used data source, **Level1**, by the new data source, **Levels**, in all nested format elements of the selected format element.</span></span>

    <span data-ttu-id="42ee5-234">Použitá vazba byla sestavena jako volání parametrizovaného počítaného pole.</span><span class="sxs-lookup"><span data-stu-id="42ee5-234">Applied binding has been built as a call of the parameterized calculated field.</span></span> <span data-ttu-id="42ee5-235">Standardně se název prvku vázaného formátu používá jako argument pro parametrizované počítané pole za následujících podmínek:</span><span class="sxs-lookup"><span data-stu-id="42ee5-235">By default, the name of the bound format element is used as an argument for parameterized calculated field under the following conditions:</span></span>

      - <span data-ttu-id="42ee5-236">Vypočítané pole je nakonfigurováno pro použití jediného parametru.</span><span class="sxs-lookup"><span data-stu-id="42ee5-236">The calculated field is configured to use a single parameter.</span></span>
      - <span data-ttu-id="42ee5-237">Datový typ tohoto parametru je definován jako **Řetězec**.</span><span class="sxs-lookup"><span data-stu-id="42ee5-237">The data type of this parameter is defined as **String**.</span></span>

    <span data-ttu-id="42ee5-238">Je-li název prvku vázaného formátu prázdný, bude název zdroje dat tohoto prvku použit v použité vazbě.</span><span class="sxs-lookup"><span data-stu-id="42ee5-238">When the name of the bound format element is blank, the data source name of this element is used in applied binding.</span></span>

5. <span data-ttu-id="42ee5-239">Vyberte prvek formátu **Statement.Taxation.Reduced**.</span><span class="sxs-lookup"><span data-stu-id="42ee5-239">Select the **Statement.Taxation.Reduced** format element.</span></span>
6. <span data-ttu-id="42ee5-240">Vyberte možnost **vazba**.</span><span class="sxs-lookup"><span data-stu-id="42ee5-240">Select **Bind**.</span></span>
7. <span data-ttu-id="42ee5-241">Vyberte možnost **Ano**, pokud chcete potvrdit nahrazení aktuálně používaného zdroje dat **Level2** novým zdrojem dat **Levels** ve všech vnořených formátovacích prvcích vybraného prvku formátu.</span><span class="sxs-lookup"><span data-stu-id="42ee5-241">Select **Yes** to confirm the replacement of the currently used data source, **Level2**, by the new data source, **Levels**, in all nested format elements under the selected format element.</span></span>
8. <span data-ttu-id="42ee5-242">Vyberte prvek formátu **Statement.Taxation.None**.</span><span class="sxs-lookup"><span data-stu-id="42ee5-242">Select the **Statement.Taxation.None** format element.</span></span>
9. <span data-ttu-id="42ee5-243">Vyberte možnost **vazba**.</span><span class="sxs-lookup"><span data-stu-id="42ee5-243">Select **Bind**.</span></span>
10. <span data-ttu-id="42ee5-244">Vyberte možnost **Ano**, pokud chcete potvrdit nahrazení aktuálně používaného zdroje dat **Level3** novým zdrojem dat **Levels** ve všech vnořených formátovacích prvcích vybraného prvku formátu.</span><span class="sxs-lookup"><span data-stu-id="42ee5-244">Select **Yes** to confirm the replacement of the currently used data source, **Level3**, by the new data source, **Levels**, in all nested format elements under the selected format element.</span></span>

   <span data-ttu-id="42ee5-245">Když zadáte argument parametrizovaného pole pro prvek XML představující úroveň zdanění (například **Model.Data2.Levels("Reduced")** jako textovou hodnotu), nemusíte provádět stejnou akci pro vnořené atributy XML – jejich vazby automaticky zdědí hodnotu argumentu definovaného na nadřazené úrovni (**Model.Data2.Levels.aggregated.Base**, nikoli **Model.Data2.Levels("Reduced").aggregated.Base**).</span><span class="sxs-lookup"><span data-stu-id="42ee5-245">When you specify the argument of the parameterized calculated field for the XML element representing taxation level (for example, **Model.Data2.Levels("Reduced")** as a text value), you don’t need to do the same for nested XML attributes—their bindings will automatically inherit the value of the argument defined on the parent level (**Model.Data2.Levels.aggregated.Base**, not **Model.Data2.Levels("Reduced").aggregated.Base**).</span></span>

<span data-ttu-id="42ee5-246">Opakující se volání jakéhokoliv parametrizovaného pole nejsou podporována.</span><span class="sxs-lookup"><span data-stu-id="42ee5-246">Recurrent calls of any parameterized calculated field are not supported.</span></span>

<span data-ttu-id="42ee5-247">Můžete vybrat možnost **Upravit vzorec** a změnit argument vyrovnáno podle výchozího pole ve vybrané vazbě.</span><span class="sxs-lookup"><span data-stu-id="42ee5-247">You can select **Edit formula**, and change the applied-by-default argument of the parameterized calculated field in the selected binding.</span></span> <span data-ttu-id="42ee5-248">Pokud tento argument chybí, může způsobit chyby za běhu – uživatelé jsou informováni o takové situaci, když je aktuální formát ověřen.</span><span class="sxs-lookup"><span data-stu-id="42ee5-248">If this argument is missing, it can cause errors at run time — users are informed about such a situation when the current format is validated.</span></span>

![Upozornění na potvrzení ověření](media/er-calculated-field-type-10.png)

## <a name="configure-a-parameterized-calculated-field-to-return-a-record"></a><span data-ttu-id="42ee5-250">Konfigurace parametrizovaného vypočítaného pole pro návrat záznamu</span><span class="sxs-lookup"><span data-stu-id="42ee5-250">Configure a parameterized calculated field to return a record</span></span>
<span data-ttu-id="42ee5-251">Pokud parametrizované pole vrací záznam, je nutné podporovat vazby jednotlivých polí tohoto záznamu k formátování prvků.</span><span class="sxs-lookup"><span data-stu-id="42ee5-251">When a parameterized calculated field returns a record, you need to support binding of individual fields of this record to format elements.</span></span> <span data-ttu-id="42ee5-252">V takovém případě nebude existovat žádná nadřazená vazba, která obsahuje hodnotu argumentu pro volání parametrizovaného počítaného pole - tato hodnota musí být definována ve vazbě pole jednoho záznamu.</span><span class="sxs-lookup"><span data-stu-id="42ee5-252">In such cases there will be no parent binding that contains the value of an argument to call a parameterized calculated field — this value must be defined in the binding of a single record’s field.</span></span>

### <a name="start-adding-a-new-calculated-field"></a><span data-ttu-id="42ee5-253">Začít přidávat nové počítané pole</span><span class="sxs-lookup"><span data-stu-id="42ee5-253">Start adding a new calculated field</span></span>

1. <span data-ttu-id="42ee5-254">Vyberte položku **Model.Data2**.</span><span class="sxs-lookup"><span data-stu-id="42ee5-254">Select the **Model.Data2** item.</span></span>
2. <span data-ttu-id="42ee5-255">Vyberte **přidat**.</span><span class="sxs-lookup"><span data-stu-id="42ee5-255">Select **Add**.</span></span>
3. <span data-ttu-id="42ee5-256">Vyberte **Funkce\\vypočítané pole**.</span><span class="sxs-lookup"><span data-stu-id="42ee5-256">Select **Functions\\Calculated field**.</span></span>
4. <span data-ttu-id="42ee5-257">Do pole **Název** zadejte **LevelRecord**.</span><span class="sxs-lookup"><span data-stu-id="42ee5-257">In the **Name** field, enter **LevelRecord**.</span></span>
5. <span data-ttu-id="42ee5-258">Vyberte možnost **Upravit vzorec**.</span><span class="sxs-lookup"><span data-stu-id="42ee5-258">Select **Edit formula**.</span></span>

### <a name="define-a-parameter-for-adding-a-calculated-field"></a><span data-ttu-id="42ee5-259">Definovat parametr pro přidání vypočítaného pole</span><span class="sxs-lookup"><span data-stu-id="42ee5-259">Define a parameter for adding a calculated field</span></span>

1. <span data-ttu-id="42ee5-260">Vyberte **Parametry**.</span><span class="sxs-lookup"><span data-stu-id="42ee5-260">Select **Parameters**.</span></span>
2. <span data-ttu-id="42ee5-261">Zvolte **Nové**.</span><span class="sxs-lookup"><span data-stu-id="42ee5-261">Select **New**.</span></span>
3. <span data-ttu-id="42ee5-262">Do pole **Název** zadejte **Úroveň zdanění**.</span><span class="sxs-lookup"><span data-stu-id="42ee5-262">In the **Name** field, enter **Taxation Level**.</span></span>
4. <span data-ttu-id="42ee5-263">V poli **Typ** vyberte **Řetězec**.</span><span class="sxs-lookup"><span data-stu-id="42ee5-263">In the **Type** field, select **String**.</span></span>
5. <span data-ttu-id="42ee5-264">Vyberte **OK**.</span><span class="sxs-lookup"><span data-stu-id="42ee5-264">Select **OK**.</span></span>

### <a name="define-an-expression-for-adding-a-calculated-field"></a><span data-ttu-id="42ee5-265">Definovat výraz pro přidání vypočítaného pole</span><span class="sxs-lookup"><span data-stu-id="42ee5-265">Define an expression for adding a calculated field</span></span>

1. <span data-ttu-id="42ee5-266">V poli **Vzorec** zadejte následující:</span><span class="sxs-lookup"><span data-stu-id="42ee5-266">In the **Formula** field, enter the following:</span></span>  
    
    <span data-ttu-id="42ee5-267">**FIRSTORNULL(\@.Levels(**</span><span class="sxs-lookup"><span data-stu-id="42ee5-267">**FIRSTORNULL(\@.Levels(**</span></span>

2. <span data-ttu-id="42ee5-268">Vyberte parametr **Úroveň zdanění**.</span><span class="sxs-lookup"><span data-stu-id="42ee5-268">Select the **Taxation Level** parameter.</span></span>
3. <span data-ttu-id="42ee5-269">Vyberte **Přidat zdroj dat**.</span><span class="sxs-lookup"><span data-stu-id="42ee5-269">Select **Add data source**.</span></span>
4. <span data-ttu-id="42ee5-270">V poli **Vzorec** přidejte **"Úroveň zdanění"))** do stavu, který jste zadali v kroku 1 a dokončete výraz na:</span><span class="sxs-lookup"><span data-stu-id="42ee5-270">In the **Formula** field, append **'Taxation Level'))** to what you entered in Step 1 to finalize the expression to:</span></span>  
    
    <span data-ttu-id="42ee5-271">**FIRSTORNULL(\@.Levels('Taxation Level'))**</span><span class="sxs-lookup"><span data-stu-id="42ee5-271">**FIRSTORNULL(\@.Levels('Taxation Level'))**</span></span>

5. <span data-ttu-id="42ee5-272">Zvolte **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="42ee5-272">Select **Save**.</span></span>
6. <span data-ttu-id="42ee5-273">Zavřete stránku **Návrhář vzorce**.</span><span class="sxs-lookup"><span data-stu-id="42ee5-273">Close **the Formula designer** page.</span></span>

### <a name="finish-adding-a-new-calculated-field"></a><span data-ttu-id="42ee5-274">Dokončete přidávávání nových počítaných polí</span><span class="sxs-lookup"><span data-stu-id="42ee5-274">Finish adding a new calculated field</span></span>

-   <span data-ttu-id="42ee5-275">Vyberte **OK**.</span><span class="sxs-lookup"><span data-stu-id="42ee5-275">Select **OK**.</span></span>

### <a name="use-the-configured-calculated-field-to-bind-format-elements"></a><span data-ttu-id="42ee5-276">Použít nakonfigurované počítané pole pro svázání prvků formátu</span><span class="sxs-lookup"><span data-stu-id="42ee5-276">Use the configured calculated field to bind format elements</span></span>

1. <span data-ttu-id="42ee5-277">Rozbalením **Model.Data2.LevelRecord** vyberte nakonfigurované počítané pole.</span><span class="sxs-lookup"><span data-stu-id="42ee5-277">Expand **Model.Data2.LevelRecord** to select the configured calculated field.</span></span>
2. <span data-ttu-id="42ee5-278">Rozbalte kontejner **Model.Data2.LevelRecord.aggregated** nakonfigurovaného počítaného pole.</span><span class="sxs-lookup"><span data-stu-id="42ee5-278">Expand the **Model.Data2.LevelRecord.aggregated** container of the configured calculated field.</span></span>
3. <span data-ttu-id="42ee5-279">Vyberte pole **Model.Data2.LevelRecord.aggregated.Base**.</span><span class="sxs-lookup"><span data-stu-id="42ee5-279">Select the **Model.Data2.LevelRecord.aggregated.Base** field.</span></span>
4. <span data-ttu-id="42ee5-280">Vyberte prvek formátu **Statement.Taxation.None**.</span><span class="sxs-lookup"><span data-stu-id="42ee5-280">Select the **Statement.Taxation.None** format element.</span></span>
5. <span data-ttu-id="42ee5-281">Vyberte možnost **Zrušit vazbu**.</span><span class="sxs-lookup"><span data-stu-id="42ee5-281">Select **Unbind**.</span></span>
6. <span data-ttu-id="42ee5-282">Vyberte prvek formátu **Statement.Taxation.None.Base**.</span><span class="sxs-lookup"><span data-stu-id="42ee5-282">Select the **Statement.Taxation.None.Base** format element.</span></span>
7. <span data-ttu-id="42ee5-283">Vyberte možnost **vazba**.</span><span class="sxs-lookup"><span data-stu-id="42ee5-283">Select **Bind**.</span></span>
8. <span data-ttu-id="42ee5-284">Vyberte možnost **Upravit vzorec**.</span><span class="sxs-lookup"><span data-stu-id="42ee5-284">Select **Edit formula**.</span></span>
9. <span data-ttu-id="42ee5-285">Změňte výraz na **Model.Data2.LevelRecord("None").aggregated.Base**.</span><span class="sxs-lookup"><span data-stu-id="42ee5-285">Change the expression to **Model.Data2.LevelRecord("None").aggregated.Base**.</span></span>

![Aktualizovaný výraz](media/er-calculated-field-type-11.png)

## <a name="remove-calculated-fields-that-are-not-used"></a><span data-ttu-id="42ee5-287">Odebrat vypočtená pole, která nejsou použita</span><span class="sxs-lookup"><span data-stu-id="42ee5-287">Remove calculated fields that are not used</span></span>

1. <span data-ttu-id="42ee5-288">Vyberte **Model.Data2.Level1**.</span><span class="sxs-lookup"><span data-stu-id="42ee5-288">Select **Model.Data2.Level1**.</span></span>
2. <span data-ttu-id="42ee5-289">Zvolte **Odstranit**.</span><span class="sxs-lookup"><span data-stu-id="42ee5-289">Select **Delete**.</span></span>
3. <span data-ttu-id="42ee5-290">Vyberte **Model.Data2.Level2**.</span><span class="sxs-lookup"><span data-stu-id="42ee5-290">Select **Model.Data2.Level2**.</span></span>
4. <span data-ttu-id="42ee5-291">Zvolte **Odstranit**.</span><span class="sxs-lookup"><span data-stu-id="42ee5-291">Select **Delete**.</span></span>
5. <span data-ttu-id="42ee5-292">Vyberte **Model.Data2.Level3**.</span><span class="sxs-lookup"><span data-stu-id="42ee5-292">Select **Model.Data2.Level3**.</span></span>
6. <span data-ttu-id="42ee5-293">Zvolte **Odstranit**.</span><span class="sxs-lookup"><span data-stu-id="42ee5-293">Select **Delete**.</span></span>
7. <span data-ttu-id="42ee5-294">Zvolte **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="42ee5-294">Select **Save**.</span></span>

  > [!NOTE]
  > <span data-ttu-id="42ee5-295">Znovu jste použili stejný model počítaného pole **Model.Data2.Levels** několikrát ve formátu vazeb.</span><span class="sxs-lookup"><span data-stu-id="42ee5-295">You reused the same calculated field **Model.Data2.Levels** several times in format bindings.</span></span> <span data-ttu-id="42ee5-296">Je mnohem jednodušší použít a udržovat jedno vypočítané pole namísto více podobných polí.</span><span class="sxs-lookup"><span data-stu-id="42ee5-296">It is much easier to use and maintain a single calculated field instead of doing this for multiple similar fields.</span></span>

8. <span data-ttu-id="42ee5-297">Zavřete stránku **Návrhář formátu**.</span><span class="sxs-lookup"><span data-stu-id="42ee5-297">Close the **Format designer** page.</span></span>

## <a name="complete-adjusted-version-of-a-derived-format"></a><span data-ttu-id="42ee5-298">Dokončete upravenou verzi odvozeného formátu</span><span class="sxs-lookup"><span data-stu-id="42ee5-298">Complete adjusted version of a derived format</span></span>

1. <span data-ttu-id="42ee5-299">Na pevné záložce **Verze** vyberte možnost **Stav změny**.</span><span class="sxs-lookup"><span data-stu-id="42ee5-299">In the **Versions** FastTab, select **Change status**.</span></span>
2. <span data-ttu-id="42ee5-300">Zvolte **Dokončit**.</span><span class="sxs-lookup"><span data-stu-id="42ee5-300">Select **Complete**.</span></span>

## <a name="export-completed-version-of-a-derived-format"></a><span data-ttu-id="42ee5-301">Exportujte dokončenou verzi odvozeného formátu</span><span class="sxs-lookup"><span data-stu-id="42ee5-301">Export completed version of a derived format</span></span>

1. <span data-ttu-id="42ee5-302">Vyberte **Formát pro učení parametrizovaných volání (vlastní)** ve stromu konfigurací.</span><span class="sxs-lookup"><span data-stu-id="42ee5-302">Select **Format to learn parameterized calls (custom)** format in the configurations tree.</span></span>
2. <span data-ttu-id="42ee5-303">Na pevné záložce **Verze** vyberte dokončenou verzi 1.1.1.</span><span class="sxs-lookup"><span data-stu-id="42ee5-303">In the **Versions** FastTab, select the completed version 1.1.1.</span></span>
3. <span data-ttu-id="42ee5-304">Vyberte **Exchange**.</span><span class="sxs-lookup"><span data-stu-id="42ee5-304">Select **Exchange**.</span></span>
4. <span data-ttu-id="42ee5-305">Vyberte **Exportovat jako soubor XML**.</span><span class="sxs-lookup"><span data-stu-id="42ee5-305">Select **Export as XML file**.</span></span>
5. <span data-ttu-id="42ee5-306">Uloží staženou konfiguraci místně ve formátu XML.</span><span class="sxs-lookup"><span data-stu-id="42ee5-306">Store the downloaded configuration locally, in XML format.</span></span>

## <a name="test-er-formats"></a><span data-ttu-id="42ee5-307">Testovat formáty ER</span><span class="sxs-lookup"><span data-stu-id="42ee5-307">Test ER formats</span></span> 
<span data-ttu-id="42ee5-308">Chcete-li se ujistit, že nakonfigurovaná počítaná pole fungují správně, můžete spustit počáteční a vylepšené formáty ER.</span><span class="sxs-lookup"><span data-stu-id="42ee5-308">You can run the initial and improved ER formats to make sure that configured parameterized calculated fields work properly.</span></span>

### <a name="import-er-configurations"></a><span data-ttu-id="42ee5-309">Import konfigurací ER</span><span class="sxs-lookup"><span data-stu-id="42ee5-309">Import ER configurations</span></span>
<span data-ttu-id="42ee5-310">Revidované konfigurace lze importovat z RCS pomocí úložiště ER typu **RCS**.</span><span class="sxs-lookup"><span data-stu-id="42ee5-310">You can import reviewed configurations from RCS by using the ER repository of the **RCS** type.</span></span> <span data-ttu-id="42ee5-311">Pokud jste již provedli kroky v tématu, [Import konfigurace elektronického vykazování z Regulatory Configuration Service](rcs-download-configurations.md), použijte nakonfigurované úložiště ER pro import konfigurací popsaných dříve v tomto tématu do vašeho prostředí.</span><span class="sxs-lookup"><span data-stu-id="42ee5-311">If you already went through the steps in the topic, [Import Electronic reporting configurations from Regulatory Configuration Services](rcs-download-configurations.md), use the configured ER repository to import configurations discussed earlier in this topic to your environment.</span></span> <span data-ttu-id="42ee5-312">V opačném případě postupujte takto:</span><span class="sxs-lookup"><span data-stu-id="42ee5-312">Otherwise, follow these steps:</span></span>

1. <span data-ttu-id="42ee5-313">Vyberte společnost **DEMF** a na výchozím řídicím panelu vyberte možnost **Elektronické vykazování**.</span><span class="sxs-lookup"><span data-stu-id="42ee5-313">Select the **DEMF** company and on the default dashboard, select **Electronic reporting**.</span></span>
2. <span data-ttu-id="42ee5-314">Vyberte **Konfigurace vykazování**.</span><span class="sxs-lookup"><span data-stu-id="42ee5-314">Select **Reporting configurations**.</span></span>
3. <span data-ttu-id="42ee5-315">Import stažených konfigurací z Microsoft Download Center v následujícím pořadí: datový model, mapování modelu, formát.</span><span class="sxs-lookup"><span data-stu-id="42ee5-315">Import the configurations from Microsoft Download Center in the following sequence: data model, model mapping, format.</span></span> <span data-ttu-id="42ee5-316">Pro každou konfiguraci ER proveďte následující kroky:</span><span class="sxs-lookup"><span data-stu-id="42ee5-316">Complete the following steps for each ER configuration:</span></span>

    1. <span data-ttu-id="42ee5-317">Vyberte **Exchange**.</span><span class="sxs-lookup"><span data-stu-id="42ee5-317">Select **Exchange.**</span></span>
    2. <span data-ttu-id="42ee5-318">Vyberte **Načíst ze souboru XML**.</span><span class="sxs-lookup"><span data-stu-id="42ee5-318">Select **Load from XML file**.</span></span>
    3. <span data-ttu-id="42ee5-319">Zvolte **Procházet** a vyberte požadovanou konfiguraci elektronického výkaznictví ve formátu XML.</span><span class="sxs-lookup"><span data-stu-id="42ee5-319">Select **Browse** to select the required ER configuration in XML format.</span></span>
    4. <span data-ttu-id="42ee5-320">Vyberte **OK**.</span><span class="sxs-lookup"><span data-stu-id="42ee5-320">Select **OK**.</span></span>

4. <span data-ttu-id="42ee5-321">Importujte exportované z RCS dokončené verze 1.1.1 **Formát pro učení parametrizovaných volání (vlastní)**:</span><span class="sxs-lookup"><span data-stu-id="42ee5-321">Import the exported from RCS completed version 1.1.1 of the **Format to learn parameterized calls (custom)** format:</span></span>

    1. <span data-ttu-id="42ee5-322">Vyberte **Exchange**.</span><span class="sxs-lookup"><span data-stu-id="42ee5-322">Select **Exchange.**</span></span>
    2. <span data-ttu-id="42ee5-323">Vyberte **Načíst ze souboru XML**.</span><span class="sxs-lookup"><span data-stu-id="42ee5-323">Select **Load from XML file**.</span></span>
    3. <span data-ttu-id="42ee5-324">Vyberte **Procházet** a vyberte místně uložený soubor **Formát pro učení parametrizovaných volání (vlastní)** ve formátu XML.</span><span class="sxs-lookup"><span data-stu-id="42ee5-324">Select **Browse** to select the locally stored **Format to learn parameterized calls (custom)** file in XML format.</span></span>
    4. <span data-ttu-id="42ee5-325">Vyberte **OK**.</span><span class="sxs-lookup"><span data-stu-id="42ee5-325">Select **OK**.</span></span>

### <a name="run-er-formats"></a><span data-ttu-id="42ee5-326">Spustit formáty ER</span><span class="sxs-lookup"><span data-stu-id="42ee5-326">Run ER formats</span></span>

1. <span data-ttu-id="42ee5-327">Ve stromu konfigurace rozbalte obsah položky **Model pro seznámení s parametrizovanými voláními**.</span><span class="sxs-lookup"><span data-stu-id="42ee5-327">In the configuration tree, expand the content of the **Model to learn parameterized calls** item.</span></span>
2. <span data-ttu-id="42ee5-328">Vyberte **Formát pro informace o voláních s parametry**.</span><span class="sxs-lookup"><span data-stu-id="42ee5-328">Select **Format to learn parameterized calls**.</span></span>
3. <span data-ttu-id="42ee5-329">Vyberte **Spustit** na horním pásu.</span><span class="sxs-lookup"><span data-stu-id="42ee5-329">Select **Run** on the top-most ribbon.</span></span>
4. <span data-ttu-id="42ee5-330">Uložte místně generovaný výstup.</span><span class="sxs-lookup"><span data-stu-id="42ee5-330">Save the locally generated output.</span></span>
5. <span data-ttu-id="42ee5-331">Vyberte položku **Formát pro učení parametrizovaných volání (vlastní)**.</span><span class="sxs-lookup"><span data-stu-id="42ee5-331">Select the **Format to learn parameterized calls (custom)** item.</span></span>
6. <span data-ttu-id="42ee5-332">Vyberte **Spustit** na horním pásu.</span><span class="sxs-lookup"><span data-stu-id="42ee5-332">Select **Run** on the top-most ribbon.</span></span>
7. <span data-ttu-id="42ee5-333">Uložte generovaný výstup místně.</span><span class="sxs-lookup"><span data-stu-id="42ee5-333">Save the generated output locally.</span></span> 
8. <span data-ttu-id="42ee5-334">Porovnejte obsah generovaných výstupů.</span><span class="sxs-lookup"><span data-stu-id="42ee5-334">Compare the contents of the generated outputs.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="42ee5-335">Další zdroje</span><span class="sxs-lookup"><span data-stu-id="42ee5-335">Additional resources</span></span>
[<span data-ttu-id="42ee5-336">Návrhář receptur v elektronickém výkaznictví</span><span class="sxs-lookup"><span data-stu-id="42ee5-336">Formula designer in Electronic reporting</span></span>](general-electronic-reporting-formula-designer.md)
