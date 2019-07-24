---
title: Vylepšení ve sledování výsledků vygenerovaných sestav elektronického výkaznictví a jejich porovnání s hodnotami směrného plánu
description: Toto téma obsahuje informace o tom, jak byla vylepšena funkce směrného plánu ER v aplikaci Microsoft Dynamics 365 for Finance and Operations verze 10.0.3 (červen 2019) vylepšena.
author: NickSelin
manager: AnnBe
ms.date: 06/19/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 220314
ms.assetid: 2685df16-5ec8-4fd7-9495-c0f653e82567
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2018-04-01
ms.dyn365.ops.version: Release 8.0
ms.openlocfilehash: 222a415f686c8028fc2a414f97eed0291d850ae7
ms.sourcegitcommit: 9917df8c0c9320955c61186cd922c8df894a4f25
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/21/2019
ms.locfileid: "1700675"
---
# <a name="improvements-in-tracing-the-results-of-generated-er-reports-and-comparing-them-with-baseline-values"></a><span data-ttu-id="52d50-103">Vylepšení ve sledování výsledků vygenerovaných sestav elektronického výkaznictví a jejich porovnání s hodnotami směrného plánu</span><span class="sxs-lookup"><span data-stu-id="52d50-103">Improvements in tracing the results of generated ER reports and comparing them with baseline values</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="52d50-104">V tomto tématu je popsána první sada vylepšení, která byla provedena ve funkci směrného plánu systému elektronického výkaznictví (ER).</span><span class="sxs-lookup"><span data-stu-id="52d50-104">This topic describes the first set of improvements that have been made to the baseline feature of the Electronic reporting (ER) framework.</span></span> <span data-ttu-id="52d50-105">Tato vylepšení jsou k dispozici v aplikaci Microsoft Dynamics 365 for Finance and Operations verze 10.0.3 (červen 2019) a novějších.</span><span class="sxs-lookup"><span data-stu-id="52d50-105">These improvements are available in Microsoft Dynamics 365 for Finance and Operations version 10.0.3 (June 2019) and later.</span></span>

## <a name="automate-the-setting-of-baseline-rules"></a><span data-ttu-id="52d50-106">Automatizace nastavení pravidel směrného plánu</span><span class="sxs-lookup"><span data-stu-id="52d50-106">Automate the setting of baseline rules</span></span>

<span data-ttu-id="52d50-107">Téma [Sledování generovaných výsledků sestav a jejich porovnání s hodnotami směrného plánu](er-trace-reports-compare-baseline.md) vysvětluje, jak konfigurovat rámec ER na shromažďování informací o spouštění formátu ER a vyhodnotit výsledky těchto spuštění.</span><span class="sxs-lookup"><span data-stu-id="52d50-107">The [Trace generated report results and compare them with baseline values](er-trace-reports-compare-baseline.md) topic explains how to configure the ER framework to collect information about ER format executions and evaluate the results of those executions.</span></span> <span data-ttu-id="52d50-108">Příklad v tomto tématu obsahuje kroky, které je nutné provést.</span><span class="sxs-lookup"><span data-stu-id="52d50-108">The example in this topic shows the steps that must be completed.</span></span>

<span data-ttu-id="52d50-109">Tady jsou některé kroky:</span><span class="sxs-lookup"><span data-stu-id="52d50-109">Here are some of the steps:</span></span>

- <span data-ttu-id="52d50-110">Chcete-li generovat odchozí soubor, spusťte formát ER a soubor uložte lokálně.</span><span class="sxs-lookup"><span data-stu-id="52d50-110">Run an ER format to generate an outbound file, and store the file locally.</span></span>
- <span data-ttu-id="52d50-111">Přidejte lokálně uložený soubor jako přílohu směrného plánu, který byl přidán do formátu ER.</span><span class="sxs-lookup"><span data-stu-id="52d50-111">Add the locally stored file as an attachment of the baseline that was added for an ER format.</span></span>
- <span data-ttu-id="52d50-112">Nakonfigurujte pravidlo směrného plánu pro přidaný směrný plán.</span><span class="sxs-lookup"><span data-stu-id="52d50-112">Configure the baseline rule for the added baseline.</span></span> <span data-ttu-id="52d50-113">Tato konfigurace zahrnuje následující kroky:</span><span class="sxs-lookup"><span data-stu-id="52d50-113">This configuration includes the following steps:</span></span>

    - <span data-ttu-id="52d50-114">Určete formátovací prvek ER, který slouží k vygenerování odchozího souboru.</span><span class="sxs-lookup"><span data-stu-id="52d50-114">Specify an ER format element that is used to generate an outbound file.</span></span>
    - <span data-ttu-id="52d50-115">Vyberte přílohu, která odkazuje na generovaný výstupní soubor.</span><span class="sxs-lookup"><span data-stu-id="52d50-115">Select the attachment that refers to the generated outbound file.</span></span>

> [!NOTE]
> <span data-ttu-id="52d50-116">Tyto kroky je nutné provést ručně, přestože nové schopnosti ER umožňují jejich automatizované provedení.</span><span class="sxs-lookup"><span data-stu-id="52d50-116">These steps must be done manually, even though the new ER capabilities enable them to be automated.</span></span> <span data-ttu-id="52d50-117">Chcete-li získat další informace o této funkci, vyplňte následující příklad.</span><span class="sxs-lookup"><span data-stu-id="52d50-117">To learn more about this feature, complete the following example.</span></span>

## <a name="example-automate-the-setting-of-baseline-rules"></a><span data-ttu-id="52d50-118">Příklad: Automatizace nastavení pravidel směrného plánu</span><span class="sxs-lookup"><span data-stu-id="52d50-118">Example: Automate the setting of baseline rules</span></span>

<span data-ttu-id="52d50-119">Chcete-li dokončit kroky v tomto příkladu, musíte nejprve dokončit kroky v příkladu v tématu [Sledování generovaných výsledků sestav a jejich porovnání s hodnotami směrného plánu](er-trace-reports-compare-baseline.md), a to až do části Přidání nového směrného plánu pro navržený formát ER.</span><span class="sxs-lookup"><span data-stu-id="52d50-119">To complete the steps in this example, you must first complete the steps in the example in the [Trace generated report results and compare them with baseline values](er-trace-reports-compare-baseline.md) topic, up through the "Add a new baseline for a designed ER format" section.</span></span>

### <a name="review-added-baseline"></a><span data-ttu-id="52d50-120">Kontrola přidaného směrného plánu</span><span class="sxs-lookup"><span data-stu-id="52d50-120">Review added baseline</span></span>

1. <span data-ttu-id="52d50-121">Přejděte do části **Správa organizace** \> **Elektronické výkaznictví** \> **Konfigurace**.</span><span class="sxs-lookup"><span data-stu-id="52d50-121">Go to **Organization administration** \> **Electronic reporting** \> **Configurations**.</span></span>
2. <span data-ttu-id="52d50-122">Vyberte **Směrné plány**.</span><span class="sxs-lookup"><span data-stu-id="52d50-122">Select **Baselines**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="52d50-123">Tlačítko **Směrný plán** v podokně akcí je k dispozici pouze v případě že je pro aktuální společnost zapnutý parametr ER **Spustit v režimu ladění**.</span><span class="sxs-lookup"><span data-stu-id="52d50-123">The **Baselines** button on the Action Pane is available only when the **Run in debug mode** ER user parameter is turned on for the current company.</span></span>

<span data-ttu-id="52d50-124">Směrný plán byl přidán k vybranému **Formátu pro osvojení si směrných plánů**, ale pravidla směrného plánu pro tento směrný plán ještě nebyla přidána.</span><span class="sxs-lookup"><span data-stu-id="52d50-124">The baseline has been added for the selected **Format to learn ER baselines** format, but the baseline rules haven't yet been added for this baseline.</span></span>

<span data-ttu-id="52d50-125">![Stránka směrného plánu formátu elektronického výkaznictví](media/GER-BaselineSample-AddBaseline2.PNG "Snímek obrazovky stránky směrného plánu formátu elektronického výkaznictví")</span><span class="sxs-lookup"><span data-stu-id="52d50-125">![Electronic reporting format baselines page](media/GER-BaselineSample-AddBaseline2.PNG "Screenshot of the Electronic reporting format baselines page")</span></span>

### <a name="make-a-new-baseline-rule"></a><span data-ttu-id="52d50-126">Vtvoření nového pravidla směrného plánu</span><span class="sxs-lookup"><span data-stu-id="52d50-126">Make a new baseline rule</span></span>

1. <span data-ttu-id="52d50-127">Přejděte do části **Správa organizace** \> **Elektronické výkaznictví** \> **Konfigurace**.</span><span class="sxs-lookup"><span data-stu-id="52d50-127">Go to **Organization administration** \> **Electronic reporting** \> **Configurations**.</span></span>
2. <span data-ttu-id="52d50-128">Ve stromové struktuře rozbalte **Model pro učení směrných plánů ER**.</span><span class="sxs-lookup"><span data-stu-id="52d50-128">In the tree, expand **Model to learn ER baselines**.</span></span>
3. <span data-ttu-id="52d50-129">Ve stromové struktuře vyberte **Model pro učení směrných plánů ER\\Formát pro učení směrných plánů ER**.</span><span class="sxs-lookup"><span data-stu-id="52d50-129">In the tree, select **Model to learn ER baselines\\Format to learn ER baselines**.</span></span>
4. <span data-ttu-id="52d50-130">Na pevné záložce **Verze** vyberte **Spustit**.</span><span class="sxs-lookup"><span data-stu-id="52d50-130">On the **Versions** FastTab, select **Run**.</span></span>
5. <span data-ttu-id="52d50-131">Do pole **Zadat ID** zadejte **1**.</span><span class="sxs-lookup"><span data-stu-id="52d50-131">In the **Enter Id** field, enter **1**.</span></span>
6. <span data-ttu-id="52d50-132">Nastavte volbu **vytvořit soubory směrného plánu** na **Ano**.</span><span class="sxs-lookup"><span data-stu-id="52d50-132">Set the **Make baseline files** option to **Yes**.</span></span>
7. <span data-ttu-id="52d50-133">Vyberte **OK**.</span><span class="sxs-lookup"><span data-stu-id="52d50-133">Select **OK**.</span></span>

    <span data-ttu-id="52d50-134">![Dialogové okno parametry elektronické sestavy](media/GER-BaselineSample-FormatRunToMakeBaselineFile3.PNG "– obrazovka dialogového okna parametry elektronické sestavy")</span><span class="sxs-lookup"><span data-stu-id="52d50-134">![Electronic report parameters dialog box](media/GER-BaselineSample-FormatRunToMakeBaselineFile3.PNG "Screenshot of the Electronic report parameters dialog box")</span></span>

8. <span data-ttu-id="52d50-135">Vyberte **Směrné plány**.</span><span class="sxs-lookup"><span data-stu-id="52d50-135">Select **Baselines**.</span></span>

    <span data-ttu-id="52d50-136">![Stránka směrného plánu formátu elektronického výkaznictví](media/GER-BaselineSample-ReviewAddedBaselineLine.PNG "Snímek obrazovky stránky směrného plánu formátu elektronického výkaznictví")</span><span class="sxs-lookup"><span data-stu-id="52d50-136">![Electronic reporting format baselines page](media/GER-BaselineSample-ReviewAddedBaselineLine.PNG "Screenshot of the Electronic reporting format baselines page")</span></span>

    <span data-ttu-id="52d50-137">Generovaný výstupní soubor byl automaticky připojen ke směrnému plánu provedeného formátu ER.</span><span class="sxs-lookup"><span data-stu-id="52d50-137">The generated outbound file has been automatically attached to the baseline of the executed ER format.</span></span> <span data-ttu-id="52d50-138">Do tohoto směrného plánu bylo automaticky přidáno pravidlo směrného plánu, které obsahuje také odkaz na připojený soubor.</span><span class="sxs-lookup"><span data-stu-id="52d50-138">The baseline rule has been automatically added to this baseline and also contains the reference to the attached file.</span></span>

9. <span data-ttu-id="52d50-139">Do pole **Název** zadejte **Směrný plán 1**.</span><span class="sxs-lookup"><span data-stu-id="52d50-139">In the **Name** field, enter **Baseline 1**.</span></span>
10. <span data-ttu-id="52d50-140">Do pole **Maska názvu souboru** zadejte **.xml**.</span><span class="sxs-lookup"><span data-stu-id="52d50-140">In the **File name mask** field, enter **.xml**.</span></span>
11. <span data-ttu-id="52d50-141">Zvolte **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="52d50-141">Select **Save**.</span></span>

### <a name="run-the-format"></a><span data-ttu-id="52d50-142">Spuštění formátu</span><span class="sxs-lookup"><span data-stu-id="52d50-142">Run the format</span></span>

<span data-ttu-id="52d50-143">Nyní můžete dokončit zbývající kroky v příkladu v tématu [Sledování generovaných výsledků sestavy a jejich porovnání s hodnotami směrného plánu](er-trace-reports-compare-baseline.md), počínaje částí Spuštění navrženého formátu ER a kontrola protokolu k analýze výsledků.</span><span class="sxs-lookup"><span data-stu-id="52d50-143">You're now ready to complete the remaining steps in the example in the [Trace generated report results and compare them with baseline values](er-trace-reports-compare-baseline.md) topic, starting from the "Run the designed ER format and review the log to analyze the results" section.</span></span>

> [!NOTE]
> <span data-ttu-id="52d50-144">Odstraníte-li automaticky přidané pravidlo směrného plánu na pevné záložce **Směrné plány**, odkazovaná příloha nebude automaticky odstraněna.</span><span class="sxs-lookup"><span data-stu-id="52d50-144">When you delete the automatically added baseline rule on the **Baselines** FastTab, the referenced attachment isn't automatically deleted.</span></span>

## <a name="configure-the-baseline-so-that-it-ignores-constantly-changing-parts-of-the-er-output"></a><span data-ttu-id="52d50-145">Konfigurace směrného plánu tak, aby ignoroval neustále se měnící části výstupu ER</span><span class="sxs-lookup"><span data-stu-id="52d50-145">Configure the baseline so that it ignores constantly changing parts of the ER output</span></span>

<span data-ttu-id="52d50-146">Pokud byl formát ER navržen tak, aby obsahoval informace, které se změní při spuštění formátu, musí být formát vyžadován pro použití funkce směrného plánu pro porovnání generovaných výsledků s hodnotami podle směrného plánu.</span><span class="sxs-lookup"><span data-stu-id="52d50-146">When an ER format has been designed to contain information that is changed when the format is run, the format must be required to use the ER baseline feature to compare the generated results with baseline values.</span></span> <span data-ttu-id="52d50-147">Informace mohou být například datum a čas zpracování nebo jedinečný identifikátor vygenerovaného dokumentu v různých formátech (globálně jedinečný identifikátor \[GUID\] atd.).</span><span class="sxs-lookup"><span data-stu-id="52d50-147">For example, the information might be the processing date and time or the unique identifier of a generated document in different formats (globally unique identifier \[GUID\], and so on).</span></span> <span data-ttu-id="52d50-148">Nové možnosti ER umožňují konfigurovat pravidlo směrného plánu tak, aby při spuštění formátu s cílem porovnání hodnot podle směrného plánu s výsledky provádění formátu ignorovalo změny ve formátu ER.</span><span class="sxs-lookup"><span data-stu-id="52d50-148">The new ER capabilities let you configure the baseline rule so that it ignores changeable elements of an ER format when the format is run with the purpose of comparing baseline values with the results of the format's execution.</span></span> <span data-ttu-id="52d50-149">Chcete-li získat další informace o této funkci, vyplňte následující příklad.</span><span class="sxs-lookup"><span data-stu-id="52d50-149">To learn more about this feature, complete the following example.</span></span>

## <a name="example-configure-the-baseline-so-that-it-ignores-constantly-changing-parts-of-the-er-output"></a><span data-ttu-id="52d50-150">Příklad: Konfigurace směrného plánu tak, aby ignoroval neustále se měnící části výstupu ER</span><span class="sxs-lookup"><span data-stu-id="52d50-150">Example: Configure the baseline so that it ignores constantly changing parts of the ER output</span></span>

<span data-ttu-id="52d50-151">Chcete-li dokončit kroky v tomto příkladu, musíte nejprve dokončit kroky v příkladu v tématu [Sledování generovaných výsledků sestav a jejich porovnání s hodnotami směrného plánu](er-trace-reports-compare-baseline.md).</span><span class="sxs-lookup"><span data-stu-id="52d50-151">To complete the steps in this example, you must first complete the steps in the example in the [Trace generated report results and compare them with baseline values](er-trace-reports-compare-baseline.md) topic.</span></span>

### <a name="modify-a-configured-er-format"></a><span data-ttu-id="52d50-152">Úprava konfigurovaného formátu ER</span><span class="sxs-lookup"><span data-stu-id="52d50-152">Modify a configured ER format</span></span>

1. <span data-ttu-id="52d50-153">Přejděte do části **Správa organizace** \> **Elektronické výkaznictví** \> **Konfigurace**.</span><span class="sxs-lookup"><span data-stu-id="52d50-153">Go to **Organization administration** \> **Electronic reporting** \> **Configurations**.</span></span>
2. <span data-ttu-id="52d50-154">Ve stromové struktuře rozbalte **Model pro učení směrných plánů ER**.</span><span class="sxs-lookup"><span data-stu-id="52d50-154">In the tree, expand **Model to learn ER baselines**.</span></span>
3. <span data-ttu-id="52d50-155">Ve stromové struktuře vyberte **Model pro učení směrných plánů ER\\Formát pro učení směrných plánů ER**.</span><span class="sxs-lookup"><span data-stu-id="52d50-155">In the tree, select **Model to learn ER baselines\\Format to learn ER baselines**.</span></span>
4. <span data-ttu-id="52d50-156">Vyberte možnost **Návrhář**.</span><span class="sxs-lookup"><span data-stu-id="52d50-156">Select **Designer**.</span></span>
5. <span data-ttu-id="52d50-157">Ve stromovém zobrazení vyberte **Výstup\\Dokument**.</span><span class="sxs-lookup"><span data-stu-id="52d50-157">In the tree, select **Output\\Document**.</span></span>
6. <span data-ttu-id="52d50-158">Vyberte **přidat**.</span><span class="sxs-lookup"><span data-stu-id="52d50-158">Select **Add**.</span></span>
7. <span data-ttu-id="52d50-159">V rozevíracím dialogovém okně ve stromu vyberte **XML\\Atribut**.</span><span class="sxs-lookup"><span data-stu-id="52d50-159">In the drop-down dialog box, in the tree, select **XML\\Attribute**.</span></span>
8. <span data-ttu-id="52d50-160">Do pole **Název** zadejte **ProcessingDateTime**.</span><span class="sxs-lookup"><span data-stu-id="52d50-160">In the **Name** field, enter **ProcessingDateTime**.</span></span>
9. <span data-ttu-id="52d50-161">Vyberte **OK**.</span><span class="sxs-lookup"><span data-stu-id="52d50-161">Select **OK**.</span></span>
10. <span data-ttu-id="52d50-162">Na kartě **mapování** ve stromové struktuře vyberte **Output\\Document\\ProcessingDateTime.**</span><span class="sxs-lookup"><span data-stu-id="52d50-162">On the **Mapping** tab, in the tree, select **Output\\Document\\ProcessingDateTime**.</span></span>
11. <span data-ttu-id="52d50-163">Vyberte možnost **Upravit vzorec**.</span><span class="sxs-lookup"><span data-stu-id="52d50-163">Select **Edit formula**.</span></span>
12. <span data-ttu-id="52d50-164">Do pole **Vzorec** zadejte následující výraz: **DATETIMEFORMAT(NOW(), "O")**</span><span class="sxs-lookup"><span data-stu-id="52d50-164">In the **Formula** field, enter the following expression: **DATETIMEFORMAT(NOW(), "O")**</span></span>
13. <span data-ttu-id="52d50-165">Vyberte **Uložit** a potom **Test**.</span><span class="sxs-lookup"><span data-stu-id="52d50-165">Select **Save**, and then select **Test**.</span></span>
14. <span data-ttu-id="52d50-166">Pokud chcete znovu otestovat konfigurovaný výraz, znovu vyberte **Test**.</span><span class="sxs-lookup"><span data-stu-id="52d50-166">Select **Test** again to retest the configured expression.</span></span>

    <span data-ttu-id="52d50-167">![Stránka návrháře vzorců](media/GER-BaselineSample-DefineProcessingDTExpression.PNG "Snímek obrazovky stránky návrháře vzorců")</span><span class="sxs-lookup"><span data-stu-id="52d50-167">![Formula designer page](media/GER-BaselineSample-DefineProcessingDTExpression.PNG "Screenshot of the Formula designer page")</span></span>

    > [!NOTE]
    > <span data-ttu-id="52d50-168">Na kartě **Výsledek** testu se zobrazuje, že konfigurovaný výraz vrací při každém volání jinou hodnotu data a času.</span><span class="sxs-lookup"><span data-stu-id="52d50-168">The **Test result** tab shows that the configured expression returns a different date and time value whenever it's called.</span></span>

15. <span data-ttu-id="52d50-169">Vyberte stránku **Návrhář vzorců** a potom **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="52d50-169">Close the **Formula designer** page, and then select **Save**.</span></span>

    <span data-ttu-id="52d50-170">![Stránka návrháře formátu](media/GER-BaselineSample-FormatMappingDesign2.PNG "Snímek obrazovky stránky návrháře formátu")</span><span class="sxs-lookup"><span data-stu-id="52d50-170">![Format designer page](media/GER-BaselineSample-FormatMappingDesign2.PNG "Screenshot of the Format designer page")</span></span>

16. <span data-ttu-id="52d50-171">Zavřete stránku **Návrhář formátu**.</span><span class="sxs-lookup"><span data-stu-id="52d50-171">Close the **Format designer** page.</span></span>

### <a name="remove-an-existing-baseline-rule"></a><span data-ttu-id="52d50-172">Odebrání existujícího pravidla směrného plánu</span><span class="sxs-lookup"><span data-stu-id="52d50-172">Remove an existing baseline rule</span></span>

1. <span data-ttu-id="52d50-173">Přejděte do části **Správa organizace** \> **Elektronické výkaznictví** \> **Konfigurace**.</span><span class="sxs-lookup"><span data-stu-id="52d50-173">Go to **Organization administration** \> **Electronic reporting** \> **Configurations**.</span></span>
2. <span data-ttu-id="52d50-174">Vyberte **Směrné plány**.</span><span class="sxs-lookup"><span data-stu-id="52d50-174">Select **Baselines**.</span></span>
3. <span data-ttu-id="52d50-175">V seznamu směrných plánů vyberte směrný plán, který je nakonfigurován pro **Formát pro učení směrných plánů**.</span><span class="sxs-lookup"><span data-stu-id="52d50-175">In the list of baselines, select the baseline that is configured for the **Format to learn ER baselines** format.</span></span>
4. <span data-ttu-id="52d50-176">Na pevné záložce **Směrné plány** vyberte **Odstranit** k odebrání dříve vytvořeného pravidla směrného plánu.</span><span class="sxs-lookup"><span data-stu-id="52d50-176">On the **Baselines** FastTab, select **Delete** to remove the baseline rule that you configured earlier.</span></span>

<span data-ttu-id="52d50-177">![Stránka směrného plánu formátu elektronického výkaznictví](media/GER-BaselineSample-AddBaseline3.PNG "Snímek obrazovky stránky směrného plánu formátu elektronického výkaznictví")</span><span class="sxs-lookup"><span data-stu-id="52d50-177">![Electronic reporting format baselines page](media/GER-BaselineSample-AddBaseline3.PNG "Screenshot of the Electronic reporting format baselines page")</span></span>

### <a name="define-replacements-for-bindings-of-designed-er-format"></a><span data-ttu-id="52d50-178">Definování náhrad pro vazby navrženého formátu ER</span><span class="sxs-lookup"><span data-stu-id="52d50-178">Define replacements for bindings of designed ER format</span></span>

1. <span data-ttu-id="52d50-179">Na stránce **Konfigurace** na pevné záložce **Náhrady** vyberte **Vybrat komponenty**.</span><span class="sxs-lookup"><span data-stu-id="52d50-179">On the **Configurations** page, on the **Replacements** FastTab, select **Select components**.</span></span>
2. <span data-ttu-id="52d50-180">Ve stromu komponent formátu rozbalte **Výstup**, rozbalte **Výstup\\Dokument** a zaškrtněte políčko **Výstup\\Dokument\\ProcessingDateTime**.</span><span class="sxs-lookup"><span data-stu-id="52d50-180">In the format components tree, expand **Output**, expand **Output\\Document**, and then select the check box for **Output\\Document\\ProcessingDateTime**.</span></span>

    <span data-ttu-id="52d50-181">![Dialogové okno Vybrat komponenty](media/GER-BaselineSample-SelectComponentForBindingReplacement.PNG "– snímek obrazovky dialogového okna Vybrat komponenty")</span><span class="sxs-lookup"><span data-stu-id="52d50-181">![Select Components dialog box](media/GER-BaselineSample-SelectComponentForBindingReplacement.PNG "Screenshot of the Select Components dialog box")</span></span>

3. <span data-ttu-id="52d50-182">Vyberte **OK**.</span><span class="sxs-lookup"><span data-stu-id="52d50-182">Select **OK**.</span></span>

<span data-ttu-id="52d50-183">![Stránka směrného plánu formátu elektronického výkaznictví](media/GER-BaselineSample-AddBaseline4.PNG "Snímek obrazovky stránky směrného plánu formátu elektronického výkaznictví")</span><span class="sxs-lookup"><span data-stu-id="52d50-183">![Electronic reporting format baselines page](media/GER-BaselineSample-AddBaseline4.PNG "Screenshot of the Electronic reporting format baselines page")</span></span>

<span data-ttu-id="52d50-184">Vybraná koponenta formátu ER byla přidána do seznamu komponent na pevné záložce **Náhrady**.</span><span class="sxs-lookup"><span data-stu-id="52d50-184">The selected ER format component has been added to the list of components on the **Replacements** FastTab.</span></span> <span data-ttu-id="52d50-185">Při spuštění základního formátu ER v režimu ladění bude vazba formátu pro každou součást nahrazena vazbou, která je zobrazena ve sloupci **vazba**.</span><span class="sxs-lookup"><span data-stu-id="52d50-185">When the base ER format is run in debug mode, the format's binding for each component will be replaced by the binding that is shown in the **Binding** column.</span></span> <span data-ttu-id="52d50-186">Chcete-li změnit výchozí vazbu pro komponentu, která je uvedena na pevné záložce **Náhrady**, vyberte **Upravit**.</span><span class="sxs-lookup"><span data-stu-id="52d50-186">To change the default binding for a component that is listed on the **Replacements** FastTab, select **Edit**.</span></span>

### <a name="make-a-new-baseline-rule"></a><span data-ttu-id="52d50-187">Vtvoření nového pravidla směrného plánu</span><span class="sxs-lookup"><span data-stu-id="52d50-187">Make a new baseline rule</span></span>

<span data-ttu-id="52d50-188">Postupujte podle kroků v části Příklad: automatizace nastavení pravidel směrného plánu dříve v tomto tématu.</span><span class="sxs-lookup"><span data-stu-id="52d50-188">Follow the steps in the "Example: Automate the setting of baseline rules" section earlier in this topic.</span></span> <span data-ttu-id="52d50-189">Zobrazí se upozornění, že výstupní soubor byl vygenerován pomocí nastavení směrného plánu a že došlo k vynucenému nahrazení vazeb formátu.</span><span class="sxs-lookup"><span data-stu-id="52d50-189">A notification warns you that the outbound file has been generated by using baseline settings, and that a forced replacement of the format bindings has occurred.</span></span>

<span data-ttu-id="52d50-190">![Snímek obrazovky s konfiguracemi](media/GER-BaselineSample-FormatRunToMakeBaselineFile4.PNG "Snímek obrazovky stránky s oznámením na stránce konfigurace")</span><span class="sxs-lookup"><span data-stu-id="52d50-190">![Notification on the Configurations page](media/GER-BaselineSample-FormatRunToMakeBaselineFile4.PNG "Screenshot of the notification on the Configurations page")</span></span>

### <a name="suppress-warnings-about-the-replacement-of-format-bindings"></a><span data-ttu-id="52d50-191">Potlačení upozornění na náhradní vazby formátu</span><span class="sxs-lookup"><span data-stu-id="52d50-191">Suppress warnings about the replacement of format bindings</span></span>

<span data-ttu-id="52d50-192">Nastavením specifických parametrů ER můžete potlačit upozornění na nahrazení formátovacích vazeb.</span><span class="sxs-lookup"><span data-stu-id="52d50-192">By setting specific ER parameters, you can suppress notifications that warn about the replacement of format bindings.</span></span> <span data-ttu-id="52d50-193">Toto potlačení může být užitečné, pokud jsou formátovací vazby nahrazeny bezobslužným režimem pomocí Regression Suite Automation Tool.</span><span class="sxs-lookup"><span data-stu-id="52d50-193">This suppression can be useful when format bindings are replaced in an unattended mode by using the Regression Suite Automation Tool.</span></span> <span data-ttu-id="52d50-194">V tomto případě může být upozornění považováno za selhání testovacího případu, který běží.</span><span class="sxs-lookup"><span data-stu-id="52d50-194">In this case, the warning can be considered a failure of the test case that is running.</span></span>

1. <span data-ttu-id="52d50-195">Na stránce **Konfigurace** v podokně akcí na kartě **Konfigurace** vyberte **Parametry uživatelů**.</span><span class="sxs-lookup"><span data-stu-id="52d50-195">On the **Configurations** page, on the Action Pane, on the **Configurations** tab, select **User parameters**.</span></span>
2. <span data-ttu-id="52d50-196">Nastavte volbu **potlačit upozornění** podle směrného plánu na hodnotu **Ano** a pak klikněte na tlačítko **OK**.</span><span class="sxs-lookup"><span data-stu-id="52d50-196">Set the **Suppress baseline warnings** option to **Yes**, and then select **OK**.</span></span>

<span data-ttu-id="52d50-197">![Dialogové okno Parametry uživatele](media/GER-BaselineSample-ERUserParameters1.png "Obrázek dialogového okna Parametry uživatele")</span><span class="sxs-lookup"><span data-stu-id="52d50-197">![User parameters dialog box](media/GER-BaselineSample-ERUserParameters1.png "Screenshot of the User parameters dialog box")</span></span>

### <a name="review-the-generated-baseline-file"></a><span data-ttu-id="52d50-198">Kontrola generovaného souboru směrného plánu</span><span class="sxs-lookup"><span data-stu-id="52d50-198">Review the generated baseline file</span></span>

1. <span data-ttu-id="52d50-199">Přejděte do části **Správa organizace** \> **Elektronické výkaznictví** \> **Konfigurace**.</span><span class="sxs-lookup"><span data-stu-id="52d50-199">Go to **Organization administration** \> **Electronic reporting** \> **Configurations**.</span></span>
2. <span data-ttu-id="52d50-200">Vyberte **Směrné plány**.</span><span class="sxs-lookup"><span data-stu-id="52d50-200">Select **Baselines**.</span></span>
3. <span data-ttu-id="52d50-201">Vyberte **Přílohy**.</span><span class="sxs-lookup"><span data-stu-id="52d50-201">Select **Attachments**.</span></span>

    <span data-ttu-id="52d50-202">![Stránka Přílohy](media/GER-BaselineSample-AttachedBaselineFile.PNG "Snímek obrazovky stránky Přílohy")</span><span class="sxs-lookup"><span data-stu-id="52d50-202">![Attachments page](media/GER-BaselineSample-AttachedBaselineFile.PNG "Screenshot of the Attachments page")</span></span>

    > [!NOTE]
    > <span data-ttu-id="52d50-203">Vygenerovaný soubor obsahuje text data a času zpracování (**"#"**) z vazby, která byla nakonfigurována v přidaném základním pravidlu, ne z vazby formátu.</span><span class="sxs-lookup"><span data-stu-id="52d50-203">The generated file contains the processing date and time text (**"#"**) from the binding that was configured in the added baseline rule, not from the format's binding.</span></span>

4. <span data-ttu-id="52d50-204">Zavřete stránku **Přílohy**.</span><span class="sxs-lookup"><span data-stu-id="52d50-204">Close the **Attachments** page.</span></span>

### <a name="run-the-designed-er-format-and-review-the-log-to-analyze-the-results"></a><span data-ttu-id="52d50-205">Spuštění navrženého formát ER a kontrola protokolu pro analýzu výsledků</span><span class="sxs-lookup"><span data-stu-id="52d50-205">Run the designed ER format and review the log to analyze the results</span></span>

1. <span data-ttu-id="52d50-206">Přejděte do části **Správa organizace** \> **Elektronické výkaznictví** \> **Konfigurace**.</span><span class="sxs-lookup"><span data-stu-id="52d50-206">Go to **Organization administration** \> **Electronic reporting** \> **Configurations**.</span></span>
2. <span data-ttu-id="52d50-207">Ve stromové struktuře rozbalte **Model pro učení směrných plánů ER**.</span><span class="sxs-lookup"><span data-stu-id="52d50-207">In the tree, expand **Model to learn ER baselines**.</span></span>
3. <span data-ttu-id="52d50-208">Ve stromové struktuře vyberte **Model pro učení směrných plánů ER\\Formát pro učení směrných plánů ER**.</span><span class="sxs-lookup"><span data-stu-id="52d50-208">In the tree, select **Model to learn ER baselines\\Format to learn ER baselines**.</span></span>
4. <span data-ttu-id="52d50-209">Na pevné záložce **Verze** vyberte **Spustit**.</span><span class="sxs-lookup"><span data-stu-id="52d50-209">On the **Versions** FastTab select **Run**.</span></span>
5. <span data-ttu-id="52d50-210">Do pole **Zadat ID** zadejte **1**.</span><span class="sxs-lookup"><span data-stu-id="52d50-210">In the **Enter Id** field, type **1**.</span></span>
6. <span data-ttu-id="52d50-211">Vyberte **OK**.</span><span class="sxs-lookup"><span data-stu-id="52d50-211">Select **OK**.</span></span>
7. <span data-ttu-id="52d50-212">Přejděte do části **Správa organizace** \> **Elektronické výkaznictví** \> **Konfigurovat protokoly ladění**.</span><span class="sxs-lookup"><span data-stu-id="52d50-212">Go to **Organization administration** \> **Electronic reporting** \> **Configuration debug logs**.</span></span>

<span data-ttu-id="52d50-213">Protokol spuštění obsahuje informace o výsledcích porovnání generovaného souboru s nakonfigurovaným směrným plánem.</span><span class="sxs-lookup"><span data-stu-id="52d50-213">The execution log contains information about the results of the comparison of the generated file with the configured baseline.</span></span> <span data-ttu-id="52d50-214">Protokol označuje, že vygenerovaný soubor a směrný plán jsou stejné, přestože spuštěný formát obsahuje vazbu k zadání neustále se měnící hodnoty data a času v odchozím souboru.</span><span class="sxs-lookup"><span data-stu-id="52d50-214">The log indicates that the generated file and the baseline are equal, even though the executed format contains the binding to enter a constantly changing date and time value in the outbound file.</span></span>

> [!NOTE]
> <span data-ttu-id="52d50-215">Přestože byl výstupní soubor vygenerován pomocí nastavení směrného plánu, které vynutí nahrazení vazeb formátu, neobdržíte žádná upozornění o náhradě.</span><span class="sxs-lookup"><span data-stu-id="52d50-215">Although the outbound file has been generated by using baseline settings that force the replacement of the format's bindings, you don't receive any warnings about the replacement.</span></span>

## <a name="exchange-baseline-settings-between-environments"></a><span data-ttu-id="52d50-216">Výměna nastavení směrného plánu mezi prostředími</span><span class="sxs-lookup"><span data-stu-id="52d50-216">Exchange baseline settings between environments</span></span>

### <a name="export-baseline-settings"></a><span data-ttu-id="52d50-217">Export nastavení směrného plánu</span><span class="sxs-lookup"><span data-stu-id="52d50-217">Export baseline settings</span></span>

<span data-ttu-id="52d50-218">Nové možnosti ER umožňují exportovat nastavení směrného plánu pro vybraný formát ER z aktuálního prostředí pro modul Finance and Operations a uložit je jako soubory XML.</span><span class="sxs-lookup"><span data-stu-id="52d50-218">The new ER capabilities let you export baseline settings for the selected ER format from the current Finance and Operations environment and store them as XML files.</span></span> 

<span data-ttu-id="52d50-219">Pokud chcete exportovat nastavení směrného plánu, na stránce **Směrné plány formátu elektrického výkaznictví** vyberte **Export**.</span><span class="sxs-lookup"><span data-stu-id="52d50-219">To export baseline settings, on the **Electronic reporting format baselines** page, select **Export**.</span></span>

### <a name="import-baseline-settings"></a><span data-ttu-id="52d50-220">Importovat základní nastavení</span><span class="sxs-lookup"><span data-stu-id="52d50-220">Import baseline settings</span></span>

<span data-ttu-id="52d50-221">Exportované nastavení směrného plánu lze importovat do prostředí modulu Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="52d50-221">Exported baseline settings can be imported into a different Finance and Operations environment.</span></span> <span data-ttu-id="52d50-222">Prostředí musí být nejprve importováno jako formát ER.</span><span class="sxs-lookup"><span data-stu-id="52d50-222">The environment must first be imported as an ER format.</span></span> <span data-ttu-id="52d50-223">Poté můžete importovat nastavení směrného plánu.</span><span class="sxs-lookup"><span data-stu-id="52d50-223">You can then import the baseline settings.</span></span>

<span data-ttu-id="52d50-224">Pokud chcete importovat nastavení směrného plánu z lokálně uloženého souboru XML, na stránce **Směrné plány formátu elektronického výkaznictví** vyberte **Import** a potom po kliknutí na **Procházet** vyberte soubor XML.</span><span class="sxs-lookup"><span data-stu-id="52d50-224">To import baseline settings from a locally stored XML file, on the **Electronic reporting format baselines** page, select **Import**, and then select **Browse** to select the XML file.</span></span>

<span data-ttu-id="52d50-225">![Dialogové okno Importovat nastavení směrného plánu](media/GER-BaselineSample-ImportBaseline1.PNG "Snímek obrazovky dialogového okna Importovat nastavení směrného plánu")</span><span class="sxs-lookup"><span data-stu-id="52d50-225">![Import baseline settings dialog box](media/GER-BaselineSample-ImportBaseline1.PNG "Screenshot of the Import baseline settings dialog box")</span></span>

<span data-ttu-id="52d50-226">Chcete-li importovat nastavení směrného plánu ze souboru XML, který je uložen na serveru SharePoint společnosti Microsoft na základě aktuálního nastavení správy dokumentů a vybraného typu dokumentu, na stránce **Směrné plány formátu elektronického výkaznictví** vyberte možnost **Importovat ze zdroje**.</span><span class="sxs-lookup"><span data-stu-id="52d50-226">To import baseline settings from an XML file that is stored on the Microsoft SharePoint Server, based on the current Document management settings and the selected document type, on the **Electronic reporting format baselines** page, select **Import from source**.</span></span> <span data-ttu-id="52d50-227">Pak vyberte typ dokumentu a soubor XML.</span><span class="sxs-lookup"><span data-stu-id="52d50-227">Then select the document type and the XML file.</span></span> <span data-ttu-id="52d50-228">Požadovaný typ dokumentu pro přístup do složky SharePoint musí být nakonfigurován předem.</span><span class="sxs-lookup"><span data-stu-id="52d50-228">The required document type to access the SharePoint folder must be configured in advance.</span></span>

<span data-ttu-id="52d50-229">![Dialogové okno Importovat ze zdroje](media/GER-BaselineSample-ImportBaseline2.PNG "Snímek obrazovky dialogového okna Importovat ze zdroje")</span><span class="sxs-lookup"><span data-stu-id="52d50-229">![Import from source dialog box](media/GER-BaselineSample-ImportBaseline2.PNG "Screenshot of the Import from source dialog box")</span></span>

> [!NOTE]
> <span data-ttu-id="52d50-230">Pomocí záznamníku úkolů můžete zaznamenat postup pro výběr požadovaného typu dokumentu a název souboru v dialogovém okně **Importovat ze zdroje**.</span><span class="sxs-lookup"><span data-stu-id="52d50-230">You can use Task recorder to record the steps for selecting the required document type and the file name in the **Import from source** dialog box.</span></span> <span data-ttu-id="52d50-231">Tímto způsobem můžete ponechat požadované nastavení směrného plánu na serveru SharePoint a poté je automaticky importovat přehráním záznamu úkolu při spuštění automatizovaných testů pomocí nástroje Regression Suite Automation Tool.</span><span class="sxs-lookup"><span data-stu-id="52d50-231">In this way, you can keep required baseline settings on SharePoint Server and then automatically import them by playing a task recording when you run automated tests by using the Regression Suite Automation Tool.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="52d50-232">Další zdroje</span><span class="sxs-lookup"><span data-stu-id="52d50-232">Additional resources</span></span>

- [<span data-ttu-id="52d50-233">Sledování výsledků vygenerovaných sestav a jejich porovnání se základními hodnotami</span><span class="sxs-lookup"><span data-stu-id="52d50-233">Trace generated report results and compare them with baseline values</span></span>](er-trace-reports-compare-baseline.md)
- [<span data-ttu-id="52d50-234">Záznamník úkolů</span><span class="sxs-lookup"><span data-stu-id="52d50-234">Task recorder</span></span>](../user-interface/task-recorder.md)
