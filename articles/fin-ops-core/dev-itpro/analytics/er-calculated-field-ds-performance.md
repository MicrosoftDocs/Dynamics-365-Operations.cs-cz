---
title: Zlepšete výkon řešení elektronického výkaznictví přidáním parametrizovaných zdrojů dat typu POČÍTANÉ POLE
description: Tohle téma popisuje, jak můžete zlepšit výkon řešení elektronického výkaznictví přidáním parametrizovaných zdrojů dat typu POČÍTANÉ POLE.
author: NickSelin
manager: AnnBe
ms.date: 09/02/2020
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
ms.openlocfilehash: 940b696a06fb46bcd0557f059327cd4340448137
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 12/05/2020
ms.locfileid: "4681273"
---
# <a name="improve-the-performance-of-er-solutions-by-adding-parameterized-calculated-field-data-sources"></a><span data-ttu-id="f8277-103">Zlepšete výkon řešení elektronického výkaznictví přidáním parametrizovaných zdrojů dat typu POČÍTANÉ POLE</span><span class="sxs-lookup"><span data-stu-id="f8277-103">Improve the performance of ER solutions by adding parameterized CALCULATED FIELD data sources</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="f8277-104">Tohle téma popisuje, jak můžete použít informace ze spuštěných [sledování výkonu](trace-execution-er-troubleshoot-perf.md) z formátů [elektronického výkaznictví](general-electronic-reporting.md) ke zlepšení výkonu prostřednictvím parametrizovaných zdrojů dat typu **Počítané pole**.</span><span class="sxs-lookup"><span data-stu-id="f8277-104">This topic explains how you can take [performance traces](trace-execution-er-troubleshoot-perf.md) of [Electronic reporting (ER)](general-electronic-reporting.md) formats that are run, and then use the information from those traces to help improve performance by configuring a parameterized **Calculated field** data source.</span></span>

<span data-ttu-id="f8277-105">V rámci procesu vytváření konfigurací elektronického výkaznictví pro generování obchodních dokumentů definujete metodu, která se používá k načtení dat z aplikace a jejich zadávání do generovaného výstupu.</span><span class="sxs-lookup"><span data-stu-id="f8277-105">As part of the process of designing ER configurations to generate business documents, you define the method that is used to retrieve data from the application and enter it in the generated output.</span></span> <span data-ttu-id="f8277-106">Návrhem parametrizovaného zdroje dat elektronického výkaznictví typu **Počítané pole** můžete snížit počet volání databáze a výrazně snížit čas a náklady spojené se shromažďováním podrobností při spuštění formátu elektronického výkaznictví.</span><span class="sxs-lookup"><span data-stu-id="f8277-106">By designing a parametrized ER data source of the **Calculated field** type, you can reduce the number of database calls, and significantly reduce the time and cost that are involved in collecting the details of ER format execution.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="f8277-107">Předpoklady</span><span class="sxs-lookup"><span data-stu-id="f8277-107">Prerequisites</span></span>

- <span data-ttu-id="f8277-108">Abyste mohli dokončit příklady v tomto tématu, musíte mít přístup k některé z následujících [rolí](../sysadmin/tasks/assign-users-security-roles.md):</span><span class="sxs-lookup"><span data-stu-id="f8277-108">To complete the examples in this topic, you must have the access to one of the following [roles](../sysadmin/tasks/assign-users-security-roles.md):</span></span>

    - <span data-ttu-id="f8277-109">Návrhář elektronického výkaznictví</span><span class="sxs-lookup"><span data-stu-id="f8277-109">Electronic reporting developer</span></span>
    - <span data-ttu-id="f8277-110">Funkční konzultant elektronického výkaznictví</span><span class="sxs-lookup"><span data-stu-id="f8277-110">Electronic reporting functional consultant</span></span>
    - <span data-ttu-id="f8277-111">Správce systému</span><span class="sxs-lookup"><span data-stu-id="f8277-111">System administrator</span></span>

- <span data-ttu-id="f8277-112">Společnost musí být nastavena na **DEMF**.</span><span class="sxs-lookup"><span data-stu-id="f8277-112">The company must be set to **DEMF**.</span></span>
- <span data-ttu-id="f8277-113">Podle pokynů v [příloze 1](#appendix1) tohoto tématu si stáhněte součásti ukázkového řešení elektronického výkaznictví společnosti Microsoft, které jsou potřeba k provedení příkladů v tomto tématu.</span><span class="sxs-lookup"><span data-stu-id="f8277-113">Follow the steps in [Appendix 1](#appendix1) of this topic to download the components of the sample Microsoft ER solution that is required to complete the examples in this topic.</span></span>
- <span data-ttu-id="f8277-114">Podle pokynů v [příloze 2](#appendix2) v tomto tématu můžete nakonfigurovat minimální sadu parametrů elektronického výkaznictví, které jsou potřeba k použití architektury elektronického výkaznictví k zlepšení výkonu ukázkového řešení elektronického výkaznictví společnosti Microsoft.</span><span class="sxs-lookup"><span data-stu-id="f8277-114">Follow the steps in [Appendix 2](#appendix2) of this topic to configure the minimal set of ER parameters that is required to use the ER framework to help improve the performance of the sample Microsoft ER solution.</span></span>

## <a name="import-the-sample-er-solution"></a><span data-ttu-id="f8277-115">Import ukázkového řešení elektronického výkaznictví</span><span class="sxs-lookup"><span data-stu-id="f8277-115">Import the sample ER solution</span></span>

<span data-ttu-id="f8277-116">Představte si, že musíte navrhnout nové řešení elektronického výkaznictví pro generování nové sestavy, která obsahuje transakce dodavatele.</span><span class="sxs-lookup"><span data-stu-id="f8277-116">Imagine that you must design an ER solution to generate a new report that shows vendor transactions.</span></span> <span data-ttu-id="f8277-117">Momentálně můžete najít transakce pro zvoleného dodavatele na stránce **Transakce dodavatele** (přejděte na **Závazky** \> **Dodavatelé** \> **Všichni dodavatelé**, zvolte dodavatele a potom v podokně akcí na kartě **Dodavatel** ve skupině **Transakce** zvolte **Transakce**).</span><span class="sxs-lookup"><span data-stu-id="f8277-117">Currently, you can find the transactions for a selected vendor on the **Vendor transactions** page (go to **Account payable** \> **Vendors** \> **All vendors**, select a vendor, and then, on the Action Pane, on the **Vendor** tab, in the **Transactions** group, select **Transactions**).</span></span> <span data-ttu-id="f8277-118">Chcete však mít všechny transakce dodavatele současně v jednom elektronickém dokumentu ve formátu XML.</span><span class="sxs-lookup"><span data-stu-id="f8277-118">However, you want to have all vendor transactions together in one electronic document in XML format.</span></span> <span data-ttu-id="f8277-119">Toto řešení bude obsahovat několik konfigurací elektronického výkaznictví, které obsahují požadovaný datový model, mapování modelu a součásti formátu.</span><span class="sxs-lookup"><span data-stu-id="f8277-119">This solution will consist of several ER configurations that contain the required data model, model mapping, and format components.</span></span>

<span data-ttu-id="f8277-120">Prvním krokem je import ukázkového řešení elektronického výkaznictví k vygenerování sestavy transakcí dodavatele.</span><span class="sxs-lookup"><span data-stu-id="f8277-120">The first step is to import the sample ER solution to generate a vendor transactions report.</span></span>

1. <span data-ttu-id="f8277-121">Přihlaste se k instanci Microsoft Dynamics 365 Finance, která je zřízena pro vaši společnost.</span><span class="sxs-lookup"><span data-stu-id="f8277-121">Sign in to the instance of Microsoft Dynamics 365 Finance that is provisioned for your company.</span></span>
2. <span data-ttu-id="f8277-122">V tomto tématu vytvoříte a upravíte konfigurace pro vzorovou společnost **Litware, Inc.**.</span><span class="sxs-lookup"><span data-stu-id="f8277-122">In this topic, you will create and modify configurations for the **Litware, Inc.** sample company.</span></span> <span data-ttu-id="f8277-123">Ujistěte se, že tento poskytovatel konfigurace byl přidán do instance Finance a je označen jako aktivní.</span><span class="sxs-lookup"><span data-stu-id="f8277-123">Make sure that this configuration provider has been added to your Finance instance and is marked as active.</span></span> <span data-ttu-id="f8277-124">Další informace naleznete ve [Vytvoření poskytovatelů konfigurace a jejich označení jako aktivních](tasks/er-configuration-provider-mark-it-active-2016-11.md).</span><span class="sxs-lookup"><span data-stu-id="f8277-124">For more information, see [Create configuration providers and mark them as active](tasks/er-configuration-provider-mark-it-active-2016-11.md).</span></span>
3. <span data-ttu-id="f8277-125">V pracovním prostoru **Elektronické výkaznictví** vyberte dlaždici **Konfigurace výkaznictví**.</span><span class="sxs-lookup"><span data-stu-id="f8277-125">In the **Electronic reporting** workspace, select the **Reporting configurations** tile.</span></span>
4. <span data-ttu-id="f8277-126">Na stránce **Konfigurace** importujte konfigurace elektronického výkaznictví, které jste stáhli jako nezbytný požadavek do Finance, v následujícím pořadí: datový model, mapování modelu, formát.</span><span class="sxs-lookup"><span data-stu-id="f8277-126">On the **Configurations** page, import the ER configurations that you downloaded as a prerequisite into Finance, in the following order: data model, model mapping, format.</span></span> <span data-ttu-id="f8277-127">Pro každou konfiguraci postupujte takto:</span><span class="sxs-lookup"><span data-stu-id="f8277-127">For each configuration, follow these steps:</span></span>

    1. <span data-ttu-id="f8277-128">V podokně akcí vyberte **Směnka** \> **Načíst ze souboru XML**.</span><span class="sxs-lookup"><span data-stu-id="f8277-128">On the Action Pane, select **Exchange** \> **Load from XML file**.</span></span>
    2. <span data-ttu-id="f8277-129">Zvolte **Procházet** a vyberte příslušný soubor pro konfiguraci elektronického výkaznictví ve formátu XML.</span><span class="sxs-lookup"><span data-stu-id="f8277-129">Select **Browse**, and select the appropriate file for the ER configuration in XML format.</span></span>
    3. <span data-ttu-id="f8277-130">Vyberte **OK**.</span><span class="sxs-lookup"><span data-stu-id="f8277-130">Select **OK**.</span></span>

![Importované konfigurace na stránce Konfigurace](./media/er-calculated-field-ds-performance-imported-configurations.png)

## <a name="review-the-sample-er-solution"></a><span data-ttu-id="f8277-132">Kontrola ukázkového řešení elektronického výkaznictví</span><span class="sxs-lookup"><span data-stu-id="f8277-132">Review the sample ER solution</span></span>

### <a name="review-the-model-mapping"></a><span data-ttu-id="f8277-133">Kontrola mapování modelu</span><span class="sxs-lookup"><span data-stu-id="f8277-133">Review the model mapping</span></span>

1. <span data-ttu-id="f8277-134">Na stránce **Konfigurace** ve stromu konfigurací položku **Model zlepšení výkonu** a vyberte možnost **Mapování zlepšení výkonu**.</span><span class="sxs-lookup"><span data-stu-id="f8277-134">On the **Configurations** page, in the configuration tree, expand **Performance improvement model**, and select **Performance improvement mapping**.</span></span>
2. <span data-ttu-id="f8277-135">V podokně akcí zvolte **Návrhář**.</span><span class="sxs-lookup"><span data-stu-id="f8277-135">On the Action Pane, select **Designer**.</span></span>
3. <span data-ttu-id="f8277-136">Na stránce **Mapování modelu na zdroj dat** v podokně Akce vyberte možnost **Návrhář**.</span><span class="sxs-lookup"><span data-stu-id="f8277-136">On the **Model to datasource mapping** page, on the Action Pane, select **Designer**.</span></span>

    <span data-ttu-id="f8277-137">Toto mapování modelu elektronického výkaznictví je navrženo k následujícím akcím:</span><span class="sxs-lookup"><span data-stu-id="f8277-137">This ER model mapping is designed to perform the following actions:</span></span>

    - <span data-ttu-id="f8277-138">Načtěte seznam transakcí dodavatele, které jsou uloženy v tabulce VendTrans (zdroj dat **Trans**).</span><span class="sxs-lookup"><span data-stu-id="f8277-138">Fetch the list of vendor transactions that are stored in the VendTrans table (**Trans** data source).</span></span>
    - <span data-ttu-id="f8277-139">Pro každou transakci načtěte z tabulky VendTable záznam dodavatele, pro kterého byla transakce zaúčtována (zdroj dat **\#Vend**).</span><span class="sxs-lookup"><span data-stu-id="f8277-139">For every transaction, fetch, from the VendTable table, the record of a vendor that the transaction has been posted for (**\#Vend** data source).</span></span>

    > [!NOTE]
    > <span data-ttu-id="f8277-140">Zdroj dat **\#Vend** je nakonfigurován tak, aby načetl odpovídající záznam dodavatele pomocí existujícího vztahu N:1 **\@'\>Relations'.VendTable\_AccountNum**.</span><span class="sxs-lookup"><span data-stu-id="f8277-140">The **\#Vend** data source is configured to fetch the corresponding vendor record by using the existing many-to-one relation **\@.'\>Relations'.VendTable\_AccountNum**.</span></span>

    <span data-ttu-id="f8277-141">Mapování modelu v této konfiguraci implementuje základní datový model pro všechny formáty elektronického výkaznictví vytvořené pro tento model a spuštěné ve Finance.</span><span class="sxs-lookup"><span data-stu-id="f8277-141">The model mapping in this configuration implements the base data model for any ER formats that are created for this model and run in Finance.</span></span> <span data-ttu-id="f8277-142">V důsledku toho je obsah zdroje dat **Trans** vystaven pro formáty elektronického výkaznictví, jako jsou například abstraktní zdroje dat **modelu**.</span><span class="sxs-lookup"><span data-stu-id="f8277-142">Therefore, the content of the **Trans** data source is exposed for ER formats such as abstract **model** data sources.</span></span>

    ![Zdroj dat Trans na stránce návrháře mapování modelů](media/er-calculated-field-ds-performance-mapping-1.png)

4. <span data-ttu-id="f8277-144">Zavřete stránku **Návrhář mapování modelu**.</span><span class="sxs-lookup"><span data-stu-id="f8277-144">Close the **Model mapping designer** page.</span></span>
5. <span data-ttu-id="f8277-145">Zavřete stránku **Mapování modelu na zdroj dat**.</span><span class="sxs-lookup"><span data-stu-id="f8277-145">Close the **Model to datasource mapping** page.</span></span>

### <a name="review-format"></a><span data-ttu-id="f8277-146">Zkontrolovat formát</span><span class="sxs-lookup"><span data-stu-id="f8277-146">Review format</span></span>

1. <span data-ttu-id="f8277-147">Na stránce **Konfigurace** ve stromu konfigurací položku **Model zlepšení výkonu** a vyberte možnost **Formát zlepšení výkonu**.</span><span class="sxs-lookup"><span data-stu-id="f8277-147">On the **Configurations** page, in the configuration tree, expand **Performance improvement model**, and select **Performance improvement format**.</span></span>
2. <span data-ttu-id="f8277-148">V podokně akcí zvolte **Návrhář**.</span><span class="sxs-lookup"><span data-stu-id="f8277-148">On the Action Pane, select **Designer**.</span></span>
3. <span data-ttu-id="f8277-149">Na stránce **Návrhář formátu** na kartě **Mapování** vyberte **Rozbalit/sbalit**.</span><span class="sxs-lookup"><span data-stu-id="f8277-149">On the **Format designer** page, on the **Mapping** tab, select **Expand/Collapse**.</span></span>
4. <span data-ttu-id="f8277-150">Rozbalte položky **Model**, **Data** a **Transakce**.</span><span class="sxs-lookup"><span data-stu-id="f8277-150">Expand the **Model**, **Data,** and **Transaction** items.</span></span>

    <span data-ttu-id="f8277-151">Tento formát elektronického výkaznictví je navržen tak, aby generoval zprávu o transakcích dodavatele ve formátu XML.</span><span class="sxs-lookup"><span data-stu-id="f8277-151">This ER format is designed to generate a vendor transactions report in XML format.</span></span>

    ![Formátování zdroje dat a konfigurovaných vazeb prvků formátu na stránce Návrhář formátu](media/er-calculated-field-ds-performance-format.png)

5. <span data-ttu-id="f8277-153">Zavřete stránku **Návrhář formátu**.</span><span class="sxs-lookup"><span data-stu-id="f8277-153">Close the **Format designer** page.</span></span>

## <a name="run-the-sample-er-solution-to-trace-execution"></a><span data-ttu-id="f8277-154">Spuštění ukázkového řešení elektronického výkaznictví pro sledování provádění</span><span class="sxs-lookup"><span data-stu-id="f8277-154">Run the sample ER solution to trace execution</span></span>

<span data-ttu-id="f8277-155">Představte si, že jste dokončili návrh první verze řešení elektronického výkaznictví.</span><span class="sxs-lookup"><span data-stu-id="f8277-155">Imagine that you've finished designing the first version of the ER solution.</span></span> <span data-ttu-id="f8277-156">Nyní chcete řešení vyzkoušet v instanci Finance a analyzovat výkon při jeho provádění.</span><span class="sxs-lookup"><span data-stu-id="f8277-156">You now want to test the solution in your Finance instance and analyze the execution performance.</span></span>

### <a name="turn-on-the-er-performance-trace"></a><span data-ttu-id="f8277-157">Zapnutí sledování výkonu elektronického výkaznictví</span><span class="sxs-lookup"><span data-stu-id="f8277-157">Turn on the ER performance trace</span></span>

1. <span data-ttu-id="f8277-158">Vyberte společnost **DEMF**.</span><span class="sxs-lookup"><span data-stu-id="f8277-158">Select the **DEMF** company.</span></span>
2. <span data-ttu-id="f8277-159">Podle pokynů v části [Zapnutí sledování výkonu elektronického výkaznictví](trace-execution-er-troubleshoot-perf.md#turn-on-the-er-performance-trace) vygenerujte sledování výkonu, když je spuštěn formát elektronického výkaznictví.</span><span class="sxs-lookup"><span data-stu-id="f8277-159">Follow the steps in [Turn on the ER performance trace](trace-execution-er-troubleshoot-perf.md#turn-on-the-er-performance-trace) to generate a performance trace while an ER format is run.</span></span>

    ![Dialogové okno Parametry uživatele](media/er-calculated-field-ds-performance-format-user-parameters.png)

### <a name="run-the-er-format"></a><a id="run-format"></a><span data-ttu-id="f8277-161">Spuštění formátu elektronického výkaznictví</span><span class="sxs-lookup"><span data-stu-id="f8277-161">Run the ER format</span></span>

1. <span data-ttu-id="f8277-162">Přejděte do části **Správa organizace** \> **Elektronické výkaznictví** \> **Konfigurace**.</span><span class="sxs-lookup"><span data-stu-id="f8277-162">Go to **Organization administration** \> **Electronic reporting** \> **Configurations**.</span></span>
2. <span data-ttu-id="f8277-163">Na stránce **Konfigurace** ve stromové struktuře konfigurace vyberte položku **Formát zlepšení výkonu**.</span><span class="sxs-lookup"><span data-stu-id="f8277-163">On the **Configurations** page, in the configuration tree, select **Performance improvement format**.</span></span>
3. <span data-ttu-id="f8277-164">V podokně akcí zvolte **Spustit**.</span><span class="sxs-lookup"><span data-stu-id="f8277-164">On the Action Pane, select **Run**.</span></span>

## <a name="use-the-performance-trace-to-analyze-model-mapping-performance"></a><span data-ttu-id="f8277-165">Použití sledování výkonu k analýze výkonu mapování modelů</span><span class="sxs-lookup"><span data-stu-id="f8277-165">Use the performance trace to analyze model mapping performance</span></span>

1. <span data-ttu-id="f8277-166">Na stránce **Konfigurace** ve stromové struktuře konfigurace vyberte položku **Mapování zlepšení výkonu**.</span><span class="sxs-lookup"><span data-stu-id="f8277-166">On the **Configurations** page, in the configuration tree, select **Performance improvement mapping**.</span></span>
2. <span data-ttu-id="f8277-167">V podokně akcí zvolte **Návrhář**.</span><span class="sxs-lookup"><span data-stu-id="f8277-167">On the Action Pane, select **Designer**.</span></span>
3. <span data-ttu-id="f8277-168">Na stránce **Mapování modelu** v podokně Akce vyberte možnost **Návrhář**.</span><span class="sxs-lookup"><span data-stu-id="f8277-168">On the **Model mappings** page, on the Action Pane, select **Designer**.</span></span>
4. <span data-ttu-id="f8277-169">Na stránce **Návrhář mapování modelu** v podokně akcí vyberte **Sledování výkonu**.</span><span class="sxs-lookup"><span data-stu-id="f8277-169">On the **Model mapping designer** page, on the Action Pane, select **Performance trace**.</span></span>
5. <span data-ttu-id="f8277-170">Vyberte nejnovější sledování, které bylo vygenerováno, a poté vyberte **OK**.</span><span class="sxs-lookup"><span data-stu-id="f8277-170">Select the most recent trace that was generated, and then select **OK**.</span></span>

<span data-ttu-id="f8277-171">Nyní jsou dostupné nové informace pro některé položky zdroje dat aktuálního mapování modelu:</span><span class="sxs-lookup"><span data-stu-id="f8277-171">New information is now available for some data source items of the current model mapping:</span></span>

- <span data-ttu-id="f8277-172">Skutečný čas strávený získáváním dat pomocí zdroje dat</span><span class="sxs-lookup"><span data-stu-id="f8277-172">The actual time that was spent getting data by using the data source</span></span>
- <span data-ttu-id="f8277-173">Stejný čas vyjádřený jako procento z celkového času stráveného spouštěním celého mapování modelu</span><span class="sxs-lookup"><span data-stu-id="f8277-173">The same time expressed as a percentage of the total time that was spent running the whole model mapping</span></span>

![Podrobnosti o době provedení na stránce návrháře mapování modelů](./media/er-calculated-field-ds-performance-mapping-2.png)

<span data-ttu-id="f8277-175">Mřížka **Statistiky výkonu** ukazuje, že zdroj dat **Trans** jednou volá tabulku VendTrans.</span><span class="sxs-lookup"><span data-stu-id="f8277-175">The **Performance statistics** grid shows that the **Trans** data source calls the VendTrans table one time.</span></span> <span data-ttu-id="f8277-176">Hodnota **\[265\]\[Q:265\]** ze zdroje dat **Trans** udává, že 265 transakcí dodavatele bylo načteno z tabulky aplikace a vráceno do datového modelu.</span><span class="sxs-lookup"><span data-stu-id="f8277-176">The value **\[265\]\[Q:265\]** of the **Trans** data source indicates that 265 vendor transactions have been fetched from the application table and returned to the data model.</span></span>

<span data-ttu-id="f8277-177">Mřížka **Statistiky výkonu** také ukazuje, že aktuální model mapování duplikuje databázové požadavky, zatímco je spuštěn zdroj dat **\#Vend**.</span><span class="sxs-lookup"><span data-stu-id="f8277-177">The **Performance statistics** grid also shows that the current model mapping duplicates database requests while the **\#Vend** data source is run.</span></span> <span data-ttu-id="f8277-178">Tato duplikace se vyskytuje z následujících důvodů:</span><span class="sxs-lookup"><span data-stu-id="f8277-178">This duplication occurs for the following reasons:</span></span>

- <span data-ttu-id="f8277-179">Tabulka dodavatele je volána dvakrát pro každou z 265 iterovaných transakcí dodavatele, celkem tedy 530 volání:</span><span class="sxs-lookup"><span data-stu-id="f8277-179">The vendor table is called two times for each of the 265 iterated vendor transactions, for a total of 530 calls:</span></span>

    - <span data-ttu-id="f8277-180">Jedním voláním se zadá číslo účtu dodavatele.</span><span class="sxs-lookup"><span data-stu-id="f8277-180">One call is made to enter the vendor account number.</span></span>
    - <span data-ttu-id="f8277-181">Jedním voláním se zadá název dodavatele.</span><span class="sxs-lookup"><span data-stu-id="f8277-181">One call is made to enter the vendor name.</span></span>

- <span data-ttu-id="f8277-182">Tabulka dodavatelů je volána pro každou iterovanou transakci dodavatele, přestože načtené transakce byly zaúčtovány pouze pro pět dodavatelů.</span><span class="sxs-lookup"><span data-stu-id="f8277-182">The vendor table is called for each iterated vendor transaction, even though the fetched transactions have been posted for only five vendors.</span></span> <span data-ttu-id="f8277-183">Z 530 hovorů je 525 duplikátů.</span><span class="sxs-lookup"><span data-stu-id="f8277-183">Of the 530 calls, 525 are duplicates.</span></span> <span data-ttu-id="f8277-184">Následující obrázek ukazuje zprávu, kterou obdržíte o duplicitních voláních (databázové požadavky).</span><span class="sxs-lookup"><span data-stu-id="f8277-184">The following illustration shows the message that you receive about duplicate calls (database requests).</span></span>

![Zpráva o duplicitních žádostech databáze na stránce návrháře mapování modelu](./media/er-calculated-field-ds-performance-mapping-2a.png)

<span data-ttu-id="f8277-186">Z celkové doby provedení mapování modelu (přibližně osm sekund) si všimněte, že více než 80 procent (přibližně šest sekund) bylo vynaloženo na načtení hodnot z tabulky aplikace VendTable.</span><span class="sxs-lookup"><span data-stu-id="f8277-186">Of the total model mapping execution time (approximately eight seconds), notice that more than 80 percent (approximately six seconds) has been spent retrieving values from the VendTable application table.</span></span> <span data-ttu-id="f8277-187">Toto procento je příliš vysoké pro dva atributy pěti dodavatelů ve srovnání s objemem informací z tabulky aplikace VendTrans.</span><span class="sxs-lookup"><span data-stu-id="f8277-187">That percentage is too large for two attributes of five vendors, compared with the volume of information from the VendTrans application table.</span></span>

<span data-ttu-id="f8277-188">Chcete-li snížit počet volání, abyste získali podrobnosti o dodavateli pro každou transakci a zlepšili výkon mapování modelu, můžete použít ukládání do mezipaměti pro zdroj dat **\#Vend**.</span><span class="sxs-lookup"><span data-stu-id="f8277-188">To reduce the number of calls that are made to get the vendor details for every transaction, and to improve the performance of the model mapping, you can use caching for the **\#Vend** data source.</span></span>

> [!NOTE]
> <span data-ttu-id="f8277-189">Zdroj dat **Trans\\\#Vend** bude uložen do mezipaměti v rozsahu aktuální transakce zdroje dat **Trans** za běhu.</span><span class="sxs-lookup"><span data-stu-id="f8277-189">The **Trans\\\#Vend** data source will be cached in the scope of the current transaction of the **Trans** data source at runtime.</span></span>

<span data-ttu-id="f8277-190">Uložením zdroje dat **\#Vend** do mezipaměti snížíte počet duplicitních hovorů z 525 na 260, ale duplikaci zcela neodstraníte.</span><span class="sxs-lookup"><span data-stu-id="f8277-190">By caching the **\#Vend** data source, you reduce the number of duplicated calls from 525 to 260, but you don't completely eliminate the duplication.</span></span> <span data-ttu-id="f8277-191">Chcete-li zcela vyloučit duplikaci, můžete nakonfigurovat nový parametrizovaný zdroj dat typu **Počítané pole**.</span><span class="sxs-lookup"><span data-stu-id="f8277-191">To completely eliminate duplication, you can configure a new parameterized data source of the **Calculated field** type.</span></span>

## <a name="improve-the-model-mapping-based-on-information-from-the-execution-trace"></a><span data-ttu-id="f8277-192">Vylepšení mapování modelu na základě informací ze sledování provádění</span><span class="sxs-lookup"><span data-stu-id="f8277-192">Improve the model mapping based on information from the execution trace</span></span>

### <a name="change-the-logic-of-the-model-mapping"></a><span data-ttu-id="f8277-193">Změna logiky mapování modelu</span><span class="sxs-lookup"><span data-stu-id="f8277-193">Change the logic of the model mapping</span></span>

<span data-ttu-id="f8277-194">Pomocí těchto kroků můžete použít ukládání zdroje dat typu **Počítané pole** do mezipaměti, aby se zabránilo duplicitním voláním do databáze.</span><span class="sxs-lookup"><span data-stu-id="f8277-194">Follow these steps to use caching and a data source of the **Calculated field** type, to help prevent duplicate calls to the database.</span></span>

1. <span data-ttu-id="f8277-195">Na stránce **Konfigurace** ve stromové struktuře konfigurace vyberte položku **Mapování zlepšení výkonu**.</span><span class="sxs-lookup"><span data-stu-id="f8277-195">On the **Configurations** page, in the configuration tree, select **Performance improvement mapping**.</span></span>
2. <span data-ttu-id="f8277-196">V podokně akcí zvolte **Návrhář**.</span><span class="sxs-lookup"><span data-stu-id="f8277-196">On the Action Pane, select **Designer**.</span></span>
3. <span data-ttu-id="f8277-197">Na stránce **Mapování modelu** v podokně Akce vyberte možnost **Návrhář**.</span><span class="sxs-lookup"><span data-stu-id="f8277-197">On the **Model mappings** page, on the Action Pane, select **Designer**.</span></span>
4. <span data-ttu-id="f8277-198">Na stránce **Návrhář mapování modelů** postupujte podle těchto kroků, abyste přidali zdroj dat typu **Záznamy tabulky** pro přístup k záznamům v tabulce aplikace VendTable:</span><span class="sxs-lookup"><span data-stu-id="f8277-198">On the **Model mapping designer** page, follow these steps to add a data source of the **Table records** type to access records in the VendTable application table:</span></span>

    1. <span data-ttu-id="f8277-199">V podokně **Typy zdrojů dat** rozbalte **Dynamics 365 for Operations** a vyberte **Záznamy tabulky**.</span><span class="sxs-lookup"><span data-stu-id="f8277-199">In the **Data source types** pane, expand **Dynamics 365 for Operations**, and select **Table records**.</span></span>
    2. <span data-ttu-id="f8277-200">Vyberte **Přidat kořen**.</span><span class="sxs-lookup"><span data-stu-id="f8277-200">Select **Add root**.</span></span>
    3. <span data-ttu-id="f8277-201">V dialogovém okně do pole **Název** zadejte **Vend**.</span><span class="sxs-lookup"><span data-stu-id="f8277-201">In the dialog box, in the **Name** field, enter **Vend**.</span></span>
    4. <span data-ttu-id="f8277-202">Do pole **Tabulka** zadejte **VendTable**.</span><span class="sxs-lookup"><span data-stu-id="f8277-202">In the **Table** field, enter **VendTable**.</span></span>
    5. <span data-ttu-id="f8277-203">Vyberte **OK**.</span><span class="sxs-lookup"><span data-stu-id="f8277-203">Select **OK**.</span></span>

5. <span data-ttu-id="f8277-204">Můžete parametrizovat volání zdrojů dat typu **Počítané pole**, pouze pokud jsou tyto zdroje dat umístěny v kontejneru.</span><span class="sxs-lookup"><span data-stu-id="f8277-204">You can parameterize calls to data sources of the **Calculated field** type only if those data sources reside in a container.</span></span> <span data-ttu-id="f8277-205">Proto podle těchto pokynů přidejte zdroj dat typu **Prázdný kontejner** pro uchování nového parametrizovaného zdroje dat typu **Počítané pole**:</span><span class="sxs-lookup"><span data-stu-id="f8277-205">Therefore, follow these steps to add a data source of the **Empty container** type to hold a new parameterized data source of the **Calculated field** type:</span></span>

    1. <span data-ttu-id="f8277-206">V podokně **Typy zdrojů dat** rozbalte **Obecné** a vyberte **Prázdný kontejner**.</span><span class="sxs-lookup"><span data-stu-id="f8277-206">In the **Data source types** pane, expand **General**, and select **Empty container**.</span></span>
    2. <span data-ttu-id="f8277-207">Vyberte **Přidat kořen**.</span><span class="sxs-lookup"><span data-stu-id="f8277-207">Select **Add root**.</span></span>
    3. <span data-ttu-id="f8277-208">V dialogovém okně do pole **Název** zadejte **Box**.</span><span class="sxs-lookup"><span data-stu-id="f8277-208">In the dialog box, in the **Name** field, enter **Box**.</span></span>
    3. <span data-ttu-id="f8277-209">Vyberte **OK**.</span><span class="sxs-lookup"><span data-stu-id="f8277-209">Select **OK**.</span></span>

    ![Zdroj dat Box na stránce návrháře mapování modelů](./media/er-calculated-field-ds-performance-mapping-3.png)

6. <span data-ttu-id="f8277-211">Pomocí těchto kroků přidáte parametrizovaný zdroj dat typu **Počítané pole**:</span><span class="sxs-lookup"><span data-stu-id="f8277-211">Follow these steps to add a parameterized data source of the **Calculated field** type:</span></span>

    1. <span data-ttu-id="f8277-212">V podokně **Zdroje dat** vyberte **Box**.</span><span class="sxs-lookup"><span data-stu-id="f8277-212">In the **Data sources** pane, select **Box**.</span></span>
    2. <span data-ttu-id="f8277-213">V podokně **Typy zdrojů dat** rozbalte **Funkce** a vyberte **Počítané pole**.</span><span class="sxs-lookup"><span data-stu-id="f8277-213">In the **Data source types** pane, expand **Functions**, and select **Calculated field**.</span></span>
    3. <span data-ttu-id="f8277-214">Vyberte **přidat**.</span><span class="sxs-lookup"><span data-stu-id="f8277-214">Select **Add**.</span></span>
    4. <span data-ttu-id="f8277-215">V dialogovém okně do pole **Název** zadejte **Vend**.</span><span class="sxs-lookup"><span data-stu-id="f8277-215">In the dialog box, in the **Name** field, enter **Vend**.</span></span>
    5. <span data-ttu-id="f8277-216">Vyberte možnost **Upravit vzorec**.</span><span class="sxs-lookup"><span data-stu-id="f8277-216">Select **Edit formula**.</span></span>
    6. <span data-ttu-id="f8277-217">Na stránce **Návrhář vzorců** vyberte **Parametry** k určení parametrů, které je nutné zadat při volání tohoto zdroje dat.</span><span class="sxs-lookup"><span data-stu-id="f8277-217">On the **Formula designer** page, select **Parameters** to specify the parameters that must be provided when this data source is called.</span></span>
    7. <span data-ttu-id="f8277-218">V dialogovém okně **Parametry** vyberte **Nový**.</span><span class="sxs-lookup"><span data-stu-id="f8277-218">In the **Parameters** dialog box, select **New**.</span></span>
    8. <span data-ttu-id="f8277-219">Do pole **Název** zadejte **parmVendAccNumber**.</span><span class="sxs-lookup"><span data-stu-id="f8277-219">In the **Name** field, enter **parmVendAccNumber**.</span></span>
    9. <span data-ttu-id="f8277-220">V poli **Typ** vyberte **Řetězec**.</span><span class="sxs-lookup"><span data-stu-id="f8277-220">In the **Type** field, select **String**.</span></span>
    10. <span data-ttu-id="f8277-221">Vyberte **OK**.</span><span class="sxs-lookup"><span data-stu-id="f8277-221">Select **OK**.</span></span>
    11. <span data-ttu-id="f8277-222">V poli **Vzorec** zadejte **FIRSTORNULL(FILTER(Vend, Vend.AccountNum=parmVendAccNumber))**.</span><span class="sxs-lookup"><span data-stu-id="f8277-222">In the **Formula** field, enter **FIRSTORNULL(FILTER(Vend, Vend.AccountNum=parmVendAccNumber))**.</span></span>
    12. <span data-ttu-id="f8277-223">Vyberte **Uložit** a zavřete stránku **Návrhář vzorců**.</span><span class="sxs-lookup"><span data-stu-id="f8277-223">Select **Save**, and close the **Formula designer** page.</span></span>
    13. <span data-ttu-id="f8277-224">Vyberte **OK** pro přidání nového zdroje dat.</span><span class="sxs-lookup"><span data-stu-id="f8277-224">Select **OK** to add the new data source.</span></span>

7. <span data-ttu-id="f8277-225">Chcete-li během provádění označit přidaný zdroj dat, že je v mezipaměti, postupujte takto:</span><span class="sxs-lookup"><span data-stu-id="f8277-225">Follow these steps to mark the added data source as cached during the execution:</span></span>

    1. <span data-ttu-id="f8277-226">V podokně **Zdroje dat** vyberte **Box\\Vend**.</span><span class="sxs-lookup"><span data-stu-id="f8277-226">In the **Data sources** pane, select **Box\\Vend**.</span></span>
    2. <span data-ttu-id="f8277-227">Vyberte **Mezipaměť**.</span><span class="sxs-lookup"><span data-stu-id="f8277-227">Select **Cache**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="f8277-228">Zdroj dat **Box\\Vend** bude uložen do mezipaměti v rozsahu všech transakcí dodavatele zdroje dat **Trans** za běhu.</span><span class="sxs-lookup"><span data-stu-id="f8277-228">The **Box\\Vend** data source will be cached in the scope of all vendor transactions of the **Trans** data source at runtime.</span></span>

8. <span data-ttu-id="f8277-229">Podle těchto pokynů aktualizujte vnořený zdroj dat **Trans\\\#Vend** tak, že používá zdroj dat **Box\\Vend**:</span><span class="sxs-lookup"><span data-stu-id="f8277-229">Follow these steps to update the nested **Trans\\\#Vend** data source so that it uses the **Box\\Vend** data source:</span></span>

    1. <span data-ttu-id="f8277-230">V podokně **Zdroje dat** rozbalte **Trans**.</span><span class="sxs-lookup"><span data-stu-id="f8277-230">In the **Data sources** pane, expand **Trans**.</span></span>
    2. <span data-ttu-id="f8277-231">Vyberte zdroj dat **Trans\\\#Vend** a poté vyberte **Upravit** \> **Upravit vzorec**.</span><span class="sxs-lookup"><span data-stu-id="f8277-231">Select the **Trans\\\#Vend** data source, and then select **Edit** \> **Edit formula**.</span></span>
    3. <span data-ttu-id="f8277-232">Na stránce **Návrhář vzorců** v poli **Vzorec** zadejte **Box.Vend(\@.AccountNum)**.</span><span class="sxs-lookup"><span data-stu-id="f8277-232">On the **Formula designer** page, in the **Formula** field, enter **Box.Vend(\@.AccountNum)**.</span></span>
    4. <span data-ttu-id="f8277-233">Vyberte **Uložit** a poté zavřete stránku **Návrhář vzorců**.</span><span class="sxs-lookup"><span data-stu-id="f8277-233">Select **Save**, and then close the **Formula designer** page.</span></span>
    5. <span data-ttu-id="f8277-234">Tlačítkem **OK** dokončíte změny ve vybraném zdroji dat.</span><span class="sxs-lookup"><span data-stu-id="f8277-234">Select **OK** to complete your changes to the selected data source.</span></span>

9. <span data-ttu-id="f8277-235">Zvolte **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="f8277-235">Select **Save**.</span></span>

    ![Zdroj dat Vend na stránce návrháře mapování modelů](./media/er-calculated-field-ds-performance-mapping-4.png)

10. <span data-ttu-id="f8277-237">Zavřete stránku **Návrhář mapování modelu**.</span><span class="sxs-lookup"><span data-stu-id="f8277-237">Close the **Model mapping designer** page.</span></span>
11. <span data-ttu-id="f8277-238">Zavřete stránku **Mapování modelu**.</span><span class="sxs-lookup"><span data-stu-id="f8277-238">Close the **Model mappings** page.</span></span>

### <a name="complete-the-modified-version-of-the-er-model-mapping"></a><span data-ttu-id="f8277-239">Dokončení upravené verze mapování modelu elektronického výkaznictví</span><span class="sxs-lookup"><span data-stu-id="f8277-239">Complete the modified version of the ER model mapping</span></span>

1. <span data-ttu-id="f8277-240">Na stránce **Konfigurace** na záložce s náhledem **Verze** vyberte verzi **1.2** konfigurace **Mapování zlepšení výkonu**.</span><span class="sxs-lookup"><span data-stu-id="f8277-240">On the **Configurations** page, on the **Versions** FastTab, select version **1.2** of the **Performance improvement mapping** configuration.</span></span>
2. <span data-ttu-id="f8277-241">Vyberte **Změnit stav** \> **Dokončit** a poté vyberte **OK**.</span><span class="sxs-lookup"><span data-stu-id="f8277-241">Select **Change status** \> **Complete**, and then select **OK**.</span></span>

## <a name="run-the-modified-er-solution-to-trace-execution"></a><span data-ttu-id="f8277-242">Spuštění upraveného řešení elektronického výkaznictví pro sledování provádění</span><span class="sxs-lookup"><span data-stu-id="f8277-242">Run the modified ER solution to trace execution</span></span>

<span data-ttu-id="f8277-243">Opakujte kroky v části [Spuštění formátu elektronického výkaznictví](#run-format) výše v tomto tématu, pro vygenerování nového sledování výkonu.</span><span class="sxs-lookup"><span data-stu-id="f8277-243">Repeat the steps in the [Run the ER format](#run-format) section earlier in this topic to generate a new performance trace.</span></span>

## <a name="use-the-performance-trace-to-analyze-adjustments-to-the-model-mapping"></a><span data-ttu-id="f8277-244">Použití sledování výkonu k analýze úprav mapování modelů</span><span class="sxs-lookup"><span data-stu-id="f8277-244">Use the performance trace to analyze adjustments to the model mapping</span></span> 

1. <span data-ttu-id="f8277-245">Na stránce **Konfigurace** ve stromové struktuře konfigurace vyberte položku **Mapování zlepšení výkonu**.</span><span class="sxs-lookup"><span data-stu-id="f8277-245">On the **Configurations** page, in the configuration tree, select **Performance improvement mapping**.</span></span>
2. <span data-ttu-id="f8277-246">V podokně akcí zvolte **Návrhář**.</span><span class="sxs-lookup"><span data-stu-id="f8277-246">On the Action Pane, select **Designer**.</span></span>
3. <span data-ttu-id="f8277-247">Na stránce **Mapování modelu** v podokně Akce vyberte možnost **Návrhář**.</span><span class="sxs-lookup"><span data-stu-id="f8277-247">On the **Model mappings** page, on the Action Pane, select **Designer**.</span></span>
4. <span data-ttu-id="f8277-248">Na stránce **Návrhář mapování modelu** v podokně akcí vyberte **Sledování výkonu**.</span><span class="sxs-lookup"><span data-stu-id="f8277-248">On the **Model mapping designer** page, on the Action Pane, select **Performance trace**.</span></span>
5. <span data-ttu-id="f8277-249">Vyberte nejnovější sledování, které bylo vygenerováno, a poté vyberte **OK**.</span><span class="sxs-lookup"><span data-stu-id="f8277-249">Select the most recent trace that was generated, and then select **OK**.</span></span>

<span data-ttu-id="f8277-250">Všimněte si, že úpravy provedené v mapování modelu odstranily duplicitní dotazy do databáze.</span><span class="sxs-lookup"><span data-stu-id="f8277-250">Notice that the adjustments that you made to the model mapping have eliminated duplicate queries to database.</span></span> <span data-ttu-id="f8277-251">Počet volání databázových tabulek a zdrojů dat pro toto mapování modelu byl snížen.</span><span class="sxs-lookup"><span data-stu-id="f8277-251">The number of calls to database tables and data sources for this model mapping has also been reduced.</span></span>

![Informace o sledování na stránce Návrhář mapování modelů 1](./media/er-calculated-field-ds-performance-mapping-5.png)

<span data-ttu-id="f8277-253">Celková doba provedení byla snížena přibližně 20krát (z přibližně 8 sekund na přibližně 400 milisekund).</span><span class="sxs-lookup"><span data-stu-id="f8277-253">The total execution time has been reduced about 20 times (from about 8 seconds to about 400 milliseconds).</span></span> <span data-ttu-id="f8277-254">Z toho vyplývá zvýšení výkonu celého řešení elektronického výkaznictví.</span><span class="sxs-lookup"><span data-stu-id="f8277-254">Therefore, the performance of the whole ER solution has been improved.</span></span>

![Informace o sledování na stránce Návrhář mapování modelů 2](./media/er-calculated-field-ds-performance-mapping-5a.png)

## <a name="appendix-1-download-the-components-of-the-sample-microsoft-er-solution"></a><a name="appendix1"></a><span data-ttu-id="f8277-256">Příloha 1: Stáhněte si součásti ukázkového řešení elektronického výkaznictví Microsoft</span><span class="sxs-lookup"><span data-stu-id="f8277-256">Appendix 1: Download the components of the sample Microsoft ER solution</span></span>

<span data-ttu-id="f8277-257">Je nutné stáhnout a místně uložit následující soubory.</span><span class="sxs-lookup"><span data-stu-id="f8277-257">You must download the following files and store them locally.</span></span>

| <span data-ttu-id="f8277-258">Soubor</span><span class="sxs-lookup"><span data-stu-id="f8277-258">File</span></span>                                        | <span data-ttu-id="f8277-259">Obsah</span><span class="sxs-lookup"><span data-stu-id="f8277-259">Content</span></span> |
|---------------------------------------------|---------|
| <span data-ttu-id="f8277-260">Performance improvement model.version.1</span><span class="sxs-lookup"><span data-stu-id="f8277-260">Performance improvement model.version.1</span></span>     | [<span data-ttu-id="f8277-261">Vzorová konfigurace datového modelu elektronického výkaznictví</span><span class="sxs-lookup"><span data-stu-id="f8277-261">Sample ER data model configuration</span></span>](https://mbs.microsoft.com/customersource/Global/AX/downloads/hot-fixes/365optelecrepeg) |
| <span data-ttu-id="f8277-262">Performance improvement mapping.version.1.1</span><span class="sxs-lookup"><span data-stu-id="f8277-262">Performance improvement mapping.version.1.1</span></span> | [<span data-ttu-id="f8277-263">Vzorová konfigurace mapování elektronického výkaznictví</span><span class="sxs-lookup"><span data-stu-id="f8277-263">Sample ER model mapping configuration</span></span>](https://mbs.microsoft.com/customersource/Global/AX/downloads/hot-fixes/365optelecrepeg) |
| <span data-ttu-id="f8277-264">Performance improvement format.version.1.1</span><span class="sxs-lookup"><span data-stu-id="f8277-264">Performance improvement format.version.1.1</span></span>  | [<span data-ttu-id="f8277-265">Vzorová konfigurace formátu elektronického výkaznictví</span><span class="sxs-lookup"><span data-stu-id="f8277-265">Sample ER format configuration</span></span>](https://mbs.microsoft.com/customersource/Global/AX/downloads/hot-fixes/365optelecrepeg) |

## <a name="appendix-2-configure-the-er-framework"></a><a name="appendix2"></a><span data-ttu-id="f8277-266">Příloha 2: Konfigurace architektury elektronického výkaznictví</span><span class="sxs-lookup"><span data-stu-id="f8277-266">Appendix 2: Configure the ER framework</span></span>

<span data-ttu-id="f8277-267">Než začnete používat architekturu elektronického výkaznictví ke zlepšení výkonu ukázkového řešení elektronického výkaznictví Microsoft, musíte nakonfigurovat minimální sadu parametrů elektronického výkaznictví.</span><span class="sxs-lookup"><span data-stu-id="f8277-267">Before you can start to use the ER framework to improve the performance of the sample Microsoft ER solution, you must configure the minimal set of ER parameters.</span></span>

### <a name="configure-er-parameters"></a><a id="ConfigureParameters"></a><span data-ttu-id="f8277-268">Konfigurace parametrů elektronického výkaznictví</span><span class="sxs-lookup"><span data-stu-id="f8277-268">Configure ER parameters</span></span>

1. <span data-ttu-id="f8277-269">Přejděte do části **Správa organizace** \> **Pracovní prostory** \> **Elektronické výkaznictví**.</span><span class="sxs-lookup"><span data-stu-id="f8277-269">Go to **Organization administration** \> **Workspaces** \> **Electronic reporting**.</span></span>
2. <span data-ttu-id="f8277-270">Na stránce **Konfigurace lokalizace** vyberte v části **Související odkazy** možnost **Parametry elektronického výkaznictví**.</span><span class="sxs-lookup"><span data-stu-id="f8277-270">On the **Localization configurations** page, in the **Related links** section, select **Electronic reporting parameters**.</span></span>
3. <span data-ttu-id="f8277-271">Na stránce **Parametry elektronického výkaznictví** nastavte na kartě **Obecné** u možnosti **Povolit režim návrhu** hodnotu **Ano**.</span><span class="sxs-lookup"><span data-stu-id="f8277-271">On the **Electronic reporting parameters** page, on the **General** tab, set the **Enable design mode** option to **Yes**.</span></span>
4. <span data-ttu-id="f8277-272">Na kartě **Přílohy** natavte následující parametry:</span><span class="sxs-lookup"><span data-stu-id="f8277-272">On the **Attachments** tab, set the following parameters:</span></span>

    - <span data-ttu-id="f8277-273">V poli **Konfigurace** vyberte pro společnost **DEMF** typ **Soubor**.</span><span class="sxs-lookup"><span data-stu-id="f8277-273">In the **Configurations** field, select the **File** type for the **DEMF** company.</span></span>
    - <span data-ttu-id="f8277-274">V polích **Archiv úloh**, **Dočasné**, **Základ** a **Ostatní** vyberte typ **souboru**.</span><span class="sxs-lookup"><span data-stu-id="f8277-274">In the **Job archive**, **Temporary**, **Baseline**, and **Others** fields, select the **File** type.</span></span>

<span data-ttu-id="f8277-275">Další informace o parametrech elektronického výkaznictví najdete v tématu [Konfigurace rámce elektronického výkaznictví](electronic-reporting-er-configure-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="f8277-275">For more information about ER parameters, see [Configure the ER framework](electronic-reporting-er-configure-parameters.md).</span></span>

### <a name="activate-an-er-configuration-provider"></a><a id="ActivateProvider"></a><span data-ttu-id="f8277-276">Aktivace poskytovatele konfigurace elektronického výkaznictví</span><span class="sxs-lookup"><span data-stu-id="f8277-276">Activate an ER configuration provider</span></span>

<span data-ttu-id="f8277-277">U každé přidané konfigurace elektronického výkaznictví je vyznačen jako vlastník poskytovatel konfigurace elektronického výkaznictví.</span><span class="sxs-lookup"><span data-stu-id="f8277-277">Every ER configuration that is added is marked as owned by an ER configuration provider.</span></span> <span data-ttu-id="f8277-278">Pro tyto účely se používá poskytovatel konfigurace elektronického výkaznictví, který je aktivován v pracovním prostoru **Elektronické výkaznictví**.</span><span class="sxs-lookup"><span data-stu-id="f8277-278">The ER configuration provider that is activated in the **Electronic reporting** workspace is used for this purpose.</span></span> <span data-ttu-id="f8277-279">Než začnete přidávat nebo upravovat konfigurace elektronického výkaznictví, musíte proto aktivovat poskytovatele konfigurace elektronického výkaznictví v pracovním prostoru **Elektronické výkaznictví**.</span><span class="sxs-lookup"><span data-stu-id="f8277-279">Therefore, you must activate an ER configuration provider in the **Electronic reporting** workspace before you start to add or edit ER configurations.</span></span>

> [!NOTE]
> <span data-ttu-id="f8277-280">Pouze vlastník konfigurace elektronického výkaznictví může konfiguraci upravovat.</span><span class="sxs-lookup"><span data-stu-id="f8277-280">Only the owner of an ER configuration can edit the configuration.</span></span> <span data-ttu-id="f8277-281">Konfiguraci elektronického výkaznictví proto můžete upravovat teprve poté, co je příslušná konfigurace elektronického výkaznictví aktivována v pracovním prostoru **Elektronické výkaznictví**.</span><span class="sxs-lookup"><span data-stu-id="f8277-281">Therefore, before an ER configuration can be edited, the appropriate ER configuration provider must be activated in the **Electronic reporting** workspace.</span></span>

#### <a name="review-the-list-of-er-configuration-providers"></a><a id="ReviewProvidersList"></a><span data-ttu-id="f8277-282">Kontrola seznamu poskytovatelů konfigurace elektronického výkaznictví</span><span class="sxs-lookup"><span data-stu-id="f8277-282">Review the list of ER configuration providers</span></span>

1. <span data-ttu-id="f8277-283">Přejděte do části **Správa organizace** \> **Pracovní prostory** \> **Elektronické výkaznictví**.</span><span class="sxs-lookup"><span data-stu-id="f8277-283">Go to **Organization administration** \> **Workspaces** \> **Electronic reporting**.</span></span>
2. <span data-ttu-id="f8277-284">Na stránce **Konfigurace lokalizace** v části **Související odkazy** vyberte možnost **Poskytovatelé konfigurací**.</span><span class="sxs-lookup"><span data-stu-id="f8277-284">On the **Localization configurations** page, in the **Related links** section, select **Configuration providers**.</span></span>
3. <span data-ttu-id="f8277-285">Na stránce **Tabulka poskytovatelů konfigurací** má záznam každého poskytovatele jedinečný název a adresu URL.</span><span class="sxs-lookup"><span data-stu-id="f8277-285">On the **Configuration provider table** page, each provider record has a unique name and URL.</span></span> <span data-ttu-id="f8277-286">Zkontrolujte obsah této stránky.</span><span class="sxs-lookup"><span data-stu-id="f8277-286">Review the contents of this page.</span></span> <span data-ttu-id="f8277-287">Pokud již existuje záznam **Litware, Inc.**, další postup, [Přidání nového poskytovatele konfigurace elektronického výkaznictví](#ActivateProvider), přeskočte.</span><span class="sxs-lookup"><span data-stu-id="f8277-287">If a record for **Litware, Inc.** already exists, skip the next procedure, [Add a new ER configuration provider](#ActivateProvider).</span></span>

#### <a name="add-a-new-er-configuration-provider"></a><a id="ActivateProvider"></a><span data-ttu-id="f8277-288">Přidání nového poskytovatele konfigurace elektronického výkaznictví</span><span class="sxs-lookup"><span data-stu-id="f8277-288">Add a new ER configuration provider</span></span>

1. <span data-ttu-id="f8277-289">Přejděte do části **Správa organizace** \> **Pracovní prostory** \> **Elektronické výkaznictví**.</span><span class="sxs-lookup"><span data-stu-id="f8277-289">Go to **Organization administration** \> **Workspaces** \> **Electronic reporting**.</span></span>
2. <span data-ttu-id="f8277-290">Na stránce **Konfigurace lokalizace** v části **Související odkazy** vyberte možnost **Poskytovatelé konfigurací**.</span><span class="sxs-lookup"><span data-stu-id="f8277-290">On the **Localization configurations** page, in the **Related links** section, select **Configuration providers**.</span></span>
3. <span data-ttu-id="f8277-291">Na stránce **Poskytovatelé konfigurace** zvolte **Nový**.</span><span class="sxs-lookup"><span data-stu-id="f8277-291">On the **Configuration providers** page, select **New**.</span></span>
4. <span data-ttu-id="f8277-292">Do pole **Název** zadejte **Litware, Inc.**</span><span class="sxs-lookup"><span data-stu-id="f8277-292">In the **Name** field, enter **Litware, Inc.**</span></span>
5. <span data-ttu-id="f8277-293">Do pole **Internetová adresa** zadejte `https://www.litware.com`.</span><span class="sxs-lookup"><span data-stu-id="f8277-293">In the **Internet address** field, enter `https://www.litware.com`.</span></span>
6. <span data-ttu-id="f8277-294">Zvolte **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="f8277-294">Select **Save**.</span></span>

#### <a name="activate-an-er-configuration-provider"></a><a id="ActivateAddedProvider"></a><span data-ttu-id="f8277-295">Aktivace poskytovatele konfigurace elektronického výkaznictví</span><span class="sxs-lookup"><span data-stu-id="f8277-295">Activate an ER configuration provider</span></span>

1. <span data-ttu-id="f8277-296">Přejděte do části **Správa organizace** \> **Pracovní prostory** \> **Elektronické výkaznictví**.</span><span class="sxs-lookup"><span data-stu-id="f8277-296">Go to **Organization administration** \> **Workspaces** \> **Electronic reporting**.</span></span>
2. <span data-ttu-id="f8277-297">Na stránce **Konfigurace lokalizace** klikněte v části **Poskytovatelé konfigurací** na dlaždici **Litware, Inc.** a poté vyberte možnost **Nastavit jako aktivní**.</span><span class="sxs-lookup"><span data-stu-id="f8277-297">On the **Localization configurations** page, in the **Configuration providers** section, select the **Litware, Inc.** tile, and then select **Set active**.</span></span>

<span data-ttu-id="f8277-298">Další informace o poskytovatelích konfigurací elektronického výkaznictví naleznete v tématu [Vytvoření poskytovatelů konfigurací a jejich označení jako aktivních](tasks/er-configuration-provider-mark-it-active-2016-11.md).</span><span class="sxs-lookup"><span data-stu-id="f8277-298">For more information about ER configuration providers, see [Create configuration providers and mark them as active](tasks/er-configuration-provider-mark-it-active-2016-11.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="f8277-299">Další prostředky</span><span class="sxs-lookup"><span data-stu-id="f8277-299">Additional resources</span></span>

- [<span data-ttu-id="f8277-300">Přehled elektronického výkaznictví</span><span class="sxs-lookup"><span data-stu-id="f8277-300">Electronic Reporting overview</span></span>](general-electronic-reporting.md)
- [<span data-ttu-id="f8277-301">Sledování provedení formátů elektronického výkaznictví pro při řešení problémů s výkonem</span><span class="sxs-lookup"><span data-stu-id="f8277-301">Trace the execution of ER formats to troubleshoot performance issues</span></span>](trace-execution-er-troubleshoot-perf.md)
- [<span data-ttu-id="f8277-302">Podpora parametrizovaných volání zdrojů dat elektronického výkaznictví typu vypočítaného pole</span><span class="sxs-lookup"><span data-stu-id="f8277-302">Support parameterized calls of ER data sources of the Calculated field type</span></span>](er-calculated-field-type.md)
