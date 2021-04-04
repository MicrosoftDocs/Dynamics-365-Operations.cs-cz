---
title: Potlačit ovládací prvky obsahu Word v generovaných sestavách
description: Toto téma vysvětluje, jak konfigurovat formát elektronického výkaznictví (ER) pro generování zpráv jako souborů Microsoft Word, kde jsou potlačeny ovládací prvky obsahu.
author: NickSelin
manager: AnnBe
ms.date: 02/11/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ERWorkspace, ERSolutionTable, EROperationDesigner,  LedgerJournalTable, LedgerJournalTransVendPaym
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2020-01-01
ms.dyn365.ops.version: Version 10.0.6
ms.openlocfilehash: 81ad25514154dd8982aa4f849f0b2bfeb85270f7
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/09/2021
ms.locfileid: "5562111"
---
# <a name="suppress-word-content-controls-in-generated-reports"></a><span data-ttu-id="3afae-103">Potlačit ovládací prvky obsahu Word v generovaných sestavách</span><span class="sxs-lookup"><span data-stu-id="3afae-103">Suppress Word content controls in generated reports</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="3afae-104">Chcete-li generovat sestavy jako dokumenty Microsoft Word, musíte navrhnout šablonu pro zprávy jako dokument aplikace Word.</span><span class="sxs-lookup"><span data-stu-id="3afae-104">To generate reports as Microsoft Word documents, you must design a template for the reports as a Word document.</span></span> <span data-ttu-id="3afae-105">Tato šablona musí obsahovat ovládací prvky obsahu Word jako zástupné symboly pro data, která budou vyplněna za běhu.</span><span class="sxs-lookup"><span data-stu-id="3afae-105">This template must contain Word content controls as placeholders for data that will be filled in at runtime.</span></span> <span data-ttu-id="3afae-106">Chcete-li použít vytvořený dokument Word jako šablonu pro své sestavy, můžete [nakonfigurovat](er-design-configuration-word.md) nové [řešení](er-quick-start1-new-solution.md) [elektronického výkaznictví (ER)](general-electronic-reporting.md).</span><span class="sxs-lookup"><span data-stu-id="3afae-106">To use the Word document that is created as a template for your reports, you can [configure](er-design-configuration-word.md) a new [Electronic reporting (ER)](general-electronic-reporting.md) [solution](er-quick-start1-new-solution.md).</span></span> <span data-ttu-id="3afae-107">Řešení musí obsahovat [konfiguraci ER](general-electronic-reporting.md#Configuration), která obsahuje komponentu [formát](general-electronic-reporting.md#FormatComponentOutbound) ER.</span><span class="sxs-lookup"><span data-stu-id="3afae-107">The solution must include an ER [configuration](general-electronic-reporting.md#Configuration) that contains an ER [format](general-electronic-reporting.md#FormatComponentOutbound) component.</span></span> <span data-ttu-id="3afae-108">Tento formát ER musí být nakonfigurován pro použití navržené šablony pro generování sestav.</span><span class="sxs-lookup"><span data-stu-id="3afae-108">This ER format must be configured to use the designed template for report generation.</span></span>

<span data-ttu-id="3afae-109">Ve verzi 10.0.6 a novější Dynamics 365 Finance můžete nakonfigurovat vzorce ve formátu ER tak, aby potlačily některé ovládací prvky obsahu Word v generovaných dokumentech.</span><span class="sxs-lookup"><span data-stu-id="3afae-109">In version 10.0.6 and later of Dynamics 365 Finance, you can configure formulas in your ER format to suppress some Word content controls in generated documents.</span></span>

<span data-ttu-id="3afae-110">Následující kroky vysvětlují, jak může uživatel, který je přiřazen správci systému nebo roli konzultanta funkčních elektronických zpráv, nakonfigurovat formát ER, který generuje sestavy jako soubory aplikace Word a potlačuje některé ovládací prvky obsahu v generovaných sestavách, které byly konfigurovány pomocí šablony Word.</span><span class="sxs-lookup"><span data-stu-id="3afae-110">The following steps explain how a user who is assigned to the System administrator or Electronic reporting functional consultant role can configure an ER format that generates reports as Word files and suppresses some of the content controls in the generated reports that have been configured by using a Word template.</span></span>

<span data-ttu-id="3afae-111">Tyto kroky lze provést v rámci společnosti GBSI.</span><span class="sxs-lookup"><span data-stu-id="3afae-111">These steps can be completed in the GBSI company.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="3afae-112">Předpoklady</span><span class="sxs-lookup"><span data-stu-id="3afae-112">Prerequisites</span></span>

<span data-ttu-id="3afae-113">K provedení těchto kroků je nutné nejprve provést kroky v následujících průvodcích:</span><span class="sxs-lookup"><span data-stu-id="3afae-113">To complete these steps, you must first complete the steps in the following task guides:</span></span>

- [<span data-ttu-id="3afae-114">Návrh konfigurace pro generování sestav ve formátu OPENXML</span><span class="sxs-lookup"><span data-stu-id="3afae-114">Design a configuration for generating reports in OPENXML format</span></span>](./tasks/er-design-reports-openxml-2016-11.md)
- [<span data-ttu-id="3afae-115">Opětovné použití konfigurací elektronického výkaznictví s šablonami Excel pro generování sestav ve formátu Word</span><span class="sxs-lookup"><span data-stu-id="3afae-115">Re-use ER configurations with Excel templates to generate reports in Word format</span></span>](./tasks/er-design-configuration-word-2016-11.md)

<span data-ttu-id="3afae-116">Po dokončení kroků v těchto průvodcích úkoly jsou připraveny následující položky:</span><span class="sxs-lookup"><span data-stu-id="3afae-116">When you complete the steps of these task guides, the following items are prepared:</span></span>

- <span data-ttu-id="3afae-117">Formát ER **Vzorová sestava listu**, která je nakonfigurována pro generování dokumentu ve formátu Word</span><span class="sxs-lookup"><span data-stu-id="3afae-117">A **Sample worksheet report** ER format that is configured to generate a document in Word format</span></span>
- <span data-ttu-id="3afae-118">Verze [konceptu](general-electronic-reporting.md#component-versioning) formátu ER **Vzorové sestavy listu**, který je označen jako **Spustitelný**</span><span class="sxs-lookup"><span data-stu-id="3afae-118">A [draft](general-electronic-reporting.md#component-versioning) version of the **Sample worksheet report** ER format that is marked as **Runnable**</span></span>
- <span data-ttu-id="3afae-119">**Elektronický** způsob platby, který je nakonfigurován pro použití formátu ER **Vzorové sestavy listu** pro zpracování plateb dodavatele</span><span class="sxs-lookup"><span data-stu-id="3afae-119">An **Electronic** method of payments that is configured to use the **Sample worksheet report** ER format for vendor payment processing</span></span>

<span data-ttu-id="3afae-120">Musíte si také stáhnout a uložit následující šablonu pro vzorovou sestavu:</span><span class="sxs-lookup"><span data-stu-id="3afae-120">You must also download and save the following template for the sample report:</span></span>

- [<span data-ttu-id="3afae-121">Vázaná šablona 2 sestavy platby (SampleVendPaymDocReportBounded2.docx)</span><span class="sxs-lookup"><span data-stu-id="3afae-121">Bounded Template 2 of Payment Report (SampleVendPaymDocReportBounded2.docx)</span></span>](https://download.microsoft.com/download/a/1/2/a126cb43-6281-4f7b-bde0-25e03ff9bc1e/SampleVendPaymDocReportBounded2.docx)

## <a name="review-the-downloaded-word-template"></a><a id="tag-control"></a><span data-ttu-id="3afae-122">Kontrola stažené šablony Wordu</span><span class="sxs-lookup"><span data-stu-id="3afae-122">Review the downloaded Word template</span></span>

1. <span data-ttu-id="3afae-123">V desktopové aplikaci Word otevřete soubor šablony **SampleVendPaymDocReportBounded2.docx**, který jste stáhli dříve.</span><span class="sxs-lookup"><span data-stu-id="3afae-123">In the Word desktop application, open the **SampleVendPaymDocReportBounded2.docx** template file that you downloaded earlier.</span></span>
2. <span data-ttu-id="3afae-124">Ověřte, zda soubor šablony obsahuje souhrnnou část, která zobrazuje celkové částky plateb pro každý kód měny, který byl zjištěn ve zpracovaných platbách.</span><span class="sxs-lookup"><span data-stu-id="3afae-124">Verify that the template file contains a summary section that shows the total payment amounts for every currency code that has been met in the processed payments.</span></span>

    - <span data-ttu-id="3afae-125">Souhrnná část je umístěna v samostatné tabulce dokumentu aplikace Word.</span><span class="sxs-lookup"><span data-stu-id="3afae-125">The summary section resides in a separate table of the Word document.</span></span>
    - <span data-ttu-id="3afae-126">První řádek této tabulky obsahuje záhlaví sloupců tabulky jako záhlaví sekce.</span><span class="sxs-lookup"><span data-stu-id="3afae-126">The first row of this table holds the table columns headings as the section header.</span></span>
    - <span data-ttu-id="3afae-127">Druhý řádek této tabulky obsahuje ovládací prvek opakujícího se obsahu jako podrobnosti sekce.</span><span class="sxs-lookup"><span data-stu-id="3afae-127">The second row of this table holds the repeating content control as the section details.</span></span>
    - <span data-ttu-id="3afae-128">Tento ovládací prvek obsahu je namapován na pole **Souhrnné řádky** vlastní části XML **sestavy**.</span><span class="sxs-lookup"><span data-stu-id="3afae-128">This content control is mapped to the **SummaryLines** field of the **Report** custom XML part.</span></span>
    - <span data-ttu-id="3afae-129">Na základě tohoto mapování je ovládací prvek obsahu přidružen k prvku **SummaryLines** upravitelného formátu ER.</span><span class="sxs-lookup"><span data-stu-id="3afae-129">Based on this mapping, the content control is associated with the **SummaryLines** element of the editable ER format.</span></span>

    > [!NOTE]
    > <span data-ttu-id="3afae-130">Opakující se ovládací prvek obsahu je označen klíčem **SummaryLines**, který odpovídá poli vlastní části XML, na kterou byl namapován.</span><span class="sxs-lookup"><span data-stu-id="3afae-130">The repeating content control is tagged by the **SummaryLines** key that matches the field of the custom XML part that it has been mapped to.</span></span>

    ![Rozložení šablony Word](./media/er-design-configuration-word-suppress-controls-image1.gif)

## <a name="select-the-existing-er-report-configuration"></a><span data-ttu-id="3afae-132">Volba existující konfigurace sestavy ER</span><span class="sxs-lookup"><span data-stu-id="3afae-132">Select the existing ER report configuration</span></span>

<span data-ttu-id="3afae-133">V následujících krocích znovu použijete stávající konfiguraci ER, kterou jste nakonfigurovali, když jste provedli kroky v dříve zmíněných průvodcích úkoly.</span><span class="sxs-lookup"><span data-stu-id="3afae-133">For the following steps, you will reuse the existing ER configuration that you configured when you completed the steps in the previously mentioned task guides.</span></span>

1. <span data-ttu-id="3afae-134">Přejděte do části **Správa organizace** \> **Pracovní prostory** \> **Elektronické výkaznictví**.</span><span class="sxs-lookup"><span data-stu-id="3afae-134">Go to **Organization administration** \> **Workspaces** \> **Electronic reporting**.</span></span>
2. <span data-ttu-id="3afae-135">Vyberte **Konfigurace vykazování**.</span><span class="sxs-lookup"><span data-stu-id="3afae-135">Select **Reporting configurations**.</span></span>
3. <span data-ttu-id="3afae-136">Na stránce **Konfigurace** ve stromu konfigurací rozbalte položku **Model platby** a poté vyberte možnost **Vzorová sestava listu**.</span><span class="sxs-lookup"><span data-stu-id="3afae-136">On the **Configurations** page, in the configuration tree, expand **Payment model**, and select **Sample worksheet report**.</span></span>
4. <span data-ttu-id="3afae-137">Vyberte **Návrhář** k úpravě verze konceptu vybraného formátu ER.</span><span class="sxs-lookup"><span data-stu-id="3afae-137">Select **Designer** to edit the draft version of the selected ER format.</span></span>

## <a name="replace-the-current-template-with-the-new-template"></a><span data-ttu-id="3afae-138">Výměna aktuální šablony za novou šablonu</span><span class="sxs-lookup"><span data-stu-id="3afae-138">Replace the current template with the new template</span></span>

<span data-ttu-id="3afae-139">V současné době se používá soubor SampleVendPaymDocReportBounded.docx jako šablona pro generování výstupu ve formátu Word.</span><span class="sxs-lookup"><span data-stu-id="3afae-139">Currently, the SampleVendPaymDocReportBounded.docx file is used as a template to generate the output in Word format.</span></span> <span data-ttu-id="3afae-140">V následujícím postupu tuto šablonu Word nahradíte novým souborem šablony Word SampleVendPaymDocReportBounded2.docx, kterou jste předtím stáhli.</span><span class="sxs-lookup"><span data-stu-id="3afae-140">In the following steps, you will replace this Word template with the new Word template, SampleVendPaymDocReportBounded2.docx, that you downloaded earlier.</span></span>

1. <span data-ttu-id="3afae-141">Na stránce **Návrhář formátu** zvolte **Přílohy**.</span><span class="sxs-lookup"><span data-stu-id="3afae-141">On the **Format designer** page, select **Attachments**.</span></span>
2. <span data-ttu-id="3afae-142">Na stránce **Přílohy** vyberte **Odstranit** pro odebrání existující šablony.</span><span class="sxs-lookup"><span data-stu-id="3afae-142">On the **Attachments** page, select **Delete** to remove the existing template.</span></span>
3. <span data-ttu-id="3afae-143">Vyberte **Ano** pro potvrzení odstranění.</span><span class="sxs-lookup"><span data-stu-id="3afae-143">Select **Yes** to confirm the deletion.</span></span>
4. <span data-ttu-id="3afae-144">Vyberte **Nový** \> **Soubor**.</span><span class="sxs-lookup"><span data-stu-id="3afae-144">Select **New** \> **File**.</span></span>
5. <span data-ttu-id="3afae-145">Vyberte **Procházet** a poté přejděte na a vyberte soubor **SampleVendPaymDocReportBounded2.docx**, který jste stáhli dříve.</span><span class="sxs-lookup"><span data-stu-id="3afae-145">Select **Browse**, and browse to and select the **SampleVendPaymDocReportBounded2.docx** file that you downloaded earlier.</span></span>
6. <span data-ttu-id="3afae-146">Vyberte **OK**.</span><span class="sxs-lookup"><span data-stu-id="3afae-146">Select **OK**.</span></span>
7. <span data-ttu-id="3afae-147">Zavřete stránku **Přílohy**.</span><span class="sxs-lookup"><span data-stu-id="3afae-147">Close the **Attachments** page.</span></span>
8. <span data-ttu-id="3afae-148">Na stránce **Návrhář formátů** do pole **Šablona** zadejte nebo vyberte soubor **SampleVendPaymDocReportBounded2.docx**.</span><span class="sxs-lookup"><span data-stu-id="3afae-148">On the **Format designer** page, in the **Template** field, enter or select the **SampleVendPaymDocReportBounded2.docx** file.</span></span>

## <a name="run-the-format-to-create-word-output"></a><span data-ttu-id="3afae-149">Spuštění formátu pro vytvoření výstupu ve Wordu</span><span class="sxs-lookup"><span data-stu-id="3afae-149">Run the format to create Word output</span></span>

1. <span data-ttu-id="3afae-150">Přejděte na **Závazky** \> **Platby** \> **Deník plateb**.</span><span class="sxs-lookup"><span data-stu-id="3afae-150">Go to **Accounts payable** \> **Payments** \> **Payment journal**.</span></span>
2. <span data-ttu-id="3afae-151">Na stránce **Platby dodavatele** na kartě **Seznam** vyberte všechny platby.</span><span class="sxs-lookup"><span data-stu-id="3afae-151">On the **Vendor payments** page, on the **List** tab, select all the payments.</span></span>
3. <span data-ttu-id="3afae-152">Vyberte **Stav platby** \> **Žádný**.</span><span class="sxs-lookup"><span data-stu-id="3afae-152">Select **Payment status** \> **None**.</span></span>
4. <span data-ttu-id="3afae-153">Vyberte **Generovat platby**.</span><span class="sxs-lookup"><span data-stu-id="3afae-153">Select **Generate payments**.</span></span>
5. <span data-ttu-id="3afae-154">V poli **Způsob platby** vyberte **Elektronický**.</span><span class="sxs-lookup"><span data-stu-id="3afae-154">In the **Method of payment** field, select **Electronic**.</span></span>
6. <span data-ttu-id="3afae-155">V poli **Bankovní účet** vyberte **GBSI OPER**.</span><span class="sxs-lookup"><span data-stu-id="3afae-155">In the **Bank account** field, select **GBSI OPER**.</span></span>
7. <span data-ttu-id="3afae-156">Vyberte **OK**.</span><span class="sxs-lookup"><span data-stu-id="3afae-156">Select **OK**.</span></span>
8. <span data-ttu-id="3afae-157">V dialogovém okně **Parametry elektronického přiznání** vyberte **OK** a analyzujte vygenerovaný výstup.</span><span class="sxs-lookup"><span data-stu-id="3afae-157">In the **Electronic report parameters** dialog box, select **OK**, and analyze the generated output.</span></span>

    ![Platby za zpracování na stránce Platby dodavatele](./media/er-design-configuration-word-suppress-controls-image2.gif)

    <span data-ttu-id="3afae-159">Výstup je prezentován ve formátu Word a obsahuje souhrnnou část.</span><span class="sxs-lookup"><span data-stu-id="3afae-159">The output is presented in Word format and contains the summary section.</span></span>

## <a name="configure-the-editable-format-to-suppress-the-summary-section"></a><a id="configure-to-suppress-control"></a><span data-ttu-id="3afae-160">Nakonfigurujte upravitelný formát tak, aby potlačil část shrnutí</span><span class="sxs-lookup"><span data-stu-id="3afae-160">Configure the editable format to suppress the summary section</span></span>

<span data-ttu-id="3afae-161">Pokud chcete potlačit souhrnnou část v generovaném dokumentu na základě požadavku uživatele, který spouští tento formát ER, musíte upravit upravitelný formát ER.</span><span class="sxs-lookup"><span data-stu-id="3afae-161">If you want to suppress the summary section in a generated document, based on the request of a user who runs this ER format, you must modify the editable ER format.</span></span>

1. <span data-ttu-id="3afae-162">Přejděte do **Správa organizace** \> **Pracovní prostory** \> **Elektronické hlášení** a otevřete koncept verzi formátu ER pro úpravy.</span><span class="sxs-lookup"><span data-stu-id="3afae-162">Go to **Organization administration** \> **Workspaces** \> **Electronic reporting**, and open the draft version of the ER format for editing.</span></span>
2. <span data-ttu-id="3afae-163">Vyberte **Konfigurace vykazování**.</span><span class="sxs-lookup"><span data-stu-id="3afae-163">Select **Reporting configurations**.</span></span> 
3. <span data-ttu-id="3afae-164">Na stránce **Konfigurace** ve stromu konfigurací rozbalte položku **Model platby** \> **Vzorová sestava listu**.</span><span class="sxs-lookup"><span data-stu-id="3afae-164">On the **Configurations** page, in the configuration tree, expand **Payment model** \> **Sample worksheet report**.</span></span>
4. <span data-ttu-id="3afae-165">Vyberte možnost **Návrhář**.</span><span class="sxs-lookup"><span data-stu-id="3afae-165">Select **Designer**.</span></span>
5. <span data-ttu-id="3afae-166">Na stránce **Návrhář formátů** rozbalte **Word** a vyberte **SummaryLines**.</span><span class="sxs-lookup"><span data-stu-id="3afae-166">On the **Format designer** page, expand **Word**, and select **SummaryLines**.</span></span>
6. <span data-ttu-id="3afae-167">Na kartě **Mapování** přidejte nový zdroj dat, abyste se za běhu uživatele zeptali, zda má být souhrnná část potlačena:</span><span class="sxs-lookup"><span data-stu-id="3afae-167">On the **Mapping** tab, add a new data source to ask the user, at runtime, whether the summary section should be suppressed:</span></span>

    1. <span data-ttu-id="3afae-168">Vyberte **Přidat kořen**.</span><span class="sxs-lookup"><span data-stu-id="3afae-168">Select **Add root**.</span></span>
    2. <span data-ttu-id="3afae-169">V dialogovém okně **Přidat zdroj dat** vyberte **Obecné\Uživatelský vstupní parametr** a otevřete dialogové okno **Vlastnosti zdroje dat „Uživatelský vstupní parametr“**.</span><span class="sxs-lookup"><span data-stu-id="3afae-169">In the **Add data source** dialog box, select **General\User input parameter** to open the **'User input parameter' data source properties** dialog box.</span></span>
    3. <span data-ttu-id="3afae-170">Do pole **Název** zadejte **uipSuppress**.</span><span class="sxs-lookup"><span data-stu-id="3afae-170">In the **Name** field, enter **uipSuppress**.</span></span>
    4. <span data-ttu-id="3afae-171">Do pole **Označení** zadejte **Potlačit část shrnutí**.</span><span class="sxs-lookup"><span data-stu-id="3afae-171">In the **Label** field, enter **Suppress summary section**.</span></span>
    5. <span data-ttu-id="3afae-172">V poli **Název provozního datového typu** vyberte nebo zadejte **NoYes**.</span><span class="sxs-lookup"><span data-stu-id="3afae-172">In the **Operations data type name** field, select or enter **NoYes**.</span></span>
    6. <span data-ttu-id="3afae-173">Vyberte **OK**.</span><span class="sxs-lookup"><span data-stu-id="3afae-173">Select **OK**.</span></span>

7. <span data-ttu-id="3afae-174">Přidání nového zdroje dat typu výčtu aplikace **NoYes**:</span><span class="sxs-lookup"><span data-stu-id="3afae-174">Add a new data source of the **NoYes** application enumeration type:</span></span>

    1. <span data-ttu-id="3afae-175">Vyberte **Přidat kořen**.</span><span class="sxs-lookup"><span data-stu-id="3afae-175">Select **Add root**.</span></span>
    2. <span data-ttu-id="3afae-176">V dialogovém okně **Přidat zdroj dat** vyberte **Dynamics 365 for Operations\Výčet** k otevření dialogového okna **Vlastnosti zdroje dat „výčet“**.</span><span class="sxs-lookup"><span data-stu-id="3afae-176">In the **Add data source** dialog box, select **Dynamics 365 for Operations\Enumeration** to open the **'Enumeration' data source properties** dialog box.</span></span>
    3. <span data-ttu-id="3afae-177">Do pole **Název** zadejte **enumNoYes**.</span><span class="sxs-lookup"><span data-stu-id="3afae-177">In the **Name** field, enter **enumNoYes**.</span></span>
    4. <span data-ttu-id="3afae-178">Do pole **Označení** zadejte **Potlačit možnosti**.</span><span class="sxs-lookup"><span data-stu-id="3afae-178">In the **Label** field, enter **Suppress options**.</span></span>
    5. <span data-ttu-id="3afae-179">V poli **Název provozního datového typu** vyberte nebo zadejte **NoYes**.</span><span class="sxs-lookup"><span data-stu-id="3afae-179">In the **Operations data type name** field, select or enter **NoYes**.</span></span>
    6. <span data-ttu-id="3afae-180">Vyberte **OK**.</span><span class="sxs-lookup"><span data-stu-id="3afae-180">Select **OK**.</span></span>

8. <span data-ttu-id="3afae-181">Pro vybraný prvek formátu **Souhrnné řádky** nakonfigurujte vzorec tak, aby určoval, kdy má být potlačen ovládací prvek obsahu Word, který je přidružen k vybranému prvku formátu:</span><span class="sxs-lookup"><span data-stu-id="3afae-181">For the selected **SummaryLines** format element, configure the formula to specify when the Word content control that is associated with the selected format element should be suppressed:</span></span>

    1. <span data-ttu-id="3afae-182">Na kartě **Mapování** v části **Odstraněno** vyberte **Upravit** k otevření stránky **[Návrhář vzorců](general-electronic-reporting-formula-designer.md)**.</span><span class="sxs-lookup"><span data-stu-id="3afae-182">On the **Mapping** tab, in the **Removed** section, select **Edit** to open the **[Formula designer](general-electronic-reporting-formula-designer.md)** page.</span></span>
    2. <span data-ttu-id="3afae-183">V poli **Vzorec** zadejte vzorec `uipSuppress = enumNoYes.Yes`.</span><span class="sxs-lookup"><span data-stu-id="3afae-183">In the **Formula** field, enter the formula `uipSuppress = enumNoYes.Yes`.</span></span>
    3. <span data-ttu-id="3afae-184">Vyberte **Uložit** a zavřete stránku **Návrhář vzorců**.</span><span class="sxs-lookup"><span data-stu-id="3afae-184">Select **Save**, and close the **Formula designer** page.</span></span>

        > [!NOTE]
        > <span data-ttu-id="3afae-185">Tento vzorec se použije na vygenerovaný dokument **po spuštění všech ostatních prvků formátu**.</span><span class="sxs-lookup"><span data-stu-id="3afae-185">This formula will be applied to a generated document **after all other format elements are run**.</span></span> <span data-ttu-id="3afae-186">Chcete-li použít tento vzorec, ovládací prvek obsahu Word, který je označen jako prvek formátu, pro který je vzorec nakonfigurován (**SummaryLines** v tomto případě) se nachází ve vygenerovaném dokumentu.</span><span class="sxs-lookup"><span data-stu-id="3afae-186">To apply this formula, a Word content control that is tagged as a format element that the formula is configured for (**SummaryLines** in this case) is found in a generated document.</span></span> <span data-ttu-id="3afae-187">Tento ovládací prvek obsahu je poté zcela odstraněn společně s řádkem v tabulce Word, který ho obsahuje.</span><span class="sxs-lookup"><span data-stu-id="3afae-187">That content control is then completely removed, together with the row in the Word table that holds it.</span></span> <span data-ttu-id="3afae-188">Řádek podrobností části souhrnu je odstraněn z vygenerovaného dokumentu.</span><span class="sxs-lookup"><span data-stu-id="3afae-188">The details row of the summary section is removed from the generated document.</span></span>
        >
        > <span data-ttu-id="3afae-189">V době návrhu můžete nakonfigurovat vzorec **Odstraněno** pro prvek formátu, přestože žádný ovládací prvek obsahu v šabloně Word, který používáte, nemá značku, která odpovídá názvu prvku formátu, pro který je vlastnost **Odstraněno** nakonfigurována.</span><span class="sxs-lookup"><span data-stu-id="3afae-189">At design time, you might configure the **Removed** formula for a format element, even though no content control in the Word template that you're using has a tag that matches the name of a format element that the **Removed** property is configured for.</span></span> <span data-ttu-id="3afae-190">Když ověříte formát v době návrhu, obdržíte a [varování](er-components-inspections.md#i14) o této nesrovnalosti.</span><span class="sxs-lookup"><span data-stu-id="3afae-190">When you validate the format at design time, you receive a [warning](er-components-inspections.md#i14) about this inconsistency.</span></span>
        >
        > <span data-ttu-id="3afae-191">Za běhu je vyvolána výjimka, pokud žádný ovládací prvek obsahu v šabloně Word, který používáte, nemá značku, která odpovídá názvu prvku formátu, pro který je **odstraněná** nakonfigurována.</span><span class="sxs-lookup"><span data-stu-id="3afae-191">At runtime, an exception is thrown if no content control in the Word template that you're using has a tag that matches the name of a format element that the **Removed** property is configured for.</span></span>

    4. <span data-ttu-id="3afae-192">Na kartě **Mapování** v části **Odstraněno** nastavte možnost **S nadřazeným** na **Ano**.</span><span class="sxs-lookup"><span data-stu-id="3afae-192">On the **Mapping** tab, in the **Removed** section, set the **With parent** option to **Yes**.</span></span>

        > [!NOTE]
        > <span data-ttu-id="3afae-193">Tuto možnost musíte nastavit na **Ano**, abyste odebrali celou tabulku Word jako nadřazený objekt řádku, který obsahuje podrobnosti souhrnné sekce.</span><span class="sxs-lookup"><span data-stu-id="3afae-193">You must set this option to **Yes** to remove the whole Word table as the parent object of the row that holds the summary section details.</span></span> <span data-ttu-id="3afae-194">Pokud nastavíte tuto možnost na **Ne**, řádek záhlaví sekce zůstane v generovaném dokumentu.</span><span class="sxs-lookup"><span data-stu-id="3afae-194">If you set this option to **No**, the section header row remains in the generated document.</span></span>

9. <span data-ttu-id="3afae-195">Změny upravitelného formátu uložíte výběrem možnosti **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="3afae-195">Select **Save** to save your changes to the editable format.</span></span>

    ![Generovaný výstup ve formátu Word](./media/er-design-configuration-word-suppress-controls-image3.gif)

## <a name="run-the-modified-format-to-create-word-output"></a><span data-ttu-id="3afae-197">Spuštění upraveného formátu pro vytvoření výstupu ve Wordu</span><span class="sxs-lookup"><span data-stu-id="3afae-197">Run the modified format to create Word output</span></span>

1. <span data-ttu-id="3afae-198">Přejděte na **Závazky** \> **Platby** \> **Deník plateb**.</span><span class="sxs-lookup"><span data-stu-id="3afae-198">Go to **Accounts payable** \> **Payments** \> **Payment journal**.</span></span>
2. <span data-ttu-id="3afae-199">Vyberte deník plateb, který jste vytvořili, a poté vyberte **Řádky**.</span><span class="sxs-lookup"><span data-stu-id="3afae-199">Select the payment journal that you created, and then select **Lines**.</span></span>
3. <span data-ttu-id="3afae-200">Na stránce **Platby dodavatele** vyberte všechny řádky a poté vyberte **Stav platby** \> **Žádný**.</span><span class="sxs-lookup"><span data-stu-id="3afae-200">On the **Vendor payments** page, select all the rows, and then select **Payment status** \> **None**.</span></span>
4. <span data-ttu-id="3afae-201">Vyberte **Generovat platby**.</span><span class="sxs-lookup"><span data-stu-id="3afae-201">Select **Generate payments**.</span></span>
5. <span data-ttu-id="3afae-202">V poli **Způsob platby** vyberte **Elektronický**.</span><span class="sxs-lookup"><span data-stu-id="3afae-202">In the **Method of payment** field, select **Electronic**.</span></span>
6. <span data-ttu-id="3afae-203">V poli **Bankovní účet** vyberte **GBSI OPER**.</span><span class="sxs-lookup"><span data-stu-id="3afae-203">In the **Bank account** field, select **GBSI OPER**.</span></span>
7. <span data-ttu-id="3afae-204">Vyberte **OK**.</span><span class="sxs-lookup"><span data-stu-id="3afae-204">Select **OK**.</span></span>
8. <span data-ttu-id="3afae-205">V dialogovém okně **Parametry elektronického přiznání** v poli **Potlačit část shrnutí** vyberte **Ano**.</span><span class="sxs-lookup"><span data-stu-id="3afae-205">In the **Electronic report parameters** dialog box, in the **Suppress summary section** field, select **Yes**.</span></span>
9. <span data-ttu-id="3afae-206">Vyberte **OK** a analyzujte vygenerovaný výstup.</span><span class="sxs-lookup"><span data-stu-id="3afae-206">Select **OK**, and analyze the generated output.</span></span>

    ![Generovaný výstup ve formátu Word](./media/er-design-configuration-word-suppress-controls-image4.gif)

    <span data-ttu-id="3afae-208">Všimněte si, že výstup neobsahuje souhrnnou část, protože byla potlačena.</span><span class="sxs-lookup"><span data-stu-id="3afae-208">Notice that the output doesn't contain the summary section, because it has been suppressed.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="3afae-209">Další prostředky</span><span class="sxs-lookup"><span data-stu-id="3afae-209">Additional resources</span></span>

- [<span data-ttu-id="3afae-210">Návrh konfigurace pro generování sestav ve formátu OPENXML</span><span class="sxs-lookup"><span data-stu-id="3afae-210">Design a configuration for generating reports in OPENXML format</span></span>](./tasks/er-design-reports-openxml-2016-11.md)
- [<span data-ttu-id="3afae-211">Návrh nové konfigurace elektronického výkaznictví pro generování sestav ve formátu Word</span><span class="sxs-lookup"><span data-stu-id="3afae-211">Design a new ER configuration to generate reports in Word format</span></span>](er-design-configuration-word.md)
- [<span data-ttu-id="3afae-212">Opětovné použití konfigurací elektronického výkaznictví s šablonami Excel pro generování sestav ve formátu Word</span><span class="sxs-lookup"><span data-stu-id="3afae-212">Re-use ER configurations with Excel templates to generate reports in Word format</span></span>](./tasks/er-design-configuration-word-2016-11.md)
- [<span data-ttu-id="3afae-213">Kontrola konfigurované komponenty ER zabraňující problémům za běhu</span><span class="sxs-lookup"><span data-stu-id="3afae-213">Inspect the configured ER component to prevent runtime issues</span></span>](er-components-inspections.md#i14)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]