---
title: Opětovné použití konfigurace ER se šablonami aplikace Excel ke generování zpráv ve formátu Word
description: Toto téma popisuje, jak lze konfigurovat formáty sestav, které byly navrženy ke generování sestav jako sešitů aplikace Excel, aby generovaly sestavy jako dokumenty Word.
author: NickSelin
ms.date: 01/11/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ERWorkspace, ERSolutionTable, EROperationDesigner, LedgerJournalTable, LedgerJournalTransVendPaym
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 728984678d78cf626e2b30222f1d1e603e05d117
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/31/2021
ms.locfileid: "5755051"
---
# <a name="reuse-er-configurations-with-excel-templates-to-generate-reports-in-word-format"></a><span data-ttu-id="769c4-103">Opětovné použití konfigurace ER se šablonami aplikace Excel ke generování zpráv ve formátu Word</span><span class="sxs-lookup"><span data-stu-id="769c4-103">Reuse ER configurations with Excel templates to generate reports in Word format</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="769c4-104">Pokud chcete generovat sestavy jako dokumenty Microsoft Word, můžete [nakonfigurovat](../er-design-configuration-word.md) nový [formát elektronického výkaznictví (ER)](../general-electronic-reporting.md) [formát](../general-electronic-reporting.md#FormatComponentOutbound).</span><span class="sxs-lookup"><span data-stu-id="769c4-104">To generate reports as Microsoft Word documents, you can [configure](../er-design-configuration-word.md) a new [Electronic reporting (ER)](../general-electronic-reporting.md) [format](../general-electronic-reporting.md#FormatComponentOutbound).</span></span> <span data-ttu-id="769c4-105">Alternativně můžete znovu použít formát ER, který byl původně navržen pro generování sestav jako sešity aplikace Excel.</span><span class="sxs-lookup"><span data-stu-id="769c4-105">Alternatively, you can reuse an ER format that was originally designed to generate reports as Excel workbooks.</span></span> <span data-ttu-id="769c4-106">V takovém případě musíte nahradit šablonu aplikace Excel šablonou aplikace Word.</span><span class="sxs-lookup"><span data-stu-id="769c4-106">In this case, you must replace the Excel template with a Word template.</span></span>

<span data-ttu-id="769c4-107">Následující postupy ukazují, jak může uživatel v roli správce systému nebo v roli vývojáře elektronických sestav konfigurovat formát ER tak, aby generoval sestavy jako soubory Word, a to opětovným použitím formátu ER, který byl navržen pro generování sestav jako souborů Excel.</span><span class="sxs-lookup"><span data-stu-id="769c4-107">The following procedures show how a user in either the System administrator role or the Electronic reporting developer role can configure an ER format to generate reports as Word files by reusing an ER format that was designed to generate reports as Excel files.</span></span>

<span data-ttu-id="769c4-108">Tyto postupy lze provést v rámci společnosti GBSI.</span><span class="sxs-lookup"><span data-stu-id="769c4-108">These procedures can be completed in the GBSI company.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="769c4-109">Předpoklady</span><span class="sxs-lookup"><span data-stu-id="769c4-109">Prerequisites</span></span>

<span data-ttu-id="769c4-110">Pro dokončení těchto postupů musíte nejprve provést kroky v průvodci záznamem úloh [Návrh konfigurace ke generování sestav ve formátu OPENXML](er-design-reports-openxml-2016-11.md).</span><span class="sxs-lookup"><span data-stu-id="769c4-110">To complete these procedures, you must first follow the steps in the [Design a configuration for generating reports in OPENXML format](er-design-reports-openxml-2016-11.md) task guide.</span></span>

<span data-ttu-id="769c4-111">Musíte si také stáhnout a místně uložit následující šablony pro vzorovou sestavu:</span><span class="sxs-lookup"><span data-stu-id="769c4-111">You must also download and locally save the following templates for the sample report:</span></span>

- [<span data-ttu-id="769c4-112">Šablona sestavy platby (SampleVendPaymDocReport.docx)</span><span class="sxs-lookup"><span data-stu-id="769c4-112">Template of Payment Report (SampleVendPaymDocReport.docx)</span></span>](https://go.microsoft.com/fwlink/?linkid=862266)
- [<span data-ttu-id="769c4-113">Vázaná šablona sestavy platby (SampleVendPaymDocReportBounded.docx)</span><span class="sxs-lookup"><span data-stu-id="769c4-113">Bounded Template of Payment Report (SampleVendPaymDocReportBounded.docx)</span></span>](https://go.microsoft.com/fwlink/?linkid=862266)

<span data-ttu-id="769c4-114">Tyto postupy jsou pro funkci, která byla přidána do Dynamics 365 for Operations verze 1611 (listopad 2016).</span><span class="sxs-lookup"><span data-stu-id="769c4-114">These procedures are for a feature that was added in Dynamics 365 for Operations version 1611 (November 2016).</span></span>

## <a name="select-the-existing-er-report-configuration"></a><span data-ttu-id="769c4-115">Volba existující konfigurace sestavy ER</span><span class="sxs-lookup"><span data-stu-id="769c4-115">Select the existing ER report configuration</span></span>

1. <span data-ttu-id="769c4-116">V Dynamics 365 Finance přejděte na **Správa organizace** \> **Pracovní prostory** \> **Elektronické výkaznictví**.</span><span class="sxs-lookup"><span data-stu-id="769c4-116">In Dynamics 365 Finance, go to **Organization administration** \> **Workspaces** \> **Electronic reporting**.</span></span>
2. <span data-ttu-id="769c4-117">Ujistěte se, že je poskytovatel konfigurace **Litware, Inc.** vybrán jako **Aktivní**.</span><span class="sxs-lookup"><span data-stu-id="769c4-117">Make sure that the **Litware, Inc.** configuration provider is selected as **Active**.</span></span> <span data-ttu-id="769c4-118">Pokud tomu tak není, postupujte podle pokynů v průvodci záznamem úloh [Vytvoření poskytovatelů konfigurace a jejich označení jako aktivních](er-configuration-provider-mark-it-active-2016-11.md).</span><span class="sxs-lookup"><span data-stu-id="769c4-118">If it isn't, follow the steps in the [Create configuration providers and mark them as active](er-configuration-provider-mark-it-active-2016-11.md) task guide.</span></span>
3. <span data-ttu-id="769c4-119">Vyberte **Konfigurace vykazování**.</span><span class="sxs-lookup"><span data-stu-id="769c4-119">Select **Reporting configurations**.</span></span> <span data-ttu-id="769c4-120">Znovu použijete existující konfiguraci ER, která byla původně navržena ke generování výstupu sestavy ve formátu OPENXML.</span><span class="sxs-lookup"><span data-stu-id="769c4-120">You will reuse the existing ER configuration that was designed to generate the report output in OPENXML format.</span></span>
4. <span data-ttu-id="769c4-121">Na stránce **Konfigurace** ve stromu konfigurací v levém podokně rozbalte položku **Model platby** a poté vyberte možnost **Vzorová sestava listu**.</span><span class="sxs-lookup"><span data-stu-id="769c4-121">On the **Configurations** page, in the configuration tree in the left pane, expand **Payment model**, and select **Sample worksheet report**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="769c4-122">Verzi konceptu vybraného formátu ER lze upravit na kartě s náhledem **Verze**.</span><span class="sxs-lookup"><span data-stu-id="769c4-122">The draft version of the selected ER format can be edited on the **Versions** FastTab.</span></span>

5. <span data-ttu-id="769c4-123">Vyberte možnost **Návrhář**.</span><span class="sxs-lookup"><span data-stu-id="769c4-123">Select **Designer**.</span></span>
6. <span data-ttu-id="769c4-124">Na stránce **Návrhář formátů** si všimněte, že nadpis prvku kořenového formátu označuje, že je aktuálně používána šablona aplikace Excel.</span><span class="sxs-lookup"><span data-stu-id="769c4-124">On the **Format designer** page, notice that the title of the root format element indicates that an Excel template is currently used.</span></span>

![Výběr existující konfigurace sestavy ER](../media/er-design-configuration-word-2016-11-image01.gif)

## <a name="review-the-downloaded-word-template"></a><span data-ttu-id="769c4-126">Kontrola stažené šablony Wordu</span><span class="sxs-lookup"><span data-stu-id="769c4-126">Review the downloaded Word template</span></span>

1. <span data-ttu-id="769c4-127">V desktopové aplikaci Word otevřete soubor šablony **SampleVendPaymDocReport.docx**, který jste stáhli dříve.</span><span class="sxs-lookup"><span data-stu-id="769c4-127">In the Word desktop application, open the **SampleVendPaymDocReport.docx** template file that you downloaded earlier.</span></span>
2. <span data-ttu-id="769c4-128">Ověřte, že tato šablona obsahuje pouze rozvržení dokumentu, který chcete generovat jako ER výstup.</span><span class="sxs-lookup"><span data-stu-id="769c4-128">Verify that the template contains only the layout of the document that you want to generate as ER output.</span></span>

![Rozvržení šablony Word v desktopové aplikaci](../media/er-design-configuration-word-2016-11-image02.png)

## <a name="replace-the-excel-template-with-the-word-template-and-add-a-custom-xml-part"></a><span data-ttu-id="769c4-130">Nahrazení šablony aplikace Excel šablonou aplikace Word a přidání vlastní části XML</span><span class="sxs-lookup"><span data-stu-id="769c4-130">Replace the Excel template with the Word template and add a custom XML part</span></span>

<span data-ttu-id="769c4-131">V současné době se používá dokument Excel jako šablona pro generování výstupu ve formátu OPENXML.</span><span class="sxs-lookup"><span data-stu-id="769c4-131">Currently, the Excel document is used as a template to generate the output in OPENXML format.</span></span> <span data-ttu-id="769c4-132">Tuto šablonu nahradíte souborem šablony Word SampleVendPaymDocReport.docx Word, kterou jste předtím stáhli.</span><span class="sxs-lookup"><span data-stu-id="769c4-132">You will replace this template with the SampleVendPaymDocReport.docx Word template file that you downloaded earlier.</span></span> <span data-ttu-id="769c4-133">Také provedete rozšíření šablony aplikace Word přidáním vlastní části XML.</span><span class="sxs-lookup"><span data-stu-id="769c4-133">You will also extend the Word template by adding a custom XML part.</span></span>

1. <span data-ttu-id="769c4-134">V modulu Finance na stránce **Návrhář formátu** na kartě **Formát** vyberte **Přílohy**.</span><span class="sxs-lookup"><span data-stu-id="769c4-134">In Finance, on the **Format designer** page, on the **Format** tab, select **Attachments**.</span></span>
2. <span data-ttu-id="769c4-135">Na stránce **Přílohy** vyberte **Odstranit** pro odebrání existující šablony Excel.</span><span class="sxs-lookup"><span data-stu-id="769c4-135">On the **Attachments** page, select **Delete** to remove the existing Excel template.</span></span> <span data-ttu-id="769c4-136">Vyberte **Ano**, chcete-li potvrdit změnu.</span><span class="sxs-lookup"><span data-stu-id="769c4-136">Select **Yes** to confirm the change.</span></span>
3. <span data-ttu-id="769c4-137">Vyberte **Nový** \> **Soubor**.</span><span class="sxs-lookup"><span data-stu-id="769c4-137">Select **New** \> **File**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="769c4-138">Musíte vybrat typ dokumentu, který je [konfigurován](../electronic-reporting-er-configure-parameters.md#parameters-to-manage-documents) v parametrech ER k uložení šablon formátů ER.</span><span class="sxs-lookup"><span data-stu-id="769c4-138">You must select a document type that has been [configured](../electronic-reporting-er-configure-parameters.md#parameters-to-manage-documents) in the ER parameters to store templates of ER formats.</span></span>

4. <span data-ttu-id="769c4-139">Vyberte **Procházet** a poté přejděte na a vyberte soubor **SampleVendPaymDocReport.docx**, který jste stáhli dříve.</span><span class="sxs-lookup"><span data-stu-id="769c4-139">Select **Browse**, and then browse to and select the **SampleVendPaymDocReport.docx** file that you downloaded earlier.</span></span>
5. <span data-ttu-id="769c4-140">Vyberte **OK**.</span><span class="sxs-lookup"><span data-stu-id="769c4-140">Select **OK**.</span></span>
6. <span data-ttu-id="769c4-141">Zavřete stránku **Přílohy**.</span><span class="sxs-lookup"><span data-stu-id="769c4-141">Close the **Attachments** page.</span></span>
7. <span data-ttu-id="769c4-142">Na stránce **Návrhář formátu** v poli **Šablona** zadejte nebo vyberte soubor **SampleVendPaymDocReport.docx** k použití této šablony Word místo šablony Excel, která byla použita předtím.</span><span class="sxs-lookup"><span data-stu-id="769c4-142">On the **Format designer** page, in the **Template** field, enter or select the **SampleVendPaymDocReport.docx** file to use that Word template instead of the Excel template that was previously used.</span></span>
8. <span data-ttu-id="769c4-143">Zvolte **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="769c4-143">Select **Save**.</span></span>

    <span data-ttu-id="769c4-144">Kromě uložení změn v konfiguraci aktualizuje připojenou šablonu aplikace Word rovněž akce **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="769c4-144">In addition to storing configuration changes, the **Save** action updates the attached Word template.</span></span> <span data-ttu-id="769c4-145">Hierarchická struktura navrženého formátu je přenesena do připojeného dokumentu aplikace Word jako nová vlastní část XML s názvem **Sestava**.</span><span class="sxs-lookup"><span data-stu-id="769c4-145">The hierarchical structure of the designed format is added to the attached Word document as a new custom XML part that is named **Report**.</span></span> <span data-ttu-id="769c4-146">Všimněte si, že připojená šablona aplikace Word obsahuje nejen rozvržení dokumentu, který bude generován jako výstup ER, ale zároveň i strukturu dat, která budou ER předána do této šablony za běhu.</span><span class="sxs-lookup"><span data-stu-id="769c4-146">The attached Word template contains the layout of the document that will be generated as ER output and the structure of data that ER will enter in that template at runtime.</span></span>

9. <span data-ttu-id="769c4-147">Všimněte si, že nadpis prvku kořenového formátu označuje, že je aktuálně používána šablona aplikace Word.</span><span class="sxs-lookup"><span data-stu-id="769c4-147">Notice that the title of the root format element indicates that a Word template is currently used.</span></span>

    ![Nahrazení šablony aplikace Excel šablonou aplikace Word a přidání vlastní části XML](../media/er-design-configuration-word-2016-11-image03.gif)

10. <span data-ttu-id="769c4-149">Na kartě **Formát** vyberte **Přílohy**.</span><span class="sxs-lookup"><span data-stu-id="769c4-149">On the **Format** tab, select **Attachments**.</span></span>

<span data-ttu-id="769c4-150">Nyní můžete namapovat prvky vybrané vlastní části XML **Sestava** a ovládacích prvků obsahu dokumentu aplikace Word.</span><span class="sxs-lookup"><span data-stu-id="769c4-150">You can now map the elements of the **Report** custom XML part to the content controls of the Word document.</span></span>

<span data-ttu-id="769c4-151">okud jste obeznámeni s dokumenty Word, které lze navrhovat jako formuláře obsahující [ovládací prvky obsahu](https://docs.microsoft.com/office/client-developer/word/content-controls-in-word) namapované na prvky [vlastních částí XML](https://docs.microsoft.com/visualstudio/vsto/custom-xml-parts-overview?view=vs-2019), proveďte všechny kroky dalšího dílčího úkolu pro vytvoření takového dokumentu.</span><span class="sxs-lookup"><span data-stu-id="769c4-151">If you're familiar with the process of designing Word documents as forms that contain [content controls](https://docs.microsoft.com/office/client-developer/word/content-controls-in-word) that are mapped to elements of [custom XML parts](https://docs.microsoft.com/visualstudio/vsto/custom-xml-parts-overview?view=vs-2019), complete all steps in the next procedure to create the document.</span></span> <span data-ttu-id="769c4-152">Další informace naleznete v tématu [Vytvoření formulářů, které uživatelé dokončí nebo vytisknou v aplikaci Word](https://support.office.com/article/Create-forms-that-users-complete-or-print-in-Word-040c5cc1-e309-445b-94ac-542f732c8c8b).</span><span class="sxs-lookup"><span data-stu-id="769c4-152">For more information, see [Create forms that users complete or print in Words](https://support.office.com/article/Create-forms-that-users-complete-or-print-in-Word-040c5cc1-e309-445b-94ac-542f732c8c8b).</span></span> <span data-ttu-id="769c4-153">Jinak následující postup přeskočte.</span><span class="sxs-lookup"><span data-stu-id="769c4-153">Otherwise, skip the next procedure.</span></span>

## <a name="get-a-word-document-that-has-a-custom-xml-part-and-do-data-mapping"></a><a id='get-word-doc'></a><span data-ttu-id="769c4-154">Získání dokumentu Word, který má vlastní část XML, a mapování dat</span><span class="sxs-lookup"><span data-stu-id="769c4-154">Get a Word document that has a custom XML part and do data mapping</span></span>

1. <span data-ttu-id="769c4-155">Ve Finance na stránce **Přílohy** vyberte **Otevřít** ke stažení vybrané šablony z Finance a jejímu místnímu uložení jako dokumentu Word.</span><span class="sxs-lookup"><span data-stu-id="769c4-155">In Finance, on the **Attachments** page, select **Open** to download the selected template from Finance and store it locally as a Word document.</span></span>
3. <span data-ttu-id="769c4-156">V desktopové aplikaci Word otevřete dokument, který jste právě stáhli.</span><span class="sxs-lookup"><span data-stu-id="769c4-156">In the Word desktop application, open the document that you just downloaded.</span></span>
4. <span data-ttu-id="769c4-157">Na kartě **Vývojář** vyberte **podokno mapování XML**.</span><span class="sxs-lookup"><span data-stu-id="769c4-157">On the **Developer** tab, select **XML Mapping Pane**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="769c4-158">Pokud se karta **Vývojář** nezobrazí na pásu karet, přizpůsobte jej a přidejte ji.</span><span class="sxs-lookup"><span data-stu-id="769c4-158">If the **Developer** tab doesn't appear on the ribbon, customize the ribbon to add it.</span></span>

5. <span data-ttu-id="769c4-159">V podokně **Mapování XML** v poli **Vlastní část XML** vyberte část Vlastní XML **Sestava**.</span><span class="sxs-lookup"><span data-stu-id="769c4-159">In the **XML Mapping** pane, in the **Custom XML Part** field, select the **Report** custom XML part.</span></span>
6. <span data-ttu-id="769c4-160">Namapujte prvky vybrané vlastní části XML **Sestava** a ovládací prvky obsahu dokumentu aplikace Word.</span><span class="sxs-lookup"><span data-stu-id="769c4-160">Map the elements of the selected **Report** custom XML part and the content controls of the Word document.</span></span>
7. <span data-ttu-id="769c4-161">Aktualizovaný dokument Word uložte místně jako **SampleVendPaymDocReportBounded.docx**.</span><span class="sxs-lookup"><span data-stu-id="769c4-161">Save the updated Word document locally as **SampleVendPaymDocReportBounded.docx**.</span></span>

## <a name="review-the-word-template-where-the-custom-xml-part-is-mapped-to-content-controls"></a><span data-ttu-id="769c4-162">Zkontrolujte šablonu Word, kde je vlastní část XML namapována na ovládací prvky obsahu</span><span class="sxs-lookup"><span data-stu-id="769c4-162">Review the Word template where the custom XML part is mapped to content controls</span></span>

1. <span data-ttu-id="769c4-163">V desktopové aplikaci Word otevřete soubor šablony **SampleVendPaymDocReportBounded.docx**, který jste stáhli dříve.</span><span class="sxs-lookup"><span data-stu-id="769c4-163">In the Word desktop application, open the **SampleVendPaymDocReportBounded.docx** template file.</span></span>
2. <span data-ttu-id="769c4-164">Ověřte, že tato šablona obsahuje rozvržení dokumentu, který chcete generovat jako ER výstup.</span><span class="sxs-lookup"><span data-stu-id="769c4-164">Verify that the template contains the layout of the document that you want to generate as ER output.</span></span> <span data-ttu-id="769c4-165">Ovládací prvky obsahu, které se používají jako zástupné symboly pro data, která ER za běhu zadá do této šablony, jsou založeny na mapování, která jsou konfigurována mezi vlastní částí XML **Sestava** a ovládacími prvky obsahu dokumentu Word.</span><span class="sxs-lookup"><span data-stu-id="769c4-165">The content controls that are used as placeholders for data that ER will enter in this template at runtime are based on the mappings that are configured between elements of the **Report** custom XML part and the content controls of the Word document.</span></span>

![Náhled šablony Word v desktopové aplikaci](../media/er-design-configuration-word-2016-11-image04.png)

## <a name="upload-the-word-template-where-the-custom-xml-part-is-mapped-to-content-controls"></a><span data-ttu-id="769c4-167">Nahrajte šablonu Word, kde je vlastní část XML namapována na ovládací prvky obsahu</span><span class="sxs-lookup"><span data-stu-id="769c4-167">Upload the Word template where the custom XML part is mapped to content controls</span></span>

1. <span data-ttu-id="769c4-168">Ve Finance na stránce **Přílohy** vyberte **Odstranit** k odebrání šablony Word, která nemá mapování mezi prvky vlastní části XML **Sestava** a ovládacími prvky obsahu.</span><span class="sxs-lookup"><span data-stu-id="769c4-168">In Finance, on the **Attachments** page, select **Delete** to remove the Word template that has no mappings between elements of the **Report** custom XML part and content controls.</span></span> <span data-ttu-id="769c4-169">Vyberte **Ano**, chcete-li potvrdit změnu.</span><span class="sxs-lookup"><span data-stu-id="769c4-169">Select **Yes** to confirm the change.</span></span>
2. <span data-ttu-id="769c4-170">Výběrem možností **Nový** \> **Soubor** přidejte nový soubor šablony, který obsahuje mapování mezi vlastním prvkem XML **Sestava** a ovládacími prvky obsahu.</span><span class="sxs-lookup"><span data-stu-id="769c4-170">Select **New** \> **File** to add a new template file that contains mappings between elements of the **Report** custom XML part and content controls.</span></span>

    > [!NOTE]
    > <span data-ttu-id="769c4-171">Musíte vybrat typ dokumentu, který je [konfigurován](../electronic-reporting-er-configure-parameters.md#parameters-to-manage-documents) v parametrech ER k uložení šablon formátů ER.</span><span class="sxs-lookup"><span data-stu-id="769c4-171">You must select a document type that has been [configured](../electronic-reporting-er-configure-parameters.md#parameters-to-manage-documents) in the ER parameters to store templates of ER formats.</span></span>

3. <span data-ttu-id="769c4-172">Vyberte **Procházet** a poté přejděte na a vyberte soubor **SampleVendPaymDocReportBounded.docx**, který jste stáhli nebo připravili pomocí dokončení postupu v části [Získání souboru Word, který má vlastní část XML k mapování](#get-word-doc).</span><span class="sxs-lookup"><span data-stu-id="769c4-172">Select **Browse**, and then browse to and select the **SampleVendPaymDocReportBounded.docx** file that you downloaded or prepared by completing the procedure in the [Get a Word that has a custom XML part to do data mapping](#get-word-doc) section.</span></span>
4. <span data-ttu-id="769c4-173">Vyberte **OK**.</span><span class="sxs-lookup"><span data-stu-id="769c4-173">Select **OK**.</span></span>
5. <span data-ttu-id="769c4-174">Zavřete stránku **Přílohy**.</span><span class="sxs-lookup"><span data-stu-id="769c4-174">Close the **Attachments** page.</span></span>
6. <span data-ttu-id="769c4-175">Na stránce **Návrhář formátů** v poli **Šablona** vyberte dokument, který jste právě stáhli.</span><span class="sxs-lookup"><span data-stu-id="769c4-175">On the **Format designer** page, in the **Template** field, select the document that you just downloaded.</span></span>
7. <span data-ttu-id="769c4-176">Zvolte **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="769c4-176">Select **Save**.</span></span>
8. <span data-ttu-id="769c4-177">Zavřete stránku **Návrhář formátu**.</span><span class="sxs-lookup"><span data-stu-id="769c4-177">Close the **Format designer** page.</span></span>

## <a name="mark-the-configured-format-as-runnable"></a><span data-ttu-id="769c4-178">Označení nakonfigurovaného formátu jako spustitelného</span><span class="sxs-lookup"><span data-stu-id="769c4-178">Mark the configured format as runnable</span></span>

<span data-ttu-id="769c4-179">Chcete-li spustit rámcovou verzi upravitelného formátu, musíte ji nastavit jako [spustitelnou](../er-quick-start2-customize-report.md#MarkFormatRunnable).</span><span class="sxs-lookup"><span data-stu-id="769c4-179">To run the draft version of the editable format, you must make it [runnable](../er-quick-start2-customize-report.md#MarkFormatRunnable).</span></span>

1. <span data-ttu-id="769c4-180">V aplikaci Finance na stránce **Konfigurace** v podokně akcí na kartě **Konfigurace** ve skupině **Pokročilá nastavení** vyberte **Parametry uživatelů**.</span><span class="sxs-lookup"><span data-stu-id="769c4-180">In Finance, on the **Configurations** page, on the Action Pane, on the **Configurations** tab, in the **Advanced settings** group, select **User parameters**.</span></span>
2. <span data-ttu-id="769c4-181">V dialogovém okně **Uživatelské parametry** nastavte u možnosti **Spustit nastavení** hodnotu **Ano** a poté stiskněte **OK**.</span><span class="sxs-lookup"><span data-stu-id="769c4-181">In the **User parameters** dialog box, set the **Run settings** option to **Yes**, and then select **OK**.</span></span>
3. <span data-ttu-id="769c4-182">Je-li třeba vyberte možnost **Upravit**, má-li být aktuální stránka editovatelná.</span><span class="sxs-lookup"><span data-stu-id="769c4-182">Select **Edit** to make the current page editable, as required.</span></span>
4. <span data-ttu-id="769c4-183">Pro aktuálně vybranou konfiguraci **Ukázková sestava listu** nastavte možnost **Spustit koncept** na **Ano**.</span><span class="sxs-lookup"><span data-stu-id="769c4-183">For the currently selected **Sample worksheet report** configuration, set the **Run Draft** option to **Yes**.</span></span>
5. <span data-ttu-id="769c4-184">Zvolte **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="769c4-184">Select **Save**.</span></span>

## <a name="run-the-format-to-create-output-in-word-format"></a><span data-ttu-id="769c4-185">Spuštění formátu pro vytvoření výstupu ve formátu Word</span><span class="sxs-lookup"><span data-stu-id="769c4-185">Run the format to create output in Word format</span></span>

1. <span data-ttu-id="769c4-186">V modulu Finance přejděte na **Závazky** \> **Platby** \> **Deník plateb**.</span><span class="sxs-lookup"><span data-stu-id="769c4-186">In Finance, go to **Accounts payable** \> **Payments** \> **Payment journal**.</span></span>
2. <span data-ttu-id="769c4-187">V deníku plateb, který jste zadali dříve, vyberte **Řádky**.</span><span class="sxs-lookup"><span data-stu-id="769c4-187">In a payment journal that you entered earlier, select **Lines**.</span></span>
3. <span data-ttu-id="769c4-188">Na stránce **Platby dodavatele** vyberte všechny řádky v mřížce.</span><span class="sxs-lookup"><span data-stu-id="769c4-188">On the **Vendor payments** page, select all rows in the grid.</span></span>
4. <span data-ttu-id="769c4-189">Vyberte **Stav platby** \> **Žádný**.</span><span class="sxs-lookup"><span data-stu-id="769c4-189">Select **Payment status** \> **None**.</span></span>

    ![Platby za zpracování na stránce Platby dodavatele](../media/er-design-configuration-word-2016-11-image05.png)

5. <span data-ttu-id="769c4-191">V podokně akcí vyberte **Generovat platby**.</span><span class="sxs-lookup"><span data-stu-id="769c4-191">On the Action Pane, select **Generate payments**.</span></span>
6. <span data-ttu-id="769c4-192">V rozevíracím dialogovém okně proveďte následující kroky:</span><span class="sxs-lookup"><span data-stu-id="769c4-192">In the dialog box that appears, follow these steps:</span></span>

    1. <span data-ttu-id="769c4-193">V poli **Způsob platby** vyberte **Elektronický**.</span><span class="sxs-lookup"><span data-stu-id="769c4-193">In the **Method of payment** field, select **Electronic**.</span></span>
    2. <span data-ttu-id="769c4-194">V poli **Bankovní účet** vyberte **GBSI OPER**.</span><span class="sxs-lookup"><span data-stu-id="769c4-194">In the **Bank account** field, select **GBSI OPER**.</span></span>
    3. <span data-ttu-id="769c4-195">Vyberte **OK**.</span><span class="sxs-lookup"><span data-stu-id="769c4-195">Select **OK**.</span></span>

7. <span data-ttu-id="769c4-196">V dialogovém okně **Parametry elektronické sestavy** vyberte **OK**.</span><span class="sxs-lookup"><span data-stu-id="769c4-196">In the **Electronic report parameters** dialog box, select **OK**.</span></span>
8. <span data-ttu-id="769c4-197">Generovaný výstup je ve formátu aplikace Word a obsahuje podrobnosti o zpracovaných platbách.</span><span class="sxs-lookup"><span data-stu-id="769c4-197">The generated output is presented in Word format and contains the details of the processed payments.</span></span> <span data-ttu-id="769c4-198">Analyzujte vygenerovaný výstup.</span><span class="sxs-lookup"><span data-stu-id="769c4-198">Analyze the generated output.</span></span>

    ![Generovaný výstup ve formátu Word](../media/er-design-configuration-word-2016-11-image06.png)

## <a name="additional-resources"></a><span data-ttu-id="769c4-200">Další prostředky</span><span class="sxs-lookup"><span data-stu-id="769c4-200">Additional resources</span></span>

- [<span data-ttu-id="769c4-201">Návrh nové konfigurace ER pro generování sestav ve formátu Word</span><span class="sxs-lookup"><span data-stu-id="769c4-201">Design a new ER configuration to generate reports in Word format</span></span>](../er-design-configuration-word.md)
- [<span data-ttu-id="769c4-202">Integrace obrázků a tvarů v generovaných dokumentech pomocí elektronického výkaznictví</span><span class="sxs-lookup"><span data-stu-id="769c4-202">Embed images and shapes in documents that you generate by using ER</span></span>](../electronic-reporting-embed-images-shapes.md#embed-an-image-in-a-word-document)


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]